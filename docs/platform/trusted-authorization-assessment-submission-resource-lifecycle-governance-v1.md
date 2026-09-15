# Trusted Authorization Assessment Submission Resource Lifecycle Governance v1

## 1. Purpose

This artifact governs the Assessment Submission resource lifecycle decision required
before meaningful non-production Trusted Authorization integration can proceed for
the current protected operation:

`PROTECTED_ASSESSMENT_SUBMISSION`.

It answers the lifecycle question left open by Resource-Reference Provenance
Governance v1:

At the exact moment Trusted Authorization decides whether `SUBMIT_ASSESSMENT` is
allowed, what governed Assessment Submission resource exists, who established it,
what does `resource_reference` R identify, and how was its Business Entity binding
made authoritative?

This artifact defines architecture only. It does not implement resource creation,
resource registration, persistence, target production, final composition,
runtime integration, enforcement, or production authority.

## 2. Scope

This artifact applies only to the current Trusted Authorization protected
operation:

`PROTECTED_ASSESSMENT_SUBMISSION`

which maps to:

`NonProductionApplicationOperation.SUBMIT_ASSESSMENT`

which maps through the Resource/Action Handoff to:

`RequestedAction.SUBMIT`.

The protected resource remains a distinct governed Assessment Submission resource
with semantic class:

`ResourceClass.ASSESSMENT_SUBMISSION`.

This artifact does not add protected operations, resource classes, routes,
handlers, persistence, authentication integration, evaluator integration,
deployment, or production authority.

## 3. Current Governed Context

Current governance establishes these facts:

- The protected operation catalog contains the Assessment Submission protected
  operation.
- The Resource/Action Handoff maps the operation to `RequestedAction.SUBMIT`.
- Resource/Action Applicability treats `RequestedAction.SUBMIT` as applicable to
  `ResourceClass.ASSESSMENT_SUBMISSION`.
- Resource Identity answers what governed resource R resolves to, including
  resource class, authoritative Business Entity binding, and lifecycle/currentness
  facts owned by that authority source.
- Resource-target provenance answers why R is the legitimate target of this
  operation.
- Business Entity, Membership, Entitlement, and the evaluator remain separate
  authority layers.

The protected resource is not silently redefined as a Business Entity, Principal,
HTTP request, route, payload, request ID, session, workspace, engagement, or
transport object.

## 4. Current Runtime Reality

Current `POST /assessment` runtime behavior is:

1. It receives assessment input.
2. It validates the payload.
3. It performs deterministic assessment scoring.
4. It generates a UUID `requestId`.
5. It returns `persisted=False`.

Current `POST /assessment` runtime behavior does not:

- create a governed Assessment Submission resource;
- register such a resource;
- resolve such a resource through Resource Identity;
- establish an authoritative Business Entity binding for it;
- invoke Trusted Authorization;
- invoke the evaluator;
- require ALLOW before scoring.

The current UUID `requestId` is an observability and response-correlation
identifier. It is not automatically `resource_reference` R, resource
registration, resource authority, target provenance, or proof that a governed
Assessment Submission exists.

`persisted=False` records that current runtime does not persist the Assessment
Submission. It does not prove persistence is forbidden or required.

## 5. Problem Statement

The evaluator requires a `resource_reference` that Resource Identity can resolve
to a governed resource. Resource Identity must return the authoritative resource
class, Business Entity binding, and lifecycle/currentness facts. For Assessment
Submission, the missing lifecycle question is:

When does the governed Assessment Submission resource exist relative to request
validation, authorization, scoring, submission, and materialization?

If no governed Assessment Submission exists before authorization, then Resource
Identity cannot resolve R without inventing a resource. If caller input creates
R or its Business Entity binding by assertion, authority is laundered from the
caller into authorization. If scoring or materialization occurs before
authorization, DENY cannot prevent the consequential business effect.

This artifact selects the lifecycle model that breaks that cycle.

## 6. Required Distinctions

The following distinctions are mandatory:

- candidate request input is not a governed resource;
- identifier generation is not resource authority;
- request ID is not resource reference;
- payload validation is not authorization;
- caller Business Entity assertion is not authoritative binding;
- Principal identity is not resource ownership;
- Membership is not resource ownership;
- Entitlement is not target provenance;
- resource existence is not permission;
- Resource Identity lookup is not target legitimacy;
- target provenance is not ALLOW;
- evaluator ALLOW is not mutation;
- deterministic scoring is not resource registration unless separately governed.

