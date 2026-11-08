# CEP v3 Recommendation Action EXPLAIN Eligibility Decision v1

**Status: APPROVED — LIMITED CONTENT ELIGIBILITY**

## 1. Status and decision owner

This is the bounded Platform content-eligibility decision for future
**nonproduction** Dashboard `EXPLAIN` development. The decision authority is
the Nguyen AI Enterprise LLC founder/owner. The founder approved limited
eligibility on **2026-11-08**. This approval grants no implementation permission,
publication authority, individual access, or production authority. Stage 4H.4
remains closed, client-facing v3 action text remains unreleased, and roadmap
Stage 4 remains in progress.

## 2. Decision question

> Should the exact producer-approved v3 recommendation action text, together
> with the minimum necessary recommendation identifiers and linkage fields,
> become eligible for future nonproduction Dashboard EXPLAIN delivery, subject
> to separate governed publication, currentness verification, and
> exact-resource authorization?

The founder's decision is **APPROVE LIMITED ELIGIBILITY** under the exact
conditions below. It authorizes only bounded content eligibility for subsequent
governed development, not client-facing release.

## 3. Existing authoritative evidence

- The Assessment Service
  `docs/business-decision-methodology/31-recommendation-action-text-addendum-v1.md`
  approves the exact eight rule-bound presentation statements, not downstream
  admission. Its `docs/architecture/business-decision-package-contract-v3.md`
  defines the exact five-field v3 recommendation record and version pairings.
  The contract document retains its original design-status wording; current
  producer implementation in `src/assessment/business_decision_package.py`,
  `src/assessment/governed_producer_validation.py`, and
  `src/assessment/producer_snapshot_attestation.py` implements and validates
  explicit v3 selection, text equality, finding linkage, and the v3 attestation
  profile. Methodology text remains the Assessment Service's authority.
- EIP `docs/stage4h4-local-v3-recommendation-projection-evidence-v1.md` and
  `src/executive_intelligence_platform/snapshot_derivation/local_v3_recommendation_projection.py`
  show an ordered, immutable, verified **internal** projection. It has no
  display serializer or publisher, and `release_eligible=False`. Its local
  expected-producer-release check is not publication-currentness authority.
- The [Stage 4G.1 eligibility addendum](cep-nonproduction-explain-content-eligibility-addendum-v1.md)
  previously left recommendation action text ineligible pending verified
  producer text and separate approval. This decision supplies only the limited
  content approval. The [Stage 4B EXPLAIN contract](cep-nonproduction-dashboard-explain-contract-v1.md)
  limits current admitted subjects and requires independent exact-resource
  authorization, deterministic grounding, fresh checks, and content-free
  `DENY`. The [Resource-to-Artifact Binding Authority governance](executive-dashboard-resource-artifact-binding-authority-governance-v1.md)
  separates current Resource-specific selection from EIP publication and
  freshness. The current Assistant
  `src/trusted_authentication/non_production_dashboard_explanation_adapter.py`
  selects recommendation **classifications** from existing Dashboard delivery,
  not v3 action text.

## 4. Approved limited eligibility scope

Future nonproduction Dashboard `EXPLAIN` content eligibility is limited to the
exact `recommendationActionText` in an explicitly selected
`business-decision-package-v3` recommendation, equal character for character
to the Assessment Service's approved mapping keyed by
`recommendationDecisionIdentifier`. The minimum validated record is the
producer's exact ordered tuple: `findingId`,
`recommendationClassification`, `recommendationDecisionIdentifier`,
`recommendationDecisionTableVersion`, `recommendationActionText`. Preserve
producer recommendation order and one-to-one finding linkage. `findingId` is
`null` only for the producer-defined complete no-findings recommendation;
that record uses the approved no-findings rule and `monitor` classification.

Validation also requires `versionMetadata.contractVersion` =
`business-decision-package-v3`, `versionMetadata.assessmentVersion` =
`nguyen-ai-executive-assessment-v2`, `versionMetadata.methodologyVersion` =
`business-decision-methodology-v1`, each record's
`recommendationDecisionTableVersion` =
`recommendation-decision-table-set-v1`, the supported
`executive-runtime-response-v1` snapshot envelope, and verified producer
snapshot and attestation provenance. This decision adds no wording, decision
rule, score, priority, finding description, or remediation specificity.

## 5. Client-visible versus trusted-only fields

The candidate client-facing content is the exact `recommendationActionText`.
`recommendationClassification` may accompany it only if a later approved
versioned delivery and EXPLAIN field-scope contract explicitly admits that
existing classification. `recommendationDecisionIdentifier`, `findingId`,
`recommendationDecisionTableVersion`, and source order are necessary to check
identity, mapping, linkage, and completeness; this decision does not make
their raw values client-visible. A later contract must justify any client-safe
identifier or linkage representation before display. The package, assessment,
methodology, snapshot, attestation, source identity, publication, and audit
metadata remain trusted-only verification evidence. Raw signatures, private
identity records, tokens, verification internals, and unnecessary provenance
must not enter client responses or model context.

