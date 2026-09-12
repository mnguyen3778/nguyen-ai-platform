# Trusted Authorization Authentication Trust Provenance Governance v1

## Purpose

This artifact defines the governed authentication trust-provenance boundary
required before Trusted Authorization may legitimately receive
`TrustedSubjectEvidence` with `verified=True`.

The decision prevents caller assertions, provider strings, subject strings,
route facts, raw credential presence, claims dictionaries, AI output, roles, or
application handler assumptions from being laundered into verified subject
evidence.

## Scope

This governance applies to the upstream authentication evidence boundary for
Trusted Authorization.

It governs the semantic chain:

```text
raw / mechanism-specific authentication input
    -> authentication verification mechanism
    -> verified authentication fact
    -> trusted-subject-evidence handoff
    -> TrustedSubjectEvidence
    -> Principal Mapping
    -> remaining authorization graph
```

It does not implement authentication, select Cognito, validate JWTs, wire
handlers, activate runtime behavior, create persistence, or grant production
authority.

## Existing Architecture

The implementation repository currently defines `TrustedSubjectEvidence` as a
frozen model with:

- `provider: str`
- `subject: str`
- `verified: bool`

The evaluator treats invalid subject evidence as `AUTHENTICATION_INVALID`
before later authorization facts are evaluated. Principal Mapping consumes
`provider` and `subject` and maps that verified external identity reference to a
governed Principal. Principal Mapping does not verify credentials and does not
establish authentication provenance.

Current tests and local composition can construct `TrustedSubjectEvidence`
directly. That is acceptable for bounded tests, but it is not authentication
provenance for application runtime.

## Problem Statement

The missing governed fact is:

```text
External subject S was successfully authenticated by authentication mechanism M
under an acceptable and current authentication context.
```

That fact is upstream evidence. It is not authorization, Principal Mapping,
Membership, Entitlement, Resource authority, Operation authority, or `ALLOW`.

## Authentication Trust Chain

The accepted trust chain is:

```text
RAW / MECHANISM-SPECIFIC AUTHENTICATION INPUT
    -> AUTHENTICATION VERIFICATION MECHANISM
    -> VERIFIED AUTHENTICATION FACT
    -> TRUSTED-SUBJECT-EVIDENCE HANDOFF
    -> TrustedSubjectEvidence
    -> Principal Mapping
    -> remaining authorization graph
```

Trusted Authorization does not authenticate raw credentials. It consumes
subject evidence only after an independently governed Authentication
Verification Owner has established the verified authentication fact.

## Raw / Untrusted Authentication Input

Layer 1 inputs include:

- Authorization header
- JWT text
- session cookie
- API key
- request context
- claims dictionary
- browser identity state
- request-body subject
- UI user identifier
- provider string
- AI statement

Layer 1 is not verified authentication.

The following are explicit non-authority facts:

- raw credential presence != verification
- JWT shape != verification
- claims presence != verification
- subject identifier != verification
- provider name != verification
- route match != verification
- handler execution != verification
- browser state != verification
- AI statement != verification

## Authentication Verification Owner

The Authentication Verification Owner is the logical responsibility that
actually verifies an external credential, assertion, or session and determines
whether authentication succeeded.

The owner may later be realized by an identity provider, trusted platform
authorizer, authentication service, verified session mechanism, or another
governed authentication verifier.

The owner is not automatically:

- AWS
- Cognito
- IAM
- Lambda execution role
- application handler
- route
- browser
- user
- AI system
- provider-name string

## Terminating Authentication Trust Basis

The selected terminating trust basis is:

```text
an independently governed Authentication Verification Owner's successful,
current verification result
```

The trust chain does not terminate at a Python type, caller boolean, handler
assertion, provider string, subject string, route, AI statement, raw credential
presence, or claims dictionary.

## Verified Authentication Fact

A verified authentication fact means:

```text
An independently governed authentication mechanism has successfully verified
external subject S under mechanism/provenance M and the required current
authentication validity conditions.
```

