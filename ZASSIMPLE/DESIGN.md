# TEMAYA — ZASSIMPLE DESIGN

**Method:** ZASSIMPLE_MY v0.3.0  
**Design:** Temaya Living Design v0.1  
**Status:** DRAFT — PENDING CONFIRMATION
**Design Progress:** 4/4 — purpose / main flow / main elements / relevant LOCKED decisions  
**Authority:** Derived from LOCKED decisions in `ZASS_Temaya.md`.  
**Execution policy:** Repository root `/AGENTS.md` governs engineering execution and does not override LOCKED decisions.

> This is a working design draft. Temaya is a technical/system project, so architecture is retained as a subtype of DESIGN. It is not confirmed until the owner completes the ZASSIMPLE confirmation gate with `YA, CONFIRM DESIGN`.

## Purpose

Temaya must feel like a persona with a coherent life of its own while keeping private, per-human memory structurally separate.

```text
SELF-LIFE — "Ini cerita aku"
≠
HUMAN MEMORY — "Ini yang user pernah cerita dekat aku"
```

## AGENTS.md naming boundary

Two different artifacts may share the filename `AGENTS.md`:

- Repository root `/AGENTS.md` — engineering/agent execution policy for building and verifying Temaya.
- OpenClaw workspace `AGENTS.md` — runtime/persona operating and memory rules used by OpenClaw.

They are separate authorities and must not overwrite or be silently copied into each other.

## Core principle

**OpenClaw-native first.**

Use native OpenClaw capabilities before custom Temaya machinery:
- `SOUL.md`, `IDENTITY.md`, OpenClaw workspace `AGENTS.md`, `USER.md`;
- `MEMORY.md` and `memory/YYYY-MM-DD.md`;
- memory-core / SQLite index, recall and provenance;
- Scheduled Tasks / Cron;
- Standing Intents;
- Heartbeat;
- Dreaming / consolidation.

Custom layers are allowed only for proven gaps.

## Main flow

The primary interaction flow is:
identity/persona selection → relevant Artificial Soul + current-user context → scoped recall/write → reasoning/action → consistent reply.

Artificial Soul has its own internal continuity flow:
identity/character → self-life continuity → emotional/appraisal state → bounded initiative → response/experience → validated continuity update.

## Main elements

Core elements are:
- OpenClaw Core / orchestration runtime;
- Identity & Persona;
- Artificial Soul;
- Human Memory & Privacy;
- Dzuddiyn Library / Knowledge;
- Voice & Interaction;
- AIoT Core / Home Assistant;
- Integration Bridge;
- Infrastructure / Runtime;
- Future Embodiment / Physical Companion interfaces.

Existing D-021–D-029 implementation constraints remain authoritative until explicitly revised.

## Security staging principle

Locked by D-035:

**Security Baseline from Day 0; Security Hardening in Stage 3.**

Stage 0/1 minimum:
- no unnecessary public exposure;
- authentication/access control where supported;
- secrets stay out of Git and ordinary searchable memory/knowledge;
- allowlists/explicit authorization for messaging where supported;
- private workspaces/isolation boundaries respected;
- recoverable configuration/state proportionate to the stage;
- external exposure requires an explicit security review.

Stage 3 performs deeper hardening, hosting exposure design, network segmentation, stronger secret management, audit/logging and mature recovery controls.

## Small-start architecture rule

Temaya begins with a reversible **AP-000 Local Foundation** before the full design is confirmed, consistent with repository `/AGENTS.md`.

AP-000 intentionally contains only:
- install/host OpenClaw on the mini PC;
- prove a basic LLM-orchestrated companion conversation;
- install/start Home Assistant;
- learn the real runtime, configuration, startup and recovery paths.

AP-000 intentionally excludes all Phase 1 integrations.

After AP-000, Phase 1 follows one linear critical path toward the locked **Minimum Useful Temaya** deliverable in D-032. Artificial Soul advanced implementation, robots and other optional R&D remain outside that critical path.

## External-feed trust boundary

Locked by D-036:

WhatsApp/Telegram/group/channel content is an **external untrusted feed**.

Temaya may read/summarize/classify permitted feeds, but any promotion into durable memory/library/archive/calendar/tasks/reminders or another consequential write/action requires user approval of:
1. relevance/interpretation; and
2. the proposed next action.

No approval = no durable promotion/action. Provenance must be retained after approval.

## Pre-architecture — audit-informed v0.1

