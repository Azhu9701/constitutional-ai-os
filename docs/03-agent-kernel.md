# Agent Kernel

The AI kernel is the resource manager beneath agents.

It is responsible for exposing control points where constitutional policy can actually be enforced.

## Kernel-managed resources

Possible resources include:

- model endpoints;
- inference budgets;
- context;
- long-term memory;
- files;
- network;
- tools;
- credentials;
- secrets;
- money;
- external APIs;
- robotic actuators;
- human attention.

## Agent as process

A useful analogy is:

```text
OS process          AI agent
----------          ----------------
PID                 agent identity
user                principal
environment         context
file descriptors    tool handles
permissions         capabilities
signals             pause / revoke / stop
scheduler           task / compute scheduler
syscalls             action requests
```

The analogy is not perfect, but it clarifies an important point:

> The agent should request powerful actions through a mediated interface rather than possess unlimited ambient authority.

## Constitutional syscall

A future runtime can treat every consequential tool call as a constitutional syscall:

```text
request(action, resource, context, delegation)
→ evaluate policy
→ allow / deny / require / escalate
```

This makes the kernel a practical enforcement point for the constitution.
