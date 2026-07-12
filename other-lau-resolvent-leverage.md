# lau-resolvent-leverage

## Intention

Resolvent Leverage Theorem — ‖R(λ)‖ = 1/dist, zero work at the still point, infinite sensitivity, mutual constitution of center and periphery.

## How It Works

This crate implements the **Resolvent Leverage Theorem** (also called the Still-Point Identity): for a generator matrix L with isolated kernel and spectral gap γ, the resolvent R(λ) = (λI − L)⁻¹ satisfies ‖R(λ)‖ = 1/dist(λ, σ(L)) for normal operators. The kernel (the "still point") does zero Dirichlet work, has infinite resolvent sensitivity, and is mutually constituted with the periphery.
The library provides:
- **Riesz projection** — spectral projector onto ker(L), verified idempotent (e² = e)
- **Resolvent sensitivity** — ‖R(λ)‖ → ∞ as λ → 0, the still-point identity
- **Dirichlet form** — E(f, f) = ⟨f, Lf⟩ vanishes exactly on ker(L) (zero work)
- **Spectral gap stability** — Davis–Kahan sin(θ) theorem bounds on perturbation
- **Collapse rate** — e^{−tL} → e (the projector) at rate γ
- **Mutual constitution** — center and periphery co-create each other
- **Non-normal analysis** — pseudospectral leverage for non-symmetric operators
- **Slow-mode steering** — eigenvalues closest to 0 are the "leverage points"
- **Gap engineering** — widen or narrow the spectral gap by scaling periphery dynamics
- **Crate analysis** — one-call summary of any generator's resolvent leverage properties

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Resolvent Leverage Theorem — ‖R(λ)‖ = 1/dist, zero work at the still point, infinite sensitivity, mutual constitution of center and periphery.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (281 lines), mentions tests, includes examples.

- README length: 395 lines, 13929 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (395 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
