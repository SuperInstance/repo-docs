# ternary-cipher

**GitHub**: <https://github.com/SuperInstance/ternary-cipher>

| Field | Value |
|-------|-------|
| Language | Rust |
| Stars | 0 |
| Size | 20KB |
| Created | 2026-06-05 |
| Last Push | 2026-06-13 |

## Description

ternary-cipher  Ternary cryptography: one-time pads, Feistel ciphers, commitments, Shamir secre...

## Intention

**Ternary Cipher** implements a complete suite of cryptographic primitives over the finite field **GF(3)** — one-time pads, Feistel ciphers, substitution boxes, hash commitments, Shamir secret sharing, and Merkle trees — all using balanced ternary arithmetic on **T = {−1, 0, +1}**. The crate is `#![no_std]` and `#![forbid(unsafe_code)]`, making it suitable for embedded ternary processors and constrained environments.

## How It Works

Operates within the balanced ternary {-1, 0, +1} algebraic framework. See the [full README](https://github.com/SuperInstance/ternary-cipher) for technical details.

## What It's For

Cryptographic and security applications using ternary arithmetic (Z₃ algebra).

## Who Would Use It

Security researchers and cryptographers.

## Language/Stack

**Rust** — Rust crate published to crates.io. 

## Status Assessment

Typical crate (20KB). Created 2026-06-05, last push 2026-06-13. 0 stars — no community adoption.

## Honest Assessment

Well-documented (1433 words, 20KB) with code examples and mathematical foundations. Created as part of a burst (370 repos in ~10 days) suggesting heavy AI assistance, but the content is domain-specific and internally consistent — a real, if rapidly produced, implementation.

---

*Part of the [SuperInstance ternary ecosystem](https://github.com/SuperInstance) — 370+ crates exploring balanced ternary {-1, 0, +1} computation across ML, physics, economics, music, distributed systems, cryptography, and more. The ecosystem was created in a burst (~June 4-14, 2026), likely with heavy AI assistance, yet contains individually substantive implementations with consistent mathematical foundations: Kleene three-valued logic, Z₃ arithmetic, and the conservation principle γ + η = C.*
