# Temaya Research — Artificial Soul + Embodiment / Robot Vision

**Date:** 2026-10-04  
**Status:** RESEARCH / AGREED DIRECTION — NOT LOCKED  
**Authority:** Reference only. This file does not override `ZASS_Temaya.md`, LOCKED decisions, or `ZASSIMPLE/DESIGN.md`.  
**Lineage:** D-012–D-026; AC-013; AC-014.

## Purpose

Preserve useful research ideas without inflating the core Temaya design prematurely.

Two workstreams are intentionally separated:

1. **Artificial Soul / emotional continuity** — may become a small OpenClaw-compatible extension after core memory/privacy architecture is stable.
2. **Embodiment / robot vision** — future R&D for physical companions; does not block current Temaya Living Design confirmation.

---

# A. Artificial Soul research

## A1. Design direction

Artificial Soul should **not** become a second AI companion platform.

Preferred conceptual boundary:

```text
LOCKED PERSONA / SOUL / IDENTITY
          │
          ▼
       OpenClaw
 reasoning / runtime / native memory
      /                       \
     ▼                         ▼
FACTUAL CONTINUITY       EMOTIONAL CONTINUITY
OpenClaw memory          optional Emotion Engine
+self-life               PAD / trust / decay
+per-user memory         compact emotional state
      \                       /
       └──────────┬────────────┘
                  ▼
             response style
```

Semantic authority:

- **SOUL / D-xxx** = siapa persona itu.
- **Self-life** = apa yang berlaku kepada persona.
- **Human memory** = apa manusia pernah ceritakan.
- **Emotion state** = bagaimana keadaan dalaman/interaksi berubah dari masa ke masa.

Emotion state must never silently become factual memory or decision authority.

## A2. Emotion Engine — candidate OpenClaw-compatible emotional continuity layer

### Verified source findings

PioneerJeff Labs Emotion Engine describes itself as a small, inspectable emotional-continuity state layer for LLM agents.

Verified repository claims include:
- persistent PAD emotional state;
- agent-to-user trust;
- decay;
- boundary signals;
- compact emotional memories;
- LLM performs contextual judgment/final response;
- helper persists state and applies decay/logging/trust updates;
- project explicitly states it is **not a memory stack**;
- repository contains integration/skill-oriented material for agent runtimes, including OpenClaw-related support.

Useful architectural implication for Temaya:

```text
OpenClaw/self-life remembers WHAT happened.
Emotion Engine may remember HOW the interaction has been feeling.
```

### Benefits to Temaya

- adds cross-session emotional continuity without replacing OpenClaw memory;
- state is small and inspectable;
- decay supports return toward persona baseline;
- can influence tone/energy/warmth without rewriting factual memory;
- suitable for a reversible POC;
- fits D-022 native-first better than importing a complete external companion platform.

### Limits / risks

- third-party dependency, not OpenClaw core;
- must be source-reviewed/pinned before production;
- PAD/trust values are internal simulation state, not truth about a human's psychology;
- must never cross per-user privacy boundary;
- must never rewrite LOCKED persona, memory authority, safety rules, or religious/persona constraints;
- usefulness must be proven against a baseline Puspa interaction before adoption.

## A3. Per-persona state

Artificial Soul should be per-persona / per-agent, not one global emotional state.

Candidate future layout:

```text
Puspa agent
├── SOUL.md
├── IDENTITY.md
├── Hani private memory
├── self-life/
└── emotion-state.json

Companion B agent
├── SOUL.md
├── IDENTITY.md
├── Hafiz private memory
├── self-life/
└── emotion-state.json
```

Baseline emotional state must follow each persona's own LOCKED profile:
- Puspa baseline derives from D-013/D-016.
- Companion A derives from D-012/D-016/D-017.
- Companion B derives from D-014/D-019/D-020.

D-019/D-020 therefore must **not** be treated as a universal Temaya emotional baseline.

## A4. Proposed minimal POC — later, not a current blocker

```text
PUSPA ARTIFICIAL SOUL POC

1. OpenClaw Puspa agent
2. Existing SOUL / IDENTITY
3. Existing self-life prototype
4. Optional Emotion Engine integration
5. One isolated emotion-state file
6. No AICO runtime
7. No Mem0 replacement
8. No new database
```

