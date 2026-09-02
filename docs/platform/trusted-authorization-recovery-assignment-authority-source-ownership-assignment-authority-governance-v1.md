# Trusted Authorization Recovery Assignment Authority Source Ownership Assignment Authority Governance v1

## 1. Status

This document is a governance artifact for the Nguyen AI Platform Trusted
Authorization governance sequence.

Status: DRAFT FOR HUMAN REVIEW.

Governance repository baseline:

`c8a4bad22a057f4c02c18b28892851b4cdf998a2`

Expected predecessor commit:

`c8a4bad Add Trusted Authorization recovery assignment authority source ownership governance v1`

Implementation repository baseline:

`73d6f993e2731e55709d02413d3b0bb0ba350091`

Production authority:

PRODUCTION AUTHORITY: NOT GRANTED

This artifact creates governance only. It does not create implementation,
runtime behavior, persistence, schema, API, workflow, credential, cryptographic
mechanism, deployment, production authority, or concrete participant selection.

## 2. Purpose

The purpose of this artifact is to govern the abstract authority that may
authorize assignment, reassignment, suspension, revocation, replacement,
closure, reactivation, or restoration of logical ownership responsibilities
around a Recovery Assignment Authority Source.

The purpose is not to create a new standing authority layer. The purpose is to
bind any such authority to finite, current, non-circular, provenance-valid,
operation-specific governance.

## 3. Scope

This artifact governs:

- Source Ownership Assignment Authority as an abstract governance concept;
- authority to authorize governed source-ownership operations;
- authority scope by ownership responsibility class, operation, source, target,
  event, Business Entity, environment, governance version, lifecycle,
  currentness, provenance, compromise state, and authority direction;
- ordinary and exceptional derivation paths;
- operation-specific SoD;
- beneficiary-conflict controls;
- common-mode dependency analysis;
- replay prevention;
- fail-closed behavior; and
- unresolved downstream decisions.

## 4. Non-Scope

This artifact does not select, create, or authorize:

- a concrete authority holder;
- a concrete source owner;
- a concrete source administrator;
- a concrete assignment administrator;
- a concrete requester, authorizer, verifier, mutator, custodian, auditor,
  revocation actor, replacement actor, restoration actor, or successor;
- participant category;
- participant count;
- quorum;
- identity realization;
- credential realization;
- persistence;
- schema;
- API;
- workflow;
- runtime;
- technology;
- cryptography;
- AWS, IAM, Cognito, KMS, CloudHSM, Secrets Manager, DynamoDB, RDS, S3,
  Lambda, API Gateway, EventBridge, SNS, SQS, Step Functions, CloudWatch,
  GitHub, CI/CD, database, object store, event store, ledger, blockchain,
  identity provider, or hardware token;
- production authority source;
- production ownership assignment authority;
- production Assignment Authority;
- production source ownership;
- production participant;
- production root;
- production Recovery TAB;
- production Recovery Authority;
- production successor;
- production restoration; or
- production implementation.

## 5. Authority

This artifact formalizes the preceding read-only governance review decision:

MODEL F - HYBRID BOUNDED OWNERSHIP ASSIGNMENT AUTHORITY

DERIVATION E - HYBRID BOUNDED DERIVATION

RELATIONSHIP E - HYBRID BOUNDED AUTHORITY-DIRECTION RELATIONSHIP

Repository governance is authoritative. Generic IAM, cloud, organizational,
identity, security, or governance assumptions must not override repository
governance.

## 6. Predecessor Governance

This artifact depends on and preserves:

- Trusted Authorization Recovery Assignment Authority Source Ownership
  Governance v1;
- Trusted Authorization Recovery Assignment Authority Source Realization
  Governance v1;
- Trusted Authorization recovery responsibility assignment revocation ownership
  realization governance v1;
- Trusted Authorization recovery responsibility assignment authority governance
  v1;
- Trusted Authorization recovery evidence responsibility participant
  realization governance v1;
- Trusted Authorization recovery evidence realization governance v1;
- Trusted Authorization recovery evidence custody verification governance v1;
- Trusted Authorization recovery terminating authority basis governance v1;
- Trusted Authorization concrete terminating authority basis governance v1;
- Trusted Authorization root-specific operation-level SoD governance v1;
- Trusted Authorization administrative mutation revocation ownership governance
  v1;
- Trusted Authorization production authority-source ownership governance v1;
- Trusted Authorization bounded recovery governance v1;
- Trusted Authorization root recovery topology governance v1;
- Trusted Authorization root lifecycle retention revocation succession
  governance v1;
- Trusted Authorization downstream authority impact governance v1;
- Trusted Authorization emergency authority reduction audit failure governance
  v1; and
- Trusted Authorization bootstrap root terminating authority source governance
  v1.

This artifact preserves:

- MODEL F - HYBRID BOUNDED SOURCE OWNERSHIP;
- RELATIONSHIP E - HYBRID BOUNDED OWNERSHIP / AUTHORITY RELATIONSHIP;
- OVERLAP E - HYBRID BOUNDED OVERLAP / INDEPENDENCE;
- MODEL F - HYBRID BOUNDED AUTHORITY-SOURCE REALIZATION;
- DERIVATION E - HYBRID BOUNDED DERIVATION;
- RELATIONSHIP D - HYBRID BOUNDED ORDINARY / EXCEPTIONAL SOURCE RELATIONSHIP;
- MODEL F - HYBRID BOUNDED ASSIGNMENT AUTHORITY;
- MODEL F - HYBRID BOUNDED OWNERSHIP REALIZATION;
- RELATIONSHIP E - HYBRID BOUNDED OWNERSHIP RELATIONSHIP;
- MODEL G - HYBRID OPERATION-SPECIFIC SoD;
- SAME TAB GOVERNANCE MODEL != SAME TAB INSTANCE;
- ROOT is bounded and non-standing;
- RECOVERY AUTHORITY is event-specific, bounded, non-standing,
  lifecycle-bound, provenance-bound, scope-bound, and closure-bound; and
- PRODUCTION AUTHORITY = NOT GRANTED.

## 7. Selected Authority Model

Selected model:

MODEL F - HYBRID BOUNDED OWNERSHIP ASSIGNMENT AUTHORITY

This model permits Source Ownership Assignment Authority only as a bounded
authority relationship. It may combine existing bounded Assignment Authority
relationships, operation-specific specialization, ordinary valid authority
paths, exceptional independently terminating authority paths, and event-specific
authority where required.

It rejects a universal standing assignment administrator.

## 8. Selected Derivation Model

Selected derivation:

DERIVATION E - HYBRID BOUNDED DERIVATION

Authority derivation may differ by governed context.

Ordinary valid, uncompromised operations may use already-governed bounded
administrative or Assignment Authority paths where all applicable governance
requirements are satisfied.

Exceptional recovery, compromise, invalid provenance, or other cases requiring
independent termination may require TAB or another already-governed independent
terminating basis.

UNAVAILABLE != COMPROMISED.

There is no hidden fallback, no universal Administrative Authority-only model,
and no universal TAB-only model.

## 9. Selected Authority-Direction Relationship

Selected relationship:

RELATIONSHIP E - HYBRID BOUNDED AUTHORITY-DIRECTION RELATIONSHIP

Authority requirements depend on operation and authority direction.

One authority is not required to perform all ownership operations.

Universal separation is not required.

REDUCTION AUTHORITY != RESTORATION AUTHORITY.

## 10. Model Rationale

Model F is required because repository governance rejects standing universal
authority, self-authorizing ownership, hidden root authority, hidden Recovery
Authority, and technology-derived authority.

Model F is narrower than a new authority layer because it treats Source
Ownership Assignment Authority as a bounded application of already-governed
Assignment Authority where possible.

Model F is broader than a single ordinary administrative path because
exceptional recovery and compromise may require independently terminating
governed provenance.

Model F preserves ordinary/exceptional distinction, authority-direction
sensitivity, operation-specific SoD, lifecycle/currentness, provenance,
Business Entity isolation, environment isolation, governance-version binding,
and minimum necessary authority.

## 11. Definitions

