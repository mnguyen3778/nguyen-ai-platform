# Administrative Separation of Duties Operation-Specific Requirement Set Governance v1

Version: v1

## 1. Purpose

This artifact governs authoritative operation-specific Administrative
Separation-of-Duties (SoD) Requirement Sets for bounded administrative
operations in Nguyen AI governance.

It closes the bounded policy-content question:

```text
For administrative operation O in governed context C, what authoritative
Administrative SoD Requirement Set R applies?
```

This artifact is governance only. It does not implement SoD, authorization,
administration, persistence, runtime resolution, service contracts, or
enforcement.

## 2. Governance Status

Operation-specific Administrative SoD Requirement Set semantics are GOVERNED
HERE only for the bounded domains and operations explicitly identified in this
artifact.

Domains and contexts not explicitly assigned an authoritative Requirement Set
remain UNRESOLVED and fail closed where a current authoritative Requirement
Set is required.

## 3. Scope

This artifact governs:

- the deterministic operation-specific SoD Requirement Set model;
- the conceptual binding key for operation-specific policy;
- the authoritative Requirement Set statuses used by this artifact;
- supported operation-specific policy for Business Entity administration;
- supported operation-specific policy for Principal Mapping administration;
- unresolved policy treatment for other administrative target domains;
- missing, empty, conflicting, stale, revoked, superseded, default,
  inheritance, override, and composition boundaries;
- provenance, auditability, determinism, fail-closed behavior, privacy, and
  side-effect safety; and
- non-selection and non-authority boundaries necessary to keep policy content
  separate from implementation.

## 4. Non-Scope

This artifact does not define, select, or authorize:

- SoD semantic primitives already governed by Administrative Separation of
  Duties Governance v1;
- SoD applicability semantics already governed by Administrative Separation
  of Duties Applicability Governance v1;
- SoD policy-authority semantics already governed by Administrative Separation
  of Duties Requirement Set Authority / Policy Basis Governance v1;
- policy administration, policy persistence, policy runtime, policy
  enforcement, or service contracts;
- participant-count policy, quorum, majority, voting, staffing model, or
  concrete organizational roles;
- mandatory human approval or universal human participation;
- risk tiers, sensitivity tiers, severity tiers, or criticality tiers;
- emergency, break-glass, waiver, override, exception, default, inheritance,
  or policy-composition rules;
- IAM, Cognito, Website, Portal, Assessment Service, EIP, AWS AI Knowledge
  Assistant, database, workflow, policy engine, API, endpoint, schema, or
  runtime changes; or
- implementation, deployment, or production readiness.

## 5. Predecessor Governance

This artifact depends on and preserves:

- Administrative Separation of Duties Governance v1;
- Administrative Separation of Duties Applicability Governance v1;
- Administrative Separation of Duties Requirement Set Authority / Policy Basis
  Governance v1;
- Administrative Bootstrap / Root Authority Governance v1;
- Authority Administration / Revocation Governance v1;
- Business Entity Administration Authority Governance v1;
- Business Entity Authority Source Governance v1;
- Principal Mapping Administration Authority Governance v1;
- Principal Mapping Administrative Execution Governance v1;
- Principal Mapping Authority Source Governance v1;
- Principal Mapping Persistence Governance v1;
- Stable Principal Mapping Authority Governance v1;
- Membership Authority Source Governance v1;
- Entitlement Semantics Governance v1;
- Entitlement Authority Source Governance v1;
- Deterministic Authorization Decision Semantics v1;
- Resource x Action Applicability Governance v1;
- Resource Identity Authority Source Governance v1;
- Resource Provisioning / Classification Binding Governance v1;
- Resource Classification Authority Governance v1; and
- Resource Classification Authority Source / Runtime Ownership Governance v1.

Where predecessor governance is more restrictive, the more restrictive
boundary prevails.

## 6. Sufficiency Basis

The preceding read-only sufficiency and dependency review concluded:

```text
B. PARTIAL - OPERATION-SPECIFIC REQUIREMENT SET GOVERNANCE IS REQUIRED AND MAY PROCEED NOW
```

It also concluded that SoD semantics, SoD applicability, policy authority,
administrative operation semantics, target-domain semantics, Business Entity
scope, lifecycle semantics, requirement vocabulary, deterministic resolution,
and conflict semantics are sufficient to define bounded operation-specific
Requirement Sets without additional prerequisites.

## 7. Layer Separation

The following separations are mandatory:

```text
SOD SEMANTICS != SOD APPLICABILITY
SOD APPLICABILITY != SOD REQUIREMENT-SET POLICY AUTHORITY
SOD REQUIREMENT-SET POLICY AUTHORITY != OPERATION-SPECIFIC REQUIREMENT-SET POLICY
OPERATION-SPECIFIC REQUIREMENT-SET POLICY != POLICY ADMINISTRATION
POLICY ADMINISTRATION != POLICY PERSISTENCE
POLICY PERSISTENCE != POLICY ENFORCEMENT
```

This artifact governs only the operation-specific policy-content layer.

## 8. Central Policy Model

For a bounded administrative operation, the conceptual deterministic model is:

```text
R = ResolveSoDRequirementSet(
    BusinessEntity,
    AdministrativeTargetDomain,
    AdministrativeOperation,
    ApplicableContext,
    GovernanceVersion,
    AuthoritativeSoDPolicy
)
```

