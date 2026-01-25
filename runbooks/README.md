# Runbooks

Operational procedures for repeatable product work. If you do it twice, document it.

## Philosophy

Runbooks are not bureaucracy—they're how you scale yourself and your team. They capture what works, make it repeatable, and reduce cognitive load for recurring tasks.

This is KCS in action: capture knowledge in the flow of work, make it findable, keep it current.

## Structure

```
runbooks/
├── product/          # Product management procedures
├── research/         # Customer research procedures
├── release/          # Release and deployment procedures
├── incident/         # Incident response procedures
├── ai/               # AI system procedures
└── templates/        # Runbook templates
```

## What Goes in a Runbook

A runbook documents a repeatable process:

- **When to use it**: Trigger conditions
- **Prerequisites**: What you need before starting
- **Steps**: Clear, ordered actions
- **Decision points**: Where judgment is required
- **Outputs**: What you'll have when done
- **Owner**: Who maintains this

## Runbook vs. Workflow vs. Template

| Type | Purpose | Example |
|------|---------|---------|
| **Runbook** | Operational procedure for a specific task | "How to triage a P1 incident" |
| **Workflow** | End-to-end process with multiple steps | "New feature development" |
| **Template** | Document structure to fill in | "PRD template" |

Runbooks are tactical. Workflows are strategic. Templates are structural.

## Creating a Runbook

### Rule: If you do it twice, document it

First time: Do the work, take notes
Second time: Follow your notes, refine them
Third time: You have a runbook

### Format

Use this structure:

```markdown
# [Task Name] Runbook

**Owner**: [Name]
**Last Updated**: [Date]
**Frequency**: [How often this is used]

## When to Use This
[Trigger conditions]

## Prerequisites
- [ ] Thing you need
- [ ] Another thing

## Steps

1. **[Action]**
   - Detail
   - Decision point: If X, then Y

2. **[Next action]**
   - Detail

## Common Issues

**Issue**: [What goes wrong]
**Solution**: [How to fix it]

## Outputs
- [What you'll have]

## Related
- [Link to related runbooks]
```

## Maintaining Runbooks

- **Update after each use**: If you deviate from the runbook, update it
- **Review quarterly**: Archive outdated runbooks
- **Link from tasks**: Reference runbooks in Asana/Jira/etc.
- **Make them findable**: Tag, title clearly, cross-reference

## Examples

### Product Runbooks

- Quarterly roadmap planning
- RICE scoring session
- PRD review checklist
- Go/no-go decision framework

### Research Runbooks

- Customer interview scheduling
- Signal triage process
- User research synthesis

### Release Runbooks

- Pre-launch checklist
- Release communication
- Post-launch monitoring

### Incident Runbooks

- P1 incident response
- Postmortem creation
- Action item tracking

### AI Runbooks

- AI guardrail review
- Production readiness check
- Model performance monitoring

## Why This Matters

**Without runbooks**:

- You reinvent the wheel every time
- Quality varies based on who does it
- Knowledge lives in people's heads
- Onboarding takes forever

**With runbooks**:

- Consistent execution
- Faster onboarding
- Institutional knowledge captured
- You can delegate with confidence

## Meta: Runbook for Creating Runbooks

See `templates/runbook-template.md` for the standard format.

When creating a new runbook:

1. Use the template
2. Write it as you do the task
3. Test it with someone else
4. Refine based on their feedback
5. Add to the index

---

**Remember**: Runbooks are living documents. They should evolve as your process improves.
