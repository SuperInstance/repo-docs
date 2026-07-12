# penrose-memory

## Intention
Aperiodic memory palace for AI agents. Navigate memories by distance + direction on a Penrose floor.

## How It Works
Aperiodic memory palace for AI agents. Navigate memories by distance + direction on a Penrose floor. 1. Project: Embeddings → 2D Penrose coordinates via golden-ratio hashing 2. Store: Place memories on the floor at projected coordinates 3. Recall: Dead-reckon from query toward stored memories 4. Navigate: Walk from any tile by distance + heading 5. Consolidate: Merge nearby memories using golden hierarchy (φ^k) The Fibonacci word determines tile bits (thick:thin → 1/φ). Matching rules verify valid positions. 3-coloring enables sharding.

## What It's For
Aperiodic memory palace for AI agents. Navigate memories by distance + direction on a Penrose floor.

## Who Would Use It
Rust developers in machine learning

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 3,993 characters, 117 lines
- Code examples: 4 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: no

## Honest Assessment

**Strengths:**
- Code examples present (4 code blocks)
- Installation/usage instructions provided
- Testing mentioned
- Creative/novel approach

**Concerns:**
- None immediately apparent from README alone

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
