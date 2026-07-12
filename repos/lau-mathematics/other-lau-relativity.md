# lau-relativity

## Intention

A pure-Rust library for special and general relativity — spacetime geometry, Lorentz transformations, relativistic kinematics, energy-momentum, tensor formulation, geodesic integration, gravitational redshift, and cosmology.

## How It Works

`lau-relativity` implements the core mathematical structures of Einstein's relativity as composable Rust modules. From the Minkowski metric and Lorentz boosts of special relativity through the Schwarzschild metric, Christoffel symbols, and geodesic integration of general relativity, to FLRW cosmology and ΛCDM parameters.
Every function is pure (no side effects, no I/O), uses SI units throughout, and is backed by `nalgebra` for the linear algebra. Test coverage includes interval invariance under boosts, energy-momentum relation verification, and Christoffel symbol symmetry.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. A pure-Rust library for special and general relativity — spacetime geometry, Lorentz transformations, relativistic kinematics, energy-momentum, tensor formulation, geodesic integration, gravitational 

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (232 lines), mentions tests, includes examples.

- README length: 333 lines, 12069 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (333 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
