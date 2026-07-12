# fleet-config

**URL:** https://github.com/SuperInstance/fleet-config

## Intention
Unified configuration management — bridges fragmented config (fleet.yaml, agent.yaml, env vars, runtime overrides) into one coherent system.

## How It Works
Python CLI/library with layered config priority (CLI > env > runtime > fleet.yaml > agent.yaml > defaults), schema validation, templates (dev/prod/minimal/docker), snapshot/rollback, secret redaction, and doctor diagnostics.

## What It's For
Managing fleet configuration at scale.

## Who Would Use It
Fleet operators.

## Language/Stack
Python

## Status Assessment
Active — well-designed.

## Honest Assessment
Real project — genuinely well-designed config management. The priority layering, snapshot/rollback, and doctor diagnostics show production thinking.
