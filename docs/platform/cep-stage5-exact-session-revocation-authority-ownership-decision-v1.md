# Stage 5 exact-session revocation authority ownership decision v1

## 1. Purpose and Founder decision

**APPROVED OWNERSHIP.** The Founder designates the existing Authentication Verification Owner as accountable for establishing the application's exact-session revocation currentness and submission commit-ordering guarantee. Amazon Cognito remains the identity and authentication provider.

**UNVERIFIED IMPLEMENTATION.** The concrete session authority and ordering mechanism remain unresolved. **NOT AUTHORIZED.** This decision grants no implementation, AWS change, deployment, or Git promotion approval.

## 2. Existing promoted authority baseline

| Repository | Reviewed main commit |
|---|---|
| Platform | `76b0c658d23bd888698ea900ab78d835cb5f3c9c` |
| Trusted Authorization | `4e2e6661dfaefebd5e7feff02d4ea608b22ec860` |
| Assessment Service | `365317f5fcc45b926f87588141afefe93a03a571` |

The promoted coordinator holds Assessment Attempt, SUBMIT Entitlement, Membership, Principal Mapping, Attempt Binding, Resource Identity, Business Entity, Engagement, and Participation reservations through the same synthetic marker. Its supported result remains `INCOMPLETE_COVERAGE`. The synthetic interval provides no operational ALLOW, submission writer, durable submission mutation, or cross-source atomicity guarantee. [Nine-source verification evidence](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-business-context-owner-backed-reservation-extension-v1-evidence.md#L19) · [Coverage classifier](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/src/trusted_authorization/_non_production_joint_submission_reservation.py#L56)

## 3. Cognito provider capability boundary

When applicable user-pool session tracking is enabled, Cognito issues a token-session `sid` that persists across refresh and rotation within that session. Cognito documents exact-session revocation by session ID. Its session-list reads are eventually consistent, and its documented session operations provide no ordering guarantee against an external submission commit. A locally valid JWT can still have been revoked. [AWS session management](https://docs.aws.amazon.com/cognito/latest/developerguide/managing-user-sessions.html) · [AWS ListUserSessions](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_ListUserSessions.html) · [AWS AdminRevokeUserSession](https://docs.aws.amazon.com/cognito-user-identity-pools/latest/APIReference/API_AdminRevokeUserSession.html) · [AWS JWT verification](https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-verifying-a-jwt.html)

The existing verifier does not bind `sid` as an approved exact-session identity. Its successful JWT result records `revocation_currentness_established=False`. An approved application reader, writer, and commit-ordering mechanism remain unverified. [Cognito verifier and result](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/src/trusted_authentication/cognito_authentication_verification.py#L282)

## 4. Accountable logical owner

The Authentication Verification Owner must establish or obtain an approved mechanism that binds the authenticated presentation to the exact session, verifies authoritative revocation currentness, and supplies enforceable ordering evidence through the protected submission transition. The owner must account for every applicable independent revocation path that can take effect before commit, including provider-side paths outside application control. Cognito retains its provider role. [Authentication trust and provenance governance](trusted-authorization-authentication-trust-provenance-governance-v1.md#authentication-verification-owner)

## 5. Exact-session identity requirements

- Require a provider-controlled or otherwise authoritatively established identifier. Bind the provider, issuer, app client, subject, and exact session to the relevant verified token presentation.
- Document session continuity across refresh and rotation where applicable. Treat `jti` as an individual JWT identifier and `sid` as a provider session identifier only when its provenance and applicability are established. Keep principal and Business Entity scope checks intact.
- Reject missing, substituted, or mismatched session identity. The existing private reader's session lookup key binds provider, issuer, app client, subject, and session reference. The future mechanism must establish how the verified presentation supplies that reference. [AWS access-token claims](https://docs.aws.amazon.com/en_en/cognito/latest/developerguide/amazon-cognito-user-pools-using-the-access-token.html) · [Private submission session lookup](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/src/trusted_authorization/_non_production_submission_source_reads.py#L382)

## 6. Authoritative reader and writer requirements

Identify the concrete state owner and the authoritative reader and writer for each applicable revocation path. Define the exact read key, effective revocation state, when a write takes effect, source provenance, revision or observation semantics, freshness bounds, expiry, and unavailability behavior. Preserve the distinction between verified currentness, affirmative revocation, and uncertainty. The private reader validates the pinned owner, source and version, provenance, revision, exact query, observation time, and validity interval. JWT verification and eventually consistent session listings provide insufficient evidence for this gate. [Private submission observation validation](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/src/trusted_authorization/_non_production_submission_source_reads.py#L408)

## 7. Revocation ordering requirements

A revocation that takes effect before the durable `PROVISIONAL → SUBMITTED` transition must prevent the transition. If the verified transition commits first under the required authority checks, later revocation leaves the committed record intact. Demonstrate that the guarantee covers the same submission composition through the durable commit point and covers every applicable independent revocation path. A recent lookup, local sequencing, or a synthetic marker alone leaves this requirement unmet. [Submission-time ordering contract](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-submission-time-currentness-mutation-boundary-v1.md#L23) · [Lifecycle mutation ownership contract](cep-stage5i-nonproduction-effective-submission-lifecycle-mutation-ownership-contract-v1.md#18-revocation)

## 8. Commit-boundary responsibility matrix

| Role | Responsibility |
|---|---|
| Authentication Verification Owner | Accountable for exact-session identity, authoritative revocation currentness, and enforceable ordering evidence. |
| Amazon Cognito | Identity and authentication provider. Its responsibility follows its documented service guarantees. |
| TrustedAuthorizationEvaluator | Sole authorization ALLOW/DENY decision authority. |
| Assessment Service | Canonical Assessment Attempt lifecycle authority. |
| Assessment Submission Resource Lifecycle Authority | Owns the future durable submission transition, submission persistence, and commit verification. |
| Trusted Authorization | Consumes governed authority evidence and preserves its provenance. Revocation state must come from its authoritative owner. |
| Website | Presentation and authorized request delivery only. |

[Authentication trust and provenance governance](trusted-authorization-authentication-trust-provenance-governance-v1.md#authentication-verification-owner) · [Submission-time authority roles](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/docs/cep-stage5-submission-time-currentness-mutation-boundary-v1.md#L9)

## 9. Fail-closed behavior

Missing, stale, uncertain, or unavailable required session evidence must result in `UNAVAILABLE` with empty evidence. Affirmative revocation before commit produces an empty authorization failure. Both outcomes bar submission mutation and completion evidence, including `SUBMITTED` and `ALREADY_SUBMITTED`. The current verifier returns `REVOCATION_CURRENTNESS_UNAVAILABLE` when configured to require revocation currentness. [Lifecycle mutation ownership contract](cep-stage5i-nonproduction-effective-submission-lifecycle-mutation-ownership-contract-v1.md#18-revocation) · [Cognito verifier failure behavior](https://github.com/mnguyen3778/aws-ai-knowledge-assistant/blob/4e2e6661dfaefebd5e7feff02d4ea608b22ec860/src/trusted_authentication/cognito_authentication_verification.py#L191)

## 10. Adversarial acceptance criteria

| Test cases | Required result |
|---|---|
| Revocation before authentication, after authentication, during nine-source reservation acquisition, and immediately before submission commit | Effective revocation before commit prevents any transition and completion evidence, including when local JWT verification succeeds. |
| Concurrent revocation and commit | Reproduce both orderings. Effective revocation first blocks the transition. A verified commit first remains intact after revocation. |
| Stale provider observations and provider read failure | Fail closed with empty evidence and no transition. |
| Wrong session, principal, app client, or issuer | Reject the presentation or evidence without mutation or completion evidence. |
| Refresh and rotation | Prove continuity within the same session where applicable. Reject substitution with a different session. Refresh or rotation must not restore a revoked session's authority. |
| Cancellation and cleanup | Release acquired protections and follow the lifecycle owner's commit verification and recovery rules before any completion claim. |

Reproducible tests must exercise the actual approved authority mechanism and relevant writer paths before operational acceptance. Synthetic observations and the existing synthetic marker cannot satisfy this requirement on their own.

## 11. Explicit implementation exclusions

This document authorizes no implementation, new authority source, session ledger, database, service, API, infrastructure, Cognito configuration change, live AWS call, production use or deployment, submission persistence or mutation, or Git commit or push. Existing contracts and the nine-source coordinator remain in force.

## 12. Remaining dependency and next gate

**Implementation remains BLOCKED.** The Authentication Verification Owner must demonstrate exact-session binding, an authoritative currentness reader and revocation writer, complete coverage of applicable revocation paths, enforceable ordering through the durable submission commit point, fail-closed uncertainty handling, and reproducible adversarial evidence. Obtain separate Founder authorization before implementation. Operational acceptance requires verification against the approved mechanism.

## 13. Stage 5 status

Stage 5 remains in progress. Package 1 remains operationally incomplete. Stages 6 and 7 have not started.

| Stage 5 deliverable | Status |
|---|---|
| Joint Authorization Protection | In progress |
| Governed Submission Persistence | Pending |
| End-to-End Verification | Pending |
| Final Stage 5 Closeout | Pending |
