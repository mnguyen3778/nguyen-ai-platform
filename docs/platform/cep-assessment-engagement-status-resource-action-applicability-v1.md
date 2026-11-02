# CEP Assessment Engagement Status Resource/Action Applicability v1

Version: v1 (bounded additive applicability decision)

Status: nonproduction governance contract for future synthetic verification.
Production authority: **NOT GRANTED**.

## 1. Purpose and version boundary

This decision closes the one applicability gap identified by [CEP Assessment
Engagement Status Read Contract v1](cep-assessment-engagement-status-read-contract-v1.md).
It governs the semantic validity of viewing **Assessment Engagement context
currentness** for one exact status-read Resource. It does not grant a Principal
permission, produce a Trusted Authorization `ALLOW`, or release status fields.

The [Resource × Action Applicability Governance v1](resource-action-applicability-governance-v1.md)
matrix and the three-class v1 taxonomy remain historically unchanged. Its
§§21, 39, 60–62 allow future candidate classes only through explicit version
governance. This document is a scope-specific, versioned **successor extension**
for the pair below, suitable only for separately authorized nonproduction
proofs. It is not an amendment to, or silent runtime reinterpretation of,
the original v1 matrix. A consumer must know which governed applicability
version it is evaluating; a v1-only consumer treats the new class as unknown
and denies. No production applicability activation follows from this document.

## 2. Governing boundaries

[Assessment Submission Business Context Governance v1](trusted-authorization-assessment-submission-business-context-governance-v1.md)
§§3, 6–18, 20–25, 28–29 governs exact E, immutable E -> B, independent
Business Entity currentness, and the separation of context from permission.
[Assessment Engagement Context Legitimacy Governance v1](trusted-authorization-assessment-engagement-context-legitimacy-governance-v1.md)
§§3–5, 8–13, 34–36, 43–47, 53–56, 62–65 preserves Participation and
exact-E context as distinct facts and leaves production source ownership open.
[Resource Identity Authority Source Governance v1](resource-identity-authority-source-governance-v1.md)
§§8–10, 14–15, 31–36 requires authoritative, unique, current Resource identity
with Business Entity isolation; a class label or identifier string cannot
establish it. [Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md)
§§3–8, 11–13 supplies the inherited trusted-release, audit, and denial-privacy
principles; its EIP artifact scope is not expanded here.

## 3. Exact Resource and Action decision

The narrow governed Resource class identifier is
`ASSESSMENT_ENGAGEMENT_STATUS`. It denotes the **status-read capability for
one particular governed Assessment Engagement E**, not the general Engagement
domain object, Assessment Submission, assessment result, report, Executive
Dashboard, EIP artifact, Website route, or UI component. A particular status
Resource R must be authoritatively resolved and bound to exactly one E and its
immutable authoritative Business Entity B. R, E, and B remain distinguishable
identities; no string construction from E creates Resource authority.

The canonical Requested Action is `VIEW`. `READ` is not in the approved
`VIEW`, `DOWNLOAD`, `SUBMIT`, `EXPLAIN` vocabulary and is not introduced.

| Applicability governance | Governed Resource class | Requested Action | Decision |
| --- | --- | --- | --- |
| CEP status-read extension v1 | `ASSESSMENT_ENGAGEMENT_STATUS` | `VIEW` | **APPLICABLE** |

Only this exact pair is decided. `DOWNLOAD`, `SUBMIT`, and `EXPLAIN` for this
new class remain **UNRESOLVED** under this extension and therefore cannot
produce authorization `ALLOW`. Existing pairs retain every value in the
original v1 matrix, including `ASSESSMENT_SUBMISSION × VIEW = NOT APPLICABLE`.
`EXECUTIVE_DASHBOARD × VIEW` and `REPORT × VIEW` do not cover this Resource.
No action implies another action.

**APPLICABLE** means only that `VIEW` is semantically meaningful for this
status-read class. A specific Principal's permission still requires an
independent, current Trusted Authorization decision for exact R and `VIEW`,
including a separately governed Entitlement. An `ALLOW` is not created by
classification, applicability, Participation, or possession of E. Actual
release is a further trusted boundary that validates the Phase 2B contract.

## 4. Exact Resource, Engagement, and Business Entity evidence

For future authorized nonproduction evaluation, trusted server-side evidence
must establish a stable, unambiguous R classified in this extension as
`ASSESSMENT_ENGAGEMENT_STATUS`, the exact governed E it represents, and E's
immutable E -> B binding to one current authoritative B. The Resource identity
and class association require their own authority provenance, applicable
governance version, lifecycle/currentness, and deterministic validation.
Engagement establishment provenance, source revision, currentness evidence,
and relevant revocation must agree with R/E/B at the same release decision.
Unknown, duplicate, conflicting, stale, unavailable, or cross-B facts deny.

A browser may supply a candidate Engagement or Resource reference for lookup.
It cannot establish R, E, B, their association, classification, currentness,
Entitlement, or permission. The trusted resolver must reject same-B E
substitution as well as cross-B substitution. Participation(P,E), even when
current, establishes only engagement-context standing; it never grants
status `VIEW`. The existing `E_CONTEXT_LEGITIMATE(P,A,E)` and Binding(A,E)
are scoped to an Assessment Submission attempt and current E. They cannot be
reused as status-read permission or as proof that a non-current E is viewable.