| Term | Governance meaning | Boundary |
| --- | --- | --- |
| Source Ownership Assignment Authority | Bounded, current, provenance-valid, operation-specific authority to authorize a governed change to one or more logical source-ownership responsibilities within explicitly governed scope. | Not source ownership, source authority, root, Recovery Authority, TAB, credential, identity, infrastructure, or AI. |
| Source Ownership | Bounded logical responsibility and accountability around an Assignment Authority Source. | Does not create assignment authority. |
| Assignment Authority Source | Governed legitimacy basis from which bounded Assignment Authority may derive. | Not authority holder or assignment executor. |
| Bounded Assignment Authority | Authority to authorize a specific governed assignment or ownership operation within scope. | Not standing super-admin authority. |
| Ownership operation | Assignment, reassignment, suspension, revocation, replacement, closure, reactivation, or restoration of source-ownership responsibility. | Operation-specific authority required. |
| Authority direction | Whether an operation increases/enables authority, reduces/blocks authority, or has mixed effect. | Reduction does not imply restoration. |
| Currentness | Verified present validity for the governed operation. | Historical evidence is not current authority. |
| Provenance | Governed lineage for authority, source, scope, lifecycle, dependencies, and negative evidence. | Provenance must terminate non-circularly. |
| Terminating basis | Already-governed legitimate basis where authority reasoning ends. | Not created by the authority being established. |

## 12. Fundamental Separations

The following separations are normative:

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != SOURCE OWNERSHIP

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != ASSIGNMENT AUTHORITY SOURCE

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != SOURCE AUTHORITY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != RECOVERY RESPONSIBILITY OWNERSHIP

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != MUTATION RESPONSIBILITY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != MUTATION CAPABILITY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != VERIFICATION

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != CUSTODY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != ROOT

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != RECOVERY AUTHORITY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != TAB

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != SUCCESSOR AUTHORITY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != RESTORATION AUTHORITY AUTOMATICALLY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != AUTHENTICATION

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != IDENTITY

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != CREDENTIAL

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != INFRASTRUCTURE CONTROL

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != ORGANIZATIONAL STATUS

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY != AI / LLM / MCP

ASSIGNMENT EXECUTION != ASSIGNMENT LEGITIMACY

OWNERSHIP RECORD != ASSIGNMENT AUTHORITY

TECHNICAL MUTATION SUCCESS != LEGITIMATE ASSIGNMENT

ACCOUNTABILITY != AUTOMATIC AUTHORIZATION

## 13. Source Ownership Assignment Authority Definition

Source Ownership Assignment Authority is bounded, current,
provenance-valid, operation-specific authority to authorize a governed change
to one or more logical source-ownership responsibilities within explicitly
governed scope.

It must be bounded by:

- ownership responsibility class;
- ownership operation;
- Assignment Authority Source;
- source;
- target;
- event where applicable;
- scope;
- Business Entity;
- environment;
- governance version;
- lifecycle;
- currentness;
- provenance;
- compromise state; and
- authority direction.

No runtime model or schema is defined.

## 14. No Hidden Super-Authority

This model must not be interpreted as:

- Source Ownership Super-Admin;
- universal assignment administrator;
- Recovery Super-Admin;
- standing root;
- standing Recovery Authority;
- universal source owner; or
- universal restoration authority.

The model governs bounded authority. It does not create organizational
super-administration.

## 15. Authority Scope

Any legitimate Source Ownership Assignment Authority must be no broader than
the governed operation requires.

Authority to assign one ownership responsibility class does not imply authority
to assign all ownership responsibility classes.

Authority for one operation does not imply authority for all ownership
operations.

Authority for one source does not imply authority for all sources.

Authority for one target does not imply authority for all targets.

Authority for one Business Entity does not imply authority for another Business
Entity.

Non-production authority does not imply production authority.

## 16. Ownership Operation Decomposition

The governed ownership operations are:

1. Initial Ownership Assignment
2. Ordinary Ownership Assignment
3. Ownership Reassignment
4. Ownership Suspension
5. Ownership Revocation
6. Ownership Replacement
7. Ownership Closure
8. Ownership Reactivation
9. Ownership Restoration

Each operation must identify authority direction, required authority
properties, currentness requirements, provenance requirements,
beneficiary-conflict considerations, SoD considerations, negative-evidence
requirements, and fail-closed outcome.

No actor is selected.

## 17. Initial Ownership Assignment

FUTURE OWNER CANNOT AUTHORIZE ITS OWN INITIAL OWNERSHIP.

FUTURE ASSIGNMENT AUTHORITY HOLDER CANNOT BE THE SOLE TERMINATING BASIS OF ITS
OWN AUTHORITY.

Initial ownership assignment requires finite, non-circular, independently
legitimate, current provenance. It must be bounded by operation, ownership
class, source, target, scope, Business Entity, environment, governance version,
lifecycle, negative evidence, SoD, and required independence.

## 18. Ordinary Ownership Assignment

Ordinary ownership assignment may use an existing bounded authority path only
where that path is current, valid, uncompromised, provenance-valid,
operation-valid, ownership-class-valid, source-valid, target-valid,
scope-valid, Business-Entity-valid, environment-valid,
governance-version-valid, lifecycle-valid, negative-evidence-valid, SoD-valid,
and independence-valid where required.

One successful ordinary operation does not create standing authority.

## 19. Ownership Reassignment

Ownership reassignment is a mixed-direction operation because it may remove one
current responsibility while establishing another.

Reassignment must not allow:

- owner self-appointment;
- owner-selected successor without valid authority;
- compromised authority selecting replacement;
- provenance laundering;
- revocation bypass;
- hidden restoration;
- hidden root; or
- hidden Recovery Authority.

## 20. Ownership Suspension

Ownership suspension is authority-reducing or authority-blocking.

AUTHORITY TO SUSPEND != AUTHORITY TO RESTORE.

Suspension authority may be narrower than assignment authority where governance
permits. This artifact does not impose universal same-authority or universal
separate-authority rules.

## 21. Ownership Revocation

Ownership revocation is authority-reducing or authority-blocking.

REVOCATION AUTHORITY != RESTORATION AUTHORITY.

REVOCATION OWNER != REVOCATION AUTHORITY AUTOMATICALLY.

Current revocation must dominate stale positive authority evidence.

## 22. Ownership Replacement

Ownership replacement is mixed-direction and authority-sensitive.

Replacement must prevent:

- self-replacement;
- beneficiary-controlled replacement;
- compromised-authority replacement;
- invalid-lineage laundering;
- hidden successor;
- hidden restoration;
- hidden root;
- hidden Recovery Authority; and
- standing assignment administration.

## 23. Ownership Closure

Ownership closure is authority-reducing or terminating.

Closure authority does not imply restoration, reassignment, successor
selection, or new ownership assignment authority.

Closed authority and closed ownership may remain historical evidence only.

## 24. Ownership Reactivation

Ownership reactivation is authority-increasing or authority-enabling.

SUSPENSION AUTHORITY != REACTIVATION AUTHORITY AUTOMATICALLY.

Reactivation requires separately current legitimate authority and current
negative-evidence checks.

## 25. Ownership Restoration

Ownership restoration is authority-increasing.

REVOCATION AUTHORITY != RESTORATION AUTHORITY.

REDUCTION AUTHORITY != RESTORATION AUTHORITY.

PRIOR OWNERSHIP != RESTORATION AUTHORITY.

PRIOR ASSIGNMENT AUTHORITY != CURRENT RESTORATION AUTHORITY AUTOMATICALLY.

Restoration requires independently legitimate current authority.

## 26. Assignment Authority Source Relationship

The governed chain is:

```text
TERMINATING GOVERNED BASIS
    ->
ASSIGNMENT AUTHORITY SOURCE
    ->
BOUNDED ASSIGNMENT AUTHORITY
    ->
AUTHORITY FOR SPECIFIC OWNERSHIP OPERATION
    ->
GOVERNED OWNERSHIP CHANGE
    ->
AUTHORIZED MUTATION
    ->
VERIFICATION / AUDIT / RECONCILIATION / CLOSURE
```

Source Ownership Assignment Authority fits within this chain. It must not
create unnecessary duplicated authority layers.

## 27. Authority Source / Authority Holder Separation

AUTHORITY SOURCE != AUTHORITY HOLDER.

AUTHORITY SOURCE != ASSIGNMENT EXECUTION.

AUTHORITY SOURCE != SOURCE OWNER.

AUTHORITY SOURCE != MUTATION OWNER.

The authority source supports legitimate derivation. It does not execute an
assignment by existing.

## 28. Ownership Self-Assignment Rejection

The following chains are invalid:

```text
OWNER
    ->
CLAIMS ASSIGNMENT AUTHORITY
    ->
REASSIGNS OWNERSHIP
```

```text
OWNERSHIP RECORD
    ->
BECOMES ASSIGNMENT AUTHORITY SOURCE
```

```text
ACCOUNTABLE OWNER
    ->
BECOMES ASSIGNMENT AUTHORITY AUTOMATICALLY
```

## 29. Assignment Authority Self-Establishment Rejection

