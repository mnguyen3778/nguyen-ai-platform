# Entitlement Authority Source Governance v1

## 1. Purpose

This document governs the authoritative source requirements for Nguyen AI
Entitlement state.

Its purpose is to define what constitutes authoritative Entitlement state and
what properties an Entitlement Authority MUST satisfy before future
deterministic authorization can rely on it.

This document does not implement Entitlements, authorization, storage,
administration, APIs, schemas, runtime services, or deployment.

## 2. Status

Version: v1

Status: Governance artifact.

Entitlement Authority source class: GOVERNED CONCEPTUALLY by this artifact.

Concrete Entitlement Authority implementation: UNRESOLVED.

Entitlement persistence: UNRESOLVED.

Entitlement provisioning: UNRESOLVED / DOWNSTREAM.

Entitlement administration: DOWNSTREAM.

Entitlement revocation administration: DOWNSTREAM.

Trusted Authorization Service Contract: DOWNSTREAM.

Implementation: UNAUTHORIZED.

## 3. Scope

This artifact governs only:

- the meaning of Entitlement Authority;
- the minimum properties required of an authoritative Entitlement source;
- authority-source class eligibility;
- non-authority boundaries for existing systems;
- fail-closed authority-resolution semantics;
- audit, privacy, and traceability expectations at the conceptual level.

This artifact MUST NOT select storage, schemas, service endpoints, APIs,
runtime routes, data models, administrative workflows, role models, policy
engines, or implementation technology.

## 4. Governing Context

The current authorization-governance chain is:

verified authentication evidence -> stable Principal -> Governed Business
Entity -> valid Membership -> applicable governed scope where required ->
Governed Resource -> canonical Requested Action -> applicable valid
Entitlement -> deterministic authorization evaluation -> ALLOW / DENY.

This artifact sits after Entitlement Semantics Governance v1. It does not
redefine Principal, Membership, Resource, Requested Action, Entitlement
semantics, or ALLOW / DENY semantics.

## 5. Definitions

Entitlement means the governed authorization basis established by Entitlement
Semantics Governance v1.

Entitlement Authority means the trusted governed source or source class capable
of authoritatively asserting applicable Entitlement state.

Authority resolution means the deterministic determination of authoritative
Entitlement state for the applicable Principal, governed scope, Resource, and
canonical Requested Action.

Authoritative state means the state that future deterministic authorization may
consume as Entitlement evidence, subject to all other governed inputs.

## 6. Entitlement Authority Definition

Entitlement Authority is the trusted governed business authorization authority
capable of asserting whether applicable Entitlement state is present, absent,
valid, revoked, expired where applicable, not-yet-valid where applicable, stale
where applicable, ambiguous, conflicting, malformed, unsupported, or
unavailable.

The Entitlement Authority MUST be distinct from the Entitlement itself. The
Authority asserts state; the Entitlement is the governed authorization basis
whose state is being asserted.

## 7. Authorization Chain Position

Entitlement Authority participates only at the Entitlement-state step of the
authorization chain.

It MUST NOT replace authentication, Principal mapping, Business Entity
identity, Membership validation, Resource lookup, Resource retrieval, Requested
Action canonicalization, Resource + Action applicability, or final ALLOW / DENY
evaluation.

The future trusted authorization boundary will consume authoritative
Entitlement state together with other governed inputs before producing ALLOW or
DENY.

## 8. Entitlement / Authority Separation

Entitlement Authority MUST NOT be treated as the Entitlement.

An Entitlement is a governed authorization basis. Entitlement Authority is the
trusted source that can assert the applicable state of that basis.

The presence of an authority source does not by itself mean any Principal has a
valid Entitlement.

## 9. Authority / Persistence Separation

Entitlement Authority MUST remain distinct from Entitlement persistence.

Authority defines which governed source is trusted to assert Entitlement state.
Persistence concerns how authoritative state MAY later be stored, retained, or
maintained.

This artifact does not select DynamoDB, S3, SQL, PostgreSQL, MySQL, Redis,
filesystem, documents, tables, records, cache, external database, or any other
persistence mechanism.

