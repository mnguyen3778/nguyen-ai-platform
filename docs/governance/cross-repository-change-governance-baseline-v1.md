# Cross-Repository Change Governance Baseline v1

## 1. Purpose and Scope

Cross-Repository Change Governance is the policy framework for proposing,
reviewing, approving, coordinating, and documenting changes that affect more
than one repository in the Nguyen AI Platform.

The purpose of Cross-Repository Change Governance is to ensure that
multi-repository changes preserve approved architecture, repository ownership,
bounded responsibilities, producer/consumer isolation, contract integrity,
immutable evidence, deterministic behavior, end-to-end lineage,
explainability, and human decision authority.

The scope of Cross-Repository Change Governance includes policy for governance
authority, cross-repository change principles, governed change scope, change
proposal, change review, change approval, cross-repository coordination,
change evidence, change decision categories, change stop conditions, document
ownership, and governance lifecycle.

Cross-Repository Change Governance Baseline v1 shall establish deterministic,
evidence-based governance for multi-repository changes without redefining
repository ownership, architecture, or implementation responsibilities.

This document defines governance policy only. It does not define development
workflows, Git branching strategies, CI/CD pipelines, runtime coordination,
deployment procedures, infrastructure, security architecture, APIs, schemas,
project management procedures, production code, or production implementation.

## 2. Governance Relationship

Cross-Repository Change Governance derives authority from Platform Governance
Baseline v1.

Cross-Repository Change Governance preserves repository boundaries under
Repository Governance Baseline v1.

Cross-Repository Change Governance preserves contract boundaries under Contract
Governance Baseline v1.

Cross-Repository Change Governance requires conformance evaluation under
Architecture Conformance Baseline v1.

Cross-Repository Change Governance requires release readiness alignment under
Release Governance Baseline v1 when a change proceeds toward release.

Cross-Repository Change Governance evaluates multi-repository changes against
approved architecture baselines, including:

- `docs/platform/platform-architecture-v1.md`
- `docs/platform/repository-ownership-v1.md`
- `docs/platform/platform-integration-baseline-v1.md`
- `docs/platform/system-context-baseline-v1.md`

Cross-Repository Change Governance must remain consistent with approved
governance baselines, including:

- `docs/governance/platform-governance-baseline-v1.md`
- `docs/governance/repository-governance-baseline-v1.md`
- `docs/governance/contract-governance-baseline-v1.md`
- `docs/governance/architecture-conformance-baseline-v1.md`
- `docs/governance/release-governance-baseline-v1.md`

Cross-Repository Change Governance does not supersede, redefine, or replace
approved architecture, repository ownership, contract governance, architecture
conformance, release governance, or implementation authorization.

## 3. Governance Authority

`nguyen-ai-platform` is the governing authority for cross-repository change
governance across the Nguyen AI Platform ecosystem.

The platform repository owns cross-repository change governance policy,
multi-repository change review expectations, change decision categories, change
governance stop conditions, and Cross-Repository Change Governance Baseline
document ownership.

Human decision authority is required for multi-repository change approval,
change rejection, change governance interpretation, change governance
supersession, and resolution of cross-repository change governance stop
conditions.

Cross-repository change governance authority is bounded by approved
architecture and approved governance. It may evaluate, approve, block, or
coordinate multi-repository change proposals at the policy level, but it must
not define implementation responsibilities, development workflows, operational
workflow, project management procedure, runtime behavior, or architectural
changes.

Repository autonomy is preserved within approved architecture and governance.
Repository autonomy does not authorize a repository to move responsibilities,
duplicate responsibilities, bypass approved governance, or alter another
repository's approved ownership boundary.

## 4. Cross-Repository Change Governance Principles

The following immutable principles govern cross-repository changes:

- Cross-repository changes preserve approved architecture.
- Cross-repository changes preserve repository ownership.
- Cross-repository changes preserve bounded responsibilities.
- Cross-repository changes preserve producer/consumer isolation.
- Cross-repository changes preserve contract integrity.
- Cross-repository changes are evidence-based.
- Cross-repository changes are deterministic.
- Cross-repository changes require explicit human approval.
- Cross-repository changes never bypass approved governance.
- Cross-repository changes preserve immutable evidence.
- Cross-repository changes preserve end-to-end lineage.
- Cross-repository changes preserve explainability.
- Cross-repository changes preserve versioned contracts.

## 5. Scope of Governed Changes

Cross-repository change governance applies to any proposed change that affects
more than one repository in the Nguyen AI Platform.

Governed changes include policy-level changes that affect:

- producer and consumer relationships
- approved repository boundaries
- approved cross-repository contract boundaries
- integration coordination between repositories
- architecture conformance across repositories
- release readiness across repositories
- lineage across repository boundaries
- fail-closed validation across repository boundaries
- explainability across repository boundaries

Cross-repository change governance does not apply to single-repository work
that remains fully within approved ownership boundaries and does not affect
another repository, contract boundary, integration boundary, conformance
decision, or release readiness decision.

