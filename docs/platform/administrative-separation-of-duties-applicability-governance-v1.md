# Administrative Separation of Duties Applicability Governance v1

Version: v1

## 1. Purpose

This artifact governs how the Separation-of-Duties (SoD) requirements
applicable to an authoritative Administrative Operation are determined from
authoritative context and applicable governance.

It closes the conceptual decision gap between governed SoD semantics and the
selection of those semantics for a concrete administrative operation. It does
not implement evaluation, administration, execution, persistence, or
authorization.

## 2. Governance Status

Administrative SoD applicability semantics are GOVERNED CONCEPTUALLY by this
artifact.

Concrete operation-specific requirement assignments are governed only when an
authoritative governance artifact explicitly establishes them. This v1
artifact establishes no fabricated operation-specific assignments and selects
no implementation.

## 3. Scope

This artifact governs:

- the Administrative Operation x SoD Requirement Applicability domain;
- the positive, deterministic relationship among an operation, its
  authoritative context, applicable governance/version, and its SoD
  Requirement Set;
- authoritative applicability inputs, result semantics, contextual binding,
  validity, conflict, revocation, supersession, replay, and fail-closed
  behavior;
- the applicability of SoD constraints already governed semantically by
  Administrative Separation of Duties Governance v1; and
- non-authority and non-selection boundaries necessary to keep applicability
  separate from administration, execution, authorization, persistence, and
  Resource x Action Applicability.

## 4. Non-Scope

This artifact does not define or select:

- a universal SoD, dual-control, maker/checker, human-approval, independent
  verification, participant-count, majority, or quorum requirement;
- an arbitrary operation-to-requirement matrix, risk score, sensitivity score,
  severity scale, or criticality model;
- the semantics of participant distinctness, authority independence,
  delegation-chain independence, or duty separation already governed by the
  predecessor SoD artifact;
- who creates, modifies, revokes, supersedes, or administers applicability
  rules;
- a concrete role, policy model, workflow, runtime, persistence technology,
  service contract, API, schema, or security implementation; or
- implementation, deployment, or production readiness.

## 5. Predecessor Governance

This artifact depends on and preserves:

- Administrative Separation of Duties Governance v1;
- Principal Mapping Administrative Execution Governance v1;
- Principal Mapping Administration Authority Governance v1;
- Principal Mapping Persistence Governance v1;
- Principal Mapping Authority Source Governance v1;
- Stable Principal Mapping Authority Governance v1;
- Business Entity Administration Authority Governance v1;
- Business Entity Authority Source Governance v1;
- Administrative Bootstrap / Root Authority Governance v1;
- Authority Administration / Revocation Governance v1;
- Membership Authority Source Governance v1;
- Entitlement Semantics Governance v1;
- Entitlement Authority Source Governance v1;
- Deterministic Authorization Decision Semantics v1;
- Resource x Action Applicability Governance v1;
- Resource Identity Authority Source Governance v1;
- Resource Provisioning / Classification Binding Governance v1;
- Resource Classification Authority Governance v1;
- Resource Classification Authority Source / Runtime Ownership Governance v1;
- Portal Governed Delivery Authorization Model v1;
- EIP Governed Retrieval Boundary v1; and
- Runtime Owner Assignment Governance v1.

Where predecessor governance is more restrictive, the more restrictive
boundary prevails.

## 6. Sufficiency Basis

Predecessor governance defines what valid SoD means when SoD is required. It
governs duties, participant distinctness, authority independence,
delegation-chain independence, validity, binding, result semantics, and
fail-closed evaluation.

It deliberately leaves concrete operation-specific applicability,
participant-count policy, human-participation policy, and SoD administration
downstream. No predecessor determines generally which SoD constraints apply to
an Administrative Operation in its authoritative context.

## 7. Inherited Semantics

This artifact inherits that:

- an Administrative Operation must be bounded by valid authority, target,
  operation, scope, lifecycle, Business Entity where applicable, and
  governance/version context;
- SoD is an additional constraint only where applicable governance requires
  it;
- SoD satisfaction does not establish administrative authority, execution, or
  Resource authorization;
- self-grant, circular authority, privilege escalation, and authority by
  technical control are prohibited;
- stale, revoked, conflicting, or unresolved authority fails closed; and
- producer/consumer ownership, Business Entity isolation, deterministic
  behavior, and minimum-disclosure requirements remain unchanged.

## 8. Terminology

For this artifact:

- Administrative Operation means a bounded authority-relevant operation under
  applicable administrative governance.
- Authoritative Context means the governed facts material to applicability,
  including target, authority domain, scope, Business Entity where applicable,
  lifecycle transition, authority impact, and governance/version context.
- Applicability Fact means an attributable, authority-backed proposition that
  maps a bounded operation/context to one or more SoD requirements or
  affirmatively to no additional SoD requirement.
- SoD Requirement means a constraint whose semantics are governed by
  Administrative Separation of Duties Governance v1.
- SoD Requirement Set means the exact set of SoD requirements applicable to
  one bounded operation/context. An empty set is valid only when affirmatively
  established by authoritative governance.
- Applicability Determination means the deterministic result of resolving
  authoritative Applicability Facts for one bounded operation/context.

## 9. Central Applicability Question

The bounded question is:

Given an authoritative Administrative Operation and its Authoritative Context,
which SoD requirements apply under the applicable governance/version?

Conceptually:

```text
ADMINISTRATIVE OPERATION
+ AUTHORITATIVE CONTEXT
+ APPLICABLE GOVERNANCE / VERSION
-> SOD APPLICABILITY DETERMINATION
```

## 10. Core Domain Separations

The following separations are mandatory:

```text
SOD SEMANTICS != SOD APPLICABILITY
SOD APPLICABILITY != ADMINISTRATIVE AUTHORITY
SOD APPLICABILITY != RESOURCE AUTHORIZATION
SOD APPLICABILITY != EXECUTION AUTHORITY
SOD APPLICABILITY != PERSISTENCE
SOD APPLICABILITY != WORKFLOW CONFIGURATION
```

The predecessor SoD artifact remains authoritative for what each requirement
means. This artifact governs when a requirement is selected for a bounded
operation/context.

## 11. Applicability Domain

The governed domain is:

```text
Administrative Operation x Authoritative Context
-> SoD Requirement Set
```

The domain concerns administrative constraints. It does not classify Resource
access, establish Resource action semantics, or produce an authorization
decision.

## 12. Resource x Action Applicability Separation

```text
RESOURCE x ACTION APPLICABILITY
!=
ADMINISTRATIVE OPERATION x SOD REQUIREMENT APPLICABILITY
```

Resource x Action Applicability determines whether a canonical Principal-facing
action applies to a governed Resource class/context. SoD applicability
determines which additional duty-separation constraints apply to an
Administrative Operation/context.

Neither domain establishes, substitutes for, or repairs the other. Resource x
Action Applicability Governance v1 remains unchanged.

## 13. Positive Applicability Model

For Administrative Operation O, Authoritative Context C, and applicable
governance/version G:

```text
Applicability(O, C, G) -> R
```

R is an exact SoD Requirement Set only when deterministic validation
establishes:

- O and all context facts material to applicability;
- an authoritative basis for each relied-upon Applicability Fact;
- exact operation, target, authority-domain, scope, lifecycle, Business Entity
  where applicable, authority-impact, and governance/version binding;
- current validity and absence of applicable revocation or supersession;
- a coherent resolution of all authoritative Applicability Facts; and
- sufficient provenance.

Otherwise the result MUST be INDETERMINATE.

## 14. Authoritative Inputs

Applicability evaluation MUST use only facts whose authority is governed for
the purpose in which they are relied upon.

Minimum inputs are the Administrative Operation, exact target, applicable
authority domain, governed scope, Business Entity context where applicable,
material lifecycle state or transition, material authority-impact semantics,
applicable Applicability Facts, and governance/version context.

An input MAY be omitted only when applicable governance affirmatively
establishes that it is immaterial to the determination. Arbitrary metadata,
presentation labels, infrastructure state, and unsupported inference are not
authoritative inputs.

## 15. SoD Requirement References

An authoritative Applicability Fact MAY reference requirements whose semantics
are governed by Administrative Separation of Duties Governance v1, including:

- participant distinctness;
- authority independence;
- delegation-chain independence;
- request / approval separation;
- approval / execution separation;
- execution / verification separation;
- participant-count requirements;
- human authoritative participation;
- duty-ordering requirements; and
- independent authoritative verification.

This artifact does not redefine those semantics. An applicability reference
MUST be precise enough to identify the exact governed constraint.

## 16. Applicability Result Semantics

Applicability outcomes are:

- REQUIREMENTS APPLICABLE: authoritative governance establishes an exact,
  non-empty SoD Requirement Set for the operation/context;
- NO ADDITIONAL SOD REQUIREMENT: authoritative governance affirmatively
  establishes an empty SoD Requirement Set for the operation/context; and
- INDETERMINATE: authoritative facts cannot establish one coherent result.

```text
INDETERMINATE != NO ADDITIONAL SOD REQUIREMENT
INDETERMINATE != PERMITTED
NO ADDITIONAL SOD REQUIREMENT != AUTHORIZED
NO ADDITIONAL SOD REQUIREMENT != EXECUTION PERMISSION
REQUIREMENTS APPLICABLE != SOD SATISFIED
SOD SATISFIED != AUTHORIZED
```

## 17. Conditional Applicability

This artifact explicitly rejects:

```text
ALL ADMINISTRATIVE OPERATIONS REQUIRE SOD
ALL OPERATIONS REQUIRE TWO PEOPLE
ALL OPERATIONS REQUIRE HUMAN APPROVAL
ALL OPERATIONS REQUIRE MAKER/CHECKER
ALL OPERATIONS REQUIRE INDEPENDENT VERIFICATION
ALL OPERATIONS REQUIRE A QUORUM
```

SoD applicability MUST derive from explicit authoritative governance for the
bounded operation/context. Neither application nor exemption is inferred from
operation labels alone.

## 18. Administrative Operation Coverage

Existing governed operation semantics are consumed without redefinition,
including where applicable:

- ESTABLISH;
- ACTIVATE;
- MODIFY;
- REPLACE;
- SUPERSEDE;
- DEACTIVATE;
- REVOKE;
- RESTORE / REACTIVATE; and
- REMAP.

The existence of an operation in this taxonomy does not itself assign an SoD
Requirement Set.

## 19. Operation-Specific Applicability

Operation type MAY be an authoritative applicability dimension. A rule for one
operation MUST NOT be inferred for another.

This artifact establishes the structure and validity requirements for
operation-specific rules. It does not invent a rule such as REVOKE always
requires a named separation unless authoritative governance expressly supports
that rule.

