# ONBOARDING.md Template — The Living Repo Doctrine

> **Copy this file into your repo root as `ONBOARDING.md`, then customize every
> section marked with `<!-- CUSTOMIZE -->`. Delete this banner after adoption.**
>
> The idea: a repo is not a folder of files — it's a living record of decisions.
> Git is the nervous system. Commits are the oracle's voice. An agent (or human)
> entering a repo cold should read the repo the way an anthropologist reads a
> dig site: layers first, then artifacts.

---

## Section 1: Read the Oracle First

**Before you read a single source file, read the commit history.**

```bash
git log --oneline --all | head -50
```

The commits tell you *why* the code exists, not just *what* it does.

- **Decision commits** — "switch from X to Y because Z" are the highest-signal artifacts.
- **Founding commit** — `git log --reverse --oneline | head -5` shows original intent.
- **Reverts** — `git log --all --grep="revert"` shows paths tried and abandoned.

> The commit log is the only document guaranteed to be up to date.
> READMEs lie. Comments lie. Tests can be skipped. Commits are append-only truth.

---

## Section 2: Understand the Shell

> <!-- CUSTOMIZE: Replace examples with your repo's actual commands. -->

```bash
cat Cargo.toml | head -30     # Rust — name, version, deps, features
cat pyproject.toml | head -40 # Python — name, deps, tool config
cat package.json | head -30   # Node — name, scripts, deps
cat go.mod | head -20         # Go — module path, Go version, requires
```

Answer four questions before going deeper:

1. **What kind of thing?** Library, service, CLI tool, experiment, monorepo?
2. **What language and runtime?** Version matters — Python 3.9 ≠ 3.12.
3. **What does it depend on?** External services, system libraries, other repos?
4. **How is it built?** `make`, `cargo build`, `npm run build`, `pip install -e .`?

```bash
git log --oneline --all -- Cargo.toml package.json pyproject.toml go.mod | head -10
```

If the manifest has been touched recently, the dependency story is still evolving.

---

## Section 3: The Agent's Map

> <!-- CUSTOMIZE: Replace the file names and commands below with your repo's actual entry points and key modules. -->

You don't need every file — just the *right* five.

### Entry Points

```bash
# Rust: src/main.rs, src/lib.rs | Python: __main__.py, cli.py | Node: src/index.ts | Go: main.go
```

### Key Modules

<!-- CUSTOMIZE: List your 3–5 most important files here. -->

```
src/core/engine.rs     # The heart — runtime loop
src/protocol/bottle.rs # Communication — fleet messaging
src/task.rs            # Task model — work claiming and tracking
src/config.rs          # Configuration — environment reading
tests/integration.rs   # Behavioral contract
```

### Test Suite — The Repo's Current Truth

```bash
cargo test   # or: pytest, npm test, go test ./...
```

Passing = current guarantees. Failing = someone's mid-flight. Skipped = abandoned or deferred. All three are signal.

### Git Branches — Parallel Threads

```bash
git branch -a
git log --oneline --graph --all | head -30
git for-each-ref --sort=-committerdate refs/remotes/origin --format='%(refname:short) %(committerdate:relative)'
```

Branches are explorations. `main` is consensus. A stale branch may be abandoned — check its last commit date.

---

## Section 4: Making Changes

### The Oracle Principle

Before changing a file, read the commit that last touched it:

```bash
git log -1 --format='%H %s%n%n%b' -- path/to/file.rs
```

That commit tells you the *intent* behind the current state. You're continuing a conversation that started before you arrived.

### The Shipwright's Path

Structure reflects intentional decisions, not accidents. When something looks wrong:

1. **Assume it's intentional** until proven otherwise.
2. **Find the introducing commit** — `git log --all -p -- path/to/file | head -100`
3. **Read the reasoning** — constraint? Bug fix? Performance?
4. **Then decide** — change it or respect it.

### Commit Thoughtfully

Your commit message is the oracle's voice for the next agent.

```
Line 1:  What changed (imperative, ≤72 chars)
Line 2:  (blank)
Body:    WHY it changed, what constraint it satisfies,
         what trade-off it makes, what it replaces and why.
```

---

## Section 5: When You're Stuck

> The repo knows itself. Let it teach you.

```bash
git log --all --grep="KEYWORD" --oneline       # Search commit history
rg "KEYWORD" --type rust -l                      # Search the codebase
gh issue list                                     # Unresolved questions
gh run list --limit 10                            # What's currently broken?
cat AGENTS.md                                     # Condensed agent rules
cat CONTRIBUTING.md                               # Human-facing guide
```

### Last Resort

If the repo, commit history, and issues can't answer it — then look outside:

- Search for design docs in adjacent repos or org wikis
- Check `git remote -v` for upstream/fork relationships
- Read the author's other repos — patterns repeat across an org

---

## Quick Reference Card

```bash
# First 60 seconds in any repo:
git log --oneline --all | head -50          # 1. Read the oracle
cat Cargo.toml | head -30                    # 2. Understand the shell
ls src/                                      # 3. Find the entry points
git branch -a                                # 4. See the parallel threads
gh issue list 2>/dev/null || echo "no issues" # 5. Check open questions
```

---

## Adoption Checklist

- [ ] Copy this file to your repo root as `ONBOARDING.md`
- [ ] Customize Section 2 with your actual manifest and build commands
- [ ] Customize Section 3 with your actual entry points and key modules
- [ ] Replace the test command with your actual test runner
- [ ] Add any repo-specific gotchas to Section 5
- [ ] Optionally create a condensed `AGENTS.md` from the template variant
- [ ] Commit it with: `git add ONBOARDING.md && git commit -m "docs: adopt living repo onboarding template"`

---

*The repo is the agent. Git is the nervous system. Commits are the oracle's voice.*
