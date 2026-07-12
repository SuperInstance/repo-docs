# Sheaf Topology — Index

**Total repos: 19**

Cellular sheaf theory and Hodge decomposition for multi-agent systems. This collection applies algebraic topology to agent coordination — sheaf cohomology measures consensus, the sheaf Laplacian drives synchronization, and Hodge decomposition classifies disagreements as resolvable (gradient), cyclic (curl), or irreconcilable (harmonic).

## Category Overview

### The Mathematical Foundation

The core insight: **multi-agent coordination is a problem in algebraic topology.** When agents on a network share information:
- **H⁰ (global sections)** = agents that agree — the consensus space
- **H¹ (obstructions)** = fundamental disagreements — topology prevents consensus
- **Sheaf Laplacian L₁ = δᵀδ** = generalized diffusion that respects heterogeneous information

### Sub-domains

#### 1. Sheaf Framework (~8 repos)

- **sheaf-agents** — Cellular sheaf framework for multi-agent coordination via sheaf cohomology. Assigns stalks (vector spaces) to nodes, restriction maps to edges. Implements coboundary operators and H⁰/H¹ computation
- **sheaf-agents-c** — C implementation of the sheaf agent framework
- **sheaf-agents-rs** — Rust implementation (published to crates.io)
- **sheaf-laplacian** — The flagship library. Computes L₁ = δᵀδ on cellular sheaves over graphs. 277-line README, 11 code blocks. Published to crates.io and docs.rs
- **sheaf-coherence** — Coherence measurement between agents
- **sheaf-coherence-rs** — Rust coherence implementation
- **sheaf-cohomology** — Sheaf cohomology computation
- **sheaf-constraint-synthesis** — Constraint synthesis from sheaf structure
- **sheaf-dynamics** — Sheaf dynamics and evolution
- **sheaf-gossip** — Gossip protocols using sheaf structure
- **sheaf-spectral** — Spectral properties of sheaves
- **sheaf-persistence-bundle** — Persistent sheaf bundles

#### 2. Hodge Theory (~7 repos)

- **hodge-theory** — Mathematical foundations of Hodge decomposition
- **hodge-consensus** — Hodge decomposition of agent disagreements: gradient (resolvable) + curl (cyclic) + harmonic (irreconcilable). Predicts which disputes will resolve naturally
- **hodge-consensus-rs** — Rust implementation
- **hodge-belief** — Belief revision through Hodge decomposition
- **hodge-belief-c** — C implementation
- **hodge-belief-rs** — Rust implementation
- **hodge-music-rs** — Hodge decomposition applied to musical harmony

### Key Interconnections

- **sheaf-laplacian** is one of the most polished libraries in the entire ecosystem — published to crates.io, documented on docs.rs, 277-line README
- The **Hodge consensus** model directly inspired si-hodge-consensus-demo in superinstance-core
- **sheaf-gossip** connects to the fleet communication layer (cocapn-marine)
- **hodge-music-rs** bridges to the music-spectral category
- The sheaf framework underpins conservation law verification across the ecosystem
- **gpu-sheaf-laplacian** (oxide-gpu) provides GPU acceleration for this category's computations
- Sheaf theory appears throughout lau-mathematics (lau-sheaf-cohomology, lau-sheaf-neural, etc.)

## Full Repository Listing

### Sheaf Framework

| Repo | Language | Description |
|------|----------|-------------|
| [sheaf-agents](./other-sheaf-agents.md) | Rust | Cellular sheaf for agent coordination |
| [sheaf-agents-c](./other-sheaf-agents-c.md) | C | C implementation |
| [sheaf-agents-rs](./other-sheaf-agents-rs.md) | Rust | Rust (crates.io) |
| [sheaf-laplacian](./other-sheaf-laplacian.md) | Rust | Sheaf Laplacian L₁ = δᵀδ (crates.io, docs.rs) |
| [sheaf-coherence](./other-sheaf-coherence.md) | Rust | Coherence measurement |
| [sheaf-coherence-rs](./other-sheaf-coherence-rs.md) | Rust | Rust coherence |
| [sheaf-cohomology](./other-sheaf-cohomology.md) | Rust | Cohomology computation |
| [sheaf-constraint-synthesis](./other-sheaf-constraint-synthesis.md) | Rust | Constraint synthesis |
| [sheaf-dynamics](./other-sheaf-dynamics.md) | Rust | Sheaf dynamics |
| [sheaf-gossip](./other-sheaf-gossip.md) | Rust | Sheaf gossip protocol |
| [sheaf-spectral](./other-sheaf-spectral.md) | Rust | Spectral sheaf properties |
| [sheaf-persistence-bundle](./other-sheaf-persistence-bundle.md) | Rust | Persistent bundles |

### Hodge Theory

| Repo | Language | Description |
|------|----------|-------------|
| [hodge-theory](./other-hodge-theory.md) | Rust | Mathematical foundations |
| [hodge-consensus](./other-hodge-consensus.md) | Rust | Disagreement decomposition |
| [hodge-consensus-rs](./other-hodge-consensus-rs.md) | Rust | Rust implementation |
| [hodge-belief](./other-hodge-belief.md) | Rust | Belief revision via Hodge |
| [hodge-belief-c](./other-hodge-belief-c.md) | C | C implementation |
| [hodge-belief-rs](./other-hodge-belief-rs.md) | Rust | Rust implementation |
| [hodge-music-rs](./other-hodge-music-rs.md) | Rust | Hodge decomposition for music |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
