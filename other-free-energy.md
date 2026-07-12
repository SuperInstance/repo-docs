# free-energy

## Intention
**Minimize surprise. Maximize survival. The Free Energy Principle, computed.**

## How It Works
```
free-energy
│
├── variational_free_energy    ← Core FEP computations
│   ├── free_energy()              F = complexity - accuracy
│   ├── complexity()               KL[q || p]
│   ├── accuracy()                 Expected log-likelihood
│   ├── surprise()                 -ln p(o)
│   ├── elbo()                     Evidence lower bound
│   └── optimize_variational()     Gradient-based belief update
│
├── GenerativeModel            ← Agent's world model
│   ├── set_likelihood()           p(obser

## What It's For
The Free Energy Principle, proposed by Karl Friston (2006), states that biological agents must minimize the difference between their internal model of the world and what they actually observe. This difference is called **variational free energy** — a mathematically tractable upper bound on surprise (negative log-evidence).

The core equation:

```
F = complexity - accuracy
  = KL[q(z) || p(z)] - E

## Who Would Use It
```bash
cargo add free-energy
```

Or add to your `Cargo.toml`:

```toml
[dependencies]
free-energy = "0.1"
```

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (281 line README).

## Honest Assessment
Well-documented (281 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/free-energy](https://github.com/SuperInstance/free-energy)*
