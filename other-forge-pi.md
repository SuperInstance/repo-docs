# forge-pi

## Intention
General-purpose agent runtime at the edge. The orchestrator that bridges all SuperInstance systems.

## How It Works
```
                      ┌─────────────────────┐
                      │    USER / CLIENT    │
                      └──────────┬──────────┘
                                 │ POST /forge
                                 ▼
                      ┌─────────────────────┐
                      │      forge-pi       │
                      │  Cloudflare Worker  │
                      │                     │
                      │  1. Embed query     │
                      │  2. Vector search   │

## What It's For
forge-pi is the central nervous system of the SuperInstance fleet. It sits at the edge and handles four things:

1. **Dispatch** — Route natural-language queries to the right agent
2. **Discover** — Find relevant capabilities across 543+ crates via semantic search
3. **Compose** — Chain multiple capabilities into pipelines
4. **Offload** — Delegate heavy compute to ephemeral codespace workers

Eve

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
TypeScript

## Status Assessment
Documented with code examples and API references (318 line README).

## Honest Assessment
Well-documented (318 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/forge-pi](https://github.com/SuperInstance/forge-pi)*
