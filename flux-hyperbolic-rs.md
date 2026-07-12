# flux-hyperbolic-rs

**Category:** 🎵 Math/Music/Algebra
**Status:** 🔴 Experimental
**Language:** Rust
**README:** 1,138 bytes

## Intention
Hyperbolic geometry embeddings using Poincaré ball and Lorentz models

## How It Works
Provides Poincaré ball and Lorentz (hyperboloid) models of hyperbolic space, with:
- Hyperbolic distance, exponential/logarithmic maps, Möbius addition
- Riemannian gradient descent for tradition embedding optimization
- Tradition embeddings mapped from dial space coordinates

## Usage

```rust
use flux_hyperbolic::{PoincareBall, TraditionEmbedding, RiemannianGD};

let ball = PoincareBall::unit();

// Distance between two points
let u = vec![0.1, 0.2];
let v = vec![0.3, -0.1];
println!("Distance...

## What It's For
Hyperbolic geometry embeddings using Poincaré ball and Lorentz models

## Who Would Use It
Developers in the FLUX ecosystem.

## Honest Assessment
Has code examples. **no tests, CI, or benchmarks detected**.
