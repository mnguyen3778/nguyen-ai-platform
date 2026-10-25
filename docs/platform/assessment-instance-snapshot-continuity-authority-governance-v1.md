# Assessment Instance Snapshot Continuity Authority Governance v1

Version: v1

## 1. Purpose

This decision governs the minimum authority needed to prove that one particular
assessment instance produced one exact Assessment Service
`ExecutiveAssessmentSnapshot` for the correct Business Entity and applicable
business scope. It supplies a prerequisite to the approved Executive Dashboard
Resource-to-Artifact Binding Authority. It does not produce a snapshot, create
an Executive Dashboard Resource, or authorize production implementation.

## 2. Status and Scope

Status: CONCEPTUAL GOVERNANCE DECISION. Production realization is unresolved.

The bounded subject is continuity from an authoritative Assessment Submission
attempt, or an equivalently unambiguous governed assessment instance, through
successful Assessment Service execution to exact serialized snapshot bytes and
their producer attestation. It also governs how that continuity may be
consumed for a separately authoritative Executive Dashboard Resource
association. It does not select production identifiers, fields, records,
storage, APIs, transport, runtime wiring, or administrative actors.

## 3. Inherited Approved Governance

This decision inherits, without reopening:

- [Executive Dashboard Resource-to-Artifact Binding Authority Governance v1](executive-dashboard-resource-artifact-binding-authority-governance-v1.md).
- [Trusted Authorization Assessment Engagement Context Legitimacy Governance v1](trusted-authorization-assessment-engagement-context-legitimacy-governance-v1.md).
- [Trusted Authorization Assessment Submission Business Context Governance v1](trusted-authorization-assessment-submission-business-context-governance-v1.md).
- [Trusted Authorization Assessment Submission Attempt-to-Resource Binding and Allocation Governance v1](trusted-authorization-assessment-submission-attempt-resource-binding-allocation-governance-v1.md).
- [Trusted Authorization Assessment Submission Resource Lifecycle Governance v1](trusted-authorization-assessment-submission-resource-lifecycle-governance-v1.md).
- [Trusted Authorization Assessment Submission Post-ALLOW Transition Eligibility Governance v1](trusted-authorization-assessment-submission-post-allow-transition-eligibility-governance-v1.md).
- [Business Entity Authority Source Governance v1](business-entity-authority-source-governance-v1.md).
- [Governed Resource Identity / Lookup Governance v1](governed-resource-identity-lookup-governance-v1.md).
- [Resource Identity Authority Source Governance v1](resource-identity-authority-source-governance-v1.md).
- [Trusted Authorization Administrative Mutation and Revocation Ownership Governance v1](trusted-authorization-administrative-mutation-revocation-ownership-governance-v1.md).

Assessment Service snapshot architecture and lifecycle governance, its Snapshot
Integration Contract, and the existing producer-snapshot-attestation-v1 byte
contract remain authoritative in their producer domain. No producer contract
is amended by this decision.

## 4. Attempt Identity Reuse Decision

Decision: **B — REUSE CONDITIONALLY; A GOVERNED CONTINUITY BRIDGE IS REQUIRED.**

The existing Assessment Submission authorization attempt `A` is an exact,
bounded, attempt-scoped identity under inherited governance. Its trusted
`Binding(A,E)` is non-standing and non-transferable. The separately governed
`A -> R` relation binds A to at most one Assessment Submission Resource R and
preserves A/E/B and operation provenance. Same-A retries must resolve the same
R; distinct legitimate attempts remain distinct. Neither R nor `A -> R` is an
Executive Dashboard Resource or dashboard binding.

Existing governance does not require A to be a persistent identifier, assign
a concrete production A-allocation source, or prove that A reached one
successful Assessment Service execution. Therefore A may anchor assessment-
instance continuity only when an approved bridge makes that exact A uniquely
resolvable for the required lifecycle, proves its legitimate A/E/B context,
and preserves it through submission and producer execution. If those
conditions cannot be established, A cannot be used as the continuity anchor;
an equivalently unambiguous governed assessment-instance association must be
separately approved. This decision invents no replacement identifier.

`A` is distinct from runtime `requestId`, correlation ID, snapshot digest,
producer snapshot identity, Assessment Submission R, and Executive Dashboard
Resource identity.

## 5. Successful Execution Definition

