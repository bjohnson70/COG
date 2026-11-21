---
document_id: COG-STD-006
title: COG Core Portability Standard
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-11-20
applies_to:
  - COG
  - Projects adopting COG
depends_on:
  - standards/DOCUMENTATION_STANDARD.md
  - standards/NAMING_STANDARD.md
  - standards/INFORMATION_PRESENTATION_STANDARD.md
  - governance/ADR-0002-information-lifecycle-architecture.md
  - governance/ADR-0003-shared-information-presentation-architecture.md
  - governance/ADR-0004-dependency-neutral-framework-architecture.md
---

# COG Core Portability Standard

## 1. Purpose and Scope

This standard defines minimum requirements for COG Core to remain usable
without a mandatory programming runtime, development tool, package manager,
operating system, repository service, IDE, or AI provider.

It establishes portable adoption, Markdown bootstrap behavior, capability
discovery, optional extensions, evidence-qualified validation, and public/private
boundaries. It does not prescribe a provider, language, renderer, schema,
filesystem, repository layout, or implementation framework.

## 2. Dependency-Neutral Core

COG Core SHALL be expressible through Markdown and portable structured data.

Core adoption SHALL NOT require:

- Python, Node.js, or another programming runtime.
- A package manager or installed dependency.
- An IDE or code editor.
- GitHub or another repository host.
- Git or command-line repository operations.
- A particular operating system or filesystem.
- A particular AI provider or provider-specific function.
- Browser automation or automated PDF generation.
- A fixed dashboard, export format, or renderer.

Markdown SHALL be the canonical and universal COG Core bootstrap source.
Portable structured data MAY supplement Markdown but SHALL NOT replace the
Markdown bootstrap or establish separate bootstrap authority.

## 3. Bootstrap Entry and NEW/CONTINUE

An adopting implementation SHALL provide a Markdown bootstrap entry or an
accessible delivery that derives from the canonical Markdown source.

Equivalent accessible delivery mechanisms MAY supplement Markdown, but SHALL
NOT replace the Markdown source or establish a separate bootstrap authority.

The bootstrap SHALL identify:

- COG scope and applicable controlled documents.
- User-authorized purpose and scope.
- NEW or CONTINUE behavior.
- Available capabilities.
- Unavailable or unverified capabilities.
- Project or Local Context authority.
- Public/private boundaries.
- Pending decisions and approvals.
- Optional technologies and dependencies.

NEW SHALL establish a new governed work scope.

CONTINUE SHALL resume an existing authorized context without silently
recreating prior decisions, approvals, evidence, or unresolved matters.

GitHub-optional onboarding SHALL remain separate from public-bootstrap
implementation. Repository access SHALL NOT be required for Core bootstrap.

## 4. AI Capability Discovery

Before environment-dependent actions, an implementation SHALL discover or
request relevant capabilities.

Relevant capabilities include:

- Markdown or structured-data access.
- Filesystem or repository access.
- Code execution.
- IANA timezone or calendar conversion.
- HTML, email, print, or PDF inspection.
- Deterministic test execution.
- Git or repository-host operations.
- Manual or human review.
- Provider-specific tools.

Unavailable capability SHALL be disclosed. An unavailable capability SHALL
NOT be converted into PASS evidence.

Semantic or provider-assisted interpretation SHALL be identified as such.
AI-generated interpretation SHALL NOT be described as executed code,
rendered output, repository verification, or deterministic test evidence.

## 5. Optional Execution Technologies

Projects MAY use Python, Node.js, GitHub, APIs, package managers, IDEs,
timezone libraries, renderers, test frameworks, browser tools, or other
technologies.

Optional extensions SHALL disclose:

- Runtime and dependency requirements.
- Platform or provider limitations.
- Required services or permissions.
- Fallback behavior.
- Output and temporary-file location.
- Executed versus manual or semantic evidence.
- Applicable project authority.

No optional extension SHALL become a COG Core requirement.

## 6. Portable Structured Data

Portable structured data SHOULD be used when it improves validation, transfer,
or automation.

It SHALL:

- Use explicit field names and units where relevant.
- Identify required and optional fields.
- Preserve original values and associated context.
- Preserve units, denominators, populations, and timezone context.
- Distinguish confirmed, missing, unavailable, stale, partial, unverified,
  uncertain, and unresolved values.
- Preserve conversion provenance.
- Avoid silently converting date-only values or uncertain historical context
  into confirmed absolute instants.
- Avoid creating universal COG metrics, statuses, calendars, thresholds, or
  deadlines.

Portable structured data SHALL NOT itself establish project authority or
require a fixed schema.

## 7. Evidence-Qualified Validation

Validation SHALL report:

- **PASS:** sufficient applicable evidence was executed or inspected and the
  criterion was met.
- **FAIL:** sufficient applicable evidence was executed or inspected and the
  criterion was not met.
- **INCOMPLETE:** required capability or evidence was unavailable.

Validation records SHALL identify whether evidence came from:

- Deterministic execution.
- Semantic analysis.
- Manual inspection.
- Provider-assisted processing.
- Repository verification.

