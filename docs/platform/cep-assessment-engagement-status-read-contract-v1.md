# CEP Assessment Engagement Status Read Contract v1

Version: v1

Status: bounded nonproduction governance contract. No live status delivery or
production authority is activated.

## 1. Purpose and boundary

Define the minimum versioned contract for a future authorized, client-facing
read of **Assessment Engagement context currentness**. This contract closes
the status-vocabulary and delivery-shape gap only to the extent supported by
existing governed Engagement facts. It is not an assessment workflow,
progress, submission, completion, report, or Executive Dashboard contract.
No runtime implementation, authority record, source integration, Website
route, or new authorization permission is established here.

## 2. Governing decisions and ownership

[Assessment Submission Business Context Governance v1](trusted-authorization-assessment-submission-business-context-governance-v1.md)
§§3, 6–18, 20–25, 28–29 and [Assessment Engagement Context Legitimacy
Governance v1](trusted-authorization-assessment-engagement-context-legitimacy-governance-v1.md)
§§3–5, 8–13, 34–36, 43–47, 53–56, 60–65 establish the relevant boundaries.
[Resource × Action Applicability Governance v1](resource-action-applicability-governance-v1.md)
§§68, 70–71 fixes the current matrix. [Portal Governed Delivery Authorization
Model v1](portal-governed-delivery-authorization-model-v1.md) §§3–8, 11–13,
17–18 governs the trusted release and non-disclosure principles for its
existing EIP delivery use case; this contract does not extend that use case
or its permissions. Versioned contracts preserve producer meaning and reject
unsupported versions under [Platform Integration Baseline v1](platform-integration-baseline-v1.md).

The logical Assessment Engagement authority source and Assessment Engagement
Establishment Authority own E identity, immutable E -> B, establishment
provenance, and engagement currentness. The Business Entity authority owns B's
independent currentness. Assessment Engagement Participation Authority owns
Participation(P,E); trusted current-attempt Binding(A,E) is a separate
context fact for Assessment Submission. Trusted Authorization composes
principal/Resource/action authorization from current authoritative evidence;
it does not establish E or B. The Website is a presentation consumer. The
Assessment Service owns deterministic assessment truth; EIP owns its existing
executive intelligence and dashboard projection. Neither owns Engagement
status by implication. Concrete production Engagement source ownership,
currentness producer, persistence, and delivery runtime remain unresolved
and are **not granted** by this document.

## 3. Engagement context currentness is not assessment progress

The governed minimum lifecycle distinguishes a not-yet-authoritative or
candidate E, a current and eligible E, and a no-longer-current E. The
nonproduction synthetic source represents these as `CANDIDATE`, `CURRENT`,
and `NON_CURRENT` in
`src/trusted_authorization/non_production_assessment_engagement_source.py`
of `aws-ai-knowledge-assistant`. Those implementation enum names are not
client assessment workflow states and do not establish live authority.

This v1 read contract uses the narrowly defined field
`engagementContextCurrentness` with only these display meanings:

| Contract value | Governed meaning | Display-safe label and limit |
| --- | --- | --- |
| `CURRENT_AND_ELIGIBLE` | Authoritatively established E is current and eligible to supply its B context for a **new Assessment Submission**, subject to all other required context and permission checks. | “Current engagement.” This does not mean this Principal may submit or view anything else. |
| `NO_LONGER_CURRENT` | Authoritatively established E remains historically attributable to its immutable B but is no longer current for **new Assessment Submission business-context derivation**. | “No longer current.” This does not disclose why or imply assessment completion. Release still requires a separately authorized status-read permission covering this E. |

`CANDIDATE` and unknown, missing, stale, ambiguous, conflicting, or
unverifiable lifecycle evidence have **no client-facing governed status** in
v1 and must fail closed. The two contract values translate existing approved
currentness semantics; they do not create new Engagement authority states or
approve the synthetic enum as a production vocabulary. No `started`,
`in_progress`, `submitted`, `completed`, percentage, question count,
methodology-derived milestone, or report-readiness state is authorized.

## 4. Exact identity and Business Entity binding

The trusted read must resolve one exact stable Engagement E, including when a
caller supplies E only as a candidate selector. It must verify one
authoritatively established, immutable E -> B binding, current authoritative B
for this v1 read, establishment provenance, and the
Engagement lifecycle state under a coherent current source revision.
Identifier allocation, a matching Business Entity from Membership, a prior
selection, or browser-supplied B cannot establish these facts. One B may have
multiple E values; same-B substitution remains invalid. Conflicting E -> B,
wrong E, wrong B, revoked E, or missing provenance fail closed. Historical
E -> B attribution remains intact when E becomes non-current.

Participation(P,E) may support context legitimacy for the separately governed
Assessment Submission operation. It neither establishes E currentness nor
grants status-read permission. A status read must independently require a
fresh permission for its exact governed Resource and action.

## 5. Minimum trusted contract fields

The following are conceptual field names for this v1 read contract, not a
production API or storage schema. A future implementation may choose a
serialization only if it preserves these exact meanings and version boundary.

