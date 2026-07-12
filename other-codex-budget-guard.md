# codex-budget-guard

**Cluster:** rust-misc  
**Language:** Rust  
**Source:** [SuperInstance/codex-budget-guard](https://github.com/SuperInstance/codex-budget-guard)

## Intention

Budget enforcement for Codex CLI — daily/weekly/monthly token limits, phase detection, auto-throttle, and Serde audit snapshots

## How It Works

[code]

## What It's For

Budget enforcement for Codex CLI — daily/weekly/monthly token limits, phase detection, auto-throttle, and Serde audit snapshots

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (228 lines, 8106 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# codex-budget-guard

> 💰 Budget enforcement for [OpenAI Codex CLI](https://github.com/openai/codex).

**Codex is brilliant.** It's the best coding agent in a terminal. But every `codex 'fix this bug'` costs tokens — and tokens cost money. Codex burns through models like GPT-5-codex, which adds up fast when you're iterating.

**Conservation-checker keeps it from being expensive.**

This crate combines Codex's token-tracking architecture with `conservation-checker`'s one-sided conservation laws to give you:

- **Set a budget** — daily, weekly, and monthly token limits
- **Get warned** before you exceed it — phase detection catches accelerating spending
- **Auto-downgrade** when you're close — GPT-5 → GPT-4.1 → GPT-4.1-mini → GPT-4.1-nano
- **Audit snapshots** — Serde-serialized checkpoints for billing and forensics

## How it works

```
┌─────────────────────────────────────────────────────┐
│                   Codex CLI                         │
│  ┌─────────────┐  ┌──────────────┐  ┌────────────┐ │
│  │ TokenUsage   │  │ ModelRouter │  │  Responses  │ │
│  │ (input+      │──│ (which model │  │  API call   │ │
│  │  output+     │  │  to use?)    │  │            │ │
│  │  reasoning)  │  └──────┬───────┘  └─────┬──────┘ │
│  └──────┬──────┘         │                 │       │
│         │                │                 │       │
└─────────┼────────────────┼─────────────────┼───────┘
          │                │                 │
          ▼                ▼                 ▼
┌─────────────────────────────────────────────────────┐
│               codex-budget-guard                    │
│                                                     │
│  ┌─────────────────────────────────────────────┐   │
│  │         BudgetGuard                          │   │
│  │  ┌──────────┐  ┌──────────┐  ┌──────────┐  │   │
│  │  │ Daily    │  │ Weekly   │  │ Monthly  │  │   │
│  │  │ budget   │  │ budget   │  │ budget   │  │   │
│  │  └────┬─────┘  └────┬─────┘  └────┬─────┘  │   │
│  │       │              │              │        │   │
│  │  ┌────▼──────────────▼──────────────▼────┐  │   │
│  │  │   conservation-checker                │  │   │
│  │  │   (Phase detection, drift rates)      │  │   │
│  │  └───────────────────────────────────────┘  │   │
│  │                                             │   │
│  │  Output: BudgetAction                       │   │
│  │  ├─ Proceed("gpt-5-codex")                  │   │
│  │  ├─ Throttle("gpt-4.1-mini")               │   │
│  │  └─ Halt                                    │   │
│  └─────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────┘
```

## Architecture context

At the time of writing, Codex CLI (openai/codex, 88K+ stars) tracks token usage through:

- **`codex_protocol::protocol::TokenUsage`** — total tokens, input tokens, cached tokens, output tokens, reasoning tokens per API call
- **`codex_core`** — session management, model routing, auto-compaction when context windo
```
