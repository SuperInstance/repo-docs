# luau-spatial

## Intention

Spatial indexing for Roblox games — QuadTree, GridHash, SpatialHash

## How It Works

Find what's near what, fast. Essential for collision detection, neighbor AI, proximity triggers, and rendering culling in Roblox games.
Now with **full 3D support** — `Vec3`, `BoundingBox3D`, and `OcTree` alongside the existing 2D structures.
Six modules, one goal: efficient spatial queries on ANY data — not just BaseParts.
### Option 1: Wally (recommended)
Add to your `wally.toml`:
```toml
[dependencies]
Spatial = "superinstance/luau-spatial@0.1.0"
```
Then run `wally install`.
### Option 2: Rojo
Clone this repo and use the included `default.project.json` with Rojo:
```bash
rojo serve
```

## What It's For

Spatial indexing for Roblox games — QuadTree, GridHash, SpatialHash

## Who Would Use It

Game developers, particularly those working with Roblox/Luau. Educators using game mechanics to teach mathematical concepts.

## Language / Stack

- **Primary language:** Luau

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (217 lines), includes examples.

- README length: 287 lines, 9786 characters
- Documented sections: What This Does, Install, Quick Start, API Reference, Quick Start — 3D

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (287 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
