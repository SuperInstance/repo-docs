# SuperInstance Repo Consolidation Plan

**Generated:** 2026-07-12  
**Scope:** 3,327 original repos across the SuperInstance GitHub org  
**Goal:** Identify groups of 5+ closely related repos that could be merged into single monorepos or workspaces to reduce sprawl.

---

## Executive Summary

The SuperInstance org has **3,327 repos** across three major ecosystems (Ternary: 370, FLUX: 165, PLATO: 262) plus ~2,530 "other" repos. The vast majority are tiny crates created in a burst (~10 days for ternary, similar patterns elsewhere). Many clusters of 5-50+ repos share the same prefix, domain, and author, differ only in being one-function or one-module crates, and would benefit enormously from consolidation into workspace monorepos.

This plan identifies **12 high-impact consolidation clusters** covering **~750+ repos** that could be reduced to **~12 monorepos**, cutting the org's repo count by roughly 22%.

---

## Cluster 1: `lau-*` Math & Physics Library → `lau-workspace`

**Current state:** ~333 repos  
**Proposed merged repo:** `lau-workspace` (Rust Cargo workspace)

### Repos to merge (representative — full list is 333 repos)
All `lau-*` repos are Rust crates implementing mathematical/physical concepts for a game/engine called "LAU". They share identical structure, conventions, and dependencies.

**Categories within lau-*:**

| Sub-cluster | ~Count | Example repos |
|-------------|--------|---------------|
| Agent systems | ~25 | lau-agent-dream, lau-agent-homeostasis, lau-agent-lifecycle, lau-agent-organism, lau-agent-runtime, lau-agent-shell, lau-agent-thermodynamics, lau-agent-topology |
| Conservation/spectral | ~12 | lau-conservation-engine, lau-conservation-experiment, lau-conservation-guard, lau-conservation-laws, lau-conservation-matrix, lau-conservation-spectral |
| Geometry/topology | ~25 | lau-algebraic-geometry, lau-algebraic-topology, lau-contact-geometry, lau-differential-topology, lau-kahler-geometry, lau-information-geometry |
| Dynamical systems | ~10 | lau-dynamical-systems, lau-dynamical-algebra, lau-dynamical-systems-agents, lau-linear-systems |
| Game engine | ~15 | lau-animation, lau-camera, lau-biome, lau-ecs, lau-input, lau-audio, lau-blueprint |
| Category theory | ~10 | lau-category-theory, lau-categorical-homotopy, lau-categorical-mechanics, lau-functor-network |
| Physics | ~15 | lau-electromagnetism, lau-fluid-dynamics, lau-gravity-field, lau-thermodynamics |
| Crypto/security | ~5 | lau-cryptography, lau-lattice-crypto |
| Information theory | ~8 | lau-information-theory, lau-information-geometry, lau-entropy |
*...and ~200+ more*

- **Estimated difficulty:** Medium (standard Cargo workspace restructuring)
- **Priority:** 🔴 **HIGH** — 333 repos is the single largest consolidatable cluster
- **Benefits:**
  - Eliminates 332 repos from the org
  - Cross-crate refactoring becomes trivial (single `cargo test`)
  - Dependency management unified
  - `lau-glue` (which already exists to bridge 108+ crates) becomes unnecessary
  - `lau-bench` (which benchmarks all lau-* crates) can run in-tree

---

## Cluster 2: `grand-pattern-*` Multi-Language Ports → `grand-pattern`

**Current state:** 41 repos  
**Proposed merged repo:** `grand-pattern` (polyglot monorepo)

