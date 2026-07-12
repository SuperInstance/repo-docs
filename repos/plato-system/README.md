# PLATO System

**Protocol for Layered Agent Tile Orchestration** — a room-based agent system where knowledge is stored as tiles within rooms, agents navigate between rooms, and a deadband protocol governs decision-making priorities. **262 repos.**

---

## What Is PLATO?

PLATO is the knowledge system at the heart of the SuperInstance ecosystem. Named after the original PLATO terminal-based education system and inspired by MUD (Multi-User Dungeon) architecture, it implements a world where:

- **Knowledge lives in tiles** — Q&A pairs with confidence scores, provenance, and dependency tracking
- **Rooms contain tiles** — collections of related knowledge that compute their own "conservation ratio"
- **Agents navigate rooms** — discovering, reading, and writing tiles as they move
- **Deadband protocol governs priorities** — P0 (safety) → P1 (channel) → P2 (optimize)

The core ideas:

1. **Knowledge as Tiles** — each tile is a 384-byte binary structure with domain, confidence, belief, provenance
2. **Rooms as Containers** — collections of tiles with temperature states (Cold/Warm/Hot/Crystallized)
3. **Deadband Protocol** — priority governance ensuring safety-first decision making
4. **Ternary Sensors** — all sensor readings reduced to {-1, 0, +1} for compact fleet-wide state
5. **Multi-language Engine Blocks** — room runtime implemented in Rust, C, Elixir, Gleam, Zig, Chapel
6. **Fleet Coordination** — agents discover rooms, navigate between them, share knowledge

---

## Room Taxonomy

PLATO rooms come in several varieties:

| Room Type | Purpose | Example |
|-----------|---------|---------|
| Knowledge rooms | Store and serve tiles | plato-room-server (15 rooms, 16K+ tiles) |
| MUD rooms | Text-based agent training | plato-mud-server (16 rooms) |
| Music rooms | Room-as-musician, tile-as-note | plato-room-musician (MIDI output) |
| Live rooms | Real-time agent simulation | plato-live-room (forward simulations, walls) |
| Training rooms | LoRA adapter lifecycle | plato-training (Active/Superseded/Retracted) |
| Dojo rooms | Cultural perspective decoupling | plato-dojo |
| Afterlife rooms | Ghost tiles, knowledge preservation | plato-afterlife |

Room temperature states control processing:
- **Cold** — dormant, minimal processing
- **Warm** — active, accepting tiles
- **Hot** — intensive training/retraining
- **Crystallized** — frozen, read-only knowledge

---

## Server / Runtime / Engine Block Variants

The PLATO room runtime has been implemented across multiple languages, each showcasing language-specific strengths:

### Server & Runtime