Cross-repository change governance does not define implementation procedures,
development workflows, Git branching strategies, CI/CD pipelines, runtime
coordination, deployment procedures, infrastructure, security architecture,
APIs, schemas, project management procedures, or production implementation.

## 6. Change Proposal Policy

A proposed cross-repository change must identify one bounded responsibility.

A proposed cross-repository change must identify:

- affected repositories
- owning repository for each affected responsibility
- producer and consumer boundaries
- contract boundaries when applicable
- governing architecture baselines
- governing governance baselines
- expected preservation of lineage
- expected preservation of fail-closed validation
- expected preservation of deterministic behavior
- expected preservation of explainability
- explicit human approval requirement

A proposed cross-repository change must not rely on unsupported
interpretation, inferred implementation behavior, undocumented operational
state, or implementation assumptions as evidence for approval.

A proposed cross-repository change must be evaluated against approved
architecture, governance, ownership, contract, conformance, and release
baselines before approval when those baselines apply to the change.

## 7. Change Review Policy

Cross-repository change review must evaluate the proposed change against:

- Platform Architecture Baseline v1
- Repository Ownership Baseline v1
- Platform Integration Baseline v1
- Platform Governance Baseline v1
- Repository Governance Baseline v1
- Contract Governance Baseline v1 when contract boundaries are involved
- Architecture Conformance Baseline v1
- Release Governance Baseline v1 when release readiness is involved

Change review must verify:

- approved architecture is preserved
- approved repository ownership is preserved
- bounded responsibility is preserved
- producer and consumer isolation is preserved
- contract boundaries are preserved when applicable
- versioned contracts are preserved when applicable
- immutable evidence is preserved
- deterministic behavior is preserved
- end-to-end lineage is preserved
- explainability is preserved
- human decision authority is preserved
- governance stop conditions are absent

Change review must not introduce architecture, implementation guidance,
development workflow, runtime behavior, deployment procedure, or project
management procedure.

## 8. Change Approval Policy

Cross-repository change approval is a governance decision made under human
decision authority.

Change approval requires:

- one bounded responsibility
- identified affected repositories
- identified ownership boundaries
- identified producer and consumer boundaries
- identified contract boundaries when applicable
- completed governance review
- approved conformance path
- no active governance stop conditions
- explicit human approval

Change approval must not authorize:

- responsibility migration
- ownership duplication
- architectural responsibility overlap
- bypass of approved contract boundaries
- bypass of architecture conformance
- bypass of release governance when release readiness is involved
- implementation work outside approved repository ownership
- architectural change not reflected in an approved architectural baseline

## 9. Cross-Repository Coordination Policy

Cross-repository coordination must preserve approved architecture and approved
repository ownership.

Coordination may identify affected repositories, ownership boundaries,
producer and consumer boundaries, contract boundaries, conformance dependencies,
and release readiness dependencies.

Coordination must not move responsibility between repositories.

Coordination must not duplicate repository responsibilities.

Coordination must not authorize one repository to perform another repository's
owned responsibility.

Coordination must not bypass approved governance, architecture conformance, or
release readiness requirements.

Cross-repository coordination is policy-level only. It does not define
development workflows, project management procedures, runtime coordination,
deployment procedures, CI/CD pipelines, Git branching strategies, automation
tooling, or implementation procedure.

## 10. Change Evidence Requirements

Cross-repository change governance requires approved evidence sufficient to
support a deterministic change decision.

Change evidence may include policy-level references to:

- governing architecture baselines
- governing governance baselines
- affected repository list
- ownership boundary statement
- producer/consumer impact statement
- contract impact statement when applicable
- conformance evidence expectations
- release alignment expectations when applicable
- stop-condition assessment
- human approval status

Change Governance evaluates only approved governance evidence. Unsupported
interpretation, assumptions, inferred implementation behavior, undocumented
operational state, or implementation assumptions shall not be considered
evidence for cross-repository change approval.

Change evidence must be traceable to approved architecture, approved
governance, approved conformance expectations, approved release governance when
applicable, and explicit human approval.

Change evidence requirements are policy-level only. They do not define
technical checklists, development workflows, project management procedures,
tooling rules, runtime checks, deployment procedures, or implementation
procedures.

## 11. Change Decision Categories

Cross-repository change governance decisions must use one of the following
policy-level categories:

### `APPROVED FOR COORDINATION`

The proposed change is aligned with approved architecture and governance,
preserves one bounded responsibility, has sufficient approved evidence, has no
active stop condition, and has explicit human approval to proceed to
coordination.

### `APPROVED WITH RECOMMENDATIONS`

The proposed change is aligned with approved architecture and governance and
may proceed with explicit human approval. Non-blocking recommendations may be
identified, but they must not be required to preserve governance compliance.

### `NOT APPROVED`

The proposed change lacks required evidence, lacks explicit human approval,
violates approved architecture or governance, or has an active stop condition.

