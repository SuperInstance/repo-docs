# entropy-gpu-rs

## Intention
**Batch information-theoretic computation library** providing Shannon entropy, KL divergence, Jensen-Shannon divergence, mutual information matrices, transfer entropy, and entropy profiles (permutation entropy, sample entropy) — designed for parallel batch processing with `rayon` and trivial GPU portability.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
Information-theoretic measures are the backbone of modern data analysis: feature selection (mutual information), causal inference (transfer entropy), anomaly detection (entropy profile shifts), and model comparison (KL divergence between predicted and true distributions). However, computing these measures for large numbers of distributions or long time series is computationally expensive.

This li

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (138 line README).

## Honest Assessment
Moderately documented (138 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/entropy-gpu-rs](https://github.com/SuperInstance/entropy-gpu-rs)*
