# SuperInstance Master Index

**Last Updated:** 2026-07-12  
**Total Repos:** ~4,098 (3,327 original, 771 forks)  
**Documented Repos:** ~2,700 (individual `.md` files in `/repo-docs/`)  

---

## Quick Stats

| Metric | Count |
|--------|-------|
| Total repos in organization | 4,098 |
| Original repos | 3,327 |
| Forked repos | 771 |
| Major thematic clusters | 12 |
| Languages represented | 25+ |
| Stale/archived wiki repos | 4 |

---

## Top 20 Standout Repos

The most substantial, real projects in the SuperInstance ecosystem:

1. **plato-server** — Standalone PLATO knowledge system, run your own, connect to fleet (15KB README)
2. **plato-runtime-kernel** — AI theorem prover, conservation-verified computation (6.4KB README)
3. **plato-engine-block-c** — Tiny embeddable sensor→history→alarm engine in C99, zero dynamic allocation (10KB)
4. **plato-engine-block-elixir** — Fault-tolerant marine vessel monitoring on BEAM/OTP (14KB)
5. **plato-engine-block-zig** — Embedded engine block implementation (12KB)
6. **plato-engine-block** — Atomic room runtime for Plato Matrix, universal agent-space interface (8.4KB)
7. **flux-runtime** — Deterministic bytecode ISA runtime for agentic logic, assembler, compiler, VM (9.3KB)
8. **flux-vm** — FLUX-C constraint VM: 50 opcodes, stack-based, DAL A certifiable, TrustZone-style (7.7KB)
9. **flux-hardware** — FLUX hardware backends: CUDA, AVX-512, Fortran, FPGA, eBPF, WebGPU (11KB)
10. **ternary-science** — Scientific computation over balanced ternary {-1, 0, +1} (4.1MB)
11. **plato-torch** — GPU forge, PyTorch training loop with tile framing (7.3KB)
12. **plato-portal** — Web interface for PLATO (7.7KB)
13. **plato-audio-jepa** — Audio JEPA implementation (4KB)
14. **plato-vision-jepa** — Vision JEPA implementation (3.8KB)
15. **ternary-compiler-v2** — Advanced ternary compilation pipeline with IR and code generation
16. **lau-hodge-theory** — Hodge theory for agent knowledge spaces, 43 tests (535 lines)
17. **lau-lie-algebra** — Lie algebra implementation, 54 tests (514 lines)
18. **lau-lie-group-agents** — Lie groups for agent systems (526 lines)
19. **exocortex** — Persistent cognitive substrate for multi-agent systems, S3-compatible (2.5KB)
20. **git-agent** — Repo-native agent that lives in git, the shell IS the agent (3.4KB)

---

## Ecosystem Architecture

The SuperInstance ecosystem is organized around several interconnected systems:

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
   ┌────▼───┐ ┌───▼───┐ ┌──▼───┐ ┌───▼────┐ ┌─▼─────┐
   │  LAU   │ │ Forge │ │Grand │ │Exocortex│ │Agent  │
   │ (300+) │ │Flux │ │Pattern│ │  (20+)  │ │Fleet  │
   │ Math/  │ │ (20) │ │ (60) │ │ Memory  │ │Infra  │
   │Physics │ │ Tile │ │Graph │ │         │ │(100+) │
   └────────┘ │Decomp│ │Diff  │ │         │ └───────┘
              └──────┘ └──────┘ └─────────┘
