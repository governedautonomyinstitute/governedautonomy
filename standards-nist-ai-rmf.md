> **Canonical:** https://governedautonomy.org/standards/nist-ai-rmf/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy and the NIST AI Risk Management Framework

The canonical risk vocabulary for enterprise AI — written before agents could act. NIST's own agent-specific work is still in development. This mapping covers both facts.

The NIST AI Risk Management Framework (AI RMF 1.0, January 2023) is the reference point for enterprise AI risk in the United States: a voluntary framework organized around four functions, extended in July 2024 by a Generative AI Profile naming twelve risks specific to generative systems. It is the document most enterprise AI governance programs are built on. It is also, by its own timeline, a pre-agentic document: it manages the risks of systems that produce outputs, not systems that take actions. NIST knows this; its agent-specific work is proceeding through separate efforts that have not yet published. This page maps what transfers, what does not, and what governs the interval.

## What the AI RMF establishes

| RMF function | What it covers                                                              | Where it lands in this doctrine                                                                                                                                                                                                                                         |
| ------------ | --------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GOVERN       | Cross-cutting culture, policy, roles, and accountability for AI risk        | [Plane 4, Human Oversight, Audit & Traceability](/architecture/#plane-4-human-oversight-audit-traceability); [Law 5](/laws/#law-5-humans-retain-the-right-to-intervene). The RMF governs the organization; the doctrine adds governance of the agent's behavior itself. |
| MAP          | Establishing context: what the system is, who it affects, what can go wrong | [Pillar 2, Mission Definition](/framework/#pillar-2-mission-definition): an agent's context is its mission, and mapping it is where Least Agency is set.                                                                                                                |
| MEASURE      | Analyzing, benchmarking, and monitoring AI risk                             | The [Conformance Layer proposed in RFC 001](/rfc/v4-conformance-layer/) is this doctrine's answer to what measurement means for agent governance: criteria with determinate verification questions, assessable per deployment.                                          |
| MANAGE       | Allocating resources to mapped and measured risks; response and recovery    | Partially [Plane 3](/architecture/#plane-3-policy-compliance-engine). But see the gap below: management is a lifecycle activity, and agent risk concentrates at runtime.                                                                                                |

Of the Generative AI Profile's twelve named risks, four bear directly on agents: information security, human-AI configuration (automation bias and over-reliance, the same failure the doctrine addresses under Law 5), value-chain and component integration (the supply chain beneath the agent), and confabulation (why an agent's account of its own action cannot serve as evidence about that action). The profile names no agent-specific risks; it predates the agentic wave by design and by date.

## The interval, stated plainly

NIST's agent-specific work is real and public: a control-overlay program whose concept paper proposes dedicated overlays for single-agent and multi-agent systems, and an agent standards initiative launched in February 2026 covering interoperability, identity, and security. As of this mapping's publication, the two agent overlays have no published draft. That is not a criticism; deliberate standards work takes time. But it defines the present interval: enterprises are deploying autonomous agents today under a risk framework written before agents could act, while the agent-specific guidance is still being drafted. This doctrine exists for that interval. It is versioned and revised in the open precisely so that when the overlays publish, they can be mapped here rather than argued with, exactly as was done for [CISA's agentic guidance](/standards/cisa-agentic-ai/).

## Where each is thinner

### What the RMF supplies that this doctrine does not

An organizational risk-management discipline: roles, culture, documentation, lifecycle process, and a vocabulary that procurement offices, auditors, and regulators already speak. Measurement science and testbeds behind the MEASURE function. Federal standing. On enterprise risk process, the RMF is the stronger instrument, and this doctrine defers to it entirely: nothing here replaces an RMF program, and a mature organization will run both.

### What this doctrine supplies that the RMF does not

The RMF's functions operate on the lifecycle: before deployment (map, measure) and around it (govern, manage). An autonomous agent's defining risk arises during execution, mid-mission, at machine speed, across systems, where a framework of organizational practices has no enforcement surface. The doctrine's contribution is the runtime layer the RMF does not claim to provide: agents as governed identities, policy evaluated at each governed action, intervention that takes effect before the next one, trust re-established at every handoff. In RMF terms: the doctrine is what MANAGE has to become when the system being managed makes its own decisions between reviews.

## Complementary layers, not competing standards

Run the RMF as the enterprise risk chassis. Use this doctrine for the layer the RMF leaves open: what must be true, architecturally and at runtime, for an autonomous agent's actions to be governed while they happen. When NIST's agent overlays publish, this page gains a sibling mapping them criterion by criterion. One further note for the record: the phrase "governed autonomy" appears in none of the NIST documents cited here. The state the overlays are being written to enable is the state this doctrine names, defines, and proposes to make testable.

## Primary sources

  - [NIST AI RMF 1.0 (NIST AI 100-1, January 2023)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)
  - [Generative AI Profile (NIST AI 600-1, July 2024)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)
  - [NIST Control Overlays for Securing AI Systems (COSAiS)](https://csrc.nist.gov/projects/cosais) and the [concept paper](https://csrc.nist.gov/csrc/media/Projects/cosais/documents/NIST-Overlays-SecuringAI-concept-paper.pdf) proposing single-agent and multi-agent overlays
  - [NIST AI Agent Standards Initiative (February 2026)](https://www.nist.gov/artificial-intelligence/ai-agent-standards-initiative)