## 7. Candidate Lifecycle Models

### Model A - Pre-Existing Assessment Submission

A governed Assessment Submission exists before `SUBMIT_ASSESSMENT`.
Authorization operates against that existing resource.

### Model B - Provisional Resource Before Authorization

A governed but non-effective provisional Assessment Submission identity is
established before authorization. Authorization evaluates against that
provisional resource. Business execution, submission transition, scoring if
consequential, and materialization occur only after ALLOW.

### Model C - Pending Resource Before Authorization

A pending governed Assessment Submission is created before authorization, then
transitioned after authorization.

### Model D - Parent-Resource Authorization Before Child Creation

Authorization occurs against another pre-existing governed parent resource, and
the Assessment Submission is created only after ALLOW.

### Model E - Post-Creation Authorization

Assessment Submission is created or materialized first, and authorization is
performed afterward.

### Model F - Other

Any other lifecycle model not captured above.

## 8. Model Evaluation

| Model | Resource exists when? | Authorization target | BE binding basis | Resource Identity availability | Circularity risk | IDOR/BOLA implications | Compatibility | Complexity | Decision |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A - Pre-existing resource | Before submission | Existing Assessment Submission | Existing Resource Identity record | Available if resource exists | Low only if pre-creation is explained | Strong if target provenance is real | Weak against current runtime semantics because no such resource exists | Medium | Rejected |
| B - Provisional before authorization | After governed establishment, before evaluator | Provisional Assessment Submission | Independently governed business context accepted by lifecycle authority | Available before evaluator | Controlled because establishment is non-effective and not permission | Strong if target provenance and Resource Identity remain separate | Strong; preserves distinct protected resource and permits DENY before consequential execution | Medium | Selected |
| C - Pending before authorization | Before evaluator | Pending Assessment Submission | Same as Model B | Available before evaluator | Similar to B | Similar to B | Redundant unless pending has distinct authority meaning | Medium-high | Rejected |
| D - Parent-resource authorization | Parent exists before child | Parent resource | Parent Resource Identity | Available for parent, not Assessment Submission | Low if parent exists | Strong only after protected resource model changes | Conflicts with current Assessment Submission protected resource unless new governance changes it | High | Rejected |
| E - Post-creation authorization | After creation/materialization | Created Assessment Submission | Risk of caller/materialization contamination | Available after business effect | High | Weak because DENY may be too late | Conflicts with fail-closed authorization-before-effect principle | Low code complexity, high authority risk | Rejected |
| F - Other | Undefined | Undefined | Undefined | Undefined | Undefined | Undefined | No needed alternative identified | Undefined | Rejected |

## 9. Selected Lifecycle Model

The selected lifecycle model is:

MODEL B - PROVISIONAL RESOURCE BEFORE AUTHORIZATION.

The governed Assessment Submission resource exists for authorization as a
minimal, non-effective, provisional resource before evaluator invocation.

The provisional resource is sufficient for Resource Identity and permission
evaluation, but it is not a completed submission, scored result, report,
materialized business record, or proof that the Principal may submit it.

## 10. Resource Existence Semantics

A governed Assessment Submission resource exists for authorization only when all
minimum authorization-facing resource facts have been established by the
Assessment Submission Resource Lifecycle Authority:

- stable `resource_reference` R;
- semantic class `ResourceClass.ASSESSMENT_SUBMISSION`;
- authoritative Business Entity binding B;
- lifecycle state `PROVISIONAL`;
- lifecycle authority/provenance reference sufficient for audit;
- applicable governance/version context sufficient to interpret the lifecycle
  fact.

Existence does not mean:

- a UUID was generated;
- a Python object was constructed;
- an HTTP request arrived;
- a payload passed schema validation;
- a route was invoked;
- the caller supplied an identifier;
- deterministic scoring already occurred.

For this governance layer, existence means there is a governed, non-effective,
authorization-facing Assessment Submission resource identity that Resource
Identity may resolve before evaluator invocation.

## 11. Resource Reference Semantics

`resource_reference` R identifies exactly one governed provisional Assessment
Submission resource for the authorization decision.

