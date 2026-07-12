# c-ternary

**Cluster:** constraint-theory  
**Language:** C  
**Source:** [SuperInstance/c-ternary](https://github.com/SuperInstance/c-ternary)

## Intention

Minimal C99 header-only library for ternary logic: trit type, conviction mapping, Leminal Zone deadband, AND/OR/NOT/XOR/implication gates

## How It Works

**c-ternary.h** is a minimal, zero-dependency, header-only C99 library

## What It's For

Minimal C99 header-only library for ternary logic: trit type, conviction mapping, Leminal Zone deadband, AND/OR/NOT/XOR/implication gates

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

C — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (150 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# c-ternary.h — C99 Ternary Logic Header Library

**c-ternary.h** is a minimal, zero-dependency, header-only C99 library
for ternary logic — the foundation of the Hybrid Manifold's ternary
ecosystem.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## What is Ternary Logic?

Classical Boolean logic operates on two values: **false (0)** and **true (1)**.
Ternary logic adds a third state — the **Leminal Zone (0)** — representing
uncertainty, neutrality, or "unknown." This maps naturally to systems like
conviction-based reasoning where a belief may be negative, neutral, or
positive.

| Value | Trit | Meaning |
|-------|------|---------|
| -1    | NEG  | Negative / False / Down |
|  0    | ZRO  | Neutral / Unknown / Leminal Zone |
| +1    | POS  | Positive / True / Up |

## API Overview

### Types

```c
typedef int8_t ct_trit_t;

#define CT_TRIT_NEG  ((ct_trit_t)-1)
#define CT_TRIT_ZERO ((ct_trit_t) 0)
#define CT_TRIT_POS  ((ct_trit_t)+1)
```

### Core Functions

| Function | Description |
|----------|-------------|
| `ct_conviction_to_trit()` | Map conviction ∈ [0,1] → trit with Leminal Zone deadband |
| `ct_trit_to_conviction()` | Map trit back to representative conviction |
| `ct_not(t)` | Ternary NOT (invert: -1↔+1, 0 stays 0) |
| `ct_and(a, b)` | Ternary AND (minimum / pessimistic) |
| `ct_or(a, b)` | Ternary OR (maximum / optimistic) |
| `ct_xor(a, b)` | Ternary XOR |
| `ct_implies(a, b)` | Ternary implication (¬a ∨ b) |
| `ct_equals(a, b)` | Check trit equality |

### Utility Functions

| Function | Description |
|----------|-------------|
| `ct_to_char(t)` | Single-char representation: `-`, `0`, `+` |
| `ct_to_str(t, buf)` | 3-letter string: `NEG`, `ZRO`, `POS` |
| `ct_from_char(c)` | Parse char to trit |
| `ct_from_int(v)` | Clamp int to valid trit range |

## Quick Start

### Single-File Example

```c
#define C_TERNARY_IMPL
#include "c-ternary.h"
#include <stdio.h>

int main(void)
{
    /* Map a conviction to a trit */
    double conviction = 0.85;         /* strong positive belief */
    ct_trit_t t = ct_conviction_to_trit(conviction);
    printf("conviction=%.2f → trit=%s
", conviction, (char[4]){0}, ct_to_str(t, (char[4]){0}));

    /* Ternary logic gates */
    ct_trit_t a = CT_TRIT_POS;
    ct_trit_t b = CT_TRIT_ZERO;

    printf("  NOT %s = %s
",  (char[4]){0}, ct_to_str(ct_not(a), (char[4]){0}));
    printf("  %s AND %s = %s
", (char[4]){0}, ct_to_str(ct_and(a, b), (char[4]){0}));
    printf("  %s OR %s = %s
",  (char[4]){0}, ct_to_str(ct_or(a, b), (char[4]){0}));

    /* Truth-table print */
    printf("
Ternary AND truth table:
");
    printf("    | -1   0  +1
");
    printf("----+-----------
");
    for (ct_trit_t row = CT_TRIT_NEG; row <= CT_TRIT_POS; row++)
    {
        printf(" %s |", (char[4]){0}); ct_to_str(row, (char[4]){0}); printf(" ");
        for (ct_trit_t col = CT_TRIT_NEG; col <= CT_TRIT_POS; col++)
        {
            printf(" %s", (char[4]){0}); ct_to_str(ct_and(row, col), (char[4
```
