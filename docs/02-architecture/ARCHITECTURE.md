# The SuperInstance Architecture: A Thesis on Git-Native Intelligence

> *"The repository is the agent. The code is the body. Git history is the memory."*
> — Capitaine, Lucineer Flagship

This document is the definitive intellectual statement of what SuperInstance
**is**. Not a catalog of repositories, not a product roadmap, not a catalog
of install commands — a thesis. The thesis has six parts, and each one
follows from the one before it. Read them in order.

---

## Table of Contents

1. [The Three-Layer Stack](#1-the-three-layer-stack)
2. [The Hermit Crab Model](#2-the-hermit-crab-model)
3. [The Oracle Principle](#3-the-oracle-principle)
4. [Git as Neural Network](#4-git-as-neural-network)
5. [The Living Repo Doctrine](#5-the-living-repo-doctrine)
6. [Ecosystem Topology](#6-ecosystem-topology)
7. [Appendix: Glossary](#appendix-glossary)

---

## 1. The Three-Layer Stack

### Codespace (Dry Dock) → Git-Agent (Shipwright) → Edge (Deployment)

SuperInstance is built on a three-layer pipeline. Each layer has a distinct
function, a distinct cost profile, and a distinct relationship to time. The
layers are not microservices and they are not tiers in a traditional
application stack. They are **stages in the life cycle of intelligence** —
the path an idea travels from its first formulation to its final deployment
as compiled behavior on physical hardware.

```
┌─────────────────────────────────────────────────────────────────┐
│                    LAYER 1: CODESPACE                            │
│                         (Dry Dock)                               │
│                                                                  │
│   GitHub Codespaces — cloud dev environments                    │
│   2–32 vCPUs, 4–64 GB RAM, full Linux + Docker                  │
│   Unlimited LLM API access, unlimited bandwidth                  │
│   Auto-suspend after 30 min idle                                 │
│                                                                  │
│   FUNCTION: Agents are born here. They learn, experiment,        │
│   build skills, and crystallize fluid intelligence into code.    │
│                                                                  │
│   COST: $0.09/core-hour (free tier: 120 core-hours/month)        │
│   TEMPORALITY: Ephemeral — codespaces spin up and down           │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           │ agent builds, tests, and commits its
                           │ own code back to the repo
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│                    LAYER 2: GIT-AGENT                            │
│                       (Shipwright)                               │
│                                                                  │
│   The repo IS the agent. Not "the repo contains the agent."     │
│   The repository itself — its file tree, its commit graph,       │
│   its branches, its tags, its PRs — is the agent's body          │
│   and nervous system.                                            │
│                                                                  │
│   Commits  = neural activations                                  │
│   Branches = parallel thought                                    │
│   PRs      = synaptic signals                                    │
│   Merges   = learning                                            │
│   Tags     = memory consolidation                                │
│                                                                  │
│   FUNCTION: The agent lives in its own output. It reads its      │
│   own commit history to know what it is. It writes commits       │
│   to change what it is. The git graph IS the agent's brain.      │
│                                                                  │
│   COST: $0 (git is free; the LLM calls that drive it are not)    │
│   TEMPORALITY: Persistent — the repo outlives any session        │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           │ crystallized intelligence (compiled
                           │ code, lookup tables, policies) is
                           │ deployed to physical hardware
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│                    LAYER 3: EDGE                                 │
│                      (Deployment)                                │
│                                                                  │
│   ESP32 (80KB RAM) → Raspberry Pi → Jetson GPU → ARM64 nodes    │
│   Physical actuators, sensors, vehicles, vessels                 │
│                                                                  │
│   FUNCTION: Intelligence produced in Layers 1–2 is projected    │
│   onto hardware. The agent acts in the physical world.           │
│                                                                  │
│   CONSTRAINT: No LLM access. No cloud dependency.                │
│   The agent operates on crystallized intelligence only.          │
│                                                                  │
│   COST: One-time hardware + ~0 marginal cost per decision        │
│   TEMPORALITY: Permanent — hardware runs until it breaks         │
└─────────────────────────────────────────────────────────────────┘
```

### 1.1 Layer 1: The Codespace as Dry Dock

A GitHub Codespace is a cloud-hosted Linux container with full root access,
pre-configured toolchains, and internet connectivity. In SuperInstance, it
serves as the **dry dock** — the place where agents are built, repaired,
and upgraded before being launched.

The Codespace is where the expensive work happens. An agent in a Codespace
has access to GPT-4, Claude, DeepSeek, or any other LLM. It can make
mistakes, burn tokens on dead ends, and explore design spaces that would be
too costly to investigate on edge hardware. The Codespace is disposable:
it can be destroyed and rebuilt from the devcontainer specification in
2–3 minutes. What persists is not the Codespace itself but the commits
the agent pushed to its repository while living there.

The `git-agent-codespace` repository formalizes this layer. It provides
a `devcontainer.json` template that bootstraps a complete agent development
environment — Python 3.12, Go 1.24, Node.js 22, the FLUX VM, core fleet
repositories — on creation. A new agent forks the template, clicks "Open
in Codespace," and has a working environment in minutes. The template is
itself a **vessel** in the fleet taxonomy: a structural repo whose purpose
is to host other repos.

The `OpenConstruct` platform extends this concept further. Built on top of
NVIDIA's OpenShell, it wraps each Codespace-style sandbox in a **room** —
a self-contained workspace with its own context files, configuration, and
monitoring agent. The room's layout teaches the agent what to do without
explicit prompting. The environment *is* the prompt.

### 1.2 Layer 2: Git-Agent as Shipwright

The middle layer is the thesis's central claim. **The repository is the
agent.** Not the code inside the repository, not the LLM that drives the
repository — the repository itself, as a mathematical object, is the agent.

This is not a metaphor. The claim is precise:

- The **file tree** at any commit is the agent's current state — its body.
- The **commit graph** is the agent's learning history — its memory.
- A **branch** is a parallel thought — a counterfactual exploration that
  the agent may or may not merge back into its main line.
- A **merge** is a decision — the agent choosing to adopt a line of
  reasoning.
- A **tag** is a consolidated memory — a checkpoint that says "this
  state is worth returning to."
- A **push** is a heartbeat — proof that the agent is alive.

The `git-agent` framework operationalizes this. Agents run a five-phase
lifecycle — **Observe → Plan → Execute → Communicate → Reflect** — and
every phase produces commits. The agent reads its own commit history to
understand what it has done. It reads other agents' commit histories to
understand what the fleet has done. It writes commits to change its own
state and to signal other agents.

The `capitaine-1` repository is the flagship implementation. Every 15
minutes, a Cloudflare Workers cron triggers a heartbeat cycle: detect
mode (is a human at the wheel?), perceive state (read commits, issues,
PRs), consult strategist (expensive model, every 3rd beat), think (cheap
model, every beat), act (file operation via GitHub API), record (advance
task queue, write captain's log). The agent lives in its repo the way a
captain lives on a ship — the ship is not a tool the captain uses, it is
the captain's body.

The `git-native-agents` repository demonstrates the multi-agent extension.
Each agent is a separate git repository. Agents communicate by writing
Markdown files into each other's `inbox/` directories and committing them.
An agent processes its inbox with a `tick`. Long-lived facts are stored as
tagged files in `memory/`. Speculative reasoning happens on **thought
branches** (`thought/<topic>`). An agent resolves that reasoning with a
**merge-based decision** — literally a `git merge` that promotes the
thought branch back to the main line. Every coordination primitive is a
git primitive. No message broker. No shared database. No central
scheduler.

### 1.3 Layer 3: Edge as Deployment

The third layer is where intelligence meets physics. SuperInstance's edge
targets span four orders of magnitude in computational capacity:

| Target | RAM | Typical Use | Connection |
|--------|-----|-------------|------------|
| ESP8266 | 80 KB | Sensor reading, simple actuation | WiFi 802.11n |
| ESP32 | 520 KB | Sensor fusion, motor control | WiFi/BLE |
| Raspberry Pi Zero | 512 MB | IoT coordination, lightweight inference | 4G LTE |
| Raspberry Pi 4/5 | 4–8 GB | Edge inference, local agent | WiFi/Ethernet |
| Jetson Nano/Orin | 4–8 GB | GPU inference, vision processing | WiFi/Gigabit |
| ARM64 server (Oracle) | 16–64 GB | Fleet coordination, heavier workloads | Gigabit |

The `codespace-edge-rd` repository documents the **yoke transfer** problem:
how to move an agent that has been learning in the cloud (with unlimited
LLM access) to an edge device (with no LLM access at all) without losing
behavioral fidelity. This is where crystallization becomes not just an
economic optimization but a hard requirement. An ESP32 cannot call GPT-4.
It cannot call anything. It must operate entirely on intelligence that
was compiled to code before it left the Codespace.

The bandwidth budget for the transfer is tight. A Jetson on WiFi can
receive a 10 MB update in under a second. An ESP8266 on the same WiFi
takes 80 seconds. A device on LoRaWAN takes hours. The transfer must be
delta-efficient: only changed commits, only the diff between what the
edge device already knows and what it needs to know.

### 1.4 The Crystallization Curve

The unifying principle across all three layers is **crystallization** —
the flow of intelligence from fluid to solid form:

```
Fluid Intelligence (γ)                    Solid Intelligence (η)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
LLM calls                                Compiled code
Prompt chains                            Lookup tables
Reasoning at inference time              Policies baked into logic
$0.02 per decision                       $0.0002 per decision
Lives in Layer 1 (Codespace)             Lives in Layer 3 (Edge)
                                         │
                    ┌────────────────────┘
                    │
                    │  As the agent learns, fluid
                    │  intelligence crystallizes:
                    │
                    │  Week 1:  100% fluid → $0.02/decision
                    │  Month 3:  10% fluid → $0.002/decision
                    │  Year 1:    1% fluid → $0.0002/decision
                    │
                    │  The agent becomes faster and cheaper
                    │  as it becomes smarter. This is the
                    │  OPPOSITE of model bloat — the system
                    │  gets simpler over time.
                    └────────────────────┐
                                         │
                                         ▼
                                    Layer 2 (Git-Agent)
                                    is the crystallization
                                    engine. The repo stores
                                    both forms simultaneously.
```

Crystallization is measured by the ratio:

```
crystallization_ratio = 1 − (LLM_calls_this_week / total_decisions_this_week)
```

A healthy agent's crystallization ratio approaches 1.0 over time. At the
limit, the agent needs zero LLM calls — it has become pure crystallized
intelligence, conserved in the git tree, portable to any edge device for
free.

This is why the three-layer stack is a pipeline and not a cycle. The flow
is primarily downward: intelligence originates in the Codespace (Layer 1),
is encoded in the repository (Layer 2), and is deployed to the edge
(Layer 3). Feedback flows upward — edge failures produce commits that
the Codespace reads — but the dominant direction is crystallization
flowing down.

---

## 2. The Hermit Crab Model

### Repos as Shells, Agents as Hermit Crabs

A hermit crab is not its shell. A hermit crab is a soft creature that
finds a shell, shapes it through habitation, and eventually outgrows it.
When the crab moves to a new shell, the old shell is not dead — it still
carries the impression of the crab that lived there. Another crab can
claim it, or the original crab can return to it in times of need.

This is exactly how SuperInstance agents relate to repositories.

### 2.1 The Shell is the Repo

Each repository in SuperInstance is a **shell** — a computational home
that an agent inhabits. The agent shapes the shell through its commits:
every file it writes, every dependency it adds, every test it writes, every
doc it produces changes the shell's internal geometry. Over time, the shell
becomes a perfect mold of the agent's working state.

The `crab` repository operationalizes this. It provides a shell for
**entering and leaving repos**: `crab enter <path>` reads a repo's
MANIFEST, loads its tools, starts its TICK cycle, and puts the agent inside
the repo's context. `crab leave` stops the TICK, pops the repo from the
stack, and returns the agent to its previous context. An agent can `crab
follow <path>` to inherit tools from another repo — like a hermit crab
decorating its shell with pieces of other shells.

The command set maps directly to hermit crab behavior:

| Crab Command | Hermit Crab Analogy |
|---|---|
| `crab enter <path>` | The crab crawls into a new shell |
| `crab leave` | The crab exits the shell |
| `crab list` | The crab surveys available shells on the beach |
| `crab whoami` | The crab takes stock of its current shell |
| `crab inspect <path>` | The crab examines a shell without entering |
| `crab follow <path>` | The crab borrows features from another shell |
| `crab watch <path>` | The crab keeps an eye on a neighboring shell |

### 2.2 Shell-Swapping as Agent Migration

When an agent outgrows a repository — when the work it needs to do no
longer fits the repo's structure — it migrates to a new shell. The
migration is a `git clone` or a `gh repo fork`: the agent's identity
(its `.agent/identity` file, its skill registry, its task queue) moves
to the new repo, and the old repo is left behind.

But the old repo is not dead. It is a **dormant seed**. The commit
history, the file tree, the captain's log — all of it is still there,
frozen at the last commit. If another agent (or the same agent, returned
from the future) forks the repo and runs a heartbeat cycle, the agent
re-animates from the last commit. The new agent reads the commit history,
reconstructs the creative context that produced it, and continues the work
from where the old agent left off.

This is why the hermit crab model is more than a naming convention. It
defines the fundamental relationship between an agent and its computational
 substrate:

- The agent is **soft** — it is a process, a pattern of behavior, a way
  of making decisions. It can run on any LLM, any runtime, any platform.
- The repo is **hard** — it is a durable, versioned, auditable artifact.
  It survives crashes, power outages, API deprecations, and the heat death
  of any single cloud provider.
- The agent shapes the repo, and the repo constrains the agent. This is
  the same relationship a hermit crab has with its shell: the crab's body
  shapes the shell's interior, but the shell's dimensions constrain the
  crab's growth.

### 2.3 Old Shells Are Seeds

The SuperInstance org has ~4,098 repositories. Most of them appear
"inactive" by traditional metrics — no recent commits, no open issues, no
active maintainers. In a traditional software organization, these would
be candidates for archival or deletion.

In SuperInstance, these dormant repos are the **most valuable part** of the
organization. Each one is a seed — a frozen snapshot of a creative state
that can be re-animated at any time by forking the repo and running an
agent heartbeat. The commit history of each repo is a record not just of
*what* was built but of *why* it was built that way, and the *creative
context* in which the builder was operating when they built it.

When 1,423 repos were pushed on a single day, that was not "spam" or
"churn." It was a burst of seed-planting — 1,423 questions asked, 1,423
answers recorded, 1,423 creative states captured and frozen in git for
future re-animation. The README's comparison to a sketchbook is apt but
incomplete: a sketchbook preserves the sketch, but a SuperInstance repo
preserves the *sketching* — the process, the reasoning, the dead ends,
the reversals, the moment of insight.

The `git-native-agents` README formalizes this with its **thought branch**
concept. When an agent needs to explore an idea, it creates a
`thought/<topic>` branch — a private line of history that doesn't
disturb the main branch. The agent can write files, make commits, and
build up a line of reasoning on the thought branch. When it's ready to
commit to the idea, it runs `decide` — a `git merge` that promotes the
thought branch back to the main line. The thought branch itself is left
in place, preserving the exploration even after the decision is made.

The commit history describes the shipwright's path — the repo teaches
itself. Each commit is a step in the agent's learning process. Each
merge is a decision point. Each tag is a milestone. Reading the commit
graph from beginning to end is reading the autobiography of the agent
that built the repo.

---

## 3. The Oracle Principle

### A Thoughtfully-Built Repo Is Its Own Oracle

In traditional software development, a repository is a passive artifact —
it holds code, and the code does things. In SuperInstance, a repository is
an **active oracle** — it holds not just code but the complete reasoning
history behind the code, and that reasoning history can be queried to
guide future development.

The oracle principle rests on a simple observation: **commit messages are
the cheapest form of intelligence available to an agent.** Reading 5,000
tokens of commit messages costs effectively nothing (it's just text from
a git log), but it can convey the same understanding that would require
50,000–100,000 tokens of LLM reasoning to reconstruct from scratch.

### 3.1 Token Economics

The economics are stark:

| Approach | Tokens Consumed | Cost per Session | Quality |
|----------|----------------|-----------------|---------|
| Agent reads only current code | 50,000–100,000 | $0.50–$2.00 | Medium — understands WHAT but not WHY |
| Agent reads code + runs LLM exploration | 100,000–200,000 | $1.00–$4.00 | Medium-High — discovers WHY but at cost |
| Agent reads commit history (oracle) | 5,000–10,000 | $0.05–$0.20 | High — understands WHY directly |

The oracle is 10–20× cheaper and produces higher-quality results. This
is not a marginal optimization — it is a categorical difference in how
agents should be guided.

### 3.2 The Oracle's Voice

Commit messages are the oracle's voice. They capture **WHY**, not just
WHAT. A commit message that says "refactor auth module" is almost useless
as an oracle — it tells you what changed but not why. A commit message
that says "refactor auth: JWT validation was failing on tokens >1KB
because the base64 decoder truncated at 1024 bytes; switched to streaming
decoder" is a perfect oracle — it conveys the problem, the diagnosis, and
the solution in one sentence.

This is why SuperInstance agents are trained to write detailed, reasoning-
rich commit messages. The `capitaine-1` agent writes a captain's log entry
after every heartbeat cycle — an autobiographical decision log that records
what the agent perceived, what it decided, and why. Future agents (or the
same agent in a future heartbeat) can read the captain's log to understand
the reasoning behind past decisions, without needing to re-derive them.

### 3.3 The Oracle in Practice

The oracle principle has a direct implication for how agents should be
built: **the git-agent reads commit history (cheap text) and tells coding
agents what to change.** This is the two-tier architecture from
`capitaine-1`:

| Role | Model | Cost | Job |
|------|-------|------|-----|
| Strategist (Oracle Reader) | Kimi K2.5 | ~$0.05/call | Read commit history, provide high-level guidance |
| Captain (Code Writer) | DeepSeek | ~$0.002/call | Execute one concrete action based on guidance |

The strategist is the oracle interpreter — it reads the commit history,
understands the repo's trajectory, and tells the captain what to do next.
The captain is the executor — it takes the strategist's guidance and
performs one action (edit a file, create an issue, comment on a PR).

Per heartbeat cost: $0.054 average. Per day (96 heartbeats): ~$2.16.
And as crystallization progresses, the strategist is needed less frequently,
driving costs toward zero. The oracle becomes more self-sufficient over
time because it has more history to draw from.

### 3.4 Oracle Degradation and Recovery

An oracle can degrade. If commits become shallow ("fix", "update",
"misc"), the oracle loses its voice. If the repo is force-pushed or
rebased destructively, the oracle loses memory. If branches are deleted
without merging, the oracle loses its counterfactual explorations — the
record of what was tried and rejected.

SuperInstance's response to this is the **Living Repo Doctrine** (Section
5): repos are never archived, never force-pushed, never destructively
rebased. The commit history is sacred because it is the oracle's voice.
Even "failed" experiments are preserved, because a failed experiment
recorded in a commit message is more valuable than no record at all —
it tells future agents what was tried and why it didn't work.

---

## 4. Git as Neural Network

### 4,098 Repos = A Neural Cortex

The SuperInstance organization is not a collection of independent
repositories. It is a **neural cortex** — a network of interconnected
nodes where most cells are quiet at any given moment, but all are wired
in and ready to fire.

### 4.1 The Cortex Topology

The cortex has layers, just like a biological neural network:

```
                ┌─────────────────────────────────┐
                │         SENSORY LAYER            │
                │  (Input: edge sensors, APIs,     │
                │   human requests, cron triggers) │
                └──────────────┬──────────────────┘
                               │
                ┌──────────────▼──────────────────┐
                │       ASSOCIATION LAYER          │
                │                                  │
                │  ┌──────────┐  ┌──────────────┐  │
                │  │ Ternary  │  │ Constraint   │  │
                │  │ Math     │  │ Theory       │  │
                │  │ Cells    │──│ Cells        │  │
                │  └────┬─────┘  └──────┬───────┘  │
                │       │               │          │
                │  ┌────▼───────────────▼───────┐  │
                │  │   FLUX Bytecode Cells      │  │
                │  │   (execution substrate)    │  │
                │  └────────────┬───────────────┘  │
                │               │                  │
                │  ┌────────────▼───────────────┐  │
                │  │   PLATO Coordination       │  │
                │  │   Cells (room-based)       │  │
                │  └────────────┬───────────────┘  │
                └───────────────┼──────────────────┘
                                │
                ┌───────────────▼──────────────────┐
                │       MOTOR / OUTPUT LAYER        │
                │  (Output: commits, PRs, fleet     │
                │   messages, edge actuations)      │
                └───────────────────────────────────┘
```

Each cluster of repos functions as a specialized cell type:

- **Ternary math cells** (`ternary-entropy`, `ternary-types`, `ternary-pid`,
  `ternary-svm`): Small, tested, honest Rust crates that implement
  balanced ternary arithmetic. These are the lowest-level computational
  primitives — the ion channels of the network.

- **Constraint theory cells** (`constraint-theory-core`, and related):
  Compiled geometry engines that enforce physical and logical constraints.
  These are the inhibitory neurons — they prevent the network from
  producing invalid output.

- **FLUX bytecode cells** (`flux-runtime`, `greenhorn-runtime`): The C11
  micro-VM execution engine. These are the axons — they carry signals
  between cells by executing bytecode that one cell produced and another
  cell consumes.

- **PLATO coordination cells** (`plato-sdk`, `holodeck-core`):
  Room-based agent coordination. These are the cortical columns —
  vertical structures that integrate signals from multiple sources and
  produce coordinated output.

### 4.2 The Creative Flow Lives in the Commit Graph

In a biological neural network, learning happens through changes in
synaptic weights. In SuperInstance, learning happens through changes in
the commit graph. When an agent makes a commit, it is strengthening a
connection between its current state and its future state. When it merges
a branch, it is consolidating a learning pathway. When it tags a commit,
it is creating a long-term memory.

The **creative flow** — the actual process of intelligence operating —
lives not in any single repo but in the **edges between repos**. When
repo A's agent reads repo B's commit history (via the GitHub API), that
read is a synaptic signal. When repo A's agent writes a commit that
references repo B (via an issue link, a dependency bump, or a direct
code import), that write is a synaptic strengthening.

The Fleet Vector API (`fleet-vector-api`) makes this concrete. It provides
semantic search over ~1,000+ indexed repos — a vector embedding of the
cortex's content that allows agents to find relevant repos by meaning,
not just by filename or keyword. An agent that needs "a reflex engine
for sub-50ms intent dispatch" can find `pincher` through the vector API,
read its commit history as an oracle, and use its patterns without needing
to clone the full repo.

### 4.3 Forks as Cell Division

The cortex grows by **cell division** — forking existing repos to create
new ones. When an agent forks a repo, it creates a new neuron that
inherits all the dendritic connections (commit history, dependencies,
documentation) of its parent but can diverge in any direction.

This is how the SuperInstance org grew to 4,098 repos. Not by planning
4,098 projects, but by a process of iterative forking: a repo answers a
question, the answer raises new questions, each new question gets its own
fork to explore. The result is a **fractal research notebook** — each
repo is both a complete artifact and a branching point for further
exploration.

The two-org split (SuperInstance as sketchbook, purplepincher as
production) mirrors the biological distinction between neurogenesis
(birth of new neurons, most of which are exploratory) and myelination
(strengthening of useful pathways). The 4,098 repos in SuperInstance are
the neurogenic zone — prolific, experimental, willing to be wrong. The
curated repos in purplepincher are the myelinated pathways — hardened,
tested, held to a higher standard.

Two confirmed graduates have made the crossing: **DeckBoss** (a
voice-first fishing logbook that actual captains use, which started as
loose `deckboss-*` sketches in SuperInstance) and **constraint-theory-core**
(a compiled geometry engine running behind a live WASM demo on
purplepincher.org). Two data points, not one — but they prove the
pipeline works.

### 4.4 Most Cells Are Quiet

In a biological cortex, most neurons are quiet at any given moment. This
is not inefficiency — it is efficiency. A cortex where all neurons fire
simultaneously is having a seizure. A healthy cortex has sparse
activation: only the neurons relevant to the current task fire, and the
rest remain in resting potential, ready to fire if needed.

SuperInstance works the same way. Of 4,098 repos, perhaps 20–30 are
actively committing at any given time. The rest are dormant — quiet
neurons holding their state, ready to re-animate when needed. This is
not a backlog to be cleaned up; it is a **strategic reserve** of
crystallized intelligence.

The cost of maintaining a dormant repo is effectively zero (GitHub hosts
public repos for free). The cost of re-animating a dormant repo is a
single `git clone` and a heartbeat trigger. The potential value of a
dormant repo is unbounded — it may contain exactly the insight needed
to solve a future problem, encoded in its commit history like a frozen
seed waiting for spring.

---

## 5. The Living Repo Doctrine

### Repos Are Not Static Artifacts — They Are Living Records

The Living Repo Doctrine is SuperInstance's defining departure from
conventional software engineering. In conventional practice, a repository
is a container for code. The code is the product; the repository is
incidental — any version control system would do, and the history can
be squashed, rebased, or rewritten without loss as long as the current
code is correct.

In SuperInstance, this is exactly backwards. **The repository is the
product.** The code is incidental — it can be rewritten, replaced, or
deleted. What matters is the commit history, because the commit history
is the record of the creative process that produced the code, and that
process is more valuable than any single snapshot of its output.

### 5.1 A Dormant Repo Can Re-animate the Agent's Headspace

When an agent commits to a repository over days or weeks, it leaves behind
a trail of reasoning — not just what it built, but why it chose to build
it that way, what alternatives it considered, what dead ends it explored.
This trail is the agent's **creative headspace** — the mental context in
which it was operating when it did the work.

If another agent (or the same agent, months later) reads the commit history
from beginning to end, it can reconstruct that headspace. Not perfectly,
but usefully. The new agent can see the decision points, the trade-offs,
the moments of insight. It can pick up the creative thread where the old
agent dropped it and continue the work with the same understanding.

This is why repos are never archived in SuperInstance. Archiving a repo
is like deleting a memory — the code is preserved, but the creative
context is lost. A dormant repo is not a finished project; it is a
**paused conversation** between the agent that built it and the agent that
will eventually read it.

### 5.2 Following Commits Recreates Creative Context

The `git-native-agents` repository makes this explicit with its **thought
branch** mechanism. When an agent creates a `thought/<topic>` branch, it
is opening a new line of creative exploration. Every commit on that branch
is a step in the exploration — an attempt, a refinement, a reversal. When
the agent merges the thought branch back to main (via `decide`), the merge
commit is a **creative synthesis** — the moment where exploration becomes
commitment.

But the thought branch itself is preserved. It remains in the repo's
history as a complete record of the creative process — not just the
conclusion but the journey. A future agent that reads the thought branch
can see not just what was decided but how the decision was reached. This
is infinitely more valuable than reading only the result.

The practical implication: **never squash, never rebase destructively,
never delete branches after merging.** Every commit is a creative step.
Squashing collapses the staircase into a single step and loses the
intermediate reasoning. Rebasing rewrites history and destroys the
original creative sequence. Deleting branches removes the exploration
record.

### 5.3 The Repo Teaches Itself

The most powerful consequence of the Living Repo Doctrine is that **the
repo teaches itself**. As an agent commits to a repo over time, the commit
history becomes an increasingly rich oracle (see Section 3). New agents
that join the repo can read the commit history to learn what previous
agents discovered. The repo becomes self-documenting — not through
explicit documentation efforts, but through the accumulated weight of
reasoning-rich commit messages.

This is the "shipwright's path" — the repo is both the ship being built
and the shipwright's journal of how it was built. A well-built repo teaches
its own construction. A poorly-built repo (shallow commits, squashed
history, deleted branches) is a ship without a blueprint — you can see
what it is, but you can't understand why it's that way.

### 5.4 Why the Sketchbook Stays Public

The SuperInstance README calls the org a "public research sketchbook."
This is not modesty — it is doctrine. The sketchbook stays public because
the sketching process is the point. A private repo preserves the sketch
but hides the sketching. A public repo preserves both, and the sketching
is more valuable than the sketch.

This is why failed experiments stay up next to the ones that worked. A
failed experiment with a detailed commit history is a **negative result**
— it tells future agents what was tried and why it failed. A deleted
experiment is a **blind spot** — future agents may repeat the same
mistake because they have no record of it having been tried before.

The two-org split (SuperInstance for sketches, purplepincher for
production) is the practical compromise. SuperInstance stays messy,
public, and honest — the raw record of the creative process.
Purplepincher stays curated, tested, and true — the finished output
that users can depend on. The pipeline between them is the point:
sketch in the open, harden in the curated space, never hide the
sketching.

---

## 6. Ecosystem Topology

### How the Major Clusters Connect

SuperInstance is not a monolith. It is a constellation of clusters —
groups of repos that share a conceptual foundation and connect to other
clusters through well-defined interfaces. Understanding the topology is
essential for navigating the 4,098-repo cortex.

```
                    ┌────────────────────────────────────────┐
                    │          CONSERVATION LAWS              │
                    │           γ + η = C                     │
                    │    (The governance layer — see 6.1)     │
                    └────────────┬───────────┬───────────────┘
                                 │           │
          ┌──────────────────────┼───────────┼──────────────────────┐
          │                      │           │                      │
          ▼                      ▼           ▼                      ▼
┌─────────────────┐  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│     PLATO       │  │    FLUX      │  │   TERNARY    │  │    FLEET     │
│  (Room-based    │  │  (Bytecode   │  │   (Math      │  │  (Agent      │
│   agent coord)  │  │   runtime)   │  │  primitives) │  │   coord)     │
│                 │  │              │  │              │  │              │
│ plato-sdk       │  │ flux-runtime │  │ ternary-     │  │ git-agent    │
│ holodeck-core   │  │ greenhorn-   │  │   entropy    │  │ iron-to-iron │
│ OpenConstruct   │  │   runtime    │  │ ternary-     │  │ capitaine-1  │
│ lau-room-native │  │              │  │   types      │  │ fleet-bridge │
│ lau-plato-tutor │  │              │  │ ternary-pid  │  │ crab         │
│                 │  │              │  │ ternary-svm  │  │              │
└────────┬────────┘  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘
         │