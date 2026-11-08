# CEP v3 Publication, Binding, and Continuity Logical Authority-Source Decision v1

**Status: FOUNDER APPROVED — LOGICAL SOURCE ARCHITECTURE ONLY**

**Approval date:** 2026-11-08

**Decision authority:** Nguyen AI Enterprise LLC founder/owner.

## 1. Decision and scope

The founder conditionally approves three logically independent sources of
record: an EIP Publication Register, a Continuity Authority Instance Bridge
Register, and a Binding Authority Current-Selection Register. This establishes
their intended logical separation and existing authority ownership for future
nonproduction v3 Dashboard `EXPLAIN` development. It does not establish a live
source, production integration, release eligibility, or principal access.

This decision applies beneath the approved
[Stage 4H.5A limited content eligibility decision](cep-v3-recommendation-action-explain-eligibility-decision-v1.md)
and [Stage 4H.5B versioned delivery specification](cep-v3-recommendation-action-explain-delivery-contract-proposal-v1.md).
It preserves the [EIP artifact identity and revision governance](eip-artifact-instance-revision-identity-governance-v1.md),
the [Assessment Instance Snapshot Continuity Authority governance](assessment-instance-snapshot-continuity-authority-governance-v1.md),
and the [Executive Dashboard Resource-to-Artifact Binding Authority governance](executive-dashboard-resource-artifact-binding-authority-governance-v1.md).
Those decisions remain authoritative in their respective domains; this record
does not amend their source, actor, or release boundaries.

## 2. Approved logical sources and owners

| Independent source of record | Logical owner and authority | Required logical capabilities | Authority excluded |
| --- | --- | --- | --- |
| **1. EIP Publication Register** | Executive Intelligence Platform; authoritative approval and lifecycle state for one exact governed EIP artifact. | Exact artifact identity; distinguishable publication occurrence and associated revision; explicit approval; current effective publication state; withdrawal, supersession, and applicable revocation or invalidation; auditable transitions; trusted fresh current-state retrieval. | Does not grant principal access or select an artifact for a Resource. |
| **2. Continuity Authority Instance Bridge Register** | Conceptual Assessment Instance Snapshot Continuity Authority; authoritative association of a particular governed assessment execution with its exact successful, signed producer snapshot. | Stable assessment-instance identity or separately approved equivalent; legitimate execution association; exact attested snapshot identity; Business Entity and applicable scope; current association; invalidation or revocation; auditable transitions; trusted fresh current-state retrieval. | Does not produce or alter assessment truth, insert instance identity into immutable producer content, publish EIP artifacts, or select a Dashboard Resource. |
| **3. Binding Authority Current-Selection Register** | Conceptual Resource-to-Artifact Binding Authority; authoritative current selection for one exact governed Dashboard Resource and applicable scope. | Exact Resource identity; Business Entity isolation; authoritative Client, Engagement, and workspace scope where applicable; assessment-instance, snapshot, and artifact linkage; exact EIP publication occurrence and revision; at most one effective current selection per governed binding scope; explicit replacement, withdrawal, and revocation; auditable transitions; trusted fresh current-state retrieval. | Does not create, repair, or override EIP publication approval or principal authorization. |

Distinct assessment executions remain distinct even if their deterministic
signed snapshot bytes and `producerSnapshotIdentity` match. The Continuity
Authority must distinguish the executions through a governed instance bridge
outside the immutable producer snapshot and attestation. An Assessment
Submission Resource is not an Executive Dashboard Resource. Engagement and
workspace scope are required only where the governed Resource scope requires
them; Client and Business Entity are not presumed identical.

The three logical sources must remain independently controlled. Shared future
physical infrastructure is permissible only if logical authority, mutation
permissions, evidence provenance, environment separation, and trusted
current-state verification remain independent. This decision selects no
physical infrastructure, database, cloud account, API, storage product, or
production custodian.

## 3. Authority lifecycle and release invariants

1. Historical signed evidence, an old `published` indicator, or possession of
   artifact bytes does not prove present currentness. Each authority must
   support a trusted fresh read of its effective state.
2. Withdrawal, revocation, invalidation, and applicable supersession defeat
   older positive evidence. Current-state ambiguity, conflict, missing
   evidence, or source unavailability fails closed.
