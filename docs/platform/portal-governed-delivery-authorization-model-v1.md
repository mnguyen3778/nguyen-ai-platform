# Portal Governed Delivery Authorization Model v1

## 1. Purpose and Scope

This document defines the architecture and governance model required to safely
transform authenticated Cognito identity evidence into authorization to receive
a governed Executive Intelligence Platform Website Projection Delivery artifact.

The scope is narrowly limited to authenticated Client Engagement Portal access
to governed EIP Website Projection Delivery artifacts.

The governed delivery artifact for this model is:

- `website-projection-delivery-contract-v1`

This document is architecture and governance only. It does not implement:

- runtime authorization
- API Gateway
- Lambda
- Cognito configuration
- DynamoDB
- S3
- EIP persistence
- EIP API
- Website endpoint
- AI Knowledge Assistant backend
- Bedrock
- RAG
- assessment methodology

This document does not define APIs, schemas, algorithms, persistence,
transport protocols, deployment architecture, infrastructure, production code,
or runtime behavior.

This model derives from the approved Platform Architecture Baseline v1,
Repository Ownership Baseline v1, Platform Integration Baseline v1, System
Context Baseline v1, Platform Governance Baseline v1, Repository Governance
Baseline v1, and Cross-Repository Contract Governance Baseline v1.

Website-local identity, authorization, tenancy, and security documents may
provide architectural evidence for portal requirements. They do not assign
cross-repository runtime ownership for this governed delivery boundary.

## 2. Architectural Invariants

The Assessment Service remains the sole authoritative producer of deterministic
assessment business truth.

The Executive Intelligence Platform remains the deterministic consumer and
deriver of assessment truth and the producer of governed executive
intelligence, including `website-projection-delivery-contract-v1`.

A trusted authorization and delivery backend is the future enforcement boundary
for identity-to-resource authorization and governed artifact delivery. That
boundary is not implemented or assigned by this document.

The Website remains a presentation-only consumer. It consumes governed Website
Projection Delivery Contracts and MUST NOT derive assessment truth, executive
intelligence, authorization truth, membership state, or entitlement state.

The AI Knowledge Assistant may become a future authorized consumer or explainer
only after separate architecture review. It MUST NOT become authoritative for
assessment truth, executive intelligence, governed delivery eligibility, or
authorization decisions.

Downstream consumers MUST NOT redefine upstream truth. They MUST preserve the
producer-owned meaning, lineage, version identity, and fail-closed boundaries
of upstream artifacts.

## 3. Authentication vs Authorization

Authentication answers:

```text
Who presented valid identity evidence?
```

Authorization answers:

```text
What Nguyen AI resources may this authenticated principal access right now?
```

Authentication evidence MAY identify a subject after server-side verification.
Authentication evidence MUST NOT by itself grant access to client data.

A valid Cognito token MUST NOT by itself grant access to client data.

Cognito claims, groups, roles, tenant values, client identifiers, engagement
identifiers, workspace identifiers, and custom claims MUST NOT independently
expand Nguyen AI resource authorization unless explicitly governed by a future
approved authority model.

Authorization MUST be evaluated by a trusted server-side boundary using current
Nguyen AI authoritative authorization state.

## 4. Principal Identity

A Nguyen AI principal is the conceptual subject evaluated for resource access
after authentication evidence has been verified by a trusted backend.

The future trusted backend MUST derive the principal from verified
authentication evidence. A stable external identity reference MAY be represented
conceptually as:

```text
identity_provider
+
provider_subject
```

This conceptual reference identifies the external authenticated subject. It is
not a database schema and does not define persistence.

Email is non-authoritative for resource authorization.

Browser-provided identity attributes are non-authoritative.

Unverified token claims are non-authoritative.

Only backend-verified identity evidence may enter authorization evaluation.

## 5. Authorization Resource Boundary

The minimum governed authorization resource scope for portal delivery is:

```text
client
+
engagement
+
workspace
```

The governed delivery resource exists within that boundary.

The conceptual authorization relationship is:

```text
Principal
        |
        v
Membership / Entitlement
        |
        v
Client
        |
        v
Engagement
        |
        v
Workspace
        |
        v
Governed Website Projection Delivery
```

Conceptual authorization keys identify governed scope. They are not physical
database keys, table keys, storage paths, object keys, or implementation
indexes.

Possession of a client, engagement, workspace, artifact, projection, or
delivery identifier MUST NOT be treated as authorization.

## 6. Authoritative Authorization State

A future server-side authority MUST exist before governed delivery to
authenticated portal users can be implemented.

That authority must conceptually address:

- principal identity
- membership
- role, permission, or entitlement
- client scope
- engagement scope
- workspace scope
- membership status
- revocation
- suspension
- expiration
- governed resource entitlement

Current Nguyen AI authorization records MUST override stale provider state,
stale browser state, stale session state, and stale token claims.

Missing, inactive, expired, suspended, revoked, ambiguous, conflicting, or
unavailable authoritative authorization state MUST result in denial.

This document does not choose DynamoDB, SQL, Cognito Groups, policy engines,
filesystems, caches, or any other persistence or evaluation technology.

## 7. Trusted vs Untrusted Inputs

The following browser-supplied inputs are UNTRUSTED and NON-AUTHORITATIVE:

- `clientId`
- `tenantId`
- `engagementId`
- `workspaceId`
- `organizationId`
- `role`
- `email`
- artifact ID
- projection ID
- delivery ID
- resource selection

A future backend MAY receive a resource reference if required by an approved API
contract, but it MUST independently verify entitlement before any governed
artifact is returned.

TRUSTED inputs may include only data derived from approved server-side
authorities after verification.

Possession of an identifier does not prove authorization.

## 8. Authorization Decision Model

The conceptual authorization decision is:

```text
verified principal
+
current authoritative membership
+
current role / entitlement
+
client boundary
+
engagement boundary
+
workspace boundary
+
resource eligibility
=
ALLOW or DENY
```

The default decision is DENY.

No UNKNOWN state may become implicit ALLOW.

Missing or unavailable authority state MUST fail closed.

This document does not implement an algorithm, evaluator, middleware, API,
query pattern, or runtime decision contract.

## 9. EIP Responsibility Boundary

EIP publication eligibility is separate from portal-user authorization.

EIP remains authoritative for the governed delivery contract and its existing:

- compatibility
- eligibility
- freshness
- lineage
- limitations
- classification
- publication state

The future authorization service MUST NOT recreate EIP publication,
compatibility, eligibility, freshness, lineage, limitation, classification, or
publication-state rules.

EIP's `authorizationScopeState` or equivalent governed contract indicator MUST
NOT be treated as proof that a particular Cognito principal is entitled to
receive the artifact.

Portal-user authorization MUST evaluate the verified principal against current
authoritative membership, entitlement, and governed resource scope.

## 10. Governed Delivery Rule

The narrow output allowed to cross into the Website for this use case is:

- `website-projection-delivery-contract-v1`

The future backend SHOULD return the narrowest governed client-safe artifact
required by the Website.

The future backend MUST NOT expose raw:

- assessment answers
- evidence
- BusinessDecisionPackage
- ExecutiveAssessmentSnapshot
- SnapshotCatalogEntry
- SnapshotDerivedArtifact
- Executive Intelligence Package

unless separately governed in a future approved version.

## 11. Fail-Closed Semantics

Authorization and governed delivery MUST deny or fail closed when any required
condition cannot be established.

At minimum, DENY or fail-closed behavior is required for:

- token missing
- token invalid
- token expired
- wrong issuer
- wrong audience
- identity unknown
- principal mapping absent
- membership absent
- membership inactive
- membership expired
- membership suspended
- membership revoked
- role or entitlement absent
- scope mismatch
- conflicting authorization state
- requested resource unauthorized
- engagement inactive
- workspace unauthorized
- governed delivery absent
- governed delivery unpublished
- governed delivery ineligible
- governed delivery incompatible
- governed delivery stale
- lineage invalid
- classification denied
- authorization authority unavailable
- artifact retrieval unavailable

No failure may cause:

- synthetic dashboard fallback
- cross-client fallback
- previous-client fallback
- broad or default client selection
- fabricated executive intelligence

## 12. Information Disclosure

Denial behavior MUST avoid cross-client information leakage.

A denied caller SHALL NOT learn:

- whether another client's artifact exists
- another client's identifiers
- another client's engagement status
- another client's workspace structure
- another client's projection metadata

Denial reason classification MAY support audit and operations review, but
caller-visible denial behavior MUST NOT disclose another client's resource
existence, structure, status, or metadata.

This document does not specify HTTP status codes unless a future approved
service contract requires them.

## 13. Audit Requirements

A future runtime implementation MUST produce audit evidence for authorization
decisions.

At minimum, audit obligations include:

- authorization decision timestamp
- verified principal reference
- action attempted
- governed resource scope
- allow or deny outcome
- reason classification
- policy or model version
- correlation or request identifier

Audit records MUST NOT log:

- raw access tokens
- secrets
- unnecessary sensitive payload content

This document does not choose a logging technology, storage technology, audit
transport, audit schema, or retention implementation.

