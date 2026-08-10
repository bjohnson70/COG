---
title: Common Operations Guide
document_id: COG-ROOT-001
version: 1.0
status: Active
owner: BSJ
last_updated: 2026-08-09
---

# Common Operations Guide (COG)

> Define once. Reference everywhere. Override only when a project has a legitimate project-specific requirement.

---

# Purpose

The **Common Operations Guide (COG)** is the shared operational, development, documentation, and governance framework used across BSJ projects.

COG exists to prevent each project from maintaining separate copies of the same basic standards, workflows, and development instructions.

Instead of repeatedly defining common practices inside:

- EIB
- POG
- VOG
- Future repositories

those practices should be defined once in COG and referenced by the applicable project repositories.

---

# Why COG Exists

As additional projects are created, many recurring needs appear repeatedly.

Examples include:

- GitHub development workflow
- Device-aware working methods
- Repository standards
- File naming
- Markdown conventions
- Documentation metadata
- Commit-message patterns
- ADR usage
- Public versus private repository practices
- Idea capture
- Cross-device development
- AI-assisted development workflow

Duplicating those rules creates several problems:

```text
Duplicate documents
        ↓
Standards drift
        ↓
Conflicting instructions
        ↓
More maintenance
        ↓
More opportunity for mistakes