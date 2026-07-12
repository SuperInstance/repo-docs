# lau-scheduler

## Intention

Tick-based task scheduler for game loops

## How It Works

The heartbeat of the **Lau (Layered Agent-UI)** game loop. Every game tick, the scheduler decides what runs and when. Tasks have priorities (critical, high, normal, low, idle), can be one-shot or recurring, and can be cancelled mid-flight.
Built for deterministic game loops: same tick count + same task graph = same execution order. Every time.

## What It's For

Tick-based task scheduler for game loops

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (52 lines), mentions tests, includes examples.

- README length: 74 lines, 2658 characters
- Documented sections: What This Does, Quick Start, API Reference, Testing, Part of the Lau Platform

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
