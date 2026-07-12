# betti-curve

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/betti-curve](https://github.com/SuperInstance/betti-curve)

## Intention

Betti curves, barcodes, Euler curves, and persistence entropy for topological data analysis summaries

## How It Works

[code]

## What It's For

Betti curves, barcodes, Euler curves, and persistence entropy for topological data analysis summaries

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (225 lines, 9200 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# betti-curve

> **Betti curves and Euler characteristic curves — track the topological evolution of your data across scales**

[![crates.io](https://img.shields.io/crates/v/betti-curve.svg)](https://crates.io/crates/betti-curve)
[![docs.rs](https://docs.rs/betti-curve/badge.svg)](https://docs.rs/betti-curve)
[![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## What is a Betti Curve?

In persistent homology, topological features (connected components, loops, voids) are born and die as you vary a scale parameter ε. A **barcode** records each feature's lifetime as an interval [b, d). A **Betti curve** βₖ(ε) counts how many k-dimensional features are alive at each scale — it's a step function that rises when features are born and falls when they die.

The **Euler characteristic curve** χ(ε) = β₀(ε) − β₁(ε) + β₂(ε) − ... compresses all dimensions into a single integer-valued function that captures the overall topological complexity at each scale.

Together with **persistence entropy** (a Shannon entropy measure over bar lengths), these curves provide functional summaries of topological data suitable for statistical analysis, machine learning features, and visual interpretation.

## Why Does This Matter?

Betti curves and Euler curves are among the most useful summaries in topological data analysis:

- **Functional data analysis**: Betti curves are functions you can feed into FDA methods — smoothing, PCA, regression
- **Scale selection**: Peaks in Betti curves indicate "interesting" scales where topology is richest
- **Classification**: The shape of Betti curves distinguishes different data-generating processes
- **Complexity monitoring**: Euler curves track total topological complexity as a single number
- **Entropy**: Persistence entropy quantifies the diversity of topological feature lifetimes

Real-world applications:
- **Protein folding**: Track how secondary structure elements (loops, tunnels) appear during folding
- **Network analysis**: Monitor connected components and cycles in dynamic graphs
- **Image analysis**: Characterize texture via the topological signature across scales
- **Cosmology**: Study the topology of the cosmic web (voids, filaments, clusters)

## Architecture

```
┌───────────────────────────────────────────────────────────────┐
│                   Betti Curve Pipeline                         │
│                                                               │
│  Barcodes (H₀, H₁, H₂, ...)                                  │
│  ┌─────────────────────┐                                      │
│  │ H₀: ████  ██████    │    BettiCurve                        │
│  │ H₁:    ████         │──▶ β₀(ε): ───┐   ┌────             │
│  │ H₂:       ██        │    β₁(ε): ────┘   └───             │
│  └─────────────────────┘                                      │
│          │                                                    │
│          ▼                                                    │
│  ┌─────────────────┐  ┌─────
```
