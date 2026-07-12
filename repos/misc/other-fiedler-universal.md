# fiedler-universal

## Intention
**Fiedler vector partitioning across every graph family — benchmark spectral clustering against k-means, spectral clustering, Louvain, and label propagation.**

## How It Works
Part of the SuperInstance ecosystem:

- **graph-neural** — Spectral GNN primitives (uses Fiedler vector)
- **fiedler-universal** — Systematic Fiedler benchmarking (this repo)

## What It's For
- **Fiedler partition** — spectral bipartitioning via algebraic connectivity eigenvector
- **Multi-k extension** — use eigenvectors 1..k for k-way partitioning
- **8 graph families** — ER, SBM, geometric, WS, BA, planted partition, ring of cliques, ladder
- **5 methods compared** — Fiedler, k-means on Fiedler, full spectral clustering, Louvain, label propagation
- **Metrics** — Adjusted Rand Index

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Python

## Status Assessment
Has some documentation (34 lines).

## Honest Assessment
Minimal documentation (34 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/fiedler-universal](https://github.com/SuperInstance/fiedler-universal)*
