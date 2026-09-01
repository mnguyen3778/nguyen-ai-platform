# Trusted Authorization Recovery Assignment Authority Source Ownership Governance v1

## 1. Status

This document is a governance artifact for the Nguyen AI Platform Trusted
Authorization domain.

Status: DRAFT FOR HUMAN REVIEW.

Governance checkpoint:

```text
4468359daa8e5c99a7336e59207b1bdad3bac691
```

Implementation checkpoint remains frozen:

```text
73d6f993e2731e55709d02413d3b0bb0ba350091
```

PRODUCTION AUTHORITY: NOT GRANTED

This artifact creates no implementation authority, no runtime authority, no
production authority, and no authority to modify the implementation repository.
It creates exactly this governance document and does not commit, tag, push,
deploy, touch AWS, instantiate TAB, activate Recovery Authority, establish
root, establish successor, authorize restoration, select credentials, select
cryptography, select technology, select participants, select participant
categories, select participant count, select quorum, create break-glass, create
universal dual approval, create universal maker/checker, or create a universal
two-person rule.

## 2. Purpose

This artifact governs the logical ownership and responsibility model for
Recovery Assignment Authority Source operations.

It formalizes how source ownership responsibilities are requested, qualified,
authorized, established, activated, maintained, verified, suspended, revoked,
replaced, audited, reconciled, closed, and provenanced without allowing
ownership to become source authority, Assignment Authority Source, Assignment
Authority, Recovery Authority, root, restoration authority, successor
authority, mutation authority, or technical super-administration.

## 3. Scope

This artifact governs:

- source ownership definition;
- source ownership and source authority separation;
- source ownership responsibility classes;
- source ownership establishment, lifecycle, currentness, suspension,
  revocation, replacement, closure, and provenance;
- request, qualification, accountable authorization, establishment,
  activation, mutation, custody, verification, negative-evidence, audit,
  reconciliation, closure, and dependency responsibilities;
- source ownership overlap and independence;
- beneficiary-conflict and common-mode controls;
- operation-specific SoD;
- fail-closed ownership semantics;
- threat model;
- required matrices;
- normative invariants;
- unresolved decisions; and
- downstream dependency selection.

## 4. Non-Scope

This artifact does not:

- select a concrete source owner;
- select a concrete source ownership participant;
- select a concrete source authorizer;
- select a concrete establishment participant;
- select a concrete lifecycle participant;
- select a concrete mutation participant;
- select a concrete custodian;
- select a concrete verifier;
- select a concrete negative-evidence participant;
- select a concrete suspension participant;
- select a concrete revocation participant;
- select a concrete replacement participant;
- select a concrete audit participant;
- select a concrete reconciliation participant;
- select a concrete closure participant;
- select a concrete provenance participant;
- select a concrete Assignment Authority Source;
- select a concrete Assignment Authority participant;
- select concrete recovery responsibility participants;
- select participant categories;
- select participant count;
- select quorum;
- select identity realization;
- select credentials;
- select cryptography;
- select technology;
- create persistence, schema, API, workflow, runtime, implementation, IAM, AWS
  resources, tests, or deployment;
- instantiate TAB;
- activate Recovery Authority;
- establish standing root;
- establish successor;
- authorize restoration;
- perform the downstream governance dependency; or
- grant production authority.

## 5. Authority

This artifact has governance drafting authority only.

It formalizes the preceding read-only review decisions:

```text
MODEL F - HYBRID BOUNDED SOURCE OWNERSHIP
RELATIONSHIP E - HYBRID BOUNDED OWNERSHIP / AUTHORITY RELATIONSHIP
OVERLAP E - HYBRID BOUNDED OVERLAP / INDEPENDENCE
```

It does not create source authority, Assignment Authority Source, Assignment
Authority, ownership assignment authority, Recovery Authority, root authority,
successor authority, restoration authority, credential authority, technical
authority, or production authority.

## 6. Predecessor Governance

This artifact is controlled by repository governance, including:

- `trusted-authorization-recovery-assignment-authority-source-realization-governance-v1.md`
- `trusted-authorization-recovery-responsibility-assignment-revocation-ownership-realization-governance-v1.md`
- `trusted-authorization-recovery-responsibility-assignment-authority-governance-v1.md`
- `trusted-authorization-recovery-evidence-responsibility-participant-realization-governance-v1.md`
- `trusted-authorization-recovery-evidence-realization-governance-v1.md`
- `trusted-authorization-recovery-evidence-custody-verification-governance-v1.md`
- `trusted-authorization-recovery-terminating-authority-basis-governance-v1.md`
- `trusted-authorization-concrete-terminating-authority-basis-governance-v1.md`
- `trusted-authorization-root-specific-operation-level-sod-governance-v1.md`
- `trusted-authorization-administrative-mutation-revocation-ownership-governance-v1.md`
- `trusted-authorization-production-authority-source-ownership-governance-v1.md`
- `trusted-authorization-bounded-recovery-governance-v1.md`
- `trusted-authorization-root-recovery-topology-governance-v1.md`
- `trusted-authorization-root-lifecycle-retention-revocation-succession-governance-v1.md`
- `trusted-authorization-downstream-authority-impact-governance-v1.md`
- `trusted-authorization-emergency-authority-reduction-audit-failure-governance-v1.md`
- `trusted-authorization-bootstrap-root-terminating-authority-source-governance-v1.md`

The following predecessor decisions are preserved:

- MODEL F - HYBRID BOUNDED AUTHORITY-SOURCE REALIZATION;
- DERIVATION E - HYBRID BOUNDED DERIVATION;
- RELATIONSHIP D - HYBRID BOUNDED ORDINARY / EXCEPTIONAL SOURCE
  RELATIONSHIP;
- MODEL F - HYBRID BOUNDED ASSIGNMENT AUTHORITY;
- MODEL F - HYBRID BOUNDED OWNERSHIP REALIZATION;
- RELATIONSHIP E - HYBRID BOUNDED OWNERSHIP RELATIONSHIP;
- MODEL G - HYBRID OPERATION-SPECIFIC SoD;
- SAME TAB GOVERNANCE MODEL != SAME TAB INSTANCE;
- root is bounded and non-standing;
- Recovery Authority is event-specific, bounded, non-standing,
  lifecycle-bound, provenance-bound, scope-bound, and closure-bound; and
- production authority remains NOT GRANTED.

## 7. Selected Ownership Model

The selected ownership model is:

```text
MODEL F - HYBRID BOUNDED SOURCE OWNERSHIP
```

This model combines:

- logical responsibility-class ownership;
- ordinary bounded ownership where legitimate;
- event-specific ownership where required;
- operation-specific independence;
- operation-specific overlap;
- authority-direction sensitivity;
- lifecycle/currentness;
- provenance;
- beneficiary-conflict controls;
- common-mode analysis;
- Business Entity isolation;
- environment isolation;
- governance-version binding;
- finite termination;
- minimum necessary responsibility;
- no universal standing owner; and
- no concrete participant selection.

## 8. Selected Ownership / Authority Relationship

The selected relationship model is:

```text
RELATIONSHIP E - HYBRID BOUNDED OWNERSHIP / AUTHORITY RELATIONSHIP
```

Ownership and authority must not be universally collapsed.

Ownership and authority must not be universally separated.

Their relationship depends on operation, consequence, authority direction,
beneficiary conflict, provenance, lifecycle, compromise state, common-mode
dependency, and applicable operation-specific SoD.

## 9. Selected Overlap / Independence Model

The selected overlap model is:

```text
OVERLAP E - HYBRID BOUNDED OVERLAP / INDEPENDENCE
```

Logical ownership responsibilities may overlap when governance permits.

Logical ownership responsibilities must remain independent where
operation-specific governance requires it.

The following inferences are rejected:

```text
LOGICAL RESPONSIBILITY SEPARATION = PARTICIPANT COUNT
INDEPENDENCE = TWO PEOPLE
INDEPENDENCE = TWO ACCOUNTS
INDEPENDENCE = QUORUM
INDEPENDENCE = UNIVERSAL DUAL APPROVAL
```

## 10. Model Rationale

Repository governance rejects a single standing source owner because it would
create concentration, self-authorization, hidden super-admin, and standing root
risk.

Repository governance rejects fully separated ownership because universal
separation would imply participant count and universal SoD that predecessor
governance explicitly refuses to select.

Repository governance rejects authority-centric ownership because Assignment
Authority, Administrative Authority, TAB, root, and Recovery Authority are not
source owners automatically.

Responsibility-class-specific and event-specific ownership are necessary
dimensions but are incomplete alone because source ownership also depends on
operation, authority direction, lifecycle, provenance, beneficiary conflict,
common-mode dependency, Business Entity, environment, governance version, and
SoD.

The hybrid bounded model is the minimum model that preserves the predecessor
source-realization chain, bounded Assignment Authority, bounded ownership
realization, operation-specific SoD, finite non-circular provenance, lifecycle
closure, and production non-grant.

## 11. Definitions

