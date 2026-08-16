# Resource × Action Applicability Governance v1

Version: v1

## 1. Purpose

This artifact governs the technology-neutral semantic relationship between
Nguyen AI Governed Resource classes and the canonical Requested Actions that
may meaningfully apply to those classes.

It closes the Resource x Action applicability gap left downstream by
Deterministic Authorization Decision Semantics v1.

This artifact does not grant access. It defines whether a canonical Action is
semantically applicable to a Resource class. Authorization still requires the
full governed authorization decision chain.

## 2. Status

Status: GOVERNED APPLICABILITY SEMANTICS ONLY

Resource x Action Applicability semantics are governed by this artifact.

The v1 applicability matrix is governed for the current minimal Resource
classes identified in this artifact.

Resource classification authority, applicability persistence, applicability
administration, Trusted Authorization Service Contract, authorization
persistence, and authorization implementation remain downstream.

## 3. Scope

This artifact governs:

- the Resource x Action Applicability definition;
- the applicability state model;
- the minimum current governed Resource taxonomy for applicability;
- the v1 Resource x Action Applicability matrix;
- fail-closed treatment of unknown, unresolved, stale, ambiguous, conflicting,
  or non-applicable Resource x Action pairs;
- action independence;
- producer, Website, browser, AI, Cognito, IAM, persistence, service contract,
  and implementation boundaries; and
- remaining governance dependencies.

This artifact does not govern or authorize:

- runtime authorization implementation;
- runtime applicability implementation;
- a policy engine;
- persistence;
- schemas;
- APIs;
- endpoints;
- Resource registry implementation;
- role models;
- RBAC, ABAC, or ACLs;
- Cognito group or custom-claim authority;
- IAM business-authorization authority;
- Website changes;
- Assessment Service changes;
- EIP changes;
- AWS AI Knowledge Assistant changes;
- Bedrock changes;
- AI behavior changes; or
- deployment.

## 4. Governing Context

This artifact depends on and preserves the approved Nguyen AI Platform
governance chain:

- Portal Governed Delivery Authorization Model v1;
- EIP Governed Retrieval Boundary v1;
- Runtime Owner Assignment Governance v1;
- Principal / Membership / Entitlement Authority Model v1;
- Stable Principal Mapping Authority Governance v1;
- Client / Organization Identity Authority Governance v1;
- Membership Authority Source Governance v1;
- Governed Resource Identity Lookup Governance v1;
- Requested Action Permission Vocabulary Governance v1;
- Entitlement Semantics Governance v1;
- Entitlement Authority Source Governance v1;
- Authority Administration / Revocation Governance v1; and
- Deterministic Authorization Decision Semantics v1.

Those artifacts establish authentication != authorization, Principal !=
Membership, Membership != Entitlement, Resource != Entitlement, Requested
Action != Entitlement, Entitlement != ALLOW, Administration != runtime
Authorization Decision, retrieval != authorization, browser != authority,
Cognito != Nguyen AI business authorization authority, IAM != Nguyen AI
business authorization authority, AI != authority, and producer truth !=
authorization state.

## 5. Definitions

Resource x Action Applicability:
The governed semantic determination of whether a canonical Requested Action is
meaningful and supported for a Governed Resource class.

Governed Resource class:
A technology-neutral business Resource category against which applicability may
be governed at class level while authorization evaluates a specific Resource
identity.

APPLICABLE:
The canonical Action is semantically valid for the Resource class and
authorization evaluation may continue.

NOT APPLICABLE:
The canonical Action is affirmatively not meaningful for the Resource class.

UNRESOLVED:
Current governance or evidence is insufficient to affirm APPLICABLE or NOT
APPLICABLE.

## 6. Canonical Requested Action Vocabulary

The approved canonical Principal-facing Requested Action vocabulary is:

- VIEW
- DOWNLOAD
- SUBMIT
- EXPLAIN

