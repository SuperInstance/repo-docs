# constraint-bench-suite

## Summary
AVX-512 + CUDA benchmark suite.

## Intention
Benchmark Eisenstein integer constraint checking across CPU SIMD (AVX-512) and GPU (CUDA) to determine optimal precision and throughput on real silicon.

## How It Works
Implemented in C.

## What It's For
- Performance benchmarking on real CPU/GPU silicon

## Who Would Use It
- Researchers and engineers in distributed systems, physics simulation, AI agent coordination
- Developers needing numerical determinism and zero-drift computation
- Music theorists and computational musicologists
- HPC developers optimizing for GPU/SIMD

## Language/Stack
- **Primary language:** C
- **Dependencies:** Minimal (most ecosystem crates are zero-dependency)

## Status Assessment
**No README available** — repository may be empty or a placeholder.

## Honest Assessment
Genuinely useful benchmark data. The finding that FP64 is fastest on Zen 5 is counterintuitive and valuable. BF16 catastrophic failure analysis is important. However, this is benchmark output, not a reusable library. Hardware-specific results may not generalize.
