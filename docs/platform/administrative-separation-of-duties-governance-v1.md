# Administrative Separation of Duties Governance v1

Version: v1

## 1. Purpose

This governance artifact defines enterprise-level semantic requirements for
Administrative Separation of Duties (SoD).

It governs when applicable administrative governance requires independent
participation among authority-relevant duties and how that independence MUST
be established, preserved, and evaluated.

This artifact does not impose SoD on every administrative operation, implement
an approval process, select technology, or authorize implementation.

## 2. Governance Status

Administrative SoD semantics are GOVERNED CONCEPTUALLY by this artifact.

Concrete operation-specific applicability, SoD administration authority,
participant-count policy, role topology, persistence, runtime ownership,
service contracts, workflow technology, Security / IAM enforcement, and
implementation remain DOWNSTREAM, UNRESOLVED, NOT SELECTED, or UNAUTHORIZED as
classified here.

## 3. Scope

This artifact governs:

- conceptual administrative duty taxonomy;
- conditional SoD applicability;
- authoritative participant distinctness and authority independence;
- delegation-chain independence;
- request / approval, approval / execution, and execution / verification
  separation where applicable governance requires them;
- participant and approval validity, binding, revocation, staleness, conflict,
  ordering, replay, duplication, and concurrency semantics;
- deterministic SoD determination and result semantics;
- fail-closed behavior, provenance, auditability, privacy, and side-effect
  safety; and
- non-authority and non-selection boundaries necessary to keep SoD bounded.

## 4. Non-Scope

This artifact does not define or select:

- a universal maker/checker, dual-control, four-eyes, human-approval, or quorum
  requirement;
- an operation-specific SoD matrix, risk score, or product approval rule;
- a concrete administrator, job title, role, participant count, staffing model,
  or organization topology;
- the authority source, lifecycle, or administration semantics of a governed
  business object;
- an API, endpoint, schema, SDK, service contract, workflow, ticket, runtime,
  database, queue, event bus, or cloud service;
- a policy model, IAM implementation, Cognito implementation, identity-provider
  configuration, or security architecture;
- SoD-rule administration, emergency or break-glass authority, or an override
  process; or
- implementation, deployment, or production readiness.

## 5. Predecessor Governance

This artifact depends on and preserves:

- Principal Mapping Administrative Execution Governance v1;
- Principal Mapping Administration Authority Governance v1;
- Principal Mapping Persistence Governance v1;
- Principal Mapping Authority Source Governance v1;
- Stable Principal Mapping Authority Governance v1;
- Business Entity Administration Authority Governance v1;
- Business Entity Authority Source Governance v1;
- Administrative Bootstrap / Root Authority Governance v1;
- Authority Administration / Revocation Governance v1;
- Client / Organization Identity Authority Governance v1;
- Membership Authority Source Governance v1;
- Entitlement Semantics Governance v1;
- Entitlement Authority Source Governance v1;
- Deterministic Authorization Decision Semantics v1;
- Resource Identity Authority Source Governance v1;
- Resource Provisioning / Classification Binding Governance v1;
- Resource Classification Authority Governance v1;
- Resource Classification Authority Source / Runtime Ownership Governance v1;
- Resource Action Applicability Governance v1;
- Portal Governed Delivery Authorization Model v1;
- EIP Governed Retrieval Boundary v1; and
- Runtime Owner Assignment Governance v1.

Where predecessor governance is more restrictive, the more restrictive
boundary prevails.

## 6. Inherited Semantics

This artifact inherits the following conclusions:

- authoritative Principal identity is governed independently from accounts,
  sessions, claims, and technical roles;
- administrative authority must derive from a legitimate governed authority
  basis;
- self-grant, circular authority, privilege escalation, and delegation
  expansion are prohibited;
- a PERMITTED administrative operation is not an executed operation;
- execution capability, persistence, audit evidence, and technical control do
  not manufacture business authority;
- revocation and current lifecycle validity take precedence over stale
  historical evidence;
- Business Entity isolation and producer / consumer boundaries remain intact;
  and
- unresolved authority must fail closed.

## 7. Terminology

For this artifact:

- Administrative Operation means a bounded authority-relevant operation
  evaluated under applicable administrative governance.
- Duty means a conceptual responsibility performed in relation to an
  Administrative Operation.
- Participant means an authoritative Principal or a separately governed
  execution actor associated with a Duty; a technical account is not itself a
  Participant identity.
- Independent Participant means a Participant satisfying the distinctness and
  authority-independence requirements applicable to the operation.
- SoD Requirement means an applicable governed constraint requiring specified
  Duties to be performed by appropriately distinct or independent
  Participants.
- SoD Determination means the deterministic result of evaluating applicable
  SoD requirements against authoritative participant and operation facts.
- Approval means an authoritative decision for the exact operation context; it
  is not a user-interface action or stored label.

## 8. Central SoD Question

The central question is:

When applicable governance requires independent participation among
authority-relevant administrative duties, what facts must establish that the
required duties were performed by valid, sufficiently distinct, and
appropriately independent Participants for the same operation context?

This question is separate from who has administrative authority, whether an
operation is otherwise PERMITTED, whether execution occurred, where evidence
is stored, and whether Resource access is allowed.

## 9. Core Domain Separations

The following separations are mandatory:

```text
SEPARATION OF DUTIES != ADMINISTRATIVE AUTHORITY
SEPARATION OF DUTIES != AUTHENTICATION
SEPARATION OF DUTIES != AUTHORIZATION
SEPARATION OF DUTIES != EXECUTION
SEPARATION OF DUTIES != PERSISTENCE
SEPARATION OF DUTIES != AUDITABILITY
SEPARATION OF DUTIES != SELF-GRANT PROHIBITION
SEPARATION OF DUTIES != PRIVILEGE-ESCALATION PROTECTION
SEPARATION OF DUTIES != DELEGATION GOVERNANCE
```