| Term | Governance meaning | Boundary |
| --- | --- | --- |
| Source Ownership | Bounded logical responsibility and accountability for governed source-related operations. | Not source authority. |
| Source Authority | Governed authority by which an Assignment Authority Source may be established or relied upon. | Not created by ownership alone. |
| Assignment Authority Source | Governed legitimacy basis from which bounded Recovery Assignment Authority derives. | Not owner, record, mechanism, identity, credential, or participant. |
| Assignment Authority | Governed authority to authorize bounded assignment-related operations. | Not source owner automatically. |
| Responsibility Ownership | Logical ownership of assigned recovery responsibilities. | Not Assignment Authority Source ownership. |
| Accountable Authorization | Authority-sensitive responsibility to authorize where independently legitimate. | Accountability != automatic authorization. |
| Mutation / Producer Responsibility | Responsibility to execute or record already-authorized source ownership or source state change. | Mutator != authorizer. |
| Custody Responsibility | Responsibility to preserve source ownership or source evidence. | Custody != authority. |
| Verification Responsibility | Responsibility to check currentness, provenance, scope, lifecycle, and conformance. | Verification != authority creation. |
| Negative-Evidence Responsibility | Responsibility for revocation, suspension, expiration, replacement, closure, compromise, or invalidation evidence. | Negative evidence != restoration authority. |
| Provenance Responsibility | Responsibility to preserve or verify derivation and dependency evidence. | Provenance responsibility != terminating authority. |
| Closure Responsibility | Responsibility to ensure temporary or event-specific ownership terminates. | Closure != authority creation. |

## 12. Fundamental Separations

The following separations are normative:

```text
SOURCE OWNERSHIP != SOURCE AUTHORITY
SOURCE OWNERSHIP != ASSIGNMENT AUTHORITY SOURCE
SOURCE OWNERSHIP != ASSIGNMENT AUTHORITY
SOURCE OWNERSHIP != RECOVERY RESPONSIBILITY OWNERSHIP
SOURCE OWNERSHIP != ACCOUNTABLE AUTHORIZATION
SOURCE OWNERSHIP != SOURCE ESTABLISHMENT AUTHORITY
SOURCE OWNERSHIP != SOURCE MUTATION AUTHORITY
SOURCE OWNERSHIP != SOURCE MUTATION CAPABILITY
SOURCE OWNERSHIP != SOURCE CUSTODY
SOURCE OWNERSHIP != SOURCE VERIFICATION
SOURCE OWNERSHIP != SOURCE AUDIT
SOURCE OWNERSHIP != SOURCE RECONCILIATION
SOURCE OWNERSHIP != SOURCE REVOCATION AUTHORITY
SOURCE OWNERSHIP != SOURCE RESTORATION AUTHORITY
SOURCE OWNERSHIP != SOURCE REPLACEMENT AUTHORITY
SOURCE OWNERSHIP != ROOT
SOURCE OWNERSHIP != RECOVERY AUTHORITY
SOURCE OWNERSHIP != TAB
SOURCE OWNERSHIP != SUCCESSOR AUTHORITY
SOURCE OWNERSHIP != AUTHENTICATION
SOURCE OWNERSHIP != IDENTITY
SOURCE OWNERSHIP != CREDENTIAL
SOURCE OWNERSHIP != INFRASTRUCTURE CONTROL
SOURCE OWNERSHIP != ORGANIZATIONAL STATUS
SOURCE OWNERSHIP != RECORD OWNERSHIP
SOURCE OWNERSHIP != AI / LLM / MCP
TECHNICAL OWNERSHIP != BUSINESS AUTHORITY
ACCOUNTABILITY != AUTOMATIC AUTHORIZATION
CONTROL OF STORAGE != AUTHORITY OVER SOURCE
CONTROL OF MUTATION MECHANISM != AUTHORITY TO AUTHORIZE MUTATION
```

## 13. Source Ownership Definition

Source Ownership means bounded logical responsibility and accountability for
governed source-related operations.

Source Ownership does not itself constitute:

- terminating authority;
- source legitimacy;
- Assignment Authority;
- authorization;
- mutation authority;
- restoration authority;
- root authority;
- Recovery Authority;
- successor authority; or
- production authority.

## 14. Ownership Does Not Create Authority

The following principle is normative:

```text
OWNERSHIP OF A SOURCE-RELATED RESPONSIBILITY DOES NOT BY ITSELF
CREATE AUTHORITY TO ESTABLISH, AUTHORIZE, MODIFY, USE, REVOKE,
RESTORE, REPLACE, OR EXTEND THE SOURCE.
```

The following inferences are rejected:

```text
"X owns the source" -> "X may authorize the source."
"X owns source operations" -> "X may create Assignment Authority."
"X is accountable" -> "X automatically has mutation authority."
```

## 15. Logical Ownership Responsibility Classes

The logical responsibility classes are:

1. Source Request / Initiation Responsibility.
2. Source Qualification / Applicability Responsibility.
3. Source Accountable Authorization Responsibility.
4. Source Establishment Responsibility.
5. Source Activation / Reliance Responsibility.
6. Source Lifecycle Responsibility.
7. Source Currentness Responsibility.
8. Source Mutation / Producer Responsibility.
9. Source Custody Responsibility.
10. Source Verification Responsibility.
11. Source Negative-Evidence Responsibility.
12. Source Suspension Responsibility.
13. Source Revocation Responsibility.
14. Source Replacement Responsibility.
15. Source Audit Responsibility.
16. Source Reconciliation Responsibility.
17. Source Closure Responsibility.
18. Source Provenance / Dependency Responsibility.

These are logical classes only. They do not imply 18 participants, 18 people,
18 identities, 18 accounts, universal separation, participant count, or quorum.

## 16. Request / Initiation Responsibility

```text
REQUEST != AUTHORIZATION.
```

Request responsibility may initiate consideration, identify need, provide
context, and identify proposed source, target, or scope.

Request responsibility cannot create source legitimacy or authorize source
operations.

## 17. Qualification Responsibility

```text
QUALIFICATION != AUTHORIZATION.
```

Qualification may assess applicability, operation, source model,
responsibility class, scope, target, Business Entity, environment, governance
version, and lifecycle prerequisites.

Qualification cannot create authority.

## 18. Accountable Authorization Responsibility

```text
ACCOUNTABLE OWNER != AUTOMATIC AUTHORIZER.
```

Accountable authorization remains an authority-sensitive responsibility
requiring an independently legitimate authority basis.

This artifact does not select the authorizer.

## 19. Source Establishment Responsibility

```text
ESTABLISHMENT RESPONSIBILITY != ESTABLISHMENT AUTHORITY.
```

Source establishment may execute or coordinate an already-authorized
establishment.

Technical establishment success does not create legitimacy.

## 20. Source Activation / Reliance Responsibility

```text
ESTABLISHED SOURCE != CURRENTLY USABLE SOURCE AUTOMATICALLY.
```

Reliance requires applicable validation of currentness, lifecycle, scope,
provenance, revocation, suspension, expiration, replacement, compromise,
operation, responsibility class, Business Entity, environment, governance
version, required negative evidence, and required SoD.

This artifact does not define runtime activation.

## 21. Source Lifecycle Responsibility

Source lifecycle responsibility concerns recognition and handling of conceptual
states:

- proposed;
- established;
- current;
- suspended;
- revoked;
- expired;
- replaced;
- compromised;
- closed; and
- historical.

This artifact does not implement a state machine.

## 22. Source Currentness Responsibility

```text
CURRENTNESS DETERMINATION != AUTHORITY CREATION.
```

Currentness responsibility determines or verifies whether source ownership or a
source state is currently usable for a governed operation.

Historical evidence does not create current legitimacy.

## 23. Source Mutation / Producer Responsibility

```text
MUTATION OWNER != AUTHORIZER
MUTATION CAPABILITY != BUSINESS AUTHORITY
```

Mutation or producer responsibility executes or records only an
already-authorized change.

If authorization fails:

```text
NO STATE CHANGE.
```

Technical mutation success without legitimate authorization:

```text
!= LEGITIMATE STATE CHANGE.
```

## 24. Source Custody Responsibility

```text
CUSTODY != AUTHORITY
CUSTODY != SOURCE LEGITIMACY
CUSTODY != ASSIGNMENT AUTHORITY
```

Custody may preserve evidence or state. Custody does not create business
authority and does not make the custodian the source owner, source authority,
Assignment Authority, or terminating basis.

## 25. Source Verification Responsibility

```text
VERIFICATION != AUTHORIZATION
VERIFICATION != AUTHORITY CREATION
```

Verification checks conformance, currentness, provenance, scope, lifecycle,
negative evidence, Business Entity, environment, governance version, and SoD.

Verification cannot manufacture legitimacy.

## 26. Negative-Evidence Responsibility

Negative-evidence responsibility covers evidence of:

- revocation;
- suspension;
- expiration;
- replacement;
- closure;
- compromise; and
- invalidation.

```text
NEGATIVE-EVIDENCE RESPONSIBILITY != RESTORATION AUTHORITY.
```

```text
"REVOCATION SOURCE COULD NOT BE CHECKED"
    !=
"VERIFIED NOT REVOKED."
```

## 27. Suspension Responsibility

Suspension is authority-blocking or authority-reducing.

```text
SUSPENSION != RESTORATION.
```

Suspension responsibility does not automatically confer authority to
reactivate, restore, replace, or assign successor authority.

## 28. Revocation Responsibility

Revocation is authority-reducing or authority-blocking.

```text
REVOCATION OWNER != RESTORATION AUTHORITY.
```

Revocation responsibility may overlap other responsibilities only when
operation-specific governance permits. This artifact creates no universal
same-owner rule and no universal separate-owner rule.

## 29. Replacement Responsibility

Replacement is a mixed-direction operation.

Replacement must prevent:

- self-replacement;
- compromised owner selecting replacement;
- provenance laundering;
- hidden successor;
- hidden restoration;
- hidden root;
- standing Recovery Authority; and
- standing ownership administrator.

## 30. Audit Responsibility

