# crdt-map

**Cluster:** cs-ds-algos  
**Language:** Rust  
**Source:** [SuperInstance/crdt-map](https://github.com/SuperInstance/crdt-map)

## Intention

See README.

## How It Works

### GCounter (Grow-Only Counter)

A counter that only increases. Each replica maintains its own monotonic counter. The total value is the sum of all per-replica counters.

[code]

Merge rule: component-wise `max` for each replica ID. This ensures:
- **Commutativity**: merge(A, B) = merge(B, A)
- **Associativity**: merge(A, merge(B, C)) = merge(merge(A, B), C)
- **Idempotence**: merge(A, A) = A

### PNCounter (Positive-Negative Counter)

Supports both increment and decrement via a pair of G-Counters:
- `P` counts increments
- `N` counts decrements
- Value = P.value() - N.value()

### LWWRegiste

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (160 lines, 5721 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# CRDT Map

A Rust library implementing Conflict-free Replicated Data Types (CRDTs) for distributed state management. Provides GCounter, PNCounter, LWWRegister, ORSet, and a CRDTMap for building eventually consistent distributed systems.

## Why This Matters

In distributed systems, achieving consistency without coordination is extraordinarily valuable. Traditional approaches require distributed locking, consensus rounds, or two-phase commits — all expensive and failure-prone. CRDTs provide a mathematically proven alternative: data structures that **always converge** regardless of message ordering, duplication, or delay.

CRDTs power real-world systems:
- **Riak KV** — Shopping carts, counters, sets
- **Amazon DynamoDB** — Conflict resolution for globally distributed tables
- **Automerge** — Collaborative editing (Google Docs-style)
- **Apple Notes** — Offline-first sync across devices

## Architecture

### GCounter (Grow-Only Counter)

A counter that only increases. Each replica maintains its own monotonic counter. The total value is the sum of all per-replica counters.

```
Replica A: {A: 5, B: 0}  → value = 5
Replica B: {A: 0, B: 3}  → value = 3
Merged:    {A: 5, B: 3}  → value = 8
```

Merge rule: component-wise `max` for each replica ID. This ensures:
- **Commutativity**: merge(A, B) = merge(B, A)
- **Associativity**: merge(A, merge(B, C)) = merge(merge(A, B), C)
- **Idempotence**: merge(A, A) = A

### PNCounter (Positive-Negative Counter)

Supports both increment and decrement via a pair of G-Counters:
- `P` counts increments
- `N` counts decrements
- Value = P.value() - N.value()

### LWWRegister (Last-Writer-Wins Register)

Stores a single value with a timestamp. On conflict, the value with the higher timestamp wins. Ties are broken deterministically by replica ID comparison.

**Warning**: LWW depends on clock synchronization. Use hybrid logical clocks (HLC) in production to minimize clock skew effects.

### ORSet (Observed-Remove Set)

A set supporting add and remove operations where:
- Each `add(e)` attaches a unique tag to the element
- `remove(e)` only removes tags that the calling replica has observed
- Concurrent add and remove of the same element: **add wins**

This provides intuitive semantics: if you haven't seen someone add an element, removing it won't affect their future observation of it.

### CRDTMap

A key-value store combining OR-Set (for key membership) with LWW-Register (for values). Supports insert, remove, and merge operations.

## Usage

```rust
use crdt_map::{GCounter, PNCounter, LWWRegister, ORSet, CRDTMap};

// === G-Counter ===
let mut c1 = GCounter::new("node-1");
let mut c2 = GCounter::new("node-2");
c1.increment(10);
c2.increment(20);
let merged = c1.merge(&c2);
assert_eq!(merged.value(), 30);

// === PN-Counter ===
let mut pn = PNCounter::new("node-1");
pn.increment(100);
pn.decrement(30);
assert_eq!(pn.value(), 70);

// === LWW Register ===
let mut reg = LWWRegister::new("initial", 1, "node-1");
reg.set("upda
```
