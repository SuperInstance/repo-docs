# fleet-containers

**URL:** https://github.com/SuperInstance/fleet-containers

## Intention
Docker-based agent containerization for FLUX Fleet — reproducible deployments, isolated execution.

## How It Works
Docker Compose setup with layered images: base (Python+Go+Node+Rust), flux-runtime (FastAPI), and agent images. Bridge network on 172.28.0.0/16 with defined CPU/memory allocations per agent type. 72 tests.

## What It's For
Reproducible fleet deployment via Docker.

## Who Would Use It
DevOps engineers.

## Language/Stack
Python (Docker/Compose)

## Status Assessment
Active — 72 tests passing.

## Honest Assessment
Real project — comprehensive Docker setup with proper architecture, health checks, and resource limits.
