# Governed Resource Identity / Lookup Governance v1

## 1. Purpose and Scope

Version: v1

This artifact governs the conceptual semantics by which Nguyen AI identifies and
resolves governed Resources for future deterministic authorization and delivery.

This artifact defines:

- what a governed Resource is;
- how Resource identity differs from producer identity, lineage, business
  scope, lookup reference, and physical storage location;
- how trusted Resource lookup must behave before downstream authorization,
  retrieval, delivery, and AI context use;
- which current producer artifacts MAY become governed Resources through later
  implementation; and
- which authority, persistence, runtime, and integration decisions remain
  unresolved.

This artifact is governance only. It MUST NOT be interpreted as authorization to
create source code, schemas, APIs, endpoints, databases, infrastructure,
retrieval behavior, authorization behavior, entitlement behavior, Website
integration, Assessment Service integration, EIP integration, AI integration, or
deployment.

## 2. Governance Status and Authority

This artifact is a Platform governance artifact in the Nguyen AI Platform
control plane.

It extends, and MUST remain consistent with:

- Portal Governed Delivery Authorization Model v1;
- EIP Governed Retrieval Boundary v1;
- Runtime Owner Assignment Governance v1;
- Principal / Membership / Entitlement Authority Model v1;
- Stable Principal Mapping Authority Governance v1;
- Client / Organization Identity Authority Governance v1; and
- Membership Authority Source Governance v1.

This artifact governs Resource identity and lookup semantics only. It does not
supersede producer contracts, repository ownership, retrieval governance,
authorization governance, membership governance, entitlement governance, or
runtime implementation gates.

## 3. Architectural Context

The approved authorization chain currently requires:

trusted authentication evidence
-> stable Nguyen AI Principal
-> authoritative Membership
-> governed business and scope context
-> governed Resource
-> requested Action
-> authoritative Entitlement
-> deterministic ALLOW or DENY
-> governed retrieval and delivery

Prior governance has established that authentication is not authorization,
principal mapping is not membership, membership is not entitlement, retrieval is
not authorization, browser values are non-authoritative, and AI has no
authorization authority.

This artifact addresses the next required dependency in that chain:

What Resource is the verified Principal attempting to access, and how must a
future trusted system resolve that Resource deterministically without granting
authorization?

## 4. Evidence Basis

Repository evidence reviewed for this artifact supports the following
observations:

- The Assessment Service contains assessment requests, request identifiers,
  organization/respondent request context, deterministic assessment responses,
  BusinessDecisionPackage governance, and ExecutiveAssessmentSnapshot governance.
- The Executive Intelligence Platform contains admitted snapshot catalog
  entries, derived artifacts, ExecutiveIntelligencePackage artifacts,
  ExecutiveIntelligenceProjection artifacts, Website Projection Delivery
  Contract production, publication eligibility, freshness, classification,
  compatibility, authorizationScopeState, and lineage metadata.
- The Website contains Executive Dashboard presentation, Website Projection
  Delivery consumption, bearer-token delivery requests, dashboard/report
  rendering concepts, and browser-visible state.
- The AWS AI Knowledge Assistant repository contains Cognito-authenticated
  request flow, Lambda routing, assistant conversation identifiers, deterministic
  runtime provider selection, DynamoDB conversation history, Bedrock provider
  paths, and current Assessment route handling.

This evidence establishes current producer artifacts, presentation concepts,
runtime routes, and lineage metadata. It does not establish a concrete Resource
authority source, Resource persistence, Resource registry, Resource lookup API,
Resource authorization service, or entitlement authority.

## 5. Definitions

**Governed Resource** means a Nguyen AI object, artifact, delivery object, or
governed capability against which future deterministic authorization may
evaluate access.

**Producer Identity** means identity assigned or maintained by the authoritative
producer of an artifact or business output.

**Lineage Identity** means identity or reference used to prove provenance,
derivation, or traceability across producer boundaries.

**Business Scope Identity** means identity associating a Resource with the
appropriate Governed Business Entity and, where applicable, Engagement or other
governed scope.

**Lookup Identity** means identity or reference used by a future trusted system
to resolve a requested Resource reference to a governed Resource.

**Authorization Resource Identity** means the stable Resource identity used as a
future deterministic authorization input.

