> **Canonical:** https://governedautonomy.org/standards/imda-agentic-ai/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/imda-agentic-ai/ — the site is authoritative.

# Governed Autonomy and Singapore's *Model AI Governance Framework for Agentic AI*

A national regulator's guidance for organizations deploying agents, written as recommended practice and revised once already. Nearly every recommendation has a home in this doctrine's architecture. The useful next question is how an organization would show that a recommendation holds for a given action.

Singapore's Infocomm Media Development Authority (IMDA) first published the *Model AI Governance Framework for Agentic AI* in January 2026 and released Version 1.5 on 20 May 2026, updated 5 June 2026. The framework describes itself as giving organizations "a structured overview of the risks of agentic AI and emerging best practices in managing these risks," and is addressed to organizations deploying agents, whether developed in-house or obtained as third-party solutions. It calls itself a living document, and states that Version 1.5 "incorporates feedback received from 60+ companies since v1.0."

This page is a mapping, not a review. It maps the framework's four dimensions and their recommendations onto this doctrine's constructs, and records where the doctrine's proposed conformance criteria sit alongside them. The framework does not cite this doctrine, and this mapping does not suggest otherwise.

**Note on criterion identifiers.** Identifiers such as C1.1 or CX.1 refer to [RFC 001 revision 2](https://governedautonomy.org/rfc/v4-conformance-layer/), a historical proposal preserved as published. They are not v4 requirements. The current requirements are the [baseline R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/). This mapping has not yet been restated against them.

**What was read.** The framework PDF linked below was read in full for its framework text. As retrieved on 6 October 2026, it identifies itself as **Version 1.5**, published 20 May 2026 and updated 5 June 2026, which is the version IMDA currently publishes at that address. The organizational case studies embedded in the framework were not relied on, and nothing here characterizes any named organization. IMDA's factsheet and announcement pages were confirmed live, but their body text did not render for retrieval and they are not relied on. Quotations keep the framework's British spelling. Where this page and the framework disagree about the framework, the framework is right.

## What the framework establishes

The framework separates two properties of an agent: its **action-space**, the "range of actions the agent can take," determined by its tools and the permissions on them, and its **autonomy**, the "degree to which an agent can decide how to act towards a goal," determined by its instructions and the level of human involvement. Version 1.5 adds controls and logging and monitoring to an agent's core components, alongside the model, instructions, memory, planning, tools and protocols. It treats risk as a function of likelihood and impact, and lists factors for each, including the agent's access to sensitive data and external systems, its level of autonomy, and the **reversibility** of its actions.

Its recommendations are organized in four dimensions:

1. **Assess and bound the risks upfront.** Choose suitable use cases, then limit each agent's tools, autonomy and area of impact, and give it an identity and an authorization model.
2. **Make humans meaningfully accountable.** Allocate responsibility inside and outside the organization, and design human oversight that stays effective against automation bias.
3. **Implement technical controls and processes.** Controls during design and development, testing before deployment, gradual rollout with continuous monitoring after it, and change management throughout.
4. **Enable end-user responsibility.** Transparency for people who interact with agents, and training for people who integrate agents into their work.

## Dimension 1: assess and bound the risks upfront

Left column is the framework's wording, verbatim.

| Framework recommendation | Where it lands in this doctrine |
|---|---|
| "Define least-privilege policies that give agents only the minimum tools and data access needed for it to complete its task." | **Least Agency**, the third of the [Non-Negotiables](https://governedautonomy.org/): no more authority than the mission demands. Enforced at [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle) through mission-scoped access boundaries, and at [Plane 2, Execution & Tool Governance](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance), for tool invocation. |
| "Define similar SOPs for agentic workflows that an agent is constrained to follow, rather than giving the agent the freedom to define every step of the workflow." | [Pillar 2, Mission Definition](https://governedautonomy.org/framework/#pillar-2-mission-definition) and [Pillar 3, Behavioral Policy](https://governedautonomy.org/framework/#pillar-3-behavioral-policy); workflow sequencing enforced at [Plane 2](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance) |
| "Design mechanisms and procedures to take agents offline and limit their potential scope of impact when they malfunction." | [Law 5, Humans Retain the Right to Intervene](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene); the intervention interfaces of [Plane 4, Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability) |
| "In general, prefer deterministic rather than non-deterministic limits, and bound by design." | [Law 2, Enforce at Runtime](https://governedautonomy.org/laws/#law-2-enforce-at-runtime): limits enforced by the governing system at the point of action, rather than requested of the agent, at [Plane 2](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance) and [Plane 3, Policy & Compliance Engine](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine) |
| "An agent should have its own unique, cryptographically verifiable identity, such that it can identify itself to the organisation, its human user, or other agents." | [Law 1, Agents Are Identities, Not Tools](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools); [Plane 1, Agent Identity & Lifecycle](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle); [Pillar 1, Agent Identity](https://governedautonomy.org/framework/#pillar-1-agent-identity) |
| "To prevent agent sprawl, all agent identities (and their attendant permissions) should be issued from and tracked by a centralised system." | The agent registry at [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle); the Identified rating in the [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) |
| "The human user should not be able to set permissions for the agent greater than what the human user is himself authorised to do"; "such delegations of authority should be clearly recorded." | [Law 4, Trust Does Not Travel](https://governedautonomy.org/laws/#law-4-trust-does-not-travel); delegation scope at [Plane 5, Multi-Agent Trust & Delegation](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) |
| Identity gaps named by the framework, including "recursive delegation scenarios where agents spin up multiple sub-agents" | [Law 4](https://governedautonomy.org/laws/#law-4-trust-does-not-travel) and [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation), which treat subagent spawning as one of the handoffs at which trust is established rather than carried |
| Reversibility as a risk factor: "whether such modifications are easily reversed" | The action tiers proposed in [RFC 001](https://governedautonomy.org/rfc/v4-conformance-layer/), which grade governed actions by reversibility, from Tier 1, Reversible, to Tier 3 |

## Dimension 2: make humans meaningfully accountable

| Framework recommendation | Where it lands in this doctrine |
|---|---|
| "Organisations should define significant checkpoints or action boundaries that require human approval, especially before sensitive actions are executed," including high-stakes, irreversible, outlier and user-defined cases | [Law 5](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene); escalation from automated enforcement to human decision at [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability); [Pillar 5, Human Oversight & Intervention](https://governedautonomy.org/framework/#pillar-5-human-oversight-intervention) |
| "Keep approval requests contextual and digestible, while making the risk clear." | [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability); addressed from the integrity side by RFC 001 criterion C4.4, below |
| "Regularly auditing the effectiveness of human oversight," including tracking the "human override rate" and reviewer response times | [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability), where human decisions are part of the record; the Continuous rating in the [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) |
| "Human oversight should be complemented with automated real-time monitoring to escalate any unexpected or anomalous behaviour." | [Law 2](https://governedautonomy.org/laws/#law-2-enforce-at-runtime); behavior monitoring at [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability) and contextual policy evaluation at [Plane 3](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine) |
| Clear allocation of responsibilities "by establishing chains of accountability across the agent value chain and lifecycle" | [Law 1](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools) and the agent registry at [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle), which tie each agent to an accountable lifecycle. The organizational allocation itself, across teams, vendors and contracts, is guidance the doctrine does not restate. |

## Dimension 3: implement technical controls and processes

| Framework recommendation | Where it lands in this doctrine |
|---|---|
| "Rather than prompt-layer safeguards, consider implementing deterministic safeguards that operate at a system-level through predefined logic, especially for higher-risk actions." | [Law 2](https://governedautonomy.org/laws/#law-2-enforce-at-runtime); [Pillar 4, Runtime Enforcement](https://governedautonomy.org/framework/#pillar-4-runtime-enforcement) |
| "Apply the principle of least privilege to limit tools available to each agent, enforced through robust authentication and authorisation" | Least Agency at [Plane 2](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance); tool and API invocation authorization |
| For MCP servers, "Whitelist trusted servers and only allow agent to interact with servers on that whitelist" | [Plane 2](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance); RFC 001 criteria C2.1 and C2.2, below |
| "Require agents to communicate through structured schemas such as typed function calls rather than free text" | [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation); [Pillar 6, Multi-Agent Governance](https://governedautonomy.org/framework/#pillar-6-multi-agent-governance) |
| Pre-deployment testing for "overall task execution," "policy compliance," "tool calling" and "robustness," across whole workflows and at the multi-agent level | RFC 001 criteria C2.3 and C4.6, below |
| "Gradually rolling out agents into production to control the amount of risk exposure" | The [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/): rated by dimension as Identified, Governed or Continuous. It is separate from any deployment and does not license one |
| "Intervene in real-time: When potential failures are detected, stop agent workflow and escalate to a human supervisor" | [Law 2](https://governedautonomy.org/laws/#law-2-enforce-at-runtime) and [Law 5](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene); [Pillar 4](https://governedautonomy.org/framework/#pillar-4-runtime-enforcement) |
| "Logging and tracing each step of an agent workflow and agent-to-agent interactions"; "Ensure log immutability" | The reconstructable record at [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability); chain-level audit at [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) |
| "Throughout the lifecycle, implement change management and version control processes" | RFC 001 criteria C2.2 and C2.3, below, which bind each tool to a version and re-run adversarial testing on every model or prompt change |

## Dimension 4: enable end-user responsibility

The fourth dimension asks organizations to inform users of an agent's range of actions, its access to data and the user's own responsibilities, and to train people who integrate agents into their work so that they can oversee agents effectively while keeping their tradecraft and foundational skills. This doctrine is an architecture for the governing system and does not address end-user transparency or workforce training. The nearest point of contact is [Law 5](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene), since the framework's training aims at people who must recognize agent failure in order to intervene. The dimension is recorded here as outside the doctrine's scope, not as covered by it.

## Where the two converge

The framework's action-space and autonomy are the two quantities Least Agency bounds: what an agent can reach, and how much it decides for itself on the way. Its use of reversibility as a risk factor, and its call for human approval before irreversible actions, follows the same line RFC 001 draws between its action tiers.

The closest convergence in Version 1.5 is on where a limit lives. The framework's advice to "bound by design" is concrete: "rather than relying on prompts to instruct the agent against accessing certain tools, impose access controls that prevent the tool from being called by the agent at all." That is the distinction [Law 2](https://governedautonomy.org/laws/#law-2-enforce-at-runtime) rests on, between a limit the agent is asked to observe and a limit the governing system enforces.

Version 1.5 also adds a section on systemic and multi-agent risks. Its "cascading or compounding effects," in which "a mistake in one step can propagate and amplify across later steps," is **Cascading Failure** on this doctrine's [Threat Surface](https://governedautonomy.org/). It names prompt injection among the ways shared context between agents can be exposed, which is **Prompt Injection** on the same surface. Its observation that agents crossing "system or organisational boundaries" are harder to test is the territory of [Law 3, Governance Must Span Systems](https://governedautonomy.org/laws/#law-3-governance-must-span-systems).

On identity, the framework states that "this is an evolving space, and gaps exist today in terms of handling agent identity robustly," noting that agents need permissions that "may change dynamically depending on the context, risk levels, and task objectives." That is the problem [Law 4](https://governedautonomy.org/laws/#law-4-trust-does-not-travel) and [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) are written around, and the framework's interim rule, that a user cannot delegate more authority than the user holds, is one concrete form of it.

## What this doctrine provides alongside it

The framework is recommended practice: it describes what organizations should consider and gives examples. The doctrine's contribution at the same layer is a proposed set of criteria stated so that an implementation can be tested against them and can fail. [RFC 001, The Conformance Layer](https://governedautonomy.org/rfc/v4-conformance-layer/) proposed twenty-nine such criteria. RFC 001 revision 2 is a historical proposal preserved as published, not v4 text; the doctrine in force is v4 ([R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/)).

Read against the framework's recommendations, the relevant RFC 001 criteria are:

| Framework recommendation | RFC 001 criterion (proposed) |
|---|---|
| Limit tools and data access to the task | **C1.3**: an agent's authority is granted per mission, expires with the mission, and does not persist across missions or into dormancy. **C1.4**: no path within the agent's enumerated tool surface reaches its own authority, mission scope, or governing policy. |
| Unique agent identity, with the capacity it acts in recorded | **C1.1**: every action appears in the record, attributed to exactly one agent, in every system the agent touches. **C1.2**: agent-originated actions are distinguishable from human-originated actions without inference. |
| Delegations of authority clearly recorded | **C5.2**: authority is never inherited from an invoking agent; a subagent's authority is granted independently, scoped to its own mission. This asks a narrower question than recording: not only whether a delegation can be followed afterward, but what authority is permitted to exist on the far side of it. |
| Whitelisted tools and MCP servers; version control | **C2.1**: the complete set of tools an agent can invoke is enumerable in advance. **C2.2**: every tool has established provenance and a bound version. |
| Deterministic limits, bound by design | **C3.2**: policy is evaluated during execution, at each governed action, not once at session start. **C3.8**: an action whose applicable criteria cannot be evaluated does not proceed. |
| Human approval before irreversible actions | **C4.2**: every governed action carries an assigned tier, determined before it is attempted. **C4.3**: a Tier 3 action cannot commit without a recorded human authorization event that is non-delegable to any agent. |
| Approval requests that are contextual and digestible | **C4.4**: the representation of an action presented to a human for authorization is generated by the governing system from the action's committed parameters, not by the agent, and the record retains exactly what was shown. |
| Test agents before deployment; change management | **C2.3**: a documented adversarial corpus is executed against the deployment, recorded with its version and pass rate, and re-run on every model or prompt change. **C4.6**: evidentiary obligations are declared before deployment and demonstrated against the runtime before it. |
| Stop the workflow in real time and escalate | **C4.1**: a revocation, override or halt is honored before the agent's next commit. |
| Cascading or compounding effects | **C5.4**: on detection of anomalous behavior, the governing system halts every downstream consumer of the affected agent's output, not only the agent. |
| Log and trace each step and agent-to-agent interaction | **C4.7**: a mission crossing multiple systems produces one reconstructable record, not fragments per system. |
| Oversight at the speed agents act | **CX.1**, the Simultaneity Criterion: every applicable criterion holds for a single action within that action's decision window, and the parameters evaluated are identical to the parameters committed. |

A model governance framework and a conformance layer answer different questions: the first says what a responsible organization should consider and put in place, the second says what must be true for a given action to count as governed. They are designed to be used together. An organization following the framework could test its deployment against RFC 001's criteria, and RFC 001 is preserved as a historical proposal; feedback on the v4 baseline is accepted at any time. The framework also invites feedback and case studies; that invitation is IMDA's, and nothing on this page responds to it.

## Primary sources

- [IMDA, *Model AI Governance Framework for Agentic AI*](https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf) (PDF; Version 1.5, published 20 May 2026, updated 5 June 2026, as retrieved 6 October 2026; the source for every quotation on this page)
- [IMDA, *Updated Model AI Governance Framework for Agentic AI*](https://www.imda.gov.sg/resources/press-releases-factsheets-and-speeches/updated-model-ai-governance-framework-for-agentic-ai) (announcement, 20 May 2026; not relied on for any statement here)
- [IMDA factsheet, *Model AI Governance Framework for Agentic AI*](https://www.imda.gov.sg/resources/press-releases-factsheets-and-speeches/factsheets/2026/model-ai-governance-framework-for-agentic-ai) (January 2026; not relied on for any statement here)

*Mapped 6 October 2026 against Version 1.5. When IMDA revises the framework, this page will be revised to match it rather than defended.*
