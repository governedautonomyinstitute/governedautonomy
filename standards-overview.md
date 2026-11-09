> **Canonical:** https://governedautonomy.org/standards/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/ — the site is authoritative.

# Governed Autonomy and the Standards Landscape

Standards bodies are converging on agentic risk faster than they are converging on agentic architecture. These mappings show where each document lands.

The [category comparisons](https://governedautonomy.org/vs/) ask how Governed Autonomy relates to the existing *control stack* — IAM, security monitoring, orchestration, guardrails. This section asks a different question: how does the doctrine relate to the published *standards and guidance* that address the same problem?

The answer is usually the same shape. Standards work is strongest at the control layer — what to require, what to prohibit, what to log. It has been weakest at the architectural layer — where each control lives, which must hold simultaneously, and what a deployment must demonstrate against the mandatory baseline. That is changing: the AARM and SCIM mappings below both draw architectural boundaries, and this section records where they now reach further than a control catalogue. Each mapping below is written to be useful in both directions: what the standard supplies that the doctrine does not, and what the doctrine supplies that the standard does not.

---

## [CISA — *Careful Adoption of Agentic AI Services*](https://governedautonomy.org/standards/cisa-agentic-ai/)

The first multi-nation government guidance written specifically for agentic AI, published 1 May 2026 by six national cyber agencies. Its five risk categories independently reproduce three of the four threats this doctrine names. In our reading, the most prescriptive control-level document mapped here, including per-action policy decisions and a recommendation to limit agentic AI to low-risk, non-sensitive tasks.

---

## [OWASP — *Top 10 for Agentic Applications 2026*](https://governedautonomy.org/standards/owasp-agentic-top10/)

The broadest community statement on agentic risk: ten ranked failure modes from more than one hundred contributors. Two of this doctrine's four named threats appear in nearly its own words, independently. The mapping also records where the two documents share an open edge, and treats the Top 10's Least-Agency advice as the convergent twin of this doctrine's law.

---

## [NIST — *AI Risk Management Framework*](https://governedautonomy.org/standards/nist-ai-rmf/)

The canonical enterprise vocabulary for AI risk, written for organizational risk management rather than runtime agent control. The mapping covers the four functions, the Generative AI Profile, and the interval that matters: NIST's agent-specific overlays remain unpublished, and enterprises deploying agents today are working ahead of their own risk framework.

---

## [AARM — *Autonomous Action Runtime Management v1.0*](https://governedautonomy.org/standards/aarm/)

A Cloud Security Alliance working group specification with a DOI: nine RFC 2119 requirements for a control plane that intercepts every agent action before it executes, against a threat model of eleven classes. In our reading, the most rigorous runtime specification mapped here, and the closest convergence with this doctrine's Threat Surface — all four threats appear. The mapping records what a conformant control plane still cannot answer: what would make a particular decision correct.

---

## [IETF — *SCIM Agent Governance Extension*](https://governedautonomy.org/standards/scim-agent-governance/)

An early individual Internet-Draft giving provisioned agent identities a lifecycle state model grounded in ISO/IEC 24760-1 and an autonomy classification. The only document mapped here that is still open for comment. Its exclusions carry the finding: it rules action-level authorization out of provisioning, and defers delegated authority entirely on the grounds that the cross-protocol semantics for it do not yet exist.

---

## [DEMM-Bench — *Governance-Evidence Sufficiency*](https://governedautonomy.org/standards/demm-bench/)

A benchmark that asks whether agent-runtime records are sufficient to reconstruct a decision, rather than whether they exist. It finds that trace-present and schema-present baselines overclaim on 75% of cases, and names the failure mode the container fallacy. The mapping records the distinction that matters most here: retrospective evidence sufficiency is not a conformance verdict, and a system can score perfectly while making consistently wrong decisions, perfectly recorded.

---

## [Blueprint Alliance — *Reference Architecture for Securing AI Agents*](https://governedautonomy.org/standards/blueprint-alliance/)

A cross-industry coalition of twelve founding members announced in September 2026, publishing an open, multi-vendor reference architecture built on six principles and four questions. Each principle has a counterpart among this doctrine's Laws and Non-Negotiables, and the interoperability commitment is the cross-system span of Law 3 pursued as an engineering program. The mapping is drawn from the public announcement and records where RFC 001's proposed criteria sit alongside a reference architecture.

---

## [IMDA — *Model AI Governance Framework for Agentic AI*](https://governedautonomy.org/standards/imda-agentic-ai/)

Singapore's regulator-issued guidance for organizations deploying agents, first published January 2026 and now at Version 1.5, organized in four dimensions: bound the risks upfront, keep humans meaningfully accountable, implement technical controls, and enable end-user responsibility. Its split between an agent's action-space and its autonomy is the pair of quantities Least Agency bounds, and its preference for deterministic limits "bound by design" is the distinction Law 2 rests on. The mapping is against Version 1.5 and records where RFC 001's proposed criteria would make each recommendation testable.

---

## [NIST — *AI Agent Identity and Authorization*](https://governedautonomy.org/standards/nist-caisi-agent-standards/)

NIST's AI Agent Standards Initiative and the NCCoE concept paper on software and AI agent identity and authorization, released for comment in February 2026, together with NIST's September 2026 summary of the more than 600 responses. The paper's focus areas of identification, authorization, access delegation and logging land on Laws 1, 2 and 4 and Plane 4, and the comments converge on deterministic enforcement, authorization at the moment of action and attenuated delegation. The mapping records where RFC 001's proposed criteria would make each of the paper's questions testable.

---

## [CoSAI — *Open Delegation & Identity Standard (ODIS)*](https://governedautonomy.org/standards/cosai-odis/)

An open draft standard developed through the Coalition for Secure AI, an OASIS Open Project, for the identity, delegation and governance of AI agents across enterprise trust domains. Its framing connects the principal an agent represents, the authority it has been given and the running instance taking the action, which is Law 1, Law 4 and Least Agency in its own words. It already states normative requirements and three conformance profiles. The mapping records its four pillars and three layers against the Planes, two places where the two differ by design, and where RFC 001's proposed criteria reach past its stated identity-and-delegation scope.

---

For a survey of the wider landscape, including artifacts that do not yet have a full mapping page, see the [Standards Observatory](https://governedautonomy.org/observatory/).

---

Further mappings are planned against the EU AI Act and ISO/IEC 42001, each following the same structure: what the document establishes, where the two converge, where each is thinner, and the gap that survives compliance. When NIST's single-agent and multi-agent control overlays publish, they will be mapped criterion by criterion.
