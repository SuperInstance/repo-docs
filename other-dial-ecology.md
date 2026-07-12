# dial-ecology

**Cluster:** ecology-sim  
**Language:** Rust  
**Source:** [SuperInstance/dial-ecology](https://github.com/SuperInstance/dial-ecology)

## Intention

Ecological succession on the cultural dial: Lotka-Volterra dynamics for tradition competition, niche theory, Allee extinction, Shannon biodiversity

## How It Works

> *What if cultural traditions are species? What if the spectrum of human belief is a landscape — and every tradition is an organism competing for niche space, subject to the same merciless mathematics that governs forests, coral reefs, and tide pools?*

## What It's For

Ecological succession on the cultural dial: Lotka-Volterra dynamics for tradition competition, niche theory, Allee extinction, Shannon biodiversity

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (227 lines, 8480 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# dial-ecology

**Ecological succession on the cultural dial.**

> *What if cultural traditions are species? What if the spectrum of human belief is a landscape — and every tradition is an organism competing for niche space, subject to the same merciless mathematics that governs forests, coral reefs, and tide pools?*

`dial-ecology` models cultural traditions as species in an ecological system. They grow, compete, coexist, and go extinct according to the laws of population ecology — specifically, the **Lotka-Volterra competition equations**. The "dial" is the spectrum of cultural expression: left to right, traditional to progressive, sacred to secular, old to new. Every tradition occupies a niche. Every niche has limited space.

## The Ecology of Culture

### 🌱 Traditions Are Species

A religion, a political ideology, a folk practice, a scientific paradigm — each is a "species" with:

- **Population** — number of adherents
- **Growth rate** — how fast it spreads (proselytizing religions grow fast; contemplative orders grow slow)
- **Carrying capacity** — the maximum population the niche can sustain
- **Dial position** — where on the cultural spectrum it lives

### ⚔️ Competition Is Real

Two traditions occupying the same niche **compete**. The Lotka-Volterra equations govern this:

```
dT₁/dt = r₁·T₁·(1 - T₁/K₁ - α₁₂·T₂/K₁)
dT₂/dt = r₂·T₂·(1 - T₂/K₂ - α₂₁·T₁/K₂)
```

Where:
- `r` = intrinsic growth rate
- `K` = carrying capacity
- `α` = competition coefficient (derived from niche overlap)

**High niche overlap → high α → fierce competition → one tradition may drive the other to extinction.**

### 🤝 Coexistence Requires Differentiation

Two traditions can coexist *if and only if*:

```
α₁₂ < K₁/K₂  AND  α₂₁ < K₂/K₁
```

This is the ecological translation of tolerance: *you can share the landscape, but only if you're different enough*. Identical niches mean war. Differentiated niches mean peace.

### 🌊 Succession Unfolds

Like bare rock colonized by lichens → mosses → grasses → shrubs → trees:

1. **Pioneer traditions** — fast-growing, low diversity, few adherents, high zeal
2. **Intermediate community** — more traditions emerge, competition intensifies
3. **Climax community** — stable, diverse, many coexisting traditions at equilibrium

The cultural landscape matures just like an ecosystem.

### 💀 Extinction Happens

A tradition goes extinct when its population falls below a critical threshold. The **Allee effect** makes this irreversible: small populations grow *slower*, not faster — they've lost the critical mass needed for cultural transmission. A language with 5 speakers is already dead. A religion with 50 practitioners is dying.

### 🌈 Biodiversity = Resilience

The **Shannon diversity index** measures ecosystem health:

```
H' = -Σ(pᵢ · ln(pᵢ))
```

- **High diversity** → many traditions, evenly distributed → resilient to disruption
- **Low diversity** → monoculture or near-monoculture → fragile, vulnerable to collapse
- **Monoculture** → on
```