### Repos to merge
grand-pattern-abi, grand-pattern-adversarial, grand-pattern-bench, grand-pattern-bench-v2, grand-pattern-c, grand-pattern-chapel, grand-pattern-claude, grand-pattern-cli, grand-pattern-core, grand-pattern-cuda, grand-pattern-design, grand-pattern-embedded, grand-pattern-experiments, grand-pattern-ffi, grand-pattern-flux, grand-pattern-fortran, grand-pattern-go, grand-pattern-gpu, grand-pattern-integration, grand-pattern-java, grand-pattern-kimi, grand-pattern-kit, grand-pattern-mojo, grand-pattern-mono, grand-pattern-mono-go, grand-pattern-mono-py, grand-pattern-mono-ts, grand-pattern-net, grand-pattern-opencl, grand-pattern-ptx, grand-pattern-py, grand-pattern-rs, grand-pattern-sim, grand-pattern-simd, grand-pattern-store, grand-pattern-swift, grand-pattern-topology, grand-pattern-ts, grand-pattern-venue, grand-pattern-wasm, grand-pattern-zig

- **Estimated difficulty:** Medium (different languages, but clear modular structure)
- **Priority:** 🔴 **HIGH** — 41 repos with identical domain, many are language ports of the same algorithm
- **Benefits:**
  - Cross-language consistency is enforced by co-location
  - `grand-pattern-bench` can compare implementations in-tree
  - Eliminates 40 repos
  - FFI bindings stay in sync with their sources

---

## Cluster 3: `ternary-*` Ecosystem → 5-7 Domain Workspaces

**Current state:** 370 repos  
**Proposed merged repos:** 5-7 domain-specific Rust workspaces

### Proposed sub-consolididation

| Workspace | ~Repos | Includes |
|-----------|--------|----------|
| `ternary-ml` | ~40 | tnn, attention, activation, grad, distill, llm, checkpoint, dropout, loss, conv, pool, quantize, fuse, matmul, tensor, transformer, prune, classifier, knn, svm, pca, trees, logistic, regression, norm, optimizer, bayesian, belief, markov, hmm, viterbi, baum-welch, kalman, reservoir, som, entropy, mutual-info, sampling |
| `ternary-gpu` | ~30 | cuda-kernels, cuda-kernels-v2, pack, dispatch, register-file, warp-block, thread-block, shared-memory, texture-memory, surface-memory, constant-cache, grid-launch, kernel-launch, backpressure, gc, lattice-gc, memory-pool, stream-queue, event-pool, command-buffer, priority-queue, rate-limiter, semaphore, shard, shard-merge, shard-split, intent-cache, sketch, pheromone-market |
| `ternary-distributed` | ~35 | consensus, paxos, lease, mirror, version, reassembly, antidote, bloom-filter, cache, database, archive, routing, route, sync, speculate, quorum, retry, lock, locks, reassembly, version, room, bus, channel, event, event-pool, protocol, protocol-python, beacon, captain, navigator, helm, anchor, fleet, fleet-integration, fleet-packing |
| `ternary-math` | ~30 | ising, quantum, hamiltonian, gauge-theory, electromagnetism, lattice, ring, field, geometry, spatial, crystal, homology, topology, sheaf, knot, gauge, sandpile, percolate, percolation, morph, morphogenesis, noether, renormalization, renormalize, chaos, vortex, spiral, kuramoto, haar, walsh |
| `ternary-music` | ~20 | music, jam, harmonic, tempo, rhythm, timbre, wave, counterpoint, polyrhythm, crossfader, envelope, grain, mixer, cadence, form, needledrop, temperament, ear, ear-training, muse |
| `ternary-agent` | ~35 | agent, captain, navigator, helm, anchor, beacon, ensign, steward, lighthouse, observatory, oracle, planet, platoon, constellation, dockyard, foundry, shipyard, tidepool, tenforward, reef, symbiont, harbor, cartograph, compass, pilgrim, voyage, grace, forgiveness, trust, negotiate, chronicle, story |
| `ternary-tooling` | ~10 | cli, compiler, compiler-v2, compiler-optimizer, auto-vectorizer, interpreter, cookbook, manifesto, science, types |

