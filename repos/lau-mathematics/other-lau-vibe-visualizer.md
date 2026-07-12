# lau-vibe-visualizer

## Intention

Turns the mono-dimensional vibe scalar into voxel colors, materials, heights, and particle effects. The vibe is one number (-1.0 to 1.0) — everything visual follows deterministically from that number.

## How It Works

`lau-vibe-visualizer` is the rendering math layer for the Lau voxel game. Given a 16×16 grid of vibe values (a `VibeField`), it computes:
- **Colors** for every voxel column, interpolated between cold blue (negative), gray (neutral), and warm gold (positive)
- **Materials** — 9 voxel types from ice to starblock, determined by vibe thresholds
- **Heights** — base height ± vibe × 16 blocks
- **Particle density** — absolute vibe scaled to 0–100
It also provides `RoomVisualization`, a ready-to-use struct that packages a vibe field with visualization mode and color map, plus conservation error checking between fields.

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Turns the mono-dimensional vibe scalar into voxel colors, materials, heights, and particle effects. The vibe is one number (-1.0 to 1.0) — everything visual follows deterministically from that number.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (183 lines), mentions tests, includes examples.

- README length: 260 lines, 8270 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
