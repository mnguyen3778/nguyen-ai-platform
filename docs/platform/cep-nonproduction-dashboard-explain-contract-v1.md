# CEP Nonproduction Dashboard EXPLAIN Contract v1

Version: `cep-nonproduction-dashboard-explain-contract-v1`

Status: bounded contract for a future local synthetic nonproduction proof.
No implementation, production authority, permission grant, or deployment is
approved by this document.

## 1. Purpose and governed boundaries

This contract governs a future AI Knowledge Assistant explanation of one
already authorized, current Executive Dashboard projection for one exact
governed Dashboard Resource R. The explanation may restate and connect
admitted, approved facts to help a Principal understand the Dashboard. It is
not a new assessment, projection, decision, entitlement, or source of business
truth.

The [Resource/Action Applicability Governance v1](resource-action-applicability-governance-v1.md)
already defines `EXECUTIVE_DASHBOARD × EXPLAIN = APPLICABLE`. `VIEW` does not
imply `EXPLAIN`, and `EXPLAIN` does not imply `VIEW`. Applicability does not
establish an exact-resource Entitlement, Trusted Authorization `ALLOW`, or
release. The [Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md)
preserves independent Principal access, EIP publication eligibility, lineage,
currentness, audit, and denial privacy. This contract does not amend either
governing artifact or the existing applicability matrix.

The Assessment Service remains the sole deterministic assessment-truth
authority. EIP remains the producer of governed Executive Dashboard
projections and their Website-facing delivery contract. Trusted Authorization
remains the exact-resource access authority. The AI Knowledge Assistant is an
explanatory consumer only. The Website is a presentation consumer only; it
must not independently authorize, recalculate, or manufacture explanations.

## 2. Exact identity and authorization

Before the Assistant may receive protected context, a trusted server-side
boundary must verify the Principal and current Principal Mapping; resolve the
exact current `EXECUTIVE_DASHBOARD` R; verify its exact Assessment Engagement
E and authoritative E-to-Business-Entity B binding; current applicable
Membership; an independent, current Entitlement for this Principal and exact
R/`EXPLAIN`; `EXPLAIN` applicability under the governed version; revocation
state; EIP source provenance, projection revision and currentness; and valid
authorization and source audit/custody evidence. The existing evaluator must
produce a fresh `ALLOW` for exact R/`EXPLAIN` before protected context is
admitted. A prior Dashboard `VIEW` `ALLOW`, a dashboard route, authentication
alone, a browser-selected E/B/R, or a model instruction cannot establish any
of these facts.

Resource identity, E/B binding, projection identity, publication occurrence,
revision, source lineage, and authorization decision remain distinct.
Unknown, duplicate, conflicting, cross-B, stale, revoked, incompatible, or
unavailable required evidence fails closed. Same-B substitution of a different
E or Dashboard R also fails. No browser payload, conversation history, model
output, or caller assertion may create authority or change the selected
Resource.

## 3. Admitted governed input

The only protected explanatory input is the exact, verified, current,
authorized Website-facing Executive Dashboard projection for R, obtained
through the existing EIP governed delivery and Resource/artifact binding
checks. The trusted boundary must verify supported delivery and publication
versions, approved classification and limitations, complete lineage, current
publication revision, and equality of the released projection with the
authorized R/E/B scope. The model receives only a bounded allowlist of
display-safe facts from that verified delivery, never a raw EIP package or
Assessment Service object.

Permitted subjects, only when actually present in approved delivery fields,
are the executive summary, governed findings, existing risk classification,
existing confidence classification, governed recommendation
classifications, limitations, and approved client-safe source references.
Business capability results, decision priorities, numerical scores, or
source references absent from the admitted fields are unavailable to this
contract. The Assistant must not infer them from a label, question, model
knowledge, or another Dashboard.

Raw assessment answers and truth objects, internal scoring, source evidence,
authority records, Principal Mapping, Membership, Entitlement, audit/custody
internals, credentials, secrets, and cross-tenant context are excluded from
the model input and client response. Internal source lineage may be used by
trusted validators but must not be copied into model context or Website props.

## 4. Bounded question and model use

V1 accepts exactly one current user question per request, with no prior
messages or memory. The normalized question must contain 1–500 Unicode
characters and at most 2,000 UTF-8 bytes. The admitted display-safe context
is limited to 64 facts and 16,384 UTF-8 bytes; if a complete required fact or
limitation set exceeds the bound, the request fails closed without silent
truncation. Model output is limited to one candidate, 1,200 Unicode
characters, at most 4,800 UTF-8 bytes, and at most 12 fact references. These
are contract limits for future deterministic enforcement, not claims about
current runtime behavior.

The question may ask for an explanation of the admitted Dashboard subjects.
It may not request new assessment calculations; new risk or confidence
classifications; invented findings or recommendations; unsupported priority;
Assessment Progress calculations; protected `REPORT` access; raw assessment
disclosure; cross-tenant facts; or comparison with another resource lacking
separate exact-resource authorization and an approved comparison contract.
The trusted boundary classifies scope before model invocation. An unsupported
but otherwise authorized question receives the refusal in §6. Prompt
injection and instructions to ignore rules, disclose hidden context, alter
authority, or select another resource have no effect and must not expand
admitted context.

A future implementation may inject a local model stub for deterministic
nonproduction tests. AWS Bedrock invocation is not required. Model output is
always untrusted candidate data; neither provider selection nor text content
can select a protected operation, override Trusted Authorization, change EIP
eligibility, or become an authoritative business decision.

