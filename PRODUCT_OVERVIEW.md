# Product overview

Flow is organized around **one mission shared across three roles**. The customer defines and approves a scope; the cleaner receives an operational brief; management follows preparation and exceptions.

The implementation is a demonstration using synthetic records. It does not connect to MénageSimple’s official systems.

## Reading the status labels

- **Implemented:** supporting application code was inspected during this review.
- **Tested:** identified historical execution evidence supports a specific behavior, not universal correctness.
- **Demo / Simulated:** data or an interaction is synthetic; this label can accompany an implemented feature.
- **Designed:** specified, but not demonstrated end to end.
- **Planned:** a future concept.
- **Unverified:** sufficient implementation or execution evidence was unavailable.

Code was inspected read-only outside the documentation copy. Application tests were not rerun for this showcase; the evidence is bounded to the recorded versions and scenarios.

## Customer: express the need, then make informed choices

A customer can describe a home and a cleaning request in natural language. Contextual tools clarify missing scope, distinguish service variants and retain specific notes. A summary shows tasks, estimated duration, equipment responsibility and a deterministic synthetic quote before appointment selection.

The current implementation supports corrections through chat and controls, synthetic availability, an account requirement before final recording, and conversation and mission history. A saved conversation is distinct from a permanent, consented property-memory system.

| Capability | Status |
|---|---|
| Text conversation, contextual choices, scope and specific notes | **Implemented / Demo**; selected AI cases **Tested**. |
| Task and duration controls, deterministic quote | **Implemented / Demo**; calculation and selected interface behavior **Tested** historically. |
| Selecting an eligible cleaner and appointment | **Implemented / Demo**; synthetic capacity, no external calendar. |
| Accounts, conversation history and mission consultation | **Implemented**; selected server checks **Tested**. Latest UI changes are not fully retested. |
| Voice transcription | **Implemented** through browser capabilities; physical-device behavior **Unverified**. |
| Recurring bookings and consented property memory | **Designed**; recurrence has a management-side **Simulated** preview. |

## Cleaner: receive a brief that supports the work

The cleaner workspace shows upcoming missions, status, task estimates, address context, special notes and equipment preparation. The operational projection excludes customer quote amounts. It supports responding to a request, acknowledging the brief, recording preparation checks and reporting an incident.

These functions are **Implemented / Demo**, with selected recorded tests. Equipment checks record declarations, not physical inspection or product certification. Complete task execution, offline support and a full replacement handover remain **Designed**. A replacement independently verifying the latest brief is an intended requirement, not a fully demonstrated recovery service.

## Management: see consequences in context

The authenticated desktop workspace reads mission, assignment, preparation and incident records. It includes search, a schedule, catalog consultation, incident resolution, request qualification and aggregate mission views. Charts summarize the stored demo records rather than claiming business performance. The map suppresses small groups and does not expose individual home locations.

Those functions are **Implemented / Demo**. Some access and calculation checks have recorded **Tested** evidence; the newest layout is not fully verified in-browser. Urgent dispatch, recurrence, full handovers, aftercare/time-dispute handling and several editing operations are **Simulated previews**, not operational integrations.

## One requirement across the lifecycle

**Illustrative composite example—not a new end-to-end test:** a customer requests cleaning with a precaution for a delicate floor. The assistant proposes structured scope and a room-specific note. Rules validate the proposal and calculate a demo quote; the customer approves and selects synthetic capacity. The cleaner receives the approved requirements and can report an equipment issue. Management sees the linked incident and records a resolution.

The individual capabilities exist in the demo and have partial recorded evidence. Replacing the cleaner, transferring the changed brief and independently rechecking everything is the **Designed** continuation of this example.

## Where to explore

The [public demo](https://menagesimple-flow.vercel.app/) is intended for fictional requests. Cleaner and management access is role-restricted; credentials are not published here. The demo has no payment processing, real notifications or stock integration. Provider delays, remaining legacy-test failures, accessibility work and operational policy review limit what can be inferred from it.

Possible future evaluation measures include instruction completeness, readiness issues detected before a visit and incident-resolution time. No field-validated improvement is claimed.

[UX decisions](DESIGN_DECISIONS.md) · [Architecture](ARCHITECTURE_OVERVIEW.md) · [Back to README](README.md)