R is exactly one of:

- an authoritative non-empty SoD Requirement Set;
- an affirmatively authoritative empty Requirement Set; or
- INDETERMINATE / FAIL-CLOSED.

This model defines governance semantics only. It does not define runtime
syntax, a resolver implementation, a service, or storage.

## 9. Policy Binding Key

Operation-specific Requirement Set policy MUST be bound by the minimum
conceptual dimensions necessary for deterministic use.

Potential binding dimensions include, where material:

- Business Entity;
- administrative target domain;
- administrative operation;
- lifecycle context;
- authority-impact context;
- applicable SoD context;
- governance/version; and
- authoritative policy identity.

A dimension MAY be omitted only when authoritative governance establishes that
the dimension is immaterial for that policy. Omitted dimensions MUST NOT be
filled by technical metadata, UI labels, runtime defaults, AI inference, or
operator preference.

## 10. Administrative Target Domains

Operation-specific SoD policy is bound to an administrative target domain.

At minimum, the following target domains are conceptually distinct:

- Business Entity;
- Principal Mapping;
- Membership;
- Entitlement;
- Resource Identity;
- Resource Classification / Binding; and
- Resource x Action Applicability.

```text
POLICY FOR D1 != POLICY FOR D2
```

Cross-domain reuse requires explicit authoritative governance.

## 11. Business Entity Binding

Where Business Entity context applies:

```text
POLICY FOR B1 != POLICY FOR B2
```

Policy for one Business Entity MUST NOT apply to another Business Entity
unless an authoritative policy basis explicitly establishes broader scope.

This artifact does not select persistence representation for Business Entity
binding.

## 12. Administrative Operation Binding

Different administrative operations MAY have different authoritative SoD
Requirement Sets.

This artifact consumes existing governed operation concepts including:

- ESTABLISH;
- ACTIVATE;
- MODIFY;
- REPLACE;
- SUPERSEDE;
- DEACTIVATE;
- REVOKE;
- RESTORE / REACTIVATE; and
- REMAP.

Operation names are governance concepts, not API methods. Policy for one
operation MUST NOT be reused for another operation without explicit
authoritative equivalence.

## 13. Requirement Vocabulary

This artifact uses only SoD requirement primitives governed by Administrative
Separation of Duties Governance v1.

The supported v1 policy-content vocabulary is:

- request / approval separation;
- participant distinctness for separated duties;
- authority independence for separated duties;
- delegation-chain independence where delegated authority is relied upon;
- operation, target, scope, lifecycle, Business Entity, and governance/version
  binding of SoD participation; and
- prohibition on self-approval, self-authorization, circular authority, and
  stale participation where those facts would defeat the selected separation.

This artifact does not create a new requirement primitive.

## 14. Participant Count Boundary

This artifact does not establish a universal participant count.

A selected request / approval separation requirement necessarily requires
distinct authoritative participants for those two duties, but that is the
minimum semantic separation required by the selected SoD primitive. It is not
a universal two-person, quorum, majority, voting, or staffing rule.

## 15. Human Participation Boundary

This artifact does not establish mandatory human approval or universal human
participation.

```text
SOD != MANDATORY HUMAN APPROVAL
```

Where this artifact selects request / approval separation, it selects
governed authoritative participant separation. It does not select a human-only
workflow or prohibit future governance from requiring human participation for
specific contexts.

## 16. Self-Authorization / Self-Approval

For any non-empty Requirement Set governed here, the same authoritative subject
MUST NOT satisfy incompatible request and approval duties for the same
operation/context.

This is not a universal workflow requirement. It applies only where this
artifact or future authoritative policy selects the relevant separation.

## 17. Authority-Domain Separation

Where authority independence is selected, distinct participant identity alone
is insufficient.

The approving or permitting duty MUST be supported by authority that is not
circularly created, self-granted, wholly controlled by the requestor for the
purpose being evaluated, or invalid under the applicable delegation chain.

This artifact does not create organizational role names.

## 18. Empty Requirement Set

An operation may have an authoritative empty Requirement Set only when an
affirmative authoritative policy establishes that result for the exact
operation/context.

```text
AUTHORITATIVE EMPTY REQUIREMENT SET != MISSING POLICY
```

This v1 artifact establishes no authoritative empty Requirement Set.

## 19. Missing Policy

If no authoritative operation-specific policy resolves for a context, the
result is INDETERMINATE / FAIL-CLOSED.

Missing policy MUST NOT be interpreted as:

- no SoD required;
- an empty Requirement Set;
- an exception;
- an authorization allowance; or
- execution permission.

## 20. Conflict Handling

If multiple apparently authoritative operation-specific policies conflict and
applicable governance cannot deterministically resolve the conflict, the result
MUST be INDETERMINATE / FAIL-CLOSED.

This artifact does not select newest-wins, last-write-wins, administrator
preference, runtime priority, source priority, majority vote, quorum, or AI
precedence.

## 21. Default Policy Boundary

This artifact establishes no implicit default SoD policy.

```text
NO IMPLICIT DEFAULT
```

Missing policy fails closed. A future default policy would require explicit
authoritative governance and must not be inferred from this artifact.

## 22. Inheritance Boundary

This artifact establishes no policy inheritance.

