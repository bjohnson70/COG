---
title: COG Shared vs Project-Specific Governance
document_id: COG-GOV-001
version: 1.0
status: Active
owner: COG Project
last_updated: 2026-09-09
applies_to:
  - COG
  - Projects adopting COG
---

# COG Shared vs Project-Specific Governance

## Purpose

This document governs whether a rule, standard, template, workflow, practice,
or other durable concept should be governed centrally by COG or remain under
project-specific authority.

The goal is to make genuinely reusable practices easier to adopt and reference
without centralizing concepts that are better governed by an individual
project.

## Core Principles

- Existing projects are evidence for COG standards, not automatic standards.
- Define reusable governance once and reference it everywhere.
- One governed concept should have one authoritative source.
- COG governs reusable cross-project outcomes and practices.
- Projects govern their domain-specific requirements and implementations.
- Project-specific does not mean less governed, less authoritative, or less
  important. It means the individual project is the appropriate authority.
- COG adoption must not force inappropriate structural or cosmetic changes.

## Determining Where a Concept Belongs

A concept is a strong COG candidate when most of the following are true:

- It is reusable across multiple projects or project types.
- It expresses a common outcome, governance rule, engineering practice, or
  reusable operating practice.
- It is not inherently tied to one project's domain, data model, workflow,
  audience, or operating context.
- Centralizing it reduces duplication or inconsistent interpretation.
- It is stable enough to govern reuse.
- Projects can adopt it without inappropriate structural or cosmetic changes.
- It retains value independently of the project where it was first observed.

These are judgment criteria, not a numeric scoring system. They do not require
every condition, and there is no minimum number of projects required before a
concept can be considered for COG.

## Evidence Is Not Authority

Patterns observed in EIB, POG, VOG, or other projects may provide evidence
that reusable COG guidance would be valuable. Repetition alone does not create
a COG standard.

Before promoting a project-derived practice into COG, determine:

- Whether the concept has value beyond the originating project.
- Which portion is genuinely reusable.
- Which portion is project-specific implementation.
- Whether an existing COG authoritative source already governs the concept.
- Whether centralizing it improves consistency without creating unnecessary
  coupling.

Project conventions remain evidence for evaluation. They are not templates
that future projects must copy.

## Material That Normally Remains Project-Specific

The following are illustrative examples of material that normally remains
project-specific:

- Domain-specific architecture
- Business rules
- Project-specific workflows
- Project-specific data models
- Project-specific operational procedures
- Project-specific requirements
- Project-specific security or privacy details
- Project-specific inventories or registers
- Project-specific status models
- Project-specific implementation choices

Project-specific material remains authoritative within its project. It may be
more detailed or restrictive than COG when the project's domain, risk,
architecture, operations, or obligations justify it. COG should not absorb
project-specific detail merely because that detail is important.

## Material That May Be Appropriate for COG

The following are illustrative examples of material that may be appropriate
for COG:

- Reusable governance principles
- Documentation standards
- Naming conventions
- Decision-record practices
- Reusable templates
- Repository engineering practices
- Cross-project operating practices
- Reusable validation patterns

Inclusion in this list does not automatically establish a COG standard. The
placement decision still requires the judgment described above.

## Promotion: Project to COG

Promotion should remain lightweight:

1. Observe a reusable pattern, recurring problem, or cross-project need.
2. Determine whether it has value beyond the originating project.
3. Separate the reusable outcome or governance from project-specific
   implementation.
4. Check whether an existing COG authoritative source already governs it.
5. Create or refine one COG authoritative source only when justified.
6. Let projects evaluate and adopt the reusable result as appropriate.

This process does not require approval boards, fixed project-count thresholds,
mandatory committees, or an ADR for every promotion.

## Adoption: COG to Project

Projects should:

1. Evaluate whether the COG requirement or guidance applies.
2. Adopt applicable concepts using project-appropriate structures.
3. Document non-applicability or justified exceptions when useful or required.
4. Update material references when practical.
5. Migrate implementation when operationally justified.

COG changes do not automatically require immediate project migration. Projects
are not required to reorganize merely to achieve cosmetic consistency with
COG. A project's implementation may differ while still satisfying the
reusable COG outcome.

## Exceptions and Non-Applicability

A project may:

- Adopt applicable COG requirements.
- Determine that a COG requirement is not applicable.
- Document a justified exception.
- Implement the reusable outcome through project-specific structures.
- Establish stricter project-specific requirements when appropriate.

This document does not create a universal exception-record format. An
exception does not automatically require an ADR. The [Decision Record
Standard](../standards/DECISION_RECORD_STANDARD.md) determines when an
exception is consequential enough to warrant an ADR.

## Authority and Duplication

- One authoritative source should govern each governed concept.
- Reusable cross-project governance belongs in COG when justified.
- Project-specific implementation remains under project authority.
- Project READMEs and local documentation may reference applicable COG
  standards.
- Projects should reference COG rather than wholesale-copying COG governance
  when practical.
- COG may reference project evidence without becoming a duplicate repository
  of project-specific material.

This document governs placement and authority boundaries. It does not
duplicate detailed catalog, lifecycle, naming, repository-layout, or ADR
requirements.

## Relationship to Other COG Documents

The boundaries with related Active COG documents are:

- [DOCUMENTATION_STANDARD.md](../standards/DOCUMENTATION_STANDARD.md) governs
  controlled-document identity, metadata, lifecycle, catalogs, references,
  supersession, and retirement.
- [REPOSITORY_STANDARD.md](../standards/REPOSITORY_STANDARD.md) governs
  repository organization outcomes, discoverability, hygiene, and repository
  implementation boundaries.
- [NAMING_STANDARD.md](../standards/NAMING_STANDARD.md) governs naming
  conventions.
- [DECISION_RECORD_STANDARD.md](../standards/DECISION_RECORD_STANDARD.md)
  governs when consequential decisions require ADRs and ADR governance.

These documents remain authoritative for their stated boundaries. This
document should reference them rather than reproduce their detailed
requirements.