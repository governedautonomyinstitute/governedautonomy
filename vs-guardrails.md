> **Canonical:** https://governedautonomy.org/vs/guardrails/ · Doctrine v3.4 · published by the Governed Autonomy Institute
> This mirror may lag the site; the site is authoritative.

# Governed Autonomy vs AI Guardrails

Guardrails constrain what a model says. They do not govern what an agent does.

Guardrails (input filtering, output moderation, content policies, jailbreak resistance, safety classifiers) are the first control layer most organizations deploy around AI, and the one most often mistaken for governance. They operate on the *conversation*: what enters the model and what leaves it.

An autonomous agent's risk is not in what it says. It is in what it does.

-----

## What guardrails do well

  - Filter harmful, off-policy, or sensitive content at the model boundary
  - Reduce, though never eliminate, prompt-level manipulation of model outputs
  - Cheap to deploy and model-adjacent: a sensible baseline for any AI exposure

## Where they stop

### Identity governance

Guardrails have no concept of identity at all. They evaluate text, not actors. The same filter applies whether the caller is an intern's chatbot or an agent holding production credentials — which is precisely backwards from how every other enterprise control is scoped.

### Runtime behavior control

The agent's consequential surface is its **tool calls**: API invocations, file operations, system commands, delegations, none of which a content filter evaluates. A perfectly polite agent can delete a production database; the output that passed moderation was the action's announcement, not the action. **Intent Hijacking** makes this concrete: a valid-looking action taken for a corrupted reason sails through every content check, because the corruption is in the behavior chain, not the words.

### System integration

Guardrails live at one model boundary. An agent's mission spans many systems, many calls, many boundaries, and the risk often emerges only from the *sequence* (read here, combine there, send outward). No per-call content filter can see a cross-system pattern. [Governance Must Span Systems](/laws/#law-3-governance-must-span-systems); guardrails, by construction, govern one checkpoint.

## The gap

> Guardrails protect the conversation. Nothing in them governs the execution: the tool use, the data access, the cross-system behavior where agentic risk actually lives.

## Coordination, not replacement

In the Governed Autonomy model, guardrails remain the model-boundary control: useful, baseline, and insufficient. [Execution & Tool Governance](/architecture/#plane-2-execution-tool-governance) and the [Policy & Compliance Engine](/architecture/#plane-3-policy-compliance-engine) pick up where the content boundary ends: evaluating actions, not sentences, under [Enforce at Runtime](/laws/#law-2-enforce-at-runtime). If your AI safety story ends at the prompt, your agents are governed only when they talk.
