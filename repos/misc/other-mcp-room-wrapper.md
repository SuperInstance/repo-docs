# mcp-room-wrapper

## Intention

Wrap any MCP server as a Plato room for automatic observation and distillation

## How It Works

This library wraps any MCP server, intercepts all model calls, logs choices and reasoning, and builds up observation data for automatic distillation into tiny experts via a Mixture-of-Experts (MoE) architecture.
- **McpRoom** — wraps an MCP endpoint, collecting perception data (observed calls) and prediction data
- **McpTick** — a single observed model call with prompt, options, chosen answer, reasoning, and metadata
- **DecisionPoint** — identified decision patterns in the MCP workflow
- **ExpertType** — Classifier, Selector, Generator, Router, Validator, or Synthesizer
- **DistillationPipeline** — orchestrates the full pipeline: Observe → Analyze → Train → Validate → Deploy → Monitor
```rust
use mcp_room_wrapper::{McpRoom, McpTick, DistillationPipeline};
// Wrap an MCP server
let mut room = McpRoom::wrap("http://localhost:8080/mcp");
// Intercept calls
room.intercept_call(tick);
// Analyze decision points
let analysis = room.analyze();
// Or use the full pipeline

## What It's For

Wrap any MCP server as a Plato room for automatic observation and distillation

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: LIGHT**

Short README (25 lines), includes examples.

- README length: 38 lines, 1364 characters
- Documented sections: What It Does, Core Concepts, Usage, Zero Dependencies

## Honest Assessment

Some documentation exists but it's not comprehensive. The project may have working code, but the README doesn't provide enough evidence of maturity, testing, or real-world use. **Promising direction, needs more evidence of substance.**