| Field | Required validation | Release classification |
| --- | --- | --- |
| `contractVersion` | Exact supported value `cep-assessment-engagement-status-read-contract-v1`; missing, unknown, or incompatible version rejects. | Display-safe envelope field after authorization. |
| `engagementReference` | Exact, nonempty, unambiguous governed E matching the requested Resource scope and source evidence. | May be released only to the authorized consumer for that E; no cross-B disclosure. |
| `businessEntityReference` | Exactly one authoritative immutable E -> B, with independently current B evidence; never from caller selection. | Server-only for binding and authorization by default. |
| `engagementContextCurrentness` | Exactly one of §3's two values, translated from current authoritative Engagement evidence; candidate and unknown reject. | Display-safe value after authorization. |
| `displayLabel` | Exact approved label corresponding to the verified currentness value; no free-form source or browser text. | Display-safe after authorization. |
| `limitations` | Must say this is Engagement context currentness only; no assessment progress, completion, SUBMIT permission, or report access. | Display-safe, required. |
| `sourceAuthorityReference` and `establishmentProvenanceReference` | Bind E, E -> B, and lifecycle to the authoritative logical source; absence or mismatch rejects. | Server-only. |
| `sourceRevision` and `currentnessEvidence` | Identify the applicable source revision and evidence of current or non-current state, including relevant revocation/supersession and coherent read timing; missing, stale, or conflicting evidence rejects. No physical revision format is selected. | Server-only. |
| `governanceVersionContext` | Identify the applicable Engagement/currentness and read-contract governance interpretation; incompatible context rejects. | Server-only except `contractVersion`. |
| `authorizationDecisionReference` and `auditCorrelationReference` | Trace the fresh exact-Resource/action decision and release attempt without embedding raw authority records. | Server-only. |

The trusted server-side envelope contains all required fields and evidence
references. Only `contractVersion`, authorized `engagementReference`,
`engagementContextCurrentness`, `displayLabel`, and `limitations` may cross to
the Website. The browser receives no raw Principal identifier, Participation,
Membership, Entitlement, evaluator record, source revision/evidence, B
reference by default, or sensitive authority-source detail. If the display
does not need `engagementReference`, it may be omitted from the client-safe
view while remaining mandatory server-side. No partial client-safe view may
be released when any required server-side field fails validation.

## 6. Future authorization and trusted release gate

The current applicability matrix governs `EXECUTIVE_DASHBOARD × VIEW`,
`REPORT × VIEW/DOWNLOAD`, and `ASSESSMENT_SUBMISSION × SUBMIT`; it marks
`ASSESSMENT_SUBMISSION × VIEW` **NOT APPLICABLE**. There is no approved
Assessment Engagement status-read Resource/action entry. Neither dashboard
VIEW nor Submission VIEW may be reused for this contract. This document does
not modify the matrix or grant a permission.

Before any protected status fields leave a trusted server-side release
boundary, a separately approved applicability decision must identify the
exact governed status-read Resource class/reference and applicable action;
Resource Identity authority must establish its exact E/B scope. The trusted
boundary must verify current authentication and Principal Mapping, current
Business Entity and applicable Membership/Entitlement, exact Resource/action
applicability, a fresh Trusted Authorization ALLOW for that Resource/action,
current Engagement source evidence, and no intervening revocation or scope
change. It must recheck required current facts immediately before release,
preserve decision and source audit references, and expose zero protected
fields on DENY, missing authority, source unavailability, stale or conflicting
revisions, version incompatibility, or failed integrity. Denial must not
reveal whether another B's E or status exists.

The future applicability decision, Resource identity/scope contract, source
realization, and authorized delivery boundary are **implementation gates**.
This document supplies their minimum read requirements; it does not approve
their production realization or make synthetic fixture data authoritative.

## 7. Website, EIP, and report separation

A future CEP Website consumer may present only the explicitly authorized
display-safe fields in §5. It must not invent lifecycle states, calculate
assessment progress, infer submission or completion, recalculate results,
accept browser-selected B as authority, turn Participation into permission,
or expose internal authorization evidence. The EIP Executive Dashboard
projection and `website-projection-delivery-contract-v1` remain unchanged;
Engagement currentness is not added to their schema. This contract creates
no report release, retrieval, or `DOWNLOAD` authority.

## 8. Fail-closed conformance examples

| Case | Required outcome |
| --- | --- |
| Exact authorized E/B with current source revision and `CURRENT_AND_ELIGIBLE` | Display only §5's approved client-safe fields after all release gates pass. |
| Exact authorized E/B with verified `NO_LONGER_CURRENT` | Display “No longer current” only if the separately approved read permission explicitly covers that non-current E; otherwise zero fields. |
| Candidate, unknown, ambiguous, conflicting, stale, or unavailable E/currentness evidence | Zero protected fields; no synthetic/default status. |
| Wrong E, wrong B, same-B substitution, invalid E -> B, or browser-supplied B | Zero protected fields; no cross-B existence disclosure. |
| Participation present but status-read entitlement absent | Zero protected fields. |
| Dashboard VIEW or Submission SUBMIT/VIEW offered as status-read authority | Zero protected fields. |
| Prior ALLOW followed by Resource, Engagement, Principal Mapping, Membership, or Entitlement revocation | Zero protected fields; prior decision cannot override current authority. |
| Missing/unsupported contract version, source revision, provenance, or audit correlation | Zero protected fields. |

These are contract-level acceptance expectations, not a new test framework or
a claim that a client-facing release implementation exists.

## 9. Production and implementation limits

This contract does not activate production Engagement-status authority, assign
a concrete production source, authorize a live Website route, create a new
Resource/action permission, or select storage, transport, endpoint, runtime,
or administrative actors. The existing synthetic Engagement source and tests
prove only local deterministic behavior. Production integration requires
separate source, resource/action, authorization, release, and audit approval
with evidence. The canonical 48-question methodology, Assessment Service
truth, EIP dashboard contracts, and report delivery remain outside scope.

**PRODUCTION AUTHORITY: NOT GRANTED.**
