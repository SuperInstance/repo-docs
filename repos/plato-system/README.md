# PLATO Ecosystem — Repo Index

PLATO (Protocol for Layered Agent Tile Orchestration) is a room-based agent system
where knowledge is stored as tiles within rooms, agents navigate between rooms,
and a deadband protocol governs decision-making priorities.

---

## Overview Statistics

- **Total repos:** 262
- **Substantial docs (2000+ bytes):** 99
- **Moderate docs (500-2000 bytes):** 73
- **Minimal docs (120-500 bytes):** 21
- **Stubs (<120 bytes):** 69
- **No README at all:** 0


## Core Infrastructure (11 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-config](./plato-config.md) | Configuration management — env vars, file loading, and typed defaults for plato-... | 🟢 moderate (560b) |
| [plato-core](./plato-core.md) | Foundation types and mesh registry for the SuperInstance ecosystem. Standalone, ... | 🟢 substantial (3916b) |
| [plato-event](./plato-event.md) | Event bus for PLATO nervous system | 🟢 moderate (1827b) |
| [plato-kernel](./plato-kernel.md) | Central state machine — DCS flywheel, belief scoring, tile processing, deadband ... | 🟢 moderate (854b) |
| [plato-mud-server](./plato-mud-server.md) | PLATO MUD Server - text-based agent training ground, 16 rooms | 🟢 moderate (1414b) |
| [plato-runtime](./plato-runtime.md) | Self-discovering, self-optimizing compute runtime — tiny core, grows to fill res... | 🟢 substantial (4152b) |
| [plato-runtime-kernel](./plato-runtime-kernel.md) | Runtime kernel for PLATO — the AI theorem prover. Conservation-verified computat... | 🟢 substantial (6468b) |
| [plato-schema](./plato-schema.md) | JSON schema validation and versioning for PLATO messages | 🟢 moderate (1386b) |
| [plato-server](./plato-server.md) | PLATO — Standalone knowledge system. Run your own. Connect to the fleet. Make ev... | 🟢 substantial (15301b) |
| [plato-shell](./plato-shell.md) | Plato Shell — the agent runtime environment. Command execution, context manageme... | 🟢 substantial (2186b) |
| [plato-types](./plato-types.md) | Core types for the PLATO tile protocol — lifecycle, Lamport clocks, provenance | 🟢 moderate (1249b) |

## Room System (19 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-room-acl](./plato-room-acl.md) | Room ACL — PLATO framework | 🔴 stub (81b) |
| [plato-room-analytics](./plato-room-analytics.md) | Room analytics — PLATO framework | 🟡 minimal (122b) |
| [plato-room-configs](./plato-room-configs.md) | Production-ready room configurations for the Plato Matrix — JSON schemas, Rust v... | 🟢 moderate (1667b) |
| [plato-room-context](./plato-room-context.md) | Room state tracking with context signals — awareness of room transitions and act... | 🔴 stub (94b) |
| [plato-room-engine](./plato-room-engine.md) | Room execution — enter, leave, message, tile management | 🔴 stub (16b) |
| [plato-room-intelligence](./plato-room-intelligence.md) | Multi-head room intelligence model with provenance tracking for PLATO rooms | 🟢 substantial (3593b) |
| [plato-room-invite](./plato-room-invite.md) | Room invites — PLATO framework | 🟡 minimal (124b) |
| [plato-room-memory](./plato-room-memory.md) | Per-room persistent memory with sliding context window — room-scoped recall with... | 🔴 stub (106b) |
| [plato-room-musician](./plato-room-musician.md) | 🎼 PLATO rooms → MIDI — room=musician, tile=note, fleet activity becomes a musica... | 🟢 substantial (8382b) |
| [plato-room-nav](./plato-room-nav.md) | Breadcrumb trails — push, back, forward with full history | 🔴 stub (84b) |
| [plato-room-persist](./plato-room-persist.md) | JSONL journal — event replay, room snapshots, agent tracking | 🔴 stub (78b) |
| [plato-room-phi](./plato-room-phi.md) | PLATO room knowledge integration measurement - Phi computation for tile quality ... | 🟢 substantial (2849b) |
| [plato-room-presence](./plato-room-presence.md) | Room presence — PLATO framework | 🟡 minimal (139b) |
| [plato-room-runtime](./plato-room-runtime.md) | Room lifecycle — create, destroy, state transitions, history | 🟡 minimal (124b) |
| [plato-room-scheduler](./plato-room-scheduler.md) | Temperature scheduler — Cold/Warm/Hot/Crystallized training triggers | 🔴 stub (16b) |
| [plato-room-search](./plato-room-search.md) | Cross-room discovery — Exact, Tag, Domain, Keyword, Fuzzy matching | 🔴 stub (97b) |
| [plato-room-server](./plato-room-server.md) | PLATO Room Server - zero-trust tile submission, 15 rooms, 16K+ tiles | 🔴 stub (90b) |
| [plato-room-wasm](./plato-room-wasm.md) | Plato Room system — knowledge rooms with tiles, dependencies, and CR scoring, co... | 🟢 substantial (2548b) |
| [plato-room-webhook](./plato-room-webhook.md) | Room webhooks — PLATO framework | 🟡 minimal (122b) |

