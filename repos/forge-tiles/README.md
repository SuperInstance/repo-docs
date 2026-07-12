# Forge Tiles — Index

**Total repos: 39**

The ForgeFlux ecosystem: a tile-based pipeline system that decomposes data, code, audio, images, and text into transformable tiles, processes them through conservation-aware pipelines, and reassembles the results. Tiles are the atomic unit of computation — everything becomes tiles, tiles get transformed, tiles get composed.

## Category Overview

### The Tile Abstraction

Tiles are uniform units of computation that flow through pipelines:
- Source material (code, audio, images, text) is decomposed into tiles
- Tiles flow through transform pipelines with conservation ratio tracking
- Conservation laws (from the SuperInstance spectral conservation theorems T1–T5) verify that information isn't lost
- Processed tiles are reassembled into output

### Sub-domains

#### 1. Core Forge System (~15 repos)

- **forge-cli** — Unified CLI tying all forge-* crates together
- **forge-code** — Source code → tiles → PLATO agents
- **forge-code-archaeologist** — Archaeological analysis of code history through tiles
- **forge-conservation** — Conservation ratio tracking for tile transforms (implements T1–T5 theorems)
- **forge-pipeline** — Pipeline orchestration for tile flows
- **forge-flux** — FLUX protocol integration
- **forge-meta** — Metadata management
- **forge-tick** — Tick-based scheduling
- **forge-transform** — Tile transformation library
- **forge-detect** — Pattern detection in tiles
- **forge-memory** — Memory management for tile state
- **forge-data** — Data handling
- **forge-a2a** — Agent-to-agent tile exchange
- **forge-pi** — Raspberry Pi deployment

#### 2. Media Processing (~4 repos)

- **forge-audio** — Audio → tiles → processing
- **forge-image** — Image → tiles → processing
- **forge-text** — Text → tiles → processing
- **forge-subtitle** — Subtitle → tiles → processing
- **forge-soniqo** — Sonic/audio analysis

#### 3. Sensor & IoT (~1 repo)

- **forge-sensor** — Sensor data → tiles

#### 4. Tile Infrastructure (~8 repos)

- **tile-compiler** — Compiling tile definitions
- **tile-cuda** — GPU-accelerated tile processing
- **tile-neon** — ARM NEON optimized tiles
- **tile-opencl** — OpenCL tile kernels
- **tile-lifecycle** — Tile lifecycle management
- **tile-lock-synthesis** — Lock synthesis for concurrent tile access
- **tile-memory-early-version** — Early tile memory system
- **tile-refiner** — Tile refinement
- **tile-chain** — Tile blockchain / provenance chain

#### 5. Sketch / Experimental (~9 repos)

Experimental and exploratory work:
- **sketch-composite-headspace** — Composite headspace exploration
- **sketch-fleet-oracle-construct** — Fleet oracle constructs
- **sketch-forgemaster-experiments** — Forgemaster experiments
- **sketch-gc-pid-feedback-loop** — GC/PID feedback loops
- **sketch-oracle2-construct-readme** — Oracle v2 constructs
- **sketch-rotation-adaptation-to-fleet-oracle** — Rotation adaptation
- **sketch-rotation-audit-provenance** — Rotation audit provenance
- **sketch-self-hosting-construct** — Self-hosting constructs
- **sketch-ternary-kihn-metaphor** — Ternary Kihn metaphor
- **sketch-workspace-sketchbook-pattern** — Workspace sketchbook patterns

### Key Interconnections

- **forge-conservation** implements the same conservation theorems as the conservation-laws category
- **forge-code** produces tiles that feed into PLATO agents (plato-system category)
- **tile-cuda/tile-neon/tile-opencl** provide the same GPU/hardware acceleration pattern as oxide-gpu
- **forge-flux** integrates with the FLUX protocol used by agent-framework
- **forge-a2a** uses the agent-to-agent protocol from lau-mathematics
- The tile metaphor connects to lau-memory-tiles and lau-tile-compress in lau-mathematics

## Full Repository Listing

### Forge Core

