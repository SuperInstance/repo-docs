# lau-number-theory

## Intention

Algebraic and analytic number theory in pure Rust — prime generation and testing, modular arithmetic, arithmetic functions (Euler's totient, Möbius, divisor sums, Riemann zeta), continued fractions, quadratic residues, Diophantine equations (linear + Pell's), Dirichlet characters and L-functions, an

## How It Works

This library covers the core of computational number theory:
- **Primes** — Sieve of Eratosthenes, trial division, deterministic Miller-Rabin (12 witnesses, correct for all u64), prime factorization, modular exponentiation (overflow-safe), nth prime, prime counting function π(n).
- **Modular arithmetic** — Extended Euclidean algorithm, modular inverse, Chinese Remainder Theorem (CRT), Tonelli-Shanks modular square root, modular add/sub/mul.
- **Arithmetic functions** — Euler's totient φ(n) (single + sieve), Möbius function μ(n) (single + linear sieve), divisor count d(n), divisor sum σ(n) (overflow-safe u128 variant), Riemann zeta ζ(s) via Euler product, Mertens function M(n), gcd, lcm.
- **Continued fractions** — CF expansion of √n (periodic part extraction), convergent computation (h/k pairs), rational CF expansion, period length.
- **Quadratic residues** — Legendre symbol (a/p), Jacobi symbol (a/n), Kronecker symbol (a/n), quadratic residue testing, enumeration of all QRs mod p.
- **Diophantine equations** — Linear Diophantine solver (particular + general parameterized solution), Pell's equation x²−Dy²=1 (fundamental solution via continued fractions), negative Pell x²−Dy²=−1, nth Pell solution via exponentiation in ℤ[√D].
- **Dirichlet characters & L-functions** — Principal and Legendre characters, L(s,χ) evaluation for real and complex s, custom Complex type with arithmetic ops.
- **Agent IDs** — Cryptographic agent identifiers from strong primes, deterministic generation, verification via factorization and totient checking, CRT-based agent namespaces, multi-agent hashing.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Algebraic and analytic number theory in pure Rust — prime generation and testing, modular arithmetic, arithmetic functions (Euler's totient, Möbius, divisor sums, Riemann zeta), continued fractions, q

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (229 lines), mentions tests, includes examples.

- README length: 333 lines, 12563 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (333 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
