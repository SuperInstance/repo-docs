# negative-space-core

## Intention

Core theory of negative space intelligence — intelligence is what you learn to AVOID, not what you choose

## How It Works

### The 294:1 Conservation Law
The core invariant: for any sufficiently large agent population, the ratio of avoided decisions to chosen decisions converges to approximately 294. This is verified empirically using the `ConservationLaw` checker across population scales {10, 100, 1000, 5000}:
```
ratio = total_avoidances / total_choices ≈ 294.0
std_dev(ratios across scales) < 0.01
```
The verification algorithm runs in **O(N · S)** time where N is total agents and S is the number of population scales tested.
### Feedback Refinement via EMA
The `FeedbackLoop` updates the estimated avoidance ratio using exponential moving average:
```
μ_(t+1) = μ_t · (1 - α) + r_observed · α
```
where α is the learning rate (default 0.01). This converges to the true ratio with error decreasing as **O(1/√t)** by the law of large numbers. The EMA prevents oscillation while tracking distribution shifts.
### Inference from Absence
The `InferenceEngine` finds gaps between avoided options. If agents consistently avoid both X and Y, the space between them likely contains an undiscovered Z. Confidence is computed as:

## What It's For

Core theory of negative space intelligence — intelligence is what you learn to AVOID, not what you choose

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (62 lines), mentions tests, includes examples.

- README length: 96 lines, 5080 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**