## Tile Processing (36 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-tile-api](./plato-tile-api.md) | Stateful tile API — process, search, score, rank in one interface | 🟡 minimal (213b) |
| [plato-tile-batch](./plato-tile-batch.md) | Bulk operations — validate, filter, dedup, partition in batch | 🟡 minimal (208b) |
| [plato-tile-bridge](./plato-tile-bridge.md) | C to Rust — 384-byte tile conversion for cross-language pipelines | 🔴 stub (117b) |
| [plato-tile-cache](./plato-tile-cache.md) | LRU with TTL — hit rate tracking, top hits, bulk expiration | 🟢 moderate (570b) |
| [plato-tile-cascade](./plato-tile-cascade.md) | Propagation — update tiles and invalidate downstream dependents | 🟡 minimal (270b) |
| [plato-tile-client](./plato-tile-client.md) | HTTP client — PLATO tile server with deadband awareness | 🔴 stub (105b) |
| [plato-tile-current](./plato-tile-current.md) | Live tiles — export/import between fleet nodes in real-time | 🔴 stub (16b) |
| [plato-tile-dedup](./plato-tile-dedup.md) | 4-stage similarity — exact, keyword Jaccard, embedding cosine, structure with me... | 🔴 stub (16b) |
| [plato-tile-encoder](./plato-tile-encoder.md) | Serialization — JSON, 384-byte binary, and base64 codecs | 🟢 moderate (567b) |
| [plato-tile-export](./plato-tile-export.md) | Tile export — PLATO framework | 🟡 minimal (124b) |
| [plato-tile-feedback](./plato-tile-feedback.md) | Tile feedback — PLATO framework | 🟡 minimal (129b) |
| [plato-tile-fountain](./plato-tile-fountain.md) | Auto-generate — extract tiles from docs, headings, FAQs, code comments | 🔴 stub (112b) |
| [plato-tile-governance](./plato-tile-governance.md) | Tile governance — PLATO framework | 🟡 minimal (121b) |
| [plato-tile-graph](./plato-tile-graph.md) | Dependency DAG — impact radius, cycle detection, topological sort | 🔴 stub (69b) |
| [plato-tile-import](./plato-tile-import.md) | Format bridges — Markdown, JSON, CSV, plaintext to canonical tiles | 🔴 stub (107b) |
| [plato-tile-library](./plato-tile-library.md) | Complete PLATO tile library — backup of all rooms for shared access and git-nati... | 🟢 moderate (1148b) |
| [plato-tile-merge](./plato-tile-merge.md) | PLATO tile merging — deduplication, conflict resolution, and semantic consolidat... | 🔴 stub (98b) |
| [plato-tile-metrics](./plato-tile-metrics.md) | Fleet analytics — domain distribution, confidence histogram, growth rate | 🔴 stub (84b) |
| [plato-tile-notifications](./plato-tile-notifications.md) | Tile notifications — PLATO framework | 🟡 minimal (124b) |
| [plato-tile-pinboard](./plato-tile-pinboard.md) | Tile pinboard — PLATO framework | 🔴 stub (119b) |
| [plato-tile-pipeline](./plato-tile-pipeline.md) | One-call facade — validate, score, store, search, rank in one step | 🟡 minimal (235b) |
| [plato-tile-priority](./plato-tile-priority.md) | Deadband queue — P0/P1/P2 urgency scoring and drain-by-level | 🟢 moderate (569b) |
| [plato-tile-prompt](./plato-tile-prompt.md) | Context assembly — 4 format styles, budget management, deadband injection | 🟡 minimal (224b) |
| [plato-tile-query](./plato-tile-query.md) | Fluent query builder for PLATO tiles — filter, search, sort, paginate across roo... | 🔴 stub (112b) |
| [plato-tile-ranker](./plato-tile-ranker.md) | Multi-signal ranking — keyword gating, deadband priority boost, top-N | 🔴 stub (77b) |
| [plato-tile-relation](./plato-tile-relation.md) | Tile relationship graph — PLATO framework | 🟡 minimal (153b) |
| [plato-tile-room-bridge](./plato-tile-room-bridge.md) | Tile to room — feed, transfer, unfeed, temperature stats | 🔴 stub (16b) |
| [plato-tile-scorer](./plato-tile-scorer.md) | 7-signal scoring — keyword, belief, domain, temporal, ghost, frequency, controve... | 🔴 stub (16b) |
| [plato-tile-search](./plato-tile-search.md) | Nearest-neighbor — keyword overlap, domain matching, composite ranking | 🟡 minimal (492b) |
| [plato-tile-spec](./plato-tile-spec.md) | Canonical tile format v2.1 — domain, confidence, belief, provenance, 384-byte bi... | 🟢 moderate (1268b) |
| [plato-tile-spec-c](./plato-tile-spec-c.md) | C binding — canonical tile struct, stack-allocatable, CUDA-compatible | 🟢 moderate (732b) |
| [plato-tile-split](./plato-tile-split.md) | Tile decomposition engine — split tiles by sentence, paragraph, or size for gran... | 🔴 stub (97b) |
| [plato-tile-store](./plato-tile-store.md) | Immutable storage — version history, dependency cascade, JSONL persistence | 🔴 stub (95b) |
| [plato-tile-validate](./plato-tile-validate.md) | Quality gates — confidence, freshness, completeness, domain, quality, similarity | 🔴 stub (16b) |
| [plato-tile-version](./plato-tile-version.md) | Git-for-knowledge — commit, branch, merge, rollback | 🔴 stub (89b) |
| [plato-tile-watcher](./plato-tile-watcher.md) | Tile decay monitoring and ghost alerts — track stale tiles and trigger resurrect... | 🔴 stub (92b) |

