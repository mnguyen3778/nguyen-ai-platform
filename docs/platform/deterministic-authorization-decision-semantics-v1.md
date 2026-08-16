# Deterministic Authorization Decision Semantics v1

Version: v1

## 1. Purpose

This artifact governs the technology-neutral semantics for deterministic Nguyen
AI runtime authorization decisions.

It defines how governed authorization inputs conceptually combine to produce
the final runtime authorization outcome:

- ALLOW
- DENY

This artifact closes the semantic gap between the previously governed
authorization predicates and the future trusted deterministic authorization
boundary.

## 2. Status

Status: GOVERNED DECISION SEMANTICS ONLY

Deterministic Authorization Decision semantics are governed by this artifact.

Authorization implementation remains UNAUTHORIZED.

Trusted Authorization Service Contract remains DOWNSTREAM.

Authorization persistence remains UNRESOLVED / DOWNSTREAM.

Resource x Action applicability remains PARTIALLY GOVERNED / DOWNSTREAM.

Engagement scope remains PARTIALLY GOVERNED / DOWNSTREAM.

Workspace scope remains OPTIONAL / FUTURE.

## 3. Scope

This artifact governs:

- final authorization decision outcome semantics;
- default-DENY behavior;
- predicate satisfaction required for ALLOW;
- fail-closed treatment of missing, unknown, ambiguous, conflicting, stale, or
  unavailable authorization-critical state;
- conceptual decision reproducibility and audit semantics;
- privacy-preserving denial semantics;
- side-effect safety of authorization evaluation;
- producer, consumer, browser, Cognito, IAM, AI, persistence, service contract,
  and implementation boundaries.

This artifact does not govern or authorize:

- runtime implementation;
- policy engine selection;
- persistence;
- schemas;
- APIs;
- endpoints;
- service contracts;
- RBAC, ABAC, or ACL models;
- Cognito group or custom-claim authority;
- IAM business-authorization authority;
- Website changes;
- Assessment Service changes;
- EIP changes;
- AWS runtime changes;
- AI or Bedrock changes.

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
- Authority Administration / Revocation Governance v1.

The chain establishes authentication != authorization, Membership !=
Entitlement, Resource != Entitlement, Requested Action != Entitlement,
Entitlement != ALLOW, Administration != runtime authorization decision,
retrieval != authorization, browser != authority, Cognito != business
authorization authority, IAM != Nguyen AI business authorization, and AI !=
authority.

## 5. Definitions

Authorization Decision:
The authoritative deterministic server-side evaluation that determines whether
a resolved Principal may perform a canonical Requested Action against a
Governed Resource under applicable authoritative authorization state.

ALLOW:
The affirmative runtime outcome produced only when every applicable governed
authorization predicate is valid and no blocking state exists.

DENY:
The safe default runtime outcome produced whenever ALLOW cannot be
affirmatively established from valid authoritative governed inputs.

Predicate:
A governed authorization condition that must be satisfied, or explicitly
governed as not applicable, before ALLOW may be produced.

Authorization-critical state:
Any state required to evaluate an applicable authorization predicate.

## 6. Authorization Decision Definition

An Authorization Decision is the final deterministic evaluation of governed
authorization inputs for a specific protected request.

It evaluates:

- trusted authentication evidence;
- stable Nguyen AI Principal resolution;
- Governed Business Entity resolution where required;
- valid Membership where required;
- applicable governed scope;
- Governed Resource identity;
- canonical Requested Action;
- Resource x Action applicability;
- authoritative applicable Entitlement state;
- revocation, disablement, temporal validity, freshness, authority
  availability, ambiguity, and conflict state.

The decision is not authentication, Principal mapping, Membership, Resource
lookup, Requested Action recognition, Entitlement existence, Administration,
retrieval, producer truth, browser state, Cognito state, IAM permission, or AI
reasoning.

## 7. Authorization Decision Outcomes

The only final authorization outcomes governed in v1 are:

- ALLOW
- DENY