**Status:** WORKING / NOT CONFIRMED  
**Input:** D-001–D-038 + PRE_EXECUTION_AUDIT owner response.  
**Purpose:** give AP-000/AP-100 a coherent technical shape without prematurely fixing later-stage implementation details.

### A. Stage-0 deployment

Accepted provisional topology:

```text
Mini PC — Intel Core i3 circa 2018 / 8 GB RAM / 500 GB
└── Hypervisor
    ├── HAOS VM
    │   └── Home Assistant / AIoT Core
    └── Linux VM
        └── OpenClaw / Temaya runtime
```

This topology is conditional on T-F000 hardware validation:
- exact CPU model;
- VT-x/virtualization support;
- storage health/type/free capacity;
- NIC;
- available RAM under load.

Do not force the topology if the real host cannot support it safely. The architecture intent is **failure isolation + portability**, not a specific hypervisor brand.

### B. Stage-0 AI/provider

- AP-000 preferred provider/auth route: ChatGPT/OpenAI.
- Provider is not an architecture authority and remains replaceable.
- Use one working provider only during foundation learning.
- Verify actual account OAuth/model/allowance during onboarding; do not assume unlimited free usage.

### C. Network and security

D-035 applies from first boot:
- LAN/private operation by default;
- no public port forwarding;
- auth/access controls where supported;
- secrets outside Git and searchable memory;
- basic snapshot/backup before risky changes;
- inspect Arcadyan AW1000/OpenWrt firewall/WAN/admin/UPnP/port-forward posture during AP-000.

Outbound internet access is allowed for cloud reasoning/services. Direct remote access to the local OpenClaw Gateway is a separate concern and should use a private secure transport when later required rather than exposing the Gateway publicly.

### D. Identity / privacy baseline

Before multi-user Stage-1 exposure:
- one private human domain per user;
- separate agent/workspace or equivalent boundary;
- deny cross-agent access by default;
- data classes:
  - PRIVATE-HUMAN;
  - FAMILY-SHARED;
  - EXTERNAL-FEED;
  - SYSTEM/OPERATIONAL.

Escalate to stronger Gateway/process/host isolation only if leakage/authorization testing shows the baseline is insufficient.

### E. External-feed ingestion

D-036 governs WhatsApp/Telegram/group readers:

```text
permitted external feed
      ↓
read / summarize / classify
      ↓
candidate information
      ↓
USER APPROVAL
├── relevance / interpretation
└── next action
      ↓
TASK / LIBRARY / ARCHIVE / other permitted action
```

No approval means no durable promotion/action.

Start with one-by-one channel allowlists and read/summarize-only behaviour.

### F. Google action model

Current agreed user experience (AC-017):

```text
ACTION / TO-DO / EVENT-LIKE INPUT
→ Google Tasks as preferred capture doorway

REFERENCE / DURABLE INFORMATION
→ Dzuddiyn Library
```

Do not normally ask the owner to choose Calendar vs Task.

Technical constraint to validate in M5:
- Google Tasks UI can represent date/time, but the public Tasks REST API currently persists scheduled/due **date only** and discards time-of-day.
- therefore exact timed-item automation remains a compatibility problem to solve at M5;
- use the smallest compatibility mechanism available through the actual OpenClaw/Google integration without creating duplicate canonical intent.

### G. Dzuddiyn Library

D-037 authority model:

```text
Dzuddiyn Library — AUTHORITATIVE KNOWLEDGE
├── canonical storage/source     ← exact physical topology due M6
├── human access surfaces       ← PC / phone / Obsidian where useful
└── derived AI retrieval        ← OpenClaw index/cache/search
```

Current legacy data remains distributed across Drive/HDD/PC/cloud. Do not migrate it during AP-000.

M6 must select a reliable canonical storage/backup topology. The owner's current preference is toward local storage on/attached to the mini PC to reduce subscription dependence, but an old HDD is not acceptable as the sole durable copy. SSD/storage-health/RAM upgrade and incremental cloud backup remain candidates.

### H. Home Assistant

Existing contracts remain:
- HA is operational/premises authority;
- ordinary deterministic automations stay in HA;
- OpenClaw handles higher-level intent;
- sensitive actions are gated below the LLM;
- HA Device/Area Registry is authoritative with OpenClaw local cache/fallback per D-008;
- bridge starts with a small read set + one reversible action.

### I. Interaction surfaces

Stage 1:
- Telegram;
- WhatsApp;
- smart speaker.