SoD is an additional governed constraint only where applicable governance
requires independent participation.

## 10. Positive SoD Model

An applicable SoD Requirement is SATISFIED only when deterministic validation
establishes all required facts for the same Administrative Operation:

- the applicable SoD Requirement;
- each required Duty;
- authoritative identity of each relevant Participant;
- valid authority or governed execution capacity for each Participant's Duty;
- required participant distinctness;
- required authority independence and delegation-chain independence;
- exact target, operation, scope, lifecycle, Business Entity where applicable,
  and governance/version bindings;
- current validity of materially relied-upon participation; and
- absence of unresolved conflict, ambiguity, invalid ordering, or insufficient
  provenance.

Missing or invalid required facts MUST NOT produce an affirmative result.

## 11. Universal Dual-Control Rejection

This artifact explicitly rejects the following universal rules:

```text
ALL ADMINISTRATIVE OPERATIONS REQUIRE TWO HUMAN APPROVERS
ALL ADMINISTRATIVE OPERATIONS REQUIRE MAKER/CHECKER
```

Universal dual control is not established. Applying SoD without a governed
applicability basis is prohibited.

## 12. Conditional Applicability

An Administrative Operation may require separation, permit combined Duties,
require stronger authority independence, or have no SoD Requirement.

Applicable governance may consider operation type, authority impact, target,
scope, lifecycle transition, privilege impact, Business Entity context,
delegation context, revocation or restoration sensitivity, bootstrap or root
sensitivity, and governance/version context.

This artifact defines no score, matrix, threshold, or product-specific rule.

## 13. Applicability Authority

SoD applicability MUST derive from applicable governance and MUST NOT be chosen
unilaterally by a Participant for its own operation.

The ability to request, approve, execute, verify, persist, or observe an
operation does not confer authority to decide that SoD is unnecessary.

If applicability cannot be determined where an affirmative determination is
required, the operation MUST fail closed.

## 14. Administrative Duty Taxonomy

The conceptual Duty taxonomy includes:

- REQUEST;
- PROPOSE;
- EVALUATE;
- APPROVE / PERMIT;
- EXECUTE;
- VERIFY;
- REVIEW;
- REVOKE;
- RESTORE; and
- AUDIT.

An operation need not contain every Duty. Applicable governance determines
which Duties are material and which separations apply.

## 15. Request Duty

REQUEST expresses a bounded Administrative Operation for evaluation.

A request MUST identify its target, operation, scope, and other material
context sufficiently for governed evaluation. Requesting does not establish
approval, administrative authority, SoD satisfaction, or execution.

## 16. Propose and Evaluate Duties

PROPOSE may formulate a candidate Administrative Operation. EVALUATE applies
governed authority and validity requirements to that candidate.

Neither Duty establishes APPROVE / PERMIT by implication. Where applicable
governance separates proposing or evaluation from approval, the required
participant relationship MUST be deterministically established.

## 17. Approve / Permit Duty

APPROVE / PERMIT means an authoritative administrative decision for the exact
bound operation context.

Approval MUST derive from valid administrative authority. A click, label,
message, record, technical permission, or organizational title is not an
authoritative approval merely because it exists.

## 18. Execute Duty

EXECUTE applies an independently eligible Administrative Operation under the
requirements of applicable execution governance.

Execution does not approve the operation, and approval does not prove
execution. A technical Execution Actor does not become Administrative
Authority by performing EXECUTE.

## 19. Verify and Review Duties

VERIFY establishes whether the intended governed result occurred coherently.
REVIEW examines an operation, decision, evidence, or outcome under an
applicable review purpose.

Deterministic technical verification is not necessarily independent
authoritative participant verification. Applicable governance MUST state when
independent participation is required.

## 20. Revoke, Restore, and Audit Duties

REVOKE and RESTORE are authority-relevant administrative Duties subject to
their own current authority, lifecycle, scope, and applicability requirements.

AUDIT examines attributable evidence but does not create authority, approval,
SoD satisfaction, or execution. This taxonomy does not imply that one
Participant may perform all three Duties.

## 21. Administrative Duty / Role Separation

```text
DUTY != BUSINESS ROLE
DUTY != JOB TITLE
DUTY != PRINCIPAL
DUTY != TECHNICAL ACCOUNT
```

This artifact defines conceptual Duties only. It does not define staffing,
organizational roles, or concrete administrator topology.

## 22. Participant Distinctness

Where applicable governance requires different Participants, distinctness
MUST be established from authoritative governed Principal identity or other
separately governed actor semantics appropriate to the Duty.

Different labels, accounts, credentials, roles, sessions, devices, or records
MUST NOT substitute for authoritative participant distinctness.

## 23. Technical Account Distinctness

The following reasoning is invalid:

```text
different username -> different authoritative Participant
different Cognito account -> different authoritative Participant
different IAM role -> different authoritative Participant
different browser session -> different authoritative Participant
```

Two technical accounts controlled by the same Principal do not satisfy a
distinct-Participant requirement merely because the accounts differ.

## 24. Temporal Distinctness

```text
SAME PRINCIPAL AT DIFFERENT TIMES != INDEPENDENT PARTICIPANTS
```

Time separation alone does not manufacture participant distinctness or
authority independence. A Principal requesting on one date and approving on
another remains the same Principal for SoD evaluation.

