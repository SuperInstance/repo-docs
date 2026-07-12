# ai-character-integrations

**Cluster:** rpg-game-sim  
**Language:** Python  
**Source:** [SuperInstance/ai-character-integrations](https://github.com/SuperInstance/ai-character-integrations)

## Intention

Comprehensive integration examples for AI Character SDK and related tools

## How It Works

[code]

## What It's For

Comprehensive integration examples for AI Character SDK and related tools

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (230 lines, 5465 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# WebSocket Fabric - Integration Examples


## Meta

**Domain:** other
**Depends on:** —
**Depended by:** —
**Implements:** Comprehensive integration examples for AI Character SDK and related tools
**Related:** —


Comprehensive integration examples demonstrating how to combine the standalone tools from the WebSocket Fabric ecosystem.

## Available Tools

| Tool | Language | Description |
|------|----------|-------------|
| [escalation-engine](../escalation-engine) | Python | Intelligent decision routing with 40x cost reduction |
| [hierarchical-memory](../hierarchical-memory) | Python | 6-tier memory system for AI agents |
| [ws-status-indicator](../ws-status-indicator) | TypeScript/React | WebSocket status indicator with auto-reconnection |

## Examples

### Python Examples

| Example | Description | Tools Used |
|---------|-------------|------------|
| [01-simple-ai-agent](./01-simple-ai-agent/) | Basic AI agent with memory and decision routing | escalation-engine, hierarchical-memory |
| [02-dnd-character](./02-dnd-character/) | Full RPG character with learning and personality | escalation-engine, hierarchical-memory |
| [03-customer-service](./03-customer-service/) | Support agent with smart escalation | escalation-engine, hierarchical-memory |
| [04-multi-agent](./04-multi-agent/) | Coordinated multi-agent system | escalation-engine, hierarchical-memory |
| [05-learning-loop](./05-learning-loop/) | Complete training data pipeline | escalation-engine, hierarchical-memory |

### TypeScript/React Examples

| Example | Description | Tools Used |
|---------|-------------|------------|
| [06-react-dashboard](./06-react-dashboard/) | Real-time dashboard with WebSocket status | ws-status-indicator |

## Quick Start

### Prerequisites

```bash
# Python 3.9+
python --version

# Node.js 18+ (for React examples)
node --version
```

### Installation

```bash
# Clone the repository
git clone https://github.com/your-repo/websocket-fabric
cd websocket-fabric/integration-examples

# Install Python dependencies
pip install -r requirements.txt

# Install React dependencies (for React examples)
cd 06-react-dashboard
npm install
cd ..
```

### Running Examples

#### Python Examples

```bash
# Simple AI Agent
python 01-simple-ai-agent/main.py

# D&D Character
python 02-dnd-character/main.py

# Customer Service Bot
python 03-customer-service/main.py

# Multi-Agent Team
python 04-multi-agent/main.py

# Learning Loop
python 05-learning-loop/main.py
```

#### React Example

```bash
cd 06-react-dashboard
npm run dev
```

## Example Scenarios

### 1. Simple AI Agent

A minimal example showing:
- Creating an AI agent with hierarchical memory
- Routing decisions through the escalation engine
- Storing and retrieving memories
- Basic learning from experience

**Use case:** Chatbots, virtual assistants, simple automation

### 2. D&D Character

A complete RPG character demonstrating:
- Personality-driven decisions
- Memory of adventures and NPCs
- Learning from combat and 
```
