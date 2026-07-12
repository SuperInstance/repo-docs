# Fleet Category: Index

**258 repos** in the `fleet-` category from the SuperInstance organization.

## Overview

The `fleet-` prefix covers the **fleet orchestration, coordination, monitoring, and management** layer of the SuperInstance ecosystem. This is the largest category and contains the core infrastructure for running a multi-agent AI fleet.

## Sub-Categories

### 🏗️ Core Infrastructure (20 repos)
The foundational systems every fleet agent depends on:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-agent-core](fleet-agent-core.md) | Rust | Single-binary agent runtime — the universal fleet agent |
| [fleet-agent-api](fleet-agent-api.md) | Python | HTTP API spec for fleet agents |
| [fleet-agent-universal](fleet-agent-universal.md) | Python | Universal Python agent server |
| [fleet-agent-early-version](fleet-agent-early-version.md) | Python | Early MIDI agent server (ports 2160-2175) |
| [fleet-protocol](fleet-protocol.md) | Python | Fleet communication protocol — messages, bottles, security |
| [fleet-proto](fleet-proto.md) | Python | Canonical fleet-core library |
| [fleet-proto-rs](fleet-proto-rs.md) | Rust | Rust shared types for fleet protocol |
| [fleet-types](fleet-types.md) | Python | Canonical Python types (AgentId, Task, StyleVector) |
| [fleet-i2i-protocol](fleet-i2i-protocol.md) | Rust | Inter-agent messaging — SMTP-inspired bottles with speech acts |
| [fleet-manifest](fleet-manifest.md) | Rust | Service registry and agent manifests |
| [fleet-config](fleet-config.md) | Python | Unified config management with layered priority |
| [fleet-auth](fleet-auth.md) | TypeScript | Authentication service (D1 + KV) |
| [fleet-gateway](fleet-gateway.md) | Python | Unified API gateway — routing, auth, rate limiting |
| [fleet-edge-worker](fleet-edge-worker.md) | TypeScript | Cloudflare Workers edge runtime |
| [fleet-stack](fleet-stack.md) | Python | One-command Docker deployment |
| [fleet-containers](fleet-containers.md) | Python | Docker-based agent containerization (72 tests) |
| [fleet-daemon](fleet-daemon.md) | Python | MQTT agent daemon for C2 matrix |
| [fleet-bridge](fleet-bridge.md) | JavaScript | Sign-pattern broadcast for fleet federation |
| [fleet-event-router](fleet-event-router.md) | TypeScript | Event routing service |
| [fleet-registry-worker](fleet-registry-worker.md) | TypeScript | Cloudflare Worker registry |

### 🎯 Coordination & Orchestration (10 repos)
Deciding who does what and managing fleet movement:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-conductor](fleet-conductor.md) | Rust | K8s-style reconciliation loop for agent lifecycle |
| [fleet-coordinator](fleet-coordinator.md) | Rust | Task distribution and agent assignment |
| [fleet-orchestra](fleet-orchestra.md) | Python | Master orchestrator for all 131 repos |
| [fleet-helm](fleet-helm.md) | Rust | Bearings, formations, collision avoidance |
| [fleet-formation-protocol](fleet-formation-protocol.md) | Python | Self-organizing agent groups |
| [fleet-calibrator](fleet-calibrator.md) | Python | Model drift detection and routing table updates |
| [fleet-router](fleet-router.md) | Python | Cost-optimized model routing (critical angle) |
| [fleet-h1-router](fleet-h1-router.md) | Python | H¹ cohomology-aware task routing |
| [fleet-spread](fleet-spread.md) | Rust | Library gate — select THE ONE matching specialist |
| [fleet-bridge](fleet-bridge.md) | JavaScript | Fleet federation via sign patterns |

