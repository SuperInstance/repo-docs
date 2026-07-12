# ct-bridge-npm

**Cluster:** archived-preserved  
**Language:** TypeScript  
**Source:** [SuperInstance/ct-bridge-npm](https://github.com/SuperInstance/ct-bridge-npm)

## Intention

Preserved workspace artifact

## How It Works

Constraint Theory solver bridge — CSP compilation and FLUX execution for Node.js.

## What It's For

Preserved workspace artifact

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

TypeScript — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** real-project
- **Note:** Well-documented (178 lines). Working examples and usage.

## Honest Assessment

Well-documented with working examples. Genuine project within the ecosystem. AI-created but shows real engineering. May see production use within the fleet.

## README Excerpt

```
# @cocapn/ct-bridge

Constraint Theory solver bridge — CSP compilation and FLUX execution for Node.js.

Wraps the Python [`constraint-theory`](https://pypi.org/project/constraint-theory/) package for use in Node.js via a persistent subprocess bridge with JSON-RPC messaging.

## Requirements

- **Node.js** >= 18
- **Python** >= 3.11
- **constraint-theory** pip package: `pip install constraint-theory`

## Installation

```bash
npm install @cocapn/ct-bridge
```

## Quick Start

```typescript
import { CTBridge } from "@cocapn/ct-bridge";

async function main() {
  const ct = new CTBridge();
  await ct.init();

  const solution = await ct.solve(
    ["x", "y", "z"],
    {
      x: { type: "range", min: 1, max: 10 },
      y: { type: "range", min: 1, max: 10 },
      z: { type: "range", min: 1, max: 10 },
    },
    [
      { id: "c1", variables: ["x", "y"], expression: "x + y == 10" },
      { id: "c2", variables: ["y", "z"], expression: "y < z" },
    ],
    "backtracking",
  );

  console.log(solution.assignments); // { x: 1, y: 9, z: 10 } (example)
  console.log(solution.consistent);  // true

  // Verify the solution
  const verification = await ct.verify(solution.assignments, [
    { id: "c1", variables: ["x", "y"], expression: "x + y == 10" },
    { id: "c2", variables: ["y", "z"], expression: "y < z" },
  ]);
  console.log(verification.valid); // true

  ct.destroy();
}
```

## API Reference

### `CTBridge`

Main class. Manages the Python subprocess lifecycle.

#### `new CTBridge(options?)`

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `pythonPath` | `string` | `"python3"` | Path to Python binary |
| `callTimeout` | `number` | `30000` | Timeout per call (ms) |
| `maxRestarts` | `number` | `3` | Max auto-restarts on crash |

#### `init(): Promise<void>`

Start the Python bridge process. Call once before any other method.

#### `solve(variables, domains, constraints, method?): Promise<Solution>`

Solve a constraint satisfaction problem.

| Parameter | Type | Description |
|-----------|------|-------------|
| `variables` | `string[]` | Variable names |
| `domains` | `Record<string, Domain>` | Per-variable domains |
| `constraints` | `Constraint[]` | Boolean predicates |
| `method` | `SolveMethod` | Solver strategy (default: `"backtracking"`) |

Returns a `Solution` with `assignments`, `consistent`, and `solveTimeMs`.

**Solver methods:**
- `"backtracking"` — Classic depth-first search with backtracking
- `"forward_checking"` — Backtracking with forward checking
- `"arc_consistency"` — AC-3 preprocessing + backtracking
- `"min_conflicts"` — Local search for optimization problems

#### `compile(problem): Promise<FLUXBytecode>`

Compile a CSP to FLUX bytecode. Returns the full instruction list with variable and constraint maps.

```typescript
const bytecode = await ct.compile({
  variables: ["x", "y"],
  domains: { x: { type: "set", values: [1, 2, 3] }, y: { type: "set", values: [4, 5, 6] } },
  constraints: [
```
