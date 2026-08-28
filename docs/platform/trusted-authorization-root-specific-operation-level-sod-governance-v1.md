# Trusted Authorization Root-Specific Operation-Level SoD Governance v1

Version: v1

## 1. Purpose

This artifact defines deterministic, operation-specific Separation-of-Duties
(SoD) governance for sensitive Trusted Authorization root, succession,
recovery, restoration, authority reduction, mutation, verification, audit, and
closure operations.

It answers:

```text
WHICH LOGICAL RESPONSIBILITIES MUST BE INDEPENDENT
FOR WHICH AUTHORITY OPERATION?
```

It does not answer:

```text
WHICH SPECIFIC PEOPLE PERFORM THEM?
```

This artifact does not establish universal dual approval, universal
maker/checker, universal quorum, universal human approval, fixed participant
count, concrete participants, concrete machine identities, credentials,
authority sources, runtime implementation, or production authority.

## 2. Status

Status: GOVERNANCE ARTIFACT.

Root-specific operation-level SoD governance: GOVERNED CONCEPTUALLY.

Selected SoD model family: MODEL G - HYBRID OPERATION-SPECIFIC SoD.

Concrete Terminating Authority Basis: UNRESOLVED.

Concrete Recovery Terminating Authority Basis: UNRESOLVED.

Concrete root authority source: UNRESOLVED.

Concrete Recovery Authority source: UNRESOLVED.

Concrete authority-source producer or mutator: UNRESOLVED.

Concrete audit or reconciliation authority: UNRESOLVED.

Concrete closure authority: UNRESOLVED.

Concrete participants or machine identities: UNRESOLVED.

Concrete quorum, approval count, or participant count: UNRESOLVED.

Production authority: NOT GRANTED.

This artifact is authorized by the completed read-only Trusted Authorization
Root-Specific Operation-Level Separation-of-Duties Governance Review, which
concluded:

```text
READY TO DRAFT ROOT-SPECIFIC OPERATION-LEVEL SoD GOVERNANCE
```

The selected model family is:

```text
MODEL G - HYBRID OPERATION-SPECIFIC SoD
```

The Trusted Authorization implementation remains closed. That closure does not
grant production authority.

## 3. Controlling Predecessor Governance

This artifact inherits and preserves:

- Trusted Authorization Root / Recovery Topology Governance v1;
- Trusted Authorization Emergency Authority-Reduction Audit-Failure Governance
  v1;
- Trusted Authorization Bounded Recovery Governance v1;
- Trusted Authorization Downstream Authority Impact Governance v1;
- Trusted Authorization Root Lifecycle, Retention, Revocation, and Succession
  Governance v1;
- Trusted Authorization Bootstrap / Root Terminating Authority Source
  Governance v1;
- Trusted Authorization Administrative Mutation and Revocation Ownership
  Governance v1;
- Trusted Authorization Production Authority-Source Ownership Governance v1;
- Administrative Bootstrap / Root Authority Governance v1;
- Authority Administration / Revocation Governance v1;
- Administrative Separation of Duties Governance v1;
- Administrative Separation of Duties Applicability Governance v1;
- Administrative Separation of Duties Operation-Specific Requirement Set
  Governance v1;
- Administrative Separation of Duties Requirement Set Authority / Policy Basis
  Governance v1;
- Principal Mapping Administration Authority Governance v1;
- Principal Mapping Administrative Execution Governance v1;
- Principal Mapping Authority Source Governance v1;
- Principal Mapping Persistence Governance v1;
- Stable Principal Mapping Authority Governance v1;
- Business Entity Administration Authority Governance v1;
- Business Entity Authority Source Governance v1;
- Membership Authority Source Governance v1;
- Principal Membership Entitlement Authority Model v1;
- Entitlement Semantics Governance v1;
- Entitlement Authority Source Governance v1;
- Resource Identity Authority Source Governance v1;
- Governed Resource Identity Lookup Governance v1;
- Resource Provisioning / Classification Binding Governance v1;
- Resource Classification Authority Governance v1;
- Resource Classification Authority Source / Runtime Ownership Governance v1;
- Resource x Action Applicability Governance v1;
- Requested Action Permission Vocabulary Governance v1;
- Deterministic Authorization Decision Semantics v1;
- Runtime Owner Assignment Governance v1;
- Repository Ownership v1; and
- Architecture Conformance Baseline v1 under `docs/governance`.

Where domain-specific predecessor governance is more precise than this
artifact, the domain-specific governance controls.

## 4. Selected SoD Model

The selected model family is:

```text
MODEL G - HYBRID OPERATION-SPECIFIC SoD
```

This model combines:

- operation-specific independence;
- authority-direction sensitivity;
- consequence sensitivity;
- topology alignment;
- deterministic rules;
- fail-closed required SoD;
- stronger treatment for foundational and authority-increasing operations;
- bounded treatment for authority-reducing operations; and
- verification, audit, and reconciliation independence where self-certification
  risk exists.

This model is a governance model family, not a runtime enum, workflow,
identity model, or implementation architecture.

## 5. Operation-Specific, Not Universal

SoD MUST be determined by governed operation requirements.

The same separation MUST NOT be imposed on every mutation merely because state
changes.

Routine bounded administration MUST NOT inherit root or recovery ceremony unless
existing domain governance requires it.

Where a specific operation lacks sufficient current governance to determine its
SoD requirement, the gap remains unresolved and MUST NOT be converted into a
default waiver.

## 6. SoD Is Not Universal Dual Approval

Separation of Duties is not universal two-person approval.

No rule in this artifact means that every sensitive action requires two humans.

Logical responsibility independence may be satisfied differently by future
approved governance and implementation. This artifact does not select
participants, people, identities, or staffing models.

## 7. SoD Is Not Universal Maker/Checker

Not every mutation requires a universal maker/checker pair.

Maker/checker-like separation MAY be required for specific sensitive operations,
including foundational establishment, recovery establishment, restoration,
successor activation, broad authority expansion, and other operations where
approval and mutation collapse would create self-authorization or concentration
risk.

It is not a platform-wide default merely because an operation mutates state.

## 8. SoD Is Not Universal Quorum

No universal quorum is established.

This artifact does not select:

- 2-of-3;
- majority;
- unanimous approval;
- fixed threshold;
- voting mechanism;
- fixed approval count; or
- fixed participant count.

Exact quorum, if ever needed, remains a downstream operation-specific governance
decision.

## 9. Responsibility Independence Is Not Person Count

Logical responsibility independence is not the number of people.

This artifact governs responsibility relationships such as:

- requester;
- terminating-legitimacy authority;
- approval or decision authority;
- affected authority;
- predecessor;
- successor;
- Recovery Authority;
- reduction authority;
- restoration authority;
- authoritative producer or mutator;
- verifier;
- audit evidence producer;
- audit or reconciliation authority; and
- closure authority.

These responsibilities are not mapped to concrete people, accounts, roles,
groups, machine identities, services, or credentials.

## 10. Deterministic SoD

Required SoD MUST be deterministic.

Given the same:

- governed operation;
- target;
- scope;
- authority direction;
- lifecycle;
- Business Entity;
- environment;
- governance/version; and
- required evidence,

the required SoD result MUST NOT depend on AI judgment, probabilistic scoring,
operator preference, runtime heuristic discretion, or administrative
convenience.

Risk-based SoD means that risk has already been translated into governed
operation classes and deterministic rules. It does not mean probabilistic
runtime risk scoring.

## 11. Authority Direction

Authority direction is a governance input for SoD strength.

Authority-increasing operations create, restore, reactivate, expand, revalidate,
or otherwise increase current or future authority effect.

Authority-reducing operations suspend, revoke, narrow, retire, terminate, deny
activation, deny restoration, or otherwise reduce current or future authority
effect.

Authority-neutral operations verify, inspect, audit, reconcile, validate
compatibility, or review evidence without themselves changing authority.

