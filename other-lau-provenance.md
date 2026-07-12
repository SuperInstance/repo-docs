# lau-provenance

## Intention

> Every decision leaves a trail. This crate makes sure that trail is recorded, queryable, and rewindable.

## How It Works

This crate provides three things:
| Component | Purpose |
|---|---|
| **`ProvenanceEntry`** | A single, richly-structured decision record (intent, model, alternatives, tradeoffs, debt, files changed, test status, conservation cost). |
| **`ProvenanceLedger`** | A searchable, serialisable collection of entries with time-range queries, commit/room lookups, full-text search, and aggregate statistics. |
| **`ProvenanceHook`** | Pre-commit enforcement — validates that files being committed have a corresponding provenance entry with all required fields. |
Every entry renders to and parses from a `.logic_provenance.md` Markdown format, so provenance lives alongside the code in human-readable form.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. > Every decision leaves a trail. This crate makes sure that trail is recorded, queryable, and rewindable.

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: SUBSTANTIAL**

Detailed README (215 lines), mentions tests, includes examples.

- README length: 309 lines, 9242 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

This is one of the more thoroughly documented repos in the collection. The README is extensive (309 lines) with substantial detail. The concepts are clearly articulated and the implementation appears serious. However, context matters: SuperInstance has spawned hundreds of repositories, and even the well-documented ones exist within a self-referential ecosystem. **Strong documentation and evident effort, but whether the ecosystem achieves real-world utility beyond its own internal consistency remains an open question.**
