> **Canonical:** https://governedautonomy.org/standards/scim-agent-governance/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/standards/scim-agent-governance/ — the site is authoritative.

# Governed Autonomy and the IETF SCIM Agent Governance Extension

Most documents mapped on this site are strongest in what they require. This one is most useful in what it declines to require — and in saying plainly that the semantics for it do not yet exist.

In July 2026 an individual Internet-Draft, *SCIM Agent Governance Extension*, was submitted to the IETF. It extends the SCIM Agent resource type with governance metadata for provisioned agent identities: a lifecycle state model, an autonomy classification, an operational validity window, and a reference to credential discovery information. The lifecycle state values are grounded in the identity information lifecycle of ISO/IEC 24760-1, with one agent-specific addition.

It is an early-stage individual submission, not an adopted working group document or a published RFC, and it may never become one. It is mapped here anyway, for a reason the other pages in this section cannot claim: it is **open**. Every other document mapped on this site is finished. This one is a live draft in a standards venue that accepts comment.

**Status.** `draft-kushwaha-scim-agent-governance-00`, Informational, dated 26 July 2026, expires 27 January 2027. Individual submission. Nothing on this page should be read as implying IETF consensus, working group adoption, or endorsement of this doctrine.

## What the draft establishes

Three of its provisions matter to this doctrine directly:

| Provision | What it does | Where it lands in this doctrine |
|---|---|---|
| **Lifecycle state model** | Replaces a boolean active flag with a state set grounded in ISO/IEC 24760-1: distinguishing reversible suspension from terminal decommissioning, freezing an agent during investigation while preserving evidence, and recording permitted transitions | [Plane 1, Agent Identity & Lifecycle](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle), almost exactly. Plane 1 was renamed from "Identity & Access Control" precisely because lifecycle, not access, is the governed property. |
| **Autonomy classification** | An attribute recording how autonomous a provisioned agent is, carried on the identity record itself | [Agents Are Identities, Not Tools](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools), which asks that identity be attributable and graded by autonomy. Autonomy as an attribute of a registered identity is the doctrine's first Law in schema form. |
| **Operational validity window** | A bounded period over which the agent identity is valid | [Least Agency](https://governedautonomy.org/laws/#law-1-agents-are-identities-not-tools) in the time dimension — authority that expires rather than persisting until revoked |

The convergence worth naming is not any single attribute. It is that a standards venue is now treating an autonomous agent as a *provisioned identity with a governed lifecycle* rather than as a configured tool. That is this doctrine's first Law, and this is the first time it has appeared in a standards-track document rather than a vendor specification or a preprint.

## The exclusions are the substance

The draft is unusually explicit about what it refuses to carry, and each refusal draws a boundary this doctrine also draws.

### Action-level authorization is out of scope

Attributes enumerating permitted or denied actions per tool are ruled out as authorization policy rather than provisioning metadata; the draft states that fine-grained agent authorization belongs in the authorization layer, and notes that deny-list constructions in particular create false assurance through incomplete enumeration.

That is the provisioning/runtime boundary this doctrine draws between [Plane 1](https://governedautonomy.org/architecture/#plane-1-agent-identity-lifecycle) and [Planes 2](https://governedautonomy.org/architecture/#plane-2-execution-tool-governance) and [3](https://governedautonomy.org/architecture/#plane-3-policy-compliance-engine), arrived at independently and for the same reason. It is also the clearest external statement of the argument the doctrine makes against identity systems as a governance substitute (see [the IAM comparison](https://governedautonomy.org/vs/iam/)): the identity layer knowing an agent is authorized is not the same as anything knowing that what the agent is doing right now is sanctioned. The draft agrees, and declines to pretend otherwise.

### Delegated authority is deferred, and the reason is stated

This is the finding. Attributes describing where an agent may operate and under whose delegated authority are acknowledged as real enterprise concerns, and then explicitly deferred: they are not local to SCIM, because to be useful they must be legible across provisioning, federation and authorization protocols at once. The draft points at OAuth 2.0 Token Exchange (RFC 8693) for delegation at token time, and at the IETF WIMSE working group for cross-system workload identity context, and concludes that a SCIM binding can follow *once cross-protocol semantics exist*.

Read that last clause carefully. A standards document is stating, in the venue where such semantics would be defined, that the semantics for cross-system delegated authority between agents **do not yet exist**.

That is [Trust Does Not Travel](https://governedautonomy.org/laws/#law-4-trust-does-not-travel) and [Plane 5, Multi-Agent Trust & Delegation](https://governedautonomy.org/architecture/#plane-5-multi-agent-trust-delegation) — described here not as this doctrine's assertion but as an acknowledged open problem, by a party with no interest in this doctrine's position. Plane 5 exists because authority granted to one agent does not automatically remain valid when that agent hands work to another. The draft reaches the same conclusion from the opposite direction: it cannot record delegation scope on an identity, because there is nothing coherent across protocols to record.

## Where each is thinner

### What the draft supplies that this doctrine does not

Schema. Plane 1 states that agents are first-class identities with governed lifecycles; it does not define attribute names, value sets, or permitted state transitions, and does not intend to. The draft supplies exactly that, anchored to an existing ISO identity lifecycle standard and to a provisioning protocol enterprises already run. If Plane 1 is ever implemented in a real identity platform, it will be through work of this kind, and this doctrine defers to it on schema.

### What this doctrine supplies that the draft does not

Everything after provisioning. The draft governs the identity record; it explicitly does not govern the action, the verdict, the audit evidence, or the human's right to intervene mid-mission. It has no view on which controls must hold simultaneously for a single agent action to be sanctioned, and no maturity model. Those are [the other four Planes](https://governedautonomy.org/architecture/), and the runtime half is where specifications such as [AARM](https://governedautonomy.org/standards/aarm/) are working. A provisioned agent with a correct lifecycle state and an accurate autonomy classification can still take an unsanctioned action one second later.

## What this suggests about the shape of the problem

Four independent efforts now specify how a single agent's runtime actions are controlled. This draft specifies how a single agent's identity is provisioned and retired. Between them they cover Planes 1 through 4 with increasing rigour. All of them stop at the same place, and this draft is the only one that says so explicitly: what happens to authority when one agent hands work to another is unspecified, and the primitives to specify it are not agreed.

That is a convergent finding, not a competitive one. It suggests Plane 5 is not an artifact of this doctrine's architecture but a genuine gap in the field, and that the venues most likely to close it are WIMSE and the OAuth delegation work the draft names.

## Primary sources

- [draft-kushwaha-scim-agent-governance-00 — SCIM Agent Governance Extension](https://datatracker.ietf.org/doc/draft-kushwaha-scim-agent-governance/) (IETF Internet-Draft, Informational, 26 July 2026)
- [RFC 8693 — OAuth 2.0 Token Exchange](https://datatracker.ietf.org/doc/html/rfc8693), cited by the draft for delegation at token time
- [RFC 7643 — SCIM Core Schema](https://datatracker.ietf.org/doc/html/rfc7643)
- [IETF WIMSE working group](https://datatracker.ietf.org/wg/wimse/about/) — cross-system workload identity context
