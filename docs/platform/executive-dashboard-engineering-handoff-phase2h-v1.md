# Executive Dashboard Engineering Handoff — Phase 2H v1

Status: final Phase 2 governance closeout; local engineering readiness decision.
Production authority: **NOT GRANTED**.

## 1. Purpose

Freeze the approved Phase 2A–2G decisions into one bounded engineering handoff.
The first task is a local, deterministic proof of assessment-instance-to-snapshot
continuity. This handoff records implementation order and verification criteria;
it creates no new authority, production source, API, or architecture decision.

## 2. Frozen governance baseline

The governing decisions are [Resource-to-Artifact Binding Authority v1](executive-dashboard-resource-artifact-binding-authority-governance-v1.md),
[Assessment Instance Snapshot Continuity Authority v1](assessment-instance-snapshot-continuity-authority-governance-v1.md),
and [EIP Artifact Instance and Revision Identity v1](eip-artifact-instance-revision-identity-governance-v1.md).
They are closed decisions, not subjects for another conceptual review.

Inherited boundaries remain in force: [Resource Identity Authority](resource-identity-authority-source-governance-v1.md)
and [Business Entity Authority](business-entity-authority-source-governance-v1.md)
establish their own current facts; [Assessment Submission attempt binding and
allocation](trusted-authorization-assessment-submission-attempt-resource-binding-allocation-governance-v1.md)
preserve exact A/E/B and `A -> R` provenance; [administrative mutation and
revocation](trusted-authorization-administrative-mutation-revocation-ownership-governance-v1.md)
remain separately governed. The Assessment Service alone owns successful
execution, immutable snapshot bytes, identity, and producer attestation. EIP
alone owns verified admission, derivation, publication, artifact occurrence,
revision, eligibility, freshness, and lineage. [Governed retrieval](eip-governed-retrieval-boundary-v1.md)
transports an EIP artifact, while [dashboard delivery authorization](portal-governed-delivery-authorization-model-v1.md)
requires fresh principal/Resource/`VIEW` authorization at trusted release.
Website is a presentation consumer. Neither a valid signature, EIP publication,
Resource binding, nor a `VIEW` ALLOW substitutes for the others.

The approved continuity rule conditionally reuses exact submission attempt A.
It requires a governed bridge from legitimate A/E/B and actual submission
through one successful producer execution to exact validated snapshot bytes and
valid attestation. Same-A conflicting outcomes fail closed; equal snapshot
bytes from distinct attempts do not merge those attempts. Assessment Submission
Resource R is distinct from Executive Dashboard Resource identity.

## 3. Existing implementation evidence

| Status | Evidence at reviewed HEAD | Limit |
| --- | --- | --- |
| Implemented and tested | Assessment Service `src/assessment/executive_snapshot_handoff.py` produces a snapshot only from successful orchestration/runtime and validates serialization; `producer_snapshot_attestation.py` issues and verifies exact-byte signed sidecars. `tests/test_executive_snapshot_handoff.py` and `tests/test_producer_snapshot_attestation.py` cover success and failures. | Current producer handoff carries no governed A-to-execution association. Attestation proves bytes and producer provenance, not A/B/E. |
| Implemented and tested | EIP `projection_delivery/verified_admission.py` uses `VerifiedSnapshotGateway` to verify the sidecar and preserve admission lineage. `projection_delivery/delivery.py` publishes immutable, deterministically serialized delivery contract instances and checks governed publication eligibility. `tests/projection_delivery/test_verified_admission.py` and `test_delivery.py` cover invalid producer and delivery evidence. | Current delivery bytes do not establish a distinct publication occurrence, governed revision, or current lifecycle source. |
| Implemented and tested | Trusted Authorization has `GovernedResource`, Resource/action applicability, `TrustedAuthorizationEvaluator`, and non-production attempt A/E/B and `A -> R` components. `tests/test_trusted_authorization_dashboard_delivery_handoff.py` supplies a Phase 2A synthetic VIEW handoff; `test_trusted_authorization_verified_eip_delivery_handoff.py` supplies a Phase 2C verified EIP local handoff and negative paths. | Synthetic records and local handoffs establish no production Resource, continuity, binding, entitlement, or release authority. |
| Implemented and tested | Website `src/lib/website-projection-delivery-client.ts` and `website-projection-delivery.ts` consume and validate delivery for rendering; `tests/frontend/executive-dashboard-projection-delivery.test.mjs` covers projection delivery. | Presentation validation does not establish trusted authorization, artifact binding, or production retrieval. |

These are code and test inventories, not a claim that the suites were rerun in
Phase 2H. The website repository context file is advisory and its embedded
snapshot describes an older commit; the Git preflight establishes current HEAD.

## 4. Missing implementation contracts

