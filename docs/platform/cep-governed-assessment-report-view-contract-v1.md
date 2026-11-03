# CEP Governed Assessment Report VIEW Contract v1

Version: `cep-governed-assessment-report-view-contract-v1`

Status: bounded nonproduction contract decision. Report production, delivery,
permission, persistence, and production authority are not activated.

## 1. Decision and governing boundaries

The initial CEP Assessment Report is a **distinct, read-only governed executive
report projection** to be produced by the Executive Intelligence Platform
(EIP) from eligible, immutable EIP package and projection inputs. It is a
client-facing representation of approved Assessment Service conclusions and
governed executive intelligence. It has its own future identity, content
contract, lineage, revision, and release-eligibility decision. It is not the
existing Executive Dashboard or a renamed dashboard projection; an Assessment
Service scoring result; a raw `BusinessDecisionPackage` or
`ExecutiveAssessmentSnapshot`; a persisted PDF or document; a Website-generated
report; or an AI-generated conclusion. No report projection is asserted to
exist today.

The Assessment Service's `business-decision-package-v2` governed conclusions
are the source for the candidate report content below. Its v1 foundation
confidence, recommendation priority, and summary fields do not become final
governed conclusions by presentation. EIP's existing
`executive-intelligence-projection-v1` and
`website-projection-delivery-contract-v1` establish lineage-preserving
representation and dashboard delivery boundaries. Neither is a report
contract. The [Resource/Action Applicability Governance v1](resource-action-applicability-governance-v1.md)
already classifies `REPORT × VIEW` as `APPLICABLE`. The
[Protected Application Operation Catalog v1](trusted-authorization-protected-application-operation-catalog-governance-v1.md)
still defers the real report-view operation. This document does not amend
either decision.

## 2. Producer and consumer authority

The Assessment Service alone owns methodology, deterministic scoring, business
conclusions, and source assessment versions. EIP is the **proposed future
producer** of the governed report projection: it may select and arrange
approved immutable source content into the report sections defined here,
preserve lineage, validate the report contract, and establish report-projection
release eligibility. It must not recalculate, reinterpret, or modify
Assessment Service truth. EIP reporting is not yet implemented.

Trusted Authorization decides access to one exact Report Resource; it does
not make report content or EIP publication decisions. The Website consumes
only an already authorized, display-safe report result and renders it without
reconstructing conclusions or authorizing access. The AI Knowledge Assistant
may in a separately governed future capability explain separately authorized
content; it cannot create, score, approve, or override report truth.

## 3. Exact Report Resource and binding

One future report projection maps to one exact canonical `REPORT` Resource R,
distinct from any `EXECUTIVE_DASHBOARD` Resource. R must be resolved by a
trusted server-side, source-backed Resource Identity authority; a string,
route, browser reference, EIP projection reference, or Entitlement alone cannot
establish R. The required chain is:

```text
exact Report R -> exact Assessment Engagement E -> authoritative Business Entity B
```

The R-to-E association and E-to-B binding must each have independent trusted
authority evidence, unique identity, provenance, revision/currentness, and
consistent scope at release. Report identity, E, B, report projection contract
version, report revision, source assessment identity/version, and EIP
projection provenance remain distinguishable. A report revision is not an
Assessment Service source revision. Browser-supplied B or a synthetic sample
identifier is never production authority. Missing, duplicate, conflicting,
stale, cross-B, or browser-derived association fails closed; same-B E
substitution also fails.

No concrete Report Resource, binding record, persistence model, or production
identity source is created by this contract.

## 4. Minimal v1 report content boundary

The future report projection may carry only the following section meanings,
under a separately implemented exact report allowlist. Every displayed value
must be copied or deterministically represented from the approved governed
source meaning, with source artifact and field lineage retained server-side.
An EIP report projection may order, group, and label approved material; it may
not derive a new assessment decision or narrative. The Website receives only
the report-specific display-safe representation, never a raw package,
snapshot, general projection, or dashboard delivery payload.

| Section | Approved meaning and source | Display-safe limit | Missing or invalid evidence |
| --- | --- | --- | --- |
| Executive Summary | Assessment Service v2 `governedConclusions.executiveSummary` deterministic approved template text, through eligible EIP lineage. | Approved section text in source order; no new narrative or conclusion. | Required summary or lineage missing: report ineligible; no partial summary. |
| Risk and Confidence Context | Assessment Service v2 `governedConclusions.assessmentRisk` and `.confidence`. | Approved classifications and separately approved interpretation/limitation text only; no raw evidence or internal decision trace. | Either conclusion missing, unsupported, or contradictory: report ineligible. |
| Governed Findings | Assessment Service v2 `governedConclusions.severityAssignedFindings`. | Approved client-safe finding title, type, and severity in canonical order. Empty governed findings may be shown as empty; EIP must not invent significance ranking. | Missing, conflicting, or untraceable finding: report ineligible. |
| Recommendations | Assessment Service v2 `governedConclusions.recommendations`. | Approved recommendation classification and client-safe reference to its governed finding, preserving source order; no invented priority or action text. | Missing, conflicting, or untraceable recommendation: report ineligible. |
| Limitations and Interpretation Guidance | Approved producer limitations and EIP report-projection limitations. | Only a separately allowlisted client-safe limitation or approved interpretation; required limitations remain visible. | Missing required limitation or unsupported wording: report ineligible. |

The candidate **Assessment Classification** section is deferred: this contract
does not promote a foundation readiness value into a final client-facing
classification. **Priority Recommendations** are also deferred as a distinct
claim because the v2 package does not assert final recommendation priority.
The recommendations section above carries only governed recommendation
meaning. No dashboard field becomes report-safe solely by being dashboard-safe.
No source absence may be repaired by default values, AI text, or another
assessment's content.

