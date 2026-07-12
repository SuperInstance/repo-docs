# Constraint Repos — Index

Total repos: 45

| Repo | Language | Description |
|------|----------|-------------|
| [constraint-audio](./constraint-constraint-audio.md) | Rust | Rust audio DSP built on lattice consonance theory |
| [constraint-bench-suite](./constraint-constraint-bench-suite.md) | C | AVX-512 + CUDA benchmark suite |
| [constraint-crdt](./constraint-constraint-crdt.md) | Rust | CRDT-backed constraint states for distributed consensus |
| [constraint-demo](./constraint-constraint-demo.md) | HTML | Browser-based fleet constraint awareness demo |
| [constraint-demos](./constraint-constraint-demos.md) | HTML | Interactive HTML demos for constraint theory |
| [constraint-dialect](./constraint-constraint-dialect.md) | C++ | MLIR Constraint Dialect |
| [constraint-dsl](./constraint-constraint-dsl.md) | Python | Declarative YAML-like DSL for constraint graphs |
| [constraint-dynamics](./constraint-constraint-dynamics.md) | Rust | Physics of constraints |
| [constraint-dynamics-rs](./constraint-constraint-dynamics-rs.md) | Rust | Constraint dynamics for agent behavior |
| [constraint-flow](./constraint-constraint-flow.md) | TypeScript | Enterprise automation with constraint guarantees |
| [constraint-flow-protocol](./constraint-constraint-flow-protocol.md) | Python | A2A constraint sharing at FLUX bytecode level |
| [constraint-gpu-kernels](./constraint-constraint-gpu-kernels.md) | Cuda | Production CUDA kernels for constraint theory |
| [constraint-hamiltonian](./constraint-constraint-hamiltonian.md) | Rust | Hamiltonian constraint systems |
| [constraint-inference](./constraint-constraint-inference.md) | TypeScript | Reverse-engineers constraints from behavior |
| [constraint-instrument](./constraint-constraint-instrument.md) | Python | Constraint Instrument with 7 modes |
| [constraint-kernel-verify](./constraint-constraint-kernel-verify.md) | Cuda | Exhaustive verification for CUDA kernels |
| [constraint-mcp-server](./constraint-constraint-mcp-server.md) | Python | MCP server for constraint theory |
| [constraint-mux](./constraint-constraint-mux.md) | Rust | Serial port multiplexer with consonance analysis |
| [constraint-physics](./constraint-constraint-physics.md) | Rust | ZHC constraint-based physics engine |
| [constraint-playground](./constraint-constraint-playground.md) | Makefile | CSP solver with GDSII layout |
| [constraint-ranch](./constraint-constraint-ranch.md) | TypeScript | Gamified multi-agent system |
| [constraint-schedule](./constraint-constraint-schedule.md) | Rust | Constraint-satisfaction scheduling |
| [constraint-snap](./constraint-constraint-snap.md) | Python | Geometric constraint snapping |
| [constraint-solver-viz](./constraint-constraint-solver-viz.md) | Python | Visualization tools for constraint solving |
| [constraint-studio](./constraint-constraint-studio.md) | HTML | Studio-quality constraint theory visualization |
| [constraint-substrate](./constraint-constraint-substrate.md) | Python | Constraint primitives in Rust, C, Python |
| [constraint-synth](./constraint-constraint-synth.md) | Python | Constraint-theory synthesizer |
| [constraint-theory-backup](./constraint-constraint-theory-backup.md) | TypeScript | Backup of Constraint Theory workspace |
| [constraint-theory-core](./constraint-constraint-theory-core.md) | Rust | Unified geometric constraint theory core |
| [constraint-theory-core-cuda](./constraint-constraint-theory-core-cuda.md) | Rust | Preserved workspace artifact |
| [constraint-theory-ecosystem](./constraint-constraint-theory-ecosystem.md) | Python | Ecosystem overview and documentation |
| [constraint-theory-engine-cpp-lua](./constraint-constraint-theory-engine-cpp-lua.md) | C++ | C++ constraint engine with LuaJIT |
| [constraint-theory-llvm](./constraint-constraint-theory-llvm.md) | Rust | LLVM backend for constraint theory |
| [constraint-theory-math](./constraint-constraint-theory-math.md) | Python | Sheaf cohomology and GL(9) holonomy |
| [constraint-theory-mlir](./constraint-constraint-theory-mlir.md) | C++ | Custom MLIR dialect for constraint theory |
| [constraint-theory-mojo](./constraint-constraint-theory-mojo.md) | Mojo | Mojo + MLIR constraint engine |
| [constraint-theory-papers](./constraint-constraint-theory-papers.md) | TeX | Research papers on constraint theory |
| [constraint-theory-py](./constraint-constraint-theory-py.md) | Python | Python constraint theory library v0.3.0 |
| [constraint-theory-python](./constraint-constraint-theory-python.md) | Python | Python bindings for constraint-theory-core |
| [constraint-theory-research](./constraint-constraint-theory-research.md) | Python | Mathematical foundations and research |
| [constraint-theory-rust-python](./constraint-constraint-theory-rust-python.md) | Rust | Rust constraint engine with PyO3 |
| [constraint-theory-web](./constraint-constraint-theory-web.md) | JavaScript | WASM demos for constraint theory |
| [constraint-tminus-bridge](./constraint-constraint-tminus-bridge.md) | JavaScript | Cognitive constraint networks |
| [constraint-toolkit](./constraint-constraint-toolkit.md) | Python | Constraint space analysis toolkit |
| [constraint-viz](./constraint-constraint-viz.md) | Python | Multi-scale constraint visualization |

## Category Overview

The constraint theory ecosystem is the mathematical core of SuperInstance. Centers on Eisenstein integer lattices (A2) for exact geometric computation, replacing floating-point arithmetic with lattice snapping for zero-drift determinism.

**Key results:**
- 341B constraints/second on consumer GPU (RTX 4050)
- FP64 is fastest precision on AMD Zen 5 (precision is free)
- Formal proofs via Coq, verified across 60M inputs
- 83 tests in core library, zero dependencies

**Sub-categories:**
- **Core theory:** constraint-theory-core, constraint-theory-math, constraint-theory-py
- **Performance:** constraint-gpu-kernels, constraint-bench-suite, constraint-theory-llvm
- **Compiler:** constraint-dialect, constraint-theory-mlir, constraint-theory-engine-cpp-lua
- **Music:** constraint-audio, constraint-synth, constraint-instrument
- **Distributed:** constraint-crdt, constraint-flow, constraint-flow-protocol
- **Applications:** constraint-physics, constraint-schedule, constraint-ranch
- **Tools:** constraint-mcp-server, constraint-dsl, constraint-toolkit