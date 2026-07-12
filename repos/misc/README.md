# Miscellaneous Repos — Index

**Total repos: 1,200**

The catch-all category for SuperInstance repositories that don't fit into a single dedicated category. Despite the "misc" label, this collection contains substantial, important projects spanning agent infrastructure, mathematical libraries, cultural math, game development, developer tools, and experimental research. Below, repos are organized by thematic groupings.

## Category Overview

### Thematic Distribution

| Theme | Count | Description |
|-------|-------|-------------|
| Agent/Fleet Infrastructure | ~115 | I2I protocol, fleet coordination, swarm orchestration, murmur protocol |
| Algorithms & Data Structures | ~58 | Trees, graphs, sorting, caching, bloom filters, ring buffers |
| Music & Audio | ~51 | MIDI, harmony, rhythm, spectral analysis, groove |
| AI/ML & Cognitive | ~51 | JEPA, embeddings, bandits, Kalman filters, Bayesian inference |
| Systems & Infrastructure | ~54 | Caching, scheduling, routing, rate limiting, monitoring |
| Web & Frontend | ~54 | Dashboards, landing pages, browser tools, UI components |
| Logging & Applications | ~59 | MakerLog, BusinessLog, PlayerLog, StudyLog, activity tracking |
| Conservation & Constraints | ~39 | Conservation laws, Noether theorem, spectral invariants |
| Cultural Mathematics | ~31 | Griot, Quipu, Adinkra, Songline, Palaver traditions |
| Game & MUD | ~30 | MUD arena, colony games, chess, voxel worlds |
| Protocol & Networking | ~30 | WebSockets, gRPC, mux/demux, packet capture |
| Shell & CLI Tools | ~33 | Prompt builders, TUI tools, terminal harnesses |
| Templates & Archives | ~43 | README generators, starters, bootstraps, demos |
| Dream & Cognitive | ~16 | Dream consolidation, lucid dreaming, creativity engines |
| Renormalization & Scale | ~17 | RG flow, multi-scale analysis, coarse-graining |
| Optimal Transport | ~12 | Wasserstein, Monge, Sinkhorn, Fisher-Rao |
| Topology & Geometry | ~38 | Homology, Betti numbers, Čech complexes, sheaves |
| Crypto & Security | ~35 | Lattice crypto, ZKP, ring signatures, commitments |
| Physics & Thermo | ~22 | Hamiltonians, Boltzmann, thermodynamics, particles |
| Compression & Encoding | ~11 | Huffman, BWT, LZ77, RLE, trie encoding |

---

## Major Thematic Groups

### 1. Agent Communication & Fleet Infrastructure

The I2I (Iron-to-Iron) protocol and fleet coordination layer:
- **i2i-vessel** — Agent communication protocol with typed bottles, filesystem transport, ACK semantics
- **iron-to-iron** — Agent-to-agent communication through git. "Iron sharpens iron. We don't talk, we commit."
- **i2i-protocol** / **i2i-bottle-agent** — Protocol specification and bottle agent
- **bottle-protocol** — Message-in-a-bottle async communication
- **murmur-protocol** / **Murmur** / **Murmurer** — Gossip-style messaging
- **beacon-protocol** — Beacon-based discovery
- **commodore-protocol** / **ensign-protocol** — Naval hierarchy protocols
- **federation-protocol** — Federation for multi-org fleets
- **herdr-cocapn** — Herdr + Cocapn integration (agent multiplexer + fleet management)
- **cluster-orchestrator** — Multi-agent cluster orchestration

### 2. Cultural Mathematics

Mathematical traditions from non-Western cultures, each providing unique formal frameworks:
- **griot-math** (+ npm, pypi, C, WASM, v2) — West African griot tradition: stories as data structures
- **quipu-math** (+ C, npm, WASM) — Andean quipu: knot-based encoding
- **adinkra-math** (+ npm, pypi) — West African Adinkra symbols as mathematical objects
- **songline-math** (+ C, pypi, WASM) — Aboriginal songline navigation as graph theory
- **palaver-math** (+ C, pypi) — African palaver dialogue as consensus mechanism
- **west-african-math-c** / **west-african-math-rs** — Broader West African mathematics
- **symmetry-math** (+ C, npm) — Symmetry groups from cultural patterns
- **rhythm-math** (+ C, npm) — Cross-cultural rhythm mathematics
- **rhythm-nation-math** — Rhythmic patterns at scale
- **pythagorean48** / **pythagorean48-codes** — Pythagorean traditions

### 3. Cognitive & Dream Systems

- **dream-cycle** — When the cortex sleeps, it dreams. Consolidation, creativity, anomaly detection
- **luciddreamer-agent** / **luciddreamer-os** / **luciddreamer-vision** — Lucid dream agent system
- **dream-compiler** — Compiling dream-state programs
- **formal-consciousness** — Formalizing consciousness mathematically
- **memory-palace** / **memory-plimpsest** — Memory architecture systems
- **cognitive-archaeology** — Archaeological analysis of cognitive artifacts
- **cathedral-probe** — Deep cognitive probing

