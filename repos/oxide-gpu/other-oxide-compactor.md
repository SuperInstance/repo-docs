# oxide-compactor

## Intention
Background compaction for GPU data structures with ternary compaction state

## How It Works
Background compaction for GPU data structures with ternary compaction state. A Rust library that implements merge-sort compaction of sorted runs in GPU memory, with a scheduler that uses a three-valued (ternary) trigger to decide which segments need attention — and which are healthy enough to skip. GPU workloads that maintain sorted data structures (columnar stores, LSM-tree-style indexes, spatial indexes) accumulate fragmentation over time as records are inserted and deleted. Dead space inside GPU segments wastes VRAM, degrades memory locality, and increases the cost of scans.

## What It's For
Background compaction for GPU data structures with ternary compaction state

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 7,007 characters, 189 lines
- Code examples: 5 blocks
- Installation instructions: no
- Testing mentioned: yes
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (5 code blocks)
- Testing mentioned
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
