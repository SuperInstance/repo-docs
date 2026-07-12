# adinkra-math-pypi

**Cluster:** math-research  
**Language:** Python  
**Source:** [SuperInstance/adinkra-math-pypi](https://github.com/SuperInstance/adinkra-math-pypi)

## Intention

West African Adinkra symbolic encoding + SUSY adinkras for data scientists

## How It Works

**Symbol Vectors:** Each `SymbolType` maps to a dimension in a fixed-length feature vector. A symbol's vector is the weighted sum of its primitives' contributions.

**Concept Encoding:** Uses deterministic hashing (SHA-family) to map arbitrary text to a float vector of configurable dimension. Same input always produces the same vector.

**K-means:** Standard Lloyd's algorithm — random initialization, assign to nearest centroid, recompute centroids, repeat until convergence or max iterations.

**SUSY Adinkras:** For rank N, creates 2^(N-1) boson and 2^(N-1) fermion nodes connected by N generato

## What It's For

West African Adinkra symbolic encoding + SUSY adinkras for data scientists

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (186 lines, 6700 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# adinkra-math

> West African Adinkra symbols as a mathematical framework — symbolic encoding, topology, supersymmetry, and machine learning.

## What This Does

`adinkra-math` implements the mathematics inspired by Adinkra symbols — the visual symbols of the Ashanti people of West Africa. It provides symbolic encoding of concepts as geometric primitives, glyph composition with invariant preservation, topological analysis (Euler characteristic, genus), supersymmetry Adinkra graphs (Boson-Fermion classification with chromotopology verification), and basic ML operations (kNN, K-means) on symbol vectors. Use it for symbolic AI, topological data analysis, physics simulations, or cultural math education.

## The Cultural Root

Adinkra symbols originated with the Ashanti (Asante) people of Ghana and Côte d'Ivoire. Each symbol encodes a proverb or concept — Sankofa ("go back and fetch it") represents learning from the past. The mathematical insight: **symbols compress complex meaning into structured geometric primitives**, which is exactly what feature vectors do in machine learning. Adinkras also appear in theoretical physics: supersymmetry Adinkras are bipartite graphs encoding the relationship between bosons and fermions.

## Install

```bash
pip install adinkra-math
```

## Quick Start

```python
from adinkramath.symbol import Symbol, SymbolType, get_builtin_symbols
from adinkramath.glyph import Glyph, GlyphOperation, compose
from adinkramath.topology import euler_characteristic, genus
from adinkramath.encoding import encode_concept, knn, kmeans
from adinkramath.supersymmetry import create_adinkra, verify_chromotopology

# Work with built-in Adinkra symbols
symbols = get_builtin_symbols()
for s in symbols:
    print(f"{s.name}: {s.to_vector()}")

# Compose glyphs (symbols combined)
g1 = Glyph(symbols=[symbols[0]])
g2 = Glyph(symbols=[symbols[1]])
composed = compose(g1, g2, GlyphOperation.SUPERIMPOSE)
print(f"Composed weight: {composed.total_weight()}")

# Check topological invariant
from adinkramath.glyph import preserve_invariant
print(f"Invariant preserved: {preserve_invariant(composed)}")

# Encode concepts as vectors
c1 = encode_concept("courage", seed=42)
c2 = encode_concept("wisdom", seed=42)
print(f"Vector length: {len(c1.vector)}")

# K-nearest neighbors
from adinkramath.encoding import Concept, nearest_concept
concepts = [encode_concept(w, seed=0) for w in ["love", "war", "peace", "fear"]]
result = nearest_concept(encode_concept("bravery", seed=0).vector, concepts)

# K-means clustering
clusters = kmeans(concepts, k=2)

# Supersymmetry Adinkras
adinkra = create_adinkra(rank=2)
print(f"Bosons: {len(adinkra.bosons)}, Fermions: {len(adinkra.fermions)}")
valid = verify_chromotopology(adinkra)
print(f"Chromotopology valid: {valid}")

# Topology
euler = euler_characteristic(vertices=8, edges=12, faces=6)
print(f"Euler characteristic: {euler}, Genus: {genus(euler)}")
```

## API Reference

### `symbol` module

#### `SymbolType` (enum)
`CIRCLE`, `
```
