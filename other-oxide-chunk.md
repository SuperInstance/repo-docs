# oxide-chunk

## Intention
GPU memory chunk management with ternary allocation status. Buddy splitting, coalescing, defragmentation, utilization stats.

## How It Works
Oxide Chunk provides GPU memory chunk management with ternary allocation status — +1 (Allocated), 0 (Fragmented), -1 (Free) — featuring buddy-style splitting and merging, automatic coalescing on deallocation, defragmentation, and utilization statistics. GPU memory is a scarce resource: a typical GPU has 8-24GB of VRAM shared by dozens of kernels. Without proper memory management, fragmentation — where free memory is split into many small, non-contiguous blocks — makes it impossible to allocate large buffers even when total free memory is sufficient. Oxide Chunk implements the buddy allocator algorithm (used by Linux's old zoned allocator and FreeBSD's uma zone allocator) with ternary status tracking. The buddy system guarantees that any allocation request that fits within total free memory

## What It's For
GPU memory chunk management with ternary allocation status. Buddy splitting, coalescing, defragmentation, utilization stats.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 6,221 characters, 164 lines
- Code examples: 7 blocks
- Installation instructions: yes
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (7 code blocks)
- Installation/usage instructions provided
- Solid README with good coverage

**Concerns:**
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
