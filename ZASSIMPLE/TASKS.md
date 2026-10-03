# TEMAYA — ZASSIMPLE TASKS

**Method:** ZASSIMPLE_MY v0.3.0  
**Status:** EXECUTION QUEUE  
**Authority:** Tasks execute the plan. They do not rewrite LOCKED decisions.  
**Execution policy:** Repository root `/AGENTS.md` applies to all engineering/execution work.

## Current task

### T-F001 | READY — Inspect Mini-PC Hardware / Firmware

**Type:** FOUNDATION / REVERSIBLE INSPECTION  
**Source:** D-033 / D-035 / AP-000 / PRE_EXECUTION_AUDIT  
**Do:** Inspect the actual mini-PC before any install:
- exact CPU model;
- x86-64 and virtualization support;
- RAM total/usable;
- storage type, health and free capacity;
- NIC;
- BIOS/UEFI/virtualization state.

**Known owner input:** Intel Core i3 circa 2018, 8 GB RAM, 500 GB storage, no discrete GPU.

**Why:** The accepted Hypervisor → HAOS VM + Linux/OpenClaw topology is provisional. Do not install it blindly on insufficient hardware.

**Pass:**
- exact hardware facts recorded;
- virtualization viability known;
- storage health known;
- a safe resource allocation for HAOS + Linux/OpenClaw is plausible.

**If blocked/fail:** stop before installation and reconcile a simpler topology or hardware upgrade.  
**Then:** T-F002.

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

### GATE-C001 | BLOCKED UNTIL T-F008 PASS — CONFIRM DESIGN

**Source:** D-038 / ZASSIMPLE v0.3 confirmation discipline  
**Trigger:** AP-000 evidence complete through T-F008.  
**Owner action required then:** review the evidence-informed core design and explicitly complete the project confirmation command/gate.  
**Blocks:** private multi-user memory rollout, WhatsApp/Telegram production ingestion, Google writes, HA control.  
**Reminder:** surface this gate immediately when T-F008 passes; do not silently continue.

### GATE-N001 | DUE BEFORE COMPANION A/B BUILD — Final Names
Choose final names for Companion A and Companion B before those personas are instantiated/routed. This gate does not block AP-000 or Puspa-only work.

Stage sequence: AP-000 → GATE-C001 → AP-100 → AP-200 → Stabilization/Portability Gate → Stage 3 Security + Hosting/Hybrid Cloud.

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
