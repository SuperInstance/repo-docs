# logic-foundations

## Intention

Logic foundations in Rust. From propositions to proofs.

## How It Works

`logic-foundations` provides the core machinery of formal logic as composable Rust types and algorithms:
- **Propositional logic** — syntax trees, truth tables, tautology/satisfiability checking, entailment, equivalence.
- **Connectives** — truth-table definitions for all standard binary connectives (AND, OR, IMPLIES, IFF, NAND, NOR, XOR) with commutativity and duality.
- **CNF / DNF conversion** — negation normal form (NNF), distribution-based CNF, and **Tseitin encoding** for linear-size equisatisfiable CNF.
- **DPLL SAT solver** — unit propagation, pure literal elimination, backtracking search.
- **Resolution** — clausal resolution with unification for both propositional and predicate literals.
- **Predicate logic** — terms, quantifiers (∀, ∃), substitution (capture-avoiding), unification, and Robinson's unification algorithm.
- **Natural deduction** — proof terms as a typed λ-calculus (Curry-Howard correspondence) with full type-checking.
- **Gödel numbering** — encode propositional and predicate formulas as natural numbers via prime factorization.

## What It's For

Logic foundations in Rust. From propositions to proofs.

## Who Would Use It

DevOps engineers and system operators needing observability tooling.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (124 lines), includes examples.

- README length: 174 lines, 7291 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
