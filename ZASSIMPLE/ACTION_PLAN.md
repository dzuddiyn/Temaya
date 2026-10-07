# TEMAYA — ZASSIMPLE ACTION PLAN

**Method:** ZASSIMPLE_MY v0.3.0  
**Status:** INTERNAL WORKING ARTIFACT  
**Authority:** Planning artifact only. It must not override `D-xxx | LOCKED` decisions in `ZASS_Temaya.md`.  
**Execution policy:** Repository root `/AGENTS.md` governs engineering execution. Any OpenClaw workspace `AGENTS.md` mentioned below is runtime/persona configuration, not the repository policy file.

## Purpose

Capture implementation thinking discovered during DECIDE and DESIGN without burdening the owner.

Planning may feed design and design may feed planning:

```text
DECISIONS
    ↓
ACTION PLAN
    ↕
DESIGN
```

Practical constraints, dependencies, sequencing, experiments, feasibility findings and later execution discoveries may refine the plan or design. They must never silently rewrite a LOCKED owner decision.

## Current plan

### Critical path — one linear path

```text
AP-000 Local Foundation
        ↓
AP-100 Minimum Useful Temaya — Stage 1
        ↓
AP-200 Artificial Soul Development — Stage 2
        ↓
Stabilization / Portability Gate
        ↓
Stage 3 Security + Hosting / Private-Cloud Hybrid
```

Within AP-100, milestones execute **sequentially**. They are acceptance milestones, not parallel architecture branches.

### Pre-execution audit gate

**Status:** OWNER AUDIT COMPLETED FOR PLANNING — PRE-ARCHITECTURE READY.

`ZASSIMPLE/PRE_EXECUTION_AUDIT.md` now contains the owner's responses. Later-stage items remain intentionally deferred until their due gate.

Remaining execution-time check:
- exact CPU model / virtualization capability / storage health / NIC / usable RAM must be inspected before installing the accepted hypervisor topology.

Audit output:
`AUDIT → pre-architecture refinement → ACTION_PLAN sequencing → task slicing → execution evidence`.

### AP-000 | READY — Local OpenClaw + HA Foundation

**Source:** D-033, D-035, D-038 + owner pre-execution audit  
**Type:** FOUNDATION / REVERSIBLE IMPLEMENTATION  
**Goal:** learn and prove the minimum real runtimes on the mini PC before Stage-1 integrations.

#### Accepted provisional topology

```text
Mini PC
└── Hypervisor
    ├── HAOS VM
    └── Linux VM
        └── OpenClaw
```

The topology is **provisional until T-F001 hardware inspection passes**. Do not force it if the real machine cannot safely support it.

#### AP-000 sequence

1. **T-F001 — Hardware / firmware inspection**
   - exact CPU model;
   - x86-64 / virtualization support;
   - RAM availability;
   - storage type/health/free capacity;
   - NIC;
   - UEFI/BIOS state.

2. **T-F002 — Preserve / prepare host**
   - protect any existing data;
   - establish rollback/backup point;
   - decide hypervisor install path only after T-F001 PASS.

3. **T-F003 — Hypervisor foundation**
   - install/configure selected hypervisor;
   - LAN/private only;
   - no public exposure.

4. **T-F004 — Home Assistant**
   - create HAOS VM;
   - assign conservative resources;
   - start HA successfully;
   - record VM/config/storage location.

5. **T-F005 — Linux/OpenClaw VM**
   - create minimal Linux VM;
   - install supported Node/OpenClaw runtime;
   - create one minimal OpenClaw agent/workspace.

6. **T-F006 — ChatGPT/OpenAI foundation auth**
   - use the owner-selected ChatGPT/OpenAI route for AP-000;
   - verify the actual OAuth/model availability and allowance from the connected account;
   - do not assume unlimited free usage;
   - keep architecture provider-agnostic.

