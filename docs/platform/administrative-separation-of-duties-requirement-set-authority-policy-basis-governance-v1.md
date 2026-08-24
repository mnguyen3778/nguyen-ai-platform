# Administrative Separation of Duties Requirement Set Authority / Policy Basis Governance v1

Version: v1

## 1. Purpose

This artifact governs what makes an Administrative Separation-of-Duties
Requirement-Set Policy authoritative for Nguyen AI administrative governance.

It establishes the conceptual authority and policy-basis semantics required
before future governance may legitimately define concrete operation-specific
SoD Requirement Sets.

It does not define which SoD requirements apply to any concrete operation.

## 2. Governance Status

Administrative SoD Requirement-Set Policy Authority semantics are GOVERNED
CONCEPTUALLY by this artifact.

Concrete operation-specific SoD Requirement Sets, participant-count policy,
mandatory human-participation policy, emergency or exception policy,
administration, persistence, runtime, service contracts, policy engines, and
implementation remain downstream or not selected as stated in this artifact.

## 3. Scope

This artifact governs:

- the Administrative SoD Requirement-Set Policy authority domain;
- the positive authority model for a policy fact to become authoritative;
- policy identity, evidence, scope, lifecycle, versioning, provenance,
  determinism, conflict handling, and fail-closed behavior;
- the separation between policy authority, policy content, policy
  administration, persistence, runtime representation, and applicability
  resolution; and
- non-authority boundaries necessary to prevent technical control, AI,
  repository state, IAM, Cognito, runtime ownership, or persistence from
  manufacturing SoD policy authority.

## 4. Non-Scope

This artifact does not define, select, or authorize:

- concrete operation-specific SoD Requirement Sets;
- mappings for ESTABLISH, ACTIVATE, MODIFY, REPLACE, SUPERSEDE, DEACTIVATE,
  REVOKE, RESTORE, REACTIVATE, REMAP, or any other administrative operation;
- participant counts, quorum, majority, or voting requirements;
- mandatory human approval or universal human participation;
- risk tiers, sensitivity tiers, severity tiers, or criticality tiers;
- emergency, break-glass, waiver, override, or exception policy;
- organizational roles, role hierarchy, or staffing topology;
- workflow, ticketing, queue, notification, or state-machine topology;
- persistence technology, runtime, API, service contract, policy engine,
  IAM, Cognito, Website, Assessment Service, EIP, or AWS changes; or
- implementation, deployment, or production readiness.

## 5. Predecessor Governance

This artifact depends on and preserves:

- Administrative Separation of Duties Governance v1;
- Administrative Separation of Duties Applicability Governance v1;
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

## 6. Four-Layer Separation

The following separations are mandatory:

```text
SOD SEMANTICS != SOD APPLICABILITY
SOD APPLICABILITY != SOD REQUIREMENT-SET POLICY AUTHORITY
SOD REQUIREMENT-SET POLICY AUTHORITY != CONCRETE OPERATION-SPECIFIC REQUIREMENT SET
```

Administrative Separation of Duties Governance v1 governs what valid
separation means.

Administrative Separation of Duties Applicability Governance v1 governs how
authoritative operation/context facts and authoritative policy facts are
resolved into an applicability outcome.

This artifact governs what makes the SoD Requirement-Set Policy fact itself
authoritative.

Future operation-specific governance may define concrete requirement sets only
after the policy fact can be grounded in valid authority.

## 7. Central Governance Question

The central question governed here is:

```text
What makes policy P an authoritative Administrative SoD Requirement-Set Policy?
```

This artifact answers why P may be relied upon as authoritative policy. It
does not answer which concrete SoD requirements P assigns to a specific
operation.

## 8. Terminology

For this artifact:

- Administrative SoD Requirement-Set Policy means the governed policy fact
  that authoritatively establishes, for a bounded administrative operation
  and context, what SoD Requirement Set future applicability resolution may
  consume.
- SoD Requirement-Set Policy Authority Basis means the governed
  organizational, business, or governance authority competent to establish
  that policy fact within a bounded scope.
- Policy Evidence means the authoritative support used to validate policy
  identity, authority basis, scope, lifecycle, governance/version, and
  provenance.
- Policy Resolution means deterministic consumption of authoritative policy
  facts by future applicability evaluation.

These are conceptual governance terms and select no representation.

