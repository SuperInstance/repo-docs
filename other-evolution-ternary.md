# evolution-ternary

## Intention
**Evolutionary dynamics on ternary strategy spaces** — agents carry strategy vectors over the alphabet {0, 1, 2}, with tournament/roulette/rank selection, single-point/uniform crossover, point mutation, fitness-proportionate evaluation across multiple environments, speciation, and convergence detection.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Genetic algorithms (GAs) are optimization methods inspired by natural selection: maintain a population of candidate solutions, evaluate fitness, select parents, recombine, mutate, and repeat. Traditional GAs use binary {0, 1} or real-valued chromosomes. This crate uses **ternary {0, 1, 2}** encoding, which offers:

1. **Expressiveness**: Three states (underweight, neutral, overweight) vs. binary's

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (171 line README).

## Honest Assessment
Moderately documented (171 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/evolution-ternary](https://github.com/SuperInstance/evolution-ternary)*
