# Trusted Authorization Resource-Reference Provenance Governance v1

Version: v1

## 1. Purpose

This artifact governs one bounded Trusted Authorization fact:

```text
What makes resource_reference R the legitimate protected resource target for
PROTECTED_ASSESSMENT_SUBMISSION before Resource Identity lookup and downstream
authorization consume R?
```

It governs resource-reference provenance for the sole current protected
operation. It does not decide whether a Principal may perform that operation.
Permission remains downstream and requires Resource Identity, Business Entity,
Membership, Entitlement, applicability, version validation, and final evaluator
composition.

## 2. Scope

This artifact governs:

- resource-reference provenance for `PROTECTED_ASSESSMENT_SUBMISSION`;
- Assessment Submission target semantics;
- the logical legitimacy owner for target establishment;
- the terminating provenance basis for treating a resource reference as the
  actual target;
- candidate input boundaries;
- operation-target binding requirements;
- the relationship to Resource Identity and Business Entity binding;
- deterministic fail-closed behavior; and
- bounded non-production realization implications.

This artifact does not govern or authorize:

- report view or report download operations;
- assistant resource/use operations;
- administrative operations;
- generic CRUD operations;
- new protected application operations;
- new Resource classes;
- implementation;
- tests;
- runtime activation;
- handler integration;
- route binding;
- authentication integration;
- Cognito integration;
- AWS authentication integration;
- JWT/JWKS verification;
- persistence;
- deployment;
- production resource integration; or
- production authority.

## 3. Current Architecture Context

Trusted Authorization currently has bounded non-production proofs for:

```text
already-legitimate verified authentication fact
        -> TrustedSubjectEvidence
```

and:

```text
already-legitimate application capability fact
        -> PROTECTED_ASSESSMENT_SUBMISSION
```

The application-operation selector maps the current Layer-2 protected operation
to the current Trusted Authorization operation. The resource/action handoff
maps the Trusted Authorization operation plus a supplied resource reference to a
canonical RequestedAction and preserved reference. Resource Identity then
resolves the supplied reference to a governed resource or fails closed.

The unresolved fact is upstream of Resource Identity lookup:

```text
why resource_reference R is legitimately the target for this assessment
submission operation.
```

## 4. Current Protected Operation

The current protected-operation scope contains exactly one accepted operation:

```text
PROTECTED_ASSESSMENT_SUBMISSION
        -> NonProductionApplicationOperation.SUBMIT_ASSESSMENT
        -> RequestedAction.SUBMIT
```

This artifact does not add report view, report download, assistant invocation,
administrative action, future CRUD, dynamic registration, or generic operation
selection.

## 5. Protected Resource Model

The protected resource for the current operation is a distinct governed
Assessment Submission resource.

The existing Resource class is:

```text
ResourceClass.ASSESSMENT_SUBMISSION
```

The protected resource is a stable authorization-facing `GovernedResource`
representing the specific Assessment Submission target or context against which
deterministic assessment submission and scoring is being performed.

The protected resource is not:

- the HTTP request;
- the route;
- the request body;
- the assessment answers;
- the authenticated Principal;
- the Governed Business Entity itself;
- an API Gateway request ID;
- a Lambda invocation ID;
- a correlation ID;
- a trace ID; or
- an arbitrary transaction ID.

## 6. Resource-Reference Semantics

`resource_reference` is a stable, minimal, authorization-facing identifier or
handle used to refer to the governed Assessment Submission resource.

The preferred property is opaque stability. The reference should not
unnecessarily expose:

- personally identifiable information;
- client identity;
- Business Entity identity;
- authorization facts;
- authority-source internals; or
- implementation storage details.

This artifact does not prescribe UUID, database key format, route shape, token
format, table schema, or storage encoding.

A resource identifier is not authority. Possession of `R` does not establish:

- target legitimacy;
- Business Entity membership;
- Entitlement;
- permission;
- ALLOW.

## 7. Resource-Target Legitimacy Owner

The logical owner is:

```text
Governed Assessment Submission Resource-Target Authority
```

This authority is part of the governed application/resource architecture. Its
narrow responsibility is to establish that resource reference `R` is the actual
Assessment Submission target for the current governed application capability.

This v1 artifact does not automatically assign that authority to:

