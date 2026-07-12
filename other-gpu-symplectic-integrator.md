# gpu-symplectic-integrator

## Intention
**CUDA symplectic integrators for N-body gravitational systems — Euler, Störmer-Verlet, and 4th-order Yoshida with energy and angular momentum conservation tracking.**

## How It Works
Part of the SuperInstance ecosystem:

- **gpu-sheaf-laplacian** — CUDA sheaf Laplacian
- **gpu-symplectic-integrator** — CUDA symplectic N-body (this repo)

## What It's For
- **Symplectic Euler** — 1st order, preserves phase space volume
- **Störmer-Verlet** — 2nd order, time-reversible, excellent energy conservation
- **Yoshida 4th order** — composed integrator with minimal energy drift
- **Batch integration** — N_sim independent N-body systems in parallel
- **Energy & angular momentum tracking** — GPU parallel reduction
- **Benchmarking suite** — throughput compari

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Cuda

## Status Assessment
Documented with code examples and API references (58 line README).

## Honest Assessment
Has documentation (58 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/gpu-symplectic-integrator](https://github.com/SuperInstance/gpu-symplectic-integrator)*
