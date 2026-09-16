# Trusted Authorization Assessment Submission Business Context Governance v1

## 1. Purpose

This artifact governs the minimum Assessment Submission business-context
semantics required before provisional Assessment Submission resource
establishment can consume an authoritative Business Entity binding.

It translates the human-approved product/domain decision that every Assessment
Submission occurs within a pre-established governed Assessment Engagement.

It defines governance only. It does not implement an Assessment Engagement
source, business-context source, runtime integration, persistence, permission
evaluation, target production, lifecycle mutation, or production authority.

## 2. Scope

This artifact governs only the bounded business-context question:

What finite, non-circular governed fact supplies the authoritative Business
Entity B for a new Assessment Submission?

The selected answer is a current, legitimately selected, pre-established
governed Assessment Engagement E that is authoritatively bound to exactly one
current Business Entity B.

This artifact is not:

- general Client Engagement governance;
- CRM governance;
- general Workspace governance;
- portal governance;
- billing governance;
- contract governance;
- project-management governance;
- participant-management governance;
- general Assessment lifecycle governance;
- production implementation architecture.

## 3. Human-Approved Product Decision

The human-approved product/domain architecture is:

- every Assessment Submission occurs within a pre-established governed
  Assessment Engagement;
- each Assessment Engagement is authoritatively bound to exactly one Business
  Entity;
- one Business Entity may have multiple Assessment Engagements;
- the Assessment Engagement supplies the authoritative Business Entity context
  required before provisional Assessment Submission establishment.

Conceptually:

```text
authoritative current Business Entity B
    -> governed Assessment Engagement E
    -> authoritative immutable E -> B binding
    -> legitimate current operation context E
    -> Assessment Submission Business Context B
    -> provisional Assessment Submission establishment
```

This decision supplies domain intent. It does not by itself implement any
authority source or grant production authority.

## 4. Definitions

Business Entity B means a governed, current Business Entity resolved under
separate Business Entity authority.

Assessment Engagement E means a governed domain context under which Assessment
Submissions are conducted for exactly one Business Entity.

Assessment Submission means the protected Assessment Submission resource whose
provisional lifecycle is governed separately.

Assessment Submission Business Context means the authoritative Business Entity
binding derived from a legitimate current Assessment Engagement and supplied to
provisional Assessment Submission establishment.

Assessment Engagement Request means candidate input asking that an engagement
be created, resolved, selected, or used. A request is not authority.

Assessment Engagement Establishment Authority means the narrow logical
responsibility that may establish governed Assessment Engagement facts under
independently valid establishment authority.

Engagement Context Legitimacy means the separate fact that the current
operation or request legitimately operates within the resolved Assessment
Engagement.

BUSINESS_CONTEXT_READY means only that a legitimate current Assessment
Engagement has supplied authoritative B for provisional Assessment Submission
establishment. It does not mean SUBMIT is authorized.

## 5. Authority Boundaries

The following distinctions are mandatory:

- Business Entity existence is not Assessment Engagement existence.
- Assessment Engagement existence is not Assessment Engagement context
  legitimacy.
- Assessment Engagement context legitimacy is not Assessment Submission
  permission.
- Membership is not Assessment Engagement authority.
- Entitlement is not Assessment Engagement authority.
- Authentication is not Assessment Engagement authority.
- Caller-selected B is not authoritative B.
- Caller-selected E is not authoritative E context.
- Assessment Service scoring authority is not Assessment Engagement authority.
- Website or portal presentation is not Assessment Engagement authority.
- Resource Identity is not Assessment Engagement context legitimacy.
- Target legitimacy is not Business Entity binding.
- Resource allocation is not resource or business-context authority.

No downstream permission fact may bootstrap the upstream engagement authority
needed to establish business context.

## 6. Assessment Engagement Domain Model

An Assessment Engagement is narrowly defined as a governed domain context under
which Assessment Submissions are conducted for exactly one Business Entity.

Minimum conceptual properties are:

- stable engagement identity E;
- authoritative binding to exactly one B;
- engagement currentness or lifecycle;
- establishment provenance;
- historical traceability.