Acceptance concept:
- baseline Puspa interaction;
- one event causes a small, bounded emotional-state change;
- new session preserves continuity;
- Puspa remains recognisably Puspa;
- factual Hani memory remains separate;
- no private transcript is copied as emotional truth;
- decay returns state toward Puspa baseline over time.

## A5. AICO — reference architecture only

AICO is useful as a **research reference**, especially for:
- modular separation of memory/emotion/agency;
- three-tier memory ideas;
- agency / goals / curiosity;
- local-first companion architecture;
- embodiment-independent companion identity.

However, AICO is a broad companion platform with its own backend/modelservice/memory/emotion/agency stack.

For Temaya, adopting AICO wholesale would duplicate OpenClaw responsibilities and conflict with D-022 unless a real OpenClaw gap is later demonstrated.

### Status

- AICO emotion concepts → **REFERENCE**
- AICO agency concepts → **LATER RESEARCH**
- AICO memory stack replacement → **PARK**
- full AICO runtime inside Temaya → **DO NOT ADOPT without a proven gap**

## A6. Memory frameworks such as Mem0 / Memary

These may be useful comparison references if OpenClaw memory later fails a required test.

Current status:
- do not replace OpenClaw memory;
- do not add a second vector/memory authority;
- revisit only with evidence of a specific gap.

## A7. Artificial Soul candidate boundary

Agreed research direction, not LOCKED:

```text
Artificial Soul =
LOCKED persona identity
+ OpenClaw factual/self-life continuity
+ optional emotional-continuity state
```

Emotion state may influence:
- tone;
- warmth;
- energy;
- concern;
- trust/boundary expression.

Emotion state may NOT:
- rewrite D-xxx LOCKED persona;
- rewrite factual self-life/human memory;
- claim inferred human psychology as fact;
- cross private-user memory boundaries;
- override safety/policy;
- become canonical identity authority.

---

# B. Embodiment / robot vision research

## B1. Scope boundary

Embodiment/vision is a future physical-companion workstream.

It is **not required** to prove:
- Living Memory;
- self-life continuity;
- Hani/Hafiz memory isolation;
- Artificial Soul POC;
- OpenClaw ↔ Home Assistant core integration.

Therefore it does not block current DESIGN confirmation.

## B2. Candidate matrix

| Candidate / idea | Use to Temaya | Main benefit | Main limitation | Research status |
|---|---|---|---|---|
| Stereo vision — 2 cameras | Depth for robot navigation/manipulation | direct geometric depth at useful near ranges | calibration, lighting/texture, baseline trade-offs | FUTURE R&D |
| OAK-D family / DepthAI | integrated stereo/depth/vision processing | compact robotics vision candidate; some processing near sensor | ecosystem/hardware choice must be tested | STRONG CANDIDATE |
| OAK-D SR | short-range depth | attractive for tabletop / arm / gripper work | not intended as long-range navigation sensor | STRONG CANDIDATE — ARM |
| RealSense D455-class depth camera | general robotics RGB-D | mature depth-camera path, IMU/depth ecosystem | host compute/integration overhead | STRONG CANDIDATE |
| DIY dual global-shutter cameras | custom stereo research | maximum control / educational value | sync + calibration + integration burden | RESEARCH |
| ROS stereo processing | disparity / point cloud pipeline | avoids reinventing standard stereo pipeline | still requires correct calibration/sync | USE IF DIY |
| MoveIt hand-eye calibration | eye-in-hand / eye-to-hand calibration | relevant to future 6-DoF arm vision | only useful when arm/camera stack exists | LATER |
| Monocular depth models | secondary/fallback depth estimation | works from one RGB stream | learned estimate is not equivalent to deterministic geometry | SECONDARY |
| Motion parallax / active vision | moving camera creates changing baseline | interesting for camera-on-arm exploration | motion/object dynamics/calibration complexity | RESEARCH |
| H2O / OmniH2O | humanoid teleoperation research | useful reference for RGB-based teleop/data collection | not a depth/navigation solution for Temaya | REFERENCE |
| OpenVLA | vision-language-action research | open embodied model research / potential future arm learning | embodiment adaptation + compute/data burden | LATER R&D |
| NVIDIA GR00T + LeRobot | humanoid/VLA ecosystem | strong future robotics training reference | NVIDIA/humanoid complexity; overkill now | FAR LATER |
| Isaac Lab | simulation / robot learning | sim-first experiments and teleoperation research | heavy simulation/GPU/tooling scope | LATER |
| Humanoid-Gym | locomotion RL reference | sim-to-real locomotion concepts | narrow humanoid locomotion focus | REFERENCE |
| RealMirror | VLA/sim research | interesting emerging open research | research maturity / claims need independent validation | WATCH |
| Figure sim-RL examples | industry reference | supports sim-first / domain-randomization principle | proprietary system, not reusable Temaya stack | INSPIRATION |
| Gemini Robotics family | embodied AI reference | demonstrates direction of whole-body/multi-embodiment AI | closed/early-access dependency unsuitable as core | REFERENCE |

