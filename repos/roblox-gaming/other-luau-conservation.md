# luau-conservation

## Intention

Conservation law checking for Roblox — Noether's theorem, playable

## How It Works

Conservation law checking for Roblox games. Verify that energy, mass, momentum, and tile values are conserved across game transforms. Built for educational games teaching physics and mathematics through gameplay.
The core idea comes from **Noether's theorem**: for every symmetry in a system, there's a corresponding quantity that never changes. Time symmetry → energy conservation. Rotational symmetry → angular momentum. This crate makes that playable.
### Wally
```toml
[dependencies]
Conservation = "superinstance/luau-conservation@0.1.0"
```
### Manual
Copy `src/` into ReplicatedStorage.

## What It's For

Conservation law checking for Roblox — Noether's theorem, playable

## Who Would Use It

Game developers, particularly those working with Roblox/Luau. Educators using game mechanics to teach mathematical concepts.

## Language / Stack

- **Primary language:** Luau

## Status Assessment

**Status: MODERATE**

Reasonable README (59 lines), includes examples.

- README length: 77 lines, 2473 characters
- Documented sections: What This Does, Install, Quick Start, API Reference, Noether's Theorem Mapping

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
