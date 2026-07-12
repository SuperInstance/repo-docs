# fleet-vector-api

**URL:** https://github.com/SuperInstance/fleet-vector-api

## Intention
Semantic search API for the SuperInstance crate ecosystem. Indexes all fleet repos by meaning rather than keyword.

## How It Works
TypeScript/Rust API implementing brute-force cosine similarity search over in-memory vectors. Uses Cloudflare Workers AI `@cf/baai/bge-small-en-v1.5` (384-dim BGE embeddings) for semantic embedding. At N≈1,000 vectors, brute-force is faster than ANN indices. Includes deployed Cloudflare Worker instance. Designed for scaling to HNSW at N>10K.

## What It's For
Finding relevant crates by semantic similarity instead of keyword matching. "Rate limiting middleware" finds "throttle handler" even with zero token overlap.

## Who Would Use It
Fleet developers discovering repos, and AI agents needing to find relevant tools.

## Language/Stack
TypeScript/Rust, Cloudflare Workers, BGE embeddings

## Status Assessment
Active — deployed to Cloudflare Workers with live endpoint.

## Honest Assessment
Real project — genuine semantic search with legitimate engineering. The brute-force-at-small-scale reasoning is correct, and the scaling path to HNSW is well-reasoned. The deployed instance and concrete API make this practical, not theoretical.
