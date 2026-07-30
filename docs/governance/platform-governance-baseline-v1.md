# Platform Governance Baseline v1

## 1. Purpose and Scope

Platform Governance defines the policy-level rules that preserve the approved
Nguyen AI Platform architecture across planning, review, implementation
coordination, conformance, and release readiness.

The purpose of Platform Governance is to ensure that every platform activity
preserves producer and consumer isolation, immutable evidence, deterministic
behavior, end-to-end lineage, fail-closed validation, versioned contracts,
explainability, repository ownership, human decision authority, and separation
of responsibilities.

The scope of authority for this document is governance policy only. It defines
how approved architecture is protected and reviewed. It does not define
architecture, implementation, deployment, infrastructure, security architecture,
testing, roadmap, release procedures, schemas, APIs, algorithms, transports, or
production code.

This document is governed by the approved Phase I Architecture Foundation:

- `docs/platform/platform-architecture-v1.md`
- `docs/platform/repository-ownership-v1.md`
- `docs/platform/platform-integration-baseline-v1.md`
- `docs/platform/system-context-baseline-v1.md`
- `docs/platform/foundation-baseline-review-v1.md`

This document defines governance policy only and does not supersede approved
architecture unless a future approved architectural baseline explicitly does
so.

## 2. Governance Authority

`nguyen-ai-platform` is the architectural governance authority for the Nguyen AI
Platform ecosystem.

The platform repository owns governance policy, architecture review,
repository ownership review, integration review, architecture conformance
review, and release readiness review. It does not own production runtime
application behavior.

Human decision authority is required for architectural approval, governance
approval, implementation authorization, release readiness decisions, and
supersession of approved baselines.

Repository autonomy is preserved within approved architectural boundaries. Each
implementation repository may evolve its owned responsibilities only within the
architecture, ownership, integration, and governance constraints approved by
the platform repository.

Governance may block progression when a proposed activity violates approved
architecture. Governance must not move responsibilities between repositories,
duplicate responsibilities, or replace evidence-backed outputs with unsupported
interpretation.

## 3. Governance Principles

The Nguyen AI Platform is governed by these immutable principles:

- Producer and consumer isolation must be preserved.
- Immutable evidence must be preserved.
- Assessment truth must remain immutable after production by
  `nguyen-ai-assessment-service`.
- Deterministic behavior must be preserved within each producing repository.
- End-to-end lineage must be preserved across repository boundaries.
- Validation must fail closed when inputs, contracts, or artifacts are invalid,
  missing, unknown, incompatible, or unapproved.
- Contracts crossing repository boundaries must be versioned.
- Executive-facing outputs must remain explainable.
- Repository ownership must be preserved.
- Human decision authority must be preserved.
- Governance must protect approved architecture without introducing production
  implementation.
- Consumers must not recreate, reinterpret, or replace producer-owned
  responsibility.

## 4. Governance Reviews

### Architecture Review

Architecture Review confirms that proposed work is consistent with the
approved Phase I Architecture Foundation.

Architecture Review must verify:

- governing architecture documents are identified
- intended producers and consumers are clear
- repository ownership is preserved
- versioned contract boundaries are preserved
- immutable evidence and end-to-end lineage are preserved
- deterministic behavior and explainability are preserved
- any genuine architectural gap is identified before implementation planning

### Repository Ownership Review

Repository Ownership Review confirms that proposed work belongs in the correct
repository and does not move or duplicate responsibility.

Repository Ownership Review must verify:

- `nguyen-ai-platform` remains architecture and governance only
- `nguyen-ai-assessment-service` remains the sole producer of assessment truth
- `executive-intelligence-platform` remains the sole producer of executive
  intelligence
- `nguyen-ai-website` remains presentation only
- no repository assumes another repository's owned responsibility
- explicit ownership exclusions are preserved

### Integration Review

Integration Review confirms that cross-repository interaction preserves
approved architecture and repository ownership.

Integration Review must verify:

- communication occurs only through approved versioned contracts
- producer and consumer boundaries are preserved
- contract compatibility expectations are preserved
- incompatible contracts fail closed
- downstream artifacts preserve upstream meaning and lineage
- no direct ownership violation is introduced through integration

### Architecture Conformance Review

Architecture Conformance Review confirms that completed work remains aligned
with approved architecture.

Architecture Conformance Review must verify:

- the owning repository performed only its approved responsibility
- no responsibility moved across repositories
- approved contract boundaries were preserved
- deterministic behavior was preserved
- immutable evidence and assessment truth were not modified by downstream
  consumers
- lineage remained complete
- fail-closed validation remained intact
- explainability remained intact

### Release Readiness Review

Release Readiness Review confirms that a release candidate remains aligned with
approved architecture and governance policy.

Release Readiness Review must verify:

- architecture review is complete
- repository ownership review is complete
- integration review is complete when cross-repository boundaries are involved
- architecture conformance review is complete after implementation
- governance stop conditions are not present
- release scope matches the approved bounded responsibility
- release labeling does not imply readiness beyond the approved scope

## 5. Governance Invariants

The following governance invariants apply platform-wide:

- Responsibilities cannot migrate between repositories without approved
  architectural change.
- Downstream systems must not reinterpret assessment truth.
- Human decision authority cannot be bypassed.
- Governance never overrides evidence-backed outputs.
- Repository ownership is immutable unless superseded through approved
  architecture governance.
- `nguyen-ai-assessment-service` remains the sole producer of assessment truth.
- `executive-intelligence-platform` remains the sole producer of executive
  intelligence.
- `nguyen-ai-website` remains presentation only.
- `nguyen-ai-platform` remains architecture and governance only.
- Versioned contract boundaries must remain explicit.
- Invalid or incompatible contracts must fail closed.
- End-to-end lineage must remain complete.
- Explainability must remain preserved.

## 6. Governance Stop Conditions

Progression is prohibited when any of the following conditions are present:

- repository ownership is violated
- responsibility is moved between repositories without approved architectural
  change
- responsibility is duplicated across repositories
- producer and consumer isolation is weakened
- assessment truth is modified by a downstream repository
- downstream systems reinterpret assessment truth
- immutable evidence is modified or obscured
- deterministic behavior is replaced with unsupported interpretation
- end-to-end lineage is broken or incomplete
- contract boundaries are missing, bypassed, unversioned, invalid, or
  incompatible
- fail-closed validation is weakened or bypassed
- explainability is weakened or removed
- human decision authority is bypassed
- architecture conformance fails
- immutable architectural principles are violated
- proposed work combines multiple bounded responsibilities
- production runtime application code is introduced into `nguyen-ai-platform`

When a stop condition is present, governance must prevent progression until the
condition is resolved through the smallest valid bounded responsibility
consistent with approved architecture.

## 7. Platform Conformance Requirements

Every repository must satisfy these requirements to remain platform compliant:

- preserve its approved repository ownership
- preserve explicit producer and consumer boundaries
- communicate across repository boundaries only through approved versioned
  contracts
- reject invalid, missing, unknown, incompatible, or unapproved contract inputs
- preserve upstream artifact meaning when acting as a consumer
- preserve end-to-end lineage for downstream artifacts
- preserve deterministic behavior for owned production responsibilities
- preserve explainability for executive-facing outputs
- avoid duplicating business logic owned by another repository
- avoid deriving outputs owned by another repository
- keep human decision authority intact
- remain within the approved bounded responsibility for the active sprint

Repository-specific conformance requirements:

- `nguyen-ai-platform` must contain only architecture, governance, ownership,
  coordination, conformance, and release governance documentation.
- `nguyen-ai-assessment-service` must remain the sole producer of immutable
  assessment truth and Executive Assessment Snapshots.
- `executive-intelligence-platform` must remain the sole consumer of Executive
  Assessment Snapshots in the canonical platform flow and the sole producer of
  executive intelligence and Website Projection Delivery Contracts.
- `nguyen-ai-website` must remain a presentation-only consumer of Website
  Projection Delivery Contracts.

## 8. Document Governance

Versioning:

This document is versioned as Platform Governance Baseline v1. Future versions
must identify the superseded version and the approved reason for change.

Review expectations:

This document must be reviewed against the approved Phase I Architecture
Foundation before it is used as the governance baseline for future platform
work.

Supersession:

This document remains authoritative until superseded by a future approved
Platform Governance Baseline. Supersession must preserve approved architecture
unless a future approved architectural baseline explicitly changes that
architecture.

Relationship to future governance documents:

Future governance documents may define narrower review standards, conformance
criteria, or release governance policy. Those documents must remain consistent
with this baseline and must not redefine approved architecture, repository
ownership, or integration boundaries.