### `REQUIRES ARCHITECTURAL REVIEW`

The proposed change reveals a genuine architectural gap, ambiguity, or proposed
architectural change that cannot be resolved through existing approved
baselines.

### `REQUIRES GOVERNANCE CORRECTION`

The proposed change reveals a governance inconsistency, missing governance
evidence, incomplete governance review, or governance stop condition that must
be corrected before approval.

## 12. Change Governance Stop Conditions

Cross-repository change governance shall prohibit progression when any of the
following conditions are present:

- proposed change moves responsibility between repositories
- proposed change duplicates repository responsibility
- proposed change weakens producer/consumer isolation
- proposed change bypasses approved contract boundaries
- proposed change weakens versioned contracts
- proposed change weakens lineage
- proposed change weakens fail-closed validation
- proposed change weakens deterministic behavior
- proposed change weakens explainability
- proposed change modifies or obscures immutable evidence
- proposed change lacks explicit human approval
- proposed change combines multiple bounded responsibilities
- proposed change is not evaluated against approved architecture, governance,
  ownership, contract, conformance, and release baselines where applicable
- proposed change violates Repository Ownership Baseline v1
- proposed change violates Platform Integration Baseline v1
- proposed change violates Platform Governance Baseline v1
- proposed change violates Repository Governance Baseline v1
- proposed change violates Contract Governance Baseline v1
- proposed change violates Architecture Conformance Baseline v1
- proposed change violates Release Governance Baseline v1 when release
  readiness is involved
- proposed change introduces production runtime application code into
  `nguyen-ai-platform`

When a cross-repository change governance stop condition is present,
progression must stop until the condition is resolved through an approved
bounded responsibility consistent with approved architecture and governance.

## 13. Document Ownership

`nguyen-ai-platform` owns Cross-Repository Change Governance Baseline v1.

The document owner is responsible for preserving consistency with approved
architecture baselines, Platform Governance Baseline v1, Repository Governance
Baseline v1, Contract Governance Baseline v1, Architecture Conformance
Baseline v1, and Release Governance Baseline v1.

Cross-Repository Change Governance Baseline v1 must not be owned, modified, or
superseded by implementation repositories.

Document ownership does not authorize architecture changes, repository
ownership changes, contract implementation, implementation procedures,
development workflows, runtime coordination, deployment procedures,
infrastructure, security architecture, APIs, schemas, project management
procedures, or production implementation.

## 14. Cross-Repository Change Lifecycle

Proposal:

A cross-repository change begins as a proposed bounded responsibility affecting
more than one repository.

Initial governance review:

Initial governance review determines whether the proposed change is
cross-repository, whether it identifies one bounded responsibility, and whether
governance stop conditions are present.

Architecture review:

Architecture review determines whether the proposed change preserves approved
architecture or reveals a genuine architectural gap requiring architectural
review before progression.

Repository coordination:

Repository coordination identifies affected repositories, approved ownership
boundaries, producer and consumer boundaries, contract boundaries when
applicable, and required governance alignment.

Approval:

Approval requires completed applicable governance review, no active stop
conditions, and explicit human approval.

Release alignment:

Release alignment applies when a cross-repository change proceeds toward
release readiness. Release alignment must preserve Release Governance Baseline
v1 and must not imply release approval without required release governance.

Completion:

Completion confirms that the approved cross-repository bounded responsibility
has reached its governance-defined endpoint without introducing ownership,
architecture, contract, conformance, or release governance violations.

Governance closure:

Governance closure confirms that required governance evidence, decision
category, and human approval status are documented at the policy level.

This lifecycle defines governance policy only. It does not introduce
implementation guidance, operational workflow, project management procedure,
runtime behavior, or architectural changes.

## 15. Governance Lifecycle

Governance adoption:

Cross-Repository Change Governance Baseline v1 becomes the canonical
cross-repository change governance policy after architecture review confirms
consistency with approved architecture and governance baselines.

Governance use:

Cross-repository change governance policy is used to evaluate proposed,
approved, coordinated, and completed multi-repository changes against approved
architecture and governance.

Governance review:

Cross-repository change governance policy must be reviewed against approved
architecture and governance before it is used as an authoritative governance
baseline.

Governance revision:

Cross-repository change governance revisions must be bounded, policy-level, and
justified by an approved governance need or approved architectural change.

Governance supersession:

A future Cross-Repository Change Governance Baseline may supersede this
document only after approved governance review. Supersession must not redefine
architecture, repository ownership, contract boundaries, architecture
conformance, release governance, development workflows, operational workflows,
project management procedures, runtime behavior, or production implementation.

Governance retirement:

Cross-repository change governance documents may be retired only when
superseded by an approved governance document or when the governed scope is no
longer valid under approved architecture.

This lifecycle defines governance policy only. It does not introduce
implementation guidance, development workflows, operational workflow, project
management procedure, runtime behavior, or architectural changes.
