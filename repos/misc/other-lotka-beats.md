# lotka-beats

## Intention

🦁 Generative music via Lotka-Volterra dynamics — genres compete, fusion genres emerge at equilibrium

## How It Works

```
┌─────────────────────────────┐
│      MusicEcosystem          │
│ (species list, time, dt,     │
│  history of snapshots)        │
└──────────┬──────────────────┘
│
┌────────────────┼──────────────────┐
│                │                  │
┌─────────▼──────┐ ┌──────▼──────┐ ┌────────▼───────┐
│ MusicalSpecies │ │LotkaVolterra│ │ Equilibrium    │
│ (name, scale,  │ │ (RK4 solver │ │ Analysis       │
│  rhythm, timbre│ │  for dN/dt) │ │ (fixed points, │
│  growth, death,│ │             │ │  stability,    │
│  interaction)  │ │             │ │  genre names)  │

## What It's For

🦁 Generative music via Lotka-Volterra dynamics — genres compete, fusion genres emerge at equilibrium

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (219 lines), includes examples.

- README length: 287 lines, 9440 characters
- Documented sections: The Problem, The Key Insight, Architecture, The Math: Generalized Lotka-Volterra, Quick Start

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (287 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
