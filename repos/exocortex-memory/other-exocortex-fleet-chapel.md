# exocortex-fleet-chapel

## Intention
**Chapel's PGAS is what the fleet actually is — one address space, many devices.**

## How It Works
```
┌─────────────────────────────────────────────────────────────────────┐
│                        EXOCORTEX FLEET                             │
│                                                                     │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐          │
│  │  Device   │  │  Device   │  │  Device   │  │  Device   │          │
│  │  (GPU)    │  │  (CPU)    │  │  (MCU)    │  │(Browser)  │          │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘  └────┬─────┘

## What It's For
Full Raft includes:
- Log replication with consistency checks
- Log compaction (snapshotting)
- Dynamic membership changes
- Linearizable reads via ReadIndex

We omit these because:
1. **Pedagogical clarity**: The election mechanism is the most interesting part for fleet coordination. Log replication is mechanical.
2. **Fleet semantics**: In our model, the leader proposes *configuration changes* (

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Chapel

## Status Assessment
Documented with code examples and API references (695 line README).

## Honest Assessment
Well-documented (695 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/exocortex-fleet-chapel](https://github.com/SuperInstance/exocortex-fleet-chapel)*
