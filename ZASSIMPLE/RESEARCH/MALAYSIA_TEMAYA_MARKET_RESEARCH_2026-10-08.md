# Malaysia Temaya Market Research — 2026-10-08

**Status:** RESEARCH SNAPSHOT — FACTS + ANALYSIS + FORECAST, NOT A LOCKED DECISION  
**Date:** 2026-10-08  
**Purpose:** Consolidate the Malaysia-market, ageing/care, personal-agent, agent-to-agent and future Temaya commercialization research discussed on 2026-10-08.  
**Authority:** Research evidence only. It does not override `D-xxx | LOCKED` decisions, current `DESIGN.md`, `ACTION_PLAN.md` or `TASKS.md`.

---

## 0. Evidence discipline

Every important statement below is classified as one of:

- **FACT** — directly supported by a cited source.
- **VENDOR CLAIM** — stated by a product/vendor on its own site; not independently verified.
- **OWNER ASPIRATION** — future direction explicitly stated by the project owner.
- **ANALYSIS / INFERENCE** — interpretation drawn from facts; not itself a measured fact.
- **FORECAST** — forward-looking estimate; uncertain and non-authoritative.

Research cut-off: **2026-10-08**.

Where a source is a vendor page, this document records what the vendor claims or offers; it does not independently certify performance, reliability, security or customer adoption.

---

# 1. Executive findings

## 1.1 Malaysia already has adjacent personal-AI products, but the market is fragmented

**FACT / VENDOR CLAIM:** Current Malaysia-accessible products cover separate slices of the problem:

- **Proxi** — WhatsApp-based AI personal operator with email/calendar/follow-ups; paid tiers RM199/month and RM499/month; its free DIY route is based on OpenClaw and is self-hosted.  
  Source: https://www.proxi.my/pricing
- **Jadwal** — WhatsApp-native scheduling assistant with Google Calendar, guest coordination, venue recommendations and flight search; listed pricing RM49 / RM149 / RM399 per month.  
  Source: https://www.asisten.bot/
- **AI Bradaa** — Malaysia-focused AI companion with persistent conversation memory, a bond/relationship progression system, local-language/cultural positioning and multiple AI capabilities.  
  Sources: https://www.aibradaa.com/ and https://www.aibradaa.com/features
- **Gemini Personal Intelligence** — available in Malaysia and able to connect Gmail, Photos, YouTube and Search, subject to user choice.  
  Source: https://blog.google/intl/en-my/products/explore-get-answers/google-launches-personal-intelligence-in-the-gemini-app-in-malaysia/
- **Grab Shopping Agent** — already available in Malaysia for grocery-list assistance; Grab AI Assistant was announced for Malaysia rollout by end-2026.  
  Sources: https://www.grab.com/inside-grab/stories/grabx-ai-shopping-agent-grocery-list/ and https://www.grab.com/my/ms/press/others/grab-unveils-13-ai-powered-experiences-at-grabx-2026-as-southeast-asias-intelligent-everyday-guide/
- **Ryt AI** — conversational banking interface supporting transfer/payment flows, transaction lookup and JomPAY-assisted bill payments with user confirmation.  
  Source: https://www.rytbank.my/ryt-ai

**ANALYSIS:** No product reviewed in this snapshot clearly combines all of Temaya's intended future dimensions at once: private family identity/memory separation, persistent companion/persona continuity, WhatsApp, ambient smart-speaker voice, local/offline household control, Home Assistant, durable family knowledge, and a future scoped external liaison agent.

This is a **gap observation**, not proof of market demand.

---

## 1.2 The strongest near-term market pattern is "AI assists, human approves"

**FACT:** Adyen's Malaysia 2026 research reported:
- 74% of surveyed Malaysian consumers use AI while shopping;
- 52% are uncomfortable allowing AI to complete purchases on their behalf;
- 47% of surveyed retailers plan to invest in AI-driven or agentic-commerce solutions in 2026;
- survey sample: 1,031 Malaysian consumers and 314 senior retail employees.

Source: https://www.adyen.com/press-and-media/adyen-index-my-2026

**ANALYSIS:** This supports a near-term product pattern:

```text
AI discovers / narrows / prepares
          ↓
human selects / confirms
          ↓
AI executes
          ↓
result is verified
```

It does **not** support assuming Malaysian users broadly want fully autonomous purchasing.

---

## 1.3 Agent-to-agent commerce is no longer only speculative infrastructure

**FACT:** Mastercard announced its first authenticated live agentic transactions in Malaysia on **2026-03-04**, in a controlled pilot with CIMB and RHB using Mastercard Agent Pay. The inaugural case had an AI agent book a ride from KLIA to KL Sentral through hoppa.

Source: https://www.mastercard.com/news/ap/en/newsroom/press-releases/en/2026/mastercard-conducts-first-live-agentic-transaction-in-malaysia-with-cimb-and-rhb-pilot/

**FACT:** Google introduced:
- **A2A** as an open protocol for agent-to-agent collaboration;
- **AP2** as an open agent-payments protocol;
- **UCP** as an open commerce protocol intended to let agents, businesses and payment providers interoperate across the shopping journey.

Sources:
- https://developers.googleblog.com/a2a-a-new-era-of-agent-interoperability/
- https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol
- https://blog.google/products/ads-commerce/agentic-commerce-ai-tools-protocol-retailers-platforms/

**FACT:** Google stated in May 2026 that UCP expansion was planned beyond retail into verticals including **hotel booking and local food delivery**.

Source: https://blog.google/products-and-platforms/products/shopping/google-shopping-cart/

**ANALYSIS:** Temaya does not need every physical merchant in Malaysia to operate its own AI agent. Interoperability with a smaller set of high-coverage digital platforms may be enough to unlock large practical value.

---

# 2. Malaysia personal-agent / assistant landscape

## 2.1 Proxi

**Classification:** adjacent/direct competitor for productivity/personal-operator use.

### Verified vendor facts

As of this research date, Proxi lists:

| Tier | Price | Selected capabilities |
|---|---:|---|
| Free | RM0 | OpenClaw, self-hosted, own keys |
| Proxi | RM199/month + RM500 setup | WhatsApp, email, calendar, follow-ups, reminders, research |
| Proxi Max | RM499/month + RM2,000 setup | custom workflows, API/database integration, orchestration, process automation, Stripe/payment integration |

Source: https://www.proxi.my/pricing

Its terms describe the service as an AI-powered personal assistant accessible through WhatsApp, including task management, scheduling, research, drafting and administration.

Source: https://www.proxi.my/terms

### Comparison with Temaya

**ANALYSIS:**
- Proxi currently validates the **WhatsApp personal operator** model locally.
- It appears positioned around productivity/admin/workflow value.
- Temaya's intended differentiation is not to compete head-on on premium personal productivity.
- Temaya's future differentiation is intended to centre on private family continuity, care/assistive use, household context, local/offline operation and Home Assistant integration.

---

## 2.2 Jadwal

**Classification:** focused adjacent competitor / substitute for scheduling.

### Verified vendor facts

Jadwal describes itself as a WhatsApp AI scheduling assistant available in Malaysia. It supports:
- Google Calendar sync;
- group scheduling;
- guest gatekeeper;
- venue recommendations;
- flight search;
- English and Bahasa / mixed-language input.

Listed pricing:
- Starter RM49/month;
- Pro RM149/month;
- Business RM399/month.

Source: https://www.asisten.bot/

### Comparison with Temaya

**ANALYSIS:** Jadwal is strong evidence that familiar-channel UX can remove friction. Its scope is much narrower than the intended Temaya family/care system.

---

## 2.3 AI Bradaa

**Classification:** adjacent companion competitor.

### Verified vendor facts / claims

AI Bradaa markets itself as a Malaysia-focused AI companion with:
- persistent conversation memory;
- six bond levels: Stranger → Kenalan → Kawan → Sahabat → Nakama → Soulmate;
- Malaysian-language/cultural positioning;
- multiple models and agentic workflows.

Sources:
- https://www.aibradaa.com/
- https://www.aibradaa.com/features

### Important correction: "Soul Component"

