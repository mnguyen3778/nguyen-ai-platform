# EIP Governed Retrieval Boundary v1

## 1. Purpose and Scope

This document defines the governed boundary between the Executive Intelligence
Platform's production of an approved Website Projection Delivery Contract and a
future trusted consumer that needs to retrieve that contract.

The scope is narrowly limited to retrieval of an already-produced, governed:

- `website-projection-delivery-contract-v1`

from EIP by a future approved trusted consumer.

This document governs the architecture contract of retrieval. It does not
define, implement, or select:

- persistence
- database
- object storage
- HTTP
- REST
- API Gateway
- Lambda
- queue
- event bus
- filesystem
- cache
- S3
- DynamoDB
- SQL
- Cognito
- IAM
- authorization runtime
- endpoint
- runtime repository
- AI
- Bedrock
- RAG

This document does not govern individual Portal-user authorization. Portal-user
authorization remains governed separately by
[Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md).

## 2. Architectural Invariants

The Assessment Service remains the sole deterministic producer of assessment
business truth.

The Executive Intelligence Platform remains the deterministic executive
intelligence producer and authoritative producer of
`website-projection-delivery-contract-v1`.

The Governed Retrieval Boundary is the future mechanism for obtaining an
already-governed EIP delivery artifact. It is not an assessment, derivation,
publication, authorization, or presentation boundary.

The trusted consumer is a future server-side consumer of the governed EIP
delivery artifact. This document does not assign that consumer to a runtime
repository.

The Website remains a presentation-only consumer of Website Projection Delivery
Contracts.

The AI Knowledge Assistant may become a future authorized consumer or explainer
only after separate architecture review. It MUST NOT become authoritative for
assessment truth, executive intelligence, governed retrieval, or authorization
decisions.

Retrieval MUST NOT become derivation.

Retrieval MUST NOT become authorization.

Retrieval MUST NOT become methodology.

## 3. Producer Authority

EIP alone determines the governed contents and publication state of
`website-projection-delivery-contract-v1`.

A future retrieval mechanism MUST NOT:

- recompute EIP outputs
- derive replacement executive intelligence
- alter publication state
- alter eligibility
- alter freshness
- alter classification
- alter lineage
- alter compatibility
- alter limitations
- fabricate missing values
- repair rejected artifacts

Retrieval is transport or access to approved producer output. It is not a
second producer and MUST NOT become a competing source of executive
intelligence.

## 4. Approved Retrieval Artifact

The only approved artifact for this boundary is:

- `website-projection-delivery-contract-v1`

or an explicitly governed future version of that contract.

The retrieval boundary operates on the governed serialized contract instance or
output approved by EIP. The current EIP evidence includes
`WebsiteProjectionDeliveryContractInstance` and deterministic serialization of
that instance.

The retrieval boundary MUST NOT expose raw upstream objects merely because they
are convenient within EIP implementation.

## 5. Prohibited Upstream Artifacts

This retrieval boundary MUST NOT expose raw:

- assessment answers
- evidence
- BusinessDecisionPackage
- ExecutiveAssessmentSnapshot
- SnapshotCatalogEntry
- SnapshotDerivedArtifact
- ExecutiveIntelligencePackage
- ExecutiveIntelligenceProjection internal objects

unless a separately versioned future governance artifact explicitly authorizes
that exposure.

The Website-facing use case remains narrow. Internal EIP artifacts are not
client delivery artifacts.

## 6. Publication and Eligibility Preservation

Retrieval MUST preserve EIP's existing publication decision.

A retrieval consumer MUST NOT reinterpret an unpublished or ineligible artifact
as publishable.

If EIP marks an artifact as:

- unpublished
- ineligible
- incompatible
- denied
- otherwise non-deliverable

retrieval MUST fail closed according to the governed producer state.

The retrieval boundary MUST NOT recreate the EIP decision algorithm. It MUST
preserve the producer-owned result of EIP publication, eligibility,
compatibility, and delivery governance.

## 7. Freshness Preservation

EIP-owned freshness semantics remain authoritative.

The retrieval boundary MUST NOT:

- invent a new freshness rule
- silently refresh an artifact
- substitute an older artifact
- return a previous artifact merely because the current one is unavailable
- reinterpret stale as current

If freshness state prevents delivery, retrieval MUST fail closed.

Retrieval freshness checks, if later implemented, MUST preserve EIP-owned
freshness state and MUST NOT replace it with consumer cache state, transport
state, browser state, or local availability.

## 8. Lineage Preservation

Producer lineage and provenance MUST survive retrieval.

The trusted consumer must be able to establish that the artifact came from the
approved EIP publication boundary.

Retrieval MUST NOT sever lineage.

Retrieval MUST NOT fabricate lineage.