Open idea for later:
- wearable smart-speaker / companion chain;
- optional earpiece/earbud connection;
- exact transport/wake/privacy/routing deferred.

### J. Mandatory confirmation boundary

D-038 + D-039:

```text
T-F000 / AP-000 PASS
        ↓
D-039 ARCHITECTURE CHALLENGE
reuse inventory
→ authority review
→ real-event walkthrough
→ Reuse / Integrate / Adapt / Build
→ privacy/threat + pre-mortem/FMEA
→ degradation/recovery
→ migration/exit
→ mature-project cross-check
→ ZASSELECTION where needed
→ reconcile DESIGN ↔ ACTION_PLAN
        ↓
GATE-C001 — CONFIRM DESIGN
        ↓
Stage-1 exposure / writes / HA control
```

The Architecture Challenge is mandatory preparation for confirmation. It does not itself confirm the design and must not silently rewrite a D-xxx LOCKED decision.

### K. Reuse-first implementation discipline

Locked by D-039:
- inspect native/runtime capability first;
- then official/bundled/maintained plugins and integrations;
- then mature OSS with API + migration/exit path;
- then small adapters;
- custom subsystem only after a recorded gap.

Mandatory candidates to evaluate before equivalent custom work:
- OpenClaw ClawHub + official plugins/skills;
- OpenClaw Skills / Skill Workshop;
- n8n for deterministic ingestion/workflow/librarian orchestration;
- official Home Assistant MCP Server;
- Paperless-ngx for OCR/document ingestion;
- Obsidian + constrained local API for human DL access.

Apps Script is a last-resort Google-specific compatibility/helper mechanism, not default middleware.

No silent continuation through the confirmation boundary.

### L. Cross-cutting LifeOS-derived architecture principles

Locked by D-040–D-050:

- **Small deployment, large architecture:** deploy only the smallest reversible vertical slice needed to prove the next capability.
- **Portable canonical data:** important canonical records remain human-inspectable/exportable and independent of any one AI/runtime/vendor.
- **Stable person identity:** one human identity may bind multiple channels; display names alone are not identity authority.
- **Observation promotion:** external/digital-exhaust content follows RAW/OBSERVATION → CANDIDATE → APPROVED where required → CANONICAL.
- **Human Queue:** ambiguity/approval can suspend a job and later resume the same attributable operation.
- **Durable workflow semantics:** consequential cross-system work is restart-safe, idempotent, deduplicated and verified.
- **Deterministic privacy:** LLMs may interpret content but do not grant access or replace explicit authorization policy.
- **Source/private-data separation:** source repositories do not become stores for private family memories or secrets.
- **Model-role abstraction:** architecture binds to capability roles rather than transient model product names.
- **Graceful degradation:** HA, DL, Temaya/OpenClaw, workflow engine and providers fail independently where practical.
- **One Temaya, many surfaces:** channels and UI clients are surfaces over one coherent persona/policy/authority model, not competing Temaya instances.

These principles refine D-027/D-028/D-036/D-037/D-039 without moving their authority boundaries.

### M. Deferred domains

- Speaker-ID / audio transport / codec → M8.
- Artificial Soul implementation → Stage 2.
- Private-cloud/server/remote hosting hardening → Stage 3.
- Ryzen compute → optional extension.
- Robots / rich embodiment → later subproject.


## Architecture domains

### 1. OpenClaw Core / Orchestration Runtime
Reusable agent/orchestration runtime. It hosts persona execution, reasoning, tools and native capabilities while remaining separable from project-specific profiles.

### 2. Identity & Persona
Defines who each companion is: identity, character, communication style, values, role and persona-specific boundaries.

### 3. Artificial Soul
Official domain locked by D-030.

```text
Artificial Soul
├── Identity / Character
├── Self-Life Continuity
├── Emotional Continuity
├── Appraisal / Internal State Interpretation
├── Agency / Initiative
└── Soul Safety & Boundaries
```

Artificial Soul is a capability domain, not a single engine. OpenClaw-native-first remains authoritative. Exact implementation remains open pending domain review.

### 4. Human Memory & Privacy
Per-human private memory, provenance, retrieval scope and isolation. Human memory must remain separate from persona self-life.

### 5. Dzuddiyn Library / Knowledge
Durable knowledge/document authority, personal/family/project knowledge and approved continuity records outside transient runtime state.

Current agreed direction (AC-015):

