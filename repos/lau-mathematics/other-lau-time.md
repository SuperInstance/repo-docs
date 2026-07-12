# lau-time

## Intention

A game-time engine for the Lau ecosystem — tick-based clocks, day/night cycles, room-driven time dilation, and a tick-indexed event scheduler.

## How It Works

`lau-time` provides the temporal backbone for a game world:
- **GameTime** — A monotonic tick counter that maps ticks to real-world seconds. Pause, resume, advance one tick or many. Query whether it's day or night, which day you're on, and the fractional time-of-day.
- **TimeOfDay** — An enum (`Dawn`, `Morning`, `Midday`, …, `Midnight`) derived from the current tick, partitioning a 2400-tick day into eight named phases.
- **TimeDilation** — A speed multiplier (0.5× = slow, 1.0× = normal, 2.0× = fast) that can be derived from a room's *vibe* score, making contemplative rooms feel slower and exciting rooms feel faster.
- **Schedule** — A `BTreeMap`-backed calendar indexed by tick number. Add events, then drain all events due at or before the current tick. Used for quest starts, room dissolves, weather shifts, agent milestones, and season changes.
Everything is `Serialize`/`Deserialize` via **serde**, so game state snapshots round-trip through JSON (or any serde format) trivially.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. A game-time engine for the Lau ecosystem — tick-based clocks, day/night cycles, room-driven time dilation, and a tick-indexed event scheduler.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (184 lines), mentions tests, includes examples.

- README length: 261 lines, 8806 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
