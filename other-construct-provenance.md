# construct-provenance

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/construct-provenance](https://github.com/SuperInstance/construct-provenance)

## Intention

Full provenance tracking for GPU constructs. Append-only log of compile→deploy→execute. Query: what version produced this result?

## How It Works

### Append-Only Log Model

The log is a `Vec<ProvenanceEntry>` — entries are only ever appended, never mutated or deleted. This gives:

- **Tamper evidence**: any modification breaks the time-ordered sequence
- **O(1) append**: push to the end, amortized constant time
- **O(n) full scan**: for range queries, linear in the number of entries

### Dual Index Structure

Two `HashMap` indexes provide fast lookup:

[code]

| Operation | Time Complexity | Space Complexity |
|-----------|----------------|-----------------|
| `record_compile` | O(1) amortized | O(1) per entry |
| `record_deploy` | O(1)

## What It's For

Full provenance tracking for GPU constructs. Append-only log of compile→deploy→execute. Query: what version produced this result?

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (125 lines, 6198 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# construct-provenance

**Append-only provenance tracking for GPU compute constructs** — every compilation, deployment, execution, and hotswap is recorded in a tamper-evident log with O(1) indexed lookup. Query "what version produced this result?" and get the full chain of custody in constant time.

## Why It Matters

In distributed GPU fleets, the same kernel may be compiled from different git commits, deployed to different nodes, and hotswapped at runtime. When a model produces a bad result, you need to trace *which* version of *which* construct on *which* node generated it — and what happened before and after. This is the software-supply-chain problem applied to GPU artifacts.

Production systems like MLflow, Weights & Biases, and Kubernetes audit logs solve this for ML training runs and cluster events. `construct-provenance` brings the same discipline to GPU construct lifecycle management: a lightweight, in-memory append-only log with dual indexes (by construct name and by result hash) that answers provenance queries without scanning the entire history.

## How It Works

### Append-Only Log Model

The log is a `Vec<ProvenanceEntry>` — entries are only ever appended, never mutated or deleted. This gives:

- **Tamper evidence**: any modification breaks the time-ordered sequence
- **O(1) append**: push to the end, amortized constant time
- **O(n) full scan**: for range queries, linear in the number of entries

### Dual Index Structure

Two `HashMap` indexes provide fast lookup:

```
index_by_construct: HashMap<String, Vec<usize>>  // name → entry indices
index_by_result:    HashMap<String, Vec<usize>>  // result_hash → entry indices
```

| Operation | Time Complexity | Space Complexity |
|-----------|----------------|-----------------|
| `record_compile` | O(1) amortized | O(1) per entry |
| `record_deploy` | O(1) amortized | O(1) per entry |
| `record_execute` | O(1) amortized | O(1) per entry |
| `record_hotswap` | O(1) amortized | O(1) per entry |
| `find_producer(hash)` | O(1) expected | O(k) where k = executions with that hash |
| `construct_history(name)` | O(k) where k = entries for that construct | O(k) |
| `range(start, end)` | O(n) worst case | O(n) for result vec |

### Event Types

The state machine for a construct's lifecycle:

```
Compiled → Deployed → Executed → (Hotswapped → Executed)* → (RolledBack)?
```

Each transition is logged with a monotonically increasing timestamp (microsecond granularity), the construct name, version string, git hash (for compiles), node identifier, and optional result hash (for executions).

### Information-Theoretic Integrity

Each entry stores `git_hash` (SHA-1 of the source tree at compile time). The probability of a hash collision is:

$$P(\text{collision}) = \frac{n^2}{2 \times 2^{160}}$$

For n = 10⁶ constructs, this is ≈ 4.3 × 10⁻³⁵ — effectively zero.

## Quick Start

```rust
use construct_provenance::ProvenanceLog;

let mut log = ProvenanceLog::new();

// Record a construct's lifecycle
log.rec
```