## 9. Governed Policy Fact

An Administrative SoD Requirement-Set Policy is a governed policy fact.

It is distinct from:

- configuration;
- persistence;
- runtime state;
- audit records;
- UI representation;
- recommendation;
- draft;
- proposal; and
- historical version.

A technical representation may carry evidence only when an independent
governed authority basis and all validity requirements are satisfied.

## 10. Positive Policy Authority Model

A policy P is authoritative only when authoritative evidence establishes all
required conditions:

- a governed policy identity exists;
- the policy is in the Administrative SoD Requirement-Set Policy domain;
- a valid SoD Requirement-Set Policy Authority Basis supports P;
- the supporting evidence is authoritative and provenance-backed;
- policy scope is valid and explicit enough for the governed use;
- Business Entity binding is valid where applicable;
- target-domain binding is valid;
- governance/version binding is valid;
- lifecycle/current validity is satisfied where current policy is required;
- interpretation is deterministic; and
- the authority chain is non-circular.

Technical storage, runtime loading, repository existence, IAM permission,
Cognito status, browser state, or AI output is not part of the authority
model.

## 11. Required Conditions

Failure of any required authority condition produces no affirmative policy
authority.

The result is not an empty SoD Requirement Set, not a waiver, and not
authorization to proceed without SoD.

## 12. Authority Basis

The SoD Requirement-Set Policy Authority Basis is the legitimate governed
organizational, business, or governance authority competent to establish a
policy fact for the bounded Administrative SoD Requirement-Set Policy domain.

It must be independent of:

- technical control;
- repository write access;
- IAM permission;
- Cognito status;
- database access;
- runtime ownership;
- developer status;
- Website administration; and
- AI recommendation.

## 13. Authority Source / Technical Source Separation

The following separation is mandatory:

```text
AUTHORITY SOURCE != TECHNICAL SOURCE
```

A future authority source for SoD Requirement-Set Policy must be capable of
providing authoritative policy evidence, provenance, lifecycle validity,
scope, governance/version binding, and deterministic validation.

This artifact does not select a database, Git repository, configuration file,
API, Lambda, policy engine, workflow engine, IAM, Cognito, or any other
technical source.

## 14. Policy Identity

An authoritative policy must have stable conceptual identity sufficient to
distinguish it from other policy facts and from historical versions.

Policy identity is not the same as:

- a persistence key;
- a file path;
- a commit;
- a tag;
- a runtime object; or
- an audit event.

This artifact selects no identifier format.

## 15. Policy Authority Domain

The bounded authority domain is:

```text
Administrative SoD Requirement-Set Policy Domain
```

This domain is distinct from Resource x Action Applicability, Resource
Classification, Membership, Entitlement, Business Entity identity, Principal
Mapping, Resource authorization, IAM policy, Cognito groups, and generic
technical configuration.

## 16. Policy Evidence

Authoritative policy evidence must substantively establish:

- policy identity;
- policy authority basis;
- policy scope;
- target-domain binding;
- operation/context binding where applicable;
- governance/version context;
- lifecycle/current status where current use is required; and
- provenance.

This artifact does not select evidence storage, schema, repository layout,
record format, or API payload.

## 17. Policy Scope

Policy scope must be explicit enough to prevent unauthorized reuse.

Potential scope dimensions include, where applicable:

- administrative target domain;
- administrative operation;
- Business Entity context;
- lifecycle context;
- authority-impact context; and
- governance/version context.

No scope dimension is required universally unless applicable governance makes
it material for the policy fact.

## 18. Business Entity Isolation

Policy authority for one Business Entity does not automatically establish
policy authority for another Business Entity.

```text
AUTHORITY FOR B1 != AUTHORITY FOR B2
```

Broader scope may exist only when explicit governed authority establishes it.
This artifact does not create tenant-specific concrete policy.

## 19. Target-Domain Isolation

Policy authority for one administrative target domain does not automatically
establish policy authority for another target domain.

