# World Model

The world model provides facts and evidence to policy.

It should not be allowed to become policy merely because it is machine-readable.

## Separation

```text
World model:
"Person P is inside zone Z."

Constitution:
"Robot R may not enter zone Z while a person is present."

Policy runtime:
DENY robot.move
```

Each layer has a different job.

## Evidence-aware state

For policy-relevant facts, a world model should be able to provide:

- claim;
- source;
- observation time;
- confidence or uncertainty;
- validity interval;
- conflicting evidence;
- provenance chain.

## Risk-based evidence

A low-risk recommendation may tolerate uncertain data.

A high-impact physical or financial action may require:

- recent evidence;
- multiple sources;
- direct sensor confirmation;
- human verification.

The constitution should be able to express those differences.

## Feedback

Action changes the world.

Therefore the full loop is:

```text
world state
→ agent intent
→ constitutional decision
→ action
→ observation
→ updated world state
```

This creates a bridge between AI reasoning and accountable real-world operation.