| Repo | Language | Description |
|------|----------|-------------|
| [forge-cli](./other-forge-cli.md) | Rust | Unified CLI for ForgeFlux |
| [forge-code](./other-forge-code.md) | Rust | Code → tiles → PLATO agents |
| [forge-code-archaeologist](./other-forge-code-archaeologist.md) | Rust | Code history archaeology |
| [forge-conservation](./other-forge-conservation.md) | Rust | Conservation ratio tracking (T1–T5) |
| [forge-pipeline](./other-forge-pipeline.md) | Rust | Pipeline orchestration |
| [forge-flux](./other-forge-flux.md) | Rust | FLUX integration |
| [forge-meta](./other-forge-meta.md) | Rust | Metadata management |
| [forge-tick](./other-forge-tick.md) | Rust | Tick scheduling |
| [forge-transform](./other-forge-transform.md) | Rust | Transform library |
| [forge-detect](./other-forge-detect.md) | Rust | Pattern detection |
| [forge-memory](./other-forge-memory.md) | Rust | Memory management |
| [forge-data](./other-forge-data.md) | Rust | Data handling |
| [forge-a2a](./other-forge-a2a.md) | Rust | Agent-to-agent exchange |
| [forge-pi](./other-forge-pi.md) | Rust | Raspberry Pi deployment |

### Media Processing

| Repo | Language | Description |
|------|----------|-------------|
| [forge-audio](./other-forge-audio.md) | Rust | Audio processing |
| [forge-image](./other-forge-image.md) | Rust | Image processing |
| [forge-text](./other-forge-text.md) | Rust | Text processing |
| [forge-subtitle](./other-forge-subtitle.md) | Rust | Subtitle processing |
| [forge-soniqo](./other-forge-soniqo.md) | Rust | Sonic analysis |

### Sensor

| Repo | Language | Description |
|------|----------|-------------|
| [forge-sensor](./other-forge-sensor.md) | Rust | Sensor data tiles |

### Tile Infrastructure

| Repo | Language | Description |
|------|----------|-------------|
| [tile-compiler](./other-tile-compiler.md) | Rust | Tile compilation |
| [tile-cuda](./other-tile-cuda.md) | CUDA | GPU tiles |
| [tile-neon](./other-tile-neon.md) | ARM | NEON optimized tiles |
| [tile-opencl](./other-tile-opencl.md) | OpenCL | OpenCL tiles |
| [tile-lifecycle](./other-tile-lifecycle.md) | Rust | Lifecycle management |
| [tile-lock-synthesis](./other-tile-lock-synthesis.md) | Rust | Lock synthesis |
| [tile-memory-early-version](./other-tile-memory-early-version.md) | Rust | Early memory system |
| [tile-refiner](./other-tile-refiner.md) | Rust | Tile refinement |
| [tile-chain](./other-tile-chain.md) | Rust | Tile provenance chain |

### Sketch / Experimental

| Repo | Language | Description |
|------|----------|-------------|
| [sketch-composite-headspace](./other-sketch-composite-headspace.md) | Rust | Composite headspace |
| [sketch-fleet-oracle-construct](./other-sketch-fleet-oracle-construct.md) | Rust | Fleet oracle |
| [sketch-forgemaster-experiments](./other-sketch-forgemaster-experiments.md) | Rust | Forgemaster experiments |
| [sketch-gc-pid-feedback-loop](./other-sketch-gc-pid-feedback-loop.md) | Rust | GC/PID feedback |
| [sketch-oracle2-construct-readme](./other-sketch-oracle2-construct-readme.md) | Rust | Oracle v2 |
| [sketch-rotation-adaptation-to-fleet-oracle](./other-sketch-rotation-adaptation-to-fleet-oracle.md) | Rust | Rotation adaptation |
| [sketch-rotation-audit-provenance](./other-sketch-rotation-audit-provenance.md) | Rust | Rotation audit |
| [sketch-self-hosting-construct](./other-sketch-self-hosting-construct.md) | Rust | Self-hosting |
| [sketch-ternary-kihn-metaphor](./other-sketch-ternary-kihn-metaphor.md) | Rust | Ternary Kihn |
| [sketch-workspace-sketchbook-pattern](./other-sketch-workspace-sketchbook-pattern.md) | Rust | Sketchbook patterns |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