**FACT / VENDOR CLAIM:** AI Bradaa's feature page describes its **Soul Component** as a living ferrofluid animation representing states such as idle, listening, thinking, processing, ready and speaking.

Source: https://www.aibradaa.com/features

Its roadmap says the Soul Component animation and some other capabilities are in development.

Source: https://www.aibradaa.com/roadmap

**ANALYSIS:** The name "Soul Component" should **not** be treated as evidence that AI Bradaa implements an Artificial Soul equivalent to Temaya's self-memory / self-life / continuity concept. Persistent memory and the Bond System are separate product features.

This corrects the earlier loose comparison.

---

## 2.4 Gemini Personal Intelligence

**Classification:** major-platform substitute / strategic threat.

**FACT:** Google launched Personal Intelligence in the Gemini app in Malaysia on 2026-04-14. Users may connect Gmail, Google Photos, YouTube and Search, and Google describes the feature as reasoning across those sources and retrieving specific personal details.

Source: https://blog.google/intl/en-my/products/explore-get-answers/google-launches-personal-intelligence-in-the-gemini-app-in-malaysia/

**ANALYSIS:** Google can commoditise large parts of personal-context retrieval because it already owns major user surfaces. Temaya therefore should not rely on generic "personalisation" alone as a durable differentiator.

Potential Temaya differentiation remains:
- family-level authority and isolation;
- local/private ownership;
- household/home context;
- cross-provider portability;
- assistive/care deployment;
- explicit provenance/authority boundaries.

---

## 2.5 Grab

**Classification:** targeted-action platform / likely external service counterparty.

**FACT:** Grab Shopping Agent is available in Malaysia. It accepts typed, spoken or photographed shopping lists, finds matching items and prepares a cart for user review.

Source: https://www.grab.com/inside-grab/stories/grabx-ai-shopping-agent-grocery-list/

**FACT:** Grab announced in April 2026 that Grab AI Assistant would roll out to Malaysia by the end of 2026. Grab describes it as a personal AI concierge intended to reduce daily mental load; announced use cases include restaurant recommendations/bookings and food-delivery assistance.

Source: https://www.grab.com/my/ms/press/others/grab-unveils-13-ai-powered-experiences-at-grabx-2026-as-southeast-asias-intelligent-everyday-guide/

**ANALYSIS:** Grab supports the owner thesis that large digital service platforms can become targeted execution agents. Temaya does not need to reproduce Grab's merchant network.

---

## 2.6 Ryt AI

**Classification:** targeted domain agent / banking execution proof.

**FACT:** Ryt AI supports natural-language banking tasks including transfer initiation, transaction lookup, bill/photo parsing and JomPAY payment preparation. Ryt's page states that user confirmation is required for some flows such as moving funds.

Source: https://www.rytbank.my/ryt-ai

**ANALYSIS:** Ryt AI is a useful Malaysia example of the "domain agent + human confirmation" model rather than a universal personal agent.

---

## 2.7 Tab — global reference, not Malaysia competitor

**Classification:** external reference / trust-oriented personal agent.

**FACT:** TechCrunch reported on 2026-10-07 that Tab emerged from stealth at a **US$300 million valuation**; exact funding was not disclosed. The founders named were Brennan Erbz, Stafford Schlitt and Ammar Amdani.

**FACT:** According to the same report, Tab accepts requests through iMessage or WhatsApp and is designed to handle tasks such as groceries, gifts, bills, bookings and calls. The company frames trust as a core product principle.

Source: https://techcrunch.com/2026/10/07/another-personal-ai-assistant-has-launched-meet-tab-which-emerged-from-stealth-with-a-300m-valuation/

**ANALYSIS:** Tab validates the global "trusted personal operator" thesis, but Temaya should not simply replicate its booking/purchase stack.

---

# 3. Malaysia AI-commerce trust and readiness

## 3.1 Consumer behaviour

**FACT:** Adyen's 2026 Malaysia survey:
- 74% use AI assistants during shopping;
- 52% are uncomfortable with AI completing purchases for them;
- 26% have abandoned purchases due to security/trust concerns;
- 59% say payment errors negatively affect their view of a business.

