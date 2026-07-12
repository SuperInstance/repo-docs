# lau-matrix-analysis

## Intention

A Rust library for matrix analysis: decompositions (LU, QR, Cholesky, SVD, eigendecomposition), matrix norms, perturbation theory, structured matrices, Kronecker products, matrix functions (exp, log, sqrt, pow), sparse matrices, and agent similarity analysis — built on `nalgebra`.

## How It Works

`lau-matrix-analysis` provides the core algorithms of numerical linear algebra as pure functions operating on `nalgebra::DMatrix<f64>`:
- **Decompositions** — LU with partial pivoting, QR via modified Gram-Schmidt, Cholesky, SVD via deflation, eigendecomposition (symmetric: Jacobi; general: QR iteration), linear system solving.
- **Norms** — Frobenius, operator (spectral), nuclear, 1-norm, ∞-norm, condition number, trace, rank.
- **Perturbation theory** — Eigenvalue condition numbers, Bauer-Fike bound, Weyl's inequality, element-wise eigenvalue sensitivity.
- **Positive definite matrices** — PD/PSD verification, nearest PSD matrix (Higham's algorithm), eigenvalue range reporting.
- **Sparse matrices** — COO format with sparse-dense and sparse-vector multiplication.
- **Kronecker products** — ⊗ product, mixed-product verification, Kronecker sum.
- **Matrix functions** — Exponential (eigendecomposition & Padé with scaling-and-squaring), logarithm, square root, arbitrary real powers — all via spectral decomposition.
- **Structured matrices** — Toeplitz, symmetric Toeplitz, circulant (with structured multiply), Vandermonde (with determinant), Hankel.
- **Agent analysis** — Spectral clustering on similarity matrices, Gaussian (RBF) kernel, diversity metrics.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. A Rust library for matrix analysis: decompositions (LU, QR, Cholesky, SVD, eigendecomposition), matrix norms, perturbation theory, structured matrices, Kronecker products, matrix functions (exp, log, 

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (186 lines), mentions tests, includes examples.

- README length: 255 lines, 11206 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
