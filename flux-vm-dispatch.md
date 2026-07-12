# flux-vm-dispatch

**Category:** ⚙️ Core VM/ISA
**Status:** 🟡 Development
**Language:** Rust
**README:** 4,752 bytes

## Intention
Miniature Flux bytecode VM producing GPU command dispatches. Tests flux-core to cudaclaw synergy.

## How It Works
### Instruction Set

The VM supports a compact instruction set with both binary and ternary operations:

| Instruction | Operands | GPU Dispatch | Semantics |
|-------------|----------|-------------|-----------|
| `MOVI` | reg, imm | — | Load immediate |
| `ADD` | rd, rs1, rs2 | `KernelLaunch("iadd", 256)` | rd = rs1 + rs2 |
| `SUB` | rd, rs1, rs2 | `KernelLaunch("isub", 256)` | rd = rs1 − rs2 |
| `TADD` | rd, ra, rb | `KernelLaunch("ternary_add", 256)` | Z₃ addition |
| `TMUL` | rd, ra, rb | `K...

## What It's For
Miniature Flux bytecode VM producing GPU command dispatches. Tests flux-core to cudaclaw synergy.

## Who Would Use It
Systems engineers and HPC developers targeting specific hardware (NVIDIA GPUs, FPGAs, AVX-512 CPUs).

## Honest Assessment
Has code examples. missing: tests, benchmarks.
