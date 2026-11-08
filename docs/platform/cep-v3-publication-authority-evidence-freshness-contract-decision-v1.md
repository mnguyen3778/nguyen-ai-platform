# CEP v3 Publication Authority Evidence and Freshness Contract Decision v1

**Stage:** 4H.6E

**Decision status:** FOUNDER APPROVED — MINIMUM BEHAVIORAL CONTRACT ONLY

**Approval date:** 2026-11-08

**Implementation status:** NOT AUTHORIZED

**Git promotion:** Authorized through a separate founder instruction; promotion
completion is verified through the repository's Git history.

## 1. Purpose and inherited authority

The founder approves the minimum behavioral contract for a *future*
authoritative EIP Publication Register. This is a Platform governance decision,
not a final evidence schema, live authority source, implementation plan, or
publication decision. It is subordinate to the approved
[three-register logical source architecture](cep-v3-publication-binding-continuity-logical-authority-source-decision-v1.md),
[EIP artifact instance and revision identity governance](eip-artifact-instance-revision-identity-governance-v1.md),
[Resource-to-Artifact Binding Authority governance](executive-dashboard-resource-artifact-binding-authority-governance-v1.md),
[Assessment Instance Snapshot Continuity Authority governance](assessment-instance-snapshot-continuity-authority-governance-v1.md),
[limited v3 content eligibility](cep-v3-recommendation-action-explain-eligibility-decision-v1.md),
and the [v3 EXPLAIN delivery specification](cep-v3-recommendation-action-explain-delivery-contract-proposal-v1.md).
The [Trusted Authorization administrative mutation and revocation governance](trusted-authorization-administrative-mutation-revocation-ownership-governance-v1.md)
preserves bounded actor authority, audit, and fail-closed lifecycle rules; this
decision appoints no actors and reopens no bootstrap or root decision.

EIP owns artifact production, publication approval, eligibility, lifecycle,
version compatibility, and freshness. Assessment Service owns producer truth,
snapshot identity, and attestation. The Continuity Authority owns the
particular assessment-instance-to-snapshot association. The Binding Authority
owns exact Resource-specific current artifact selection. Trusted Authorization
owns principal access decisions. The Website and AI model create none of these
facts. These authorities remain logically independent even if future physical
infrastructure is shared under separately approved controls.

## 2. Read-only Stage 4H.6D evidence and its limit

The promoted EIP
[Stage 4H.6D synthetic verifier](../../../executive-intelligence-platform/src/executive_intelligence_platform/projection_delivery/non_production_v3_publication_evidence.py)
and [implementation evidence](../../../executive-intelligence-platform/docs/stage4h6d-internal-v3-publication-evidence-adapter-evidence-v1.md)
demonstrate local fixture checks for identity, producer lineage, occurrence,
revision, generation, withdrawal, supersession, revocation, and conflict.
Fixture equality is not live publication provenance or approval. Its synthetic
integrity hash covers a canonical internal projection and verification evidence;
it is not automatically the identity or integrity proof of the exact serialized
artifact that a future publication would approve. The verifier's
`(series, revision)` uniqueness check is local fixture behavior, not universal
governance. Its accepted result remains `release_eligible=False`, with no
client serializer or live register. This decision does not promote that
synthetic proof into production authority.

## 3. Publication identity and integrity contract

Every EIP publication decision must identify one exact governed artifact and
verify integrity against the *approved published representation* under its
supported delivery and serialization context. An internal projection hash or
producer snapshot digest alone cannot prove identity of those published bytes.
Producer snapshot identity, EIP artifact content identity, publication
occurrence, and governed revision are distinct. Identical artifact bytes may
belong to separate publication occurrences; an explicit authoritative retry
decision is needed to treat a repeat as the same occurrence.

Occurrence and revision identity must be unambiguous within explicit
authoritative scopes. A newer occurrence or revision neither approves nor
automatically supersedes another. Retries and duplicate transitions must not
create conflicting current authority. Missing, duplicate, conflicting, or
ambiguous occurrence or revision evidence fails closed. Final identifier
formats, uniqueness domains, sequencing, and idempotency mechanisms remain
reserved.

## 4. Explicit approval evidence contract

Authoritative evidence for a publication must establish, together:

- exact approved artifact identity and integrity, with verified producer
  snapshot, admission, derivation, and delivery lineage;
- applicable Business Entity, environment, publication scope, package and
  methodology versions, delivery contract version, and approved v3 field scope;
- distinguishable publication occurrence, associated revision, explicit EIP
  publication approval decision, decision provenance, and applicable lifecycle
  state.

Publication approval is an EIP-owned affirmative decision. It cannot be
inferred from a producer signature, artifact existence, synthetic verifier
`PASS`, newer revision, caller-provided `current` flag, or possession of prior
published bytes. The concrete approver and decision representation are not
selected here. Approval evidence does not establish present currentness,
Resource selection, assessment continuity, principal authorization, or
client-facing release eligibility.

## 5. Trusted current-state read contract

