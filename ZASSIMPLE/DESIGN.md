# TEMAYA — ZASSIMPLE DESIGN

**Method:** ZASSIMPLE_MY v0.3.0  
**Design:** Temaya Living Design v0.1  
**Status:** DRAFT — PENDING CONFIRMATION
**Design Progress:** 4/4 — purpose / main flow / main elements / relevant LOCKED decisions  
**Authority:** Derived from LOCKED decisions in `ZASS_Temaya.md`.

> This is a working design draft. Temaya is a technical/system project, so architecture is retained as a subtype of DESIGN. It is not confirmed until the owner completes the ZASSIMPLE confirmation gate with `YA, CONFIRM DESIGN`.

## Purpose

Temaya must feel like a persona with a coherent life of its own while keeping private, per-human memory structurally separate.

```text
SELF-LIFE — "Ini cerita aku"
≠
HUMAN MEMORY — "Ini yang user pernah cerita dekat aku"
```

## Core principle

**OpenClaw-native first.**

Use native OpenClaw capabilities before custom Temaya machinery:
- `SOUL.md`, `IDENTITY.md`, `AGENTS.md`, `USER.md`;
- `MEMORY.md` and `memory/YYYY-MM-DD.md`;
- memory-core / SQLite index, recall and provenance;
- Scheduled Tasks / Cron;
- Standing Intents;
- Heartbeat;
- Dreaming / consolidation.

Custom layers are allowed only for proven gaps.

## Main flow

The primary flow is memory-domain selection → scoped recall/write → consistent reply.

## Main elements

Core elements are OpenClaw persona/bootstrap files, self-life domain, per-user human-memory domains, native memory-core/retrieval, native scheduling, and the small Life Event Generator.

## Architecture (when applicable)

```text
                     TEMAYA PERSONA
                          │
        ┌─────────────────┼──────────────────┐
        │                 │                  │
    SOUL.md          IDENTITY.md         AGENTS.md
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
| Operating/memory rules | NATIVE OPENCLAW — CONFIGURE/EXTEND | `AGENTS.md` |
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

Locked requirements:
- user-private memory never crosses user boundaries;
- self-life never becomes a human-memory namespace;
- human memory never becomes self-life;
- all writes carry provenance/source;
- use agent/workspace isolation or stronger boundary when privacy requires it.

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
3. If several agents share one persona life, what is the lightest single-writer/many-reader mechanism?
4. Is per-agent workspace on one Gateway enough for family privacy, or is stronger Gateway/host separation required?
5. What minimum provenance metadata is enough for Phase 1?

## Minimal Phase 1 prototype

```text
PUSPA — PHASE 1

Native OpenClaw:
SOUL.md
IDENTITY.md
AGENTS.md
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

Core decisions D-021–D-026 are LOCKED.

Overall design remains **PENDING CONFIRMATION** because Dreaming scope, retrieval scoping and production isolation still require testing.
