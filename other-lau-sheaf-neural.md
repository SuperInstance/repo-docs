# lau-sheaf-neural

## Intention

Sheaf-theoretic neural networks — replacing graph Laplacians with sheaf Laplacians.

## How It Works

Standard graph neural networks (GNNs) suffer from **over-squashing**: on graphs with bottleneck edges (low curvature), exponentially-growing neighborhoods get compressed into fixed-size vectors, preventing distant nodes from communicating effectively.
**Sheaf neural networks** solve this by enriching the graph with a **cellular sheaf**:
- Each node v gets a **stalk** F(v) — a vector space (possibly higher-dimensional than the feature vector)
- Each edge (v, w) gets a **restriction map** F_{v≺e}: F(v) → F(w) — a linear map encoding the relationship
- The **sheaf Laplacian** LΣ respects these maps, providing directed, geometry-aware message passing
This crate provides:
- **Cellular sheaves** — the core data structure
- **Sheaf Laplacian** — the operator powering sheaf diffusion
- **Sheaf diffusion** — continuous message passing layers (dx/dt = −σ(LΣ x + b))
- **Sheaf attention** — learn restriction maps from data (attention mechanism)
- **Connection Laplacian** — for oriented sheaves with unitary restriction maps
- **Sheaf curvature** — diagnose over-squashing via Ollivier-Ricci-style curvature
- **p-Laplacian** — nonlinear sheaf diffusion (p > 2 for stronger smoothing)
- **Multi-hop sheaf** — compose restriction maps across k-hop neighborhoods
- **Sheaf pooling** — hierarchy-preserving graph coarsening

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Sheaf-theoretic neural networks — replacing graph Laplacians with sheaf Laplacians.

## Who Would Use It

Machine learning engineers and researchers. Teams deploying or managing ML models.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (296 lines), mentions tests, includes examples.

- README length: 410 lines, 15165 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (410 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
