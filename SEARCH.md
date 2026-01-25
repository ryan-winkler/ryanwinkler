# How to Search This Repository

This repository is designed to be searchable. Here's how to find what you need.

---

## 🔍 Quick Search Examples

### By Topic

```bash
# AI and production
grep -r "AI\|guardrails\|production\|observability" runbooks/ insights/ templates/

# Prioritization and frameworks
grep -r "RICE\|DRICE\|priorit" knowledge/ templates/ runbooks/

# Customer research
grep -r "customer\|interview\|research\|journey" workflows/ templates/ insights/

# Trust and safety
grep -r "trust\|safety\|risk\|compliance" insights/ runbooks/ templates/

# Incidents and operations
grep -r "incident\|postmortem\|runbook\|procedure" templates/ runbooks/

# Domain Driven Design
grep -r "domain\|bounded\|context\|DDD" knowledge/ templates/

# Knowledge management
grep -r "knowledge\|KCS\|signal" knowledge/ insights/
```

---

## 📁 By Directory

### Find All Files of a Type

```bash
# All runbooks
find runbooks/ -name "*.md"

# All templates
find templates/ -name "*.md"

# All insights
find insights/ -name "*.md"

# All workflows
find workflows/ -name "*.md"

# All knowledge docs
find knowledge/ -name "*.md"
```

### Search Within Specific Directories

```bash
# Search only runbooks
grep -r "roadmap" runbooks/

# Search only insights
grep -r "trust" insights/

# Search only templates
grep -r "PRD" templates/

# Search only workflows
grep -r "feature" workflows/
```

---

## 🏷️ By Tag

Common tags used throughout the repository:

### AI & Production

```bash
grep -r "#ai\|#production\|#guardrails\|#observability" .
```

**Tags**: `ai`, `production`, `guardrails`, `observability`, `safety`, `rollback`, `confidence`

### Customer & Research

```bash
grep -r "#customer\|#research\|#interview\|#journey" .
```

**Tags**: `customer`, `research`, `interview`, `journey`, `signal`, `feedback`

### Trust & Safety

```bash
grep -r "#trust\|#safety\|#risk\|#compliance" .
```

**Tags**: `trust`, `safety`, `risk`, `compliance`, `incident`, `postmortem`

### Prioritization

```bash
grep -r "#prioritization\|#rice\|#drice\|#scoring" .
```

**Tags**: `prioritization`, `rice`, `drice`, `scoring`, `roadmap`, `planning`

### Operations

```bash
grep -r "#runbook\|#procedure\|#operational" .
```

**Tags**: `runbook`, `procedure`, `operational`, `repeatability`, `process`

### Knowledge

```bash
grep -r "#knowledge\|#kcs\|#documentation" .
```

**Tags**: `knowledge`, `kcs`, `documentation`, `insight`, `pattern`

---

## 📊 By Content Type

### Frameworks

```bash
grep -r "RICE\|DDD\|KCS\|Customer Journey\|LNO\|DHM" knowledge/
```

### Procedures

```bash
grep -r "runbook\|procedure\|checklist" runbooks/ templates/
```

### Patterns

```bash
grep -r "pattern\|insight\|learning" insights/
```

### Templates

```bash
grep -r "template\|PRD\|RFC\|incident" templates/
```

---

## 🎯 By Use Case

### "I'm launching an AI feature"

```bash
grep -r "AI\|guardrails\|production\|rollback" runbooks/ai/ workflows/ templates/
```

**Start with**:

- [AI Production Readiness Check](runbooks/ai/production-readiness-check.md)
- [AI Feature Launch Workflow](workflows/ai-feature-launch.md)
- [AI Guardrails Template](templates/template_ai_guardrails.md)

### "I'm planning a roadmap"

```bash
grep -r "roadmap\|planning\|RICE\|priorit" runbooks/product/ templates/
```

**Start with**:

- [Quarterly Roadmap Planning](runbooks/product/quarterly-roadmap-planning.md)
- [RICE/DRICE Template](templates/template_rice_drice.md)
- [PRIORITISATION_SYSTEM.md](PRIORITISATION_SYSTEM.md)

### "I'm doing customer research"

```bash
grep -r "customer\|interview\|research\|signal" workflows/ templates/ insights/
```

**Start with**:

- [Signal Review Template](templates/template_signal_review.md)
- [New Feature Workflow](workflows/new-feature.md)
- [SIGNAL_TO_DECISION.md](SIGNAL_TO_DECISION.md)

### "I'm responding to an incident"

```bash
grep -r "incident\|postmortem\|review" templates/ runbooks/
```

**Start with**:

- [Incident Review Template](templates/template_incident_review.md)
- [AI Production Readiness Check](runbooks/ai/production-readiness-check.md)

### "I'm writing a PRD"

```bash
grep -r "PRD\|requirements\|specification" templates/ workflows/
```

**Start with**:

- [PRD Template](templates/template_prd.md)
- [New Feature Workflow](workflows/new-feature.md)

---

## 🔎 Advanced Search

### Case-Insensitive Search

```bash
grep -ri "pattern" .
```

### Search with Context (show surrounding lines)

```bash
# Show 2 lines before and after match
grep -r -C 2 "guardrails" runbooks/
```

### Search for Multiple Terms

```bash
# Find files containing both terms
grep -r "AI" . | grep "production"
```

### Exclude Directories

```bash
# Search but exclude .git directory
grep -r --exclude-dir=.git "pattern" .
```

### Count Matches

```bash
# Count how many times a term appears
grep -r "customer" . | wc -l
```

---

## 📖 Browse by Topic

For a curated view of content by topic, see:

- [Topic Index](index/README.md) — Organized by subject area

---

## 💡 Tips

1. **Start broad, then narrow**: Search across all directories first, then drill into specific areas
2. **Use the topic index**: [index/README.md](index/README.md) provides curated paths to content
3. **Check related insights**: Many documents link to related content
4. **Use tags**: Documents are tagged for easy filtering
5. **Combine searches**: Use `|` to search for multiple terms

---

## 🆘 Can't Find What You Need?

1. Check the [Topic Index](index/README.md)
2. Browse the [README](README.md) for an overview
3. Look at the [Repository Structure](README.md#-repository-structure)
4. Search by tag or use case (examples above)

---

**Last updated**: 2026-01-25