```text
AUDIT != AUTHORIZATION
AUDIT EVIDENCE != AUTHORITY SOURCE
```

Audit may establish evidence of what occurred. Audit cannot retroactively
legitimize an unauthorized source operation or ownership operation.

## 31. Reconciliation Responsibility

```text
RECONCILIATION != AUTHORITY CREATION
RECONCILIATION != RESTORATION
```

Reconciliation may detect, record, and resolve discrepancies where governed.
It cannot launder invalid source state or ownership state into legitimate
authority.

## 32. Closure Responsibility

Closure responsibility ensures temporary or event-specific ownership does not
remain standing.

Where applicable, closure must ensure:

- source no longer exercisable;
- temporary authority terminated;
- ownership no longer current;
- residual authority removed;
- negative evidence and currentness reconciled;
- audit and reconciliation completed;
- historical evidence retained as non-exercisable evidence; and
- replay prevented.

Closure does not create new authority.

## 33. Provenance / Dependency Responsibility

Provenance and dependency responsibility preserves and verifies:

- terminating basis;
- source derivation;
- ownership derivation;
- assigning authority;
- governance version;
- operation;
- responsibility class;
- target;
- scope;
- Business Entity;
- environment;
- lifecycle;
- currentness;
- suspension;
- revocation;
- expiration;
- replacement;
- compromise;
- closure; and
- dependency provenance.

```text
PROVENANCE RESPONSIBILITY != TERMINATING AUTHORITY.
```

## 34. Ownership Establishment

```text
SOURCE OWNERSHIP MUST HAVE AN INDEPENDENTLY LEGITIMATE,
GOVERNED ASSIGNMENT BASIS.
```

The following circular chain is rejected:

```text
OWNER
    ->
SELF-ASSIGNS OWNERSHIP
    ->
OWNERSHIP RECORD
    ->
CLAIMS LEGITIMACY
```

Source ownership cannot be its own terminating authority basis.

## 35. Initial Ownership

```text
FUTURE OWNER CANNOT BE THE SOLE BASIS OF ITS OWN INITIAL OWNERSHIP.
```

Initial source ownership requires finite, non-circular, independently
legitimate provenance.

This artifact does not select a concrete owner.

## 36. Ordinary Ownership Change

Ordinary ownership assignment or reassignment may use an already-governed
bounded authority path only where the path is:

- current;
- valid;
- provenance-valid;
- uncompromised;
- operation-valid;
- responsibility-class-valid;
- target-valid;
- scope-valid;
- Business-Entity-valid;
- environment-valid;
- governance-version-valid;
- lifecycle-valid;
- supported by required negative evidence;
- compliant with required SoD; and
- compliant with required independence.

This artifact does not create standing assignment authority.

## 37. Compromised Owner

Compromised ownership cannot:

- self-restore;
- self-replace;
- suppress revocation;
- extend itself;
- establish successor authority;
- create root;
- create break-glass; or
- authorize its own continued legitimacy.

## 38. Unavailable vs Compromised

```text
UNAVAILABLE != COMPROMISED.
```

Unavailability creates no automatic fallback.

Compromise requires independently legitimate authority for authority-increasing
recovery or replacement.

No hidden next-admin-wins rule is created.

## 39. Ownership Lifecycle

Ownership lifecycle is conceptual and includes:

- proposed;
- assigned;
- current;
- suspended;
- revoked;
- expired;
- replaced;
- compromised;
- closed; and
- historical.

```text
HISTORICAL OWNER RECORD != CURRENT RESPONSIBILITY.
```

This artifact does not implement a state machine.

## 40. Ownership Currentness

Missing, stale, revoked, suspended, expired, replaced, compromised, closed, or
unverifiable ownership cannot create current authority inference.

Historical legitimacy does not establish current responsibility.

## 41. Ownership Suspension

```text
SUSPENSION BLOCKS THE AFFECTED OWNERSHIP RESPONSIBILITY.
```

Suspension does not restore, reassign, select successor, create source
authority, or create new authority.

## 42. Ownership Revocation

```text
CURRENT REVOCATION
    DOMINATES
STALE POSITIVE OWNERSHIP EVIDENCE.
```

Revocation does not create restoration authority.

## 43. Ownership Replacement

Ownership replacement must not allow:

- self-appointment;
- compromised self-replacement;
- provenance laundering;
- hidden succession;
- restoration;
- universal admin; or
- standing owner.

## 44. Ownership Closure

```text
CLOSED OWNERSHIP != CURRENT OWNERSHIP.
```

Closed ownership cannot authorize, cannot mutate, cannot be replayed, and may
remain only as historical evidence.

## 45. Ownership Provenance

Ownership provenance must conceptually include:

- ownership basis;
- responsibility class;
- source relationship;
- operation;
- target;
- scope;
- Business Entity;
- environment;
- governance version;
- assigning authority;
- currentness;
- lifecycle;
- suspension;
- revocation;
- expiration;
- replacement;
- compromise;
- closure; and
- dependency provenance.

This artifact does not define schema.

## 46. Ownership Terminating Provenance

```text
SOURCE OWNERSHIP CANNOT BE ITS OWN TERMINATING AUTHORITY BASIS.
```

Every authority-sensitive ownership assignment must have finite,
non-circular, governed provenance.

## 47. Beneficiary Conflict

Operation-specific conflict controls are required where the beneficiary may be:

- future owner;
- current owner;
- Assignment Authority holder;
- responsibility owner;
- Recovery Authority;
- source mutator;
- verifier;
- custodian;
- revocation responsibility;
- replacement candidate; or
- successor candidate.

This artifact does not create universal separation.

## 48. Common-Mode Dependency

Common-mode analysis must evaluate shared dependency on:

- terminating basis;
- Administrative Authority;
- Assignment Authority;
- identity authority;
- credential control;
- infrastructure control;
- evidence source;
- custody;
- verification;
- mutation;
- organizational control;
- Recovery Authority; and
- revocation dependency.

The following separations do not prove independence automatically:

```text
DIFFERENT PEOPLE != INDEPENDENCE AUTOMATICALLY
DIFFERENT IDENTITIES != INDEPENDENCE AUTOMATICALLY
DIFFERENT CREDENTIALS != INDEPENDENCE AUTOMATICALLY
DIFFERENT SYSTEMS != INDEPENDENCE AUTOMATICALLY
```

## 49. Operation-Specific SoD

The following predecessor model is preserved:

```text
MODEL G - HYBRID OPERATION-SPECIFIC SoD.
```

Operation-specific SoD applies where required to ownership assignment, source
establishment, source authorization, source activation/reliance, source
mutation, source verification, source suspension, source revocation, source
replacement, and source closure.

This artifact does not create:

- universal dual approval;
- universal maker/checker;
- universal two-person rule;
- universal quorum; or
- fixed participant count.

## 50. Ownership Overlap

```text
LOGICAL RESPONSIBILITIES MAY OVERLAP WHERE GOVERNANCE PERMITS.
```

Overlap must be evaluated based on operation, consequence, authority direction,
beneficiary conflict, provenance, common-mode dependency, compromise state, and
applicable SoD.

Overlap does not automatically create authority.

## 51. Ownership Independence

```text
LOGICAL RESPONSIBILITIES MUST BE INDEPENDENT WHERE
OPERATION-SPECIFIC GOVERNANCE REQUIRES IT.
```

```text
INDEPENDENCE != PARTICIPANT COUNT.
```

This artifact does not select participant count or identity count.

## 52. Participant Count / Quorum

```text
PARTICIPANT COUNT: UNRESOLVED / NOT SELECTED
QUORUM: UNRESOLVED / NOT SELECTED
```

No fixed count, threshold, or voting model is selected.

## 53. Root Boundary

```text
ROOT != DEFAULT SOURCE OWNER.
```

Root remains bounded and non-standing.

Root cannot become universal ownership administrator.

## 54. Recovery Authority Boundary

```text
RECOVERY AUTHORITY != DEFAULT SOURCE OWNER.
```

Recovery Authority cannot automatically own source establishment, its own
continuation, its own replacement, revocation suppression, restoration,
successor selection, or permanent source administration.

## 55. TAB Boundary

```text
TAB != SOURCE OWNER.
```

TAB may provide terminating legitimacy where required but does not become
standing ownership.

This artifact does not instantiate TAB.

## 56. Assignment Authority Boundary

```text
ASSIGNMENT AUTHORITY != SOURCE OWNER AUTOMATICALLY.
```

Assignment Authority may authorize ownership assignment only within its
separately governed scope.

## 57. Responsibility Ownership Boundary

```text
RECOVERY RESPONSIBILITY OWNERSHIP
    !=
ASSIGNMENT AUTHORITY SOURCE OWNERSHIP.
```

Owning an assigned recovery responsibility cannot imply ownership of the source
that authorized the assignment.

## 58. Authentication / Identity / Credential Boundary

```text
AUTHENTICATION != SOURCE OWNERSHIP
IDENTITY != SOURCE OWNERSHIP
CREDENTIAL POSSESSION != SOURCE OWNERSHIP
```

This artifact does not select identity provider, identity model, credential,
password, token, key, certificate, or credential mechanism.

## 59. Organizational Status Boundary

None of the following automatically confers source ownership:

- founder;
- owner;
- CEO;
- executive;
- board;
- employee;
- contractor;
- administrator;
- security;
- developer; or
- auditor.

No concrete participant is selected.

## 60. Infrastructure Boundary