Mixed or lifecycle-transition operations combine directionally different
effects, such as activating a successor while terminating a predecessor.

These are governance concepts only. This artifact does not create runtime
enums.

## 12. Authority-Increasing Operations

Authority-increasing operations receive the strongest SoD scrutiny.

Examples include:

- establishing root or bootstrap authority;
- establishing initial foundational Administrative Authority;
- expanding root scope;
- establishing successor authority;
- activating successor authority;
- establishing Recovery Authority;
- activating Recovery Authority;
- recovery-authorized authority increase;
- restoration or reactivation;
- Administrative Authority expansion;
- establishing new independent provenance; and
- future production authority establishment if separately governed.

This artifact does not authorize any authority-increasing operation.

## 13. Authority-Reducing Operations

Authority-reducing operations may require different SoD from
authority-increasing operations.

Examples include:

- suspension;
- revocation;
- scope narrowing;
- retirement;
- predecessor termination;
- Recovery Authority termination;
- emergency temporary non-usability; and
- emergency authoritative reduction.

Authority reduction MUST NOT automatically inherit authority-increase ceremony.
Containment MUST NOT be made unsafe through excessive procedural delay.

Authoritative destructive reduction still requires bounded safeguards against
malicious denial-of-service, overbroad revocation, and hidden authority
transformation.

## 14. Authority-Neutral Operations

Authority-neutral operations include:

- verification;
- read-only lineage validation;
- provenance inspection;
- audit evidence production;
- audit review;
- reconciliation;
- compatibility validation; and
- status inspection.

Authority-neutral operations MAY require independence where self-certification
risk exists even though they do not themselves increase authority.

Authority-neutral activity MUST NOT become authority creation, authority
restoration, authority mutation, or production authority.

## 15. Operation Classes

The following governance classes are established for conceptual SoD analysis.
They are not runtime enums and do not replace more specific domain governance.

CLASS A - FOUNDATIONAL AUTHORITY ESTABLISHMENT:

- root or bootstrap establishment;
- new independently legitimate authority chain;
- successor establishment after invalid or compromised lineage; and
- Recovery Authority establishment.

CLASS B - AUTHORITY RESTORATION / EXPANSION:

- restoration;
- reactivation;
- scope expansion;
- successor activation; and
- authority-increasing recovery mutation.

CLASS C - ORDINARY GOVERNED AUTHORITY MUTATION:

- routine bounded administrative operations already authorized by domain
  governance.

CLASS D - AUTHORITY REDUCTION:

- suspension;
- revocation;
- narrowing;
- retirement; and
- Recovery Authority termination.

CLASS E - VERIFICATION / AUDIT / RECONCILIATION:

- independent verification;
- audit review;
- reconciliation; and
- closure verification.

An operation MUST NOT be forced into a class where predecessor governance
supports a more specific rule.

## 16. Independence Dimensions

Root-specific operation-level SoD may require independence across these logical
relationships:

| Dimension | Independence question | Governance treatment |
| --- | --- | --- |
| Requester / approver | Can the requester be the sole approver? | Required or conditional by operation |
| Approver / mutator | Can the decision authority be the authoritative mutator? | Required for sensitive operations where collapse creates concentration risk |
| Mutator / verifier | Can the mutator be the sole verifier? | Required where self-certification would establish legitimacy |
| Mutator / auditor | Can the mutator be the sole audit/reconciliation authority? | Required where audit integrity would otherwise depend on the mutation actor |
| Affected authority / approver | Can affected authority solely approve operations on itself? | Prohibited for establishment, expansion, restoration, recovery, self-protection, and revalidation |
| Predecessor / successor | Can predecessor naming alone legitimize successor? | Prohibited |
| Recovered authority / recovery authorizer | Can the recovered authority solely authorize its recovery? | Prohibited |
| Reduced authority / restoration authorizer | Can reduced authority restore itself? | Prohibited |
| Compromised authority / recovery authorizer | Can compromised authority authorize its own recovery? | Prohibited |
| Producer / own authority | Can an authority-source producer be sole source of its own authority? | Prohibited where circular |
| Recovery activator / closure authority | Can recovery activator keep recovery open by self-certifying closure? | Prohibited where closure would preserve residual authority |
| Root / own revocation-restoration | Can root solely control its own revocation or restoration? | Prohibited for restoration; prohibited as sole control over revocation |
| Decision / execution | Can decision and execution collapse? | Conditional by operation |
| Audit evidence producer / reconciler | Can evidence producer be sole reconciler? | Conditional; prohibited where it would defeat reconciliation independence |

Only independence actually required by the governed operation applies.

## 17. Root Establishment SoD

Root or bootstrap establishment is foundational authority creation.

The following responsibilities MUST be independently governed:

- terminating legitimacy;
- authorization or decision;
- authoritative establishment or mutation;
- verification; and
- audit.

ROOT CANNOT SELF-AUTHORIZE.

Founder, owner, CEO, executive, employee, developer, repository owner,
security administrator, infrastructure operator, authentication status,
repository state, IAM permission, Cognito status, AI output, or MCP request
does not satisfy root establishment SoD by itself.

This artifact does not select the Terminating Authority Basis or participants.

## 18. Initial Administrative Authority SoD

The bounded bootstrap path may establish initial bounded Administrative
Authority:

```text
Terminating Authority Basis
-> bounded root/bootstrap operation
-> initial bounded Administrative Authority
```

Root may participate according to topology governance, but root must not become:

- universal administrator;
- universal approver;
- universal mutator;
- universal verifier; or
- universal auditor.

Initial Administrative Authority establishment is authority-increasing and
requires current provenance, lifecycle, scope, applicable SoD, verification,
and audit.

Domain governance remains controlling for the target administrative domain.

## 19. Routine Administration SoD

Routine bounded administration SHOULD follow existing domain-specific
governance.

Root-specific ceremony MUST NOT be imposed merely because authority state
changes.

Principal Mapping and Business Entity authority-relevant operations remain
subject to existing RS-A governance where applicable.

Membership, Entitlement, Resource Identity, Resource Classification, Resource
Binding, and Resource x Action Applicability operation-specific SoD remain
unresolved where predecessor governance leaves them unresolved. This artifact
does not silently resolve them.

## 20. Root Retirement SoD

Root retirement is authority-reducing.

SoD for root retirement must be sufficient to establish:

- correct target;
- valid lifecycle transition;
- no unintended authority preservation;
- provenance and auditability; and
- no self-certified indefinite root.

Root may potentially request its retirement where governed. Requesting
retirement does not itself satisfy approval, mutation, verification, or closure.

Root retirement MUST NOT automatically require restoration-strength SoD.

## 21. Root Suspension SoD

Root suspension must distinguish:

```text
immediate fail-closed non-usability
```

from:

```text
authoritative suspension mutation
```

Suspected compromise must not remain usable solely because ordinary approval
ceremony cannot complete immediately.

Authoritative suspension mutation requires bounded decision, mutation,
verification, audit, and closure controls sufficient to prevent malicious
suspension or overbroad denial-of-service.

Emergency authority-reduction audit-failure governance remains controlling.

## 22. Root Revocation SoD

Root must not be the sole authority controlling whether it may be revoked.

Root revocation SoD must distinguish:

- ordinary revocation;
- planned replacement;
- confirmed compromise;
- never-legitimate root; and
- degraded-audit emergency condition.

Root revocation is authority-reducing, but final or broad revocation may require
stronger independence than temporary suspension or non-usability.

No universal descendant rule is created. Downstream authority impact governance
remains controlling.

## 23. Root Restoration / Reactivation SoD

Restoration or reactivation is authority-increasing.

REDUCED / SUSPENDED / REVOKED AUTHORITY CANNOT RESTORE ITSELF.

Where future governance permits restoration or reactivation, the following must
be independently governed where applicable:

- evidence of resolved condition;
- authorization;
- mutation;
- verification; and
- audit or reconciliation.

This artifact does not authorize actual restoration.

