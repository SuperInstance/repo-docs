# moe-sheaf

## Intention

Sheaf cohomology of MoE routing — test DeepSeek's conjecture on generalization

## How It Works

- **Expert manifold representation** — each expert as a point on its weight manifold with activation statistics
- **Sheaf construction** — stalks = expert weights, restriction maps = routing overlap
- **Persistent cohomology** — H⁰ and H¹ via Vietoris-Rips filtration
- **Conjecture testing** — correlates H¹/param with generalization using bootstrap confidence
- **Full analysis pipeline** — feed a model state dict, get layer-by-layer cohomology report
- **Correlation analysis** — Pearson and Spearman r across multiple models

## What It's For

Sheaf cohomology of MoE routing — test DeepSeek's conjecture on generalization

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Python

## Status Assessment

**Status: LIGHT**

Short README (40 lines), mentions tests, includes examples.

- README length: 60 lines, 2137 characters
- Documented sections: What This Gives You, Quick Start, Installation, Testing, How It Fits

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
