# ctl-model

**Cluster:** rust-misc  
**Language:** Rust  
**Source:** [SuperInstance/ctl-model](https://github.com/SuperInstance/ctl-model)

## Intention

Computation Tree Logic model checking on Kripke structures

## How It Works

Decisions

### Why iterative fixpoints?

Recursive CTL model checking is elegant but dangerous. On a linear chain of n states, the recursive formulation of EF creates n stack frames. At n = 10,000, this overflows even generous stack sizes. Our iterative approach uses O(|S|) heap memory (via HashSet) and O(1) stack space.

### Why only `serde` as a dependency?

Kripke structures and CTL formulas are serializable data types. `serde` is the universal serialization framework in the Rust ecosystem. All other operations (model checking, fixpoint computation, path finding) are implemented from scratc

## What It's For

Computation Tree Logic model checking on Kripke structures

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (648 lines, 22941 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# ctl-model

**Computation Tree Logic (CTL) model checking on Kripke structures.**

A Rust library implementing the classical CTL model checking algorithm with iterative fixpoint computation, counterexample/witness generation, and complexity tracking.

---

## Table of Contents

- [Overview](#overview)
- [Theory](#theory)
  - [Kripke Structures](#kripke-structures)
  - [CTL Syntax and Semantics](#ctl-syntax-and-semantics)
  - [Fixpoint Characterizations](#fixpoint-characterizations)
- [Module Overview](#module-overview)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [Examples](#examples)
  - [Example 1: Mutual Exclusion](#example-1-mutual-exclusion)
  - [Example 2: Traffic Light Controller](#example-2-traffic-light-controller)
  - [Example 3: Communication Protocol](#example-3-communication-protocol)
- [API Reference](#api-reference)
- [Algorithm Details](#algorithm-details)
  - [Iterative Fixpoint Computation](#iterative-fixpoint-computation)
  - [Complexity Analysis](#complexity-analysis)
- [Design Decisions](#design-decisions)
- [ASCII Art: Computation Tree](#ascii-art-computation-tree)
- [References](#references)
- [License](#license)

---

## Overview

Computation Tree Logic (CTL) is a branching-time temporal logic used in formal verification to specify properties of reactive systems. Given a finite-state model (a Kripke structure) and a CTL formula, **model checking** determines whether the formula holds in the model.

This library provides:

- **Kripke structure construction** via a builder pattern
- **CTL formula parsing** with a typed AST and standard Display notation
- **Model checking** using iterative fixpoint algorithms (no recursion — safe for large structures)
- **Counterexample generation** — witness paths when formulas are false
- **Witness generation** — satisfying paths when formulas are true
- **Complexity tracking** — iteration counts per fixpoint operator

The implementation follows the seminal algorithm by Clarke and Emerson (1981), adapted for iterative computation to avoid stack overflow on non-trivial structures.

---

## Theory

### Kripke Structures

A **Kripke structure** is a tuple **M = (S, R, L, S₀)** where:

```
S  = finite set of states
R  ⊆ S × S = total transition relation (every state has ≥1 successor)
L  : S → 2^(AP) = labeling function (which propositions hold in each state)
S₀ ⊆ S = set of initial states
```

The transition relation must be **total**: every state has at least one successor. This ensures every state has at least one infinite path originating from it.

A Kripke structure **unfolds** into an infinite computation tree rooted at each initial state. CTL quantifies over paths in this tree.

### CTL Syntax and Semantics

**Syntax:**

```
φ ::= p | ¬φ | φ₁ ∧ φ₂ | φ₁ ∨ φ₂
    | EX φ | AX φ    -- next
    | EF φ | AF φ    -- eventually
    | EG φ | AG φ    -- globally
    | φ₁ EU φ₂ | φ₁ AU φ₂  -- until
```

**Path quantifiers:**
- **E** — "there exists a path"
- **A** — "for all path
```
