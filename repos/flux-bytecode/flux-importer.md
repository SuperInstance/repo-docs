# flux-importer

**Category:** 🔗 Interop/Bridging
**Status:** 🟡 Development
**Language:** Rust
**README:** 8,030 bytes

## Intention
Flux bytecode → synthetic MIR bridge for cuda-oxide. Translates agent-native Flux bytecode into MIR compatible with the Rust-to-PTX compilation pipeline. First-class ternary ops, GPU addressing, construct imports.

## How It Works
### Translating raw bytecode

The most direct way to use the crate is to hand it a slice of bytes and receive a `MirModule`:

```rust
use flux_importer::{FluxToMir, ImportConfig};

// Bytecode: MOVI R0, 42; HALT
let bytecode = vec![0x01, 0x00, 0x2A, 0x00, 0xFF];

let config = ImportConfig::default();
let module = FluxToMir::translate(&bytecode, &config)?;

// `module` is now synthetic MIR ready for mir-lower.
assert_eq!(module.functions[0].name, "flux_main");
```

### Using the GPU builder

If y...

## What It's For
Flux bytecode → synthetic MIR bridge for cuda-oxide. Translates agent-native Flux bytecode into MIR compatible with the Rust-to-PTX compilation pipeline. First-class ternary ops, GPU addressing, construct imports.

## Who Would Use It
Systems engineers and HPC developers targeting specific hardware (NVIDIA GPUs, FPGAs, AVX-512 CPUs).

## Honest Assessment
Has code examples. missing: tests, benchmarks.
