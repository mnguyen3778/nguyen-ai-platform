# Platform Integration Baseline v1

## 1. Purpose

Platform integration exists to connect the four Nguyen AI Platform repositories
without merging their responsibilities.

Controlled integration is required so assessment truth, executive intelligence,
and website presentation remain independently owned, contract-bound, traceable,
and explainable.

Integration depends on repository ownership. Each repository may integrate with
other repositories only through the artifacts and boundaries appropriate to its
owned platform responsibility.

## 2. Integration Principles

The Nguyen AI Platform integration model is governed by these immutable
principles:

- Repository ownership is preserved.
- Producer and consumer isolation is preserved.
- Repositories communicate only through approved contracts.
- Assessment truth remains immutable after production by
  `nguyen-ai-assessment-service`.
- Processing remains deterministic at each producer boundary.
- Contracts are versioned.
- Validation fails closed when an input is invalid or incompatible.
- End-to-end lineage is preserved across repository boundaries.
- Executive-facing outputs remain explainable.
- Direct ownership violations are prohibited.
- Consumers do not recreate, reinterpret, or replace producer-owned
  responsibility.

## 3. Integration Model

### `nguyen-ai-platform`

Integration responsibility:

`nguyen-ai-platform` defines the authoritative architecture and integration
boundaries for the ecosystem.

It identifies repository responsibilities, producer and consumer relationships,
and approved cross-repository contract boundaries. It does not participate as a
runtime producer or consumer in platform integration.

### `nguyen-ai-assessment-service`

Integration responsibility:

`nguyen-ai-assessment-service` integrates with the platform as the sole producer
of assessment truth.

It exposes assessment truth to downstream consumers through
`ExecutiveAssessmentSnapshot` output and the Snapshot Integration Contract. It
does not produce executive intelligence or website projection artifacts.

### `executive-intelligence-platform`

Integration responsibility:

`executive-intelligence-platform` integrates with the platform as the sole
producer of executive intelligence.

It consumes `ExecutiveAssessmentSnapshot` input, performs snapshot admission,
produces Executive Intelligence Packages and Executive Projections, and emits
Website Projection Delivery Contracts for website consumption. It does not
produce assessment truth or website presentation.

### `nguyen-ai-website`

Integration responsibility:

`nguyen-ai-website` integrates with the platform as the presentation consumer.

It consumes Website Projection Delivery Contracts and presents the website
experience. It does not perform assessment processing, snapshot admission, or
executive intelligence derivation.

## 4. Integration Contracts

### `ExecutiveAssessmentSnapshot`

Purpose:

`ExecutiveAssessmentSnapshot` is the assessment truth artifact produced by
`nguyen-ai-assessment-service` for downstream executive intelligence
processing.

Producer:

- `nguyen-ai-assessment-service`

Consumer:

- `executive-intelligence-platform`

### Snapshot Integration Contract

Purpose:

The Snapshot Integration Contract defines the approved integration boundary for
transferring `ExecutiveAssessmentSnapshot` output from the assessment service to
the Executive Intelligence Platform.

Producer:

- `nguyen-ai-assessment-service`

Consumer:

- `executive-intelligence-platform`

### Executive Intelligence Package

Purpose:

The Executive Intelligence Package is an executive intelligence artifact
produced from an admitted assessment snapshot.

Producer:

- `executive-intelligence-platform`

Consumer:

- `executive-intelligence-platform`

### Executive Projections

Purpose:

Executive Projections are downstream executive intelligence outputs produced
from Executive Intelligence Package content for projection-specific use.

Producer:

- `executive-intelligence-platform`

Consumer:

- `executive-intelligence-platform`

### Website Projection Delivery Contract

Purpose:

The Website Projection Delivery Contract is the approved presentation-facing
contract consumed by the website.

Producer:

- `executive-intelligence-platform`

Consumer:

- `nguyen-ai-website`

## 5. Producer / Consumer Flow

The canonical integration flow is:

1. `nguyen-ai-assessment-service` produces assessment truth.
2. Assessment truth is emitted as an `ExecutiveAssessmentSnapshot`.
3. The Snapshot Integration Contract defines the transfer boundary into
   `executive-intelligence-platform`.
4. `executive-intelligence-platform` performs snapshot admission.
5. `executive-intelligence-platform` produces the Executive Intelligence
   Package.
6. `executive-intelligence-platform` produces Executive Projections.
7. `executive-intelligence-platform` produces the Website Projection Delivery
   Contract.
8. `nguyen-ai-website` consumes the Website Projection Delivery Contract.
9. `nguyen-ai-website` presents the website experience.

`nguyen-ai-platform` defines the architecture for this flow but does not
produce or consume runtime integration artifacts.

## 6. Cross-Repository Communication Rules

