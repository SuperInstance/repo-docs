# construct-hotswap

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/construct-hotswap](https://github.com/SuperInstance/construct-hotswap)

## Intention

Experiment: live construct hotswap with CRDT state sync. Tests loading GPU capabilities from git, deploying to persistent kernels, and hotswapping without stopping execution.

## How It Works

### Construct Lifecycle State Machine

[code]

States follow a strict transition protocol:

| Transition | Trigger | Latency |
|-----------|---------|---------|
| → Loaded | `load(name, version)` | 100 µs |
| → Deployed | `deploy(name, node)` | 50 µs |
| → Draining | `hotswap(name, new_ver)` start | — |
| → Deployed | `hotswap(name, new_ver)` complete | 300 µs + CRDT sync (200 µs) |

### CRDT Merge Protocol

Each node maintains a `HashMap<String, String>` mapping construct names to versions. The CRDT merge is **last-writer-wins (LWW)** based on microsecond timestamps:

$$\text{merge}(S_A, S_B)

## What It's For

Experiment: live construct hotswap with CRDT state sync. Tests loading GPU capabilities from git, deploying to persistent kernels, and hotswapping without stopping execution.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (131 lines, 5490 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# construct-hotswap

A Rust library for **live construct hotswapping with CRDT state synchronization**, simulating zero-downtime kernel/circuit updates across a multi-node GPU cluster. It models construct lifecycle states (Load → Deploy → Drain → Hotswap) with eventual consistency via CRDT merge across nodes.

## Why It Matters

Live hotswapping — updating code without interrupting service — is the holy grail of high-availability systems. This crate models the pattern used in:

- **GPU kernel hotswapping** — updating CUDA/PTX kernels without pipeline stalls
- **WebAssembly module replacement** — hot-loading new WASM in edge workers
- **Database migrations** — blue-green schema swaps with backfill
- **Game engine updates** — swapping shader/compute pipelines mid-frame
- **Service mesh sidecars** — Envoy/proxy filter chain hot reload

The CRDT (Conflict-free Replicated Data Type) state sync ensures all nodes converge to the same construct version set without coordination — critical for ultra-low-latency systems where distributed consensus is too slow.

## How It Works

### Construct Lifecycle State Machine

```
    Load         Deploy        Hotswap
  ──────→      ──────→         ──────→
  Loaded      Deployed        Draining
                              Deployed
```

States follow a strict transition protocol:

| Transition | Trigger | Latency |
|-----------|---------|---------|
| → Loaded | `load(name, version)` | 100 µs |
| → Deployed | `deploy(name, node)` | 50 µs |
| → Draining | `hotswap(name, new_ver)` start | — |
| → Deployed | `hotswap(name, new_ver)` complete | 300 µs + CRDT sync (200 µs) |

### CRDT Merge Protocol

Each node maintains a `HashMap<String, String>` mapping construct names to versions. The CRDT merge is **last-writer-wins (LWW)** based on microsecond timestamps:

$$\text{merge}(S_A, S_B) = \{(k, v) : v = \arg\max_t \{(k, v, t) \in S_A \cup S_B\}\}$$

The sync operation:
1. Compute the union of all node states
2. For each key, keep the value from the node with the highest timestamp
3. Broadcast merged state to all nodes

This is an **eventual consistency** model — all nodes converge after one sync round.

### Hotswap Protocol

The zero-downtime hotswap sequence:

```
1. Set construct state → Draining     (in-flight requests finish)
2. Swap version + kernel PTX          (atomic pointer swap)
3. Set construct state → Deployed      (new requests accepted)
4. CRDT sync to all nodes              (version propagation)
```

Total hotswap latency: `300 µs (drain) + 100 µs (swap) + 200 µs (sync) = 600 µs`

### Complexity Analysis

| Operation | Time | Space |
|-----------|------|-------|
| `load(name, version)` | O(1) | O(1) |
| `deploy(name, node)` | O(1) | O(1) |
| `crdt_sync()` | O(N × K) | O(K) |
| `hotswap(name, version)` | O(N × K) | O(K) |

Where N = node count, K = total deployed constructs.

## Quick Start

```rust
use construct_hotswap::HotswapExperiment;

let mut exp = HotswapExperiment::new(3); // 3 GPU nodes
exp.load("at
```
