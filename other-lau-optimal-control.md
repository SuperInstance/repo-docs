# lau-optimal-control

## Intention

Optimal control theory in Rust — LQR, Riccati equations, Pontryagin's Maximum Principle, Hamilton-Jacobi-Bellman, trajectory optimization, controllability/observability analysis, bang-bang control, and agent action planning.

## How It Works

| Module | What you get |
|---|---|
| **LQR** | Discrete and continuous LQR with gain matrix K and cost-to-go V(x) = x'Px |
| **Riccati** | DARE, CARE, and differential Riccati equation (finite horizon) |
| **Pontryagin** | Hamiltonian system solver, PMP condition verification |
| **HJB** | Grid-based 1D Hamilton-Jacobi-Bellman solver, LQR value function |
| **Bang-bang** | Double integrator time-optimal control, switching function analysis |
| **Trajectory** | Direct collocation and single shooting with gradient-based optimization |
| **Controllability** | Rank test, Gramian computation, stabilizability/detectability |
| **Dynamics** | Linear and nonlinear system simulation, Jacobian linearization |
| **Agent** | Policy computation, trajectory simulation, action planning, discrete action selection |
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Optimal control theory in Rust — LQR, Riccati equations, Pontryagin's Maximum Principle, Hamilton-Jacobi-Bellman, trajectory optimization, controllability/observability analysis, bang-bang control, an

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (252 lines), mentions tests, includes examples.

- README length: 373 lines, 13497 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (373 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
