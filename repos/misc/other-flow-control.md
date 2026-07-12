# flow-control

## Intention
Flow control with sliding window, credit-based, and rate-limiting algorithms.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- **Sliding Window** — Sequence-numbered window with send/ack tracking
- **Credit Manager** — Per-stream credit allocation and consumption
- **Rate Limiter** — Token bucket and leaky bucket rate limiting
- **Buffer Manager** — Circular buffer with watermarks and backpressure signals
- **Flow Scheduler** — Priority-based weighted fair queueing
- Zero external dependencies — pure `std`

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (28 line README).

## Honest Assessment
Minimal documentation (28 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/flow-control](https://github.com/SuperInstance/flow-control)*
