# Product Management Frameworks

Core frameworks Ryan uses in product work.

## RICE / DRICE Prioritization

### RICE Formula

For a deep dive, see [RICE: Simple Prioritization for Product Managers](https://www.intercom.com/blog/rice-simple-prioritization-for-product-managers/) (Intercom).

```
Score = (Reach × Impact × Confidence) / Effort
```

**Reach**: Number of customers affected per time period (usually per quarter)

- Count unique customers, not page views or sessions
- Use actual data when possible, estimates when necessary

**Impact**: How much this improves the customer experience

- 3 = Massive impact
- 2 = High impact
- 1 = Medium impact
- 0.5 = Low impact
- 0.25 = Minimal impact

**Confidence**: How sure are we about Reach, Impact, and Effort?

- 100% = High confidence (strong data)
- 80% = Medium confidence (some data, some assumptions)
- 50% = Low confidence (mostly assumptions)

**Effort**: Person-months of work

- Include all team members (PM, Eng, Design, QA)
- Account for complexity and unknowns
- Minimum score: 0.5 (less than 2 weeks)

### DRICE Formula (for complex work)

Proposed by Lenny Rachitsky for complex environments. See [Introducing DRICE](https://www.lennysnewsletter.com/p/introducing-drice-a-modern-prioritization).

```
Score = (Reach × Impact × Confidence) / (Effort × Dependencies × Risk)
```

**Dependencies**: External dependencies that could block or delay

- 0 = No external dependencies
- 1 = 1-2 dependencies, low risk
- 2 = 3-5 dependencies, medium risk
- 3 = 6+ dependencies or high-risk dependencies

**Risk**: Technical, product, or operational risk

- 1 = Low risk (proven approach, reversible)
- 2 = Medium risk (some unknowns, mostly reversible)
- 3 = High risk (many unknowns, hard to reverse)
- 4 = Critical risk (could cause major issues)

### When to Use DRICE vs RICE

| Scenario | Use | Reason |
|----------|-----|--------|
| Simple, low-risk feature | RICE | Keep it simple |
| Cross-team collaboration | DRICE | Make dependencies visible |
| High uncertainty | DRICE | Surface risks explicitly |
| Hard to reverse | DRICE | Account for commitment |
| Proven, incremental work | RICE | Avoid overhead |

## Domain Driven Design (DDD)

For a foundational intro, see [DomainDrivenDesign](https://martinfowler.com/bliki/DomainDrivenDesign.html) by Martin Fowler.

### Bounded Contexts

A bounded context is a boundary within which a particular domain model is defined and applicable.

**Key Principles:**

- Each context has its own ubiquitous language
- Explicit boundaries prevent model confusion
- Clear ownership for each context
- Contexts communicate through well-defined interfaces

**Identifying Bounded Contexts:**

1. Look for different meanings of the same term
2. Find natural organizational boundaries
3. Identify different data ownership
4. Notice where language changes

**Example:**

- "Order" in Sales context = customer purchase
- "Order" in Fulfillment context = picking and shipping
- "Order" in Finance context = revenue recognition

### Ubiquitous Language

Use the same terms in code, docs, and conversations.

**Rules:**

- Terms must be precise and unambiguous within a context
- Avoid technical jargon when domain terms exist
- Update language when the model evolves
- Document terms in context documentation

## Knowledge-Centered Service (KCS)

The consortium standard for knowledge management. See the [KCS v6 Methodology](https://www.serviceinnovation.org/kcs/).

### Core Principles

**Solve and Capture**

- Capture knowledge in the flow of work
- Don't wait for "perfect" documentation
- Make it easy to contribute

**Structure and Reuse**

- Organize knowledge for findability
- Link related content
- Update based on usage

**Improve and Evolve**

- Knowledge is never "done"
- Update based on feedback
- Retire outdated content

### Signal Quality in KCS

**High-Quality Signal:**

- Reproducible (can be verified)
- Specific (concrete examples)
- Frequent (pattern, not one-off)
- Severe (meaningful impact)
- Evidence-based (data, not opinion)

**Low-Quality Signal:**

- One-off occurrence
- Vague or general
- Opinion without evidence
- Cannot be reproduced
- Contradicts other signals

## Customer Journey Mapping

A foundational tool for empathy. See [Journey Mapping 101](https://www.nngroup.com/articles/journey-mapping-101/) by Nielsen Norman Group.

### Journey Stages

**Awareness**: Customer discovers the product
**Evaluation**: Customer assesses fit
**Onboarding**: Customer gets started
**Adoption**: Customer uses core features
**Expansion**: Customer uses advanced features
**Renewal**: Customer decides to continue
**Advocacy**: Customer recommends to others

### Friction Points

For each stage, identify:

- What's the customer trying to do?
- What's getting in their way?
- How severe is the friction?
- How often does this happen?
- What's the impact if we fix it?

### Trust Impact

Some friction points affect trust more than others:

- Data accuracy issues
- Unexpected behavior
- Security or privacy concerns
- Reliability problems
- Unclear or misleading communication

## AI Evaluation in Production

This is not a branded framework. It is the working pattern I use when an AI feature moves from demo mode into live use.

### What to evaluate

- **Real inputs**: Use live or representative conversations, requests, and edge cases
- **Escalation behavior**: Define when the system should hand off instead of improvising
- **Failure visibility**: Make sure silent failure is visible to users and operators
- **Quality thresholds**: Agree upfront on what good enough looks like
- **Fallback paths**: Keep a reviewable, reversible path when the model is wrong
- **Learning loop**: Feed edge cases, incident patterns, and docs gaps back into the system

### Practical rules

- Do not evaluate only on happy-path prompts
- Keep routing, handoff, and refusal behavior explicit
- Track the difference between an impressive answer and a useful answer
- Treat adoption as a trust problem as much as a feature problem
- Update prompts, policies, and knowledge artifacts together

### What this helps avoid

- over-confident outputs that should have escalated
- demos that collapse in live traffic
- policy drift between teams
- AI features that feel clever but never become dependable

## Four Risks Framework

From Marty Cagan (SVPG). See [The Four Big Risks](https://svpg.com/four-big-risks/).

Every product faces four types of risk:

**Value Risk**: Will customers buy it or choose to use it?

- Validate: Customer interviews, prototypes, usage data

**Usability Risk**: Can customers figure out how to use it?

- Validate: Usability testing, onboarding metrics, support tickets

**Feasibility Risk**: Can we build it with available technology and resources?

- Validate: Technical spikes, prototypes, architecture review

**Business Viability Risk**: Does this work for our business?

- Validate: Financial modeling, strategic alignment, operational assessment
