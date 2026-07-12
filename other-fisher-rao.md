# fisher-rao

## Intention
**Fisher-Rao metric, Cramér-Rao bound, information matrix, and Rao distance for parametric statistical families.**

## How It Works
```
                    ┌─────────────────────────────┐
                    │        fisher-rao           │
                    │                             │
                    │  ┌───────────────────────┐  │
                    │  │       metric          │  │
                    │  │  FisherRaoMetric      │◄─┼── Entry point: compute gᵢⱼ(θ)
                    │  │  gᵢⱼ = E[∂ᵢℓ · ∂ⱼℓ] │  │
                    │  └───────────┬───────────┘  │
                    │              │               │

## What It's For
See intention above.

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Has substantial documentation (393 lines).

## Honest Assessment
Moderately documented (393 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/fisher-rao](https://github.com/SuperInstance/fisher-rao)*