## 24. Root Scope Expansion SoD

Root scope expansion is a high-risk authority increase.

Root cannot be the sole approver of its own expansion.

Broader Business Entity scope, environment scope, operation scope, authority
category scope, or authority-source control may require stronger independence.

This artifact does not authorize expansion.

## 25. Planned Successor Establishment SoD

Planned successor establishment is ordinary governance, not recovery.

Predecessor may participate where governed, but:

```text
PREDECESSOR CANNOT BE SOLE SUCCESSOR LEGITIMIZER
```

Successor establishment requires independent successor provenance appropriate
to the operation, current scope, lifecycle, governance/version compatibility,
verification, and audit.

No participant count is selected.

## 26. Successor Activation SoD

Successor establishment or designation is distinct from successor activation or
exercisability.

Activation is authority-increasing and requires current:

- scope;
- lifecycle;
- provenance;
- governance/version compatibility;
- applicable independent authorization;
- verification; and
- audit.

Successor cannot self-legitimize activation solely because it was named.

## 27. Predecessor Termination SoD

Predecessor termination after succession is authority-reducing but carries
conflict and self-benefit risk.

Governance must prevent:

- successor self-benefit;
- indefinite overlap;
- predecessor persistence;
- conflicting authority; and
- hidden dual-root authority.

Successor participation is not automatically prohibited, but successor alone
MUST NOT be sufficient where the operation would let it eliminate a competing
authority without independent governance.

## 28. Succession Overlap Closure SoD

Where bounded predecessor/successor overlap exists, closure must verify:

- successor validity;
- predecessor intended lifecycle result;
- no unintended residual root authority;
- provenance continuity;
- scope;
- Business Entity and environment boundaries; and
- audit.

The mutating participant must not be sole closure authority where that would
permit self-certification or indefinite overlap.

No overlap duration is selected.

## 29. Recovery Qualification SoD

The authority seeking recovery cannot be the sole authority determining that
recovery is justified.

Recovery qualification must establish that ordinary governance cannot safely
operate.

Recovery qualification must not be established solely by:

- compromised authority;
- lost authority;
- authority seeking restoration;
- infrastructure administrator;
- AI or LLM; or
- MCP.

This artifact does not select the qualifier.

## 30. Recovery Authority Establishment SoD

Event-specific Recovery Authority cannot establish itself.

Recovered authority cannot be the sole basis for recovery.

The following responsibilities must be independently governed where applicable:

- qualifying condition;
- terminating legitimacy;
- authorization;
- authoritative establishment or mutation;
- verification; and
- audit.

This artifact does not select a Recovery Terminating Authority Basis.

## 31. Recovery Authority Activation SoD

Recovery Authority establishment is distinct from Recovery Authority activation.

Activation requires current:

- qualifying event;
- scope;
- lifecycle;
- provenance;
- governance/version compatibility;
- applicable SoD; and
- audit posture or controlling degraded-audit rules.

Recovery Authority cannot activate itself solely because it exists.

## 32. Recovery-Authorized Mutation SoD

Recovery authorization is not arbitrary authority-source mutation authority.

A bounded recovery decision must not automatically make the recovery participant
the universal source producer.

Producer and mutation ownership remain distinct from recovery approval.

Sensitive recovery mutations require operation-specific approver/mutator,
mutator/verifier, and mutator/auditor separation where collapse would create
self-certification or authority concentration.

## 33. Recovery-Authorized Authority Increase SoD

Authority-increasing recovery mutation requires strong SoD.

Examples include:

- establishing replacement Administrative Authority;
- establishing successor authority;
- creating new bounded authority; and
- restoring usability where separately permitted.

Recovery cannot self-certify the legitimacy of its own authority increase.

## 34. Recovery-Authorized Authority Reduction SoD

Recovery-authorized authority reduction applies bounded authority-reduction
SoD.

It MUST NOT automatically require authority-increase ceremony.

It MUST preserve minimum necessary containment, fail-closed behavior,
producer/mutation ownership, verification, audit, and closure where applicable.

## 35. Recovery Verification SoD

The mutator must not be the sole governance verifier where self-certification
would determine recovery legitimacy.

This artifact distinguishes:

- deterministic technical verification;
- independent governance verification; and
- audit review.

Independent verification does not automatically mean another human.

## 36. Recovery Closure SoD

RECOVERY MUST CLOSE.

Recovery closure must establish that:

- intended recovery operation completed or terminated safely;
- resulting authority state is known;
- replacement or successor authority is valid where applicable;
- temporary Recovery Authority is terminated;
- no residual recovery privilege remains;
- required audit or reconciliation is complete or explicitly governed as
  outstanding; and
- anomalies are recorded.

Recovery activator or mutator cannot preserve temporary Recovery Authority by
solely self-certifying closure.

## 37. Future Recovery Event SoD

Historical Recovery Authority and historical SoD evidence cannot authorize a
new recovery event.

A later recovery event requires new current:

- qualification;
- terminating legitimacy;
- scope;
- lifecycle;
- applicable SoD;
- provenance; and
- audit context.

Recovery capability is not standing Recovery Authority.

## 38. Compromised Recovery Authority SoD

Compromised Recovery Authority cannot control:

- its own suspension;
- its own revocation;
- its own replacement;
- its own recovery; or
- its own restoration.

Independent containment and future recovery governance are required where
ordinary paths cannot safely operate.

## 39. Terminating Authority Basis Compromise SoD

A compromised Terminating Authority Basis cannot be the sole authority for:

- declaring itself valid;
- replacing itself; or
- authorizing recovery solely from itself.

This artifact does not solve concrete higher-order basis governance.

Concrete higher-order legitimacy for a compromised or invalid terminating basis
remains downstream and unresolved.

## 40. Emergency Temporary Non-Usability SoD

Emergency temporary non-usability preserves the hybrid emergency
authority-reduction model.

Temporary deterministic fail-closed non-usability may require less prior
ceremony than permanent authoritative revocation.

Governance MUST NOT force credibly compromised authority to remain usable merely
because normal approval or audit paths are degraded.

Controls against malicious denial-of-service remain required through bounded
scope, current evidence where available, verification, audit or reconciliation
where applicable, and closure.

## 41. Emergency Authoritative Reduction SoD

Authoritative reduction under degraded audit requires logical independence
among relevant:

- compromise evidence;
- reduction decision;
- producer or mutation responsibility;
- degraded evidence production;
- verification;
- reconciliation; and
- closure.

This artifact does not select concrete emergency actors.

Emergency conditions do not erase producer ownership, SoD, audit debt, or
closure obligations.

## 42. Restoration After Emergency Reduction SoD

Reduction authority does not imply restoration authority.

Restoration must not occur solely because:

- reducer requests it;
- affected authority requests it;
- recovery participant requests it;
- audit service becomes healthy; or
- infrastructure state changes.

Restoration is a new authority-increasing governance decision.

## 43. Downstream Revalidation SoD

Downstream revalidation cannot launder invalid lineage.

Where revalidation changes current usability, governance must distinguish:

- revalidation decision;
- authoritative mutation;
- verification; and
- audit.

Affected authority cannot be the sole authority declaring itself revalidated.

Downstream authority impact governance remains controlling.

## 44. Independent Reapproval SoD

Independent reapproval must create explicit new provenance.

Invalid or compromised predecessor authority cannot be the sole source of
independent reapproval.

Independent reapproval must not merely relabel compromised lineage.

This artifact does not select the approver.

## 45. Authority-Source Mutation SoD

Decision authority is not mutation authority where governance requires
separation.

Strong candidates for approver/mutator separation include:

- root establishment;
- Recovery Authority establishment;
- successor activation;
- restoration;
- broad authority expansion; and
- sensitive recovery-authorized mutation.

This artifact does not impose separation universally on every low-risk
administrative write unless predecessor governance requires it.

## 46. Mutation Verification SoD

