# flux-fleet-stdlib

**Category:** 🤝 Agent Coordination
**Status:** 🟡 Development
**Language:** Python
**README:** 5,014 bytes

## Intention
Shared error codes, status types, and common utilities for the entire FLUX fleet — the common language every repo speaks

## How It Works
Principles

1. **Same strings everywhere** — error code values are plain strings (`"COOP_TIMEOUT"`) that work as Python enum values, Go constants, and Rust `&str` constants.
2. **Zero dependencies** — stdlib only. No external packages.
3. **Wire-ready** — every type has JSON serialization for git-based message transport.
4. **Rich context** — `FleetError` carries `source_repo`, `source_agent`, `timestamp`, `error_id`, and an arbitrary `context` dict.
5. **Composable** — `ErrorChain` wraps nested...

## What It's For
Shared error codes, status types, and common utilities for the entire FLUX fleet — the common language every repo speaks

## Who Would Use It
AI/ML engineers building multi-agent systems with structured coordination protocols.

## Honest Assessment
Has code examples. missing: tests, benchmarks.
