# bsp-tree

**Cluster:** cs-ds-algos  
**Language:** Rust  
**Source:** [SuperInstance/bsp-tree](https://github.com/SuperInstance/bsp-tree)

## Intention

A Rust library for Bsp Tree

## How It Works

**Construction:** The tree is built recursively from a set of line segments:

[code]

**Line splitting:** A line segment AB is classified against a divider by computing the cross product:

[code]

- side > 0: P is in front (left) of the line
- side < 0: P is behind (right)
- side = 0: P is on the line

If the two endpoints of a segment are on opposite sides, the segment is split at the intersection point using parametric interpolation:

[code]

**Front-to-back traversal:** Given a viewpoint V:

[code]

This produces an O(n) ordered output — no sorting needed.

**Complexity:**

| Operation | Ti

## What It's For

A Rust library for Bsp Tree

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (115 lines, 4871 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# BSP Tree

**BSP Tree** (Binary Space Partitioning) is a Rust library implementing a 2D BSP tree for spatial partitioning of line segments — providing front-to-back ordering from any viewpoint, used in rendering, collision detection, and constructive solid geometry.

## Why It Matters

BSP trees were the rendering backbone of every major 3D game engine from Doom (1993) through Quake III Arena (1999). The core idea — recursively splitting space by hyperplanes to create an ordered traversal from any viewpoint — eliminates the need for a z-buffer and enables perfect visibility sorting. Beyond rendering, BSP trees are used in CAD systems for boolean operations on polygons, in robotics for motion planning (partitioning free space), and in collision detection for broad-phase culling. The structure's ability to produce a viewpoint-dependent ordering in O(n) traversal time (after O(n² log n) preprocessing) makes it uniquely valuable when the same geometry is viewed from many different angles.

## How It Works

**Construction:** The tree is built recursively from a set of line segments:

```
build(lines):
  if len(lines) ≤ 1: return Leaf(lines)
  splitter = lines[0]        // pick a splitting line
  front = []; back = []
  for each line in lines[1:]:
    (f, b) = line.split_by(splitter)
    if f: front.append(f)
    if b: back.append(f)
  front.append(splitter)     // splitter goes in front
  return Branch(splitter, build(front), build(back))
```

**Line splitting:** A line segment AB is classified against a divider by computing the cross product:

```
side(P) = (P.x − A.x)(B.y − A.y) − (P.y − A.y)(B.x − A.x)
```

- side > 0: P is in front (left) of the line
- side < 0: P is behind (right)
- side = 0: P is on the line

If the two endpoints of a segment are on opposite sides, the segment is split at the intersection point using parametric interpolation:

```
t = side(A) / (side(A) − side(B))
intersection = A + t × (B − A)
```

**Front-to-back traversal:** Given a viewpoint V:

```
traverse(node, V):
  if Leaf: output all lines
  if Branch:
    if splitter.side(V) ≥ 0:  // viewer in front
      traverse(front, V)
      traverse(back, V)
    else:                      // viewer behind
      traverse(back, V)
      traverse(front, V)
```

This produces an O(n) ordered output — no sorting needed.

**Complexity:**

| Operation | Time | Notes |
|-----------|------|-------|
| Construction | O(n² log n) worst | Depends on splitter choice |
| Front-to-back traversal | O(n) | For n lines |
| Point classification | O(log n) | One comparison per level |
| Node count | O(n) | Each split adds ≤ 1 node |

## Quick Start

```rust
use bsp_tree::{Line, BspNode};

fn main() {
    let lines = vec![
        Line::new([0.0, 0.0], [10.0, 0.0]),
        Line::new([5.0, -5.0], [5.0, 5.0]),
        Line::new([0.0, 3.0], [10.0, 3.0]),
    ];
    let tree = BspNode::new(lines);
    println!("Tree nodes: {}", tree.node_count());

    let mut ordered = Vec::new();
    tree.collect_fro
```
