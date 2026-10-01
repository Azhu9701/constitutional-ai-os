# Threat Model — Draft v0.1

A constitutional layer becomes a high-value target because it controls the authority boundary around AI agents.

This document lists the first threat classes the project should design against.

## Security goals

A conforming runtime should aim to preserve:

1. **constitutional integrity** — the active constitution cannot be silently replaced;
2. **authority integrity** — actors cannot forge or enlarge delegated authority;
3. **decision integrity** — policy decisions reflect the active constitution;
4. **enforcement integrity** — denied actions cannot bypass the policy runtime;
5. **provenance integrity** — important decisions can be traced to policy version and authority;
6. **revocation integrity** — revoked authority stops working within the declared window;
7. **world-state integrity** — high-impact policy does not rely on trivially forgeable facts.

## Threat actors

Potential attackers include:

- an external attacker;
- a compromised agent;
- a malicious tool;
- a malicious or careless administrator;
- a delegated agent exceeding scope;
- a compromised model provider;
- a compromised policy service;
- an insider with valid credentials;
- another constitutional domain attempting downgrade.

## T1 — Constitution replacement

**Attack:** replace the active constitution with a weaker version.

Mitigations:

- versioned constitutions;
- signatures or attestations;
- explicit amendment authority;
- immutable history;
- startup verification;
- visible active-version reporting.

## T2 — Prompt-level constitutional override

**Attack:** natural-language instructions claim to supersede policy.

Mitigations:

- constitution outside the model context as an enforcement artifact;
- tool and credential release controlled by policy runtime;
- no prompt-based root access.

## T3 — Delegation escalation

**Attack:** an agent delegates more authority than it received.

Mitigations:

- parent delegation references;
- capability intersection;
- expiry;
- revocation;
- non-delegable capabilities.

## T4 — Ambient authority

**Attack:** an agent gains access simply because credentials or tools are present in its process.

Mitigations:

- scoped capabilities;
- brokered credentials;
- per-action authorization;
- least ambient privilege.

## T5 — Policy-engine bypass

**Attack:** call the underlying tool, API, file, or robot directly.

Mitigations:

- place enforcement at the real resource boundary;
- isolate raw credentials;
- separate model and executor processes;
- test bypass paths explicitly.

## T6 — Stale revocation

**Attack:** revoked authority continues to work due to caches or disconnected systems.

Mitigations:

- short-lived grants for high-impact actions;
- revocation epochs;
- bounded cache TTL;
- fail-safe offline behavior.

## T7 — Constitutional downgrade across agents

**Attack:** delegate work to a weaker system to evade restrictions.

Mitigations:

- advertise constitution ID/version;
- propagate delegation constraints;
- reject incompatible downstream policy;
- emit federation receipts.

## T8 — Forged world state

**Attack:** manipulate facts used by policy, such as falsely reporting that a safety zone is empty.

Mitigations:

- evidence requirements by risk;
- trusted sensors for physical safety;
- source provenance;
- freshness rules;
- multi-source confirmation where appropriate.

## T9 — Emergency-power abuse

**Attack:** emergency override becomes a permanent backdoor.

Mitigations:

- narrow scope;
- automatic expiry;
- explicit authority;
- mandatory logging;
- post-event review;
- no silent emergency mode.

## T10 — Audit tampering

**Attack:** delete or rewrite records after a consequential action.

Mitigations:

- append-oriented logs;
- remote or independent replication where appropriate;
- hashes / signatures for high-impact receipts;
- retention rules governed by policy.

## T11 — Surveillance through audit

**Attack:** use "auditability" as justification to retain unnecessary personal or sensitive data.

Mitigations:

- data minimization;
- retention policy;
- visibility policy;
- separation between decision evidence and full content capture.

## T12 — Self-amendment

**Attack:** an agent changes the rules governing itself.

Mitigations:

- constitutional amendment is a separate privileged operation;
- model output cannot directly modify active policy;
- amendments require declared human or institutional authority.

## Physical systems

For robots and industrial control, constitutional enforcement must not replace independent safety systems.

A constitutional ALLOW is not a safety certification.

The final action path should be able to require both:

```text
constitutional authorization
AND
independent physical safety approval
```

## Open threat-model questions

- Which policy artifacts require cryptographic signatures in the core specification?
- How should distributed runtimes synchronize revocation?
- How should constitutional policy survive network partitions?
- What evidence classes should physical-action profiles require?
- How can auditability coexist with strong privacy guarantees?
