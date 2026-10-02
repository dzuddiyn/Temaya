# TEMAYA — ZASSIMPLE ACTION PLAN

**Method:** ZASSIMPLE_MY v0.3.0  
**Status:** INTERNAL WORKING ARTIFACT  
**Authority:** Planning artifact only. It must not override `D-xxx | LOCKED` decisions in `ZASS_Temaya.md`.

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

1. Prepare minimal Puspa `SOUL.md`, `IDENTITY.md` and memory rules in `AGENTS.md`.
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
- per-user privacy cannot be enforced at the required boundary;
- Dreaming mixes self-life with human durable memory.

Do **not** expand scope before the gap is documented.

## Planning findings

- Living Design v0.1 supports native OpenClaw memory/indexing/scheduler first.
- Custom scope is limited to the self-life namespace + state-aware event generator.
- Dreaming treatment, retrieval scoping and production isolation remain **NEED TEST**.
- Design remains **PENDING CONFIRMATION**.



None promoted yet.


## Locked persona/voice implementation constraints

- D-012: Companion A proactive technical inspiration uses randomized ~1–2 week timing; exact scheduler implementation remains open.
- D-015: Puspa + Companion B require daily persona-life generation constrained by profile/rules/canon; exact schema remains open.
- D-017: Companion A/B TTS baseline is `ms-MY-OsmanNeural` with their locked prosody/post-processing ranges.
- D-018: Umar requires an English boy-robot voice; exact English TTS voice and processing remain open.

These are planning constraints only; design remains unconfirmed.