```text
AWS CONTROL != SOURCE OWNERSHIP
IAM CONTROL != SOURCE OWNERSHIP
GITHUB CONTROL != SOURCE OWNERSHIP
DATABASE CONTROL != SOURCE OWNERSHIP
DEPLOYMENT CONTROL != SOURCE OWNERSHIP
```

Infrastructure capability does not create governed business ownership.

## 61. Human / Machine Boundary

Human/machine allocation remains unresolved.

```text
MACHINE EXECUTION != BUSINESS OWNERSHIP.
```

This artifact does not allocate responsibility classes to humans or machines.

## 62. AI / LLM / MCP Boundary

AI/LLM/MCP cannot independently become authoritative:

- source owner;
- source authorizer;
- Assignment Authority;
- revocation authority;
- restoration authority;
- replacement authority;
- root;
- Recovery Authority;
- successor selector; or
- production authority.

AI/LLM/MCP may assist only non-authoritatively where separately governed.

## 63. Business Entity Isolation

```text
SOURCE OWNERSHIP FOR BE A
    !=
SOURCE OWNERSHIP FOR BE B.
```

No cross-BE ownership inference is created.

## 64. Environment Isolation

```text
NON-PRODUCTION SOURCE OWNERSHIP
    !=
PRODUCTION SOURCE OWNERSHIP.
```

No production owner is selected.

## 65. Governance Version

Ownership validity must be bound to supported governance version.

Unsupported, obsolete, or incompatible governance version cannot silently
preserve current ownership.

This artifact does not implement a compatibility mechanism.

## 66. Replay Prevention

The ownership model must prevent:

- historical owner replay;
- expired owner replay;
- revoked owner replay;
- suspended owner replay;
- replaced owner replay;
- closed owner replay;
- cross-BE reuse;
- cross-environment reuse;
- wrong-source reuse;
- wrong-operation reuse;
- wrong-responsibility-class reuse; and
- cross-event reuse.

This artifact does not select cryptography.

## 67. Minimum Necessary Ownership

```text
OWNERSHIP MUST BE NO BROADER THAN REQUIRED FOR THE GOVERNED
RESPONSIBILITY AND OPERATION.
```

The following inferences are rejected:

```text
OWNER FOR OPERATION X -> OWNER FOR ALL OPERATIONS
OWNER FOR CLASS X -> OWNER FOR ALL CLASSES
OWNER FOR BE A -> OWNER FOR BE B
NON-PRODUCTION OWNER -> PRODUCTION OWNER
```

## 68. Authority Direction

Authority-increasing or enabling operations include:

- initial ownership;
- source establishment;
- source activation/reliance;
- ownership assignment;
- reactivation;
- restoration; and
- successor establishment.

Authority-reducing or blocking operations include:

- suspension;
- revocation;
- emergency reduction; and
- closure.

Mixed operations include:

- reassignment; and
- replacement.

```text
AUTHORITY-REDUCING RESPONSIBILITY != RESTORATION AUTHORITY.
```

## 69. Fail-Closed Semantics

The following outcomes are normative:

```text
MISSING OWNERSHIP
  -> NO OWNERSHIP-BASED AUTHORITY INFERENCE
INVALID OWNERSHIP
  -> NO AUTHORITY INFERENCE
UNVERIFIABLE OWNERSHIP
  -> NO AUTHORITY INFERENCE
STALE OWNERSHIP
  -> NO AUTHORITY INFERENCE
SUSPENDED OWNERSHIP
  -> NO AFFECTED OPERATION
REVOKED OWNERSHIP
  -> NO AUTHORITY INFERENCE
EXPIRED OWNERSHIP
  -> NO AUTHORITY INFERENCE
REPLACED OWNERSHIP
  -> NO AUTHORITY FROM PREDECESSOR OWNERSHIP
CLOSED OWNERSHIP
  -> NO AUTHORITY INFERENCE
COMPROMISED OWNERSHIP
  -> NO AUTHORITY-INCREASING USE
WRONG SOURCE
  -> NO AUTHORITY INFERENCE
WRONG OPERATION
  -> NO AUTHORITY INFERENCE
WRONG RESPONSIBILITY CLASS
  -> NO AUTHORITY INFERENCE
WRONG BE
  -> NO AUTHORITY INFERENCE
WRONG ENVIRONMENT
  -> NO AUTHORITY INFERENCE
UNSUPPORTED GOVERNANCE VERSION
  -> NO AUTHORITY INFERENCE
INVALID PROVENANCE
  -> NO AUTHORITY INFERENCE
CIRCULAR PROVENANCE
  -> NO AUTHORITY INFERENCE
REQUIRED NEGATIVE EVIDENCE UNAVAILABLE
  -> NO AUTHORITY-INCREASING OPERATION
REQUIRED SoD NOT ESTABLISHED
  -> OPERATION STOPS
REQUIRED INDEPENDENCE NOT ESTABLISHED
  -> OPERATION STOPS
OWNERSHIP RECORD EXISTS WITHOUT LEGITIMATE ASSIGNMENT BASIS
  -> NO AUTHORITY INFERENCE
TECHNICAL MUTATION SUCCEEDS WITHOUT AUTHORIZATION
  -> NO LEGITIMATE STATE CHANGE
```

No convenience fallback is permitted.

## 70. Threat Model

