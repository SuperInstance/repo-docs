# grand-pattern-net

## Intention
Networking layer for the Grand Pattern. Rooms gossip over the network.

## How It Works
```
┌─────────────┐     UDP Multicast     ┌─────────────┐
│  GossipNode │◄──────────────────────►│  GossipNode │
│  (CellGraph)│                        │  (CellGraph)│
└──────┬──────┘                        └──────┬──────┘
       │                                      │
       │ TCP (reliable)                       │ TCP
       ▼                                      ▼
┌──────────────┐                      ┌──────────────┐
│  TcpGossip   │                      │  TcpGossip   │
└──────────────┘

## What It's For
- **UDP Gossip Protocol** — Multicast-based murmur propagation between nodes
- **TCP Transport** — Reliable framed delivery for murmur exchange
- **Peer Discovery** — Multicast announcement and discovery protocol
- **Binary Serialization** — Compact 32-byte murmur encoding, deterministic graph state wire format
- **Distributed Tick Coordination** — All nodes tick, exchange murmurs, integrate
- **Z

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (65 line README).

## Honest Assessment
Has documentation (65 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/grand-pattern-net](https://github.com/SuperInstance/grand-pattern-net)*
