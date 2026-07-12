# lau-singular-spde

## Intention

lau-singular-spde

## How It Works

This crate implements the mathematical machinery for studying agent learning dynamics that are governed by *singular* stochastic partial differential equations — equations where classical solutions don't exist and renormalization is required:
- **SPDE formulation** — Agent beliefs evolve as `∂ₜu = Lu + F(u) + ξ` where `ξ` is space-time white noise
- **Singularity classification** — Regular, Critical, or Singular based on regularity exponents
- **Regularity structures** — Hairer's framework: graded symbol spaces, model distributions, reconstruction operator, structure groups
- **Wick ordering** — Renormalization of divergent products: `:u²: = u² - ⟨u²⟩`, `:u³: = u³ - 3⟨u²⟩u`
- **Renormalization group** — Beta functions, fixed points (Gaussian, Wilson-Fisher), critical exponents, RG flow
- **Universal classes** — KPZ, Allen-Cahn, Φ⁴, and diffusive universality classes with their SPDEs and scaling behavior
- **Hölder regularity** — Regularity exponents for SPDE solutions, determining when renormalization is needed
- **PLATO classification** — Maps agent types (gradient descent, natural gradient, actor-critic, etc.) to their SPDE classification and renormalization requirements
- **Numerical solvers** — Euler-Maruyama integration, energy functionals, trajectory computation

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. lau-singular-spde

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (203 lines), includes examples.

- README length: 281 lines, 11805 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (281 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
