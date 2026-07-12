# Claude_Baton

**Cluster:** maritime  
**Language:** Not specified  
**Source:** [SuperInstance/Claude_Baton](https://github.com/SuperInstance/Claude_Baton)

## Intention

Generational context handoff for Claude Code. Seamless, auditable, infinite-context agents that ship forever.

## How It Works

(built on official 2026 primitives)

| Trigger (via PreCompact + SessionStart hooks) | Action |
|-----------------------------------------------|--------|
| **48 %** | Background Onboarder subagent (parallel, zero main-context impact) builds baton bundle |
| **82 %** | Spawns Young Agent (native subagent or Agent Team) loaded only with fresh onboarding files |
| **93 %** | Old Agent demoted to pure Advisor. Full A2A overlap via shared Artifacts/MCP |
| **Retirement** | Full context snapshot archived; Young Agent takes over seamlessly |

All files are git-tracked and auto-committed. Unused gene

## What It's For

Generational context handoff for Claude Code. Seamless, auditable, infinite-context agents that ship forever.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Unknown — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (109 lines, 5926 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Claude_Baton 🏃‍♂️

**Infinite context for Claude Code through automatic generational baton passing.**

Claude Code's 1M-token context (Opus 4.6) and native compaction are powerful — but long-running projects still hit the wall: slow compaction loops, lost nuance, and agents that "forget" across sessions.  

Claude_Baton fixes this at the root. When context hits 48 %, it quietly spawns an Onboarder subagent that builds a complete handover package *while you keep shipping*. At 82 % it launches a fresh Young Agent (native subagent/Agent Team), overlaps in A2A advisory mode, then retires the Old Agent gracefully.  

Result: functionally infinite context, perfect audit trail, reusable skills, and a living project memory that grows stronger with every generation.

100 % native Claude Code plugin — uses only official hooks, subagents, MCP, and Agent Teams. Zero external wrappers for the MVP.

[![Claude Code Marketplace](https://img.shields.io/badge/Install%20from%20Marketplace-blue)](https://code.claude.com/docs/en/discover-plugins)  
[![GitHub Repo](https://img.shields.io/badge/GitHub-claude-baton-black)](https://github.com/YOUR-USERNAME/claude-baton)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)  
![Stars](https://img.shields.io/github/stars/SuperInstance/claude-baton?style=social)

## Why this is becoming essential in 2026

- Native Claude Code already gives you Auto Memory (CLAUDE.md), context compaction, parallel subagents (up to 7+ in Agent Teams), and MCP for persistent storage — yet developers are still manually fighting context cliffs.
- Existing solutions like **claude-mem** (32k+ stars) do great session-to-session compression and RAG, but they summarize and lose detail. Ralph Wiggum gives long-running loops but resets context. No plugin yet delivers *proactive generational handoff* with full human-readable memoirs, decision logs, and A2A overlap.
- Claude_Baton is the production version the community has been asking for on Reddit, GitHub issues, and X: infinite context without compaction pain, auditable history, and automatic skill extraction.

## 🚀 60-Second Install

```bash
# In any Claude Code session
/plugin install claude-baton
/baton init
```

(Claude Code auto-detects complex projects and prompts you on first use. For brand-new repos it sets up `.baton/` and registers hooks instantly.)

## How It Works (built on official 2026 primitives)

| Trigger (via PreCompact + SessionStart hooks) | Action |
|-----------------------------------------------|--------|
| **48 %** | Background Onboarder subagent (parallel, zero main-context impact) builds baton bundle |
| **82 %** | Spawns Young Agent (native subagent or Agent Team) loaded only with fresh onboarding files |
| **93 %** | Old Agent demoted to pure Advisor. Full A2A overlap via shared Artifacts/MCP |
| **Retirement** | Full context snapshot archived; Young Agent takes over seamlessly |

All files are git-tracked and auto-committed. Unused generations
```
