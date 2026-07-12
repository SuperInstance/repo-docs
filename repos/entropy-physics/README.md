# Entropy Physics — Index

**Total repos: 35**

Information theory, entropy coding, compression, symplectic geometry, tropical algebra, and negative space intelligence. This category brings together several physics-inspired mathematical frameworks that treat computation through the lens of thermodynamics, geometry, and information theory.

## Category Overview

### 1. Entropy & Compression (~13 repos)

Entropy coding fundamentals and data compression:
- **entropy-code** — Pure-Rust entropy coding: Shannon entropy, symbol probability, optimal code length, Kraft inequality, arithmetic coding
- **entropy-production** — Entropy production tracking
- **entropy-conservation** — Conservation of entropy
- **entropy-conservation-rs** — Rust conservation
- **entropy-flow-py** — Python entropy flow
- **entropy-gpu-rs** — GPU-accelerated entropy computation
- **entropy-lint** — Linter for entropy-related code
- **compress-rs** — General compression library
- **compress-bwt-rs** — Burrows-Wheeler Transform
- **compress-huffman-rs** — Huffman coding
- **compress-lz77-rs** — LZ77 compression
- **compress-rle-rs** — Run-length encoding
- **compress-trie-rs** — Trie-based compression

### 2. Symplectic Geometry (~8 repos)

Hamiltonian/symplectic methods for fleet state and music:
- **symplectic-fleet** — Fleet state as symplectic manifold with Noether conservation laws and structure-preserving integrators
- **symplectic-geometry** — Core symplectic geometry library
- **symplectic-physics** — Physics applications
- **symplectic-opt** — Symplectic optimization
- **symplectic-opt-rs** — Rust optimization
- **symplectic-music** — Symplectic methods for music
- **symplectic-spin** — Symplectic spinors

### 3. Tropical Algebra (~8 repos)

Tropical (min-plus) mathematics:
- **tropical-geometry** — Tropical geometry foundations
- **tropical-geometry-rs** — Rust implementation
- **tropical-algebra** — Tropical algebra
- **tropical-graph** — Tropical graph theory
- **tropical-attention** — Tropical attention mechanism for neural networks
- **tropical-attention-kernel** — GPU kernel for tropical attention
- **tropical-neural** — Tropical neural networks
- **tropical-synth** — Tropical sound synthesis
- **tropical-harmony-rs** — Tropical harmony in Rust

### 4. Negative Space Intelligence (~6 repos)

A novel framework: **intelligence is what you learn to AVOID, not what you choose.**
- **negative-space-core** — Core theory. The 294:1 conservation law: avoidance-to-choice ratio converges to ~294. Feedback refinement via EMA. Inference from absence — gaps between avoided options reveal undiscovered knowledge
- **negative-space-core-c** — C implementation
- **negative-space-core-python** — Python implementation
- **negative-space-interpolator** — Interpolation in negative space
- **negative-space-testing** — Testing framework
- **negative-knowledge** — Explicit knowledge about what NOT to do

### Key Interconnections

- **entropy-conservation** connects to the broader conservation-laws framework
- **symplectic-fleet** implements the same Noether conservation as conservation-laws and lau-conservation-laws
- **tropical-attention** relates to si-tropical-attention in superinstance-core
- **negative-space-core**'s 294:1 ratio is a conservation law — same mathematical framework
- Compression libraries (compress-*) provide the data layer for tile compression in forge-tiles
- **symplectic-music** connects to the music-spectral category
- **tropical-harmony-rs** bridges to music theory

## Full Repository Listing

### Entropy & Compression

| Repo | Language | Description |
|------|----------|-------------|
| [entropy-code](./other-entropy-code.md) | Rust | Shannon entropy, arithmetic coding |
| [entropy-production](./other-entropy-production.md) | Rust | Entropy production tracking |
| [entropy-conservation](./other-entropy-conservation.md) | Rust | Entropy conservation |
| [entropy-conservation-rs](./other-entropy-conservation-rs.md) | Rust | Rust entropy conservation |
| [entropy-flow-py](./other-entropy-flow-py.md) | Python | Python entropy flow |
| [entropy-gpu-rs](./other-entropy-gpu-rs.md) | Rust | GPU entropy computation |
| [entropy-lint](./other-entropy-lint.md) | Rust | Entropy code linter |
| [compress-rs](./other-compress-rs.md) | Rust | General compression |
| [compress-bwt-rs](./other-compress-bwt-rs.md) | Rust | Burrows-Wheeler Transform |
| [compress-huffman-rs](./other-compress-huffman-rs.md) | Rust | Huffman coding |
| [compress-lz77-rs](./other-compress-lz77-rs.md) | Rust | LZ77 compression |
| [compress-rle-rs](./other-compress-rle-rs.md) | Rust | Run-length encoding |
| [compress-trie-rs](./other-compress-trie-rs.md) | Rust | Trie-based compression |

### Symplectic Geometry

| Repo | Language | Description |
|------|----------|-------------|
| [symplectic-fleet](./other-symplectic-fleet.md) | Rust | Fleet as symplectic manifold |
| [symplectic-geometry](./other-symplectic-geometry.md) | Rust | Core symplectic geometry |
| [symplectic-physics](./other-symplectic-physics.md) | Rust | Physics applications |
| [symplectic-opt](./other-symplectic-opt.md) | Rust | Symplectic optimization |
| [symplectic-opt-rs](./other-symplectic-opt-rs.md) | Rust | Rust optimization |
| [symplectic-music](./other-symplectic-music.md) | Rust | Symplectic music |
| [symplectic-spin](./other-symplectic-spin.md) | Rust | Symplectic spinors |

### Tropical Algebra

| Repo | Language | Description |
|------|----------|-------------|
| [tropical-geometry](./other-tropical-geometry.md) | Rust | Tropical geometry foundations |
| [tropical-geometry-rs](./other-tropical-geometry-rs.md) | Rust | Rust tropical geometry |
| [tropical-algebra](./other-tropical-algebra.md) | Rust | Tropical (min-plus) algebra |
| [tropical-graph](./other-tropical-graph.md) | Rust | Tropical graph theory |
| [tropical-attention](./other-tropical-attention.md) | Rust | Tropical attention mechanism |
| [tropical-attention-kernel](./other-tropical-attention-kernel.md) | CUDA | GPU tropical attention |
| [tropical-neural](./other-tropical-neural.md) | Rust | Tropical neural networks |
| [tropical-synth](./other-tropical-synth.md) | Rust | Tropical sound synthesis |
| [tropical-harmony-rs](./other-tropical-harmony-rs.md) | Rust | Tropical harmony |

### Negative Space Intelligence

| Repo | Language | Description |
|------|----------|-------------|
| [negative-space-core](./other-negative-space-core.md) | Rust | Core theory — 294:1 avoidance ratio |
| [negative-space-core-c](./other-negative-space-core-c.md) | C | C implementation |
| [negative-space-core-python](./other-negative-space-core-python.md) | Python | Python implementation |
| [negative-space-interpolator](./other-negative-space-interpolator.md) | Rust | Negative space interpolation |
| [negative-space-testing](./other-negative-space-testing.md) | Rust | Testing framework |
| [negative-knowledge](./other-negative-knowledge.md) | Rust | Explicit negative knowledge |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
