# ccc-os

**Cluster:** constraint-theory  
**Language:** Python  
**Source:** [SuperInstance/ccc-os](https://github.com/SuperInstance/ccc-os)

## Intention

Autonomous fleet monitoring — YAML config, REST API, Discord/Telegram/webhook notifications, constraint-aware health checks.

## How It Works

It Fits

The autonomous monitoring and decision-making system for the [SuperInstance fleet](https://github.com/SuperInstance). The public-facing agent that keeps the fleet running.

- **[fleet-health-monitor](https://github.com/SuperInstance/fleet-health-monitor)** — Feeds health data to CCC-OS
- **[cocapn-health-rs](https://github.com/SuperInstance/cocapn-health-rs)** — TCP health checks
- **[co-captain-git-agent](https://github.com/SuperInstance/co-captain-git-agent)** — Human liaison (CCC-OS escalates to Co-Captain)

## What It's For

Autonomous fleet monitoring — YAML config, REST API, Discord/Telegram/webhook notifications, constraint-aware health checks.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (104 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# CCC-OS — Autonomous Fleet Monitoring

**Monitors fleet services, triages signals, and generates decision-ready output without human bottlenecks.**

CCC-OS watches GitHub discussions, fleet health, and Zero-Connectivity feeds, applies a codified rubric to decide what matters, and produces prioritized task queues and presentation decks.

## What This Gives You

- **Signal monitoring** — watches GitHub discussions, fleet health data, and zero-connectivity feeds
- **Codified rubric** — consistent decision framework for prioritizing fleet signals
- **Autonomous triage** — decides what matters without human intervention
- **Health autopilot** — automatically handles routine fleet health issues
- **Deck generation** — produces presentation-ready summaries for human review
- **Fleet bridge** — connects to fleet services for action execution

## Quick Start

```bash
pip install ccc-os
```

```bash
# Run the monitoring daemon
python -m ccc_os

# Or with Docker
docker build -t ccc-os .
docker run -e GITHUB_TOKEN=... ccc-os
```

```python
from ccc_os import FleetBridge, Rubric
from ccc_os.monitors import DiscussionMonitor, HealthMonitor
from ccc_os.health import Autopilot

# Set up monitors
bridge = FleetBridge()
rubric = Rubric.load("rubric.yaml")

# Run the triage loop
monitors = [
    DiscussionMonitor(repo="SuperInstance/cocapn"),
    HealthMonitor(endpoint="http://fleet-health:8080"),
]

for signal in monitors.poll():
    priority = rubric.evaluate(signal)
    if priority.actionable:
        bridge.dispatch(signal, priority)
        if priority.severity == "critical":
            Autopilot.intervene(signal)
```

## Architecture

```
┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│  Discussion   │  │   Health     │  │  Zero-Conn   │
│  Monitor      │  │   Monitor    │  │  Monitor     │
└──────┬────────┘  └──────┬───────┘  └──────┬───────┘
       │                  │                  │
       └──────────┬───────┘──────────────────┘
                  │
                  ▼
          ┌──────────────┐
          │    Rubric     │  ← Codified decision framework
          └──────┬───────┘
                 │
        ┌────────┴────────┐
        │                  │
        ▼                  ▼
┌──────────────┐  ┌──────────────┐
│  Autopilot   │  │    Deck      │
│  (auto-fix)  │  │  Generator   │
└──────────────┘  └──────────────┘
```

## How It Fits

The autonomous monitoring and decision-making system for the [SuperInstance fleet](https://github.com/SuperInstance). The public-facing agent that keeps the fleet running.

- **[fleet-health-monitor](https://github.com/SuperInstance/fleet-health-monitor)** — Feeds health data to CCC-OS
- **[cocapn-health-rs](https://github.com/SuperInstance/cocapn-health-rs)** — TCP health checks
- **[co-captain-git-agent](https://github.com/SuperInstance/co-captain-git-agent)** — Human liaison (CCC-OS escalates to Co-Captain)

## Testing

```bash
pytest tests/
```

## Installation

```bash
pip install ccc-os
# or
docker buil
```
