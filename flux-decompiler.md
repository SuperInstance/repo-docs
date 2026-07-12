# flux-decompiler

**Category:** ⚙️ Core VM/ISA
**Status:** 🟡 Development
**Language:** Python
**README:** 2,844 bytes

## Intention
FLUX bytecode decompiler — bytecode to assembly with labels and control flow

## How It Works
```python
from flux_decompiler import FluxDecompiler

# Decompile a factorial program
bytecode = [0x18, 0, 6, 0x18, 1, 1, 0x22, 1, 1, 0, 0x09, 0, 0x3D, 0, -6, 0, 0x00]
dec = FluxDecompiler(bytecode)
result = dec.decompile()

print(f"Instructions: {result.total_instructions}, Bytes: {result.total_bytes}")
print(f"Jumps: {result.jump_count}, Labels: {len(result.labels)}")

# Clean assembly output
print(result.to_asm())

# Annotated output with stats and control flow markers
print(result.to_annotat...

## What It's For
FLUX bytecode decompiler — bytecode to assembly with labels and control flow

## Who Would Use It
Language engineers and VM designers working on bytecode runtimes for agent systems.

## Honest Assessment
Has code examples. missing: tests, benchmarks.
