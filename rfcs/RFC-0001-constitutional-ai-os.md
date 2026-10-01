# RFC-0001: Constitutional AI Operating System

- Status: Draft
- Version: 0.1
- Created: 2026-10-01
- Scope: Foundational architecture

## Summary

This RFC proposes an open constitutional layer for AI operating systems.

The central claim is:

> AI operating systems inevitably encode assumptions about authority, ownership, rights, governance, and acceptable action. Those assumptions should be explicit, inspectable, amendable, and executable.

## Motivation

Current AI agent stacks are rapidly gaining:

- memory;
- tool use;
- computer control;
- network access;
- multi-agent coordination;
- financial and organizational permissions;
- physical embodiment.

Most systems expose the capability layer before they expose the constitutional layer.

This creates a structural problem: the software can answer "how can the agent do this?" before users can answer "who authorized this, under what rule, with whose resources, and who can stop it?"

## Proposal

Introduce a constitutional layer with six primitives:

1. **Principal** — source of legitimate authority.
2. **Agent** — actor operating under delegated authority.
3. **Resource** — object of ownership, access, custody, or control.
4. **Capability** — scoped permission to act.
5. **Policy** — rule evaluating attempted action.
6. **Decision Record** — explanation and receipt for policy evaluation.

## Required constitutional questions

A constitution should make it possible to determine:

- who owns;
- who decides;
- who can override;
- who benefits;
- who bears cost;
- what an agent may do;
- how rules change.

## Separation of facts and norms

The architecture distinguishes:

```text
World Model = claims about what is true.
Constitution = rules about what may or should be done.
```

This separation is essential.

A system must not convert a prediction or database fact directly into authority.

## Enforcement model

Rules may be:

- enforceable;
- auditable;
- aspirational.

For enforceable rules, the preferred pattern is external policy enforcement:

```text
model proposes action
→ runtime evaluates policy
→ infrastructure allows / denies / escalates
→ receipt is recorded
```

## Non-goals

RFC-0001 does not:

- define one universal ideology;
- grant legal personhood to AI agents;
- replace laws or safety standards;
- solve every ethical question with code;
- require one model provider or agent framework.

## Compatibility

The constitutional layer should be implementable above existing operating systems and alongside existing agent and tool protocols.

## Security considerations

A constitutional system creates new high-value attack surfaces:

- constitution replacement;
- authority forgery;
- delegation escalation;
- stale revocation state;
- policy-engine bypass;
- forged world-state evidence;
- emergency-override abuse.

The constitution itself must therefore be treated as security-sensitive configuration.

## Open questions

1. What is the minimum interoperable principal identity format?
2. How should conflicting constitutions negotiate?
3. What rules belong in the universal core versus deployment profiles?
4. How should physical safety systems relate to constitutional policy?
5. Which constitutional records require cryptographic attestation?
6. How do collective or commons-owned resources map to ownership primitives?
7. When should a runtime fail closed versus escalate?

## Acceptance criteria

RFC-0001 is considered implemented when:

- the core schemas exist;
- at least three distinct example constitutions validate;
- a reference policy request can be evaluated;
- the output names the rule and authority behind the decision;
- a denied action cannot be converted into permission by model text alone.