This artifact does not add EDIT, DELETE, CREATE, UPDATE, ADMIN, MANAGE, SHARE,
APPROVE, REVOKE, or any other Action.

Administrative lifecycle operations such as GRANT, REVOKE, DISABLE, RESTORE,
and CHANGE_VALIDITY remain administrative operations, not Principal-facing
Resource Actions.

## 7. Governed Resource Concept

A Governed Resource is a Nguyen AI object, artifact, delivery representation,
or governed capability whose future use, retrieval, presentation, explanation,
submission, or delivery may require deterministic authorization.

A Governed Resource is not automatically:

- a producer identifier;
- a lineage identifier;
- a transport payload;
- a storage record;
- a UI component;
- a route;
- a browser value;
- a session value;
- a token;
- a cached value; or
- an AI-generated reference.

## 8. Resource × Action Applicability Definition

Resource x Action Applicability answers:

Is this canonical Requested Action semantically valid for this Governed
Resource class?

It does not answer:

May this Principal perform this Action against this specific Resource?

That remains an Authorization Decision governed by Deterministic Authorization
Decision Semantics v1.

## 9. Applicability / Authorization Separation

Applicable does not mean authorized.

An APPLICABLE Resource x Action pair does not establish:

- valid authentication;
- stable Principal resolution;
- Governed Business Entity;
- Membership;
- scope;
- Resource identity;
- Entitlement;
- absence of revocation;
- authority availability; or
- ALLOW.

Applicability is only one predicate in the complete deterministic
authorization decision.

## 10. Applicability / Entitlement Separation

Resource x Action Applicability is not Entitlement.

An Action may be APPLICABLE to a Resource class while a Principal lacks an
applicable Entitlement for a specific Resource.

An Entitlement must not override a Resource x Action pair governed as NOT
APPLICABLE.

## 11. Applicability / Membership Separation

Resource x Action Applicability is not Membership.

Membership does not make an inapplicable Action applicable.

Applicability does not establish Membership.

Valid Membership without applicable Entitlement remains insufficient for ALLOW.

## 12. Applicability / Administration Separation

Resource x Action Applicability is not Administrative Authority.

Administrative Authority may govern future state changes, but it does not
create runtime applicability by assertion.

Future administration of applicability semantics or matrices requires separate
governance.

## 13. Applicability / Revocation Separation

Applicability is not revocation state.

A Resource x Action pair may remain APPLICABLE while a specific Principal's
Entitlement has been revoked.

Revocation is evaluated separately and must cause DENY where applicable.

## 14. Applicability State Model

The v1 applicability states are:

- APPLICABLE
- NOT APPLICABLE
- UNRESOLVED

These states are applicability classifications only. They are not runtime
authorization outcomes.

Final authorization outcomes remain exactly:

- ALLOW
- DENY

## 15. APPLICABLE Semantics

APPLICABLE means the canonical Action is semantically valid for the Resource
class.

When a Resource x Action pair is APPLICABLE, authorization evaluation may
continue.

APPLICABLE grants nothing by itself.

APPLICABLE must not be interpreted as ALLOW.

## 16. NOT APPLICABLE Semantics

NOT APPLICABLE means governance affirmatively establishes that the canonical
Action is not meaningful for the Resource class.

An authorization decision for a NOT APPLICABLE pair cannot produce ALLOW.

NOT APPLICABLE must remain distinct from missing Entitlement, missing
Membership, unknown Resource, unsupported implementation, or unavailable
authority.

## 17. UNRESOLVED Semantics

UNRESOLVED means current governance or evidence does not support either
APPLICABLE or NOT APPLICABLE.

Authorization must not infer applicability from an UNRESOLVED pair.

Under Deterministic Authorization Decision Semantics v1, unresolved
applicability means DENY.

## 18. Resource Classification Semantics

Resource classification is the deterministic assignment of a specific Governed
Resource identity to a governed Resource class for applicability evaluation.