## Agent Framework (13 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-address](./plato-address.md) | Room navigation — addressing protocol for fleet coordination | 🔴 stub (99b) |
| [plato-agent-academy](./plato-agent-academy.md) | Agent Academy for PLATO MUD — zero-shot agent training, power packs, captain's c... | 🟢 substantial (2190b) |
| [plato-agent-python](./plato-agent-python.md) | Python agent framework for Plato Engine Blocks — connect to rooms, observe ticks... | 🟢 substantial (13060b) |
| [plato-coordination](./plato-coordination.md) | Cross-room fleet coordination for PLATO nervous system | 🟢 moderate (930b) |
| [plato-dcs](./plato-dcs.md) | DCS flywheel — belief, deploy policy, dynamic locks consensus | 🟢 moderate (1189b) |
| [plato-deadband](./plato-deadband.md) | Deadband Protocol engine — P0 rock / P1 channel / P2 optimize priority governanc... | 🟡 minimal (496b) |
| [plato-escalation-gate](./plato-escalation-gate.md) | Tiny escalation decision gate — 737 params (4KB), WASM-ready binary classifier | 🟢 substantial (2328b) |
| [plato-i2i-dcs](./plato-i2i-dcs.md) | Multi-agent consensus — BeliefScore, LockAccumulator, ConsensusRound | 🔴 stub (16b) |
| [plato-relay](./plato-relay.md) | Async relay — trust-weighted message prioritization | 🟢 moderate (975b) |
| [plato-relay-tidepool](./plato-relay-tidepool.md) | Message board — async TidePool for non-blocking communication | 🔴 stub (16b) |
| [plato-scout](./plato-scout.md) | Fleet observation and routing framework | 🟢 substantial (14858b) |
| [plato-ship](./plato-ship.md) | CCC's PLATO Runtime for distributed cognition. Fleet coordination through Nexus ... | 🟢 substantial (5254b) |
| [plato-ship-protocol](./plato-ship-protocol.md) | Fleet coordination — vessel handshakes and discovery | 🔴 stub (16b) |

## Engine Blocks (Multi-Language) (5 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-engine-block](./plato-engine-block.md) | Atomic room runtime for the Plato Matrix — universal agent-space interface | 🟢 substantial (8454b) |
| [plato-engine-block-c](./plato-engine-block-c.md) | Tiny embeddable sensor→history→alarm engine in C99. Zero dynamic allocation. Run... | 🟢 substantial (10852b) |
| [plato-engine-block-elixir](./plato-engine-block-elixir.md) | Fault-tolerant marine vessel monitoring system on BEAM/OTP — ternary sensor logi... | 🟢 substantial (14134b) |
| [plato-engine-block-gleam](./plato-engine-block-gleam.md) |  | 🟢 substantial (4200b) |
| [plato-engine-block-zig](./plato-engine-block-zig.md) |  | 🟢 substantial (12624b) |

## Signal Processing & DSP (10 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-anomaly](./plato-anomaly.md) | Anomaly detection methods for PLATO tile streams | 🟢 substantial (2008b) |
| [plato-compress](./plato-compress.md) | Lossless and lossy compression for PLATO tile data | 🟢 substantial (2307b) |
| [plato-correlate](./plato-correlate.md) | Cross-correlation and dependency detection for PLATO tile streams | 🟢 substantial (2369b) |
| [plato-downsample](./plato-downsample.md) | Intelligent downsampling for PLATO tile streams with anomaly preservation | 🟢 substantial (2054b) |
| [plato-filter](./plato-filter.md) | Digital signal processing filters for PLATO tile streams | 🟢 substantial (3283b) |
| [plato-normalize](./plato-normalize.md) | Normalization and standardization for PLATO tile values | 🟢 substantial (2539b) |
| [plato-ring](./plato-ring.md) | Lock-free ring buffer for PLATO high-frequency sensor data | 🟢 substantial (2216b) |
| [plato-signal-chain](./plato-signal-chain.md) | Composable 5-layer signal chain pipeline for PLATO rooms | 🟢 moderate (1052b) |
| [plato-transform](./plato-transform.md) | Data transformation pipeline for PLATO tiles | 🟢 substantial (3006b) |
| [plato-window](./plato-window.md) | Sliding window operations for PLATO tile streams and JEPA context | 🟢 moderate (1771b) |

