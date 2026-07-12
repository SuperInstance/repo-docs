# fleet-warden-rs

**URL:** https://github.com/SuperInstance/fleet-warden-rs

## Intention
Enhanced fleet resource guardian — disk cleanup, budget enforcement, state monitoring with anomaly detection and circuit breakers.

## How It Works
Rust crate extending fleet-warden with Z-score/MAD/IQR anomaly detection, circuit breaker pattern (Closed→Open→HalfOpen), adaptive rate limiting (p50/p95/p99), and persistent JSON state.

## What It's For
Production-grade fleet resource management.

## Who Would Use It
DevOps engineers.

## Language/Stack
Rust

## Status Assessment
Active — more sophisticated than fleet-warden.

## Honest Assessment
Real project — serious production hardening of fleet-warden with proper resilience patterns.
