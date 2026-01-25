# Domain map

## What this is

A lightweight way to name and own the problem space.
It uses DDD ideas without heavy modelling.
Use it to keep boundaries and ownership clear.

## How to name bounded contexts

Checklist:

- [ ] Use customer-facing language where possible.
- [ ] Keep names stable over time.
- [ ] Avoid names that describe teams or systems.
- [ ] Keep the scope tight and understandable.

## How to assign ownership

Checklist:

- [ ] One accountable owner per context.
- [ ] Ownership includes runbooks and decision rights.
- [ ] Shared responsibility is the exception, not the default.

## How to define interfaces and contracts

Checklist:

- [ ] Define inputs and outputs between contexts.
- [ ] Document data ownership and quality rules.
- [ ] Agree on error handling and escalation paths.

## Domain map structure

| Bounded context | Primary responsibility | Interfaces |
| --- | --- | --- |
| Identity | Authentication and access control | Support Platform, AI Agent |
| Billing | Plans, invoices, and payments | Support Platform |
| Support Platform | Case handling and triage | Knowledge Base, Identity |
| AI Agent | Assisted responses and automation | Support Platform, Knowledge Base |
| Knowledge Base | Articles and reuse of knowledge | Support Platform, AI Agent |

## Do not do this

- Shared everything with no owner.
- Boundaries that leak across multiple contexts.
- Naming that changes every quarter.