```text
POLICY AUTHORITY FOR PRINCIPAL MAPPING != POLICY AUTHORITY FOR BUSINESS ENTITY ADMINISTRATION
POLICY AUTHORITY FOR BUSINESS ENTITY ADMINISTRATION != POLICY AUTHORITY FOR MEMBERSHIP
POLICY AUTHORITY FOR MEMBERSHIP != POLICY AUTHORITY FOR ENTITLEMENT
POLICY AUTHORITY FOR ENTITLEMENT != POLICY AUTHORITY FOR RESOURCE ADMINISTRATION
POLICY AUTHORITY FOR RESOURCE ADMINISTRATION != POLICY AUTHORITY FOR CLASSIFICATION
POLICY AUTHORITY FOR CLASSIFICATION != POLICY AUTHORITY FOR APPLICABILITY ADMINISTRATION
```

Cross-domain policy authority requires explicit governed scope.

## 20. Operation / Context Binding

Where a policy is bound to an administrative operation or context, that binding
must be authoritative and explicit enough for deterministic use.

Policy for one operation or context must not automatically transfer to another
operation or context.

This artifact does not assign requirements to any specific operation.

## 21. Policy Establishment

The following separations are mandatory:

```text
DRAFT != AUTHORITATIVE POLICY
PROPOSAL != AUTHORITATIVE POLICY
RECOMMENDATION != AUTHORITATIVE POLICY
CONFIGURATION != AUTHORITATIVE POLICY
PERSISTED RECORD != AUTHORITATIVE POLICY
```

A policy becomes authoritative only through the positive authority model
defined by this artifact and any applicable successor governance.

## 22. Establishment / Validation Separation

Policy establishment is not policy validation.

Validation verifies whether the required authority, evidence, scope,
lifecycle, governance/version, provenance, and non-circularity conditions are
satisfied.

Validation must not manufacture authority.

## 23. Establishment / Resolution Separation

Policy establishment is not policy resolution.

Applicability resolution must consume authoritative policy. A resolver must
not invent, establish, alter, or select policy merely by resolving it.

## 24. Establishment / Administration Separation

Policy authority is not policy administration.

This artifact governs what makes a policy authoritative. It does not select
who operationally creates, edits, approves, revokes, supersedes, or administers
policy.

Policy administration remains downstream.

## 25. Establishment / Persistence Separation

Policy authority is not policy persistence.

Persistence may preserve or transmit evidence, but a persistence write does
not create business or governance authority.

Persistence remains downstream and not selected.

## 26. Policy Lifecycle

A policy fact may conceptually have lifecycle states including:

- PROPOSED;
- CURRENT;
- SUPERSEDED;
- REVOKED; and
- HISTORICAL.

These states are governance semantics only. This artifact does not create a
workflow, state machine, storage model, approval queue, API, or user interface.

## 27. Current Authority

Current authority means the policy is valid for authoritative reliance under
the applicable policy identity, scope, lifecycle, and governance/version
context at the time it is materially relied upon.

Historical existence does not imply current authority.

## 28. Supersession

A superseded policy must not remain current merely because it:

- persists;
- remains cached;
- remains in Git history;
- remains referenced by stale consumers; or
- appears in an audit trail.

Where current policy is required, superseded policy is not current authority.

## 29. Revocation

A revoked policy must not remain current merely because a technical
representation survives.

Revocation of policy content is a policy lifecycle fact and must be
distinguished from revocation of policy-making authority.

## 30. Replacement

Policy replacement requires governed authority and continuity.

An overwrite, file replacement, database update, deployment, runtime reload, or
configuration change does not establish replacement authority by itself.

## 31. Policy-Making Authority Revocation

Revocation of authority to establish policy and revocation of an established
policy are separate facts.

An actor whose policy-making authority is revoked must not establish future
policy merely because the actor previously had authority.

An existing policy does not become revoked solely because a policy maker's
future authority is revoked unless applicable governance establishes that
effect.

## 32. Versioning

Policy authority must be bound to governance/version context.

```text
POLICY VALID UNDER G1
does not automatically remain valid under
INCOMPATIBLE G2
```

Versioning semantics do not select file formats, schema fields, database
columns, headers, tags, branches, or APIs.

## 33. Provenance

Sufficient provenance is required to reconstruct:

- policy identity;
- authority basis;
- scope;
- supporting evidence;
- governance/version context; and
- lifecycle status.

Provenance is evidence about authority. It is not authority by itself.

```text
PROVENANCE != AUTHORITY
```

## 34. Auditability

Policy establishment, validation, supersession, replacement, revocation, and
authoritative resolution must be auditable at the conceptual level.

Auditability does not make an audit record authoritative policy.

