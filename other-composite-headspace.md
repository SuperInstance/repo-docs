# composite-headspace

**Cluster:** misc  
**Language:** JavaScript  
**Source:** [SuperInstance/composite-headspace](https://github.com/SuperInstance/composite-headspace)

## Intention

Composite Headspace — dual-shell parallel cognitive reasoning with Symmetry-Dissonance Loop

## How It Works

the Architecture Works

1. **Two reasoning shells** are spawned by the `Coordinator`, each configured with a distinct cognitive timbre and frequency band
2. **Shell A (bass)** receives a `t-minus(5)` cue — meaning it acts after 5 cognitive beats, giving it time for deep architectural reasoning
3. **Shell B (treble)** receives a `t-minus(0)` cue — acting immediately with fast pattern matching
4. Each shell emits an **a-box** (cognitive artifact) containing its analysis
5. The **Symmetry-Dissonance Loop** compares both a-boxes, finding divergence points, classifying symmetry breaks, and fusing t

## What It's For

Composite Headspace — dual-shell parallel cognitive reasoning with Symmetry-Dissonance Loop

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

JavaScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (384 lines, 15572 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# 🧠 Composite Headspace

**Symphony of Shells — Cognitive DAW Prototype**

[![npm version](https://img.shields.io/npm/v/@superinstance/composite-headspace)](https://www.npmjs.com/package/@superinstance/composite-headspace)
[![Tests: 51/51](https://img.shields.io/badge/tests-51%2F51-passing-brightgreen)](https://github.com/SuperInstance/composite-headspace)
[![Node ≥18](https://img.shields.io/badge/node-%3E%3D18-339933?logo=node.js)](https://nodejs.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

---

## Quick Start

```bash
git clone https://github.com/SuperInstance/composite-headspace && cd composite-headspace && npm install && node cli.js --sample 1
```

---

## What This Solves

Complex reasoning problems demand **multiple cognitive modes** operating in parallel. Human thinkers naturally oscillate between deep architectural analysis (first principles, trade-offs, invariants) and fast pattern matching (analogies, metaphors, structural recognition). This oscillation is the engine of genuine insight.

**Composite Headspace** is a cognitive orchestration framework that formalizes this process by running **two parallel reasoning shells** — one tuned for slow, deep architectural reasoning (bass frequency) and one tuned for fast, associative pattern matching (treble frequency) — coordinated through a **t-minus cueing protocol** that aligns their outputs at precise cognitive beats. The resulting symmetry-dissonance analysis fuses both perspectives into a synthetic insight that neither shell could produce alone.

> *"When deep reasoning and fast pattern matching converge, you get understanding that is both rigorous and intuitive."*

**Use cases:**
- **Architectural decision-making** — Evaluate trade-offs through dual lenses
- **Debug triage** — Combine systematic protocol analysis with pattern-led root cause detection
- **Design reviews** — Cross-validate intuitions against first-principles reasoning
- **Cognitive augmentation** — Externalize the stereo reasoning process that great thinkers use internally

---

## Architecture

```
                          ┌─────────────────────────────────────┐
                          │      T-Minus WebSocket Dispatcher    │
                          │           (port 9090)                │
                          └──────────┬──────────────┬───────────┘
                                     │              │
                         t-minus(5)  │              │ t-minus(0)
                                     ▼              ▼
        ┌─────────────────────────────┐  ┌─────────────────────────────┐
        │  Shell A  (α · Bass)        │  │  Shell B  (β · Treble)      │
        │  Timbre: deep-architect     │  │  Timbre: fast-pattern-matcher│
        │  Frequency: 0.01–0.1 Hz     │  │  Frequency: 1–10 Hz          │
        │  Latency: ~1500ms           │  │  Latency: ~200ms             │
        │  Token Budget: 128K         │  │  Token Budget: 32K           │
        │  Model: DeepSeek
```