The fact is legitimate only when produced by an authorized Authentication
Verification Owner under the governed authentication mechanism contract.
Matching fields on a caller-constructed object are not sufficient.

## Trusted Subject Evidence Handoff

The Trusted Subject Evidence Handoff is a separate responsibility downstream of
authentication verification.

Its responsibilities are:

- accept only already-legitimate verified authentication facts;
- validate the bounded representation;
- preserve provider/mechanism provenance and external subject identity;
- construct `TrustedSubjectEvidence`;
- set `verified=True` only from that already-legitimate verified fact;
- fail closed for malformed, foreign, or unverified input.

It does not authenticate credentials, map Principals, check Membership, check
Entitlement, determine Resource authority, select operations, or produce
`ALLOW` / `DENY`.

## TrustedSubjectEvidence Semantics

`TrustedSubjectEvidence` is the Layer-3 subject evidence consumed by Trusted
Authorization. Its presence is not itself proof that real authentication
occurred. Its legitimacy depends on provenance through the governed
authentication verification boundary and subject-evidence handoff.

## Provider Semantics

`TrustedSubjectEvidence.provider` is the provider/mechanism namespace for the
external subject identity consumed by Principal Mapping.

The provider value preserves provenance and namespace. It does not itself
establish verification.

## Subject Semantics

`TrustedSubjectEvidence.subject` is the externally authenticated subject
identifier within the governed provider/mechanism namespace.

The subject is not automatically:

- a Nguyen AI Principal;
- a username;
- an email address;
- a role;
- a permission;
- a resource relationship;
- an authorization identity.

Principal Mapping remains responsible for:

```text
(provider, subject) -> Principal
```

## Provider/Subject Binding

The verified authentication fact must bind provider/mechanism provenance and
subject together from the same verified authentication event or context.

The following is prohibited:

```text
verified provider from authentication A
    + subject from request B
    -> TrustedSubjectEvidence
```

The same subject string under different providers is not automatically the same
identity. `(provider-A, "123")` and `(provider-B, "123")` remain distinct unless
Principal Mapping governance explicitly maps them.

## verified=True Semantics

`TrustedSubjectEvidence.verified = True` means:

```text
authentication success was established upstream by the governed Authentication
Verification Owner and preserved through the governed subject-evidence handoff.
```

It does not mean:

- caller supplied `True`;
- handler decided `True`;
- provider string was recognized;
- JWT looked valid;
- claims existed;
- user had a role;
- Principal Mapping succeeded.

## Authentication != Authorization

Authentication establishes identity evidence only. It does not establish
business authorization.

## Authentication != Principal Mapping

Authentication verifies external identity evidence. Principal Mapping
determines which governed Principal corresponds to that verified external
identity.

Principal Mapping must not verify credentials or infer verified status.

## Authentication != Membership

Authenticated Principal does not imply current Membership.

## Authentication != Entitlement

Authenticated Principal does not imply Entitlement.

## Authentication != Resource Authority

Authentication establishes no resource relationship and no right to any
Resource.

## Authentication != Operation Authority

Authentication does not select `PROTECTED_ASSESSMENT_SUBMISSION`,
`SUBMIT_ASSESSMENT`, or `RequestedAction.SUBMIT`.

## Authentication != ALLOW

Authenticated does not mean authorized.

Even perfect authentication must still pass the remaining governed
authorization graph, including Principal Mapping, Resource Identity,
Applicability, Business Entity, Membership, Entitlement, version/context
validation, and evaluator composition.

## Technology Neutrality

This governance is technology neutral. It remains valid if future
authentication uses Cognito, another OIDC provider, enterprise SSO, a trusted
application session, or another governed mechanism.

No production provider is selected by this artifact.

## Raw Credential Boundary

Trusted Authorization subject handoff must not receive or verify:

- password
- access token
- ID token
- refresh token
- session cookie
- raw Authorization header
- API key
- raw JWT

Credential verification belongs to the Authentication Verification Owner.

## Cognito/AWS Status

Cognito may later realize the Authentication Verification Owner. Cognito is not
selected, configured, integrated, or activated by this governance decision.

