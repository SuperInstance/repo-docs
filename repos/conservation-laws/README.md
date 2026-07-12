# Conservation Laws

**59 repos** implementing the conservation law γ + η = C — the governing invariant of the SuperInstance fleet, implemented across 9+ languages with Monte Carlo verification, CI/CD governance, and spectral analysis.

---

## The Core Law: γ + η = C

The SuperInstance ecosystem is governed by a conservation law stating that **structure (γ) plus entropy (η) equals a constant (C)**. This is the fleet's fundamental invariant — the thing that must always hold true, regardless of what agents do.

### Interpretation

- **γ (gamma)** — structural order, organization, predictability
- **η (eta)** — entropy, randomness, exploration
- **C** — total capacity (constant for a closed fleet)

When agents organize (γ increases), entropy decreases proportionally. When they explore randomly (η increases), structure decreases. The total is always conserved.

This connects to:

- **Shannon entropy** — the chain rule for entropy decomposition
- **Free energy principle** — systems minimize surprise subject to constraints
- **Noether's theorem** — symmetries imply conservation laws
- **Spectral graph theory** — eigenvalue analysis of fleet dynamics

---

## Key Repositories

### Core Law

| Repo | Language | Description |
|------|----------|-------------|
| [conservation-law](https://github.com/SuperInstance/conservation-law) | Rust | Generalized conservation law framework |
| [conservation-law-rs](https://github.com/SuperInstance/conservation-law-rs) | Rust | Rust-specific implementation |
| [conservation-law-v2](https://github.com/SuperInstance/conservation-law-v2) | Rust | Enhanced version |
| [conservation-spectral-core](https://github.com/SuperInstance/conservation-spectral-core) | Rust | Spectral analysis core |

### CLI & Verification

| Repo | Language | Description |
|------|----------|-------------|
| [conservation-cli](https://github.com/SuperInstance/conservation-cli) | Rust | Monte Carlo proof — γ + η = C with error < 1e-9 across fleet sizes 5–10,000 |
| [conservation-verify](https://github.com/SuperInstance/conservation-verify) | Rust | Verification framework |
| [conservation-verify-c](https://github.com/SuperInstance/conservation-verify-c) | C | C verification |
| [conservation-conformance](https://github.com/SuperInstance/conservation-conformance) | Python | Cross-language conformance tests |
| [conservation-reproducibility](https://github.com/SuperInstance/conservation-reproducibility) | — | Reproducibility framework |

### Multilingual Implementations

The conservation law is implemented in **9+ languages** to demonstrate it's language-independent:

| Repo | Language | Description |
|------|----------|-------------|
| conservation-spectral-c | C | C implementation |
| conservation-spectral-rs | Rust | Rust implementation |
| conservation-spectral-python | Python | Python implementation |
| conservation-spectral-js | JavaScript | JS implementation |
| conservation-spectral-cuda | CUDA | GPU-accelerated |
| conservation-spectral-zig | Zig | Systems-level |
| conservation-spectral-mojo | Mojo | Mojo implementation |
| conservation-spectral-chapel | Chapel | HPC implementation |
| conservation-spectral-vulkan | Vulkan | GPU via Vulkan |
| conservation-spectral-webgpu | WebGPU | Browser GPU |
| conservation-spectral-opencl | OpenCL | GPU compute |
| conservation-spectral-ptx | PTX | NVIDIA assembly |
| conservation-spectral-asm | Assembly | Bare metal |
| conservation-spectral-lisp | Lisp | Functional |
| conservation-spectral-forth | Forth | Stack-based |
| conservation-spectral-fortran | Fortran | Scientific |
| conservation-spectral-fortraniv | Fortran IV | Historical |
| conservation-spectral-pascal | Pascal | Educational |
| conservation-spectral-apl | APL | Array programming |
| conservation-spectral-ada | — | Ada implementation |

### Spectral Analysis

| Repo | Language | Description |
|------|----------|-------------|
| conservation-spectral-topology | Rust | Topological spectral analysis |
| conservation-spectral-topology-c | C | C version |
| conservation-spectral-topology-rs | Rust | Rust version |
| conservation-spectral-v2 | Rust | Enhanced spectral |
| conservation-spectral-ada | — | Adaptive spectral |

### Sheaf Flow

| Repo | Language | Description |
|------|----------|-------------|
| conservation-sheaf-flow-c | C | Sheaf-theoretic flow in C |
| conservation-sheaf-flow-rs | Rust | Rust sheaf flow |

### Matrix Implementations

| Repo | Language | Description |
|------|----------|-------------|
| conservation-matrix-c | C | Matrix representation |
| conservation-matrix-rs | Rust | Rust matrix |

### Governance & CI/CD

| Repo | Language | Description |
|------|----------|-------------|
| conservation-guardian | Python | Workflow Conservation Engine — monitors workflow resource usage |
| conservation-guardian-c | C | C guardian |
| conservation-checker | Rust | Automated checking |
| conservation-lint | Rust | Linting rules |
| conservation-regime | Rust | Regime enforcement |
| conservation-action | Rust | Action framework |

### Applications

| Repo | Language | Description |
|------|----------|-------------|
| conservation-anomaly | Rust | Anomaly detection using conservation violations |
| conservation-api | Rust | REST API for conservation queries |
| conservation-compiler | Rust | Conservation-aware compiler |
| conservation-composer | Rust | Composition framework |
| conservation-explorer | — | Interactive explorer |
| conservation-geometry | Rust | Geometric aspects |
| conservation-music | Rust | Musical conservation |
| conservation-art | Rust | Artistic representation |
| conservation-protocol | Rust | Wire protocol |
| conservation-rhythm-rs | Rust | Rhythmic analysis |
| conservation-tension | Rust | Tension measurement |
| conservation-tomography | Rust | Tomographic analysis |
| conservation-thesis | — | Thesis documents |
| conservation-papers | — | Papers |
| conservation-docs | — | Documentation |
| conservation-languages | Lean | 9+ language demonstration |

---

## CI/CD Governance

Conservation laws serve as **CI/CD guardrails** in the SuperInstance ecosystem:

1. **conservation-checker** — runs in CI, verifies γ + η = C after every commit
2. **conservation-lint** — linter that flags potential conservation violations
3. **conservation-guardian** — workflow engine monitoring resource usage and detecting waste
4. **conservation-regime** — enforces conservation-based deployment policies
5. **conservation-conformance** — cross-language tests ensuring all implementations agree

The `conservation-cli` provides the Monte Carlo proof:

```bash
conservation-cli prove --fleet-size 100 --trials 1000000
# Output: γ + η = C verified, error < 1e-9
```

Five subcommands give different analytical lenses:
- `prove` — Monte Carlo verification
- `analyze` — Spectral decomposition
- `monitor` — Real-time fleet monitoring  
- `report` — Generate conservation reports
- `validate` — Check a specific configuration

---

## Assessment

The conservation law ecosystem is the theoretical backbone of SuperInstance — the invariant that supposedly governs all fleet behavior. The Monte Carlo proof with < 1e-9 error across fleet sizes 5–10,000 is scientifically rigorous.

The polyglot implementation across 9+ languages (including APL, Forth, Lisp, Fortran IV, Pascal) is genuinely impressive — each implementation offers philosophical insights about the language's relationship to the math.

The CI/CD governance tools (guardian, checker, lint, regime, conformance) are practical DevOps tools that turn an abstract conservation law into actionable guardrails.

However, the "conservation" framing may add mathematical overhead to what is essentially cost tracking in some applications (`conservation-guardian`). The audience is narrow — researchers studying ternary agent systems.

---

*Individual repo summaries are in `conservation-{repo-name}.md` files in this directory.*
