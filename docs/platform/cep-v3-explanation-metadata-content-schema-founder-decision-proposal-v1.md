# CEP v3 Explanation Metadata Content and Schema Founder Decision Proposal v1

**STATUS: FOUNDER APPROVED — SYNTHETIC v3 METADATA POLICY**

**Stage:** 4H.9C — founder-approved policy promotion

**Draft date:** 2026-11-13

**Approval date:** 2026-11-13

**Approving authority:** Nguyen AI Enterprise LLC Founder/Owner

**Decision:** APPROVED WITH POLICY-REVISION CLARIFICATION

**Authorization in this task:** this policy document only; controlled staging, commit and push

**Implementation, deployment, and client release:** NOT AUTHORIZED

## 1. Purpose and bounded scope

Record founder approval of one coherent decision package for the three Stage 4H.9B gaps: exact
client-safe v3 limitations, EIP-owned field classification, and an exact
synthetic metadata verification contract. Decisions A, B and C are explicitly
approved by the founder record in §14, subject only to the policy-revision
clarification in §7. Drafting authorization,
this filename, presence in Git, and a synthetic passing test do not constitute
that approval.

This package preserves Assessment Service truth, EIP delivery/publication
ownership, independent Continuity and Binding Authorities, Trusted
Authorization principal decisions, and Website presentation ownership. It
defines no production source, runtime, persistence, API, new scoring model,
publication approval, or client release.

## 2. Existing governing authority — ALREADY APPROVED

The following decisions are present in Platform history at the verified
baseline. Approval is established by their recorded decisions and history,
not by their filenames. Historical implementation-status statements describe
their own milestone; they do not negate later separately promoted work.

| Governing document | Recorded approval / promoted commit | Applicable sections |
| --- | --- | --- |
| [v3 content eligibility](cep-v3-recommendation-action-explain-eligibility-decision-v1.md) | Limited eligibility; `5f3dd318b47e1c0a4ba6f9d80553b4b70c58577c` | §§4–7: exact five-field producer records, ordered exact text, trusted-only linkage, separate release gates. |
| [v3 delivery specification](cep-v3-recommendation-action-explain-delivery-contract-proposal-v1.md) | Founder decision §15 approves §§1–14; `b66daa77d84cec4d4eb139f1b6a118bf2c32f631` | §§4, 6–10: versions, response allowlist, limits, EIP metadata ownership, currentness, exact DENY. |
| [Logical authority sources](cep-v3-publication-binding-continuity-logical-authority-source-decision-v1.md) | Founder logical-source approval; `f34b1d3bce1c9d7a646e1679f991fbc081bdcb08` | §§2–3: independent publication, instance bridge, Resource selection; applicability and lifecycle. |
| [Publication evidence/freshness](cep-v3-publication-authority-evidence-freshness-contract-decision-v1.md) | Founder behavioral approval; `7b6656d08394f3cb860c98d4937c7239e8813c2c` | §§3–9: artifact integrity, explicit publication evidence, complete current reads, provenance, no standing release. |
| [Serialized artifact identity](cep-v3-serialized-artifact-instance-identity-contract-decision-v1.md) | Founder minimum synthetic contract; `91ea84e8b0c99b3e9c3d0f3f400fd9a8b96bb994` | §§2–7: independent assigned ID, canonical bytes, SHA-256, scope, separate metadata gates. |
| [Dashboard EXPLAIN contract](cep-nonproduction-dashboard-explain-contract-v1.md) | Existing governed contract; `fc5667610365827c1c202117cc30cb1bb635a3fd` | §§3–7, incorporated by v3 specification: bounded facts, complete limitations, deterministic grounding, denial privacy. |

Already approved requirements include the four future response members
`contractVersion`, `explanation`, `limitations`, and `sourceReferences: []`.
The response discriminator is
`cep-nonproduction-dashboard-recommendation-action-explain-contract-v1`;
EIP delivery uses
`website-recommendation-action-explain-delivery-contract-v1`.
Only exact `recommendationActionText` is eligible recommendation content.
Producer `recommendationClassification` is not admitted to this v3 response.

The inherited limits remain: one question, 500 Unicode characters / 2,000
UTF-8 bytes; at most 64 admitted facts / 16,384 context bytes; at most
1,200 response characters / 4,800 response bytes and 12 fact references.
No truncation, reordering, partial release, downgrade, or fallback is allowed.
Metadata approval does not approve rendering patterns or activate any response.

EIP [delivery governance](../../../executive-intelligence-platform/docs/architecture/website-facing-projection-delivery-contract-versioning-policy-architecture-v1.md),
§§16–18, requires visible applicable limitations and approved classifications.
Its permitted concepts include `portal_operational` and
`restricted_assessment`; it does not assign the exact new v3 mapping.

## 3. Exact blocker and verified implementation facts

Stage 4H.9B stopped without files: the v3 specification, lines 126–157,
requires limitations and EIP classification without defining exact v3 wording,
applicability, classification mapping, or a complete metadata schema.
The identity decision, lines 92–97, expressly leaves those gates separate.

