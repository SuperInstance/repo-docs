# FLUX Bytecode Ecosystem

**166 repos** implementing the FLUX Virtual Machine — a Turing-incomplete bytecode ISA for AI agent coordination, with cross-language runtimes, assemblers, compilers, and GPU-accelerated execution.

---

## What Is FLUX?

FLUX is a custom bytecode virtual machine designed for the SuperInstance ecosystem. It provides a constrained execution environment for AI agents — **Turing-incomplete by design** (guaranteed termination), with a fixed instruction set that can be assembled, compiled, interpreted, and benchmarked across multiple language implementations.

The key design principles:

1. **Turing-incomplete** — all programs are guaranteed to terminate
2. **Cross-language** — the ISA is implemented in Rust, Python, Ruby, C, and more
3. **Constraint-safe** — the bytecode includes constraint checking and boundary validation
4. **Agent-oriented** — opcodes for agent coordination, not just arithmetic
5. **GPU-scalable** — autoscaling execution based on workload demand

---

## The FLUX ISA

The FLUX Instruction Set Architecture (v3.0) defines approximately 42–85 opcodes (the count varies across implementations and versions):

### Opcode Categories

| Category | Example Opcodes | Description |
|----------|----------------|-------------|
| **Arithmetic** | `NOP`, `IAdd`, `ISub`, `IMul`, `IDiv`, `IRem`, `INeg`, `IAbs` | Integer arithmetic |
| **Logical** | `IAnd`, `IOr`, `IXor`, `INot`, `ISHL`, `ISHR` | Bitwise operations |
| **Control Flow** | `Jump`, `BranchIfZero`, `Call`, `Return` | Limited (no unbounded loops) |
| **Memory** | `Load`, `Store`, `Alloc`, `Free` | Stack and heap operations |
| **Agent** | `Send`, `Recv`, `Spawn`, `Sync` | Inter-agent communication |
| **Constraint** | `CheckBound`, `AssertRange`, `Verify` | Safety constraints |

### Performance

From the benchmarks repo (Oracle Cloud ARM64, Ampere Altra, 4 cores, 24GB):

| Runtime | Factorial ns/iter | Speed vs C |
|---------|-------------------|------------|
| Native C | 20 | 1.0× |
| Native Rust | 20 | 1.0× |
| FLUX C VM | 403 | 0.05× |
| Python | 1,885 | 0.01× |
| FLUX Python VM | ~141,000 | 0.0001× |

The FLUX C VM is ~4.7× faster than CPython for tight arithmetic — expected since the C bytecode interpreter avoids Python's overhead.

---

## How the Runtime Works

```
Agent Intent → Assembler → Bytecode → Interpreter → Result
                                       ↓
                               SwarmRouter → A2A Message → Agent Mailbox
                                       ↓
                              CharacterStore (SQLite)
```

1. **Agent expresses intent** — a high-level goal or action
2. **Assembler** converts text assembly to binary bytecode with label resolution
3. **Bytecode** is the compact, portable representation
4. **Interpreter** executes the bytecode (Python, C, Rust, or Ruby runtime)
5. **Side effects** — agent communication, character state updates, constraint checks

### Autoscaling

The FLUX autoscaler evaluates a scaling policy on each tick:

```
avg_utilization = Σ(queue_depth_i / 100) / N

if avg_utilization > 0.8 OR any(backpressure):  → ScaleUp (+1 stream)
if avg_utilization < 0.2 AND all(queue_depth = 0): → ScaleDown (−1 stream)
else: → Hold
```

This allows FLUX execution to dynamically scale GPU streams based on agent workload.

---

## Cross-Language Implementations

One of FLUX's most interesting aspects is the same ISA implemented across many languages:

| Implementation | Language | Status | Key Feature |
|---------------|----------|--------|-------------|
| flux-check / flux-core | Rust | 🟢 Production | Core VM, constraint AST |
| flux-bridge | Python | 🟡 Development | Full pipeline: assembler + interpreter + swarm |
| flux-asm-ruby | Ruby | 🟡 Development | 42-opcode assembler/disassembler/VM |
| flux-chapel | Chapel | 🟡 Development | HPC-oriented |
| flux-cobol | COBOL | 🔴 Experimental | Enterprise retro |
| flux-algol | ALGOL | 🔴 Experimental | Historical computing |
| flux-algebra-c | C | 🟢 Production | Music algebra (Oscar.jl-inspired) |
| flux-algebra-rs | Rust | 🟢 Production | Same music algebra in Rust |

---

## Key Repositories

### Core VM & ISA

