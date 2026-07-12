# si-registry-rs

## Intention
Local fleet registry client — query repos, capabilities, budgets from Supabase or local cache

## How It Works
Local fleet registry client for SuperInstance Query repos, capabilities, and agent budgets from a Supabase-backed registry — or scan local directories for capability manifests. Built with sync Rust, zero async runtime required. - Supabase HTTP client — list, search, and query repos/capabilities/budgets - Local file cache — JSON-backed cache with configurable TTL - Conservation invariant — verify γ + η = total budget constraints across the fleet - Local scanner — discover repos by reading CAPABILITY.toml manifests from disk - Fully synchronous — uses ureq, no tokio/async needed - Serde-compatible types — serialize/deserialize everything as JSON

## What It's For
Local fleet registry client — query repos, capabilities, budgets from Supabase or local cache

## Who Would Use It
Rust developers in the SuperInstance conservation-law ecosystem

## Language / Stack
Rust

## Status Assessment
**Mature** — Comprehensive documentation suggesting active, sustained development.

- README size: 15,990 characters, 650 lines
- Code examples: 38 blocks
- Installation instructions: yes
- Testing mentioned: yes
- License mentioned: yes
- API documentation: yes
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Code examples present (38 code blocks)
- Installation/usage instructions provided
- Testing mentioned
- Extensive, detailed README documentation

**Concerns:**
- One of 40+ si-* repos — may be a proof-of-concept rather than production tool

**Overall:** Well-documented and worth serious evaluation if the domain is relevant.
