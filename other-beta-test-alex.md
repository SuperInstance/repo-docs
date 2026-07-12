# beta-test-alex

**Cluster:** beta-testing  
**Language:** Rust  
**Source:** [SuperInstance/beta-test-alex](https://github.com/SuperInstance/beta-test-alex)

## Intention

Beta test persona: Alex (developer). Tracks bugs, feedback, and developer experience metrics.

## How It Works

**Genome encoding:** Each agent has a genome of 24 trits, each ∈ {-1, 0, +1}. The genome encodes behavioral parameters that map to strategies in competitive encounters.

**Population evolution loop:**
[code]

**Species classification:** Agents are classified into one of five strategy species based on their genome's phenotype:

| Species | Description | Typical Entropy |
|---------|-------------|-----------------|
| Explorer | High entropy, weak signal | 1.5 |
| Diplomat | Adaptive, mirrors opponents | 1.0 |
| Marksman | Low entropy, specialized | 0.5 |
| Climber | Diminishing returns search | 

## What It's For

Beta test persona: Alex (developer). Tracks bugs, feedback, and developer experience metrics.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (81 lines, 4580 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Beta Test Alex

**Beta Test Alex** is a Rust crate implementing NPC behavior evolution using ternary genomes (trits: {-1, 0, +1}) with population genetics, fitness evaluation, and species classification — designed as a beta test harness for SuperInstance's ternary agent crates.

## Why It Matters

Ternary logic — using three states instead of binary's two — maps naturally to the SuperInstance conservation framework's action space: Avoid (−1), Unknown (0), and Choose (+1). This crate validates that ternary-encoded genomes can drive meaningful behavioral evolution in simulated NPCs. By evolving populations of 100 agents with 24-trit genomes across 50+ generations, the beta test confirms that: (1) fitness consistently improves from ~0.8 to ~0.99, (2) the ternary action distribution is conserved across generations (validating Law 5), and (3) the population maintains diversity without premature convergence. This provides empirical ground-truth for the conservation-law claims.

## How It Works

**Genome encoding:** Each agent has a genome of 24 trits, each ∈ {-1, 0, +1}. The genome encodes behavioral parameters that map to strategies in competitive encounters.

**Population evolution loop:**
```
for each generation:
  1. Evaluate fitness for all agents (O(pop_size × genome_length))
  2. Classify each agent into a strategy species
  3. Select parents via tournament selection (O(pop_size × tournament_size))
  4. Crossover: single-point or uniform (O(genome_length))
  5. Mutate: each trit flips with probability mutation_rate (O(genome_length))
  6. Replace population with offspring (elitism preserves top-k)
```

**Species classification:** Agents are classified into one of five strategy species based on their genome's phenotype:

| Species | Description | Typical Entropy |
|---------|-------------|-----------------|
| Explorer | High entropy, weak signal | 1.5 |
| Diplomat | Adaptive, mirrors opponents | 1.0 |
| Marksman | Low entropy, specialized | 0.5 |
| Climber | Diminishing returns search | 1.2 |
| Prospector | Sparse rewards, max diversity | 1.99 |

**Conservation check:** After each generation, the total agent count must equal the initial population size — verifying that no agents are lost or duplicated during evolution. This directly tests the population-level conservation required by Law 5.

## Quick Start

```rust
use beta_test_alex::*;

fn main() {
    let mut pop = Population::new(100, 24);
    println!("Gen 0: avg={:.4}, best={:.4}", pop.avg_fitness(), pop.best().fitness);

    for gen in 1..=50 {
        pop.evolve();
    }
    println!("Gen 50: avg={:.4}, best={:.4}", pop.avg_fitness(), pop.best().fitness);
}
```

## API

| Type/Method | Description |
|-------------|-------------|
| `Population` | Agent population with evolution loop |
| `Population::new` | Create with size and genome length |
| `Population::evolve` | Advance one generation |
| `avg_fitness` | Population mean fitness |
| `best` | Reference to top agent |
| `species_distri
```
