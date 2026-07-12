# shoal

## Intention
🔮 Conservation-bounded semantic search — the oracle that knows its limits

## How It Works
SHOAL — Semantic Hybrid Oracle for Agent Learning The conservation-bounded semantic search oracle. Every agent gets C = log₂(3) ≈ 1.585 bits of attention per query window. When cumulative γ exceeds C, queries return 429. Agents must be specific, not wasteful. SHOAL is the fleet's shared memory. Agents query it to find relevant patterns, crates, and prior solutions. But unlike a conventional search engine that tries to return as much as possible, SHOAL enforces a conservation law on semantic search: each agent receives a finite attention budget per time window, and queries that would exceed it are rate-limited.

## What It's For
🔮 Conservation-bounded semantic search — the oracle that knows its limits

## Who Would Use It
TypeScript/JavaScript developers in machine learning

## Language / Stack
TypeScript

## Status Assessment
**Mature** — Comprehensive documentation suggesting active, sustained development.

- README size: 17,733 characters, 591 lines
- Code examples: 19 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (19 code blocks)
- Installation/usage instructions provided
- Testing mentioned
- Extensive, detailed README documentation

**Concerns:**
- None immediately apparent from README alone

**Overall:** Well-documented and worth serious evaluation if the domain is relevant.