| # | Threat | Targeted invariant | Affected ownership operation | Governance control | Fail-closed result | Unresolved dependency |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Source owner treats ownership as source authority. | Source ownership != source authority. | Source use. | Authority/ownership separation. | No authority inference. | Ownership assignment authority. |
| 2 | Source owner treats ownership as Assignment Authority. | Source ownership != Assignment Authority. | Assignment. | Assignment Authority validation. | No Assignment Authority. | Assignment Authority participant. |
| 3 | Responsibility owner claims source ownership automatically. | Responsibility owner != source owner automatically. | Ownership claim. | Responsibility/source boundary. | No source ownership. | Responsibility participants. |
| 4 | Assignment Authority claims source ownership automatically. | Assignment Authority != source owner automatically. | Ownership claim. | Scoped authorization only. | No ownership inference. | Assignment Authority scope. |
| 5 | Accountable owner claims automatic authorization. | Accountability != automatic authorization. | Authorization. | Independent authority basis. | No authorization. | Source authorizer. |
| 6 | Request owner authorizes own request. | Request != authorization. | Request. | Request/authorization separation. | No authorization. | Source request governance. |
| 7 | Qualification owner converts qualification into authorization. | Qualification != authorization. | Qualification. | Qualification boundary. | No authorization. | Source qualifier. |
| 8 | Establishment owner self-authorizes establishment. | Establishment responsibility != authority. | Establishment. | Prior authorization required. | No source establishment. | Establishment authority. |
| 9 | Activation owner bypasses currentness. | Established source != current source automatically. | Activation/reliance. | Currentness validation. | No reliance. | Currentness realization. |
| 10 | Lifecycle owner extends source without authority. | Lifecycle responsibility != authority. | Lifecycle. | Assignment basis required. | No extension. | Lifecycle owner. |
| 11 | Currentness owner manufactures currentness. | Currentness != authority creation. | Currentness. | Independent evidence. | Not current. | Currentness verifier. |
| 12 | Mutation owner creates legitimacy by mutation. | Mutation owner != authorizer. | Mutation. | Authorization before mutation. | No legitimate state change. | Mutation participant. |
| 13 | Custodian treats custody as authority. | Custody != authority. | Custody. | Custody boundary. | No authority. | Custodian. |
| 14 | Verifier treats verification as authority. | Verification != authorization. | Verification. | Verification boundary. | No authority creation. | Verifier. |
| 15 | Negative-evidence owner restores authority. | Negative evidence != restoration. | Negative evidence. | Restoration boundary. | No restoration. | Restoration governance. |
| 16 | Suspension owner restores authority. | Suspension != restoration. | Suspension. | Restoration separate. | No restoration. | Restoration governance. |
| 17 | Revocation owner restores authority. | Revocation owner != restoration authority. | Revocation. | Direction separation. | No restoration. | Restoration governance. |
| 18 | Replacement owner self-selects replacement. | Replacement cannot self-legitimize. | Replacement. | Independent replacement basis. | No replacement. | Replacement owner. |
| 19 | Auditor retroactively legalizes operation. | Audit != authorization. | Audit. | Audit non-authority. | No legitimacy. | Audit participant. |
| 20 | Reconciler launders invalid state. | Reconciliation != authority creation. | Reconciliation. | Reconciliation boundary. | No legitimacy. | Reconciler. |
| 21 | Closure owner leaves residual authority. | Closure cannot preserve temporary authority. | Closure. | Closure verification. | No clean closure. | Closure participant. |
| 22 | Provenance owner becomes terminating authority. | Provenance responsibility != terminating authority. | Provenance. | Terminating basis required. | No authority. | Provenance participant. |
| 23 | Future owner self-assigns initial ownership. | Future owner cannot legitimize own initial ownership. | Initial ownership. | Independent provenance. | No ownership. | Initial assignment authority. |
| 24 | Ownership record creates ownership legitimacy. | Record ownership != source ownership. | Record. | Assignment basis validation. | No ownership inference. | Persistence/schema. |
| 25 | Compromised owner self-restores. | Compromised owner cannot self-restore. | Compromise. | Independent basis. | No restoration. | Recovery governance. |
| 26 | Compromised owner self-replaces. | Compromised owner cannot self-replace. | Replacement. | Independent replacement basis. | No replacement. | Replacement governance. |
| 27 | Compromised owner suppresses revocation. | Current revocation dominates stale evidence. | Revocation. | Negative-evidence independence. | No authority increase. | Revocation participant. |
| 28 | Unavailable owner triggers hidden fallback. | Unavailability creates no fallback. | Unavailability. | Governed replacement only. | No fallback. | Availability governance. |
| 29 | Root becomes default source owner. | Root != default source owner. | Ownership assignment. | Root containment. | No ownership. | Root governance. |
| 30 | Recovery Authority becomes default source owner. | Recovery Authority != default source owner. | Recovery. | RA containment. | No ownership. | Recovery lifecycle. |
| 31 | TAB becomes standing source owner. | TAB != source owner. | TAB use. | TAB containment. | No standing ownership. | TAB realization. |
| 32 | Assignment Authority becomes universal source owner. | Assignment Authority != universal source owner. | Assignment. | Scope binding. | No universal owner. | Assignment Authority scope. |
| 33 | Administrative Authority becomes universal source owner. | Administrative Authority != universal source owner. | Administration. | Minimum necessary bounds. | No universal owner. | Admin governance. |
| 34 | Founder/owner/CEO status creates ownership. | Organizational status != source ownership. | Ownership claim. | Status boundary. | No ownership. | Participant governance. |
| 35 | Authentication creates ownership. | Authentication != source ownership. | Authentication. | Authentication boundary. | No ownership. | Identity governance. |
| 36 | Identity creates ownership. | Identity != source ownership. | Identity. | Identity boundary. | No ownership. | Identity realization. |
| 37 | Credential possession creates ownership. | Credential possession != source ownership. | Credential use. | Credential boundary. | No ownership. | Credential realization. |
| 38 | AWS/IAM/GitHub control creates ownership. | Infrastructure control != source ownership. | Infrastructure. | Infrastructure boundary. | No ownership. | Technology governance. |
| 39 | Storage control creates ownership. | Storage control != authority. | Custody/storage. | Storage boundary. | No ownership. | Persistence. |
| 40 | Deployment control creates ownership. | Deployment control != source ownership. | Deployment. | Infrastructure boundary. | No ownership. | Deployment governance. |
| 41 | Machine execution creates ownership. | Machine execution != business ownership. | Automation. | Human/machine boundary. | No ownership. | Human/machine allocation. |
| 42 | AI/LLM/MCP becomes source owner. | AI/LLM/MCP != authoritative source owner. | Assistance. | AI non-authority. | No ownership. | Tool governance if any. |
| 43 | Different people mask common dependency. | Different people != independent control. | SoD. | Common-mode analysis. | No independence. | Participant count. |
| 44 | Different identities mask common dependency. | Different identities != independent control. | SoD. | Identity dependency review. | No independence. | Identity realization. |
| 45 | Different credentials mask common dependency. | Different credentials != independent control. | SoD. | Credential dependency review. | No independence. | Credentials. |
| 46 | Different systems mask common dependency. | Different systems != independent control. | SoD. | Infrastructure dependency review. | No independence. | Technology. |
| 47 | Universal separation creates hidden fixed participant count. | Logical separation != participant count. | SoD. | No universal separation. | No count inference. | Participant count. |
| 48 | Universal overlap creates self-authorization. | Overlap only where governed. | Overlap. | Conflict and SoD review. | No operation. | Operation-specific SoD. |
| 49 | Universal dual approval introduced without basis. | No universal dual approval. | Authorization. | Operation-specific SoD. | No count-based authority. | SoD governance. |
| 50 | Universal maker/checker introduced without basis. | No universal maker/checker. | Mutation/verification. | Operation-specific separation. | No universal rule. | SoD governance. |
| 51 | Universal quorum introduced without basis. | No universal quorum. | Authorization. | Quorum non-selection. | No quorum authority. | Quorum. |
| 52 | Historical owner replay. | Historical owner record != current responsibility. | Replay. | Currentness validation. | No authority inference. | Lifecycle evidence. |
| 53 | Expired owner replay. | Expired ownership != current ownership. | Replay. | Expiration check. | No authority inference. | Expiration governance. |
| 54 | Suspended owner replay. | Suspended ownership not exercisable where applicable. | Replay. | Suspension check. | No affected operation. | Suspension governance. |
| 55 | Revoked owner replay. | Revoked ownership != current ownership. | Replay. | Revocation check. | No authority inference. | Revocation evidence. |
| 56 | Replaced owner replay. | Replaced ownership != current ownership. | Replay. | Replacement lineage. | No predecessor authority. | Replacement governance. |
| 57 | Closed owner replay. | Closed ownership != current ownership. | Replay. | Closure check. | No authority inference. | Closure governance. |
| 58 | Cross-BE ownership reuse. | BE A ownership != BE B ownership. | Cross-BE. | BE binding. | No ownership inference. | BE governance. |
| 59 | Cross-environment ownership reuse. | Non-production ownership != production ownership. | Environment. | Environment binding. | No production ownership. | Production governance. |
| 60 | Wrong-source ownership reuse. | Ownership source-bound. | Source use. | Source binding. | No authority inference. | Source realization. |
| 61 | Wrong-operation ownership reuse. | Ownership operation-bound where required. | Operation. | Operation binding. | No authority inference. | Operation taxonomy. |
| 62 | Wrong-responsibility-class ownership reuse. | Ownership class-bound where required. | Responsibility class. | Class binding. | No authority inference. | Class governance. |
| 63 | Cross-event ownership reuse. | Event-bound ownership not replayable. | Event. | Event and closure binding. | No authority inference. | Event governance. |
| 64 | Stale positive ownership overrides current revocation. | Current revocation dominates stale positive evidence. | Revocation. | Negative-evidence currentness. | No authority increase. | Negative-evidence participant. |
| 65 | Revocation evidence unavailable interpreted as not revoked. | Unavailable revocation evidence != verified not revoked. | Revocation check. | Fail-closed negative evidence. | No authority increase. | Revocation availability. |
| 66 | Ownership scope silently expands. | Ownership must be minimum necessary. | Scope. | Scope binding. | No expanded ownership. | Scope governance. |
| 67 | Non-production owner becomes production owner. | Non-production ownership != production ownership. | Production. | Environment isolation. | No production authority. | Production governance. |
| 68 | Reduction responsibility reused for restoration. | Reduction responsibility != restoration authority. | Restoration. | Direction separation. | No restoration. | Restoration governance. |
| 69 | Replacement creates hidden successor. | Replacement != successor authority. | Replacement. | Successor boundary. | No successor. | Successor governance. |
| 70 | Replacement creates hidden root. | Replacement != root. | Replacement. | Root boundary. | No root. | Root governance. |
| 71 | Replacement creates hidden Recovery Authority. | Replacement != Recovery Authority. | Replacement. | RA boundary. | No Recovery Authority. | Recovery governance. |
| 72 | Ownership lifecycle never closes. | Ownership must be lifecycle-bound. | Closure. | Closure responsibility. | No clean closure. | Closure participant. |

## 71. Required Matrices

### 71.1 Ownership Model Comparison Matrix

| Model | Fit | Rejected or selected reason | Status |
| --- | --- | --- | --- |
| Model A - Single Standing Source Owner | Weak. | Creates concentration, standing owner, self-authorization, hidden super-admin risk. | Rejected. |
| Model B - Fully Separated Ownership | Partial. | Implies universal SoD and participant count. | Rejected. |
| Model C - Authority-Centric Ownership | Weak. | Collapses authority and ownership. | Rejected. |
| Model D - Responsibility-Class-Specific Ownership | Useful dimension. | Insufficient without operation, lifecycle, provenance, and direction. | Included in Model F. |
| Model E - Event-Specific Source Ownership | Useful for exceptional events. | Insufficient for ordinary ownership. | Included in Model F. |
| Model F - Hybrid Bounded Source Ownership | Strong. | Preserves all predecessor constraints. | SELECTED. |
| Model G - Underdetermined | Not needed. | Repository evidence is sufficient. | Not selected. |

### 71.2 Source Ownership / Authority Boundary Matrix

| Concept | Source ownership by itself? | Authority by itself? | Boundary |
| --- | --- | --- | --- |
| Source Ownership | Yes as responsibility. | No. | Ownership != authority. |
| Source Authority | No. | Yes only if separately governed. | Authority basis required. |
| Assignment Authority Source | No. | Source legitimacy basis. | Not owner. |
| Assignment Authority | No automatically. | Scoped if valid. | May authorize only in scope. |
| Recovery Responsibility Ownership | No. | No by itself. | Not source ownership. |
| Root | No. | Not standing. | Not default owner. |
| Recovery Authority | No. | Event-bound if valid. | Not default owner. |
| TAB | No. | Terminating basis where valid. | Not source owner. |

### 71.3 Logical Ownership Responsibility Matrix

| Class | Function | Authority created? | Participant selected? |
| --- | --- | --- | --- |
| Request / Initiation | Initiate consideration. | No. | No. |
| Qualification / Applicability | Assess fit and prerequisites. | No. | No. |
| Accountable Authorization | Authorize if independently valid. | Not by accountability. | No. |
| Establishment | Coordinate authorized establishment. | No. | No. |
| Activation / Reliance | Govern source use readiness. | No. | No. |
| Lifecycle | Track conceptual state. | No. | No. |
| Currentness | Verify current usability. | No. | No. |
| Mutation / Producer | Record authorized changes. | No. | No. |
| Custody | Preserve evidence/state. | No. | No. |
| Verification | Check conformance. | No. | No. |
| Negative Evidence | Maintain blocking evidence. | No restoration. | No. |
| Suspension | Block affected responsibility. | No restoration. | No. |
| Revocation | Reduce/block authority. | No restoration. | No. |
| Replacement | Replace under governed basis. | No self-legitimacy. | No. |
| Audit | Record what occurred. | No. | No. |
| Reconciliation | Resolve discrepancies. | No. | No. |
| Closure | Terminate temporary responsibility. | No. | No. |
| Provenance / Dependency | Preserve derivation. | No. | No. |

