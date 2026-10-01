# Why an AI OS Needs a Constitutional Layer

An AI operating system is not defined by having a chat window, a tool registry, or a desktop.

The deeper transition happens when the system begins deciding how to allocate:

- attention;
- memory;
- model access;
- tools;
- credentials;
- compute;
- communication;
- authority;
- real-world action.

At that point, "defaults" become a form of governance.

## Hidden constitutions already exist

Every deployed agent system already has answers to questions such as:

- Which company can change the model?
- Who can read the memory?
- Can the agent spend money?
- Can an administrator override the user?
- Which logs are retained?
- Who owns generated workflow data?
- Can the agent delegate to another agent?
- Can a safety system stop an authorized task?

If those answers are not written down, the system does not become neutral. It simply has a hidden constitution.

## Constitutional layer

The constitutional layer makes these answers first-class system objects.

It should be:

**Explicit** — rules are stated.

**Inspectable** — users and operators can read them.

**Amendable** — change procedures are defined.

**Executable** — important rules affect runtime behavior.

**Auditable** — decisions can be explained after the fact.

## Why "OS"?

Traditional operating systems mediate access to scarce and powerful resources.

AI systems add new mediated resources:

```text
traditional OS        AI OS
--------------        ----------------
CPU                   model inference
RAM                   context / memory
files                 knowledge / data
processes             agents
syscalls              tool calls
users/groups          principals / roles
permissions           capabilities / policies
device drivers        robots / external systems
```

The constitutional layer is analogous to the part of an operating system that defines who is allowed to do what — expanded to cover delegation, governance, evidence, and amendment.

## From ideology to infrastructure

"Values" become infrastructure when they determine:

- which action is permitted;
- who receives authority;
- who owns a resource;
- whose approval is required;
- what evidence counts;
- who can change the rule.

The purpose of this project is not to hide ideology behind technical language.

It is to make such choices visible enough to inspect, compare, criticize, and change.