No policy automatically flows:

- from platform to Business Entity;
- from domain to operation;
- from generic operation to specific operation; or
- from one lifecycle state to another.

Exact authoritative binding is required, otherwise the result fails closed.

## 23. Override Boundary

This artifact establishes no override semantics.

No administrator override, Business Entity override, local override, runtime
override, emergency override, waiver, or exception is authorized.

## 24. Composition Boundary

This artifact establishes no composition of multiple policy fragments.

Unless applicable governance explicitly establishes deterministic composition,
policy resolution MUST produce one authoritative resolved policy/result or
fail closed.

## 25. Emergency / Break-Glass Boundary

This artifact establishes no emergency, break-glass, waiver, exception, or
bypass policy.

```text
NO EXCEPTION GOVERNANCE = NO AUTHORIZED EXCEPTION
```

Emergency language, operational urgency, or runtime availability MUST NOT
weaken an applicable Requirement Set.

## 26. Risk / Sensitivity Boundary

This artifact establishes no risk tier, sensitivity tier, severity tier, or
criticality tier.

Operation-specific Requirement Sets in this artifact are based on governed
administrative operation semantics, authority impact, target domain, and policy
authority, not risk scoring.

## 27. Resource Classification Boundary

```text
RESOURCE CLASSIFICATION != SOD REQUIREMENT SET
```

Resource Classification does not establish, modify, strengthen, weaken, waive,
or select an Administrative SoD Requirement Set unless future authoritative
governance explicitly makes a classification fact material for a bounded SoD
policy.

## 28. Membership Boundary

```text
MEMBERSHIP != SOD POLICY
```

Membership does not determine a Requirement Set merely because a Principal is
a member of a Business Entity.

## 29. Entitlement Boundary

```text
ENTITLEMENT != SOD POLICY
```

Authority to perform an operation does not determine the SoD control governing
the operation.

## 30. Authorization Boundary

The following separations are mandatory:

```text
AUTHORIZATION ALLOW != SOD SATISFIED
SOD REQUIREMENT SET != RESOURCE AUTHORIZATION
SOD SATISFIED != RESOURCE AUTHORIZATION
```

This artifact does not merge authorization decisions with SoD policy or SoD
evaluation.

## 31. Operation Authority Boundary

Authority over an operation is separate from authority over policy for that
operation:

```text
AUTHORITY TO PERFORM O != AUTHORITY TO DEFINE POLICY FOR O
AUTHORITY TO APPROVE O != AUTHORITY TO DEFINE POLICY FOR O
```

No actor gains policy-making authority merely by requesting, approving,
executing, verifying, observing, or being affected by an operation.

## 32. Policy Authority Boundary

Every operation-specific Requirement Set governed here remains subject to
Administrative Separation of Duties Requirement Set Authority / Policy Basis
Governance v1.

Concrete policy content MUST NOT establish its own authority, expand its own
scope, or repair its own missing provenance.

## 33. Policy Identity

Each authoritative operation-specific policy MUST have stable conceptual
identity sufficient to distinguish it from:

- other policies;
- historical versions;
- persistence records;
- file paths;
- commits;
- tags;
- runtime objects; and
- audit events.

This artifact selects no identifier format.

## 34. Policy Version

Operation-specific policy MUST be bound to applicable governance/version.

```text
POLICY VALID UNDER G1
does not automatically remain valid under
INCOMPATIBLE G2
```

Version binding does not select schema fields, file names, deployment
mechanisms, branches, tags, or APIs.

## 35. Policy Lifecycle

Only CURRENT authoritative policy may govern current resolution where current
policy is required.

Superseded, revoked, invalid, or historical policy MUST NOT remain current
because it persists, remains cached, appears in Git history, appears in audit
records, or is referenced by stale consumers.

## 36. Policy Provenance

Authoritative operation-specific policy MUST have sufficient provenance to
reconstruct:

- policy identity;
- authority basis;
- binding scope;
- Requirement Set content;
- governance/version;
- lifecycle status; and
- supporting evidence.

```text
PROVENANCE != AUTHORITY
```

## 37. Policy Auditability

Authoritative operation-specific policy resolution MUST be conceptually
auditable.

Audit evidence may help reconstruct what policy was relied upon, but an audit
record does not create policy authority, satisfy SoD, authorize an operation,
or establish Resource authorization.

## 38. Deterministic Resolution

Equivalent authoritative inputs under the same applicable governance/version
MUST yield equivalent Requirement Set results.

Runtime discretion, administrator preference, AI judgment, heuristic inference,
probabilistic confidence, technical convenience, or subjective risk perception
MUST NOT select the Requirement Set.

## 39. Fail-Closed Conditions

Requirement Set resolution MUST fail closed for:

- missing policy;
- missing authority basis;
- invalid policy identity;
- Business Entity mismatch;
- target-domain mismatch;
- operation mismatch;
- lifecycle mismatch;
- governance/version mismatch;
- revoked policy;
- superseded policy where current policy is required;
- conflicting authoritative policies;
- circular authority;
- indeterminate policy authority;
- unsupported requirement primitive;
- unauthorized policy inheritance;
- unauthorized override;
- unauthorized composition;
- stale or insufficient provenance; and
- unresolved applicability context.

Uncertainty MUST NOT become an empty Requirement Set.

