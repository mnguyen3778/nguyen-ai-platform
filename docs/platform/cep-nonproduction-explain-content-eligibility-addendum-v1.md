# CEP Nonproduction EXPLAIN Content Eligibility Addendum v1

Version: `cep-nonproduction-explain-content-eligibility-addendum-v1`

Status: bounded, nonproduction content eligibility contract. This addendum
narrows content selection under the [Stage 4B Dashboard EXPLAIN Contract v1](cep-nonproduction-dashboard-explain-contract-v1.md); it changes neither that
contract nor any runtime, entitlement, projection, or release authority.

## 1. Purpose and authority

This contract governs whether a finding or recommendation value is eligible as
client-readable content in a future nonproduction CEP `EXPLAIN` response. The
Assessment Service alone owns deterministic assessment truth and approved
business meaning. EIP owns governed projection and Website delivery. Trusted
Authorization owns exact-resource access decisions. The Assistant may select
and render only admitted facts under Stage 4B. The Website presents the
released response only. No LLM-generated assessment meaning, inferred action,
or new recommendation is authorized.

## 2. Verified field provenance and decisions

`governedConclusions` below denotes the preserved Assessment Service content
in the EIP source-derived artifact, read by
`executive-intelligence-platform/src/executive_intelligence_platform/projection_delivery/delivery.py`
at `_publish_governed_dashboard_content`. The producer serialization is in
`nguyen-ai-assessment-service/src/assessment/business_decision_package.py`
(`_governed_conclusions_to_dict`); its published field set is checked by
`src/assessment/producer_snapshot_attestation.py` in that repository. EIP's
mapping and its exact value preservation are exercised by
`executive-intelligence-platform/tests/projection_delivery/test_assessment_service_snapshot_delivery.py`.
Paths here are evidence for maintainers, never client source references.

| Candidate / implemented producer field and authority | EIP governed field → existing Website delivery representation | Current Assistant exposure | Readability and eligibility decision; evidence |
| --- | --- | --- | --- |
| Finding identity: `FindingInput.finding_id` → `severityAssignedFindings[].findingId`; Assessment Service identity, not prose (`src/assessment/governed_assessment_input.py`, `src/assessment/business_decision_package.py`) | `governedConclusions.severityAssignedFindings[].findingId` → `dashboardContent.findings.items[].fields[]` with label `findingId` | Not selected as a finding fact; may be displayed by Dashboard delivery | **NOT CURRENTLY ELIGIBLE** as readable explanation prose. It is an internal identifier. EIP delivery mapping lines for findings and its delivery test verify the field. |
| Finding title: `FindingInput.title` → `severityAssignedFindings[].title`; Assessment Service owns its meaning (same producer paths) | `governedConclusions.severityAssignedFindings[].title` → `dashboardContent.findings.items[].label` | `_facts` selects this `label`; finding pattern renders `An approved finding is: {value}` | **CONDITIONALLY ELIGIBLE — specific prerequisite:** verified producer provenance, exact value trace, and separately approved client-facing semantics for the actual title, followed by current governed delivery and exact-R `EXPLAIN` authorization. `tests/test_golden_fixture_regression.py` sets `title = identifier`; current synthetic title is therefore **not** readable prose. EIP delivery test proves title-to-label equality; Assistant adapter and test prove current identifier exposure. |
| Finding description: no `FindingInput` or published `severityAssignedFindings[]` description field; no producer authority established (`src/assessment/governed_assessment_input.py`, `src/assessment/producer_snapshot_attestation.py`) | None; no `dashboardContent.findings` description | None | **NOT CURRENTLY ELIGIBLE.** No description exists in the verified producer schema or EIP mapping. Do not infer one from title, type, consequence basis, or evidence. |
| Finding evidence reference: `FindingInput.source_references` → `severityAssignedFindings[].sourceReferences`; Assessment Service evidence linkage (`src/assessment/governed_assessment_input.py`, `src/assessment/business_decision_package.py`) | Preserved in governed conclusions; omitted from `dashboardContent.findings.items[]` by EIP mapping | None; successful response uses `sourceReferences: []` | **NOT CURRENTLY ELIGIBLE** for client display. Producer linkage is verified, but no approved client-safe reference or delivery representation is established. |
| Recommendation finding link: `GovernedRecommendationResult.finding_id` → `recommendations[].findingId`; Assessment Service link to a finding, nullable for no findings (`src/assessment/governed_decision_runtime.py`, `src/assessment/business_decision_package.py`) | `governedConclusions.recommendations[].findingId` → `dashboardContent.recommendations.items[].label` when present, and `fields[]` label `findingId` | Not selected as a recommendation fact | **NOT CURRENTLY ELIGIBLE** as readable action text. The label is the finding ID or generic `Recommendation`, not recommendation content. EIP mapping and delivery test verify this representation. |
| Recommendation classification: `GovernedRecommendationResult.recommendation_classification` → `recommendations[].recommendationClassification`; Assessment Service deterministic decision-table output (`src/assessment/governed_decision_runtime.py`, `src/assessment/business_decision_package.py`) | `governedConclusions.recommendations[].recommendationClassification` → `dashboardContent.recommendations.items[].fields[]` label `recommendationClassification` | `_facts` selects the value; pattern explicitly says `recommendation classification` | **ELIGIBLE UNDER EXISTING VERIFIED AUTHORITY** only as an exact classification with its classification label, after Stage 4B release gates. It is **not** eligible as recommendation action prose. `priority-action` is a classification, repeated in the synthetic fixture; producer decision-table and EIP delivery tests verify the chain. |
| Recommendation decision identifier: `GovernedRecommendationResult.recommendation_decision_identifier` → `recommendations[].recommendationDecisionIdentifier`; Assessment Service rule identity (`src/assessment/governed_decision_runtime.py`, `src/assessment/business_decision_package.py`) | Preserved in governed conclusions; omitted from Website delivery recommendations | None | **NOT CURRENTLY ELIGIBLE** for client display. It is rule lineage, not an action or client reference. Producer attestation lists it; EIP mapping omits it. |
| Recommendation description/action text: no field in `GovernedRecommendationResult` or the published `recommendations[]` schema (`src/assessment/governed_decision_runtime.py`, `src/assessment/producer_snapshot_attestation.py`) | None | None | **NOT CURRENTLY ELIGIBLE.** There is no verified producer-approved client-readable action text. No hypothetical field is authorized by this addendum. |
| Recommendation priority: the separate `RecommendationPriorityEvaluation` and `recommendationPriorityEvaluation` package component exist (`src/assessment/recommendation_priority.py`, `src/assessment/business_decision_package.py`), but `GovernedRecommendationResult` has no priority field | No per-recommendation priority in `governedConclusions.recommendations[]` or `dashboardContent.recommendations.items[]` | None | **NOT CURRENTLY ELIGIBLE** as a recommendation priority or action. The separate evaluation does not establish a per-recommendation priority in this delivery. Classification `priority-action` must not be recast as a priority value. |

