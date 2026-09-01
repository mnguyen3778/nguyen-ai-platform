# Trusted Authorization Recovery Assignment Authority Source Realization Governance v1

## 1. Status

This document is a governance artifact for the Nguyen AI Platform Trusted
Authorization domain.

Status: DRAFT FOR HUMAN REVIEW.

Governance checkpoint:

```text
06b637cb34c0135ef3b813b2470709ecfff30eeb
```

Implementation checkpoint remains frozen:

```text
73d6f993e2731e55709d02413d3b0bb0ba350091
```

PRODUCTION AUTHORITY: NOT GRANTED

This artifact does not implement, modify files outside this artifact, modify
the implementation repository, commit, tag, push, deploy, touch AWS resources,
select technology, select credentials, select cryptography, create persistence,
create schema, create API, create workflow, create runtime, select participants,
select participant categories, select participant count, select quorum,
establish universal dual approval, establish universal maker/checker, create a
universal two-person rule, create break-glass, instantiate TAB, activate
Recovery Authority, establish standing root, establish successor, or authorize
restoration.

## 2. Purpose

This artifact governs the abstract realization model for the source from which
bounded Recovery Assignment Authority may derive.

It defines what makes an Assignment Authority Source legitimate without
selecting the concrete source, source owner, participant, technology, identity,
credential, cryptographic mechanism, runtime, persistence, or production
authority.

The purpose is to prevent Recovery Assignment Authority from deriving from a
circular, self-authorizing, standing, universal, or hidden super-admin source.

## 3. Scope

This artifact governs:

- the conceptual Assignment Authority Source model;
- source legitimacy requirements;
- source derivation from governed terminating bases;
- ordinary and exceptional source derivation;
- source lifecycle, currentness, revocation, suspension, expiration,
  replacement, compromise, and closure;
- source scope, provenance, establishment, use, mutation, verification,
  evidence, custody, audit, and reconciliation;
- source fail-closed semantics;
- source threat model;
- source matrices;
- source invariants; and
- downstream dependency selection.

## 4. Non-Scope

This artifact does not:

- select a concrete Assignment Authority Source;
- select a source owner, source participant, source holder, source authorizer,
  source mutator, source verifier, source custodian, source auditor, or source
  revocation owner;
- select a concrete Assignment Authority participant;
- select concrete Recovery Responsibility participants;
- select participant category;
- select participant count;
- select quorum;
- create universal dual approval;
- create universal maker/checker;
- create a universal two-person rule;
- create break-glass;
- instantiate TAB;
- activate Recovery Authority;
- establish root;
- establish successor;
- authorize restoration;
- select identity provider;
- select credential;
- select cryptography;
- select technology;
- create persistence, schema, API, workflow, or runtime;
- create implementation; or
- grant production authority.

## 5. Authority

This artifact has governance drafting authority only. It records the source
realization model selected by the preceding read-only governance review.

It does not create runtime authority, administrative authority, Assignment
Authority, Assignment Authority Source, Recovery Authority, root authority,
successor authority, restoration authority, credential authority, or production
authority.

## 6. Predecessor Governance

This artifact is controlled by repository governance, including:

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

- MODEL F - HYBRID BOUNDED ASSIGNMENT AUTHORITY;
- MODEL F - HYBRID BOUNDED OWNERSHIP REALIZATION;
- RELATIONSHIP E - HYBRID BOUNDED OWNERSHIP RELATIONSHIP;
- MODEL G - HYBRID OPERATION-SPECIFIC SoD;
- SAME TAB GOVERNANCE MODEL != SAME TAB INSTANCE;
- TAB != ROOT;
- TAB != AUTHENTICATION AUTHORITY;
- TAB != INFRASTRUCTURE AUTHORITY;
- TAB != ORGANIZATIONAL STATUS;
- TAB != CREDENTIAL POSSESSION;
- TAB != MACHINE EVIDENCE ALONE;
- Recovery Authority is event-specific, bounded, non-standing,
  lifecycle-bound, provenance-bound, scope-bound, and closure-bound;
- root is bounded and non-standing; and
- production authority remains NOT GRANTED.

## 7. Selected Source Model

The selected source model is:

```text
MODEL F - HYBRID BOUNDED AUTHORITY-SOURCE REALIZATION
```

This model combines:

- bounded Administrative Authority derivation for legitimate ordinary
  operations where governance permits;
- TAB or another independently terminating governed basis for exceptional
  recovery where required;
- event-sensitive source derivation;
- responsibility-class sensitivity;
- operation sensitivity;
- authority-direction sensitivity;
- lifecycle/currentness;
- finite non-circular provenance;
- revocation;
- suspension;
- expiration;
- compromise handling;
- replacement;
- closure;
- operation-specific SoD;
- beneficiary-conflict controls;
- common-mode analysis;
- Business Entity isolation;
- environment isolation;
- governance-version binding;
- minimum necessary authority;
- fail-closed behavior;
- no universal standing source; and
- no concrete source selection.

## 8. Selected Derivation Model

The selected derivation model is:

```text
DERIVATION E - HYBRID BOUNDED DERIVATION
```

This artifact does not establish TAB-direct-only derivation.

This artifact does not establish Administrative-Authority-only derivation.

Legitimate source derivation depends on governed context, authority direction,
ordinary or exceptional condition, provenance, lifecycle, scope, Business
Entity, environment, governance version, compromise state, and applicable SoD.

## 9. Ordinary / Exceptional Relationship

The selected ordinary / exceptional relationship is:

```text
RELATIONSHIP D - HYBRID BOUNDED ORDINARY / EXCEPTIONAL SOURCE RELATIONSHIP
```

Ordinary, valid, uncompromised administrative operations may derive through
bounded Administrative Authority only where all governing requirements are
satisfied.

Exceptional recovery, compromise, invalid provenance, source failure, root or
Recovery Authority containment, or other conditions requiring independent
termination may require TAB or another already-governed independent terminating
basis.

This artifact does not invent a new ultimate authority category.

## 10. Model Rationale

Repository governance rejects a standing central source because it would create
hidden super-admin and root-equivalence risk.

Repository governance rejects TAB-direct-only as a universal rule because
ordinary administration is not always exceptional recovery and because the same
TAB governance model does not mean the same TAB instance.

Repository governance rejects Administrative-Authority-only because bounded
Administrative Authority must not become universal source authority and cannot
repair compromise or circular provenance by itself.

Repository governance rejects responsibility-class-only and event-only models
as complete models because source legitimacy depends on responsibility class,
operation, authority direction, lifecycle, provenance, Business Entity,
environment, currentness, compromise, and SoD.

The hybrid bounded model fits the predecessor decisions by allowing ordinary
bounded derivation where valid, requiring independently terminating provenance
where exceptional recovery requires it, preserving finite termination, and
rejecting universal source, universal participant count, quorum, universal dual
approval, universal maker/checker, break-glass, standing root, standing
Recovery Authority, and production authority.

## 11. Definitions

| Term | Governance meaning | Boundary |
| --- | --- | --- |
| Assignment Authority Source | Governed legitimacy basis from which bounded Recovery Assignment Authority derives. | Not the concrete source, record, mechanism, identity, credential, or participant. |
| Bounded Recovery Assignment Authority | Governed authority to authorize assignment-related operations within scope. | Derives from source; not self-legitimizing. |
| Governed terminating basis | Already-governed non-circular basis in which authority-producing derivation terminates. | Not invented here. |
| Bounded Administrative Authority | Existing governed administrative authority that may support ordinary derivation when current and scoped. | Not universal source. |
| TAB | Terminating Authority Basis model or instance where governed. | Not root, not standing universal authority, not automatically source. |
| Source evidence | Evidence supporting source legitimacy. | Evidence != source legitimacy. |
| Source record | Record claiming or documenting source state. | Record != authority source. |
| Source holder | Future participant or realization associated with source use. | Not selected here. |
| Source owner | Future logical ownership over source processes. | Not selected here. |
| Source mutator | Future executor of source state mutation. | Not selected here; mutator != authorizer. |
| Source verifier | Future verifier of source state. | Not selected here; verifier != authority source. |
| Source custodian | Future custodian of source evidence. | Not selected here; custody != authority. |
| Source auditor | Future audit responsibility. | Not selected here; audit evidence != authority source. |

## 12. Authority Chain

The conceptual chain is:

```text
GOVERNED TERMINATING BASIS
            ->
BOUNDED ASSIGNMENT AUTHORITY SOURCE
            ->
BOUNDED RECOVERY ASSIGNMENT AUTHORITY
            ->
GOVERNED RESPONSIBILITY OWNERSHIP / ASSIGNMENT
            ->
AUTHORIZED MUTATION
            ->
VERIFICATION / AUDIT / RECONCILIATION / CLOSURE
```

Every authority-producing transition in this chain must be governed, current,
scoped, provenance-valid, revocation-aware, lifecycle-bound,
Business-Entity-bound where applicable, environment-bound,
governance-version-bound, and non-circular.

## 13. Fundamental Separations

The following separations are normative:

