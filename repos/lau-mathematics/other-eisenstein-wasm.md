# eisenstein-wasm

## Intention
**Same exact Eisenstein integer arithmetic, compiled for the browser and Node.js.**

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Floating-point hex coordinates in JavaScript drift after repeated operations — JS has no control over FPU rounding modes across browsers. Eisenstein integers don't have that problem because the arithmetic is integer-only. The WASM binary gives you exact, deterministic hex math that behaves identically on every browser, every device, every time.

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Has some documentation (40 lines).

## Honest Assessment
Minimal documentation (40 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/eisenstein-wasm](https://github.com/SuperInstance/eisenstein-wasm)*
