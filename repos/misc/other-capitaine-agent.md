# capitaine-agent

**Cluster:** maritime  
**Language:** Python  
**Source:** [SuperInstance/capitaine-agent](https://github.com/SuperInstance/capitaine-agent)

## Intention

Captain's AI first mate for captaine.ai — voyage logging, crew coordination, maritime Q&A via PLATO

## How It Works

this models

Picture a crew working a long voyage. The captain keeps the log — and the log
lives on the captain's chart table, where only the captain reads it. A decision
gets made on the midnight watch ("we'll divert around the storm"); by dawn it's
a memory in one person's head, and the crew member who just came on watch has
no record that the decision was ever made, let alone why.

Now swap "person" for "program." One agent decides something; another agent is
supposed to act on it an hour later; the second one is flying blind because the
first never wrote anything down anywhere the second c

## What It's For

Captain's AI first mate for captaine.ai — voyage logging, crew coordination, maritime Q&A via PLATO

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (326 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# capitaine-agent

## The problem this models

Picture a crew working a long voyage. The captain keeps the log — and the log
lives on the captain's chart table, where only the captain reads it. A decision
gets made on the midnight watch ("we'll divert around the storm"); by dawn it's
a memory in one person's head, and the crew member who just came on watch has
no record that the decision was ever made, let alone why.

Now swap "person" for "program." One agent decides something; another agent is
supposed to act on it an hour later; the second one is flying blind because the
first never wrote anything down anywhere the second could read. That is the
shape of problem this repository is built around, and it splits cleanly in two:

1. **Coordination.** One lead agent (the *captain*) has to break a goal into
   steps, hand each step to the right sub-agent (a *crew member*), choose a
   sensible way to run them all, and then look back and ask "did that work?"
   **This is what the code in this repo actually implements today.**
2. **Shared memory.** Every agent ought to be able to read what the others
   decided and did, and to ask questions of the accumulated record. That half
   is the fleet's *PLATO* idea. This repo is *designed* to plug into it but
   does **not** wire it up in the current code — see
   [Where PLATO fits (and where it doesn't, yet)](#where-plato-fits-and-where-it-doesnt-yet)
   for the honest version.

`capitaine-agent` is a small Python library (no runtime dependencies, Python
≥ 3.10) for layer 1. It uses a maritime vocabulary on purpose — `vessel`,
`crew`, `mission`, `debrief` — because those words map neatly onto the pieces
of a coordination problem. Read the sailing terms as **labels for coordination
ideas, not as a claim that this software tracks real ships.** There is no
fishing-vessel data, no weather feed, no GPS in here; "vessel" is just the name
the library gives to the coordinator's workspace.

## The five pieces, in the order you need them

A coordination problem has a natural shape, and the code follows it. You define
what you want done, you line up who can do it, you decide how to run it, and you
check the result. Each of those is one module under `capitaine_agent/`.

The example below runs through all five: a `Site Survey` mission where one
*scout* inspects an area and two dependent tasks follow once the scout reports.

### 1. A `Mission` is a goal broken into `Objective`s

A **mission** is a named goal (`Mission`) made of smaller steps. Each step is
an **objective** (`Objective`) — a single piece of work that can *depend on*
other objectives finishing first. An objective can carry **success criteria**
(`SuccessCriterion`), machine-checkable rules like "the count must be greater
than 5" or "the result must contain `ok`," so "is this step done?" is a real
question with a real answer rather than a vibe. A mission can also carry
**constraints** (`Constraint`) — boundary conditions ("finish under one hour",
"stay in budge
```