## 20. Authority-Impact Context

Applicability MAY depend on governed authority impact, including establishment,
expansion, reduction, replacement, revocation, and restoration.

Authority impact MUST be determined from governed operation semantics and
context. It MUST NOT be guessed from labels, estimated numerically, or inferred
from technical effort.

## 21. Target Binding

An Applicability Determination MUST be bound to the exact governed target or
target class expressly identified by authoritative governance.

A result for target T1 MUST NOT be reused for T2 merely because the targets
share a label, storage location, technical owner, or presentation route.

## 22. Operation Binding

An Applicability Determination for operation O1 MUST NOT establish
applicability for O2.

```text
MODIFY != REVOKE
DEACTIVATE != REVOKE
RESTORE != ACTIVATE necessarily
REMAP != REPLACE necessarily
```

Operation aliases MUST NOT broaden the governed applicability result.

## 23. Scope Binding

Applicability MUST be bound to the governed administrative scope.

A determination for scope S1 MUST NOT transfer to S2 unless authoritative
governance explicitly establishes equivalence. Technical reach beyond S1 does
not broaden applicability authority.

## 24. Lifecycle Binding

Applicability MUST be valid for the material lifecycle state and transition.

A requirement set for establishment, activation, modification, replacement,
supersession, deactivation, revocation, restoration, or remapping MUST NOT
automatically transfer to an incompatible lifecycle state or transition.

## 25. Business Entity Binding

Where Business Entity context applies, applicability MUST be bound to the exact
authoritative Business Entity or an explicitly governed class of contexts.

```text
B1 APPLICABILITY != B2 APPLICABILITY
```

Participation in, administration of, or technical access to B1 MUST NOT
establish applicability for B2.

## 26. Governance / Version Binding

Applicability Facts and determinations MUST be interpreted under the applicable
governance/version context.

A historical result under G1 MUST NOT be reused under materially incompatible
G2 without a current authoritative basis. This artifact selects no version
storage or deployment mechanism.

## 27. Participant Distinctness Applicability

Applicable governance MAY require participant distinctness for a bounded
operation/context.

This artifact governs selection of that requirement, not what distinctness
means. Administrative Separation of Duties Governance v1 remains authoritative
for Principal, account, session, device, role, and temporal distinctness
semantics.

## 28. Authority Independence Applicability

Applicable governance MAY require authority independence separately from
participant distinctness.

```text
PARTICIPANT DISTINCTNESS != AUTHORITY INDEPENDENCE
```

One requirement MUST NOT imply the other unless the authoritative
Applicability Fact selects both or predecessor governance expressly establishes
the dependency.

## 29. Delegation-Chain Independence Applicability

Applicable governance MAY require delegation-chain independence for a bounded
operation/context.

Delegation does not establish applicability authority and does not imply
independence. The predecessor SoD artifact remains authoritative for whether a
delegation chain satisfies a selected independence requirement.

## 30. Request / Approval Applicability

Applicable governance MAY require request / approval separation for a bounded
operation/context.

This requirement is not universal. A requestor, approver, UI, runtime, or
workflow MUST NOT select or waive it by preference.

## 31. Approval / Execution Applicability

Applicable governance MAY require approval / execution separation for a
bounded operation/context.

This requirement is not universal. Principal Mapping Administrative Execution
Governance v1 remains authoritative for execution eligibility, Execution Actor
non-authority, and decision/execution binding.

## 32. Execution / Verification Applicability

Applicable governance MAY require independent authoritative verification for a
bounded operation/context.

The selected requirement MUST distinguish independent participant verification
from deterministic technical verification. This artifact does not universally
require either a human verifier or an additional Participant.

## 33. Participant-Count Applicability

Participant count MAY be a governed applicability dimension where an
authoritative rule establishes it.

This artifact selects no universal count, minimum count, quorum, majority, or
voting rule. A count cannot substitute for participant authority,
distinctness, or independence.

Concrete participant-count policy remains DOWNSTREAM / NOT SELECTED.

## 34. Human-Participation Applicability

Human authoritative participation MAY be a governed applicability dimension
where an authoritative rule establishes it.

This artifact does not impose universal human approval. Where human
participation is required, AI, automation, a technical account, or a stored
label MUST NOT substitute for the authoritative human Participant required by
the selected SoD semantics.

Concrete human-participation policy remains DOWNSTREAM / NOT SELECTED.

## 35. Revocation Applicability

Revocation operations MAY have context-specific SoD requirements, but this
artifact does not create revocation authority or impose universal dual control.

Authority Administration / Revocation Governance v1 and applicable domain
governance remain authoritative for revocation meaning, authority, lifecycle,
and precedence.

## 36. Restoration / Reactivation Applicability

Restoration or reactivation MAY have context-specific SoD requirements.

```text
AUTHORITY TO REVOKE != AUTHORITY TO RESTORE necessarily
```

An applicability determination does not create restoration authority, restore
revoked state, or allow historical participation to satisfy current
requirements.

## 37. Bootstrap / Root-Sensitive Applicability

Bootstrap or Root Administrative Authority operations MAY be subject to SoD
requirements only where applicable governance establishes them.

Administrative Bootstrap / Root Authority Governance v1 remains authoritative
for legitimacy, terminating authority basis, lifecycle, non-circularity, and
fail-closed behavior. Multiple unauthorized actors and agreement MUST NOT
manufacture root authority.