Mutation verification requires independence where mutation correctness or
legitimacy could otherwise be self-certified.

A mutator may potentially perform technical confirmation.

For sensitive operations, technical confirmation by the mutator MUST NOT be the
sole governance evidence of legitimacy where independent verification is
required.

## 47. Audit Evidence Production SoD

This artifact does not require separate human action for every audit record.

A mutator or system may produce audit evidence.

Audit evidence production is not sole audit or reconciliation authority.

Integrity and independent review remain required where applicable governance
requires them.

## 48. Audit / Reconciliation SoD

For sensitive operations, audit and reconciliation must not collapse entirely
into the authority performing mutation where that would permit:

- evidence suppression;
- self-certification;
- unresolved degraded-audit state; or
- hidden residual authority.

This artifact does not select audit infrastructure.

## 49. Closure Authority SoD

Closure applies to:

- bootstrap ceremony;
- planned succession;
- recovery; and
- degraded-audit emergency events.

The operation participant or mutator must not be sole closure authority where
that would permit standing temporary authority, residual privilege, or
self-certification.

This artifact does not select a closure actor.

## 50. Requester / Approver Relationship

Self-request is not universally prohibited.

A principal or authority may potentially request retirement, suspension,
replacement, or another governed operation.

Requesting does not confer approval.

Self-request MUST NOT satisfy required independent authorization for
authority-increasing, self-protective, self-recovery, or self-restoration
operations.

## 51. Approver / Mutator Relationship

Approver and mutator separation is required where operation consequence makes
approval/mutation collapse unsafe.

This includes foundational authority, recovery, restoration, successor
activation, broad expansion, and other operations where a single responsibility
could both authorize and produce its own authority.

This separation is not universal for every administrative write.

## 52. Mutator / Verifier Relationship

Mutator and verifier separation is required where self-verification could
establish legitimacy.

Independence does not necessarily mean another human.

It MUST NOT be required universally for trivial technical confirmation unless
future governance says so.

## 53. Mutator / Auditor Relationship

Mutator and auditor or reconciler separation is required where sole mutator
control over audit or reconciliation would defeat evidence integrity.

This artifact does not create universal manual auditing.

## 54. Affected Authority

Affected authority cannot be sole decision authority for its own:

- establishment;
- authority expansion;
- restoration;
- recovery;
- successor legitimacy;
- prevention of revocation; or
- revalidation after compromise.

Affected authority may potentially request or participate where safe.

Participation is not sole authorization.

## 55. Reversibility

Reversibility is a governance factor for SoD strength.

Governance must distinguish:

- temporary non-usability;
- suspension;
- permanent revocation;
- scope narrowing;
- restoration;
- root establishment;
- successor activation; and
- recovery closure.

Reversibility MUST NOT become heuristic runtime scoring.

## 56. Scope

Scope is a governance factor for SoD strength.

Relevant scope dimensions include:

- one operation;
- one authority;
- one domain;
- one Business Entity;
- multiple Business Entities;
- one environment;
- production; and
- broad authority-source control.

Broader authority impact may require stronger independence.

This artifact does not create universal cross-Business Entity authority.

## 57. Business Entity SoD

Business Entity isolation is preserved.

Cross-Business Entity authority-changing operations, if ever governed, MUST NOT
inherit single-Business Entity SoD assumptions automatically.

This artifact does not authorize cross-Business Entity mutation or select an
enterprise approver.

## 58. Environment SoD

Production, staging, test, and development remain distinct environments.

SoD evidence from one environment MUST NOT automatically satisfy another
environment.

Non-production SoD does not establish production authority.

## 59. Production SoD

This artifact does not design concrete production SoD.

Any future production root or recovery operation requires separately governed:

- production scope;
- production provenance;
- production lifecycle;
- production SoD;
- production authority source;
- production mutation ownership;
- production verification; and
- production audit.

Production authority remains NOT GRANTED.

## 60. Principal Mapping SoD

Existing stronger Principal Mapping RS-A governance is preserved.

This artifact does not weaken, duplicate, or replace it.

Root or recovery SoD does not automatically grant Principal Mapping mutation.

## 61. Business Entity Domain SoD

Existing stronger Business Entity authority-relevant RS-A governance is
preserved.

This artifact does not weaken it.

Root or recovery SoD does not create cross-Business Entity authority.

## 62. Membership SoD

Membership is not Entitlement.

Membership operation-specific SoD remains partially governed or unresolved
where predecessor governance leaves Membership administration unresolved.

This artifact does not silently solve unrelated Membership administration.

## 63. Entitlement SoD

Entitlement is not ALLOW.

This artifact does not use root or recovery SoD to create Entitlement authority.

Entitlement administration SoD remains unresolved where predecessor governance
leaves it unresolved.

## 64. Resource SoD

Resource identity, classification, binding, and applicability governance is
preserved.

Root or recovery SoD does not create universal Resource mutation authority.

Resource administration SoD remains unresolved where predecessor governance
leaves it unresolved.

## 65. Requested Action / Applicability

Requested Action and Applicability cannot create new authority.

Successful SoD cannot authorize an otherwise unsupported action.

Root or recovery SoD does not override Requested Action vocabulary or Resource x
Action Applicability governance.

## 66. SoD And Terminating Authority Basis

A future Terminating Authority Basis may itself contain independently governed
components.

Its internal composition does not automatically satisfy every downstream
operation-level SoD requirement.

Basis legitimacy and operation-level SoD are related but distinct.

This artifact does not select a concrete Terminating Authority Basis.

## 67. Composite Basis

A future composite basis may conceptually include independently governed human
approval evidence and machine-verifiable evidence.

No component self-authorizes.

Composite basis components MUST NOT automatically be treated as:

- two votes;
- quorum;
- dual approval; or
- fixed approval count.

Components may serve different governance functions.

## 68. Multiple Independent Bases

Multiple independent bases do not automatically mean:

- any-one;
- all-of;
- majority;
- quorum; or
- scope union.

Exact combination semantics remain downstream concrete governance.

## 69. SoD And Lineage

Required SoD satisfaction is part of authority legitimacy and provenance.

Technical mutation success does not create legitimate authority when required
SoD failed.

Lineage must preserve applicable SoD evidence or references conceptually.

This artifact does not define schema, graph semantics, persistence, or runtime
lineage implementation.

## 70. Failed SoD

Where required SoD is not satisfied:

- authority-increasing operation must not become legitimate;
- resulting unsupported authority must not become ALLOW-producing merely because
  a write technically occurred;
- later use does not cure failed SoD; and
- audit history alone does not cure failed SoD.

Future bounded independent reapproval or remediation may create new legitimate
provenance if separately governed.

Failed SoD does not retroactively rewrite history.

## 71. Missing / Invalid SoD Evidence

Required SoD evidence that is missing, malformed, stale, conflicting,
unverifiable, unsupported, incompatible with governance/version, out of scope,
or bound to the wrong operation, target, lifecycle, event, Business Entity, or
environment MUST fail closed.

This artifact does not select an evidence schema.

## 72. SoD Replay

Historical SoD evidence must not be replayed to authorize:

- new root;
- future recovery event;
- new successor;
- restoration;
- scope expansion;
- different Business Entity;
- different environment;
- incompatible governance version;
- unrelated target; or
- unrelated operation.

## 73. SoD Scope Binding

Required SoD evidence must conceptually bind to applicable:

- operation;
- target;
- authority;
- scope;
- Business Entity;
- environment;
- lifecycle;
- event; and
- governance/version.

This artifact does not define storage or schema.

## 74. SoD Lifecycle

SoD approval or verification does not remain valid forever merely because it
was once satisfied.

It must remain compatible with current:

- lifecycle;
- event;
- scope;
- authority status; and
- governance/version.

This artifact does not choose timeout values.

## 75. Emergency Audit Failure

Emergency authority-reduction audit-failure governance is preserved.

Audit failure does not permit authority increase.