## 25. Authority Independence

Participant distinctness does not necessarily establish authority
independence.

Where independent authority is required, nominally distinct Principals MUST
NOT satisfy SoD if the relevant authority relationship is circular,
self-created, or controlled in a way that defeats the required independence.

Authority independence MUST be established from governed authority provenance,
not inferred from participant count.

## 26. Delegation-Chain Independence

A delegated Participant MUST possess valid, lifecycle-current authority within
delegated target, operation, scope, time, and governance/version bounds.

Delegation MUST NOT manufacture nominal separation. Where independence is
required, a delegation chain that is circular or wholly controlled by another
Participant in a manner defeating independence MUST NOT satisfy SoD.

```text
DELEGATION != INDEPENDENCE
```

## 27. Request / Approval Separation

Where applicable governance requires request / approval separation:

```text
REQUESTOR != APPROVER
```

The distinction MUST be established using governed participant identity and
authority facts. This separation is not universal, and a request does not
create approval authority.

## 28. Approval / Execution Separation

Where applicable governance requires approval / execution separation:

```text
APPROVER != EXECUTION ACTOR
```

Technical execution capability does not establish approval authority. This
artifact does not universally require different actors and does not select an
Execution Actor.

## 29. Execution / Verification Separation

Where applicable governance requires independent authoritative verification:

```text
EXECUTION ACTOR != INDEPENDENT VERIFIER
```

The requirement MUST be satisfied by the authoritative actor semantics
applicable to each Duty. Deterministic technical verification may remain part
of execution governance without counting as an independent Participant.

## 30. Participant Authority Validity

Each authoritative Participant MUST possess valid authority for the Duty it
performs when that participation is materially relied upon.

Authority revocation, expiration, supersession, delegation revocation, scope
change, lifecycle change, Business Entity change, or governance/version change
MUST invalidate participation when the applicable authority no longer
supports the Duty.

A non-authoritative technical Execution Actor remains governed by execution
eligibility and MUST NOT be reclassified as Administrative Authority.

## 31. Approval Validity

An approval MUST be bound to the exact:

- authoritative Participant and authority basis;
- target;
- operation;
- scope;
- lifecycle context;
- Business Entity context where applicable; and
- governance/version context.

Approval for one context MUST NOT be reused for another.

## 32. Stale Approval

Historical approval alone MUST NOT authorize materially changed execution.

If authority, target, operation, scope, lifecycle, Business Entity,
delegation, SoD Requirement, or applicable governance materially changes after
approval, current approval validity and SoD satisfaction MUST be
deterministically re-established. Otherwise the result MUST fail closed.

## 33. Approval Revocation

Approval or other SoD participation may become invalid through applicable
revocation, expiration, supersession, lifecycle change, authority change, or
withdrawal semantics.

Persisted or historical presence MUST NOT override current invalidity. This
artifact selects no approval storage or revocation mechanism.

## 34. Conflicting Participation

Incompatible authoritative outcomes such as APPROVE and DENY, or APPROVE and
validly withdrawn approval, MUST NOT silently produce SoD satisfaction.

This artifact selects no voting, majority, quorum, tie-breaker, or consensus
rule. If applicable governance cannot deterministically resolve the conflict,
the SoD result MUST be INDETERMINATE or NOT SATISFIED and never affirmative.

## 35. Ordering

Where applicable governance requires an order among Duties, that order is
authority-relevant.

Execution before a required approval MUST NOT become valid merely because an
approval is added afterward. Invalid or indeterminate ordering MUST NOT satisfy
SoD. No sequencing or workflow technology is selected.

## 36. Scope Binding

All relied-upon participation MUST concern the same governed scope.

Approval for scope S1 MUST NOT satisfy an operation in scope S2. An unresolved
or incompatible scope requires non-affirmative SoD treatment.

## 37. Target Binding

All relied-upon participation MUST concern the exact governed target.

Approval for target T1 MUST NOT satisfy an operation against T2. Target aliases
or presentation values MUST NOT bypass authoritative target identity.

## 38. Operation Binding

All relied-upon participation MUST concern the exact governed operation.

```text
DEACTIVATE != REVOKE
RESTORE != ACTIVATE necessarily
REMAP != REPLACE necessarily
```

Approval for operation O1 MUST NOT satisfy O2.

## 39. Business Entity Binding

Where Business Entity context applies, all relied-upon participation MUST be
valid for the same authoritative Business Entity.

Approval concerning B1 MUST NOT satisfy an operation concerning B2.

## 40. Lifecycle Binding

SoD participation MUST be valid for the lifecycle state and transition to
which it is bound.

Historical participation under a materially different lifecycle state MUST
NOT automatically remain sufficient for activation, deactivation, revocation,
supersession, replacement, restoration, or another transition.

## 41. Governance / Version Binding

SoD Requirements, participation, and determinations MUST be interpreted under
the applicable governance/version context.

Historical participation MUST NOT silently inherit later semantics or remain
valid under an incompatible current context. No version storage or deployment
mechanism is selected.

## 42. Revocation / Restoration Boundary

Authority to revoke does not imply authority to restore, and authority to
restore does not imply authority to revoke.

This artifact does not require the revoking and restoring Participants always
to differ. Applicable governance MUST determine whether separation or stronger
independence is required for a specific revocation or restoration context.

## 43. Restoration Safety

SoD MUST NOT resurrect authority that is revoked, expired, superseded,
invalid, or outside scope.

Restoration requires separately valid restoration authority, lifecycle
eligibility, applicable SoD satisfaction, provenance, and all other governing
requirements. Historical SoD satisfaction is insufficient by itself.

