# Nguyen AI Platform

The Nguyen AI Platform is an evidence-governed executive intelligence ecosystem.
It transforms deterministic business assessment evidence into explainable
executive intelligence while preserving strict repository ownership, immutable
evidence, deterministic behavior, end-to-end lineage, fail-closed validation,
and versioned contracts.

This repository is the architectural control plane for the Nguyen AI Platform.
It contains platform architecture, governance, documentation, diagrams,
architecture decision records, release coordination, and cross-repository
relationship guidance only.

This repository must never contain production runtime application code.

## Four-Repository Ecosystem

The platform is organized into four repositories with immutable ownership
boundaries.

### nguyen-ai-platform

The platform repository owns:

- platform architecture
- governance
- repository ownership
- platform roadmap
- cross-repository relationships
- integration documentation
- architecture decision records
- release compatibility guidance
- system context
- diagrams

It does not own runtime application behavior, assessment execution, executive
intelligence generation, website rendering, APIs, persistence, infrastructure,
or deployment code.

### nguyen-ai-assessment-service

The Assessment Service is the sole producer of assessment truth.

It owns:

- assessment methodology
- deterministic assessment execution
- business rules
- evidence processing
- decision engine behavior
- immutable `ExecutiveAssessmentSnapshot` production

It produces `ExecutiveAssessmentSnapshot` artifacts and consumes no downstream
platform outputs.

### executive-intelligence-platform

The Executive Intelligence Platform is the sole consumer of assessment truth and
the sole producer of executive intelligence.

It owns:

- snapshot compatibility validation
- snapshot admission
- snapshot catalog
- deterministic derivations
- Executive Intelligence Package
- Executive Intelligence Projection
- Website Projection Delivery Contract

It consumes `ExecutiveAssessmentSnapshot` artifacts and produces Website-facing
projection delivery contracts.

### nguyen-ai-website

The Website is presentation only.

It owns:

- user interface
- user interaction
- rendering
- executive dashboard presentation

It consumes Website Projection Delivery Contracts. It must never derive
intelligence, perform assessment logic, own business rules, validate snapshots,
assemble packages, create projections, or recompute assessment truth.

## Platform Philosophy

Business value drives architecture. Governance drives implementation.
Technology serves business needs and must not override repository ownership or
evidence integrity.

The platform favors:

- deterministic systems over opaque automation
- evidence-governed intelligence over unsupported interpretation
- explainable outputs over hidden inference
- long-term maintainability over short-term implementation convenience
- explicit contracts over implicit coupling
- one bounded responsibility per sprint

## High-Level Architecture

The approved producer-to-consumer architecture is:

```text
nguyen-ai-assessment-service
  -> ExecutiveAssessmentSnapshot

executive-intelligence-platform
  -> compatibility validation
  -> snapshot catalog
  -> deterministic derivation
  -> Executive Intelligence Package
  -> Executive Intelligence Projection
  -> Website Projection Delivery Contract

nguyen-ai-website
  -> Executive Dashboard presentation
```

The platform repository governs this architecture but does not participate in
runtime execution.

## Documentation Structure

- `docs/platform/` contains platform-level architecture and ecosystem context.
- `docs/governance/` contains governance policies, review workflows, and release
  controls.
- `docs/diagrams/` contains architecture diagrams and visual system context.
- `docs/adr/` contains architecture decision records.
