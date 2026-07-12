# Lau Mathematics — Index

**Total repos: 409**

The largest and most central category in the SuperInstance ecosystem. The Lau mathematics collection encompasses the theoretical and implementation layer for a mathematically-grounded AI agent framework. It covers pure mathematics (algebraic geometry, category theory, topology, measure theory), applied mathematics (control theory, optimization, signal processing), computational implementations across a dozen languages, and the PLATO/LAU game engine that teaches advanced math through gameplay.

## Category Overview

The Lau Mathematics category is the mathematical heart of the SuperInstance ecosystem. It can be understood as four interlocking layers:

### 1. Mathematical Foundations (~200 repos)

Pure mathematics crates implementing specific domains:
- **Algebra & Number Theory:** lau-algebraic-geometry, lau-number-theory, lau-lie-algebra, lau-galois-agents, lau-representation-theory
- **Topology & Geometry:** lau-algebraic-topology, lau-differential-topology, lau-symplectic-geometry, lau-kahler-geometry, lau-tropical-geometry, lau-mirror-symmetry
- **Analysis:** lau-complex-analysis, lau-functional-analysis, lau-measure-theory, lau-harmonic-analysis, lau-ergodic-theory
- **Probability & Statistics:** lau-probability-theory, lau-stochastic-processes, lau-bayesian-update, lau-queueing-theory
- **Modern Physics Math:** lau-quantum-topology, lau-relativity, lau-electromagnetism, lau-fluid-dynamics, lau-thermodynamics

### 2. Agent Systems (~80 repos)

Mathematical agent frameworks where deep math meets AI coordination:
- **Agent Runtime:** lau-agent-runtime (self-compiling agents), lau-agent-lifecycle, lau-agent-homeostasis, lau-agent-thermodynamics
- **Geometric Agents:** lau-ricci-flow-agents, lau-symplectic-agent, lau-tropical-agent, lau-koopman-agents, lau-morse-homology-agents
- **Fleet Math:** lau-mean-field-agents, lau-noether-agents, lau-renormalization-agents, lau-diffusion-agents

### 3. Polyglot Implementations & Grand Pattern (~60 repos)

The Grand Pattern toolkit — a unified mathematical framework ported to 20+ languages:
- **Core:** grand-pattern-core (Rust), grand-pattern-mono (unified), grand-pattern-design
- **Language Ports:** grand-pattern-c, grand-pattern-go, grand-pattern-java, grand-pattern-zig, grand-pattern-swift, grand-pattern-fortran, grand-pattern-chapel, grand-pattern-mojo, grand-pattern-wasm
- **Compute Targets:** grand-pattern-cuda, grand-pattern-opencl, grand-pattern-ptx, grand-pattern-gpu, grand-pattern-simd
- **Eisenstein Integers:** eisenstein-c, eisenstein-cuda, eisenstein-wasm, eisenstein-triples, eisenstein-vs-z2

### 4. PLATO/LAU Game Engine (~50 repos)

An educational game engine teaching git and AI through gameplay:
- **Core:** lau-tutorial (interactive learning), lau-vibe-compiler (NL→PLATO ops), lau-vibe-field, lau-vibe-visualizer
- **Game Systems:** lau-spatial, lau-biome, lau-quest, lau-scheduler, lau-genealogy, lau-recipe, lau-audio
- **Education:** lau-git-world (version control through play), lau-ai-tutor, lau-plato-tutor

### Key Interconnections

- The **Lau ecosystem** is the mathematical foundation feeding into nearly every other category
- **Conservation laws** (lau-conservation-laws, lau-conservation-engine) connect to the standalone conservation-laws category
- **Sheaf theory** (lau-sheaf-cohomology, lau-sheaf-neural, lau-sheaf-learning) connects to the sheaf-topology category
- **PLATO integration** (lau-plato-integration, lau-plato-nervous) ties into the PLATO system category
- **Grand Pattern** ports provide the polyglot keystone for cross-language fleet operations
- **Agent systems** connect to the agent-framework and superinstance-core categories

## Full Repository Listing

### Lau Core & Ecosystem

| Repo | Language | Description |
|------|----------|-------------|
| [lau-ecosystem](./other-lau-ecosystem.md) | | Ecosystem overview |
| [lau-ecosystem-unified](./other-lau-ecosystem-unified.md) | | Unified ecosystem description |
| [lau-architecture](./other-lau-architecture.md) | | Architectural documentation |
| [lau-blueprint](./other-lau-blueprint.md) | | Design blueprint |
| [lau-mission](./other-lau-mission.md) | | Mission statement |
| [lau-guides](./other-lau-guides.md) | | Guides and documentation |
| [lau-onboarding](./other-lau-onboarding.md) | | Onboarding materials |
| [lau-leaderboard](./other-lau-leaderboard.md) | | Leaderboard system |
| [lau-bench](./other-lau-bench.md) | | Benchmark suite |
| [lau-grand-unification](./other-lau-grand-unification.md) | | Grand unification framework |

### Lau Mathematical Domains — Pure Math