The Assistant evidence is
`aws-ai-knowledge-assistant/src/trusted_authentication/non_production_dashboard_explanation_adapter.py`
and `tests/test_non_production_dashboard_explanation_adapter.py`. The Website
consumer is `nguyen-ai-website/src/lib/dashboard-explanation-delivery.ts` and
`src/app/portal/nonproduction/executive-dashboard/explanation-interaction.tsx`;
its integration tests reject nonempty `sourceReferences`. These paths prove
present behavior; they do not approve a new field or response shape.

## 3. Eligibility rules

A finding title may be displayed as readable explanation content only when its
Assessment Service producer provenance and exact `title` → EIP `label` trace
are verified for the current governed projection, its actual value has
approved client-facing semantics and is readable prose, and fresh
resource-specific `EXPLAIN` authorization and every Stage 4B release gate
pass. A title containing only an identifier fails the readability condition.
A finding description requires an implemented, verified producer field and
explicit semantic approval before it can be considered; this addendum grants
none. Missing text is never inferred.

For recommendations, keep identity, classification, description/action text,
priority, and approved client-readable meaning distinct. The present
classification may be rendered only as a classification. `priority-action`
cannot become an invented instruction, action, priority, or description. No
verified approved recommendation description currently exists, so readable
recommendation action text remains unavailable. A future producer field name
or shape must be established and approved separately before eligibility can
be reconsidered.

## 4. Client-safe references and privacy

The Stage 4B response permits only approved client-safe `sourceReferences` and
allows an empty array. Current adapter output and Website validation use an
empty array. This addendum defines no new client-reference format and
approves no current finding evidence reference for display. Internal
repository paths, private lineage identifiers, authorization tokens, tenant
secrets, internal assessment implementation details, unapproved raw inputs,
and unnecessary PII are excluded from model context and client response.
Trusted validators may retain internal provenance server-side.

## 5. Authorization and fail-closed release

Every eligible value remains subject to the Stage 4B independent `EXPLAIN`
Entitlement and fresh Trusted Authorization `ALLOW` for exact Dashboard R,
with verified Engagement E and Business Entity B binding and isolation,
Principal Mapping, Membership, applicability, current governed source and
publication revision, lineage, revocation, and audit/custody evidence. The
trusted boundary rechecks authorization and source currentness before release.
Browser-selected identity, question, prompt, model output, or caller assertion
cannot supply authority. Missing or ineligible content is omitted from the
eligible fact set; it is never replaced with fabricated prose. A failed
required release gate returns exactly `{"decision":"DENY"}` without content.
An authorized out-of-scope question may receive only the Stage 4B fixed
refusal after its required checks; refusal and DENY remain distinct. This
addendum grants no REPORT delivery or production route behavior.

## 6. Subsequent bounded implementation dependencies

If client-readable finding text is pursued, Assessment Service must first
provide an approved client-facing title value or separately approved
description from deterministic governed input, with tests for provenance and
meaning. EIP would then verify and project only the approved source field
through a versioned delivery contract. The trusted adapter would admit and
render only eligible values after the existing exact-resource checks. Website
would validate and present that approved response contract. For recommendation
action text, the first missing dependency is a separately approved,
deterministic Assessment Service producer definition and actual field;
subsequent EIP, adapter, and Website changes each require their own bounded
approval and tests. No change in those repositories, AWS, Bedrock, production
integration, or deployment is authorized here.
