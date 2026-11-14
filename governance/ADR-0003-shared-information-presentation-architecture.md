---
document_id: ADR-0003
title: "Shared Information-Presentation Architecture"
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-11-13
---

# ADR-0003: Shared Information-Presentation Architecture

## ADR Decision Status

Accepted

## Decision Date

2026-11-13

---

## Context

Projects may need to present information to different audiences as reports or
dashboards and in different output formats. Separate, independently defined
presentation models could duplicate content semantics and weaken traceability.
A single presentation model, however, must not centralize project-specific
facts, decision authority, classification, permissions, or release policy.

The presentation architecture must preserve the information lifecycle and
authority boundaries established by [ADR-0001](ADR-0001-cog-operating-model.md)
and [ADR-0002](ADR-0002-information-lifecycle-architecture.md). In particular,
ADR-0002 establishes the Evidence Chain, Effective Information, and Decision
Chain, while leaving some relationships among decision concepts open for
future design.

This ADR records an accepted architecture, not an implementation
authorization. Its controlled-document lifecycle status is Active; its ADR
decision status is Accepted.

## Decision

COG adopts one reusable information-presentation foundation with a shared
content contract and distinct reporting and dashboard profiles. The foundation
defines reusable presentation semantics and traceability expectations.
Projects remain authoritative for the information presented and for
project-specific business rules, classification, permissions, approval, and
release.

The foundation is a presentation concern, not a new information-lifecycle
chain. It consumes or references information from the Evidence Chain and
Decision Chain without changing their meaning or stages.

### Shared Content Semantics

The common content contract should support, as applicable:

- Content identity, such as a title or purpose, and the intended scope.
- Intended audience or audiences.
- Facts and findings.
- Assessments.
- Recommendations.
- Decisions and dispositions.
- Actions.
- Provenance from presented claims or values to relevant source evidence,
  Effective Information, or authoritative decision information.
- Lineage for derived, transformed, or aggregated values, sufficient to
  identify their relevant inputs and transformations where available.
- The time represented by source information, distinguished from the time
  content was generated.
- Material limitations, uncertainty, assumptions, unresolved items, and
  known omissions.
- The applicable project or Local Context boundary where relevant to
  interpreting or distributing the presentation.

These are shared semantic capabilities, not a mandatory schema, field list,
serialization format, or project status model. The requiredness and
representation of individual elements remain for a later standard or project
definition.

Facts, findings, assessments, recommendations, decisions, dispositions, and
actions must remain semantically distinguishable where they are represented.
A presentation must not imply that an assessment is a decision, a
recommendation is authorized, or an action has occurred merely because it is
shown.

Audience-specific selection, ordering, and level of detail may differ, but
must not silently change the underlying information, provenance, authority,
or meaning.

### Reporting Profile

A report is a point-in-time presentation. It should make its scope, audience,
generation time, source-time or freshness limitations, and material
limitations clear enough for its intended use. A report may be rendered in
different formats without changing the meaning or authority of its content.

This profile does not select a required file format, rendering engine,
distribution mechanism, or project approval process.

### Dashboard Profile

A dashboard may be static or interactive. A static dashboard presents a
bounded view without requiring interaction. An interactive dashboard may
support user-driven filtering, navigation, or detail views.

Both forms should make scope and information freshness understandable.
Interactions and derived views should preserve, or provide a path to, relevant
provenance and Local Context. A dashboard's display or interaction must not
itself be treated as a decision or authorization.

This profile does not require live data, any particular refresh interval,
interactivity, persistence, or export capability.

### Lifecycle and Local Context Boundaries

Presentation consumes or references information produced or used by the
existing Evidence Chain and Decision Chain; it does not define a new stage or
resolve the ordering or relationships of Decision Chain concepts. Presentation
must not rewrite source evidence, Effective Information, provenance,
assessments, decisions, or their history. Any presented decision-related
information remains subject to its originating authority.

