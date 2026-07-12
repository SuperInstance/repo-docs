# oxide-tombstone

## Intention
Tombstone-based deletion for GPU distributed data with ternary states. Lazy deletion, compaction, purge by watermark.

## How It Works
Oxide Tombstone provides tombstone-based deletion for GPU distributed data with ternary entry states — +1 (alive), 0 (tombstoned), -1 (purged) — implementing lazy deletion, compaction, and garbage collection for concurrent data stores. Distributed key-value stores cannot synchronously delete data that may be replicated across nodes or actively read by concurrent threads. Tombstones solve this: a deleted key is marked as "tombstoned" (invisible to reads) but not physically removed. Later, a compaction pass purges tombstones once all replicas acknowledge the deletion. This is exactly how Cassandra, LevelDB, and RocksDB handle deletion. Oxide Tombstone brings this pattern to GPU memory management with version tracking and ternary lifecycle states. State transitions: Alive → Tombstoned → Purge

## What It's For
Tombstone-based deletion for GPU distributed data with ternary states. Lazy deletion, compaction, purge by watermark.

## Who Would Use It
Rust developers in distributed GPU computing

## Language / Stack
Rust

## Status Assessment
**Active** — Well-documented README with meaningful detail.

- README size: 4,093 characters, 115 lines
- Code examples: 6 blocks
- Installation instructions: no
- Testing mentioned: no
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (6 code blocks)

**Concerns:**
- No clear installation instructions
- One of 30+ oxide-* repos — ecosystem fragmentation risk

**Overall:** Solid foundation; worth investigating if the specific capability is needed.
