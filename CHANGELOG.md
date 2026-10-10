# primalSpring — Evolution Record

The changelog is sorted by capability surface, not by date.
Each section tells the arc: what emerged, what it replaced, what it became.
The date-sorted history lives in `CHANGELOG_ARCHIVE.md`.

`H(data|epitope) < H(data|date) < H(data)`

---

## Atomic Harness — live primal spawn, validate, teardown

Shell-script NUCLEUS coordination → pure-Rust synchronous harness with RAII lifecycle, graph-driven startup waves, and capability-based probing.

- **Live Atomic Harness** (v0.3.0→v0.6.0): Absorbed biomeOS coordination into `launcher/` + `harness/` modules — `discover_binary()` (5-tier search), `spawn_primal()`, `SocketNucleation`, `PrimalProcess` RAII, `RunningAtomic::client_for(cap)`.
- **Topological startup** (v0.3.0): Kahn's algorithm `topological_waves()` from deploy graph DAGs replaced sequential spawn lists; `graph.waves` and `graph.capabilities` RPC endpoints expose ordering.
- **Neural API co-start** (v0.3.0): `start_with_neural_api()` + `NeuralBridge` access; exp001 evolved to spawn Tower + Neural API when `ECOPRIMALS_PLASMID_BIN` set.
- **NUCLEUS validation** (v0.6.0): Nest Atomic (socket-only, ZFS degrade) + Node Atomic (dual-protocol toadStool) + exp068 full 3-layer composition; 58/58 gates PASS.
- **Tower stability** (v0.4.0→v0.5.0): 24/24 Tower Atomic gates; `--port 0` ephemeral binding fixed songbird port contention; exp062–065 subsystem sweeps validated live.
- **Composition validation library** (v0.9.10): `CompositionContext`, `validate_parity`, typed IPC extractors, 7 named math tolerances — one-call parity comparison for cross-atomic experiments.

---

## Deploy Graphs & NUCLEUS Atomics — the periodic table of composition

Ad-hoc graph sprawl → atomic-aligned fragments, profiles, and patterns forming the NUCLEUS particle model.

- **Atomic fragments** (v0.9.6): `tower_atomic` (BearDog + Songbird), `node_atomic` (+ ToadStool + barraCuda + coralReef), `nest_atomic` (+ NestGate + provenance trio), `meta_tier`, `nucleus` — aligned to gen3 ECOSYSTEM_ARCHITECTURE §3.
- **NUCLEUS profiles** (v0.9.6): 9 documented slices in `graphs/profiles/` (`tower`, `node`, `nest`, `nucleus`, `full`, `tower_ai`, etc.) replaced 8 root-level subset graphs.
- **Graph consolidation** (v0.9.5→v0.9.10): 107 → 67 deploy graphs; stale `science/`, `sketches/`, `gen4/` fossilized; ludoSpring/esotericWebb rewritten as pure compositions (no spawnable binaries).
- **Proto-nucleate coverage** (v0.9.9): All 7 science springs have proto-nucleate graphs; `NUCLEUS_SPRING_ALIGNMENT.md` documents spring × atomic matrix.
- **Bonding alignment** (v0.9.7): Duplicate bonding tables merged; `nest_atomic` upgraded where provenance trio present; cross-atomic graphs declare `[graph.bonding_policy]`.
- **Foundation validation** (Phase 59): `foundation_validation.toml` 12-node sediment pipeline; exp107 8-phase IPC validation; structural checks require provenance trio for validation-purpose graphs.

---

## Capability Discovery & Registry — finding primals by what they do

Hardcoded `KNOWN_PRIMALS` roster → capability-first resolution with 389+ registered methods and zero drift CI.

- **Capability-first pivot** (v0.3.0): All RPC handlers, discovery, and experiments default to capability resolution; identity-based retained as `mode: "identity"` fallback; 21 niche capabilities in `capability_registry.toml`.
- **Discovery escalation** (Phase 59): 5-tier hierarchy in `CompositionContext::discover()` — Songbird → biomeOS Neural API → UDS → socket registry → TCP probing.
- **Method string SSOT** (Phase 59): PG-65 RESOLVED — `tools/check_method_strings.sh` validates 211 source strings against 389 registered methods; zero drift at ship.
- **Registry evolution** (Phase 60+): 369 → 389 methods (+ionic tokens, +nautilus, +streaming, +composition.reload, +crypto.contract.*).
- **Provenance taxonomy** (Phase 59): `"provenance"` removed from routing aliases; standardized to `by_capability = "dag"` across 8 graph TOMLs.

---

## Neural API & IPC — the validation client's wire stack

Direct socket calls → resilient IPC with circuit breakers, BTSP handshake, and inference wire standard.

- **IPC resilience stack** (v0.2.0): `IpcError` (8 variants), `CircuitBreaker`, `RetryPolicy`, `resilient_call()`, `DispatchOutcome<T>`, 4-format capability parsing.
- **BTSP client handshake** (v0.9.4): `ipc::btsp_handshake` — secure-by-default authentication before capability calls; all 107 deploy graphs carry `secure_by_default = true`.
- **Inference wire standard** (v0.9.4): Vendor-agnostic `inference.complete/embed/models` types + Squirrel bridge; ToadStool semantic cleanup removed unimplemented inference mappings.
- **Health probes** (v0.2.0): `health.liveness` + `health.readiness` Kubernetes-style probes; `CompositionContext::health_check()` normalizes diverse response formats.
- **NestGate transport parity** (Wave 9): Resolved upstream debt; composition trio pipeline validated end-to-end.

---

## Experiments & Validation — pressure-testing the ecosystem

38 scaffold experiments → 89+ live validation experiments driving upstream gap resolution.

