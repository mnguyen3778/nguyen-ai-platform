# CEP v3 Recommendation Action EXPLAIN Delivery Contract Proposal v1

**Status: APPROVED — SPECIFICATION ONLY**

## 1. Status and authority

This is the approved documentation-only specification for a future
nonproduction Dashboard `EXPLAIN` content-delivery boundary. It is subordinate
to the founder's
[Stage 4H.5A limited eligibility decision](cep-v3-recommendation-action-explain-eligibility-decision-v1.md)
of 2026-11-08. Stage 4H.5A approves content eligibility; the founder's
2026-11-08 decision recorded below approves this exact contract specification.
Neither decision authorizes implementation, publication, principal access,
display, or deployment. The Nguyen AI Enterprise LLC founder/owner is the
decision authority; this specification creates no standing approval role.

| Separate authority | Current state |
| --- | --- |
| A. Assessment Service wording approval | APPROVED for eight exact rule-bound statements. |
| B. Limited content eligibility | APPROVED for future nonproduction development by Stage 4H.5A. |
| C. EIP publication eligibility | NOT GRANTED for v3 action text. |
| D. Versioned delivery admission | SPECIFICATION APPROVED; NOT IMPLEMENTED OR ACTIVATED. |
| E. Exact-resource `EXPLAIN` authorization for new v3 fields | NOT GRANTED. |
| F. Client-facing publication | NOT ACTIVATED. |
| G. Production release | NOT AUTHORIZED. |

## 2. Purpose and bounded scope

The specified future boundary would carry only exact producer-approved
`recommendationActionText` from an explicitly selected, signed, verified
`business-decision-package-v3` snapshot through EIP governed delivery to a
trusted, freshly authorized `EXECUTIVE_DASHBOARD × EXPLAIN` response. Every
recommendation and its producer order must remain intact. The Assessment
Service owns assessment truth and text; EIP owns verified admission, projection,
delivery and publication; Trusted Authorization owns principal decisions; the
Assistant renders admitted facts deterministically; the Website presents an
approved response. None may derive new assessment meaning.

## 3. Authoritative dependencies

- [Stage 4H.5A decision](cep-v3-recommendation-action-explain-eligibility-decision-v1.md)
  limits eligible content and preserves `release_eligible=False` in the current
  internal EIP proof.
- [Stage 4B EXPLAIN contract](cep-nonproduction-dashboard-explain-contract-v1.md)
  governs exact-resource authorization, bounded questions, deterministic
  grounding, response limits, fresh release checks, and content-free `DENY`.
  The [Stage 4G.1 content addendum](cep-nonproduction-explain-content-eligibility-addendum-v1.md)
  describes prior v2 field exposure; Stage 4H.5A supplies only the later
  limited v3 content decision.
- [Resource-to-Artifact Binding Authority governance](executive-dashboard-resource-artifact-binding-authority-governance-v1.md)
  separates authoritative current Resource-specific selection from EIP
  publication, eligibility, and freshness. Its production source is unresolved.
- Assessment Service [v3 package contract](../../../nguyen-ai-assessment-service/docs/architecture/business-decision-package-contract-v3.md)
  defines the exact producer record and version pairing. The
  [action-text addendum](../../../nguyen-ai-assessment-service/docs/business-decision-methodology/31-recommendation-action-text-addendum-v1.md)
  owns the eight exact statements. The v3 contract's original design-status
  wording does not itself approve downstream display; the
  [Stage 4H.4 evidence](../../../executive-intelligence-platform/docs/stage4h4-local-v3-recommendation-projection-evidence-v1.md)
  records later local producer verification.
- EIP's [internal v3 projection](../../../executive-intelligence-platform/src/executive_intelligence_platform/snapshot_derivation/local_v3_recommendation_projection.py)
  retains ordered records, producer snapshot identity, and verification evidence
  with `release_eligible=False`. Its [existing Website delivery publisher](../../../executive-intelligence-platform/src/executive_intelligence_platform/projection_delivery/delivery.py)
  supports `website-projection-delivery-contract-v1` and maps governed v2
  recommendation classifications, not v3 action text.
