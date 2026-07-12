# ActiveLog — Index

**Total repos: 11**

Activity logging, active inference, and ledger systems for the SuperInstance fleet. The ActiveLog collection provides the observability and cognitive layer — logging what agents do, inferring why they did it, and maintaining ledgers of fleet activity.

## Category Overview

### Three Sub-systems

#### 1. ActiveLog — Activity Logging Pipeline

A three-stage pipeline:
- **activelog-agent** — Monitoring agent that observes fleet activity
- **activelog-backend** — Python backend service that stores and queries logs
- **activelog** / **ActiveLog-MVP** — The core product (currently no README, described as "complete system")
- **ActiveLog-TechnicalRepo** — Technical documentation repository
- **activelog-claude** — Claude integration for log analysis
- **activelog-ai-pages** — AI-powered log analysis pages
- **active-probe** — Active probing for system health

#### 2. Active Inference — Cognitive Framework

- **active-inference** — Rust implementation of the Free Energy Principle. Agents don't just perceive — they act to reduce expected free energy. Implements policy enumeration, expected free energy evaluation, precision-weighted action selection, and Bayesian state estimation. Published to crates.io. 265-line README with architecture, math background, and API reference.

#### 3. ActiveLedger — Distributed Ledger

- **activeledger-agent** — Agent for the ActiveLedger system
- **activeledger-ai-pages** — AI-powered ledger analysis

### The Pipeline

```
activelog-agent (monitors) → activelog-backend (stores/queries) → activelog-claude/ai (analyzes)
                                                          ↓
                                               activeledger-agent (records)
```

### Key Interconnections

- **active-inference** provides the cognitive theory — agents minimizing free energy, which drives both perception and action. This is the theoretical complement to the practical logging pipeline.
- **activelog-backend** is a Python service that stores agent activity for later analysis
- **activelog-claude** shows integration with Claude for AI-powered log interpretation
- The logging pipeline feeds into fleet health monitoring (si-fleet-health in superinstance-core)
- Active inference connects to the broader mathematical framework: it uses the same variational methods as si-variational-agent

## Full Repository Listing

### ActiveLog Pipeline

| Repo | Language | Description |
|------|----------|-------------|
| [activelog](./other-activelog.md) | — | Core product (complete system) |
| [ActiveLog-MVP](./other-ActiveLog-MVP.md) | — | MVP version |
| [ActiveLog-TechnicalRepo](./other-ActiveLog-TechnicalRepo.md) | — | Technical documentation |
| [activelog-agent](./other-activelog-agent.md) | Python | Monitoring agent |
| [activelog-backend](./other-activelog-backend.md) | Python | Backend storage/query |
| [activelog-claude](./other-activelog-claude.md) | — | Claude integration |
| [activelog-ai-pages](./other-activelog-ai-pages.md) | HTML | AI-powered analysis pages |
| [active-probe](./other-active-probe.md) | — | Active system probing |

### Active Inference

| Repo | Language | Description |
|------|----------|-------------|
| [active-inference](./other-active-inference.md) | Rust | Free Energy Principle — perception + action |

### ActiveLedger

| Repo | Language | Description |
|------|----------|-------------|
| [activeledger-agent](./other-activeledger-agent.md) | — | Ledger agent |
| [activeledger-ai-pages](./other-activeledger-ai-pages.md) | HTML | Ledger AI pages |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