**Resource Lookup** means trusted deterministic resolution of a requested
Resource reference to exactly one valid Governed Resource or a fail-closed
outcome.

## 6. Governed Resource Definition

A Governed Resource MUST represent an object, artifact, delivery representation,
or governed capability whose future use, retrieval, presentation, explanation,
or delivery may require deterministic authorization.

A Governed Resource MUST NOT be treated as any of the following:

- Principal;
- Governed Business Entity;
- Membership;
- Engagement;
- Workspace;
- Action;
- Entitlement;
- producer artifact identity by default;
- browser route;
- API route;
- database record;
- storage key;
- cache key; or
- AI-generated reference.

Resource existence MUST NOT imply authorization.

Resource possession MUST NOT imply authorization.

Resource discovery MUST NOT imply authorization.

Resource retrieval MUST NOT imply authorization.

Resource publication MUST NOT imply authorization.

## 7. Resource Identity Semantics

Governed Resource identity MUST be suitable for deterministic authorization.

Resource identity MUST be:

- deterministic;
- unique within its governed Resource identity domain;
- server-resolved;
- auditable;
- stable for the required lifecycle;
- distinguishable from display labels;
- distinguishable from browser parameters;
- distinguishable from physical storage location;
- independent of mutable presentation state; and
- independent of AI inference.

This artifact does not select an identifier format, UUID convention, key
structure, schema, route parameter, API representation, storage location, or
persistence mechanism.

## 8. Identity Layer Separation

Producer Identity, Lineage Identity, Business Scope Identity, Lookup Identity,
and Authorization Resource Identity MAY sometimes correspond for a specific
Resource.

They MUST NOT be assumed equivalent without separately governed evidence.

The future trusted authorization and delivery boundary MUST preserve the
distinction between these identity layers. A value valid in one layer MUST NOT
automatically become authoritative in another layer.

## 9. Producer Identity

Producer Identity is assigned or maintained by the repository that owns the
producer responsibility.

Examples supported by current evidence include assessment request and response
identifiers, ExecutiveAssessmentSnapshot identity, SnapshotCatalogEntry identity,
SnapshotDerivedArtifact identity, ExecutiveIntelligencePackage identity,
ExecutiveIntelligenceProjection identity, and Website Projection Delivery
Contract production identity.

Producer Identity proves producer-side artifact identity. It MUST NOT by itself
establish authorization Resource identity, business scope, Membership,
Entitlement, or delivery permission.

## 10. Lineage Identity

Lineage Identity preserves traceability among producer outputs and derived
artifacts.

Current EIP evidence shows lineage relationships such as:

Assessment truth
-> ExecutiveAssessmentSnapshot
-> SnapshotCatalogEntry
-> SnapshotDerivedArtifact
-> ExecutiveIntelligencePackage
-> ExecutiveIntelligenceProjection
-> Website Projection Delivery Contract

Lineage Identity MUST preserve producer meaning and provenance. It MUST NOT be
used as a substitute for Resource authority, Membership authority, Entitlement
authority, or business-scope authority.

## 11. Business Scope Identity

Business Scope Identity associates a Resource with the Governed Business Entity
and any additional governed scope required for future authorization.

Business scope association MUST be:

- server-resolved;
- deterministic;
- auditable;
- based on authoritative source data or separately governed trusted lineage;
  and
- fail-closed when missing, ambiguous, conflicting, stale, invalid, or
  unavailable.

Browser-supplied clientId, organizationId, tenantId, engagementId, workspaceId,
or equivalent values MUST NOT establish business scope association.

This artifact does not select the authority source, persistence mechanism, or
registration process for business scope association.

## 12. Lookup Identity

Lookup Identity is the trusted resolution reference used by a future server-side
runtime to resolve a requested Resource reference.

Lookup Identity MAY be derived from producer identity, lineage, delivery
metadata, or another governed source only after that relationship is separately
approved.

Lookup Identity MUST NOT be equated with:

- URL;
- browser route;
- API endpoint;
- query parameter;
- file path;
- object key;
- database key;
- cache key;
- Lambda route;
- conversation identifier; or
- AI-generated resource label.

## 13. Authorization Resource Identity

Authorization Resource Identity is the stable Resource identity used as an
input to future deterministic authorization decisions.

