# fluid-sim

## Intention
A from-scratch implementation of the **Stam (1999) Stable Fluids** algorithm — a grid-based (Eulerian) fluid solver that is unconditionally stable via a semi-Lagrangian advection scheme. The simulation evolves a velocity field **u** = (u, v) and a density field **ρ** through the Navier–Stokes equations for incompressible flow.

## How It Works
The solver advances the incompressible Navier–Stokes equations:

```
∂u/∂t = -(u·∇)u + ν∇²u - ∇p + f
∇·u = 0
```

Each timestep applies four operators sequentially:

## What It's For
Fluid simulation is the backbone of visual effects, weather modeling, and aerodynamics. The Stable Fluids method was revolutionary because it decoupled simulation stability from timestep size — previous explicit schemes required `dt` small enough to satisfy CFL conditions that made interactive simulation impossible. This implementation demonstrates every core operator in a computational fluid dyna

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (118 line README).

## Honest Assessment
Moderately documented (118 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/fluid-sim](https://github.com/SuperInstance/fluid-sim)*
