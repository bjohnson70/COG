# COG Decision Record Standard

## 1. Purpose

This document establishes the Common Operation Guide (COG) standard for
recording significant architectural, engineering, governance, and operational
decisions.

The purpose of a decision record is to preserve:

- What was decided
- Why the decision was necessary
- What alternatives were considered
- What constraints influenced the decision
- What consequences resulted from the decision

A good decision record allows a future contributor to understand why the
current system exists without reconstructing the original conversation.

---

## 2. Core Principle

Important decisions should not exist only in:

- Chat conversations
- Email
- Meeting notes
- Personal memory
- Commit history
- Issue discussions

Those sources may provide useful evidence, but the resulting decision should
be captured in the repository when it materially affects the project.

The repository should preserve the decision, not require future maintainers
to rediscover it.

---

## 3. When a Decision Record Is Appropriate

Create a formal decision record when a decision materially affects:

- Architecture
- Repository structure
- Development workflow
- Data models
- Security
- Privacy
- Governance
- Naming conventions
- Public versus private information
- Technology selection
- Integration patterns
- Long-term maintenance
- Cross-project compatibility

A decision record is especially useful when reasonable alternatives existed.

---

## 4. When a Decision Record Is Not Required

Not every decision requires a formal record.

Routine implementation choices generally do not require one.

Examples include:

- Minor wording changes
- Typographical corrections
- Routine file additions
- Formatting changes
- Small refactoring with no architectural consequence
- Temporary troubleshooting steps
- Decisions already governed by an established standard

Avoid creating decision records merely to document activity.

The purpose is to preserve meaningful decisions.

---

## 5. Decision Record Types

COG recognizes two general categories of decisions.

### 5.1 Project-Specific Decisions

These decisions apply to one repository or project.

They should remain within that project.

Examples:

- A project's domain model
- A project-specific API
- A specialized data structure
- A project-specific security requirement

### 5.2 Reusable Decisions

These decisions may apply across multiple projects.

They should be evaluated for inclusion in COG.

Examples:

- Repository organization
- Naming conventions
- Git workflow
- Documentation practices
- Device-aware development practices

A reusable decision discovered in another project is evidence for COG.

It does not automatically become a COG standard.

---

## 6. Decision Record Location

Projects should maintain formal decision records in a clearly identified
directory.

Recommended location:

```text
adr/