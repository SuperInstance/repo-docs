# forge-sensor

## Intention
Sensor readings → tiles → Plato agents.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- **Parse any sensor line** — `"sonar:45.2:fathoms@1700001000"` → structured tile
- **Filter by type or time** — give me all sonar readings from the last hour
- **Latest by type** — what's the current reading for each sensor?
- **Statistics** — min, max, mean, std_dev for any set of readings
- **Zero dependencies** beyond serde + uuid

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
Rust

## Status Assessment
Has some documentation (21 lines).

## Honest Assessment
Minimal documentation (21 lines). Early-stage or thinly documented.

---
*Source: [GitHub - SuperInstance/forge-sensor](https://github.com/SuperInstance/forge-sensor)*
