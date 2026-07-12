# flux-ast

**Category:** ✅ Constraint/Safety
**Status:** 🟢 Production-oriented
**Language:** Rust
**README:** 2,065 bytes

## Intention
FLUX constraint safety - flux-ast

## How It Works
```rust
use flux_ast::*;

let constraint = ConstraintNode::And(vec![
    ConstraintNode::Bound(BoundNode {
        signal: SignalRef::local("velocity"),
        lower: Value::Integer(0),
        upper: Value::Integer(300),
        severity: Severity::Hard,
    }),
    ConstraintNode::Delta(DeltaNode {
        signal: SignalRef::local("velocity"),
        max_delta: Value::Integer(15),
        window: Window::PerFrame,
        severity: Severity::Hard,
    }),
]);

// All generators read from the...

## What It's For
FLUX constraint safety - flux-ast

## Who Would Use It
Formal methods practitioners and safety-critical systems engineers.

## Honest Assessment
Has code examples. missing: benchmarks. Has implementation code but **test coverage needs verification**..
