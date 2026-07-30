# Repository Ownership Baseline v1

## 1. Purpose

Repository ownership exists to keep each Nguyen AI Platform responsibility in
one authoritative location.

Clear ownership boundaries make the platform maintainable by preventing
duplicated business logic, ambiguous producers, hidden derivation, and
cross-repository responsibility drift.

This baseline is the canonical ownership reference for determining where
platform responsibilities belong across the four-repository ecosystem.

## 2. Repository Ownership Principles

The Nguyen AI Platform ownership model is governed by these principles:

- Single responsibility: each repository owns one bounded platform role.
- Clear producer and consumer boundaries: every artifact has one authoritative
  producer and explicitly defined consumers.
- No duplicated business logic: business rules and derivation logic must remain
  in their owning repository.
- Deterministic ownership: ownership is determined by platform responsibility,
  not by convenience, presentation needs, or downstream demand.
- Architecture before implementation: repository ownership must be established
  architecturally before implementation work is assigned.
- Contract-mediated interaction: repositories interact through versioned
  contracts rather than shared internal responsibility.
- Fail-closed compatibility: incompatible contracts must not be treated as
  valid platform inputs.
- Lineage preservation: downstream artifacts must remain traceable to their
  upstream source artifacts.
- Presentation separation: presentation must not become assessment or executive
  intelligence production.

## 3. Repository Ownership Matrix

### `nguyen-ai-platform`

Primary purpose:

The architectural control plane for the Nguyen AI Platform ecosystem.

Owned responsibilities:

- platform architecture
- repository ownership baselines
- cross-repository integration boundaries
- architectural baselines
- architecture decision records
- governance documentation
- release coordination documentation

Produced artifacts:

- platform architecture documents
- repository ownership documents
- cross-repository integration references
- architecture decision records
- governance and release coordination documentation

Consumed artifacts:

- approved architecture inputs
- repository ownership inputs
- cross-repository integration requirements

External interfaces:

- architecture references for implementation repositories
- repository ownership references for platform contributors
- cross-repository contract boundary documentation

### `nguyen-ai-assessment-service`

Primary purpose:

The sole producer of assessment truth for the Nguyen AI Platform.

Owned responsibilities:

- assessment truth
- assessment methodology
- deterministic assessment execution
- business rules
- evidence processing
- decision engine behavior
- `ExecutiveAssessmentSnapshot` production

Produced artifacts:

- assessment truth outputs
- `ExecutiveAssessmentSnapshot` records

Consumed artifacts:

- assessment inputs
- assessment evidence
- assessment methodology definitions owned by the service

External interfaces:

- `ExecutiveAssessmentSnapshot` contract consumed by
  `executive-intelligence-platform`

### `executive-intelligence-platform`

Primary purpose:

The sole producer of executive intelligence for the Nguyen AI Platform.

Owned responsibilities:

- `ExecutiveAssessmentSnapshot` validation
- snapshot admission
- executive intelligence catalog behavior
- executive intelligence derivation
- Executive Intelligence Package production
- Executive Intelligence Projection production
- Website Projection Delivery Contract production

Produced artifacts:

- admitted snapshot records
- Executive Intelligence Packages
- Executive Intelligence Projections
- Website Projection Delivery Contracts

Consumed artifacts:

- `ExecutiveAssessmentSnapshot` records produced by
  `nguyen-ai-assessment-service`

External interfaces:

- snapshot admission boundary for `ExecutiveAssessmentSnapshot` inputs
- Website Projection Delivery Contract consumed by `nguyen-ai-website`

### `nguyen-ai-website`

Primary purpose:

The presentation layer for the Nguyen AI Platform.

Owned responsibilities:

- website presentation
- rendering
- user interaction
- Executive Dashboard UI
- consumption and presentation of Website Projection Delivery Contracts

Produced artifacts:

- website presentation output
- rendered Executive Dashboard experience
- user-facing website interactions

