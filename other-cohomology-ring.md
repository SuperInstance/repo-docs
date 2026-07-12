# cohomology-ring

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/cohomology-ring](https://github.com/SuperInstance/cohomology-ring)

## Intention

See README.

## How It Works

[code]

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (276 lines, 10219 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# cohomology-ring

> **Cup product. Cohomology operations. The ring structure of H*(X).**

[![crates.io](https://img.shields.io/crates/v/cohomology-ring.svg)](https://crates.io/crates/cohomology-ring)
[![docs.rs](https://docs.rs/cohomology-ring/badge.svg)](https://docs.rs/cohomology-ring)
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

A Rust library for computing cohomology rings and cohomology operations. Implements cochain complexes, cup product (giving cohomology its multiplicative ring structure), Bockstein homomorphism, and Steenrod squares. Distinguishes spaces that homology alone cannot — the algebraic structure that makes cohomology strictly more powerful than homology.

---

## Table of Contents

- [What is a Cohomology Ring?](#what-is-a-cohomology-ring)
- [Why Does This Matter?](#why-does-this-matter)
- [Architecture](#architecture)
- [Quick Start](#quick-start)
- [API Reference](#api-reference)
- [Mathematical Background](#mathematical-background)
- [Installation](#installation)
- [Related Crates](#related-crates)
- [License](#license)

---

## What is a Cohomology Ring?

**Cohomology** assigns to each topological space X a sequence of groups H⁰(X), H¹(X), H²(X), ... that capture the space's structure. But cohomology is more than groups — it's a **graded ring**.

The **cup product** ∪: Hᵏ × Hˡ → Hᵏ⁺ˡ gives cohomology a multiplicative structure:

```
α ∈ Hᵏ(X),  β ∈ Hˡ(X)  →  α ∪ β ∈ Hᵏ⁺ˡ(X)
```

This ring structure is a strictly stronger invariant than cohomology groups alone. For example:
- CP² (complex projective plane) and S² ∨ S⁴ (wedge of spheres) have identical cohomology **groups**
- But their cohomology **rings** differ: in CP², α ∪ α ≠ 0 for α ∈ H², while in S² ∨ S⁴, α ∪ α = 0

**Cohomology operations** go further:
- **Bockstein** β: Hᵏ(X; Z/p) → Hᵏ⁺¹(X; Z/p) — detects torsion
- **Steenrod squares** Sqⁱ: Hᵏ(X; Z/2) → Hᵏ⁺ⁱ(X; Z/2) — stable cohomology operations

These operations provide information that even the ring structure alone cannot capture.

## Why Does This Matter?

**For topology**: Cohomology rings are fundamental invariants for classifying spaces. Two spaces with the same cohomology ring are "close" topologically — the ring is a powerful discriminator.

**For data analysis**: Applied topology (TDA) uses cohomology to analyze the shape of data. The cup product captures relationships between features in different dimensions — how 1D loops combine to create 2D voids.

**For physics**: Cohomology rings classify characteristic classes of vector bundles — the mathematical language of gauge theories, magnetic monopoles, and topological insulators.

**For agent systems**: Topological invariants of agent state spaces classify the "shape" of agent behavior. The ring structure captures how behavioral primitives compose into complex patterns.

## Architecture

```
cohomology-ring
│
├── Cochain                    ← Basic cochain element
│   ├── zero(degree)               Zero cochain
│   ├── basis(degr
```
