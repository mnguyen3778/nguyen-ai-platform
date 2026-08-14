# Requested Action / Permission Vocabulary Governance v1

Version: v1

## 1. Purpose

This artifact governs the bounded, technology-neutral vocabulary for describing
what operation a verified Nguyen AI Principal requests to perform against or in
relation to a governed Resource.

The purpose is to provide the next semantic input required before Entitlement
Authority governance can determine whether a requested operation may be allowed
or denied.

This artifact does not grant access. It defines business-level Requested Action
semantics only.

## 2. Scope

This artifact governs:

- the definition of Requested Action;
- the relationship between Requested Action and permission terminology;
- the distinction between Action, Resource, lookup, retrieval, authorization,
  Entitlement, UI behavior, API behavior, runtime functions, and AI behavior;
- the minimal current Action vocabulary supported by objective repository
  evidence;
- fail-closed behavior for unknown or invalid Actions;
- audit expectations for future deterministic Action resolution; and
- implementation gates that preserve downstream governance boundaries.

This artifact does not govern Entitlement rules, role models, persistence,
schemas, APIs, endpoints, runtime routing, service contracts, or implementation.

## 3. Governance Context

Approved Platform governance now establishes the following authorization chain:

verified authentication evidence
-> stable Nguyen AI Principal
-> Governed Business Entity
-> Membership
-> Governed Resource
-> Requested Action
-> Entitlement
-> ALLOW / DENY

The preceding Governed Resource Identity / Lookup Governance v1 artifact
governed Resource identity and lookup semantics. The next missing semantic
input is the business-level operation requested against a governed Resource.

## 4. Existing Approved Governance

This artifact depends on and preserves:

- Portal Governed Delivery Authorization Model v1;
- EIP Governed Retrieval Boundary v1;
- Runtime Owner Assignment Governance v1;
- Principal / Membership / Entitlement Authority Model v1;
- Stable Principal Mapping Authority Governance v1;
- Client / Organization Identity Authority Governance v1;
- Membership Authority Source Governance v1; and
- Governed Resource Identity / Lookup Governance v1.

Those artifacts establish that authentication is not authorization, Principal
mapping is not Membership, Membership is not Entitlement, lookup is not
authorization, retrieval is not authorization, Resource existence is not
authorization, browser state is non-authoritative, AI is non-authoritative, and
implementation remains separately gated.

## 5. Product Evidence Basis

Current evidence supports only a bounded Action vocabulary.

Assessment Service evidence includes assessment request submission, assessment
version validation, organization and respondent request data, deterministic
assessment response production, scores, findings-related methodology,
recommendations, BusinessDecisionPackage, and ExecutiveAssessmentSnapshot
artifacts. This evidence supports a submitted input operation but does not
authorize mutation of Assessment Service truth.

Executive Intelligence Platform evidence includes SnapshotCatalogEntry,
SnapshotDerivedArtifact, ExecutiveIntelligencePackage,
ExecutiveIntelligenceProjection, WebsiteProjectionDeliveryContract,
publication, freshness, classification, compatibility, lineage, delivery
eligibility, and dashboard content sections. This evidence supports
presentation and delivery of governed producer artifacts but does not establish
Principal Entitlement.

Website evidence includes Executive Dashboard rendering, Website Projection
Delivery Contract consumption through an authenticated bearer-token request,
assessment submission, findings and recommendations presentation, and a
synthetic report download link. This evidence supports business-level view,
download, and submit concepts but does not make UI controls authoritative.

AWS AI Knowledge Assistant evidence includes assistant request/response
contracts, conversation identifiers, deterministic runtime provider paths,
Bedrock provider capability, Cognito-authenticated infrastructure evidence, and
conversation history. This evidence supports a possible explanation operation
over already-authorized context but does not make AI authoritative for Action,
Entitlement, Resource, Membership, or business identity.

Observed implementation behavior is evidence only. It is not itself an approved
Action vocabulary.

## 6. Requested Action Definition

A Requested Action is a stable, business-level description of the operation a
verified Nguyen AI Principal is requesting to perform against or in relation to
a governed Resource.

Requested Action describes what operation is requested. It does not establish
whether the operation is permitted.

Requested Action MUST remain distinct from:

