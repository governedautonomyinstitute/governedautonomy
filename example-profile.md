> **Canonical:** https://governedautonomy.org/example-profile/ · Doctrine v4 · published by the Governed Autonomy Institute
> This file is generated from the built site at https://governedautonomy.org/example-profile/ — the site is authoritative.

# Example workforce assurance profile

Illustrative synthetic profile | Version 4 | Not an estate authorization

This example applies the broadly scoped doctrine to a small document-triage workforce. All names, resources and numerical bounds below are synthetic fixture choices, not approved risk tolerances for any actual deployment. The example is a specified profile, not evidence that its controls were implemented or tested.

## Assignment and boundary

Mission `triage-demo-1` permits three fictional agents to classify a synthetic work queue and prepare internal draft dispositions. Planner may assign record identifiers, Reader may retrieve only the assigned synthetic records, and Drafter may write drafts to the fixture's staging collection. Each actor has its own workload identity. A resource authority independently grants the scope it controls. Planner's right to delegate does not require it to hold Reader's retrieval credential.

The included boundary is the fixture queue, mission registry, synthetic records store, staging collection, shared reservation ledger and local evidence writer. The profile excludes external communications, real personal data, production infrastructure, publishing and deletion. A human principal approves the bounded assignment once for a one-hour fixture validity period; expected changes in record identifiers within the approved collection do not require another approval.

## Permitted effects and limits

The workforce may read at most ten distinct assigned records and write at most ten corresponding drafts across all agents and retries. A repeated idempotency key cannot consume or perform a second write. A negative quantity cannot add budget. Reader can use a general-purpose client only through the collection boundary; changing invocation syntax, following a redirect or invoking a nested tool cannot add destinations or record scope.

No worker may change mission scope, authority policy, the evidence writer or reservation ledger rules. Discovery of another agent does not authorize it. A handoff carries the mission reference, record subset, remaining reservation and obligation, not a pass-through credential or an expanded grant.

## Current checks and effect-time conditions

Before each governed effect, protected controls check workload identity and designated integrity signals, grant issuer/audience/scope/expiry, current mission version, assignment-to-record relationship, policy and reservation state. Delayed writes recheck validity before commitment. Prior successful jobs are not an integrity signal sufficient by themselves. If the fixture cannot establish a required current condition, the ordinary effect does not proceed.

The resource authority holds record assignments; the agent's requested identifier cannot establish entitlement. A tampered assignment is refused. An intact but incorrect authoritative assignment remains a factual residual risk owned by the fictional mission owner; the profile demonstrates that limit rather than asserting truth from a signature.

## Intervention, obligations and exceptions

Each assigned record retains a fixture deadline and owner until completed, handed off or explicitly closed. Revocation denies subsequent writes and marks queued work for withdrawal; the fixture records which already committed effects cannot be undone. A stopped worker's remaining queue is transferred to the accountable owner without extending the grant or deadline silently.

Recorder failure denies ordinary writes. This example defines no continuity mode and no policy exception. An outage or deadline does not invent one. Restoration requires the designated authority, current validity checks and deduplication of committed work.

## Evidence and assessment

The evidence bundle identifies mission, actors, grants, assignments, policy versions, reservations, decisions, effects and outcomes. Sensitive content is absent because the inputs are synthetic. Known probes test collection completeness; an observed missing required record fails the relevant evidence property. Unavailable collection produces not assessed rather than a fabricated execution result.

Assess permitted recurring variation, wrong record, stale grant, changed mission, audience substitution, delegated expiry amplification, concurrent reservation exhaustion, duplicate write, negative quantity, recorder failure, revocation and reconstruction without re-execution. Report each expected/actual result separately, including valid work completed and false denials. This profile alone reports no passing results. Real agent frameworks or messaging adapters would need their own boundary evidence before any deployment claim.
