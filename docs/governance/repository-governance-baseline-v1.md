# Repository Governance Baseline v1

## 1. Purpose

Repository Governance Baseline v1 establishes the canonical governance policy
for repository autonomy, repository ownership conformance, repository
responsibility boundaries, repository interaction, repository governance
lifecycle, governance reviews, and repository conformance across the Nguyen AI
Platform.

This document governs repositories as repositories.

This document does not govern:

- cross-repository contracts
- platform architecture
- implementation
- runtime behavior

Those responsibilities belong to existing approved baselines.

This document is governance only. It does not define APIs, schemas,
algorithms, runtime behavior, production code, deployment, infrastructure,
testing guidance, release procedures, security implementation, validation
implementation, transport protocols, serialization, or implementation
mechanics.

## 2. Scope

Repository governance applies to the approved repositories in the Nguyen AI
Platform ecosystem:

- `nguyen-ai-platform`
- `nguyen-ai-assessment-service`
- `executive-intelligence-platform`
- `nguyen-ai-website`

In scope:

- repository autonomy governance
- repository ownership conformance
- repository responsibility boundary governance
- repository interaction policy
- repository governance lifecycle policy
- repository governance review requirements
- repository governance conformance requirements
- repository governance stop conditions

Out of scope:

- cross-repository contract governance
- platform architecture definition
- repository ownership redefinition
- implementation guidance
- runtime behavior
- production code
- deployment
- infrastructure
- testing guidance
- release procedures
- security implementation
- validation implementation
- APIs
- schemas
- algorithms
- transport protocols
- serialization

## 3. Governance Authority

The `nguyen-ai-platform` repository is the governing authority for Repository
Governance Baseline v1.

This authority is limited to governance policy for repository autonomy,
repository ownership conformance, repository responsibility boundaries,
repository interaction rules, repository governance reviews, and repository
conformance.

Repository governance derives from the approved architecture and governance
baselines. It does not supersede or redefine those baselines.

Human decision authority is required for approval, revision, supersession, or
retirement of repository governance policy.

Repository governance authority must not move responsibilities between
repositories, duplicate responsibilities, create new repository
responsibilities, or authorize implementation outside approved repository
ownership.

## 4. Repository Governance Philosophy

Repository governance is based on the following governing philosophy:

- Architecture assigns responsibilities.
- Repository ownership assigns accountability.
- Contracts govern communication.
- Repositories govern implementation within approved ownership boundaries.
- Governance preserves these boundaries over time.

Repository governance protects the relationship between approved architecture,
approved repository ownership, governed contract boundaries, and repository
autonomy. It does not replace architecture, contract governance, or
implementation repository authority.

## 5. Relationship to Existing Approved Baselines

This document derives from the approved Phase I Platform Architecture
Foundation and the approved Phase II governance baselines.

Approved Phase I baselines:

- Platform Repository Foundation v1.
- Platform Architecture Baseline v1.
- Repository Ownership Baseline v1.
- Platform Integration Baseline v1.
- System Context Baseline v1.
- Foundation Baseline Review v1.

Approved Phase II baselines:

- Platform Governance Baseline v1.
- Cross-Repository Contract Governance Baseline v1.

Repository Governance Baseline v1 must remain consistent with:

- Platform Governance Baseline v1.
- Cross-Repository Contract Governance Baseline v1.
- Repository Ownership Baseline v1.
- Platform Architecture Baseline v1.
- Platform Integration Baseline v1.

This document does not supersede, redefine, or modify any approved baseline. If
there is a conflict between this document and an approved architecture or
governance baseline, the approved baseline remains authoritative until changed
through approved governance.

## 6. Repository Governance Principles

Repository governance preserves the following principles:

- Repository ownership is immutable unless changed through approved
  architecture governance.
- Repository autonomy exists only within approved architectural boundaries.
- Each repository remains accountable for its approved responsibility only.
- Producer and consumer isolation is preserved.
- Repository boundaries shall not blur through implementation convenience.
- Repository interaction shall preserve versioned contract boundaries.
- Immutable evidence is preserved.
- Deterministic behavior is preserved.
- End-to-end lineage is preserved.
- Fail-closed validation is preserved.
- Explainability is preserved.
- Human decision authority is preserved.
- Repository governance shall not redefine architecture.
- Repository governance shall not redefine repository ownership.
- Repository governance shall not redefine cross-repository contract
  governance.

## 7. Repository Identity

Every approved repository possesses a stable architectural identity.

Repository identity is independent of implementation details, runtime behavior,
deployment environment, infrastructure, code organization, internal modules, or
operational state.

Repository identity changes only through approved architectural governance.

Repository identity must remain traceable to the approved Platform Architecture
Baseline v1 and Repository Ownership Baseline v1.

## 8. Repository Autonomy

Each repository may evolve only within its approved ownership boundary.

Repository autonomy shall never be interpreted as architectural independence.
Repository evolution remains subordinate to approved architecture and
governance baselines.

Repository autonomy permits repositories to govern their owned implementation
responsibilities within approved boundaries. Repository autonomy does not
authorize architecture changes, ownership changes, contract governance changes,
or runtime behavior outside approved ownership.

Repository autonomy prohibits:

- ownership migration
- responsibility migration
- business logic duplication
- unauthorized artifact production
- unauthorized artifact consumption
- contract boundary bypass
- runtime behavior in the Platform repository

## 9. Repository Authority

Each repository possesses authority only within its approved ownership
boundary.

Repository authority cannot expand through implementation.

Repository authority cannot be inferred from convenience, dependency pressure,
presentation needs, downstream demand, operational preference, or repository
proximity.

Repository authority changes only through approved architecture governance.

Repository authority must remain consistent with approved ownership,
approved exclusions, approved producer and consumer boundaries, and governed
contract boundaries.