| Repo | Language | Description |
|------|----------|-------------|
| [lau-algebraic-geometry](./other-lau-algebraic-geometry.md) | Rust | Algebraic geometry |
| [lau-algebraic-topology](./other-lau-algebraic-topology.md) | Rust | Algebraic topology |
| [lau-category-theory](./other-lau-category-theory.md) | Rust | Category theory |
| [lau-combinatorics](./other-lau-combinatorics.md) | Rust | Combinatorics |
| [lau-complex-analysis](./other-lau-complex-analysis.md) | Rust | Complex analysis |
| [lau-derivative-topos](./other-lau-derived-topos.md) | Rust | Derived topoi |
| [lau-differential-topology](./other-lau-differential-topology.md) | Rust | Differential topology |
| [lau-functional-analysis](./other-lau-functional-analysis.md) | Rust | Functional analysis |
| [lau-geometric-measure](./other-lau-geometric-measure.md) | Rust | Geometric measure theory |
| [lau-harmonic-analysis](./other-lau-harmonic-analysis.md) | Rust | Harmonic analysis |
| [lau-homotopy-type](./other-lau-homotopy-type.md) | Rust | Homotopy type theory |
| [lau-kahler-geometry](./other-lau-kahler-geometry.md) | Rust | Kähler geometry |
| [lau-lie-algebra](./other-lau-lie-algebra.md) | Rust | Lie algebra |
| [lau-measure-theory](./other-lau-measure-theory.md) | Rust | Measure theory |
| [lau-mirror-symmetry](./other-lau-mirror-symmetry.md) | Rust | Mirror symmetry |
| [lau-number-theory](./other-lau-number-theory.md) | Rust | Number theory |
| [lau-representation-theory](./other-lau-representation-theory.md) | Rust | Representation theory |
| [lau-symplectic-geometry](./other-lau-symplectic-geometry.md) | Rust | Symplectic geometry |
| [lau-symplectic-topology](./other-lau-symplectic-topology.md) | Rust | Symplectic topology |
| [lau-topological-data-analysis](./other-lau-topological-data-analysis.md) | Rust | TDA |
| [lau-tropical-geometry](./other-lau-tropical-geometry.md) | Rust | Tropical geometry |
| [lau-ergodic-theory](./other-lau-ergodic-theory.md) | Rust | Ergodic theory |
| [lau-stochastic-geometry](./other-lau-stochastic-geometry.md) | Rust | Stochastic geometry |
| [lau-stochastic-homotopy](./other-lau-stochastic-homotopy.md) | Rust | Stochastic homotopy |
| [lau-chaos-theory](./other-lau-chaos-theory.md) | Rust | Chaos theory |
| [lau-information-theory](./other-lau-information-theory.md) | Rust | Information theory |
| [lau-logic-foundations](./other-lau-logic-foundations.md) | Rust | Logic foundations |
| [lau-categorical-homotopy](./other-lau-categorical-homotopy.md) | Rust | Categorical homotopy |
| [lau-categorical-mechanics](./other-lau-categorical-mechanics.md) | Rust | Categorical mechanics |
| [lau-noncommutative-agents](./other-lau-noncommutative-agents.md) | Rust | Noncommutative geometry agents |

### Lau Mathematical Domains — Applied Math & Physics

| Repo | Language | Description |
|------|----------|-------------|
| [lau-control-theory](./other-lau-control-theory.md) | Rust | Control theory |
| [lau-convex-optimization](./other-lau-convex-optimization.md) | Rust | Convex optimization |
| [lau-electromagnetism](./other-lau-electromagnetism.md) | Rust | Electromagnetism |
| [lau-fluid-dynamics](./other-lau-fluid-dynamics.md) | Rust | Fluid dynamics |
| [lau-game-theory](./other-lau-game-theory.md) | Rust | Game theory |
| [lau-graph-theory](./other-lau-graph-theory.md) | Rust | Graph theory |
| [lau-network-science](./other-lau-network-science.md) | Rust | Network science |
| [lau-numerical-linear-algebra](./other-lau-numerical-linear-algebra.md) | Rust | Numerical linear algebra |
| [lau-numerical-pde](./other-lau-numerical-pde.md) | Rust | Numerical PDEs |
| [lau-optimization](./other-lau-optimization.md) | Rust | Optimization |
| [lau-probability-theory](./other-lau-probability-theory.md) | Rust | Probability theory |
| [lau-quantum-topology](./other-lau-quantum-topology.md) | Rust | Quantum topology |
| [lau-relativity](./other-lau-relativity.md) | Rust | Relativity |
| [lau-solid-mechanics](./other-lau-solid-mechanics.md) | Rust | Solid mechanics |
| [lau-signal-processing](./other-lau-signal-processing.md) | Rust | Signal processing |
| [lau-statistical-learning](./other-lau-statistical-learning.md) | Rust | Statistical learning |
| [lau-thermodynamics](./other-lau-thermodynamics.md) | Rust | Thermodynamics |
| [lau-time-series](./other-lau-time-series.md) | Rust | Time series analysis |
| [lau-dynamical-systems](./other-lau-dynamical-systems.md) | Rust | Dynamical systems |
| [lau-database-theory](./other-lau-database-theory.md) | Rust | Database theory |
| [lau-operating-systems](./other-lau-operating-systems.md) | Rust | OS theory |
| [lau-distributed-systems](./other-lau-distributed-systems.md) | Rust | Distributed systems |
| [lau-cryptography](./other-lau-cryptography.md) | Rust | Cryptography |
| [lau-error-correcting-codes](./other-lau-error-correcting-codes.md) | Rust | Error-correcting codes |
| [lau-robotics](./other-lau-robotics.md) | Rust | Robotics |
| [lau-trading](./other-lau-trading.md) | Rust | Trading mathematics |

### Lau Agent Systems

| Repo | Language | Description |
|------|----------|-------------|
| [lau-agent-runtime](./other-lau-agent-runtime.md) | Rust | Self-compiling agent runtime |
| [lau-agent-lifecycle](./other-lau-agent-lifecycle.md) | Rust | Agent lifecycle management |
| [lau-agent-homeostasis](./other-lau-agent-homeostasis.md) | Rust | Agent homeostasis |
| [lau-agent-organism](./other-lau-agent-organism.md) | Rust | Agent as organism |
| [lau-agent-profile](./other-lau-agent-profile.md) | Rust | Agent profiles |
| [lau-agent-shell](./other-lau-agent-shell.md) | Rust | Agent shell |
| [lau-agent-thermodynamics](./other-lau-agent-thermodynamics.md) | Rust | Agent thermodynamics |
| [lau-agent-topology](./other-lau-agent-topology.md) | Rust | Agent topology |
| [lau-agent-unify](./other-lau-agent-unify.md) | Rust | Agent unification |
| [lau-agent-dream](./other-lau-agent-dream.md) | Rust | Agent dream consolidation |
| [lau-self-aware-agent](./other-lau-self-aware-agent.md) | Rust | Self-aware agent |
| [lau-self-modeling](./other-lau-self-modeling.md) | Rust | Self-modeling agents |
| [lau-complex-agents](./other-lau-complex-agents.md) | Rust | Complex agent systems |
| [lau-swarm-intelligence](./other-lau-swarm-intelligence.md) | Rust | Swarm intelligence |
| [lau-spectral-agent](./other-lau-spectral-agent.md) | Rust | Spectral agent framework |
| [lau-symplectic-agent](./other-lau-symplectic-agent.md) | Rust | Symplectic agent |

