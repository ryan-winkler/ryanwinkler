# Prioritisation system

## What this is

A practical stack that links customer signal to scoring and decisions.
It combines RICE/DRICE, DDD, KCS, and the end-to-end journey.
Use it to make prioritisation explicit and repeatable.
See [SIGNAL_SCORECARD.md](SIGNAL_SCORECARD.md), [DOMAIN_MAP.md](DOMAIN_MAP.md), and [templates/template_rice_drice.md](../templates/template_rice_drice.md).

## When to use RICE vs DRICE

| Use case | Use | Why |
| --- | --- | --- |
| Low dependency, low risk changes | RICE | Keep it simple and fast. |
| Cross-team work or high uncertainty | DRICE | Make dependencies and risks visible. |
| Changes that are hard to undo | DRICE + reversibility note | Prevents accidental lock-in. |
| Small, local improvements | RICE | Avoid overhead. |

## How DDD shapes what counts as a “thing” worth scoring

Use bounded contexts and ownership to define the unit of work. See [DOMAIN_MAP.md](DOMAIN_MAP.md).

Checklist:

- [ ] The work sits in a named bounded context.
- [ ] The owning team is clear.
- [ ] The language matches the domain (ubiquitous language).
- [ ] The work is not a mix of multiple contexts.

## How KCS influences inputs

Signal quality drives confidence and should be visible in scoring. See [SIGNAL_SCORECARD.md](SIGNAL_SCORECARD.md).

Checklist:

- [ ] Signals are captured with evidence and reproducibility.
- [ ] Repeated signals are merged and counted once.
- [ ] Noise is labelled (one-off, opinion-only, or unverified).
- [ ] Learning is added to the knowledge base.

## How the customer journey changes scoring

Where the friction sits affects impact and trust.

Checklist:

- [ ] Journey stage is explicit (onboarding, core use, support, renewal).
- [ ] Severity is assessed in customer terms.
- [ ] Frequency reflects how often customers hit the issue.
- [ ] Trust impact is called out when reliability or safety is at risk.

## End-to-end flow

Signal → Domain → Candidate work → Score → Decision → Ship → Learn

Decision table:

| Stage | Output | Owner |
| --- | --- | --- |
| Signal | Tagged, logged signal | Signal owner |
| Domain | Bounded context + owner | Domain owner |
| Candidate work | A scoped unit of work | PM/EM pair |
| Score | RICE/DRICE score with confidence | PM/EM pair |
| Decision | Do / Defer / Drop | Decision owner |
| Ship | Release and comms | Delivery owner |
| Learn | Post-ship signal and updates | Product owner |
