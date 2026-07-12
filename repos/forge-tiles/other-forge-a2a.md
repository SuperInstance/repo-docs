# forge-a2a

## Intention
A2A (agent-to-agent) messaging for **ForgeFlux** tile pipelines.

## How It Works
- **`ForgeMessage`** — A single message on the bus, carrying a type, payload, sender, and timestamp.
- **`ForgeMsgType`** — Enum of event types (`PipelineStarted`, `StageCompleted`, `TileProduced`, `TransformRequest`, etc.).
- **`ForgePayload`** — Tagged union for status, tile, error, transform, and subscription data.
- **`ForgeBus`** — In-process publish/subscribe bus with filter-based routing and history.
- **`ForgeSubscriber`** — A named subscriber with an optional filter list.
- **`ForgeMess

## What It's For
A2A messaging for ForgeFlux tile pipelines

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (47 line README).

## Honest Assessment
Minimal documentation (47 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/forge-a2a](https://github.com/SuperInstance/forge-a2a)*