7. **T-F007 — Day-0 security**
   - apply D-035;
   - inspect Arcadyan AW1000/OpenWrt relevant firewall/WAN/admin/UPnP/port-forward posture;
   - keep OpenClaw/HA private/LAN-only unless a reviewed secure access path is explicitly enabled;
   - secrets outside Git/searchable memory.

8. **T-F008 — Restart / recovery proof**
   - reboot/restart;
   - prove HA returns;
   - prove OpenClaw returns;
   - prove one basic Temaya/OpenClaw conversation;
   - record state/config locations and recovery steps.

9. **GATE-C001 — CONFIRM DESIGN**
   - mandatory after AP-000 PASS;
   - use actual AP-000 evidence to review core design;
   - no broader Stage-1 exposure/writes/control until explicit confirmation.

#### Explicitly excluded from AP-000

- Artificial Soul implementation;
- Emotion Engine/AICO;
- custom self-life generator;
- OpenClaw ↔ HA control bridge;
- WhatsApp/Telegram production ingestion;
- Google writes;
- Dzuddiyn Library migration/integration;
- voice/STT/TTS/smart-speaker pipeline;
- multi-agent family rollout;
- robot/embodiment.

#### AP-000 PASS

- T-F001–T-F008 pass with evidence;
- accepted deployment topology is either validated or reconciled to a simpler evidence-supported alternative;
- OpenClaw and HA start/recover reliably enough for design confirmation;
- D-035 security baseline is verified;
- one basic Temaya/OpenClaw conversation works;
- no unnecessary custom subsystem is required.

#### Exit

AP-000 exits only into **GATE-C001 — CONFIRM DESIGN**.

---

### AP-100 | LOCKED-SCOPE PLAN — Minimum Useful Temaya Phase 1

**Source:** D-032  
**Goal:** Deliver the smallest Temaya that is genuinely useful to the family, while preserving one linear execution path.

#### Milestone order

```text
M1  Basic Temaya companion
 ↓
M2  Per-user privacy/isolation baseline
 ↓
M3  Telegram + group reader
 ↓
M4  WhatsApp + group reader
 ↓
M5  Google Tasks + Calendar + Drive
    + Apps Script helper only where useful
 ↓
M6  Dzuddiyn Library practical access
    + simple PC/phone surface such as Obsidian where appropriate
 ↓
M7  Home Assistant basic bridge
    following AIoT Core / premises authority
 ↓
M8  Smart speaker
    convenient family/Hani voice interface
 ↓
M9  D-026 Living Memory proof
    self-life vs human-memory separation
 ↓
M10 End-to-end Phase 1 verification
```

#### M1 — Basic Temaya companion

- evolve AP-000 agent into a usable Temaya/Puspa baseline;
- keep OpenClaw-native orchestration;
- no advanced Artificial Soul requirement;
- before Companion A/B are instantiated or routed, complete **GATE-N001 — final names for Companion A and Companion B**. Puspa work does not need to wait for those names.

**Pass:** ordinary companion interaction is reliable enough to continue integration work.

#### M2 — Privacy / isolation baseline

- establish the D-027 per-user isolation mechanism before broad multi-user exposure;
- keep cross-user access deny-by-default;
- document actual OpenClaw isolation behaviour discovered in the runtime.

**Pass:** owner/Hani private contexts can be separated at the chosen baseline boundary.

#### M3 — Telegram integration + group reader

- connect Temaya to Telegram;
- enforce D-036: permitted group content is untrusted feed data; summarization/classification may occur, but durable promotion or consequential actions require explicit user approval of interpretation/relevance and next action;
- default approved destinations should follow the owner UX: TASK / LIBRARY / ARCHIVE / NOTHING; avoid asking Calendar-vs-Task as a normal choice.
- support relevant group/channel reading within platform permissions and explicit privacy rules;
- begin with read/summarize/useful extraction before adding unnecessary write automation.

**Pass:** Temaya can ingest and use selected Telegram group information reliably.

#### M4 — WhatsApp integration + group reader

