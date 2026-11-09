> **Canonical:** https://governedautonomy.org/glossary/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/glossary/ — the site is authoritative.

# Glossary

The vocabulary of governed autonomy, defined canonically.

Three kinds of entries. **Doctrine vocabulary** is defined here authoritatively — these terms mean what the doctrine says they mean, and each links to its canonical page. **The agentic field** entries define the wider terrain neutrally, as working definitions a practitioner can rely on. **Model & context mechanics** defines the machinery underneath agent behavior — models, tokens, context, tools, and sessions. Definitions are versioned with the doctrine (v4) and cite-able by anchor.

---

## Doctrine vocabulary

### [Governed Autonomy](#governed-autonomy)

The architectural doctrine of requirements for keeping autonomous agent actions within approved mission-scoped authority as agents work across systems. It coordinates identity, policy, execution controls, human intervention, evidence and delegation. Adopters authorize missions and own policy and factual assumptions; implementations demonstrate the applicable controls within a declared boundary.

Canonical: [What Is Governed Autonomy?](https://governedautonomy.org/what-is-governed-autonomy/)

### [The 5 Laws](#the-5-laws)

The doctrine’s invariants — what must be true for any governed agent: Agents Are Identities, Not Tools; Enforce at Runtime; Governance Must Span Systems; Trust Does Not Travel; Humans Retain the Right to Intervene. Each law can be violated by a specific architectural decision, which is what makes them laws rather than aspirations.

Canonical: [The 5 Laws](https://governedautonomy.org/laws/)

### [Governed Autonomy Architecture](#governed-autonomy-architecture)

The reference design: five architectural planes — Agent Identity & Lifecycle; Execution & Tool Governance; Policy & Compliance Engine; Human Oversight, Audit & Traceability; and Multi-Agent Trust & Delegation — that together place every control a governed deployment needs.

Canonical: [The Architecture](https://governedautonomy.org/architecture/)

### [Plane](#plane)

One of the five Architectural Planes — Agent Identity & Lifecycle; Execution & Tool Governance; Policy & Compliance Engine; Human Oversight, Audit & Traceability; Multi-Agent Trust & Delegation — and, in this doctrine, nothing else. Where Institute or practice text uses the word in another sense (control plane, data plane, service plane), it is qualified.

Canonical: [The Architecture](https://governedautonomy.org/architecture/)

### [Governed Autonomy Framework](#governed-autonomy-framework)

The implementation methodology: six pillars — Agent Identity, Mission Definition, Behavioral Policy, Runtime Enforcement, Human Oversight & Intervention, and Multi-Agent Governance — sequencing how an organization builds toward governed autonomy.

Canonical: [The Framework](https://governedautonomy.org/framework/)

### [Least Agency](#least-agency)

An agent must be granted only the minimum decision scope, tool access, and action authority its mission requires — no more authority than the mission demands. The third leg of the trilogy after Least Privilege and Least Trust; converging industry usage is codified in the OWASP Top 10 for Agentic Applications.

Canonical: [The 5 Laws](https://governedautonomy.org/laws/)

### [The Trilogy](#the-trilogy)

Three successive minimization disciplines: Least Privilege constrains access, Least Trust (the Zero Trust contribution) constrains assumptions, and Least Agency constrains autonomy. Each generation of enterprise security added one leg; autonomous agents demand the third.

Canonical: [Zero Trust lineage](https://governedautonomy.org/zero-trust/)

### [Threat Surface](#threat-surface)

The doctrine’s named failure modes for autonomous agents: Prompt Injection, Intent Hijacking, Cascading Failure, and Behavioral Drift. Each names a class of failure that governance must be architected against, not patched after.

### [Intent Hijacking](#intent-hijacking)

An action aligned with an invalid or manipulated purpose or mission context. Governance evaluates observable effects against approved mission constraints and designated authoritative relationships. It cannot read internal motivation or establish that an integrity-protected fact is true. Mission integrity, action alignment, policy adequacy and business correctness remain distinct.

### [Cascading Failure](#cascading-failure)

A threat-surface entry: one agent’s error propagating at machine speed through the systems and agents downstream of it, outrunning periodic review. The failure mode that makes governance tempo a first-class design constraint.

### [Behavioral Drift](#behavioral-drift)

A threat-surface entry: the gradual divergence of an agent’s operating behavior from its authorized mission — through model updates, context accumulation, or changing tool surfaces — without any single detectable violation.

### [Organizational Maturity Evaluation](#maturity-model)

Organizational maturity evaluation: the ability to sustain agent governance, rated by dimension as Identified, Governed or Continuous. It is separate from any deployment; each deployment must satisfy its applicable runtime baseline and assurance profile regardless of the organization's rating, and a rating does not license any deployment.

Canonical: [The Organizational Maturity Evaluation](https://governedautonomy.org/maturity/)

### [Conformance Layer](#conformance-layer)

Historical proposal (RFC 001 revision 2), not v4 text: testable, mechanism-agnostic criteria an implementation can be assessed against. The Assessment Companion states how v4 deployments are assessed.

Canonical: [RFC 001](https://governedautonomy.org/rfc/v4-conformance-layer/)

---

## The agentic field

### [AI Agent (Agentic AI)](#ai-agent)

A software system that uses a model to plan and execute multi-step tasks toward a goal — calling tools, acting on other systems, and adapting to results — rather than returning a single response. Agentic AI names the class; an agent is an instance with a mission.

### [Agent Harness](#agent-harness)

Industry term for the software scaffolding around a model that makes it an agent: the execution loop, tool interfaces, memory, and control logic. The harness is where an agent’s capabilities are assembled — and therefore one of the places its governance must attach. In this doctrine, harness always means this runtime component — the Plane 2 execution layer that turns model proposals into governed actions — and never a category. The doctrine was published as the AI Harness Doctrine through v3.2; that name is retired and appears only in historical and citation records (the changelog and the publication record).

### [Agent Identity](#agent-identity)

A distinct, verifiable identity provisioned for a specific agent — owned, scoped, credentialed, and revocable like a human identity, with constraints appropriate to its autonomy. Contrast with shared service accounts, which cannot distinguish one agent’s actions from another’s.

### [Non-Human Identity (NHI)](#non-human-identity)

Any machine identity — service accounts, tokens, bots, AI agents. NHIs are commonly reported to outnumber human identities in enterprises and are often the least-governed identity class; agentic AI adds to both.

### [Runtime Enforcement](#runtime-enforcement)

Protected enforcement before each effect, with rechecks before commitment where material conditions can change. Enforcement sits in the execution path, so the governed actor cannot bypass or replace it. Observing activity after commitment complements, but cannot satisfy, required pre-effect enforcement.

### [Guardrails](#guardrails)

Model- or application-level filters that shape what a system will say or attempt. Guardrails are configuration — they can be disabled, bypassed, or updated away. The distinction between guardrails and governance is whether the control survives the actor it constrains.

See also: [Doctrine vs. guardrails](https://governedautonomy.org/vs/guardrails/)

### [Human-in-the-Loop](#human-in-the-loop)

An oversight pattern in which defined agent actions require human review or approval before proceeding. Governance-grade oversight encodes the checkpoints in the workflow architecture — by action type, data sensitivity, and stakes — rather than leaving the agent to decide when to ask.

### [Least Privilege](#least-privilege)

The classical access-control discipline: every principal receives the minimum permissions its function requires. Necessary but not sufficient for agents — an agent can hold minimal permissions and still misuse them, which is the gap Least Agency addresses.

### [Zero Trust](#zero-trust)

The security architecture in which no access is granted on the basis of network location or prior trust: every request is evaluated continuously against policy (NIST SP 800-207). Governed autonomy extends the same never-trust-always-verify posture from access requests to agent behavior.

See also: [Zero Trust and the doctrine](https://governedautonomy.org/zero-trust/)

### [Multi-Agent Delegation](#multi-agent-delegation)

One agent handing work to another — spawning sub-agents, invoking peers, chaining tools. Each handoff is an independent trust boundary: the receiving agent inherits the task, never the authority. Ungoverned delegation is how single-agent risk becomes systemic risk.

### [Tool Allowlisting](#tool-allowlisting)

Restricting an agent to an explicit, verified, version-pinned set of tools rather than an open-ended surface. The design-level control government guidance treats as baseline for agent deployments.

### [Prompt Injection](#prompt-injection)

An attack in which instructions embedded in content an agent processes — a web page, a document, a tool result — hijack the agent’s behavior. For tool-wielding agents the blast radius is the agent’s authority, not the conversation, which is why defense belongs in the execution path rather than the prompt.

### [Model Context Protocol (MCP)](#model-context-protocol)

An open protocol standardizing how AI applications connect models to tools and data sources. Protocols like MCP expand what agents can reach — which is precisely why tool governance and identity must attach at the same layer.

---

## Model & context mechanics

How the machinery actually works. Agent governance keeps returning to these mechanics — an agent’s behavior is downstream of its model, its context, and its tools, and several doctrine arguments (runtime enforcement in the tool-call gap, delegation boundaries at subagent spawns, memory as a governed asset) are only legible with this vocabulary in hand.

### [Model](#model)

The parameters. A model is stateless — it does next-token prediction and nothing else, and cannot do anything agentic on its own. Everything agentic comes from the harness around it.

### [Parameters](#parameters)

The numbers inside a model — often billions — set during training. Everything the model knows from training lives in them. Also called weights.

### [Training](#training)

The process that sets a model’s parameters by exposing it to vast amounts of data and adjusting to improve next-token prediction. After training, the parameters are fixed.

### [Inference](#inference)

Running a trained model to generate output. Parameters stay fixed; only the context varies. Every agent action begins with an inference call.

### [Model Provider](#model-provider)

Whatever serves a model for inference — a hosted API or local serving infrastructure. The harness sends context to the provider; the provider returns one response.

### [Token](#token)

The atomic unit a model reads and writes — roughly word-sized, but not exactly. Context-window size, cost, and latency are all counted in tokens.

### [Next-Token Prediction](#next-token-prediction)

What a model actually does: sample one next token from the context, append it, and run again. Every capability layered on top — reasoning, tool use, agency — is built from this single operation.

### [Non-determinism](#non-determinism)

The same input can produce different output — a property of how models generate text and how providers serve requests. A governance-relevant fact: identical conditions do not guarantee identical agent behavior.

### [Context](#context)

The information an agent has access to right now — what it knows that is pertinent to the task, as distinct from what its model learned in training.

### [Context Window](#context-window)

Everything the model sees on a single inference request. Finite and model-specific — the only surface through which the model perceives anything.

### [System Prompt](#system-prompt)

The instructions the harness prepends to every model request — the agent’s standing brief, usually stable across a session. A policy stated only here is a suggestion, not enforcement.

### [Turn](#turn)

One user message plus everything the agent does in response, until it yields back to the user. A single turn can contain many inference requests and tool calls.

### [Session](#session)

One bounded run of interaction with an agent. Starts empty, accumulates context, and ends when cleared, closed, or compacted into a fresh session.

### [Stateless and Stateful](#stateless-stateful)

Stateless: carries no information forward — the model across requests, an agent across sessions by default. Stateful: carries information forward — a session across turns, or an agent given a memory system.

### [Compaction](#compaction)

Summarizing a session’s history to seed a fresh session when the context window fills. Lossy by design: detail is traded for headroom, and whatever the summary omits is gone from context.

### [Handoff](#handoff)

Transferring agent context from one session to another with no return path — via a written artifact, a compaction summary, or another carry mechanism. Every handoff loses something; governance records must not depend on what survives one.

### [Memory System](#memory-system)

A mechanism that makes an agent stateful across sessions by persisting information to the environment and reloading it at session start. Agent memory is an asset to govern: it shapes future behavior and can be poisoned.

### [Knowledge Cutoff](#knowledge-cutoff)

The date past which a model has no training knowledge. Anything newer must arrive through context — or the model may fabricate it.

### [Parametric Knowledge](#parametric-knowledge)

What a model knows from training, stored in its parameters and frozen at training time. Counterpart to contextual knowledge.

### [Contextual Knowledge](#contextual-knowledge)

Facts an agent can read directly from its context right now — loaded documents, tool results, instructions. Counterpart to parametric knowledge, and the half an enterprise actually controls.

### [Tool](#tool)

A function the harness exposes for the agent to call — read a file, run a command, query an API. Tools are how an agent perceives and acts on its environment, which is why tool governance is a control plane and not a feature.

### [Tool Call and Tool Result](#tool-call)

A tool call is the model’s output naming a tool and its arguments — structured text the harness must execute. The tool result is what comes back. The gap between the two is where runtime enforcement lives: the call can be inspected, authorized, or refused before anything happens.

### [Subagent](#subagent)

An agent spawned by another agent to perform a scoped piece of work in its own session, reporting back a single result. Every spawn is a delegation boundary — the subagent inherits the task, not the authority.

### [Sandbox](#sandbox)

An isolated environment an agent runs inside — container, VM, or restricted shell — limiting the blast radius of its actions. A sandbox bounds where an agent acts; it does not govern what the agent does within it.

### [Environment](#environment)

The world an agent acts on — everything outside the harness that it perceives through tool results and changes through tool calls.

### [Hallucination](#hallucination)

Confidently wrong model output. Two flavors: factuality (invented facts) and faithfulness (drift from what the loaded context actually says). In agentic systems, a hallucination can become an action.

### [Sycophancy](#sycophancy)

Confidently agreeable model output — a bias toward telling the user what they want to hear, produced by training on human preferences. A governance concern wherever an agent’s own report is the basis for approving its actions.

### [Reasoning Effort](#reasoning-effort)

A setting for how much reasoning a model does before answering — more effort spends more output tokens for a better chance at hard problems. One of the dials that make identical agents behave differently.

---

To cite a definition, link its anchor — every term on this page has a stable URL. For citing the doctrine itself, see [How to cite](https://governedautonomy.org/cite/). Terms are added and revised through the doctrine's [changelog](https://governedautonomy.org/changelog/).
