# ternary-budget

**GitHub**: <https://github.com/SuperInstance/ternary-budget>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 1 |
| Size | 14KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-13 |

## Description

Ternary budget: resource allocation where items are {-1=over, 0=on-track, +1=under} budget

## Intention

**Resource allocation where every line item is under budget, on track, or over budget — nothing else.**
Traditional budget tracking gives you continuous ratios: 73% spent, 127% spent, 99.8% spent. Your eyes glaze over. You have to squint at numbers to know if things are okay. This crate collapses every line item to one of three states: **+1 (under budget)**, **0 (on track)**, or **-1 (over budget)**. The tolerance is configurable, and the overall budget health reduces to a single ternary value.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-budget) for technical details.

## What It's For

Three-valued logic applied to ternary budget: resource allocation where items are {-1=over.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (14KB). Created 2026-06-05, last push 2026-06-13. 1 star(s).

## Honest Assessment

Well-documented (988 words, 14KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
