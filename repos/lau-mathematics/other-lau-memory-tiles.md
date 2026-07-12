# lau-memory-tiles

## Intention

Memory tiles for AI agents — observations, actions, thoughts, decisions, dreams, and more.

## How It Works

This crate provides the memory substrate for an AI agent:
1. **TileType** — 9 typed memory categories: Observation, Action, Thought, Decision, Dream, Error, Signal, Response, and Custom.
2. **MemoryTile** — individual memory entries with importance scoring, access counting, embedding vectors, connections to other tiles, and arbitrary metadata.
3. **MemoryStore** — capacity-bounded tile storage with LRU-like eviction (lowest importance first), decay, reinforcement on access, pruning, and memory-pressure tracking.
4. **MemoryGraph** — weighted connection graph between tiles. Supports finding the strongest path between two tiles via BFS.
5. **MemoryQuery** — fluent builder for filtered, sorted queries over the store (by room, agent, type, importance, time range, content substring).
6. **MemoryConsolidator** — "dream phase" engine that groups similar tiles, creates Dream tiles summarizing clusters, connects them to originals, and decays the source tiles.
Everything is pure Rust, zero dependencies beyond `serde` + `serde_json`, and fully serializable.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Memory tiles for AI agents — observations, actions, thoughts, decisions, dreams, and more.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (213 lines), mentions tests, includes examples.

- README length: 298 lines, 9972 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (298 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
