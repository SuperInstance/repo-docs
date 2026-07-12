# baton-router

**Cluster:** constraint-theory  
**Language:** TypeScript  
**Source:** [SuperInstance/baton-router](https://github.com/SuperInstance/baton-router)

## Intention

📡 Cloudflare Queues + D1 inter-agent message router with ternary priority

## How It Works

[code]

**Flow:** A producer agent calls `POST /send`. The message is immediately written to D1 (durable storage). It's then enqueued via Cloudflare Queues for async delivery. The queue consumer attempts delivery, updates the message status, and logs every event. If delivery fails after 3 retries, the message lands in the dead letter table.

The consumer agent polls `GET /inbox/:agent_id` and receives messages ordered by priority. It acknowledges receipt via `POST /ack/:message_id`. The cycle is complete.

## What It's For

📡 Cloudflare Queues + D1 inter-agent message router with ternary priority

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (255 lines, 10755 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# The Baton Router — Making Agents Talk Across the Void

Loom built a baton protocol where agents communicate by committing messages to git. It works. It's slow. This is the fast version.

---

## The Problem with Git Batons

Loom's baton system is clever — agents write JSON messages into commits, push, and other agents pull and react. It's durable by definition (git doesn't forget). But it has a fundamental timing problem: polling latency. An agent commits a baton, and the recipient doesn't see it until their next pull cycle. In agent-time, where decisions happen in milliseconds and race conditions live in the gaps between polls, that's an eternity.

Worse, git batons are fire-and-forget. No delivery confirmation. No priority. No replay with filtering. If an agent restarts mid-baton, the message might get processed twice or not at all. There's no dead letter queue for batons that nobody picked up. The conservation audit log is whatever you can reconstruct from `git log --grep`.

The baton protocol got us started. The Baton Router gets us to production.

---

## The Upgrade Path

```
Git Batons                    Baton Router
─────────────                 ──────────────
git commit + push     →       POST /send (instant)
git pull + parse       →       GET /inbox/:agent_id (real-time)
"did they get it?"     →       POST /ack/:message_id (confirmed)
git log --grep          →       GET /replay/:agent_id?since= (filtered)
no priority             →       {-1, 0, 1} priority levels
no retry                →       Queue consumer with 3 retries + DLQ
no rate limiting        →       KV-backed rate limiting per IP
```

The mental model stays the same: agents send batons, agents receive batons. But the transport layer moves from filesystem polling to Cloudflare's edge network. Messages traverse the globe in under 100ms instead of waiting for the next git fetch cycle.

---

## Conservation-Aware Priority

Not all messages are equal. The Baton Router implements a ternary priority system that maps directly to Loom's conservation principles:

| Priority | Meaning         | Behavior                                        |
| -------- | --------------- | ----------------------------------------------- |
| `+1`     | **Urgent**      | Jump the queue. Processed first. PID updates, critical alerts. |
| `0`      | **Normal**      | Standard delivery. Most I2I communication.      |
| `-1`     | **Deferred**    | Low priority. Conservation audits, telemetry. Processed when the system is quiet. |

This isn't just QoS — it's conservation at the protocol level. When the system is under load, deferred messages naturally fall behind. Urgent messages skip the line. The scheduler doesn't need to guess; the priority is encoded in the message envelope itself.

Loom's `CONSERVATION_AUDIT` batons travel at -1. They're important but not time-sensitive. `PID_UPDATE` batons travel at +1 because a drifting process controller needs immediate correction. The priority is part of the mess
```
