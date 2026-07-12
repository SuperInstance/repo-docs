# Exocortex Memory — Index

**Total repos: 11**

The exocortex-memory collection implements persistent semantic memory for AI agents across a polyglot set of language implementations. The core idea: an "exocortex" — external brain — that gives AI agents durable, queryable, typed memory with confidence scoring, ternary embeddings, and multi-modal retrieval.

## Category Overview

This is a tightly focused polyglot implementation family. One conceptual system (the Exocortex Compute Kernel + Semantic Memory Store) implemented across 11 languages and runtimes:

### The Concept

The exocortex stores **Insights** — discrete pieces of knowledge — each annotated with:
- **Ternary embedding vectors** — compact {-1, 0, +1} discretized representations
- **Tags** — categorical metadata for filtering
- **Confidence** — uncertainty quantification [0, 1]
- **Timestamps** — temporal provenance
- **Source** — where the knowledge came from

### Implementations by Language

| Language | Repo | Role |
|----------|------|------|
| **C** | exocortex-kernel-c | Core compute kernel (984-line README) — matrix ops, stats, ternary |
| **Zig** | exocortex-memory-zig | Comptime-verified semantic memory (874-line README) |
| **C++** | exocortex-ast-cpp | AST-based knowledge parsing |
| **Mojo** | exocortex-embed-mojo | Mojo embedding engine |
| **Lua** | exocortex-script-lua | Scripting interface |
| **Python** | exocortex-tiny-py | Minimal Python implementation |
| **Chapel** | exocortex-fleet-chapel | Parallel fleet memory |
| **TypeScript** | exocortex-mcp-ts | MCP (Model Context Protocol) server |
| **WebAssembly** | exocortex-wasm-runtime | WASM runtime |
| **ESP32** | exocortex-esp32 | Embedded edge deployment |
| **Multi** | exocortex-clients | Client libraries |

### Key Interconnections

- The **C kernel** (exocortex-kernel-c) is the reference implementation with the most documentation
- The **Zig** implementation adds compile-time schema verification — a genuinely interesting use of Zig's comptime
- The **TypeScript MCP server** connects to broader AI ecosystems via Model Context Protocol
- The **ESP32** deployment shows the ambition: memory that runs on microcontrollers
- Ternary embeddings connect to the broader ternary math ecosystem
- This is the memory layer that Lau agents (lau-mathematics) and SuperInstance agents (superinstance-core) would use for persistent state

## Full Repository Listing

| Repo | Language | Description |
|------|----------|-------------|
| [exocortex-kernel-c](./other-exocortex-kernel-c.md) | C | Core compute kernel — matrix, stats, ternary ops |
| [exocortex-memory-zig](./other-exocortex-memory-zig.md) | Zig | Comptime-verified semantic memory store |
| [exocortex-ast-cpp](./other-exocortex-ast-cpp.md) | C++ | AST-based knowledge representation |
| [exocortex-embed-mojo](./other-exocortex-embed-mojo.md) | Mojo | Mojo embedding engine |
| [exocortex-script-lua](./other-exocortex-script-lua.md) | Lua | Lua scripting interface |
| [exocortex-tiny-py](./other-exocortex-tiny-py.md) | Python | Minimal Python exocortex |
| [exocortex-fleet-chapel](./other-exocortex-fleet-chapel.md) | Chapel | Parallel fleet memory |
| [exocortex-mcp-ts](./other-exocortex-mcp-ts.md) | TypeScript | MCP server for AI integration |
| [exocortex-wasm-runtime](./other-exocortex-wasm-runtime.md) | WASM | WebAssembly runtime |
| [exocortex-esp32](./other-exocortex-esp32.md) | C/C++ | ESP32 embedded deployment |
| [exocortex-clients](./other-exocortex-clients.md) | Multi | Client libraries |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
