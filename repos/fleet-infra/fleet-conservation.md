# fleet-conservation

**URL:** https://github.com/SuperInstance/fleet-conservation

## Intention
Conservation law tracker — γ + η = C, where γ is generation cost and η is innovation value.

## How It Works
Rust crate tracking the balance between compute spent (tokens, API calls, time) and value produced (files changed, tests passed). Normalized: γ + η ≈ 1.0. Includes forgecode hook integration. 37 tests.

## What It's For
Detecting spinning agents and optimizing fleet resource use.

## Who Would Use It
Agent fleet operators.

## Language/Stack
Rust

## Status Assessment
Active — 37 tests, forgecode integration.

## Honest Assessment
Real project — genuinely useful accounting system for agent productivity. The conservation law metaphor is creative but the tracking is practical.
