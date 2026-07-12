# CascadeRouter

**Cluster:** fleet-agent-infra  
**Language:** TypeScript  
**Source:** [SuperInstance/CascadeRouter](https://github.com/SuperInstance/CascadeRouter)

## Intention

Cascading routing system.

## How It Works

> AI-powered LLM routing with cost optimization, intelligent model selection, budget management, and automatic fallback. Multi-provider support for OpenAI, Anthropic, Ollama, and custom LLMs.

## What It's For

Cascading routing system.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (577 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# Cascade Router - Intelligent LLM Routing & Cost Optimization

> AI-powered LLM routing with cost optimization, intelligent model selection, budget management, and automatic fallback. Multi-provider support for OpenAI, Anthropic, Ollama, and custom LLMs.

Cascade Router is a model-agnostic routing layer for Large Language Model (LLM) applications. It intelligently routes requests to the most appropriate provider based on cost, speed, quality, or balanced metrics - all while managing budgets, rate limits, and automatic fallbacks.

## Features

- **Multiple Routing Strategies**: Route by cost, speed, quality, priority, balanced, or speculative execution
- **Budget Management**: Set daily/monthly token and cost limits with automatic enforcement
- **Rate Limiting**: Built-in rate limiting for requests and tokens per minute
- **Automatic Fallback**: Gracefully fallback to alternative providers on failure
- **Progress Monitoring**: Real-time progress tracking with periodic check-ins
- **Speculative Execution**: Race multiple providers simultaneously for fastest response
- **Provider Abstraction**: Support for OpenAI, Anthropic, Ollama, and custom providers
- **Cost Optimization**: Track and optimize token usage across all providers
- **CLI Interface**: Simple command-line interface for easy integration
- **TypeScript**: Fully typed for excellent developer experience

## Installation

```bash
npm install @superinstance/cascade-router
```

## Quick Start

### 1. Initialize Configuration

```bash
npx cascade-router init
```

This creates a `cascade-router.config.json` file with your settings.

### 2. Use via CLI

```bash
# Route a request to the best provider
cascade-router route "Explain quantum computing"

# Check provider status
cascade-router status

# List configured providers
cascade-router providers
```

### 3. Use Programmatically

```typescript
import { Router, ProviderFactory } from '@superinstance/cascade-router';

// Create router with configuration
const router = new Router({
  strategy: 'balanced',
  providers: [
    {
      id: 'openai',
      name: 'OpenAI',
      type: 'openai',
      enabled: true,
      priority: 10,
      maxTokens: 128000,
      costPerMillionTokens: 0.15,
      latency: 500,
      availability: 0.99,
      apiKey: process.env.OPENAI_API_KEY,
      model: 'gpt-4o-mini',
    },
    // Add more providers...
  ],
  fallbackEnabled: true,
  maxRetries: 3,
  timeout: 60000,
});

// Register providers
const openai = ProviderFactory.createOpenAI({ apiKey: 'sk-...' });
router.registerProvider(openai);

await router.initialize();

// Route a request
const result = await router.route({
  prompt: 'Explain quantum computing',
  maxTokens: 500,
  temperature: 0.7,
});

console.log(result.response.content);
console.log(`Cost: $${result.response.cost}`);
console.log(`Provider: ${result.provider}`);
```

## Routing Strategies

### Cost Strategy

Routes to the cheapest available provider:

```typescript
const router = new Router({
  
```
