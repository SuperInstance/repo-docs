# cost-analysis

**Cluster:** data-analytics  
**Language:** TypeScript  
**Source:** [SuperInstance/cost-analysis](https://github.com/SuperInstance/cost-analysis)

## Intention

Tool to analyze and track costs effectively.

## How It Works

[![npm version](https://badge.fury.io/js/%40luciddreamer%2Fcost-analysis.svg)](https://www.npmjs.com/package/@luciddreamer/cost-analysis)

## What It's For

Tool to analyze and track costs effectively.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (357 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# @luciddreamer/cost-analysis

[![npm version](https://badge.fury.io/js/%40luciddreamer%2Fcost-analysis.svg)](https://www.npmjs.com/package/@luciddreamer/cost-analysis)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Multi-provider cost visualization and analysis dashboard for AI API usage with real-time tracking, forecasting, and optimization insights.

## Features

- **Cost Breakdown** - Visualize costs by provider, model, and usage
- **Time-Series Analysis** - Track costs over time with detailed metrics
- **Cost Forecasting** - Predict future costs with confidence intervals
- **Provider Comparison** - Compare providers and identify savings opportunities
- **Budget Tracking** - Monitor spending against budgets with alerts
- **Token Analysis** - Understand token usage patterns
- **Interactive Charts** - Responsive visualizations with Recharts
- **Dark/Light Theme** - Built-in theme support
- **TypeScript Support** - Full type definitions included

## Installation

```bash
npm install @luciddreamer/cost-analysis
# or
yarn add @luciddreamer/cost-analysis
# or
pnpm add @luciddreamer/cost-analysis
```

## Quick Start

```tsx
import React, { useState, useEffect } from 'react';
import { CostAnalysis } from '@luciddreamer/cost-analysis';

function App() {
  const [costData, setCostData] = useState(null);

  useEffect(() => {
    // Fetch cost data from your API
    const fetchCostData = async () => {
      const response = await fetch('/api/costs');
      const data = await response.json();
      setCostData(data);
    };

    fetchCostData();
  }, []);

  return (
    <CostAnalysis
      costData={costData}
      forecast={{
        period: 'Next 30 days',
        projectedCost: 450.00,
        confidence: 0.85,
        factors: {
          trend: 'increasing',
        },
      }}
      comparison={{
        providers: ['OpenAI', 'Anthropic', 'Google'],
        costs: [320.50, 285.30, 410.80],
        savings: {
          provider: 'Anthropic',
          amount: 35.20,
          percentage: 11.0,
        },
      }}
      theme="dark"
    />
  );
}
```

## Components

### CostAnalysis

Main dashboard component aggregating all cost analysis features.

**Props:**

- `costData: CostBreakdown` - Cost breakdown data
- `forecast?: CostForecast` - Cost forecast data
- `comparison?: CostComparison` - Provider comparison data
- `onProviderClick?: (provider: string) => void` - Provider click handler
- `theme?: 'light' | 'dark'` - Color theme (default: 'dark')

### CostBreakdownChart

Bar and pie charts showing cost distribution by provider.

**Props:**

- `data: ProviderCost[]` - Array of provider cost data
- `showTokens?: boolean` - Show token counts (default: false)
- `showRequests?: boolean` - Show request counts (default: false)
- `animated?: boolean` - Enable animations (default: true)

### CostTimeline

Time-series chart showing cost trends with optional forecast.

**Props:**

- `data: CostDataPoi
```
