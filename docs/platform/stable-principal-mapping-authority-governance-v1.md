# Stable Principal Mapping Authority Governance v1

## 1. Purpose and Scope

This document defines the governance semantics by which trusted authentication
evidence may be associated with a stable Nguyen AI principal for future
deterministic authorization.

The purpose is narrow:

- define what a Nguyen AI principal means for authorization;
- define how verified authentication evidence may resolve to that principal;
- define fail-closed behavior for unmapped, ambiguous, disabled, revoked, or
  unavailable principal state;
- preserve the boundary between authentication, principal mapping, membership,
  entitlement, retrieval, and delivery.

This document is governance only. It does not implement principal mapping,
select persistence, create schemas, define APIs, create endpoints, modify
Cognito, modify Lambda, modify API Gateway, modify IAM, modify the Website,
modify the Assessment Service, modify the Executive Intelligence Platform,
modify the AI Knowledge Assistant, modify Bedrock, or authorize deployment.

## 2. Governance Status and Authority

Governance owner:

- `nguyen-ai-platform`

Governed increment:

- Stable Principal Mapping Authority Governance v1

This document resolves the principal mapping semantics identified as
unresolved by
[Principal / Membership / Entitlement Authority Model v1](principal-membership-entitlement-authority-model-v1.md).

This document does not supersede:

- [Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md)
- [EIP Governed Retrieval Boundary v1](eip-governed-retrieval-boundary-v1.md)
- [Runtime Owner Assignment Governance v1](runtime-owner-assignment-governance-v1.md)
- [Principal / Membership / Entitlement Authority Model v1](principal-membership-entitlement-authority-model-v1.md)

This document is subordinate to approved Platform architecture, repository
ownership, integration, repository governance, and cross-repository contract
governance.

## 3. Architectural Context

Approved authorization governance establishes the following chain:

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
governed resource / action
        |
        v
