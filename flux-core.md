# flux-core

**Category:** ⚙️ Core VM/ISA
**Status:** 🔴 Experimental
**Language:** Rust
**README:** 5,839 bytes

## Intention
FLUX bytecode runtime in Rust — VM, assembler, disassembler, A2A. 13 tests, zero deps.

## How It Works

A register-based VM with 16 general-purpose registers (i32), 16 floating-point registers (f64), PC, SP, and two condition flags (zero, sign). The instruction set spans 0x00–0x81 with single-byte opcodes and 1–4 byte instructions. Categories: arithmetic (IADD, ISUB, IMUL, IDIV, IMOD), logic (IAND, IOR, IXOR, ISHL, ISHR), control flow (JMP, JZ, JNZ, CALL), stack (PUSH, POP, DUP, RET), memory (MOV, MOVI), comparison (CMP), A2A messaging (TELL, ASK, DELEGATE, BROADCAST), and system (HALT, YIELD).

The assembler is two-pass: pass 1 computes instruction sizes and records label positions, pass 2 emits bytecode with jump fixups. O(n) time, O(n) space. Includes cycle budgets for sandboxing (agents can't run forever).

The A2A opcodes are the interesting part — TELL sends a message to another agent, ASK queries, DELEGATE assigns work, BROADCAST sends to all. This makes agent coordination a first-class VM primitive rather than a library call.

## What It's For
The deterministic execution layer for FLUX agents — same bytecode always produces the same result on any node. Designed so agents can share, verify, and audit each other's computation.

## Who Would Use It
Developers building multi-agent systems who want deterministic, auditable computation. The Rust implementation targets those who need performance and memory safety.

## Honest Assessment

**The ISA design is clean and well-thought-out.** Register-based with A2A opcodes as first-class primitives is a genuinely interesting architectural choice — most agent frameworks handle messaging at the library level, not the instruction level.

**However:** Only 13 tests claimed for a VM with ~50 opcodes — that's thin. No CI badge, no benchmarks in the README, no Apache/MIT license mentioned. The README is well-written prose but lacks evidence of rigorous testing (no property-based tests, no fuzzing mentioned, no formal verification). The VM is i32-only for general purpose — no 64-bit support is a limitation.

For a "zero deps" Rust VM, the implementation is plausible but unverified. The claim of O(1) per instruction is standard for interpreters and not remarkable. The cycle budget idea is good but the enforcement mechanism isn't shown.

**Bottom line:** Interesting architecture, probably real code, but needs significantly more test coverage and external verification before being trusted for anything serious.
