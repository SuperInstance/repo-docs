# keeper-agent

## Intention
Secret-keeper proxy for FLUX Fleet standalone agents. Holds all API keys, issues scoped tokens, double-checks that no secrets leave the SuperInstance.

## How It Works
README covers: The Problem, The Solution, Core Components, Vault (`src/vault.ts`), Auth (`src/auth.ts`), Secret Scanner (`src/scanner.ts`), Proxy Engine (`src/proxy.ts`), Audit Log (`src/audit.ts`). Published to npm. 

## What It's For
Secret-keeper proxy for FLUX Fleet standalone agents. Holds all API keys, issues scoped tokens, double-checks that no secrets leave the SuperInstance.

## Who Would Use It
AI agent developers and researchers.

## Language / Stack
TypeScript/JavaScript (npm)

## Status Assessment
production, basic tests, moderately documented (153 lines)

## Honest Assessment
Strengths: thorough documentation (153 lines). Concerns: tightly coupled to the SuperInstance/PLATO/FLUX ecosystem — limited standalone value.
