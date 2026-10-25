# EIP Artifact Instance and Revision Identity Governance v1

Version: v1

## 1. Purpose

This decision defines the minimum governed identity and revision semantics for
an EIP-produced Website Projection Delivery Contract. It distinguishes exact
artifact content, an EIP publication occurrence, a governed revision, and
current EIP publication eligibility from the separate Resource-specific
current selection owned by the Executive Dashboard Resource-to-Artifact
Binding Authority.

## 2. Status and Scope

Status: CONCEPTUAL GOVERNANCE DECISION. Production realization is unresolved.

The bounded subject is the identity and lifecycle evidence needed for one
specific EIP delivery artifact to be recognized, compared, superseded,
withdrawn, and verified at a trusted release boundary. This document does not
create a production identifier, field, schema, source, service, persistence
mechanism, API, or implementation authorization.

## 3. Inherited Approved Governance

This decision inherits, without reopening:

- [Executive Dashboard Resource-to-Artifact Binding Authority Governance v1](executive-dashboard-resource-artifact-binding-authority-governance-v1.md).
- [Assessment Instance Snapshot Continuity Authority Governance v1](assessment-instance-snapshot-continuity-authority-governance-v1.md).
- [EIP Governed Retrieval Boundary v1](eip-governed-retrieval-boundary-v1.md).
- [Governed Resource Identity / Lookup Governance v1](governed-resource-identity-lookup-governance-v1.md).
- [Resource Identity Authority Source Governance v1](resource-identity-authority-source-governance-v1.md).
- [Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md).
- [Trusted Authorization Administrative Mutation and Revocation Ownership Governance v1](trusted-authorization-administrative-mutation-revocation-ownership-governance-v1.md).
- [Repository Ownership Baseline v1](repository-ownership-v1.md).

EIP's
`docs/architecture/website-facing-projection-delivery-contract-versioning-policy-architecture-v1.md`
remains authoritative for delivery versioning, compatibility, publication,
eligibility, freshness, classification, limitations, and lineage. Assessment
Service producer-snapshot-attestation-v1 remains authoritative for exact
upstream snapshot-byte provenance. Neither contract is changed here.

## 4. Existing EIP Representations

Current EIP implementation has `VerifiedSnapshotGateway`, which verifies
Assessment Service snapshot bytes and signed sidecar, admits the snapshot, and
rechecks continuity through derivation and delivery. Internal
`VerificationEvidence` retains issuer, producer release, snapshot identity,
digests, attestation version, and key reference. Governed dashboard publication
requires verified admission and rejects substituted delivery content.

`WebsiteProjectionDeliveryContractInstance` is immutable and serializes its
delivery deterministically. Its delivery representation carries
`deliveryContractVersion`, `publicationPolicyVersion`, producer snapshot
lineage, version context, publication and eligibility indicators,
compatibility, freshness, classification, and limitations. Existing tests
verify deterministic repeat publication, immutable instances, and rejection
of invalid delivery or producer evidence.

These are reusable producer representations. They do not currently establish
a stable publication-occurrence identity, distinct governed revision identity,
authoritative current publication history, explicit supersession relation,
or withdrawal transition record. Repeated publication of the same delivery
result can yield identical serialized bytes. An indicator carried in earlier
bytes is not, by itself, proof of the producer's later current state.

## 5. Artifact Identity Distinctions

| Identity | Governed meaning | Existing representation and limit |
| --- | --- | --- |
| Contract family identity | The EIP-owned delivery definition and version. | `website-projection-delivery-contract-v1` / `deliveryContractVersion` exists; it does not identify an artifact instance. |
| Artifact content identity | The exact serialized delivery bytes under the applicable contract and serialization semantics. | Deterministic `serialize()` and exact-byte comparison are reusable; no distinct governed content-identity reference is selected here. Equal bytes do not distinguish publication occurrences. |
| Publication instance identity | One specific EIP-authorized publication occurrence and its provenance. | Required logical identity; no stable representation exists in reviewed delivery code. It must distinguish separate occurrences even with equal bytes. |
| Artifact revision identity | One governed revision in an applicable EIP publication series or scope, with traceable predecessor/successor relationships where changed. | Required logical identity and scope; no reviewed revision field or lifecycle source exists. It is distinct from contract and policy versions. |
| Producer snapshot identity | Exact Assessment Service snapshot bytes and signed producer provenance. | `producerSnapshotIdentity` and verified admission exist; neither identifies an EIP publication occurrence nor a customer assessment instance. |
| Resource-specific current selection | The revision approved now for one exact Dashboard Resource and business scope. | Phase 2D.1 Binding Authority owns this determination; EIP publication status does not create it. |

