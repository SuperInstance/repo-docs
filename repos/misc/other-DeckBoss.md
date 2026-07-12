# DeckBoss

**Cluster:** maritime  
**Language:** TypeScript  
**Source:** [SuperInstance/DeckBoss](https://github.com/SuperInstance/DeckBoss)

## Intention

🛩️ Agent Edge OS — flight deck for launching, recovering, and coordinating agents. (Unrelated to purplepincher/deckboss, the fishing logbook — same name, coincidence, different product.)

## How It Works

### System Overview

[code]

### Mission State Machine

[code]

### Memory Stack

[code]

### Design Philosophy: Glue vs Handmade

| Layer | Approach | Rationale |
|-------|----------|-----------|
| **Director + Weaver** | Handmade (~200 LOC) | Owns orchestration, state, continual learning — control where it matters |
| **MCP Server** | Glue (official SDK) | Zero custom protocol, single Worker entrypoint |
| **Cloudflare Primitives** | Glue (official APIs) | Vectorize, D1, R2, Workers AI — zero maintenance |
| **Squadrons** | Plugin (separate Workers/DOs) | Zero overhead until used — specifici

## What It's For

🛩️ Agent Edge OS — flight deck for launching, recovering, and coordinating agents. (Unrelated to purplepincher/deckboss, the fishing logbook — same name, coincidence, different product.)

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (567 lines, 22247 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# DeckBoss — The Agent Edge OS

> **📚 Documentation:** [`PLUG_AND_PLAY.md`](./PLUG_AND_PLAY.md) · [`GETTING_STARTED.md`](./GETTING_STARTED.md) · [`ARCHITECTURE.md`](./ARCHITECTURE.md) · [`API_REFERENCE.md`](./API_REFERENCE.md) · [`LOW_LEVEL.md`](./LOW_LEVEL.md)

> **Flight deck for AI agents.** Launch from Claude Code (or any MCP client), recover results anywhere, run background missions while you sleep. We're not another agent framework — we're the roads, fuel, and traffic laws that make persistent, self-improving agents the new normal.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Quick Start](#quick-start)
- [CLI Commands & API](#cli-commands--api)
- [Configuration](#configuration)
- [Squadrons (Built-in Agents)](#squadrons-built-in-agents)
- [Custom Squadrons](#custom-squadrons)
- [Integration with commodore-protocol & Fleet](#integration-with-commodore-protocol--fleet)
- [Repository Structure](#repository-structure)
- [Development](#development)
- [Roadmap](#roadmap)
- [License](#license)

---

## Overview

DeckBoss gives every MCP-native agent (Claude Code, Grok, Ollama, Cloudflare-native, ManusAI...) a **persistent, globally-distributed, continually-learning backend** that runs on *your* free Cloudflare account.

Claude handles reasoning. DeckBoss handles memory, orchestration, and background execution.

**Why DeckBoss?**

| Problem | DeckBoss Solution |
|---------|-------------------|
| Claude forgets everything when the laptop closes | Missions survive via Durable Objects + alarms |
| No background execution for long-running tasks | Edge-native parallel execution across 330+ locations |
| No persistent memory across sessions | Cognitive model with semantic + episodic + procedural memory |
| Context window fills up fast | Offload indexing, scraping, monitoring to agent squadrons |
| Expensive to run | Free tier: 10K AI inferences/day, 200K vectors, 5 GB D1, zero surprise bills |

### Key Principles

- **Free** — 10k AI inferences/day, 200k vectors, 5 GB D1, zero surprise bills
- **Persistent** — Missions survive laptop closure via Durable Objects + alarms
- **Parallel & Edge-Native** — 330+ locations, no Docker, no local infra
- **Yours** — Your CF account, your data, your cognitive model forever
- **General-purpose first** — One universal MCP server + Director core
- **Hyper-specific second** — Squadrons load as dynamic plugins (no monolith bloat)

---

## Features

### Core Capabilities

| Feature | Description | Status |
|---------|-------------|--------|
| **MCP Server** | Native Model Context Protocol integration with Claude Code, Windsurf, Grok, etc. | ✅ Stable |
| **Director Durable Object** | Per-user stateful brain — orchestration, state, continual learning (~200 LOC) | ✅ Stable |
| **Mission Manager** | Episodic memory + alarm-based scheduling for background tasks | ✅ Stable |
| **Cognitive Model** | Hybrid memory: semantic (Vectorize), episodic (SQLite), procedura
```
