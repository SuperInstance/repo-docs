# crate-graph

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/crate-graph](https://github.com/SuperInstance/crate-graph)

## Intention

Dependency graph analysis for Rust crate fleets

## How It Works

**Graph construction:**
1. Scan directory for `Cargo.toml` files
2. Parse each with `toml` crate to extract crate name and dependencies
3. Build a `petgraph::DiGraph<String, ()>` where nodes are crate names and edges are dependencies
4. Detect cycles via DFS (O(V + E))

**Layer computation (topological layering):**
[code]
Crates at layer 0 are leaf crates (depended-on by others but depend on nothing in-fleet). Higher layers are higher-level crates. Computed via Kahn's algorithm: O(V + E).

**Critical path:**
The longest path in the DAG, computed via dynamic programming on the topologically sor

## What It's For

Dependency graph analysis for Rust crate fleets

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (94 lines, 4713 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Crate Graph

**Crate Graph** is a Rust CLI tool for analyzing dependency graphs of Rust crate fleets — scanning Cargo.toml manifests, building a dependency graph with `petgraph`, computing layered architecture, critical paths, impact analysis, and bisimulation of structurally equivalent subgraphs.

## Why It Matters

When a monorepo or fleet contains dozens to hundreds of crates, understanding the dependency topology becomes critical for maintenance: which crates are most depended-on (highest blast radius for breaking changes), what is the longest dependency chain (critical path for compilation time), and are there circular dependencies (which Cargo cannot resolve)? Crate Graph answers these questions by building the full dependency graph and applying graph algorithms. It identifies the layer structure (a topological sort into levels), finds the critical path (longest path in the DAG), and detects bisimilar subgraphs — pairs of crates with structurally identical dependency neighborhoods, indicating potential for consolidation.

## How It Works

**Graph construction:**
1. Scan directory for `Cargo.toml` files
2. Parse each with `toml` crate to extract crate name and dependencies
3. Build a `petgraph::DiGraph<String, ()>` where nodes are crate names and edges are dependencies
4. Detect cycles via DFS (O(V + E))

**Layer computation (topological layering):**
```
layer(v) = 0  if v has no in-fleet dependents
         = 1 + max(layer(u) for all u that v depends on)
```
Crates at layer 0 are leaf crates (depended-on by others but depend on nothing in-fleet). Higher layers are higher-level crates. Computed via Kahn's algorithm: O(V + E).

**Critical path:**
The longest path in the DAG, computed via dynamic programming on the topologically sorted graph:

```
dist(v) = max(dist(u) + 1) for all edges (u, v)
```

This represents the longest compilation chain — if crate A depends on B depends on C, the path length is 2 (two sequential compilation steps).

**Impact analysis:**
For each crate, count how many other crates transitively depend on it (downstream impact):

```
downstream(v) = |{u : v ∈ ancestors(u)}|
```

Computed via reverse BFS from each node. O(V × (V + E)) for all nodes.

**Bisimulation:**
Two nodes u and v are bisimilar if they have identical dependency signatures — same set of dependencies and dependents. Found by clustering on (dep_signature, rdep_signature) pairs. O(V × E) in the naive case.

## Quick Start

```bash
# Analyze a fleet directory
cargo run -- /path/to/fleet

# Show impact for a specific crate
cargo run -- --impact fleet-auth

# Show critical path
cargo run -- --critical-path

# Find bisimilar pairs
cargo run -- --bisimilar
```

## API

| Module | Description |
|--------|-------------|
| `DependencyGraph` | Graph construction with cycle detection |
| `LayerCalculator` | Topological layering (Kahn's algorithm) |
| `CriticalPath` | Longest dependency chain |
| `ImpactAnalyzer` | Downstream impact per crate |
| `BisimulationChec
```
