# Trusted Authorization Recovery Responsibility Assignment Authority Governance v1

## 1. Status

This document is a governance artifact for the Nguyen AI Platform Trusted
Authorization architecture.

It is governance-only. It does not implement recovery, create runtime code,
create tests, create persistence, create schemas, create APIs, create
workflows, create credentials, select technology, assign participants, select
participant count, select quorum, establish universal dual approval, establish
universal maker/checker, establish break-glass, instantiate a TAB, activate
Recovery Authority, establish standing root, establish successor, authorize
restoration, deploy, touch AWS resources, commit, tag, push, or grant
production authority.

PRODUCTION AUTHORITY: NOT GRANTED
## 2. Purpose

This artifact formalizes the governance model for the authority that may
assign, suspend, revoke, replace, or terminate logical Recovery
responsibilities.

It answers:

```text
What legitimate governance basis may assign, suspend, revoke, replace, or
terminate a Recovery responsibility without allowing the assignment mechanism
itself to become a self-authorizing, circular, standing, or hidden super-admin
authority source?
```

## 3. Scope

This artifact governs:

- Recovery Responsibility Assignment Authority;
- assignment legitimacy;
- terminating assignment-authority provenance;
- responsibility-class assignment sensitivity;
- assignment, suspension, revocation, replacement, restoration, and closure
  boundaries;
- assignment authorization and mutation separation;
- operation-specific assignment SoD;
- beneficiary-conflict controls;
- common-mode dependency controls;
- lifecycle/currentness requirements;
- fail-closed assignment semantics;
- assignment evidence boundaries; and
- unresolved downstream decisions.

## 4. Non-Scope

This artifact does not:

- assign concrete Assignment Authority;
- assign concrete participants;
- assign participant categories;
- select participant count;
- select quorum;
- create universal dual approval;
- create universal maker/checker;
- create break-glass;
- instantiate TAB;
- activate Recovery Authority;
- establish root;
- establish successor;
- authorize restoration;
- select credentials;
- select cryptography;
- select technology;
- create persistence, schema, API, workflow, runtime, deployment, tests, or
  code; or
- perform the downstream Trusted Authorization Recovery Responsibility
  Assignment / Revocation Ownership Realization Governance Review.

## 5. Authority

This artifact derives from the governance repository at checkpoint
`fe4fc5ecfe05e5050de51fa55347c18d74b2455e`.

It formalizes the immediately preceding read-only review decision:

```text
MODEL F - HYBRID BOUNDED ASSIGNMENT AUTHORITY
```

It does not create authority beyond the governance rules stated here.

## 6. Predecessor Governance

This artifact is governed by:

- `trusted-authorization-recovery-evidence-responsibility-participant-realization-governance-v1.md`
- `trusted-authorization-recovery-evidence-realization-governance-v1.md`
- `trusted-authorization-recovery-evidence-custody-verification-governance-v1.md`
- `trusted-authorization-recovery-terminating-authority-basis-governance-v1.md`
- `trusted-authorization-concrete-terminating-authority-basis-governance-v1.md`
- `trusted-authorization-root-specific-operation-level-sod-governance-v1.md`
- `trusted-authorization-administrative-mutation-revocation-ownership-governance-v1.md`
- `trusted-authorization-bounded-recovery-governance-v1.md`
- `trusted-authorization-root-recovery-topology-governance-v1.md`
- `trusted-authorization-root-lifecycle-retention-revocation-succession-governance-v1.md`
- `trusted-authorization-downstream-authority-impact-governance-v1.md`
- `trusted-authorization-emergency-authority-reduction-audit-failure-governance-v1.md`
- `trusted-authorization-bootstrap-root-terminating-authority-source-governance-v1.md`
- `trusted-authorization-production-authority-source-ownership-governance-v1.md`

Predecessor governance establishes:

- Model F - Hybrid Bounded Responsibility / Participant Realization;
- Model G - Hybrid Operation-Specific SoD;
- Model G - Hybrid Bounded Recovery TAB;
- Model I - Hybrid Bounded Terminating Authority Basis;
- assignment authority was intentionally unresolved;
- authorization != mutation;
- mutation success != legitimate authorization;
- failed administrative authorization -> no state change;
- Recovery TAB != Recovery Authority;
- Recovery Authority != successor;
- reduction != restoration;
- current revocation dominates stale positive evidence;
- responsibility independence != participant count;
- no universal quorum;
- no universal dual approval;
- no universal maker/checker;
- no unrestricted break-glass; and
- production authority remains not granted.

No direct predecessor contradiction was identified.

## 7. Selected Governance Model

The selected model is:

```text
MODEL F - HYBRID BOUNDED ASSIGNMENT AUTHORITY
```

This model combines, where applicable:

- bounded Administrative Authority;
- terminating provenance;
- responsibility-class scope;
- operation-specific authorization;
- minimum-necessary authority;
- Business Entity binding;
- environment binding;
- lifecycle/currentness;
- governance-version binding;
- beneficiary-conflict controls;
- provenance-based independence;
- common-mode dependency analysis;
- operation-specific SoD;
- separate assignment authorization and mutation execution;
- distinct assignment, suspension, revocation, replacement, restoration, and
  closure semantics;
- finite termination;
- fail-closed behavior;
- auditable evidence;
- no standing universal assigner;
- no universal participant count; and
- no universal quorum.

## 8. Model Rationale

Model F is selected because repository governance supports neither a standing
central assigner nor a universal dual-control/quorum model. Administrative
Authority derivation is necessary but insufficient by itself because assignment
authority must also be responsibility-class-bound, operation-bound,
scope-bound, lifecycle-bound, provenance-bound, and constrained by
operation-specific SoD.

TAB-derived authority is necessary for exceptional recovery contexts, but not
every ordinary reassignment requires TAB-level recovery. A hybrid bounded model
preserves ordinary governed administration while requiring terminating
provenance and stronger controls for authority-increasing, successor,
restoration, Recovery Authority, root, closure, and compromised-authority cases.

## 9. Definitions

| Term | Governance meaning | Boundary |
| --- | --- | --- |
| Recovery Responsibility | A logical recovery responsibility class governed by predecessor responsibility/participant realization governance. | Not authority by itself. |
| Assignment Authority | Governed legitimacy to authorize assignment, suspension, revocation, replacement, or termination of a responsibility within a bounded scope. | Not a participant, identity, credential, root, Recovery Authority, or mechanism. |
| Assignment Authorization | The governed decision that an assignment is permitted. | Not assignment mutation or execution. |
| Assignment Mutation | Technical recording or execution of an already-authorized assignment. | Mutation success does not prove legitimacy. |
| Assignment Evidence | Evidence that an assignment decision or record exists. | Not current authority by itself. |
| Assigned Responsibility | The responsibility granted to a future participant. | Not the authority to assign that responsibility. |
| Assignment Mechanism | Any future technical or procedural means that records, transmits, validates, or executes assignment. | Mechanism != Assignment Authority. |
| Assignment Record | A retained representation of an assignment. | Record != authority source. |
| Terminating Provenance | Finite governed authority chain that explains why Assignment Authority is legitimate. | Must not be circular or self-created. |

## 10. Central Governance Rule

```text
A RECOVERY RESPONSIBILITY ASSIGNMENT IS LEGITIMATE ONLY WHEN
A CURRENT, BOUNDED, NON-CIRCULAR, PROVENANCE-VALID,
OPERATION-APPROPRIATE ASSIGNMENT AUTHORITY AUTHORIZES THE
ASSIGNMENT WITHIN ITS GOVERNED SCOPE.
```

The following are normative:

```text
ASSIGNMENT MECHANISM != ASSIGNMENT AUTHORITY
ASSIGNMENT RECORD != AUTHORITY SOURCE
TECHNICAL ASSIGNMENT SUCCESS != LEGITIMATE ASSIGNMENT
```

## 11. Fundamental Separations

The following separations are normative:

```text
RESPONSIBILITY != AUTHORITY
PARTICIPANT != AUTHORITY
ASSIGNMENT != AUTHORIZATION
ASSIGNMENT AUTHORITY != ASSIGNED RESPONSIBILITY
ASSIGNMENT AUTHORITY != PARTICIPANT IDENTITY
ASSIGNMENT AUTHORITY != ROOT
ASSIGNMENT AUTHORITY != RECOVERY AUTHORITY
ASSIGNMENT AUTHORITY != SUCCESSOR
ASSIGNMENT AUTHORITY != RESTORATION AUTHORITY
ASSIGNMENT AUTHORITY != AUTHENTICATION AUTHORITY
ASSIGNMENT AUTHORITY != INFRASTRUCTURE AUTHORITY
ASSIGNMENT AUTHORITY != CREDENTIAL POSSESSION
ASSIGNMENT AUTHORITY != ORGANIZATIONAL STATUS
ASSIGNMENT AUTHORITY != EVIDENCE CUSTODY
ASSIGNMENT AUTHORITY != EVIDENCE VERIFICATION
ASSIGNMENT AUTHORITY != MUTATION CAPABILITY
ASSIGNMENT AUTHORITY != AUDIT RESPONSIBILITY
ASSIGNMENT AUTHORITY != RECONCILIATION RESPONSIBILITY
ASSIGNMENT AUTHORITY != AI / LLM / MCP
ASSIGNMENT EXECUTION != ASSIGNMENT LEGITIMACY
ASSIGNMENT RECORD != AUTHORITY SOURCE
REQUEST != ASSIGNMENT AUTHORIZATION
QUALIFICATION != ASSIGNMENT AUTHORIZATION
ELIGIBILITY != ASSIGNMENT
MUTATION SUCCESS != LEGITIMATE AUTHORIZATION
```

