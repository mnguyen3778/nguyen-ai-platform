# Trusted Authorization Assessment Engagement Context Legitimacy Governance v1

## 1. Purpose

This artifact governs the authority semantics for Assessment Engagement context
legitimacy.

It defines the bounded governance contract for:

- Assessment Engagement Participation;
- trusted current-attempt-to-Assessment-Engagement binding; and
- their exact-Engagement conjunction into Assessment Engagement context
  legitimacy.

It exists to complete the authority gap identified by Trusted Authorization
Assessment Submission Business Context Governance v1:

```text
candidate E
    -> trusted Assessment Engagement resolution
    -> current governed E
    -> immutable authoritative E -> B
    -> independent E-context legitimacy
    -> BUSINESS_CONTEXT_READY
```

This artifact is governance only. It does not implement Participation,
attempt-binding derivation, context-legitimacy composition, Business Context
derivation, runtime integration, persistence, deployment, or production
authority.

## 2. Scope

This artifact governs only the engagement-context legitimacy question:

What finite, non-circular governed facts prove that the current Assessment
Submission authorization attempt legitimately operates within a specific
resolved current Assessment Engagement E?

The governed answer is:

```text
current authoritative Participation(P,E)
    + current trusted Binding(A,E)
    + exact E match
    + current resolved E
    -> E_CONTEXT_LEGITIMATE(P,A,E)
```

Where:

- P is the authoritatively resolved Nguyen AI Principal;
- A is the current bounded authorization attempt or evaluation context; and
- E is the exact current governed Assessment Engagement resolved by the
  Assessment Engagement authority source.

This artifact is not:

- Membership governance;
- Entitlement governance;
- general portal/session governance;
- general Client Engagement governance;
- Assessment Engagement establishment governance;
- Business Context source implementation;
- Assessment Submission lifecycle implementation;
- target provenance governance;
- Resource Identity governance;
- final authorization/evaluator governance; or
- production implementation architecture.

## 3. Binding Human Product Decision

The human-approved product/domain decision is:

Every authenticated Principal who may operate within an Assessment Engagement
must have a current, explicit, pre-established governed Assessment Engagement
Participation relationship with that exact Assessment Engagement.

Every Assessment Submission authorization attempt must additionally possess a
trusted current-attempt-to-Assessment-Engagement binding identifying the exact
Assessment Engagement under which that attempt is operating.

E-context legitimacy requires both:

1. current governed Participation(P,E); and
2. current trusted Binding(A,E);

with both facts referring to the exact same resolved current E.

Same Business Entity is not sufficient.

This establishes engagement context only. It does not establish Membership,
Entitlement, permission, target legitimacy, BUSINESS_CONTEXT_READY by itself,
ALLOW, DENY, runtime authority, persistence authority, or production authority.

## 4. Definitions

Assessment Engagement E means the governed domain context under which
Assessment Submissions are conducted for exactly one Business Entity B, as
governed by Assessment Submission Business Context Governance v1.

Assessment Engagement Participation means the governed standing relationship
between Principal P and Assessment Engagement E establishing that P currently
has engagement-context standing within E.

Assessment Engagement Participation Authority means the narrow logical
authority category that may establish, change where separately valid, revoke,
or otherwise govern Participation relationships within its bounded scope.

Authorization Attempt A means the current bounded authorization evaluation or
attempt context for a protected Assessment Submission operation. A need not be a
persistent identifier unless future governance selects one.

Trusted Current-Attempt Binding means the bounded authority fact Binding(A,E)
answering which exact pre-established Assessment Engagement the current
authorization attempt is operating under.

E_CONTEXT_LEGITIMATE(P,A,E) means the derived governed fact that, for current
Principal P and current authorization attempt A, the attempt legitimately
operates within exact current Assessment Engagement E at the engagement-context
level.

Candidate E means caller- or flow-supplied engagement intent. Candidate E is a
selector or request value only. It is not authority.

## 5. Core Invariant

E_CONTEXT_LEGITIMATE(P,A,E) may exist only if all of the following are true:

- P is authoritatively resolved;
- E is authoritatively resolved;
- E is current;
- E is authoritatively and immutably bound to exactly one Business Entity B;
- Participation(P,E) is current and authoritative;
- Binding(A,E) is current and authoritative;
- Participation and Binding reference the exact same E;
- required provenance/currentness evidence is valid; and
- no required authority fact is missing, ambiguous, conflicting, stale,
  unsupported, or derived only from caller assertion.

E_CONTEXT_LEGITIMATE(P,A,E) establishes engagement context only.

It does not mean:

- P may SUBMIT;
- P may VIEW;
- P may DOWNLOAD;
- P may EXPLAIN;
- P has Entitlement;
- R is a legitimate target;
- BUSINESS_CONTEXT_READY exists;
- ALLOW; or
- DENY.

## 6. Participation Semantics

Assessment Engagement Participation is a governed standing relationship:

```text
Principal P
    <->
Assessment Engagement E
```

It means:

