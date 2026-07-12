# ecc-rs

## Intention
**Error-correcting codes in Rust. When your data has to survive the real world.**

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
When bits travel through a noisy channel, some flip. Error-correcting codes add structured redundancy so the receiver can detect *and fix* errors. This library implements the full classical stack:

- **Parity codes** — single-bit error detection
- **Hamming codes** — single-error correction, double-error detection
- **Linear codes** — generator matrices, parity-check matrices, minimum distance, sy

## Who Would Use It
```toml
[dependencies]
ecc-rs = "0.1"
```

Requires **Rust 2021 edition**. Dependencies: `serde`, `nalgebra`.

---

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (248 line README).

## Honest Assessment
Well-documented (248 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/ecc-rs](https://github.com/SuperInstance/ecc-rs)*
