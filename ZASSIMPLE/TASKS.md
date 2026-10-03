# TEMAYA — ZASSIMPLE TASKS

**Method:** ZASSIMPLE_MY v0.3.0  
**Status:** EXECUTION QUEUE  
**Authority:** Tasks execute the plan. They do not rewrite LOCKED decisions.  
**Execution policy:** Repository root `/AGENTS.md` applies to all engineering/execution work.

## Current task

### T-F000 | READY — AP-000 Local Foundation

**Type:** FOUNDATION / REVERSIBLE IMPLEMENTATION  
**Source:** D-033 / AP-000  
**Do:** Prepare the mini PC deployment and prove OpenClaw + Home Assistant both install, start and recover to a known running state.  
**Why:** Learn the real runtimes before building integrations; avoid branching/backward redesign.  
**Pass:**
- D-035 Day-0 security baseline is verified;
- OpenClaw starts reliably;
- one basic Temaya/OpenClaw LLM conversation works;
- minimal workspace/bootstrap files are loaded;
- Home Assistant starts reliably;
- basic restart/recovery is demonstrated;
- runtime/config/state locations are recorded;
- no Phase 1 integration is pulled into the foundation prematurely.

**If blocked:** record the exact runtime/deployment blocker and update ACTION_PLAN/DESIGN only from evidence.  
**Then:** **GATE-C001 — CONFIRM DESIGN**. AP-100 integration tasks must not be promoted until the owner completes this ZASS gate.

**Design gate note:** This task is permitted before full DESIGN confirmation because repository `/AGENTS.md` explicitly allows reversible FOUNDATION / proof work that does not silently lock unresolved architecture.


## Queue

### GATE-C001 | BLOCKED UNTIL T-F000 PASS — CONFIRM DESIGN

**Source:** AC-016 / ZASSIMPLE v0.3 confirmation discipline  
**Trigger:** T-F000/AP-000 reaches PASS.  
**Owner action required then:** review the evidence-informed core design and explicitly complete the project confirmation command/gate before production-like Stage-1 exposure/writes/control.  
**Blocks:** private multi-user memory rollout, WhatsApp/Telegram production ingestion, Google writes, HA control.  
**Reminder:** surface this gate immediately when T-F000 passes; do not silently continue.



Stage sequence: AP-000 → AP-100 → AP-200 → Stabilization/Portability Gate → Stage 3 Security + Hosting/Hybrid Cloud.

Only tasks from the current eligible stage should be promoted. Later-stage tasks remain planned and must not create parallel execution branches.

Empty until design confirmation.

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
