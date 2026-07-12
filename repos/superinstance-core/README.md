# SuperInstance Core — Index

**Total repos: 51**

The central runtime, tooling, and theoretical framework for the SuperInstance ecosystem. This category contains the core libraries, CLI tools, multi-language runtimes, and mathematical agents that define what SuperInstance *is* as a platform. If the lau-mathematics category is the theory, superinstance-core is the practice.

## Category Overview

### 1. Core Runtime & Platform (~8 repos)

The beating heart of the ecosystem:
- **si-superinstance** — The main platform definition
- **si-core-c** — General-purpose C library for constraint-aware AI (conservation laws, spectral methods, capability discovery). 522-line README, 21 code examples — one of the most mature repos in the entire ecosystem
- **si-cli** — Unified CLI with 8 subcommands: scan, audit, rank, graph, generate, plus conservation verification. 639-line README — the most documented tool
- **si-registry-rs** — Fleet registry in Rust
- **si-catalog** — Ecosystem catalog
- **si-scanner** — Repository scanner
- **si-bench** — Benchmarking suite
- **si-validator** — Validation framework

### 2. Multi-Language Runtimes (~6 repos)

The SuperInstance runtime ported to multiple languages:
- **Rust** (default, via si-core-c and others)
- **si-runtime-go** — Go runtime
- **si-runtime-js** — JavaScript/TypeScript runtime
- **si-runtime-python** — Python runtime
- **si-runtime-wasm** — WebAssembly runtime
- **si-runtime-zig** — Zig runtime

### 3. Mathematical Fleet Agents (~15 repos)

Theoretical agent frameworks applying deep mathematics to fleet coordination:
- **si-hodge-consensus-demo** — Hodge decomposition for agent disagreements (gradient/curl/harmonic). Proof of concept predicting which disputes resolve
- **si-symplectic-agent** — Symplectic geometry for fleet state
- **si-curvature-agent** — Ricci curvature for fleet dynamics
- **si-kernel-agent** — Kernel methods for agent coordination
- **si-noether-agent** — Noether's theorem for conserved quantities
- **si-persistence-agent** — Persistent homology for agent state
- **si-variational-agent** — Variational inference for fleet decisions
- **si-lyapunov-fleet** — Lyapunov stability for fleet convergence
- **si-markov-fleet** — Markov chain fleet modeling
- **si-wasserstein-fleet** — Wasserstein distance for fleet comparison
- **si-mean-field** — Mean field theory for large-scale fleets
- **si-gradient-flow** — Gradient flow dynamics
- **si-information-geodesic** — Information geometry for fleet routing
- **si-morse-theory** — Morse theory for fleet topology
- **si-spectral-gap** — Spectral gap analysis

### 4. Conservation & Gossip (~6 repos)

- **si-conservation-diffusion** — Conservation law diffusion
- **si-conservation-gauge-live** — Live gauge conservation
- **si-conservation-python** — Python conservation SDK
- **si-conservation-wasm** — WASM conservation
- **si-sheaf-gossip** — Sheaf-theoretic gossip protocol
- **si-symplectic-gossip** — Symplectic gossip

### 5. Tropical & Topological (~5 repos)

- **si-tropical-attention** — Tropical attention mechanisms
- **si-tropical-transport** — Tropical optimal transport
- **si-topological-protect** — Topological protection
- **si-fibration-timing** — Fibration timing analysis
- **si-variational-bayes** — Variational Bayes for fleet inference

### 6. Fleet Management & Demo (~4 repos)

- **si-fleet-api** — Fleet REST API
- **si-fleet-health** — Fleet health monitoring
- **si-geometric-demo** — Geometric demonstration
- **si-compaction-poc** — Compaction proof of concept
- **si-renyi-entropy** — Rényi entropy measures

### 7. Spreadsheet Engine (~6 repos)

A surprisingly complete spreadsheet engine within the ecosystem:
- **spreadsheet-cells** — Cell engine
- **spreadsheet-conservation-wasm** — Conservation laws in WASM spreadsheets
- **spreadsheet-engine** — Core engine
- **spreadsheet-formulas** — Formula evaluation
- **spreadsheet-moment-proto** — Moment protocol
- **spreadsheet-plr-bridge** — PLR bridge
- **spreadsheet-projection** — Projection system

### Key Interconnections

- **si-cli** is the entry point for developers, connecting to ecosystem scanning, conservation verification, and template generation
- **si-core-c** provides the foundational C library that runs on embedded devices, compiles to WASM, and links into kernels
- The mathematical agents (si-hodge-consensus-demo, si-symplectic-agent, etc.) consume theory from lau-mathematics and sheaf-topology
- Multi-language runtimes enable the polyglot fleet model — agents written in Go, Python, JS, Zig, or WASM all interoperate
- The spreadsheet engine is an unexpected but interesting sub-system, possibly for configuration or data management

## Full Repository Listing

### Core Platform

| Repo | Language | Description |
|------|----------|-------------|
| [si-superinstance](./other-si-superinstance.md) | Rust | Platform definition |
| [si-core-c](./other-si-core-c.md) | C | Constraint-aware AI core library |
| [si-cli](./other-si-cli.md) | Rust | Unified CLI (scan, audit, rank, graph) |
| [si-registry-rs](./other-si-registry-rs.md) | Rust | Fleet registry |
| [si-catalog](./other-si-catalog.md) | Rust | Ecosystem catalog |
| [si-scanner](./other-si-scanner.md) | Rust | Repository scanner |
| [si-bench](./other-si-bench.md) | Rust | Benchmarking suite |
| [si-validator](./other-si-validator.md) | Rust | Validation framework |

