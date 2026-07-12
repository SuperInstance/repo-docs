# Constraint Theory

**46 repos** applying geometric constraint satisfaction to real-world problems — CSP solvers, Hamiltonian constraints, Laman rigidity, scheduling, and the unified constraint theory core that solves floating-point drift.

---

## What Is Constraint Theory Here?

Constraint theory is the SuperInstance approach to solving problems not by integrating equations of motion, but by **directly satisfying constraints**. Instead of computing F=ma and accumulating error, you snap values to the nearest configuration that satisfies all constraints exactly.

The flagship library, `constraint-theory-core`, solves the universal problem of **floating-point drift** — the IEEE 754 arithmetic errors that compound over time in physics simulations, multiplayer games, and distributed systems. It uses **Eisenstein integer lattice (A₂)** to snap continuous values to exact discrete coordinates with bounded error.

### Key Principles

1. **Zero drift** — values snap to lattice points, eliminating cumulative error
2. **Geometric satisfaction** — constraints are geometric, not algebraic
3. **Laman rigidity** — structural guarantees borrowed from rigidity theory
4. **Eisenstein lattice** — hexagonal coordinate system with 6-fold symmetry
5. **Constraint DSL** — declarative YAML-like language for constraint graphs

---

## Key Repositories

### Core Theory