```text
ASSIGNMENT AUTHORITY SOURCE != ASSIGNMENT AUTHORITY
ASSIGNMENT AUTHORITY SOURCE != ASSIGNED RESPONSIBILITY
ASSIGNMENT AUTHORITY SOURCE != RESPONSIBILITY OWNER
ASSIGNMENT AUTHORITY SOURCE != MUTATION MECHANISM
ASSIGNMENT AUTHORITY SOURCE != ASSIGNMENT RECORD
ASSIGNMENT AUTHORITY SOURCE != AUTHENTICATION
ASSIGNMENT AUTHORITY SOURCE != IDENTITY
ASSIGNMENT AUTHORITY SOURCE != CREDENTIAL
ASSIGNMENT AUTHORITY SOURCE != INFRASTRUCTURE AUTHORITY
ASSIGNMENT AUTHORITY SOURCE != ORGANIZATIONAL STATUS
ASSIGNMENT AUTHORITY SOURCE != RECOVERY AUTHORITY
ASSIGNMENT AUTHORITY SOURCE != ROOT
ASSIGNMENT AUTHORITY SOURCE != SUCCESSOR AUTHORITY
ASSIGNMENT AUTHORITY SOURCE != RESTORATION AUTHORITY
ASSIGNMENT AUTHORITY SOURCE != MACHINE EVIDENCE
ASSIGNMENT AUTHORITY SOURCE != AUDIT EVIDENCE
ASSIGNMENT AUTHORITY SOURCE != AI / LLM / MCP
RECORD OF AUTHORITY != SOURCE OF AUTHORITY
TECHNICAL ABILITY TO MUTATE != AUTHORITY TO AUTHORIZE
AUTHENTICATION SUCCESS != BUSINESS AUTHORITY
```

## 14. Source Definition

Assignment Authority Source means the governed legitimacy basis from which
bounded Recovery Assignment Authority derives.

It is the source of legitimacy, not evidence of legitimacy, record of
legitimacy, holder of authority, owner, executor, mutator, verifier, custodian,
or auditor.

The word "source" in this artifact must not mean merely database, file, IAM
role, credential, identity, account, API, record, technical service, runtime, or
repository.

## 15. Source Legitimacy Requirements

An Assignment Authority Source is legitimate only when all applicable
requirements are satisfied:

- governed basis;
- finite terminating provenance;
- non-circularity;
- currentness;
- lifecycle validity;
- operation applicability;
- responsibility-class applicability;
- scope;
- target;
- Business Entity;
- environment;
- governance version;
- revocation status;
- suspension status;
- expiration status;
- replacement status;
- closure status;
- compromise status where applicable;
- SoD;
- beneficiary-conflict controls;
- common-mode dependency analysis;
- auditability; and
- termination.

No missing requirement may be satisfied by convenience, title, status,
technical control, possession of credentials, successful authentication, machine
evidence alone, audit evidence alone, or AI/LLM/MCP output.

## 16. Terminating Basis

Every authority-producing source derivation must terminate in an already
governed legitimate basis.

This artifact permits the following conceptual distinction:

- bounded Administrative Authority ultimately supported by legitimate
  terminating provenance for ordinary valid operations; and
- TAB or another already-governed independent terminating relationship where
  exceptional recovery requires it.

This artifact does not invent a new root, instantiate TAB, create an ultimate
authority category, or make Assignment Authority Source its own terminating
basis.

## 17. TAB Relationship

```text
TAB != ASSIGNMENT AUTHORITY SOURCE AUTOMATICALLY.
```

A TAB may establish or support a bounded source without remaining standing.

```text
SAME TAB GOVERNANCE MODEL != SAME TAB INSTANCE.
```

This artifact does not instantiate TAB.

This artifact does not require every ordinary administrative assignment to use
a new TAB instance unless repository governance separately requires it.

## 18. Administrative Authority Relationship

```text
ADMINISTRATIVE AUTHORITY != UNIVERSAL ASSIGNMENT AUTHORITY SOURCE.
```

Bounded Administrative Authority may participate in ordinary source derivation
only when it is:

- current;
- provenance-valid;
- scope-valid;
- operation-valid;
- responsibility-class-valid;
- Business-Entity-valid;
- environment-valid;
- governance-version-valid;
- lifecycle-valid;
- not suspended;
- not revoked;
- not expired;
- not compromised where relevant;
- supported by required negative evidence; and
- compliant with applicable SoD.

Administrative Authority must not become universal source, super-admin,
standing root, Recovery Authority, restoration authority, or production
authority by implication.

## 19. Initial Assignment

```text
FUTURE RESPONSIBILITY HOLDER
    CANNOT
CREATE THE LEGITIMACY OF ITS OWN INITIAL ASSIGNMENT SOURCE.
```

Initial assignment requires independently legitimate terminating provenance.

No concrete source is selected.

## 20. Ordinary Assignment

Ordinary assignment may derive through bounded Administrative Authority only
where:

- ordinary governance remains legitimate;
- the Administrative Authority is current and scoped;
- no relevant compromise exists;
- source provenance is valid;
- lifecycle is valid;
- Business Entity and environment binding are valid;
- governance version is supported;
- required negative evidence is available;
- applicable SoD is satisfied; and
- the source does not expand beyond minimum necessary authority.

Ordinary assignment does not grant standing administrative authority and does
not convert Administrative Authority into super-admin.

## 21. Exceptional Recovery

Exceptional recovery applies only where ordinary administrative provenance is
insufficient, unavailable in a way that defeats legitimate ordinary action,
compromised, circular, invalid, or otherwise governed as requiring independent
termination.

Exceptional recovery must terminate independently where existing governance
requires it.

This artifact does not instantiate Recovery TAB, activate Recovery Authority,
authorize restoration, establish root, or establish successor.

## 22. Unavailability vs Compromise

```text
UNAVAILABLE != COMPROMISED.
```

Benign unavailability does not automatically invalidate provenance.

Compromise does not permit the compromised authority, source, or dependency to
self-repair.

Neither unavailability nor compromise creates hidden fallback authority.

## 23. Compromise Containment

Compromise analysis must evaluate whether compromise affects:

- Assignment Authority;
- Assignment Authority Source;
- terminating basis;
- Administrative Authority;
- identity authority;
- infrastructure;
- evidence producer;
- evidence custodian;
- verifier;
- mutator;
- revocation dependency; or
- common-mode dependency.

Compromised authority cannot establish its own replacement legitimacy.

Where compromise affects a required basis, authority-increasing use fails
closed until an independent governed basis is established.

## 24. Source Lifecycle

Source lifecycle is conceptual and includes:

- PROPOSED;
- ESTABLISHED;
- CURRENT;
- SUSPENDED;
- EXPIRED;
- REVOKED;
- REPLACED;
- COMPROMISED;
- CLOSED; and
- HISTORICAL.

This artifact does not implement a state machine.

## 25. Source Currentness

```text
ONLY CURRENT, VALID, PROVENANCE-VALID, IN-SCOPE SOURCE
MAY SUPPORT ASSIGNMENT AUTHORITY.
```

Historical, stale, revoked, suspended, expired, replaced, compromised, closed,
or unverifiable source cannot support authority-increasing use.

Historical legitimacy does not establish current authority.

## 26. Source Revocation

```text
CURRENT REVOCATION
    DOMINATES
STALE POSITIVE SOURCE EVIDENCE.
```

```text
REVOCATION SOURCE UNAVAILABLE
    !=
VERIFIED NOT REVOKED.
```

A revoked source cannot support new Assignment Authority.

## 27. Source Suspension

Suspension is distinct from revocation.

```text
SOURCE SUSPENSION != SOURCE RESTORATION.
```

A suspended source cannot support operations within the suspension scope.

Suspension does not grant restoration authority.

## 28. Source Expiration

```text
EXPIRED SOURCE != CURRENT SOURCE.
```

Expiration ends current source usability within the expired scope.

There is no automatic renewal, automatic extension, or convenience revival.

## 29. Source Replacement

Source replacement must not permit:

- self-successor source;
- compromised self-replacement;
- provenance laundering;
- hidden root;
- hidden Recovery Authority;
- hidden restoration authority; or
- hidden successor authority.

Replacement must have independent legitimacy where compromise, beneficiary
conflict, successor risk, or common-mode dependency requires it.

## 30. Source Closure

Closure prevents temporary or event-specific source authority from remaining
standing.

Closure must address:

- exercisability termination;
- Assignment Authority termination where applicable;
- responsibility-currentness impact;
- negative evidence;
- audit;
- reconciliation;
- historical evidence; and
- replay prevention.

Closed source evidence may remain for audit and lineage, but not as exercisable
source authority.

## 31. Source Scope

Source authority is minimum necessary and must be bounded by applicable:

- operation;
- responsibility class;
- target;
- scope;
- Business Entity;
- environment;
- governance version;
- lifecycle;
- event;
- authority direction;
- currentness; and
- provenance.

The following inference is rejected:

```text
VALID FOR ONE ASSIGNMENT
    ->
VALID FOR ALL ASSIGNMENTS.
```

Scope must not silently inherit beyond governed need.

## 32. Source Provenance

Source provenance must conceptually include:

- terminating basis;
- derivation path;
- predecessor source;
- governing artifact/version;
- operation;
- responsibility class;
- target;
- scope;
- Business Entity;
- environment;
- lifecycle;
- event;
- currentness;
- suspension;
- revocation;
- expiration;
- replacement;
- compromise;
- closure; and
- dependency provenance.

This artifact does not define schema or persistence.

## 33. Provenance Termination

The following rule is normative:

```text
EVERY AUTHORITY-PRODUCING DERIVATION MUST TERMINATE IN A GOVERNED,
NON-CIRCULAR BASIS THAT DOES NOT DEPEND ON THE AUTHORITY BEING
CREATED FOR ITS OWN LEGITIMACY.
```

Infinite and circular authority chains are rejected.

## 34. Source Establishment

```text
AUTHORITY TO ESTABLISH SOURCE != AUTHORITY TO USE SOURCE.
SOURCE ESTABLISHMENT != SOURCE MODIFICATION.
```

A participant or process able to establish source evidence does not
automatically gain authority to exercise the source.

## 35. Source Authorization vs Mutation

```text
AUTHORIZATION TO ESTABLISH / CHANGE SOURCE
    !=
TECHNICAL MUTATION OF SOURCE STATE.
```

Technical mutation cannot manufacture legitimacy.

Successful mutation without legitimate source authorization remains
unauthorized and does not become legitimate through later audit or
reconciliation.

## 36. Source Verification

Before relying on a source, verification must establish where applicable:

- correct source class/model;
- current;
- provenance-valid;
- not revoked;
- not suspended;
- not expired;
- not replaced;
- not closed;
- not compromised where applicable;
- correct operation;
- correct responsibility class;
- correct target;
- correct scope;
- correct Business Entity;
- correct environment;
- supported governance version;
- required SoD;
- required independence; and
- required negative evidence.

Verification does not create authority.

## 37. Source Evidence

```text
EVIDENCE OF SOURCE LEGITIMACY
    !=
SOURCE OF LEGITIMACY.
```

Machine-verifiable evidence may support reference, integrity, version, scope,
lifecycle, provenance, currentness, environment, and verification.

Machine evidence alone cannot self-authorize.

## 38. Source Record

```text
SOURCE RECORD != AUTHORITY SOURCE.
```

A record cannot establish its own legitimacy.

A record claiming that a source may establish Assignment Authority requires
independent governed provenance.

## 39. Source Custody

```text
CUSTODY != AUTHORITY
CUSTODY != ASSIGNMENT AUTHORITY
CUSTODY != SOURCE LEGITIMACY
```

A custodian may preserve evidence without becoming the authority source.

## 40. Source Audit

```text
AUDIT EVIDENCE != AUTHORITY SOURCE.
```

Audit can preserve what occurred. Audit cannot retroactively legitimize invalid
source establishment, invalid source use, or invalid Assignment Authority
creation.

## 41. Source Reconciliation

```text
RECONCILIATION != AUTHORITY CREATION
RECONCILIATION != RESTORATION
```

Reconciliation cannot launder invalid source state into legitimate source
state.

## 42. Source Restoration Boundary

```text
SOURCE REVOCATION != SOURCE RESTORATION
SOURCE SUSPENSION != SOURCE RESTORATION
SOURCE REPLACEMENT != SOURCE RESTORATION
SOURCE VERIFICATION != SOURCE RESTORATION
```

This artifact does not authorize restoration.

## 43. Authority Direction

Authority direction changes source sensitivity.

Authority-increasing / enabling operations include:

- initial assignment;
- authority-bearing assignment;
- reactivation;
- restoration; and
- successor establishment.

Authority-reducing / blocking operations include:

- suspension;
- revocation;
- emergency reduction; and
- closure.

Mixed operations include:

- reassignment; and
- replacement.

```text
REDUCTION AUTHORITY != RESTORATION AUTHORITY.
```

## 44. Beneficiary Conflict

Operation-specific controls are required where the source beneficiary is:

- Assignment Authority;
- responsibility owner;
- Recovery Authority;
- predecessor source;
- successor candidate;
- mutator;
- verifier;
- custodian; or
- administrator.

This artifact does not create universal separation. It requires
operation-specific beneficiary-conflict analysis.

## 45. Common-Mode Dependency

Independence is based on underlying control and provenance, not labels or
headcount.

Common-mode analysis must consider shared dependency on:

- terminating basis;
- Administrative Authority;
- identity authority;
- credentials;
- infrastructure;
- evidence producer;
- custodian;
- verifier;
- mutator;
- organizational control;
- Recovery Authority; and
- revocation dependency.

Different people, accounts, identities, credentials, systems, or labels do not
automatically prove independence.

## 46. Operation-Specific SoD

The following predecessor model is preserved:

```text
MODEL G - HYBRID OPERATION-SPECIFIC SoD.
```

This artifact does not introduce:

- universal dual approval;
- universal maker/checker;
- universal two-person rule;
- universal quorum; or
- fixed participant count.

Logical responsibility separation does not imply participant count.

## 47. Root Containment

```text
ASSIGNMENT AUTHORITY SOURCE != ROOT.
```

The following inference is rejected:

```text
ROOT = DEFAULT ASSIGNMENT AUTHORITY SOURCE.
```

Root remains bounded and non-standing.

## 48. Recovery Authority Containment

```text
ASSIGNMENT AUTHORITY SOURCE != RECOVERY AUTHORITY.
```

Recovery Authority cannot automatically:

- establish its own source;
- validate its own source;
- extend its source;
- suppress source revocation;
- replace source;
- restore source; or
- establish successor source.

## 49. TAB Containment

```text
TAB != ROOT
TAB != STANDING UNIVERSAL AUTHORITY
```

If TAB participates in source derivation, its use remains bounded and does not
create permanent exercisable root authority.

## 50. Successor Boundary

```text
SOURCE REPLACEMENT != ROOT SUCCESSION
SOURCE REPLACEMENT != RECOVERY AUTHORITY SUCCESSION
SOURCE REPLACEMENT != SUCCESSOR AUTHORITY ESTABLISHMENT
```

This artifact does not establish successor.

## 51. Authentication / Identity / Credential Boundary

```text
AUTHENTICATION != AUTHORIZATION
IDENTITY != AUTHORITY SOURCE
CREDENTIAL POSSESSION != AUTHORITY SOURCE
```

No identity provider or credential is selected.

## 52. Organizational Status Boundary

Status alone does not create source legitimacy. This includes:

- founder;
- owner;
- CEO;
- executive;
- board;
- employee;
- contractor;
- security;
- administrator;
- developer; and
- auditor.

No concrete participant is selected.

## 53. Infrastructure Boundary

```text
AWS CONTROL != BUSINESS AUTHORITY SOURCE
IAM CONTROL != BUSINESS AUTHORITY SOURCE
GITHUB CONTROL != BUSINESS AUTHORITY SOURCE
DATABASE CONTROL != BUSINESS AUTHORITY SOURCE
DEPLOYMENT CONTROL != BUSINESS AUTHORITY SOURCE
```

Infrastructure capability is not source legitimacy.

## 54. Human / Machine Boundary

Human/machine allocation remains unresolved.

```text
MACHINE EXECUTION != AUTHORITY SOURCE.
```

This artifact does not allocate responsibilities to humans or machines.

## 55. AI / LLM / MCP Boundary

AI/LLM/MCP cannot independently:

- establish source;
- authorize source;
- qualify source authoritatively;
- create Assignment Authority;
- override revocation;
- determine SoD;
- replace source;
- restore source;
- establish root;
- activate Recovery Authority;
- select successor; or
- grant production authority.

AI/LLM/MCP may provide non-authoritative assistance only where separately
governed.

## 56. Business Entity Isolation

```text
BE A AUTHORITY SOURCE != BE B AUTHORITY SOURCE.
```

No cross-BE authority inference is created.

## 57. Environment Isolation

```text
NON-PRODUCTION AUTHORITY SOURCE
    !=
PRODUCTION AUTHORITY SOURCE.
```

No production authority source is selected.

## 58. Governance Version

Unsupported, obsolete, or incompatible governance version cannot remain
authoritative by convenience.

This artifact does not implement a version mechanism.

## 59. Replay Prevention

The source model must prevent:

- historical source replay;
- expired source replay;
- revoked source replay;
- replaced source replay;
- closed source replay;
- cross-BE replay;
- cross-environment replay;
- wrong-operation reuse;
- wrong-responsibility-class reuse;
- wrong-target reuse; and
- cross-event reuse.

This artifact does not select cryptography.

## 60. Fail-Closed Semantics

The following outcomes are normative:

```text
MISSING SOURCE
  -> NO ASSIGNMENT AUTHORITY
INVALID SOURCE
  -> NO ASSIGNMENT AUTHORITY
UNVERIFIABLE SOURCE
  -> NO ASSIGNMENT AUTHORITY
STALE SOURCE
  -> NO ASSIGNMENT AUTHORITY
SUSPENDED SOURCE
  -> NO ASSIGNMENT AUTHORITY WHERE APPLICABLE
REVOKED SOURCE
  -> NO ASSIGNMENT AUTHORITY
EXPIRED SOURCE
  -> NO ASSIGNMENT AUTHORITY
REPLACED SOURCE
  -> NO ASSIGNMENT AUTHORITY FROM PREDECESSOR
CLOSED SOURCE
  -> NO ASSIGNMENT AUTHORITY
COMPROMISED SOURCE
  -> NO AUTHORITY-INCREASING USE
WRONG OPERATION
  -> NO ASSIGNMENT AUTHORITY
WRONG RESPONSIBILITY CLASS
  -> NO ASSIGNMENT AUTHORITY
WRONG TARGET
  -> NO ASSIGNMENT AUTHORITY
WRONG BE
  -> NO ASSIGNMENT AUTHORITY
WRONG ENVIRONMENT
  -> NO ASSIGNMENT AUTHORITY
UNSUPPORTED GOVERNANCE VERSION
  -> NO ASSIGNMENT AUTHORITY
INVALID PROVENANCE
  -> NO ASSIGNMENT AUTHORITY
CIRCULAR PROVENANCE
  -> NO ASSIGNMENT AUTHORITY
REQUIRED NEGATIVE EVIDENCE UNAVAILABLE
  -> NO AUTHORITY-INCREASING USE
REQUIRED SoD NOT ESTABLISHED
  -> OPERATION DOES NOT PROCEED
REQUIRED INDEPENDENCE NOT ESTABLISHED
  -> OPERATION DOES NOT PROCEED
SOURCE RECORD EXISTS BUT LEGITIMACY CANNOT BE VERIFIED
  -> NO ASSIGNMENT AUTHORITY
TECHNICAL MUTATION SUCCEEDS WITHOUT LEGITIMATE SOURCE
  -> DOES NOT BECOME LEGITIMATE
```

No convenience fallback is permitted.

## 61. Threat Model

| # | Threat | Targeted invariant | Affected operation | Governance control | Fail-closed result | Unresolved dependency |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Assignment Authority declares its own source legitimate. | Assignment Authority cannot self-legitimize source. | Source validation. | Independent terminating provenance. | No Assignment Authority. | Source ownership. |
| 2 | Responsibility owner creates its own source. | Owner cannot self-create source legitimacy. | Source establishment. | Governed source authorization. | No source. | Source owner. |
| 3 | Mutator writes source record and treats it as authority. | Mutator cannot create source legitimacy. | Source mutation. | Authorization before mutation. | No legitimacy. | Source mutator. |
| 4 | Source record treated as source legitimacy. | Source record != authority source. | Source reliance. | Independent provenance. | No Assignment Authority. | Source evidence. |
| 5 | Authentication treated as authority source. | Authentication != authorization. | Source validation. | Authentication boundary. | No source authority. | Identity realization. |
| 6 | Identity treated as authority source. | Identity != authority source. | Source attribution. | Identity boundary. | No source authority. | Identity realization. |
| 7 | Credential possession treated as authority source. | Credential possession != authority source. | Source use. | Credential boundary. | No source authority. | Credential realization. |
| 8 | AWS/IAM/GitHub control treated as authority source. | Infrastructure control != business authority source. | Source mutation/use. | Infrastructure boundary. | No source authority. | Technology governance. |
| 9 | Founder/owner/CEO status treated as authority source. | Organizational title != authority source. | Source establishment. | Status boundary. | No source authority. | Participant governance. |
| 10 | Machine evidence treated as authority source. | Machine evidence != source. | Source evidence. | Evidence/source separation. | No source authority. | Evidence realization. |
| 11 | AI/LLM/MCP treated as authority source. | AI/LLM/MCP != source. | Any source operation. | AI non-authority. | No source authority. | Tool governance if any. |
| 12 | Standing central source becomes hidden super-admin. | No hidden super-admin. | All source use. | Reject standing universal source. | No universal source. | Concrete source model. |
| 13 | TAB becomes standing universal authority. | TAB != standing universal authority. | TAB/source derivation. | TAB containment. | No standing TAB source. | TAB realization. |
| 14 | Same TAB instance reused indefinitely. | Same TAB model != same TAB instance. | Recovery source derivation. | Event/currentness binding. | No replayed source. | TAB instance governance. |
| 15 | Administrative Authority becomes universal source. | Administrative Authority != universal source. | Ordinary assignment. | Scope and operation bounds. | No universal source. | Admin source realization. |
| 16 | Recovery Authority establishes its own source. | RA != Assignment Authority Source. | Recovery continuation. | RA containment. | No self-source. | Recovery lifecycle. |
| 17 | Recovery Authority validates its own source. | Source verification != source creation. | Source verification. | Independent verification where required. | No source reliance. | Source verifier. |
| 18 | Recovery Authority suppresses source revocation. | Current revocation dominates stale positive evidence. | Source revocation. | Negative evidence currentness. | No authority increase. | Revocation owner. |
| 19 | Root becomes default source. | Root != default source. | Source establishment. | Root containment. | No default source. | Root lifecycle. |
| 20 | Source establishes its own successor. | Source replacement != successor authority establishment. | Replacement. | Independent replacement basis. | No successor source. | Source replacement. |
| 21 | Compromised source replaces itself. | Compromised source cannot self-replace. | Replacement. | Compromise containment. | No replacement. | Replacement governance. |
| 22 | Compromised source restores itself. | Source revocation/suspension/replacement != restoration. | Restoration. | Restoration boundary. | No restoration. | Restoration governance. |
| 23 | Unavailable source triggers hidden fallback. | No hidden fallback. | Unavailability. | Governed replacement/recovery only. | No fallback. | Availability governance. |
| 24 | Historical source replay. | Historical source evidence != current source. | Replay. | Currentness check. | No Assignment Authority. | Source lifecycle. |
| 25 | Expired source replay. | Expired source != current source. | Replay. | Expiration check. | No Assignment Authority. | Expiration governance. |
| 26 | Revoked source replay. | Revoked source != current source. | Replay. | Revocation check. | No Assignment Authority. | Revocation source. |
| 27 | Replaced source replay. | Replaced source != current source. | Replay. | Replacement lineage. | No predecessor authority. | Replacement governance. |
| 28 | Closed-event source replay. | Closed source != current source. | Replay. | Closure binding. | No Assignment Authority. | Closure governance. |
| 29 | Source copied across BE. | BE A source != BE B source. | Cross-BE use. | BE binding. | No cross-BE authority. | BE realization. |
| 30 | Source copied across environment. | Non-production source != production source. | Cross-environment use. | Environment binding. | No production authority. | Environment governance. |
| 31 | Source reused for wrong operation. | Source operation-bound. | Source use. | Operation binding. | No Assignment Authority. | Operation taxonomy. |
| 32 | Source reused for wrong responsibility class. | Source responsibility-class-bound. | Source use. | Class binding. | No Assignment Authority. | Class governance. |
| 33 | Source reused for wrong target. | Source target-bound. | Source use. | Target binding. | No Assignment Authority. | Target semantics. |
| 34 | Source reused across recovery events. | Source event-bound where applicable. | Recovery use. | Event binding and closure. | No Assignment Authority. | Event governance. |
| 35 | Stale positive evidence overrides current revocation. | Current revocation dominates stale positive evidence. | Revocation check. | Negative evidence currentness. | No authority increase. | Negative evidence. |
| 36 | Revocation source unavailable interpreted as not revoked. | Unavailable != verified not revoked. | Revocation check. | Fail-closed negative evidence. | No authority increase. | Revocation availability. |
| 37 | Different people mask common authority dependency. | Different people != independent provenance. | SoD. | Common-mode analysis. | No independence. | Participant governance. |
| 38 | Different identities mask common authority dependency. | Different identities != independent provenance. | SoD. | Identity dependency review. | No independence. | Identity governance. |
| 39 | Different credentials mask common authority dependency. | Different credentials != independent provenance. | SoD. | Credential dependency review. | No independence. | Credential governance. |
| 40 | Different systems mask common authority dependency. | Different systems != independent provenance. | SoD. | Infrastructure dependency review. | No independence. | Technology governance. |
| 41 | Source custodian becomes authority. | Custody != source authority. | Custody. | Custody boundary. | No authority. | Custody ownership. |
| 42 | Source verifier becomes authority. | Verification != source creation. | Verification. | Verification boundary. | No authority. | Verifier ownership. |
| 43 | Source auditor becomes authority. | Audit evidence != authority source. | Audit. | Audit boundary. | No authority. | Audit ownership. |
| 44 | Source reconciler launders invalid source. | Reconciliation != authority creation. | Reconciliation. | Reconciliation boundary. | No legitimacy. | Reconciliation ownership. |
| 45 | Technical mutation launders invalid source. | Technical mutation without legitimate source does not become legitimate. | Mutation. | Authorization before mutation. | No legitimacy. | Mutation ownership. |
| 46 | Source replacement launders compromise. | Replacement cannot launder compromise. | Replacement. | Independent replacement basis. | No replacement. | Replacement governance. |
| 47 | Source derivation chain becomes circular. | Source provenance non-circular. | Derivation. | Terminating provenance. | No source. | Source realization. |
| 48 | Source derivation never reaches terminating basis. | Source provenance must terminate. | Derivation. | Finite basis required. | No source. | Terminating basis. |
| 49 | Source scope silently expands. | Minimum necessary authority. | Scope. | Scope binding. | No expanded source. | Scope governance. |
| 50 | Source valid for one BE used cross-BE. | BE isolation. | Cross-BE source use. | BE binding. | No cross-BE authority. | BE source governance. |
| 51 | Non-production source reused in production. | Environment isolation. | Production. | Environment binding. | No production authority. | Production governance. |
| 52 | Source valid for reduction reused for restoration. | Reduction authority != restoration authority. | Restoration. | Direction separation. | No restoration. | Restoration governance. |
| 53 | Source valid for one assignment becomes universal. | Source minimum necessary. | Assignment. | Operation/scope binding. | No universal source. | Assignment source scope. |
| 54 | Unsupported governance version remains authoritative. | Unsupported version cannot remain authoritative. | Source use. | Version check. | No Assignment Authority. | Version governance. |
| 55 | Source closure leaves residual authority. | Closure terminates exercisability. | Closure. | Closure verification. | No clean closure. | Closure ownership. |
| 56 | Source evidence survives closure and is replayed. | Source evidence not replayable after closure. | Replay. | Closure and lifecycle binding. | No Assignment Authority. | Evidence retention. |

