# Search Guide

This repository is intentionally searchable.

Use `rg` from the repo root.

## Quick examples

```bash
# Current public story, including deprecated AI tooling names
rg -n "Dublin|Zendesk|HiveNet|Meitheal|Moltis|ZeroClaw|Nemoclaw" README.md START_HERE.md NOW.md CHANGELOG.md projects/

# AI and evaluation
rg -n "AI|guardrails|quality|fallback|escalation" core/ knowledge/ runbooks/ insights/ projects/

# Internal platforms and developer tooling
rg -n "platform|internal|developer|workflow|DDD" core/ knowledge/ projects/ templates/

# Trust, risk, and compliance
rg -n "trust|risk|compliance|incident|policy" core/ insights/ runbooks/

# Signal, feedback loops, and KCS
rg -n "signal|feedback|KCS|knowledge" core/ runbooks/ templates/ insights/

# Curated outside tools and reading
rg -n "Get Shit Done|Operator OS|Moltis|Ollama|Integrity Institute" BOOKMARKS.md
```

## Browse by area

```bash
rg --files core
rg --files knowledge
rg --files projects
rg --files runbooks
rg --files templates
rg --files workflows
```

## Follow what changed

```bash
rg -n "^## \\[" CHANGELOG.md
rg -n "Meitheal|Coolock|Moltis|ZeroClaw|Nemoclaw" NOW.md README.md projects/
```

## Find the public project notes

```bash
rg -n "## Summary|## The product problem|## Why it matters now|## Current lessons" projects/
```

## Find reusable tools

```bash
rg -n "Template|Checklist|Runbook|Workflow" templates/ runbooks/ workflows/
```

## Find product proof points

```bash
rg -n "48 business hours|Improved reliability|135%|40\\+ engineering teams" README.md projects/ NOW.md docs/PROOF_NOTES.md
```
