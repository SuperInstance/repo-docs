# AGENTS.md — Repo Root Quick Start

> Condensed from [ONBOARDING.md](./ONBOARDING.md). Delete this line after customizing.

## First 60 Seconds

```bash
git log --oneline --all | head -50   # The oracle — read WHY before WHAT
cat Cargo.toml | head -30             # What is this? (replace with your manifest)
ls src/                               # Where does execution begin?
```

## Rules

1. **Read the commit before the code.** `git log -1 --format='%s%n%n%b' -- <file>`
   The last commit touching your area explains its current state and intent.
2. **Commits are the source of truth.** READMEs drift. Comments lie. Tests get
   skipped. The commit log is append-only and always current.
3. **Assume structure is intentional.** Before changing something that looks
   wrong, find the commit that introduced it and read the reasoning.
4. **Commit messages are for the next agent.** Write the WHY, not just the WHAT.
   Include the constraint, the trade-off, what you replaced and why.

## Making Changes

```bash
# Read the last commit on your target file
git log -1 --format='%H %s%n%n%b' -- path/to/file

# Make your change, then commit thoughtfully
git commit -m "fix: handle empty fleet state in engine loop

The engine assumed at least one agent was always active. When the fleet
drained to zero (maintenance mode), the loop panicked on None unwrap.
Added early return with IdleState. Fixes #42."
```

## When Stuck

```bash
git log --all --grep="KEYWORD" --oneline
rg "KEYWORD" --type rust -l
gh issue list
gh run list --limit 5
```

## Quick Reference

| Question | Command |
|----------|---------|
| Why does this exist? | `git log --reverse --oneline \| head -5` |
| What changed recently? | `git log --oneline -20` |
| What's the current truth? | `cargo test` (or equivalent) |
| What branches exist? | `git branch -a` |
| What's broken? | `gh run list --limit 5` |

---

*Read the repo like an anthropologist: layers first, then artifacts.*
*The repo knows itself — let it teach you.*
