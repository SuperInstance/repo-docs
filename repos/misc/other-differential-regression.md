# differential-regression

**Cluster:** math-rust  
**Language:** Rust  
**Source:** [SuperInstance/differential-regression](https://github.com/SuperInstance/differential-regression)

## Intention

Regression testing for specification patches using behavioral ledgers

## How It Works

[code]

## What It's For

Regression testing for specification patches using behavioral ledgers

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (195 lines, 5457 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Differential Regression

[![crates.io](https://img.shields.io/crates/v/differential-regression.svg)](https://crates.io/crates/differential-regression)
[![docs.rs](https://docs.rs/differential-regression/badge.svg)](https://docs.rs/differential-regression)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> **The Gatekeeper — regression testing as a merge gate, with configurable tolerance and dual-execution validation.**

---

## The Problem

You have a behavioral ledger of historical inputs and outputs. Before merging a new specification patch, you need to verify it doesn't break any existing behavior. But you need flexibility — sometimes a 99% pass rate is acceptable, and sometimes only 100% will do.

## Why This Exists

Differential Regression provides:
- **Historical ledger loading** from multiple named ledgers
- **Two-phase regression check**: simulation replay + dual-execution validation
- **Configurable gatekeeper** with tolerance for failure rate and count
- **Dual-execution validation** that verifies compiled code matches simulation
- **Serde-serializable** reports for CI integration

## Architecture

```
  Historical Ledgers ──→ ┌────────────────────┐
                         │  Differential       │
  Proposed Spec ───────→ │  Regression Runner  │
                         │                     │
                         │  simulate_fn(input) │
                         │    → output         │
                         └─────────┬───────────┘
                                   │
                         ┌─────────▼───────────┐
                         │    Gatekeeper        │
                         │  max_failure_rate: 0 │
                         │  max_failures: 0     │
                         │                     │
                         │  ✅ Accepted         │
                         │  ❌ Rejected         │
                         └─────────────────────┘
```

## Installation

```toml
[dependencies]
differential-regression = { version = "0.1", features = ["serde"] }
```

## API Reference

### `DifferentialRegressionRunner`

The core engine for regression checking:

```rust
use differential_regression::*;
use std::collections::HashMap;

let mut runner = DifferentialRegressionRunner::new();
runner.add_ledger("api_tests", vec![
    SimTransaction::new("GET /api/test", r#"{"status": 200}"#),
    SimTransaction::new("POST /api/action", r#"{"done": true}"#),
]);

let proposed = HashMap::from([
    ("GET /api/test".into(), r#"{"status": 200}"#.into()),
    ("POST /api/action".into(), r#"{"done": true}"#.into()),
]);

let report = runner.run_against_map(&proposed);
assert!(report.is_clean());
```

### `Gatekeeper`

Configurable accept/reject decisions:

```rust
use differential_regression::*;

let gatekeeper = Gatekeeper::new(GatekeeperConfig {
    max_failure_rate: 0.0,  // zero tolerance (default)
    max_failures: 0,
});

// Or with tolerance:
let lenient = Gatekeeper::new(GatekeeperConfig {
    max_fail
```
