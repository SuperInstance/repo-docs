# beta-test-elena

**Cluster:** beta-testing  
**Language:** Rust  
**Source:** [SuperInstance/beta-test-elena](https://github.com/SuperInstance/beta-test-elena)

## Intention

Dr. Elena's rigorous stress-test of the SuperInstance ternary agent ecosystem's 5 laws

## How It Works

[code]

## What It's For

Dr. Elena's rigorous stress-test of the SuperInstance ternary agent ecosystem's 5 laws

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (174 lines, 6251 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# beta-test-elena

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Language: Rust](https://img.shields.io/badge/language-Rust-orange.svg)]()
[![SuperInstance](https://img.shields.io/badge/part%20of-SuperInstance-9cf.svg)](https://github.com/SuperInstance)

Dr. Elena's rigorous stress-test of the SuperInstance ternary agent ecosystem's 5 claimed laws. Statistical validation across 10,000+ environments, 7 interaction matrices, and 7 population scales.

## What It Does

This is a **falsification machine**. It takes the 5 laws claimed by the SuperInstance framework and tries to break them with adversarial inputs, extreme scales, and statistical brute force. The results feed into `BETA-REPORT.md` — a law-by-law verdict with specific counterexamples and suggested fixes.

## Results at a Glance

| Law | Claim | Verdict | Pass Rate |
|-----|-------|---------|-----------|
| 1 | Negative space discovers structure | ✅ PASS | 99.99% (10,000 envs) |
| 2 | Avoidance dominates (>100:1) | ✅ PASS* | 100/100 runs |
| 3 | Species coexistence (100% survival) | ❌ FAIL | 14.3% (1/7 matrices) |
| 4 | Population > Individual | ❌ TAUTOLOGY | 0% (identical by construction) |
| 5 | Conservation (std < 0.01) | ❌ FAIL | 0% (massive drift at all scales) |

*Law 2 passes trivially — all-adversarial matrices produce ∞ ratio (zero engagement), not meaningful dominance.

## Installation

```bash
cargo run --bin beta-test-elena
```

Dependencies: `rand` 0.8, `rand_distr` 0.4, `statrs` 0.16.

## Architecture

```
main.rs
├── conservation_matrix
│   ├── conserved_quantity(population) → Φ
│   │     Φ = -Σ pᵢ·ln(pᵢ/K) + Σ pᵢ²/K²
│   └── evolve(population, interaction, dt, steps)
│         Lotka-Volterra with interaction terms
│
├── negative_space_core
│   ├── Environment { features, latent_dimensions }
│   │     random(), uniform(), with_noise()
│   └── discover(env, probes, rng) → f64
│         Stochastic sampling with 1.5× amplification
│
├── ternary_fitness
│   ├── population_fitness(pop, matrix) → f64
│   └── individual_fitness_sum(pop, matrix) → f64
│
├── Law 1 test: 10,000 random environments
├── Law 2 test: 100 adversarial runs
├── Law 3 test: 7 interaction matrices (3–15 species)
├── Law 4 test: 50 random trials (n=3..11)
└── Law 5 test: 7 scales (n=10..10,000)
```

## The Five Laws Tested

### Law 1: Negative Space Discovery

```rust
// From negative_space_core module
pub fn discover(env: &Environment, probes: usize, rng: &mut impl Rng) -> f64 {
    let discovered = (0..probes)
        .filter(|_| {
            let prob = env.latent_dimensions as f64 / (env.features.len().max(1) as f64);
            rng.gen::<f64>() < prob * 1.5
        })
        .count();
    (discovered as f64 / probes as f64).min(1.0)
}
```

10,000 random environments tested. Mean discovery rate = 0.41, nonzero discovery = 99.98%. **Passes.**

### Law 2: Avoidance Dominance

```rust
// Avoidance/engagement ratio with adversarial matrices
fn avoidance_engagement_ratio(pop: &[f64
```
