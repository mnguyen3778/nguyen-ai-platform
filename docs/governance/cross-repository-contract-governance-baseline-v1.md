# Cross-Repository Contract Governance Baseline v1

## 1. Purpose

The Cross-Repository Contract Governance Baseline v1 establishes the canonical
governance policy for all cross-repository contracts used throughout the Nguyen
AI Platform.

This document governs contract ownership, lifecycle, versioning, compatibility,
validation policy, supersession, and cross-repository coordination. It exists to
preserve approved architectural boundaries while allowing repositories to
communicate through governed contract boundaries.

This document is governance only. It does not define implementation guidance,
production behavior, APIs, schemas, algorithms, serialization, runtime
validation, transport protocols, deployment, infrastructure, testing guidance,
or production code.

## 2. Scope

This document applies to governed contracts that cross repository boundaries in
the Nguyen AI Platform.

In scope:

- Cross-repository contract governance policy.
- Contract ownership governance.
- Producer and consumer responsibility governance.
- Contract identity governance.
- Contract lifecycle governance.
- Versioning governance.
- Compatibility governance.
- Validation governance at policy level.
- Supersession governance.
- Cross-repository coordination governance.
- Contract governance conformance.

Out of scope:

- Production implementation.
- Repository implementation details.
- Contract schemas.
- APIs.
- Serialization formats.
- Algorithms.
- Runtime validation mechanics.
- Transport protocols.
- Deployment architecture.
- Infrastructure.
- Security architecture.
- Testing guidance.
- Release procedures.
- Roadmaps.
- Architecture redesign.
- Repository ownership redesign.

## 3. Governance Authority

The `nguyen-ai-platform` repository is the governing authority for
cross-repository contract governance.

This authority is limited to architecture and governance. The platform
repository does not own production runtime behavior, business logic, assessment
execution, executive intelligence generation, website presentation, or contract
implementation.

Human decision authority remains required for approving, revising, superseding,
or retiring governed cross-repository contract governance policy.

Repository autonomy is preserved within approved architectural boundaries.
Repositories govern their own implementation only within the responsibilities
assigned by approved architecture and repository ownership baselines.

## 4. Governance Principles

Cross-repository contract governance preserves the following principles:

- Architecture governs responsibilities.
- Contracts govern communication.
- Repositories govern implementation within approved ownership boundaries.
- Governance governs change.
- Producer and consumer responsibilities remain isolated.
- Producer-owned meaning is preserved across repository boundaries.
- Immutable evidence is preserved.
- Deterministic behavior is preserved.
- End-to-end lineage is preserved.
- Fail-closed validation is preserved.
- Versioned contracts are preserved.
- Explainability is preserved.
- Repository ownership is preserved.
- Human decision authority is preserved.

These principles apply to all governed cross-repository contracts regardless of
implementation, transport, storage, runtime environment, or operational context.

## 5. Relationship to Existing Approved Baselines

This document derives authority from the approved Phase I architecture
foundation and the approved Phase II Platform Governance Baseline v1.

Approved Phase I baselines:

- Platform Repository Foundation v1.
- Platform Architecture Baseline v1.
- Repository Ownership Baseline v1.
- Platform Integration Baseline v1.
- System Context Baseline v1.
- Foundation Baseline Review v1.

Approved Phase II baseline:

- Platform Governance Baseline v1.

This document does not supersede, redefine, or modify any approved baseline. If
there is a conflict between this document and an approved architectural baseline,
the approved architectural baseline remains authoritative until superseded by a
future approved architectural baseline.

Cross-repository contract governance must remain consistent with:

- Platform Governance Baseline v1.
- Platform Architecture Baseline v1.
- Repository Ownership Baseline v1.
- Platform Integration Baseline v1.

## 6. Repository Boundaries

Cross-repository contract governance preserves the approved repository
boundaries of the Nguyen AI Platform.

The `nguyen-ai-assessment-service` repository is the sole producer of assessment
truth. It owns assessment methodology, deterministic assessment execution,
business rules, evidence processing, decision engine behavior, and immutable
Executive Assessment Snapshot production.

The `executive-intelligence-platform` repository is the sole producer of
executive intelligence. It consumes Executive Assessment Snapshots and owns
snapshot validation, snapshot admission, catalog, derivation, Executive
Intelligence Package production, Executive Intelligence Projection production,
and Website Projection Delivery Contract production.

The `nguyen-ai-website` repository is a presentation-only consumer. It consumes
Website Projection Delivery Contracts only and must never produce assessment
truth, generate executive intelligence, or redefine producer-owned meaning.

