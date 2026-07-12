# free-probability-c

## Intention
**Xavier initialization. He initialization. Kaiming initialization.**

## How It Works
The MP moments for λ=1 are the Catalan numbers: 1, 2, 5, 14, 42, 132... These are also the moments of Wigner's semicircle law. That's not a coincidence — it's the free probability version of the central limit theorem. Stack enough freely independent random matrices and their eigenvalue distribution converges to a semicircle, exactly like summing classically independent random variables converges to a Gaussian.

The free cumulants of MP(λ=1) are the cleanest objects in all of free probability: κ_

## What It's For
Take a random weight matrix W of shape d×d with entries drawn from N(0, σ²). Form the covariance WᵀW/d. What do its eigenvalues look like?

Not Gaussian. Not uniform. They follow the **Marchenko-Pastur distribution**:

```
ρ(x) = √((b−x)(x−a)) / (2πσ²λx)
```

where λ = p/n is the feature-to-sample ratio, a = σ²(1−√λ)², b = σ²(1+√λ)².

This distribution has **hard edges**. The eigenvalues are packe

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
C

## Status Assessment
Has substantial documentation (273 lines).

## Honest Assessment
Moderately documented (273 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/free-probability-c](https://github.com/SuperInstance/free-probability-c)*