## 12. Assignment Legitimacy

An assignment is legitimate only when the Assignment Authority is:

- authoritative for the responsibility class;
- accountable where the operation is authority-significant;
- current;
- scoped;
- operation-bound;
- target-bound where applicable;
- Business Entity-bound;
- environment-bound;
- governance-version-bound;
- lifecycle-valid;
- provenance-valid;
- non-revoked;
- non-suspended;
- non-expired;
- non-closed for the attempted use;
- independent where required by operation-specific SoD;
- not beneficiary-collapsed where that would create self-authorization;
- not common-mode compromised where independence is required; and
- auditable.

No concrete schema, persistence, participant, identity, or technology is
defined.

## 13. Terminating Authority Requirement

```text
ASSIGNMENT AUTHORITY MUST HAVE A FINITE GOVERNED PROVENANCE CHAIN.
```

That chain must ultimately derive legitimacy from already governed authority
concepts such as, where applicable:

- valid bounded Administrative Authority;
- operation-specific accountable authorization;
- independently governed terminating authority provenance;
- applicable TAB-derived authority for exceptional recovery contexts; or
- another separately governed non-circular basis.

Assignment Authority MUST NOT become its own terminating basis.

This artifact does not instantiate a TAB, select a concrete authority source,
create a new root, or grant production authority.

## 14. Assignment Authority Scope

Assignment Authority MUST be bounded where applicable by:

- responsibility class;
- operation;
- target;
- scope;
- Business Entity;
- environment;
- lifecycle;
- governance version;
- event; and
- affected authority.

The following inference is rejected:

```text
CAN ASSIGN ONE RESPONSIBILITY
    ->
CAN ASSIGN ALL RESPONSIBILITIES
```

The following inference is rejected:

```text
NON-PRODUCTION ASSIGNMENT AUTHORITY
    ->
PRODUCTION ASSIGNMENT AUTHORITY
```

## 15. Minimum Necessary Authority

Assignment Authority MUST be no broader than required for the governed
operation. Broad "can assign everything" semantics are rejected.

Minimum necessary authority must consider responsibility class, operation,
target, scope, Business Entity, environment, lifecycle, governance version,
event, authority direction, and affected authority.

## 16. Responsibility-Class Sensitivity

Responsibility classes do not have equal authority consequence. Assignment
governance MUST distinguish:

- authority-increasing;
- authority-enabling;
- authority-reducing;
- blocking;
- evidence/support;
- mutation;
- accountability; and
- lifecycle/termination.

Class sensitivity is defined in the matrices below. No concrete participant is
assigned.

## 17. Initial Assignment

The bootstrap rule is:

```text
THE FUTURE HOLDER OF A RESPONSIBILITY CANNOT CREATE THE
LEGITIMACY OF ITS OWN INITIAL ASSIGNMENT.
```

Initial assignment must derive from an independently legitimate,
non-circular governed basis. A holder-existing-yet paradox MUST NOT be solved
through self-authorization.

This artifact does not instantiate the initial assigner.

## 18. Ordinary Reassignment

Ordinary reassignment is distinct from exceptional recovery. It may use a
bounded ordinary administrative path when:

- existing governing authority remains legitimate;
- no relevant compromise exists;
- lifecycle transition is ordinary;
- provenance remains valid; and
- applicable SoD remains satisfied.

Ordinary reassignment MUST NOT automatically invoke Recovery Authority.

## 19. Assignment Authorization vs Mutation

```text
ASSIGNMENT AUTHORIZATION != ASSIGNMENT MUTATION.
```

A technical mutator may eventually execute an already-authorized assignment.
Technical capability does not confer assignment legitimacy.

Where required administrative authorization is not established:

```text
FAILED ADMINISTRATIVE AUTHORIZATION -> NO STATE CHANGE
```

No mutator is selected and no mutation is implemented.

## 20. Request Boundary

```text
REQUEST TO ASSIGN != AUTHORITY TO ASSIGN.
```

A requester may initiate consideration without gaining assignment
authorization. Self-request may be permissible where separately governed, but it
MUST NOT create authority.

## 21. Qualification / Eligibility Boundary

```text
QUALIFICATION != AUTHORIZATION
ELIGIBILITY != ASSIGNMENT
```

Determining that a participant is eligible to hold a responsibility does not
authorize assignment. A qualifier does not automatically become assigner.

## 22. Accountable Authorization Boundary

Authority-significant assignments may require accountable authorization
appropriate to the operation.

This artifact does not select the accountable authorizer, define participant
count, or create universal dual approval.

## 23. Self-Assignment

Authority-bearing self-assignment MUST fail closed where it would create
circular authority.

At minimum, governance MUST prevent:

- participant self-authorizing its own authority-bearing assignment;
- assigner granting itself broader Assignment Authority;
- Recovery Authority assigning itself future or permanent responsibility;
- root converting itself into standing assignment administrator;
- verifier self-assigning authorization responsibility;
- custodian self-assigning authority-source responsibility;
- mutator self-assigning authorizer responsibility; and
- compromised assigner selecting itself as replacement.

Harmless self-request or technical action is not universally prohibited where a
separately legitimate authorization already exists.

## 24. Beneficiary Conflict

Beneficiary-conflict analysis is operation-specific.

Where assignment directly benefits or preserves authority for the recipient,
governance MUST determine whether independent authorization is required based
on:

- authority consequence;
- self-certification risk;
- common-mode dependency;
- affected authority;
- successor implications;
- restoration implications; and
- closure implications.

This artifact does not create universal separation.

## 25. Operation-Specific SoD

This artifact preserves:

```text
MODEL G - HYBRID OPERATION-SPECIFIC SoD
```

Assignment-authority SoD depends on operation and risk. It does not imply:

- universal dual approval;
- universal maker/checker;
- universal two-person rule;
- universal quorum; or
- fixed participant count.

```text
RESPONSIBILITY INDEPENDENCE != PARTICIPANT COUNT.
```

## 26. Independence

Independence is provenance/control-dependency based.

Different people, identities, accounts, IAM roles, credentials, systems,
services, records, files, organizations, or technologies do not automatically
establish independence.

Independence MUST consider underlying authority and control dependencies.

## 27. Common-Mode Compromise

Common-mode analysis MUST cover:

- authority source;
- Administrative Authority;
- identity authority;
- credential control;
- infrastructure control;
- evidence source;
- Recovery Authority;
- predecessor authority;
- organizational control;
- mutation control; and
- verification control.

Apparent separation MUST NOT launder shared compromised provenance.

## 28. Assignment Authority Lifecycle

Assignment Authority lifecycle is conceptual and includes:

- proposed;
- established;
- current;
- suspended;
- expired;
- revoked;
- replaced;
- closed; and
- historical.

No runtime state machine is created.

```text
HISTORICAL ASSIGNMENT AUTHORITY != CURRENT ASSIGNMENT AUTHORITY.
```

## 29. Currentness

Assignment Authority MUST be currently valid for the operation.

The following fail closed:

- stale authority;
- revoked authority;
- suspended authority;
- expired authority;
- closed authority;
- compromised authority;
- unsupported governance version; and
- unverifiably current authority.

Historical legitimacy does not establish present authority.

## 30. Provenance

Assignment Authority provenance must conceptually include, where applicable:

- authority basis;
- authority source;
- accountable authorization reference;
- operation;
- responsibility class;
- target participant/reference;
- scope;
- Business Entity;
- environment;
- governance version;
- lifecycle;
- predecessor assignment;
- suspension;
- revocation;
- expiration;
- replacement;
- closure; and
- dependency provenance.

This artifact does not define schema or persistence.

## 31. Assignment Evidence

Assignment evidence may prove:

- authorization-at-time;
- assignment-at-time;
- scope;
- provenance;
- lifecycle;
- audit lineage; and
- replacement lineage.

But:

```text
ASSIGNMENT EVIDENCE != CURRENT AUTHORITY.
```

Stale, revoked, expired, malformed, unsupported, unverifiable, out-of-scope,
wrong-BE, wrong-environment, or closed assignment evidence cannot establish new
authority.

## 32. Negative Evidence

Applicable negative evidence includes:

- revocation;
- suspension;
- expiration;
- replacement;
- closure;
- invalidation; and
- compromise.

The following rules are normative:

```text
CURRENT REVOCATION DOMINATES STALE POSITIVE EVIDENCE.
"NO REVOCATION FOUND" != "REVOCATION SOURCE COULD NOT BE CHECKED."
```

If required negative evidence cannot be verified:

```text
NO NEW AUTHORITY.
```

## 33. Replay Prevention

Assignment evidence and Assignment Authority MUST be bound as applicable to:

- responsibility class;
- participant;
- operation;
- scope;
- Business Entity;
- environment;
- lifecycle;
- governance version;
- event;
- replacement lineage; and
- closure.

Historical or closed assignment evidence MUST NOT be replayed into a new
authority context.

