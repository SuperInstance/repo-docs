# plato-loader

## Intention
PLATO loading program — reads rooms, computes knowledge graphs, produces minimal update sets. Pure Rust.

## How It Works
Agents walk into a room, load knowledge, walk out knowing things. Parses knowledge tiles from [plato-room](https://github.com/SuperInstance/plato-room), builds dependency graphs, diffs against previous loads, and produces minimal updates. **Part of the [Plato](https://github.com/SuperInstance/plato-shell) ecosystem.** - **Parse tiles** — read knowledge units from a room (concepts, procedures, facts, code patterns)

## What It's For
Part of the PLATO ecosystem. PLATO loading program — reads rooms, computes knowledge graphs, produces minimal update sets. Pure Rust.

## Who Would Use It
PLATO ecosystem developers and SuperInstance fleet operators.

## Language / Stack
Rust

## Status Assessment
🟢 Moderate — has real documentation with concepts and some code

## Honest Assessment
Real implementation with documented concepts, code examples, and test coverage. This is a working component of the PLATO ecosystem, not just a placeholder.

## README Substance Level
- **Size:** 1929 bytes
- **Substance:** moderate
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Gives You, Quick Start, How It Fits, Installation, Testing, License
