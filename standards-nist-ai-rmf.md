> **Canonical:** https://governedautonomy.org/standards/nist-ai-rmf/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/nist-ai-rmf/ — the site is authoritative.

# Governed Autonomy and the NIST AI Risk Management Framework

The canonical risk vocabulary for enterprise AI, written for organizational risk management rather than runtime agent control. NIST's own agent-specific work is still in development. This mapping covers both facts.

**Note on criterion identifiers.** Identifiers such as C1.1 or CX.1 refer to [RFC 001 revision 2](https://governedautonomy.org/rfc/v4-conformance-layer/), a historical proposal preserved as published. They are not v4 requirements. The current requirements are the [baseline R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/). This mapping has not yet been restated against them.

The NIST AI Risk Management Framework (AI RMF 1.0, January 2023) is the reference point for enterprise AI risk in the United States: a voluntary framework organized around four functions, extended in July 2024 by a Generative AI Profile naming twelve risks specific to generative systems. It is the document most enterprise AI governance programs are built on. It already contemplates systems that operate with varying levels of autonomy: MEASURE 2.4 calls for monitoring the system's behavior in production, and MANAGE 2.4 for mechanisms to supersede, disengage or deactivate a system whose outcomes are inconsistent with intended use. What it does not supply, by design, is an agent-specific runtime architecture: how authority is scoped to a mission, evaluated at each action and re-established at each handoff. NIST's agent-specific work is proceeding through separate efforts that have not yet published. This page maps what transfers, what does not, and what governs the interval.

## What the AI RMF establishes

| RMF function | What it covers | Where it lands in this doctrine |
|---|---|---|
| GOVERN | Cross-cutting culture, policy, roles, and accountability for AI risk | [Plane 4, Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability); [Law 5](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene). The RMF governs the organization; the doctrine adds governance of the agent's behavior itself. |
| MAP | Establishing context: what the system is, who it affects, what can go wrong | [Pillar 2, Mission Definition](https://governedautonomy.org/framework/#pillar-2-mission-definition): an agent's context is its mission, and mapping it is where Least Agency is set. |
| MEASURE | Analyzing, benchmarking, and monitoring AI risk | The [Conformance Layer proposed in RFC 001](https://governedautonomy.org/rfc/v4-conformance-layer/) is this doctrine's answer to what measurement means for agent governance: criteria with determinate verification questions, assessable per deployment. |
| MANAGE | Allocating resources to mapped and measured risks; response and recovery | Partially [Plane 3](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine). But see the gap below: management is a lifecycle activity, and agent risk concentrates at runtime. |

Of the Generative AI Profile's twelve named risks, four bear directly on agents: information security, human-AI configuration (automation bias and over-reliance, the same failure the doctrine addresses under Law 5), value-chain and component integration (the supply chain beneath the agent), and confabulation (why an agent's account of its own action cannot serve as evidence about that action). The profile names no agent-specific risks; it was written for generative systems.

## The interval, stated plainly

NIST's agent-specific work is real and public: a control-overlay program whose concept paper proposes dedicated overlays for single-agent and multi-agent systems, and an agent standards initiative launched in February 2026 covering interoperability, identity, and security. As of this mapping's publication, the two agent overlays have no published draft. That is not a criticism; deliberate standards work takes time. But it defines the present interval: enterprises are deploying autonomous agents today under a general risk framework, while the agent-specific guidance is still being drafted. This doctrine exists for that interval. It is versioned and revised in the open precisely so that when the overlays publish, they can be mapped here rather than argued with, exactly as was done for [CISA's agentic guidance](https://governedautonomy.org/standards/cisa-agentic-ai/).

## No floor: 212 actions carry no tier

The timing gap above is not the Generative AI Profile's only structural property worth naming. The profile's 212 suggested actions carry no minimum viable subset, no tiering by organizational size or risk exposure, and no companion Playbook of the kind the base AI RMF has. A [public comment on the June 2024 draft](https://live-cltc.pantheon.berkeley.edu/wp-content/uploads/2024/06/GAI-Profile-NIST-AI-600-1-Berkeley-Comments-.pdf), from UC Berkeley's Center for Long-Term Cybersecurity, recommended NIST designate a prioritized minimum tier; the final document did not adopt the recommendation. An organization deploying its first generative AI system receives the same 212-item, unranked list as one operating at frontier scale.

That gap has a direct answer in this doctrine. The mandatory runtime baseline ([R01 to R18](https://governedautonomy.org/doctrine/)) applies to every deployment, with an applicability matrix, and the [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) describes organizational capability without deferring any baseline requirement. Where the RMF's four functions supply the enterprise risk vocabulary and this doctrine supplies the runtime layer (below), the baseline supplies what a 212-item undifferentiated list cannot: a stated set of requirements and a way to decide which apply.

## Where each is thinner

### What the RMF supplies that this doctrine does not

An organizational risk-management discipline: roles, culture, documentation, lifecycle process, and a vocabulary that procurement offices, auditors, and regulators already speak. Measurement science and testbeds behind the MEASURE function. Federal standing. On enterprise risk process, the RMF is the stronger instrument, and this doctrine defers to it entirely: nothing here replaces an RMF program, and a mature organization will run both.

### What this doctrine supplies that the RMF does not

The RMF's functions operate on the lifecycle: mapping and measuring the system, monitoring it in production, and governing and managing around it. An autonomous agent's defining risk arises as it acts, mid-mission, at machine speed, across systems, where a framework of organizational practices has no enforcement surface. The doctrine's contribution is the runtime layer the RMF does not claim to provide: agents as governed identities, policy evaluated at each governed action, intervention that takes effect before the next one, trust re-established at every handoff. In RMF terms: the doctrine is what MANAGE has to become when the system being managed makes its own decisions between reviews.

## Complementary layers, not competing standards

Run the RMF as the enterprise risk chassis. Use this doctrine for the layer the RMF leaves open: what must be true, architecturally and at runtime, for an autonomous agent's actions to be governed while they happen. When NIST's agent overlays publish, this page gains a sibling mapping them criterion by criterion.

## Primary sources

- [NIST AI RMF 1.0 (NIST AI 100-1, January 2023)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)
- [Generative AI Profile (NIST AI 600-1, July 2024)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)
- [NIST Control Overlays for Securing AI Systems (COSAiS)](https://csrc.nist.gov/projects/cosais) and the [concept paper](https://csrc.nist.gov/csrc/media/Projects/cosais/documents/NIST-Overlays-SecuringAI-concept-paper.pdf) proposing single-agent and multi-agent overlays
- [NIST AI Agent Standards Initiative (February 2026)](https://www.nist.gov/artificial-intelligence/ai-agent-standards-initiative)
- [UC Berkeley Center for Long-Term Cybersecurity, public comment on the AI 600-1 draft (June 2024)](https://live-cltc.pantheon.berkeley.edu/wp-content/uploads/2024/06/GAI-Profile-NIST-AI-600-1-Berkeley-Comments-.pdf)
