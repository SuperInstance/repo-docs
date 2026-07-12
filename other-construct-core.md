# construct-core

**Cluster:** fleet-agent-infra  
**Language:** Rust  
**Source:** [SuperInstance/construct-core](https://github.com/SuperInstance/construct-core)

## Intention

Hardware-agnostic agent runtime with layered trait system for the SuperInstance Construct API

## How It Works

[code]

## What It's For

Hardware-agnostic agent runtime with layered trait system for the SuperInstance Construct API

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (157 lines, 5777 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# construct-core

**The v2 layered trait system for the SuperInstance Construct API.**

This crate implements a hardware-agnostic agent runtime with three progressively
capable trait layers. Each layer adds capabilities — but also requirements. An
ESP32 implements only Layer 0. A DGX cluster implements all three.

## Architecture

```
┌─────────────────────────────────────────┐
│  Layer 2: AsyncConstruct                │  std + async (tokio)
│  • request_tool / release_tool          │  Tool lifecycle management
│  • query_async                          │  Async I/O, GPU, network
│  • active_tools                         │
├─────────────────────────────────────────┤
│  Layer 1: SyncConstruct                 │  no_std + alloc
│  • load_skill / unload_skill            │  Dynamic skill management
│  • query_owned                          │  Heap-allocated queries/responses
│  • loaded_skills                        │
├─────────────────────────────────────────┤
│  Layer 0: BareMetalConstruct            │  no_std, no alloc
│  • query_lookup                         │  O(1) table lookup
│  • capabilities                         │  Static capability introspection
│  • query (default impl)                 │  Stack-only, zero alloc
└─────────────────────────────────────────┘
```

## Why Split Traits This Way?

**Because hardware is not a spectrum — it's a taxonomy.** An ESP32 will never
have a heap. A Raspberry Pi will never run tokio. Rather than a single trait
with `unimplemented!()` stubs, we give each hardware class its own trait that
covers exactly what it can actually do.

This means:

- **Compile-time correctness**: If you have a `&dyn BareMetalConstruct`, the
  compiler guarantees you can't accidentally call `load_skill` on hardware that
  can't allocate.
- **Zero-cost abstractions**: No `Option<Box<dyn Tool>>` on bare metal. No
  `alloc::vec::Vec` on ESP32. Each layer uses only the primitives it needs.
- **Clear upgrade path**: Moving from ESP32 → Pi → DGX means implementing
  additional traits, not rewriting everything.

## Feature Gates

```toml
[features]
default = ["std"]
std = ["alloc"]        # Layer 2 + Layer 1 + Layer 0
alloc = []             # Layer 1 + Layer 0
bare-metal = []        # Layer 0 only
```

| Feature | Layers Available | Target |
|---------|-----------------|--------|
| `bare-metal` | 0 | ESP32, Cortex-M bare metal |
| `alloc` | 0 + 1 | Raspberry Pi, embedded Linux |
| `std` (default) | 0 + 1 + 2 | Workstation, DGX, Cloud |

## Usage

### Layer 0: Bare Metal (ESP32)

```rust
use construct_core::{BareMetalConstruct, EspConstruct, TritAction};

let esp = EspConstruct::new();
let action = esp.query_lookup(42);
println!("Action at index 42: {}", action);

let caps = esp.capabilities();
println!("Lookup table size: {}", caps.lookup_table_size);
```

### Layer 1: Sync (Raspberry Pi)

```rust
use construct_core::{SyncConstruct, PiConstruct, SkillId, QueryKind, OwnedQuery};

let mut pi = PiConstruct::new();
pi.load_skill(SkillId::Terna
```
