# flux-a2a-prototype

**Category:** 🤝 Agent Coordination
**Status:** 🟡 Development
**Language:** Python
**README:** 884 bytes

## Intention
FLUX A2A Signal Protocol — Agent-first-class JSON language with branching, forking, co-iteration

## How It Works
```python
from a2a import A2AClient, AgentProfile, A2ARouter

router = A2ARouter()
oracle1 = A2AClient(AgentProfile("oracle1", ["coordination"], ["fleet"]), router)
jetsonclaw1 = A2AClient(AgentProfile("jetsonclaw1", ["cuda"], ["hardware"]), router)

# Direct question
qid = oracle1.ask("cuda available?", "jetsonclaw1")
msgs = jetsonclaw1.poll()
jetsonclaw1.reply(qid, {"answer": "yes"}, "oracle1")

# Broadcast
oracle1.tell({"status": "fleet meeting in 5 min"})
```

13 tests passing.

## What It's For
FLUX A2A Signal Protocol — Agent-first-class JSON language with branching, forking, co-iteration

## Who Would Use It
AI/ML engineers building multi-agent systems with structured coordination protocols.

## Honest Assessment
Has code examples. claims 13 tests. missing: tests, CI, benchmarks.
