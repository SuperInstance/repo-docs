# ternary-tnn

**GitHub**: <https://github.com/SuperInstance/ternary-tnn>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 1 |
| Size | 36KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-14 |

## Description

Ternary Neural Network layers: {-1,0,+1} weights with LUT matmul, straight-through estimation, and BitNet-style 1.58-bit quantization

## Intention

Ternary neural network layers for Rust. Weights live in {-1, 0, +1}. The forward pass does no floating-point multiplications — only additions, subtractions, and skips.
This is the layer-primitive crate behind the BitNet b1.58 idea: quantize float weights to trits at training time, run inference with integer arithmetic, dequantize once per output neuron with a single scale multiply. Microsoft's 2024 paper showed this matches float16 quality at scale. This crate gives you the building blocks.
---

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-tnn) for technical details.

## What It's For

Ternary neural network building blocks — quantized ML with {-1, 0, +1} weights for memory-efficient inference.

## Who Would Use It

ML researchers and engineers building ternary/quantized neural networks (BitNet 1.58-bit style).

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (36KB). Created 2026-06-05, last push 2026-06-14. 1 star(s).

## Honest Assessment

Adequately documented (740 words, 36KB). Part of the burst-created ternary ecosystem. Appears genuine but produced at scale.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