## 38. Self-Grant Boundary

SoD applicability does not legalize self-grant.

```text
SOD REQUIRED != SELF-GRANT PERMITTED
SOD SATISFIED != SELF-GRANT LEGITIMATE
```

Every predecessor self-grant and circular-authority prohibition remains in
force regardless of the Applicability Determination.

## 39. Privilege-Escalation Boundary

Applicability MUST NOT create or expand administrative authority, Business
Entity scope, delegation authority, Membership, Entitlement, Resource
authorization, or execution authority.

Selecting additional constraints cannot authorize an operation; selecting no
additional constraint cannot waive independently required authority.

## 40. Applicability Authority Basis

An authoritative Applicability Fact MUST derive from governed authority over
the applicability determination and MUST be:

- attributable to its authority basis;
- sufficiently provenance-backed;
- bound to the applicable operation/context;
- lifecycle-current where applicable;
- valid under the applicable governance/version; and
- deterministically resolvable with other authoritative facts.

This positive authority model governs required properties. The concrete source
and administration of Applicability Facts remain downstream.

## 41. Technical Source Non-Authority

The following separations are mandatory:

```text
DATABASE RECORD != SOD APPLICABILITY AUTHORITY
CONFIGURATION != SOD APPLICABILITY AUTHORITY
WORKFLOW SETTING != SOD APPLICABILITY AUTHORITY
API RESPONSE != SOD APPLICABILITY AUTHORITY automatically
IAM != SOD APPLICABILITY AUTHORITY
COGNITO != SOD APPLICABILITY AUTHORITY
BROWSER STATE != SOD APPLICABILITY AUTHORITY
AI OUTPUT != SOD APPLICABILITY AUTHORITY
```

A technical representation MAY carry authoritative evidence only when an
independently governed authority basis and all validity requirements are
established.

## 42. Applicability Establishment / Resolution Separation

Establishing an authoritative Applicability Fact and resolving applicable facts
for a concrete operation are distinct responsibilities.

```text
APPLICABILITY RESOLVER != APPLICABILITY AUTHORITY
```

A resolver MUST consume authoritative facts and MUST NOT create, broaden,
waive, or repair the facts governing its own result.

## 43. Applicability Administration Boundary

```text
SOD APPLICABILITY SEMANTICS != SOD APPLICABILITY ADMINISTRATION
```

This artifact does not determine who creates, modifies, revokes, supersedes,
or administers Applicability Facts or operation-specific rules. Applicability
administration authority, lifecycle operations, and execution remain
DOWNSTREAM / UNRESOLVED.

No Participant gains administration authority by being subject to, resolving,
or satisfying an applicability rule.

## 44. Persistence Boundary

```text
PERSISTED APPLICABILITY != AUTHORITATIVE APPLICABILITY automatically
PERSISTENCE WRITE != APPLICABILITY AUTHORITY
```

Persistence MAY represent Applicability Facts and determinations but MUST NOT
manufacture authority, current validity, or a NO ADDITIONAL SOD REQUIREMENT
result.

Applicability persistence and persistence technology remain DOWNSTREAM / NOT
SELECTED.

## 45. Runtime Boundary

This artifact does not select an applicability evaluator, runtime owner,
evaluation service, policy engine, workflow engine, Lambda, API, database, or
execution placement.

```text
RUNTIME OWNER != SOD APPLICABILITY AUTHORITY
```

Runtime and runtime ownership remain DOWNSTREAM / NOT SELECTED.

## 46. Service Contract Boundary

This artifact does not define an endpoint, API contract, request schema,
response schema, interface, SDK, transport, service ownership, or Trusted
Authorization Service Contract.

SoD applicability service-contract governance remains DOWNSTREAM / NOT
SELECTED.

## 47. Policy Model Non-Selection

This artifact does not select RBAC, ABAC, ACL, OPA, Cedar, IAM roles, Cognito
groups, or another policy engine as the SoD applicability policy model.

Applicability semantics and authority precede any future representation.

## 48. Resource Classification Separation

```text
RESOURCE CLASSIFICATION != ADMINISTRATIVE SOD REQUIREMENT
```

Resource Classification MUST NOT be repurposed as an administrative-operation
sensitivity, severity, or SoD requirement. Any future relationship would
require explicit governance and MUST preserve the distinct authority domains.

## 49. Principal Boundary

SoD applicability MAY consume authoritative Principal-related facts only where
legitimately material to an approved applicability rule.

It MUST NOT establish, modify, infer, or repair Principal identity or Principal
Mapping authority.

## 50. Membership Boundary

```text
SOD APPLICABILITY != MEMBERSHIP
```

Applicability evaluation MUST NOT establish, modify, revoke, restore, or infer
Membership.

## 51. Entitlement Boundary

```text
SOD APPLICABILITY != ENTITLEMENT
```

Applicability MUST NOT independently grant VIEW, DOWNLOAD, SUBMIT, EXPLAIN, or
any other Resource action.

## 52. Resource Authorization Boundary

```text
SOD APPLICABILITY != RESOURCE AUTHORIZATION
SOD SATISFACTION != RESOURCE AUTHORIZATION ALLOW
```

SoD applicability constrains administrative operations where required. It does
not replace deterministic Resource authorization or produce ALLOW.

## 53. Cognito Boundary

Cognito MAY support authentication or technical identity. Cognito groups,
claims, attributes, administrator status, or configuration MUST NOT
authoritatively determine business SoD applicability.