This artifact does not design tokens or cryptography.

## 34. Suspension

Suspension is authority-reducing or blocking.

Authority to suspend may be narrower than authority to assign.

```text
SUSPENSION AUTHORITY != RESTORATION AUTHORITY.
```

Suspension MUST NOT create restoration authority.

## 35. Revocation

Revocation is authority-reducing.

Where operation-specific governance requires distinction:

```text
REVOCATION AUTHORITY != ASSIGNMENT AUTHORITY
```

Always preserve:

```text
REVOCATION AUTHORITY != RESTORATION AUTHORITY.
```

Revocation MUST NOT silently create authority to reassign or restore.

## 36. Replacement

Replacement semantics apply to:

- ordinary lifecycle replacement;
- unavailability;
- revocation;
- compromise;
- departure;
- beneficiary conflict; and
- common-mode compromise.

```text
REPLACEMENT != SELF-APPOINTMENT.
REPLACEMENT != SUCCESSOR AUTHORITY ESTABLISHMENT.
```

A compromised Assignment Authority MUST NOT be the sole basis for its own
replacement.

## 37. Restoration / Reactivation

Restoration/reactivation is authority-increasing.

```text
ASSIGNMENT != RESTORATION
REASSIGNMENT != RESTORATION
REVOCATION != RESTORATION
REDUCTION != RESTORATION
```

Assignment Authority alone MUST NOT restore revoked, suspended, expired,
compromised, invalidated, or closed authority.

Restoration remains separately governed and NOT AUTHORIZED here.

## 38. Recovery Authority Containment

```text
ASSIGNMENT AUTHORITY != RECOVERY AUTHORITY.
```

Recovery Authority MUST NOT automatically gain power to:

- assign future Recovery Authority;
- perpetuate itself;
- assign itself permanent responsibilities;
- establish successor legitimacy;
- restore itself;
- redefine Assignment Authority;
- suppress revocation;
- suppress closure; or
- create future Recovery TAB legitimacy.

## 39. Root Containment

```text
ASSIGNMENT AUTHORITY != ROOT.
```

Root remains bounded and non-standing.

The following is rejected:

```text
ROOT = CAN ASSIGN EVERYTHING
```

Standing root assignment administration is not created.

## 40. Successor Boundary

```text
RESPONSIBILITY REPLACEMENT != SUCCESSOR AUTHORITY ESTABLISHMENT.
```

A predecessor MUST NOT be the sole legitimizer of a successor where independent
legitimacy is required.

Assignment Authority MUST NOT become a hidden succession mechanism.

## 41. Compromised Assignment Authority

If Assignment Authority itself is compromised, it MUST NOT:

- restore itself;
- reauthorize itself;
- select itself as replacement;
- suppress revocation;
- suppress negative evidence;
- establish successor legitimacy;
- invoke hidden root;
- invoke automatic break-glass;
- use stale authority evidence; or
- broaden its own scope.

Applicable bounded recovery governance governs exceptional recovery. This
artifact does not perform recovery.

## 42. Unavailable Assignment Authority

```text
UNAVAILABLE != COMPROMISED.
```

Unavailability alone creates no fallback authority. Ordinary governed
replacement or succession is preferred where legitimate.

No convenience recovery is created.

## 43. Assignment Authority Recovery

```text
RECOVERY OF ASSIGNMENT AUTHORITY != STANDING RECOVERY AUTHORITY.
```

Recovery must comply with existing bounded Recovery TAB and Recovery Authority
governance.

No recovery authority is instantiated here.

## 44. Assignment Authority Replacement

Replacement of Assignment Authority requires independent legitimacy appropriate
to the operation.

The following circular rule is rejected:

```text
CURRENT ASSIGNMENT AUTHORITY
    ->
SOLELY AUTHORIZES ITS OWN REPLACEMENT
    ->
REPLACEMENT BECOMES LEGITIMATE
```

This especially fails closed when compromise affects current Assignment
Authority.

## 45. Assignment Authority Closure

Event-specific Assignment Authority MUST terminate when its governed event
closes.

Closure MUST prevent residual or replayable assignment authority.

Historical evidence may remain for audit and lineage. Historical evidence is
not exercisable authority.

## 46. Authority Direction

Assignment governance MUST distinguish direction:

Authority-increasing or enabling:

- initial assignment;
- authority-significant assignment;
- restoration/reactivation; and
- successor establishment where applicable.

Authority-reducing or blocking:

- suspension;
- revocation;
- emergency reduction; and
- closure.

Mixed:

- reassignment; and
- replacement.

Identical authorization requirements MUST NOT be assumed in both directions.

```text
REDUCTION AUTHORITY != INCREASE AUTHORITY.
```

## 47. Fail-Closed Semantics

The following outcomes are normative:

```text
MISSING ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
INVALID ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
STALE ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
REVOKED ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
SUSPENDED ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
EXPIRED ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
CLOSED ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
UNVERIFIABLY CURRENT ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
OUT-OF-SCOPE ASSIGNMENT AUTHORITY -> NO ASSIGNMENT
WRONG BUSINESS ENTITY -> NO ASSIGNMENT
WRONG ENVIRONMENT -> NO ASSIGNMENT
UNSUPPORTED GOVERNANCE VERSION -> NO ASSIGNMENT
REQUIRED SoD NOT ESTABLISHED -> NO ASSIGNMENT
REQUIRED INDEPENDENCE NOT ESTABLISHED -> NO ASSIGNMENT
CONFLICTING AUTHORITY EVIDENCE -> NO ASSIGNMENT
REQUIRED NEGATIVE EVIDENCE UNAVAILABLE -> NO ASSIGNMENT
FAILED ADMINISTRATIVE AUTHORIZATION -> NO STATE CHANGE
COMPROMISE AFFECTS REQUIRED BASIS -> NO NEW AUTHORITY
```

No convenience fallback is permitted.

## 48. Trusted Authorization Domain Boundaries

Recovery Responsibility Assignment Authority MUST NOT become an alternate
authority source for:

- Principal Mapping;
- Business Entity;
- Membership;
- Entitlement;
- Resource Identity;
- Resource Classification;
- Resource Binding;
- Requested Action; or
- Applicability.

The following separations are preserved:

```text
Membership != Entitlement
Entitlement != ALLOW
Resource Identity != Entitlement
Requested Action / Applicability cannot create authority
```

## 49. Producer / Consumer Boundaries

Existing platform boundaries are preserved:

- Assessment Service remains the deterministic business-truth producer.
- Executive Intelligence Platform remains governed consumer / derivation.
- Website / Client Engagement Portal remains presentation consumer.
- AI Knowledge Assistant remains explanation consumer.
- Trusted Authorization remains the deterministic authorization boundary.

This artifact does not alter those boundaries.

## 50. Authentication Boundary

```text
AUTHENTICATION != AUTHORIZATION
AUTHENTICATED IDENTITY != ASSIGNMENT AUTHORITY
```

No identity technology is selected.

## 51. Organizational Status Boundary

None of the following creates Assignment Authority by status alone:

- founder;
- owner;
- CEO;
- executive;
- board member;
- employee;
- contractor;
- security team;
- administrator;
- developer; or
- auditor.

None is assigned by this artifact.

## 52. Infrastructure Boundary

Infrastructure control cannot substitute for governed business legitimacy:

```text
AWS ADMIN != ASSIGNMENT AUTHORITY
IAM ADMIN != ASSIGNMENT AUTHORITY
GITHUB ADMIN != ASSIGNMENT AUTHORITY
DATABASE ADMIN != ASSIGNMENT AUTHORITY
DEPLOYMENT AUTHORITY != ASSIGNMENT AUTHORITY
```

## 53. Credential Boundary

```text
CREDENTIAL POSSESSION != ASSIGNMENT AUTHORITY.
```

This artifact does not select credentials.

## 54. Human / Machine Boundary

A future realization may contain accountable human authorization, deterministic
machine validation, deterministic machine mutation, or bounded combinations.

```text
MACHINE EXECUTION != ASSIGNMENT AUTHORITY.
```

Human/machine allocation remains unresolved.

## 55. AI / LLM / MCP Boundary

AI/LLM/MCP cannot independently:

- authorize assignment;
- assign responsibilities;
- create Assignment Authority;
- override revocation;
- waive SoD;
- restore authority;
- select legitimate replacement;
- establish successor; or
- certify itself as authoritative.

AI may only provide non-authoritative assistance if separately governed.

## 56. Business Entity Isolation

```text
BE A ASSIGNMENT AUTHORITY != BE B ASSIGNMENT AUTHORITY.
```

No universal cross-BE Assignment Authority is created.

## 57. Environment Isolation

```text
NON-PRODUCTION ASSIGNMENT AUTHORITY != PRODUCTION ASSIGNMENT AUTHORITY.
```

This artifact grants no production authority.

## 58. Participant Count

Participant count remains:

```text
UNRESOLVED / NOT SELECTED.
```

This artifact does not select one-person, two-person, 2-of-3, majority,
unanimous, N-of-M, or any other count model.

## 59. Quorum

Quorum remains:

```text
UNRESOLVED / NOT SELECTED.
```

This artifact does not select quorum.

## 60. Dual Approval

```text
NO UNIVERSAL DUAL APPROVAL.
```

