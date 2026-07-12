# Claude-Abstraction

**Cluster:** python-misc  
**Language:** Python  
**Source:** [SuperInstance/Claude-Abstraction](https://github.com/SuperInstance/Claude-Abstraction)

## Intention

Abstraction layer for Claude API.

## How It Works

Principles

- **Zero dependencies** — only uses Python stdlib (+ pytest for tests)
- **Dataclasses throughout** — clean, typed, immutable-friendly
- **Composable by default** — every core type supports `+` operator
- **Framework agnostic** — no coupling to any specific LLM API

## What It's For

Abstraction layer for Claude API.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (146 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# Claude Abstraction

Abstraction layers and prompt engineering patterns for managing LLM complexity.

## Installation

```bash
pip install -e .
```

For development:
```bash
pip install -e ".[dev]"
```

## Quick Start

### AbstractionLayer — Nested Context

Compose layers of instructions, examples, and constraints:

```python
from claude_abstraction import AbstractionLayer

system = AbstractionLayer(
    "system",
    instructions="You are a helpful assistant.",
    constraints=["Be concise", "No hallucinations"],
)
persona = AbstractionLayer("persona", instructions="Speak like a pirate.")

merged = system + persona
print(merged.render())

# Use as context manager
with AbstractionLayer("session", instructions="Focus on Python."):
    # layer is active
    pass
```

### PromptTemplate — Variables & Conditionals

```python
from claude_abstraction import PromptTemplate

tpl = PromptTemplate(
    "review",
    "Review this {{language}} code:
{{code}}{{#if strict}}
Be extra strict.{{/if}}",
    defaults={"language": "Python"},
)

print(tpl.render(code="def foo(): pass", strict=True))
# "Review this Python code:
def foo(): pass
Be extra strict."

# Compose templates
header = PromptTemplate("header", "You are {{role}}.

")
body = PromptTemplate("body", "Task: {{task}}")
full = header + body
print(full.render(role="reviewer", task="Find bugs"))
```

### PromptChain — Sequential Pipelines

```python
from claude_abstraction import PromptChain, PromptTemplate

chain = (
    PromptChain("analyze")
    .step(PromptTemplate("extract", "Extract key facts from:
{{input}}"))
    .step(PromptTemplate("summarize", "Summarize concisely:
{{extract_output}}"))
)

results = chain.run(input="Long text about quantum computing...")
# Each step's output is available as {step_name}_output in subsequent steps

for r in results:
    print(f"[{r.step_name}] {r.output}")
```

### PromptRouter — Query Routing

```python
from claude_abstraction import PromptRouter, PromptTemplate

router = PromptRouter()
router.add("code", {"code", "function", "debug"}, PromptTemplate("code", "Code: {{input}}"))
router.add("chat", {"chat", "talk"}, PromptTemplate("chat", "Chat: {{input}}"))
router.set_default(PromptTemplate("general", "General: {{input}}"))

handler, route = router.route("Help me debug this function")
print(route)  # "code"

# Or render directly
print(router.render("Let's chat about weather", input="weather"))
```

### PromptOptimizer — Compression & Analysis

```python
from claude_abstraction import PromptOptimizer

opt = PromptOptimizer()

result = opt.optimize(
    "In order to write good code, please note that you should "
    "test test your your code code."
)
print(f"Saved {result.savings_pct}% ({result.original_chars} → {result.optimized_chars} chars)")
for suggestion in result.suggestions:
    print(f"  - {suggestion}")
```

## API Reference

| Class | Description |
|-------|-------------|
| `AbstractionLayer` | Nested, composable layers of prompt context |
| `PromptTemp
```