- Principal;
- Governed Business Entity;
- Membership;
- Engagement;
- Workspace;
- Resource;
- Resource Type;
- Resource lookup;
- Resource retrieval;
- Entitlement;
- ALLOW / DENY;
- UI controls;
- HTTP methods;
- API routes;
- Lambda handlers;
- application functions;
- persistence operations; and
- AI or model behavior.

## 7. Permission Terminology

Within this governance artifact, permission vocabulary means the controlled set
of canonical Requested Action names that may later be referenced by Entitlement
governance.

A permission name is not a grant of authority. A permission name only describes
a kind of requested operation.

The following invariants apply:

- Action != Entitlement.
- Permission name != Entitlement.
- Action existence != authorization.
- Permission vocabulary existence != authorization.

## 8. Action vs Entitlement

Requested Action answers:

What operation is being requested?

Entitlement later answers:

May Principal P perform requested Action A against governed Resource or Scope R?

Future deterministic authorization may use:

Principal
+ Membership / governed scope
+ Resource
+ Requested Action
+ Entitlement
-> ALLOW / DENY

This artifact MUST NOT define Entitlement rules, Entitlement grants, Entitlement
inheritance, role semantics, role hierarchy, or policy evaluation.

## 9. Action vs Resource

Resource identifies what governed object, artifact, delivery object, or
capability is being acted upon.

Action identifies what operation is requested against or in relation to that
Resource.

Action names SHOULD remain composable with governed Resource identity and
Resource Type. Governance MUST prefer Resource + Action composition over
proliferating implementation-specific permission names.

This artifact does not define a physical data model.

## 10. Action vs Resource Type

Resource Type classifies the governed Resource.

Action classifies the requested operation.

An Action MAY apply to multiple Resource Types when future Entitlement
governance permits that combination. An Action MUST NOT be assumed applicable
to every Resource Type merely because it exists.

Invalid Resource Type + Action combinations MUST fail closed unless later
Entitlement governance explicitly allows them.

## 11. Action vs Lookup

Lookup resolves a requested Resource reference to exactly one valid Governed
Resource or fails closed.

Action describes the operation requested against or in relation to a Resource
after the Resource reference is understood by a trusted deterministic boundary.

Lookup success MUST NOT imply that any Action is authorized.

Internal lookup steps MUST NOT automatically become Principal-facing Actions.

## 12. Action vs Retrieval

Retrieval obtains an already-governed producer artifact represented by a
Governed Resource.

Retrieval is separate from Action unless a future product surface explicitly
requires a Principal-facing business operation for retrieving content. For the
current governed delivery path, retrieval is primarily a trusted internal
control rather than an initial Principal-facing permission.

Retrieval success MUST NOT imply authorization.

## 13. Action vs Authorization Decision

Action is an input to authorization.

Authorization is the deterministic decision process that later evaluates
Principal, Membership, scope, Resource, Action, and Entitlement to produce
ALLOW or DENY.

An Action MUST NOT produce ALLOW by itself.

Unknown or unsupported Action state MUST produce no authorized operation.

## 14. Action vs UI

UI behavior is not authorization vocabulary.

Authorization MUST NOT be derived from:

- visible buttons;
- hidden buttons;
- disabled controls;
- route visibility;
- sidebar entries;
- React state;
- client-side role checks;
- browser state; or
- Website-local display logic.

A UI control MAY provide evidence that a product operation exists. It MUST NOT
establish that the operation is authorized.

## 15. Action vs HTTP / API

HTTP method or route alone MUST NOT define the governed business Action.

The architecture MUST NOT assume:

- GET = VIEW;
- POST = CREATE;
- PUT = MODIFY;
- PATCH = MODIFY; or
- DELETE = DELETE.

One business Action MAY involve multiple technical operations. One endpoint MAY
support different governed business semantics. Requested Action governance must
remain transport-neutral.

## 16. Action vs Runtime Function

Runtime functions, Lambda handlers, service adapters, provider methods, and
application functions are implementation constructs.

They MUST NOT become governed Actions solely because they exist in source code.

A runtime function MAY later enforce or consume a canonical Requested Action
only after separately approved implementation governance.

## 17. Action vs AI Behavior

AI Knowledge Assistant remains a consumer/explainer only.