Operation-specific independence does not imply universal dual approval.

## 61. Maker / Checker

```text
NO UNIVERSAL MAKER / CHECKER.
```

Authorization/mutation separation may be required where operation risk
justifies it, but it is not universal.

## 62. Break-Glass

Break-glass remains:

```text
NOT SELECTED.
```

This artifact does not create unrestricted emergency Assignment Authority.

## 63. Minimum Disclosure

Assignment Authority evidence SHOULD expose only what is required to establish:

- authority basis;
- assignment legitimacy;
- scope;
- lifecycle;
- currentness;
- provenance;
- SoD;
- revocation; and
- auditability.

Unnecessary personal identity disclosure is not required. Privacy technology is
not defined.

## 64. Threat Model

| Threat | Targeted invariant | Affected operation | Governance control | Fail-closed result | Unresolved dependency |
| --- | --- | --- | --- | --- | --- |
| Participant self-assignment. | Participant cannot create authority through self-assignment. | Initial assignment. | Independent assignment basis. | No assignment. | Concrete assignment authority. |
| Assigner self-elevation. | Assignment Authority cannot create its own terminating basis. | Scope expansion. | Scope-bound authority and beneficiary conflict review. | No broader authority. | Assignment authority source. |
| Standing universal assigner. | No hidden super-admin. | All assignments. | Minimum necessary authority. | No universal assigner. | Concrete model realization. |
| Hidden super-admin. | No hidden super-admin. | Assignment authority. | Bounded class/scope/event limits. | No assignment. | Assignment ownership. |
| Standing root assignment administrator. | Root cannot become standing Assignment Authority. | Root/admin assignment. | Root containment. | No standing root assigner. | Root lifecycle governance. |
| Recovery Authority self-perpetuation. | Recovery Authority cannot perpetuate itself. | Future recovery assignment. | RA containment and closure. | No future RA authority. | Recovery authority lifecycle. |
| Successor legitimacy laundering. | Predecessor cannot create successor merely by assignment. | Successor establishment. | Independent successor provenance. | No successor authority. | Successor governance. |
| Restoration laundering. | Assignment != restoration. | Restoration/reactivation. | Separate restoration authority. | No restoration. | Restoration ownership. |
| Reassignment laundering revocation. | Reassignment cannot launder revocation. | Reassignment. | Negative evidence verification. | No reassignment. | Revocation authority. |
| Replacement laundering compromise. | Replacement cannot launder compromise. | Replacement. | Compromise-aware independent basis. | No replacement. | Replacement authority. |
| Revocation suppression. | Current revocation dominates stale positive evidence. | Assignment/reassignment. | Negative evidence completeness. | No assignment. | Revocation realization. |
| Suspension suppression. | Suspended authority cannot assign. | Assignment. | Suspension check. | No assignment. | Suspension authority. |
| Expiration suppression. | Expired authority cannot assign. | Assignment. | Expiration check. | No assignment. | Lifecycle realization. |
| Negative-evidence suppression. | Required negative evidence unavailable != verified not revoked. | Assignment. | Required negative evidence verification. | No assignment. | Negative-evidence source. |
| Historical assignment replay. | Historical evidence != current authority. | Replay. | Currentness and closure binding. | No assignment. | Assignment evidence realization. |
| Stale authority replay. | Stale Assignment Authority cannot assign. | Assignment. | Currentness verification. | No assignment. | Currentness realization. |
| Stale governance version. | Unsupported version cannot assign. | Assignment. | Version compatibility. | No assignment. | Version governance. |
| Assignment record treated as authority source. | Assignment record != authority source. | Verification. | Source/record separation. | No authority. | Source realization. |
| Mutator treated as authorizer. | Assignment authorization != mutation. | Mutation. | Authorization before mutation. | No state change. | Mutation ownership. |
| Verifier treated as authorizer. | Assignment Authority != verification. | Verification. | Verification non-authority. | No assignment. | Verifier assignment. |
| Custodian treated as authorizer. | Assignment Authority != custody. | Custody. | Custody non-authority. | No assignment. | Custody assignment. |
| Requester treated as authorizer. | Request != assignment authorization. | Request. | Request boundary. | No assignment. | Request workflow. |
| Qualifier treated as authorizer. | Qualification != assignment authorization. | Qualification. | Eligibility boundary. | No assignment. | Qualification model. |
| Auditor/reconciler treated as authorizer. | Assignment Authority != audit/reconciliation. | Audit/reconciliation. | Audit/recon non-authority. | No assignment. | Audit ownership. |
| Compromised assigner self-replacement. | Compromised authority cannot self-replace. | Replacement. | Independent replacement basis. | No replacement. | Replacement authority. |
| Unavailable assigner causing hidden fallback. | Unavailability creates no fallback authority. | Assignment. | Ordinary path or bounded recovery only. | No fallback. | Recovery path. |
| Founder/owner/CEO status authority. | Status != Assignment Authority. | Assignment. | Organizational non-authority. | No assignment. | Participant assignment. |
| AWS/IAM/GitHub control authority. | Infrastructure != Assignment Authority. | Assignment. | Infrastructure boundary. | No assignment. | Technology governance. |
| Credential-possession authority. | Credential possession != Assignment Authority. | Assignment. | Credential boundary. | No assignment. | Credential governance. |
| Machine-execution authority. | Machine execution != Assignment Authority. | Mutation. | Execution after authorization. | No state change. | Human/machine allocation. |
| AI/LLM/MCP authority. | AI/LLM/MCP != Assignment Authority. | Any. | Non-authoritative assistance only. | No assignment. | AI use governance if any. |
| Cross-BE assignment. | BE A != BE B Assignment Authority. | Assignment. | BE binding. | No assignment. | BE assignment governance. |
| Non-prod-to-prod assignment. | Non-production != production Assignment Authority. | Assignment. | Environment binding. | No production assignment. | Production governance. |
| Common-mode assigner/recipient compromise. | Different participants != independent provenance. | Assignment. | Dependency analysis. | No independence. | Dependency provenance. |
| Fake independence through identities. | Different identities != independence. | SoD. | Identity dependency analysis. | No independence. | Identity realization. |
| Fake independence through accounts. | Different accounts != independence. | SoD. | Authority/control dependency analysis. | No independence. | Technology later. |
| Fake independence through credentials. | Different credentials != independence. | SoD. | Credential dependency analysis. | No independence. | Credential governance. |
| Universal dual approval mistaken for legitimacy. | No universal dual approval. | Authorization. | Operation-specific SoD. | No authority from count. | Participant count. |
| Quorum mistaken for legitimacy. | No universal quorum. | Authorization. | Quorum non-selection. | No authority from quorum. | Quorum if ever required. |
| Participant count mistaken for independence. | Responsibility independence != participant count. | SoD. | Provenance-based independence. | No independence. | Participant count. |
| Assignment chain circularity. | Assignment Authority must terminate non-circularly. | Assignment basis. | Finite terminating provenance. | No assignment. | Assignment source. |
| Assignment chain non-termination. | Assignment Authority must terminate non-circularly. | Assignment basis. | Finite termination. | No assignment. | Terminating basis. |
| Closure omission. | Closed authority cannot assign. | Event-specific assignment. | Closure evidence and non-replay. | No clean closure. | Closure ownership. |
| Reduction capability becoming restoration capability. | Reduction authority != increase authority. | Suspension/revocation. | Direction separation. | No restoration. | Restoration ownership. |
| Compromised authority using stale positive evidence. | Current revocation dominates stale positive evidence. | Assignment. | Current negative evidence and compromise review. | No assignment. | Compromise handling. |
| Required revocation source unavailable but treated as not revoked. | Required negative evidence unavailable != verified not revoked. | Assignment verification. | Fail-closed negative evidence check. | No assignment. | Revocation realization. |

## 65. Required Matrices

### 65.1 Assignment Authority Model Definition Matrix

| Model | Non-circularity | Fail-closed fit | Operation-specific SoD fit | Scope bounding | Lifecycle fit | Self-assignment resistance | Common-mode resistance | Standing-authority risk | Participant-count assumption | Quorum assumption | Governance fit | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Model A - Standing Central Assignment Authority | Weak. | Weak. | Weak. | Weak. | Weak. | Weak. | Weak. | High. | None. | None. | Conflicts with governance. | Rejected. |
| Model B - Responsibility-Class-Specific Assignment Authorities | Medium. | Medium. | Medium. | Strong by class. | Medium. | Medium. | Medium. | Low/medium. | None. | None. | Useful component. | Included in Model F. |
| Model C - Universal Dual-Control Assignment | Medium. | Medium. | Weak. | Medium. | Medium. | Medium. | Weak under common-mode. | Medium. | Yes. | Quorum-like. | Conflicts with no universal count. | Rejected. |
| Model D - Administrative Authority Derivation | Medium. | Strong if bounded. | Medium. | Medium. | Medium. | Medium. | Medium. | Medium/high if broad. | None. | None. | Useful component. | Included in Model F. |
| Model E - TAB-Derived Operation-Specific Assignment Authority | Strong for recovery. | Strong. | Strong. | Strong. | Strong. | Strong. | Strong. | Low. | None. | None. | Useful for exceptional cases. | Included in Model F. |
| Model F - Hybrid Bounded Assignment Authority | Strong. | Strong. | Strong. | Strong. | Strong. | Strong. | Strong. | Low. | None. | None. | Best fit. | SELECTED. |
| Model G - Underdetermined | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Not needed. | Not selected. |