## 40. Requirement Set Status

This artifact uses the following statuses:

- AUTHORITATIVE NON-EMPTY: current authoritative policy establishes at least
  one governed SoD requirement for the exact context.
- AUTHORITATIVE EMPTY: current authoritative policy affirmatively establishes
  no additional SoD requirement for the exact context.
- UNRESOLVED: no authoritative policy content is established here for that
  domain, operation, or context.
- INDETERMINATE / FAIL-CLOSED: authoritative resolution cannot produce exactly
  one valid result for the operation/context.

UNRESOLVED and INDETERMINATE / FAIL-CLOSED are never equivalent to
AUTHORITATIVE EMPTY.

## 41. V1 Requirement Set RS-A

Requirement Set RS-A is the v1 non-empty SoD Requirement Set used by this
artifact for supported authority-impacting Business Entity and Principal
Mapping administrative operations.

RS-A requires:

- request / approval separation;
- participant distinctness between the requestor or proposer and the
  approver or permitter;
- authority independence for the approval or permit duty;
- delegation-chain independence where delegated authority is materially relied
  upon; and
- exact target, operation, scope, lifecycle, Business Entity where applicable,
  and governance/version binding for the separated duties.

RS-A does not require approval / execution separation, execution /
verification separation, independent verification, a named role, a human-only
approval, quorum, majority, voting, or a specific participant count beyond the
distinct participants required by request / approval separation.

## 42. RS-A Rationale

RS-A is selected only for operations whose governed semantics materially create,
activate, alter, replace, supersede, deactivate, revoke, restore, or remap
authority-relevant administrative state in a supported target domain.

The governed rationale is:

- the operation changes current authority-relevant state or lifecycle meaning;
- predecessor governance prohibits self-grant, circular authority, and
  authority by technical control;
- the requestor or proposer MUST NOT be the sole authoritative participant
  determining the operation that changes the governed authority state; and
- authority independence is necessary to prevent nominal participant
  distinctness from satisfying separation where the approval authority is
  circular, self-created, or defeated by delegation control.

RS-A is the minimum v1 semantic control selected here. Stronger controls remain
unselected unless future authoritative governance requires them.

## 43. Business Entity Policy Coverage

Business Entity Administration Authority Governance v1 sufficiently governs
Business Entity establishment, activation, authority-relevant modification,
replacement, supersession, deactivation, revocation, and conditional
restoration/reactivation administration semantics for v1 SoD policy coverage.

This artifact governs only the SoD Requirement Set for those operations. It
does not create Business Entity authority, Business Entity identity,
restoration permission, persistence, runtime, or administration workflow.

## 44. Business Entity Requirement-Set Matrix

| Administrative target domain | Administrative operation/context | Requirement Set status | Requirement Set | Rationale | Governance status |
| --- | --- | --- | --- | --- | --- |
| Business Entity | ESTABLISH candidate Business Entity authority context | AUTHORITATIVE NON-EMPTY | RS-A | Establishment can initiate authority-bearing Business Entity state and must not be self-asserted by the requestor alone. | GOVERNED HERE |
| Business Entity | ACTIVATE current Business Entity authority context where activation is recognized | AUTHORITATIVE NON-EMPTY | RS-A | Activation can make authority-relevant Business Entity state current for downstream use. | GOVERNED HERE |
| Business Entity | MODIFY authority-relevant Business Entity state | AUTHORITATIVE NON-EMPTY | RS-A | Authority-relevant modification can affect identity, isolation, lifecycle validity, evidence, provenance, or downstream authority evaluation. | GOVERNED HERE |
| Business Entity | MODIFY non-authority-relevant presentation metadata | UNRESOLVED | None established here | Predecessor governance excludes ordinary presentation metadata unless it affects governed authority concerns. | DOWNSTREAM / FAIL-CLOSED WHERE POLICY REQUIRED |
| Business Entity | REPLACE Business Entity authority context | AUTHORITATIVE NON-EMPTY | RS-A | Replacement can affect lineage, historical meaning, and current authority interpretation. | GOVERNED HERE |
| Business Entity | SUPERSEDE Business Entity authority context | AUTHORITATIVE NON-EMPTY | RS-A | Supersession determines current identity/context without erasing historical meaning. | GOVERNED HERE |
| Business Entity | DEACTIVATE Business Entity authority context | AUTHORITATIVE NON-EMPTY | RS-A | Deactivation can remove current usability for future authority evaluation. | GOVERNED HERE |
| Business Entity | REVOKE Business Entity authority state | AUTHORITATIVE NON-EMPTY | RS-A | Revocation changes future authority evaluation and must be independently approved from the request. | GOVERNED HERE |
| Business Entity | RESTORE / REACTIVATE where otherwise authorized by future lifecycle governance | AUTHORITATIVE NON-EMPTY | RS-A | Restoration/reactivation can restore current authority effect and requires current independent approval if the operation is otherwise permitted. | GOVERNED HERE FOR SOD ONLY |

## 45. Principal Mapping Policy Coverage

Principal Mapping Administration Authority Governance v1 and Principal Mapping
Administrative Execution Governance v1 sufficiently govern Principal Mapping
operation and lifecycle semantics for v1 SoD policy coverage.

