# bayesian-update

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/bayesian-update](https://github.com/SuperInstance/bayesian-update)

## Intention

See README.

## How It Works

A Rust library for **Bayesian belief updating** with conjugate priors, credible intervals, and Kalman filtering.

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (156 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# bayesian-update

A Rust library for **Bayesian belief updating** with conjugate priors, credible intervals, and Kalman filtering.

[![crates.io](https://img.shields.io/crates/v/bayesian-update.svg)](https://crates.io/crates/bayesian-update)
[![Documentation](https://docs.rs/bayesian-update/badge.svg)](https://docs.rs/bayesian-update)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Overview

Bayesian inference provides a principled framework for updating beliefs in light of new evidence. This library implements core Bayesian updating mechanisms with a focus on:

- **Conjugate priors** — closed-form posterior computation
- **Beta-Binomial models** — for binary/binary-outcome data
- **Credible intervals** — quantifying uncertainty in parameter estimates
- **Kalman filtering** — sequential Gaussian Bayesian estimation

Whether you're building recommendation systems, A/B testing frameworks, sensor fusion pipelines, or statistical analysis tools, `bayesian-update` provides the mathematical primitives you need.

## Installation

Add to your `Cargo.toml`:

```toml
[dependencies]
bayesian-update = "0.1.0"
```

## Quick Start

### Beta-Binomial Updating

```rust
use bayesian_update::{BetaDistribution, BinomialLikelihood, ConjugateUpdate};

// Start with a uniform prior (we know nothing)
let prior = BetaDistribution::new(1.0, 1.0);

// Observe 7 successes and 3 failures
let data = BinomialLikelihood::new(7, 3);

// Compute the posterior: Beta(8, 4)
let posterior = prior.conjugate_update(&data);

println!("Posterior mean: {}", posterior.mean()); // 0.666...
println!("Posterior mode: {}", posterior.mode()); // 0.636...
```

### Credible Intervals

```rust
use bayesian_update::{BetaDistribution, CredibleInterval};

let posterior = BetaDistribution::new(8.0, 4.0);

// 95% equal-tailed credible interval
let (lower, upper) = CredibleInterval::equal_tailed(&posterior, 0.95);
println!("95% CI: [{:.3}, {:.3}]", lower, upper);

// Highest density interval (narrowest interval with 95% mass)
let (hdi_lower, hdi_upper) = CredibleInterval::hdi(&posterior, 0.95);
println!("95% HDI: [{:.3}, {:.3}]", hdi_lower, hdi_upper);
```

### Kalman Filter

```rust
use bayesian_update::{Gaussian, KalmanFilter};

// Start with high uncertainty
let initial = Gaussian::new(0.0, 100.0);
let mut kf = KalmanFilter::new(initial, 0.1);

// Incorporate noisy measurements
for measurement in [1.1, 0.9, 1.05, 0.95, 1.02] {
    kf.step(0.0, measurement, 0.5);
}

println!("Estimated state: {:.3} ± {:.3}", 
    kf.state().mean, kf.state().variance.sqrt());
```

## Core Concepts

### Beta Distribution

The `BetaDistribution` is the conjugate prior for the Bernoulli and binomial likelihoods. It's parameterized by two shape parameters α and β:

- **α > 0** — controls the concentration of mass near 1
- **β > 0** — controls the concentration of mass near 0
- **Mean** = α / (α + β)
- **Mode** = (α - 1) / (α + β - 2) when α, β > 1

Special cases:
| Parameters | Interpreta
```
