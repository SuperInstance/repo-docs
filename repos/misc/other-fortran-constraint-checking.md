# fortran-constraint-checking

## Intention
**High-performance multi-language constraint checking** — Fortran core with Python, Rust, and C bindings, optimized for AMD Zen 5 / AVX-512 auto-vectorization.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Fortran auto-vectorizes better than C for constraint checking because:

1. **No pointer aliasing by default** — the compiler can freely reorder and SIMD-ify array operations
2. **Array-first semantics** — whole-array operations map directly to SIMD instructions
3. **Intrinsics like `count()`** — compiler emits `vpcmpq + vpopcntdq` without manual intrinsics
4. **Proven in HPC** — decades of numeric

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Fortran

## Status Assessment
Documented with code examples and API references (325 line README).

## Honest Assessment
Well-documented (325 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/fortran-constraint-checking](https://github.com/SuperInstance/fortran-constraint-checking)*
