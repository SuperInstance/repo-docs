# lever-runner-wasm

## Intention

WebAssembly build of lever-runner carapace for browser deployment

## How It Works

### Intent Hashing (BLAKE2b-128)
Every intent string is hashed using BLAKE2b with a 128-bit digest:
$$h = \text{BLAKE2b}_{128}(\text{intent})$$
BLAKE2b is a cryptographic hash function faster than MD5 and SHA-1, with a proven security margin. The hash provides `O(1)` exact-match lookup via hash-table comparison.
### Position-Aware Character Embedding
The `embed_intent` function produces a 64-dimensional vector capturing both *what* characters appear and *where* they appear:
**Dimensions 0–39: Character frequency with positional decay.** Each character's contribution is weighted by:
$$w_{\text{pos}}(i) = 1 + \frac{2}{1 + i}$$
where $i$ is the character position. Earlier characters contribute more — this mirrors the primacy effect in human text comprehension. The result is L²-normalized.
**Dimensions 40–55: Bigram frequency.** 16 hash buckets capture character-pair co-occurrence:
$$\text{bucket}(c_i, c_{i+1}) = (c_i \cdot 31 + c_{i+1}) \mod 16$$
This is a feature-hashing trick (Weinberger et al., 2009), reducing the $|\Sigma|^2$ bigram space to 16 dimensions.
**Dimensions 56–63: Structural features.** Log-normalized length, word count, average word length, character diversity, digit/path presence, separator ratio.
### Vector Search: Cosine Similarity
Similarity between query embedding $\mathbf{q}$ and stored embedding $\mathbf{d}$ is computed via cosine similarity:

## What It's For

WebAssembly build of lever-runner carapace for browser deployment

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** WASM

## Status Assessment

**Status: MODERATE**

Reasonable README (82 lines), includes examples.

- README length: 127 lines, 5976 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
