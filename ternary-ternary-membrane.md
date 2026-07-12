# ternary-membrane

**GitHub**: <https://github.com/SuperInstance/ternary-membrane>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 17KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-10 |

## Description

ternary-membrane  Membrane transport dynamics with ternary concentrations

## Intention

Compartment transport dynamics with ternary concentrations. Diffusion, osmosis, active transport, gated channels, and full simulation.
Biological membranes are selective barriers: they let some molecules through, block others, and actively pump against gradients using energy. This crate models that exact mechanism with ternary concentrations {-1, 0, +1}. Compartments hold solute concentrations. Membranes control permeability. Channels provide selective, gated transport. And the simulation engine runs it all forward in discrete steps.
Built for `#![no_std]` with only `alloc`. Runs anywhere you can allocate a `Vec`.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-membrane) for technical details.

## What It's For

Three-valued logic applied to ternary-membrane  membrane transport dynamics with ternary concentrations.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (17KB). Created 2026-06-05, last push 2026-06-10. 0 stars — no community adoption.

## Honest Assessment

Well-documented (1006 words, 17KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