```text
AUDIT RECORD != POLICY AUTHORITY
```

This artifact does not select audit storage, observability tooling, logging
format, event schema, or retention mechanism.

## 35. Determinism

The same authoritative policy evidence, authority context, and
governance/version context must produce the same authoritative policy meaning.

Heuristic, probabilistic, AI-inferred, runtime-preferred, or operator-preferred
interpretation must not create authoritative policy meaning.

## 36. Conflict Handling

Conflicting apparently-authoritative policy facts must fail closed unless
applicable governance deterministically resolves the conflict.

This artifact does not select:

- last-write-wins;
- newest database record;
- Git commit order;
- runtime priority;
- majority vote;
- administrator preference;
- source preference by technical location; or
- AI-selected precedence.

## 37. Missing Policy

Missing authoritative policy must not silently become an empty Requirement
Set.

```text
MISSING AUTHORITATIVE POLICY != EMPTY REQUIREMENT SET
MISSING AUTHORITATIVE POLICY != NO SOD REQUIRED
```

Where an authoritative policy is required and no current authoritative policy
can be established, the result must fail closed.

## 38. Authoritative Empty Policy Content

A future concrete policy may affirmatively establish that no additional SoD
Requirement Set applies to a bounded operation/context.

That empty set must itself be authoritative, scoped, current,
governance/version-valid, and provenance-backed.

```text
AUTHORITATIVE EMPTY SET != MISSING POLICY
```

This artifact does not select which operations, if any, receive empty sets.

## 39. Circular Authority Prohibition

Policy must not establish its own authority.

A policy maker must not become authoritative solely because the same policy
says that actor is authoritative to establish it.

A runtime must not establish policy merely by evaluating it.

Persistence must not establish policy merely by storing it.

A repository must not establish policy merely by containing it.

Authority must trace to an independent governed authority basis.

## 40. Self-Grant Prohibition

A subject must not gain authority to weaken controls governing itself merely
by self-designation, self-authored policy, self-approved policy, or circularly
created policy-making authority.

This artifact does not create an approval workflow.

## 41. Privilege-Escalation Prohibition

SoD policy authority must not silently expand:

- Principal authority;
- Membership;
- Entitlement;
- Business Entity scope;
- Resource authorization; or
- administrative execution authority.

Authority to define policy is not authority to perform governed operations.

## 42. Bootstrap / Root Boundary

Administrative Bootstrap / Root Authority Governance v1 remains authoritative
for terminating legitimacy, root authority, bootstrap operations,
non-circularity, lifecycle, and fail-closed behavior.

SoD Requirement-Set Policy Authority must be grounded in a valid governed
authority chain where required.

Root or bootstrap authority does not automatically establish concrete SoD
policy content.

## 43. Delegation

If SoD policy-making authority is delegated by future governance, delegated
authority must not exceed delegating authority.

```text
DELEGATED AUTHORITY <= DELEGATING AUTHORITY
```

Delegation must not expand domain, Business Entity scope, target scope,
lifecycle authority, governance/version authority, or policy content authority.

This artifact does not define delegation records, workflows, APIs, roles, or
implementation.

## 44. Authority Lifecycle

Authority to establish SoD Requirement-Set Policy may itself become valid,
expire, be revoked, be superseded, or become historical under applicable
governance.

Policy-maker authority lifecycle is distinct from policy lifecycle.

## 45. Generic Authority Governance Relationship

Authority Administration / Revocation Governance v1 governs administrative
authority and revocation semantics for governed authorization state and
preserves SoD policy as downstream.

This artifact does not duplicate generic administration governance. It governs
the distinct bounded fact of what makes Administrative SoD Requirement-Set
Policy authoritative.

## 46. Business Entity Administration Boundary

Authority to administer a Business Entity is not authority to define
Administrative SoD Requirement-Set Policy.

```text
AUTHORITY TO ADMINISTER BUSINESS ENTITY != AUTHORITY TO DEFINE SOD POLICY
```

Business Entity administration authority may be relevant evidence only where
future governance explicitly grants policy authority within scope.

## 47. Principal Mapping Administration Boundary

Authority to administer Principal Mapping is not authority to define SoD
policy governing Principal Mapping.

```text
AUTHORITY TO ADMINISTER PRINCIPAL MAPPING != AUTHORITY TO DEFINE SOD POLICY GOVERNING PRINCIPAL MAPPING
```

