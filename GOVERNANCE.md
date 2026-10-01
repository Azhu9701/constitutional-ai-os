# Project Governance

Constitutional AI OS is an open specification and implementation project.

The governance model should reflect the project thesis: important power should be visible, scoped, reviewable, and amendable.

## Principles

### Open discussion

Major changes should be discussed in public issues or RFCs.

### Traceable authority

Maintainer powers should be visible in repository permissions and documented here rather than treated as informal mystery authority.

### Separation of mechanism and example constitutions

The core project defines mechanisms that can represent multiple constitutional models.

Example constitutions may express stronger normative positions, but they must not silently become protocol requirements.

### Rough consensus, explicit disagreement

Consensus is preferred, but unresolved disagreement should be recorded rather than erased.

Competing RFCs and example constitutions are welcome.

## Change classes

### Class A — editorial

Typos, wording clarification, examples, and non-normative documentation.

A normal pull request is sufficient.

### Class B — compatible specification change

Adds fields or behavior without invalidating existing conforming constitutions.

Requires:

- issue or RFC;
- maintainer review;
- compatibility note.

### Class C — constitutional or breaking change

Changes normative meaning, root governance, required semantics, or compatibility.

Requires:

- RFC;
- public review period;
- migration plan;
- explicit approval from project maintainers;
- version increment.

## RFC lifecycle

```text
Draft
  ↓
Discussion
  ↓
Accepted | Rejected | Withdrawn
  ↓
Implementation
  ↓
Stabilized
```

RFC numbers are permanent and must not be reused.

## Amendments to this project's Constitution

A change to CONSTITUTION.md that alters normative meaning should:

1. identify the affected articles;
2. explain the reason;
3. describe foreseeable implementation impact;
4. describe alternatives considered;
5. state whether the change is breaking.

## Maintainers

The initial repository owner acts as bootstrap maintainer.

As participation grows, this file should be amended to define:

- maintainer admission;
- maintainer removal;
- voting or consensus rules;
- conflict-of-interest handling;
- release authority;
- security response authority.

The bootstrap phase should not be mistaken for a permanent governance model.

## Versioning

Specification versions use semantic-style version numbers:

- patch: editorial clarification;
- minor: compatible normative extension;
- major: breaking semantic or governance change.

Pre-1.0 versions may make larger changes, but breaking changes must still be documented.

## Security-sensitive changes

Changes involving:

- credential handling;
- physical actuation;
- authentication;
- policy bypass;
- emergency override;
- cryptographic identity;
- secret storage

should receive additional security review before being described as production-ready.