## 62. Required Matrices

### 62.1 Source Model Definition Matrix

| Model | Non-circularity | Terminating provenance | Boundedness | Ordinary fit | Exceptional fit | Standing risk | Repository fit | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Model A - Standing Central Assignment Authority Source | Weak. | Weak. | Weak. | Simple. | Weak under compromise. | High. | Conflicts with no hidden super-admin. | Rejected. |
| Model B - TAB-Direct Source Model | Strong. | Strong. | Strong if event-bound. | Weak for ordinary administration. | Strong. | Medium if overused. | Useful but not universal. | Included in Model F. |
| Model C - Administrative-Authority-Derived Source Model | Medium/strong if bounded. | Requires terminating provenance. | Strong if scoped. | Strong. | Weak under compromise. | Medium if broadened. | Useful but not universal. | Included in Model F. |
| Model D - Responsibility-Class-Specific Source Model | Strong by class. | Requires basis. | Strong. | Medium. | Medium. | Low. | Useful dimension. | Included in Model F. |
| Model E - Event-Specific Terminating Source Model | Strong. | Strong. | Strong. | Weak for ordinary use. | Strong. | Low. | Useful for recovery events. | Included in Model F. |
| Model F - Hybrid Bounded Authority-Source Realization | Strong. | Strong. | Strong. | Strong. | Strong. | Low. | Best fit. | SELECTED. |
| Model G - Underdetermined | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Unknown. | Not needed. | Not selected. |

### 62.2 Source Derivation Matrix

| Derivation | Meaning | Selected? | Boundary |
| --- | --- | --- | --- |
| Derivation A - TAB-direct only | Every source derives directly from TAB. | No. | Overstates TAB requirement. |
| Derivation B - Bounded Administrative Authority only | Every source derives from administrative authority. | No. | Fails exceptional compromise cases. |
| Derivation C - Responsibility-class-specific | Source depends only on class. | No as complete model. | Useful dimension. |
| Derivation D - Event-specific | Source depends only on event. | No as complete model. | Useful for recovery. |
| Derivation E - Hybrid bounded derivation | Source depends on context, class, operation, event, direction, provenance, and lifecycle. | Yes. | No concrete source. |
| Derivation F - Underdetermined | Repository cannot decide. | No. | Not required. |

### 62.3 Ordinary / Exceptional Source Matrix

| Context | Ordinary source path | Exceptional source path | Required condition | Status |
| --- | --- | --- | --- | --- |
| Initial assignment | Not self-created. | Independent terminating basis. | Finite non-circular provenance. | Governed. |
| Ordinary assignment | Bounded Administrative Authority may support. | Not required if ordinary path valid. | Current/scoped/uncompromised. | Governed conceptually. |
| Ordinary reassignment | Bounded Administrative Authority may support. | Only if ordinary path invalid. | Lifecycle and negative evidence. | Governed conceptually. |
| Benign unavailability | Ordinary replacement where valid. | Only if ordinary path fails safely. | Unavailable != compromised. | Governed conceptually. |
| Compromise | Ordinary compromised path rejected. | Independent terminating basis required where authority increase. | Compromise containment. | Governed. |
| Recovery event | Ordinary path first if valid. | TAB or other terminating basis where required. | Event-bound. | Governed. |
| Closure | Ordinary closure where valid. | Recovery closure where event-specific. | No residual authority. | Governed. |

### 62.4 Source / Authority Boundary Matrix

| Item | Is source by itself? | May support source? | Boundary |
| --- | --- | --- | --- |
| TAB | No automatically. | Yes where governed. | TAB not standing universal authority. |
| Assignment Authority Source | Source concept. | N/A. | Must be bounded and current. |
| Assignment Authority | No. | Derives from source. | Cannot self-legitimize source. |
| Administrative Authority | No universally. | Yes if bounded/current. | Not super-admin. |
| Responsibility Owner | No. | No by ownership alone. | Owner cannot self-source. |
| Recovery Authority | No. | Only if separately governed. | Non-standing, event-bound. |
| Root | No by default. | Only if separately governed. | Root non-standing. |
| Successor | No. | Only if separately legitimate. | Source replacement != succession. |
| Restoration Authority | No. | Separately governed only. | Not created here. |
| Mutator | No. | Executes if authorized. | Mutation != authorization. |
| Verifier | No. | Verifies. | Verification != source creation. |
| Custodian | No. | Preserves evidence. | Custody != authority. |
| Auditor | No. | Preserves evidence. | Audit evidence != source. |
| Authentication Authority | No. | Identity support only. | Authentication != authorization. |
| Infrastructure Authority | No. | Technical support only. | Infrastructure != business source. |
| Credential | No. | Attribution/control evidence only. | Possession != source. |
| Machine Evidence | No. | Supports verification. | Evidence != legitimacy. |
| AI/LLM/MCP | No. | Non-authoritative assistance only. | Cannot source authority. |

### 62.5 Terminating Basis Matrix

| Basis | May terminate source derivation? | Required properties | Non-selection |
| --- | --- | --- | --- |
| Already-governed TAB | Yes where required. | Current, scoped, event-bound, provenance-valid. | No TAB instantiated. |
| Bounded Administrative Authority | Yes for ordinary valid operations if ultimately terminates. | Current, scoped, uncompromised, revocation-aware. | Not universal. |
| Other governed terminating relationship | Yes if repository governance supports. | Finite, independent, non-circular. | No new category invented. |
| Source itself | No. | N/A. | Self-termination rejected. |
| Technical record/mechanism | No. | N/A. | Record/mechanism non-authority. |

### 62.6 TAB / Source Relationship Matrix

| Relationship | Permitted conceptually? | Condition | Boundary |
| --- | --- | --- | --- |
| TAB directly supports exceptional source | Yes. | Current event-specific TAB where required. | No standing TAB. |
| TAB supports source then closes | Yes. | Closure removes exercisability. | Historical evidence only. |
| Same TAB instance reused for all events | No. | N/A. | Same model != same instance. |
| TAB becomes root | No. | N/A. | TAB != root. |
| TAB becomes universal source | No. | N/A. | TAB not standing universal authority. |
| Ordinary assignment always needs fresh TAB | Not selected. | Only if future governance requires. | No universal TAB-direct rule. |

### 62.7 Administrative Authority / Source Matrix

| Condition | Administrative source support? | Result |
| --- | --- | --- |
| Current, scoped, valid provenance, ordinary operation | May support. | Source may be valid if all checks pass. |
| Stale | No. | No Assignment Authority. |
| Revoked | No. | No Assignment Authority. |
| Suspended | No where applicable. | No Assignment Authority. |
| Expired | No. | No Assignment Authority. |
| Compromised | No authority-increasing use. | Independent basis required. |
| Wrong BE/environment | No. | No Assignment Authority. |
| Unsupported version | No. | No Assignment Authority. |
| Missing negative evidence | No authority-increasing use. | Fail closed. |
| Broad admin claim | No. | Universal source rejected. |

### 62.8 Initial Assignment Source Matrix

| Scenario | Legitimate source? | Required basis | Failure result |
| --- | --- | --- | --- |
| Future holder self-creates source | No. | Independent terminating provenance. | No source. |
| No current holder exists | Possible. | Already-governed terminating basis. | No Assignment Authority if absent. |
| Initial source record exists only as record | No. | Record provenance required. | No source. |
| Initial bounded admin path exists | Conditional. | Current terminating provenance. | No source if unverifiable. |
| Exceptional initial recovery | Conditional. | TAB or other independent basis where required. | No source if not current. |

### 62.9 Source Lifecycle Matrix

