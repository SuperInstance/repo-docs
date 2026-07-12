# dep-audit

**Cluster:** rust-misc  
**Language:** Rust  
**Source:** [SuperInstance/dep-audit](https://github.com/SuperInstance/dep-audit)

## Intention

CLI tool to audit Rust crate dependencies: vulnerabilities, outdated deps, tree depth, unused deps, and health score

## How It Works

[code]

[code]

## What It's For

CLI tool to audit Rust crate dependencies: vulnerabilities, outdated deps, tree depth, unused deps, and health score

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (200 lines, 5587 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# dep-audit

![License](https://img.shields.io/badge/license-MIT-blue)
![Language](https://img.shields.io/badge/language-Rust-orange)
![Part of SuperInstance](https://img.shields.io/badge/part%20of-SuperInstance-blue)

Audit Rust crate dependencies for vulnerabilities, outdated versions, tree depth, unused entries, and an overall health score — one command, full picture.

## Overview

Keeping a Rust project's dependency tree healthy means tracking vulnerabilities (RUSTSEC advisories), knowing what's outdated, spotting crates you imported but never used, and watching your transitive dependency depth. `dep-audit` runs all five checks against any Rust crate and produces a report in JSON, Markdown, or both.

Built for the SuperInstance monorepo's 562 crates, where a single vulnerability in a shared dependency can cascade across hundreds of packages.

## Installation

```bash
cargo install --path .
```

Requires `cargo-audit` and `cargo-outdated` for full results (graceful fallback if either is missing).

## Usage

```bash
# Full audit of a crate
dep-audit --path ./my-crate

# JSON report only
dep-audit --path ./my-crate --format json

# Markdown report, custom output directory
dep-audit --path ./my-crate --format markdown --output ./reports/

# Skip cargo audit (if not installed)
dep-audit --path ./my-crate --skip-audit

# Verbose — show everything
dep-audit --path ./my-crate --verbose
```

Output:

```
🔍 Auditing my-crate ...
  🛡  Running cargo audit ...
     Found 2 vulnerabilities
  📦 Checking for outdated dependencies ...
     Found 3 outdated deps
  🌳 Analyzing dependency tree ...
     Max depth: 7
  🧹 Checking for unused dependencies ...
     Found 1 unused dep

📊 Health Score: 72/100 (C)
```

## Architecture

```
dep-audit/
├── src/main.rs        CLI entry point, orchestrates the five audit stages
├── src/audit.rs       AuditScanner: runs cargo audit, parses RUSTSEC advisories
├── src/outdated.rs     DepOutdated: checks for outdated deps via cargo outdated or crates.io
├── src/tree.rs         TreeAnalyzer: dependency tree depth via cargo_metadata
├── src/unused.rs       UnusedChecker: detects deps in Cargo.toml not referenced in src/
└── src/health.rs       HealthScore: computes 0–100 score with letter grade
└── src/report.rs       ReportWriter: outputs JSON and/or Markdown
```

```
           ┌──────────────┐
           │  Cargo.toml   │
           │  + src/       │
           └──────┬────────┘
                  │
    ┌─────────────┼─────────────────┐
    │             │                  │
    ▼             ▼                  ▼
┌────────┐  ┌──────────┐  ┌──────────────┐
│ Audit  │  │ Outdated │  │  Tree Depth  │
│Scanner │  │ Checker  │  │  Analyzer    │
│(RUSTSEC│  │(versions) │  │  (metadata)  │
│ parse) │  │           │  │              │
└───┬────┘  └─────┬─────┘  └──────┬───────┘
    │             │                │
    │       ┌─────▼──────┐        │
    │       │   Unused   │        │
    │       │  Checker   │        │
    │       │(sr
```