Source: https://www.adyen.com/press-and-media/adyen-index-my-2026

**ANALYSIS:** Trust, reversibility, transparent confirmation and verified execution are likely to matter as much as raw AI capability.

This aligns with existing Temaya principles around Human Queue, deterministic authorization and independently verified writes.

---

## 3.2 Retail-side readiness

**FACT:** In the same Adyen study:
- 85% of surveyed retailers said they were familiar with agentic commerce;
- 47% planned to invest in AI-driven or agentic-commerce solutions in 2026;
- 39% cited data privacy, security and compliance as a barrier;
- 41% cited customer relationship / brand-control concerns.

Source: https://www.adyen.com/press-and-media/adyen-index-my-2026

**ANALYSIS:** Merchant-side agent adoption can grow while still remaining constrained by trust and integration complexity.

---

# 4. Malaysia ageing — current size and official projections

## 4.1 Current 2026 population

**FACT:** DOSM estimates for 2026:
- total population: 34.4 million;
- age 60+: **4.2 million (12.3%)**;
- age 65+: **2.9 million (8.4%)**;
- old-age dependency ratio: **11.9 people aged 65+ per 100 people aged 15–64**, up from 11.4 in 2025.

Sources:
- https://www.dosm.gov.my/site/downloadrelease?admin_view=&id=current-population-estimates-2026&lang=English
- https://www.dosm.gov.my/uploads/release-content/file_20260903105212.pdf

---

## 4.2 Official long-term projection

**FACT:** DOSM Population Projections 2020–2060:

| Year | Population 60+ | Share | Population 65+ | Share |
|---|---:|---:|---:|---:|
| 2020 | 3.3m | 10.3% | 2.2m | 6.8% |
| 2030 | 4.9m | 13.3% | 3.4m | 9.3% |
| 2040 | 6.5m | 16.5% | 4.6m | 11.6% |
| 2050 | 8.8m | 21.0% | 6.3m | 15.1% |
| 2060 | 10.3m | 24.2% | 7.8m | 18.3% |

Source: https://www.dosm.gov.my/portal-main/release-document-log?release_document_id=15087  
Supporting publication: https://storage.dosm.gov.my/demography/population_projection_2060.pdf

**FACT:** DOSM states that Malaysia is expected to become an **aged society** by 2048 using the UN threshold of 14% of population aged 65+.

Source: https://storage.dosm.gov.my/demography/population_projection_2060.pdf

---

## 4.3 Longevity after age 60

**FACT:** DOSM Abridged Life Tables 2026:
- a male reaching age 60 in 2026 is expected to live another **18.9 years**;
- a female reaching age 60 is expected to live another **21.7 years**.

Source: https://www.dosm.gov.my/portal-main/release-content/abridged-life-tables-malaysia-2026

**ANALYSIS:** Care/support relationships can therefore last many years; this strengthens the relevance of continuity, maintainability and long-lived private memory.

---

# 5. Older-person health, social support and caregiver burden

## 5.1 NHMS 2025 — strongest current evidence

**FACT:** NHMS 2025 Older Persons Health surveyed adults aged 60+ and informal caregivers. Its factsheet reports:

| Indicator | Prevalence |
|---|---:|
| Ageing well | 14.7% |
| Poor social support | **33.1%** |
| Dementia | **9.8%** |
| Depression | **8.0%** |
| Severe depression | 2.2% |
| IADL limitation | **27.3%** |
| ADL limitation | **10.0%** |
| Sarcopenia | 45.3% |
| Pre-frail | 60.0% |
| Frailty | 10.7% |
| Burden among primary informal caregivers | **32.2%** |

Source: https://iku.nih.gov.my/images/nhms-2025/factsheet_eng.pdf  
NHMS portal: https://iku.nih.gov.my/nhms2025

**ANALYSIS:** These data provide direct evidence that social support, cognitive impairment, daily-living assistance and caregiver burden are material problems among Malaysia's older population.

They do **not** prove that AI is the correct solution or that older people will pay for it.

---

## 5.2 Broader functional difficulty

**FACT:** NHMS 2023 reported:
- overall disability prevalence among age 60+ at **26.0%**;
- overall difficulty prevalence among age 60+ at **48.9%**.

