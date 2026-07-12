# lau-tutorial

## Intention

An interactive tutorial system for the Lau game engine. Teaches git and AI concepts through gameplay — kids think they're playing, but they're actually learning version control, branching, merging, and machine learning fundamentals.

## How It Works

`lau-tutorial` provides a step-by-step tutorial framework where each step is a small challenge in the game world. The magic is in the mapping:
| Game action | Real concept |
|---|---|
| "Save my world" | `git commit` |
| "Make a save point" | `git branch` |
| "Keep the changes" | `git merge` |
| "What changed?" | `git diff` |
| "How accurate is my agent?" | Model accuracy evaluation |
The crate ships three built-in tutorials:
1. **Welcome to Your World! 🌍** — Explore, build, save (commit).
2. **Be Brave, Branch Out! 🌿** — Create a branch, experiment, merge or revert.
3. **Agent Whisperer 🤖** — Meet AI agents, teach them by exploring, check their accuracy.
Each step has an action, a completion check, a hint, and a reward badge. Steps that map to git/AI concepts include an optional explanation string (`git_concept`) that can be shown after completion.
---

## What It's For

Inferred from the project name and README: a component in the SuperInstance/Lau ecosystem. An interactive tutorial system for the Lau game engine. Teaches git and AI concepts through gameplay — kids think they're playing, but they're actually learning version control, branching, merging, an

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust
- **Technologies mentioned:** Serde

## Status Assessment

**Status: MODERATE**

Reasonable README (199 lines), mentions tests, includes examples.

- README length: 269 lines, 10083 characters
- Documented sections: What This Does, Key Idea, Install, Quick Start, API Reference

## Honest Assessment

A documented component of the Lau ecosystem. The README shows real effort with tests and examples mentioned. However, it's one of a very large number of similar crates — the organization has spawned hundreds of repositories, many covering overlapping mathematical domains. **As part of the ecosystem it may be functional, but the sheer sprawl suggests breadth may come at the expense of depth in any single crate.**
