> **Canonical:** https://governedautonomy.org/framework/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy Framework

The structured implementation methodology for governing autonomous AI agents through mission-scoped identity, policy, and runtime behavioral control across enterprise systems.

The Governed Autonomy Framework translates Governed Autonomy Architecture into design decisions, implementation patterns, and operational practices. It defines how enterprises adopt Governed Autonomy — not conceptually, but practically.

Architecture defines *where* control sits. Framework defines *how* you build it.

The framework is built on **6 Pillars**, mapped directly to the 5 Architectural Planes. The 5 Planes map to 6 Pillars because Plane 1 (Agent Identity & Lifecycle) requires two distinct implementation concerns — identity provisioning and mission scoping — each warranting its own pillar.

-----

## Pillar 1: Agent Identity

**AI agents are first-class enterprise identities.**

  - Identity lifecycle (creation, rotation, revocation)
  - System-level access scopes
  - Trust boundaries
  - Credential management (including ephemeral credentials)
  - Agent registry: every agent provisioned, tracked, and revocable

### Key shift: Service Accounts → Agent Identities

Identity is the foundation of everything that follows. Without a governed identity, there is no surface to attach policy, no subject to audit, and no entity to revoke. Agent identity is not a feature of deployment — it is a prerequisite.

*Architecture alignment: Plane 1, Agent Identity & Lifecycle*

-----

## Pillar 2: Mission Definition

**AI agents must operate within explicitly defined missions.**

  - The objective of the agent
  - Systems it can interact with
  - Boundaries of operation
  - Acceptable outcomes and failure conditions

### Key shift: Roles → Missions

Traditional systems assign roles. Governed Autonomy assigns missions: bounded objectives with explicit scope, constraints, and success criteria. Mission scope is where Least Agency is operationalized: the mission defines exactly what the agent is authorized to accomplish, and nothing beyond it.

*Architecture alignment: Plane 1, Agent Identity & Lifecycle*

-----

## Pillar 3: Behavioral Policy

**AI behavior must be governed across systems, not just at access points.**

  - Allowed actions per system and context
  - Conditional constraints (environment, data sensitivity, operational state)
  - Cross-system behavioral rules
  - Prohibited action patterns and escalation triggers

### Key shift: Access Control → Behavioral Control

Access policies answer: *can this agent reach this system?* Behavioral policies answer: *what is this agent allowed to do within and across systems, given current context?* Access control is necessary. It is not sufficient.

*Architecture alignment: Plane 3, Policy & Compliance Engine*

-----

## Pillar 4: Runtime Enforcement

**All AI agent actions must be evaluated and constrained during execution in real time.**

  - Interception points (API calls, tool usage, workflow transitions)
  - Enforcement decisions (allow, deny, modify, escalate)
  - Real-time context evaluation
  - Response to policy violations during execution
  - Human escalation paths: when automated enforcement triggers human decision-making

### Key shift: Pre/Post Control → In-Execution Control

Runtime enforcement is the core of Governed Autonomy. It is the mechanism through which the 5 Laws are applied in practice.

*Architecture alignment: Planes 2 and 3, Execution & Tool Governance + Policy & Compliance Engine*

-----

## Pillar 5: Human Oversight & Intervention

**At every layer of an agentic system, a human must be able to inspect, interrupt, and override.**

  - Visibility interfaces: what humans can see about agent behavior in real time
  - Interrupt mechanisms: how execution is paused or halted
  - Override controls: how human decisions supersede agent decisions
  - Escalation triggers: conditions that require human review before execution continues
  - Full execution trace: forensic reconstruction of every action taken

### Key shift: Passive Audit → Active Oversight

Logging what happened is necessary. Enabling humans to act on what is happening, in real time, is non-negotiable. Audit without intervention capability is observation without control. Governed Autonomy requires both.

*Architecture alignment: Plane 4, Human Oversight, Audit & Traceability*

-----

## Pillar 6: Multi-Agent Governance

**Every handoff is a trust boundary that must be explicitly governed: delegation, orchestration, tool invocation, subagent spawning.**

  - Delegation scope: what authority transfers, what does not
  - Independent identity enforcement: every participant in an interaction chain carries its own governed identity
  - Trust boundaries across all handoff types: explicit, auditable, and revocable
  - Chain-level audit: full traceability across every interaction in an execution sequence
  - Trust revocation propagation: revoking one participant's authority propagates appropriately through the chain

### Key shift: Single-Agent Governance → Chain Governance

The agent on the receiving end of any handoff inherits the task, not the authority. Trust does not travel. Every participant in an interaction chain must be independently identified, independently authorized, and independently governed.

*Architecture alignment: Plane 5, Multi-Agent Trust & Delegation*

-----

## Framework Summary

| Pillar                     | What It Governs         | Key Shift                           | Plane        |
| -------------------------- | ----------------------- | ----------------------------------- | ------------ |
| 1\. Agent Identity         | Who the agent is        | Service Accounts → Agent Identities | Plane 1      |
| 2\. Mission Definition     | Why the agent acts      | Roles → Missions                    | Plane 1      |
| 3\. Behavioral Policy      | What is allowed         | Access → Behavior                   | Plane 3      |
| 4\. Runtime Enforcement    | When control happens    | Before/After → During               | Planes 2 & 3 |
| 5\. Human Oversight        | Who can intervene       | Passive Audit → Active Oversight    | Plane 4      |
| 6\. Multi-Agent Governance | How chains are governed | Single Agent → Chain                | Plane 5      |
