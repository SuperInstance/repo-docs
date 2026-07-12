# lau-probability-theory

## Intention

Probability theory library — distributions, limit theorems, Bayesian inference, hypothesis testing, and MCMC

## How It Works

This crate provides a comprehensive toolkit for probabilistic modeling and statistical inference:
- **Discrete distributions** — Bernoulli, Binomial, Poisson, Geometric, Uniform, Hypergeometric
- **Continuous distributions** — Normal, Exponential, Uniform, Gamma, Beta, Chi-squared, Student-t
- **Distribution traits** — unified `Distribution` trait with PDF/PMF, CDF, mean, variance, sampling
- **Limit theorems** — Law of Large Numbers (weak & strong), Central Limit Theorem verification
- **Bayesian inference** — conjugate priors (Beta-Binomial, Normal-Normal), posterior updates, credible intervals, Bayesian model comparison
- **Hypothesis testing** — Z-test, t-test, chi-squared test for proportions, with p-value computation
- **MCMC** — Metropolis-Hastings sampler with configurable proposal, burn-in, thinning, and diagnostics
- **Copulas** — Gaussian copula, Clayton copula, Independence copula, with CDF, sampling, and Kendall's tau
- **Agent beliefs** — `BinaryBelief` (Beta posterior), `ContinuousBelief` (Normal posterior), `Decision` with expected-utility maximization

## What It's For

Probability theory library — distributions, limit theorems, Bayesian inference, hypothesis testing, and MCMC

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (198 lines), mentions tests, includes examples.

- README length: 283 lines, 10171 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