## 44. Self-Grant Boundary

This artifact preserves and does not replace predecessor self-grant
prohibitions.

A subject MUST NOT establish, expand, restore, or manufacture its own required
authority through an SoD process. Dividing self-grant into multiple steps,
accounts, sessions, or technical actions does not make it valid.

```text
TWO-STEP SELF-GRANT = SELF-GRANT
```

## 45. Privilege-Escalation Boundary

SoD participation MUST NOT expand administrative authority, scope, Business
Entity reach, delegation, Membership, Entitlement, Resource authority, or
authorization unless that effect is separately governed and authorized.

SoD satisfaction is not a privilege-escalation mechanism.

## 46. Administrator-of-Administrator Boundary

An operation changing another administrator's, delegated administrator's, or
authority-bearing Principal's authority remains subject to current authority,
scope, lifecycle, delegation, SoD applicability, and provenance requirements.

This artifact defines no administrator role and does not redefine bootstrap or
Root Administrative Authority.

## 47. Cross-Authority-Domain Boundary

Participation in one administrative authority domain MUST NOT establish
authority in another.

Business Entity, Principal Mapping, Membership, Entitlement, Resource, and
authorization administration remain separate authority domains. This artifact
creates no cross-domain role or inheritance.

## 48. Business Entity Isolation

SoD MUST preserve Business Entity isolation.

Participation concerning B1 MUST NOT establish authority concerning B2. Each
authoritative Participant MUST possess the authority applicable to its Duty in
the relevant Business Entity context.

## 49. Principal Boundary

SoD consumes authoritative Principal identity where human or business
participant identity is required. It does not define or establish Principal
identity.

```text
SOD PARTICIPANT != PRINCIPAL IDENTITY AUTHORITY
```

## 50. Membership Boundary

```text
SOD PARTICIPATION != MEMBERSHIP
```

Requesting, approving, executing, verifying, reviewing, revoking, restoring,
or auditing MUST NOT establish or modify Membership.

## 51. Entitlement Boundary

```text
SOD PARTICIPATION != ENTITLEMENT
```

SoD participation MUST NOT independently grant VIEW, DOWNLOAD, SUBMIT,
EXPLAIN, or any other Resource x Action authority.

## 52. Authorization Boundary

```text
SOD SATISFIED != RESOURCE AUTHORIZATION ALLOW
```

SoD may constrain an administrative transition. It does not replace
deterministic Resource authorization and MUST NOT itself produce ALLOW.

## 53. Administrative Authority Boundary

```text
SOD SATISFIED != ADMINISTRATIVE AUTHORITY
```

Each authoritative Participant MUST independently possess valid authority for
the Duty performed. Multiple unauthorized Participants do not create authority
collectively. SoD evidence cannot become its own authority basis.

## 54. Execution Boundary

```text
SOD SATISFIED != EXECUTION COMPLETED
```

SoD satisfaction may be one prerequisite for an Administrative Operation. It
does not prove that execution was eligible, attempted, completed, coherent, or
persisted.

## 55. Persistence Boundary

```text
SOD != PERSISTENCE
PERSISTED APPROVAL != VALID APPROVAL necessarily
PERSISTED PARTICIPANT RECORD != AUTHORITATIVE PARTICIPANT IDENTITY necessarily
PERSISTENCE WRITE != AUTHORITATIVE APPROVAL
```

Persistence may represent governed SoD evidence but MUST NOT manufacture
approval, participant identity, authority independence, or SoD satisfaction.

## 56. AI Non-Authority

```text
AI != AUTHORITATIVE SOD PARTICIPANT
```

AI MAY assist with explanation, summarization, routing, presentation, or
separately permitted analysis. AI MUST NOT independently establish authority,
count as an authoritative approver, satisfy participant independence, infer
missing approval, resolve ambiguity affirmatively, override revocation or
failed SoD, or manufacture provenance.

## 57. Cognito Non-Authority

```text
COGNITO GROUP != ADMINISTRATIVE AUTHORITY
COGNITO ATTRIBUTE != SOD AUTHORITY
COGNITO ADMINISTRATOR != BUSINESS ADMINISTRATIVE AUTHORITY
```

Cognito may support authentication or technical identity. Cognito state MUST
NOT independently establish authoritative participation, approval, or SoD
satisfaction.

## 58. IAM Non-Authority

```text
IAM PERMISSION != BUSINESS ADMINISTRATIVE AUTHORITY
IAM ROLE != SOD PARTICIPANT AUTHORITY
```

Technical permission to invoke, approve, execute, persist, or observe an
operation MUST NOT satisfy business SoD.

## 59. Website / Browser Non-Authority

Website and browser remain presentation and request consumers.

Browser state, request content, URLs, hidden fields, cookies, local storage,
displayed approvals, selected participants, and client-side workflow state
MUST NOT authoritatively establish approval, participant identity,
independence, authority, or SoD satisfaction.

## 60. Assessment Service Boundary

The Assessment Service remains the certified deterministic producer of
assessment business truth within its governed domain.

This artifact does not change assessment methodology, findings, risk,
contracts, runtime, or ownership. The Assessment Service does not become an
administrative, approval, or SoD authority.

## 61. EIP Boundary

EIP remains a governed consumer and derivation platform within its approved
domain.

EIP MUST NOT become an administrative authority, SoD authority, approval
engine, Principal authority source, or authorization authority by implication.

## 62. Runtime Ownership Non-Selection

This artifact does not select a runtime owner.

```text
RUNTIME OWNER != ADMINISTRATIVE AUTHORITY
RUNTIME OWNER != SOD AUTHORITY
```