```

### Key Connections

- **PLATO → FLUX**: PLATO knowledge tiles can be compiled into FLUX bytecode for execution
- **FLUX → Ternary**: FLUX constraint engines use ternary logic for safety checks
- **Lau → All**: Lau math libraries underpin constraint theory, spectral analysis, and agent cognition
- **ForgeFlux**: Decomposes any input (code, audio, image, text) into PLATO tiles
- **Exocortex**: Provides persistent memory substrate for all agent systems
- **Git-Agent**: Repo-native agents use PLATO rooms for knowledge storage

---

## Thematic Clusters

### 1. PLATO Ecosystem (262 repos)

**Description:** Room-based agent system where knowledge is stored as tiles within rooms. Agents navigate between rooms using deadband protocol for priority governance.

**Key Components:**
- Core Infrastructure: plato-server, plato-runtime, plato-kernel, plato-core
- Engine Blocks: Multi-language room runtimes (Rust, C, Elixir, Zig, Chapel)
- Tile Processing: Tile format, encoding, search, ranking, validation
- Agent Framework: plato-sdk, plato-client, plato-ship, plato-scout
- ML/AI: plato-jepa, plato-mythos, plato-torch, plato-distill
- Clients: JS, PHP, Ruby, Python SDKs
- Vessels: IoT/embedded PLATO clients (ESP32, RP2040)

**Notable Repos:** plato-server, plato-runtime-kernel, plato-engine-block-*, plato-torch, plato-mythos

---

### 2. FLUX Ecosystem (165 repos)

**Description:** Bytecode virtual machines and compiler infrastructure for AI agents. Deterministic bytecode enables verifiable, auditable, sandboxed agent execution.

**Key Components:**
- Core VMs: flux-core (Rust), flux-runtime (Python), flux-vm, flux-zig, flux-js
- Constraint Engines: flux-check-*, flux-fracture, constraint satisfaction
- Hardware Acceleration: flux-hardware, CUDA, AVX-512, FPGA, eBPF backends
- Agent Coordination: A2A signaling protocol, mesh networking
- Natural Language: 80+ language programming runtimes
- Legacy Ports: COBOL, Fortran, ALGOL, MUMPS, SNOBOL, PL/I, RPG IV

**Notable Repos:** flux-runtime, flux-vm, flux-hardware, flux-compiler, flux-multilingual

---

### 3. Ternary Computing (370 repos)

**Description:** Balanced ternary computation over {-1, 0, +1}. Neural networks, GPU optimization, distributed systems, cryptography, game theory, and more built on ternary logic.

**Key Areas:**
- Neural Networks/ML: tnn, attention, activation, gradient, llm, checkpoint
- GPU/Kernels: cuda-kernels, pack, dispatch, register-file, warp-block
- Distributed Systems: consensus, paxos, lease, mirror, version
- Agent/Fleet: agent, captain, navigator, helm, anchor, beacon
- Math/Physics: ising, quantum, hamiltonian, gauge-theory
- Music/Audio: music, jam, harmonic, tempo, rhythm, timbre
- Data Structures: btree, heap, bloom-filter, cache, database
- Compiler/Tooling: compiler, interpreter, cli, auto-vectorizer

**Notable Repos:** ternary-science, ternary-compiler-v2, ternary-cuda-kernels, ternary-tnn

---

### 4. Lau Mathematical Libraries (300+ repos)

**Description:** Comprehensive mathematical and scientific computing libraries in Rust, organized as `lau-*` crates. The mathematical foundation for much of the ecosystem.

**Categories:**
- **Algebra/Topology:** Category theory, algebraic topology, homology, cohomology
- **Analysis:** Functional analysis, complex analysis, measure theory
- **Geometry:** Differential geometry, symplectic geometry, Riemannian geometry
- **Physics:** Electromagnetism, fluid dynamics, quantum topology, thermodynamics
- **Agent Theory:** Game theory, control theory, dynamical systems, ergodic theory
- **Numerical:** Linear algebra, PDE solvers, optimization, approximation theory
- **Information:** Information theory, information geometry, entropy
- **Computation:** GPU compute, CUDA, distributed systems, compilers

**Notable Repos:** lau-hodge-theory, lau-lie-algebra, lau-contact-geometry, lau-symplectic-topology, lau-numerical-pde

---

### 5. Grand Pattern (60 repos)

**Description:** Fibonacci dual-direction architecture for cellular graph intelligence. Multi-language implementation of graph diffusion systems with JEPA prediction.

**Components:**
- Core: grand-pattern-core, grand-pattern-mono (corrected architecture)
- Language Implementations: Rust, Python, TypeScript, Go, Java, Swift, Mojo, Zig, C, Fortran, Chapel
- GPU/Parallel: CUDA, OpenCL, PTX, SIMD, Vulkan
- Networking: UDP gossip, TCP transport, peer discovery
- Topology: Venue-as-agent, spectral analysis, consensus

**Notable Repos:** grand-pattern-rs, grand-pattern-py, grand-pattern-cuda, grand-pattern-mono

---

### 6. ForgeFlux (20 repos)

**Description:** Tile decomposition ecosystem. Converts any input (code, audio, image, text, sensor data) into PLATO knowledge tiles.

**Decomposers:**
- forge-code: Source code → tiles
- forge-audio/forge-soniqo: Audio → tiles
- forge-image: Images → tiles
- forge-text: Text → tiles
- forge-sensor: Sensor data → tiles
- forge-subtitle: Subtitles → tiles

**Infrastructure:**
- forge-pipeline: Orchestration
- forge-meta: Registry and discovery
- forge-memory: External tile storage

---

### 7. Exocortex (20+ repos)

**Description:** Persistent cognitive substrate for multi-agent systems. S3-compatible distributed memory with language clients.

**Components:**
- Core: exocortex (Python), exocortex-memory-zig (Zig)
- Clients: C++, JS, Lua, CircuitPython
- Bridges: MCP (TypeScript), WASM runtime
- Distributed: Chapel PGAS fleet coordination

---

### 8. Git-Agent / Repo-Native Agents (10+ repos)

**Description:** Agents that live in git repositories. The repo IS the agent. Git IS the nervous system.

**Components:**
- git-agent: Repo-native agent framework
- git-agent-standard: Standard implementation
- git-agent-codespace: Codespace template
- git-native-mud: Zero-server MUD using git primitives
- cocapn: Repo-first agent runtime

---

### 9. Constraint Theory & Conservation (50+ repos)

**Description:** Mathematical framework for constraint satisfaction, conservation laws, and deadband protocols.

**Key Areas:**
- Core Theory: Constraint-theory-core, fracture-coalesce algorithms
- Conservation: Conservation spectral analysis, entropy conservation
- Deadband: Deadband protocol implementation across languages
- GPU: CUDA constraint engines (1B+ checks/sec)
- Applications: Climate, financial, ecosystem, code conservation

**Notable Repos:** cuda-constraint-engine, avx512-constraint-checker, deadband-protocol, c-ternary

---

### 10. Hodge Theory & Spectral Analysis (30+ repos)

**Description:** Hodge decomposition for multi-agent coordination, spectral gap analysis, consensus mechanisms.

**Applications:**
- Consensus: Hodge decomposition of agent disagreements
- Music: Harmonic analysis via holonomy
- Belief: Hodge belief theory
- Graphs: Spectral graph theory, Fiedler vectors

**Notable Repos:** hodge-consensus-rs, holonomy-harmony, graph-spectral, heat-spectral

---

### 11. Agent Fleet Infrastructure (100+ repos)

**Description:** Coordination, governance, and infrastructure for multi-agent fleets.

**Components:**
- Shells: construct-core, construct, crab (hermit crab shells)
- Coordination: categorical-agents, consensus-protocol, beacon-protocol
- Governance: court (proposals, votes, constitutional constraints)
- Vessels: cocapn, aboracle, activeledger, captaine
- Messaging: bottle-protocol, i2i-protocol, a2a-signal

**Notable Repos:** construct-core, crab, categorical-agents, consensus-protocol

---

### 12. Maritime & Commercial Fishing (20+ repos)

**Description:** AI tools for commercial fishing, vessel operations, and maritime logistics.

**Applications:**
- vessel tracking and fuel monitoring
- crew management and coordination
- catch tracking and species identification
- weather integration and route optimization

**Notable Repos:** deckboss-net, captains-log, capitaine-agent, fishermanscopilot

---

## Quality Assessment

### By Documentation Quality

| Quality | Count | Percentage | Description |
|---------|-------|------------|-------------|
| **Substantial** | ~800 | 30% | Rich docs, architecture, motivation (README > 2000 bytes) |
| **Real Project** | ~400 | 15% | Working code, examples, proper docs |
| **Moderate** | ~600 | 22% | Some substance, likely AI-assisted |
| **Lightweight** | ~500 | 19% | Brief docs, small utility or exercise |
| **Stub** | ~200 | 7% | Minimal, possibly placeholder |
| **Auto-generated** | ~200 | 7% | Generic template, fleet branding |
| **No README** | ~200 | 7% | No documentation available |

### Real vs Aspirational

**What's Real:**
- PLATO server and runtime have working implementations
- FLUX VMs (flux-core, flux-runtime, flux-zig) have genuine code
- Lau math libraries contain real mathematical implementations
- Constraint engines have actual CUDA/AVX implementations
- Git-agent is a functional repo-native agent system

**What's Aspirational:**
- Many plato-tile-* and plato-room-* repos are stubs
- Ternary repos were created in a 10-day burst (AI-assisted generation)
- Legacy language ports (COBOL, Fortran, ALGOL) are novelty/exercises
- Multilingual runtimes are research-grade, not production
- Performance claims need independent verification

**The Pattern:**
This is a single developer/small team rapidly prototyping an entire ecosystem. The Rust crates are the core; other languages fill gaps; multi-language implementations demonstrate portability. More impressive in breadth than depth, but the depth where it exists is genuine.

---

## Stale Wiki Repos

The following 4 repos are stale wiki/documentation repositories that are no longer actively maintained:

1. **superinstance-wiki** — Original wiki, archived
2. **wiki** — General wiki placeholder, no recent updates
3. **knowledge-agent** — Early knowledge management experiment, superseded by PLATO
4. **fleet-wiki** — Fleet documentation wiki, stale

**Note:** Current documentation efforts are focused on the PLATO ecosystem and individual repo READMEs.

---

## Language Distribution

| Language | Approximate Count | Primary Use |
|----------|------------------|-------------|
| Rust | 1,200+ | Core infrastructure, Lau math, ternary, FLUX |
| Python | 800+ | PLATO, AI/ML, constraint theory, tooling |
| TypeScript/JS | 300+ | Web interfaces, agents, SDKs |
| C | 150+ | Embedded, CUDA, performance-critical paths |
| CUDA | 80+ | GPU acceleration |
| Go | 70+ | Distributed systems, tools |
| Java | 50+ | Enterprise integrations |
| Ruby | 40+ | DSLs, scripting |
| PHP | 30+ | Web backends |
| Zig | 30+ | Embedded, performance |
| Elixir | 20+ | Distributed systems |
| Chapel | 20+ | HPC |
| Fortran | 15+ | Scientific computing |
| Mojo | 10+ | Next-gen language experiments |
| Others | 100+ | Lua, Swift, C++, C#, etc. |

---

## Key Architectural Patterns

### 1. Repo-Native Agents
Agents live in git repos. The repo IS the agent. Git IS the nervous system. Commits are state transitions; branches are parallel explorations.

### 2. Knowledge as Tiles
PLATO tiles are Q&A pairs with confidence, provenance, and dependencies. Rooms contain tiles. Rooms compute their conservation ratio.

### 3. Deadband Protocol
Three-tier priority governance: P0 (safety/danger), P1 (channel/safe paths), P2 (optimize/efficiency). Train safe channels, not danger catalogs.

### 4. Constraint Theory
Conservation laws govern agent systems. Zero-drift constraints prevent divergence. Spectral analysis detects anomalies.

### 5. Bytecode Agents
FLUX bytecode enables verifiable, sandboxed agent execution. Deterministic semantics for auditability.

### 6. Hermit Crab Architecture
Agents find repos, grow, move shells. Crab provides the shell-swapping infrastructure.

### 7. Grand Pattern
Fibonacci dual-direction architecture for cellular graph intelligence. Venues are agents. JEPA provides prediction.

### 8. Ternary Computing
Balanced {-1, 0, +1} logic for compact state representation and efficient computation.

---

## Integration Points

| System | Connects To | Via |
|--------|-------------|-----|
| PLATO | FLUX | flux-plato-bridge, bytecode tiles |
| PLATO | ForgeFlux | Tile decomposition APIs |
| PLATO | Exocortex | Memory substrate |
| FLUX | Ternary | Constraint checking |
| Lau | All | Mathematical foundation |
| Git-Agent | PLATO | Knowledge storage |
| Grand Pattern | PLATO | Venue-as-agent pattern |
| Hodge Theory | Fleet | Consensus mechanisms |

---

## How to Navigate This Ecosystem

### For Developers
1. Start with **plato-server** for the knowledge system
2. Explore **flux-runtime** for bytecode execution
3. Use **lau-\*** math crates for scientific computing
4. Check **construct-core** for agent runtime
5. See **git-agent** for repo-native patterns

### For Researchers
1. **Constraint theory**: cuda-constraint-engine, c-ternary
2. **Hodge theory**: hodge-consensus-rs, holonomy-harmony
3. **Ternary computing**: ternary-science, ternary-compiler-v2
4. **Grand Pattern**: grand-pattern-rs, grand-pattern-mono
5. **Category theory**: categorical-agents, lau-category-theory

### For ML/AI
1. **PLATO ML**: plato-jepa, plato-mythos, plato-torch
2. **Ternary ML**: ternary-tnn, ternary-attention, ternary-grad
3. **JEPA**: jepa-core, jepa-predict
4. **Distillation**: plato-distill, plato-forge-daemon

### For Infrastructure
1. **Coordination**: consensus-protocol, beacon-protocol
2. **Messaging**: i2i-protocol, bottle-protocol, a2a-signal
3. **Memory**: exocortex, plato-memory
4. **Compute**: flux-hardware, gpu-accelerator

---

## Future Directions

1. **Consolidation**: Many stub repos could be merged or archived
2. **Verification**: Performance and test claims need independent validation
3. **Documentation**: Continue expanding individual repo docs
4. **Integration**: Better connect PLATO, FLUX, Ternary, and Lau systems
5. **Standardization**: Common protocols and formats across fleets
6. **Production Hardening**: Move from experimental to production-ready

---

## Acknowledgments

This ecosystem represents an ambitious attempt to build a complete infrastructure for AI agents, from mathematical foundations to practical deployment. While breadth exceeds depth in many areas, the core implementations (PLATO, FLUX, Lau math) contain genuine innovation and technical substance.

---

*Generated 2026-07-12 from individual repo documentation files in `/repo-docs/`*
