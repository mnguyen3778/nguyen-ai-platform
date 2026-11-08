# CEP v3 Serialized Artifact-Instance Identity Contract Decision v1

**Stage:** 4H.8B

**Decision:** FOUNDER APPROVED — MINIMUM SYNTHETIC ARTIFACT IDENTITY CONTRACT

**Approval date:** 2026-11-08

**Implementation:** NOT AUTHORIZED

**Git promotion:** SEPARATELY AUTHORIZED ONLY; completion is verified through
Git history. This document makes no claim that promotion has occurred.

## 1. Purpose and inherited boundaries

The founder approves a deterministic, nonproduction representation and identity
contract for one internal EIP v3 recommendation-action delivery artifact. It
unblocks a separately authorized synthetic Stage 4H.8A implementation; it does
not create an artifact, publisher, EIP Publication Register, current approval,
Resource binding, client response, or release eligibility.

This decision is subordinate to the [EIP artifact instance and revision identity
governance](eip-artifact-instance-revision-identity-governance-v1.md), the
[three-register logical authority-source decision](cep-v3-publication-binding-continuity-logical-authority-source-decision-v1.md),
the [publication evidence and freshness contract](cep-v3-publication-authority-evidence-freshness-contract-decision-v1.md),
the [Resource-to-Artifact Binding Authority governance](executive-dashboard-resource-artifact-binding-authority-governance-v1.md),
the [Assessment Instance Snapshot Continuity Authority governance](assessment-instance-snapshot-continuity-authority-governance-v1.md),
the [limited v3 action-text eligibility decision](cep-v3-recommendation-action-explain-eligibility-decision-v1.md),
and the [v3 EXPLAIN delivery specification](cep-v3-recommendation-action-explain-delivery-contract-proposal-v1.md).
Assessment Service retains immutable producer truth and attestation. EIP owns
the delivery artifact and its identity. The three logical authority sources,
principal authorization, and client release remain independent.

## 2. Approved synthetic artifact-instance model

1. EIP assigns one stable, immutable artifact-instance identifier before
   serializing an instance. It is assigned independently of the digest and is
   not computed from producer snapshot identity, recommendation text, a
   publication occurrence, or a publication revision. The synthetic fixture
   supplies the identifier; this decision chooses no production allocator or
   identifier format.
2. One identifier binds to exactly one finalized serialized byte sequence,
   supported delivery and serialization versions, verified producer lineage,
   and EIP artifact scope. A conflicting identifier-to-content or scope claim
   fails closed. No instance can silently change its bound bytes.
3. A separately verified integrity reference covers the exact finalized
   envelope bytes under section 4. The digest checks bytes; it is not the
   artifact-instance identifier, a publication decision, or a currentness
   signal.
4. Distinct artifact instances may have identical ordered recommendation
   **content**. Because this profile includes the instance identifier in the
   envelope, distinct identifiers make the complete envelope bytes differ.
   Either instance may participate in a separately governed publication
   occurrence; equal content never merges instances or occurrences.
5. Publication occurrence and revision are separate identities. The same
   immutable artifact instance can be referenced by distinct publication
   occurrences only under separately governed publication evidence. A new
   occurrence does not automatically create a revision, and a new revision
   does not automatically supersede an old one. This decision does not settle
   production uniqueness, retry, series, or revision domains.

## 3. Exact trusted-internal envelope schema

The synthetic artifact is one JSON object with **exactly** these members.
Every named object below also has exactly its listed members. All members are
required. The table states a synthetic wire schema, not a production API or
client response.

| JSON path | Exact value and validation |
| --- | --- |
| `artifactInstanceId` | Nonempty EIP-assigned synthetic identifier string; immutable for this instance. |
| `artifactScope` | Object with exactly `businessEntityId`, `engagementId`, and `environmentId`. These are trusted EIP artifact-scope facts, not producer snapshot fields. |
| `artifactScope.businessEntityId` | Nonempty governed Business Entity reference string. |
| `artifactScope.environmentId` | Nonempty governed environment reference string. |
| `artifactScope.engagementId` | Nonempty string when Engagement applies; JSON `null` only when trusted scope evidence establishes that it does not apply. Unresolved applicability rejects. |
| `content` | Object with exactly `recommendations`. This object alone is the candidate client-safe content projection. |
| `content.recommendations` | Nonempty array, in the exact verified producer recommendation order. Each element is an object with exactly one string member, `recommendationActionText`; its value matches the complete producer-approved text character for character. No reordering, trimming, omission, or partial release. |
| `deliveryContractVersion` | Exactly `website-recommendation-action-explain-delivery-contract-v1`. |
| `fieldScope` | Array containing exactly one string: `recommendationActionText`. Trusted envelope metadata, not an extra recommendation value. |
| `producerLineage` | Object with exactly `producerSnapshotIdentity`, matching the identity from the same-gateway verified signed v3 snapshot. This is a reference, not a substitute for verification evidence. |
| `serializationProfileVersion` | Exactly `eip-synthetic-v3-artifact-json-v1`. Unsupported versions reject. |
| `versionContext` | Object with exactly `assessmentVersion`, `methodologyVersion`, `packageContractVersion`, `recommendationDecisionTableVersion`, and `snapshotResponseContractVersion`. Values are respectively `nguyen-ai-executive-assessment-v2`, `business-decision-methodology-v1`, `business-decision-package-v3`, `recommendation-decision-table-set-v1`, and `executive-runtime-response-v1`, each checked against the verified producer candidate. |