Source: https://iku.nih.gov.my/images/nhms2023/report-nhms-2023.pdf

**ANALYSIS:** Accessibility and low-friction interaction are not niche design details for an elderly-focused product.

---

# 6. Mental-health evidence — use carefully

## 6.1 National depression trend

**FACT:** NHMS 2023 found adult depression prevalence of **4.6%**, about 1 million people aged 16+, compared with **2.3% in 2019**.

Source: https://iku.nih.gov.my/images/nhms2023/key-findings-nhms-2023.pdf

Age-group prevalences shown in the key findings:
- 16–19: 7.9%
- 20–29: 7.6%
- 30–39: 4.1%
- 40–49: 3.1%
- 50–59: 2.4%
- 60+: 3.1%

**FACT:** NHMS 2025, which specifically studied older persons, reports depression prevalence of **8.0%** among its older-person sample using its 2025 methodology.

Source: https://iku.nih.gov.my/images/nhms-2025/factsheet_eng.pdf

### Interpretation boundary

**ANALYSIS:** The evidence supports mental-health burden as an important social problem, but it does **not** support the simplistic claim that mental illness necessarily rises because the population ages. Different surveys, age groups and methodologies must not be conflated.

Any Temaya mental-health use must remain assistive and supportive, not diagnostic or a replacement for professional/human care.

---

# 7. Malaysia care-policy direction

## 7.1 Malaysia Care Strategic Framework and Action Plan 2026–2030

**FACT:** KPWKM's framework has five strategic thrusts, including **Research, Technology and Data**. Listed strategies include:
- promoting social innovation in the care economy;
- promoting technology and digitalisation in care services;
- strengthening reporting/analytical systems;
- data-driven monitoring/accountability;
- strategic collaboration.

It explicitly lists ministries, departments, agencies, higher-learning institutions, corporate/private sector, NGOs, industry players and community as strategic partners.

Source: https://www.kpwkm.gov.my/uploads/content-downloads/file_20251114162252.pdf  
KPWKM plans index: https://www.kpwkm.gov.my/portal-main/documents?frontendpage=documents&page=1&params=&per-page=12&type=pelan-kpwkm

**ANALYSIS:** This gives policy alignment for future care-technology pilots and partnership exploration. It does not imply government endorsement or funding for Temaya.

---

## 7.2 Thirteenth Malaysia Plan / National Ageing Blueprint

**FACT:** RMK13 states that the **National Ageing Blueprint 2025–2045** was approved in 2025 and identifies preparation for an aged nation as a priority, including establishment of a sustainable long-term-care ecosystem.

Source: https://rmk13.ekonomi.gov.my/wp-content/uploads/2025/09/120925-Main-Document-e-Book.pdf

RMK13 FAQ also lists strengthening the health and long-term-care system for older people among the objectives.

Source: https://rmk13.ekonomi.gov.my/rmk13-soalan-lazim/

**ANALYSIS:** Future B2G/B2B2C exploration is consistent with national policy direction, but any actual public-sector procurement path remains unknown.

---

# 8. Temaya future positioning — owner aspiration, not market fact

The following points are **OWNER ASPIRATION** and are intentionally separated from research facts.

## 8.1 Help-first / problem-first

Temaya commercialisation should not start by asking which demographic is richest or which segment maximises TAM.

It should ask:
- who has a recurring problem;
- whether Temaya can reduce it reliably;
- whether it can do so privately, safely and with dignity.

This adapts Kerani_Core_SuperBasic's V-Road principle:
**Value → Verbal → Volume → Viral → Vary → Venture → Versatile.**

---

## 8.2 Deliberate market boundary

**OWNER ASPIRATION:** Temaya should not intentionally chase the primary affluent personal-productivity / premium-companion market already being served by products such as Proxi, AI Bradaa and Jadwal.

This is a positioning choice, not a claim that those companies only serve wealthy users or that they will never expand into care.

Temaya's preferred future problem space:
- ageing and care;
- family continuity;
- accessibility;
- household assistance;
- people living alone;
- people with limited family support;
- persistent companionship;
- local/private assistive infrastructure;
- underserved high-friction human problems.

