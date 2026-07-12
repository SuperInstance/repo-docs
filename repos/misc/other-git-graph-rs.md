# git-graph-rs

## Intention
A Rust library that models git commit history as directed acyclic graphs (DAGs), branches as forests, agent assignments as topologies, and commit-graph paths as message routes. Built on `petgraph` for multi-agent coordination systems where git is the shared state.

## How It Works
A Rust library that models git commit history as directed acyclic graphs (DAGs), branches as forests, agent assignments as topologies, and commit-graph paths as message routes. Built on `petgraph` for multi-agent coordination systems where git is the shared state.

## What It's For
When multiple AI agents work in the same repository — each on their own branch — the commit graph becomes the **shared coordination substrate**. Reasoning about this graph lets you answer:

- **Where did branches diverge?** (find common ancestors for merge planning)
- **Who's working on what?** (agent-to-branch topology)
- **Are two agents going to conflict?** (divergence detection)
- **How do mes

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Documented with code examples and API references (127 line README).

## Honest Assessment
Moderately documented (127 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/git-graph-rs](https://github.com/SuperInstance/git-graph-rs)*