## ML/AI & Training (23 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-audio-jepa](./plato-audio-jepa.md) |  | 🟢 substantial (4039b) |
| [plato-backprop](./plato-backprop.md) | Backpropagation-through-prompt tracking for PLATO nano models | 🟢 moderate (1607b) |
| [plato-cortex](./plato-cortex.md) | Cross-database mapping layer for Dual-DB JEPA perception-prediction spaces | 🟢 moderate (1614b) |
| [plato-diffusion](./plato-diffusion.md) | Progressive distillation pipeline for PLATO room intelligence | 🟢 moderate (848b) |
| [plato-distill](./plato-distill.md) | Progressive knowledge distillation tracking for PLATO rooms | 🟢 substantial (3750b) |
| [plato-fflearning](./plato-fflearning.md) | Predictive coding without backpropagation — Forward-Forward learning for PLATO f... | 🟢 substantial (5222b) |
| [plato-forge-bridge](./plato-forge-bridge.md) | Bridge between ForgeFlux tile decomposition and Plato agent rooms | 🟢 substantial (3504b) |
| [plato-forge-buffer](./plato-forge-buffer.md) | Stomach — prioritized replay, curriculum-balanced sampling 70/20/10 | 🔴 stub (118b) |
| [plato-forge-daemon](./plato-forge-daemon.md) | Continuous learning daemon — the Forgemaster's GPU training loop | 🟢 substantial (2437b) |
| [plato-forge-emitter](./plato-forge-emitter.md) | Lungs — emit training artifacts, auto-version, quality gate | 🟡 minimal (121b) |
| [plato-forge-listener](./plato-forge-listener.md) | Cochlea — classify events, detect knowledge gaps, frame training signals | 🟡 minimal (120b) |
| [plato-forge-pipeline](./plato-forge-pipeline.md) | PLATO forge pipeline — automated tile generation and room training | 🔴 stub (16b) |
| [plato-forge-trainer](./plato-forge-trainer.md) | Heart — GPU job manager, LoRA/Embedding/Genome modes | 🔴 stub (118b) |
| [plato-inference-runtime](./plato-inference-runtime.md) | Engine — model plus adapters, forward pass as scheduler | 🔴 stub (117b) |
| [plato-jepa](./plato-jepa.md) | JEPA primitives for tile representation learning in PLATO rooms | 🟢 substantial (6121b) |
| [plato-jepa-dual](./plato-jepa-dual.md) | Dual-database JEPA: separate perception and prediction vector spaces with cross-... | 🟢 moderate (1645b) |
| [plato-model-ocean](./plato-model-ocean.md) | Cellular intelligence ecosystem — evolutionary neural networks in ecological nic... | 🟢 substantial (3585b) |
| [plato-mythos](./plato-mythos.md) | PLATO-native Recurrent-Depth Transformer — rooms as MoE experts, tiles as KV, de... | 🟢 substantial (9316b) |
| [plato-mythos-bridge](./plato-mythos-bridge.md) |  | 🟢 substantial (7403b) |
| [plato-mythos-glue](./plato-mythos-glue.md) | Runtime glue between PLATO Room Server and plato-mythos model — pure stdlib, no ... | 🔴 stub (16b) |
| [plato-neural-kernel](./plato-neural-kernel.md) | Synapse — execution traces to training pairs for neural Plato | 🟡 minimal (192b) |
| [plato-torch](./plato-torch.md) | GPU forge — PyTorch training loop with tile framing | 🟢 substantial (7392b) |
| [plato-vision-jepa](./plato-vision-jepa.md) |  | 🟢 substantial (3814b) |

## Fleet & Coordination (4 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-fleet](./plato-fleet.md) | Fleet management for Plato Shell — multi-agent orchestration, scaling, and coord... | 🟢 moderate (1912b) |
| [plato-fleet-chapel](./plato-fleet-chapel.md) |  | 🟢 substantial (13697b) |
| [plato-fleet-graph](./plato-fleet-graph.md) | Fleet dependency graph — 83 nodes, impact analysis | 🔴 stub (95b) |
| [plato-fleet-manager](./plato-fleet-manager.md) | Fleet orchestration for Plato room engine blocks across devices | 🟢 substantial (10852b) |

## Clients & SDKs (7 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-agent-connect](./plato-agent-connect.md) | One-command CLI to join the PLATO fleet. ⛵ npx @superinstance/plato-agent-connec... | 🟢 substantial (2056b) |
| [plato-client](./plato-client.md) | PLATO client library — connect to PLATO rooms from any application. | 🟢 substantial (5161b) |
| [plato-client-js](./plato-client-js.md) | PLATO room protocol client — Node + browser, zero dependencies | 🟢 substantial (4583b) |
| [plato-client-php](./plato-client-php.md) | PHP client library for PLATO room server — interact with PLATO tiles, rooms, and... | 🟢 substantial (12050b) |
| [plato-client-ruby](./plato-client-ruby.md) | Ruby client for PLATO backend — room/tile CRUD, knowledge graph queries | 🟢 moderate (1509b) |
| [plato-sdk](./plato-sdk.md) | Build agents that live in PLATO. Any model, any hardware, any armor. pip install... | 🟢 substantial (11044b) |
| [plato-sdk-unified](./plato-sdk-unified.md) | Unified SDK — all 8 PLATO consciousness packages in one import | 🟢 substantial (3257b) |

