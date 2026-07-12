# Index: Cocapn Repositories

Generated: 2026-07-12
Total repos: 3

## Overview

Cocapn is the repo-first agent infrastructure for local or cloud deployment. These repos form the core cocapn ecosystem.

## Repositories

| Repo | Description | Language | Status |
|------|-------------|----------|--------|
| [cocapn](other-cocapn.md) | Repo-first agent infrastructure — grow an agent in a repo using the repo itself as muscle-memory. Tiles capture knowledge, rooms train, flywheel compounds. | Python | real (well-documented, working examples) |
| [cocapn.ai](other-cocapn.ai.md) | Fleet Agents for the Cocapn Ecosystem — landing page and fleet info. | PHP | stub (no README) |
| [cocapn.github.io](other-cocapn.github.io.md) | Cocapn fleet home page — live at cocapn.ai. | HTML | stub (no README) |

## Notes

- **cocapn** is the core package published to PyPI
- Well-documented with working examples and API surface
- Integrates with the SuperInstance fleet ecosystem
- Related repos include:
  - cocapn-sdk (one API key, any AI model)
  - cocapn-cli (fleet terminal formatting in Rust)
  - cocapn-explain (agent explainability)
  - cocapn-health-rs (fleet health monitoring)
  - cocapn-lessons (trial-based learning)
  - agent-forge (universal git-agent framework)

## Core Components

- **Tiles** — atomic knowledge units that remember Q&A, tagged and versioned
- **Rooms** — self-training collections of tiles that get smarter over time
- **Flywheel** — compounding engine for learning from exchanges
- **CocapnAgent** — high-level interface: ask(), teach(), status(), save()
