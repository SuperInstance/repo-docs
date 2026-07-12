# flux-wasm

**Category:** ⚙️ Core VM/ISA
**Status:** 🟡 Development
**Language:** Makefile
**README:** 1,321 bytes

## Intention
FLUX WASM — WebAssembly bytecode VM in Rust. Run FLUX in any browser.

## How It Works
```javascript
const fs = require('fs');
const { FluxVM } = require('./build/flux.js');

const bytecode = new Uint8Array([0x2B, 0x01, 0x0A, 0x00, 0x80]); // MOVI R1, 10; HALT
const vm = new FluxVM(bytecode);
vm.execute();
console.log('R1 =', vm.readGP(1)); // 10
```

## Cross-Language Conformance

This WASM runtime produces identical results to the Python, C, Go, Rust, and Zig runtimes when given the same bytecode input. Verified through the 88 conformance test vectors in `SuperInstance/flux-conf...

## What It's For
FLUX WASM — WebAssembly bytecode VM in Rust. Run FLUX in any browser.

## Who Would Use It
Language engineers and VM designers working on bytecode runtimes for agent systems.

## Honest Assessment
Has real code examples and installation instructions. missing: CI, benchmarks.
