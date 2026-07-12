# gc-pid-bridge

## Intention
A thin Rust binary wrapping `ternary-pid` for use by the host-level GC system. **v1.2.0** replaces the old bash `bc` PID math with an optimized ARM64 binary tuned for Neoverse-N1.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Rust bridge between gc-intelligent.sh and ternary-pid — host-level disk PID controller

## Who Would Use It
```bash
cargo install --git https://github.com/SuperInstance/gc-pid-bridge
```

Or build locally:

```bash
cd gc-pid-bridge
RUSTFLAGS="-C target-cpu=neoverse-n1" cargo build --release
sudo cp target/release/gc-pid-bridge /usr/local/bin/
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (76 line README).

## Honest Assessment
Has documentation (76 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/gc-pid-bridge](https://github.com/SuperInstance/gc-pid-bridge)*