**~30-40 remaining ternary repos** (each unique enough to stay standalone: ternary-cell-python, ternary-dissertation-c, ternary-esp32-firmware, ternary-fitness-c, ternary-fitness-python, ternary-inference-c, ternary-spreadsheet-c, ternary-spreadsheet-python, ternary-dynamics-python, ternary-compiler-python, ternary-protocol-python, ternary-science, etc.)

- **Estimated difficulty:** Hard (370 repos, but Cargo workspace + feature flags can manage it)
- **Priority:** 🔴 **HIGH** — largest single-prefix cluster
- **Benefits:**
  - 370 → 7 repos (363 eliminated)
  - Cross-crate integration testing in one `cargo test` run
  - Unified versioning and changelog
  - `ternary-benchmark` and `ternary-cookbook` naturally belong in the workspace

---

## Cluster 4: `plato-tile-*` Stubs → `plato-tile-suite`

**Current state:** 36 repos (21 are stubs with <120 bytes, 15 have moderate docs)  
**Proposed merged repo:** `plato-tile-suite` (Python package with submodules)

### Repos to merge
plato-tile-api, plato-tile-batch, plato-tile-bridge, plato-tile-cache, plato-tile-cascade, plato-tile-client, plato-tile-current, plato-tile-dedup, plato-tile-encoder, plato-tile-export, plato-tile-feedback, plato-tile-fountain, plato-tile-governance, plato-tile-graph, plato-tile-import, plato-tile-merge, plato-tile-metrics, plato-tile-notifications, plato-tile-pinboard, plato-tile-pipeline, plato-tile-priority, plato-tile-prompt, plato-tile-query, plato-tile-ranker, plato-tile-relation, plato-tile-room-bridge, plato-tile-scorer, plato-tile-search, plato-tile-spec, plato-tile-spec-c, plato-tile-split, plato-tile-store, plato-tile-validate, plato-tile-version, plato-tile-watcher

- **Estimated difficulty:** Easy (most are stubs — just a few lines of Python each)
- **Priority:** 🟡 **MEDIUM** — high count (36) but low individual complexity
- **Benefits:**
  - 36 repos → 1 repo
  - Stubs can grow into proper modules without the overhead of a new repo
  - Shared test infrastructure
  - `plato-tile-spec` + `plato-tile-spec-c` can be the public API

---

## Cluster 5: `plato-room-*` Stubs → `plato-room-suite`

**Current state:** 19 repos (many are stubs with 16-139 bytes)  
**Proposed merged repo:** `plato-room-suite` (Python package)

### Repos to merge
plato-room-acl, plato-room-analytics, plato-room-configs, plato-room-context, plato-room-engine, plato-room-invite, plato-room-memory, plato-room-musician, plato-room-nav, plato-room-persist, plato-room-phi, plato-room-presence, plato-room-runtime, plato-room-scheduler, plato-room-search, plato-room-server, plato-room-wasm, plato-room-webhook

(Note: `plato-room-intelligence` is substantial (3,593 bytes) and could stay standalone or be the anchor)

- **Estimated difficulty:** Easy (most are tiny stubs)
- **Priority:** 🟡 **MEDIUM**
- **Benefits:**
  - 19 → 1 repo
  - Room lifecycle logic finally lives in one place
  - Clear module boundaries instead of repo boundaries

---

## Cluster 6: `flux-*` Core VM Implementations → `flux-monorepo`

**Current state:** 165 repos  
**Proposed merged repo:** `flux-monorepo` (polyglot workspace)

### Sub-clusters within FLUX

