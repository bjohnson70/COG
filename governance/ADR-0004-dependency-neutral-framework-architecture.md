---
document_id: ADR-0004
title: "Dependency-Neutral Framework Architecture"
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-11-20
---

# ADR-0004: Dependency-Neutral Framework Architecture

## ADR Decision Status

Accepted

## Decision Date

2026-11-20

## Context

COG defines reusable governance, lifecycle, documentation, presentation,
locality, and validation concepts. Those concepts must remain usable when a
user supplies a Markdown bootstrap to a compatible AI assistant in an
environment that does not provide a programming runtime, package manager,
IDE, repository host, operating-system-specific capability, or particular AI
provider.

Existing COG governance establishes relevant boundaries:

- [COG-STD-005](../standards/INFORMATION_PRESENTATION_STANDARD.md) defines
  reusable presentation semantics and technology-neutral conformance outcomes.
- [ADR-0002](ADR-0002-information-lifecycle-architecture.md) preserves
  Evidence Chain, Effective Information, Decision Chain, provenance, Local
  Context, and public/private boundaries.
- [ADR-0003](ADR-0003-shared-information-presentation-architecture.md)
  defines shared presentation architecture while leaving project-specific
  information and implementation authority in projects.
- [COG-GDE-001](../guides/PRESENTATION_DESIGN_GUIDE.md) provides advisory
  presentation guidance.

COG-STD-005 and ADR-0003 identify universal NEW/CONTINUE bootstrap,
GitHub-optional onboarding, and common presentation automation as deferred
workstreams. This ADR establishes the dependency-neutral architectural
direction and must not be treated as public-bootstrap implementation.

## Decision

COG adopts a dependency-neutral framework architecture.

### Core Requirements

COG Core MUST:

1. Be expressed in Markdown and portable structured data.
2. Use Markdown as the canonical and universal bootstrap entry point.
3. Avoid a mandatory programming language, runtime, package manager, IDE,
   operating system, repository service, or AI provider.
4. Support NEW and CONTINUE behavior.
5. Discover available capabilities and disclose unavailable functionality
   explicitly.
6. Preserve provenance, Local Context, public/private boundaries, and
   temporal and information-state distinctions.
7. Keep project-specific metrics, calendars, deadlines, thresholds,
   operational evidence, and release authority in project authority.
8. Separate Core adoption from optional executable implementations.

Equivalent accessible delivery mechanisms MAY supplement Markdown. They MUST
NOT replace the Markdown source or establish separate bootstrap authority.

### Markdown Bootstrap

The canonical bootstrap artifact SHALL be Markdown. It SHALL identify:

- Applicable COG controlled documents.
- The intended governed scope.
- NEW or CONTINUE behavior.
- Available capabilities.
- Unavailable or unverified capabilities.
- Public/private and Local Context boundaries.
- Owner-authorized scope, prior decisions, and unresolved matters.
- Optional technologies and their limitations.

NEW behavior establishes a new governed work scope. CONTINUE behavior resumes
an existing authorized context without silently recreating prior decisions,
approvals, evidence, or unresolved matters.

GitHub-optional onboarding SHALL remain separate from public-bootstrap
implementation. Repository access and Git operations are optional conveniences,
not Core prerequisites.

### Capability Discovery

Before environment-dependent work, an implementation SHOULD discover whether
it can read or write Markdown, access a filesystem or repository, execute
code, convert timezone or calendar data, render output, run deterministic
tests, access Git or a repository service, or perform manual review.

Unavailable capability SHALL be reported as INCOMPLETE or materially limited.
AI-generated interpretation SHALL NOT be represented as code execution,
rendering, repository verification, or deterministic test evidence.

Semantic analysis, manual inspection, deterministic execution,
provider-assisted processing, and repository verification are distinct
evidence categories.

### Optional Technologies

Python, Node.js, GitHub, APIs, package managers, IDEs, timezone libraries,
renderers, browser automation, test frameworks, and other technologies MAY
be used as optional extensions.

An optional extension SHALL disclose its runtime, dependencies, platform or
provider limitations, fallback behavior, and generated-output location.
An optional extension SHALL NOT become a Core prerequisite or impose its
metrics, schemas, calendar rules, or implementation choices on adopters.

### Reporting Semantics

Dependency neutrality does not alter COG reporting requirements.

Reporting SHALL preserve purpose, audience, scope, source context,
generation context, material limitations, reporting and presentation
timezone roles, applicable UTC-comparable instants, original source
representations, and source, effective, cutoff, refresh, generation,
publication, and authorization times where material.

It SHALL distinguish availability from freshness and SHALL preserve zero,
missing, unavailable, stale, partial, unverified, uncertain, and unresolved
states. Project-specific metrics, denominators, thresholds, calendars,
deadlines, and status definitions remain project authority.