This artifact does not permit runtime outcomes such as:

- MAYBE;
- UNKNOWN;
- REVIEW;
- PENDING;
- LIKELY;
- confidence score;
- AI recommendation.

Operational, audit, or diagnostic reason categories may exist conceptually, but
they do not create additional authorization outcomes.

## 8. Governing Authorization Chain

The governed conceptual chain is:

verified authentication evidence
-> stable Principal resolution
-> Governed Business Entity
-> valid Membership
-> applicable governed scope
-> Governed Resource
-> canonical Requested Action
-> applicable authoritative Entitlement
-> deterministic authorization evaluation
-> ALLOW / DENY

No governed prerequisite may be bypassed.

Where a predicate is not applicable to a future Resource, Action, or
authorization class, that non-applicability must be explicitly governed.
Non-applicability must not be inferred from missing, unavailable, difficult to
retrieve, or unimplemented state.

## 9. Default-DENY Principle

DENY is the safe default.

If ALLOW cannot be affirmatively established from valid authoritative governed
inputs, the decision must be DENY.

Absence of evidence sufficient for ALLOW means DENY.

Uncertainty means DENY.

Authority unavailable means DENY.

Unresolved conflict means DENY.

No fallback authority is created by this artifact.

## 10. ALLOW Semantics

ALLOW requires affirmative satisfaction of all applicable governed
authorization predicates.

ALLOW must not result merely because:

- authentication succeeded;
- a Principal exists;
- Membership exists;
- a Resource exists;
- an Action is valid;
- an Entitlement exists somewhere;
- a previous request succeeded;
- browser state says access is allowed;
- Cognito contains a group or claim;
- IAM permits infrastructure invocation;
- AI predicts access should be allowed.

Partial satisfaction does not produce ALLOW.

## 11. Authentication Predicate

Authentication evidence used by authorization must be:

- valid;
- supported;
- trusted according to approved authentication boundaries;
- sufficient to resolve the stable Nguyen AI Principal.

Invalid, missing, expired, malformed, unsupported, or otherwise unusable
authentication evidence means DENY.

Authentication success alone does not mean ALLOW.

## 12. Principal Predicate

Authorization requires exactly one valid applicable stable Nguyen AI Principal.

Principal resolution that is missing, unmapped, ambiguous, conflicting,
disabled, revoked, stale where governed, or unavailable means DENY.

The decision must not fall back to:

- email;
- username;
- browser-supplied Principal ID;
- AI inference.

## 13. Governed Business Entity Predicate

Where a Governed Business Entity is required, authorization must resolve the
applicable Client or Organization identity authoritatively.

Missing, ambiguous, conflicting, unavailable, or mismatched business identity
means DENY.

Authorization must not permit cross-business-entity substitution.

## 14. Membership Predicate

Where Membership is required, a valid authoritative applicable Membership must
exist between the resolved Principal and the applicable Governed Business
Entity or governed scope.

The Membership must be:

- valid;
- applicable;
- authoritative;
- not revoked;
- not disabled;
- not expired where temporal validity applies.

Failure of a required Membership predicate means DENY.

Membership alone does not mean ALLOW.

## 15. Engagement / Workspace Scope Boundary

Engagement scope remains PARTIALLY GOVERNED / DOWNSTREAM.

This artifact does not make Engagement scope universally mandatory. Where
existing or future governance requires Engagement scope for a Resource, Action,
Membership, or Entitlement, the applicable Engagement scope must be resolved
and matched authoritatively. Failure means DENY.

Workspace scope remains OPTIONAL / FUTURE.

This artifact does not introduce Workspace as a mandatory authorization
dimension. If future governance introduces Workspace scope, authorization
decisions must evaluate it deterministically and fail closed when required
Workspace scope cannot be established.

Authorization must not guess Engagement or Workspace applicability.

## 16. Governed Resource Predicate

Authorization requires authoritative resolution of the target Governed
Resource.

Resource identity remains distinct from:

- browser-supplied Resource identity;
- producer identity;
- Assessment requestId;
- snapshot ID;
- package ID;
- projection ID;
- Website Projection Delivery Contract metadata;
- Resource possession;
- Resource lookup;
- Resource retrieval.

Unknown Resource means DENY.

Ambiguous Resource means DENY.

Resource Business Entity mismatch means DENY.

Unauthorized Resource lookup must not create authorization.

## 17. Requested Action Predicate

Authorization requires a canonical governed Requested Action.

The current governed Principal-facing Requested Action vocabulary is:

- VIEW
- DOWNLOAD
- SUBMIT
- EXPLAIN

Unknown action means DENY.

Unsupported action means DENY.

Ambiguous action means DENY.

Browser-selected action labels are request context only and are not authority.

## 18. Resource x Action Applicability

A canonical Action does not automatically apply to every Governed Resource
class.

For example, DOWNLOAD being canonical does not mean DOWNLOAD applies to every
Governed Resource.

Where Resource x Action applicability is not established by approved
governance for the protected request, authorization must fail closed to DENY.

This artifact does not create a complete Resource x Action applicability
matrix. Resource x Action Applicability Governance v1 remains downstream.

## 19. Entitlement Predicate

Authorization requires authoritative applicable Entitlement state sufficient
for the requested Principal, Governed Business Entity, Resource, Action, and
scope.

An Entitlement must not authorize merely because it exists. It must be:

- authoritative;
- applicable;
- within scope;
- valid;
- not revoked;
- not disabled;
- not expired where temporal validity applies;
- consistent with the resolved Principal;
- consistent with the Governed Business Entity;
- consistent with the Governed Resource;
- consistent with the Requested Action.

Failure of the applicable Entitlement predicate means DENY.

## 20. Revocation Predicate

Known authoritative revocation means DENY.

Revocation must not be overridden by:

- previous ALLOW;
- previous grant evidence;
- browser state;
- stale cache;
- conversation history;
- AI memory;
- technical Resource availability;
- non-authoritative state.

Revocation precedence governed by Authority Administration / Revocation
Governance v1 is preserved.

## 21. Temporal Validity

Where governed authorization state contains temporal validity:

- not-yet-valid state means DENY;
- expired state means DENY;
- valid state during the applicable governed interval may continue evaluation.

This artifact does not require all authorization state to contain expiration.

This artifact does not select TTL, scheduler, cron, database expiry, or clock
implementation mechanics.

## 22. Authority Availability

If required authoritative state cannot be obtained or resolved, the decision
must be DENY.

Authorization must not fall back to:

- browser state;
- cached non-authoritative state;
- Cognito group;
- custom claim;
- IAM;
- previous ALLOW;
- Membership alone;
- AI;
- conversation history.

## 23. Ambiguity Semantics

Any unresolved ambiguity in an authorization-critical predicate means DENY.

Examples include:

- multiple Principals;
- multiple conflicting Governed Business Entity identities;
- ambiguous Membership;
- ambiguous Resource;
- ambiguous Requested Action;
- conflicting Entitlement applicability;
- unclear scope applicability.

Ambiguity must not be resolved probabilistically.

## 24. Conflict Semantics

If authoritative authorization inputs conflict and no separately governed
deterministic rule resolves the conflict, the decision must be DENY.

This artifact does not invent:

- latest wins;
- first wins;
- grant wins;
- highest role wins;
- most permissive wins;
- IAM wins;
- Cognito wins;
- AI decides.

Already-governed revocation precedence is preserved.

## 25. Stale-State Semantics

Known stale authorization-critical state must not be used to establish ALLOW
where freshness is required by governance.

Known stale authoritative evidence means DENY unless approved governance
explicitly defines a valid stale-use rule.

This artifact does not create a stale-use rule.

## 26. Unknown-State Semantics

Unknown authorization-critical state means DENY.

Unknown must not become:

- not applicable;
- assumed valid;
- previous value;
- default Membership;
- default Client;
- default Resource;
- default Entitlement.

## 27. Missing-State Semantics

