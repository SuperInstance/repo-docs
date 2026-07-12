# exocortex-mcp-ts

## Intention
**TypeScript implementation of the Exocortex MCP server + REST API** — the web-native interface to the notebook runtime. Proves the protocol is language-independent.

## How It Works
The **Model Context Protocol** (Anthropic, 2024) is an open protocol that standardizes how applications provide context to Large Language Models. Think of it as a **USB-C port for AI applications** — a universal connector that lets any LLM client talk to any tool server.

Key concepts from the MCP specification (Anthropic, 2024; version `2024-11-05`):

| Concept | Description |
|---------|-------------|
| **Protocol** | JSON-RPC 2.0 over stdio or SSE |
| **Server** | Exposes tools, resources, an

## What It's For
**exocortex-mcp-ts** is a pure TypeScript implementation of the Exocortex notebook runtime, exposing both an **MCP (Model Context Protocol)** server and a **REST API**. It proves that the MCP protocol is language-independent — the same interface that works in Python works identically in TypeScript.

The system provides:

- **Three compute kernels** — MicroNN (2-layer MLP), Logistic Regression, and

## Who Would Use It
```bash

## Language / Stack
TypeScript

## Status Assessment
Claims production-ready with tests and documentation.

## Honest Assessment
Well-documented (817 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/exocortex-mcp-ts](https://github.com/SuperInstance/exocortex-mcp-ts)*