- Assessment Service;
- Website;
- browser;
- Lambda;
- API Gateway;
- Cognito;
- IAM;
- Bedrock;
- AI;
- database; or
- any concrete production service.

No concrete production owner is selected in v1.

## 8. Terminating Provenance Basis

Resource-reference provenance terminates in a deterministic governed
server-side target-resolution or workflow fact, owned by the Governed
Assessment Submission Resource-Target Authority, establishing that `R` is the
actual Assessment Submission target for the governed assessment-submission
application capability.

The provenance chain must not terminate at:

- caller assertion;
- route;
- body;
- UI selection;
- identifier syntax;
- Resource Identity lookup success;
- Principal identity;
- authentication success;
- AI classification;
- AWS/IAM identity.

## 9. Selected Provenance Model

The selected model is:

```text
MODEL H - BOUNDED HYBRID RESOURCE-TARGET PROVENANCE
```

A legitimate target may originate through either path:

```text
untrusted candidate reference
        -> governed deterministic trusted server-side target resolution
        -> already-legitimate Assessment Submission target fact
```

or:

```text
already-governed server-side workflow/resource context
        -> governed deterministic target establishment
        -> already-legitimate Assessment Submission target fact
```

Both paths converge on the same authority contract. Neither transport nor
Python representation creates legitimacy.

## 10. Candidate Input Boundary

A caller may provide a candidate resource identifier in a future integration.
Such input is:

```text
UNTRUSTED CANDIDATE INPUT ONLY
```

This applies whether the candidate arrives through:

- body;
- route/path parameter;
- query parameter;
- header;
- UI/browser;
- session;
- workflow input; or
- other transport.

Candidate input may be evidence to a governed server-side process. It is not a
trusted resource-target fact.

## 11. Minimum Provenance Facts

The minimum resource-target provenance facts are:

1. resource reference `R`;
2. Assessment Submission target semantics;
3. binding to the governed assessment-submission application capability /
   `PROTECTED_ASSESSMENT_SUBMISSION`;
4. provenance or producer authority reference sufficient to identify the
   governing target-establishment basis; and
5. provenance/version context sufficient for deterministic interpretation.

The provenance fact must not automatically duplicate:

- Principal;
- Membership;
- Entitlement;
- Business Entity permission;
- ALLOW/DENY.

## 12. Operation-Target Binding

The target fact must be semantically bound to:

```text
governed Assessment Submission application capability
        / PROTECTED_ASSESSMENT_SUBMISSION
```

Legitimacy must not be defined only against generic `RequestedAction.SUBMIT`.
`RequestedAction` is the downstream normalized authorization vocabulary, not
the application-level target owner.

## 13. Resource Identity Relationship

Resource-Target Provenance answers:

```text
WHY is R legitimately the target?
```

Resource Identity answers:

```text
WHAT governed resource does R resolve to?
```

Both are required. Neither replaces the other.

Resource Identity lookup success is not resource-target provenance. Resource
Identity lookup success is not permission. An attacker who guesses a valid `R`
must not gain authority merely because `R` resolves.

The following circular chain is prohibited:

```text
R is legitimate because Resource Identity found R.
Resource Identity may consume R because R was supplied.
```

Lookup success cannot establish the provenance required to justify lookup
consumption. The provenance basis must be independently governed.

## 14. Business Entity Relationship

The Assessment Submission resource belongs to or is scoped by a Governed
Business Entity:

```text
Assessment Submission resource R
        -> belongs to / is scoped by
        -> Governed Business Entity B
```

Resource Identity remains authoritative for the governed resource's Business
Entity binding unless a later separately governed authority model changes that
ownership.

Resource-target provenance need not duplicate authoritative Business Entity
binding. If a target-provenance producer carries Business Entity context as
evidence, it must not override contradictory authoritative Resource Identity
facts. Any mismatch must fail closed.

## 15. Subject / Permission Separation

Resource-target provenance establishes:

```text
this is target R
```

It does not establish:

```text
Principal P may submit to R
```

Authentication, Principal identity, Membership, and Entitlement remain separate
authorization predicates.

Membership answers a downstream governed relationship question. It does not
establish target provenance.

Entitlement answers downstream permission facts. It does not establish target
provenance.

## 16. Resource Cardinality

Each authorization decision for `PROTECTED_ASSESSMENT_SUBMISSION` must have
exactly one legitimate protected Assessment Submission resource target.

