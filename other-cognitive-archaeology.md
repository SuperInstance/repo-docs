# cognitive-archaeology

**Cluster:** ai-cognitive  
**Language:** Rust  
**Source:** [SuperInstance/cognitive-archaeology](https://github.com/SuperInstance/cognitive-archaeology)

## Intention

See README.

## How It Works

[code]

## What It's For

See README.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (187 lines, 5713 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Cognitive Archaeology

[![crates.io](https://img.shields.io/crates/v/cognitive-archaeology.svg)](https://crates.io/crates/cognitive-archaeology)
[![docs.rs](https://docs.rs/cognitive-archaeology/badge.svg)](https://docs.rs/cognitive-archaeology)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> **Layered cognitive history with archaeological excavation — dig through the strata of an agent's mind.**

---

## The Problem

Agent cognition evolves over time. An agent that started with basic reflexes later developed planning, then self-awareness. But when debugging or auditing an agent, there's no way to "dig down" through these layers to understand how a particular behavior originated. The history is either flat (all events in one list) or lost entirely.

## Why This Exists

Cognitive Archaeology models an agent's history as **geological strata** — layered deposits where the oldest layers are at the bottom and the most recent are on top. You can excavate through these layers to discover the origins of thoughts, analyze density patterns, and recover artifacts with surrounding context.

## Architecture

```
  ╔═══════════════════════════════════╗
  ║  Reflective (density: 0.9)       ║ ← TOP (most recent)
  ║  "Self-awareness, metacognition"  ║
  ╠═══════════════════════════════════╣
  ║  Deliberative (density: 0.7)     ║
  ║  "Planning, reasoning"           ║
  ╠═══════════════════════════════════╣
  ║  Reactive (density: 0.4)         ║
  ║  "Reflexive behavior"            ║
  ╠═══════════════════════════════════╣
  ║  Primitive (density: 0.2)        ║ ← BOTTOM (oldest)
  ║  "Basic perception"              ║
  ╚═══════════════════════════════════╝
  
  Excavation: dig_to(depth) → find_origin(predicate) → recover_artifact
  Stratigraphy: analyze density gradients, find densest layers
```

## Installation

```toml
[dependencies]
cognitive-archaeology = "0.1"
```

## API Reference

### `Stratum`

A cognitive layer with timestamp, label, data, and density:

```rust
use cognitive_archaeology::Stratum;

let s = Stratum::new("s1", 100.0, "primitive", "basic perception", 0.2);
assert_eq!(s.age(150.0), 50.0);
```

### `ArchaeologicalSite`

A stack of strata representing cognitive history:

```rust
use cognitive_archaeology::*;

let mut site = ArchaeologicalSite::new();
site.deposit(Stratum::new("s1", 100.0, "primitive", "basic perception", 0.2));
site.deposit(Stratum::new("s2", 200.0, "reactive", "reflexive behavior", 0.4));
site.deposit(Stratum::new("s3", 300.0, "deliberative", "planning layer", 0.7));
site.deposit(Stratum::new("s4", 400.0, "reflective", "self-awareness", 0.9));

assert_eq!(site.depth(), 4);
assert_eq!(site.bottom().unwrap().label, "primitive");
assert_eq!(site.top().unwrap().label, "reflective");
```

### `Excavation`

Dig through layers to find origins:

```rust
use cognitive_archaeology::*;

let site = /* ... build site ... */;
let excavation = Excavation::new(&site);

// Dig to specific depth
let layer = ex
```