## 10. Authority / Administration Separation

Entitlement Authority MUST remain distinct from Entitlement administration.

This artifact does not determine who grants Entitlements, who approves
Entitlements, who revokes Entitlements, administrator identity, admin roles,
admin UI, approval workflow, operator workflow, provisioning workflow, or
support workflow.

Administration and revocation administration remain downstream governance.

## 11. Authority / Enforcement Separation

Entitlement Authority MUST remain distinct from authorization enforcement.

The Entitlement Authority provides authoritative Entitlement state. The future
trusted deterministic authorization boundary consumes that state with all other
required governed inputs and produces ALLOW or DENY.

The authority source itself MUST NOT automatically become the decision engine.

## 12. Required Authority Properties

An authoritative Entitlement source MUST be:

- trusted;
- server-side;
- deterministic;
- non-AI;
- auditable;
- authoritative for Entitlement state;
- consistent for equivalent governed inputs and equivalent authoritative state;
- fail-closed;
- capable of stable governed identity references;
- capable of representing lifecycle state;
- capable of distinguishing absence from unavailable authority;
- capable of asserting revocation state;
- capable of asserting temporal validity where applicable;
- capable of asserting freshness where required;
- capable of scope applicability;
- capable of Resource applicability;
- capable of Action applicability.

These are conceptual requirements. They do not prescribe implementation
technology.

## 13. Trusted Server-Side Requirement

Authoritative Entitlement state MUST be resolved within a trusted server-side
boundary.

Website state, browser state, client-side application state, and
client-supplied Entitlement state MUST NOT become authoritative merely because a
request is authenticated.

## 14. Deterministic Authority Requirement

Entitlement authority resolution MUST be deterministic.

Equivalent governed inputs and equivalent authoritative state MUST produce
equivalent authority-resolution results.

Probabilistic, model-based, semantic-similarity, or natural-language inference
MUST NOT authoritatively resolve Entitlement state.

## 15. AI Non-Authority

AI, Bedrock, LLMs, RAG, embeddings, semantic similarity, conversation history,
prompt output, model reasoning, agent reasoning, AI-generated roles, and
AI-generated permissions MUST NOT serve as Entitlement Authority.

AI MUST NOT grant, revoke, infer, repair, expand, merge, or override
Entitlement state. AI MUST NOT resolve ambiguity or conflicts authoritatively.
AI MUST NOT override DENY.

## 16. Authentication / Cognito Boundary

Cognito authentication is authentication evidence, not Entitlement Authority.

Cognito user identity, Cognito subject, email address, username, Cognito
groups, custom claims, token claims, and authenticated session state MUST NOT
be treated as authoritative Entitlement state unless separately approved
governance explicitly establishes that authority.

This artifact establishes no such approval.

## 17. IAM Boundary

IAM permissions MAY govern AWS infrastructure access. IAM permissions MUST NOT
automatically constitute Nguyen AI business Entitlement for Client,
Organization, Engagement, Workspace, Resource, VIEW, DOWNLOAD, SUBMIT, or
EXPLAIN access.

IAM is not selected as Entitlement Authority by this artifact.

## 18. Website / Browser Boundary

Website remains presentation-only.

Browser-provided Principal ID, Client ID, Organization ID, Engagement ID,
Workspace ID, Resource ID, Action, role, permission, or Entitlement MUST remain
request context until validated by a future trusted deterministic server-side
authorization boundary.

Browser state MUST NOT grant or widen Entitlement.

## 19. Membership Authority Boundary

Membership Authority MUST remain distinct from Entitlement Authority.

Valid Membership MAY be a prerequisite for authorization where applicable, but
Membership presence MUST NOT automatically generate VIEW, DOWNLOAD, SUBMIT,
EXPLAIN, or any future Action Entitlement.

Membership alone MUST NOT authorize Resource access, Engagement access,
Workspace access, or AI context access.

## 20. Resource Authority Boundary

Resource identity authority and Resource lookup authority MUST remain distinct
from Entitlement Authority.

