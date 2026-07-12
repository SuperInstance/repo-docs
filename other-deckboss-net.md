# deckboss-net

**Cluster:** maritime  
**Language:** TypeScript  
**Source:** [SuperInstance/deckboss-net](https://github.com/SuperInstance/deckboss-net)

## Intention

Commercial fishing fleet operations — vessel tracking, fuel monitoring, crew management, and delivery reconciliation at deckboss.net

## How It Works

**Message abstraction:**
Each message is wrapped in an envelope:

[code]

**Delivery model — At-Least-Once with idempotency:**
[code]

The receiver deduplicates by `message_id`, making the protocol idempotent — safe for retry storms.

**Backoff schedule:**
[code]

Total time to give up: ~5 minutes. This tolerates 5-minute network blackouts (typical for vessel-island occlusion).

**Priority classes:**

| Priority | Behavior | Use Case |
|----------|----------|----------|
| Critical | No backoff, immediate retry | Safety alerts |
| High | Short backoff (base 100ms) | Fleet commands |
| Normal | 

## What It's For

Commercial fishing fleet operations — vessel tracking, fuel monitoring, crew management, and delivery reconciliation at deckboss.net

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (101 lines, 4088 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Deckboss Net

**Deckboss Net** is a Rust networking library implementing reliable inter-agent message delivery over unreliable transport, designed for the SuperInstance fleet's maritime-deployed edge nodes where connectivity is intermittent and bandwidth is constrained.

## Why It Matters

Maritime and remote-edge deployments face the most challenging networking conditions: satellite connections with 500ms+ latency, VHF data links with 10⁻³ packet loss rates, and complete blackouts when vessels pass behind islands. Traditional TCP performs poorly in these conditions due to its assumption of low-latency, reliable transport — its congestion control misinterprets packet loss as network congestion, throttling throughput to unusable levels. Deckboss Net implements a message-oriented reliability layer that decouples delivery guarantees from transport: messages are acknowledged individually with exponential backoff retry, and the application is notified of delivery status rather than blocking on retransmission. This is the same architectural pattern used in naval communications systems (Link 16, AIS) and satellite IoT protocols.

## How It Works

**Message abstraction:**
Each message is wrapped in an envelope:

```
Envelope {
    message_id: UUIDv4,
    sequence: u64,
    payload: Vec<u8>,
    priority: Priority,
    ttl: Duration,
}
```

**Delivery model — At-Least-Once with idempotency:**
```
send(msg):
  envelope = wrap(msg)
  retries = 0
  while not acked(envelope.id) and retries < MAX_RETRIES:
    transmit(envelope)
    wait(backoff(retries))   // 100ms × 2^retries, cap 30s
    retries++
  notify(sender, status)
```

The receiver deduplicates by `message_id`, making the protocol idempotent — safe for retry storms.

**Backoff schedule:**
```
delay(r) = min(base × 2^r, cap)
base = 100ms, cap = 30s, MAX_RETRIES = 10
```

Total time to give up: ~5 minutes. This tolerates 5-minute network blackouts (typical for vessel-island occlusion).

**Priority classes:**

| Priority | Behavior | Use Case |
|----------|----------|----------|
| Critical | No backoff, immediate retry | Safety alerts |
| High | Short backoff (base 100ms) | Fleet commands |
| Normal | Standard backoff | Telemetry data |
| Low | Long backoff (base 1s) | Log synchronization |

**Bandwidth adaptation:** The library monitors round-trip time and adjusts send window size:

```
window = max(1, throughput_bps × RTT / average_message_size)
```

This implements a simplified congestion-control algorithm inspired by BBR (Bottleneck Bandwidth and RTT) rather than loss-based CUBIC, which performs poorly on satellite links.

## Quick Start

```rust
// The library provides transport-agnostic message envelopes.
// Usage pattern:
// 1. Create envelope with priority and TTL
// 2. Send via underlying transport (UDP, TCP, WebSocket)
// 3. Acknowledgments are handled asynchronously
// 4. Failed deliveries trigger application callbacks

fn main() {
    println!("Deckboss Net: maritime-grade message delivery
```
