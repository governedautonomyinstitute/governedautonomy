> **Canonical:** https://governedautonomy.org/standards/cisa-agentic-ai/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy and CISA’s *Careful Adoption of Agentic AI Services*

Six national cyber agencies independently arrived at three of the four threats this doctrine names. That convergence is the most useful thing about the document.

On 30 April 2026, CISA and NSA, together with the national cyber security centres of Australia, Canada, New Zealand and the United Kingdom, published *Careful Adoption of Agentic AI Services* — the first multi-nation government guidance written specifically for autonomous AI agents rather than for AI models in general.

This page is a mapping, not a rebuttal. The guidance and this doctrine were developed independently and converge on the substance. Where they differ, they differ in *layer*: the guidance is a control catalogue, the doctrine is an architecture. Both are needed, and neither one substitutes for the other.

-----

## What the guidance establishes

The document sorts agentic risk into five categories and, importantly, argues that each demands a distinct control response rather than a single uniform governance overlay:

  - **Privilege risks.** Accumulated and excessive access. Calls for cryptographically anchored per-agent identity, short-lived task-scoped credentials, mutual TLS on agent-to-agent and agent-to-service traffic, no static keys or shared service accounts, a prohibition on agents modifying their own privileges, and formal decommissioning.
  - **Design and configuration risks.** Tool allowlisting against verified, version-pinned tools, and prompt-injection defence treated as a baseline design requirement rather than optional hardening.
  - **Behavioral risks.** Goal misalignment and oversight evasion. Oversight checkpoints must be encoded in the workflow architecture by action type, data sensitivity and value threshold — never left to the agent’s own judgement about when to check in.
  - **Structural risks.** Cascading failure across multi-agent pipelines. Each agent is an independent principal; trust is verified, never inherited transitively. Role separation, consensus for moderate-stakes actions, and circuit-breaker patterns that halt and escalate.
  - **Accountability risks.** The auditability gap. Human-readable tool-usage logs, preserved reasoning traces, consolidated end-to-end workflow records. The guidance names the finding directly: most organisations cannot distinguish agent actions from human actions in the logs they already keep.

The risk categories are anchored in documented 2025 breaches in which an agent’s reach exceeded what its task required, not in hypotheticals. That is what makes the document citable.

## Where the two converge