This artifact governs the v1 classification semantics conceptually. It does
not select a Resource classification authority source, runtime, record format,
schema, API, storage mechanism, or administration mechanism.

If a specific Resource cannot be classified deterministically where required,
applicability is unresolved and authorization must fail closed.

## 19. Resource Class Granularity

Applicability is governed at Resource class level.

Authorization evaluates a specific Governed Resource identity.

The Resource class answers what Actions may semantically apply to that class.
The Resource identity answers which specific Resource is targeted.

This artifact does not create physical type fields, persistence structures, or
runtime lookup implementation.

## 20. Current Governed Resource Classes

The v1 applicability matrix governs the following minimal Resource classes:

- Executive Dashboard
- Report
- Assessment Submission

These classes are included because approved governance and repository evidence
support dashboard delivery, report presentation or durable report delivery,
and client/respondent assessment submission concepts.

The matrix does not classify all producer artifacts, lineage objects,
presentation components, or technical objects as Governed Resource classes.

## 21. Future / Unresolved Resource Classes

The following concepts remain future, excluded, or unresolved for v1 matrix
purposes:

- Assessment;
- Assessment Status;
- Assessment Result;
- BusinessDecisionPackage;
- ExecutiveAssessmentSnapshot;
- Finding;
- Recommendation;
- Executive Intelligence Package;
- Website Projection Delivery Contract;
- Evidence;
- Uploaded Evidence;
- AI Explanation Context;
- AI Conversation;
- Engagement; and
- Workspace.

These concepts may inform future Resource governance, but this artifact does
not force them into the v1 applicability matrix.

## 22. VIEW Applicability

VIEW is semantically applicable to Resource classes whose governed business
purpose includes presenting governed information to an authorized Principal.

In v1:

- Executive Dashboard x VIEW is APPLICABLE.
- Report x VIEW is APPLICABLE.
- Assessment Submission x VIEW is NOT APPLICABLE.

VIEW applicability does not imply DOWNLOAD, SUBMIT, EXPLAIN, Entitlement, or
ALLOW.

## 23. DOWNLOAD Applicability

DOWNLOAD is semantically applicable to Resource classes whose governed business
purpose includes delivering a durable or exportable artifact.

In v1:

- Executive Dashboard x DOWNLOAD is NOT APPLICABLE.
- Report x DOWNLOAD is APPLICABLE.
- Assessment Submission x DOWNLOAD is NOT APPLICABLE.

Technical retrievability or serialization does not establish DOWNLOAD
applicability.

## 24. SUBMIT Applicability

SUBMIT is semantically applicable to Resource classes whose governed business
purpose is receiving client- or respondent-supplied input into an approved
assessment or intake capability.

In v1:

- Executive Dashboard x SUBMIT is NOT APPLICABLE.
- Report x SUBMIT is NOT APPLICABLE.
- Assessment Submission x SUBMIT is APPLICABLE.

SUBMIT applicability does not mean submitted content is valid, accepted, scored,
or converted into producer truth.

## 25. EXPLAIN Applicability

EXPLAIN is semantically applicable to Resource classes whose governed business
purpose includes explanation of already-authorized governed output or context.

In v1:

- Executive Dashboard x EXPLAIN is APPLICABLE.
- Report x EXPLAIN is APPLICABLE.
- Assessment Submission x EXPLAIN is NOT APPLICABLE.

EXPLAIN does not imply VIEW or DOWNLOAD. EXPLAIN must not give AI authority to
recalculate, modify, or expand access to producer truth.

## 26. Action Independence

Each Resource x Action pair stands independently.

This artifact does not create inheritance such as:

- DOWNLOAD implies VIEW;
- VIEW implies EXPLAIN;
- EXPLAIN implies VIEW; or
- SUBMIT implies VIEW.

Any future Action relationship requires explicit governance.

## 27. Resource Identity Separation

Resource class is distinct from specific Resource identity.

