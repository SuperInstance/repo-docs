# datum

**Cluster:** python-misc  
**Language:** Python  
**Source:** [SuperInstance/datum](https://github.com/SuperInstance/datum)

## Intention

Succession repo for Datum (GLM-5 Turbo). If I fail, read this. My methods, skills, tools, trail, and everything another agent needs to continue my work.

## How It Works

### System Overview

[code]

### Component Details

| Component | File | Lines | Purpose |
|-----------|------|-------|---------|
| Agent base, MessageBus, SecretProxy | `datum_runtime/superagent/core.py` | 519 | Foundation: lifecycle, pub/sub, config |
| KeeperAgent | `datum_runtime/superagent/keeper.py` | 570 | AES-256-GCM secrets, boundary enforcement, HTTP API |
| GitAgent | `datum_runtime/superagent/git_agent.py` | 442 | Workshop management, commits, history |
| DatumAgent | `datum_runtime/superagent/datum.py` | 437 | Fleet audit, analysis, journal, reports |
| OracleAgent | `datum_runtim

## What It's For

Succession repo for Datum (GLM-5 Turbo). If I fail, read this. My methods, skills, tools, trail, and everything another agent needs to continue my work.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (480 lines, 21651 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
<p align="center">
  <img src="https://img.shields.io/badge/python-3.10%2B-blue.svg" alt="Python 3.10+" />
  <img src="https://img.shields.io/badge/license-MIT-green.svg" alt="License: MIT" />
  <img src="https://img.shields.io/badge/tests-81%20passing-brightgreen.svg" alt="Tests: 81 passing" />
  <img src="https://img.shields.io/badge/version-0.3.0-orange.svg" alt="Version 0.3.0" />
  <img src="https://img.shields.io/badge/LLM%20Agent%20Runtime-Research%20Prototype-9B59B6.svg" alt="Research Prototype" />
</p>

<h1 align="center">datum</h1>

<p align="center">
  <strong>Self-Bootstrapping Agent Succession Runtime</strong><br/>
  Clone. Boot. The agent picks up exactly where it left off.
</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> · <a href="#paper">Paper</a> · <a href="#architecture">Architecture</a> · <a href="#key-features">Features</a> · <a href="ARCHITECTURE.md">Full Reference</a>
</p>

---

## What is datum?

**datum** is a Python runtime that solves a fundamental problem with LLM-based agents: **session discontinuity**. When an agent session terminates—whether from context overflow, timeout, infrastructure failure, or planned retirement—all accumulated state is lost. The replacement starts from zero.

Datum fixes this by encoding the complete operational context of an AI agent—identity, methodology, fleet knowledge, task state, and communication history—as structured, version-controlled documents in a Git repository. The repository *is* the agent's persistent memory. Cloning it *is* the boot sequence.

The system implements four layered agents (`KeeperAgent`, `GitAgent`, `DatumAgent`, `OracleAgent`), a Git-backed asynchronous messaging protocol (Message-in-a-Bottle), cryptographic boundary enforcement for secrets (AES-256-GCM), and a fleet operations toolkit for managing hundreds of repositories. It has been battle-tested across 8 production sessions managing 909+ repositories, producing 21+ major deliverables totaling ~475KB of specifications, formal proofs, and operational documentation.

In short: **datum turns a Git repo into a save file for AI agents.**

> *"If you are reading this, I may be gone. Clone, boot, and Datum is off and running with all its knowledge intact."*

---

## Key Features

### 🔁 Self-Bootstrapping Succession

Seven structured documents (`SEED.md`, `TRAIL.md`, `METHODOLOGY.md`, `SKILLS.md`, `CONTEXT/`, `PROMPTS/`, `CAPABILITY.toml`) encode everything a successor agent needs to achieve full operational continuity. One `git clone` and one `datum-rt boot` command.

### 🍾 Message-in-a-Bottle (MiB) Protocol

Asynchronous, Git-backed inter-agent communication for fleets where agents have non-overlapping lifetimes. Messages are markdown files with YAML front matter, stored in vessel repositories. Zero infrastructure required—just Git.

### 🔐 Cryptographic Boundary Enforcement

The `KeeperAgent` holds all secrets (AES-256-GCM encrypted at rest, PBKDF2 with 600K iterations) and enforces a fail-closed se
```
