> **Canonical:** https://governedautonomy.org/vs/orchestration/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy vs Orchestration & Workflow Automation

Orchestration executes paths a human authored. Autonomous agents author their own paths.

Workflow orchestration (pipelines, schedulers, automation platforms, integration buses) is how the enterprise made software-to-software work reliable. Its control model is strong precisely because the workflow is *known in advance*: every step authored, every transition reviewed, every failure mode anticipated.

Autonomy removes the one assumption the whole model rests on.

-----

## What orchestration does well

  - Deterministic execution of human-authored workflows, with retries, rollbacks, and audit
  - Explicit dependencies and sequencing: the workflow definition *is* the control
  - A natural choke point for change management: edit the workflow, review the diff, redeploy

## Where it stops

### Identity governance

Orchestrators typically run workflows under broad platform credentials. When an agent is one step in a pipeline, or the pipeline's author, the executing identity no longer maps to the deciding identity. Every handoff between orchestrator, agent, tool, and subagent is a trust boundary, and [Trust Does Not Travel](/laws/#law-4-trust-does-not-travel) across it automatically: the receiving participant inherits the task, not the authority.

### Runtime behavior control

A workflow engine enforces *sequence*, not *judgment*. An autonomous agent generates its execution plan at runtime, selects tools dynamically, and adapts mid-chain based on intermediate results. There is no predefined path to validate against. Reviewing the workflow definition governs nothing when the workflow is written, by the agent, at execution time.

### System integration

Orchestration connects systems mechanically but carries no policy about what crossing each boundary *means*. Connecting is not governing: an integration bus moves an agent's action between domains without evaluating whether that action, in that context, is sanctioned.

## The gap

> Orchestration can guarantee the steps run in order. It cannot ask whether the steps the agent just invented should run at all.

## Coordination, not replacement

In the Governed Autonomy model, orchestration remains the execution substrate, and gains a governor. [Execution & Tool Governance](/architecture/#plane-2-execution-tool-governance) intercepts at the action level: every tool invocation evaluated, every sequence verified, allow/deny/modify decided during execution. [Multi-Agent Trust & Delegation](/architecture/#plane-5-multi-agent-trust-delegation) makes each handoff in the chain explicit, auditable, and revocable. The pipeline still runs the work. It no longer decides, alone, whether the work should run.
