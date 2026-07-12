# evolution-ternary-c

## Intention
**Evolution Ternary (C)** is a C library implementing evolutionary algorithms over ternary genomes {-1, 0, +1} — providing genome operations (crossover, mutation), population management, tournament selection, and configurable evolution parameters with a clean C99 API.

## How It Works
**Genome representation:**
```c
typedef struct {
    int  *trits;    // array of {-1, 0, +1}
    size_t length;
} Genome;
```

Each trit takes a full `int` for simplicity and FFI compatibility. A 24-trit genome uses 96 bytes (vs 3 bytes packed), trading memory for speed — array indexing is O(1) without bit manipulation.

**Crossover:**
- **Single-point:** Copy parent A up to point P, parent B from P onward. O(length).
- **Uniform:** For each locus, select from A with probability p, else B. O(len

## What It's For
Binary evolutionary algorithms (genetic algorithms with {0, 1} genomes) are well-studied, but ternary genomes {-1, 0, +1} map naturally to the SuperInstance action space where they encode Avoid, Unknown, and Choose behaviors. This C implementation provides the high-performance computational core for fleet-scale ternary evolution, suitable for embedding in CUDA kernels, microcontrollers, or any env

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
C

## Status Assessment
Documented with code examples and API references (147 line README).

## Honest Assessment
Moderately documented (147 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/evolution-ternary-c](https://github.com/SuperInstance/evolution-ternary-c)*
