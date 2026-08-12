> **Canonical:** https://governedautonomy.org/what-is-governed-autonomy/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# What Is Governed Autonomy?

The term the industry converged on. The definition it still lacks.

> **Governed autonomy** is the operating state in which autonomous AI agents plan and execute freely inside bounds that are explicitly defined, continuously enforced at runtime, and revocable by humans at any moment. Autonomy is what the agent contributes. Governance is what the enterprise retains. Neither is negotiable.

## A term in wide circulation

Since late 2025, "governed autonomy" has appeared across the industry: in vendor operating models for finance and security operations, in consultancy frameworks for the agentic enterprise, in analyst research, in academic work on agent safety, and in glossaries of agentic identity. The usages differ in scope and motive. They agree on the essentials: autonomy is a dial rather than a switch; policy must be encoded in the runtime rather than appended after it; every agent action must be explainable, auditable, and reversible; and the human role shifts from approving individual transactions to governing behavior.

That convergence is evidence. When vendors, analysts, and researchers reach independently for the same phrase, the requirement underneath it is real. This doctrine treats independent convergence the same way everywhere it appears: documented, not claimed. See the [standards landscape](/standards/) for the method.

## What the circulating usages cannot do

Nearly every published use of governed autonomy is an assertion: a product that promises it, an operating model that describes it, a talk that recommends it. None of them can be failed. A description of governed autonomy tells you what good looks like. It cannot tell you whether a given deployment has it, and it offers no way to be proven wrong.

That is the difference between a phrase and a standard. A definition you cannot test is marketing. A standard you can fail is a discipline.

## The standard

The Governed Autonomy Doctrine defines the term operationally, in four layers that can each be checked against a real deployment:

  - [The 5 Laws](/laws/) state what must be true for any governed agent: agents are identities, not tools; enforcement happens at runtime; governance spans systems; trust does not travel; humans retain the right to intervene.
  - [The Architecture](/architecture/) places control: five planes covering agent identity and lifecycle, execution and tool governance, policy and compliance, human oversight and traceability, and multi-agent trust.
  - [The Framework](/framework/) sequences implementation: six pillars from agent identity through multi-agent governance.
  - [The Maturity Model](/maturity/) stages the journey: Identified, Governed, Continuous. The goal is not to reach Level 3 immediately. The goal is to never deploy agents beyond your current governance maturity.

A fifth layer is proposed and open for comment: [RFC 001, the Conformance Layer](/rfc/v4-conformance-layer/), defines twenty-nine testable, mechanism-agnostic criteria that any implementation can be assessed against, and can fail. It is the first attempt to make governed autonomy falsifiable rather than aspirational.

> Validation test: if runtime enforcement of autonomous AI agent behavior is removed and the system would still meet its objective, it is not governed autonomy.

## Provenance

This doctrine did not begin with the phrase. Development began in late 2025 with work on prompt injection and the trustworthiness of agent-retrieved data, matured through the arrival of largely ungoverned agent scaffolding in early 2026, and was first published as a public doctrine in May 2026, versioned and revised in the open. The August 2026 renaming matched the doctrine to its own oldest language: the Maturity Model has described "the path to governed autonomy" since its first publication. Every substantive change is recorded in the [changelog](/changelog/).

Where to start: read the [Declaration](/), then the [5 Laws](/laws/). To assess a real deployment, start with [RFC 001](/rfc/v4-conformance-layer/).
