# Common Operations Guide (COG)

> Define once. Reference everywhere.

## Purpose

The Common Operations Guide (COG) is the reusable cross-project standards and governance layer for BSJ projects. It provides a concise home for practices that are genuinely shared across projects, so each project does not need to define or maintain duplicate guidance.

## What COG Is

COG defines reusable concepts, practices, and outcomes for project operations, development, documentation, repository organization, and governance. It is authoritative for the common practices it explicitly establishes.

Existing projects such as EIB, POG, and VOG provide evidence and lessons for developing COG standards. Their conventions do not automatically become COG standards.

## What COG Is Not

COG is not a copy of each project's documentation, a project-specific requirements repository, or a mandate for identical physical repository layouts. It does not standardize practices merely because they exist in an existing project, and it should not introduce bureaucracy or premature standardization.

## Core Principles

- Define once. Reference everywhere.
- Standardize genuinely reusable cross-project practices.
- Standardize required concepts and outcomes before prescribing identical repository layouts.
- Keep project-specific requirements within the project.
- Allow projects to adopt applicable COG standards and document exceptions or non-applicability.
- Maintain one authoritative source for each governed concept.
- Use existing projects as evidence, not as automatic templates.
- Avoid unnecessary bureaucracy and premature standardization.

## Repository Organization

- [`development/`](development/) contains shared development workflow guidance, including [`GITHUB_WORKFLOW.md`](development/GITHUB_WORKFLOW.md).
- [`governance/`](governance/) contains governance guidance, including [`SHARED_VS_PROJECT_SPECIFIC.md`](governance/SHARED_VS_PROJECT_SPECIFIC.md).
- [`roadmap/`](roadmap/) records planned direction in [`ROADMAP.md`](roadmap/ROADMAP.md).
- [`standards/`](standards/) contains established reusable standards, including [repository](standards/REPOSITORY_STANDARD.md), [documentation](standards/DOCUMENTATION_STANDARD.md), and [naming](standards/NAMING_STANDARD.md) standards.
- [`templates/`](templates/) contains reusable document starting points, including the [ADR template](templates/ADR_TEMPLATE.md) and [project README template](templates/PROJECT_README_TEMPLATE.md).

## Using COG

1. Identify the COG standard or governance document relevant to the work.
2. Apply it when it is applicable to the project.
3. Keep project-specific requirements in the project repository.
4. Record justified exceptions or non-applicability in the project's authoritative documentation.
5. Link to COG rather than copying shared requirements into project documents.

Contributors and coding agents should inspect the applicable COG documents and the target project before making changes. The [GitHub Development Workflow](development/GITHUB_WORKFLOW.md) provides the current shared workflow guidance.

## Relationship to Projects

Projects may adopt applicable COG standards and may supplement them with project-specific requirements. A project remains responsible for its own architecture, product decisions, requirements, and other concerns that are not genuinely reusable across BSJ projects.

COG may evolve as projects provide evidence, but project history alone does not establish a COG standard. Changes to a shared practice belong in COG so that projects can reference one authoritative source.

## Current Status

COG is under active development. The initial minimum baseline is being established, and the current repository contains foundational workflow, governance, repository, documentation, and naming guidance.

Security, AI-assisted development, device-aware workflow, automation, and maintenance standards are potential future capabilities unless and until an authoritative COG document implements them.

## Navigation

- Start with the [repository standard](standards/REPOSITORY_STANDARD.md) for shared repository conventions.
- Read the [documentation standard](standards/DOCUMENTATION_STANDARD.md) for documentation guidance.
- Read the [naming standard](standards/NAMING_STANDARD.md) for naming conventions.
- Review [shared versus project-specific governance](governance/SHARED_VS_PROJECT_SPECIFIC.md) when deciding where a rule belongs.
- Follow the [GitHub development workflow](development/GITHUB_WORKFLOW.md) for repository work.
- Check the [roadmap](roadmap/ROADMAP.md) for planned COG work.
