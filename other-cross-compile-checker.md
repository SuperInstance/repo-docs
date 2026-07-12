# cross-compile-checker

**Cluster:** rust-misc  
**Language:** Rust  
**Source:** [SuperInstance/cross-compile-checker](https://github.com/SuperInstance/cross-compile-checker)

## Intention

CLI tool to check cross-compilation compatibility of Rust projects

## How It Works

[code]

[code]

## What It's For

CLI tool to check cross-compilation compatibility of Rust projects

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (184 lines, 5846 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# cross-compile-checker

![License](https://img.shields.io/badge/license-MIT-blue)
![Language](https://img.shields.io/badge/language-Rust-orange)
![Part of SuperInstance](https://img.shields.io/badge/part%20of-SuperInstance-blue)

CLI tool to check cross-compilation compatibility of Rust projects — analyzes `Cargo.toml` dependencies against known target triples, runs `cargo check` across platforms, and generates compatibility matrix reports.

## Overview

When you're shipping a Rust crate that needs to run on more than `x86_64-unknown-linux-gnu`, figuring out *which* targets actually work is tedious. This tool parses your `Cargo.toml`, checks every dependency against a built-in database of 50+ Rust target triples, detects platform-specific crates (winapi, cocoa, nix, x11...), flags wasm/no_std incompatibilities, and produces a report telling you exactly where your project will break and why.

Built for the SuperInstance fleet, where crates need to run on everything from ESP32 (`thumbv6m-none-eabi`) to WASM to `aarch64-apple-darwin`.

## Installation

```bash
cargo install --path .
```

Requires Rust 1.70+. No external dependencies beyond what's in `Cargo.toml`.

## Usage

### List known targets

```bash
# All targets
cross-compile-checker targets

# Filter by OS
cross-compile-checker targets --os linux

# Filter by architecture
cross-compile-checker targets --arch aarch64
```

### Check compatibility

```bash
# Analyze a Cargo.toml against all targets
cross-compile-checker compat --path ./Cargo.toml

# JSON output for scripting
cross-compile-checker compat --json
```

Output shows risk levels per target:

```
Cross-compilation compatibility analysis for ./Cargo.toml

  ✅ Safe x86_64-unknown-linux-gnu
  ⚠️  Warning wasm32-unknown-unknown
      → tokio likely won't work on wasm32-unknown-unknown
      → reqwest likely won't work on wasm32-unknown-unknown
  ❌ Danger thumbv6m-none-eabi
      → tokio requires std — incompatible with bare-metal
      → serde_json requires std — incompatible with bare-metal

Summary: 12 safe, 5 warnings, 3 danger (out of 20 targets)
```

### Run cargo check across targets

```bash
# Check popular targets
cross-compile-checker check --project ./my-crate

# Specific targets
cross-compile-checker check --targets x86_64-pc-windows-msvc,aarch64-unknown-linux-gnu,wasm32-unknown-unknown
```

### Generate a compatibility report

```bash
# Table format (default)
cross-compile-checker report --project ./my-crate

# Markdown for READMEs
cross-compile-checker report --project ./my-crate --format markdown

# JSON for CI pipelines
cross-compile-checker report --project ./my-crate --format json
```

### Suggest CI targets

```bash
# Get top 5 CI targets based on popularity + compatibility
cross-compile-checker suggest --path ./Cargo.toml --top 5
```

## Architecture

```
cross-compile-checker
├── src/main.rs            CLI entry, clap subcommands (Targets, Compat, Check, Report, Suggest)
├── src/target_db.rs       Built-in database of
```
