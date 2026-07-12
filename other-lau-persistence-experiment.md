# lau-persistence-experiment

## Intention

Persistence diagrams of agent belief manifolds predict learning trajectories — a topological data analysis framework for understanding how agents learn, in pure Rust.

## How It Works

This crate tests a specific hypothesis from the PLATO/LAU research program:
> **Agents whose belief manifolds have long-lived topological features (high persistence) learn more slowly but more robustly. Agents with short-lived features learn fast but are fragile.**
It does this by applying **persistent homology** — the core tool of topological data analysis (TDA) — to the trajectory of an agent's belief states as it learns. The result is a *persistence diagram* that captures the birth and death of topological features (connected components, loops, voids) across scales.
From that diagram, the crate derives:
- **Betti curves** — how topology evolves during learning
- **Persistence landscapes** — functional summaries suitable for ML pipelines
- **Topological complexity** — a learning-difficulty predictor
- **Birth-death events** — when features appear and disappear
- **Phase transitions** — sudden topology changes = breakthroughs or failures
- **Robustness scores** — high persistence ⟹ robust, low ⟹ fragile
- **Cross-agent comparison** — do different learners have different topological signatures?
- **Falsification** — systematic search for counterexamples
Part of the **PLATO/LAU ecosystem** — a mathematically rigorous framework for building educational agents.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Persistence diagrams of agent belief manifolds predict learning trajectories — a topological data analysis framework for understanding how agents learn, in pure Rust.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (387 lines), mentions tests, includes examples.

- README length: 509 lines, 17986 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (509 lines) with tests, examples, and benchmarks referenced. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
