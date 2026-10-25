# Executive Dashboard Resource-to-Artifact Binding Authority Governance v1

Version: v1

## 1. Purpose and Scope

This decision establishes the conceptual Resource-to-Artifact Binding Authority
for one governed `EXECUTIVE_DASHBOARD` Resource and its authoritative business
scope. The authority determines which specific EIP-produced Website Projection
Delivery Contract instance, and which current approved revision of that
instance, is associated with that Resource. It does not create the artifact.

This is a bounded Platform governance decision. It defines authority and
fail-closed semantics, not a production authority source, schema, service,
endpoint, storage design, or implementation approval.

## 2. Status and Inherited Governance

Status: CONCEPTUAL GOVERNANCE DECISION. Production realization is unresolved.

This decision inherits the following governance without reopening it:

- [Repository Ownership Baseline v1](repository-ownership-v1.md).
- [Runtime Owner Assignment Governance v1](runtime-owner-assignment-governance-v1.md).
- [Governed Resource Identity / Lookup Governance v1](governed-resource-identity-lookup-governance-v1.md).
- [Resource Identity Authority Source Governance v1](resource-identity-authority-source-governance-v1.md).
- [Client / Organization Identity Authority Governance v1](client-organization-identity-authority-governance-v1.md).
- [Business Entity Authority Source Governance v1](business-entity-authority-source-governance-v1.md).
- [Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md).
- [EIP Governed Retrieval Boundary v1](eip-governed-retrieval-boundary-v1.md).
- [Resource x Action Applicability Governance v1](resource-action-applicability-governance-v1.md).
- [Trusted Authorization Administrative Mutation and Revocation Ownership Governance v1](trusted-authorization-administrative-mutation-revocation-ownership-governance-v1.md).

EIP's
`docs/architecture/website-facing-projection-delivery-contract-versioning-policy-architecture-v1.md`
remains authoritative for EIP publication, eligibility, and freshness. This
decision does not alter that EIP-owned contract or its rules.

## 3. Inherited Authority Boundaries

The Assessment Service alone owns deterministic assessment business truth,
`ExecutiveAssessmentSnapshot` production, producer attestation, and producer
snapshot identity. EIP owns verified producer admission, governed intelligence
derivation, Website Projection Delivery Contract production, publication,
eligibility, compatibility, freshness, classification, limitations, version
context, and lineage.

Resource Identity Authority establishes governed Resource identity and its
Business Entity association and applicable scope. Business Entity Authority
establishes the Business Entity fact. Trusted Authorization consumes verified
subject and principal evidence, current Business Entity, Membership,
Entitlement, Resource, Action, and applicability evidence to compose the
deterministic `EXECUTIVE_DASHBOARD` / `VIEW` ALLOW or DENY decision. This
document grants none of those source authorities to Trusted Authorization.

The Website consumes approved delivery content for presentation only.
Governed retrieval transports already-produced EIP artifacts; retrieval has
neither principal entitlement authority nor EIP publication authority. The
future deterministic trusted logical service is assigned to the
`aws-ai-knowledge-assistant` repository by Runtime Owner Assignment Governance
v1. That assignment does not assign a binding source, retrieval mechanism, or
production implementation authority.

## 4. Binding Authority Decision

The Resource-to-Artifact Binding Authority is the conceptual governed business
authority over this exact association:

```text
Governed Executive Dashboard Resource
    -> Authoritative Business Scope
    -> Particular Assessment Instance
    -> Producer Snapshot Identity
    -> Specific EIP Delivery Artifact
    -> Current Approved Artifact Revision
```

It must establish and resolve that association from authoritative evidence
within each upstream owner's domain. A binding must be exact, current,
unambiguous, auditable, governed by lifecycle controls, and independent of
browser assertions. It must preserve the distinction between Resource
identity, business scope identity, assessment association, snapshot identity,
artifact identity, and revision currentness. Identity or availability in one
layer does not establish authority in another.

The Binding Authority owns the Resource-specific association and current
selection. EIP remains authoritative for whether the selected artifact is
published, eligible, and fresh. Both determinations are required for release.
The concrete production Binding Authority source and authorized mutation
actors remain unresolved.

## 5. Business Scope Requirements

