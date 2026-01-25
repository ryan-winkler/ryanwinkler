---
description: End-to-end workflow for new feature development
---

# New Feature Development Workflow

## When to Use

When developing a new feature from customer signal to production.

## Prerequisites

- Customer signal or problem identified
- Initial problem statement

## Steps

### 1. Validate the Signal

**Action**: Review and assess signal quality

```
/signal-review [problem or signal]
```

**Questions**:

- Is this a real pattern or a one-off?
- Do we have enough evidence?
- What's the customer impact?

**Output**: Signal review document in `tracker/signals/`

**Decision Point**:

- ✅ High-quality signal → Continue
- ⚠️ Need more data → Conduct interviews
- ❌ Low-quality signal → Drop or defer

---

### 2. Understand the Customer (if needed)

**Action**: Conduct customer interviews

```
/customer-interview [problem area]
```

**Questions**:

- What's the current workflow?
- What breaks down?
- What workarounds exist?
- How do they measure success?

**Output**: Interview guide and synthesis in `research/interviews/`

---

### 3. Define the Solution

**Action**: Create a PRD

```
/prd [feature name]
```

**Include**:

- Problem statement
- Success metrics
- Requirements
- Out of scope
- Dependencies
- Risks

**Output**: PRD in `projects/[feature-name]-prd.md`

---

### 4. Review Technical Feasibility

**Action**: Get engineering perspective

```
/review engineering-lead
```

**Questions**:

- Can we build this?
- What are the technical risks?
- What's the effort estimate?
- What dependencies exist?

**Output**: Engineering review comments in PRD

---

### 5. Score and Prioritize

**Action**: Calculate RICE or DRICE score

```
/rice-score [feature name]
```

**Inputs**:

- Reach (from signal review)
- Impact (from customer interviews)
- Confidence (from evidence quality)
- Effort (from engineering review)
- Dependencies (if using DRICE)
- Risk (if using DRICE)

**Output**: Score card in `tracker/scores/[feature-name]-score.md`

**Decision Point**:

- ✅ High score → Add to roadmap
- ⚠️ Medium score → Consider for later
- ❌ Low score → Defer or drop

---

### 6. Define Architecture

**Action**: Document system design

```
/architecture [feature name]
```

**Include**:

- Bounded contexts
- System components
- Failure modes
- Observability plan

**Output**: Architecture doc in `context/architecture/[feature-name].md`

---

### 7. Review from Multiple Perspectives

**Action**: Get diverse feedback

```
/review critical-thinker
/review customer-success
/review data-analyst
```

**Questions**:

- What could go wrong?
- How will customers adopt this?
- How do we measure success?

**Output**: Review comments and updates to PRD

---

### 8. Add to Roadmap

**Action**: Update product roadmap

```
/roadmap [quarter]
```

**Include**:

- Feature with score
- Dependencies and sequencing
- Owner and timeline
- Success metrics

**Output**: Updated roadmap in `projects/roadmap-[quarter].md`

---

### 9. Build and Ship

**Action**: Execute development

**During Development**:

- Track progress
- Update stakeholders
- Adjust based on learnings

**Before Launch**:

- Test against success criteria
- Prepare rollback plan
- Train support team
- Create user documentation

---

### 10. Monitor and Learn

**Action**: Track post-launch metrics

**Monitor**:

- Success metrics from PRD
- User adoption and behavior
- Support tickets and feedback
- System performance

**After 2-4 weeks**:

- Review results
- Update knowledge base
- Document learnings
- Decide on iteration

---

## Outputs

By the end of this workflow, you'll have:

- ✅ Signal review
- ✅ Customer interview insights (if needed)
- ✅ Comprehensive PRD
- ✅ RICE/DRICE score
- ✅ Architecture documentation
- ✅ Multi-perspective reviews
- ✅ Roadmap placement
- ✅ Launch plan
- ✅ Post-launch learnings

## Next Steps

- For AI features → Use `ai-feature-launch.md` workflow
- For releases → Use `release-planning.md` workflow
- For incidents → Use `incident-triage.md` workflow

## Common Variations

**Fast Track** (low complexity, high confidence):

1. Signal review
2. PRD
3. RICE score
4. Build and ship

**High Risk** (AI, trust-sensitive, complex):

1. Signal review
2. Customer interviews
3. PRD
4. Architecture
5. Multiple reviews (engineering, trust-safety, critical-thinker)
6. DRICE score
7. Phased rollout
