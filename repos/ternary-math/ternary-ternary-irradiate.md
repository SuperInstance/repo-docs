# ternary-irradiate

**GitHub**: <https://github.com/SuperInstance/ternary-irradiate>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 20KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-11 |

## Description

Ternary irradiation: radiation damage, cascade simulation, annealing, defect tracking

## Intention

**Radiation and energy propagation on ternary grids. Point sources, inverse-square falloff, diffusion, shadows, and half-life decay.** How does energy spread from a point source across a grid? Inverse-square law says the intensity falls off as 1/r². But on a discrete ternary grid, the continuous function is quantized: at each cell, the irradiance is snapped to {-1, 0, +1} based on configurable thresholds. Energy propagates outward, diffuses into neighbors, decays over time with configurable half-life, and is blocked by shadow-casting obstacles. This crate models all of that: point sources, field computation, diffusion, shadow casting, cascade events (chain reactions where irradiated cells...

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-irradiate) for technical details.

## What It's For

Scientific simulation and physics modeling on ternary state spaces.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (20KB). Created 2026-06-05, last push 2026-06-11. 0 stars — no community adoption.

## Honest Assessment

Adequately documented (606 words, 20KB). Part of the burst-created ternary ecosystem. Appears genuine but produced at scale.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
