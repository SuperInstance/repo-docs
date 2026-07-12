# lau-memory-arena

## Intention

Custom arena allocator for game entities — pre-allocated pools, generation-based IDs, no runtime alloc on hot path.

## How It Works

`lau-memory-arena` provides two core types:
- **`Arena<T>`** — A pre-allocated, generation-based arena allocator that stores values in a contiguous `Vec<T>`. Allocation reuses freed slots via a free list and only grows when new capacity is needed past the initial reserve. Deallocation increments the entry's generation so stale IDs become invalid.
- **`SlotMap<T>`** — An ergonomic wrapper around `Arena<T>` with a slot-map-style API including iteration and `retain`.
Plus ready-made type aliases:
- `EntityArena = Arena<EntitySlot>` — for game entities with a component mask
- `VibeArena = Arena<f64>` — for vibe/energy values
---

## What It's For

Custom arena allocator for game entities — pre-allocated pools, generation-based IDs, no runtime alloc on hot path.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (240 lines), mentions tests, includes examples.

- README length: 349 lines, 11723 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (349 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
