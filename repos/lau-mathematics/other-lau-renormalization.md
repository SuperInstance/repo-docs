# lau-renormalization

## Intention

Renormalization group theory — RG flows, fixed points, critical exponents, Wilsonian RG, epsilon expansion, universality classes, scaling relations, and real-space RG.

## How It Works

The renormalization group explains why wildly different physical systems behave identically near critical points. Water boiling, magnets losing magnetization, and binary-choice agent populations all follow the same mathematical law. The RG tells you which details matter and which don't — coarse-grain the microscopic description, and most details wash out, leaving only a few "relevant" parameters that determine universal behavior.
You get:
- **Beta functions** — the RG flow equations β(g) = dg/d(ln μ) with Euler and RK4 integrators
- **Fixed point analysis** — Newton's method and scanning for β(g*)=0, stability classification
- **Critical exponents** — ν, α, β, γ, δ, η with scaling relation verification (Rushbrooke, Widom, Fisher, Josephson)
- **Wilsonian RG** — momentum shell integration, effective actions, one-loop flow equations
- **Epsilon expansion** — systematic d=4−ε analysis for O(n) models to O(ε²)
- **Universality classes** — Ising 2D/3D, XY, Heisenberg, Potts, mean-field with exponent registries
- **Scaling relations** — correlation length, order parameter, susceptibility, finite-size scaling
- **Real-space RG** — decimation, Migdal-Kadanoff approximation, critical coupling search
- **Agent RG** — agent populations at different scales, phase transition detection, behavioral universality
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Renormalization group theory — RG flows, fixed points, critical exponents, Wilsonian RG, epsilon expansion, universality classes, scaling relations, and real-space RG.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (319 lines), mentions tests, includes examples.

- README length: 445 lines, 16614 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (445 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
