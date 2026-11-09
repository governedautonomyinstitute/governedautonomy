> **Canonical:** https://governedautonomy.org/standards/aarm/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/aarm/ — the site is authoritative.

# Governed Autonomy and AARM

AARM specifies where the control point goes and what it must be capable of. It does not specify what a correct decision at that control point would be. That is the difference between a mechanism and a verdict, and both are load-bearing.

**Note on criterion identifiers.** Identifiers such as C1.1 or CX.1 refer to [RFC 001 revision 2](https://governedautonomy.org/rfc/v4-conformance-layer/), a historical proposal preserved as published. They are not v4 requirements. The current requirements are the [baseline R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/). This mapping has not yet been restated against them.

In February 2026 the Cloud Security Alliance Technical Working Group published *Autonomous Action Runtime Management* (AARM) v1.0, a system category specification under CC BY 4.0 with a DOI. It defines a control plane that intercepts, evaluates, decides on, and records every agent-initiated action before execution, independent of model, framework or environment. Nine requirements are stated in RFC 2119 language — six MUST (Core), three SHOULD (Extended) — against a threat model of eleven named classes.

This page is a mapping, not a rebuttal. AARM is, in our reading, the most rigorous runtime-governance specification we have mapped, it is openly licensed, and it is testable in the way this doctrine has argued governance must be testable. On mechanism, this doctrine defers to it.

**Read AARM first.** Where this page and the specification disagree about AARM, the specification is right. It is short, free, and precise, and it is doing something this doctrine deliberately does not: naming the implementation.

## What AARM establishes

Six MUST requirements define the Core conformance level:

| Requirement | What it requires | Where it lands in this doctrine |
|---|---|---|
| **R1** Pre-execution interception | Every agent-initiated action is intercepted before it executes; no action bypasses the control plane | [Enforce at Runtime](https://governedautonomy.org/laws/#law-2-enforce-at-runtime), stated as a MUST. This doctrine's second Law expressed as a conformance requirement, by an independent body. |
| **R2** Context accumulation | Stated intent, prior actions and task thread are maintained and available to policy evaluation at decision time | [Plane 3, Policy & Compliance Engine](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine); the mission-scoping input the [Mission Definition pillar](https://governedautonomy.org/framework/) produces |
| **R3** Policy evaluation with intent alignment | Each action is evaluated against both the action and its alignment with stated intent; isolated evaluation does not conform | The closest published analogue to this doctrine's **Intent Hijacking** threat: a valid action taken for an invalid reason. R3 is the requirement that makes it detectable at all. |
| **R4** Five authorization decisions | The engine must be capable of ALLOW, DENY, MODIFY, STEP_UP, DEFER | [Plane 2](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance) for the effect, [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability) for STEP_UP. Note that STEP_UP encodes [Humans Retain the Right to Intervene](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene) as a decision type rather than an escape hatch. |
| **R5** Tamper-evident receipts | Every evaluated action produces a verifiable record of action, decision, timestamp and policy context | [Plane 4, Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability). More specific than anything this doctrine publishes on evidence form. |
| **R6** Identity binding | Each receipt is cryptographically bound to a uniquely identified agent, supporting non-repudiation | [Agents Are Identities, Not Tools](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools); [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle). The Law asserts it; R6 makes it verifiable per action. |

Three SHOULD requirements define Extended conformance: **R7** semantic distance tracking between proposed actions and original intent over long horizons — the closest operational treatment of **Behavioral Drift** in any published specification; **R8** telemetry export in an interoperable format; **R9** least-privilege credential scoping at action time, which is [Least Agency](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools) applied to credentials rather than to authority.

## Where the two converge

AARM's eleven threat classes reproduce all four threats on this doctrine's [Declaration](https://governedautonomy.org/), not three: prompt injection (T1) by name, goal hijacking (T4) as the substance of Intent Hijacking, cross-agent propagation (T7) as Cascading Failure, and intent drift (T6) as Behavioral Drift — and T6 carries its own SHOULD requirement. This is the closest convergence with any external document mapped on this site. The Threat Surface was locked in May 2026 and AARM published in February 2026; neither derives from the other.

The deeper convergence is temporal. AARM's definition of runtime management insists that governance operate *during* execution, not in preprocessing or planning, because only then can an action be halted before its consequence is incurred. That is this doctrine's first Non-Negotiable in a specification's voice: governance operates in the execution path, at the time relevant conditions must hold.

## Where each is thinner

### What AARM supplies that this doctrine does not

A conformance target an implementation can be tested against and can fail, with an evidence package and a review process behind it. Named decision types. Receipt content requirements. Four implementation architectures with their trust trade-offs stated — protocol gateway, SDK instrumentation, kernel eBPF, vendor integration — which is a level of mechanism this doctrine does not publish and does not intend to. On *how to build the control point*, AARM is the stronger document.

### What this doctrine supplies that AARM does not

R3 requires that policy evaluate an action against intent alignment. It does not say what alignment consists of, or what would make a particular ALLOW correct. That is deliberate and appropriate for a system category specification — and it leaves the verdict criterion open. A control plane can satisfy every one of R1–R9, return wrong decisions consistently, and remain fully conformant. [RFC 001](https://governedautonomy.org/rfc/v4-conformance-layer/) is proposed against exactly that gap: criteria for what a correct decision would have to satisfy, stated so that an assessor can attempt to falsify a claim.

Three further surfaces AARM's scope excludes by design. It governs action execution, so the **identity lifecycle** before and after the action — provisioning, autonomy classification, suspension, decommissioning — is out of frame; that is [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle), and the live IETF work mapped at [SCIM Agent Governance](https://governedautonomy.org/standards/scim-agent-governance/) is addressing it from the other end. There is no **organizational maturity** dimension: AARM states what conformance requires of a control plane, while the [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) describes how consistently an organization sustains governance and defers no baseline requirement. And **intervention rights** appear as STEP_UP, a decision the engine may produce, rather than as a standing human right the architecture must preserve.

## Multi-agent delegation: an open edge, and a closing one

AARM v1.0's requirements govern what a single agent may do at the moment it acts. Cross-agent propagation appears in the threat model as T7 and a conformant implementation must address it, but the nine requirements describe interception at one agent's control plane; they do not specify what authority survives a handoff, or how trust is evaluated when one agent delegates to another. That is [Trust Does Not Travel](https://governedautonomy.org/laws/#law-4-trust-does-not-travel) and [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation).

This should be stated with an expiry date on it. The specification says v2.0 will *introduce multi-agent coordination requirements* and add guidance for stateful long-horizon task governance. When it does, part of what this doctrine currently supplies at Plane 5 will exist as testable requirements published by a working group with a DOI, and this page will need rewriting rather than defending. That is the correct outcome. A doctrine that needs its neighbours to stay incomplete is not a doctrine.

## Complementary layers, not competing standards

Use AARM to build the control plane and assess it against AARM's own conformance requirements. Use this doctrine to decide which planes that control plane sits between, and what a correct verdict at it would be against the mandatory baseline. The relationship is the one an architecture has with a component specification: the component can be conformant and the system still wrong, and no amount of component rigour closes that.

## Primary sources

- [AARM v1.0 — Autonomous Action Runtime Management](https://aarm.dev/spec) (Cloud Security Alliance Technical Working Group, February 2026, CC BY 4.0)
- [arXiv:2602.09433](https://arxiv.org/abs/2602.09433) — the specification paper
- [CSA AARM Technical Working Group](https://cloudsecurityalliance.org/research/working-groups/autonomous-action-runtime-management-aarm)
- [aarm-dev/aarm](https://github.com/aarm-dev/aarm) — errata and contributions
