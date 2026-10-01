# Glossary

This glossary defines the core vocabulary used by Constitutional AI OS.

## Agent

A software or embodied system capable of taking actions under delegated authority.

An agent is not assumed to be a legal person and is not automatically a source of legitimate authority.

## Principal

A human, organization, collective, role, or other constitutionally recognized source of authority.

## Constitution

The highest-level policy object that defines authority, rights, ownership, amendment, and enforcement defaults.

## Authority

Recognized power to make, delegate, revoke, approve, or amend decisions.

## Delegation

A transfer of bounded authority from one principal or agent to another.

Delegation should define scope, duration, conditions, and revocation.

## Capability

A concrete, bounded ability to perform an action on a resource.

Capabilities answer "what can this actor do?" They do not by themselves answer "is this use legitimate?"

## Right

A constitutional rule protecting or permitting a subject with respect to an action or resource.

## Obligation

A constitutional requirement that an actor must satisfy.

## Resource

Anything over which access, ownership, custody, control, or use may matter.

Examples include data, memory, credentials, models, tools, money, compute, robots, facilities, and generated outputs.

## Ownership

A declared relationship between a holder and a resource.

The framework distinguishes ownership from custody, access, control, operation, licensing, and beneficiary status.

## Policy

A rule that evaluates an attempted action.

## Policy Runtime

Infrastructure that evaluates policy independently of the model and returns a decision such as ALLOW, DENY, REQUIRE, or ESCALATE.

## Decision Record

A record explaining how a policy decision was reached, including the request, relevant rules, policy version, and outcome.

## Action Receipt

Evidence that an action was attempted or completed under a particular authority and policy version.

## World Model

A structured representation of claims about the world: entities, relations, events, state, time, evidence, and uncertainty.

A world model describes what is believed to be true. A constitution governs what may be done.

## Root Authority

The highest authority recognized by a constitution for a given scope.

Root authority must be explicit.

## Emergency Authority

Temporarily elevated authority for exceptional conditions.

It should be bounded, logged, expire automatically where possible, and require post-event review.

## Constitutional Downgrade

A failure mode in which an agent delegates work to another system governed by weaker constraints, thereby bypassing the original constitution.

## Fail Closed

A policy behavior in which inability to establish permission results in denial or safe mode rather than unrestricted execution.

## Enforceable Rule

A rule that runtime infrastructure can directly check and enforce.

## Auditable Rule

A rule that may not be preventable in real time but can be checked after the fact.

## Aspirational Rule

A guiding principle that requires human interpretation and cannot yet be mechanically enforced.

## Conformance

The degree to which an implementation satisfies the project's declared constitutional interfaces and runtime properties.