Principal P has current engagement-context standing within exact
pre-established Assessment Engagement E.

Participation must be:

- E-specific;
- Principal-specific;
- scoped;
- current;
- revocable;
- auditable;
- provenance-preserving; and
- non-universal.

Participation must not be wildcard authority. This artifact does not create:

```text
P -> ALL ENGAGEMENTS
```

or:

```text
administrator -> ALL PARTICIPATION
```

## 7. Participation Cardinality

The permitted cardinality is:

```text
P -> zero, one, or multiple E
E -> zero, one, or multiple P
```

No one-to-one Participation relationship is imposed.

A Principal may legitimately participate in multiple Assessment Engagements.

Multiple Principals may legitimately participate in one Assessment Engagement.

Participation cardinality does not change the existing Assessment Engagement
cardinality:

```text
E -> exactly one B
B -> zero or multiple E
```

## 8. Participation Is Not Membership

Membership(P,B) does not imply Participation(P,E) merely because E -> B.

Example:

```text
E1 -> B1
E2 -> B1
Membership(P,B1)
Participation(P,E1)
```

The above does not imply:

```text
Participation(P,E2)
```

Membership in a Business Entity does not automatically confer participation in
every Assessment Engagement belonging to that Business Entity.

This is a mandatory same-B substitution defense.

## 9. Participation Is Not Entitlement

Participation establishes standing in E.

Entitlement establishes bounded action authority.

Participation must never imply:

- SUBMIT;
- VIEW;
- DOWNLOAD;
- EXPLAIN; or
- any future RequestedAction.

Entitlement remains independently governed and independently evaluated.

Participation is not permission and cannot become permission by being current.

## 10. Participation Is Not Authentication

Authentication proves verified subject provenance.

Principal Mapping resolves:

```text
verified subject -> Principal P
```

Neither authentication nor Principal Mapping establishes:

```text
Participation(P,E)
```

Authentication-provider claims, Cognito groups, IAM identity, session state, or
browser identity state must not become Participation authority.

## 11. Participation Is Not E Currentness

Participation cannot revive or override a non-current Assessment Engagement.

The following must fail context legitimacy:

```text
current Participation(P,E)
+ non-current E
```

Current Participation proves standing only if E is also independently current.

## 12. Participation Is Not B Currentness

Participation cannot make a non-current Business Entity valid for Business
Context.

E -> B remains authoritative and immutable under Assessment Submission Business
Context Governance v1.

B currentness remains independently required before BUSINESS_CONTEXT_READY
where Business Context governance requires current B.

## 13. Participation Authority Owner

The logical authority category is:

```text
Assessment Engagement Participation Authority
```

Assessment Engagement Participation Authority may establish, change where
separately valid, revoke, or otherwise govern Participation relationships only
within the bounded Participation scope.

It is not:

- root;
- generic administrator;
- founder;
- owner;
- repository owner;
- Business Entity Membership authority;
- Entitlement authority;
- Authentication authority;
- Principal Mapping authority;
- Assessment Engagement Establishment Authority by default;
- Assessment Service authority;
- Website or portal authority;
- AWS/IAM authority;
- Cognito authority;
- AI/LLM/agent authority; or
- production authority.

Assessment Engagement Establishment Authority may establish initial
Participation only if future governance explicitly authorizes that bounded
operation and its evidence basis. It does not gain Participation authority
merely because it establishes E -> B.

## 14. Participation Terminating Authority Basis

Participation establishment must terminate in:

```text
accountable Participation authorization
    + independently verifiable evidence
```

The evidence must be scoped to at least:

- Principal P;
- Assessment Engagement E;
- relationship establishment, change, revocation, or restoration where
  applicable;
- the authority basis for that operation; and
- applicable governance or version context.

Participation Authority cannot self-authorize.

The following are insufficient terminating bases:

- Python object construction;
- record existence alone;
- generic administrator status;
- founder status;
- owner status;
- company status;
- repository access;
- database write access;
- AWS/IAM credentials;
- Cognito claims or groups;
- Website or browser state;
- Assessment Service ownership;
- Membership;
- Entitlement;
- prior successful authorization;
- AI/LLM output; or
- server-side code existence.

## 15. Participation Establishment

Participation must be explicitly established before it may support context
legitimacy.

No implicit Participation may be created from:

- Membership;
- Entitlement;
- authentication;
- Principal Mapping;
- portal access;
- caller E;
- E existence;
- E currentness;
- same-B relationship;
- Business Entity existence;
- Assessment Service ownership;
- Resource Identity;
- target legitimacy; or
- provisional Assessment Submission R.

Participation may be represented later by a non-production read-side proof, but
construction of a representation does not create real Participation authority.

## 16. Participation Currentness

Only current authoritative Participation may support E-context legitimacy.

Future realization may distinguish:

- authority-record currentness; and
- Participation business lifecycle/currentness.

Where both dimensions exist, both must support current usability before
Participation may contribute to E-context legitimacy.

