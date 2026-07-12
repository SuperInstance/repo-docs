# b-tree-rs

**Cluster:** maritime  
**Language:** Rust  
**Source:** [SuperInstance/b-tree-rs](https://github.com/SuperInstance/b-tree-rs)

## Intention

B-tree of order t with node splitting, deletion via merge/borrow, search, and range queries

## How It Works

### Insertion

1. Search from root to find the correct leaf.
2. If the leaf has room (`< 2t-1` keys), insert in sorted position.
3. If the leaf is full, **split** it: the median key moves up to the parent, and the right half becomes a new sibling. If the parent is also full, split recursively.
4. If the root splits, a new root is created — the tree grows by one level.

The implementation uses the **proactive split** strategy: when descending for insertion, if a child is full, split it *before* entering it. This guarantees no upward propagation is needed (single-pass insertion).

### Deletion



## What It's For

B-tree of order t with node splitting, deletion via merge/borrow, search, and range queries

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (130 lines, 6849 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# b-tree-rs

[![crates.io](https://img.shields.io/crates/v/b-tree-rs.svg)](https://crates.io/crates/b-tree-rs)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

B-tree with configurable minimum degree, supporting split/merge, range queries, and all CLRS deletion cases.

## The Problem

You need an ordered map that stays balanced under arbitrary insertions and deletions, with good cache behavior. Binary trees (AVL, red-black) suffer from poor locality — each node holds one key and two pointers, meaning a lookup touches a new cache line at every level. For disk-backed or memory-bound workloads, you want wider nodes that pack multiple keys together.

## The Insight

A B-tree of minimum degree `t` stores between `t-1` and `2t-1` keys per node (except the root). Each node has between `t` and `2t` children. This means:

1. **Shallow trees.** A B-tree with `t=100` stores millions of keys in height 3-4. Fewer levels = fewer pointer dereferences.
2. **Cache-friendly.** Keys within a node are contiguous in memory. A binary search within a node stays in the same cache line.
3. **Balance maintained by structure.** All leaves are at the same depth. No per-node balance factors or color bits.

The cost: nodes can be partially empty (as few as `t-1` keys), and insertion/deletion require careful splitting and merging to maintain the invariant.

## How It Works

### Insertion

1. Search from root to find the correct leaf.
2. If the leaf has room (`< 2t-1` keys), insert in sorted position.
3. If the leaf is full, **split** it: the median key moves up to the parent, and the right half becomes a new sibling. If the parent is also full, split recursively.
4. If the root splits, a new root is created — the tree grows by one level.

The implementation uses the **proactive split** strategy: when descending for insertion, if a child is full, split it *before* entering it. This guarantees no upward propagation is needed (single-pass insertion).

### Deletion

Deletion is the complex part. The CLRS algorithm handles several cases:

1. **Key in a leaf with > t-1 keys:** Simply remove it.
2. **Key in an internal node:** Replace with predecessor (rightmost of left subtree) or successor (leftmost of right subtree), then delete recursively.
3. **Key in a subtree whose root has only t-1 keys:** First ensure the child has at least `t` keys by:
   - **Borrowing** from an adjacent sibling (rotate through parent), or
   - **Merging** with a sibling (combining with parent separator key)
4. If the root ends up empty after a merge, its single child becomes the new root — the tree shrinks.

### Range Query

In-order traversal with pruning: at each node, recurse into child `i` only if `node.keys[i]` could be in `[low, high]`. This skips entire subtrees that fall outside the range.

## Usage

```rust
use b_tree_rs::BTree;

let mut tree = BTree::new(3);  // minimum degree t=3, each node holds 2..5 keys

// Insert — returns false for duplicates
assert!(tree.inser
```
