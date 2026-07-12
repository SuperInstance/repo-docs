# license-compliance

## Intention

CLI tool to check open-source license compatibility across dependency trees

## How It Works

`license-compliance` scans a Rust project's `Cargo.lock`, resolves each dependency's license from its `Cargo.toml` metadata, parses SPDX license expressions (handling `AND`, `OR`, `WITH`, `+`, and parenthesized groups), checks compatibility against your project's license, and generates a report listing compatible, incompatible, and unknown dependencies along with attribution requirements.
The conservation law **γ + η = C** applies: compatible licenses (γ) plus incompatible/unknown ones (η) sum to the total dependency count C. The goal is η = 0.
```
┌──────────────────────────────────────────────────┐
│                   CLI (clap)                      │
│  check / list-licenses / lookup / parse-expr     │
├──────────┬──────────────┬────────────────────────┤
│SpdxParser│  LicenseDb   │  CargoParser           │
│          │              │                        │
│ parse()  │  18 licenses │  scan_dependencies()   │
│ AND/OR/  │  MIT, Apache,│  find_license_for_dep()│
│ WITH/+   │  GPL, BSD... │  lookup_known_crate_   │
│          │              │  license()             │
├──────────┴──────────────┴────────────────────────┤
│          DependencyScanner                        │

## What It's For

CLI tool to check open-source license compatibility across dependency trees

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Tokio, Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (152 lines), includes examples.

- README length: 198 lines, 7124 characters
- Documented sections: What It Does, Architecture, Installation, Usage, API Reference

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