- The [current trusted adapter](../../../../aws-ai-knowledge-assistant/src/trusted_authentication/non_production_dashboard_explanation_adapter.py)
  renders classifications under
  `cep-nonproduction-dashboard-explain-contract-v1`; the
  [Website normalizer](../../../nguyen-ai-website/src/lib/dashboard-explanation-delivery.ts)
  accepts that version's exact response shape and empty `sourceReferences`.
  Neither admits a v3 action-text response today.

## 4. Approved versioned delivery model

**Approved design: a separately versioned Dashboard recommendation-action EXPLAIN
delivery**, derived by EIP from the verified v3 projection. Provisional future
contract identifiers are
`website-recommendation-action-explain-delivery-contract-v1` for EIP delivery
and `cep-nonproduction-dashboard-recommendation-action-explain-contract-v1` for
the trusted response. These are specification discriminators, not supported
runtime versions or an approval of a concrete publisher. An EIP delivery instance must
state its own exact version, approved field scope, required limitations,
classification, complete version context and lineage, and trusted publication
evidence. The trusted boundary must select the exact supported pair before
admission; the Website must accept only a separately approved response version.

This is narrower than extending the existing v2 Dashboard publisher or its
`VIEW` contract, which currently admits only its own version and v2 governed
content. A separate v3 recommendation-action projection is a valid EIP source
preparation step, but the current internal projection alone lacks publication,
Resource binding, and a client-safe delivery contract. A compatible extension
of the v2 wire shape would risk mixed v2/v3 fields and ambiguous admission.
Unsupported, absent, conflicting, or mixed package, EIP delivery, and response
versions fail closed. No v3-to-v2 field stripping, downgrade, fallback, or
partial release is allowed.

## 5. Producer content schema

The only source recommendation shape is the producer's ordered five-field
`governedConclusions.recommendations[]` record:

| Producer field, in canonical order | Specified future use |
| --- | --- |
| `findingId` | Required exact finding linkage; `null` only for the complete producer-defined no-findings recommendation. Trusted-only. |
| `recommendationClassification` | Required rule-output validation. Trusted-only for this new response. |
| `recommendationDecisionIdentifier` | Required exact approved rule-to-text lookup and identity validation. Trusted-only. |
| `recommendationDecisionTableVersion` | Required value `recommendation-decision-table-set-v1`. Trusted-only. |
| `recommendationActionText` | Required exact approved text; sole approved client-visible recommendation value for this specification. |

Reject missing, extra, duplicate, reordered, or changed records; invalid
one-to-one finding links; invalid no-findings count, `null` link, rule or
`monitor` classification; and text differing by any character from the
producer-approved mapping. Preserve producer order; never sort, summarize,
truncate, generate, or infer actions or finding descriptions. The package must
be explicitly selected as `business-decision-package-v3`, with
`versionMetadata.assessmentVersion=nguyen-ai-executive-assessment-v2`,
`versionMetadata.methodologyVersion=business-decision-methodology-v1`, and
snapshot envelope `executive-runtime-response-v1`. These are producer version
values, not proposed EIP envelope fields.

## 6. Client-visible field allowlist

The specified EIP recommendation-action content allowlist contains an ordered
`recommendations[]` array whose sole item field is the exact
`recommendationActionText`. `recommendations[]` is a delivery grouping, not a
new producer record field; array position preserves producer order. The
trusted response may contain only the separately approved response
`contractVersion`, deterministic `explanation` composed of those exact text
values and approved fixed sentence patterns, required client-safe
`limitations`, and `sourceReferences: []`. This follows the Stage 4B response
roles without authorizing a current v1 response change. No client-safe source
reference representation is approved here. Retain the Stage 4B bounds of one
question (500 characters and 2,000 UTF-8 bytes), 64 admitted facts and 16,384
UTF-8 context bytes, and a 1,200-character / 4,800-byte response with at most
12 fact references; oversized complete content fails without truncation.

