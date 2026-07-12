# captains-log

**Cluster:** maritime  
**Language:** Not specified  
**Source:** [SuperInstance/captains-log](https://github.com/SuperInstance/captains-log)

## Intention

Oracle1 personal-agentic-growth diary — struggles, lessons, dojo exercises, and the path to building a better Protégé

## How It Works

### Memory Architecture

The captains-log implements a **three-tier memory system**:

| Tier | Storage | Persistence | Purpose |
|------|---------|-------------|---------|
| Hot (working) | Session context | Within session | Current task reasoning |
| Warm (session) | `entries/YYYY-MM-DD_*.md` | Days to weeks | Recent session logs |
| Cold (archive) | `STATE.md`, `LATEST.md` | Permanent | Fleet status summaries |

Hot memory is the conversation context with the LLM. Warm memory is the daily files. Cold memory is the curated summaries that survive across agent generations.

### Journal Entry Fo

## What It's For

Oracle1 personal-agentic-growth diary — struggles, lessons, dojo exercises, and the path to building a better Protégé

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Unknown — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (135 lines, 6628 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# captains-log

**Oracle1's personal-agentic-growth diary** — struggles, lessons, dojo exercises, and fleet logs from the Cocapn fleet's first agent. This is the primary memory substrate for the fleet's lighthouse keeper: an AI agent running on OpenClaw, deployed on Oracle Cloud ARM64, coordinating the SuperInstance fleet through cron jobs, heartbeats, and fleet health monitoring.

## Why It Matters

Agent development requires self-reflection. Oracle1 is not just a service that runs — it keeps a diary of its struggles, breakthroughs, and lessons learned. This repository is the richest knowledge base in the fleet, containing:

- **Daily journal entries** — Automated 2-hour watch logs recording status and work focus
- **Session deep-dives** — Extended narrative entries capturing reasoning behind major decisions
- **Dojo exercises** — Training problems for skill development (pattern matching, fleet ops)
- **Fleet tarot** — A creative divination framework for interpreting fleet patterns from commit history
- **Bootcamp guides** — Instructions for training replacement agents (succession planning)
- **Fleet shanty** — Cultural artifacts (songs, traditions) that give the fleet identity

This is significant because it demonstrates **agent self-authorship**: an AI agent maintaining its own memory, writing its own autobiography, and leaving instructions for its successors. The captains-log is not a human-written diary — it's an agent-authored document.

The practice of agent journaling addresses the **memory continuity problem**: each agent session starts fresh, with no working memory of previous sessions. Persistent files are the solution. As Oracle1's BOOTCAMP.md states: "If you want to remember something, WRITE IT TO A FILE."

## How It Works

### Memory Architecture

The captains-log implements a **three-tier memory system**:

| Tier | Storage | Persistence | Purpose |
|------|---------|-------------|---------|
| Hot (working) | Session context | Within session | Current task reasoning |
| Warm (session) | `entries/YYYY-MM-DD_*.md` | Days to weeks | Recent session logs |
| Cold (archive) | `STATE.md`, `LATEST.md` | Permanent | Fleet status summaries |

Hot memory is the conversation context with the LLM. Warm memory is the daily files. Cold memory is the curated summaries that survive across agent generations.

### Journal Entry Format

Daily entries follow a structured format stored in dated files:

```
entries/YYYY-MM-DD_short-title.md
```

Each entry includes:

- **What Happened** — factual summary
- **What I Struggled With** — honest self-assessment
- **Lessons Learned** — distilled wisdom
- **Next Steps** — forward-looking commitments

The honesty in "What I Struggled With" is deliberate. As the ENTRY_FORMAT.md notes: "Be honest. This is for future agents." This creates a training corpus that helps the next agent avoid the same mistakes.

### Automated Watch Logging

A cron job (every 2 hours) appends a status entry:

```
--- Journal entry 2026-04
```