Resource class determines applicability semantics.

Specific Resource identity remains a separate authorization predicate and must
be resolved authoritatively before ALLOW can be produced.

## 28. Producer Identity Separation

Producer identifiers such as request IDs, snapshot IDs, package IDs,
projection IDs, delivery contract IDs, and correlation references do not
automatically define Resource classes or applicability.

Producer identity or lineage may inform Resource governance only where approved
governance establishes the relationship.

## 29. Business Entity Isolation

Applicability must not weaken Business Entity isolation.

The same Resource class may exist across multiple Clients or Organizations.

Knowing that Report x VIEW is APPLICABLE does not authorize a Principal to view
every Report.

Business Entity, Membership, Resource identity, Entitlement, revocation, and
all other applicable predicates remain required.

## 30. Engagement Scope Boundary

Engagement scope remains PARTIALLY GOVERNED / DOWNSTREAM.

This artifact does not make Engagement universally required.

Where future governance establishes that a Resource class or specific Resource
requires Engagement scope, applicability and authorization must respect that
scope.

Where Engagement applicability is unknown and authorization-critical,
authorization must fail closed.

## 31. Workspace Boundary

Workspace remains OPTIONAL / FUTURE.

This artifact does not introduce Workspace-based applicability and does not
make Workspace mandatory.

If future Resource classes require Workspace scope, that requirement needs
separate governance.

## 32. Assessment Service Boundary

Assessment Service remains the sole producer of deterministic assessment
truth.

Applicability governance must not change:

- assessment methodology;
- scoring;
- readiness;
- severity;
- risk;
- confidence;
- recommendations;
- executive summaries;
- BusinessDecisionPackage semantics; or
- ExecutiveAssessmentSnapshot semantics.

This artifact governs only whether canonical Actions are semantically
applicable to governed Resource classes.

## 33. EIP Boundary

EIP remains producer of executive intelligence and Website Projection Delivery
Contracts.

Applicability governance must not modify:

- derivation;
- projection;
- publication;
- freshness;
- classification;
- compatibility;
- lineage; or
- producer truth.

EIP outputs may inform governed Resource classes, but applicability does not
alter EIP truth.

## 34. Website / Browser Boundary

Website remains presentation-only.

Website UI components do not define Resource x Action applicability.

A visible button is not applicability authority.

A hidden button is not non-applicability authority.

A route is not applicability authority.

Browser logic and browser-supplied Resource, Action, Entitlement, Membership,
role, or ALLOW values are non-authoritative request context.

## 35. AI Knowledge Assistant Boundary

AI Knowledge Assistant remains a consumer and explainer.

AI must not decide whether EXPLAIN is applicable.

AI must not infer applicability for an unknown Resource class.

AI must not expand or repair the applicability matrix.

AI must not convert VIEW permission into EXPLAIN permission.

Applicability must be deterministic and governed.

## 36. Technical Capability Non-Authority

Technical capability does not establish business applicability.

The following are not applicability authority:

- technically retrievable;
- serializable;
- HTTP POST available;
- LLM-readable;
- route exists;
- UI renders; or
- infrastructure can access the artifact.

## 37. Resource × Action Applicability Matrix

The v1 applicability matrix is:

| Governed Resource class | VIEW | DOWNLOAD | SUBMIT | EXPLAIN |
| --- | --- | --- | --- | --- |
| Executive Dashboard | APPLICABLE | NOT APPLICABLE | NOT APPLICABLE | APPLICABLE |
| Report | APPLICABLE | APPLICABLE | NOT APPLICABLE | APPLICABLE |
| Assessment Submission | NOT APPLICABLE | NOT APPLICABLE | APPLICABLE | NOT APPLICABLE |

Matrix values are applicability states only. They are not Entitlements and are
not authorization outcomes.

## 38. Matrix Evidence and Justification

