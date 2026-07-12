# lau-numerical-pde

## Intention

Numerical methods for PDEs — finite differences, heat/wave/Poisson/advection-diffusion solvers, boundary conditions, error analysis, and agent field dynamics

## How It Works

This crate is a **from-scratch PDE solver toolkit** in pure Rust:
| Module | What you get |
|---|---|
| **Finite differences** | 1D/2D uniform grids, central/forward/backward differences, 2nd and 4th order |
| **Heat equation** | Forward Euler (explicit), Backward Euler (implicit), Crank-Nicolson |
| **Wave equation** | Leapfrog, Lax-Wendroff with dissipation, energy conservation tracking |
| **Poisson equation** | Jacobi, Gauss-Seidel, SOR (with optimal ω), 2D elliptic solver |
| **Advection-diffusion** | Upwind advection + central diffusion, 1D and 2D, CFL/Peclet analysis |
| **Boundary conditions** | Dirichlet, Neumann, Periodic — composable for 1D and 2D |
| **Error analysis** | L2/L∞/L1 norms, convergence order, Richardson extrapolation, total variation |
| **Agent fields** | Information diffusion simulation, consensus metrics, biased diffusion |
76 unit tests cover stability, convergence, conservation, and accuracy.
---

## What It's For

Numerical methods for PDEs — finite differences, heat/wave/Poisson/advection-diffusion solvers, boundary conditions, error analysis, and agent field dynamics

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (248 lines), mentions tests, includes examples.

- README length: 369 lines, 13881 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (369 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**

> ⚠️ **Ecosystem dependency:** This repo makes 4+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
