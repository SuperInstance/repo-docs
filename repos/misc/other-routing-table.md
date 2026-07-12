# routing-table

## Intention
Rust crate: routing-table

## How It Works
Routing table with prefix matching (trie-based), path selection, and metric computation. A zero-dependency Rust library for building and querying IPv4 routing tables with longest prefix match. - Prefix — CIDR parsing, containment checks, supernet/subnet relationships - Routing Trie — Binary trie for O(32) longest prefix match lookups - Route — Routing entries with next-hop, interface, and metric tracking - Metric — Composite metric computation with admin distance and OSPF-style costs - Route Selector — Best-path selection among multiple candidate routes - Zero external dependencies — pure std

## What It's For
Rust crate: routing-table

## Who Would Use It
Rust developers

## Language / Stack
Rust

## Status Assessment
**Developing** — Moderate documentation with some structure and examples.

- README size: 1,004 characters, 33 lines
- Code examples: 1 blocks
- Installation instructions: yes
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: no

## Honest Assessment

**Strengths:**
- Installation/usage instructions provided

**Concerns:**
- None immediately apparent from README alone

**Overall:** Early but potentially interesting — read the source to verify.
