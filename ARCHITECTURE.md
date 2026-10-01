# Reference Architecture — v0.1

Constitutional AI OS separates **what the system believes**, **what the system values**, **who has authority**, and **what the runtime can actually enforce**.

## 1. Layer model

```text
┌─────────────────────────────────────────────┐
│  Constitution                              │
│  principles · amendment · root authority   │
├─────────────────────────────────────────────┤
│  Rights & Ownership                        │
│  subjects · resources · grants · duties    │
├─────────────────────────────────────────────┤
│  AI Kernel                                 │
│  model · memory · context · scheduler       │
├─────────────────────────────────────────────┤
│  Policy Runtime                            │
│  evaluate · enforce · explain · audit       │
├─────────────────────────────────────────────┤
│  Agent Protocol                            │
│  identity · delegation · capability · A2A   │
├─────────────────────────────────────────────┤
│  World Model                               │
│  entities · relations · events · evidence   │
├─────────────────────────────────────────────┤
│  Action                                    │
│  software · finance · organization · robot  │
└─────────────────────────────────────────────┘
```

The layers are conceptually distinct even when an implementation combines them.

## 2. Constitution

The constitution is the root policy document.

It contains:

- principles;
- authority definitions;
- rights and prohibitions;
- ownership rules;
- amendment procedures;
- enforcement defaults;
- emergency procedures;
- provenance.

A constitution can contain prose, but its enforceable subset should be represented in machine-readable form.

## 3. Rights & Ownership

This layer answers:

- Who is the subject?
- What resource is involved?
- What action is being attempted?
- Who owns or controls the resource?
- What authority permits the action?
- What obligations accompany permission?

Resources may include data, memories, credentials, models, tools, money, compute, devices, robots, facilities, or generated outputs.

## 4. AI Kernel

The AI kernel manages scarce and sensitive agent resources:

- model access;
- context windows;
- memory;
- tool execution;
- credentials;
- compute budgets;
- task scheduling;
- communication channels.

The kernel is not itself the constitution. It is the execution substrate that exposes policy-relevant control points.

## 5. Policy Runtime

The policy runtime turns constitutional rules into decisions.

Reference flow:

```text
Agent intent
   ↓
Action request
   ↓
Identity + delegation chain
   ↓
Resource context
   ↓
Constitution / policy evaluation
   ↓
ALLOW | DENY | REQUIRE | ESCALATE
   ↓
Runtime enforcement
   ↓
Decision record + action receipt
```

A model saying "I should not do that" is not equivalent to enforcement.

For high-impact boundaries, policy should be checked by infrastructure outside the model process.

## 6. Agent Protocol

Agents need a standard way to communicate constitutional facts such as:

- stable identity;
- principal on whose behalf they act;
- delegated capabilities;
- scope and expiry;
- policy version;
- evidence requirements;
- revocation endpoint;
- action receipts.

The framework should be compatible with existing tool and agent protocols rather than require a proprietary network.

## 7. World Model

The world model represents claims about reality:

- entities;
- relations;
- events;
- state;
- time;
- evidence;
- uncertainty.

The constitution consumes these facts but should not confuse them with values.

Example:

```text
World model: "Machine M is in safety zone Z."
Constitution: "No autonomous motion is allowed in Z while a human is present."
Policy runtime: DENY motion command.
```

## 8. Physical and economic action

The same constitutional path should work for actions such as:

- send an email;
- modify a repository;
- spend money;
- sign a contract;
- operate machinery;
- move a robot;
- schedule labor;
- publish data.

The risk tier changes, but the authority chain should remain inspectable.

## 9. Core objects

v0.1 uses six core objects:

### Principal

A human, organization, legal entity, collective, or another constitutionally recognized authority.

### Agent

A software or embodied system capable of taking actions under delegated authority.

### Resource

Something over which access, ownership, custody, or control matters.

### Capability

A bounded authority to perform an action on a resource.

### Policy

A rule that evaluates an attempted action.

### Decision record

An immutable or tamper-evident explanation of how policy affected an action.

## 10. Trust boundaries

At minimum, implementations should distinguish:

1. **Model boundary** — model outputs are untrusted proposals, not direct authority.
2. **Tool boundary** — tools enforce scoped credentials and policy.
3. **Identity boundary** — agent identity and delegation must be authenticated.
4. **Data boundary** — data access is separate from data ownership.
5. **Physical boundary** — real-world actuators need independent safety interlocks.
6. **Constitution boundary** — policy changes require stronger authority than ordinary actions.

## 11. Constitutional boot sequence

A conforming implementation could boot in this order:

```text
1. Load constitution
2. Verify constitution signature / provenance
3. Resolve principals and authorities
4. Load policy modules
5. Initialize revocation state
6. Start AI kernel
7. Register agents and capabilities
8. Accept action requests
```

If the constitution cannot be loaded or verified, the runtime should enter a constitution-defined safe mode rather than silently operating without policy.

## 12. Minimal decision API

Conceptually:

```json
{
  "subject": "agent:planner-01",
  "principal": "human:alice",
  "action": "robot.move",
  "resource": "robot:arm-7",
  "context": {
    "zone": "assembly-a",
    "risk": "physical"
  }
}
```

Response:

```json
{
  "decision": "escalate",
  "rule_ids": ["physical.high-impact.human-approval"],
  "explanation": "Human approval is required for this action.",
  "policy_version": "0.1.0"
}
```

## 13. Design goal

The architecture should make this chain possible:

```text
human / community intent
→ constitutional text
→ machine-readable policy
→ runtime decision
→ enforced boundary
→ auditable outcome
```
