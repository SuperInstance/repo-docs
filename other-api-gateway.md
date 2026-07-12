# api-gateway

**Cluster:** infra-devops  
**Language:** Rust  
**Source:** [SuperInstance/api-gateway](https://github.com/SuperInstance/api-gateway)

## Intention

API Gateway with routing, rate limiting, authentication, and request/response transformation

## How It Works

The gateway implements a **reverse proxy routing model**. Each incoming request is matched against a routing table:

[code]

**Routing complexity:** O(R) for R routes with linear scan, or O(log R) with a trie-based router. For the SuperInstance fleet with ~20 services, linear scan at O(20) is negligible.

**Request lifecycle:**
1. **Ingress:** Receive HTTP request, parse method/path/headers
2. **Authentication:** Validate JWT or API key against `fleet-auth` D1 database
3. **Rate limiting:** Token bucket per client IP (capacity 100, refill 10/min)
4. **Routing:** Match path prefix to upstream s

## What It's For

API Gateway with routing, rate limiting, authentication, and request/response transformation

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (74 lines, 4383 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# API Gateway

**API Gateway** is a Rust library providing the routing, request dispatch, and upstream management layer for the SuperInstance fleet's HTTP API infrastructure, directing incoming requests to appropriate backend services.

## Why It Matters

An API gateway is the single entry point that sits between clients and backend services. It handles cross-cutting concerns — request routing, authentication, rate limiting, load balancing, and response transformation — so that individual backend services can focus on business logic. In microservice architectures, the gateway pattern reduces client-side complexity (one URL instead of dozens), centralizes security policy enforcement, and provides a natural point for observability instrumentation. Without a gateway, every backend service must independently implement authentication, CORS, logging, and rate limiting — duplicating infrastructure code and creating inconsistent security postures across the fleet.

## How It Works

The gateway implements a **reverse proxy routing model**. Each incoming request is matched against a routing table:

```
route(request):
  for each (path_prefix, upstream) in routes:
    if request.path.starts_with(path_prefix):
      return forward(request, upstream)
  return 404
```

**Routing complexity:** O(R) for R routes with linear scan, or O(log R) with a trie-based router. For the SuperInstance fleet with ~20 services, linear scan at O(20) is negligible.

**Request lifecycle:**
1. **Ingress:** Receive HTTP request, parse method/path/headers
2. **Authentication:** Validate JWT or API key against `fleet-auth` D1 database
3. **Rate limiting:** Token bucket per client IP (capacity 100, refill 10/min)
4. **Routing:** Match path prefix to upstream service URL
5. **Forward:** Proxy request with timeout (30s default)
6. **Response:** Return upstream response, log metrics to `fleet-metrics-cron`

**Load balancing:** When multiple upstream instances are available, the gateway uses weighted round-robin, distributing load proportional to declared capacity. Health checks (HTTP GET `/health` every 10s) remove failed instances from rotation automatically.

## Quick Start

```rust
fn main() {
    println!("api-gateway: routing requests to upstreams");
    // The gateway runs as a Worker on Cloudflare's edge network,
    // routing to fleet services:
    //   /search    → fleet-vector-api
    //   /auth      → fleet-auth
    //   /metrics   → fleet-metrics-cron
    //   /ingest    → fleet-edge-worker
}
```

## API

| Endpoint | Upstream | Purpose |
|----------|----------|---------|
| `POST /search` | fleet-vector-api | Semantic crate search |
| `POST /auth/*` | fleet-auth | Authentication/authorization |
| `GET /metrics` | fleet-metrics-cron | Fleet performance metrics |
| `POST /ingest` | fleet-edge-worker | Bulk data ingestion |
| `GET /health` | self | Health check |

## Architecture Notes

The API Gateway is the **η-layer ingress point** in the SuperInstance fleet. It routes incom
```
