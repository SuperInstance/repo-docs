# gpu-persistent-homology

## Intention
**CUDA persistent homology — H⁰ and H¹ persistence diagrams, union-find on GPU, Wasserstein distance computation.**

## How It Works
Part of the SuperInstance ecosystem:

- **persistent-sheaf** — Rust persistent sheaf cohomology
- **gpu-persistent-homology** — CUDA persistent homology (this repo)

## What It's For
- **H⁰ persistence** — GPU union-find for connected component tracking across filtration
- **H⁰ persistence** — Loop detection via boundary matrix operations
- **Wasserstein distance** — p-Wasserstein and bottleneck distances between diagrams
- **Distance matrix** — Tiled pairwise Euclidean distances
- **Test suite** — Correctness verification against CPU reference

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Cuda

## Status Assessment
Has some documentation (49 lines).

## Honest Assessment
Minimal documentation (49 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/gpu-persistent-homology](https://github.com/SuperInstance/gpu-persistent-homology)*