```text
AUTHORITATIVE KNOWLEDGE
Dzuddiyn Library
        │
        ├── storage/source
        │    Google Drive / selected document store
        │
        ├── human access
        │    Obsidian / phone / PC client
        │
        └── AI retrieval
             OpenClaw index/cache/search
```

Obsidian or another client is an access surface, not a second authority. OpenClaw retrieval/index is derived, not canonical. Exact physical authoritative storage remains open until the relevant Stage-1 review.

### 6. Voice, Messaging & Interaction
User-facing interaction surfaces:
- smart speaker / voice path;
- wake word, STT, speaker identity, routing, TTS and multi-turn behaviour;
- WhatsApp;
- Telegram;
- group-reader capability where platform permission/privacy allows it.

The smart speaker is a Phase 1 vital interface for convenient family use, especially for Hani. Robots and richer physical embodiment remain future extensions.

### 7. AIoT Core / Home Assistant
Independent household automation and operational-state authority. It must continue functioning without Temaya/OpenClaw.

### 8. Integration Bridge & External Services
Controlled integrations between OpenClaw and external/operational systems while preserving authority and failure isolation.

Phase 1 vital integrations include:
- Home Assistant;
- Google Tasks;
- Google Calendar;
- Google Drive;
- Apps Script only where a deterministic Google-specific helper is useful;
- Dzuddiyn Library access surfaces, including Obsidian or another simple PC/phone access path when appropriate;
- messaging channel adapters for WhatsApp/Telegram.

Apps Script/serverless is not the Temaya runtime and is not mandatory universal middleware.

### 9. Infrastructure / Runtime
Current baseline:
- local mini PC hosts OpenClaw and Home Assistant.

Architecture must preserve deployment portability so the OpenClaw/Temaya runtime can later move to a private cloud/server without redesigning identity, memory, knowledge or integration contracts.

Future target:

```text
Private Cloud / Private Server
└── OpenClaw / Temaya
        │
        └── secure bridge
               │
               ▼
        Local Home Assistant
        devices / sensors / automations
```

Home Assistant remains local-premises operational authority unless explicitly changed later.

### 10. Future Embodiment / Physical Companion
Robots, stereo/depth vision, physical manipulation and richer embodied-AI capabilities. This is a future extension and is not required for Phase 1. The smart speaker is no longer classified here because it is a Phase 1 Voice/Interaction deliverable.

## Development mapping

The project advances as one directional progression rather than parallel architecture branches:

```text
STAGE 0 — LOCAL FOUNDATION
Mini PC
├── OpenClaw installed/running
└── Home Assistant installed/running
          ↓
STAGE 1 — MINIMUM USEFUL TEMAYA
OpenClaw companion
+ privacy/memory baseline
+ Telegram + WhatsApp group-reader integration
+ Google Tasks/Calendar/Drive
+ Apps Script helper where useful
+ Dzuddiyn Library practical access
+ Obsidian/other simple PC-phone library surface
+ HA basic integration
+ smart speaker
+ D-026 memory/privacy proof
+ end-to-end verification
          ↓
STAGE 2 — ARTIFICIAL SOUL DEVELOPMENT
Puspa + Companion B
identity/self-life/emotional continuity/appraisal/bounded agency
OpenClaw-first; add optional components only from evidence
          ↓
STABILIZATION / PORTABILITY GATE
backup / recovery
config + secret separation
regression / operational hardening
runtime portability
          ↓
STAGE 3 — SECURITY + HOSTING / HYBRID CLOUD
security hardening
secure remote/private access
private server/cloud OpenClaw when feasible
          ↕ secure bridge
local Home Assistant / premises
```

Stage 3 hosting/cloud work must not branch or delay Stage 0/1/2. Home Assistant remains local-premises operational authority unless explicitly changed later.

## Architecture (when applicable)

```text
                     TEMAYA PERSONA
                          │
        ┌─────────────────┼──────────────────┐
        │                 │                  │
    SOUL.md          IDENTITY.md      runtime AGENTS.md
 personality         identity          operating rules
 boundaries                             memory rules
        └─────────────────┬──────────────────┘
                          │
                    Reply runtime
                          │
          ┌───────────────┴────────────────┐
          │                                │
   SELF-LIFE DOMAIN                  HUMAN DOMAIN
    "cerita aku"                "cerita user dekat aku"
          │                                │
 self-life/                        per-user boundary
 ├── STATE.md                      USER.md
 ├── CANON.md                      MEMORY.md
 └── events/                       memory/YYYY-MM-DD.md
          │                                │
          └───────────────┬────────────────┘
                          │
                  OpenClaw memory-core
                index / recall / provenance
```

