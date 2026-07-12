# lau-thermodynamics

## Intention

Classical and statistical thermodynamics — energy, entropy, and equilibrium

## How It Works

| Module | What It Gives You |
|---|---|
| `constants` | R, k_B, N_A, σ, atm, temperature conversions |
| `laws` | All four laws — zeroth (equilibrium transitivity), first (ΔU = Q − W), second (ΔS_universe ≥ 0), third (S → 0 at 0 K) — plus heat capacities for monatomic & diatomic ideal gases |
| `gas` | Ideal gas law (PV = nRT) in all directions, van der Waals equation with built-in parameters for N₂, O₂, CO₂, H₂O, He, compressibility factor Z, Boyle temperature |
| `carnot` | Carnot efficiency, work, heat rejected, COP for refrigerators & heat pumps, full `CarnotCycle` struct, Carnot-limit violation checker |
| `entropy` | Clausius ΔS = Q/T, isothermal/isobaric/isochoric/adiabatic entropy changes, entropy of mixing, Boltzmann S = k_B ln Ω, Gibbs S = −k_B Σ pᵢ ln pᵢ, phase-transition entropy, information entropy |
| `maxwell` | All four Maxwell relations, ideal-gas verification, thermodynamic potential derivatives, isothermal compressibility, thermal expansion coefficient |
| `phase` | Clausius–Clapeyron equation, boiling point vs pressure, triple point & critical point data for water, Gibbs phase rule, phase equilibrium verification |
| `statistical` | Boltzmann factor, canonical partition function Z, internal energy from Z, average energy, Helmholtz free energy, heat capacity from Z, Fermi–Dirac & Bose–Einstein distributions |
| `heat_transfer` | Fourier conduction, thermal resistance (series & parallel), Newton's cooling, Stefan–Boltzmann radiation, Biot & Fourier numbers |
| `agent_budget` | `AgentStep` / `EnergyBudget` for tracking agent compute energy per step, Landauer cost per bit, heat-engine analogy for agent efficiency |
All types derive `Serialize`/`Deserialize`. **76 tests** verify every formula against known values.
---

## What It's For

Classical and statistical thermodynamics — energy, entropy, and equilibrium

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (321 lines), mentions tests, includes examples.

- README length: 435 lines, 16219 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (435 lines) with tests, examples, and benchmarks referenced. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
