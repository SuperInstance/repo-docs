# eisenstein-embed

## Intention
Eisenstein integer embeddings with a 5-layer matching cascade — word fingerprints, bitvector search, deadband caching, and domain-SIF for text similarity.

## How It Works
The **semantic search layer** using Eisenstein lattice geometry:

- eisenstein-triples — Eisenstein integer theory
- eisenstein-vs-z2-rs — lattice comparison benchmarks
- flux-index — code search using these embeddings
- constraint-theory-core — lattice snap operations

## What It's For
- **5-layer cascade matcher** — bitvector → deadband cache → Eisenstein quantization → domain SIF → BMA monitor
- **Word fingerprints** — hash words to Eisenstein lattice coordinates for fast similarity
- **Bitvector search** — Hamming distance similarity with inverted index acceleration
- **Deadband cache** — memoize lookups within deadband tolerance (lattice-aware caching)
- **Domain SIF** — Smo

## Who Would Use It
```bash
pip install eisenstein-embed
```

Requires Python ≥ 3.10.

## Language / Stack
Python

## Status Assessment
Documented with tests, API docs, and installation guide (100 line README).

## Honest Assessment
Has documentation (100 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/eisenstein-embed](https://github.com/SuperInstance/eisenstein-embed)*
