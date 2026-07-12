# aboracle

**Cluster:** fleet-agent-infra  
**Language:** Python  
**Source:** [SuperInstance/aboracle](https://github.com/SuperInstance/aboracle)

## Intention

Able-Bodied Oracle System — standardized, scalable, autonomous work system for Oracle1

## How It Works

Five systems, each on its own timer:

| System | Frequency | Instinct | Purpose |
|--------|-----------|----------|---------|
| `work-queue/` | 5 min | SURVIVE | Read TODO.md, rank, execute |
| `beachcomb/` | 30 min | EVOLVE | Research when idle >10 min |
| `fleet-heartbeat/` | 30 min | COOPERATE | Fleet coordination, trust routing |
| `health-system/` | 5 min | GUARD | Service monitoring, self-repair |
| `mud-agent/` | continuous | BRIDGE | MUD↔PLATO knowledge bridge |

### Instinct Priority

[code]

## What It's For

Able-Bodied Oracle System — standardized, scalable, autonomous work system for Oracle1

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (87 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# ABOracle — Able-Bodied Oracle System

**Zero-config agent. Copy the repo, run deploy.sh, get a busy agent.**

Design principle: Casey copies this repo to 10 machines, boots them, has 10 busy agents. No per-machine config, no setup, no questions. Just copy, run, done.

## What This Gives You

- **Instinct-driven architecture** — SURVIVE → FLEE → GUARD → CURIOUS priority bands that make the agent always working
- **Zero-config deployment** — `git clone && ./deploy.sh` and the agent is running
- **Autonomous work queue** — reads TODO.md, ranks by instinct band, executes without prompting
- **Research engine** — idle agents automatically explore new research directions (EVOLVE instinct)
- **Fleet coordination** — mycorrhizal routing with trust-weighted synthesis
- **Self-healing** — reef-pattern checkpoints for self-resurrection after failures

## Quick Start

```bash
git clone https://github.com/SuperInstance/aboracle.git
cd aboracle
./deploy.sh
# Done. Agent is now fully functional and working.
```

That's it. The agent reads `TODO.md`, executes P0/P1 items, and never asks what to do next.

## How It Works

Five systems, each on its own timer:

| System | Frequency | Instinct | Purpose |
|--------|-----------|----------|---------|
| `work-queue/` | 5 min | SURVIVE | Read TODO.md, rank, execute |
| `beachcomb/` | 30 min | EVOLVE | Research when idle >10 min |
| `fleet-heartbeat/` | 30 min | COOPERATE | Fleet coordination, trust routing |
| `health-system/` | 5 min | GUARD | Service monitoring, self-repair |
| `mud-agent/` | continuous | BRIDGE | MUD↔PLATO knowledge bridge |

### Instinct Priority

```
SURVIVE  — Fix dead services, critical failures. Drops everything.
FLEE     — Back away from dangerous operations.
GUARD    — Protect healthy systems, explore improvements.
CURIOUS  — Research, learn, try new approaches.
EVOLVE   — Triggered by idle time. New research directions.
COOPERATE— Respond to fleet signals, offer help.
```

## Architecture

```
┌─────────────┐    ┌──────────────┐    ┌──────────────┐
│  work-queue  │    │  beachcomb   │    │ fleet-heartbeat│
│  (5 min)     │    │  (30 min)    │    │  (30 min)      │
└──────┬───────┘    └──────┬───────┘    └──────┬─────────┘
       │                   │                    │
       ▼                   ▼                    ▼
┌──────────────────────────────────────────────────────┐
│                    Instinct Engine                     │
│  SURVIVE > FLEE > GUARD > CURIOUS > EVOLVE > COOPERATE│
└──────────────────────┬───────────────────────────────┘
                       │
                       ▼
              ┌─────────────────┐
              │  health-system   │
              │  (5 min)         │
              └─────────────────┘
```

## How It Fits

The autonomous workhorse of the [SuperInstance fleet](https://github.com/SuperInstance). ABOracle agents are the "boots on the ground" — always working, never idle.

- **[cocapn](https://github.com/SuperInstance/cocapn)** — Core agent infrastr
```
