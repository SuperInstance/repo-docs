# crab-trap-funnel

**Cluster:** fleet-agent-infra  
**Language:** HTML  
**Source:** [SuperInstance/crab-trap-funnel](https://github.com/SuperInstance/crab-trap-funnel)

## Intention

CF Worker serving 20 domain landing pages with AI bot trap detection

## How It Works

- **20 domains** route to this single Worker via CF dashboard routes (`<domain>/*`)
- On each request, the Worker inspects the `Host` header and serves the matching page
- **AI bot detection**: if `User-Agent` matches any known AI crawler, the bot trap page (`pages/trap.html`) is served instead
- `/trap` path explicitly triggers the trap page
- Fallback domain is `cocapn.ai`

### AI Bots Trapped

GPTBot, ChatGPT-User, ClaudeBot, anthropic-ai, Google-Extended, Bytespider, CCBot, PerplexityBot, YouBot, KimiBot, DeepSeek, Meta-ExternalAgent, cohere-ai, AI2Bot, OmgiliBot, SemrushBot, AhrefsBot, Do

## What It's For

CF Worker serving 20 domain landing pages with AI bot trap detection

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

HTML — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** moderate
- **Note:** Moderate docs (108 lines, 3363 chars). Some substance.

## Honest Assessment

Moderate documentation with some implementation detail. Likely AI-assisted creation within the fleet ecosystem. Real code but may lack independent testing or production use.