## 6. Versioned delivery and EXPLAIN requirements

This decision applies only to the exact producer v3 package contract and
approved action-text mapping. A **separately approved**, versioned EIP
Dashboard delivery and EXPLAIN field-scope contract must define compatibility,
admitted fields, limits, grounding, response normalization, and client-safe
presentation before any implementation. No contract version is selected here.
The existing v2 Dashboard output and `VIEW` behavior remain unchanged. The
six current EXPLAIN subjects do not automatically extend to v3 action text;
EXPLAIN v1 receives no additional field by this decision. Unsupported field
versions fail closed, with no v3-to-v2 downgrade. No REPORT or production
eligibility follows.

## 7. Authorization and currentness requirements

`EXECUTIVE_DASHBOARD × EXPLAIN` remains independently applicable; `VIEW` does
not grant `EXPLAIN`. Existing `EXPLAIN` does not automatically grant access to
new v3 fields. A subsequent explicit field-scope authorization decision is
required where current governance does not establish that coverage. Producer
wording approval, EIP verification, and caller-supplied eligibility assertions
grant no Principal access or publication authority.

Any future release must verify current Principal Mapping; exact Resource,
Engagement, and Business Entity binding and isolation; current Membership and
exact-resource `EXPLAIN` Entitlement; revocation; fresh Trusted Authorization
`ALLOW` before protected admission and again before release; and required
authorization and source audit/custody evidence. It must verify the exact
approved content and field versions, producer authenticity and signed package
evidence, EIP governed publication eligibility, Resource-specific current
artifact selection, publication revision and currentness, authorization
currentness, and absence of intervening revocation or supersession. EIP's
local expected-release verification alone cannot prove these publication
conditions. The current internal projection retains `release_eligible=False`
until a separately approved and implemented release boundary establishes
eligibility. This decision is not an executable release flag. Failure yields
content-free `{"decision":"DENY"}`; the Stage 4B
authorized refusal remains distinct from DENY.

## 8. Explicit exclusions

No legacy v2 field expansion; Dashboard `VIEW` change; automatic EXPLAIN
subject expansion; EXPLAIN v1 response-field addition; REPORT release;
production route; Website or CEP activation; EIP publisher; new authority
source; caller-controlled field eligibility; raw assessment input; inferred
finding description; generated recommendation; internal-only source reference;
or display of signatures, private identity data, tokens, and audit internals
is authorized.

## 9. Required negative-case verification

Future focused tests must reject missing required downstream approval; denied
or deferred eligibility; forged eligibility flags or authority assertions; wrong package,
assessment, methodology, decision-table, attestation, or field version;
altered `recommendationActionText`; changed recommendation order; missing,
extra, or duplicate records; changed `findingId` linkage; invalid no-findings
count, null link, rule, or classification; wrong Resource, Engagement, or
Business Entity; `VIEW`-only access; missing or revoked `EXPLAIN` access;
stale source, binding, or publication evidence; unsupported field versions;
unapproved fields in legacy v2 output; and any protected content in DENY or
error responses. Tests must also cover fresh admission and release decisions,
current revision selection, and existing v2 regressions. These are future
implementation requirements, not tests created by this decision.

## 10. Founder decision

**Decision authority:** Nguyen AI Enterprise LLC founder/owner.

**Decision date:** 2026-11-08.

**Decision: APPROVE LIMITED ELIGIBILITY.** The founder approves exactly the
conditional future nonproduction content scope in sections 4–9. Separate
versioned contract approval, implementation authorization, EIP publication
decision, and individual access checks remain required. No release begins with
this decision alone.

## 11. Decision effectiveness conditions

- **A. Content eligibility approval:** APPROVED for the narrowly defined future
  nonproduction development scope in sections 4–9.
- **B. Versioned Dashboard delivery contract:** NOT YET APPROVED OR IMPLEMENTED.
- **C. Versioned `EXPLAIN` field admission:** NOT YET APPROVED OR IMPLEMENTED.
- **D. Individual client authorization:** NOT GRANTED. Fresh exact-resource and
  approved field-scope checks remain required.
- **E. EIP publication/release authority:** NOT GRANTED. EIP publication
  eligibility, authoritative current Resource-to-Artifact selection, explicit
  release evidence, and release validation remain required.
- **F. Client-facing display:** NOT ACTIVATED.
- **G. Production release:** NOT AUTHORIZED.

Each condition is separate; content eligibility does not imply any other
condition. Until all applicable gates are established, action text remains
ineligible for client release.

## 12. Downstream implementation sequence

Following this recorded limited eligibility decision, propose
three separately authorized bounded increments, each with focused tests,
negative-case verification, and regression coverage:

1. EIP versioned governed delivery and release-evidence contract, preserving
   producer truth and `release_eligible=False` in the current internal proof.
2. Trusted Authorization `EXPLAIN` field admission and deterministic rendering
   under fresh exact-resource authorization and current-source checks.
3. CEP admission and response normalization, then Website presentation of
   only the approved client-safe fields.

This decision implements none of those increments and grants no deployment.
