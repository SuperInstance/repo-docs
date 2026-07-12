# ternary-auto-vectorizer

**GitHub**: <https://github.com/SuperInstance/ternary-auto-vectorizer>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 23KB |
| Created | 2026-06-06 |
| Last Push | 2026-06-11 |

## Description

Auto-vectorizes scalar Z₃ ternary ops to warp-level parallel versions. Proves equivalence — real compiler optimization for ternary GPU code.

## Intention

A compiler pass that lifts scalar Z₃ ternary dot-threshold kernels to warp-parallel vectorized form, then **formally proves equivalence** by exhaustive enumeration over all 3ⁿ input combinations.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-auto-vectorizer) for technical details.

## What It's For

Compilation tooling and runtime for ternary compute.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (23KB). Created 2026-06-06, last push 2026-06-11. 0 stars — no community adoption.

## Honest Assessment

Well-documented (1126 words, 23KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
