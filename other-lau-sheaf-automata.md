# lau-sheaf-automata

## Intention

Sheaf-theoretic protocol verification — deadlock-free iff H¹ = 0, composition as cup product.

## How It Works

In concurrent and distributed systems, **deadlock** — where agents cyclically wait on each other forever — is notoriously hard to detect. Traditional approaches (model checking, type systems) don't scale well to large systems with many agents.
This crate takes a **topological** approach:
1. Model a protocol's configuration space as a **sheaf** — a mathematical object that assigns local data (stalks) to regions of a space and connects them with restriction maps
2. Compute the **sheaf cohomology** H⁰ and H¹ using coboundary maps and linear algebra
3. **Deadlock ≡ H¹ ≠ 0**: a non-trivial cohomology class is an "obstruction" to deadlock freedom
Additionally:
- **Protocol composition** (running two protocols together) corresponds to the **cup product** ⌣: H¹ × H¹ → H²
- **Refinement** (making a protocol more specific) is a **natural transformation** between sheaf functors
- **Consensus** is detected via **ergodic theory** on the sheaf's state space
- The **sheaf Laplacian** provides spectral verification of global consistency
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Sheaf-theoretic protocol verification — deadlock-free iff H¹ = 0, composition as cup product.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (266 lines), mentions tests, includes examples.

- README length: 355 lines, 12466 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (355 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
