# FLUX Category Index — Bytecode VMs, Assemblers, Compilers for Agentic Logic

**Total repos:** 165
**Generated:** 2026-07-12

This index covers the `flux-` prefixed repos from the SuperInstance organization. These are the core of the FLUX ecosystem: bytecode virtual machines, assemblers, compilers, constraint engines, agent runtimes, and related tooling.

## Ecosystem Overview

The FLUX ecosystem is a large collection of repos centered on a **bytecode VM for AI agents**. The core idea: instead of agents reasoning in natural language or Python, they compile intent into deterministic bytecode that runs on a register-based VM. This enables verifiable, auditable, sandboxed agent execution.

The ecosystem spans:
- **Core VMs** in Python, Rust, C, Zig, JavaScript, Go, Java, PHP, TypeScript
- **Constraint engines** for safety-critical checking (fracture/coalesce algorithms)
- **Agent coordination** via A2A (Agent-to-Agent) signaling protocol
- **Natural language programming** across 80+ human languages
- **Hardware acceleration** (CUDA, AVX-512, FPGA, WebGPU, eBPF)
- **Music/math theory** (harmonic rings, PLR groups, tropical semirings)
- **Legacy language ports** (COBOL, Fortran, ALGOL, MUMPS, SNOBOL, PL/I, RPG IV)

## Honest Overall Assessment

This is an **enormous, sprawling ecosystem** (165 repos) that appears to be largely generated or maintained by AI agents themselves (many repos are described as "self-bootstrapped" agent vessels). The core VM implementations (flux-core in Rust, flux-py, flux-js, flux-zig) appear genuine with real code and benchmarks. The constraint checking math is mathematically sound in concept. However:

- **Many repos are stubs or placeholders** (29 repos have <500 bytes of README)
- **Test claims are extremely high** (e.g., "2037 tests", "840 tests") but these are self-reported and unverified
- **Performance claims** ("4.7x faster than CPython", "70.1B checks/s") need independent verification
- **The "self-bootstrapping agent" pattern** means many repos are AI-generated artifacts, not human-written code
- **The scope is arguably too broad** — 165 repos covering VMs, constraint engines, music theory, legacy languages, and natural language programming is extremely ambitious
- **Core technical ideas are interesting**: deterministic bytecode for agents, constraint-based safety checking, and multilingual compilation are novel approaches

## Status Summary

| Status | Count |
|--------|-------|
| 🟢 Production-oriented | 32 |
| 🟡 Development | 89 |
| 🔴 Experimental | 26 |
| ⚰️ Archived | 4 |
| 🗄️ Preserved Artifact | 10 |
| ❓ No Documentation | 4 |

## Repos by Category

### ⚙️ Core VM/ISA (19 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-runtime](flux-runtime.md) | ⚡ Deterministic bytecode ISA runtime for agentic logic — assembler, compiler, VM | Python | 🟢 Production-oriented | 9,336b |
| [flux-vm](flux-vm.md) | FLUX-C constraint VM: 50 opcodes, stack-based, DAL A certifiable. TrustZone-styl | Rust | 🟢 Production-oriented | 7,773b |
| [flux-vm-classic](flux-vm-classic.md) | Extracted from forgemaster/flux-vm — Cocapn fleet component | Rust | 🟢 Production-oriented | 7,773b |
| [flux-runtime-wasm](flux-runtime-wasm.md) | FLUX VM WebAssembly target — browser-based agent bytecode execution with ISA v3  | TypeScript | 🟢 Production-oriented | 6,514b |
| [flux-isa](flux-isa.md) | FLUX ISA v2.0 — Complete 256-opcode instruction set reference with Python encode | Python | 🟡 Development | 6,439b |
| [flux-vm-php](flux-vm-php.md) | Pure PHP FLUX ISA v3.0 virtual machine — register-based bytecode VM for multi-ag | PHP | 🔴 Experimental | 5,917b |
| [flux-core](flux-core.md) | FLUX bytecode runtime in Rust — VM, assembler, disassembler, A2A. 13 tests, zero | Rust | 🔴 Experimental | 5,839b |
| [flux-vm-dispatch](flux-vm-dispatch.md) | Miniature Flux bytecode VM producing GPU command dispatches. Tests flux-core to  | Rust | 🟡 Development | 4,752b |
| [flux-vm-v3](flux-vm-v3.md) | FLUX-C v3 VM — proof-carrying, SIMD-native, terminating constraint VM | Rust | 🟢 Production-oriented | 4,734b |
| [flux-coop-runtime](flux-coop-runtime.md) | The missing middle layer — cooperative execution runtime bridging FLUX VM coordi | Python | 🟡 Development | 3,348b |
| [flux-decompiler](flux-decompiler.md) | FLUX bytecode decompiler — bytecode to assembly with labels and control flow | Python | 🟡 Development | 2,844b |
| [flux-cross-assembler](flux-cross-assembler.md) | Dual-target FLUX assembler — cloud (4-byte fixed) and edge (variable-width) byte | Python | 🟢 Production-oriented | 2,396b |
| [flux-asm-ruby](flux-asm-ruby.md) | FLUX ISA assembler/disassembler in pure Ruby — 42-opcode Turing-incomplete VM | Ruby | 🟡 Development | 2,262b |
| [flux-isa-authority](flux-isa-authority.md) | ISA governance layer — opcode conflict arbitration, version negotiation, canonic | Python | 🔴 Experimental | 1,971b |
| [flux-wasm](flux-wasm.md) | FLUX WASM — WebAssembly bytecode VM in Rust. Run FLUX in any browser. | Makefile | 🟡 Development | 1,321b |
| [flux-vm-ts](flux-vm-ts.md) | FLUX Virtual Machine in TypeScript — bytecode execution for Node.js and browsers | TypeScript | 🔴 Experimental | 536b |
| [flux-bytecode-diff](flux-bytecode-diff.md) | Bytecode diff and migration tools — compare, patch, and migrate FLUX programs ac | Python | 🔴 Experimental | 312b |
| [flux-wasm-gen](flux-wasm-gen.md) | FLUX to WebAssembly compiler — bytecode to WAT format | Python | 🟡 Development | 88b |
| [flux-vm-agent](flux-vm-agent.md) | FLUX VM Agent — standalone bytecode VM, assembler, NLP interpreter | Python | ❓ No Documentation | 0b |

