# Runtime Owner Assignment Governance v1

## 1. Purpose and Scope

This document formally assigns the repository ownership domain permitted to host
the future deterministic trusted logical runtime for governed Website delivery.

Owner repository:

- `/Users/aiadmin/aws-ai-knowledge-assistant`

Logical responsibility:

- separate deterministic trusted logical service

This is a repository and logical service ownership decision only. It is not
runtime implementation authorization.

This document does not create the logical service, implement runtime behavior,
select persistence, select transport, define an API, modify infrastructure,
implement authorization, implement EIP retrieval, modify the Website, modify
the Assessment Service, modify the Executive Intelligence Platform, or change
AI behavior.

## 2. Ownership Decision

Governance owner:

- `nguyen-ai-platform`

Trusted runtime repository owner:

- `aws-ai-knowledge-assistant`

Trusted runtime logical service:

- separate deterministic trusted service boundary

AI Knowledge Assistant:

- separate consumer and explainer capability within the same repository
  ownership domain

Same repository does not mean same logical service.

Same repository does not mean same authority.

Same repository does not make the AI Knowledge Assistant the authorization
authority, retrieval authority, Assessment Service truth producer, or Executive
Intelligence Platform producer.

## 3. Evidence Basis

The runtime-owner review inspected `/Users/aiadmin/aws-ai-knowledge-assistant`
at commit `e2c16a8`, tagged
`ai-knowledge-assistant-production-readiness-v1.0.0`.

Objective evidence supporting this ownership assignment includes:

- documented API Gateway and Lambda runtime foundations
- documented Cognito-protected server-side boundary
- Lambda request handling in `src/lambda_function.py`
- explicit routing for `/v1/assistant`
- explicit routing for `/assessment`
- deterministic runtime provider support in `src/assistant_runtime/provider.py`
- runtime provider dispatch under `src/assistant_runtime/`
- Bedrock provider isolation behind the runtime provider interface
- default deterministic runtime behavior when Bedrock is not selected
- documented CloudFront and WAF production boundary
- documented CloudWatch, alarms, and SNS operational foundations
- documented DynamoDB conversation-history capability
- versioned service contract governance under `docs/contracts/`
- evidence that the repository can host multiple bounded runtime paths

The evidence distinguishes implemented source behavior from documented
operational foundations. Existing documentation for DynamoDB, CloudFront, WAF,
Cognito, API Gateway, Lambda, CloudWatch, alarms, and SNS is evidence of an AWS
runtime ownership domain, not authorization to modify or reuse those
capabilities for this governed delivery service.

## 4. Trusted Service Responsibility

After later governance authorizes implementation, the separate deterministic
trusted logical service MAY be responsible for:

- trusted server-side request handling
- verified identity context
- separately governed principal and resource authorization enforcement
- governed EIP retrieval consumption
- contract and version validation
- fail-closed governed resource delivery
- Website-facing deterministic APIs
- audit and observability
- resource isolation

These are responsibility boundaries only. This document does not authorize
implementation of any listed capability.

## 5. Assessment Service Protection

The Assessment Service remains the sole deterministic assessment business-truth
producer.

The trusted runtime MUST NOT:

- score assessments
- aggregate dimensions
- weight dimensions
- determine readiness
- determine severity
- determine risk
- determine confidence
- create recommendations
- generate authoritative executive summaries
- implement assessment methodology
- duplicate Assessment Service logic
- reinterpret Assessment Service truth

The existing AWS repository's local `/assessment` behavior does not grant
Assessment Service ownership.

Future integration with assessment behavior MUST consume or proxy the certified
Assessment Service through separately governed contracts.

## 6. EIP Protection

The Executive Intelligence Platform remains the authoritative producer of
governed executive intelligence and
`website-projection-delivery-contract-v1`.

The trusted runtime MUST NOT:

- derive executive intelligence
- reconstruct EIP projections
- alter publication state
- alter eligibility
- alter freshness
- alter lineage
- alter classification
- fabricate delivery contracts
- repair rejected EIP artifacts