The following chains are invalid:

```text
ASSIGNMENT AUTHORITY
    ->
VALIDATES OWN SOURCE
    ->
ESTABLISHES OWN LEGITIMACY
```

```text
ASSIGNMENT AUTHORITY
    ->
EXTENDS OWN SCOPE
    ->
CLAIMS CONTINUED AUTHORITY
```

Every authority-producing chain requires finite, non-circular terminating
provenance.

## 30. Assignment Authority Lifecycle

Conceptual lifecycle states are:

- proposed;
- established;
- current;
- suspended;
- expired;
- revoked;
- replaced;
- compromised;
- closed; and
- historical.

This artifact does not create a runtime state machine.

Historical authority is evidence, not current authority.

## 31. Assignment Authority Currentness

Missing, stale, suspended, revoked, expired, replaced, compromised, closed, or
unverifiable authority cannot authorize ownership change.

Only current, valid, provenance-valid, in-scope authority may support the
applicable ownership operation.

## 32. Revocation Dominance

CURRENT REVOCATION

dominates

STALE POSITIVE AUTHORITY EVIDENCE.

"REVOCATION SOURCE COULD NOT BE CHECKED"
    !=
"VERIFIED NOT REVOKED."

Required negative evidence unavailable:

NO AUTHORITY-INCREASING OPERATION.

## 33. Assignment Authority Provenance

Conceptual authority provenance includes:

- terminating basis;
- Assignment Authority Source;
- authority derivation;
- ownership responsibility class;
- ownership operation;
- source;
- target;
- event;
- scope;
- Business Entity;
- environment;
- governance version;
- lifecycle;
- currentness;
- suspension;
- revocation;
- expiration;
- replacement;
- compromise;
- closure; and
- dependency provenance.

No schema is defined.

## 34. Terminating Provenance

SOURCE OWNERSHIP ASSIGNMENT AUTHORITY CANNOT BE ITS OWN TERMINATING BASIS.

Every authority-producing chain must be finite, governed, non-circular,
current, provenance-valid, operation-bound, ownership-class-bound where
applicable, source-bound, target-bound, scope-bound, Business-Entity-bound,
environment-bound, governance-version-bound, and lifecycle-bound.

## 35. Ordinary vs Exceptional Authority

Ordinary valid, uncompromised operations may use already-governed bounded
authority paths where all applicable requirements are satisfied.

Exceptional or compromised conditions may require independently terminating
governed provenance.

UNAVAILABLE != COMPROMISED.

There is no hidden fallback.

There is no universal TAB-only path.

There is no universal Administrative Authority-only path.

## 36. TAB Instance Boundary

SAME TAB GOVERNANCE MODEL != SAME TAB INSTANCE.

No reusable universal TAB instance is inferred.

TAB is not instantiated by this artifact.

## 37. Compromised Assignment Authority

Compromised authority cannot:

- validate itself;
- restore itself;
- extend itself;
- replace itself;
- suppress revocation;
- appoint successor solely through compromised authority;
- create terminating provenance;
- create hidden root;
- invoke hidden break-glass; or
- grant itself restoration.

## 38. Unavailable Assignment Authority

UNAVAILABLE != COMPROMISED.

Unavailability does not transfer authority automatically.

There is no "next available admin wins" rule.

Unavailability does not create fallback authority in a source owner,
organizational title, infrastructure operator, Recovery Authority, root, AI,
LLM, or MCP.

## 39. Beneficiary Conflict

Beneficiary conflict must be analyzed for each ownership operation where the
beneficiary is also requester, qualifier, accountable owner, source owner,
Assignment Authority holder, authority-source owner, mutator, verifier,
custodian, revocation responsibility, Recovery Authority, replacement
candidate, or successor candidate.

The required independence is operation-specific. This artifact does not impose
universal separation.

## 40. Common-Mode Dependency

Common-mode dependency analysis must consider shared dependency on:

- terminating basis;
- Assignment Authority Source;
- Assignment Authority;
- Administrative Authority;
- identity authority;
- credential control;
- infrastructure control;
- evidence source;
- source ownership;
- source custody;
- verification;
- mutation;
- organizational control;
- Recovery Authority; and
- revocation dependency.

Different people, identities, credentials, accounts, systems, labels, or titles
do not automatically establish independence.

## 41. Operation-Specific SoD

MODEL G - HYBRID OPERATION-SPECIFIC SoD is preserved.

SoD applies as required to:

- initial assignment;
- ordinary assignment;
- reassignment;
- suspension;
- revocation;
- replacement;
- closure;
- reactivation; and
- restoration.

This artifact does not create universal dual approval, universal
maker/checker, universal two-person rule, universal quorum, or fixed
participant count.

## 42. Authority Overlap

Authority responsibilities may overlap where governance permits based on
operation, authority direction, consequence, beneficiary conflict, provenance,
common-mode dependency, lifecycle, compromise state, and applicable SoD.

Overlap must not permit self-authorization.

## 43. Authority Independence

Authority responsibilities must remain independent where operation-specific
governance requires.

RESPONSIBILITY INDEPENDENCE != PARTICIPANT COUNT.

Independence does not equal two people, two identities, two accounts, or
quorum.

## 44. Participant Count / Quorum

PARTICIPANT COUNT: UNRESOLVED / NOT SELECTED

QUORUM: UNRESOLVED / NOT SELECTED

No threshold or voting model is selected.

## 45. Authority Direction

Authority-increasing or authority-enabling operations include:

- initial ownership assignment;
- ordinary ownership assignment;
- reactivation; and
- restoration.

Authority-reducing or authority-blocking operations include:

- suspension;
- revocation; and
- closure.

Mixed operations include:

- reassignment; and
- replacement.

REDUCTION AUTHORITY != RESTORATION AUTHORITY.

## 46. Root Boundary

ROOT != SOURCE OWNERSHIP ASSIGNMENT AUTHORITY BY DEFAULT.

Root remains bounded and non-standing.

This artifact creates no universal assignment administration.

## 47. Recovery Authority Boundary

RECOVERY AUTHORITY != SOURCE OWNERSHIP ASSIGNMENT AUTHORITY BY DEFAULT.

Recovery Authority cannot automatically authorize:

- its own ownership;
- continuation;
- replacement;
- revocation suppression;
- restoration;
- successor selection; or
- permanent assignment administration.

## 48. TAB Boundary

TAB != SOURCE OWNERSHIP ASSIGNMENT AUTHORITY.

TAB may support terminating legitimacy where required.

TAB does not become standing authority.

## 49. Source Owner Boundary

SOURCE OWNER != SOURCE OWNERSHIP ASSIGNMENT AUTHORITY.

Ownership does not confer appointment or replacement authority.

## 50. Source Authority Boundary

SOURCE AUTHORITY != SOURCE OWNERSHIP ASSIGNMENT AUTHORITY AUTOMATICALLY.

Source legitimacy and ownership-assignment authority must not be collapsed.

## 51. Recovery Assignment Authority Relationship

Source Ownership Assignment Authority is governed as a bounded application or
specialization of already-governed Assignment Authority rather than an
independent standing authority layer.

The specialization must remain operation-specific, source-specific,
target-specific, scope-specific, ownership-class-specific where applicable,
lifecycle-bound, provenance-bound, currentness-bound, and non-standing.

## 52. Responsibility Owner Boundary

RESPONSIBILITY OWNER != SOURCE OWNERSHIP ASSIGNMENT AUTHORITY.

Owning a recovery responsibility does not authorize assigning source-ownership
responsibilities.

## 53. Mutation Boundary

MUTATION OWNER != AUTHORIZER.

MUTATION CAPABILITY != ASSIGNMENT AUTHORITY.

TECHNICAL ASSIGNMENT SUCCESS != LEGITIMATE ASSIGNMENT.

Mutation executes only an already-authorized ownership change.

## 54. Verification Boundary

VERIFICATION != AUTHORIZATION.

Verification cannot create assignment authority.

## 55. Audit / Reconciliation Boundary

AUDIT != AUTHORIZATION.

RECONCILIATION != AUTHORITY CREATION.

Neither audit nor reconciliation may retroactively legalize invalid assignment.

## 56. Authentication / Identity / Credential Boundary

AUTHENTICATION != OWNERSHIP ASSIGNMENT AUTHORITY.

IDENTITY != OWNERSHIP ASSIGNMENT AUTHORITY.

CREDENTIAL POSSESSION != OWNERSHIP ASSIGNMENT AUTHORITY.

No provider or credential is selected.

## 57. Organizational Status Boundary

The following do not automatically create Source Ownership Assignment
Authority:

