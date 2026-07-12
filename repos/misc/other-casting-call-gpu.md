# casting-call-gpu

**Cluster:** gpu-native-compute  
**Language:** Python  
**Source:** [SuperInstance/casting-call-gpu](https://github.com/SuperInstance/casting-call-gpu)

## Intention

GPU-native engine for anchor-point signature matrices, voice spline interpolation, and batch corpus processing

## How It Works

It Fits

The computational engine behind [casting-call-mcp](https://github.com/SuperInstance/casting-call-mcp). Uses GPU acceleration for the heavy math of model selection.

- **[casting-call-mcp](https://github.com/SuperInstance/casting-call-mcp)** — MCP interface for casting decisions
- **[cocapn-benchmark](https://github.com/SuperInstance/cocapn-benchmark)** — Benchmark data feeds signatures
- **[Claude-PRISM-CF](https://github.com/SuperInstance/Claude-PRISM-CF)** — Edge routing

## What It's For

GPU-native engine for anchor-point signature matrices, voice spline interpolation, and batch corpus processing

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (77 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# casting-call-gpu — GPU-Accelerated Model Casting

**Anchor-point signature mathematics for model selection. GPU-accelerated distance matrices, voice spline interpolation, and model clustering.**

## What This Gives You

- **Signature computation** — represent text/model outputs as points in N-dimensional anchor space
- **GPU-accelerated distances** — fast signature distance matrix computation (CuPy/PyTorch, NumPy fallback)
- **Voice spline interpolation** — predict model performance on novel task types
- **Model clustering** — group models by behavioral similarity
- **Insight CLI** — command-line tool for quick model comparisons

## Quick Start

```bash
pip install casting-call-gpu
```

```python
from cast_gpu import SignatureEngine, VoiceSpline, ModelCluster

# Compute signatures for model outputs
engine = SignatureEngine(anchors=64)
sig_a = engine.signature("Claude produces clean, well-documented code")
sig_b = engine.signature("GPT-4 generates creative but verbose solutions")

# Distance tells us how similar
distance = engine.distance(sig_a, sig_b)
print(f"Signature distance: {distance:.3f}")

# Build voice spline for a model
spline = VoiceSpline(model="claude-3.5-sonnet")
spline.add_point(task_type="code-gen", signature=sig_a)
spline.add_point(task_type="review", signature=sig_b)

# Predict performance on a new task type
predicted = spline.interpolate(task_type="refactoring")
print(f"Predicted similarity: {predicted:.2f}")

# Cluster models by behavior
cluster = ModelCluster()
cluster.add("claude-3.5-sonnet", signatures=[sig_a])
cluster.add("gpt-4o", signatures=[sig_b])
groups = cluster.fit(n_clusters=3)
```

### CLI

```bash
# Quick model comparison
insight compare --models claude-3.5-sonnet,gpt-4o,deepseek-chat --task "code review"

# Cluster analysis
insight cluster --data signatures.jsonl --clusters 3
```

## How It Fits

The computational engine behind [casting-call-mcp](https://github.com/SuperInstance/casting-call-mcp). Uses GPU acceleration for the heavy math of model selection.

- **[casting-call-mcp](https://github.com/SuperInstance/casting-call-mcp)** — MCP interface for casting decisions
- **[cocapn-benchmark](https://github.com/SuperInstance/cocapn-benchmark)** — Benchmark data feeds signatures
- **[Claude-PRISM-CF](https://github.com/SuperInstance/Claude-PRISM-CF)** — Edge routing

## Testing

```bash
pytest tests/
```

## Installation

```bash
pip install casting-call-gpu
```

Python 3.10+. Optional: CuPy or PyTorch for GPU acceleration. MIT license.

```
