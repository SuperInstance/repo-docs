# Oxide GPU — Index

**Total repos: 42**

GPU computing infrastructure for the SuperInstance ecosystem. The oxide-gpu collection provides synchronization primitives, distributed systems patterns, computational kernels, and GPU-accelerated mathematical computing — all designed for the unique constraints of GPU programming (massive parallelism, memory hierarchies, synchronization challenges).

## Category Overview

This category splits into three clear sub-domains:

### 1. Oxide Distributed Systems Primitives (~20 repos)

GPU-native implementations of classic distributed systems patterns, adapted for the GPU programming model where thousands of threads must coordinate:
- **Synchronization:** oxide-barrier (ternary arrival state barriers), oxide-ring (ring buffers), oxide-slotmap (slot maps)
- **Consensus & Replication:** oxide-raft-log (Raft consensus on GPU), oxide-crdt (CRDTs for GPU state), oxide-federation (federated state)
- **Reliability:** oxide-circuit-breaker, oxide-loadshed, oxide-health-monitor, oxide-canary, oxide-checkpoint
- **Data Management:** oxide-compactor, oxide-chunk, oxide-tombstone, oxide-journal, oxide-epoch
- **Multi-tenancy:** oxide-tenancy, oxide-partition, oxide-lease-grid, oxide-sandbox
- **Runtime:** oxide-flux-runtime, oxide-workflow, oxide-pipeline, oxide-fleet

### 2. GPU Computational Kernels (~12 repos)

CUDA/OpenCL kernels for mathematical computing:
- **Math Acceleration:** gpu-accelerator, gpu-kernels, gpu-optimizer, gpu-scaling, gpu-bench-lab
- **Specialized Kernels:** gpu-sheaf-laplacian (sheaf theory on GPU), gpu-persistent-homology (TDA on GPU), gpu-symplectic-integrator (Hamiltonian dynamics), gpu-ternary-engine (ternary arithmetic), gpu-ga-kernel (geometric algebra), gpu-annealing (simulated annealing)
- **Experiments:** gpu-experiments (testing ground)

### 3. Oxide Conservation & Constructs (~10 repos)

GPU-aware conservation law tracking and construct integrations:
- oxide-conservation, oxide-energy-balance, oxide-gradient, oxide-constructs
- oxide-compile-cache, oxide-capacity, oxide-federation

### Key Interconnections

- **Sheaf Laplacian GPU** connects directly to the sheaf-topology category, providing GPU acceleration for sheaf cohomology computations
- **Conservation tracking** (oxide-conservation, oxide-energy-balance) implements the same conservation framework as the conservation-laws and lau-conservation repos
- **Ternary engine** relates to the broader ternary math ecosystem (ternary-math category)
- **Oxide barriers** enable the GPU-accelerated agent coordination used by superinstance-core

## Full Repository Listing

### Oxide Distributed Systems

| Repo | Language | Description |
|------|----------|-------------|
| [oxide-barrier](./other-oxide-barrier.md) | Rust | Ternary arrival state GPU barriers |
| [oxide-ring](./other-oxide-ring.md) | Rust | GPU ring buffers |
| [oxide-slotmap](./other-oxide-slotmap.md) | Rust | GPU slot maps |
| [oxide-raft-log](./other-oxide-raft-log.md) | Rust | Raft consensus on GPU |
| [oxide-crdt](./other-oxide-crdt.md) | Rust | CRDTs for GPU state |
| [oxide-federation](./other-oxide-federation.md) | Rust | Federated state management |
| [oxide-circuit-breaker](./other-oxide-circuit-breaker.md) | Rust | Circuit breaker pattern |
| [oxide-loadshed](./other-oxide-loadshed.md) | Rust | Load shedding |
| [oxide-health-monitor](./other-oxide-health-monitor.md) | Rust | Health monitoring |
| [oxide-canary](./other-oxide-canary.md) | Rust | Canary deployment |
| [oxide-checkpoint](./other-oxide-checkpoint.md) | Rust | Checkpoint/restore |
| [oxide-compactor](./other-oxide-compactor.md) | Rust | Data compaction |
| [oxide-chunk](./other-oxide-chunk.md) | Rust | Chunked storage |
| [oxide-tombstone](./other-oxide-tombstone.md) | Rust | Tombstone management |
| [oxide-journal](./other-oxide-journal.md) | Rust | Write-ahead journal |
| [oxide-epoch](./other-oxide-epoch.md) | Rust | Epoch management |
| [oxide-tenancy](./other-oxide-tenancy.md) | Rust | Multi-tenancy |
| [oxide-partition](./other-oxide-partition.md) | Rust | Partition management |
| [oxide-lease-grid](./other-oxide-lease-grid.md) | Rust | Lease grid coordination |
| [oxide-sandbox](./other-oxide-sandbox.md) | Rust | GPU sandboxing |
| [oxide-flux-runtime](./other-oxide-flux-runtime.md) | Rust | FLUX runtime |
| [oxide-workflow](./other-oxide-workflow.md) | Rust | GPU workflow engine |
| [oxide-pipeline](./other-oxide-pipeline.md) | Rust | GPU pipelines |
| [oxide-fleet](./other-oxide-fleet.md) | Rust | Fleet coordination |
| [oxide-capacity](./other-oxide-capacity.md) | Rust | Capacity planning |
| [oxide-compile-cache](./other-oxide-compile-cache.md) | Rust | Compile caching |

### GPU Computational Kernels

| Repo | Language | Description |
|------|----------|-------------|
| [gpu-accelerator](./other-gpu-accelerator.md) | CUDA | GPU acceleration framework |
| [gpu-kernels](./other-gpu-kernels.md) | CUDA | General GPU kernels |
| [gpu-optimizer](./other-gpu-optimizer.md) | CUDA | GPU optimization |
| [gpu-scaling](./other-gpu-scaling.md) | CUDA | GPU scaling studies |
| [gpu-bench-lab](./other-gpu-bench-lab.md) | CUDA | Benchmarking lab |
| [gpu-experiments](./other-gpu-experiments.md) | CUDA | Experimental kernels |
| [gpu-sheaf-laplacian](./other-gpu-sheaf-laplacian.md) | CUDA | Sheaf Laplacian on GPU |
| [gpu-persistent-homology](./other-gpu-persistent-homology.md) | CUDA | TDA on GPU |
| [gpu-symplectic-integrator](./other-gpu-symplectic-integrator.md) | CUDA | Hamiltonian integration |
| [gpu-ternary-engine](./other-gpu-ternary-engine.md) | CUDA | Ternary arithmetic engine |
| [gpu-ga-kernel](./other-gpu-ga-kernel.md) | CUDA | Geometric algebra kernel |
| [gpu-annealing](./other-gpu-annealing.md) | CUDA | Simulated annealing |

### Oxide Conservation & Constructs

| Repo | Language | Description |
|------|----------|-------------|
| [oxide-conservation](./other-oxide-conservation.md) | Rust | GPU conservation laws |
| [oxide-energy-balance](./other-oxide-energy-balance.md) | Rust | Energy balance tracking |
| [oxide-gradient](./other-oxide-gradient.md) | Rust | GPU gradient computation |
| [oxide-constructs](./other-oxide-constructs.md) | Rust | Construct integrations |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