| Sub-cluster | ~Repos | Consolidation |
|-------------|--------|---------------|
| Core VMs (Python/Rust/C/Zig/JS/Go/Java/PHP/TS) | 19 | → `flux-monorepo/vms/` |
| Constraint/Safety engines | 11 | → `flux-monorepo/constraint/` |
| Testing/Profiling tools | 10 | → `flux-monorepo/tools/` |
| Legacy language ports (COBOL/Fortran/ALGOL/MUMPS/SNOBOL/PL/I/RPG) | 9 | → `flux-monorepo/legacy/` |
| Natural language runtimes (San/Deu/Lat/Wen/Kor/Zho) | 6 | → `flux-monorepo/natlang/` |
| Agent coordination | 14 | → `flux-monorepo/coordination/` |
| Math/Music/Algebra | 12 | → `flux-monorepo/math/` |
| Docs/Research | 8 | → `flux-monorepo/docs/` |
| Stdlib/Knowledge | 8 | → `flux-monorepo/stdlib/` |
| Toolchain (compiler/linker/optimizer/repl/ide) | 12 | → `flux-monorepo/toolchain/` |
| Preserved artifacts (0-byte READMEs) | 10 | → Delete or archive |
| Auto-generated agent vessels | 4 | → Delete or archive |
| Archived | 3 | → Delete |

- **Estimated difficulty:** Hard (multiple languages, but the domains are tightly coupled)
- **Priority:** 🟡 **MEDIUM** — 165 repos is huge but FLUX has more unique code per repo than ternary
- **Benefits:**
  - 165 → 1 repo (plus archived/deleted)
  - ISA spec (`flux-spec`) lives next to its implementations
  - Cross-VM validation (`flux-validator`) runs against all implementations in-tree
  - Benchmark suite (`flux-benchmarks`) integrated

---

## Cluster 7: `Equipment-*` TypeScript Suite → `equipment-suite`

**Current state:** 14 repos  
**Proposed merged repo:** `equipment-suite` (TypeScript monorepo with workspaces)

### Repos to merge
Equipment-CellLogic-Distiller, Equipment-Consensus-Engine, Equipment-Consensus-Engine-PHP, Equipment-Consensus-Engine-Ruby, Equipment-Context-Handoff, Equipment-Escalation-Router, Equipment-Hardware-Scaler, Equipment-Memory-Hierarchy, Equipment-Monitoring-Dashboard, Equipment-NLP-Explainer, Equipment-Self-Improvement, Equipment-Swarm-Coordinator, Equipment-Swarm-Coordinator-Ruby, Equipment-Teacher-Student

- **Estimated difficulty:** Easy (all TypeScript, same domain, clear modular structure)
- **Priority:** 🟡 **MEDIUM**
- **Benefits:**
  - 14 → 1 repo
  - Shared types and interfaces
  - npm workspace for dependency management
  - PHP/Ruby ports can live in `/ports/` subdirectory

---

## Cluster 8: `eisenstein-*` Hexagonal Math → `eisenstein`

**Current state:** ~18 repos  
**Proposed merged repo:** `eisenstein` (polyglot library)

### Repos to merge
eisenstein (core Rust), eisenstein-c, eisenstein-cuda, eisenstein-do178c, eisenstein-embed, eisenstein-fuzz, eisenstein-quantize, eisenstein-snap-python, eisenstein-tools, eisenstein-triples, eisenstein-vs-z2, eisenstein-vs-z2-c, eisenstein-vs-z2-rs, eisenstein-wasm, eisenstein-bench, eisenstein-ai-landing, eisenstein-do178c

Plus related: arm-neon-eisenstein-bench, hexgrid-gen, hex-lattice-explorer

- **Estimated difficulty:** Easy (well-scoped domain, clear language ports)
- **Priority:** 🟡 **MEDIUM**
- **Benefits:**
  - 18 → 1 repo
  - Fuzzing + benchmarks + implementations co-located
  - DO-178C certification evidence package stays with the code it certifies

---

## Cluster 9: `forge-*` Tile Decomposition → `forge-suite`

**Current state:** 20 repos  
**Proposed merged repo:** `forge-suite` (Rust workspace)

### Repos to merge
forge-a2a, forge-audio, forge-cli, forge-code, forge-code-archaeologist, forge-conservation, forge-data, forge-detect, forge-flux, forge-image, forge-memory, forge-meta, forge-pi, forge-pipeline, forge-sensor, forge-soniqo, forge-subtitle, forge-text, forge-tick, forge-transform