This artifact governs only the SoD Requirement Set for supported Principal
Mapping operations. It does not create Principal Mapping authority, execution
authority, stable Principal identity, persistence, runtime, or recovery
workflow.

## 46. Principal Mapping Requirement-Set Matrix

| Administrative target domain | Administrative operation/context | Requirement Set status | Requirement Set | Rationale | Governance status |
| --- | --- | --- | --- | --- | --- |
| Principal Mapping | ESTABLISH authoritative External Identity to stable Principal mapping | AUTHORITATIVE NON-EMPTY | RS-A | Establishment creates authority-relevant identity binding and must not rely solely on self-assertion or technical account evidence. | GOVERNED HERE |
| Principal Mapping | ACTIVATE mapping where lifecycle semantics require activation | AUTHORITATIVE NON-EMPTY | RS-A | Activation can make a mapping currently authoritative without creating downstream Membership, Entitlement, or ALLOW. | GOVERNED HERE |
| Principal Mapping | MODIFY authority-relevant mapping state | AUTHORITATIVE NON-EMPTY | RS-A | Authority-relevant modification can affect identity binding, scope, lifecycle, evidence, provenance, validity, or governance/version interpretation. | GOVERNED HERE |
| Principal Mapping | MODIFY cosmetic or presentation metadata with no governed authority effect | UNRESOLVED | None established here | Predecessor governance does not treat cosmetic metadata as authority-relevant merely because it exists. | DOWNSTREAM / FAIL-CLOSED WHERE POLICY REQUIRED |
| Principal Mapping | REMAP External Identity or stable Principal binding | AUTHORITATIVE NON-EMPTY | RS-A | Remapping can shift current identity binding and must preserve prior mapping provenance and historical interpretability. | GOVERNED HERE |
| Principal Mapping | REPLACE mapping authority context | AUTHORITATIVE NON-EMPTY | RS-A | Replacement changes authoritative mapping meaning and must not reduce to overwrite semantics. | GOVERNED HERE |
| Principal Mapping | SUPERSEDE mapping authority context | AUTHORITATIVE NON-EMPTY | RS-A | Supersession changes current mapping interpretation while preserving historical meaning. | GOVERNED HERE |
| Principal Mapping | DEACTIVATE mapping authority context | AUTHORITATIVE NON-EMPTY | RS-A | Deactivation removes current mapping use for future authority evaluation where current mapping authority is required. | GOVERNED HERE |
| Principal Mapping | REVOKE mapping authority context | AUTHORITATIVE NON-EMPTY | RS-A | Revocation must take precedence over stale technical or cached state and must be independently approved from the request. | GOVERNED HERE |
| Principal Mapping | RESTORE / REACTIVATE where otherwise authorized by current governance | AUTHORITATIVE NON-EMPTY | RS-A | Restoration/reactivation can restore current identity authority effect and must not be inferred from historical validity or technical rollback. | GOVERNED HERE FOR SOD ONLY |

## 47. Membership Policy Coverage

Membership Authority Source Governance v1 governs Membership authority-source
semantics, but current governance does not sufficiently establish Membership
administration operation semantics for concrete operation-specific SoD policy
content in this artifact.

Membership administration SoD Requirement Sets remain UNRESOLVED.

## 48. Entitlement Policy Coverage

Entitlement Semantics Governance v1 and Entitlement Authority Source
Governance v1 govern Entitlement semantics and authority-source requirements.

Current governance does not sufficiently establish a bounded Entitlement
administration operation taxonomy for concrete operation-specific SoD policy
content in this artifact.

Entitlement administration SoD Requirement Sets remain UNRESOLVED.

## 49. Resource Identity Policy Coverage

Resource Identity Authority Source Governance v1 governs Resource identity
authority-source semantics.

Current governance does not sufficiently establish Resource Identity
administration authority and operation semantics for concrete
operation-specific SoD policy content in this artifact.

Resource Identity administration SoD Requirement Sets remain UNRESOLVED.

## 50. Resource Classification / Binding Policy Coverage

Resource Classification Authority Governance v1, Resource Classification
Authority Source / Runtime Ownership Governance v1, and Resource Provisioning /
Classification Binding Governance v1 govern classification and binding
authority boundaries.

Current governance does not sufficiently establish Classification / Binding
administration operation-specific SoD policy content in this artifact.

Classification / Binding administration SoD Requirement Sets remain
UNRESOLVED.

## 51. Resource Action Applicability Policy Coverage

Resource x Action Applicability Governance v1 governs Principal-facing
Resource action applicability.

Current governance does not sufficiently establish Resource x Action
Applicability administration operation-specific SoD policy content in this
artifact.

Resource x Action Applicability administration SoD Requirement Sets remain
UNRESOLVED.

## 52. Partial Domain Coverage

This v1 artifact deliberately provides partial domain coverage.

It governs operation-specific Requirement Sets only where predecessor
administrative operation semantics and policy authority are sufficient.

Unresolved domains are not defects, empty sets, exemptions, or authorizations.
They remain fail-closed where a current authoritative Requirement Set is
required.

## 53. Establishment Policy

For supported Business Entity and Principal Mapping contexts, ESTABLISH has
Requirement Set RS-A where establishment affects authority-relevant state.

This policy does not authorize establishment, create the target, or bypass
authority-source requirements.

## 54. Activation Policy

