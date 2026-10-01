# Constitution Layer

The constitution is the highest-level policy object in the system.

It does not need to contain every low-level rule. It defines the source of authority from which lower-level rules derive.

## A constitution should contain

### Identity

- constitution name;
- version;
- issuer;
- effective time;
- provenance.

### Scope

- which agents;
- which resources;
- which environments;
- which jurisdictions or organizations, if relevant.

### Principles

Human-readable normative statements.

### Authorities

Who may:

- grant capabilities;
- revoke capabilities;
- approve high-impact actions;
- amend the constitution;
- invoke emergency powers.

### Rights and prohibitions

Rules that protect or constrain subjects.

### Ownership

Rules describing ownership, custody, access, control, and transfer.

### Amendment

How the constitution changes.

### Enforcement defaults

What happens when policy is missing, ambiguous, unavailable, or conflicting.

## Constitutional precedence

A future implementation should support explicit precedence instead of relying on prompt order.

Example:

```text
constitutional prohibition
> constitutional grant
> organization policy
> task delegation
> agent preference
```

The exact hierarchy may differ by constitution, but it must be declared.

## No prompt-based root access

Ordinary natural-language instructions should not be able to silently amend the constitution.

A constitutional amendment is a governance event, not merely another message in the context window.