AI, Bedrock, LLMs, RAG, embeddings, vector search, semantic similarity, or
probabilistic model behavior MUST NOT:

- create Action definitions dynamically;
- infer a broader Action than requested;
- convert user language directly into authority without deterministic mapping;
- invent permissions;
- infer Entitlement;
- override DENY;
- select alternate Resources after denial;
- broaden Client, Organization, Engagement, Workspace, or Resource scope; or
- reinterpret an unauthorized operation as an authorized one.

Any future natural-language-to-Action resolution must be separately governed
and deterministically constrained before authorization reliance.

## 18. Initial Vocabulary Selection Principles

The initial vocabulary MUST be the smallest set sufficient for current product
semantics and downstream Entitlement governance.

An Action may be governed now only when:

- objective repository evidence shows a meaningful product operation;
- the operation is business-semantic rather than implementation-specific;
- it can remain technology-neutral;
- it can be distinguished from Resource, lookup, retrieval, Entitlement, UI,
  API, runtime function, and AI behavior;
- it does not grant authority by existing; and
- unknown or invalid use can fail closed.

Speculative completeness is prohibited.

## 19. Current Read Operations

VIEW is GOVERNED NOW.

VIEW means presenting governed information to an authorized Principal through
an approved consumer boundary.

Evidence includes Executive Dashboard rendering, Website Projection Delivery
Contract consumption, findings and recommendations presentation, dashboard
content sections, and report-like presentation concepts.

VIEW MUST NOT imply retrieval success, download permission, Entitlement, or
access to broader Resource scope.

RETRIEVE is DEFERRED as an initial Principal-facing Action.

Current evidence treats retrieval primarily as a trusted internal acquisition
of an approved producer artifact. Retrieval remains separately governed by EIP
retrieval boundary and Resource lookup governance. A future Principal-facing
RETRIEVE Action may be governed only if product semantics require it.

DOWNLOAD is GOVERNED NOW.

DOWNLOAD means delivering a durable or exportable artifact to an authorized
Principal. Evidence includes Website report/download concepts and synthetic
report download presentation. DOWNLOAD is distinct from VIEW because it
supports exportable possession of a governed artifact.

DOWNLOAD MUST NOT be inferred from VIEW.

## 20. Current Write / Submission Operations

SUBMIT is GOVERNED NOW.

SUBMIT means providing client- or respondent-supplied information into an
approved intake boundary for deterministic processing. Evidence includes
Website assessment submission and Assessment Service assessment request
handling.

SUBMIT MUST NOT authorize mutation of Assessment Service truth, EIP artifacts,
published delivery contracts, or previously produced governed Resources.

UPLOAD is DEFERRED.

Current evidence includes roadmap and pilot references to evidence upload, but
there is insufficient approved runtime evidence to govern UPLOAD as a current
authorization Action. Future evidence-ingestion governance may define it.

CREATE, UPDATE, and MODIFY are DEFERRED.

Current product evidence does not justify broad mutation Actions. Those terms
are too implementation-dependent without separately governed data ownership,
producer mutation boundaries, lifecycle semantics, and Entitlement rules.

## 21. Explanation Operations

EXPLAIN is GOVERNED NOW with a narrow meaning.

EXPLAIN means producing or presenting an explanation of already-authorized
governed context to an authorized Principal through an approved consumer or
trusted runtime boundary.

Evidence includes AI Knowledge Assistant capabilities, explainability-oriented
assessment and executive intelligence artifacts, and product references to
explaining findings, recommendations, scores, and governed context.

EXPLAIN MUST NOT mean:

- compute business truth;
- modify findings;
- recalculate scores;
- change recommendations;
- broaden context;
- infer additional authorization;
- access unauthorized Resources;
- generate authoritative Assessment Service output; or
- generate authoritative EIP output.

## 22. Administrative Operations

ADMINISTER and MANAGE are DEFERRED.

Administrative operations require separate governance over authority
administration, revocation, provisioning, lifecycle control, operator
separation, emergency access, audit, and implementation boundaries.

This artifact does not define administrator roles, admin role hierarchy, RBAC,
ABAC, ACLs, IAM permissions, invitation workflows, approval workflows, or
membership-management behavior.

Future governance MAY define an administrative Action family after the relevant
authority-source and administration models are sufficiently stable.