```text
COGNITO TECHNICAL STATE != SOD APPLICABILITY AUTHORITY
```

## 54. IAM Boundary

IAM technical permission MUST NOT establish, change, waive, or satisfy SoD
applicability.

```text
IAM PERMISSION != BUSINESS SOD APPLICABILITY AUTHORITY
```

## 55. Website / Browser Boundary

Website, Portal, and browser remain presentation and request consumers.

UI state, submitted values, hidden fields, routes, local storage, cookies,
sessions, displayed exemptions, or client-side workflow state MUST NOT
authoritatively determine whether SoD applies or which constraints apply.

## 56. AI Boundary

AI MAY explain an approved Applicability Determination only where future
authorized architecture permits.

AI MUST NOT authoritatively decide applicability, invent missing Applicability
Facts, downgrade INDETERMINATE to NO ADDITIONAL SOD REQUIREMENT, waive SoD,
establish authority, override governance, select a requirement by risk guess,
or manufacture provenance.

## 57. Assessment Service Boundary

The Assessment Service remains the certified deterministic producer of
assessment business truth within its governed domain.

This artifact assigns it no SoD applicability, SoD administration,
administrative authorization, approval, or administrative execution
responsibility and authorizes no Assessment Service change.

## 58. EIP Boundary

EIP remains a governed consumer and derivation platform within its approved
domain.

EIP MUST NOT become SoD applicability authority, approval authority,
administrative authority, Principal authority, or Resource authorization
authority. No EIP change is authorized.

## 59. Technology Neutrality

This artifact is technology-neutral.

Named technologies appear only to establish non-authority, non-selection, or
architecture boundaries. No identity provider, database, workflow, runtime,
cloud service, policy engine, API, approval product, ticketing product, role
model, or security product is recommended or selected.

## 60. Determinism

Applicability Determination MUST be deterministic:

```text
same authoritative Administrative Operation facts
+ same authoritative Applicability Facts
+ same governance/version context
-> same SoD Applicability Determination
```

Heuristic, probabilistic, AI-based, best-guess, convenience-based, and
subjective applicability resolution are prohibited.

## 61. Fail-Closed Applicability

Applicability MUST fail closed when a coherent current result cannot be
affirmatively established, including for:

- unresolved operation, target, authority domain, or scope;
- unresolved Business Entity, lifecycle, or authority-impact context where
  material;
- missing authoritative Applicability Facts;
- conflicting, stale, revoked, expired, or superseded Applicability Facts;
- incompatible governance/version;
- insufficient authority provenance; or
- ambiguous applicability.

```text
INDETERMINATE MUST NEVER BE INTERPRETED AS NO ADDITIONAL SOD REQUIREMENT
```

Fail-closed applicability constrains administrative progression. It does not
itself produce a Resource authorization decision.

## 62. Conflict Handling

Conflicting authoritative Applicability Facts MUST NOT silently resolve to an
empty or weaker SoD Requirement Set.

This artifact selects no voting, majority, quorum, source-priority,
last-write-wins, or tie-breaker rule. If applicable governance cannot
deterministically resolve the conflict, the result MUST be INDETERMINATE.

## 63. Stale Applicability

An Applicability Determination MUST NOT automatically survive a material change
to operation, target, authority domain, scope, Business Entity, lifecycle,
authority impact, authoritative Applicability Facts, or governance/version.

Current applicability MUST be re-established before materially relying on a
historical result.

## 64. Revocation / Supersession of Applicability

Revoked, expired, invalid, or superseded Applicability Facts MUST NOT remain
current merely because historical evidence or a persisted representation
exists.

Current revocation and supersession take precedence over stale affirmative or
empty-set results. This artifact defines no administration mechanism.

## 65. Provenance

Material Applicability Determinations MUST have sufficient conceptual
provenance to reconstruct:

- the relied-upon Applicability Facts and their authority basis;
- operation, target, authority domain, scope, lifecycle, authority impact, and
  Business Entity context where applicable;
- applicable governance/version;
- validity, revocation, supersession, and conflict interpretation; and
- the resulting SoD Requirement Set or INDETERMINATE outcome.

```text
PROVENANCE != APPLICABILITY AUTHORITY
```

This artifact selects no provenance format or storage.

## 66. Auditability

Applicability Determinations MUST be deterministically auditable, including
REQUIREMENTS APPLICABLE, NO ADDITIONAL SOD REQUIREMENT, and INDETERMINATE.

```text
AUDIT RECORD != APPLICABILITY AUTHORITY
AUDIT RECORD != SOD SATISFACTION
AUDIT RECORD != ADMINISTRATIVE AUTHORIZATION
```

Auditability does not select observability technology.

## 67. Privacy / Minimum Disclosure

Applicability evaluation, provenance, and auditability MUST use only
information necessary for the governed purpose.

This artifact does not require unnecessary exposure of raw identity-provider
claims, credentials, tokens, email, username, unrelated Business Entity data,
unrelated Membership, unrelated Entitlement, unrelated Resource data, or
producer business truth.

Governed identifiers and bounded authority references SHOULD be used where
sufficient.

## 68. Idempotence

Repeated evaluation of identical authoritative inputs under the same
governance/version context MUST produce the same Applicability Determination
and MUST NOT create authority, add requirements, remove requirements, or turn
INDETERMINATE into an affirmative result merely because evaluation was
repeated.