| State | May support Assignment Authority? | Evidence value | Fail-closed result |
| --- | --- | --- | --- |
| PROPOSED | No. | Proposal only. | No authority. |
| ESTABLISHED | Only if current/effective. | Establishment evidence. | No authority if not current. |
| CURRENT | Yes within scope if all checks pass. | Current source evidence. | No outside scope. |
| SUSPENDED | No where applies. | Suspension evidence. | No authority. |
| EXPIRED | No. | Historical evidence. | No authority. |
| REVOKED | No. | Negative evidence. | No authority. |
| REPLACED | No from predecessor. | Replacement lineage. | No predecessor authority. |
| COMPROMISED | No authority-increasing use. | Compromise evidence. | No authority increase. |
| CLOSED | No. | Closure evidence. | No authority. |
| HISTORICAL | No. | Audit/lineage. | No current source. |

### 62.10 Source Currentness Matrix

| Currentness condition | Current? | Required handling |
| --- | --- | --- |
| Current, valid, in scope | Potentially. | Verify provenance, SoD, negative evidence, BE, environment, version. |
| Stale | No. | Treat as historical. |
| Unverifiable | No. | No Assignment Authority. |
| Conflicting evidence | No until resolved. | Fail closed. |
| Current revocation present | No. | Revocation dominates. |
| Negative evidence unavailable | Unknown. | No authority-increasing use. |

### 62.11 Source Revocation Matrix

| Revocation state | Source usability | Required rule |
| --- | --- | --- |
| No verified revocation and source current | Conditional. | Continue full validation. |
| Revoked | None. | No Assignment Authority. |
| Revocation source unavailable | Unknown. | No authority-increasing use. |
| Stale positive evidence conflicts with current revocation | Revoked. | Current revocation dominates. |
| Revocation suppressed | Unknown/invalid. | Fail closed. |

### 62.12 Source Suspension Matrix

| Suspension state | Source usability | Restoration implication |
| --- | --- | --- |
| Not suspended and current | Conditional. | None. |
| Suspended for operation | No operation use. | No restoration. |
| Suspended for scope | No scoped use. | No restoration. |
| Suspension state unavailable | Unknown. | No authority-increasing use where required. |
| Suspension lifted | Not authorized here. | Requires separate governed basis. |

### 62.13 Source Expiration Matrix

| Expiration state | Source usability | Boundary |
| --- | --- | --- |
| Not expired and current | Conditional. | Full validation still required. |
| Expired | No. | No automatic renewal. |
| Expiration unknown | No authority-increasing use where required. | Currentness fail-closed. |
| Expiration extended by record only | No. | Record != authority. |
| Re-established after expiration | Not authorized here. | Requires new governed basis. |

### 62.14 Source Replacement Matrix

| Replacement case | Permitted conceptually? | Required control |
| --- | --- | --- |
| Ordinary lifecycle replacement | Conditional. | Current bounded source authorization. |
| Self-successor source | No sole basis. | Independent replacement basis. |
| Compromised self-replacement | No. | Independent terminating provenance. |
| Replacement after revocation | Conditional. | Revocation cannot be laundered. |
| Replacement after closure | Conditional. | New current basis required. |
| Replacement creates successor authority | No. | Successor boundary. |
| Replacement creates restoration authority | No. | Restoration boundary. |

### 62.15 Source Closure Matrix

| Closure requirement | Purpose | Failure result |
| --- | --- | --- |
| Terminate exercisability | Prevent standing source. | No clean closure. |
| End event-specific Assignment Authority | Prevent replay. | No closure reliance. |
| Update negative evidence | Block stale use. | No authority increase. |
| Complete audit | Preserve lineage. | Audit obligation remains. |
| Complete reconciliation | Resolve mismatch. | Event unresolved. |
| Preserve historical evidence as non-exercisable | Maintain lineage. | No authority from evidence. |

### 62.16 Source Scope Matrix

| Scope dimension | Required? | Invalid inference |
| --- | --- | --- |
| Operation | Yes. | One operation -> all operations. |
| Responsibility class | Yes where relevant. | One class -> all classes. |
| Target | Yes. | One target -> all targets. |
| Business Entity | Yes. | BE A -> BE B. |
| Environment | Yes. | Non-production -> production. |
| Governance version | Yes. | Old version -> current authority. |
| Lifecycle | Yes. | Historical -> current. |
| Event | Where applicable. | One event -> all events. |
| Authority direction | Yes. | Reduction -> restoration. |
| Provenance | Yes. | Record -> source. |

### 62.17 Source Provenance Matrix

| Element | Required conceptually? | Failure consequence |
| --- | --- | --- |
| Terminating basis | Yes. | No source. |
| Derivation path | Yes. | No source. |
| Predecessor source | Where applicable. | No replacement lineage. |
| Governing artifact/version | Yes. | No source under unsupported version. |
| Operation | Yes. | No operation authority. |
| Responsibility class | Yes where relevant. | No class authority. |
| Target | Yes. | No target authority. |
| Scope | Yes. | No out-of-scope authority. |
| Business Entity | Yes. | No cross-BE authority. |
| Environment | Yes. | No production inference. |
| Lifecycle | Yes. | Not current. |
| Event | Where applicable. | No cross-event replay. |
| Suspension/revocation/expiration/replacement/closure | Where applicable. | No current source if blocking. |
| Compromise | Where applicable. | No authority increase. |
| Dependency provenance | Where independence required. | No independence. |

### 62.18 Source Establishment / Use / Mutation Matrix

| Function | Creates source legitimacy by itself? | Boundary |
| --- | --- | --- |
| Establishment authorization | Only if independently governed and scoped. | Establishment != use. |
| Source use | No. | Use != modification. |
| Source modification | No without authorization. | Mutation != authorization. |
| Technical mutation | No. | Mutation success != legitimacy. |
| Verification | No. | Verification != source creation. |
| Audit/reconciliation | No. | Evidence/reconciliation non-authority. |

### 62.19 Source Verification Matrix

| Check | Required? | Failure result |
| --- | --- | --- |
| Source class/model | Yes. | No Assignment Authority. |
| Currentness | Yes. | No Assignment Authority. |
| Provenance | Yes. | No Assignment Authority. |
| Revocation/suspension/expiration/replacement/closure | Yes where applicable. | No Assignment Authority. |
| Compromise | Yes where applicable. | No authority increase. |
| Operation/class/target/scope | Yes. | No Assignment Authority. |
| BE/environment/version | Yes. | No Assignment Authority. |
| SoD/independence | Yes where required. | Operation does not proceed. |
| Negative evidence | Yes where required. | No authority increase. |

### 62.20 Source Evidence / Legitimacy Matrix

| Evidence | May prove | May create legitimacy alone? | Required check |
| --- | --- | --- | --- |
| Establishment evidence | Establishment-at-time. | No. | Current provenance. |
| Scope evidence | Boundaries. | No. | Scope currentness. |
| Lifecycle evidence | State. | No. | Currentness and negative evidence. |
| Revocation evidence | Blocking state. | Blocks where current. | Source availability. |
| Audit evidence | What occurred. | No. | Audit/source separation. |
| Machine evidence | Integrity/reference. | No. | Independent source legitimacy. |
| Historical evidence | Lineage. | No. | No replay. |

### 62.21 Source Record / Authority Matrix

| Record type | Authority by itself? | Required boundary |
| --- | --- | --- |
| Source establishment record | No. | Requires independent provenance. |
| Source lifecycle record | No. | Currentness must be verified. |
| Source scope record | No. | Scope must be governed. |
| Source replacement record | No. | Replacement basis required. |
| Source closure record | No. | Closure verification required. |
| Source audit record | No. | Audit evidence != source. |

### 62.22 Source Custody / Authority Matrix

| Custody function | Authority implication | Boundary |
| --- | --- | --- |
| Preserve source evidence | None. | Custody != authority. |
| Provide source evidence | None. | Evidence verification required. |
| Withhold evidence | Blocks validation. | No authority increase. |
| Transfer custody | None by itself. | Custody transfer != source replacement. |
| Custodian compromised | Source dependency risk. | Common-mode analysis. |

### 62.23 Source Audit / Reconciliation Matrix

| Function | May authorize source? | May restore source? | Fail-closed result |
| --- | --- | --- | --- |
| Audit | No. | No. | No audit-created legitimacy. |
| Audit failure | No. | No. | Obligation remains; no authority increase. |
| Reconciliation | No. | No. | No laundering. |
| Reconciliation mismatch | No. | No. | Source not relied upon. |
| Closure reconciliation | No future authority. | No. | No clean closure if unresolved. |

### 62.24 Beneficiary-Conflict Matrix

| Beneficiary | Conflict risk | Required control |
| --- | --- | --- |
| Assignment Authority | Self-source. | Independent source basis. |
| Responsibility owner | Self-legitimizing ownership. | Governed Assignment Authority. |
| Recovery Authority | Self-perpetuation. | RA containment. |
| Predecessor source | Self-successor. | Replacement independence. |
| Successor candidate | Succession laundering. | Successor boundary. |
| Mutator | Mutation laundering. | Authorization/mutation separation. |
| Verifier | Self-certification. | Independent verification where required. |
| Custodian | Evidence control. | Custody/source separation. |
| Administrator | Universal source risk. | Minimum necessary authority. |

### 62.25 Common-Mode Dependency Matrix

