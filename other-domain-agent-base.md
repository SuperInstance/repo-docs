# domain-agent-base

## Intention
Shared `DomainAgent` base class for the Cocapn fleet's per-domain Python agents. One file (`agent.py`, 126 lines). Inherit it, implement `run()`, get PLATO tile submission, health checks, and stats reporting.

## How It Works
If the intent is for this to be the real shared base, in order:

1. Make it importable (add the `[tool.hatch.build.targets.wheel]` target + a
   `domain_agent_base/` package). 🔮
2. Reconcile the version (`0.1.0` vs `1.0.0`).
3. Add at least one test so CI's `pytest` has something to run (and drop the `|| true`
   once a test exists).
4. Either get one real consumer to import it hard (drop the `try/except` fallback in
   `fishinglog-agent`), or relabel this repo explicitly as a **template** and u

## What It's For
All of the following is read directly from `agent.py`. Marker key: ✅ real today ·
⚠️ real but conditional · 🔮 later phase.

## Who Would Use It
This is the single most important honesty gap in the repo, so it gets its own section.

**Symptom.** `from domain_agent_base import DomainAgent` raises
`ModuleNotFoundError: No module named 'domain_agent_base'`, and the package fails to
install:

```
$ uv pip install -e .

## Language / Stack
Python

## Status Assessment
Marked as archived, WIP, or early version.

## Honest Assessment
Well-documented (272 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/domain-agent-base](https://github.com/SuperInstance/domain-agent-base)*