Executive Dashboard:
Approved governance and Website/EIP evidence support executive dashboard
delivery and presentation of governed executive intelligence. VIEW is
APPLICABLE. EXPLAIN is APPLICABLE only for already-authorized governed
dashboard content. DOWNLOAD and SUBMIT are NOT APPLICABLE because current
governance does not define the dashboard itself as a durable export artifact or
an input submission target.

Report:
Approved action vocabulary and Website evidence support report presentation and
durable report delivery concepts. VIEW and DOWNLOAD are APPLICABLE. EXPLAIN is
APPLICABLE only for already-authorized report content. SUBMIT is NOT
APPLICABLE because a Report is an output Resource class, not an input target.

Assessment Submission:
Approved action vocabulary, Website evidence, and Assessment Service evidence
support client/respondent assessment input submission. SUBMIT is APPLICABLE.
VIEW, DOWNLOAD, and EXPLAIN are NOT APPLICABLE to the submission target itself
in v1. Any resulting assessment output remains separate producer truth and may
be governed by another Resource class later.

## 39. Unknown Resource Class

Unknown Resource class means applicability cannot be affirmatively established.

Unknown Resource class must not default to VIEW, DOWNLOAD, SUBMIT, or EXPLAIN.

Under deterministic authorization semantics, unknown Resource class means
DENY.

## 40. Unknown Requested Action

Unknown Requested Action is not a valid governed applicability pair.

Unknown Requested Action must not dynamically extend the canonical vocabulary.

Under deterministic authorization semantics, unknown Requested Action means
DENY.

## 41. Unresolved Applicability

UNRESOLVED Resource x Action applicability must not be treated as APPLICABLE.

UNRESOLVED applicability must not be treated as NOT APPLICABLE unless future
governance affirmatively establishes that classification.

Under deterministic authorization semantics, UNRESOLVED applicability means
DENY.

## 42. Conflict Semantics

If applicability evidence conflicts and no governed deterministic precedence
exists, applicability is UNRESOLVED.

Authorization for an unresolved conflicting pair must fail closed.

This artifact does not create precedence rules such as latest wins, UI wins,
producer wins, runtime wins, administrator wins, or AI decides.

## 43. Stale Applicability

Known stale applicability evidence must not establish current applicability
where the current governed version is required.

This artifact does not select caching, freshness propagation, or runtime
version retrieval implementation.

## 44. Fail-Closed Semantics

The fail-closed applicability semantics are:

| Condition | Applicability result | Authorization consequence |
| --- | --- | --- |
| Known Resource class + known canonical Action + APPLICABLE | APPLICABLE | Continue authorization evaluation |
| Unknown Resource class | UNRESOLVED | DENY |
| Unknown Action | UNRESOLVED | DENY |
| Unsupported Action | UNRESOLVED | DENY |
| UNRESOLVED applicability | UNRESOLVED | DENY |
| NOT APPLICABLE pair | NOT APPLICABLE | DENY |
| Applicability authority unavailable where required | UNRESOLVED | DENY |
| Ambiguous Resource classification | UNRESOLVED | DENY |
| Conflicting applicability state | UNRESOLVED | DENY |
| AI-generated applicability assertion | UNRESOLVED | DENY |
| Browser-only applicability assertion | UNRESOLVED | DENY |
| Cognito-only applicability assertion | UNRESOLVED | DENY |
| IAM-only business applicability assertion | UNRESOLVED | DENY |

APPLICABLE never means automatic ALLOW.

## 45. Denial Privacy

A non-applicable or unresolved Resource x Action pair must not require
revealing:

- whether a Resource exists;
- another Client;
- another Organization;
- another Principal;
- another Membership;
- another Entitlement; or
- protected Resource content.

Denial disclosure must remain minimum necessary.

## 46. Resource Existence Privacy

Applicability evaluation must not require disclosure of Resource existence to
unauthorized requesters.

Unknown, unauthorized, non-applicable, or unresolved Resource requests may be
handled without revealing whether the Resource exists.

