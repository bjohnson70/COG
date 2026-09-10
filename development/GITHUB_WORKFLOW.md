---
title: GitHub Development Workflow
document_id: COG-DEV-002
version: 1.0
status: Active
owner: COG Project
last_updated: 2026-09-09
applies_to:
    - COG
    - Projects adopting COG
depends_on:
    - standards/REPOSITORY_STANDARD.md
    - standards/NAMING_STANDARD.md
    - standards/DOCUMENTATION_STANDARD.md
---

# GitHub Development Workflow

## Purpose

This document defines reusable Git and GitHub execution practices for COG and
projects adopting COG.

The workflow aims to make repository work:

- Consistent and understandable
- Recoverable and low-friction
- Verifiable
- Safe for future contributors
- Reusable across projects

It supports GitHub work without requiring one particular device, editor,
client, or command sequence.

## Guiding Principle

> Inspect first. Change deliberately. Commit clearly. Verify before declaring completion.

Repository work should leave the project easier to understand than before the
change.

## Scope

This workflow governs reusable execution practices for repository changes,
including as applicable:

- Repository inspection
- File creation and editing
- File moves and renames
- Branch execution
- Diff review
- Validation
- Staging, commits, and pushes
- AI-assisted repository editing
- Recovery and correction

It does not redefine repository structure, naming syntax, controlled-document
governance, ADR governance, COG-versus-project placement decisions, or
project-specific release and deployment procedures. Project requirements may
supplement this workflow.

## Repository Context Comes First

Before changing repository content, contributors SHOULD understand relevant
context, including as applicable:

- Current repository state and existing uncommitted or untracked work
- Current branch and local versus remote synchronization
- Available permissions
- Explicit task and file scope
- Applicable COG standards
- Applicable project-specific guidance
- Authoritative sources for governed content

Contributors SHOULD inspect enough context to make the intended change safely.
They SHOULD NOT begin by assuming repository state or authority.

## Git Change Lifecycle

Use this lightweight lifecycle proportionally to the change:

1. **Inspect:** Understand repository state, scope, and applicable authority.
2. **Edit:** Make the smallest coherent logical change and keep unrelated
     changes outside the intended scope.
3. **Review:** Inspect the actual resulting content and diff, not only an
     editing tool's summary.
4. **Validate:** Run checks appropriate to the affected content and risk.
5. **Stage:** Verify the staged file set before committing.
6. **Commit:** Commit one coherent logical unit after review and validation.
7. **Push:** Treat remote publication as a separate deliberate action.
8. **Verify:** Verify repository state after the operation being performed.

A push is not required when the task ends at a local commit. When a push
occurs, remote publication SHOULD be verified as appropriate.

## Branch Workflow

Branch policy should remain lightweight and project-appropriate.

- Direct work on the repository's primary branch MAY be appropriate when
    project policy, collaboration context, change size, and risk make it
    reasonable.
- A branch SHOULD be used when isolation, review, parallel work, risk, or
    project policy justifies it.
- Branch naming follows the [Naming Standard](../standards/NAMING_STANDARD.md).
- Contributors SHOULD synchronize with relevant remote state before beginning
    work when practical and material to the change.
- Integration, merge, and review follow applicable project policy.
- Short-lived branches SHOULD be cleaned up after integration when appropriate.

COG does not universally mandate GitFlow, trunk-based development, feature
branches for every change, pull requests for every change, direct work on the
primary branch, or any single branching model.

## Tool and Device Flexibility

Repository work may be performed through command-line Git, GitHub web
interfaces, desktop clients, editors or IDEs, mobile or tablet interfaces, or
other appropriate tools. The tool or device may change the mechanics but not
the required outcome.

Regardless of interface, contributors remain responsible for verifying:

- Repository state
- Intended file scope
- Actual content
- Resulting changes
- Applicable validation
- Commit and push state when those operations occur

This document does not prescribe detailed procedures for any particular tool,
device, editor, browser, or client.

## AI-Assisted Repository Work

AI-generated or AI-edited repository changes are proposals until reviewed.