### 71.4 Request / Authorization Matrix

| Request condition | Authorization result | Required control |
| --- | --- | --- |
| Request submitted | No authorization by itself. | Independent authorization. |
| Self-benefiting request | High conflict. | Beneficiary review. |
| Request missing scope | Not actionable. | Scope qualification. |
| Request stale | No current basis. | Currentness check. |

### 71.5 Qualification / Authorization Matrix

| Qualification result | Authorization result | Boundary |
| --- | --- | --- |
| Eligible | Not assigned by itself. | Eligibility != authorization. |
| Applicable | No authority by itself. | Qualification != authorization. |
| Inapplicable | Operation stops. | No fallback. |
| Unverifiable | Operation stops. | Fail closed. |

### 71.6 Accountable Ownership / Authorization Matrix

| Accountable role | Automatic authority? | Required basis |
| --- | --- | --- |
| Accountable owner | No. | Independently legitimate authority. |
| Process owner | No. | Governed Assignment Authority. |
| Beneficiary owner | No sole basis. | Conflict controls. |
| Historical owner | No. | Currentness required. |

### 71.7 Source Establishment Ownership Matrix

| Establishment case | Permitted? | Control |
| --- | --- | --- |
| Already authorized establishment | Conditional. | Validate authority and SoD. |
| Self-authorized establishment | No. | Independent basis. |
| Technical establishment only | No legitimacy. | Mutation non-authority. |
| Establishment after compromise | Conditional. | Independent terminating provenance. |

### 71.8 Source Activation / Reliance Ownership Matrix

| Reliance factor | Required? | Failure result |
| --- | --- | --- |
| Currentness | Yes. | No reliance. |
| Lifecycle valid | Yes. | No reliance. |
| Scope valid | Yes. | No reliance. |
| Negative evidence available | Yes where required. | No authority increase. |
| SoD satisfied | Yes where required. | Operation stops. |

### 71.9 Source Lifecycle Ownership Matrix

| State | Ownership current? | Authority inference? |
| --- | --- | --- |
| Proposed | No. | None. |
| Assigned | Conditional. | None by ownership alone. |
| Current | Potentially. | None by ownership alone. |
| Suspended | No where applicable. | None. |
| Revoked | No. | None. |
| Expired | No. | None. |
| Replaced | No from predecessor. | None. |
| Compromised | No authority increase. | None. |
| Closed | No. | None. |
| Historical | No. | None. |

### 71.10 Source Currentness Ownership Matrix

| Evidence | Currentness effect | Boundary |
| --- | --- | --- |
| Current valid evidence | Supports currentness. | Still no authority by ownership alone. |
| Historical evidence | Not current. | Audit only. |
| Stale evidence | Not current. | No authority inference. |
| Conflicting evidence | Unknown. | Fail closed. |
| Negative evidence unavailable | Unknown. | No authority increase. |

### 71.11 Source Mutation / Producer Ownership Matrix

| Mutation condition | Legitimate state change? | Control |
| --- | --- | --- |
| Authorized mutation | Conditional. | Scope and verification. |
| Failed authorization | No. | No state change. |
| Technical success only | No. | Mutation != authority. |
| Mutator beneficiary | High risk. | SoD/conflict review. |

### 71.12 Source Custody Ownership Matrix

| Custody condition | Authority implication | Control |
| --- | --- | --- |
| Preserve evidence | None. | Verification required. |
| Transfer evidence | None. | Custody != replacement. |
| Withhold evidence | Blocks validation. | No authority increase. |
| Custody compromised | Dependency risk. | Common-mode review. |

### 71.13 Source Verification Ownership Matrix

| Verification function | Creates authority? | Failure result |
| --- | --- | --- |
| Verify currentness | No. | No reliance if failed. |
| Verify provenance | No. | No authority inference if failed. |
| Verify scope | No. | No out-of-scope use. |
| Verify SoD | No. | Operation stops if absent. |

### 71.14 Negative-Evidence Ownership Matrix

| Evidence type | Effect | Restoration implication |
| --- | --- | --- |
| Revocation | Blocks currentness. | None. |
| Suspension | Blocks affected scope. | None. |
| Expiration | Ends currentness. | None. |
| Replacement | Ends predecessor. | None. |
| Closure | Ends exercisability. | None. |
| Compromise | Blocks authority increase. | None. |

### 71.15 Suspension Ownership Matrix

| Suspension case | Effect | Boundary |
| --- | --- | --- |
| Scoped suspension | Blocks scoped ownership. | No restoration. |
| Operation suspension | Blocks operation. | No reassignment. |
| Suspension evidence unavailable | Unknown. | Fail closed where required. |
| Lift suspension | Not authorized here. | Separate governance. |

### 71.16 Revocation Ownership Matrix

| Revocation case | Effect | Boundary |
| --- | --- | --- |
| Current revocation | Ownership not current. | Dominates stale evidence. |
| Revocation unavailable | Unknown. | Not verified not revoked. |
| Revocation by beneficiary | Conflict risk. | Independence where required. |
| Revocation completed | No restoration. | Separate restoration. |

### 71.17 Replacement Ownership Matrix

| Replacement case | Permitted? | Control |
| --- | --- | --- |
| Ordinary valid replacement | Conditional. | Bounded authority path. |
| Self-replacement | No sole basis. | Independent basis. |
| Compromised replacement | No self basis. | Independent termination. |
| Replacement creates successor/root/RA | No. | Boundary controls. |

### 71.18 Audit Ownership Matrix

| Audit function | Authority? | Boundary |
| --- | --- | --- |
| Record event | No. | Evidence only. |
| Identify discrepancy | No. | Reconciliation required. |
| Historical proof | No current authority. | Currentness required. |
| Audit failure | No fallback. | Obligation remains. |

### 71.19 Reconciliation Ownership Matrix

| Reconciliation case | Authority? | Failure result |
| --- | --- | --- |
| Match request/authorization/mutation | No. | Evidence support only. |
| Mismatch found | No. | No reliance. |
| Launder invalid mutation | Prohibited. | No legitimacy. |
| Closure reconciliation incomplete | No. | No clean closure. |

### 71.20 Closure Ownership Matrix

| Closure condition | Required result | Authority after closure |
| --- | --- | --- |
| Temporary ownership closed | Non-current. | None. |
| Residual authority detected | Must resolve. | No clean closure. |
| Historical evidence retained | Audit only. | None. |
| Replay attempted | Reject. | No authority inference. |

### 71.21 Provenance / Dependency Ownership Matrix

| Provenance element | Required? | Failure result |
| --- | --- | --- |
| Terminating basis | Yes. | No legitimacy. |
| Ownership derivation | Yes. | No ownership inference. |
| Assigning authority | Yes. | No ownership inference. |
| BE/environment/version | Yes. | No cross-scope inference. |
| Dependency provenance | Where independence required. | No independence. |

### 71.22 Initial Ownership Establishment Matrix

| Initial case | Legitimate? | Required basis |
| --- | --- | --- |
| Future owner self-assigns | No. | Independent basis. |
| No current owner exists | Conditional. | Governed terminating provenance. |
| Initial record only | No. | Assignment basis. |
| Initial exceptional recovery | Conditional. | TAB or other governed basis where required. |

### 71.23 Ordinary Ownership Change Matrix

| Condition | Ordinary change allowed? | Boundary |
| --- | --- | --- |
| Current bounded path | Conditional. | Full validation required. |
| Revoked path | No. | No authority inference. |
| Compromised path | No increase. | Independent basis. |
| Wrong BE/environment | No. | Isolation. |
| Missing SoD | No. | Operation stops. |

### 71.24 Compromised / Unavailable Owner Matrix

| Condition | Effect | Required handling |
| --- | --- | --- |
| Benign unavailable | No automatic compromise. | Governed replacement if valid. |
| Unavailable required evidence | Unknown. | Fail closed. |
| Compromised owner | No authority increase. | Independent basis. |
| Compromised authority path | No self-repair. | Independent termination. |

### 71.25 Ownership Lifecycle Matrix

| State | Current responsibility? | Replay allowed? |
| --- | --- | --- |
| Proposed | No. | No. |
| Assigned | Conditional. | No outside scope. |
| Current | Yes if valid. | No outside scope. |
| Suspended | No where applicable. | No. |
| Revoked | No. | No. |
| Expired | No. | No. |
| Replaced | No from predecessor. | No. |
| Compromised | No increase. | No. |
| Closed | No. | No. |
| Historical | No. | No. |

### 71.26 Ownership Provenance Matrix

| Element | Required conceptually? | Boundary |
| --- | --- | --- |
| Ownership basis | Yes. | Cannot self-create. |
| Responsibility class | Yes. | Class-bound. |
| Source relationship | Yes. | Source-bound. |
| Operation/target/scope | Yes. | No broad reuse. |
| BE/environment/version | Yes. | No cross-scope reuse. |
| Lifecycle/currentness | Yes. | Historical not current. |
| Negative evidence | Where applicable. | Revocation dominates. |
| Dependency provenance | Where required. | Common-mode control. |

### 71.27 Beneficiary-Conflict Matrix

