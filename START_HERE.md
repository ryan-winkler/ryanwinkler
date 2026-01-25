# Start Here 👋

**Welcome to my product operating system.** This repository demonstrates how I approach product management in practice.

---

## ⚡ Quick Start (30 seconds)

**I'm a hiring manager looking for**:

- [AI Product / AI Platform](#ai-product--ai-platform) →
- [Trust / Risk / Safety](#trust--risk--compliance--safety) →
- [Internal Platforms / Dev Tooling](#internal-platforms--developer-tooling) →
- [Customer-Facing Product](#customer-facing-product) →

**I want to**:

- [Browse by topic](index/README.md) — Organized content index
- [Search for something](docs/SEARCH.md) — Grep examples and search guide
- [See the big picture](README.md) — Full README with everything

---

## 📚 Core Documents (Start Here)

| Document | What It Covers | Time to Read |
| :--- | :--- | :--- |
| [README.md](README.md) | Complete overview, structure, navigation | 5 min |
| [HOW_I_WORK.md](core/HOW_I_WORK.md) | Operating principles and habits | 3 min |
| [AI_IN_PRODUCTION.md](core/AI_IN_PRODUCTION.md) | AI production framework | 4 min |
| [PRIORITISATION_SYSTEM.md](core/PRIORITISATION_SYSTEM.md) | RICE/DRICE prioritization | 3 min |
| [SIGNAL_TO_DECISION.md](core/SIGNAL_TO_DECISION.md) | Signal intake process | 2 min |

---

## 🎯 For Hiring Managers

### AI Product / AI Platform

**Read** (10 min):

- [AI_IN_PRODUCTION.md](core/AI_IN_PRODUCTION.md) — My framework for AI in production
- [runbooks/ai/production-readiness-check.md](runbooks/ai/production-readiness-check.md) — Pre-launch checklist
- [insights/patterns/ai-guardrails-non-negotiable.md](insights/patterns/ai-guardrails-non-negotiable.md) — Why guardrails matter

**What you'll see**:

- ✅ Guardrails framework (handoff, refusal, confidence, policy)
- ✅ Observability requirements (metrics, logs, alerts)
- ✅ Failure mode analysis and rollback procedures

**Quick search**:

```bash
grep -r "guardrails\|observability\|rollback" runbooks/ insights/
```

---

### Trust / Risk / Compliance / Safety

**Read** (8 min):

- [ARCHITECTURE.md](core/ARCHITECTURE.md) — System boundaries and failure modes
- [DECISIONS.md](core/DECISIONS.md) — Decision log with rationale
- [templates/template_incident_review.md](templates/template_incident_review.md) — Postmortem template

**What you'll see**:

- ✅ Blameless incident review process
- ✅ Risk assessment and mitigation
- ✅ Explicit ownership and escalation paths

**Quick search**:

```bash
grep -r "risk\|compliance\|incident" templates/ runbooks/
```

---

### Internal Platforms / Developer Tooling

**Read** (8 min):

- [SIGNAL_TO_DECISION.md](core/SIGNAL_TO_DECISION.md) — Signal intake and triage
- [DOMAIN_MAP.md](core/DOMAIN_MAP.md) — Bounded contexts and ownership
- [templates/template_rfc.md](templates/template_rfc.md) — RFC template

**What you'll see**:

- ✅ Domain-driven design in practice
- ✅ Signal quality assessment
- ✅ Knowledge-centered service approach

**Quick search**:

```bash
grep -r "domain\|signal\|RFC" knowledge/ templates/
```

---

### Customer-Facing Product

**Read** (8 min):

- [HOW_I_WORK.md](core/HOW_I_WORK.md) — Customer-centric principles
- [PRIORITISATION_SYSTEM.md](core/PRIORITISATION_SYSTEM.md) — Customer journey focus
- [insights/patterns/sync-delays-break-trust.md](insights/patterns/sync-delays-break-trust.md) — Trust patterns

**What you'll see**:

- ✅ End-to-end customer journey thinking
- ✅ Evidence-based prioritization
- ✅ Customer research methodology

**Quick search**:

```bash
grep -r "customer\|journey\|trust" insights/ workflows/
```

---

## 🗂️ Browse by Topic

[**Topic Index →**](index/README.md)

Organized content by subject area:

- AI in Production
- Product Prioritization
- Customer Research
- Domain Driven Design
- Trust & Safety
- Incident Response
- Knowledge Management
- Product Strategy
- Operational Excellence

---

## 🔍 Search This Repository

[**Search Guide →**](docs/SEARCH.md)

Quick examples:

```bash
# AI and production
grep -r "AI\|guardrails\|production" runbooks/ insights/

# Prioritization
grep -r "RICE\|priorit" knowledge/ templates/

# Customer research
grep -r "customer\|interview" workflows/ templates/
```

---

## 📁 Repository Structure

```text
ryanwinkler/
├── 📘 Core Documents          # Start here
├── 📚 Knowledge Base          # Frameworks & insights
├── 🔧 Operational Systems     # How to execute
├── 📊 Active Work             # Track & execute
└── 🧠 Memory & Learning       # Continuous improvement
```

[See full structure →](README.md#-repository-structure)

---

## 🎓 Learning Paths

### Path 1: AI Product Manager (30 min)

1. [AI_IN_PRODUCTION.md](core/AI_IN_PRODUCTION.md) — 4 min
2. [runbooks/ai/production-readiness-check.md](runbooks/ai/production-readiness-check.md) — 10 min
3. [workflows/ai-feature-launch.md](workflows/ai-feature-launch.md) — 8 min
4. [insights/patterns/ai-guardrails-non-negotiable.md](insights/patterns/ai-guardrails-non-negotiable.md) — 5 min
5. [templates/template_ai_guardrails.md](templates/template_ai_guardrails.md) — 3 min

### Path 2: Product Operations (25 min)

1. [HOW_I_WORK.md](core/HOW_I_WORK.md) — 3 min
2. [PRIORITISATION_SYSTEM.md](core/PRIORITISATION_SYSTEM.md) — 3 min
3. [runbooks/product/quarterly-roadmap-planning.md](runbooks/product/quarterly-roadmap-planning.md) — 10 min
4. [workflows/new-feature.md](workflows/new-feature.md) — 6 min
5. [templates/template_prd.md](templates/template_prd.md) — 3 min

### Path 3: Trust & Safety (20 min)

1. [ARCHITECTURE.md](core/ARCHITECTURE.md) — 3 min
2. [insights/patterns/sync-delays-break-trust.md](insights/patterns/sync-delays-break-trust.md) — 5 min
3. [insights/patterns/ai-guardrails-non-negotiable.md](insights/patterns/ai-guardrails-non-negotiable.md) — 5 min
4. [templates/template_incident_review.md](templates/template_incident_review.md) — 5 min
5. [DECISIONS.md](core/DECISIONS.md) — 2 min

### Path 4: Customer Research (20 min)

1. [SIGNAL_TO_DECISION.md](core/SIGNAL_TO_DECISION.md) — 2 min
2. [SIGNAL_SCORECARD.md](core/SIGNAL_SCORECARD.md) — 3 min
3. [workflows/new-feature.md](workflows/new-feature.md) — 6 min
4. [templates/template_signal_review.md](templates/template_signal_review.md) — 5 min
5. [knowledge/frameworks.md](knowledge/frameworks.md) — 4 min

---

## 🛠️ What's Inside

| Category | Count | Examples |
| :--- | :--- | :--- |
| **Frameworks** | 7 | RICE, DDD, KCS, Customer Journey |
| **Runbooks** | 2 | Roadmap planning, AI readiness |
| **Workflows** | 3 | Feature dev, AI launch, research |
| **Templates** | 7+ | PRD, RFC, incident review, AI guardrails |
| **Insights** | 2 | Trust patterns, AI safety |

---

## 🧑‍💼 About Me

**Ryan Winkler** — Senior Product Manager, Dublin, Ireland

I build customer-facing and internal systems, including AI-enabled workflows, trust-sensitive platforms, and tooling for decision-making in production.

**Focus areas**:

- AI in production (guardrails, observability, safety)
- Trust-sensitive platforms (compliance, risk, reliability)
- Customer signal to decision loops (KCS, DDD, journey mapping)

[All profiles →](README.md#-connect)

---

## 🔗 Quick Links

- [README](README.md) — Complete overview
- [Topic Index](index/README.md) — Browse by subject
- [Search Guide](docs/SEARCH.md) — Find anything
- [How I Work](core/HOW_I_WORK.md) — Operating principles
- [AI in Production](core/AI_IN_PRODUCTION.md) — AI framework

---

_These materials reflect how I approach product work in practice and are shared for reference._

**Last updated**: 2026-01-25