This artifact MUST NOT require unavailable normal audit infrastructure as the
only path to contain compromised authority.

This artifact does not create emergency bypass authority.

## 76. Malicious Reduction / Denial-of-Service

This artifact governs the tension between rapid containment and malicious
authority reduction.

Temporary fail-closed non-usability may have lighter prior SoD than permanent
authoritative revocation.

Permanent destructive mutation may require stronger independent decision,
verification, reconciliation, or closure controls.

Containment MUST NOT be made impossible.

## 77. Compromise Window

Where compromise scope or time is uncertain, governance should favor bounded
safe posture:

- temporary non-usability;
- bounded suspension;
- independent verification; and
- downstream revalidation.

Immediate permanent restoration or universal revocation MUST NOT be inferred
from uncertain evidence.

Downstream impact governance remains controlling.

## 78. Authentication Non-Authority

Authentication success is not SoD satisfaction.

Cognito, IdP authentication, authentication claims, group membership, session
state, or login status does not independently satisfy required business SoD.

No Cognito integration is authorized.

## 79. Infrastructure Non-Authority

AWS, IAM, GitHub, CI/CD, database, deployment, host, secret, repository, or
filesystem access does not satisfy business SoD merely because infrastructure
access exists.

This artifact does not select infrastructure operators as authority
participants.

## 80. Human Status Non-Authority

Founder, owner, CEO, executive, employee, developer, repository owner, security
administrator, or infrastructure operator status does not automatically satisfy
required SoD.

This artifact does not select concrete humans.

## 81. AI / LLM / MCP Non-Authority

AI and LLM systems cannot independently:

- satisfy SoD;
- act as required independent approver;
- establish root;
- establish Recovery Authority;
- authorize successor;
- authorize restoration;
- authorize revocation;
- authorize mutation;
- establish independent provenance;
- validate their own authority decision; or
- close recovery.

MCP cannot independently satisfy or bypass SoD.

AI may later explain approved deterministic governance or evidence.

## 82. Historical Authorization

SoD governance does not rewrite historical authorization facts.

Governance must distinguish:

- authorization-at-time;
- historical SoD state;
- later-discovered failed SoD;
- current usability; and
- new independent provenance.

History must not be silently rewritten.

## 83. Historical Business Truth

This artifact does not rewrite:

- Assessment Service deterministic truth;
- historical assessments;
- findings;
- recommendations;
- Executive Intelligence Platform historical intelligence; or
- reports.

Authorization legitimacy and current access remain separate from business truth.

## 84. Producer / Consumer Architecture

Existing architecture is preserved.

Assessment Service is the deterministic business truth producer.

Executive Intelligence Platform is a governed consumer and derived intelligence
layer according to existing contracts.

Website / Client Engagement Portal is a presentation consumer.

AI Knowledge Assistant is an explanation consumer using approved knowledge and
authorized data.

Trusted Authorization is the deterministic authorization governance and
evaluation boundary.

None becomes SoD authority merely because it participates in the platform.

## 85. SoD Invariants

The following invariants are governed where supported by predecessor
governance:

1. SoD is operation-specific.
2. No universal dual approval is established.
3. No universal maker/checker is established.
4. No universal quorum is established.
5. Responsibility independence is not person count.
6. Required SoD is deterministic.
7. Required SoD evidence is current and scope-bound.
8. Required SoD failure fails closed.
9. Authority cannot satisfy required SoD solely for itself.
10. Compromised authority cannot satisfy recovery SoD for itself.
11. Reduced authority cannot satisfy restoration SoD for itself.
12. Predecessor cannot be sole successor legitimizer.
13. Recovery Authority cannot establish itself.
14. Recovery Authority cannot activate itself solely from itself.
15. Recovery participant does not automatically gain restoration authority.
16. Reduction authority does not automatically gain restoration authority.
17. Approval authority is not mutation authority where separation is required.
18. Mutation authority is not sole verification authority where separation is
    required.
19. Mutation authority is not sole audit or reconciliation authority where
    separation is required.
20. Root establishment receives stronger scrutiny than routine administration.
21. Restoration receives stronger scrutiny than temporary containment where
    applicable.
22. Temporary fail-closed containment must not be blocked by excessive ceremony.
23. Permanent revocation may require stronger verification than temporary
    non-usability.
24. Recovery qualification is independent from authority seeking recovery where
    required.
25. Recovery closure prevents residual Recovery Authority.
26. Historical SoD evidence cannot be replayed for new authority events.
27. SoD evidence is bound to operation, scope, target, Business Entity,
    environment, lifecycle, event, and governance context.
28. Technical mutation success is not legitimate authority if required SoD
    failed.
29. Audit evidence alone cannot cure failed SoD.
30. Independent reapproval creates new provenance.
31. Authentication is not SoD satisfaction.
32. Infrastructure authority is not SoD satisfaction.
33. Organizational status is not SoD satisfaction.
34. AI, LLM, and MCP cannot independently satisfy SoD.
35. Business Entity isolation remains.
36. Environment isolation remains.
37. Production SoD is separately governed.
38. Historical authorization facts are not rewritten.
39. Historical business truth is not rewritten.
40. Production authority remains NOT GRANTED.

## 86. Threat Model

| Threat | Governance control | Required logical independence | Remaining unresolved dependency |
| --- | --- | --- | --- |
| Root self-approval | Root cannot self-authorize | Root distinct from establishment authorization | Concrete TAB and participants |
| Root self-restoration | Reduced root cannot restore itself | Affected root distinct from restoration authorization | Restoration authority |
| Root blocking own revocation | Root cannot solely control revocation | Affected root distinct from revocation decision | Revocation SoD details |
| Root unilaterally selecting successor | Predecessor alone insufficient | Predecessor distinct from successor legitimacy | Successor authority |
| Predecessor/successor collusion | Bounded overlap and closure | Closure/verifier distinct where required | Exact overlap controls |
| Recovery self-authorization | Recovery cannot establish itself | Recovery authority distinct from recovery authorization | Recovery basis |
| Compromised authority authorizes own recovery | Self-recovery prohibited | Affected authority distinct from recovery qualification | Recovery authority assignment |
| Recovery Authority preserves itself | Recovery must close | Activator/mutator distinct from closure where required | Closure authority |
| Recovery participant gains restoration | Recovery != restoration | Recovery participant distinct from restoration authority | Restoration governance |
| Reducer restores authority it reduced | Reduction != restoration | Reducer distinct from restoration authorization where required | Restoration governance |
| Requester self-approves expansion | Self-increase prohibited | Requester distinct from approver | Exact expansion policy |
| Approver mutates without separation | Approval != mutation where required | Approver distinct from mutator for sensitive operations | Producer assignment |
| Mutator self-verifies | Self-certification prohibited where required | Mutator distinct from verifier | Verification authority |
| Mutator suppresses audit | Audit separation where required | Mutator distinct from audit/reconciliation authority | Audit authority |
| Auditor mutates authority | Audit != mutation | Auditor distinct from mutator where required | Audit/mutation assignment |
| Producer writes own authority | Producer self-authority prohibited | Producer distinct from its own authority basis | Producer authority source |
| Universal dual approval paralysis | No universal dual approval | Operation-specific independence only | Operation-specific policy |
| Universal maker/checker ceremony | No universal maker/checker | Separation only where required | Operation-specific policy |
| Universal quorum lockout | No universal quorum | No fixed count selected | Concrete quorum, if any |
| Insufficient SoD creates super-admin | Operation-specific controls | Duties separated by consequence | Concrete authority model |
| Excessive SoD blocks containment | Temporary containment distinct | Lighter containment pathway | Emergency procedure details |
| Malicious reduction / DoS | Reduction controls and closure | Decision/mutation/verification as needed | Reduction authority |
| Stale SoD replay | Replay rejected | Current evidence required | Evidence schema |
| Cross-BE replay | BE binding required | Scope-bound SoD evidence | Cross-BE governance |
| Cross-environment replay | Environment binding required | Environment-bound SoD evidence | Environment-specific policy |
| Non-prod SoD used for production | Production separately governed | Production-specific SoD required | Production governance |
| Unsupported governance-version SoD | Version compatibility required | Current version evidence | Version migration policy |
| Approval scope widening | Scope-bound SoD evidence | Approver authority bound to scope | Scope policy |
| Lineage laundering | Independent reapproval creates new provenance | Invalid predecessor not sole approver | Reapproval authority |
| Compromised TAB replaces itself | TAB cannot self-replace | Basis distinct from replacement legitimacy | Higher-order basis governance |
| Infrastructure admin satisfies SoD | Infrastructure non-authority | Infra operator not SoD by status | Concrete participants |
| Repository owner satisfies root SoD | Repository ownership non-authority | Repo owner not SoD by status | Concrete participants |
| Founder/CEO status satisfies SoD | Human status non-authority | Org label not SoD | Concrete participants |
| Authentication satisfies SoD | Authentication non-authority | Authenticated principal not sufficient | Identity/authority source |
| AI acts as approver | AI non-authority | AI not independent approver | None for rejection |
| MCP bypasses SoD | MCP non-authority | MCP not authority path | None for rejection |
| Recovery closure self-certification | Closure independence where required | Mutator/activator not sole closure | Closure authority |
| Temporary recovery remains active | Recovery closure required | Closure distinct where required | Recovery lifecycle |
| Audit/reconciliation collapse | Audit distinct from mutation | Mutator not sole reconciler | Audit authority |
| Restoration as simple undo | Restoration is authority-increasing | Restoration authority distinct | Restoration governance |
| Reduction/increase treated identically | Direction-sensitive SoD | Different controls by direction | Operation-specific policy |
| Technical success treated as legitimacy | Failed SoD fails closed | Technical writer not legitimacy source | Runtime/evidence implementation |