For supported Business Entity and Principal Mapping contexts, ACTIVATE has
Requirement Set RS-A where activation makes authority-relevant state current
or usable under governed lifecycle semantics.

This policy does not require activation to exist as a physical workflow state.

## 55. Modification Policy

For supported Business Entity and Principal Mapping contexts, MODIFY has
Requirement Set RS-A only when the modification is authority-relevant under
predecessor governance.

Non-authority-relevant or cosmetic modification contexts receive no
authoritative empty set here. They are UNRESOLVED unless future governance
affirmatively establishes a Requirement Set.

## 56. Remapping Policy

For supported Principal Mapping contexts, REMAP has Requirement Set RS-A.

REMAP MUST NOT be treated as ordinary MODIFY where predecessor governance
distinguishes remapping from other mapping changes.

This artifact establishes no REMAP policy for domains that do not support a
governed REMAP operation.

## 57. Replacement Policy

For supported Business Entity and Principal Mapping contexts, REPLACE has
Requirement Set RS-A where replacement changes authority-relevant state,
lineage, current interpretation, or historical meaning.

Replacement MUST NOT be reduced to technical overwrite.

## 58. Supersession Policy

For supported Business Entity and Principal Mapping contexts, SUPERSEDE has
Requirement Set RS-A where supersession changes current authority-relevant
interpretation while preserving historical meaning.

Supersession policy MUST NOT be reused for replacement unless the exact
operation/context binding supports it.

## 59. Deactivation Policy

For supported Business Entity and Principal Mapping contexts, DEACTIVATE has
Requirement Set RS-A where deactivation removes current usability or current
authority effect.

This policy does not define deactivation mechanics or persistence.

## 60. Revocation Policy

For supported Business Entity and Principal Mapping contexts, REVOKE has
Requirement Set RS-A where revocation changes current or future authority
evaluation.

This policy does not impose the strongest possible control. It selects the
minimum governed request / approval separation and authority-independence
controls necessary to prevent unilateral requestor-controlled revocation.

## 61. Restoration / Reactivation Policy

For supported Business Entity and Principal Mapping contexts, RESTORE /
REACTIVATE has Requirement Set RS-A only where restoration or reactivation is
otherwise authorized by current applicable governance.

This artifact does not create restoration authority, reactivation authority,
technical rollback authority, or permission to disregard prior revocation
history.

## 62. Operation Equivalence

Operations MUST NOT be considered equivalent merely because they appear
related.

Any future equivalence among operations must be explicitly established by
authoritative governance. Otherwise each operation requires its own exact
binding or fails closed.

## 63. Policy Minimization

Requirement Sets MUST include only controls necessary for the governed
operation/context.

This v1 artifact selects RS-A and leaves stronger requirements unselected
because predecessor governance does not require approval / execution
separation, execution / verification separation, independent verification,
human-only approval, quorum, voting, or a broader participant-count rule for
the supported contexts.

## 64. No Security Theater

Requirements MUST NOT be added solely because they sound stronger or appear
more secure.

Every selected Requirement Set MUST trace to:

- governed SoD semantics;
- governed policy authority; and
- governed administrative context.

## 65. Policy Content / Implementation Separation

This artifact states what separation requirement applies. It does not state
how any implementation enforces it.

It does not select an approval queue, workflow engine, database transaction,
Lambda, Step Functions, IAM policy, Cognito group, OPA, Cedar, UI approval
button, or other implementation mechanism.

## 66. Policy Administration Boundary

This artifact does not select who operationally creates, changes, revokes,
supersedes, approves, or administers SoD policy.

Policy administration remains DOWNSTREAM.

## 67. Persistence Boundary

This artifact does not select where SoD policy or SoD determinations are
stored.

Persistence remains DOWNSTREAM / NOT SELECTED.

## 68. Runtime Boundary

This artifact does not select the runtime that resolves, evaluates, enforces,
or observes SoD policy.

Policy runtime remains DOWNSTREAM / NOT SELECTED.

## 69. Service Contract Boundary

This artifact does not define an API, endpoint, request schema, response
schema, transport, SDK, service contract, or service owner.

Service-contract governance remains DOWNSTREAM / NOT SELECTED.

## 70. IAM Boundary

IAM does not become SoD policy authority, SoD satisfaction evidence, or SoD
enforcement architecture through this artifact.

IAM implementation remains DOWNSTREAM / NOT SELECTED.

## 71. Cognito Boundary

Cognito identity, claims, groups, attributes, sessions, and administration do
not establish SoD policy, select Requirement Sets, satisfy SoD, or waive SoD.

Cognito implementation remains DOWNSTREAM / NOT SELECTED.

## 72. Website / Portal Boundary

Website and Portal behavior remains presentation-only relative to
authoritative SoD policy.

Browser state, UI labels, submitted values, route names, or displayed buttons
MUST NOT establish, modify, satisfy, or waive a Requirement Set.

## 73. AI Boundary

AI may explain approved SoD requirements, compare approved policy, and identify
governance gaps.

AI MUST NOT:

- choose Requirement Sets at runtime;
- strengthen Requirement Sets;
- weaken Requirement Sets;
- create exceptions;
- resolve policy ambiguity;
- manufacture missing policy;
- create human-approval requirements; or
- create risk tiers.

## 74. Assessment Service Boundary