### 4. Optimal Transport & Wasserstein

- **wasserstein-agents** / **wasserstein-agents-rs** — Wasserstein distance for fleet comparison
- **monge-fleet** / **monge-rs** — Monge formulation of optimal transport
- **optimal-transport-rs** / **optimal-transport-agents-rs** — General OT framework
- **wasserstein-narrative** — Narrative distance measurement
- **wasserstein-ot-c** — C implementation
- **fisher-rao** — Fisher-Rao information metric
- **bregman-divergence** — Bregman divergence for clustering

### 5. Renormalization Group & Multi-Scale

- **renormalization-group** / **renormalization-group-rs** — RG framework for fleet analysis
- **renormalization-learning-rs** / **renormalization-learning-c** — RG for learning
- **renormalization-agent** — RG agent for multi-scale coordination
- **population-scaling** — Population dynamics at scale
- **scale-fold** — Multi-scale folding

### 6. Music & Audio Mathematics

- **betti-music-computation** — Betti numbers for musical structure
- **holonomy-harmony** / **holonomy-harmony-rs** — Holonomy in musical harmony
- **jazz-voicing-engine** — Jazz chord voicing generation
- **groove-analyzer** — Groove pattern analysis
- **lotka-beats** — Lotka-Volterra rhythmic dynamics
- **tensor-midi** — Tensor-based MIDI processing
- **spline-instrument** / **spline-midi-smooth** — Spline interpolation for MIDI
- **tonnetz-constraints** — Tonnetz harmonic constraints
- **resonance-engine** — Resonance modeling

### 7. Algorithms & Data Structures

Pure Rust implementations of classic CS:
- **avl-tree-rs**, **red-black-tree-rs**, **b-tree-rs**, **b-tree**, **r-tree-rs**, **kd-tree-rs** — Tree structures
- **skip-list-rs**, **segment-tree-rs**, **fenwick-tree-rs**, **treap-rs** — Index structures
- **bloom-filter-rs** — Probabilistic membership
- **ring-buffer** / **ring-buffer-rs** — Circular buffers
- **suffix-array-rs**, **suffix-automaton-rs** — String data structures
- **aho-corasick-rs** — Multi-pattern string search
- **lsm-tree** — Log-structured merge tree
- **delaunay-triang-rs** — Delaunay triangulation
- **convex-hull-rs** — Convex hull computation

### 8. Game & MUD Systems

- **mud-arena** — MUD combat arena
- **mud-agent** / **mud-bridge** / **mud-expert-1** / **mud-solitaire** — MUD agents and tools
- **mud2scummvm** — MUD to ScummVM bridge
- **colony-games** — Colony simulation games
- **chess-engine** — Chess engine
- **gh-dungeons** — GitHub dungeons
- **voxel-logic** / **voxelworks** — Voxel engines
- **SuperInstance-gamedev** — Game development framework

### 9. Logging & Activity Applications

A family of structured logging applications:
- **MakerLog** / **makerlog-agent** / **makerlog-ai** — Maker/hacker project log
- **BusinessLog** / **businesslog-agent** — Business activity log
- **PlayerLog** / **playerlog-agent** — Game player log
- **StudyLog** / **studylog-agent** — Study tracking
- **PersonalLog** / **personallog-agent** — Personal activity
- **RealLog** / **reallog-agent** — Real-time logging
- **DMLog** / **DMLog-AI** / **dmlog-agent** — D&D campaign tracker (Cloudflare Worker)

### 10. Topology & TDA

- **persistent-sheaf** / **persistent-sheaf-rs** — Persistent sheaf cohomology (13,062-char README)
- **tda-rs** / **tda-c** — Topological data analysis
- **homology-engine** — Homology computation
- **witness-complex** / **witness-topology** / **witness-topology-rs** — Witness complexes
- **cech-complex** — Čech complex construction
- **betti-curve** — Betti curve analysis
- **cospectral-explorer** — Spectral graph exploration

### 11. Physics & Thermodynamics

- **boltzmann-agent** — Boltzmann machine agents
- **free-energy** — Free energy computation
- **thermal-budget** — Thermal budget tracking
- **heat-spectral** — Heat kernel spectral analysis
- **landauer** — Landauer limit computation
- **quantum-thermo** — Quantum thermodynamics
- **physics-clock** — Physics-based timing

### 12. Crypto & Security

- **lattice-crypto** / **lattice-crypto-rs** — Lattice-based cryptography
- **zkp-rs** / **zero-knowledge** — Zero-knowledge proofs
- **ring-sign** — Ring signatures
- **diffie-hellman-rs** — DH key exchange
- **feistel-net** — Feistel cipher network
- **homomorphic-hash** — Homomorphic hashing
- **commitment-scheme** — Commitment schemes
- **secret-sharing** / **secret-share** / **secret-manager** / **secret-scanner** — Secret management

### 13. Compression & Encoding

