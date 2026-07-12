# fleet-health-monitor

**URL:** https://github.com/SuperInstance/fleet-health-monitor

## Intention
Daemonized fleet health monitoring with necrosis detection, health scoring, and alerting. Zero external dependencies.

## How It Works
Python package (published to PyPI as si-fleet-health-monitor) with a 4-state health model (HEALTHY → DEGRADED → UNHEALTHY → UNKNOWN), watchdog timers, threshold configs, and ASCII dashboard. 248 tests.

## What It's For
Monitoring fleets of 200+ agents for stalls, resource exhaustion, and silent failures.

## Who Would Use It
Fleet operators and DevOps.

## Language/Stack
Python

## Status Assessment
Production-ready v0.1.0 with 248 tests.

## Honest Assessment
Real project — genuinely useful monitoring tool with serious test coverage. Production-quality.
