# ternary-grad

**GitHub**: <https://github.com/SuperInstance/ternary-grad>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 1 |
| Size | 18KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-13 |

## Description

Ternary gradient descent: straight-through estimator, ternary Adam/SGD optimizers, gradient clipping in trit space, cosine LR scheduling

## Intention

**Ternary gradient descent: the training infrastructure that makes {-1, 0, +1} neural networks learnable.**
You can't backpropagate through `sign(x)` — the gradient is zero almost everywhere (and undefined at 0). The **Straight-Through Estimator** (STE, Bengio et al., 2013) solves this: during the forward pass, quantize latent weights to {-1, 0, +1}. During the backward pass, pretend the quantization didn't happen and pass the gradient through unchanged.
This crate provides STE plus ternary-aware optimizers (SGD, Adam), gradient clipping, learning rate schedules, quantization diagnostics, and weight decay — everything you need to train a ternary neural network from scratch.
---

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-grad) for technical details.

## What It's For

Ternary neural network building blocks — quantized ML with {-1, 0, +1} weights for memory-efficient inference.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (18KB). Created 2026-06-05, last push 2026-06-13. 1 star(s).

## Honest Assessment

Well-documented (1754 words, 18KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