Principal Mapping administration remains compatible with future
operation-specific SoD policy, but it does not create that policy.

## 48. Operation Authority / Policy Authority Separation

The following separations are mandatory:

```text
AUTHORITY TO PERFORM O != AUTHORITY TO DEFINE CONTROL POLICY FOR O
AUTHORITY TO APPROVE O != AUTHORITY TO DEFINE CONTROL POLICY FOR O
```

An operation actor, approver, verifier, or executor does not become policy
authority merely by participating in the operation.

## 49. Concrete Policy Content Prohibition

This artifact establishes no concrete operation-specific SoD mappings.

It does not define the SoD Requirement Set for ESTABLISH, ACTIVATE, MODIFY,
REPLACE, SUPERSEDE, DEACTIVATE, REVOKE, RESTORE, REACTIVATE, REMAP, or any
other operation.

Concrete operation-specific policy remains downstream.

## 50. Participant Count Boundary

This artifact does not select:

- one participant;
- two participants;
- three participants;
- quorum;
- majority; or
- any participant-count rule.

Participant-count policy remains downstream and not selected.

## 51. Human Participation Boundary

This artifact does not establish mandatory human approval.

```text
SOD != HUMAN APPROVAL automatically
```

Where future governance requires human participation, that requirement must be
separately and authoritatively established.

## 52. Risk / Sensitivity Boundary

This artifact does not create risk tiers, sensitivity tiers, severity tiers,
criticality tiers, or numerical scoring.

Resource Classification is not an administrative SoD policy basis unless
future governance explicitly establishes that relationship.

```text
RESOURCE CLASSIFICATION != ADMINISTRATIVE SOD POLICY BASIS automatically
```

## 53. Emergency / Exception Boundary

This artifact creates no emergency bypass, break-glass bypass, waiver,
override, or exception policy.

Absence of exception governance does not imply an exception exists.

Emergency or break-glass governance remains downstream.

## 54. Resource Classification Non-Authority

Resource Classification must not establish Administrative SoD Requirement-Set
Policy merely by classifying a Resource.

Classification may affect authorization only within its own governed domain
and any explicitly governed future relationship.

## 55. Resource Action Applicability Non-Authority

Resource x Action Applicability must not establish Administrative SoD
Requirement-Set Policy.

Resource x Action Applicability answers whether a Principal-facing Action is
applicable to a governed Resource class/context. It is not authority over
administrative SoD policy.

## 56. Membership Non-Authority

Membership must not establish SoD policy merely because a Principal is a
member of a Business Entity, Client, Organization, Engagement, or other
governed scope.

Membership is not SoD policy authority.

## 57. Entitlement Non-Authority

Entitlement must not establish SoD policy merely because authority exists to
perform an action or because a Principal has a permission.

Entitlement is not authority to define the control policy governing
administrative operations.

## 58. Authorization Non-Authority

The following separations are mandatory:

```text
AUTHORIZATION ALLOW != AUTHORITY TO DEFINE SOD POLICY
AUTHORITATIVE SOD POLICY != RESOURCE AUTHORIZATION
```

SoD policy may become an administrative governance input where future
governance authorizes it. It does not become Resource authorization.

## 59. Persistence Non-Authority

Persistence does not establish policy authority.

A database row, file, object, message, cache entry, backup, snapshot, document,
or configuration record is not authoritative policy merely because it exists
or can be written.

No persistence technology is selected.

## 60. Runtime Non-Authority

Runtime loading, resolving, evaluating, caching, displaying, or enforcing a
policy representation must not create SoD policy authority.

No runtime, runtime owner, Lambda, workflow engine, service, queue, scheduler,
or evaluation boundary is selected.

## 61. Service Contract Non-Selection

This artifact does not define an API, endpoint, request schema, response
schema, service contract, transport, service owner, event contract, command
contract, or message contract.

Service contract governance remains downstream.

## 62. Policy Engine Non-Selection

This artifact does not select RBAC, ABAC, ACL, OPA, Cedar, IAM policy,
Cognito groups, a custom policy engine, or any policy evaluation technology.

Policy authority semantics remain independent from policy-engine selection.

## 63. Git / Repository Non-Authority

The following separations are mandatory:

