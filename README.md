# SuperInstance Repository Documentation

> **4,098 repos analyzed. 3,327 original. 25+ languages. One ecosystem.**

This repository is the comprehensive, honest documentation of every repo in the [SuperInstance GitHub organization](https://github.com/SuperInstance). It was produced by an automated deep-audit of all repos — fetching READMEs, analyzing code structure, running tests where possible, and writing honest assessments.

---

## What Is SuperInstance?

SuperInstance is a large-scale AI-agent ecosystem built by [Casey](https://github.com/SuperInstance). It spans distributed agent coordination, ternary mathematics, bytecode virtual machines, edge/embedded computing, marine instrumentation, spectral music theory, and more.

The org contains **4,098 repositories** — 3,327 original, 771 forks. The dominant language is Rust (1,200+ repos), followed by Python (800+), TypeScript (300+), C (150+), and CUDA (80+).

### Core Philosophy

The ecosystem is built on several novel ideas:

- **Conservation Laws** — The equation **γ + η = C** (tension + entropy = constant) appears as a governance principle across the codebase, enforced in CI/CD
- **Ternary Logic** — Balanced ternary **{-1, 0, +1}** as a mathematical foundation for computation, routing, and decision-making
- **PLATO Rooms** — Knowledge organized into discrete "rooms" with tile-based lifecycles and simulation-first design
- **FLUX Bytecode** — A deterministic ISA for agentic logic with implementations in Python, Rust, JS, C, and Zig
- **Deadband Protocol** — Signal-chain architecture from sensor → deadband → nano-model → LoRA → fleet → cloud
- **Fleet Orchestration** — Git-native multi-agent coordination using commits, branches, tags, and notes instead of databases

---

## Repository Structure

```
repo-docs/
│
├── README.md                          ← You are here
├── LICENSE                            ← MIT
│
├── docs/                              ← Analysis & meta-documentation
│   ├── 01-overview/                   ← Master index, ecosystem analysis, unified wiki
│   │   ├── MASTER-INDEX.md            ← Top-level index of all repos by cluster
│   │   ├── ECOSYSTEM-ANALYSIS.md      ← Big-picture analysis & maturity matrix
│   │   ├── UNIFIED-WIKI.md            ← Consolidated wiki (replaces 4 stale wikis)
│   │   └── WIKI-MIGRATION-PLAN.md     ← How to archive old wikis
│   │
│   ├── 02-architecture/               ← Architectural analysis
│   │   └── CONSOLIDATION-PLAN.md      ← Which repos should merge
│   │
│   ├── 03-production-audit/           ← Tier-ranked readiness assessment
│   │   ├── PRODUCTION-AUDIT.md        ← Full audit of 40 top repos
│   │   └── audit-*.md (19)            ← Individual deep audits
│   │
│   └── 04-shipping-log/              ← What's been hardened & shipped
│       └── SHIPPED-*.md (6)           ← Per-repo shipping reports
│
└── repos/                             ← Individual repo documentation
    ├── README.md                      ← Guide to all categories
    │
    ├── ternary-math/     (371)        ← {-1, 0, +1} computing ecosystem
    ├── plato-system/     (264)        ← PLATO knowledge rooms & runtime
    ├── flux-bytecode/    (166)        ← Deterministic agentic bytecode VM
    ├── fleet-infra/      (266)        ← Agent fleet orchestration
    ├── lau-mathematics/  (409)        ← Lie algebra, Hodge theory, graphs
    ├── constraint-theory/ (46)        ← CSP, Hamiltonian, Lama rigidity
    ├── conservation-laws/ (59)        ← γ+η=C governance, multilingual
    ├── music-spectral/    (31)        ← Spectral music theory in Rust
    ├── edge-embedded/     (59)        ← ESP32, Jetson, ARM, vessel bridge
    ├── a2a-a2ui/           (8)        ← Agent-to-agent & agent-to-UI protocols
    ├── oxide-gpu/         (42)        ← Distributed GPU compute stack
    ├── superinstance-core/ (51)       ← Core org tooling & infrastructure
    ├── cocapn-marine/     (11)        ← Marine sensors, NMEA, autopilot
    ├── agent-framework/    (9)        ← Git-native agent frameworks
    ├── exocortex-memory/  (11)        ← Persistent cognitive substrate
    ├── persona-ai/        (11)        ← Persona engine & character SDK
    ├── roblox-gaming/     (11)        ← Roblox/Luau agent frameworks
    ├── dev-tools/         (16)        ← Snapkit, testing, API tools
    ├── forge-tiles/       (39)        ← Forge pattern & tile decomposition
    ├── sheaf-topology/    (19)        ← Sheaf theory & topology for agents
    ├── entropy-physics/   (35)        ← Thermodynamic & symplectic computing
    ├── activelog/         (11)        ← Activity logging & tracking
    ├── equipment-catalog/ (14)        ← Edge equipment taxonomy
    ├── openconstruct/      (6)        ← OpenConstruct embedded clients
    ├── zeroclaw/          (21)        ← ZeroClaw nightly experiments
    └── misc/            (1200)        ← Everything else (algorithms, tools, experiments)
```

---

## Key Findings

### Tier 1: Ship-Ready Repos

These repos have real tests, working CI, proper packaging, and functional code:

| Repo | Language | Tests | Description |
|------|----------|-------|-------------|
| **flux-runtime** | Python | 54 files | Deterministic bytecode ISA VM — assembler, compiler, debugger |
| **flux-core** | Rust | 54 tests | Rust FLUX bytecode runtime with criterion benchmarks |
| **plato-server** | Python | 2 suites | Standalone PLATO knowledge server (SQLite + HTTP) |
| **plato-engine-block-c** | C | 3 suites | Zero-malloc embedded sensor→alarm engine (C99) |
| **git-agent** | Python | 234 tests | Repo-native agent — your repo IS your brain |
| **plato-runtime-kernel** | Rust | 42 tests | Conservation-verified AI computation kernel |

### Tier 2: Near-Ready (13 repos)

flux-vm, flux-compiler, plato-engine-block-elixir, categorical-agents, construct-core, flux-js, plato-core, plato-audio-jepa, plato-vision-jepa, plato-engine-block-zig, ternary-compiler-v2, plato-torch, exocortex

See `docs/03-production-audit/PRODUCTION-AUDIT.md` for the full breakdown.

### Quality Distribution

| Quality | Count | Description |
|---------|-------|-------------|
| Substantial | ~800 | Rich docs, real architecture (README > 2KB) |
| Real Project | ~400 | Working code, examples, tests |
| Moderate | ~600 | Some substance, AI-assisted |
| Lightweight | ~500 | Brief docs, small utility |
| Stub | ~200 | Minimal, placeholder |
| Auto-generated | ~200 | Template, fleet branding |
| No README | ~200 | No documentation available |

### Stale Wiki Repos

These 4 repos are stale and superseded by this documentation:

1. `superinstance-wiki` — Original wiki, archived
2. `wiki` — General wiki placeholder
3. `knowledge-agent` — Early knowledge management experiment
4. `fleet-wiki` — Fleet documentation wiki

**Replacement:** See `docs/01-overview/UNIFIED-WIKI.md`

---

## How to Use This Repo

### "I want to understand the SuperInstance ecosystem"
→ Start with `docs/01-overview/ECOSYSTEM-ANALYSIS.md`

### "I want to find production-ready repos to use"
→ Check `docs/03-production-audit/PRODUCTION-AUDIT.md`

### "I want to explore a specific area"
→ Browse `repos/<category>/README.md` for that category

### "I want to understand a specific repo"
→ Find its `.md` file in the appropriate `repos/` subdirectory

### "I want to know what should be consolidated"
→ Read `docs/02-architecture/CONSOLIDATION-PLAN.md`

### "I want to see what's been shipped/hardened"
→ Check `docs/04-shipping-log/`

---

## Stats

| Metric | Value |
|--------|-------|
| Total repos analyzed | 4,098 |
| Original (non-fork) repos | 3,327 |
| Documentation files | 3,200+ |
| Major category clusters | 27 |
| Tier 1 (ship-ready) repos | 6 |
| Tier 2 (near-ready) repos | 13 |
| Languages documented | 25+ |
| AI tools used | OpenClaw, Claude Code, Kimi, Crush, OpenCode |

---

## License

MIT — see [LICENSE](LICENSE)

---

*Generated 2026-07-12 by OpenClaw with assistance from Claude Code, Kimi, Crush, and OpenCode.*
