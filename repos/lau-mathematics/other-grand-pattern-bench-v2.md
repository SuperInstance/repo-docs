# grand-pattern-bench-v2

## Intention
**Root Cause:** Raw perceptions have higher magnitude than averaged predictions, causing linear drift. The benchmark proved it: 100% violation rate across 1.8M room-tick pairs.

## How It Works
- **18 configurations:** 3 dimensions (4, 8, 16) × 3 windows (50, 200, 500) × 2 GC thresholds (100, 500)
- **10 rooms**, **10,000 ticks** each
- **Anomaly injection** at tick 5000: sudden 10× magnitude spike (100 ticks)
- **Metrics:** max error, avg error, violation rate, vibe convergence, surprise spike height

## What It's For
Fixing the conservation law — three proposed fixes tested against the broken baseline

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Has some documentation (47 lines).

## Honest Assessment
Minimal documentation (47 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/grand-pattern-bench-v2](https://github.com/SuperInstance/grand-pattern-bench-v2)*