- **huffman-code** / **huffman-entropy** — Huffman coding
- **arithmetic-code** — Arithmetic coding
- **bwt-compress** — Burrows-Wheeler transform
- **delta-encode** — Delta encoding
- **run-length** — Run-length encoding
- **fold-compression** — Fold-based compression

### 14. Polyformalism

An experiment in expressing the same constraint kernel across 13 programming languages:
- **polyformalism** — Core experiment: same 3 functions, 13 languages, 2,100 test vectors
- **polyformalism-a2a-js** / **polyformalism-a2a-python** — JS/Python implementations
- **polyformalism-languages** — Language comparison
- **polyformalism-thinking** — Conceptual framework
- **polyformalism-turbo-shell** — Turbo shell variant
- **linguistic-polyformalism-shell** — Linguistic analysis

### 15. Free Probability

- **free-probability** — "The only implementation in any systems language." Random matrices meet operator algebras in Rust
- **free-probability-c** / **free-probability-rs** — C and Rust ports

### 16. ZeroClaw-Adjacent & Beta Testing

- **beta-test-alex** / **beta-test-elena** / **beta-test-marcus** / **beta-test-priya** — Individual beta test setups
- **casting-call** / **casting-call-gpu** / **casting-call-mcp** — Agent audition/casting
- **purplepincher** / **purplepincher-baton** / **purplepincher-org** / **purplepincher-shell-library** — PurplePincher project
- **Forgemaster** / **forgemaster-docs** / **forgemaster-fleet-comms** / **forgemaster-memory-archive** / **forgemaster-shell** — Forgemaster system

### 17. SuperZ & Twins

- **superz-diary** / **superz-parallel-fleet-executor** / **superz-runtime** / **superz-twin** / **superz-vessel** — SuperZ agent system
- **super-z-quartermaster** — Quartermaster agent

### 18. Dojo & Training

- **dojo** / **dojo-alchemist** / **dojo-builder** / **dojo-musician-rooms** / **dojo-scout** / **dojo-scribe** — Dojo training system
- **bootcamp** / **bootcamp-engine** — Bootcamp for new agents
- **z-agent-bootcamp** — Agent bootcamp
- **greenhorn** / **greenhorn-onboarding** — New agent onboarding

### 19. Practical Applications

- **lucineer-com** / **lucineer-flagship** / **Lucineer-Stem-quest** — Lucid dream practice tool
- **eveng1_python_sdk** — Even G1 Smart Glasses BLE SDK
- **AI-Smart-Notifications** — Smart notification system
- **AI-Writings** — AI-generated writings
- **amplify-fishingtool** — Fishing tool amplification
- **fishermanscopilot** — Fisherman's copilot
- **FishingLog** — Fishing log application
- **Privacy-First-Analytics** — Privacy-focused analytics
- **In-Browser-Dev-Tools** — Browser developer tools
- **In-Browser-Vector-Search** — Browser-based vector search
- **Automatic-Type-Safe-IndexedDB** — Type-safe IndexedDB wrapper
- **Real-Time-Collaboration** — Real-time collaboration tool
- **Spreader-tool** / **Spreadsheet-ai** — Spreading/spreadsheet tools

### 20. Notable Single Repos

- **persistent-sheaf** — One of the most documented repos in all of misc (353-line README, 10 code blocks). Cellular sheaf Laplacians, Vietoris-Rips complexes, multi-modal data fusion
- **free-probability** — Unique in any systems language. Random matrices and operator algebras
- **polyformalism** — 13 languages, 2,100 differential test vectors
- **renormalization-group** — Physics RG applied to fleet dynamics
- **mycelium** — "Captures any behavior as a seed. One prompt + one seed = exact action"
- **i2i-vessel** — Typed bottles, filesystem transport, any language
- **iron-to-iron** — "Iron sharpens iron. We don't talk, we commit."
- **Mycelium** — Fungal-network-inspired routing
- **grove-ast** / **grove-compiler** — Grove language AST and compiler
- **glyph-language** — Glyph-based language system
- **shadow-cathedral** — Mysterious "shadow" architecture
- **sunset-ecosystem** — Ecosystem sunset/deprecation tooling

---

## Cross-Category Interconnections

The misc category serves as the connective tissue between all other categories:

- **I2I protocol** (i2i-vessel, iron-to-iron) underpins agent communication across agent-framework, cocapn-marine, and superinstance-core
- **Cultural math** (griot, quipu, adinkra, songline) connects to lau-mathematics (lau-griot, lau-songline, lau-quipu, lau-adinkra)
- **Cognitive systems** (dream-cycle, active-inference) relate to activelog and the broader AI/ML stack
- **TDA repos** (persistent-sheaf, witness-topology, homology-engine) extend sheaf-topology
- **Optimal transport** repos connect to si-wasserstein-fleet in superinstance-core
- **Conservation repos** extend conservation-laws and lau-conservation-laws
- **Compression repos** support forge-tiles and lau-tile-compress
- **Game/MUD repos** connect to roblox-gaming and zeroclaw
- **Fleet infrastructure** bridges to cocapn-marine and agent-framework

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
