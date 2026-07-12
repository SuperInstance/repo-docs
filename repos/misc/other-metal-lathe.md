# metal-lathe

## Intention

The research wheel — churns experimental results into novel questions, hypotheses, and experiments tested on metal

## How It Works

```bash
# No package needed — single-file Python script
pip install numpy  # required for conservation-verification.py
python metal_lathe.py
```
```python
from metal_lathe import MetalLathe, Observation
# Initialize the wheel
lathe = MetalLathe(state_dir="~/.metal-lathe")
# Phase 1: OBSERVE — record what you measured
lathe.observe(
source="lever-runner",
metric="call_degree:process_request",
value=47,
unit="edges",

## What It's For

The research wheel — churns experimental results into novel questions, hypotheses, and experiments tested on metal

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Python

## Status Assessment

**Status: MODERATE**

Reasonable README (179 lines), mentions tests, includes examples.

- README length: 221 lines, 8300 characters
- Documented sections: Why This Exists, The Six Phases, Installation, Usage, API Reference

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
