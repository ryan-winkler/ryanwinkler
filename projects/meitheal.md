# Meitheal

## Summary

Meitheal is a Home Assistant-native, local-first execution hub for household and homelab work.

It started as a task list inside Home Assistant and grew into a coordination layer for capture, planning, follow-through, automation, voice flows, and agent workflows.

## The product problem

Most household and homelab systems answer one of two questions well:

- what do I have
- what needs tracking

Meitheal is aimed at a different problem:

- what should happen next
- who owns it
- how do we keep it moving without adding more overhead

## Constraints that matter

- It has to work as a Home Assistant add-on
- It has to stay local-first
- It has to respect ingress-safe behavior inside Home Assistant
- It has to keep DDD boundaries and ubiquitous language clear
- It has to treat KCS artifacts as part of the product, not cleanup work

## Why it matters now

- It is the clearest public example of how I work on local-first systems with real operating constraints
- It makes DDD, KCS, voice, and agent handoff decisions visible inside one product
- It keeps the product problem practical: capture, clarify, assign, and move work without adding SaaS overhead

## Current lessons

- local-first products need clearer boundaries, not fewer boundaries
- voice and agent workflows are only useful when the fallback path is obvious
- ubiquitous language changes are product work, not only naming work
- Home Assistant is a good forcing function for practical product decisions because the environment is real and constrained

## Links

- [Meitheal repository](https://github.com/Coolock-Village/meitheal)
