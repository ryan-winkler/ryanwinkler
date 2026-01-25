---
description: Launch AI features safely in production
---

# AI Feature Launch Workflow

## When to Use

When launching any feature that uses AI/ML in production.

## Prerequisites

- Feature PRD exists
- Basic architecture defined
- Engineering team aligned

## Steps

### 1. Define AI Guardrails

**Action**: Establish safety boundaries

```
/ai-guardrails [feature name]
```

**Define**:

- Handoff triggers (when to escalate to human)
- Refusal scenarios (what's out of scope)
- Confidence thresholds (how certain must the AI be)
- Policy enforcement (what rules govern behavior)

**Output**: Guardrails doc in `context/ai-guardrails/[feature-name].md`

---

### 2. Design Observability

**Action**: Plan monitoring and metrics

**Metrics to Define**:

- **Input Quality**: Missing context, ambiguous requests
- **Output Quality**: Accuracy, helpfulness, policy compliance
- **User Behavior**: Acceptance rate, edit rate, override rate
- **System Behavior**: Latency, cost per request, error rate

**Alerts to Set**:

- Refusal rate spike
- Confidence drop
- Error rate increase
- Latency degradation

**Output**: Monitoring plan in architecture doc

---

### 3. Identify Failure Modes

**Action**: Think through what can go wrong

**Common Failure Modes**:

- Over-confident answers on uncertain inputs
- Silent refusal that looks like success
- Policy gaps and inconsistencies
- Feedback loops amplifying bad outputs
- Automation bias (users stop checking)

**For Each Failure Mode**:

- How do we detect it?
- What's the impact?
- How do we prevent it?
- How do we recover?

**Output**: Failure mode analysis in architecture doc

---

### 4. Create Rollback Plan

**Action**: Define how to turn it off

**Rollback Requirements**:

- Kill switch that disables AI quickly
- Safe defaults (what happens when AI is off)
- Rollback triggers (when do we pull the plug)
- Rollback owner (who decides)
- Communication plan (how do we tell users)

**Test**: Actually test the rollback procedure

**Output**: Rollback plan in PRD

---

### 5. Review Production Readiness

**Action**: Comprehensive pre-launch review

```
/ai-review [feature name]
```

**Check**:

- ✅ Guardrails documented and tested
- ✅ Metrics and alerts configured
- ✅ Failure modes assessed
- ✅ Rollback plan tested
- ✅ User education ready
- ✅ Support team trained

**Output**: Readiness review in `research/ai-reviews/[feature-name]-review.md`

**Decision Point**:

- ✅ All checks pass → Proceed to launch
- ⚠️ Minor gaps → Fix and re-review
- ❌ Major gaps → Block launch

---

### 6. Get Trust & Safety Review

**Action**: Risk and compliance assessment

```
/review trust-safety
```

**Questions**:

- What are the abuse vectors?
- What regulatory requirements apply?
- What's the worst-case harm scenario?
- Do we have the right controls?

**Output**: Trust & Safety review comments

---

### 7. Plan Phased Rollout

**Action**: Don't launch to everyone at once

**Rollout Phases**:

1. **Internal** (1-2 weeks): Team members only
2. **Beta** (2-4 weeks): Friendly customers who opt in
3. **Limited** (2-4 weeks): 10-25% of users
4. **General** (ongoing): All users

**Between Phases**:

- Review metrics
- Collect feedback
- Adjust guardrails
- Fix issues

**Rollback Criteria**: Define what would trigger rollback at each phase

---

### 8. Launch and Monitor

**Action**: Ship and watch closely

**First 24 Hours**:

- Monitor dashboards continuously
- Review every refusal and handoff
- Check error logs
- Collect user feedback

**First Week**:

- Daily metric reviews
- Support ticket analysis
- User feedback synthesis
- Guardrail adjustments

**First Month**:

- Weekly reviews
- Pattern analysis
- Knowledge base updates
- Iteration planning

---

### 9. Iterate and Improve

**Action**: Continuous improvement

**Review**:

- What's working well?
- What's not working?
- What are users doing that we didn't expect?
- What guardrails are triggering most often?

**Adjust**:

- Confidence thresholds
- Refusal scenarios
- Handoff triggers
- User messaging

**Document**: Update knowledge base with learnings

---

### 10. Post-Launch Review

**Action**: Formal review after 4-8 weeks

**Questions**:

- Did we hit our success metrics?
- What surprised us?
- What would we do differently?
- What did we learn about AI in production?

**Output**: Post-launch review in `memory/learnings/[feature-name]-launch.md`

---

## Outputs

By the end of this workflow, you'll have:

- ✅ Comprehensive AI guardrails
- ✅ Monitoring and alerting
- ✅ Failure mode analysis
- ✅ Tested rollback plan
- ✅ Production readiness review
- ✅ Trust & Safety approval
- ✅ Phased rollout plan
- ✅ Post-launch learnings

## Red Flags (Do Not Launch)

- ❌ No rollback plan
- ❌ No monitoring or alerts
- ❌ Guardrails not tested
- ❌ Support team not trained
- ❌ Failure modes not assessed
- ❌ Trust & Safety concerns unresolved

## Next Steps

- For incidents → Use `ai-incident-response.md` workflow
- For monitoring → Use `ai-monitoring.md` workflow
- For iteration → Use `new-feature.md` workflow

## Remember

**AI in production is different**:

- Behavior is probabilistic, not deterministic
- Failure modes are subtle and emergent
- User trust is fragile
- Rollback is not always clean

**When in doubt, slow down and add more guardrails.**
