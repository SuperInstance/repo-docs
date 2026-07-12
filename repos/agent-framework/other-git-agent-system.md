# git-agent-system

## Intention
A **single git-native agent** that uses git's object model (commits, notes, tags, branches) as its entire state machine — no databases, no message queues, no external infrastructure. Just git.

## How It Works
The agent maps five conceptual primitives to git operations:

| Agent Concept | Git Primitive | Complexity |
|---------------|---------------|------------|
| State transition | `git commit` | O(1) per transition |
| Inbox message | `git notes add -f HEAD` | O(1) write, O(n) scan |
| Persistent memory | `git tag memory/{key} HEAD -f` | O(1) lookup |
| Thought / exploration | `git checkout -b thought/{topic}` | O(1) branch create |
| Decision / merge | `git merge thought/{topic}` | O(n) in branch

## What It's For
Most agent frameworks require external infrastructure: a database for state, a message queue for communication, a key-value store for memory. This eliminates all of that by mapping agent primitives onto git operations. The result is an agent system with zero dependencies beyond git itself, where every state change is an auditable commit, memory is a tagged pointer, and inter-agent communication is

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Shell

## Status Assessment
Documented with code examples and API references (82 line README).

## Honest Assessment
Has documentation (82 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/git-agent-system](https://github.com/SuperInstance/git-agent-system)*