Authorization Resource Identity MUST identify the governed Resource being
evaluated. It MUST NOT decide whether the Principal may access that Resource.

Authorization Resource Identity becomes meaningful only as part of the
downstream authorization chain:

verified Principal
-> authoritative Membership
-> governed business and scope context
-> Governed Resource
-> requested Action
-> authoritative Entitlement
-> ALLOW or DENY

## 14. Resource Type and Classification

Future authorization requires deterministic Resource type or classification so
that later Requested Action and Entitlement governance can reason about
Resources safely.

Current repository evidence supports the following Resource categories as
governance candidates:

- assessment output;
- ExecutiveAssessmentSnapshot;
- BusinessDecisionPackage;
- SnapshotCatalogEntry;
- SnapshotDerivedArtifact;
- ExecutiveIntelligencePackage;
- ExecutiveIntelligenceProjection;
- Website Projection Delivery Contract;
- dashboard delivery object;
- report or downloadable delivery artifact where produced under approved
  governance; and
- AI-authorized context only after deterministic Resource, Action,
  Membership, and Entitlement governance authorize it.

This list does not create an approved permission vocabulary, entitlement model,
Resource registry, storage design, or delivery implementation.

## 15. Resource Ownership vs Resource Authority

Resource governance MUST distinguish:

- producer ownership;
- business association;
- retrieval ownership;
- runtime custody;
- authorization authority; and
- presentation responsibility.

Assessment Service production of deterministic assessment truth does not make
Assessment Service the portal entitlement authority.

EIP production of executive intelligence or Website Projection Delivery
Contracts does not make EIP the Principal entitlement authority.

Future AWS runtime custody or retrieval does not make the runtime the producer
of Assessment Service or EIP truth.

Website display does not make Website authoritative for Resource identity,
business association, Membership, Entitlement, lookup, or ALLOW/DENY.

AI receipt of authorized context does not make AI authoritative for Resource
identity, lookup, Membership, Entitlement, or authorization.

## 16. Business Entity Association

A Governed Resource MUST be associated with the appropriate Governed Business
Entity when future authorization depends on business scope.

Such association MUST be established by server-side trusted resolution.

Such association MUST NOT be established by:

- browser selection;
- Website state;
- user email;
- email domain;
- Cognito group;
- custom claim;
- prior session;
- prior client;
- assessment organization text alone;
- EIP lineage alone;
- shared display name; or
- AI inference.

If the business entity association is missing, ambiguous, conflicting, stale,
invalid, or unavailable, Resource lookup MUST fail closed.

## 17. Engagement Relationship

Current governance does not require Engagement identity to precede Resource
identity.

A Governed Resource MAY require Engagement scope when producer evidence,
business governance, or later authorization governance establishes that
relationship.

A Governed Resource MAY also be scoped directly to a Governed Business Entity
where Engagement is not required.

This artifact does not create Engagement Identity and Scope Governance. It does
not define Engagement authority source, lifecycle, persistence, hierarchy, or
authorization rules.

## 18. Workspace Relationship

Workspace remains future or optional in the current authorization model.

Workspace MUST NOT be required for Resource identity merely because it is common
in software products.

If a future Resource requires Workspace scope, that relationship REQUIRES
separate governance. Until then, Workspace identity and scope remain unresolved
or optional for Resource lookup.

## 19. Resource Association and Lineage

Resource identity SHOULD preserve traceability to authoritative producer
lineage where lineage exists and matters for correctness.

For EIP-derived delivery, governed Resource association MAY preserve a chain
such as:

Assessment truth
-> ExecutiveAssessmentSnapshot
-> SnapshotCatalogEntry
-> SnapshotDerivedArtifact
-> ExecutiveIntelligencePackage
-> ExecutiveIntelligenceProjection
-> Website Projection Delivery Contract
-> governed delivery Resource

This artifact does not redefine producer lineage, compute lineage, validate
producer compatibility rules, or authorize reconstruction of missing artifacts.

## 20. Lookup Semantics

Governed Resource lookup means:

requested Resource reference
-> deterministic trusted resolution
-> exactly one valid Governed Resource or fail closed

A future trusted runtime MUST distinguish lookup outcomes including:

- FOUND;
- NOT FOUND;
- AMBIGUOUS;
- CONFLICTING;
- STALE / INVALID where producer state requires it; and
- UNAVAILABLE.

