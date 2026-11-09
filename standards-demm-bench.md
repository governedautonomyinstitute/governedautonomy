> **Canonical:** https://governedautonomy.org/standards/demm-bench/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/demm-bench/ — the site is authoritative.

# Governed Autonomy and DEMM-Bench

Most audit requirements ask whether a record exists. DEMM-Bench asks whether the records that exist can answer a governance question about a specific decision. Those are different tests, and the second is much harder to pass.

**Note on criterion identifiers.** Identifiers such as C1.1 or CX.1 refer to [RFC 001 revision 2](https://governedautonomy.org/rfc/v4-conformance-layer/), a historical proposal preserved as published. They are not v4 requirements. The current requirements are the [baseline R01 to R18](https://governedautonomy.org/doctrine/) and the [Assessment Companion](https://governedautonomy.org/assessment/). This mapping has not yet been restated against them.

In June 2026 a benchmark paper, *DEMM-Bench: A Cross-Regime Benchmark for Agent-Runtime Governance-Evidence Sufficiency*, was published as a preprint ([arXiv:2606.20634](https://arxiv.org/abs/2606.20634), DOI [10.48550/arXiv.2606.20634](https://doi.org/10.48550/arXiv.2606.20634)). Grounded in a Decision Evidence Maturity Model, it evaluates whether records emitted across eight evidence regimes are *sufficient to reconstruct decision-level properties*, rather than simply present.

This page is a mapping, not a rebuttal. DEMM-Bench is, to our knowledge, the first published instrument to make audit adequacy falsifiable, and it lands squarely on the plane this doctrine names [Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability). On *how to measure whether your evidence is any good*, this doctrine defers to it.

**A note on scope.** This is a preprint benchmark, not a standards-body specification, and it should not be cited as one. Its contribution is a method and a dataset. What makes it load-bearing here is not its status but its finding.

## What DEMM-Bench establishes

The benchmark normalises eight evidence regimes through adapters — traces, ledgers, provenance graphs, policy logs, delegation tokens, cache events, tool-firewall records, and schemas — then asks property questions over eight dimensions of a decision: **actor, authority, action, policy, decision basis, resource touch, lifecycle context, and verification strength**. Eight deterministic degradation conditions are applied, and performance is scored across 64 published cases.

Two metrics carry the argument. **Property Sufficiency Accuracy** measures how often an evidence substrate genuinely answers the property question. **Overclaim Rate** measures how often it appears to answer and does not, and it is the primary diagnostic and the more useful of the two.

The headline result is the reason this page exists. Trace-present and schema-present baselines **overclaim on 75% of cases**; ledger-present overclaims on 50%. Three quarters of the time, having the trace is mistaken for being able to answer the question.

The paper names this failure mode the **container fallacy**: treating the presence of an evidence container as an answer to a governance question.

## Where the two converge

The container fallacy is this doctrine's own argument, arrived at independently and applied to the audit plane. This site has held from its [Declaration](https://governedautonomy.org/) onward that a definition you cannot test is marketing and a standard you can fail is a discipline. DEMM-Bench makes the same move one layer down: a log you cannot fail is not evidence, it is furniture. The convergence is not vocabulary. It is the same epistemic standard applied to a surface this doctrine had asserted rather than measured.

The eight properties also map cleanly onto the architecture, which is worth stating because it is not a coincidence. Both documents are decomposing the same object.

| DEMM property | Where it lands in this doctrine |
|---|---|
| **Actor** | [Agents Are Identities, Not Tools](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools); [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle). Reconstructing *which* agent acted presupposes the agent was an identity when it acted. |
| **Authority** | [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle) for the grant, [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) for what survives a handoff. See the open edge below. |
| **Action** and **resource touch** | [Plane 2, Execution & Tool Governance](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance) |
| **Policy** and **decision basis** | [Plane 3, Policy & Compliance Engine](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine). Decision basis is the harder of the two and the one substrates most often fail. |
| **Lifecycle context** | [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle); the provisioning and decommissioning states the [SCIM extension](https://governedautonomy.org/standards/scim-agent-governance/) is specifying from the identity end. |
| **Verification strength** | [Plane 4](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability), and the closest published treatment of what this doctrine means by traceability that can be relied on. |

## Where each is thinner

### What DEMM-Bench supplies that this doctrine does not

A measurable test. This doctrine requires that agent behaviour be auditable and that oversight be exercisable; it does not say how an organisation would discover that its audit trail cannot actually support either. DEMM-Bench does, with a dataset, construction-oracle labels, baselines, adapters, and a reproducible score. It also supplies the more uncomfortable half: a number for how often practitioners believe they have evidence and do not. That is a contribution this doctrine should adopt rather than restate.

### What this doctrine supplies that DEMM-Bench does not

The distinction here is precise and it matters more than it first appears, so it is stated plainly rather than left to inference.

**DEMM-Bench scores retrospective evidence sufficiency. It does not issue a conformance verdict.** It asks: given what was recorded, can an investigator reconstruct who acted, under what authority, on what basis? That is a forensic question, asked after the fact, about one decision. It does not ask whether the decision was *correct*, whether the governing policy was adequate, or whether the implementation that produced it conforms to any standard. A system can achieve a perfect Property Sufficiency Accuracy score while making consistently wrong decisions, perfectly recorded.

[RFC 001](https://governedautonomy.org/rfc/v4-conformance-layer/) is proposed against the other question: criteria for what a correct decision would have to satisfy, stated so an assessor can attempt to falsify a claim. Reconstructability is a precondition for that assessment, not a substitute for it. Both are needed, they are not the same instrument, and a reader who meets DEMM-Bench first will reasonably assume the ground is already covered.

Two further surfaces sit outside the benchmark's frame by design. There is no **organizational maturity** dimension: DEMM-Bench measures the evidence a system produces today, not an organization's capability to sustain governance, which the [Organizational Maturity Evaluation](https://governedautonomy.org/maturity/) describes. And it is an **evaluation instrument, not a control**. It scores substrates after they exist and specifies nothing about enforcing anything at runtime, which is [Law 2](https://governedautonomy.org/laws/#law-2-enforce-at-runtime).

## Multi-agent delegation: still open

The benchmark's *authority* property is retrospective attribution, establishing from the record under what authority an actor acted. It is not a treatment of what authority survives when one agent delegates to another at runtime, and the benchmark does not claim it is. Delegation tokens appear as one of the eight evidence regimes, so DEMM-Bench can score whether a delegation was *recorded legibly*. Whether the delegation was *legitimate*, and what scope should have travelled with it, remains outside the frame.

That is [Trust Does Not Travel](https://governedautonomy.org/laws/#law-4-trust-does-not-travel) and [Plane 5](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation). It is now one of six independent published artifacts that govern single-agent runtime behaviour and leave cross-agent delegated authority open. At some point a gap that survives six independent attempts stops being an oversight and starts being a research problem. The [Standards Observatory](https://governedautonomy.org/observatory/) tracks which artifacts have reached it.

## Complementary instruments, not competing ones

Use DEMM-Bench to find out whether your agent-runtime evidence can answer a governance question at all. Use this doctrine to decide which questions must be answerable, at which plane, and which baseline requirements apply. An evidence substrate can be sufficient and the governance it evidences still wrong. Measuring the record does not adjudicate the decision.

## Primary sources

- [arXiv:2606.20634](https://arxiv.org/abs/2606.20634), *DEMM-Bench: A Cross-Regime Benchmark for Agent-Runtime Governance-Evidence Sufficiency* (preprint, June 2026)
- DOI [10.48550/arXiv.2606.20634](https://doi.org/10.48550/arXiv.2606.20634)

*Mapped 2 September 2026 against the June 2026 preprint. If the benchmark is revised or published at a venue, this page is re-checked against the revision rather than defended.*