| Repo | Language | Description |
|------|----------|-------------|
| [constraint-theory-core](https://github.com/SuperInstance/constraint-theory-core) | Rust | The flagship — solves floating-point drift using Eisenstein lattice A₂. 83 tests, zero dependencies |
| [constraint-theory-math](https://github.com/SuperInstance/constraint-theory-math) | Rust | Mathematical foundations |
| [constraint-theory-research](https://github.com/SuperInstance/constraint-theory-research) | — | Research notes |
| [constraint-theory-papers](https://github.com/SuperInstance/constraint-theory-papers) | — | Papers on constraint theory |
| [constraint-theory-backup](https://github.com/SuperInstance/constraint-theory-backup) | — | Backup of theory work |

### Multi-Language Implementations

| Repo | Language | Description |
|------|----------|-------------|
| constraint-theory-core | Rust | Reference implementation |
| constraint-theory-core-cuda | CUDA | GPU-accelerated constraint solving |
| constraint-theory-py | Python | Python implementation |
| constraint-theory-python | Python | Alternative Python port |
| constraint-theory-rust-python | Rust+Python | Hybrid Rust/Python |
| constraint-theory-llvm | LLVM | LLVM IR compilation |
| constraint-theory-mlir | MLIR | Multi-Level IR |
| constraint-theory-mojo | Mojo | Mojo implementation |
| constraint-theory-engine-cpp-lua | C++/Lua | Embedded engine |
| constraint-theory-ecosystem | — | Ecosystem documentation |
| constraint-theory-web | JavaScript | Web implementation |

### Solvers & Satisfaction

| Repo | Language | Description |
|------|----------|-------------|
| constraint-hamiltonian | Rust | Hamiltonian constraint systems |
| constraint-schedule | Rust | Constraint-satisfaction scheduling |
| constraint-physics | Rust | ZHC constraint-based physics engine — replaces F=ma with direct constraint resolution |
| constraint-dynamics | Rust | Constraint dynamics |
| constraint-dynamics-rs | Rust | Rust dynamics variant |
| constraint-inference | Rust | Inference under constraints |
| constraint-crdt | Rust | CRDTs with constraint awareness |

### DSL & Configuration

| Repo | Language | Description |
|------|----------|-------------|
| constraint-dsl | Python | Declarative YAML-like DSL for constraint graphs |
| constraint-dialect | Python | Dialect for constraint expressions |
| constraint-flow | Rust | Constraint flow protocol |
| constraint-flow-protocol | Rust | Protocol definition |

### GPU & Performance

| Repo | Language | Description |
|------|----------|-------------|
| constraint-gpu-kernels | CUDA | GPU kernels for parallel constraint solving |
| constraint-kernel-verify | Rust | Kernel verification |
| constraint-bench-suite | — | Benchmark suite |
| constraint-mux | Rust | Multiplexer for constraint streams |

### Tools & Visualization

| Repo | Language | Description |
|------|----------|-------------|
| constraint-studio | — | Studio IDE for constraint editing |
| constraint-playground | — | Interactive playground |
| constraint-solver-viz | Python | Visualization tools for constraint solving |
| constraint-viz | — | Visualization utilities |
| constraint-toolkit | — | General toolkit |
| constraint-instrument | — | Instrumentation |

### Applications

| Repo | Language | Description |
|------|----------|-------------|
| constraint-audio | Rust | Audio constraint processing |
| constraint-synth | Rust | Constraint-driven synthesis |
| constraint-ranch | Rust | Constraint ranch (distributed) |
| constraint-snap | Rust | Lattice snapping |
| constraint-substrate | Rust | Constraint substrate |
| constraint-demo | Rust | Demo applications |
| constraint-demos | Rust | Multiple demos |
| constraint-mcp-server | — | MCP server interface |

---

## How It Works: Eisenstein Lattice Snapping

The core insight: instead of representing values as IEEE 754 floats (which introduce drift), represent them as points on the **Eisenstein integer lattice** — a hexagonal grid where:

- **Coordinates** are pairs (a, b) of integers
- **Norm** is N(a,b) = a² − ab + b² (always non-negative)
- **60° rotation** is (-b, a-b) — two subtractions and a negation
- **D₆ symmetry** — all six rotations
- **6.8× denser** than Pythagorean triples at the same norm bound
- **Closed under multiplication** (ring property)

When a computation would introduce drift, the result is **snapped** to the nearest Eisenstein lattice point, bounding error to ≤ √3/3 per operation.

### Comparison with ℤ² (Square Lattice)

The `eisenstein-vs-z2` benchmark rigorously compares hexagonal vs. square lattice snapping for 2D constraint resolution. The hexagonal lattice provides tighter packing and better error bounds.

---

## The Constraint Physics Engine

`constraint-physics` replaces traditional force-integration physics with **Zero-Holonomy Constraint (ZHC)** satisfaction:

| Traditional Physics | ZHC Physics |
|--------------------|-------------|
| Compute forces | Measure constraint violations |
| Integrate F=ma | Resolve violations directly |
| Error accumulates | Error bounded by lattice |
| Needs small timesteps | Constraint-based, timestep-independent |
| 2D, 3D | 2D (3D planned) |

Laman rigidity theory provides structural guarantees — a graph is rigid iff it has 2n−3 edges satisfying the Laman condition. This means the constraint system can prove whether a structure is stable.

---

## The DSL

The constraint DSL is a declarative YAML-like language for defining constraint graphs:

```yaml
constraints:
  - type: bound
    signal: velocity
    lower: 0
    upper: 300
    severity: hard
    
  - type: delta
    signal: velocity
    max_delta: 15
    window: per_frame
    severity: hard
    
  - type: hamiltonian
    energy: total_energy
    tolerance: 0.001
```

---

## Assessment

The constraint theory ecosystem solves a real problem (floating-point drift) with elegant mathematics (Eisenstein lattice). The flagship library has 83 tests and zero dependencies. The multi-language implementations (Rust, CUDA, Python, LLVM, MLIR, Mojo, C++/Lua, Web) show serious commitment to portability.

The physics engine (constraint-based instead of force-integration) is an interesting research direction with real theoretical backing (Laman rigidity). However, it's a research prototype — 2D only, limited collision detection, no broad-phase optimization.

The DSL, studio, playground, and visualization tools form a complete development environment for constraint-based programming.

---

*Individual repo summaries are in `constraint-{repo-name}.md` files in this directory.*
