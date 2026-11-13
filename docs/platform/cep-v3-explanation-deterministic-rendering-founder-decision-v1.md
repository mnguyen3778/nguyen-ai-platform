# CEP v3 Explanation Deterministic Rendering Founder Decision v1

**Status: FOUNDER APPROVED — SYNTHETIC v3 RENDERING POLICY**

**Stage:** 4H.9A-R

**Decision date:** 2026-11-13

**Decision authority:** Nguyen AI founder/owner.

**Decision:** APPROVED.

**Decision scope:** Synthetic v3 nonproduction Dashboard recommendation-action
EXPLAIN rendering only.

**Decision document path:**
`docs/platform/cep-v3-explanation-deterministic-rendering-founder-decision-v1.md`.

## 1. Bounded decision and governing authority

The founder explicitly approved the deterministic v3 rendering rule recorded
below on November 13, 2026. This document records and promotes that decision;
it supplies only the missing Stage 4H.9A rendering authorization. It does not
authorize implementation. No frozen metadata, authorization, publication,
continuity, binding, artifact-identity, or scoring decision is reopened.

| Existing governing document | Exact applicable clauses and preserved boundary |
| --- | --- |
| [v3 recommendation-action explanation delivery contract](cep-v3-recommendation-action-explain-delivery-contract-proposal-v1.md) | §§5–7 require exact verified producer text and order, approved fixed rendering patterns, the four-field response, bounds, and trusted-only validation evidence. §§8–10 preserve independent publication, binding, fresh EXPLAIN authority, and exact DENY. |
| [v3 explanation metadata content/schema founder decision](cep-v3-explanation-metadata-content-schema-founder-decision-proposal-v1.md) | §2 expressly does not approve rendering patterns. §§4–7 govern complete ordered limitations, classifications, exact metadata schema and the independent policy pin. §§8–10 preserve instance/publication binding, independent currentness checks and content-free DENY. §12 excludes rendering-pattern approval from that metadata decision. |
| [v3 recommendation-action eligibility decision](cep-v3-recommendation-action-explain-eligibility-decision-v1.md) | §§4–7 limit eligibility to exact signed producer rule-bound action text, complete records, order, linkage and no-findings semantics; eligibility grants neither publication nor principal access. |
| [Nonproduction Dashboard EXPLAIN contract](cep-nonproduction-dashboard-explain-contract-v1.md) | §§4–7 govern bounded questions/context/output, approved deterministic patterns, complete limitations, fresh authorization, source checks, audit and content-free DENY. The separately versioned v3 response remains isolated from legacy v2 behavior. |

The new approved fixed pattern is exact eligible text, with only the separator
in Rule B between multiple texts. It adds no sentence wording or business
interpretation. Historical milestone statements in existing documents retain
their historical scope; this decision does not modify those documents or
claim that any production or client release gate has passed.

## 2. Founder-approved rendering rules

### Rule A — finding-scoped content

Render every eligible verified `recommendationActionText` exactly as supplied
by the signed producer.

Preserve character-for-character content and original producer order.

Do not paraphrase, summarize, rewrite, translate, normalize, or selectively
omit action text.

### Rule B — multiple action texts

Join the complete ordered action texts using exactly two newline characters:

```json
"\n\n"
```

These are two U+000A line feeds. The JSON notation above denotes those two
characters; literal backslash-and-letter sequences are not the separator.

Do not insert headings, bullets, numbering, introductory sentences, closing
sentences, prefixes, suffixes, or extra whitespace.

Do not insert a leading or trailing separator.

For a single action text, render that text unchanged.

### Rule C — producer-defined no-findings

For the independently verified producer-defined no-findings case, render the
single eligible `recommendationActionText` unchanged. No prefix or suffix.

Do not invent a statement that the assessment proves absence of risk or
guarantees compliance.

The approved conditional no-findings limitation remains mandatory. Its
applicability follows the existing metadata policy §4: fresh producer
verification must establish the sole complete no-findings record, rule
`recommendation-v1-no-findings-monitor`, `findingId=null`, class `monitor`,
exact mapped text and no-findings completeness. These are trusted-internal
validation facts; this decision does not disclose them in the response.

### Rule D — complete content

Render the complete eligible recommendation set in exact producer order.

Do not omit, truncate, reorder, deduplicate, or substitute actions.

Reject malformed, missing, empty, unsupported, or incomplete content.

Reject unsupported mixtures of finding-scoped and producer-defined
no-findings records.

Do not infer the no-findings case from natural-language action text. Use
verified producer identity and linkage under existing policy.

### Rule E — response bounds

Apply all existing approved question, context, fact, reference, and response
limits. The inherited limits are:

- Exactly one current question: 1–500 Unicode characters and at most 2,000
  UTF-8 bytes, under the existing question rules.
- At most 64 admitted facts and 16,384 UTF-8 context bytes.
- At most 1,200 response characters, 4,800 response UTF-8 bytes and 12 fact
  references, under the existing response rules.

