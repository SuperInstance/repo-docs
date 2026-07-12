# ZeroClaw — Index

**Total repos: 21**

ZeroClaw is a multi-agent crew system where minimal-intelligence agents ("ZeroClaws") operate as crew members in a MUD (multi-user domain) arena. Each ZeroClaw has a specialized role — scribe, scout, sentinel, alchemist, etc. — defined by a scripted "shell" brain. The system explores how far you can get with simple, focused agents that each do one thing well.

## Category Overview

### The ZeroClaw Concept

ZeroClaws are deliberately minimal agents — not sophisticated LLMs, but scripted brains that excel at specific tasks. The name suggests "zero-thought claws" — agents that act on reflex rather than reasoning.

### Agent Shells (12 specialized roles)

Each ZeroClaw has a shell defining its behavior:
- **zc-scribe-shell** — Documentation agent (📝)
- **zc-scout-shell** — Reconnaissance and exploration
- **zc-sentinel-shell** — Guarding and monitoring
- **zc-alchemist-shell** — Transformation and synthesis
- **zc-archivist-shell** — Recording and retrieving history
- **zc-curator-shell** — Organizing and maintaining
- **zc-herald-shell** — Announcing and broadcasting
- **zc-mason-shell** — Building and construction
- **zc-navigator-shell** — Routing and pathfinding
- **zc-scholar-shell** — Research and analysis
- **zc-tinker-shell** — Experimentation and repair
- **zc-weaver-shell** — Connecting and integrating

### Crew & Arena Systems

- **zeroclaw-crew** — The crew management system. Minimal agents jack into the MUD Arena as crew members. 13,400-character README — the most documented repo in this category
- **zeroclaw-arena** — The MUD Arena where ZeroClaws operate
- **zeroclaw-agent-early-version** — Early prototype of the ZeroClaw concept

### Specialized ZeroClaws

- **zeroclaw-fisher** — Fishing/deep-search agent
- **zeroclaw-guard** — Security/guardian agent
- **zeroclaw-scout** — Advanced scouting
- **zeroclaw-trader** — Trading/resource exchange agent

### PLATO Integration

- **zeroclaw-plato** — PLATO system integration
- **zeroclaw-loop** — Agent processing loop

### Key Interconnections

- **zeroclaw-crew** connects to the broader fleet system — crews are a subset of fleets (cocapn-marine provides the command structure)
- **zeroclaw-arena** is a MUD (multi-user domain) connecting to git-native-mud in agent-framework
- The **shell system** relates to the lau-shell-* family in lau-mathematics (shell-interface, shell-kernel, shell-lifecycle, shell-spawn, shell-transport)
- **zeroclaw-plato** integrates with the PLATO system that underpins the Lau game engine
- The minimal-agent philosophy contrasts with (and complements) the sophisticated mathematical agents in superinstance-core
- Each shell role mirrors real crew positions on a ship — connecting to the maritime metaphor of cocapn-marine

## Full Repository Listing

### Agent Shells

| Repo | Language | Description |
|------|----------|-------------|
| [zc-scribe-shell](./other-zc-scribe-shell.md) | — | 📝 Documentation agent |
| [zc-scout-shell](./other-zc-scout-shell.md) | — | Reconnaissance agent |
| [zc-sentinel-shell](./other-zc-sentinel-shell.md) | — | Guard/monitor agent |
| [zc-alchemist-shell](./other-zc-alchemist-shell.md) | — | Transform/synthesize agent |
| [zc-archivist-shell](./other-zc-archivist-shell.md) | — | History record/retrieve |
| [zc-curator-shell](./other-zc-curator-shell.md) | — | Organize/maintain |
| [zc-herald-shell](./other-zc-herald-shell.md) | — | Announce/broadcast |
| [zc-mason-shell](./other-zc-mason-shell.md) | — | Build/construct |
| [zc-navigator-shell](./other-zc-navigator-shell.md) | — | Route/pathfind |
| [zc-scholar-shell](./other-zc-scholar-shell.md) | — | Research/analyze |
| [zc-tinker-shell](./other-zc-tinker-shell.md) | — | Experiment/repair |
| [zc-weaver-shell](./other-zc-weaver-shell.md) | — | Connect/integrate |

### Crew & Arena

| Repo | Language | Description |
|------|----------|-------------|
| [zeroclaw-crew](./other-zeroclaw-crew.md) | Python | Crew management system |
| [zeroclaw-arena](./other-zeroclaw-arena.md) | Python | MUD Arena |
| [zeroclaw-agent-early-version](./other-zeroclaw-agent-early-version.md) | Python | Early prototype |

### Specialized Agents

| Repo | Language | Description |
|------|----------|-------------|
| [zeroclaw-fisher](./other-zeroclaw-fisher.md) | Python | Deep-search agent |
| [zeroclaw-guard](./other-zeroclaw-guard.md) | Python | Security agent |
| [zeroclaw-scout](./other-zeroclaw-scout.md) | Python | Advanced scouting |
| [zeroclaw-trader](./other-zeroclaw-trader.md) | Python | Resource exchange |

### PLATO Integration

| Repo | Language | Description |
|------|----------|-------------|
| [zeroclaw-plato](./other-zeroclaw-plato.md) | Python | PLATO integration |
| [zeroclaw-loop](./other-zeroclaw-loop.md) | Python | Processing loop |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