- connect Temaya to WhatsApp using the simplest maintainable supported route;
- **I-065 field evidence:** when Hani already has the phone in hand, treat her private WhatsApp → Puspa path as the primary low-friction daily target, not merely WhatsApp group ingestion;
- prove that Hani can send a simple natural household message (for example, "telur habis") through her normal WhatsApp habit without first switching assistant modes/apps or using a special voice invocation;
- capture the intent/message first; any downstream task/list/library/calendar write remains governed by the relevant later milestone, authority and approval rules;
- enforce D-036 human approval before any group-derived information becomes memory/library/archive/calendar/task/reminder or triggers another durable/consequential action;
- support relevant group reading where the actual platform/integration permits it;
- preserve privacy and source provenance.

**Pass:** Hani can use her normal private WhatsApp path to reach Puspa/Temaya with low friction, and Temaya can also ingest/use the required WhatsApp group-information path at a basic useful level.

#### M5 — Google services

Required user-facing model:
- **Google Tasks = primary capture doorway** for ACTION / TO-DO / EVENT-like items;
- **Google Drive = document/file integration**;
- **Dzuddiyn Library = reference/durable knowledge authority**.

Google Calendar:
- do not make the owner choose Calendar vs Task during normal capture;
- dated Tasks may appear in Calendar naturally;
- the Google Tasks public API currently cannot persist due time-of-day, so M5 must test the actual OpenClaw/Google integration path;
- if exact time-of-day cannot be represented through Tasks, use the smallest compatibility mechanism necessary while preserving Tasks-first UX and avoiding duplicate canonical intent.

Apps Script:
- allowed as a deterministic helper where Google-specific work is easier/cleaner with it;
- not mandatory middleware;
- do not recreate the old serverless-sprawl architecture.

Write rules:
- direct authenticated user request may write once permission/identity is clear;
- external-feed-derived data obeys D-036 approval first;
- important writes require read-back verification.

**Pass:** the owner can capture normal to-do/event intent through one Tasks-first interaction model; date-only and exact-time cases behave predictably; Drive workflows work; important writes verify correctly.

#### M6 — Dzuddiyn Library practical access

- Temaya can access/retrieve from the authoritative Dzuddiyn Library path selected for Phase 1;
- owner has a practical direct PC/phone access surface;
- Obsidian or another simple client may be integrated if it improves usability without becoming a new authority layer;
- do not reorganize the entire legacy library merely to begin;
- before choosing local canonical storage, verify storage health/reliability; the owner's old HDD must not become the sole durable copy;
- evaluate SSD/storage/RAM upgrade and a second backup copy (local or cloud) at this milestone, without changing D-037 authority semantics.

**Pass:** owner and Temaya can both reach the library through practical, understandable paths.

#### M7 — Home Assistant basic bridge

- integrate OpenClaw/Temaya with HA at a basic level;
- follow D-007/D-008/D-010/D-028;
- HA remains premises/device/automation authority;
- AIoT Core remains independently operable.

**Pass:** Temaya can read a small verified HA state set and perform one controlled basic action without making HA dependent on OpenClaw.

#### M8 — Smart speaker

- provide a convenient voice interface for Hani/family;
- follow existing ESPHome / voice-gateway / OpenClaw architecture direction;
- implement D-055 using **Seeed Studio reSpeaker Lite Voice Assistant Kit (reSpeaker Lite 2-Mic Array + XIAO ESP32S3)** as the endpoint baseline;
- reuse the already-owned **reSpeaker Pi HAT + Raspberry Pi Zero + USB Wi-Fi** as an early audio/wake/transport prototype/test asset where useful before additional prototype purchases;
- keep the endpoint thin: local wake word + audio I/O/transport; heavy STT, Speaker ID, identity routing, OpenClaw reasoning and memory remain off-device;
- preserve the independent Home Assistant native voice fallback;
- **I-065 field evidence:** kitchen/cooking/hands-busy use is a primary Hani smart-speaker scenario; reliable wake-word invocation must be treated as a core usability/acceptance concern;
- resolve H1/H2/H3 at the M8 gate: Speaker-ID engine, audio transport, and return-audio codec/path;
- exact seller/price/unit count remains evidence/need-driven under D-054;
- no robot/embodiment requirement;
- wearable smart-speaker/earpiece chain (I-061) stays optional/future and must not delay the fixed smart-speaker PASS.