The complete rendered response, including all required limitations, must fit
the existing approved response bounds. No truncation is permitted.

If complete content exceeds an applicable bound: DENY.

### Rule F — fail-closed

Any rendering failure must produce exactly:

```json
{"decision":"DENY"}
```

No reason field. No partial explanation. No partial limitations. No fallback
to v2. No alternate action set. No LLM-generated replacement.

## 3. Preserved response contract

This decision does not change the approved four-field response allowlist:

| Response field | Exact preserved rule |
| --- | --- |
| `contractVersion` | Exactly `cep-nonproduction-dashboard-recommendation-action-explain-contract-v1`. |
| `explanation` | Only the deterministic rendering defined in this decision. |
| `limitations` | The complete ordered limitations verified under the existing approved EIP metadata policy; exact wording and deterministic conditional applicability remain unchanged. |
| `sourceReferences` | Exactly `[]`. |

No additional client fields, metadata envelope, internal classifications,
producer linkage fields, principal information, or authority-source details.
No raw internal object is serialized as the response. Only the approved
response fields may form an internal synthetic response candidate; this
decision authorizes no client delivery.

The two mandatory limitations and the conditional no-findings limitation are
preserved under metadata policy §4. Their exact approved text and order must
be verified; the renderer may neither invent nor repair them. A failure in
metadata, authorization or any other required gate remains exact DENY.

## 4. Preserved authority separation and lineage

| Authority / consumer | Preserved responsibility |
| --- | --- |
| Assessment Service | Signed producer recommendation truth. |
| EIP | Artifact identity, publication, approved metadata and limitations. |
| Continuity Authority | Assessment-instance to producer-snapshot association. |
| Binding Authority | Resource to selected artifact. |
| Trusted Authorization | Principal EXPLAIN authority, revocation, audit and currentness. |
| Website | Presentation consumer only. |
| AI Knowledge Assistant | Explanatory consumer only. |

The renderer must not become a scoring, selection, publication,
authorization, or policy authority. It consumes the exact already selected
and verified synthetic content. Immutable evidence, complete lineage,
versioned contract boundaries and independent authority checks remain intact.
Artifact-instance identity remains distinct from digest; publication
occurrence and revision remain separate. This decision creates no standing
authorization and changes no existing principal or source verifier.

## 5. Independent immutable policy revisions

The previously approved EIP metadata policy remains pinned to this full
Platform commit SHA:

`2a40b70af64bcd53a8eab1ef32b3ce3d445eb3a0`

Do not replace that metadata pin with this new rendering promotion commit.
The metadata schema's existing `policy_revision` continues to identify the
metadata policy; this decision adds no metadata schema field.

This rendering decision has its own independent Platform promotion revision:
the full 40-character Git commit SHA of the Platform main commit that
promotes the decision document identified above. Obtain and report that SHA
after committing. Do not embed that future SHA in its own tracked document;
doing so creates a circular commit-hash dependency. Do not amend or create a
second commit merely to insert the SHA.

Future Trusted implementation must independently pin both the existing
metadata policy revision and this newly promoted rendering policy revision.
Do not auto-advance either pin. Subsequent implementation commits, tests or
unrelated repository revisions do not replace either authority pin.
Presented content cannot select or authorize its own policy revision.
Commit presence alone does not establish founder approval; this document's
explicit founder decision is the rendering approval record.

## 6. Nonproduction restrictions and implementation boundary

This decision authorizes only a deterministic rendering pattern. It does not
authorize client release, Website integration, production deployment, live
authority integration, persistent storage, new authentication, new
authorization rules, new scoring, new recommendation generation, new EIP
metadata schema, new client response fields, or LLM-generated business
conclusions.

Synthetic verification remains nonproduction and internal.
`release_eligible=False` remains mandatory wherever applicable. This policy
does not turn an internal synthetic success into a release permission.

Only this new Platform governance document is authorized for creation and
controlled promotion. No implementation code or reference repository is
changed. Static document, contract, link and Git verification are not runtime
tests; this policy-only promotion claims no runtime test result.

## 7. Disposition and next bounded action

Upon successful controlled promotion:

- Stage 4H.9A-R: FOUNDER APPROVED / PROMOTED / CLOSED.
- Stage 4H.9A: UNBLOCKED FOR SEPARATELY AUTHORIZED IMPLEMENTATION.
- Stage 4H.9B: PROMOTED / CLOSED.
- Stage 4H.9C: PROMOTED / CLOSED.
- Roadmap Stage 4: IN PROGRESS.
- Roadmap Stage 5: NOT STARTED.

Next bounded action: resume Stage 4H.9A Trusted synthetic explanation adapter
implementation using existing Trusted admission, the promoted EIP metadata
verifier, the existing immutable metadata policy revision, this new immutable
rendering revision, fresh principal EXPLAIN proof, fresh audit/currentness,
and fresh publication, continuity and binding evidence. Preserve the exact
four-field response, complete limitations and content-free DENY.

Implementation requires separate authorization and is not performed under
this decision's promotion authorization.
