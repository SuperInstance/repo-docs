# lau-wasm-bridge

## Intention

A zero-dependency WASM compilation target for PLATO core types. Provides world simulation primitives — vibe fields, agents, rooms, and a full world hierarchy — with hand-rolled binary serialization designed for `wasm32-unknown-unknown`.

## How It Works

`lau-wasm-bridge` is the data layer you compile to WebAssembly when the Lau/PLATO game engine needs to run inside a browser or embedded WASM runtime. It ships four core types:
- **WasmVibeField** — A growable array of `f64` values with conservation-law tracking. Set a baseline, fill values, then check whether `sum()` deviates from the baseline by more than a tolerance.
- **WasmAgent** — An entity with an internal state vector, sensor inputs, and actuator outputs. A reactive `tick(vibe)` computes `actuators[0] = vibe × state[0]`.
- **WasmRoom** — A container for agents with a shared `vibe` value and an energy budget. `room_tick()` advances all agents and tracks conservation error against the budget.
- **WasmWorld** — The top-level container of rooms. `world_tick()` advances every room, and `global_conservation_error()` measures total actuator output vs. total energy budget.
Plus manual **binary serialization** (`serialize_field`/`deserialize_field`, `serialize_world`/`deserialize_world`) — no serde, no allocator surprises, just little-endian byte slices.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. A zero-dependency WASM compilation target for PLATO core types. Provides world simulation primitives — vibe fields, agents, rooms, and a full world hierarchy — with hand-rolled binary serialization de

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** WASM, Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (184 lines), mentions tests, includes examples.

- README length: 255 lines, 9675 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
