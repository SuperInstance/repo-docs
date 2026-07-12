# dial-theory-rs

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/dial-theory-rs](https://github.com/SuperInstance/dial-theory-rs)

## Intention

Cultural dial positions for agent personality — theoretical spectrums, traditions, clustering, and evolution

## How It Works

Cultural dial positions for agent personality — where agents fall on theoretical spectrums.

## What It's For

Cultural dial positions for agent personality — theoretical spectrums, traditions, clustering, and evolution

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (444 lines, 15496 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# dial-theory-rs

Cultural dial positions for agent personality — where agents fall on theoretical spectrums.

Models cultural traditions as positions in a 2D continuous space. Traditions cluster, drift, merge, split, and compete — the same dynamics that govern real cultural ecosystems, now available as composable Rust primitives.

Part of the **sunset-ecosystem**: tradition positions feed into `conservation-law` (which enforces resource conservation as traditions evolve), and fleet-level coordination uses `si-fleet-api` to propagate dial state across agents.

## The Math

### Dial Positions as Points on a Manifold

Each tradition occupies a position $(x, y) \in [-1, 1]^2$ on a cultural dial. The distance between two traditions is:

$$d(p_1, p_2) = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2}$$

This is Euclidean distance, but we also support Manhattan ($L_1$), Chebyshev ($L_\infty$), angular, and cosine metrics — each reveals a different aspect of cultural topology.

### Lotka-Volterra Competition

When two traditions occupy similar dial positions, they compete. The Lotka-Volterra competition model describes how tradition strengths evolve:

$$\frac{ds_i}{dt} = r_i s_i \left(1 - \frac{s_i + \alpha_{ij} s_j}{K_i}\right)$$

where $s_i$ is the strength of tradition $i$, $r_i$ its growth rate, $K_i$ its carrying capacity, and $\alpha_{ij}$ the competition coefficient encoding how much tradition $j$ suppresses $i$.

### K-Means Clustering

Traditions cluster by proximity using k-means. The algorithm minimizes inertia:

$$J = \sum_{k=1}^{K} \sum_{i \in C_k} d(p_i, \mu_k)^2$$

where $\mu_k$ is the centroid of cluster $C_k$.

### Tradition Evolution as a Dynamical System

Traditions evolve via four operations:
- **Drift**: move toward a target at rate $\alpha$: $p_{t+1} = (1 - \alpha) p_t + \alpha \cdot p_{\text{target}}$
- **Merge**: weighted average of two traditions
- **Split**: spawn a new tradition at an offset
- **Pressure**: external force pushing toward a source point

## Installation

```toml
[dependencies]
dial-theory-rs = { git = "https://github.com/SuperInstance/dial-theory-rs" }
```

## Usage

### Creating Traditions and Measuring Distance

```rust
use dial_theory_rs::position::DialPosition;
use dial_theory_rs::tradition::{Tradition, TraditionSet};
use dial_theory_rs::distance::{distance, DistanceMetric};

// Define traditions at cultural positions
let stoicism = Tradition::new("stoicism", DialPosition::new(0.8, -0.3))
    .describe("Virtue ethics, emotional resilience");
let epicureanism = Tradition::new("epicureanism", DialPosition::new(0.2, 0.5))
    .describe("Pleasure as absence of suffering");

// Euclidean distance between traditions
let d = stoicism.distance_to(&epicureanism);
println!("Distance: {:.3}", d);

// Cosine similarity — are they pointing the same direction?
let cos_dist = distance(
    &stoicism.position,
    &epicureanism.position,
    &DistanceMetric::Cosine,
);
println!("Cosine distance: {:.3}", cos_dist);

// Weighted blend —
```