---

## 8.3 Future payer / deployment channels

**OWNER ASPIRATION:**

### B2C
A child/family member pays for Temaya for a parent or dependent family member.

### B2B2C
A care centre purchases local Temaya/Home Assistant infrastructure; each resident receives a separately isolated personal Temaya.

### B2G
Government/state/agency funds deployment to selected populations/programmes.

### B2NGO / waqaf / CSR
NGO, waqaf, foundation or CSR sponsor pays for access for older, low-income, isolated or underserved users.

**ANALYSIS:** These payer models reduce dependence on the end user personally affording a premium monthly subscription.

No willingness-to-pay data has yet been collected for any of these models.

---

# 9. Future care-centre architecture direction — owner hypothesis

**OWNER ASPIRATION / DESIGN HYPOTHESIS:**

```text
CARE CENTRE
│
├── local/private Temaya infrastructure
├── Home Assistant / building automation
├── staff escalation layer
│
├── Resident A → private Temaya
├── Resident B → private Temaya
└── Resident C → private Temaya
```

Candidate value:
- voice-accessible room comfort controls;
- reminders and routine assistance;
- staff-call/escalation;
- companionship;
- local alarms;
- controlled family communication;
- reduced repetitive coordination burden for staff.

Important boundary:
- Temaya is not a replacement for carers, clinicians, emergency services or human companionship;
- high-impact clinical/safety decisions require proper human/institutional authority;
- future regulatory, clinical and safeguarding requirements remain OPEN.

**OWNER ASPIRATION:** sensitive resident context and core local functions should favour **offline/private-first** operation where technically feasible.

---

# 10. Future private-principal-agent / Office Agent direction

## 10.1 Owner thesis

**OWNER ASPIRATION:** Temaya's valuable long-term asset is not a bespoke connector to every merchant. It is the trusted private personal/family context.

Future model:

```text
PRIVATE TEMAYA
identity + memory + family context + preferences + permissions
        │
        │ scoped mandate / minimum disclosure
        ▼
OFFICE / LIAISON AGENT
        │
        ▼
service / merchant / platform agent
        │
        ▼
proposal / transaction / result
        │
        ▼
Temaya verifies + records
```

The Office/Liaison Agent should not have unrestricted access to raw private memory.

---

## 10.2 Why this direction is technically plausible

**FACT:** A2A exists as an open interoperability protocol for agents from different vendors/frameworks.

Source: https://developers.googleblog.com/a2a-a-new-era-of-agent-interoperability/

**FACT:** UCP exists as an open agentic-commerce protocol and is designed to interoperate with A2A, AP2 and MCP.

Source: https://blog.google/products/ads-commerce/agentic-commerce-ai-tools-protocol-retailers-platforms/

**FACT:** AP2 defines payment mandates for human-present and delegated-agent transactions.

Source: https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol

**ANALYSIS:** These standards make a future "private agent delegates to external agent" architecture more plausible. They do not guarantee broad Malaysian merchant adoption.

---

# 11. Addressable-population arithmetic — not a revenue forecast

Using DOSM's official 60+ projections:

| Year | 60+ population | 1.0m users would equal | 5% adoption would equal |
|---|---:|---:|---:|
| 2030 | 4.9m | 20.4% | 245k |
| 2040 | 6.5m | 15.4% | 325k |
| 2050 | 8.8m | 11.4% | 440k |
| 2060 | 10.3m | 9.7% | 515k |

Calculation: simple share of DOSM projected 60+ population.

**ANALYSIS:** A 1-million-user elderly deployment would be a large penetration challenge, but it is not equivalent to the whole elderly market.

This table is **not** a TAM, revenue projection or evidence of willingness to pay.

Potential payer can differ from user:
- user;
- family;
- care institution;
- government;
- NGO/waqaf/CSR sponsor.

---

# 12. Forecast — explicitly uncertain

These are **FORECASTS**, not facts.

## Horizon A — 2026–2028: targeted agents expand first

**Confidence: HIGH**