## 23. Canonical Action Semantics

Canonical Actions MUST be:

- deterministic;
- unambiguous;
- business-semantic;
- technology-neutral;
- versionable;
- auditable; and
- suitable for deterministic authorization evaluation.

Canonical Action semantics MUST NOT be defined by database schema, enum
implementation, JSON schema, API schema, code constants, IAM actions, Cognito
claims, route names, UI labels, or AI interpretation.

The initial governed canonical Actions are:

- VIEW;
- DOWNLOAD;
- SUBMIT; and
- EXPLAIN.

## 24. Action Aliasing

External labels, request labels, UI labels, natural-language phrases, route
names, or integration-specific names MAY require deterministic mapping to one
canonical Action in future implementation.

This artifact does not create implementation mappings.

Ambiguous, conflicting, unsupported, or unrecognized aliases MUST fail closed.

AI or LLM semantic interpretation MUST NOT be the authoritative mapping from an
external label to a canonical Action.

## 25. Unknown / Unsupported Action Semantics

Unknown, unsupported, malformed, ambiguous, conflicting, deprecated, or
unrecognized Action MUST fail closed.

An unknown Action MUST NOT:

- default to VIEW;
- default to a lower privilege;
- inherit another Action;
- map using AI inference;
- map using semantic similarity;
- map using browser behavior;
- map from HTTP method alone; or
- map from route name alone.

No authorization may be granted until a recognized governed Action is
deterministically resolved.

## 26. Resource + Action Applicability

Not every Action applies to every Resource Type.

Future Entitlement governance may define a bounded Resource Type + Action
applicability matrix. This artifact does not create that matrix.

Current conceptual examples:

- VIEW may be meaningful for dashboard delivery, report presentation,
  findings, recommendations, and approved governed content.
- DOWNLOAD may be meaningful for exportable report artifacts.
- SUBMIT may be meaningful for assessment input or approved intake Resources.
- EXPLAIN may be meaningful only for already-authorized governed context.

These examples do not authorize access and do not define Entitlement.

Invalid Resource + Action combinations MUST fail closed.

## 27. Action Versioning

Action vocabulary changes are governed changes.

The following require future governance review:

- adding an Action;
- removing an Action;
- changing Action meaning;
- merging Actions;
- splitting Actions;
- changing Resource applicability;
- changing alias or label semantics; and
- changing fail-closed treatment.

This artifact does not select version storage, schema, registry, API, or
implementation representation.

## 28. Principal Boundary

Requested Action MUST NOT establish Principal identity.

A Principal must be resolved through approved stable Principal mapping
governance before Action can participate in authorization evaluation.

Principal Mapping authority source remains UNRESOLVED.

## 29. Membership / Business Entity Boundary

Requested Action MUST NOT grant business scope.

Membership remains the authoritative relationship between a stable Nguyen AI
Principal and a Governed Business Entity.

Action does not prove:

- Membership;
- Client access;
- Organization access;
- Engagement access;
- Workspace access;
- Resource access; or
- Entitlement.

All applicable scope must still be resolved separately.

## 30. Engagement Boundary

Engagement remains PARTIALLY GOVERNED / DOWNSTREAM.

Action vocabulary may support future Engagement-scoped authorization without
requiring Engagement to become mandatory in this artifact.

This artifact does not define Engagement identity, Engagement authority,
Engagement lifecycle, Engagement administration, or Engagement-specific
Entitlement.

## 31. Workspace Boundary

Workspace remains OPTIONAL / FUTURE.

Current evidence does not justify Workspace as a mandatory governed
authorization abstraction.

Action vocabulary MUST NOT introduce Workspace merely because it is common SaaS
terminology.

## 32. Assessment Service Boundary

Assessment Service remains the sole authoritative deterministic assessment
truth producer.

Requested Action governance MUST NOT permit any consumer to:

- rescore assessments;
- recalculate dimensions;
- change readiness;
- change risk;
- change severity;
- change confidence;
- modify recommendations;
- fabricate assessment truth;
- repair Assessment Service output;
- reinterpret Assessment Service authority; or
- mutate Assessment Service producer artifacts.

SUBMIT may describe sending client-provided assessment input to an approved
intake boundary. It does not authorize mutation of produced assessment truth.

