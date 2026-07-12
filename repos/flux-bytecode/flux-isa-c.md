# flux-isa-c

**Category:** 🗄️ Preserved Artifact
**Status:** 🗄️ Preserved Artifact
**Language:** C
**README:** 2,976 bytes

## Intention
Preserved workspace artifact

## How It Works
- **Stack**: 256-entry `double` stack
- **Call stack**: 64-entry depth
- **Registers**: 16 general-purpose `double` registers (LOAD/STORE)
- **Trace buffer**: configurable, default 1024 entries
- **Outputs**: dynamically grown output stream via SNAP/DUMP

## Return Codes

| Code | Meaning |
|------|---------|
| 0    | Success |
| -1   | Stack overflow/underflow or invalid state |
| -2   | Division by zero |
| -3   | Call stack overflow |
| -4   | Call stack underflow (RETURN with empty call stac...

## What It's For
Preserved workspace artifact

## Who Would Use It
Nobody actively — this is a preserved snapshot.

## Honest Assessment
Has code examples. **preserved artifact** (snapshot, not active). missing: benchmarks.
