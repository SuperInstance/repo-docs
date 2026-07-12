# avl-tree-rs

**Cluster:** cs-ds-algos  
**Language:** Rust  
**Source:** [SuperInstance/avl-tree-rs](https://github.com/SuperInstance/avl-tree-rs)

## Intention

AVL self-balancing BST with LL/RR/LR/RL rotations, balance factor tracking, insert/delete/contains, and inorder traversal

## How It Works

The tree uses `Option<Box<Node<T>>>` links — a classic owned recursive structure. Each node stores its height, enabling O(1) balance factor computation.

**Insert:** Recursive descent to find the insertion point, then propagate back up, calling `rebalance()` at each ancestor. The rebalance function checks the balance factor and applies the appropriate rotation.

**Delete:** Recursive descent to find the node. Three sub-cases for the found node:
- Leaf → remove directly
- One child → replace with child
- Two children → swap with in-order successor (minimum of right subtree), then delete the suc

## What It's For

AVL self-balancing BST with LL/RR/LR/RL rotations, balance factor tracking, insert/delete/contains, and inorder traversal

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (113 lines, 5883 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# avl-tree-rs

[![crates.io](https://img.shields.io/crates/v/avl-tree-rs.svg)](https://crates.io/crates/avl-tree-rs)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

AVL self-balancing binary search tree in Rust — LL, RR, LR, and RL rotations with guaranteed O(log n) height.

## The Problem

A plain binary search tree degrades to O(n) when keys are inserted in sorted or nearly-sorted order. This happens often in practice: sequential IDs, timestamps, auto-incrementing counters. You need a tree that stays balanced regardless of insertion order, without paying the overhead of a B-tree's wide nodes.

## The Insight

The AVL tree (Adelson-Velsky and Landis, 1962) maintains the invariant: **for every node, the heights of its left and right subtrees differ by at most 1.** When an insertion or deletion violates this invariant (balance factor leaves the range `[-1, 0, 1]`), a local rotation restores it.

There are four cases:
- **LL** (left-left): Left child is left-heavy → single right rotation
- **RR** (right-right): Right child is right-heavy → single left rotation
- **LR** (left-right): Left child is right-heavy → left rotation on left child, then right rotation
- **RL** (right-left): Right child is left-heavy → right rotation on right child, then left rotation

Each rotation is O(1) — just pointer rewiring — and at most one rotation (double rotation counts as two) is needed per level. So rebalancing costs O(log n) total.

## How It Works

The tree uses `Option<Box<Node<T>>>` links — a classic owned recursive structure. Each node stores its height, enabling O(1) balance factor computation.

**Insert:** Recursive descent to find the insertion point, then propagate back up, calling `rebalance()` at each ancestor. The rebalance function checks the balance factor and applies the appropriate rotation.

**Delete:** Recursive descent to find the node. Three sub-cases for the found node:
- Leaf → remove directly
- One child → replace with child
- Two children → swap with in-order successor (minimum of right subtree), then delete the successor

Rebalancing propagates back up the recursion stack. Deletion can trigger rotations at multiple levels (unlike insertion, which triggers at most one).

**Contains:** Iterative descent from root — no recursion needed for lookups.

## Usage

```rust
use avl_tree_rs::AvlTree;  // crate name on crates.io; lib name is avl_tree

let mut tree = AvlTree::new();

// Insert — returns false for duplicates
assert!(tree.insert(5));
assert!(tree.insert(3));
assert!(tree.insert(7));
assert!(!tree.insert(5));  // duplicate, returns false

// Search
assert!(tree.contains(&3));
assert!(!tree.contains(&4));

// Sorted traversal
assert_eq!(tree.inorder(), vec![&3, &5, &7]);

// Delete
assert!(tree.delete(&5));
assert!(!tree.contains(&5));
assert_eq!(tree.len(), 2);

// Balance information
println!("height: {}, balance_factor: {}", tree.height(), tree.balance_factor_root());

// Works with any Ord type
let mut s
```