Assessment Service remains the deterministic producer of assessment business
truth.

This artifact does not modify Assessment Service architecture and does not
make Assessment Service SoD policy authority.

## 75. EIP Boundary

EIP remains a consumer and derivation platform under its governed boundary.

This artifact does not modify EIP architecture and does not make EIP SoD
policy authority.

## 76. Privacy / Minimum Disclosure

SoD policy resolution MUST use only information necessary to resolve the
applicable policy.

It MUST NOT require unnecessary PII, raw identity-provider claims, credentials,
tokens, unrelated Business Entity data, unrelated Membership, unrelated
Entitlement, unrelated Resource data, Assessment Service content, EIP content,
or AI conversation content.

## 77. Idempotence / Side-Effect Safety

Policy resolution MUST NOT mutate policy authority, policy content,
administrative authority, Membership, Entitlement, Resource authorization,
Business Entity state, Principal Mapping state, or producer truth.

Repeated evaluation of unchanged authoritative inputs MUST produce equivalent
Requirement Set results.

## 78. Adversarial Validation

This artifact resolves the required adversarial cases as follows:

- A. Developer hard-codes two-person approval for REVOKE: REJECTED; technical
  code/configuration is not authoritative policy.
- B. Administrator creates a policy without authoritative policy basis:
  REJECTED; policy authority is required.
- C. AI recommends stronger control and runtime adopts it: REJECTED; AI and
  runtime discretion are non-authoritative.
- D. AI recommends weaker control and runtime adopts it: REJECTED; AI cannot
  waive governed requirements.
- E. Missing policy becomes empty Requirement Set: REJECTED; missing policy
  fails closed.
- F. B1 policy is reused for B2: REJECTED unless explicit broader authority
  exists.
- G. Principal Mapping policy is reused for Resource administration: REJECTED;
  target-domain binding is required.
- H. REVOKE policy is reused for RESTORE without authority: REJECTED;
  operation binding is required.
- I. MODIFY policy is reused for REMAP without authority: REJECTED; REMAP is
  independently bound where governed.
- J. G1 policy is used under incompatible G2: REJECTED; governance/version
  binding is required.
- K. Revoked policy remains active due to persistence: REJECTED; revoked
  policy is not current.
- L. Superseded policy remains active due to cache: REJECTED; superseded
  policy is not current.
- M. Two authoritative policies conflict: FAIL-CLOSED unless deterministic
  governance resolves the conflict.
- N. Administrator applies an override: REJECTED; override semantics are not
  selected.
- O. Runtime composes two policies: REJECTED; composition is not selected.
- P. Platform-wide default is invented: REJECTED; no implicit default exists.
- Q. Emergency bypass is invented: REJECTED; no exception governance means no
  authorized exception.
- R. Resource Classification silently changes SoD requirements: REJECTED;
  Resource Classification is not SoD policy.
- S. Entitlement is treated as SoD satisfaction: REJECTED; Entitlement is not
  SoD satisfaction.
- T. Authorization ALLOW is treated as SoD satisfaction: REJECTED;
  authorization is not SoD satisfaction.
- U. Policy requires named organizational role without governance basis:
  REJECTED; role model is not selected.
- V. Policy requires human approval without governance basis: REJECTED; human
  participation is not selected here.
- W. Policy adds risk tiers without governance basis: REJECTED; risk tiers are
  not selected.
- X. Empty set is authoritative without affirmative policy evidence: REJECTED;
  authoritative empty set requires affirmative evidence.
- Y. Requirement primitive is invented inside the artifact: REJECTED; only
  predecessor-governed primitives may be used.
- Z. Operation policy expands policy-maker authority: REJECTED; policy content
  cannot expand policy authority.

## 79. Authority Status Model

| Area | Status | Governance meaning |
| --- | --- | --- |
| SoD semantics | GOVERNED BY PREDECESSOR | Valid separation semantics remain defined by Administrative Separation of Duties Governance v1. |
| SoD applicability | GOVERNED BY PREDECESSOR | Applicability resolution remains defined by Administrative Separation of Duties Applicability Governance v1. |
| SoD policy authority | GOVERNED BY PREDECESSOR | Policy authority remains defined by Administrative Separation of Duties Requirement Set Authority / Policy Basis Governance v1. |
| Operation-specific Requirement Set semantics | GOVERNED HERE | This artifact defines v1 policy-content resolution semantics. |
| Business Entity operation-specific policy | GOVERNED HERE / PARTIALLY GOVERNED | Supported authority-relevant operations receive RS-A; non-authority-relevant contexts remain unresolved. |
| Principal Mapping operation-specific policy | GOVERNED HERE / PARTIALLY GOVERNED | Supported authority-relevant operations receive RS-A; non-authority-relevant contexts remain unresolved. |
| Membership operation-specific policy | UNRESOLVED | Administration operation semantics are insufficient for v1 concrete policy content. |
| Entitlement operation-specific policy | UNRESOLVED | Administration operation taxonomy remains insufficient for v1 concrete policy content. |
| Resource Identity operation-specific policy | UNRESOLVED | Administration authority/operation semantics remain unresolved. |
| Classification / Binding operation-specific policy | UNRESOLVED | No concrete SoD content selected. |
| Resource x Action Applicability operation-specific policy | UNRESOLVED | Applicability administration policy remains separate. |
| Participant count | NOT SELECTED | No universal count, quorum, majority, or voting rule. |
| Human participation | NOT SELECTED | No mandatory human approval rule. |
| Risk / sensitivity | NOT SELECTED | No risk, sensitivity, severity, or criticality tiers. |
| Emergency exceptions | NOT SELECTED | No bypass, waiver, override, or exception. |
| Defaults | NOT SELECTED | No implicit default policy. |
| Inheritance | NOT SELECTED | No policy inheritance. |
| Overrides | NOT SELECTED | No override semantics. |
| Composition | NOT SELECTED | No policy-fragment composition. |
| Policy administration | DOWNSTREAM | Who operationally changes policy is not selected. |
| Policy persistence | DOWNSTREAM / NOT SELECTED | No storage authority or technology selected. |
| Policy runtime | DOWNSTREAM / NOT SELECTED | No resolver or enforcement runtime selected. |
| Service contract | DOWNSTREAM / NOT SELECTED | No API, schema, endpoint, or service owner selected. |
| Enforcement | DOWNSTREAM / UNAUTHORIZED | Enforcement architecture is not selected. |
| Implementation | UNAUTHORIZED | This artifact authorizes no implementation. |

