# LifeOS Reuse-First Research & Pre-Confirmation Architecture Challenge

**Date:** 2026-10-05  
**Status:** D-039 SUPPORTING RESEARCH — reuse discipline and challenge flow LOCKED; named component adoption remains evidence-gated  
**Scope:** Temaya + OpenClaw + Dzuddiyn Library + n8n + Home Assistant + Google services  
**Authority:** This note does not override any D-xxx LOCKED decision in `ZASS_Temaya.md`.

## Purpose

Avoid rebuilding capabilities that already exist in maintained open-source projects, OpenClaw plugins/skills, n8n nodes/workflows, Home Assistant integrations, or mature document/knowledge tools.

Working principle:

> Reuse first. Integrate second. Adapt third. Build custom only when a verified gap remains.

The objective is not to adopt another LifeOS wholesale. Temaya remains a family-oriented architecture with explicit identity, privacy, memory and household-authority boundaries.

## Reuse hierarchy

Prefer, in order:

1. Existing capability already bundled in the chosen runtime.
2. Official/maintained plugin or integration.
3. Well-maintained open-source component with an API and migration path.
4. Small adapter around an existing component.
5. Custom subsystem only after the gap is demonstrated.

Every candidate must still pass privacy, authority, security, maintenance, recovery and exit-path review.

## High-value reuse candidates

### RC-L01 — OpenClaw ClawHub + official plugin inventory

OpenClaw now has a public registry for versioned skills/plugins and an official plugin inventory. Treat these as the first discovery surface before writing custom OpenClaw integrations.

Relevant current capabilities/candidates include:
- `active-memory` — bounded pre-reply retrieval / per-agent Remember;
- `document-extract` — extract text/page images from document attachments;
- `telegram` — bundled Telegram channel;
- `whatsapp` — official external WhatsApp channel;
- `imap` — authenticated incoming-mail watcher to isolated agent sessions;
- `onepassword` / `vault` — secret references and audited secret access;
- local/cloud model-provider plugins;
- speech / realtime-transcription / TTS plugins.

**Temaya use:** reduce custom channel, attachment, memory-tool and provider plumbing.

**Guardrail:** plugin capability does not transfer canonical authority to OpenClaw.

References:
- https://docs.openclaw.ai/tools/clawdhub
- https://docs.openclaw.ai/plugins/plugin-inventory

### RC-L02 — OpenClaw Skill Workshop for Temaya-specific reusable behaviour

OpenClaw Skill Workshop provides a proposal/review/apply lifecycle for reusable skills.

Candidate Temaya skills:
- librarian intake;
- classify candidate as TASK / LIBRARY / ARCHIVE / NOTHING;
- provenance capture;
- approval-request wording;
- source-aware summarization;
- safe DL retrieval;
- household briefing.

**Temaya use:** implement reusable behaviour as inspectable skills before building a custom application/service.

**Guardrail:** important durable writes remain policy/workflow governed and independently verified.

Reference:
- https://docs.openclaw.ai/skills

### RC-L03 — n8n as deterministic ingestion/workflow gatekeeper

n8n already supplies integrations/workflow patterns for Google Tasks, Calendar, Drive, Telegram and Home Assistant plus generic HTTP/webhook/API support.

Candidate responsibilities:
- normalize incoming events;
- deduplicate by source/event id;
- classify/route candidate records;
- maintain approval lifecycle;
- schedule workflows;
- retry safely;
- call Google Tasks/Calendar/Drive;
- perform read-back verification;
- produce audit/event history;
- coordinate cross-system workflows.

**Temaya use:** the “librarian clerk/workflow keeper”, not the library itself.

**Do not make n8n:**
- canonical memory authority;
- persona authority;
- privacy-policy decision-maker delegated to an LLM;
- mandatory hop for simple OpenClaw → HA actions.

References:
- https://n8n.io/integrations/google-tasks/
- https://n8n.io/integrations/google-calendar/
- https://n8n.io/integrations/google-drive/
- https://n8n.io/integrations/home-assistant/

### RC-L04 — Official Home Assistant MCP Server

Use the official HA MCP Server as the primary candidate bridge for direct OpenClaw/Temaya access to selected HA entities.

**Temaya use:** read verified household state and perform narrowly exposed actions without custom HA middleware.

**Guardrail:** HA remains household/device/automation authority; expose only approved entities.

Reference:
- https://www.home-assistant.io/integrations/mcp_server

### RC-L05 — Paperless-ngx for document ingestion/OCR

Paperless-ngx is an open-source document-management system with OCR-oriented ingestion and a documented REST API.

Potential DL use:
- receipts;
- bills;
- scanned letters;
- manuals;
- invoices;
- paper correspondence.

Possible role:
`scan/file → Paperless ingestion/OCR/metadata → approved promotion/reference into DL`.

**Do not assume:** Paperless becomes the whole Dzuddiyn Library or canonical owner of all knowledge.

**Decision test:** adopt only if it materially removes OCR/document-management work that Temaya would otherwise need to build.

References:
- https://docs.paperless-ngx.com/
- https://docs.paperless-ngx.com/api/

