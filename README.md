# Temaya

Temaya is the family-assistant project integrating persona continuity, private per-user memory, Dzuddiyn Library, OpenClaw, Home Assistant, voice interfaces, and related services.

## Repository entry points

Read these in order before substantial implementation:

1. `AGENTS.md` — repository engineering/execution policy.
2. `ZASS_Temaya.md` — authoritative decision lineage, including D-xxx LOCKED decisions.
3. `ZASSIMPLE/DESIGN.md` — current design/architecture subtype; currently subject to its recorded confirmation status.
4. `ZASSIMPLE/ACTION_PLAN.md` — implementation planning.
5. `ZASSIMPLE/TASKS.md` — execution queue.

## Important AGENTS.md distinction

The repository root `/AGENTS.md` governs how engineering agents work on this project.

Any `AGENTS.md` inside an OpenClaw workspace is runtime/persona configuration. It is a different artifact and must not overwrite or be confused with the repository execution policy.

## Current project discipline

- Preserve D-xxx LOCKED decisions.
- Keep Temaya self-life separate from private human memory.
- Prefer OpenClaw-native capability before custom subsystems where D-022 applies.
- Verify important writes and live behavior independently.
- Keep planning/design/task status truthful.
- Start small with reversible foundations or proofs where architecture allows, then feed findings back into ACTION_PLAN ↔ DESIGN.
