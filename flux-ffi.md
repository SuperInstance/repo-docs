# flux-ffi

**Category:** 🔗 Interop/Bridging
**Status:** 🟡 Development
**Language:** Rust
**README:** 5,247 bytes

## Intention
Cross-language FFI bindings for Flux constraint math primitives.

## How It Works
```
src/
├── lib.rs           # Public API + re-exports
├── eisenstein.rs    # Eisenstein integer operations
├── laman.rs         # Laman graph rigidity
├── holonomy.rs      # Holonomy checking
├── manhattan.rs     # Manhattan/lattice distance
├── pythagorean.rs   # 48-cell spectral encoding
└── ffi/
    └── bindings.rs  # Raw extern "C" bindings (auto-generated)
```

### FFI Layer

```
┌──────────────────────┐
│  Safe Rust API       │  ← What you use
├──────────────────────┤
│  Rust wrappers   ...

## What It's For
Cross-language FFI bindings for Flux constraint math primitives.

## Who Would Use It
Formal methods practitioners and safety-critical systems engineers.

## Honest Assessment
Has code examples. missing: benchmarks. Has implementation code but **test coverage needs verification**..
