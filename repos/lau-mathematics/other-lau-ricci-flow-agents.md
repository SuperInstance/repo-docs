# lau-ricci-flow-agents

## Intention

> Networks have curvature. Not the kind you see — the kind you measure by how efficiently information flows between neighbors. Ollivier-Ricci curvature quantifies this: positive curvature means neighbors are already close, negative means they're far apart. Run Ricci flow to smooth the curvature, and

## How It Works

This crate implements **discrete Ricci curvature and Ricci flow on weighted graphs**, with direct application to **agent network community detection**. It computes how "curved" the connections between nodes are, then evolves the graph to make curvature uniform — revealing natural community boundaries as edges between communities weaken.
It provides:
- **Ollivier-Ricci curvature** via exact optimal transport (min-cost flow with Bellman-Ford / transportation simplex) between lazy random walk distributions
- **Forman-Ricci curvature** — a combinatorial alternative (faster to compute, coarser signal)
- **Ricci flow evolution** — edge weights update by `dω/dt = -κ·ω`, curvature smooths over iterations
- **Community detection** — after Ricci flow, cut weak edges and extract connected components
- **Spectral analysis** — normalized Laplacian eigenvalues, spectral gap, Cheeger constant, expander detection
- **Agent similarity graphs** — build networks from agent feature vectors, detect communities via curvature evolution
Every structure is `serde`-serializable. The entire pipeline works on pure Rust with no external solver dependencies.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. > Networks have curvature. Not the kind you see — the kind you measure by how efficiently information flows between neighbors. Ollivier-Ricci curvature quantifies this: positive curvature means neighb

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (252 lines), mentions tests, includes examples.

- README length: 351 lines, 14947 characters
- Documented sections: What This Does, The Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (351 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
