> **Canonical:** https://governedautonomy.org/observatory/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/observatory/ — the site is authoritative.

# Standards Observatory

A running survey of published work on governing autonomous AI agents. What each artifact establishes, what it leaves open, and what the field has converged on without coordinating.

**Last updated 1 November 2026.** This page is maintained continuously and dated on every revision. Entries are added when an artifact is published, verified against its primary source, and assessed for what it covers. Nothing is listed here that has not been read.

**What this page is for.** Anyone trying to govern autonomous agents today faces a dozen documents published in eighteen months by standards bodies, government agencies, vendors and researchers, with no map between them. This is the map. It is deliberately written to be useful whether or not you adopt this doctrine, and every entry links to its primary source so the assessment can be checked.

**Citation convention.** Artifacts are cited by publishing body and document identifier, never by individual author. Where a document has a DOI, the DOI is given.

## What the field agrees on

Read together, the artifacts below show more convergence than their variety suggests. Four points are now effectively settled across independent documents that do not cite one another:

1. **Governance has to run in the execution path.** Pre-deployment review and retrospective audit are both necessary and neither is sufficient. Every runtime specification published since early 2026 assumes an interception point before an action takes effect.
2. **Agents need durable identities.** Treating an agent as a feature of an application, rather than as an identity with a lifecycle, breaks attribution, revocation and audit simultaneously.
3. **Enforcement must span systems.** A control that governs one framework, one vendor or one tool surface is bypassable by construction.
4. **Evidence has to be more than present.** The newest work has moved from requiring logs to asking whether the logs can answer a question.

And one point is consistently *not* settled. **Every artifact surveyed here governs what a single agent may do at the moment it acts. None specifies what authority survives when one agent delegates work to another.** Several name cross-agent propagation as a threat; at least one mediates agent-to-agent messages through a policy engine; one standards-track document states explicitly that a binding for delegated scope must wait until cross-protocol semantics exist. The gap has now survived six independent attempts from four different kinds of organisation, which suggests it is a research problem rather than an oversight.

---

## Standards bodies and government guidance

### AARM v1.0 — Autonomous Action Runtime Management

*Cloud Security Alliance Technical Working Group, February 2026. CC BY 4.0, with a DOI.*

A system category specification defining a control plane that intercepts, evaluates, decides on and records every agent-initiated action before execution, independent of model, framework or environment. Nine requirements in RFC 2119 language, six MUST and three SHOULD, against a threat model of eleven named classes, with formal conformance levels.

**Covers:** pre-execution interception, context accumulation, intent-alignment evaluation, five authorization decision types, tamper-evident receipts, cryptographic identity binding. **Leaves open:** what would make a particular decision correct; identity lifecycle before and after the action; maturity staging. Its requirements describe interception at one agent's control plane. v2.0 is stated to introduce multi-agent coordination requirements.

