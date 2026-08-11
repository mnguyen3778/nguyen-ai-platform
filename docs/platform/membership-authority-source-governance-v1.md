# Membership Authority Source Governance v1

## 1. Purpose and Scope

This document governs the authority-source semantics for Nguyen AI membership.

The purpose is narrow:

- define Membership as the authoritative relationship between a stable Nguyen
  AI Principal and a Governed Business Entity;
- define what future membership authority must prove before membership can be
  treated as current and valid;
- preserve the distinction between membership, entitlement, engagement scope,
  workspace scope, resource access, and requested action permission;
- document current evidence without inventing a concrete membership authority
  source.

This document is governance only. It does not implement membership, create
membership records, select persistence, define schemas, define APIs, define
endpoints, modify Cognito, create groups or custom claims, implement
entitlement, implement authorization, modify runtime repositories, modify
producer repositories, modify Website behavior, modify AI behavior, or
authorize deployment.

## 2. Governance Status and Authority

Governance owner:

- `nguyen-ai-platform`

Governed increment:

- Membership Authority Source Governance v1

Version:

- v1

This document is governed by:

- [Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md)
- [EIP Governed Retrieval Boundary v1](eip-governed-retrieval-boundary-v1.md)
- [Runtime Owner Assignment Governance v1](runtime-owner-assignment-governance-v1.md)
- [Principal / Membership / Entitlement Authority Model v1](principal-membership-entitlement-authority-model-v1.md)
- [Stable Principal Mapping Authority Governance v1](stable-principal-mapping-authority-governance-v1.md)
- [Client / Organization Identity Authority Governance v1](client-organization-identity-authority-governance-v1.md)

This document does not supersede approved Platform architecture, repository
ownership, integration governance, cross-repository contract governance,
producer/consumer boundaries, principal mapping governance, Client /
Organization identity governance, or authorization governance.

## 3. Architectural Context

Approved authorization governance establishes this chain:

```text
trusted authentication evidence
        |
        v
stable Nguyen AI principal
        |
        v
Governed Business Entity
        |
        v
authoritative membership
        |
        v
engagement / workspace scope where applicable
        |
        v
governed resource identity
        |
        v
requested action
        |
        v
authoritative entitlement
        |
        v
ALLOW / DENY
```

Stable Principal Mapping Authority Governance v1 governs the actor concept and
principal mapping semantics.

Client / Organization Identity Authority Governance v1 governs the conceptual
business identity target for membership.

This document governs the relationship authority required between those two
governed concepts.

Authentication is not authorization.

Principal mapping is not membership.

Membership is not entitlement.

Retrieval is not authorization.

Resource association is not principal access.

## 4. Evidence Basis

Current repository evidence was inspected only to classify existing concepts.

Platform evidence:

- Platform governance defines membership conceptually as the relationship
  between a principal and a client / organization context.
- Platform governance now defines stable principal semantics and Governed
  Business Entity semantics.
- Platform governance does not approve a concrete membership authority source.

AWS AI Knowledge Assistant evidence:

- Cognito User Pool, App Client, API Gateway Cognito authorizer, token-based
  authentication evidence, Lambda routing, deterministic runtime provider
  support, Bedrock paths, IAM execution roles, and DynamoDB conversation
  history evidence exist.
- Assistant message `role` fields are assistant contract data.
- IAM roles are infrastructure permission evidence.
- DynamoDB conversation `UserId` evidence is conversation-history persistence.
- No approved membership authority, membership lifecycle authority,
  principal-to-business-entity membership record, entitlement authority, or
  governed-resource authorization authority exists.

Website evidence:

- Website Cognito configuration, AuthProvider, access-token acquisition,
  authenticated portal routes, Website Projection Delivery client behavior,
  dashboard rendering, and Website-local tenancy/security documents exist.
- Website-local tenancy/security documents are documentation evidence only for
  this Platform governance review.
- Browser state, route state, delivery view-model groups, and requested
  context values are presentation or request context.
- No browser-side or Website-side value is authoritative membership state.

Assessment Service evidence:

- Assessment `organization`, `respondent`, `requestId`, assessment version,
  `BusinessDecisionPackage`, `ExecutiveAssessmentSnapshot`, and lineage
  evidence exist.
- Those concepts are assessment input, deterministic business-truth,
  runtime-context, package, snapshot, or producer lineage evidence.
- Question-to-dimension membership in methodology documents is methodology
  configuration, not principal membership.
- No Assessment Service evidence establishes principal-to-business-entity
  membership authority.

EIP evidence:

- EIP package identity, projection identity, publication, freshness,
  classification, compatibility, `authorizationScopeState`, Website Projection
  Delivery Contract, and lineage evidence exist.
- Those concepts are producer metadata, delivery eligibility, resource
  identity, or lineage evidence.
- EIP metadata does not establish principal membership, entitlement, or
  business identity authority.

Field existence, documentation existence, UI state, producer metadata, and
authenticated session state do not establish membership authority.

## 5. Terminology

Stable Nguyen AI Principal:

- the governed authorization actor concept established by Stable Principal
  Mapping Authority Governance v1.

Governed Business Entity:

- the stable business identity concept established by Client / Organization
  Identity Authority Governance v1 as the top-level target for future
  membership and authorization scope.

Membership:

- the authoritative relationship indicating that a stable Nguyen AI Principal
  is recognized as belonging to or acting within a Governed Business Entity
  context.

Membership Authority Source:

- the future approved authority permitted to establish current membership
  truth.

Membership Persistence:

- the future storage or representation mechanism, if any, used to hold or
  retrieve membership state.

Entitlement:

- downstream permission to perform an approved action against an approved
  governed scope or resource.

## 6. Membership Definition

Membership is the authoritative relationship between:

```text
stable Nguyen AI Principal
+
Governed Business Entity
```

Membership answers:

```text
Does Principal P have an authoritative relationship with Governed Business
Entity B?
```

Membership MUST be current, deterministic, server-authoritative, auditable,
and fail-closed.

Membership MUST NOT be inferred from:

- authentication alone;
- principal existence alone;
- business entity existence alone;
- email address;
- email domain;
- username;
- Cognito user state;
- Cognito group state;
- custom claims;
- browser state;
- Assessment Service input;
- EIP lineage;
- AI inference.

## 7. Membership Authority Source Concept

A Membership Authority Source is the future approved authority that may
establish whether a membership relationship is valid at the time of
authorization evaluation.

This document governs authority-source requirements. It does not select the
concrete source.

The concrete Membership Authority Source is:

- UNRESOLVED

No current repository evidence justifies selecting a repository, database,
identity provider, token claim, group, custom claim, administrative system,
configuration file, or external system as the concrete source of membership
truth.

## 8. Authority Source Requirements

A future Membership Authority Source MUST be capable of:

- resolving membership for a stable Nguyen AI Principal and a Governed
  Business Entity;
- distinguishing active/current membership from missing, inactive, disabled,
  revoked, expired, terminated, ambiguous, conflicting, malformed, stale,
  unavailable, unknown, or unsupported membership state;
- supporting deterministic server-side evaluation;
- supporting fail-closed behavior;
- supporting audit evidence sufficient to explain membership resolution;
- preserving revocation semantics;
- remaining independent of browser assertion;
- remaining independent of AI inference;
- remaining separate from entitlement, action permission, and resource access.

A future Membership Authority Source MUST NOT depend on:

- LLM output;
- browser-selected context;
- email/domain matching;
- previous successful access;
- cached presentation state;
- producer metadata alone;
- retrieval success alone.

## 9. Membership Resolution Model

Conceptual membership resolution evaluates:

```text
verified Nguyen AI Principal
+
Governed Business Entity
+
authoritative membership state
->
ACTIVE MEMBERSHIP / NO MEMBERSHIP / DENY
```

The governed outcomes are:

- ACTIVE MEMBERSHIP: exactly one current valid authoritative relationship is
  established.
- NO MEMBERSHIP: no authoritative relationship exists.
- INVALID MEMBERSHIP: a relationship exists but is inactive, disabled,
  revoked, expired, terminated, malformed, stale where current validity is
  required, or otherwise unsupported.