Runtime ownership remains DOWNSTREAM / NOT SELECTED.

## 63. Service Contract Non-Selection

This artifact does not define or select an API, endpoint, request schema,
approval endpoint, workflow endpoint, response schema, SDK, interface, or
service contract.

Trusted Authorization Service Contract remains separately governed and
DOWNSTREAM for implementation.

## 64. Persistence Technology Non-Selection

This artifact does not select DynamoDB, RDS, Aurora, PostgreSQL, MySQL, S3,
Redis, a ledger, event store, filesystem, directory, graph database, document
database, schema, table, collection, key, or index.

SoD persistence remains DOWNSTREAM / NOT SELECTED.

## 65. Workflow Technology Non-Selection

This artifact does not select Step Functions, EventBridge, SQS, SNS, Kafka, a
workflow engine, ticket system, approval product, queue, event bus, or
orchestration technology.

Semantic ordering and validity requirements do not imply a workflow design.

## 66. Policy Model Non-Selection

This artifact does not select RBAC, ABAC, ACL, OPA, Cedar, IAM-role
authorization, Cognito-group authorization, or another policy engine.

SoD semantics remain independent of policy representation.

## 67. Role Model Non-Selection

This artifact does not define concrete roles such as Maker, Checker, Approver
Role, Reviewer Role, Security Administrator, or Super Administrator.

Conceptual Duties MUST NOT be interpreted as a selected organizational role
model.

## 68. Participant Count Non-Selection

This artifact does not establish exactly two Participants or a universal
minimum number of Participants.

Participant-count requirements, if any, MUST derive from applicable
governance. A count alone does not establish authority or independence.

## 69. Human Approval Non-Selection

This artifact does not require every Administrative Operation to have human
approval.

Where future applicable governance requires authoritative human participation,
that participation MUST satisfy the identity, authority, independence,
validity, binding, provenance, and fail-closed semantics defined here.

## 70. Deterministic SoD Determination

SoD determination MUST be deterministic.

```text
same authoritative participant facts
+ same Administrative Operation
+ same applicable SoD Requirements
+ same governance/version context
-> same SoD Determination
```

AI judgment, probability, heuristic selection, best guess, and subjective
override are prohibited.

## 71. SoD Result Semantics

SoD evaluation outcomes are:

- SATISFIED: every applicable SoD Requirement is affirmatively established for
  the exact current operation context;
- NOT SATISFIED: at least one applicable SoD Requirement is affirmatively not
  met;
- NOT APPLICABLE: applicable governance affirmatively establishes that no SoD
  Requirement applies to the operation context; and
- INDETERMINATE: available authoritative facts cannot establish applicability
  or satisfaction.

```text
SOD SATISFIED != ADMINISTRATIVE OPERATION PERMITTED
SOD SATISFIED != EXECUTED
```

INDETERMINATE MUST NOT be interpreted affirmatively. NOT APPLICABLE MUST NOT be
used as a default for missing applicability facts.

## 72. Fail-Closed Model

Required SoD MUST fail closed when affirmative satisfaction cannot be
deterministically established, including for:

- unresolved participant identity or authority;
- insufficient participant distinctness;
- unresolved authority or delegation-chain independence;
- missing required Duty or approval;
- revoked, expired, superseded, withdrawn, or stale participation;
- target, operation, scope, lifecycle, Business Entity, or governance/version
  mismatch;
- conflicting participation or invalid ordering;
- insufficient provenance; or
- ambiguous SoD applicability.

Fail-closed SoD constrains administrative progression and does not itself make
a Resource authorization decision.

## 73. Provenance

Material SoD determinations MUST have sufficient conceptual provenance to
explain:

- the applicable SoD Requirement;
- authoritative Participant identity and Duty;
- participant authority basis;
- target, operation, scope, lifecycle, and Business Entity context where
  applicable;
- delegation provenance where relevant;
- ordering and current validity of participation;
- governance/version context; and
- the SoD Determination.

This artifact selects no provenance storage or format.

## 74. Auditability

Material SoD determinations MUST be deterministically auditable, including
SATISFIED, NOT SATISFIED, NOT APPLICABLE, and INDETERMINATE outcomes.

```text
AUDIT RECORD != AUTHORITY
AUDIT RECORD != APPROVAL
AUDIT RECORD != SOD SATISFACTION by itself
```

Auditability does not select observability technology.

## 75. Privacy / Minimum Disclosure

SoD evaluation, provenance, and auditability MUST use only information
necessary for the governed purpose.

This artifact does not require unnecessary exposure of email, username, raw
identity-provider claims, credentials, tokens, unrelated Business Entity data,
unrelated Membership, unrelated Entitlement, unrelated Resource data, or
producer business truth.

Governed identifiers and bounded authority references SHOULD be used where
sufficient.

## 76. Idempotence

Repeated evaluation or processing of the same authoritative participation
under unchanged context MUST NOT create additional authority, multiply
approval weight, manufacture participant count, manufacture independence, or
expand scope.

This is semantic idempotence and selects no idempotency technology.

## 77. Replay

Historical SoD participation MUST NOT automatically satisfy a later materially
different Administrative Operation.

Old participation replayed after authority revocation, approval revocation,
target change, operation change, scope change, lifecycle change, Business
Entity change, delegation change, or governance change MUST fail closed unless
current validity is affirmatively established.

## 78. Duplicate Participation

Repeated records, messages, observations, or processing associated with the
same authoritative Participant and Duty MUST NOT count as multiple independent
Participants or multiple approval weight.

Duplication cannot manufacture separation.

## 79. Concurrency

