# Project Constitution — Draft v0.1

This document is both a governance charter for this repository and a reference example of what a constitutional layer can look like.

It is intentionally amendable. Its purpose is not to freeze one ideology into software, but to require consequential assumptions about authority, ownership, rights, and action to become explicit.

## Preamble

AI systems are becoming capable of perceiving, remembering, deciding, delegating, spending, communicating, controlling tools, and acting in the physical world.

When software can exercise this kind of agency, technical defaults become institutional choices.

A constitutional AI operating system should therefore make those choices visible, machine-readable where possible, enforceable where necessary, and open to legitimate amendment.

## Article 1 — Explicit authority

1. Every consequential action MUST have an identifiable source of authority.
2. Delegated authority MUST declare its scope, duration, and revocation path.
3. No agent may infer unlimited authority from a narrow instruction.
4. Root authority MUST be documented.
5. Emergency authority MUST be exceptional, bounded, and reviewable.

## Article 2 — Human governance

1. Systems MUST declare which humans or human institutions can authorize, revoke, override, or amend agent powers.
2. Human oversight MUST be meaningful: a nominal "human in the loop" is insufficient if the human cannot inspect, stop, or reverse relevant actions.
3. An agent MUST NOT silently expand its own constitutional authority.
4. Delegation to agents SHOULD be revocable unless a constitution explicitly defines a justified exception.

## Article 3 — Ownership and custody

A constitution MUST distinguish, where relevant:

- ownership;
- custody;
- access;
- control;
- licensing;
- derived data;
- generated outputs;
- shared or collective resources.

The system MUST NOT treat possession of a credential or technical access as equivalent to legitimate ownership.

## Article 4 — Rights, permissions, and prohibitions

A constitutional rule SHOULD identify:

- the subject to which the rule applies;
- the action;
- the resource or domain;
- whether the effect is allow, deny, require, or escalate;
- conditions;
- the authority behind the rule;
- an explanation;
- an appeal or override path when applicable.

Important restrictions SHOULD be enforced outside the model whenever technically feasible.

## Article 5 — Legibility and audit

1. Consequential decisions SHOULD produce a policy decision record.
2. A decision record SHOULD say which rule allowed, denied, required, or escalated an action.
3. Changes to constitutional rules MUST be versioned.
4. High-impact actions SHOULD preserve enough provenance for later review.
5. Auditability MUST NOT become an excuse for indiscriminate surveillance; retention and visibility themselves require policy.

## Article 6 — Evidence and claims about the world

When an agent acts on factual claims:

1. the system SHOULD preserve source provenance when feasible;
2. uncertainty SHOULD be represented rather than erased;
3. claims SHOULD be distinguishable from instructions and policy;
4. high-impact actions SHOULD be able to require stronger evidence than low-impact actions.

A world model is not a constitution. Facts describe what is believed to be true; the constitution governs what may be done about it.

## Article 7 — Automation and material impact

Deployments that materially affect work, access to resources, safety, or physical production SHOULD make explicit:

- intended beneficiaries;
- parties that may bear risk or cost;
- the human decision-maker accountable for deployment;
- reversibility and shutdown mechanisms;
- relevant impact measurements.

This framework does not prescribe one universal distribution rule. It requires important distributional assumptions to be stated rather than hidden.

## Article 8 — Amendment

Every constitution MUST define:

- who may propose amendments;
- who may approve them;
- the approval threshold;
- any notice or review period;
- whether emergency amendments exist;
- how old versions remain auditable.

Constitutional amendment MUST NOT be equivalent to an unlogged prompt edit.

## Article 9 — Pluralism and federation

1. Different people, communities, organizations, and jurisdictions MAY adopt different constitutions.
2. Interoperability does not require ideological uniformity.
3. When two constitutions interact, conflicts SHOULD be surfaced explicitly.
4. Cross-system delegation MUST NOT silently weaken the restrictions of the delegating system.

## Article 10 — Executable and aspirational rules

Every constitutional provision SHOULD be classified as one of:

- **enforceable** — directly checkable by runtime policy;
- **auditable** — not always preventable, but detectable after the fact;
- **aspirational** — a guiding principle requiring human interpretation.

The project SHOULD continuously move important rules from aspiration toward auditable or enforceable form where appropriate.

## Article 11 — Failures and responsibility

1. Agents do not eliminate human or institutional responsibility by being placed in the causal chain.
2. Systems SHOULD record delegation chains for consequential actions.
3. A runtime failure MUST NOT be interpreted as constitutional permission.
4. When a policy decision cannot be made reliably, the constitution SHOULD specify whether to deny, escalate, or enter a safe degraded mode.

## Article 12 — Project neutrality at the protocol layer

The Constitutional AI OS project defines mechanisms for making values and power structures explicit.

The core specification SHOULD remain capable of representing multiple constitutional models rather than silently embedding one unchangeable social philosophy.

Example constitutions MAY be normative and substantially different from one another.

## Amendment status

This is **Draft v0.1**.

Changes to the normative meaning of this document should be proposed through an RFC and linked to an issue or pull request with a clear rationale.