- AMBIGUOUS MEMBERSHIP: membership evidence is conflicting or resolves to more
  than one incompatible relationship.
- AUTHORITY UNAVAILABLE: required membership authority cannot be reached or
  trusted.

Only ACTIVE MEMBERSHIP may proceed to later entitlement evaluation.

All other outcomes grant no protected business scope.

These are governance semantics, not runtime enums or schema values.

## 10. Active Membership

Membership may be considered active only when all required authority proves:

- the Nguyen AI Principal resolves validly;
- the Governed Business Entity resolves validly;
- exactly one authoritative membership relationship is established for the
  requested principal and business entity context;
- the relationship is active/current;
- the relationship is not disabled;
- the relationship is not revoked;
- the relationship is not expired where expiration applies;
- the relationship is not terminated;
- the relationship is not stale where current validity is required;
- the authority state is available and trustworthy.

Active membership is a prerequisite to later entitlement evaluation. It is not
itself entitlement.

## 11. Absent Membership

No membership relationship means the principal has no authoritative membership
in the requested Governed Business Entity context.

Absent membership MUST NOT become:

- guest membership;
- trial membership;
- default membership;
- implicit membership;
- organization-wide entitlement;
- prior membership;
- public resource permission;
- cross-client membership.

For protected governed resources, absent membership requires DENY unless a
future separately governed public capability explicitly permits access outside
membership.

This document does not approve such a public capability.

## 12. Invalid Lifecycle States

Future membership governance and implementation must preserve lifecycle
semantics sufficient to deny invalid authority.

Conceptual membership lifecycle states may include:

- active;
- inactive;
- disabled;
- revoked;
- expired where applicable;
- terminated where appropriate;
- unknown;
- unavailable;
- malformed;
- conflicting;
- stale where current validity is required.

This document does not require these exact implementation labels.

The invariant is:

```text
anything other than currently valid authoritative membership
does not grant protected business scope
```

## 13. Revocation Semantics

Revoked membership no longer establishes business relationship authority.

Revocation MUST fail closed.

Revoked membership MUST NOT be restored by:

- stale prior state;
- browser/session cache;
- previous successful access;
- token validity alone;
- Cognito authentication alone;
- Cognito groups;
- custom claims;
- email/domain matching;
- Assessment organization text;
- EIP lineage;
- AI inference.

This document does not design an administration UI, workflow engine, API,
database, event propagation, cache invalidation behavior, session invalidation
behavior, or revocation service.

Broader Authority Administration / Revocation Governance remains a future
bounded governance decision.

## 14. Principal Boundary

Principal mapping is not membership.

Stable Principal Mapping Authority Governance v1 governs the actor concept and
principal mapping semantics. This document assumes that a valid Nguyen AI
Principal has already been resolved when membership is evaluated.

Principal existence MUST NOT imply:

- membership;
- business entity access;
- engagement access;
- workspace access;
- resource access;
- action permission;
- entitlement.

Principal Mapping Authority Source remains unresolved and is not selected by
this document.

## 15. Governed Business Entity Boundary

Membership attaches conceptually to a Governed Business Entity.

Client / Organization Identity Authority Governance v1 governs Client and
Organization as related but not automatically equivalent concepts and defines
the Governed Business Entity as the top-level business identity target for
future membership.

This document does not decide:

- whether every Client equals exactly one Organization;
- whether one Client may represent multiple Organizations;
- whether one Organization may participate in multiple Client relationships;
- the concrete Client / Organization authority source;
- business identity persistence;
- business identity provisioning.

Business entity existence alone does not grant membership.

## 16. Multiplicity

The architecture MUST be capable of supporting:

- one Principal with zero memberships;
- one Principal with one membership;
- one Principal with multiple memberships;
- one Governed Business Entity with zero member Principals;
- one Governed Business Entity with one member Principal;
- one Governed Business Entity with multiple member Principals.

Membership in Governed Business Entity A MUST NOT imply membership in
Governed Business Entity B.

Multiplicity is conceptual governance only. This document does not create
membership records, account-linking rules, administrative workflows, or
storage models.

## 17. Authentication / Cognito Boundary