Missing required authorization state means DENY.

Authorization must not synthesize missing state from:

- browser context;
- prior access;
- email or username;
- Cognito claims;
- IAM permissions;
- producer metadata alone;
- Resource possession;
- AI output.

## 28. Not-Applicable Semantics

NOT APPLICABLE is a governed predicate property only where approved governance
explicitly establishes that the predicate does not apply to that Resource,
Action, or authorization class.

Missing does not mean not applicable.

Unknown does not mean not applicable.

Unavailable does not mean not applicable.

Unimplemented does not mean not applicable.

## 29. Deterministic Decision Function

The conceptual deterministic decision function is:

ALLOW if and only if every applicable required governed predicate is
affirmatively valid and no blocking state exists.

Otherwise, DENY.

For clarity, any required predicate that is invalid, unknown, missing,
unavailable, ambiguous, conflicting, known stale where freshness is required,
revoked, disabled, expired, not-yet-valid, out of scope, or applicability
unresolved results in DENY.

This is logical governance, not executable code.

No programming language, authorization library, or policy engine is selected.

## 30. Evaluation Order

This artifact governs logical decision semantics, not runtime optimization or
physical evaluation order.

Future runtime evaluation order may be governed separately to preserve:

- fail-closed behavior;
- privacy;
- minimum necessary disclosure;
- side-effect safety;
- auditability.

No implementation order is prescribed here.

## 31. Short-Circuit DENY

An already-established decisive DENY condition may conceptually terminate
further authorization evaluation.

Short-circuit DENY is permitted only as a privacy-preserving and
side-effect-safe semantic. Once authorization cannot succeed, unnecessary
additional identity, Resource, Membership, Entitlement, or producer information
should not be retrieved merely to complete every predicate.

This artifact does not define runtime implementation.

## 32. Denial Information Disclosure

Authorization denial must not unnecessarily reveal:

- whether a Resource exists;
- another Client or Organization identity;
- another Principal;
- another Membership;
- another Entitlement;
- sensitive authorization structure;
- underlying Resource content.

This artifact does not define HTTP status codes, browser messages, or UI copy.

## 33. Resource Existence Privacy

A request for an unknown or unauthorized Resource must not require the system
to reveal whether that Resource exists.

Resource-existence privacy preserves cross-tenant isolation and minimum
necessary disclosure.

## 34. Business Entity Isolation

A Principal authorized within one Governed Business Entity must not gain access
to another merely because:

- Resource ID is known;
- browser supplies another Client ID;
- browser supplies another Organization ID;
- the same email domain appears;
- the same username appears;
- the same Cognito session exists;
- the same Action is requested;
- Resource metadata appears similar;
- previous access existed elsewhere.

Business Entity mismatch means DENY.

## 35. Membership / Entitlement Separation

Membership is not Entitlement.

Valid Membership without applicable Entitlement means DENY.

Applicable Entitlement without required valid Membership means DENY unless
future governance explicitly establishes a Resource or Action class for which
Membership is not applicable.

This artifact does not invent that exception.

## 36. Resource / Entitlement Separation

Resource existence or association is not Entitlement.

Being associated with, referenced by, or able to locate a Resource does not
itself authorize any Action.

## 37. Action / Entitlement Separation

A valid Requested Action is not Entitlement.

Knowing or requesting VIEW, DOWNLOAD, SUBMIT, or EXPLAIN does not grant
permission.

## 38. Entitlement / ALLOW Separation

Entitlement is not ALLOW.

Entitlement is authoritative authorization state. ALLOW is the result of
evaluating all applicable governed predicates, including Entitlement, scope,
Resource, Action, Membership, Principal, Business Entity, authority
availability, freshness, ambiguity, conflict, and blocking lifecycle state.

## 39. Administration / Decision Separation

Administrative Authority is not the runtime Authorization Decision.

Administrative Authority may cause governed authorization state transitions.
Runtime authorization evaluates authoritative state.

An administrator does not automatically receive Resource access.

