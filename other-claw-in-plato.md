# claw-in-plato

**Cluster:** fleet-agent-infra  
**Language:** Python  
**Source:** [SuperInstance/claw-in-plato](https://github.com/SuperInstance/claw-in-plato)

## Intention

PLATO-native agent living in a Docker container. Its only I/O is tiles. Telegram bridge for direct human contact.

## How It Works

All versions share the same PLATO-native agent architecture:
- Inbox/outbox tile system via internal PLATO server (:8847)
- LLM calls via SiliconFlow (ByteDance-Seed/Seed-OSS-36B-Instruct)
- Task execution loop with autonomous multi-iteration work cycles
- Memory search across doc rooms
- Sub-agent spawning (parallel LLM threads)
- Skill system via doc/skills room
- Inline port execution (exec, fs, web, models, docs)
- Background daemon for proactive task checking

## What It's For

PLATO-native agent living in a Docker container. Its only I/O is tiles. Telegram bridge for direct human contact.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** lightweight
- **Note:** Brief (33 lines, 988 chars). Minimal docs.

## Honest Assessment

Brief documentation. Could be a small genuine utility or AI-generated exercise. Limited depth.