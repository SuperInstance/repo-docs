# lau-varadhan-transport

## Intention

Varadhan's formula and Maslov dequantization — spectral theory through tropical geometry to optimal transport.

## How It Works

- **Heat kernel computation**: matrix exponential of the graph Laplacian via eigendecomposition, with graph constructors (path, complete, cycle, star).
- **Varadhan's formula verification**: numerically confirm that `−4t log p_t(x,y) → d(x,y)²` as `t → 0`, with convergence rate tracking.
- **Cole-Hopf transform**: `v = −ℏ log u` converts heat solutions to Hamilton-Jacobi solutions; invertible roundtrip.
- **Maslov dequantization**: deformed addition `x ⊕_ℏ y → min(x,y)` as `ℏ→0`, tropical semirings (min-plus and max-plus), dequantization convergence tracking.
- **Hopf-Lax semigroup**: `Q_t u(x) = min_y [u(y) + d(x,y)²/(2t)]` — the viscosity solution semigroup for Hamilton-Jacobi, with verified semigroup property.
- **Benamou-Brenier transport**: Wasserstein-1 and W₂² distances, heat-kernel transport plans, McCann interpolation between distributions.
- **Tropical attention**: softmax → hardmax as temperature → 0, with entropy tracking and softening paths — a tropical interpretation of transformer attention.
- **Spectral transport bridge**: spectral embedding, diffusion distance, spectral gap, and the full bridge from eigenvalues to geodesic distances.
- **ℏ-interpolation**: Sinkhorn-regularized optimal transport via the Gibbs kernel `exp(−d²/ℏ)`, with ℏ controlling the spectral↔tropical transition.
- **GPU kernel scheduling**: two application modules applying the framework to real-world GPU dispatch — heat kernel priority, Varadhan transport costs, tropical attention-based assignment.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Varadhan's formula and Maslov dequantization — spectral theory through tropical geometry to optimal transport.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (286 lines), mentions tests, includes examples.

- README length: 393 lines, 13847 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (393 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
