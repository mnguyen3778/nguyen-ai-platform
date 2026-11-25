# Stage 5 application-governed submission enforcement boundary v1

## 1. Decision and scope

The Founder approves Option B for bounded Stage 5 nonproduction development. Future submission must enforce application-governed authority through the durable transition and obtain required point-in-time Cognito authentication evidence. This amendment defines the contract. Implementation and operational acceptance require separate approval.

## 2. Superseded strict requirement

For this nonproduction scope, this amendment supersedes the requirement to order every independently effective Cognito revocation against the durable submission commit. The earlier exact-session ownership decision and companion submission-time contract remain the historical baseline. Their requirements for ownership, exact identity, same-composition custody, fail-closed behavior, and application-controlled ordering continue to apply. The Platform lifecycle contract continues to govern the transition, commit verification, recovery, and completion evidence. [Exact-session ownership decision](cep-stage5-exact-session-revocation-authority-ownership-decision-v1.md#7-revocation-ordering-requirements) · [Companion submission-time contract](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-submission-time-currentness-mutation-boundary-v1.md#L31) · [Platform lifecycle contract](cep-stage5i-nonproduction-effective-submission-lifecycle-mutation-ownership-contract-v1.md#17-authorization-currentness)

## 3. Preserved ownership boundaries

| Owner | Responsibility |
|---|---|
| Authentication Verification Owner | Authentication provenance, exact-session identity, and approved session-currentness evidence. |
| Amazon Cognito | External identity and authentication provider under its documented service guarantees. |
| TrustedAuthorizationEvaluator | Sole ALLOW/DENY authority. |
| Assessment Service | Canonical Assessment Attempt lifecycle authority. |
| Assessment Submission Post-ALLOW Eligibility Authority | Fresh eligibility and its private same-composition lineage handoff. |
| Assessment Submission Resource Lifecycle Authority | Durable submission transition, commit verification, recovery, and custody of lifecycle evidence. |
| Trusted Authorization and governed source owners | Trusted Authorization consumes governed evidence. Each source owner remains authoritative for its own state and mutations. |
| Website | Presentation and authorized request delivery. |

[Authentication governance](trusted-authorization-authentication-trust-provenance-governance-v1.md#authentication-verification-owner) · [Submission-time owner roles](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-submission-time-currentness-mutation-boundary-v1.md#L9)

## 4. Guarantee A — Application-governed authority

The future commit protocol must order every applicable application-controlled change that affects submission eligibility against the durable transition. This covers the nine existing governed sources and any application-owned session or submission revocation state separately approved for implementation. A disqualifying change committed first must prevent a later submission. A submission committed first must have satisfied all applicable authority checks through durability. Subsequent revocation leaves that committed record intact and applies to later access. [Platform lifecycle revocation contract](cep-stage5i-nonproduction-effective-submission-lifecycle-mutation-ownership-contract-v1.md#18-revocation)

## 5. Guarantee B — Cognito authentication evidence

The application must verify the presented token and obtain required authoritative point-in-time evidence from the approved Cognito operation for the intended pool, app client, and presentation. The approved policy must specify what its response establishes for the exact token or session. Cognito remains the provider. Independent provider invalidation can take effect after the final successful check and before the durable commit. Guarantee B establishes only the approved point-in-time evidence. [Promoted provider capability boundary](cep-stage5-exact-session-revocation-authority-ownership-decision-v1.md#3-cognito-provider-capability-boundary)

## 6. Authentication evidence rules

- Pin the trusted issuer and intended app client. Verify the signature with trusted issuer keys, require the approved access-token type, enforce token expiry and the governed audience and age rules, and authenticate the signed subject. Resolve that subject through verified Principal Mapping. Preserve exact principal, Business Entity, Attempt, and resource binding for SUBMIT.
- Bind required exact-session evidence to the provider, issuer, app client, subject, and verified token presentation. `jti` identifies an individual JWT, `origin_jti` identifies refresh-token revocation lineage where applicable, and provider-issued `sid` identifies a tracked session where supported. Pool eligibility, provider issuance, claim provenance, and refresh and rotation continuity require verification. Missing required exact-session identity fails closed.
- Require an approved provider evidence source with explicit scope, provenance, timing, freshness and expiry. Verify the result against the same presentation and composition. Untrusted, substituted, invalid, or unavailable required evidence blocks submission. [Promoted exact-session binding](cep-stage5-exact-session-revocation-authority-ownership-decision-v1.md#5-exact-session-identity-requirements)

## 7. Provider-currentness policy

| Policy item | Requirement |
|---|---|
| When to check | Obtain the required provider evidence within the trusted submission composition before authorization completion. The final provider check must be fresh for that attempt, as close to the commit boundary as the approved sequence permits, and bound to the same presentation and scope. The implementation must specify the check's placement relative to reservations and final revalidation. |
| Maximum age and cache | Require a fresh provider operation for the final check. Previously cached positive currentness from another attempt cannot satisfy it. The maximum acceptable evidence age and validity cutoff within the attempt are G2 gates. Derive them from verified provider behavior and the actual submission timing budget. Until approved bounds exist, the provider predicate cannot pass. |
| Evidence semantics and consistency | Approve the exact operation, identity key, accepted response, read consistency, provenance, and evidence lifetime. An eventually consistent active-session list supplies only the observation its semantics support. Its presence or absence alone cannot establish authoritative exact-session revocation status. JWT verification and absence of a known revocation cannot satisfy a required provider currentness check. |
| Failure and timeout | Missing, stale, invalid, ambiguous, unsupported, timed-out, or unavailable required evidence blocks submission. There is no fallback to cached currentness or signature-only verification. Affirmative invalidation observed before authorization completion or later before commit prevents the transition. |
| Expiration | Enforce token expiration and any authoritative session expiration required by policy through the durable commit point, together with the approved evidence cutoff and application authority deadlines. A pre-commit clock check alone does not prove a late commit is impossible. Unavailable required expiry evidence fails closed. |
| Discovery after verified completion | Record the later discovery and observation time with protected audit custody. Preserve the committed transition. Require fresh authorization and provider evidence for subsequent protected operations or completion disclosure. Discovery after completion supplies no proof of when provider invalidation took effect relative to commit. |

The approved provider operation, its exact-session support, timing budget, maximum age and cutoff, and handling of provider consistency remain implementation gates. If the chosen operation cannot establish the evidence required by the approved policy, fail closed. [Prior provider findings](cep-stage5-exact-session-revocation-authority-ownership-decision-v1.md#3-cognito-provider-capability-boundary) · [Lifecycle currentness and disclosure](cep-stage5i-nonproduction-effective-submission-lifecycle-mutation-ownership-contract-v1.md#17-authorization-currentness)

## 8. Application ordering requirements

Preserve the verified acquisition order and reverse release for the nine source-owner reservations.

1. Assessment Attempt
2. SUBMIT Entitlement
3. Membership
4. Principal Mapping
5. Attempt Binding
6. Resource Identity
7. Business Entity
8. Engagement
9. Participation

The future protocol must specify where protected acquisition begins, who holds each reservation, how the lifecycle guard joins the same composition, and how any separately approved application-controlled revocation source participates. Within bounded waits, validate each authoritative record and revision or governed observation, the separately governed Attempt Binding, and the exact principal, tenant, resource, action, and lineage. Revalidate applicable authority with fresh evaluator-owned `ALLOW` and same-composition `ELIGIBLE` for a first transition.

Keep the necessary protections effective through commit or definite abort. Release them in reverse acquisition order on a definite outcome, and prove safe cleanup on failures and process loss. The commit guard must reject a disqualifying change that becomes effective first. Acquisition failure, timeout, cancellation, or uncertainty before commit must prevent starting the write. Cancellation or timeout during the write requires recovery if the outcome is uncertain. Preserve the earliest applicable deadline and verify that expiry prevents a late durable success. The current nine SQLite reservations overlap at a synthetic marker, and their verified classification remains `INCOMPLETE_COVERAGE`. [Nine-source verification](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-business-context-owner-backed-reservation-extension-v1-evidence.md#L19) · [Commit and deadline contract](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-submission-time-currentness-mutation-boundary-v1.md#L25)

## 9. Commit and recovery requirements

Only the lifecycle owner may commit the single `PROVISIONAL → SUBMITTED` transition. A known abort produces no completion claim. An indeterminate commit returns a bounded `UNAVAILABLE` result with empty evidence. The lifecycle owner must resolve the outcome through authoritative read-back before any retry. Verified absence permits a new attempt with fresh authority. A verified matching commit permits the governed duplicate result only under fresh authorization and exact identity. Preserve the original mutation identity and prohibit duplicate writes and blind replay.

Retain protected audit evidence for the exact composition, source owners and revisions or observations, provider evidence provenance and times, ordering and deadlines, mutation identity, and commit and read-back outcome. Keep token material and sensitive authority payloads out of caller-facing results. Affirmatively invalid authority yields the governed empty authorization failure. Missing, stale, or unavailable required authority yields `UNAVAILABLE` with empty evidence. Both withhold mutation and completion evidence. [Commit and recovery outcomes](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-submission-time-currentness-mutation-boundary-v1.md#L39) · [Lifecycle evidence custody](cep-stage5i-nonproduction-effective-submission-lifecycle-mutation-ownership-contract-v1.md#19-evidence-and-audit-custody)

## 10. Residual provider race

Independent Cognito revocation may take effect after the final provider check and before the durable submission commit. Applicable paths can include user and administrative revocation, global sign-out, refresh-token revocation, and automatic session eviction. Provider invalidation observed before authorization completes, or otherwise known before commit, must block the submission. An invalidation that is still unobserved in the check-to-commit window may coexist with a successful application-governed commit. Provider read consistency can also limit what the final observation establishes. [Promoted Cognito boundary](cep-stage5-exact-session-revocation-authority-ownership-decision-v1.md#3-cognito-provider-capability-boundary)

## 11. Nonproduction risk acceptance

The Founder accepts this residual provider risk solely for bounded Stage 5 nonproduction development. The risk remains material. Production acceptance requires a separate security review and explicit Founder approval.

## 12. Explicit nonclaims

This amendment establishes no universal Cognito revocation ordering, zero provider revocation lag, cross-source atomicity, or verified durability guarantee. The synthetic marker provides no operational ALLOW or submission write. This decision grants no authority to implement a session store, add infrastructure, change Cognito, deploy to AWS, or implement durable submission persistence.

## 13. Implementation acceptance gates

Each gate is open for the future submission implementation. Historical synthetic verification remains evidence for its existing scope.

| Gate | Acceptance evidence required |
|---|---|
| G1 | Verify the intended Cognito configuration and supported exact-session identity, including issuance and continuity where applicable. |
| G2 | Approve the provider currentness operation and evidence policy, timing, maximum age, consistency limits, expiry, and failure behavior. |
| G3 | Verify deterministic token, subject, exact-session, and principal binding with tenant and resource isolation. |
| G4 | Integrate the nine existing reservations with the actual lifecycle commit boundary, preserving acquisition, release, and same-composition behavior. |
| G5 | Demonstrate ordering for every applicable application-controlled authority change and revocation path. |
| G6 | Verify an enforceable guard through the single durable transition and authoritative read-back. |
| G7 | Enforce token, session, evidence, and application deadlines as applicable through durability, with safe timeout and cancellation behavior. |
| G8 | Verify crash cleanup and authoritative recovery after uncertain commit without duplicate writes. |
| G9 | Pass negative and deterministic concurrency tests using the approved integration and actual ordering mechanism. |
| G10 | Verify protected audit evidence and bounded fail-closed errors without disclosure of sensitive information. |

## 14. Adversarial verification requirements

| Scenario | Acceptance requirement |
|---|---|
| Application revocation before or during acquisition, after final validation, and concurrent with commit | Force both durable orderings for applicable sources. Revocation first blocks submission. A verified commit first leaves one durable transition. Test all nine source paths and any separately approved application revocation path. |
| Wrong issuer, app client, subject, principal, session, tenant, resource, Attempt or Binding | Reject substitution and replay before mutation or completion disclosure. Verify refresh and rotation continuity where applicable. |
| Provider outage, timeout, stale or ambiguous evidence, and observed revocation | Fail closed. Exercise affirmative invalidation before and after final revalidation but before commit when the application observes it. |
| Independent Cognito revocation after the final check | Exercise the residual window and verify that evidence and reporting reflect the point-in-time policy and its limits. Require fresh authority for later access. |
| Lock timeout, cancellation, deadline crossing, process loss, and indeterminate commit | Prove cleanup, no late commit, authoritative read-back, and at most one durable transition. Completion claims require verified outcomes. |

## 15. Fixed Stage 5 roadmap status

Stage 5 remains in progress. Package 1 remains operationally incomplete. Stages 6 and 7 have not started.

| Deliverable | Status |
|---|---|
| Joint Authorization Protection | In progress |
| Governed Submission Persistence | Pending |
| End-to-End Verification | Pending |
| Final Stage 5 Closeout | Pending |
