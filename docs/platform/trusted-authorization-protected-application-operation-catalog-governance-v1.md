# Trusted Authorization Protected Application Operation Catalog Governance v1

Version: v1

## 1. Purpose

This artifact defines the current governed product/application operation
catalog for the bounded non-production Trusted Authorization
application-operation selection proof.

It resolves the blocked Layer-2 product architecture fact:

Which application-owned operations may be treated as protected Trusted
Authorization operations before they are mapped to
`NonProductionApplicationOperation`.

This artifact does not authorize implementation.

## 2. Scope

This artifact governs only the product/application operation semantics needed
for a future non-production selector proof.

It does not govern or authorize:

- runtime activation;
- handler wiring;
- authentication integration;
- Cognito integration;
- AWS integration;
- persistence;
- production authority sources;
- production operation catalog;
- deployment;
- final ALLOW or DENY enforcement.

## 3. Definitions

Layer 1 - Transport / External Event:
HTTP method, route, request body, browser event, UI control, JSON field,
assistant message, provider string, function name, AI output, or any other
external/runtime representation. Layer 1 is not operation authority.

Layer 2 - Governed Protected Application Operation:
A stable application-owned capability identity meaning: this application
capability is executing this specific protected operation.

Layer 3 - Trusted Authorization Operation:
The existing non-production authorization operation vocabulary represented by
`NonProductionApplicationOperation`.

## 4. Three-Layer Trust Model

The approved direction is:

```text
real application capability
        ->
governed protected application operation identity
        ->
NonProductionApplicationOperation
        ->
RequestedAction
        ->
deterministic Trusted Authorization
```

The following reverse direction is prohibited:

```text
RequestedAction exists
        ->
invent application operation
```

## 5. Protected Application Operation Ownership

Protected application operation identity is owned by governed application
capability architecture.

It is not owned by:

- browser or UI;
- HTTP method;
- route string;
- API Gateway event shape;
- Lambda dispatch condition;
- Python function name;
- provider or producer identifier;
- Bedrock model or runtime provider;
- AI, LLM, MCP, or agent output;
- role, group, scope, owner, or admin flag;
- resource identifier format or resource-name pattern.

## 6. Current Application Capability Inventory

| Application Capability | Exists Today? | Protected TA Operation? | Layer-2 Operation Identity | Mapped NonProductionApplicationOperation | Status | Rationale |
| --- | --- | --- | --- | --- | --- | --- |
| Assessment submission and deterministic scoring | Yes | Yes | `PROTECTED_ASSESSMENT_SUBMISSION` | `SUBMIT_ASSESSMENT` | ACCEPTED CURRENT | The implementation repository contains assessment request validation and deterministic scoring. The capability is to submit an assessment for scoring, independent of `POST /assessment`. |
| Assistant invocation | Yes | No current mapping | None | None | NOT A TA OPERATION | Current assistant invocation is a conversational/runtime capability. It does not currently map to VIEW, DOWNLOAD, or SUBMIT, and AI must not select authorization operation identity. |
| Report viewing | No | Not current | None | None | DEFERRED | No current report-view delivery surface was identified in the implementation repository. |
| Report downloading | No | Not current | None | None | DEFERRED | No current report-download delivery surface was identified in the implementation repository. |

## 7. Current Protected Operation Catalog

The current catalog contains exactly one accepted current protected operation:

| Layer-2 Operation Identity | Product/Application Meaning | Layer-3 Mapping | Status |
| --- | --- | --- | --- |
| `PROTECTED_ASSESSMENT_SUBMISSION` | Application code is submitting an assessment for deterministic scoring. | `NonProductionApplicationOperation.SUBMIT_ASSESSMENT` | ACCEPTED CURRENT |

`PROTECTED_ASSESSMENT_SUBMISSION` is not the route `/assessment`.

`PROTECTED_ASSESSMENT_SUBMISSION` is not the HTTP method `POST`.

`PROTECTED_ASSESSMENT_SUBMISSION` is not a browser form or button.

It is the application capability of submitting an assessment for deterministic
scoring.

## 8. Deferred Candidate Operations

The following candidates are deferred:

| Candidate | Required Before Entry |
| --- | --- |
| Report viewing | A real report-view application capability and resource relationship. |
| Report downloading | A real report-download application capability and resource relationship. |
| Assistant access to authorized governed content | A separately governed assistant resource/use operation model. |

Deferred candidates must not be selected by a future operation selector.

## 9. Operation To Non-Production Operation Relationship

The only current governed mapping is:

```text
PROTECTED_ASSESSMENT_SUBMISSION
        ->
NonProductionApplicationOperation.SUBMIT_ASSESSMENT
```

No current Layer-2 operation maps to:

- `NonProductionApplicationOperation.VIEW_RESOURCE`;
- `NonProductionApplicationOperation.DOWNLOAD_RESOURCE`.

Those mappings remain unavailable until real governed product/application
capabilities exist.

## 10. Transport Independence

Operation identity must survive route, method, or framework changes.

If the assessment submission endpoint changes from `/assessment` to another
route, the protected application operation remains
`PROTECTED_ASSESSMENT_SUBMISSION` if the application capability remains
assessment submission for deterministic scoring.

No operation may be inferred solely from:

- `/assessment`;
- `/v1/assistant`;
- `/report/*`;
- `GET`;
- `POST`;
- `PUT`;
- `DELETE`.

## 11. UI Independence

No browser or UI field may establish operation identity.

The following are non-authoritative:

- button text;
- form name;
- browser route;
- hidden input;
- frontend action string;
- client-provided operation label.

## 12. Provider Independence

Provider selection is not operation authority.

The following must not select a Trusted Authorization operation:

- Bedrock;
- model ID;
- runtime provider;
- provider fallback;
- producer identifier;
- assistant runtime dispatch.

Provider/runtime code may only inherit an already-selected governed protected
operation from application architecture in a future separately authorized
integration.

## 13. AI Independence

AI, LLM, MCP, agent planning, prompt content, and model output must not select
or infer protected operation identity.

AI may assist user interaction only downstream of deterministic controls where
separately governed.

## 14. Authentication Separation

The protected operation catalog does not authenticate a subject.

Catalog membership does not create:

- `TrustedSubjectEvidence`;
- Principal Mapping;
- Membership;
- Entitlement;
- ALLOW.

## 15. Resource Separation

Protected operation identity does not establish:

- resource existence;
- resource ownership;
- Business Entity;
- ResourceClass;
- resource reference validity;
- permission.

Resource Identity remains responsible for resolving governed resources.

## 16. Membership And Entitlement Separation

Catalog membership does not create Membership or Entitlement.

`PROTECTED_ASSESSMENT_SUBMISSION` does not mean any principal may submit an
assessment. It only identifies what protected application capability is being
executed.

## 17. Evaluator Finality

The deterministic Trusted Authorization evaluator remains the sole final
ALLOW/DENY decision composer.

The catalog cannot produce ALLOW or DENY.

## 18. Catalog Entry Criteria

A future catalog entry requires all of the following:

1. An explicit product/application capability exists.
2. The capability has a stable semantic definition independent of transport.
3. The governed resource relationship is understood.
4. The relationship to `NonProductionApplicationOperation` is explicit.
5. The operation is independent of UI, browser, provider, function name, AI,
   role, RBAC, and resource-name pattern inference.
6. The entry is approved through governed architecture review.

No dynamic runtime registration is permitted.

## 19. Catalog Change And Retirement Criteria

Adding, removing, renaming, splitting, merging, or changing the semantics of a
protected application operation requires a governed architecture decision.

Retired or superseded operations must fail closed until a replacement is
explicitly governed.

## 20. Fail-Closed Principles

If an application capability is not explicitly accepted into this catalog, it
must not be treated as a recognized protected application operation.

There is no default operation.

Unknown, uncataloged, deferred, ambiguous, or externally supplied operations
must not map to:

- `VIEW_RESOURCE`;
- `DOWNLOAD_RESOURCE`;
- `SUBMIT_ASSESSMENT`;
- `EXPLAIN`;
- ALLOW.

## 21. Non-Production Implementation Boundary

A future bounded selector proof may use this catalog only for non-production
application-operation selection.

The future selector scope is limited to:

```text
PROTECTED_ASSESSMENT_SUBMISSION
        ->
NonProductionApplicationOperation.SUBMIT_ASSESSMENT
```

The future selector must not map deferred report view or report download
operations.

## 22. Explicit Non-Authority Statements

This catalog is not:

- permission;
- authentication;
- resource identity;
- Membership;
- Entitlement;
- applicability;
- final authorization;
- endpoint routing;
- handler integration;
- production operation policy.

## 23. Open Questions

The following remain open:

- production protected application operation catalog;
- real report-view capability;
- real report-download capability;
- assistant governed-resource operation model;
- authentication handoff;
- runtime activation;
- DENY enforcement;
- TOCTOU binding;
- audit transport and persistence;
- production authority-source realization.

## 24. Next Review Gate

The next gate is:

STRICT READ-ONLY BOUNDED APPLICATION-OPERATION SELECTION / TRUST HANDOFF
IMPLEMENTATION-AUTHORIZATION REVIEW.

That review must determine whether implementation may be authorized for the
non-production selector proof bounded by this artifact.