ALLOW / DENY
```

This document governs only the transition from verified authentication evidence
to verified principal.

Current repository evidence includes:

- Cognito User Pool, App Client, email sign-in, JWT issuance, and API Gateway
  Cognito authorizer evidence in `/Users/aiadmin/aws-ai-knowledge-assistant`;
- trusted server-side Lambda execution evidence in
  `/Users/aiadmin/aws-ai-knowledge-assistant`;
- Website-side Cognito configuration, AuthProvider session handling, access
  token acquisition, and bearer-token delivery requests in
  `/Users/aiadmin/projects/nguyen-ai-website`;
- no approved Nguyen AI principal mapping authority source;
- no approved membership authority source;
- no approved entitlement authority source.

Authentication evidence exists. Nguyen AI business-resource authorization does
not automatically follow from that evidence.

## 4. Problem Statement

The Platform must know which stable Nguyen AI authorization subject is making a
request before membership or entitlement can be evaluated.

Current Cognito evidence can prove that an external identity provider
authenticated a subject after trusted server-side verification. It does not by
itself define:

- the canonical Nguyen AI principal;
- whether the external subject is mapped to a Nguyen AI principal;
- whether the mapped principal is active;
- whether the mapped principal belongs to any client or organization;
- whether the mapped principal is entitled to any governed resource.

Without governed principal mapping semantics, later membership, entitlement,
audit, revocation, service contract, persistence, and implementation decisions
would either invent an actor identity implicitly or treat authentication as
authorization.

## 5. Definitions

Authentication evidence:

- trusted evidence that an approved identity provider authenticated a subject.

External authenticated identity:

- the provider-issued identity attributes or subject references obtained from
  server-verified authentication evidence.

Nguyen AI Principal:

- the stable governed authorization subject used by Nguyen AI to evaluate
  future membership and entitlement relationships.

Principal mapping:

- the deterministic server-side resolution of verified authentication evidence
  to exactly one valid Nguyen AI principal.

Mapped principal:

- the result when sufficient trusted authority exists to associate verified
  authentication evidence with exactly one active Nguyen AI principal.

Unmapped principal:

- the result when authentication evidence is valid but no authoritative Nguyen
  AI principal mapping exists.

Ambiguous mapping:

- any condition in which authentication evidence cannot resolve to exactly one
  active Nguyen AI principal.

Principal mapping authority:

- the future approved authority source or process that establishes mappings.
  This v1 document governs required semantics but does not select the source,
  storage, process, schema, API, or implementation.

## 6. Authentication Evidence

Authentication evidence may establish that a trusted identity provider
authenticated a subject.

Current evidence shows Cognito authentication capabilities, including a User
Pool, App Client, JWT issuance, email sign-in, and API Gateway Cognito
authorizer behavior.

Authentication evidence MUST be verified by a trusted server-side boundary
before it can be used for principal mapping.

Authentication evidence alone MUST NOT establish:

- client membership;
- organization membership;
- engagement membership;
- workspace membership;
- entitlement;
- governed resource access;
- role authority;
- business-resource authorization.

Authentication is not authorization.

## 7. Nguyen AI Principal

A Nguyen AI Principal is the stable authorization subject against which future
deterministic authorization decisions are evaluated.

A Nguyen AI Principal MUST be:

- stable within the governed Nguyen AI identity domain;
- unique for authorization evaluation within that domain;
- resolved server-side from trusted authority;
- auditable without storing raw authentication tokens;
- independent from browser assertions;
- suitable as the subject of future membership relationships;
- suitable as the subject of future entitlement relationships.

This document does not define:

- database schema;
- identifier format;
- UUID format;
- table structure;
- storage location;
- API representation;
- provisioning workflow;
- account linking workflow.

## 8. External Identity vs Nguyen AI Principal

External authenticated identity and Nguyen AI Principal are distinct concepts.

External identity evidence may include provider-issued attributes or references
such as:

- provider subject identifiers;
- username;
- email;
- verified email indicator;
- provider groups;
- custom claims.

Those values may be evidence considered by a future governed mapping authority.
They are not automatically the canonical Nguyen AI Principal.

This document does not declare any existing Cognito claim, username, email
address, group, custom claim, or IAM identity to be the canonical Nguyen AI
Principal.

Future governance MAY approve a mapping model that uses a provider-specific
subject reference as an input. Such approval must preserve the distinction
between external identity evidence and the Nguyen AI Principal.

## 9. Principal Mapping Model

The governed principal mapping model is:

```text
verified authentication evidence
        |
        v
trusted principal mapping resolution
        |
        v
