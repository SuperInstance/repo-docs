# forgetting-curve

## Intention
**Memories decay. Spaced repetition fights back.**

## How It Works
```
forgetting-curve
│
├── ForgettingCurve            ← Core decay function
│   ├── retrievability(t, S)       R = e^(−t/S)
│   └── time_to_decay(S, target)   When R drops below threshold
│
├── MemoryStrength             ← Memory stability tracker
│   ├── new(initial)               Start with initial stability
│   ├── rehearse(factor)           Boost: S *= factor
│   ├── decay(factor)              Reduce: S *= factor
│   └── default_initial()          1.0
│
├── Quality (enum)             ← Recal

## What It's For
In 1885, Hermann Ebbinghaus conducted the first scientific study of memory. He discovered that **retention follows an exponential decay curve** — without reinforcement, memories fade predictably:

```
Retention %
100 │╲
    │ ╲
    │  ╲
 80 │   ╲
    │    ╲
    │     ╲
 60 │      ╲
    │       ╲
    │        ╲
 40 │         ╲───────
    │                 ────────
 20 │                         ────

## Who Would Use It
```bash
cargo add forgetting-curve
```

Or add to your `Cargo.toml`:

```toml
[dependencies]
forgetting-curve = "0.1"
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (330 line README).

## Honest Assessment
Well-documented (330 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/forgetting-curve](https://github.com/SuperInstance/forgetting-curve)*