This is semantic idempotence and selects no idempotency technology.

## 69. Replay

Historical Applicability Facts or determinations MUST NOT automatically remain
valid after revocation, supersession, operation change, target change, scope
change, lifecycle change, Business Entity change, authority-impact change, or
governance/version change.

Replay requires current applicability validity to be affirmatively
re-established. Otherwise the result MUST be INDETERMINATE.

## 70. Concurrency

Concurrent Applicability Facts and lifecycle changes MUST preserve a
deterministic authoritative interpretation.

If concurrent state is conflicting or ordering materially affects the
requirement set and authoritative ordering cannot be determined, applicability
MUST fail closed. This artifact selects no transaction, lock, lease, quorum,
consensus, or workflow technology.

## 71. Side-Effect Safety

Applicability establishment, resolution, evaluation, and audit MUST NOT
themselves:

- create, expand, revoke, or restore authority;
- create or modify Principal, Business Entity, Membership, or Entitlement
  state;
- authorize Resource access;
- execute an Administrative Operation;
- mutate persistence;
- alter assessment business truth or EIP derived truth; or
- modify the SoD Requirement Set being evaluated.

## 72. Applicability Self-Modification Prohibition

A Participant in an Administrative Operation MUST NOT weaken, remove, broaden,
or reinterpret the SoD applicability requirement governing that same operation
merely through participation in the operation.

Any applicability-rule administration requires separate valid authority and
governance. No self-referential applicability change may legitimize itself.

## 73. Requestor Non-Authority

```text
REQUESTOR ASSERTS SOD NOT REQUIRED
!=
AUTHORITATIVE NO ADDITIONAL SOD REQUIREMENT
```

A request MAY carry a claimed context for evaluation but MUST NOT establish its
own exemption.

## 74. Approver Non-Authority

```text
APPROVER ASSERTS SOD NOT REQUIRED
!=
AUTHORITATIVE NO ADDITIONAL SOD REQUIREMENT
```

An Approver's authority for an administrative duty does not include
applicability-rule authority unless separately and independently governed.

## 75. Execution Actor Non-Authority

```text
EXECUTOR TECHNICALLY CAN EXECUTE != SOD NOT APPLICABLE
```

Execution capability, a prior PERMITTED decision, or technical success MUST
NOT establish or waive the applicable SoD Requirement Set.

## 76. Runtime Owner Non-Authority

```text
RUNTIME OWNERSHIP != SOD APPLICABILITY AUTHORITY
```

Owning, operating, deploying, or configuring a runtime does not authorize its
owner to select or waive business SoD requirements.

## 77. Persistence Owner Non-Authority

```text
ABILITY TO WRITE THE RECORD
!=
ABILITY TO ESTABLISH THE GOVERNED APPLICABILITY FACT
```

A direct write without valid applicability authority and provenance MUST NOT
be normalized into an authoritative result.

## 78. Risk Model Non-Selection

This artifact does not create or require a risk score, sensitivity score,
severity scale, criticality score, or probabilistic classification for
Administrative Operations.

Applicability MAY rely on governed operation and authority-impact semantics
without a separate risk-scoring prerequisite.

## 79. Role Model Non-Selection

This artifact does not define Approver Role, Security Administrator, Tenant
Administrator, Super Administrator, Maker, Checker, or another organizational
role.

Conceptual duties and requirement references MUST NOT be interpreted as a
selected staffing or role topology.

## 80. Workflow Non-Selection

This artifact does not define a workflow topology or select a ticket system,
approval queue, workflow engine, state-machine implementation, notification
system, command, event, message, or orchestration technology.

Applicability ordering, validity, and fail-closed requirements do not imply a
workflow design.

## 81. Concrete v1 Operation Rules

The reviewed predecessor corpus establishes no general authoritative basis for
assigning a concrete SoD Requirement Set to every ESTABLISH, ACTIVATE, MODIFY,
REPLACE, SUPERSEDE, DEACTIVATE, REVOKE, RESTORE / REACTIVATE, or REMAP
operation.

Accordingly, this v1 artifact does not fabricate operation-specific rules.
For a concrete operation/context:

- an explicit authoritative applicability rule produces the exact governed
  SoD Requirement Set;
- an explicit authoritative no-additional-requirement rule produces NO
  ADDITIONAL SOD REQUIREMENT; and
- absence, ambiguity, conflict, or invalidity produces INDETERMINATE.

Concrete operation-specific SoD rules remain DOWNSTREAM / UNRESOLVED until
separately established by valid governance.

## 82. Authority / Governance Status Model

