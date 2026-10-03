# TEMAYA — PRE-EXECUTION BLOCKER & OPEN-ITEM AUDIT

**Method:** ZASSIMPLE_MY v0.3.0  
**Purpose:** Close only the decisions that are actually due before execution, while preserving later-stage options.  
**Workflow:** AUDIT → pre-architecture refinement → ACTION_PLAN ordering → task slicing → execution → evidence → CONFIRM DESIGN gate after AP-000.

> Rule: an OPEN item is not automatically a blocker. It becomes a blocker only at its stated **DUE GATE**.

---

# HOW TO FILL

For each item, fill only:

- **OWNER CHOICE:** ...
- **NOTES / CONSTRAINTS:** ...

You may simply write **ACCEPT RECOMMENDATION**.

Status meanings:
- **NOW** — resolve before AP-000 real install.
- **AFTER AP-000** — resolve using real runtime evidence before CONFIRM DESIGN.
- **BEFORE Mx** — defer until that milestone becomes current.
- **STAGE 2 / STAGE 3** — intentionally deferred.

---

# A — NOW: AP-000 PRE-REQUISITES

## A1 — Q-001 Mini-PC host topology
**DUE:** NOW — before installing both OpenClaw and Home Assistant.

**Need to decide:** how the mini PC hosts HA and OpenClaw while preserving D-010 independence.

**RECOMMENDATION:**  
Use a virtualization boundary if the mini-PC resources are sufficient:

```text
Mini PC
└── Hypervisor
    ├── HAOS VM
    └── Linux VM
        └── OpenClaw
```

Why:
- clean HA/OpenClaw failure isolation;
- easier backup/snapshot/migration;
- supports D-031 future portability;
- avoids mixing HA appliance concerns with OpenClaw/Linux runtime.

If hardware resources are too limited, choose the simplest supported alternative during AP-000 and document the trade-off rather than over-engineer.

**OWNER CHOICE:**  
**NOTES / CONSTRAINTS:**  

---

## A2 — Mini-PC actual hardware / capacity
**DUE:** NOW.

**Need to record:** CPU, RAM, storage, NIC(s), virtualization support.

**RECOMMENDATION:**  
Do not lock a deployment topology before checking the actual mini-PC capacity. AP-000 should begin with a resource inventory.

**OWNER CHOICE:**  
**NOTES / CONSTRAINTS:**  

---

## A3 — AP-000 LLM/provider baseline
**DUE:** NOW / during OpenClaw install.

**Need to decide:** one working model/provider/auth route for foundation testing.

**RECOMMENDATION:**  
Use **one provider only** for AP-000 — whichever is already available, stable and affordable. Do **not** lock Temaya architecture to that provider. Provider comparison belongs later only if a real need appears.

**OWNER CHOICE:**  
**NOTES / CONSTRAINTS:**  

---

## A4 — D-035 Day-0 security baseline
**DUE:** NOW.

**LOCKED baseline:** no unnecessary public exposure; auth/access controls; secrets out of Git/searchable memory; explicit authorization/allowlists; recoverable config/state.

**RECOMMENDATION FOR AP-000:**
- LAN/private access only;
- no router port-forward/public URL;
- use auth where supported;
- credentials outside repository;
- basic backup/snapshot before risky changes;
- record where OpenClaw and HA state/config live.

**OWNER CHOICE:** ACCEPT LOCKED BASELINE / ADD CONSTRAINTS  
**NOTES / CONSTRAINTS:**  

---

# B — AFTER AP-000: EVIDENCE-INFORMED CORE DESIGN GATE

## B1 — Host topology validation
**DUE:** AFTER AP-000, before CONFIRM DESIGN.

Check:
- Did chosen topology run reliably?
- Is restart/recovery understandable?
- Are HA/OpenClaw genuinely failure-isolated enough?
- Is backup/migration practical?

**RECOMMENDATION:**  
Keep the topology if it passes. Do not redesign merely for elegance.

**OWNER CHOICE:**  
**EVIDENCE / NOTES:**  

---

## B2 — Mandatory CONFIRM DESIGN gate
**DUE:** immediately after AP-000 PASS.

