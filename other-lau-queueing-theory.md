# lau-queueing-theory

## Intention

Queueing theory — mathematical analysis of waiting lines and service systems (M/M/1, M/M/c, M/G/1, Erlang formulas, Jackson networks, priority queues, agent scheduling)

## How It Works

`lau-queueing-theory` provides closed-form and algorithmic solutions for the performance metrics of queueing systems: expected queue length, waiting time, server utilisation, blocking probability, throughput, and more.
You define a system by its **Kendall notation** (A/S/c/K/N/D), call the appropriate module, and get back typed structs with every metric you'd compute by hand in an operations-research course. No simulation, no Monte Carlo — exact formulas where they exist, numerically stable recursions where they don't.
---

## What It's For

Queueing theory — mathematical analysis of waiting lines and service systems (M/M/1, M/M/c, M/G/1, Erlang formulas, Jackson networks, priority queues, agent scheduling)

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (190 lines), mentions tests, includes examples.

- README length: 279 lines, 8637 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