**Pass:** a family member can invoke Temaya from the reSpeaker-based smart-speaker path and receive the reply on the source device; the HA native fallback remains independently usable.

#### M9 — D-026 Living Memory milestone

D-026 remains the locked memory/privacy acceptance milestone inside the broader Phase 1 scope.

Use AP-001 below as the detailed sub-plan unless/until its implementation details are explicitly revised.

#### M10 — End-to-end Phase 1 verification

Phase 1 is DELIVERED only when:
- AP-000 foundation remains stable;
- required messaging paths work;
- Google integrations work;
- Dzuddiyn Library path is practical;
- HA basic bridge works without breaking HA independence;
- smart speaker works;
- D-026 memory/privacy proof passes;
- important writes/actions are independently verified;
- evidence and current architecture findings are recorded.

#### Not on the Phase 1 critical path

- advanced Artificial Soul;
- Emotion Engine/AICO;
- robots/stereo vision/VLA;
- cloud migration;
- custom UI/dashboard unless a real usability gap appears;
- optional integrations not required by D-032.

---

### AP-001 | DEFERRED WITHIN AP-100 M9 — Living Memory Proof

**Source:** D-021–D-026, D-032  
**Role:** Detailed sub-plan for AP-100 Milestone M9. D-026 remains authoritative for this milestone but no longer defines the whole Phase 1 deliverable.  
**Goal:** Prove consistent self-life + separate Hani memory using native OpenClaw facilities first.

#### Build only

```text
self-life/
├── STATE.md
├── CANON.md
└── events/
```

Plus one small state-aware event generator and one native Scheduled Task.

#### Sequence

1. Prepare minimal Puspa `SOUL.md`, `IDENTITY.md` and memory rules in the **OpenClaw workspace `AGENTS.md`** (runtime config; not repository root `/AGENTS.md`).
2. Create `self-life/STATE.md`, `CANON.md`, and `events/`.
3. Configure native memory indexing/search for self-life if supported.
4. Create one daily native Scheduled Task that generates **one** believable Puspa event after reading STATE + CANON + recent events.
5. Record event with provenance and `reality_class: persona_narrative`.
6. Test same-day self-life recall.
7. Record one Hani personal episodic memory in Hani's private memory domain.
8. Test later Hani-memory recall.
9. Verify neither domain contaminated the other.
10. Record findings about Dreaming, retrieval scoping and isolation; do not add custom subsystems unless a concrete gap is demonstrated.

#### Acceptance test

- morning: one Puspa self-life event exists;
- afternoon: Hani asks what Puspa did/ate;
- Puspa recalls the **same** stored event;
- Hani shares one personal story;
- later Puspa recalls Hani's story;
- Hani story is absent from self-life;
- Puspa self-life is absent from Hani fact memory;
- no custom DB;
- no second scheduler;
- no custom reflection engine;
- no web UI.

#### Stop / failure conditions

Stop and document a gap if:
- native retrieval cannot separate domains reliably;
- native provenance is insufficient for generated persona narrative;
- D-027 per-user isolation cannot be enforced at the required boundary;
- D-028 authority boundaries would require duplicated/conflicting canonical state;
- D-029 single-writer self-life ownership cannot be maintained;
- Dreaming mixes self-life with human durable memory.

Do **not** expand scope before the gap is documented.

