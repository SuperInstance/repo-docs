# ternary-experiment

**GitHub**: <https://github.com/SuperInstance/ternary-experiment>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 12KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-13 |

## Description

Experiment runner — sweep parameters, run instances, collect results

## Intention

**Ternary Experiment** is a zero-dependency experiment runner for ternary agent simulations. It sweeps parameters (tunnel rate, trap rate, forgiveness, population size, ticks), runs stochastic simulations with seeded RNGs, and collects metrics (γ, entropy, survival rate, dwell time, flip rate) — all without external frameworks or abstractions.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-experiment) for technical details.

## What It's For

Three-valued logic applied to experiment runner — sweep parameters.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (12KB). Created 2026-06-05, last push 2026-06-13. 0 stars — no community adoption.

## Honest Assessment

Adequately documented (577 words, 12KB). Part of the burst-created ternary ecosystem. Appears genuine but produced at scale.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