R must be:

- authorization-facing;
- stable for the decision;
- unambiguous;
- scoped to one governed Assessment Submission resource;
- independent of caller authority.

R must not be automatically equated with:

- HTTP request ID;
- correlation ID;
- trace ID;
- payload hash;
- Principal ID;
- Business Entity ID;
- route;
- browser identifier;
- generated UUID by itself.

Future realizations may use opaque identifiers, but opacity and uniqueness do
not create authority.

## 12. Resource Establishment / Registration

The selected model requires semantic resource registration before evaluator
invocation.

Registration means the Assessment Submission Resource Lifecycle Authority has
established a minimal provisional resource fact that Resource Identity can
resolve. Registration is an authority concept, not a storage technology.

This artifact does not select DynamoDB, SQL, S3, in-memory storage, AWS service,
file storage, or any production persistence mechanism.

Registration must fail closed when the lifecycle authority cannot establish a
single unambiguous provisional Assessment Submission resource with an
authoritative Business Entity binding.

## 13. Initial Business Entity Binding

The initial Business Entity binding for a provisional Assessment Submission must
come from an already-authoritative governed business context accepted by the
Assessment Submission Resource Lifecycle Authority.

The terminating rule is:

The lifecycle authority may bind provisional Assessment Submission resource R to
Business Entity B only when B is supplied by, or resolved from, an independently
governed business context whose authority does not depend on the caller's
assertion, Principal identity, Membership, Entitlement, or the provisional
resource being authorized.

Caller payload fields such as `organization`, caller-supplied
`business_entity_id`, UI selection, browser state, route value, session value,
or request metadata are untrusted candidate context until independently resolved
by that governed business context.

This artifact does not select a concrete production source for that business
context. It defines the logical authority rule needed to break BE circularity.

## 14. Resource Lifecycle States

The selected model requires only these lifecycle states at this governance
stage:

### PROVISIONAL

The resource exists for authorization and Resource Identity resolution. It is
not effective business submission state. `SUBMIT_ASSESSMENT` may be evaluated
against it.

### SUBMITTED

The business transition permitted after ALLOW. The resource may become an
effective submitted Assessment Submission only through a separate mutation layer.

### ABANDONED

A non-effective terminal or cleanup-eligible state for a provisional resource
after DENY, failed authorization context, timeout, or cancelled operation.

### STALE

A non-current state that Resource Identity or the lifecycle authority may expose
when the resource is no longer eligible for authorization.

This artifact does not require a larger state machine. Additional states require
separate governance if they carry authority meaning.

## 15. Target-Provenance Relationship

Lifecycle/resource establishment and target provenance are distinct.

Lifecycle establishment creates a governed provisional resource fact:

R exists as a provisional Assessment Submission bound to Business Entity B.

Resource-target provenance establishes:

R is the actual target of this `PROTECTED_ASSESSMENT_SUBMISSION` operation.

Resource existence alone does not prove target legitimacy. Target legitimacy
alone does not prove Resource Identity, Business Entity binding, Membership,
Entitlement, or ALLOW.

The existing Governed Assessment Submission Resource-Target Authority remains
responsible for target legitimacy. A real target producer remains future work.

## 16. Resource Identity Relationship

Resource lifecycle/registration establishes authoritative resource facts.

Resource Identity resolves those authoritative facts for authorization:

- resource reference;
- resource ID if applicable;
- resource class;
- Business Entity binding;
- lifecycle/currentness state.

Resource Identity does not create target legitimacy, permission, Membership,
Entitlement, or ALLOW. Successful lookup does not prove why R is the intended
target of the operation.

## 17. Authorization Sequence

The selected conceptual sequence is:

1. Request arrives with untrusted input.
2. Safe parsing, syntactic validation, and non-authoritative normalization may
   occur.
3. Assessment Submission Resource Lifecycle Authority establishes one
   provisional Assessment Submission resource R with authoritative Business
   Entity binding B.
4. Governed Assessment Submission Resource-Target Authority establishes that R
   is the actual target of this protected operation.
5. Resource Identity resolves R to a governed Assessment Submission resource.
6. Applicability confirms `RequestedAction.SUBMIT` applies to
   `ResourceClass.ASSESSMENT_SUBMISSION`.
