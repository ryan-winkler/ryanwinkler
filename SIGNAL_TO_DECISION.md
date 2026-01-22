# Signal to decision

A lightweight operating model for turning customer signal into action.

## Inputs

- Customer conversations
- Incidents and edge cases
- Internal tooling usage
- Support and operational notes

## Triage rules

- Log the signal in a shared system of record.
- Tag the signal with a clear product area.
- Assign an owner within a defined time window.
- Record severity and customer impact using a consistent scale.

## Decision thresholds

- A single high-severity signal can trigger action.
- Repeated low-severity signals trigger investigation.
- Signals without ownership are closed or reassigned.

## Where signals stop

- If the signal is not actionable, document why.
- If it is out of scope, redirect it with a clear owner.
- If it is a duplicate, merge and close.

## Feedback loop

- Share outcomes with the source team.
- Update runbooks or tooling when patterns repeat.