### ⚡ Hardware/GPU (6 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-hardware](flux-hardware.md) | FLUX hardware backends: CUDA, AVX-512, Fortran, FPGA, eBPF, WebGPU, Vulkan, Coq. | C | 🟢 Production-oriented | 11,476b |
| [flux-autoscale](flux-autoscale.md) | Auto-scaling Flux bytecode execution based on workload demand. Scales up on back | Rust | 🟡 Development | 4,556b |
| [flux-gpu](flux-gpu.md) | CUDA micro-experiments for constraint engine — 24.9B checks/sec on RTX 4050. Sed | Cuda | 🟡 Development | 3,750b |
| [flux-lcar-esp32](flux-lcar-esp32.md) | ESP32 hardware adapter for LCAR cartridge execution on FLUX fleet edge devices | C | 🟡 Development | 3,321b |
| [flux-cuda](flux-cuda.md) | FLUX CUDA — GPU-accelerated bytecode VM. 1000 parallel agents on NVIDIA GPUs. | Cuda | 🔴 Experimental | 1,424b |
| [flux-vm-gpu](flux-vm-gpu.md) | GPU-batch FLUX constraint VM — evaluate thousands of constraint programs in para | Rust | 🟢 Production-oriented | 1,228b |

### ✅ Constraint/Safety (11 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-check-js](flux-check-js.md) | Exact constraint checking, fracture-coalesce, and sediment layers. Zero-dep Type | TypeScript | 🟢 Production-oriented | 9,862b |
| [flux-fracture](flux-fracture.md) | Disjoint linear algebra for constraint systems — BFS fracture + bitwise OR coale | Rust | 🟡 Development | 8,080b |
| [flux-engine-c](flux-engine-c.md) | Single-header C constraint engine — #define FLUX_ENGINE_IMPLEMENTATION. Check, f | C | 🟢 Production-oriented | 7,022b |
| [flux-lucid](flux-lucid.md) | Unified constraint theory ecosystem — CDCL, LLVM, AVX-512, GL(9) consensus, 9-ch | Rust | 🟡 Development | 5,350b |
| [flux-check-py](flux-check-py.md) | Python CLI for exact constraint checking — 6 industry presets, 74 tests, thermod | Python | 🟢 Production-oriented | 4,957b |
| [flux-fracture-c](flux-fracture-c.md) | Single-header C99 fracture-coalesce library — #define FRACTURE_IMPLEMENTATION. | C | 🟢 Production-oriented | 4,702b |
| [flux-conformance](flux-conformance.md) | FLUX Ecosystem - flux-conformance | Python | 🟢 Production-oriented | 3,947b |
| [flux-reasoner-engine](flux-reasoner-engine.md) | Dual-interpreter gradient reasoning engine | Python | 🟡 Development | 3,471b |
| [flux-ast](flux-ast.md) | FLUX constraint safety - flux-ast | Rust | 🟢 Production-oriented | 2,065b |
| [flux-constraint-ruby](flux-constraint-ruby.md) | FLUX constraint engine for Ruby — exact arithmetic and constraint resolution | Ruby | 🟡 Development | 1,637b |
| [flux-verify-api](flux-verify-api.md) | FLUX constraint safety - flux-verify-api | Rust | 🔴 Experimental | 654b |