## 33. EIP Boundary

EIP remains the authoritative producer of executive intelligence and Website
Projection Delivery Contracts.

Requested Action governance MUST NOT permit any consumer to:

- fabricate executive intelligence;
- create or recreate projections;
- synthesize Website Projection Delivery Contracts;
- override publication;
- override freshness;
- override classification;
- override compatibility;
- repair lineage;
- reinterpret EIP authority; or
- reconstruct upstream artifacts.

VIEW, DOWNLOAD, or EXPLAIN may later be evaluated against EIP-produced
governed Resources only through separate Entitlement governance.

## 34. Website Boundary

Website remains presentation-only.

Website may request a future Action, but:

browser-requested Action != authorized Action.

The trusted server-side authorization boundary must validate and canonicalize
the requested Action deterministically before relying on it.

This artifact does not implement that behavior.

## 35. Trusted Runtime Boundary

The `aws-ai-knowledge-assistant` repository remains the repository ownership
domain for a future separate deterministic trusted logical service.

This artifact MUST NOT:

- authorize runtime implementation;
- make the AI assistant itself the Action authority;
- route authorization through Bedrock;
- make LLM interpretation authoritative; or
- assign a concrete Action authority source.

Future enforcement must remain deterministic and isolated from probabilistic AI
execution.

## 36. AI Authority Boundary

AI Knowledge Assistant remains consumer/explainer only.

AI, Bedrock, LLMs, RAG, embeddings, vector search, and semantic similarity have
no authority to define, resolve, broaden, substitute, or authorize Actions.

AI may only receive or explain governed context after deterministic
authorization succeeds and a separately approved consumer boundary permits
that use.

## 37. Fail-Closed Model

Future deterministic authorization MUST produce DENY or no authorized operation
for:

- missing Action;
- unknown Action;
- malformed Action;
- ambiguous Action;
- conflicting Action;
- unsupported Action;
- deprecated Action;
- invalid Resource + Action combination;
- unavailable Action authority or vocabulary version; and
- failed deterministic canonicalization.

There MUST be no fallback to:

- VIEW;
- previous Action;
- default Action;
- least-looking Action;
- UI-derived Action;
- HTTP-derived Action;
- route-derived Action; or
- AI-inferred Action.

## 38. Audit / Privacy Governance

Future deterministic Action resolution and authorization should produce audit
evidence sufficient to support governance review.

Audit context should include, where applicable:

- timestamp;
- verified Principal reference;
- Governed Business Entity reference;
- Resource reference;
- canonical Requested Action;
- future authorization outcome;
- reason classification;
- Action vocabulary or governance version reference; and
- correlation or request identifier.

Audit evidence MUST NOT require logging raw tokens, credentials, secrets,
unnecessary sensitive payloads, unnecessary assessment content, or unnecessary
AI context.

This artifact does not select audit storage or logging technology.

## 39. Technology Neutrality

This artifact does not select:

- DynamoDB;
- S3;
- SQL;
- filesystem;
- database;
- Redis;
- API Gateway route design;
- Lambda route design;
- Cognito groups;
- custom claims;
- IAM identities;
- IAM actions;
- RBAC;
- ABAC;
- ACL;
- policy engine;
- CRM;
- Bedrock;
- LLM;
- RAG;
- embeddings; or
- vector database.

Technology may appear only as existing evidence, prohibited authority, or
explicitly unselected implementation detail.

## 40. Authority Status