## Planning findings
- Home Assistant <> Temaya context sync confirms direct HA MCP before n8n for HA integration evidence; n8n remains cross-system workflow/gatekeeper candidate, not default HA middleware.
- HA Device/Area Registry authority + OpenClaw localization cache/fallback must be proven together during T-C001.
- Local AI/Ollama-like runtime is optional and benchmark-gated; MQTT/Node-RED/Open WebUI remain need-driven.

- Living Design v0.1 supports native OpenClaw memory/indexing/scheduler first.
- Custom scope is limited to the self-life namespace + state-aware event generator.
- D-027 resolves the minimum per-user isolation baseline: private agent/workspace or equivalent boundary, deny-by-default cross-agent access.
- D-028 resolves authority split: Dzuddiyn Library/document stores = knowledge, OpenClaw = persona/conversational memory, Home Assistant = operational household state.
- D-029 resolves self-life ownership: one authoritative writer per persona.
- Dreaming behaviour, retrieval scoping, exact Gateway/host isolation and minimum provenance metadata remain **NEED TEST** during implementation.
- D-030 keeps Artificial Soul as an official design domain; D-034 schedules AP-DESIGN-001/AP-200 in Stage 2, after Minimum Useful Temaya.
- D-031 fixes the deployment progression: local mini-PC baseline → stabilized portable runtime → future private-cloud OpenClaw with local HA hybrid.
- D-032 defines the Phase 1 Minimum Useful Temaya deliverable and removes ambiguity that D-026 was the whole Phase 1.
- D-033 keeps AP-000 intentionally small: install/run OpenClaw + HA and learn the real runtimes.
- The architecture is sufficient for AP-000 reversible foundation work and the linear AP-100 Phase 1 integration path before full confirmation.
- Design remains **PENDING CONFIRMATION**; final confirmation is no longer blocked by completing Artificial Soul detail first.
- Repository execution policy is now explicit in root `/AGENTS.md`; this is an execution-governance clarification, not a new Temaya architecture decision.



None promoted yet.


## Locked persona/voice implementation constraints

- D-012: Companion A proactive technical inspiration uses randomized ~1–2 week timing; exact scheduler implementation remains open.
- D-015: Puspa + Companion B require daily persona-life generation constrained by profile/rules/canon; exact schema remains open.
- D-017: Companion A/B TTS baseline is `ms-MY-OsmanNeural` with their locked prosody/post-processing ranges.
- D-018: Umar requires an English boy-robot voice; exact English TTS voice and processing remain open.

These are planning constraints only; design remains unconfirmed.


### AP-200 | PLANNED — Artificial Soul Development

**Source:** D-030, D-034  
**Stage:** 2 — begins only after AP-100 Minimum Useful Temaya is delivered.

Goal:
- develop Artificial Soul for Puspa and Companion B on top of the working OpenClaw-based Temaya;
- improve trusted companionship, continuity, positivity and safe/private emotional expression without making Stage 1 depend on advanced soul machinery.

Scope to review when Stage 2 starts:
1. Identity / Character.
2. Self-Life Continuity.
3. Emotional Continuity.
4. Appraisal / Internal State Interpretation.
5. Agency / Initiative.
6. Soul Safety & Boundaries.

Implementation principle:
- OpenClaw-first;
- reuse the already-working Stage 1 runtime;
- optional Emotion Engine/AICO-inspired components only if evidence shows value;
- review implementation-heavy D-015/D-023/D-024/D-026/D-029 details before adding custom machinery;
- no hosting/cloud migration inside AP-200.

Exit:
- Artificial Soul behaviour is useful, bounded, private, testable and regression-safe;
- no contamination of human/private memory;
- Stage 1 functions remain intact.

### Stabilization / Portability Gate

Runs after AP-200 and before Stage 3.

Required:
- backup/recovery;
- configuration and secret separation;
- regression testing across Stage 1 + Stage 2;
- operational hardening;
- runtime portability and migration readiness.

### Stage 3 — Security + Hosting / Hybrid Cloud

Only after stabilization.