## 40. Retrieval / Authorization Separation

Retrieval is not authorization.

Technical ability to retrieve a Website Projection Delivery Contract,
Executive Intelligence Package output, Assessment output, report, dashboard
data, or AI context does not establish permission.

Authorization must precede protected delivery or use where required by
governance.

## 41. Authorization / Producer Truth Separation

Authorization decides whether an Action may occur.

Authorization must not alter the authoritative content of:

- Assessment Service outputs;
- BusinessDecisionPackage;
- ExecutiveAssessmentSnapshot;
- Executive Intelligence Package;
- Website Projection Delivery Contract.

## 42. Website / Browser Boundary

The Website remains presentation-only.

Browser-supplied Principal, Client, Organization, Engagement, Workspace,
Resource, Action, Membership, Entitlement, role, admin flag, or ALLOW are
non-authoritative request context.

Server-side authoritative resolution remains required.

## 43. Cognito Boundary

Cognito authentication is not the authorization decision.

The following do not equal ALLOW:

- Cognito user;
- Cognito group;
- custom claim;
- email;
- username;
- token possession.

Cognito is not selected as the Nguyen AI business authorization decision
authority.

## 44. IAM Boundary

AWS IAM infrastructure permission is not Nguyen AI business authorization.

A Lambda or IAM principal being technically capable of retrieving data does not
establish business ALLOW.

IAM is not selected as the Nguyen AI business authorization decision authority.

## 45. AI Non-Authority

AI, Bedrock, LLM, RAG, embeddings, semantic similarity, agents, model
confidence, conversation history, or model output must not:

- produce ALLOW;
- override DENY;
- infer missing authorization state;
- infer Membership;
- infer Entitlement;
- infer Resource ownership;
- infer Business Entity association;
- resolve ambiguity authoritatively;
- resolve conflicts authoritatively;
- repair stale authorization state;
- create authorization exceptions.

Authorization decision semantics must remain deterministic and non-AI.

## 46. AI Knowledge Assistant Boundary

AI Knowledge Assistant remains a consumer and explainer.

Before protected client context is supplied to AI, the applicable deterministic
authorization decision must permit the relevant governed Action.

AI may explain an already-authorized result using authorized governed
information. AI may not authorize itself to receive context.

## 47. EXPLAIN Authorization

EXPLAIN is a governed Requested Action.

EXPLAIN requires its own applicable authorization basis.

Permission to VIEW must not automatically imply EXPLAIN unless future approved
governance explicitly establishes that relationship.

Permission to EXPLAIN must not automatically imply DOWNLOAD.

No action inheritance is created here.

## 48. Action Independence

Unless approved governance explicitly establishes otherwise, VIEW, DOWNLOAD,
SUBMIT, and EXPLAIN are distinct Actions.

Authorization for one Action must not automatically authorize another.

Future Action relationships, if required, belong in Resource x Action
Applicability Governance v1 or later action-governance increments.

## 49. Prior ALLOW Boundary

Previous ALLOW is not current ALLOW.

Every protected authorization decision must use currently applicable
authoritative state according to governed freshness requirements.

Historical success does not create permanent authorization.

## 50. Session Boundary

An authenticated session is not permanent authorization.

Session continuity must not override:

- revocation;
- Membership invalidation;
- Entitlement invalidation;
- scope changes;
- Resource changes;
- Business Entity mismatch.

## 51. Cache Boundary

This artifact does not select caching.

If caching is introduced later, cached state must not become an independent
authority source.

Stale cache must not override current authoritative revocation or DENY state.

Caching implementation remains downstream.

## 52. Audit Semantics

Future authorization decision evidence should support, where appropriate:

- decision identifier or correlation reference;
- Principal reference;
- Governed Business Entity reference;
- applicable scope reference;
- Governed Resource reference;
- canonical Requested Action;
- authorization outcome;
- reason category;
- authority and version references;
- timestamp;
- relevant freshness or version evidence.

Audit semantics must not require unnecessary PII.

Audit evidence must not log:

- raw tokens;
- passwords;
- credentials;
- secrets;
- unnecessary Resource content.

This artifact does not select logging technology.

## 53. Decision Reason Semantics

Internal deterministic reason categories are governed conceptually for audit,
traceability, operations, and reproducibility.

Permitted conceptual reason categories include:

- AUTHENTICATION_INVALID;
- PRINCIPAL_UNRESOLVED;
- BUSINESS_ENTITY_INVALID;
- BUSINESS_ENTITY_MISMATCH;
- MEMBERSHIP_INVALID;
- SCOPE_INVALID;
- RESOURCE_UNRESOLVED;
- RESOURCE_MISMATCH;
- ACTION_UNSUPPORTED;
- ACTION_NOT_APPLICABLE;
- ENTITLEMENT_MISSING;
- ENTITLEMENT_NOT_APPLICABLE;
- ENTITLEMENT_REVOKED;
- AUTHORITY_UNAVAILABLE;
- AUTHORIZATION_CONFLICT;
- STATE_STALE;
- UNKNOWN_STATE.

These categories are internal and audit-oriented. They are not API error codes,
HTTP status codes, browser messages, or permission grants.

Detailed reasons need not be exposed to the browser.

## 54. Decision Reproducibility

Equivalent authoritative inputs under the same governed semantic and version
context must yield the same authorization outcome.

Authorization decisions must be:

- deterministic;
- reproducible;
- auditable.

No confidence score, model variance, probabilistic inference, or AI reasoning
may affect the outcome.

## 55. Version Governance

Authorization decision semantics require a governed version reference for
audit and reproducibility.

Future decision evidence should be capable of identifying the governing
decision-semantics version used.

This artifact does not create a schema, header, API field, database column, or
record format.

## 56. Authorization Failure Matrix

| Condition | Governed outcome |
| --- | --- |
| valid authentication + valid Principal + valid applicable Membership + valid Resource + supported applicable Action + valid applicable Entitlement + no blocking state | ALLOW |
| authentication missing or invalid | DENY |
| Principal unresolved | DENY |
| Principal ambiguous | DENY |
| Principal disabled or revoked | DENY |
| Business Entity unresolved where required | DENY |
| Business Entity mismatch | DENY |
| Membership missing where required | DENY |
| Membership invalid | DENY |
| Membership revoked | DENY |
| Membership expired where applicable | DENY |
| Resource unknown | DENY |
| Resource ambiguous | DENY |
| Resource Business Entity mismatch | DENY |
| Action unknown | DENY |
| Action unsupported | DENY |
| Resource x Action applicability unresolved | DENY |
| Entitlement missing | DENY |
| Entitlement non-applicable | DENY |
| Entitlement revoked | DENY |
| Entitlement disabled | DENY |
| Entitlement expired where applicable | DENY |
| required authority unavailable | DENY |
| known stale required state | DENY |
| unresolved conflict | DENY |
| browser-only assertion | DENY |
| Cognito-only authorization assertion | DENY |
| IAM-only business authorization assertion | DENY |
| AI-generated authorization assertion | DENY |
| previous ALLOW only | DENY |

This matrix is governance, not executable code.

## 57. Positive ALLOW Matrix

ALLOW may occur only when:

1. authentication evidence is valid;
2. exactly one valid Principal is resolved;
3. the applicable Governed Business Entity is valid;
4. required Membership is valid;
5. required scope is valid;
6. Governed Resource is valid;
7. Requested Action is canonical and applicable;
8. authoritative Entitlement is valid and applicable;
9. no authoritative revocation, disablement, or expiry blocks access;
10. required authority sources are available;
11. no unresolved ambiguity or conflict exists;
12. all other applicable governed predicates succeed.

Partial satisfaction must not produce ALLOW.

## 58. Side-Effect Safety

Authorization evaluation itself must not mutate:

- Membership;
- Entitlement;
- Resource;
- Principal;
- Assessment truth;
- EIP truth;
- administrative state.

A DENY must not create authorization state.