This artifact does not select a database, schema, cloud service, API, route,
storage key, or implementation representation for E.

## 7. Engagement Identity

E must have a stable identity sufficient for trusted resolution and audit.

Identifier allocation is distinct from authority. Generating or receiving an
engagement reference does not establish that E exists, is current, belongs to
B, or is legitimate for the current request.

Engagement identity must fail closed when it is malformed, unknown, ambiguous,
conflicting, stale, or unsupported by required establishment evidence.

## 8. Business Entity Dependency

Before E may be authoritatively established for B, B must itself be a
governed, current Business Entity.

Existing Business Entity authority may establish that B exists and currently
resolves. It does not establish:

- E exists;
- E belongs to B;
- E is current;
- this request legitimately operates within E;
- a Principal may submit within E.

Business Entity existence is a prerequisite, not a substitute for engagement
establishment.

## 9. Cardinality

An Assessment Engagement must bind to exactly one Business Entity:

```text
E1 -> B1
```

One Business Entity may have zero or more Assessment Engagements:

```text
B1
  -> E1
  -> E2
  -> E3
```

The following is invalid and must fail closed:

```text
E1 -> B1
E1 -> B2
```

Multiple engagements for the same Business Entity are permissible for distinct
assessment periods, scopes, reassessments, or business engagements. Business
Entity equality alone does not prove that the correct E was selected.

## 10. Engagement Establishment Authority

Assessment Engagement Establishment Authority is the narrow logical
responsibility that may establish the governed engagement fact required by this
artifact.

It may establish:

- E identity or context;
- E -> B binding;
- initial engagement currentness or lifecycle;
- required establishment provenance.

It must not establish:

- Principal identity;
- Membership;
- Entitlement;
- requested action;
- target legitimacy;
- Assessment Submission permission;
- ALLOW or DENY;
- Assessment Submission lifecycle transition;
- production authority.

## 11. Terminating Authority Basis

The selected establishment model is governed administrative establishment.

Administrative does not mean:

- administrator account;
- super-admin;
- founder;
- owner;
- employee;
- cloud principal;
- standing privileged identity;
- authentication-provider group.

Administrative means a bounded governed administrative business action
performed under independently valid establishment authority.

The establishment authority must terminate in accountable business
authorization plus independently verifiable evidence scoped specifically to:

- the Assessment Engagement;
- the Business Entity binding;
- the establishment action;
- the applicable governance or version context.

The following are prohibited as terminating bases:

- self-authorization;
- circular authorization;
- infinite authority recursion;
- founder shortcut;
- owner shortcut;
- company-status shortcut;
- authentication shortcut;
- infrastructure shortcut;
- server-side-code shortcut;
- Membership shortcut;
- Entitlement shortcut.

It is insufficient to say that an authorized administrator establishes E.
Administrative identity itself is not the terminating basis. The legitimacy of
the establishment action must derive from independently governed authority
evidence.

Concrete participant and source realization remain open.

## 12. Engagement Request vs Authority

An Assessment Engagement Request is not a Governed Assessment Engagement.

A client, user, system, or workflow may request:

```text
start an Assessment Engagement for B
```

The request may contain candidate E, candidate B, scope, or metadata. None of
those values becomes authoritative merely because it appears in the request.

A request may initiate an authority process. It may not complete that authority
process by assertion.

## 13. Engagement Currentness / Minimum Lifecycle

A governed Assessment Engagement must be current and eligible to supply
Business Entity context for a new Assessment Submission.

This artifact governs only minimum lifecycle semantics:

- not-yet-authoritative or candidate engagement;
- current and eligible engagement;
- no-longer-current engagement.

Closed, revoked, stale, expired, cancelled, or otherwise non-current
engagements must fail closed for new Assessment Submission business-context
derivation.

Exact lifecycle state names, transition mechanisms, storage mechanics, and
workflow implementation remain unresolved.

## 14. Immutable E -> B Binding

After authoritative establishment, E -> B is immutable.

An established engagement must not be rebound from:

```text
E1 -> B1
```

to:

```text
E1 -> B2
```

