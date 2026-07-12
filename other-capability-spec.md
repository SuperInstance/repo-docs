# capability-spec

**Cluster:** docs-specs  
**Language:** Python  
**Source:** [SuperInstance/capability-spec](https://github.com/SuperInstance/capability-spec)

## Intention

Fleet discovery protocol — CAPABILITY.toml specification and crawler

## How It Works

Formal capability specification language and runtime for AI agents. Defines agent capabilities, permissions, and resource access patterns in a machine-readable format for fleet-wide capability management.

## What It's For

Fleet discovery protocol — CAPABILITY.toml specification and crawler

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Python — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (190 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# Capability Spec

Formal capability specification language and runtime for AI agents. Defines agent capabilities, permissions, and resource access patterns in a machine-readable format for fleet-wide capability management.

## Features

- **TOML-based declarations** — `CAPABILITY.toml` files define what agents can do
- **Schema validation** — check completeness, types, and constraints
- **Capability matching** — find the best agent for a task by confidence and recency
- **Dependency resolution** — topological sort of capability dependencies
- **A2A adapter** — convert to Google A2A Agent Card format
- **Versioning** — semantic versioning for specs with diff and upgrade support
- **Fleet discovery** — scan GitHub orgs for CAPABILITY.toml files
- **Zero external deps** — uses only stdlib (tomllib on 3.11+)

## Quick Start

```python
from capability_spec import CapabilitySpec, validate_capability, match_specialists

# Parse a CAPABILITY.toml file
spec = CapabilitySpec.from_file("CAPABILITY.toml")
print(f"{spec.name}: {len(spec.capabilities)} capabilities")

# Validate it
data = spec.to_dict()
result = validate_capability(data)
if not result.ok:
    for err in result.errors:
        print(f"ERROR: {err}")

# Find the best agent for a task across a fleet
agents = [spec1.to_dict(), spec2.to_dict()]
specialists = match_specialists(agents, "testing", min_confidence=0.8)
for s in specialists:
    print(f"  {s['avatar']} {s['name']}: score={s['score']:.2f}")
```

## Programmatic Spec Creation

```python
from capability_spec import CapabilitySpec

spec = CapabilitySpec(name="MyBot", agent_type="vessel", status="active")
spec.add_capability("testing", confidence=0.9, description="Test writing")
spec.add_capability("research", confidence=0.8, description="Deep research", requires=["testing"])

spec.upgrade_version("minor", "added research capability")
print(f"Version: {spec.version}")
```

## Schema Dataclasses

```python
from capability_spec.schema import CapabilitySchema, Capability, AgentInfo

# Build from dict (e.g., parsed TOML)
schema = CapabilitySchema.from_dict(data)

# Access typed fields
schema.agent.name          # str
schema.agent.type          # str (validated)
schema.capabilities        # dict[str, Capability]
schema.capabilities["testing"].confidence   # float (0-1)
schema.capabilities["testing"].requires     # list[str]
schema.resources.cpu_cores # Optional[float]
```

## Dependency Resolution

```python
from capability_spec import DependencyResolver, CapabilitySchema

schema = CapabilitySchema.from_dict(data)
resolver = DependencyResolver(schema)

# Get capabilities in dependency order
order = resolver.resolve()  # dependencies first

# Check for cycles
if resolver.has_cycle():
    print("Circular dependency detected!")

# What depends on "testing"?
dependents = resolver.get_dependents("testing")
```

## Spec Versioning & Diffing

```python
from capability_spec import CapabilitySpec, SpecVersion

v1 = CapabilitySpec.from_file("CAPABILITY.tom
```