### 65.2 Responsibility Class / Assignment Sensitivity Matrix

| Responsibility class | Assignment consequence | Authority direction | Beneficiary risk | Self-assignment risk | Independence sensitivity | Assignment-authority sensitivity | Unresolved |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Request | Initiates process. | Neutral. | Medium. | Low/medium. | Conditional. | Low/medium. | Concrete participant. |
| Qualification | Establishes recovery condition. | Authority-enabling. | High. | High. | High. | High. | Qualification responsibility. |
| Accountable Authorization | Authorizes bounded recovery. | Authority-increasing. | Very high. | Very high. | Very high. | Very high. | Accountable authorizer. |
| Recovery TAB Establishment | Establishes terminating legitimacy. | Authority-enabling. | Very high. | Very high. | Very high. | Very high. | TAB establishment responsibility. |
| Recovery TAB Activation | Makes bounded authority exercisable. | Authority-increasing. | Very high. | Very high. | Very high. | Very high. | Activation responsibility. |
| Evidence Production | Produces authority evidence. | Evidence/support or mixed. | Medium/high. | Medium/high. | Function-specific. | Medium/high. | Producer ownership. |
| Custody | Preserves evidence. | Evidence/support. | Medium. | Medium. | Medium/high. | Medium. | Custody assignment. |
| Verification | Evaluates evidence. | Evidence/support. | High. | High. | High. | High. | Verifier assignment. |
| Negative Evidence / Revocation | Blocks authority. | Authority-reducing/blocking. | High. | High. | Very high. | High. | Revocation authority. |
| Lifecycle | Governs currentness. | Mixed. | High. | High. | High. | High. | Lifecycle ownership. |
| Provenance / Dependency | Establishes lineage. | Evidence/support. | High. | High. | Very high. | High. | Provenance ownership. |
| Mutation | Records/applies state. | Mutation/mixed. | High. | High. | High. | High. | Mutation ownership. |
| Audit | Accountability. | Accountability. | Medium/high. | Medium/high. | Conditional/high. | Medium. | Audit ownership. |
| Reconciliation | Resolves obligations. | Blocking/accountability. | Medium/high. | High. | Conditional/high. | Medium/high. | Reconciliation ownership. |
| Closure | Terminates event. | Lifecycle/termination. | High. | High. | High. | High. | Closure ownership. |
| Successor Establishment | Future authority. | Authority-increasing. | Very high. | Very high. | Very high. | Very high. | Successor governance. |
| Restoration / Reactivation | Restores authority. | Authority-increasing. | Very high. | Very high. | Very high. | Very high. | Restoration ownership. |
| Emergency Authority Reduction | Contains risk. | Authority-reducing. | Medium. | Medium. | Medium/high. | Medium/high. | Emergency reduction authority. |

### 65.3 Assignment / Suspension / Revocation / Replacement Matrix

| Operation | Authority direction | Same authority permitted conceptually? | Independence sensitivity | Lifecycle effect | Fail-closed result | Unresolved |
| --- | --- | --- | --- | --- | --- | --- |
| Initial assignment | Increase/enabling. | Conditional only with independent basis. | High. | Establishes current responsibility. | No assignment. | Initial authority source. |
| Ordinary reassignment | Mixed. | Conditional. | Medium/high. | Replaces current holder. | No reassignment. | Reassignment ownership. |
| Suspension | Reducing/blocking. | May be narrower. | Medium/high. | Suspends current use. | No restoration. | Suspension authority. |
| Revocation | Reducing. | Distinct where required. | High. | Ends current use. | No assignment from revoked authority. | Revocation authority. |
| Expiration | Reducing/time-bound. | Lifecycle governed. | Medium. | Converts to historical. | No assignment. | Expiration handling. |
| Replacement | Mixed. | Not self-appointment. | High. | Establishes replacement if legitimate. | No replacement. | Replacement authority. |
| Restoration/reactivation | Increasing. | Assignment alone insufficient. | Very high. | Restores usability only if separately governed. | No restoration. | Restoration ownership. |
| Closure | Terminating. | Conditional by event. | High. | Ends event-specific authority. | No clean closure. | Closure ownership. |

### 65.4 Assignment Authority / Responsibility Relationship Matrix

| Responsibility | May request assignment? | May authorize assignment by role? | May execute mutation? | May verify? | May assign itself? | Authority source by role? | Required independence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Request | Yes. | No. | No. | No by role. | No authority-bearing self-assignment. | No. | Conditional. |
| Qualification | Maybe. | No. | No. | Qualification only. | No where self-recovery risk exists. | No. | High for recovery. |
| Accountable Authorization | Maybe. | Only if separately governed. | No by role. | No by role. | No beneficiary sole basis. | Not by label. | Very high. |
| TAB Establishment | Maybe. | No by role. | No. | Establishment only. | No. | No. | Very high. |
| TAB Activation | Maybe. | No missing authorization. | Conditional if separately governed. | No by role. | No. | No. | Very high. |
| Evidence Production | Maybe. | No. | Conditional. | Conditional. | No where circular. | Not by production alone. | Function-specific. |
| Custody | Maybe. | No. | No authority mutation. | Conditional. | No. | No. | Medium/high. |
| Verification | Maybe. | No. | No. | Yes. | No self-replacement. | No. | High where consequential. |
| Negative Evidence | Maybe. | No. | Conditional if authorized. | Conditional. | No suppression. | Not by role. | Very high. |
| Lifecycle | Maybe. | No by role. | Conditional if authorized. | Conditional. | No restoration. | Not by role. | High. |
| Provenance | Maybe. | No by role. | Conditional if authorized. | Conditional. | No self-provenance. | Not by role. | Very high. |
| Mutation | Maybe. | No. | Yes after authorization. | Conditional. | No. | No. | High. |
| Audit | Maybe. | No. | No authority mutation. | Audit only. | No. | No. | Conditional/high. |
| Reconciliation | Maybe. | No. | No restoration. | Reconciliation only. | No. | No. | Conditional/high. |
| Closure | Maybe. | No future authority. | Conditional if authorized. | Closure only. | No where residual risk. | No. | High. |
| Successor | Maybe. | No by role. | Conditional if authorized. | Conditional. | No sole basis. | No. | Very high. |
| Restoration | Maybe. | Only if separately governed. | Conditional if authorized. | Conditional. | No. | No. | Very high. |
| Emergency Reduction | Maybe. | Only if separately governed. | Conditional if authorized. | Conditional. | No restoration. | No. | Medium/high. |

### 65.5 Assignment Authorization / Mutation Separation Matrix

| Concept | Governance function | May create assignment legitimacy? | May execute state change? | Boundary |
| --- | --- | --- | --- | --- |
| Assignment request | Initiates consideration. | No. | No. | Request != authorization. |
| Eligibility/qualification | Determines fitness/condition. | No by itself. | No. | Eligibility != assignment. |
| Assignment authorization | Determines permitted assignment. | Yes within governed scope. | No by itself. | Authorization != mutation. |
| Assignment mutation | Records/applies authorized assignment. | No. | Yes only after authorization. | Mutation success != legitimacy. |
| Assignment verification | Evaluates evidence. | No. | No. | Verification != authorization. |
| Assignment audit | Records accountability. | No. | No authority mutation. | Audit != authority. |

### 65.6 Self-Action / Circularity Matrix

| Self-action | Generally allowed? | Authority consequence | Circularity risk | Required independent basis | Fail-closed result |
| --- | --- | --- | --- | --- | --- |
| Self-request | Conditional. | None alone. | Low/medium. | Later assignment authorization. | No assignment. |
| Self-qualification | Conditional/no where self-recovery. | Authority-enabling. | High. | Independent qualification. | No qualification. |
| Self-assignment | No where authority-bearing. | Increase/enabling. | Very high. | Independent Assignment Authority. | No assignment. |
| Self-verification | Conditional/no where consequential. | Evidence reliance. | High. | Independent verification. | No verified basis. |
| Self-mutation | No missing authorization. | State change. | High. | Prior assignment authorization. | No state change. |
| Self-suspension | Conditional. | Reduction/blocking. | Medium. | Governed reduction basis. | No restoration. |
| Self-revocation | Conditional. | Reduction. | Medium. | Governed revocation basis. | No restoration. |
| Self-replacement | No where compromised or authority-bearing. | Mixed/increase. | Very high. | Independent replacement basis. | No replacement. |
| Self-restoration | No. | Increase. | Very high. | Independent restoration authority. | No restoration. |
| Self-succession | No sole basis. | Future authority. | Very high. | Independent successor basis. | No successor authority. |
| Self-closure | Conditional/no with residual privilege. | Termination. | High. | Closure legitimacy and residual privilege check. | No clean closure. |

### 65.7 Assignment Authority Lifecycle Matrix

