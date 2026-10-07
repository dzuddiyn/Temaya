# FUTURE PRIVATE PRINCIPAL AGENT + AGENT-TO-AGENT DIRECTION

**Status:** OPEN FUTURE ASPIRATION — NOT LOCKED  
**Date:** 2026-10-08  
**Scope:** Future productization / commercialization direction. Not current Stage 0/1 critical path.

## Owner premise

Temaya's long-term defensible value should not be defined by building a bespoke booking, calling, purchasing or merchant-integration stack for every business.

The stronger long-term thesis is:

1. **Temaya is the user's/family's private principal agent.**
2. Its expensive/valuable asset is trusted private context, memory, preferences, identity, household continuity, permissions and history.
3. Businesses are expected to increasingly expose their own AI agents or agent-ready interfaces for sales, service, booking, support, commerce and other front-door interactions.
4. A future **Office / Liaison Agent** can act as Temaya's controlled outward-facing delegate and communicate with business/merchant agents on behalf of the user.
5. Direct merchant-specific integrations should therefore be gap-driven fallbacks, not the core product thesis.

This direction is aspirational, not a prediction that every business will definitely have an AI agent within a specific timeframe.

## Future boundary

```text
PRIVATE TEMAYA / FAMILY PRINCIPAL AGENT
identity + private memory + household context + preferences + authority
                    |
                    | scoped mandate only
                    v
            OFFICE / LIAISON AGENT
      minimum necessary external context
                    |
                    | agent-to-agent / protocol interaction
                    v
        BUSINESS / MERCHANT / SERVICE AGENT
                    |
                    v
        proposal / booking / quote / result
                    |
                    v
            Temaya verifies + records
```

## Privacy and authority principle

The Office / Liaison Agent should **not** receive unrestricted access to raw private memory.

It should receive only:
- minimum necessary context for the current task;
- explicit user/household identity claims required for the task;
- scoped authorization;
- spending/commitment limits where relevant;
- expiry/timeout for the mandate;
- required return evidence.

Consequential, irreversible, financial or privacy-sensitive actions must still respect existing Temaya Human Queue, deterministic authorization and verification principles.

## Protocol direction

Future interoperability should prefer open/maintainable standards where viable rather than one-off merchant adapters.

Current 2026 examples include:
- Agent2Agent (A2A) for agent communication;
- Model Context Protocol (MCP) for tool/context access;
- Universal Commerce Protocol (UCP) / Agentic Commerce Protocol (ACP) for commerce workflows;
- Agent Payments Protocol (AP2) and other payment authorization/settlement rails.

Exact protocol choices remain OPEN and must be evidence-driven when this future work becomes current.

## Malaysia market signal

Current market evidence supports exploring this direction later, but does not make it a current implementation requirement.

Observed signals in 2026 include:
- Malaysia has already seen a live agentic transaction pilot involving Mastercard Agent Pay with CIMB and RHB;
- Malaysian consumers show high AI-assisted shopping usage but meaningful hesitation about allowing AI to complete purchases autonomously;
- Malaysian retailers are actively exploring AI/agentic commerce.

The strategic implication is that **trust, privacy, identity, authorization, reliability and onboarding** may matter more than raw model capability for a consumer/family agent.

## Productization aspiration

Current priority remains:

```text
FAMILY-ONLY
    ↓
RELIABLE
    ↓
LOW-FRICTION ONBOARDING
    ↓
PROVE REAL DAILY VALUE
    ↓
GENERALIZE SAFELY
    ↓
MALAYSIA PRODUCT / MARKET TEST
    ↓
SCALE ONLY AFTER EVIDENCE
```

Do not prematurely optimize Temaya for a commercial market before the family deployment is genuinely reliable and useful.

## Current implementation consequence

For present Stage 0/1 work:
- do not build a broad merchant-booking/purchase/calling subsystem merely to imitate other personal-agent products;
- preserve reusable action/approval/verification foundations because they remain useful for future agent-to-agent delegation;
- prefer protocol-ready, replaceable integration boundaries;
- only build merchant-specific connectors when a proven real use case justifies them;
- keep private personal/family context as the high-value core.

## Open questions for future review

- final name and role boundary of the Office / Liaison Agent;
- external-agent identity and authentication;
- mandate/delegation format;
- selective-disclosure model;
- merchant-agent discovery;
- A2A/UCP/ACP/AP2 or successor protocol selection;
- payment/legal/liability boundaries;
- audit receipts and dispute handling;
- Malaysian regulatory requirements;
- product packaging, pricing and onboarding;
- whether the commercial product remains family-first or expands to individuals/small teams.

No D-xxx decision is changed by this note.
