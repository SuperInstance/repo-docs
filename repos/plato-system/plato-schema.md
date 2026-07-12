# plato-schema

## Intention
JSON schema validation and versioning for PLATO messages

## How It Works
> JSON schema validation for PLATO tile data and configuration plato-schema validates JSON data against schemas defined in code. It checks types, ranges, required fields, string patterns, and enum values — ensuring tile data, sensor configurations, and pipeline settings conform to expected shapes before processing. Bad data causes subtle bugs. A temperature that's suddenly -999 or a sensor_id that's empty can cascade through the entire pipeline. plato-schema catches these problems at the boun...

## What It's For
Part of the PLATO ecosystem. JSON schema validation and versioning for PLATO messages

## Who Would Use It
PLATO ecosystem developers and SuperInstance fleet operators.

## Language / Stack
Rust

## Status Assessment
🟢 Moderate — has real documentation with concepts and some code

## Honest Assessment
Real implementation with documented concepts, code examples, and test coverage. This is a working component of the PLATO ecosystem, not just a placeholder.

## README Substance Level
- **Size:** 1386 bytes
- **Substance:** moderate
- **Has code examples:** True
- **Mentions testing:** True
- **Sections:** What This Does, The Key Idea, Install, Quick Start, Testing, License
