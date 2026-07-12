# field-dynamics

## Intention
**Interactive multi-agent field dynamics simulator — watch conservation, Fiedler partitioning, and spectral warfare play out in real-time.**

## How It Works
Agents carry 5D affinity vectors. Pairwise cosine similarity defines edge weights in the interaction graph. The Laplacian is built each frame, and the Fiedler vector (eigenvector for λ₂) partitions agents into two groups — shown by color.

**Conservation ratio** = λ₂/λₙ. High means the graph is well-connected and smooth. Saboteurs have random affinity (low similarity with everyone), which drops CR.

## What It's For
- **Real-time conservation tracking** — watch CR drop when you inject a saboteur or start a spectral war
- **Fiedler vector coloring** — agents colored by algebraic connectivity partition, live
- **Saboteur injection** — drop a bad agent into the fleet and watch conservation collapse
- **Spectral warfare** — split agents into competing teams and observe CR divergence
- **Heatmap overlay** — see th

## Who Would Use It
No installation needed. Single HTML file with inline CSS and JavaScript.

## Language / Stack
HTML

## Status Assessment
Has some documentation (63 lines).

## Honest Assessment
Has documentation (63 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/field-dynamics](https://github.com/SuperInstance/field-dynamics)*
