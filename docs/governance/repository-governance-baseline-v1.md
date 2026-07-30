# Repository Governance Baseline v1

## 1. Purpose and Scope

Repository Governance is the policy framework that preserves approved
repository ownership, architectural boundaries, and repository autonomy within
the Nguyen AI Platform.

The purpose of repository governance is to ensure that each repository remains
within its approved responsibility boundary and that cross-repository work does
not move, duplicate, obscure, or bypass repository-owned responsibilities.

The scope of repository governance includes policy for repository ownership
protection, repository boundary preservation, cross-repository coordination,
repository conformance, governance compliance, and repository governance review.

This document derives authority from:

- `docs/governance/platform-governance-baseline-v1.md`
- `docs/platform/repository-ownership-v1.md`

This document does not supersede the Platform Governance Baseline v1 or the
Repository Ownership Baseline v1. If there is a conflict, those baselines remain
authoritative.

This document defines governance policy only. It does not define architecture,
repository responsibilities, implementation, deployment, infrastructure,
security architecture, contract schemas, APIs, algorithms, transport
definitions, validation implementation, testing guidance, release procedures,
ADRs, roadmaps, or production behavior.

## 2. Governance Authority

`nguyen-ai-platform` is the governing authority for repository governance across
the Nguyen AI Platform ecosystem.

The platform repository owns repository governance policy, repository ownership
review, repository conformance expectations, and governance compliance review.
It does not own runtime application behavior in implementation repositories.

Repository autonomy is preserved within approved architectural boundaries. Each
repository may make decisions within its approved responsibility boundary, but
repository autonomy does not authorize ownership violations, responsibility
migration, duplicated responsibility, or bypass of approved contracts.

Human decision authority is required for repository governance approval,
ownership interpretation, conformance decisions, and supersession of repository
governance documents.

Repository governance authority is bounded by the approved architecture.
Repository governance may protect, interpret, and review approved ownership
boundaries, but it must not redefine architecture, redefine repository
ownership, move responsibilities, or introduce new repository responsibilities.

## 3. Repository Governance Principles

Repository governance is governed by these policy principles:

- Approved repository ownership must be preserved.
- Repository autonomy must be preserved within approved architectural
  boundaries.
- Producer and consumer isolation must be preserved.
- Immutable evidence must be preserved.
- Deterministic behavior must be preserved.
- End-to-end lineage must be preserved.
- Fail-closed validation must be preserved.
- Versioned contract boundaries must be preserved.
- Explainability must be preserved.
- Human decision authority must be preserved.
- Repositories must not assume another repository's owned responsibility.
- Governance must not replace evidence-backed outputs with unsupported
  interpretation.

## 4. Repository Governance Responsibilities

Repository governance is responsible for repository ownership protection.

Repository ownership protection ensures that proposed and completed work remains
within the ownership boundaries defined by the Repository Ownership Baseline v1.

Repository governance is responsible for repository boundary preservation.

Repository boundary preservation ensures that no repository performs,
duplicates, obscures, or bypasses another repository's approved responsibility.

Repository governance is responsible for cross-repository coordination.

Cross-repository coordination ensures that repositories interact only through
approved architectural boundaries and versioned contracts, while preserving
producer and consumer isolation.

Repository governance is responsible for repository conformance.

Repository conformance ensures that each repository remains compliant with the
Platform Governance Baseline v1, Repository Ownership Baseline v1, and approved
Phase I architectural baselines.

Repository governance is responsible for governance compliance.

Governance compliance ensures that ownership review, boundary review,
conformance review, and stop-condition enforcement are applied before
progression.

This section defines governance responsibilities only. It does not redefine
repository responsibilities.

## 5. Repository Governance Boundaries

Repository governance prohibits responsibility migration.

Responsibilities must not move between repositories unless approved through
architecture governance and reflected in an approved architectural baseline.

Repository governance prohibits ownership duplication.

A repository must not duplicate business logic, derivation responsibility,
assessment responsibility, presentation responsibility, or governance
responsibility owned by another repository.

Repository governance prohibits architectural responsibility overlap.

Repository responsibilities must remain distinct, explicit, and traceable to the
approved Repository Ownership Baseline v1.

Repository governance prohibits unauthorized artifact production.

