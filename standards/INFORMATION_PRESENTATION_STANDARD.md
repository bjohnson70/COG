---
document_id: COG-STD-005
title: COG Shared Information-Presentation Standard
status: Active
version: 1.1
owner: COG Project
last_updated: 2026-11-15
applies_to:
  - COG
  - Projects adopting COG
depends_on:
  - governance/ADR-0002-information-lifecycle-architecture.md
  - governance/ADR-0003-shared-information-presentation-architecture.md
---

# COG Shared Information-Presentation Standard

## 1. Purpose, Scope, Authority, and Non-Goals

This standard establishes reusable requirements for presenting information
as reports and dashboards. It defines a shared semantic contract and three
profiles: Reporting, Static Dashboard, and Interactive Dashboard.

The standard is intended to help projects present information consistently
while preserving traceability, meaning, project authority, and Local Context
boundaries. It addresses presentation outcomes rather than project business
rules, data models, or implementation choices.

This standard is an Active COG authority. Its requirements are available for
project adoption and MUST NOT be represented as binding on a project that has
not adopted them. Projects remain authoritative for deciding whether and how
to adopt this standard, subject to their own governance.

This standard does not:

- Define or change the Evidence Chain, Effective Information boundary, or
  Decision Chain established by
  [ADR-0002](../governance/ADR-0002-information-lifecycle-architecture.md).
- Supersede or amend the accepted presentation architecture in
  [ADR-0003](../governance/ADR-0003-shared-information-presentation-architecture.md).
- Establish project-specific business rules, metric definitions, thresholds,
  classifications, access permissions, approval authorities, or release
  policies.
- Require cross-context information flow or copying of project-specific
  information into COG.
- Mandate a schema, renderer, dashboard library, connector, file layout,
  distribution channel, or implementation technology.
- Define or implement the universal COG Pre-Flight Gate.

## 2. Relationship to ADR-0002 and ADR-0003

[ADR-0002](../governance/ADR-0002-information-lifecycle-architecture.md)
defines the Evidence Chain and Decision Chain, connected through Effective
Information. Presentation consumes or references information from those
chains; it is not an additional lifecycle stage and MUST NOT rewrite source
evidence, Effective Information, provenance, or decision history.

ADR-0002 establishes distinctions among assessment, recommendation, decision,
disposition, and presentation/action while leaving some ordering and
relationship questions open. This standard preserves those distinctions and
does not resolve the deferred questions.

[ADR-0003](../governance/ADR-0003-shared-information-presentation-architecture.md)
establishes one shared information-presentation foundation with distinct
reporting and dashboard profiles. This standard establishes conformance
requirements for that foundation, including a separate static dashboard
profile. It applies the architecture without creating separate content models
for reports and dashboards.

