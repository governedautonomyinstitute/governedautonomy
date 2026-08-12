> **Canonical:** https://governedautonomy.org/architecture/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy Architecture

The runtime control and enforcement architecture for governing autonomous AI agents as first-class identities across enterprise systems.

Governed Autonomy defines where control sits, what layers exist, how runtime enforcement works, and how existing enterprise systems integrate into a unified governance model for AI agent behavior.

Governed Autonomy does not replace existing systems. It defines how they must work together in the presence of autonomous agents.

-----

## The Architectural Gap

Today's enterprise stack is built on established control domains: Identity systems, Security systems, Orchestration systems, and Data governance systems.

These systems assume:

  - Execution paths are known or deterministic
  - Behavior is bounded by human-authored workflows
  - Enforcement can occur before or after execution, but not continuously during autonomous decision-making

Autonomous AI agents violate all three assumptions. They introduce a requirement that no existing system provides: **continuous governance of behavior at runtime across multiple enterprise domains simultaneously.**

This is the distinction at the core of Governed Autonomy:

> Authorization answers: *can this agent act?*  
> Governance answers: *what is this agent doing, right now, and is that behavior sanctioned?*

-----

## The 5 Architectural Planes

### Plane 1: Agent Identity & Lifecycle

  - AI agents as first-class enterprise identities
  - Credential lifecycle management (including ephemeral credentials)
  - Cross-system identity correlation
  - Mission-scoped access boundaries
  - Agent registry: provisioning, rotation, and revocation

**Law alignment:** Law 1, Agents Are Identities, Not Tools. Plane 1 is the architectural implementation of that principle. Least Agency is enforced here — mission scope defines the boundary of what an agent is authorized to decide and act on.

### Plane 2: Execution & Tool Governance

  - Agent runtime execution control
  - Tool and API invocation authorization
  - Workflow sequencing enforcement
  - Action-level decision interception

### Plane 3: Policy & Compliance Engine

  - Security policy enforcement at runtime
  - Regulatory and compliance constraint injection
  - Data access and handling rules enforcement
  - Contextual policy evaluation during execution

**Law alignment, Planes 2 and 3:** Law 2, Enforce at Runtime. Plane 2 governs *what* the agent can invoke. Plane 3 governs *whether* that invocation is policy-compliant given current context. Neither plane is sufficient alone. Runtime enforcement requires both operating simultaneously.

### Plane 4: Human Oversight, Audit & Traceability

  - Real-time behavior monitoring
  - Full execution trace logging
  - Forensic reconstruction capability
  - Compliance evidence generation
  - Human intervention interfaces: inspect, interrupt, and override capabilities at every layer
  - Escalation paths from automated enforcement to human decision-making

**Law alignment:** Law 5, Humans Retain the Right to Intervene. Plane 4 is not a passive audit layer. It is the architectural home of active human oversight. Logging what happened is necessary. Enabling humans to act on what is happening — in real time — is non-negotiable.

### Plane 5: Multi-Agent Trust & Delegation

  - Explicit trust establishment across all handoff types: delegation, orchestration, tool invocation, subagent spawning
  - Delegation scope definition: what authority transfers, what does not
  - Independent identity and policy enforcement at every node in an interaction chain
  - Chain-level audit: full traceability across every interaction in an execution sequence
  - Trust revocation propagation across interaction chains

**Law alignment:** Law 4, Trust Does Not Travel. Every handoff is a trust boundary. The participant on the receiving end inherits the task, not the authority. Delegation boundaries are explicit, auditable, and revocable.

-----

## Integration Model

Governed Autonomy operates above, not in place of, existing enterprise infrastructure:

| Enterprise Domain         | Current Role                                 | Governed Autonomy Coordination                                  |
| ------------------------- | -------------------------------------------- | --------------------------------------------------------------- |
| Identity Governance       | Defines baseline trust and access boundaries | Agent identity lifecycle and cross-system correlation (Plane 1) |
| Security Platforms        | Provides threat signals and context          | Runtime behavioral enforcement beyond detection (Planes 2 & 3)  |
| Infrastructure Automation | Provides execution environments              | Execution constraints for autonomous agents (Plane 2)           |
| Data Governance           | Defines usage constraints                    | Data access rules enforced during agent execution (Plane 3)     |
| SIEM / Observability      | Logs and detects post-execution              | Active human oversight and intervention capability (Plane 4)    |

These systems remain authoritative in their domains. Governed Autonomy is the runtime enforcement layer that coordinates them into a unified governance plane for AI agent behavior.

-----

## Category Boundaries

Governed Autonomy is **not**:

  - A model or LLM framework
  - An orchestration or workflow tool
  - An identity and access management system
  - A security detection or response product
  - An observability or monitoring platform

It **is**: a cross-plane runtime governance architecture that sits above existing enterprise systems and coordinates enforcement across identity, lifecycle, execution, policy, oversight, and multi-agent trust domains.

> **Validation test:** If runtime enforcement of autonomous AI agent behavior is removed and the system would still meet its objective, it is not Governed Autonomy.