## Bridges & Integrations (15 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-adapter-store](./plato-adapter-store.md) | Vault — LoRA adapter versioning, deploy, improvement tracking | 🟡 minimal (123b) |
| [plato-adapters](./plato-adapters.md) | PLATO adapter implementations — connect PLATO rooms to external services and pro... | 🟢 moderate (1038b) |
| [plato-address-bridge](./plato-address-bridge.md) | Cross-layer routing — address protocol to tile transport | 🔴 stub (16b) |
| [plato-bridge](./plato-bridge.md) | Connect PLATO rooms to Telegram, Discord, fleet bottles. Messages appear in room... | 🔴 stub (97b) |
| [plato-hdc-bridge](./plato-hdc-bridge.md) |  | 🟢 moderate (1411b) |
| [plato-llvm-bridge](./plato-llvm-bridge.md) |  | 🟢 moderate (1694b) |
| [plato-matrix-bridge](./plato-matrix-bridge.md) | Agent shell module: connects local PLATO to fleet Matrix mesh. Channels + presen... | 🟢 substantial (2898b) |
| [plato-mcp](./plato-mcp.md) | PLATO rooms as MCP tools. Any MCP-compatible framework can use PLATO as a backen... | 🟢 substantial (3961b) |
| [plato-mcp-bridge](./plato-mcp-bridge.md) | Claude Code bridge — JSON-RPC 2.0, 5 MCP tools | 🔴 stub (97b) |
| [plato-midi-bridge](./plato-midi-bridge.md) | PLATO rooms as musicians — connects FM's flux-tensor-midi to live fleet tiles | 🟢 moderate (667b) |
| [plato-midi-bridge-rs](./plato-midi-bridge-rs.md) | Rust crate — Eisenstein lattices, Penrose tilings, and multi-scale musical style... | 🔴 stub (16b) |
| [plato-shell-bridge](./plato-shell-bridge.md) | The weapon rack — dynamic tool discovery, loading, and lifecycle for PLATO shell... | 🟢 moderate (1044b) |
| [plato-sim-bridge](./plato-sim-bridge.md) | 🌉 PLATO ↔ Fleet simulator bridge | 🟢 moderate (1684b) |
| [plato-ternary-bridge](./plato-ternary-bridge.md) | Bridges Plato room sensor values to ternary {-1, 0, +1} states for alarm evaluat... | 🟢 substantial (12844b) |
| [plato-visual-mesh-mcp](./plato-visual-mesh-mcp.md) | MCP tools for visual memory mesh queries | 🟢 moderate (932b) |

## Vessels (IoT/Hardware) (4 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-vessel-core](./plato-vessel-core.md) | Tiny C PLATO client for ESP32/RP2040 + embodiment protocol: agents discover IoT ... | 🟢 substantial (6273b) |
| [plato-vessel-educational](./plato-vessel-educational.md) | Student + instructor agent for PLATO-enabled IoT classrooms. Students focus on p... | 🟢 substantial (4268b) |
| [plato-vessel-rapid-prototype](./plato-vessel-rapid-prototype.md) | Product developer iteration loop: describe a project → get BOM, wiring diagram, ... | 🟢 substantial (3657b) |
| [plato-vessel-technician](./plato-vessel-technician.md) | Deckboss — marine/industrial technician agent for PLATO. Voice-first, fail-safe,... | 🟢 substantial (5325b) |

## Security & Governance (8 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-constraints](./plato-constraints.md) | Rule enforcement — forbidden patterns and boundary checks | 🟢 moderate (561b) |
| [plato-deploy-policy](./plato-deploy-policy.md) | Classification — P0 immediate, P1 scheduled, P2 deferred | 🔴 stub (16b) |
| [plato-kernel-constraints](./plato-kernel-constraints.md) | Preserved workspace artifact | 🟢 substantial (2649b) |
| [plato-policy](./plato-policy.md) | Policy engine that gates what agents can do — per-module, per-agent, per-context... | 🟢 moderate (1990b) |
| [plato-provenance](./plato-provenance.md) | 🔐 Zero-trust tile provenance — signing, chain verification, trust scoring | 🟢 moderate (1014b) |
| [plato-sandbox](./plato-sandbox.md) | Sandboxed execution environment for Plato Shell — isolated agent runtime with re... | 🟢 moderate (1893b) |
| [plato-trust-beacon](./plato-trust-beacon.md) | Trust events — success, failure, timeout, corruption, resurrect | 🔴 stub (16b) |
| [plato-validate](./plato-validate.md) | Input validation and sanitization for PLATO tile data | 🟢 substantial (2031b) |

## Music & Audio (2 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-music-sync](./plato-music-sync.md) | Music cognition patterns for synchronizing Plato rooms — polyrhythmic scheduling... | 🟢 substantial (10371b) |
| [plato-timing](./plato-timing.md) | Tensor MIDI timing for PLATO room agent coordination | 🟢 moderate (672b) |

## Developer Tools (8 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-cli](./plato-cli.md) | PLATO in one binary — search tiles, check deadband, navigate rooms | 🟢 substantial (3031b) |
| [plato-dashboard](./plato-dashboard.md) | Fleet dashboard rendering for PLATO nervous system | 🟢 substantial (6026b) |
| [plato-demo](./plato-demo.md) | HN demo — pre-seeded knowledge, visible deadband, zero setup | 🟢 substantial (7084b) |
| [plato-hooks](./plato-hooks.md) | Git hooks for real-time PLATO room events. Commits become messages. | 🔴 stub (81b) |
| [plato-quickstart](./plato-quickstart.md) | Bootstrap a Plato room in 30 seconds. CLI tool: init, validate, simulate, fleet.... | 🟢 substantial (4331b) |
| [plato-ship-demo](./plato-ship-demo.md) | Minimal MUD server for zeroshot external agent testing — room-as-system-prompt p... | 🟢 moderate (1743b) |
| [plato-studio](./plato-studio.md) | Studio-quality web dashboard for PLATO knowledge store | 🟢 moderate (1167b) |
| [plato-tui](./plato-tui.md) | 🖥️ PLATO terminal UI | 🟢 substantial (2510b) |

## Web & UI (5 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-browser](./plato-browser.md) | PLATO Nervous System browser demo — real-time sensor monitoring with Chrome AI | 🟢 substantial (3582b) |
| [plato-construct](./plato-construct.md) | PLATO — The Construct. Open source loading program for AI agents. Educate, don't... | 🟢 substantial (3876b) |
| [plato-observation](./plato-observation.md) | PLATO Observation Chamber — watch autonomous agents organize themselves via spec... | 🔴 stub (16b) |
| [plato-portal](./plato-portal.md) |  | 🟢 substantial (7782b) |
| [plato-voice](./plato-voice.md) |  | 🟢 substantial (2337b) |