## 87. Operation-Level SoD Matrix

Legend:

- RA = requester/approver separation.
- AM = approver/mutator separation.
- MV = mutator/verifier separation.
- MA = mutator/audit or reconciliation separation.
- AA = affected-authority independence.
- PS = predecessor/successor independence.
- RI = recovery independence.

| # | Operation | Direction | Class | Consequence and reversibility | Key risks | Required independence | Audit/reconciliation | BE/env sensitivity | SoD strength | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Establish Terminating Authority Basis | Increase/foundational | A | New legitimacy; high impact | Self-basis, circularity, concentration | RA, AM, MV, MA, AA as applicable | Required | Scope-bound; production separate | Strongest | UNRESOLVED |
| 2 | Establish root/bootstrap authority | Increase/foundational | A | Creates root event; high impact | Root self-authority | RA, AM, MV, MA, AA | Required | BE/env bound | Strongest | PARTIALLY GOVERNED |
| 3 | Establish initial Administrative Authority | Increase | A | Creates foundational admin | Root super-admin drift | RA, AM, MV, MA, AA | Required | Domain-bound | Strong | PARTIALLY GOVERNED |
| 4 | Routine Administrative Authority mutation | Mixed | C | Bounded domain change | Over-ceremony, domain bypass | Existing domain SoD | Required by domain | Domain-bound | Existing policy | PARTIALLY GOVERNED |
| 5 | Expand Administrative Authority | Increase | B | Wider authority | Self-expansion | RA, AM, MV, MA, AA | Required | Scope/BE/env | Strong | PARTIALLY GOVERNED |
| 6 | Retire root | Reduction | D | Root non-standing | Self-certified persistence | MV, MA, closure independence where required | Required | Root scope | Moderate | PARTIALLY GOVERNED |
| 7 | Suspend root | Reduction | D | Temporary reduction | DoS, delayed containment | AA, AM/MV/MA for authoritative suspension | Required or degraded | Scope unknown conservative | Moderate/strong | PARTIALLY GOVERNED |
| 8 | Revoke root | Reduction | D | Final reduction | DoS, descendant impact | AA, AM, MV, MA | Required | Cause/scope sensitive | Strong | PARTIALLY GOVERNED |
| 9 | Restore/reactivate root | Increase | B | Restores authority | Self-restoration | RA, AM, MV, MA, AA | Required | Root scope; production separate | Strongest | UNRESOLVED |
| 10 | Establish planned successor | Increase | A/B | Future root/admin continuity | Sole predecessor naming | RA, AM, MV, MA, PS | Required | Scope-bound | Strong | PARTIALLY GOVERNED |
| 11 | Activate successor | Increase | B | Makes successor usable | Self-legitimation | RA, AM, MV, MA, PS, AA | Required | Scope-bound | Strong | UNRESOLVED |
| 12 | Terminate predecessor | Reduction/mixed | D | Ends predecessor | Successor self-benefit | PS, MV, MA, closure independence | Required | Scope-bound | Moderate/strong | PARTIALLY GOVERNED |
| 13 | Close succession overlap | Neutral/reducing | E | Ends dual authority | Indefinite overlap | MV, MA, PS where applicable | Required | Scope-bound | Strong | PARTIALLY GOVERNED |
| 14 | Determine recovery qualification | Neutral/enabling | E/A | Enables recovery | Self-recovery | RA, AA, RI | Required | Event/scope bound | Strong | PARTIALLY GOVERNED |
| 15 | Establish Recovery Authority | Increase/foundational | A | Creates event authority | Recovery self-authority | RA, AM, MV, MA, AA, RI | Required | Event/BE/env bound | Strongest | PARTIALLY GOVERNED |
| 16 | Activate Recovery Authority | Increase | B | Makes recovery usable | Self-activation | RA, MV, MA, AA, RI | Required/degraded rules | Event/scope bound | Strong | UNRESOLVED |
| 17 | Recovery-authorized authority increase | Increase | B | Creates/restores authority | Recovery super-admin | RA, AM, MV, MA, AA, RI | Required | Target scope | Strongest | UNRESOLVED |
| 18 | Recovery-authorized authority reduction | Reduction | D | Contains/removes authority | DoS, overreach | AA, AM/MV/MA as applicable, RI | Required/degraded rules | Target scope | Moderate/strong | PARTIALLY GOVERNED |
| 19 | Recovery-authorized replacement/successor establishment | Increase/foundational | A | New chain or successor | Lineage laundering | RA, AM, MV, MA, PS, RI | Required | Scope/version | Strongest | UNRESOLVED |
| 20 | Verify recovery mutation | Neutral | E | Legitimacy evidence | Self-certification | MV, MA | Required | Event-bound | Strong | PARTIALLY GOVERNED |
| 21 | Close recovery | Neutral/reducing | E/D | Terminates recovery | Residual authority | MV, MA, RI, closure independence | Required | Event-bound | Strong | PARTIALLY GOVERNED |
| 22 | Establish future recovery event | Increase/foundational | A | New event authority | Replay | RA, AM, MV, MA, AA, RI | Required | Event-bound | Strongest | UNRESOLVED |
| 23 | Suspend compromised Recovery Authority | Reduction | D | Contains recovery | Self-preservation | AA, AM/MV/MA as applicable | Required/degraded rules | Event-bound | Strong | UNRESOLVED |
| 24 | Revoke compromised Recovery Authority | Reduction | D | Ends recovery authority | Self-preservation, DoS | AA, AM, MV, MA | Required | Event-bound | Strong | UNRESOLVED |
| 25 | Restore/reactivate previously reduced authority | Increase | B | Restores usability | Self-restoration | RA, AM, MV, MA, AA | Required | Target scope | Strong | UNRESOLVED |
| 26 | Emergency temporary non-usability | Reduction/runtime | D | Immediate DENY; reversible | DoS vs compromise | AA where applicable; verification after | Evidence where possible | Scope unknown conservative | Bounded | PARTIALLY GOVERNED |
| 27 | Emergency authoritative suspension | Reduction | D | Authoritative temporary reduction | DoS, audit degradation | RA/AA, AM, MV, MA | Degraded evidence and reconciliation | Scope-bound | Strong | PARTIALLY GOVERNED |
| 28 | Emergency authoritative revocation | Reduction | D | Final reduction | Malicious revocation | RA/AA, AM, MV, MA | Degraded evidence and reconciliation | Scope-bound | Strong | PARTIALLY GOVERNED |
| 29 | Emergency scope narrowing | Reduction | D | Narrows authority | Hidden transformation | RA/AA, AM, MV, MA | Required/degraded rules | Scope-bound | Moderate/strong | PARTIALLY GOVERNED |
| 30 | Reconcile degraded-audit mutation | Neutral | E | Resolves audit obligation | Self-certification | MA, MV | It is reconciliation | Event-bound | Strong | UNRESOLVED |
| 31 | Close degraded-audit event | Neutral/reducing | E | Ends unresolved event | Silent discard | MV, MA, closure independence | Required | Event-bound | Strong | UNRESOLVED |
| 32 | Downstream revalidation | Increase/neutral | B/E | May restore usability | Lineage laundering | RA, AM/MV/MA, AA | Required | BE/env/version | Strong | PARTIALLY GOVERNED |
| 33 | Independent reapproval | Increase/provenance | A/B | New provenance | Invalid predecessor | RA, AA, PS where applicable | Required | Scope-bound | Strong | PARTIALLY GOVERNED |
| 34 | Authoritative source mutation | Mixed | C/D/B | Writes authority state | Producer overreach | AM, MV, MA where required | Required | Source/domain bound | Operation-specific | PARTIALLY GOVERNED |
| 35 | Mutation verification | Neutral | E | Confirms result | Self-verification | MV | Required where material | Target-bound | Moderate/strong | PARTIALLY GOVERNED |
| 36 | Audit evidence production | Neutral | E | Evidence creation | Evidence control | MA where required | Required | Event-bound | Bounded | GOVERNED |
| 37 | Audit review | Neutral | E | Review evidence | Auditor mutation | MA | Required where material | Event-bound | Moderate/strong | PARTIALLY GOVERNED |
| 38 | Reconciliation | Neutral | E | Establishes audit truth | Self-reconciliation | MA, MV | Required | Event-bound | Strong | UNRESOLVED |
| 39 | Bootstrap closure | Neutral/reducing | E | Ends bootstrap ceremony | Residual root | MV, MA, closure independence | Required | Bootstrap scope | Strong | PARTIALLY GOVERNED |
| 40 | Succession closure | Neutral/reducing | E | Ends transition | Double-root | MV, MA, PS | Required | Scope-bound | Strong | PARTIALLY GOVERNED |
| 41 | Root scope expansion | Increase | B | Widens root | Super-admin drift | RA, AM, MV, MA, AA | Required | BE/env/production | Strongest | UNRESOLVED |
| 42 | Cross-BE authority mutation | Mixed/increase | B/C | Cross-BE effect | Isolation breach | RA, AM, MV, MA, AA | Required | Cross-BE strong | Strongest | UNRESOLVED |
| 43 | Production root establishment | Increase/foundational | A | Production root | Production risk | RA, AM, MV, MA, AA | Production audit required | Production separate | Strongest | UNRESOLVED |
| 44 | Production recovery establishment | Increase/foundational | A | Production recovery | Production super-admin | RA, AM, MV, MA, AA, RI | Production audit required | Production separate | Strongest | UNRESOLVED |
| 45 | Governance-version migration affecting authority | Mixed | B/E | Changes interpretation | Version laundering | RA, AM/MV/MA as applicable, AA | Required | Version/scope | Strong | UNRESOLVED |

