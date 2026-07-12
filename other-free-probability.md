# free-probability

## Intention
**Free probability in Rust. The only implementation in any systems language. Random matrices meet operator algebras.**

## How It Works
Models N individuals as random matrices — as N → ∞, collective behavior converges to a free probability distribution.

```rust
let model = AgentPopulationModel::new(1000, vec![0.0, 1.0]);
let limiting = model.limiting_distribution();
let moments = model.collective_moments(6);
let entropy = model.collective_entropy(100, 3.0);
```

---

## What It's For
When random matrices get large enough, their eigenvalues stop being random in the usual sense — they converge to deterministic distributions governed by **free probability**. The free CLT says sums of freely independent operators converge to the semicircle law, just as the classical CLT gives the Gaussian. This crate implements the full mathematical toolkit.

You get:
- **Non-crossing partitions**

## Who Would Use It
```toml
[dependencies]
free-probability = "0.1"
```

Requires Rust 2021 edition.

---

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (243 line README).

## Honest Assessment
Well-documented (243 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/free-probability](https://github.com/SuperInstance/free-probability)*
