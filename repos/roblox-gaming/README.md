# Roblox Gaming — Index

**Total repos: 11**

The Luau game engine: a collection of Roblox/Luau packages implementing an educational math game where players learn git version control, AI concepts, and advanced mathematics through gameplay. The demo wires all 10 packages into a single game loop.

## Category Overview

This is a cohesive game engine built in Luau (Roblox's scripting language) where every gameplay mechanic maps to a real mathematical or computer science concept. The design philosophy: **kids think they're playing, but they're actually learning.**

### The 10 Luau Packages

| Package | Game Role | Real Concept |
|---------|-----------|-------------|
| **luau-spatial** | Entity position indexing (QuadTree) | Spatial data structures |
| **luau-biome** | Procedural terrain (10 biome types) | Procedural generation |
| **luau-quest** | Mission tracking with math objectives | Goal-directed planning |
| **luau-scheduler** | Priority-based game loop | Scheduling algorithms |
| **luau-conservation** | Physics law verification | Noether's theorem / conservation |
| **luau-recipe** | Crafting with biome/skill gates | Constraint satisfaction |
| **luau-genealogy** | Entity lineage and evolution | Graph theory / ancestry |
| **luau-math** | Symmetry groups, rhythm, sequences | Group theory / abstract algebra |
| **luau-git-world** | World versioning (teaches git!) | Version control |
| **luau-audio** | Musical feedback and scales | Music theory / harmonics |

### luau-demo

The integration demo — wires every Luau package into a single game loop. Each tick:
1. Scheduler runs priority tasks
2. Spatial system updates entity positions
3. Biome system generates terrain
4. Conservation system verifies physics
5. Quest system checks objectives
6. Genealogy tracks entity history
7. Git-world saves state as commits
8. Audio provides musical feedback
9. Math system computes symmetry/rhythm

### Package Details

- **luau-math** — Core math library: cyclic groups (`Z/nZ`), dihedral groups, rhythm mathematics, sequence generation. Published to Wally (Roblox package manager)
- **luau-conservation** — Physics law verification: energy, momentum conservation checks in-game
- **luau-git-world** — World state versioning using git concepts. "Save my world" = `git commit`, "Make a save point" = `git branch`, "Keep the changes" = `git merge`
- **luau-spatial** — QuadTree-based spatial indexing for efficient entity queries
- **luau-biome** — 10 procedural biome types with distinct generation rules

### Key Interconnections

- This is the **Luau/Roblox frontend** for the broader Lau mathematics ecosystem (lau-mathematics category)
- **luau-conservation** implements the same conservation framework as the Rust conservation-laws category
- **luau-git-world** teaches the same git concepts used by the agent-framework category's git-native agents
- The game loop architecture mirrors the PLATO tick runtime
- Available via **Wally** (Roblox package manager) — `superinstance/luau-math@0.1.0`

## Full Repository Listing

| Repo | Language | Description |
|------|----------|-------------|
| [luau-demo](./other-luau-demo.md) | Luau | Integration demo — all 10 packages wired together |
| [luau-spatial](./other-luau-spatial.md) | Luau | QuadTree spatial indexing |
| [luau-biome](./other-luau-biome.md) | Luau | Procedural terrain (10 biomes) |
| [luau-quest](./other-luau-quest.md) | Luau | Mission tracking with math objectives |
| [luau-scheduler](./other-luau-scheduler.md) | Luau | Priority-based game loop scheduler |
| [luau-conservation](./other-luau-conservation.md) | Luau | Physics law verification |
| [luau-recipe](./other-luau-recipe.md) | Luau | Crafting system with constraints |
| [luau-genealogy](./other-luau-genealogy.md) | Luau | Entity lineage and evolution |
| [luau-math](./other-luau-math.md) | Luau | Symmetry groups, rhythm, sequences |
| [luau-git-world](./other-luau-git-world.md) | Luau | Git-based world versioning |
| [luau-audio](./other-luau-audio.md) | Luau | Musical feedback and scales |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
