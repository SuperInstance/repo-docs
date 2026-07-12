# position-aware-embed

## Intention
Position-aware text embedding — 44% top-1 accuracy for command matching, sub-microsecond latency

## How It Works
Position-weighted text embedding for command matching — 44% top-1 accuracy with ~1µs latency and zero ML dependencies. Pure hash embeddings treat "check disk" and "disk check" as identical — same bag of words, same hash. But in command matching, word order matters: "check disk" means "run the disk check command," while "disk check" probably means "show the disk check results." This crate fixes that by hashing each word with its position (blake2b("0:check"), blake2b("1:disk")) and weighting by position (front-loaded: 1/(1 + i0.5)). The result: 44% top-1 accuracy on command matching vs 0% for pure hash. The design is deliberately zero-dependency for ML. No model downloads, no GPU, no Python. Just blake2b hashing, position weighting, and L2 normalization. The VectorIndex provides a simple bru

## What It's For
Position-aware text embedding — 44% top-1 accuracy for command matching, sub-microsecond latency

## Who Would Use It
Rust developers in machine learning

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 7,302 characters, 168 lines
- Code examples: 7 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (7 code blocks)
- Installation/usage instructions provided
- Testing mentioned
- Solid README with good coverage

**Concerns:**
- None immediately apparent from README alone

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