## 80. Resolved Here

This artifact resolves only:

- the deterministic operation-specific SoD Requirement Set model;
- the binding dimensions for operation-specific SoD policy;
- Requirement Set status semantics;
- RS-A as the v1 non-empty Requirement Set for supported authority-impacting
  Business Entity and Principal Mapping administrative operations;
- Business Entity operation-specific SoD policy for supported
  authority-relevant operations;
- Principal Mapping operation-specific SoD policy for supported
  authority-relevant operations;
- explicit unresolved treatment for Membership, Entitlement, Resource
  Identity, Classification / Binding, and Resource x Action Applicability
  administration policy content;
- missing, empty, conflict, default, inheritance, override, composition,
  lifecycle, provenance, auditability, deterministic, and fail-closed
  semantics for operation-specific policy; and
- non-authority and non-selection boundaries stated here.

It does not resolve full authorization architecture or implementation
readiness.

## 81. Remaining Governance

Likely blocking before initial authorization implementation, depending on the
bounded implementation slice:

- Trusted Authorization Service Contract evaluation;
- Authorization Persistence evaluation;
- Authorization Audit / Observability evaluation;
- Security / IAM Boundary evaluation;
- explicit bounded implementation authorization/readiness; and
- any target-domain administration policy whose implementation slice requires
  a currently UNRESOLVED operation-specific SoD Requirement Set.

Non-blocking downstream governance:

- SoD policy administration authority;
- SoD policy persistence;
- SoD policy runtime / enforcement architecture;
- SoD applicability administration;
- SoD applicability persistence;
- concrete policy administration workflow;
- Website / Portal administrative presentation behavior; and
- observability details beyond minimum implementation authorization needs.

Optional / future governance:

- risk or sensitivity models;
- emergency / break-glass governance;
- policy defaults;
- policy inheritance;
- policy overrides;
- policy composition;
- concrete organizational role models;
- participant-count policy beyond selected semantic separation; and
- mandatory human-participation policy.

This artifact does not declare every remaining item to be a standalone
governance artifact or immediate prerequisite.

## 82. Governance Proportionality

Future standalone governance artifacts SHOULD be created only where a genuine
unresolved semantic, authority, security, auditability, or
implementation-authorization dependency exists.

Implementation choices that can be safely governed within a bounded
implementation design MUST NOT be promoted into standalone governance gates
merely because they are undecided.

## 83. Implementation Gate

ADMINISTRATIVE / AUTHORIZATION / EXECUTION / PERSISTENCE /
SEPARATION-OF-DUTIES POLICY IMPLEMENTATION REMAINS UNAUTHORIZED.

This artifact does not authorize:

- administrative implementation;
- authorization implementation;
- SoD runtime implementation;
- policy persistence;
- policy administration tooling;
- service contracts;
- APIs;
- IAM changes;
- Cognito changes;
- Website or Portal changes;
- Assessment Service changes;
- EIP changes;
- AI enforcement; or
- deployment.

## 84. Duplication Review

This artifact adds genuine new governance.

It does not duplicate Administrative Separation of Duties Governance v1 because
it does not redefine SoD semantic primitives.

It does not duplicate Administrative Separation of Duties Applicability
Governance v1 because it does not merely define how applicability is resolved;
it supplies bounded v1 operation-specific policy content for supported
administrative domains.

It does not duplicate Administrative Separation of Duties Requirement Set
Authority / Policy Basis Governance v1 because it does not define what makes
policy authoritative; it defines the authoritative policy content that consumes
that authority model.

It does not duplicate generic authority governance, administrative execution
governance, or Resource x Action Applicability because it neither grants
administrative authority, governs execution, nor classifies Resource actions.

## 85. Architecture Decision

Nguyen AI v1 operation-specific Administrative SoD Requirement Set governance
is established for supported authority-impacting Business Entity and Principal
Mapping administrative operations.

Those supported contexts use Requirement Set RS-A.

All other administrative target domains and unsupported contexts remain
UNRESOLVED unless future authoritative governance establishes a concrete
Requirement Set.

No implementation is authorized.