**AGREED (AC-016):** do not proceed to broader private memory, production messaging ingestion, Google writes or HA control until owner completes ZASS `CONFIRM DESIGN`.

**RECOMMENDATION:**  
At this gate, review actual AP-000 evidence and close only Stage-1 prerequisites. Do not reopen Stage-2/3 items.

**OWNER CHOICE:** ACCEPT / MODIFY  
**NOTES:**  

---

# C — BEFORE M2: HUMAN MEMORY / PRIVACY

## C1 — Exact isolation topology
**DUE:** BEFORE M2.

**Existing locks:** D-025 + D-027.

**Need to determine:** whether one OpenClaw Gateway with separate agents/workspaces is sufficient for the required family privacy, or whether stronger process/Gateway/host separation is necessary.

**RECOMMENDATION:**  
Start with:
- separate agent/workspace + separate private memory domain per human;
- deny-by-default cross-agent access;
- no shared durable personal memory.

Then test leakage/authorization. Escalate to stronger Gateway/process/host isolation only if the native boundary cannot meet the privacy requirement.

**OWNER CHOICE:**  
**NOTES:**  

---

## C2 — Q-005 family data classes
**DUE:** BEFORE M3/M4 multi-user/external feeds.

**RECOMMENDATION:** use four simple classes:

1. **PRIVATE-HUMAN** — one person only.
2. **FAMILY-SHARED** — explicitly shareable inside family.
3. **EXTERNAL-FEED** — WhatsApp/Telegram/school/community input; D-036 approval required before durable promotion/action.
4. **SYSTEM/OPERATIONAL** — HA/device/system state; not human memory.

Children/school information stays PRIVATE or FAMILY-SHARED unless explicitly promoted.

**OWNER CHOICE:**  
**NOTES:**  

---

# D — BEFORE M3/M4: TELEGRAM + WHATSAPP

## D1 — D-036 approval UX
**DUE:** BEFORE first production-like group-reader use.

**LOCKED rule:** external/group feed may be read/summarized/classified, but durable write/action needs user approval of relevance/interpretation + next action.

**RECOMMENDATION:** one compact approval interaction:

```text
Temaya found:
"School sports day: 18 Oct, 8:00 AM"

Related to our family?
[YES] [NO] [EDIT]

If YES:
What should I do?
[CALENDAR] [TASK] [LIBRARY] [ARCHIVE] [NOTHING]
```

No approval = temporary context only / no durable promotion.

**OWNER CHOICE:**  
**NOTES:**  

---

## D2 — Q-019 persona routing
**DUE:** BEFORE multi-user channel rollout.

**RECOMMENDATION:** avoid AI guessing identity/persona from message content.

Initial deterministic routing:
- Hani private identity/channel → Puspa.
- Hafiz default personal route → Companion B.
- Hafiz explicitly invokes/selects Companion A for technical/idea work.
- group feed reader operates as Temaya ingestion function, not as a private persona memory writer.

Later, richer routing can be added only if useful.

**OWNER CHOICE:**  
**NOTES:**  

---

## D3 — Channel scope
**DUE:** BEFORE M3/M4.

For each group/channel, classify:
- permitted to read?
- permitted to summarize?
- which human may approve promotion/actions?
- retention policy for raw feed?

**RECOMMENDATION:** allowlist groups one-by-one. Start read/summarize only.

**OWNER CHOICE:**  
**NOTES:**  

---

# E — BEFORE M5: GOOGLE TASKS / CALENDAR / DRIVE

## E1 — Task vs Calendar object rule
**DUE:** BEFORE Google write automation.

**RECOMMENDATION: use BOTH, with no duplication.**

### Google Tasks
Use when the primary meaning is **something to do**:
- call someone;
- pay fee;
- buy item;
- submit form;
- homework/action item;
- recurring chore;
- reminder with due date/time.

### Google Calendar
Use when the primary meaning is **something happening at a time/date**:
- appointment;
- school event;
- medical visit;
- shift;
- meeting;
- trip;
- exam/event window;
- family commitment;
- external date that should coexist with other events/holidays/availability.

Rule:
```text
ACTION → Task
EVENT / TIME COMMITMENT → Calendar
REFERENCE KNOWLEDGE → Library
```

