# bordercollie

**Cluster:** fleet-agent-infra  
**Language:** Python  
**Source:** [SuperInstance/bordercollie](https://github.com/SuperInstance/bordercollie)

## Intention

herding 10,000 local cuda-based agents with memories and skills

## How It Works

[code]

### Component Overview

| Component | Role |
|-----------|------|
| `Herd` | Main class. Manages agent registry, tracks status |
| Drift Detector | Compares agent behavior against expected baseline |
| Goal Propagator | Broadcasts goals to agents, tracks acknowledgment |
| Priority Router | Routes tasks based on priority and agent capacity |
| Status Monitor | Real-time aligned/drifting counts |

### Herding Flow

[code]

## What It's For

herding 10,000 local cuda-based agents with memories and skills

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (209 lines, 5525 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
**Topics:** `fleet-coordination` `agent-herding` `synchronization` `task-routing` `distributed-agents` `cocapn`

---

# BorderCollie — Fleet Herding Agent

> Fleet herding at scale — keeping 10,000+ agents aligned and heading in the same direction.

**BorderCollie** is a **fleet coordination agent** that keeps distributed AI agents synchronized and heading toward shared goals. Like a border collie managing sheep, it manages, groups, and directs tasks across distributed systems — ensuring no agent drifts off course while the herd moves together.

Part of the [Cocapn fleet](https://github.com/SuperInstance) — lighthouse keeper architecture.

---

## What It Does

BorderCollie manages the **alignment problem** in distributed agent fleets:

- **Alignment** — Ensures all agents see consistent goals and constraints
- **Synchronization** — Keeps agent state and configuration in sync across the fleet
- **Herding** — Detects drift and nudges agents back on course
- **Grouping** — Organizes agents into working groups (teams, roles, specializations)

### Key Features

- **Goal propagation** — Push goals to all agents in the herd
- **Drift detection** — Monitor agent behavior against expected baseline
- **Priority routing** — High/medium/low priority task distribution
- **Status tracking** — Real-time view of aligned vs. drifting agents

---

## Quick Start

### Install

```bash
pip install cocapn-bordercollie
```

### Basic Usage

```python
from bordercollie import Herd

# Create a herd
herd = Herd()

# Register agents with roles
herd.add("oracle1", {"role": "coordinator", "capacity": 100})
herd.add("jetson1", {"role": "worker", "capacity": 60})
herd.add("ccc1", {"role": "worker", "capacity": 40})

# Herd toward a goal
herd.herd_toward(goal="sync-config", priority="high")

# Check status
status = herd.status()
print(f"Aligned: {status['aligned']}")
print(f"Drifting: {status['drifting']}")
```

### Advanced Usage

```python
from bordercollie import Herd, Priority

# Create herd with configuration
herd = Herd(
    drift_threshold=0.15,      # Flag agents >15% off baseline
    sync_interval=30,          # Re-sync every 30 seconds
    priority=Priority.HIGH
)

# Add agents with metadata
herd.add("agent-1", {"role": "orchestrator", "specialization": "code"})
herd.add("agent-2", {"role": "worker", "specialization": "research"})
herd.add("agent-3", {"role": "worker", "specialization": "docs"})

# Broadcast a goal to a subset
herd.herd_subset(
    goal="audit-fleet",
    filter={"role": "worker"},
    priority=Priority.MEDIUM
)

# Get drift report
drift_report = herd.drift_report()
for agent, drift_score in drift_report.items():
    if drift_score > 0.5:
        print(f"ALERT: {agent} is drifting ({drift_score:.0%})")
```

---

## Architecture

```
bordercollie/
├── README.md
├── CHARTER.md
├── DOCKSIDE-EXAM.md
├── LICENSE
└── tests/
    └── test_bordercollie_docs.py   # Documentation contract tests
```

### Component Overview

| Component | Role |
|-----------|---
```