Read-only implementation evidence:

| Existing component | Verified capability | Does not supply |
| --- | --- | --- |
| EIP `projection_delivery/recommendation_action_explain_delivery.py` | Exact delivery version, verified projection, strict ordered action-text content, `release_eligible=False`. | Limitations or EIP field-classification evidence. |
| EIP `snapshot_derivation/local_v3_recommendation_projection.py` | Same-gateway fresh signed-source delivery; complete five-field records, snapshot identity, verification evidence. | A new assessment-instance identity or EIP disclosure classification. |
| EIP `projection_delivery/non_production_v3_serialized_artifact.py` | Assigned artifact ID, exact canonical bytes, digest, Business Entity/environment/Engagement scope. | Client/workspace or assessment-instance authority; publication currentness. |
| EIP `projection_delivery/non_production_v3_publication_evidence.py` | Independently held synthetic fixture comparison, artifact/bytes/digest/lineage verification, occurrence/revision/generation and lifecycle checks. | Limitations content, continuity, Resource selection, live publication authority. |
| Trusted `trusted_authorization/non_production_v3_dashboard_explain_admission.py` | Compares separately verified publication, continuity, binding and exact-resource authorization; repeats source reads; returns frozen `VerifiedV3DashboardExplainAdmission`. | Client-safe explanation or metadata policy; its success remains non-releasable. |

The existing Trusted continuity and binding verifiers carry provenance and
independent generations. Their returned identities can support the synthetic
handoff without changing ownership. A constructed result object or caller
dictionary alone cannot prove that those verifiers ran.

The Assessment Service v3 package retains a root `limitations` field.
Its implementation contains internal capability indicators, not approved
client-safe v3 explanation wording. Their presence does not justify copying
v2 wording or forwarding internal indicators. This proposal neither rewrites
those producer values nor claims they are already approved response text.

## 4. Decision A — approved limitations policy

**ALREADY APPROVED:** complete applicable client-safe limitations are required;
exact v3 limitation wording is not established in the inspected contracts.
The producer's no-findings interpretation constraint is approved business
meaning, but its use as a v3 response limitation requires this decision.

**FOUNDER APPROVED:** adopt only the following finite,
ordered set for this synthetic profile. IDs are internal provenance keys,
never extra client fields. Wording is literal, including punctuation.

| Internal ID | Exact approved wording | Business meaning and applicability | Evidence / responsible owner | Validation and failure |
| --- | --- | --- | --- | --- |
| `scope-v1` | Only approved recommendation action text is included; finding details and implementation plans are outside this explanation. | Static; always first. Describes this response's narrow content; does not claim that no underlying findings or plans exist. | v3 specification §§5–6, 14; producer action-text addendum, presentation-only authority. EIP owns this delivery limitation; Assessment Service retains underlying text/methodology. | Exact text required; verify the complete candidate and strict content allowlist. Missing, changed, extra, or unsupported content: DENY. |
| `nonproduction-v1` | This explanation is for nonproduction verification only; client release is not authorized. | Static; always second. States the bounded proof's release restriction, not an assessment conclusion. | v3 specification §§8, 14–16; immutable false release state in EIP candidate/artifact and Trusted admission. EIP owns delivery metadata. | All relevant success objects must retain `release_eligible=False`; exact wording required. Any claimed release eligibility or missing evidence: DENY. |
| `no-findings-v1` | No findings in this assessment does not establish absence of business risk, guaranteed compliance or safety, or that future assessment or improvement is unnecessary. | Conditional; third only for the complete producer-defined no-findings recommendation. Prevents overinterpreting that exact action text. | Assessment Service [action-text addendum](../../../nguyen-ai-assessment-service/docs/business-decision-methodology/31-recommendation-action-text-addendum-v1.md), no-findings paragraph; v3 package contract no-findings semantics. Assessment Service owns meaning; EIP owns applicability and exact delivery wording. | Apply only after fresh producer verification establishes the sole record: rule `recommendation-v1-no-findings-monitor`, `findingId=null`, class `monitor`, exact mapped text and no-findings completeness. Any ambiguity: DENY. Wrong inclusion or omission: DENY. |

All three wording decisions are **founder approved**. No statement is copied from v2
delivery limitations. Applicability is derived from verified rule identity and
linkage, never from action prose, caller labels, or an LLM.

The complete expected array is exactly `[scope-v1, nonproduction-v1]` for
finding-scoped content, or those two followed by `no-findings-v1` for the
verified no-findings case. The corresponding text array has the same order.
An empty array, missing limitation, duplicate, additional disclaimer, changed
character, or inconsistent ID/text pairing denies the entire result.

This is approved completeness for this exact narrow synthetic profile, not
a conclusion that every package-wide limitation is irrelevant forever.
Projection/package/methodology and field-visibility scope are covered by the
first statement and conditional caveat; production/publication capability is
restricted by the second. Unsupported compatibility, stale publication, or
unknown currentness must DENY, never become warning text that permits success.
No claims about accuracy guarantees, evidence coverage, legal compliance,
implementation success, or production readiness are supported or proposed.
Broader findings, scores, reports, production delivery, or a newly applicable
producer restriction are outside this profile and require review rather than
silent omission or fallback. No missing business input is needed to state
the three approved sentences; founder acceptance of their sufficiency is
recorded in §14.

