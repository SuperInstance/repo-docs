# ternary-priority-queue

**GitHub**: <https://github.com/SuperInstance/ternary-priority-queue>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 16KB |
| Created | 2026-06-06 |
| Last Push | 2026-06-13 |

## Description

Priority queue for GPU kernel scheduling with ternary scoring. {-1=deprioritize, 0=normal, +1=prioritize}. O(1) classify, O(log n) ordering.

## Intention

A priority queue for GPU kernel scheduling that combines **O(1) ternary classification** with **O(log n) exact ordering**. Each job is scored on the ternary scale `{-1 = deprioritize, 0 = normal, +1 = prioritize}`, then refined by an exact integer priority and submission time for stable, deterministic dequeue order.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-priority-queue) for technical details.

## What It's For

GPU optimization for ternary kernels — memory packing, scheduling, and dispatch.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (16KB). Created 2026-06-06, last push 2026-06-13. 0 stars — no community adoption.

## Honest Assessment

Adequately documented (792 words, 16KB). Part of the burst-created ternary ecosystem. Appears genuine but produced at scale.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
