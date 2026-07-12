# ga-core

## Intention
Geometric algebra lets you do 3D math without matrices. Rotors don't gimbal lock. Reflections compose into rotations. The geometric product unifies dot products and cross products into one operation.

## How It Works
Geometric algebra lets you do 3D math without matrices. Rotors don't gimbal lock. Reflections compose into rotations. The geometric product unifies dot products and cross products into one operation.

This crate implements Cl(3,1) — the spacetime algebra of 4D spacetime (3 space + 1 time dimension), plus conformal embedding for unified treatment of points, lines, planes, and spheres.

```rust
use ga_core::*;
```

---

## What It's For
| Problem | Traditional | Geometric Algebra |
|---------|------------|-------------------|
| Rotate a vector | 3×3 matrix or quaternion | `R v R̃` |
| Compose rotations | Matrix multiply or q×q | Rotor compose (same thing, cleaner) |
| Gimbal lock | Euler angles break | Rotors never lose a degree of freedom |
| Dot product | `a·b` | `½(ab + ba)` scalar part |
| Cross product | `a×b` (only in 3D!)

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (388 line README).

## Honest Assessment
Well-documented (388 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/ga-core](https://github.com/SuperInstance/ga-core)*