Successful Assessment Submission authorization, post-ALLOW transition
eligibility, and actual submission lifecycle state are separate from successful
Assessment Service execution. A prior SUBMIT ALLOW or eligibility for
`PROVISIONAL -> SUBMITTED` is not proof that the transition occurred or that
the producer executed successfully.

For this continuity contract, producer success requires an Assessment Service
successful `ExecutiveRuntimeResult`, construction of
`ExecutiveAssessmentSnapshot` from that exact successful result, successful
deterministic serialization and validation of the snapshot, and a producer
attestation over the exact bytes presented for downstream use. Failed runtime,
snapshot creation, serialization, validation, or attestation establishes no
releasable continuity. Producer-owned success and exact-byte evidence must be
associated with the intended A by the governed bridge; the current producer
handoff does not itself carry A. Successful execution does not upgrade the
snapshot's producer-owned production-authority status or grant dashboard
release eligibility.

## 6. New Continuity Authority Decision

The conceptual Assessment Instance Snapshot Continuity Authority owns the
determination that one exact governed assessment instance, with its
authoritative business context, corresponds to one exact successful producer
execution and attested snapshot. It consumes facts from their respective
owners; it may not create or reinterpret them. Its concrete production source,
authorized establishment and revocation actors, and evidence representation
remain unresolved.

The minimum accepted continuity proposition is:

```text
exact governed A or equivalent assessment instance
    + authoritative applicable Business Entity and scope
    + verified successful Assessment Service execution
    + exact validated serialized ExecutiveAssessmentSnapshot bytes
    + matching producerSnapshotIdentity and valid producer attestation
    + no conflicting, stale, invalid, or revoked association
    -> authoritative instance-to-snapshot continuity
```

The proposition is not principal VIEW permission and does not itself bind an
EIP artifact or Executive Dashboard Resource. Historical continuity evidence
must remain traceable, while current eligibility must be independently
established whenever later use requires current authority.

## 7. Minimum Evidence Chain

| Relationship | Owner and existing representation | New verification and failure requirement |
| --- | --- | --- |
| A or equivalent instance -> Business Entity B | Attempt-context and Business Entity authorities; `BUSINESS_CONTEXT_READY(A,E,B)` is governed for Assessment Submission. | Prove exact legitimate current A/B context and authority provenance. Missing or conflicting context fails closed. |
| A -> Assessment Engagement E, when applicable | Assessment Engagement and current-attempt binding authorities; `Binding(A,E)` and immutable `E -> B` are governed for submission. | Preserve exact E and verify required current scope. Same-B but wrong-E substitution fails closed. Dashboard Engagement scope remains conditional under Resource governance. |
| A -> Assessment Submission R | Assessment Submission allocation and Attempt-to-Resource Binding authorities; immutable `A -> R` is governed. | Use only as submission-target provenance. R must not become the Executive Dashboard Resource. Missing or replayed binding cannot establish continuity. |
| A -> accepted submission -> producer execution | Submission lifecycle authority owns actual transition; Assessment Service owns its execution outcome. Post-ALLOW eligibility and `ExecutiveRuntimeResult.is_success` are represented separately. | A governed bridge must prove the same A reached the exact successful producer execution. Eligibility, route receipt, requestId, or prior ALLOW alone is insufficient. This bridge is not implemented. |
| Successful execution -> exact snapshot bytes | Assessment Service owns `ExecutiveAssessmentSnapshot` production and serialization. | Prove the snapshot was constructed and validated from that exact successful result. Failure or ambiguous execution-to-bytes custody fails closed. |
| Exact bytes -> producer identity/attestation | Assessment Service owns `producerSnapshotIdentity` and signed `producer-snapshot-attestation-v1`; existing verifier checks exact bytes. | Verify issuer, trusted key, release and contract versions, digest, signature, and snapshot content. Attestation does not prove A, B, E, or dashboard ownership. |
| Continuity -> Executive Dashboard Resource | Resource Identity Authority owns dashboard R and B/scope; Phase 2D.1 Binding Authority owns Resource-specific association. | Compare exact current Resource/B/applicable scope with continuity evidence. No automatic equality with Assessment Submission R; mismatch fails closed. |

No physical evidence format is selected. A consumer must be able to verify the
provenance, exactness, lifecycle relevance, and authority of every required
relationship without trusting browser or runtime request assertions.

## 8. Business Entity and Conditional Scope

