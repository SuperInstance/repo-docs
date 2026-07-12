# cosmic-web

**Cluster:** ecology-sim  
**Language:** Rust  
**Source:** [SuperInstance/cosmic-web](https://github.com/SuperInstance/cosmic-web)

## Intention

Fleet as cosmic web: dependency filaments, empty voids, repo clusters, hub nodes with centrality measures, and large-scale structure statistics

## How It Works

[code]

## What It's For

Fleet as cosmic web: dependency filaments, empty voids, repo clusters, hub nodes with centrality measures, and large-scale structure statistics

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (303 lines, 10582 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# 🌌 cosmic-web

**The cosmic web as fleet architecture.**

Map your dependency ecosystem onto the large-scale structure of the universe.
Filaments of repos connected by imports. Voids where no repos exist.
Clusters of tightly-coupled modules. Hub nodes as critical infrastructure.

```
         ╭─ ★ cluster-core ──★──★ cluster-utils ─╮
        ╱                    │                    ╲
  ·  ·  ·  ·  ·  ·  ·  ·  ★ hub-node  ·  ·  ·  ·  ·  ·  VOID
        ╲                    │                    ╱
         ╰─ ★ filament-b ───★──★ filament-c ───★─── filament-d ─── ·  ·
                                  │
                             ★ cluster-deep
                              ╱   │   ╲
                             ★    ★    ★
```

## The Metaphor

In cosmology, the **cosmic web** is the largest known structure in the universe —
a network of filaments, clusters, and voids stretching across billions of light-years.
Matter isn't uniformly distributed; it clumps along filaments, accumulates at nodes,
and leaves vast empty voids in between.

Your dependency ecosystem is the same:

| Cosmology | Fleet Architecture |
|-----------|-------------------|
| **Filaments** | Chains of repos linked by imports — deep supply chains |
| **Voids** | Gaps in dependency-space — untapped niches, missing abstractions |
| **Clusters** | Tightly-coupled repo groups — should probably be one repo |
| **Nodes** | Critical hubs — single points of failure in the ecosystem |
| **Density field** | Smoothed map of where repos concentrate |
| **LSS statistics** | Correlation functions, power spectra — scaling relations of code |

## Modules

### `filament` — Dependency Filaments

Detect chains of repos connected by imports using **Minimum Spanning Tree (MST)**
of the dependency graph. Long filaments = deep supply chains = fragile infrastructure.

```rust
use cosmic_web::{DependencyGraph, FilamentDetector};

let mut graph = DependencyGraph::new();
graph.add_edge("serde", "serde_json", 1.0);
graph.add_edge("serde_json", "my-api", 0.8);
graph.add_edge("my-api", "my-app", 0.6);

let detector = FilamentDetector::new(2);
let filaments = detector.detect(&graph);

for f in &filaments {
    println!("Filament: {} repos, length={:.2}, strength={:.2}",
        f.repos.len(), f.length, f.strength);
}
```

### `void` — Void Detection

Find empty regions of dependency-space using a **watershed algorithm** on a density field.
Voids represent untapped niche space — no repos exist there yet.

```rust
use cosmic_web::{DependencyGraph, VoidDetector};

let graph = build_ecosystem_graph();
let detector = VoidDetector::new(50, 0.1);
let voids = detector.detect(&graph);

for v in &voids {
    println!("Void: radius={:.2}, volume={:.2}, nearby={} repos",
        v.radius, v.volume, v.nearby_repos);
}
```

### `cluster` — Repo Clusters

Detect groups of tightly-coupled repos with the **friends-of-friends (FoF)** algorithm.
Clusters suggest modules that should be merged or refactored.

```rust
use cosmic_w
```