Expected pattern:
- shopping agent;
- food/service concierge;
- banking/payment agent;
- scheduling agent;
- business/customer-service agent.

Rationale:
- Grab Shopping Agent already exists in Malaysia;
- Ryt AI already executes banking workflows;
- Mastercard Malaysia has completed a controlled live agentic-transaction pilot;
- Malaysian retailers report active agentic-commerce investment plans.

Likely UX:
**AI prepares → user approves → AI executes.**

---

## Horizon B — 2028–2031: major digital platforms become sufficient agent front doors

**Confidence: MEDIUM-HIGH**

Forecast:
Malaysia does not need every individual shop to operate an AI agent. If large platforms covering food delivery, mobility, travel, finance, commerce and service expose agent-ready interfaces, a personal agent can perform a meaningful share of daily digital errands.

Uncertainty:
- platform API openness;
- commercial incentives;
- authentication;
- regulation;
- payment liability;
- agent identity standards.

---

## Horizon C — 2028–2032: private personal AI becomes more valuable as generic model capability commoditises

**Confidence: MEDIUM-HIGH**

Forecast:
As general AI reasoning becomes widely available, differentiation shifts toward:
- trusted memory;
- context;
- permission;
- provenance;
- continuity;
- privacy;
- action reliability.

Counter-risk:
large platform vendors may bundle enough personal context and execution that independent personal agents struggle to differentiate.

---

## Horizon D — 2030–2035: family/care AI becomes a recognisable product category

**Confidence: MEDIUM**

Forecast:
Ageing demographics, caregiver burden, home automation, conversational interfaces and lower AI cost may support a family/care AI category.

This is **not** evidence that Temaya will succeed.

Key gating conditions:
- reliability;
- easy onboarding;
- privacy;
- clear human-authority boundaries;
- institutional acceptance;
- support economics;
- safeguarding;
- regulatory compliance.

---

# 13. Temaya development implication

## Current priority

```text
FAMILY-ONLY
   ↓
RELIABLE
   ↓
TRUSTED / PRIVATE
   ↓
EASY ONBOARDING
   ↓
REPEATED REAL VALUE
   ↓
EXTERNAL HOUSEHOLD TEST
   ↓
CARE / PARTNER PILOT
   ↓
SCALE ONLY AFTER EVIDENCE
```

### Do now
- make the family deployment genuinely useful;
- prove private per-human boundaries;
- prove reliable WhatsApp and smart-speaker interaction;
- prove Home Assistant integration safely;
- prove memory/knowledge continuity;
- make failures truthful and recoverable.

### Do not do now
- build a bespoke connector for every merchant;
- optimise for a million-user deployment;
- chase Proxi/Jadwal/AI-Bradaa positioning;
- claim elderly/care product-market fit before field evidence;
- claim clinical benefit;
- assume public-sector funding;
- assume all Malaysian users want autonomous AI decisions.

---

# 14. Research conclusions

## FACT-backed conclusions

1. Malaysia is ageing rapidly, with 60+ projected from 4.9m in 2030 to 10.3m in 2060.
2. Current older-person health evidence shows material social-support, cognitive, functional and caregiver-burden problems.
3. Malaysia's national care policy explicitly includes technology/digitalisation and long-term-care development.
4. Malaysia already has consumer/productivity AI assistants and targeted execution agents.
5. Agentic payments have already been demonstrated in a controlled Malaysia pilot.
6. Malaysian AI-shopping adoption is high, but autonomous-purchase trust remains limited.
7. Open agent-to-agent / commerce / payments protocols now exist.

## Analysis conclusions

1. Temaya should not compete on generic AI capability.
2. Private context, family authority, local/offline ownership and reliable action are more defensible differentiators.
3. Targeted platform agents may remove the need for Temaya to build many merchant-specific integrations.
4. The care/ageing opportunity is structurally plausible, but product-market fit is **unproven**.
5. A multi-payer model is strategically plausible, but willingness-to-pay must be tested.
6. Easy onboarding may become a more important commercial gate than model quality.

## Owner philosophy carried forward

> **Help first. Solve real friction. Value first; market and scale follow evidence.**

---

# 15. Source ledger

