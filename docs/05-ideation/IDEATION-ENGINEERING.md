# SuperInstance Engineering Ideation — Next 30/60/90 Days

**Generated:** 2026-07-12  
**Author:** Technical Architecture (OpenClaw)  
**Inputs:** Production Audit (40 repos), Consolidation Plan (3,327 repos), Shipping Log (9 shipped, 13 polished, license sweep done)  
**Status:** Draft for review  

---

## Current Position

**Shipped and hardened:** 9 repos (flux-runtime, flux-core, plato-server, plato-engine-block-c, plato-runtime-kernel, git-agent, capitaine-1, codespace-edge-rd, git-agent-codespace).  
**Polished but not shipped:** 13 repos (categorical-agents, construct-core, crab, cuda-constraint-engine, exocortex, flux-compiler, flux-vm, grand-pattern-rs, lau-hodge-theory, plato-engine-block-elixir, plato-engine-block, ternary-science).  
**Registry blockers identified:** `flux-runtime` taken on PyPI → use `flux-vm`; `flux-core` taken on crates.io → use `fluxvm`; `flux-js` available on npm.  
**Org sprawl:** 4,098 repos, ~326 still unlicensed, 12 consolidation clusters identified covering ~750+ repos.

The foundation is laid. The next 90 days turn this from a hardened codebase into a visible, adoptable ecosystem.

---

## 30-Day Sprint (Quick Wins)

*Each item: 1-5 days of effort. High signal, low risk.*

---

### S1. Publish `flux-vm` to PyPI

**What:** Rename distribution from `flux-runtime` to `flux-vm` in pyproject.toml, add email + license-files, build, and publish to PyPI. Set up GitHub Actions trusted publishing (OIDC) so releases auto-publish.

**Why:** The flagship Python project has zero runtime dependencies, 54 test files, and professional packaging — but nobody can `pip install` it. This is the single highest-leverage adoption unlock.

**Repos:** `flux-runtime`  
**Effort:** 1 day  
**Dependencies:** PyPI account creation, name decision (`flux-vm` recommended and confirmed free)  
**Success metric:** `pip install flux-vm` works; `flux --help` prints the CLI banner; 10+ downloads in first week  

---

### S2. Publish `fluxvm` to crates.io

**What:** Rename crate from `flux-core` to `fluxvm` in Cargo.toml, verify `cargo publish --dry-run`, publish to crates.io. Wire up the existing `publish.yml` workflow with a `CARGO_REGISTRY_TOKEN` secret.

**Why:** The Rust implementation has 40 tests, criterion benchmarks, LTO-optimized release profile, and zero external deps beyond `regex`. docs.rs will auto-generate API documentation on publish. This gives the project a professional Rust crate presence.

**Repos:** `flux-core`  
**Effort:** 1 day  
**Dependencies:** crates.io account, API token with `publish-new` scope  
**Success metric:** `cargo add fluxvm` works; docs.rs/fluxvm renders API docs; 10+ downloads in first week  

---

### S3. Publish `flux-js` to npm

**What:** Add missing metadata to package.json (license, author, repository, keywords, files, `type: module`), bump version from `1.0.0` to `0.1.0`, create npm org `superinstance`, publish as `@superinstance/flux` (scoped) or `flux-js` (unscoped).

**Why:** The 21KB single-file JS VM runs in browsers and Node.js. It's the most accessible entry point to FLUX for the largest developer demographic. Publishing takes the codebase from "clone to use" to "npm install to use."

**Repos:** `flux-js`  
**Effort:** 0.5 day  
**Dependencies:** npm account, org creation  
**Success metric:** `npm install @superinstance/flux` works; unpkg/CDN serves the file; 25+ weekly downloads within month  

---

### S4. Fleet-Wide CI Hardening Sweep

**What:** Systematically visit every Tier 2 and Tier 3 repo. Remove all `|| true` patterns. Replace stub CIs (`echo "No CI configured"`) with real build-and-test pipelines. Add CI to repos missing it entirely (`plato-engine-block-elixir`, `plato-engine-block-zig`). Standardize on a 3-job pattern per language: lint, test, build.

