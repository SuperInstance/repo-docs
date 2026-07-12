# casting-call-mcp

**Cluster:** cs-implementations  
**Language:** Python  
**Source:** [SuperInstance/casting-call-mcp](https://github.com/SuperInstance/casting-call-mcp)

## Intention

MCP server: consultative database for model casting decisions — choose the right model, temperature, and prompt prefix for any task

## How It Works

It Fits

The model selection layer for the [SuperInstance fleet](https://github.com/SuperInstance). Ensures the right model handles the right task.

- **[cocapn-sdk](https://github.com/SuperInstance/cocapn-sdk)** — Routes to selected models
- **[casting-call-gpu](https://github.com/SuperInstance/casting-call-gpu)** — GPU-accelerated casting math
- **[Claude-PRISM-CF](https://github.com/SuperInstance/Claude-PRISM-CF)** — Edge model routing

## What It's For

MCP server: consultative database for model casting decisions — choose the right model, temperature, and prompt prefix for any task

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** moderate
- **Note:** Moderate docs (75 lines, 2200 chars). Some substance.

## Honest Assessment

Moderate documentation with some implementation detail. Likely AI-assisted creation within the fleet ecosystem. Real code but may lack independent testing or production use.