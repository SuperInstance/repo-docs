# lau-scheduling-theory

## Intention

Scheduling theory — optimal resource allocation over time: job scheduling, priority rules, flow shop, branch and bound, and agent fleet scheduling

## How It Works

This crate implements the core algorithms from classical scheduling theory:
- **Job model** — jobs with processing times, weights, due dates, release dates, and deadlines; schedules with computed objectives (makespan, total completion time, weighted completion time, max lateness, total tardiness)
- **Priority rules** — SPT, EDD, WSPT, LPT, FCFS dispatching heuristics
- **Single-machine scheduling** — schedule jobs on one machine using any priority rule
- **Parallel-machine scheduling** — identical parallel machines with list scheduling and makespan lower bounds
- **Flow shop** — Johnson's algorithm for the optimal 2-machine flow shop (F2 ‖ C_max)
- **Branch and bound** — exact optimization for total weighted completion time (single machine) and makespan (parallel machines)
- **Preemptive scheduling** — Shortest Remaining Processing Time (SRPT) and preemptive EDD
- **Due-date objectives** — minimize L_max (EDD, optimal), minimize ΣT_j (slack heuristic), minimize number of tardy jobs (Moore's algorithm)
- **Precedence constraints** — topological sorting, SPT-with-precedence scheduling
- **Resource-constrained scheduling** — serial schedule generation scheme with resource capacity tracking
- **Shop scheduling** — open shop (greedy/LPT dispatching) and job shop (greedy route-based dispatching)
- **Agent fleet scheduling** — multi-agent task assignment with specializations, dependencies, capacity scaling, utilization and load-balance metrics

## What It's For

Scheduling theory — optimal resource allocation over time: job scheduling, priority rules, flow shop, branch and bound, and agent fleet scheduling

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (212 lines), mentions tests, includes examples.

- README length: 288 lines, 13127 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (288 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