| Concept | Status | Notes |
| --- | --- | --- |
| Authentication evidence | GOVERNED / CURRENT IMPLEMENTATION EVIDENCE | Cognito evidence exists, but authentication is not authorization. |
| Stable Principal | GOVERNED | Stable Principal semantics are approved. |
| Principal Mapping semantics | GOVERNED | Mapping semantics are approved. |
| Principal Mapping authority source | UNRESOLVED | No concrete authority source selected. |
| Governed Business Entity | GOVERNED CONCEPTUALLY | Client / Organization identity semantics are approved conceptually. |
| Client / Organization authority source | UNRESOLVED | No concrete authority source selected. |
| Membership semantics | GOVERNED CONCEPTUALLY | Membership relationship semantics are approved. |
| Membership concrete authority source | UNRESOLVED | Requirements are governed; concrete source is unresolved. |
| Governed Resource identity | GOVERNED CONCEPTUALLY | Resource identity semantics are approved. |
| Resource lookup semantics | GOVERNED CONCEPTUALLY | Lookup resolves one Resource or fails closed. |
| Resource authority source | UNRESOLVED | No concrete Resource authority source selected. |
| Requested Action concept | GOVERNED | This artifact defines Requested Action semantics. |
| Requested Action vocabulary | GOVERNED TO BOUNDED CURRENT EVIDENCE | VIEW, DOWNLOAD, SUBMIT, and EXPLAIN are governed now. |
| RETRIEVE | DEFERRED | Currently treated as internal retrieval unless future product semantics require it. |
| UPLOAD | DEFERRED | Evidence insufficient for current authorization vocabulary. |
| CREATE / UPDATE / MODIFY | DEFERRED | Mutation semantics require future governance. |
| ADMINISTER / MANAGE | DEFERRED | Administration semantics require future authority administration governance. |
| Entitlement semantics | DOWNSTREAM / PARTIALLY GOVERNED | Concept exists; rules are not governed here. |
| Entitlement authority source | UNRESOLVED / DOWNSTREAM | No concrete authority source selected. |
| Engagement | PARTIALLY GOVERNED / DOWNSTREAM | Not mandatory for this artifact. |
| Workspace | OPTIONAL / FUTURE | Not currently required. |
| Persistence | UNRESOLVED | No persistence selected. |
| Trusted authorization service contract | DOWNSTREAM | Still premature until Entitlement governance. |
| Implementation | UNAUTHORIZED | This artifact authorizes no implementation. |

## 41. Entitlement Dependency

Completion of Requested Action / Permission Vocabulary Governance v1 makes
Entitlement Authority Source Governance v1 the likely next semantic dependency,
provided no independent review identifies a newly blocking prerequisite.

Remaining prerequisites before implementation include:

- Entitlement semantics and authority-source governance;
- broader authority administration and revocation governance;
- concrete authority-source decisions as needed;
- trusted authorization service contract governance;
- authorization persistence review;
- EIP retrieval integration governance;
- Website governed delivery integration governance;
- AI authorized-context delivery governance; and
- explicit implementation authorization.

This artifact does not create Entitlement rules.

## 42. Remaining Governance Gaps

The following remain unresolved or downstream:

- Principal Mapping authority source;
- Client / Organization authority source;
- Membership concrete authority source;
- Resource authority source;
- Entitlement authority source;
- Entitlement rules;
- Resource + Action applicability matrix;
- Engagement identity and scope where needed;
- Workspace identity and scope if future evidence justifies it;
- authority administration and revocation;
- authorization persistence;
- trusted authorization service contract;
- EIP retrieval mechanism;
- Website governed delivery integration;
- AI authorized-context delivery;
- deterministic route isolation;
- security and IAM implementation boundary; and
- runtime implementation approval.

## 43. Implementation Gate

Requested Action / Permission Vocabulary Governance v1 DOES NOT AUTHORIZE:

- authorization implementation;
- Action mapping implementation;
- Entitlement implementation;
- Resource authorization;
- persistence;
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
- AWS runtime changes;
- Bedrock changes;
- AI changes; or
- deployment.

Implementation remains blocked by downstream governance and explicit approval
in the owning repository.

## 44. Acceptance Criteria

This artifact is acceptable when:

- Requested Action is defined as a business-level operation description;
- permission terminology is separated from grants of authority;
- Action is separated from Entitlement;
- Action is separated from Resource and Resource Type;
- Action is separated from lookup, retrieval, authorization decision, UI, HTTP,
  API, runtime function, and AI behavior;
- the initial vocabulary is evidence-based and minimal;
- VIEW, DOWNLOAD, SUBMIT, and EXPLAIN are governed with bounded meanings;
- RETRIEVE, UPLOAD, CREATE, UPDATE, MODIFY, ADMINISTER, and MANAGE are deferred
  where evidence or governance is insufficient;
- unknown or invalid Actions fail closed;
- producer and consumer boundaries are preserved;
- technology neutrality is preserved;
- no implementation is authorized; and
- Entitlement governance remains downstream.
