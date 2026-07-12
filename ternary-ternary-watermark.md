# ternary-watermark

**GitHub**: <https://github.com/SuperInstance/ternary-watermark>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 13KB |
| Created | 2026-06-06 |
| Last Push | 2026-06-10 |

## Description

Ternary watermarking for neural model provenance. Embed {-1,0,+1} fingerprints in weights that survive quantization. Verify ownership without full access.

## Intention

**Fingerprint neural network weights with {-1, +1} patterns that survive quantization.**
When you train a model for months on expensive hardware, you want to know if someone copied it. Traditional watermarking schemes embed real-valued perturbations in weights — but those get destroyed the moment someone quantizes to INT8 or ternary (BitNet b1.58). This crate takes the opposite approach: embed watermarks that are *already* ternary, so quantization can't remove them.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-watermark) for technical details.

## What It's For

Ternary neural network building blocks — quantized ML with {-1, 0, +1} weights for memory-efficient inference.

## Who Would Use It

Security researchers and cryptographers.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (13KB). Created 2026-06-06, last push 2026-06-10. 0 stars — no community adoption.

## Honest Assessment

Well-documented (1050 words, 13KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
