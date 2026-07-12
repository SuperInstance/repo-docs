# lau-solid-mechanics

## Intention

Continuum mechanics library — stress, strain, deformation, beam mechanics, FEM basics, and yield criteria for solids

## How It Works

This crate implements the fundamentals of solid and structural mechanics:
- **Stress and strain tensors** — Cauchy stress tensor and infinitesimal strain tensor as symmetric 3×3 matrices, with hydrostatic/deviatoric decomposition, principal values, invariants, traction vectors, and normal/shear stress on arbitrary planes
- **Constitutive relations** — isotropic Hooke's law (stress↔strain, Lamé parameters, shear/bulk moduli), 6×6 Voigt stiffness and compliance matrices, orthotropic elasticity tensor
- **Mohr's circle** — 2D and 3D Mohr's circle construction, stress transformation at arbitrary angles, principal stresses and maximum shear
- **Beam mechanics** — Euler-Bernoulli beam: deflection, bending moment, and shear force for simply-supported and cantilever beams with point loads, UDLs, and moments
- **Finite elements** — 1D bar elements, global stiffness assembly, boundary condition application, displacement solution, element stress recovery, strain energy, equilibrium verification
- **Yield criteria** — von Mises (equivalent stress, yield check, safety factor) and Tresca (maximum shear stress criterion)
- **Plane stress and plane strain** — 2D stress-strain conversion for both conditions, out-of-plane response, 3×3 stiffness matrices
- **Energy methods** — strain energy density (from stress, strain, or both), bar and beam strain energy, Castigliano's theorem for displacements, complementary energy
- **Agent structural analysis** — maps agent architecture components to structural analogies for stress testing, pipeline analysis via FEM, beam-based latency modeling, weakest-component detection, health scoring

## What It's For

Continuum mechanics library — stress, strain, deformation, beam mechanics, FEM basics, and yield criteria for solids

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (235 lines), mentions tests, includes examples, has benchmarks.

- README length: 310 lines, 14863 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (310 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
