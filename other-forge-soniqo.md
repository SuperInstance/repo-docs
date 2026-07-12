# forge-soniqo

## Intention
Audio decomposition for Plato agents. Part of the **forge-flux** ecosystem.

## How It Works
1. **Ingest**: Raw audio (WAV files, streamed samples) enters the pipeline
2. **Decompose**: `forge-soniqo` splits into chunks with spectral metadata
3. **Store**: Audio tiles go into `forge-memory` for persistence
4. **Query**: Agents can search by spectral characteristics (e.g., "find loud segments")

## What It's For
- **Chunking** — split audio into fixed-duration tiles (e.g., 100ms chunks)
- **Spectral features** — peak frequency, RMS energy, zero-crossing rate per chunk
- **WAV parsing** — built-in 16-bit PCM WAV decoder
- **Reassembly** — merge tiles back into a continuous sample buffer
- **Zero dependencies** — pure Rust, no audio frameworks

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (56 line README).

## Honest Assessment
Has documentation (56 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/forge-soniqo](https://github.com/SuperInstance/forge-soniqo)*
