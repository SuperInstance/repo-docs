# ecosystem-graph

## Intention
**SuperInstance crate dependency analyzer.** Maps the ecosystem's interconnections, finds orphans, identifies foundational libraries, and powers visualization.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
A crate ecosystem with 1,100+ crates needs map. Without dependency analysis, you can't answer:
- Which crates are **foundational** (many dependents, few dependencies)?
- Which crates are **orphaned** (nobody depends on them)?
- Where are the **clusters** — tightly coupled subgraphs?
- What's the **dependency path** from crate A to crate B?

Ecosystem Graph answers these with D1-backed graph querie

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
TypeScript

## Status Assessment
Documented with code examples and API references (123 line README).

## Honest Assessment
Moderately documented (123 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/ecosystem-graph](https://github.com/SuperInstance/ecosystem-graph)*
