# gpu-optimizer

## Intention
GPU-accelerated parallel simulated annealing for optimization problems, built on PyTorch.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
| Module | Description |
|---|---|
| `ParallelSA` | Core engine: batch N SA trials as parallel tensor ops |
| `SphereBenchmark` | Baseline quadratic optimization (sphere function) |
| `RastriginBenchmark` | Multi-modal optimization with many local minima |
| `TSPSolver` | Small traveling salesman problems (10–30 cities) |
| `PortfolioOptimizer` | Minimize portfolio variance subject to return const

## Who Would Use It
```bash
pip install -e .

## Language / Stack
Python

## Status Assessment
Documented with tests, API docs, and installation guide (148 line README).

## Honest Assessment
Moderately documented (148 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/gpu-optimizer](https://github.com/SuperInstance/gpu-optimizer)*
