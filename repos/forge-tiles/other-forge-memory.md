# forge-memory

## Intention
External tile memory store for Plato agents. Part of the **forge-flux** ecosystem.

## How It Works
1. **Ingest**: Raw content gets decomposed by `forge-code`, `forge-soniqo`, or similar decomposers
2. **Store**: Resulting tiles are persisted in `forge-memory` with kind and source indices
3. **Retrieve**: Downstream agents query tiles by kind, source, or content
4. **Search**: Agents can semantically search the tile space for relevant context
5. **Compact**: Periodic garbage collection removes orphaned tiles

## What It's For
- **Embedded storage** via sled — zero network dependencies, no external database
- **Bincode serialization** — fast, compact binary encoding for tiles
- **Content search** — full-text search with optional kind filtering and embedding similarity
- **Index-based queries** — look up tiles by source UUID or kind
- **Compact** — garbage-collect orphaned tiles whose

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (53 line README).

## Honest Assessment
Has documentation (53 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/forge-memory](https://github.com/SuperInstance/forge-memory)*
