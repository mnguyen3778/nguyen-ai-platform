# Trusted Authorization Corrective Implementation Governance v1

Version: v1

## 1. Purpose

This artifact governs one narrowly bounded corrective implementation phase for
the first Trusted Authorization implementation in:

```text
/Users/aiadmin/aws-ai-knowledge-assistant
```

It exists only to close post-implementation governance findings identified after
review of implementation checkpoint:

```text
bf0f21f0f00ec210b5091c1cab8ba2af1e1e2ce1
```

This artifact does not authorize production authority, integration, deployment,
public contract expansion, persistence, or broader authorization scope.

## 2. Governance Status

Status: BOUNDED CORRECTIVE IMPLEMENTATION AUTHORIZED

The corrective phase is authorized only if it remains within the exact boundary
defined here and preserves all predecessor governance.

## 3. Authoritative Predecessor Artifacts

This artifact inherits and preserves:

- Trusted Authorization Implementation Readiness Governance v1;
- Deterministic Authorization Decision Semantics v1;
- Resource x Action Applicability Governance v1;
- Requested Action Permission Vocabulary Governance v1;
- Stable Principal Mapping Authority Governance v1;
- Principal Mapping Authority Source Governance v1;
- Business Entity Authority Source Governance v1;
- Membership Authority Source Governance v1;
- Entitlement Semantics Governance v1;
- Entitlement Authority Source Governance v1;
- Resource Identity Authority Source Governance v1;
- Governed Resource Identity Lookup Governance v1;
- Resource Classification Authority Governance v1;
- Runtime Owner Assignment Governance v1;
- Portal Governed Delivery Authorization Model v1;
- EIP Governed Retrieval Boundary v1; and
- Architecture Conformance Baseline v1.

Predecessor governance remains authoritative. This artifact clarifies corrective
implementation authority only where the post-implementation review found gaps.

## 4. Corrective Findings

The corrective phase may address only these findings:

1. Authority lifecycle state is not sufficiently explicit.
2. Governed version/context validation is incomplete.
3. Governance-to-code-to-test traceability is incomplete.
4. Positive automated evidence is narrower than the governed applicability
   surface.

No other finding, feature, integration, or implementation expansion is
authorized by this artifact.

## 5. Finding Classification

| Finding | Governance classification | Rationale |
| --- | --- | --- |
| Authority lifecycle state explicitness | GOVERNANCE CLARIFICATION REQUIRED | Existing governance requires lifecycle and revocation fail-closed behavior, but the implementation review showed that omitted lifecycle state can be represented as `ACTIVE`. This artifact clarifies that absence of required lifecycle state is missing authority and must not become active authority by default. |
| Governed version/context validation | ALREADY REQUIRED | Existing governance requires governance/version context, deterministic reproducibility, and DENY for unsupported governance/version. The correction is implementation conformance, not a new semantic decision. |
| Governance-to-code-to-test traceability | ALREADY REQUIRED | Existing readiness governance already requires explicit governance requirement to implementation component to automated evidence traceability. |
| Positive evidence across applicable v1 surface | GOVERNANCE CLARIFICATION REQUIRED | Existing governance requires positive ALLOW evidence and governs the complete v1 Resource x Action applicability surface. This artifact clarifies that corrective verification must cover each APPLICABLE bounded v1 Resource x Action pair. |

No finding requires a new broad authorization model. No finding is outside the
authorized Trusted Authorization ownership domain if implemented within this
artifact.

## 6. Lifecycle State Clarification

For the corrective phase, every authority-bearing record relied upon to produce
ALLOW must carry explicit lifecycle state sufficient to determine current
authority.

Authority-bearing records include at minimum:

- Principal Mapping;
- Business Entity;
- Membership;
- Governed Resource;
- Entitlement; and
- any governed version/context authority record if represented as authority
  evidence.

Missing lifecycle state, malformed lifecycle state, unsupported lifecycle state,
inactive state, disabled state, revoked state, expired state, terminated state,
stale state, unknown state, ambiguous lifecycle state, conflicting lifecycle
state, or unavailable lifecycle evidence must produce DENY.

Implementation must not treat omitted lifecycle state, constructor defaults,
fixture defaults, adapter defaults, cached values, prior ALLOW, or inferred state
as explicit current active authority.

This clarification does not require all authority to contain expiration windows.
Where temporal validity is present or required, predecessor temporal validity
governance remains authoritative.

## 7. Governed Version / Context Validation

The corrective phase must validate governed version/context as an authorization
input before ALLOW.

At minimum, validation must cover:

- deterministic authorization semantics version;
- Resource x Action applicability governance version;
- bounded implementation evaluation context; and
- any additional governed version/context input required by the implemented
  first-slice authority model.

Missing, malformed, unsupported, stale, conflicting, ambiguous, incompatible, or
unavailable governed version/context must produce DENY.

Emitting a version string in audit evidence is not sufficient. The version or
context must be validated as part of the authority conditions required for
ALLOW.

This artifact does not select an API field, header, database column, schema,
transport, storage mechanism, or persistence representation for governed
version/context.

## 8. Traceability Completion

The corrective phase must provide explicit traceability:

```text
GOVERNANCE REQUIREMENT
-> IMPLEMENTATION COMPONENT
-> AUTOMATED VERIFICATION / EVIDENCE
```

Traceability may be implemented in code comments, tests, documentation, a table,
or another reviewable repository-local mechanism. The format is not governed.

Traceability must cover at minimum:

- explicit lifecycle-state requirement;
- lifecycle fail-closed behavior;
- governed version/context validation;
- version/context fail-closed behavior;
- ALLOW/DENY-only decision semantics;
- default-DENY behavior;
- Business Entity isolation;
- membership enforcement;
- entitlement enforcement;
- governed resource lookup;
- requested-action and applicability enforcement;
- minimum necessary audit evidence;
- AI/LLM non-authority;
- Website/browser non-authority; and
- absence of unauthorized integration or production authority.

## 9. Positive Evidence Clarification

The corrective phase must include deterministic positive ALLOW evidence for each
APPLICABLE pair in the bounded v1 Resource x Action applicability matrix:

| Governed Resource class | Applicable actions requiring positive ALLOW evidence |
| --- | --- |
| Executive Dashboard | VIEW, EXPLAIN |
| Report | VIEW, DOWNLOAD, EXPLAIN |
| Assessment Submission | SUBMIT |

Each positive case must still prove all required predicates for ALLOW:

- valid trusted authentication evidence;
- authoritative stable Principal mapping;
- authoritative Business Entity;
- valid Membership where required;
- authoritative governed Resource identity;
- canonical Requested Action;
- APPLICABLE Resource x Action governance;
- applicable Entitlement;
- explicit active lifecycle state for all required authority records;
- valid governed version/context; and
- no blocking stale, revoked, conflicting, unavailable, unsupported, or
  indeterminate state.

Positive evidence for one applicable pair must not imply positive evidence for
another pair.

## 10. Corrective Implementation Boundary

The subsequent corrective implementation may change only what is necessary in
`/Users/aiadmin/aws-ai-knowledge-assistant` to:

- require explicit lifecycle state for authority-bearing records;
- deny when lifecycle state is missing, malformed, unsupported, stale, revoked,
  inactive, disabled, expired, terminated, unknown, conflicting, ambiguous,
  unavailable, or otherwise non-authoritative;
- validate governed version/context before ALLOW;
- deny when governed version/context is missing, malformed, unsupported, stale,
  conflicting, ambiguous, incompatible, unavailable, or otherwise
  non-authoritative;
- produce governed denial reason categories sufficient for audit review;
- preserve minimum necessary audit evidence;
- complete explicit governance-to-code-to-test traceability;
- add deterministic positive evidence for every APPLICABLE bounded v1 Resource x
  Action pair; and
- add deterministic negative/fail-closed evidence for the corrected lifecycle and
  governed version/context behaviors.

Permitted implementation surfaces are limited to the existing Trusted
Authorization domain/model, evaluator, applicability/version-context handling,
fixture/evidence adapters, audit evidence, and automated tests needed for this
corrective phase.

## 11. Out of Scope

This artifact does not authorize:

- Cognito integration;
- Website or Client Engagement Portal integration;
- EIP integration;
- Assessment Service integration;
- persistence;
- API or runtime wiring;
- deployment;
- production authority-source integration;
- production authorization;
- public contract changes;
- methodology changes;
- new Resource classes;
- new Requested Actions;
- new Entitlement semantics;
- new Business Entity semantics;
- broader administrative authorization;
- SoD expansion;
- AI/LLM authorization authority;
- Website/browser authorization authority;
- IAM business-authorization authority; or
- changes to any repository other than `/Users/aiadmin/aws-ai-knowledge-assistant`.

## 12. Acceptance Criteria

The corrective implementation is acceptable only when automated evidence proves:

1. ALLOW is impossible unless every required authority-bearing record carries
   explicit active lifecycle state.
2. Missing lifecycle state produces DENY.
3. Malformed or unsupported lifecycle state produces DENY.
4. Inactive, disabled, revoked, expired, terminated, stale, unknown,
   unavailable, ambiguous, or conflicting lifecycle state produces DENY.
5. ALLOW is impossible unless required governed version/context is valid and
   compatible with the bounded v1 implementation.
6. Missing, malformed, unsupported, stale, conflicting, ambiguous,
   incompatible, or unavailable governed version/context produces DENY.
7. Equivalent governed inputs under equivalent governed version/context produce
   equivalent decisions and equivalent governed reason categories.
8. Every APPLICABLE bounded v1 Resource x Action pair has a positive ALLOW test.
9. NOT APPLICABLE, unknown, unsupported, mismatched, or unresolved Resource x
   Action pairs produce DENY.
10. Business Entity, Resource, Action, Membership, and Entitlement isolation are
    preserved.
11. Audit evidence supports reconstruction without unnecessary PII, raw identity
    provider claims, tokens, protected Assessment Service content, protected EIP
    content, or unrelated Business Entity data.
12. Traceability from governance requirement to implementation component to
    automated evidence is explicit and reviewable.
13. No AI, LLM, prompt, model, vector search, retrieval generation, browser
    state, Website state, Cognito group/claim, IAM permission, or prior ALLOW is
    necessary or sufficient to produce authorization ALLOW.
14. No public contract, endpoint, persistence, deployment, production authority
    source, integration, or cross-repository change is introduced.

## 13. Production Authority

This governance step does not grant production authority.

Completion of the corrective implementation does not grant production authority,
production deployment, production data access, production authorization
enforcement, public contract expansion, or client reliance.

Production authority remains downstream and requires a separate governed
production-readiness review.

## 14. Architecture Decision

One corrective Trusted Authorization implementation phase is authorized to
proceed only within `/Users/aiadmin/aws-ai-knowledge-assistant` and only for the
bounded corrective responsibilities defined in this artifact.

Implementation must stop and return to governance if it requires any integration,
production authority source, persistence, public contract, new Resource class,
new Requested Action, new entitlement semantics, new Business Entity semantics,
broader administrative authorization, SoD expansion, or cross-repository change.