The trusted runtime MAY only consume EIP output through the approved governed
retrieval boundary after implementation is separately authorized.

## 7. Website Protection

The Website remains presentation-only.

The trusted runtime does not move authoritative authorization into the browser.

Website and browser identifiers remain non-authoritative unless a server-side
authority independently validates them.

The Website MUST consume only authorized governed output.

## 8. AI Knowledge Assistant Separation

The AI Knowledge Assistant is not the Trusted Deterministic Service.

Even though both may live in the same repository ownership domain, the AI
Knowledge Assistant remains:

- consumer
- explainer
- conversational interface

The AI Knowledge Assistant MUST NOT:

- authorize principals
- decide membership
- decide entitlement
- choose authoritative resources
- compute Assessment Service truth
- derive EIP intelligence
- override deterministic authorization
- repair missing governed data
- become fallback business logic

## 9. Bedrock / Model Isolation

Trusted deterministic operations MUST NOT depend on Bedrock or model execution.

At minimum:

- identity verification MUST NOT depend on LLM output
- membership decisions MUST NOT depend on LLM output
- entitlement decisions MUST NOT depend on LLM output
- client or resource authorization MUST NOT depend on LLM output
- EIP retrieval selection MUST NOT depend on LLM output
- contract validation MUST NOT depend on LLM output
- fail-closed behavior MUST NOT depend on LLM output

AI invocation MAY occur only downstream of deterministic controls when
separately authorized.

## 10. Logical Service Isolation

The trusted runtime MUST be a separate logical service boundary from existing
assistant and model execution behavior.

This document does not prescribe implementation topology.

This document does not require:

- separate Lambda
- separate API Gateway
- separate repository
- separate deployment
- separate process

unless later governance selects those boundaries.

Logical isolation is established through responsibility, authority, contract,
routing, and fail-closed behavior.

## 11. Authentication vs Authorization

Cognito authentication exists as evidence that the AWS repository can operate
behind a trusted server-side authentication boundary.

Authentication is not resource authorization.

Runtime-owner assignment MUST NOT be interpreted as proof that Nguyen AI
principal, membership, entitlement, client, engagement, workspace, or resource
authorization authority exists.

Those authorities remain separately governed prerequisites.

## 12. Retrieval vs Authorization

EIP retrieval is not principal authorization.

The trusted runtime MAY eventually host both enforcement stages, but they MUST
remain logically distinct controls.

Successful retrieval MUST NOT imply entitlement.

Successful authentication MUST NOT imply entitlement.

## 13. Principal / Membership / Entitlement Status

The current governed state remains:

- Nguyen AI principal model: unresolved
- principal mapping: unresolved
- membership authority: unresolved
- entitlement authority: unresolved
- client authorization: unresolved
- engagement authorization: unresolved
- workspace authorization: unresolved
- resource authorization: unresolved

This document does not design schemas, storage, policy engines, or data models
for those authorities.

## 14. EIP Integration Status

EIP integration is currently absent from the AWS repository.

This ownership assignment means the repository is permitted to host a future
governed EIP consumer service.

It does not mean EIP integration currently exists.

It does not authorize implementation of EIP integration.

## 15. Existing /Assessment Constraint

The AWS repository currently contains local `/assessment` behavior that is not
the certified Assessment Service producer integration.

That behavior MUST NOT become the authoritative assessment path through this
ownership assignment.

This increment does not modify, remove, replace, or reconcile the local
`/assessment` behavior.

Future reconciliation requires separate architecture review where applicable.

## 16. Legacy Bedrock Routing Constraint

Legacy unmatched routes may currently invoke Bedrock.

This does not invalidate repository ownership because deterministic route
separation exists.

The future trusted logical service MUST use explicit deterministic routing and
MUST NOT fall through into legacy Bedrock or model execution.

This increment does not modify routing.

## 17. Persistence Non-Assignment

Existing DynamoDB conversation-history documentation or capability does not
authorize reuse for:

- principal authority
- membership
- entitlement
- EIP artifacts
- governed delivery
- assessment artifacts

Persistence technology and persistence authority remain separately governed.

This document does not select DynamoDB, S3, SQL, filesystem storage, cache,
queue, event bus, or any other persistence or transport mechanism.

## 18. Security / Trust Boundary

The AWS repository is an appropriate ownership domain because it already
evidences a trusted AWS server-side boundary with capabilities such as Cognito,
API Gateway, Lambda, and production security and operations foundations.

This ownership assignment does not automatically authorize changes to:

- Cognito
- IAM
- WAF
- CloudFront
- API Gateway
- Lambda
- logging
- alarms
- persistence

Those remain implementation decisions requiring later governance and approval.

## 19. Fail-Closed Requirement

Future trusted service implementation MUST fail closed for missing or invalid:

- authentication evidence
- verified principal
- membership
- entitlement
- client scope
- engagement scope
- workspace scope
- resource scope
- EIP artifact
- publication state
- freshness
- lineage
- classification
- compatibility or version
- retrieval authority

Failure MUST NOT cause:

- AI fallback
- synthetic governed delivery
- previous-client fallback
- default-client fallback
- cross-resource substitution
- fabricated executive intelligence

## 20. Repository vs Service Ownership

Repository ownership:

- `aws-ai-knowledge-assistant`

Logical service ownership:

- deterministic trusted service

AI logical service:

- AI Knowledge Assistant

This governance decision deliberately allows multiple bounded logical services
in one repository ownership domain.

This decision does not authorize a monolith or god service.

## 21. God-Service Prevention

The trusted runtime MUST NOT absorb:

- Assessment Service methodology
- EIP derivation
- Website presentation
- AI model authority
- governance authority
- unrelated business logic

Repository reuse is justified by trusted AWS runtime cohesion, not by
centralizing all platform behavior.

## 22. Contract Boundaries

Future implementation MUST consume governed and versioned contracts.

At minimum, future implementation MUST preserve:

- Assessment Service contracts
- EIP `website-projection-delivery-contract-v1`
- future trusted service API contract
- Website consumer contract

This ownership artifact does not modify any existing contract.

## 23. Implementation Prerequisites

Before implementation may be authorized, the following governance gates remain:

1. Principal / Membership / Entitlement Authority Model v1
2. trusted deterministic service responsibility and authority boundary if
   further detail is required
3. API/service contract governance
4. EIP retrieval mechanism selection
5. stable resource and artifact lookup semantics
6. authorization-state authority
7. persistence decision if required
8. audit and observability requirements
9. IAM and security boundary
10. Website integration contract
11. explicit deterministic route isolation from AI and Bedrock
12. Assessment Service integration or reconciliation review where applicable

This document does not resolve those gates.

## 24. Implementation Gate

THIS RUNTIME OWNER ASSIGNMENT DOES NOT AUTHORIZE IMPLEMENTATION.

It does not authorize:

- creation of the logical service
- source-code changes
- endpoint creation
- API Gateway changes
- Lambda changes
- Cognito changes
- IAM changes
- WAF changes
- CloudFront changes
- DynamoDB changes
- S3
- persistence
- EIP integration
- Assessment Service integration
- authorization implementation
- principal mapping
- membership implementation
- entitlement implementation
- Website changes
- Bedrock changes
- AI changes
- deployment

No implementation may begin from this ownership assignment alone.

## 25. Acceptance Criteria

This governance increment passes only if:

- owner repository is explicitly assigned
- logical service is explicitly separate from AI Knowledge Assistant
- deterministic non-AI operation is required
- Assessment Service authority is preserved
- EIP authority is preserved
- Website remains presentation-only
- AI remains consumer and explainer
- authentication remains distinct from authorization
- retrieval remains distinct from authorization
- principal, membership, and entitlement remain unresolved
- EIP integration remains explicitly absent
- persistence remains unselected
- legacy Bedrock fallthrough is identified as a constraint
- local `/assessment` behavior is identified as non-authoritative
- implementation remains unauthorized