## 14. Runtime Ownership Decision

Governance owner:

- `nguyen-ai-platform`

Future runtime owner:

- not yet assigned

Runtime ownership MUST NOT be assigned without objective repository evidence
and formal architecture review.

The Assessment Service cannot own this runtime authorization and delivery
boundary because that would contaminate the deterministic assessment producer
with downstream portal authorization and governed delivery concerns.

EIP cannot own portal-user authorization because that would mix executive
intelligence production and publication eligibility with application identity
entitlement.

The Website cannot own this boundary because browser or client-side
authorization is not a trusted security boundary.

`aws-ai-knowledge-assistant` cannot yet be assigned because the repository was
unavailable for inspection during the architecture review, so its actual
responsibility cannot be established from evidence.

Objective evidence required before assigning runtime ownership includes:

- local or reviewed repository availability
- approved repository identity
- approved ownership and exclusion boundaries
- evidence that the repository is intended to own trusted server-side
  authorization and governed delivery
- evidence that the ownership assignment preserves Assessment Service, EIP,
  Website, and Platform repository boundaries
- approved integration and contract boundaries for EIP retrieval and Website
  delivery
- governance approval of the runtime ownership decision

## 15. EIP Retrieval Prerequisite

EIP currently produces and serializes
`website-projection-delivery-contract-v1`, but no reviewed runtime persistence,
API, or retrieval mechanism exists for Website-facing governed delivery.

Therefore, a future endpoint implementation also requires an approved governed
retrieval boundary.

This document does not solve the retrieval boundary.

This document does not choose S3, DynamoDB, API Gateway, Lambda, queues,
databases, filesystems, object stores, caches, or any other retrieval,
persistence, or transport mechanism.

The governed retrieval boundary is a prerequisite to implementation of a live
backend-authorized EIP delivery endpoint.

## 16. Future Consumer Reuse

The trusted authorization boundary MAY eventually serve multiple authenticated
client-safe consumers, including:

- Executive Dashboard
- AI Knowledge Assistant
- reports or other authenticated client-safe consumers

Reuse is permitted only when each consumer receives only approved resources for
its approved purpose.

The AI Knowledge Assistant MUST remain a consumer or explainer. It MUST never
become authoritative for:

- assessment scores
- readiness
- severity
- risk
- confidence
- recommendations
- executive summaries
- authorization decisions

Any future consumer reuse MUST preserve producer-owned meaning, governed
resource scope, versioned contracts, fail-closed authorization, and
consumer-specific output minimization.

## 17. Versioning and Change Governance

Material changes to any of the following require formal version governance:

- authorization authority
- identity mapping
- resource scope
- trust model
- allow or deny semantics
- runtime ownership
- cross-repository responsibility

No implementation may silently redefine this model.

Any future revision MUST preserve approved repository ownership, producer and
consumer isolation, immutable evidence, deterministic behavior, end-to-end
lineage, fail-closed validation, versioned contracts, and explainability unless
an approved architectural supersession explicitly changes those requirements.

## 18. Implementation Gate

Before a live backend-authorized EIP delivery endpoint may be implemented, all
of the following prerequisites MUST be satisfied:

1. Authorization governance approved.
2. Runtime owner and repository assigned.
3. Stable verified-principal mapping approved.
4. Authoritative membership and entitlement authority approved.
5. Resource scope approved.
6. EIP governed delivery retrieval boundary approved.
7. Audit obligations approved.
8. Fail-closed semantics approved.
9. API or service contract separately reviewed.
10. Producer and consumer boundaries reconfirmed.

THIS GOVERNANCE ARTIFACT DOES NOT AUTHORIZE ENDPOINT IMPLEMENTATION BY ITSELF.

Implementation MUST NOT begin until the owning runtime repository has been
assigned through approved architecture governance and the implementation scope
has been separately approved for that repository.

## 19. Acceptance Criteria

This governance increment passes only if it establishes:

- authentication is not authorization
- server-side authorization authority is required
- browser identifiers are non-authoritative
- client plus engagement plus workspace scope is governed
- deny-by-default authorization behavior is required
- synthetic fallback is prohibited
- EIP eligibility is separate from user entitlement
- Website remains presentation-only
- Assessment Service remains the deterministic producer
- EIP remains the governed intelligence producer
- runtime owner is not guessed
- EIP retrieval prerequisite is recorded
- future AI consumer cannot alter business truth

This artifact is ready for review only if it preserves approved repository
ownership, approved producer and consumer boundaries, governed contract
boundaries, fail-closed semantics, and the Platform repository's
architecture-and-governance-only role.