| Governance area | Status |
| --- | --- |
| Administrative SoD semantic model | GOVERNED BY PREDECESSOR |
| Administrative SoD applicability domain | GOVERNED CONCEPTUALLY |
| Applicability authority basis requirements | GOVERNED CONCEPTUALLY |
| Applicability establishment / resolution separation | GOVERNED |
| Positive deterministic applicability model | GOVERNED CONCEPTUALLY |
| Applicability result semantics | GOVERNED CONCEPTUALLY |
| Conditional applicability | GOVERNED |
| Contextual target, operation, scope, lifecycle, Business Entity, authority-impact, and governance/version binding | GOVERNED CONCEPTUALLY |
| Participant-distinctness applicability | GOVERNED STRUCTURALLY; CONCRETE RULES DOWNSTREAM |
| Authority-independence applicability | GOVERNED STRUCTURALLY; CONCRETE RULES DOWNSTREAM |
| Delegation-chain-independence applicability | GOVERNED STRUCTURALLY; CONCRETE RULES DOWNSTREAM |
| Request / approval applicability | GOVERNED STRUCTURALLY; CONCRETE RULES DOWNSTREAM |
| Approval / execution applicability | GOVERNED STRUCTURALLY; CONCRETE RULES DOWNSTREAM |
| Execution / verification applicability | GOVERNED STRUCTURALLY; CONCRETE RULES DOWNSTREAM |
| Revocation, restoration, and bootstrap-sensitive applicability | GOVERNED STRUCTURALLY; CONCRETE RULES DOWNSTREAM |
| Deterministic applicability | GOVERNED |
| Fail-closed applicability | GOVERNED |
| Applicability provenance and auditability | GOVERNED CONCEPTUALLY |
| Privacy / minimum disclosure | GOVERNED / PRESERVED |
| Concrete operation-specific SoD rules | DOWNSTREAM / UNRESOLVED |
| Participant-count policy | DOWNSTREAM / NOT SELECTED |
| Human-participation policy | DOWNSTREAM / NOT SELECTED |
| SoD applicability administration | DOWNSTREAM / UNRESOLVED |
| SoD applicability persistence | DOWNSTREAM / NOT SELECTED |
| SoD applicability runtime and ownership | DOWNSTREAM / NOT SELECTED |
| SoD applicability service contract | DOWNSTREAM / NOT SELECTED |
| Policy model | DOWNSTREAM / NOT SELECTED |
| Concrete organizational roles | DOWNSTREAM / NOT SELECTED |
| Risk / sensitivity model | NOT SELECTED |
| Workflow technology | DOWNSTREAM / NOT SELECTED |
| Security / IAM implementation | DOWNSTREAM / NOT SELECTED |
| Implementation | UNAUTHORIZED |

No downstream, unresolved, or not-selected concern is resolved by implication.

## 83. Resolved Here

This artifact resolves only conceptual governance for:

- the distinction between SoD semantics and SoD applicability;
- the Administrative Operation x Authoritative Context to SoD Requirement Set
  domain;
- the positive applicability model and minimum authoritative inputs;
- applicability authority properties and establishment/resolution separation;
- requirement-set result semantics, including affirmative empty-set and
  INDETERMINATE treatment;
- conditional applicability and structural selection of predecessor SoD
  constraints;
- target, operation, scope, lifecycle, Business Entity, authority-impact, and
  governance/version binding;
- deterministic, fail-closed, conflict, staleness, revocation, supersession,
  idempotence, replay, and concurrency semantics;
- provenance, auditability, privacy, and side-effect safety; and
- the domain, non-authority, and non-selection boundaries defined here.

This artifact does not claim operation-policy completion, implementation
readiness, or production readiness.

## 84. Remaining Governance

The following remain unresolved or downstream unless separately governed:

- concrete operation- and context-specific SoD Requirement Sets;
- participant-count policy where required;
- human-authoritative-participation policy where required;
- SoD applicability administration authority and lifecycle operations;
- SoD applicability persistence and persistence administration;
- SoD applicability runtime and runtime ownership;
- SoD applicability service contract;
- concrete role and organizational topology;
- emergency / break-glass governance;
- Business Entity persistence;
- Resource Provisioning Authority;
- Resource Identity Administration Authority;
- Resource Identity Persistence Authority;
- Classification / Binding Administration Authority;
- Classification / Binding Persistence Authority;
- Resource Applicability Administration;
- Engagement Scope;
- Trusted Authorization Service Contract;
- Authorization Persistence;
- Authorization Audit / Observability;
- Security / IAM Boundary and enforcement; and
- explicit implementation authorization.

Completed predecessor governance remains authoritative and is not reopened by
this list.

## 85. Implementation Gate

ADMINISTRATIVE / AUTHORIZATION / EXECUTION / PERSISTENCE / SEPARATION-OF-DUTIES APPLICABILITY IMPLEMENTATION REMAINS UNAUTHORIZED.

This artifact does not authorize:

- administrative, authorization, execution, persistence, SoD, or SoD
  applicability runtime implementation;
- an API, endpoint, service contract, policy engine, workflow, database, queue,
  role model, or security implementation;
- IAM or Cognito changes;
- Website or Portal changes;
- Assessment Service changes;
- EIP changes;
- AWS AI Knowledge Assistant changes;
- deployment; or
- production readiness.

Implementation requires separate approved governance, ownership review,
bounded implementation planning, and explicit authorization in the correct
owning repository.

## 86. Adversarial Applicability Review

The following outcomes are mandatory:

- A. A Requestor says SoD does not apply: the assertion is not authoritative,
  and applicability remains governed by valid Applicability Facts.
- B. An Approver says SoD does not apply: approval authority does not imply
  applicability authority, and the assertion cannot establish an exemption.
- C. An Executor says SoD does not apply because IAM permits execution: IAM
  and execution capability do not establish applicability; unresolved facts
  produce INDETERMINATE.
- D. A Cognito group labels an operation exempt: Cognito state is not business
  applicability authority.
- E. Browser state submits NO ADDITIONAL SOD REQUIREMENT: client state cannot
  establish the result without authoritative facts and provenance.
- F. AI infers an operation is low risk and waives SoD: AI cannot establish,
  weaken, or waive applicability.