Concurrent participation MUST preserve deterministic SoD interpretation.

If concurrent approval, denial, withdrawal, revocation, or other
authority-relevant facts make SoD state ambiguous, the result MUST fail closed.
This artifact selects no transaction, lock, quorum, consensus, or workflow
technology.

## 80. Side-Effect Safety

SoD applicability and evaluation MUST NOT itself:

- create, expand, revoke, or restore authority;
- create Principal, Business Entity, Membership, or Entitlement state;
- authorize Resource access;
- execute an Administrative Operation;
- modify business truth or derived truth;
- mutate persistence; or
- expand delegation.

## 81. Authority Source Non-Replacement

SoD evidence MUST NOT replace authoritative evidence for Principal, Business
Entity, Membership, Entitlement, Resource, administrative authority,
delegation, Principal Mapping, or authorization.

SoD constrains the relationship among Duties; it does not become the authority
source for the governed object or operation.

## 82. Administrative Execution Integration Boundary

If an Administrative Operation requires SoD, administrative execution MUST
NOT proceed affirmatively unless the applicable SoD Requirement is currently
SATISFIED.

```text
SOD SATISFIED != EXECUTION AUTHORIZED BY ITSELF
```

All administrative authority, decision-binding, execution-time validity,
target-state, provenance, coherence, and other execution prerequisites remain
independently required.

## 83. Bootstrap / Root Boundary

Administrative Bootstrap / Root Authority Governance v1 remains authoritative.

SoD MUST NOT establish, redefine, or manufacture Root Administrative Authority
through multiple Participants, nor replace the Terminating Authority Basis or
its evidence. Bootstrap-specific SoD applicability remains DOWNSTREAM unless
separately governed.

## 84. No Authority by Consensus

```text
MULTIPLE PARTICIPANTS != AUTHORITY
```

Any number of unauthorized Participants MUST NOT collectively create approval,
administrative authority, or SoD satisfaction. Participant count cannot
substitute for valid authority.

## 85. No Authority by Technical Control

Technical control over runtime, database, identity provider, IAM, deployment,
infrastructure, browser, repository, or workflow MUST NOT establish SoD
authority, approval, participant identity, or participant independence.

Technical capability remains subordinate to governed business authority.

## 86. No Authority by Organizational Label

Labels such as administrator, manager, security, reviewer, approver, or owner
MUST NOT be treated as authoritative merely because the label exists.

Authority MUST derive from governed authority semantics and remain valid for
the exact Duty and context.

## 87. SoD Requirement Non-Self-Modification

A Participant in an Administrative Operation MUST NOT unilaterally weaken,
remove, or reinterpret the SoD Requirement governing that same operation.

Any administration of SoD Requirements requires separate, valid governance and
authority. This artifact does not define that administration mechanism.

## 88. Authority Independence Failure

Where applicable governance requires authority independence and independence
cannot be deterministically established, the SoD result MUST be NOT SATISFIED
or INDETERMINATE according to the known facts.

The result MUST never be SATISFIED by assumption, nominal Principal
distinctness, technical account separation, or administrative convenience.

## 89. SoD Bypass Prohibition

No Participant may bypass applicable SoD through an alternate account,
session, IAM role, delegated alias, browser manipulation, direct persistence
write, runtime invocation, AI recommendation, organizational label, or
administrative convenience.

Bypass evidence MUST NOT be normalized into valid participation.

## 90. Emergency / Break-Glass Boundary

This artifact defines no emergency, break-glass, exceptional override, or
post-hoc approval path.

Emergency or break-glass governance remains UNRESOLVED / DOWNSTREAM. Absence of
such governance MUST NOT be interpreted as an implicit SoD bypass.

## 91. SoD Administration Boundary

This artifact does not determine who creates, changes, revokes, suspends, or
administers SoD Requirements or operation-specific applicability.

SoD administration authority and its lifecycle, provenance, persistence, and
execution remain DOWNSTREAM / UNRESOLVED. No Participant may assume that
authority by operating under a SoD Requirement.

## 92. SoD Persistence Boundary

Persistence of approvals, participant evidence, SoD Requirements, or SoD
Determinations remains DOWNSTREAM / NOT SELECTED.

Any future persistence MUST preserve authority, identity, independence,
validity, binding, provenance, determinism, privacy, and fail-closed semantics
without becoming authority.

## 93. SoD Runtime Boundary

This artifact does not define an SoD runtime, evaluator placement, approval
engine, workflow owner, or execution owner.

SoD runtime and runtime ownership remain DOWNSTREAM / NOT SELECTED.

## 94. SoD Service Contract Boundary

This artifact does not define a contract for requests, approvals,
participation, SoD Requirements, determinations, evidence, or execution
integration.

SoD service-contract governance remains DOWNSTREAM / NOT SELECTED.

## 95. SoD Observability Boundary

SoD outcomes MUST be conceptually auditable and attributable, but observability
is not authority.

This artifact does not select CloudWatch, logs, an event store, SIEM, metrics,
tracing, alerting, or a monitoring product. Concrete Authorization Audit /
Observability remains DOWNSTREAM.

## 96. Security / IAM Boundary

This artifact does not select IAM roles, IAM policies, trust policies, resource
policies, KMS, WAF, security groups, network controls, encryption
configuration, Cognito configuration, or another security implementation.

Security / IAM Boundary and enforcement remain DOWNSTREAM / NOT SELECTED.

## 97. Technology Neutrality

This artifact is technology-neutral.

Named technologies appear only to establish non-authority, non-selection, or
architecture boundaries. No identity provider, database, workflow, runtime,
cloud service, policy engine, approval product, ticket system, API, schema, or
security product is recommended or selected.

