> **Canonical:** https://governedautonomy.org/vs/siem/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/vs/siem/ — the site is authoritative.

# Governed Autonomy vs Security Monitoring

SIEM, SOAR, and detection answer: what happened, and how do we respond? Autonomous agents force a harder question: what is happening, and should it continue?

Security monitoring is the enterprise's record of truth — telemetry collection, correlation, detection, and increasingly automated response. Against human-speed adversaries and deterministic software, detect-and-respond is a workable control model.

Against autonomous agents, the timeline collapses.

---

## What monitoring does well

- Cross-domain visibility: one place where firewall, endpoint, identity, and application telemetry converge
- Detection logic refined over decades — correlation, anomaly identification, threat intelligence
- Forensic reconstruction and the evidentiary record that audit and incident response depend on

## Where it stops

### Identity governance

Monitoring sees *events*, not *actors with missions*. If agent actions are not emitted as first-class telemetry tied to a governed identity, the most consequential actor in the environment is also the least visible one. Most agent behavior today produces no security telemetry at all.

### Runtime behavior control

Detection is, by definition, after the fact. An autonomous agent executing a corrupted plan completes it in seconds — a **Cascading Failure** propagates across interconnected workflows before the first alert is triaged. [Enforce at Runtime](https://governedautonomy.org/laws/#law-2-enforce-at-runtime) names the requirement: enforcement before each effect, not detection after it. And automated response carries its own trap: a SOAR platform empowered to act autonomously is itself a privileged agent, and ungoverned, it becomes the next incident.

### System integration

Monitoring aggregates many systems' logs — but aggregation is not enforcement. Seeing an agent's actions across domains is not the same as holding authority to allow, deny, or escalate them across those domains.

## The gap

> Monitoring can reconstruct exactly how the agent caused the incident. It cannot be the reason the incident never happened.

## Coordination, not replacement

In the Governed Autonomy model, security platforms supply the risk context that runtime enforcement decisions consume, and agent behavior itself becomes first-class telemetry feeding them. [Human Oversight, Audit & Traceability](https://governedautonomy.org/architecture/#plane-4-human-oversight-audit-traceability) is built on monitoring's strengths: the evidentiary record, reconstruction of what happened, and the interfaces through which [Humans Retain the Right to Intervene](https://governedautonomy.org/laws/#law-5-humans-retain-the-right-to-intervene). Detection remains essential. It is the floor of governance, not the ceiling.

## The test for any control

Whatever its vendor calls it: does the control mediate consequential actions, and can the governed actor bypass or disable it? A product sold as a guardrail that intercepts actions before they execute is a Plane 2 mechanism regardless of its label. A control the agent can update away, or that sits in only one system, is not governance, whatever it is called. What makes a control part of Governed Autonomy is that it is external to the agent, cannot be modified by the agent, and spans the systems the agent touches ([Law 2](https://governedautonomy.org/laws/#law-2-enforce-at-runtime), [Law 3](https://governedautonomy.org/laws/#law-3-governance-must-span-systems)).