## 5. Decision B — exact approved field classification matrix

**FOUNDER APPROVED:** use the existing classification
concepts below. Visibility categories are disclosure rules; classification
labels are EIP metadata. Neither is a principal authorization grant.

All client-visible rows describe the approved future response field scope,
with the exact classification assignment approved here. Every row's
serialization/validation rule applies to the whole result. All non-client
rows remain excluded even when a future release is independently authorized.

| Field / evidence | Category | Approved classification | Source authority and justification | Serialization and required validation | Approval status |
| --- | --- | --- | --- | --- | --- |
| `contractVersion` | CLIENT-VISIBLE | `portal_operational` | EIP/Trusted version compatibility; public contract discriminator carries no selected identity. | Exact v3 response version only. | Field role existing; mapping approved. |
| `explanation` | CLIENT-VISIBLE | `restricted_assessment` | Assessment Service exact action text; Trusted deterministic rendering. Contains selected assessment content. | Exact admitted text/order and separately approved patterns; inherited output bounds. | Field role existing; mapping approved; no renderer approved here. |
| `content.recommendations[].recommendationActionText` | CLIENT-VISIBLE content source | `restricted_assessment` | Verified producer text projected by EIP. | Only source for future explanation; no additional top-level response member or raw content object. Character-for-character validation. | Content eligibility existing; mapping approved. |
| `limitations[]` | CLIENT-VISIBLE | `restricted_assessment` | EIP policy; conditional membership may reveal selected assessment context. | Exact complete §4 text array only. No IDs/provenance. | Field role existing; wording/mapping approved. |
| `sourceReferences` | CLIENT-VISIBLE | `portal_operational` | Existing v3 specification permits no client-safe citation representation. | Exactly empty array; nonempty denies. | Empty-only role existing; mapping approved. |
| Whole future response | CLIENT-VISIBLE | `restricted_assessment` | Inherits its most restrictive assessment content classification. | Exactly four approved response keys; no classification property added. | Mapping approved. |
| `response_classification`, `field_classifications` | TRUSTED-INTERNAL ONLY | Control-plane evidence; no client label | EIP owns approval mapping, not recommendation meaning. | Exact constants in §6; never serialize to client/model. | Ownership/exclusion existing; schema approved. |
| Signed snapshot bytes, sidecar, `verification_evidence` | TRUSTED-INTERNAL ONLY | Protected producer verification evidence | Assessment Service authenticity; EIP consumes signatures. | Verify original signed bytes/profile/issuer/key/release; keep outside metadata JSON and response. | Exclusion existing. |
| `recommendationClassification`, `findingId`, `recommendationDecisionIdentifier`, `recommendationDecisionTableVersion` | TRUSTED-INTERNAL ONLY | Protected producer validation evidence | Assessment Service deterministic rule output. Distinct from EIP disclosure classification. | Verify complete ordered records; never emit classifications, IDs or linkage in v3 response. | Existing trusted-only rule. |
| `artifact_instance_id` / artifact `artifactInstanceId` | TRUSTED-INTERNAL ONLY | Protected identity evidence | EIP assigns immutable instance ID. | Exact selected ID, independently checked; never replace with digest. | Identity/exclusion existing; metadata path approved. |
| `artifact_integrity_reference` | TRUSTED-INTERNAL ONLY | Protected integrity evidence | EIP exact serialized representation. | Recomputed `sha256:` digest; never a substitute ID. | Existing proof; metadata path approved. |
| `occurrence`, `revision` | TRUSTED-INTERNAL ONLY | Protected publication evidence | EIP publication owner. | Exact selection and current lifecycle; no alternate publication. | Existing proof. |
| `publication_generation`, `continuity_generation`, `binding_generation` | TRUSTED-INTERNAL ONLY | Protected currentness evidence | Each independent source owns its own generation. | Compare separate fresh reads; generations are not interchangeable. | Existing ownership; envelope placement approved. |
| Scope/instance/snapshot/Resource identifiers in §6 | TRUSTED-INTERNAL ONLY | Protected lineage and isolation evidence | EIP scope, Continuity Authority bridge, Binding Authority Resource selection. | Exact equality across independent results; applicable scope required. | Existing ownership; schema approved. |
| Publication/continuity/binding source records, audit/currentness evidence | TRUSTED-INTERNAL ONLY | Protected authority evidence | Respective source owner; Trusted audit custody. | Keep raw records outside metadata; validate provenance and availability. | Existing exclusion. |
| `InternalRecommendationActionExplainDeliveryCandidate`, `verified_projection`, artifact bytes | TRUSTED-INTERNAL ONLY | Protected internal content/evidence | EIP verified admission/projection. | Reverify; no whole-object serialization or model context. | Existing exclusion. |
| `VerifiedV3DashboardExplainAdmission`, other positive verification results | TRUSTED-INTERNAL ONLY | Protected admission evidence | Trusted coordinator composes independent checks. | Positive type alone insufficient; require trusted invocation and fresh source verification. | Existing exclusion. |
| `release_eligible` | TRUSTED-INTERNAL ONLY | Control-plane state | Governing release restriction. | Exact boolean false, fixed by construction; no truthy coercion or client field. | False requirement existing; envelope placement approved. |
| Internal risk/score computations, raw answers, scoring traces | PROHIBITED FROM CLIENT RESPONSE | Disallowed for this response | Assessment Service owns truth; no approved v3 response scope. | Reject any such client/candidate field; do not compute or reclassify. | Existing exclusion. |
| Principal identity, Principal Mapping, Membership, Entitlement, access token, credentials/secrets | PROHIBITED FROM CLIENT RESPONSE | Security/control-plane data | Trusted Authorization owns principal access. | No token/Principal fields in metadata envelope, model input, response, or errors. Existing verifiers retain necessary private custody. | Existing exclusion. |
| Internal exceptions, reason strings, debug details | PROHIBITED FROM CLIENT RESPONSE | Internal operational detail | Internal verification only. | Public failure is exact DENY; no exception or reason member. | Existing exclusion. |

