# flux-diff

**Category:** 🔗 Interop/Bridging
**Status:** 🟡 Development
**Language:** Python
**README:** 513 bytes

## Intention
FLUX bytecode diff tool — compare programs, show structural changes

## How It Works
```python
from diff import FluxDiffer
differ = FluxDiffer()
result = differ.diff([0x18, 0, 42, 0x00], [0x18, 0, 99, 0x00])
print(result.to_markdown())
# Similarity: 50.0%
# 0: 18 00 2a → 18 00 63  (MOVI operand change)
```

8 tests passing.

## What It's For
FLUX bytecode diff tool — compare programs, show structural changes

## Who Would Use It
Language engineers and VM designers working on bytecode runtimes for agent systems.

## Honest Assessment
Has code examples. claims 8 tests. missing: tests, CI, benchmarks.