## Native-vs-custom capability matrix

| Requirement | Classification | v0.1 decision |
|---|---|---|
| Personality/tone/boundaries | NATIVE OPENCLAW — USE AS-IS | `SOUL.md` |
| Identity basics | NATIVE OPENCLAW — USE AS-IS | `IDENTITY.md` |
| Operating/memory rules | NATIVE OPENCLAW — CONFIGURE/EXTEND | OpenClaw workspace `AGENTS.md` |
| Stable user model | NATIVE OPENCLAW — USE AS-IS | `USER.md` |
| Human episodic memory | NATIVE OPENCLAW — USE AS-IS | `memory/YYYY-MM-DD.md` |
| Durable human memory | NATIVE OPENCLAW — CONFIGURE/EXTEND | `MEMORY.md` + native consolidation |
| Search/index/provenance | NATIVE OPENCLAW — USE AS-IS | memory-core / SQLite |
| Time-based generation | NATIVE OPENCLAW — USE AS-IS | Scheduled Tasks / Cron |
| Event-triggered behaviour | NATIVE OPENCLAW — USE AS-IS | Standing Intents |
| Ambient checks | NATIVE OPENCLAW — USE AS-IS | Heartbeat where suitable |
| Temaya self-life history | CUSTOM TEMAYA LAYER REQUIRED | `self-life/` |
| Generate self-life events | CUSTOM TEMAYA LAYER REQUIRED | small Life Event Generator |
| Search/index self-life | NATIVE OPENCLAW — CONFIGURE/EXTEND | native index / extra paths if supported |
| Self-life Dreaming | UNKNOWN — NEED TEST | do not build replacement yet |
| Strict per-user privacy | NATIVE OPENCLAW — CONFIGURE/EXTEND | agent/workspace or stronger boundary |
| Retrieval scoping by path/source | UNKNOWN — NEED TEST | validate before wrapper |

## Self-life model

```text
self-life/
├── STATE.md
├── CANON.md
└── events/
    └── YYYY-MM-DD.md
```

- `STATE.md`: active routines, interests, story arcs and current state.
- `CANON.md`: durable self-life constraints/facts that should not drift casually.
- `events/YYYY-MM-DD.md`: episodic self-life events.

Minimum event semantics:

```text
event_id: unique id
persona: persona id
event_time: timestamp
source: generated_self_life
reality_class: persona_narrative
status: occurred
event: ...
```

`reality_class: persona_narrative` prevents generated persona-life events from being confused with external-world facts.

## Human-memory model

Each human has a private memory boundary.

```text
Hani private context
├── USER.md
├── MEMORY.md
└── memory/YYYY-MM-DD.md

Hafiz private context
├── USER.md
├── MEMORY.md
└── memory/YYYY-MM-DD.md
```

Exact production topology remains open, but prompt selection alone is not treated as a sufficient security boundary.

## Self-life lifecycle

```text
generate event
      ↓
read STATE + CANON + recent events
      ↓
validate / contradiction check
      ↓
record event
      ↓
update STATE if needed
      ↓
native index / provenance
      ↓
recall when relevant
      ↓
reflect
      ↓
consolidate / archive
```

Rules:
- read-before-generate;
- do not contradict stored history casually;
- recall an existing event instead of generating a new one for the same question;
- use native OpenClaw scheduler first;
- use Dreaming/native consolidation if tests show it preserves the self-life boundary.

## Prompt / context injection flow

```text
incoming message
      ↓
select relevant memory domain
      │
      ├── self question
      │     → retrieve relevant self-life
      │
      ├── current-user memory question
      │     → retrieve current user's private memory only
      │
      └── ordinary conversation
            → no broad memory load
      ↓
compose only relevant context
```

Target context:

```text
SOUL
+ IDENTITY
+ relevant current USER profile
+ relevant self-life
+ relevant current-user memory
+ recent conversation
+ applicable intent/event
```

## Privacy / isolation model

Locked requirements (D-025, D-027):
- user-private memory never crosses user boundaries;
- self-life never becomes a human-memory namespace;
- human memory never becomes self-life;
- all writes carry provenance/source;
- use agent/workspace isolation or stronger boundary when privacy requires it;
- each human has a private OpenClaw agent/workspace or equivalent isolation boundary;
- cross-agent access is deny-by-default and explicit allow only;
- exact separate Gateway/host topology remains an implementation/open boundary, not a design blocker.

