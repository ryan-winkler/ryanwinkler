# AI Production Readiness Check Runbook

**Owner**: Ryan Winkler  
**Last Updated**: 2026-01-25  
**Frequency**: Before every AI feature launch

## When to Use This

Use this runbook before launching any AI feature to production. This is a go/no-go checklist based on real production requirements, not demo standards.

## Prerequisites

- [ ] AI feature PRD exists and is approved
- [ ] Guardrails document created (`/ai-guardrails`)
- [ ] Architecture documented with failure modes
- [ ] Engineering implementation complete
- [ ] Staging environment available for testing

## Steps

### 1. Validate Guardrails Implementation

**Action**: Verify all safety guardrails are implemented and tested.

Check each guardrail type:

**Handoff Guardrails**

- [ ] Handoff triggers are defined and tested
- [ ] Handoff path routes to correct human/team
- [ ] Context is preserved during handoff
- [ ] Handoff is logged for review

**Refusal Guardrails**

- [ ] Out-of-scope requests are detected
- [ ] Refusal language is clear and helpful
- [ ] Refusals are logged with reason codes
- [ ] Refusal rate is monitored

**Confidence Guardrails**

- [ ] Confidence scores are calculated
- [ ] Thresholds trigger appropriate behaviors
- [ ] Low confidence triggers handoff or refusal
- [ ] Confidence is surfaced to users when appropriate

**Policy Guardrails**

- [ ] Policy rules are enforced
- [ ] Policy violations are logged
- [ ] Escalation path for violations exists
- [ ] Policy is documented and accessible

**Decision point**: If any guardrail is not implemented or tested, this is a **NO-GO**. Do not proceed.

### 2. Verify Observability

**Action**: Confirm all monitoring and alerting is in place.

**Metrics**

- [ ] Input quality metrics defined and instrumented
- [ ] Output quality metrics defined and instrumented
- [ ] User behavior metrics defined and instrumented
- [ ] System behavior metrics defined and instrumented
- [ ] Metrics dashboard created and accessible

**Logs**

- [ ] All AI requests/responses are logged
- [ ] Guardrail triggers are logged
- [ ] Errors and exceptions are logged
- [ ] Logs are searchable and retained appropriately

**Alerts**

- [ ] Refusal rate spike alert configured
- [ ] Confidence drop alert configured
- [ ] Error rate alert configured
- [ ] Latency alert configured
- [ ] Alert routing and escalation defined

**Decision point**: If observability is incomplete, this is a **NO-GO**. You cannot fix what you cannot see.

### 3. Test Failure Modes

**Action**: Actively test each documented failure mode.

For each failure mode in the architecture doc:

- [ ] Test the scenario
- [ ] Verify detection works
- [ ] Confirm mitigation activates
- [ ] Check that impact is contained
- [ ] Validate recovery process

**Common failure modes to test**:

- Over-confident answer on uncertain input
- Silent failure (looks like success but isn't)
- Policy gap (behavior not covered by rules)
- Feedback loop (bad output reinforces bad behavior)
- Automation bias (user stops checking outputs)

**Decision point**: If any critical failure mode is not detected or mitigated, this is a **NO-GO**.

### 4. Validate Rollback Plan

**Action**: Ensure you can turn off the AI feature quickly and safely.

- [ ] Kill switch exists and is tested
- [ ] Safe defaults are defined (what happens when AI is off)
- [ ] Rollback procedure is documented
- [ ] Rollback owner is assigned
- [ ] Rollback triggers are defined
- [ ] Rollback has been tested in staging

**Test the rollback**:

1. Enable the AI feature
2. Trigger the kill switch
3. Verify safe defaults activate
4. Confirm core functionality still works
5. Re-enable and verify recovery

**Decision point**: If rollback is not tested and working, this is a **NO-GO**.

### 5. Check User Education

**Action**: Verify users understand what the AI can and cannot do.

- [ ] Capability boundaries are communicated
- [ ] User documentation exists
- [ ] In-product messaging explains AI behavior
- [ ] Examples of good/bad use cases provided
- [ ] Human override path is clear and accessible

**Decision point**: If users don't understand the AI's limits, adoption will fail or trust will break.

### 6. Validate Support Readiness

**Action**: Ensure support team can handle AI-related issues.

- [ ] Support team trained on AI feature
- [ ] Support runbooks created
- [ ] Escalation path to product/engineering defined
- [ ] Common issues and solutions documented
- [ ] Support can access AI logs for debugging

**Decision point**: If support is not ready, you'll be pulled into every issue. Not scalable.

### 7. Review with Trust & Safety

**Action**: Get explicit sign-off from trust & safety perspective.

Run `/review trust-safety` and address:

- Abuse vectors and mitigations
- Regulatory compliance requirements
- Privacy and data protection
- Worst-case harm scenarios
- Incident response plan

**Decision point**: If trust & safety has concerns, address them before launch. Do not skip this.

### 8. Conduct Go/No-Go Review

**Action**: Make the final launch decision.

**GO Criteria** (all must be true):

- ✅ All guardrails implemented and tested
- ✅ Observability complete (metrics, logs, alerts)
- ✅ Failure modes tested and mitigated
- ✅ Rollback tested and working
- ✅ User education ready
- ✅ Support team trained
- ✅ Trust & safety sign-off received

**NO-GO Criteria** (any one triggers delay):

- ❌ Guardrails incomplete or untested
- ❌ Cannot observe AI behavior
- ❌ Critical failure mode not mitigated
- ❌ Rollback not working
- ❌ Support not ready
- ❌ Trust & safety concerns unresolved

Document the decision in `/decision-log`.

### 9. Plan Phased Rollout

**Action**: Define rollout phases and success criteria.

**Phase 1: Internal** (1-2 weeks)

- Enable for team members only
- Collect feedback and issues
- Refine guardrails based on real usage
- Success criteria: No critical issues, guardrails working

**Phase 2: Beta** (2-4 weeks)

- Enable for opt-in beta customers
- Monitor metrics closely
- Iterate based on feedback
- Success criteria: Metrics within targets, positive feedback

**Phase 3: Limited** (2-4 weeks)

- Enable for 10-25% of users
- Continue monitoring
- Prepare for full rollout
- Success criteria: No degradation, adoption trending up

**Phase 4: General Availability**

- Enable for all users
- Ongoing monitoring and iteration

**Rollback triggers at each phase**:

- Error rate >5%
- Refusal rate >20%
- Confidence avg <70%
- User complaints spike
- Policy violations detected

### 10. Set Post-Launch Review

**Action**: Schedule reviews to assess AI performance.

- [ ] 24-hour review scheduled
- [ ] 1-week review scheduled
- [ ] 1-month review scheduled
- [ ] Ongoing monitoring plan defined

**What to review**:

- Metrics vs. targets
- Guardrail effectiveness
- User feedback and adoption
- Support ticket trends
- Unexpected behaviors or issues

## Common Issues

### Issue: Guardrails trigger too often

**Symptoms**: High refusal rate, frequent handoffs, user frustration  
**Solution**: Review confidence thresholds, refine refusal scenarios  
**Prevention**: Test with real user inputs before launch, not just happy path

### Issue: Metrics show degradation post-launch

**Symptoms**: Latency increase, error rate spike, user drop-off  
**Solution**: Investigate root cause, consider rollback if severe  
**Prevention**: Load test in staging, monitor closely in early phases

### Issue: Users don't understand AI limitations

**Symptoms**: Complaints about "broken" feature, misuse, low adoption  
**Solution**: Improve in-product messaging, add examples, educate users  
**Prevention**: User test the messaging before launch

### Issue: Support overwhelmed with AI questions

**Symptoms**: Support ticket spike, escalations to product/eng  
**Solution**: Create better support docs, add FAQs, improve in-product help  
**Prevention**: Train support thoroughly, create runbooks before launch

## Outputs

By the end of this runbook, you should have:

- ✅ Guardrails validated and tested
- ✅ Observability confirmed (metrics, logs, alerts)
- ✅ Failure modes tested
- ✅ Rollback tested and working
- ✅ User education ready
- ✅ Support team trained
- ✅ Trust & safety sign-off
- ✅ Go/no-go decision documented
- ✅ Phased rollout plan
- ✅ Post-launch reviews scheduled

## Quality Checks

- [ ] All checklist items above are complete
- [ ] No critical gaps or concerns remain
- [ ] Rollback has been tested successfully
- [ ] Team is aligned on go/no-go decision
- [ ] Phased rollout plan is realistic
- [ ] Post-launch monitoring plan is clear

## Related

- [AI_IN_PRODUCTION.md](../../AI_IN_PRODUCTION.md) - AI production principles
- [workflows/ai-feature-launch.md](../../workflows/ai-feature-launch.md) - Full AI launch workflow
- `/ai-guardrails` command - Guardrails definition
- `/ai-review` command - Production readiness review
- `/review trust-safety` - Trust & safety perspective

## Revision History

| Date | Change | Updated By |
|------|--------|------------|
| 2026-01-25 | Initial creation | Ryan Winkler |

---

**Notes**: This is a production readiness check, not a demo readiness check. The bar is higher because real users and real trust are at stake. When in doubt, delay the launch and fix the gaps.
