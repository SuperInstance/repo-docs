# Bayesian-Multi-Armed-Bandits

**Cluster:** math-research  
**Language:** TypeScript  
**Source:** [SuperInstance/Bayesian-Multi-Armed-Bandits](https://github.com/SuperInstance/Bayesian-Multi-Armed-Bandits)

## Intention

Library for Bayesian multi-armed bandits.

## How It Works

> **Bayesian multi-armed bandit algorithms for intelligent A/B testing and optimization**

## What It's For

Library for Bayesian multi-armed bandits.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (405 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# @superinstance/bayesian-multi-armed-bandits

> **Bayesian multi-armed bandit algorithms for intelligent A/B testing and optimization**

[![TypeScript](https://img.shields.io/badge/TypeScript-5.6-blue)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![npm version](https://img.shields.io/npm/v/@superinstance/bayesian-multi-armed-bandits.svg)](https://www.npmjs.com/package/@superinstance/bayesian-multi-armed-bandits)

A powerful TypeScript library for A/B testing and optimization using multi-armed bandit algorithms with Bayesian statistical analysis. Automatically balances exploration and exploitation to maximize rewards while minimizing regret.

## ✨ Features

- 🎰 **4 Bandit Algorithms** - Epsilon-Greedy, UCB1, Thompson Sampling, Adaptive
- 📊 **Bayesian Analysis** - Posterior distributions, credible intervals, probability of being best
- 🎯 **Adaptive Allocation** - Dynamically optimize traffic allocation based on performance
- 🚀 **Production Ready** - Zero dependencies, fully typed, battle-tested
- 📈 **Algorithm Comparison** - Built-in tools to compare algorithms
- 🔧 **Highly Configurable** - Exploration rates, confidence levels, temperature parameters

## 🚀 Quick Start

### Installation

```bash
npm install @superinstance/bayesian-multi-armed-bandits
```

### Basic Usage

```typescript
import { MultiArmedBandit } from '@superinstance/bayesian-multi-armed-bandits';

// Define your variants
const variants = [
  { id: 'control', name: 'Control', weight: 1, config: {}, isControl: true },
  { id: 'variant_a', name: 'Variant A', weight: 1, config: {} },
  { id: 'variant_b', name: 'Variant B', weight: 1, config: {} },
];

// Create bandit with Thompson Sampling (recommended)
const bandit = new MultiArmedBandit({
  algorithm: 'thompson-sampling',
  minPullsPerVariant: 10,
});

// Run experiment
for (let i = 0; i < 1000; i++) {
  // Select variant
  const selection = bandit.selectVariant(variants);
  console.log(`Selected: ${selection.variantId}`);

  // Show variant to user and get reward
  const reward = await showVariantAndGetReward(selection.variantId);
  // Reward: 0-1 for binary (success/failure), or any continuous value

  // Update bandit
  bandit.updateReward(selection.variantId, reward);
}

// Get best variant
const bestVariant = bandit.getBestVariant();
console.log(`Best variant: ${bestVariant}`);

// Check convergence
if (bandit.hasConverged()) {
  console.log('Experiment converged!');
}

// Get statistics
const stats = bandit.getArmStatistics();
console.log('Statistics:', stats);
```

## 📖 Algorithms

### 1. Epsilon-Greedy

Simple exploration vs exploitation strategy:
- With probability ε: explore (random variant)
- With probability 1-ε: exploit (best variant)

**Best for:** Low-traffic experiments, simple use cases

```typescript
const bandit = new MultiArmedBandit({
  algorithm: 'epsilon-greedy',
  epsilon: 0.1, // 10% exploration
  decayExploration: true, // Decay exploration ov
```