## 10. Repository Responsibilities

Repository Governance Baseline v1 references approved repository
responsibilities but does not redefine them.

`nguyen-ai-platform` is the architectural and governance control plane for the
Nguyen AI Platform. It owns architecture and governance only.

`nguyen-ai-assessment-service` is the sole producer of assessment truth.

`executive-intelligence-platform` is the sole producer of executive
intelligence.

`nguyen-ai-website` is the presentation-only consumer of Website Projection
Delivery Contracts.

The authoritative repository responsibility definitions remain in the approved
Platform Architecture Baseline v1 and Repository Ownership Baseline v1.

## 11. Repository Ownership Conformance

Repository ownership conformance requires:

- preservation of approved ownership
- preservation of ownership exclusions
- preservation of producer and consumer boundaries
- preservation of approved artifact ownership
- no duplicated responsibility
- no migrated responsibility
- no hidden expansion of repository authority
- no assumption of another repository's responsibility

Repository ownership conformance applies to repository-level governance
decisions. It does not authorize implementation work or redefine repository
responsibility.

## 12. Repository Interaction Rules

Repository interaction must preserve approved architecture, approved ownership,
and governed contract boundaries.

Repository interaction rules require:

- interaction only through approved governed contract boundaries
- no ownership violations
- no downstream reinterpretation of producer-owned meaning
- no bypass of approved producer and consumer flow
- no hidden dependencies
- no implicit ownership transfer
- no undocumented communication paths
- fail-closed behavior whenever interaction validity cannot be established

Repository interaction policy does not govern cross-repository contracts
themselves. Cross-repository contract governance remains governed by
Cross-Repository Contract Governance Baseline v1.

## 13. Repository Boundary Preservation

Repository governance preserves the approved repository boundaries of the
Nguyen AI Platform.

The Assessment Service is the sole producer of assessment truth.

The Executive Intelligence Platform is the sole producer of executive
intelligence.

The Website consumes Website Projection Delivery Contracts only.

The Platform repository owns architecture and governance only.

Repository boundaries must not be weakened, bypassed, duplicated, or blurred by
implementation convenience, repository autonomy, interaction needs, downstream
demand, or contract consumption.

## 14. Repository Governance Lifecycle

Repository governance lifecycle defines policy only for the lifecycle of
repository governance authority.

Governance adoption:

Repository Governance Baseline v1 becomes the canonical repository governance
baseline after approval under the governing platform process.

Governance review:

Repository governance must be reviewed against approved architecture,
approved repository ownership, Platform Governance Baseline v1, and
Cross-Repository Contract Governance Baseline v1 where repository interaction
depends on governed contracts.

Governance conformance:

Repository governance remains conformant only while it preserves approved
repository ownership, approved responsibility boundaries, approved exclusions,
producer and consumer isolation, and human decision authority.

Governance revision:

Repository governance revisions must remain bounded, policy-level, and
consistent with approved architecture and governance baselines.

Governance supersession:

A future Repository Governance Baseline may supersede this document only
through approved governance. Supersession must not redefine architecture,
repository ownership, contract governance, implementation, or runtime behavior.

Governance retirement:

Repository governance may be retired only when superseded by an approved
governance baseline or when its governed scope is no longer valid under
approved architecture.

This lifecycle does not define implementation workflow, release workflow,
runtime behavior, or operational processes.

## 15. Governance Review Requirements

Repository governance requires review of:

- repository ownership compliance
- repository autonomy
- responsibility boundaries
- ownership exclusions
- producer and consumer isolation
- repository interaction conformance
- Platform Governance alignment
- Cross-Repository Contract Governance alignment where applicable

Repository governance review must confirm that proposed or completed
repository-level governance activity remains within the approved repository
ownership model.

Repository governance review must not redefine architecture, redefine
ownership, define implementation guidance, or define contract governance.

## 16. Governance Conformance Requirements

Every repository must preserve:

- approved ownership
- approved exclusions
- repository autonomy within approved architectural boundaries
- producer and consumer isolation
- immutable evidence
- deterministic behavior
- end-to-end lineage
- fail-closed validation
- versioned contract boundaries
- explainability
- human decision authority

Repository governance conformance must be based on approved architecture and
governance evidence only. Unsupported interpretation, assumptions, inferred
implementation behavior, or undocumented operational state must not be used to
establish repository governance conformance.

## 17. Stop Conditions

Repository governance prohibits progression whenever:

- repository ownership is violated
- responsibilities migrate without approved architecture governance
- business logic is duplicated
- assessment truth is produced or modified outside the Assessment Service
- executive intelligence is generated outside the Executive Intelligence
  Platform
- the Website derives assessment truth or executive intelligence
- the Website consumes anything other than approved Website Projection
  Delivery Contracts
- the Platform repository introduces runtime behavior or production code
- producer and consumer isolation is weakened
- versioned contract boundaries are bypassed
- hidden repository dependencies are introduced
- lineage is broken
- fail-closed behavior is weakened
- human decision authority is bypassed
- approved architecture or governance baselines are redefined without approval

Any stop condition requires governance resolution before progression.

## 18. Success Criteria

Repository Governance Baseline v1 is successful when it:

- establishes the canonical Repository Governance Baseline v1
- preserves Platform Governance Baseline v1
- preserves Cross-Repository Contract Governance Baseline v1
- preserves Repository Ownership Baseline v1
- preserves Platform Architecture Baseline v1
- preserves Platform Integration Baseline v1
- preserves immutable repository responsibilities
- defines one bounded governance responsibility only
- governs repository autonomy and repository conformance only
- introduces no architectural changes
- introduces no repository ownership changes
- contains no implementation guidance
- contains no production code
