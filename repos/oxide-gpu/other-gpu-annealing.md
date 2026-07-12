# gpu-annealing

## Intention
A pure-Rust orchestration layer for GPU-accelerated simulated annealing. Provides cooling schedules, parallel trial management, topology-aware annealing over DAGs, and conservation-constrained optimization. The crate contains **no GPU code** — it manages the state, scheduling, and decision logic that drives a GPU kernel executing thousands of annealing trials in parallel.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Simulated annealing (SA) is one of the most versatile **global optimization** algorithms — it can escape local minima that trap gradient-based methods. But SA is slow: it requires millions of function evaluations. GPU parallelism solves this by running thousands of independent annealing chains simultaneously, then selecting the best. This crate provides the **CPU-side orchestration** that decides

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (127 line README).

## Honest Assessment
Moderately documented (127 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/gpu-annealing](https://github.com/SuperInstance/gpu-annealing)*