```text
FILE IN REPOSITORY != AUTHORITATIVE BUSINESS POLICY automatically
COMMIT != BUSINESS POLICY AUTHORITY automatically
TAG != BUSINESS POLICY AUTHORITY automatically
```

Git may provide provenance or evidence when future governance permits it. Git
does not become business policy authority merely through technical existence.

## 64. IAM Non-Authority

IAM permission to edit, deploy, read, evaluate, or administer a technical
representation does not imply authority to establish Administrative SoD
Requirement-Set Policy.

IAM is not SoD policy authority.

## 65. Cognito Non-Authority

Cognito identity, group, claim, attribute, authentication status, or
administrator status does not establish SoD policy authority.

Cognito may authenticate where future architecture permits, but authentication
is not policy authority.

## 66. Website / Browser Non-Authority

Website and browser state remain presentation-layer or interaction-layer
state relative to authoritative policy.

Submitted UI state, browser storage, client-side flags, form values, or
screen labels must not independently establish authoritative policy.

## 67. AI Non-Authority

AI may potentially explain approved policy, compare approved policy, identify
governance gaps, or recommend candidate controls where future governance
permits.

AI output is not authoritative SoD policy.

AI must not establish participant count, mandatory human approval,
operation-specific requirements, exemptions, emergency bypasses, provenance,
or authority.

## 68. Assessment Service Boundary

Assessment Service remains the deterministic producer of assessment business
truth.

It is not SoD policy authority and is not assigned SoD policy administration,
applicability, approval, execution, persistence, runtime, or authorization
responsibility by this artifact.

## 69. EIP Boundary

EIP remains a governed consumer and derivation platform within its approved
producer/consumer boundary.

It is not SoD policy authority and is not assigned policy-making authority by
this artifact.

## 70. Portal Boundary

Portal and Website remain presentation consumers relative to authoritative
policy.

Portal state, display labels, workflow screens, and browser assertions are not
SoD policy authority.

## 71. Privacy / Minimum Disclosure

Policy authority validation and resolution must use minimum necessary
information.

They must not require unnecessary PII, raw IdP claims, tokens, credentials,
email addresses, usernames, unrelated Business Entity data, unrelated
Membership, unrelated Entitlement, unrelated Resource data, Assessment Service
content, EIP content, or Website presentation data.

## 72. Idempotence / Side-Effect Safety

Conceptual validation or resolution of policy authority must not mutate policy
authority merely by evaluating it.

Repeated evaluation of unchanged authoritative inputs under the same
governance/version context must not create new authority, alter lifecycle
state, change policy content, or authorize an administrative operation.

## 73. Fail-Closed Behavior

The following conditions must fail closed where authoritative policy is
required:

- missing authority basis;
- missing authoritative evidence;
- invalid scope;
- Business Entity mismatch;
- target-domain mismatch;
- invalid governance/version;
- revoked policy-making authority;
- revoked policy;
- superseded policy where current policy is required;
- conflicting authoritative evidence;
- circular authority; and
- indeterminate authority.

Uncertainty must not be translated into an empty Requirement Set or into no
SoD required.

## 74. Policy Authority Status Model

| Governance area | Status |
| --- | --- |
| SoD semantic model | GOVERNED BY PREDECESSOR |
| SoD applicability model | GOVERNED BY PREDECESSOR |
| SoD Requirement-Set Policy authority semantics | GOVERNED HERE |
| SoD Requirement-Set Policy authority basis | GOVERNED CONCEPTUALLY |
| Authority source requirements | GOVERNED CONCEPTUALLY; CONCRETE SOURCE NOT SELECTED |
| Policy identity | GOVERNED CONCEPTUALLY |
| Policy scope | GOVERNED CONCEPTUALLY |
| Policy establishment semantics | GOVERNED CONCEPTUALLY |
| Establishment / validation / resolution separation | GOVERNED |
| Policy lifecycle | GOVERNED CONCEPTUALLY |
| Versioning | GOVERNED CONCEPTUALLY |
| Revocation and supersession | GOVERNED CONCEPTUALLY |
| Provenance and auditability | GOVERNED CONCEPTUALLY |
| Conflict handling | GOVERNED CONCEPTUALLY / FAIL CLOSED |
| Concrete operation-specific policy content | DOWNSTREAM / UNRESOLVED |
| Participant-count policy | DOWNSTREAM / NOT SELECTED |
| Human-participation policy | DOWNSTREAM / NOT SELECTED |
| Risk / sensitivity model | NOT SELECTED |
| Emergency / exception policy | DOWNSTREAM / UNRESOLVED |
| Policy administration | DOWNSTREAM / UNRESOLVED |
| Policy persistence | DOWNSTREAM / NOT SELECTED |
| Policy runtime | DOWNSTREAM / NOT SELECTED |
| Service contract | DOWNSTREAM / NOT SELECTED |
| Policy engine | DOWNSTREAM / NOT SELECTED |
| Organizational roles | DOWNSTREAM / NOT SELECTED |
| Implementation | UNAUTHORIZED |

