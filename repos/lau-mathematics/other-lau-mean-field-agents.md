# lau-mean-field-agents

## Intention

Mean-field games for agent populations — Lasry-Lions coupled HJB/Fokker-Planck fixed point.

## How It Works

This crate implements the full MFG pipeline:
| Module | Role | Key Equations |
|---|---|---|
| **HJB** | Backward value function (cost-to-go) | −∂u/∂t = σ²/2·Δu + H(∇u) + f(x, m) |
| **Fokker-Planck** | Forward density evolution | ∂m/∂t = σ²/2·Δm − div(m·α*) |
| **Lasry-Lions** | Coupled fixed-point iteration | Solve HJB → extract controls → solve FP → repeat |
| **McKean-Vlasov** | N-agent → continuum limit | μₜ = Law(Xₜ), propagation of chaos |
| **Nash equilibrium** | Best response, social cost | Price of anarchy, cooperative vs competitive |
| **Wasserstein** | Distance between distributions | W₁ (earth mover), W₂ (quantile-based) |
| **Existence** | Verification of MFG conditions | Lasry-Lions monotonicity, contraction |

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Mean-field games for agent populations — Lasry-Lions coupled HJB/Fokker-Planck fixed point.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (203 lines), mentions tests, includes examples.

- README length: 280 lines, 9221 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (280 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