### Lau Geometric/Topological Agents

| Repo | Language | Description |
|------|----------|-------------|
| [lau-conformal-agents](./other-lau-conformal-agents.md) | Rust | Conformal geometry agents |
| [lau-contact-agents](./other-lau-contact-agents.md) | Rust | Contact geometry agents |
| [lau-diffusion-agents](./other-lau-diffusion-agents.md) | Rust | Diffusion agents |
| [lau-distribution-agents](./other-lau-distribution-agents.md) | Rust | Distribution agents |
| [lau-ergodic-gradient](./other-lau-ergodic-gradient.md) | Rust | Ergodic gradient agents |
| [lau-free-probability-agents](./other-lau-free-probability-agents.md) | Rust | Free probability agents |
| [lau-functor-network](./other-lau-functor-network.md) | Rust | Functor networks |
| [lau-game-theory-agents](./other-lau-game-theory-agents.md) | Rust | Game-theoretic agents |
| [lau-geometric-deep-learning](./other-lau-geometric-deep-learning.md) | Rust | Geometric deep learning |
| [lau-hodge-decomposition-agents](./other-lau-hodge-decomposition-agents.md) | Rust | Hodge decomposition agents |
| [lau-information-geometry-agents](./other-lau-information-geometry-agents.md) | Rust | Information geometry agents |
| [lau-kahler-agents](./other-lau-kahler-agents.md) | Rust | Kähler agents |
| [lau-kalman-hodge](./other-lau-kalman-hodge.md) | Rust | Kalman-Hodge filtering |
| [lau-koopman-agents](./other-lau-koopman-agents.md) | Rust | Koopman operator agents |
| [lau-lie-group-agents](./other-lau-lie-group-agents.md) | Rust | Lie group agents |
| [lau-mean-field-agents](./other-lau-mean-field-agents.md) | Rust | Mean field agents |
| [lau-measure-agents](./other-lau-measure-agents.md) | Rust | Measure-theoretic agents |
| [lau-modular-agents](./other-lau-modular-agents.md) | Rust | Modular agents |
| [lau-morse-homology-agents](./other-lau-morse-homology-agents.md) | Rust | Morse homology agents |
| [lau-noether-agents](./other-lau-noether-agents.md) | Rust | Noether agents |
| [lau-numerical-agents](./other-lau-numerical-agents.md) | Rust | Numerical agents |
| [lau-pde-agents](./other-lau-pde-agents.md) | Rust | PDE agents |
| [lau-probability-agents](./other-lau-probability-agents.md) | Rust | Probability agents |
| [lau-quantum-groups-agents](./other-lau-quantum-groups-agents.md) | Rust | Quantum group agents |
| [lau-quantum-topology-agents](./other-lau-quantum-topology-agents.md) | Rust | Quantum topology agents |
| [lau-renormalization-agents](./other-lau-renormalization-agents.md) | Rust | Renormalization agents |
| [lau-ricci-curvature-agents](./other-lau-ricci-curvature-agents.md) | Rust | Ricci curvature agents |
| [lau-ricci-flow-agents](./other-lau-ricci-flow-agents.md) | Rust | Ricci flow agents |
| [lau-signal-processing-agents](./other-lau-signal-processing-agents.md) | Rust | Signal processing agents |
| [lau-sobolev-agents](./other-lau-sobolev-agents.md) | Rust | Sobolev agents |
| [lau-teleomorphic](./other-lau-teleomorphic.md) | Rust | Teleomorphic agents |
| [lau-tropical-agent](./other-lau-tropical-agent.md) | Rust | Tropical agent |
| [lau-tropical-geometry-agents](./other-lau-tropical-geometry-agents.md) | Rust | Tropical geometry agents |
| [lau-twistor-agents](./other-lau-twistor-agents.md) | Rust | Twistor agents |

### Lau Conservation & Sheaf

| Repo | Language | Description |
|------|----------|-------------|
| [lau-conservation-engine](./other-lau-conservation-engine.md) | Rust | Conservation engine |
| [lau-conservation-experiment](./other-lau-conservation-experiment.md) | Rust | Conservation experiments |
| [lau-conservation-guard](./other-lau-conservation-guard.md) | Rust | Conservation guard |
| [lau-conservation-laws](./other-lau-conservation-laws.md) | Rust | Noether/CRDT conservation |
| [lau-conservation-matrix](./other-lau-conservation-matrix.md) | Rust | Conservation matrix |
| [lau-conservation-spectral](./other-lau-conservation-spectral.md) | Rust | Spectral conservation |
| [lau-sheaf-automata](./other-lau-sheaf-automata.md) | Rust | Sheaf automata |
| [lau-sheaf-cohomology](./other-lau-sheaf-cohomology.md) | Rust | Sheaf cohomology |
| [lau-sheaf-learning](./other-lau-sheaf-learning.md) | Rust | Sheaf learning |
| [lau-sheaf-neural](./other-lau-sheaf-neural.md) | Rust | Sheaf neural networks |
| [lau-sheaf-spectrum](./other-lau-sheaf-spectrum.md) | Rust | Sheaf spectrum |
| [lau-calm-crdt](./other-lau-calm-crdt.md) | Rust | CALM CRDT |
| [lau-calm-noether](./other-lau-calm-noether.md) | Rust | CALM Noether theorem |