The Local Context protections in ADR-0002 remain in force. COG's reusable
presentation concepts may be shared while project information remains in its
appropriate private, protected, restricted, or environment-specific context.
Sharing COG definitions does not authorize or require information flow between
Local Contexts. COG must not require cross-pollination between security
domains. Projects remain responsible for context boundaries and for
authorization, classification, permissions, and release. This ADR does not
specify technical isolation or information-flow controls.

No private project information or evidence is to be copied into COG as part of
this architecture.

### Generation, Validation, Authorization, and Distribution

Generation, validation, authorization, distribution, and success verification
are distinct concerns and should be represented as distinct outcomes where
needed:

- **Generation** produces a presentation from identified inputs.
- **Validation** checks the content contract and the selected presentation
  profile, including relevant provenance, time, limitations, and
  presentation behavior.
- **Authorization** is the project-defined approval to release information;
  passing validation does not imply authorization.
- **Distribution** is the project-authorized delivery or publication of the
  output.
- **Success verification** confirms the expected generation or distribution
  outcome. Distribution success is evidenced by the appropriate downstream
  delivery confirmation, not merely by attempting to send or publish. Where
  relevant, provider acceptance, delivery, recipient acknowledgment, and
  actual consumption are distinct states. Projects determine which
  confirmation is appropriate; COG does not universally require proof that a
  recipient read or acted upon the output. A successful generation does not
  by itself establish successful distribution.

COG does not establish a universal approval authority, recipient model,
classification scheme, distribution channel, or release policy.

### Conceptual Pre-Flight Requirements

The Pre-Flight Gate is a reusable COG workflow capability. This ADR defines
its application to information presentation only; it does not establish the
universal Pre-Flight specification or implementation. Implementation remains
deferred. Before generation or release, an adopting process should be able to
determine and communicate:

- **Readiness:** whether required inputs, audience, scope, context, and
  applicable project prerequisites are available.
- **Content checks:** whether relevant contract elements, distinctions,
  provenance, source times, limitations, and unresolved items are represented
  adequately for the intended use.
- **Presentation checks:** whether the selected profile and output are usable
  and whether rendering or interaction preserves meaning and context.
- **Project authorization:** whether the project-required approval for the
  intended release exists. COG validation cannot grant that approval.
- **Pending state:** which prerequisites, checks, approvals, or delivery
  outcomes remain incomplete. Pending work must not be reported as completed.
- **Success verification:** whether the expected generation and, when
  applicable, distribution outcome occurred.
- **Controlled retry:** whether a failed or incomplete step can be retried
  without misrepresenting prior outcomes or causing unintended duplicate
  distribution or action. Retry safety and authorization remain
  implementation and project responsibilities.

This ADR does not require a fixed sequence, blocking gate, automated
validator, or universal status vocabulary. The operational behavior and
acceptance criteria require later design and project approval.

### Initial Portability Direction

Markdown/chat-friendly authoring and browser-first HTML/CSS are initial design
directions for evaluating usability and portability. They are not mandatory
implementation technologies, schemas, renderers, or runtime dependencies.
Other output formats may be evaluated without changing the shared content
semantics.

Version-pinned adoption and GitHub-optional onboarding remain separate future
workstreams. This ADR does not establish their requirements or a universal
adoption mechanism.

## Rationale

A shared content contract can reduce duplicated semantics and preserve
consistent traceability across reports and dashboards. Distinct profiles
recognize that point-in-time reports and static or interactive dashboards
have different presentation behavior without requiring separate underlying
content models.

Keeping COG's role at reusable semantics and presentation outcomes preserves
project authority over domain information and release. Explicit lifecycle and
Local Context boundaries prevent presentation from being mistaken for a new
decision stage or a mechanism for moving information between contexts.

Defining Pre-Flight concepts before implementation allows readiness,
validation, authorization, pending work, success, and retry to be considered
without prematurely mandating tools or automation.

## Alternatives Considered

### Separate Content Models for Reports and Dashboards

Independent models could optimize each output type, but risk duplicated
semantics, inconsistent provenance, and divergent meanings for shared
information. Distinct profiles over a common contract provide different
presentation behavior without duplicating core semantics.