All identifiers are JSON strings; version values are the exact values stated
above. Synthetic scope and instance identifiers must be nonempty ASCII
strings without control characters or leading/trailing whitespace. The
producer snapshot identity must equal the verified gateway evidence. The
recommendation action text must be a valid Unicode scalar sequence and is
never normalized or coerced. The existing candidate's ordered content shape
remains `recommendations[]` with only `recommendationActionText` per entry.

`artifactInstanceId`, scope, version context, field scope, and producer lineage
are trusted-only envelope metadata. They must never be copied into the
client-safe projection or model context. The full future v3 delivery and
release contract still requires separately governed classification,
limitations, publication, binding, and authorization evidence. This minimal
synthetic identity envelope neither supplies nor bypasses those gates.

Publication occurrence, revision, approval, currentness generation, lifecycle
state, Resource binding, Principal identity, authorization, and the final
integrity digest are **not** envelope members. They remain in separately
governed trusted evidence. No envelope field asserts `releaseEligible` or
constitutes approval.

## 4. Deterministic synthetic byte profile and integrity

The `eip-synthetic-v3-artifact-json-v1` profile is defined as follows:

1. Validate the complete section 3 schema, exact types, allowed values,
   required fields, and Unicode before serialization. No implicit type
   coercion, unknown field, duplicate key, non-finite value, or numeric value
   is permitted anywhere in this minimum envelope. The sole permitted JSON
   `null` is `artifactScope.engagementId` under the stated applicability rule.
2. Serialize exactly one JSON value using UTF-8, with no byte-order mark,
   no leading or trailing bytes, and no insignificant whitespace. Object keys
   are the exact ASCII names in section 3 and are emitted in ascending ASCII
   lexicographic order at every nesting level. Array order is preserved.
   Separators are one comma `,` and one colon `:` with no spaces.
3. JSON strings use a fixed ASCII-escaped form, consistent with the existing
   EIP v2 serializer's `ensure_ascii=True` behavior: printable ASCII U+0020
   through U+007E is literal except quotation mark and backslash, which are
   `\"` and `\\`; slash is literal. Use `\b`, `\t`, `\n`, `\f`, and `\r` for
   U+0008, U+0009, U+000A, U+000C, and U+000D respectively. Other U+0000
   through U+001F values use lowercase `\u00xx`. U+007F through U+FFFF use
   lowercase `\uxxxx`; U+10000 through U+10FFFF use a pair of lowercase
   `\uxxxx` escapes for the UTF-16 high and low surrogates. An isolated
   surrogate is invalid. No Unicode normalization is performed, so different
   scalar sequences remain different byte sequences.
4. Parse verification input as strict UTF-8 JSON: reject invalid encoding,
   byte-order marks, duplicate keys at any depth, invalid Unicode or isolated
   surrogate escapes, missing or unknown fields, wrong types, unsupported
   versions, and numeric or non-finite values. Validate the exact schema,
   then reserialize by rules 1–3 and require byte-for-byte equality with the
   presented bytes. Alternative key order, escaping, or whitespace is not an
   equivalent artifact under this profile.
5. After final serialization, compute SHA-256 over **those exact bytes**. The
   synthetic integrity reference is the literal prefix `sha256:` followed by
   exactly 64 lowercase hexadecimal digits. Reject other algorithms, uppercase
   or malformed encoding, byte mismatch, and digest mismatch. Recompute the
   digest from the presented bytes during verification. The reference is held
   in separately bound trusted evidence, never embedded in the bytes it
   hashes. It does not prove source authenticity, publication approval, or
   currentness by itself.

The artifact-instance identifier is assigned before rule 2; the digest is
computed after rule 2. The identifier is inside the envelope; the digest is
outside it. There is no circular hash dependency. This SHA-256 profile is
approved for the bounded synthetic proof only. Production digest profile,
identifier allocation, storage, and retrieval remain separate decisions.

## 5. Producer lineage, scope, and authority separation