The [COG operating model](../governance/ADR-0001-cog-operating-model.md) and
[Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
remain authoritative for the boundary between reusable COG guidance and
project authority. The [Documentation Standard](DOCUMENTATION_STANDARD.md)
remains authoritative for controlled-document identity, lifecycle, adoption,
and exceptions.

## 3. Normative Language and Applicability

This section defines the intended meaning of normative terms in this
standard:

- **MUST** identifies a requirement necessary to preserve semantic integrity,
  traceability, authority, or an applicable profile outcome.
- **MUST NOT** identifies a prohibited outcome that could misrepresent
  information, authority, or context.
- **SHOULD** identifies a recommended practice that is normally appropriate.
  A project may choose another approach when its context justifies it.
- **MAY** identifies an optional practice or capability.

Requirements apply according to their stated scope:

- **Shared requirements** apply to every presentation within this standard's
  scope.
- **Conditional requirements** apply only when the stated information,
  context, or feature is present or material.
- **Profile requirements** apply only to the selected Reporting, Static
  Dashboard, or Interactive Dashboard profile.

Examples and explanatory guidance are not mandatory controls unless expressly
identified as requirements. A project may document non-applicability or a
justified exception in accordance with its authority and applicable
governance. This standard creates no conformance obligation for projects
that have not adopted it.

## 4. Shared Information-Presentation Contract

The shared contract defines semantic outcomes, not a required field list,
serialization format, schema, or citation layout.

### 4.1 Meaning and authority

1. A presentation MUST preserve the meaning and authority of the information
   it represents.
2. Where represented, source evidence, facts and findings, assessments,
   recommendations, decisions, dispositions, and actions MUST remain
   distinguishable when their distinction is material to interpretation,
   authority, accountability, or traceability.
3. A presentation MUST NOT imply that a recommendation has been approved, a
   decision has been made, a disposition has been authorized, or an action has
   been completed unless supported by authoritative information.
4. Audience-specific selection, ordering, summarization, or level of detail
   MUST NOT silently change meaning, provenance, or authority.
5. A presentation MUST NOT, by itself, create or confer decision, disposition,
   authorization, or completion authority. It MAY faithfully represent an
   appropriately authorized decision, disposition, or action record.

### 4.2 Purpose, audience, and scope

Where material to the intended use, a presentation SHOULD make its identity,
purpose, intended audience, and scope understandable. Conditional details
SHOULD be included when their absence could materially mislead the audience.
No universal metadata schema or set of labels is required.

### 4.3 Traceability

A presentation MUST provide traceability appropriate to the information and
its intended use so that relevant claims or values can be related to
authoritative source information, evidence, Effective Information, or
decision information. Traceability MUST be made available through
project-authorized means appropriate to the intended authorized audience,
applicable classification, access permissions, information sensitivity,
Local Context boundaries, and project governance. This does not require
underlying evidence or sensitive details to be reproduced or exposed to every
recipient.

Traceability MAY be provided through direct references, linked supporting
material, an accompanying source list, or another project-appropriate method,
provided the method respects those authorization and context boundaries. This
standard does not prescribe a universal citation format, placement, or
technical mechanism.

### 4.4 Time and limitations

Where time affects interpretation, a presentation MUST distinguish relevant
source observation or effective time from presentation generation time. If
refresh occurs, refresh time SHOULD be distinguishable from those other
times. A recently generated presentation MUST NOT be described as current or
live solely because of its generation time.

Material uncertainty, assumptions, known omissions, missing inputs,
unresolved matters, and other limitations MUST be disclosed in a manner
appropriate to the intended authorized audience and use, applicable
classification and access permissions, information sensitivity, Local Context
boundaries, and project governance. Disclosure does not require exposing
sensitive details to recipients who are not authorized to receive them.

## 5. Provenance, Derived-Value Lineage, Freshness, Limitations, and Local Context

### 5.1 Provenance and derived values

The traceability outcome in Section 4.3 applies to source claims and values
presented. For a transformed, calculated, or aggregated value, the
presentation MUST preserve or provide an appropriate path to enough
information about relevant inputs and transformations to support
interpretation and reasonable verification.

The amount and form of lineage may depend on the derivation, risk, audience,
and intended use. The standard does not require disclosure of irrelevant
implementation detail or prescribe one universal lineage record, formula
format, or display location. Access to supporting inputs and transformations
MUST respect applicable authorization, classification, access permissions,
information sensitivity, Local Context boundaries, and project governance.

### 5.2 Freshness and limitations

Projects SHOULD represent source currency and freshness in terms suitable to
the information and intended use. Where multiple sources have materially
different times or refresh states, the presentation SHOULD avoid implying a
single uniform currency.

When relevant, a presentation SHOULD distinguish:

- Source observation, effective, or reporting time.
- Refresh time, if the information or view is refreshed.
- Presentation generation time.

It SHOULD distinguish unavailable, missing, stale, uncertain, and unresolved
information where those states affect interpretation. These are semantic
distinctions, not a required universal status vocabulary.

Projects SHOULD distinguish zero, no data, unavailable data, stale data,
and unresolved information where applicable and material to interpretation.
These conditional distinctions do not establish a fixed status vocabulary,
state machine, dashboard widget, or live-refresh requirement.

Temporal representation and interpretation apply proportionately where
temporal context materially affects interpretation, comparison, calculation,
reporting boundaries, or historical reconstruction. These requirements do
not require every narrative presentation to expose UTC or to implement
timezone-conversion infrastructure.

Where an adopting implementation represents absolute instants in
machine-readable form for comparison, calculation, ordering, or historical
reconstruction, those instants MUST be unambiguous and comparable on the UTC
timeline. UTC MUST be the canonical representation used for those instants.

UTC normalization MUST NOT be interpreted as authorization to discard
original source timestamps, offsets, timezone identifiers, or other material
provenance. The canonical UTC representation MAY coexist with the original
source representation and associated conversion context. Normalization does
not require the audience-facing presentation to display UTC.

Where a reporting period, business day, date-only deadline, fiscal period, or
other local-calendar rule determines an instant boundary, the project MUST
specify the applicable reporting timezone and the interpretation rule
sufficiently to determine that boundary. The project remains authoritative
for its calendars, cutoffs, business-day rules, and deadline policies. A
reporting timezone and an audience's presentation timezone are distinct
contexts; they MAY be the same or different.
Reporting and presentation timezones MUST NOT be silently conflated, even
when they use the same timezone identifier; their respective semantic roles
remain distinct.

A date-only value MUST NOT be silently interpreted as a UTC timestamp or
other absolute instant. Converting a date-only value to an instant requires
an applicable calendar boundary and timezone rule. Where a local wall-clock
time is ambiguous or nonexistent, the project MUST define how that case is
resolved or rejected; it MUST NOT be silently assigned a different instant.

Where omitting timezone or offset context could materially change an
audience's interpretation of a displayed timestamp, the presentation MUST
identify sufficient timezone or offset context. A presentation MAY show UTC,
local time, or both, as appropriate to the audience, use, medium, and
traceability needs. Showing both is not a universal requirement.

Where material to interpretation, auditability, or historical reconstruction,
projects SHOULD preserve the original timestamp representation, the
corresponding effective instant, and the conversion context, including
relevant offset and timezone information. For local-calendar rules, a stable
timezone identifier and any project-defined interpretation policy SHOULD be
retained when needed to reproduce the result. Converting a timestamp changes
its representation, not the underlying observation, event, decision, action,
or authorization, and MUST NOT be recorded as creating a new one.

Where historical timezone, offset, or calendar-rule information is
insufficient to determine an exact instant reliably, an implementation MUST
NOT silently infer the missing information from the host machine, current
location, or an assumed default. Material uncertainty MUST be identified
where it affects interpretation, calculation, or historical reconstruction.
An unverified instant MUST NOT be presented as confirmed. These requirements
do not mandate automatic migration or rewriting of historical records.

Source observation time, effective time, reporting cutoff, refresh time,
generation time, publication time, and decision authorization time are
distinct concepts. A presentation MUST distinguish those that materially
affect its interpretation; conversion between timezones MUST NOT collapse
them into one time or imply that one occurred at another.

These requirements do not prescribe a programming language, library, data
schema, field list, renderer, fixed reporting timezone, universal calendar,
freshness threshold, or dual-time display. Projects determine implementation,
business rules, and any stricter controls. Existing adoption, proportionality,
and exception provisions in this standard remain applicable.

### 5.3 Local Context and information-flow boundaries

The Local Context protections in ADR-0002 remain in force. Sharing this
standard or another COG framework definition does not authorize or require
information flow between Local Contexts.

This standard MUST NOT require cross-context information flow. Project-specific
data, credentials, identities, permissions, private evidence, connector
details, and operational information MUST remain under the responsible
project's authority and MUST NOT be copied into the shared COG standard.
Examples in this document are generic and do not authorize any particular
information flow.

Projects remain responsible for deciding how context boundaries, access,
classification, authorization, and release are represented and enforced.

## 6. Reporting Profile

A report is a bounded point-in-time presentation. A report MUST make its
scope, relevant information currency, and generation time understandable for
its intended use. It SHOULD identify its purpose and intended audience where
those are not otherwise clear.

Where material to interpretation, a report SHOULD identify source context and
distinguish source times from generation time. It MUST disclose material
limitations under Section 4.4.

A report MAY provide a concise executive summary, detailed assessment,
supporting evidence, or multiple levels of detail. A summary MUST NOT change
the underlying meaning, authority, or traceability of the information it
summarizes.

Pending or unresolved matters MUST NOT be presented as completed findings or
actions. The report's format and layout may vary by audience, medium, and
project need.

## 7. Static Dashboard Profile

A static dashboard presents a bounded view that does not require interaction
to understand the displayed information. It MUST make its snapshot scope and
relevant information currency understandable.

A static dashboard MUST NOT imply live refresh or current status without
supporting evidence. Where material, it SHOULD identify source context,
generation time, and freshness limitations.

Values, applicable units and categories, and material limitations MUST be
understandable for the intended audience. Summarized or derived values MUST
retain or provide an appropriate path to relevant provenance and lineage.

This profile does not require an export function, live data, or any particular
visual arrangement.

## 8. Interactive Dashboard Profile

An interactive dashboard MAY support filtering, drill-down, navigation,
selection, or changing views. It MUST preserve enough context for users to
understand what information is currently displayed and how interaction affects
that view.

Where material, the dashboard MUST make applied filters, selections, scope,
units, populations, and denominators visible or otherwise discoverable.
Interactions MUST NOT silently alter the source scope, population, units,
denominator, or authority in ways that materially change interpretation.

Where applicable and material to interpretation, the presentation SHOULD
distinguish zero from no data, unavailable data, stale data, and unresolved
information. These distinctions do not establish a universal status
vocabulary, fixed state machine, mandatory dashboard widget, or live-refresh
requirement.

Filtering, navigating, selecting, or drilling down MUST preserve applicable
Local Context and information-flow boundaries. Relevant provenance and
lineage SHOULD remain available through project-authorized means. This does
not require sensitive context identifiers, security architecture, internal
authorization details, or private evidence to be displayed. Interaction
behavior and access control remain subject to project authority.

## 9. Presentation Quality and Accessibility

Presentations SHOULD use clear visual hierarchy, legible text, meaningful
labels, understandable units, and a consistent treatment of equivalent
information. Status or meaning SHOULD NOT be conveyed by color alone.

For applicable digital presentations, **WCAG 2.2 Level AA is a design target**,
subject to medium-specific feasibility and project context. This target is
not, by itself, a certification, audit result, or universal legal-compliance
claim. Output media may not support every WCAG success criterion in the same
way; projects SHOULD identify material limitations and suitable
accommodations.

Where applicable to the medium and interaction, presentations SHOULD support
keyboard operation, meaningful structure and labels for assistive technology,
and text alternatives for relevant non-text content. Projects remain
responsible for determining applicable obligations and conformance claims.

## 10. Output Portability and Format-Specific Considerations

The shared contract is technology-neutral. When information is rendered in
multiple formats, its semantic meaning, provenance, time context, and
limitations SHOULD remain available and understandable in each format.
Format-specific differences SHOULD be documented where they materially affect
interpretation or use.

The following format-specific notes are advisory compatibility guidance, not
additional normative requirements or mandated technologies, renderers, export
functions, layouts, or output channels. Apply them as appropriate to the
project and medium. The normative requirements above and the applicable
accessibility considerations in Section 9 remain in effect.

- **Markdown and chat-friendly outputs:** consider clear headings, labels,
  lists, and links; retain essential scope, time, limitations, and traceability
  in the content available to the reader.
- **Browser-first HTML/CSS:** consider meaningful document structure and
  usable responsive presentation where the target environment supports it.
  As an advisory design consideration, make essential scope or limitations
  discoverable without requiring interaction.
- **Outlook-compatible HTML email:** consider variation in email-client
  rendering and feature support. As an advisory design consideration,
  preserve important meaning when styling or advanced layout is unavailable;
  consider a suitable plain-text or equivalent fallback where the project
  requires it.
- **Printable or PDF-style outputs:** consider page boundaries, legibility,
  meaningful reading order, and whether links or references remain usable in
  the intended print or document context. A static export may identify the
  scope and time represented where material.

These considerations do not establish mandatory output formats, a preferred
renderer, or a required output stack.

## 11. Presentation Pre-Flight and Validation

The Pre-Flight Gate is a reusable COG workflow capability. This section
defines only its application to information presentation and does
not establish the universal Pre-Flight specification, a blocking gate, or an
implementation.

An adopting process SHOULD be able to determine and communicate, as
applicable:

- **Readiness:** whether required inputs, audience, scope, context, and
  project prerequisites are available.
- **Content checks:** whether applicable contract requirements, semantic
  distinctions, traceability, lineage, times, limitations, and unresolved
  matters are adequately represented.
- **Profile checks:** whether the selected profile's requirements are met,
  including relevant rendering, accessibility, portability, or interaction
  behavior.
- **Validation outcome:** which applicable checks passed, failed, were not
  performed, or remain pending, without treating pending work as complete.
- **Authorization prerequisite:** whether project-required authorization is
  present before release; validation cannot grant that authorization.
- **Generation-only use:** whether the expected output was generated. Local
  use or internal viewing without a distribution step does not require a
  distribution outcome.
- **Downstream verification:** when distribution occurs, whether the
  distribution outcome has appropriate downstream confirmation.

Projects determine applicable checks, acceptance criteria, evidence, process,
and retry behavior. This standard does not require automation, a universal
status vocabulary, or a prescribed check sequence.

## 12. Authorization, Distribution, and Success Verification

Generation, validation, authorization, distribution when applicable, and
success verification MUST be treated as distinct outcomes where relevant.
Passing validation MUST NOT be presented as release authorization. Generation
for local use or internal viewing without a distribution step does not require
a fictional distribution outcome.

When a process claims successful distribution, that claim MUST be based on
appropriate downstream confirmation, not solely on attempting to send or
publish. Depending on the channel and purpose, provider acceptance, delivery,
recipient acknowledgment, and actual consumption may be distinct outcomes.
Projects determine which confirmation is appropriate. Proof that a recipient
read or acted on an output is not universally required.

Projects retain authority over classification, access permissions,
authorization, approval, release, recipients, and distribution mechanisms.
This standard does not define a universal release or delivery process.

## 13. Conformance, Exceptions, and Project Adoption

Conformance SHOULD be assessed proportionally and by applicable
profile. An adopting project SHOULD:

1. Identify the presentation types and profiles in scope.
2. Determine which shared, conditional, and profile requirements apply.
3. Assess whether the intended outcomes are met.
4. Document material exceptions or non-applicability where useful or required
   by project governance.

This standard does not create a central COG certification authority or
require a particular assessment record, audit method, or scoring system.
Projects remain authoritative for adoption, classification, access,
authorization, approval, release, and implementation. Projects MAY establish
stricter project-specific controls.

## 14. Open Questions and Deferred Decisions

This standard does not resolve the following:

- What minimum provenance and derived-value lineage is sufficient for
  different presentation risks and uses.
- How projects should represent mixed source times, partial completion, or
  stale information consistently without a universal schema or status model.
- Whether a future revision should establish more specific accessibility
  evaluation guidance beyond the WCAG 2.2 Level AA design target.
- Which output formats merit additional compatibility guidance based on
  adoption evidence.
- What evidence and retry conditions are appropriate for particular
  distribution channels and projects.
- Whether common examples or templates would provide enough demonstrated
  value to justify separate artifacts.

The following remain separate or deferred workstreams and are not established
by this standard:

- Universal schemas.
- Renderers, dashboard libraries, connectors, or distribution integrations.
- Automated validators.
- Universal Pre-Flight specification or implementation.
- Universal NEW/CONTINUE bootstrap.
- GitHub-optional onboarding.
- Practitioner Discovery adoption.
- Project-specific templates, workflows, business rules, or status models.

## 15. References

- [ADR-0001: COG Operating Model](../governance/ADR-0001-cog-operating-model.md)
- [ADR-0002: COG Information Lifecycle Architecture](../governance/ADR-0002-information-lifecycle-architecture.md)
- [ADR-0003: Shared Information-Presentation Architecture](../governance/ADR-0003-shared-information-presentation-architecture.md)
- [Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
- [COG Documentation Standard](DOCUMENTATION_STANDARD.md)
- [COG Decision Record Standard](DECISION_RECORD_STANDARD.md)
- [COG Naming Standard](NAMING_STANDARD.md)
- [COG Repository Standard](REPOSITORY_STANDARD.md)
- [GitHub Development Workflow](../development/GITHUB_WORKFLOW.md)