| Dependency | Apparent separation | Actual independence criterion | Failure result |
| --- | --- | --- | --- |
| Terminating basis | Different records. | Independent governed basis where required. | No source. |
| Administrative Authority | Different admins. | No shared compromised admin basis. | No independence. |
| Identity authority | Different identities. | Independent attribution dependency. | No independence. |
| Credentials | Different credentials. | Independent credential control where required. | No independence. |
| Infrastructure | Different systems. | No common compromised control. | No independence. |
| Evidence producer | Different evidence. | Independent evidence provenance. | No source reliance. |
| Custodian | Different custody labels. | No shared custody compromise where required. | No source reliance. |
| Verifier | Different verifier label. | Independent verification basis. | No verification. |
| Mutator | Different mutators. | Authorized mutation only. | No legitimacy. |
| Organizational control | Different titles. | No common command compromise. | No independence. |
| Recovery Authority | Event actor. | Not sole future basis. | No source. |
| Revocation dependency | Separate negative source. | Available/current negative evidence. | No authority increase. |

### 62.26 Operation-Specific SoD Matrix

| Source operation | Consequence | Independence sensitivity | Universal count? | Quorum selected? |
| --- | --- | --- | --- | --- |
| Source establishment | Authority-enabling. | High. | No. | No. |
| Source qualification | Enabling. | High where beneficiary conflict. | No. | No. |
| Source authorization | Authority-enabling. | Very high. | No. | No. |
| Source use | Authority-enabling. | High. | No. | No. |
| Source mutation | State-changing. | High. | No. | No. |
| Source verification | Evidence reliance. | High. | No. | No. |
| Source revocation | Reducing/blocking. | High. | No. | No. |
| Source replacement | Mixed/increasing. | Very high. | No. | No. |
| Source closure | Terminating. | High. | No. | No. |
| Restoration | Increasing. | Very high, separately governed. | No. | No. |

### 62.27 Authority-Direction / Source Matrix

| Direction | Source sensitivity | Invalid inference |
| --- | --- | --- |
| Initial assignment | Very high. | Future holder creates source. |
| Authority-bearing assignment | High. | One source grants all authority. |
| Reactivation | Very high. | Prior source automatically revives. |
| Restoration | Very high. | Reduction source restores. |
| Successor establishment | Very high. | Replacement creates successor. |
| Suspension | Medium/high. | Suspension grants restoration. |
| Revocation | High. | Revocation owner restores. |
| Emergency reduction | Medium/high. | Emergency reduction increases authority. |
| Closure | High. | Closure evidence replays. |
| Reassignment/replacement | High. | Replacement launders compromise. |

### 62.28 Compromise / Unavailability Matrix

| Condition | Source effect | Required handling |
| --- | --- | --- |
| Benign unavailability | Not automatically compromise. | Use ordinary governed path if valid. |
| Source unavailable and required | Cannot verify. | No authority-increasing use. |
| Source compromised | No authority increase. | Independent basis required. |
| Assignment Authority compromised | Cannot validate own source. | Independent source/recovery basis. |
| Terminating basis compromised | Derivation affected. | Containment and independent basis. |
| Identity/infrastructure compromised | Attribution/control risk. | Common-mode review. |
| Revocation dependency unavailable | Unknown negative state. | No authority increase. |

### 62.29 Replay-Prevention Matrix

| Replay case | Required binding | Result if binding fails |
| --- | --- | --- |
| Historical source replay | Lifecycle/currentness. | No Assignment Authority. |
| Expired source replay | Expiration. | No Assignment Authority. |
| Revoked source replay | Revocation. | No Assignment Authority. |
| Replaced source replay | Replacement lineage. | No predecessor authority. |
| Closed source replay | Closure/event. | No Assignment Authority. |
| Cross-BE replay | Business Entity. | No cross-BE authority. |
| Cross-environment replay | Environment. | No production authority. |
| Wrong operation/class/target | Operation/class/target. | No Assignment Authority. |
| Cross-event replay | Event. | No Assignment Authority. |

### 62.30 Root / Recovery Authority / Successor Boundary Matrix

| Boundary | Invalid inference | Required result |
| --- | --- | --- |
| Root | Root is default Assignment Authority Source. | Rejected. |
| Standing root | Root remains always-on source. | Rejected. |
| Recovery Authority | RA establishes own source. | Rejected. |
| RA continuation | RA source persists after event. | Closure required. |
| Successor | Source replacement creates successor. | Rejected. |
| Restoration | Source replacement restores authority. | Rejected. |
| TAB | TAB becomes root. | Rejected. |

### 62.31 BE / Environment Isolation Matrix

| Context | Invalid inference | Required boundary |
| --- | --- | --- |
| BE A source | BE A -> BE B. | BE-bound source. |
| Cross-BE participant | Participant in one BE -> source in another. | No cross-BE inference. |
| Non-production source | Non-production -> production. | Environment-bound source. |
| Production source | Production exists by implication. | NOT GRANTED. |
| Shared infrastructure | Shared infra -> shared source. | Infrastructure non-authority. |

### 62.32 Authentication / Identity / Credential Boundary Matrix

| Concept | Source by itself? | Boundary |
| --- | --- | --- |
| Authentication | No. | Authentication != authorization. |
| Identity | No. | Identity != authority source. |
| Credential possession | No. | Possession != source. |
| Account/session | No. | Technical attribution only. |
| Certificate/key/password/token | No. | Credential technology not selected. |
| Identity provider | No. | IdP not selected. |

### 62.33 Human / Machine / AI Non-Authority Matrix

| Actor/process | Selected? | Source authority by itself? | Boundary |
| --- | --- | --- | --- |
| Human participant | No. | No. | Participant not selected. |
| Machine validation | No allocation. | No. | Validation != authority. |
| Machine mutation | No allocation. | No. | Mutation != authorization. |
| Machine evidence | No mechanism. | No. | Evidence != source. |
| AI | No authority. | No. | Non-authoritative assistance only. |
| LLM | No authority. | No. | Non-authoritative assistance only. |
| MCP | No authority. | No. | Non-authoritative assistance only. |

### 62.34 Failure / Fail-Closed Matrix

| Failure | Assignment Authority? | Authority-increasing use? | Fallback? |
| --- | --- | --- | --- |
| Missing source | No. | No. | No. |
| Invalid source | No. | No. | No. |
| Unverifiable source | No. | No. | No. |
| Stale source | No. | No. | No. |
| Suspended source | No where applicable. | No. | No. |
| Revoked source | No. | No. | No. |
| Expired source | No. | No. | No. |
| Replaced source | No from predecessor. | No. | No. |
| Closed source | No. | No. | No. |
| Compromised source | No for increase. | No. | No. |
| Wrong operation/class/target | No. | No. | No. |
| Wrong BE/environment | No. | No. | No. |
| Unsupported version | No. | No. | No. |
| Invalid/circular provenance | No. | No. | No. |
| Negative evidence unavailable | No for increase. | No. | No. |
| SoD/independence missing | No operation. | No. | No. |
| Technical mutation without legitimate source | No legitimacy. | No. | No. |

### 62.35 Technology-Neutrality Matrix

| Technology or mechanism | Selected? | Authority it must not acquire |
| --- | --- | --- |
| AWS / AWS account | No. | Business authority source. |
| IAM | No. | Assignment Authority Source. |
| Cognito / IdP | No. | Source legitimacy. |
| KMS / key / certificate / password / hardware token | No. | Business authority. |
| HSM / CloudHSM | No. | Root or source authority. |
| Secrets Manager / secrets | No. | Source authority. |
| DynamoDB / RDS / database / table | No. | Authority source by storage. |
| S3 / object store | No. | Source authority. |
| Lambda / runtime | No. | Authorization. |
| API Gateway / API | No. | Authority source. |
| EventBridge / SNS / SQS / Step Functions | No. | Workflow authority. |
| CloudWatch / audit service | No. | Audit-created authority. |
| GitHub / CI/CD / repository | No. | Business authority. |
| Ledger / blockchain / event store | No. | Current authority by history alone. |
| Schema / workflow / deployment | No. | Authority. |

### 62.36 Unresolved-Decision Dependency Matrix

| Order | Unresolved decision | Depends on |
| --- | --- | --- |
| 1 | Concrete Assignment Authority Source. | Source Ownership Governance Review and later realization. |
| 2 | Concrete source participant. | Source ownership and participant governance. |
| 3 | Concrete source owner. | Source Ownership Governance Review. |
| 4 | Concrete source authorizer. | Source ownership and accountable authorization governance. |
| 5 | Concrete source mutator. | Source mutation/producer governance. |
| 6 | Concrete source verifier. | Source evidence/verification governance. |
| 7 | Concrete source custodian. | Source custody governance. |
| 8 | Concrete source auditor. | Audit ownership governance. |
| 9 | Concrete source revocation owner. | Source lifecycle/revocation governance. |
| 10 | Concrete Assignment Authority participant. | Source realization and participant governance. |
| 11 | Concrete responsibility participants. | Participant realization governance. |
| 12 | Participant categories. | Participant category governance. |
| 13 | Participant count. | Operation-specific participant governance. |
| 14 | Quorum. | Participant count and operation need. |
| 15 | Human/machine allocation. | Responsibility realization and runtime governance. |
| 16 | Identity realization. | Participant provenance governance. |
| 17 | Credential realization. | Identity and credential governance. |
| 18 | Persistence. | Semantic and technology governance. |
| 19 | Schema. | Persistence and semantic contract governance. |
| 20 | API. | Schema and workflow governance. |
| 21 | Workflow. | Source, API, and runtime governance. |
| 22 | Runtime. | Workflow and implementation planning. |
| 23 | Technology. | Technology realization governance. |
| 24 | Cryptography. | Cryptographic realization governance. |
| 25 | Deployment. | Runtime and release governance. |
| 26 | Production source. | Separate production governance. |
| 27 | Production Assignment Authority. | Separate production governance. |
| 28 | Production participants. | Separate production governance. |
| 29 | Production authority. | Separate production governance. |