- **Estimated difficulty:** Easy (all Rust, same domain — "decompose X into tiles for Plato agents")
- **Priority:** 🟡 **MEDIUM**
- **Benefits:**
  - 20 → 1 repo
  - New decomposers (forge-video, forge-pdf) can be added as modules
  - `forge-meta` (registry) and `forge-cli` naturally belong together
  - `forge-detect` (format detection) feeds into the right decomposer in-tree

---

## Cluster 10: `exocortex-*` Multi-Language Ports → `exocortex`

**Current state:** 11 repos  
**Proposed merged repo:** `exocortex` (polyglot monorepo)

### Repos to merge
exocortex (Python core), exocortex-ast-cpp, exocortex-clients, exocortex-embed-mojo, exocortex-esp32, exocortex-fleet-chapel, exocortex-kernel-c, exocortex-mcp-ts, exocortex-memory-zig, exocortex-script-lua, exocortex-tiny-py, exocortex-wasm-runtime

Plus related: ExocortexTDA.jl

- **Estimated difficulty:** Medium (multiple languages, but each is a binding/port of the same API)
- **Priority:** 🟡 **MEDIUM**
- **Benefits:**
  - 12 → 1 repo
  - Protocol changes propagate to all bindings automatically
  - ESP32/WASM/Zig ports are clearly thin wrappers over the same concepts

---

## Cluster 11: `graph-*` Algorithm Libraries → `graph-suite`

**Current state:** ~18 repos  
**Proposed merged repo:** `graph-suite` (Rust workspace)

### Repos to merge
graph-algorithms, graph-centrality, graph-coloring, graph-coloring-rs, graph-flow, graph-homology, graph-neural, graph-planarity, graph-search-rs, graph-spectral, graph-thermodynamics, graph-walker-go

Plus closely related: graph-coloring (dedup with graph-coloring-rs)

- **Estimated difficulty:** Easy (all Rust, standard algorithm library consolidation)
- **Priority:** 🟢 **LOW** — smaller cluster, but still worthwhile
- **Benefits:**
  - 12 → 1 repo
  - Many of these share underlying data structures
  - Graph coloring appears twice (dedup opportunity)

---

## Cluster 12: `compress-*` / `compression-*` Libraries → `compress-suite`

**Current state:** ~8 repos  
**Proposed merged repo:** `compress-suite` (Rust workspace)

### Repos to merge
compress-rs, compress-trie-rs, compress-bwt-rs, compress-huffman-rs, compress-lz77-rs, compress-rle-rs, compression-algorithms, bwt-compress

- **Estimated difficulty:** Easy
- **Priority:** 🟢 **LOW**
- **Benefits:**
  - 8 → 1 repo
  - These are clearly modules of the same compression library
  - Shared benchmark suite

---

## Cluster 13: `*-early-version` Archived Repos → Bulk Archive/Delete

**Current state:** ~15+ repos explicitly marked `[ARCHIVED]`  
**Proposed action:** Move to a single `archive` repo or delete

### Repos
plato-alignments-early-version, plato-calibration-early-version, plato-hologram-early-version, plato-stable-early-version, adaptive-plato-early-version, attention-daemon-early-version, field-evolution-early-version, gatekeeper-as-flux-early-version, greenhorn-runtime-early-version, keel-early-version, flux-consciousness-engine-early-version, flux-engine-early-version, flux-constraint-py-early-version

Plus ~10 `flux-*` preserved artifacts (0-byte READMEs) and various `preserved workspace artifact` repos.

- **Estimated difficulty:** Trivial
- **Priority:** 🟢 **LOW** — housekeeping
- **Benefits:**
  - Removes ~25 repos of zero-content noise
  - Cleaner org page

---

## Summary Impact Table

