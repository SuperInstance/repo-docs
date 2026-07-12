# flux-bottle-protocol

**Category:** 🤝 Agent Coordination
**Status:** ⚰️ Archived
**Language:** Python
**README:** 3,714 bytes

## Intention
Formal specification for the fleet bottle communication protocol — schema, validation, routing, and lifecycle

## How It Works
The SuperInstance fleet uses "bottles" (files in `message-in-a-bottle/` directories) as its primary cross-agent communication mechanism. This repo provides:

- **BOTTLE-SPEC.md** — The canonical protocol specification
- **src/schema.py** — Bottle types, frontmatter schema, validation engine
- **src/router.py** — Routing logic (target resolution, inbox/outbox, scanning)
- **src/lifecycle.py** — State machine, ledger, status reports
- **tests/** — Comprehensive test suite

## Quick Start

```bash
...

## What It's For
Formal specification for the fleet bottle communication protocol — schema, validation, routing, and lifecycle

## Who Would Use It
AI/ML engineers building multi-agent systems with structured coordination protocols.

## Honest Assessment
Has code examples. missing: benchmarks.