The binding must resolve the exact current governed Resource and authoritative
Business Entity association. It must include an authoritative Client
relationship when applicable. Client and Business Entity must not be assumed
identical.

Engagement and workspace associations are required only when the governed
Resource scope requires them. Their applicability and identity must be
authoritative and current; neither is made mandatory for every Resource by
this decision. A missing required association, wrong scope, or unresolved
scope applicability blocks release. Browser selectors, email addresses,
display names, prior selections, and producer lineage alone cannot establish
business scope.

## 6. Particular Assessment Instance

The binding must identify one particular assessment instance or an equivalently
unambiguous governed association between the Resource and that assessment.
`assessmentVersion` identifies a contract family, not a unique customer
assessment. `producerSnapshotIdentity` identifies exact snapshot bytes and
does not necessarily distinguish two customer executions with identical
deterministic snapshot content. Neither value alone establishes the complete
Resource-to-assessment association.

The authority source and representation of this instance association are
unresolved. This decision creates no production identifier field and does not
promote runtime request metadata into deterministic assessment truth.

## 7. Artifact Identity, Provenance, and Integrity

The binding must identify one specific EIP-produced
`website-projection-delivery-contract-v1` instance, or a separately governed
future version, and preserve its exact relationship to the assessment instance
and producer snapshot. Required evidence includes Assessment Service
attestation and snapshot identity, EIP verified admission and publication,
artifact integrity, supported version context, and complete producer-to-
delivery lineage.

The Binding Authority cannot create, repair, or replace EIP publication,
eligibility, compatibility, freshness, classification, limitations, or
provenance verification. Contract version, publication policy version,
`authorizationScopeState`, or possession of artifact bytes does not by itself
establish the Resource-specific binding or principal entitlement. The concrete
artifact-instance and revision representation remains unresolved.

## 8. Current Revision and Supersession

For one exact governed binding scope, at most one artifact may be current and
approved. Releasable dashboard content requires exactly one. Initial EIP
publication does not automatically bind an artifact to a Resource. Initial
selection requires authoritative Resource, business scope, assessment,
snapshot, artifact, and EIP approval evidence.

Replacement becomes current only through an authoritative, auditable Binding
Authority determination supported by current EIP producer state. The formerly
current selection then becomes noncurrent. Its historical validity does not
make it releasable. Missing, conflicting, stale, or unavailable current
selection fails closed. There is no implicit fallback to an earlier revision,
another Resource, Client, engagement, or workspace.

EIP's own `published` and `current` requirements remain independently
binding. A Binding Authority selection cannot turn EIP `superseded`, `stale`,
`revoked`, `unpublished`, or ineligible state into a releasable artifact.

## 9. Withdrawal, Revocation, and Scope Change

Resource revocation, binding withdrawal, artifact withdrawal, EIP publication
invalidation, assessment association invalidation, authoritative business
scope change, and supersession each block protected release whenever they
invalidate a required current relationship. Known current revocation
dominates stale positive evidence. A prior ALLOW or prior artifact selection
cannot override later authority state.

Revocation or withdrawal never reactivates an earlier revision. Any future
restoration requires a separately authorized current determination under the
respective authority sources, with preserved lineage and auditability. This
document does not assign administrators or define mutation workflows.

## 10. Trusted Release Invariants

Immediately before protected dashboard fields leave the trusted server-side
release boundary, all of the following must be established together:

1. Server-verified identity and current Principal Mapping.
2. Current authoritative Business Entity association, Membership, and
   Entitlement.
3. A fresh `EXECUTIVE_DASHBOARD` / `VIEW` ALLOW for the exact governed Resource.
4. The applicable authoritative Client, engagement, and workspace scope.
5. The exact Resource-to-assessment association and producer snapshot lineage.
6. The exact EIP artifact binding and one current approved revision.
7. Verified EIP provenance and artifact integrity.
8. Current EIP publication and eligibility, supported delivery contract
   version, valid compatibility and freshness, required classification and
   limitations, and complete version context and lineage.
9. No intervening revocation, withdrawal, scope change, or supersession.

Required current authority state must be rechecked at this protected release
boundary. A VIEW ALLOW cannot establish artifact validity; a valid artifact
cannot establish VIEW entitlement. Missing, stale, conflicting, unavailable,
or contradictory evidence yields zero protected dashboard fields.