Successful authentication does not establish membership.

Successful Cognito authentication does not establish membership.

The following MUST NOT be authoritative membership by default:

- Cognito user;
- `sub`;
- username;
- email;
- verified email;
- group;
- custom claim;
- token role;
- domain;
- token possession;
- session possession.

These may be authentication evidence or request context only unless a future
approved governance artifact explicitly grants them membership-authority
status.

## 18. Email / Domain Boundary

Email address alone MUST NOT establish membership.

Verified email alone MUST NOT establish membership.

Email domain alone MUST NOT establish membership.

Organization domain alone MUST NOT establish membership.

Username or display name alone MUST NOT establish membership.

Example:

```text
user@example-company.com
```

does not establish membership in Example Company.

Email/domain matching MUST NOT be used as fallback membership resolution.

## 19. Client / Organization Boundary

Client and Organization are related but not automatically equivalent.

Membership attaches to the Governed Business Entity concept approved by Client
/ Organization Identity Authority Governance v1.

This document MUST NOT be read to silently collapse Client and Organization
for implementation.

This document MUST NOT select the Client / Organization authority source.

No browser-supplied client, organization, or tenant value establishes
membership.

## 20. Engagement Boundary

Engagement does not need to precede membership governance.

Engagement remains downstream authorization scope.

Membership in a Governed Business Entity MUST NOT automatically grant:

- engagement access;
- engagement administration;
- engagement evidence access;
- engagement assessment access;
- engagement report access;
- engagement resource access.

Engagement identity, engagement lifecycle, and engagement authorization remain
future bounded governance decisions.

## 21. Workspace Boundary

Membership MUST NOT automatically grant workspace access.

Workspace remains:

- PARTIALLY GOVERNED / UNRESOLVED

Workspace may be an operational, isolation, portal, or resource boundary where
applicable, but this document does not require every engagement to have a
workspace.

Workspace identity, workspace lifecycle, and workspace authorization remain
future bounded governance decisions.

## 22. Resource Boundary

Membership MUST NOT automatically grant access to:

- assessments;
- evidence;
- `BusinessDecisionPackage`;
- `ExecutiveAssessmentSnapshot`;
- `ExecutiveIntelligencePackage`;
- projections;
- Website Projection Delivery Contracts;
- reports;
- AI context;
- downloads;
- dashboards;
- other governed resources.

Membership is not resource entitlement.

Resource identity, resource lookup, resource association, and resource
authorization remain downstream governance decisions.

## 23. Action / Permission Boundary

Membership MUST NOT imply permission to:

- view;
- retrieve;
- download;
- upload;
- manage;
- administer;
- explain;
- modify;
- publish;
- revoke;
- perform any other governed action.

Requested Action / Permission Vocabulary remains unresolved.

This document does not create roles, permissions, action names, role matrices,
or permission inheritance.

## 24. Entitlement Boundary

Membership is not entitlement.

Membership answers:

```text
Does Principal P have an authoritative relationship with Governed Business
Entity B?
```

Entitlement later answers:

```text
May Principal P perform Action A against governed Scope or Resource R?
```

This document does not implement entitlement, define entitlement rules, select
entitlement authority, define permission inheritance, or authorize any
resource action.

## 25. Assessment Service Boundary

The Assessment Service remains the sole deterministic assessment
business-truth producer.

Assessment Service evidence includes:

- `organization`;
- `respondent`;
- `requestId`;
- assessment identity;
- assessment version;
- `BusinessDecisionPackage`;
- `ExecutiveAssessmentSnapshot`;
- lineage.

Those values are assessment input, business data, deterministic truth,
runtime-context, provenance, or lineage evidence. They MUST NOT establish
membership.

Assessment input, assessment business truth, and Assessment Service provenance
are not membership authority.

## 26. EIP Boundary

The Executive Intelligence Platform remains the producer of governed executive
intelligence and Website Projection Delivery Contracts.

EIP evidence includes:

- lineage;
- projection identity;
- package identity;
- publication;
- freshness;
- classification;
- compatibility;
- `authorizationScopeState`;
- delivery contract state.

