# Quarterly Roadmap Planning Runbook

**Owner**: Ryan Winkler  
**Last Updated**: 2026-01-25  
**Frequency**: Quarterly (6 weeks before quarter start)

## When to Use This

Use this runbook when planning the product roadmap for an upcoming quarter. Start 6 weeks before the quarter begins to allow time for scoring, sequencing, and alignment.

## Prerequisites

- [ ] Previous quarter's roadmap and outcomes reviewed
- [ ] Signal reviews from past quarter collected (in `tracker/signals/`)
- [ ] RICE/DRICE scores updated for candidate work
- [ ] Team capacity estimates from engineering leads
- [ ] Strategic priorities confirmed with leadership

## Steps

### 1. Collect and Review Signals

**Action**: Gather all customer signals, support data, and operational feedback from the past quarter.

- Review `tracker/signals/` for tagged and scored signals
- Check support ticket trends and severity
- Review usage data and drop-off points
- Collect engineering and ops feedback

**Decision point**: If signal quality is low (no frequency data, vague descriptions), run `/signal-review` to improve before proceeding.

### 2. Score All Candidate Work

**Action**: Calculate RICE or DRICE scores for each opportunity.

- Use `/rice-score` for each feature or initiative
- Document scores in `tracker/scores/`
- Use DRICE for cross-team or high-uncertainty work
- Include confidence levels based on signal quality

**Output**: Scored list of all candidate work with rationale.

### 3. Map Dependencies

**Action**: Identify what needs to happen in what order.

- Create dependency map (can be simple text list)
- Identify blockers (APIs, data, team availability)
- Note what can run in parallel vs. sequential
- Flag external dependencies (vendors, partners, compliance)

**Decision point**: If dependencies are complex or risky, run `/architecture` to clarify system boundaries and ownership.

### 4. Sequence by Priority and Feasibility

**Action**: Build a prioritized, sequenced roadmap.

- Start with highest RICE/DRICE scores
- Adjust for dependencies (can't do B before A)
- Consider team capacity and skills
- Balance quick wins with strategic bets

**Use `/roadmap` command** to generate structured roadmap document.

### 5. Validate with Multi-Perspective Review

**Action**: Get feedback from key stakeholders.

Run these reviews:

- `/review engineering-lead` - Technical feasibility and effort
- `/review product-strategist` - Strategic alignment
- `/review customer-success` - Customer impact and adoption
- `/review critical-thinker` - Challenge assumptions and find gaps

**Decision point**: If major concerns are raised, revisit scoring or sequencing before proceeding.

### 6. Check Capacity and Adjust

**Action**: Ensure roadmap fits within team capacity.

- Calculate total effort (person-weeks)
- Compare to available capacity
- Leave 20% buffer for incidents, support, and unknowns
- If over-capacity, defer lowest-priority items

**Common issue**: Teams often over-commit. Be realistic about what can ship in a quarter.

### 7. Create Communication Plan

**Action**: Prepare roadmap communication for different audiences.

- **Engineering**: Detailed specs, dependencies, timelines
- **Leadership**: Strategic rationale, outcomes, risks
- **Customers**: Value proposition, timelines (conservative)
- **Support**: What's changing, when, how to handle questions

Use `/comms` command to draft stakeholder-specific updates.

### 8. Document Decisions

**Action**: Log key decisions and trade-offs.

- Use `/decision-log` for major prioritization calls
- Document what was deferred and why
- Link to supporting evidence (scores, signals, reviews)
- Set review date for mid-quarter check-in

### 9. Set Success Metrics

**Action**: Define how you'll measure if the roadmap is working.

For each major initiative:

- Define success metrics (from PRDs)
- Set up instrumentation and dashboards
- Plan mid-quarter and end-of-quarter reviews
- Assign metric owners

### 10. Publish and Align

**Action**: Share roadmap and get final alignment.

- Publish roadmap in `projects/roadmap-[quarter].md`
- Present to engineering, leadership, and stakeholders
- Address questions and concerns
- Get explicit buy-in from engineering leads

**Output**: Finalized, published roadmap with team alignment.

## Common Issues

### Issue: Roadmap is too ambitious

**Symptoms**: Engineering pushback, capacity calculations show 120%+ allocation  
**Solution**: Defer lowest-priority items, break large items into phases  
**Prevention**: Start with 80% capacity target, leave buffer

### Issue: Dependencies block everything

**Symptoms**: Most items can't start until something else finishes  
**Solution**: Identify critical path, consider parallel workstreams, escalate blockers  
**Prevention**: Map dependencies early, design for incremental delivery

### Issue: Priorities shift mid-planning

**Symptoms**: Leadership changes direction, new urgent work appears  
**Solution**: Re-score with new context, adjust roadmap, communicate changes  
**Prevention**: Align on strategic priorities before detailed planning

### Issue: Signal quality is poor

**Symptoms**: Scores have low confidence, unclear customer impact  
**Solution**: Run customer interviews, improve signal collection process  
**Prevention**: Maintain signal quality throughout quarter, not just at planning time

## Outputs

By the end of this runbook, you should have:

- ✅ Scored list of all candidate work
- ✅ Dependency map
- ✅ Prioritized, sequenced roadmap document
- ✅ Multi-perspective reviews completed
- ✅ Capacity validation
- ✅ Communication plan
- ✅ Decision log entries
- ✅ Success metrics defined
- ✅ Published roadmap with team alignment

## Quality Checks

- [ ] All roadmap items have RICE/DRICE scores
- [ ] Dependencies are mapped and accounted for
- [ ] Capacity is realistic (80% or less of available capacity)
- [ ] Success metrics are defined for major initiatives
- [ ] Engineering leads have reviewed and signed off
- [ ] Deferred items are documented with rationale
- [ ] Communication plan covers all stakeholders

## Related

- [PRIORITISATION_SYSTEM.md](../../core/PRIORITISATION_SYSTEM.md) - Prioritization framework
- [workflows/new-feature.md](../../workflows/new-feature.md) - Feature development workflow
- [templates/template_rice_drice.md](../../templates/template_rice_drice.md) - Scoring template
- `/roadmap` command - Roadmap generation
- `/rice-score` command - Prioritization scoring

## Revision History

| Date | Change | Updated By |
|------|--------|------------|
| 2026-01-25 | Initial creation | Ryan Winkler |

---

**Notes**: This runbook assumes you're working with a cross-functional team and have access to customer signals and usage data. Adjust timeline and steps based on your organization's planning cycle.
