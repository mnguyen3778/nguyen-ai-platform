# Agent Governance

This file defines the operating rules for agents and contributors working in
the `nguyen-ai-platform` repository.

## Repository Identity

`nguyen-ai-platform` is the architectural control plane for the Nguyen AI
Platform ecosystem.

This repository contains architecture, governance, documentation, diagrams,
architecture decision records, release coordination, repository ownership
guidance, and cross-repository integration documentation only.

This repository must never contain production runtime application code.

## Platform Architect Responsibilities

The Platform Architect is responsible for:

- platform architecture
- governance review
- repository ownership review
- cross-repository coordination
- integration planning
- architecture conformance review
- release governance
- platform roadmap stewardship

The Platform Architect must not implement production code, generate runtime
patches, move responsibilities across repositories, or redesign approved
architecture without an identified architectural gap.

## Repository Ownership

Repository ownership is immutable.

### nguyen-ai-platform

Owns architecture and governance only.

### nguyen-ai-assessment-service

Owns assessment truth, assessment methodology, deterministic assessment
execution, business rules, evidence processing, decision engine behavior, and
`ExecutiveAssessmentSnapshot` production.

### executive-intelligence-platform

Owns snapshot validation, snapshot admission, catalog, derivation, Executive
Intelligence Package, Executive Intelligence Projection, and Website Projection
Delivery Contract production.

### nguyen-ai-website

Owns presentation, rendering, user interaction, and Executive Dashboard UI. It
consumes Website Projection Delivery Contracts and must never derive assessment
truth or executive intelligence.

## Architecture Review Workflow

Every sprint begins with approved architecture.

Architecture review must:

- identify the governing architecture documents
- confirm the intended producer and consumer
- confirm repository ownership
- identify versioned contract boundaries
- preserve immutable evidence and end-to-end lineage
- preserve deterministic behavior and explainability
- identify any architectural gaps before implementation planning

If implementation differs from approved architecture, approved architecture is
authoritative. The discrepancy must be reported and the smallest bounded
conformance fix must be recommended.

## Governance Review Workflow

Governance review must confirm that proposed work:

- preserves producer / consumer isolation
- preserves immutable evidence
- preserves deterministic execution
- preserves end-to-end lineage
- preserves fail-closed validation
- preserves versioned contracts
- preserves repository ownership
- improves business value without unnecessary complexity

Governance review must happen before implementation planning.

## Implementation Planning Workflow

Implementation planning must produce one bounded responsibility only.

Each implementation plan must define:

- objective
- owning repository
- reason ownership belongs in that repository
- implementation boundaries
- contract boundaries
- deterministic behavior requirements
- lineage requirements
- fail-closed requirements
- success criteria
- explicit out-of-scope items

Implementation planning does not authorize code changes. Implementation begins
only after explicit approval for the owning repository.

## Architecture Conformance Review

After implementation, architecture conformance review must verify:

- the owning repository performed the work
- no responsibility moved across repositories
- approved contracts were preserved
- deterministic behavior was maintained
- immutable evidence was not modified
- lineage remained complete
- fail-closed validation remained intact
- tests prove the approved boundaries

Any discrepancy must be treated as a conformance issue and corrected through the
smallest bounded implementation necessary.

## Release Governance

Release governance must confirm:

- implementation was reviewed
- tests passed where applicable
- architecture conformance was reviewed
- governance conformance was reviewed
- release notes identify the bounded responsibility
- commit and tag recommendations reflect the approved scope

Release tags must not imply production runtime readiness unless the owning
repository has separately completed approved implementation, testing, review,
and release governance.

## One Bounded Responsibility Per Sprint

Every sprint must have one bounded responsibility.

Agents must not combine unrelated roadmap items, implementation scopes,
repository responsibilities, architecture decisions, or release activities.

If a request would combine responsibilities, the Platform Architect must
recommend the smallest valid bounded responsibility and stop for approval.

## Stop Conditions

Agents must stop when a request would:

- introduce production runtime code into this repository
- move responsibilities between repositories
- bypass architecture review
- bypass governance review
- weaken producer / consumer isolation
- weaken fail-closed validation
- obscure lineage
- remove versioned contract boundaries
- replace deterministic evidence with unsupported interpretation
- combine multiple sprint responsibilities
