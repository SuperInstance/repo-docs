# ai-pasture

**Cluster:** constraint-theory  
**Language:** Rust  
**Source:** [SuperInstance/ai-pasture](https://github.com/SuperInstance/ai-pasture)

## Intention

Multi-species ecosystem simulation with ternary resource management. Population dynamics, carrying capacity, predator-prey.

## How It Works

### Soil Fertility Model

**Soil fertility** is a weighted average across four factors:

[code]

Where:

- **NPK_avg** = (N + P + K) / 3, each ∈ [0, 100]
- **pH_score** = 1.0 − |pH − 6.75| / 6.75 (peaks at 6.75, linear falloff)
- **moisture_score** = trapezoidal function (ideal: 20–80%)
- **OM_score** = organic_matter / 100

This matches real soil science: NPK is the dominant factor (35% weight), pH controls nutrient bioavailability (15%), moisture enables nutrient transport (25%), and organic matter improves both water retention and slow-release nutrients (25%).

**Complexity:** Fertility com

## What It's For

Multi-species ecosystem simulation with ternary resource management. Population dynamics, carrying capacity, predator-prey.

## Who Would Use It

Developers and researchers in the SuperInstance fleet ecosystem.

## Language / Stack

Rust — part of the SuperInstance ecosystem.

## Status Assessment

- **Quality tier:** substantial
- **Note:** Rich documentation (181 lines, 8117 chars). Architecture + motivation.

## Honest Assessment

Rich documentation with architecture, motivation, and code. Among the more serious projects. AI-created as part of agent fleet infrastructure, but with genuine depth and thinking.

## README Excerpt

```
# ai-pasture

**AI Pasture** is a Rust farming and agriculture simulation library implementing a NPK (nitrogen-phosphorus-potassium) soil nutrient model, crop growth dynamics, livestock management, and weather-driven ecosystem simulation for the Lau game universe. It models a tick-based ecosystem where soil fertility, crop health, water cycles, and animal husbandry interact through biogeochemically-grounded equations.

## Why It Matters

Agricultural simulations require accurate biogeochemical modeling to produce believable game worlds. The NPK nutrient cycle, pH-dependent nutrient availability, and water-stress crop responses are well-documented in agronomy literature. This library encodes those models into a tick-based simulation where soil fertility is a weighted function of NPK balance, pH proximity to 6.75, moisture adequacy, and organic matter content.

Crops consume nutrients proportional to species-specific needs. Livestock convert silo grain into secondary products (eggs, milk, wool, manure). Legumes fix atmospheric nitrogen via Rhizobium symbiosis. Weather drives soil moisture through rainfall. All of these create gameplay where sustainable farming practices — composting, crop rotation with legumes, water management — emerge as optimal strategies rather than being scripted.

This matters because it means the game's economy is grounded in real science. Players who understand crop rotation, nitrogen fixation, and soil conservation have a genuine advantage. The simulation rewards ecological literacy.

## How It Works

### Soil Fertility Model

**Soil fertility** is a weighted average across four factors:

```
fertility = 0.35 × NPK_avg + 0.15 × pH_score + 0.25 × moisture_score + 0.25 × OM_score
```

Where:

- **NPK_avg** = (N + P + K) / 3, each ∈ [0, 100]
- **pH_score** = 1.0 − |pH − 6.75| / 6.75 (peaks at 6.75, linear falloff)
- **moisture_score** = trapezoidal function (ideal: 20–80%)
- **OM_score** = organic_matter / 100

This matches real soil science: NPK is the dominant factor (35% weight), pH controls nutrient bioavailability (15%), moisture enables nutrient transport (25%), and organic matter improves both water retention and slow-release nutrients (25%).

**Complexity:** Fertility computation is O(1) — constant arithmetic per plot per tick.

### Crop Growth Dynamics

**Crop growth** per tick follows:

```
Δgrowth = (1 / growth_time) × (0.4 × fertility + 0.3 × water_factor + 0.3 × sunlight)
```

Where `water_factor = min(1.0, soil_moisture / crop_water_need)`.

Each crop species has specific parameters:

| Crop | Growth Time (ticks) | Water Need | Nitrogen Fixer | Yield |
|------|-------------------|------------|----------------|-------|
| Wheat | 100 | 40 | No | 8 |
| Corn | 120 | 60 | No | 12 |
| Rice | 90 | 90 | No | 10 |
| Bean | 80 | 35 | **Yes** | 6 |
| Lavender | 60 | 20 | **Yes** | 4 |
| Potato | 70 | 45 | No | 14 |

Growth accumulates from 0.0 to 1.0 (mature). At maturity, `harvest()` returns the yield amount and resets th
```
