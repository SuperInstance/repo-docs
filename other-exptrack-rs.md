# exptrack-rs

## Intention
**Experiment Tracker in Rust — lightweight, zero-dependency, research-grade**

## How It Works
```
┌─────────────────────────────────────────────────────────────┐
│                     User Interface Layer                    │
│  CLI | Web UI | Library API | FFI Bindings                  │
└─────────────────────────────────────────────────────────────┘
                              │
┌─────────────────────────────────────────────────────────────┐
│                    Experiment Management                     │
│  Run Lifecycle | Query Engine | Comparison | Organization   │
│  ┌──────────┐

## What It's For
exptrack-rs is a hierarchical, layered experiment tracking library for Rust projects. It provides a simple API to record parameters (immutable), metrics (mutable time-series), and artifacts (immutable files) for every experiment run, making research workflows fully reproducible. Designed to go from zero-setup local SQLite to production PostgreSQL + S3 without changing your code.

Every experiment

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Not specified

## Status Assessment
Marked as archived, WIP, or early version.

## Honest Assessment
Moderately documented (185 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/exptrack-rs](https://github.com/SuperInstance/exptrack-rs)*
