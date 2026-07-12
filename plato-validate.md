# plato-validate

## Intention
Input validation and sanitization for PLATO tile data

## How It Works
> Input validation for PLATO tile data — range checks, type checks, regex, custom rules plato-validate provides a rule-based validation system for tile data. Define rules (range, not-null, type, regex, enum, custom function), apply them to field-value maps, and get structured validation results with per-field error messages. Garbage in, garbage out. Before tile data enters the pipeline, validate it: temperature must be a number between -50 and 150, sensor_id must not be null, status must be o...

## What It's For
Part of the PLATO ecosystem. Input validation and sanitization for PLATO tile data

## Who Would Use It
PLATO ecosystem developers and SuperInstance fleet operators.

## Language / Stack
Rust

## Status Assessment
🟢 Substantial — comprehensive documentation with architecture, examples, API refs

## Honest Assessment
Core component with thorough documentation, architecture diagrams, code examples, and test coverage. This is production-track work, not a stub.

## README Substance Level
- **Size:** 2031 bytes
- **Substance:** substantial
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Does, The Key Idea, Install, Quick Start, API Reference, Testing, License