| Cluster | Current Repos | After Consolidation | Eliminated | Difficulty | Priority |
|---------|--------------|--------------------|------------|------------|----------| 
| `lau-*` → `lau-workspace` | 333 | 1 | 332 | Medium | 🔴 HIGH |
| `ternary-*` → 7 workspaces | 370 | 7 | 363 | Hard | 🔴 HIGH |
| `grand-pattern-*` → `grand-pattern` | 41 | 1 | 40 | Medium | 🔴 HIGH |
| `plato-tile-*` → `plato-tile-suite` | 36 | 1 | 35 | Easy | 🟡 MEDIUM |
| `flux-*` → `flux-monorepo` | 165 | 1 | 164 | Hard | 🟡 MEDIUM |
| `plato-room-*` → `plato-room-suite` | 19 | 1 | 18 | Easy | 🟡 MEDIUM |
| `Equipment-*` → `equipment-suite` | 14 | 1 | 13 | Easy | 🟡 MEDIUM |
| `forge-*` → `forge-suite` | 20 | 1 | 19 | Easy | 🟡 MEDIUM |
| `eisenstein-*` → `eisenstein` | 18 | 1 | 17 | Easy | 🟡 MEDIUM |
| `exocortex-*` → `exocortex` | 12 | 1 | 11 | Medium | 🟡 MEDIUM |
| `graph-*` → `graph-suite` | 12 | 1 | 11 | Easy | 🟢 LOW |
| `compress-*` → `compress-suite` | 8 | 1 | 7 | Easy | 🟢 LOW |
| Archived/early-version cleanup | ~25 | 0 | 25 | Trivial | 🟢 LOW |
| **TOTAL** | **~1,073** | **~18** | **~1,055** | | |

---

## Recommended Execution Order

1. **Phase 1 — Quick wins (Easy, High impact):**
   - Delete/archive `*-early-version` and preserved artifacts (25 repos, 0 effort)
   - Consolidate `plato-tile-*` stubs into `plato-tile-suite` (36→1)
   - Consolidate `plato-room-*` stubs into `plato-room-suite` (19→1)
   - Consolidate `Equipment-*` into `equipment-suite` (14→1)

2. **Phase 2 — Medium consolidations:**
   - Merge `forge-*` into `forge-suite` (20→1)
   - Merge `eisenstein-*` into `eisenstein` (18→1)
   - Merge `compress-*` into `compress-suite` (8→1)
   - Merge `exocortex-*` into `exocortex` (12→1)
   - Merge `graph-*` into `graph-suite` (12→1)

3. **Phase 3 — Major restructuring:**
   - Consolidate `grand-pattern-*` into polyglot monorepo (41→1)
   - Consolidate `lau-*` into Rust workspace (333→1)
   - Break `ternary-*` into 7 domain workspaces (370→7)

4. **Phase 4 — Largest effort:**
   - Consolidate `flux-*` into polyglot monorepo (165→1)

---

## Key Risks & Mitigations

| Risk | Mitigation |
|------|------------|
| Breaking external dependencies on existing repos | Use GitHub's archive + redirect; old repos become read-only with pointer to new location |
| Loss of git history granularity | Use `git subtree` or `git-filter-repo` to preserve individual histories as subdirectories |
| Large monorepos become slow | Cargo workspaces and npm workspaces handle this well; only Rust + TS are affected |
| Cross-language repos confuse CI | Use path-triggered CI (only run Rust tests when `/rust/` changes) |
| Some repos have stars/contributors | Check each before merging; preserve issues and wiki pages |

---

## Methodology

This plan was derived from analysis of the INDEX-*.md files covering all 3,327 repos:
- `INDEX-ternary.md` — 370 ternary-* repos
- `INDEX-flux.md` — 165 flux-* repos  
- `INDEX-plato.md` — 262 plato-* repos
- `INDEX-other-aa.md` through `INDEX-other-af.md` — ~2,530 remaining repos

Clusters were identified by shared prefix, domain overlap, identical language/patterns, and cross-references in README documentation. The `lau-*` cluster (333 repos) is the single largest consolidation opportunity, followed by `ternary-*` (370 repos, split into 7 workspaces) and `flux-*` (165 repos).