| State | May assign? | Currentness requirement | Evidence value | Replacement implication | Fail-closed result |
| --- | --- | --- | --- | --- | --- |
| Proposed | No. | Proposal only. | Draft lineage. | None. | No assignment. |
| Established | Only if effective/current. | Establishment provenance. | Establishment record. | None by itself. | No if incomplete. |
| Current | Yes within scope. | Current verified basis. | Current authority evidence. | Replacement not implied. | No outside scope. |
| Suspended | No where suspension applies. | Suspension verified. | Suspension evidence. | May require replacement. | No assignment. |
| Expired | No. | Expiration verified. | Historical evidence. | May require replacement. | No assignment. |
| Revoked | No. | Revocation verified. | Revocation evidence. | Replacement separately governed. | No assignment. |
| Replaced | Not by default. | Replacement effective status. | Replacement lineage. | Replacement authority required. | No assignment. |
| Closed | No for event-specific authority. | Closure verified. | Closure evidence. | New basis required. | No assignment. |
| Historical | No. | Historical context. | Audit/lineage. | None. | No current authority. |

### 65.8 Assignment Authority Currentness Matrix

| Condition | Current authority? | Required handling |
| --- | --- | --- |
| Current and in scope | Potentially yes if all other requirements pass. | Verify provenance, SoD, negative evidence, and scope. |
| Stale | No. | Treat as historical. |
| Revoked | No. | Block assignment. |
| Suspended | No where suspension applies. | Block assignment. |
| Expired | No. | Historical only. |
| Closed | No for event-specific use. | Block replay. |
| Compromised | No for affected basis. | Revalidate or recover through governed path. |
| Unsupported version | No. | No assignment. |
| Unverifiably current | No. | No assignment. |

### 65.9 Assignment Authority Provenance Matrix

| Provenance element | Required conceptually? | Currentness requirement | Independence relevance | Failure consequence |
| --- | --- | --- | --- | --- |
| Authority basis | Yes. | Current. | High. | No assignment. |
| Authority source | Yes where applicable. | Current/valid. | High. | No assignment. |
| Accountable authorization reference | Where authority-significant. | Current/event-bound. | High. | No assignment. |
| Operation | Yes. | Current operation. | Medium/high. | No operation authority. |
| Responsibility class | Yes. | Current class. | High. | No class authority. |
| Target participant/reference | Yes where applicable. | Current. | Medium/high. | No assignment. |
| Scope | Yes. | Current scope. | High. | No out-of-scope assignment. |
| Business Entity | Yes. | Current BE. | High. | No cross-BE assignment. |
| Environment | Yes. | Current environment. | High. | No production from non-production. |
| Governance version | Yes. | Compatible. | High. | No assignment. |
| Lifecycle | Yes. | Current. | High. | No assignment. |
| Predecessor assignment | Where applicable. | Valid lineage. | High. | No replacement/succession. |
| Suspension | Where applicable. | Current. | High. | No assignment if suspended. |
| Revocation | Yes. | Current. | Very high. | No assignment if revoked or unverifiable. |
| Expiration | Yes where bounded. | Current. | High. | No assignment if expired. |
| Replacement | Where applicable. | Current. | High. | No replacement. |
| Closure | Where applicable. | Current. | High. | No replay. |
| Dependency provenance | Yes where independence required. | Current enough. | Very high. | Independence not established. |

### 65.10 Beneficiary-Conflict Matrix

| Context | May benefit? | May assign itself? | May authorize own assignment? | Independence sensitivity | Fail-closed result |
| --- | --- | --- | --- | --- | --- |
| Recipient | Yes. | No sole basis. | No sole basis. | High. | No assignment. |
| Requester | Yes. | Conditional/no. | No by request. | Medium/high. | No assignment. |
| Qualifier | Sometimes. | No sole basis where risk exists. | No by qualification. | High. | No assignment. |
| Authorizer | Sometimes. | Only if separately governed and non-circular. | Only within scope. | High. | No assignment. |
| Recovery Authority | Yes. | No future/permanent basis. | No sole basis. | Very high. | No future RA authority. |
| Predecessor | Yes. | No sole successor basis. | No sole successor legitimacy. | Very high. | No successor. |
| Successor candidate | Yes. | No sole basis. | No sole basis. | Very high. | No successor. |
| Mutator | Yes. | No. | No by mutation. | High. | No state change. |
| Verifier | Indirect. | No self-replacement. | No. | High. | No assignment. |
| Custodian | Indirect. | No source assignment. | No. | Medium/high. | No assignment. |
| Auditor | Indirect. | No authority-bearing assignment by audit. | No. | Medium. | No assignment. |
| Closure responsibility | Yes if residual privilege. | No sole basis where risk exists. | No. | High. | No clean closure. |

### 65.11 Operation-Specific SoD Matrix

| Operation | Authority consequence | Independence sensitivity | Beneficiary conflict | Stronger SoD required? | Universal participant count? | Quorum selected? |
| --- | --- | --- | --- | --- | --- | --- |
| Initial assignment | Authority-enabling. | High. | High. | Yes where authority-significant. | No. | No. |
| Ordinary reassignment | Mixed. | Medium/high. | Medium. | Conditional. | No. | No. |
| Recovery qualification assignment | Authority-enabling. | High. | High. | Yes. | No. | No. |
| Accountable authorization assignment | Authority-increasing. | Very high. | Very high. | Yes. | No. | No. |
| TAB establishment assignment | Authority-enabling. | Very high. | High. | Yes. | No. | No. |
| Recovery Authority activation assignment | Authority-increasing. | Very high. | Very high. | Yes. | No. | No. |
| Mutation assignment | State-change enabling. | High. | High. | Yes where authority-increasing. | No. | No. |
| Custody/verification assignment | Evidence reliance. | Medium/high. | Medium/high. | Conditional/high. | No. | No. |
| Audit/reconciliation assignment | Accountability. | Medium/high. | Medium/high. | Conditional. | No. | No. |
| Closure assignment | Termination/non-replay. | High. | High. | Conditional/high. | No. | No. |
| Successor assignment | Future authority. | Very high. | Very high. | Yes. | No. | No. |
| Restoration assignment | Authority-increasing. | Very high. | Very high. | Yes. | No. | No. |

### 65.12 Common-Mode Dependency Matrix

| Dependency | Apparent separation | Actual independence criterion | Compromise consequence | Required control | Unresolved |
| --- | --- | --- | --- | --- | --- |
| Authority source | Different assignment records. | Separate legitimate source/provenance where required. | Assignment laundering. | Source dependency mapping. | Authority-source realization. |
| Administrative Authority | Different administrators. | No shared compromised admin authority where required. | Coordinated unauthorized assignment. | Admin provenance. | Assignment authority source. |
| Identity authority | Different identities. | Independent identity dependency where required. | False attribution. | Identity provenance. | Identity realization. |
| Credential control | Different credentials. | Independent credential issuer/control where required. | Credential capture. | Credential non-authority. | Credential governance. |
| Infrastructure control | Different systems/accounts. | No common control plane where required. | Infrastructure takeover. | Infrastructure non-authority. | Technology later. |
| Evidence source | Different evidence records. | Independent evidence source where required. | Evidence laundering. | Evidence provenance. | Evidence realization. |
| Recovery Authority | Separate event actor. | Not sole future assignment basis. | Standing recovery authority. | RA containment. | Recovery lifecycle. |
| Predecessor authority | Prior lineage. | Not sole successor legitimacy where required. | Self-perpetuation. | Successor independence. | Successor governance. |
| Organizational control | Different titles. | No shared command capture where required. | Role-label laundering. | Organizational non-authority. | Participant categories. |
| Mutation control | Different mutators. | Mutation independent from authorization where required. | Self-certified mutation. | Mutation/authorization separation. | Mutation ownership. |
| Verification control | Different verifiers. | Verification not same compromised dependency where required. | False validation. | Verification independence. | Verifier assignment. |

### 65.13 Authority-Direction Matrix

| Operation | Increase/reduction/neutral | Authorization sensitivity | SoD sensitivity | Same-authority implication | Restoration risk |
| --- | --- | --- | --- | --- | --- |
| Initial assignment | Increase/enabling. | High. | High. | Not self-created. | Medium. |
| Reassignment | Mixed. | Medium/high. | Medium/high. | Conditional. | Medium. |
| Suspension | Reduction/blocking. | Medium. | Medium. | May be narrower. | Must not restore. |
| Revocation | Reduction. | High. | High. | Does not imply assignment. | Must not restore. |
| Emergency reduction | Reduction. | Medium/high. | Medium/high. | Separate from restoration. | Must not restore. |
| Replacement | Mixed. | High. | High. | Not self-appointment. | Compromise laundering risk. |
| Restoration | Increase. | Very high. | Very high. | Assignment alone insufficient. | Direct. |
| Closure | Termination. | High. | High. | No residual privilege. | Prevent replay. |

### 65.14 Assignment Evidence / Authority Matrix

| Evidence type | May prove | May create current authority alone? | Required check |
| --- | --- | --- | --- |
| Assignment authorization evidence | Authorization-at-time. | No. | Currentness, scope, revocation, provenance. |
| Assignment record | Assignment-at-time. | No. | Source and lifecycle. |
| Assignment mutation evidence | State was changed. | No. | Prior authorization. |
| Assignment verification evidence | Evidence was evaluated. | No. | Verification non-authority. |
| Assignment audit evidence | Accountability. | No. | Audit non-authority. |
| Historical assignment evidence | Lineage. | No. | Historical/current separation. |
| Negative assignment evidence | Revocation/suspension/expiration/closure. | Blocks where current. | Completeness and currentness. |