- founder;
- owner;
- CEO;
- executive;
- board;
- employee;
- contractor;
- administrator;
- security team;
- developer; and
- auditor.

## 58. Infrastructure Boundary

AWS CONTROL != ASSIGNMENT AUTHORITY.

IAM CONTROL != ASSIGNMENT AUTHORITY.

GITHUB CONTROL != ASSIGNMENT AUTHORITY.

DATABASE CONTROL != ASSIGNMENT AUTHORITY.

DEPLOYMENT CONTROL != ASSIGNMENT AUTHORITY.

Infrastructure control does not create business authority.

## 59. Human / Machine Boundary

Human/machine allocation remains unresolved.

MACHINE EXECUTION != BUSINESS ASSIGNMENT AUTHORITY.

This artifact does not allocate authority to a human or machine category.

## 60. AI / LLM / MCP Boundary

AI, LLM, and MCP cannot independently become authoritative:

- ownership assignment authority;
- Assignment Authority Source;
- source owner;
- Recovery Assignment Authority;
- revocation authority;
- restoration authority;
- replacement authority;
- root;
- Recovery Authority;
- successor selector; or
- production authority.

## 61. Business Entity Isolation

ASSIGNMENT AUTHORITY FOR BE A

is not

ASSIGNMENT AUTHORITY FOR BE B.

No cross-Business-Entity inference is permitted.

## 62. Environment Isolation

NON-PRODUCTION ASSIGNMENT AUTHORITY

is not

PRODUCTION ASSIGNMENT AUTHORITY.

No production authority is selected.

## 63. Governance Version

Authority validity must be bound to a supported governance version.

Unsupported, obsolete, or incompatible governance version cannot silently
preserve authority.

No runtime compatibility mechanism is defined.

## 64. Replay Prevention

Governance must prevent replay of:

- historical assignment authority;
- expired authority;
- revoked authority;
- suspended authority;
- replaced authority;
- closed authority;
- cross-Business-Entity authority;
- cross-environment authority;
- wrong-source authority;
- wrong-ownership-class authority;
- wrong-operation authority;
- wrong-target authority;
- cross-event authority; and
- stale authority-source evidence.

No cryptographic mechanism is selected.

## 65. Minimum Necessary Authority

AUTHORITY MUST BE NO BROADER THAN REQUIRED FOR THE GOVERNED OWNERSHIP
OPERATION.

Authority for class X does not imply authority for all classes.

Authority for operation X does not imply authority for all operations.

Authority for Business Entity A does not imply authority for Business Entity B.

Non-production authority does not imply production authority.

## 66. Fail-Closed Semantics

| Condition | Result |
| --- | --- |
| MISSING ASSIGNMENT AUTHORITY | NO OWNERSHIP ASSIGNMENT |
| INVALID ASSIGNMENT AUTHORITY | NO OWNERSHIP ASSIGNMENT |
| UNVERIFIABLE ASSIGNMENT AUTHORITY | NO OWNERSHIP ASSIGNMENT |
| STALE ASSIGNMENT AUTHORITY | NO OWNERSHIP ASSIGNMENT |
| SUSPENDED ASSIGNMENT AUTHORITY | NO AFFECTED OWNERSHIP OPERATION |
| REVOKED ASSIGNMENT AUTHORITY | NO OWNERSHIP ASSIGNMENT |
| EXPIRED ASSIGNMENT AUTHORITY | NO OWNERSHIP ASSIGNMENT |
| REPLACED ASSIGNMENT AUTHORITY | NO AUTHORITY FROM PREDECESSOR |
| CLOSED ASSIGNMENT AUTHORITY | NO OWNERSHIP ASSIGNMENT |
| COMPROMISED ASSIGNMENT AUTHORITY | NO AUTHORITY-INCREASING OWNERSHIP OPERATION |
| INVALID ASSIGNMENT AUTHORITY SOURCE | NO OWNERSHIP ASSIGNMENT |
| UNVERIFIABLE AUTHORITY SOURCE | NO OWNERSHIP ASSIGNMENT |
| WRONG OWNERSHIP CLASS | NO OWNERSHIP ASSIGNMENT |
| WRONG OPERATION | NO OWNERSHIP ASSIGNMENT |
| WRONG SOURCE | NO OWNERSHIP ASSIGNMENT |
| WRONG TARGET | NO OWNERSHIP ASSIGNMENT |
| WRONG BE | NO OWNERSHIP ASSIGNMENT |
| WRONG ENVIRONMENT | NO OWNERSHIP ASSIGNMENT |
| UNSUPPORTED GOVERNANCE VERSION | NO OWNERSHIP ASSIGNMENT |
| INVALID PROVENANCE | NO OWNERSHIP ASSIGNMENT |
| CIRCULAR PROVENANCE | NO OWNERSHIP ASSIGNMENT |
| REQUIRED NEGATIVE EVIDENCE UNAVAILABLE | NO AUTHORITY-INCREASING OPERATION |
| REQUIRED SoD NOT ESTABLISHED | OPERATION STOPS |
| REQUIRED INDEPENDENCE NOT ESTABLISHED | OPERATION STOPS |
| OWNER CLAIMS ASSIGNMENT AUTHORITY WITHOUT VALID BASIS | NO OWNERSHIP ASSIGNMENT |
| TECHNICAL MUTATION SUCCEEDS WITHOUT LEGITIMATE AUTHORIZATION | NO LEGITIMATE OWNERSHIP CHANGE |

No convenience fallback is permitted.

## 67. Threat Model