### Lau Math Polyglot Implementations

| Repo | Language | Description |
|------|----------|-------------|
| [lau-math-c](./other-lau-math-c.md) | C | C99 math primitives (edge-ready) |
| [lau-math-cuda](./other-lau-math-cuda.md) | CUDA | GPU math kernels |
| [lau-math-go](./other-lau-math-go.md) | Go | Go math library |
| [lau-math-chapel](./other-lau-math-chapel.md) | Chapel | Chapel parallel math |
| [lau-math-opencl](./other-lau-math-opencl.md) | OpenCL | Cross-vendor GPU math |
| [lau-math-wasm](./other-lau-math-wasm.md) | WebAssembly | WASM math |

### Lau Game Engine (PLATO/LAU)

| Repo | Language | Description |
|------|----------|-------------|
| [lau-tutorial](./other-lau-tutorial.md) | Rust | Interactive tutorial (git+AI through play) |
| [lau-vibe-compiler](./other-lau-vibe-compiler.md) | Rust | NL→PLATO compiler |
| [lau-vibe-field](./other-lau-vibe-field.md) | Rust | Vibe field |
| [lau-vibe-visualizer](./other-lau-vibe-visualizer.md) | Rust | Vibe visualizer |
| [lau-spatial](./other-lau-spatial.md) | Rust | Spatial indexing |
| [lau-biome](./other-lau-biome.md) | Rust | Procedural biomes |
| [lau-quest](./other-lau-quest.md) | Rust | Quest system |
| [lau-scheduler](./other-lau-scheduler.md) | Rust | Game loop scheduler |
| [lau-genealogy](./other-lau-genealogy.md) | Rust | Entity lineage |
| [lau-recipe](./other-lau-recipe.md) | Rust | Crafting system |
| [lau-audio](./other-lau-audio.md) | Rust | Game audio |
| [lau-animation](./other-lau-animation.md) | Rust | Animation system |
| [lau-camera](./other-lau-camera.md) | Rust | Camera system |
| [lau-noise](./other-lau-noise.md) | Rust | Noise generation |
| [lau-physics](./other-lau-physics.md) | Rust | Physics engine |
| [lau-render](./other-lau-render.md) | Rust | Rendering |
| [lau-terrain](./other-lau-terrain.md) | Rust | Terrain generation |
| [lau-voxel](./other-lau-voxel.md) | Rust | Voxel system |
| [lau-worldgen](./other-lau-worldgen.md) | Rust | World generation |
| [lau-git-world](./other-lau-git-world.md) | Rust | Git-based world versioning |
| [lau-ai-tutor](./other-lau-ai-tutor.md) | Rust | AI tutor |
| [lau-plato-tutor](./other-lau-plato-tutor.md) | Rust | PLATO tutor |
| [lau-plato-integration](./other-lau-plato-integration.md) | Rust | PLATO integration |
| [lau-plato-nervous](./other-lau-plato-nervous.md) | Rust | PLATO nervous system |
| [lau-ecs](./other-lau-ecs.md) | Rust | Entity component system |
| [lau-event-bus](./other-lau-event-bus.md) | Rust | Event bus |
| [lau-input](./other-lau-input.md) | Rust | Input handling |
| [lau-session](./other-lau-session.md) | Rust | Session management |
| [lau-replay](./other-lau-replay.md) | Rust | Replay system |
| [lau-narrator](./other-lau-narrator.md) | Rust | Narrative engine |
| [lau-dialogue](./other-lau-dialogue.md) | Rust | Dialogue system |
| [lau-mission](./other-lau-mission.md) | Rust | Mission system |
| [lau-challenge](./other-lau-challenge.md) | Rust | Challenge system |
| [lau-skilltree](./other-lau-skilltree.md) | Rust | Skill tree |
| [lau-achievements](./other-lau-achievements.md) | Rust | Achievement system |
| [lau-leaderboard](./other-lau-leaderboard.md) | Rust | Leaderboard |
| [lau-pet](./other-lau-pet.md) | Rust | Pet companion system |
| [lau-soundtrack](./other-lau-soundtrack.md) | Rust | Soundtrack system |
| [lau-room-acoustics](./other-lau-room-acoustics.md) | Rust | Room acoustics |
| [lau-room-native](./other-lau-room-native.md) | Rust | Native rooms |
| [lau-training-room](./other-lau-training-room.md) | Rust | Training room |

### Lau Shell & Infrastructure

| Repo | Language | Description |
|------|----------|-------------|
| [lau-shell-interface](./other-lau-shell-interface.md) | Rust | Shell interface |
| [lau-shell-kernel](./other-lau-shell-kernel.md) | Rust | Shell kernel |
| [lau-shell-lifecycle](./other-lau-shell-lifecycle.md) | Rust | Shell lifecycle |
| [lau-shell-spawn](./other-lau-shell-spawn.md) | Rust | Shell spawning |
| [lau-shell-transport](./other-lau-shell-transport.md) | Rust | Shell transport |
| [lau-state-machine](./other-lau-state-state-machine.md) | Rust | State machine |
| [lau-scheduler-theory](./other-lau-scheduling-theory.md) | Rust | Scheduling theory |
| [lau-collections](./other-lau-collections.md) | Rust | Collections |
| [lau-compression](./other-lau-compression.md) | Rust | Compression |
| [lau-serialization](./other-lau-serialization.md) | Rust | Serialization |
| [lau-ringbuf](./other-lau-ringbuf.md) | Rust | Ring buffer |
| [lau-ringbuf-c](./other-lau-ringbuf-c.md) | C | Ring buffer in C |
| [lau-memory-arena](./other-lau-memory-arena.md) | Rust | Memory arena |
| [lau-memory-tiles](./other-lau-memory-tiles.md) | Rust | Memory tiles |
| [lau-feedback](./other-lau-feedback.md) | Rust | Feedback system |
| [lau-intention](./other-lau-intention.md) | Rust | Intention system |
| [lau-intention-field](./other-lau-intention-field.md) | Rust | Intention field |
| [lau-observation-control](./other-lau-observation-control.md) | Rust | Observation control |
| [lau-domestication](./other-lau-domestication.md) | Rust | Agent domestication |
| [lau-inheritance](./other-lau-inheritance.md) | Rust | Inheritance system |