### 65.15 Negative Evidence Matrix

| Negative evidence | Effect | Suppression risk | Required handling | Fail-closed result |
| --- | --- | --- | --- | --- |
| Revocation | Blocks authority. | High. | Verify current revocation. | No assignment. |
| Suspension | Temporarily blocks. | Medium/high. | Verify suspension scope. | No assignment where applicable. |
| Expiration | Ends current use. | Medium. | Verify validity boundary. | No assignment. |
| Replacement | Prior holder no longer current. | Medium/high. | Verify replacement lineage. | No assignment from replaced basis. |
| Closure | Ends event-specific authority. | High. | Verify closure/non-replay. | No replay. |
| Invalidation | Blocks legitimacy. | High. | Verify invalidation cause/scope. | No assignment. |
| Compromise | Blocks affected basis. | High. | Cause/scope/provenance analysis. | No new authority from affected basis. |
| Negative source unavailable | Unknown status. | High. | Must not treat as clear. | No assignment. |

### 65.16 Replay / Binding Matrix

| Binding | Replay threat | Required binding | Failure result |
| --- | --- | --- | --- |
| Responsibility class | Class expansion. | Assign only named class. | No assignment. |
| Participant/reference | Different recipient. | Bind target participant/reference. | No assignment. |
| Operation | Operation expansion. | Bind operation. | No operation authority. |
| Scope | Scope widening. | Minimum necessary scope. | No out-of-scope assignment. |
| Business Entity | Cross-BE replay. | BE binding. | No cross-BE assignment. |
| Environment | Non-prod to production. | Environment binding. | No production assignment. |
| Lifecycle | Stale/closed replay. | Current lifecycle. | No assignment. |
| Governance version | Version laundering. | Compatible version. | No assignment. |
| Event | Event replay. | Event binding where applicable. | No event authority. |
| Replacement lineage | Replacement laundering. | Replacement chain. | No replacement. |
| Closure | Residual temporary authority. | Closure binding. | No clean closure/no replay. |

### 65.17 Failure / Fail-Closed Matrix

| Failure | Assignment allowed? | State change? | Fallback? | Recovery implication | Unresolved |
| --- | --- | --- | --- | --- | --- |
| Authority missing | No. | No. | No. | May require governed path. | Assignment source. |
| Stale | No. | No. | No. | Re-establish currentness. | Currentness. |
| Revoked | No. | No. | No. | Replacement separately governed. | Revocation authority. |
| Suspended | No where applicable. | No. | No. | Reactivation separately governed. | Suspension authority. |
| Expired | No. | No. | No. | Replacement separately governed. | Expiration handling. |
| Unsupported version | No. | No. | No. | Version governance. | Migration if any. |
| Out of scope | No. | No. | No. | New in-scope basis required. | Scope model. |
| Wrong BE | No. | No. | No. | BE-specific basis required. | BE assignments. |
| Wrong environment | No. | No. | No. | Environment-specific basis. | Production governance. |
| Independence unknown | No. | No. | No. | Dependency analysis. | Provenance. |
| SoD failure | No. | No. | No. | Correct governed SoD. | Assignment SoD. |
| Negative evidence unavailable | No. | No. | No. | Verify negative source. | Negative evidence. |
| Conflict | No. | No. | No. | Conflict review. | Conflict handling. |
| Compromise suspected | No for affected basis. | No. | No. | Revalidate/recover. | Compromise handling. |
| Compromise confirmed | No for affected basis. | No. | No. | Replacement/recovery governed. | Replacement authority. |
| Assignment Authority unavailable | No by unavailability. | No. | No hidden fallback. | Ordinary path or bounded recovery. | Recovery of assigner. |
| Assignment mutation fails | No effective assignment. | No or unknown. | No. | Reconcile. | Mutation ownership. |
| Audit fails | No authority increase by audit failure. | No. | No. | Reconciliation. | Audit ownership. |

### 65.18 Compromise / Replacement Matrix

| Condition | Historical effect | Current assignment effect | Replacement rule | Fail-closed result |
| --- | --- | --- | --- | --- |
| Suspected compromise | Historical truth not rewritten. | Affected basis not relied on for new authority. | Revalidate or replace through governed basis. | No assignment from affected basis. |
| Confirmed compromise | Preserve incident history. | Affected basis blocked. | Independent replacement basis required. | No assignment. |
| Partial compromise | Preserve unaffected evidence where proven. | Affected scope blocked. | Scope-specific replacement. | No affected assignment. |
| Compromise discovered after assignment | Preserve audit trail. | Revalidate downstream impact. | Cause/scope/provenance analysis. | No new reliance until valid. |
| Compromised assigner self-replaces | No cure. | Invalid. | Separate legitimate basis required. | No replacement. |
| Common-mode compromise | Apparent separation invalid. | Independence not established. | Separate dependency required. | No assignment. |

### 65.19 Authority / Non-Authority Boundary Matrix

| Item | Identity? | Technical control? | Assignment Authority by itself? | Business authority by itself? | Standing authority? | Boundary |
| --- | --- | --- | --- | --- | --- | --- |
| Founder | Maybe. | No. | No. | No. | No. | Status != authority. |
| Owner | Maybe. | Maybe. | No. | No. | No. | Ownership != authority. |
| CEO | Maybe. | No. | No. | No. | No. | Title != authority. |
| Organizational role | Maybe. | Maybe. | No. | No. | No. | Role label != authority. |
| Authentication | Yes. | No. | No. | No. | No. | Authentication != authorization. |
| Credential | Maybe. | Yes. | No. | No. | No. | Possession != authority. |
| AWS admin | Maybe. | Yes. | No. | No. | No. | Infrastructure != authority. |
| IAM admin | Maybe. | Yes. | No. | No. | No. | IAM admin != Assignment Authority. |
| GitHub admin | Maybe. | Yes. | No. | No. | No. | GitHub admin != Assignment Authority. |
| Deployment admin | Maybe. | Yes. | No. | No. | No. | Deployment authority != Assignment Authority. |
| Assignment record | Evidence. | No. | No. | No. | No. | Record != source. |
| Assignment mutator | Maybe. | Yes. | No. | No. | No. | Mutation != authorization. |
| Verifier | Maybe. | Maybe. | No. | No. | No. | Verification != authorization. |
| Participant | Yes. | Maybe. | No. | No. | No. | Participant != authority. |
| Recovery Authority | Maybe. | Maybe. | No universal future assignment authority. | Only if separately established. | No. | Event-bound. |
| Root | Maybe. | Maybe. | No standing assignment authority. | Only if separately established. | No standing admin. | Bounded/non-standing. |
| AI/LLM/MCP | No authoritative identity. | Tooling. | No. | No. | No. | Non-authoritative. |

### 65.20 BE / Environment Isolation Matrix

| Context | Invalid inference | Required boundary | Failure result |
| --- | --- | --- | --- |
| BE A assignment | BE A -> BE B. | BE-specific authority. | No BE B assignment. |
| Cross-BE participant | Participant in one BE -> authority in another. | Assignment provenance by BE. | No cross-BE authority. |
| Non-production assignment | Non-production -> production. | Environment-specific authority. | No production assignment. |
| Production assignment | Production requires separate governance. | Production authority not granted here. | No production authority. |
| Shared infrastructure | Same infrastructure -> shared business authority. | Infrastructure non-authority. | No assignment. |
| Shared identity | Same identity system -> cross-environment authority. | Identity non-authority. | No assignment. |

### 65.21 Technology-Neutrality Matrix

| Category | Selected now? | Possible future property | Authority it must not acquire | Status |
| --- | --- | --- | --- | --- |
| AWS account | No. | Isolation if later governed. | Assignment Authority. | Non-selected. |
| IAM | No. | Technical permission if later governed. | Business authority. | Non-selected. |
| Cognito / IdP | No. | Identity attribution if later governed. | Assignment Authority. | Non-selected. |
| KMS / keys / certificates | No. | Integrity/authenticity if later governed. | Business legitimacy. | Non-selected. |
| HSM / CloudHSM | No. | Protected mechanism if later governed. | Root or Assignment Authority. | Non-selected. |
| Secrets Manager / secrets | No. | Secret handling if later governed. | Recovery or Assignment Authority. | Non-selected. |
| Database / RDS / DynamoDB | No. | Persistence if later governed. | Authority source by default. | Non-selected. |
| S3 / object store | No. | Retention if later governed. | Independent authority. | Non-selected. |
| Lambda / runtime | No. | Execution if later governed. | Authorization. | Non-selected. |
| API Gateway / API | No. | Interface if later governed. | Authority. | Non-selected. |
| EventBridge / SNS / SQS / Step Functions | No. | Workflow/eventing if later governed. | Authority. | Non-selected. |
| CloudWatch / audit service | No. | Observability if later governed. | Assignment Authority. | Non-selected. |
| GitHub / CI/CD | No. | Source/deployment if later governed. | Business authority. | Non-selected. |
| Ledger / blockchain / event store | No. | History if later governed. | Current authority by itself. | Non-selected. |
| Schema / workflow / deployment | No. | Representation/process if later governed. | Authority. | Non-selected. |

### 65.22 Unresolved-Decision Dependency Matrix

