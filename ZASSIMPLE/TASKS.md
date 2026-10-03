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
- OpenClaw starts reliably;
- one basic Temaya/OpenClaw LLM conversation works;
- minimal workspace/bootstrap files are loaded;
- Home Assistant starts reliably;
- basic restart/recovery is demonstrated;
- runtime/config/state locations are recorded;
- no Phase 1 integration is pulled into the foundation prematurely.

**If blocked:** record the exact runtime/deployment blocker and update ACTION_PLAN/DESIGN only from evidence.  
**Then:** AP-100 M1 — Basic Temaya companion.

**Design gate note:** This task is permitted before full DESIGN confirmation because repository `/AGENTS.md` explicitly allows reversible FOUNDATION / proof work that does not silently lock unresolved architecture.


## Queue

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
