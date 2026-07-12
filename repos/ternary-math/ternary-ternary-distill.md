# ternary-distill

**GitHub**: <https://github.com/SuperInstance/ternary-distill>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 15KB |
| Created | 2026-06-06 |
| Last Push | 2026-06-13 |

## Description

Knowledge distillation for ternary networks. Teacher speaks in probabilities, student answers in trits. Soft targets, KL divergence, gradual ternarization.

## Intention

**Ternary Distill** compresses knowledge from a full-precision teacher network into ternary student weights {-1, 0, +1}. It implements temperature-scaled softmax distillation, blends soft teacher targets with hard labels, and converts the result to ternary votes via threshold-based quantization. The KL divergence between teacher and student distributions is tracked to measure distillation quality.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-distill) for technical details.

## What It's For

Three-valued logic applied to knowledge distillation for ternary networks.

## Who Would Use It

Researchers and developers in the SuperInstance ternary ecosystem.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (15KB). Created 2026-06-06, last push 2026-06-13. 0 stars — no community adoption.

## Honest Assessment

Adequately documented (581 words, 15KB). Part of the burst-created ternary ecosystem. Appears genuine but produced at scale.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
