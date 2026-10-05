# CONTEXT SYNC — Home Assistant <> Temaya

**Date:** 2026-10-05  
**Status:** RECONCILED CONTEXT — NOT A NEW DECISION AUTHORITY  
**Authority:** Existing D-xxx LOCKED decisions in `ZASS_Temaya.md` remain authoritative.

## Purpose

Reconcile the prior project conversation **Home Assistant <> Temaya** and its AIoT Core context with the current canonical Temaya repository, without duplicating or silently changing architecture authority.

## Preserved context

### AIoT Core / Home Assistant role

- **AIoT Core** is the reusable premises/home-automation architecture direction.
- **Home Assistant** is the first local controller/runtime and remains the authority for physical household/device state, registry, deterministic automation and safe execution.
- Temaya is a reference integration over the reusable OpenClaw Core + AIoT Core boundary.
- Dzuddiyn Library is **not** a Home Assistant database and must not become one.

This is already represented by D-010, D-028, D-037, D-049 and DESIGN.

### OpenClaw ↔ Home Assistant integration

Primary path:
```text
OpenClaw / Temaya
      ↓
Official Home Assistant MCP
      ↓
Home Assistant authority
```

Fallbacks remain:
1. Home Assistant Conversation API
2. direct REST/WebSocket tools

Do **not** put n8n inline between OpenClaw and HA for ordinary direct control merely because n8n exists.

This is already represented by D-007 and the current DESIGN.

### Device / area context

- Home Assistant Device/Area Registry remains authoritative.
- OpenClaw/Temaya may keep a synced local cache/fallback for `device_id → area_id → area_name`.
- Cached localization is a fallback/context accelerator, not a competing registry authority.

Already locked by D-008.

### Privacy / authorization

- Sensitive access/permission decisions are deterministic policy concerns below/outside the LLM.
- LLMs may interpret intent but must not grant themselves authority.

Already locked by D-006, D-027, D-035, D-036 and D-046.

### n8n

n8n is useful when a **cross-system workflow** actually needs:
- normalization;
- deduplication;
- approval/Human Queue;
- retries/restart safety;
- scheduling;
- multi-step verified writes;
- Google/DL workflow orchestration.

n8n is **not** the default inline path for OpenClaw → HA control.

This aligns with D-039, D-043–D-045 and RC-004.

### Local AI / Ollama-like runtime

Local AI is a bounded replaceable compute provider for use cases such as:
- classification;
- structured extraction;
- local/private summarization;
- low-risk transformations;
- eligible offline/basic fallback.

It is not persona, memory, authorization or canonical knowledge authority.

Adoption remains benchmark/use-case gated, not mandatory.

Already locked by D-048, D-051 and D-052.

### MQTT / Node-RED / auxiliary services

- MQTT is introduced only when an actual device/integration requires it.
- ZHA / ESPHome / native HA do not imply MQTT is mandatory.
- Node-RED is not baseline; introduce only when its event-flow role is proven useful beyond HA-native automation/n8n.
- Do not inherit BSE-specific devices/inventory such as SLZB-MR2 into Temaya/AIoT Core baseline.

This aligns with D-053 and the reusable-core boundary.

## Planning consequence

The Home Assistant <> Temaya context strengthens this evidence order for the pre-confirmation Architecture Challenge:

```text
AP-000 PASS
   ↓
1. OpenClaw native/plugin capability audit
   ↓
2. Official HA MCP read-only / reversible proof
   ↓
3. HA registry/cache/fallback contract proof
   ↓
4. Local-AI bounded benchmark if hardware allows
   ↓
5. n8n workflow-gatekeeper POC on synthetic workflow
   ↓
6. DL/document/access/retrieval POCs
   ↓
7. Stage-1 ordering ZASSELECTION
   ↓
8. Reconcile DESIGN ↔ ACTION_PLAN
   ↓
GATE-C001 — CONFIRM DESIGN
```

Reason:
- prove the shortest direct authority path first;
- test optional orchestration only after the direct path is understood;
- avoid introducing workflow infrastructure merely to control HA;
- use evidence from the real HA/OpenClaw runtime before final Stage-1 ordering.

## No authority changes

This sync does **not**:
- alter D-007/D-008/D-010/D-028;
- make n8n mandatory;
- make local AI mandatory;
- change AP-100 milestone order by itself;
- bypass I-064 / P-C008 ZASSELECTION;
- bypass D-038/D-039 confirmation discipline.