### Multi-Language Runtimes

| Repo | Language | Description |
|------|----------|-------------|
| [si-runtime-go](./other-si-runtime-go.md) | Go | Go runtime |
| [si-runtime-js](./other-si-runtime-js.md) | JavaScript | JS runtime |
| [si-runtime-python](./other-si-runtime-python.md) | Python | Python runtime |
| [si-runtime-wasm](./other-si-runtime-wasm.md) | WASM | WebAssembly runtime |
| [si-runtime-zig](./other-si-runtime-zig.md) | Zig | Zig runtime |

### Mathematical Fleet Agents

| Repo | Language | Description |
|------|----------|-------------|
| [si-hodge-consensus-demo](./other-si-hodge-consensus-demo.md) | Rust | Hodge decomposition for disagreements |
| [si-symplectic-agent](./other-si-symplectic-agent.md) | Rust | Symplectic fleet geometry |
| [si-curvature-agent](./other-si-curvature-agent.md) | Rust | Ricci curvature agent |
| [si-kernel-agent](./other-si-kernel-agent.md) | Rust | Kernel methods agent |
| [si-noether-agent](./other-si-noether-agent.md) | Rust | Noether conserved quantities |
| [si-persistence-agent](./other-si-persistence-agent.md) | Rust | Persistent homology agent |
| [si-variational-agent](./other-si-variational-agent.md) | Rust | Variational inference agent |
| [si-lyapunov-fleet](./other-si-lyapunov-fleet.md) | Rust | Lyapunov stability |
| [si-markov-fleet](./other-si-markov-fleet.md) | Rust | Markov chain fleet modeling |
| [si-wasserstein-fleet](./other-si-wasserstein-fleet.md) | Rust | Wasserstein fleet comparison |
| [si-mean-field](./other-si-mean-field.md) | Rust | Mean field theory |
| [si-gradient-flow](./other-si-gradient-flow.md) | Rust | Gradient flow dynamics |
| [si-information-geodesic](./other-si-information-geodesic.md) | Rust | Information geodesics |
| [si-morse-theory](./other-si-morse-theory.md) | Rust | Morse theory for fleet topology |
| [si-spectral-gap](./other-si-spectral-gap.md) | Rust | Spectral gap analysis |
| [si-renyi-entropy](./other-si-renyi-entropy.md) | Rust | Rényi entropy measures |

### Conservation & Gossip

| Repo | Language | Description |
|------|----------|-------------|
| [si-conservation-diffusion](./other-si-conservation-diffusion.md) | Rust | Conservation diffusion |
| [si-conservation-gauge-live](./other-si-conservation-gauge-live.md) | Rust | Live gauge conservation |
| [si-conservation-python](./other-si-conservation-python.md) | Python | Python conservation SDK |
| [si-conservation-wasm](./other-si-conservation-wasm.md) | WASM | WASM conservation |
| [si-sheaf-gossip](./other-si-sheaf-gossip.md) | Rust | Sheaf gossip protocol |
| [si-symplectic-gossip](./other-si-symplectic-gossip.md) | Rust | Symplectic gossip |

### Tropical & Topological

| Repo | Language | Description |
|------|----------|-------------|
| [si-tropical-attention](./other-si-tropical-attention.md) | Rust | Tropical attention |
| [si-tropical-transport](./other-si-tropical-transport.md) | Rust | Tropical optimal transport |
| [si-topological-protect](./other-si-topological-protect.md) | Rust | Topological protection |
| [si-fibration-timing](./other-si-fibration-timing.md) | Rust | Fibration timing |
| [si-variational-bayes](./other-si-variational-bayes.md) | Rust | Variational Bayes |

### Fleet Management

| Repo | Language | Description |
|------|----------|-------------|
| [si-fleet-api](./other-si-fleet-api.md) | Rust | Fleet REST API |
| [si-fleet-health](./other-si-fleet-health.md) | Rust | Fleet health monitoring |
| [si-geometric-demo](./other-si-geometric-demo.md) | Rust | Geometric demo |
| [si-compaction-poc](./other-si-compaction-poc.md) | Rust | Compaction PoC |

### Spreadsheet Engine

| Repo | Language | Description |
|------|----------|-------------|
| [spreadsheet-engine](./other-spreadsheet-engine.md) | Rust | Core spreadsheet engine |
| [spreadsheet-cells](./other-spreadsheet-cells.md) | Rust | Cell engine |
| [spreadsheet-formulas](./other-spreadsheet-formulas.md) | Rust | Formula evaluation |
| [spreadsheet-conservation-wasm](./other-spreadsheet-conservation-wasm.md) | WASM | Conservation in spreadsheets |
| [spreadsheet-moment-proto](./other-spreadsheet-moment-proto.md) | Rust | Moment protocol |
| [spreadsheet-plr-bridge](./other-spreadsheet-plr-bridge.md) | Rust | PLR bridge |
| [spreadsheet-projection](./other-spreadsheet-projection.md) | Rust | Projection system |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