Cognito configuration is not authentication governance by itself. Cognito
authentication success would still require a governed adapter/handoff into
Trusted Authorization evidence.

AWS credential, IAM principal, Lambda execution role, or infrastructure
identity must not automatically become business-user `TrustedSubjectEvidence`.
Infrastructure authority is not application authentication and is not business
authorization.

## Handler/Route/UI Boundary

Application handlers may later consume an already verified authentication
result. Handler identity, route possession, or route matching does not establish
verification.

The following are not authentication provenance:

- `POST /assessment`
- `/v1/assistant`
- HTTP method
- Authorization header presence
- browser `loggedIn=true`
- UI user ID
- displayed email
- request-body subject

## AI/Provider Boundary

AI, LLM, agent, MCP, Bedrock, provider selection, model identity, or generated
text has zero authentication authority.

An AI statement such as "the user is authenticated as subject X" must not
establish verified subject evidence.

## Role/RBAC Boundary

Role labels such as `admin`, `owner`, `founder`, `member`, `employee`, or
`client` do not establish authentication provenance.

Authentication identity is distinct from role authority, Membership, and
Entitlement.

## Lifecycle / Freshness

A verified authentication fact must represent current valid authentication for
the relevant authentication context, not merely historical success.

The concrete mechanics for expiration, session lifetime, token freshness,
authentication time, key rotation, and revocation are responsibilities of the
Authentication Verification Owner and future production integration.

The bounded subject handoff must not claim those mechanics are solved.

## Revocation Responsibility

A previously verified identity may cease to be valid.

Future production realization must not allow stale or revoked authentication
evidence to remain indefinitely authoritative. Revocation detection and
validity-currentness are Authentication Verification Owner and production
adapter responsibilities.

## Replay Responsibility

Replay resistance belongs to the authentication verifier and production
integration. The Trusted Subject Evidence Handoff must not treat replayed raw
credentials, copied claims, or copied request context as verified facts.

## TOCTOU Scope

Authentication validity may change after verification. This governance
acknowledges that risk but does not solve end-to-end decision-to-execution
TOCTOU binding.

Authentication freshness is separate from authorization decision enforcement
and protected-operation execution binding.

## Minimum Necessary Data

For V1 semantics, the verified authentication fact must preserve:

- authentication provider/mechanism namespace;
- external subject identifier;
- successful current verification semantics.

Deferred to concrete authentication mechanism governance:

- issuer;
- audience;
- authentication time;
- expiration mechanics;
- session identifier;
- verification event identifier;
- provider key rotation;
- revocation mechanism.

Not required by the Trusted Authorization subject handoff:

- raw tokens;
- passwords;
- cookies;
- full claims dictionaries;
- names;
- emails;
- profile data;
- roles;
- group memberships;
- unnecessary PII.

## Privacy

Authentication evidence should expose the minimum information needed for
provenance, Principal Mapping, and governed audit.

Opaque external subject identifiers are preferred over email, name, or other PII
where the authentication mechanism supports them.

## Audit Provenance

Audit should eventually be able to identify:

- provider/mechanism namespace;
- external subject identifier;
- verification-result provenance;
- whether the subject handoff accepted or rejected the verified fact.

Raw credential or token retention is not required and should be avoided unless
separately governed.

## Non-Production Proof Semantics

A future non-production implementation may legitimately prove only:

```text
Given an already-legitimate verified authentication fact satisfying this
governance contract, the Trusted Subject Evidence Handoff deterministically and
fail-closed produces TrustedSubjectEvidence without expanding authentication or
authorization authority.
```

It may not prove:

- Cognito authentication works;
- JWT validation works;
- production sessions are valid;
- revocation is solved;
- arbitrary Python code cannot construct objects.

Tests may simulate an already-verified authentication fact as fixture
realization of the governed upstream fact. Test construction is not credential
verification.

## Future Production Realization

Future production integration must separately prove:

