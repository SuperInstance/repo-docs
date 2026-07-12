# Ternary Repos Index

**370 repos** in the SuperInstance ternary ecosystem.

## Ecosystem Overview

The SuperInstance ternary ecosystem is a collection of 370+ Rust crates (with some Python, C, CUDA, and TypeScript) exploring **balanced ternary computation** — arithmetic over {-1, 0, +1} instead of {0, 1}. The ecosystem covers an extraordinarily wide range: neural networks, GPU optimization, distributed systems, cryptography, game theory, cellular automata, physics simulations, music theory, economics, biology, and more.

### Key Facts

| Metric | Value |
|--------|-------|
| Total repos | 370 |
| Primary language | Rust (350+), with Python (7), C (5), CUDA (2), TypeScript (1) |
| Creation window | June 4-14, 2026 (~10 days) |
| Stars | 336 repos with 0★, 34 with 1★ |
| Median repo size | 16KB |
| Largest repo | ternary-science (4.1MB) |
| README quality | 362/370 have detailed READMEs (500+ words) |

### Thematic Clusters

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

### Creation Pattern

All 370 repos were created within ~10 days (June 4-14, 2026), with pushes continuing through June 16. This burst pattern, combined with the sheer volume and consistent documentation style, strongly suggests **heavy AI-assisted generation**. However, the individual crates contain domain-specific implementations with real mathematical content (Kleene logic, Z₃ algebra, Shannon entropy, variational inference, lattice gauge theory, etc.) that go beyond boilerplate. Each crate appears to be a genuine, if small, Rust implementation.

## All Repos

