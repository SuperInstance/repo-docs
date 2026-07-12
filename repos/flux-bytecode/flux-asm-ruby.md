# flux-asm-ruby

**Category:** ⚙️ Core VM/ISA
**Status:** 🟡 Development
**Language:** Ruby
**README:** 2,262 bytes

## Intention
FLUX ISA assembler/disassembler in pure Ruby — 42-opcode Turing-incomplete VM

## How It Works
```
lib/flux-asm/
  flux-asm.rb           # Main require + VERSION
  flux-asm/
    opcodes.rb          # FLUX ISA v3.0 opcode table + lookup helpers
    assembler.rb       # Text assembly → binary bytecode
    disassembler.rb    # Binary bytecode → text assembly
    vm.rb              # Reference execution engine
```

## Opcode Support

Core subset of FLUX ISA v3.0:
- **Arithmetic**: `NOP`, `IAdd`, `ISub`, `IMul`, `IDiv`, `IRem`, `INeg`, `IAbs`
- **Logical**: `IAnd`, `IOr`, `IXor`, `INot`, `ISHL...

## What It's For
FLUX ISA assembler/disassembler in pure Ruby — 42-opcode Turing-incomplete VM

## Who Would Use It
Language engineers and VM designers working on bytecode runtimes for agent systems.

## Honest Assessment
Has real code examples and installation instructions. missing: tests, benchmarks.
