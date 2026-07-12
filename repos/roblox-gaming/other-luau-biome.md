# luau-biome

## Intention

Deterministic biome generation for Roblox — 10 zones, mathematical structures, seeded worlds

## How It Works

### Option 1: Wally (recommended)
Add to your `wally.toml`:
```toml
[dependencies]
luau-biome = "superinstance/luau-biome@0.1.0"
```
Then run:
```sh
wally install
```
### Option 2: Manual
Copy the `src/` folder into your Roblox project under `ReplicatedStorage/luau-biome`.
### Option 3: Rojo
Use the included `default.project.json` with Rojo to sync into Studio:
```sh

## What It's For

Deterministic biome generation for Roblox — 10 zones, mathematical structures, seeded worlds

## Who Would Use It

Game developers, particularly those working with Roblox/Luau. Educators using game mechanics to teach mathematical concepts.

## Language / Stack

- **Primary language:** Luau

## Status Assessment

**Status: MODERATE**

Reasonable README (105 lines), mentions tests, includes examples.

- README length: 144 lines, 4371 characters
- Documented sections: Features, Install, Usage, Biome Reference, Architecture

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
