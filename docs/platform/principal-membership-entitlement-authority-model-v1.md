# Principal / Membership / Entitlement Authority Model v1

## 1. Purpose and Scope

This document establishes the deterministic authority model connecting verified
identity evidence to authorized Nguyen AI governed resources.

This document defines governance semantics only. It does not implement
principal mapping, membership, entitlement, authorization, APIs, endpoints,
persistence, schemas, databases, Cognito configuration, IAM, EIP retrieval,
Website behavior, Assessment Service behavior, AI behavior, Bedrock behavior,
or runtime code.

## 2. Authority Chain

The governed authorization authority chain is:

```text
authentication evidence
        |
        v
verified principal
        |
        v
membership
        |
        v
entitlement
        |
        v
governed scope
        |
        v
governed resource
        |
        v
ALLOW / DENY
```

Authentication is not authorization.

Membership is not entitlement.

Retrieval is not authorization.

Resource existence is not resource entitlement.

Every authority in the chain MUST be established by trusted server-side
evidence before access is allowed.

## 3. Verified Principal

A verified principal is the stable server-verified identity against which
authorization is evaluated.

A principal MUST originate from trusted server-side verification of approved
authentication evidence.

Browser-provided identity values are not authoritative.

This model does not require a specific Cognito claim as the principal key.
Future implementation MUST define any provider-subject mapping through approved
governance before use.

Email address MUST NOT be treated as inherently authoritative for resource
access.

## 4. Authentication Evidence

Authentication evidence is proof used to establish the verified principal.

Current Cognito infrastructure may provide authentication evidence.

Cognito authentication alone MUST NOT grant:

- client access
- engagement access
- workspace access
- report access
- dashboard access
- EIP artifact access
- Assessment artifact access

Authentication evidence MAY identify a subject after trusted server-side
verification. It MUST NOT create or expand Nguyen AI resource authorization.

## 5. Membership

Membership is an authoritative relationship between:

```text
principal
+
Nguyen AI client / organization boundary
```

Membership answers:

```text
Is this principal recognized as belonging to or acting within this governed
client / organization context?
```

Membership MUST be current, authoritative, and scoped.

Membership alone MUST NOT imply access to every engagement, workspace, report,
dashboard, artifact, AI context, or governed resource.

## 6. Entitlement

Entitlement is the authoritative permission allowing a verified principal,
within valid membership context, to perform an approved action against an
approved governed scope or resource.

Entitlement answers:

```text
May this principal perform this action against this governed resource?
```

Entitlement MUST be deterministic.

Entitlement MUST NOT be inferred by AI, browser state, token claims, email
domain, possession of identifiers, or previous successful access.

## 7. Client / Organization Scope

The client or organization boundary is the top-level governed business context
for authorization.

Authorization MUST prevent:

- cross-client access
- default-client fallback
- previous-client fallback
- browser-selected authoritative client
- email-domain-only authorization unless separately governed
- implicit organization assignment

Client or organization scope identifiers are conceptual authorization scope
references in this model. This document does not design storage schemas,
database keys, tenant indexes, or persistence records.

## 8. Engagement Scope

An engagement is a governed business scope subordinate to an authorized client
or organization relationship.

A principal MUST NOT receive engagement access solely because client membership
exists.

Engagement authorization MUST be explicit or deterministically derived from
separately approved authoritative entitlement rules.

Engagement identity and engagement lifecycle authority remain future
implementation prerequisites unless separately governed by an approved
authority source.

## 9. Workspace Scope

A workspace is a governed operational or resource boundary where applicable.

Current Platform governance uses workspace semantics as part of the minimum
portal delivery authorization scope:

```text
client
+
engagement
+
workspace
```

This document preserves workspace semantics without assuming every engagement
requires a workspace.

Workspace authority remains conceptual and unimplemented in this document.
Future implementation MUST define when workspace scope is required and how it
is established by authoritative state.

## 10. Governed Resource

A governed resource is an approved Nguyen AI resource whose delivery or use is
controlled by authorization.

Conceptual governed resources may include:

- Website Projection Delivery Contract
- executive dashboard delivery
- report
- approved assessment output
- engagement evidence
- authorized AI Knowledge Assistant context

These examples do not imply that every resource type is currently implemented
or authorized for delivery.

This document does not create resource schemas, resource registries, storage
models, lookup keys, route parameters, or resource APIs.

## 11. Action / Permission Model

Authorization evaluates:

```text
principal
+
membership
+
entitlement
+
scope
+
resource
+
requested action
```

This model does not design or select RBAC, ABAC, ACLs, policy engines, rule
engines, database tables, claims mapping, or permission schemas.

RBAC, ABAC, ACLs, and policy engines MAY be evaluated later as implementation
options only after the governing authority source and service contract are
approved.

## 12. ALLOW Semantics

