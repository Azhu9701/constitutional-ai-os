# Roadmap

The project should move deliberately from **language → schema → evaluator → enforcement → real systems**.

## v0.1 — Make the hidden constitution visible

Status: **in progress**

Goals:

- establish vocabulary;
- publish the draft project constitution;
- define the reference architecture;
- define initial JSON Schemas;
- publish example constitutions;
- open an RFC process;
- distinguish enforceable, auditable, and aspirational rules.

Exit condition:

> A person can describe an AI system's authority, ownership, rights, amendment process, and enforcement defaults in a machine-readable constitution.

## v0.2 — Policy decision model

Build a small reference evaluator.

Goals:

- normalized action request;
- ALLOW / DENY / REQUIRE / ESCALATE decisions;
- rule precedence;
- delegation chains;
- revocation;
- human approval hooks;
- decision receipts;
- deterministic tests.

Exit condition:

> The same request evaluated under the same constitution produces an explainable policy decision.

## v0.3 — Runtime adapters

Connect the constitutional layer to real agent systems.

Candidate adapters:

- local shell / process sandbox;
- file system;
- HTTP / network access;
- tool protocols;
- agent-to-agent messaging;
- secret and credential brokers.

Exit condition:

> At least one real agent runtime cannot bypass a constitutional denial through ordinary model output.

## v0.4 — Identity, delegation, and attestations

Goals:

- principal identifiers;
- agent identifiers;
- capability tokens;
- scoped delegation;
- expiry and revocation;
- signed policy version;
- action receipts.

Exit condition:

> A third party can verify who authorized an agent to perform a consequential action and which constitution governed it.

## v0.5 — World model and evidence

Goals:

- provenance-aware claims;
- evidence requirements by risk tier;
- uncertainty representation;
- policy conditions driven by world state;
- separation of facts from norms.

Exit condition:

> A policy can depend on a traceable claim about the world without treating that claim as unquestionable truth.

## v0.6 — Physical production profile

Goals:

- robot capability model;
- safety zones;
- physical interlocks;
- human approval boundaries;
- production resource ownership;
- shutdown and emergency procedures;
- labor-impact declarations.

Exit condition:

> A robot action can be authorized through the same constitutional chain as a software action while respecting independent physical safety controls.

## v0.7 — Multi-constitution federation

Goals:

- constitution discovery;
- conflict detection;
- cross-agent delegation;
- minimum shared constraints;
- federation receipts;
- constitutional negotiation without silent downgrade.

Exit condition:

> Two agents governed by different constitutions can identify policy conflicts before action.

## v1.0 — Conformance

Goals:

- stable core schema;
- test suite;
- reference runtime;
- threat model;
- governance maturity;
- implementation profiles;
- conformance levels.

Proposed conformance levels:

1. **Declared** — constitution is machine-readable.
2. **Auditable** — consequential actions emit decision records.
3. **Enforced** — runtime boundaries enforce declared policy.
4. **Attested** — identity, policy version, and action receipts are independently verifiable.

## Research tracks

Parallel questions that may not fit the main release path:

- constitutional inheritance;
- collective ownership models;
- constitutions for autonomous organizations;
- constitutional memory;
- agent rights versus agent permissions;
- constitutional conflict across jurisdictions;
- governance of self-modifying agents;
- economic allocation and automation dividends;
- constitutional interfaces for robots;
- constitutional simulation before deployment.