- the authentication mechanism actually verifies credentials or assertions;
- the verified result satisfies this governance contract;
- the adapter preserves provider/subject provenance;
- provider and subject originate from the same verified authentication context;
- freshness and revocation requirements are satisfied;
- untrusted request fields cannot bypass verification;
- raw credentials are not treated as Trusted Authorization evidence;
- only then may `TrustedSubjectEvidence` enter Trusted Authorization.

## Failure Model

Future subject handoff must fail closed when:

- input is not the governed verified-authentication fact representation;
- provider provenance is missing;
- subject is missing;
- provider is malformed;
- subject is malformed;
- verification/currentness semantics are not satisfied;
- foreign type is supplied;
- raw token is supplied;
- claims dictionary is supplied;
- request context is supplied;
- caller boolean is supplied;
- route, HTTP method, UI state, AI output, role, or provider name is supplied.

Failure must produce no `TrustedSubjectEvidence` with `verified=True`.

No default provider, default subject, default `verified=True`, fallback
authentication mechanism, or anonymous-to-authenticated promotion is allowed.

## Authority-Laundering Matrix

| Input | May establish verified authentication? |
| --- | --- |
| raw subject string | NO |
| provider string | NO |
| provider + subject | NO |
| caller boolean | NO |
| claims dictionary | NO |
| JWT-looking string | NO |
| raw JWT | NO, until verified by Authentication Verification Owner |
| request context | NO, unless future governed adapter proves already-verified authentication result |
| route | NO |
| HTTP method | NO |
| browser state | NO |
| UI identity | NO |
| AI output | NO |
| provider/model output | NO |
| role | NO |
| RBAC label | NO |
| AWS execution role | NO |
| IAM credential | NO |
| organization ownership | NO |
| governed Authentication Verification Owner output | YES, subject to required validity/provenance semantics |

## Circularity Prohibitions

The following circular models are rejected:

- authentication fact is trusted because handoff accepted it;
- handoff accepted it because the authentication fact says `verified`;
- provider is trusted because provider string says provider;
- subject is trusted because subject field contains subject;
- Python exact type is treated as proof real authentication occurred.

Exact type checks may enforce bounded application contracts. They are not proof
that real authentication occurred.

## Governance Model Decision

Selected:

```text
MODEL A - INDEPENDENT AUTHENTICATION VERIFICATION OWNER /
VERIFIED-AUTHENTICATION FACT TRUST BASIS
```

Rejected:

- MODEL B - Trusted Authorization performs authentication verification.
  Rejected because it collapses authentication verification into Trusted
  Authorization and would require credential/JWT/session mechanics outside this
  boundary.
- MODEL C - Application handler assertion trust basis. Rejected because handler
  assertion is self-verification.
- MODEL D - Infrastructure/provider implicit trust basis. Rejected because
  infrastructure identity, provider names, and route state do not prove
  business-user authentication.
- MODEL E - Caller-constructible verified assertion trust basis. Rejected
  because it launders caller assertions into `verified=True`.

## Open Questions / Deferred Decisions

The following remain deferred:

- concrete identity provider;
- Cognito configuration;
- JWT validation implementation;
- issuer and audience rules;
- session lifetime;
- token expiration mechanics;
- revocation mechanism;
- authentication event identifier;
- production adapter;
- audit persistence.

These deferred production details do not block the bounded non-production
subject-handoff proof because this artifact now governs the terminating
semantic trust basis.

## Governance Sufficiency

This decision is sufficient for a future strict read-only implementation-
authorization review of a bounded, technology-neutral, non-production
authenticated-subject / TrustedSubjectEvidence handoff.

That future review must still define exact files, types, fields, validation,
tests, and stop conditions. This artifact grants no implementation authority.

## Next Gate

Next gate:

```text
STRICT READ-ONLY AUTHENTICATION TRUST-PROVENANCE GOVERNANCE V1
CONFORMANCE / ACCEPTANCE REVIEW
```

After acceptance, a separate strict read-only implementation-authorization
review may determine whether a bounded non-production handoff implementation is
authorized.

## Production Authority Status

Production authentication is:

```text
NOT SELECTED / NOT INTEGRATED / NOT AUTHORIZED
```

Production authority is:

```text
NOT GRANTED
```