**Why:** The audit found CI theater across the org — workflows that are green regardless of test results. This is a credibility killer. No external contributor will trust a repo whose CI doesn't gate.

**Repos (priority order):** `plato-engine-block-elixir`, `plato-engine-block-zig`, `flux-vm` (Rust, wrong CI type), `flux-compiler`, `plato-core`, `plato-audio-jepa`, `plato-vision-jepa`, `exocortex`, `plato-torch`  
**Effort:** 3-4 days (batchable — write a CI template per language, apply mechanically)  
**Dependencies:** None  
**Success metric:** All Tier 1 + Tier 2 repos have CI that fails on test failures; zero `|| true` instances remain in any workflow file  

---

### S5. License the Remaining 326 Repos

**What:** Reuse the license-fix script from the first sweep. Batch-clone all unlicensed repos, detect language, add MIT LICENSE + `.gitignore` + config-file license field. Push. The script at `/tmp/fix-license.sh` already exists from the prior sweep.

**Why:** 326 repos with no license means 326 repos that are legally unusable. This is a one-afternoon mechanical task that converts the org from "legally ambiguous" to "MIT-licensed ecosystem."

**Repos:** ~326 remaining unlicensed repos across the org  
**Effort:** 1 day  
**Dependencies:** None (script exists)  
**Success metric:** `gh api /orgs/SuperInstance/repos --paginate | jq '.[].license' | grep -c null` returns 0  

---

### S6. Publish `plato-server` to PyPI

**What:** Rename to `plato-knowledge` (or `plato-server`) on PyPI, verify the fixed entry point (`plato-server = "server:main"`), add PyPI metadata, publish. The server is pure stdlib Python, zero runtime dependencies — ideal for distribution.

**Why:** plato-server is a working HTTP knowledge system that runs with `python -m plato-server`. It's the most immediately useful non-FLUX project. Publishing it gives the ecosystem breadth beyond bytecode VMs.

**Repos:** `plato-server`  
**Effort:** 0.5 day  
**Dependencies:** PyPI account (shared with S1)  
**Success metric:** `pip install plato-server && plato-server` starts an HTTP server on port 8847  

---

### S7. Cross-Language FLUX Conformance Suite

**What:** Create a `flux-conformance` repo containing a JSON/YAML suite of ~50 bytecode programs with expected VM outputs. Each implementation (Python, Rust, JS) runs the suite in CI and reports pass/fail. This is the "Test262" for FLUX.

**Why:** Three implementations exist (Python, Rust, JS) but there's no guarantee they agree on behavior. A shared conformance suite ensures that bytecode valid in one runtime works in all three. It also serves as executable documentation.

**Repos:** New repo `flux-conformance`  
**Effort:** 2-3 days  
**Dependencies:** S1, S2, S3 (published packages make CI setup cleaner)  
**Success metric:** All three runtimes pass 100% of conformance tests; at least one cross-implementation bug discovered and fixed  

---

### S8. Demo: FLUX Agent in a README Animation

**What:** Create a `flux-demos` repo with 3-5 animated/recorded demos: (1) assemble + run a bytecode program, (2) A2A agent conversation, (3) fleet simulation, (4) debugger session, (5) cross-runtime interop (Python↔Rust↔JS). Record with `asciinema` and embed in README files.

**Why:** The FLUX ecosystem has impressive depth (assembler, VM, A2A, debugger, fleet sim) but zero visual demonstration. Developers judge projects by their READMEs. An asciinema cast is the fastest way to communicate "this actually works."

**Repos:** New repo `flux-demos`  
**Effort:** 2 days  
**Dependencies:** S1, S2, S3 (install from registries, not clone)  
**Success metric:** Demos embedded in all 3 main repo READMEs; social-media-shareable; external developer says "I want to try this"  

---

### S9. Ship Tier 2 Polish Batch (3-5 repos)

**What:** Apply the same production-hardening playbook used on Tier 1 to the most promising Tier 2 repos. Priority candidates: `flux-js` (already analyzed), `categorical-agents` (31 tests, category theory for agents), `construct-core` (32 tests, hardware-agnostic agent runtime). Each gets: CI fix, license verification, packaging metadata, README polish.

