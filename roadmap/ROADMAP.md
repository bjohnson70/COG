# COG Roadmap

## 1. Purpose

This roadmap defines the planned development direction for the
Common Operation Guide (COG).

COG exists to capture reusable engineering, development, governance, and
operational practices that can be applied across multiple projects.

The roadmap helps ensure that COG develops intentionally rather than becoming
a collection of unrelated standards.

---

## 2. Vision

COG should become a reusable foundation for creating and maintaining projects.

A new project should not need to rediscover basic practices for:

- Repository organization
- Naming
- Documentation
- Git and GitHub workflows
- Decision records
- Device-aware development
- Project governance
- Templates
- Security practices
- Project initialization
- Ongoing maintenance

COG should provide sensible defaults while allowing projects to retain
legitimate domain-specific requirements.

---

## 3. Core Principle

COG is not intended to contain every lesson from every project.

The knowledge flow should be:

```text
Project Experience
       |
       v
Lesson Learned
       |
       v
Evaluate Reusability
       |
   +---+---+
   |       |
  No      Yes
   |       |
   v       v
Project   Candidate
Specific  COG Practice
             |
             v
       Evaluate / Refine
             |
             v
         COG Standard