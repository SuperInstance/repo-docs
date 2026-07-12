# ternary-llm

**GitHub**: <https://github.com/SuperInstance/ternary-llm>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 1 |
| Size | 37KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-13 |

## Description

Ternary LLM building blocks: token embeddings, transformer blocks with ternary weights, BitNet 1.58-bit quantization, KV-cache compression

## Intention

BitNet 1.58-bit large language model building blocks in pure Rust. Each weight is stored as a trit ∈ {-1, 0, +1} alongside a single per-tensor float scale, enabling **~20× memory compression** over FP32 with minimal quality loss.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-llm) for technical details.

## What It's For

Data structures and storage optimized for ternary-valued data.

## Who Would Use It

ML researchers and engineers building ternary/quantized neural networks (BitNet 1.58-bit style).

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (37KB). Created 2026-06-05, last push 2026-06-13. 1 star(s).

## Honest Assessment

Adequately documented (709 words, 37KB). Part of the burst-created ternary ecosystem. Appears genuine but produced at scale.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
