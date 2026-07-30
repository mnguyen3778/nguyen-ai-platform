# Platform Architecture Baseline v1

## 1. Purpose

The Nguyen AI Platform exists to produce trustworthy, explainable executive
intelligence from structured assessment evidence.

The business objective of the platform is to support executive decision-making
by transforming deterministic assessment results into validated intelligence
products and presentation-ready website projections without weakening the
source of assessment truth.

The platform vision is a clear producer and consumer ecosystem in which each
repository has a bounded architectural role, each contract has an explicit
producer, and every executive-facing output remains traceable to the assessment
evidence and deterministic processing that produced it.

## 2. Platform Overview

The Nguyen AI Platform is a four-repository ecosystem:

- `nguyen-ai-platform`
- `nguyen-ai-assessment-service`
- `executive-intelligence-platform`
- `nguyen-ai-website`

Together these repositories define a controlled flow from assessment evidence
to executive-facing website presentation.

The platform separates responsibilities across architectural layers:

- architecture and governance are owned by the platform repository
- assessment truth is produced by the assessment service
- executive intelligence is produced by the executive intelligence platform
- website presentation is produced by the website repository

This separation preserves deterministic behavior, evidence integrity,
explainability, and ownership boundaries across the platform.

## 3. Four-Repository Architecture

### `nguyen-ai-platform`

`nguyen-ai-platform` is the architectural control plane for the Nguyen AI
Platform ecosystem.

It defines platform architecture, governance, repository ownership,
cross-repository integration boundaries, and authoritative platform
documentation.

It does not produce runtime application behavior, assessment truth, executive
intelligence, or website presentation.

### `nguyen-ai-assessment-service`

`nguyen-ai-assessment-service` is the sole producer of assessment truth.

It owns assessment methodology, deterministic assessment execution, business
rules, evidence processing, decision engine behavior, and
`ExecutiveAssessmentSnapshot` production.

It produces the assessment output consumed by the Executive Intelligence
Platform.

### `executive-intelligence-platform`

`executive-intelligence-platform` is the sole producer of executive
intelligence.

It owns snapshot validation, snapshot admission, catalog behavior, derivation,
Executive Intelligence Package production, Executive Intelligence Projection
production, and Website Projection Delivery Contract production.

It consumes `ExecutiveAssessmentSnapshot` records from the assessment service
and produces website-consumable projection contracts.

### `nguyen-ai-website`

`nguyen-ai-website` is the presentation layer for the Nguyen AI Platform.

It owns rendering, user interaction, Executive Dashboard UI, and presentation of
Website Projection Delivery Contracts.

It consumes website projection contracts and presents them to users without
deriving assessment truth or executive intelligence.

## 4. Repository Ownership

### `nguyen-ai-platform`

Owns:

- platform architecture
- governance documentation
- repository ownership guidance
- cross-repository integration documentation
- architectural baselines
- architecture decision records
- release coordination documentation

Must never own:

- production runtime application code
- assessment methodology execution
- evidence processing behavior
- decision engine behavior
- executive intelligence derivation
- website rendering or user interaction

### `nguyen-ai-assessment-service`

Owns:

- assessment truth
- assessment methodology
- deterministic assessment execution
- business rules
- evidence processing
- decision engine behavior
- `ExecutiveAssessmentSnapshot` production

Must never own:

- platform governance
- executive intelligence derivation beyond assessment truth production
- Executive Intelligence Package production
- Executive Intelligence Projection production
- Website Projection Delivery Contract production
- website presentation

### `executive-intelligence-platform`

Owns:

- `ExecutiveAssessmentSnapshot` validation
- snapshot admission
- executive intelligence catalog behavior
- executive intelligence derivation
- Executive Intelligence Package production
- Executive Intelligence Projection production
- Website Projection Delivery Contract production

Must never own:

- assessment truth production
- assessment methodology
- deterministic assessment execution
- raw evidence mutation
- website rendering
- website user interaction
- platform governance

### `nguyen-ai-website`

Owns:

- website presentation
- rendering
- user interaction
- Executive Dashboard UI
- consumption of Website Projection Delivery Contracts

Must never own:

- assessment truth
- assessment methodology
- evidence processing
- executive intelligence derivation
- Executive Intelligence Package production
- Executive Intelligence Projection production
- Website Projection Delivery Contract production
- platform governance

## 5. Architectural Principles

The following principles are immutable for the Nguyen AI Platform:

- The Assessment Service is the sole producer of assessment truth.
- The Executive Intelligence Platform is the sole producer of executive
  intelligence.
- The Website is presentation only.
- The Platform repository owns architecture and governance only.
- Producer and consumer isolation must be preserved.
- Immutable evidence must be preserved.
- Deterministic behavior must be preserved.
- End-to-end lineage must be preserved.
- Fail-closed validation must be preserved.
- Versioned contracts must be preserved.
- Explainability must be preserved.
- Repository ownership must be preserved.

These principles define the architectural boundaries for all repository
interaction and platform evolution.

## 6. System Context

The platform ecosystem is organized around explicit producers and consumers.

`nguyen-ai-assessment-service` produces assessment truth as
`ExecutiveAssessmentSnapshot` output. This output is consumed by
`executive-intelligence-platform`.

`executive-intelligence-platform` validates and admits assessment snapshots,
derives executive intelligence, and produces Website Projection Delivery
Contracts. These contracts are consumed by `nguyen-ai-website`.

`nguyen-ai-website` renders the website experience from the Website Projection
Delivery Contract. It is a consumer of executive intelligence output and does
not reinterpret, recompute, or derive the underlying intelligence.

`nguyen-ai-platform` provides the architectural reference and governance
context for the ecosystem. It does not participate in runtime production of
assessment truth, executive intelligence, or website presentation.

## 7. End-to-End Platform Flow

The canonical platform flow is:

1. Assessment evidence and assessment inputs are processed by
   `nguyen-ai-assessment-service`.
2. `nguyen-ai-assessment-service` executes deterministic assessment behavior
   and produces assessment truth.
3. Assessment truth is emitted as an `ExecutiveAssessmentSnapshot`.
4. `executive-intelligence-platform` consumes the
   `ExecutiveAssessmentSnapshot`.
5. `executive-intelligence-platform` validates and admits the snapshot.
6. `executive-intelligence-platform` derives executive intelligence from the
   admitted snapshot.
7. `executive-intelligence-platform` produces executive intelligence artifacts,
   including the Website Projection Delivery Contract.
8. `nguyen-ai-website` consumes the Website Projection Delivery Contract.
9. `nguyen-ai-website` presents the executive dashboard and related website
   experience without deriving assessment truth or executive intelligence.

The flow preserves lineage from website presentation back through executive
intelligence outputs, admitted snapshots, assessment truth, and assessment
evidence.

## 8. Architectural Boundaries

This architecture baseline intentionally excludes:

- governance processes
- roadmap planning
- deployment architecture
- security architecture
- release management
- implementation details
- runtime design
- infrastructure design
- sequence diagrams
- infrastructure diagrams
- repository-specific build, test, or deployment mechanics

These topics may be addressed by future bounded responsibilities, but they are
outside the scope of the Platform Architecture Baseline v1.

## 9. Assumptions

The architecture baseline assumes:

- the platform remains a four-repository ecosystem
- repository ownership remains immutable
- assessment truth originates only from `nguyen-ai-assessment-service`
- executive intelligence originates only from `executive-intelligence-platform`
- website presentation consumes Website Projection Delivery Contracts
- the website does not derive assessment truth or executive intelligence
- contracts between producers and consumers are versioned
- accepted platform outputs remain explainable and traceable to source evidence
- validation failure prevents downstream admission or presentation of invalid
  artifacts

## 10. Future Expansion

Future platform expansion may occur through additional bounded contracts,
additional executive intelligence artifacts, additional presentation surfaces,
or additional repository participants with explicitly defined producer and
consumer boundaries.

Any future expansion must preserve the existing producer and consumer
boundaries, immutable evidence, deterministic behavior, fail-closed validation,
end-to-end lineage, versioned contracts, explainability, and repository
ownership defined by this baseline.

This baseline identifies extension points only. It does not design future
implementations.
