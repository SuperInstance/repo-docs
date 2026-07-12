# dynamical-systems

## Intention
Dynamical systems in Rust. Bifurcations, stability, and the geometry of change.

## How It Works
The library builds from primitives upward:

1. **Continuous systems** implement `ContinuousSystem` with a vector field f(x,t) and optional analytic Jacobian. The RK4 integrator steps forward with classical 4th-order accuracy.

2. **Discrete systems** implement `DiscreteSystem` with a step function. The `iterate` function accumulates trajectories.

3. **Fixed-point analysis** uses the Jacobian at a point to compute eigenvalues. For continuous systems, stability depends on the sign of the real par

## What It's For
| Module | What you get |
|---|---|
| `continuous` | Trait for ODE systems, RK4 integrator, Lorenz system, Lotka-Volterra predator-prey |
| `discrete` | Trait for iterated maps, logistic map, Hénon map |
| `fixed_points` | Find fixed points via Newton's method; classify stability (Stable/Unstable/Saddle/Marginal) via eigenvalue analysis |
| `bifurcation` | Bifurcation diagrams for logistic map & c

## Who Would Use It
```toml
[dependencies]
dynamical-systems = { git = "https://github.com/SuperInstance/dynamical-systems" }
```

Requires Rust 2021 edition. Dependencies: `nalgebra` 0.33, `num-complex` 0.4, `serde` 1.

---

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (307 line README).

## Honest Assessment
Well-documented (307 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/dynamical-systems](https://github.com/SuperInstance/dynamical-systems)*
