# discovery-mad-libs

## Intention
A standalone discovery engine for agents and humans. Walk in, answer questions, watch it explore. Rewind if it goes off track. Let it run if it's onto something.

## How It Works
```
┌──────────────┐
│  ONBOARDING  │ ← Essential questions define the quest
└──────┬───────┘
       │
┌──────▼───────┐
│   TEMPLATE   │ ← Mad-libs shapes the exploration style
└──────┬───────┘
       │
┌──────▼───────┐
│   ENGINE     │ ← LLM generates, GPU verifies, LLM evaluates
│  (loop)      │
└──────┬───────┘
       │
┌──────▼───────┐
│ DISCOVERIES  │ ← Timestamped, readable, rewindable
└──────┬───────┘
       │
┌──────▼───────┐
│   REVIEWER   │ ← You (agent or human) steer the direction
└─

## What It's For
A structured system for iterative discovery — research, world-building, experimentation, ideation, anything. You (human or agent) define the quest. The engine runs autonomous discovery loops using LLMs and (optionally) GPU experiments. You review the output. If it's good, let it run. If it went wrong, rewind to where it diverged and steer it back.

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Python

## Status Assessment
Has substantial documentation (128 lines).

## Honest Assessment
Moderately documented (128 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/discovery-mad-libs](https://github.com/SuperInstance/discovery-mad-libs)*
