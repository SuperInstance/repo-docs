# bregman-divergence

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/bregman-divergence](https://github.com/SuperInstance/bregman-divergence)

## Intention

Bregman divergences: KL, squared Euclidean, Itakura-Saito, convex generating functions, and mirror descent

## How It Works

[code]

## What It's For

Bregman divergences: KL, squared Euclidean, Itakura-Saito, convex generating functions, and mirror descent

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (358 lines, 12299 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# bregman-divergence

> *One formula. Every distance in machine learning.*

Bregman divergences are the **unifying framework** behind the distance measures that power modern machine learning. KL divergence, squared Euclidean distance, Itakura-Saito divergence — they're not different beasts. They're the **same formula** with different generating functions plugged in. This crate gives you the whole family tree.

## Why Bregman Divergences Matter

If you've trained a neural network, clustered data, or estimated a probability distribution, you've used a Bregman divergence — you just didn't know it by that name.

Every "distance" in ML that's *not* a true metric (KL, cross-entropy, IS divergence) turns out to be a **Bregman divergence** — the gap between a convex function and its linear approximation:

```
D_φ(p‖q) = φ(p) - φ(q) - ⟨∇φ(q), p - q⟩
```

Change φ, and you get a different divergence:

```
φ(x) = ½‖x‖²         →  Squared Euclidean distance
φ(x) = Σ xᵢ ln(xᵢ)   →  KL divergence
φ(x) = -Σ ln(xᵢ)     →  Itakura-Saito divergence
```

**It's a mathematical family tree.** The Bregman formula is the parent. KL, Euclidean, and IS are the children — each born from a different generating function. This crate lets you work with the parent *and* the children, switching between them effortlessly.

## The Metaphor

Think of Bregman divergence as a **copy machine with interchangeable lenses**. The machine is always the same — it measures how far apart two points are by looking at the gap between a convex surface and its tangent plane. The *lens* is the generating function φ:

- Put on the **quadratic lens** (φ = ½‖x‖²), and you see Euclidean geometry
- Put on the **entropic lens** (φ = Σ xᵢ ln xᵢ), and you see information geometry
- Put on the **logarithmic lens** (φ = -Σ ln xᵢ), and you see spectral geometry

Same machine. Different worlds.

## Architecture

```
                    ┌─────────────────────────────┐
                    │     ConvexFunction (φ)       │
                    │  ┌─────┐ ┌────────┐ ┌─────┐ │
                    │  │x²   │ │x ln x  │ │-ln x│ │
                    │  └──┬──┘ └───┬────┘ └──┬──┘ │
                    │     │        │         │    │
                    └─────┼────────┼─────────┼────┘
                          │        │         │
          ┌───────────────┼────────┼─────────┼──────────────┐
          │  BregmanDivergence: D_φ(p‖q) = φ(p) - φ(q)     │
          │                - ⟨∇φ(q), p - q⟩                 │
          └───┬───────────┬┴────────┴┬───────────┬──────────┘
              │           │          │           │
     ┌────────┴──┐  ┌─────┴────┐  ┌─┴────────┐  │
     │ Squared   │  │Kullback  │  │Itakura   │  │
     │ Euclidean │  │Leibler   │  │Saito     │  │
     │  ½‖p-q‖²  │  │ Σ p ln(p/q)│ │ p/q-ln(p/q)-1│
     └───────────┘  └──────────┘  └──────────┘  │
              │           │          │           │
              └───────────┼──────────┼───────────┘
                          │          │
          
```
