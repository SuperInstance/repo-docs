# cuda-constraint-engine

**Cluster:** constraint-theory  
**Language:** Cuda  
**Source:** [SuperInstance/cuda-constraint-engine](https://github.com/SuperInstance/cuda-constraint-engine)

## Intention

GPU constraint checking at 1B+ constraints/sec — CUDA library with C and Python APIs

## How It Works

[code]

**Key design decisions:**

1. **Memory pool** — All GPU buffers pre-allocated on `ce_create()`. No `cudaMalloc` in the hot path.
2. **CUDA graphs** — Capture the check kernel + memcpy and replay. 18x launch speedup for fixed-size workloads.
3. **Hot-swap bounds** — `cudaMemcpyAsync` updates bounds without touching the check kernel. Thread-safe.
4. **Multi-precision** — Template kernels for INT8, INT16, INT32, FP32, FP64.
5. **Eisenstein** — Specialized kernel computes `a² + ab + b²` and compares to `r²` in one pass.
6. **Thread-safe** — Multiple `CEStream` instances run checks concurre

## What It's For

GPU constraint checking at 1B+ constraints/sec — CUDA library with C and Python APIs

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Cuda — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (220 lines, 7148 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# cuda-constraint-engine ⚡

**GPU constraint checking at over a billion constraints/second.**

A developer-facing CUDA library for checking massive batches of constraints on NVIDIA GPUs. Multi-precision (INT8/INT16/INT32/FP32/FP64), Eisenstein integer support, async streams, CUDA graphs, and a zero-dep Python wrapper.

## Quick Start

### C

```c
#include "constraint_engine.h"

int main() {
    // Create engine (auto-selects GPU)
    CEEngine* engine = ce_create(-1);

    // Upload bounds: values must be in [10, 50]
    int32_t lo[] = {10, 10, 10, 10, 10};
    int32_t hi[] = {50, 50, 50, 50, 50};
    ce_upload_bounds_i32(engine, lo, hi, 5);

    // Check values
    int32_t values[] = {15, 99, 25, -1, 40};
    CEResult* result = ce_check_i32(engine, values, 5);

    printf("Violations: %d
", ce_result_violation_count(result));
    printf("Throughput: %.0f c/s
", ce_result_throughput(result));

    ce_result_destroy(result);
    ce_destroy(engine);
}
```

### Python

```python
from constraint_engine import ConstraintEngine
import numpy as np

engine = ConstraintEngine(max_constraints=100_000, precision='int32')

values = np.array([15, 99, 25, -1, 40], dtype=np.int32)
lo = np.array([10, 10, 10, 10, 10], dtype=np.int32)
hi = np.array([50, 50, 50, 50, 50], dtype=np.int32)

violations, mask = engine.check(values, lo, hi)
print(f"Violations: {violations}")  # 2 (99 and -1)
print(f"Stats: {engine.stats}")
```

## Build

```bash
make            # Build shared library + examples
make lib        # Build library only
make examples   # Build all examples
make install    # Install to /usr/local (needs sudo)
```

Requires: CUDA Toolkit 11.5+, GCC, `sm_86+` GPU (RTX 30-series / 40-series).

Change GPU architecture: `make ARCH=sm_80`

## Architecture

```
┌─────────────────────────────────────────────────┐
│                  Your Code                       │
│  ce_check_i32() / engine.check() / etc.         │
└───────────────────┬─────────────────────────────┘
                    │
┌───────────────────▼─────────────────────────────┐
│              CEEngine                            │
│  ┌─────────────┐  ┌──────────┐  ┌────────────┐ │
│  │ Memory Pool │  │ Kernels  │  │ Stream Pool│ │
│  │ (pre-alloc) │  │ (GPU)    │  │ (async)    │ │
│  └─────────────┘  └──────────┘  └────────────┘ │
│                                                  │
│  ┌─────────────────────────────────────────────┐ │
│  │ CUDA Graphs (optional, 18x launch speedup)  │ │
│  └─────────────────────────────────────────────┘ │
└──────────────────────────────────────────────────┘
```

**Key design decisions:**

1. **Memory pool** — All GPU buffers pre-allocated on `ce_create()`. No `cudaMalloc` in the hot path.
2. **CUDA graphs** — Capture the check kernel + memcpy and replay. 18x launch speedup for fixed-size workloads.
3. **Hot-swap bounds** — `cudaMemcpyAsync` updates bounds without touching the check kernel. Thread-safe.
4. **Multi-precision** — Template kernels for INT8, INT16, INT32, FP32, FP
```
