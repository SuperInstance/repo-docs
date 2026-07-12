# lau-shell-spawn

## Intention

Shell spawning system — Hermes creates child shells in their own sandboxes

## How It Works

`lau-shell-spawn` provides a Rust library for managing a hierarchy of **child shells**. A parent shell (typically Hermes) can:
- **Spawn** child shells of different kinds (ZeroClaw, CUDAClaw, Ensign, custom)
- **Template** common shell configurations for one-command instantiation
- **Sandbox** certain shell types so they can only access their own subtree
- **Budget** each child's resource consumption with conservation limits
- **Control** the full lifecycle: spawn → grant/revoke APIs → destroy
Every child shell carries its own set of ports, APIs, rooms, and a resource budget — all serializable to JSON for persistence or network transport.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Shell spawning system — Hermes creates child shells in their own sandboxes

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** CUDA, Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (238 lines), mentions tests, includes examples.

- README length: 336 lines, 11206 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (336 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
