# System Context Baseline v1

## 1. Purpose

The System Context Baseline defines the Nguyen AI Platform in relation to its
surrounding business and technical environment.

System context is important because the platform must distinguish internal
platform responsibilities from external actors, external systems, and external
sources of input or consumption.

This baseline complements the Platform Architecture Baseline v1 by defining the
platform boundary and external interactions at a conceptual architecture level.

## 2. Platform Boundary

The Nguyen AI Platform boundary contains the four platform repositories:

- `nguyen-ai-platform`
- `nguyen-ai-assessment-service`
- `executive-intelligence-platform`
- `nguyen-ai-website`

Inside the platform boundary:

- platform architecture and authoritative platform documentation are defined
- assessment truth is produced from assessment evidence
- executive intelligence is produced from admitted assessment outputs
- website presentation is produced from presentation-ready projection outputs
- platform outputs remain traceable to their originating evidence and producer
  artifacts

Outside the platform boundary:

- executive stakeholders
- business users
- assessment operators
- platform administrators
- client organizations
- external source evidence repositories
- external identity providers
- external cloud platform services
- external notification systems
- external reporting consumers

The architectural boundary separates platform-owned responsibilities from
external participants and services. External parties may provide inputs,
consume outputs, or support platform operation, but they do not own the
platform's internal assessment truth, executive intelligence, presentation, or
architecture responsibilities.

## 3. External Actors

### Executive Stakeholders

Executive stakeholders consume executive-facing platform outputs through the
website presentation surface.

They rely on the platform to provide explainable intelligence that remains
traceable to assessment truth and source evidence.

### Business Users

Business users interact with platform outputs to understand assessment-derived
business intelligence and related presentation views.

They consume platform information without owning assessment logic, executive
intelligence derivation, or platform architecture.

### Assessment Operators

Assessment operators provide or manage assessment inputs and source evidence
for assessment activity.

They interact with the platform at the assessment context boundary and do not
own downstream executive intelligence or website presentation.

### Platform Administrators

Platform administrators manage the platform operating context at a conceptual
level.

They may interact with platform context or operational coordination, but they
do not change repository ownership or redefine platform architecture through
operational activity.

### Client Organizations

Client organizations are the business entities whose evidence, assessments, or
executive-facing outputs may be represented by the platform.

They exist outside the platform boundary and interact with the platform through
bounded input and output relationships.

## 4. External Systems

### Source Evidence Repositories

Source evidence repositories may provide evidence or supporting materials used
as inputs to assessment activity.

They are external sources and do not produce platform assessment truth.

### Identity Providers

Identity providers may support actor identity context for platform access.

They are external systems and do not own platform business responsibilities or
internal platform artifacts.

### Cloud Platform Services

Cloud platform services may provide external operating context for platform
components.

They are outside the platform architecture boundary described by this baseline
and do not define repository responsibilities.

### Notification Systems

Notification systems may receive platform-originated notification context or
support delivery of platform-related messages.

They are external consumers or supporting systems and do not derive assessment
truth or executive intelligence.

### Reporting Consumers

Reporting consumers may consume executive-facing or business-facing outputs at
a conceptual boundary.

They are downstream consumers and do not own the production of assessment truth,
executive intelligence, or website presentation.

## 5. High-Level Platform Context

The platform receives assessment-related inputs from external actors and
external source systems at the platform boundary.

Within the platform boundary, assessment truth is produced, executive
intelligence is derived from admitted assessment outputs, and website
presentation exposes executive-facing information to external actors.

External actors and systems exchange information with the platform through
bounded input and output relationships. These exchanges must preserve the
platform's internal architectural boundaries, deterministic producer
responsibilities, fail-closed validation expectations, and end-to-end lineage.

The platform boundary ensures that external inputs do not become assessment
truth until processed by the appropriate platform producer, and external
consumption does not alter the meaning of platform-produced outputs.

## 6. Trust Boundaries

External actors exist outside the Nguyen AI Platform trust boundary.

External systems exist outside the Nguyen AI Platform trust boundary, even when
they provide inputs, support access context, or consume outputs.

The Nguyen AI Platform boundary separates external participants from internal
platform repositories and platform-owned artifacts.

Internal repositories have distinct trust boundaries from one another because
each repository owns a separate platform responsibility. Crossing an internal
repository boundary requires preservation of the producing repository's
artifact meaning, lineage, and version expectations.

Trust boundaries in this baseline identify where assumptions change between
external actors, external systems, the platform as a whole, and internal
repositories. This baseline does not define security controls.

## 7. Context Assumptions

The system context assumes:

- the Nguyen AI Platform remains a four-repository platform
- external actors interact with the platform through bounded input or output
  relationships
- external systems remain outside the platform boundary
- source evidence may originate outside the platform boundary
- assessment truth is produced only inside the platform boundary
- executive intelligence is produced only inside the platform boundary
- website presentation is produced only inside the platform boundary
- external consumers do not modify platform-produced artifacts
- platform outputs remain explainable and traceable to their source context

## 8. Context Constraints

The surrounding environment imposes these architectural constraints:

- external evidence cannot be treated as platform assessment truth before
  platform assessment production
- external consumers cannot redefine the meaning of platform outputs
- external systems cannot own platform repository responsibilities
- external actor needs cannot bypass internal platform boundaries
- internal repository boundaries must remain visible at the platform context
  level
- platform outputs must remain traceable across the platform boundary when
  presented to external actors or consumed by external systems
- incompatible or invalid external inputs must not be accepted as valid platform
  artifacts

## 9. Context Invariants

The following context invariants must remain true unless changed by an approved
architectural decision:

- the Nguyen AI Platform boundary contains the four platform repositories
- external actors remain outside the platform boundary
- external systems remain outside the platform boundary
- source evidence from outside the platform boundary is not assessment truth
  until produced as platform assessment truth
- executive-facing outputs must remain traceable to platform-produced artifacts
- external consumers must not alter the meaning of platform-produced outputs
- internal repository boundaries must remain distinct inside the platform
  boundary
- trust boundary descriptions must not redefine repository responsibilities
- context boundaries must preserve deterministic behavior, fail-closed
  validation, explainability, and end-to-end lineage
