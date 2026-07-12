# meta-agent

## Intention

A meta-agent coordinator that dispatches tasks to agents based on capabilities, load, and dependency graphs

## How It Works

`meta-agent` solves the problem of "who does what" in a multi-agent system. It maintains an `AgentPool` of workers with declared capabilities, a `TaskQueue` with priority levels and dependency constraints, and a `Dispatcher` that assigns ready tasks to the best-fit agent. A `WorkGraph` computes the critical path through the dependency DAG, and a `Simulation` runs the full dispatch-execute cycle to predict makespan, agent utilization, and parallelism.
The conservation law **γ + η = C** applies directly: productive agent time (γ) plus idle/wasted time (η) sums to the total makespan C. The critical path analysis ensures γ is maximized.
```
┌──────────────────────────────────────────────────────┐
│                     Simulation                        │
│  run() → SimulationResult (ticks, utilization, etc.) │
├───────────┬──────────────────┬───────────────────────┤
│ AgentPool │    TaskQueue     │      Dispatcher        │
│ ┌───────┐ │ ┌──────────────┐ │  dispatch_round()      │
│ │Agent  │ │ │Task {        │ │  → Vec<Assignment>     │
│ │ caps  │ │ │  caps, deps, │ │                         │
│ │ load  │ │ │  priority,   │ │  best_agent() → lowest │
│ │ speed │ │ │  state       │ │  load/speed score       │
│ │}      │ │ │}             │ │                         │
│ └───────┘ │ └──────────────┘ │                         │

## What It's For

A meta-agent coordinator that dispatches tasks to agents based on capabilities, load, and dependency graphs

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (141 lines), mentions tests, includes examples.

- README length: 180 lines, 7227 characters
- Documented sections: What It Does, Architecture, Installation, Usage, API Reference

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
