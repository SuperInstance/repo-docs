# lau-thermal-rl

## Intention

Kimi's Theorem 5: KL-regularized RL as Helmholtz free energy, Fisher metric as thermodynamic metric, temperature as exploration parameter

## How It Works

This crate implements a thermodynamic interpretation of KL-regularized reinforcement learning. The central insight (Kimi's Theorem 5) is that the standard KL-regularized RL objective is *exactly* the Helmholtz free energy from statistical mechanics:
```
J(θ) = E[Σ γᵗ rₜ] − β D_KL(Π_θ ‖ Π_ref)  ≡  F = U − TS
```
The crate provides:
- **Free energy objectives** mapping reward + KL penalty to internal energy + TS
- **Fisher information metric** as the thermodynamic (Riemannian) metric on policy space
- **Natural gradient** descent using the Fisher metric as a covariant derivative
- **LQR cost as Fisher geodesic energy** — classical control connects to information geometry
- **Temperature scheduling** with multiple annealing strategies (linear, exponential, cosine, inverse-sqrt)
- **Phase transition detection** — the explore/exploit boundary is a thermodynamic phase transition with a critical temperature T_c
- **Thermodynamic integration** via path integrals for policy evaluation
- **Entropy production tracking** — the second law applied to policy optimization
- **Thermal (Boltzmann) policies** parameterized by temperature
- **PLATO fleet agents** — multi-agent RL with fleet-wide thermodynamic coordination

## What It's For

Kimi's Theorem 5: KL-regularized RL as Helmholtz free energy, Fisher metric as thermodynamic metric, temperature as exploration parameter

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (226 lines), includes examples.

- README length: 311 lines, 11455 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (311 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