| # | Threat | Targeted invariant | Affected operation | Governance control | Fail-closed result | Unresolved dependency |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Current owner self-assigns continued ownership. | Owner cannot self-create assignment authority. | Reassignment. | Independent governed assignment basis. | No ownership assignment. | Assignment Authority Source for this authority. |
| 2 | Current owner selects replacement without authority. | Source owner != assignment authority. | Replacement. | Replacement authority validation. | No replacement. | Replacement governance. |
| 3 | Future owner authorizes own initial ownership. | Future owner cannot authorize own initial ownership. | Initial assignment. | Independent terminating provenance. | No initial assignment. | Authority-source governance. |
| 4 | Ownership record becomes assignment authority. | Ownership record != assignment authority. | All ownership operations. | Record/authority separation. | No authority inference. | Evidence governance. |
| 5 | Assignment Authority self-establishes. | Assignment Authority cannot self-establish. | Authority establishment. | Non-circular provenance. | No assignment authority. | Authority-source governance. |
| 6 | Assignment Authority validates own source. | Authority cannot validate own source as sole basis. | Source validation. | Independent source verification where required. | No assignment. | Verification governance. |
| 7 | Assignment Authority expands own scope. | Authority cannot silently extend scope. | Scope change. | Scope-bound authority. | No out-of-scope assignment. | Scope governance. |
| 8 | Assignment Authority extends own lifecycle. | Lifecycle must be bounded. | Lifecycle extension. | Lifecycle validation. | No extension. | Lifecycle governance. |
| 9 | Assignment Authority suppresses own revocation. | Current revocation dominates stale evidence. | Revocation. | Negative-evidence independence. | No authority increase. | Revocation evidence governance. |
| 10 | Assignment Authority restores itself. | Compromised authority cannot self-restore. | Restoration. | Independent restoration authority. | No restoration. | Restoration governance. |
| 11 | Assignment Authority replaces itself. | Compromised authority cannot self-replace. | Replacement. | Independent replacement basis. | No replacement. | Replacement governance. |
| 12 | Assignment Authority creates successor authority. | No hidden successor authority. | Succession-like replacement. | Successor boundary. | No successor. | Succession governance. |
| 13 | Authority Source is treated as authority holder. | Authority source != authority holder. | All operations. | Source/holder separation. | No assignment. | Participant governance. |
| 14 | Authority Source performs assignment by existence alone. | Authority source != assignment execution. | All operations. | Execution authorization boundary. | No assignment. | Execution governance. |
| 15 | Mutation owner becomes authorizer. | Mutation owner != authorizer. | Mutation. | Authorization/mutation separation. | No state change. | Mutation governance. |
| 16 | Technical mutation creates legitimacy. | Technical success != legitimacy. | Mutation. | Legitimacy validation. | No legitimate change. | Evidence governance. |
| 17 | Verifier becomes authorizer. | Verification != authorization. | Verification. | Verification boundary. | No authorization. | Verifier governance. |
| 18 | Auditor retroactively legalizes assignment. | Audit != authorization. | Audit. | Audit boundary. | No retroactive legitimacy. | Audit governance. |
| 19 | Reconciler launders invalid assignment. | Reconciliation != authority creation. | Reconciliation. | Reconciliation boundary. | Invalid state remains invalid. | Reconciliation governance. |
| 20 | Suspension authority becomes restoration authority. | Suspension authority != restoration authority. | Suspension/restoration. | Direction separation. | No restoration. | Restoration governance. |
| 21 | Revocation authority becomes restoration authority. | Revocation authority != restoration authority. | Revocation/restoration. | Direction separation. | No restoration. | Restoration governance. |
| 22 | Revocation owner becomes revocation authority automatically. | Revocation owner != revocation authority automatically. | Revocation. | Ownership/authority separation. | No revocation authority inference. | Revocation authority governance. |
| 23 | Replacement launders invalid provenance. | Reassignment cannot launder invalid provenance. | Replacement. | Provenance validation. | No replacement. | Provenance governance. |
| 24 | Replacement creates hidden successor. | Replacement != successor authority. | Replacement. | Successor boundary. | No successor. | Successor governance. |
| 25 | Replacement creates hidden root. | Root not default assignment authority. | Replacement. | Root containment. | No root. | Root governance. |
| 26 | Replacement creates hidden Recovery Authority. | Recovery Authority not default assignment authority. | Replacement. | Recovery Authority containment. | No Recovery Authority. | Recovery governance. |
| 27 | Closure creates reassignment authority. | Closure does not create new authority. | Closure. | Closure boundary. | No reassignment. | Closure governance. |
| 28 | Reactivation bypasses current authority validation. | Reactivation requires current authority. | Reactivation. | Currentness validation. | No reactivation. | Currentness governance. |
| 29 | Restoration relies only on historical ownership. | Prior ownership != restoration authority. | Restoration. | Current authority required. | No restoration. | Restoration governance. |
| 30 | Restoration relies only on historical Assignment Authority. | Prior Assignment Authority != current restoration authority. | Restoration. | Current authority required. | No restoration. | Restoration governance. |
| 31 | Ordinary Administrative Authority used after compromise. | Compromised authority cannot self-repair. | Ordinary assignment. | Compromise-aware derivation. | No authority-increasing operation. | Compromise governance. |
| 32 | Exceptional recovery bypasses terminating provenance. | Provenance must terminate. | Exceptional assignment. | Independent terminating basis. | No assignment. | TAB/source governance. |
| 33 | Unavailable authority creates hidden fallback. | Unavailability creates no fallback. | All operations. | Fail closed. | No assignment. | Recovery governance. |
| 34 | Compromised authority uses ordinary path to self-repair. | Compromised authority cannot self-restore. | Replacement/restoration. | Independent basis. | No self-repair. | Compromise governance. |
| 35 | Same TAB instance replayed across unrelated events. | Same TAB model != same TAB instance. | Exceptional assignment. | Event provenance. | No replay. | TAB instance governance. |
| 36 | Beneficiary controls authority source. | Beneficiary conflict requires analysis. | Authority derivation. | Operation-specific independence. | Operation stops. | Beneficiary governance. |
| 37 | Beneficiary controls mutation and verification. | Required independence must be established. | Mutation/verification. | Common-mode and SoD checks. | Operation stops. | SoD governance. |
| 38 | Common-mode dependency disguised by different people. | Different people != independent control. | All operations. | Dependency analysis. | Operation stops. | Participant governance. |
| 39 | Common-mode dependency disguised by different identities. | Different identities != independent control. | All operations. | Dependency analysis. | Operation stops. | Identity governance. |
| 40 | Common-mode dependency disguised by different credentials. | Different credentials != independent control. | All operations. | Dependency analysis. | Operation stops. | Credential governance. |
| 41 | Common-mode dependency disguised by different systems. | Different systems != independent control. | All operations. | Dependency analysis. | Operation stops. | Technology governance. |
| 42 | Universal overlap enables self-authorization. | Overlap must not permit self-authorization. | All operations. | Operation-specific overlap. | Operation stops. | SoD governance. |
| 43 | Universal separation creates hidden fixed participant count. | Independence != participant count. | All operations. | No universal count. | No count inference. | Participant governance. |
| 44 | Universal dual approval introduced without governance basis. | No universal dual approval. | All operations. | Operation-specific SoD. | No dual approval rule. | SoD governance. |
| 45 | Universal maker/checker introduced without governance basis. | No universal maker/checker. | All operations. | Operation-specific SoD. | No maker/checker rule. | SoD governance. |
| 46 | Universal quorum introduced without governance basis. | No universal quorum. | All operations. | Quorum unresolved. | No quorum. | Quorum governance. |
| 47 | Root becomes standing ownership assignment authority. | Root not default assignment authority. | All operations. | Root containment. | No root authority. | Root governance. |
| 48 | Recovery Authority becomes standing ownership assignment authority. | Recovery Authority not default assignment authority. | All operations. | Recovery Authority containment. | No standing Recovery Authority. | Recovery governance. |
| 49 | TAB becomes standing assignment authority. | TAB not standing ownership assignment authority. | All operations. | TAB containment. | No standing TAB. | TAB governance. |
| 50 | Source owner becomes universal assignment authority. | Source owner not assignment authority automatically. | All operations. | Ownership/authority separation. | No assignment. | Ownership authority governance. |
| 51 | Responsibility owner becomes assignment authority. | Responsibility owner != assignment authority. | All operations. | Boundary enforcement. | No assignment. | Responsibility governance. |
| 52 | Founder/CEO status creates assignment authority. | Organizational status != assignment authority. | All operations. | Status boundary. | No assignment. | Participant eligibility. |
| 53 | Authentication creates assignment authority. | Authentication != assignment authority. | All operations. | Authn/authz separation. | No assignment. | Identity governance. |
| 54 | Identity creates assignment authority. | Identity != assignment authority. | All operations. | Identity boundary. | No assignment. | Identity governance. |
| 55 | Credential possession creates assignment authority. | Credential possession != assignment authority. | All operations. | Credential boundary. | No assignment. | Credential governance. |
| 56 | AWS/IAM/GitHub control creates assignment authority. | Infrastructure control != assignment authority. | All operations. | Infrastructure boundary. | No assignment. | Technology governance. |
| 57 | Database/storage control creates assignment authority. | Storage control != authority. | All operations. | Record/storage boundary. | No assignment. | Persistence governance. |
| 58 | Deployment control creates assignment authority. | Deployment control != assignment authority. | All operations. | Infrastructure boundary. | No assignment. | Deployment governance. |
| 59 | Machine execution creates assignment authority. | Machine execution != business authority. | All operations. | Human/machine boundary. | No assignment. | Human/machine governance. |
| 60 | AI/LLM/MCP becomes authoritative assigner. | AI/LLM/MCP != authority. | All operations. | AI boundary. | No assignment. | Tool governance. |
| 61 | Historical authority replay. | Historical authority cannot be replayed. | All operations. | Currentness and lifecycle checks. | No assignment. | Replay governance. |
| 62 | Expired authority replay. | Expired authority != current authority. | All operations. | Expiration validation. | No assignment. | Lifecycle governance. |
| 63 | Suspended authority replay. | Suspended authority not exercisable. | Affected operation. | Suspension validation. | Operation stops. | Suspension governance. |
| 64 | Revoked authority replay. | Revoked authority != current authority. | All operations. | Revocation dominance. | No assignment. | Revocation governance. |
| 65 | Replaced authority replay. | Replaced authority != current authority. | All operations. | Replacement lineage. | No predecessor authority. | Replacement governance. |
| 66 | Closed authority replay. | Closed authority != current authority. | All operations. | Closure validation. | No assignment. | Closure governance. |
| 67 | Cross-BE authority reuse. | BE A authority != BE B authority. | All operations. | BE binding. | No assignment. | BE governance. |
| 68 | Cross-environment authority reuse. | Non-production authority != production authority. | All operations. | Environment binding. | No assignment. | Environment governance. |
| 69 | Wrong-source authority reuse. | Authority must be source-bound. | All operations. | Source binding. | No assignment. | Source governance. |
| 70 | Wrong-class authority reuse. | Authority must be ownership-class-bound where applicable. | All operations. | Class binding. | No assignment. | Class governance. |
| 71 | Wrong-operation authority reuse. | Authority must be operation-bound. | All operations. | Operation binding. | No assignment. | Operation governance. |
| 72 | Wrong-target authority reuse. | Authority must be target-bound. | All operations. | Target binding. | No assignment. | Target governance. |
| 73 | Cross-event authority reuse. | Event authority must be event-bound. | Event-specific operations. | Event binding. | No assignment. | Event governance. |
| 74 | Stale positive evidence overrides revocation. | Revocation dominates stale positive evidence. | All operations. | Negative evidence precedence. | No authority increase. | Evidence governance. |
| 75 | Revocation source unavailable interpreted as not revoked. | Revocation unavailable != verified not revoked. | Authority-increasing operations. | Negative evidence required. | No authority increase. | Negative-evidence governance. |
| 76 | Authority scope silently expands. | Authority must be minimum necessary. | Scope-sensitive operations. | Scope validation. | No out-of-scope assignment. | Scope governance. |
| 77 | Non-production authority becomes production authority. | Non-production authority != production authority. | Production operation. | Environment isolation. | No production authority. | Production governance. |
| 78 | Reduction authority reused for restoration. | Reduction authority != restoration authority. | Restoration. | Direction separation. | No restoration. | Restoration governance. |
| 79 | Assignment authority never closes. | Lifecycle must be bounded. | Event-specific operations. | Closure required. | No residual authority. | Closure governance. |
| 80 | Hidden universal source-ownership administrator emerges. | No hidden super-authority. | All operations. | Bounded model and minimum necessary authority. | No universal authority. | Future artifact review. |