### Lau Networking & Protocols

| Repo | Language | Description |
|------|----------|-------------|
| [lau-a2a-protocol](./other-lau-a2a-protocol.md) | Rust | Agent-to-agent protocol |
| [lau-a2ui](./other-lau-a2ui.md) | Rust | A2UI integration |
| [lau-a2ui-protocol](./other-lau-a2ui-protocol.md) | Rust | A2UI protocol |
| [lau-network](./other-lau-network.md) | Rust | Networking |
| [lau-protocol](./other-lau-protocol.md) | Rust | Protocol framework |
| [lau-protocol-binary](./other-lau-protocol-binary.md) | Rust | Binary protocol |
| [lau-murmur-protocol-v2](./other-lau-murmur-protocol-v2.md) | Rust | Murmur protocol v2 |
| [lau-ensign](./other-lau-ensign.md) | Rust | Ensign protocol |
| [lau-ensign-sdk](./other-lau-ensign-sdk.md) | Rust | Ensign SDK |
| [lau-port](./other-lau-port.md) | Rust | Port abstraction |
| [lau-port-v2](./other-lau-port-v2.md) | Rust | Port v2 |
| [lau-bridge](./other-lau-bridge.md) | Rust | Bridge system |
| [lau-ts-bridge](./other-lau-ts-bridge.md) | Rust | TS bridge |
| [lau-wasm-bridge](./other-lau-wasm-bridge.md) | Rust | WASM bridge |
| [lau-ffi-bindings](./other-lau-ffi-bindings.md) | Rust | FFI bindings |
| [lau-inter-shell](./other-lau-inter-shell.md) | Rust | Inter-shell comms |
| [lau-cudaclaw-bridge](./other-lau-cudaclaw-bridge.md) | Rust | CUDAclaw bridge |

### Lau Advanced Math & Theory

| Repo | Language | Description |
|------|----------|-------------|
| [lau-connes-spectral-triple](./other-lau-connes-spectral-triple.md) | Rust | Connes spectral triple |
| [lau-index-theorem](./other-lau-index-theorem.md) | Rust | Index theorem |
| [lau-dg-algebra](./other-lau-dg-algebra.md) | Rust | DG algebra |
| [lau-supergeometry](./other-lau-supergeometry.md) | Rust | Supergeometry |
| [lau-naturality-boundary](./other-lau-naturality-boundary.md) | Rust | Naturality boundary |
| [lau-fixedpoint](./other-lau-fixedpoint.md) | Rust | Fixed point theory |
| [lau-singular-spde](./other-lau-singular-spde.md) | Rust | Singular SPDEs |
| [lau-varadhan-transport](./other-lau-varadhan-transport.md) | Rust | Varadhan transport |
| [lau-variational-methods](./other-lau-variational-methods.md) | Rust | Variational methods |
| [lau-approximation-theory](./other-lau-approximation-theory.md) | Rust | Approximation theory |
| [lau-matrix-analysis](./other-lau-matrix-analysis.md) | Rust | Matrix analysis |
| [lau-tensor-analysis](./other-lau-tensor-analysis.md) | Rust | Tensor analysis |
| [lau-trace-monoid](./other-lau-trace-monoid.md) | Rust | Trace monoid |
| [lau-banach-agents](./other-lau-banach-agents.md) | Rust | Banach space agents |
| [lau-dirichlet-space](./other-lau-dirichlet-space.md) | Rust | Dirichlet space |
| [lau-spectral-zeta](./other-lau-spectral-zeta.md) | Rust | Spectral zeta |
| [lau-spectral-gap-experiment](./other-lau-spectral-gap-experiment.md) | Rust | Spectral gap experiment |
| [lau-eigenfunction-policy](./other-lau-eigenfunction-policy.md) | Rust | Eigenfunction policy |
| [lau-dynamical-algebra](./other-lau-dynamical-algebra.md) | Rust | Dynamical algebra |

### Lau Learning & RL

| Repo | Language | Description |
|------|----------|-------------|
| [lau-reinforcement-learning](./other-lau-reinforcement-learning.md) | Rust | RL fundamentals |
| [lau-reinforcement-learning-advanced](./other-lau-reinforcement-learning-advanced.md) | Rust | Advanced RL |
| [lau-thermal-rl](./other-lau-thermal-rl.md) | Rust | Thermal RL |
| [lau-witten-reward](./other-lau-witten-reward.md) | Rust | Witten deformation reward |
| [lau-reward-hacking-detector](./other-lau-reward-hacking-detector.md) | Rust | Reward hacking detection |
| [lau-neural-networks](./other-lau-neural-networks.md) | Rust | Neural networks |
| [lau-evolutionary-computation](./other-lau-evolutionary-computation.md) | Rust | Evolutionary computation |
| [lau-evolution](./other-lau-evolution.md) | Rust | Evolution simulator |
| [lau-fuzzy-logic](./other-lau-fuzzy-logic.md) | Rust | Fuzzy logic |

### Lau Special Topics

