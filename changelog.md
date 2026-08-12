> **Canonical:** https://governedautonomy.org/changelog/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Changelog

The doctrine is versioned, dated, and revised in the open.

A doctrine that asks enterprises to govern autonomous behavior must itself be governed: every substantive change to the Governed Autonomy Doctrine is versioned, dated, and recorded here. The current version is **v3.4**. Versions v1.0 through v3.2 were published as the *AI Harness Doctrine* at aiharnessdoctrine.org; the historical entries below retain that name because that is the name under which they shipped.

-----

## In review

[RFC 001: The Conformance Layer](/rfc/v4-conformance-layer/) proposes a fourth doctrine layer for v4: twenty-nine testable, mechanism-agnostic Conformance Criteria across the five Architectural Planes, an Action Tiering construct that closes the Law 5 gap recorded below, an architectural home for Intent Hijacking, and a rebuild of the Maturity Model as an assessment instrument in which each level licenses a tier of agent action. Now at **revision 2** (1 August 2026), which corrects three internal contradictions found in adversarial review of revision 1 and records them openly. Open for comment through 31 October 2026. It is a proposal and is not in force.

-----

## v3.4 · August 7, 2026

  - Two standards mappings published: the [OWASP Top 10 for Agentic Applications 2026](/standards/owasp-agentic-top10/) (including the convergent treatment of Least-Agency) and the [NIST AI Risk Management Framework](/standards/nist-ai-rmf/) (including the status of NIST's unpublished agent-specific control overlays).
  - Reference pages added: [the canonical definition](/what-is-governed-autonomy/) (August 6), [the Evolution page](/evolution/) with the pre-publication artifact ledger and SHA-256 fingerprints (August 7), [About](/about/) with the publishing-entity description, and [How to Cite](/cite/) with version-pinned formats and anchor-citation guidance.
  - Doctrine substance unchanged: no change to the Laws, Planes, Pillars, Threat Surface, or Maturity Model.

-----

## v3.3 · August 6, 2026

  - **The doctrine is republished at governedautonomy.org as the Governed Autonomy Doctrine.** The substance is unchanged: the 5 Laws, the 5 Architectural Planes, the 6 Framework Pillars, the Threat Surface, and the Maturity Model carry over intact, with their anchors preserved. Only the name changes.
  - Rationale, recorded plainly: across the industry, “harness” now denotes the enablement scaffolding around a model — the semantic inverse of this doctrine's subject — and the former name collided with several unrelated works. “Governed autonomy” is the state the doctrine exists to make reachable, and has been this doctrine's own language since the Maturity Model shipped.
  - Publisher renamed accordingly: the **Governed Autonomy Institute**.
  - Technical: [llms.txt](/llms.txt) is now generated from the built site at every deploy (an [llms-full.txt](/llms-full.txt) with full page text was added); structured data expanded (per-page TechArticle plus a DefinedTermSet for the canonical vocabulary); cache-control headers added so stale page variants cannot be served after a deploy.

-----

## v3.2 · July 31, 2026

  - Opened the [standards landscape](/standards/) section: mappings between the doctrine and published standards or government guidance on agentic AI.
  - First mapping published: [CISA's *Careful Adoption of Agentic AI Services*](/standards/cisa-agentic-ai/) (30 April 2026). Three of the four named Threat Surface items have verbatim counterparts in its risk categories, arrived at independently.
  - Recorded two acknowledged gaps in the doctrine relative to that guidance: [Agent Identity & Lifecycle](/architecture/#plane-1-agent-identity-lifecycle) states the identity requirement without specifying mechanism, and [Humans Retain the Right to Intervene](/laws/#law-5-humans-retain-the-right-to-intervene) asserts the right without defining the stakes tiers at which it is exercised. Both are carried as open revision items.
  - Recognised “authority drift” as a secondary term in circulation for the failure mode **Least Agency** constrains, noted on the [CISA mapping](/standards/cisa-agentic-ai/). Least Agency remains the canonical name.

-----

## v3.1 · June 10, 2026

  - Added stable anchor identifiers to every Law, Plane, and Pillar so external documents can cite doctrine sections directly.
  - Introduced doctrine versioning, this changelog, and structured publisher metadata (author: AI Harness Institute).
  - Published the [category comparison series](/vs/): AI Harness vs Identity & Access Management, Security Monitoring, Orchestration, and AI Guardrails.
  - Published [llms.txt](/llms.txt) for language-model discoverability.

-----

## v3.0 · May 11–12, 2026

Major revision of the doctrine's structure and vocabulary.

  - **Least Agency** introduced as a first-class principle, the third leg of the governance trilogy (Least Privilege → Least Trust → Least Agency) — and landed in Law 1.
  - **Law 4 renamed** from "Agent-to-Agent Trust Must Be Explicit" to **"Trust Does Not Travel,"** broadening its scope to every handoff type: delegation, orchestration, tool invocation, and subagent spawning.
  - **Architecture expanded from 4 to 5 Planes.** Plane 5 (Multi-Agent Trust & Delegation) added as the architectural home of Law 4; Plane 1 renamed to Agent Identity & Lifecycle; Plane 4 broadened to Human Oversight, Audit & Traceability.
  - **Framework expanded to 6 Pillars.** Mission Definition split out from Agent Identity; Multi-Agent Governance added.
  - **Threat Surface** section added to the Declaration: prompt injection, intent hijacking, cascading failure, behavioral drift.
  - **Maturity Model** published as a standalone page: Identified → Governed → Continuous.
  - The Declaration's three non-negotiables sharpened; homepage redesigned.

-----

## v1.0 · May 8, 2026

  - Initial public publication of the AI Harness Doctrine at aiharnessdoctrine.org: Declaration, 5 Laws, Architecture, Framework, and the Zero Trust parallel.

-----

> Proposed revisions are evaluated against one test: does the change make autonomous AI agents more governable at runtime, across systems, at the level of behavior?
