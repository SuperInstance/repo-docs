# graph-coloring

## Intention
Three graph coloring algorithms with increasing accuracy and complexity: **greedy sequential** (O(V+E)), **DSatur** (saturation-degree heuristic), and **exact backtracking** (finds the chromatic number). Operates on adjacency-list graphs with `HashSet` neighbors for O(1) edge queries.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Graph coloring is one of the most fundamental problems in computer science, with direct applications in:

- **Register allocation**: Color interference graphs to map variables to CPU registers (Chaitin, 1981)
- **Scheduling**: Assign time slots to exams/meetings so no conflicts share a slot
- **Frequency assignment**: Color cell towers so adjacent towers use different frequencies
- **Map coloring*

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (131 line README).

## Honest Assessment
Moderately documented (131 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/graph-coloring](https://github.com/SuperInstance/graph-coloring)*
