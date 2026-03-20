# Browse by Topic

Use this page when you already know the kind of material you want.

If you want the shortest route through the repo, start with [README.md](../README.md).

---

## AI in Production

**Core Documents**:

- [AI_IN_PRODUCTION.md](../core/AI_IN_PRODUCTION.md) — Framework for AI in production
- [runbooks/ai/production-readiness-check.md](../runbooks/ai/production-readiness-check.md) — Pre-launch checklist

**Insights**:

- [AI Guardrails Are Non-Negotiable](../insights/patterns/ai-guardrails-non-negotiable.md)

**Templates**:

- [AI Guardrails Template](../templates/template_ai_guardrails.md)

**Workflows**:

- [AI Feature Launch](../workflows/ai-feature-launch.md)

**Search**:

```bash
rg -n "AI|guardrails|production|observability" runbooks/ insights/ templates/
```

**Tags**: `ai`, `production`, `guardrails`, `observability`, `safety`, `rollback`

---

## Product Prioritization

**Core Documents**:

- [PRIORITISATION_SYSTEM.md](../core/PRIORITISATION_SYSTEM.md) — RICE/DRICE framework
- [SIGNAL_SCORECARD.md](../core/SIGNAL_SCORECARD.md) — Signal quality assessment

**Templates**:

- [RICE/DRICE Scoring Template](../templates/template_rice_drice.md)
- [Signal Review Template](../templates/template_signal_review.md)

**Runbooks**:

- [Quarterly Roadmap Planning](../runbooks/product/quarterly-roadmap-planning.md)

**Search**:

```bash
rg -n "RICE|DRICE|priorit|scoring" knowledge/ templates/ runbooks/
```

**Tags**: `prioritization`, `rice`, `drice`, `scoring`, `roadmap`

---

## Customer Research

**Core Documents**:

- [SIGNAL_TO_DECISION.md](../core/SIGNAL_TO_DECISION.md) — Signal intake process
- [knowledge/frameworks.md](../knowledge/frameworks.md) — Customer Journey Mapping

**Templates**:

- [Signal Review Template](../templates/template_signal_review.md)

**Workflows**:

- [New Feature Development](../workflows/new-feature.md)

**Search**:

```bash
rg -n "customer|interview|research|journey" workflows/ templates/ insights/
```

**Tags**: `customer`, `research`, `interview`, `journey`, `signal`

---

## Domain Driven Design

**Core Documents**:

- [DOMAIN_MAP.md](../core/DOMAIN_MAP.md) — Bounded contexts and ownership
- [ARCHITECTURE.md](../core/ARCHITECTURE.md) — System boundaries
- [knowledge/frameworks.md](../knowledge/frameworks.md) — DDD framework

**Templates**:

- [RFC Template](../templates/template_rfc.md)

**Search**:

```bash
rg -n "domain|bounded|context|ownership" knowledge/ templates/
```

**Tags**: `ddd`, `domain`, `architecture`, `boundaries`, `ownership`

---

## Trust & Safety

**Core Documents**:

- [AI_IN_PRODUCTION.md](../core/AI_IN_PRODUCTION.md) — AI safety framework

**Insights**:

- [Sync Delays Break Trust](../insights/patterns/sync-delays-break-trust.md)
- [AI Guardrails Are Non-Negotiable](../insights/patterns/ai-guardrails-non-negotiable.md)

**Templates**:

- [Incident Review Template](../templates/template_incident_review.md)
- [AI Guardrails Template](../templates/template_ai_guardrails.md)

**Search**:

```bash
rg -n "trust|safety|risk|compliance" insights/ templates/ runbooks/
```

**Tags**: `trust`, `safety`, `risk`, `compliance`, `incident`

---

## Incident Response

**Core Documents**:

- [DECISIONS.md](../core/DECISIONS.md) — Decision log

**Templates**:

- [Incident Review Template](../templates/template_incident_review.md)

**Runbooks**:

- [AI Production Readiness Check](../runbooks/ai/production-readiness-check.md)

**Search**:

```bash
rg -n "incident|postmortem|review" templates/ runbooks/
```

**Tags**: `incident`, `postmortem`, `review`, `response`

---

## Knowledge Management

**Core Documents**:

- [SIGNAL_SCORECARD.md](../core/SIGNAL_SCORECARD.md) — Signal quality (KCS)
- [knowledge/frameworks.md](../knowledge/frameworks.md) — KCS framework

**Runbooks**:

- [Runbooks README](../runbooks/README.md) — Runbook system

**Insights**:

- [Insights README](../insights/README.md) — Insight capture system

**Templates**:

- [Runbook Template](../templates/template_runbook.md)

**Search**:

```bash
rg -n "knowledge|KCS|runbook|insight" knowledge/ runbooks/ insights/
```

**Tags**: `knowledge`, `kcs`, `runbook`, `insight`, `documentation`

---

## Product Strategy

**Core Documents**:

- [HOW_I_WORK.md](../core/HOW_I_WORK.md) — Operating principles
- [PRIORITISATION_SYSTEM.md](../core/PRIORITISATION_SYSTEM.md) — Strategic prioritization

**Runbooks**:

- [Quarterly Roadmap Planning](../runbooks/product/quarterly-roadmap-planning.md)

**Templates**:

- [PRD Template](../templates/template_prd.md)
- [RFC Template](../templates/template_rfc.md)

**Search**:

```bash
rg -n "strategy|roadmap|planning" runbooks/ templates/
```

**Tags**: `strategy`, `roadmap`, `planning`, `prd`

---

## Operational Excellence

**Core Documents**:

- [HOW_I_WORK.md](../core/HOW_I_WORK.md) — Operational habits

**Runbooks**:

- [Quarterly Roadmap Planning](../runbooks/product/quarterly-roadmap-planning.md)
- [AI Production Readiness Check](../runbooks/ai/production-readiness-check.md)

**Search**:

```bash
rg -n "operat|runbook|checklist|incident" runbooks/ core/ insights/
```

**Tags**: `operations`, `runbook`, `execution`, `reliability`
