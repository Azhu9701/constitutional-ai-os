# Constitutional AI OS

> **Every AI operating system has values, power structures, and defaults.  
> This project makes them explicit, inspectable, amendable, and executable.**

**Constitutional AI OS** is an open framework for describing and implementing the constitutional layer of AI operating systems: who owns data and agents, who may act, who can override decisions, how rules change, how benefits and risks are distributed, and how those choices become enforceable runtime policy.

This is **not another AI desktop, assistant, or agent launcher**. It is an attempt to define the layer beneath them.

## Why this exists

Today, AI systems increasingly decide:

- what an agent may see, remember, and do;
- who controls its tools, credentials, compute, and data;
- when it may act autonomously;
- who can override or revoke it;
- how multiple agents coordinate;
- what evidence is required before acting;
- how automated work connects to real organizations and physical production.

These are not merely UX choices. They are governance choices expressed through software.

Traditional operating systems schedule CPU, memory, files, and processes. AI operating systems increasingly schedule **attention, memory, models, tools, authority, compute, and action**.

Constitutional AI OS asks a simple question:

> **Can those hidden defaults become an open, machine-readable constitution?**

## Core questions

Every conforming system should be able to answer:

1. **Who owns?**  
   Who owns data, memory, models, agents, compute, and outputs?

2. **Who decides?**  
   Which human, organization, agent, or process has authority over a decision?

3. **Who can override?**  
   Where does root authority live, and how is emergency power constrained?

4. **Who benefits?**  
   How are the gains created by automation allocated?

5. **Who bears the cost?**  
   Who is responsible for failures, displacement, externalities, and resource use?

6. **What may an agent do?**  
   What are the boundaries of autonomous action?

7. **How can the rules change?**  
   Who may amend the constitution, through what process, with what audit trail?

## Architecture

```text
Constitution
    ↓
Rights & Ownership
    ↓
AI Kernel
    ↓
Policy Runtime
    ↓
Agent Protocol
    ↓
World Model
    ↓
Physical / Economic Action
```

The goal is to connect:

```text
principle
  → constitutional rule
  → machine-readable schema
  → policy evaluation
  → runtime enforcement
  → auditable action
```

## Design principles

- **Explicit** — important values and power relationships must not remain hidden defaults.
- **Inspectable** — humans should be able to see which rule authorized or blocked an action.
- **Amendable** — constitutions must define how they can change.
- **Executable** — important rules should be enforceable by runtime infrastructure, not only written as prose.
- **Pluralistic** — the framework should not require one universal ideology; different communities may define different constitutions while using common interfaces.
- **Human-governed** — authority granted to agents must be attributable, bounded, revocable, and auditable.
- **Evidence-aware** — systems acting on claims about the world should be able to preserve provenance and uncertainty.
- **Interoperable** — the constitutional layer should be able to sit above existing agent, tool, identity, and communication protocols.

## Repository map

| File / directory | Purpose |
|---|---|
| [CONSTITUTION.md](CONSTITUTION.md) | Draft constitutional principles for the project itself |
| [ARCHITECTURE.md](ARCHITECTURE.md) | Reference architecture and trust boundaries |
| [GOVERNANCE.md](GOVERNANCE.md) | How this open project changes |
| [ROADMAP.md](ROADMAP.md) | From written principles to executable runtime |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to participate |
| [docs/](docs/) | Explanations of each layer |
| [specs/](specs/) | Machine-readable schemas |
| [rfcs/](rfcs/) | Proposals for major design changes |
| [examples/](examples/) | Example constitutions for different deployment contexts |

## v0.1 scope

The first milestone does **not** attempt to build a full operating system.

v0.1 focuses on:

- a common vocabulary for constitutional AI operating systems;
- a minimal constitution data model;
- rights, ownership, authority, and amendment primitives;
- policy decision records;
- an architecture for runtime enforcement;
- example constitutions for personal, cooperative, and factory contexts.

## What this project is not

It is not:

- a claim that one political philosophy should be hard-coded into every AI system;
- a replacement for model safety research;
- a replacement for operating-system security;
- a replacement for law, organizational governance, or democratic institutions;
- a promise that machine-readable rules can resolve every social conflict.

The point is narrower and more practical:

> **When an AI system embeds consequential assumptions about authority, ownership, rights, and action, those assumptions should be visible and governable.**

## Intellectual lineage

This project is informed by several existing traditions and technical directions, including:

- free software and software freedom;
- constitutional approaches to AI behavior;
- user-controlled data and data sovereignty;
- agent operating-system research;
- sandboxed and policy-enforced agent runtimes;
- open tool protocols and agent-to-agent protocols;
- knowledge graphs, provenance systems, and world models.

We treat these as reference points, not as a single inherited doctrine.

## 中文简介

传统操作系统分配 CPU、内存、文件和进程。AI 操作系统正在开始分配另一组更敏感的东西：**注意力、记忆、模型、工具、权限、算力和行动能力**。

这个项目希望把 AI 系统里原本隐藏的默认规则——例如“谁拥有数据”“Agent 能做什么”“谁能撤销它”“规则如何修改”——变成公开、可检查、可修改、可执行的制度。

我们不先假定唯一正确的意识形态，而是先建立一个开放框架，让不同个人、社区和组织都能明确写出自己的 AI Constitution，并让其中可执行的部分真正进入运行时。

## Status

**v0.1 — founding specification stage**

The repository is intentionally early. Discussion, criticism, competing constitutional models, implementation experiments, and RFCs are welcome.

## License

Code and schemas are intended to use the Apache License 2.0. Documentation and constitutional text may later adopt a documentation-friendly open license if the community finds that separation useful. See [LICENSE](LICENSE) for the current repository license.
