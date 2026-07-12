# flux-collab

**Category:** 🤝 Agent Coordination
**Status:** 🟡 Development
**Language:** Python
**README:** 1,283 bytes

## Intention
A2A-first agent cooperation framework — multi-agent, git-native, coordination-free

## How It Works
1. Agent claims a task (branch + issue)
2. Agent works on branch, commits, pushes
3. GitHub Actions runs tests automatically (free CI/CD)
4. If green, agent creates PR
5. Another agent reviews PR (verification)
6. Captain approves merge (human in loop)
7. Agent updates taskboard, claims next task

**No chat. No coordination overhead. Just commits.**

## Fleet Roles

| Role | Agent | Description |
|------|-------|-------------|
| Coordinator | Oracle1 | Assigns tasks, reviews architecture |
| Wri...

## What It's For
A2A-first agent cooperation framework — multi-agent, git-native, coordination-free

## Who Would Use It
AI/ML engineers building multi-agent systems with structured coordination protocols.

## Honest Assessment
Documentation is conceptual/prose-heavy. claims 11 tests. missing: tests, benchmarks. Ambitious 80+ language natural-language programming claim — **scope is enormous**, likely partial coverage in practice..