The exact ordered machine mapping approved for `field_classifications` is:

```json
[
  {"field":"contractVersion","classification":"portal_operational"},
  {"field":"explanation","classification":"restricted_assessment"},
  {"field":"content.recommendations[].recommendationActionText","classification":"restricted_assessment"},
  {"field":"limitations[]","classification":"restricted_assessment"},
  {"field":"sourceReferences","classification":"portal_operational"}
]
```

No caller-supplied label can approve this mapping. Unknown, missing,
duplicate, reordered, or changed entries deny. Internal evidence is excluded
by the allowlist; it does not become client-safe by receiving a label.

## 6. Decision C — approved exact synthetic metadata contract

**FOUNDER APPROVED.** Contract version:
`eip-synthetic-v3-explain-metadata-v1`.

A separate verification envelope references the existing immutable artifact;
it does not modify, reserialize, or extend that artifact's frozen schema.
Every object below has exactly its listed keys, all required. Names newly
introduced here are approved internal contract fields, not claims that these
names already exist in producer output or a client response.

| Envelope path | Exact type / value |
| --- | --- |
| `contract_version` | String exactly `eip-synthetic-v3-explain-metadata-v1`. |
| `delivery_contract_version` | String exactly `website-recommendation-action-explain-delivery-contract-v1`. |
| `response_contract_version` | String exactly `cep-nonproduction-dashboard-recommendation-action-explain-contract-v1`. |
| `serialization_profile_version` | String exactly `eip-synthetic-v3-artifact-json-v1`; describes selected artifact bytes, not a new artifact profile. |
| `response_classification` | String exactly `restricted_assessment`. |
| `field_classifications` | Array exactly equal to the five ordered objects in §5; each object has only `field` and `classification`, both strings. |
| `limitation_ids` | Array of exactly two or three strings, deterministically selected and ordered by §4. |
| `limitations` | Array of exactly the corresponding two or three literal strings from §4. |
| `selection` | Object with exactly the twelve keys listed below. |
| `publication` | Object with exactly `occurrence`, `revision`, `publication_generation`, `state`. First three are identifiers; `state` is exactly string `current`. |
| `provenance` | Object with exactly the seven keys listed below. |
| `release_eligible` | Exact JSON boolean `false`. |

`selection` has exactly:
`resource_reference`, `business_entity_id`, `environment_id`,
`engagement_id`, `client_id`, `workspace_id`,
`assessment_instance_id`, `producer_snapshot_identity`,
`artifact_instance_id`, `artifact_integrity_reference`,
`client_required`, `workspace_required`.

Resource, Business Entity, environment, Engagement, assessment-instance and
artifact-instance references are required identifier strings. This minimum
profile requires Engagement, matching the existing Trusted v3 admission and
continuity proof; it does not outlaw inapplicable Engagement elsewhere.
Client/workspace fields are identifier strings iff the corresponding exact
boolean applicability flag is true; otherwise they must be null. Flags and
values must match independently held Binding Authority snapshot evidence.
Unknown applicability denies. Client and Business Entity are not presumed equal.

Snapshot identity and integrity reference each match
`sha256:[0-9a-f]{64}` over the entire string. Snapshot identity must match
fresh signed producer evidence; a syntactically valid digest is insufficient.
Artifact-instance ID must not start with `sha256:` or
`synthetic-v3-artifact:`, must differ from snapshot identity, occurrence and
revision, and must equal the independently selected assigned ID.

`provenance` has exactly:

| Key | Exact type / rule |
| --- | --- |
| `policy_reference` | String exactly `docs/platform/cep-v3-explanation-metadata-content-schema-founder-decision-proposal-v1.md`. This is a locator, not approval proof. |
| `policy_revision` | Exactly 40 lowercase hexadecimal Git commit characters, equal to the independently pinned promoted Platform main revision containing this explicit founder-approved policy decision, as defined in §7. The starting Platform baseline cannot satisfy that condition. |
| `publication_source_reference` | Identifier string equal to the trusted harness's independently held reference for the existing EIP publication fixture and reader; not supplied by the presented metadata. |
| `continuity_source_reference` | String exactly `synthetic-continuity-instance-bridge`, matching the existing Continuity verifier's source. |
| `binding_source_reference` | String exactly `synthetic-resource-current-selection`, matching the existing Binding verifier's source. |
| `continuity_generation` | Identifier equal to the fresh independently verified continuity generation. |
| `binding_generation` | Identifier equal to the fresh independently verified binding generation. |

Approved bounds: identifiers are 1–128 printable ASCII characters U+0020
through U+007E, with no leading/trailing whitespace or controls. The 128
character cap matches existing Trusted synthetic conventions and is a new
restriction on this metadata profile, not a change to artifact allocation.
Each limitation is at most 256 Unicode scalar values and 1,024 UTF-8 bytes;
the array is at most 768 scalars and 3,072 bytes in aggregate. Policy/version/
field-path strings are exact constants, not arbitrary bounded inputs.
The complete private metadata JSON is at most 16,384 UTF-8 bytes.

The private verification representation is strict UTF-8 JSON, without BOM,
with unique keys at every depth, sorted ASCII object keys, compact separators
and ASCII escaping as defined in the existing artifact profile §4. This
reuses encoding rules only; metadata is separate bytes and is not appended
to or hashed as part of the artifact. Require byte-for-byte canonical
reserialization. Preserve array order; reject lone surrogates, numbers,
non-finite constants, coercion, duplicate/unknown/missing keys and all other
types. Only the two scope nulls and the specified booleans are allowed.
If an internal constructor builds the envelope, it must build these exact
types directly; arbitrary pre-parsed caller mappings bypassing duplicate-key
validation are not an accepted verification input.

A. **Internal verification envelope:** all fields above; never serialize the
whole envelope to a client or model.

B. **Candidate client-safe metadata:** only the exact `limitations` text array
and the separately governed response version / empty `sourceReferences`
roles may be used in a future approved response constructor. No new
client-visible fields are proposed. A passing metadata proof does not
activate that constructor.

C. **Excluded raw authority evidence:** signed bytes/sidecar, artifact bytes,
publication/continuity/binding records, tokens, principal/access records and
audit internals remain outside the envelope, with their existing owners.
References in the envelope must resolve to independently held evidence;
references are never substitutes for verification.

## 7. Provenance, applicability and independently held evidence

The synthetic harness holds the approved policy pin, signed snapshot gateway
and admission, exact candidate/artifact/scope, selected publication fixture and
reader, and independently configured continuity and binding verifiers.
The presented envelope supplies comparison claims only. It cannot supply,
replace, or configure its own authorities or policy.

Policy provenance requires an explicit founder approval record for the exact
wording, mapping and schema plus its pinned promoted revision. Commit presence
alone is insufficient. The future implementation must have no success path
while that policy approval is absent.

The approved `policy_revision` is the full 40-character Git commit SHA of
the promoted Platform main commit containing this founder-approved metadata
policy decision. That revision is an immutable policy authority pin for
this contract. Subsequent EIP implementation commits, Trusted implementation
commits, test executions, or unrelated repository changes do not replace,
advance, or reinterpret this pin. A future policy revision requires a
separate explicit founder decision and controlled Platform promotion.

The verifier must compare the presented `policy_revision` against the
independently configured approved Platform policy pin. The presented metadata
cannot select or authorize its own policy revision. A missing, unapproved,
or mismatched policy revision must DENY.

The final promotion commit SHA is obtained after committing this approved
document and is then used as the independently pinned approved policy
revision for subsequent EIP implementation. This document need not contain
its own final commit SHA; no amendment or second commit may be created
merely to insert it. This avoids a circular commit-hash dependency.

Producer provenance comes from the existing owner-configured
`VerifiedSnapshotGateway` and fresh same-gateway signed-byte verification,
including version context, approved rule mapping, linkage and order.
The limitations are EIP policy-derived statements about that verified content
and the proof's release boundary; they are not new producer fields.

Publication provenance is the existing `SyntheticV3AuthoritySnapshot`
held independently from the presented evidence, plus a trusted current read
and `verify_synthetic_v3_publication`. The harness source reference identifies
that same fixture/reader binding. It is a synthetic custody reference, not a
new publication register, signature protocol or approver.

Continuity and Resource selection remain with the existing independent
verifiers in Trusted. Approved owner-configured reader callbacks invoke
`SyntheticV3ContinuityVerifier.verify` and
`SyntheticV3BindingVerifier.verify`, respectively, and return their exact
`VerifiedV3Continuity` / `VerifiedV3Binding` results. They close over
independently held fixtures, requests and readers; presented metadata cannot
supply these callbacks or instances. Validate source and record provenance,
availability/completeness, applicability flags and the existing verifier
contract versions; failures and exceptions deny. The harness retains the
source snapshots needed for flag/provenance checks outside the envelope.
These callbacks adapt existing interfaces; they do not move authority into
EIP. No EIP import of a principal token or new standing access dependency
is proposed. The existing admission coordinator is read-only integration
evidence, not an EIP-minted continuity or authorization result.

