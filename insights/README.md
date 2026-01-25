# Product Insights

Curated learnings, patterns, and insights from product work. This is where hard-won knowledge lives.

## Purpose

This directory captures insights that don't fit neatly into frameworks or runbooks:

- Patterns you've seen work (or fail) repeatedly
- Lessons from shipped features
- Customer behavior insights
- Operational learnings
- Industry observations

This is **not** a blog or a collection of hot takes. It's a working knowledge base for product decisions.

## Structure

```
insights/
├── patterns/           # Recurring patterns in product work
├── customer/           # Customer behavior and needs
├── technical/          # Technical insights and constraints
├── operational/        # Operational learnings
└── industry/           # Industry trends and observations
```

## Format

Each insight follows this structure:

```markdown
# [Insight Title]

**Date**: YYYY-MM-DD
**Context**: [Where this came from]
**Tags**: [Relevant tags]

## Observation

[What you noticed or learned]

## Why It Matters

[Why this is important for product decisions]

## When to Apply

[Situations where this insight is relevant]

## Examples

[Concrete examples from your work]

## Related

[Links to related insights, decisions, or frameworks]
```

## How to Use This

### When Making Decisions

Search insights for relevant patterns before deciding. Have others solved this before?

### When Onboarding

Share relevant insights with new team members to transfer context quickly.

### When Reviewing Work

Reference insights in PRD reviews, architecture discussions, or postmortems.

### When Learning

Capture insights immediately after shipping, incidents, or customer conversations.

## Capturing Insights

### Rule: Capture in the flow of work

Don't wait for a "knowledge capture session." Write insights when they're fresh:

- After shipping a feature
- After a customer conversation
- After an incident
- After a decision that worked (or didn't)

### Keep It Practical

Focus on actionable insights:

- ✅ "Users don't read onboarding tooltips. Show value immediately instead."
- ❌ "Onboarding is important."

### Link to Evidence

Connect insights to real work:

- Link to PRDs, decisions, signals
- Reference specific customers or incidents
- Include metrics when available

## Examples of Good Insights

### Pattern: "Sync delays break trust faster than missing features"

**Context**: Observed across multiple inventory management customers

**Observation**: When data sync has any delay (even 5-10 minutes), customers lose trust in the entire system. They'd rather have fewer features with real-time data than more features with stale data.

**Why It Matters**: Prioritize data freshness over feature richness for trust-sensitive workflows.

**When to Apply**: Any feature where users make decisions based on the data. If the data can be wrong, the feature is worse than useless.

### Pattern: "AI confidence thresholds need customer-specific calibration"

**Context**: Learned from AI support response generator launch

**Observation**: A single confidence threshold (e.g., 80%) doesn't work for all customers. Risk-averse customers want 95%+, while high-volume customers accept 70% to reduce support load.

**Why It Matters**: Build configurability into AI features from day one. One-size-fits-all fails.

**When to Apply**: Any AI feature where different customers have different risk tolerances.

## Maintenance

- **Review quarterly**: Archive outdated insights, update with new learnings
- **Tag consistently**: Use tags for findability
- **Cross-reference**: Link related insights together
- **Share**: Reference insights in team discussions and documentation

## Why This Matters

**Without insights**:

- You repeat mistakes
- Context is lost when people leave
- Decisions lack historical perspective
- Onboarding is slow and incomplete

**With insights**:

- Faster, better decisions
- Institutional knowledge preserved
- Patterns become visible
- New team members ramp up quickly

---

**Remember**: Insights are only valuable if they're findable and used. Capture them, tag them, and reference them in your work.
