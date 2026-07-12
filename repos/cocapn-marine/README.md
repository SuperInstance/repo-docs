# Cocapn Marine — Index

**Total repos: 11**

Maritime-themed fleet command and underwater sensing systems for the SuperInstance ecosystem. The cocapn-marine collection implements the fleet coordination layer where a Captain agent receives dispatched work and distributes it across fleet vessels, along with sonar/acoustic sensing for environmental awareness.

## Category Overview

### Fleet Command (Maritime Metaphor)

The SuperInstance fleet uses a naval hierarchy metaphor:
- **Captain** — The commanding vessel that receives work from the Co-Captain (human liaison) and distributes tasks across fleet agents using priority queues, strategy selection, and leadership styles
- **Co-Captain** — The human liaison that dispatches work to the Captain
- **Cocapn** — The inter-agent messaging and coordination SDK

### Sub-domains

#### 1. Fleet Command & Coordration

- **captain** — Fleet commanding vessel with priority queues, strategy engine (sequential, parallel, adaptive), leadership styles (directive, collaborative, delegative), and structured fleet health reports
- **captains-log** — Captain's logging system — structured narrative of fleet decisions
- **cocapn-cli** — CLI tool for fleet operations
- **cocapn-sdk** — SDK for building fleet-aware applications
- **cocapn-explain** — Explanation and interpretability layer for fleet decisions

#### 2. Sonar & Acoustic Sensing

- **sonar-vision** — Pure-Python sonar ping/echo simulation, signal processing, multi-object tracking, and spatial mapping (86 tests)
- **sonar-vision-c** — C implementation of sonar processing
- **sonar-vision-rs** — Rust implementation
- **sonar-vision-landing** — Landing page / documentation site

#### 3. Fishing & Activity Logging

- **fishinglog-agent** — Agent for the FishingLog application
- **fishinglog-ai-pages** — AI-powered pages for fishing logs

### Key Interconnections

- **captain** receives work from **co-captain-git-agent** (in the agent-framework category) and distributes to fleet agents
- **cocapn-sdk** and **cocapn-cli** are the developer-facing tools for fleet operations
- **sonar-vision** provides environmental sensing — the "eyes" of the fleet
- The maritime metaphor extends to other categories: vessels (superinstance-core), crews (zeroclaw), and ports (lau-mathematics)
- **captain** connects to cluster-orchestrator for multi-agent task assignment
- The fleet coordination model uses the same conservation/spectral framework as the rest of the ecosystem

## Full Repository Listing

| Repo | Language | Description |
|------|----------|-------------|
| [captain](./other-captain.md) | Python | Fleet commanding vessel — strategy, priorities, leadership |
| [captains-log](./other-captains-log.md) | Python | Structured fleet decision log |
| [cocapn-cli](./other-cocapn-cli.md) | Rust | Fleet operations CLI |
| [cocapn-sdk](./other-cocapn-sdk.md) | Rust | Fleet coordination SDK |
| [cocapn-explain](./other-cocapn-explain.md) | Rust | Fleet decision explainability |
| [sonar-vision](./other-sonar-vision.md) | Python | Sonar simulation & signal processing |
| [sonar-vision-c](./other-sonar-vision-c.md) | C | C sonar processing |
| [sonar-vision-rs](./other-sonar-vision-rs.md) | Rust | Rust sonar processing |
| [sonar-vision-landing](./other-sonar-vision-landing.md) | HTML | Sonar documentation site |
| [fishinglog-agent](./other-fishinglog-agent.md) | Python | Fishing log agent |
| [fishinglog-ai-pages](./other-fishinglog-ai-pages.md) | HTML | AI-powered fishing log pages |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
