# Signal scorecard

## What this is

A simple way to turn customer signal into scoring inputs.
It supports KCS practices and keeps signal quality visible.
Use it before RICE/DRICE scoring.

## What qualifies as signal

Examples of valid signal categories:

- Customer conversations (calls, tickets, feedback forms)
- Production incidents and edge cases
- Support notes and escalations
- Usage patterns or drop-offs
- Compliance or risk reviews

Checklist:
- [ ] The signal has a source and timestamp.
- [ ] The signal is linked to a product area or domain.
- [ ] The signal includes evidence, not just opinion.

## Signal quality rubric

| Quality | Evidence | Reproducibility | Customer impact | Frequency |
| --- | --- | --- | --- | --- |
| High | Clear examples or data | Reproducible | Measurable impact | Repeats consistently |
| Medium | Partial evidence | Sometimes reproducible | Some impact | Repeats occasionally |
| Low | Hearsay or vague | Not reproducible | Unclear impact | One-off |

## Signal quality → confidence guidance

| Signal quality | Suggested confidence range |
| --- | --- |
| High | 0.7–0.9 |
| Medium | 0.4–0.6 |
| Low | 0.1–0.3 |

## Common signal traps

- Loud customer bias.
- Recency bias after a fresh incident.
- Support-only visibility with no product context.
- Over-weighting opinions without evidence.
- Merging unrelated issues into one theme.

## Operational definitions

- **Severity**: size of harm if the issue occurs.
- **Frequency**: how often the issue occurs in a time period.
- **Trust impact**: effect on reliability, safety, or perceived integrity.