For Assessment Submission, inherited governance requires a pre-established
Assessment Engagement E bound immutably to exactly one Business Entity B and
legitimate current A/E context. This is a submission-domain prerequisite.
The later Executive Dashboard Resource has its own authoritative B and only
those Client, Engagement, or workspace associations required by its governed
scope. The continuity consumer must compare the applicable identities and
reject cross-B, wrong-E, or wrong-workspace substitution. This decision does
not make Engagement or workspace mandatory for every dashboard Resource and
does not assume Client equals Business Entity.

Assessment request organization text, browser selectors, email, provider
claims, and prior selections cannot establish B or E authority.

## 9. Snapshot Identity and Attestation

`producerSnapshotIdentity` identifies exact serialized snapshot bytes under
the producer attestation contract. The attestation signs producer provenance,
release and contract-version context, snapshot digest, and governed conclusion
digest. It does not include A, B, E, Assessment Submission R, Executive
Dashboard Resource identity, or a customer assessment-instance assertion.

`assessmentVersion` identifies a contract family. Runtime request IDs and
correlation IDs remain outside deterministic snapshot truth. No attempt,
request, Business Entity, or dashboard identifier may be inserted into the
frozen snapshot serialization or signing contract by this decision.

## 10. Assessment-Instance Distinction and Cardinality

Two distinct executions, including executions for A1 and A2, may produce
identical deterministic snapshot bytes and the same producer snapshot identity.
The authoritative A-or-equivalent instance association must therefore remain
distinguishable even when bytes and digest are equal. Equal content does not
merge assessment instances or transfer business scope.

For one exact A, at most one successful execution-to-snapshot association may
be accepted as current under this v1 continuity decision. A same-A retry that
re-presents the same established outcome may preserve that outcome only with
matching authority and provenance; it may not silently create a second
accepted outcome. Conflicting successful executions or different snapshots
for the same A fail closed. Corrections or replacement of assessment truth
require separately governed producer and continuity treatment; this decision
does not authorize rebinding A, replacing its Assessment Submission R, or
silently superseding its snapshot association.

## 11. Authority Ownership

Assessment Submission attempt context and `Binding(A,E)` retain their bounded
governed owners. Assessment Submission Resource Reference Allocation Authority
owns allocation of submission R; Attempt-to-Resource Binding Authority owns
`A -> R`. Assessment Engagement and Business Entity authorities own E and B
facts. Submission lifecycle authority owns actual submission transition
semantics; post-ALLOW eligibility does not mutate lifecycle state.

Assessment Service exclusively owns successful assessment execution truth,
snapshot production, exact-byte serialization and validation, producer
snapshot identity, and attestation. The new conceptual Continuity Authority
owns only the cross-boundary instance-to-successful-snapshot association.
Resource Identity Authority owns Executive Dashboard Resource identity and
its B/scope. Phase 2D.1 Binding Authority owns the later Resource-specific
association. Trusted Authorization consumes current authoritative evidence
and alone composes principal VIEW ALLOW/DENY; EIP owns its downstream artifact
production and publication; Website presents approved content only.

No concrete production source or repository is assigned to the Continuity
Authority here. Assessment Service producer ownership does not automatically
assign cross-context customer-instance authority, and Trusted Authorization
runtime custody does not create producer truth.

## 12. Continuity Lifecycle

An allocated or context-bound A may exist without submission or successful
execution. An actual submission may fail during assessment execution. A
successful producer result may fail snapshot creation, validation, or
attestation. Only completion of the entire section 7 chain permits the
Continuity Authority to accept the association.

Accepted continuity must preserve exact A, B, applicable E, producer success,
snapshot bytes, identity, attestation, and authority provenance for audit.
Current use must account for later attempt invalidation, Business Entity or
scope change, association withdrawal, or conflicting evidence. Known current
revocation dominates stale positive evidence. Revocation prevents future
permissive use without erasing historical provenance or reactivating another
attempt's association. Restoration and correction require separate explicit
authority; they are not inferred from retry, signature validity, or a prior
successful execution.

## 13. Negative Verification Matrix

Every rejection below yields no accepted continuity and zero protected
dashboard fields if the association is requested for dashboard release.