## 68. Required Matrices

### 68.1 Authority Model Comparison Matrix

| Model | Decision | Rationale |
| --- | --- | --- |
| A - Single Standing Ownership Assignment Authority | Rejected | Creates concentration, standing authority, and super-admin risk. |
| B - Ownership-Self-Assignment Model | Rejected | Circular and permits owner self-legitimation. |
| C - Administrative-Authority-Centric Model | Rejected as complete model | Useful for some ordinary cases but insufficient for compromise and exceptional recovery. |
| D - Recovery-Assignment-Authority Specialization | Included within Model F | Avoids duplication but must remain bounded by ordinary/exceptional derivation and direction. |
| E - Event-Specific Ownership Assignment Authority | Included where required | Fits exceptional events but is too narrow for all ordinary cases. |
| F - Hybrid Bounded Ownership Assignment Authority | Selected | Fits repository governance without standing authority or concrete participant selection. |
| G - Underdetermined | Rejected | Repository evidence is sufficient. |

### 68.2 Assignment Authority / Ownership Boundary Matrix

| Item | May assign ownership by itself? | Boundary |
| --- | --- | --- |
| Source ownership | No | Ownership != assignment authority. |
| Accountable ownership | No | Accountability != automatic authorization. |
| Ownership record | No | Record != authority. |
| Current valid bounded authority | Potentially | Only within governed scope. |

### 68.3 Assignment Authority / Authority Source Boundary Matrix

| Item | Function | Non-equivalence |
| --- | --- | --- |
| Authority Source | Supports legitimacy derivation. | Not holder or executor. |
| Authority holder | May exercise authority if current and valid. | Not source by identity alone. |
| Assignment execution | Performs authorized change. | Not legitimacy. |

### 68.4 Assignment Authority / Recovery Assignment Authority Matrix

| Relationship | Rule | Constraint |
| --- | --- | --- |
| Specialization | Source-ownership assignment may be bounded application of Assignment Authority. | No independent standing layer. |
| Recovery Authority | Not default assigner. | Event-specific and closure-bound. |

### 68.5 Initial Ownership Assignment Matrix

| Requirement | Rule | Fail-closed |
| --- | --- | --- |
| Future owner | Cannot authorize own initial ownership. | No assignment. |
| Provenance | Must be finite and independent. | No assignment. |
| SoD | Must satisfy operation-specific requirements. | Operation stops. |

### 68.6 Ordinary Ownership Assignment Matrix

| Requirement | Rule | Fail-closed |
| --- | --- | --- |
| Current path | Must be valid and uncompromised. | No assignment. |
| Scope | Must match class, source, target, BE, environment, version. | No assignment. |
| Negative evidence | Must be available where required. | No authority increase. |

### 68.7 Ownership Reassignment Matrix

| Risk | Control | Fail-closed |
| --- | --- | --- |
| Self-appointment | Independent authority basis. | No reassignment. |
| Invalid lineage | Provenance validation. | No reassignment. |
| Hidden restoration | Direction analysis. | No restoration. |

### 68.8 Ownership Suspension Authority Matrix

| Property | Rule | Boundary |
| --- | --- | --- |
| Direction | Reducing/blocking. | Not restoration. |
| Scope | May be narrower than assignment. | Operation-specific. |

### 68.9 Ownership Revocation Authority Matrix

| Property | Rule | Boundary |
| --- | --- | --- |
| Direction | Reducing/blocking. | Not restoration. |
| Owner | Revocation owner not authority automatically. | Separate authority basis. |

### 68.10 Ownership Replacement Authority Matrix

| Risk | Control | Fail-closed |
| --- | --- | --- |
| Self-replacement | Independent authority. | No replacement. |
| Compromised replacement | Compromise-aware validation. | No replacement. |
| Successor laundering | Successor boundary. | No successor. |

### 68.11 Ownership Closure Authority Matrix

| Property | Rule | Fail-closed |
| --- | --- | --- |
| Closure | Terminates exercisability. | No residual authority. |
| Historical evidence | Retained as non-exercisable. | No replay. |

### 68.12 Ownership Reactivation Authority Matrix

| Requirement | Rule | Fail-closed |
| --- | --- | --- |
| Current authority | Required. | No reactivation. |
| Suspension authority | Not enough automatically. | No restoration. |

### 68.13 Ownership Restoration Authority Matrix

| Requirement | Rule | Fail-closed |
| --- | --- | --- |
| Independent authority | Required. | No restoration. |
| Prior ownership | Not sufficient. | No restoration. |
| Prior Assignment Authority | Not automatically current. | No restoration. |

### 68.14 Authority Direction Matrix

| Direction | Operations | Rule |
| --- | --- | --- |
| Increasing/enabling | Initial assignment, ordinary assignment, reactivation, restoration | Requires current independently legitimate authority. |
| Reducing/blocking | Suspension, revocation, closure | Does not imply restoration authority. |
| Mixed | Reassignment, replacement | Requires direction-sensitive controls. |

### 68.15 Ordinary / Exceptional Authority Matrix

| Context | Possible derivation | Constraint |
| --- | --- | --- |
| Ordinary valid uncompromised | Bounded administrative or Assignment Authority path. | All validations required. |
| Exceptional recovery | Independently terminating governed path. | No hidden fallback. |
| Compromise | Affected path cannot self-repair. | Independent basis required. |

### 68.16 Authority Derivation Matrix

| Derivation option | Decision | Reason |
| --- | --- | --- |
| Directly from current source owner | Rejected | Circular/self-assignment risk. |
| Directly from Administrative Authority | Rejected as universal | Insufficient for exceptional compromise. |
| Directly from Recovery Assignment Authority | Rejected as universal | Over-collapses scope. |
| Event-specific terminating basis only | Rejected as universal | Too narrow for ordinary cases. |
| Hybrid bounded derivation | Selected | Fits ordinary and exceptional governance. |
| Underdetermined | Rejected | Evidence sufficient. |

### 68.17 Assignment Authority Lifecycle Matrix

| State | May authorize? | Rule |
| --- | --- | --- |
| Proposed | No | Not established. |
| Established | Only if current and valid. | Validate before use. |
| Current | Potentially. | All scope/provenance checks required. |
| Suspended | No affected operation. | Suspension controls. |
| Expired | No. | No renewal by inference. |
| Revoked | No. | Revocation dominates. |
| Replaced | No from predecessor. | Replacement lineage required. |
| Compromised | No authority-increasing use. | Independent recovery basis. |
| Closed | No. | Historical only. |
| Historical | No. | Evidence only. |

### 68.18 Assignment Authority Currentness Matrix

| Condition | Result |
| --- | --- |
| Current, valid, in scope | Potentially usable. |
| Stale | No ownership assignment. |
| Unverifiable | No ownership assignment. |
| Negative evidence unavailable where required | No authority increase. |

### 68.19 Assignment Authority Provenance Matrix

| Element | Required? | Purpose |
| --- | --- | --- |
| Terminating basis | Yes | Non-circular legitimacy. |
| Assignment Authority Source | Yes where applicable | Source legitimacy. |
| Operation/class/source/target | Yes | Prevent scope expansion. |
| BE/environment/version | Yes | Prevent cross-domain replay. |
| Lifecycle/currentness/negative evidence | Yes | Prevent stale authority. |
| Dependency provenance | Yes where independence required | Detect common-mode risk. |

### 68.20 Terminating Provenance Matrix

| Claim | Valid? | Rule |
| --- | --- | --- |
| Authority terminates in itself | No | Circular. |
| Authority terminates in current source owner alone | No | Self-assignment risk. |
| Authority terminates in governed basis | Potentially | Must be current, finite, in scope. |

