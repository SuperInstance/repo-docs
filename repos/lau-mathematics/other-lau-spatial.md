# lau-spatial

## Intention

Spatial indexing library for game worlds — QuadTree, GridHash, and SpatialHash

## How It Works

Spatial indexing for the **Lau (Layered Agent-UI)** game world. When your game has thousands of entities — players, NPCs, projectiles, particles — checking every pair for proximity is O(n²). Spatial indexing brings it down to O(n log n) or O(n) by dividing space into buckets.
Three data structures, three tradeoffs:
- **QuadTree** — hierarchical, adaptive, great for non-uniform distributions
- **GridHash** — simple uniform grid, fastest for roughly-uniform worlds
- **SpatialHash** — grid + support for entity sizes, best for collision detection

## What It's For

Spatial indexing library for game worlds — QuadTree, GridHash, and SpatialHash

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (121 lines), mentions tests, includes examples.

- README length: 169 lines, 5776 characters
- Documented sections: What This Does, The Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
