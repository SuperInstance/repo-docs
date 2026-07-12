# ternary-version

**GitHub**: <https://github.com/SuperInstance/ternary-version>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 12KB |
| Created | 2026-06-06 |
| Last Push | 2026-06-09 |

## Description

Version vectors with ternary comparison for distributed GPU state. Conflict detection, merge, dominance.

## Intention

Version vectors with ternary comparison. Know whether your state is newer, older, or in conflict—instantly.
Distributed systems need to compare state across nodes. With version vectors, the answer is always one of three things: **I'm newer** (+1), **you're newer** (-1), or **we're concurrent** (0). That ternary comparison isn't just convenient—it's the mathematically complete classification. Two version vectors can relate in exactly three ways.
This crate gives you version vectors, ternary comparison, merge (component-wise max), and a `ConflictResolver` that tracks merge history. All in ~170 lines with no dependencies beyond `HashMap`.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-version) for technical details.

## What It's For

GPU optimization for ternary kernels — memory packing, scheduling, and dispatch.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (12KB). Created 2026-06-06, last push 2026-06-09. 0 stars — no community adoption.

## Honest Assessment

Well-documented (949 words, 12KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