### RC-L06 — Obsidian + API plugin as a human DL surface

Obsidian remains a candidate human-facing PC/phone surface for inspectable Markdown-based knowledge. Community open-source REST API plugins can expose CRUD/search/metadata operations to local automation.

Potential use:
- human browse/edit surface;
- Markdown-native DL access;
- n8n/OpenClaw integration through a constrained local API.

**Guardrail:** Obsidian/plugin is a surface/adapter; it must not silently become a second authority.

Candidate references:
- https://github.com/swarogan/obsidian-api
- https://github.com/Yant2023/obsidian-localserver-api

## Patterns to reuse from existing LifeOS projects

1. **Architecture large, deployment small.**
2. **Canonical human-readable data is more important than the app.**
3. **Indexes/embeddings are rebuildable derived state, not canonical truth.**
4. **External feeds are untrusted observations, not instructions or durable memory.**
5. **Raw → Candidate → Approved → Canonical promotion.**
6. **Human Queue for ambiguity/consequential actions.**
7. **Jobs/workflows must be restart-safe, deduplicated and idempotent.**
8. **Deterministic permission/privacy boundaries; LLMs may interpret but not grant access.**
9. **Framework/code separated from private family data and secrets.**
10. **Model roles instead of hard-coded model names.**
11. **Graceful degradation: HA, DL, Temaya, n8n and cloud providers fail independently where practical.**
12. **UI/channel is a surface, not the source of truth.**
13. **Identity resolution across channels, while preserving per-user isolation.**
14. **Plugin/reuse-first before custom subsystem construction.**

## Mandatory pre-confirmation Architecture Challenge — D-039

**Status:** MANDATORY PRE-GATE-C001 REVIEW — LOCKED VIA D-039.

Run after AP-000 evidence is complete and before the owner completes `GATE-C001 — CONFIRM DESIGN`. D-039 makes this challenge mandatory while D-038 remains the owner confirmation gate.

### Challenge methods

1. **First-principles / authority review**  
   For every data/action class: who owns truth, who may derive/cache, who may write?

2. **Reuse / Integrate / Adapt / Build matrix**  
   For every planned subsystem, search existing OpenClaw skills/plugins, n8n nodes/templates, HA integrations and mature OSS first.

3. **Event Storming / lifecycle walkthrough**  
   Walk real events end-to-end: private DM, group message, school notice, document, task, calendar commitment, DL reference, HA command.

4. **Pre-mortem + FMEA**  
   Assume Temaya failed after six months. Identify likely failure modes, severity, detection and recovery.

5. **Threat/privacy challenge**  
   Test prompt injection, cross-user leakage, over-broad plugin permissions, secret exposure and untrusted-feed promotion.

6. **Graceful-degradation test**  
   What still works if internet/cloud AI/OpenClaw/n8n/DL index/HA bridge is unavailable?

7. **Migration/exit test**  
   Can data, workflows and identity rules survive replacement of a model, plugin, OpenClaw, n8n or storage implementation?

8. **Reference-project cross-check**  
   Compare the design against proven LifeOS/assistant patterns; record what is reused, deliberately rejected, or still unique to Temaya.

9. **ZASSELECTION for genuine alternatives**  
   When two or more viable implementations remain, compare them explicitly before locking.

### Expected outputs

- capability/reuse inventory;
- authority matrix;
- data/event lifecycle;
- candidate plugin/component matrix;
- build-vs-reuse decisions with rationale;
- failure/privacy findings;
- unresolved architecture gates;
- proposed updates to `DESIGN.md` and `ACTION_PLAN.md`;
- only then owner `CONFIRM DESIGN`.

## Candidate adoption rule

A plugin/open-source component should be adopted only when it:
- removes meaningful custom work;
- respects the locked authority/privacy boundaries;
- is inspectable and maintainable;
- supports backup/export/migration;
- can be permission-scoped;
- has a recoverable failure mode;
- does not create a duplicate canonical store without an explicit decision.

For plugins:
- prefer bundled/official/maintained sources;
- inspect source/security status;
- pin production versions;
- test in a reversible POC;
- verify after installation;
- keep an uninstall/exit path.

## Current interpretation

Likely reusable rather than custom-built:
- Telegram channel → OpenClaw bundled plugin;
- WhatsApp channel → official OpenClaw plugin, subject to runtime proof;
- HA bridge → official HA MCP;
- cross-system workflow / librarian gatekeeper → n8n;
- attachment text extraction → OpenClaw document-extract where sufficient;
- document OCR/filing → evaluate Paperless-ngx before custom work;
- human-readable library surface → evaluate Obsidian + constrained API;
- reusable Temaya procedures → OpenClaw Skills/Skill Workshop;
- Google Tasks/Calendar/Drive workflow → n8n/direct supported integration first;
- Apps Script → compatibility helper only when a verified Google-specific gap remains.

Still likely Temaya-specific:
- multi-user family privacy/identity policy;
- Temaya self-memory vs human-memory separation;
- D-036 external-feed approval semantics;
- authority mapping across DL/OpenClaw/HA;
- family-specific persona/continuity rules;
- provenance and promotion rules that bind the whole system together.