Stale, revoked, expired, disabled, terminated, unknown, unavailable, or
otherwise non-current Participation must fail closed.

## 17. Participation Revocation

Participation revocation or non-currentness invalidates future use of that
Participation for E-context legitimacy.

Participation revocation need not require:

- revoking Membership;
- revoking Entitlement;
- closing E; or
- revoking Principal Mapping;

unless a separate governance artifact requires such propagation.

Participation is its own authority relationship.

Historical evidence of prior Participation must remain auditable. Revocation
does not erase historical truth that Participation previously existed.

## 18. Participation Rebinding

A Participation relationship for:

```text
P1 -> E1
```

must not silently become:

```text
P1 -> E2
```

or:

```text
P2 -> E1
```

Material identity correction must preserve historical evidence and require a
new governed relationship or authority fact rather than mutable authority
laundering.

This artifact does not select storage mechanics for correction or historical
retention.

## 19. Trusted Current-Attempt Binding

Trusted Current-Attempt Binding is a bounded authority fact answering:

Which exact pre-established Assessment Engagement is this authorization attempt
operating under?

Conceptually:

```text
Authorization Attempt A
    -> Assessment Engagement E
```

Binding does not establish:

- Participation(P,E);
- permission;
- Entitlement;
- E existence;
- E currentness;
- E -> B;
- B currentness;
- target legitimacy;
- Resource Identity;
- BUSINESS_CONTEXT_READY;
- ALLOW; or
- DENY.

## 20. Binding Scope

Binding must be:

- attempt-scoped;
- non-standing;
- non-transferable;
- non-reusable by default;
- non-rebinding;
- current for that attempt; and
- provenance-preserving.

Binding must not become a durable substitute for Participation.

Binding for attempt A must not automatically authorize attempt B.

## 21. Raw Caller Intent

Caller-supplied E is candidate intent only.

Potential transport forms include:

- request body;
- path;
- query;
- form;
- browser state;
- portal selection;
- session state; or
- any other request-carried value.

No transport representation creates authority.

The caller may communicate:

```text
I intend E1.
```

The caller may not authorize:

```text
E1 is legitimate context.
```

## 22. Derived Binding Model

The preferred bounded model is deterministic derived Binding.

Binding(A,E) may be derived for the current authorization attempt only after
independent validation of:

- verified Principal P;
- candidate E as intent;
- authoritative current resolved E;
- immutable E -> B;
- current authoritative Participation(P,E); and
- bounded current authorization attempt A.

Authority comes from the independently governed prerequisites and the bounded
derivation contract.

Authority does not come from:

- server says so;
- caller supplied E;
- portal displayed E;
- session contains E;
- route contains E; or
- code copied E into an object.

No separately standing Binding authority store is required by this governance.
This artifact does not prohibit a future represented binding proof if later
governance authorizes one, but no persistence or token technology is selected.

## 23. Binding Derivation Responsibility

The logical responsibility is a bounded deterministic attempt-context
derivation responsibility.

It may emit:

```text
Binding(A,E)
```

only when governed prerequisites succeed.

It may not:

- create Participation;
- create E;
- change E -> B;
- grant Entitlement;
- grant permission;
- establish target legitimacy;
- establish BUSINESS_CONTEXT_READY by itself;
- return ALLOW; or
- return DENY.

Its authority terminates in independently governed prerequisite facts:

```text
verified P
+ candidate intent E
+ current resolved E
+ current Participation(P,E)
+ bounded attempt A
```

## 24. Binding Failure

Binding derivation must fail closed if:

- P is missing or invalid;
- candidate E is missing or invalid;
- E is not found;
- E is stale or non-current;
- E is ambiguous or conflicting;
- Participation(P,E) is missing;
- Participation(P,E) is stale, revoked, or non-current;
- Participation references another E;
- required provenance is missing or invalid;
- attempt context is invalid; or
- prerequisite authority is unavailable or unsupported.

No default E is permitted.

## 25. Single-E Shortcut

The system must not automatically bind an attempt to E merely because P has
exactly one current Participation.

Standing Participation must not silently become request intent.

If the current attempt does not identify an intended E through the governed
candidate-input boundary, Binding fails closed.

## 26. Binding Replay

Binding(A,E) applies only to the bounded attempt A for which it was derived or
otherwise governed.

Binding(A,E) must not automatically authorize or establish context for:

```text
Attempt B
```

Replay, transfer, or reuse requires future explicit governance. It is not
authorized here.

## 27. Binding Rebinding

Once attempt A is bound to E1, that same authoritative Binding must not silently
become bound to E2.

A materially different engagement selection requires a distinct bounded
evaluation or binding event.

No mutation from:

```text
Binding(A,E1)
```

to:

```text
Binding(A,E2)
```

is permitted within the same authoritative binding.

## 28. Exact-E Conjunction

E-context legitimacy requires:

```text
Participation(P,E1)
+ Binding(A,E2)
+ E1 == E2
```

The equality check must use exact governed Assessment Engagement identity.

Same-B equivalence is prohibited.

