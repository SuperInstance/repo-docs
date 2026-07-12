# chern-classes

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/chern-classes](https://github.com/SuperInstance/chern-classes)

## Intention

Characteristic classes for vector bundles — Chern, Pontryagin, Todd classes

## How It Works

[code]

## What It's For

Characteristic classes for vector bundles — Chern, Pontryagin, Todd classes

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (220 lines, 6443 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# chern-classes

> **Characteristic classes for vector bundles — the bridge between geometry and topology.**

[![crates.io](https://img.shields.io/crates/v/chern-classes.svg)](https://crates.io/crates/chern-classes)
[![docs.rs](https://docs.rs/chern-classes/badge.svg)](https://docs.rs/chern-classes)
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![tests](https://img.shields.io/badge/tests-16-passing-green.svg)]()

Computes Chern classes, Pontryagin classes, Todd classes, and related invariants for complex and real vector bundles. Implements the splitting principle for decomposing bundles into line bundles.

---

## Why This Exists

Characteristic classes are the **central tool** of differential topology — they translate geometric information (curvature, connections) into topological invariants (cohomology classes). But working with them typically requires:

- Dense textbooks (Milnor & Stasheff, 300+ pages)
- Symbolic algebra systems (Mathematica, Sage)
- Manual polynomial manipulation

`chern-classes` makes characteristic classes **computable** — a Rust library that handles the polynomial algebra so you can focus on the geometry.

---

## Architecture

```
                    ┌─────────────────────┐
                    │   Vector Bundle E    │
                    │   rank n, type C/R   │
                    └────────┬────────────┘
                             │
              ┌──────────────┼──────────────┐
              │              │              │
     ┌────────▼───┐  ┌──────▼─────┐  ┌─────▼──────────┐
     │ Chern      │  │ Pontryagin │  │ Todd           │
     │ Classes    │  │ Classes    │  │ Class          │
     │ c₁...cₙ   │  │ p₁...pₙ/₂ │  │ td(E)         │
     └────────┬───┘  └──────┬─────┘  └─────┬──────────┘
              │              │              │
              └──────┬───────┘              │
                     │                      │
          ┌──────────▼──────────┐           │
          │ Splitting Principle │◄──────────┘
          │ E → L₁ ⊕ ... ⊕ Lₙ │
          └─────────────────────┘
                     │
          ┌──────────▼──────────┐
          │ Polynomial Ring     │
          │ (add, mul, eval)    │
          └─────────────────────┘
```

---

## Installation

```toml
[dependencies]
chern-classes = "0.1.0"
```

---

## Quick Start

```rust
use chern_classes::{ChernCalculator, Polynomial};

// Chern class of a line bundle with c₁ = 3
let c = ChernCalculator::line_bundle_class(3.0);
// c = 1 + 3x

// Whitney sum: c(E ⊕ F) = c(E) · c(F)
let c1 = ChernCalculator::line_bundle_class(1.0);
let c2 = ChernCalculator::line_bundle_class(2.0);
let total = ChernCalculator::whitney_sum(&c1, &c2);
// (1+x)(1+2x) = 1 + 3x + 2x²
assert!((total.coeff(1) - 3.0).abs() < 0.001);
assert!((total.coeff(2) - 2.0).abs() < 0.001);
```

---

## Usage Examples

### Example 1: Chern Character

```rust
use chern_classes::ChernCalculator;

// Chern character: ch(E) = rank + c₁ + (c₁² - 2c₂)/2
let ch = ChernCalculato
```
