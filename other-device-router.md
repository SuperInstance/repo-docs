# device-router

**Cluster:** fleet-agent-infra  
**Language:** Python  
**Source:** [SuperInstance/device-router](https://github.com/SuperInstance/device-router)

## Intention

Heterogeneous compute router — auto-detect CUDA, iGPU, CPU, NPU and route ML workloads optimally

## How It Works

### Without any dependencies
`device-router` runs pure CPU detection:
- CPU architecture, core count, frequency
- Instruction set features (AVX, AVX2, AVX-512, VNNI, AMX, NEON, SSE4)
- This is enough to route small models optimally

### With `torch` installed
Adds CUDA detection:
- GPU count, name, VRAM, compute capability
- CUDA/cuDNN version
- Enables AMP and GPU benchmarking

### With `torch-directml` installed
Adds iGPU detection:
- DirectML device availability
- Enables iGPU offloading for medium workloads

### Routing decision logic

[code]

## What It's For

Heterogeneous compute router — auto-detect CUDA, iGPU, CPU, NPU and route ML workloads optimally

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (157 lines, 5183 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# device-router

[![PyPI version](https://img.shields.io/pypi/v/device-router.svg)](https://pypi.org/project/device-router/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/downloads/)
[![Tests](https://img.shields.io/badge/tests-passing-brightgreen.svg)](tests/)
[![Status: Beta](https://img.shields.io/badge/status-beta-orange.svg)](https://pypi.org/project/device-router/)

> Heterogeneous compute router — auto-detect CUDA, iGPU, CPU, NPU and route ML workloads optimally.

Modern laptops and workstations have **multiple compute units**: a discrete GPU (CUDA), an integrated GPU (iGPU/DirectML), a Neural Processing Unit (NPU), and the CPU. Most ML frameworks pick one device and stick with it. **That's wasteful.**

`device-router` detects what's available and routes each workload to the best device automatically.

## Why it matters

| Workload | Best device | Why |
|---|---|---|
| Single embedding | CPU | No GPU transfer overhead (~9μs) |
| Small model (int8) | CPU (VNNI) | CPU has dedicated VNNI instructions |
| Medium model batched | iGPU | Good compute, low power |
| Large model training | CUDA GPU | Parallelism + AMP |
| ONNX inference | CPU | ONNX Runtime is CPU-optimized |

## Install

```bash
pip install device-router
```

Optional dependencies:

```bash
pip install device-router[cuda]      # CUDA GPU detection via torch
pip install device-router[directml]  # iGPU detection via torch-directml
pip install device-router[all]       # Everything
pip install device-router[dev]       # pytest + numpy for development
```

## Quick start

```python
from device_router import DeviceRouter, RoutingStrategy

router = DeviceRouter()
router.detect()  # Finds CUDA, DirectML, CPU features, NPU

# Route a workload
decision = router.route(
    model_size=1_000_000,  # parameters
    batch_size=32,
    precision="fp32",      # or "fp16", "bf16", "int8"
    strategy=RoutingStrategy.AUTO,
)
print(f"Use {decision.device} ({decision.reason})")
# → Use cuda (Medium/large model (1,000,000 params) — GPU recommended)

# System overview
overview = router.overview()
# Returns: {cuda: {...}, cpu: {...}, igpu: {...}, npu: {...}}
```

## Routing strategies

| Strategy | Description | Use case |
|---|---|---|
| `AUTO` | Best guess based on model size & batch | Default |
| `LATENCY` | Optimize for single-sample speed | Real-time inference |
| `THROUGHPUT` | Optimize for batch processing | Batch jobs |
| `POWER` | Prefer CPU/iGPU for efficiency | Laptops, mobile |

## How it works

### Without any dependencies
`device-router` runs pure CPU detection:
- CPU architecture, core count, frequency
- Instruction set features (AVX, AVX2, AVX-512, VNNI, AMX, NEON, SSE4)
- This is enough to route small models optimally

### With `torch` installed
Adds CUDA detection:
- GPU count, name, VRAM, compute capability
- CUDA/cuDNN version
- E
```