If E1 and E2 differ, E-context legitimacy fails even when:

```text
E1 -> B1
E2 -> B1
```

## 29. Same-B Substitution

Mandatory same-B substitution case:

```text
E1 -> B1
E2 -> B1
Membership(P,B1)
Participation(P,E1)
Binding(A,E2)
```

Result:

```text
E_CONTEXT_LEGITIMATE(P,A,E2) = FAIL
```

Reason:

Participation and Binding reference different E.

Membership and same Business Entity cannot repair the mismatch.

## 30. Cross-B Substitution

Cross-B substitution case:

```text
E1 -> B1
E2 -> B2
Participation(P,E1)
Binding(A,E2)
```

Result:

```text
E_CONTEXT_LEGITIMATE(P,A,E2) = FAIL
```

No Principal, Membership, session, default, or Business Entity rewrite may
transform authoritative E2 -> B2 into B1.

## 31. Multiple Legitimate Engagements

Multiple current Participations are permitted:

```text
Participation(P,E1)
Participation(P,E2)
```

If Binding(A,E2) is current, E2 is current, and all E2 prerequisites are valid,
context may legitimately resolve to E2.

E1 must not create ambiguity merely because P also participates in E1.

Binding selects the current attempt context among independently legitimate E
contexts.

## 32. Binding Without Participation

The following must fail:

```text
Binding(A,E)
+ no current Participation(P,E)
```

Binding does not grant standing.

## 33. Participation Without Binding

The following must fail:

```text
Participation(P,E)
+ no current Binding(A,E)
```

Standing does not establish current attempt context.

## 34. Context Legitimacy

Assessment Engagement Context Legitimacy is the derived governed fact proving
only:

For current Principal P and current authorization attempt A, the attempt
legitimately operates within exact current Assessment Engagement E at the
engagement-context level.

Context legitimacy must preserve enough provenance to demonstrate:

- P;
- E;
- Participation authority basis or reference;
- Binding derivation basis or reference;
- exact-E match;
- currentness of prerequisites;
- applicable governance or version context where available; and
- failure reason category where legitimacy is denied by missing or invalid
  prerequisite.

Context legitimacy must not be persisted, reused, or interpreted beyond its
bounded attempt scope unless future governance explicitly authorizes that
behavior.

## 35. Context Legitimacy Is Not BUSINESS_CONTEXT_READY

E-context legitimacy is required for BUSINESS_CONTEXT_READY, but it is not
identical to BUSINESS_CONTEXT_READY.

Business Context readiness additionally depends on committed governance,
including authoritative:

- current E;
- immutable E -> B;
- current B;
- required provenance/currentness; and
- all other Assessment Submission Business Context Governance v1 requirements.

Do not collapse E-context legitimacy into Business Context readiness.

## 36. BUSINESS_CONTEXT_READY Is Not ALLOW

BUSINESS_CONTEXT_READY is not ALLOW.

BUSINESS_CONTEXT_READY establishes governed business context for downstream
provisional Assessment Submission establishment.

It does not grant protected action permission and does not replace Membership,
Entitlement, target legitimacy, Resource Identity, applicability, evaluator
composition, final composer, or enforcement.

## 37. Membership Ordering

Membership(P,B) remains an independently governed authorization fact.

This artifact does not change existing evaluator semantics.

Membership must not produce Participation.

Participation must not bypass Membership where Membership is required by
downstream authorization governance.

Under the current conceptual Assessment Submission path, Membership remains
downstream of Business Context derivation and is evaluated independently by the
authorization evaluator where applicable.

## 38. Entitlement Ordering

Entitlement remains downstream permission authority.

No E-context legitimacy result may imply Entitlement or RequestedAction
permission.

Entitlement must not produce Participation, Binding, E-context legitimacy, or
Business Context.

## 39. Authentication and Principal Ordering

The conceptual prerequisite order is:

```text
verified authentication
    -> Principal Mapping
    -> Principal P
    -> Participation(P,E)
```

Authentication does not establish Participation.

Principal Mapping does not establish Participation.

Invalid or unresolved Principal P prevents Participation from supporting
context legitimacy.

## 40. Business Context Order

The governed conceptual order is:

```text
verified subject
    -> Principal P
    -> candidate E
    -> authoritative Assessment Engagement resolution
    -> current E
    -> immutable E -> B
    -> current Participation(P,E)
    -> trusted Binding(A,E)
    -> exact-E conjunction
    -> E_CONTEXT_LEGITIMATE(P,A,E)
    -> current B / required business-context validation
    -> BUSINESS_CONTEXT_READY
    -> provisional Assessment Submission establishment
    -> target / Resource Identity / applicability / Membership / Entitlement
    -> evaluator ALLOW / DENY
```

Where an existing committed governance artifact specifies a more precise
ordering for its own domain, that artifact remains authoritative.

This artifact does not rewrite evaluator semantics.

## 41. Target Legitimacy Separation

Target legitimacy answers:

Why is R the legitimate protected resource target?

