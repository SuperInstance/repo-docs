# Dev Tools — Index

**Total repos: 16**

Development tooling for the SuperInstance ecosystem: snapshot toolkits (SnapKit) across multiple languages and a collection of testing tools. These are the utilities that other SuperInstance developers use to build, test, and verify their crates.

## Category Overview

### SnapKit — Polyglot Snapshot Toolkit (9 repos)

SnapKit is a snapshot testing and state management toolkit implemented across 9 languages. The core concept: capture, diff, merge, compress, and verify structured key-value state. Each implementation provides the same API surface in a different language:

- **snapkit-rs** (Rust) — The reference implementation. 23 documented tests. Capture, diff, merge, compress, verify.
- **snapkit-c** — C99 implementation for embedded/edge
- **snapkit-cuda** — GPU-accelerated snapshot processing
- **snapkit-fortran** — Fortran implementation (scientific computing heritage)
- **snapkit-js** — JavaScript/TypeScript for web
- **snapkit-python** — Python implementation
- **snapkit-rust** — Alternative Rust implementation
- **snapkit-v2** — Next-generation unified SnapKit
- **snapkit-zig** — Zig implementation (comptime generics)

### Testing Tools (7 repos)

- **test-runner-vessel** — Fleet agent for running tests (part of the fleet coordination system)
- **test-rs** — Rust testing utilities
- **test-mutator** — Mutation testing framework
- **test-repo** — Test repository for validation
- **test-pages-repo** — GitHub Pages testing
- **test-sdk-connection** — SDK connection testing
- **test-tool-extract** — Tool extraction testing

### Key Interconnections

- **SnapKit** provides the state verification layer used across the ecosystem — agents snapshot their state, diff against expected results, and verify conservation laws
- The polyglot SnapKit implementations mirror the Grand Pattern polyglot approach (lau-mathematics)
- **test-runner-vessel** is a fleet agent that connects to the agent-framework and cocapn-marine categories
- SnapKit's capture/diff/merge model relates to CRDT concepts used in the oxide-gpu and conservation-laws categories

## Full Repository Listing

### SnapKit

| Repo | Language | Description |
|------|----------|-------------|
| [snapkit-rs](./other-snapkit-rs.md) | Rust | Reference implementation (23 tests) |
| [snapkit-c](./other-snapkit-c.md) | C | C99 snapshot toolkit |
| [snapkit-cuda](./other-snapkit-cuda.md) | CUDA | GPU-accelerated snapshots |
| [snapkit-fortran](./other-snapkit-fortran.md) | Fortran | Fortran snapshots |
| [snapkit-js](./other-snapkit-js.md) | JavaScript | JS snapshot toolkit |
| [snapkit-python](./other-snapkit-python.md) | Python | Python snapshots |
| [snapkit-rust](./other-snapkit-rust.md) | Rust | Alternative Rust impl |
| [snapkit-v2](./other-snapkit-v2.md) | Multi | Next-gen unified toolkit |
| [snapkit-zig](./other-snapkit-zig.md) | Zig | Zig snapshots |

### Testing Tools

| Repo | Language | Description |
|------|----------|-------------|
| [test-runner-vessel](./other-test-runner-vessel.md) | — | Fleet test runner agent |
| [test-rs](./other-test-rs.md) | Rust | Rust testing utilities |
| [test-mutator](./other-test-mutator.md) | Rust | Mutation testing |
| [test-repo](./other-test-repo.md) | — | Validation test repo |
| [test-pages-repo](./other-test-pages-repo.md) | — | Pages testing |
| [test-sdk-connection](./other-test-sdk-connection.md) | — | SDK connection tests |
| [test-tool-extract](./other-test-tool-extract.md) | — | Tool extraction tests |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
