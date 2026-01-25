# Ryan Winkler — Product Operating System

**Product manager based in Dublin, Ireland**

This repository is a working product operating system for AI in production, trust-sensitive platforms, and customer signal to decision loops. It demonstrates how I approach product work in practice.

---

## What This Is

A systematic approach to product management that combines:

- **Proven frameworks** — RICE/DRICE, Domain Driven Design, Knowledge-Centered Service, Customer Journey
- **Operational rigor** — Runbooks, decision logs, signal scorecards
- **AI in production** — Guardrails, observability, failure modes, rollback procedures
- **Knowledge capture** — Insights, patterns, and learnings from shipped work

This is not theoretical. These are the actual systems, templates, and procedures I use to ship products that work in production.

---

## Repository Structure

```
├── 📘 Core Documents
│   ├── START_HERE.md              # Begin here
│   ├── HOW_I_WORK.md              # Operating principles
│   ├── AI_IN_PRODUCTION.md        # AI production framework
│   ├── PRIORITISATION_SYSTEM.md   # How I prioritize
│   └── SIGNAL_TO_DECISION.md      # Signal intake process
│
├── 📚 Knowledge Base
│   ├── knowledge/                 # PM frameworks (RICE, DDD, KCS, etc.)
│   ├── insights/                  # Patterns and learnings from shipped work
│   └── context/                   # Domain knowledge and architecture
│
├── 🔧 Operational Systems
│   ├── runbooks/                  # Repeatable procedures
│   ├── workflows/                 # End-to-end processes
│   └── templates/                 # Document templates
│
├── 📊 Active Work
│   ├── tracker/                   # Signals, scores, incidents
│   ├── projects/                  # PRDs and specs
│   └── research/                  # Customer research artifacts
│
└── 🧠 Memory & Learning
    └── memory/                    # Decisions, preferences, patterns
```

---

## For Hiring Managers

### If you're hiring for AI Product / AI Platform

**Read**:

- [AI_IN_PRODUCTION.md](AI_IN_PRODUCTION.md) — My framework for AI in production
- [runbooks/ai/production-readiness-check.md](runbooks/ai/production-readiness-check.md) — Pre-launch checklist
- [insights/patterns/ai-guardrails-non-negotiable.md](insights/patterns/ai-guardrails-non-negotiable.md) — Why guardrails matter

**See**:

- Guardrails framework (handoff, refusal, confidence, policy)
- Observability requirements (metrics, logs, alerts)
- Failure mode analysis and rollback procedures

### If you're hiring for Trust / Risk / Compliance / Safety

**Read**:

- [ARCHITECTURE.md](ARCHITECTURE.md) — System boundaries and failure modes
- [DECISIONS.md](DECISIONS.md) — Decision log with rationale
- [templates/template_incident_review.md](templates/template_incident_review.md) — Postmortem template

**See**:

- Blameless incident review process
- Risk assessment and mitigation
- Explicit ownership and escalation paths

### If you're hiring for Internal Platforms / Developer Tooling

**Read**:

- [SIGNAL_TO_DECISION.md](SIGNAL_TO_DECISION.md) — Signal intake and triage
- [DOMAIN_MAP.md](DOMAIN_MAP.md) — Bounded contexts and ownership
- [templates/template_rfc.md](templates/template_rfc.md) — RFC template

**See**:

- Domain-driven design in practice
- Signal quality assessment
- Knowledge-centered service approach

### If you're hiring for Customer-Facing Product

**Read**:

- [HOW_I_WORK.md](HOW_I_WORK.md) — Customer-centric principles
- [PRIORITISATION_SYSTEM.md](PRIORITISATION_SYSTEM.md) — Customer journey focus
- [insights/patterns/sync-delays-break-trust.md](insights/patterns/sync-delays-break-trust.md) — Trust patterns

**See**:

- End-to-end customer journey thinking
- Evidence-based prioritization
- Customer research methodology

---

## Key Frameworks

### RICE / DRICE Prioritization

Systematic scoring for feature prioritization:

- **RICE** = (Reach × Impact × Confidence) / Effort
- **DRICE** adds Dependencies and Risk for complex work

See: [PRIORITISATION_SYSTEM.md](PRIORITISATION_SYSTEM.md)

### Domain Driven Design

Clear boundaries, explicit ownership, ubiquitous language:

- Bounded contexts define system boundaries
- Ownership is explicit, not shared
- Language is consistent across teams and tools

See: [DOMAIN_MAP.md](DOMAIN_MAP.md), [ARCHITECTURE.md](ARCHITECTURE.md)

### Knowledge-Centered Service

Knowledge as a product surface:

- Capture in the flow of work
- Signal quality drives decisions
- Documentation is a first-class concern

See: [SIGNAL_SCORECARD.md](SIGNAL_SCORECARD.md), [runbooks/](runbooks/)

### Customer Journey Mapping

End-to-end experience thinking:

- Map friction points by journey stage
- Assess severity and frequency
- Prioritize trust-impacting issues

See: [PRIORITISATION_SYSTEM.md](PRIORITISATION_SYSTEM.md)

---

## Operational Highlights

### Runbooks for Repeatable Work

If you do it twice, document it:

- [Quarterly Roadmap Planning](runbooks/product/quarterly-roadmap-planning.md)
- [AI Production Readiness Check](runbooks/ai/production-readiness-check.md)

### Product Insights

Patterns and learnings from shipped work:

- [Sync Delays Break Trust](insights/patterns/sync-delays-break-trust.md)
- [AI Guardrails Are Non-Negotiable](insights/patterns/ai-guardrails-non-negotiable.md)

