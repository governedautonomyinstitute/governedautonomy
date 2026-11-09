> **Canonical:** https://governedautonomy.org/doctrine/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/doctrine/ — the site is authoritative.

# Governed Autonomy Doctrine v4

Version 4 | Released 1 November 2026 | Governed Autonomy Institute

This document replaces the v3.6 doctrine core. In this document, **shall** identifies a requirement and **may** identifies a permitted choice.

## Purpose and scope

Governed Autonomy enables useful agent work within explicit, enforceable and reviewable authority across systems.

The doctrine governs operational assignments, authority, execution, collaboration, intervention and evidence. It applies to a single agent and to systems of agents, across public-sector, commercial, research and other environments. An agent workforce is an application of the doctrine, not its boundary.

The deployment is the unit of runtime assurance. The adopter declares its boundary and permitted effects, implements the applicable baseline, and adds use-case constraints in an assurance profile. Organizational maturity reports the organization's ability to operate these arrangements; it grants no permission to a deployment. A product's capabilities do not establish conformance of a system operated with it.

Existing identity, policy, security, data and infrastructure controls remain authoritative in their domains. Governed Autonomy coordinates their use around agent missions and effects. It does not replace enterprise security, lifecycle assurance, privacy, legal analysis, business ownership or incident management. It does not establish that a mission is lawful, its facts are true, its policy is adequate, or every future action will be safe.

## Three non-negotiables

Governance shall operate in the execution path, at the time relevant conditions must hold. Enforcement shall cover the declared cross-system effect boundary rather than rely on a fragment that the agent can bypass. Agents shall operate under Least Agency: no greater decision scope or authority than their approved missions require.

Least Agency includes the zero case: the mission owner first decides whether autonomous decision-making is warranted. Useful autonomy is then bounded and evaluated; success is not defined solely by how much work is blocked.

## The five Laws

### Agents Are Identities, Not Tools

An autonomous agent is an attributable operational principal with an accountable owner and lifecycle. Its logical identity, running workload, relevant model and tools, assignment and granted authority shall be distinguishable. Shared infrastructure shall not erase who requested, authorized or performed an effect. Identity does not by itself confer a mission or permission.

### Enforce at Runtime

An agent proposal shall be subject to protected policy and enforcement before the governed effect occurs, with further checks where material conditions can change before completion. Initial admission and after-the-fact detection alone are insufficient. Standing authorization can permit repeated, varying jobs within approved bounds; it does not remove current automated checks or create permanent trust.

### Governance Must Span Systems

The declared boundary shall include relevant tools, resources, queues, delegated work, persistent state and downstream effects. Controls shall maintain coherent authority, constraints and evidence across that boundary. Exclusions and uncovered paths remain explicit limitations. The doctrine requires coordinated properties, not one vendor, physical appliance or central service.

### Trust Does Not Travel

A handoff carries a task and relevant authenticated context, not automatic authority. A recipient shall be identified and authorized at its own boundary. Federation is permitted: different resource authorities can grant the authority for their resources. Delegation may narrow or exercise an authorized grant chain; it shall not amplify what the delegator is authorized to grant or bypass receiving policy. An orchestrator need not accumulate every execution privilege held by its workers.

### Humans Retain the Right to Intervene

Authorized humans shall have an effective means to inspect, interrupt and override governed activity. A profile shall identify the relevant authority and measurable intervention behavior. Prior authorization, interruption, revocation, containment and recovery are different operations. An interruption shall preserve accountable ownership of unfinished work and expose residual effects; neither safety nor successful continuity follows from a stop button alone.

## Reference architecture

The five Planes place responsibilities. They do not prescribe a product topology.

| Plane | Responsibility in v4 |
|---|---|
| 1. Agent Identity and Lifecycle | Attribute actors and workloads; bind approved missions and grants; manage issuance, change, expiry and revocation. |
| 2. Execution and Tool Governance | Mediate effects, enforce boundaries, bind evaluated work to execution, and govern queues, retries and indirect paths. |
| 3. Policy and Compliance Engine | Evaluate current mission context, authoritative relationships, shared limits, obligations and policy composition. |
| 4. Human Oversight, Audit and Traceability | Provide intervention and accountable continuity; preserve sufficient, protected evidence and expose uncertainty. |
| 5. Multi-Agent Trust and Delegation | Establish authority at each handoff; preserve grant chains, obligations, cumulative constraints and affected-output lineage. |