A dated Google Task can already appear in Calendar, so do not create a duplicate Calendar event merely to make a task visible.

**OWNER CHOICE:**  
**NOTES:**  

---

## E2 — Google write approval
**DUE:** BEFORE M5 writes.

**RECOMMENDATION:**
- user-created direct request ("add this task") may execute directly once identity/permission is clear;
- external-feed-derived candidate must obey D-036 approval first;
- important writes read back and verify.

**OWNER CHOICE:**  
**NOTES:**  

---

## E3 — Apps Script boundary
**DUE:** BEFORE first Apps Script addition.

**RECOMMENDATION:** Apps Script only when Google-specific deterministic logic is clearly simpler than direct OpenClaw/plugin/API use.

Do not make Apps Script:
- Temaya runtime;
- mandatory middleware;
- universal state store.

**OWNER CHOICE:** ACCEPT / MODIFY  
**NOTES:**  

---

# F — BEFORE M6: DZUDDIYN LIBRARY

## F1 — Q-003 authoritative physical storage
**DUE:** BEFORE M6 implementation.

**Agreed architecture (AC-015):**
Dzuddiyn Library is knowledge authority; clients/indexes are not.

**RECOMMENDATION DEFAULT:**  
If current Dzuddiyn Library is already practical in Google Drive, keep Google Drive/document stores as Stage-1 authoritative storage rather than migrating everything. Add local/other storage later only for a proven need.

**OWNER CHOICE:**  
**NOTES:**  

---

## F2 — Human access surface
**DUE:** BEFORE M6.

**RECOMMENDATION:**  
Use the simplest existing PC/phone access first. Add Obsidian only where its local Markdown/linking/search UX materially improves use. Obsidian must not become a second authority requiring bidirectional reconciliation unless explicitly designed.

**OWNER CHOICE:**  
**NOTES:**  

---

## F3 — OpenClaw retrieval layer
**DUE:** BEFORE M6.

**RECOMMENDATION:**  
OpenClaw index/cache/search is derived and rebuildable. Preserve source IDs/links/provenance back to authoritative documents.

**OWNER CHOICE:** ACCEPT / MODIFY  
**NOTES:**  

---

# G — BEFORE M7: HOME ASSISTANT BASIC

## G1 — Q-011 control split refinement
**DUE:** BEFORE M7.

**Existing direction:** D-007/D-008/D-010/D-028.

**RECOMMENDATION:**
- ordinary deterministic household automations stay in HA;
- OpenClaw interprets higher-level intent and calls permitted HA capabilities;
- sensitive actions use permission/gating below the LLM;
- start with a tiny read set + one controlled reversible action.

**OWNER CHOICE:**  
**NOTES:**  

---

# H — BEFORE M8: SMART SPEAKER

## H1 — Q-013 Speaker-ID engine
**DUE:** BEFORE M8.
**NOW:** DEFER.

**RECOMMENDATION WHEN DUE:** benchmark 1–2 simple candidates; Speaker ID must not be the only authorization signal for sensitive actions.

**OWNER CHOICE NOW:** DEFER / OTHER  
**NOTES:**  

---

## H2 — Q-014 audio transport
**DUE:** BEFORE M8.
**NOW:** DEFER.

**RECOMMENDATION WHEN DUE:** choose the simplest reliable local transport that ESPHome/end-device and Voice Gateway can support; avoid streaming complexity until required.

**OWNER CHOICE NOW:** DEFER / OTHER  
**NOTES:**  

---

## H3 — Q-015 return audio codec/path
**DUE:** BEFORE M8.
**NOW:** DEFER.

**RECOMMENDATION WHEN DUE:** begin with a simple file/URL/local playback path if it meets latency/usability; upgrade to streaming only if evidence requires it.

**OWNER CHOICE NOW:** DEFER / OTHER  
**NOTES:**  

---

# I — STAGE 2: ARTIFICIAL SOUL

## I1 — Artificial Soul implementation details
**DUE:** STAGE 2.
**NOW:** DEFER.

Review then:
- D-015 daily/custom engine mechanism;
- D-023 exact self-life schema;
- D-024 generator implementation;
- D-026 implementation prescription;
- D-029 exact writer mechanism;
- emotion/appraisal/agency model;
- optional Emotion Engine / other components.