Scope:
- deeper security hardening;
- secure remote/private access;
- hosting/server architecture;
- private-cloud OpenClaw/Temaya when feasible;
- secure bridge back to local Home Assistant;
- preserve HA premises authority and independent operation.

---

## Research candidates — not execution tasks

These items are preserved for later evaluation and **do not enter the current execution queue**.

### RC-001 — Artificial Soul emotional continuity POC

**Source:** AC-013  
**Status:** PARKED UNTIL CORE MEMORY/PRIVACY VERTICAL SLICE IS STABLE

Candidate:
- OpenClaw remains runtime/persona/factual-memory authority;
- optional third-party Emotion Engine may provide compact emotional continuity;
- evaluate only through a reversible POC;
- no AICO/Mem0/custom memory replacement.

Pass concept:
- continuity persists across sessions;
- persona remains within LOCKED profile;
- factual/user memory remains separate;
- no cross-user leakage;
- decay returns state toward persona baseline.

### RC-002 — Embodiment / Robot Vision benchmark

**Source:** AC-014  
**Status:** FUTURE R&D — NOT A CURRENT DESIGN BLOCKER

When physical embodiment becomes active scope, compare integrated stereo/RGB-D candidates before selecting hardware.

Research reference:
`ZASSIMPLE/RESEARCH/ARTIFICIAL_SOUL_AND_EMBODIMENT.md`.


### Home Assistant <> Temaya alignment

**Source:** `ZASSIMPLE/CONTEXT_SYNC_HOME_ASSISTANT_TEMAYA.md`  
**Status:** REPLANNED — NO LOCKED AUTHORITY CHANGE

Planning rule:
- prove the shortest direct authority path before introducing optional orchestration;
- OpenClaw → official HA MCP is tested before n8n is considered for HA-related work;
- HA Device/Area Registry + OpenClaw cache/fallback is included in the direct integration proof;
- local AI is benchmarked only for bounded utility roles and only if host resources allow;
- n8n is tested as a workflow/Human-Queue/idempotency layer on a synthetic cross-system workflow, not as mandatory HA middleware;
- MQTT/Node-RED/Open WebUI remain need-driven and may legitimately result in `NO NEED`.

Preferred T-C001 evidence order:

```text
P-C001 OpenClaw native/plugin audit
      ↓
P-C003 Official HA MCP + D-008 registry/cache proof
      ↓
P-C007 Local AI bounded benchmark (if hardware allows)
      ↓
P-C002 n8n workflow/gatekeeper POC
      ↓
P-C004/P-C005/P-C006 DL/document/access/retrieval POCs
      ↓
P-C009 Auxiliary-service need review
      ↓
P-C010 Hardware scaling review
      ↓
P-C008 Stage-1 ordering ZASSELECTION
      ↓
reconcile DESIGN ↔ ACTION_PLAN
      ↓
GATE-C001
```

**Important:** this is the T-C001 evidence order, not a silent rewrite of AP-100 M1→M10. I-064/P-C008 remains the explicit decision point for any Stage-1 sequence change.

### RC-003 — LifeOS reuse-first / plugin-first architecture challenge

**Source:** I-063  
**Status:** LOCKED-SCOPE PRE-GATE-C001 REVIEW — mandated by D-039

Goal:
- avoid rebuilding mature capabilities from zero;
- inventory reusable OpenClaw skills/plugins, n8n nodes/templates, HA integrations and mature open-source components;
- compare reuse/integration/adaptation against custom implementation before design confirmation;
- specifically challenge librarian/ingestion, messaging, Google, DL access, HA bridge, document processing and local-AI plumbing.

Mandatory reuse candidates to evaluate before equivalent custom implementation:
- OpenClaw ClawHub and official plugin inventory;
- OpenClaw Skills / Skill Workshop;
- n8n as ingestion/workflow/approval/dedup/verified-write layer;
- official Home Assistant MCP Server;
- Paperless-ngx for OCR/document-management POC where useful;
- Obsidian + constrained local API as a human DL surface;
- Apps Script only as a compatibility helper after a demonstrated gap.

