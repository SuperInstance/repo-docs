# dify-budget-watchdog

## Intention
Dify makes building AI apps easy. This makes running them affordable. Set a budget. Get warned before you exceed it. Models auto-downgrade when you're close.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
If you run 50+ Dify workflows with GPT-4o, Claude Opus, and Gemini Pro, your API bills can
spiral out of control fast. Most teams:

1. Don't know they're overspending until the bill arrives.
2. Have no automatic mechanism to downgrade models when budgets are tight.
3. Lack per-team-member visibility into aggregate consumption.

Dify Budget Watchdog solves all three with a lightweight, embeddable R

## Who Would Use It
Add to your `Cargo.toml`:

```toml
[dependencies]
dify-budget-watchdog = "0.1"
```

## Language / Stack
Rust

## Status Assessment
Claims production-ready with tests and documentation.

## Honest Assessment
Well-documented (390 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/dify-budget-watchdog](https://github.com/SuperInstance/dify-budget-watchdog)*
