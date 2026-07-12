# plato-normalize

## Intention
Normalization and standardization for PLATO tile values

## How It Works
> Normalization methods for PLATO tile data — MinMax, Z-Score, Robust, Log, Quantile plato-normalize provides five normalization methods for scaling tile data to a common range. Each method can be fit to training data (learning min/max/mean/std/median/IQR), then applied to new data and inverted. A pipeline orchestrates normalization across multiple named series. Different sensors produce values on wildly different scales: temperature in Celsius (15-35), humidity in percent (0-100), CO2 in ppm...

## What It's For
Part of the PLATO ecosystem. Normalization and standardization for PLATO tile values

## Who Would Use It
Signal processing engineers working with PLATO tile streams.

## Language / Stack
Rust

## Status Assessment
🟢 Substantial — comprehensive documentation with architecture, examples, API refs

## Honest Assessment
Core component with thorough documentation, architecture diagrams, code examples, and test coverage. This is production-track work, not a stub.

## README Substance Level
- **Size:** 2539 bytes
- **Substance:** substantial
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Does, The Key Idea, Install, Quick Start, API Reference, Testing, License