If the original B binding is materially incorrect, the incorrect engagement
must cease to be valid for new context according to governed lifecycle or
correction semantics, and a new governed engagement must be established with
the correct B.

This artifact does not specify storage mutation mechanics.

## 15. Historical Traceability

E -> B immutability protects:

- historical assessment attribution;
- authorization reproducibility;
- report provenance;
- resource ownership consistency;
- prevention of cross-Business-Entity rebinding;
- prevention of retroactive authorization reinterpretation.

Closing or revoking E does not erase historical truth that E was bound to B.
Currentness and historical provenance are distinct.

Historical Assessment results must remain attributable to the Business Entity
context under which they were created.

## 16. Submission -> Engagement Invariant

Every Assessment Submission belongs to exactly one governed Assessment
Engagement.

No Assessment Submission may obtain authoritative Business Entity context
without an Assessment Engagement under this product model.

Future realization should preserve engagement reference E as provenance and
context for the Assessment Submission. The existing provisional lifecycle proof
records B directly and does not yet carry E; this artifact does not modify that
proof.

## 17. Engagement Resolution

A future trusted authority must independently resolve candidate E to governed
engagement facts.

Minimum resolved facts needed conceptually are:

- E identity;
- authoritative B;
- currentness or lifecycle status;
- establishment provenance sufficient for trust;
- applicable governance or version evidence where required.

Caller-provided E is only a selector. It may ask trusted authority to resolve
E, but it cannot establish that E exists, is current, belongs to B, or is
legitimate for the current request.

This artifact does not select the implementation source, persistence mechanism,
or runtime interface for engagement resolution.

## 18. Engagement Context Legitimacy

E exists is not the same as this request legitimately operates within E.

A separate engagement-context legitimacy fact is required before E may supply
Business Entity context for a new Assessment Submission.

This fact must not be established solely by:

- caller-selected E;
- caller-selected B;
- Membership;
- Entitlement;
- Business Entity match;
- session or browser state;
- route, payload, or query parameter;
- infrastructure identity.

The concrete producer of engagement-context legitimacy remains open.

## 19. Business Context Derivation

The future conceptual derivation is:

```text
candidate engagement reference E
    -> trusted engagement resolution
    -> current governed E
    -> independent E-context legitimacy
    -> authoritative immutable E -> B
    -> Assessment Submission Business Context
    -> provisional Assessment Submission establishment
```

The business-context boundary must provide at least authoritative B plus
sufficient provenance tying that B to E, engagement currentness, legitimate
engagement context, and applicable governance or version evidence as required.

This derivation creates business context. It does not create permission.

## 20. Permission Separation

Assessment Engagement business context does not authorize SUBMIT.

Permission remains downstream and requires the separately governed chain of
authenticated subject, principal mapping, resource/action applicability,
Business Entity, Membership, Entitlement, evaluator composition, and any
required final composition and enforcement.

BUSINESS_CONTEXT_READY is not ALLOW.

## 21. Membership / Entitlement Separation

Membership may later prove that P is associated with authoritative B. It does
not establish:

- E;
- E -> B;
- E currentness;
- E context legitimacy;
- Assessment Submission ownership.

Entitlement remains downstream permission evidence. It must not establish:

- E;
- E -> B;
- business context.

The following circularity is invalid:

```text
need B to establish R
need R to evaluate Entitlement
need Entitlement to establish B
```

## 22. Authentication Separation

Authentication establishes verified subject provenance. It does not establish:

- E;
- B;
- E -> B;
- engagement currentness;
- engagement context legitimacy.

Authentication-provider organization claims do not automatically become
business authority.

## 23. Portal / Website Separation

Website and Client Engagement Portal experiences remain presentation consumers.

They may display engagements, allow a user to select candidate E, and submit
candidate E to trusted server-side logic.

They may not establish:

- E;
- E -> B;
- E currentness;
- E context legitimacy;
- Assessment Submission permission.

Browser state, local storage, page state, URL structure, or UI selection is not
Assessment Engagement authority.

## 24. Assessment Service / EIP Separation

The Assessment Service remains authoritative for deterministic assessment and
business decision truth where separately governed.

That role does not automatically grant:

- Assessment Engagement establishment authority;
- Business Entity ownership authority;
- engagement-context legitimacy authority.

The Executive Intelligence Platform remains a consumer and projection producer
under its existing governance. It does not establish Assessment Engagement
business context.

## 25. Resource Identity / Target / Allocation Separation

This artifact does not make Assessment Engagement a protected resource class or
equivalent authorization resource category.

Resource Identity remains separate and is not modified by this artifact.
Assessment Submission R remains the current protected resource.

Assessment Engagement business context does not establish Assessment Submission
target legitimacy. Target provenance remains independently governed.

Resource-reference allocation remains distinct. Identifier allocation is not E
authority, B authority, permission, target legitimacy, or business-context
authority.

Whether E later becomes a domain context, authority-source fact, new protected
resource category, or another source type remains open.

## 26. Same-B Substitution

Threat:

```text
B1 has E1 and E2
P is valid for B1
the intended operation is E1
caller substitutes E2
```

Because both engagements map to B1, Business Entity match alone cannot detect
the substitution.

Defense:

- trusted engagement resolution must resolve the supplied E;
- independent engagement-context legitimacy must prove that the current
  operation legitimately operates within that E;
- Membership or Business Entity match must not repair missing E-context
  legitimacy.

## 27. Cross-B Substitution

Threat:

```text
P belongs to B1
caller selects E2
trusted E resolution determines E2 -> B2
```

The architecture must preserve B2. It must not replace B2 with B1 because P has
Membership in B1.

Downstream Membership and Entitlement must evaluate against authoritative B2
and fail closed when P lacks required authority.

## 28. Stale / Closed Engagement Handling

Threat:

```text
caller supplies historically valid E
E is closed, revoked, stale, expired, or no longer eligible
```

Trusted resolution must identify E as non-current. Non-current E must not
supply Business Entity context for a new Assessment Submission.

Historical attribution remains preserved.

## 29. Fail-Closed Rules

Business-context derivation must fail closed if:

- E is malformed;
- E is unknown;
- E is ambiguous;
- E is conflicting;
- E is non-current;
- E is closed, revoked, stale, expired, or ineligible;
- E -> B is malformed;
- E resolves to zero Business Entities;
- E resolves to multiple Business Entities;
- B is unknown;
- B is non-current;
- engagement establishment evidence is invalid;
- engagement context legitimacy is missing;
- engagement context legitimacy is invalid;
- required governance or version evidence is unavailable;
- source evidence is circular or non-terminating;
- any required authority fact is derived only from caller assertion.

No fallback Business Entity is permitted.

Prohibited fallback sources include:

- default B;
- first Membership B;
- only Membership B;
- last-used B;
- session B;
- browser B;
- route B;
- environment B;
- configuration B;
- cloud account B;
- organization payload B.

No fallback engagement is permitted.

Prohibited fallback engagements include:

- first engagement;
- only engagement;
- latest engagement;
- session engagement;
- browser engagement;
- route engagement;
- cached engagement.

Caller or runtime input must not dynamically register an engagement as
authoritative merely because it was requested.

## 30. Decision Table

| E known? | E current? | E has exactly one authoritative B? | B current? | E-context legitimacy present? | Outcome |
| --- | --- | --- | --- | --- | --- |
| No | N/A | N/A | N/A | N/A | FAIL CLOSED |
| Yes | No | N/A | N/A | N/A | FAIL CLOSED |
| Yes | Yes | No, none | N/A | N/A | FAIL CLOSED |
| Yes | Yes | No, multiple or conflicting | N/A | N/A | FAIL CLOSED |
| Yes | Yes | Yes | No | N/A | FAIL CLOSED |
| Yes | Yes | Yes | Yes | No | FAIL CLOSED |
| Yes | Yes | Yes | Yes | Yes | BUSINESS_CONTEXT_READY |

BUSINESS_CONTEXT_READY is not ALLOW. It means only that authoritative B is
available for provisional Assessment Submission establishment.

## 31. Threat Model

Caller-B laundering:
Caller-provided B must not become authoritative by schema validation,
Business Entity lookup, Membership validation, Entitlement validation,
server-side copying, persistence, or resource creation.

