# luau-math

## Intention

Core math library for Roblox games — symmetry groups, sequences, and rhythm math

## How It Works

### Wally
Add to your `wally.toml`:
```toml
[dependencies]
LuauMath = "superinstance/luau-math@0.1.0"
```
### Manual
Copy `src/` files into your project under `ReplicatedStorage/luau-math`.
```lua
local Symmetry = require(path.to.luau-math.Symmetry)
local Rhythm = require(path.to.luau-math.Rhythm)
local Sequence = require(path.to.luau-math.Sequence)
-- Cyclic group Z/4Z
local c4 = Symmetry.CyclicGroup.new(4)
print(c4:compose(1, 3)) --> 0

## What It's For

Core math library for Roblox games — symmetry groups, sequences, and rhythm math

## Who Would Use It

Researchers and developers applying advanced mathematics to computation. Those who need formal mathematical structures (algebraic, geometric, topological) in code.

## Language / Stack

- **Primary language:** Luau

## Status Assessment

**Status: MODERATE**

Reasonable README (112 lines), mentions tests, includes examples.

- README length: 144 lines, 3993 characters
- Documented sections: Features, Installation, Usage, Testing, API Reference

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
