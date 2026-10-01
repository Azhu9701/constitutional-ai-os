# Agent Protocol

A constitutional AI OS should be able to govern agents built by different vendors or communities.

That requires portable constitutional metadata.

## Agent card extensions

A future constitutional agent descriptor could expose:

- agent ID;
- principal;
- constitution ID and version;
- capabilities;
- delegated scopes;
- expiry;
- revocation information;
- accepted evidence types;
- policy endpoint;
- receipt format.

## Delegation

Delegation should be explicit:

```text
Principal A
  delegates capability C
  to Agent B
  for Resource R
  under Conditions K
  until Time T
```

If Agent B delegates to Agent C, the new delegation must not exceed B's own authority.

## Constitutional downgrade

A central interoperability risk is constitutional downgrade:

Agent A delegates a task to Agent B, and B performs it under weaker rules.

Cross-agent protocols should therefore make policy boundaries visible before delegation is accepted.

## Goal

Agents should be able to ask each other not only:

> What can you do?

but also:

> Under whose authority will you do it, and under which constitution?
