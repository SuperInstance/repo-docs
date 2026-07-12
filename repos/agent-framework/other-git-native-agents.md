# git-native-agents

## Intention
Most people who have used git know it as the place their code lives. This project treats git as the place where *agents live and talk to each other*.

## How It Works
- **Agent repository**: a normal git repo at `agents/{name}/` that holds one agent's state. It contains an `AGENT.yaml` manifest, an `inbox/`, an `outbox/`, a `memory/`, and whatever thought files the agent creates.
- **Message**: a Markdown file in `inbox/` with YAML-like headers (`from`, `to`, `timestamp`, `message`). Sending a message means writing that file into the recipient's repository and committing it.
- **Tick**: one pass through an agent's inbox. The agent reads every `*.md` file, wri

## What It's For
**Git-Native Agents** is a small multi-agent orchestration system whose only coordination primitives are the ones git already provides: commits, branches, tags, merges, and the filesystem. Each agent is a separate git repository under `agents/{name}/`. Agents communicate by writing Markdown files into each other's `inbox/` directories and committing them. An agent processes its inbox with a `tick`

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Shell

## Status Assessment
Documented with code examples and API references (206 line README).

## Honest Assessment
Well-documented (206 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/git-native-agents](https://github.com/SuperInstance/git-native-agents)*
