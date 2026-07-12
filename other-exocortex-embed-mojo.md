# exocortex-embed-mojo

## Intention
**SIMD-accelerated embedding operations for the exocortex — proving Mojo's explicit hardware parallelism makes vector math fast at bare metal.**

## How It Works
```
src/exocortex_embed/
├── __init__.mojo      # Module exports
├── vector.mojo        # SIMD vector ops: dot, norm, cosine, euclidean, add, scale, normalize
├── matrix.mojo        # Matrix multiply (with B^T pre-transpose for cache locality), transpose
├── random_proj.mojo   # JL transform via Gaussian random matrix (LCG + CLT)
├── index.mojo         # Brute-force vector index with top-k cosine search
└── quantize.mojo      # Scalar quantization: f64 → i8 with per-dim min/max fitting
```

Data

## What It's For
The exocortex needs fast embedding operations. Not "fast enough for a prototype" — **fast**. The kind of fast where the CPU's vector units are fully utilized and the memory controller is the bottleneck, not the code.

Most embedding libraries are written in C++ or CUDA and called from Python via FFI. That works, but it introduces:

- **Abstraction overhead**: NumPy → BLAS → kernel launches, each l

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Mojo

## Status Assessment
Documented with code examples and API references (818 line README).

## Honest Assessment
Well-documented (818 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/exocortex-embed-mojo](https://github.com/SuperInstance/exocortex-embed-mojo)*
