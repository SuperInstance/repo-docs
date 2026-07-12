# oxide-ring

## Intention
Ring buffer for GPU event logging with ternary overflow state. Lossless until overflow, then oldest dropped. Query by kind.

## How It Works
Oxide Ring is a ring buffer for GPU event logging with ternary overflow state — +1 (Normal), 0 (NearFull), -1 (Overflowed) — providing lossless event recording until capacity is exceeded, then graceful degradation with oldest-event dropping and overflow tracking. GPU kernels generate thousands of events per millisecond: kernel launches, memory transfers, synchronization points, and errors. Logging all of them requires a buffer that can absorb burst writes without blocking the GPU. Oxide Ring provides this: a bounded ring buffer that accepts events at O(1) write cost, never blocks (overwrites oldest on overflow), and exposes a ternary state — Normal, NearFull, or Overflowed — so consumers know whether they're reading complete or potentially-gapped history. The NearFull state (configurable t

## What It's For
Ring buffer for GPU event logging with ternary overflow state. Lossless until overflow, then oldest dropped. Query by kind.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 5,095 characters, 138 lines
- Code examples: 7 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (7 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
