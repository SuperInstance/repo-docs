# lau-songline

## Intention

Walking IS computing — Aboriginal songlines as executable algorithms

## How It Works

Aboriginal songlines are navigation systems encoded as songs. Each landmark in the song corresponds to a real place. Walking the songline executes the path. The rhythm encodes distance, the melody encodes direction, the verses encode landmarks.
This crate implements songlines as computational graphs:
- **Waypoints** are landmarks — computational checkpoints
- **Walking** executes the path between waypoints
- **Singing** is the execution trace — the audit log of what happened
- **Songline networks** connect multiple routes, enabling path composition
- **Navigation** finds paths through the network, but the path is always a *song*
The insight: computation isn't separate from the journey. The journey IS the computation.

## What It's For

Walking IS computing — Aboriginal songlines as executable algorithms

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (40 lines), mentions tests, includes examples.

- README length: 55 lines, 2329 characters
- Documented sections: The concept in 60 seconds, Quick start, Key types

## Honest Assessment

Part of the sprawling Lau/PLATO ecosystem. The README covers basics but the project is one of many math/computation crates in this organization. The breadth of repos in SuperInstance (hundreds) raises questions about depth vs. breadth — many appear to be auto-generated or lightly documented. **This crate likely works as a component but standalone value is limited without the broader ecosystem.**