Those values are producer metadata, resource identity, publication state,
delivery eligibility, or lineage evidence. They MUST NOT establish membership.

Producer metadata is not membership authority.

## 27. Website / Browser Boundary

The Website remains presentation-only.

Browser-supplied values MUST NOT establish authoritative membership,
including:

- principal ID;
- client ID;
- organization ID;
- tenant ID;
- engagement ID;
- workspace ID;
- membership flag;
- role;
- email;
- resource ID;
- report ID;
- projection ID;
- delivery ID;
- route state;
- browser storage;
- dashboard state.

Browser state may request context only.

The Website may render authorized results after a trusted server-side boundary
has resolved principal, business entity, membership, entitlement, scope,
resource, and action where required by approved governance.

## 28. Trusted Runtime Boundary

Runtime Owner Assignment Governance v1 assigns:

```text
aws-ai-knowledge-assistant
```

as the repository ownership domain for a future separate deterministic trusted
logical service.

Repository ownership is not membership authority.

The future deterministic trusted logical service may later evaluate membership
only after:

- membership authority-source governance is approved;
- any required authority source, persistence, contract, security, and
  implementation governance is approved;
- implementation is explicitly authorized.

This document does not implement that service and does not make the AI
Knowledge Assistant the membership authority.

## 29. AI / Bedrock / Model Authority Boundary

AI, Bedrock, LLMs, RAG, and the AI Knowledge Assistant MUST NOT:

- infer membership;
- create membership;
- repair membership;
- merge membership;
- revoke membership;
- restore membership;
- select membership authority;
- resolve ambiguous membership;
- override deterministic membership state;
- make membership-based ALLOW decisions;
- infer entitlement from membership;
- fabricate missing membership authority.

AI remains a downstream consumer or explainer only after deterministic
authorization succeeds and a separately approved consumer boundary permits use
of authorized governed context.

## 30. Conflict and Ambiguity

Membership resolution MUST fail closed when:

- multiple sources conflict;
- multiple relationships conflict;
- principal identity cannot be resolved;
- business entity identity cannot be resolved;
- membership authority is unavailable;
- membership state is stale where current validity is required;
- membership state is malformed;
- membership state is ambiguous;
- lifecycle state is unknown;
- authority source status is unsupported.

The system MUST NOT pick the most likely membership.

The system MUST NOT use AI inference to resolve ambiguity.

The outcome MUST grant no protected business scope.

## 31. Membership Authority vs Persistence

Membership Authority Source and Membership Persistence are separate decisions.

Membership Authority Source answers:

```text
What trusted authority is permitted to establish membership truth?
```

Membership Persistence answers:

```text
Where or how is membership state stored, represented, cached, or retrieved?
```

This document does not select persistence.

Membership persistence remains:

- UNRESOLVED

This document does not select DynamoDB, S3, SQL, filesystem, Cognito, external
database, CRM, configuration files, cache, queue, event bus, or any other
store.

## 32. Membership Authority vs Administration

Membership authority and membership administration are separate decisions.

Membership authority determines what establishes membership truth.

Membership administration determines who or what may create, update, disable,
revoke, expire, terminate, review, or audit membership authority.

This document governs membership lifecycle and revocation semantics
conceptually.

This document does not implement or fully select:

- administrator roles;
- invitation workflows;
- approval workflows;
- account provisioning;
- organization administrator model;
- client administrator model;
- membership management UI;
- membership APIs;
- operational runbooks.

Broader administration governance remains a future bounded governance
decision.

## 33. Principal Mapping Authority Source Boundary

Stable principal semantics are governed.

Principal Mapping Authority Source remains:

- UNRESOLVED

This document does not solve principal mapping authority source, principal
persistence, principal provisioning, account linking, or identity-provider
migration.

Membership governance may depend conceptually on a valid resolved Nguyen AI
Principal without selecting how principal mappings are stored, administered,
or implemented.

## 34. Client / Organization Authority Source Boundary

Governed Business Entity semantics are governed conceptually.

Client / Organization Authority Source remains:

- UNRESOLVED

This document does not solve Client / Organization identity authority source,
business identity persistence, business identity provisioning, merge/split
administration, aliasing, or Client / Organization implementation
representation.

