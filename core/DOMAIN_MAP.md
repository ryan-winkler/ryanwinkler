# Domain Map

## What this map covers

This repository is a public product operating system, not a generic knowledge dump.

Keeping the bounded contexts clear helps in two ways:

- public claims stay tied to the right source of truth
- reusable frameworks stay separate from project-specific proof

## Bounded contexts

| Bounded context | Primary responsibility | System of record | Interfaces |
| --- | --- | --- | --- |
| Public Narrative | State who I am, what is current, and what evidence matters most | `README.md`, `START_HERE.md`, `NOW.md` | Pulls proof from Project Proof and Operating Frameworks |
| Operating Frameworks | Capture the models and principles I reuse across work | `core/`, `knowledge/` | Referenced by Delivery Systems and Project Proof |
| Delivery Systems | Turn principles into repeatable execution artifacts | `templates/`, `runbooks/`, `workflows/` | Consumes Operating Frameworks and feeds Insights |
| Project Proof | Show how the frameworks hold up inside real systems | `projects/` | Feeds Public Narrative and Insights |
| Insights and Learning | Capture patterns, signal, and updates that change how I work | `insights/`, `research/`, `tracker/`, `memory/` | Updates Operating Frameworks and Delivery Systems |

## What belongs where

- Put public positioning changes in **Public Narrative**
- Put reusable methods in **Operating Frameworks**
- Put templates, runbooks, and workflows in **Delivery Systems**
- Put Meitheal, Coolock Village Forge, and Moltis notes in **Project Proof**
- Put observations and recurring lessons in **Insights and Learning**

## Ownership rules

- **Public Narrative** can summarize a project, but it should not invent new proof
- **Project Proof** can explain a system, but it should not become a full framework library
- **Operating Frameworks** should stay portable and not depend on one project to make sense
- **Insights and Learning** should close the loop when new work changes how I operate

## Do not do this

- Mix public positioning copy into framework docs
- Turn project notes into inflated case studies
- Duplicate the same claim across multiple contexts without a clearer source of truth
- Let a deprecated system stay described as current