Primary / official:
1. DOSM — Population Projections 2020–2060  
   https://www.dosm.gov.my/portal-main/release-document-log?release_document_id=15087
2. DOSM — Population projection publication  
   https://storage.dosm.gov.my/demography/population_projection_2060.pdf
3. DOSM — Current Population Estimates 2026  
   https://www.dosm.gov.my/site/downloadrelease?admin_view=&id=current-population-estimates-2026&lang=English
4. DOSM — Abridged Life Tables Malaysia 2026  
   https://www.dosm.gov.my/portal-main/release-content/abridged-life-tables-malaysia-2026
5. Institute for Public Health — NHMS 2025 Older Persons factsheet  
   https://iku.nih.gov.my/images/nhms-2025/factsheet_eng.pdf
6. Institute for Public Health — NHMS 2023 key findings  
   https://iku.nih.gov.my/images/nhms2023/key-findings-nhms-2023.pdf
7. Institute for Public Health — NHMS 2023 technical report  
   https://iku.nih.gov.my/images/nhms2023/report-nhms-2023.pdf
8. KPWKM — Malaysia Care Strategic Framework and Action Plan 2026–2030  
   https://www.kpwkm.gov.my/uploads/content-downloads/file_20251114162252.pdf
9. RMK13 — main document  
   https://rmk13.ekonomi.gov.my/wp-content/uploads/2025/09/120925-Main-Document-e-Book.pdf
10. RMK13 — ageing FAQ  
    https://rmk13.ekonomi.gov.my/rmk13-soalan-lazim/
11. Mastercard — Malaysia Agent Pay pilot with CIMB/RHB  
    https://www.mastercard.com/news/ap/en/newsroom/press-releases/en/2026/mastercard-conducts-first-live-agentic-transaction-in-malaysia-with-cimb-and-rhb-pilot/
12. Google — A2A  
    https://developers.googleblog.com/a2a-a-new-era-of-agent-interoperability/
13. Google — AP2  
    https://cloud.google.com/blog/products/ai-machine-learning/announcing-agents-to-payments-ap2-protocol
14. Google — UCP  
    https://blog.google/products/ads-commerce/agentic-commerce-ai-tools-protocol-retailers-platforms/
15. Google — UCP / Universal Cart expansion  
    https://blog.google/products-and-platforms/products/shopping/google-shopping-cart/
16. Google Malaysia — Gemini Personal Intelligence  
    https://blog.google/intl/en-my/products/explore-get-answers/google-launches-personal-intelligence-in-the-gemini-app-in-malaysia/
17. Grab — Shopping Agent  
    https://www.grab.com/inside-grab/stories/grabx-ai-shopping-agent-grocery-list/
18. Grab Malaysia — GrabX 2026 product availability  
    https://www.grab.com/my/ms/press/others/grab-unveils-13-ai-powered-experiences-at-grabx-2026-as-southeast-asias-intelligent-everyday-guide/
19. Ryt Bank — Ryt AI  
    https://www.rytbank.my/ryt-ai

Vendor / market sources:
20. Proxi pricing  
    https://www.proxi.my/pricing
21. Proxi terms  
    https://www.proxi.my/terms
22. Jadwal  
    https://www.asisten.bot/
23. AI Bradaa home  
    https://www.aibradaa.com/
24. AI Bradaa features  
    https://www.aibradaa.com/features
25. AI Bradaa roadmap  
    https://www.aibradaa.com/roadmap
26. Adyen Index Malaysia 2026  
    https://www.adyen.com/press-and-media/adyen-index-my-2026
27. TechCrunch — Tab, 2026-10-07  
    https://techcrunch.com/2026/10/07/another-personal-ai-assistant-has-launched-meet-tab-which-emerged-from-stealth-with-a-300m-valuation/

---

## Research maintenance rule

This snapshot will age.

Before using it for:
- investment;
- pricing;
- procurement;
- government proposal;
- market-entry decision;
- public claim;
- grant application;
- sales material;

re-verify time-sensitive facts against current primary sources.

No market forecast in this file should be promoted into a `D-xxx | LOCKED` decision without explicit owner instruction.
