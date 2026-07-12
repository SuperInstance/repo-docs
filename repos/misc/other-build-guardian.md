# build-guardian

**Cluster:** infra-devops  
**Language:** TypeScript  
**Source:** [SuperInstance/build-guardian](https://github.com/SuperInstance/build-guardian)

## Intention

Build Budget Guardian — tracks build resource usage, enforces budgets, detects bloat trends

## How It Works

[code]

## What It's For

Build Budget Guardian — tracks build resource usage, enforces budgets, detects bloat trends

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (330 lines, 9767 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# @superinstance/build-guardian

**Build Budget Guardian** — tracks build resource usage, enforces budgets, detects bloat trends, and integrates with any JS/TS bundler and CI pipeline.

[![npm version](https://img.shields.io/npm/v/@superinstance/build-guardian.svg)](https://www.npmjs.com/package/@superinstance/build-guardian)
[![CI](https://github.com/SuperInstance/build-guardian/actions/workflows/ci.yml/badge.svg)](https://github.com/SuperInstance/build-guardian/actions/workflows/ci.yml)

## Why?

Builds grow. Bundles bloat. Nobody notices until it's too late. Build Guardian watches your build output over time and tells you when things are getting out of hand — before your users notice.

## Features

- **Multi-bundler support** — Webpack (multi-compiler, code-split, lazy routes), Vite/Rollup, esbuild
- **Budget enforcement** — Set size, time, and memory limits per entry
- **Bloat detection** — Automatic alerts when entries grow beyond threshold
- **Configurable alerting rules** — Fail CI on growth, warn on total size, detect consecutive growth
- **Trend analysis** — Linear regression on per-entry sizes over time
- **Persistence** — Save/load build history to JSON, track per-route size over time
- **4 export formats** — Markdown, Prometheus/Grafana, Slack blocks, GitHub PR comments
- **Conservation scores** — Prioritize optimization targets by size × frequency × complexity
- **Zero dependencies** — Pure TypeScript, no runtime deps

## Install

```bash
npm install @superinstance/build-guardian
```

## Quick Start

```typescript
import { BuildBudget } from '@superinstance/build-guardian';

const budget = new BuildBudget({ bloatThreshold: 0.20 });

// Set budgets
budget.addBudget({ entry: 'dashboard', maxSizeBytes: 100 * 1024 });
budget.addBudget({ entry: 'admin/*', maxSizeBytes: 250 * 1024 });

// Record entries from your build
budget.recordEntry({
  entry: 'dashboard',
  buildTimeMs: 1200,
  sizeBytes: 78 * 1024,
  memoryPeakBytes: 150 * 1024 * 1024,
  modules: [
    { name: './Dashboard.tsx', sizeBytes: 15000 },
    { name: 'd3-full', sizeBytes: 45000 },
    { name: 'moment', sizeBytes: 18000 },
  ],
  timestamp: Date.now(),
});

// Finalize and get report
const report = budget.finalizeBuild();
console.log(report.totalSizeBytes);   // 78 * 1024
console.log(report.alerts.length);    // 0 (first build, no history)
console.log(report.violations.length); // 0 (within budget)
```

## API Reference

### `BuildBudget`

Main class for tracking build metrics.

```typescript
const budget = new BuildBudget({ bloatThreshold: 0.20 });
```

#### Methods

| Method | Description |
|--------|-------------|
| `recordEntry(metrics)` | Record metrics for a single entry |
| `finalizeBuild(label?)` | Finalize build, run detection, return `BuildReport` |
| `addBudget(budget)` | Add an entry budget |
| `setBudgets(budgets)` | Replace all budgets |
| `addAlertRule(rule)` | Add an alert rule |
| `setAlertRules(rules)` | Replace all alert rules |
| `setFrequencyEstimates(e
```