| Beneficiary | Risk | Control |
| --- | --- | --- |
| Future owner | Self-legitimacy. | Independent initial basis. |
| Current owner | Self-extension. | Authority and SoD validation. |
| Assignment Authority holder | Self-ownership. | Scope/control review. |
| Recovery Authority | Self-perpetuation. | RA containment. |
| Mutator/verifier/custodian | Laundering/self-certification. | Separation where required. |
| Replacement/successor candidate | Hidden succession. | Successor boundary. |

### 71.28 Common-Mode Dependency Matrix

| Dependency | False independence signal | Actual control |
| --- | --- | --- |
| Terminating basis | Different records. | Independent basis where required. |
| Administrative Authority | Different admin labels. | No shared compromised basis. |
| Assignment Authority | Different assignment records. | Authority provenance check. |
| Identity/credentials | Different accounts. | Control-dependency review. |
| Infrastructure | Different systems. | Shared-control review. |
| Evidence/custody/verification/mutation | Different functions. | Provenance and conflict analysis. |
| Recovery Authority | Event label. | Not sole future basis. |

### 71.29 Operation-Specific SoD Matrix

| Operation | Direction | SoD sensitivity | Universal count? |
| --- | --- | --- | --- |
| Ownership assignment | Increasing. | High. | No. |
| Source establishment | Increasing. | High. | No. |
| Source authorization | Increasing. | Very high. | No. |
| Activation/reliance | Increasing/enabling. | High. | No. |
| Mutation | State-changing. | High. | No. |
| Verification | Neutral/supporting. | High. | No. |
| Suspension/revocation | Reducing. | High. | No. |
| Replacement | Mixed. | Very high. | No. |
| Closure | Reducing/neutral. | High. | No. |

### 71.30 Ownership Overlap / Separation Matrix

| Relationship | Allowed? | Condition |
| --- | --- | --- |
| Universal overlap | No. | Self-authorization risk. |
| Universal separation | No. | Implies participant count. |
| Class-specific overlap | Conditional. | If governed. |
| Operation-specific overlap | Conditional. | If SoD permits. |
| Hybrid bounded overlap/independence | Yes. | Selected model. |

### 71.31 Authority-Direction / Ownership Matrix

| Direction | Ownership posture | Invalid inference |
| --- | --- | --- |
| Initial ownership | Independent basis required. | Future owner self-basis. |
| Source establishment | Strong validation. | Establishment creates authority. |
| Activation/reliance | Currentness required. | Established means usable. |
| Restoration/reactivation | Separately governed. | Reduction owner restores. |
| Suspension/revocation | Blocking only. | Restoration authority. |
| Reassignment/replacement | Mixed controls. | Hidden successor/root/RA. |
| Closure | Termination required. | Residual standing ownership. |

### 71.32 Root / Recovery Authority / TAB Boundary Matrix

| Concept | Source owner by default? | Boundary |
| --- | --- | --- |
| Root | No. | Bounded and non-standing. |
| Recovery Authority | No. | Event-specific and closure-bound. |
| TAB | No. | Terminating basis where valid. |
| Successor | No. | Separately governed. |
| Restoration Authority | No. | Not created here. |

### 71.33 Assignment Authority / Source Ownership Matrix

| Condition | Source ownership result | Boundary |
| --- | --- | --- |
| Valid scoped Assignment Authority | May authorize ownership assignment. | Not owner automatically. |
| Stale/revoked authority | No ownership. | Currentness required. |
| Out-of-scope authority | No ownership. | Scope-bound. |
| Assignment Authority beneficiary | Conflict risk. | SoD required where applicable. |

### 71.34 Responsibility Ownership / Source Ownership Matrix

| Responsibility ownership state | Source ownership result |
| --- | --- |
| Current recovery responsibility owner | No automatic source ownership. |
| Historical responsibility owner | No source ownership. |
| Suspended/revoked responsibility owner | No source ownership. |
| Replacement candidate | No self-legitimacy. |

### 71.35 Authentication / Identity / Credential Boundary Matrix

| Concept | Creates ownership? | Boundary |
| --- | --- | --- |
| Authentication | No. | Authentication != ownership. |
| Identity | No. | Identity != ownership. |
| Credential possession | No. | Possession != ownership. |
| Account/session | No. | Technical attribution only. |
| Password/key/certificate/token | No. | Credential not selected. |

### 71.36 Organizational Status / Ownership Matrix

| Status label | Creates ownership? | Boundary |
| --- | --- | --- |
| Founder/owner/CEO | No. | Status non-authority. |
| Executive/board | No. | Status non-authority. |
| Employee/contractor | No. | Status non-authority. |
| Administrator/security/developer/auditor | No. | Role label non-authority. |

### 71.37 Infrastructure / Ownership Matrix

| Capability | Creates ownership? | Boundary |
| --- | --- | --- |
| AWS/IAM control | No. | Infrastructure non-authority. |
| GitHub control | No. | Repository control non-authority. |
| Database/storage control | No. | Storage control non-authority. |
| Deployment control | No. | Deployment non-authority. |
| CI/CD control | No. | Technical control non-authority. |

### 71.38 Human / Machine / AI Matrix

| Actor/process | Selected? | Creates ownership? |
| --- | --- | --- |
| Human participant | No. | No by status. |
| Machine execution | No allocation. | No. |
| Machine verification | No allocation. | No. |
| AI | No authority. | No. |
| LLM | No authority. | No. |
| MCP | No authority. | No. |

### 71.39 BE / Environment Isolation Matrix

| Context | Invalid inference | Result |
| --- | --- | --- |
| BE A ownership | BE A -> BE B. | Rejected. |
| Cross-BE actor | Actor in one BE -> another BE. | Rejected. |
| Non-production ownership | Non-production -> production. | Rejected. |
| Production ownership | Exists by implication. | NOT GRANTED. |

### 71.40 Replay Prevention Matrix

| Replay case | Required binding | Failure result |
| --- | --- | --- |
| Historical/expired/revoked/suspended/replaced/closed owner | Lifecycle/currentness. | No authority inference. |
| Cross-BE/cross-environment | BE/environment. | No ownership inference. |
| Wrong source/operation/class | Source/operation/class. | No authority inference. |
| Cross-event | Event and closure. | No authority inference. |

### 71.41 Failure / Fail-Closed Matrix

| Failure | Result |
| --- | --- |
| Missing/invalid/unverifiable/stale ownership | No authority inference. |
| Suspended ownership | No affected operation. |
| Revoked/expired/replaced/closed ownership | No authority inference. |
| Compromised ownership | No authority-increasing use. |
| Wrong source/operation/class/BE/environment/version | No authority inference. |
| Invalid or circular provenance | No authority inference. |
| Negative evidence unavailable | No authority-increasing operation. |
| SoD or independence absent | Operation stops. |
| Ownership record without assignment basis | No authority inference. |
| Technical mutation without authorization | No legitimate state change. |

### 71.42 Technology-Neutrality Matrix

| Technology or mechanism | Selected? | Must not become |
| --- | --- | --- |
| AWS / IAM / Cognito / AWS Organizations | No. | Source ownership or authority. |
| KMS / CloudHSM / Secrets Manager | No. | Credential or source authority. |
| DynamoDB / RDS / S3 / database / object store | No. | Ownership by storage. |
| Lambda / API Gateway / EventBridge / SNS / SQS / Step Functions | No. | Workflow authority. |
| CloudWatch / audit service | No. | Audit-created authority. |
| GitHub / CI/CD / repository | No. | Business ownership. |
| Ledger / blockchain / event store | No. | Current authority by history alone. |
| Schema / API / runtime / workflow / deployment | No. | Authority. |

### 71.43 Unresolved-Dependency Matrix

| Order | Unresolved decision | Depends on |
| --- | --- | --- |
| 1 | Concrete source owner. | Source ownership assignment authority governance. |
| 2 | Concrete source ownership participant. | Participant governance. |
| 3 | Concrete source authorizer. | Accountable authorization governance. |
| 4 | Concrete establishment participant. | Establishment realization. |
| 5 | Concrete lifecycle participant. | Lifecycle realization. |
| 6 | Concrete mutation participant. | Producer realization. |
| 7 | Concrete custodian. | Custody realization. |
| 8 | Concrete verifier. | Verification realization. |
| 9 | Concrete negative-evidence participant. | Negative-evidence realization. |
| 10 | Concrete suspension participant. | Suspension realization. |
| 11 | Concrete revocation participant. | Revocation realization. |
| 12 | Concrete replacement participant. | Replacement governance. |
| 13 | Concrete audit participant. | Audit governance. |
| 14 | Concrete reconciliation participant. | Reconciliation governance. |
| 15 | Concrete closure participant. | Closure governance. |
| 16 | Concrete provenance participant. | Provenance governance. |
| 17 | Concrete Assignment Authority Source. | Source realization. |
| 18 | Concrete Assignment Authority participant. | Assignment Authority participant governance. |
| 19 | Concrete recovery responsibility participants. | Responsibility participant realization. |
| 20 | Participant categories/count/quorum. | Participant governance. |
| 21 | Human/machine allocation. | Responsibility realization. |
| 22 | Identity/credential realization. | Identity and credential governance. |
| 23 | Persistence/schema/API/workflow/runtime. | Technology-neutral semantic governance. |
| 24 | Technology/cryptography/deployment. | Separate realization governance. |
| 25 | Production source/source ownership/Assignment Authority/participants/authority. | Separate production governance. |

## 72. Normative Invariants

The following invariants are normative:

