# graph-flow

## Intention
Network flow algorithms for Rust. Pure `std` — no external dependencies.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- **Ford-Fulkerson** — Maximum flow via DFS augmenting paths
- **Edmonds-Karp** — BFS-based max flow with O(VE²) guarantee
- **Min-cost max-flow** — Successive shortest paths with Bellman-Ford
- **Bipartite matching** — Maximum matching via flow reduction, König's theorem
- **Circulation with demands** — Feasibility checking with lower/upper bounds

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (33 line README).

## Honest Assessment
Minimal documentation (33 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/graph-flow](https://github.com/SuperInstance/graph-flow)*