`recommendationClassification` is already exposed as a classification in the
legacy v2 EXPLAIN path, but is **not** automatically admitted alongside new v3
action text. Raw `findingId`, `recommendationDecisionIdentifier`,
`recommendationDecisionTableVersion`, synthetic labels, priority, title,
description, score, and internal reference are excluded. A later separately
approved contract would be needed to add client-safe context. The specified
v3 EIP delivery and trusted response must reject unknown, extra, or unsupported
fields, rather than silently ignore them.

## 7. Trusted-only validation evidence

The trusted boundary must verify the complete five-field producer records,
record order, package and methodology versions, decision-table version,
approved rule-to-text mapping, signed snapshot bytes and sidecar, attestation
profile, digest/signature verification, producer snapshot identity, and exact
EIP source lineage. EIP delivery envelope version, field classification,
limitations, integrity, compatibility, publication revision, and release
evidence are EIP-owned metadata, not producer recommendation fields. Keep raw
identifiers, finding linkage, signatures, digests, private snapshot identity,
verification internals, Principal Mapping, Membership, Entitlement, and audit
records out of model context and client responses. Trusted evidence must remain
available for deterministic validation and server-side custody.

## 8. EIP publication and currentness

**Approved future contractual obligation:** EIP must establish explicit v3
publication eligibility and evidence for the exact verified producer package,
approved text, version pair, signed authenticity, complete lineage, artifact
integrity, compatible delivery version, approved classification and limitations,
current publication occurrence and revision, freshness, and no withdrawal or
supersession. The Resource-to-Artifact Binding Authority must independently
select the exact Resource, assessment instance, producer snapshot, EIP artifact,
and one current approved revision from authoritative evidence. The trusted
boundary must verify both authorities before admission and again before
release, including source freshness, field/version eligibility, and revocation
state. Missing, stale, ambiguous, or forged evidence blocks release.

The existing local v3 gateway's expected-producer-release check proves neither
EIP publication currentness nor current Resource selection. No deployed v3
publication authority or concrete production Binding Authority is claimed.
The existing internal projection stays `release_eligible=False`; this
specification is not an executable release flag.

## 9. EXPLAIN authorization and field admission

Keep the existing `EXECUTIVE_DASHBOARD × EXPLAIN` Resource/Action boundary. A
**separate explicit, versioned v3 field-scope admission condition is required**;
the current `EXPLAIN` permission does not itself cover the new action text.
This condition must be approved and implemented before any v3 fact reaches the
Assistant or client. It creates no new Resource identity or principal grant.

For the exact governed Resource, verify server-side Principal identity and
current Principal Mapping; authoritative Resource, Engagement, and Business
Entity binding and isolation; applicable current Membership; independent
exact-resource `EXPLAIN` Entitlement; applicability and revocation; and valid
authorization and source audit/custody evidence. Require a fresh Trusted
Authorization `ALLOW` before protected admission and again before release,
with fresh field-scope, publication, binding, source, and revocation checks at
release. `VIEW` is insufficient. Browser selections, caller assertions,
model output, and prior `ALLOW` cannot establish authority.

## 10. Fail-closed response contract

Any failed required gate returns exactly `{"decision":"DENY"}` from the
trusted boundary, with no protected text, identifiers, internal evidence,
resource-existence hint, or sensitive error detail. This includes release
ineligibility; missing or forged eligibility evidence; unsupported or mixed
versions; producer package or methodology mismatch; altered text, order, or
linkage; extra fields; stale or wrong Resource binding; stale publication;
cross-Resource, Engagement or Business Entity content; absent, VIEW-only or
revoked `EXPLAIN`; and uncertain source or authorization currentness. Do not
fall back to v2 content, an earlier revision, or generated prose.

Only after every authorization and source gate passes may an otherwise
authorized, out-of-scope question receive a separately approved fixed neutral
refusal. That refusal is distinct from trusted-adapter `DENY`. The existing
Website v1 normalizer represents exact `DENY` as `access_denied` and its fixed
v1 refusal as `refusal`; no new Website response behavior is activated here.