Mandatory challenge methods:
1. first-principles authority review;
2. reuse / integrate / adapt / build matrix;
3. event-storming lifecycle walkthrough;
4. pre-mortem + FMEA;
5. threat/privacy challenge;
6. graceful-degradation test;
7. migration/exit test;
8. reference-project cross-check;
9. ZASSELECTION for remaining viable alternatives.

Timing:
- **mandatory after AP-000 evidence is complete and before owner completion of `GATE-C001 — CONFIRM DESIGN`**;
- D-039 adds this review as a prerequisite to confirmation while preserving D-038 as the owner confirmation gate.

Research reference:
`ZASSIMPLE/RESEARCH/LIFEOS_REUSE_AND_ARCHITECTURE_CHALLENGE.md`.

### RC-012 — Official HA MCP + Registry/Cache Proof

**Source:** D-007, D-008, D-010, D-028, I-064  
**Status:** BLOCKED UNTIL AP-000 PASS / T-C001

POC scope:
- connect OpenClaw test context to the official Home Assistant MCP Server;
- expose only a small approved entity set;
- prove a read-only household-state query;
- verify HA remains authority for state/device/area registry;
- resolve `device_id → area_id → area_name`;
- create/read a small local OpenClaw cache/fallback of the authoritative mapping;
- prove the cache can be treated as stale/fallback rather than authority;
- optional reversible/test-only action only if the current gate permits it.

Pass:
- direct OpenClaw↔HA path works without n8n;
- authority remains unambiguous;
- registry/cache fallback contract is observable;
- failure of OpenClaw does not remove HA native operation.

### RC-004 — n8n Librarian / Workflow Gatekeeper POC

**Source:** D-039, D-043–D-045 + Home Assistant <> Temaya context sync  
**Status:** BLOCKED UNTIL DIRECT HA-MCP PROOF / T-C001

**Boundary:** n8n is not the default inline OpenClaw→HA control path. Run this POC only after the direct official HA MCP path is understood, and use n8n to prove cross-system workflow value rather than duplicate HA/OpenClaw authority.

POC scope:
- ingest one synthetic/reversible message/event;
- normalize + classify to TASK / LIBRARY / ARCHIVE / NOTHING;
- deduplicate by stable source/event id;
- create a Human Queue / approval state when required;
- perform one reversible verified write to a non-production target or test record;
- prove retry/restart does not duplicate the action.

Pass: n8n demonstrates useful deterministic workflow value without becoming memory/persona/privacy authority.

### RC-005 — Paperless-ngx Document Ingestion POC

**Source:** D-039, D-041, D-043  
**Status:** BLOCKED UNTIL T-C001 / AP-000 PASS

POC scope:
- ingest a non-sensitive sample scan/PDF;
- OCR/extract metadata;
- preserve source/provenance;
- export/retrieve through API;
- show that Paperless can feed/reference DL without becoming DL authority.

Pass: measurable reduction in custom OCR/document-filing work with a clean exit/export path.

### RC-006 — Obsidian + Constrained API Human DL Surface POC

**Source:** D-037, D-039, D-041, D-050  
**Status:** BLOCKED UNTIL T-C001 / AP-000 PASS

POC scope:
- human-readable sample library content;
- PC/phone browse/edit path where practical;
- constrained local/API read-write test;
- provenance/canonical-source mapping;
- prove the client/API remains a surface rather than a competing authority.

Pass: practical human access improves without introducing a second canonical store.

### RC-007 — Rebuildable Hybrid Retrieval POC

**Source:** D-037, D-041  
**Status:** BLOCKED UNTIL SUITABLE SAMPLE CORPUS EXISTS

POC scope:
- compare keyword/BM25-style retrieval with vector/semantic retrieval and a hybrid path;
- measure retrieval usefulness on representative DL samples;
- delete/rebuild the derived index from canonical source;
- preserve provenance to source records.

