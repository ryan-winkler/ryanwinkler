# Ryan Winkler — Public Product Operating System

**Website**: [ryanw.eu](https://ryanw.eu)  
**Location**: Dublin, Ireland

I’m Ryan Winkler, a Senior Product Manager in Dublin. This repository is the public version of how I work: product frameworks, runbooks, project notes, and reusable templates shaped by trust and compliance work at Zendesk, hands-on AI evaluation work, and the systems I build in public.

This is not a full CV. It is the smallest useful public set of artifacts that shows what I am good at, what I keep current, and how I turn product work into something other people can actually reuse.

## Selected Proof Points

| Area | Evidence | Start here |
| --- | --- | --- |
| Trust and compliance | Built a Compliance Agreements platform at Zendesk that cut turnaround from roughly 30 days to 48 business hours | [docs/PROOF_NOTES.md#compliance-agreements-turnaround](docs/PROOF_NOTES.md#compliance-agreements-turnaround) |
| Reliability and customer trust | Improved reliability and reduced repeat complaints on a trust-sensitive transparency surface | [docs/PROOF_NOTES.md#access-logs-reliability-and-trust](docs/PROOF_NOTES.md#access-logs-reliability-and-trust) |
| Internal platforms and developer flow | Helped scale an internal platform used across 40+ engineering teams and introduced a micro-frontend approach that increased contributing PRs by 135% | [docs/PROOF_NOTES.md#internal-platform-adoption-and-contribution-flow](docs/PROOF_NOTES.md#internal-platform-adoption-and-contribution-flow) |
| AI evaluation in production | In a short HiveNet contract, reviewed real Intercom Fin conversations, tuned escalation paths, tagged edge cases, and set quality thresholds | [docs/PROOF_NOTES.md#ai-evaluation-in-production](docs/PROOF_NOTES.md#ai-evaluation-in-production) |

Short public context for those metrics lives in [docs/PROOF_NOTES.md](docs/PROOF_NOTES.md).

## Call Me When

- trust, compliance, or policy work needs to become clearer inside the product
- an internal platform or developer workflow needs better ownership, structure, or adoption
- AI needs real evaluation, fallback paths, and quality thresholds instead of demo language
- a local-first or operationally messy system needs clearer boundaries and better day-two behavior

## What Is Current

| System | Status | Why it matters now |
| --- | --- | --- |
| [Meitheal](projects/meitheal.md) | Active | A Home Assistant-native, local-first execution hub that makes DDD, KCS, and human-plus-agent workflows visible inside a real system |
| [Coolock Village Forge](projects/coolock-village-forge.md) | Active | A civic coordination site that keeps clarity, search, accessibility, and public trust tied to real local use |
| [AI gateway tooling notes](projects/moltis-zeroClaw.md) | Current / deprecated / emerging | Moltis is the live AI gateway. ZeroClaw is deprecated as of March 2026. Nemoclaw is part of the naming thread around what may come next, but it is not the canonical live system today |

## Start Here

| If you want to... | Start here |
| --- | --- |
| Get the current overview | [START_HERE.md](START_HERE.md) |
| See what I am focused on now | [NOW.md](NOW.md) |
| Understand how I work | [core/HOW_I_WORK.md](core/HOW_I_WORK.md) |
| See how I turn signal into decisions | [core/SIGNAL_TO_DECISION.md](core/SIGNAL_TO_DECISION.md) |
| Read the public project notes | [projects/README.md](projects/README.md) |
| Borrow the frameworks and templates | [knowledge/frameworks.md](knowledge/frameworks.md), [templates/](templates/), [runbooks/](runbooks/) |
| Browse the full power-user index | [index/README.md](index/README.md) |

## What You Can Reuse

### Operating frameworks

- [How I Work](core/HOW_I_WORK.md)
- [AI in Production](core/AI_IN_PRODUCTION.md)
- [Signal to Decision](core/SIGNAL_TO_DECISION.md)
- [Prioritisation System](core/PRIORITISATION_SYSTEM.md)
- [Domain Map](core/DOMAIN_MAP.md)
- [Frameworks Reference](knowledge/frameworks.md)

### Delivery assets

- [Quarterly Roadmap Planning](runbooks/product/quarterly-roadmap-planning.md)
- [AI Production Readiness Check](runbooks/ai/production-readiness-check.md)
- [PRD Template](templates/template_prd.md)
- [RFC Template](templates/template_rfc.md)
- [RICE / DRICE Template](templates/template_rice_drice.md)
- [Signal Review Template](templates/template_signal_review.md)
- [Incident Review Template](templates/template_incident_review.md)
- [AI Guardrails Template](templates/template_ai_guardrails.md)
- [Runbook Template](templates/template_runbook.md)

## If You Are Evaluating Fit

| Angle | Read this |
| --- | --- |
| AI product and evaluation | [core/AI_IN_PRODUCTION.md](core/AI_IN_PRODUCTION.md), [projects/moltis-zeroClaw.md](projects/moltis-zeroClaw.md) |
| Internal platforms and developer tooling | [core/SIGNAL_TO_DECISION.md](core/SIGNAL_TO_DECISION.md), [core/DOMAIN_MAP.md](core/DOMAIN_MAP.md), [projects/meitheal.md](projects/meitheal.md) |
| Trust, risk, and compliance | [core/ARCHITECTURE.md](core/ARCHITECTURE.md), [insights/patterns/ai-guardrails-non-negotiable.md](insights/patterns/ai-guardrails-non-negotiable.md) |
| Customer signal and operational clarity | [core/HOW_I_WORK.md](core/HOW_I_WORK.md), [runbooks/product/quarterly-roadmap-planning.md](runbooks/product/quarterly-roadmap-planning.md) |

## Selected References

These are the outside resources I come back to most often and have kept intentionally small.

- [RICE: Simple Prioritization for Product Managers](https://www.intercom.com/blog/rice-simple-prioritization-for-product-managers/)
- [DomainDrivenDesign](https://martinfowler.com/bliki/DomainDrivenDesign.html) by Martin Fowler
- [KCS v6 Methodology](https://www.serviceinnovation.org/kcs/)
- [The Four Big Risks](https://www.svpg.com/four-big-risks/)
- [Introducing DRICE](https://www.lennysnewsletter.com/p/introducing-drice-a-modern-prioritization)

## Connect

- [ryanw.eu](https://ryanw.eu)
- [ryanw.eu/llms.txt](https://ryanw.eu/llms.txt)
- [LinkedIn](https://www.linkedin.com/in/ryan-winkler-dublin-pm/)
- [GitHub](https://github.com/ryan-winkler)

_These materials reflect how I approach product work in practice and are kept public because useful systems should be shareable._

**Last updated**: 2026-03-19
