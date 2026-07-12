# ltl-spec

## Intention

Linear Temporal Logic (LTL) specification library for Rust agents

## How It Works

**ltl-spec** is a no-std-compatible (with `serde`) library for working with
Linear Temporal Logic (LTL) formulas in Rust. LTL extends classical
propositional logic with temporal operators that reason about the future
evolution of a system over time.
Originally introduced by Amir Pnueli in 1977 \[1\], LTL has become a
foundational tool in formal verification, model checking, and runtime
monitoring. This library provides:
- **Parsing**: Convert human-readable strings like `G(p -> F(q))` into
structured formula representations.
- **Normalization**: Transform formulas into Negation Normal Form (NNF)
where negation appears only on atoms.
- **Classification**: Determine whether a formula represents a safety
property, a liveness property, or both.
- **Trace Verification**: Check whether an execution trace satisfies an
LTL formula using an iterative (non-recursive) evaluation algorithm.

## What It's For

Linear Temporal Logic (LTL) specification library for Rust agents

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (567 lines), mentions tests, includes examples.

- README length: 747 lines, 22589 characters
- Documented sections: Table of Contents, Overview, Architecture, Theory, Quick Start

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (747 lines) with tests, examples, and benchmarks referenced. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