## 88. Responsibility-Relationship Matrix

| Relationship | May be same responsibility? | Must be independent? | Conditionally independent? | Prohibited self-authorization or circularity | Status |
| --- | --- | --- | --- | --- | --- |
| Requester / approver | Yes for operations where governance permits | Yes for self-increase, recovery, restoration, and sensitive establishment | Yes | Request alone cannot approve itself where separation applies | PARTIALLY GOVERNED |
| Terminating legitimacy / root | No as sole authority | Yes | Yes | Root cannot be its own terminating basis | GOVERNED |
| Approver / affected authority | Not for self-increase/restoration/recovery | Yes in listed sensitive cases | Yes | Affected authority cannot solely authorize itself | GOVERNED |
| Approver / mutator | Sometimes | Yes for sensitive operations | Yes | Approval/mutation collapse cannot create authority | PARTIALLY GOVERNED |
| Mutator / verifier | Technical confirmation may overlap | Yes where self-certification risk exists | Yes | Mutator cannot solely verify legitimacy where separation required | PARTIALLY GOVERNED |
| Mutator / audit/reconciliation | Evidence production may overlap | Yes where audit integrity risk exists | Yes | Mutator cannot be sole reconciler where separation required | PARTIALLY GOVERNED |
| Predecessor / successor legitimizer | Participation allowed | Sole legitimization prohibited | Yes | Predecessor naming alone insufficient | GOVERNED |
| Successor / predecessor terminator | Participation possible | Required where self-benefit risk exists | Yes | Successor cannot exploit termination without governance | PARTIALLY GOVERNED |
| Recovery Authority / recovery establisher | No as sole source | Yes | Yes | Recovery cannot establish itself | GOVERNED |
| Recovered authority / recovery authorizer | No as sole source | Yes | Yes | Self-recovery prohibited | GOVERNED |
| Recovery activator / recovery closure | Sometimes | Required where residual authority risk exists | Yes | Activator cannot keep recovery open by self-certification | PARTIALLY GOVERNED |
| Reduction authority / restoration authority | Not by implication | Yes for restoration | Yes | Reducer does not inherit restoration | GOVERNED |
| Restoration authority / affected authority | Not sole affected authority | Yes where affected authority reduced | Yes | Reduced authority cannot restore itself | GOVERNED |
| Producer / its own authority source | No where circular | Yes where writes own authority | Yes | Producer-created authority cannot legitimize producer | GOVERNED |
| Audit evidence producer / reconciler | Sometimes evidence producer only | Yes where reconciliation integrity required | Yes | Evidence production cannot self-reconcile authority | PARTIALLY GOVERNED |
| Closure authority / mutator | Sometimes | Yes for recovery, succession overlap, degraded audit where required | Yes | Mutator cannot self-close residual privilege | PARTIALLY GOVERNED |

## 89. Authority-Direction Matrix

| Direction | Default independence posture | Self-authorization concern | Mutation separation | Verification requirement | Audit requirement | Emergency treatment | Restoration treatment |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Authority increase | Strong independent authorization and evidence | High | Required where sensitive | Required | Required | Must fail closed under audit failure | Restoration is separate increase |
| Authority reduction | Bounded, scope-sensitive independence | Medium to high for self-protection and DoS | Required for authoritative mutation where sensitive | Required where material | Required or degraded rules | Temporary containment may be faster | Does not imply restoration |
| Authority-neutral verification | Independent where self-certification risk exists | Low unless it validates own mutation | Not mutation | Required by function | Required where material | Supports containment/reconciliation | Cannot restore |
| Mixed lifecycle transition | Operation-specific combination | High where activation and termination combine | Required where sensitive | Required | Required | Use safest direction-specific controls | Restorative part treated as increase |

## 90. Root Operation Matrix

