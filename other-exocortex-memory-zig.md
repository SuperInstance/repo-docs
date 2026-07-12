# exocortex-memory-zig

## Intention
**A comptime-verified semantic memory store written in Zig.**

## How It Works
```
┌─────────────────────────────────────────────────────────────────────┐
│                     COMPTIME SCHEMA VALIDATION                      │
│                                                                     │
│   validateInsight() ──→ @typeInfo() introspection                  │
│       │                   ├── required fields present?              │
│       │                   ├── field types correct (u64, f64, i64)? │
│       │                   ├── confidence ∈ [0, 1]?

## What It's For
`exocortex-memory-zig` is a memory store for semantic retrieval — the kind of
system you'd use to give an AI agent persistent, queryable memory. It stores
**Insights** (discrete pieces of knowledge), each annotated with:

- **Ternary embedding vectors** — compact {-1, 0, +1} discretized representations
- **Tags** — categorical metadata for filtering
- **Confidence** — uncertainty quantification [0

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Zig

## Status Assessment
Documented with code examples and API references (874 line README).

## Honest Assessment
Well-documented (874 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/exocortex-memory-zig](https://github.com/SuperInstance/exocortex-memory-zig)*