E-context legitimacy answers:

Why does P/current attempt A legitimately operate within E?

They are independent.

Target legitimacy must not establish Participation, Binding, or E-context
legitimacy.

E-context legitimacy must not establish target legitimacy.

## 42. Resource Lifecycle Separation

Provisional Assessment Submission R remains downstream of Business Context
readiness.

Context legitimacy must not be bootstrapped from provisional R.

The following circularity is prohibited:

```text
R -> E proves E legitimacy
need E legitimacy to establish R
```

The existing provisional lifecycle proof remains unchanged by this artifact.

## 43. Resource Identity Separation

Assessment Engagement E remains governed domain context.

This artifact does not make Assessment Engagement a ResourceClass.

Resource Identity authority is not expanded.

Resource Identity lookup success must not establish Participation, Binding, or
E-context legitimacy.

## 44. Evaluator Separation

The evaluator remains the final ALLOW/DENY composer under existing Trusted
Authorization architecture.

E-context legitimacy must not produce ALLOW or DENY.

The evaluator must not be treated as the producer of Participation or Binding
unless future governance explicitly creates such a responsibility, which this
artifact does not do.

## 45. Applicability Separation

Resource/action applicability does not establish engagement standing.

Applicability must not establish Participation, Binding, E-context legitimacy,
Business Context, Membership, Entitlement, or target legitimacy.

## 46. Website and Portal Separation

Website and portal surfaces remain presentation and request surfaces.

They may display engagements and communicate candidate E.

They cannot produce:

- Participation;
- trusted Binding;
- E-context legitimacy;
- Business Context;
- permission; or
- ALLOW/DENY.

Browser state, local storage, URL structure, UI selection, form values, or page
state is not authority.

## 47. Assessment Service Separation

Assessment Service ownership of methodology, deterministic assessment
execution, business decision truth, scoring, or evidence processing does not
make the Assessment Service Participation Authority or engagement-context
authority.

Assessment Service may later consume governed context facts where separately
authorized. It does not originate them by ownership status.

## 48. AI and Agent Separation

AI, LLMs, agents, AI Knowledge Assistant, MCP, prompts, model output,
multi-agent consensus, and model reasoning cannot establish or override:

- Participation;
- Binding;
- E-context legitimacy;
- Business Context;
- Membership;
- Entitlement;
- target legitimacy;
- ALLOW; or
- DENY.

AI may explain governed facts only where separately authorized and only after
those facts exist under non-AI authority.

## 49. AWS and Cognito Separation

Authentication and infrastructure authority are not engagement authority.

AWS IAM, Cognito, cloud credentials, execution roles, deployment access,
database access, API Gateway, Lambda identity, or server execution identity do
not create Participation, Binding, or E-context legitimacy.

Cognito may verify authentication only where separately governed. It does not
create P -> E Participation.

## 50. Administrative Separation

Generic administrator status does not create Participation authority.

Any future administrative Participation establishment must operate under the
bounded Assessment Engagement Participation Authority and its terminating
authority basis.

Existing administrative request, approval, mutation, revocation, restoration,
and audit distinctions are preserved.

This artifact does not impose universal dual approval, universal quorum, or a
fixed participant count.

## 51. Root Separation

Root is not universal authority.

Root cannot automatically:

- create Participation;
- bind arbitrary attempt to E;
- grant E-context legitimacy;
- grant permission; or
- grant production authority.

Existing TAB, root, and recovery governance remains authoritative for its own
domain. Root and recovery concepts are not imported merely because they exist.

## 52. Participation Authority Is Not Universal

Assessment Engagement Participation Authority is scoped to specific authorized
Participation establishment, change, revocation, or restoration events.

No actor or source receives standing wildcard power merely because it is
classified as Participation Authority.

Each authority-relevant operation must have its own valid basis, scope,
currentness, provenance, and fail-closed evaluation.

## 53. Provenance Requirements

Participation provenance must be sufficient to identify:

- authority basis or reference;
- Principal P;
- Assessment Engagement E;
- relationship currentness or lifecycle;
- establishment, change, revocation, restoration, or non-currentness
  provenance where applicable; and
- applicable governance or version context where available.

Binding provenance must be sufficient to identify:

- current bounded attempt or evaluation context A;
- Principal P;
- Assessment Engagement E;
- candidate-intent provenance as non-authoritative input where useful;
- derivation basis;
- Participation evidence or reference;
- currentness and attempt scope; and
- applicable governance or version context where available.

Context-legitimacy provenance must trace both Participation and Binding and
must show exact-E equality.

This artifact does not prescribe storage schema, event format, database,
token, API, or retention mechanics.

## 54. Currentness and Revocation Propagation

E-context legitimacy must fail or become unusable if any required authority
prerequisite is no longer current.

At minimum:

- invalid or non-current Principal prevents context legitimacy;
- non-current E prevents context legitimacy;
- revoked or non-current Participation prevents context legitimacy;
- expired, stale, wrong-attempt, replayed, or otherwise non-current Binding
  prevents context legitimacy;
