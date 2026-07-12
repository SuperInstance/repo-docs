# strategy-transfer

## Intention
Testing whether ternary strategies transfer across domains

## How It Works
**Strategy transfer** tests whether ternary strategies — sequences of {-1, 0, +1} choices optimized in one domain — generalize to different domains. This crate runs controlled transfer experiments: train a strategy on a source domain, apply it to a target domain, and compare against training from scratch. The key finding: cross-domain transfer is **neutral** — no positive or negative transfer.

The README includes code examples and API documentation.

Key topics: ternary math, fleet orchestration

## What It's For
Managing distributed fleet operations.

## Who Would Use It
Rust developers, (primarily SuperInstance ecosystem users)

## Language / Stack
- **Language:** Rust
- **Dependencies:** Standard
- **Published:** GitHub only

## Status Assessment
Proof of concept — experimental

## Honest Assessment
No test count mentioned in README — implementation depth unclear. Explicitly labeled as proof of concept or experiment — not production-ready. Not published to any package registry — GitHub-only. Lacks installation instructions — may be difficult to get started.

## README Length
5316 characters
