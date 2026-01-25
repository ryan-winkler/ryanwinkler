# AI Context Engineering

**Date**: 2026-01-25
**Context**: Adapted from the "Get Shit Done" methodology for AI-driven development.
**Tags**: `ai`, `operations`, `context`, `engineering`, `workflow`

## Observation

AI agents degrade in quality when context windows get cluttered. To maintain high performance, context must be engineered, not just dumped.

## Why It Matters

"Context Engineering" is the new "Requirements Gathering." If you feed an AI a messy, 100k-token history, it gets confused. If you feed it structured, atomic context, it performs like a senior engineer.

## The "Context-First" Loop

Instead of one long chat, break work into four distinct phases with fresh context for each:

1. **Discuss** (Context Shaping):
    * Goal: Capture preferences *before* planning.
    * Output: `CONTEXT.md` (Design decisions, API styles, constraints).
    * *Why*: prevents the AI from guessing your taste during execution.

2. **Plan** (Research & Architect):
    * Goal: Create atomic plans without writing code.
    * Output: `PLAN.md` (Step-by-step XML/structured tasks).
    * *Why*: separating planning from coding prevents "coding yourself into a corner."

3. **Execute** (Atomic Action):
    * Goal: Implement the plan in a *fresh* context window.
    * Method: 1 Task = 1 Context = 1 Commit.
    * *Why*: Keeps the AI sharp. No accumulated garbage from previous turns.

4. **Verify** (Human-in-the-Loop):
    * Goal: Confirm it works as expected, not just that tests pass.
    * Output: `UAT.md` (User Acceptance Testing results).
    * *Why*: Automated tests catch bugs; humans catch misunderstandings.

## Application

When assigning work to AI agents (or human teams):

1. **Externalize State**: Don't keep the plan in the chat history. Maintain a `STATE.md` or `ROADMAP.md` that is the single source of truth.
2. **Reset Often**: Don't be afraid to clear context once a task is done. The `PROJECT.md` and `REQUIREMENTS.md` provide enough continuity.
3. **review-driven**: Verify work *before* moving to the next phase.

## Related

* [AI_IN_PRODUCTION.md](../../core/AI_IN_PRODUCTION.md)
* [How I Work](../../core/HOW_I_WORK.md)
