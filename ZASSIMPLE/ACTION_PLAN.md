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
AP-000 OpenClaw Foundation
        ↓
AP-001 Living Memory Phase 1
        ↓
Privacy/isolation validation
        ↓
Home Assistant bridge proof
        ↓
expand only from evidence
```

No parallel Artificial Soul, robot, voice-hardware, WhatsApp, VLA or custom-memory work is on the current critical path.

### AP-000 | READY — OpenClaw Foundation

**Type:** FOUNDATION / REVERSIBLE IMPLEMENTATION  
**Goal:** Learn and prove the minimum real OpenClaw runtime before adding Temaya-specific complexity.

#### Build only

1. One OpenClaw agent/workspace.
2. Minimal `SOUL.md`, `IDENTITY.md`, runtime `AGENTS.md`, and `USER.md`.
3. Basic LLM orchestration/reply loop.
4. Native session/memory behaviour only.
5. Private workspace and backup discipline.

#### Explicitly excluded

- Artificial Soul implementation;
- Emotion Engine/AICO;
- custom self-life generator;
- Home Assistant bridge;
- voice/STT/TTS hardware pipeline;
- multi-agent family routing;
- robot/embodiment;
- WhatsApp.

#### Pass

- agent starts reliably;
- persona/bootstrap files are actually loaded;
- ordinary conversation works across restart/session boundaries as OpenClaw supports;
- workspace/state locations are understood and inspectable;
- no new custom subsystem is required just to make Temaya converse;
- findings are recorded before AP-001 is refined.

#### Why first

The owner is still learning OpenClaw. This foundation converts assumptions into evidence and prevents ACTION_PLAN from branching or forcing backward redesign.



### AP-001 | READY FOR PROTOTYPE — Temaya Living Memory Phase 1

**Source:** D-021–D-026  
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
- The architecture is sufficient for AP-000 reversible OpenClaw Foundation work before full confirmation.
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

