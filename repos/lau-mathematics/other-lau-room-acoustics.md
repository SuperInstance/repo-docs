# lau-room-acoustics

## Intention

Room acoustics for PLATO — reverberation time, standing wave modes, resonance profiles, signal paths, and impulse response analysis, all implemented from first principles.

## How It Works

Given a room's physical dimensions (width, depth, height), wall absorption coefficient, and temperature, this library computes:
1. **Reverberation** — RT60 (Sabine equation), early decay time, clarity (C50/C80), definition (D50)
2. **Standing waves** — Axial, tangential, and oblique room modes up to a cutoff frequency
3. **Resonance profiles** — Mode density, Schröder frequency, problem frequency detection
4. **Signal paths** — Direct sound distance, first reflection (image source method), propagation delay, inverse-square attenuation
5. **Impulse responses** — Energy, frequency spectrum (DFT), causality check
6. **Full analysis** — One-stop characterisation: dead/live/balanced, problem spots, comparison between rooms

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Room acoustics for PLATO — reverberation time, standing wave modes, resonance profiles, signal paths, and impulse response analysis, all implemented from first principles.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (163 lines), mentions tests, includes examples.

- README length: 240 lines, 7484 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