A repository must not produce artifacts assigned to another repository by the
approved architectural baselines.

Repository governance prohibits unauthorized artifact consumption.

A repository must not consume artifacts outside approved architectural
boundaries or bypass approved producer and consumer relationships.

Repository governance references approved architectural baselines only. It does
not define new architecture or new repository responsibilities.

## 6. Repository Conformance Requirements

Every repository must satisfy these requirements to remain repository
governance compliant:

- remain within approved ownership boundaries
- preserve producer and consumer isolation
- preserve versioned contract boundaries
- preserve deterministic behavior
- preserve immutable evidence
- preserve explainability
- preserve end-to-end lineage
- preserve fail-closed validation
- preserve human decision authority
- avoid duplicating another repository's responsibilities
- avoid producing artifacts owned by another repository
- avoid consuming artifacts outside approved architectural boundaries
- preserve approved ownership exclusions
- remain consistent with Platform Governance Baseline v1
- remain consistent with Repository Ownership Baseline v1
- remain consistent with approved Phase I architectural baselines

Repository conformance applies to proposed work, active work, completed work,
and release readiness review.

## 7. Repository Governance Reviews

### Ownership Assignment Review

Ownership Assignment Review confirms that proposed work is assigned to the
repository that owns the relevant responsibility under the Repository Ownership
Baseline v1.

### Ownership Exclusions Review

Ownership Exclusions Review confirms that proposed work does not violate any
explicit ownership exclusion defined by approved architectural baselines.

### Repository Boundaries Review

Repository Boundaries Review confirms that proposed work preserves each
repository's approved boundary and does not create responsibility overlap.

### Cross-Repository Responsibility Drift Review

Cross-Repository Responsibility Drift Review confirms that responsibility does
not migrate through convenience, dependency pressure, presentation needs, or
downstream demand.

### Architecture Conformance Review

Architecture Conformance Review confirms that completed work remains aligned
with approved architecture, repository ownership, and integration boundaries.

### Platform Governance Conformance Review

Platform Governance Conformance Review confirms that repository governance
decisions remain consistent with Platform Governance Baseline v1.

## 8. Repository Governance Stop Conditions

Repository governance shall prohibit progression when any of the following
conditions are present:

- repository ownership is violated
- responsibilities migrate without approved architectural change
- business logic is duplicated
- `nguyen-ai-assessment-service` derives executive intelligence
- `executive-intelligence-platform` modifies assessment truth
- `nguyen-ai-website` derives assessment truth
- `nguyen-ai-website` derives executive intelligence
- `nguyen-ai-platform` introduces production runtime behavior
- Platform Governance Baseline v1 is violated
- Repository Ownership Baseline v1 is violated
- approved Phase I architectural baselines are violated
- producer and consumer isolation is weakened
- immutable evidence is modified or obscured
- deterministic behavior is replaced with unsupported interpretation
- end-to-end lineage is broken
- fail-closed validation is weakened or bypassed
- versioned contract boundaries are bypassed or removed
- explainability is weakened or removed
- human decision authority is bypassed

When a repository governance stop condition is present, progression must stop
until the condition is resolved through an approved bounded responsibility that
preserves approved architecture and repository ownership.

## 9. Repository Governance Lifecycle

Governance adoption:

Repository Governance Baseline v1 becomes the canonical repository governance
baseline after architecture review confirms consistency with Platform
Governance Baseline v1, Repository Ownership Baseline v1, and approved Phase I
architectural baselines.

Governance conformance:

Repository governance documents must remain consistent with the Platform
Governance Baseline v1 and Repository Ownership Baseline v1.

Governance review:

Repository governance documents must be reviewed for consistency with approved
architecture, repository ownership, governance principles, governance stop
conditions, and repository conformance requirements.

Governance revision:

Repository governance revisions must be bounded, policy-level, and justified by
an approved governance need or approved architectural change.

Governance supersession:

A future Repository Governance Baseline may supersede this document only after
approved governance review. Supersession must not redefine architecture or
repository ownership unless a future approved architectural baseline explicitly
does so.

Governance retirement:

Repository governance documents may be retired only when superseded by an
approved governance document or when the governed scope is no longer valid
under approved architecture.

This lifecycle defines governance policy only. It does not introduce
implementation guidance, release procedures, production behavior, or
architectural changes.
