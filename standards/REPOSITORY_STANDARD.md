---
title: Repository Standard
document_id: COG-STD-001
version: 1.0
status: Active
owner: BSJ
last_updated: 2026-08-09
applies_to:
  - COG
  - EIB
  - POG
  - VOG
  - Future BSJ repositories
---

# Repository Standard

## Purpose

This document defines the common repository structure, naming, and organization standards used across BSJ projects.

The objective is to establish one reusable engineering standard so that each new project does not independently reinvent basic repository conventions.

This standard is maintained by the **Common Operations Guide (COG)** and should be referenced by project repositories.

---

# Governing Principle

> **Define once. Reference everywhere. Override only when a project has a legitimate project-specific requirement.**

Repository conventions that apply substantially unchanged across multiple projects belong in COG.

Project repositories should contain the architecture, requirements, workflows, and documentation specific to that project.

---

# Existing Projects Are Evidence, Not Automatically the Standard

EIB, POG, VOG, and other existing projects provide valuable experience.

They do not automatically define the common standard.

When creating or refining a COG standard:

1. Review lessons learned from existing projects.
2. Identify what worked well.
3. Identify inconsistencies or unnecessary complexity.
4. Compare the practice with generally accepted engineering conventions.
5. Establish the preferred common standard in COG.
6. Gradually bring existing projects into alignment where beneficial.

This prevents historical decisions from becoming permanent merely because they occurred first.

---

# Repository Naming

Repository names should normally use the established project acronym.

Examples:

```text
COG
EIB
POG
VOG