- non-current B prevents BUSINESS_CONTEXT_READY where Business Context
  governance requires current B.

No stale derived legitimacy survives stale prerequisites.

Known current revocation or non-currentness must dominate stale positive
evidence.

## 55. Coherent Snapshot and TOCTOU Boundary

Consequential context derivation must use a coherent set of authority facts
appropriate to one authorization evaluation.

At minimum, future realization must avoid combining stale Participation with
newer E state, stale Binding with current Participation, or stale B with
current E in a way that creates unauthorized context.

This artifact does not implement GovernedVersionContext or select exact
snapshot mechanics.

Exact realization of coherent version, snapshot, cache, and TOCTOU handling
remains a downstream governance or implementation boundary unless already
resolved by predecessor governance.

## 56. Fail-Closed Contract

Context-legitimacy derivation must fail closed for:

- missing Principal;
- malformed Principal context;
- missing candidate E;
- malformed candidate E;
- E NOT_FOUND;
- E stale or non-current;
- ambiguous E;
- conflicting E;
- missing Participation;
- stale Participation;
- non-current Participation;
- revoked Participation;
- Participation for a different E;
- missing Binding;
- stale Binding;
- expired Binding;
- wrong-attempt Binding;
- replayed Binding;
- Binding for a different E;
- missing required provenance;
- invalid required provenance;
- non-current B where required for Business Context readiness;
- unsupported authority state; and
- any fact derived solely from caller assertion.

No default allow.

No default E.

No default Participation.

No default Binding.

## 57. Anti-Laundering Rules

None of the following independently establish Participation, Binding, or
E-context legitimacy:

- Authentication;
- Principal Mapping;
- Membership;
- Entitlement;
- caller E;
- caller B;
- portal selection;
- browser state;
- session state;
- E existence;
- E currentness;
- E -> B;
- Business Entity existence;
- Business Entity Membership;
- Assessment Service ownership;
- generic administrator;
- founder, owner, or company status;
- AWS IAM;
- Cognito;
- root;
- AI/LLM/agent output;
- target legitimacy;
- Resource Identity;
- provisional Assessment Submission R;
- runtime composition; or
- production deployment.

## 58. Authority Termination Graph

Participation termination:

```text
accountable Participation authorization
    + independently verifiable evidence
    -> bounded Participation Authority
    -> Participation(P,E)
```

Binding termination:

```text
verified P
    + candidate intent E
    + authoritative current E resolution
    + current authoritative Participation(P,E)
    + bounded current authorization attempt A
    -> deterministic bounded derivation
    -> Binding(A,E)
```

Context-legitimacy termination:

```text
Participation(P,E)
    + Binding(A,E)
    + exact-E equality
    + current prerequisites
    -> E_CONTEXT_LEGITIMATE(P,A,E)
```

No edge may terminate in self-assertion, circular authority, infinite
recursion, generic administrator status, infrastructure control, AI output, or
caller assertion.

## 59. Derived Binding Non-Circularity

The preferred derived Binding is not circular because caller E supplies intent
only.

Independent E resolution establishes what E is.

Independent Participation establishes P's standing in E.

The bounded derivation establishes only:

```text
this attempt is operating under the exact independently valid E selected by
candidate intent
```

The derivation does not manufacture standing, E existence, E currentness, E ->
B, permission, target legitimacy, or Business Context.

If a server copies caller E into a trusted object without independent E
resolution and Participation verification, no trusted Binding exists.

## 60. Binding Producer Boundary

This artifact governs only the logical bounded derivation responsibility.

It does not select:

- JWT;
- session;
- database;
- cache;
- API;
- route;
- Lambda;
- Cognito;
- IAM;
- Website;
- Assessment Service runtime; or
- any other production technology.

Production source or producer realization remains OPEN / NOT GRANTED.

## 61. Participation Producer Boundary

Concrete production Participation producer remains OPEN / NOT GRANTED.

This artifact does not choose:

- database;
- admin UI;
- portal;
- API;
- workflow engine;
- Cognito group;
- IAM role;
- source repository;
- persistence mechanism; or
- runtime service.

The artifact governs logical authority semantics only.

## 62. Production Source Ownership

Concrete production source ownership is not granted.

Logical authority category does not equal production implementation.

Existing source-ownership governance principles remain controlling:

- source ownership is scoped;
- technical control is not authority;
- production source selection requires separate governance; and
- production authority remains not granted until explicitly approved.

## 63. No Persistence Decision

This artifact selects no persistence.

Representation may later use bounded non-production deterministic evidence
where separately authorized.

Production storage remains unresolved.

## 64. No Runtime Decision

This artifact does not authorize runtime composition.

No handler, route, Assessment Service runtime, Website, Cognito, AWS, or
deployment integration is selected or authorized.

## 65. No Production Authority

This artifact grants no production authority.

Its existence establishes governance semantics only.

Production Participation Authority, production Binding Authority, production
E-context legitimacy authority, production Business Context authority,
persistence, runtime integration, deployment, and production authority remain
NOT GRANTED.

