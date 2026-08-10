---
title: GitHub Development Workflow
document_id: COG-DEV-002
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
depends_on:
  - standards/REPOSITORY_STANDARD.md
  - development/DEVICE_AWARE_WORKFLOW.md
  - governance/SHARED_VS_PROJECT_SPECIFIC.md
---

# GitHub Development Workflow

## Purpose

This document defines the common GitHub development workflow used across BSJ repositories.

The goal is to make repository work:

- Consistent
- Easy to understand
- Recoverable
- Device-aware
- Low-friction
- Verifiable
- Safe for future contributors
- Reusable across projects

The workflow applies to COG and to project repositories that adopt COG standards.

---

# Guiding Principle

> **Inspect first. Change deliberately. Commit clearly. Verify before declaring completion.**

Repository work should leave the project easier to understand than before the change.

---

# Scope

This is a shared COG development standard.

It governs common GitHub practices such as:

- Repository inspection
- File reads
- File creation
- File updates
- File moves
- Commit behavior
- Branch usage
- Verification
- Manual tablet workflow
- Direct PC workflow
- Change sequencing
- Recovery from mistakes

Project-specific engineering requirements may supplement this standard.

---

# Repository Context Comes First

Before making a change, identify:

```text
Repository
    +
Current branch
    +
Current device
    +
Available permissions
    +
Applicable COG standards
    +
Applicable project standards