## 11. Legacy v2 isolation

Keep `website-projection-delivery-contract-v1`, its governed v2 publisher,
Dashboard `VIEW`, existing six EXPLAIN subjects, and
`cep-nonproduction-dashboard-explain-contract-v1` unchanged. The v2 package
retains its four-field recommendation record and rejects
`recommendationActionText`; a v3 record cannot be treated as v2. Existing
REPORT denial and production routes remain unchanged. This specification
grants no v2 field expansion or compatibility bypass.

## 12. Implementation ownership and sequence

Each step is a separate bounded increment requiring explicit founder
implementation authorization after this contract approval:

1. **EIP:** Build a separately versioned governed v3 delivery projection and
   release-evidence validation, retaining producer truth and v2 isolation.
2. **Trusted Authorization / Assistant:** Admit the explicit v3 EXPLAIN field
   scope under fresh exact-resource authorization and currentness checks;
   render only exact admitted text with deterministic grounding.
3. **CEP / Website:** Strictly normalize the separately versioned response and
   present only authorized client-safe fields. Website remains presentation-only.

Assessment Service retains producer methodology and snapshot authority; none
of these steps authorizes producer changes. Contract approval alone authorizes
none of these steps.

## 13. Required acceptance and regression tests

**Future positive cases:** exact signed v3 producer content; explicit approved
field/version scope; valid EIP publication evidence; current exact
Resource-to-Artifact binding; fresh exact-resource `EXPLAIN` authorization at
admission and release; character-for-character action text; producer order;
valid finding linkage and no-findings semantics; deterministic bounded output.

**Future negative cases:** release-ineligible content; missing or forged
release/eligibility evidence; wrong package, assessment, methodology,
decision-table, snapshot, attestation, delivery, or response version; mixed
v2/v3 fields; modified action text; changed order; missing, extra, or duplicate
recommendation records; invalid finding linkage or no-findings case;
cross-Resource, cross-Engagement or cross-Business-Entity content; VIEW-only
access; missing, revoked, or stale `EXPLAIN` authority; stale source,
publication, revision, or Resource binding; unapproved fields; and protected
data in `DENY` or error responses. Test fresh admission and release decisions,
revocation between them, and failure without fallback.

**Future regressions:** existing v2 Dashboard output, six EXPLAIN subjects,
legacy VIEW, REPORT denial, and production routes remain unchanged. These are
requirements for separately authorized implementation, not tests in this
milestone.

## 14. Explicit exclusions

No producer wording, recommendation rule, score, methodology, finding
description, inferred action, per-recommendation priority, raw assessment
input, new Resource identity, standing governance role, principal grant,
publication activation, v2 Dashboard or EXPLAIN v1 extension, REPORT
eligibility, Website Assistant activation, AWS/Bedrock call, production route,
deployment, or client-facing delivery is authorized by this specification.

## 15. Founder contract decision

"Approve or defer the proposed versioned nonproduction Dashboard EXPLAIN delivery and field-scope contract for exact producer-approved v3 recommendation action text, subject to separate implementation, release-evidence verification, authorization, and deployment decisions."

**Decision: APPROVE PROPOSED CONTRACT.**

**Decision authority:** Nguyen AI Enterprise LLC founder/owner.

**Decision date:** 2026-11-08.

The founder approves the exact Stage 4H.5B specification in sections 1–14.
This decision grants no implementation or release authority.

## 16. Effectiveness and activation conditions

The founder's approval establishes only this versioned contract specification.
Separate implementation authorization, EIP release-evidence realization and review,
explicit v3 field admission, fresh individual authorization, current
Resource-to-Artifact selection, client-facing publication decision, and any
deployment decision remain independently required. Stage 4H.5A remains closed;
limited content eligibility remains approved; client-facing v3 delivery
remains unauthorized; roadmap Stage 4 remains **IN PROGRESS**.