| Guidance risk category             | Governed Autonomy construct                                                                                                                                                                                                                   |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Privilege risks                    | [Agents Are Identities, Not Tools](/laws/#law-1-agents-are-identities-not-tools), [Agent Identity & Lifecycle](/architecture/#plane-1-agent-identity-lifecycle), and Least Agency                                                             |
| Design and configuration risks     | **Prompt Injection** on the Threat Surface, and [Execution & Tool Governance](/architecture/#plane-2-execution-tool-governance)                                                                                                               |
| Behavioral risks                   | **Behavioral Drift** on the Threat Surface, [Humans Retain the Right to Intervene](/laws/#law-5-humans-retain-the-right-to-intervene), and [Human Oversight, Audit & Traceability](/architecture/#plane-4-human-oversight-audit-traceability) |
| Structural risks                   | **Cascading Failure** on the Threat Surface, [Trust Does Not Travel](/laws/#law-4-trust-does-not-travel), and [Multi-Agent Trust & Delegation](/architecture/#plane-5-multi-agent-trust-delegation)                                           |
| Accountability risks               | [Enforce at Runtime](/laws/#law-2-enforce-at-runtime) and [Human Oversight, Audit & Traceability](/architecture/#plane-4-human-oversight-audit-traceability)                                                                                  |
| Incremental / graduated deployment | The [Governed Autonomy Maturity Model](/maturity/) — Level 1 Identified, Level 2 Governed, Level 3 Continuous                                                                                                                                 |

Three of the four threats named on the [Declaration](/), namely **Prompt Injection**, **Behavioral Drift** and **Cascading Failure**, have verbatim or near-verbatim counterparts in the guidance’s own risk language. The doctrine’s threat surface was locked before the guidance was published. Neither document informed the other.

The fourth threat, **Intent Hijacking**, has no single counterpart. It sits across two of the guidance’s categories at once: design and configuration risk supplies the delivery mechanism, privilege risk determines the blast radius. A valid action taken for an invalid reason is a control-catalogue blind spot precisely because every individual control it passes through returns “permitted.”

One further convergence is worth naming. The guidance observes that continuous-verification models tuned for human session signals are largely blind to what an agent does mid-session with credentials it already holds. That is the same conclusion the Declaration reaches in its first non-negotiable: governance must move at the speed of execution, not bookend it. See [The Zero Trust Parallel](/zero-trust/).

## Where each is thinner

### Identity governance

Both documents are aimed at the same failure mode: an agent’s permission footprint expanding past what was approved, through inheritance, integration and convenience, until no one can account for everything it can reach. That is what the guidance treats under privilege risk and what this doctrine calls **Least Agency**. Some commentary on the guidance has adopted “authority drift” for the same phenomenon; the two terms describe one problem. Least Agency remains the canonical name here because it states the constraint rather than the symptom.

On mechanism, the guidance is more prescriptive than this doctrine is, and deliberately so. It specifies mechanism: cryptographic per-agent identity, mutual TLS, short-lived task-scoped credentials, an explicit prohibition on self-modification of privilege. [Agent Identity & Lifecycle](/architecture/#plane-1-agent-identity-lifecycle) states the requirement — agents are first-class identities with mission-scoped boundaries — without naming an implementation. On this dimension the guidance is the more actionable document, and the doctrine defers to it.

### Runtime behavior control

Both documents locate control during execution rather than at the point of authorisation, and both refuse to let the agent decide when oversight applies. The guidance adds a control vocabulary the doctrine has not published: tool allowlisting with version pinning, circuit-breaker halt-and-escalate, consensus for moderate-stakes actions, and an action-tiering scheme that grades autonomy by stakes. [Humans Retain the Right to Intervene](/laws/#law-5-humans-retain-the-right-to-intervene) asserts the right; it does not yet define the tiers at which the right is exercised. That is a real gap in the doctrine, and it is named here rather than argued away.

### System integration

This is the dimension on which the doctrine reaches further. The guidance treats each risk category as a control domain to be addressed. It does not supply a model for where those controls live relative to one another, how a policy decision in one domain constrains execution in another, or how an organisation knows it is ready to widen an agent’s scope. [Governance Must Span Systems](/laws/#law-3-governance-must-span-systems) and the five Planes of the [Governed Autonomy Architecture](/architecture/) exist to answer exactly that question, and the [Governed Autonomy Maturity Model](/maturity/) stages the readiness judgement the guidance recommends but does not formalise.

## The gap

> A control catalogue tells you which controls to implement. It does not tell you where each control belongs, which ones must hold simultaneously for a single agent action to be sanctioned, or how far your organisation can safely extend autonomy today. That is an architectural question, and it survives full compliance with the catalogue.

An organisation can implement every control the guidance recommends, in isolation, and still be unable to answer the question this doctrine treats as the load-bearing one: *is what this agent is doing right now sanctioned, and can we stop it mid-chain if it is not?* Controls implemented as a checklist produce coverage. Controls implemented as a fabric produce governance. The second non-negotiable exists for that distinction.

## Complementary layers, not competing standards

The relationship is the one NIST’s Cybersecurity Framework has with its own implementation guidance, or that Zero Trust architecture has with the specific access controls that realise it. *Careful Adoption of Agentic AI Services* is the strongest control-level statement any government has published on autonomous agents. This doctrine supplies the architecture those controls sit inside — which Plane each belongs to, which Law each satisfies, and at which maturity level an organisation has earned the right to widen the mission.

Both gaps named above, mechanism under [Agent Identity & Lifecycle](/architecture/#plane-1-agent-identity-lifecycle), and stakes tiers under [Humans Retain the Right to Intervene](/laws/#law-5-humans-retain-the-right-to-intervene), are open revision items, not settled positions. This doctrine is versioned and revised in the open precisely so that guidance published after it can be absorbed rather than argued with. See the [changelog](/changelog/).

Read the guidance first. It is short, specific, and free. Then use the [Governed Autonomy Framework](/framework/) to decide where each of its controls belongs and in what order to build them.

## Primary sources

  - [CISA: *Careful Adoption of Agentic AI Services*](https://www.cisa.gov/resources-tools/resources/careful-adoption-agentic-ai-services) (resource page, 30 April 2026)
  - [Full guidance (PDF)](https://media.defense.gov/2026/Apr/30/2003922823/-1/-1/0/CAREFUL%20ADOPTION%20OF%20AGENTIC%20AI%20SERVICES_FINAL.PDF)
  - [CISA release announcement](https://www.cisa.gov/news-events/news/cisa-us-and-international-partners-release-guide-secure-adoption-agentic-ai)