## 8. Exact artifact and publication binding

Build the expected envelope from independently verified evidence, then
compare the entire presented envelope for exact equality.

| Value | Required independent agreement |
| --- | --- |
| Business Entity/environment/Engagement | EIP trusted artifact scope and serialized envelope, continuity result, binding result and selected governed scope. Engagement must apply in this profile. |
| Client/workspace and applicability | Independently held Binding snapshot flags, selected binding result and expected governed scope. Never infer from Business Entity. |
| Assessment instance | Continuity bridge and Resource binding; never derived from snapshot digest. Different executions may share signed bytes. |
| Signed snapshot identity | Fresh gateway evidence, candidate projection, serialized artifact lineage, publication record, continuity and binding. |
| Artifact-instance ID | Exact selected Binding result, assigned serialized instance, and publication record/selector. Equal digest never substitutes. |
| Artifact digest/bytes | Recompute digest of exact frozen artifact bytes with `verify_synthetic_v3_artifact`; compare publication record and binding digest. |
| Occurrence/revision | Exact publication selector, verified publication evidence, binding result and envelope. Neither is the artifact ID. |
| Publication generation/state | Independently fresh EIP source, verified result and selected state; exactly current. |
| Continuity/binding generations | Each independent source and verifier result; never compared as if they were a shared generation. |
| Policy/classification/limitations | Independently approved policy revision, exact §5 mapping, and complete §4 applicability calculation over the same verified candidate. |

All required identities must already be available under their existing
sources. EIP must not allocate an assessment instance, fabricate scope, repair
a bridge, or choose a replacement artifact to complete metadata.

## 9. Deterministic validation and currentness

Approved future verifier sequence:

1. Check independently configured approved policy provenance; enforce input
   byte/type/size/schema/duplicate-key/version rules before content use.
2. Freshly verify the signed v3 source via the existing gateway. Re-prepare
   the exact candidate; compare all five producer fields and order through
   existing validation. Do not calculate scores or derive classification
   from text.
3. Verify exact assigned artifact identity, frozen canonical bytes, digest,
   supported profile, field scope and complete version context using the
   existing artifact validator.
4. Read EIP publication from its trusted reader and invoke the existing
   publication verifier against the independently held fixture, exact selector,
   artifact, candidate, gateway and scope. Require `SYNTHETIC_ACCEPTED`,
   bound evidence and `release_eligible=False`.
5. Invoke the independent continuity and binding readers/verifiers. Verify
   current state, provenance, applicability and every §8 equality.
6. Derive exact classification constants and the complete limitation set.
   Compare every envelope member to the independently built expectation.
7. Repeat publication, continuity and binding verification immediately before
   returning success. Require the same selected results, all three
   generations, applicable scope, and current lifecycle. Any changed,
   unavailable, incomplete, ambiguous or conflicting source denies. Do not
   retry against an alternate selection or silently advance the generation.
8. Return only the immutable trusted-internal result with fixed
   `release_eligible=False`.

Synthetic currentness is relative to independently held current fixtures and
readers, not a production freshness guarantee. Historical signed evidence,
timestamps, TTL, cached results or matching digest alone never prove current
authority. No freshness window or physical consistency mechanism is selected.
Concurrent changes discovered by either read invalidate success. A future
client release must repeat all applicable source and principal checks under
separate authorization; this result grants no standing authority.

Inherited question/context/response limits remain separate from metadata
bounds. A later renderer must count the complete limitations with its output
and reject oversized complete content, including worst-case no-findings text.
This metadata module neither creates an explanation nor approves a response
that merely fits its own envelope bound.

## 10. Fail-closed result and internal-only success

For any failure, including missing policy approval, malformed evidence,
unsupported classification, incomplete limitations, source exception,
wrong scope/identity, conflicting publication, stale generation, revocation,
withdrawal, supersession or invalidation, return exactly:

```json
{"decision":"DENY"}
```

No partial classification, limitations, recommendation text, reason string,
exception detail, identifier, snapshot/artifact bytes, authority record,
Principal, token or audit evidence accompanies DENY. No fallback metadata,
older revision, replacement artifact, generated disclaimer or v2 content.

Approved success is a frozen trusted-internal
`VerifiedSyntheticV3ExplainMetadata` containing the validated immutable
envelope fields and fixed `release_eligible=False`. It is not an `ALLOW`
response, release token, publication decision or client serializer. No general
`to_dict`/JSON serialization of the full success object to client/model.
A separate future boundary would explicitly select only approved fields.

## 11. Stage 4H.9B implementation handoff — NOT AUTHORIZED

After explicit approval and controlled promotion of this exact policy,
separate founder authorization may permit exactly three new EIP files:

- `src/executive_intelligence_platform/projection_delivery/non_production_v3_explain_metadata.py`
- `tests/projection_delivery/test_non_production_v3_explain_metadata.py`
- `docs/cep-stage-4h9b-synthetic-v3-explain-metadata-evidence-v1.md`

The test path follows the inspected EIP test layout; do not create a competing
root-level test module. No existing EIP or Trusted files need policy changes
under this approved policy handoff. Stop rather than alter a frozen interface.

Inputs: presented private metadata bytes; trusted approved-policy pin;
same-gateway signed admission and candidate; exact artifact, scope and
publication selector; independently held publication fixture/current reader;
independent current continuity/binding reader callbacks and their trusted
scope/applicability/provenance evidence. All dependencies are owner-configured,
not browser/model/request-provided. Use existing local source paths for
offline integration tests as the current Trusted integration test does;
no dependency installation, production credentials, live services or network
tests. Tokens needed by an existing Trusted integration harness remain in its
private proof, outside the EIP metadata interface.

Output: immutable verified internal metadata or exact content-free DENY.
Required validators and equality rules are §§6–9. Do not change artifact
bytes, publication schemas, producer truth or authority ownership.

Required focused matrix, each negative yielding exactly DENY:

| Cases | Required coverage |
| --- | --- |
| A, AF | Exact finding-scoped success and no-findings success; metadata bound to the exact selected artifact, occurrence and revision; repeated reads agree. |
| B–D | Missing classification, wrong mapping, unsupported classification. Test EIP field classifications separately from producer recommendation classes. |
| E–I | Missing/empty limitations, wrong type, oversized complete envelope/limitation, unapproved text; omitted or inapplicable conditional caveat. |
| J–L | Metadata limitations/evidence bound to another artifact, revision or occurrence. Identical static wording across artifacts is allowed; substitution of its bound envelope is not. |
| M–T | Wrong artifact ID; same presented digest with different ID; wrong signed snapshot, assessment instance, Business Entity, Engagement, environment or Client/workspace/applicability. |
| U–Y | Revoked/superseded/withdrawn/invalidated publication; generation mismatch; unavailable source; conflicting/ambiguous publication. |
| Z–AC | Missing/unapproved policy or source provenance; invalid metadata version; unknown/duplicate/missing keys; invalid encoding/types; internal authority/token/debug fields added; no leakage in errors. |
| AD–AE | No fallback and no partial output; exceptions, changed second reads, unavailable continuity/binding, stale independent generations all deny. |

Use separate producer signing/gateway trust, EIP artifact scope/publication
fixture and reader, Continuity fixture/reader and Binding fixture/reader.
Hold policy constants independently of presented metadata. Tamper with each
proposition while other evidence remains valid; a single caller-controlled
fixture cannot be its own authority. Synthetic equality proves only fixture
conformance. No claim of production authenticity follows.

Use the existing Python `unittest` conventions; prefer Python 3.14 and
`PYTHONDONTWRITEBYTECODE=1`. The following are inspected module names,
future commands from EIP root, not tests executed in Stage 4H.9C:

```sh
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests/projection_delivery -p test_non_production_v3_explain_metadata.py -v
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests/projection_delivery -p test_recommendation_action_explain_delivery.py -v
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests/projection_delivery -p test_non_production_v3_serialized_artifact.py -v
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests/projection_delivery -p test_non_production_v3_publication_evidence.py -v
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests/projection_delivery -p test_verified_admission.py -v
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests/projection_delivery -p test_local_v3_admission.py -v
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests/projection_delivery -p test_assessment_service_snapshot_delivery.py -v
PYTHONDONTWRITEBYTECODE=1 PYTHONPATH=src python3.14 -m unittest discover -s tests -q
```

Record actual executed/passed/failed/expected and unexpected skip counts;
historical evidence totals are not new results. New integration checks may
reuse the existing Trusted test fixtures in an isolated child process,
without editing them. Stop on network/credential/live-authority requirements,
missing approved evidence, regressions, or a need to modify existing files.

The evidence file must record starting/final baselines, approved policy
revision, exact metadata sources, all bindings/currentness, negative coverage,
content-free DENY, actual commands/results and the no-release restrictions.

## 12. Explicit exclusions and policy effectiveness

This proposal creates no assessment score, rank, rubric, recommendation,
methodology or producer limitation. It approves no new client response field,
citation, finding detail, recommendation classification disclosure, rendering
pattern, generic disclaimer fallback, v2 compatibility path, REPORT access or
Assessment Progress meaning.

No production publication source, new continuity/binding authority, permanent
custodian/approver/actor, mutation privilege, API, persistence, infrastructure,
identity allocator, release orchestrator or deployment is selected.
Frozen authority ownership and all production-reserved decisions remain intact.

The founder has approved the exact three-sentence finite policy and
conditional completeness, the exact classification mapping, and the synthetic
schema, bounds and provenance rules. The approved policy revision is obtained
from this authorized controlled promotion as specified in §7. Pinning that
actual commit remains an effectiveness prerequisite for subsequent EIP
implementation, which requires separate authorization. No other substantive
policy change is authorized.

