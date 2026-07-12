# eisenstein-vs-z2-rs

## Intention
**Rigorous comparison of hexagonal (Eisenstein) vs square (ℤ²) lattice snapping in Rust.**

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- **`EisensteinInt`** — Eisenstein integer type with arithmetic (add, multiply, conjugate, norm)
- **Lattice snapping** — snap arbitrary 2D points to the nearest Eisenstein or ℤ² lattice point
- **`Benchmark`** — configurable benchmark suite comparing both lattices across sample sizes and trials
- **`ConvergenceAnalysis`** — verify that Eisenstein's advantage holds and converges as sample size gro

## Who Would Use It
Add to your `Cargo.toml`:

```toml
[dependencies]
eisenstein-vs-z2 = { git = "https://github.com/SuperInstance/eisenstein-vs-z2-rs" }
```

Or from source:

```bash
git clone https://github.com/SuperInstance/eisenstein-vs-z2-rs.git
cd eisenstein-vs-z2-rs
cargo build
```

Dependencies: `serde` + `serd

## Language / Stack
Rust

## Status Assessment
Documented with tests, API docs, and installation guide (306 line README).

## Honest Assessment
Well-documented (306 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/eisenstein-vs-z2-rs](https://github.com/SuperInstance/eisenstein-vs-z2-rs)*