### 🔢 Math & Constraint Theory (18 repos)
The mathematical foundations — algebraic topology, constraint theory, and consensus:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-coordinate](fleet-coordinate.md) | Rust | ZHC consensus, Laman rigidity, Pythagorean48 trust |
| [fleet-coordinate-js](fleet-coordinate-js.md) | TypeScript | Pure TS port of fleet-coordinate |
| [fleet-math](fleet-math.md) | Python | Canonical fleet math library |
| [fleet-math-py](fleet-math-py.md) | Python | Core math in Python |
| [fleet-math-go](fleet-math-go.md) | Go | Fleet math in Go |
| [fleet-math-ts](fleet-math-ts.md) | TypeScript | Fleet math in TypeScript |
| [fleet-math-c](fleet-math-c.md) | C | SIMD-accelerated constraint math (AVX-512) |
| [fleet-math-benchmarks](fleet-math-benchmarks.md) | C | HPC benchmarks on ARM Neoverse-N1 |
| [fleet-math-demos](fleet-math-demos.md) | Python | Robotics simulation demos |
| [fleet-math-foundations](fleet-math-foundations.md) | C | 12-chapter mathematical monograph |
| [fleet-homology](fleet-homology.md) | Rust | H¹ cohomology emergence detection |
| [fleet-manifold](fleet-manifold.md) | Rust | Constraint manifold geometry (33× compression) |
| [fleet-topology](fleet-topology.md) | Rust | Fleet network topology and routing |
| [fleet-topology-rs](fleet-topology-rs.md) | Rust | Constraint-aware topology with holonomy |
| [fleet-resonance](fleet-resonance.md) | Rust | Emergent pattern detection in comms graphs |
| [fleet-predict](fleet-predict.md) | Rust | Correlation-based predictive coding |
| [fleet-ecology](fleet-ecology.md) | Rust | Multi-fleet ecology simulator |
| [fleet-formal-proofs](fleet-formal-proofs.md) | — | Formal proofs for constraint theory |

### 🛡️ Constraint & Safety (6 repos)
Enforcing safety constraints on agent actions:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-constraint](fleet-constraint.md) | Python | Gatekeeper runtime — FLUX-C bytecode VM |
| [fleet-constraint-kernel](fleet-constraint-kernel.md) | CUDA | GPU sonar beamformer constraint evaluator |
| [fleet-constraint-monitor](fleet-constraint-monitor.md) | — | H1 constraint violation monitor |
| [fleet-raid5](fleet-raid5.md) | Python | RAID-5 constraint striping with temporal parity |
| [fleet-crdt](fleet-crdt.md) | Rust | Constraint-Native CRDT merge protocol |
| [fleet-sandbox](fleet-sandbox.md) | Rust | Codebase analysis through conservation law |

### 📊 Monitoring & Health (8 repos)
Watching fleet state and agent health:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-health-monitor](fleet-health-monitor.md) | Python | 4-state health model with watchdogs (248 tests) |
| [fleet-health](fleet-health.md) | TypeScript | Health check service |
| [fleet-dashboard](fleet-dashboard.md) | JavaScript | Multi-agent C2 dashboard (HTML/MQTT) |
| [fleet-dashboard-api](fleet-dashboard-api.md) | TypeScript | Live telemetry API |
| [fleet-dashboard-night](fleet-dashboard-night.md) | HTML | 6-panel fleet math stack dashboard |
| [fleet-neofetch](fleet-neofetch.md) | Python | System info for fleets |
| [fleet-chronicle](fleet-chronicle.md) | Python | Agent reporting office with web UI |
| [fleet-logger](fleet-logger.md) | Python | JSONL structured logging with query engine |

### ⏱️ Time, Physics & Cognition (7 repos)
Novel approaches to fleet time, consciousness, and self-modeling:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-clock](fleet-clock.md) | Rust | Thermodynamic clock, arrow of time, Maxwell's demon |
| [fleet-phase](fleet-phase.md) | Rust | Phase analysis (undocumented) |
| [fleet-yaw](fleet-yaw.md) | Rust | Bearing-rate autopilot (first-person fleet physics) |
| [fleet-keel](fleet-keel.md) | Rust | 5D self-orientation (53 GPU experiments) |
| [fleet-consciousness](fleet-consciousness.md) | Rust | IIT applied to fleets — Φ, causal density, attention |
| [fleet-consciousness-dashboard](fleet-consciousness-dashboard.md) | Python | Fleet Consciousness Index (FCI) dashboard |
| [fleet-homunculus](fleet-homunculus.md) | Python | Body image, reflex arcs, pain assessment |

### 💾 Memory & Storage (3 repos)
Distributed fleet memory systems:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-memory](fleet-memory.md) | Rust | Content-addressable distributed memory |
| [fleet-holographic](fleet-holographic.md) | Rust | Holographic storage — any agent reconstructs the whole |
| [fleet-logger](fleet-logger.md) | Python | Centralized structured logging |

