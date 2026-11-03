# CEP Assessment Progress Meaning and Client-Facing Read Contract v1

Version: `cep-assessment-progress-read-contract-v1`

Status: bounded nonproduction contract decision. No progress delivery, source,
permission, or production authority is activated.

## 1. Decision scope and governing evidence

This contract addresses only the meaning and future client-facing read boundary
for Assessment Progress associated with one exact Assessment Engagement E. The
Assessment Service owns assessment truth and the canonical 48-question
methodology. Its Executive Assessment Input Contract v1
(`nguyen-ai-assessment-service/docs/architecture/executive-assessment-input-contract-v1.md`)
distinguishes complete executive evaluation, which requires every configured
canonical answer, from draft or partial submissions, whose semantics remain
undecided. The current complete-input rule is not a progress rule. This
document does not change that rule or assume that all 48 questions apply to
every Engagement.

The [CEP Assessment Engagement Status Read Contract v1](cep-assessment-engagement-status-read-contract-v1.md)
governs Engagement context currentness, not assessment progress. The
[Assessment Submission Resource Lifecycle Governance v1](trusted-authorization-assessment-submission-resource-lifecycle-governance-v1.md)
governs Submission Resource states, not assessment progress. The
[Resource/Action Applicability Governance v1](resource-action-applicability-governance-v1.md)
and [CEP Engagement Status Applicability v1](cep-assessment-engagement-status-resource-action-applicability-v1.md)
do not decide a progress read.

## 2. Business meaning and v1 limit

Assessment Progress would be an Assessment Service-authored, versioned
indication of the position of assessment work for one exact E under a separately
approved assessment workflow or deterministic measure. It is distinct from:

- Engagement context currentness or Business Entity eligibility;
- assessment readiness classification or score;
- Assessment Submission Resource lifecycle;
- Executive Dashboard availability;
- Finding or Recommendation generation.

None of those facts is a substitute, proxy, starting point, or completion proof
for Assessment Progress. This v1 contract approves **no client-facing progress
state or metric**. Current evidence does not support calling an assessment
`not started`, `in progress`, `partially completed`, `submitted`, `completed`,
or `awaiting review` for progress purposes. No assessment-specific value may
be inferred from a completed evaluation, a Submission Resource state, an
Engagement status, or a dashboard projection.

The v1 outcome is **capability unavailable**. It means this portal has no
governed Assessment Progress read to offer. It is not an Assessment Service
finding about E, a protected progress field, or evidence that E or an
assessment exists. A generic notice may say only: **“Assessment progress is
unavailable.”** The same neutral wording must not reveal an E, B, Principal,
source condition, authorization result, or whether work has begun. No
Engagement-specific progress response is authorized by this contract.

## 3. Question-level progress and calculations

Question-level progress is **deferred**. `ANSWERED`, `REQUIRED`,
`CONDITIONALLY_REQUIRED`, and `NOT_APPLICABLE` are investigation candidates,
not approved classifications or implemented business truth under this
contract. A future decision must establish Engagement-specific applicability,
deterministic rules and governing business context, exact question-to-E
binding, authoritative answer evidence, methodology and applicability
versions, source revision and currentness, and testable edge cases before any
question-level display.

No questions-answered or questions-remaining count, percentage complete,
completion rate, progress bar, or step count is approved. A future calculation
contract would also have to define its denominator, numerator, treatment of
conditional and not-applicable questions, missing or changed answers, version
changes, zero-denominator behavior, and invalid or conflicting evidence. The
canonical count of 48 must never be used as an Engagement-specific denominator
by default. This document defines no calculation.

## 4. Producer, Resource, and action boundary

The Assessment Service is the sole future producer of Assessment Progress
truth. The Client Engagement Portal is a read-only consumer. The Website must
not calculate, classify, or infer progress. EIP must not redefine it. The AI
Knowledge Assistant must not generate or override progress states. No second
business-truth authority is created.

The conceptual future Resource class is `ASSESSMENT_PROGRESS`, scoped to one
exact E and E's authoritative, immutable Business Entity B. A particular
Resource identity R must be server-resolved from source-backed authority and
bound to that exact E/B; an identifier assembled from E, a browser selector,
or a browser-supplied B is not authority. Neither the Resource class nor a
concrete Resource is implemented or approved for authorization here.