Retrieval MUST preserve the producer-owned lineage and version context carried
by the governed delivery contract.

This document does not prescribe a cryptographic implementation, storage
implementation, transport implementation, or proof mechanism.

## 9. Classification Preservation

EIP classification and content restrictions remain binding after retrieval.

The retrieval boundary MUST NOT:

- downgrade classification
- strip restrictive metadata to make an artifact deliverable
- reinterpret denied content
- expose content prohibited by the producer contract

If classification state prevents delivery, retrieval MUST fail closed.

## 10. Contract Version and Compatibility

Retrieval MUST preserve contract version and compatibility semantics.

The trusted consumer MUST NOT silently coerce an unsupported contract into a
supported one.

Unsupported, incompatible, missing, unapproved, or unversioned contracts MUST
fail closed unless separately governed compatibility behavior exists.

The retrieval boundary MUST preserve:

```text
contract version
+
compatibility semantics
```

from the EIP-produced delivery artifact.

## 11. Artifact Identity

A retrieved artifact must be unambiguously associated with the correct governed
delivery instance or resource.

Artifact identity governance is conceptual in this version. This document does
not invent:

- database primary keys
- URL structures
- S3 keys
- DynamoDB keys
- UUID requirements
- route parameters

Current EIP evidence exposes governed identity and lineage metadata, including
delivery contract version, publication policy version, projection version
context, producer snapshot identity, lineage, and Assessment Service
provenance references. Those concepts may support future identity governance,
but this document does not decide stable runtime lookup identity.

Stable runtime lookup identity remains a future implementation prerequisite.

Possession of an artifact identifier MUST NOT imply user authorization.

## 12. Retrieval Consumer Responsibility

The future trusted retrieval consumer is a consumer only.

It MAY:

- request an approved governed delivery artifact
- validate required contract and version state
- preserve producer metadata
- pass the approved artifact into a separately governed authorization and
  delivery process

It MUST NOT:

- derive executive intelligence
- mutate producer truth
- alter EIP publication state
- make Assessment Service decisions
- become the source of methodology
- infer missing producer outputs
- use AI to replace unavailable deterministic data

Consumer validation must preserve producer-owned meaning and fail closed when
the governed artifact cannot be established as approved, compatible, current,
classified for delivery, and lineage-complete.

## 13. Retrieval vs User Authorization

EIP governed retrieval is not Portal-user authorization.

Retrieval answers conceptually:

```text
Can the trusted system obtain this governed producer artifact through the
approved producer-consumer boundary?
```

Authorization answers conceptually:

```text
May this verified principal receive this governed resource?
```

The retrieval boundary MUST NOT interpret:

- Cognito identity
- membership
- entitlement
- role
- client authorization

unless separately governed later.

Successful retrieval MUST NOT imply that any Portal user is entitled to the
artifact.

The retrieved artifact is an input to later authorization and delivery
evaluation. It is not proof of principal entitlement.

## 14. Fail-Closed Retrieval Semantics

Retrieval MUST fail closed when any required retrieval or producer condition
cannot be established.

At minimum, retrieval MUST fail closed for:

- artifact absent
- artifact unavailable
- producer state unavailable
- publication state invalid
- artifact unpublished
- artifact ineligible
- artifact incompatible
- artifact stale
- lineage invalid or unavailable
- classification denied
- malformed serialized contract
- unsupported contract version
- conflicting producer metadata
- retrieval authority unavailable
- retrieval mechanism unavailable

Failure MUST NOT cause:

- older artifact fallback
- previous-client fallback
- default artifact selection
- cross-client artifact selection
- synthetic contract creation
- reconstruction from raw upstream artifacts
- fabricated executive intelligence

No UNKNOWN, missing, unavailable, stale, conflicting, or malformed state may
become implicit retrieval success.

## 15. Cross-Client Isolation

The retrieval boundary MUST preserve resource isolation.

A request or reference for one governed delivery MUST NOT result in another
client's, engagement's, or workspace's artifact.

This document does not define individual user authorization. It establishes
that retrieval identity and scope must be sufficiently precise to prevent
accidental cross-resource substitution before any later authorization decision
receives the artifact.

Current EIP delivery evidence exposes producer snapshot identity, projection
version context, lineage, and publication metadata. It does not establish an
approved runtime lookup model for `client + engagement + workspace` scope.

If client, engagement, or workspace scope metadata is required for future
retrieval, that metadata and lookup behavior MUST be governed before retrieval
runtime implementation. This document does not invent those fields.

## 16. Data Minimization

Retrieval MUST return the narrowest governed artifact required by the approved
consumer.

For the Executive Dashboard use case, the approved client-safe retrieval
boundary is:

- `website-projection-delivery-contract-v1`