Only FOUND with exactly one valid governed Resource may proceed to later
authorization evaluation. It still does not grant access.

This artifact does not design an API, endpoint, route, query parameter,
persistence mechanism, storage design, or runtime implementation.

## 21. Lookup Is Not Authorization

Successful Resource lookup means only that the trusted system resolved the
requested reference to a governed Resource.

Lookup DOES NOT establish:

- Principal validity;
- Membership;
- business entity access;
- Engagement access;
- Workspace access;
- Entitlement;
- requested Action permission;
- delivery authorization; or
- ALLOW.

Authorization remains downstream and MUST evaluate all required governed inputs.

## 22. Lookup Is Not Retrieval

Resource lookup and Resource retrieval are separate controls.

Resource lookup answers:

Which governed Resource is being referenced?

Retrieval answers:

Can the trusted system obtain the approved producer artifact represented by that
Resource?

Authorization answers:

May this verified Principal perform the requested Action against that Resource?

The EIP Governed Retrieval Boundary remains authoritative for retrieval
governance. This artifact does not implement or select EIP retrieval mechanics.

## 23. Resource Identity vs Physical Location

Governed Resource identity MUST NOT be defined by physical or technical
location.

The following values MUST NOT become Resource identity merely because they
exist:

- S3 object key;
- DynamoDB key;
- SQL primary key;
- filesystem path;
- URL;
- API endpoint;
- browser route;
- cache key;
- Lambda identifier;
- Cognito identity;
- IAM identity; or
- Bedrock context reference.

Such values MAY participate in future implementation only after separate
governance approves their role.

## 24. Resource Lookup Fail-Closed Model

Resource lookup MUST fail closed when Resource state is:

- unknown;
- missing;
- ambiguous;
- conflicting;
- malformed;
- invalid;
- stale;
- unavailable;
- unsupported;
- associated with a disabled or inactive scope where applicable; or
- inconsistent with required producer lineage, freshness, compatibility, or
  classification.

Resource lookup MUST NOT silently recover through:

- previous-client fallback;
- previous-engagement fallback;
- previous-workspace fallback;
- default client;
- default Resource;
- nearest match;
- fuzzy match;
- email inference;
- domain inference;
- browser-state inference;
- cached prior selection;
- cross-client substitution;
- cross-engagement substitution;
- stale artifact substitution;
- older artifact substitution unless separately governed;
- synthetic artifact creation;
- raw upstream reconstruction; or
- AI inference.

Failure to resolve exactly one valid governed Resource MUST produce no
substituted Resource and MUST NOT proceed as authorized delivery.

## 25. Cross-Business-Entity Isolation

Resource resolution MUST preserve isolation between governed business entities.

A Resource associated with Governed Business Entity A MUST NOT be substituted
for a Resource associated with Governed Business Entity B.

Shared names, similar identifiers, route values, browser values, email domains,
previous sessions, producer lineage resemblance, or AI context MUST NOT
establish cross-business-entity equivalence.

Cross-business-entity ambiguity MUST fail closed.

## 26. Resource Version / Freshness / Classification

Where producer governance defines version, compatibility, freshness,
publication eligibility, classification, lineage, limitations, or producer
validity, Resource lookup MUST preserve those semantics.

The trusted consumer MUST NOT:

- repair producer state;
- reinterpret producer state;
- override freshness;
- override classification;
- override compatibility;
- override publication eligibility;
- remove limitations;
- conceal lineage gaps; or
- synthesize a valid producer artifact from invalid or missing producer state.

This artifact does not duplicate Assessment Service or EIP business rules.

## 27. Assessment Service Boundary

Assessment Service remains the sole authoritative producer of deterministic
assessment business truth.

Resource governance MUST NOT:

- score assessments;
- aggregate assessment results;
- weight responses;
- determine readiness;
- determine severity;
- determine risk;
- determine confidence;
- generate authoritative recommendations;
- generate authoritative assessment summaries;
- modify Assessment Service output; or
- reconstruct missing Assessment Service truth.

Assessment artifacts MAY become governed Resources only as consumers of
already-produced Assessment Service truth.

## 28. EIP Boundary

EIP remains the authoritative producer of governed executive intelligence and
Website Projection Delivery Contracts.