**RECOMMENDATION:** decide from the working Stage-1 OpenClaw system, not assumptions.

**OWNER CHOICE NOW:** DEFER / OTHER  
**NOTES:**  

---

# J — STAGE 3: SECURITY / HOSTING / CLOUD

## J1 — Cloud/private server
**DUE:** STAGE 3.
**NOW:** DEFER.

Evaluate then:
- private cloud/VPS/managed server;
- cloud OpenClaw ↔ local HA secure bridge;
- cost;
- operational burden;
- privacy;
- latency;
- disaster recovery.

**OWNER CHOICE NOW:** DEFER / OTHER  
**NOTES:**  

---

## J2 — Security hardening
**DUE:** STAGE 3.
**NOW:** DEFER beyond D-035 baseline.

Evaluate:
- network segmentation;
- hardened ingress;
- stronger secrets management;
- audit/logging;
- stronger tenant/cell isolation;
- mature backup/DR;
- remote access architecture.

**OWNER CHOICE NOW:** DEFER / OTHER  
**NOTES:**  

---

# K — NON-BLOCKING / PARKED ITEMS

These are not blockers for Stage 0/1 unless explicitly promoted.

## K1 — Q-007 meaning of local-first
**RECOMMENDATION:** interpret pragmatically: local authority/control where important; cloud reasoning/services allowed. Do not require all inference local.

**OWNER CHOICE:** ACCEPT / MODIFY / DEFER  
**NOTES:**  

## K2 — Q-008 Ryzen workstation
**RECOMMENDATION:** optional extension only; not Temaya core requirement.

**OWNER CHOICE:** ACCEPT / MODIFY / DEFER  
**NOTES:**  

## K3 — Q-010 robot companion
**RECOMMENDATION:** future peripheral/subproject after smart-speaker/core value is proven.

**OWNER CHOICE:** ACCEPT / MODIFY / DEFER  
**NOTES:**  

## K4 — Q-020 exact Persona Life Rules
**RECOMMENDATION:** defer to Stage 2 Artificial Soul review.

**OWNER CHOICE:** DEFER / OTHER  
**NOTES:**  

## K5 — Q-021 Umar exact English boy-robot TTS
**RECOMMENDATION:** defer until Umar device/voice implementation becomes current.

**OWNER CHOICE:** DEFER / OTHER  
**NOTES:**  

---

# L — STALE OPEN ITEMS / CONFLICTS TO CLOSE AFTER OWNER AUDIT

Proposed cleanup after this form is completed:

- Q-006 WhatsApp timing → RESOLVED by D-032/M4.
- Q-009 Puspa smart-speaker prototype priority → effectively RESOLVED by D-032/M8 vital smart speaker.
- CF-001 local vs cloud contradiction → RESOLVED by D-031/D-034 staged hybrid mapping.
- CF-003 custom WhatsApp containers vs native routing → use native/maintainable OpenClaw-supported route first; custom bridge only on proven gap.
- R-005 overbuild → mitigated by D-034 linear stages.
- R-006 mandatory Apps Script middleware → mitigated/resolved by D-031/D-032 boundary.
- R-009 subsystem overlap → mitigated by D-028 authority domains + D-034 linear plan.

**OWNER CHOICE:** ACCEPT PROPOSED CLEANUP / MODIFY  
**NOTES:**  

---

# M — AUDIT COMPLETION GATE

The audit is sufficient to start AP-000 when:
- A1–A4 are answered;
- no unresolved NOW item blocks installation;
- D-035 baseline is accepted/applied;
- T-F000 remains the only promoted execution task.

The audit is sufficient for core DESIGN confirmation after AP-000 when:
- B1–B2 are completed with actual evidence;
- C/D/E/F/G/H items are either resolved at their due gate or explicitly deferred with no impact on the next milestone;
- ZASS `CONFIRM DESIGN` is explicitly completed by the owner.

After owner fills this form:
1. Distill answers.
2. Update OPEN/RESOLVED statuses.
3. Build the evidence-informed pre-architecture.
4. Refine ACTION_PLAN by priority + prerequisites.
5. Slice only the next eligible task(s).
6. Execute Stage 0.
