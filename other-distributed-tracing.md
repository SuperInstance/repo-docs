# distributed-tracing

## Intention
A high-performance, OpenTelemetry-compliant distributed tracing library for Rust and Go microservices.

## How It Works
```
┌─────────────────────────────────────────────────────────────┐
│                     Application Layer                        │
├─────────────────────────────────────────────────────────────┤
│  ┌──────────┐  ┌──────────┐  ┌──────────┐                  │
│  │ Service  │  │ Service  │  │ Service  │                  │
│  │    A     │  │    B     │  │    C     │                  │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘                  │
│       │             │             │

## What It's For
- **OpenTelemetry Integration**: Full compliance with OpenTelemetry standards
- **Context Propagation**: Automatic trace context propagation across service boundaries
- **Flexible Sampling**: Multiple sampling strategies (probabilistic, rate-limiting, parent-based)
- **High Performance**: <100µs overhead per span, <1% CPU at 1% sampling
- **Multi-Language Support**: Rust and Go implementations
- *

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Claims production-ready with tests and documentation.

## Honest Assessment
Well-documented (438 lines) with code examples, API docs, and usage guides. Appears to be a genuine, developed project.

---
*Source: [GitHub - SuperInstance/distributed-tracing](https://github.com/SuperInstance/distributed-tracing)*
