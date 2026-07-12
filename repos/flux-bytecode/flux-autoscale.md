# flux-autoscale

**Category:** ⚡ Hardware/GPU
**Status:** 🟡 Development
**Language:** Rust
**README:** 4,556 bytes

## Intention
Auto-scaling Flux bytecode execution based on workload demand. Scales up on backpressure, down on idle. More agents = more GPU streams.

## How It Works
The autoscaler evaluates a **scaling policy** on each tick:

### Scaling Decision Logic

```
avg_utilization = Σ(queue_depth_i / 100) / N

if avg_utilization > 0.8 OR any(backpressure):  → ScaleUp (+1 stream)
if avg_utilization < 0.2 AND all(queue_depth = 0): → ScaleDown (−1 stream)
else: → Hold
```

The thresholds (0.8 / 0.2) are the **scale_up_threshold** and **scale_down_threshold** respectively, configurable at construction time.

### Backpressure Signal

Backpressure is a boolean per-stream...

## What It's For
Auto-scaling Flux bytecode execution based on workload demand. Scales up on backpressure, down on idle. More agents = more GPU streams.

## Who Would Use It
Systems engineers and HPC developers targeting specific hardware (NVIDIA GPUs, FPGAs, AVX-512 CPUs).

## Honest Assessment
Has code examples. missing: tests, benchmarks.