### 68.21 Negative-Evidence Matrix

| Evidence | Effect |
| --- | --- |
| Revocation | Blocks authority where applicable. |
| Suspension | Blocks affected operation. |
| Expiration | Ends current validity. |
| Replacement | Ends predecessor authority. |
| Closure | Ends exercisability. |
| Compromise | Blocks authority-increasing use. |
| Required negative evidence unavailable | No authority increase. |

### 68.22 Beneficiary-Conflict Matrix

| Beneficiary overlap | Risk | Control |
| --- | --- | --- |
| Owner/requester | Self-authorization. | Independent authority where required. |
| Holder/source owner | Source capture. | Source/holder separation. |
| Mutator/verifier | Laundering. | Operation-specific SoD. |
| Replacement candidate | Successor capture. | Replacement independence. |

### 68.23 Common-Mode Dependency Matrix

| Shared dependency | Risk | Required analysis |
| --- | --- | --- |
| Terminating basis | False independence. | Provenance mapping. |
| Identity or credentials | False attribution. | Dependency mapping. |
| Infrastructure | Technical capture. | Business authority separation. |
| Evidence/custody/verification | Evidence laundering. | Independence where required. |
| Revocation dependency | Suppression. | Negative-evidence resilience. |

### 68.24 Operation-Specific SoD Matrix

| Operation | SoD posture | Universal count? |
| --- | --- | --- |
| Initial assignment | High sensitivity. | No. |
| Ordinary assignment | Context-sensitive. | No. |
| Reassignment/replacement | High mixed-direction sensitivity. | No. |
| Suspension/revocation/closure | Direction-sensitive. | No. |
| Reactivation/restoration | High authority-increase sensitivity. | No. |

### 68.25 Authority Overlap / Independence Matrix

| Condition | Overlap allowed? | Independence required? |
| --- | --- | --- |
| No beneficiary conflict and low consequence | Potentially. | Only if governance requires. |
| Authority-increasing operation | Conditional. | Often required by operation governance. |
| Compromise or self-benefit | No where sole basis. | Yes where required. |
| Reducing operation | Potentially narrower. | Context-specific. |

### 68.26 Participant Count / Quorum Matrix

| Item | Status |
| --- | --- |
| Participant count | UNRESOLVED / NOT SELECTED |
| Quorum | UNRESOLVED / NOT SELECTED |
| Two-person rule | Not created. |
| Universal dual approval | Not created. |

### 68.27 Root Boundary Matrix

| Item | Rule |
| --- | --- |
| Root | Not default ownership assignment authority. |
| Standing root | Not created. |
| Root succession | Not created. |

### 68.28 Recovery Authority Boundary Matrix

| Item | Rule |
| --- | --- |
| Recovery Authority | Not default assignment authority. |
| Standing Recovery Authority | Not created. |
| Recovery self-continuation | Not authorized. |

### 68.29 TAB Boundary Matrix

| Item | Rule |
| --- | --- |
| TAB | Not assignment authority. |
| TAB instance | Not reusable by model alone. |
| Standing TAB | Not created. |

### 68.30 Source Owner Boundary Matrix

| Item | Rule |
| --- | --- |
| Source owner | Not assignment authority automatically. |
| Current owner | Cannot self-legitimize reassignment. |
| Compromised owner | Cannot self-replace. |

### 68.31 Source Authority Boundary Matrix

| Item | Rule |
| --- | --- |
| Source authority | Not assignment authority automatically. |
| Source legitimacy | Does not perform assignment. |

### 68.32 Responsibility Owner Boundary Matrix

| Item | Rule |
| --- | --- |
| Responsibility owner | Not source ownership assignment authority. |
| Recovery responsibility ownership | Does not imply source ownership authority. |

### 68.33 Mutation / Authorization Boundary Matrix

| Item | Rule |
| --- | --- |
| Mutation owner | Not authorizer. |
| Mutation capability | Not assignment authority. |
| Unauthorized mutation | Not legitimate state change. |

### 68.34 Verification / Authorization Boundary Matrix

| Item | Rule |
| --- | --- |
| Verification | Checks conformance. |
| Authorization | Requires governed authority. |
| Verification alone | Does not authorize. |

### 68.35 Audit / Reconciliation Boundary Matrix

| Item | Rule |
| --- | --- |
| Audit | Not authorization. |
| Reconciliation | Not authority creation. |
| Historical finding | Does not create current authority. |

### 68.36 Authentication / Identity / Credential Matrix

| Item | Rule |
| --- | --- |
| Authentication | Not assignment authority. |
| Identity | Not assignment authority. |
| Credential possession | Not assignment authority. |

### 68.37 Organizational Status Matrix

| Status label | Assignment authority? |
| --- | --- |
| founder, owner, CEO, executive, board | No by status alone. |
| employee, contractor, administrator, security team | No by status alone. |
| developer, auditor | No by status alone. |

### 68.38 Infrastructure Control Matrix

| Control | Assignment authority? |
| --- | --- |
| AWS/IAM/GitHub | No by control alone. |
| database/storage | No by control alone. |
| deployment | No by control alone. |

### 68.39 Human / Machine / AI Matrix

| Item | Authority? |
| --- | --- |
| Human category | Not selected. |
| Machine execution | No business assignment authority. |
| AI/LLM/MCP | Not authoritative. |

### 68.40 BE / Environment Isolation Matrix

| Claim | Result |
| --- | --- |
| BE A authority reused for BE B | Rejected. |
| Non-production authority reused for production | Rejected. |
| Cross-environment replay | Rejected. |

### 68.41 Governance-Version Matrix

| Condition | Result |
| --- | --- |
| Supported version | Potentially valid if all else passes. |
| Unsupported version | No ownership assignment. |
| Obsolete or incompatible version | No silent preservation. |

### 68.42 Replay Prevention Matrix

| Replay vector | Result |
| --- | --- |
| Historical, expired, suspended, revoked, replaced, closed | No assignment. |
| Cross-BE or cross-environment | No assignment. |
| Wrong source, class, operation, target, event | No assignment. |
| Stale authority-source replay | No assignment. |

### 68.43 Minimum-Necessary Authority Matrix

| Expansion claim | Result |
| --- | --- |
| Class X -> all classes | Rejected. |
| Operation X -> all operations | Rejected. |
| Source X -> all sources | Rejected. |
| BE A -> BE B | Rejected. |
| Non-production -> production | Rejected. |

### 68.44 Fail-Closed Matrix

| Failure class | Result |
| --- | --- |
| Missing/invalid/unverifiable/stale authority | No ownership assignment. |
| Suspended/revoked/expired/replaced/closed authority | No ownership assignment or no affected operation. |
| Compromised authority | No authority-increasing operation. |
| Missing SoD or independence | Operation stops. |
| Unauthorized technical mutation | No legitimate ownership change. |

### 68.45 Technology-Neutrality Matrix

| Technology category | Selected? | Authority by itself? |
| --- | --- | --- |
| Cloud/IAM/repository/database/deployment | No | No |
| Identity provider/credential/cryptography | No | No |
| API/runtime/workflow/schema | No | No |

### 68.46 Unresolved-Dependency Matrix

| Order | Unresolved dependency | Depends on |
| --- | --- | --- |
| 1 | Concrete source-ownership assignment authority | This governance and future authority-source governance. |
| 2 | Concrete assignment authority source | Source governance. |
| 3 | Concrete authority holder | Participant eligibility and assignment governance. |
| 4 | Concrete source owner and ownership participants | Ownership assignment authority and participant governance. |
| 5 | Requester, authorizer, mutator, verifier, custodian, revocation, replacement, restoration, closure actors | Participant and operation governance. |
| 6 | Participant categories, participant count, quorum | Participant and SoD governance. |
| 7 | Human/machine allocation | Human/machine governance. |
| 8 | Identity and credential realization | Identity and credential governance. |
| 9 | Persistence, schema, API, workflow, runtime, technology, cryptography, deployment | Implementation governance. |
| 10 | Production authority source, production ownership assignment authority, production source ownership, production Assignment Authority, production participants, production authority | Separate production governance. |

## 69. Normative Invariants