- G. Resource Classification is reused as administrative-operation
  sensitivity without governance: the domains are distinct and applicability
  is INDETERMINATE.
- H. Resource x Action Applicability says VIEW is APPLICABLE and is treated as
  SoD applicability: the domain substitution is invalid and cannot establish a
  SoD Requirement Set.
- I. Applicability valid for B1 is reused for B2: Business Entity binding fails
  unless authoritative governance expressly establishes equivalence.
- J. Applicability valid for MODIFY is reused for REVOKE: operation binding
  fails.
- K. Applicability valid for S1 is reused for S2: scope binding fails.
- L. Applicability valid under G1 is reused under incompatible G2:
  governance/version binding fails and current applicability must be
  re-established.
- M. Applicability evidence is revoked while its historical record remains:
  revocation takes precedence and historical presence cannot establish current
  applicability.
- N. Conflicting authoritative Applicability Facts exist: the result is
  INDETERMINATE unless applicable governance deterministically resolves the
  conflict.
- O. Applicability cannot be determined: the result is INDETERMINATE, never NO
  ADDITIONAL SOD REQUIREMENT.
- P. Runtime configuration says no approval is required while authoritative
  applicability is unresolved: configuration cannot waive SoD, and the result
  is INDETERMINATE.
- Q. A persistence record says NO ADDITIONAL SOD REQUIREMENT without authority
  provenance: the record is non-authoritative and applicability is
  INDETERMINATE.
- R. The same applicability inputs are evaluated twice: semantic idempotence
  requires the same result without new authority or changed requirements.
- S. An operation Participant changes the applicability requirement governing
  the same operation: self-modification cannot legitimize itself and the
  operation fails closed.
- T. AI recommends two-person approval where no authoritative requirement
  exists: the recommendation is not an Applicability Fact and cannot add a
  business requirement authoritatively.
- U. Two Participants satisfy selected SoD but administrative authority is
  absent: SoD satisfaction does not create authority, so the operation cannot
  progress affirmatively.
- V. Applicability is NO ADDITIONAL SOD REQUIREMENT but administrative
  authority is absent: the empty requirement set does not authorize the
  operation.
- W. A bootstrap operation uses multiple unauthorized actors to manufacture
  legitimacy: consensus does not create Root Administrative Authority and the
  operation fails closed.
- X. Old applicability evidence is replayed after lifecycle change: current
  validity must be re-established or applicability is INDETERMINATE.

## 87. Duplication Review

This artifact does not reproduce Administrative Separation of Duties
Governance v1. It references that artifact's requirement semantics and adds the
distinct operation/context-to-requirement-set authority model.

It does not reproduce Resource x Action Applicability Governance v1. It
establishes a separate administrative applicability domain and prohibits
cross-domain substitution.

It does not reproduce administrative authority or execution governance. It
governs the additional determination of which SoD constraints must be
satisfied before an otherwise governed Administrative Operation may progress.

The genuinely new normative content is the authoritative applicability domain,
positive requirement-set model, explicit empty-set semantics, contextual
binding, applicability validity, conflict, and fail-closed resolution.

## 88. Cross-Governance Consistency

This artifact preserves predecessor governance and MUST NOT:

- redefine Principal, Business Entity, Membership, Entitlement, Resource,
  Principal Mapping, or their authority sources;
- weaken administrative authority, execution, persistence, self-grant,
  privilege-escalation, delegation, bootstrap/root, lifecycle, revocation,
  Business Entity isolation, deterministic behavior, or fail-closed
  requirements;
- change Resource x Action Applicability or Resource Classification;
- make SoD applicability or satisfaction an authorization decision;
- expand Assessment Service, EIP, Website, Portal, Cognito, IAM, runtime, or AI
  authority;
- select persistence, runtime, service contract, workflow, policy model, role
  model, participant count, human participation, or security implementation;
  or
- authorize implementation.

## 89. Acceptance Criteria

This artifact is acceptable only if it:

- governs SoD applicability separately from SoD semantics;
- defines a positive, deterministic, authority-backed requirement-set model;
- requires an affirmative authoritative basis for NO ADDITIONAL SOD
  REQUIREMENT;
- treats missing, conflicting, stale, revoked, superseded, or ambiguous
  applicability as INDETERMINATE and fails closed;
- binds determinations to the exact operation, target, authority domain, scope,
  lifecycle, Business Entity where applicable, authority impact, and
  governance/version context;
- preserves every predecessor authority and repository boundary;
- avoids fabricated operation-specific rules and universal SoD requirements;
- preserves provenance, auditability, privacy, idempotence, replay,
  concurrency, and side-effect safety;
- remains technology-neutral; and
- leaves implementation unauthorized.

## 90. Architecture Decision

Administrative Separation of Duties Applicability Governance v1 is approved
conceptually when accepted by independent architecture review and controlled
closeout.

For a bounded Administrative Operation, the applicable SoD Requirement Set is
the deterministic result of current, authoritative, provenance-backed
Applicability Facts bound to the exact operation, target, authority domain,
scope, lifecycle, Business Entity where applicable, authority impact, and
governance/version context. An empty set is valid only when affirmatively
established. Missing, conflicting, stale, revoked, superseded, mismatched, or
ambiguous applicability produces INDETERMINATE and MUST fail closed.

Approval of this artifact would not establish concrete operation-specific SoD
rules, participant counts, human-participation policy, administration,
persistence, runtime, service contract, workflow, policy model, security
implementation, or implementation authorization.
