# lau-vibe-field

## Intention

CUDA/cuDNN of PLATO — the vibe field as a first-class compute primitive.

## How It Works

`lau-vibe-field` provides the core spatial data structure for the Lau platform. A **vibe field** is a 2D grid of `f64` values representing energy, attention, emotion, or any continuous scalar quantity distributed across space. The library enforces **strict energy conservation** (deposits and withdrawals are atomic, total energy is tracked incrementally) and provides PDE-level operations: diffusion (heat equation), semi-Lagrangian advection, gradient/Laplacian computation, and divergence.
Multiple fields are managed by a `VibeFieldEngine` that ticks them forward together, and `VibeFieldPair` enables conservation-preserving energy transfers between two fields.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. CUDA/cuDNN of PLATO — the vibe field as a first-class compute primitive.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** CUDA, Serde, PyTorch

## Status Assessment

**Status: MODERATE**

Reasonable README (184 lines), mentions tests, includes examples.

- README length: 272 lines, 9383 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