7. Business Entity, Membership, and Entitlement are resolved independently.
8. Evaluator composes final ALLOW or DENY.
9. DENY prevents effective submission and consequential business execution.
10. ALLOW permits a separate mutation/execution layer to transition the resource
    and perform consequential business execution.

No step may borrow authority from another.

## 18. ALLOW Semantics

Evaluator ALLOW permits, but does not itself perform, the governed transition:

`PROVISIONAL -> SUBMITTED`

and any associated consequential business execution such as materialized scoring
or effective submission processing.

ALLOW is not mutation. ALLOW is not persistence. ALLOW is not resource
registration. ALLOW is not proof that a later execution step cannot fail.

## 19. DENY Semantics

Evaluator DENY means no effective Assessment Submission may be submitted,
materialized, or consequentially scored under the denied authorization decision.

The provisional resource must remain non-effective and may transition to
`ABANDONED` or equivalent non-effective cleanup state under lifecycle authority.

DENY cleanup mechanics are implementation details and are not authorized here.

## 20. Validation vs Consequential Execution

The selected model allows limited pre-authorization work:

- request parsing;
- syntactic/schema validation;
- duplicate-key rejection;
- assessment version recognition;
- non-authoritative normalization needed to evaluate admissibility.

The selected model does not allow these pre-authorization activities to become:

- resource authority;
- Business Entity authority;
- target provenance;
- Membership;
- Entitlement;
- ALLOW.

Consequential business execution must wait for ALLOW.

## 21. Deterministic Scoring Relationship

Deterministic scoring is not automatically resource registration.

Scoring may be split conceptually:

- pre-authorization validation may inspect whether the payload is syntactically
  admissible;
- consequential scoring that creates, materializes, publishes, stores, admits,
  or otherwise makes Assessment Submission business state effective must occur
  only after ALLOW.

Current runtime scoring is not yet integrated with Trusted Authorization and is
not governed by this artifact as authorized execution.

## 22. IDOR/BOLA Analysis

The intended chain is:

untrusted request or candidate
    -> governed provisional resource establishment
    -> legitimate R
    -> target establishment for this operation
    -> Resource Identity
    -> authoritative Business Entity binding
    -> Membership
    -> Entitlement
    -> Evaluator
    -> ALLOW or DENY
    -> only then permitted business transition or execution.

R2 substitution fails because a caller cannot make raw R2 a legitimate target by
supplying it, formatting it correctly, causing it to resolve, sharing the same
Business Entity, or having otherwise broad permission. The Resource-Target
Authority must establish R2 as the actual target of this operation, and Resource
Identity and permission layers must still pass independently.

## 23. Same-BE Substitution Analysis

If R1 is the intended Assessment Submission and R2 is another valid Assessment
Submission in the same Business Entity with the same class and broad permission,
same-BE authorization is still not target legitimacy.

The selected model prevents substitution through these requirements:

- one provisional resource R is established for the current operation;
- target provenance must establish that this R is the actual target;
- Resource Identity lookup success does not select the target;
- Membership and Entitlement do not select the target;
- caller-supplied R2 remains candidate input unless target provenance accepts it.

## 24. Cross-BE Substitution Analysis

If caller attempts R2 belonging to another Business Entity:

- target provenance must first establish R2 as the actual target;
- Resource Identity returns the authoritative BE binding for R2;
- caller-supplied BE cannot override that binding;
- Membership must independently cover that BE;
- Entitlement must independently cover that resource/action tuple;
- evaluator composes final ALLOW or DENY.

No layer may borrow another layer's authority.

## 25. Circular Authority Analysis

The selected model breaks the cycle:

authorization required to create resource
    -> resource required to authorize
    -> authorization required to create resource.

It breaks the cycle by distinguishing provisional authorization-facing resource
establishment from effective business creation or submission.

The lifecycle authority may establish a minimal non-effective provisional
resource before authorization. That establishment is not permission and does not
make business state effective. Authorization then determines whether the
provisional resource may transition to submitted/effective state.

## 26. Authentication Separation

Real authentication producer remains open.

Authentication proves subject provenance. It does not create resource identity,
Business Entity binding, target legitimacy, Membership, Entitlement, permission,
or ALLOW.

Authenticated Principal identity does not automatically determine the
Assessment Submission resource's Business Entity.

