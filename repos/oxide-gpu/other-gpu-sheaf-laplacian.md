# gpu-sheaf-laplacian

## Intention
**CUDA sheaf Laplacian computation — distance matrices, CSR adjacency, spectral invariants, and power iteration eigenvalues, all on GPU.**

## How It Works
Part of the SuperInstance ecosystem:

- **persistent-sheaf** — Rust sheaf cohomology
- **gpu-sheaf-laplacian** — CUDA-accelerated sheaf Laplacian (this repo)

## What It's For
- **Tiled distance matrix** — pairwise Euclidean distances via shared-memory tiling
- **CSR adjacency** — epsilon-threshold with Gaussian kernel weights
- **Sheaf Laplacian** — L_F = D - W modified by stalk features
- **Power iteration eigenvalues** — top-k eigenvalues with deflation
- **Spectral invariants** — radius, gap, spread, trace, all on GPU
- **Benchmarking suite** — GPU vs CPU scaling co

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Cuda

## Status Assessment
Has some documentation (54 lines).

## Honest Assessment
Has documentation (54 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/gpu-sheaf-laplacian](https://github.com/SuperInstance/gpu-sheaf-laplacian)*