No identity may be inferred solely from an object address, caller reference,
transport location, browser selector, timestamp, contract version, snapshot
digest, or prior authorization result. This decision does not mandate a
digest or any concrete identifier format.

## 6. Publication-Instance Authority

EIP alone establishes that a particular immutable delivery representation
was produced and approved for one governed publication occurrence. Minimum
authoritative evidence must make the following propositions verifiable:

1. The exact serialized artifact and supported contract/serialization context.
2. Its verified producer snapshot, admission, derivation, and delivery lineage.
3. The EIP publication decision and applicable policy/version context.
4. A publication occurrence distinguishable from every other occurrence in
   its governed identity domain, including occurrences with equal bytes.
5. The associated governed revision and publication scope.
6. Its current EIP-owned publication status, eligibility, and lifecycle
   relationship to any replacement, supersession, or withdrawal.
7. Provenance sufficient to audit establishment and later state changes.

Successful serialization, artifact possession, or a `published` value in old
bytes does not itself establish current publication-instance authority. EIP
must be able to reject missing, duplicate, ambiguous, conflicting, stale,
revoked, or unavailable publication evidence. Concrete evidence representation,
establishment actor, and source remain future EIP implementation decisions.

## 7. Revision Identity

A governed revision distinguishes a publication's content and approval
position within its applicable EIP publication series or scope. Its identity
must be stable for audit and unambiguous within that scope. A revision must
remain associated with the exact approved publication occurrence and content
evidence; it may not silently point to altered bytes or another producer
snapshot.

Repeated publication of identical bytes is a separate publication occurrence
unless EIP authoritatively determines that the operation is a retry of the
same occurrence. Equal bytes alone cannot make that determination. A new
publication occurrence does not automatically create a new revision, and a
new revision does not automatically supersede an earlier one. EIP must make
each relationship explicit and auditable. The representation, uniqueness
domain, and permitted retry semantics are unresolved implementation contracts.

## 8. Producer Lineage and Artifact Integrity

EIP must preserve verified Assessment Service attestation, exact snapshot-byte
identity, verified admission, catalog/derivation/package/projection lineage,
delivery version context, and exact artifact integrity through publication
and retrieval. A consumer must verify that retrieved content is the artifact
approved for the specified EIP publication occurrence and revision. An
attestation valid for a different snapshot, or content valid for a different
publication occurrence, cannot satisfy the selected instance.

Phase 2F Continuity Authority separately establishes the particular customer
assessment instance and its snapshot. EIP producer lineage does not replace
that association, and this decision does not alter immutable snapshots or
their signed sidecars.

## 9. Publication Lifecycle

EIP retains sole authority for artifact production, publication, eligibility,
compatibility, freshness, classification, limitations, and publication
lifecycle. A first publication requires verified lineage, exact content,
governed publication approval, a distinguishable occurrence, and an associated
revision before that instance can support protected delivery.

Publication state must be determinable from current EIP authority, not solely
from historical serialized indicators, cache state, or consumer inference.
Where EIP designates a single-current revision within a governed publication
series, conflicting current claims fail closed. Multiple separately scoped
EIP publications may exist; this document does not define one global current
artifact across all clients, resources, or publication scopes.

EIP must preserve historical identity and state-transition evidence without
silently rewriting earlier publication meaning. No storage or event mechanism
is selected.

## 10. Supersession, Withdrawal, and Invalidation

An EIP replacement or supersession requires an authoritative, auditable
determination identifying the affected prior publication/revision and the
resulting producer state. The prior occurrence becomes noncurrent for EIP
delivery where the transition applies. Historical integrity does not restore
eligibility. Withdrawal, revocation, invalidation, or loss of required
compatibility/freshness prevents delivery even when bytes and original
attestation remain valid.

No newer publication silently supersedes an earlier one, and no EIP change
silently changes a Resource-specific Binding Authority selection. Neither
withdrawal nor revocation reactivates an older revision. Restoration or
replacement requires its own separately authorized EIP determination under
existing lifecycle governance.

## 11. Resource-Specific Currentness Boundary

Protected release requires the conjunction of three separate current facts:

```text
EIP: exact publication instance and revision are currently eligible
+ Binding Authority: that exact revision is currently selected for R/B/scope
+ Trusted Authorization: this principal currently has R / VIEW ALLOW
```

