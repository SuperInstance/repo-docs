# plato-threshold

## Intention
Adaptive threshold calculation for PLATO deadband filters

## How It Works
> Adaptive and static thresholds for PLATO tile data — moving average, exponential smoothing, percentile-based plato-threshold provides both static (fixed min/max) and adaptive thresholds that adjust based on observed data. Adaptive methods include moving average, exponential smoothing, and percentile-based approaches. Each threshold check returns whether a value is within range, how far outside, and a confidence score. Static thresholds break. A temperature alert set at 30°C fires all summer...

## What It's For
Part of the PLATO ecosystem. Adaptive threshold calculation for PLATO deadband filters

## Who Would Use It
PLATO ecosystem developers and SuperInstance fleet operators.

## Language / Stack
Rust

## Status Assessment
🟢 Substantial — comprehensive documentation with architecture, examples, API refs

## Honest Assessment
Core component with thorough documentation, architecture diagrams, code examples, and test coverage. This is production-track work, not a stub.

## README Substance Level
- **Size:** 2149 bytes
- **Substance:** substantial
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Does, The Key Idea, Install, Quick Start, API Reference, Testing, License
