# lau-ts-bridge

## Intention

TypeScript bridge between the PLATO backend (Rust) and the Lau game frontend (browser/engine). Converts the mono-dimensional vibe scalar into colors, heights, materials, and game events. Provides noise functions for procedural world generation, conservation checking, and a kid-friendly naming layer 

## How It Works

`lau-ts-bridge` is the glue between the backend simulation and the game the player sees. The core idea: the entire world state is driven by a single number — the **vibe** (ranging from -1.0 to 1.0). This library provides pure functions that deterministically map that number to:
- **Colors** (negative = blue, zero = gray, positive = gold)
- **Materials** (ice → water → stone → grass → wood → sand → crystal → glowstone → starblock)
- **Heights** (vibe × 16 blocks offset from base)
- **Game events** (weather changes, music BPM shifts)
- **World generation** via hash-based noise and fractal Brownian motion
It also includes a **conservation checker** (verify that vibe is preserved across transformations) and **iteration classification** for the tutoring system.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. TypeScript bridge between the PLATO backend (Rust) and the Lau game frontend (browser/engine). Converts the mono-dimensional vibe scalar into colors, heights, materials, and game events. Provides nois

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** TypeScript

## Status Assessment

**Status: MODERATE**

Reasonable README (181 lines), mentions tests, includes examples.

- README length: 251 lines, 8429 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