Internal EIP structures are not retrieval conveniences.

Retrieval MUST NOT expose broader EIP packages, projections, snapshot records,
catalog records, derived artifacts, assessment evidence, or methodology
internals when the approved consumer only requires the Website Projection
Delivery Contract.

## 17. Observability and Audit Boundary

Future runtime implementation should make retrieval auditable without logging
unnecessary sensitive payload content.

At minimum, future retrieval observability should make it possible to audit:

- retrieval timestamp
- requested governed resource reference
- retrieved contract version
- producer or publication state
- retrieval success or failure
- failure reason classification
- correlation or request identifier

Retrieval observability MUST NOT require logging raw access tokens, secrets,
credentials, raw upstream artifacts, unnecessary sensitive payload content, or
complete governed delivery payloads unless a future approved audit model
explicitly authorizes that content.

This document does not choose CloudWatch, logging technology, storage
technology, telemetry transport, audit schema, or retention implementation.

Retrieval observability is distinct from the later principal-authorization
audit decision governed by the Portal Governed Delivery Authorization Model v1.

## 18. Technology Neutrality

This v1 governance artifact does not select:

- push versus pull
- synchronous versus asynchronous
- persistence versus direct retrieval
- API versus service invocation
- S3
- DynamoDB
- SQL
- filesystem
- cache
- queue
- event bus
- API Gateway
- Lambda
- container service

Technology selection requires later evidence and governance.

No implementation may treat this document as approval for storage, transport,
runtime, infrastructure, deployment, endpoint, or data-access design.

## 19. Runtime Ownership Non-Assignment

Governance owner:

- `nguyen-ai-platform`

EIP producer owner:

- `executive-intelligence-platform`

Future retrieval runtime owner:

- not yet assigned

This increment is not a runtime-owner assignment.

Runtime ownership MUST NOT be assigned by inference from producer ownership,
presentation needs, cloud proximity, repository convenience, or future consumer
interest.

This document does not assign retrieval runtime ownership to:

- Assessment Service
- EIP
- Website
- `aws-ai-knowledge-assistant`
- another repository

unless future objective evidence establishes an existing approved
responsibility through separate architecture governance.

## 20. Relationship to Authorization Governance

This document is subordinate to and consistent with the
[Portal Governed Delivery Authorization Model v1](portal-governed-delivery-authorization-model-v1.md).

The governed sequence is:

```text
EIP governed publication
        |
        v
governed retrieval
        |
        v
trusted authorization / delivery boundary
        |
        v
principal entitlement decision
        |
        v
Website
```

The retrieval artifact is an input to later authorization and delivery. It is
not evidence of principal entitlement.

Portal-user authorization still requires verified principal identity, current
authoritative membership or entitlement, client scope, engagement scope,
workspace scope, governed resource entitlement, and fail-closed authorization
decision semantics.

## 21. Implementation Prerequisites

Before retrieval runtime implementation may be authorized, the following
prerequisites remain unresolved:

- runtime owner and repository assignment
- retrieval mechanism selection
- persistence decision if persistence is required
- stable artifact or resource lookup semantics
- producer and consumer service contract
- authorization integration boundary
- audit and observability implementation
- failure semantics
- security controls
- producer and consumer boundary reconfirmation

This document does not resolve those prerequisites.

## 22. Implementation Gate

THIS GOVERNANCE ARTIFACT DOES NOT AUTHORIZE EIP RETRIEVAL RUNTIME
IMPLEMENTATION.

This governance artifact also does not authorize:

- endpoint implementation
- persistence implementation
- API Gateway
- Lambda
- S3
- DynamoDB
- Website integration changes
- Cognito changes
- IAM changes
- principal mapping
- membership or entitlement implementation
- AI Knowledge Assistant integration

No implementation may begin until runtime ownership, retrieval mechanism,
service contract, authorization integration, security controls, observability,
and producer/consumer boundaries are separately approved.

## 23. Acceptance Criteria

This governance increment passes only if it establishes:

- EIP remains authoritative producer
- retrieval is consumer behavior, not derivation
- `website-projection-delivery-contract-v1` is the approved retrieval artifact
- raw upstream artifacts remain protected
- publication state is preserved
- freshness is preserved
- lineage is preserved
- classification is preserved
- compatibility and version state are preserved
- retrieval and user authorization remain distinct
- retrieval fails closed
- no synthetic fallback exists
- cross-resource substitution is prohibited
- technology remains unselected
- runtime owner remains unassigned
- endpoint implementation remains unauthorized

This artifact is ready for review only if it preserves approved repository
ownership, approved producer and consumer boundaries, governed contract
boundaries, fail-closed semantics, and the Platform repository's
architecture-and-governance-only role.
