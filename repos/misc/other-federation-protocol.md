# federation-protocol

## Intention
Two PLATO instances exchange ONE tile type: agent coupling summaries.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
The coupling summary carries:
- Health signal (is the other fleet alive?)
- Load signal (how many agents?)
- Coherence signal (is the other fleet functioning?)

Three signals are enough to make federation decisions: route work to the healthy fleet, avoid the saturated one, trust the coherent one.

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Not specified

## Status Assessment
Has some documentation (29 lines).

## Honest Assessment
Minimal documentation (29 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/federation-protocol](https://github.com/SuperInstance/federation-protocol)*