### Decision Logs

Explicit decisions with rationale:

- What was decided and why
- Options considered and trade-offs
- Reversibility and review dates

See: [DECISIONS.md](DECISIONS.md)

---

## How I Work

**Core principles**:

- Everything is a signal — customer conversations, incidents, edge cases
- Write decisions down — even when they feel obvious
- Clarify boundaries early — use DDD for ownership
- Prefer evidence over opinion — data and examples, not hunches
- Set feedback loops before shipping — know how to measure success

**Operational habits**:

- Runbooks for repeatable work
- Meetings for coordination, not discovery
- Async-first communication
- Blameless postmortems
- Knowledge capture in the flow of work

See: [HOW_I_WORK.md](HOW_I_WORK.md)

---

## AI in Production

My approach to AI features:

**Guardrails** (non-negotiable):

- Handoff — when to escalate to humans
- Refusal — safe handling of out-of-scope requests
- Confidence — surface uncertainty to users
- Policy — enforce compliance and safety

**Observability**:

- Input quality, output quality, user behavior, system behavior
- Metrics, logs, alerts from day one
- Dashboards for monitoring

**Failure Modes**:

- Over-confident answers on uncertain inputs
- Silent failures that look like success
- Policy gaps and inconsistencies
- Feedback loops amplifying bad outputs

**Rollback**:

- Kill switch tested before launch
- Safe defaults when AI is disabled
- Clear triggers and ownership

See: [AI_IN_PRODUCTION.md](AI_IN_PRODUCTION.md)

---

## Templates & Tools

**Product Development**:

- [PRD Template](templates/template_prd.md)
- [RICE/DRICE Scoring](templates/template_rice_drice.md)
- [RFC Template](templates/template_rfc.md)

**Research & Signals**:

- [Signal Review](templates/template_signal_review.md)
- [Customer Interview Guide](templates/)

**Incidents & Operations**:

- [Incident Review](templates/template_incident_review.md)
- [Runbook Template](templates/template_runbook.md)

**AI Features**:

- [AI Guardrails](templates/template_ai_guardrails.md)
- [Production Readiness Checklist](runbooks/ai/production-readiness-check.md)

---

## About Me

**Ryan Winkler**  
Senior Product Manager, Dublin, Ireland

I build customer-facing and internal systems, including AI-enabled workflows, trust-sensitive platforms, and tooling for decision-making in production. I turn customer conversations and operational signal into clear decisions and shipped systems.

**Experience**:

- Zendesk (trust, transparency, compliance surfaces)
- Intercom Fin (AI in production, live environment)

**Focus areas**:

- AI in production (guardrails, observability, safety)
- Trust-sensitive platforms (compliance, risk, reliability)
- Customer signal to decision loops (KCS, DDD, journey mapping)

---

## Connect

- **Website**: [ryanw.eu](https://ryanw.eu)
- **Machine-readable profile**: [ryanw.eu/llms.txt](https://ryanw.eu/llms.txt)
- **LinkedIn**: [ryan-winkler-dublin-pm](https://www.linkedin.com/in/ryan-winkler-dublin-pm/)
- **X**: [@ryanw_product](https://x.com/ryanw_product)
- **GitHub**: [ryan-winkler](https://github.com/ryan-winkler)
- **Wellfound**: [ryanw-eu-product-manager-dublin](https://wellfound.com/u/ryanw-eu-product-manager-dublin)
- **Crunchbase**: [ryan-winkler-b002](https://www.crunchbase.com/person/ryan-winkler-b002)
- **Wikidata**: [Q137838541](https://www.wikidata.org/wiki/Q137838541)
- **Clay**: [Ryan-Winkler-Product-Manager](https://clay.earth/profile/Ryan-Winkler-Product-Manager)

---

## Resources

This repository is part of a broader product management community. Here are other valuable resources:

### Product Management Collections

- [Awesome Product Management](https://github.com/dend/awesome-product-management) by [@dend](https://github.com/dend) — Curated list of PM resources, tools, and articles
- [Awesome Product Manager](https://github.com/yuhenobi/awesome-product-manager) by [@yuhenobi](https://github.com/yuhenobi) — Curated resources for product managers to learn and grow
- [Open Product Management](https://github.com/ProductHired/open-product-management) by [@ProductHired](https://github.com/ProductHired) — PM advice for technical people
- [Lenny's Podcast Transcripts](https://github.com/ChatPRD/lennys-podcast-transcripts) by [@ChatPRD](https://github.com/ChatPRD) — Searchable transcripts from Lenny's Podcast
- [LogChimp](https://github.com/logchimp/logchimp) by [@logchimp](https://github.com/logchimp) — Open-source customer feedback and product roadmap tool
- [Awesome Claude Skills](https://github.com/ComposioHQ/awesome-claude-skills) by [@ComposioHQ](https://github.com/ComposioHQ) — Claude AI customization and workflows

### Related Topics

- **Product Management** — Frameworks, prioritization, decision-making
- **AI in Production** — Guardrails, observability, safety, rollback
- **Domain Driven Design** — Bounded contexts, ubiquitous language, ownership
- **Knowledge-Centered Service** — Signal quality, knowledge capture, documentation
- **Trust & Safety** — Risk assessment, compliance, incident response
- **Operational Excellence** — Runbooks, procedures, repeatability

---

## License

This work is shared under the [Creative Commons Attribution 4.0 International License](LICENSE).

You're welcome to use these frameworks, templates, and approaches in your own work. Attribution appreciated but not required.

---

_These materials reflect how I approach product work in practice and are shared for reference._