Primary sources: [aarm.dev/spec](https://aarm.dev/spec) · [arXiv:2602.09433](https://arxiv.org/abs/2602.09433). Full mapping: [Governed Autonomy and AARM](https://governedautonomy.org/standards/aarm/).

### SCIM Agent Governance Extension

*IETF individual Internet-Draft, Informational, July 2026. Expires 27 January 2027.*

Extends the SCIM Agent resource type with a lifecycle state model grounded in ISO/IEC 24760-1, an autonomy classification, a validity window and credential discovery. The only document surveyed here that is still open for comment.

**Covers:** provisioning, lifecycle state, autonomy class, credential discovery for agent identities. **Leaves open, explicitly:** action-level authorization is ruled out of provisioning on the grounds that fine-grained agent authorization belongs in the authorization layer; tenant and delegation scope are deferred entirely, with the draft stating that a binding can follow once cross-protocol semantics exist.

Primary source: [datatracker.ietf.org](https://datatracker.ietf.org/doc/draft-kushwaha-scim-agent-governance/). Full mapping: [Governed Autonomy and SCIM Agent Governance](https://governedautonomy.org/standards/scim-agent-governance/).

### Careful Adoption of Agentic AI Services

*Six national cyber agencies, April 2026.*

The first multi-nation government guidance written specifically for agentic AI. Sorts risk into five categories and is, in our reading, the most prescriptive control-level document surveyed here.

**Covers:** risks and recommended practices for organisations that design, develop, deploy and operate agentic AI systems. **Leaves open:** architecture. It recommends practices, including per-action policy decision points, rather than an architecture that places each control or says which must hold simultaneously.

Full mapping: [Governed Autonomy and CISA guidance](https://governedautonomy.org/standards/cisa-agentic-ai/).

### OWASP Top 10 for Agentic Applications 2026

*OWASP, 2026.*

Ten ranked failure modes drawn from more than one hundred contributors. The broadest community statement on agentic risk, in this list.

**Covers:** ranked, named failure modes with practitioner framing. **Leaves open:** conformance. A ranked risk list is a checklist, not a testable requirement set.

Full mapping: [Governed Autonomy and the OWASP Agentic Top 10](https://governedautonomy.org/standards/owasp-agentic-top10/).

### NIST AI Risk Management Framework

*NIST.*

The canonical enterprise vocabulary for AI risk, written for organizational risk management, plus the Generative AI Profile. A NIST AI Agent Standards Initiative was launched in February 2026 naming agent security and identity as core pillars.

**Covers:** organisational risk governance vocabulary and process. **Leaves open:** agent-specific control overlays remain unpublished, so enterprises deploying agents today are working ahead of their own risk framework.

Full mapping: [Governed Autonomy and the NIST AI RMF](https://governedautonomy.org/standards/nist-ai-rmf/).

---

## Open specifications and reference implementations

### Agent Control Standard

*Open standard, MIT licensed, announced May 2026.*

Standardised middleware hooks, runtime policy interfaces and interoperability mechanisms for governing agents across frameworks. Hooks fire when an agent receives input, calls a tool, transitions from planning to execution, stores a memory, executes code or invokes a sub-agent; policy evaluation returns allow, deny or modify before the action reaches production systems.

**Covers:** cross-framework interception points and an inline verdict model, with reference implementations. **Leaves open:** what policy should say, and the delegation question at sub-agent invocation, which it hooks but does not govern.

### Open Agent Governance Specification

*Vendor-published open specification, 2026.*

Five primitives: deterministic identity, declarative policy, runtime enforcement, structured audit evidence, and cryptographic verification.

**Covers:** a primitive set that maps closely onto identity, policy, enforcement and audit. **Leaves open:** multi-agent delegation, maturity staging, and standing intervention rights.

### Agent Governance Toolkit

*MIT licensed, 2026.*

Ten formal RFC 2119 specifications with a published conformance test suite, addressing runtime enforcement against the OWASP agentic risk set.

**Covers:** testable specifications with executable conformance tests, which is rare in this field and worth noting. **Leaves open:** the same delegation boundary; the specifications govern enforcement within a deployment.

---

## Research artifacts

### DEMM-Bench — governance-evidence sufficiency

*Preprint, June 2026. arXiv:2606.20634, DOI 10.48550/arXiv.2606.20634.*

A cross-regime benchmark measuring whether agent-runtime records are *sufficient to reconstruct a decision* rather than merely present. Eight evidence regimes, eight decision properties, eight degradation conditions, 64 published cases. Finds that trace-present and schema-present baselines overclaim on 75% of cases, and names the failure mode the container fallacy.

**Covers:** a measurable, falsifiable test of audit adequacy. The first of its kind. **Leaves open:** whether a decision was correct, as distinct from reconstructable; runtime enforcement; delegation legitimacy.

Full mapping: [Governed Autonomy and DEMM-Bench](https://governedautonomy.org/standards/demm-bench/).

### Deontic policies for runtime governance

*Preprint, June 2026. arXiv:2606.19464, DOI 10.48550/arXiv.2606.19464. Stated for a 2026 IEEE symposium.*

A deontic policy language expressed in OWL and evaluated at runtime by a logic engine outside the model. Argues that permit and prohibit engines cover only a subset of governance, and that obligations, obligation lifecycle, dispensations, and meta-policy conflict resolution are missing from current approaches.

**Covers:** obligations and waivers as first-class policy constructs, and states that one pipeline governs both tool invocations and agent-to-agent messages. **Leaves open:** mediating messages through a single engine governs traffic within one control plane; what authority survives a handoff between separately governed agents is not addressed.

### Hardware-rooted runtime enforcement

*Preprint, May 2026. arXiv:2605.17909.*

A runtime enforcement architecture combining grammar-constrained decoding, CRDT-based policy synchronisation, hardware-attested execution in trusted execution environments, and machine-readable audit logging, with bounded formal verification. Relocates the policy enforcement point into the inference pipeline.

**Covers:** the deepest enforcement mechanism published, and formalises *governance latency*, the interval between deciding a policy and enforcing it, putting it at 14 to 30 days for retrospective management-system regimes. **Leaves open:** delegation breadth. A single control plane inside one inference stack, with a hardware trust envelope narrower than most deployments.

### Behavioral governance via composed authorities

*Preprint, June 2026. arXiv:2606.30970.*

A runtime governance framework evaluating each proposed action against three independent authorities, delegated authorization, owner-signed behavioral constitutions, and site action contracts, composed conservatively into a permit, review or deny verdict before execution.

**Covers:** composition of multiple independent authority sources, which is the closest published treatment of conflicting policy sources. **Leaves open:** the composition is evaluated for one acting agent.

### Runtime governance over execution paths

*Preprint, 2026. arXiv:2603.16586.*

Governance policies expressed and enforced over agent execution paths rather than isolated actions, addressing sequences whose individual steps are each permissible.

**Covers:** multi-step sequence risk, which single-action interception misses. **Leaves open:** paths are traced within one agent's execution.

### Governance-first architecture for authorized autonomous operations

*Peer-reviewed, 2026. DOI 10.3389/frai.2026.1800407.*

An architectural rather than control-catalogue treatment of authorized autonomous AI operations. Notable as one of the few peer-reviewed, DOI-bearing artifacts working at the architectural layer.

**Covers:** architecture-level structuring of authorized autonomy. **Leaves open:** assessed against the delegation boundary, the same edge remains.

---

## Method and corrections

Entries are added only after the primary source has been read and its URL verified. Assessments state what a document covers and what it leaves open, and are written so that a reader who disagrees can check the claim against the source in one click. Where a document is revised, the entry is re-checked against the revision rather than defended.

Two standing constraints on this page. Artifacts are cited by publishing body and document identifier only, never by individual author. And a document's status is stated accurately: a preprint is called a preprint, a working-group specification is called one, and neither is upgraded to the other for rhetorical convenience.

Corrections are welcome and are recorded in the [changelog](https://governedautonomy.org/changelog/) rather than made silently. If an entry mischaracterises your work, the assessment is wrong and should be fixed.

*This survey is maintained by the Governed Autonomy Institute alongside the Governed Autonomy Doctrine. The doctrine's own positions are set out separately; this page is intended to be usable independently of them, and the per-artifact mappings under Standards are where the two are explicitly related.*