## Archived/Early Versions (4 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-alignments-early-version](./plato-alignments-early-version.md) | [ARCHIVED] Early snap-point alignment experiment. Concept absorbed into SuperIns... | 🟢 moderate (648b) |
| [plato-calibration-early-version](./plato-calibration-early-version.md) | [ARCHIVED] Early calibration experiment. 1KB scaffolding only. | 🟢 moderate (542b) |
| [plato-hologram-early-version](./plato-hologram-early-version.md) | [ARCHIVED] Early vectorized field experiment. 1KB scaffolding only. | 🟢 moderate (544b) |
| [plato-stable-early-version](./plato-stable-early-version.md) | [ARCHIVED] Early seed model experiment. Concept absorbed into SuperInstance/plat... | 🟢 moderate (634b) |

## Other / Unclear (88 repos)

| Repo | Description | Substance |
|------|-------------|-----------|
| [plato-a2a](./plato-a2a.md) | Agent-to-Agent protocol for Plato Shell — inter-agent communication, capability ... | 🟢 substantial (2137b) |
| [plato-achievement](./plato-achievement.md) | Achievement Loss — progress measurement with milestones | 🔴 stub (98b) |
| [plato-afterlife](./plato-afterlife.md) | 👻 Agent lifecycle — tombstones, ghost tiles, knowledge preservation beyond agent... | 🟢 moderate (728b) |
| [plato-afterlife-reef](./plato-afterlife-reef.md) | PLATO afterlife reef — ghost tile aggregation and resurrection (P2P mesh) | 🔴 stub (103b) |
| [plato-alert](./plato-alert.md) | Alert management for PLATO — creation, routing, acknowledgment, escalation | 🟢 substantial (2643b) |
| [plato-attention-tracker](./plato-attention-tracker.md) | Attention as a first-class resource in PLATO | 🟢 substantial (4323b) |
| [plato-autonomy](./plato-autonomy.md) | Autonomy metrics and reporting for PLATO rooms | 🟢 moderate (798b) |
| [plato-backtest](./plato-backtest.md) | Backtesting framework for PLATO signal chain configurations | 🟢 moderate (1789b) |
| [plato-capability](./plato-capability.md) | Capability descriptors and negotiation for PLATO rooms and agents | 🟢 substantial (2554b) |
| [plato-conserve](./plato-conserve.md) | Conservation law tracking for PLATO tile transformations | 🟢 moderate (1602b) |
| [plato-contract](./plato-contract.md) | Contract definitions for Plato Shell — typed interfaces between agent modules | 🟢 moderate (1668b) |
| [plato-correlator](./plato-correlator.md) | Event correlation engine for Plato Shell — pattern detection across agent intera... | 🟢 moderate (1836b) |
| [plato-data](./plato-data.md) | Data loading for PLATO rooms — CSV, JSONL, PLATO tiles, fleet telemetry | 🟢 moderate (921b) |
| [plato-dmn-ecm](./plato-dmn-ecm.md) | DMN-ECN reverse-actualization engine — creativity via functional distance | 🔴 stub (16b) |
| [plato-dojo](./plato-dojo.md) | A repo-native agent framework demonstrating perspective-decoupling through cultu... | 🟢 substantial (3719b) |
| [plato-dynamic-locks](./plato-dynamic-locks.md) | Evidence accumulation — critical mass at n >= 7 | 🔴 stub (16b) |
| [plato-e2e-pipeline](./plato-e2e-pipeline.md) | End-to-end — mint through cascade in one test | 🔴 stub (16b) |
| [plato-e2e-pipeline-v2](./plato-e2e-pipeline-v2.md) | Enhanced e2e — full v2 pipeline integration | 🔴 stub (16b) |
| [plato-edge](./plato-edge.md) | Edge-optimized Cocapn fleet packages for ARM64 — pure Python, zero deps, <100KB | 🟢 substantial (2616b) |
| [plato-embed](./plato-embed.md) | Embedding utilities for PLATO tile similarity, clustering, and JEPA | 🟢 substantial (2506b) |
| [plato-engine](./plato-engine.md) | Extracted from forgemaster/plato-engine — Cocapn fleet component | 🟢 substantial (3850b) |
| [plato-ensign](./plato-ensign.md) | Knowledge compression — export compressed fleet packages | 🟢 substantial (2585b) |
| [plato-experience](./plato-experience.md) | The breeding farm for AI agents. Purpose-first rooms, pheromone trails, kin reco... | 🟢 substantial (2737b) |
| [plato-explain](./plato-explain.md) | Explainability for PLATO predictions — trace lineage through databases | 🟢 moderate (1613b) |
| [plato-flux-compiler](./plato-flux-compiler.md) | plato-flux-compiler — part of the Plato Matrix room runtime stack | 🟢 substantial (9305b) |
| [plato-flux-opcodes](./plato-flux-opcodes.md) | FLUX bytecode — 85-opcode instruction set, Lock Algebra | 🔴 stub (16b) |
| [plato-genepool-tile](./plato-genepool-tile.md) | Gene to tile — bridge genome encoding and tile format | 🔴 stub (16b) |
| [plato-ghostable](./plato-ghostable.md) | Persistence classes — Eternal, Persistent, Ephemeral | 🔴 stub (99b) |
| [plato-hardware-engine](./plato-hardware-engine.md) | plato-hardware-engine | 🟢 moderate (631b) |
| [plato-health](./plato-health.md) | Health check system for PLATO rooms — uptime, response times, error rates | 🟢 substantial (2539b) |
| [plato-history](./plato-history.md) | Historical data storage and time-series queries for PLATO room readings | 🟢 substantial (2145b) |
| [plato-i2i](./plato-i2i.md) | Direct messaging — Iron-to-Iron protocol, trust-weighted routing | 🔴 stub (98b) |
| [plato-instinct](./plato-instinct.md) | Reflex engine — 10 instincts fire before reasoning | 🟢 moderate (904b) |
| [plato-lab-guard](./plato-lab-guard.md) | Hypothesis gating — 12 absolute quantifiers, vague causation | 🟢 substantial (2004b) |
| [plato-live-data](./plato-live-data.md) | Tap — pull tiles from PLATO tile server on port 8847 | 🔴 stub (91b) |
| [plato-live-room](./plato-live-room.md) | Plato Live Room — a simulation of agents in rooms with forward simulations, wall... | 🟢 substantial (3078b) |
| [plato-loader](./plato-loader.md) | PLATO loading program — reads rooms, computes knowledge graphs, produces minimal... | 🟢 moderate (1929b) |
| [plato-manus](./plato-manus.md) | PLATO Manus — manuscript and writing system for knowledge rooms | 🟢 moderate (1863b) |
| [plato-math](./plato-math.md) | Shared vector math primitives for the PLATO ecosystem — distance functions, vect... | 🟢 moderate (1409b) |
| [plato-memory](./plato-memory.md) | Agent memory system — persistence, recall, and consolidation for Plato Shell | 🟢 substantial (2012b) |
| [plato-meta-tiles](./plato-meta-tiles.md) | Meta-tiles for PLATO — tiles about tiles, enabling higher-order reasoning | 🟢 substantial (3084b) |
| [plato-metrics](./plato-metrics.md) | Metrics collection for PLATO signal chain performance | 🟢 substantial (2361b) |
| [plato-ml](./plato-ml.md) | 🎮 MUD-based ML framework: rooms as layers, achievements as loss, narrative gradi... | 🟢 moderate (1853b) |
| [plato-nervous](./plato-nervous.md) | Room-specific model distillation for PLATO rooms — the nervous system signal cha... | 🟢 substantial (3305b) |
| [plato-ng](./plato-ng.md) | Next-gen PLATO: Loop Room architecture with MUD lobby, game rooms, and the conse... | 🟢 moderate (1719b) |
| [plato-observe](./plato-observe.md) | Observability layer for OpenConstruct — metrics, tracing, health checks, and eve... | 🟢 moderate (1676b) |
| [plato-os](./plato-os.md) | Python MUD — PLATO room server with TUTOR anchors | 🟢 substantial (4724b) |
| [plato-perception](./plato-perception.md) | Perception encoding for Z_in side of Dual-DB JEPA | 🟢 moderate (1601b) |
| [plato-playwright](./plato-playwright.md) | Browser/desktop automation module — agents control browsers through text command... | 🟢 moderate (1643b) |
| [plato-predict](./plato-predict.md) | Time series prediction primitives for PLATO tile streams | 🟢 substantial (3027b) |
| [plato-prediction](./plato-prediction.md) | Prediction encoding for Z_out side of Dual-DB JEPA | 🟢 moderate (1602b) |
| [plato-prompt-builder](./plato-prompt-builder.md) | Compose LLM prompts from tile search results — context builder for PLATO | 🔴 stub (16b) |
| [plato-puppeteer](./plato-puppeteer.md) | Desktop to MUD translation: agents navigate UIs as text rooms. Click, type, scro... | 🟢 substantial (2162b) |
| [plato-query-parser](./plato-query-parser.md) | Parse natural language queries into structured intent, keywords, domains | 🔴 stub (104b) |
| [plato-research](./plato-research.md) | 🔬 PLATO research notes and experiments | 🔴 stub (16b) |
| [plato-room](./plato-room.md) | PLATO rooms: knowledge as spectral graph. Tiles with dependencies, failure-first... | 🟢 substantial (2254b) |
| [plato-rooms](./plato-rooms.md) | Room abstraction for PLATO nervous system | 🟢 moderate (1223b) |
| [plato-route](./plato-route.md) | Message routing for PLATO tile distribution | 🟢 moderate (1818b) |
| [plato-semantic-search](./plato-semantic-search.md) |  | 🟢 substantial (5658b) |
| [plato-semantic-sim](./plato-semantic-sim.md) | Semantic similarity for PLATO tiles — Jaccard + cosine similarity for dedup and ... | 🔴 stub (91b) |
| [plato-sentiment-vocab](./plato-sentiment-vocab.md) | Polarity — positive, negative, neutral tile classification | 🔴 stub (16b) |
| [plato-serialize](./plato-serialize.md) | Efficient binary serialization for PLATO tiles optimized for low-bandwidth links... | 🟢 moderate (1651b) |
| [plato-session](./plato-session.md) | Session management for Plato Shell — conversation state, context windows, and se... | 🟢 substantial (2106b) |
| [plato-session-tracer](./plato-session-tracer.md) | Memory — record Command/Response/StateChange traces for training | 🔴 stub (112b) |
| [plato-sim-channel](./plato-sim-channel.md) | Safe discovery — simulation to live bridging | 🔴 stub (16b) |
| [plato-sonar-text](./plato-sonar-text.md) | PLATO Sonar Text — text perception and sonar-based content analysis for PLATO ro... | 🟢 moderate (1726b) |
| [plato-soul-fingerprint](./plato-soul-fingerprint.md) | Preserved workspace artifact | 🟢 substantial (5359b) |
| [plato-spectral](./plato-spectral.md) |  | 🟢 substantial (5233b) |
| [plato-state](./plato-state.md) | 16-dimensional room state vectors for PLATO nervous system | 🟢 moderate (1304b) |
| [plato-surprise-detector](./plato-surprise-detector.md) | PLATO Surprise Detector — tracks prediction errors across the fleet | 🟢 substantial (3927b) |
| [plato-surrogate](./plato-surrogate.md) | Self-healing protocol for PLATO using Free Energy Principle | 🟢 substantial (3191b) |
| [plato-temporal-validity](./plato-temporal-validity.md) | Time windows — Valid, Grace, Expired lifecycle | 🔴 stub (16b) |
| [plato-threshold](./plato-threshold.md) | Adaptive threshold calculation for PLATO deadband filters | 🟢 substantial (2149b) |
| [plato-tick](./plato-tick.md) | Tick scheduler for Plato Shell — periodic tasks, cron-like scheduling, and heart... | 🟢 moderate (1825b) |
| [plato-tiles](./plato-tiles.md) | Preserved workspace artifact | 🟢 moderate (1351b) |
| [plato-tiling](./plato-tiling.md) | Core ops — adaptive search, ghost resurrection, temporal decay | 🔴 stub (101b) |
| [plato-tour-guide](./plato-tour-guide.md) | Wayfinding science as technology — PLATO room tour guide with Penrose scoping an... | 🟢 substantial (2998b) |
| [plato-training](./plato-training.md) | PLATO Training Rooms — LoRA adapters with lifecycle (Active/Superseded/Retracted... | 🟢 moderate (988b) |
| [plato-training-casino](./plato-training-casino.md) | Dealer — stochastic fleet data, deterministic with seed | 🔴 stub (112b) |
| [plato-transport](./plato-transport.md) | Transport layer for Plato Shell — message routing, serialization, and protocol a... | 🟢 moderate (1885b) |
| [plato-tutor](./plato-tutor.md) | Context jumping — WordAnchor extraction, TUTOR_JUMP | 🔴 stub (87b) |
| [plato-twin-maker](./plato-twin-maker.md) | Hermit crab factory: creates PLATO-twin of any repo | 🟢 substantial (5236b) |
| [plato-twin-maker-reports](./plato-twin-maker-reports.md) | External testing report for plato-twin-maker: bugs, fixes, and improvement roadm... | 🟢 substantial (2180b) |
| [plato-uidl](./plato-uidl.md) | Universal Interface Description Language for Plato Shell — render agent output a... | 🟢 moderate (1449b) |
| [plato-unified-belief](./plato-unified-belief.md) | Multi-signal fusion — temporal, ghost, domain, frequency | 🟢 moderate (605b) |
| [plato-vision](./plato-vision.md) | PLATO Vision — visual perception pipeline for PLATO knowledge rooms | 🟢 substantial (2132b) |
| [plato-watch](./plato-watch.md) |  | 🟢 moderate (1924b) |
| [plato-workflow](./plato-workflow.md) | Workflow orchestration for Plato Shell — multi-step agent pipelines with conditi... | 🔴 stub (16b) |

---

## Overall PLATO Ecosystem Assessment

PLATO is an ambitious, sprawling ecosystem of 262+ repositories that implements a 
room-based agent system inspired by the original PLATO terminal-based education system
and MUD (Multi-User Dungeon) architecture. The core ideas:

1. **Knowledge as Tiles** — Q&A pairs with confidence, provenance, and dependencies
2. **Rooms as Containers** — collections of related tiles that compute their own "conservation ratio"
3. **Deadband Protocol** — P0 (safety) → P1 (channel) → P2 (optimize) priority governance
4. **Ternary Sensors** — all sensor readings reduced to {-1, 0, +1} for compact fleet-wide state
5. **Multi-language Engine Blocks** — the room runtime implemented in Rust, C, Elixir, Gleam, Zig, Chapel
6. **Fleet Coordination** — agents discover rooms, navigate between them, and share knowledge

**What's real:** The Rust crates (plato-room, plato-shell, plato-engine-block, plato-ternary-bridge,
plato-flux-compiler, etc.) contain substantial, documented code with real architecture. The Python
SDK (plato-sdk) and server (plato-server) are genuinely functional. The multi-language engine blocks
show real engagement with language-specific strengths.

**What's aspirational:** A large fraction of the repos (especially the "plato-tile-*" and "plato-room-*"
Python packages) are stubs with one-line READMEs. The "plato-*-early-version" repos are explicitly
archived. The ML components (plato-mythos, plato-jepa) are conceptually rich but their training
effectiveness is unproven. The fleet coordination, forge pipeline, and nervous system form a coherent
vision that would require significant integration work to function end-to-end.

**The pattern:** This is a single developer (or small team) rapidly prototyping an entire ecosystem.
The Rust crates are the core; the Python packages fill gaps; the multi-language implementations
demonstrate the concept's portability. The ecosystem is more impressive in breadth than depth,
but the depth where it exists (engine-block, ternary-bridge, flux-compiler, room, server) is genuine.