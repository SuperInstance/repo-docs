# lau-pde-agents

## Intention

Partial differential equations for agent dynamics — numerical solvers for the PDEs that govern how agent beliefs propagate, diffuse, oscillate, and reach equilibrium.

## How It Works

### Grid System
All solvers operate on discretized domains:
- **`Grid1D`** — 1D domain [a, b] with N interior points (uniform spacing)
- **`Grid2D`** — 2D rectangular domain [aₓ, bₓ] × [aᵧ, bᵧ]
Grids store the spacing `dx` (and `dy`) for you, and provide methods to evaluate interior point locations.
### Finite Difference Laplacian
The core building block is `laplacian_1d()`, which constructs the standard tridiagonal second-difference matrix:
```
L = (1/dx²) * [ -2   1   0  ...  0  ]
[  1  -2   1  ...  0  ]
[  0   1  -2  ...  0  ]
[ ...                ... ]
[  0  ...  1  -2   1  ]
[  0  ...  0   1  -2  ]
```

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Partial differential equations for agent dynamics — numerical solvers for the PDEs that govern how agent beliefs propagate, diffuse, oscillate, and reach equilibrium.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (243 lines), mentions tests, includes examples.

- README length: 343 lines, 10835 characters
- Documented sections: Why PDEs for Agents?, Quick Start, Architecture, Solvers in Detail, Theoretical Foundations

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (343 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
