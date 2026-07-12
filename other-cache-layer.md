# cache-layer

**Cluster:** cs-ds-algos  
**Language:** Rust  
**Source:** [SuperInstance/cache-layer](https://github.com/SuperInstance/cache-layer)

## Intention

Multi-layer caching system with L1/L2/L3 caches, invalidation, and persistence

## How It Works

cache-layer implements the timeless principle of **memory hierarchy**: data closer to computation is faster to access. The multi-tier design balances speed, size, and cost by automatically managing data placement across storage layers.

[code]

For detailed architecture information, see [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

## What It's For

Multi-layer caching system with L1/L2/L3 caches, invalidation, and persistence

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (267 lines, 7730 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# cache-layer

**Multi-tier caching library for high-performance data access**

Sub-microsecond memory reads, millisecond-scale persistence, automatic tier promotion.

## Overview

cache-layer provides a sophisticated multi-tier caching system that combines three levels of storage hierarchy:

- **L1 Cache (Memory)**: ~100ns reads, 100MB typical capacity
- **L2 Cache (Redis)**: ~1ms reads, 10GB typical capacity, shared across instances
- **L3 Cache (Disk)**: ~10ms reads, 1TB typical capacity, persistent storage

The library automatically manages data movement between tiers, promoting frequently accessed data to faster layers and evicting to slower layers when capacity limits are reached.

## Key Features

### Multi-Tier Architecture
- **Automatic tiering**: Data seamlessly flows between memory, Redis, and disk
- **Intelligent promotion**: Cache hits promote data to faster tiers
- **Configurable eviction**: LRU, LFU, or FIFO policies per tier
- **TTL support**: Time-based expiration for cached items

### Performance
- **Sub-microsecond L1 reads**: ~100ns average latency for memory cache hits
- **High hit rates**: Target >80% L1, >15% L2, <1% overall miss rate
- **Zero-copy**: Rust implementation eliminates unnecessary allocations
- **Lock-free reads**: Concurrent access without blocking

### Developer Experience
- **Simple API**: Three core operations - get, set, delete
- **Type-safe**: Generics support any serializable type
- **Language bindings**: Rust core with Go bindings for easy integration
- **Comprehensive metrics**: Built-in monitoring and observability

## Quick Start

### Installation

**Rust:**
```toml
[dependencies]
cache-layer = "0.1"
```

**Go:**
```bash
go get github.com/equilibrium-tokens/cache-layer-go
```

### Basic Usage

```rust
use cache_layer::{MultiTierCache, MemoryCache, RedisCache, DiskCache};

// Create a multi-tier cache
let cache = MultiTierCache::new()
    .with_l1(MemoryCache::new(100_000_000)?)  // 100MB
    .with_l2(RedisCache::new("redis://localhost:6379")?)
    .with_l3(DiskCache::new("/var/cache/myapp")?)
    .build();

// Store a value
cache.set("user:123", User {
    id: 123,
    name: "Alice".to_string(),
}).await?;

// Retrieve a value (automatically searches L1 → L2 → L3)
if let Some(user) = cache.get(&"user:123").await? {
    println!("User: {}", user.name);
}

// Delete a value across all tiers
cache.delete(&"user:123").await?;
```

### Advanced Usage

```rust
use cache_layer::{MultiTierCache, MemoryCache, EvictionPolicy};
use std::time::Duration;

// Configure with custom eviction policies and TTL
let cache = MultiTierCache::new()
    .with_l1(
        MemoryCache::builder()
            .capacity(200_000_000)  // 200MB
            .eviction_policy(EvictionPolicy::LRU)
            .build()
    )
    .with_ttl(Duration::from_secs(3600))  // 1 hour default TTL
    .with_metrics(true)  // Enable collection of cache metrics
    .build();

// Cache warming
let mut cache_warmed = 0;
for key in preload_keys {
   
```
