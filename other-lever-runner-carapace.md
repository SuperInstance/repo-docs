# lever-runner-carapace

## Intention

Shell runner for lever — multi-agent orchestration with ternary control signals.

## How It Works

**Three-gate pipeline** — the core resolution engine:
```
Input intent string
↓
Gate 1: Exact hash match (BLAKE2b-256 comparison)
↓ (miss)
Gate 2: Vector similarity (cosine ≥ 0.85 threshold)
↓ (miss/below threshold)
Gate 3: Unresolved (return best candidate + score)
```
**Gate 1 — BLAKE2b hashing**: Each registered intent pattern is hashed with BLAKE2b-256, producing a deterministic 32-byte digest. Query intents are hashed the same way; comparison is O(1) memcmp. BLAKE2b is faster than SHA-256 while providing equivalent security. For N registered patterns, Gate 1 costs O(N) hash comparisons (each O(1)) — typically <10μs for 1000 intents.
**Gate 2 — Position-aware embedding**: No neural network — embeddings are computed mathematically:
```
For each word at position p in the intent:
salted = f"{p}:{word}"

## What It's For

Shell runner for lever — multi-agent orchestration with ternary control signals.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (92 lines), mentions tests, includes examples.

- README length: 121 lines, 5627 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
