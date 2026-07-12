# ternary-heap

**GitHub**: <https://github.com/SuperInstance/ternary-heap>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 1 |
| Size | 14KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-11 |

## Description

Ternary min-heap priority queue: 3 children per node, O(log₃ n) push/pop, merge, decrease-key

## Intention

A **ternary min-heap** — each node has up to three children, giving O(log₃ n) `push` and `pop` with O(1) `peek`.
---

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-heap) for technical details.

## What It's For

Data structures and storage optimized for ternary-valued data.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (14KB). Created 2026-06-05, last push 2026-06-11. 1 star(s).

## Honest Assessment

Well-documented (881 words, 14KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
