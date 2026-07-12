# oxide-crdt

## Intention
GPU-aware CRDT types for distributed Flux→PTX runtime state synchronization. Kernel state, agent assignments, and metrics merge across GPU nodes without coordination.

## How It Works
GPU-aware CRDT types for distributed state synchronization in the Flux→PTX runtime. When you're running kernels across a fleet of GPU nodes, the last thing you want is a consensus round-trip every time an agent migrates or a kernel gets hot-swapped. Network partitions happen. Clocks drift. Nodes reboot. This crate gives you convergent data structures that merge correctly without coordination — so your distributed GPU state stays consistent even when the fabric doesn't. Why CRDTs for GPU State?

## What It's For
GPU-aware CRDT types for distributed Flux→PTX runtime state synchronization. Kernel state, agent assignments, and metrics merge across GPU nodes without coordination.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 8,220 characters, 182 lines
- Code examples: 6 blocks
- Installation instructions: yes
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: no

## Honest Assessment

**Strengths:**
- Code examples present (6 code blocks)
- Installation/usage instructions provided
- Solid README with good coverage

**Concerns:**
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
