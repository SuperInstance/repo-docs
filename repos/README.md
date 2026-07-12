# Repos Directory — SuperInstance Category Index

Each subdirectory contains individual `.md` documentation files for repos in that category, plus a README with expanded analysis.

## Categories

| Directory | Count | Description |
|-----------|-------|-------------|
| [ternary-math/](ternary-math/) | 371 | Balanced ternary {-1,0,+1} computing: types, search, neural networks, compilers, physics, chemistry |
| [plato-system/](plato-system/) | 264 | PLATO knowledge rooms: server, runtime, engine blocks, JEPA models, portal, torch |
| [flux-bytecode/](flux-bytecode/) | 166 | FLUX deterministic bytecode ISA: VMs, assemblers, compilers, hardware backends (CUDA, FPGA, WebGPU) |
| [fleet-infra/](fleet-infra/) | 266 | Fleet orchestration: conductor, oracle, relay, dashboard, metrics, matrix bridge, MIDI coordination |
| [lau-mathematics/](lau-mathematics/) | 409 | Mathematical foundations: Lie algebra, Lie groups, Hodge theory, graph spectral, Adinkra symbols |
| [constraint-theory/](constraint-theory/) | 46 | Constraint satisfaction: CSP solvers, Hamiltonian mechanics, Laman rigidity, fermentation metaphors |
| [conservation-laws/](conservation-laws/) | 59 | Conservation law governance (γ+η=C): multilingual implementations, CI/CD, ternary entropy |
| [music-spectral/](music-spectral/) | 31 | Spectral music theory: chord nodes, voice-leading edges, counterpoint as constraint satisfaction |
| [edge-embedded/](edge-embedded/) | 59 | Edge computing: ESP32 clients, vessel bridge, holodeck-c, kintsugi-math-c, relay agents |
| [oxide-gpu/](oxide-gpu/) | 42 | Distributed GPU compute: CUDA kernels, async dispatch, bf16 tools, MEP protocol |
| [a2a-a2ui/](a2a-a2ui/) | 8 | Agent-to-agent & agent-to-UI protocols: A2A bridge, A2UI component rendering |
| [superinstance-core/](superinstance-core/) | 51 | Core org tooling: spreadsheets, protocol, embedder, FFI, harness, ecosystem management |
| [cocapn-marine/](cocapn-marine/) | 11 | Marine instrumentation: NMEA 0183, autopilot PID, bathymetric recording, sonar vision |
| [agent-framework/](agent-framework/) | 9 | Git-native agent frameworks: repo-as-brain, ability transfer, operations patterns |
| [exocortex-memory/](exocortex-memory/) | 11 | Persistent cognitive substrate: S3-compatible memory, dream cycles, knowledge bases |
| [persona-ai/](persona-ai/) | 11 | Persona engine: decompose/dial/compose personalities, character SDK, voice |
| [roblox-gaming/](roblox-gaming/) | 11 | Roblox/Luau: game build framework, CraftMind agents, Scrapcraft |
| [dev-tools/](dev-tools/) | 16 | Development tools: Snapkit, API generators, testing harnesses |
| [forge-tiles/](forge-tiles/) | 39 | Forge pattern decomposition: tile lifecycle, sketch systems, fleet tiles |
| [sheaf-topology/](sheaf-topology/) | 19 | Sheaf theory & algebraic topology for agent knowledge spaces |
| [entropy-physics/](entropy-physics/) | 35 | Thermodynamic computing: entropy analysis, symplectic integration, tropical algebra |
| [activelog/](activelog/) | 11 | Activity logging: ActiveLog MVP, backend, Claude plugin, AI pages |
| [equipment-catalog/](equipment-catalog/) | 14 | Edge equipment taxonomy & vessel room navigation |
| [openconstruct/](openconstruct/) | 6 | OpenConstruct: ESP32 client, agent onboarding, shell commands |
| [zeroclaw/](zeroclaw/) | 21 | ZeroClaw experiments: nightly scripts, reports, chain logic |
| [misc/](misc/) | 1200 | Everything else: algorithms, experiments, one-offs, research prototypes |

## How Repos Are Organized

Each repo has a `.md` file named `{prefix}-{repo-name}.md` containing:

- **Intention** — Why this repo exists
- **How it works** — Technical approach
- **What it's for** — Practical use case
- **Who would use it** — Target audience
- **Language/Stack** — Primary technologies
- **Status assessment** — Active, stale, abandoned, or complete
- **Honest assessment** — Real project vs auto-generated artifact

## Cross-References

Many repos span categories. The LAU mathematics libraries, for example, provide foundations used by both the ternary and constraint-theory ecosystems. See `../docs/01-overview/MASTER-INDEX.md` for cross-cutting relationships.
