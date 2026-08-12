> **Canonical:** https://governedautonomy.org/maturity/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy Maturity Model

Where is your organization on the path to governed autonomy?

The Governed Autonomy Maturity Model gives enterprises a framework to assess their current state, identify gaps, and sequence their adoption of Governed Autonomy principles. It maps directly to the 5 Laws, 5 Architectural Planes, and 6 Framework Pillars.

There are three maturity levels. Each one is independently meaningful. Level 1 is not just a stepping stone, it is a defensible operational posture for organizations in early agentic AI deployment.

-----

## Level 1: Identified

***You know what your agents are.***

  - Agents are inventoried and registered as enterprise identities
  - Each agent has a defined owner, a provisioned credential, and a revocation path
  - Mission scope is documented: what the agent is authorized to accomplish
  - Least Agency boundaries are defined: minimum decision scope established per mission
  - Basic audit logging is in place

At Level 1, you have eliminated the most dangerous condition in agentic AI: unknown agents operating with unknown scope. You cannot govern what you cannot see.

**Law alignment:** Law 1, Agents Are Identities, Not Tools

-----

## Level 2: Governed

***You control what your agents do.***

  - Behavioral policy is defined and enforced across systems
  - Runtime enforcement intercepts and evaluates agent actions during execution
  - Human oversight interfaces are operational: inspect, interrupt, and override are available
  - Cross-system governance is active: no single domain governs in isolation
  - Least Agency is enforced: agents operate with minimum decision scope required for their mission
  - Threat surface monitoring is active for prompt injection and intent hijacking

At Level 2, authorization and governance are both present. The gap identified in the Governed Autonomy Declaration is closed. You have moved from *"we authorized the agent"* to *"we govern the behavior."*

**Law alignment:** Laws 2, 3, and 5

-----

## Level 3: Continuous

***Your governance evolves as fast as your agents do.***

  - Every handoff type (delegation, orchestration, tool invocation, subagent spawning) is explicitly governed with defined, enforced, and revocable trust boundaries
  - Behavioral drift detection is active: deviations from sanctioned behavior identified in real time
  - Full threat surface coverage: prompt injection, intent hijacking, cascading failure, and behavioral drift
  - Governance policy evolves continuously based on observed agent behavior
  - Full forensic reconstruction available for every agent action across every system
  - Governance scales with agent deployment, with no manual bottlenecks

At Level 3, governance is not a control layer. It is an operating characteristic of the system. Agents scale. Governance scales with them.

**Law alignment:** All 5 Laws, full doctrine operational

-----

## Maturity Summary

| Level | Name       | What It Means                            | Primary Laws |
| ----- | ---------- | ---------------------------------------- | ------------ |
| 1     | Identified | You know what your agents are            | Law 1        |
| 2     | Governed   | You control what your agents do          | Laws 2, 3, 5 |
| 3     | Continuous | Your governance evolves with your agents | All 5 Laws   |

> The goal is not to reach Level 3 immediately. The goal is to never deploy agents beyond your current governance maturity.
