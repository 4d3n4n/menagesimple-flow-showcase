# Case study: designing continuity around one mission

**By Adenan kHACHNANE · Independent recruitment exercise · Evidence reviewed through 13 November 2026**

MénageSimple Flow aims to turn fragmented cleaning-service operations into a structured, traceable and coordinated workflow. The project asks how a request can remain understandable as it moves from customer conversation to cleaner preparation and management follow-up.

## Start with the business, not the chat box

The discovery work dated 7 November examined public service descriptions, customer and cleaner application listings, recruitment material and review platforms. It also considered how instructions, equipment and exceptions might interact in a recurring household service.

The important observation was that an existing digital service and a human relationship already coexist. Flow should not claim to invent online booking or replace that relationship. Instead, it explores continuity around a mission and the moments where responsibilities need to be explicit. The [research summary](RESEARCH_AND_DISCOVERY.md) separates public statements, user-reported experiences, hypotheses and design responses.

A recurring theme became a question rather than an accusation: **what if the information needed to perform a visit is not the same as the information needed to book it?** Equipment, access and a surface-specific instruction may matter more to the cleaner than the customer’s original wording or the quoted price.

## Convert hypotheses into product choices

| Hypothesis to investigate | Potential operational consequence | Design response | Evidence boundary |
|---|---|---|---|
| A booking description can leave task boundaries ambiguous. | Clarification or disagreement shortly before a visit. | A structured scope, focused questions and an editable mission summary. | Implemented in the demo; real-world frequency is unknown. |
| Equipment responsibilities may need to be explicit. | A visit cannot start as expected. | Identify who supplies equipment and show targeted preparation requirements. | Implemented demo checks; actual equipment is not verified. |
| A change of cleaner can interrupt continuity. | A special instruction must be repeated or is missed. | Keep an approved mission brief and require checks appropriate to the assigned cleaner. | Brief and version-aware checks exist; full handover remains designed. |
| Management needs context as well as counts. | An incident is visible without an understandable next step. | Link missions, preparation and incidents in an operational workspace. | Database-backed demo; no demonstrated organizational impact. |

## Three decisions that changed the project

### 9 November: move beyond a local interface simulation

An earlier proposal used a browser-centered application. The technical decision was to use a server-backed modular application so that authorization, shared mission state and transactional booking could be enforced beyond one screen. The trade-off was greater integration complexity, including hosting and database constraints.

### 10 November: correct a conversational form that still behaved like a wizard

The first implementation did not fully match the intended UX: interpreting a message was followed by a general form that could ask for information already supplied. A dated UX review led to a continuous conversation with contextual tools and one persistent draft. The useful pricing engine was retained; the orchestration changed.

That distinction matters. The pivot was not “add AI to a form.” It was to make a customer’s previous answer continue to count.

### 11–12 November: make exceptions precise and inspect AI failure

Subsequent refinements separated an equipment-cleaning method from another item’s method, preserved room-specific instructions and let a clear correction update the relevant scope. When a complex prompt failed, the investigation distinguished provider transport problems from interpretation and verification problems.

Selected later executions succeeded after corrections, including a multi-part request with exclusions and access instructions and a studio-layout case. Earlier failures remain part of the record. A successful example does not establish reliable interpretation of every synonym, language or future prompt.

## Engineer one coordinated workflow

The demo connects natural-language input, validated operations, calculated scope and price, synthetic availability and a persisted mission. The cleaner sees the operational brief without the quote. Management can inspect preparation and incidents through a separate authorized interface.

The [software architecture](ARCHITECTURE_OVERVIEW.md) explains these boundaries. A parallel engineering concern was preserving context across AI-assisted sessions: dated decisions, retained sources, execution evidence and concise handoffs distinguish what was intended from what was actually verified. This helped make the development history reviewable; it did not eliminate mistaken assumptions or incomplete work.

## What validation establishes

The available evidence includes historical unit, browser, build and database checks, together with selected real-provider executions. The production deployment recorded on 12 November completed successfully. During this showcase review, the public landing page responded without redirecting to a Vercel login.

The latest changes have not all received a complete end-to-end retest. Some legacy tests remain unresolved; physical-device voice input and several operational scenarios still need validation. Demo controls and synthetic records must not be mistaken for a service operating with real customers.

## What I would validate next

Interview customers, cleaners and operational staff to test the hypotheses, observe how a mission is prepared, and measure where clarification is actually needed. Then evaluate instruction completeness, readiness issues caught before a visit, continuity after changes and incident-resolution time—with clear denominators and privacy safeguards.

Those are proposed measures, not achieved results. The project’s contribution is a working demo and a traceable set of product and engineering decisions, with its remaining boundaries visible.

[Product scope](PRODUCT_OVERVIEW.md) · [UX rationale](DESIGN_DECISIONS.md) · [Back to README](README.md)