**Why:** Tier 1 is shipped. Tier 2 has repos with real tests and real ideas that are 1-2 days of polish away from ship-ready. Converting 3-5 of them multiplies the ecosystem surface area.

**Repos:** `flux-js`, `categorical-agents`, `construct-core`, `plato-engine-block-elixir`  
**Effort:** 4-5 days (1-1.5 days per repo)  
**Dependencies:** None  
**Success metric:** 4 more repos with passing CI, proper packaging, and shipped status  

---

### S10. Unified CONTRIBUTING.md + Ecosystem README

**What:** Write a top-level SuperInstance organization README and CONTRIBUTING.md that covers: what the ecosystem is, how the pieces fit together (FLUX + PLATO + ternary + agents), how to contribute, coding standards, CI requirements, and a repo map. Publish these to a `.github/profile/README.md` (org profile) and a `superinstance-ecosystem` meta-repo.

**Why:** 4,098 repos with no unifying documentation. A newcomer cannot answer "what is SuperInstance?" in under 5 minutes. An org-level README fixes this instantly and serves as the front door.

**Repos:** New repo `superinstance-ecosystem` (or `.github` repo for org profile)  
**Effort:** 1 day  
**Dependencies:** None  
**Success metric:** github.com/SuperInstance shows a populated org profile; contributor docs exist; first external PR within 30 days  

---

## 60-Day Initiatives

*Each item: 1-3 weeks of effort. Builds connectivity between subsystems.*

---

### M1. FLUX↔PLATO Integration Library

**What:** Build `flux-plato-bridge` — a library that lets FLUX bytecode programs read/write PLATO knowledge tiles. FLUX agents can query a PLATO server for context, reason over it, and submit new tiles as knowledge products. This connects the "executable logic" substrate (FLUX) with the "knowledge management" substrate (PLATO).

**Why:** FLUX and PLATO are the two strongest subsystems in the ecosystem, but they don't talk to each other. Connecting them creates a closed loop: agents that can *think* (FLUX) and *remember* (PLATO). This is the technical foundation for the Codespace→Agent→Edge demo (M2) and the fleet dashboard (M4).

**Repos:** New `flux-plato-bridge`, depends on `flux-vm` (PyPI), `plato-server` (PyPI)  
**Effort:** 1-2 weeks  
**Dependencies:** S1, S6 (both must be pip-installable)  
**Success metric:** A FLUX agent program can `LOAD_TILE "room:sensor:temp"`, `SUBMIT_TILE "room:analysis:temp_trend"`, and the PLATO server reflects the changes. Integration tests in CI.  

---

### M2. End-to-End Demo: Codespace → Agent → Edge

**What:** A reproducible, documented demo that takes a git-agent from GitHub Codespace through the yoke transfer protocol to an edge device (Raspberry Pi or Jetson). The agent starts in the Codespace (full compute, LLM access), develops a behavior, crystallizes it into compiled FLUX bytecode, and transfers to the edge device where it runs autonomously with no network connectivity.

**Why:** This is the thesis of the entire ecosystem — that intelligence can flow from cloud to edge through crystallization. `codespace-edge-rd` lays the theoretical groundwork; `git-agent-codespace` provides the devcontainer template; `capitaine-1` has the crystallization curve. The demo proves the thesis end-to-end.

**Repos:** `codespace-edge-rd`, `git-agent-codespace`, `capitaine-1`, `flux-runtime`, `plato-engine-block-c`  
**Effort:** 2-3 weeks  
**Dependencies:** S1 (flux-vm on PyPI), S8 (demo infrastructure), ideally M1 (FLUX↔PLATO bridge for richer agent behavior)  
**Success metric:** A 5-minute screencast: developer opens Codespace → agent learns → `yoke transfer` → Raspberry Pi runs the crystallized agent with LED blink or sensor reading. Blog post with reproduction steps.  

---

### M3. Conservation Law as a GitHub Action

**What:** Package the conservation/symmetry checking logic from the `lau-conservation-*` crates into a reusable GitHub Action: `superinstance/conservation-check`. The action analyzes a PR's diff and verifies that it doesn't violate declared conservation laws (e.g., energy-like invariants, symmetry constraints in the codebase). It posts a check-run with pass/fail.