The envelope's snapshot reference must match a freshly same-gateway-verified
signed `business-decision-package-v3` snapshot and its trusted internal
verification evidence. The gateway must verify exact bytes, signature,
attestation profile, producer snapshot identity, package and methodology
versions, producer recommendation order and text, and applicable decision-table
version. The trusted artifact-instance binding must retain that evidence and
the exact EIP delivery version, scope, and digest. A caller's envelope claims
cannot establish Business Entity, environment, or Engagement authority; those
must match separately held trusted synthetic scope evidence. Producer lineage
alone does not establish which customer assessment instance produced the
snapshot; the independent Continuity Authority owns that association.

These propositions remain distinct:

| Proposition | Owner and required evidence |
| --- | --- |
| Producer snapshot authenticity | Assessment Service signed bytes; EIP same-gateway verification consumes them. |
| Artifact-instance identity | EIP immutable identifier bound to exact envelope bytes, version, lineage, and scope. |
| Serialized-byte integrity | Recomputed SHA-256 reference for those exact bytes. |
| Publication occurrence and revision | Separate EIP publication identity and lifecycle evidence. |
| EIP publication approval and currentness | Separate EIP Publication Register decision and fresh effective-state evidence. |
| Assessment-instance continuity | Separate Continuity Authority association. |
| Resource-to-Artifact current selection | Separate Binding Authority evidence for one exact Resource and artifact instance. |
| Principal `EXECUTIVE_DASHBOARD × EXPLAIN` authorization | Separate fresh Trusted Authorization decision and explicit v3 field-scope admission. |
| Client-facing release | Separately governed release checks; this synthetic artifact remains non-releasable. |

No artifact identifier, digest, producer signature, synthetic PASS, historical
publication record, or binding record can substitute for another proposition.
The approved EIP Publication Register, Continuity Authority Instance Bridge
Register, and Binding Authority Current-Selection Register remain logically
independent. The existing v2 Dashboard contract is unchanged.

## 6. Interfaces for separately authorized synthetic implementation

An EIP Stage 4H.8A update must replace the current internal-projection-hash
substitute in `verify_synthetic_v3_publication` with comparison of the exact
artifact-instance identifier, canonical serialized bytes, recomputed digest,
verified producer lineage, delivery and serialization versions, approved field
scope, selected publication occurrence and revision, synthetic authority
generation, and effective lifecycle state. The synthetic publication fixture
must bind the identifier to exactly one complete artifact claim in its scope;
missing, duplicate, or conflicting claims reject. It must retain
`release_eligible=False`, return no client-facing payload, and issue no actual
publication approval. The existing Stage 4H.6D digest of the internal
projection remains internal test evidence only.

A later Trusted synthetic v3 binding check must require the exact governed
Dashboard Resource, Business Entity, environment, applicable Engagement and
workspace, exact artifact-instance identifier and digest reference, selected
publication occurrence and revision, and its **independent** binding generation,
current lifecycle state, and trusted source evidence. It must independently
establish one current Resource selection and verify EIP publication evidence;
publication does not create a binding. Client and workspace applicability
remain governed by the Resource scope. This decision does not implement the
Trusted validator or grant principal access.

## 7. Fail-closed verification requirements

Synthetic verification rejects absent, duplicate, conflicting, or mismatched
artifact-instance identity; changed bytes or digest; unsupported digest or
serialization version; wrong delivery or producer version; wrong verified
producer lineage; wrong Business Entity, environment, or applicable Engagement;
reordered, missing, or altered recommendation text; unknown envelope or
recommendation fields; duplicate JSON keys; invalid Unicode; missing required
fields; wrong types; ambiguous encoding; and unapproved client-visible
metadata. It rejects any attempt to use publication occurrence, revision,
producer snapshot identity, or the internal projection digest as the artifact
instance identifier or as proof of serialized integrity. Publication and
binding checks also reject substituted occurrence or revision, stale or
conflicting generation, withdrawn, superseded, revoked, invalidated, missing,
or unavailable authority, with no fallback to an older artifact or version.
An accepted synthetic identity check never changes `release_eligible=False`
or releases action text to a client.

## 8. Reserved decisions and disposition

This decision does not select production identifier format or uniqueness
domain, allocation authority details, artifact custody or durable storage,
publication approver or mutation/revocation actors, production authority
generation or freshness window, trusted production retrieval, API endpoints,
Cognito integration, production Trusted Authorization, release orchestration,
infrastructure, deployment, or client-facing publication. It authorizes no
Stage 5, 6, or 7 implementation and no standing administrator role.

**Disposition:** Stage 4H.8B founder minimum synthetic contract decision
recorded. Stage 4H.8A remains blocked pending separately authorized identity
interface implementation; Stage 4H.8 remains blocked pending 4H.8A. Roadmap
Stage 4 remains in progress; Stage 5 has not started.
