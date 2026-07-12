# negative-space-core-c

## Intention

C implementation of negative space intelligence — intelligence is what you learn to AVOID

## How It Works

### Avoidance Tracking
The `NSAvoidanceTracker` records a timestamped stream of ternary actions: `AVOID (-1)`, `CHOOSE (+1)`, or `UNKNOWN (0)`. At any point, it computes the avoidance ratio:
```
R_avoid = N_avoid / N_total
```
along with the choose ratio and unknown ratio. The standard deviation of action types provides a dispersion measure. Storage is O(N) with a fixed-capacity ring of `NS_TRACKER_MAX_ACTIONS = 4096`.
### Conservation Law
The central hypothesis: *if avoidance ratios are conserved across scales, the agent possesses genuine knowledge*. The library partitions the action stream into `k` equal windows and computes the avoidance ratio for each:
```
R_k = N_avoid(window_k) / N_actions(window_k)
```
If the variance `Var(R_1, ..., R_k)` falls below a user-supplied threshold, the avoidance pattern is **conserved** — indicating structured knowledge rather than random noise. This is analogous to the Reynolds number in fluid dynamics: when the dimensionless ratio stays constant across scales, you have a physical law, not coincidence.
### Inference Engine
Given an avoidance map, the inference engine identifies **gaps** — contiguous regions of the action space that were systematically avoided. Each gap yields a `NSGap` struct with:
```

## What It's For

C implementation of negative space intelligence — intelligence is what you learn to AVOID

## Who Would Use It

Developers and researchers in the SuperInstance ecosystem. Those building systems that need this specific computational primitive.

## Language / Stack

- **Primary language:** C

## Status Assessment

**Status: MODERATE**

Reasonable README (73 lines), includes examples.

- README length: 110 lines, 5753 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
