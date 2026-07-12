# ternary-spreadsheet-c

**GitHub**: <https://github.com/SuperInstance/ternary-spreadsheet-c>

| Field | Value |
|-------|-------|
| Language | C |
| Stars | 0 |
| Size | 21KB |
| Created | 2026-06-04 |
| Last Push | 2026-06-13 |

## Description

Ternary spreadsheet engine in C. Minimal footprint Z₃ cell computation for embedded targets.

## Intention

A **ternary spreadsheet** is a grid where each cell holds a balanced ternary value (−1, 0, +1) and optional formulas (SUM, PRODUCT, THRESHOLD) over rectangular ranges. This C library provides grid creation, formula evaluation with topological dependency ordering, fitness-based sorting, and mutation-based autofill.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-spreadsheet-c) for technical details.

## What It's For

Three-valued logic applied to ternary spreadsheet engine in c.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**C** — Rust crate published to crates.io. C implementation for embedded/bare-metal targets.

## Status Assessment

Typical crate (21KB). Created 2026-06-04, last push 2026-06-13. 0 stars — no community adoption.

## Honest Assessment

Adequately documented (780 words, 21KB). Part of the burst-created ternary ecosystem. Appears genuine but produced at scale.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
