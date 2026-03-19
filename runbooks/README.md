# Runbooks

Operational procedures for repeatable product work. If you do it twice, document it.

## Philosophy

Runbooks are how you make good work repeatable without turning it into theatre.

This is KCS in practice: capture knowledge in the flow of work, make it findable, and keep it current enough that someone else can actually use it.

## Current structure

```text
runbooks/
├── ai/
│   └── production-readiness-check.md
└── product/
    └── quarterly-roadmap-planning.md
```

Runbook templates live in [templates/template_runbook.md](../templates/template_runbook.md), not under `runbooks/`.

## What goes in a runbook

A runbook documents a repeatable process:

- **When to use it**: trigger conditions
- **Prerequisites**: what needs to be true before you start
- **Steps**: clear ordered actions
- **Decision points**: where judgment is required
- **Outputs**: what exists when you are done
- **Owner**: who keeps it current

## Current runbooks

- [Quarterly roadmap planning](product/quarterly-roadmap-planning.md)
- [AI production readiness check](ai/production-readiness-check.md)

## Runbook vs. workflow vs. template

| Type | Purpose | Example |
|------|---------|---------|
| **Runbook** | Operational procedure for a specific recurring task | "AI production readiness check" |
| **Workflow** | End-to-end process with multiple stages | "New feature development" |
| **Template** | A reusable document structure | "PRD template" |

## Creating a runbook

### Rule: if you do it twice, document it

First time: do the work and take notes.  
Second time: follow the notes and tighten them.  
Third time: you have a runbook worth keeping.

Use [templates/template_runbook.md](../templates/template_runbook.md) as the starting structure.

## Maintaining runbooks

- Update them when reality changes
- Remove steps that no longer earn their place
- Link them from templates, workflows, and project notes where they help
- Keep the title literal enough that someone can find it fast

---

**Remember**: runbooks are working documents. If they stop matching the real process, they stop being useful.
