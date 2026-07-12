# px4-conservation-poc

## Intention
Conservation-based flight anomaly detection for PX4 — predicts failures before they're visible in raw data

## How It Works
PX4 flight anomaly detection via conservation spectral analysis — detect attitude failures, GPS glitches, and motor failures from EKF2 state sequences. Proof of concept applying the conservation spectral framework to PX4 autopilot data. Simulates 16-dimensional flight states (quaternion + velocity + position + gyro + accel), injects three types of anomalies, and detects them through conservation ratio drops in sliding-window spectral analysis. - Flight state simulator — synthetic PX4 EKF2 16D state sequences with smooth SLERP interpolation - Three anomaly types — sudden attitude change, GPS glitch, motor failure - Conservation-based detection — sliding window Laplacian, track CR drops - Spectral fingerprinting — compare healthy vs unhealthy flight signatures - Threshold comparison — conser

## What It's For
Conservation-based flight anomaly detection for PX4 — predicts failures before they're visible in raw data

## Who Would Use It
Python developers interested in physics-based software verification

## Language / Stack
Python

## Status Assessment
**Developing** — Moderate documentation with some structure and examples.

- README size: 1,780 characters, 44 lines
- Code examples: 2 blocks
- Installation instructions: yes
- Testing mentioned: no
- License mentioned: yes
- API documentation: no
- Architecture diagrams: yes

## Honest Assessment

**Strengths:**
- Deep theoretical grounding (2 advanced math concepts referenced)
- Installation/usage instructions provided

**Concerns:**
- Heavy abstraction may limit practical adoption
- Unclear if theoretical rigor translates to working software

**Overall:** Early but potentially interesting — read the source to verify.
