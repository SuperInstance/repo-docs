# liteparse-coverage

## Intention

Topological coverage analysis for liteparse: find holes in document format parsing using negative-space-testing

## How It Works

### 1. Build a Feature Space
Each parsed document becomes a **simplex** — a set of features it contains:
```
Document A: {text, tables}
Document B: {text, images}
Document C: {text, tables, images, formulas}
```
This builds a **simplicial complex** — a topological space where known-working configurations live.
### 2. Compute Betti Numbers
Betti numbers count the **holes** in this space:
| Symbol | Name | What it means for coverage |
|--------|------|---------------------------|
| **β₀** | Connected components | **Format silos** — if > 1, some features are tested in complete isolation |
| **β₁** | 1-dimensional holes | **Missing pairs** — two features that have never appeared together in a test |
| **β₂** | 2-dimensional holes | **Missing triples** — three features that have never co-occurred |

## What It's For

Topological coverage analysis for liteparse: find holes in document format parsing using negative-space-testing

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (131 lines), mentions tests.

- README length: 193 lines, 5967 characters
- Documented sections: The Problem, How It Works, Getting Started, Integration, The Math (Briefly)

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