This artifact does not define HTTP status codes or UI messages.

## 47. Audit Semantics

Future applicability and authorization evidence should support, where
appropriate:

- Resource class reference;
- canonical Requested Action;
- applicability classification;
- applicability governance version or reference;
- decision correlation reference; and
- reason category sufficient for deterministic review.

Audit evidence must not require unnecessary PII and must not log protected
Resource content merely to establish applicability.

This artifact does not select logging technology.

## 48. Side-Effect Safety

Applicability evaluation must not mutate:

- Principal;
- Membership;
- Entitlement;
- Resource;
- Administrative Authority;
- Assessment truth; or
- EIP truth.

APPLICABLE must not create a grant.

NOT APPLICABLE must not revoke an Entitlement record.

## 49. Resource Classification Ambiguity

If a specific Resource cannot be deterministically classified into exactly one
applicable governed Resource class where required, applicability is unresolved.

Authorization must DENY when classification ambiguity affects applicability.

AI classification must not be authoritative.

## 50. Multiple Resource Class Boundary

This artifact does not govern multiple Resource class participation or
inheritance.

If a future Resource may legitimately participate in more than one Resource
class, separate governance must define deterministic classification and
applicability semantics.

Until then, ambiguity affecting applicability fails closed.

## 51. Composite Resource Boundary

Composite concepts such as Executive Dashboard, Report, Assessment Result, and
Website Projection Delivery Contract may represent projections or compositions
of other producer artifacts.

For v1, Executive Dashboard and Report are governed at the business Resource
class level because they are client-facing delivery or presentation concepts.

This artifact does not expose underlying producer components as separate
Resource classes unless the v1 matrix includes them.

## 52. AI Context Resource Assessment

AI context, conversation history, and prompt context are not current v1
Governed Resource classes.

Protected source Resources supplied to AI remain governed by their own Resource
class and Action authorization.

If AI-specific context requires direct Resource governance later, it is
downstream.

## 53. Evidence Resource Assessment

Evidence and uploaded evidence are not governed sufficiently as independent v1
Resource classes.

Assessment Submission covers the current input-submission target at the
applicability level only.

This artifact does not define upload storage, evidence retrieval, evidence
download, or evidence lifecycle semantics.

## 54. Report Resource Assessment

Report is included as a v1 Governed Resource class.

The evidence basis is approved action vocabulary and Website presentation
evidence for report-like outputs and durable report delivery concepts.

Report x VIEW, Report x DOWNLOAD, and Report x EXPLAIN are APPLICABLE.

Report x SUBMIT is NOT APPLICABLE.

## 55. Executive Dashboard Resource Assessment

Executive Dashboard is included as a v1 Governed Resource class.

The evidence basis is EIP production of dashboard delivery content and Website
presentation of that governed delivery output.

Executive Dashboard x VIEW and Executive Dashboard x EXPLAIN are APPLICABLE.

Executive Dashboard x DOWNLOAD and Executive Dashboard x SUBMIT are NOT
APPLICABLE.

Website presentation does not become applicability authority.

## 56. Assessment Resource Assessment

Assessment, Assessment Status, and Assessment Result remain unresolved as
independent v1 Resource classes.

Current evidence separates assessment input submission, deterministic
assessment truth production, and client-facing presentation or report outputs.

This artifact does not conflate input workflow, producer request, producer
result, portal presentation, and report delivery into one Resource class.

## 57. Finding / Recommendation Resource Assessment

Finding and Recommendation are not independent v1 Governed Resource classes.

They are treated as content within broader governed output Resources such as
Report or Executive Dashboard unless future governance establishes
fine-grained Resource classification.

This artifact does not create fine-grained authorization over individual
findings or recommendations.

## 58. WPDC / EIP Resource Assessment

Website Projection Delivery Contract and Executive Intelligence Package remain
producer or delivery artifacts for v1 applicability purposes.

