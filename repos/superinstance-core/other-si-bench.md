# si-bench

## Intention
Fleet-wide benchmarking and performance regression testing for SuperInstance conservation-law crates

## How It Works
Fleet-wide benchmarking and performance regression testing for SuperInstance. si-bench measures the performance of conservation-law operations across the fleet and detects regressions between runs. - bench — Core benchmarking with statistical analysis (mean, median, std_dev, p95, p99) - conservation_bench — Pre-built conservation-law benchmarks - registry_bench — Pre-built registry/scan benchmarks - regression — Regression detection with configurable threshold - report — Output formatting (table, markdown, JSON)

## What It's For
Fleet-wide benchmarking and performance regression testing for SuperInstance conservation-law crates

## Who Would Use It
Rust developers in the SuperInstance conservation-law ecosystem

## Language / Stack
Rust

## Status Assessment
**Developing** — Moderate documentation with some structure and examples.

- README size: 2,358 characters, 80 lines
- Code examples: 3 blocks
- Installation instructions: no
- Testing mentioned: yes
- License mentioned: yes
- API documentation: no
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (3 code blocks)
- Testing mentioned

**Concerns:**
- No clear installation instructions
- One of 40+ si-* repos — may be a proof-of-concept rather than production tool

**Overall:** Early but potentially interesting — read the source to verify.
