# SuperInstance Repo Documentation

Documentation for the **SuperInstance** GitHub organization — **4,098 repositories** exploring ternary computing, agent fleets, mathematical physics, constraint theory, and more.

---

## Directory Guide

The documentation is organized into 27 subdirectories by theme. Each has its own README with detailed analysis.

### Major Ecosystems

| Directory | Repos | Description |
|-----------|-------|-------------|
| [ternary-math](./ternary-math/) | 370 | Balanced ternary {-1, 0, +1} computation — neural networks, GPU kernels, distributed systems, cryptography, physics, music. The largest single-theme ecosystem. |
| [plato-system](./plato-system/) | 263 | PLATO (Protocol for Layered Agent Tile Orchestration) — room-based knowledge system with tiles, deadband protocol, multi-language engine blocks. |
| [flux-bytecode](./flux-bytecode/) | 165 | FLUX Virtual Machine — Turing-incomplete bytecode ISA for AI agents, with cross-language runtimes (Rust, Python, Ruby, C). |
| [fleet-infra](./fleet-infra/) | 265 | Fleet orchestration — conductor, oracle, relay, dashboard, thermodynamic clock, consciousness index. Kubernetes for AI agents. |
| [lau-mathematics](./lau-mathematics/) | 409 | LAU math foundations — Lie algebras, Hodge theory, spectral graphs, tropical geometry, category theory, Eisenstein integers, Grand Pattern. |
| [misc](./misc/) | 1,200 | Everything else — algorithms, tools, games, experiments, one-off prototypes across 1,200 repos. |

### Theory & Foundations

| Directory | Repos | Description |
|-----------|-------|-------------|
| [constraint-theory](./constraint-theory/) | 45 | Geometric constraint satisfaction — CSP solvers, Hamiltonian constraints, Laman rigidity, Eisenstein lattice snapping. |
| [conservation-laws](./conservation-laws/) | 58 | The γ + η = C conservation law — Monte Carlo verification, 9+ language implementations, CI/CD governance. |
| [entropy-physics](./entropy-physics/) | 35 | Entropy and compression — BWT, Huffman, LZ77, RLE, entropy flow, thermodynamic modeling. |
| [sheaf-topology](./sheaf-topology/) | 19 | Sheaf theory and Hodge theory for agents — belief propagation, consensus, music analysis via sheaves. |

### Infrastructure & Tooling

| Directory | Repos | Description |
|-----------|-------|-------------|
| [superinstance-core](./superinstance-core/) | 51 | Core SuperInstance libraries — CLI, catalog, conservation, curvature agents, core C implementations. |
| [edge-embedded](./edge-embedded/) | 58 | Edge computing — ESP32, Jetson, ARM64, holodeck simulation, OpenConstruct ABI, vessel marine nodes, kintsugi fault tolerance. |
| [dev-tools](./dev-tools/) | 16 | Developer tooling — cross-compilation, crates publishing, build tools. |
| [equipment-catalog](./equipment-catalog/) | 14 | Equipment and hardware catalog. |
| [a2a-a2ui](./a2a-a2ui/) | 7 | Agent-to-Agent and Agent-to-UI protocols. |
| [openconstruct](./openconstruct/) | 6 | Agent onboarding framework — C ABI with language bindings. |

### Compute & Performance

| Directory | Repos | Description |
|-----------|-------|-------------|
| [oxide-gpu](./oxide-gpu/) | 42 | GPU computing — kernels, accelerators, annealing, benchmarks, persistent homology on GPU, scaling studies. |
| [forge-tiles](./forge-tiles/) | 39 | Tile processing pipeline — A2A, audio, code archaeology, data detection, image processing, FLUX integration. |

### AI & Agents

