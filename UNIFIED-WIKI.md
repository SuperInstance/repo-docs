# SuperInstance Unified Wiki

**The single source of truth for the SuperInstance ecosystem.**

---

## Quick Start

| You Are | Start Here |
|---------|------------|
| New to SuperInstance | [What is SuperInstance?](#what-is-superinstance) |
| Developer | [Getting Started](#getting-started) |
| Researcher | [Key Concepts](#key-concepts) |
| Looking for a specific repo | [Repository Guide](#repository-guide) |
| Wanting detailed docs | [repo-docs System](#repo-docs-system) |

---

## What is SuperInstance?

SuperInstance is a research ecosystem building **autonomous AI agent systems grounded in mathematical physics and conservation laws**. Founded on the principle that AI agents should behave like physical systems — every action has an energy cost, coordination follows musical principles, and knowledge has spatial/temporal semantics.

### The Core Thesis

> **AI agents should be governed by conservation laws, not unbounded token generation.**

This means:
- Every agent action has an energy cost tracked through conservation equations (γ + η = C)
- Agent coordination follows musical principles (harmony, counterpoint, rhythm, polyphony)
- Knowledge is organized into "rooms" with spatial/temporal semantics
- Computation uses ternary logic {-1, 0, +1} for richer decision-making
- Agent logic compiles to deterministic bytecode for verifiable execution

### By The Numbers

| Metric | Count |
|--------|-------|
| Total Repositories | ~4,098 (3,327 original, 771 forks) |
| Languages | 25+ (Rust, Python, TypeScript, C, CUDA, Go, and more) |
| Major Thematic Clusters | 12 |
| Open Source License | Apache 2.0 |
| Active Development | Ongoing |

### Not A Startup

SuperInstance is closer to a **one-person research institute expressed in code** — equal parts genuine engineering, mathematical exploration, and ambitious synthesis. It represents an attempt to build a complete infrastructure for AI agents, from mathematical foundations to practical deployment.

---

## Key Concepts

### PLATO — Knowledge Rooms

**PLATO** organizes knowledge into "rooms" — bounded contexts where agents operate. Think of it as a house where each room represents a domain of knowledge.

- **Tiles**: Units of knowledge/work (like Trello cards but mathematical)
- **Deadband Protocol**: Only signal when something changes beyond a threshold (like a thermostat)
- **Lifecycle**: Rooms can be born, grow, merge, die
- **Nervous System**: Sensor → Deadband → Nano-model → LoRA → Fleet → Cloud

**Key Repos**: `plato-server`, `plato-runtime-kernel`, `plato-engine-block-c`, `plato-torch`

### FLUX — Deterministic Bytecode

**FLUX** is a bytecode VM for running agent logic. The idea: agent decisions should be auditable bytecode, not opaque LLM calls.

- **flux-runtime**: Python reference implementation
- **flux-vm**: Constraint-verified Rust VM (DAL-A certifiable)
- **flux-hardware**: CUDA, AVX-512, FPGA, eBPF backends
- **flux-cross-assembler**: Cloud + edge bytecode compilation

**Key Repos**: `flux-runtime`, `flux-vm`, `flux-hardware`, `flux-compiler`

### Conservation Laws

Governance through physics: **γ + η = C** (gamma + eta = constant). Every agent operation must conserve — you can't create energy from nothing.

- `conservation-action`: CI/CD enforcement
- `conservation-languages`: Same law in 9+ languages
- `conservation-spectral-python`: Spectral analysis of tension graphs

**Key Insight**: This conservation-law governance for AI agents is a genuine research contribution — nobody else is doing this.

### Ternary Computing

The entire **{-1, 0, +1}** number system reimplemented from scratch. Why ternary? It offers richer state representation and more efficient computation for certain problems.

- `ternary-types`, `ternary-algebra`, `ternary-matrix` — core math
- `ternary-svm`, `ternary-search`, `ternary-pid` — applied ML and control
- `ternary-compiler-v2` — compilation pipeline

### Fleet Orchestration

The "nervous system" connecting agents across instances.

- `fleet-i2i-protocol`: Instance-to-instance communication
- `fleet-conductor`: Orchestration, health, graceful shutdown
- `fleet-health-monitor`: One of the most tested repos (248 tests)
- `fleet-warden-rs`: Security and policy enforcement
- Musical coordination: ~100 MIDI-themed repos mapping rhythm, harmony, counterpoint to fleet operations

### Constraint Theory

Geometric constraint satisfaction as a universal solver.

- `constraint-theory-core`: 83 tests, Eisenstein lattices, Laman rigidity
- `constraint-hamiltonian`: Symplectic integration with conservation
- `constraint-schedule`: CSP solver with AC-3 and simulated annealing

### Lau Mathematical Libraries

Comprehensive math in Rust underlying the entire ecosystem.

- `lau-hodge-theory`: Hodge theory for agent knowledge spaces (43 tests)
- `lau-lie-algebra`: Lie algebra implementation (54 tests)
- `lau-lie-group-agents`: Lie groups for agent systems
- Category theory, differential geometry, spectral graph theory, and more

### Grand Pattern

Fibonacci dual-direction architecture for cellular graph intelligence with JEPA prediction.

- Multi-language implementations (Rust, Python, TypeScript, Go, Java, and more)
- GPU/Parallel: CUDA, OpenCL, PTX, SIMD, Vulkan
- Venue-as-agent topology with spectral analysis

### Git-Native Agents

Agents that live in git repositories. The repo **IS** the agent. Git **IS** the nervous system.

- `git-agent`: Repo-native agent framework
- `git-native-mud`: Zero-server MUD using git primitives
- `cocapn`: Repo-first agent runtime

### Exocortex

Persistent cognitive substrate for multi-agent systems. S3-compatible distributed memory.

- `exocortex`: Python core
- `exocortex-memory-zig`: Zig implementation
- Clients: C++, JS, Lua, CircuitPython
- Bridges: MCP (TypeScript), WASM runtime

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                    SUPERINSTANCE ECOSYSTEM                      │
└─────────────────────────────────────────────────────────────────┘
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
   ┌────▼────┐         ┌─────▼──────┐       ┌─────▼────┐
   │  PLATO   │         │   FLUX     │       │ Ternary  │
   │ (262)    │         │  (165)     │       │  (370)   │
   │ Knowledge │         │ Bytecode   │       │ {-1,0,+1}│
   │  Rooms   │         │    VMs     │       │ Computing │
   └────┬────┘         └─────┬──────┘       └─────┬────┘
        │                     │                     │
        │          ┌──────────┼──────────┐         │
        │          │          │          │         │
   ┌────▼───┐ ┌──▼───┐ ┌──▼───┐ ┌───▼────┐ ┌─▼─────┐
   │  LAU   │ │ Forge │ │Grand │ │Exocortex│ │Agent  │
   │ (300+) │ │Flux │ │Pattern│ │  (20+)  │ │Fleet  │
   │ Math/  │ │ (20) │ │ (60) │ │ Memory  │ │Infra  │
   │Physics │ │Tile  │ │Diff  │ │         │ │(100+) │
   └────────┘ │Decomp│ │Graph │ │         │ └───────┘
              └──────┘ └──────┘ └─────────┘
```

### Key Connections

- **PLATO → FLUX**: PLATO knowledge tiles can be compiled into FLUX bytecode
- **FLUX → Ternary**: FLUX constraint engines use ternary logic for safety checks
- **Lau → All**: Lau math libraries underpin constraint theory, spectral analysis, and cognition
- **ForgeFlux**: Decomposes any input into PLATO tiles
- **Exocortex**: Provides persistent memory for all agent systems
- **Git-Agent**: Repo-native agents use PLATO rooms for knowledge storage

---

## Getting Started

### For Developers

1. **Explore PLATO** — Start with `plato-server` for the knowledge system
2. **Try FLUX** — Check `flux-runtime` for bytecode execution
3. **Use Lau Math** — Import `lau-*` crates for scientific computing
4. **Run an Agent** — See `git-agent` for repo-native patterns
5. **Build Fleet** — Use `construct-core` for agent runtime

### For Researchers

1. **Constraint Theory** — `cuda-constraint-engine`, `c-ternary`
2. **Hodge Theory** — `hodge-consensus-rs`, `holonomy-harmony`
3. **Ternary Computing** — `ternary-science`, `ternary-compiler-v2`
4. **Grand Pattern** — `grand-pattern-rs`, `grand-pattern-mono`
5. **Category Theory** — `categorical-agents`, `lau-category-theory`

### For ML/AI

1. **PLATO ML** — `plato-jepa`, `plato-mythos`, `plato-torch`
2. **Ternary ML** — `ternary-tnn`, `ternary-attention`, `ternary-grad`
3. **JEPA** — `jepa-core`, `jepa-predict`
4. **Distillation** — `plato-distill`, `plato-forge-daemon`

### For Infrastructure

1. **Coordination** — `consensus-protocol`, `beacon-protocol`
2. **Messaging** — `i2i-protocol`, `bottle-protocol`, `a2a-signal`
3. **Memory** — `exocortex`, `plato-memory`
4. **Compute** — `flux-hardware`, `gpu-accelerator`

---

## Repository Guide

### Top 20 Standout Repos

The most substantial, real projects in the ecosystem:

| Repo | Description | Language |
|------|-------------|----------|
| **plato-server** | Standalone PLATO knowledge system | Rust |
| **plato-runtime-kernel** | AI theorem prover, conservation-verified | Rust |
| **plato-engine-block-c** | Embedded sensor→history→alarm engine (C99, zero alloc) | C |
| **plato-engine-block-elixir** | Fault-tolerant marine monitoring on BEAM/OTP | Elixir |
| **flux-runtime** | Deterministic bytecode ISA for agentic logic | Python |
| **flux-vm** | FLUX-C constraint VM, DAL-A certifiable | Rust |
| **flux-hardware** | CUDA, AVX-512, FPGA, eBPF backends | Multiple |
| **ternary-science** | Scientific computation over balanced ternary | Python |
| **plato-torch** | GPU forge, PyTorch with tile framing | Python |
| **ternary-compiler-v2** | Advanced ternary compilation pipeline | Rust |
| **lau-hodge-theory** | Hodge theory for agent knowledge (43 tests) | Rust |
| **lau-lie-algebra** | Lie algebra implementation (54 tests) | Rust |
| **exocortex** | Persistent cognitive substrate, S3-compatible | Python |
| **git-agent** | Repo-native agent, the shell IS the agent | Shell |
| **constraint-theory-core** | Eisenstein lattices, Laman rigidity (83 tests) | Rust |
| **fleet-health-monitor** | Fleet health with 248 tests | Rust |
| **grand-pattern-rs** | Fibonacci dual-direction architecture | Rust |
| **hodge-consensus-rs** | Hodge decomposition for agent coordination | Rust |
| **construct-core** | Agent runtime shell | Rust |
| **plato-portal** | Web interface for PLATO | TypeScript |

### By Thematic Cluster

#### PLATO Ecosystem (262 repos)
- Core: `plato-server`, `plato-runtime`, `plato-kernel`
- Engine Blocks: Multi-language room runtimes (Rust, C, Elixir, Zig, Chapel)
- ML/AI: `plato-jepa`, `plato-mythos`, `plato-torch`
- Clients: JS, PHP, Ruby, Python SDKs
- Vessels: IoT/embedded clients (ESP32, RP2040)

#### FLUX Ecosystem (165 repos)
- Core VMs: `flux-core`, `flux-runtime`, `flux-vm`, `flux-zig`
- Hardware: CUDA, AVX-512, FPGA, eBPF backends
- Languages: 80+ language programming runtimes
- Legacy: COBOL, Fortran, ALGOL, MUMPS ports

#### Ternary Computing (370 repos)
- ML/Neural: `tnn`, `attention`, `gradient`, `llm`, `checkpoint`
- GPU/Kernels: `cuda-kernels`, `pack`, `dispatch`
- Distributed: `consensus`, `paxos`, `lease`, `mirror`
- Math/Physics: `ising`, `quantum`, `hamiltonian`
- Data Structures: `btree`, `heap`, `bloom-filter`, `database`

#### Lau Math Libraries (300+ repos)
- Algebra/Topology: Category theory, homology, cohomology
- Analysis: Functional analysis, complex analysis, measure theory
- Geometry: Differential, symplectic, Riemannian
- Physics: Electromagnetism, fluid dynamics, quantum topology
- Agent Theory: Game theory, control theory, dynamical systems

#### Fleet Orchestration (100+ repos)
- Coordination: `fleet-conductor`, `fleet-i2i-protocol`
- Health: `fleet-health-monitor`, `fleet-warden-rs`
- Time/Space: `fleet-clock`, `fleet-coordinate`
- Musical: ~100 MIDI-themed repos for coordination

#### Constraint & Conservation (50+ repos)
- Theory: `constraint-theory-core`, `fracture-coalesce`
- Conservation: `conservation-spectral`, `conservation-action`
- GPU: `cuda-constraint-engine`, `avx512-constraint-checker`

### Quality Assessment

| Quality | Count | Description |
|---------|-------|-------------|
| **Substantial** | ~800 | Rich docs, architecture, motivation (README > 2KB) |
| **Real Project** | ~400 | Working code, examples, proper docs |
| **Moderate** | ~600 | Some substance, likely AI-assisted |
| **Lightweight** | ~500 | Brief docs, small utility |
| **Stub/Auto-generated** | ~400 | Minimal, placeholder, or template |

### What's Real vs Aspirational

**Real Working Implementations:**
- PLATO server and runtime have working implementations
- FLUX VMs have genuine code with test suites
- Lau math libraries contain real mathematical algorithms
- Constraint engines have actual CUDA/AVX implementations
- Git-agent is a functional repo-native system

**Aspirational / Experimental:**
- Many plato-tile-* and plato-room-* repos are stubs
- Ternary repos were created in a burst (AI-assisted)
- Legacy language ports (COBOL, Fortran) are novelty exercises
- Performance claims need independent verification

---

## repo-docs System

The **repo-docs** system is the detailed reference for the entire ecosystem. It contains:

### MASTER-INDEX.md
- Complete statistics and overview
- Top 20 standout repos
- All 12 thematic clusters with descriptions
- Language distribution
- Quality assessment framework
- Integration points

### ECOSYSTEM-ANALYSIS.md
- Deep analysis of SuperInstance's core thesis
- Conservation law governance framework
- Dependency graphs and architectural relationships
- Maturity matrix for each sub-ecosystem
- Consolidation recommendations

### Individual Repo Docs (~2,700 files)
Each repository has its own `.md` file with:
- README content
- Code quality indicators
- Dependencies
- Test coverage
- Related repos

### How to Use repo-docs

1. **Browse the Index** — Start with `MASTER-INDEX.md` for overview
2. **Deep Dive** — Read `ECOSYSTEM-ANALYSIS.md` for understanding
3. **Find Specifics** — Look up individual repos in the `/repo-docs/` directory

The repo-docs system is the **canonical reference** for the SuperInstance ecosystem. This unified wiki is the **entry point** — repo-docs is the deep reference.

---

## Ecosystem Maturity

| Sub-ecosystem | Repos | Maturity | Notes |
|---|---|---|---|
| **FLUX VM** | 164 | 🔨 Prototype | Core VMs work, no production deployments |
| **PLATO** | 262 | 🔨 Prototype | Server exists, rooms concept is strong |
| **Ternary math** | 370 | 🧪 Experimental | Real math, unclear practical value |
| **Constraint theory** | 45 | 🧪 Experimental | Genuine algorithms, needs validation |
| **Conservation laws** | 58 | 📐 Theoretical | Sound math, novel governance |
| **Fleet orchestration** | 257 | 🔨 Prototype | I2I protocol designed, not deployed |
| **LAU math** | ~50 | ✅ Usable | Real implementations with tests |
| **Edge/embedded** | ~30 | 🔨 Prototype | C99/Zig/ESP32 code is practical |
| **Git-Native Agents** | ~10 | 🔨 Prototype | Functional, novel approach |

---

## Language Distribution

| Language | Approximate | Primary Use |
|----------|-------------|-------------|
| Rust | 1,200+ | Core infrastructure, math, FLUX |
| Python | 800+ | PLATO, AI/ML, tooling |
| TypeScript/JS | 300+ | Web interfaces, SDKs |
| C | 150+ | Embedded, CUDA, performance |
| CUDA | 80+ | GPU acceleration |
| Go | 70+ | Distributed systems |
| Others | 500+ | Java, Ruby, Zig, Elixir, Chapel, Fortran, etc. |

---

## Design Principles

1. **Conservation First** — Every operation conserves energy (γ + η = C)
2. **Deadband Governance** — Only signal when change exceeds threshold
3. **Deterministic Bytecode** — Agent logic should be auditable
4. **Repo-Native** — Git as the nervous system for agents
5. **Ternary Logic** — {-1, 0, +1} for richer state representation
6. **Musical Coordination** — Harmony, rhythm, counterpoint for fleets
7. **Spatial Knowledge** — Rooms and tiles for organizing information
8. **Mathematical Foundation** — Real math underlying everything

---

## Related Projects

SuperInstance is part of a broader vision for autonomous AI systems:

- **OpenConstruct** — Agent onboarding platform
- **Cocapn** — Fleet orchestration and agent runtime
- **ForgeFlux** — Tile decomposition ecosystem

---

## Contributing

SuperInstance is primarily a research ecosystem, but contributions are welcome:

1. **Real Code** — Working implementations, tests, documentation
2. **Consolidation** — Merge stub repos into meaningful monorepos
3. **Verification** — Independent testing of performance claims
4. **Documentation** — Improve repo-docs entries

---

## License

All SuperInstance repositories are **Apache 2.0 licensed**.

---

## Navigation

- **[MASTER-INDEX.md](MASTER-INDEX.md)** — Complete ecosystem index
- **[ECOSYSTEM-ANALYSIS.md](ECOSYSTEM-ANALYSIS.md)** — Deep analysis
- **[Individual Repo Docs](./)** — Browse by repository name
- **[GitHub Organization](https://github.com/SuperInstance)** — Source code

---

*Last Updated: 2026-07-12*
*This unified wiki replaces superinstance-wiki, wiki, knowledge-agent, and fleet-wiki*