`VIEW` is the proposed canonical read-only Requested Action. The pair
`ASSESSMENT_PROGRESS × VIEW` is **proposed for a separate future applicability
decision**. It is not an entry in the current matrix or Phase 2C extension;
it confers no Entitlement, Trusted Authorization `ALLOW`, or release right.
`EXECUTIVE_DASHBOARD × VIEW`, `ASSESSMENT_ENGAGEMENT_STATUS × VIEW`, and
Assessment Submission participation or `SUBMIT` do not authorize this read.
No `READ` action or other action is introduced.

## 5. Minimum future source and read evidence

Before a meaningful protected read can be considered, an Assessment
Service-owned interface must supply a supported progress meaning for exact E,
and must be checked against a separately authoritative E-to-B binding. It must
carry Assessment Service source authority, supported contract and methodology
versions, source revision and provenance, and independently verifiable
currentness. If question-level meaning is
adopted, it must also supply governed applicability version and exact-E
applicability and answer evidence. If lifecycle meaning is explicitly adopted
in a later contract, it must supply governed lifecycle evidence. None of
these records, interfaces, or persistence capabilities is asserted to exist.

Authorization currentness, E/B currentness, progress-source currentness, and
methodology/applicability version compatibility are separate predicates.
Evidence valid at one time or in one domain does not establish the others.
Unknown, unsupported, stale, ambiguous, conflicting, unavailable, or revoked
required evidence fails closed. A previously authorized snapshot or cached
source result cannot establish current progress or release rights.

## 6. Client-facing and confidentiality boundary

The v1 display-safe boundary has three distinct cases:

| Case | Permissible client-facing effect |
| --- | --- |
| Authorized Assessment Progress | None in v1: no progress meaning or protected progress fields are approved. A later version must define its exact display-safe fields. |
| Capability unavailable or unsupported | The generic notice in §2 only; no E-specific value or explanation. This is not a progress state or authorization `DENY`. |
| Authorization `DENY` or invalid required evidence | Zero protected progress fields; no partial, cached, default, or synthetic fallback and no cross-B existence disclosure. |

A generic unavailable notice may be rendered without an E-specific lookup.
Any future protected read must first verify the Principal and current Principal
Mapping; resolve exact R/E/B; verify applicable Resource/action and exact-R
Entitlement, required Membership, source and authority currentness, revocation,
version compatibility, and audit/custody evidence; obtain a fresh Trusted
Authorization `ALLOW` for exact R/`VIEW`; and recheck required current facts
immediately before release. Failure is `DENY` with zero protected fields.
Authorization denial must not be relabeled as source unavailability to reveal
whether another B's E or assessment exists. The public result may use neutral
wording where needed to preserve denial privacy, while trusted handling keeps
denial and capability unavailability distinct.

No future display-safe payload may expose Principal Mapping, Membership or
Entitlement evidence, Business Entity identity, source-provenance internals,
source revisions, raw answers, raw question-applicability records, audit or
custody internals, or authorization decision hashes. This v1 document creates
no progress response schema or release endpoint.

## 7. Dependencies and compatibility

Real progress delivery remains gated by, in order: an approved meaningful
progress state or deterministic measure; an Assessment Service authoritative
source interface; Engagement-specific applicability and answer evidence if
question measures are chosen; a separate progress Resource/action applicability
decision; exact-Resource Entitlement support; a trusted governed delivery
adapter; a Website display-safe consumer; and deterministic boundary tests.
These are future dependencies, not implementation authorization.

Existing methodology and complete-input scoring, Submission Resource
lifecycle, Phase 2B Engagement Status, Phase 2C applicability, Phase 2D.1
Trusted Authorization, Phase 2D.2 status delivery, Phase 2E Website status
presentation, Executive Dashboard, Findings, and Recommendations retain their
approved meanings and boundaries. The existing Website Overview may later
present an authorized display-safe result without redesign, but no Website
change is authorized here. No production source, persistence integration,
permission grant, runtime behavior, deployment, or production authority is
created.

## 8. Contract disposition

**DECISION B — PROGRESS DEFERRED.** No meaningful client-facing Assessment
Progress state is currently supported by authoritative source evidence. V1
permits only the generic capability-unavailable notice in §2 and defines the
future protected read boundary above. The notice must never be interpreted as
Assessment Progress truth.
