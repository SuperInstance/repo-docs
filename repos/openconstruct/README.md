# OpenConstruct — Index

**Total repos: 6**

Hardware-agnostic agent runtime with a layered trait system for the SuperInstance Construct API. OpenConstruct defines three progressively capable layers — from bare-metal microcontrollers to full async compute clusters — so the same agent code runs on an ESP32, a laptop, or a DGX.

## Category Overview

### The Layered Trait System

The core innovation: **three trait layers**, each adding capabilities but also hardware requirements:

```
┌─────────────────────────────────────────┐
│  Layer 2: AsyncConstruct                │  std + async (tokio)
│  • request_tool / release_tool          │  Tool lifecycle management
│  • query_async                          │  Async I/O, GPU, network
│  • active_tools                         │
├─────────────────────────────────────────┤
│  Layer 1: SyncConstruct                 │  no_std + alloc
│  • load_skill / unload_skill            │  Dynamic skill management
│  • query_owned                          │  Heap-allocated queries
│  • loaded_skills                        │
├─────────────────────────────────────────┤
│  Layer 0: BareConstruct                 │  no_std, no alloc
│  • query                                │  Static queries only
│  • available_skills                     │  Compile-time skill list
│  • hardware_id                          │  Hardware identification
└─────────────────────────────────────────┘
```

- **ESP32** → Layer 0 only (no heap, no async)
- **Standard laptop** → Layer 0 + Layer 1 (heap allocation, dynamic skills)
- **DGX cluster** → All three layers (async I/O, GPU access, network)

### Repositories

- **construct-core** — The v2 layered trait system implementation. Hardware-agnostic runtime. 157-line README with architecture diagram and motivation. The flagship repository.
- **construct-coordination** — Coordination layer for multi-agent constructs
- **construct-hotswap** — Hot-swapping skills at runtime (load/unload without restart)
- **construct-provenance** — Provenance tracking — where did each piece of knowledge come from?
- **construct-supply-chain** — Supply chain management for agent capabilities
- **openconstruct-docs** — Ecosystem-wide documentation: architecture, API references, getting started, integration guides, best practices

### Key Interconnections

- **construct-core** provides the runtime that agents in agent-framework and superinstance-core build on
- The layered trait system connects to the broader polyglot strategy — Layer 0 implementations exist in C (si-core-c), Layer 2 in Rust
- **construct-hotswap** enables the dynamic skill loading that lau-agent-runtime requires
- **construct-provenance** connects to lau-provenance-chain for knowledge lineage tracking
- The OpenConstruct model is referenced throughout the cocapn-marine fleet coordination system
- The construct layer system mirrors the Grand Pattern polyglot approach: same concepts, different hardware targets

## Full Repository Listing

| Repo | Language | Description |
|------|----------|-------------|
| [construct-core](./other-construct-core.md) | Rust | Layered trait system (v2) — hardware-agnostic runtime |
| [construct-coordination](./other-construct-coordination.md) | Rust | Multi-agent coordination |
| [construct-hotswap](./other-construct-hotswap.md) | Rust | Runtime skill hot-swapping |
| [construct-provenance](./other-construct-provenance.md) | Rust | Knowledge provenance tracking |
| [construct-supply-chain](./other-construct-supply-chain.md) | Rust | Capability supply chain |
| [openconstruct-docs](./other-openconstruct-docs.md) | Markdown | Architecture, API refs, guides |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
