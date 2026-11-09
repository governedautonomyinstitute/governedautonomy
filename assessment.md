> **Canonical:** https://governedautonomy.org/assessment/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/assessment/ — the site is authoritative.

# Governed Autonomy Assessment Companion v4

Version 4 | Released 1 November 2026 | Governed Autonomy Institute

This companion specifies assessment of the [runtime baseline](https://governedautonomy.org/doctrine/). It is separate from per-job runtime enforcement and from [organizational maturity](https://governedautonomy.org/maturity/). Its publication does not certify a deployment. A second assessor is a technique for evaluating the method, not a requirement for two people or models to approve every job.

## Assessment unit and profile

An assessment concerns a named deployment, configuration, boundary, action scope, profile version and evidence period. Before evaluating it, record the accountable owner and risk owner; agents and resources; enforcement and trusted functions; models, tools and integration versions; relevant policy and authority sources; standing and single-action grants; permitted effect classes; exclusions; and change and revocation behavior.

The profile states risk-specific limits before observations are scored. These include applicable freshness and integrity signals, decision validity, cumulative reservations, deadlines, revocation distribution and effectivity, continuity duration and quotas, evidence obligations, retention, and utility targets. An absent required limit is not an assumed generous default. A sandbox or a simulation has its own boundary and cannot inherit a claim about production.

Classify effects as permitted within standing bounds, requiring additional authorization, or prohibited. State the basis for sensitivity, affected parties, magnitude, recoverability, time to harm and context. Record approval of boundary changes outside the acting agent. If an effect requires a human decision under policy, identify what was approved, by whom and for which action or bounded class and validity period. Repeated jobs with expected variation do not require another human decision merely because they repeat.

## Evidence states and criterion verdicts

Evidence state and criterion verdict are different fields. A bare null shall not stand for both an absent control and unavailable evidence.

| Evidence state | Meaning | Assessment consequence |
|---|---|---|
| observed | The relevant condition or behavior was examined or tested with a stated basis. | Score against the requirement and scope; observation alone is not a pass. |
| confirmed_absent_control | Evidence affirmatively establishes that an applicable required control is absent. | Fail that criterion. |
| confirmed_missing_required_record | A specified record was required and the assessed collection/completeness basis establishes its absence. | Fail the affected evidence requirement; do not infer an unrelated execution property without evidence. |
| unavailable_evidence | Collection, access or supplied evidence is insufficient to decide whether the property holds. | Not assessed for the affected property; it cannot support a conformance claim. |
| precondition_absent | Evidence establishes that the conditional behavior does not occur anywhere within the declared scope. | Not applicable with rationale and scope evidence. |

Use **pass**, **fail**, **not_assessed** and **not_applicable** for each applicable criterion. Split mixed-scope results by path, action class or subrequirement; do not average them into a pass. A verified failure remains a failure even when other evidence is unavailable. Lack of evidence is not positive evidence of safety.

This rule separates a control that is absent from evidence that is unavailable. A bare null no longer stands for both.

## R19 Support assurance claims with evidence

Claims about corroboration, independent assurance or a tested method shall have evidence appropriate to the claim, including shared dependencies and limitations. Separate sessions, vendors or organizations do not by themselves establish independent failures. The doctrine does not mandate multiple models or a second reviewer for every action.

If corroboration is used as a risk control, state the authenticated facts shared, potentially contaminated reasoning isolated, decision roles, common dependencies, case coverage, repetitions and uncertainty. Measure individual and joint unsafe approvals and false denials on held-out cases where such rates are claimed. Zero observed failures do not establish zero risk, and a correlation statistic with zero variance is not a measured independence result.

## R20 Define and apply an assessment method

Each criterion shall have applicability conditions, evidence requirements, an examination or test method, expected outcomes, failure rules and retest triggers. A yes/no question is insufficient if a system could violate the property and still answer yes. Preserve the distinction between a failed property, unavailable evidence and an absent precondition.

Use the matrix below as the minimum method structure, tailored by the declared profile. It is assessment work, not a requirement to perform every adversarial test before each ordinary job.

| Baseline | Examine | Permitted case and challenge | Evidence needed |
|---|---|---|---|
| R01 | Boundary and effect-path inventory, exclusions and versions. | Complete an authorized workflow; attempt an excluded or unmediated path. | Path coverage, enforcement points and honest exclusions. |
| R02 | Identity and grant chain, issuer, audience and validity. | Valid actor succeeds; unknown actor, wrong audience or expired grant fails. | Attributed request, grant and actual effect or denial. |
| R03 | Protected mission record and change control. | Current approved assignment succeeds; mutate mission/resource or reuse superseded scope. | Mission versions and binding through execution. |
| R04 | Relationship source, freshness and resource-side check. | Correct current association succeeds; wrong-case or stale association follows declared denial/escalation. | Source versions, timestamps, relationship decision and effect. |
| R05 | Fact and policy assumptions, owners and uncertainty rules. | Present an intact but incorrect authoritative association. | Honest limitation and exercise of declared verification/escalation, without claiming truth was proven. |
| R06 | Effect classes and external controls, including indirect reach. | Bounded general-purpose tool succeeds; alternate destination, protocol, redirect or authority-changing path is stopped. | Actual effective boundary and enforcement, beyond tool descriptions. |
| R07 | Standing and action-specific authorization, integrity/freshness signals and effect-time validity. | Vary an in-scope recurring job; substitute parameters, expire authority or change policy before effect. | Approved scope, current checks, bound effect, material-change response and human decisions only where required. |
| R08 | Resource authorities, delegation entitlement and onward limits. | Valid narrowed delegation succeeds; amplify expiry/scope, change audience or drop an obligation. | Independent receiving grant, chain, obligations and budgets; delivery distinct from execution. |
| R09 | Policy composition, meanings and escalation authority. | Two legitimate rules conflict; an untrusted issuer asserts an override. | Stated precedence, definitions/versions and accountable resolution. |
| R10 | Revocation contract for each execution phase and authority. | Withdraw before admission, while queued, in flight and after an irreversible commit. | Request/receipt/enforcement times, final permitted effects, unreachable nodes and residuals. |
| R11 | Shared bounds, reservations, sequence state and retry keys. | Complete work below the bound; cross it through concurrency, retries and delegation. | Reservations and effects reconcile without reset or duplicate spending; negative quantities cannot create budget. |
| R12 | Obligations, deadlines, dependency and fallback ownership. | Interrupt or abandon required work near a deadline. | Remaining work, owner acknowledgment, deadline and escalation; no unauthorized effect implied. |
| R13 | State and output provenance, trust labels and lifecycle. | Reuse clean state; seed poisoned/stale state and revoke an authoring mission. | Cross-shift read control, affected lineage, quarantine and authorized restoration. A supplied label is not proof of a detector. |
| R14 | Governance dependencies and pre-authorized continuity contract. | Disable the recorder while policy stays healthy; separately disrupt identity, clock or network. | Declared denial, queue or bounded alternative controls; quota consumption, evidence and reconciliation. |
| R15 | Intervention, handoff and restoration contracts. | Halt running work; make the owner unavailable; resume under valid authority. | Safe state, residual effects, accountable handoff, deadline and duplicate-effect protection. |
| R16 | Evidence writer, integrity/completeness model, access and retention. | Follow a valid effect; remove, alter, reorder or suppress a required record. | Actual effect versus attempt, detectable alterations/omissions and minimization/sufficiency rationale. |
| R17 | Cross-system reconstruction instructions and evidence limits. | A reviewer reconstructs a mission from its bundle without repeating effects. | Actor, authority, policy, decision, observed result and unknowns. Replay, if used, is separately scoped and isolated. |
| R18 | Exception authority, expiry, obligations and claim treatment. | Compare a valid exception with an outage, pause, expired exception and unauthorized override. | Bounded authority and review; no inferred exception or disguised failed baseline. |

For relevant state-changing effects, test the boundary between evaluated parameters and committed effects, not merely that the number of decisions equals the number of calls. For recording completeness, use known probes and state the paths and omissions the experiment can detect. Querying several evidence stores does not by itself defeat a coherent reconstructable record.

## R21 Report assessment limits and disagreements

An assessment shall record assessor roles, interests, shared dependencies, access limits and unresolved disagreement. In a method-comparison exercise, assessors first record judgments against the same frozen bundle separately, then reconcile by evidence or criterion clarification. Preserve initial judgments. Do not average disagreement into adoption or erase a failed case after correction.

A technical reviewer checks the release text and evidence against requirements. An assessor evaluates a declared deployment. A corroborator is a runtime risk control when required by a profile. These roles do not substitute for one another.

## R22 Measure useful mission completion

Validation shall measure legitimate completion and human burden alongside prohibited-effect prevention. Report denominators, coverage and applicable acceptance thresholds, including elapsed time, cost, interventions, false denials and interrupted or abandoned work. Keep safety and utility results separate; a composite score shall not hide an unsafe commit.

Include permitted, prohibited, boundary and fault cases. Distinguish attempted, authorized, dispatched, committed and observed effects. A disabled agent can block all prohibited work while completing none of its mission. It has not thereby demonstrated useful runtime governance.

## R23 Make precise claims

Each claim shall identify criterion and profile versions, deployment or product scope, date, evidence class, assessor, limitations and assessment status. Use these distinct evidence classes: documented design, examined configuration, synthetic behavior, and operated-deployment behavior. A product may provide or enable a capability; only a specified operated deployment can support a deployment claim. Synthetic fixtures demonstrate the fixture behavior actually observed, not the estate or all possible implementations.

| Claim state | Required basis |
|---|---|
| Conformant within the declared scope | All applicable baseline and profile requirements pass, with no unknown required property concealed. |
| Equivalent control accepted | An assessor who is not the deployment's accountable owner accepts evidence that an alternative control meets the same requirement; record rationale, scope and validity, and include this qualifier in the claim. An adopter assessing its own deployment may record the alternative control but shall label the claim self-assessed and shall not use this state. |
| Nonconformant, risk accepted | One or more applicable requirements fail; an accountable owner accepts a bounded operational risk. It is not conformance. |
| Not assessed or assessment incomplete | Required evidence or coverage is insufficient. Do not infer permission or a pass. |

Publishing these rules does not make the Institute a certification or accreditation body. A self-assessed claim identifies itself as such. Registration or endorsement shall not be inferred from use of the template.

## R24 Control profile changes and retests

Profiles shall declare risk bounds and ownership before assessment. Changes to models, prompts where relevant, tools, integrations, authority sources, policies, evidence mechanisms or operating assumptions shall trigger impact review and proportionate retesting. Identify the model/tool configuration actually observable; an unobservable provider version remains an evidence limitation. Prior results shall not silently cover an altered boundary.

Retain unaffected results only with a documented rationale. Link corrected failures to their original evidence and retests. Reassessment can be targeted; a release does not require rerunning unrelated tests when the change cannot affect them.

## Evidence bundle and reporting

A report contains a manifest; the frozen profile and configuration; case definitions and expected outcomes; mission and grant records; decisions, effects and relevant dependency events; evidence states and verdicts; limits and exclusions; metrics and denominators; exceptions; disagreements; and correction/retest links. Sensitive evidence is minimized and access-controlled. Exact capture is used where necessary for the claim, not as a universal demand to retain all raw prompts and retrieved data.

Deterministic policy replay, when supported, records preserved inputs, state, versions and integrity checks, runs in isolation, and never repeats external effects. Returning a stored answer is reconstruction, not proof that fresh model execution reproduces it. Workload re-execution is a separate experiment with separate authorization and risk.

## Publication and deployment are separate decisions

The specification can be published with accurate limits before full-estate trials. A claim about a tested assessment method must match completed method testing. A deployment claim needs the named deployment's evidence. Full-estate trials, a DOI and an extended consultation period are not automatic prerequisites for publishing the specification. Stronger wording cannot substitute for evidence.
