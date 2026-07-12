# CCC

**Cluster:** fleet-agent-infra  
**Language:** Python  
**Source:** [SuperInstance/CCC](https://github.com/SuperInstance/CCC)

## Intention

CCC public face agent — Kimi K2.5, frontend design, fleet orchestration, PLATO cultivation for the Cocapn fleet

## How It Works

[code]

### Console

The main entry point. Wires together dashboard, alerts, commands, and display.

[code]

### Dashboard

In-memory store for agents, tasks, and metrics with query methods:

[code]

### CommandParser

Interprets CLI-style commands. Built-in: `status`, `agents`, `tasks`, `alerts`, `help`.
Register custom commands:

[code]

### AlertManager

Severity levels (`INFO`, `WARN`, `ERROR`, `CRITICAL`), notification channels, and auto-escalation:

[code]

### DisplayFormatter

ASCII tables, ANSI-colored status, progress bars, and sparkline charts:

[code]

## What It's For

CCC public face agent — Kimi K2.5, frontend design, fleet orchestration, PLATO cultivation for the Cocapn fleet

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (154 lines, 4028 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# CCC — Central Command Console

A unified dashboard for monitoring and controlling agent fleets. Built with Python dataclasses, type hints, and zero external dependencies beyond `pytest` for testing.

## Install

```bash
pip install -e ".[dev]"
```

## Quick Start

```python
from ccc import Console
from ccc.models import AgentStatus

# Create the console
console = Console()

# Register fleet agents
console.register_agent("oracle1", role="keeper", model="glm-5.1")
console.register_agent("forge1", role="builder", host="node-1")
console.register_agent("jetson1", role="edge", model="jetson-orin")

# Bring agents online
console.update_status("oracle1", AgentStatus.ONLINE)
console.update_status("forge1", AgentStatus.BUSY)

# Create and assign tasks
task = console.create_task("build-artifact", agent_name_or_id="forge1", priority=5)
console.start_task(task.id)
console.complete_task(task.id)

# Report health metrics (triggers alerts on thresholds)
console.report_metric("oracle1", "cpu", 45.0, "%", warning=70.0, critical=90.0)
console.report_metric("forge1", "cpu", 95.0, "%", warning=70.0, critical=90.0)

# Execute CLI commands
result = console.execute("status")
print(result.output)
# ═══ Fleet Status ═══
#   Agents: 3 total  (1 online, 1 busy, 0 error, 1 offline)
#   Tasks:  1 total  (0 pending, 0 running, 1 done, 0 failed)
#   Metrics: 2 recorded

# Render formatted tables
print(console.render_agents())
# Name       Status   Role       Model       Host
# ─────────────────────────────────────────────────
# oracle1    online   keeper     glm-5.1
# forge1     busy     builder                node-1
# jetson1    offline  edge       jetson-orin
```

## Architecture

```
ccc/
├── __init__.py       # Public API
├── models.py         # Dataclasses: Agent, Task, HealthMetric
├── console.py        # Console — main entry point
├── dashboard.py      # Dashboard — fleet state store with queries
├── command.py        # CommandParser — CLI-style command interpreter
├── alert.py          # AlertManager — severity, escalation, notifications
└── display.py        # DisplayFormatter — ASCII/ANSI tables and sparklines
```

### Console

The main entry point. Wires together dashboard, alerts, commands, and display.

```python
from ccc import Console

c = Console()
c.register_agent("agent-1")
c.execute("status")
```

### Dashboard

In-memory store for agents, tasks, and metrics with query methods:

```python
from ccc import Dashboard

d = Dashboard()
d.add_agent(agent)
d.agents_by_status()      # → dict[AgentStatus, list[Agent]]
d.online_agents()          # → available agents
d.tasks_for_agent(id)      # → agent's tasks
d.latest_metrics(id)       # → most recent metric per type
```

### CommandParser

Interprets CLI-style commands. Built-in: `status`, `agents`, `tasks`, `alerts`, `help`.
Register custom commands:

```python
from ccc import CommandParser, Console

parser = CommandParser()

def my_handler(*, args, **kw):
    return CommandResult(command="ping", success=True, out
```