Caller-E laundering:
Caller-provided E is a selector only. It cannot establish E existence,
currentness, B binding, or context legitimacy.

Same-B engagement substitution:
B match is insufficient where B has multiple engagements. E-context legitimacy
is required.

Cross-B engagement substitution:
Trusted E -> B must be preserved. Membership in another B must not overwrite
the resolved B.

Stale or closed engagement reuse:
Historically valid but non-current E must not supply context for new
submissions.

Engagement rebinding:
E -> B must not be silently changed from B1 to B2 after authoritative
establishment.

Membership-derived B:
Membership may constrain downstream permission but must not originate E or B
for submission context.

Entitlement circularity:
Entitlement must not establish B where B is needed before resource and
Entitlement evaluation.

Principal-derived B:
Principal identity does not determine Assessment Engagement context.

Portal, session, or browser laundering:
Presentation state is not authority.

Infrastructure authority laundering:
Cloud account, execution role, API gateway, database ownership, or
authentication-provider identity is not business authority.

Assessment Service authority expansion:
Scoring authority does not automatically become engagement establishment or
business-context authority.

AI or agent authority laundering:
Model output, prompt content, agent reasoning, or multi-agent consensus cannot
establish E, B, E -> B, currentness, context legitimacy, or permission.

Ambiguous engagement resolution:
Ambiguous E must fail closed.

Conflicting E -> B evidence:
Conflicting Business Entity evidence for E must fail closed.

Missing engagement-context legitimacy:
E existence and B binding are insufficient without proof that the current
operation legitimately operates within E.

TOCTOU:
Engagement currentness may change between resolution, authorization, and
consequential mutation. This risk is deferred and must be addressed by future
architecture before production enforcement.

## 32. Audit / Evidence Requirements

Future realization must preserve enough evidence to explain:

- which E was used;
- which B E was bound to;
- whether E was current;
- what establishment provenance supported E;
- what engagement-context legitimacy supported this request;
- what governance or version basis applied.

This artifact does not select storage format, retention mechanics, or audit
system implementation.

## 33. Traceability

Future realization must support conceptual traceability:

```text
Assessment Submission R
    -> Assessment Engagement E
    -> Business Entity B
    -> engagement establishment provenance
    -> applicable governance
```

This traceability requirement does not modify the existing provisional
Assessment Submission lifecycle proof.

## 34. AI / Agent Boundary

AI, LLMs, agents, multi-agent consensus, MCP, prompts, and model output cannot
establish:

- E;
- B;
- E -> B;
- engagement currentness;
- engagement context legitimacy;
- permission.

AI may later explain governed facts. It does not originate authority.

## 35. AWS / Infrastructure Boundary

Cloud accounts, infrastructure ownership, execution roles, identity providers,
API gateways, serverless functions, databases, CDNs, and infrastructure
configuration do not themselves establish business authority.

They may host or transport future governed evidence only when separately
authorized by governance.

## 36. Founder / Owner Boundary

Founder status, company ownership, repository ownership, administrator status,
employee status, consultant status, or client administrator status does not
automatically confer Assessment Engagement establishment authority.

Concrete people, roles, and participants remain unresolved. Logical
responsibility is not a standing human or infrastructure privilege.

## 37. Security Invariants

The following invariants are mandatory:

1. E binds to exactly one B.
2. B may have zero or more E.
3. E -> B binding is immutable after authoritative establishment.
4. Caller B is not authority.
5. Caller E is not authority.
6. E existence is not E-context legitimacy.
7. E-context legitimacy is not permission.
8. Membership is not E authority.
9. Entitlement is not E authority.
10. Authentication is not E authority.
11. Business Entity existence is not E establishment.
12. Portal selection is not authority.
13. Assessment Service scoring authority is not E authority.
14. Resource Identity is not E-context legitimacy.
15. Target legitimacy is not E-context legitimacy.
16. Resource allocation is not business-context authority.
17. Closed, revoked, stale, or otherwise non-current E cannot supply context
    for new submissions.
18. Every Assessment Submission requires exactly one governed E.
19. Historical E -> B attribution survives closure or revocation.
20. BUSINESS_CONTEXT_READY is not ALLOW.

