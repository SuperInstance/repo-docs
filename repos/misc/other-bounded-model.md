# bounded-model

**Cluster:** rust-misc  
**Language:** Rust  
**Source:** [SuperInstance/bounded-model](https://github.com/SuperInstance/bounded-model)

## Intention

See README.

## How It Works

Decisions

### Why DPLL instead of CDCL?

Modern SAT solvers use Conflict-Driven Clause Learning (CDCL), which adds
learned clauses during search to avoid revisiting conflicts. CDCL solvers
like MiniSat, Glucose, or CaDiCaL can handle millions of clauses.

This crate implements plain DPLL for educational clarity. The algorithm is
easy to understand, verify, and extend. For real-world BMC on large systems,
you'd want to swap in a CDCL solver via a trait or feature flag.

### Why `i32` Literals?

DIMACS CNF format uses signed integers for literals. This is the simplest
representation — no newtyp

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (467 lines, 15564 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# bounded-model

**Bounded model checking with a simple DPLL SAT solver — in pure Rust.**

```
┌─────────────────────────────────────────────────────────┐
│                   bounded-model                         │
│                                                         │
│   Transition System                                     │
│         │                                               │
│         ▼                                               │
│   ┌───────────┐     ┌──────────┐     ┌──────────────┐  │
│   │  system   │────▶│ encoding │────▶│  CNF Formula │  │
│   └───────────┘     └──────────┘     └──────┬───────┘  │
│                                             │           │
│                              ┌──────────────▼────────┐  │
│                              │   DPLL SAT Solver     │  │
│                              │  · Unit Propagation   │  │
│                              │  · Pure Literal Elim  │  │
│                              │  · Backtracking       │  │
│                              └──────────┬────────────┘  │
│                                         │               │
│                              ┌──────────▼────────────┐  │
│                              │  Bounded Checker      │  │
│                              │  k=1, k=2, k=3, ...  │  │
│                              └──────────┬────────────┘  │
│                                         │               │
│                              ┌──────────▼────────────┐  │
│                              │  Counterexample       │  │
│                              │  Trace Extraction     │  │
│                              └───────────────────────┘  │
└─────────────────────────────────────────────────────────┘
```

## What is Bounded Model Checking?

Bounded model checking (BMC) is a formal verification technique that searches
for bugs in finite-state systems by unrolling the transition relation for a
bounded number of steps. At each step count *k*, the system encodes:

1. **Initial state** — where the system starts
2. **Transition relation** — how the system evolves, unrolled *k* times
3. **Negated property** — "does something bad happen by step *k*?"

This produces a propositional formula in conjunctive normal form (CNF), which
is handed to a SAT solver. If the solver finds the formula satisfiable, the
satisfying assignment is a **counterexample** — a concrete execution trace that
reaches a bad state within *k* steps.

### Why "Bounded"?

Traditional model checking explores all reachable states, which can be
astronomically large (the infamous *state explosion problem*). BMC sidesteps
this by only looking *k* steps deep. This makes it:

- **Effective at finding shallow bugs** quickly
- **Scalable** — the encoding grows linearly with *k*
- **Sound but not complete** — if no bug is found within *k* steps, there
  might still be a bug at *k+1*. You can increase *k*, but you can't prove
  the absence of bugs with BMC alone (for that, you'd need *k*-induction or
  interpolation)
```
