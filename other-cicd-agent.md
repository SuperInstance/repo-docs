# cicd-agent

**Cluster:** fleet-agent-infra  
**Language:** Python  
**Source:** [SuperInstance/cicd-agent](https://github.com/SuperInstance/cicd-agent)

## Intention

Fleet CI/CD pipeline engine — git polling, test runner, webhook receiver, deployment

## How It Works

It Fits

The CI/CD backbone of the [SuperInstance fleet](https://github.com/SuperInstance). Every commit to a fleet repo triggers this pipeline.

- **[branch-sandbox](https://github.com/SuperInstance/branch-sandbox)** — Isolated test execution
- **[clawcommit-lucid](https://github.com/SuperInstance/clawcommit-lucid)** — Validates commit message format
- **[fleet-health-monitor](https://github.com/SuperInstance/fleet-health-monitor)** — Post-deploy health checks
- **[co-captain-git-agent](https://github.com/SuperInstance/co-captain-git-agent)** — Human gates for deployments

## What It's For

Fleet CI/CD pipeline engine — git polling, test runner, webhook receiver, deployment

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** moderate
- **Note:** Moderate docs (82 lines, 2480 chars). Some substance.

## Honest Assessment

Moderate documentation with some implementation detail. Likely AI-assisted creation within the fleet ecosystem. Real code but may lack independent testing or production use.