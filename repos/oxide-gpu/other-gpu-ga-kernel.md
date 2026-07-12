# gpu-ga-kernel

## Intention
**CUDA geometric algebra kernels — Cl(3,1) multivector operations, rotor compositions, and conformal embeddings running on GPU.**

## How It Works
Part of the SuperInstance ecosystem:

- **ga-core** — Rust geometric algebra library
- **gpu-ga-kernel** — CUDA geometric algebra kernels (this repo)

## What It's For
- **Geometric product** — full Cl(3,1) multivector multiplication on GPU
- **Rotor operations** — compose, normalize, apply (sandwich product)
- **Conformal embeddings** — Euclidean 3D points → conformal space
- **Batch processing** — transform millions of points per kernel launch
- **Benchmarking** — throughput measurements for all operations

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Cuda

## Status Assessment
Has some documentation (46 lines).

## Honest Assessment
Minimal documentation (46 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/gpu-ga-kernel](https://github.com/SuperInstance/gpu-ga-kernel)*