3. A new publication occurrence or record does not silently supersede an
   older one. An authorized, auditable transition must establish replacement
   or supersession in the applicable authority domain.
4. Revocation or withdrawal does not reactivate a previous publication
   revision, continuity association, or Resource binding. Restoration requires
   a separate authorized current determination.
5. EIP publication currentness, continuity of the exact assessment instance
   to its signed snapshot, and Resource-specific current selection must each
   be verified under their own authority. None supplies another's decision.
   Principal `EXECUTIVE_DASHBOARD × EXPLAIN` access remains a separate fresh
   Trusted Authorization decision under the approved v3 field-scope contract.
6. Business Entity and environment isolation remain enforced. Wrong or
   unresolved applicable Client, Engagement, or workspace scope fails closed.
   The Website, browser, AI model, and caller assertions cannot create or
   approve authority records.
7. No standing super-admin role or universal mutation right is created.
   Synthetic fixtures and local proof evidence remain non-authoritative for
   production and cannot activate client-facing release.

## 4. Reserved founder decisions — NOT YET APPROVED

The following require separate bounded decisions before production source
realization or integration. The founder's general ownership of Nguyen AI
Enterprise LLC does not assign any actor or permanent administrative privilege:

- Concrete EIP publication approver, publication source custodian, and
  publication establishment, mutation, withdrawal, supersession, and
  revocation actors.
- Publication occurrence and revision uniqueness domains; revision-series
  scope; retry and idempotency semantics; and evidence of authorized
  lifecycle transitions.
- Concrete Continuity Authority custodian; stable assessment-instance source
  or approved equivalent; authorized execution-to-snapshot handoff; and
  continuity establishment, invalidation, restoration, and revocation actors.
- Concrete Binding Authority custodian and binding creation, replacement,
  withdrawal, restoration, and revocation actors.
- Final evidence field schemas, trusted retrieval and verification contracts,
  current-state generation and freshness requirements, audit custody, and
  environment-separation controls for all three sources.
- Physical storage, infrastructure, cloud account, API, deployment, and
  production authority-source integration.

This record does not choose AWS DynamoDB, Amazon RDS, S3, or another product.
No unresolved source fact is assigned to Assessment Service, EIP, Trusted
Authorization, Website, or an individual merely because they can transport,
consume, or inspect its evidence.

## 5. Explicit non-authorizations

This approval does not authorize production authority-source integration;
physical infrastructure; specific source custodians, approvers, mutation or
revocation actors; final field schemas; live EIP publication eligibility;
Resource-binding activation; principal access; client-facing v3 delivery;
REPORT eligibility; Website or Trusted Authorization changes; deployment; or
production release. The Stage 4H.4 internal v3 projection remains
`release_eligible=False`. This document is not an executable release flag.

Assessment Service retains immutable producer truth, methodology, snapshot
identity, and attestation. EIP retains delivery and publication authority.
The Continuity Authority owns only the cross-boundary instance-to-snapshot
association. The Binding Authority owns only the Resource-specific current
selection. Trusted Authorization alone composes principal access decisions;
Website presentation cannot create authority. No approved governance is
reopened by this decision.

## 6. Next bounded implementation milestone — NOT AUTHORIZED

**Stage 4H.6D — Internal EIP Synthetic v3 Publication-Evidence Adapter** is
the recommended next milestone in
`/Users/aiadmin/projects/executive-intelligence-platform`. Its expected
bounded scope is one new adapter module, one focused test module, and one
implementation evidence document. A separate founder instruction is required
before implementation.

The future adapter would use synthetic authority evidence only; verify exact
v3 artifact identity, publication occurrence and revision, producer lineage,
and current-state generation; reject withdrawal, supersession, stale, forged,
and conflicting evidence; retain `release_eligible=False`; preserve the
existing v2 publisher; and avoid client-facing release. Synthetic validation
would not establish a live EIP publication register, Binding Authority source,
principal authorization, production readiness, or publication permission.

**Stage 4H.6C disposition:** founder logical design decision recorded; Founder-approved logical authority-source decision;
controlled Git promotion authorized separately.
Implementation and production authority remain unapproved. **Stage 4H.6D:** not authorized.
**V3 client-facing publication:** not authorized. **Roadmap Stage 4:** in progress.
