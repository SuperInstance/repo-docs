# plato-correlate

## Intention
Cross-correlation and dependency detection for PLATO tile streams

## How It Works
> Cross-correlation and dependency detection between PLATO tile streams plato-correlate detects relationships between tile streams using cross-correlation. Given multiple named time series, it finds which ones are correlated, at what lag, and builds a dependency graph showing which streams predict which others. If kitchen temperature rises 5 minutes before the HVAC kicks on, that's a lagged correlation. plato-correlate slides one time series past another at different lags and computes the Pea...

## What It's For
Part of the PLATO ecosystem. Cross-correlation and dependency detection for PLATO tile streams

## Who Would Use It
PLATO ecosystem developers and SuperInstance fleet operators.

## Language / Stack
Rust

## Status Assessment
🟢 Substantial — comprehensive documentation with architecture, examples, API refs

## Honest Assessment
Core component with thorough documentation, architecture diagrams, code examples, and test coverage. This is production-track work, not a stub.

## README Substance Level
- **Size:** 2369 bytes
- **Substance:** substantial
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Does, The Key Idea, Install, Quick Start, API Reference, Testing, License