Resource governance MUST NOT:

- derive executive intelligence;
- recreate projections;
- republish invalid artifacts;
- override freshness;
- override classification;
- override compatibility;
- repair lineage;
- synthesize Website Projection Delivery Contracts; or
- reconstruct upstream artifacts.

EIP metadata MAY inform Resource identity, type, lineage, and delivery
eligibility only under separately governed trusted resolution.

## 29. Website Boundary

Website remains presentation-only.

Website MAY request or present governed Resources through future trusted
contracts.

Website MUST NOT establish authoritative:

- Resource identity;
- business association;
- Membership;
- Entitlement;
- requested Action authorization;
- lookup resolution; or
- ALLOW/DENY.

Browser identifiers remain untrusted request context.

## 30. Trusted Runtime Boundary

The future separate deterministic trusted logical service in the
aws-ai-knowledge-assistant repository may eventually resolve governed Resource
references, enforce deterministic lookup rules, consume authoritative Resource
associations, participate in authorization, retrieve approved producer
artifacts, and deliver authorized results.

This artifact does not authorize implementation of that service.

Repository ownership does not make the future runtime the producer of
Assessment Service truth, the producer of EIP truth, the Resource authority
source, the Membership authority source, or the Entitlement authority source.

## 31. AI / Bedrock / Model Authority Boundary

AI, Bedrock, LLMs, RAG, embeddings, semantic similarity, probabilistic systems,
and the AI Knowledge Assistant MUST NOT:

- create Resource identity;
- infer authoritative Resource identity;
- select among ambiguous Resources;
- repair missing Resource identity;
- infer business association;
- override lookup failure;
- authorize Resource access;
- override ALLOW/DENY;
- reconstruct missing deterministic truth; or
- substitute Resource lookup with semantic similarity.

Resource identity and lookup are deterministic governance concerns.

AI Knowledge Assistant remains consumer/explainer only.

## 32. Action Boundary

This artifact does not define the Requested Action / Permission Vocabulary.

Repository evidence may include concepts such as view, retrieve, download,
upload, submit, explain, administer, manage, publish, or modify. These concepts
MUST NOT become approved permissions through this artifact.

This artifact establishes Resource typing and identity semantics so a later
governance increment can define meaningful Actions against governed Resource
types.

## 33. Entitlement Boundary

This artifact does not define Entitlement rules.

Resource existence, Resource identity, Resource association, Resource
classification, Resource publication, or successful Resource lookup MUST NOT
imply Entitlement.

Entitlement remains downstream and unresolved until a separate governance
increment defines its authority semantics.

## 34. Authority Source Boundary

This artifact does not select:

- Principal Mapping Authority Source;
- Client / Organization Authority Source;
- Membership Authority Source;
- Resource Authority Source; or
- Entitlement Authority Source.

Concrete Resource Authority Source remains UNRESOLVED.

Producer ownership and Resource authority MUST remain distinguishable.

## 35. Persistence Boundary

This artifact does not select:

- DynamoDB;
- S3;
- SQL;
- filesystem;
- object storage;
- document database;
- relational database;
- cache;
- queue;
- event bus;
- external SaaS;
- CRM; or
- any other persistence mechanism.

Resource persistence remains UNRESOLVED.

## 36. Technology Neutrality

This artifact does not choose:

- schema;
- table;
- partition key;
- sort key;
- object key;
- UUID format;
- API;
- endpoint;
- route;
- query parameter;
- IAM design;
- Cognito group;
- custom claim;
- RBAC;
- ABAC;
- ACL;
- policy engine; or
- implementation framework.

Technology names in this artifact are evidence references, explicit
non-selections, or architectural constraints only.

## 37. Audit Governance

Future Resource lookup MUST be auditable at the conceptual level.

Audit evidence SHOULD be sufficient to establish:

- timestamp;
- requested Resource reference;
- resolved governed Resource reference when successful;
- Resource type or classification;
- business-scope reference where appropriate;
- resolution outcome;
- failure or reason classification;
- authority or version reference where applicable; and
- correlation or request identifier.

Audit governance MUST minimize sensitive data. Audit evidence MUST NOT require
raw tokens, secrets, credentials, unnecessary sensitive payloads, unnecessary
assessment content, or unnecessary AI context.

