# exocortex-wasm-runtime

## Intention
A minimal C implementation of the TAP (Think-Act-Predict) protocol for WASM targets. Zero heap allocation, fixed-size buffers only.

## How It Works
- Fixed-size ring buffers (no malloc/free)
- Deterministic behavior suitable for WASM sandbox
- All state is static — no global heap usage

## What It's For
Minimal C TAP protocol for WASM - zero heap allocation

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
C

## Status Assessment
Documented with code examples and API references (35 line README).

## Honest Assessment
Minimal documentation (35 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/exocortex-wasm-runtime](https://github.com/SuperInstance/exocortex-wasm-runtime)*
