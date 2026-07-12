# lau-numerical-linear-algebra

## Intention

Numerical linear algebra — iterative methods, Krylov subspace methods, eigenvalue algorithms, sparse solvers, preconditioners, SVD, and least squares for large-scale agent simulations

## How It Works

This crate gives you a **from-scratch numerical linear algebra toolkit** in pure Rust:
| Category | What you get |
|---|---|
| **Iterative solvers** | Jacobi, Gauss-Seidel, SOR |
| **Krylov subspace** | Conjugate Gradient (CG), GMRES (restarted), BiCGSTAB |
| **Eigenvalue algorithms** | Power iteration, inverse iteration, QR algorithm, Lanczos |
| **Sparse solvers** | COO/CSR storage, sparse CG, sparse triangular solves |
| **Preconditioners** | Jacobi (diagonal), Incomplete Cholesky IC(0), preconditioned CG |
| **SVD** | Full SVD, truncated SVD, randomized SVD |
| **Least squares** | QR-based, SVD-based, normal equations |
| **Condition estimation** | κ(A) from eigenvalues or singular values |
57 unit tests cover correctness, convergence, and edge cases across every module.
---

## What It's For

Numerical linear algebra — iterative methods, Krylov subspace methods, eigenvalue algorithms, sparse solvers, preconditioners, SVD, and least squares for large-scale agent simulations

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (237 lines), mentions tests, includes examples.

- README length: 347 lines, 13925 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (347 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