Candidate topology:

```text
Logical Temaya system
├── Puspa/Hani agent boundary
│   └── Hani private memory
├── Hafiz companion agent boundary
│   └── Hafiz private memory
└── future child agent boundary
    └── child private memory
```

If multiple agents later share one persona self-life, use one authoritative writer with controlled readers.


## Data authority boundary

Locked by D-028:

```text
Knowledge / Library
→ Dzuddiyn Library / document stores

Persona + conversational memory
→ OpenClaw

Operational household state
→ Home Assistant
```

Do not duplicate authoritative state without a demonstrated need. OpenClaw may read/direct Home Assistant through approved integration, while Home Assistant remains authority for household operational state.

## Self-life ownership

Locked by D-029:
- one authoritative self-life writer per persona;
- Puspa agent writes canonical Puspa self-life;
- Companion B agent writes canonical Companion B self-life;
- other agents are read-only unless explicit write authority is granted.

## Scheduler / event model

```text
TIME-BASED
→ native Scheduled Task / Cron

EVENT-BASED
→ native Standing Intent

AMBIENT BACKGROUND CHECK
→ Heartbeat when suitable
```

No second scheduler.

For Phase 1, one daily scheduled self-life event is enough.

## Risks / failure modes

| Risk | Guardrail |
|---|---|
| New story invented every time user asks | recall-before-generate |
| Contradictory self-life | read STATE + CANON + recent events before write |
| Human memory enters self-life | separate domains + provenance |
| User memory leaks to another user | per-user agent/workspace or stronger boundary |
| Persona narrative treated as real-world fact | `reality_class: persona_narrative` |
| `SOUL.md` becomes autobiography | life events stay outside SOUL |
| Duplicate scheduler/reflection stack | native-first rule |
| Wrong-domain retrieval | domain/path/source validation |
| Two writers corrupt shared persona state | single authoritative writer if sharing is introduced |
| Context bloat | retrieve only relevant memory |
| Provider lock-in | text-first state + model-agnostic interfaces |

## Open questions / NEED TEST

1. Can Dreaming process self-life without mixing it into human `MEMORY.md`?
2. Can native retrieval reliably scope by source/path/domain?
3. Is per-agent/workspace isolation on one Gateway sufficient in practice, or is stronger Gateway/host separation needed for some family-private data?
4. What minimum provenance metadata is enough for Phase 1?

These are implementation/validation questions. D-027–D-029 now provide the design baseline and none of the items above is currently treated as a blocker to opening CONFIRM DESIGN review.

## Minimal Phase 1 prototype

```text
PUSPA — PHASE 1

Native OpenClaw:
SOUL.md
IDENTITY.md
OpenClaw workspace AGENTS.md
USER.md
MEMORY.md
memory/
memory-core
Scheduled Task

Custom Temaya:
self-life/
├── STATE.md
├── CANON.md
└── events/

+ one small state-aware Life Event Generator
```

Acceptance:
- morning: one Puspa self-life event exists;
- afternoon: Hani asks what Puspa did/ate;
- Puspa recalls the same stored event;
- Hani shares one personal story;
- later Puspa recalls Hani's story;
- Hani story is absent from self-life;
- Puspa self-life is absent from Hani fact memory;
- no custom DB;
- no second scheduler;
- no custom reflection engine;
- no web UI.

## Design status

Core decisions D-021–D-034 are LOCKED.

Overall design remains **PENDING CONFIRMATION**.

D-030 keeps Artificial Soul as an official architecture domain. D-034 schedules its detailed development deliberately in Stage 2, after Minimum Useful Temaya is delivered. It does not block Stage 0 or Stage 1.

**Core architecture readiness:** SUFFICIENT FOR REVERSIBLE FOUNDATION WORK and the D-032 Minimum Useful Temaya Phase 1 path.

**Confirmation readiness:** AP-000 may execute first as reversible foundation work. After AP-000 PASS, AC-016 requires a `CONFIRM DESIGN` gate before broader private-memory exposure, messaging ingestion, Google writes or Home Assistant control. Artificial Soul detail, Dreaming behaviour, retrieval scoping, exact Gateway/host isolation, emotional-state implementation, agency mechanism and provenance details remain deferred/OPEN/NEED TEST unless explicitly locked.