## 38. Existing Governance Dependencies

This artifact relies on existing governance principles rather than restating
their full content.

Relevant existing governance includes:

- Business Entity authority source governance for B existence and currentness;
- Membership authority governance for P-to-B relationship evidence;
- Entitlement semantics and authority governance for downstream permission
  evidence;
- Resource Identity and governed lookup governance for protected resource
  resolution;
- resource-reference provenance governance for R separation;
- Assessment Submission resource lifecycle governance for provisional
  establishment after authoritative B is available;
- resource/action applicability governance for action-to-resource-class
  applicability;
- administrative mutation and revocation ownership governance for general
  administrative authority discipline;
- assignment authority and source ownership governance where reusable;
- terminating authority basis governance for finite, non-circular authority
  chains;
- root and recovery governance only where generally applicable to terminating
  authority, scope, minimization, and fail-closed behavior.

Recovery-specific semantics are not imported merely because they exist.

## 39. Open Questions / Deferred Decisions

The following remain open or deferred:

- concrete Assessment Engagement authority source;
- concrete establishment participants;
- operational establishment workflow;
- engagement identifier allocator;
- engagement persistence;
- engagement lifecycle enumeration;
- engagement-context legitimacy producer;
- participant assignment;
- real business-context source implementation;
- real authentication producer;
- real capability producer;
- real target producer;
- Assessment Submission lifecycle awareness downstream;
- governed version-context provenance;
- final composer;
- enforcement;
- TOCTOU controls;
- runtime integration;
- production authority.

Concrete production authority source ownership is unresolved. This artifact
does not select any database, cloud service, authentication system, website,
Assessment Service component, runtime function, or account as the production
authority source.

Separation of duties is not universally imposed here. Whether particular
Assessment Engagement establishment or correction operations require separation
of duties is risk- and operation-specific and remains unresolved.

Participant assignment is separate from E -> B authority.

Potential future engagement attributes such as assessment scope, methodology,
commercial terms, dates, participants, billing, and reports are outside this
artifact unless strictly required for B authority.

## 40. Production Non-Grants

Production Assessment Engagement Authority: NOT GRANTED.

Production Assessment Engagement Establishment: NOT GRANTED.

Production Assessment Engagement Source: NOT GRANTED.

Production Business Context Authority: NOT GRANTED.

Production Business Context Source: NOT GRANTED.

Production Resource Lifecycle: NOT GRANTED.

Production Resource Integration: NOT GRANTED.

Production Authentication: NOT GRANTED.

Production Capability Integration: NOT GRANTED.

Persistence: NOT GRANTED.

Runtime Integration: NOT GRANTED.

Deployment: NOT GRANTED.

Production Authority: NOT GRANTED.

## 41. Implementation Non-Grant

This artifact does not grant implementation authority.

After governance creation, a separate strict read-only adversarial governance
conformance review is required.

Only after successful conformance review and human commit approval may this
governance artifact be committed.

Only after committed governance may a separate implementation-authorization
review determine whether bounded non-production implementation is justified.

This artifact does not authorize modifying any implementation repository,
Resource Identity, resource classes, Membership, Entitlement, evaluator,
Applicability, target producer, resource allocation, authentication,
capability integration, final composer, enforcement, lifecycle mutation,
persistence, runtime, deployment, or production authority.

## 42. Governance Decision Summary

The governed Assessment Submission business-context model is:

```text
current governed Assessment Engagement E
    + immutable authoritative E -> B
    + current governed Business Entity B
    + independent E-context legitimacy
    -> BUSINESS_CONTEXT_READY
    -> B may be consumed by provisional Assessment Submission establishment
```

This model preserves:

- finite Business Entity binding through Assessment Engagement;
- engagement currentness as a prerequisite for new submissions;
- immutable historical E -> B traceability;
- separation between business context, target legitimacy, and permission;
- fail-closed behavior for missing, ambiguous, conflicting, stale, circular, or
  caller-derived authority;
- no production authority grant.

The next valid gate is strict read-only adversarial governance conformance
review of this artifact.
