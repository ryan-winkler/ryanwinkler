# Personal Copilot Workflow

**Date**: 2026-01-25
**Context**: Adapted from "Ultimate Claude Code Masterclass" patterns.
**Tags**: `workflow`, `automation`, `productivity`, `copilot`, `mcp`

## Observation

Most "AI Copilots" are just chat windows. A true *Personal Copilot* has context on your schedule, your tasks, and your active documents.

## Why It Matters

Context switching kills productivity. If you have to copy-paste your schedule into an AI to get a briefing, you won't do it. If the AI *already knows* your schedule, it can proactively prepare you.

## The "Start Day" Trigger

Create a simple local prompt/script that acts as a daily initialization:

1. **Read Context**:
    * Connect to Calendar (via MCP).
    * Read active `TODO.md` or task list.
    * Read `NOW.md` (current focus).

2. **Synthesize**:
    * match tasks to free blocks.
    * Flag conflicts or missing prep.
    * Draft briefing notes for upcoming 1:1s based on previous running notes.

## Implementation Pattern

```
# .claude/prompts/morning-briefing.md

You are my Chief of Staff.
1. Read my calendar for today (using google-calendar-mcp).
2. Read my 'tracker/todos.md' file.
3. Read 'NOW.md'.

Output a briefing:
- What is the one thing I must ship today?
- What meetings am I unprepared for? (Check if I have notes in 'memory/meetings/' for these people).
- Suggest a schedule block for deep work.
```

## When to Apply

* **Daily Start**: Run this first thing in the morning.
* **Context Recovery**: Run it after a vacation to get back up to speed.
* **Weekly Review**: Adapt the prompt to look back at the week's completed items.
