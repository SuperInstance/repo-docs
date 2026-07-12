# ternary-complexity

**GitHub**: <https://github.com/SuperInstance/ternary-complexity>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 12KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-08 |

## Description

Kolmogorov complexity proxy via LZ77 compression for ternary genomes

## Intention

Kolmogorov complexity proxies for ternary sequences. Compress, measure, compare.
How complex is a ternary sequence? A string of all zeros is trivial—it compresses to nothing. A truly random sequence is incompressible—every symbol carries information. This crate estimates where a sequence falls on that spectrum using three complementary approaches: LZ77 compression ratio, Lempel-Ziv substring counting, and conditional entropy rate. Plus a unique `forgiveness_compression` function that measures how much complexity drops when you replace defection patterns (-1) with neutral (0).

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-complexity) for technical details.

## What It's For

Data compression and encoding for ternary representations.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (12KB). Created 2026-06-05, last push 2026-06-08. 0 stars — no community adoption.

## Honest Assessment

Well-documented (1076 words, 12KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