## 27. Capability Separation

Real application-capability producer remains open.

Capability semantics identify what protected application operation is being
attempted. They do not establish target R, resource existence, Business Entity
binding, Membership, Entitlement, or ALLOW.

Route identity alone is not capability authority.

## 28. Permission Separation

Resource lifecycle authority may establish that R exists provisionally.

Resource-target authority may establish that R is the target.

Resource Identity may establish what R resolves to.

Membership may establish Principal membership in Business Entity B.

Entitlement may establish permission for the tuple.

The evaluator alone composes ALLOW or DENY.

Resource authority is not permission.

## 29. Mutation Separation

Authorization is not mutation.

Evaluator ALLOW permits a governed business transition. A separate
execution/mutation layer performs that transition, subject to later enforcement
and TOCTOU governance.

Evaluator DENY prevents the transition from becoming effective.

## 30. GovernedVersionContext Dependency

`GovernedVersionContext` provenance remains open/deferred.

Lifecycle establishment should eventually carry enough version/governance
context for audit and reproducibility, but this artifact does not close the
full `GovernedVersionContext` producer boundary.

If a future implementation needs a concrete lifecycle-governance version field,
that must be reviewed in a separate implementation-authorization or governance
review.

## 31. Enforcement Boundary

Enforcement remains open.

This artifact defines where enforcement logically belongs: before effective
submission transition and before consequential scoring/materialization.

It does not implement ALLOW gating, route binding, handler integration,
evaluator invocation, or business execution blocking.

## 32. TOCTOU Boundary

TOCTOU remains open/deferred.

Facts whose freshness may matter between ALLOW and execution include:

- provisional resource lifecycle state;
- resource class;
- Business Entity binding;
- Membership;
- Entitlement;
- governed version context;
- target identity.

This artifact does not define locking, transactions, leases, or replay controls.

## 33. Persistence Decision

Persistence is:

UNRESOLVED UNTIL IMPLEMENTATION ARCHITECTURE.

The selected model requires semantic registration before authorization, but it
does not require a specific persistence technology. A future realization must
show how Resource Identity can resolve R deterministically and fail closed.

Persistence authority is NOT GRANTED.

## 34. Technology Neutrality

This artifact selects no concrete technology as authoritative.

The lifecycle model does not require or authorize:

- DynamoDB;
- RDS;
- S3;
- API Gateway;
- Lambda;
- Cognito;
- IAM;
- JWT/JWKS;
- AWS-specific resource IDs;
- environment variables;
- plugins;
- AI classifiers.

Logical authority semantics precede implementation technology.

## 35. Explicit Prohibitions

The following must not establish resource existence, resource reference
legitimacy, Business Entity binding, lifecycle state, permission, or ALLOW:

- caller-provided resource reference;
- caller-provided Business Entity identifier;
- caller-provided organization field;
- payload schema validity;
- route match;
- request ID;
- browser/UI selection;
- session storage;
- Python object construction;
- Resource Identity lookup alone;
- Principal identity alone;
- Membership alone;
- Entitlement alone;
- AI/LLM/MCP inference;
- AWS identity;
- IAM permission;
- Lambda execution role;
- API Gateway context;
- network location;
- deployment identity;
- founder status;
- company owner status;
- administrator status;
- developer status;
- AWS account owner status.

No universal maker-checker, dual approval, quorum, or standing separation of
duties is introduced by this artifact.

## 36. Production Boundary

Production Authentication Authority: NOT GRANTED.

Production Capability Integration Authority: NOT GRANTED.

Production Resource Integration Authority: NOT GRANTED.

Production Resource Lifecycle Authority: NOT GRANTED.

Persistence Authority: NOT GRANTED.

Deployment Authority: NOT GRANTED.

Production Authority: NOT GRANTED.

No concrete production owner, service, database, AWS principal, person, team,
credential, or role is selected.

## 37. Fail-Closed Rules

The lifecycle and downstream authorization chain must fail closed under these
conditions:

| Condition | Responsible boundary | Required result |
| --- | --- | --- |
| No legitimate provisional resource can be established | Lifecycle authority | No valid R; authorization cannot proceed as valid target |
| Resource reference absent | Lifecycle/target handoff or evaluator input | INVALID or DENY as appropriate |
| Resource reference ambiguous | Lifecycle or Resource Identity | Fail closed; no arbitrary selection |
| Resource establishment conflicting | Lifecycle authority | Fail closed; no target fact |
| BE binding absent | Lifecycle/Resource Identity | Fail closed |
| BE binding ambiguous | Lifecycle/Resource Identity | Fail closed |
| BE binding conflicting | Lifecycle/Resource Identity | Fail closed |
| Caller BE assertion only | Lifecycle authority | Not authoritative; fail closed absent independent context |
| Wrong resource class | Resource Identity/applicability | DENY/no ALLOW |
| Stale resource | Resource Identity/lifecycle authority | DENY/no ALLOW |
| Inapplicable action | Applicability/evaluator | DENY/no ALLOW |
| Target provenance absent | Resource-Target Authority | No valid target fact |
| Target provenance conflicting | Resource-Target Authority | Fail closed; no precedence by default |
| Membership missing | Membership/evaluator | DENY |
| Entitlement missing | Entitlement/evaluator | DENY |
| Authorization context incomplete | Evaluator/final composer | DENY or no valid evaluator request |

Failures must remain attributed to the correct authority layer.

## 38. Future Bounded Realization

After this artifact is committed and separately reviewed, a future bounded
non-production realization may be considered to prove:

- provisional Assessment Submission resource establishment;
- stable authorization-facing R;
- authoritative initial Business Entity binding from governed business context;
- minimal lifecycle state;
- compatibility with Resource Identity;
- compatibility with the existing target-fact handoff;
- deterministic fail-closed behavior.

Any such work requires a separate STRICT READ-ONLY IMPLEMENTATION-AUTHORIZATION
REVIEW. This artifact grants no implementation authority.

## 39. Anti-Recursion / Governance Stopping Rule

This artifact stops at the finite logical authority basis:

The Assessment Submission Resource Lifecycle Authority may establish a
non-effective provisional Assessment Submission resource only from an
already-authoritative governed business context, and may not derive that context
from caller assertion, Principal identity, Membership, Entitlement, or the
resource being authorized.

This does not require immediate governance for who appoints the lifecycle
authority, who owns that owner, or who allocates an identifier generator.

## 40. Decision Summary

The selected model is:

MODEL B - PROVISIONAL RESOURCE BEFORE AUTHORIZATION.

At evaluator authorization time, the concrete authorization-facing resource fact
is:

A governed, non-effective, provisional Assessment Submission resource R with
`ResourceClass.ASSESSMENT_SUBMISSION`, authoritative Business Entity binding B,
and lifecycle state `PROVISIONAL`, established by the Assessment Submission
Resource Lifecycle Authority before evaluator invocation.

The Business Entity binding is authoritative because it comes from an
independently governed business context accepted by the lifecycle authority, not
from caller assertion, Principal identity, Membership, Entitlement, or permission
circularity.

The business effect prevented until ALLOW is:

effective Assessment Submission transition/materialization and consequential
business execution, including consequential scoring where scoring would create
or materialize business state.

## 41. Unresolved Future Integration Questions

The following remain open:

- real authentication producer and runtime integration;
- real application-capability producer and runtime integration;
- real Assessment Submission resource lifecycle producer;
- real Assessment Submission resource-target producer;
- concrete resource registration realization;
- concrete Resource Identity source realization for provisional resources;
- concrete governed business context source;
- `GovernedVersionContext` provenance;
- final evaluator request assembly;
- evaluator invocation integration;
- decision consumption/enforcement;
- TOCTOU hardening;
- persistence architecture if needed;
- production authority-source realization.

These are not authorized by this artifact.

## 42. Authority Statement

This artifact grants:

- bounded governance decision authority for Assessment Submission resource
  lifecycle semantics only.

This artifact does not grant:

- implementation;
- implementation-file modification;
- runtime integration;
- resource-target producer implementation;
- resource lifecycle producer implementation;
- resource registration implementation;
- persistence;
- database or DynamoDB work;
- handler integration;
- route binding;
- authentication integration;
- Cognito;
- AWS authentication integration;
- JWT/JWKS;
- final composer implementation;
- evaluator integration;
- enforcement;
- TOCTOU implementation;
- deployment;
- production resource integration;
- production authority;
- git commit;
- git push;
- git tag.