| Repo | Description |
|------|-------------|
| [flux-check](https://github.com/SuperInstance/flux-check) | Core constraint checking VM |
| [flux-ast](https://github.com/SuperInstance/flux-ast) | Constraint AST — `ConstraintNode::And`, `BoundNode`, `DeltaNode` with severity levels |
| [flux-asm-ruby](https://github.com/SuperInstance/flux-asm-ruby) | Ruby assembler/disassembler/VM — 42 opcodes, text↔binary |
| [flux-bytecode-diff](https://github.com/SuperInstance/flux-bytecode-diff) | Compare, patch, and migrate FLUX programs across ISA versions |
| [flux-adaptive-opcodes](https://github.com/SuperInstance/flux-adaptive-opcodes) | Adaptive opcode extensions for the base ISA |

### Compilation & Interpretation

| Repo | Description |
|------|-------------|
| [flux-compiler-interpreter](https://github.com/SuperInstance/flux-compiler-interpreter) | Python compiler+interpreter, loads into PLATO shell |
| [flux-compiler-agentic](https://github.com/SuperInstance/flux-compiler-agentic) | Agentic compilation — agents compile their own strategies |
| [flux-bridge](https://github.com/SuperInstance/flux-bridge) | Full Python pipeline: Agent Intent → Assembler → Bytecode → Interpreter |

### Performance & Scaling

| Repo | Description |
|------|-------------|
| [flux-benchmarks](https://github.com/SuperInstance/flux-benchmarks) | Real perf data across 7 runtimes — 4.7× faster than CPython |
| [flux-autoscale](https://github.com/SuperInstance/flux-autoscale) | Workload-based auto-scaling for GPU streams |
| [flux-baton](https://github.com/SuperInstance/flux-baton) | Generational context handoff — the baton IS the brain |
| [flux-baton-test](https://github.com/SuperInstance/flux-baton-test) | Testing framework for baton handoffs |

### Music & Algebra

| Repo | Description |
|------|-------------|
| [flux-algebra](https://github.com/SuperInstance/flux-algebra) | Oscar.jl-inspired music algebra — HarmonicRing, PLRGroup, TropicalHarmony (226 tests) |
| [flux-algebra-c](https://github.com/SuperInstance/flux-algebra-c) | C implementation of the same music algebra |
| [flux-algebra-rs](https://github.com/SuperInstance/flux-algebra-rs) | Rust implementation |

The `flux-algebra` family is the most mathematically substantive part of the FLUX ecosystem. It treats music theory as applied abstract algebra:

- **HarmonicRing**: Z/nZ ring arithmetic for pitch-class theory
- **PLR Group**: Neo-Riemannian Parallel/Leading-tone/Relative transformations
- **Tropical Semiring**: Min-plus algebra for voice-leading optimization
- **Tuning Fields**: Algebraic extensions for equal temperament, just intonation, microtonal systems

### Agent Coordination

| Repo | Description |
|------|-------------|
| [flux-collab](https://github.com/SuperInstance/flux-collab) | Collaborative agent protocols |
| [flux-bottle-protocol](https://github.com/SuperInstance/flux-bottle-protocol) | Async message passing protocol |
| [flux-certify](https://github.com/SuperInstance/flux-certify) | Certification and verification of FLUX programs |

### Tooling

| Repo | Description |
|------|-------------|
| [flux-check-js](https://github.com/SuperInstance/flux-check-js) | JavaScript constraint checker |
| [flux-check-py](https://github.com/SuperInstance/flux-check-py) | Python constraint checker |
| [flux-chronometer](https://github.com/SuperInstance/flux-chronometer) | Timing analysis for FLUX programs |
| [flux-agent-runtime](https://github.com/SuperInstance/flux-agent-runtime) | Runtime environment for FLUX-native agents |

---

## Architecture

```
┌────────────────────────────────────────────────────┐
│              Agent Intent Layer                      │
│   (flux-bridge, flux-compiler-interpreter)           │
└─────────────────────┬──────────────────────────────┘
                      │
┌─────────────────────▼──────────────────────────────┐
│            Compilation Layer                         │
│   (flux-compiler-agentic, flux-ast)                  │
│   Intent → AST → Bytecode                            │
└─────────────────────┬──────────────────────────────┘
                      │
┌─────────────────────▼──────────────────────────────┐
│            Bytecode Layer                            │
│   42-85 opcodes, Turing-incomplete                   │
│   (flux-bytecode-diff for versioning)                │
└─────────────────────┬──────────────────────────────┘
                      │
         ┌────────────┼────────────┐
         │            │            │
┌────────▼───┐ ┌──────▼─────┐ ┌───▼──────────┐
│ Rust VM    │ │ Python VM  │ │ Ruby VM      │
│ (fastest)  │ │ (bridge)   │ │ (asm-ruby)   │
└────────────┘ └────────────┘ └──────────────┘
         │            │            │
┌────────▼────────────▼────────────▼──────────────┐
│            GPU Autoscale Layer                       │
│   (flux-autoscale — scale up on backpressure)       │
└────────────────────────────────────────────────────┘
```

---

## Complete Repo Categories

| Category | ~Count | Representative repos |
|----------|--------|---------------------|
| Core VM / ISA | ~15 | check, ast, asm-ruby, bytecode-diff, adaptive-opcodes |
| Compilation | ~12 | compiler-interpreter, compiler-agentic, bridge |
| Performance | ~10 | benchmarks, autoscale, baton, chronometer |
| Music / Algebra | ~8 | algebra, algebra-c, algebra-rs |
| Agent Coordination | ~15 | collab, bottle-protocol, certify, agent-runtime |
| Language Ports | ~10 | chapel, cobol, algol |
| Constraint / Safety | ~20 | check-js, check-py, constraint AST |
| Hardware / GPU | ~15 | autoscale, PTX integration |
| Interop / Bridging | ~25 | bridge, bottle-protocol, agent coordination |
| Preserved Artifacts | ~6 | historical snapshots |
| Testing / Profiling | ~10 | benchmarks, baton-test |
| Other | ~20 | various |

---

## Assessment

The FLUX ecosystem is a genuinely interesting experiment in constrained computation for AI agents. The Turing-incomplete design choice is smart — it guarantees termination, which is valuable for agent systems where unbounded computation is dangerous. The cross-language implementations demonstrate the ISA's portability.

The music algebra library (`flux-algebra` and ports) is the most mathematically substantive component. The connection between music algebra and a bytecode VM for AI agents is unclear and possibly nonexistent — it reads like a standalone computational musicology library that's been prefixed with "flux-" to fit the ecosystem.

The benchmark numbers are honest and informative. The 4.7× speedup claim over CPython is technically true but misleading — the FLUX C VM is written in C, so it's really "C bytecode interpreter faster than CPython interpreter."

---

*Individual repo summaries are in `flux-{repo-name}.md` files in this directory.*