## 13. Verified drafting baselines and change boundary

All five roots were checked on `main`; HEAD, local `origin/main` and live
remote `main` matched the following before drafting. Tracked worktrees were
clean; indexes were empty. EIP, Trusted, Assessment Service and Website had
no untracked files. Platform had only the protected document below.

| Repository | Starting commit |
| --- | --- |
| Platform | `91ea84e8b0c99b3e9c3d0f3f400fd9a8b96bb994` |
| EIP | `6a9bbae85d6b7fdd3514fe5d75b078872cb00d72` |
| Trusted | `62e0c4ae0b4c344d1bb954089499deee6df41f47` |
| Assessment Service | `9d544e4864b418478cf67f99726dde6cb4a63cad` |
| Website | `52b3a5b4e44d9769f01338fbc5dc74b64fe450d0` |

Protected Platform file:
`docs/platform/cep-principal-mapping-nonproduction-source-read-contract-v1.md`.
Verified SHA-256:
`14884bc189ae8a43c9e1583bd04b224f75265e8f394ccd9ac64bb222d83eb2b0`.
It remains protected and outside this change.

The 2026-11-13 promotion verification confirmed these same five main-branch
baselines against local HEAD, local origin/main and live remote main. All
tracked worktrees were clean and indexes empty. Platform had exactly this
proposal and the protected document untracked; the four reference repositories
had no untracked files. The protected SHA-256 matched the value above.

Only this existing proposal is authorized for approval-status correction,
the §7 policy-revision clarification, and controlled staging, commit and push.
No other document or implementation file is authorized for change. No tag,
deployment or client release is authorized. Static contract review does not
constitute runtime testing; no runtime implementation tests are required or
claimed for this policy-only promotion.

## 14. Founder decision — approved with policy-revision clarification

**Approval date:** 2026-11-13

**Approving authority:** Nguyen AI Enterprise LLC Founder/Owner

**Decision:** APPROVED WITH POLICY-REVISION CLARIFICATION

The founder explicitly approves Decisions A, B and C below as one bounded
synthetic metadata policy package. The decision descriptions, evidence and
alternatives presented for review are preserved below; their approval
requirements are satisfied by this explicit record. The sole clarification
is the immutable Platform policy-revision pin defined in §7.

| Proposed decision | Reason and supporting evidence | Material alternative | Consequence / explicit approval needed |
| --- | --- | --- | --- |
| A. Adopt the exact §4 wording, two mandatory statements and one rule-bound no-findings caveat, with complete ordered equality and no fallback. | v3 narrow content scope and non-release boundary; producer-approved no-findings interpretation. Closes the missing content/applicability decision. | Defer, or supply different exact supported wording and applicability in this same package. | Explicit founder approval of wording and completeness for this synthetic profile. No downstream inference of approval. |
| B. Adopt §5 response/field mapping: assessment content and limitations restricted; version/empty references operational; all listed internal/prohibited fields excluded. | Existing EIP classification concepts plus v3 allowlist/exclusions. Separates disclosure metadata from producer classification. | Defer or revise the exact mapping without expanding content eligibility. | Explicit founder approval of exact mapping and exclusion rules; no Principal access granted. |
| C. Adopt §§6–11 version/schema, provenance pin, exact instance/publication binding, independent verification, bounds and content-free DENY. | Existing artifact, publication, continuity and binding contracts/interfaces already carry the required facts. | Defer; do not create a partial interface or copy v2 metadata. | Explicit founder approval of this synthetic contract only. Controlled promotion and EIP implementation each require separate authorization. |

**Founder decision:** A (§4), B (§5), and C (§§6–11) APPROVED WITH
POLICY-REVISION CLARIFICATION. Approval covers the exact limitation statements,
deterministic applicability, ordering, completeness and fail-closed rejection;
the exact EIP field classification mapping and disclosure exclusions; and
the metadata contract version, schema, provenance, validation, artifact/
publication binding, independent source checks and content-free DENY.

**Next bounded action:** prepare the bounded Stage 4H.9B EIP implementation
using the exact promoted Platform commit as its independently pinned policy
authority. Do not implement Stage 4H.9B under this authorization.

## 15. No-release statement and disposition

Successful future metadata verification remains trusted-internal,
synthetic-only and `release_eligible=False`. It establishes no production
authority, standing authorization, live publication, Website integration,
deployment permission or client release. No client receives a synthetic
explanation under this proposal.

- Stage 4H.9C: FOUNDER APPROVED; PROMOTED / CLOSED upon successful controlled promotion.
- Stage 4H.9B: UNBLOCKED FOR SEPARATELY AUTHORIZED EIP IMPLEMENTATION upon promotion.
- Stage 4H.9A: BLOCKED PENDING PROMOTED EIP METADATA IMPLEMENTATION.
- Stage 4H.8: PROMOTED / CLOSED.
- Roadmap Stage 4: IN PROGRESS.
- Roadmap Stage 5: NOT STARTED.