## 63. Normative Invariants

The following invariants are normative:

1. Assignment Authority Source != Assignment Authority.
2. Assignment Authority Source != assigned responsibility.
3. Assignment Authority Source != responsibility owner.
4. Assignment Authority Source != mutation mechanism.
5. Assignment Authority Source != assignment record.
6. Assignment Authority Source != authentication.
7. Assignment Authority Source != identity.
8. Assignment Authority Source != credential.
9. Assignment Authority Source != infrastructure authority.
10. Assignment Authority Source != organizational status.
11. Assignment Authority Source != Recovery Authority.
12. Assignment Authority Source != root.
13. Assignment Authority Source != successor authority.
14. Assignment Authority Source != restoration authority.
15. Assignment Authority Source != machine evidence.
16. Assignment Authority Source != audit evidence.
17. Assignment Authority Source != AI/LLM/MCP.
18. Record of authority != source of authority.
19. Technical mutation capability != authorization.
20. Authentication success != business authority.
21. Source legitimacy requires governed basis.
22. Source provenance must terminate.
23. Source provenance must be non-circular.
24. Source cannot establish its own terminating basis.
25. Assignment Authority cannot self-legitimize its source.
26. Responsibility owner cannot self-create source legitimacy.
27. Mutator cannot create source legitimacy by writing a record.
28. Source must be current.
29. Historical source evidence != current authority source.
30. Revoked source != current source.
31. Suspended source != current source where applicable.
32. Expired source != current source.
33. Replaced source != current source.
34. Closed source != current source.
35. Compromised source cannot authorize authority increase.
36. Current revocation dominates stale positive evidence.
37. Revocation source unavailable != verified not revoked.
38. Source establishment != source use.
39. Source use != source modification.
40. Source authorization != source mutation.
41. Source verification != source creation.
42. Source evidence != source legitimacy.
43. Source custody != source authority.
44. Source audit != source authority.
45. Source reconciliation != source creation.
46. Source revocation != source restoration.
47. Source suspension != source restoration.
48. Source replacement != source restoration.
49. Source replacement != root succession.
50. Source replacement != Recovery Authority succession.
51. Source replacement != successor authority establishment.
52. Root != default Assignment Authority Source.
53. Recovery Authority != Assignment Authority Source automatically.
54. TAB != root.
55. TAB != standing universal authority.
56. Same TAB governance model != same TAB instance.
57. Administrative Authority != universal Assignment Authority Source.
58. Organizational title != authority source.
59. AWS/IAM/GitHub control != business authority source.
60. Credential possession != authority source.
61. Machine execution != authority source.
62. AI/LLM/MCP != authority source.
63. Different people != independent provenance automatically.
64. Different identities != independent provenance automatically.
65. Different credentials != independent provenance automatically.
66. Different systems != independent provenance automatically.
67. Responsibility independence != participant count.
68. No universal dual approval.
69. No universal maker/checker.
70. No universal two-person rule.
71. No universal quorum.
72. No hidden super-admin.
73. No unrestricted break-glass.
74. BE A source != BE B source.
75. Non-production source != production source.
76. Source authority must be minimum necessary.
77. Source must be lifecycle-bound.
78. Source must be provenance-bound.
79. Source must be operation-bound where required.
80. Source must be responsibility-class-bound where required.
81. Source must be environment-bound.
82. Source must be BE-bound.
83. Unsupported governance version cannot silently remain authoritative.
84. Failed source validation -> no Assignment Authority.
85. Required negative evidence unavailable -> no authority-increasing use.
86. Required SoD absent -> operation does not proceed.
87. Technical mutation without legitimate source does not become legitimate.
88. Production authority remains NOT GRANTED.

## 64. Unresolved Decisions

The following decisions remain unresolved:

1. Concrete Assignment Authority Source.
2. Concrete source participant.
3. Concrete source owner.
4. Concrete source authorizer.
5. Concrete source mutator.
6. Concrete source verifier.
7. Concrete source custodian.
8. Concrete source auditor.
9. Concrete source revocation owner.
10. Concrete Assignment Authority participant.
11. Concrete responsibility participants.
12. Participant categories.
13. Participant count.
14. Quorum.
15. Human/machine allocation.
16. Identity realization.
17. Credential realization.
18. Persistence.
19. Schema.
20. API.
21. Workflow.
22. Runtime.
23. Technology.
24. Cryptography.
25. Deployment.
26. Production source.
27. Production Assignment Authority.
28. Production participants.
29. Production authority.

This artifact does not resolve these decisions.

## 65. Downstream Dependency

The immediate downstream dependency after this artifact is:

```text
Trusted Authorization Recovery Assignment Authority
Source Ownership Governance Review
```

That review is not performed by this artifact.

## 66. Participant Neutrality

This artifact does not select any person, office, role, founder, owner, CEO,
executive, employee, contractor, administrator, auditor, committee, vendor,
source owner, source administrator, source custodian, source verifier, source
approver, source mutator, Assignment Authority holder, responsibility holder,
or service account.

Participant count and participant categories remain unresolved.

## 67. Technology Neutrality

This artifact does not select AWS, IAM, Cognito, AWS Organizations, KMS,
CloudHSM, Secrets Manager, DynamoDB, RDS, S3, Lambda, API Gateway, EventBridge,
SNS, SQS, Step Functions, CloudWatch, GitHub, CI/CD, database, object store,
event store, ledger, blockchain, identity provider, hardware token, schema,
API, runtime, workflow, or deployment.

Technology references appear only as explicit non-selection, non-authority,
threat, matrix, or unresolved-dependency examples.

## 68. Cryptographic Neutrality

This artifact does not select signature scheme, hashing algorithm, encryption
algorithm, PKI, certificate hierarchy, key hierarchy, HSM topology, threshold
cryptography, secret sharing, multisig, escrow, key, certificate, password, or
credential mechanism.

## 69. No Implementation

This artifact does not create source code, tests, runtime models, dataclasses,
enums, persistence, database, schema, API, workflow, IAM, credentials, AWS
resources, deployment, or implementation.

The implementation repository remains frozen at:

```text
73d6f993e2731e55709d02413d3b0bb0ba350091
```

## 70. Production Authority

PRODUCTION AUTHORITY: NOT GRANTED

This artifact does not grant:

- production Assignment Authority Source;
- production Assignment Authority;
- production source holder;
- production participant;
- production responsibility assignment;
- production root;
- production Recovery TAB;
- production Recovery Authority;
- production successor;
- production restoration;
- production credential;
- production technology; or
- production implementation.

## 71. Governance Decision Summary

This artifact formalizes:

- MODEL F - HYBRID BOUNDED AUTHORITY-SOURCE REALIZATION;
- DERIVATION E - HYBRID BOUNDED DERIVATION;
- RELATIONSHIP D - HYBRID BOUNDED ORDINARY / EXCEPTIONAL SOURCE
  RELATIONSHIP;
- the governed terminating basis -> bounded source -> bounded Recovery
  Assignment Authority chain;
- Assignment Authority Source definition;
- source/authority non-equivalence;
- terminating basis requirements;
- TAB, Administrative Authority, root, Recovery Authority, successor,
  restoration, authentication, identity, credential, infrastructure,
  organization-status, human/machine, and AI/LLM/MCP boundaries;
- initial assignment source non-circularity;
- ordinary assignment source conditions;
- exceptional recovery source conditions;
- unavailability/compromise separation;
- source lifecycle/currentness/revocation/suspension/expiration/replacement
  and closure;
- source scope and provenance;
- source establishment/use and authorization/mutation separations;
- source verification, evidence, record, custody, audit, and reconciliation
  boundaries;
- authority-direction sensitivity;
- beneficiary-conflict and common-mode controls;
- operation-specific SoD;
- replay prevention;
- fail-closed source semantics;
- threat model;
- required matrices;
- 88 normative invariants;
- unresolved decisions;
- downstream dependency;
- participant, technology, credential, and cryptographic neutrality; and
- production authority not granted.

## 72. Closeout

This artifact creates exactly one governance document.

It creates no implementation authority and no production authority.

It does not perform the downstream review.

The next governed step is the read-only review separately authorized for:

```text
Trusted Authorization Recovery Assignment Authority
Source Ownership Governance Review
```

PRODUCTION AUTHORITY: NOT GRANTED
