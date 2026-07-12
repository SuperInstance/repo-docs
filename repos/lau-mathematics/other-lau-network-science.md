# lau-network-science

## Intention

Network science library: models, centrality, community detection, epidemic spreading, and agent social network analysis

## How It Works

`lau-network-science` gives you a toolbox for working with graphs as a scientist, not just a programmer:
- **Build graphs** — undirected and directed, with adjacency-list storage, BFS, connected components, and serialization via `serde`.
- **Generate networks** — Erdős–Rényi (G(n,p) and G(n,M)), Barabási–Albert preferential attachment, Watts–Strogatz small-world.
- **Measure centrality** — degree, betweenness (Brandes' algorithm), closeness, eigenvector (power iteration), and PageRank (undirected + directed).
- **Find communities** — Louvain modularity maximization, label propagation, modularity scoring, and Normalized Mutual Information (NMI) for comparing partitions.
- **Analyze structure** — small-world metrics (σ, γ, λ), clustering coefficient, transitivity, degree assortativity, mixing matrices, k_nn(k).
- **Simulate epidemics** — discrete SIR and SIS models on arbitrary graphs, epidemic threshold computation, averaged multi-run final-size estimation.
- **Probe resilience** — random node/edge percolation, targeted degree-based attacks, Molloy–Reed critical threshold.
- **Fit distributions** — power-law MLE (Clauset–Shalizi–Newman), CCDF, Gini coefficient, scale-free detection.
- **Model agents** — `AgentNetwork` attaches named agents with attributes to a graph, tracks weighted interactions, and computes influence rankings, bridge agents, community memberships, and full summary statistics.
---

## What It's For

Network science library: models, centrality, community detection, epidemic spreading, and agent social network analysis

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (229 lines), mentions tests, includes examples, has benchmarks.

- README length: 336 lines, 14058 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (336 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