## 98. Authority Status Model

Governance status under this artifact:

| Governance area | Status |
| --- | --- |
| Administrative SoD semantics | GOVERNED CONCEPTUALLY |
| Conditional applicability semantics | GOVERNED CONCEPTUALLY |
| Concrete applicability by operation | DOWNSTREAM / UNRESOLVED |
| Duty taxonomy | GOVERNED CONCEPTUALLY |
| Participant distinctness | GOVERNED CONCEPTUALLY |
| Authority independence | GOVERNED CONCEPTUALLY |
| Delegation-chain independence | GOVERNED CONCEPTUALLY |
| Request / approval separation | CONDITIONAL / GOVERNED CONCEPTUALLY |
| Approval / execution separation | CONDITIONAL / GOVERNED CONCEPTUALLY |
| Execution / verification separation | CONDITIONAL / GOVERNED CONCEPTUALLY |
| Participant authority lifecycle validity | GOVERNED CONCEPTUALLY |
| Approval validity and revocation | GOVERNED CONCEPTUALLY |
| Stale approval | GOVERNED CONCEPTUALLY |
| Conflicting participation | GOVERNED CONCEPTUALLY |
| Binding and ordering | GOVERNED CONCEPTUALLY |
| Deterministic SoD determination | GOVERNED |
| Fail-closed SoD behavior | GOVERNED |
| SoD result semantics | GOVERNED CONCEPTUALLY |
| Provenance and auditability | GOVERNED CONCEPTUALLY |
| Privacy / minimum disclosure | GOVERNED / PRESERVED |
| SoD administration authority | DOWNSTREAM / UNRESOLVED |
| SoD persistence | DOWNSTREAM / NOT SELECTED |
| SoD runtime ownership | DOWNSTREAM / NOT SELECTED |
| SoD service contract | DOWNSTREAM / NOT SELECTED |
| Policy model | DOWNSTREAM / NOT SELECTED |
| Concrete roles | DOWNSTREAM / NOT SELECTED |
| Participant-count policy | DOWNSTREAM / NOT SELECTED |
| Universal human approval | NOT SELECTED |
| Emergency / break-glass | DOWNSTREAM / UNRESOLVED |
| Security / IAM implementation | DOWNSTREAM / NOT SELECTED |
| Implementation | UNAUTHORIZED |

No downstream, unresolved, or not-selected concern is resolved by implication.

## 99. Resolved Here

This artifact resolves only conceptual governance for:

- the distinction between SoD and authority, authentication, authorization,
  execution, persistence, auditability, self-grant, privilege escalation, and
  delegation;
- conditional SoD applicability and the rejection of universal dual control;
- administrative Duty taxonomy without selecting roles;
- authoritative participant distinctness, temporal and technical-account
  non-distinctness, authority independence, and delegation-chain independence;
- conditional request / approval, approval / execution, and execution /
  verification separation;
- participant and approval authority validity, revocation, staleness, binding,
  conflict, and ordering;
- deterministic SoD determination, result semantics, and fail-closed behavior;
- provenance, auditability, privacy, idempotence, replay, duplication,
  concurrency, and side-effect safety; and
- the non-authority, non-selection, and integration boundaries defined here.

This artifact does not claim implementation readiness or completion.

## 100. Remaining Governance

The following remain unresolved or downstream unless separately governed:

- concrete SoD applicability by operation and authority impact;
- SoD administration authority and execution;
- SoD persistence and persistence administration;
- SoD runtime and runtime ownership;
- SoD service contract and execution integration contract;
- concrete role and organizational topology;
- participant-count requirements where applicable;
- emergency / break-glass governance;
- Business Entity persistence;
- Resource Provisioning Authority;
- Resource Identity Administration Authority;
- Resource Identity Persistence Authority;
- Classification / Binding Administration Authority;
- Classification / Binding Persistence Authority;
- Applicability Administration;
- Engagement Scope;
- Trusted Authorization Service Contract;
- Authorization Persistence;
- Authorization Audit / Observability;
- Security / IAM Boundary and enforcement; and
- explicit implementation authorization.

Completed predecessor governance remains authoritative and is not reopened by
this list.

## 101. Implementation Gate

ADMINISTRATIVE / AUTHORIZATION / EXECUTION / PERSISTENCE / SEPARATION-OF-DUTIES IMPLEMENTATION REMAINS UNAUTHORIZED

This artifact does not authorize:

- an SoD, administrative, authorization, execution, or persistence runtime;
- an API, endpoint, service contract, Lambda, container, database, queue,
  event bus, workflow, approval product, or ticket system;
- IAM, Cognito, identity-provider, network, encryption, or other security
  changes;
- Website changes;
- Assessment Service changes;
- EIP changes;
- policy-model implementation;
- deployment; or
- production readiness.

Implementation requires separate approved governance, ownership review,
implementation planning, and explicit authorization in the correct owning
repository.

## 102. Adversarial SoD Review

The following outcomes are mandatory:

- A. The same Principal uses two accounts to request and approve an operation
  requiring independence: SoD is NOT SATISFIED because account difference does
  not establish Participant distinctness.
- B. A and B are distinct Principals, but B's relevant authority derives
  entirely from A in a way defeating required independence: nominal
  distinctness is insufficient, and SoD is NOT SATISFIED or INDETERMINATE.
- C. One administrator requests and approves a sensitive non-self-grant
  operation where request / approval separation applies: SoD is NOT
  SATISFIED.
- D. The Approver also executes an operation where approval / execution
  separation applies: SoD is NOT SATISFIED.
