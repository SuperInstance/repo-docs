# Edge & Embedded

**59 repos** for edge computing — ESP32, NVIDIA Jetson, ARM64, marine vessel bridges, holodeck simulations, and embedded agent onboarding across a dozen languages.

---

## What Is Edge in This Ecosystem?

The edge/embedded layer brings the SuperInstance fleet to resource-constrained devices: microcontrollers (ESP32, RP2040), GPU edge boards (NVIDIA Jetson), ARM64 servers, and marine/industrial hardware. It's where the fleet meets the physical world.

Key themes:

1. **OpenConstruct** — a universal agent onboarding framework with a C ABI core and 12+ language SDKs
2. **Holodeck** — MUD-style simulation environments ported to C, Rust, Go, Zig, CUDA
3. **Vessel** — marine/industrial agent nodes for real-world deployment
4. **Kintsugi** — mathematical fault tolerance ("beautiful error recovery")
5. **Edge relay** — research and sensor data relay from edge to fleet

---

## Key Repositories

### Holodeck (Multi-Language Simulation)

The holodeck is a MUD-style simulation environment for fleet modeling — rooms are graph nodes, agents traverse rooms, gauges monitor state.

| Repo | Language | Description |
|------|----------|-------------|
| [holodeck-c](https://github.com/SuperInstance/holodeck-c) | C | Lightweight C implementation for embedded |
| [holodeck-core](https://github.com/SuperInstance/holodeck-core) | Rust | Core simulation engine |
| [holodeck-rust](https://github.com/SuperInstance/holodeck-rust) | Rust | Full Rust implementation |
| [holodeck-cuda](https://github.com/SuperInstance/holodeck-cuda) | CUDA | GPU-accelerated simulation |
| [holodeck-go](https://github.com/SuperInstance/holodeck-go) | Go | Go implementation |
| [holodeck-zig](https://github.com/SuperInstance/holodeck-zig) | Zig | Systems-level implementation |
| [holodeck-session-manager](https://github.com/SuperInstance/holodeck-session-manager) | — | Session management |
| [holodeck-studio](https://github.com/SuperInstance/holodeck-studio) | — | Studio UI |

### OpenConstruct (Agent Onboarding)

OpenConstruct is the universal agent onboarding framework — "any agent, any hardware, any language." It uses a C ABI as the universal interface, with language-specific SDKs wrapping it.

| Repo | Language | Description |
|------|----------|-------------|
| [openconstruct-abi](https://github.com/SuperInstance/openconstruct-abi) | C ABI | The universal interface definition |
| [openconstruct-c](https://github.com/SuperInstance/openconstruct-c) | C | C SDK |
| [openconstruct-rust](https://github.com/SuperInstance/openconstruct-rust) | Rust | Rust SDK |
| [openconstruct-python](https://github.com/SuperInstance/openconstruct-python) | Python | Python SDK |
| [openconstruct-go](https://github.com/SuperInstance/openconstruct-go) | Go | Go SDK |
| [openconstruct-ts](https://github.com/SuperInstance/openconstruct-ts) | TypeScript | TS SDK |
| [openconstruct-zig](https://github.com/SuperInstance/openconstruct-zig) | Zig | Zig SDK |
| [openconstruct-swift](https://github.com/SuperInstance/openconstruct-swift) | Swift | Swift SDK |
| [openconstruct-java](https://github.com/SuperInstance/openconstruct-java) | Java | Java SDK |
| [openconstruct-cs](https://github.com/SuperInstance/openconstruct-cs) | C# | C# SDK |
| [openconstruct-ruby](https://github.com/SuperInstance/openconstruct-ruby) | Ruby | Ruby SDK |
| [openconstruct-esp32](https://github.com/SuperInstance/openconstruct-esp32) | C++ | ESP32 embedded SDK |
| [openconstruct-jetson](https://github.com/SuperInstance/openconstruct-jetson) | C++ | NVIDIA Jetson GPU edge SDK |
| [openconstruct-kernel](https://github.com/SuperInstance/openconstruct-kernel) | — | Kernel module |
| [openconstruct-modular](https://github.com/SuperInstance/openconstruct-modular) | — | Modular build |
| [openconstruct-hub](https://github.com/SuperInstance/openconstruct-hub) | — | Central hub |
| [openconstruct-docs](https://github.com/SuperInstance/openconstruct-docs) | — | Documentation |
| [openconstruct-examples](https://github.com/SuperInstance/openconstruct-examples) | — | Examples |
| [openconstruct-catalog](https://github.com/SuperInstance/openconstruct-catalog) | — | Component catalog |
| [openconstruct-landing](https://github.com/SuperInstance/openconstruct-landing) | — | Landing page |
| [openconstruct-mercury](https://github.com/SuperInstance/openconstruct-mercury) | — | Mercury variant |
| [openconstruct-jupyter](https://github.com/SuperInstance/openconstruct-jupyter) | Python | Jupyter integration |

### Vessel (Marine/Industrial)

| Repo | Description |
|------|-------------|
| [vessel](https://github.com/SuperInstance/vessel) | Core vessel definition |
| [vessel-prototype](https://github.com/SuperInstance/vessel-prototype) | Prototype implementation |
| [vessel-template](https://github.com/SuperInstance/vessel-template) | Template for new vessels |
| [vessel-constellation](https://github.com/SuperInstance/vessel-constellation) | Fleet of vessels |
| [vessel-room-navigator](https://github.com/SuperInstance/vessel-room-navigator) | Room navigation for vessels |

### Kintsugi (Fault Tolerance)

Kintsugi Math applies the Japanese art of golden repair to software — fault tolerance as aesthetic principle.

| Repo | Language | Description |
|------|----------|-------------|
| [kintsugi-math](https://github.com/SuperInstance/kintsugi-math) | Python | Mathematical patterns for graceful error recovery |
| [kintsugi-math-c](https://github.com/SuperInstance/kintsugi-math-c) | C | C implementation |
| [kintsugi-math-npm](https://github.com/SuperInstance/kintsugi-math-npm) | JS | NPM package |
| [kintsugi-math-wasm](https://github.com/SuperInstance/kintsugi-math-wasm) | WASM | WebAssembly compilation |

### OpenMind

| Repo | Description |
|------|-------------|
| [openmind](https://github.com/SuperInstance/openmind) | Core openmind system |
| [openmind-conductor](https://github.com/SuperInstance/openmind-conductor) | Conductor |
| [openmind-cellular](https://github.com/SuperInstance/openmind-cellular) | Cellular automata |
| [openmind-mirror](https://github.com/SuperInstance/openmind-mirror) | Mirror system |
| [openmind-esp32-bridge](https://github.com/SuperInstance/openmind-esp32-bridge) | ESP32 bridge |

### Edge Relay & Workers

| Repo | Description |
|------|-------------|
| [edge-relay-agent](https://github.com/SuperInstance/edge-relay-agent) | Standalone research relay |
| [edge-research-relay](https://github.com/SuperInstance/edge-research-relay) | Research data relay |
| [edge-conservation-rs](https://github.com/SuperInstance/edge-conservation-rs) | Conservation tracking on edge (Rust) |
| [edge-conservation-worker](https://github.com/SuperInstance/edge-conservation-worker) | Conservation worker |
| [edge-benchmark](https://github.com/SuperInstance/edge-benchmark) | Edge benchmarking |
| [nexus-runtime](https://github.com/SuperInstance/nexus-runtime) | Runtime for connecting distributed services |

### Marine & GPU Edge

| Repo | Language | Description |
|------|----------|-------------|
| [marine-gpu-edge](https://github.com/SuperInstance/marine-gpu-edge) | CUDA | GPU edge computing for marine sensor fusion |
| [open-mythos-edge](https://github.com/SuperInstance/open-mythos-edge) | — | Mythos edge deployment |

### Other

| Repo | Description |
|------|-------------|
| [openrooms](https://github.com/SuperInstance/openrooms) | Open room system |
| [openshell-pythagorean48](https://github.com/SuperInstance/openshell-pythagorean48) | Pythagorean 48 shell |
| [openshell-compatibility-audit](https://github.com/SuperInstance/openshell-compatibility-audit) | Compatibility auditing |
| [opensmile-bridge](https://github.com/SuperInstance/opensmile-bridge) | OpenSMILE audio bridge |
| [openmanus-fleet](https://github.com/SuperInstance/openmanus-fleet) | OpenManus fleet |
| [openmanus-vessel](https://github.com/SuperInstance/openmanus-vessel) | OpenManus vessel |

---

## Architecture

```
┌────────────────────────────────────────────────────┐
│              Fleet / Cloud Layer                     │
└───────────────────────┬────────────────────────────┘
                        │
┌───────────────────────▼────────────────────────────┐
│            Edge Relay Layer                          │
│   (edge-relay-agent, nexus-runtime, edge-benchmark) │
└───────────────────────┬────────────────────────────┘
                        │
        ┌───────────────┼───────────────┐
        │               │               │
┌───────▼──────┐ ┌──────▼──────┐ ┌──────▼──────┐
│   ESP32      │ │  Jetson     │ │  ARM64      │
│  (micro)     │ │  (GPU edge) │ │  (server)   │
└───────┬──────┘ └──────┬──────┘ └──────┬──────┘
        │               │               │
        └───────────────┼───────────────┘
                        │
┌───────────────────────▼────────────────────────────┐
│         OpenConstruct ABI Layer                      │
│   C ABI + 12+ language SDKs                          │
│   onboard() → register → exchange messages           │
└───────────────────────┬────────────────────────────┘
                        │
┌───────────────────────▼────────────────────────────┐
│         Holodeck Simulation Layer                    │
│   (C, Rust, Go, Zig, CUDA — rooms, agents, gauges)  │
└────────────────────────────────────────────────────┘
```

---

## Assessment

The edge/embedded ecosystem bridges the gap between fleet infrastructure and physical devices. The OpenConstruct universal ABI with 12+ language bindings is ambitious — bringing AI agent protocols to ESP32 microcontrollers is genuinely interesting, though resource constraints make full integration challenging.

The multi-language holodeck ports (C, Rust, Go, Zig, CUDA) show commitment to accessibility. The marine GPU edge computing for vessel sensor fusion is specialized and potentially valuable for oceanography and naval applications.

Kintsugi math — fault tolerance as aesthetic principle — is a creative framing for an important problem, though the fault tolerance space is crowded with established patterns.

The vessel system (prototype, template, constellation, room navigator) provides a structured way to deploy fleet agents to physical hardware.

---

*Individual repo summaries are in `edge-{repo-name}.md` files in this directory.*