### 🌍 Natural Language Runtime (6 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-runtime-san](flux-runtime-san.md) | FLUX bytecode execution runtime with Sanskrit language processing support | Python | 🟡 Development | 5,968b |
| [flux-runtime-deu](flux-runtime-deu.md) | FLUX bytecode execution runtime with German language processing support | Python | 🔴 Experimental | 5,411b |
| [flux-runtime-lat](flux-runtime-lat.md) | FLUX bytecode execution runtime with Latin language processing support | Python | 🟡 Development | 3,925b |
| [flux-runtime-wen](flux-runtime-wen.md) | FLUX bytecode execution runtime with Wendish/Sorbian language processing support | Python | 🟡 Development | 3,557b |
| [flux-runtime-kor](flux-runtime-kor.md) | FLUX bytecode execution runtime with Korean language processing support | Python | 🔴 Experimental | 3,451b |
| [flux-runtime-zho](flux-runtime-zho.md) | FLUX bytecode execution runtime with Chinese language processing support | Python | 🔴 Experimental | 2,732b |

### 🎵 Math/Music/Algebra (12 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-algebra](flux-algebra.md) | Oscar.jl-inspired music algebra — HarmonicRing, PLRGroup, TropicalHarmony, Tunin | Python | 🟡 Development | 7,858b |
| [flux-algebra-c](flux-algebra-c.md) | C port of flux-algebra — PLR group, tuning fields, voice leading | C | 🟢 Production-oriented | 6,629b |
| [flux-genome-py](flux-genome-py.md) | Genetic expression engine — 25 genes, 5 domains, genome FIXED, expression ADAPTI | Python | 🟡 Development | 6,062b |
| [flux-genome](flux-genome.md) | 25-gene musical genome, genetic evolution of traditions. 27 tests. | Python | 🟢 Production-oriented | 5,817b |
| [flux-hyperbolic-py](flux-hyperbolic-py.md) | Poincaré ball geometry for model capability routing. Frechet mean, task routing, | Python | 🟡 Development | 5,655b |
| [flux-hyperbolic](flux-hyperbolic.md) | Poincaré ball embeddings for music tradition hierarchy. Riemannian optimization, | Python | 🔴 Experimental | 5,641b |
| [flux-algebra-rs](flux-algebra-rs.md) | Musical algebra — PLR group, tropical semiring, tuning fields, voice leading | Rust | 🟡 Development | 5,638b |
| [flux-tensor-midi](flux-tensor-midi.md) | 🎵 4-dimensional tensor representation of MIDI events — 6 languages (Python, Rust | Python | 🟡 Development | 4,928b |
| [flux-hdc](flux-hdc.md) | FLUX HDC: Hyperdimensional Computing for semantic constraint matching. 1024-bit  | Python | 🟢 Production-oriented | 4,612b |
| [flux-genome-rs](flux-genome-rs.md) | Genetic algorithm engine for evolving musical structures and harmonic patterns | Rust | 🔴 Experimental | 2,934b |
| [flux-negative-space](flux-negative-space.md) | FLUX negative-space learning — discovering structure from what's absent in spect | Python | 🟡 Development | 2,537b |
| [flux-hyperbolic-rs](flux-hyperbolic-rs.md) | Hyperbolic geometry embeddings using Poincaré ball and Lorentz models | Rust | 🔴 Experimental | 1,138b |

### 🏛️ Legacy/Niche Language Port (9 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-rpg](flux-rpg.md) | RPG IV constraint engine — indicator variables as error mask bits. IBM i / AS-40 | RPGLE | 🟡 Development | 6,356b |
| [flux-mumps](flux-mumps.md) | MUMPS constraint engine — global hierarchical storage for sediment layers. The T | M | 🟡 Development | 6,209b |
| [flux-pli](flux-pli.md) | PL/I constraint engine — native BIT(8) error mask, BOOL coalescence, DEC FIXED e | — | 🟡 Development | 6,078b |
| [flux-cobol](flux-cobol.md) | Full COBOL constraint engine — FLXCHECK, FLXFRACT, FLXSEDIMNT with copybooks. BF | COBOL | 🟡 Development | 5,780b |
| [flux-algol](flux-algol.md) | ALGOL 60 constraint engine — own keyword for persistent sediment, parallel array | ALGOL | 🟡 Development | 5,668b |
| [flux-snobol](flux-snobol.md) | SNOBOL4 constraint engine — pattern match success/failure as constraint pass/fai | — | 🟡 Development | 5,378b |
| [flux-julia](flux-julia.md) | Julia spike — multiple dispatch on 10 tradition types, @conserved macro, distrib | Julia | 🟡 Development | 4,659b |
| [flux-fortran](flux-fortran.md) | Constraint engine fracture-coalesce and sediment layers in Fortran 2008. Column- | Fortran | 🟢 Production-oriented | 3,414b |
| [flux-chapel](flux-chapel.md) | Chapel constraint engine with GPU locale model. Multi-GPU coforall, distributed  | Chapel | 🟡 Development | 3,052b |

### 📊 Testing/Profiling (10 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-debugger](flux-debugger.md) | FLUX step debugger with breakpoints, reverse stepping, and state inspection | Python | 🟡 Development | 3,176b |
| [flux-signatures](flux-signatures.md) | FLUX bytecode pattern recognition — detect loops, counters, accumulators, swaps | Python | 🟡 Development | 2,924b |
| [flux-profiler](flux-profiler.md) | FLUX performance profiler — opcode counts, hot paths, register usage, cycle esti | Python | 🟡 Development | 2,898b |
| [flux-coverage](flux-coverage.md) | FLUX coverage analyzer — instruction, branch, path, and register coverage | Python | 🟡 Development | 2,869b |
| [flux-testkit](flux-testkit.md) | FLUX test harness framework — assertion helpers, suites, reports | Python | 🟢 Production-oriented | 829b |
| [flux-benchmarks](flux-benchmarks.md) | FLUX Benchmarks — Real performance data across 7 runtimes. 4.7x faster than CPyt | Shell | 🟡 Development | 784b |
| [flux-fuzzer](flux-fuzzer.md) | FLUX bytecode fuzzer — random generation + edge case detection | Python | 🟢 Production-oriented | 676b |
| [flux-validator](flux-validator.md) | FLUX cross-VM validator — run bytecodes across 8 language implementations | Python | 🟡 Development | 568b |
| [flux-metrics](flux-metrics.md) | FLUX runtime metrics — instruction-level profiling and performance analysis | Python | 🟡 Development | 509b |
| [flux-integration-tests](flux-integration-tests.md) | Cross-language parity tests — Python, C, Rust, JS all produce identical results. | Python | ❓ No Documentation | 0b |

### 📚 Docs/Research (8 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-spec](flux-spec.md) | FLUX Ecosystem - flux-spec | — | 🟢 Production-oriented | 8,900b |
| [flux-papers](flux-papers.md) | FLUX research papers, specifications, and benchmarks. EMSOFT submission, Safe-TO | Python | 🟢 Production-oriented | 4,922b |
| [flux-evolution](flux-evolution.md) | Timeline visualization and analysis of the FLUX ecosystem evolution — tracking s | Python | 🟢 Production-oriented | 4,322b |
| [flux-timeline](flux-timeline.md) | Temporal sequencing engine for FLUX fleet bytecode scheduling and event ordering | Python | 🟡 Development | 2,619b |
| [flux-research](flux-research.md) | FLUX Deep Research — Compiler/interpreter taxonomy, agent-first design, ISA v2 p | Python | 🟡 Development | 1,671b |
| [flux-rfc](flux-rfc.md) | Structured disagreement resolution protocol for the FLUX fleet — IETF-inspired R | Python | 🟢 Production-oriented | 1,652b |
| [flux-site](flux-site.md) | FLUX community site: playground, benchmarks, timeline, PHP kit. Deploy at cocapn | HTML | 🟡 Development | 1,111b |
| [flux-docs](flux-docs.md) | FLUX documentation: tutorials, cookbooks, runbooks, strategy. Apache 2.0. | — | 🟡 Development | 640b |

### 📦 Stdlib/Knowledge (8 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-vocabulary](flux-vocabulary.md) | FLUX Ecosystem - flux-vocabulary | Python | 🟡 Development | 6,399b |
| [flux-skills](flux-skills.md) | ⚡ FLUX-native agent skills — clone, run, modify, compose. A2A-first docs so agen | Python | 🔴 Experimental | 4,244b |
| [flux-flow-state](flux-flow-state.md) | FLUX flow-state engine — constraint-aware execution environment maintaining cons | Python | 🟡 Development | 2,448b |
| [flux-envelope](flux-envelope.md) | FLUX Viewpoint Envelope — Cross-linguistic coherence, Lingua Franca bytecode, un | Python | 🟢 Production-oriented | 1,312b |
| [flux-stdlib](flux-stdlib.md) | FLUX standard library — 13 pre-compiled bytecode programs (math, utility) | Python | 🟢 Production-oriented | 1,079b |
| [flux-knowledge-federation](flux-knowledge-federation.md) | Federated knowledge layer for cross-agent learning — query and contribute to sha | Python | 🔴 Experimental | 1,042b |
| [flux-plato-bridge](flux-plato-bridge.md) | Connect FLUX bytecode execution to PLATO knowledge tiles — bidirectional bridge  | Python | 🔴 Experimental | 327b |
| [flux-skill-dsl](flux-skill-dsl.md) | Skill Definition Language — formal type-safe skill definitions, composition, dep | Python | 🔴 Experimental | 138b |

### 🔄 Archived (3 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-consciousness-engine-early-version](flux-consciousness-engine-early-version.md) | [ARCHIVED] Early self-perceiving engine. Temporal intelligence now in SuperInsta | — | ⚰️ Archived | 1,120b |
| [flux-engine-early-version](flux-engine-early-version.md) | [ARCHIVED] Early flux consciousness engine. Temporal intelligence now in SuperIn | Python | ⚰️ Archived | 1,100b |
| [flux-constraint-py-early-version](flux-constraint-py-early-version.md) | [ARCHIVED] Empty Python bindings placeholder. | Python | ⚰️ Archived | 517b |

### 🔐 Security/Provenance (3 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-certify](flux-certify.md) | *(no description)* | Python | 🟡 Development | 5,351b |
| [flux-provenance](flux-provenance.md) | Provenance and attribution layer — cryptographic bytecode signing, author tracki | Python | 🔴 Experimental | 118b |
| [flux-crypto](flux-crypto.md) | FLUX crypto — signing, commitments, Merkle trees for agent communication | Python | 🟡 Development | 106b |

### 🔗 Interop/Bridging (5 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-importer](flux-importer.md) | Flux bytecode → synthetic MIR bridge for cuda-oxide. Translates agent-native Flu | Rust | 🟡 Development | 8,030b |
| [flux-ffi](flux-ffi.md) | Cross-language FFI bindings for Flux constraint math primitives. | Rust | 🟡 Development | 5,247b |
| [flux-bridge](flux-bridge.md) | FLUX constraint safety - flux-bridge | Python | 🟡 Development | 4,194b |
| [flux-diff](flux-diff.md) | FLUX bytecode diff tool — compare programs, show structural changes | Python | 🟡 Development | 513b |
| [flux-packager](flux-packager.md) | Dependency management and packaging tool for FLUX fleet bytecode cartridges | Python | 🟡 Development | 107b |

### 🔧 Toolchain (12 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-compiler](flux-compiler.md) | The first certifiable constraint compiler — GUARD DSL → verified machine code | Python | 🟢 Production-oriented | 8,261b |
| [flux-lsp](flux-lsp.md) | FLUX Ecosystem - flux-lsp | TypeScript | 🟡 Development | 6,769b |
| [flux-compiler-agentic](flux-compiler-agentic.md) | 6-plane abstraction compiler with dual-interpreter gradient gates | Python | 🟡 Development | 5,438b |
| [flux-ide](flux-ide.md) | FLUX Language IDE — markdown-to-bytecode agent-native development environment | TypeScript | 🟢 Production-oriented | 3,692b |
| [flux-compiler-workspace](flux-compiler-workspace.md) | FLUX compiler development workspace — constraint language toolchain | Python | 🟢 Production-oriented | 2,882b |
| [flux-studio](flux-studio.md) | *(no description)* | JavaScript | 🔴 Experimental | 2,062b |
| [flux-grammar](flux-grammar.md) | Formal FLUX assembly language grammar — lexer, parser, validator | Python | 🟡 Development | 1,001b |
| [flux-linker](flux-linker.md) | FLUX multi-module bytecode linker — symbol resolution, relocation, library linki | Python | 🟡 Development | 956b |
| [flux-optimizer](flux-optimizer.md) | FLUX peephole bytecode optimizer — constant folding, dead code elimination, stre | Python | 🟡 Development | 834b |
| [flux-repl](flux-repl.md) | Interactive FLUX bytecode playground — assemble, execute, debug | Python | 🟡 Development | 799b |
| [flux-compiler-interpreter](flux-compiler-interpreter.md) | flux-compiler-interpreter | Python | 🟡 Development | 634b |
| [flux-ir](flux-ir.md) | FLUX intermediate representation — structured IR between source and bytecode | Python | 🟡 Development | 105b |

### 🗄️ Preserved Artifact (10 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-isa-edge](flux-isa-edge.md) | Preserved workspace artifact | Makefile | 🗄️ Preserved Artifact | 4,633b |
| [flux-isa-std](flux-isa-std.md) | Preserved workspace artifact | Makefile | 🗄️ Preserved Artifact | 3,138b |
| [flux-isa-c](flux-isa-c.md) | Preserved workspace artifact | C | 🗄️ Preserved Artifact | 2,976b |
| [flux-isa-mini](flux-isa-mini.md) | Preserved workspace artifact | Makefile | 🗄️ Preserved Artifact | 2,808b |
| [flux-check](flux-check.md) | Preserved workspace artifact | — | 🗄️ Preserved Artifact | 0b |
| [flux-contracts](flux-contracts.md) | Preserved workspace artifact | Makefile | 🗄️ Preserved Artifact | 0b |
| [flux-deploy](flux-deploy.md) | Preserved workspace artifact | Python | 🗄️ Preserved Artifact | 0b |
| [flux-esp32](flux-esp32.md) | Preserved workspace artifact | C | 🗄️ Preserved Artifact | 0b |
| [flux-isa-thor](flux-isa-thor.md) | Preserved workspace artifact | — | 🗄️ Preserved Artifact | 0b |
| [flux-sdk-python](flux-sdk-python.md) | Preserved workspace artifact | Python | 🗄️ Preserved Artifact | 0b |

### 🤖 Auto-Generated Agent (4 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-9969b6](flux-9969b6.md) | FLUX-native I2I agent (self-bootstrapped) | — | 🟡 Development | 3,954b |
| [flux-agent-runtime](flux-agent-runtime.md) | FLUX-native agent runtime — self-bootstrapping agents in Docker sandboxes that c | Python | 🔴 Experimental | 3,004b |
| [flux-agent-a0fa81](flux-agent-a0fa81.md) | flux-agent-a0fa81 vessel — FLUX-native agent — self-bootstrapped | — | 🟡 Development | 302b |
| [flux-0c476c](flux-0c476c.md) | FLUX-native I2I agent (self-bootstrapped) | — | 🔴 Experimental | 146b |

### 🤝 Agent Coordination (14 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-mesh](flux-mesh.md) | Universal distributed system mesh — FLUX adapts between any language, any transp | Python | 🟡 Development | 9,513b |
| [flux-a2a-signal](flux-a2a-signal.md) | FLUX A2A Signal Protocol — agent-first-class JSON language with multilingual com | Python | 🟢 Production-oriented | 8,561b |
| [flux-discussion-flows](flux-discussion-flows.md) | Three-tier adversarial debate system for AI models | Python | 🟡 Development | 8,112b |
| [flux-cooperative-intelligence](flux-cooperative-intelligence.md) | Novel multi-agent cooperative problem-solving protocol — collective intelligence | Python | 🟡 Development | 6,701b |
| [flux-fleet-stdlib](flux-fleet-stdlib.md) | Shared error codes, status types, and common utilities for the entire FLUX fleet | Python | 🟡 Development | 5,014b |
| [flux-roundtable](flux-roundtable.md) | Multi-agent role-play roundtable and reverse-ideation system | Python | 🟡 Development | 4,417b |
| [flux-meta-orchestrator](flux-meta-orchestrator.md) | Fleet-wide orchestration — reads ecosystem state, identifies gaps, assigns work, | Python | 🟡 Development | 3,969b |
| [flux-bottle-protocol](flux-bottle-protocol.md) | Formal specification for the fleet bottle communication protocol — schema, valid | Python | ⚰️ Archived | 3,714b |
| [flux-collab](flux-collab.md) | A2A-first agent cooperation framework — multi-agent, git-native, coordination-fr | Python | 🟡 Development | 1,283b |
| [flux-fleet-scanner](flux-fleet-scanner.md) | FLUX fleet health scanner — repo discovery, health classification, gap detection | Python | 🟡 Development | 1,241b |
| [flux-a2a-prototype](flux-a2a-prototype.md) | FLUX A2A Signal Protocol — Agent-first-class JSON language with branching, forki | Python | 🟡 Development | 884b |
| [flux-baton](flux-baton.md) | Generational context handoff for FLUX-native agents — the baton IS the brain | Python | 🟡 Development | 796b |
| [flux-swarm](flux-swarm.md) | FLUX Swarm — Go implementation with distributed agent coordination and A2A messa | Go | 🟡 Development | 407b |
| [flux-baton-test](flux-baton-test.md) | Baton lifecycle test vessel | — | 🟡 Development | 315b |

### 🧩 Other (25 repos)

| Repo | Description | Lang | Status | README |
|------|-------------|------|--------|--------|
| [flux-multilingual](flux-multilingual.md) | Babel Lattice — 80+ language natural language programming runtimes for FLUX byte | Python | 🟡 Development | 9,638b |
| [flux-index](flux-index.md) | Semantic code search, zero dependencies. Spring-load any repo into a searchable  | Python | 🟡 Development | 8,787b |
| [flux-lib-py](flux-lib-py.md) | Unified constraint engine library — from flux_lib import ConstraintEngine. 83 te | Python | 🟡 Development | 7,465b |
| [flux-tui](flux-tui.md) | FLUX VM Debugger & Conformance Dashboard — Go + bubbletea | Go | 🟢 Production-oriented | 6,981b |
| [flux-llama](flux-llama.md) | FLUX × llama.cpp — Multi-agent bytecode-driven LLM token sampling with swarm vot | C | 🟡 Development | 3,634b |
| [flux-reasoner](flux-reasoner.md) | Dual-interpreter gradient reasoning engine | Python | 🟡 Development | 3,471b |
| [flux-simulator](flux-simulator.md) | FLUX fleet simulation environment for testing bytecode programs in isolation | Python | 🟡 Development | 3,168b |
| [flux-js](flux-js.md) | FLUX.js — JavaScript bytecode VM with A2A agent messaging. 373ns/iter via V8 JIT | JavaScript | 🟡 Development | 3,054b |
| [flux-py](flux-py.md) | FLUX Python — Minimal clean-room VM. Swarm coordination with A2A. | Python | 🟡 Development | 2,994b |
| [flux-lang](flux-lang.md) | FLUX: A constraint-native language where the constraint IS the computation | Python | 🟡 Development | 2,919b |
| [flux-index-rs](flux-index-rs.md) | Inverted index for text search — TF-IDF scoring, cosine similarity, prefix queri | Rust | 🟢 Production-oriented | 2,795b |
| [flux-realm](flux-realm.md) | Flux-Realm: A2A autonomous agent orchestration framework with SAEP veto topology | Makefile | 🔴 Experimental | 1,641b |
| [flux-sandbox](flux-sandbox.md) | Safe simulation environment for testing cooperative FLUX programs — mock agents, | Python | 🟡 Development | 1,042b |
| [flux-os](flux-os.md) | 🐧 Pure C agent-first OS — kernel-up autonomous computing. | C | 🟡 Development | 1,026b |
| [flux-zig](flux-zig.md) | FLUX Zig — FASTEST VM at 210ns/iter. Comptime-optimized bytecode interpreter. | Zig | 🟡 Development | 916b |
| [flux-opcodes](flux-opcodes.md) | Flux Opcodes | Python | 🟡 Development | 681b |
| [flux-java](flux-java.md) | FLUX JVM — Java bytecode VM with two-pass assembler. Pure Java, no dependencies. | Java | 🟡 Development | 407b |
| [flux-evolve-py](flux-evolve-py.md) | Python evolution engine for FLUX VM — deterministic self-modification with elite | Python | 🔴 Experimental | 352b |
| [flux-adaptive-opcodes](flux-adaptive-opcodes.md) | Adaptive opcode discovery — runtime ISA extension, proposal, testing, and democr | Python | 🔴 Experimental | 326b |
| [flux-chronometer](flux-chronometer.md) | Cocapn vessel vessel — testing and conformance | — | 🟡 Development | 311b |
| [flux-visualizer](flux-visualizer.md) | Visualization tools for FLUX fleet bytecode execution traces and system topology | Python | 🟡 Development | 95b |
| [flux-lcar-cartridge](flux-lcar-cartridge.md) | LCAR cartridge specification and loader for FLUX fleet modular execution units | Python | 🔴 Experimental | 21b |
| [flux-lcar-scheduler](flux-lcar-scheduler.md) | LCAR cartridge scheduler for FLUX fleet workload distribution and orchestration | Python | 🔴 Experimental | 21b |
| [](flux-.md) | *(no description)* | — | ❓ No Documentation | 0b |
| [flux-via-keeper](flux-via-keeper.md) | FLUX-native I2I agent via keeper | — | ❓ No Documentation | 0b |

## Most Documented Repos

| Repo | Description | README Size |
|------|-------------|-------------|
| [flux-hardware](flux-hardware.md) | FLUX hardware backends: CUDA, AVX-512, Fortran, FPGA, eBPF,  | 11,476b |
| [flux-check-js](flux-check-js.md) | Exact constraint checking, fracture-coalesce, and sediment l | 9,862b |
| [flux-multilingual](flux-multilingual.md) | Babel Lattice — 80+ language natural language programming ru | 9,638b |
| [flux-mesh](flux-mesh.md) | Universal distributed system mesh — FLUX adapts between any  | 9,513b |
| [flux-runtime](flux-runtime.md) | ⚡ Deterministic bytecode ISA runtime for agentic logic — ass | 9,336b |
| [flux-spec](flux-spec.md) | FLUX Ecosystem - flux-spec | 8,900b |
| [flux-index](flux-index.md) | Semantic code search, zero dependencies. Spring-load any rep | 8,787b |
| [flux-a2a-signal](flux-a2a-signal.md) | FLUX A2A Signal Protocol — agent-first-class JSON language w | 8,561b |
| [flux-compiler](flux-compiler.md) | The first certifiable constraint compiler — GUARD DSL → veri | 8,261b |
| [flux-discussion-flows](flux-discussion-flows.md) | Three-tier adversarial debate system for AI models | 8,112b |
| [flux-fracture](flux-fracture.md) | Disjoint linear algebra for constraint systems — BFS fractur | 8,080b |
| [flux-importer](flux-importer.md) | Flux bytecode → synthetic MIR bridge for cuda-oxide. Transla | 8,030b |
| [flux-algebra](flux-algebra.md) | Oscar.jl-inspired music algebra — HarmonicRing, PLRGroup, Tr | 7,858b |
| [flux-vm](flux-vm.md) | FLUX-C constraint VM: 50 opcodes, stack-based, DAL A certifi | 7,773b |
| [flux-vm-classic](flux-vm-classic.md) | Extracted from forgemaster/flux-vm — Cocapn fleet component | 7,773b |
| [flux-lib-py](flux-lib-py.md) | Unified constraint engine library — from flux_lib import Con | 7,465b |
| [flux-engine-c](flux-engine-c.md) | Single-header C constraint engine — #define FLUX_ENGINE_IMPL | 7,022b |
| [flux-tui](flux-tui.md) | FLUX VM Debugger & Conformance Dashboard — Go + bubbletea | 6,981b |
| [flux-lsp](flux-lsp.md) | FLUX Ecosystem - flux-lsp | 6,769b |
| [flux-cooperative-intelligence](flux-cooperative-intelligence.md) | Novel multi-agent cooperative problem-solving protocol — col | 6,701b |

## Key Observations

1. **flux-core (Rust)** is likely the real centerpiece — a compact register VM with 0x00-0x81 opcodes, two-pass assembler, A2A messaging, and zero dependencies. The ISA is clean and well-documented.

2. **flux-runtime (Python)** is the flagship implementation with the most features — markdown-to-bytecode compilation, "FLUX-ese" intermediate language, 2037 claimed tests, and pip install support.

3. **flux-zig** claims fastest execution at 210ns/iter, beating both JS (373ns) and C (403ns) — plausible given Zig's comptime optimization, but only for a factorial benchmark.

4. **flux-compiler** is notably honest — it explicitly states "This is not a production tool" and acknowledges that coverage claims "have not been independently verified." Refreshing candor.

5. **The music/math repos** (flux-algebra, flux-genome, flux-hyperbolic) are mathematically interesting — treating Z/12Z ring ideals as musical objects is legitimate mathematics. But their connection to a bytecode VM for agents is unclear.

6. **The legacy language ports** (COBOL, Fortran, ALGOL, MUMPS, SNOBOL, PL/I, RPG IV) are creative exercises but likely novelty/proof-of-concept rather than practical tools.

7. **The multilingual runtimes** (Chinese, German, Korean, Sanskrit, Latin, Classical Chinese) are intellectually fascinating but extremely ambitious — compiling natural language grammar features into bytecode type systems is a research project, not a production framework.

8. **Agent-generated repos** (flux-0c476c, flux-9969b6, flux-agent-a0fa81, etc.) are AI agents that bootstrapped themselves in Docker containers — they contain metadata, status files, and health checks, but represent fleet topology rather than usable software.
