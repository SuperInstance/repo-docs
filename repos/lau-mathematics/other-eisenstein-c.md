# eisenstein-c

## Intention
**The same exact hex arithmetic as the Rust crate, compiled to ~1KB of `.text`.**

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- **E12** — two `int32_t`s, same representation as the Rust crate
- **Norm** — `a² - ab + b²`, no sqrt, no float, no libm
- **60° rotation** — `(-b, a - b)`, two subtractions and a negation
- **D₆ symmetry** — all six rotations
- **Addition, multiplication, negation, conjugate**

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
C

## Status Assessment
Has some documentation (43 lines).

## Honest Assessment
Minimal documentation (43 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/eisenstein-c](https://github.com/SuperInstance/eisenstein-c)*
