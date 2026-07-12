# plato-downsample

## Intention
Intelligent downsampling for PLATO tile streams with anomaly preservation

## How It Works
> Intelligent downsampling for PLATO tile streams with anomaly preservation plato-downsample reduces data volume while preserving the shape of your signal. It implements multiple methods — LTTB (Largest-Triangle-Three-Buckets), MinMax, Average, and Random — and can optionally preserve anomalous data points that would otherwise be lost. An ESP32 sensor producing 100 readings/second can't send them all to the cloud. But naive downsampling (take every Nth point) destroys the interesting parts — ...

## What It's For
Part of the PLATO ecosystem. Intelligent downsampling for PLATO tile streams with anomaly preservation

## Who Would Use It
Signal processing engineers working with PLATO tile streams.

## Language / Stack
Rust

## Status Assessment
🟢 Substantial — comprehensive documentation with architecture, examples, API refs

## Honest Assessment
Core component with thorough documentation, architecture diagrams, code examples, and test coverage. This is production-track work, not a stub.

## README Substance Level
- **Size:** 2054 bytes
- **Substance:** substantial
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Does, The Key Idea, Install, Quick Start, API Reference, Testing, License
