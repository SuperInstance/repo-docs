# dial-theory

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/dial-theory](https://github.com/SuperInstance/dial-theory)

## Intention

Dial theory framework for algebraic structure analysis

## How It Works

**Seven Axes:** Each tradition is positioned on seven orthogonal dimensions:
1. **Epistemology** — Rationalist (−1) ↔ Empiricist (+1)
2. **Social** — Individualist (−1) ↔ Collectivist (+1)
3. **Methodology** — Reductionist (−1) ↔ Holist (+1)
4. **Abstraction** — Abstract (−1) ↔ Concrete (+1)
5. **Change** — Conservative (−1) ↔ Progressive (+1)
6. **Scope** — Universalist (−1) ↔ Relativist (+1)
7. **Reasoning** — Formalist (−1) ↔ Intuitionist (+1)

A `Dial` is a single axis-position pair with an optional confidence value (0.0–1.0). A `Tradition` is a collection of seven dials, forming a point i

## What It's For

Dial theory framework for algebraic structure analysis

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (90 lines, 5560 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Dial Theory

**A framework for mapping intellectual traditions onto a seven-dimensional dial space** — quantifying philosophical positions as coordinates and computing distances, clusters, and synthesis potential between traditions. It turns qualitative "schools of thought" into geometric data that can be measured, clustered, and visualized.

## Why It Matters

The humanities struggle with a fundamental problem: how do you compare intellectual traditions objectively? "How close is Pragmatism to Analytic Philosophy?" is usually answered with prose, not numbers. Dial Theory provides a quantitative alternative: position each tradition on seven continuous axes (epistemology, social organization, methodology, etc.) and use geometric distance to measure similarity.

This approach has real applications in **computational humanities**, **education** (visualizing how ideas relate), **AI alignment** (mapping different safety frameworks), and **interdisciplinary research** (finding traditions that bridge disciplines). The framework supports:

- **Distance computation** — Euclidean, angular, and Manhattan distances in 7D dial space
- **Nearest-neighbor search** — Find the k most similar traditions to any query
- **Bridge detection** — Find traditions that mediate between distant schools of thought
- **Synthesis with paradox detection** — Merge two traditions and identify where their core commitments conflict
- **Evolution simulation** — Model how traditions drift, split, and merge over historical time
- **Topology analysis** — Find clusters, sparse regions ("holes"), and boundary traditions

## How It Works

**Seven Axes:** Each tradition is positioned on seven orthogonal dimensions:
1. **Epistemology** — Rationalist (−1) ↔ Empiricist (+1)
2. **Social** — Individualist (−1) ↔ Collectivist (+1)
3. **Methodology** — Reductionist (−1) ↔ Holist (+1)
4. **Abstraction** — Abstract (−1) ↔ Concrete (+1)
5. **Change** — Conservative (−1) ↔ Progressive (+1)
6. **Scope** — Universalist (−1) ↔ Relativist (+1)
7. **Reasoning** — Formalist (−1) ↔ Intuitionist (+1)

A `Dial` is a single axis-position pair with an optional confidence value (0.0–1.0). A `Tradition` is a collection of seven dials, forming a point in 7D space.

**Distance metrics:** The primary distance is Euclidean (L2) across all seven axes, with optional per-axis weights. Angular distance (cosine similarity) captures directional alignment regardless of magnitude. The tension points analysis identifies which specific axes contribute most to the distance between two traditions.

**Synthesis and paradox detection:** When synthesizing two traditions (weighted average of positions), the framework detects paradoxes — axes where both parents have strong (>0.5) opposing positions. For example, synthesizing Marxism (Change=+0.9) with Confucianism (Change=−0.6) produces a paradox on the Change axis because both traditions have strong, opposite commitments.

**Topology analysis:** Single-linkage clustering with unio
```