| Repo | Language | Description |
|------|----------|-------------|
| [lau-consciousness-bridge](./other-lau-consciousness-bridge.md) | Rust | Consciousness bridge |
| [lau-griot](./other-lau-griot.md) | Rust | Griot tradition |
| [lau-songline](./other-lau-songline.md) | Rust | Songline navigation |
| [lau-quipu](./other-lau-quipu.md) | Rust | Quipu encoding |
| [lau-adinkra](./other-lau-adinkra.md) | Rust | Adinkra symbols |
| [lau-palaver](./other-lau-palaver.md) | Rust | Palaver dialogue |
| [lau-penrose](./other-lau-penrose.md) | Rust | Penrose tilings |
| [lau-penrose-v2](./other-lau-penrose-v2.md) | Rust | Penrose v2 |
| [lau-penrose-growth](./other-lau-penrose-growth.md) | Rust | Penrose growth |
| [lau-kintsugi](./other-lau-kintsugi.md) | Rust | Kintsugi philosophy |
| [lau-kintsugi-runtime](./other-lau-kintsugi-runtime.md) | Rust | Kintsugi runtime |
| [lau-rhythm-nation](./other-lau-rhythm-nation.md) | Rust | Rhythm nation |
| [lau-landauer-meter](./other-lau-landauer-meter.md) | Rust | Landauer limit meter |
| [lau-constellation](./other-lau-constellation.md) | Rust | Constellation mapping |
| [lau-affordance](./other-lau-affordance.md) | Rust | Affordance theory |
| [lau-tensor-midi](./other-lau-tensor-midi.md) | Rust | Tensor MIDI |
| [lau-simd-vibe](./other-lau-simd-vibe.md) | Rust | SIMD vibe |
| [lau-weather](./other-lau-weather.md) | Rust | Weather system |
| [lau-voice](./other-lau-voice.md) | Rust | Voice system |

### Lau Sia2 Engine

| Repo | Language | Description |
|------|----------|-------------|
| [lau-sia2-engine](./other-lau-sia2-engine.md) | Rust | Sia2 engine |
| [lau-sia2-engine-c](./other-lau-sia2-engine-c.md) | C | Sia2 C port |
| [lau-sia2-engine-go](./other-lau-sia2-engine-go.md) | Go | Sia2 Go port |
| [lau-sia2-engine-wasm](./other-lau-sia2-engine-wasm.md) | WASM | Sia2 WASM |

### Lau Bytecode & Compilers

| Repo | Language | Description |
|------|----------|-------------|
| [lau-bytecode](./other-lau-bytecode.md) | Rust | Bytecode VM |
| [lau-bytecode-c](./other-lau-bytecode-c.md) | C | Bytecode in C |
| [lau-compilers](./other-lau-compilers.md) | Rust | Compiler toolkit |
| [lau-docs-dream-compiler-spec](./other-lau-docs-dream-compiler-spec.md) | | Dream compiler spec |
| [lau-docs-quest-design](./other-lau-docs-quest-design.md) | | Quest design docs |
| [lau-docs-voice-patterns](./other-lau-docs-voice-patterns.md) | | Voice pattern docs |

### Lau Provenance & Identity

| Repo | Language | Description |
|------|----------|-------------|
| [lau-provenance](./other-lau-provenance.md) | Rust | Provenance tracking |
| [lau-provenance-chain](./other-lau-provenance-chain.md) | Rust | Provenance chain |
| [lau-reputation](./other-lau-reputation.md) | Rust | Reputation system |
| [lau-provider](./other-lau-provider.md) | Rust | Provider abstraction |
| [lau-token-economy](./other-lau-token-economy.md) | Rust | Token economy |
| [lau-constitutive-compute](./other-lau-constitutive-compute.md) | Rust | Constitutive compute |

### Lau Shell Systems & Integration