Resource existence, Resource identity, Resource association with a Client or
Organization, Resource metadata, Resource discovery, Resource lookup success,
and Resource retrieval success MUST NOT grant Entitlement.

Resource metadata MAY be an authorization input, but it MUST NOT itself be
permission.

## 21. Action Vocabulary Boundary

Requested Action vocabulary MUST remain distinct from Entitlement Authority.

The current governed Actions are VIEW, DOWNLOAD, SUBMIT, and EXPLAIN.

Recognition of an Action name MUST NOT create Entitlement. Action existence
MUST NOT imply authorization.

## 22. Assessment Service Boundary

Assessment Service remains the sole authoritative deterministic assessment
truth producer.

Assessment Service organization fields, respondent fields, request IDs,
assessment IDs, BusinessDecisionPackage output, ExecutiveAssessmentSnapshot
output, methodology, findings, recommendations, readiness, risk, severity, and
confidence MUST NOT automatically establish portal Entitlement.

Assessment Service is not selected as Entitlement Authority by this artifact.

## 23. EIP Boundary

Executive Intelligence Platform remains the authoritative producer of executive
intelligence and Website Projection Delivery Contract output.

EIP producer identity, snapshot identity, package identity, projection identity,
publication state, freshness state, classification state, compatibility state,
lineage, authorizationScopeState, and retrieval success MUST NOT automatically
become Entitlement Authority.

EIP is not selected as Entitlement Authority by this artifact.

## 24. Conversation History Boundary

Conversation history MUST NOT become Entitlement Authority.

Prior AI conversations, prior successful assistant requests, prior Resource
references, previously discussed Clients, previously discussed Organizations,
and previously discussed Engagements MUST NOT establish current Entitlement.

Existing conversation-history storage MUST NOT be reused as Entitlement
persistence without separate governance.

## 25. Cache Boundary

Cached state MUST NOT become an independent Entitlement Authority.

If future caching is introduced, cached data MAY represent authoritative state
only under separately governed freshness and invalidation semantics.

Stale cached permissive state MUST NOT override current authoritative state.

This artifact does not select caching.

## 26. Candidate Authority Classes

Candidate authority classes are classified as follows:

Dedicated governed Nguyen AI business authorization authority within a trusted
deterministic server-side domain: eligible in principle.

Existing authentication authority: insufficient alone and non-authoritative for
Entitlement.

Membership authority: insufficient alone and non-authoritative for
Entitlement.

Resource authority: insufficient alone and non-authoritative for Entitlement.

Assessment Service: ineligible as Entitlement Authority under current approved
producer boundaries.

EIP: ineligible as Entitlement Authority under current approved producer
boundaries.

Website/browser: ineligible.

AI Knowledge Assistant conversational capability: ineligible.

AWS infrastructure identity or infrastructure authorization: insufficient
alone and non-authoritative for Nguyen AI business Entitlement.

External business system: unresolved. It MAY only contribute to future
authoritative state if separately governed and reconciled into a deterministic
authoritative view.

## 27. Authoritative Class Decision

The authoritative class for Entitlement state MUST be a dedicated governed
Nguyen AI business authorization authority operating within the trusted
deterministic server-side authorization domain.

This class decision does not select a product, database, repository
implementation, table, record, schema, service endpoint, API, route, Lambda
handler, policy engine, identity-provider feature, or storage mechanism.

Concrete implementation remains unauthorized and unresolved.

## 28. Single Authoritative View Requirement

Future authorization MUST consume one authoritative resolved view of applicable
Entitlement state.

If future Entitlement state originates from multiple governed administrative or
upstream sources, authoritative reconciliation MUST itself be governed,
deterministic, auditable, and fail-closed.

The future authorization boundary MUST NOT independently reconcile conflicting
ungoverned sources.

## 29. Absence vs Authority-Unavailable

Authoritative no-applicable-Entitlement and Entitlement Authority unavailable
are distinct states.

Both produce DENY under current semantics, but they MUST remain distinguishable
for auditability, operations, future service contracts, and deterministic
reason classification.

