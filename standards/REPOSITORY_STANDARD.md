---
title: COG Repository Standard
document_id: COG-STD-001
version: 1.0
status: Active
owner: COG Project
last_updated: 2026-09-05
applies_to:
  - COG
  - EIB
  - POG
  - VOG
  - Future BSJ repositories
---

# COG Repository Standard

## 1. Purpose

This standard defines reusable repository-level organization and governance
outcomes for projects that adopt the Common Operations Guide (COG).

It exists to make repositories discoverable, maintainable, traceable, and safe
to change without requiring identical physical layouts. The standard is
intentionally repository-agnostic: projects remain responsible for their own
architecture, requirements, workflows, and domain-specific documentation.

## 2. Governing Principles

- Define once. Reference everywhere.
- One governed concept MUST have one canonical authoritative source.
- Existing projects are evidence for COG standards, not automatic templates.
- Required concepts and outcomes should be standardized before identical
  physical layouts are prescribed.
- Project-specific requirements remain within the project.
- Repository organization SHOULD improve discoverability, maintainability,
  traceability, and safe change.
- Repository changes SHOULD avoid unnecessary restructuring and duplicate
  authoritative documentation.

## 3. Repository Entry Point

Each adopting repository MUST provide a clear human-oriented entry point,
normally `README.md` or an equivalent document.

The entry point SHOULD allow a new human contributor or coding agent to
determine:

- What the repository is
- Why it exists
- Where authoritative documentation is located
- How to find important project guidance
- Where to begin before making changes

The entry point does not need to be a controlled document. Its role is human
navigation; controlled-document identity, authority, lifecycle, and metadata are
governed by the [COG Documentation Standard](DOCUMENTATION_STANDARD.md).

## 4. Discoverability and Authoritative Documentation

Repositories SHOULD make authoritative project information discoverable from
the entry point or other clearly identified governing documentation.

Repositories using controlled documents SHOULD follow the
[COG Documentation Standard](DOCUMENTATION_STANDARD.md), or document an
explicit project alternative or exception.

Where an authoritative catalog is warranted under the Documentation Standard,
the repository SHOULD make that catalog readily discoverable from its entry
point or governing documentation. This standard does not require a catalog for
every repository.

## 5. Repository Organization

Repositories SHOULD organize files so that:

- Authoritative material is discoverable.
- Unrelated concerns are reasonably separated.
- Generated, temporary, or local-only artifacts are distinguishable from
  authoritative source material.
- Contributors can identify where a new artifact belongs.
- Obsolete structures do not compete indefinitely with canonical structures.

This standard defines organization outcomes, not one universal directory tree.
It does not mandate identical directory names across projects, and existing
projects MUST NOT be required to migrate solely for cosmetic consistency with
COG. COG MAY define a default layout for new COG repositories elsewhere in the
future without making that layout universally mandatory here.

## 6. Reusable and Project-Specific Concerns

Reusable cross-project practices belong in COG when they meet COG governance
criteria. Domain-specific requirements, architecture, business rules,
operational details, and project-specific implementation choices remain within
the adopting project.

Projects SHOULD separate reusable guidance from project-specific guidance so
that COG remains a reusable standards layer rather than a repository for every
convention observed in one project.

The [Shared Versus Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
standard governs how that distinction is evaluated.

## 7. Canonical Sources and Duplication

At the repository level, one governed concept MUST have one canonical
authoritative source. Repository organization MUST NOT create competing
canonical locations for the same governed concept.

Duplicate authoritative material SHOULD be consolidated, superseded, or
retired deliberately. Transitional legacy paths MAY temporarily coexist with
canonical paths when migration requires them, but authority MUST remain
unambiguous throughout the transition.

The [COG Documentation Standard](DOCUMENTATION_STANDARD.md) governs detailed
documentation authority, lifecycle, metadata, supersession, and retirement
rules. This standard does not duplicate those requirements.

## 8. Stable References

Repositories SHOULD favor references that remain understandable and
maintainable as the repository evolves. Internal documentation links SHOULD be
repository-relative where practical, consistent with the Documentation
Standard.

Controlled-document identity SHOULD remain stable through reasonable file moves
or renames. A controlled document's identity MUST NOT depend solely on its file
location.

The [COG Naming Standard](NAMING_STANDARD.md) governs naming conventions, and
the Documentation Standard governs detailed Document ID rules. This standard
does not duplicate either set of requirements.

## 9. Repository Hygiene

Repositories SHOULD avoid committing:

- Temporary editor files
- Local machine artifacts
- Generated files that are not intended repository artifacts
- Credentials or secrets
- Unnecessary duplicate files
- Obsolete artifacts that could be mistaken for current authority

Project-specific ignore rules and security requirements remain project
responsibilities unless another COG standard governs them. This section does
not establish a security standard.

## 10. Change Discipline

Before declaring repository work complete, contributors and coding agents
SHOULD:

1. Inspect the relevant existing repository state.
2. Make the smallest coherent logical change.
3. Review the resulting diff.
4. Verify affected references or dependencies where practical.
5. Verify that no unintended files changed.
6. Run applicable project checks.
7. Commit related changes together when they form one logical unit.

These are repository-level outcomes, not a prescribed command sequence. The
[GitHub Development Workflow](../development/GITHUB_WORKFLOW.md) contains
detailed shared development workflow guidance.

## 11. Adoption and Exceptions

Projects MAY adopt this standard without copying COG's directory structure.
Projects MAY:

- Implement the required outcomes using their existing repository structure.
- Declare requirements not applicable.
- Document justified exceptions.
- Establish stricter project-specific requirements.

Exceptions SHOULD identify the reason and the responsible project authority
when appropriate. COG adoption should be evaluated primarily by governed
outcomes, not cosmetic layout conformity.

## 12. Relationship to Other COG Documents

The boundaries with related COG documents are:

- [DOCUMENTATION_STANDARD.md](DOCUMENTATION_STANDARD.md) governs controlled
  document identity, authority, lifecycle, metadata, catalogs, references,
  review, supersession, and retirement.
- [NAMING_STANDARD.md](NAMING_STANDARD.md) governs repository, directory,
  file, branch, and related naming conventions.
- [DECISION_RECORD_STANDARD.md](DECISION_RECORD_STANDARD.md) governs ADRs and
  decision-record practices.
- [SHARED_VS_PROJECT_SPECIFIC.md](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
  governs whether a practice belongs in COG or within a project.
- [GITHUB_WORKFLOW.md](../development/GITHUB_WORKFLOW.md) governs detailed
  shared GitHub development workflow practices.

This standard governs repository-level organization and governance outcomes.
It does not become the detailed authority for documentation lifecycle and
metadata, filename syntax, ADR processes, Git command sequences,
AI-assisted development, device-specific workflows, security requirements, or
release management.