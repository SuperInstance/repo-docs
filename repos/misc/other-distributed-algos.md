# distributed-algos

## Intention
Distributed systems algorithms, readable in Rust. Learn consensus, replication, and consistency by reading code.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
| Module | What you get |
|---|---|
| `vector_clock` | Vector clocks, causal ordering, conflict resolution (LWW, merge) |
| `consensus::paxos` | Full Paxos: proposer, acceptor, learner; simulated multi-node runs |
| `consensus::raft` | Raft consensus: leader election, log replication, state machine |
| `consistency` | Strong / Eventual / Causal consistency models; replica merging |
| `quorum` | Qu

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Has substantial documentation (106 lines).

## Honest Assessment
Moderately documented (106 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/distributed-algos](https://github.com/SuperInstance/distributed-algos)*