Consumed artifacts:

- Website Projection Delivery Contracts produced by
  `executive-intelligence-platform`

External interfaces:

- Website Projection Delivery Contract consumption boundary
- user-facing presentation surface

## 4. Explicit Ownership Exclusions

### `nguyen-ai-platform`

Must never own:

- production runtime application code
- runtime application behavior
- assessment truth
- assessment methodology execution
- evidence processing behavior
- decision engine behavior
- executive intelligence derivation
- Executive Intelligence Package production
- Executive Intelligence Projection production
- Website Projection Delivery Contract production
- website rendering
- website user interaction
- business logic owned by implementation repositories

### `nguyen-ai-assessment-service`

Must never own:

- platform architecture ownership
- platform governance ownership
- executive intelligence derivation
- Executive Intelligence Package production
- Executive Intelligence Projection production
- Website Projection Delivery Contract production
- website presentation
- website rendering
- website user interaction

### `executive-intelligence-platform`

Must never own:

- assessment truth production
- assessment methodology
- deterministic assessment execution
- business rules owned by `nguyen-ai-assessment-service`
- raw evidence mutation
- website presentation
- website rendering
- website user interaction
- platform architecture ownership
- platform governance ownership

### `nguyen-ai-website`

Must never own:

- platform architecture ownership
- platform governance ownership
- assessment truth
- assessment methodology
- assessment logic
- evidence processing
- decision engine behavior
- executive intelligence derivation
- Executive Intelligence Package production
- Executive Intelligence Projection production
- Website Projection Delivery Contract production

## 5. Producer / Consumer Relationships

The canonical ownership chain is:

1. `nguyen-ai-assessment-service` produces assessment truth.
2. Assessment truth is emitted as an `ExecutiveAssessmentSnapshot`.
3. `executive-intelligence-platform` consumes the
   `ExecutiveAssessmentSnapshot`.
4. `executive-intelligence-platform` validates and admits the snapshot.
5. `executive-intelligence-platform` produces executive intelligence artifacts.
6. `executive-intelligence-platform` emits the Website Projection Delivery
   Contract.
7. `nguyen-ai-website` consumes the Website Projection Delivery Contract.
8. `nguyen-ai-website` presents the website experience.

`nguyen-ai-platform` owns the architectural reference for this chain but does
not participate as a runtime producer or consumer in the chain.

## 6. Cross-Repository Interaction Rules

Cross-repository interaction is governed by these ownership rules:

- Repositories must not assume direct ownership of another repository's
  responsibilities.
- Cross-repository communication must occur only through approved versioned
  contracts.
- Producers own the meaning, structure, and validity of the artifacts they
  produce.
- Consumers may consume approved artifacts but must not recreate, reinterpret,
  or replace producer-owned responsibility.
- Contract consumers must respect version compatibility requirements.
- Contract incompatibility must fail closed.
- Downstream artifacts must preserve lineage to the upstream producer artifact.
- Ownership boundaries must remain explicit at every platform boundary.

## 7. Ownership Invariants

The following ownership invariants must not change without an approved
architectural decision:

- `nguyen-ai-platform` owns architecture and governance only.
- `nguyen-ai-platform` must not contain production runtime application code.
- `nguyen-ai-assessment-service` is the sole producer of assessment truth.
- `nguyen-ai-assessment-service` is the sole producer of
  `ExecutiveAssessmentSnapshot` records.
- `executive-intelligence-platform` is the sole producer of executive
  intelligence.
- `executive-intelligence-platform` is the sole producer of Website Projection
  Delivery Contracts.
- `nguyen-ai-website` is presentation only.
- `nguyen-ai-website` must consume Website Projection Delivery Contracts
  without deriving assessment truth or executive intelligence.
- Producer and consumer boundaries must remain separate.
- Versioned contract boundaries must remain explicit.
- Contract incompatibility must fail closed.
- Repository ownership must remain deterministic and immutable.