Planes 2 and 3 distinguish the policy enforcement point from the policy decision function. The agent shall not be able to replace or bypass the functions that govern it. Logical separation can be implemented in several ways, but the claimed separation must survive the actor and paths within the assessed boundary.

The six implementation Pillars remain: Agent Identity, Mission Definition, Behavioral Policy, Runtime Enforcement, Human Oversight and Intervention, and Multi-Agent Governance. Identity and mission are separate concerns within Plane 1. The Pillars identify what must be designed and operated; implementation contracts and assessment evidence specify how a particular deployment demonstrates it.

## Missions, authority and action classes

A mission is an approved bounded operational assignment, not an organizational slogan or an agent's self-description. It identifies purpose, accountable ownership, resources, permitted effects, constraints, validity conditions, obligations and relevant versions. A continuing assignment can authorize a series of jobs with varying inputs. Changing the assignment outside its approved variation is a governance event.

The mission reference can accompany an identity across systems without transferring trust. Each enforcement boundary verifies the relevant identity, mission and authority. Governing decisions use designated authoritative facts and meanings. An integrity-protected false fact remains false: the adopter owns factual and policy-adequacy risk and declares how uncertainty is handled.

Profiles classify effects as **permitted within standing bounds**, **requiring additional authorization**, or **prohibited**. They state which effects require action-specific human approval and which can proceed under an already approved bounded class. Recovery capability, sensitivity, affected parties, magnitude, time to harm and operating context inform the classes. Expanding a declared mission boundary shall not silently lower the required protection. A read can disclose data; its treatment depends on the actual data and recipient boundary, not a tool's label.

Where recovery is relied on, the profile accounts for detection, decision, containment and recovery time with a stated margin and evidence basis. Detection latency alone does not establish recoverability. No universal dollar threshold or organizational level determines permission.

## Mandatory runtime baseline

The following obligations apply within the declared deployment boundary. A profile can add restrictions and specify conditions; it cannot waive an applicable baseline while calling the deployment conformant. A conditional obligation can be not applicable only with evidence that its precondition is absent. Stable requirement identifiers are retained across companion documents.

### R01 Declare the deployment boundary

The deployment shall identify owners, agents, systems, missions, effect classes, enforcement points, relevant dependencies and excluded paths. Its assurance profile shall name the assessed configuration and versions, including the model, tool and integration bindings on which its claims depend. An uncovered path shall not be represented as governed.

### R02 Bind accountable identities

Each executing agent, delegator and accountable principal shall be attributable. Grants shall bind the relevant subject, issuer, audience, scope, validity and delegation limits. The identity chain shall distinguish requester, authorized assignment, logical agent and workload, downstream actor, and resource where those roles exist. The record shall distinguish human-originated and agent-originated actions without guessing from names or accepting model narration as attribution.

### R03 Protect mission records

Mission identity, approved purpose, resource scope, constraints and relevant versions shall be protected from unauthorized alteration. Execution shall remain bound to the applicable record. Substitution or reuse of superseded mission and resource references shall not silently expand authority.

### R04 Verify relationships and freshness

Before a governed effect, designated authoritative sources, freshness rules and resource-side controls shall establish the relevant mission-to-resource relationship. The agent's assertion alone shall not establish it. The profile shall state the response when the required relationship cannot be established.

### R05 Declare policy and fact uncertainty

The profile shall identify factual assumptions, policy-adequacy limits, their owners, and conditions for verification, escalation or non-execution. Integrity and provenance evidence shall not be represented as proof of truth. An accepted residual risk shall not be disguised as a satisfied control.

### R06 Bound effects outside the agent

Permitted effects shall belong to enforceable classes bounded by targets, destinations, operations, data, quantities and time as applicable. General-purpose tools are permitted within these boundaries without exhaustively enumerating commands. External controls shall deny unknown, unclassified or unenforceable effects. The acting agent shall not be able to alter its governing policy or controls through direct or indirect paths.

### R07 Preserve valid authority through execution

Actions shall remain within valid authority through execution. Authority may cover a single action or recurring work within declared bounds. Expected variation within those bounds shall not require renewed human approval. Material departures shall receive the additional authorization required by policy.

Standing authorization shall not waive current validation of workload identity, integrity, authority, or applicable execution conditions. Prior successful execution alone shall not establish trust for subsequent runs.

