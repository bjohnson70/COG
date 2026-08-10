# COG Documentation Standard

## 1. Purpose

This document establishes the Common Operation Guide (COG) standard for
creating, organizing, maintaining, and retiring repository documentation.

Documentation should make a project easier to understand and maintain.

It should not create unnecessary administrative overhead or become more
difficult to manage than the system it describes.

---

## 2. Core Principle

Repository documentation should answer four fundamental questions:

1. What is this?
2. Why does it exist?
3. How does it work?
4. Where do I find additional information?

Documentation should support understanding without requiring contributors to
reconstruct the project from:

- Chat conversations
- Email
- Personal memory
- Commit history
- Meeting notes
- Unstructured directories

Important project knowledge should eventually become durable repository
documentation.

---

## 3. Documentation Is Part of the System

Documentation is not separate from the project.

Changes to architecture, workflows, standards, or repository organization may
require corresponding documentation changes.

A technically correct implementation with materially incorrect documentation
is an incomplete change.

Documentation should therefore be considered during:

- Design
- Implementation
- Review
- Refactoring
- Release
- Repository reorganization

---

## 4. Documentation Categories

Documentation should be organized according to purpose.

Common categories include:

### Standards

Rules and conventions governing the project.

Examples:

```text
standards/NAMING_STANDARD.md
standards/REPOSITORY_STANDARD.md