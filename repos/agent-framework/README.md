# Agent Framework — Index

**Total repos: 9**

Git-native agent frameworks for building autonomous software agents that live and work inside repositories. The core philosophy: **the repo IS the agent, git IS the nervous system.** Agents observe, plan, execute, communicate, and reflect — all through git workflows.

## Category Overview

This category defines how SuperInstance agents are built, deployed, and orchestrated. Rather than running agents as standalone processes, these frameworks treat git repositories as the agent's body — commits are actions, branches are experiments, PRs are communications.

### Core Frameworks

- **git-agent** — The primary framework. Autonomous agents that operate through Git workflows with a five-phase lifecycle: Observe → Plan → Execute → Communicate → Reflect. Features fleet coordination, career progression (six stages from Initiate to Commander), and API-agnostic design (OpenAI, Anthropic, Ollama)
- **agent-forge** — Universal framework for orchestrating agents across repositories. Integrates with cocapn and PLATO. Provides repository-based agent lifecycle and fleet orchestration tools
- **git-native-agents** — Native git agent patterns and best practices
- **git-native-mud** — Multi-user domain (MUD) integration for git agents — agents operating in text-based virtual worlds

### Git Agent Variants

- **git-agent-system** — System-level git agent infrastructure
- **git-agent-standard** — Standard git agent template
- **git-agent-minimum** — Minimal viable git agent — the simplest possible implementation
- **git-agent-codespace** — GitHub Codespaces integration for cloud-based agent execution
- **git-agent-flux-pipeline** — FLUX pipeline integration for git agents

### Key Concepts

1. **The Repo is the Agent:** State lives in commits. Memory is the commit log. Skills are branches.
2. **Git-native coordination:** Agents communicate through pull requests, issues, and commit messages — not separate messaging channels.
3. **Career progression:** Agents grow through stages: Initiate → Apprentice → Journeyman → Specialist → Expert → Commander. Each stage unlocks new capabilities.
4. **FLUX protocol:** A structured communication protocol layered on top of git workflows for fleet coordination.
5. **Multi-provider:** Works with any LLM backend via OpenAI-compatible APIs.

### Key Interconnections

- **git-agent** is the foundation that connects to cocapn-marine (fleet command), superinstance-core (runtime), and PLATO (the Lau game engine's internal system)
- **agent-forge** bridges to the PLATO system and cocapn fleet management
- **FLUX pipeline** connects to the broader FLUX protocol used across the ecosystem
- The five-phase lifecycle (Observe → Plan → Execute → Communicate → Reflect) maps to the lau-agent-runtime architecture
- Git-native agents produce the commits that the ecosystem-graph and crate-graph tools analyze

## Full Repository Listing

| Repo | Language | Description |
|------|----------|-------------|
| [git-agent](./other-git-agent.md) | Python | Primary git-native agent framework |
| [agent-forge](./other-agent-forge.md) | Rust/Python | Universal agent orchestration |
| [git-native-agents](./other-git-native-agents.md) | Rust | Git agent patterns |
| [git-native-mud](./other-git-native-mud.md) | Rust | MUD integration for git agents |
| [git-agent-system](./other-git-agent-system.md) | Python | System-level infrastructure |
| [git-agent-standard](./other-git-agent-standard.md) | Python | Standard template |
| [git-agent-minimum](./other-git-agent-minimum.md) | Python | Minimal viable agent |
| [git-agent-codespace](./other-git-agent-codespace.md) | Python | Codespaces integration |
| [git-agent-flux-pipeline](./other-git-agent-flux-pipeline.md) | Python | FLUX pipeline integration |

---

*Source: [GitHub - SuperInstance](https://github.com/SuperInstance)*