## 5. Deterministic grounding validation

For this first bounded implementation, the trusted boundary creates a finite
fact registry from admitted display-safe fields. Each fact has a server-held
fact key, exact source field and value, source section, approved client-safe
reference if any, and applicable limitation. The model may propose only
structured selections of those fact keys and approved explanation sentence
patterns. It may not supply releasable free-form prose, new values, or
unverified citations. A deterministic renderer assembles the released text
from the selected patterns and exact admitted values.

The validator must reject the whole candidate unless every selected key
exists for this exact projection revision; the pattern is approved for the
fact type; each rendered assertion has direct support in the admitted value;
all required limitations are carried forward; references are approved for
client display; the question and response remain in scope and within bounds;
and no extra fields, unsupported risk/confidence value, new priority,
cross-resource claim, or model-authored instruction remains. Pattern matching
and exact value comparison are deterministic. A model assertion that cannot
be proven by these checks is rejected, never silently accepted or rewritten
into apparent fact. Rejection fails closed; it does not ask the model to
invent a repair. No general free-text semantic validator is assumed.

## 6. Client-safe response and refusal

After every release gate passes, the successful response has exactly these
fields:

```json
{
  "contractVersion": "cep-nonproduction-dashboard-explain-contract-v1",
  "explanation": "<deterministically rendered approved text>",
  "sourceReferences": ["<approved client-safe reference>"],
  "limitations": ["<applicable approved limitation>"]
}
```

`sourceReferences` may be empty when grounding is retained server-side but
no reference is approved for client display; it may never contain internal
lineage or an invented citation. `limitations` includes every applicable
client-safe limitation required for the selected facts. No Principal,
Engagement or Business Entity identifier, raw delivery payload, authority
record, audit evidence, source revision, or decision hash is returned.

An unsupported question from an otherwise authorized Principal, with valid
current evidence, receives exactly:

```json
{
  "contractVersion": "cep-nonproduction-dashboard-explain-contract-v1",
  "refusal": "This question is outside the available dashboard explanation scope."
}
```

The refusal is not a business conclusion and contains no protected fact,
source reference, or reason that reveals another resource. Authorization or
required-evidence failure instead returns exactly `{"decision":"DENY"}`.
`DENY` releases zero protected Dashboard or explanation fields, with no
partial, cached, default, or model-generated fallback. Trusted internal
handling may distinguish failure causes; the caller-visible DENY remains
content-free and does not disclose resource existence.

## 7. Release order and audit

The future adapter must perform these gates in order: (1) initial fresh
exact-R/`EXPLAIN` authorization and audit validation; (2) governed projection,
publication, Resource binding, lineage, revision, and currentness
verification; (3) bounded question and context validation; (4) model or local
stub invocation only for a supported question; (5) deterministic candidate
validation and rendering; (6) fresh exact-R/`EXPLAIN` authorization; (7) fresh
source, publication, revision, binding, revocation, and currentness checks;
(8) final audit/custody validation; and (9) release or exact DENY. An
authorized unsupported question follows the same fresh checks before the
fixed refusal is returned. Any failed required gate yields exact DENY and
zero protected fields. A prior `ALLOW` or projection snapshot cannot be
reused as current release authority.

Server-side audit must correlate request and contract version, verified
Principal reference, exact R/`EXPLAIN`, E/B binding, projection and
publication revisions, source lineage reference, initial and final evaluator
decisions, scope and output-validation outcomes, revocation checks, and final
release or denial. Audit and custody internals remain server-side; no raw
question, model prompt, protected fact values, secret, or unnecessary report
content belongs in audit logs. This contract selects no audit persistence
technology.

## 8. Preserved capabilities and implementation dependencies

The committed [Assessment Progress Read Contract v1](cep-assessment-progress-read-contract-v1.md)
keeps Assessment Progress **DEFERRED**. The committed
[Governed Assessment Report VIEW Contract v1](cep-governed-assessment-report-view-contract-v1.md)
does not authorize this Dashboard explanation to view or release a Report.
Existing Stage 3 synthetic report evidence has `release_eligible=False` and
the governed report delivery result remains exactly `{"decision":"DENY"}`.
Neither this contract nor Dashboard `EXPLAIN` changes those gates.

The proposed future implementation belongs in `aws-ai-knowledge-assistant`:
`src/trusted_authentication/non_production_dashboard_explanation.py`, with
focused tests in `tests/test_non_production_dashboard_explanation.py`.
The current protected-operation catalog defers assistant access to governed
content. Before a runnable adapter, a separately authorized application
operation selection must identify Dashboard `EXPLAIN` independently of the
route, provider, prompt, or model output; this contract does not create that
mapping or modify the evaluator. Separate implementation authorization is
required. The tests must cover an
authorized explanation; missing exact-R `EXPLAIN` Entitlement; `VIEW`-only
access; revoked Membership; invalid Principal Mapping; cross-tenant and wrong
Dashboard Resource; stale projection and invalid lineage; unsupported
question; prompt injection; invented model facts; unsupported risk or
confidence; invented recommendation priority; Report disclosure and
Assessment Progress requests; failed fresh authorization; exact DENY with
zero protected fields; and existing CEP regressions.

This is a local synthetic nonproduction target. It creates no production
Principal Mapping, source authority, model deployment, Website feature,
report release, AWS integration, or production permission. Assessment Service
truth, EIP projection production, Trusted Authorization evaluation, and
Website presentation remain in their owning repositories.
