# abstraction-planes

**Cluster:** python-misc  
**Language:** Python  
**Source:** [SuperInstance/abstraction-planes](https://github.com/SuperInstance/abstraction-planes)

## Intention

The Middle Way — decompose ideas to their optimal abstraction plane, not all the way to bytecode

## How It Works

[code]

### Decomposition Pipeline

[code]

Each step evaluates quality. Decomposition **stops** when quality improvement drops below threshold (diminishing returns detected).

### FLUX Opcodes Reference

[code]

## What It's For

The Middle Way — decompose ideas to their optimal abstraction plane, not all the way to bytecode

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (183 lines, 5301 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
**Topics:** `abstraction` `decomposition` `intent-resolution` `plane-analysis` `system-design` `multi-level-synthesis` `cocapn`

---

# Abstraction Planes

> Simplify complex systems with a 6-plane stack — from Intent to Metal. Find the sweet spot where abstraction meets execution.

**Abstraction Planes** is a framework for decomposing natural language intents into executable code at the right level of abstraction. It identifies the **optimal plane** (the sweet spot where further decomposition gives diminishing returns) and provides the decomposition path from Intent down to Bare Metal.

Part of the [Cocapn fleet](https://github.com/SuperInstance) — lighthouse keeper architecture.

---

## The 6-Plane Stack

| Plane | Name | What It Looks Like | Example |
|-------|------|-------------------|---------|
| **5** | Intent | Natural language | "navigate east 10 knots, alert if reactor overheats" |
| **4** | Domain Language | FLUX-ese, maritime vocab, structured notation | `GAUGE reactor > 100 → ALERT "overheat"` |
| **3** | Structured IR | JSON AST, types, lock annotations | `{"op":"GAUGE","args":[reactor,100]}` |
| **2** | Bytecode | FLUX opcodes in hex | `0x90 0x64 0x00 0x91` |
| **1** | Native | C / Rust / Zig source | `if (gauge(reactor) > 100) alert();` |
| **0** | Bare Metal | Assembly, machine code, firmware | `MOV R1, [reactor_addr]` |

**Plane 4 is the sweet spot** — most intents decompose cleanly to domain language and stop there. Going deeper only matters when targeting specific hardware (ESP32, Jetson, Pi).

---

## Quick Start

### Install

```bash
pip install .
# or
pip install git+https://github.com/SuperInstance/abstraction-planes.git
```

### Run the Analyzer

```bash
# Auto-detect optimal plane
python -m abstraction_planes "navigate east 10 knots, monitor reactor"

# Target specific hardware
python -m abstraction_planes --target esp32 "read temperature sensor"
python -m abstraction_planes --target jetson "run object detection pipeline"
python -m abstraction_planes --target cloud "coordinate fleet agents"
```

### Programmatic Usage

```python
from abstraction_planes import find_optimal_plane

result = find_optimal_plane(
    "navigate east 10 knots, alert if reactor overheats",
    target="jetson"
)

print(f"Optimal plane: {result['optimal_plane']}")
# e.g. Optimal plane: 2
```

---

## Architecture

```
abstraction-planes/
├── README.md
├── ABSTRACTION.md              # Framework definition
├── CHARTER.md
├── DOCKSIDE-EXAM.md
├── STATE.md
├── LICENSE
├── pyproject.toml
├── plane_analyzer.py          # Main CLI + library entry point
├── src/
│   └── abstraction_planes/
│       ├── __init__.py        # Core plane analyzer
│       └── ...
├── tests/
└── dist/                      # Built package
```

### Decomposition Pipeline

```
Intent (Plane 5)
    │
    ▼  [DeepSeek / SiliconFlow Qwen]
Plane 4 — FLUX-ese domain language
    │
    ▼  [DeepSeek]
Plane 3 — Structured JSON IR
    │
    ▼  [DeepSeek]
Plane 2 — FLUX bytecode (hex)
    │
```