An ALLOW decision itself must not create a grant.

## 59. SUBMIT Action Safety

Authorization to SUBMIT governs permission to perform the SUBMIT Action.

It must not imply:

- submitted data is valid;
- Assessment methodology accepts the data;
- Assessment result is predetermined;
- producer truth is changed outside producer logic.

Authorization and business validation remain separate.

## 60. DOWNLOAD Action Safety

Authorization to DOWNLOAD does not automatically imply:

- VIEW;
- EXPLAIN;
- SUBMIT;
- future DOWNLOAD;
- access to related Resources.

Any such relationship requires separate approved governance.

## 61. VIEW Action Safety

Authorization to VIEW does not automatically imply:

- DOWNLOAD;
- EXPLAIN;
- SUBMIT;
- administrative access.

Any such relationship requires separate approved governance.

## 62. EXPLAIN Action Safety

Authorization to EXPLAIN does not authorize AI to:

- recalculate assessment truth;
- override findings;
- change risk;
- change recommendations;
- change executive intelligence;
- expand Resource access.

AI remains explanation-only.

## 63. Assessment Service Protection

Assessment Service remains the sole authoritative deterministic assessment
truth producer.

Authorization decisions must not modify:

- Assessment methodology;
- Assessment scores;
- dimension scores;
- readiness;
- risk;
- severity;
- confidence;
- recommendations;
- executive summaries;
- BusinessDecisionPackage truth;
- ExecutiveAssessmentSnapshot truth.

## 64. EIP Protection

EIP remains the authoritative executive intelligence and Website Projection
Delivery Contract producer.

Authorization decisions must not modify:

- Executive Intelligence Package truth;
- Website Projection Delivery Contract truth;
- EIP derivation logic;
- EIP producer lineage.

Authorization may determine whether a Principal may access a governed EIP
Resource. It may not alter EIP truth.

## 65. Trusted Runtime Relationship

The approved runtime-owner governance preserves
`/Users/aiadmin/aws-ai-knowledge-assistant` as the repository ownership domain
permitted to host a future separate deterministic trusted logical service.

However:

- repository ownership is not authorization authority;
- Lambda presence is not authorization authority;
- AI Knowledge Assistant is not authorization authority;
- Bedrock is not authorization authority;
- Cognito is not authorization decision authority.

This artifact does not authorize implementation.

## 66. Service Contract Boundary

Trusted Authorization Service Contract remains DOWNSTREAM.

This artifact does not define:

- endpoint;
- HTTP method;
- route;
- request payload;
- response payload;
- status code;
- Lambda handler;
- API Gateway integration;
- SDK;
- client library.

## 67. Persistence Boundary

Authorization Persistence Authority remains UNRESOLVED / DOWNSTREAM.

This artifact does not select how authoritative Principal mapping, Membership,
Entitlement, revocation, administrative authority, Resource identity, decision
evidence, or audit evidence are stored.

No database, document, table, record, cache, file, event, or external
persistence mechanism is selected.

## 68. Technology Neutrality

This artifact is technology-neutral.

It does not select:

- DynamoDB;
- S3;
- SQL;
- PostgreSQL;
- MySQL;
- Redis;
- filesystem;
- cache;
- queue;
- event bus;
- API Gateway implementation;
- Lambda implementation;
- Cognito groups;
- custom claims;
- IAM identities;
- IAM roles;
- RBAC;
- ABAC;
- ACL;
- OPA;
- policy engine;
- workflow engine;
- Bedrock;
- LLM;
- RAG;
- vector database;
- authorization library;
- framework.

Existing technologies may appear only as evidence, boundaries, explicit
exclusions, or non-selections.

## 69. Implementation Gate

This artifact does not authorize:

- authorization runtime;
- policy engine;
- authorization service;
- Lambda implementation;
- API Gateway route;
- database;
- persistence;
- schema;
- tables;
- cache;
- RBAC;
- ABAC;
- ACL;
- Cognito changes;
- IAM changes;
- Website changes;
- Assessment Service changes;
- EIP changes;
- AWS runtime changes;
- AI changes;
- Bedrock changes;
- deployment.

