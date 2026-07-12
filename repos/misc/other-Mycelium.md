# Mycelium

## Intention

**Mycelium captures any behavior as a seed. One prompt + one seed = exact action, every time. No code needed—just show it once, then share the seed. Intelligence becomes instructions anyone can run.**

## How It Works

The mycelial coordination model operates on three principles derived directly from fungal biology:
### 1. Diffuse Signaling
Agents do not address messages to specific recipients. Instead, they deposit signals into the substrate at their local position. Neighbors within a signal radius detect and react. This mirrors how hyphae secrete chemical compounds that diffuse through soil.
**Signal propagation** follows an inverse-square attenuation:
```
signal_strength(d) = S₀ / (1 + (d / λ)²)
```
Where `S₀` is the original signal amplitude, `d` is distance, and `λ` is the characteristic diffusion length (analogous to hyphal spacing). Below a detection threshold `θ`, the signal is imperceptible — creating a natural locality boundary.
**Complexity:** Signal propagation to N neighbors within radius r is O(N), where N ∝ r². For bounded-radius propagation, each agent interaction is O(r²·log r) in a spatial hash.
### 2. Resource Routing via Gradients
When an agent needs a resource (computation, data, capability), it follows the gradient of availability in the substrate. This is gradient-based routing, the same mechanism Physarum polycephalum (slime mold) uses to solve network design problems (Nakagaki et al., 2000 — slime mold recreated the Tokyo rail network).
The gradient at agent position x is:
```
∇R(x) = Σᵢ (Rᵢ - R(x)) · ĥᵢ / |dᵢ|²
```

## What It's For

**Mycelium captures any behavior as a seed. One prompt + one seed = exact action, every time. No code needed—just show it once, then share the seed. Intelligence becomes instructions anyone can run.**

## Who Would Use It

Developers building agent systems within the Lau/PLATO ecosystem. Those working on multi-agent coordination, fleet management, or AI agent infrastructure.

## Language / Stack

- **Primary language:** Rust

## Status Assessment

**Status: MODERATE**

Reasonable README (74 lines), includes examples.

- README length: 117 lines, 7144 characters
- Documented sections: Why It Matters, How It Works, Quick Start, API, Architecture Notes

## Honest Assessment

The README shows genuine effort with reasonable documentation. There's evidence of structure and intent. However, as with many repos in this organization, it's unclear if there's real adoption or if this is primarily a research/portfolio project. **Solid documentation, real concepts, but real-world deployment status is unclear.**

> ⚠️ **Ecosystem dependency:** This repo makes 3+ references to SuperInstance-specific concepts (PLATO, Lau, conservation laws, spectral framework). It's tightly coupled to this ecosystem and unlikely to be useful independently.
