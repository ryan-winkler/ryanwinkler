# AI in production

AI in production means the product is accountable for real-world outcomes: users rely on it, decisions are logged, and failure modes are managed like any other system. It is not a demo or a lab exercise; it is part of the operating surface.

## Guardrails

- **Handoff**: clear paths to a human when uncertainty is high.
- **Refusal**: safe, plain-language refusals when a request is out of scope.
- **Escalation**: explicit triggers for review and intervention.
- **Confidence and uncertainty**: the system should surface how sure it is, and when it is unsure.

## Observability

Measure what the system does and what users do after it acts.

- Input quality (missing context, ambiguous requests).
- Output quality (accuracy, helpfulness, alignment with policy).
- User behaviour (acceptance, edits, overrides, time saved).
- System behaviour (latency, cost per request, drift over time).

## Failure modes

- Over-confident answers on uncertain inputs.
- Silent refusal that looks like a successful action.
- Policy gaps where the model behaves inconsistently.
- Feedback loops that amplify low-quality signal.
- Automation bias where users stop checking outputs.

## Rollback expectations

- A kill switch that can disable AI behaviour quickly.
- Safe defaults that keep core flows working without AI.
- Reversible changes with clear ownership.

## Adoption

- Users need to understand what the system can and cannot do.
- Trust grows when the model is predictable and transparent about limits.
- Human override is a feature, not a failure.

## Exploratory pattern: inference efficiency + behavioural abuse signals

In production, inference efficiency shows up as a product and CX problem. Distributed inference on consumer-grade GPUs can create uneven latency, repeated work, and higher support load when behaviour is inconsistent. These are not just engineering details; they change how users judge reliability.

Long-context usage and KV cache behaviour are practical constraints that shape how the product feels. They affect tail latency, cost predictability, and how often the system can safely reuse past work without confusing the user.

Lightweight similarity or fingerprinting techniques (for example, Nilsimsa-style approaches) can help with routing, dedupe, and caching. They are not security magic. Temporal and behavioural signals can act as early warning indicators for abuse patterns, not guarantees.

Observed leverage points (conceptual):
- Request shaping to reduce repeated work.
- Routing based on similarity and context size.
- Cache policies aligned to user-visible behaviour.
- Guardrails that degrade gracefully under load.
- Early warning flags from temporal and behavioural patterns.

### Pre-launch minimum bar

- [ ] Guardrails are documented and enforced.
- [ ] Escalation paths are tested with real scenarios.
- [ ] Key metrics are defined and monitored.
- [ ] Rollback plan is written and owned.
- [ ] Users have a clear way to correct or override outputs.