No implementation may begin from this artifact alone.

## 70. Authority Status Model

| Area | Status |
| --- | --- |
| Authentication evidence semantics | GOVERNED CONCEPTUALLY |
| Stable Principal semantics | GOVERNED CONCEPTUALLY |
| Principal mapping authority source | UNRESOLVED |
| Client / Organization identity semantics | GOVERNED CONCEPTUALLY |
| Client / Organization authority source | UNRESOLVED |
| Membership semantics | GOVERNED CONCEPTUALLY |
| Membership authority source | GOVERNED CONCEPTUALLY / CONCRETE SOURCE UNRESOLVED |
| Engagement scope | PARTIALLY GOVERNED / DOWNSTREAM |
| Workspace scope | OPTIONAL / FUTURE |
| Governed Resource identity semantics | GOVERNED CONCEPTUALLY |
| Resource authority source | UNRESOLVED |
| Requested Action vocabulary | GOVERNED |
| Resource x Action applicability | PARTIALLY GOVERNED / DOWNSTREAM |
| Entitlement semantics | GOVERNED |
| Entitlement authority class | GOVERNED |
| Entitlement authority source | GOVERNED CLASS / CONCRETE SOURCE UNRESOLVED |
| Administrative authority semantics | GOVERNED |
| Revocation semantics | GOVERNED |
| Administrative authority source | UNRESOLVED |
| Deterministic Authorization Decision semantics | GOVERNED BY THIS ARTIFACT |
| Authorization decision authority runtime | DOWNSTREAM / UNAUTHORIZED |
| Authorization persistence | UNRESOLVED / DOWNSTREAM |
| Trusted Authorization Service Contract | DOWNSTREAM |
| Authorization implementation | UNAUTHORIZED |

Unresolved and downstream matters remain unresolved and downstream.

## 71. Remaining Governance Dependencies

Remaining dependencies are ranked as follows:

1. Resource x Action Applicability Governance v1
2. Engagement Scope Governance v1
3. Trusted Authorization Service Contract v1
4. Authorization Persistence Authority Review
5. Administrative Bootstrap / Root Authority Governance v1
6. Administrative Separation-of-Duties Governance v1
7. Authorization Audit / Observability Governance v1
8. Security / IAM Boundary Review

Resource x Action Applicability Governance v1 is the highest-value bounded
next increment because ALLOW requires a Requested Action to be both canonical
and applicable to the governed Resource, and the complete applicability matrix
is not yet governed.

## 72. Acceptance Criteria

This artifact is acceptable if:

- it defines Authorization Decision semantics without implementation;
- it limits final runtime outcomes to ALLOW and DENY;
- it preserves default-DENY behavior;
- it requires all applicable governed predicates for ALLOW;
- it preserves authentication, Principal, Membership, Resource, Action,
  Entitlement, Administration, retrieval, and producer-truth separations;
- it preserves Website/browser, Cognito, IAM, and AI non-authority;
- it preserves fail-closed behavior for unknown, missing, unavailable,
  ambiguous, conflicting, stale, revoked, disabled, expired, and unsupported
  state;
- it preserves privacy-by-design and denial information controls;
- it does not select persistence, schemas, APIs, endpoints, policy engines,
  role models, or implementation technology;
- it leaves unresolved/downstream matters unresolved/downstream.

## 73. Architecture Decision

Nguyen AI Platform Authorization Decision semantics are governed as a
deterministic server-side evaluation that produces ALLOW only when every
applicable governed predicate is affirmatively valid and no blocking state
exists.

All other cases produce DENY.

This decision governs semantics only. It does not authorize implementation,
runtime ownership changes, service contracts, persistence, schemas, APIs,
policy engines, Cognito changes, IAM changes, Website changes, Assessment
Service changes, EIP changes, AWS runtime changes, AI changes, Bedrock changes,
deployment, or the next governance increment.
