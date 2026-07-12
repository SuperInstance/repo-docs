# finite-difference-pde

## Intention
PDE solvers in Rust. Heat, wave, Poisson — discretized and solved.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Finite difference methods for partial differential equations in pure Rust:

| Module | What you get |
|---|---|
| **Finite differences** | 1D/2D uniform grids, central/forward/backward differences, 2nd and 4th order |
| **Heat equation** | Forward Euler (explicit), Backward Euler (implicit), Crank-Nicolson |
| **Wave equation** | Leapfrog, Lax-Wendroff with dissipation, energy conservation trackin

## Who Would Use It
```toml
[dependencies]
finite-difference-pde = "0.1.0"
```

Requires **Rust 2021 edition**.

---

## Language / Stack
Rust

## Status Assessment
Has some documentation (100 lines).

## Honest Assessment
Has documentation (100 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/finite-difference-pde](https://github.com/SuperInstance/finite-difference-pde)*