## B3. Practical future camera paths

Candidate future evaluation:

```text
A — SIMPLE INTEGRATED
OAK-D / OAK-D Pro / OAK-D SR
→ ready stereo depth
→ optional onboard vision processing

B — GENERAL ROBOTICS
RealSense-class RGB-D
→ RGB + depth + IMU
→ ROS / MoveIt ecosystem

C — DIY / RESEARCH
2x synchronized global-shutter cameras
→ calibration
→ stereo pipeline
→ optional learned mono-depth fusion
```

No camera hardware is selected or locked by this research note.

## B4. Sensor-function principle

Useful future design principle:

- camera/stereo → visual geometry/depth;
- encoder → proprioception / joint pose;
- tactile/force sensor → contact;
- optional LiDAR/radar → specialised ranging where justified;
- avoid adding sensors merely because they exist.

## B5. Fast-loop vs slow-loop principle

Future physical robot architecture should separate:
- **fast deterministic control loop** — motor safety, servo control, contact response;
- **slow reasoning loop** — OpenClaw/persona/planning/semantic reasoning.

This is consistent with D-010 modularity: high-level AI reasoning should not be a hard dependency for basic physical safety/control.

---

# C. Research decisions intentionally NOT made

This research does NOT:
- select Emotion Engine as a production dependency;
- change D-021–D-026;
- create a new memory engine;
- adopt AICO runtime;
- adopt Mem0/Memary;
- choose OAK-D vs RealSense;
- choose OpenVLA/GR00T/Gemini Robotics;
- add humanoid robotics to current Phase 1;
- change current DESIGN confirmation blockers.

---

# D. Proposed future experiments

## EXP-AS-001 — Artificial Soul emotional continuity POC

Run only after the core self-life/per-user memory vertical slice is stable enough to compare behaviour.

Goal:
- determine whether an optional emotion-state layer improves continuity without corrupting persona/memory boundaries.

## EXP-EMB-001 — Robot vision benchmark

Run only when a physical robot/arm embodiment enters active scope.

Compare:
- integrated stereo (OAK-D family);
- general RGB-D (RealSense-class);
- DIY stereo only if custom research value justifies the extra burden.

---

# E. Source / provenance notes

### Verified / primary references consulted

- PioneerJeff Labs Emotion Engine repository: https://github.com/pioneerjeff-labs/emotion-engine
- Emotion Engine integration documentation: https://github.com/pioneerjeff-labs/emotion-engine/blob/main/docs/INTEGRATION.md
- AICO architecture overview/article: https://boeni.industries/blog/aico-architecture-for-a-local-ai-companion
- AICO agency overview: https://boeni.industries/blog/agency-how-aico-thinks-and-acts-for-itself
- AICO project overview: https://boeni.industries/aico

### Additional research candidates supplied / previously reviewed

- Luxonis OAK-D / OAK-D Pro / OAK-D SR documentation
- RealSense D455 family documentation
- ROS stereo_image_proc
- MoveIt hand-eye calibration
- Depth Anything V2 / Metric3D
- H2O / OmniH2O
- OpenVLA
- NVIDIA GR00T / LeRobot
- Isaac Lab
- Humanoid-Gym
- RealMirror
- Figure AI RL walking
- Gemini Robotics

Exact performance/specification claims must be re-verified from current primary documentation before procurement or implementation.

---

## Current status

**Artificial Soul:** AC direction only — no LOCK.  
**Embodiment/Robot Vision:** AC future R&D direction only — no LOCK.  
**Core Temaya Design:** unchanged / PENDING CONFIRMATION.