The Binding Authority must also preserve Phase 2F's approved assessment-
instance-to-snapshot continuity and the exact EIP artifact association.
Resource Identity Authority supplies the exact Dashboard Resource and
Business Entity, plus applicable Client, Engagement, or workspace scope.
Engagement and workspace remain conditional on governed Resource scope.

The trusted server-side release boundary must verify exact artifact bytes,
EIP publication identity/revision and current eligibility, producer lineage,
Resource-specific current selection, assessment continuity, and fresh
principal authorization immediately before releasing protected fields. None
of these authorities is sufficient alone. An EIP publication is not approved
for every Resource; a Binding Authority selection cannot publish; a VIEW ALLOW
cannot validate an artifact.

## 12. Revision Lifecycle Decision Matrix

Every unresolved or contradictory state below blocks protected release. The
table governs outcomes, not storage or concurrency mechanisms.

| Event | Owner; prior to resulting state and required evidence | Trusted release requirement |
| --- | --- | --- |
| 1. First publication | EIP; no approved occurrence to one approved occurrence/revision, with verified content, lineage, policy, and identity evidence. | Require current EIP approval and separate Resource selection; otherwise zero fields. |
| 2. Repeated identical bytes | EIP; prior occurrence to explicit same-occurrence retry or distinguishable new occurrence, with authority/provenance. | Reject ambiguous identity or presumed currentness from byte equality. |
| 3. New revision | EIP; prior governed series to a distinct revision with exact content and relationship evidence. | Require current eligibility; new revision alone does not change Resource selection. |
| 4. Publication replacement | EIP; prior publication to explicit replacement decision and resulting state, preserving old identity/history. | Reject old publication if no longer eligible; require Binding Authority selection of replacement. |
| 5. Supersession | EIP; previously eligible occurrence to noncurrent where governed, with predecessor/successor evidence. | Reject superseded occurrence; no older fallback. |
| 6. Withdrawal | EIP; published occurrence to withdrawn/non-deliverable, with withdrawal authority and audit evidence. | Reject regardless of old `published` bytes or Binding Authority selection. |
| 7. Invalidation | EIP; formerly eligible occurrence to non-deliverable after failed provenance, integrity, compatibility, or policy evidence. | Reject and expose no protected fields. |
| 8. Concurrent publication change | EIP; previously observed state to re-established current producer state, or unresolved. | Recheck current state at release; unresolved change blocks. |
| 9. Concurrent Resource binding change | Binding Authority; previously selected revision to current exact selection, or unresolved. | Recheck selection at release; EIP cannot resolve this change. |
| 10. Publication-source unavailability | EIP source; current producer state cannot be established. | Fail closed; do not use cached positive status. |
| 11. Conflicting revision records | EIP source; incompatible identity, relationship, or current-state claims remain conflicting. | Fail closed; no newest-wins or duplicate fallback. |
| 12. Historical artifact replay | EIP and Binding Authority; old valid occurrence presented after state or selection change. | Compare both current authorities; reject the historical instance. |

## 13. Authority Ownership

Assessment Service owns immutable assessment truth, snapshot identity, and
producer attestation. EIP owns verified admission, delivery artifact content,
publication-instance and revision authority, publication status, eligibility,
freshness, supersession, withdrawal, and artifact lineage. Phase 2F Continuity
Authority owns the customer assessment-instance-to-snapshot association;
Phase 2D.1 Binding Authority owns the Resource-specific artifact association
and current selection. Resource Identity and Business Entity authorities own
their respective identity/scope facts. Trusted Authorization alone composes
principal VIEW ALLOW/DENY. Retrieval transports governed EIP output; Website
presents authorized content.

EIP publication ownership does not assign retrieval runtime ownership. EIP,
the Binding Authority, the Continuity Authority, Trusted Authorization,
retrieval, and Website cannot acquire one another's decision authority by
holding or validating evidence.

## 14. Negative Verification Matrix

Every rejection below releases **zero protected dashboard fields**. These
cases extend the existing Phase 2D.1 fail-closed matrix for EIP identity and
revision; they do not create new production error codes.

