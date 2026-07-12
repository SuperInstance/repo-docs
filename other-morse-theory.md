# morse-theory

## Intention

Morse theory on manifolds — critical points, Morse complex, handle attachments

## How It Works

### Morse Functions
A smooth function f: M → ℝ is a **Morse function** if all its critical points (where ∇f = 0) are **non-degenerate** (the Hessian matrix H_f is invertible at each critical point).
The **Morse index** μ(p) of a critical point p is the number of negative eigenvalues of H_f(p) — i.e., the dimension of the unstable manifold at p.
### The Morse Polynomial
The **Morse polynomial** encodes the critical point structure:
```
𝓜_f(t) = Σ_p t^{μ(p)}
```
For example, a torus with standard height function has critical points of index 0, 1, 1, 2:
```
𝓜(t) = t⁰ + 2t¹ + t² = 1 + 2t + t²
```
### The Morse Inequalities
Let c_k = number of critical points of index k, and b_k = k-th Betti number of M. Then:
**Weak inequalities:**

## What It's For

Morse theory on manifolds — critical points, Morse complex, handle attachments

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (80 lines), includes examples.

- README length: 123 lines, 4748 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