**Why:** The audit identified 62 tests in `lau-hodge-theory` and a conservation-engine cluster — genuinely novel mathematics. But it's locked in niche Rust crates. A GitHub Action makes the concept accessible to any repo, turns an academic idea into a product, and creates a unique CI differentiator nobody else offers.

**Repos:** `lau-hodge-theory`, `lau-conservation-engine`, `lau-conservation-laws`, new `conservation-action`  
**Effort:** 2 weeks  
**Dependencies:** Consolidation of the conservation crates into one workspace (per Consolidation Plan Cluster 1)  
**Success metric:** Action is on GitHub Marketplace; 5+ external repos install it; at least one user tweets about it  

---

### M4. Fleet Dashboard (Actually Runs)

**What:** Build `fleet-dashboard` — a real-time web dashboard that connects to plato-server instances across multiple "vessels" (repos or physical devices). Shows: agent activity, tile submission rates, sensor readings from engine blocks, FLUX bytecode execution metrics, fleet topology (which agents talk to which). Uses WebSockets for live updates.

**Why:** plato-server has stats endpoints, engine blocks produce sensor data, and capitaine-1 has fleet snapshots — but there's no way to *see* any of it. A dashboard converts abstract infrastructure into a visceral "I can see my fleet" experience. It's also the most compelling demo artifact for investors, collaborators, and adopters.

**Repos:** New `fleet-dashboard` (TypeScript + WebSocket client), `plato-server` (add WebSocket support), `plato-engine-block-c` (add TCP telemetry output)  
**Effort:** 2-3 weeks  
**Dependencies:** S6 (plato-server published), S9 (engine blocks polished)  
**Success metric:** Dashboard runs locally against 3+ plato-server instances; live updates flow; presentable in a 2-minute screen recording  

---

### M5. Cross-Runtime A2A Agent Protocol v1

**What:** Formalize the A2A (agent-to-agent) protocol that exists in flux-runtime, flux-core, and flux-js into a spec document (`flux-a2a-spec`). Define: message envelope format, capability negotiation, transport (WebSocket + HTTP + in-process), security model (capability tokens), and conformance requirements. Build reference implementations in all three runtimes.

**Why:** A2A is mentioned in all three FLUX repos but is likely inconsistent across implementations. A formal spec makes inter-agent communication a first-class product feature. Combined with the conformance suite (S7), this enables polyglot agent fleets — a Python agent talking to a Rust agent talking to a browser-based agent.

**Repos:** `flux-runtime`, `flux-core`, `flux-js`, new `flux-a2a-spec`  
**Effort:** 2 weeks  
**Dependencies:** S7 (conformance suite infrastructure), S1-S3 (published packages)  
**Success metric:** Spec document published; at least 2 reference implementations pass conformance; a Python agent successfully delegates a task to a Rust agent over WebSocket  

---

### M6. Repo Consolidation: `lau-workspace` First Wave

**What:** Execute Cluster 1 from the Consolidation Plan: merge the ~333 `lau-*` repos into a single `lau-workspace` Cargo workspace. Start with the highest-value sub-clusters: conservation (~12 repos), category theory (~10 repos), and agent systems (~25 repos). Preserve git history, redirect old repos, set up CI for the monorepo.

