# Client / Organization Identity Authority Governance v1

## 1. Purpose and Scope

This document defines the governance semantics for the stable Nguyen AI
business identity to which future membership and authorization scope may
attach.

The purpose is narrow:

- distinguish client, organization, tenant, engagement, workspace, producer
  lineage, Website context, and browser-provided values;
- define the conceptual stable business identity needed before membership
  authority can be governed;
- preserve deterministic, server-side, fail-closed authorization boundaries;
- document current authority-source status without inventing an authority
  source.

This document is governance only. It does not implement client identity,
organization identity, principal-to-client mapping, membership, entitlement,
authorization, resource lookup, persistence, schemas, APIs, endpoints, Cognito
changes, infrastructure, EIP retrieval, Website behavior, Assessment Service
behavior, AI behavior, Bedrock behavior, or deployment.

## 2. Governance Status and Authority

Governance owner:

- `nguyen-ai-platform`

Governed increment:

- Client / Organization Identity Authority Governance v1

Version:

- v1

This document resolves the conceptual client / organization identity semantics
identified as unresolved by:

- [Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md)
- [Principal / Membership / Entitlement Authority Model v1](principal-membership-entitlement-authority-model-v1.md)
- [Stable Principal Mapping Authority Governance v1](stable-principal-mapping-authority-governance-v1.md)

This document does not supersede existing Platform architecture, repository
ownership, integration, repository governance, cross-repository contract
governance, producer/consumer boundaries, principal mapping governance, or
authorization governance.

## 3. Architectural Context

Approved authorization governance establishes the following conceptual chain:

```text
trusted authentication evidence
        |
        v
stable Nguyen AI principal
        |
        v
authoritative client / organization identity
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

Stable Principal Mapping Authority Governance v1 governs the actor side of
future authorization. This document governs the top-level business-identity
side of future membership scope.

Authentication is not authorization.

Principal mapping is not membership.

Membership is not entitlement.

Resource existence is not entitlement.

## 4. Evidence Basis

Current repository evidence shows business-identity terminology in several
forms:

- Platform governance uses `client`, `organization`, `engagement`, and
  `workspace` as conceptual authorization scopes.
- `/Users/aiadmin/aws-ai-knowledge-assistant` includes AWS runtime,
  authentication, Lambda, deterministic runtime, AI assistant, local
  assessment, and DynamoDB conversation-history evidence, but no approved
  client / organization identity authority.
- `/Users/aiadmin/projects/nguyen-ai-website` includes Website-side Cognito
  session handling, Website Projection Delivery consumption, portal UI,
  proposed tenancy/security documents, and client / engagement / workspace
  presentation concepts, but no approved browser-side business identity
  authority.
- `/Users/aiadmin/projects/nguyen-ai-assessment-service` includes
  `organization`, `respondent`, `requestId`, assessment version,
  `BusinessDecisionPackage`, `ExecutiveAssessmentSnapshot`, and producer
  lineage evidence, but those fields are assessment input, runtime,
  deterministic-truth, or lineage evidence rather than authorization identity
  authority.
- `/Users/aiadmin/projects/executive-intelligence-platform` includes package,
  projection, publication, classification, freshness, compatibility, lineage,
  `authorizationScopeState`, and
  `website-projection-delivery-contract-v1` evidence, but no principal
  membership or client identity authority.

Field existence, label existence, UI state, producer lineage, and authenticated
session state do not establish business identity authority.

## 5. Terminology

Nguyen AI Client:

- the governed business relationship context under which Nguyen AI may deliver
  services, governed artifacts, or portal experiences to an external business
  party.

Organization:

- the external business entity or organizational context represented in
  assessment input, commercial context, Website copy, or future governed
  records.

Governed Business Entity:

- the stable Nguyen AI business identity used as the top-level target for
  future membership and authorization scope.

Tenant:

- a term that may appear in security or isolation discussions, but is not the
  canonical business identity in this governance increment.

Engagement:

- a governed business scope subordinate to a governed business entity unless
  separately governed otherwise.

Workspace:

- an operational, isolation, or resource boundary where applicable; it is not
  automatically required for every engagement by this document.

## 6. Client Concept

A Nguyen AI Client is governed in v1 as a business relationship concept.

A Client MAY represent the commercial or service relationship through which
Nguyen AI is permitted to deliver governed work or artifacts.

A Client MUST NOT be established solely by:

- a browser-supplied `clientId`;
- a Cognito token claim;
- an email domain;
- an assessment `organization` field;
- EIP lineage;
- Website route state;
- AI inference;
- a default, previous, or cached selection.

Client identity semantics are governed by this document only at the conceptual
level. The client identity authority source remains unresolved.

## 7. Organization Concept

An Organization is governed in v1 as the external business entity or business
context that may be described by inputs, evidence, commercial records, or
future authority records.

Organization labels, names, profile fields, domain names, email domains,
assessment-provided organization objects, or Website text are not
authoritative business identity by themselves.

Organization identity semantics are governed by this document only at the
conceptual level. The organization identity authority source remains
unresolved.

## 8. Client / Organization Relationship

Current evidence does not support declaring Client and Organization to be
strict synonyms for all future governance.

For v1:

- Client is the governed relationship context.
- Organization is the external business entity or context.
- Future authorization requires a stable Governed Business Entity that can
  safely represent the top-level business scope for membership.

The Governed Business Entity MAY ultimately be implemented as a client record,
an organization record, or a governed relationship between them, but this
document does not select that representation.

Future governance MUST determine whether:

- one Client may represent one Organization;
- one Client may represent multiple Organizations;
- one Organization may participate in multiple Client relationships;
- Client and Organization should be collapsed for a bounded v1 implementation;
- Client and Organization must remain distinct.

Until that authority source is approved, no field, claim, label, or lineage
value may be treated as the authoritative Client / Organization identity.

## 9. Stable Business Identity Model

The future authoritative business identity MUST be:

- stable within its governed authority domain;
- unique for authorization evaluation within that domain;
- resolved server-side;
- auditable;
- independent of mutable display labels;
- independent of browser assertions;
- independent of email domains;
- suitable as the target of future membership relationships;
- suitable as the top-level scope for future engagement and resource
  authorization.

This document does not define:

- identifier format;
- UUID requirements;
- database keys;
- table structure;
- schema;
- storage location;
- API representation;
- route parameters;
- provisioning workflow.

Conceptual identity is governance. Physical representation is a future
implementation decision after authority sources and contracts are approved.

## 10. Principal Relationship and Multiplicity

The governed relationship between principal and business identity remains
conceptual until membership authority is separately governed.

Architecture MUST allow:

- one stable Nguyen AI principal to be associated with zero, one, or multiple
  Governed Business Entities through separately governed membership;
- one Governed Business Entity to be associated with zero, one, or multiple
  stable Nguyen AI principals through separately governed membership.

This multiplicity does not create membership records.

A principal is not a client.

A principal is not an organization.

Principal mapping is not membership.

Membership is not entitlement.

The existence of a principal and the existence of a business identity MUST NOT
grant access without current authoritative membership and entitlement.

## 11. Assessment Service Boundary

The Assessment Service remains the sole deterministic assessment business-truth
producer.

Assessment Service evidence includes `organization`, `respondent`, `requestId`,
assessment version, `BusinessDecisionPackage`, `ExecutiveAssessmentSnapshot`,
response status, package metadata, and lineage.

Assessment `organization` and `respondent` data are business input,
context, provenance, or runtime-context data only unless a future approved
authority source explicitly governs otherwise.

Assessment `organization` and `respondent` data MUST NOT become:

- authoritative client identity;
- authoritative organization identity;
- membership authority;
- entitlement authority;
- resource authorization authority.

Assessment outputs may be governed resources later. Their business identity
association and delivery authorization remain downstream governance decisions.

## 12. EIP Boundary

The Executive Intelligence Platform remains the producer of governed executive
intelligence and `website-projection-delivery-contract-v1`.

EIP evidence includes producer snapshot identity, package identity, projection
identity, lineage, publication state, compatibility, freshness,
classification, `authorizationScopeState`, and Website Projection Delivery
Contract publication.

Those values establish producer-owned artifact identity, lineage, publication,
classification, compatibility, freshness, and delivery-governance metadata.
They do not establish:

- principal membership;
- client identity authority;
- organization identity authority;
- entitlement authority;
- browser authorization;
- business identity provisioning.

`authorizationScopeState` is EIP delivery-scope metadata. It is not a
principal entitlement decision and does not prove that any principal belongs to
the corresponding business scope.

## 13. Website and Browser Boundary

The Website remains presentation-only.

The browser may request or reference a business scope through values such as:

- `clientId`;
- `organizationId`;
- `tenantId`;
- `engagementId`;
- `workspaceId`;
- `resourceId`;
- `reportId`;
- `projectionId`;
- `deliveryId`;
- route state;
- browser storage;
- dashboard state.

All browser-supplied values are requests or hints only.

The Website and browser MUST NOT authoritatively determine:

- business identity;
- principal-to-business relationship;
- membership;
- entitlement;
- client scope;
- organization scope;
- engagement scope;
- workspace scope;
- resource authorization.

A trusted server-side authority must independently resolve and validate any
business scope before governed resources are delivered.

## 14. AWS Trusted Runtime Boundary

Runtime Owner Assignment Governance v1 assigns
`aws-ai-knowledge-assistant` as the repository ownership domain permitted to
host a future separate deterministic trusted logical service.

This document does not implement that service.

This document does not make the AI Knowledge Assistant the business identity
authority.

The future deterministic trusted logical service MAY later resolve business
identity only after:

- business identity authority source governance is approved;
- membership governance is approved;
- entitlement governance is approved;
- persistence and service contracts are separately approved;
- implementation is explicitly authorized.

AI assistant routes, Bedrock routes, local `/assessment` behavior, Cognito
configuration, API Gateway, Lambda, DynamoDB, and existing AWS documentation do
not establish client / organization identity authority.

## 15. Tenant Terminology

The term `tenant` appears in security and isolation contexts, but current
Platform authorization governance has not made `tenant` the canonical Nguyen
AI business identity.

For this increment, tenant is treated as an implementation or isolation term
unless separately governed.

Tenant MUST NOT be used as a synonym for Client, Organization, or Governed
Business Entity without future approved governance.

Browser-supplied `tenantId`, provider tenant claims, route tenant values, and
cached tenant state are non-authoritative.

## 16. Engagement Boundary

An engagement is a governed business scope subordinate to a Governed Business
Entity unless future approved governance establishes a different relationship.

Engagement is not the top-level membership target in this document.

Engagement access MUST NOT be granted solely because:

- a principal is mapped;
- a Governed Business Entity exists;
- a browser supplies an `engagementId`;
- assessment or EIP lineage references an engagement-like context;
- a previous engagement was selected.

Engagement identity and engagement lifecycle authority remain future bounded
governance prerequisites.

## 17. Workspace Boundary

Workspace is preserved as a possible operational, isolation, portal, or
resource boundary.

Current governance uses workspace as part of the minimum conceptual portal
delivery authorization scope, but this document does not require every
engagement to have a workspace.

Workspace identity remains unresolved.

Workspace MUST NOT be established solely by:

- browser `workspaceId`;
- route state;
- cached dashboard state;
- EIP lineage;
- assessment input;
- default workspace selection;
- AI inference.

Future governance MUST determine when workspace is required, what authority
establishes workspace identity, and how workspace relates to engagement and
business identity.

## 18. Resource Association Boundary

Governed resources may later be associated with a Governed Business Entity,
engagement, workspace, or other approved scope.

Examples of governed resources may include:

- assessment;
- `BusinessDecisionPackage`;
- `ExecutiveAssessmentSnapshot`;
- `ExecutiveIntelligencePackage`;
- projection;
- `website-projection-delivery-contract-v1`;
- report;
- authorized AI Knowledge Assistant context.

Resource association, producer lineage, publication state, or resource
existence MUST NOT by itself grant principal access.

Detailed resource identity, lookup, association, and authorization remain
future governance increments.

## 19. Identity Authority Source Status

This document governs identity semantics only.

The Client / Organization identity authority source is:

- UNRESOLVED

The following remain separate decisions:

- identity semantics;
- identity authority source;
- identity persistence;
- identity provisioning;
- identity lifecycle administration;
- membership authority source;
- entitlement authority source;
- resource lookup.

No current repository evidence proves an approved authority source for stable
Client / Organization identity.

## 20. Identity Lifecycle Concepts

Future Client / Organization identity authority must define lifecycle
semantics sufficient for authorization safety.

At minimum, future governance must address conceptual states such as:

- active;
- inactive;
- disabled;
- revoked;
- superseded;
- merged;
- split;
- unknown;
- unavailable.

This document does not define schema values, status enums, databases, records,
or lifecycle workflows.

Inactive, disabled, revoked, unknown, conflicting, stale where current
validity is required, or unavailable business identity state MUST NOT produce
ALLOW.

Merges, splits, reassignments, and replacements MUST NOT silently transfer
membership, entitlement, or resource access without separate approved
authority.

## 21. Fail-Closed Semantics

Business identity resolution MUST fail closed when identity state is:

- missing;
- unknown;
- unavailable;
- malformed;
- ambiguous;
- conflicting;
- inactive;
- disabled;
- revoked;
- stale where current validity is required;
- unsupported;
- outside approved scope.

No fallback may use:

- organization name;
- company name;
- email domain;
- user email;
- provider group;
- custom claim;
- previous client;
- previous organization;
- browser selection;
- cached browser state;
- default tenant;
- assessment organization text;
- EIP lineage alone;
- Website display state;
- AI inference.

Failure to establish exactly the governed business identity required for a
future authorization decision MUST result in no authorized business scope.

## 22. AI / Bedrock / Model Authority Boundary

AI, Bedrock, LLMs, RAG, and the AI Knowledge Assistant MUST NOT:

- infer authoritative client identity;
- infer authoritative organization identity;
- infer organization membership;
- merge organizations;
- split organizations;
- create client relationships;
- repair ambiguous identity;
- select a tenant;
- determine membership;
- determine entitlement;
- authorize resources;
- override deterministic business identity state;
- fabricate missing business authority.

AI MAY only consume already-authorized governed context after deterministic
authorization succeeds and a separate approved consumer boundary permits that
use.

## 23. Audit and Privacy Governance

Future business identity resolution and authorization decisions must be
auditable without collecting unnecessary business or personal data.

Conceptual audit evidence MAY include:

- timestamp;
- governed business identity reference when successfully resolved;
- authority/version reference where applicable;
- requested operation or context;
- resolution outcome;
- reason classification;
- correlation or request identifier.

Audit governance MUST minimize identity evidence to what is necessary for
resolution, authorization, troubleshooting, and compliance review.

Audit records MUST NOT require raw authentication tokens, secrets,
credentials, unnecessary profile attributes, unnecessary respondent data, or
unnecessary business details.

This document does not select logging, monitoring, storage, retention, or audit
technology.

## 24. Technology Neutrality

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
Service, EIP, or AI capability becomes the Client / Organization identity
authority through this document.

## 25. Producer and Consumer Boundaries

Assessment Service remains the sole deterministic assessment business-truth
producer.

EIP remains the governed executive-intelligence and
`website-projection-delivery-contract-v1` producer.

Website remains presentation-only.

The future deterministic trusted logical service remains a future enforcement
boundary only after separate implementation approval.

AI Knowledge Assistant remains a separate consumer and explainer capability.

Client / Organization identity governance MUST NOT move assessment truth,
executive intelligence production, Website presentation authority, or AI
authority into the business identity layer.

## 26. Authority Status Matrix

| Area | Status | Governance meaning |
| --- | --- | --- |
| Stable principal concept | GOVERNED | Stable Principal Mapping Authority Governance v1 defines the actor concept. |
| Principal mapping semantics | GOVERNED | Mapping semantics are governed; implementation is not authorized. |
| Principal mapping authority source | UNRESOLVED | No approved source currently establishes mappings. |
| Client / Organization concept | GOVERNED CONCEPTUALLY | This document defines the business-identity concepts and boundaries. |
| Client / Organization identity semantics | GOVERNED CONCEPTUALLY | Stable, server-resolved, auditable business identity semantics are governed. |
| Client / Organization authority source | UNRESOLVED | No approved source currently establishes authoritative business identity. |
| Client / Organization persistence | UNRESOLVED | No storage or persistence mechanism is selected. |
| Client / Organization provisioning | UNRESOLVED | No creation, onboarding, merge, split, or administration workflow is selected. |
| Membership semantics | GOVERNED CONCEPTUALLY | PME v1 defines membership as principal plus client / organization context. |
| Membership authority source | UNRESOLVED | No approved source currently establishes membership. |
| Engagement identity | PARTIALLY GOVERNED / UNRESOLVED | Engagement is subordinate scope conceptually; authority source remains unresolved. |
| Workspace identity | PARTIALLY GOVERNED / UNRESOLVED | Workspace is preserved as a possible scope boundary; authority source remains unresolved. |
| Resource identity / lookup | PARTIALLY GOVERNED / UNRESOLVED | Producer artifact identity exists, but runtime lookup and authorization identity remain unresolved. |
| Entitlement authority | UNRESOLVED | No approved source currently establishes entitlement. |

This matrix must not be read as implementation approval.

## 27. Unresolved Decisions and Future Governance

The following remain unresolved:

- Client / Organization identity authority source;
- Client / Organization persistence;
- Client / Organization provisioning;
- Client / Organization lifecycle administration;
- handling of organization merge, split, replacement, and aliasing;
- whether Client and Organization remain distinct in implementation;
- whether one Client may represent multiple Organizations;
- whether one Organization may participate in multiple Client relationships;
- principal mapping authority source;
- membership authority source;
- entitlement authority source;
- engagement identity and lifecycle;
- workspace identity and lifecycle;
- governed resource identity and lookup;
- requested action vocabulary;
- authority administration and revocation;
- trusted authorization service contract;
- EIP retrieval mechanism;
- Website authorized delivery integration;
- audit and observability implementation;
- security and IAM boundaries;
- deterministic route isolation.

Each unresolved item requires separate approved governance before
implementation may begin.

## 28. Implementation Prerequisites

Before Client / Organization identity can support authorization
implementation, future governance must approve at least:

1. authority source for stable Client / Organization identity;
2. lifecycle semantics for active, inactive, disabled, revoked, merged, split,
   superseded, unknown, and unavailable identity state;
3. relationship between Client and Organization for implementation scope;
4. principal-to-business-identity membership authority;
5. engagement identity and scope model;
6. workspace identity and scope model where applicable;
7. governed resource identity and lookup model;
8. requested action vocabulary;
9. entitlement authority source;
10. administration and revocation model;
11. persistence mechanism;
12. API or service contract;
13. audit and observability model;
14. security and IAM boundary;
15. EIP retrieval integration;
16. Website authorized delivery integration;
17. deterministic route isolation.

This prerequisite list does not authorize any implementation.

## 29. Implementation Gate

CLIENT / ORGANIZATION IDENTITY AUTHORITY GOVERNANCE v1 DOES NOT AUTHORIZE
IMPLEMENTATION.

It does not authorize:

- client identity implementation;
- organization identity implementation;
- principal-to-client mapping;
- principal-to-organization mapping;
- membership;
- entitlement;
- authorization;
- persistence;
- provisioning;
- identity administration;
- schemas;
- APIs;
- endpoints;
- Cognito changes;
- Cognito groups;
- custom claims;
- IAM changes;
- DynamoDB;
- S3;
- SQL;
- infrastructure changes;
- EIP integration;
- EIP retrieval;
- Assessment Service changes;
- Website changes;
- AWS runtime changes;
- AI changes;
- Bedrock changes;
- deployment.

Any implementation requires separate architecture approval, governance
approval, owning-repository approval, implementation plan, and explicit
authorization.

## 30. Acceptance Criteria

This artifact is acceptable only if:

- Client is governed as a business relationship concept;
- Organization is governed as an external business entity or context;
- Client and Organization are not falsely declared universally synonymous;
- the stable Governed Business Entity concept is defined;
- stable business identity is independent of mutable labels and browser
  assertions;
- principal, membership, and entitlement remain distinct;
- conceptual multiplicity is allowed without creating membership;
- assessment organization and respondent data remain non-authoritative for
  authorization;
- EIP lineage and `authorizationScopeState` remain producer metadata, not
  principal entitlement;
- Website and browser values remain non-authoritative;
- tenant remains non-canonical unless separately governed;
- engagement and workspace boundaries are preserved without implementation;
- resource association does not imply access;
- authority source, persistence, and provisioning remain unresolved;
- fail-closed behavior is explicit;
- AI has no business-identity authority;
- producer and consumer boundaries remain intact;
- no technology is selected;
- implementation remains unauthorized.