### One Prescribed Universal Output

A single required format or renderer could simplify implementation, but would
create unnecessary coupling to particular tools and could limit adoption by
projects and users with different environments. This ADR therefore records
Markdown/chat-friendly authoring and browser-first HTML/CSS only as initial
design directions.

### Project-Defined Presentation Only

Leaving all presentation semantics to each project would maximize local
freedom, but would not provide reusable cross-project conventions for
provenance, audience, freshness, and clear separation of decision concepts.
Project authority remains intact for domain-specific content and controls.

### Implement an Automated Gate Immediately

Immediate automation could make checks repeatable, but readiness,
authorization, success, and safe retry criteria are not yet sufficiently
specified for a universal implementation. This ADR establishes conceptual
requirements and defers implementation.

## Consequences

### Benefits

- Provides one reusable semantic foundation for reports and dashboards.
- Preserves provenance and lineage as information is presented to different
  audiences.
- Supports static and interactive dashboard profiles and point-in-time
  reporting.
- Keeps project authority and Local Context boundaries explicit.
- Separates output validation from project authorization and distribution.
- Provides a basis for future Pre-Flight design without requiring automation.

### Tradeoffs and Limitations

- A later standard must define conformance and clarify which contract
  capabilities are required or conditional.
- Projects must map their information and approval processes to the shared
  concepts where they adopt them.
- Presentation behavior can differ by audience and output, so preserving
  equivalent meaning and provenance requires care.
- This ADR does not provide schemas, templates, renderers, validators, or
  distribution tooling.

### Risks

- A presentation may omit provenance, freshness, limitations, or context and
  thereby mislead its audience.
- Derived or aggregated values may obscure their source lineage.
- Audience-specific simplification may accidentally alter meaning or imply
  authority not granted by the project.
- A future gate may be misread as granting release permission unless
  authorization remains distinct from validation.
- Retry behavior may cause duplicate release or action if implementations do
  not verify prior outcomes.

## Open Questions

- Which shared content capabilities must be present in every presentation,
  and which are conditional on profile or project context?
- What minimum provenance and derived-value lineage is sufficient for
  different report and dashboard use cases?
- How should source time, generation time, and freshness limitations be
  represented consistently without prescribing a schema?
- When should a dashboard provide a stable point-in-time view, and how should
  that view relate to later refreshed or interactive states?
- What evidence should establish generation and distribution success, and
  what retry conditions avoid duplicate effects?
- How should a project represent partial completion, exceptions, or
  authorization pending without creating a universal status model?
- Which output formats merit future conformance guidance beyond the initial
  Markdown/chat-friendly and browser-first HTML/CSS direction?
- How should projects pin and update adopted versions, and what GitHub-optional
  onboarding is needed? These remain separate future workstreams.

This ADR does not resolve the open Decision Chain questions in ADR-0002,
including the sequence, boundaries, or requiredness of stages after Effective
Information; the status of Recommendation as a canonical stage or optional
output; or the conditions under which decision concepts may be combined.

## Implementation Notes

This accepted ADR establishes architecture only. It does not create a
mandatory content schema, directory structure, tool, rendering engine,
workflow, implementation, or automated Pre-Flight Gate.

Follow-on work may define a controlled information-presentation standard, then
optional templates or examples. Any implementation should be
considered only after the relevant project requirements, authorization,
validation, and distribution behavior are defined.

## Related Documents

- [ADR-0001: COG Operating Model](ADR-0001-cog-operating-model.md)
- [ADR-0002: COG Information Lifecycle Architecture](ADR-0002-information-lifecycle-architecture.md)
- [COG Documentation Standard](../standards/DOCUMENTATION_STANDARD.md)
- [COG Decision Record Standard](../standards/DECISION_RECORD_STANDARD.md)
- [COG Shared vs Project-Specific Governance](SHARED_VS_PROJECT_SPECIFIC.md)
- [COG Roadmap](../roadmap/ROADMAP.md)

## Supersedes

Not applicable.

## Superseded By

Not applicable.