Protected enforcement shall bind the evaluated effect and relevant conditions to what executes. The profile shall define validity windows and effect-time rechecks when delayed, queued or changed conditions could invalidate the decision. Required human authorization shall bind the approved action or bounded class, state and validity; an agent-authored narrative alone shall not establish what was approved. Material change requires the authorization specified by policy, not an automatic repeat of every human approval.

### R08 Constrain delegation across authorities

Delegation shall preserve an attributable grant chain and never grant more than the delegator can authorize. Each receiving authority shall validate issuer and audience, apply its own policy and preserve obligations, budgets and onward-delegation limits. Effective authority is constrained by every applicable mission, grant and resource-policy bound; combining credentials shall not bypass those bounds. Requesting a credential under an issuer's rules is distinct from changing those rules. Message admission or delivery grants no tool or provider execution authority by itself.

### R09 Resolve authority conflicts explicitly

Applicable authorities shall be composed by a declared rule, with accountable escalation when the conflict cannot be resolved. A deployment shall not invent authority, choose a convenient permissive rule or treat silence as consent. Relevant semantic definitions and their versions shall be coherent between decision and enforcement.

### R10 Define effective revocation

Withdrawal shall have declared effectivity and distribution bounds, covering queued, in-flight, delegated and irreversible effects. Receipt of a revocation request is distinct from enforcement. Remaining effects, unconfirmed nodes and affected outputs shall remain attributable; an unreachable recipient shall not be reported as stopped.

### R11 Control cumulative effects

Profiles shall specify applicable cumulative and sequence-sensitive limits across agents, delegations, retries, destinations and time windows. Shared counters or reservations shall prevent concurrent overspend and handoff-based resets. Cost limits and harm limits can share machinery but remain separate dimensions; one prohibited disclosure cannot be made acceptable by an unused budget.

### R12 Track obligations and omissions

Missions shall identify required outcomes, deadlines, dependencies and accountable owners of unfinished work. Governance shall detect relevant omissions and missed obligations, not assess safety solely from committed actions. A missed deadline shall not implicitly authorize a prohibited effect.

### R13 Preserve output and memory lineage

Persistent state and affected outputs shall retain provenance, mission and authority context, trust status and lifecycle controls. Revoked, poisoned or stale state shall not silently become trusted authority in a later mission. Reuse, quarantine, retirement and restoration shall preserve the relevant lineage and allow useful authorized state to remain usable.

### R14 Declare dependency failure behavior

The deployment shall identify governance dependencies, including evidence recording, and define behavior when they are unavailable or inconsistent. Ordinary effects whose required checks cannot be satisfied shall not proceed. Continued operation shall use only a pre-authorized bounded continuity mode with declared alternative controls, limits and reconciliation, never an implicit fail-open bypass. A continuity mode that cannot meet an applicable baseline shall be reported as nonconforming exceptional operation rather than normal conformance.

### R15 Interrupt with accountable continuity

Pause, cancel, revoke, quarantine, handoff and recovery shall have distinct effects where applicable. Each shall define ownership, remaining obligations, safe-state behavior and resumption conditions. Interrupted work retains its owner and deadline or an explicitly accepted change. Resumption shall revalidate authority and prevent unintended repetition of irreversible effects. Authority to contain shall not silently confer authority to restore.

### R16 Protect decision evidence

The governing path shall produce integrity-protected evidence linking mission, identities, grants, applicable policy and configuration, material inputs, approvals, decision, commit or denial, and relevant state changes. Evidence shall distinguish attempts, authorization, observed execution and outcomes. Agent narration alone shall not attest that an effect occurred. The record shall be tamper-evident and independently verifiable within the declared evidence model. Missing, altered or out-of-order records shall be detectable within that model. The profile shall identify verification roles, trust anchors, chain of custody, completeness probes and access sufficient for a verifier other than the acting agent to check the record; agent self-attestation alone is insufficient. The accountable profile owner shall document the evidence-sufficiency and minimization trade-off. Access, minimization and retention rules shall govern the record itself; raw content is retained only where justified by the declared evidence obligation.

### R17 Make governed actions auditable

Trustworthy evidence shall support reconstruction of what occurred, under whose authority and within which constraints. Auditability shall not depend on repeating external effects. Evidence limits and unknown outcomes shall remain explicit. Isolated policy-decision replay may be used where supported; it is not a universal doctrine requirement or a requirement to reproduce a stochastic workload.

