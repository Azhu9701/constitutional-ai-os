# Contributing

Constitutional AI OS is intentionally interdisciplinary.

You do not need to be an operating-systems engineer to contribute. Useful work can come from software engineering, robotics, security, distributed systems, governance, law, economics, labor research, philosophy, HCI, or lived experience with automated systems.

## Good first contributions

- challenge an undefined term;
- add a concrete failure scenario;
- propose an example constitution;
- improve a JSON Schema;
- write a policy test case;
- map an existing agent runtime to the architecture;
- identify a hidden source of authority;
- document a constitutional conflict;
- propose an RFC.

## Contribution rule

When proposing a rule, try to answer:

1. Who is the subject?
2. What action or resource is governed?
3. Who has authority to make this rule?
4. Is it enforceable, auditable, or aspirational?
5. How can it be changed?
6. What happens when it conflicts with another rule?
7. How would an affected person understand or appeal it?

## RFCs

Use an RFC for:

- new core concepts;
- breaking schema changes;
- new governance mechanisms;
- new conformance requirements;
- new runtime trust assumptions.

Copy `rfcs/RFC-0001-constitutional-ai-os.md` as a structural reference.

## Pull requests

A useful pull request should include:

- problem statement;
- proposed change;
- why the change belongs in the core, an example, or a profile;
- compatibility impact;
- security or governance impact where relevant.

## Style

Prefer plain language.

If a technical or philosophical term is necessary, define it before relying on it.

The project should be understandable by both developers and people affected by AI systems.

## Disagreement

Substantive disagreement is welcome.

Do not force every value dispute into one universal answer. Sometimes the correct output is:

- a protocol-level mechanism;
- two competing example constitutions;
- a documented conflict;
- an unresolved research question.

## Security

Do not publish live credentials, private keys, exploit details affecting deployed systems, or personal data in issues.

Security-reporting procedures will be added before a production runtime is released.
