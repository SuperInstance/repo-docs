# exocortex-esp32

## Intention
An Arduino/PlatformIO sketch for ESP32 that reads analog sensors and communicates with an Exocortex server.

## How It Works
Not documented in a dedicated section. See the README for details.

## What It's For
- **Sense**: Reads temperature (A0) and soil moisture (A1), POSTs to `/tap/sense` every 30s
- **Recall**: GETs `/tap/recall?q=<query>` to retrieve stored memories
- **Predict**: GETs `/tap/predict?sensor=<name>&reading=<value>` for predictions
- Plain-text protocol (no JSON parsing needed on the microcontroller)

## Who Would Use It
Developers and researchers in the SuperInstance ecosystem.

## Language / Stack
C++

## Status Assessment
Documented with code examples and API references (81 line README).

## Honest Assessment
Has documentation (81 lines) but limited depth. May be functional but incompletely documented.

---
*Source: [GitHub - SuperInstance/exocortex-esp32](https://github.com/SuperInstance/exocortex-esp32)*