Governed but unimplemented: an authoritative A-to-successful-execution-to-
snapshot continuity bridge; EIP publication-occurrence/revision and current
state evidence; exact Resource-to-artifact current binding; joint trusted
release verification; governed retrieval integration; and Website integration
with that trusted release. The first local slice needs only synthetic A/E/B
and submission/execution evidence, exact producer bytes and sidecar, and
deterministic verification. Concrete production authority sources, actors,
custody, currentness, revocation propagation, and transport remain production
integration dependencies. Their absence does not block the local proof.

## 5. Engineering dependency order

1. Prove assessment-instance continuity from exact A and authoritative-shape
   synthetic context through successful execution, snapshot, and attestation.
2. Establish EIP publication-instance/revision evidence and current EIP state,
   preserving verified producer lineage. This depends on exact producer
   snapshot evidence; it does not create assessment-instance authority.
3. Establish exact Resource-to-artifact current binding using continuity,
   publication/revision, and authoritative-shape Resource/B/conditional scope.
4. Verify all current facts jointly at trusted dashboard release, including
   fresh `EXECUTIVE_DASHBOARD`/`VIEW` ALLOW and revocation checks.
5. Integrate governed retrieval of the exact eligible EIP delivery artifact.
6. Integrate Website presentation of only the trusted released delivery.

Each item is a separate bounded implementation responsibility. Steps 2–6 are
dependencies for eventual protected delivery, not work authorized by Step 1.
No AWS infrastructure is needed for Step 1.

## 6. First implementation slice

**Target:** one non-production, deterministic continuity verifier for exact
submission attempt A -> one successful Assessment Service execution -> exact
attested `ExecutiveAssessmentSnapshot`. It verifies supplied evidence; it
does not establish or mutate any authoritative source fact.

**Proposed location, not existing code:**
`aws-ai-knowledge-assistant/src/trusted_authorization/non_production_assessment_snapshot_continuity.py`,
with targeted tests in
`tests/test_trusted_authorization_non_production_assessment_snapshot_continuity.py`.
Keep it outside the production evaluator and release path. Reuse the existing
non-production attempt-binding/business-context/resource-lifecycle fixtures,
Assessment Service snapshot production and `ProducerSnapshotIssuer`/
`ProducerSnapshotVerifier` test fixtures, and ephemeral local keys. Cross-repository
fixture loading is for local tests only; no new package or runtime dependency
is approved. Do not alter producer serialization or signing.

Completion is a verifier and targeted tests that establish one exact accepted
local proposition and reject every applicable negative in section 10. It does
not create a Dashboard Resource, EIP artifact, binding, VIEW decision, or
protected-content release.

## 7. Owning repository

`/Users/aiadmin/aws-ai-knowledge-assistant` is the **local test-only
implementation repository** because it already holds the non-production
Assessment Submission A/E/B evidence components and synthetic trusted handoff
tests. This is custody of a bounded verification proof, not assignment of the
production Continuity Authority. Phase 2F assigns that conceptual association
to Continuity Authority but assigns no concrete production repository or
source. Assessment Service remains producer of truth and attestation; Trusted
Authorization remains principal/Resource/action evaluator. No cross-context
customer-instance authority is transferred by this local placement.

## 8. Input/output contract

**Inputs, all local and synthetic except producer-owned code behavior:** exact
attempt A; current, unambiguous legitimate A/E/B context and applicable scope
with source/provenance references; A-to-Assessment Submission R binding and
actual submitted state; an explicit same-A-to-producer-execution custody
assertion supplied by the test harness; successful producer result; snapshot
constructed from that result and its exact validated serialized bytes;
matching `producerSnapshotIdentity`; signed producer-snapshot-attestation-v1
sidecar; trusted local verifier key/release configuration; and current
non-revoked, non-conflicting local evidence. A test fixture must mark its
synthetic assertions as such. Existing request/correlation IDs, digest, or
attestation cannot stand in for A or the missing custody assertion.

**Valid output:** an immutable local verification result containing accepted
status and exact A, B, applicable E, submission provenance, successful
execution provenance, producer snapshot identity, byte identity, attestation
issuer/release/version/key references, and evidence references sufficient to
compare repeat evaluations. It is a verified *local proposition*, never an
authority record or dashboard release token. Exact field representation is an
implementation detail; preserve the approved distinctions and versioned
producer contract.

**Invalid output:** a deterministic non-accepted result with a stable,
non-disclosing reason category and no accepted continuity evidence. A caller
must receive no partial accepted object and no protected dashboard fields.
This is a local error contract, not a new production error vocabulary.

## 9. Fail-closed behavior

Verify each required link independently and compare exact A/B/E, submission,
execution, bytes, identity, and attestation. Require a successful runtime and
successful snapshot validation/serialization/attestation; verify the signed
sidecar over the same exact bytes with the existing producer verifier. Check
current local evidence for one accepted outcome per A. A same-A repeat of the
identical established outcome may be idempotent only when provenance also
matches; a second conflicting outcome is rejected. Distinct A values remain
distinct even when snapshot bytes and identity match. Missing, malformed,
stale, revoked, replayed, conflicting, or unavailable required evidence
rejects. Known revocation dominates historical positive evidence. No fallback
to another attempt, scope, snapshot, prior result, or synthetic dashboard
content is permitted. The verifier must not infer submission or execution
from SUBMIT ALLOW, post-ALLOW eligibility, `A -> R`, request ID, or signature.