| Repo | Description |
|------|-------------|
| [ternary-accumulator](https://github.com/SuperInstance/ternary-accumulator) | Ternary gradient accumulation for sign-based training |
| [ternary-activation](https://github.com/SuperInstance/ternary-activation) | ternary-activation - SuperInstance ecosystem crate |
| [ternary-active-inference](https://github.com/SuperInstance/ternary-active-inference) | Active Inference with ternary {-1,0,+1} actions: generative models, variational Bayes, expected free energy minimization |
| [ternary-adversarial](https://github.com/SuperInstance/ternary-adversarial) | Ternary Adversarial  Adversarial testing for ternary agents |
| [ternary-agent](https://github.com/SuperInstance/ternary-agent) | Core agent types for the ternary ecosystem |
| [ternary-anchor](https://github.com/SuperInstance/ternary-anchor) | ternary-anchor: Stability and persistence for rooms in dynamic fleet environments |
| [ternary-antidote](https://github.com/SuperInstance/ternary-antidote) | CRDTs for GPU cluster state with ternary merge outcomes |
| [ternary-archive](https://github.com/SuperInstance/ternary-archive) | Persistent storage and retrieval of ternary knowledge in balanced ternary {-1, 0, +1} systems |
| [ternary-arena](https://github.com/SuperInstance/ternary-arena) | Multi-agent competition arena for balanced ternary systems |
| [ternary-arithmetic](https://github.com/SuperInstance/ternary-arithmetic) | ternary-arithmetic - SuperInstance ecosystem crate |
| [ternary-attention](https://github.com/SuperInstance/ternary-attention) | Attention mechanisms adapted for ternary inputs on {-1, 0, +1} |
| [ternary-auction](https://github.com/SuperInstance/ternary-auction) | Ternary auction mechanisms |
| [ternary-auto-vectorizer](https://github.com/SuperInstance/ternary-auto-vectorizer) | Auto-vectorizes scalar Z₃ ternary ops to warp-level parallel versions |
| [ternary-automata](https://github.com/SuperInstance/ternary-automata) | Cellular automata with ternary states |
| [ternary-backpressure](https://github.com/SuperInstance/ternary-backpressure) | Backpressure management for GPU pipelines with ternary pressure signals |
| [ternary-baum-welch](https://github.com/SuperInstance/ternary-baum-welch) | ternary-baum-welch - SuperInstance ecosystem crate |
| [ternary-bayesian](https://github.com/SuperInstance/ternary-bayesian) | Bayesian inference for ternary variables on {-1, 0, +1} |
| [ternary-beacon](https://github.com/SuperInstance/ternary-beacon) | Discovery and presence protocol for fleet agents |
| [ternary-belief](https://github.com/SuperInstance/ternary-belief) | Belief propagation on ternary factor graphs: sum-product message passing, loopy BP, evidence clamping, marginal infer... |
| [ternary-benchmark](https://github.com/SuperInstance/ternary-benchmark) | ternary-benchmark  Standardized benchmarks for ternary agent systems |
| [ternary-bite](https://github.com/SuperInstance/ternary-bite) | Bite for ternary systems |
| [ternary-blockchain](https://github.com/SuperInstance/ternary-blockchain) | Blockchain primitives using balanced ternary: trit-based sponge hash, proof-of-work mining, Merkle trees, {-1,0,+1} t... |
| [ternary-bloom-filter](https://github.com/SuperInstance/ternary-bloom-filter) | Ternary Bloom filter for GPU membership testing |
| [ternary-bridge](https://github.com/SuperInstance/ternary-bridge) | Bridge pattern for connecting heterogeneous ternary systems |
| [ternary-btree](https://github.com/SuperInstance/ternary-btree) | B-tree with ternary branching |
| [ternary-budget](https://github.com/SuperInstance/ternary-budget) | Ternary budget: resource allocation where items are {-1=over, 0=on-track, +1=under} budget |
| [ternary-bus](https://github.com/SuperInstance/ternary-bus) | ternary-bus Communication bus for inter-room messaging with ternary payloads |
| [ternary-cache](https://github.com/SuperInstance/ternary-cache) | Ternary cache: caching with entries in {-1=invalid, 0=stale, +1=fresh} states |
| [ternary-cadence](https://github.com/SuperInstance/ternary-cadence) | Cadence detection for agent outputs |
| [ternary-captain](https://github.com/SuperInstance/ternary-captain) | Captain/leadership pattern for fleet coordination |
| [ternary-cargo](https://github.com/SuperInstance/ternary-cargo) | Ternary Cargo |
| [ternary-cartograph](https://github.com/SuperInstance/ternary-cartograph) | Mapping and spatial representation for fleet topology visualization |
| [ternary-causality](https://github.com/SuperInstance/ternary-causality) | ternary-causality  Causal inference for ternary strategy systems |
| [ternary-cell](https://github.com/SuperInstance/ternary-cell) | Ternary cell |
| [ternary-cell-python](https://github.com/SuperInstance/ternary-cell-python) | Cell Python for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-channel](https://github.com/SuperInstance/ternary-channel) | Communication channel abstractions for inter-room messaging |
| [ternary-chaos](https://github.com/SuperInstance/ternary-chaos) | Chaos and nonlinear dynamics for ternary systems |
| [ternary-checkpoint](https://github.com/SuperInstance/ternary-checkpoint) | Ternary model checkpointing with 16× compression |
| [ternary-chemistry](https://github.com/SuperInstance/ternary-chemistry) | Chemistry for ternary {-1, 0, +1} systems |
| [ternary-chronicle](https://github.com/SuperInstance/ternary-chronicle) | Historical record and narrative generation for ternary state systems |
| [ternary-cipher](https://github.com/SuperInstance/ternary-cipher) | ternary-cipher  Ternary cryptography: one-time pads, Feistel ciphers, commitments, Shamir secre |
| [ternary-circuit](https://github.com/SuperInstance/ternary-circuit) | Circuit and logic design with ternary values |
| [ternary-classifier](https://github.com/SuperInstance/ternary-classifier) | Classifier for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-cli](https://github.com/SuperInstance/ternary-cli) | CLI tools for the ternary computing ecosystem |
| [ternary-clustering](https://github.com/SuperInstance/ternary-clustering) | ternary-clustering  Clustering algorithms for ternary data represented as vectors of `Ternary` |
| [ternary-codes](https://github.com/SuperInstance/ternary-codes) | Error-correcting codes for ternary data |
| [ternary-collatz](https://github.com/SuperInstance/ternary-collatz) | Collatz for ternary systems |
| [ternary-color](https://github.com/SuperInstance/ternary-color) | ternary-color  Color theory and perception with ternary classification |
| [ternary-command](https://github.com/SuperInstance/ternary-command) | ternary-command: Command parsing and dispatch with ternary outcomes |
| [ternary-command-buffer](https://github.com/SuperInstance/ternary-command-buffer) | ternary-command-buffer - SuperInstance ecosystem crate |
| [ternary-compass](https://github.com/SuperInstance/ternary-compass) | Orientation and direction in ternary state space |
| [ternary-compiler](https://github.com/SuperInstance/ternary-compiler) | Ternary expression compiler: parse, optimize, and evaluate ternary logic expressions |
| [ternary-compiler-optimizer](https://github.com/SuperInstance/ternary-compiler-optimizer) | Optimization passes for ternary bytecode |
| [ternary-compiler-python](https://github.com/SuperInstance/ternary-compiler-python) | Ternary expression compiler in Python |
| [ternary-compiler-v2](https://github.com/SuperInstance/ternary-compiler-v2) | Advanced ternary compilation pipeline with IR, register allocation, and code generation |
| [ternary-complexity](https://github.com/SuperInstance/ternary-complexity) | Kolmogorov complexity proxy via LZ77 compression for ternary genomes |
| [ternary-compress](https://github.com/SuperInstance/ternary-compress) | Experiment: ternary data compression for sparse GPU workloads |
| [ternary-compression](https://github.com/SuperInstance/ternary-compression) | ternary-compression  Compress ternary sequences using various algorithms |
| [ternary-compression-v2](https://github.com/SuperInstance/ternary-compression-v2) | Advanced ternary compression for streams of {-1, 0, +1} values |
| [ternary-conduct](https://github.com/SuperInstance/ternary-conduct) | ternary-conduct  Orchestration and tempo control for coordinated ternary fleet operations |
| [ternary-consensus](https://github.com/SuperInstance/ternary-consensus) | ternary-consensus  Consensus algorithms for distributed ternary agents |
| [ternary-conserve](https://github.com/SuperInstance/ternary-conserve) | Parametric conservation across resource domains |
| [ternary-constant-cache](https://github.com/SuperInstance/ternary-constant-cache) | Constant cache simulation for ternary kernels |
| [ternary-constellation](https://github.com/SuperInstance/ternary-constellation) | Constellation pattern for grouping related ternary crates into deployable units |
| [ternary-constraint](https://github.com/SuperInstance/ternary-constraint) | Constraint satisfaction and propagation for ternary variables |
| [ternary-control](https://github.com/SuperInstance/ternary-control) | Control theory with ternary decisions |
| [ternary-conv](https://github.com/SuperInstance/ternary-conv) | Ternary convolution operations for {-1, 0, +1} signals and images |
| [ternary-cookbook](https://github.com/SuperInstance/ternary-cookbook) | Working demos, tutorials, and developer guides for the ternary {-1, 0, +1} ecosystem |
| [ternary-coordination](https://github.com/SuperInstance/ternary-coordination) | Balanced ternary {-1,0,+1} coordination algebra: Z/3Z arithmetic, ternary matrices, consensus convergence proofs, spe... |
| [ternary-core](https://github.com/SuperInstance/ternary-core) | ternary-core  Core traits and types shared across the ternary fleet |
| [ternary-cortex](https://github.com/SuperInstance/ternary-cortex) | Hierarchical processing layers for ternary intelligence |
| [ternary-counterpoint](https://github.com/SuperInstance/ternary-counterpoint) | ternary-counterpoint  Species counterpoint for ternary music |
| [ternary-critical](https://github.com/SuperInstance/ternary-critical) | ternary-critical  Critical phenomena in ternary Ising models |
| [ternary-criticality](https://github.com/SuperInstance/ternary-criticality) | Criticality for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-crossfader](https://github.com/SuperInstance/ternary-crossfader) | Crossfader dynamics |
| [ternary-crystal](https://github.com/SuperInstance/ternary-crystal) | ternary-crystal  Crystallography and lattice symmetry in ternary space |
| [ternary-cuda-kernels](https://github.com/SuperInstance/ternary-cuda-kernels) | PTX kernels for ternary jam sessions, matmul, and harmony reduction on GPU |
| [ternary-cuda-kernels-v2](https://github.com/SuperInstance/ternary-cuda-kernels-v2) | GPU-accelerated music cognition patterns |
| [ternary-current](https://github.com/SuperInstance/ternary-current) | ternary-current: Information flow and momentum through fleet topologies |
| [ternary-curriculum](https://github.com/SuperInstance/ternary-curriculum) | Curriculum learning for ternary agents |
| [ternary-database](https://github.com/SuperInstance/ternary-database) | Database operations for ternary data |
| [ternary-depth](https://github.com/SuperInstance/ternary-depth) | Depth measurement and pressure modeling for nested ternary systems |
| [ternary-dice](https://github.com/SuperInstance/ternary-dice) | Stochastic exploration with configurable randomness for balanced ternary systems |
| [ternary-diehard](https://github.com/SuperInstance/ternary-diehard) | Game of Life variants on ternary grids (Dead/Idle/Alive) |
| [ternary-diff](https://github.com/SuperInstance/ternary-diff) | ternary-diff  Diff and patch for ternary strategies: compare, merge, and resolve conflicts |
| [ternary-dispatch](https://github.com/SuperInstance/ternary-dispatch) | Async dispatch of ternary-packed GPU kernels |
| [ternary-dissertation-c](https://github.com/SuperInstance/ternary-dissertation-c) | C implementation of the dissertation engine |
| [ternary-distill](https://github.com/SuperInstance/ternary-distill) | Knowledge distillation for ternary networks |
| [ternary-distributed](https://github.com/SuperInstance/ternary-distributed) | Distributed systems primitives for ternary protocols |
| [ternary-dockyard](https://github.com/SuperInstance/ternary-dockyard) | Maintenance and repair of ternary agents |
| [ternary-drift](https://github.com/SuperInstance/ternary-drift) | Drift for ternary {-1, 0, +1} systems |
| [ternary-dropout](https://github.com/SuperInstance/ternary-dropout) | ternary-dropout - SuperInstance ecosystem crate |
| [ternary-dynamics](https://github.com/SuperInstance/ternary-dynamics) | Ternary Dynamics  Temporal dynamics of ternary agent systems |
| [ternary-dynamics-python](https://github.com/SuperInstance/ternary-dynamics-python) | Ternary dynamical systems in Python |
| [ternary-ear](https://github.com/SuperInstance/ternary-ear) | ternary-ear  Listening and pattern recognition across a ternary agent fleet |
| [ternary-ear-training](https://github.com/SuperInstance/ternary-ear-training) | ternary-ear-training - SuperInstance ecosystem crate |
| [ternary-echo](https://github.com/SuperInstance/ternary-echo) | Echo for ternary {-1, 0, +1} systems |
| [ternary-ecology](https://github.com/SuperInstance/ternary-ecology) | ternary-ecology  Ecological dynamics on ternary populations |
| [ternary-econ](https://github.com/SuperInstance/ternary-econ) | Economic models with ternary market signals |
| [ternary-ecosystem](https://github.com/SuperInstance/ternary-ecosystem) | Full ecosystem simulation with multiple ternary species and food webs |
| [ternary-electromagnetism](https://github.com/SuperInstance/ternary-electromagnetism) | Electromagnetic field simulation on ternary Yee lattices: Maxwell's equations with {-1,0,+1} charge, wave propagation... |
| [ternary-em](https://github.com/SuperInstance/ternary-em) | ternary-em - SuperInstance ecosystem crate |
| [ternary-energy](https://github.com/SuperInstance/ternary-energy) | Energy and thermodynamic models for ternary systems |
| [ternary-engine](https://github.com/SuperInstance/ternary-engine) | Ternary Engine  Unified simulation engine for ternary {-1,0,+1} agent systems |
| [ternary-ensemble](https://github.com/SuperInstance/ternary-ensemble) | ternary-ensemble  Ensemble methods for ternary agents |
| [ternary-ensign](https://github.com/SuperInstance/ternary-ensign) | Specialist agent pattern inspired by naval ensigns |
| [ternary-entropy](https://github.com/SuperInstance/ternary-entropy) | Entropy analysis for ternary strategy distributions |
| [ternary-envelope](https://github.com/SuperInstance/ternary-envelope) | Envelope/ADSR dynamics for ternary (-1, 0, +1) signals |
| [ternary-epidemic](https://github.com/SuperInstance/ternary-epidemic) | ternary-epidemic  Epidemic and diffusion dynamics on ternary networks |
| [ternary-epoch](https://github.com/SuperInstance/ternary-epoch) | Epoch for ternary {-1, 0, +1} systems |
| [ternary-esp32-firmware](https://github.com/SuperInstance/ternary-esp32-firmware) | Esp32 Firmware for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-event](https://github.com/SuperInstance/ternary-event) | ternary-event: Pub/sub event dispatch with ternary priorities |
| [ternary-event-pool](https://github.com/SuperInstance/ternary-event-pool) | ternary-event-pool - SuperInstance ecosystem crate |
| [ternary-evolution-advanced](https://github.com/SuperInstance/ternary-evolution-advanced) | Advanced evolutionary algorithms for ternary optimization: differential evolution, CMA-ES-like ad |
| [ternary-experiment](https://github.com/SuperInstance/ternary-experiment) | Experiment runner |
| [ternary-experiment-workers](https://github.com/SuperInstance/ternary-experiment-workers) | Experiment Workers for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-explain](https://github.com/SuperInstance/ternary-explain) | ternary-explain  Explainability for ternary agent decisions |
| [ternary-failure](https://github.com/SuperInstance/ternary-failure) | Failure analysis with ternary classification |
| [ternary-fault-tree](https://github.com/SuperInstance/ternary-fault-tree) | Fault tree analysis for GPU systems with ternary node states {+1=healthy, 0=degraded, -1=failed} |
| [ternary-federated](https://github.com/SuperInstance/ternary-federated) | Federated learning for ternary agents |
| [ternary-fence](https://github.com/SuperInstance/ternary-fence) | ternary-fence - SuperInstance ecosystem crate |
| [ternary-fib](https://github.com/SuperInstance/ternary-fib) | Fib for ternary systems |
| [ternary-field](https://github.com/SuperInstance/ternary-field) | Field for ternary systems |
| [ternary-fire](https://github.com/SuperInstance/ternary-fire) | Fire for ternary systems |
| [ternary-fitness](https://github.com/SuperInstance/ternary-fitness) | Fitness landscape analysis for ternary agent systems {-1, 0, +1} |
| [ternary-fitness-c](https://github.com/SuperInstance/ternary-fitness-c) | C implementation of ternary fitness landscapes |
| [ternary-fitness-python](https://github.com/SuperInstance/ternary-fitness-python) | Fitness Python for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-fleet](https://github.com/SuperInstance/ternary-fleet) | Fleet ML workspace for ternary neural networks |
| [ternary-fleet-integration](https://github.com/SuperInstance/ternary-fleet-integration) | Bridge ternary math into Forgemaster fleet infrastructure |
| [ternary-fleet-packing](https://github.com/SuperInstance/ternary-fleet-packing) | Packing and encoding algorithms for ternary representations |
| [ternary-flux](https://github.com/SuperInstance/ternary-flux) | Flux/state-flow engine for tracking ternary value propagation |
| [ternary-forgiveness](https://github.com/SuperInstance/ternary-forgiveness) | Forgiveness for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-form](https://github.com/SuperInstance/ternary-form) | **Musical form analysis for multi-agent task decomposition |
| [ternary-foundry](https://github.com/SuperInstance/ternary-foundry) | Casting and forging ternary strategies from raw materials |
| [ternary-free-energy](https://github.com/SuperInstance/ternary-free-energy) | Free Energy Principle for ternary systems: variational free energy, KL divergence on Z₃, surprise minimization, Marko... |
| [ternary-frontier](https://github.com/SuperInstance/ternary-frontier) | Exploration and discovery of unknown state space in balanced ternary {-1, 0, +1} systems |
| [ternary-fuse](https://github.com/SuperInstance/ternary-fuse) | Operator fusion for ternary networks |
| [ternary-fuzzy](https://github.com/SuperInstance/ternary-fuzzy) | Fuzzy logic with ternary membership |
| [ternary-ga](https://github.com/SuperInstance/ternary-ga) | Genetic algorithm toolkit for ternary genomes ({-1, 0, +1}) |
| [ternary-game-of-life](https://github.com/SuperInstance/ternary-game-of-life) | ternary-game-of-life - SuperInstance ecosystem crate |
| [ternary-game-theory](https://github.com/SuperInstance/ternary-game-theory) | Game theory with ternary strategies: normal-form games, Nash equilibrium, prisoners dilemma varia |
| [ternary-games](https://github.com/SuperInstance/ternary-games) | Ternary Games  Game theory for ternary agents |
| [ternary-gate](https://github.com/SuperInstance/ternary-gate) | Gate for ternary systems |
| [ternary-gauge](https://github.com/SuperInstance/ternary-gauge) | Gauge for ternary {-1, 0, +1} systems |
| [ternary-gauge-theory](https://github.com/SuperInstance/ternary-gauge-theory) | Z₃ lattice gauge theory on a 2D square lattice |
| [ternary-gc](https://github.com/SuperInstance/ternary-gc) | Garbage collection for GPU memory with ternary marking |
| [ternary-genetic](https://github.com/SuperInstance/ternary-genetic) | Genetic algorithms with ternary genomes: crossover in trit space, trit-flip mutation, tournament selection on {-1,0,+... |
| [ternary-genome](https://github.com/SuperInstance/ternary-genome) | Genetic encoding and expression for evolving ternary agent populations |
| [ternary-geometry](https://github.com/SuperInstance/ternary-geometry) | Geometric algorithms for ternary spaces |
| [ternary-grace](https://github.com/SuperInstance/ternary-grace) | Grace vs Trust Rebuild |
| [ternary-grad](https://github.com/SuperInstance/ternary-grad) | Ternary gradient descent: straight-through estimator, ternary Adam/SGD optimizers, gradient clipping in trit space, c... |
| [ternary-gradient](https://github.com/SuperInstance/ternary-gradient) | Gradient-free and gradient-like optimization for ternary landscapes |
| [ternary-gradient-queue](https://github.com/SuperInstance/ternary-gradient-queue) | Priority queue for ternary gradients |
| [ternary-grain](https://github.com/SuperInstance/ternary-grain) | Granular synthesis for ternary (-1, 0, +1) streams |
| [ternary-grammar](https://github.com/SuperInstance/ternary-grammar) | ternary-grammar  Context-free grammar for generating and parsing valid ternary strategy express |
| [ternary-graph](https://github.com/SuperInstance/ternary-graph) | ternary-graph  Graph algorithms operating on ternary-weighted edges (`-1`, `0`, `+1`) |
| [ternary-grid-launch](https://github.com/SuperInstance/ternary-grid-launch) | ternary-grid-launch - SuperInstance ecosystem crate |
| [ternary-haar](https://github.com/SuperInstance/ternary-haar) | Haar wavelet transform for ternary-valued signals |
| [ternary-hamiltonian](https://github.com/SuperInstance/ternary-hamiltonian) | Hamiltonian mechanics on ternary phase space: symplectic integration, energy conservation, Poisson brackets in {-1,0,+1} |
| [ternary-harbor](https://github.com/SuperInstance/ternary-harbor) | Harbor pattern for agent docking and resource management |
| [ternary-hardware](https://github.com/SuperInstance/ternary-hardware) | Hardware abstraction for ternary operations |
| [ternary-harmonic](https://github.com/SuperInstance/ternary-harmonic) | ternary-harmonic Harmonic series and overtones for ternary signals |
| [ternary-hash](https://github.com/SuperInstance/ternary-hash) | Hashing and fingerprinting for ternary data ({-1, 0, +1}) |
| [ternary-heap](https://github.com/SuperInstance/ternary-heap) | Ternary min-heap priority queue: 3 children per node, O(log₃ n) push/pop, merge, decrease-key |
| [ternary-helm](https://github.com/SuperInstance/ternary-helm) | ternary-helm: Steering and control for fleet navigation |
| [ternary-hmm](https://github.com/SuperInstance/ternary-hmm) | Hidden Markov Models with Ternary States and Emissions |
| [ternary-homology](https://github.com/SuperInstance/ternary-homology) | ternary-homology  Simplicial homology over Z₃ |
| [ternary-hotswap-inference](https://github.com/SuperInstance/ternary-hotswap-inference) | Adaptive ternary inference with atomic model hotswap and CRDT audit trail |
| [ternary-inference](https://github.com/SuperInstance/ternary-inference) | ternary-inference  Inference from ternary negative spaces |
| [ternary-inference-c](https://github.com/SuperInstance/ternary-inference-c) | Ternary neural network inference engine in C |
| [ternary-inference-sim](https://github.com/SuperInstance/ternary-inference-sim) | Simulated ternary neural network inference |
| [ternary-intent-cache](https://github.com/SuperInstance/ternary-intent-cache) | Cache for intent→bytecode compilations |
| [ternary-interpreter](https://github.com/SuperInstance/ternary-interpreter) | Ternary bytecode interpreter for GPU control flow |
| [ternary-inventory](https://github.com/SuperInstance/ternary-inventory) | Items, inventory, equipment, and loot tables with ternary-valued properties |
| [ternary-irradiate](https://github.com/SuperInstance/ternary-irradiate) | Ternary irradiation: radiation damage, cascade simulation, annealing, defect tracking |
| [ternary-ising](https://github.com/SuperInstance/ternary-ising) | Ternary Ising model |
| [ternary-jam](https://github.com/SuperInstance/ternary-jam) | ternary-jam  Musical jam session as multi-agent coordination |
| [ternary-kalman](https://github.com/SuperInstance/ternary-kalman) | Kalman filter adapted for ternary state spaces with fixed-point arithmetic |
| [ternary-kernel-launch](https://github.com/SuperInstance/ternary-kernel-launch) | ternary-kernel-launch - SuperInstance ecosystem crate |
| [ternary-knn](https://github.com/SuperInstance/ternary-knn) | K-Nearest Neighbors for Ternary Vector Spaces |
| [ternary-knot](https://github.com/SuperInstance/ternary-knot) | ternary-knot  Knot theory and braid groups in ternary space |
| [ternary-kuramoto](https://github.com/SuperInstance/ternary-kuramoto) | Discrete Kuramoto oscillator for ternary {-1,0,+1} systems |
| [ternary-language](https://github.com/SuperInstance/ternary-language) | Language and grammar processing with ternary sentiment |
| [ternary-language-evolution](https://github.com/SuperInstance/ternary-language-evolution) | How communication protocols evolve over time in balanced ternary {-1, 0, +1} systems |
| [ternary-language-model](https://github.com/SuperInstance/ternary-language-model) | Language modeling with ternary token predictions |
| [ternary-lattice](https://github.com/SuperInstance/ternary-lattice) | Lattice structures for ternary values |
| [ternary-lattice-gc](https://github.com/SuperInstance/ternary-lattice-gc) | Lattice-based garbage collection for GPU object graphs with ternary liveness |
| [ternary-lease](https://github.com/SuperInstance/ternary-lease) | Distributed lease management for GPU resources with ternary states |
| [ternary-life](https://github.com/SuperInstance/ternary-life) | Life for ternary {-1, 0, +1} systems |
| [ternary-lighthouse](https://github.com/SuperInstance/ternary-lighthouse) | Guidance and warning system for fleet navigation |
| [ternary-llm](https://github.com/SuperInstance/ternary-llm) | Ternary LLM building blocks: token embeddings, transformer blocks with ternary weights, BitNet 1 |
| [ternary-locks](https://github.com/SuperInstance/ternary-locks) | Lock algebra inspired by Oracle1's research |
| [ternary-logic](https://github.com/SuperInstance/ternary-logic) | Advanced ternary logic systems |
| [ternary-logistic](https://github.com/SuperInstance/ternary-logistic) | ternary-logistic - SuperInstance ecosystem crate |
| [ternary-loop](https://github.com/SuperInstance/ternary-loop) | Loop for ternary systems |
| [ternary-loss](https://github.com/SuperInstance/ternary-loss) | ternary-loss - SuperInstance ecosystem crate |
| [ternary-manifesto](https://github.com/SuperInstance/ternary-manifesto) | Manifesto for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-market](https://github.com/SuperInstance/ternary-market) | Economic exchange and resource allocation in balanced ternary {-1, 0, +1} systems |
| [ternary-markov](https://github.com/SuperInstance/ternary-markov) | Markov chains on ternary state spaces |
| [ternary-matmul](https://github.com/SuperInstance/ternary-matmul) | Ternary matrix multiplication for {-1, 0, +1} matrices |
| [ternary-matrix](https://github.com/SuperInstance/ternary-matrix) | Matrix operations optimized for ternary values ({-1, 0, +1}) |
| [ternary-membrane](https://github.com/SuperInstance/ternary-membrane) | ternary-membrane  Membrane transport dynamics with ternary concentrations |
| [ternary-memory](https://github.com/SuperInstance/ternary-memory) | ternary-memory  Memory systems for ternary agents |
| [ternary-memory-pool](https://github.com/SuperInstance/ternary-memory-pool) | ternary-memory-pool - SuperInstance ecosystem crate |
| [ternary-mesh](https://github.com/SuperInstance/ternary-mesh) | Dynamic mesh networking between agents with ternary-weighted connections |
| [ternary-metrics](https://github.com/SuperInstance/ternary-metrics) | Performance metrics collection and reporting for ternary systems |
| [ternary-minority](https://github.com/SuperInstance/ternary-minority) | Minority for ternary {-1, 0, +1} systems |
| [ternary-mirror](https://github.com/SuperInstance/ternary-mirror) | State mirroring for GPU cluster replication with ternary consistency |
| [ternary-mixer](https://github.com/SuperInstance/ternary-mixer) | Multi-channel ternary mixer |
| [ternary-morph](https://github.com/SuperInstance/ternary-morph) | Ternary morphological operations: erosion, dilation, opening, closing, skeletonization |
| [ternary-morphogenesis](https://github.com/SuperInstance/ternary-morphogenesis) | ternary-morphogenesis  Alan Turing's morphogenesis: reaction-diffusion patterns on ternary grids |
| [ternary-motion](https://github.com/SuperInstance/ternary-motion) | Ternary motion |
| [ternary-mud](https://github.com/SuperInstance/ternary-mud) | MUD room connections as balanced ternary {-1,0,+1} algebra with Hodge decomposition for navigability |
| [ternary-muse](https://github.com/SuperInstance/ternary-muse) | Creative generation and artistic exploration with ternary systems |
| [ternary-music](https://github.com/SuperInstance/ternary-music) | ternary-music  Musical theory with ternary harmony |
| [ternary-mutual-info](https://github.com/SuperInstance/ternary-mutual-info) | Mutual information for ternary {-1,0,+1} sequences |
| [ternary-navigator](https://github.com/SuperInstance/ternary-navigator) | Ternary Navigator |
| [ternary-needledrop](https://github.com/SuperInstance/ternary-needledrop) | Needle drop |
| [ternary-negotiate](https://github.com/SuperInstance/ternary-negotiate) | Ternary negotiation: agents negotiate using {-1=reject, 0=neutral, +1=accept} signals |
| [ternary-network](https://github.com/SuperInstance/ternary-network) | Network science for ternary-weighted graphs |
| [ternary-noether](https://github.com/SuperInstance/ternary-noether) | Noether's theorem for discrete ternary systems: symmetry→conservation law derivation, verification by numerical simul... |
| [ternary-noise](https://github.com/SuperInstance/ternary-noise) | ternary-noise  Study the effect of noise on ternary agent systems |
| [ternary-norm](https://github.com/SuperInstance/ternary-norm) | ternary-norm - SuperInstance ecosystem crate |
| [ternary-observatory](https://github.com/SuperInstance/ternary-observatory) | Ternary Observatory |
| [ternary-optimizer](https://github.com/SuperInstance/ternary-optimizer) | ternary-optimizer - SuperInstance ecosystem crate |
| [ternary-oracle](https://github.com/SuperInstance/ternary-oracle) | Prediction market for fleet intelligence with ternary confidence staking |
| [ternary-pack](https://github.com/SuperInstance/ternary-pack) | Experimental bit-packing of ternary {-1,0,+1} values for GPU memory efficiency |
| [ternary-pagerank](https://github.com/SuperInstance/ternary-pagerank) | ternary-pagerank  PageRank and centrality measures on ternary-weighted graphs |
| [ternary-pan](https://github.com/SuperInstance/ternary-pan) | Pan for ternary {-1, 0, +1} systems |
| [ternary-pareto](https://github.com/SuperInstance/ternary-pareto) | ternary-pareto  Pareto optimization for ternary agents |
| [ternary-paxos](https://github.com/SuperInstance/ternary-paxos) | Simplified Paxos consensus for GPU cluster decisions with ternary votes |
| [ternary-pca](https://github.com/SuperInstance/ternary-pca) | Principal component analysis for ternary data ({-1, 0, +1}) |
| [ternary-percolate](https://github.com/SuperInstance/ternary-percolate) | Ternary percolation theory: cluster finding, threshold detection, conductance |
| [ternary-percolation](https://github.com/SuperInstance/ternary-percolation) | Percolation for ternary systems |
| [ternary-permutation](https://github.com/SuperInstance/ternary-permutation) | Permutation groups acting on ternary vectors |
| [ternary-petri](https://github.com/SuperInstance/ternary-petri) | Petri for ternary {-1, 0, +1} systems |
| [ternary-phase](https://github.com/SuperInstance/ternary-phase) | ternary-phase Phase relationships between ternary oscillators |
| [ternary-pheromone-market](https://github.com/SuperInstance/ternary-pheromone-market) | Autonomous GPU load balancing via ternary pheromone markets |
| [ternary-pid](https://github.com/SuperInstance/ternary-pid) | Ternary PID controller: continuous PID with ternary output {-1, 0, +1} |
| [ternary-pilgrim](https://github.com/SuperInstance/ternary-pilgrim) | Journey patterns and pilgrimage routes through fleet rooms |
| [ternary-pipeline](https://github.com/SuperInstance/ternary-pipeline) | Composable pipelines for ternary data processing |
| [ternary-pipeline-parallel](https://github.com/SuperInstance/ternary-pipeline-parallel) | Pipeline parallelism for ternary models |
| [ternary-planning](https://github.com/SuperInstance/ternary-planning) | Planning and scheduling with ternary priorities |
| [ternary-platoon](https://github.com/SuperInstance/ternary-platoon) | Group formation and coordinated movement for ternary agents |
| [ternary-polyrhythm](https://github.com/SuperInstance/ternary-polyrhythm) | ternary-polyrhythm Multiple simultaneous rhythmic patterns with ternary support |
| [ternary-pool](https://github.com/SuperInstance/ternary-pool) | Ternary pooling operations for {-1, 0, +1} matrices |
| [ternary-popgen](https://github.com/SuperInstance/ternary-popgen) | Population genetics for ternary agent systems |
| [ternary-predict](https://github.com/SuperInstance/ternary-predict) | Prediction-first perception |
| [ternary-priority-queue](https://github.com/SuperInstance/ternary-priority-queue) | Priority queue for GPU kernel scheduling with ternary scoring |
| [ternary-projection](https://github.com/SuperInstance/ternary-projection) | ternary-projection  Dimensionality reduction techniques adapted for ternary data (`-1`, `0`, `+1`) |
| [ternary-proof](https://github.com/SuperInstance/ternary-proof) | Ternary proof system: verification returns {-1=invalid, 0=inconclusive, +1=valid} |
| [ternary-prophet](https://github.com/SuperInstance/ternary-prophet) | Prediction and forecasting with uncertainty for ternary state systems |
| [ternary-protocol](https://github.com/SuperInstance/ternary-protocol) | ternary-protocol  Wire protocol for communication between ternary agents |
| [ternary-protocol-python](https://github.com/SuperInstance/ternary-protocol-python) | Protocol Python for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-prune](https://github.com/SuperInstance/ternary-prune) | Ternary network pruning |
| [ternary-quantize](https://github.com/SuperInstance/ternary-quantize) | ternary-quantize - SuperInstance ecosystem crate |
| [ternary-quantum](https://github.com/SuperInstance/ternary-quantum) | Quantum-inspired computing with ternary states (qutrits) |
| [ternary-quorum](https://github.com/SuperInstance/ternary-quorum) | Ternary quorum: distributed consensus using ternary voting with Byzantine tolerance |
| [ternary-rack](https://github.com/SuperInstance/ternary-rack) | Signal routing and patching between ternary rooms |
| [ternary-rate-limiter](https://github.com/SuperInstance/ternary-rate-limiter) | Rate limiter for GPU kernel submissions with ternary feedback |
| [ternary-reassembly](https://github.com/SuperInstance/ternary-reassembly) | Message reassembly for GPU cluster communication with ternary fragment status |
| [ternary-reef](https://github.com/SuperInstance/ternary-reef) | Coral reef ecosystem pattern for long-lived collective intelligence |
| [ternary-regex](https://github.com/SuperInstance/ternary-regex) | ternary-regex  Pattern matching on ternary sequences (`-1`, `0`, `+1`) |
| [ternary-register-file](https://github.com/SuperInstance/ternary-register-file) | Register file allocation for ternary GPU kernels |
| [ternary-registry](https://github.com/SuperInstance/ternary-registry) | Capability and skill registry for construct-core integration |
| [ternary-registry-v2](https://github.com/SuperInstance/ternary-registry-v2) | Enhanced skill registry with versioning and dependency management |
| [ternary-regression](https://github.com/SuperInstance/ternary-regression) | ternary-regression - SuperInstance ecosystem crate |
| [ternary-renormalization](https://github.com/SuperInstance/ternary-renormalization) | ternary-renormalization  The renormalization group in ternary systems |
| [ternary-renormalize](https://github.com/SuperInstance/ternary-renormalize) | Renormalize for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-replay](https://github.com/SuperInstance/ternary-replay) | Deterministic replay of agent experiments from seeds |
| [ternary-reservoir](https://github.com/SuperInstance/ternary-reservoir) | Reservoir computing with ternary nodes: echo state networks on {-1, 0, +1}, reservoir dynamics, r |
| [ternary-resilience](https://github.com/SuperInstance/ternary-resilience) | Resilience for ternary {-1, 0, +1} systems |
| [ternary-resonance](https://github.com/SuperInstance/ternary-resonance) | ternary-resonance  Resonance and sympathetic vibration between agents in ternary state spaces |
| [ternary-retry](https://github.com/SuperInstance/ternary-retry) | Retry policy for GPU kernel execution with ternary outcome |
| [ternary-rhythm](https://github.com/SuperInstance/ternary-rhythm) | Temporal pattern recognition and generation using ternary time patterns |
| [ternary-rigging](https://github.com/SuperInstance/ternary-rigging) | Interactive value manipulation and ripple propagation for balanced ternary systems |
| [ternary-ring](https://github.com/SuperInstance/ternary-ring) | Ring and field structures for ternary values |
| [ternary-rl](https://github.com/SuperInstance/ternary-rl) | Reinforcement learning with ternary actions |
| [ternary-robotics](https://github.com/SuperInstance/ternary-robotics) | Robotics control with ternary decisions |
| [ternary-room](https://github.com/SuperInstance/ternary-room) | Recursive room-tensor architecture |
| [ternary-route](https://github.com/SuperInstance/ternary-route) | Ternary routing: route requests with {-1=reject, 0=queue, +1=accept} decisions |
| [ternary-routing](https://github.com/SuperInstance/ternary-routing) | Self-optimizing request routing with ternary feedback |
| [ternary-runlength](https://github.com/SuperInstance/ternary-runlength) | ternary-runlength - SuperInstance ecosystem crate |
| [ternary-sampler](https://github.com/SuperInstance/ternary-sampler) | Sampling strategies for ternary (-1, 0, +1) populations |
| [ternary-sandbox](https://github.com/SuperInstance/ternary-sandbox) | ternary-sandbox  A safe sandbox for running ternary agent experiments with configurable environ |
| [ternary-sandpile](https://github.com/SuperInstance/ternary-sandpile) | Sandpile for ternary {-1, 0, +1} systems |
| [ternary-scheduler](https://github.com/SuperInstance/ternary-scheduler) | Ternary task scheduler with priority {-1=deferred, 0=normal, +1=urgent} |
| [ternary-scheduling](https://github.com/SuperInstance/ternary-scheduling) | Task scheduling using ternary decisions |
| [ternary-scheduling-v2](https://github.com/SuperInstance/ternary-scheduling-v2) | Advanced scheduling with ternary priorities |
| [ternary-science](https://github.com/SuperInstance/ternary-science) | Ternary Science |
| [ternary-scoring](https://github.com/SuperInstance/ternary-scoring) | Multi-criteria scoring for ternary strategies |
| [ternary-search](https://github.com/SuperInstance/ternary-search) | Search algorithms over ternary strategy spaces |
| [ternary-search-index](https://github.com/SuperInstance/ternary-search-index) | Ternary-weighted search index for GPU-accelerable retrieval |
| [ternary-search-rs](https://github.com/SuperInstance/ternary-search-rs) | High-performance ternary vector search server in Rust (axum + rayon + SIMD) |
| [ternary-secret-share](https://github.com/SuperInstance/ternary-secret-share) | Secret sharing schemes over Z/3Z |
| [ternary-seed](https://github.com/SuperInstance/ternary-seed) | Seeded-Model-Programming (SMP) foundation for balanced ternary systems |
| [ternary-semaphore](https://github.com/SuperInstance/ternary-semaphore) | Ternary semaphore for GPU resource control |
| [ternary-sensor](https://github.com/SuperInstance/ternary-sensor) | Sensor data processing with ternary classification |
| [ternary-shard](https://github.com/SuperInstance/ternary-shard) | Sharded ternary data for multi-GPU inference |
| [ternary-shard-merge](https://github.com/SuperInstance/ternary-shard-merge) | Merge distributed ternary weight shards back together |
| [ternary-shard-split](https://github.com/SuperInstance/ternary-shard-split) | Shard ternary model weights across devices |
| [ternary-shared-memory](https://github.com/SuperInstance/ternary-shared-memory) | ternary-shared-memory - SuperInstance ecosystem crate |
| [ternary-sheaf](https://github.com/SuperInstance/ternary-sheaf) | Sheaf for ternary {-1, 0, +1} systems |
| [ternary-shield](https://github.com/SuperInstance/ternary-shield) | Shield for ternary systems |
| [ternary-shipyard](https://github.com/SuperInstance/ternary-shipyard) | Ternary Shipyard |
| [ternary-signal-flow](https://github.com/SuperInstance/ternary-signal-flow) | Experiment: ternary signal flow through GPU processing pipeline |
| [ternary-signaling](https://github.com/SuperInstance/ternary-signaling) | Ternary signaling games |
| [ternary-signals](https://github.com/SuperInstance/ternary-signals) | Ternary signal processing: convolution, filtering, spectral analysis on {-1, 0, +1} signals |
| [ternary-sketch](https://github.com/SuperInstance/ternary-sketch) | Ternary sketch for approximate GPU workload analysis |
| [ternary-som](https://github.com/SuperInstance/ternary-som) | Self-organizing maps (SOM) for ternary data |
| [ternary-sort](https://github.com/SuperInstance/ternary-sort) | Sorting algorithms for ternary data |
| [ternary-spatial](https://github.com/SuperInstance/ternary-spatial) | Ternary spatial math: P48 + Eisenstein |
| [ternary-speculate](https://github.com/SuperInstance/ternary-speculate) | Speculative sync |
| [ternary-spiral](https://github.com/SuperInstance/ternary-spiral) | Spiral wave dynamics from Rock-Paper-Scissors cyclic dominance |
| [ternary-spreadsheet](https://github.com/SuperInstance/ternary-spreadsheet) | Ternary Spreadsheet  Core logic for the SuperInstance Spreadsheet |
| [ternary-spreadsheet-c](https://github.com/SuperInstance/ternary-spreadsheet-c) | Ternary spreadsheet engine in C |
| [ternary-spreadsheet-python](https://github.com/SuperInstance/ternary-spreadsheet-python) | Ternary spreadsheet engine in Python |
| [ternary-steganography](https://github.com/SuperInstance/ternary-steganography) | ternary-steganography  Hide information in ternary strategy noise |
| [ternary-steward](https://github.com/SuperInstance/ternary-steward) | Resource stewardship and sustainable management for ternary systems |
| [ternary-story](https://github.com/SuperInstance/ternary-story) | Ternary narrative engine |
| [ternary-stream-queue](https://github.com/SuperInstance/ternary-stream-queue) | ternary-stream-queue - SuperInstance ecosystem crate |
| [ternary-streaming](https://github.com/SuperInstance/ternary-streaming) | Streaming processing of ternary signals |
| [ternary-surface-memory](https://github.com/SuperInstance/ternary-surface-memory) | Surface memory for ternary texture-like access |
| [ternary-svm](https://github.com/SuperInstance/ternary-svm) | Support Vector Machines for Ternary Feature Spaces |
| [ternary-swarm](https://github.com/SuperInstance/ternary-swarm) | Swarm intelligence with ternary movement and decision making |
| [ternary-symbiont](https://github.com/SuperInstance/ternary-symbiont) | Symbiotic relationships between ternary agents |
| [ternary-symmetry](https://github.com/SuperInstance/ternary-symmetry) | ternary-symmetry  Group theory and symmetry operations in ternary space |
| [ternary-sync](https://github.com/SuperInstance/ternary-sync) | Sync for ternary {-1, 0, +1} systems |
| [ternary-temperament](https://github.com/SuperInstance/ternary-temperament) | Temperament for ternary {-1, 0, +1} systems |
| [ternary-tempo](https://github.com/SuperInstance/ternary-tempo) | Tempo and rhythm detection for ternary sequences |
| [ternary-tenforward](https://github.com/SuperInstance/ternary-tenforward) | Ten-Forward |
| [ternary-tensor](https://github.com/SuperInstance/ternary-tensor) | Tensor operations for ternary multi-dimensional arrays |
| [ternary-tensor-parallel](https://github.com/SuperInstance/ternary-tensor-parallel) | Tensor parallelism for ternary models |
| [ternary-texture-memory](https://github.com/SuperInstance/ternary-texture-memory) | ternary-texture-memory - SuperInstance ecosystem crate |
| [ternary-thermodynamics](https://github.com/SuperInstance/ternary-thermodynamics) | Ternary Thermodynamics  Statistical mechanics analogs for ternary agent systems |
| [ternary-thermostat](https://github.com/SuperInstance/ternary-thermostat) | Ternary thermostat: climate control with PID, multi-zone, and scheduling |
| [ternary-thread-block](https://github.com/SuperInstance/ternary-thread-block) | ternary-thread-block - SuperInstance ecosystem crate |
| [ternary-tidelight](https://github.com/SuperInstance/ternary-tidelight) | Temporal rhythm and timing coordination across the fleet |
| [ternary-tidepool](https://github.com/SuperInstance/ternary-tidepool) | ternary-tidepool: Small protected environments for agent experimentation |
| [ternary-timbre](https://github.com/SuperInstance/ternary-timbre) | **Timbre analysis for agent output characterization |
| [ternary-tnn](https://github.com/SuperInstance/ternary-tnn) | Ternary Neural Network layers: {-1,0,+1} weights with LUT matmul, straight-through estimation, and BitNet-style 1 |
| [ternary-topology](https://github.com/SuperInstance/ternary-topology) | ternary-topology  Persistent homology for ternary networks |
| [ternary-transfer](https://github.com/SuperInstance/ternary-transfer) | ternary-transfer  Transfer learning for ternary agents |
| [ternary-transform](https://github.com/SuperInstance/ternary-transform) | Transform theory for ternary data on {-1, 0, +1} |
| [ternary-transformer](https://github.com/SuperInstance/ternary-transformer) | ternary-transformer - SuperInstance ecosystem crate |
| [ternary-trees](https://github.com/SuperInstance/ternary-trees) | Decision trees and forests for ternary classification on {-1, 0, +1} |
| [ternary-trust](https://github.com/SuperInstance/ternary-trust) | ternary-trust: Trust and relationship dynamics between agents |
| [ternary-tuple](https://github.com/SuperInstance/ternary-tuple) | Tuple for ternary {-1, 0, +1} systems |
| [ternary-turing](https://github.com/SuperInstance/ternary-turing) | ternary-turing  Turing machines over ternary alphabet {-1, 0, 1} |
| [ternary-types](https://github.com/SuperInstance/ternary-types) | Types for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-validation](https://github.com/SuperInstance/ternary-validation) | Validate ternary strategies against constraints |
| [ternary-version](https://github.com/SuperInstance/ternary-version) | Version vectors with ternary comparison for distributed GPU state |
| [ternary-visualization](https://github.com/SuperInstance/ternary-visualization) | Visualization data generation for ternary systems |
| [ternary-visualizer](https://github.com/SuperInstance/ternary-visualizer) | Ternary agent dynamics visualizer |
| [ternary-viterbi](https://github.com/SuperInstance/ternary-viterbi) | Viterbi decoder for ternary state sequences |
| [ternary-vortex](https://github.com/SuperInstance/ternary-vortex) | ternary-vortex  Vortex dynamics and fluid-like flow on ternary grids |
| [ternary-voting](https://github.com/SuperInstance/ternary-voting) | ternary-voting  Voting and consensus mechanisms with ternary values |
| [ternary-voyage](https://github.com/SuperInstance/ternary-voyage) | Long-duration mission planning and execution with ternary progress tracking |
| [ternary-vu](https://github.com/SuperInstance/ternary-vu) | Vu for ternary {-1, 0, +1} systems |
| [ternary-walk](https://github.com/SuperInstance/ternary-walk) | Ternary random walks: simple, biased, correlated, and Lévy flights on Z₃ state space |
| [ternary-walsh](https://github.com/SuperInstance/ternary-walsh) | Walsh functions and transforms for ternary-valued signal analysis |
| [ternary-warp](https://github.com/SuperInstance/ternary-warp) | Warp for ternary systems |
| [ternary-warp-block](https://github.com/SuperInstance/ternary-warp-block) | ternary-warp-block - SuperInstance ecosystem crate |
| [ternary-wasm](https://github.com/SuperInstance/ternary-wasm) | Wasm for the SuperInstance ternary {-1, 0, +1} ecosystem |
| [ternary-watermark](https://github.com/SuperInstance/ternary-watermark) | Ternary watermarking for neural model provenance |
| [ternary-wave](https://github.com/SuperInstance/ternary-wave) | Wave for ternary systems |
| [ternary-weather](https://github.com/SuperInstance/ternary-weather) | Environmental conditions and their effects on agent operations |
| [ternary-world](https://github.com/SuperInstance/ternary-world) | World model for ternary simulations |
| [ternary-zigzag](https://github.com/SuperInstance/ternary-zigzag) | Zigzag scanning for ternary matrix compression |
| [ternary-zkp](https://github.com/SuperInstance/ternary-zkp) | Zero-knowledge proofs over ternary fields GF(3^n) |

## Detailed Summaries

Individual repo summaries are in `ternary-{repo-name}.md` files in this directory.
