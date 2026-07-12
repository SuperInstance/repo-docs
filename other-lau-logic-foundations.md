# lau-logic-foundations

## Intention

A Rust library for mathematical logic: propositional logic, predicate logic, automated reasoning (DPLL, resolution), natural deduction proofs, Gödel numbering, and agent behavioral contract verification.

## How It Works

`lau-logic-foundations` provides the core machinery of formal logic as composable Rust types and algorithms:
- **Propositional logic** — syntax trees, truth tables, tautology/satisfiability checking, entailment, equivalence.
- **Connectives** — truth-table definitions for all standard binary connectives (AND, OR, IMPLIES, IFF, NAND, NOR, XOR) with commutativity and duality.
- **CNF / DNF conversion** — negation normal form (NNF), distribution-based CNF, and **Tseitin encoding** for linear-size equisatisfiable CNF.
- **DPLL SAT solver** — unit propagation, pure literal elimination, backtracking search.
- **Resolution** — clausal resolution with unification for both propositional and predicate literals.
- **Predicate logic** — terms, quantifiers (∀, ∃), substitution (capture-avoiding), unification, and Robinson's unification algorithm.
- **Natural deduction** — proof terms as a typed λ-calculus (Curry-Howard correspondence) with full type-checking.
- **Gödel numbering** — encode propositional and predicate formulas as natural numbers via prime factorization.
- **Agent reasoning** — behavioral contracts with preconditions/postconditions/invariants, SAT-based consistency checking, safety verification, and knowledge-base queries.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. A Rust library for mathematical logic: propositional logic, predicate logic, automated reasoning (DPLL, resolution), natural deduction proofs, Gödel numbering, and agent behavioral contract verificati

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (156 lines), mentions tests, includes examples.

- README length: 223 lines, 10537 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