The `nguyen-ai-platform` repository owns architecture and governance only. It
must never contain production runtime application code or own business logic.

Contract governance must not move, duplicate, or blur these repository
boundaries.

## 7. Contract Ownership Model

Every governed cross-repository contract must have exactly one approved
producer.

Every governed cross-repository contract must have approved consumers.

The approved producer owns the contract meaning. Producer-owned meaning includes
the business semantics, architectural intent, lineage expectations, and
authoritative interpretation of the contract within approved architecture.

Consumers never become co-producers by consuming a contract.

Consumers must never redefine producer-owned semantics.

Producer ownership cannot migrate through implementation, operational usage,
consumer interpretation, integration convenience, or downstream dependency.

Contract ownership remains bound to approved repository ownership unless changed
through approved architectural governance.

## 8. Producer Responsibilities

Approved producers are responsible for preserving the governed meaning and
architectural boundary of the contracts they produce.

Producer responsibilities include:

- Preserve producer-owned meaning.
- Preserve immutable evidence where the producer owns evidence.
- Preserve deterministic contract meaning.
- Preserve contract identity.
- Preserve versioned contract boundaries.
- Preserve lineage from producer-owned source responsibility.
- Publish only approved governed contracts for cross-repository consumption.
- Ensure contract changes remain within approved repository ownership.
- Support explainability of producer-owned contract meaning.

Producer responsibilities do not authorize producers to assume downstream
consumer responsibilities or to redefine repository ownership.

## 9. Consumer Responsibilities

Approved consumers are responsible for preserving producer-defined meaning when
consuming governed cross-repository contracts.

Consumer responsibilities include:

- Consume only approved contracts from approved producers.
- Preserve producer-owned meaning.
- Preserve producer and consumer isolation.
- Preserve versioned contract boundaries.
- Preserve lineage across consumption boundaries.
- Fail closed when contract validity, compatibility, identity, approval, or
  version status cannot be established.
- Preserve explainability of downstream use without reinterpreting upstream
  truth.
- Remain within approved repository ownership.

Consumer responsibilities do not authorize consumers to modify producer-owned
truth, generate producer-owned outputs, or become co-producers of governed
contracts.

## 10. Contract Identity

Every governed cross-repository contract must possess a persistent identity.

Contract identity is independent of implementation. It must not depend on
runtime mechanics, serialization format, transport protocol, storage location,
or implementation-specific naming.

Contract identity remains stable across compatible revisions.

Contract identity changes only through approved supersession governance.

Contract identity must preserve traceability to the approved producer, approved
consumers, approved architectural boundary, and approved contract purpose.

## 11. Contract Lifecycle Governance

Cross-repository contract lifecycle governance defines policy for the following
states:

- Proposal: A proposed cross-repository contract or contract change is
  identified for governance consideration.
- Approval: Human governance authority determines whether the proposed contract
  or change conforms to approved architecture and governance.
- Publication: An approved contract is made available as a governed
  cross-repository boundary.
- Adoption: Approved consumers recognize and consume the governed contract
  within approved repository boundaries.
- Revision: A governed contract is changed while preserving identity,
  compatibility expectations, producer-owned meaning, ownership, lineage, and
  governance approval.
- Supersession: A governed contract is replaced by an approved successor through
  explicit governance action.
- Retirement: A governed contract is withdrawn from active governed use while
  preserving lineage, auditability, and historical evidence.

Lifecycle governance is policy only. It does not define operational workflow,
implementation mechanics, release procedures, or runtime behavior.

## 12. Versioning Governance

Governed cross-repository contracts must have versioned boundaries.

Versioning governance requires:

- Approved version identity.
- Approved version ownership.
- Traceability from each governed version to its approved producer.
- Traceability from each governed version to approved consumers.
- Compatibility expectations for governed versions.
- Preservation of lineage across revisions.
- Preservation of producer-owned meaning across compatible revisions.
- Human governance approval for supersession or retirement.

This document does not define version numbering schemes, file formats,
serialization formats, or implementation mechanisms.

## 13. Compatibility Governance

Contract compatibility must be evaluated against approved architecture,
approved repository ownership, approved integration boundaries, producer-owned
meaning, lineage preservation, explainability, and fail-closed behavior.

Compatible contract revisions must preserve:

- Contract identity.
- Approved producer ownership.
- Approved consumer boundaries.
- Producer-owned meaning.
- Repository ownership.
- End-to-end lineage.
- Deterministic interpretation.
- Explainability.
- Fail-closed validation expectations.

Unknown, incompatible, invalid, unapproved, or unversioned contracts must fail
closed.