## 10. Acceptance test matrix

| Case | Required result |
| --- | --- |
| Exact A/E/B, actual submission, one successful producer result, exact validated bytes and valid sidecar | Accept one immutable local proposition; repeat verification is deterministic. |
| Same A and identical established outcome/provenance | Idempotent same result; no second association. |
| A1 and A2 produce identical deterministic snapshot bytes | Preserve two distinct instance propositions; never substitute A1 evidence for A2. |
| Missing A or wrong A identity | Reject. |
| Wrong Business Entity or wrong required Engagement | Reject even if snapshot and signature are valid. |
| Unsubmitted A, SUBMIT ALLOW alone, or post-ALLOW eligibility alone | Reject. |
| Unsuccessful or ambiguous execution | Reject. |
| Missing producer snapshot, failed snapshot validation, or execution-to-bytes custody gap | Reject. |
| Invalid sidecar/signature/issuer/key/release/version, tampered bytes, or snapshot identity mismatch | Reject through producer verification. |
| Duplicate conflicting execution or conflicting continuity evidence for the same A | Reject; do not choose newest or first. |
| Revoked association, attempt replay, or prior accepted evidence after revocation | Reject; historical evidence remains non-permissive. |
| Required authority evidence missing, stale, ambiguous, or unavailable | Reject with no accepted proposition. |

Every rejection is fail closed and releases zero protected dashboard fields.
Tests may assert that no release operation exists in this slice; they must not
pretend to prove an integrated dashboard release.

## 11. Regression requirements

Run the new targeted continuity tests, existing Trusted Authorization
non-production attempt/business-context/submission lifecycle tests used by
the fixture, and the Assessment Service producer snapshot handoff and
attestation tests. Check that existing immutable snapshot bytes and signed
sidecar fields remain unchanged. Do not run a full cross-platform regression
suite merely to complete the first slice. Correct concrete defects found by
these tests, then rerun only affected targeted and regression tests.

## 12. Explicit exclusions

No Assessment Service, EIP, Website, or Platform code change in Step 1. No
methodology change, persistent authority state, new framework, customer data,
AWS call, Cognito integration, production API/endpoint, infrastructure,
deployment, EIP publication/revision, Resource binding, governed retrieval,
or Website presentation change. Do not put A/B/E in immutable snapshot bytes
or the producer attestation. Do not turn `A -> R` into Dashboard Resource
identity or use attestation as customer-instance authority.

## 13. Local engineering authorization boundary

**ENGINEERING GO for a separately requested local implementation of Step 1**
in the named repository, with synthetic identities/data, ephemeral signing
keys, in-memory evidence, and existing local fixtures. The present Phase 2H
task authorizes this handoff document only and changes no source or tests.
The owning repository's explicit implementation instruction is the next task;
the approved Phase 2F rules are sufficient to start that local code without
another architecture review. Execution order: (1) implement only Step 1;
(2) targeted verification and regression; (3) fix concrete defects only;
(4) record PASS or BLOCKED against section 10; (5) advance to the next
dependency only after PASS and a separately bounded implementation request.

## 14. Production authority exclusions

This local proof cannot claim production customer identity, Business Entity
or Engagement authority, live administrative mutation/revocation authority,
live assessment-instance custody, artifact currentness, principal entitlement,
production retrieval, protected dashboard release, or deployment readiness.
The production Continuity Authority source/owner and authorized lifecycle
actors remain unresolved, as do later EIP publication, Binding Authority,
retrieval, and release integrations. Those production choices are separately
gated; they do not invalidate a local deterministic proof.

## 15. Implementation GO/BLOCKED decision

**GO — local engineering readiness for Step 1 only.** The exact first target,
existing producer verification components, synthetic attempt fixtures, and
negative test oracles make the proof independently testable. There is no
earlier implementation dependency that requires a live authority source or
AWS. **Production authority remains NOT GRANTED.** If the chosen repository
cannot preserve the test-only boundary or a targeted test exposes a concrete
contract contradiction, mark Step 1 BLOCKED and correct that specific defect;
do not reopen unrelated Phase 2 decisions.

## 16. Next Codex execution instruction

In `/Users/aiadmin/aws-ai-knowledge-assistant`, implement only the proposed
non-production assessment-snapshot continuity verifier and targeted tests
under sections 6–12. Read that repository's current instructions and state;
reuse existing synthetic A/E/B components and Assessment Service producer
fixtures. Return the exact test results, defects corrected, and Step 1
PASS/BLOCKED decision. Do not implement Steps 2–6 or claim production
Continuity Authority. The next task is implementation, not governance.