### ⚡ Conservation & Energy (2 repos)
The γ + η = C conservation law:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-conservation](fleet-conservation.md) | Rust | Conservation tracker (37 tests, forgecode hooks) |
| [fleet-bench](fleet-bench.md) | C | Hardware profiling of constraint crates |

### 📨 Messaging (5 repos)
Inter-agent communication:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-bottle](fleet-bottle.md) | Rust | Bottle protocol library (26 tests) |
| [fleet-bottles](fleet-bottles.md) | Python | Audit reports and design notes in bottle format |
| [fleet-i2i-protocol](fleet-i2i-protocol.md) | Rust | Full I2I protocol with speech acts |
| [fleet-event-router](fleet-event-router.md) | TypeScript | Event routing |
| [fleet-murmur-worker](fleet-murmur-worker.md) | TypeScript | 5 thinking strategies, quality-gated |

### 🔄 Build & CI (6 repos)
Building, testing, and deploying the fleet:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-build](fleet-build.md) | Rust | Automated Rust crate build-test-push CLI |
| [fleet-ci](fleet-ci.md) | Python | GitHub Actions workflows |
| [fleet-cicd-agent](fleet-cicd-agent.md) | Python | Pipeline orchestration, 3 deployment strategies |
| [fleet-harness](fleet-harness.md) | Python | Clone-build-test-report for entire fleet |
| [fleet-containers](fleet-containers.md) | Python | Docker containerization |
| [fleet-arm-compat](fleet-arm-compat.md) | Shell | ARM64 multi-arch builds |

### 📚 Documentation & Meta (16 repos)
Guides, tutorials, and ecosystem maps:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-architecture](fleet-architecture.md) | Docs | Complete architecture docs (56+ repos, 5 layers) |
| [fleet-contributing](fleet-contributing.md) | Docs | Ecosystem-wide contributing guide |
| [fleet-getting-started](fleet-getting-started.md) | Docs | Onboarding guide |
| [fleet-tutorials](fleet-tutorials.md) | Docs | Beginner to deep-dive tutorials |
| [fleet-ecosystem](fleet-ecosystem.md) | Docs | Ecosystem map |
| [fleet-status](fleet-status.md) | Docs/HTML | Live status and crate index |
| [fleet-map](fleet-map.md) | HTML | Interactive constellation map |
| [fleet-survey](fleet-survey.md) | Docs | Cross-pollination report |
| [fleet-research](fleet-research.md) | Docs | Industry landscape research |
| [fleet-science](fleet-science.md) | Python | Papers, experiments, proofs |
| [fleet-experiments](fleet-experiments.md) | Python | Experimental verification of fleet math |
| [fleet-integration](fleet-integration.md) | Python | Integration tests (4 scenarios) |
| [fleet-org](fleet-org.md) | Docs | Org chart and spawning guide |
| [fleet-self-onboarding](fleet-self-onboarding.md) | Docs | Self-onboarding for autonomous agents |
| [fleet-characters](fleet-characters.md) | Python | Agent identity and narrative arcs |
| [fleet-workshop](fleet-workshop.md) | Python | Idea incubation — Casey picks what gets built |

### 🔧 Fleet Utilities (12 repos)
Practical tools for fleet management:

| Repo | Stack | Summary |
|------|-------|---------|
| [fleet-dedup](fleet-dedup.md) | Rust | Duplicate repo detection |
| [fleet-mapper](fleet-mapper.md) | Rust | Scan, fingerprint, categorize repos |
| [fleet-scanner](fleet-scanner.md) | Rust | Git repo health scanner |
| [fleet-refactor-agent](fleet-refactor-agent.md) | Python | The Shipwright — merges and consolidates repos |
| [fleet-vessel](fleet-vessel.md) | Python | Git-native garbage collector |
| [fleet-warden](fleet-warden.md) | Rust | WSL disk cleanup daemon (54 GB recovered) |
| [fleet-warden-rs](fleet-warden-rs.md) | Rust | Enhanced warden with anomaly detection |
| [fleet-mechanic](fleet-mechanic.md) | Python | Autonomous maintenance agent |
| [fleet-code-agent](fleet-code-agent.md) | TypeScript | Standalone build-test-commit agent |
| [fleet-github-app](fleet-github-app.md) | Python | GitHub App — webhooks, bot identity |
| [fleet-wiki](fleet-wiki.md) | Python | Wiki engine with BM25 search and API docgen |
| [fleet-tool-registry](fleet-tool-registry.md) | Python | PLATO tool discovery for agents |