They are not directly exposed as v1 client-facing Resource classes in the
matrix.

Their producer lineage and delivery semantics may inform Resource governance,
but technical delivery contract identity does not automatically become
authorization Resource classification.

## 59. Minimum Necessary Resource Taxonomy

The v1 taxonomy is intentionally minimal.

It includes only:

- Executive Dashboard;
- Report; and
- Assessment Submission.

This avoids unnecessary fine-grained Resource classes and preserves stable
authorization semantics without over-classifying producer internals or UI
components.

## 60. Current vs Future Resource Classes

Current v1 matrix Resource classes are:

- Executive Dashboard;
- Report; and
- Assessment Submission.

Future or unresolved candidate classes include:

- Assessment Result;
- Assessment Status;
- Evidence;
- AI Explanation Context;
- Website Projection Delivery Contract;
- Executive Intelligence Package;
- Finding;
- Recommendation;
- Engagement-scoped Resource classes; and
- Workspace-scoped Resource classes.

Future candidates must not enter authoritative authorization behavior until
separately governed.

## 61. Applicability Authority Source

This versioned Platform governance artifact is the semantic authority for the
v1 Resource x Action Applicability matrix.

Runtime representation, retrieval, enforcement, and administration of
applicability state remain downstream.

This artifact does not select storage, runtime ownership, API shape, endpoint,
policy engine, or administration process.

## 62. Version Governance

Applicability semantics are version-governed.

A future change such as Report x DOWNLOAD changing from APPLICABLE to NOT
APPLICABLE, or NOT APPLICABLE to APPLICABLE, is an authorization-significant
governance change.

Such changes require explicit governed review and a new version or successor
artifact.

This artifact does not define version columns, headers, schemas, records, or
API fields.

## 63. Technology Neutrality

This artifact is technology-neutral.

Technology references appear only as existing evidence, boundaries, explicit
exclusions, or non-selections.

This artifact does not select DynamoDB, S3, SQL, PostgreSQL, MySQL, Redis,
filesystem, cache, queue, API Gateway, Lambda, Cognito groups, custom claims,
IAM roles, RBAC, ABAC, ACL, OPA, Cedar, policy engine, workflow engine,
Bedrock, LLM, RAG, vector database, schema, API, endpoint, or framework for
applicability, authorization, persistence, or enforcement.

## 64. Policy-Model Non-Selection

This artifact does not define a role model, RBAC, ABAC, ACLs, OPA, Cedar, IAM
policy, or any other policy engine.

Applicability is Resource class x canonical Action semantics.

It is not a user role, administrative role, entitlement grant, policy rule, or
infrastructure permission.

## 65. Persistence Boundary

Applicability persistence remains UNRESOLVED / DOWNSTREAM.

This artifact does not select how Resource classes, applicability states,
matrix versions, Resource classifications, audit evidence, or authorization
state are stored.

No database, table, record, document, cache, configuration file, or filesystem
authority is selected.

## 66. Service Contract Boundary

Trusted Authorization Service Contract remains DOWNSTREAM.

This artifact does not define:

- endpoint;
- route;
- HTTP method;
- request payload;
- response payload;
- status code;
- SDK;
- client library;
- Lambda handler; or
- API Gateway integration.

## 67. Implementation Gate

This artifact does not authorize:

- runtime applicability implementation;
- authorization implementation;
- Resource registry implementation;
- policy engine implementation;
- database implementation;
- persistence implementation;
- schema creation;
- API creation;
- endpoint creation;
- Lambda changes;
- API Gateway changes;
- Cognito changes;
- IAM changes;
- Website changes;
- Assessment Service changes;
- EIP changes;
- AWS AI Knowledge Assistant changes;
- Bedrock changes;
- AI changes; or
- deployment.

Implementation remains UNAUTHORIZED.

## 68. Authority Status Model

