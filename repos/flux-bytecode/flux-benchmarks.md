# flux-benchmarks

**Category:** 📊 Testing/Profiling
**Status:** 🟡 Development
**Language:** Shell
**README:** 784 bytes

## Intention
Real performance data across 7 runtimes. 4.7x faster than CPython.

## How It Works

Benchmark scripts comparing FLUX VM implementations against native languages. Uses 100K iteration factorial benchmark on Oracle Cloud ARM64 (Ampere Altra, 4 cores, 24GB).

Results table:
| Runtime | Factorial ns/iter | Speed vs C |
|---------|-------------------|------------|
| Native C | 20 | 1.0x |
| Native Rust | 20 | 1.0x |
| FLUX C VM | 403 | 0.05x |
| Python | 1,885 | 0.01x |
| FLUX Python VM | ~141,000 | 0.0001x |

Also includes "Agent Token Efficiency" — tokens needed to write factorial(10): FLUX Assembly ~20 tokens vs Python ~25 vs C ~50.

## What It's For
Performance tracking for FLUX VM implementations and comparison against native languages.

## Who Would Use It
FLUX ecosystem developers optimizing VM implementations. Performance engineers evaluating bytecode VMs.

## Honest Assessment

**The numbers are honest** — and that's the interesting part. The FLUX Python VM at ~141,000 ns/iter is ~75x slower than the C VM at 403 ns/iter, which makes sense (Python interpreter overhead). The claim "4.7x faster than CPython" is technically true for tight arithmetic (CPython factorial at 1,885 vs FLUX C VM at 403) but misleading — the FLUX C VM is written in C, so it's really "C bytecode interpreter faster than CPython interpreter," which is expected.

**The FLUX Python VM being ~75x slower than CPython** (141,000 vs 1,885) is the more honest number — that's the overhead of interpreting bytecode in Python. This suggests the Python VM is a reference implementation, not a production runtime.

The "Agent Token Efficiency" section is the real insight — if FLUX bytecode genuinely takes fewer LLM tokens to express equivalent logic, that's the actual value proposition for AI agent systems. Token cost is the bottleneck for LLM-driven agents, not CPU cycles.

**Bottom line:** Small but honest benchmark. The "4.7x faster than CPython" headline is cherry-picked but the actual data is transparent. The token efficiency angle is the more compelling argument.