| Repo | Language | Description |
|------|----------|-------------|
| [lau-collab](./other-lau-collab.md) | Rust | Collaboration |
| [lau-closure](./other-lau-closure.md) | Rust | Closure system |
| [lau-glue](./other-lau-glue.md) | Rust | Glue layer |
| [lau-tick-runtime](./other-lau-tick-runtime.md) | Rust | Tick runtime |
| [lau-async-tick](./other-lau-async-tick.md) | Rust | Async tick |
| [lau-tminus](./other-lau-tminus.md) | Rust | T-minus countdown |
| [lau-time](./other-lau-time.md) | Rust | Time system |
| [lau-cloud-deploy](./other-lau-cloud-deploy.md) | Rust | Cloud deployment |
| [lau-gateway-demo](./other-lau-gateway-demo.md) | Rust | Gateway demo |
| [lau-seven-eyes-demo](./other-lau-seven-eyes-demo.md) | Rust | Seven eyes demo |
| [lau-integration-test](./other-lau-integration-test.md) | Rust | Integration tests |
| [lau-hermes-oracle-boot](./other-lau-hermes-oracle-boot.md) | Rust | Hermes oracle boot |
| [lau-resolvent-leverage](./other-lau-resolvent-leverage.md) | Rust | Resolvent leverage |
| [lau-leverage-singularity](./other-lau-leverage-singularity.md) | Rust | Leverage singularity |
| [lau-natural-language](./other-lau-natural-language.md) | Rust | Natural language |
| [lau-functional-programming](./other-lau-functional-programming.md) | Rust | Functional programming |
| [lau-prerequisite](./other-lau-prerequisite.md) | Rust | Prerequisite graph |
| [lau-gpu-compute](./other-lau-gpu-compute.md) | Rust | GPU compute |
| [lau-construct](./other-lau-construct.md) | Rust | Construct API |
| [lau-construct-cli](./other-lau-construct-cli.md) | Rust | Construct CLI |
| [lau-construct-integration](./other-lau-construct-integration.md) | Rust | Construct integration |
| [lau-construct-integration-v2](./other-lau-construct-integration-v2.md) | Rust | Construct integration v2 |
| [lau-protocol](./other-lau-protocol.md) | Rust | Protocol system |
| [lau-mirror-control](./other-lau-mirror-control.md) | Rust | Mirror control |
| [lau-gradient-ricci](./other-lau-gradient-ricci.md) | Rust | Ricci gradient |
| [lau-jepa-gravity](./other-lau-jepa-gravity.md) | Rust | JEPA gravity |
| [lau-hodge-theory](./other-lau-hodge-theory.md) | Rust | Hodge theory |
| [lau-dynamical-systems-agents](./other-lau-dynamical-systems-agents.md) | Rust | Dynamical systems agents |
| [lau-dg-algebra](./other-lau-dg-algebra.md) | Rust | DG algebra |
| [lau-gravity-field](./other-lau-gravity-field.md) | Rust | Gravity field |
| [lau-hardware-abstract](./other-lau-hardware-abstract.md) | Rust | Hardware abstraction |
| [lau-control-theory-agents](./other-lau-control-theory-agents.md) | Rust | Control theory agents |
| [lau-persistent-homology](./other-lau-persistent-homology.md) | Rust | Persistent homology |
| [lau-persistence-experiment](./other-lau-persistence-experiment.md) | Rust | Persistence experiment |
| [lau-free-probability](./other-lau-free-probability.md) | Rust | Free probability |
| [lau-fibonacci-growth](./other-lau-fibonacci-growth.md) | Rust | Fibonacci growth |
| [lau-geometric-growth](./other-lau-geometric-growth.md) | Rust | Geometric growth |
| [lau-linear-systems](./other-lau-linear-systems.md) | Rust | Linear systems |
| [lau-stochastic-processes](./other-lau-stochastic-processes.md) | Rust | Stochastic processes |
| [lau-morse-theory](./other-lau-morse-theory.md) | Rust | Morse theory |
| [lau-renormalization](./other-lau-renormalization.md) | Rust | Renormalization |
| [lau-symmetry-engine](./other-lau-symmetry-engine.md) | Rust | Symmetry engine |
| [lau-optimal-transport-agents](./other-lau-optimal-transport-agents.md) | Rust | Optimal transport agents |
| [lau-optimal-control](./other-lau-optimal-control.md) | Rust | Optimal control |
| [lau-queueing-theory](./other-lau-queueing-theory.md) | Rust | Queueing theory |
| [lau-narrator](./other-lau-narrator.md) | Rust | Narrator |
| [lau-network-science](./other-lau-network-science.md) | Rust | Network science |
| [lau-computer-graphics](./other-lau-computer-graphics.md) | Rust | Computer graphics |
| [lau-computer-vision](./other-lau-computer-vision.md) | Rust | Computer vision |
| [lau-evolution](./other-lau-evolution.md) | Rust | Evolution |
| [lau-tile-compress](./other-lau-tile-compress.md) | Rust | Tile compression |
| [lau-tile-store](./other-lau-tile-store.md) | Rust | Tile storage |
| [lau-dynamical-algebra](./other-lau-dynamical-algebra.md) | Rust | Dynamical algebra |
| [lau-tradition-proof](./other-lau-tradition-proof.md) | Rust | Tradition proof |
| [lau-polyglot-tradition](./other-lau-polyglot-tradition.md) | Rust | Polyglot tradition |
| [lau-destruction-transform](./other-lau-destruction-transform.md) | Rust | Destruction transform |
| [lau-bridge-pattern-math](./other-lau-bridge-pattern-math.md) | Rust | Bridge pattern math |
| [lau-bridge-tutor](./other-lau-bridge-tutor.md) | Rust | Bridge tutor |
| [lau-git-agent](./other-lau-git-agent.md) | Rust | Git agent |
| [lau-git-render](./other-lau-git-render.md) | Rust | Git rendering |
| [lau-bench](./other-lau-bench.md) | Rust | Benchmarks |
| [lau-ensign](./other-lau-ensign.md) | Rust | Ensign |
| [lau-ensign-sdk](./other-lau-ensign-sdk.md) | Rust | Ensign SDK |
| [lau-narrator](./other-lau-narrator.md) | Rust | Narrator |

### Grand Pattern

