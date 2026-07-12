# delaunay-triang-rs

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/delaunay-triang-rs](https://github.com/SuperInstance/delaunay-triang-rs)

## Intention

Delaunay triangulation and Voronoi diagrams in pure Rust: Bowyer-Watson, edge flip, quad-edge

## How It Works

### Bowyer-Watson (`bowyer_watson`)

1. Create a **super-triangle** large enough to contain all input points.
2. For each point:
   - Find all triangles whose circumcircle contains the point.
   - Identify the boundary polygon of the cavity (edges shared with exactly one bad triangle).
   - Delete bad triangles; create new triangles from each boundary edge to the new point.
3. Remove all triangles that reference super-triangle vertices.

The super-triangle trick ensures the point always lies inside some triangle's circumcircle, so the cavity is never empty.

### Edge Flip (`edge_flip`)

Given 

## What It's For

Delaunay triangulation and Voronoi diagrams in pure Rust: Bowyer-Watson, edge flip, quad-edge

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (154 lines, 8328 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# delaunay-triang-rs

[![crates.io](https://img.shields.io/crates/v/delaunay-triang-rs.svg)](https://crates.io/crates/delaunay-triang-rs)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Delaunay triangulation and Voronoi diagrams in pure Rust — Bowyer-Watson incremental insertion, edge flip, and Guibas-Stolfi quad-edge.

## The Problem

Given a set of 2D points, you need the "best" triangulation — one that avoids skinny triangles and is uniquely defined by the input points. This is the Delaunay triangulation: for every triangle, no other input point lies inside its circumcircle.

The dual of the Delaunay triangulation is the **Voronoi diagram**, which partitions the plane into regions closest to each site. Both structures are fundamental in computational geometry: mesh generation, nearest-neighbor queries, terrain modeling, and spatial interpolation.

## The Insight

The Delaunay property has a clean geometric characterization: a triangulation is Delaunay if and only if for every edge, the sum of the opposite angles in the two adjacent triangles is ≤ 180°. Equivalently, no point lies inside any triangle's circumcircle.

This property enables two algorithmic approaches:

1. **Incremental insertion (Bowyer-Watson):** Add points one at a time. For each new point, find all triangles whose circumcircle contains it (the "cavity"), delete them, and re-triangulate the resulting polygonal hole with the new point.
2. **Edge flipping:** Start with any triangulation. Find edges that violate the Delaunay property (opposite angles sum > 180°) and flip them. Repeat until no more flips are needed. Guaranteed to terminate because each flip increases the minimum angle.

## How It Works

### Bowyer-Watson (`bowyer_watson`)

1. Create a **super-triangle** large enough to contain all input points.
2. For each point:
   - Find all triangles whose circumcircle contains the point.
   - Identify the boundary polygon of the cavity (edges shared with exactly one bad triangle).
   - Delete bad triangles; create new triangles from each boundary edge to the new point.
3. Remove all triangles that reference super-triangle vertices.

The super-triangle trick ensures the point always lies inside some triangle's circumcircle, so the cavity is never empty.

### Edge Flip (`edge_flip`)

Given an existing triangulation:
1. For each pair of adjacent triangles sharing an edge (a, b) with opposite vertices c and d.
2. If point d lies inside the circumcircle of triangle (a, b, c), the edge is **illegal**.
3. Flip: replace edge (a, b) with edge (c, d), creating triangles (c, d, a) and (c, d, b).
4. Repeat until no illegal edges remain.

Bounded by O(n²) flips in the worst case, but typically O(n) for well-behaved inputs.

### Quad-Edge (`quad_edge`)

The Guibas-Stolfi data structure represents a planar subdivision using **quad-edges** — each logical edge is stored as four directed half-edges (original, rotated 90°, symmetric, rotated 270°). Operations:

- `
```
