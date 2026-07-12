# oxide-capacity

## Intention
GPU cluster capacity planning with ternary utilization signals. Bin packing, scale recommendations, trend prediction.

## How It Works
GPU cluster capacity planning with ternary utilization signals. GPU clusters are expensive, and utilization is the only lever that matters. But "utilization" as a single number is a lie — a node at 95% memory but 20% compute isn't "overutilized," it's misconfigured. You need multi-dimensional bin packing, and you need a signal that captures the three states that actually drive decisions: waste money (underutilized, scale down), sweet spot (balanced, hold), risk (overloaded, scale up). The ternary classification ( 0.8 → overloaded) maps directly to operational decisions. No dashboards to interpret, no thresholds to tune per workload. One signal, one action.

## What It's For
GPU cluster capacity planning with ternary utilization signals. Bin packing, scale recommendations, trend prediction.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,869 characters, 135 lines
- Code examples: 3 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (3 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
