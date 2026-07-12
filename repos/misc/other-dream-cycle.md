# dream-cycle

## Intention
**When the cortex sleeps, it dreams. Consolidation, creativity, anomaly detection.**

## How It Works
```
dream-cycle
│
├── DreamPhase (enum)          ← Sleep stage
│   ├── NremLight                  Shallow scanning
│   ├── NremDeep                   Deep consolidation
│   └── Rem                        Creative recombination
│
├── DreamState                 ← Current dream state
│   ├── new()                      Start at NREM Light, depth 0
│   ├── advance()                  Phase transition: Light→Deep→REM→Light
│   └── is_idle_threshold(events)  Should the agent start dreaming?
│
├── Memory

## What It's For
The human brain doesn't process information only during wakefulness. During sleep, it cycles through distinct phases — each with a specific cognitive function:

```
┌─────────────────────────────────────────────────────────┐
│              90-minute Sleep Cycle                       │
│                                                         │
│  NREM Light ──► NREM Deep ──► REM ──► NREM Light ──►

## Who Would Use It
```bash
cargo add dream-cycle
```

Or add to your `Cargo.toml`:

```toml
[dependencies]
dream-cycle = "0.1"
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (278 line README).

## Honest Assessment
Well-documented (278 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/dream-cycle](https://github.com/SuperInstance/dream-cycle)*