AI interpretation, code presence, fixture availability, or unavailable
execution SHALL NOT be described as a passed test.

## 8. Provenance and Information States

Implementations SHALL preserve:

- Source observation and effective time.
- Reporting cutoff and refresh time.
- Presentation generation and publication time.
- Decision authorization time.
- Original source representation and canonical UTC representation where
  applicable.
- Reporting and presentation timezone roles.
- Date-only versus absolute-instant distinctions.
- Missing timezone, offset, or calendar context.
- Availability independently from freshness.
- Qualified information states.

Unknown or uncertain context SHALL remain disclosed. It SHALL NOT be silently
inferred or presented as confirmed.

Timezone conversion SHALL NOT create a new observation, event, decision,
action, or authorization.

## 9. Public Framework and Private Data

COG Core SHALL remain usable without private project data.

Implementations SHALL keep project evidence, identities, credentials, network
details, protected personal data, confidential incidents, operational data,
and proprietary sources within their authorized Local Context.

A public bootstrap SHALL contain no private operational or protected data.

Public-bootstrap implementation SHALL be separately authorized from project
report examples or F3 reporting implementation.

## 10. Browser, Email, Print, and Cross-Medium Meaning

Cross-medium presentation SHALL preserve:

- Scope and reporting period.
- Reporting and presentation timezone context.
- Metric values and denominators.
- Exception qualifications.
- Source and freshness context.
- Temporal meaning.
- Provenance and limitations.
- Distinguishable information states.
- Absence of implied authority.

HTML, Outlook-compatible email, print, PDF, static dashboard, interactive
dashboard, and machine-readable exports are optional media. No medium or
renderer is mandatory for COG Core.

Browser printing or PDF export MAY be optional project behavior. Automated PDF
generation SHALL NOT become a Core requirement.

## 11. Accessibility and Platform Independence

Documentation SHALL use readable Markdown and meaningful headings, labels,
lists, tables, and text alternatives where relevant.

Applicable digital content SHOULD follow COG-STD-005's WCAG 2.2 Level AA
design target. Accessibility SHALL remain medium-specific and SHALL not be
presented as certification unless independently established.

Instructions SHALL NOT require an IDE, GitHub, command line, package manager,
specific operating system, or provider-specific interface.

## 12. Conformance

A conforming implementation SHALL:

1. Provide a canonical Markdown bootstrap entry.
2. Support NEW and CONTINUE semantics.
3. Discover and disclose relevant environment capabilities.
4. Keep GitHub and repository hosting outside mandatory Core adoption.
5. Preserve applicable COG semantic requirements.
6. Keep project authority and Local Context boundaries explicit.
7. Preserve provenance and temporal distinctions.
8. Keep private data outside COG Core.
9. Distinguish PASS, FAIL, and INCOMPLETE evidence.
10. Document optional technologies and dependencies.
11. Document material exceptions and non-applicability.
12. Avoid universalizing project-specific metrics or calendar rules.

Conformance is proportionate and profile-dependent. It does not require a
particular runtime, provider, repository, filesystem, or output format.

## 13. Exceptions

Exceptions SHALL identify:

- Missing capability or evidence.
- Requirements affected.
- Semantic, manual, or alternative evidence.
- Project authority approving the exception.
- Residual limitation or risk.
- Reconsideration conditions.

An exception SHALL NOT convert INCOMPLETE evidence into PASS.

## 14. D01-D10 Relationship

The standard implements the owner-approved prospective D01-D10 architecture:

- D01: dependency-neutral and AI-provider-agnostic COG Core.
- D02: Markdown canonical bootstrap with portable structured data.
- D03: capability discovery and explicit unavailable-functionality disclosure.
- D04: Python, GitHub, APIs, and comparable technologies as optional
  extensions.
- D05: COG-STD-006 as the controlled portability standard.
- D06: ADR-0004 as the architectural decision record.
- D07: preservation of existing F3 reporting semantics without universalizing
  them.
- D08: temporary retention of Python artifacts, with replacement reserved for
  a future separately authorized gate.
- D09: evidence-qualified PASS, FAIL, and INCOMPLETE validation.
- D10: separation of public-bootstrap and F3 report-example implementation.

These mappings state conformance to owner approval; they do not reconstruct or
assert historical F2 decision provenance.

## 15. References

- [COG-STD-001](REPOSITORY_STANDARD.md)
- [COG-STD-002](NAMING_STANDARD.md)
- [COG-STD-004](DOCUMENTATION_STANDARD.md)
- [COG-STD-005](INFORMATION_PRESENTATION_STANDARD.md)
- [COG-GDE-001](../guides/PRESENTATION_DESIGN_GUIDE.md)
- [COG-GOV-001](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
- [COG-DEV-002](../development/GITHUB_WORKFLOW.md)
- [ADR-0002](../governance/ADR-0002-information-lifecycle-architecture.md)
- [ADR-0003](../governance/ADR-0003-shared-information-presentation-architecture.md)
- [ADR-0004](../governance/ADR-0004-dependency-neutral-framework-architecture.md)
