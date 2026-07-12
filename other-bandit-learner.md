# bandit-learner

**Cluster:** misc  
**Language:** Not specified  
**Source:** [SuperInstance/bandit-learner](https://github.com/SuperInstance/bandit-learner)

## Intention

Multi-armed bandit algorithms for exploration-exploitation and online learning

## How It Works

[code]

## What It's For

Multi-armed bandit algorithms for exploration-exploitation and online learning

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Unknown — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (243 lines, 6101 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# bandit-learner

**Production-Ready Contextual Bandit Library for Online Learning**

bandit-learner extends frozen-model-rl with comprehensive contextual bandit implementations designed for production environments. It provides battle-tested algorithms for real-time decision-making with sub-millisecond latency.

## Philosophy

**"Learn fast, serve faster"**

bandit-learner is built for production systems that need to:
- Learn from user interactions in real-time
- Serve decisions with <1ms latency
- Scale to thousands of concurrent learners
- Provide production-grade monitoring and safety

## Key Features

- Multiple bandit algorithms (LinUCB, Thompson Sampling, Epsilon-Greedy, Neural Bandit)
- Production-ready training and serving infrastructure
- Comprehensive monitoring and experimentation framework
- Built-in A/B testing capabilities
- Safe exploration with fallback policies
- Model persistence and state management
- Python and Rust APIs

## Quick Start

### Python API

```python
from bandit_learner import LinUCB, BanditConfig

# Create a bandit
config = BanditConfig(
    n_arms=20,
    context_dim=12,
    alpha=0.5
)
bandit = LinUCB(config)

# Select an action
context = [0.5] * 12
arm = bandit.select_arm(context)

# Update with reward
reward = 0.8
bandit.update(arm, context, reward)
```

### Rust API

```rust
use bandit_learner::bandit::LinUCB;

let mut bandit = LinUCB::new(20, 12, 0.5)?;

let context = vec![0.5; 12];
let arm = bandit.select_arm(&context)?;
let reward = 0.8;
bandit.update(arm, &context, reward)?;
```

## Algorithms

| Algorithm | Type | Latency | Best For |
|-----------|------|---------|----------|
| **LinUCB** | Linear UCB | <1ms | High-dimensional contexts, proven guarantees |
| **Thompson Sampling** | Bayesian | <1ms | Uncertainty quantification, non-linear models |
| **Epsilon-Greedy** | Exploration | <1ms | Simple problems, baseline comparisons |
| **Neural Bandit** | Deep Learning | <5ms | Complex patterns, large-scale problems |

## Performance

- **Inference Latency**: <1ms (LinUCB, Thompson Sampling, Epsilon-Greedy)
- **Training**: Online, incremental updates (<100µs per update)
- **Memory Footprint**: <10MB per bandit instance
- **Throughput**: 1000+ decisions per second per instance

## Use Cases

### 1. Content Recommendation

```python
# Learn which content to show based on user context
bandit = LinUCB(n_arms=100, context_dim=20)
context = extract_user_features(user)
article_id = bandit.select_arm(context)

# User engagement is the reward
reward = 1.0 if user.clicked else 0.0
bandit.update(article_id, context, reward)
```

### 2. Constraint Weight Optimization

```python
# Learn optimal constraint weights for equilibrium-tokens
from bandit_learner import ThompsonSampling
from frozen_model_rl import EquilibriumOrchestrator

bandit = ThompsonSampling(n_arms=20, context_dim=12)
orchestrator = EquilibriumOrchestrator()

# Select weights for this conversation turn
context = extract_conversation_features(conversation)

```
