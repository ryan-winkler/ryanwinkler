# System architecture notes

This document sets boundaries for how I think about product systems.
It is intentionally high level and portable.

## Customer signal pipeline

- Capture signal from conversations, incidents, and edge cases.
- Normalise inputs so they can be compared across tools.
- Assign ownership early to avoid stalled decisions.
- Close the loop by showing how decisions change the system.

## AI in production: guardrails over cleverness

- Use AI where failure is reviewable and reversible.
- Prefer human-in-the-loop for trust-sensitive workflows.
- Make source data, prompts, and outputs traceable.
- Define a fallback path when automation is wrong.

## Incident posture

- Incidents are a product input, not just an operations event.
- Each incident results in a decision, a system change, or a deliberate choice not to act.
- Runbooks are part of the product surface.

## Internal tooling

- Tools should reduce manual work and improve signal quality.
- Ownership and permissions are explicit.
- Metrics follow decisions, not the other way round.

## What not to automate

- Decisions that require trust, judgement, or context that cannot be encoded.
- Workflows without clear ownership or review paths.
