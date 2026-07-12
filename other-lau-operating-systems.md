# lau-operating-systems

## Intention

OS fundamentals — scheduling, memory management, concurrency primitives

## How It Works

| Module | What you get |
|---|---|
| **CPU Scheduling** | FCFS, SJF, Round Robin, Priority, MLFQ |
| **Memory Management** | Page tables, TLB simulation with LRU eviction |
| **Page Replacement** | FIFO, LRU, Clock (Second Chance), Optimal |
| **Virtual Memory** | Demand paging simulator with fault rate tracking |
| **Disk Scheduling** | FCFS, SSTF, SCAN, C-SCAN |
| **Synchronization** | Mutex, counting semaphore, producer-consumer |
| **Deadlock** | Resource Allocation Graph (cycle detection), Banker's Algorithm |
| **Agent Scheduler** | Auto-selects best algorithm, dependency-aware scheduling (topological sort + SJF) |
58 tests cover correctness, edge cases, Belady's anomaly, and classic OS textbook examples.
---

## What It's For

OS fundamentals — scheduling, memory management, concurrency primitives

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (219 lines), mentions tests, includes examples.

- README length: 324 lines, 14252 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (324 lines) with tests, examples, and benchmarks referenced. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
