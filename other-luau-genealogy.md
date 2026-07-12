# luau-genealogy

## Intention

Lineage tracking for game entities in Luau (Roblox)

## How It Works

### Wally
Add to your `wally.toml`:
```toml
[dependencies]
GenealogyTree = "superinstance/luau-genealogy@0.1.0"
```
### Manual
Copy `src/GenealogyTree.luau` into your project.
```lua
local GenealogyTree = require(path.to.GenealogyTree)
local tree = GenealogyTree.new()
-- Create roots
local origin = tree:createRoot("Origin")
-- Spawn children
local child1 = tree:spawnChild(origin, "Child1")

## What It's For

Lineage tracking for game entities in Luau (Roblox)

## Who Would Use It

Game developers, particularly those working with Roblox/Luau. Educators using game mechanics to teach mathematical concepts.

## Language / Stack

- **Primary language:** Luau

## Status Assessment

**Status: MODERATE**

Reasonable README (66 lines), includes examples.

- README length: 109 lines, 2961 characters
- Documented sections: Features, Installation, Usage, API

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
