# dual-connection

## Intention
**Dual affine connections on statistical manifolds — the geometry behind information.**

## How It Works
```
                        ┌──────────────────┐
                        │   dual-connection │
                        └────────┬─────────┘
                                 │
         ┌───────────┬───────────┼───────────┬───────────┐
         │           │           │           │           │
    ┌────┴────┐ ┌────┴────┐ ┌───┴────┐ ┌────┴────┐ ┌────┴────┐
    │connection│ │  dual   │ │parallel│ │curvature│ │torsion  │
    │         │ │         │ │transport│ │         │ │         │
    │ Point   │

## What It's For
Connections are fundamentally functions Γ(p, k, i, j) → ℝ. The alternative — a trait object or enum — would make it harder to define connections as closures that capture the α parameter. `Rc<dyn Fn>` is the most natural representation.

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (379 line README).

## Honest Assessment
Well-documented (379 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/dual-connection](https://github.com/SuperInstance/dual-connection)*
