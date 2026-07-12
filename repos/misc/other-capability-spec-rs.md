# capability-spec-rs

**Cluster:** docs-specs  
**Language:** Rust  
**Source:** [SuperInstance/capability-spec-rs](https://github.com/SuperInstance/capability-spec-rs)

## Intention

Agent capability specification framework — typed descriptors, validation, and runtime introspection

## How It Works

**Production-grade capability specification parser with semver, dependency graphs, and weighted scoring.**

## What It's For

Agent capability specification framework — typed descriptors, validation, and runtime introspection

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (277 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# capability-spec-rs

**Production-grade capability specification parser with semver, dependency graphs, and weighted scoring.**

A capability specification (`CAPABILITY.toml`) is a declarative manifest that describes what a software agent **can do**, how it communicates, what resources it needs, and how it fits into a larger fleet. Think of it as a résumé for autonomous agents — a machine-readable contract for fleet orchestrators.

## What This Gives You

- **`CapabilitySchema`** — Full `CAPABILITY.tomL` schema with serde support
- **TOML parsing + validation** — Parse specs, validate confidence ranges, agent types, statuses
- **`SemVer`** — Semantic versioning with comparison, compatibility, and breaking-change detection
- **`DependencyGraph`** — Directed graph with Kahn's algorithm topological sort, reachability, and LCA
- **Capability scoring** — Weighted scores with recency decay for ranking
- **`CapabilityMatcher`** — Compare two agents' capabilities, compute compatibility and coverage
- **`CapabilitySchemaBuilder`** — Fluent API for programmatic schema construction

## Quick Start

### Parse and validate a spec

```rust
use capability_spec::parser::{parse_capability_toml, validate};

let schema = parse_capability_toml(r#"
version = "1.0.0"

[agent]
name = "my-agent"
type = "vessel"
status = "active"

[capabilities.code_gen]
confidence = 0.9
last_used = "2025-01-15"
description = "Generate code from prompts"
version = "2.1.0"

[capabilities.review]
confidence = 0.8
requires = ["code_gen"]
"#).unwrap();

assert_eq!(schema.agent.name, "my-agent");
assert_eq!(schema.capabilities.len(), 2);
assert!(validate(&schema).is_ok());
```

### Build a schema programmatically

```rust
use capability_spec::builder::CapabilitySchemaBuilder;

let schema = CapabilitySchemaBuilder::new("vessel-7")
    .agent_type("vessel")
    .status("active")
    .capability("code_gen", 0.92, Some("2025-12-01"), Some("Generate code"))
    .capability("review", 0.85, Some("2025-12-03"), Some("Review PRs"))
    .resource_compute("high")
    .resource_cpu(8.0)
    .language("rust")
    .constraint_max_duration("2h")
    .refuse("destructive_ops")
    .build();
```

### Semantic versioning

```rust
use capability_spec::semver::SemVer;

let v = SemVer::parse("1.2.3").unwrap();
assert!(v > SemVer::new(1, 2, 0));
assert!(SemVer::new(1, 5, 0).is_compatible(&SemVer::new(1, 2, 0)));
assert!(!SemVer::new(2, 0, 0).is_compatible(&SemVer::new(1, 2, 0)));
assert!(SemVer::new(2, 0, 0).is_breaking(&SemVer::new(1, 9, 9)));
```

### Dependency graph with topological sort

```rust
use capability_spec::graph::DependencyGraph;

let mut g = DependencyGraph::new();
g.add_edge("deploy", "review");   // deploy depends on review
g.add_edge("review", "code_gen"); // review depends on code_gen

let sorted = g.topological_sort().unwrap();
// code_gen first (no deps), then review, then deploy
assert_eq!(sorted, vec!["code_gen", "review", "deploy"]);

// Reachability: what does deploy transitively depend 
```