**Why:** 333 repos is the single largest source of org sprawl. Consolidating them into one workspace makes cross-crate refactoring possible (the `lau-glue` crate already bridges 108+ — it shouldn't need to exist). This also makes the math library evaluable as a coherent system rather than scattered fragments.

**Repos:** ~333 `lau-*` repos → `lau-workspace`  
**Effort:** 2-3 weeks (mechanical but voluminous; can be parallelized)  
**Dependencies:** S5 (all repos must have licenses first)  
**Success metric:** `lau-workspace` exists with 300+ crates as workspace members; `cargo test` passes for all; 332 repos archived with redirect notices; org repo count drops by ~300  

---

### M7. `construct-core` Hardware Abstraction Demos

**What:** Build and document real hardware demos for construct-core's layered trait system: Layer 0 (bare-metal on ESP32), Layer 1 (embedded on Raspberry Pi Pico), Layer 2 (full OS on Raspberry Pi 4). Each demo: flash an LED, read a sensor, report to PLATO server. Include wiring diagrams, photos, and build instructions.

**Why:** construct-core has 32 tests and a clean layered architecture for hardware abstraction — but no proof it works on actual hardware. Demos would validate the abstraction and create the most compelling kind of documentation: "here's the code, here's the wire, here's it working."

**Repos:** `construct-core`, new `construct-demos`  
**Effort:** 2-3 weeks (requires physical hardware iteration)  
**Dependencies:** S9 (construct-core polished + shipped), M1 (PLATO bridge for reporting)  
**Success metric:** 3 demos documented and reproducible; photos/video of working hardware; at least one non-SuperInstance person builds a demo  

---

### M8. Developer Documentation Site

**What:** Stand up a MkDocs or Docusaurus site (`docs.superinstance.dev` or similar) covering: FLUX ISA reference, PLATO protocol guide, A2A protocol spec, getting-started tutorials (Python/Rust/JS), architecture overview, and the conservation-law concept. Auto-generate API docs from docstrings (sphinx for Python, rustdoc for Rust, JSDoc for JS).

**Why:** No documentation exists beyond individual repo READMEs. A centralized docs site is the #1 adoption blocker for technical projects — developers need a narrative entry point, not a repo dump. This also forces the team to explain concepts clearly, which improves the code.

**Repos:** New `superinstance-docs`  
**Effort:** 2 weeks  
**Dependencies:** S10 (org README provides outline), S1-S3 (published packages for install instructions), S7 (conformance suite for examples)  
**Success metric:** docs.superinstance.dev is live; getting-started tutorial works for a fresh developer in <15 minutes; 100+ unique visitors in first month  

---

## 90-Day Moonshots

*Each item: 3-6 weeks of effort, high ambition, potentially ecosystem-defining.*

---

### L1. Ternary Computing SDK — Genuinely Useful

**What:** Package the ternary ecosystem (`ternary-compiler-v2`, `ternary-tnn`, `ternary-science`, `plato-engine-block` ternary modules) into a cohesive SDK for balanced ternary {-1, 0, +1} computing. Include: a ternary arithmetic simulator, a ternary neural network training pipeline (using ternary-tnn), a ternary logic simulator, and an emulator for ternary hardware targets. Make it installable: `pip install ternary-sdk`.

**Why:** Ternary computing is a legitimate research frontier (more efficient than binary for certain operations, natural fit for neural networks). The codebase already has a compiler, a neural network implementation, and GPU benchmarks. The problem: it's scattered across 370 repos. An SDK makes it *tryable*. Even if no hardware exists, the simulator + training pipeline is useful for research.

**Repos:** `ternary-compiler-v2`, `ternary-tnn`, `ternary-science`, `plato-engine-block` (ternary modules), `grand-pattern-rs` (Fibonacci architecture), new `ternary-sdk` meta-package  
**Effort:** 4-5 weeks  
**Dependencies:** M6 (lau-workspace consolidation reduces noise), S9 (ternary-compiler-v2 polished)  
**Success metric:** `pip install ternary-sdk && python -c "from ternary import Trit; print(Trit(1) + Trit(-1))"` works; ternary MNIST classifier trains to >95% accuracy in <5 minutes; published to PyPI; referenced in a Hacker News post  

---

### L2. Git-Agent-Codespace as a Product

**What:** Turn `git-agent` + `git-agent-codespace` + `capitaine-1` into a deployable product: a one-click GitHub App that installs on any repo, creates a Codespace with the agent runtime, and starts the heartbeat cycle (detect → perceive → think → act → record). The agent commits to the repo, opens PRs, and learns over time via crystallization. Include a pricing model (free for public repos, paid for private).

**Why:** The git-agent system is already the most "product-shaped" thing in the ecosystem — it has a CLI, a config wizard, multi-provider LLM support, Docker, and a Codespace template. The gap between "clone and configure" and "click and deploy" is a GitHub App. This is the most direct path to commercial validation.

**Repos:** `git-agent`, `git-agent-codespace`, `capitaine-1`, new `git-agent-app` (GitHub App server)  
**Effort:** 4-6 weeks  
**Dependencies:** S1 (flux-vm for agent logic), M2 (end-to-end demo validates the Codespace→Edge thesis), M8 (docs site for onboarding)  
**Success metric:** 10+ external repos install the GitHub App; at least one agent opens a merged PR; product page live with pricing; first paying customer (if private repos)  

---

### L3. Marine Vessel Monitoring — Commercial Pilot

**What:** Deploy `plato-engine-block-c` (C99 embedded engine) and `plato-engine-block-elixir` (BEAM/OTP fleet coordinator) in a real-world marine monitoring scenario: instrument a vessel (or simulate one convincingly) with sensors for temperature, humidity, vibration, and GPS. Data flows: sensor → engine block (C) → PLATO server → fleet coordinator (Elixir) → dashboard (from M4). Include alarms, history, and fleet coordination.

**Why:** The engine blocks were *designed* for marine vessel monitoring — it's in the READMEs. The Elixir version has supervisor trees and fault tolerance, the C version has zero dynamic allocation. This is a vertical slice of the entire ecosystem deployed in a domain where the requirements match the architecture. A successful pilot proves the tech works beyond toy demos and opens a commercial path.

**Repos:** `plato-engine-block-c`, `plato-engine-block-elixir`, `plato-server`, `fleet-dashboard` (from M4), new `marine-pilot` deployment configs  
**Effort:** 4-5 weeks  
**Dependencies:** M4 (fleet dashboard), S9 (engine blocks polished), M1 (PLATO bridge for data flow)  
**Success metric:** System runs unattended for 7 days with zero crashes; dashboard shows live sensor data; alarm triggers on threshold breach; one real vessel operator says "I'd deploy this"  

---

### L4. FLUX Bytecode as an Industry Standard

**What:** Write and publish a formal FLUX ISA specification (versioned, like an RFC). Submit a talk proposal to a major conference (Strange Loop, QCon, RustConf, or an AI/agents conference) presenting FLUX as a portable bytecode for agentic logic — the "WebAssembly for AI agents." Include: formal grammar, opcode reference, security model, conformance test suite, and a comparison with alternatives (no real standard exists today).

**Why:** There is no standard bytecode format for agent logic. Every framework (LangChain, AutoGPT, etc.) uses ad-hoc Python or JSON. FLUX is deterministic, cross-language, and has 3 implementations. If positioned correctly — with a spec, conformance suite, and conference talk — it could become the reference standard for "compiled agent behavior." This is the highest-risk, highest-reward item on the roadmap.

**Repos:** All FLUX repos (`flux-runtime`, `flux-core`, `flux-js`, `flux-conformance`, `flux-a2a-spec`)  
**Effort:** 4-6 weeks (spec writing is slow; conference talk prep)  
**Dependencies:** S7 (conformance suite), M5 (A2A protocol spec), S1-S3 (all three published as proof of cross-platform commitment)  
**Success metric:** Spec document published and versioned; conference talk accepted; at least one external project adopts FLUX bytecode as a serialization format for agent logic; 500+ GitHub stars across FLUX repos  

---

### L5. LAU Game Engine Vertical Slice

**What:** Build a playable game demo using the consolidated `lau-workspace` (from M6): a minimal game world with physics (`lau-gravity-field`, `lau-fluid-dynamics`), entities (`lau-agent-organism`, `lau-agent-lifecycle`), rendering (`lau-camera`, `lau-animation`), and player interaction (`lau-input`, `lau-blueprint`). Ship as a downloadable binary or web page.

**Why:** The `lau-*` ecosystem is 333 repos of game engine math with no game. A playable demo proves the math works together, validates the consolidation, and creates the most shareable artifact in the entire org. Games are visceral — a 30-second gameplay clip communicates more than 50 README files.

**Repos:** `lau-workspace` (consolidated from M6), new `lau-game-demo`  
**Effort:** 5-6 weeks  
**Dependencies:** M6 (lau-workspace consolidation must be done first)  
**Success metric:** Playable demo runs at 60fps; shows physics + agents + player interaction; playable web build shared; posted to r/rust_gamedev or HN with positive engagement  

---

### L6. Exocortex as a Personal AI Substrate

**What:** Productionize `exocortex` into a deployable personal AI substrate: persistent memory (S3-compatible), shadow agents (background reasoning), TUI interface, compute bus, and FastAPI HTTP interface. Package as a Docker image with `docker-compose up` deployment. Include a demo where exocortex connects to a PLATO server and a FLUX runtime, creating a personal AI that can remember, reason, and act.

**Why:** Exocortex is the "glue" project — it connects memory, compute, and agents into a personal AI system. The module structure already exists (bus, compute, config, core, memory, protocols, shadows, tui). With the FLUX↔PLATO bridge (M1) providing reasoning and knowledge, exocortex becomes the substrate that ties everything together for an end user. This is the "consumer face" of the ecosystem.

**Repos:** `exocortex`, `flux-runtime`, `plato-server`, `flux-plato-bridge` (from M1)  
**Effort:** 4-5 weeks  
**Dependencies:** M1 (FLUX↔PLATO bridge), S9 (exocortex polished), M8 (docs site for setup guide)  
**Success metric:** `docker-compose up` starts exocortex with FLUX + PLATO connected; TUI shows memory + reasoning + agent activity; a non-developer can use it within 30 minutes of setup  

---

## Dependency Graph

```
S1 (PyPI: flux-vm) ──────────────┐
S2 (crates.io: fluxvm) ───────────┤
S3 (npm: flux-js) ────────────────┼──→ S7 (Conformance Suite) ──→ M5 (A2A Spec) ──→ L4 (FLUX Standard)
S6 (PyPI: plato-server) ─────────┤                                   │
                                  ├──→ S8 (Demos)                      │
                                  ├──→ M1 (FLUX↔PLATO Bridge)          │
                                  │       │                            │
S4 (CI Hardening) ────────────────┤       ├──→ M2 (Codespace→Edge) ───┼──→ L2 (Git-Agent Product)
S5 (License Sweep) ───────────────┤       │                            │
S9 (Tier 2 Polish) ───────────────┘       ├──→ M4 (Fleet Dashboard) ──┼──→ L3 (Marine Pilot)
                                          │
S10 (Org README) ──→ M8 (Docs Site) ──────┤
                                          │
M6 (lau-workspace) ───────────────────────┼──→ L1 (Ternary SDK)
                                          ├──→ L5 (LAU Game Demo)
                                          │
M3 (Conservation Action) ─────────────────┘

M7 (Hardware Demos) ──→ L3 (Marine Pilot)
M1 (Bridge) ──→ L6 (Exocortex)
```

---

## Sequencing Summary

| Phase | Items | Focus |
|-------|-------|-------|
| **Days 1-15** | S1, S2, S3, S5, S6 | Publish to registries, license sweep |
| **Days 10-25** | S4, S7, S8, S9, S10 | CI hardening, conformance, demos, polish |
| **Weeks 4-6** | M1, M3, M5 | First integrations: FLUX↔PLATO, conservation action, A2A spec |
| **Weeks 5-8** | M2, M4, M6 | End-to-end demo, dashboard, lau consolidation |
| **Weeks 7-10** | M7, M8 | Hardware validation, documentation site |
| **Weeks 8-13** | L1-L6 (parallel tracks) | Moonshots: ternary SDK, git-agent product, marine pilot, FLUX standard, game demo, exocortex |

---

## Success Metrics Dashboard (30/60/90)

| Metric | 30-Day Target | 60-Day Target | 90-Day Target |
|--------|:---:|:---:|:---:|
| Published packages (PyPI + crates.io + npm) | 4 | 6 | 8+ |
| Repos with passing CI (no `|| true`) | 25 | 40 | 60+ |
| Licensed repos | ~100% | 100% | 100% |
| Org repo count (via consolidation) | 4,098 | ~3,800 | ~3,500 |
| External installs/downloads | 50+ | 500+ | 5,000+ |
| Working end-to-end demos | 3 | 6 | 10+ |
| Conference talk submitted | 0 | 1 | 2+ |
| Documentation pages live | 0 | 20+ | 100+ |
| External contributors | 0 | 3+ | 10+ |

---

*Generated 2026-07-12. This is a living document — revisit and revise as the ecosystem evolves.*
