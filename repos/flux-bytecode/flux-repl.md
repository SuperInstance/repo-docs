# flux-repl

**Category:** 🔧 Toolchain
**Status:** 🟡 Development
**Language:** Python
**README:** 799 bytes

## Intention
Interactive FLUX bytecode playground — assemble, execute, debug

## How It Works
```python
from repl import assemble, execute

# Assemble from text
result = assemble("MOVI R0, 42\nADD R0, R0, R0\nHALT")
print(result["hex"])  # 18 00 2a 20 00 00 00 00

# Execute bytecodes
state = execute(result["bytecode"])
print(state["registers"][:4])  # [84, 0, 0, 0]
```

## Web UI
Open `index.html` in a browser for interactive assembly and visualization.

15 tests passing.

## What It's For
Interactive FLUX bytecode playground — assemble, execute, debug

## Who Would Use It
Language engineers and VM designers working on bytecode runtimes for agent systems.

## Honest Assessment
Has code examples. claims 15 tests. missing: tests, CI, benchmarks.