Required behavior:

| Condition | Required result |
| --- | --- |
| zero targets | fail closed |
| multiple targets | fail closed |
| ambiguous target | fail closed |
| conflicting target | fail closed |

No arbitrary first-match behavior is permitted.

## 17. Identifier Domain and Minimum Exposure

The resource-reference domain must be governed sufficiently to prevent:

- cross-resource collision;
- cross-Business-Entity substitution;
- cross-resource-class confusion.

This artifact does not freeze a physical encoding. Future realization may
choose an exact identifier format only after preserving these semantic
uniqueness requirements.

Opaque stable references are preferred over:

- PII-bearing identifiers;
- human identity fields;
- business-sensitive semantic composites.

The reasons are minimum necessary exposure, reduced enumeration/leakage, and
separation of authorization identity from presentation.

Identifier generation alone is not resource-target legitimacy. Generating a
UUID, random token, database key, or request ID does not establish that the
identifier represents a legitimate Assessment Submission target. A governed
creation, registration, resolution, or workflow fact must bind the identifier
to the resource semantics.

## 18. Lifecycle / Currentness Ownership

Resource Identity or the governed resource authority source remains responsible
for authoritative resource lifecycle/currentness unless later governance changes
that ownership.

Examples include:

- active;
- stale;
- revoked;
- deleted;
- superseded;
- closed;
- archived.

Resource-target provenance must not override a downstream stale, revoked,
inactive, invalid, or unavailable Resource Identity result.

A previously legitimate `R` may become unusable. Historical provenance is not
current authorization eligibility.

## 19. IDOR / BOLA and Resource Substitution

The required defense chain is:

```text
candidate R
        -> governed target provenance
        -> Resource Identity
        -> authoritative Business Entity binding
        -> Membership
        -> Entitlement
        -> Evaluator
        -> ALLOW / DENY
```

Changing `R1` to `R2` must not bypass any layer.

Resource substitution through any of the following is prohibited:

- caller-controlled identifier;
- body mutation;
- path mutation;
- UI mutation;
- session mutation;
- replayed stale reference;
- foreign Business Entity reference;
- wrong resource class.

All unresolved, mismatched, ambiguous, conflicting, or stale cases fail closed.

## 20. Deterministic Fail-Closed Rules

| Condition | Required handling |
| --- | --- |
| missing candidate | no trusted target fact |
| blank candidate | no trusted target fact |
| wrong type | no trusted target fact |
| malformed candidate | no trusted target fact |
| untrusted provenance | no trusted target fact |
| zero resolved legitimate targets | fail closed |
| multiple legitimate targets | fail closed |
| ambiguous target | fail closed |
| conflicting target | fail closed |
| unknown Resource Identity | downstream fail closed / DENY |
| stale Resource Identity | downstream fail closed / DENY |
| wrong ResourceClass | fail closed / no ALLOW |
| wrong operation-target binding | fail closed |
| Business Entity mismatch | DENY |
| missing Membership | DENY |
| missing Entitlement | DENY |

Failure to establish a trusted resource-target fact means authorization
evaluation must not proceed as though a valid target exists.

Do not fabricate a target merely to obtain DENY. Where existing evaluator
contracts require a decision, later integration governance may define a
deterministic translation into a denial/error path. This artifact does not
solve that runtime contract.

Target establishment must be deterministic. The following are prohibited:

- LLM judgment;
- heuristic guessing;
- best-match selection;
- first-match selection;
- probabilistic classification.

Ambiguity fails closed.

## 21. Authority-Laundering Prohibitions

The following must not create trusted target provenance:

- caller string -> trusted target;
- route -> trusted target;
- HTTP method -> trusted target;
- body -> trusted target;
- payload validation -> trusted target;
- request ID -> trusted target;
- Principal -> trusted target;
- Business Entity alone -> trusted target;
- UI selection -> trusted target;
- AI assertion -> trusted target;
- AWS/IAM -> trusted target;
- Resource Identity lookup success -> provenance;
- Python dataclass/enum construction -> real-world provenance.

## 22. Non-Authority Boundaries

Assessment Service is authoritative for deterministic assessment business truth
and scoring under its governed methodology.

That does not automatically make Assessment Service the authorization
resource-target authority.

```text
scoring authority != target-provenance authority != authorization authority
```