No downstream, unresolved, or not-selected item is resolved by implication.

## 75. Resolved Here

This artifact resolves only:

- the distinction between SoD semantics, SoD applicability, SoD
  Requirement-Set Policy authority, and concrete operation-specific
  requirement sets;
- the Administrative SoD Requirement-Set Policy authority domain;
- positive authority-basis requirements for policy facts;
- policy identity, evidence, scope, Business Entity binding, target-domain
  binding, lifecycle, versioning, provenance, and deterministic validation;
- establishment, validation, resolution, administration, and persistence
  separations;
- current, superseded, revoked, historical, and replacement policy semantics
  at the conceptual level;
- circular-authority, self-grant, privilege-escalation, technical-control,
  repository, IAM, Cognito, Website, browser, AI, runtime, and persistence
  non-authority boundaries; and
- fail-closed treatment for missing, stale, revoked, superseded, conflicting,
  or indeterminate policy authority.

It does not claim operation-policy completion, implementation readiness, or
production readiness.

## 76. Remaining Governance

The following remain unresolved or downstream unless separately governed:

- concrete operation-specific SoD Requirement Sets;
- SoD policy administration;
- SoD policy persistence;
- SoD applicability administration;
- SoD applicability persistence;
- participant-count policy;
- human-participation policy;
- emergency / exception governance;
- Business Entity persistence;
- Resource Provisioning Authority;
- Resource Identity Administration Authority;
- Resource Identity Persistence Authority;
- Classification / Binding Administration;
- Classification / Binding Persistence;
- Applicability Administration;
- Engagement Scope;
- Trusted Authorization Service Contract;
- Authorization Persistence;
- Authorization Audit / Observability;
- Security / IAM Boundary and enforcement; and
- explicit implementation authorization.

This list does not declare every item an immediate prerequisite.

## 77. Implementation Gate

ADMINISTRATIVE / AUTHORIZATION / EXECUTION / PERSISTENCE / SEPARATION-OF-DUTIES POLICY IMPLEMENTATION REMAINS UNAUTHORIZED.

This artifact does not authorize runtime behavior, persistence, APIs, service
contracts, policy engines, workflow, IAM, Cognito, Website changes,
Assessment Service changes, EIP changes, AWS changes, deployment, or
production operation.

## 78. Duplication Review

This artifact does not duplicate Administrative Separation of Duties
Governance v1 because it does not redefine valid SoD participation,
participant distinctness, independence, duty separation, or SoD satisfaction.

It does not duplicate Administrative Separation of Duties Applicability
Governance v1 because it does not define applicability result semantics or
resolution mechanics; it defines what makes the policy fact consumed by
applicability authoritative.

It does not duplicate Authority Administration / Revocation Governance v1,
Business Entity Administration Authority Governance v1, Principal Mapping
Administration Authority Governance v1, Administrative Bootstrap / Root
Authority Governance v1, or Resource x Action Applicability Governance v1
because each governs a distinct authority domain.

This artifact adds genuine bounded governance for SoD Requirement-Set Policy
authority and policy basis.

## 79. Adversarial Policy Authority Review

The following cases are governed by this artifact:

- A. Developer writes a two-person REVOKE rule into configuration: FAIL CLOSED.
  Configuration is not policy authority.
- B. IAM administrator claims editing permission equals policy authority: FAIL
  CLOSED. IAM permission is not SoD policy authority.
- C. Database administrator inserts a policy record: FAIL CLOSED. Persistence
  is not authority.
- D. Runtime owner modifies loaded policy: FAIL CLOSED. Runtime ownership is
  not policy authority.
