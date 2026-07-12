# collective-ai

**Cluster:** ai-cognitive  
**Language:** Python  
**Source:** [SuperInstance/collective-ai](https://github.com/SuperInstance/collective-ai)

## Intention

Extracted from plato-training

## How It Works

[code]

Zero dependencies. Pure Python. Thread-safe throughout.

## What It's For

Extracted from plato-training

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (200 lines, 5444 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# collective-ai

**Simulation-first collective inference: predict, observe, gap, learn.**

A zero-dependency Python library for building systems where agents predict what should happen, observe reality, and surface mismatches (gaps) as the research agenda. Every instance is a peer. The glitches *are* the work.

Extracted from the PLATO training infrastructure.

## The Core Loop

Every room, every instance, runs this loop:

```
1. PREDICT  — "At t-minus-event, I expect X to happen"
2. LISTEN   — sensors watch for what actually happens
3. COMPARE  — prediction vs reality
4. GAP      — if mismatch → gap signal → focus queue
5. LEARN    — focus on the gap, update the room's model
6. SHARE    — broadcast updated understanding to peers via I2I
```

A fleet of instances collectively discovers what they don't know.

## Installation

```bash
pip install -e .
```

From PyPI (eventually):

```bash
pip install collective-ai
```

**Requirements:** Python ≥ 3.10. No external dependencies.

## Quick Start

```python
from collective_ai import SimulationRoom, RoomAddress, RoomKind

# Create a room
room = SimulationRoom(
    address=RoomAddress.parse("node-1/drift-detect"),
    kind=RoomKind.PREDICTOR,
    tolerance=0.1,
)

# Predict what should happen
prediction = room.predict(
    event_type="sensor_reading",
    predicted_value=42.0,
    confidence=0.95,
    horizon_seconds=60.0,
)

# Observe what actually happened
gap = room.observe("sensor_reading", actual_value=47.5)

if gap:
    print(f"Gap detected! delta={gap.delta:.3f}, severity={gap.severity.value}")
    # GapSignal(gap_id='a1b2c3d4e5f6', room='node-1/drift-detect',
    #           severity='medium', delta=0.116)
```

### Multi-Stream Detection

```python
from collective_ai import SimulationRoom, RoomAddress

room = SimulationRoom(
    address=RoomAddress.parse("fleet/monitor"),
    tolerance=0.1,
)

# Predict multiple streams
room.predict("cpu", 45.0, confidence=0.9, horizon_seconds=30)
room.predict("memory", 80.0, confidence=0.9, horizon_seconds=30)
room.predict("latency", 12.0, confidence=0.85, horizon_seconds=30)

# Observe reality
room.observe("cpu", 46.0)       # within tolerance → no gap
room.observe("memory", 92.0)    # exceeds tolerance → gap
room.observe("latency", 15.5)   # exceeds tolerance → gap

# Get focus report — what needs attention
print(room.focus_report())
```

### Nested Rooms

```python
# Rooms can contain rooms (levels)
parent = SimulationRoom(RoomAddress.parse("instance/fleet"), kind=RoomKind.LEVEL)
child = parent.add_child("drift-detect", kind=RoomKind.PREDICTOR)
grandchild = child.add_child("sub-sensor", kind=RoomKind.SENSOR)
```

### Focus Queue

The priority queue of gaps, sorted by `focus_score = confidence × delta`:

```python
queue = room.gaps

# Top gaps
top_gaps = queue.top(5)

# Filter by severity
critical = queue.by_severity(GapSeverity.CRITICAL)

# Summary
print(queue.summary())
```

## Core Types

### `SimulationRoom`

A room that predicts before it observes. Thread
```