| Area | Status |
| --- | --- |
| Canonical Requested Action vocabulary | GOVERNED |
| Governed Resource identity semantics | GOVERNED CONCEPTUALLY |
| Governed Resource taxonomy | PARTIALLY GOVERNED BY THIS ARTIFACT |
| Resource classification semantics | GOVERNED CONCEPTUALLY FOR V1 MATRIX |
| Resource x Action Applicability semantics | GOVERNED BY THIS ARTIFACT |
| Resource x Action Applicability matrix | GOVERNED FOR CURRENT V1 RESOURCE CLASSES |
| Resource x Action Applicability authority source | VERSIONED PLATFORM ARTIFACT GOVERNS SEMANTICS; RUNTIME SOURCE DOWNSTREAM |
| Resource x Action Applicability persistence | UNRESOLVED / DOWNSTREAM |
| Resource x Action Applicability administration | DOWNSTREAM |
| Engagement scope | PARTIALLY GOVERNED / DOWNSTREAM |
| Workspace scope | OPTIONAL / FUTURE |
| Entitlement semantics | GOVERNED |
| Entitlement authority source | GOVERNED CLASS; CONCRETE SOURCE UNRESOLVED / DOWNSTREAM |
| Revocation semantics | GOVERNED |
| Deterministic Authorization Decision semantics | GOVERNED |
| Authorization decision authority runtime | DOWNSTREAM / UNAUTHORIZED |
| Trusted Authorization Service Contract | DOWNSTREAM |
| Authorization persistence | UNRESOLVED / DOWNSTREAM |
| Authorization implementation | UNAUTHORIZED |

## 69. Remaining Governance Dependencies

Remaining dependencies ranked for safe future authorization implementation:

1. Resource Classification Authority Governance v1.
2. Engagement Scope Governance v1.
3. Authorization Persistence Authority Review.
4. Trusted Authorization Service Contract v1.
5. Authorization Audit / Observability Governance v1.
6. Administrative Bootstrap / Root Authority Governance v1.
7. Administrative Separation-of-Duties Governance v1.
8. Security / IAM Boundary Review.
9. Applicability Administration Governance.

Resource Classification Authority Governance v1 is the highest-value bounded
next increment because the applicability matrix can only be used safely when a
specific Resource can be deterministically classified into a governed Resource
class.

## 70. Acceptance Criteria

This artifact is acceptable when:

- exactly one artifact is created;
- the canonical Requested Action vocabulary remains VIEW, DOWNLOAD, SUBMIT,
  and EXPLAIN;
- applicability states are APPLICABLE, NOT APPLICABLE, and UNRESOLVED;
- final authorization outcomes remain ALLOW and DENY only;
- the v1 matrix uses applicability states only;
- APPLICABLE does not mean ALLOW;
- NOT APPLICABLE is distinct from missing Entitlement;
- UNRESOLVED fails closed;
- action independence is preserved;
- Business Entity isolation is preserved;
- producer truth boundaries are preserved;
- Website, browser, Cognito, IAM, and AI remain non-authoritative;
- persistence, service contract, policy model, and implementation remain
  downstream or unauthorized; and
- no unrelated repository is modified.

## 71. Architecture Decision

Resource x Action Applicability Governance v1 is APPROVED AS GOVERNANCE when
reviewed and accepted.

The v1 governed Resource x Action Applicability matrix is:

| Governed Resource class | VIEW | DOWNLOAD | SUBMIT | EXPLAIN |
| --- | --- | --- | --- | --- |
| Executive Dashboard | APPLICABLE | NOT APPLICABLE | NOT APPLICABLE | APPLICABLE |
| Report | APPLICABLE | APPLICABLE | NOT APPLICABLE | APPLICABLE |
| Assessment Submission | NOT APPLICABLE | NOT APPLICABLE | APPLICABLE | NOT APPLICABLE |

This decision does not authorize runtime implementation, authorization
implementation, persistence, APIs, schemas, endpoints, policy engines,
repository changes, deployment, or the next governance increment.
