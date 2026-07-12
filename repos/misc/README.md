# Miscellaneous Repos

This is the catchall category for SuperInstance repos that don't fit neatly into the primary thematic clusters. With ~1,200 repos, it's the largest category — but it contains genuine gems alongside experiments and one-offs.

---

## Sub-Categories

### Rust Crates (~126 repos)
Standalone Rust libraries implementing data structures, algorithms, and utilities.
**Key repos:** `treap-rs`, `convex-hull-rs`, `aho-corasick-rs`, `young-tableau-rs`, `async-rs`, `actor-rs`, `allocator-rs`, `event-bus-rs`
**Assessment:** Mix of real implementations and exercises. Several are publishable with polish.

### Mathematics & Algorithms (~50 repos)
Pure math implementations spanning algebra, analysis, geometry, and numerical methods.
**Key repos:** `wasserstein-agents-rs` (optimal transport for agents), `ode-solver` (differential equations), `pythagorean-quantize`, `lotka-volterra-agents-c` (predator-prey dynamics), `approximation-theory`, `representation-theory`, `normal-form`, `interp-spline`
**Assessment:** Research-grade code, often tied to the LAU/constraint ecosystem but standalone enough to warrant separate repos.

### Agent & AI Research (~30 repos)
Agent architectures, cognitive models, and AI research code that doesn't fit under agent-framework or fleet-infra.
**Key repos:** `SwarmOrchestration`, `attention-economy`, `narrative-field`, `ability-transfer`, `ant-colony`, `anomaly-atlas`
**Assessment:** Experimental. Ideas more than products.

### Web & AI Pages (~13 repos)
GitHub Pages sites and web interfaces for various SuperInstance sub-projects.
**Key repos:** `*-ai-pages` (personallog, activelog, activeledger, businesslog), `iching-web`, `SuperInstance-papers`

### SuperInstance Papers & Writing (~10 repos)
Essays, white papers, and creative writing from the project.
**Key repos:** `SuperInstance-papers`, `AI-Writings`, `FORGE-FLUX-ECOSYSTEM`, `abstraction-planes`

### Systems & Infrastructure (~20 repos)
Core infrastructure components — event buses, API gateways, allocators, etc.
**Key repos:** `field-core`, `pincher`, `api-gateway`, `event-bus`, `api-doc-generator`, `actualize`, `actualization-harbor`

### Physics & Chemistry (~15 repos)
Computational physics and chemistry implementations.
**Key repos:** `arm-neon-eisenstein-bench`, `amd-bf16-tools`, `async-gpu-dispatch`

### Miscellaneous Utilities (~40 repos)
One-off tools, scripts, and experiments.
**Key repos:** `seed-tick-audit`, `experiments`, `integration_tests`, `mud-solitaire`, `casting-call`, `archive`, `archives`

### Unclassified (~900 repos)
The long tail. Many are small experiments, auto-generated stubs, or AI-assisted prototypes. Use the individual `.md` files to explore.

---

## How to Explore

1. **Looking for Rust crates?** → Filter for `*-rs.md` files
2. **Looking for math?** → Search for algebra, geometry, topology keywords
3. **Looking for production code?** → Cross-reference with `../../docs/03-production-audit/PRODUCTION-AUDIT.md`
4. **Looking for something specific?** → Use `grep -ri "keyword" *.md` in this directory

## Quality Note

This category has the highest concentration of stubs and auto-generated repos in the ecosystem. Roughly:
- ~200 are genuine small projects
- ~400 are moderate AI-assisted prototypes
- ~400 are stubs or minimal experiments
- ~200 have no README

See individual `.md` files for per-repo assessments.
