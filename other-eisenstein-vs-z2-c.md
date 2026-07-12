# eisenstein-vs-z2-c

## Intention
C benchmark comparing Eisenstein (hexagonal A₂) lattice vs square (Z²) lattice for constraint quantization — snap error, packing density, and convergence rate.

## How It Works
C port of the lattice comparison benchmark:

- eisenstein-vs-z2-rs — Rust version
- eisenstein-triples — Eisenstein triple number theory
- constraint-theory-core — uses A₂ lattice for constraint quantization

## What It's For
- **Dual-lattice snap** — snap points to both Eisenstein and Z² lattices
- **Error comparison** — RMS and max snap error for each lattice
- **Packing analysis** — lattice packing density and covering radius
- **Convergence benchmarks** — how quickly each lattice converges under constraint dynamics
- **Zero dependencies** — pure C99, one header

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
C

## Status Assessment
Documented with code examples and API references (59 line README).

## Honest Assessment
Has documentation (59 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/eisenstein-vs-z2-c](https://github.com/SuperInstance/eisenstein-vs-z2-c)*
