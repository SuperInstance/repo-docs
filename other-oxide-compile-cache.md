# oxide-compile-cache

## Intention
Content-addressed compilation cache for GPU kernels. Hash source → lookup PTX → skip recompile. LRU eviction, TTL, hit rate tracking.

## How It Works
Content-addressed compilation cache for GPU kernels with LRU eviction. Kernel compilation is slow. A CUDA kernel that takes 50 μs to execute might take 500 ms to compile — a 10,000× overhead. When you're running the same kernels repeatedly (which is most GPU workloads), recompilation is pure waste. The fix is simple in concept: hash the source, check if you've already compiled it, return the cached PTX. The engineering challenge is doing this correctly — cache invalidation, eviction policy, hit rate tracking, and measuring actual time savings. The content-addressed approach means cache keys are deterministic hashes of the source code. Same source → same hash → same cached PTX. No invalidation needed when the source changes — it produces a different hash and gets a fresh compilation. LRU ev

## What It's For
Content-addressed compilation cache for GPU kernels. Hash source → lookup PTX → skip recompile. LRU eviction, TTL, hit rate tracking.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 6,191 characters, 133 lines
- Code examples: 3 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: no
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (3 code blocks)
- Solid README with good coverage

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
