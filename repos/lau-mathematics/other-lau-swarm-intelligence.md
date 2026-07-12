# lau-swarm-intelligence

## Intention

Swarm intelligence algorithms: ACO, PSO, bee algorithm, firefly, wolf pack, bacterial foraging, SDS, and flocking (Boids)

## How It Works

| Algorithm | Problem Type | Key Struct |
|---|---|---|
| **Ant Colony Optimization** (ACO) | Combinatorial — Travelling Salesman | `AntColonyOptimization` |
| **Particle Swarm Optimization** (PSO) | Continuous optimisation | `ParticleSwarmOptimization` |
| **Bee Algorithm** | Continuous optimisation | `BeeAlgorithm` |
| **Firefly Algorithm** | Continuous optimisation | `FireflyAlgorithm` |
| **Wolf Pack Algorithm** | Continuous optimisation | `WolfPackAlgorithm` |
| **Bacterial Foraging Optimization** (BFO) | Continuous optimisation | `BacterialForaging` |
| **Stochastic Diffusion Search** (SDS) | Continuous optimisation | `StochasticDiffusionSearch` |
| **Flocking (Boids)** | Emergent-behaviour simulation | `Flocking` |
| **Agent Swarm** | Role-based flocking coordination | `AgentSwarm` |
Every optimiser accepts a closure `Fn(&[f64]) -> f64` (minimisation) and returns a typed result struct carrying the best solution, fitness history, and algorithm-specific diagnostics. All configs and results derive `Serialize` / `Deserialize`.
---

## What It's For

Swarm intelligence algorithms: ACO, PSO, bee algorithm, firefly, wolf pack, bacterial foraging, SDS, and flocking (Boids)

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (202 lines), mentions tests, includes examples.

- README length: 275 lines, 11658 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (275 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
