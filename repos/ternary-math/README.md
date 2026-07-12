# Ternary Math Ecosystem

**370+ repos** exploring balanced ternary computation — arithmetic, neural networks, GPU optimization, distributed systems, cryptography, physics, music, and more, all built on the algebra of {-1, 0, +1}.

---

## What Is Ternary Math Here?

The SuperInstance ternary ecosystem is a vast collection of Rust crates (with some Python, C, CUDA, and TypeScript) that takes **balanced ternary** — the base-3 number system using digits {-1, 0, +1} — and applies it to literally everything.

In classical computing, every value is a bit: 0 or 1. In the ternary world, every value is a **trit**: -1, 0, or +1. This maps naturally to:

- **Three-valued logic**: false / unknown / true (Kleene's K₃)
- **Z₃ algebra**: the cyclic group with three elements
- **Signal processing**: negative / silence / positive
- **Decisions**: reject / abstain / accept
- **Conservation**: deficit / balanced / surplus

The {-1, 0, +1} philosophy permeates every crate. Neural network weights become ternary (enabling BitNet-style 1.58-bit quantization). Sensor readings collapse to three states. Consensus votes are ternary. Even musical harmony and lattice gauge theory get the treatment.

### Key Facts

| Metric | Value |
|--------|-------|
| Total repos | 370 |
| Primary language | Rust (350+), with Python (7), C (5), CUDA (2), TypeScript (1) |
| Creation window | June 4–14, 2026 (~10 days) |
| Stars | 336 repos with 0★, 34 with 1★ |
| Median repo size | 16KB |
| Largest repo | ternary-science (4.1MB) |
| README quality | 362/370 have detailed READMEs (500+ words) |

---

## The {-1, 0, +1} Philosophy

Every value in this ecosystem is one of three things: **negative, neutral, or positive**. This isn't just a data type — it's a worldview:

- **Ternary logic (Kleene K₃)**: true / unknown / false — more expressive than Boolean logic
- **Balanced ternary arithmetic**: addition, multiplication, and division over ℤ with symmetric representation
- **Z₃ cyclic algebra**: {-1, 0, +1} forms a group under addition mod 3, enabling clean algebraic manipulation
- **Information density**: log₂(3) ≈ 1.585 bits per trit — the theoretical basis for BitNet's 1.58-bit weights
- **Natural decision theory**: every choice is accept (+1), reject (−1), or defer (0)

The `ternary-types` crate provides the foundational `Trit` enum used everywhere:

```rust
pub enum Trit {
    Negative = -1,
    Neutral  =  0,
    Positive = +1,
}
```

---

## Key Repositories

### Core Infrastructure

| Repo | Purpose |
|------|---------|
| [ternary-types](https://github.com/SuperInstance/ternary-types) | The `Trit` enum, conversion traits, optional serde support — the atom of the ecosystem |
| [ternary-core](https://github.com/SuperInstance/ternary-core) | Core traits and types shared across the ternary fleet |
| [ternary-arithmetic](https://github.com/SuperInstance/ternary-arithmetic) | Arithmetic coding for ternary data with frequency-adaptive compression |
| [ternary-logic](https://github.com/SuperInstance/ternary-logic) | Advanced ternary logic systems — Kleene K₃, Łukasiewicz Ł₃, Z₃ |
| [ternary-ring](https://github.com/SuperInstance/ternary-ring) | Ring and field structures for ternary values |

### Compiler & Tooling

| Repo | Purpose |
|------|---------|
| [ternary-compiler-v2](https://github.com/SuperInstance/ternary-compiler-v2) | Advanced compilation pipeline with three-address IR, ternary register allocation, and balanced-ternary code generation |
| [ternary-compiler](https://github.com/SuperInstance/ternary-compiler) | Parse, optimize, and evaluate ternary logic expressions |
| [ternary-interpreter](https://github.com/SuperInstance/ternary-interpreter) | Ternary bytecode interpreter for GPU control flow |
| [ternary-cli](https://github.com/SuperInstance/ternary-cli) | CLI tools for the ternary computing ecosystem |
| [ternary-auto-vectorizer](https://github.com/SuperInstance/ternary-auto-vectorizer) | Auto-vectorizes scalar Z₃ ternary ops to warp-level parallel versions |
| [ternary-wasm](https://github.com/SuperInstance/ternary-wasm) | WebAssembly bindings for ternary operations |

### Science & Evidence

| Repo | Purpose |
|------|---------|
| [ternary-science](https://github.com/SuperInstance/ternary-science) | Experimental evidence backing the Negative Space Intelligence theory — five proved conservation laws, universal strategy species from 2400-game GPU runs, RTX 4050 benchmarks, cross-language validation |
| [ternary-search](https://github.com/SuperInstance/ternary-search) | Search algorithms over ternary strategy spaces — binary threshold search, BFS/DFS, beam search, A* with fitness heuristics (7.7MB, one of the largest repos) |
| [ternary-search-rs](https://github.com/SuperInstance/ternary-search-rs) | High-performance ternary vector search server (axum + rayon + SIMD) |

### Neural Networks & ML

| Repo | Purpose |
|------|---------|
| [ternary-tnn](https://github.com/SuperInstance/ternary-tnn) | Ternary Neural Network layers — {-1,0,+1} weights with LUT matmul, straight-through estimation, BitNet-style 1.58-bit |
| [ternary-attention](https://github.com/SuperInstance/ternary-attention) | Scaled dot-product, multi-head, and cross-attention for ternary inputs |
| [ternary-activation](https://github.com/SuperInstance/ternary-activation) | ReLU, sigmoid, tanh, GELU, softmax — mapped to {-1, 0, +1} |
| [ternary-grad](https://github.com/SuperInstance/ternary-grad) | Ternary gradient descent — STE, ternary Adam/SGD, gradient clipping in trit space |
| [ternary-llm](https://github.com/SuperInstance/ternary-llm) | Ternary LLM building blocks — token embeddings, transformer blocks with ternary weights |
| [ternary-bayesian](https://github.com/SuperInstance/ternary-bayesian) | Bayesian inference — priors, posteriors, Bayesian networks, variational inference on ternary variables |
| [ternary-active-inference](https://github.com/SuperInstance/ternary-active-inference) | Active Inference with ternary actions — generative models, variational Bayes, expected free energy minimization |

### GPU & Kernel

| Repo | Purpose |
|------|---------|
| [ternary-cuda-kernels](https://github.com/SuperInstance/ternary-cuda-kernels) | PTX kernels for ternary matmul, jam sessions, and harmony reduction on GPU |
| [ternary-pack](https://github.com/SuperInstance/ternary-pack) | Bit-packing of ternary values for GPU memory efficiency |
| [ternary-dispatch](https://github.com/SuperInstance/ternary-dispatch) | Async dispatch of ternary-packed GPU kernels |
| [ternary-register-file](https://github.com/SuperInstance/ternary-register-file) | Register file allocation for ternary GPU kernels |

### Physics & Math

| Repo | Purpose |
|------|---------|
| [ternary-ising](https://github.com/SuperInstance/ternary-ising) | Ternary Ising model — three-state spin glasses |
| [ternary-hamiltonian](https://github.com/SuperInstance/ternary-hamiltonian) | Hamiltonian mechanics on ternary phase space — symplectic integration, energy conservation |
| [ternary-gauge-theory](https://github.com/SuperInstance/ternary-gauge-theory) | Z₃ lattice gauge theory on a 2D square lattice |
| [ternary-electromagnetism](https://github.com/SuperInstance/ternary-electromagnetism) | Maxwell's equations on ternary Yee lattices with {-1,0,+1} charge |
| [ternary-noether](https://github.com/SuperInstance/ternary-noether) | Noether's theorem for discrete ternary systems — symmetry → conservation law derivation |
| [ternary-quantum](https://github.com/SuperInstance/ternary-quantum) | Quantum-inspired computing with ternary states (qutrits) |

### Distributed Systems & Fleet

| Repo | Purpose |
|------|---------|
| [ternary-consensus](https://github.com/SuperInstance/ternary-consensus) | Consensus algorithms for distributed ternary agents |
| [ternary-paxos](https://github.com/SuperInstance/ternary-paxos) | Simplified Paxos for GPU cluster decisions with ternary votes |
| [ternary-antidote](https://github.com/SuperInstance/ternary-antidote) | CRDTs for GPU cluster state with ternary merge outcomes |
| [ternary-mirror](https://github.com/SuperInstance/ternary-mirror) | State mirroring for GPU cluster replication with ternary consistency |
| [ternary-beacon](https://github.com/SuperInstance/ternary-beacon) | Discovery and presence protocol for fleet agents |

### Crypto & Security

| Repo | Purpose |
|------|---------|
| [ternary-blockchain](https://github.com/SuperInstance/ternary-blockchain) | Trit-based sponge hash, proof-of-work mining, Merkle trees, {-1,0,+1} transactions |
| [ternary-cipher](https://github.com/SuperInstance/ternary-cipher) | One-time pads, Feistel ciphers, commitments, Shamir secret sharing over Z/3Z |
| [ternary-zkp](https://github.com/SuperInstance/ternary-zkp) | Zero-knowledge proofs over ternary fields GF(3ⁿ) |
| [ternary-watermark](https://github.com/SuperInstance/ternary-watermark) | Ternary watermarking for neural model provenance |

### Music & Audio

| Repo | Purpose |
|------|---------|
| [ternary-music](https://github.com/SuperInstance/ternary-music) | Musical theory with ternary harmony |
| [ternary-jam](https://github.com/SuperInstance/ternary-jam) | Musical jam session as multi-agent coordination |
| [ternary-harmonic](https://github.com/SuperInstance/ternary-harmonic) | Harmonic series and overtones for ternary signals |
| [ternary-rhythm](https://github.com/SuperInstance/ternary-rhythm) | Temporal pattern recognition using ternary time patterns |

---

## How They Interconnect

The ternary ecosystem follows a layered architecture:

```
                    ┌──────────────────────────────────────┐
                    │         Application Layer             │
                    │  (games, economics, music, biology)   │
                    └──────────────┬───────────────────────┘
                                   │
            ┌──────────────────────┼──────────────────────┐
            │                      │                      │
   ┌────────▼────────┐  ┌─────────▼─────────┐  ┌────────▼────────┐
   │   ML / NN       │  │  Distributed      │  │   Physics       │
   │   (tnn, attn,   │  │  (consensus,      │  │   (ising,       │
   │    grad, llm)   │  │   paxos, crdt)    │  │    gauge, ham)  │
   └────────┬────────┘  └─────────┬─────────┘  └────────┬────────┘
            │                      │                      │
            └──────────────────────┼──────────────────────┘
                                   │
                    ┌──────────────▼───────────────────────┐
                    │      Compiler & Tooling Layer         │
                    │  (compiler-v2, interpreter, cli,      │
                    │   auto-vectorizer, wasm)              │
                    └──────────────┬───────────────────────┘
                                   │
                    ┌──────────────▼───────────────────────┐
                    │        Core Types & Algebra           │
                    │  (ternary-types, ternary-core,        │
                    │   ternary-arithmetic, ternary-logic)  │
                    └──────────────┬───────────────────────┘
                                   │
                    ┌──────────────▼───────────────────────┐
                    │     GPU / Hardware Layer              │
                    │  (cuda-kernels, pack, dispatch,       │
                    │   register-file)                      │
                    └──────────────────────────────────────┘
```

All crates depend on `ternary-types` for the `Trit` enum. ML crates build on `ternary-tnn` and `ternary-attention`. The compiler toolchain (`ternary-compiler-v2`) generates code targeting GPU kernels (`ternary-cuda-kernels`). Distributed systems crates (`ternary-consensus`, `ternary-paxos`) use ternary voting for consensus. The science crate (`ternary-science`) validates the theory with experimental evidence.

---

## Thematic Clusters

| Cluster | ~Count | Example repos |
|---------|--------|---------------|
| Neural Networks / ML | ~40 | tnn, attention, activation, grad, distill, llm, checkpoint |
| GPU / Kernel | ~30 | cuda-kernels, pack, dispatch, register-file, warp-block |
| Distributed Systems | ~35 | consensus, paxos, lease, mirror, version, reassembly |
| Agent / Fleet | ~35 | agent, captain, navigator, helm, anchor, beacon |
| Math / Physics | ~30 | ising, quantum, hamiltonian, gauge-theory, electromagnetism |
| Music / Audio | ~20 | music, jam, harmonic, tempo, rhythm, timbre, wave |
| Data Structures | ~20 | btree, heap, bloom-filter, cache, database, archive |
| Crypto / Security | ~10 | cipher, blockchain, zkp, secret-share, watermark |
| Evolution / Genetics | ~10 | ga, genome, fitness, popgen, swarm |
| Game Theory / Economics | ~10 | games, auction, market, voting, pareto |
| Compiler / Tooling | ~10 | compiler, interpreter, cli, auto-vectorizer |

---

## Complete Repo Listing

| Repo | Description |
|------|-------------|
| ternary-accumulator | Ternary gradient accumulation for sign-based training |
| ternary-activation | Non-linearities born ternary — ReLU, sigmoid, tanh, GELU, softmax → {-1,0,+1} |
| ternary-active-inference | Active Inference with ternary actions — generative models, variational Bayes |
| ternary-adversarial | Adversarial testing for ternary agents |
| ternary-agent | Core agent types for the ternary ecosystem |
| ternary-anchor | Stability and persistence for rooms in dynamic fleet environments |
| ternary-antidote | CRDTs for GPU cluster state with ternary merge outcomes |
| ternary-archive | Persistent storage and retrieval of ternary knowledge |
| ternary-arena | Multi-agent competition arena for balanced ternary systems |
| ternary-arithmetic | Arithmetic coding for ternary data with adaptive compression |
| ternary-attention | Attention mechanisms for ternary inputs — scaled dot-product, multi-head |
| ternary-auction | Ternary auction mechanisms |
| ternary-auto-vectorizer | Auto-vectorizes scalar Z₃ ternary ops to warp-level parallel versions |
| ternary-automata | Cellular automata with ternary states — Wolfram numbering, pattern analysis |
| ternary-backpressure | Backpressure management for GPU pipelines with ternary pressure signals |
| ternary-baum-welch | Baum-Welch algorithm for ternary HMMs |
| ternary-bayesian | Bayesian inference — priors, posteriors, Bayesian networks, variational inference |
| ternary-beacon | Discovery and presence protocol for fleet agents |
| ternary-belief | Belief propagation on ternary factor graphs — sum-product, loopy BP |
| ternary-benchmark | Standardized benchmarks for ternary agent systems |
| ternary-bite | Bite for ternary systems |
| ternary-blockchain | Trit-based sponge hash, PoW mining, Merkle trees, {-1,0,+1} transactions |
| ternary-bloom-filter | Ternary Bloom filter for GPU membership testing |
| ternary-bridge | Bridge pattern for connecting heterogeneous ternary systems |
| ternary-btree | B-tree with ternary branching |
| ternary-budget | Resource allocation where items are {-1=over, 0=on-track, +1=under} budget |
| ternary-bus | Communication bus for inter-room messaging with ternary payloads |
| ternary-cache | Caching with entries in {-1=invalid, 0=stale, +1=fresh} states |
| ternary-cadence | Cadence detection for agent outputs |
| ternary-captain | Captain/leadership pattern for fleet coordination |
| ternary-cargo | Ternary Cargo |
| ternary-cartograph | Mapping and spatial representation for fleet topology |
| ternary-causality | Causal inference for ternary strategy systems |
| ternary-cell | Ternary cell |
| ternary-cell-python | Cell Python for the ternary ecosystem |
| ternary-channel | Communication channel abstractions for inter-room messaging |
| ternary-chaos | Chaos and nonlinear dynamics for ternary systems |
| ternary-checkpoint | Ternary model checkpointing with 16× compression |
| ternary-chemistry | Chemistry for ternary {-1, 0, +1} systems |
| ternary-chronicle | Historical record and narrative generation for ternary state systems |
| ternary-cipher | Ternary cryptography — OTPs, Feistel ciphers, commitments, Shamir over Z/3Z |
| ternary-circuit | Circuit and logic design with ternary values |
| ternary-classifier | Classifier for ternary {-1, 0, +1} |
| ternary-cli | CLI tools for the ternary computing ecosystem |
| ternary-clustering | Clustering algorithms for ternary data |
| ternary-codes | Error-correcting codes for ternary data |
| ternary-collatz | Collatz conjecture for ternary systems |
| ternary-color | Color theory and perception with ternary classification |
| ternary-command | Command parsing and dispatch with ternary outcomes |
| ternary-command-buffer | Command buffer for ternary GPU operations |
| ternary-compass | Orientation and direction in ternary state space |
| ternary-compiler | Ternary expression compiler — parse, optimize, evaluate |
| ternary-compiler-optimizer | Optimization passes for ternary bytecode |
| ternary-compiler-python | Ternary expression compiler in Python |
| ternary-compiler-v2 | Advanced ternary compilation pipeline with IR, register allocation, codegen |
| ternary-complexity | Kolmogorov complexity proxy via LZ77 for ternary genomes |
| ternary-compress | Ternary data compression for sparse GPU workloads |
| ternary-compression | Compress ternary sequences using various algorithms |
| ternary-compression-v2 | Advanced ternary compression for streams of {-1, 0, +1} |
| ternary-conduct | Orchestration and tempo control for coordinated fleet operations |
| ternary-consensus | Consensus algorithms for distributed ternary agents |
| ternary-conserve | Parametric conservation across resource domains |
| ternary-constant-cache | Constant cache simulation for ternary kernels |
| ternary-constellation | Constellation pattern for grouping related crates into deployable units |
| ternary-constraint | Constraint satisfaction and propagation for ternary variables |
| ternary-control | Control theory with ternary decisions |
| ternary-conv | Ternary convolution for {-1, 0, +1} signals and images |
| ternary-cookbook | Demos, tutorials, and developer guides for the ternary ecosystem |
| ternary-coordination | Balanced ternary coordination algebra — Z/3Z arithmetic, consensus proofs |
| ternary-core | Core traits and types shared across the ternary fleet |
| ternary-cortex | Hierarchical processing layers for ternary intelligence |
| ternary-counterpoint | Species counterpoint for ternary music |
| ternary-critical | Critical phenomena in ternary Ising models |
| ternary-criticality | Criticality for ternary systems |
| ternary-crossfader | Crossfader dynamics |
| ternary-crystal | Crystallography and lattice symmetry in ternary space |
| ternary-cuda-kernels | PTX kernels for ternary matmul, jam, harmony reduction on GPU |
| ternary-cuda-kernels-v2 | GPU-accelerated music cognition patterns |
| ternary-current | Information flow and momentum through fleet topologies |
| ternary-curriculum | Curriculum learning for ternary agents |
| ternary-database | Database operations for ternary data |
| ternary-depth | Depth measurement and pressure modeling for nested ternary systems |
| ternary-dice | Stochastic exploration with configurable randomness |
| ternary-diehard | Game of Life variants on ternary grids (Dead/Idle/Alive) |
| ternary-diff | Diff and patch for ternary strategies |
| ternary-dispatch | Async dispatch of ternary-packed GPU kernels |
| ternary-dissertation-c | C implementation of the dissertation engine |
| ternary-distill | Knowledge distillation for ternary networks |
| ternary-distributed | Distributed systems primitives for ternary protocols |
| ternary-dockyard | Maintenance and repair of ternary agents |
| ternary-drift | Drift for ternary systems |
| ternary-dropout | Dropout for ternary neural networks |
| ternary-dynamics | Temporal dynamics of ternary agent systems |
| ternary-dynamics-python | Ternary dynamical systems in Python |
| ternary-ear | Listening and pattern recognition across ternary fleet |
| ternary-ear-training | Ear training for ternary audio |
| ternary-echo | Echo for ternary systems |
| ternary-ecology | Ecological dynamics on ternary populations |
| ternary-econ | Economic models with ternary market signals |
| ternary-ecosystem | Full ecosystem simulation with multiple ternary species and food webs |
| ternary-electromagnetism | Maxwell's equations on ternary Yee lattices |
| ternary-em | Ternary expectation-maximization |
| ternary-energy | Energy and thermodynamic models for ternary systems |
| ternary-engine | Unified simulation engine for ternary agent systems |
| ternary-ensemble | Ensemble methods for ternary agents |
| ternary-ensign | Specialist agent pattern inspired by naval ensigns |
| ternary-entropy | Entropy analysis for ternary strategy distributions |
| ternary-envelope | Envelope/ADSR dynamics for ternary signals |
| ternary-epidemic | Epidemic and diffusion dynamics on ternary networks |
| ternary-epoch | Epoch for ternary systems |
| ternary-esp32-firmware | ESP32 firmware for ternary computing |
| ternary-event | Pub/sub event dispatch with ternary priorities |
| ternary-event-pool | Event pool for ternary systems |
| ternary-evolution-advanced | Differential evolution, CMA-ES-like adaptation for ternary |
| ternary-experiment | Experiment runner |
| ternary-experiment-workers | Experiment workers for ternary systems |
| ternary-explain | Explainability for ternary agent decisions |
| ternary-failure | Failure analysis with ternary classification |
| ternary-fault-tree | Fault tree analysis with ternary node states |
| ternary-federated | Federated learning for ternary agents |
| ternary-fence | Fence for ternary systems |
| ternary-fib | Fibonacci for ternary systems |
| ternary-field | Field for ternary systems |
| ternary-fire | Fire for ternary systems |
| ternary-fitness | Fitness landscape analysis for ternary agents |
| ternary-fitness-c | C implementation of ternary fitness landscapes |
| ternary-fitness-python | Python ternary fitness landscapes |
| ternary-fleet | Fleet ML workspace for ternary neural networks |
| ternary-fleet-integration | Bridge ternary math into Forgemaster fleet infrastructure |
| ternary-fleet-packing | Packing and encoding for ternary representations |
| ternary-flux | Flux/state-flow engine for tracking ternary value propagation |
| ternary-forgiveness | Forgiveness for ternary systems |
| ternary-form | Musical form analysis for multi-agent task decomposition |
| ternary-foundry | Casting and forging ternary strategies from raw materials |
| ternary-free-energy | Free Energy Principle — variational free energy, KL divergence on Z₃ |
| ternary-frontier | Exploration and discovery of unknown state space |
| ternary-fuse | Operator fusion for ternary networks |
| ternary-fuzzy | Fuzzy logic with ternary membership |
| ternary-ga | Genetic algorithm toolkit for ternary genomes |
| ternary-game-of-life | Game of Life on ternary grids |
| ternary-game-theory | Game theory — normal-form games, Nash equilibrium on ternary |
| ternary-games | Game theory for ternary agents |
| ternary-gate | Gate for ternary systems |
| ternary-gauge | Gauge for ternary systems |
| ternary-gauge-theory | Z₃ lattice gauge theory on a 2D square lattice |
| ternary-gc | Garbage collection for GPU memory with ternary marking |
| ternary-genetic | Genetic algorithms with ternary genomes — crossover, mutation |
| ternary-genome | Genetic encoding and expression for evolving ternary populations |
| ternary-geometry | Geometric algorithms for ternary spaces |
| ternary-grace | Grace vs Trust Rebuild |
| ternary-grad | Ternary gradient descent — STE, ternary Adam/SGD, gradient clipping |
| ternary-gradient | Gradient-free optimization for ternary landscapes |
| ternary-gradient-queue | Priority queue for ternary gradients |
| ternary-grain | Granular synthesis for ternary streams |
| ternary-grammar | Context-free grammar for ternary strategy expressions |
| ternary-graph | Graph algorithms on ternary-weighted edges |
| ternary-grid-launch | Grid launch for ternary GPU kernels |
| ternary-haar | Haar wavelet transform for ternary signals |
| ternary-hamiltonian | Hamiltonian mechanics on ternary phase space — symplectic integration |
| ternary-harbor | Harbor pattern for agent docking and resource management |
| ternary-hardware | Hardware abstraction for ternary operations |
| ternary-harmonic | Harmonic series and overtones for ternary signals |
| ternary-hash | Hashing and fingerprinting for ternary data |
| ternary-heap | Ternary min-heap — 3 children per node, O(log₃ n) push/pop |
| ternary-helm | Steering and control for fleet navigation |
| ternary-hmm | Hidden Markov Models with ternary states and emissions |
| ternary-homology | Simplicial homology over Z₃ |
| ternary-hotswap-inference | Adaptive ternary inference with atomic model hotswap |
| ternary-inference | Inference from ternary negative spaces |
| ternary-inference-c | Ternary neural network inference engine in C |
| ternary-inference-sim | Simulated ternary neural network inference |
| ternary-intent-cache | Cache for intent→bytecode compilations |
| ternary-interpreter | Ternary bytecode interpreter for GPU control flow |
| ternary-inventory | Items, inventory, equipment with ternary-valued properties |
| ternary-irradiate | Radiation damage, cascade simulation, annealing |
| ternary-ising | Ternary Ising model — three-state spin glasses |
| ternary-jam | Musical jam session as multi-agent coordination |
| ternary-kalman | Kalman filter for ternary state spaces |
| ternary-kernel-launch | Kernel launch for ternary GPU operations |
| ternary-knn | K-Nearest Neighbors for ternary vector spaces |
| ternary-knot | Knot theory and braid groups in ternary space |
| ternary-kuramoto | Discrete Kuramoto oscillator for ternary systems |
| ternary-language | Language and grammar processing with ternary sentiment |
| ternary-language-evolution | Communication protocol evolution in ternary systems |
| ternary-language-model | Language modeling with ternary token predictions |
| ternary-lattice | Lattice structures for ternary values |
| ternary-lattice-gc | Lattice-based GC for GPU object graphs with ternary liveness |
| ternary-lease | Distributed lease management for GPU resources |
| ternary-life | Life for ternary systems |
| ternary-lighthouse | Guidance and warning system for fleet navigation |
| ternary-llm | Ternary LLM building blocks — BitNet 1.58-bit style |
| ternary-locks | Lock algebra inspired by Oracle1's research |
| ternary-logic | Advanced ternary logic systems |
| ternary-logistic | Logistic regression for ternary data |
| ternary-loop | Loop for ternary systems |
| ternary-loss | Loss functions for ternary networks |
| ternary-manifesto | Manifesto for the ternary ecosystem |
| ternary-market | Economic exchange and resource allocation in ternary |
| ternary-markov | Markov chains on ternary state spaces |
| ternary-matmul | Ternary matrix multiplication for {-1, 0, +1} matrices |
| ternary-matrix | Matrix operations optimized for ternary values |
| ternary-membrane | Membrane transport dynamics with ternary concentrations |
| ternary-memory | Memory systems for ternary agents |
| ternary-memory-pool | Memory pool for ternary systems |
| ternary-mesh | Dynamic mesh networking between agents |
| ternary-metrics | Performance metrics for ternary systems |
| ternary-minority | Minority game on ternary systems |
| ternary-mirror | State mirroring for GPU cluster replication |
| ternary-mixer | Multi-channel ternary mixer |
| ternary-morph | Ternary morphological operations — erosion, dilation, skeletonization |
| ternary-morphogenesis | Turing morphogenesis — reaction-diffusion on ternary grids |
| ternary-motion | Ternary motion |
| ternary-mud | MUD room connections as balanced ternary algebra with Hodge decomposition |
| ternary-muse | Creative generation and artistic exploration with ternary |
| ternary-music | Musical theory with ternary harmony |
| ternary-mutual-info | Mutual information for ternary sequences |
| ternary-navigator | Navigation for ternary fleet |
| ternary-needledrop | Needle drop for ternary audio |
| ternary-negotiate | Agents negotiate using {-1=reject, 0=neutral, +1=accept} |
| ternary-network | Network science for ternary-weighted graphs |
| ternary-noether | Noether's theorem — symmetry → conservation law |
| ternary-noise | Effect of noise on ternary agent systems |
| ternary-norm | Norm functions for ternary data |
| ternary-observatory | Ternary observatory |
| ternary-optimizer | Optimizer for ternary systems |
| ternary-oracle | Prediction market for fleet intelligence with ternary confidence |
| ternary-pack | Bit-packing of ternary values for GPU memory efficiency |
| ternary-pagerank | PageRank and centrality on ternary-weighted graphs |
| ternary-pan | Pan for ternary systems |
| ternary-pareto | Pareto optimization for ternary agents |
| ternary-paxos | Simplified Paxos for GPU cluster decisions with ternary votes |
| ternary-pca | Principal component analysis for ternary data |
| ternary-percolate | Ternary percolation theory — clusters, thresholds, conductance |
| ternary-percolation | Percolation for ternary systems |
| ternary-permutation | Permutation groups acting on ternary vectors |
| ternary-petri | Petri nets for ternary systems |
| ternary-phase | Phase relationships between ternary oscillators |
| ternary-pheromone-market | Autonomous GPU load balancing via ternary pheromone markets |
| ternary-pid | Ternary PID controller — continuous PID with ternary output |
| ternary-pilgrim | Journey patterns and pilgrimage routes through fleet rooms |
| ternary-pipeline | Composable pipelines for ternary data processing |
| ternary-pipeline-parallel | Pipeline parallelism for ternary models |
| ternary-planning | Planning and scheduling with ternary priorities |
| ternary-platoon | Group formation and coordinated movement for ternary agents |
| ternary-polyrhythm | Multiple simultaneous rhythmic patterns with ternary support |
| ternary-pool | Ternary pooling operations for {-1, 0, +1} matrices |
| ternary-popgen | Population genetics for ternary agent systems |
| ternary-predict | Prediction-first perception |
| ternary-priority-queue | Priority queue for GPU kernel scheduling with ternary scoring |
| ternary-projection | Dimensionality reduction for ternary data |
| ternary-proof | Ternary proof system — {-1=invalid, 0=inconclusive, +1=valid} |
| ternary-prophet | Prediction and forecasting with uncertainty for ternary state |
| ternary-protocol | Wire protocol for communication between ternary agents |
| ternary-protocol-python | Python protocol for ternary agent communication |
| ternary-prune | Ternary network pruning |
| ternary-quantize | Ternary quantization |
| ternary-quantum | Quantum-inspired computing with ternary states (qutrits) |
| ternary-quorum | Distributed consensus using ternary voting with Byzantine tolerance |
| ternary-rack | Signal routing and patching between ternary rooms |
| ternary-rate-limiter | Rate limiter with ternary feedback |
| ternary-reassembly | Message reassembly with ternary fragment status |
| ternary-reef | Coral reef ecosystem pattern for collective intelligence |
| ternary-regex | Pattern matching on ternary sequences |
| ternary-register-file | Register file allocation for ternary GPU kernels |
| ternary-registry | Capability and skill registry for integration |
| ternary-registry-v2 | Enhanced skill registry with versioning and dependencies |
| ternary-regression | Regression for ternary data |
| ternary-renormalization | The renormalization group in ternary systems |
| ternary-renormalize | Renormalize for ternary systems |
| ternary-replay | Deterministic replay of agent experiments from seeds |
| ternary-reservoir | Reservoir computing with ternary nodes — echo state networks |
| ternary-resilience | Resilience for ternary systems |
| ternary-resonance | Resonance and sympathetic vibration between agents |
| ternary-retry | Retry policy with ternary outcome |
| ternary-rhythm | Temporal pattern recognition using ternary time patterns |
| ternary-rigging | Interactive value manipulation and ripple propagation |
| ternary-ring | Ring and field structures for ternary values |
| ternary-rl | Reinforcement learning with ternary actions |
| ternary-robotics | Robotics control with ternary decisions |
| ternary-room | Recursive room-tensor architecture |
| ternary-route | Route requests with {-1=reject, 0=queue, +1=accept} |
| ternary-routing | Self-optimizing request routing with ternary feedback |
| ternary-runlength | Run-length encoding for ternary data |
| ternary-sampler | Sampling strategies for ternary populations |
| ternary-sandbox | Safe sandbox for running ternary agent experiments |
| ternary-sandpile | Sandpile model on ternary systems |
| ternary-scheduler | Task scheduler with priority {-1=deferred, 0=normal, +1=urgent} |
| ternary-scheduling | Task scheduling using ternary decisions |
| ternary-scheduling-v2 | Advanced scheduling with ternary priorities |
| ternary-science | Experimental evidence — conservation laws, strategy species, benchmarks |
| ternary-scoring | Multi-criteria scoring for ternary strategies |
| ternary-search | Search algorithms over ternary strategy spaces — BFS/DFS, beam, A* |
| ternary-search-index | Ternary-weighted search index for GPU-accelerable retrieval |
| ternary-search-rs | High-performance ternary vector search server (axum + rayon + SIMD) |
| ternary-secret-share | Secret sharing schemes over Z/3Z |
| ternary-seed | Seeded-Model-Programming (SMP) foundation |
| ternary-semaphore | Ternary semaphore for GPU resource control |
| ternary-sensor | Sensor data processing with ternary classification |
| ternary-shard | Sharded ternary data for multi-GPU inference |
| ternary-shard-merge | Merge distributed ternary weight shards |
| ternary-shard-split | Shard ternary model weights across devices |
| ternary-shared-memory | Shared memory for ternary systems |
| ternary-sheaf | Sheaf for ternary systems |
| ternary-shield | Shield for ternary systems |
| ternary-shipyard | Ternary shipyard |
| ternary-signal-flow | Ternary signal flow through GPU processing pipeline |
| ternary-signaling | Ternary signaling games |
| ternary-signals | Ternary signal processing — convolution, filtering, spectral analysis |
| ternary-sketch | Ternary sketch for approximate GPU workload analysis |
| ternary-som | Self-organizing maps for ternary data |
| ternary-sort | Sorting algorithms for ternary data |
| ternary-spatial | Ternary spatial math — P48 + Eisenstein |
| ternary-speculate | Speculative sync |
| ternary-spiral | Spiral wave dynamics from Rock-Paper-Scissors cyclic dominance |
| ternary-spreadsheet | Ternary spreadsheet core logic |
| ternary-spreadsheet-c | Ternary spreadsheet engine in C |
| ternary-spreadsheet-python | Ternary spreadsheet engine in Python |
| ternary-steganography | Hide information in ternary strategy noise |
| ternary-steward | Resource stewardship for ternary systems |
| ternary-story | Ternary narrative engine |
| ternary-stream-queue | Stream queue for ternary systems |
| ternary-streaming | Streaming processing of ternary signals |
| ternary-surface-memory | Surface memory for ternary texture-like access |
| ternary-svm | Support Vector Machines for ternary feature spaces |
| ternary-swarm | Swarm intelligence with ternary movement |
| ternary-symbiont | Symbiotic relationships between ternary agents |
| ternary-symmetry | Group theory and symmetry operations in ternary space |
| ternary-sync | Sync for ternary systems |
| ternary-temperament | Temperament for ternary systems |
| ternary-tempo | Tempo and rhythm detection for ternary sequences |
| ternary-tenforward | Ten-Forward lounge for ternary agents |
| ternary-tensor | Tensor operations for ternary multi-dimensional arrays |
| ternary-tensor-parallel | Tensor parallelism for ternary models |
| ternary-texture-memory | Texture memory for ternary GPU access |
| ternary-thermodynamics | Statistical mechanics analogs for ternary agent systems |
| ternary-thermostat | Climate control with PID, multi-zone, scheduling |
| ternary-thread-block | Thread block for ternary GPU kernels |
| ternary-tidelight | Temporal rhythm and timing coordination across the fleet |
| ternary-tidepool | Small protected environments for agent experimentation |
| ternary-timbre | Timbre analysis for agent output characterization |
| ternary-tnn | Ternary Neural Network layers — LUT matmul, STE, BitNet 1.58-bit |
| ternary-topology | Persistent homology for ternary networks |
| ternary-transfer | Transfer learning for ternary agents |
| ternary-transform | Transform theory for ternary data |
| ternary-transformer | Transformer for ternary data |
| ternary-trees | Decision trees and forests for ternary classification |
| ternary-trust | Trust and relationship dynamics between agents |
| ternary-tuple | Tuple for ternary systems |
| ternary-turing | Turing machines over ternary alphabet {-1, 0, +1} |
| ternary-types | The `Trit` enum — foundational type for the ecosystem |
| ternary-validation | Validate ternary strategies against constraints |
| ternary-version | Version vectors with ternary comparison for distributed state |
| ternary-visualization | Visualization data generation for ternary systems |
| ternary-visualizer | Ternary agent dynamics visualizer |
| ternary-viterbi | Viterbi decoder for ternary state sequences |
| ternary-vortex | Vortex dynamics and fluid-like flow on ternary grids |
| ternary-voting | Voting and consensus mechanisms with ternary values |
| ternary-voyage | Long-duration mission planning with ternary progress tracking |
| ternary-vu | Vu for ternary systems |
| ternary-walk | Ternary random walks — simple, biased, correlated, Lévy flights |
| ternary-walsh | Walsh functions and transforms for ternary signal analysis |
| ternary-warp | Warp for ternary systems |
| ternary-warp-block | Warp block for ternary GPU kernels |
| ternary-wasm | WebAssembly for ternary operations |
| ternary-watermark | Ternary watermarking for neural model provenance |
| ternary-wave | Wave for ternary systems |
| ternary-weather | Environmental conditions and their effects on operations |
| ternary-world | World model for ternary simulations |
| ternary-zigzag | Zigzag scanning for ternary matrix compression |
| ternary-zkp | Zero-knowledge proofs over ternary fields GF(3ⁿ) |

---

## Assessment

All 370 repos were created within ~10 days (June 4–14, 2026). This burst pattern suggests heavy AI-assisted generation. However, individual crates contain domain-specific implementations with real mathematical content — Kleene logic, Z₃ algebra, Shannon entropy, variational inference, lattice gauge theory — that go beyond boilerplate. Each crate appears to be a genuine, if small, Rust implementation.

The ecosystem is more impressive in breadth than depth, but the depth where it exists (`ternary-science`, `ternary-search`, `ternary-compiler-v2`, `ternary-automata`, `ternary-types`) is legitimate.

---

*Individual repo summaries are in `ternary-{repo-name}.md` files in this directory.*
