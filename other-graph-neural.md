# graph-neural

## Intention
**Spectral graph neural network primitives — normalized Laplacian, spectral filters, and graph-level readout in pure Rust.**

## How It Works
Part of the SuperInstance ecosystem:

- **graph-neural** — Spectral GNN primitives (this repo)
- **heat-spectral** — Heat diffusion on graphs
- **wave-conservation** — Wave propagation on graphs

## What It's For
- **Normalized Laplacian** — L = I - D⁻½AD⁻½, eigenvalues in [0, 2]
- **Spectral convolution** — filter node features in the eigenbasis
- **Message passing** — sum, mean, or max aggregation over neighborhoods
- **Graph readout** — sum, mean, or attention-weighted pooling to graph-level representation
- **Power iteration eigendecomposition** — no external dependencies
- **Cheeger constant estimatio

## Who Would Use It
```toml
[dependencies]
graph-neural = { git = "https://github.com/SuperInstance/graph-neural" }
```

## Language / Stack
Rust

## Status Assessment
Documented with tests, API docs, and installation guide (85 line README).

## Honest Assessment
Has documentation (85 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/graph-neural](https://github.com/SuperInstance/graph-neural)*