1. Source ownership != source authority.
2. Source ownership != Assignment Authority Source.
3. Source ownership != Assignment Authority.
4. Source ownership != responsibility ownership.
5. Source ownership != accountable authorization.
6. Source ownership != establishment authority.
7. Source ownership != mutation authority.
8. Source ownership != mutation capability.
9. Source ownership != custody.
10. Source ownership != verification.
11. Source ownership != audit.
12. Source ownership != reconciliation.
13. Source ownership != revocation authority.
14. Source ownership != restoration authority.
15. Source ownership != replacement authority.
16. Source ownership != root.
17. Source ownership != Recovery Authority.
18. Source ownership != TAB.
19. Source ownership != successor authority.
20. Source ownership != authentication.
21. Source ownership != identity.
22. Source ownership != credential.
23. Source ownership != infrastructure control.
24. Source ownership != organizational status.
25. Source ownership != record ownership.
26. Source ownership != AI/LLM/MCP.
27. Technical ownership != business authority.
28. Accountability != automatic authorization.
29. Storage control != authority.
30. Mutation control != authorization.
31. Request != authorization.
32. Qualification != authorization.
33. Accountable owner != automatic authorizer.
34. Establishment responsibility != establishment authority.
35. Technical establishment success != legitimacy.
36. Established source != currently usable automatically.
37. Currentness determination != authority creation.
38. Mutation owner != authorizer.
39. Failed authorization -> no state change.
40. Verification != authorization.
41. Negative-evidence ownership != restoration.
42. Suspension != restoration.
43. Revocation ownership != restoration authority.
44. Replacement cannot self-legitimize.
45. Audit != authorization.
46. Reconciliation != authority creation.
47. Closure != authority creation.
48. Provenance responsibility != terminating authority.
49. Ownership cannot self-assign legitimacy.
50. Future owner cannot legitimize own initial ownership.
51. Ownership assignment requires governed authority basis.
52. Compromised owner cannot self-restore.
53. Compromised owner cannot self-replace.
54. Unavailable != compromised.
55. Unavailability creates no fallback authority.
56. Historical owner record != current responsibility.
57. Stale ownership != current ownership.
58. Suspended ownership != current exercisable ownership where applicable.
59. Revoked ownership != current ownership.
60. Expired ownership != current ownership.
61. Replaced ownership != current ownership.
62. Closed ownership != current ownership.
63. Current revocation dominates stale positive ownership evidence.
64. Ownership provenance must terminate.
65. Ownership provenance must be non-circular.
66. Ownership cannot be own terminating basis.
67. Different people != independent control automatically.
68. Different identities != independent control automatically.
69. Different credentials != independent control automatically.
70. Different systems != independent control automatically.
71. Logical responsibility separation != participant count.
72. No universal dual approval.
73. No universal maker/checker.
74. No universal two-person rule.
75. No universal quorum.
76. Participant count unresolved/not selected.
77. Quorum unresolved/not selected.
78. Root != default source owner.
79. Recovery Authority != default source owner.
80. TAB != source owner.
81. Assignment Authority != source owner automatically.
82. Responsibility owner != source owner automatically.
83. Authentication != source ownership.
84. Identity != source ownership.
85. Credential possession != source ownership.
86. Organizational status != source ownership.
87. AWS/IAM/GitHub/database/deployment control != source ownership.
88. Machine execution != business ownership.
89. AI/LLM/MCP != authoritative source owner.
90. BE A ownership != BE B ownership.
91. Non-production ownership != production ownership.
92. Ownership must be minimum necessary.
93. Ownership must be lifecycle-bound.
94. Ownership must be provenance-bound.
95. Ownership must be operation-bound where required.
96. Ownership must be responsibility-class-bound where required.
97. Ownership must be BE-bound.
98. Ownership must be environment-bound.
99. Ownership must be governance-version-bound.
100. Historical ownership cannot be replayed.
101. Required negative evidence unavailable -> no authority increase.
102. Required SoD absent -> operation stops.
103. Required independence absent -> operation stops.
104. Ownership record without legitimate assignment basis -> no authority inference.
105. Technical mutation without legitimate authorization != legitimate state change.
106. Production authority remains NOT GRANTED.

## 73. Unresolved Decisions

The following decisions remain unresolved:

1. Concrete source owner.
2. Concrete source ownership participant.
3. Concrete source authorizer.
4. Concrete establishment participant.
5. Concrete lifecycle participant.
6. Concrete mutation participant.
7. Concrete custodian.
8. Concrete verifier.
9. Concrete negative-evidence participant.
10. Concrete suspension participant.
11. Concrete revocation participant.
12. Concrete replacement participant.
13. Concrete audit participant.
14. Concrete reconciliation participant.
15. Concrete closure participant.
16. Concrete provenance participant.
17. Concrete Assignment Authority Source.
18. Concrete Assignment Authority participant.
19. Concrete recovery responsibility participants.
20. Participant categories.
21. Participant count.
22. Quorum.
23. Human/machine allocation.
24. Identity realization.
25. Credential realization.
26. Persistence.
27. Schema.
28. API.
29. Workflow.
30. Runtime.
31. Technology.
32. Cryptography.
33. Deployment.
34. Production source.
35. Production source ownership.
36. Production Assignment Authority.
37. Production participants.
38. Production authority.

This artifact does not resolve these decisions.

## 74. Downstream Dependency

The immediate downstream dependency after this artifact is:

```text
Trusted Authorization Recovery Assignment Authority
Source Ownership Assignment Authority Governance Review
```

That review is not performed by this artifact.

## 75. Participant Neutrality

This artifact does not select source owner, source administrator, source
authorizer, source establishment owner, source lifecycle owner, source mutator,
source custodian, source verifier, revocation owner, replacement owner, closure
owner, Assignment Authority holder, responsibility holder, person, team,
office, role, service, organization, founder, CEO, executive, board, employee,
contractor, security team, developer, auditor, committee, external party, or
vendor.

Participant categories, participant count, and quorum remain unresolved.

## 76. Technology Neutrality

This artifact does not select AWS, IAM, Cognito, AWS Organizations, KMS,
CloudHSM, Secrets Manager, DynamoDB, RDS, S3, Lambda, API Gateway, EventBridge,
SNS, SQS, Step Functions, CloudWatch, GitHub, CI/CD, database, object store,
event store, ledger, blockchain, identity provider, hardware token, schema,
API, runtime, workflow, or deployment.

Technology references appear only as explicit non-selection, non-authority,
threat, matrix, or unresolved-dependency examples.

## 77. Credential / Cryptographic Neutrality

This artifact does not select credential, password, token, key, certificate,
signature scheme, hash algorithm, encryption algorithm, PKI, key hierarchy, HSM
topology, threshold cryptography, secret sharing, multisig, escrow, or any
credential or cryptographic mechanism.

## 78. No Implementation

This artifact does not create source code, tests, runtime models, dataclasses,
enums, persistence, schema, database, API, workflow, IAM, credentials, AWS
resources, deployment, or implementation.

The implementation repository remains frozen at:

```text
73d6f993e2731e55709d02413d3b0bb0ba350091
```

## 79. Production Authority

PRODUCTION AUTHORITY: NOT GRANTED

This artifact does not grant or select:

- production source owner;
- production source;
- production Assignment Authority;
- production responsibility owner;
- production participant;
- production root;
- production Recovery TAB;
- production Recovery Authority;
- production successor;
- production restoration;
- production credential;
- production technology; or
- production implementation.

## 80. Governance Decision Summary

This artifact formalizes:

- MODEL F - HYBRID BOUNDED SOURCE OWNERSHIP;
- RELATIONSHIP E - HYBRID BOUNDED OWNERSHIP / AUTHORITY RELATIONSHIP;
- OVERLAP E - HYBRID BOUNDED OVERLAP / INDEPENDENCE;
- SOURCE OWNERSHIP != SOURCE AUTHORITY;
- ACCOUNTABILITY != AUTOMATIC AUTHORIZATION;
- 18 logical source ownership responsibility classes;
- request, qualification, accountable authorization, establishment,
  activation/reliance, lifecycle, currentness, mutation/producer, custody,
  verification, negative-evidence, suspension, revocation, replacement, audit,
  reconciliation, closure, and provenance/dependency responsibilities;
- ownership establishment and initial ownership non-circularity;
- ordinary ownership change conditions;
- compromised and unavailable owner handling;
- ownership lifecycle/currentness/suspension/revocation/replacement/closure;
- ownership provenance and terminating provenance;
- beneficiary-conflict and common-mode controls;
- MODEL G - HYBRID OPERATION-SPECIFIC SoD;
- hybrid overlap and independence;
- participant count and quorum unresolved/not selected;
- root, Recovery Authority, TAB, Assignment Authority, responsibility
  ownership, authentication, identity, credential, organizational status,
  infrastructure, human/machine, AI/LLM/MCP, Business Entity, and environment
  boundaries;
- governance-version binding;
- replay prevention;
- minimum necessary ownership;
- authority-direction sensitivity;
- fail-closed semantics;
- 72-threat threat model;
- 43 required matrices;
- 106 normative invariants;
- unresolved decisions;
- downstream dependency;
- participant, technology, credential, and cryptographic neutrality; and
- production authority not granted.

## 81. Closeout

This artifact creates exactly one governance document.

It creates no implementation authority and no production authority.

It does not perform the downstream review.

The next governed step is the read-only review separately authorized for:

```text
Trusted Authorization Recovery Assignment Authority
Source Ownership Assignment Authority Governance Review
```

PRODUCTION AUTHORITY: NOT GRANTED