| Case | Required logical rejection |
| --- | --- |
| 1. Missing publication-instance identity | Exact governed occurrence cannot be established; reject. |
| 2. Duplicate publication identity | Distinct occurrences share an authoritative identity; reject ambiguity. |
| 3. Wrong publication instance | Retrieved occurrence differs from the selected one; reject. |
| 4. Identical bytes from distinct publications | Equal content does not collapse occurrence identity; reject substitution. |
| 5. Unsupported contract version | Governed compatibility absent; reject. |
| 6. Incorrect producer lineage | Snapshot or downstream lineage differs; reject. |
| 7. Invalid producer attestation | Exact-byte or trusted-producer proof fails; reject. |
| 8. Artifact content substitution | Retrieved bytes differ from approved occurrence content; reject. |
| 9. Unpublished artifact | Current EIP publication approval absent; reject. |
| 10. Withdrawn artifact | Current EIP withdrawal removes eligibility; reject. |
| 11. Superseded artifact | Current EIP state is noncurrent; reject. |
| 12. Stale artifact | Current EIP freshness does not pass; reject. |
| 13. Conflicting current revisions | EIP or Resource selection cannot resolve one applicable current revision; reject. |
| 14. Wrong Resource association | Binding Authority selects a different Resource; reject. |
| 15. Cross-Business-Entity artifact | Resource/business scope and continuity disagree; reject without disclosure. |
| 16. Earlier ALLOW followed by entitlement revocation | Fresh Trusted Authorization no longer permits VIEW; reject. |
| 17. Publication-source unavailability | Current EIP state cannot be verified; reject. |
| 18. Binding-source unavailability | Current Resource selection cannot be verified; reject. |
| 19. Older artifact replay | Historical validity cannot establish currentness; reject. |
| 20. Concurrent publication or binding change | Required states cannot be jointly re-established at release; reject. |

No failure may select an older, previous-client, cross-scope, synthetic, or
demo artifact. Caller-visible denial must not disclose another Business
Entity's artifact existence or status.

## 15. Fail-Closed Requirements

The trusted release boundary must re-establish the exact publication
occurrence, revision, current EIP eligibility, exact artifact integrity,
approved producer lineage, current Resource binding, assessment continuity,
and fresh principal authorization. Missing, unsupported, stale, withdrawn,
revoked, conflicting, ambiguous, substituted, replayed, or unavailable
authority yields zero protected dashboard fields. A prior EIP `published`
indicator, prior binding, prior ALLOW, or valid historical signature cannot
override current authority.

## 16. Unresolved Implementation Dependencies

Future separately authorized work must resolve EIP publication-instance and
revision identity representation; uniqueness and revision scope; authoritative
publication-state source, history, supersession, withdrawal and retry
evidence; exact-content verification representation; authorized publication
and lifecycle actors; current-state disclosure to a trusted consumer; and
retrieval realization. Phase 2F continuity source, Phase 2D.1 Binding
Authority source/current selection, production Resource/Business Entity and
principal-authorization sources, and protected dashboard release remain
independent prerequisites.

This decision does not choose a database, transaction, lock, queue, event bus,
cache, API, cryptographic format, digest format, or runtime repository for
retrieval.

## 17. Acceptance Criteria

Future separately authorized implementation verification must prove that
contract version, exact bytes, publication occurrence, revision, producer
snapshot, and Resource-specific current selection remain distinguishable;
identical bytes can belong to distinct publication occurrences; publication
and revision changes are auditable; producer lineage and integrity survive
retrieval; current EIP status and Binding Authority selection are rechecked
at release; all section 14 negatives withhold every protected field; and no
Assessment Service truth, EIP publication, Binding Authority selection, or
Trusted Authorization entitlement ownership moves across boundaries.

Existing EIP deterministic publication and Phase 2A/2C handoff tests are
local evidence only. They do not establish a production publication-instance
or revision authority source.

## 18. Explicit Non-Authority Boundaries and Production Exclusions

This decision does not authorize EIP to decide principal entitlement or
Resource-specific current selection. It does not authorize the Binding
Authority or Continuity Authority to publish EIP artifacts; Trusted
Authorization to create publication state or business truth; retrieval to
derive or revise EIP content; or Website to decide producer eligibility.

It does not modify Assessment Service attestation, snapshot serialization,
EIP contracts, methodology, Resource identity, principal authorization, or
Website presentation. No production implementation, source, schema, API,
storage, infrastructure, deployment, or administrative workflow is approved.

## 19. Authority Status

This document establishes conceptual EIP publication-instance and revision
identity governance only. Concrete authority sources, representations, and
runtime integration require separate explicit approval. It does not grant
production release authority.

**PRODUCTION AUTHORITY: NOT GRANTED.**
