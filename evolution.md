> **Canonical:** https://governedautonomy.org/evolution/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Evolution of the Doctrine

Nine months of documented iteration. Built the way science is built: on prior work, in the open, and correctable.

Standards are usually presented as finished things. This one is not. The Governed Autonomy Doctrine began as a set of working papers in late 2025, was rewritten repeatedly as autonomous agents changed what enterprise software is, and reached its current form through published revisions, an adversarial review that found real contradictions, and an open comment process. This page records that lineage. The original artifacts are preserved, and their cryptographic fingerprints are published below so the record cannot be quietly rewritten — including by us.

> Where this doctrine and other work converge, the convergence is documented, not claimed. Where this doctrine was wrong, the correction is published. That is the whole method.

## Phase 1 — The trust problem (November 2025)

The earliest working papers predate the agentic wave. They address what enterprises were actually facing in late 2025: ungoverned use of consumer AI tools inside regulated environments. Two papers from mid-November frame the problem — one as a governance analysis of the dilemma itself (data exfiltration into model memory, the audit gap behind model recommendations, AI access outstripping role-based controls), and one as an adoption strategy, arguing that guardrails alone fail: if the sanctioned path is slower than the shadow path, the workforce routes around governance, so the secure way has to be made the easy way.

Two convictions from this phase survive in the doctrine today: model output cannot be trusted on the model's own account, and governance that only says no gets bypassed rather than obeyed.

## Phase 2 — The first draft standard (Q4 2025)

By the end of 2025 the working papers had consolidated into a first framework document: a predecessor standard for federal enterprise AI built on a single axiom — that an AI system's intent can never be assumed and its agency must always be verified. It was explicitly modeled on what Zero Trust did to perimeter security, and it already contained, in early form, constructs the doctrine still carries:

  - A four-tier risk classification for AI deployments, graded by stakes and autonomy — the ancestor of the [Action Tiering](/rfc/v4-conformance-layer/) construct now proposed in RFC 001.
  - A human-primacy rule: no high-tier output is final until a human has validated not just its correctness but its *intent alignment* — the ancestor of [Humans Retain the Right to Intervene](/laws/#law-5-humans-retain-the-right-to-intervene).
  - A traceability law: every AI action carries provenance metadata sufficient to reconstruct who, what model, and under whose supervision — the ancestor of [Plane 4](/architecture/#plane-4-human-oversight-audit-traceability).
  - A prohibition on ungoverned consumer AI in official use, with sanctioned gateways as the alternative.

## Phase 3 — The agentic turn (December 2025)

In December 2025 the papers register the shift that produced this doctrine: the risks stopped being about what models say and became about what agents do. A working paper on federal health argued that goal drift in an autonomous agent is not a software defect but a mission-safety failure, and drew three architectural conclusions the doctrine still stands on:

  - Enforcement must be deterministic and sit between the agent and the systems it touches. A policy stated in a prompt is a suggestion; a violating action must be stopped by machinery the agent cannot reason its way past. This is the seed of [Enforce at Runtime](/laws/#law-2-enforce-at-runtime) and of the fail-closed posture in RFC 001.
  - Multi-agent systems need flight-recorder observability: reconstruction of what happened, across every agent involved, from records alone.
  - The center of gravity must move from identities to *actions* — from what an agent can access to what it is doing. The industry's leading analysts arrived at the same formulation, independently, roughly a year later.

## Phase 4 — Practitioner grounding (November 2025 – January 2026)

In parallel, the author's own engineering work through this period — building and operating real systems with AI agents daily — supplied the doctrine's practitioner temper: direct experience of the velocity agents provide, of the illusion of competence they create, and of the complexity debt they accumulate when the human stops understanding why the system works. The doctrine's insistence that governance must not strangle autonomy, only bound it, comes from this period. It was written by someone who wants agents to run, not by someone trying to stop them.

## Phase 5 — The scaffolding era and publication (early 2026 → May 2026)

Through early 2026, as agent scaffolding and tool-connection protocols proliferated far faster than any governance of them, the framework was rebuilt around the runtime: agents as first-class identities, mission-scoped authority, cross-system enforcement, explicit multi-agent trust. It was published in May 2026 as a versioned public doctrine — five Laws, an architecture, an implementation framework, and the Zero Trust parallel — followed within days by the v3.0 restructuring that produced the current spine. From publication onward, every change is in the [changelog](/changelog/).

## Phase 6 — Falsifiability (July–August 2026)

The most recent phase is the one this doctrine regards as its real contribution: [RFC 001](/rfc/v4-conformance-layer/) proposes conformance criteria an implementation can be assessed against and can fail. The proposal was adversarially reviewed; three internal contradictions were found; revision 2 corrected them and printed the corrections. In August 2026 the doctrine was renamed to its own oldest language — the Maturity Model had described the path to governed autonomy since first publication — and republished at this domain, with the rename recorded openly in the changelog.

## The artifact ledger

The pre-publication working papers are preserved in their original form. Their SHA-256 fingerprints are published here; any claimed copy can be checked against them. Further artifacts from the early-2026 period are being retrieved from archived storage and will be added to this ledger.

| Artifact                                                                                        | Period              | SHA-256 (first 16) |
| ----------------------------------------------------------------------------------------------- | ------------------- | ------------------ |
| Governance dilemma analysis (memorandum form)                                                   | November 2025       | `23a29e8e4e167f85` |
| Adoption strategy paper (secure path as easy path)                                              | November 2025       | `baa4351f744738bf` |
| First draft standard (verify-agency axiom, four tiers, human primacy, traceability)             | Q4 2025             | `d711f71ffc35c9ff` |
| Federal-health agentic risk paper (deterministic enforcement, goal drift, identities → actions) | December 2025       | `7ebbc0e476da9098` |
| Practitioner build retrospective I                                                              | Nov 2025 – Jan 2026 | `b220e7b8bc3668ff` |
| Practitioner build retrospective II (velocity, illusion of competence, complexity debt)         | January 2026        | `976807181402890d` |

> Priority is a weak claim; provenance is a strong one. This page makes no assertion of being first to any idea here. It asserts something better evidenced: nine months of dated, preserved, iterated work, corrected in the open, and testable at the end of it.

Where to go next: the [Declaration](/) for the doctrine as it stands; the [changelog](/changelog/) for every published change; [the RFCs](/rfc/) for what may change next.