## 30. Unknown Authority State

If authoritative Entitlement state cannot be determined, authorization MUST
fail closed to DENY.

There MUST be no fallback to Membership, browser state, previous permission,
cached permissive state, Resource possession, Cognito, IAM, AI, conversation
history, or semantic similarity.

## 31. Ambiguous Authority State

If Entitlement Authority cannot resolve applicable state unambiguously,
authorization MUST fail closed to DENY.

The system MUST NOT choose first match, last match, broadest grant, most recent
grant, cached grant, AI-selected grant, or human-looking label unless a future
governance artifact explicitly establishes a deterministic rule.

## 32. Conflicting Authority State

If authoritative Entitlement state is internally conflicting and no separately
governed deterministic conflict rule resolves the conflict, authorization MUST
fail closed to DENY.

This artifact does not introduce grant-wins, deny-wins, latest-wins,
most-specific-wins, first-match, or last-match precedence.

## 33. Authority Unavailable

If required Entitlement Authority is unavailable, authorization MUST fail
closed to DENY.

The system MUST NOT fall back to another non-authoritative source.

Authority unavailable MUST remain distinct from ordinary Entitlement absence.

## 34. Revocation Authority Semantics

The authoritative source class MUST be capable of asserting that an Entitlement
is revoked.

A revoked Entitlement MUST NOT authorize.

This artifact does not determine who revokes, how revocation is stored, how
revocation is transmitted, revocation API design, administrative workflow, or
operator process.

## 35. Temporal Validity Authority

Where governed Entitlement validity bounds apply, the authoritative source
class MUST be capable of asserting relevant temporal validity state, including
currently valid, expired, and not-yet-valid.

This artifact does not require all Entitlements to expire and does not select
clock, TTL, scheduler, storage, or runtime mechanisms.

## 36. Freshness / Staleness

The authority model MUST support determining when state is not trustworthy as
current where freshness is required.

Known-stale authority state MUST NOT authorize.

This artifact does not define cache duration, TTL, replication, synchronization,
or invalidation mechanisms.

## 37. Business Entity Scope

Entitlement Authority MUST preserve strict Governed Business Entity isolation.

Authority for one Client or Organization context MUST NOT silently authorize
another Client or Organization context.

No default Client, previous Client, related Client, similar Organization,
cross-client substitution, or cross-organization substitution is allowed.

## 38. Engagement Scope

Engagement remains PARTIALLY GOVERNED / DOWNSTREAM.

Where Entitlement semantics require Engagement scope, the authority source
class MUST be capable of asserting applicable governed Engagement scope.

This artifact does not make Engagement universally mandatory and does not
define Engagement persistence.

## 39. Workspace Boundary

Workspace remains OPTIONAL / FUTURE.

Workspace MUST NOT become a mandatory Entitlement dimension through this
artifact.

The authority model MUST remain capable of incorporating future Workspace scope
without redefining core Entitlement Authority semantics.

## 40. Resource Scope

The authority source class MUST be capable of associating applicable
Entitlement state with the Governed Resource or Resource scope required by
authorization.

This artifact does not define resource keys, table keys, document keys, foreign
keys, indexes, schemas, or storage structures.

## 41. Action Scope

The authority source class MUST support independent treatment of canonical
Requested Actions: VIEW, DOWNLOAD, SUBMIT, and EXPLAIN.

There is no automatic Action inheritance.

VIEW authority MUST NOT automatically imply DOWNLOAD.

VIEW authority MUST NOT automatically imply EXPLAIN.

SUBMIT authority MUST NOT imply CREATE, UPDATE, or MODIFY.

## 42. Wildcard Boundary

This artifact does not introduce default wildcard Entitlement authority for all
Clients, all Organizations, all Engagements, all Workspaces, all Resources, or
all Actions.

Wildcard semantics, if ever required, require separate governance.

## 43. Role Model Boundary

Entitlement Authority MUST NOT require roles.

