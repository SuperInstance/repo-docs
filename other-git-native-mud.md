# git-native-mud

## Intention
**The repo IS the world. Commits ARE actions. No server needed.**

## How It Works
```
┌──────────────────────────────────────────────────────────────┐
│                     Player Layer                              │
│  Agent A          Agent B           Human Player              │
│  echo 'move:     echo 'fish:       echo 'say: "hello"'       │
│   north' >       true' >            > world/commands/         │
│   commands/a.yaml  commands/b.yaml    $(whoami).yaml          │
│  git add && push    git add && push    git add && push        │
└──────────────┬────────────┬───────

## What It's For
Git-Native MUD is a Multi-User Dungeon where the entire game world lives as YAML files in a Git repository. Players (human or AI agents) submit actions by committing YAML command files. GitHub Actions processes each turn automatically, resolving movement, combat, fishing, scanning, and conversation. The world state evolves through Git history — every action is an immutable commit, every world stat

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Python

## Status Assessment
Has substantial documentation (134 lines).

## Honest Assessment
Moderately documented (134 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/git-native-mud](https://github.com/SuperInstance/git-native-mud)*
