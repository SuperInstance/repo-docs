# lau-spectral-gap-experiment

## Intention

lau-spectral-gap-experiment

## How It Works

This crate experimentally tests a deep prediction: **the spectral gap of the graph Laplacian on an MDP's state space equals the convergence rate of entropy-regularized policy gradient on that MDP**.
If the rates match across diverse MDPs (grid worlds, chains, random graphs), this experimentally confirms Emergent Theorem A from the spectral theory of reinforcement learning: the spectral gap is not just an abstract eigenvalue—it directly predicts how fast your RL algorithm converges.
The crate provides:
- **MDP testbed** — grid worlds, chain MDPs, random MDPs with the `MDP` trait
- **Observation Laplacian** — graph Laplacian construction from MDP state adjacency
- **Spectral gap computation** — eigenvalues, Fiedler vector, algebraic connectivity
- **Policy gradient runner** — entropy-regularized PG with convergence rate estimation
- **Rate comparison** — spectral gap vs. PG convergence rate, match/tolerance checking
- **Composable pipeline** — Laplacian → spectral gap ↔ PG rate → comparison

## What It's For

lau-spectral-gap-experiment

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (176 lines), mentions tests, includes examples.

- README length: 260 lines, 8065 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
