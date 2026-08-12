> **Canonical:** https://governedautonomy.org/standards/owasp-agentic-top10/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy and the OWASP Top 10 for Agentic Applications

A hundred-contributor community ranked what goes wrong with agents. A ranking tells you what to defend against. It does not tell you where the defenses live, or when they must all hold at once.

In December 2025, the OWASP GenAI Security Project's Agentic Security Initiative published the *OWASP Top 10 for Agentic Applications 2026*: ten ranked risk categories for autonomous agents, developed with more than one hundred contributors and released under an open license. It is the broadest community statement yet on agentic risk, and its companion documents (a threat taxonomy, a multi-agent threat-modeling guide, a securing-applications guide) give it unusual depth. This page is a mapping, not a rebuttal: the two bodies of work were developed independently and converge on the substance. Where they differ, they differ in layer. The Top 10 enumerates and ranks the failure modes. The doctrine states the architecture in which the corresponding controls live, and proposes the criteria by which an implementation can be shown to hold.

## What the Top 10 establishes

Ten risks, each with attack scenarios and mitigations, mapped to the initiative's underlying threat taxonomy. In the doctrine's terms:

| OWASP entry                                | What it names                                                                           | Where it lands in this doctrine                                                                                                                                                                                                                |
| ------------------------------------------ | --------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ASI01 Agent Goal Hijack                    | An agent's objectives redirected through content it cannot distinguish from instruction | **Prompt Injection** and **Intent Hijacking** on the Threat Surface; the treat-content-as-data conformance criterion in [RFC 001](/rfc/v4-conformance-layer/)                                                                                  |
| ASI02 Tool Misuse and Exploitation         | Legitimate tools misused inside authorized privilege                                    | [Plane 2, Execution & Tool Governance](/architecture/#plane-2-execution-tool-governance); [Enforce at Runtime](/laws/#law-2-enforce-at-runtime)                                                                                                |
| ASI03 Identity and Privilege Abuse         | Delegation chains and inherited privilege without a distinct, governed identity         | [Agents Are Identities, Not Tools](/laws/#law-1-agents-are-identities-not-tools); [Plane 1](/architecture/#plane-1-agent-identity-lifecycle); Least Agency                                                                                     |
| ASI04 Agentic Supply Chain Vulnerabilities | Compromised tools, models, registries, and agent interfaces                             | Tool provenance and version binding under Plane 2; partly an acknowledged open edge of the doctrine (see below)                                                                                                                                |
| ASI05 Unexpected Code Execution            | Generated code escalating to host compromise                                            | Action-level interception under Plane 2; deny-by-default at effect granularity in RFC 001                                                                                                                                                      |
| ASI06 Memory and Context Poisoning         | Corrupted stored context biasing future behavior                                        | **Behavioral Drift** on the Threat Surface; the persistent-state governance criterion added in RFC 001 revision 2                                                                                                                              |
| ASI07 Insecure Inter-Agent Communication   | Spoofed, intercepted, or manipulated agent-to-agent exchange                            | [Trust Does Not Travel](/laws/#law-4-trust-does-not-travel); [Plane 5](/architecture/#plane-5-multi-agent-trust-delegation)                                                                                                                    |
| ASI08 Cascading Failures                   | A single fault amplifying across agents and workflows                                   | **Cascading Failure** on the Threat Surface, near-verbatim; halt-and-escalate scope under Plane 5                                                                                                                                              |
| ASI09 Human-Agent Trust Exploitation       | Automation bias and persuasive explanation defeating human review                       | [Humans Retain the Right to Intervene](/laws/#law-5-humans-retain-the-right-to-intervene), and the authorization-fidelity concern RFC 001 records: an approval based on the agent's own description of the action is laundering, not oversight |
| ASI10 Rogue Agents                         | Agents departing from intended function or authorized scope                             | **Behavioral Drift**; mid-mission revocation and decommissioning criteria under Plane 1                                                                                                                                                        |

Two of the four threats named on this doctrine's [Declaration](/) appear in the Top 10 in nearly the doctrine's own words: cascading failure by name, behavioral drift as the substance of ASI06 and ASI10. The Threat Surface was locked in May 2026; the Top 10 was published in December 2025; neither document derives from the other. As with the [CISA mapping](/standards/cisa-agentic-ai/), the convergence is the useful finding: independent bodies keep arriving at the same failure modes because the failure modes are real.

## Least Agency, in both documents

The Top 10's introduction extends least privilege with what it calls Least-Agency: advice to avoid unnecessary autonomy, because agentic behavior deployed where it is not needed expands the attack surface without adding value. This doctrine carries the same principle at a different altitude: [Least Agency as a law](/laws/#law-1-agents-are-identities-not-tools) (no more decision scope, tool access, or action authority than the mission demands) with a conformance criterion in RFC 001 written so that an assessor can attempt to falsify it. The two usages are compatible and convergent: OWASP states the advice; this doctrine states the test. Readers arriving from the OWASP corpus should treat the terms as the same principle, and this page as the citation for the difference in role.

## Where each is thinner

### What the Top 10 supplies that this doctrine does not

Ranked prevalence. Attack scenarios grounded in observed incident patterns. Per-risk mitigation catalogs. A threat taxonomy (the initiative's T-series) that this doctrine has no equivalent of and does not need to duplicate. And a form of legitimacy no solo publication can manufacture: more than one hundred named contributors and an open review process. On threat enumeration, the Top 10 is the stronger document, and this doctrine defers to it.

### What this doctrine supplies that the Top 10 does not

A ranked list is evaluated one risk at a time, and its mitigations attach to risks, not to an architecture. The Top 10 does not say which controls must hold simultaneously for a single agent action to be sanctioned, where each control lives relative to the others, how governance spans the systems an agent crosses, or how an organization decides it is ready to widen an agent's autonomy. Those are the questions the [five Planes](/architecture/), the [six Pillars](/framework/), and the [Maturity Model](/maturity/) exist to answer, and the questions RFC 001 proposes to make testable. ASI01 and ASI09 together make the doctrine's own argument: a goal-hijacked agent that presents a persuasive account of a permitted action passes every individually evaluated control. Only criteria read together, at the moment of action, catch it. That is the Simultaneity Requirement, and it is an architectural property, not a mitigation.

## The open edge both documents share

ASI04 reaches into the supply chain beneath the agent: models, tools, registries, update channels. RFC 001 carries provenance and version binding for tools, and records as an open question whether model provenance and training-data integrity belong inside a governance conformance layer at all. The honest current answer is that neither document fully governs the layer beneath the agent, and the doctrine says so rather than mapping the gap away.

## Complementary layers, not competing standards

Use the Top 10 to know what to defend against and to brief the teams who will build the defenses. Use the doctrine to decide where each defense lives, which must hold at once, and how far autonomy can safely extend today. One further note for the record: the phrase "governed autonomy" appears nowhere in the Top 10 or its companion documents. The state those documents are working to make reachable is the state this doctrine names, defines, and proposes to make testable.

## Primary sources

  - [OWASP Top 10 for Agentic Applications 2026](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/) (OWASP GenAI Security Project, Agentic Security Initiative; December 2025; CC BY-SA 4.0)
  - [Agentic AI: Threats and Mitigations](https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/) (the underlying threat taxonomy)
  - [Multi-Agentic System Threat Modeling Guide](https://genai.owasp.org/resource/multi-agentic-system-threat-modeling-guide-v1-0/)
  - [Securing Agentic Applications Guide](https://genai.owasp.org/resource/securing-agentic-applications-guide-1-0/)
