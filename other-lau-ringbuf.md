# lau-ringbuf

## Intention

Low-level lock-free-style circular buffer for real-time vibe data streaming. Single-threaded with the API shape of a real-time audio buffer.

## How It Works

```rust
use lau_ringbuf::{RingBuf, VibeRingBuf, VibeStream};
// Basic ring buffer
let mut buf: RingBuf<i32, 16> = RingBuf::new();
buf.write(42);
assert_eq!(buf.read(), Some(42));
// Vibe sample buffer
let mut vibes: VibeRingBuf<256> = VibeRingBuf::new();
vibes.write_sample(0.75);
println!("rms: {}", vibes.rms());
// Streaming analysis with sliding window
let mut stream: VibeStream<1024, 64> = VibeStream::new();
stream.push(1.0);
let stats = stream.window_stats();
let anomaly = stream.detect_anomaly(2.0);

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. Low-level lock-free-style circular buffer for real-time vibe data streaming. Single-threaded with the API shape of a real-time audio buffer.

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (25 lines), includes examples.

- README length: 33 lines, 1055 characters
- Documented sections: Features, Usage

## Honest Assessment

Part of the sprawling Lau/PLATO ecosystem. The README covers basics but the project is one of many math/computation crates in this organization. The breadth of repos in SuperInstance (hundreds) raises questions about depth vs. breadth — many appear to be auto-generated or lightly documented. **This crate likely works as a component but standalone value is limited without the broader ecosystem.**