ALLOW requires complete authoritative evidence sufficient to prove:

- principal valid
- membership valid
- entitlement valid
- requested scope valid
- requested resource valid
- requested action permitted
- relevant governed artifact state valid

No missing required authority may be inferred.

ALLOW MUST be deterministic and explainable from current trusted authority
state and governed producer state.

## 13. DENY Semantics

The default authorization decision is:

```text
DENY
```

Authorization MUST deny when required authority is:

- missing
- unknown
- unavailable
- malformed
- expired where applicable
- conflicting
- stale where applicable
- unsupported
- outside scope
- cross-client
- cross-engagement
- cross-workspace
- not entitled

Unknown MUST NOT become ALLOW.

## 14. Fail-Closed Authority

Authorization infrastructure failure MUST fail closed.

The authority model prohibits:

- synthetic membership
- synthetic entitlement
- guessed client
- guessed engagement
- guessed workspace
- previous successful authorization reuse without separately governed validity
- default client
- demo data
- fabricated governed resource
- AI-generated authorization decision

Failure to establish current authoritative state MUST produce denial and MUST
NOT produce substitute access.

## 15. Browser Trust Model

Browser-supplied values are requests or hints only.

At minimum, the following browser-supplied values are NON-AUTHORITATIVE until
validated against trusted server-side authority:

- `clientId`
- `organizationId`
- `tenantId`
- `engagementId`
- `workspaceId`
- `resourceId`
- `reportId`
- `projectionId`
- `deliveryId`
- `role`
- `email`

Possession or submission of an identifier MUST NOT prove authorization.

## 16. Role Semantics

Roles, if needed conceptually, are possible inputs to entitlement evaluation.
They are not automatically authoritative browser claims.

This document does not invent final production roles.

Role names, role assignment authority, role lifecycle, role scope, and role to
entitlement mapping remain future governance decisions unless already approved
by a separate authority model.

Provider groups, provider roles, browser roles, and custom token claims MUST
NOT independently grant or expand Nguyen AI resource authorization.

## 17. AI Prohibition

AI, Bedrock, LLMs, and RAG MUST NOT:

- establish principal identity
- establish membership
- establish entitlement
- select authoritative client
- select authoritative engagement
- select authoritative workspace
- authorize resources
- override DENY
- fabricate missing authority
- infer access from conversational context

AI MAY only consume already-authorized governed context after deterministic
authorization succeeds and a separate approved consumer boundary permits that
use.

## 18. Assessment Service Boundary

The Assessment Service remains the sole deterministic assessment business-truth
producer.

Authorization may govern who may receive an Assessment Service output.

Authorization MUST NOT change what the Assessment Service output means.

Authorization MUST NOT score assessments, alter assessment methodology,
reinterpret assessment truth, or fabricate Assessment Service outputs.

## 19. EIP Boundary

The Executive Intelligence Platform remains the executive-intelligence and
Website Projection Delivery Contract producer.

Authorization governs whether a principal may receive an already-governed EIP
artifact.

Authorization MUST NOT:

- derive EIP intelligence
- repair EIP output
- change publication state
- change eligibility
- change freshness
- change lineage
- change classification

## 20. Retrieval Relationship

Retrieval is not authorization.

Possible governed flow:

```text
authorized request
        |
        v
resource scope resolution
        |
        v
governed EIP retrieval
        |
        v
entitlement enforcement
        |
        v
authorized delivery
```

Another separately governed ordering MAY be approved if security or producer
constraints require it.

This document does not lock implementation ordering.

The invariant is that retrieval success does not itself grant principal
entitlement.

## 21. Website Boundary

The Website remains presentation-only.

The Website MUST NOT become authority for:

- principal
- membership
- entitlement
- client scope
- engagement scope
- workspace scope
- resource access

The Website MAY request resources and render authorized results.

Browser-held authentication state and browser-submitted identifiers remain
non-authoritative until evaluated by trusted server-side authority.

## 22. Trusted Runtime Responsibility

The future separate deterministic trusted logical service in
`aws-ai-knowledge-assistant` is the assigned runtime ownership domain for
future enforcement.

This document does not authorize implementation of that logical service.

The logical service remains separate from the AI Knowledge Assistant.

The logical service MUST enforce authorization deterministically if and when
implementation is separately authorized.

## 23. Authority Source Status

Current objective evidence does not establish approved runtime authority
sources for principal mapping, membership, entitlement, or governed resource
authorization.

Authority source status:

| Authority area | Status | Evidence |
| --- | --- | --- |
| Principal mapping | UNRESOLVED | Cognito authentication evidence exists, but no approved Nguyen AI principal mapping authority exists. |
| Membership | UNRESOLVED | Website-local J1 governance describes membership requirements, but no approved cross-repository runtime membership authority exists. |
| Entitlement | UNRESOLVED | Entitlement semantics are required by Platform governance, but no approved entitlement authority exists. |
| Client scope | PARTIAL EVIDENCE ONLY | Platform and Website governance use client scope concepts, but no approved authority source for client access exists. |
| Engagement scope | PARTIAL EVIDENCE ONLY | Platform and Website governance use engagement scope concepts, but no approved authority source for engagement access exists. |
| Workspace scope | PARTIAL EVIDENCE ONLY | Platform and Website governance use workspace scope concepts, but no approved authority source for workspace access exists. |
| Resource scope | PARTIAL EVIDENCE ONLY | EIP and Website Projection Delivery governance define governed resource concepts, but no approved runtime resource authorization authority exists. |

This document does not invent an authority source.

## 24. Persistence Non-Selection

This document does not select:

- DynamoDB
- S3
- SQL
- filesystem
- Cognito groups
- token custom claims
- configuration files
- another database

as the authority store.

Existing DynamoDB conversation-history capability in the AWS repository does
not become authorization persistence automatically.

Authority storage, authority lifecycle, and consistency requirements remain
future governance decisions.

## 25. Authority Administration

A future governed mechanism will be required to create, update, revoke, and
audit membership and entitlement authority.

This document does not design an administration UI, administration API,
workflow engine, approval process, database, or operational procedure.

This document does not assign human administrators, service operators, role
names, or approval roles.

Authority administration is an implementation prerequisite and requires
separate governance before runtime implementation.

## 26. Revocation

Membership and entitlement authority MUST be revocable.

Revoked authority MUST NOT continue granting access indefinitely.

Future implementation MUST define how revocation is represented, evaluated,
audited, and enforced before authorization is enabled.

This document does not select caching, token invalidation, session invalidation,
provider revocation, data replication, or consistency implementation.

## 27. Auditability

Future authorization decisions MUST be auditable.

At minimum, future authorization audit evidence should include:

- verified principal reference
- requested action
- requested governed scope
- decision
- reason classification
- authority or version reference where applicable
- request or correlation identifier
- timestamp

Audit evidence MUST NOT log raw tokens, secrets, credentials, unnecessary
sensitive payload content, or unapproved upstream artifacts.

This document does not select logging technology, audit storage, audit schema,
retention, telemetry transport, or monitoring implementation.

## 28. Privilege Principle

Authorization MUST follow:

- least privilege
- explicit scope
- deny by default
- no implicit inheritance unless separately governed
- no privilege expansion through AI or presentation state

Authorization MUST grant only the minimum governed action needed for the
approved resource and scope.

## 29. Cross-Client Isolation

Authorization MUST prohibit any path that could substitute:

```text
Client A resource
for
Client B request
```

Authorization MUST NOT leak across unauthorized client boundaries:

- reports
- dashboard data
- EIP artifacts
- Assessment outputs
- engagement evidence
- AI context

Denial behavior MUST avoid confirming another client's resource existence,
identifiers, engagement status, workspace structure, projection metadata, or
artifact metadata.

## 30. Implementation Prerequisites

Before authorization implementation may be approved, the following decisions
remain unresolved:

1. stable principal mapping authority
2. membership authority source
3. entitlement authority source
4. client / organization identity model
5. engagement identity and scope model
6. workspace model if required
7. governed resource identity model
8. requested-action model
9. authority administration model
10. revocation semantics
11. persistence mechanism
12. API/service contract
13. audit and observability implementation
14. security and IAM boundary
15. EIP resource lookup integration
16. Website request and delivery integration
17. deterministic route isolation

This document does not resolve those implementation prerequisites.

## 31. Implementation Gate

THIS AUTHORITY MODEL DOES NOT AUTHORIZE IMPLEMENTATION.

It does not authorize:

- source-code changes
- authorization code
- membership code
- entitlement code
- principal mapping implementation
- API creation
- endpoint creation
- Lambda changes
- API Gateway changes
- Cognito changes
- Cognito groups
- custom claims
- IAM changes
- DynamoDB
- S3
- SQL
- persistence
- EIP integration
- Website changes
- Assessment Service changes
- Bedrock changes
- AI changes
- deployment

No implementation may begin from this authority model alone.

## 32. Acceptance Criteria

This artifact passes only if:

- principal is clearly defined
- authentication is not authorization
- membership is clearly defined
- membership is not entitlement
- entitlement is clearly defined
- client isolation is explicit
- engagement scope is explicit
- workspace treatment is explicit
- resource authorization is explicit
- ALLOW semantics are deterministic
- default is DENY
- fail-closed behavior is explicit
- browser identifiers are non-authoritative
- AI cannot authorize
- Assessment Service authority is preserved
- EIP authority is preserved
- Website remains presentation-only
- trusted runtime ownership is preserved
- authority sources are not invented
- persistence remains unselected
- implementation remains unauthorized
