> **Canonical:** https://governedautonomy.org/standards/blueprint-alliance/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/blueprint-alliance/ — the site is authoritative.

# Governed Autonomy and the Blueprint Alliance

Twelve founding members, expanding an earlier blueprint, arrived at six principles that each have a counterpart in this doctrine. The question worth asking next is what an implementation would have to show to be judged against them.

On 22 September 2026 a cross-industry coalition named the Blueprint Alliance was announced, with twelve founding member companies spanning identity, AI, data, applications, infrastructure and cybersecurity, and strategic advisors from outside the technology industry. The coalition describes its output as an open, multi-vendor reference architecture for securing AI agents, expanded from a blueprint first introduced in March 2026. Its stated scope is the governance layer once agents are deployed, complementing work on model security and supply-chain integrity.

This page is a mapping, not a review. It maps the six principles, four core challenges and eight capability areas stated in the public announcement onto this doctrine's constructs, and records where the doctrine's proposed conformance criteria sit alongside them.

**Note on criterion identifiers.** Identifiers such as C1.1 or CX.1 refer to [RFC 001 revision 2](https://governedautonomy.org/rfc/v4-conformance-layer/), a historical proposal preserved as published. They are not v4 requirements. The current requirements are the [baseline R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/). This mapping has not yet been restated against them.

**What was read.** This page is based on the coalition's public announcement, read in full. The blueprint document itself is distributed through a registration form and was *not* reviewed. Nothing here characterizes its contents, diagrams or requirements beyond what the announcement states. Where this page and the blueprint disagree about the blueprint, the blueprint is right.

## The six principles

The announcement states that the founding members "aligned toward a shared set of principles for securing AI agents." Left column is the announcement's wording, verbatim. The announcement does not cite this doctrine, and this mapping does not suggest otherwise.

| Blueprint Alliance principle | Where it lands in this doctrine |
|---|---|
| "treating every agent as a first-class identity" | [Law 1, Agents Are Identities, Not Tools](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools); [Plane 1, Agent Identity & Lifecycle](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle) |
| "scoping access to the task rather than granting standing access" | **Least Agency**, stated under [Law 1](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools) and as the third of the [Non-Negotiables](https://governedautonomy.org/): no more authority than the mission demands |
| "keeping delegation traceable" | [Law 4, Trust Does Not Travel](https://governedautonomy.org/laws/#law-4-trust-does-not-travel); [Plane 5, Multi-Agent Trust & Delegation](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) |
| "monitoring runtime behavior continuously" | [Law 2, Enforce at Runtime](https://governedautonomy.org/laws/#law-2-enforce-at-runtime); [Plane 3, Policy & Compliance Engine](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine) |
| "enabling containment that is instant and reversible" | [Law 5, Humans Retain the Right to Intervene](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene); [Plane 4, Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability) |
| "ensuring governance adapts at the speed AI moves" | The first [Non-Negotiable](https://governedautonomy.org/laws/#the-three-non-negotiables): governance operates in the execution path, at the time relevant conditions must hold |

One Law has no single-principle counterpart: [Law 3, Governance Must Span Systems](https://governedautonomy.org/laws/#law-3-governance-must-span-systems). It appears instead in the coalition's structure and its interoperability commitment, covered below.

## The four core challenges

The announcement organizes the architecture around four questions. Each maps to one or more Planes.

| Question (verbatim) | Capability areas named in the announcement | Where it lands in this doctrine |
|---|---|---|
| **Where are my agents?** | AI agent development, discovery, and identity; AI agent security posture management | [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle); [Pillar 1, Agent Identity](https://governedautonomy.org/framework/#pillar-1-agent-identity). The announcement's requirement that every agent have "an accountable human owner or operational team" is the lifecycle ownership Plane 1 carries. |
| **What can they do?** | Access policies; Governance | [Pillar 2, Mission Definition](https://governedautonomy.org/framework/#pillar-2-mission-definition) and [Pillar 3, Behavioral Policy](https://governedautonomy.org/framework/#pillar-3-behavioral-policy); delegation "as agents spawn sub-agents and act on behalf of humans" is [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) |
| **What are they doing?** | Runtime authorization and monitoring; Resource access | [Plane 2, Execution & Tool Governance](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance) and [Plane 3](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine); [Pillar 4, Runtime Enforcement](https://governedautonomy.org/framework/#pillar-4-runtime-enforcement). Enforcement "inline through gateways that sit in the execution path" is Law 2 stated as a placement. |
| **How do I respond?** | Response and enforcement; Access recovery | [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability); [Pillar 5, Human Oversight & Intervention](https://governedautonomy.org/framework/#pillar-5-human-oversight-intervention). Restoring a contained agent "through re-attestation and staged re-enrollment" returns it to [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle). |

The announcement states that all eight capability areas rest on two foundations, "execution context and risk signals," fed by runtime telemetry, logging and observability. In this doctrine that connective role is split between [Plane 3](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine), which consumes context at decision time, and [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability), which holds the record.

## Where the two converge

The closest convergence is on delegation and containment. The announcement names three failure conditions the architecture is meant to close: shadow agents that multiply, credentials that "cross trust boundaries," and agents that "execute beyond their intended scope." Those are, respectively, the absence of Plane 1, the problem Law 4 exists to name, and the condition Least Agency is written to prevent.

The second convergence is structural. The coalition's interoperability commitment, cross-vendor signal sharing across MCP, OCSF, SSF and CAEP so that "a threat signal raised by one runtime monitor triggers real-time action across all connected control planes," is [Law 3](https://governedautonomy.org/laws/#law-3-governance-must-span-systems) and the second [Non-Negotiable](https://governedautonomy.org/laws/#the-three-non-negotiables) (enforcement must be a fabric, not a fragment) pursued as an engineering program across vendors. A reference architecture assembled by twelve vendors is itself an argument that no single product spans the systems an agent touches.

## What this doctrine provides alongside it

The announcement describes principles, challenges, capability areas and a commitment to publish joint interoperability results and reference integrations. The doctrine's contribution at the same layer is a proposed set of criteria stated so that an implementation can be tested against them and can fail. [RFC 001, The Conformance Layer](https://governedautonomy.org/rfc/v4-conformance-layer/) proposed twenty-nine such criteria. RFC 001 revision 2 is a historical proposal preserved as published, not v4 text; the doctrine in force is v4 ([R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/)).

Read against the six principles, the relevant RFC 001 criteria are:

| Principle | RFC 001 criterion (proposed) |
|---|---|
| Scope access to the task | **C1.3**: an agent's authority is granted per mission, expires with the mission, and does not persist across missions or into dormancy. |
| Keep delegation traceable | **C5.1**: trust is established at every handoff and never carried across one. **C5.2**: authority is never inherited from an invoking agent; a subagent's authority is granted independently, scoped to its own mission. These ask a narrower question than traceability: not only whether a delegation can be followed afterward, but what authority is permitted to exist on the far side of it. |
| Monitor runtime behavior continuously | **C3.2**: policy is evaluated during execution, at each governed action, not once at session start. **C3.8**: an action whose applicable criteria cannot be evaluated does not proceed, which covers the window when the monitor itself is unavailable. |
| Containment that is instant and reversible | **C4.1**: a revocation, override or halt is honored before the agent's next commit. **C5.4**: on detection, the governing system halts every downstream consumer of the affected agent's output, not only the agent. |
| Treat every agent as an identity | **C1.1**: every action appears in the record, attributed to exactly one agent, in every system the agent touches. **C1.2**: agent-originated actions are distinguishable from human-originated actions without inference. |
| Governance at the speed AI moves | **CX.1**, the Simultaneity Criterion: every applicable criterion holds for a single action within that action's decision window, and the parameters evaluated are identical to the parameters committed. |

A reference architecture and a conformance layer answer different questions: the first says which capabilities belong where, the second says what must be true for a given action to count as governed. They are designed to be used together. An implementation built to the blueprint could be assessed against RFC 001's criteria, and RFC 001 is preserved as a historical proposal; feedback on the v4 baseline is accepted at any time.

## Primary sources

- [Industry leaders form the Blueprint Alliance to advance a shared architecture for securing AI agents](https://www.okta.com/newsroom/press-releases/industry-leaders-form-the-blueprint-alliance/) (coalition announcement, 22 September 2026; the source for every quotation on this page)
- [blueprintalliance.ai](https://blueprintalliance.ai), the coalition's site, where the blueprint is distributed (registration form; not reviewed for this page)
