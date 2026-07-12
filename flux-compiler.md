# flux-compiler

**Category:** 🔧 Toolchain
**Status:** 🟢 Production-oriented
**Language:** Python
**README:** 9,103 bytes

## Intention
The first certifiable constraint compiler — GUARD DSL → verified machine code.

## How It Works

FLUX Compiler is a research compiler exploring formal methods for safety-critical code generation. It uses a system prober to detect available compilers/libraries (gcc, clang, zig, nim, fortran, etc.), a benchmark engine to measure performance, and a JIT compiler that compiles optimized kernels from source strings in 4 languages at startup.

The compiler takes GUARD DSL input and produces verified machine code. It features 5 base primitives (norm, check, bloom, fold, snap) with 20 total implementations across compiled + interpreted backends. It adapts by selecting the best-performing implementation per primitive per machine.

## What It's For
Generating safety-critical machine code with formal correctness guarantees. Targets DAL-B (Design Assurance Level B) certification for aerospace/automotive/medical.

## Who Would Use It
Safety-critical systems engineers in aerospace, automotive, medical devices. Researchers exploring formal verification of compiler output.

## Honest Assessment

**This repo is notable for its intellectual honesty** — a rarity in this ecosystem. The README explicitly states:

> "This is not a production tool — it is an experimental exploration of what a correctness-verified compiler stack could look like."

And:

> "Formal Verification Coverage and Fuzz Uptime badges have been removed pending independent audit."

This candor is refreshing compared to the grander claims elsewhere in the fleet. The README clearly delineates "What's Real" (system prober, benchmark engine, JIT compilation, perf database) from aspirational goals.

**The GUARD DSL concept is interesting** — a domain-specific language for safety constraints that compiles to verified machine code. The multi-language JIT approach (compiling C, Zig, Fortran, Nim kernels at startup and selecting the fastest) is creative but practically complex.

**Concerns:**
- The `cargo install --path flux-compiler` in Quick Start contradicts the "Python" language tag — unclear what's actually installable.
- Formal verification claims require external audit by definition — self-claims are meaningless here.
- The Coq proof files mentioned would need expert review.

**Bottom line:** Most honest README in the ecosystem. The compiler concept is legitimate research territory. The self-aware framing ("what's real" vs aspirational) makes this one of the more trustworthy repos.
