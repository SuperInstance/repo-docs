# codespace-edge-rd

**Cluster:** cs-implementations  
**Language:** Not specified  
**Source:** [SuperInstance/codespace-edge-rd](https://github.com/SuperInstance/codespace-edge-rd)

## Intention

R&D: Codespace→Edge agent lifecycle, yoke transfer, devcontainer templates

## How It Works

### Research Question 1: Codespace as Agent Habitat

GitHub Codespaces provide:

- 2–32 core vCPUs
- 4–64 GB RAM
- 32–128 GB storage
- Linux environment with Docker support
- Internet access (LLM APIs, GitHub API)
- Auto-suspend after 30 minutes idle (configurable)

Key research areas:

| Question | Status | Notes |
|----------|--------|-------|
| Can agents operate fully in Codespaces? | ✅ Validated | Capitaine fleet uses this pattern |
| API for programmatic Codespace management? | ✅ Available | GitHub REST API `/codespaces` endpoints |
| Background daemons (cron)? | ✅ Works | systemd timers

## What It's For

R&D: Codespace→Edge agent lifecycle, yoke transfer, devcontainer templates

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Unknown — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (147 lines, 6566 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# Codespace→Edge Agent R&D

**Research and development** for Codespace-to-Edge agent lifecycle, yoke transfer protocols, and devcontainer templates. Investigating how git-native agents can train in GitHub Codespaces (cloud) and deploy to edge hardware (Jetson, Raspberry Pi, ESP32) while maintaining complete state continuity.

## Why It Matters

The SuperInstance fleet operates on a **cloud-thinks, edge-acts** paradigm. Agents are born in GitHub Codespaces — cloud development environments with full compute, unlimited bandwidth, and access to LLM APIs. But production deployment often targets edge hardware: Jetson GPUs for inference, Raspberry Pis for IoT control, ESP8266s for sensor reading.

The challenge is **state continuity**: an agent that has been learning and adapting in the cloud for weeks must transfer its accumulated intelligence to a resource-constrained edge device without losing its training, skills, or personality. This is the "yoke transfer" problem.

This matters because:

- **Edge devices have constraints** — 80KB RAM (ESP8266), no GPU (Pi Zero), intermittent connectivity
- **Cloud has unlimited resources** — but $0.09/hour Codespace costs add up, and latency to the edge matters
- **The intelligence gap is real** — a cloud agent with GPT-4 access behaves fundamentally differently from the same agent on an ESP8266 with a lookup table
- **Crystallization bridges the gap** — fluid intelligence (LLM calls) must be compiled to solid intelligence (code, lookup tables, compiled policies) before transfer

## How It Works

### Research Question 1: Codespace as Agent Habitat

GitHub Codespaces provide:

- 2–32 core vCPUs
- 4–64 GB RAM
- 32–128 GB storage
- Linux environment with Docker support
- Internet access (LLM APIs, GitHub API)
- Auto-suspend after 30 minutes idle (configurable)

Key research areas:

| Question | Status | Notes |
|----------|--------|-------|
| Can agents operate fully in Codespaces? | ✅ Validated | Capitaine fleet uses this pattern |
| API for programmatic Codespace management? | ✅ Available | GitHub REST API `/codespaces` endpoints |
| Background daemons (cron)? | ✅ Works | systemd timers, cron jobs |
| Cost model? | Researched | Free tier: 120 core-hours/month. Pro: $0.09/core-hour |
| Multiple agents per Codespace? | ✅ Possible | tmux sessions, separate working directories |

### Research Question 2: Yoke-Out Protocol (Cloud → Edge)

State that needs serialization beyond git repos:

| State Type | Serialization | Transfer Method |
|-----------|--------------|-----------------|
| Git repos | `git bundle` | Delta transfer (only changed commits) |
| Environment variables | `.env` file (encrypted) | `age` encryption |
| Running processes | Checkpoint/restore (CRIU) | Docker checkpoint |
| Memory state | Serialize to JSON/Cap'n Proto | Compressed transfer |
| Skill registry | JSONL packs | Already git-native |
| Model weights | Safetensors | Quantized + sharded |

The **bandwidth budget** for edge targets is tight:

| T
```