| Case | Required rejection |
| --- | --- |
| Allocated but unsubmitted A | No actual submission or producer success; reject. |
| Submitted but unsuccessful A | Producer result is not successful; reject. |
| Successful execution without snapshot | Exact validated snapshot absent; reject. |
| Snapshot without valid attestation | Producer provenance or exact-byte integrity absent; reject. |
| Attestation without A continuity | Signature proves bytes only; reject missing instance bridge. |
| Wrong Business Entity | A/B and dashboard R/B disagree; reject. |
| Wrong applicable Engagement | A/E or required dashboard E disagrees; reject. |
| Attempt replay | Prior A context is presented as a new attempt or authority; reject. |
| Duplicate execution | Accept no second conflicting current outcome for A; reject ambiguity. |
| Identical snapshots for distinct instances | Preserve A1/A2 distinction; reject substitution across instances. |
| Attempt revocation | Current attempt authority invalid; reject future permissive use. |
| Business scope reassignment | Prior association does not silently transfer; reject until separately governed. |
| Conflicting execution evidence | Cannot establish the exact successful result; reject. |
| Missing authority evidence | Any required source fact absent; reject. |
| Authority-source unavailability | Current fact cannot be established; reject. |
| Previously valid continuity later revoked | Historical proof remains non-permissive; reject. |

There is no fallback to another attempt, snapshot, Business Entity, Engagement,
workspace, prior authorization result, older artifact, or synthetic content.

## 14. Fail-Closed Verification Boundary

Before Phase 2D.1 Binding Authority accepts an assessment-instance
association, it must consume verifiable evidence of the exact authoritative A
or equivalent instance, current B and applicable scope, actual submission
state where required, producer-owned successful execution, exact validated
snapshot bytes, matching producer identity, valid attestation, exact
execution-to-snapshot continuity, and no revocation or conflict. Missing,
stale, unavailable, replayed, ambiguous, or contradictory evidence prevents
acceptance. Later protected release must recheck required current authority
under Phase 2D.1.

A valid producer signature is not proof of customer instance or Business Entity
ownership. A prior SUBMIT or VIEW ALLOW is not continuity or current release
authority. `requestId`, a digest, or `A -> R` alone cannot repair a missing
link.

## 15. Explicit Non-Authority Boundaries

The Continuity Authority does not create A, E, B, Assessment Submission R, or
Executive Dashboard R; decide principal SUBMIT or VIEW; create or modify
assessment truth; recalculate scores; alter methodology; create or re-sign
snapshots; admit EIP artifacts; publish EIP intelligence; retrieve artifacts;
or render dashboard content. It may not treat source transport, storage,
browser selection, successful lookup, producer artifact existence, or a
previous decision as authority to establish continuity.

This decision does not reinterpret Assessment Submission R as an Executive
Dashboard Resource and does not extend the protected Assessment Submission
operation to dashboard VIEW.

## 16. Unresolved Implementation Dependencies

The following remain unresolved and require separate approval before runtime
realization:

- concrete production A identity allocation or equivalent instance source,
  uniqueness domain, and stable referential lifecycle;
- authorized A-to-producer handoff and execution-to-snapshot continuity source;
- actual submission lifecycle mutation evidence and its production source;
- concrete Continuity Authority source, authorized actors, mutation,
  withdrawal, revocation, restoration, and audit custody;
- evidence representation and trusted verification contract outside the
  immutable snapshot and existing producer attestation;
- production Business Entity, Assessment Engagement, Resource, Principal,
  Membership, and Entitlement sources and currentness;
- Dashboard Resource association, EIP artifact-instance/revision identity,
  retrieval, and protected release realization.

No field, database, event bus, API, signature extension, or infrastructure
mechanism is selected.

## 17. Future Verification and Acceptance Criteria

Future separately authorized verification must demonstrate exact same-A
continuity from legitimate submission context through one successful
Assessment Service result, validated snapshot bytes, and valid producer
attestation; exact A/B and applicable E agreement; distinction between
identical snapshots for different attempts; rejection of failed, missing,
duplicate, substituted, replayed, revoked, stale, and unavailable evidence;
preservation of immutable snapshot and signing contracts; and zero protected
dashboard content on every rejected path. It must prove no assessment truth,
publication, entitlement, or Resource identity authority moved to the
Continuity Authority.

Phase 2A and Phase 2C remain local proofs. They do not establish the missing
production A-to-snapshot continuity source.

## 18. Production Exclusions and Authority Status

This document establishes a conceptual continuity governance decision only.
It does not authorize implementation, Assessment Service changes, Trusted
Authorization changes, EIP or Website changes, production identifier creation,
snapshot schema or signing changes, administrative APIs, storage, transport,
deployment, or production release. Concrete authority-source and lifecycle
contracts require later explicit approval.

**PRODUCTION AUTHORITY: NOT GRANTED.**