Membership governance may depend conceptually on a valid resolved Governed
Business Entity without selecting its persistence or provisioning authority.

## 35. Audit and Privacy Governance

Future membership resolution must be auditable without collecting unnecessary
personal or business data.

Conceptual audit evidence should include:

- timestamp;
- Principal reference;
- Governed Business Entity reference;
- membership resolution outcome;
- membership lifecycle or state classification;
- authority/version reference where applicable;
- reason classification;
- correlation or request identifier.

Audit records MUST NOT require:

- raw access tokens;
- raw ID tokens;
- secrets;
- credentials;
- unnecessary claims;
- unnecessary profile data;
- unnecessary respondent data;
- unnecessary Assessment Service payloads;
- unnecessary EIP internals.

This document does not select audit persistence, logging technology,
telemetry, retention, schema, event transport, or monitoring implementation.

## 36. Fail-Closed Semantics

Membership resolution MUST fail closed for at least:

- missing Principal;
- invalid Principal;
- unmapped Principal;
- disabled Principal;
- revoked Principal;
- missing business entity;
- invalid business entity;
- inactive business entity where applicable;
- missing membership;
- inactive membership;
- disabled membership;
- revoked membership;
- expired membership;
- terminated membership;
- ambiguous membership;
- conflicting membership;
- stale membership where current validity is required;
- malformed membership;
- authority unavailable;
- unsupported authority state;
- unknown membership state.

No fallback may use:

- previous client;
- previous organization;
- browser selection;
- cached browser state;
- default tenant;
- email/domain matching;
- Cognito group;
- custom claim;
- Assessment organization;
- EIP lineage;
- prior membership;
- AI inference.

Anything other than current valid authoritative membership grants no protected
business scope.

## 37. Authority Status Matrix

| Area | Status | Governance meaning |
| --- | --- | --- |
| Stable principal concept | GOVERNED | Stable Principal Mapping Authority Governance v1 defines the actor concept. |
| Principal mapping semantics | GOVERNED | Principal mapping semantics are governed; implementation is not authorized. |
| Principal mapping authority source | UNRESOLVED | No approved source currently establishes principal mappings. |
| Governed Business Entity concept | GOVERNED CONCEPTUALLY | Client / Organization Identity Authority Governance v1 defines the top-level business identity target. |
| Client / Organization authority source | UNRESOLVED | No approved source currently establishes authoritative business identity. |
| Membership semantics | GOVERNED CONCEPTUALLY | PME v1 defines membership as principal plus client / organization context. |
| Membership authority-source requirements | GOVERNED | This document defines what a future membership authority source must prove. |
| Concrete membership authority source | UNRESOLVED | No concrete repository, service, store, identity provider, or administrative system is selected. |
| Membership persistence | UNRESOLVED | No storage or persistence mechanism is selected. |
| Membership administration | PARTIALLY GOVERNED / UNRESOLVED | Lifecycle and revocation semantics are governed conceptually; administration mechanisms remain unresolved. |
| Membership revocation semantics | GOVERNED CONCEPTUALLY | Revoked membership must fail closed and must not grant scope. |
| Engagement identity / scope | PARTIALLY GOVERNED / UNRESOLVED | Engagement remains downstream scope; authority source remains unresolved. |
| Workspace identity / scope | PARTIALLY GOVERNED / UNRESOLVED | Workspace remains possible scope; authority source remains unresolved. |
| Resource identity / lookup | PARTIALLY GOVERNED / UNRESOLVED | Producer artifacts exist; runtime lookup and authorization identity remain unresolved. |
| Requested action vocabulary | UNRESOLVED | No governed action vocabulary is selected. |
| Entitlement authority | UNRESOLVED | No approved source currently establishes entitlement. |
| Authorization persistence | UNRESOLVED | No authorization storage mechanism is selected. |
| Trusted authorization service contract | UNRESOLVED | No service contract, API, or endpoint is approved. |

This matrix must not be read as implementation approval.

## 38. Unresolved Decisions and Future Governance

The following remain unresolved:

- concrete membership authority source;
- membership persistence;
- membership administration model;
- membership provisioning;
- membership invitation or onboarding workflows;
- membership administration roles;
- principal mapping authority source;
- principal persistence and provisioning;
- Client / Organization authority source;
- business identity persistence and provisioning;
- engagement identity and lifecycle;
- workspace identity and lifecycle;
- governed resource identity and lookup;
- requested action vocabulary;
- entitlement authority source;
- broader authority administration and revocation governance;
- authorization persistence;
- trusted authorization service contract;
- EIP retrieval integration;
- Website authorized delivery integration;
- audit and observability implementation;
- security and IAM boundary;
- deterministic route isolation.

Each unresolved item requires separate approved governance before
implementation may begin.

## 39. Implementation Prerequisites

Before membership authority can support authorization implementation, future
governance must approve at least:

1. concrete membership authority source or approved authority-source mechanism;
2. membership persistence if persisted state is required;
3. membership administration and revocation mechanism;
4. principal mapping authority source sufficient for runtime implementation;
5. Client / Organization authority source sufficient for runtime
   implementation;
6. engagement identity and scope model;
7. workspace identity and scope model where applicable;
8. governed resource identity and lookup model;
9. requested action vocabulary;
10. entitlement authority source;
11. trusted authorization service contract;
12. audit and observability model;
13. security and IAM boundary;
14. deterministic route isolation;
15. EIP retrieval integration;
16. Website authorized delivery integration;
17. explicit implementation approval.

This prerequisite list does not authorize implementation.

## 40. Technology Neutrality

This document does not select:

- DynamoDB;
- S3;
- SQL;
- filesystem;
- Cognito groups;
- custom claims;
- IAM identities;
- RBAC;
- ABAC;
- ACL;
- policy engine;
- CRM;
- external identity database;
- schema;
- API;
- endpoint;
- persistence mechanism;
- cache;
- queue;
- event bus.

Existing technology may be referenced only as repository evidence,
architectural constraint, or explicitly unselected option.

No existing DynamoDB, Cognito, API Gateway, Lambda, Website, Assessment
Service, EIP, IAM, or AI capability becomes membership authority through this
document.

## 41. Implementation Gate

MEMBERSHIP AUTHORITY SOURCE GOVERNANCE v1 DOES NOT AUTHORIZE IMPLEMENTATION.

It does not authorize:

- membership implementation;
- membership persistence;
- membership records;
- membership provisioning;
- membership administration;
- principal mapping implementation;
- client identity implementation;
- organization identity implementation;
- entitlement;
- authorization runtime;
- engagement authorization;
- workspace authorization;
- resource authorization;
- requested action permissions;
- schemas;
- APIs;
- endpoints;
- Cognito changes;
- Cognito groups;
- custom claims;
- IAM changes;
- infrastructure changes;
- Assessment Service changes;
- EIP changes;
- Website changes;
- AWS runtime changes;
- Bedrock changes;
- AI changes;
- deployment.

Any implementation requires separate architecture approval, governance
approval, owning-repository approval, implementation plan, and explicit
authorization.

## 42. Acceptance Criteria

This artifact is acceptable only if:

- Membership is defined as the relationship between a stable Nguyen AI
  Principal and a Governed Business Entity;
- principal existence and membership existence remain distinct;
- principal mapping remains separate from membership;
- Client / Organization authority source remains unresolved;
- concrete membership authority source remains unresolved unless separately
  approved by objective evidence;
- membership authority is separated from persistence;
- membership authority is separated from administration;
- active membership conditions are explicit;
- absent, inactive, disabled, revoked, expired, terminated, ambiguous,
  conflicting, stale, malformed, unavailable, and unknown membership states
  fail closed;
- revocation semantics are explicit;
- authentication and Cognito do not establish membership;
- email and domain do not establish membership;
- browser values remain non-authoritative;
- Assessment Service data is not membership authority;
- EIP metadata is not membership authority;
- membership does not grant engagement, workspace, resource, action, or
  entitlement access;
- AI has no membership authority;
- producer and consumer boundaries remain intact;
- no technology or persistence mechanism is selected;
- implementation remains unauthorized.