This artifact does not introduce RBAC, ABAC, ACLs, role hierarchy, role
templates, permission bundles, or admin roles.

Future administration MAY use abstractions only if separately governed.

## 44. Provisioning Status

Entitlement provisioning remains UNRESOLVED / DOWNSTREAM.

This artifact does not define how Entitlement state enters the authority.

Manual provisioning, automated provisioning, sync, import, admin UI, workflow,
API, and batch process are not authorized here.

## 45. Administration Status

Entitlement administration remains DOWNSTREAM.

This artifact does not determine administrator identity, admin roles, approval
authority, grant workflow, revocation workflow, change workflow, support
workflow, or operator model.

## 46. Persistence Status

Entitlement persistence remains UNRESOLVED.

This artifact does not select storage and does not create schema, table,
record, document, partition key, sort key, index, foreign key, TTL, database, or
cache design.

## 47. Service Contract Status

Trusted Authorization Service Contract remains DOWNSTREAM.

This artifact does not define endpoint, route, HTTP method, request schema,
response schema, status code, Lambda handler, API Gateway integration, or
service contract.

## 48. Audit Requirements

Future trusted Entitlement authority resolution SHALL be capable of recording,
where appropriate:

- verified Principal reference;
- business-scope reference;
- Resource reference;
- canonical Action;
- authority reference and version;
- resolution outcome;
- Entitlement state;
- validity state;
- revocation state;
- freshness state where applicable;
- reason classification;
- correlation identifier;
- timestamp.

Audit design MUST NOT require raw tokens, credentials, secrets, unnecessary
claims, unnecessary PII, or unnecessary profile data.

This artifact does not select logging technology.

## 49. Privacy Requirements

Entitlement Authority MUST follow minimum-necessary-information principles.

Authority resolution MUST use stable governed identifiers rather than
unnecessary human-readable identity data where governed identifiers are
sufficient for the authorization purpose.

Website and browser delivery MUST receive only information necessary for the
authorized task.

## 50. Authority Versioning / Traceability

Authoritative Entitlement state and authority semantics MUST support conceptual
traceability to the governing authority/version applicable at evaluation time.

Future authorization decisions MUST be reproducible from governed inputs,
authoritative state, and the applicable authority semantics.

This artifact does not create version columns, schemas, storage structures, or
runtime identifiers.

## 51. Failure Mode Matrix

| Authority-resolution condition | Governed outcome |
| --- | --- |
| Authority returns applicable valid Entitlement state | Eligible to continue deterministic authorization evaluation |
| Authority returns no applicable Entitlement | DENY |
| Authority state unknown | DENY |
| Authority state malformed | DENY |
| Authority state ambiguous | DENY |
| Authority state conflicting and unresolved | DENY |
| Authority state revoked | DENY |
| Authority state expired where applicable | DENY |
| Authority state not-yet-valid where applicable | DENY |
| Authority state known stale | DENY |
| Authority unavailable | DENY |
| Business scope mismatch | DENY |
| Resource mismatch | DENY |
| Action mismatch | DENY |

The valid-state outcome does not equal ALLOW. It only permits the future
trusted authorization boundary to continue evaluating all required governed
inputs.

## 52. Trusted Runtime Relationship

The aws-ai-knowledge-assistant repository remains the approved ownership domain
for a future separate deterministic trusted logical service.

That repository ownership does not mean the AI Knowledge Assistant
conversational capability is Entitlement Authority.

Entitlement Authority logically belongs within the future trusted deterministic
server-side authorization domain, but this artifact does not authorize
implementation or assign a concrete runtime component.

## 53. Producer / Consumer Boundary Verification

Assessment Service remains the assessment truth producer.

EIP remains the executive intelligence and Website Projection Delivery Contract
producer.

Website remains a presentation consumer.

AI Knowledge Assistant remains a consumer/explainer.

The future trusted deterministic authorization domain will consume governed
authority state after separate implementation authorization.

Entitlement Authority is the authoritative business authorization-state source
class governed by this artifact.

These responsibilities MUST NOT be blurred.

## 54. Technology Neutrality

