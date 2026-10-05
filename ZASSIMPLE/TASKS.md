# TEMAYA — ZASSIMPLE TASKS

**Method:** ZASSIMPLE_MY v0.3.0  
**Status:** EXECUTION QUEUE  
**Authority:** Tasks execute the plan. They do not rewrite LOCKED decisions.  
**Execution policy:** Repository root `/AGENTS.md` applies to all engineering/execution work.

## Current task

### T-F001 | BLOCKED — Inspect Mini-PC Hardware / Firmware

**Type:** FOUNDATION / REVERSIBLE INSPECTION  
**Source:** D-033 / D-035 / AP-000 / PRE_EXECUTION_AUDIT  
**Evidence:** `ZASSIMPLE/EVIDENCE/T-F001_2026-10-04.md`

**Current state:** PARTIAL / BLOCKED — TARGET HOST NOT REACHABLE.

The only connected Desktop Commander device was verified as an Acer Nitro laptop with Intel Core i5-13420H, not the owner-declared Intel Core i3 circa-2018 mini PC. LAN observation identified existing Home Assistant and SMLIGHT/SLZB endpoints but did not provide inspectable access to the target mini PC.

**Do when target becomes reachable:** inspect:
- exact CPU model;
- x86-64 and virtualization support;
- RAM total/usable;
- storage type/health/free capacity;
- NIC;
- BIOS/UEFI/virtualization state.

**Pass:**
- exact target mini-PC hardware facts recorded;
- virtualization viability known;
- storage health known;
- a safe resource allocation for HAOS + Linux/OpenClaw is plausible.

**Blocker:** target mini PC must become remotely inspectable.  
**Do not proceed:** T-F002/T-F003 remain blocked.  
**Then after PASS:** T-F002.

## Queue

### T-F002 | BLOCKED BY T-F001 — Preserve / Prepare Host
Protect existing data, create rollback/backup point, and prepare the chosen hypervisor installation path.

### T-F003 | BLOCKED BY T-F002 — Hypervisor Foundation
Install/configure the selected hypervisor privately on LAN; no public exposure.

### T-F004 | BLOCKED BY T-F003 — HAOS VM
Create/start Home Assistant OS VM with conservative resources; verify HA reaches running state; record storage/config location.

### T-F005 | BLOCKED BY T-F004 — Linux + OpenClaw VM
Create minimal Linux VM; install supported Node/OpenClaw; create one minimal agent/workspace.

### T-F006 | BLOCKED BY T-F005 — ChatGPT/OpenAI Auth + Basic Conversation
Use owner-selected ChatGPT/OpenAI route; verify actual OAuth/model/allowance; prove one basic Temaya/OpenClaw conversation. Do not assume unlimited free usage.

### T-F007 | BLOCKED BY T-F006 — Day-0 Security Validation
Apply D-035. Inspect relevant Arcadyan AW1000/OpenWrt firewall/WAN/admin/UPnP/port-forward posture; keep HA/OpenClaw private; verify secrets are outside Git/searchable memory.

### T-F008 | BLOCKED BY T-F007 — Restart / Recovery Proof
Restart/reboot and independently verify HA + OpenClaw recovery, workspace/config/state locations, and the basic conversation path.

### T-C001 | BLOCKED UNTIL T-F008 PASS — Pre-Confirmation Architecture Challenge

**Source:** D-039  
**Trigger:** AP-000 evidence complete through T-F008.

Run the mandatory challenge flow:
1. capability/reuse inventory;
2. first-principles authority review;
3. real-event / Event Storming walkthrough;
4. Reuse / Integrate / Adapt / Build matrix;
5. threat/privacy challenge + pre-mortem/FMEA;
6. graceful-degradation / recovery test;
7. migration / exit-path test;
8. cross-check against mature LifeOS/assistant projects;
9. ZASSELECTION for unresolved viable alternatives;
10. reconcile findings into DESIGN.md ↔ ACTION_PLAN.md.

**Pass:** required D-039 outputs exist; any conflict with a LOCKED decision is surfaced as an explicit decision gate; DESIGN/ACTION_PLAN findings are reconciled without silently changing D-xxx authority.

### GATE-C001 | BLOCKED UNTIL T-C001 PASS — CONFIRM DESIGN

**Source:** D-038 + D-039 / ZASSIMPLE v0.3 confirmation discipline  
**Trigger:** AP-000 evidence complete through T-F008 **and** T-C001 Architecture Challenge PASS.  
**Owner action required then:** review the evidence-informed, reuse-challenged core design and explicitly complete the project confirmation command/gate.  
**Blocks:** private multi-user memory rollout, WhatsApp/Telegram production ingestion, Google writes, HA control.  
**Reminder:** surface this gate immediately when T-C001 passes; do not silently continue.

### GATE-N001 | DUE BEFORE COMPANION A/B BUILD — Final Names
Choose final names for Companion A and Companion B before those personas are instantiated/routed. This gate does not block AP-000 or Puspa-only work.

Stage sequence: AP-000 → T-C001 Architecture Challenge → GATE-C001 → AP-100 → AP-200 → Stabilization/Portability Gate → Stage 3 Security + Hosting/Hybrid Cloud.

Only tasks from the current eligible stage should be promoted. Later-stage tasks remain planned and must not create parallel execution branches.

## Delivered evidence

None yet.

<!--
Record verified outcomes that support DELIVERED !!
Required closure checks:
- Built: YES / NO
- Verified: YES / NO
- Matches design: YES / NO
- Recorded: YES / NO
Do not mark DELIVERED !! until all four are YES.
-->