## 5. Future Trusted Authorization evaluation

The future evaluation must require server-verified subject evidence and
current Principal Mapping; exact current R identity and its authoritative
status-read classification under this extension; canonical `VIEW` and this
pair's `APPLICABLE` state; exact E and authoritative B binding; current B;
applicable Membership and a separately established, current Entitlement for
R/`VIEW`; independently governed exact-E status-read context legitimacy
without treating Participation or a submission attempt as permission; current
Resource and authorization authority state plus verified current evidence of
the Engagement's lifecycle (including a verified non-current outcome where
that read is separately permitted); revocation precedence; compatible
governance/version evidence; and
complete source and decision audit references. The existing deterministic
Trusted Authorization owner retains decision composition. This document
creates no evaluator or authority source.

Missing, invalid, ambiguous, conflicting, revoked, stale, unsupported, or
unavailable required evidence yields `DENY`. The exact authorization semantics
and reason handling remain with the existing evaluator governance. A
synthetic proof cannot claim a live Principal, Entitlement, or production
Resource merely because all fixture predicates are true.

## 6. Trusted release and display boundary

Before any protected status fields leave the trusted server-side boundary,
require all of the following together: this exact applicable R/`VIEW` pair;
a fresh independent `ALLOW` for the same R/`VIEW`; current R identity,
exact E/B association and independently verified B currentness; source
provenance; supported Phase 2B
`contractVersion`; coherent `sourceRevision` and
`engagementContextCurrentness` evidence; applicable audit evidence; and a
recheck of current authorization, Engagement, and revocation facts immediately
before release. The precise status-read context legitimacy rule, including
whether a verified non-current E may be viewed, requires a separate bounded
authorization decision before release. A prior `ALLOW`, old source revision, valid Participation,
or cached currentness cannot substitute for a required current fact.

On `DENY` or any invalid, stale, contradictory, revoked, unavailable, or
unsupported evidence, release **zero protected status fields**, with no
partial, default, synthetic, cross-B, prior-client, or prior-status fallback.
Caller-visible failure must not disclose another B's E or status. Only the
display-safe fields authorized by Phase 2B §5 may reach the Website; source,
Principal, Membership, Entitlement, and audit details remain server-side.

## 7. Status and producer boundaries

The sole display meanings remain Phase 2B's `CURRENT_AND_ELIGIBLE` and
`NO_LONGER_CURRENT`, both explicitly about Engagement context currentness.
No `IN_PROGRESS`, `SUBMITTED`, `COMPLETED`, `PERCENT_COMPLETE`, assessment
workflow transition, methodology-derived progress, or report readiness is
introduced. The Assessment Service's canonical 48-question methodology and
business truth are unchanged. EIP's Executive Dashboard projection and
Website Projection Delivery Contract are unchanged. This decision creates
no report retrieval or delivery authority.

## 8. Nonproduction proof and production exclusions

This versioned decision can be used only in a separately authorized local
synthetic/nonproduction proof that explicitly selects this extension and
supplies exact synthetic R/E/B, classification, authority, entitlement, and
currentness evidence. It does not itself authorize even that code change.
Unknown versions or consumers limited to the original v1 matrix must deny.

No concrete production Assessment Engagement, Resource Identity, Resource
Classification, Business Entity, Principal Mapping, Membership, or Entitlement
source is selected. No production Resource/action activation, permission
grant, trusted delivery endpoint, Website route, Cognito/AWS integration,
infrastructure, persistence, deployment, or administrative mutation is
authorized. Production integration remains separately gated.

**PRODUCTION AUTHORITY: NOT GRANTED.**

## 9. Focused acceptance conditions

| Case | Required outcome |
| --- | --- |
| Exact R classified under this extension with `VIEW` | `APPLICABLE` only; no automatic `ALLOW` or release. |
| Original v1-only applicability context sees this class | Unknown class; `DENY`. |
| `ASSESSMENT_SUBMISSION × VIEW`, dashboard `VIEW`, or report `VIEW` offered for status read | No status-read permission; original matrix stays unchanged. |
| New class with `DOWNLOAD`, `SUBMIT`, or `EXPLAIN` | `UNRESOLVED`; `DENY`. |
| Participation(P,E) without separate R/`VIEW` Entitlement | `DENY`; zero protected fields. |
| Wrong R/E/B, same-B E substitution, cross-B association, or browser-derived authority | `DENY`; zero protected fields without cross-B disclosure. |
| Missing or invalid source provenance, classification, version, revision, currentness, or audit evidence | `DENY`; zero protected fields. |
| Prior `ALLOW` followed by revocation or source change | Recheck current facts; `DENY` and zero protected fields if no longer valid. |
| Valid exact R/`VIEW` authorization plus all Phase 2B release evidence | Only Phase 2B display-safe fields may be released by a separately authorized future delivery implementation. |

These are contract-level conformance expectations, not tests of a deployed
service or an assertion that synthetic records are production authority.