| Directory | Repos | Description |
|-----------|-------|-------------|
| [agent-framework](./agent-framework/) | 9 | Agent framework core. |
| [ai-research](./ai-research/) | 6 | AI research notes and experiments. |
| [persona-ai](./persona-ai/) | 11 | AI personas and character definitions. |
| [exocortex-memory](./exocortex-memory/) | 11 | Memory systems for AI agents. |
| [activelog](./activelog/) | 11 | Activity logging and monitoring. |
| [zeroclaw](./zeroclaw/) | 21 | ZeroClaw — companion agent framework. |

### Domain Applications

| Directory | Repos | Description |
|-----------|-------|-------------|
| [music-spectral](./music-spectral/) | 30 | Music and spectral analysis — counterpoint engines, musician souls, Cayley graphs, clustering, conservation. |
| [cocapn-marine](./cocapn-marine/) | 11 | Marine/maritime applications — Cocapn fleet for ocean environments. |
| [roblox-gaming](./roblox-gaming/) | 11 | Roblox gaming experiments. |

---

## Statistics

| Metric | Value |
|--------|-------|
| Total repos documented | 4,098 |
| Total .md doc files | 3,210 |
| Documented directories | 27 |
| Primary languages | Rust, Python, C, CUDA, TypeScript, Go, Zig, Elixir, Chapel, Lean |
| Creation window | June 2026 (burst pattern over ~10 days) |
| Largest category | misc (1,200 repos) |
| Largest single-theme | lau-mathematics (409 repos) |

---

## Cross-Cutting Themes

Several themes appear across multiple directories:

### Ternary Logic {-1, 0, +1}
The balanced ternary philosophy pervades everything. The [ternary-math](./ternary-math/) ecosystem has 370 repos. PLATO rooms use ternary sensors. FLUX bytecode has ternary-aware operations. Conservation laws track ternary distributions. LAU math works over Z₃.

### Conservation (γ + η = C)
The conservation invariant appears in [conservation-laws](./conservation-laws/), [entropy-physics](./entropy-physics/), [fleet-infra](./fleet-infra/) (conservation-aware scheduling), and [constraint-theory](./constraint-theory/) (Noether's theorem connecting symmetry to conservation).

### Sheaves & Hodge Theory
Sheaf-theoretic approaches appear in [sheaf-topology](./sheaf-topology/), [lau-mathematics](./lau-mathematics/) (lau-hodge-theory), and across PLATO rooms (belief propagation via Hodge decomposition).

### Multi-Language Polyglot
Nearly every core concept is implemented in 5+ languages. OpenConstruct has 12+ SDKs. The conservation law has 9+ implementations. Grand Pattern spans 15+ languages. Engine blocks come in Rust, C, Elixir, Gleam, Zig, Chapel.

### Fleet Coordination
The agent fleet concept ties together [fleet-infra](./fleet-infra/) (orchestration), [plato-system](./plato-system/) (knowledge rooms), [edge-embedded](./edge-embedded/) (physical devices), and [a2a-a2ui](./a2a-a2ui/) (communication protocols).

---

## How to Explore

1. **Start with** [ternary-math](./ternary-math/) — the largest and most self-contained ecosystem
2. **Then** [plato-system](./plato-system/) — the knowledge architecture
3. **Then** [fleet-infra](./fleet-infra/) — how agents are orchestrated
4. **For math depth** [lau-mathematics](./lau-mathematics/) — the theoretical foundations
5. **For practical tools** [misc](./misc/) — algorithms, utilities, experiments
6. **For theory** [constraint-theory](./constraint-theory/) and [conservation-laws](./conservation-laws/)

Each subdirectory README provides a thematic overview, key repos, architecture diagrams, and honest assessments of what's real vs. aspirational.

---

## Origin

The SuperInstance GitHub organization created ~4,098 repositories in a burst pattern during June 2026. The repos span an extraordinary range — from production-quality Rust crates to experimental stubs, from deep mathematics to whimsical games. The ecosystem appears to be heavily AI-assisted in generation but contains genuine domain-specific implementations with real mathematical content.

---

*Last updated: July 2026*