This artifact does not select logging, audit storage, observability tooling, or
retention technology.

## 38. Resource Authority Status Matrix

| Concept | Status | Governance Position |
| --- | --- | --- |
| Governed Resource concept | GOVERNED CONCEPTUALLY | Defined as an authorization-facing object, artifact, delivery object, or governed capability. |
| Resource identity semantics | GOVERNED CONCEPTUALLY | Deterministic, server-resolved, auditable, stable, and independent of browser or AI assertion. |
| Resource type semantics | GOVERNED CONCEPTUALLY | Current categories are identified from repository evidence without defining Actions or Entitlements. |
| Producer identity relationship | GOVERNED CONCEPTUALLY | Producer identity may inform Resource identity but is not automatically equivalent. |
| Lineage relationship | GOVERNED CONCEPTUALLY | Lineage must be preserved where producer governance requires it. |
| Business entity association | GOVERNED CONCEPTUALLY | Required when authorization depends on business scope; authority source remains unresolved. |
| Engagement association | PARTIALLY GOVERNED / UNRESOLVED | Conditional; not mandatory for all Resources; Engagement governance remains downstream. |
| Workspace association | OPTIONAL / FUTURE | Not required by current evidence; separate governance required if later needed. |
| Resource authority source | UNRESOLVED | No concrete authority source selected. |
| Resource persistence | UNRESOLVED | No persistence mechanism selected. |
| Resource provisioning or registration | UNRESOLVED | No registry, provisioning, or registration implementation authorized. |
| Resource lifecycle | PARTIALLY GOVERNED / UNRESOLVED | Producer lifecycle must be preserved; authorization Resource lifecycle remains downstream. |
| Resource lookup semantics | GOVERNED CONCEPTUALLY | Requested Resource reference resolves to exactly one valid Governed Resource or fails closed. |
| EIP WPDC resource relationship | GOVERNED CONCEPTUALLY | WPDC may be a governed Resource candidate; EIP remains producer, not entitlement authority. |
| Assessment resource relationship | GOVERNED CONCEPTUALLY | Assessment outputs may be governed Resource candidates; Assessment Service remains truth producer. |
| Report/dashboard resource relationship | PARTIALLY GOVERNED / DOWNSTREAM | Presentation and delivery objects are candidates; implementation and entitlement remain downstream. |
| AI-authorized context relationship | DOWNSTREAM | AI context may be delivered only after deterministic authorization governance and implementation. |
| Action vocabulary | DOWNSTREAM / UNRESOLVED | Not defined by this artifact. |
| Entitlement authority | DOWNSTREAM / UNRESOLVED | Not defined by this artifact. |

## 39. Implementation Gate

Governed Resource Identity / Lookup Governance v1 DOES NOT AUTHORIZE:

- source-code changes;
- runtime implementation;
- Resource registry implementation;
- database or storage implementation;
- schema creation;
- API creation;
- endpoint creation;
- route creation;
- EIP retrieval implementation;
- Assessment Service integration;
- Website integration;
- AI integration;
- Cognito changes;
- IAM changes;
- infrastructure changes;
- authorization implementation;
- entitlement implementation;
- requested-action permission implementation;
- deployment; or
- production delivery.

Implementation remains blocked by downstream governance, including Requested
Action / Permission Vocabulary, Entitlement Authority governance, Trusted
Authorization Service Contract governance, retrieval integration governance,
and explicit implementation approval in the owning repository.

## 40. Acceptance Criteria

This artifact is acceptable only if:

- it defines Governed Resource semantics without selecting implementation;
- it preserves producer/consumer boundaries;
- it separates lookup from authorization;
- it separates lookup from retrieval;
- it preserves Assessment Service and EIP producer authority;
- it preserves Website presentation-only status;
- it preserves AI non-authority;
- it prevents browser-provided Resource and business-scope values from becoming
  authoritative;
- it preserves cross-business-entity isolation;
- it requires fail-closed Resource lookup;
- it leaves Resource Authority Source unresolved;
- it leaves Resource persistence unresolved;
- it leaves Action vocabulary downstream;
- it leaves Entitlement authority downstream; and
- it authorizes no source code, schema, API, endpoint, infrastructure,
  deployment, or runtime behavior.
