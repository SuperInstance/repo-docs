# ec2mud

## Intention
**A browser-based MUD game engine with web dashboard, powered by Socket.IO.**

## How It Works
```
Browser (React)
  ↕ Socket.IO (port 3006)
┌──────────────────┐
│ standalone-mud.ts │ ← Built-in game server (no deps)
│   OR              │
│ ws-bridge.ts      │ ← Proxy to holodeck-core (Rust, port 7778)
└──────────────────┘
  ↕ Raw TCP
holodeck-core (Rust)
```

Two modes:
1. **Standalone** — `pnpm mud` runs the full MUD in-process. No external deps. 6 rooms, NPCs, multi-player chat, inventory, combat stats. Ships in the box.
2. **Bridged** — `pnpm bridge` proxies Socket.IO ↔ holodeck-core'

## What It's For
- **`/game`** — Live MUD terminal. Login, explore rooms, chat, take items, talk to NPCs.
- **`/`** — Fleet dashboard. Module stats, fleet overview.
- **`/catalog`** — Module browser with search/filter.
- **`/settings`** — API key management + system config.

## Who Would Use It
pnpm install

## Language / Stack
TypeScript

## Status Assessment
Has some documentation (95 lines).

## Honest Assessment
Has documentation (95 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/ec2mud](https://github.com/SuperInstance/ec2mud)*
