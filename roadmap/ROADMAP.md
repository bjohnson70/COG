---
document_id: COG-ROAD-001
title: COG Roadmap
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-09-09
applies_to:
       - COG
depends_on:
       - standards/DOCUMENTATION_STANDARD.md
       - governance/SHARED_VS_PROJECT_SPECIFIC.md
---

# COG Roadmap

## Purpose

The COG Roadmap describes current planning direction for the evolution and
adoption of the Common Operations Guide.

It identifies established baseline capability, near-term adoption and
validation priorities, areas to evaluate as evidence emerges, and areas
intentionally deferred.

The roadmap does not itself create operating requirements. A future capability
listed here does not become authoritative merely because it appears on the
roadmap.

## Roadmap Principles

- Define reusable governance once and reference it where applicable.
- Existing projects are evidence for COG practices, not automatic templates.
- Repetition alone does not create a COG standard.
- Project-specific requirements remain authoritative within their projects.
- COG should not become a collection of unrelated or speculative standards.
- New COG capabilities should respond to demonstrated reusable need.
- Avoid cosmetic migrations or structural consistency for its own sake.
- Preserve useful institutional knowledge when consolidating or retiring
       guidance.

The [Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
document is authoritative for detailed placement and promotion judgment.

## Initial Baseline - Established

The initial COG baseline now includes:

- [Documentation Standard](../standards/DOCUMENTATION_STANDARD.md)
- [Repository Standard](../standards/REPOSITORY_STANDARD.md)
- [Naming Standard](../standards/NAMING_STANDARD.md)
- [Decision Record Standard](../standards/DECISION_RECORD_STANDARD.md)
- [Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
- [ADR-0001 COG Operating Model](../governance/ADR-0001-cog-operating-model.md)
- [GitHub Development Workflow](../development/GITHUB_WORKFLOW.md)
- [Document Catalog](../DOCUMENT_CATALOG.md)

Reusable starting points also include the [ADR Template](../templates/ADR_TEMPLATE.md)
and [Project README Template](../templates/PROJECT_README_TEMPLATE.md). Templates
are not automatically controlled documents.

The [Document Catalog](../DOCUMENT_CATALOG.md) is the authoritative inventory
of controlled COG documents. This section summarizes the baseline and does not
reproduce each document's detailed requirements.

## Adoption and Validation - Next

The next COG maturity step is to apply the established baseline to actual
projects and use the results as evidence.

Initial adoption work may include EIB, POG, VOG, and future projects. Adoption
should evaluate:

- Which Active COG standards apply.
- Where project-specific authority remains appropriate.
- Justified exceptions or non-applicability where useful or required.
- Usability of standards and templates.
- Metadata, references, links, catalogs, and dependencies.
- Recurring gaps or friction.
- Opportunities for simplification.
- Repeated needs that may justify future COG capabilities.

Adoption does not require identical repository structures or cosmetic
migration. EIB, POG, and VOG are evidence and adoption targets, not templates
future projects must copy. Adoption experience should refine COG before
additional standards are created.

## Evidence-Driven Expansion - Future

Future capabilities should be considered only when repeated cross-project
evidence demonstrates a reusable need.

Candidate evaluation should ask:

- Is the need reusable across projects?
- Is COG the correct authority?
- Is the capability already adequately governed by an Active COG document?
- Would a new artifact reduce duplication or merely add another layer?
- Is a standard needed, or would guidance, a template, or automation be more
       appropriate?
- Can the need remain project-specific without loss of reusable value?

The [Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
document remains authoritative for detailed promotion and adoption rules.

## Candidate Capability Disposition

| Capability | Disposition | Planning direction |
| --- | --- | --- |
| Tool and device flexibility | ESTABLISHED | Covered by the [GitHub Development Workflow](../development/GITHUB_WORKFLOW.md); no standalone device workflow is planned unless distinct reusable requirements emerge. |
| AI-assisted repository execution | ESTABLISHED | Limited repository-development execution guidance exists in the [GitHub Development Workflow](../development/GITHUB_WORKFLOW.md). |
| Broader AI governance | DEFER UNTIL DEMONSTRATED NEED | Do not imply that a future AI standard is guaranteed. |
| Security guidance or a Security Standard | DEFER UNTIL DEMONSTRATED NEED | Project-specific security remains project authority unless a reusable COG-level need is demonstrated. |
| Validation | ESTABLISHED AT PRINCIPLE LEVEL | Proportional validation is governed by the GitHub Development Workflow and related Active standards. |
| Validation automation | EVALUATE THROUGH ADOPTION | Evaluate lightweight automation after repeated validation patterns emerge; do not promise an Automation Standard. |
| Project initialization | EVALUATE THROUGH ADOPTION | Determine whether repeated startup needs justify guidance, a template, lightweight automation, or no additional artifact. |
| Release management | DEFER UNTIL DEMONSTRATED NEED | Commit and push are separate, but COG does not need a universal release model now. |
| Standalone maintenance standard | DEFER / ABSORBED INTO EXISTING GUIDANCE | Current Documentation, Repository, and GitHub Workflow documents cover the initial baseline. Reconsider only if adoption reveals recurring gaps. |
| Compliance guidance | DEFER UNTIL DEMONSTRATED NEED | No reusable cross-project compliance need has been established. |
| Changelog or history artifact | DEFER | Git history, metadata, catalog entries, and ADRs provide existing traceability. |
| Additional templates | EVALUATE THROUGH ADOPTION | Add only when repeated authoring needs demonstrate reusable value. |
| Universal repository-layout standard | DO NOT PLAN | Repository Standard governs outcomes rather than identical physical structures. |

No candidate capability in this table is an approved standard, mandatory
project requirement, or guaranteed deliverable.

## Maintenance and Evolution - Ongoing

COG should evolve when:

- Adoption evidence reveals recurring gaps.
- Governing assumptions materially change.
- Dependencies change.
- Authoritative documents become obsolete or duplicative.
- A reusable capability demonstrates sufficient value for COG ownership.

Maintenance should favor one authoritative source per governed concept,
deliberate consolidation, preservation of useful institutional knowledge,
retirement and supersession according to the [Documentation Standard](../standards/DOCUMENTATION_STANDARD.md),
proportional validation, and avoidance of unnecessary bureaucracy.

This roadmap does not create a separate maintenance standard.

## Relationship to COG Governance

- [Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
       governs whether future concepts belong in COG.
- [ADR-0001](../governance/ADR-0001-cog-operating-model.md) preserves why COG
       uses the reusable-governance and project-authority operating model.
- [Documentation Standard](../standards/DOCUMENTATION_STANDARD.md) governs
       roadmap lifecycle and controlled-document treatment.
- [Repository Standard](../standards/REPOSITORY_STANDARD.md) and [GitHub
       Development Workflow](../development/GITHUB_WORKFLOW.md) govern their
       respective operating domains.
- [Document Catalog](../DOCUMENT_CATALOG.md) is the authoritative controlled-
       document inventory.

These documents remain authoritative for their stated boundaries. This
roadmap provides planning direction and does not duplicate their detailed
requirements.