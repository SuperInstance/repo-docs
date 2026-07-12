# grand-pattern-bench

## Intention
**Cross-language conservation law benchmarks — does the math actually hold?**

## How It Works
- Pure Rust, zero external dependencies
- Deterministic pseudo-random perception generation (sin-based)
- Simple moving-average predictor with configurable window
- Magnitude-based garbage collection with configurable threshold
- Cosine similarity for vibe convergence measurement

## What It's For
The core claim: perception entries and prediction entries should stay balanced. This benchmark:

1. Runs 10,000 ticks on a 10-room graph
2. Varies dimension (8, 16, 32), window size (3, 5, 10), GC threshold (0.01, 0.05)
3. After each tick, checks conservation error `|Z_in| - |Z_out|`
4. Reports: max error, average error, ticks where conservation broke (>tolerance)

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Has some documentation (50 lines).

## Honest Assessment
Minimal documentation (50 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/grand-pattern-bench](https://github.com/SuperInstance/grand-pattern-bench)*
