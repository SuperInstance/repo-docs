# flux-check-js

**Category:** ✅ Constraint/Safety
**Status:** 🟢 Production-oriented
**Language:** TypeScript
**README:** 9,862 bytes

## Intention
Exact constraint checking, fracture-coalesce, and sediment layers. Zero-dep TypeScript/ESM.

## How It Works
A constraint system checks whether values fall within acceptable bounds. This library does three things:

**1. Exact checking.** Given N values and N `(lo, hi)` bounds, check each value against its bound. Produce a violation array and an error bitmask. NaN always violates. Boundary values pass (`<=`). No approximations.

When constraints are **independent** (they share no underlying physical dimension), fracture splits them into parallel blocks. Set the `dims` parameter on `addConstraint()` to d...

## What It's For
Exact constraint checking, fracture-coalesce, and sediment layers. Zero-dep TypeScript/ESM.

## Who Would Use It
Formal methods practitioners and safety-critical systems engineers.

## Honest Assessment
Has real code examples and installation instructions. Has implementation code but **test coverage needs verification**..