## 66. Attack Table

| Attack | Expected outcome |
| --- | --- |
| P Member B1; E1/E2 -> B1; Participation only E1; attempt E2 | FAIL |
| P participates E1 and E2; attempt bound E2 | E2 may be context if all E2 prerequisites are valid |
| Participation E1; Binding E2; both -> B1 | FAIL |
| Participation E1; Binding E2; cross-B | FAIL |
| Binding E without Participation | FAIL |
| Participation E without Binding | FAIL |
| Stale Participation plus valid Binding | FAIL |
| Valid Participation plus stale Binding | FAIL |
| Valid Participation plus Binding plus non-current E | FAIL |
| Membership plus Entitlement but no Participation | FAIL context legitimacy |
| Portal supplies E without independent Participation | FAIL |
| Server copies caller E into object without verification | FAIL |
| AI says P belongs to E | FAIL |
| Generic admin asserts Participation without bounded authority | FAIL |
| P has exactly one Participation but no candidate/binding | FAIL |
| Binding from prior attempt replayed | FAIL |
| Binding silently rebound E1 -> E2 | FAIL |

## 67. Authority Matrix

| Fact category | Establishes | Does not establish | Logical owner | Current implementation / representation | Production status |
| --- | --- | --- | --- | --- | --- |
| Authentication | Verified subject provenance | Principal, Membership, Participation, permission, ALLOW | Authentication Verification Owner | Non-production handoff exists | NOT GRANTED |
| Principal Mapping | Subject -> Principal P | Participation, Membership, Entitlement, context | Principal Mapping Authority | Non-production source exists | NOT GRANTED |
| Business Entity | Current governed B | E, Participation, Binding, permission | Business Entity Authority | Non-production source exists | NOT GRANTED |
| Assessment Engagement | Current E, immutable E -> B, establishment provenance | Participation, Binding, context legitimacy, permission | Assessment Engagement authority source / establishment authority | Non-production read-side source exists | NOT GRANTED |
| Participation | Current P -> E standing | Binding, Entitlement, target, ALLOW | Assessment Engagement Participation Authority | Not implemented | NOT GRANTED |
| Attempt Binding | Current A -> E attempt context | Participation, E existence, permission, target | Bounded deterministic attempt-context derivation responsibility | Not implemented | NOT GRANTED |
| E-context legitimacy | P/A legitimately operates in E at context level | BUSINESS_CONTEXT_READY by itself, permission, target, ALLOW | Derived from Participation + Binding + current E | Not implemented | NOT GRANTED |
| Membership | P -> B relationship | Participation, E selection, Entitlement | Membership Authority Source | Non-production source exists | NOT GRANTED |
| Entitlement | Scoped action authority state | Participation, Binding, ALLOW by itself | Entitlement Authority | Non-production source exists | NOT GRANTED |
| BUSINESS_CONTEXT_READY | Authoritative B available for provisional R | ALLOW, target legitimacy, Entitlement | Future Business Context derivation | Not implemented | NOT GRANTED |
| Provisional R | Non-effective Assessment Submission resource fact | E legitimacy, target, permission | Assessment Submission Resource Lifecycle Authority | Non-production proof exists | NOT GRANTED |
| Target legitimacy | Why R is current protected target | Participation, Binding, Business Context, ALLOW | Governed Assessment Submission Resource-Target Authority | Non-production handoff exists | NOT GRANTED |
| Resource Identity | Resolve governed R | target legitimacy, Participation, permission | Resource Identity Authority Source | Non-production source exists | NOT GRANTED |
| Applicability | Action applies to ResourceClass | Membership, Entitlement, Participation, ALLOW | Applicability governance | Implemented matrix exists | NOT GRANTED |
| Evaluator | ALLOW/DENY from governed inputs | Source authority, Participation production, Binding production | Deterministic evaluator | Non-production evaluator exists | NOT GRANTED |

## 68. Lifecycle / Currentness Matrix

| E state | Participation state | Binding state | Exact E match? | Outcome |
| --- | --- | --- | --- | --- |
| current | current | current | yes | potentially E_CONTEXT_LEGITIMATE |
| non-current | current | current | yes | FAIL |
| current | non-current | current | yes | FAIL |
| current | current | stale | yes | FAIL |
| current | current | missing | N/A | FAIL |
| current | missing | valid | N/A | FAIL |
| current | current for E1 | current for E2 | no, even same B | FAIL |

Potentially E_CONTEXT_LEGITIMATE means only that the context-legitimacy
predicate may be satisfied. BUSINESS_CONTEXT_READY and ALLOW still require
their separately governed facts.

## 69. Cardinality Rules

The following cardinality rules are governed:

- B -> zero or multiple E;
- E -> exactly one authoritative B under existing Business Context governance;
- P -> zero or multiple E Participation;
- E -> zero or multiple P Participation;
- Attempt A -> exactly one E when Binding is valid;
- Binding(A,E) -> exactly one bounded attempt/evaluation context A;
- no wildcard Participation; and
- no wildcard Binding.

