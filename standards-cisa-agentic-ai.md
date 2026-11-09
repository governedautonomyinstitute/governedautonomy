> **Canonical:** https://governedautonomy.org/standards/cisa-agentic-ai/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/cisa-agentic-ai/ — the site is authoritative.

# Governed Autonomy and CISA's *Careful Adoption of Agentic AI Services*

Six national cyber agencies independently arrived at three of the four threats this doctrine names. That convergence is the most useful thing about the document.

**Note on criterion identifiers.** Identifiers such as C1.1 or CX.1 refer to [RFC 001 revision 2](https://governedautonomy.org/rfc/v4-conformance-layer/), a historical proposal preserved as published. They are not v4 requirements. The current requirements are the [baseline R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/). This mapping has not yet been restated against them.

On 1 May 2026, CISA and NSA, together with the national cyber security centres of Australia, Canada, New Zealand and the United Kingdom, published *Careful Adoption of Agentic AI Services* — the first multi-nation government guidance written specifically for autonomous AI agents rather than for AI models in general.

This page is a mapping, not a rebuttal. The guidance and this doctrine converge on the substance. Where they differ, they differ in *layer*: the guidance sets out risks and recommended practices, including per-action policy decisions and fail-safe defaults; the doctrine sets out an architecture for those practices to sit inside. Both are needed, and neither one substitutes for the other.

---

## What the guidance establishes

The document sorts agentic risk into five categories and, importantly, argues that each demands a distinct control response rather than a single uniform governance overlay:

- **Privilege risks.** Accumulated and excessive access. Recommends cryptographically anchored identity for each agent, mutual TLS on inter-agent and agent-to-service calls, ephemeral credentials in place of static, long-lived secrets, just-in-time credentials for privileged actions, and a prohibition on agents modifying their own privileges or delegating without expiry timers and recorded grant chains.
- **Design and configuration risks.** Tool use restricted to an approved allow list of tools and versions that are regularly verified, and prompt-injection filtering built into the design.
- **Behavioral risks.** Goal misalignment, unintended and deceptive behaviour. Human control points built into the workflow, with human approval where the cost of error is high, such as system resets, network egress or deletion of critical records.
- **Structural risks.** Cascading failure across interconnected agents. Separation of duties by role, consensus controls scaled to risk (multi-agent approval for moderate stakes, human approval added for high stakes), and fail-safe defaults that require agents to stop and escalate.
- **Accountability risks.** Actions that are hard to attribute and explain across chains of agents. Human-readable logs of tool usage, monitoring and auditing that keep decisions and actions traceable, and independent monitoring that cross-validates what agents report.

The guidance also sets deployment limits that any mapping has to carry forward. It recommends that organisations use agentic AI only for low-risk and non-sensitive tasks, and that they deploy incrementally, beginning with clearly defined low-risk tasks. It calls for continuous runtime authentication with centralised policy decision points for each action, the same per-action decision this doctrine places in Planes 2 and 3.

## Where the two converge

| Guidance risk category | Governed Autonomy construct |
|---|---|
| Privilege risks | [Agents Are Identities, Not Tools](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools), [Agent Identity & Lifecycle](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle), and Least Agency |
| Design and configuration risks | **Prompt Injection** on the Threat Surface, and [Execution & Tool Governance](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance) |
| Behavioral risks | **Behavioral Drift** on the Threat Surface, [Humans Retain the Right to Intervene](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene), and [Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability) |
| Structural risks | **Cascading Failure** on the Threat Surface, [Trust Does Not Travel](https://governedautonomy.org/laws/#law-4-trust-does-not-travel), and [Multi-Agent Trust & Delegation](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) |
| Accountability risks | [Enforce at Runtime](https://governedautonomy.org/laws/#law-2-enforce-at-runtime) and [Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability) |
| Incremental / graduated deployment | The [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) — rated by dimension as Identified, Governed or Continuous; separate from any deployment |

Three of the four threats named on the [Declaration](https://governedautonomy.org/), namely **Prompt Injection**, **Behavioral Drift** and **Cascading Failure**, have verbatim or near-verbatim counterparts in the guidance's own risk language. The doctrine's Threat Surface section was added in v3.0 (11–12 May 2026), after the guidance was published; this mapping records convergence, not independence of origin.

The fourth threat, **Intent Hijacking**, has no single counterpart. It sits across two of the guidance's categories at once: design and configuration risk supplies the delivery mechanism, privilege risk determines the blast radius. A valid action taken for an invalid reason is hard to catch with controls applied one at a time, because every individual control it passes through returns "permitted."

One further convergence is worth naming. In one of the guidance's own scenarios, an agent keeps relying on cached authorisation decisions after a component it integrates is compromised, and invokes functions that should have required per-request verification. That is the conclusion the Declaration reaches in its first non-negotiable: governance operates in the execution path, at the time relevant conditions must hold. See [The Zero Trust Parallel](https://governedautonomy.org/zero-trust/).

## Where each is thinner

### Identity governance

Both documents are aimed at the same failure mode: an agent's permission footprint expanding past what was approved, through inheritance, integration and convenience, until no one can account for everything it can reach. That is what the guidance treats under privilege risk and what this doctrine calls **Least Agency**. Some commentary on the guidance has adopted "authority drift" for the same phenomenon; the two terms describe one problem. Least Agency remains the canonical name here because it states the constraint rather than the symptom.

On mechanism, the guidance is more prescriptive than this doctrine is, and deliberately so. It specifies mechanism: cryptographic per-agent identity, mutual TLS, ephemeral and just-in-time credentials, an explicit prohibition on self-modification of privilege. [Agent Identity & Lifecycle](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle) states the requirement (agents are first-class identities with mission-scoped boundaries) without naming an implementation. On this dimension the guidance is the more actionable document, and the doctrine defers to it.

### Runtime behavior control

Both documents place control in the execution path, not only at the point of authorisation, and both refuse to let the agent decide when oversight applies. The guidance adds a control vocabulary the doctrine has not published: an allow list of verified tools and versions, fail-safe defaults that stop and escalate, and consensus controls graded by stakes, with human approval added for high-stakes actions, and a recommendation to classify agent actions by impact, likelihood and reversibility. In v4, profiles classify effects as permitted within standing bounds, requiring additional authorization, or prohibited, and state which effects require action-specific human approval (see the action classes in the [v4 text](https://governedautonomy.org/doctrine/)). That is consistent with the guidance's recommendation to classify agent actions by impact, likelihood and reversibility; this page does not claim v4 reproduces the guidance's control vocabulary.

### System integration

This is the dimension on which the doctrine reaches further. The guidance treats each risk category as a control domain to be addressed. It does not supply a model for where those controls live relative to one another, how a policy decision in one domain constrains execution in another, or which requirements a deployment must demonstrate. [Governance Must Span Systems](https://governedautonomy.org/laws/#law-3-governance-must-span-systems) and the five Planes of the [Governed Autonomy Architecture](https://governedautonomy.org/architecture/) exist to answer exactly that question, and the mandatory baseline ([R01 to R18](https://governedautonomy.org/doctrine/)) states what every deployment must demonstrate; the [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) separately describes organizational capability.

## The gap

> A list of recommended controls tells you which controls to implement. It does not tell you where each control belongs or which ones must hold simultaneously for a single agent action to be sanctioned. That is an architectural question, and it remains after every recommendation is in place.

An organisation can implement every control the guidance recommends, each inside its own system, and still be unable to show that they held together for a single action: *is what this agent is doing right now sanctioned, and can we stop it mid-chain if it is not?* Controls implemented as a checklist produce coverage. Controls implemented as a fabric produce governance. The second non-negotiable exists for that distinction.

## Complementary layers, not competing standards

The relationship is the one NIST's Cybersecurity Framework has with its own implementation guidance, or that Zero Trust architecture has with the specific access controls that realise it. *Careful Adoption of Agentic AI Services* is, in our reading, the strongest control-level government statement on autonomous agents that we have mapped. This doctrine supplies the architecture those controls sit inside: which Plane each belongs to, which Law each satisfies, and what a deployment must demonstrate under the baseline. It does not lift the guidance's own deployment cautions, including its recommendation to keep agentic AI to low-risk, non-sensitive tasks.

The mechanism gap named above, under [Agent Identity & Lifecycle](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle), has not been restated against v4. This doctrine is versioned and revised in the open so that guidance published after it can be absorbed, and feedback is accepted at any time. See the [changelog](https://governedautonomy.org/changelog/).

Read the guidance first. It is short, specific, and free. Then use the [Governed Autonomy Framework](https://governedautonomy.org/framework/) to decide where each of its controls belongs and in what order to build them.

## Primary sources

- [CISA: *Careful Adoption of Agentic AI Services*](https://www.cisa.gov/resources-tools/resources/careful-adoption-agentic-ai-services) (released 1 May 2026)
- [Full guidance (PDF)](https://media.defense.gov/2026/Apr/30/2003922823/-1/-1/0/CAREFUL%20ADOPTION%20OF%20AGENTIC%20AI%20SERVICES_FINAL.PDF)
- [CISA release announcement](https://www.cisa.gov/news-events/news/cisa-us-and-international-partners-release-guide-secure-adoption-agentic-ai)
