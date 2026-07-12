# allocator-rs

**Cluster:** cs-implementations  
**Language:** Not specified  
**Source:** [SuperInstance/allocator-rs](https://github.com/SuperInstance/allocator-rs)

## Intention

Memory allocation strategies - Pool allocators, arena allocators, custom allocators

## How It Works

### Pool Allocator

A pool allocator manages $N$ fixed-size slots of size $S$. The implementation uses a **free list** — a singly-linked list of available slots. Initially all $N$ slots are linked. Allocation pops the head of the free list ($O(1)$). Deallocation pushes the slot back onto the head ($O(1)$).

[code]

Memory overhead: 1 pointer per free slot (typically 8 bytes on 64-bit). The total pool size is $N \times S$ bytes, allocated as a single contiguous block. There is no per-allocation metadata header, unlike `malloc` which stores size/alignment prefixes.

### Arena Allocator

An arena

## What It's For

Memory allocation strategies - Pool allocators, arena allocators, custom allocators

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Unknown — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (113 lines, 5851 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# allocator-rs — Custom Memory Allocation Strategies for Rust

**allocator-rs** implements three families of custom memory allocators — **pool allocators**, **arena allocators**, and **bump allocators** — that provide deterministic allocation patterns with $O(1)$ allocation/deallocation and zero fragmentation, unlike the general-purpose system allocator (jemalloc/mimalloc) which optimizes for average-case throughput at the cost of worst-case latency and memory overhead.

## Why It Matters

Real-time systems, game engines, and high-frequency trading cannot tolerate the latency spikes caused by general-purpose allocator behavior: coalescing, splitting, and sbrk/mmap calls introduce unpredictable pauses. A **pool allocator** pre-allocates a fixed block of same-sized slots so that `alloc()` and `dealloc()` are pointer-bumps with no bookkeeping — $O(1)$ worst-case, not amortized. **Arena allocators** batch all allocations into a single contiguous region and free the entire arena at once, eliminating per-allocation free overhead entirely. These patterns are essential in request-response pipelines (allocate per-request, free per-request) and in embedded systems where `malloc` may not even be linked.

## How It Works

### Pool Allocator

A pool allocator manages $N$ fixed-size slots of size $S$. The implementation uses a **free list** — a singly-linked list of available slots. Initially all $N$ slots are linked. Allocation pops the head of the free list ($O(1)$). Deallocation pushes the slot back onto the head ($O(1)$).

```
alloc():  ptr = free_list_head; free_list_head = free_list_head->next; return ptr;
dealloc(p): p->next = free_list_head; free_list_head = p;
```

Memory overhead: 1 pointer per free slot (typically 8 bytes on 64-bit). The total pool size is $N \times S$ bytes, allocated as a single contiguous block. There is no per-allocation metadata header, unlike `malloc` which stores size/alignment prefixes.

### Arena Allocator

An arena (bump allocator) maintains a single `current` pointer into a pre-allocated buffer of size $B$. Allocation advances the pointer:

```
alloc(size, align): ptr = align_up(current, align);
                    current = ptr + size;
                    return ptr;
```

This is $O(1)$ with zero bookkeeping. Deallocation is a no-op — the entire arena is freed at once via `arena.reset()` which sets `current = base`. The trade-off: individual allocations cannot be freed. The memory efficiency is optimal: the only waste is alignment padding (at most `align - 1` bytes per allocation).

### Fragmentation Analysis

- **Pool allocator**: Zero external fragmentation (all slots are the same size). Internal fragmentation = $S - \text{requested\_size}$ if the slot is larger than needed.
- **Arena allocator**: Zero fragmentation by definition — everything is contiguous and freed together.
- **System malloc**: External fragmentation can reach 50%+ under adversarial workloads (Zygote-style allocation patterns).

### Comparison

| All
```