## 70. Non-Grants

Implementation Authority: NOT GRANTED.

Participation Implementation: NOT GRANTED.

Attempt-Binding Implementation: NOT GRANTED.

E-Context Legitimacy Implementation: NOT GRANTED.

Business Context Derivation: NOT GRANTED.

Assessment Engagement Source Modification: NOT GRANTED.

Membership Modification: NOT GRANTED.

Entitlement Modification: NOT GRANTED.

Resource Identity Modification: NOT GRANTED.

Assessment Submission Lifecycle Modification: NOT GRANTED.

Evaluator Modification: NOT GRANTED.

Applicability Modification: NOT GRANTED.

GovernedVersionContext Implementation: NOT GRANTED.

Final Composer: NOT GRANTED.

Enforcement: NOT GRANTED.

Persistence: NOT GRANTED.

Runtime Integration: NOT GRANTED.

Cognito/AWS Integration: NOT GRANTED.

Website/Portal Integration: NOT GRANTED.

Assessment Service Runtime Integration: NOT GRANTED.

Deployment: NOT GRANTED.

Production Participation Authority: NOT GRANTED.

Production Request-Binding Authority: NOT GRANTED.

Production E-Context Legitimacy Authority: NOT GRANTED.

Production Business Context Authority: NOT GRANTED.

Production Authority: NOT GRANTED.

## 71. Open Questions / Deferred Decisions

The following realization questions remain open and are not resolved by this
artifact:

- concrete Participation producer;
- concrete Participation evidence source;
- Participation persistence;
- production Participation mutation and revocation workflow;
- production Binding derivation location;
- whether any represented Binding proof is needed;
- coherent snapshot / GovernedVersionContext realization;
- production audit and evidence realization;
- Business Context derivation implementation;
- R -> E provenance downstream;
- Assessment Submission lifecycle awareness of E downstream;
- target producer integration with future Business Context;
- final composer;
- enforcement;
- runtime integration;
- Cognito/AWS integration;
- Website/Portal integration;
- Assessment Service runtime integration;
- deployment; and
- production authority.

## 72. Future Implementation Order

Expected future sequence, as governance guidance only:

1. Strict adversarial governance conformance review of this artifact.
2. Human commit approval for this governance artifact.
3. Commit and push exact reviewed governance bytes.
4. Strict post-governance convergence review.
5. Likely bounded Participation read-side implementation-authorization review.
6. Likely trusted attempt-binding derivation/handoff review.
7. Likely context-legitimacy composition proof.
8. Business Context derivation.
9. Downstream R -> E provenance or lifecycle integration as separately
   governed.
10. Runtime and production only after independent future authority gates.

None of these implementation steps is authorized by this artifact.

## 73. Governance Quality Requirements

Future reviews and implementations relying on this artifact must preserve:

- technology neutrality;
- deterministic authority semantics;
- fail-closed behavior;
- non-circularity;
- bounded scope;
- auditability;
- provenance awareness;
- currentness awareness;
- revocation awareness;
- explicit authority ownership;
- explicit non-authority inputs; and
- unresolved production realization.

Vague claims such as "trusted system validates", "authorized administrator",
"secure server", or "server-side object" are insufficient unless the authority
basis is separately governed and traceable.

## 74. Existing Governance Preservation

This artifact does not contradict or supersede existing governance.

It refines the previously open engagement-context legitimacy producer by
governing the required Participation and Binding facts and their exact-E
conjunction.

Existing governance remains authoritative for:

- Assessment Engagement E -> B establishment and currentness;
- Business Entity authority;
- Principal Mapping;
- Membership;
- Entitlement;
- authentication trust provenance;
- target provenance;
- Resource Identity;
- Assessment Submission resource lifecycle;
- applicability;
- evaluator ALLOW/DENY;
- administrative authority;
- terminating authority basis;
- source ownership;
- root/recovery boundaries; and
- production non-grants.

## 75. Governance Decision Summary

The governed Assessment Engagement context-legitimacy model is:

```text
verified subject
    -> Principal P
    -> candidate E as intent
    -> current resolved Assessment Engagement E
    -> current authoritative Participation(P,E)
    -> current trusted Binding(A,E)
    -> exact-E match
    -> E_CONTEXT_LEGITIMATE(P,A,E)
```

This model preserves:

- Participation as distinct from Membership;
- Participation as distinct from Entitlement;
- Binding as attempt-scoped and non-standing;
- exact-E matching rather than same-B equivalence;
- same-B substitution defense;
- cross-B substitution defense;
- no single-E shortcut;
- separation from target legitimacy;
- separation from Resource Identity;
- separation from Business Context readiness;
- separation from final permission;
- fail-closed behavior for missing, stale, conflicting, mismatched, replayed,
  or caller-derived authority;
- no implementation authority; and
- no production authority.

The next valid gate is strict read-only adversarial governance conformance
review of this artifact.
