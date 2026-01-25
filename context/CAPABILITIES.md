# RWOS Capabilities Map

This file helps the AI suggest relevant tools and workflows based on what you're working on.

## Signal Detection Patterns

### When you mention

**Feature Development**

- Keywords: `feature`, `build`, `develop`, `create`
- Suggest: `/prd`, `/rice-score`, `/architecture`
- Context: Check if PRD exists, if scored, if architecture defined

**Customer Feedback**

- Keywords: `customer`, `feedback`, `signal`, `complaint`, `request`
- Suggest: `/signal-review`, `/customer-interview`, `/journey-map`
- Context: Check signal quality, frequency, existing reviews

**Prioritization**

- Keywords: `priorit`, `roadmap`, `backlog`, `next`
- Suggest: `/rice-score`, `/roadmap`, `/decision-log`
- Context: Check existing scores, roadmap status, capacity

**AI Features**

- Keywords: `AI`, `LLM`, `model`, `ML`, `machine learning`
- Suggest: `/ai-guardrails`, `/ai-review`, `/architecture`
- Context: Check if guardrails defined, production readiness

**Incidents**

- Keywords: `incident`, `outage`, `failure`, `down`, `broken`
- Suggest: `/incident-review`, `/postmortem`, `/architecture`
- Context: Check if postmortem exists, action items tracked

**Architecture**

- Keywords: `system`, `architecture`, `design`, `integration`
- Suggest: `/architecture`, `/review engineering-lead`, `/review platform-architect`
- Context: Check if bounded context defined, ownership clear

**Release Planning**

- Keywords: `release`, `ship`, `deploy`, `launch`
- Suggest: `/release-plan`, `/changelog`, `/comms`
- Context: Check readiness, dependencies, rollback plan

**Research**

- Keywords: `research`, `interview`, `test`, `validate`
- Suggest: `/customer-interview`, `/ux-research`, `/signal-review`
- Context: Check research plan, participant criteria

**Decision Making**

- Keywords: `decide`, `decision`, `should we`, `options`
- Suggest: `/decision-log`, `/review critical-thinker`, `/rice-score`
- Context: Check if options scored, risks assessed

**Trust & Safety**

- Keywords: `risk`, `safety`, `compliance`, `trust`, `security`
- Suggest: `/review trust-safety`, `/ai-guardrails`, `/incident-review`
- Context: Check risk assessment, compliance requirements

## Workflow Chains

Common sequences of commands:

1. **New Feature Flow**

   ```
   /signal-review → /customer-interview → /prd → /rice-score → /architecture → /review engineering-lead → /roadmap
   ```

2. **AI Feature Flow**

   ```
   /prd → /ai-guardrails → /architecture → /ai-review → /review trust-safety → /release-plan
   ```

3. **Incident Response Flow**

   ```
   /incident-review → /postmortem → /decision-log → /architecture (update) → /runbook (update)
   ```

4. **Prioritization Flow**

   ```
   /signal-review → /rice-score → /roadmap → /decision-log → /comms
   ```

## Context Awareness

### Check before suggesting

- **Has this been scored?** → Look in `tracker/scores/`
- **Is there a PRD?** → Look in `projects/`
- **Is architecture defined?** → Look in `context/architecture/`
- **Are there related signals?** → Look in `tracker/signals/`
- **Is this on the roadmap?** → Look in `projects/roadmap-*.md`
- **Has this been decided?** → Look in `DECISIONS.md`

### Smart Reminders

- If working on AI feature without guardrails → Remind about `/ai-guardrails`
- If PRD exists but no RICE score → Suggest `/rice-score`
- If high-impact feature without architecture → Suggest `/architecture`
- If incident without postmortem → Suggest `/incident-review`
- If customer feedback without signal review → Suggest `/signal-review`

## Learning Patterns

Track and learn from:

- Which commands Ryan uses together
- Which reviews he requests most often
- Which frameworks he applies to which problems
- Which agents provide the most value
- Which suggestions he acts on vs. ignores