For the synthetic executive-report example, the following example-specific
requirements remain separate from COG-wide metric definitions:

- October 2026 reporting period.
- `America/Los_Angeles` reporting timezone.
- Independently configurable presentation timezone.
- UTC-comparable machine-readable absolute instants.
- Project-defined local date-only deadline boundaries.
- Preserved source timestamp and conversion provenance.
- 18 confirmed open items plus 1 separate unverified item.
- 4 confirmed overdue items plus 1 separate unknown-deadline item.
- 6 of 8 eligible milestones at 75 percent.
- 4 of 5 expected sources at 80 percent.
- Browser, Outlook, and US Letter/portrait print presentation.
- Manual PDF printing without automated PDF generation.

These F3 requirements remain under the separately authorized
COG-DES-001/F3 implementation gate and do not become universal COG metrics.

### Public and Private Boundaries

COG Core SHALL remain usable without private project data.

Credentials, identities, private evidence, confidential incidents,
protected personal data, operational evidence, network identifiers,
inventories, and proprietary sources SHALL remain in their authorized Local
Context and SHALL NOT be copied into public COG Core.

Public-bootstrap implementation and F3 report-example implementation are
separate workstreams. Publication of one does not authorize implementation or
publication of the other.

## Alternatives Considered

### Mandatory Repository or GitHub Bootstrap

Rejected. Repository hosting would make COG Core unavailable to users who lack
GitHub or repository access.

### Mandatory Executable Runtime

Rejected. Deterministic implementation can improve repeatability but cannot
establish or enforce Core adoption for every environment.

### Mandatory AI Provider or Platform

Rejected. Provider-specific capabilities would create vendor coupling and
platform-dependent Core assumptions.

### Markdown-First Core with Optional Extensions

Accepted. Markdown provides the canonical portable source, portable structured
data may supplement it, and executable implementations remain optional.

## Consequences

### Benefits

- Lower adoption burden.
- Cross-platform and AI-provider-independent Core entry.
- Clear separation of Core from implementation.
- Explicit evidence and limitation disclosure.
- Reusable cross-medium presentation semantics.
- Preservation of public/private and Local Context boundaries.

### Tradeoffs

- AI interpretation and manual validation may vary.
- Deterministic repeatability is environment-dependent.
- Browser, email, print, and PDF equivalence may require manual inspection.
- Capability discovery cannot guarantee provider behavior.

## Relationship to Existing Governance

- COG-STD-005 remains the presentation requirements authority.
- COG-GDE-001 remains advisory.
- COG-STD-006 establishes normative Core portability conformance.
- ADR-0002 remains authoritative for lifecycle, provenance, and Local Context.
- ADR-0003 remains authoritative for shared presentation architecture.
- COG-DEV-002 governs repository operations but does not make repository access
  a Core prerequisite.

## Adoption and Transition

Adopting projects SHOULD:

1. Provide a Markdown bootstrap entry.
2. Declare applicable COG documents and project authority.
3. Discover and disclose available capabilities.
4. Preserve public/private and Local Context boundaries.
5. Apply COG-STD-005 reporting semantics.
6. Add optional extensions only under project authority.
7. Use PASS, FAIL, and INCOMPLETE evidence classifications.
8. Document material exceptions.

Existing repositories need not adopt executable tooling merely to adopt Core.

## D01-D10 Relationship

This decision implements the owner-approved prospective D01-D10 architecture:

- D01 establishes dependency-neutral, AI-provider-agnostic COG Core.
- D02 establishes Markdown bootstrap and portable structured data.
- D03 establishes capability discovery and limitation disclosure.
- D04 makes Python, GitHub, APIs, and similar technologies optional.
- D05 establishes COG-STD-006 as the portability standard.
- D06 records this architecture in ADR-0004.
- D07 preserves existing F3 reporting semantics as example-specific semantics.
- D08 retains temporary Python artifacts while deferring replacement of the
  executable Core manifest.
- D09 requires evidence-qualified PASS, FAIL, and INCOMPLETE outcomes.
- D10 separates public-bootstrap implementation from F3 report implementation.

## References

- [COG-STD-005](../standards/INFORMATION_PRESENTATION_STANDARD.md)
- [COG-STD-006](../standards/CORE_PORTABILITY_STANDARD.md)
- [COG-GDE-001](../guides/PRESENTATION_DESIGN_GUIDE.md)
- [ADR-0002](ADR-0002-information-lifecycle-architecture.md)
- [ADR-0003](ADR-0003-shared-information-presentation-architecture.md)
- [COG-DEV-002](../development/GITHUB_WORKFLOW.md)

## Status

Active COG architecture decision. Its normative implementation details are
defined in COG-STD-006.