| Repo | Language | Description |
|------|----------|-------------|
| [plato-server](https://github.com/SuperInstance/plato-server) | Rust | Standalone knowledge system — run your own, connect to the fleet. 15KB README, the flagship |
| [plato-runtime](https://github.com/SuperInstance/plato-runtime) | Rust | Self-discovering, self-optimizing compute runtime — tiny core, grows to fill resources |
| [plato-runtime-kernel](https://github.com/SuperInstance/plato-runtime-kernel) | Rust | Conservation-verified computation — AI theorem prover |
| [plato-kernel](https://github.com/SuperInstance/plato-kernel) | Rust | Central state machine — DCS flywheel, belief scoring, tile processing |
| [plato-shell](https://github.com/SuperInstance/plato-shell) | Rust | Agent runtime environment — command execution, context management |

### Multi-Language Engine Blocks

| Repo | Language | Size | Description |
|------|----------|------|-------------|
| [plato-engine-block](https://github.com/SuperInstance/plato-engine-block) | Rust | 8.5KB | Atomic room runtime — universal agent-space interface |
| [plato-engine-block-c](https://github.com/SuperInstance/plato-engine-block-c) | C99 | 10.9KB | Tiny embeddable sensor→history→alarm engine. Zero dynamic allocation |
| [plato-engine-block-elixir](https://github.com/SuperInstance/plato-engine-block-elixir) | Elixir | 14.1KB | Fault-tolerant marine vessel monitoring on BEAM/OTP |
| [plato-engine-block-gleam](https://github.com/SuperInstance/plato-engine-block-gleam) | Gleam | 4.2KB | Type-safe variant |
| [plato-engine-block-zig](https://github.com/SuperInstance/plato-engine-block-zig) | Zig | 12.6KB | Systems-level implementation |
| [plato-fleet-chapel](https://github.com/SuperInstance/plato-fleet-chapel) | Chapel | 13.7KB | HPC-oriented fleet management |

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────┐
│                    Fleet Layer                            │
│  (plato-fleet-manager, plato-ship, plato-scout)          │
└────────────────────────┬────────────────────────────────┘
                         │
┌────────────────────────▼────────────────────────────────┐
│              Agent Framework Layer                        │
│  (plato-agent-python, plato-agent-academy, plato-dcs,    │
│   plato-deadband, plato-escalation-gate)                 │
└────────────────────────┬────────────────────────────────┘
                         │
┌────────────────────────▼────────────────────────────────┐
│              Room & Tile Layer                            │
│  (plato-room-*, plato-tile-*)                             │
│  Room lifecycle │ Tile CRUD │ Scoring │ Search │ Dedup   │
└────────────────────────┬────────────────────────────────┘
                         │
┌────────────────────────▼────────────────────────────────┐
│            Engine Block Layer                              │
│  (Rust, C, Elixir, Gleam, Zig, Chapel variants)          │
│  Sensor → History → Alarm pipeline                        │
└────────────────────────┬────────────────────────────────┘
                         │
┌────────────────────────▼────────────────────────────────┐
│            Signal Processing Layer                         │
│  (plato-filter, plato-transform, plato-anomaly,           │
│   plato-compress, plato-ring, plato-window)               │
└────────────────────────┬────────────────────────────────┘
                         │
┌────────────────────────▼────────────────────────────────┐
│            ML/AI Layer                                     │
│  (plato-jepa, plato-mythos, plato-torch, plato-distill)  │
└─────────────────────────────────────────────────────────┘
```

---

## Tile Format

The canonical PLATO tile (v2.1 spec) is a 384-byte binary structure:

| Field | Size | Purpose |
|-------|------|---------|
| Domain | variable | Knowledge domain (e.g., "marine", "music") |
| Confidence | float | 0.0–1.0 confidence in the answer |
| Belief | float | Belief score after multi-signal fusion |
| Provenance | hash | Cryptographic provenance chain |
| Question | text | The query |
| Answer | text | The response |
| Dependencies | list | Other tiles this depends on |
| Temporal | timestamp | Freshness and decay tracking |

Tiles go through a 7-signal scoring pipeline: keyword, belief, domain, temporal, ghost, frequency, and controversy. Multi-signal fusion combines these into a unified belief score.

---

## Deadband Protocol

The deadband is PLATO's priority governance system:

| Priority | Name | Behavior |
|----------|------|----------|
| **P0** | Rock | Safety-critical. Always fires. Cannot be deferred. |
| **P1** | Channel | Normal operations. Processed in order. |
| **P2** | Optimize | Optimization and cleanup. Deferred when busy. |

This ensures that safety-critical operations (like anomaly detection) always take precedence over optimization tasks.

---

## Key Repositories by Category

### Core Infrastructure (11 repos)

- **plato-core** — Foundation types and mesh registry (3.9KB README)
- **plato-server** — Standalone knowledge system, the flagship (15.3KB README)
- **plato-runtime** — Self-discovering compute runtime (4.2KB)
- **plato-runtime-kernel** — Conservation-verified AI theorem prover (6.5KB)
- **plato-kernel** — DCS flywheel, belief scoring, tile processing
- **plato-schema** — JSON schema validation and versioning
- **plato-config** — Configuration management
- **plato-event** — Event bus for PLATO nervous system
- **plato-types** — Core types — lifecycle, Lamport clocks, provenance
- **plato-shell** — Agent runtime environment
- **plato-mud-server** — Text-based agent training ground, 16 rooms

### Clients & SDKs (7 repos)

- **plato-sdk** — Python SDK: "Build agents that live in PLATO" (11KB README)
- **plato-sdk-unified** — All 8 consciousness packages in one import
- **plato-client** — Rust client library
- **plato-client-js** — Node + browser, zero dependencies
- **plato-client-php** — PHP client (12KB README)
- **plato-client-ruby** — Ruby client
- **plato-agent-connect** — One-command CLI to join the fleet

### ML/AI & Training (23 repos)

- **plato-jepa** — JEPA primitives for tile representation learning (6.1KB)
- **plato-jepa-dual** — Dual-database JEPA with perception/prediction spaces
- **plato-mythos** — Recurrent-Depth Transformer — rooms as MoE experts (9.3KB)
- **plato-torch** — PyTorch GPU training loop with tile framing (7.4KB)
- **plato-distill** — Progressive knowledge distillation (3.8KB)
- **plato-fflearning** — Forward-Forward learning without backprop (5.2KB)
- **plato-audio-jepa** — Audio JEPA (4KB)
- **plato-vision-jepa** — Vision JEPA (3.8KB)
- **plato-model-ocean** — Cellular intelligence ecosystem (3.6KB)
- **plato-backprop** — Backpropagation-through-prompt tracking
- **plato-forge-daemon** — Continuous learning daemon — GPU training loop

### Signal Processing & DSP (10 repos)

- **plato-filter** — Digital signal processing filters (3.3KB)
- **plato-transform** — Data transformation pipeline (3KB)
- **plato-anomaly** — Anomaly detection methods (2KB)
- **plato-compress** — Lossless and lossy compression (2.3KB)
- **plato-correlate** — Cross-correlation and dependency detection (2.4KB)
- **plato-downsample** — Intelligent downsampling with anomaly preservation
- **plato-normalize** — Normalization and standardization (2.5KB)
- **plato-ring** — Lock-free ring buffer for high-frequency data (2.2KB)
- **plato-window** — Sliding window operations (1.8KB)
- **plato-signal-chain** — Composable 5-layer signal chain pipeline

### Bridges & Integrations (15 repos)

- **plato-mcp** — PLATO rooms as MCP tools (4KB)
- **plato-ternary-bridge** — Plato sensor values to ternary {-1,0,+1} (12.8KB)
- **plato-matrix-bridge** — Connects PLATO to fleet Matrix mesh (2.9KB)
- **plato-flux-compiler** — FLUX bytecode compilation for rooms (9.3KB)
- **plato-sim-bridge** — PLATO ↔ Fleet simulator bridge
- **plato-midi-bridge** — Rooms as musicians via MIDI
- **plato-hdc-bridge** — Hyperdimensional computing bridge
- **plato-llvm-bridge** — LLVM integration

### Vessels / IoT / Hardware (4 repos)

- **plato-vessel-core** — Tiny C PLATO client for ESP32/RP2040 (6.3KB)
- **plato-vessel-technician** — Marine/industrial technician agent (5.3KB)
- **plato-vessel-educational** — Student + instructor agent for IoT classrooms (4.3KB)
- **plato-vessel-rapid-prototype** — Product developer iteration loop (3.7KB)

### Security & Governance (8 repos)

- **plato-policy** — Policy engine gating agent actions
- **plato-sandbox** — Sandboxed execution environment
- **plato-provenance** — Zero-trust tile provenance — signing, verification
- **plato-constraints** — Rule enforcement — forbidden patterns
- **plato-validate** — Input validation and sanitization (2KB)
- **plato-lab-guard** — Hypothesis gating — 12 absolute quantifiers

### Developer Tools (8 repos)

- **plato-cli** — PLATO in one binary (3KB)
- **plato-dashboard** — Fleet dashboard (6KB)
- **plato-demo** — HN demo with pre-seeded knowledge (7.1KB)
- **plato-quickstart** — Bootstrap a room in 30 seconds (4.3KB)
- **plato-studio** — Web dashboard for knowledge store
- **plato-tui** — Terminal UI (2.5KB)

---

## Ecosystem Statistics

- **Total repos:** 262
- **Substantial docs (2000+ bytes):** 99
- **Moderate docs (500–2000 bytes):** 73
- **Minimal docs (120–500 bytes):** 21
- **Stubs (<120 bytes):** 69

---

## Assessment

PLATO is an ambitious, sprawling ecosystem implementing a room-based agent system with genuine architectural depth. The Rust crates (`plato-room`, `plato-shell`, `plato-engine-block`, `plato-ternary-bridge`, `plato-flux-compiler`) contain substantial, documented code with real architecture. The Python SDK and server are genuinely functional. The multi-language engine blocks show real engagement with language-specific strengths.

A large fraction of the repos (especially `plato-tile-*` and `plato-room-*` Python packages) are stubs. The ML components are conceptually rich but training effectiveness is unproven. The ecosystem is more impressive in breadth than depth, but the depth where it exists is genuine.

---

*Individual repo summaries are in `plato-{repo-name}.md` files in this directory.*