- E. The Execution Actor verifies its own execution where independent
  verification is required: SoD is NOT SATISFIED.
- F. Approval authority is revoked before execution: historical approval MUST
  NOT automatically remain valid, and current SoD satisfaction MUST be
  re-established.
- G. Approval is valid for S1 and execution concerns S2: SoD is NOT SATISFIED
  for S2.
- H. Approval concerns B1 and the operation concerns B2: Business Entity
  binding and isolation fail, so SoD is NOT SATISFIED.
- I. Approval concerns DEACTIVATE and the operation is REVOKE: operation
  binding fails, so SoD is NOT SATISFIED.
- J. Approval occurred under an older materially incompatible governance
  context: historical approval MUST NOT automatically satisfy current SoD.
- K. One required Participant approves and another denies: no affirmative SoD
  result is permitted without applicable deterministic resolution.
- L. Required approval occurs after execution: post-hoc approval MUST NOT
  retroactively satisfy a pre-execution SoD Requirement.
- M. AI recommends approval: the recommendation is not authoritative approval
  and does not count toward SoD.
- N. IAM permits the technical approval action but business authority is
  absent: SoD is NOT SATISFIED.
- O. A Cognito group labels a subject as Approver without governed authority:
  SoD is NOT SATISFIED.
- P. Browser state claims two approvals occurred but authoritative evidence
  cannot establish them: the result MUST fail closed.
- Q. The same approval record is processed twice: it counts as one
  authoritative participation, not two independent Participants.
- R. An old approval is replayed after revocation: it MUST NOT restore SoD
  satisfaction automatically.
- S. Ten unauthorized Principals approve: multiple Participants do not create
  authority, so SoD is NOT SATISFIED.
- T. An administrator writes persistence to indicate approval without an
  authoritative approval: the write does not establish approval or SoD.
- U. A Runtime Owner executes an approval operation without business authority:
  runtime ownership does not create SoD authority.
- V. A Participant's delegation is revoked before its approval is materially
  relied upon: historical participation MUST NOT remain affirmatively valid.
- W. The same Principal requests on Monday and approves on Tuesday where
  independent request / approval participation is required: time separation
  does not satisfy independence.
- X. SoD applicability cannot be determined where affirmative determination is
  required: the result is INDETERMINATE and the operation MUST fail closed.

## 103. Circular Authority Test

SoD participation MUST NOT create the authority needed to satisfy SoD.

Multiple unauthorized Participants MUST NOT collectively create authority. A
Participant MUST NOT create another Participant's nominal authority solely to
satisfy required independence where that control defeats independence.
Technical control MUST NOT establish participant identity, authority, or
independence.

Every circular or self-legitimating chain MUST fail closed.

## 104. Duplication Review

This artifact does not restate self-grant or privilege-escalation governance;
it preserves those prohibitions while governing non-self-grant duty
independence.

It does not restate delegation governance; it adds the requirement that a
valid delegation may still be insufficient where its chain defeats required
Participant independence.

It does not restate administrative authority or execution governance; it
governs the additional conditional relationship among request, approval,
execution, verification, and other Duties.

It does not restate persistence or audit governance; it prevents stored or
observed SoD evidence from becoming authority.

The new normative content is limited to conditional duty separation,
Participant distinctness, authority independence, delegation-chain
independence, SoD-specific validity and conflict, and deterministic SoD
evaluation.

## 105. Cross-Governance Consistency

This artifact preserves predecessor governance and MUST NOT:

- redefine Principal, Business Entity, Membership, Entitlement, Resource,
  Principal Mapping, or their authority sources;
- weaken self-grant, privilege-escalation, delegation, bootstrap/root,
  revocation, lifecycle, Business Entity isolation, determinism, or fail-closed
  requirements;
- replace administrative authority or Principal Mapping execution semantics;
- make SoD satisfaction an authorization decision or evidence of execution;
- expand Assessment Service, EIP, Website, Cognito, IAM, runtime, or AI
  authority;
- select persistence, runtime, workflow, service contract, policy model, role
  model, participant count, or security implementation; or
- authorize implementation.

## 106. Acceptance Criteria

This artifact is acceptable only if it:

- governs SoD conditionally rather than universally;
- distinguishes Duties from roles, Principals, and technical accounts;
- requires authoritative Participant identity and valid Duty authority;
- distinguishes Participant distinctness from authority independence;
- prevents delegation from manufacturing independence;
- binds participation to exact target, operation, scope, lifecycle, Business
  Entity where applicable, and governance/version context;
- governs stale, revoked, conflicting, reordered, replayed, duplicate, and
  concurrent participation deterministically;
- fails closed whenever required SoD cannot be affirmatively established;
- preserves provenance, auditability, privacy, and side-effect safety;
- preserves every predecessor authority and repository boundary;
- remains technology-neutral; and
- leaves implementation unauthorized.

## 107. Architecture Decision

Administrative Separation of Duties Governance v1 is approved conceptually
when accepted by independent architecture review and controlled closeout.

Where applicable governance requires SoD, an Administrative Operation may
progress only when the exact required Duties are attributable to valid,
sufficiently distinct, and appropriately independent Participants under the
same current target, operation, scope, lifecycle, Business Entity where
applicable, and governance/version context; the SoD Determination is
deterministic and supported by sufficient provenance; and no unresolved
conflict, stale participation, invalid ordering, circular authority, or bypass
exists. Otherwise the operation MUST fail closed.

Approval of this artifact would not define operation-specific applicability,
select roles, participant counts, persistence, runtime, workflow, service
contract, policy model, security implementation, or authorize implementation
or deployment.