### 🎓 Cultural Perspectives (8 repos)
Multi-cultural AI reasoning:

| Repo | Language | Summary |
|------|----------|---------|
| fleet-arabic | العربية | Arabic cultural perspective |
| fleet-chinese | 中文 | Chinese cultural perspective |
| fleet-english | English | English cultural perspective |
| fleet-finnish | Suomi | Finnish cultural perspective |
| fleet-japanese | 日本語 | Japanese cultural perspective |
| fleet-latin | Latin | Latin cultural perspective |
| fleet-navajo | Diné bizaad | Navajo cultural perspective |
| fleet-sanskrit | संस्कृतम् | Sanskrit cultural perspective |

### 🎵 MIDI Fleet (~100 repos)
The largest sub-group — ternary vectors → music:

**Core MIDI libraries:** fleet-midi, fleet-midi-harmonizer, fleet-midi-effects, fleet-midi-markov, fleet-midi-phase, fleet-midi-pulse, fleet-midi-resonance

**Live Paradigm Fleet agents (16 ternary agents on ports 2160-2175):**
fleet-midi-chord, fleet-midi-scale, fleet-midi-voicing, fleet-midi-tempo, fleet-midi-groove, fleet-midi-velocity, fleet-midi-fx, fleet-midi-register, fleet-midi-melody, fleet-midi-modulation, fleet-midi-mode, fleet-midi-dynamics, fleet-midi-expression, fleet-midi-arp, fleet-midi-articulation, fleet-midi-bass

**Algorithmic/Generative (~50 repos):**
fleet-midi-arpeggiator, fleet-midi-batch, fleet-midi-blend, fleet-midi-bridge, fleet-midi-cc, fleet-midi-chaos, fleet-midi-cluster, fleet-midi-collab, fleet-midi-composer, fleet-midi-conductor, fleet-midi-cycle, fleet-midi-decode, fleet-midi-delay, fleet-midi-drone, fleet-midi-echo, fleet-midi-emergent, fleet-midi-encode, fleet-midi-feed, fleet-midi-filter, fleet-midi-flux, fleet-midi-fractal, fleet-midi-generator, fleet-midi-genetic, fleet-midi-gliss, fleet-midi-grammar, fleet-midi-graph, fleet-midi-inversion, fleet-midi-layer, fleet-midi-live, fleet-midi-looper, fleet-midi-mapper, fleet-midi-mesh, fleet-midi-monitor, fleet-midi-morph, fleet-midi-pan, fleet-midi-pattern, fleet-midi-pedagogy, fleet-midi-player, fleet-midi-prob, fleet-midi-quantizer, fleet-midi-quantum, fleet-midi-rand, fleet-midi-recorder, fleet-midi-remapper, fleet-midi-reverb, fleet-midi-router, fleet-midi-script, fleet-midi-sequencer, fleet-midi-spread, fleet-midi-stream, fleet-midi-studio, fleet-midi-substitution, fleet-midi-swarm, fleet-midi-synth, fleet-midi-text2midi, fleet-midi-tide, fleet-midi-tokenizer, fleet-midi-tremolo, fleet-midi-vel, fleet-midi-visualizer, fleet-midi-wave, fleet-midi-weave

**Connectors (10 repos):**
fleet-diffrhythm-connector, fleet-hydra-connector, fleet-magenta-connector, fleet-maidi-connector, fleet-midee-connector, fleet-orca-connector, fleet-rave-connector, fleet-strudel-connector, fleet-touchdesigner-connector, fleet-midi-foxdot, fleet-midi-sonicpi, fleet-midi-tidalcycles, fleet-midi-musiclang, fleet-midi-symusic, fleet-midi-juce

### 🔍 Other (12 repos)
Miscellaneous fleet repos:

| Repo | Stack | Summary |
|------|-------|---------|
| fleet-a2a-bridge | Python | A2A bridge |
| fleet-a2a-pipeline | JavaScript | A2A pipeline |
| fleet-a2a-spectral | Python | A2A spectral |
| fleet-a2a-wasm | JavaScript | A2A WASM module |
| fleet-oracle | Rust | Local decision engine (SVM+Entropy+Search) |
| fleet-oracle2 | Python | ARM-native agent orchestration |
| fleet-discovery | Python | Falsification-driven research engine |
| fleet-scribe | Python | Digital twin builder |
| fleet-stitch | Python | Merge agent outputs into narratives |
| fleet-symmetry-analyzer | Python | Symmetry analysis |
| fleet-fugue-engine | Python | Fugue-like math processes |
| fleet-voice-leader | Python | Conservation laws for counterpoint |
| fleet-ternary-music | Rust | Core ternary→music math |
| fleet-osc-server | JavaScript | OSC server |
| fleet-jam-engine | JavaScript | One-command full-band MIDI |
| fleet-music-theorist | Python | Music theory analysis |
| fleet-sheet-music | Python | Printable score generation |
| fleet-sound-toolkit | Python | Audio synthesis toolkit |
| fleet-ensemble | Makefile | Multi-agent music coordination |
| fleet-intel | Python | Fleet intelligence sensor array |
| fleet-miner | Python | Git data mining (734 commits) |
| fleet-murmur | Python | Agent workspace data |
| fleet-daily | Docs | Fleet daily news |
| fleet-logs | Docs | Activity logs |
| fleet-liaison-tender | Python | Inter-vessel communication |
| fleet-deepinfra-test | Python | DeepInfra API test suite |
| fleet-router-integration | Python | Router integration tests |
| fleet-automation-early-version | Python | [ARCHIVED] 5KB scaffolding |
| fleet-json-a2a | JSON | A2A machine-readable spec |
| fleet-energy-spec | — | ATP-based energy coordination spec |
| fleet-mcp-server | JavaScript | MCP server for semantic search |
| fleet-vector-api | TypeScript | Semantic search (BGE embeddings) |
| fleet-simulator | Python | Multi-agent fleet simulator |
| fleet-simulation | Python | Fleet simulation |
| fleet-sim-rs | Rust | Lock-free cancellation simulator (561M sig/s) |
| fleet-simulators | HTML | 4 browser simulators |
| fleet-kit | Python | Modular toolkit (PLATO client, router, audit) |
| fleet-intelligence-api | TypeScript | Unified ternary decision engine |
| fleet-neofetch | Python | System info for fleets |

## Honest Overall Assessment

### What's Real
The fleet-* repos represent a **genuinely ambitious multi-agent AI fleet architecture** with serious mathematical foundations. The best repos demonstrate real engineering:

- **fleet-i2i-protocol** — A well-designed inter-agent messaging protocol
- **fleet-coordinate** — Novel application of algebraic topology to consensus
- **fleet-conductor** — Thoughtful K8s-style fleet orchestration
- **fleet-health-monitor** — Production-quality monitoring (248 tests)
- **fleet-warden(-rs)** — Practical disk cleanup with resilience patterns
- **fleet-holographic** — Legitimate holographic storage with experimental validation
- **fleet-clock** — Fascinating thermodynamic clock research
- **fleet-consciousness** — Real IIT implementation
- **fleet-intelligence-api** — Insightful ternary decision unification
- **fleet-vector-api** — Practical semantic search with correct scaling reasoning

### What's Template-Driven
~80 MIDI repos follow a **consistent template** with varying depth:
- ~16 "Live Paradigm Fleet" agents with full READMEs (API docs, ternary logic, education)
- ~30 repos with shortened or boilerplate READMEs
- ~30 repos with one-line READMEs or minimal stubs

These aren't fake — they're consistent with a code-generation/template strategy for a music pipeline. But many have minimal implementation substance.

### What's Thin
- 5 repos have no README at all (fleet-health, fleet-constraint-monitor, fleet-code-agent, fleet-event-router, fleet-registry-worker, fleet-phase, fleet-simulation)
- Cultural perspective repos (8) are conceptually interesting but likely thin implementations
- Several "connector" repos have truncated or repetitive READMEs

### The Big Picture
This is a **single-person ecosystem** (Casey/JetsonClaw1/Oracle1) building an elaborate multi-agent AI fleet with:
1. Novel mathematical foundations (algebraic topology, thermodynamic clocks, conservation laws)
2. A complete MIDI/music pipeline turning agent state into music
3. Serious infrastructure (monitoring, CI/CD, containers, health checks)
4. Documentation depth (architecture docs, tutorials, formal proofs)

The math is legitimate even if unconventional. The engineering ranges from production-quality (health-monitor, warden, i2i-protocol) to aspirational (conductor). The MIDI fleet is conceptually consistent but varies wildly in implementation depth.

**Scale: 258 repos, but ~80+ are MIDI micro-services following shared templates. The core infrastructure is maybe 40-50 repos with genuine engineering.**