Allowed communication paths:

- `nguyen-ai-assessment-service` to `executive-intelligence-platform` through
  `ExecutiveAssessmentSnapshot` and the Snapshot Integration Contract.
- `executive-intelligence-platform` to `nguyen-ai-website` through the Website
  Projection Delivery Contract.
- `nguyen-ai-platform` to all repositories through architecture and ownership
  references.

Prohibited communication paths:

- `nguyen-ai-website` must not consume assessment evidence directly.
- `nguyen-ai-website` must not consume assessment truth except through Website
  Projection Delivery Contracts produced by `executive-intelligence-platform`.
- `nguyen-ai-website` must not bypass `executive-intelligence-platform` to
  derive executive intelligence.
- `executive-intelligence-platform` must not modify assessment truth.
- `executive-intelligence-platform` must not produce website presentation.
- `nguyen-ai-assessment-service` must not produce executive intelligence.
- `nguyen-ai-assessment-service` must not produce website projection or
  presentation artifacts.
- No repository may assume another repository's owned responsibility through
  direct integration.

Contract compatibility requirements:

- Cross-repository communication must use approved contracts.
- Contract consumers must accept only compatible contract versions.
- Contract producers own the meaning and validity of their produced contracts.
- Contract consumers must preserve the producer-defined meaning of consumed
  artifacts.

Version compatibility expectations:

- Integration boundaries must identify contract versions.
- Consumers must treat unknown, unsupported, or incompatible versions as
  invalid inputs.
- New contract versions must preserve explicit producer and consumer ownership.

Fail-closed behavior:

- Invalid, missing, unknown, or incompatible contract inputs must not be treated
  as valid.
- Failed contract compatibility must prevent downstream admission,
  derivation, or presentation.

## 7. Integration Boundaries

Allowed integration:

- contract-bound transfer of assessment truth from
  `nguyen-ai-assessment-service` to `executive-intelligence-platform`
- contract-bound transfer of website projections from
  `executive-intelligence-platform` to `nguyen-ai-website`
- architecture and ownership references from `nguyen-ai-platform` to the
  ecosystem
- downstream consumption that preserves upstream artifact meaning, lineage, and
  producer ownership

Prohibited integration:

- direct sharing of repository-owned business responsibility
- duplicated assessment logic outside `nguyen-ai-assessment-service`
- duplicated executive intelligence derivation outside
  `executive-intelligence-platform`
- website-side derivation of assessment truth or executive intelligence
- mutation of assessment truth outside `nguyen-ai-assessment-service`
- presentation ownership outside `nguyen-ai-website`
- runtime application behavior in `nguyen-ai-platform`

Ownership boundaries must remain intact so each platform output has one
authoritative producer, each consumer has a clear contract boundary, and every
downstream artifact can be explained from its upstream source.

## 8. Lineage Preservation

Lineage is preserved by maintaining explicit relationships between upstream
producer artifacts and downstream consumer artifacts.

Assessment truth originates in `nguyen-ai-assessment-service` and is carried
forward as an `ExecutiveAssessmentSnapshot`. The Executive Intelligence
Platform admits snapshots, produces executive intelligence artifacts, and emits
Website Projection Delivery Contracts while preserving traceability to the
admitted snapshot.

The website presents consumed projection contracts without replacing their
meaning or deriving new intelligence. This preserves lineage from website
presentation back to the Website Projection Delivery Contract, Executive
Projections, Executive Intelligence Package, admitted snapshot,
`ExecutiveAssessmentSnapshot`, and assessment truth.

## 9. Integration Invariants

The following integration invariants must not change without an approved
architectural decision:

- Repository ownership must be preserved across all integration boundaries.
- Integration must occur only through approved versioned contracts.
- `nguyen-ai-assessment-service` is the sole producer of assessment truth.
- `ExecutiveAssessmentSnapshot` is produced only by
  `nguyen-ai-assessment-service`.
- `executive-intelligence-platform` is the only consumer of
  `ExecutiveAssessmentSnapshot` in the canonical integration flow.
- Snapshot admission belongs to `executive-intelligence-platform`.
- Executive Intelligence Package production belongs to
  `executive-intelligence-platform`.
- Executive Projection production belongs to
  `executive-intelligence-platform`.
- Website Projection Delivery Contract production belongs to
  `executive-intelligence-platform`.
- Website Projection Delivery Contract consumption belongs to
  `nguyen-ai-website`.
- `nguyen-ai-website` must remain presentation only.
- `nguyen-ai-platform` must remain architecture and governance only.
- Assessment truth must remain immutable across downstream boundaries.
- Contract incompatibility must fail closed.
- End-to-end lineage must remain traceable across the full platform flow.
- Executive-facing outputs must remain explainable.
- Direct ownership violations are prohibited.