- **Experiment tracks** (v0.0.1→v0.9.46): 7 tracks → 19 tracks; exp001–004 evolved from identity-based to capability-based discovery; exp051 `discover_capabilities_for()`.
- **NUCLEUS parity** (v0.9.11→v0.9.13): exp094 canonical NUCLEUS parity — 17/17 PASS after LD-04/05/08/09 upstream resolution; cross-atomic hash→store→retrieve pipeline operational.
- **Foundation sediment** (Phase 59): exp107 8-phase validation through structural → discovery → health → provenance → storage → compute → ledger → attribution.
- **Gap resolution sprints** (Phase 56): GAP-22 through GAP-27 resolved in reharvest pass — response parsing, base64 encoding, API drift, family_id requirements.
- **Tower/HPC scenarios** (Wave 150w→150x): Tower Atomic EXCEEDS WireGuard on measured paths; 14 stress/pen scenarios + 30 known debt items triaged; LAN gap scenario added.

---

## NUCLEUS Composition & Lifecycle — 13-primal orchestration

12-primal desktop → 13-primal NUCLEUS with skunkBat meta-tier, guidestone hardening, and plasmidBin CI hub.

- **13th primal** (Phase 58): skunkBat wired as meta-tier defense/recon; NUCLEUS count 12 → 13 across 25+ files; `resolve_btsp_socket` prefers family-scoped sockets.
- **BTSP Phase 3 convergence** (Phase 57): 13/13 NUCLEUS primals ship `btsp.negotiate` + ChaCha20-Poly1305; `CRYPTO_CONSUMPTION_HIERARCHY.md` defines per-role crypto posture.
- **Guidestone hardening** (Phase 58): `call_f64_flex`/`call_array_flex` handle barraCuda response variations; desktop cell health node added.
- **plasmidBin CI hub** (Phase 58): Sole paid Actions repo; per-primal concurrency; signing roadmap documented.
- **Gate enrollment** (Wave 147b): Automated `gate.enroll` pipeline; 6-gate mesh operational.

---

## Cross-Gate & Sovereignty — mesh validation and evolution roadmap

Single-gate validation → live multi-gate mesh scenarios, sovereignty roadmap, and silicon atheism phase 2.

- **Live mesh validation** (Wave 72→74): First 2-gate → dual membrane → cross-gate trust weaving; UDS-only stadial gate (Wave 79).
- **Neural API coordination triad** (Wave 60): quorumSignal/rootPulse/waterFall wired for cephalization scenarios.
- **Covalent mesh** (Wave 48→49): Post-primordial deployment; discovery.peers RESOLVED; plasmidBin pipeline evolution.
- **Sovereignty roadmap** (Wave 150t): Evolution path documented; standards reorg; protoKarya tangibles pivot (Wave 140a).
- **Silicon atheism** (Wave 142b): Phase 2 validation — pure Rust posture verified across ecosystem.

---

## Security & Standards — ecosystem-wide hardening waves

Scattered security gaps → coordinated PG-55 through PG-65 resolution across 13 primals.

- **Bind hardening** (Phase 59): PG-55 RESOLVED — all 13 primals default `127.0.0.1`; `--bind` flags shipped; bind flag table in `NUCLEUS_IPC_METHOD_MAP.md`.
- **MethodGate adoption** (Phase 59): PG-56 NestGate BTSP method-level auth; PG-57 skunkBat multi-dimensional baseline; PG-58/PG-59 HTTP bind docs.
- **Input fuzzing** (Phase 59): All primals survived 7 malformed JSON-RPC payloads — no crashes, no hidden admin methods.
- **Zero-port standard** (Wave 10): UDS-only transport standard; pipeline fix for dead port 21114 NAT trap awareness propagated to relay docs.
- **Contract testing** (Wave 7): Semantic gate evolution; compute trio composition (Wave 8); UniBin eukaryotic evolution (Phase 60+).

---

## Documentation & Notebooks — making validation reproducible

Scattered handoffs → structured notebooks, frozen validation data, and ecosystem evolution cycle docs.

- **Public notebooks** (Phase 59): 5 notebooks following wetSpring exemplar — composition validation, benchmark comparison, ecosystem evidence, cross-spring connections, BTSP security deep-dive.
- **Ecosystem evolution cycle** (v0.9.11): `ECOSYSTEM_EVOLUTION_CYCLE.md` — water-cycle model (mountains→springs→delta→evaporation).
- **Spring guidance** (Phase 32): `PRIMALSPRING_COMPOSITION_GUIDANCE.md`, `PRIMALSPRING_ECOSYSTEM_LEVERAGE_GUIDE.md` synchronized to NUCLEUS atomic model.
- **Pattern dissemination** (Wave 33→34): Upstream ingestion; showcase fossilization; glacial shift deployment alignment.

---

## Codebase Integrity — engineering standards (cross-cutting)

Scaffolding with warnings → reference validation spring with enforced quality gates.

- **Deep debt sweeps** (Wave 46→82): Typed errors, env centralization, idiomatic Rust; vocabulary evolution signal → composition; zero DEBT/TODO/FIXME markers.
- **Graph hygiene** (Phase 60+): 1273-line executor monolith → modular pipeline; inference module archived (534 LOC fossil).
- **Test modernization** (v0.2.0→v0.9.46): 69 → 664+ package tests; proptest IPC fuzz; 11 deploy graph structural tests.
- **Pure Rust posture** (v0.3.0): `deny.toml` ecoBin 14-crate C-dep ban; AGPL-3.0-or-later LICENSE; Edition 2024 alignment.

---

*Full date-sorted history: `CHANGELOG_ARCHIVE.md`*
*Last compressed: Wave 172*