| Order | Unresolved decision | Depends on |
| --- | --- | --- |
| 1 | Concrete Assignment Authority source. | This artifact. |
| 2 | Concrete Assignment Authority participant. | Assignment authority source. |
| 3 | Concrete responsibility participants. | Assignment authority source and participant governance. |
| 4 | Participant categories. | Assignment authority and privacy governance. |
| 5 | Participant count. | Operation-specific participant governance. |
| 6 | Quorum. | Participant count and operation-specific need. |
| 7 | Human/machine allocation. | Responsibility ownership and runtime governance. |
| 8 | Identity realization. | Participant provenance. |
| 9 | Credentials. | Identity and technology governance. |
| 10 | Concrete accountable authorization responsibility. | Assignment authority. |
| 11 | Concrete qualification responsibility. | Assignment authority. |
| 12 | Custody assignment. | Assignment authority and custody governance. |
| 13 | Verifier assignment. | Assignment authority and verification governance. |
| 14 | Producer/mutation ownership. | Assignment authority and authority-source governance. |
| 15 | Audit/reconciliation/closure ownership. | Assignment authority and audit governance. |
| 16 | Restoration/reactivation ownership. | Restoration governance and assignment authority. |
| 17 | Authority-source realization. | Recovery authority-source governance. |
| 18 | Assignment persistence. | Technology and semantic contract governance. |
| 19 | Schema. | Persistence and semantic contract governance. |
| 20 | API. | Schema and workflow governance. |
| 21 | Workflow. | Assignment authority, API, and runtime governance. |
| 22 | Runtime. | Workflow and implementation planning. |
| 23 | Technology. | Technology realization governance. |
| 24 | Deployment. | Runtime and release governance. |
| 25 | Production assignments. | Separate production governance. |
| 26 | Production Assignment Authority. | Separate production governance. |
| 27 | Production authority. | Separate production governance. |

## 66. Normative Invariants

The following invariants are normative:

1. Responsibility != authority.
2. Participant != authority.
3. Assignment != authorization.
4. Assignment authority != assigned responsibility.
5. Assignment authority != participant identity.
6. Assignment authority != root.
7. Assignment authority != Recovery Authority.
8. Assignment authority != successor.
9. Assignment authority != restoration authority.
10. Assignment authority != authentication authority.
11. Assignment authority != infrastructure authority.
12. Assignment authority != credential possession.
13. Assignment authority != organizational status.
14. Assignment authority != custody.
15. Assignment authority != verification.
16. Assignment authority != mutation capability.
17. Assignment authority != audit.
18. Assignment authority != reconciliation.
19. Assignment execution != assignment legitimacy.
20. Assignment record != authority source.
21. Request != assignment authorization.
22. Qualification != assignment authorization.
23. Eligibility != assignment.
24. Technical mutation != authorization.
25. Mutation success != legitimate authorization.
26. Failed authorization -> no state change.
27. Participant cannot create authority through authority-bearing
    self-assignment.
28. Assignment Authority cannot create its own terminating basis.
29. Recovery Authority cannot perpetuate itself through assignment.
30. Root cannot become standing Assignment Authority.
31. Predecessor cannot create successor legitimacy merely by assignment.
32. Replacement != successor authority establishment.
33. Assignment != restoration.
34. Reassignment cannot launder revocation.
35. Replacement cannot launder compromise.
36. Revocation authority != restoration authority.
37. Suspension authority != restoration authority.
38. Reduction authority != increase authority.
39. Historical Assignment Authority != current Assignment Authority.
40. Historical assignment evidence != current authority.
41. Revoked Assignment Authority cannot assign.
42. Suspended Assignment Authority cannot assign where suspension applies.
43. Expired Assignment Authority cannot assign.
44. Closed Assignment Authority cannot assign.
45. Unverifiably current Assignment Authority cannot assign.
46. Out-of-scope Assignment Authority cannot assign.
47. BE A Assignment Authority != BE B Assignment Authority.
48. Non-production Assignment Authority != production Assignment Authority.
49. Different participants != independent provenance automatically.
50. Different identities != independent provenance automatically.
51. Different credentials != independent provenance automatically.
52. Different accounts != independent provenance automatically.
53. Responsibility independence != participant count.
54. No universal dual approval.
55. No universal maker/checker.
56. No universal two-person rule.
57. No universal quorum.
58. No hidden super-admin.
59. No unrestricted break-glass.
60. Founder/owner/CEO status != Assignment Authority.
61. AWS/IAM/GitHub control != Assignment Authority.
62. Credential possession != Assignment Authority.
63. Machine execution != Assignment Authority.
64. AI/LLM/MCP != Assignment Authority.
65. Assignment Authority must be minimum necessary.
66. Assignment Authority must be lifecycle-bound.
67. Assignment Authority must be provenance-bound.
68. Assignment Authority must terminate non-circularly.
69. Current revocation dominates stale positive evidence.
70. Required negative evidence unavailable != verified not revoked.
71. Assignment Authority cannot silently become authority for other Trusted
    Authorization domains.
72. Production authority remains NOT GRANTED.

## 67. Unresolved Decisions

The following decisions remain unresolved in dependency order:

1. Concrete Assignment Authority source.
2. Concrete Assignment Authority participant.
3. Concrete responsibility participants.
4. Participant categories.
5. Participant count.
6. Quorum.
7. Human/machine allocation.
8. Identity realization.
9. Credentials.
10. Concrete accountable authorization responsibility.
11. Concrete qualification responsibility.
12. Custody assignment.
13. Verifier assignment.
14. Producer/mutation ownership.
15. Audit/reconciliation/closure ownership.
16. Restoration/reactivation ownership.
17. Authority-source realization.
18. Assignment persistence.
19. Schema.
20. API.
21. Workflow.
22. Runtime.
23. Technology.
24. Deployment.
25. Production assignments.
26. Production Assignment Authority.
27. Production authority.

This artifact does not resolve these decisions.

## 68. Downstream Dependency

The immediate downstream dependency after this artifact is:

```text
Trusted Authorization Recovery Responsibility Assignment / Revocation
Ownership Realization Governance Review
```

That review is not performed by this artifact.

## 69. Technology Neutrality

This artifact does not select AWS account, IAM, Cognito, Organizations, KMS,
CloudHSM, Secrets Manager, DynamoDB, RDS, S3, Lambda, API Gateway, EventBridge,
SNS, SQS, Step Functions, CloudWatch, GitHub, CI/CD, database, object store,
event store, ledger, blockchain, IdP, hardware token, credential, key,
certificate, password, recovery code, schema, API, runtime, workflow, or
deployment.

Technology references appear only as explicit non-selection or non-authority
examples.

## 70. Cryptographic Neutrality

This artifact does not select signature scheme, hash algorithm, encryption
algorithm, PKI, certificate hierarchy, key hierarchy, HSM topology, threshold
cryptography, secret sharing, multisig, escrow, or any cryptographic mechanism.

## 71. Participant Neutrality

This artifact does not assign named human, founder, owner, CEO, executive,
board, employee, contractor, security team, administrator, developer, auditor,
third party, external custodian, office, committee, vendor, AWS identity, IAM
role, GitHub identity, service account, custodian, verifier, authorizer,
mutator, root, Recovery Authority, successor, or restorer.

Only abstract responsibility and authority classes are governed.

## 72. No Implementation

This artifact does not create Python, TypeScript, source code, tests,
dataclasses, enums, runtime models, persistence, database, schema, API,
workflow, deployment, IAM, credentials, or AWS resources.

The implementation repository remains frozen at:

```text
73d6f993e2731e55709d02413d3b0bb0ba350091
```

## 73. Production Authority

PRODUCTION AUTHORITY: NOT GRANTED

This artifact does not grant:

- production Assignment Authority;
- production participant assignment;
- production responsibility assignment;
- production Recovery TAB;
- production Recovery Authority;
- production root;
- production successor;
- production restoration;
- production credentials; or
- production implementation.

## 74. Governance Decision Summary

This artifact formalizes:

- MODEL F - HYBRID BOUNDED ASSIGNMENT AUTHORITY;
- the central legitimacy rule for Recovery responsibility assignment;
- finite terminating Assignment Authority provenance;
- assignment authorization and mutation separation;
- responsibility-class sensitivity;
- initial-assignment non-circularity;
- ordinary reassignment boundaries;
- self-assignment controls;
- beneficiary-conflict controls;
- operation-specific SoD;
- no universal participant count;
- quorum not selected;
- no universal dual approval;
- no universal maker/checker;
- no break-glass;
- lifecycle/currentness requirements;
- provenance requirements;
- negative-evidence semantics;
- revocation, suspension, replacement, restoration, Recovery Authority, root,
  and successor boundaries;
- common-mode controls;
- Business Entity and environment isolation;
- technology, participant, credential, and cryptographic neutrality;
- AI/LLM/MCP non-authority;
- fail-closed assignment semantics; and
- production authority not granted.

## 75. Closeout

This artifact creates no implementation authority and no production authority.

No downstream review is performed here.

The next governed step is the read-only or drafting step separately authorized
for:

```text
Trusted Authorization Recovery Responsibility Assignment / Revocation
Ownership Realization Governance Review
```

PRODUCTION AUTHORITY: NOT GRANTED
