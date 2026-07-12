# evo-rs

## Intention
Evolutionary optimization in Rust. GA, DE, NSGA-II, GP. When gradient descent can't help you.

## How It Works
```rust
use evo_rs::{
    ga::{GAConfig, run_ga},
    individual::RealCodedIndividual,
    fitness::FitnessFn,
};

fn rastrigin(x: &[f64]) -> f64 {
    10.0 * x.len() as f64 + x.iter().map(|xi| xi * xi - 10.0 * (2.0 * std::f64::consts::PI * xi).cos()).sum::<f64>()
}

let config = GAConfig {
    pop_size: 200,
    generations: 500,
    mutation_rate: 0.1,
    crossover_rate: 0.8,
    ..Default::default()
};

let best = run_ga(config, 10, -5.12..5.12, |ind| -rastrigin(ind.genes()));
println!("Best

## What It's For
- **Genetic algorithms** — tournament/roulette selection, single-point/two-point/uniform crossover, gaussian/bitflip mutation
- **Differential evolution** — DE/rand/1, DE/best/1, DE/current-to-best/1 with adaptive F/CR
- **NSGA-II** — multi-objective optimization with crowding distance and non-dominated sorting
- **Genetic programming** — tree-based GP with subtree crossover, tournament selection

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Has some documentation (69 lines).

## Honest Assessment
Has documentation (69 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/evo-rs](https://github.com/SuperInstance/evo-rs)*