- E. Git maintainer merges a rule and claims merge creates authority: FAIL
  CLOSED. Commit authority is not business policy authority.
- F. AI recommends a rule and it is treated as authoritative: FAIL CLOSED. AI
  output is not authoritative policy.
- G. Business Entity administrator claims platform-wide SoD policy authority:
  FAIL CLOSED unless independent governed policy authority establishes that
  scope.
- H. Principal Mapping administrator claims authority over SoD policy itself:
  FAIL CLOSED. Operation administration authority is not policy authority.
- I. Applicability resolver invents missing policy: FAIL CLOSED. Resolution is
  not establishment.
- J. Policy declares itself authoritative: FAIL CLOSED. Self-declared policy
  authority is circular.
- K. Policy maker self-grants authority to weaken controls: FAIL CLOSED unless
  independent governed authority exists and self-grant prohibitions are
  satisfied.
- L. Delegate exceeds delegating authority: FAIL CLOSED. Delegation cannot
  expand authority.
- M. B1 policy is reused for B2 without authority: FAIL CLOSED. Business
  Entity scope does not transfer automatically.
- N. Principal Mapping policy is reused for Resource administration: FAIL
  CLOSED. Target-domain scope does not transfer automatically.
- O. G1 policy is reused under incompatible G2: FAIL CLOSED. Governance/version
  binding is required.
- P. Revoked policy remains active because persistence survives: FAIL CLOSED.
  Persistence does not preserve current authority.
- Q. Superseded policy remains active because runtime cache survives: FAIL
  CLOSED. Runtime cache is not current authority.
- R. Conflicting policy facts exist: FAIL CLOSED unless deterministic
  governance resolves the conflict.
- S. Missing policy becomes empty Requirement Set: FAIL CLOSED. Missing policy
  is not an authoritative empty set.
- T. Multiple unauthorized actors agree and claim consensus creates authority:
  FAIL CLOSED. Consensus without authority is not authority.
- U. Root/bootstrap legitimacy is manufactured through ordinary SoD agreement:
  FAIL CLOSED. Bootstrap/root governance remains authoritative.
- V. Emergency bypass is claimed without emergency governance: FAIL CLOSED.
  This artifact creates no exception.
- W. Audit record is treated as authority: FAIL CLOSED. Audit record is not
  policy authority.
- X. Git tag is treated as business policy authority: FAIL CLOSED. Tag
  existence is not business policy authority.

These outcomes reject or fail closed without inventing concrete SoD content.

## 80. Cross-Governance Consistency

This artifact preserves:

- Assessment Service producer truth;
- EIP consumer and derivation boundaries;
- Website and Portal presentation boundaries;
- authentication / authorization separation;
- Principal, Membership, Entitlement, Resource, Resource Classification, and
  Resource x Action Applicability separation;
- Business Entity isolation;
- bootstrap/root governance;
- SoD semantic governance; and
- SoD applicability governance.

No predecessor authority is weakened or reassigned.

## 81. Technology Neutrality

This artifact is technology-neutral governance.

It selects no database, repository format, schema, API, endpoint, Lambda,
workflow engine, policy engine, IAM role, Cognito group, runtime, service,
queue, event bus, user interface, cloud service, or deployment architecture.

## 82. Acceptance Criteria

This artifact is acceptable only if it:

- governs what makes a concrete Administrative SoD Requirement-Set Policy
  authoritative without defining the concrete policy content;
- preserves the four-layer separation model;
- provides a positive, non-circular authority model;
- preserves policy authority, content, administration, persistence, runtime,
  and resolution as distinct concepts;
- preserves Business Entity and target-domain isolation;
- rejects technical control, repository state, IAM, Cognito, Website/browser,
  runtime, persistence, audit records, and AI as standalone authority;
- preserves participant-count, human-participation, risk, emergency,
  persistence, runtime, service contract, policy engine, role model, and
  implementation as downstream, not selected, or unauthorized; and
- contains no implementation authorization.

## 83. Architecture Decision

Administrative Separation of Duties Requirement Set Authority / Policy Basis
Governance v1 is approved as a bounded conceptual governance artifact when
accepted by independent review.

It establishes policy-authority semantics required before concrete
operation-specific SoD Requirement Sets can be governed.

It does not authorize implementation and does not begin operation-specific
requirement-set governance.