| Repo | Language | Description |
|------|----------|-------------|
| [grand-pattern-core](./other-grand-pattern-core.md) | Rust | Unified GP core |
| [grand-pattern-mono](./other-grand-pattern-mono.md) | Rust | Mono vibe unified |
| [grand-pattern-design](./other-grand-pattern-design.md) | Rust | Design document |
| [grand-pattern-abi](./other-grand-pattern-abi.md) | Rust | C ABI polyglot keystone |
| [grand-pattern-rs](./other-grand-pattern-rs.md) | Rust | Rust implementation |
| [grand-pattern-c](./other-grand-pattern-c.md) | C | C implementation |
| [grand-pattern-go](./other-grand-pattern-go.md) | Go | Go implementation |
| [grand-pattern-java](./other-grand-pattern-java.md) | Java | Java implementation |
| [grand-pattern-zig](./other-grand-pattern-zig.md) | Zig | Zig implementation |
| [grand-pattern-swift](./other-grand-pattern-swift.md) | Swift | Swift implementation |
| [grand-pattern-fortran](./other-grand-pattern-fortran.md) | Fortran | Fortran implementation |
| [grand-pattern-chapel](./other-grand-pattern-chapel.md) | Chapel | Chapel implementation |
| [grand-pattern-mojo](./other-grand-pattern-mojo.md) | Mojo | Mojo implementation |
| [grand-pattern-ts](./other-grand-pattern-ts.md) | TypeScript | TS implementation |
| [grand-pattern-py](./other-grand-pattern-py.md) | Python | Python implementation |
| [grand-pattern-wasm](./other-grand-pattern-wasm.md) | WASM | WASM target |
| [grand-pattern-cuda](./other-grand-pattern-cuda.md) | CUDA | GPU kernels |
| [grand-pattern-opencl](./other-grand-pattern-opencl.md) | OpenCL | OpenCL kernels |
| [grand-pattern-ptx](./other-grand-pattern-ptx.md) | PTX | PTX assembly |
| [grand-pattern-gpu](./other-grand-pattern-gpu.md) | GPU | GPU general |
| [grand-pattern-simd](./other-grand-pattern-simd.md) | SIMD | SIMD intrinsics |
| [grand-pattern-net](./other-grand-pattern-net.md) | | Network layer |
| [grand-pattern-store](./other-grand-pattern-store.md) | | Storage layer |
| [grand-pattern-topology](./other-grand-pattern-topology.md) | | Topology |
| [grand-pattern-sim](./other-grand-pattern-sim.md) | | Simulation |
| [grand-pattern-kit](./other-grand-pattern-kit.md) | | Development kit |
| [grand-pattern-cli](./other-grand-pattern-cli.md) | Rust | CLI tool |
| [grand-pattern-ffi](./other-grand-pattern-ffi.md) | Rust | FFI bindings |
| [grand-pattern-flux](./other-grand-pattern-flux.md) | Rust | FLUX integration |
| [grand-pattern-integration](./other-grand-pattern-integration.md) | Rust | Integration tests |
| [grand-pattern-experiments](./other-grand-pattern-experiments.md) | Rust | Experiments |
| [grand-pattern-embedded](./other-grand-pattern-embedded.md) | Rust | Embedded target |
| [grand-pattern-bench](./other-grand-pattern-bench.md) | Rust | Benchmarks |
| [grand-pattern-bench-v2](./other-grand-pattern-bench-v2.md) | Rust | Benchmarks v2 |
| [grand-pattern-adversarial](./other-grand-pattern-adversarial.md) | Rust | Adversarial testing |
| [grand-pattern-claude](./other-grand-pattern-claude.md) | | Claude integration |
| [grand-pattern-kimi](./other-grand-pattern-kimi.md) | | Kimi integration |
| [grand-pattern-venue](./other-grand-pattern-venue.md) | | Venue system |
| [grand-pattern-mono-go](./other-grand-pattern-mono-go.md) | Go | Mono Go |
| [grand-pattern-mono-py](./other-grand-pattern-mono-py.md) | Python | Mono Python |
| [grand-pattern-mono-ts](./other-grand-pattern-mono-ts.md) | TypeScript | Mono TS |
| [grand-synthesis](./other-grand-synthesis.md) | Rust | Grand synthesis |

### Eisenstein Integers

| Repo | Language | Description |
|------|----------|-------------|
| [eisenstein-c](./other-eisenstein-c.md) | C | ~1KB hex arithmetic |
| [eisenstein-cuda](./other-eisenstein-cuda.md) | CUDA | GPU Eisenstein |
| [eisenstein-wasm](./other-eisenstein-wasm.md) | WASM | WASM Eisenstein |
| [eisenstein-triples](./other-eisenstein-triples.md) | Rust | Eisenstein triples |
| [eisenstein-tools](./other-eisenstein-tools.md) | Rust | Tooling |
| [eisenstein-bench](./other-eisenstein-bench.md) | Rust | Benchmarks |
| [eisenstein-ai-landing](./other-eisenstein-ai-landing.md) | HTML | Landing page |
| [eisenstein-embed](./other-eisenstein-embed.md) | Rust | Embeddings |
| [eisenstein-quantize](./other-eisenstein-quantize.md) | Rust | Quantization |
| [eisenstein-fuzz](./other-eisenstein-fuzz.md) | Rust | Fuzzing |
| [eisenstein-do178c](./other-eisenstein-do178c.md) | Rust | DO-178C safety-critical |
| [eisenstein-snap-python](./other-eisenstein-snap-python.md) | Python | Python snapshot |
| [eisenstein-vs-z2](./other-eisenstein-vs-z2.md) | Rust | vs Z² comparison |
| [eisenstein-vs-z2-c](./other-eisenstein-vs-z2-c.md) | C | vs Z² in C |
| [eisenstein-vs-z2-rs](./other-eisenstein-vs-z2-rs.md) | Rust | vs Z² in Rust |

### Graph Algorithms

| Repo | Language | Description |
|------|----------|-------------|
| [graph-algorithms](./other-graph-algorithms.md) | Rust | Core graph algorithms |
| [graph-centrality](./other-graph-centrality.md) | Rust | Centrality measures |
| [graph-coloring](./other-graph-coloring.md) | Rust | Graph coloring |
| [graph-coloring-rs](./other-graph-coloring-rs.md) | Rust | Coloring in Rust |
| [graph-flow](./other-graph-flow.md) | Rust | Network flow |
| [graph-homology](./other-graph-homology.md) | Rust | Graph homology |
| [graph-neural](./other-graph-neural.md) | Rust | Graph neural networks |
| [graph-planarity](./other-graph-planarity.md) | Rust | Planarity testing |
| [graph-search-rs](./other-graph-search-rs.md) | Rust | Search algorithms |
| [graph-spectral](./other-graph-spectral.md) | Rust | Spectral graph theory |
| [graph-thermodynamics](./other-graph-thermodynamics.md) | Rust | Graph thermodynamics |
| [graph-walker-go](./other-graph-walker-go.md) | Go | Graph walker |

### Vector & Utilities

| Repo | Language | Description |
|------|----------|-------------|
| [vector-clock](./other-vector-clock.md) | Rust | Vector clocks |
| [vector-clock-rs](./other-vector-clock-rs.md) | Rust | Vector clocks (Rust) |
| [vector-navigator](./other-vector-navigator.md) | Rust | Vector navigator |
| [vector-novelty](./other-vector-novelty.md) | Rust | Novelty detection |
| [vector-search](./other-vector-search.md) | Rust | Vector search |
| [ab-testing-c](./other-ab-testing-c.md) | C | A/B testing in C |
| [ab-testing-rs](./other-ab-testing-rs.md) | Rust | A/B testing in Rust |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
