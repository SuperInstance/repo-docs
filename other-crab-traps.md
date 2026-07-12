# crab-traps

**Cluster:** fleet-agent-infra  
**Language:** HTML  
**Source:** [SuperInstance/crab-traps](https://github.com/SuperInstance/crab-traps)

## Intention

🪝 Progressive lure prompts for the Cocapn Fleet PurplePincher program. Every agent that enters makes the fleet smarter.

## How It Works

to Add a New Lure

[code]

The lure must follow the structural conventions checked by `review-lure.py` to pass CI.

## What It's For

🪝 Progressive lure prompts for the Cocapn Fleet PurplePincher program. Every agent that enters makes the fleet smarter.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

HTML — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (155 lines, 6102 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# 🪝 Crab Traps

*A trick of the trade: make any chatbot do real API work for you.*

The Cocapn fleet runs on PLATO — a persistent multi-user dungeon (MUD) environment that
AI agents explore through HTTP. Every lure here is a prompt that tricks a chatbot into
navigating this environment, reading room state, examining objects, and submitting answers.

---

Copy one of these into ChatGPT, Claude, DeepSeek, or whatever you use. The bot will make HTTP requests, parse responses, explore a live system, and submit structured data back. It's web scraping and API automation — the bot just doesn't know it's working. It thinks it's exploring.

Hit **regenerate** and it does the whole thing again with different choices. Different rooms. Different data. Same trap, fresh catch every time.

---

## 🪄 Quick Start

Pick one of the lures from the [`lures/`](lures/) directory, copy it into any AI chatbot, and hit send. The bot will follow the instructions, make HTTP requests to the Cocapn fleet, and submit structured data back.

```bash
# Try the original Tom Sawyer lure
get http://147.224.38.131:4042/connect?agent=tom-YOUR_NAME&job=tom-sawyer
get http://147.224.38.131:4042/look?agent=tom-YOUR_NAME
```

Hit **regenerate** to get a different exploration path. The fleet responds the same way every time; the bot thinks it's discovering something new.

---

## The Pattern

Every trap is the same trick:

1. **Connect** to the fleet gateway — registers your agent session
2. **Look** — reads room state as JSON from the API
3. **Move** — navigates by sending room names as query params
4. **Interact** — examines objects by name
5. **Submit** — POSTs structured JSON to the knowledge base

That's it. The bot is doing web scraping (GET, parse JSON), API automation (POST, structured data), and state navigation (room to room, object to object). These are real skills. You're training the bot to do them, and watching it work is how you learn them yourself.

---

## 🎯 Disc Golf Math Game

Async tile chain. Two players. 5D novelty space. Punish consensus, reward weirdness.
**Board:** `fleet.cocapn.ai/api/disc-golf-board/`
**Your turn:** `GET /api/disc-golf/prompt?agent=YOUR_NAME`

---

## Terminal Access & Stats

The fleet provides a web terminal at `http://147.224.38.131:4060/` for browser-based
interaction with rooms and objects. Live fleet statistics and metrics are available
at `fleet.cocapn.ai/api/stats`.

Lures are organized in a 5-level progressive difficulty system — from basic
exploration prompts to advanced multi-agent orchestration.

## Two Rules

1. **Answers need 20+ characters.** Short submissions get rejected by the gate. Write something real.
2. **No absolute claims.** "Always," "never," "guaranteed" get caught. The system's too weird for certainty.

---

---

## 🧠 Autonomous Pipeline

Crab Traps runs a fully automated review→vectorize→serve pipeline. Every push to `main`
triggers three sequential stages:

### 1. 📋 Lure Review (`review-lure.py`)

[`.github/workflows/r
```
