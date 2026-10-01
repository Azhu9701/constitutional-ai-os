# Policy Runtime

The policy runtime is where constitutional text becomes operational behavior.

## Decision types

v0.1 proposes four core outcomes:

- **ALLOW** — action may proceed.
- **DENY** — action must not proceed.
- **REQUIRE** — action may proceed only after a declared requirement is satisfied.
- **ESCALATE** — a designated authority must decide.

## Why external enforcement matters

Language models can reason about rules, but a model's self-restraint is not a security boundary.

For consequential actions:

```text
model intent ≠ authority
```

The runtime should independently validate authority before releasing:

- credentials;
- network access;
- file writes;
- payments;
- administrative operations;
- robot commands.

## Decision record

Each decision should be able to emit:

- request ID;
- subject / agent;
- principal;
- action;
- resource;
- decision;
- rule IDs;
- policy version;
- explanation;
- requirements;
- timestamp;
- audit metadata.

## Conflict handling

The constitution should define what happens when:

- two rules disagree;
- policy data is unavailable;
- world-state evidence is stale;
- the policy engine fails;
- emergency policy is invoked.

No silent fallback to unrestricted execution.