A future read-only trusted boundary must establish lookup scope server-side and
request the exact artifact, occurrence, revision, Business Entity, environment,
and applicable publication context. The authoritative source must return a
complete scoped view: effective current publication state, source-issued
authority generation, relevant lifecycle transitions, verifiable source and
read provenance, and explicit unavailable, missing, partial, stale, or
conflicting outcomes. A successful response must not silently omit conflicting
current claims within the governed scope. Ambiguous or incomplete outcomes
fail closed.

This contract defines behavior, not an API, database, isolation level,
storage consistency mechanism, or concrete response schema. A source read is
evidence only for its exact scope and observed generation; it cannot grant
Resource binding or Principal access.

## 6. Freshness and concurrency contract

Currentness must derive from trusted authoritative source evidence. A
historical signed record, retrieval time, TTL, cache age, or prior successful
verification is insufficient. Source-issued generation and applicable
lifecycle ordering must be verifiable so that a stale cached positive result
cannot override newer authoritative state. Source unavailability or unresolved
concurrent mutation fails closed. A new read must establish whether the
selected occurrence and revision remain approved, effective, compatible, and
fresh in the exact scope; no standing release authority follows from an
earlier read.

Concrete freshness windows, generation formats, clock rules, consistency
mechanisms, cache strategy, and retrieval implementation remain reserved.
Source-state time, where applicable, is provenance to verify, not a substitute
for current authority.

## 7. Publication lifecycle contract

Explicit, authorized, auditable transitions are required for publication
approval, EIP-owned current publication selection within an applicable
publication scope, withdrawal, supersession, revocation, and invalidation.
Each transition must identify the exact affected scope, occurrence, revision,
prior and resulting state, and trusted decision provenance. Lifecycle ordering
must be deterministic and conflicts must fail closed. A newer record does not
implicitly approve or supersede an older one. Known current revocation,
withdrawal, or invalidation defeats older positive evidence. No revocation
automatically restores an earlier revision, and no older revision becomes a
fallback. Repeated or replayed transitions must not create duplicate or
broader authority.

EIP's current publication selection is distinct from the Binding Authority's
current selection for one Dashboard Resource. Neither can override the other.
Concrete mutation, withdrawal, supersession, and revocation actors remain
unapproved.

## 8. Audit and provenance contract

Verification must retain enough trusted evidence to identify the authoritative
source, exact observed state generation, source-state time where applicable,
trusted retrieval provenance, relevant lifecycle transition references,
audit correlation, complete scoped-read semantics, and Business Entity and
environment isolation. Historical transitions remain traceable without
rewriting earlier approval meaning. Audit evidence does not itself authorize
publication, mutation, Resource binding, or release. This decision chooses no
signing scheme, audit platform, retention period, database, or custodian.

## 9. Admission and release boundary

The required authority chain remains separate:

```text
Assessment Service producer authenticity
  -> EIP publication approval and currentness
  -> assessment-instance continuity
  -> Resource-to-Artifact binding
  -> fresh exact-resource Trusted Authorization
  -> separately governed client-facing release eligibility
```

This is a verification order, not new runtime implementation. The protected
boundary must verify current authoritative state at admission and immediately
before release. A changed publication generation; withdrawal, revocation, or
supersession; changed continuity or Resource binding; changed principal
authorization; or unresolved concurrent mutation invalidates the earlier
positive result. Unknown or unavailable required evidence fails closed with
no protected content. The approved v3 `EXPLAIN` field scope stays explicit and
version-specific; existing v2 Dashboard delivery, `VIEW`, and six EXPLAIN
subjects remain unchanged. This contract grants no client-facing v3
publication or release flag change.

## 10. Stage and implementation boundaries

- **Stage 4:** Complete bounded synthetic end-to-end Assistant explanation
  verification. Stage 4H.6D synthetic verifier is closed and promoted; Stage 4
  remains in progress.
- **Stage 5:** Governed durable EIP publication and current-state integration,
  subject to separate authority, evidence, and infrastructure decisions.
- **Stage 6:** Production identity and Trusted Authorization authority-source
  integration, subject to separate approval.
- **Stage 7:** Approved API/runtime orchestration and release controls, subject
  to separate approval.

This Stage 4H.6E decision moves no Stage 5, 6, or 7 implementation into Stage
4. It authorizes no live register, production integration, deployment, or
client-facing release.

## 11. Reserved founder decisions — NOT YET APPROVED

Concrete publication custodian; publication approver; establishment,
mutation, withdrawal, supersession, and revocation actors; final artifact,
occurrence, revision, generation, and evidence schemas; exact uniqueness
domains, sequencing, retry, and idempotency rules; trusted retrieval contract;
freshness windows; storage consistency and concurrency mechanism; physical
infrastructure; API endpoints; production authentication and authorization
integration; deployment; and release authority remain unresolved. No standing
super-admin role, implicit production readiness, or actor assignment follows
from founder ownership or this behavioral decision.

**Disposition:** Founder minimum behavioral contract decision recorded locally.
Implementation not authorized; Git promotion: Authorized through a separate
founder instruction; promotion completion is verified through the repository's Git history.
Live publication and client-facing v3 release not authorized. Roadmap Stage 4
remains in progress; Roadmap Stage 5 has not started.