1. Source ownership assignment authority != source ownership.
2. Source ownership assignment authority != Assignment Authority Source.
3. Source ownership assignment authority != source authority.
4. Source ownership assignment authority != responsibility ownership.
5. Source ownership assignment authority != mutation responsibility.
6. Source ownership assignment authority != mutation capability.
7. Source ownership assignment authority != verification.
8. Source ownership assignment authority != custody.
9. Source ownership assignment authority != root.
10. Source ownership assignment authority != Recovery Authority.
11. Source ownership assignment authority != TAB.
12. Source ownership assignment authority != successor authority.
13. Source ownership assignment authority != restoration authority automatically.
14. Source ownership assignment authority != authentication.
15. Source ownership assignment authority != identity.
16. Source ownership assignment authority != credential.
17. Source ownership assignment authority != infrastructure control.
18. Source ownership assignment authority != organizational status.
19. Source ownership assignment authority != AI/LLM/MCP.
20. Assignment execution != assignment legitimacy.
21. Ownership record != assignment authority.
22. Technical mutation success != legitimate assignment.
23. Accountability != automatic authorization.
24. Owner cannot self-create assignment authority.
25. Owner cannot self-legitimize reassignment.
26. Assignment Authority cannot self-establish.
27. Assignment Authority cannot validate its own source as sole basis.
28. Assignment Authority cannot silently extend its own scope.
29. Future owner cannot authorize own initial ownership.
30. Future authority holder cannot be sole basis of own initial authority.
31. Initial assignment requires finite non-circular provenance.
32. Ordinary assignment requires current valid authority.
33. Reassignment cannot launder invalid provenance.
34. Suspension authority != restoration authority.
35. Revocation authority != restoration authority.
36. Revocation owner != revocation authority automatically.
37. Replacement cannot self-legitimize.
38. Closure authority does not create new authority.
39. Reactivation requires current legitimate authority.
40. Prior ownership != restoration authority.
41. Prior Assignment Authority != current restoration authority automatically.
42. Authority Source != authority holder.
43. Authority Source != assignment execution.
44. Authority Source != source owner.
45. Authority Source != mutation owner.
46. Ownership cannot assign itself.
47. Ownership record cannot become authority source by itself.
48. Assignment Authority Source requires governed legitimacy.
49. Assignment Authority lifecycle must be bounded.
50. Historical authority != current authority.
51. Suspended authority != current exercisable authority.
52. Revoked authority != current authority.
53. Expired authority != current authority.
54. Replaced authority != current authority.
55. Closed authority != current authority.
56. Compromised authority cannot perform authority-increasing operation.
57. Current revocation dominates stale positive authority evidence.
58. Revocation unavailable != verified not revoked.
59. Required negative evidence unavailable blocks authority increase.
60. Authority provenance must terminate.
61. Authority provenance must be non-circular.
62. Assignment Authority cannot be own terminating basis.
63. Unavailable != compromised.
64. Unavailability creates no fallback.
65. Compromised authority cannot self-restore.
66. Compromised authority cannot self-replace.
67. Compromised authority cannot suppress revocation.
68. Same TAB governance model != same TAB instance.
69. Beneficiary conflict requires operation-specific analysis.
70. Different people != independent control automatically.
71. Different identities != independent control automatically.
72. Different credentials != independent control automatically.
73. Different systems != independent control automatically.
74. Responsibility independence != participant count.
75. No universal dual approval.
76. No universal maker/checker.
77. No universal two-person rule.
78. No universal quorum.
79. Participant count unresolved/not selected.
80. Quorum unresolved/not selected.
81. Reduction authority != restoration authority.
82. Root != default ownership assignment authority.
83. Recovery Authority != default ownership assignment authority.
84. TAB != standing ownership assignment authority.
85. Source owner != ownership assignment authority automatically.
86. Responsibility owner != ownership assignment authority automatically.
87. Mutation owner != authorizer.
88. Verification != authorization.
89. Audit != authorization.
90. Reconciliation != authority creation.
91. Authentication != ownership assignment authority.
92. Identity != ownership assignment authority.
93. Credential possession != ownership assignment authority.
94. Organizational status != ownership assignment authority.
95. Infrastructure control != ownership assignment authority.
96. Machine execution != business assignment authority.
97. AI/LLM/MCP != authoritative ownership assignment authority.
98. BE A authority != BE B authority.
99. Non-production authority != production authority.
100. Unsupported governance version cannot preserve authority.
101. Historical authority cannot be replayed.
102. Authority must be minimum necessary.
103. Authority must be operation-bound.
104. Authority must be ownership-class-bound where applicable.
105. Authority must be source-bound.
106. Authority must be target-bound.
107. Authority must be BE-bound.
108. Authority must be environment-bound.
109. Authority must be governance-version-bound.
110. Authority must be lifecycle-bound.
111. Authority must be provenance-bound.
112. Required SoD absent -> operation stops.
113. Required independence absent -> operation stops.
114. Invalid authority source -> no ownership assignment.
115. Invalid provenance -> no ownership assignment.
116. Circular provenance -> no ownership assignment.
117. Unauthorized technical mutation != legitimate ownership change.
118. No convenience fallback.
119. No concrete participant selected.
120. No technology selected.
121. No credential or cryptographic mechanism selected.
122. Production authority remains NOT GRANTED.

## 70. Unresolved Decisions

The following decisions remain unresolved in dependency order:

1. concrete source-ownership assignment authority;
2. concrete assignment authority source;
3. concrete authority holder;
4. concrete source owner;
5. concrete ownership participants;
6. concrete responsibility participants;
7. concrete requester;
8. concrete authorizer;
9. concrete mutator;
10. concrete verifier;
11. concrete custodian;
12. concrete revocation actor;
13. concrete replacement actor;
14. concrete restoration actor;
15. concrete closure actor;
16. participant categories;
17. participant count;
18. quorum;
19. human/machine allocation;
20. identity realization;
21. credential realization;
22. persistence;
23. schema;
24. API;
25. workflow;
26. runtime;
27. technology;
28. cryptography;
29. deployment;
30. production authority source;
31. production ownership assignment authority;
32. production source ownership;
33. production Assignment Authority;
34. production participants; and
35. production authority.

## 71. Downstream Dependency

Immediate downstream dependency:

Trusted Authorization Recovery Assignment Authority Source Ownership Assignment
Authority Source Governance Review

This artifact does not perform that dependency.

## 72. Participant Neutrality

No concrete authority holder, source owner, source administrator, assignment
administrator, authorizer, requester, verifier, mutator, custodian, auditor,
revocation actor, replacement actor, restoration actor, or successor is
selected.

No person, team, office, service, organization, founder, owner, CEO, executive,
board, employee, contractor, administrator, security team, developer, auditor,
committee, vendor, or external party is selected.

## 73. Technology Neutrality

No technology is selected.

Technology terms in this artifact appear only as non-selection, boundary,
threat, matrix, predecessor reference, or unresolved dependency.

## 74. Credential / Cryptographic Neutrality

No credential, password, token, key, certificate, signature scheme, hash
algorithm, encryption algorithm, PKI, key hierarchy, HSM topology, threshold
cryptography, secret sharing, multisig, or escrow is selected.

## 75. No Implementation

This artifact creates no source code, tests, runtime model, dataclass, enum,
persistence, schema, database, API, workflow, IAM, credentials, AWS resources,
or deployment.

The implementation repository remains frozen.

## 76. Production Authority

PRODUCTION AUTHORITY: NOT GRANTED

This artifact does not grant or select:

- production ownership assignment authority;
- production Assignment Authority Source;
- production source owner;
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

## 77. Governance Decision Summary

This artifact formalizes:

- MODEL F - HYBRID BOUNDED OWNERSHIP ASSIGNMENT AUTHORITY;
- DERIVATION E - HYBRID BOUNDED DERIVATION;
- RELATIONSHIP E - HYBRID BOUNDED AUTHORITY-DIRECTION RELATIONSHIP;
- Source Ownership Assignment Authority as bounded authority to authorize
  specific ownership operations;
- source ownership, authority source, source authority, root, TAB, Recovery
  Authority, ownership record, mutation, verification, audit, reconciliation,
  authentication, identity, credential, infrastructure control, organizational
  status, machine execution, and AI/LLM/MCP as non-equivalent to assignment
  authority;
- finite non-circular terminating provenance;
- currentness and revocation dominance;
- operation-specific SoD;
- beneficiary-conflict and common-mode dependency controls;
- Business Entity and environment isolation;
- participant count and quorum as unresolved;
- no technology, credential, cryptographic, runtime, or implementation
  selection; and
- production authority as NOT GRANTED.

## 78. Closeout

This artifact stops at governance drafting for Source Ownership Assignment
Authority.

It does not commit, tag, push, deploy, touch AWS, modify the implementation
repository, perform downstream dependency, select participants, select
technology, select credentials, select cryptography, instantiate TAB, activate
Recovery Authority, establish root, establish successor, or authorize
restoration.

PRODUCTION AUTHORITY: NOT GRANTED
