# mux-demux

## Intention

Rust crate: mux-demux

## How It Works

```rust
use mux_demux::{Multiplexer, Demultiplexer, StreamId};
let mut mux = Multiplexer::new(1, 10);
let sid = mux.open_stream().unwrap();
mux.send(sid, b"hello");
let output = mux.drain_output();
let mut demux = Demultiplexer::new(1, 10);
demux.process(&output);
let mut buf = [0u8; 5];
demux.read(sid, &mut buf);
```

## What It's For

Rust crate: mux-demux

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (25 lines), includes examples.

- README length: 35 lines, 1106 characters
- Documented sections: Features, Usage

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
