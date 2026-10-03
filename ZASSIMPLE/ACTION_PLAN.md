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
AP-100 Minimum Useful Temaya — Phase 1
        ↓
Stage 2 Stabilize + Portable
        ↓
Stage 3 Private Cloud OpenClaw + Local HA Hybrid
```

Within AP-100, milestones execute **sequentially**. They are acceptance milestones, not parallel architecture branches.

### AP-000 | READY — Local OpenClaw + HA Foundation

**Source:** D-033  
**Type:** FOUNDATION / REVERSIBLE IMPLEMENTATION  
**Goal:** Learn and prove the minimum real runtimes on the mini PC before integration work.

#### Build only

1. Prepare the mini PC host safely.
2. Install and run OpenClaw.
3. Create one minimal OpenClaw agent/workspace.
4. Minimal `SOUL.md`, `IDENTITY.md`, runtime `AGENTS.md`, and `USER.md`.
5. Prove a basic LLM orchestration/reply loop.
6. Understand native session/memory state locations at a basic operational level.
7. Install and start Home Assistant.
8. Verify both OpenClaw and HA can restart/recover to a known running state.

#### Explicitly excluded from AP-000

- Artificial Soul implementation;
- Emotion Engine/AICO;
- custom self-life generator;
- OpenClaw ↔ HA bridge;
- WhatsApp/Telegram;
- Google services;
- Dzuddiyn Library integration;
- voice/STT/TTS/smart-speaker pipeline;
- multi-agent family routing;
- robot/embodiment.

#### PASS

- OpenClaw starts reliably on the mini PC;
- one basic Temaya/OpenClaw conversation works;
- persona/bootstrap files are actually loaded;
- OpenClaw workspace/runtime locations are understood and inspectable;
- Home Assistant starts reliably on the same premises platform according to the chosen deployment layout;
- basic restart/recovery for both is demonstrated;
- no unnecessary custom subsystem is required just to make the foundation run.

#### Exit

AP-000 ends when OpenClaw and Home Assistant are both running reliably enough to begin AP-100 integration milestones.

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
- no advanced Artificial Soul requirement.

**Pass:** ordinary companion interaction is reliable enough to continue integration work.

#### M2 — Privacy / isolation baseline

- establish the D-027 per-user isolation mechanism before broad multi-user exposure;
- keep cross-user access deny-by-default;
- document actual OpenClaw isolation behaviour discovered in the runtime.

**Pass:** owner/Hani private contexts can be separated at the chosen baseline boundary.

#### M3 — Telegram integration + group reader

- connect Temaya to Telegram;
- support relevant group/channel reading within platform permissions and explicit privacy rules;
- begin with read/summarize/useful extraction before adding unnecessary write automation.

**Pass:** Temaya can ingest and use selected Telegram group information reliably.

#### M4 — WhatsApp integration + group reader

- connect Temaya to WhatsApp using the simplest maintainable supported route;
- support relevant group reading where the actual platform/integration permits it;
- preserve privacy and source provenance.

**Pass:** Temaya can ingest/use the required WhatsApp information path at a basic useful level.

#### M5 — Google services

Required:
- Google Tasks;
- Google Calendar;
- Google Drive.

Apps Script:
- allowed as a deterministic helper where Google-specific work is easier/cleaner with it;
- not mandatory middleware;
- do not recreate the old serverless-sprawl architecture.

**Pass:** Temaya can perform the agreed useful read/write workflows for Tasks/Calendar/Drive, with verification of important writes.

#### M6 — Dzuddiyn Library practical access

- Temaya can access/retrieve from the authoritative Dzuddiyn Library path selected for Phase 1;
- owner has a practical direct PC/phone access surface;
- Obsidian or another simple client may be integrated if it improves usability without becoming a new authority layer;
- do not reorganize the entire legacy library merely to begin.

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
- choose the simplest reliable Phase 1 hardware implementation;
- no robot/embodiment requirement.

**Pass:** a family member can invoke Temaya from the smart-speaker path and receive the reply on the source device.

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

- Living Design v0.1 supports native OpenClaw memory/indexing/scheduler first.
- Custom scope is limited to the self-life namespace + state-aware event generator.
- D-027 resolves the minimum per-user isolation baseline: private agent/workspace or equivalent boundary, deny-by-default cross-agent access.
- D-028 resolves authority split: Dzuddiyn Library/document stores = knowledge, OpenClaw = persona/conversational memory, Home Assistant = operational household state.
- D-029 resolves self-life ownership: one authoritative writer per persona.
- Dreaming behaviour, retrieval scoping, exact Gateway/host isolation and minimum provenance metadata remain **NEED TEST** during implementation.
- D-030 keeps Artificial Soul as an official design domain, but AP-DESIGN-001 is deferred and removed from the current critical path.
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



## Pre-confirmation design work

### AP-DESIGN-001 | ARTIFICIAL SOUL DOMAIN REVIEW

**Source:** D-030  
**Status:** DEFERRED — NOT ON CURRENT CRITICAL PATH

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