| Root operation | Logical separations supported by governance | Status |
| --- | --- | --- |
| Establish root | Terminating legitimacy, decision, mutation, verification, and audit independent where required | PARTIALLY GOVERNED |
| Use root for initial administration | Root may participate but not become universal admin/mutator/verifier/auditor | PARTIALLY GOVERNED |
| Retire root | Lifecycle verification and closure prevent indefinite exercisable root | PARTIALLY GOVERNED |
| Suspend root | Runtime non-usability distinct from authoritative suspension; affected root not sole controller | PARTIALLY GOVERNED |
| Revoke root | Affected root not sole controller; cause-sensitive downstream impact | PARTIALLY GOVERNED |
| Restore root | Reduced root cannot self-restore; strong independent restoration controls required | UNRESOLVED |
| Expand root | Root not sole approver; broad scope requires stronger independence | UNRESOLVED |
| Replace root | Replacement requires independent provenance, producer ownership, verification, and audit | PARTIALLY GOVERNED |
| Establish successor | Predecessor may participate but cannot be sole legitimizer | PARTIALLY GOVERNED |
| Activate successor | Activation separate from designation; current evidence and independent authorization required | UNRESOLVED |
| Terminate predecessor | Successor not sole terminator where self-benefit risk exists | PARTIALLY GOVERNED |
| Close overlap | Closure verifies no residual conflicting root authority | PARTIALLY GOVERNED |

## 91. Recovery Operation Matrix

| Recovery operation | Where recovery participant cannot be sole authority | Status |
| --- | --- | --- |
| Qualify recovery event | Cannot be sole qualifier when seeking recovery or affected by recovery | PARTIALLY GOVERNED |
| Establish Recovery Authority | Cannot establish itself; recovered authority cannot be sole basis | PARTIALLY GOVERNED |
| Activate Recovery Authority | Cannot activate itself solely because it exists | UNRESOLVED |
| Recovery mutation | Cannot become arbitrary source producer or sole verifier | UNRESOLVED |
| Verify recovery mutation | Cannot self-certify legitimacy where separation required | PARTIALLY GOVERNED |
| Establish replacement/successor | Cannot launder compromised lineage or self-legitimize replacement | UNRESOLVED |
| Terminate affected invalid authority | Cannot use recovery as arbitrary revocation authority | PARTIALLY GOVERNED |
| Close recovery | Cannot preserve itself by self-certified closure | PARTIALLY GOVERNED |
| Establish later recovery event | Cannot replay historical Recovery Authority or historical SoD evidence | UNRESOLVED |

## 92. Emergency Reduction SoD Matrix

| Emergency reduction operation | SoD treatment | Status |
| --- | --- | --- |
| Temporary runtime non-usability | Bounded containment; lighter prior ceremony; verification and closure where applicable | PARTIALLY GOVERNED |
| Authoritative suspension | Independent reduction basis, producer/mutation, degraded evidence, verification, reconciliation, closure | PARTIALLY GOVERNED |
| Authoritative revocation | Stronger than suspension; finality and DoS risk require stronger verification and reconciliation | PARTIALLY GOVERNED |
| Scope narrowing | Explicit, minimum necessary, producer-controlled, scope-bound, reconcilable | PARTIALLY GOVERNED |
| Degraded evidence production | Evidence does not equal normal audit or authority; producer not sole reconciler where required | PARTIALLY GOVERNED |
| Reconciliation | Required after degraded-audit mutation; cannot restore authority by itself | UNRESOLVED |
| Closure | Must resolve or govern outstanding audit obligation; no silent discard | UNRESOLVED |
| Later restoration | Separate authority-increasing operation; reducer and affected authority not sole basis | UNRESOLVED |

## 93. Explicit Unresolved Decisions

The following decisions remain unresolved in dependency order:

1. Concrete Terminating Authority Basis.
2. Concrete Recovery Terminating Authority Basis.
3. Same, distinct, multiple, or composite basis realization.
4. Concrete root authority source.
5. Concrete Recovery Authority source.
6. Concrete participants.
7. Concrete machine identities.
8. Concrete producer or mutation authority.
9. Concrete audit, reconciliation, and closure authority.
10. Exact restoration or reactivation authority.
11. Exact root-specific participant counts, if any.
12. Exact quorum, if any.
13. Exact approval counts, if any.
14. Concrete topology representation.
15. Credentials, accounts, secrets, keys, certificates, or HSMs.
16. Persistence, schemas, APIs, service contracts, runtime, and workflow.
17. Deployment.
18. Production authority.

## 94. Technology Neutrality

This artifact does not select or authorize:

- Cognito;
- IAM;
- AWS Organizations;
- CloudWatch;
- DynamoDB;
- RDS;
- S3;
- KMS;
- Secrets Manager;
- Lambda;
- API Gateway;
- EventBridge;
- SNS;
- SQS;
- Step Functions;
- GitHub;
- CI/CD;
- database;
- graph database;
- event store;
- queue;
- local file;
- cache;
- HSM;
- hardware token;
- credential;
- key;
- certificate;
- identity provider;
- schema;
- API;
- UI;
- runtime service; or
- workflow engine.

Named technologies, where mentioned, establish non-authority boundaries only.

## 95. Strict Out Of Scope

This artifact does not authorize or perform:

- implementation;
- SoD implementation;
- actor assignment;
- participant selection;
- root creation;
- root activation;
- root retirement execution;
- root revocation execution;
- root restoration;
- root replacement execution;
- successor execution;
- Recovery Authority creation;
- recovery activation;
- recovery mutation;
- recovery closure execution;
- restoration or reactivation;
- emergency authority reduction;
- authoritative source mutation;
- concrete Terminating Authority Basis;
- concrete Recovery Terminating Authority Basis;
- concrete authority source;
- concrete producer;
- concrete auditor;
- concrete approver;
- concrete verifier;
- concrete closure authority;
- credential;
- account;
- secret;
- key;
- certificate;
- HSM;
- identity provider;
- Cognito;
- IAM business authorization;
- AWS integration;
- persistence;
- schema;
- API;
- runtime wiring;
- Website or Portal integration;
- Executive Intelligence Platform integration;
- Assessment Service integration;
- Lambda enforcement;
- deployment;
- production data access;
- production authorization enforcement;
- production authority-source integration;
- break-glass;
- standing super-admin;
- universal quorum;
- universal dual approval;
- AI authority; or
- MCP authority.

## 96. Production Authority

THIS ARTIFACT DOES NOT GRANT PRODUCTION AUTHORITY.

Production authority remains:

```text
NOT GRANTED
```

No SoD model, independence relationship, operation class, participant concept,
root concept, Recovery Authority concept, Terminating Authority Basis concept,
governance artifact, repository, account, credential, service, infrastructure
authority, human organizational status, authentication status, AI output, or MCP
request becomes production authority because this document exists.

This artifact grants no actual:

- root authority;
- Recovery Authority;
- successor authority;
- containment execution authority;
- suspension authority;
- revocation authority;
- mutation authority;
- restoration authority;
- audit waiver;
- deployment authority;
- production data access;
- production enforcement authority; or
- production authority-source integration.

## 97. Next Dependency Analysis

This artifact closes the conceptual root-specific operation-level SoD dependency
well enough to proceed to the next governance dependency.

The next dependency is not implementation. It is not actor assignment. It is not
credential selection. It is not production authority.

The next unresolved dependency exposed by this artifact is the concrete
governance basis that can legitimately terminate root and recovery authority
chains without circularity, self-authorization, infrastructure-derived business
authority, organizational-status-derived business authority, or standing
break-glass.

Therefore the next governed step should be:

```text
Trusted Authorization Concrete Terminating Authority Basis Governance Review
```

This step is only recommended. It is not performed by this artifact.

## 98. Scope Conformance

This artifact is governance documentation only.

It creates no runtime code, no implementation plan, no AWS resource, no
credential, no account, no authority source, no root authority, no Recovery
Authority, no successor authority, no production authority, and no deployment.

It preserves repository ownership and producer/consumer boundaries.

## 99. Closeout

Root-Specific Operation-Level SoD Governance v1 is ready for human review as a
bounded governance artifact when repository validation confirms:

- exactly this artifact is newly untracked;
- no tracked files changed;
- whitespace validation passes;
- the implementation repository remains untouched;
- production authority remains NOT GRANTED; and
- no commit, tag, push, deployment, AWS action, authority creation, credential
  creation, actor selection, quorum selection, or universal dual approval was
  performed.
