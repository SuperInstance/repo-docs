# fastloop-guard

## Intention
`fastloop-guard` is a high-performance semantic cache daemon for LLM query responses. It uses a **three-gate lookup** — exact BLAKE2b fingerprint → fuzzy MinHash similarity → miss — to dramatically reduce redundant LLM API calls. Built as a Unix socket server with async Tokio runtime, it provides sub-millisecond cache lookups with configurable TTL and LRU eviction.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
LLM inference is expensive: $0.01–$0.06 per 1K tokens for frontier models. In production agent systems, 30–60% of queries are near-duplicates — rephrased questions, case variants, trivial whitespace differences. Without caching, you're paying for the same answer repeatedly.

FastLoop Guard intercepts the query stream:

| Gate | Match Type | Example | Cost Saving |
|---|---|---|---|
| 1: Exact | BL

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (182 line README).

## Honest Assessment
Moderately documented (182 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/fastloop-guard](https://github.com/SuperInstance/fastloop-guard)*
