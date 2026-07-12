# lau-shell-transport

## Intention

Transport layer for inter-shell communication — message passing via files, stdio, and memory.

## How It Works

`lau-shell-transport` solves the problem of **how shell instances talk to each other**. It provides:
1. **A `Transport` trait** — a unified interface for `send`, `receive`, `poll`, `close`, and `is_connected` that works across any I/O backend.
2. **`MemoryTransport`** — in-memory inbox/outbox queues for testing and same-process communication.
3. **`StdioTransport`** — length-prefixed binary frames over stdin/stdout (or any `Read + Write` pair) for subprocess communication.
4. **`FileTransport`** — JSONL files with `flock(2)` locking for cross-process, disk-based message passing with cursor tracking.
5. **`TransportRouter`** — a multiplexer that routes messages to the correct transport by shell ID, with broadcast (`"*"`) support.
6. **`Envelope`** — a rich message container with UUID IDs, priority levels, TTL expiry, correlation IDs, and typed message categories.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Transport layer for inter-shell communication — message passing via files, stdio, and memory.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (193 lines), mentions tests, includes examples.

- README length: 290 lines, 9648 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