The client-facing v1 report excludes raw answers and question catalog records;
internal scoring intermediates; `BusinessDecisionPackage` internals; raw
`ExecutiveAssessmentSnapshot`; unapproved source evidence; decision traces;
Principal Mapping, Membership, Entitlement, or audit/custody records; source
credentials; cross-tenant references; and unapproved AI conclusions. Source
identities, revisions, internal lineage, and authorization decision hashes
remain server-side unless a later report-specific display contract explicitly
approves a narrower public reference.

## 5. Version, lineage, and currentness

Future trusted source evidence must identify the supported report contract
version, exact R/E/B binding, report revision, source assessment identity,
Assessment Service package and methodology versions, originating snapshot
identity and source revision/currentness, EIP package and projection versions,
EIP report-projection provenance and currentness, and applicable release
eligibility evidence. Every section must trace to approved source fields
through the EIP package/projection lineage. These are required future facts,
not assertions that report records or revisions currently exist.

Authorization currentness, Report Resource currentness, E/B currentness,
Assessment Service source currentness, EIP report-projection currentness, and
contract/version compatibility are independently checked. A previously valid
dashboard snapshot or prior `ALLOW` does not establish current report evidence.
Unknown, missing, stale, revoked, conflicting, incompatible, or unsupported
required evidence makes the report ineligible and blocks protected release.

## 6. VIEW release eligibility and authorization

EIP's future report-projection eligibility decision must establish, together:
a supported distinct report projection exists; exact report identity and R/E/B
binding are verified; source and projection versions and lineage are
compatible; source and report evidence are current; every released section
conforms to §4; and no authoritative revocation or invalidation blocks
release. If explicit report publication state is needed, its source and
semantics must be separately established before implementation. This contract
does not adopt `DRAFT`, `APPROVED`, `RELEASED`, `SUPERSEDED`, `ARCHIVED`, or any
other report lifecycle state. EIP eligibility is separate from Principal
permission.

`REPORT × VIEW = APPLICABLE` remains the existing canonical applicability
classification. It does not grant exact-R Entitlement, Membership, Trusted
Authorization `ALLOW`, report release, `DOWNLOAD`, or cross-B access.
Executive Dashboard `VIEW`, Engagement Status `VIEW`, and Assessment
Submission permissions cannot substitute for Report `VIEW`.

Before protected release, a trusted boundary must verify the Principal and
current Principal Mapping; exact R/`VIEW` applicability, Resource Identity,
current exact-R Entitlement and required Membership; exact E/B binding and
tenant isolation; source and Report Resource currentness; revocation;
report-projection eligibility; and audit/custody evidence. It must obtain a
fresh evaluator-owned `ALLOW` for exact R/`VIEW` and recheck required current
facts immediately before delivery. Existing Trusted Authorization governance
and evaluator ownership remain intact. No parallel evaluator is authorized.

On `DENY`, missing source, stale source, unsupported version, or report
ineligibility, release **zero protected report fields**. Trusted handling must
distinguish these causes, while caller-visible failure remains neutral and
does not disclose report existence or identity, E, B, sections, source
revisions, or authorization internals. No cached, partial, synthetic, or
cross-tenant fallback is permitted.

## 7. Audit, Website, and excluded capabilities

Future server-side audit/custody evidence must correlate exact Report Resource,
Principal decision, E/B binding verification, source versions and currentness,
report revision, EIP release-eligibility decision, final delivery decision,
and revocation/currentness failures. Evidence must preserve complete lineage
without logging raw protected report content, credentials, or authority
records. No audit persistence technology is selected; audit internals never
enter Website props.

The existing nonproduction Client Workspace Overview is the initial future
entry point. A dedicated Reports route requires a later content or interaction
need; visual convenience alone is insufficient. The Website must consume an
already authorized report-specific display-safe result. It must not generate
report content, calculate conclusions, infer release eligibility, or perform
independent authorization. No Website modification is authorized here.

This v1 read contract covers only `REPORT × VIEW`. Existing governance also
marks `REPORT × DOWNLOAD` applicable, but this document does not implement or
authorize download, PDF generation, file export, email or external sharing,
editing, regeneration, persistence, or public report URLs. Browser rendering
of a future VIEW result confers none of those capabilities.

## 8. Nonproduction target, dependencies, and compatibility

The smallest future sequence is: (1) implement the EIP report projection and
its deterministic source/section validation; (2) establish source-backed
exact Report Resource and R/E/B binding; (3) establish a report-view protected
operation and exact-resource authorization integration; (4) implement trusted
VIEW delivery with fresh checks and audit; (5) add the Website display-safe
consumer; and (6) verify deterministic and adversarial cases. Each requires
its own approval. Synthetic evidence may support bounded nonproduction tests
but is never live client authority.

The Assessment Service methodology, scoring, `business-decision-package-v2`,
and `ExecutiveAssessmentSnapshot`; EIP executive projections and
`website-projection-delivery-contract-v1`; Executive Dashboard, Findings,
Recommendations, and Engagement Status; Phase 3B Progress Deferred; existing
`REPORT` applicability; Trusted Authorization; and current nonproduction
Website routes retain their approved behavior. No production report source,
Resource identity, authorization integration, release, persistence,
deployment, or readiness is established.

## 9. Contract disposition

**DECISION A — REPORT VIEW CONTRACT APPROVED.** This v1 decision defines a
source-compatible, client-safe future EIP report projection and exact Report
`VIEW` boundary. The report projection and its release path remain
unimplemented; this decision grants no Principal access or production
authority.