Website and browser remain presentation-only. They may allow a user to select
or submit a candidate target. They cannot produce the trusted resource-target
fact.

Server-side session or workflow context is not automatically authoritative. It
may establish target provenance only when produced under a separately governed
deterministic target-establishment process. Stored server-side state alone is
not a trust argument.

Authentication does not establish target provenance. A verified Principal may
still attempt to target the wrong resource.

Principal identity alone does not select the resource.

AI, LLM, agent, or MCP output cannot create authoritative resource-target
provenance. AI may never turn an untrusted candidate `R` into trusted `R` by
assertion.

The following do not establish business target provenance:

- IAM principal;
- Lambda identity;
- AWS account;
- API Gateway;
- Cognito group;
- infrastructure credential;
- execution role.

Infrastructure authority is not business authority.

API request ID, Lambda request ID, trace ID, and correlation ID must not be
treated as the governed Assessment Submission resource reference merely because
they are unique.

## 23. Bounded Non-Production Realization Implications

A future bounded non-production proof may demonstrate:

```text
already-legitimate Assessment Submission target fact
        -> bounded exact representation
        -> deterministic fail-closed handoff
        -> resource_reference
        -> existing resource/action + Resource Identity path
```

Such proof must not accept a raw caller string and simply rename it trusted.

If a future non-production implementation introduces a Python type representing
an already-legitimate target fact, construction of that Python type is
representational only. Exact type may protect a bounded software boundary.
Exact type does not prove real-world provenance.

This preserves the same principle established for:

- `NonProductionVerifiedAuthenticationFact`;
- `NonProductionApplicationCapability`.

## 24. Ceremonial Wrapper Prohibition

This is not sufficient:

```text
string
        -> dataclass
        -> trusted string
```

A future representation is meaningful only if it represents a fact whose
legitimacy is established by the governed Resource-Target Authority outside the
representation itself.

## 25. Deferred Runtime / Enforcement / TOCTOU Boundaries

This artifact defers final evaluator-request composition. It defines only what
resource-target provenance a future composer may consume.

This artifact defers decision consumption, decision enforcement, and business
execution gating.

Decision-to-execution TOCTOU remains downstream and open. Resource state,
Membership, Entitlement, version context, operation, Business Entity
relationship, or target status may change between authorization and execution.
This artifact governs target provenance, not complete decision-to-execution
stability.

## 26. Production Non-Authorization

Production Authority: NOT GRANTED.

Production Resource Integration: NOT GRANTED.

Production resource-target producer: NOT SELECTED.

Production resource authority source: NOT GRANTED.

Runtime Activation: NOT GRANTED.

Handler Integration: NOT GRANTED.

Route Binding: NOT GRANTED.

No concrete database, table, service, AWS component, schema, route, token
format, or persistence mechanism is selected by this artifact.

## 27. Open Questions

The following remain open for later reviews:

- exact opaque identifier encoding;
- exact non-production representation type name;
- exact production storage or service;
- exact future resource creation or registration mechanism;
- exact production Resource-Target Authority implementation;
- exact runtime integration point;
- exact final evaluator-request composition contract;
- exact enforcement contract;
- decision-to-execution TOCTOU controls.

The following are not open:

- what the protected resource is;
- whether caller input is trusted;
- whether lookup success proves provenance;
- who logically owns target legitimacy;
- what terminates provenance;
- whether target provenance equals permission;
- whether AI, AWS, or browser can create authority.

## 28. Governance Decision Summary

For the sole current protected operation `PROTECTED_ASSESSMENT_SUBMISSION`,
Trusted Authorization shall treat the protected target as exactly one governed
Assessment Submission resource of `ResourceClass.ASSESSMENT_SUBMISSION`.

A caller-supplied resource reference, transport value, payload value,
Principal, UI selection, AI output, infrastructure identity, identifier syntax,
or successful Resource Identity lookup does not establish target legitimacy.

Resource-target legitimacy terminates in a deterministic governed server-side
target-resolution or workflow fact owned by the Governed Assessment Submission
Resource-Target Authority.

A future bounded non-production representation may preserve that
already-legitimate fact but may not create it.

Resource Identity remains responsible for resolving the governed resource and
authoritative Business Entity/lifecycle facts.

Membership, Entitlement, applicability, version validation, and the evaluator
remain responsible for downstream authorization.

Production resource integration and production authority remain not granted.