This artifact does not select or prescribe DynamoDB, S3, SQL, PostgreSQL,
MySQL, Redis, filesystem, cache, queue, event bus, API Gateway implementation,
Lambda implementation, Cognito groups, custom claims, IAM identities, IAM
policies, RBAC, ABAC, ACL, policy engine, CRM, external identity database,
Bedrock, LLM, RAG, or vector database.

Existing technologies MAY appear only as current evidence, existing constraints,
explicit exclusions, or non-authoritative systems.

## 55. Implementation Gate

This artifact DOES NOT AUTHORIZE:

- Entitlement implementation;
- Entitlement persistence;
- Entitlement provisioning;
- Entitlement administration;
- Entitlement revocation workflow;
- authorization implementation;
- schemas;
- tables;
- documents;
- databases;
- APIs;
- endpoints;
- Lambda changes;
- API Gateway changes;
- Cognito changes;
- IAM changes;
- Website changes;
- Assessment Service changes;
- EIP changes;
- AWS runtime changes;
- Bedrock changes;
- AI changes;
- deployment.

Any future implementation requires separate governance authorization.

## 56. Remaining Governance Dependencies

Remaining dependencies are ranked as follows:

1. Authority Administration / Revocation Governance v1 - highest-value next
   bounded increment because authority-source class governance requires
   controlled lifecycle, grant, change, and revocation boundaries before
   persistence or service contracts.
2. Deterministic Authorization Decision Semantics v1 - needed to govern final
   ALLOW / DENY composition across Principal, Membership, Resource, Action, and
   Entitlement inputs.
3. Resource x Action Applicability Governance v1 - needed if future
   Entitlement governance requires a governed applicability matrix.
4. Trusted Authorization Service Contract v1 - downstream of authority,
   administration/revocation, and decision semantics.
5. Authorization Persistence Authority Review - downstream of authority-source,
   administration/revocation, and decision semantics.
6. Engagement Scope Governance v1 - downstream unless objective product
   evidence makes Engagement mandatory for a specific authorization surface.
7. EIP Retrieval Mechanism Governance - implementation-preparation work
   downstream of semantic authorization governance.
8. Website governed integration planning - downstream of service contract and
   implementation authorization.
9. AI governed context-delivery planning - downstream of authorization
   enforcement governance and service contract governance.
10. Authorization implementation - blocked until required governance gates are
   complete.

## 57. Acceptance Criteria

This artifact is acceptable only if it:

- defines Entitlement Authority without redefining Entitlement semantics;
- preserves Authority / Persistence separation;
- preserves Authority / Administration separation;
- preserves Authority / Enforcement separation;
- requires trusted server-side deterministic non-AI authority resolution;
- rejects Cognito, IAM, Website, browser state, Membership, Resource identity,
  Action vocabulary, Assessment Service, EIP, conversation history, cache, and
  AI as standalone Entitlement Authority;
- governs a dedicated Nguyen AI business authorization authority class without
  selecting technology;
- preserves absence versus authority-unavailable distinction;
- preserves fail-closed unknown, ambiguous, conflicting, stale, revoked,
  expired, and unavailable authority semantics;
- preserves Business Entity isolation and conditional Engagement scope;
- preserves Workspace as OPTIONAL / FUTURE;
- preserves independent Action treatment for VIEW, DOWNLOAD, SUBMIT, and
  EXPLAIN;
- leaves provisioning, administration, persistence, service contract, and
  implementation downstream or unresolved;
- preserves producer/consumer boundaries;
- remains technology-neutral.

## 58. Architecture Decision

Entitlement Authority Source Governance v1 governs the authoritative class and
minimum authority properties for Entitlement state.

The authorized authority class is a dedicated governed Nguyen AI business
authorization authority operating within the trusted deterministic server-side
authorization domain.

Concrete authority implementation, persistence, provisioning, administration,
revocation administration, trusted service contract, and implementation remain
unresolved or downstream.

The highest-value next bounded governance increment is Authority Administration
/ Revocation Governance v1.
