> **Canonical:** https://governedautonomy.org/vs/iam/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/vs/iam/ — the site is authoritative.

# Governed Autonomy vs Identity & Access Management

IAM answers: can this actor reach this system? It was never asked to answer what the actor does next.

Identity and access management is the most mature control domain in the enterprise: provisioning, authentication, authorization, role and entitlement management, certification, and deprovisioning. For human users and static service accounts, it is the foundation of trust.

Autonomous AI agents strain every one of its assumptions.

---

## What IAM does well

- Establishes **who or what** can access a resource, with strong authentication and lifecycle controls
- Models entitlements against roles: stable bundles of access that match stable job functions
- Provides the certification and audit trail regulators expect for access decisions

## Where it stops

### Identity governance

Agents are provisioned today as service accounts: shared, static-credentialed, weakly owned. An autonomous agent is not a service account: it reasons, plans, and chains actions across systems. [Agents Are Identities, Not Tools](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools) demands identity rigor IAM *can* deliver — provisioning, scoping, revocation — and most deployments don't yet apply. This part of the gap is practice, not architecture.

### Runtime behavior control

This part is architecture. IAM's control moment is the **access decision**. Attribute-based access control can evaluate a requested operation (NIST SP 800-162) and Zero Trust makes that evaluation continuous (NIST SP 800-207); what neither carries into the decision is the agent's mission, its action history across other systems, or the authority it was delegated. An identity layer consulted only at the access decision does not see what the agent then does with it: which records it reads, what it chains together, what it decides mid-mission. Integrating mission and action history into authorization is an engineering problem, not something the authorization model is unable to consume. Access control is the precondition for behavioral governance, not a substitute for it.

### System integration

IAM governs access *per system*. An agent's behavior is a *cross-system chain*: a single mission may touch identity, infrastructure, security, and data domains in one execution sequence. No entitlement model expresses "allowed to read here only in service of a mission scoped there." [Governance Must Span Systems](https://governedautonomy.org/laws/#law-3-governance-must-span-systems); access grants do not.

## The gap

> IAM can tell you an agent was authorized. On its own, it does not tell you whether what the agent is doing right now is sanctioned, or stop it mid-chain when it is not.

## Coordination, not replacement

In the Governed Autonomy model, identity systems remain authoritative for who the agent is. [Agent Identity & Lifecycle](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle) builds on them: agents as first-class identities with mission-scoped boundaries and Least Agency enforced at the mission level, feeding the runtime planes that govern what the identity actually does. Strong IAM makes Governed Autonomy implementable. It does not make it unnecessary. The same test applies here as on every comparison page: does the control mediate consequential actions, and can the governed actor bypass or disable it?
