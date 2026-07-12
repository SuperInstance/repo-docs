# graph-search-rs

## Intention
**Graph algorithms in pure Rust. Zero dependencies.**

## How It Works
| Algorithm | Function | Time Complexity | Use When |
|-----------|----------|-----------------|----------|
| BFS | `bfs()` / `bfs_distances()` | O(V + E) | Shortest hop-count path, level-order traversal |
| DFS | `dfs()` | O(V + E) | Topological exploration, cycle detection |
| Dijkstra | `dijkstra()` / `dijkstra_with_path()` | O(V²) | Shortest weighted path (no negative edges) |
| Bellman-Ford | `bellman_ford()` | O(V·E) | Negative edges, cycle detection |
| A\* | `astar()` | O(V²) best case |

## What It's For
```
Need shortest path?
├── All weights positive?
│   ├── Have a heuristic? → A*
│   └── No heuristic? → Dijkstra
├── Some negative weights? → Bellman-Ford
└── Only care about hop count? → BFS distances

Need to order tasks?
├── Known DAG? → Topological Sort
└── Might have cycles? → Topological Sort (returns None) + Tarjan SCC

Need to understand graph structure?
└── Tarjan SCC → find communities,

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (269 line README).

## Honest Assessment
Well-documented (269 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/graph-search-rs](https://github.com/SuperInstance/graph-search-rs)*