Compatibility governance does not define migration algorithms, runtime
compatibility checks, APIs, schemas, or implementation mechanics.

## 14. Validation Governance

Validation governance defines policy expectations for governed
cross-repository contracts.

Governed validation must preserve:

- Approved contract identity.
- Approved producer authority.
- Approved consumer boundaries.
- Producer-owned meaning.
- Repository ownership.
- Immutable evidence.
- Deterministic behavior.
- End-to-end lineage.
- Versioned contract boundaries.
- Explainability.
- Fail-closed behavior.
- Human decision authority.

Invalid, unknown, incompatible, unapproved, or unversioned contracts must
prohibit progression.

Validation governance is policy only. It does not define APIs, schemas,
serialization, algorithms, runtime validation, transport protocols, or
implementation mechanics.

## 15. Supersession Governance

Contract supersession must occur only through explicit governance approval.

Supersession governance requires:

- Historical lineage preservation.
- Traceability to prior approved contracts.
- Traceability to the approved successor contract.
- Preservation of immutable historical evidence.
- Preservation of auditability.
- Preservation of producer-owned meaning unless an approved architectural
  change explicitly authorizes otherwise.
- Preservation of repository ownership.
- Preservation of human decision authority.

Supersession must not erase, obscure, rewrite, or invalidate historical contract
evidence.

Supersession must not be used to move responsibilities between repositories or
to redefine approved architecture.

## 16. Cross-Repository Coordination

Cross-repository contract changes require governance coordination through the
`nguyen-ai-platform` repository.

Coordination must evaluate proposed contract creation, revision, supersession,
or retirement against:

- Platform Governance Baseline v1.
- Platform Architecture Baseline v1.
- Repository Ownership Baseline v1.
- Platform Integration Baseline v1.

Cross-repository coordination must preserve:

- Approved architectural boundaries.
- Approved repository ownership.
- Producer and consumer isolation.
- Contract identity.
- Versioned contract boundaries.
- Compatibility expectations.
- Immutable evidence.
- Deterministic behavior.
- End-to-end lineage.
- Fail-closed validation.
- Explainability.
- Human decision authority.

Coordination governance does not authorize implementation activity, deployment
activity, release activity, or production behavior.

## 17. Stop Conditions

Cross-repository contract governance prohibits progression when:

- Repository ownership is violated.
- Producer ownership is ambiguous.
- Producer meaning is reinterpreted.
- Assessment truth is modified downstream.
- Executive intelligence is generated outside the Executive Intelligence
  Platform.
- The Website consumes anything other than approved Website Projection Delivery
  Contracts.
- Contract boundaries are bypassed.
- Lineage is broken.
- Contracts are invalid, unknown, incompatible, unapproved, or unversioned.
- Fail-closed behavior is weakened.
- Human decision authority is bypassed.
- Contract ownership migrates through implementation.
- Consumers become co-producers without approved architectural change.
- Approved architecture or governance baselines are superseded without explicit
  approved governance action.

Any stop condition requires governance resolution before progression.

## 18. Governance Conformance

Governed cross-repository contracts conform to this baseline only when they:

- Preserve approved architecture.
- Preserve approved repository ownership.
- Preserve approved integration boundaries.
- Preserve Platform Governance Baseline v1.
- Have exactly one approved producer.
- Have approved consumers.
- Preserve producer-owned meaning.
- Preserve producer and consumer isolation.
- Preserve contract identity.
- Preserve versioned boundaries.
- Preserve compatibility expectations.
- Preserve immutable evidence.
- Preserve deterministic behavior.
- Preserve end-to-end lineage.
- Preserve fail-closed validation.
- Preserve explainability.
- Preserve human decision authority.

Conformance evaluation must be based on approved governance and architecture
evidence only. Unsupported interpretation, assumptions, inferred implementation
behavior, or undocumented operational state must not be used to establish
contract governance conformance.

## 19. Success Criteria

Cross-Repository Contract Governance Baseline v1 is successful when it:

- Establishes the canonical Cross-Repository Contract Governance Baseline v1.
- Preserves all approved architecture baselines.
- Preserves Platform Governance Baseline v1.
- Preserves Repository Ownership Baseline v1.
- Preserves Platform Integration Baseline v1.
- Preserves immutable architectural invariants.
- Defines one bounded governance responsibility only.
- Introduces no architectural changes.
- Introduces no repository ownership changes.
- Contains no implementation guidance.
- Contains no production code.
- Establishes governance for contract ownership, identity, lifecycle,
  versioning, compatibility, validation policy, supersession, and
  cross-repository coordination.
