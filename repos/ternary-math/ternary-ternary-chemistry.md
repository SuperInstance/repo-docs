# ternary-chemistry

**GitHub**: <https://github.com/SuperInstance/ternary-chemistry>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 13KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-11 |

## Description

Chemistry for ternary {-1, 0, +1} systems — `Species`, `Reaction`, `ReactionNetwork`

## Intention

**Chemical reaction networks where concentrations are {-1, 0, +1}. Catalysts, equilibrium, and mass conservation — in discrete algebra, not differential equations.** In classical chemistry, you model reactions with systems of ordinary differential equations. Concentrations are real-valued, reaction rates are continuous, and equilibrium is a fixed point of the ODE. This crate asks: what happens when every concentration is clamped to one of three values — negative, neutral, or positive? The answer turns out to be surprisingly rich. You get discrete reaction dynamics that always converge (the state space is finite), conservation laws that you can check in O(n), and catalysis...

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-chemistry) for technical details.

## What It's For

Three-valued logic applied to chemistry for ternary {-1.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (13KB). Created 2026-06-05, last push 2026-06-11. 0 stars — no community adoption.

## Honest Assessment

Well-documented (1061 words, 13KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
