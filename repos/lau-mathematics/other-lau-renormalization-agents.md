# lau-renormalization-agents

## Intention

Wilson's renormalization group applied to agent systems — coarse-graining agent behavior reveals universal structure.

## How It Works

| Module | Concept | What you get |
|---|---|---|
| `agent` | Individual agents and populations | State vectors, interaction matrices, lattice populations |
| `coarse_graining` | Merge agent groups into effective agents | Mean, weighted mean, majority vote, decimation, variance-weighted |
| `effective_hamiltonian` | H_eff = Σ Kᵢ Oᵢ(s_eff) | Coupling constants, beta functions, rescaling |
| `rg_flow` | Trajectory in coupling space under repeated rescaling | Flow steps, convergence detection, flow visualization |
| `operators` | Relevant / irrelevant / marginal perturbations | Eigenvalue classification, scaling dimensions, operator spectra |
| `fixed_points` | K* where R_b(K*) = K* | Gaussian, trivial, Wilson-Fisher; stable / unstable / saddle / critical |
| `kadanoff` | Explicit block-spin transformation | Block averaging, Ising recursion, critical coupling |
| `wilson_rg` | Full Wilson RG pipeline | End-to-end: population → flow → fixed points → universality class |
| `universality` | Universality classes | Ising, XY, Heisenberg, Mean Field + agent-specific: herding, flocking, consensus |
| `epsilon_expansion` | Perturbative RG near d = 4 | Critical exponents (ν, η, γ, α, β, δ) at one-loop and two-loop |
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Wilson's renormalization group applied to agent systems — coarse-graining agent behavior reveals universal structure.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (200 lines), mentions tests, includes examples.

- README length: 290 lines, 12163 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