stable Nguyen AI Principal
```

Principal mapping resolution MUST be:

- deterministic;
- server-side;
- fail-closed;
- auditable;
- independent of AI;
- independent of browser assertion;
- independent of email-only inference;
- independent of provider group-only inference;
- independent of unapproved custom-claim inference.

This document does not define persistence, data structures, route behavior,
middleware, algorithms, cache behavior, migration mechanics, or provisioning
logic.

## 10. Mapped Principal Semantics

A mapped principal exists only when trusted principal mapping resolution
establishes exactly one valid Nguyen AI Principal for the verified
authentication evidence.

A mapped principal means:

- the authenticated external identity has been associated with one active
  Nguyen AI Principal;
- the actor identity stage of the authorization chain has succeeded;
- later membership and entitlement evaluation may proceed if separately
  governed and implemented.

A mapped principal MUST NOT imply:

- membership;
- entitlement;
- client access;
- organization access;
- engagement access;
- workspace access;
- governed resource access;
- dashboard access;
- report access;
- EIP artifact access;
- Assessment Service output access;
- AI context access.

Principal mapping answers who the actor is in the Nguyen AI authorization
domain. It does not answer what the actor may access.

## 11. Unmapped Principal Semantics

An unmapped principal condition exists when authentication evidence is valid
but no authoritative Nguyen AI principal mapping is established.

Unmapped principal state MUST fail closed for governed-resource authorization.

No automatic mapping may occur from:

- email;
- email domain;
- username;
- browser data;
- browser principal identifier;
- client identifier;
- organization identifier;
- tenant identifier;
- prior session;
- previous principal;
- previous client;
- AI inference;
- conversational context.

This document does not design account provisioning, invite acceptance,
onboarding, identity linking, or user administration workflows.

## 12. Ambiguous and Conflicting Mapping

Only exactly one valid authoritative mapping may establish a Nguyen AI
Principal.

Principal mapping MUST fail closed when authentication evidence resolves to:

- zero principals;
- multiple principals;
- conflicting mappings;
- stale mappings where current validity is required;
- disabled mappings;
- revoked mappings;
- unsupported provider state;
- malformed trusted identity evidence;
- unavailable mapping authority.

Ambiguity MUST NOT be resolved by:

- email matching;
- username matching;
- domain matching;
- browser selection;
- previous successful access;
- default principal selection;
- first-match selection;
- AI inference;
- manual operator assumption outside separately governed authority.

## 13. Principal Stability

Nguyen AI Principal identity MUST remain stable across ordinary non-authority
changes such as:

- email changes;
- display-name changes;
- browser sessions;
- access-token refresh;
- non-authoritative profile changes.

External identity lifecycle changes MUST NOT silently create a new Nguyen AI
Principal or merge existing Nguyen AI Principals without separately governed
authority.

Principal stability is required so future membership, entitlement, audit,
revocation, and resource access decisions remain traceable to the same
governed actor identity.

This document does not assume identity-provider migration behavior and does
not design migration mechanics.

## 14. Principal Uniqueness and Identity Linking Boundary

Principal mapping MUST NOT ambiguously bind one authenticated external identity
to multiple active Nguyen AI Principals for the same governed identity context.

Multiple external authenticated identities MAY conceptually map to one Nguyen
AI Principal only if separately governed identity-linking semantics approve
that behavior.

This document does not authorize:

- account linking;
- account merging;
- account splitting;
- provider migration;
- duplicate principal reconciliation;
- aliasing rules.

Identity linking remains unresolved future governance.

## 15. Principal Lifecycle

Principal lifecycle semantics are conceptual in this version.

A future governed principal authority must be capable of distinguishing
principal states such as:

- active;
- disabled;
- revoked;
- unavailable;
- unknown.

Only an active and valid principal may proceed to future membership and
entitlement evaluation.

Disabled, revoked, unavailable, unknown, malformed, or conflicting principal
authority MUST NOT result in ALLOW.

This document does not define persistence states, schema enumerations, update
mechanics, administrative workflows, or operational procedures.

## 16. Authentication Provider Lifecycle

Authentication-provider identity and Nguyen AI Principal identity are distinct.

Architecture MUST NOT permanently equate:

```text
Cognito user = Nguyen AI business principal
```

unless explicit future governance approves that equivalence with objective
evidence and preserves membership, entitlement, audit, revocation, and provider
lifecycle semantics.

The governance model SHOULD allow future identity-provider evolution without
requiring memberships and entitlements to be redefined solely because provider
implementation details change.

This document does not design identity-provider migration, token migration,
account migration, or provider federation.

## 17. Email, Username, Groups, and Claims Authority

Email address alone MUST NOT become Nguyen AI authorization authority.

Email MUST NOT automatically establish:

- Nguyen AI Principal identity;
- client membership;
- organization membership;
- entitlement;
- governed resource ownership;
- governed resource authorization.

Verified email is authentication or account evidence only. It is not automatic
Nguyen AI business-resource authority.

Username MUST NOT automatically establish Nguyen AI Principal identity,
membership, entitlement, or resource authorization.

Cognito groups, provider groups, IAM identities, roles, and custom claims are
not selected as authority mechanisms by this document.

Future groups or custom claims MUST NOT become authoritative merely because an
identity provider can technically issue them.

Any future authority use of email, username, provider groups, IAM identities,
roles, or custom claims requires explicit governance.

## 18. Membership Boundary

Principal mapping is not membership.

Principal mapping answers:

```text
Who is the authenticated actor in the Nguyen AI authorization domain?
```

Membership later answers:

```text
With which governed client or organization context does that principal have an
authoritative relationship?
```

This artifact MUST NOT define membership authority sources, membership storage,
membership lifecycle, membership administration, membership scope, or
membership implementation.

A principal MAY exist without any client or organization membership.

## 19. Entitlement Boundary

Principal mapping is not entitlement.

Principal mapping MUST NOT authorize:

- dashboard access;
- report access;
- assessment output access;
- EIP artifact access;
- AI context access;
- downloads;
- client resources;
- engagement resources;
- workspace resources;
- governed delivery.

Entitlement remains a later governance decision that depends on stable
principal identity, membership, governed scope, resource identity, and
requested action semantics.

## 20. Client / Organization Boundary

This document does not define authoritative client or organization identity.

Principal mapping is independent of client and organization authority.

A Nguyen AI Principal MAY exist without any client membership.

Possession of a client, organization, tenant, account, or company identifier
MUST NOT affect principal mapping unless separately governed trusted mapping
semantics approve that relationship.

Client / Organization Identity Authority remains a separate future governance
increment.

## 21. Engagement / Workspace / Resource Boundary

Principal mapping MUST NOT assign engagement scope, workspace scope, resource
scope, or resource entitlement.

Principal identity MUST NOT imply:

- engagement access;
- workspace access;
- resource access;
- assessment access;
- snapshot access;
- projection access;
- delivery contract access;
- report access;
- AI context access.

Engagement identity, workspace identity, governed resource identity, resource
lookup, and resource authorization remain downstream governed decisions.

## 22. Browser and Website Trust Boundary

The Website remains presentation-only.

The browser MAY hold or transmit authentication session evidence to a trusted
server-side boundary.

The browser MUST NOT authoritatively determine:

- Nguyen AI Principal identifier;
- principal mapping result;
- principal mapping status;
- membership;
- entitlement;
- client scope;
- engagement scope;
- workspace scope;
- resource access.

Any browser-supplied principal identifier, user identifier, email, role,
client identifier, engagement identifier, workspace identifier, resource
identifier, projection identifier, or delivery identifier is non-authoritative
until independently resolved by trusted server-side authority.

Website authentication state is request context. It is not business-resource
authorization.

## 23. AI / Bedrock / Model Authority Boundary

AI, Bedrock, LLMs, and RAG MUST NOT:

- create a Nguyen AI Principal;
- map authentication evidence to a Nguyen AI Principal;
- infer principal identity;
- merge principals;
- split principals;
- select among ambiguous principals;
- override unmapped state;
- override disabled state;
- override revoked state;
- repair missing mapping authority;
- infer membership;
- infer entitlement;
- authorize resources.

Principal mapping MUST remain deterministic and non-AI.

AI MAY consume already-authorized governed context only after deterministic
controls succeed and separate approved consumer governance permits that use.

## 24. Producer and Consumer Boundaries

Assessment Service remains the sole deterministic assessment business-truth
producer.

Principal mapping MUST NOT:

- score assessments;
- aggregate dimensions;
- weight dimensions;
- determine readiness;
- determine severity;
- determine risk;
- determine confidence;
- recommend;
- generate authoritative executive summaries;
- duplicate Assessment Service methodology.

The Executive Intelligence Platform remains the governed executive-intelligence
producer and the producer of `website-projection-delivery-contract-v1`.

Principal mapping MUST NOT:

- derive executive intelligence;
- modify executive intelligence;
- create delivery contracts;
- determine publication;
- determine freshness;
- alter lineage;
- determine classification.

The Website remains presentation-only.

The future deterministic trusted logical service remains the future server-side
enforcement boundary assigned to the `aws-ai-knowledge-assistant` repository
ownership domain. That logical service remains separate from the AI Knowledge
Assistant consumer and explainer capability.

Same repository does not mean same logical service. Same logical service does
not mean expanded producer authority.

## 25. Fail-Closed Semantics

Principal mapping MUST fail closed and produce no authorized principal for:

- missing authentication evidence;
- invalid authentication evidence;
- expired authentication evidence;
- unsupported authentication provider state;
- malformed trusted identity evidence;
- unmapped external identity;
- ambiguous mapping;
- conflicting mapping;
- unavailable mapping authority;
- disabled principal;
- revoked principal;
- unknown principal;
- stale mapping where current validity is required.

Fail-closed behavior MUST NOT use:

- email fallback;
- username fallback;
- domain fallback;
- provider group fallback;
- custom claim fallback;
- browser principal identifier;
- previous principal;
- previous client;
- previous successful access;
- cached presentation state;
- default principal;
- default client;
- AI inference.

When principal mapping fails closed, future governed-resource authorization
MUST remain denied unless a separately governed non-resource flow is approved.

## 26. Audit, Privacy, and Evidence Minimization

Future principal resolution MUST be auditable.

Conceptual audit evidence should include:

- timestamp;
- authentication-provider reference or class;
- non-secret external subject reference where appropriate;
- resolved principal reference if successful;
- resolution outcome;
- reason classification;
- authority or version reference where applicable;
- request or correlation identifier.

Audit evidence MUST NOT require logging:

- raw access tokens;
- raw ID tokens;
- secrets;
- credentials;
- unnecessary sensitive claims;
- unnecessary profile attributes;
- unnecessary governed payload content.

Identity evidence MUST be minimized to what is necessary for trusted principal
resolution and audit.

Email, profile data, group membership, custom claims, and other available
identity attributes MUST NOT become authorization inputs merely because they
are available.

This document does not select logging technology, audit storage, telemetry,
retention, data classification, encryption, or privacy infrastructure.

## 27. Unresolved Decisions and Future Governance

This document governs:

| Area | Status |
| --- | --- |
| Principal concept | GOVERNED |
| Principal mapping semantics | GOVERNED |
| External authentication evidence | PARTIAL CURRENT EVIDENCE |

This document does not resolve:

| Area | Status |
| --- | --- |
| Principal mapping authority source | UNRESOLVED |
| Principal persistence | UNRESOLVED |
| Principal provisioning | UNRESOLVED |
| Identity linking | UNRESOLVED |
| Membership authority | UNRESOLVED |
| Entitlement authority | UNRESOLVED |
| Client / organization identity authority | UNRESOLVED |
| Engagement identity and scope authority | UNRESOLVED |
| Workspace identity and scope authority | UNRESOLVED |
| Governed resource identity and lookup authority | UNRESOLVED |
| Requested action vocabulary | UNRESOLVED |
| Authorization persistence | UNRESOLVED |
| Trusted service API contract | UNRESOLVED |
| Principal administration and revocation mechanics | UNRESOLVED |

Future governance must define any authority source before implementation can
use principal mapping for governed-resource authorization.

This document does not fabricate authority to make principal mapping appear
implemented.

## 28. Implementation Gate and Acceptance Criteria

STABLE PRINCIPAL MAPPING AUTHORITY GOVERNANCE v1 DOES NOT AUTHORIZE
IMPLEMENTATION.

This document does not authorize:

- principal mapping code;
- principal storage;
- identity database;
- provisioning;
- account linking;
- membership;
- entitlement;
- authorization;
- schemas;
- APIs;
- endpoints;
- Lambda changes;
- API Gateway changes;
- Cognito changes;
- Cognito groups;
- custom claims;
- IAM changes;
- DynamoDB;
- S3;
- SQL;
- EIP integration;
- Website changes;
- Assessment Service changes;
- Bedrock changes;
- AI changes;
- deployment.

This governance increment passes only if it establishes:

- authentication evidence is distinct from Nguyen AI Principal identity;
- authentication is not authorization;
- the Nguyen AI Principal concept is stable, server-resolved, and auditable;
- external provider identity is not automatically the canonical Nguyen AI
  Principal;
- email is not authorization authority;
- username is not authorization authority;
- provider groups and custom claims are not selected as authority mechanisms;
- mapped principal semantics grant no membership or entitlement;
- unmapped, ambiguous, disabled, revoked, unavailable, or conflicting mapping
  fails closed;
- browser values remain non-authoritative;
- AI has no principal mapping authority;
- Assessment Service authority is preserved;
- EIP authority is preserved;
- Website remains presentation-only;
- trusted runtime ownership is preserved without implementation;
- persistence remains unselected;
- principal mapping authority source remains unresolved;
- implementation remains unauthorized.