Pass: retrieval improvement is demonstrated and index loss remains recoverable.

### RC-008 — Canonical Representation Portability POC

**Source:** D-041  
**Status:** BLOCKED UNTIL T-C001 / M6 SAMPLE DATA

POC scope:
- compare a small human-readable/exportable representation such as Markdown + structured JSON metadata (Git only where suitable);
- verify human inspection, backup/export, migration and machine parsing;
- do not lock one format until evidence exists.

Pass: at least one representation preserves semantics across tool/runtime replacement without depending on a proprietary internal store.

### RC-009 — Local AI Utility Benchmark POC

**Source:** D-048, D-051, D-052  
**Status:** BLOCKED UNTIL AP-000 PASS / T-C001 AND HARDWARE ALLOWS

POC scope:
- benchmark representative bounded tasks such as classification, structured extraction and private/local summarization using non-sensitive samples;
- compare at least latency, memory pressure, output quality/reliability and operational overhead;
- test one replaceable local runtime/model mapping without making it architectural authority;
- compare against a cloud/provider baseline where useful.

Pass: local inference demonstrates a concrete useful role on the actual host without violating D-051/D-052.

### RC-010 — Need-Driven Auxiliary Service Review

**Source:** D-053  
**Status:** T-C001 REVIEW / ACTIVATE ONLY ON REAL REQUIREMENT

Review MQTT/broker, Node-RED, Open WebUI and similar auxiliary services against actual requirements.

Pass rule:
- `NO NEED` is a valid PASS;
- adopt only when a concrete capability cannot be served more simply by existing HA/OpenClaw/n8n/native mechanisms;
- record owner/use case, failure/recovery path and removal/exit path.

### RC-011 — Evidence-Driven Hardware Scaling Review

**Source:** D-054 / T-F001 evidence  
**Status:** T-C001 REVIEW AFTER ACTUAL HOST METRICS

Use actual host facts/metrics to decide whether AP-100 needs no upgrade, a targeted RAM/storage upgrade, accelerator/compute extension, or host replacement. Do not lock generic 8/16/32-GB tiers as architecture requirements.

Pass: any proposed purchase/upgrade is tied to a measured constraint and the smallest adequate remedy.


## Pre-confirmation design work

### AP-DESIGN-001 | ARTIFICIAL SOUL DOMAIN REVIEW

**Source:** D-030, D-034  
**Status:** DEFERRED TO AP-200 / STAGE 2 — NOT ON STAGE 0/1 CRITICAL PATH

Goal when resumed:
- define Artificial Soul as a coherent OpenClaw-first capability domain for Puspa and Companion B;
- preserve locked persona/privacy/authority intent while reopening only implementation details where evidence supports a better architecture.

Deferral rule:
- OpenClaw alone is sufficient for current foundation and basic companion operation;
- do not let Artificial Soul implementation block core learning, privacy proof, memory proof or HA integration;
- resume only when the core companion works and there is a demonstrated need for richer emotional/self-life continuity.

Review dimensions:
1. Identity / Character authority.
2. Self-Life Continuity.
3. Emotional Continuity.
4. Appraisal / Internal State Interpretation.
5. Agency / Initiative.
6. Soul Safety & Boundaries.

Decisions explicitly flagged for review of implementation detail:
- D-015 — persistent self-life intent vs mandatory daily/custom engine mechanism;
- D-023 — self-life separation/inspectability vs exact filesystem schema;
- D-024 — history-aware continuity vs exact custom Life Event Generator implementation;
- D-026 — Phase 1 outcome/acceptance vs implementation prescription;
- D-029 — single authoritative self-life write authority vs exact writer implementation;
- D-020 — keep worldview/behaviour, review exact random-trigger mechanism only if needed.

Do not modify any LOCKED decision during this review without an explicit owner decision gate.

