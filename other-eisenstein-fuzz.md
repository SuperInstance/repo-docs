# eisenstein-fuzz

## Intention
**Domain:** constraint-theory **Depends on:** — **Depended by:** — **Implements:** Property-based fuzzing for Eisenstein integers — prove the zero-drift claim **Related:** —

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Six fuzz targets, each probing a different structural property of Eisenstein integers. Each target runs with libfuzzer behind it, generating novel inputs through coverage-guided mutation.

**`rotation_identity`** — Rotating `(a,b) → (-b, a+b)` six times must return the original. This is the D₆ rotational symmetry of the hexagonal lattice. Break this and the whole coordinate system is wrong.

**`no

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Claims production-ready with tests and documentation.

## Honest Assessment
Moderately documented (108 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/eisenstein-fuzz](https://github.com/SuperInstance/eisenstein-fuzz)*
