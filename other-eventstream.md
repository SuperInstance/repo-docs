# eventstream

## Intention
<p align="center"> <strong>Kafka-inspired event streaming for the Cocapn Fleet</strong><br/> Lightweight &middot; High-throughput &middot; WebAssembly-ready &middot; Rust-native </p>

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
**eventstream** provides a Kafka-inspired event streaming infrastructure designed for the Cocapn Fleet's real-time communication needs. The architecture supports topics with configurable partitions, append-only log segments with automatic rotation, consumer groups with offset tracking, and multiple compression strategies (None, Gzip, Snappy, Lz4, Zstd). The system is built with a dual-storage back

## Who Would Use It
Add to your `Cargo.toml`:

```toml
[dependencies]
eventstream = "0.1"
tokio = { version = "1", features = ["full"] }
serde = { version = "1", features = ["derive"] }
serde_json = "1"
```

## Language / Stack
Not specified

## Status Assessment
Has substantial documentation (340 lines).

## Honest Assessment
Moderately documented (340 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/eventstream](https://github.com/SuperInstance/eventstream)*