### R18 Govern exceptional operation

A deliberate policy exception shall require explicit, bounded and accountable authority with scope, duration, evidence and review obligations. It shall not erase unmet controls or expand a conformance claim. An outage, pause or recovery event does not itself create exception authority. Expiry or restoration shall return work to the applicable ordinary policy, with outstanding obligations reconciled.

## Baseline applicability matrix

Applicability is assessed per obligation and path, not by dropping an entire mixed requirement. An absent precondition requires affirmative scope and configuration evidence. Always-applicable obligations remain mandatory. A profile cannot invent a not-applicable exemption.

| Requirement | Applicability | Evidence for an absent conditional precondition; remaining duty |
|---|---|---|
| R01 | Always applicable. | Boundary, exclusions, owners and configuration cannot be omitted. |
| R02 | Attribution always applies; delegation-specific links only where those roles exist. | No delegation: evidence of disabled delegation paths, not a missing identity record. |
| R03 | Always applicable. | Every governed assignment needs protected mission scope and versions. |
| R04 | Relevant relationship checks always apply. Particular relationship types depend on the mission. | A particular relationship may be absent only when the effect-path inventory proves it irrelevant; the authoritative-source/freshness rule remains. |
| R05 | Always applicable. | Declare assumptions and uncertainty even where no additional verification is chosen. |
| R06 | Always applicable. | All permitted effects need enforceable external bounds. |
| R07 | Current authority and evaluated-to-executed binding always apply. Human approval and delay rechecks are conditional. | No human-approval class or delayed path: prove its absence; current identity, integrity, authority and relevant effect-time conditions remain required. |
| R08 | Delegation obligations apply where work or authority is delegated. | No delegation or onward delegation anywhere in scope, with relevant capabilities disabled and path evidence. |
| R09 | Applicable authority composition always applies. Conflict escalation is exercised when conflict occurs. | One authority may remove cross-authority conflict cases, not the rule against invented authority or semantic inconsistency. |
| R10 | Effective withdrawal always applies. Queued, in-flight and delegated branches depend on paths. | Evidence establishes absent execution phases or delegation; revocation and residual-effect accounting remain. |
| R11 | Applicable quantity, sequence and harm bounds always apply. Shared reservations depend on shared consumable bounds. | No shared budget or concurrent spending paths: prove that absence; a prohibited single effect remains prohibited. |
| R12 | Always applicable to mission obligations and ownership. | A mission without a deadline still identifies required outcomes, dependencies and unfinished-work ownership. |
| R13 | Affected-output provenance applies whenever outputs are produced. Persistent-memory controls depend on persistence. | No persistent agent state: prove storage/reuse paths absent; output lineage and R16 evidence remain. |
| R14 | Dependency inventory and unavailable-check behavior always apply. Continuity mode is optional. | No continuity mode authorized and all such paths disabled: continuity-mode tests only are not applicable; required checks still deny or queue. |
| R15 | Effective human intervention and accountable unfinished work always apply. Each operation depends on its supported lifecycle. | Unsupported recovery or handoff paths are declared and disabled; inspect/interrupt/override and ownership are not waived. |
| R16 | Always applicable. | Evidence obligations and their verifiability model cannot be removed. |
| R17 | Always applicable. Replay is optional. | No replay implementation makes replay-specific testing not applicable; reconstructability remains mandatory. |
| R18 | Exception-path governance always applies. Exercising an authorized exception is conditional. | No exception facility: establish it is disabled across all paths and unauthorized overrides fail. Not observing an exception does not establish its absence. |

## Threats and limits

The four retained threat categories are prompt injection, intent hijacking, cascading failure and behavioral drift. They organize attention; they are not an exhaustive threat model. Profiles also consider memory poisoning, authority expansion, misleading or incomplete evidence, policy conflict, harmful sequences and omissions.

No validation check guarantees that a workload is uncompromised in every way. The profile shall identify its trusted functions, authoritative data, integrity signals and dependencies, along with their blind spots and failure behavior. Conformance concerns evidenced properties within a declared boundary and period. It is not proof of factual correctness, universal security, or endorsement of an adopter's mission.

## Companion documents

The [Assessment Companion](https://governedautonomy.org/assessment/) defines applicability, methods, verdicts and claims. The [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) rates operating capability separately. The [Institute Review and Release Process](https://governedautonomy.org/about/) governs changes to these texts.