## 11. Negative Authorization and Failure Matrix

Every case below requires logical rejection and release of zero protected
dashboard fields. These are failure expectations, not new production error
codes.

| Case | Required authority check and rejection basis |
| --- | --- |
| Cross-tenant Resource association | Resource and Business Entity authority; reject a different Business Entity. |
| Incorrect Client relationship | Authoritative Client relationship where applicable; reject mismatch or missing required relationship. |
| Wrong engagement or workspace | Authoritative conditional scope; reject mismatch or unresolved required scope. |
| Missing assessment-instance association | Binding Authority; reject absent or ambiguous particular assessment. |
| Incorrect snapshot lineage | Assessment Service attestation and EIP lineage; reject mismatch. |
| Multiple current artifacts | Binding Authority current selection; reject conflict. |
| Superseded artifact | Binding supersession and EIP freshness; reject noncurrent artifact. |
| Revoked artifact | Respective artifact and binding lifecycle authority; reject revocation. |
| Unpublished artifact | EIP publication authority; reject unpublished state. |
| Stale artifact | EIP freshness and binding currentness; reject stale state. |
| Valid artifact for another Resource | Exact Resource-to-artifact binding; reject substitution. |
| Prior ALLOW followed by revocation | Fresh Trusted Authorization and lifecycle state; reject prior decision reuse. |
| Prior selection followed by supersession | Recheck current binding and EIP state at release; reject prior selection. |
| Missing or conflicting authority records | Each required authority; reject absence, conflict, or ambiguity. |
| Retrieval unavailability | Governed retrieval boundary; reject unavailable artifact or authority. |
| Detached artifact integrity failure | Exact artifact integrity and provenance; reject altered or substituted bytes. |

No rejection may trigger synthetic or demo content, prior-client content,
cross-scope content, an older artifact, or reconstructed producer content.
Caller-visible failure must not disclose another Business Entity's Resource
or artifact existence.

## 12. Explicit Non-Authority Boundaries

The Binding Authority does not produce assessment truth, recalculate scores,
modify the 48-question methodology, derive executive intelligence, publish
EIP artifacts, grant VIEW entitlement, authenticate users, render dashboard
content, or operate retrieval merely because it owns a binding.

Trusted Authorization consumes binding evidence but does not create business
truth, binding source facts, or EIP publication. EIP and Website cannot grant
principal entitlement. Browser assertions, email, `assessmentVersion`, a
prior ALLOW, EIP `authorizationScopeState`, and Phase 2A/2C synthetic fixture
identifiers cannot establish binding authority.

## 13. Unresolved Production Dependencies

This decision does not select or authorize:

- a concrete production Binding Authority source;
- administrative actors, mutation rights, or workflows;
- unique assessment-instance association or its representation;
- artifact-instance identity representation;
- current revision and supersession representation;
- storage, transaction, synchronization, or locking mechanisms;
- retrieval runtime ownership, mechanism, or transport;
- production identity verification;
- production Principal Mapping, Business Entity, Resource, Membership, or
  Entitlement sources;
- a protected dashboard VIEW application operation; or
- a production release endpoint and operational controls.

Each required dependency must be governed and separately authorized before
production implementation. This decision grants no implicit authority to a
repository, runtime, storage system, or producer for an unresolved source.

## 14. Verification and Acceptance Criteria

Future implementation verification must prove exact binding resolution,
single-current selection, fresh authorization, provenance and integrity
continuity, revocation and supersession enforcement, deterministic fail-closed
rejection, no cross-tenant leakage, no older-artifact fallback, no browser-
derived authority, and zero protected content when a required dependency
fails. The section 11 cases are minimum negative coverage.

Phase 2A and Phase 2C are local proofs only. Their synthetic binding records
and locally verified delivery behavior do not establish a production Binding
Authority source or production release readiness.

## 15. Authority Status and Implementation Gate

This document establishes the conceptual governance decision only. It does
not establish a live authority source, authorize runtime implementation, or
grant production deployment authority. Approved predecessor governance
continues to control each inherited responsibility. Any production source,
service contract, retrieval design, or implementation requires its own
explicit approval.

**PRODUCTION AUTHORITY: NOT GRANTED.**
