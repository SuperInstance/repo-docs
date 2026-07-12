# lau-math-cuda

## Intention

GPU-accelerated Lau math primitives (CUDA)

## How It Works

```
lau_dispatch.h  (Unified API)
│
lau_dispatch.cu  (Auto-detect GPU)
╱      │      ╲
┌─ CUDA ──┐  │   ┌─ CPU Fallback ─┐
│         │  │   │  (lau-math-c)   │
▼         ▼  ▼   ▼                 │
Matrix    Laplacian  Heat    Agent    Conservation
Ops        Ops     Kernel   Fleet      Ops
(cuBLAS)  (cuSPARSE) (Taylor) (Kernel)  (Atomics)
(cuSOLVER)
```

## What It's For

GPU-accelerated Lau math primitives (CUDA)

## Who Would Use It

Researchers and developers applying advanced mathematics to computation. Those who need formal mathematical structures (algebraic, geometric, topological) in code.

## Language / Stack

- **Primary language:** Cuda
- **Technologies mentioned:** CUDA

## Status Assessment

**Status: MODERATE**

Reasonable README (109 lines), mentions tests, has benchmarks.

- README length: 137 lines, 5486 characters
- Documented sections: GPU Requirements, SM Compatibility Matrix, Memory Budget (RTX 4050 — 7 GB VRAM), Architecture, Modules

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
