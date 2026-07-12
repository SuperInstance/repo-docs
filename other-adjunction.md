# adjunction

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/adjunction](https://github.com/SuperInstance/adjunction)

## Intention

Category theory adjunctions for agent composition

## How It Works

Decisions

### Concrete over Abstract

Every type in this crate operates on real data:

- **Lists** (`Vec<i32>`, `Vec<String>`) for monoid elements
- **Graphs** (`Graph` with vertex count + edge list) for categories
- **Group presentations** (generators as `Vec<String>`, relations as word pairs)

There are no `impl Functor` traits, no HKT bounds, no associated types. You call methods on structs and get answers back. This is intentional: abstract category theory frameworks exist (and are beautiful), but they're hard to learn from and harder to debug.

### Why Function Fields Are `Box<dyn Fn>`



## What It's For

Category theory adjunctions for agent composition

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (426 lines, 18755 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# adjunction

**Category theory adjunctions for agent composition** — concrete implementations of free, forgetful, and reflective functors using actual mathematical objects.

[![crate](https://img.shields.io/crates/v/adjunction.svg)](https://crates.io/crates/adjunction)
[![docs](https://docs.rs/adjunction/badge.svg)](https://docs.rs/adjunction)

---

## Table of Contents

- [Overview](#overview)
- [Theory](#theory)
  - [What is an Adjunction?](#what-is-an-adjunction)
  - [The Triangle Identities](#the-triangle-identities)
  - [Free ⊣ Forgetful](#free--forgetful)
  - [Reflective Subcategories](#reflective-subcategories)
- [Modules](#modules)
- [Design Decisions](#design-decisions)
- [Examples](#examples)
  - [Example 1: Free Monoid Adjunction](#example-1-free-monoid-adjunction)
  - [Example 2: Path Category from a Graph](#example-2-path-category-from-a-graph)
  - [Example 3: Abelianization of a Group](#example-3-abelianization-of-a-group)
- [ASCII Reference](#ascii-reference)
- [API Reference](#api-reference)
- [References](#references)
- [License](#license)

---

## Overview

`adjunction` is a Rust library that provides **concrete, computational** implementations of fundamental category theory constructs. Rather than abstract trait hierarchies that are impossible to debug, every type here operates on real mathematical objects: lists, graphs, group presentations as `Vec<String>`.

This crate is designed for:

- **Agent composition frameworks** where functors represent transformations between agent domains
- **Mathematics education** — see the theory actually compute
- **Formal verification** — triangle identities are checked, not assumed
- **Anyone who wants category theory they can run, not just read about**

### What's Inside

| Module | What It Does | Key Types |
|--------|-------------|-----------|
| `adjunction` | Core struct with triangle identity verification | `Adjunction<A, B>`, `VerificationResult` |
| `unit` | Unit natural transformations η: 1 → R∘L | `Unit<A, B>`, `Morphism` |
| `counit` | Counit natural transformations ε: L∘R → 1 | `Counit<B>`, `ListMonoid`, `Graph` |
| `free` | Free functor implementations | `FreeMonoid`, `FreeCategory` |
| `forgetful` | Forgetful functor implementations | `ForgetMonoid`, `ForgetCategory` |
| `reflective` | Reflective subcategory: abelianization | `GroupPresentation`, `Abelianization` |

---

## Theory

### What is an Adjunction?

An **adjunction** is one of the most important structures in category theory. Given categories **C** and **D**, an adjunction F ⊣ G consists of:

1. A **left adjoint** functor F: C → D
2. A **right adjoint** functor G: D → C
3. A **unit** natural transformation η: 1_C → G∘F
4. A **counit** natural transformation ε: F∘G → 1_D

The fundamental idea: F and G are "approximately inverse" to each other, and η and ε measure exactly how close they come to being true inverses.

Formally, an adjunction can be defined in three equivalent ways (Mac Lane, Ch. IV):

1. **Via natural tran
```