- Actual repository content and diffs SHOULD be inspected.
- Automated validation does not replace human governance review where human
    judgment is required.
- AI-assisted tools SHOULD operate within explicit task and file scope.
- AI-assisted tools MUST NOT stage, commit, push, merge, or otherwise change
    repository or remote state unless specifically authorized for that action.
- The final repository state SHOULD be verified against the requested scope
    and applicable standards.

This section governs repository-development execution only. It does not create
general AI, security, privacy, procurement, or model policy.

## File Moves and Repository Migrations

For moves, renames, and migrations, contributors SHOULD as applicable:

- Confirm the source and intended destination.
- Preserve content and relevant history where practical.
- Update affected repository-relative references.
- Verify controlled-document identity remains correct.
- Verify affected dependencies.
- Inspect the diff for accidental deletion or duplication.
- Verify final file scope.
- Avoid cosmetic migration that provides no meaningful project outcome.

The [Documentation Standard](../standards/DOCUMENTATION_STANDARD.md),
[Repository Standard](../standards/REPOSITORY_STANDARD.md), and [Naming
Standard](../standards/NAMING_STANDARD.md) remain authoritative for their
respective boundaries.

## Validation

Validation SHOULD be proportional to the type and risk of the change. Examples
MAY include:

- Repository status
- Actual diff review
- `git diff --check`
- Staged-file verification
- Untracked-file checks where exact scope matters
- Repository-relative link and reference validation
- Dependency validation for controlled documents
- Tests, lint, build, or project-specific validation

Where governed or controlled documentation is affected, contributors SHOULD
verify applicable metadata, catalog entries, references, and dependencies
according to the [Documentation Standard](../standards/DOCUMENTATION_STANDARD.md).
Where a change implements or affects an accepted ADR, contributors SHOULD
verify consistency with that decision. This does not redefine the ADR
threshold or governance.

## Recovery and Correction

If verification identifies an unintended change, contributors SHOULD correct
it before declaring the work complete.

Contributors SHOULD avoid hiding unrelated or pre-existing changes merely to
produce a clean status and SHOULD NOT overwrite another contributor's work
simply to restore an expected state. When recovery could destroy work or
history, inspect repository state and choose the least destructive correction
appropriate to the situation.

This workflow does not prescribe reset, rebase, revert, or other destructive
Git commands universally.

## Commit and Push Discipline

Commit and push are separate actions. A successful local commit does not imply
immediate remote publication.

Reviewed local commits MAY be deliberately batched before a push when that
improves review or operational control. Batching is not mandatory.

Before committing, contributors SHOULD verify the staged scope and use a
commit message that clearly describes the logical change. After committing,
contributors SHOULD verify repository state. Push only when authorized and
appropriate to the project or task; do not perform it automatically when it is
not part of the requested work.

## Relationship to Other COG Documents

The boundaries with related COG documents are:

- [Repository Standard](../standards/REPOSITORY_STANDARD.md) governs
    repository organization outcomes, discoverability, hygiene, and high-level
    change discipline.
- [Naming Standard](../standards/NAMING_STANDARD.md) governs repository,
    directory, file, and branch naming conventions.
- [Documentation Standard](../standards/DOCUMENTATION_STANDARD.md) governs
    controlled-document identity, metadata, lifecycle, catalogs, references,
    dependencies, supersession, and retirement.
- [Decision Record Standard](../standards/DECISION_RECORD_STANDARD.md) governs
    ADR thresholds, status, identity, numbering, and minimum content.
- [Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
    governs COG-versus-project placement, promotion, adoption, and project
    authority boundaries.

These documents remain authoritative for their stated boundaries. This
workflow operationalizes repository execution without reproducing their
detailed requirements. ADR-0001 may provide background for the COG operating
model but is not a substantive workflow dependency.

## Normative Language

MUST, SHOULD, and MAY are used deliberately. MUST is limited to essential
safety and integrity boundaries, such as preventing an AI-assisted tool from
changing repository or remote state without explicit authorization. SHOULD is
used for normal reusable practices where project context may justify variation.
MAY is used for optional approaches.