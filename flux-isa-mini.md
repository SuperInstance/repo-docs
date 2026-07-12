# flux-isa-mini

**Category:** 🗄️ Preserved Artifact
**Status:** 🗄️ Preserved Artifact
**Language:** Makefile
**README:** 2,808 bytes

## Intention
Preserved workspace artifact

## How It Works
```rust
use flux_isa_mini::{FluxOpcode, FluxInstruction, FluxVm};

let mut vm = FluxVm::new();

// Validate depth is in [0, 200m]
let program = [
    FluxInstruction::new(FluxOpcode::Load, 45.3, 0.0),   // push measured depth
    FluxInstruction::new(FluxOpcode::Load, 0.0, 0.0),    // lower bound
    FluxInstruction::new(FluxOpcode::Load, 200.0, 0.0),  // upper bound
    FluxInstruction::new(FluxOpcode::Validate, 0.0, 0.0),
    FluxInstruction::new(FluxOpcode::Assert, 0.0, 0.0),
    FluxInstruct...

## What It's For
Preserved workspace artifact

## Who Would Use It
Nobody actively — this is a preserved snapshot.

## Honest Assessment
Has code examples. **preserved artifact** (snapshot, not active). missing: tests, CI, benchmarks.
