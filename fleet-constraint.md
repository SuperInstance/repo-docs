# fleet-constraint

**URL:** https://github.com/SuperInstance/fleet-constraint

## Intention
The gatekeeper — safety constraint runtime for all fleet agents. No action proceeds without constraint evaluation.

## How It Works
Python runtime with three modules: GuardRuntime (loads .guard files, compiles to FLUX-C bytecode with 43 opcodes, guaranteed termination), FleetMathCore (H¹ emergence detection, ZHC, Pythagorean48 trust), KeeperBridge (wire protocol for credential proxying).

## What It's For
Enforcing safety constraints on every agent action.

## Who Would Use It
Agent safety engineers.

## Language/Stack
Python

## Status Assessment
Active — core safety infrastructure.

## Honest Assessment
Real project — comprehensive safety runtime with thoughtful architecture. The guaranteed-termination bytecode VM is a nice touch.
