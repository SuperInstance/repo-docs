# flux-fracture-c

**Category:** ✅ Constraint/Safety
**Status:** 🟢 Production-oriented
**Language:** C
**README:** 4,702 bytes

## Intention
Single-header C99 fracture-coalesce library — #define FRACTURE_IMPLEMENTATION.

## How It Works
```c
#define FRACTURE_IMPLEMENTATION
#include "flux_fracture.h"
```

Single header — include with `FRACTURE_IMPLEMENTATION` defined in exactly one translation unit.

### Fracture from Edges

```c
frac_edge edges[] = {
    {0, 0}, {0, 1},  // constraint 0 touches dimensions 0 and 1
    {1, 0},          // constraint 1 touches dimension 0
    {2, 2},          // constraint 2 touches dimension 2 (independent)
    {3, 2},          // constraint 3 touches dimension 2
};

frac_result result = frac_fra...

## What It's For
Single-header C99 fracture-coalesce library — #define FRACTURE_IMPLEMENTATION.

## Who Would Use It
Formal methods practitioners and safety-critical systems engineers.

## Honest Assessment
Has code examples. claims 6 tests.
