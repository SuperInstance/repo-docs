# embedding-utils

## Intention
A Python library for working with text embeddings, similarity search, and vector operations.

## How It Works
cache.set("hello", [0.1, 0.2], model="gpt-3")
embedding = cache.get("hello", model="gpt-3")

## What It's For
- **Similarity Metrics**: Cosine similarity, Euclidean distance, dot product, Manhattan distance, Jaccard similarity
- **Vector Operations**: Normalization, mean, weighted mean, concatenation, scaling
- **Embedding Cache**: In-memory cache with LRU eviction and disk persistence
- **Batch Processing**: Efficient batch embedding generation
- **Similarity Search**: In-memory index with optional metad

## Who Would Use It
```bash
pip install embedding-utils
```

## Language / Stack
Python

## Status Assessment
Documented with code examples and API references (223 line README).

## Honest Assessment
Well-documented (223 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/embedding-utils](https://github.com/SuperInstance/embedding-utils)*
