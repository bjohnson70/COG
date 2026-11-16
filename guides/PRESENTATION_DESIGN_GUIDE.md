---
document_id: COG-GDE-001
title: COG Presentation Design Guide
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-11-15
applies_to:
  - COG
  - Projects choosing to use this guidance
---

# COG Presentation Design Guide

> **Active COG controlled advisory guide.** The visual guidance and patterns
> below are non-normative and do not establish mandatory design or
> conformance obligations.

This guide does not replace or modify the Active
[COG Shared Information-Presentation Standard](../standards/INFORMATION_PRESENTATION_STANDARD.md)
(COG-STD-005). It does not grant permission to disclose information. Projects
retain authority over adoption, implementation, access, approval, and
distribution. Examples do not establish universal layouts, statuses,
thresholds, or technologies.

## 1. Purpose, Scope, and Status

This guide offers optional visual-design ideas for people preparing reports,
static dashboards, interactive dashboards, and related presentations. It is
intended to be understandable to nontechnical authors and useful to designers
and implementers.

The ideas may be considered across Markdown and AI chat, browser HTML/CSS,
Outlook-compatible HTML email, printable documents or PDF, and dashboard
views. Rendering capabilities differ by medium; an example may need to be
simplified or omitted in a particular output.

This guide is an Active COG controlled document containing advisory visual
guidance. It does not modify COG-STD-005 or
[ADR-0003](../governance/ADR-0003-shared-information-presentation-architecture.md).
COG-STD-005 remains the source for applicable presentation requirements,
including the design target of WCAG 2.2 Level AA for applicable digital
presentations. This guide makes no certification or conformance claim.

## 2. Design Principles

- **Meaning before decoration:** visual emphasis can help readers understand
  information, but should not change its meaning or authority.
- **Clear hierarchy:** titles, sections, labels, and supporting detail can
  help readers find what matters.
- **Readable density:** group related information and leave enough separation
  for the intended audience and medium.
- **Accessible, redundant cues:** where color or an icon conveys meaning,
  accompanying text or another perceivable cue can make that meaning clearer.
- **Portable meaning:** preserve important labels, context, and distinctions
  when the presentation moves between formats.
- **Context that matters:** make relevant provenance, time context, and
  limitations understandable through project-authorized means.
- **Local Context boundaries:** a visual pattern does not grant disclosure
  permission or authorize information movement between contexts.
- **Project-defined semantics:** projects determine the meaning of their
  metrics, thresholds, categories, and status labels.

The Evidence Chain, Effective Information boundary, Decision Chain, and
distinctions among evidence, findings, assessments, recommendations, decisions,
dispositions, and actions remain governed by
[ADR-0002](../governance/ADR-0002-information-lifecycle-architecture.md) and
COG-STD-005. Visual treatment should not make one of these concepts appear to
be another.

## 3. Typography and Visual Hierarchy

Typography can establish reading order without relying on decoration alone:

- Give the title and section headings distinct, consistent emphasis.
- Keep body text comfortable to read at the expected viewing distance and
  output size.
- Use labels and captions to identify values, units, time periods, and
  supporting context.
- Emphasize numbers only when the emphasis reflects their importance; retain
  enough label and unit context to interpret them.
- Use a small, understandable hierarchy rather than many nearly identical
  sizes or weights.

Font appearance and availability vary between browsers, email clients, chat
surfaces, and document viewers. A simple font fallback can preserve readable
text when a preferred typeface is unavailable. These are design considerations,
not prescribed font families or sizes.

## 4. Layout and Spacing

Related information can be grouped, aligned, and separated to help readers
understand its relationship. Headings, whitespace, rules, or restrained panels
can distinguish sections. Cards and panels are optional grouping devices, not
required components.

The useful information density depends on audience and medium. A compact
executive view may summarize information that a detailed assessment presents
more fully; the summary should retain a suitable path to supporting context.
Narrow screens, email clients, and printed pages may call for simpler
arrangements or different section breaks.

These approaches do not define a universal grid, breakpoint system, content
width, or spacing scale.

## 5. Color and Status Indicators

Color can provide a supplementary visual cue, for example to distinguish a
neutral label from an area needing attention. Consider contrast against the
background and whether the same meaning remains apparent in grayscale or
when color is not perceived. Pair color with a text label, icon, shape, or
other meaningful cue rather than relying on color alone.

An optional pattern is **icon + text + optional color**. The project defines
the state and its meaning; the icon and color merely reinforce that meaning.
Illustrative labels might include:

- Validation passed
- Awaiting approval
- Publication blocked
- Warning or at risk
- Informational
- Unavailable or no data, where the distinction is applicable

These are examples, not a fixed vocabulary, universal status taxonomy, or
state machine. Projects may use different terms and meanings.

Keep distinct concepts distinct. For example, validation passed does not mean
approved; approval does not mean published; sending does not by itself confirm
delivery; zero is not the same as no data; unavailable is not the same as
stale; and a finding is not an authorized decision. Use the distinctions
relevant to the presentation and its audience.

## 6. Tables and Structured Information

Tables can make comparisons easier when their structure remains clear:

- Use concise headers that identify what each column represents.
- Keep values aligned in a way that supports comparison; consistent alignment
  can help readers scan numbers.
- Choose a row density that remains readable in the target output.
- Give long text enough space or use a presentation appropriate to the
  medium, rather than allowing truncation to conceal material meaning.
- Label empty, unavailable, or unresolved values when those states affect
  interpretation.
- In an interactive table, make sorting or filtering behavior discoverable
  when present, and keep the active view's context understandable.

Wide tables may be difficult to read on narrow screens, in email, or in print.
A simpler summary or an alternate layout may work better in those cases.

## 7. Metrics and Key Performance Indicator (KPI) Presentation

A metric is easier to interpret when its title and value appear with applicable
units and measurement period. Where useful, comparisons can identify their
baseline or comparison period; a trend cue can include a label explaining
what direction represents.

Relevant source or freshness context and material limitations can prevent a
value from appearing more current or conclusive than its information supports.
Use precision appropriate to the source and purpose. Thresholds, definitions,
comparison rules, and interpretations remain project-specific; this guide
does not define universal KPIs or targets.

## 8. Charts and Visualizations

Choose a visualization that makes the intended comparison or relationship
understandable. Clear axis labels, units, and legends help readers interpret
what is shown. Visual proportions and scales should reflect the underlying
information rather than exaggerate or obscure a difference.

Consider a text summary or another accessible description for information
carried by a chart. Labels and patterns can help preserve meaning in grayscale
or print. An interactive chart may support exploration, while a static chart
needs enough visible context to be understood without interaction.

These are advisory considerations, not a universal chart taxonomy or a
prescribed choice of visualization.

## 9. Interactive Presentation

In an interactive view, readers benefit from being able to discover which
filters and selections are active and what scope the current view represents.
Where relevant, keep population, denominator, units, and other interpretation
context available as the view changes.

Loading, error, unavailable, and empty results may need distinct explanations
when they mean different things. Refresh cues should communicate relevant
freshness rather than imply unsupported currency. Keyboard operation and
visible focus are useful considerations for interactive controls.

Drill-down and export behavior depend on the project and medium. An
interactive pattern does not imply live refresh, export, persistence, or a
particular user-interface framework.

## 10. Medium-Specific Advisory Notes

The semantic meaning and appropriate authority of information are shared
concerns. Their visual rendering depends on the medium.

- **Markdown and AI chat:** headings, lists, and explicit labels tend to travel
  well. Keep essential context in text rather than relying on color, alignment,
  or rich layout.
- **Browser HTML/CSS:** structured headings and responsive arrangements can
  support different viewports. Interaction and styling should not be the only
  way to discover essential scope or limitations.
- **Outlook-compatible HTML email:** client rendering varies. Keep important
  meaning understandable when styling or advanced layout is unavailable; a
  plain-text or equivalent fallback may suit some project workflows.
- **Printable documents and PDF:** consider page breaks, reading order,
  legibility, link use, and grayscale output. A static export can identify the
  scope and time represented where relevant.
- **Static dashboards:** make the bounded snapshot and relevant information
  currency apparent; avoid a visual treatment that suggests unsupported live
  status.
- **Interactive dashboards:** expose relevant filters and selection context;
  provide suitable focus, loading, and error cues for the interaction.

These notes are advisory and do not require a format, renderer, layout, or
implementation technology.

## 11. Conceptual Pattern Examples

The following examples use synthetic information. They are advisory sketches,
not templates, required layouts, or project status definitions.

### A. Acceptance Criteria Scorecard

- **Audience:** Project reviewers.
- **Meaning:** Shows criteria and an assessment without implying release
  authority.
- **Text example:**

  ```text
  Review: Sample document
  Scope: Example review set | Generated: 2026-11-14
  Criterion                 Result             Supporting context
  Required fields            Meets criterion    Example source note A
  Reviewer confirmation      Awaiting review    No approval implied
  ```

- **Context:** The review scope, generation time, and suitable source
  references help readers interpret the rows.
- **Accessibility:** Text labels carry the results; color or icons, if used,
  are supplementary.
- **Medium limits:** A plain list may be easier than a table in chat or narrow
  email.
- **Status:** Advisory example.

### B. Executive Report Header

- **Audience:** Executives and decision-makers.
- **Meaning:** Orients the reader to a bounded report and concise summary.
- **Text example:**

  ```text
  Sample Operations Report
  Purpose: Illustrative monthly overview
  Scope: Example service group | Source period: October 2026
  Generated: 2026-11-14
  Limitation: One example source was not available for this summary.
  ```

- **Context:** Source period, generation time, scope, and limitation are
  separate pieces of context.
- **Accessibility:** Use a descriptive title and plain text labels.
- **Medium limits:** Keep essential context visible in email and in the first
  page or screen of a printable report.
- **Status:** Advisory example.

### C. KPI Summary

- **Audience:** Leaders and analysts.
- **Meaning:** Presents a value with its applicable unit and period rather
  than as an unsupported number.
- **Text example:**

  ```text
  Sample requests completed
  42 requests | Example period: October 2026
  Comparison: 38 requests in September 2026
  Source updated: 2026-11-10 | Generated: 2026-11-14
  Note: Values are illustrative and do not define a target.
  ```

- **Context:** Unit, comparison period, source update, and generation time
  support interpretation.
- **Accessibility:** Include the metric name and unit in text; do not make a
  trend arrow the only explanation.
- **Medium limits:** A compact value card may become a labeled list in chat,
  email, or print.
- **Status:** Advisory example.

### D. Status Table

- **Audience:** Operational readers.
- **Meaning:** Communicates project-defined states with supporting context.
- **Text example:**

  ```text
  Item             Project-defined state   Context
  Sample A         Reviewed                Example review record
  Sample B         Awaiting approval       Review is not approval
  Sample C         Unavailable             Source not received
  ```

- **Context:** The state labels are paired with explanations; “unavailable”
  does not imply “zero” or “stale.”
- **Accessibility:** Text states remain understandable without color.
- **Medium limits:** Shorten or reflow columns for narrow layouts and print.
- **Status:** Advisory example; state meanings remain project-defined.

### E. Static Dashboard Section

- **Audience:** Readers of a fixed snapshot.
- **Meaning:** Summarizes an example population without implying live status.
- **Text example:**

  ```text
  Example Service Snapshot
  Scope: Sample group | Source through: 2026-11-10
  Generated: 2026-11-14
  Received: 42 | Pending: 3 | Source unavailable: 1
  Note: This is a bounded example snapshot, not a live view.
  ```

- **Context:** Scope, source time, generation time, and limitation appear
  alongside the values.
- **Accessibility:** Explicit labels explain each value; a chart is optional.
- **Medium limits:** Retain the snapshot context in a static export or printed
  page.
- **Status:** Advisory example.

### F. Interactive Dashboard State Display

- **Audience:** Users exploring an interactive view.
- **Meaning:** Shows how selections define the displayed population.
- **Text example:**

  ```text
  View: Sample requests
  Filters: Region = Example North; Period = October 2026
  Population: 24 requests | Denominator: 24 requests
  Selected category: Example Category A
  Data through: 2026-11-10 | Refreshed: 2026-11-14 08:00
  Result: 0 of the 24 requests match Example Category A.
  ```

- **Context:** Filters, population, denominator, and relevant times explain
  the displayed zero.
- **Accessibility:** Make selections perceivable without color and consider
  keyboard access and visible focus for controls.
- **Medium limits:** A static export should identify the selected view and
  scope represented at export time.
- **Status:** Advisory example; it does not define a universal interaction or
  status model.

## 12. Adoption and Exceptions

Projects decide whether this guide is useful and
which patterns, if any, fit their context. Use remains project-owned and
selective. Nothing here creates automatic project conformance or replaces
COG-STD-005.

Visual examples do not grant permission to disclose source information.
Projects retain authority over Local Context boundaries, access, classification,
approval, and distribution. Any adoption or exception remains subject to
project governance.

This guide establishes no universal version-pinning mechanism, automatic
binding, or silent upgrade process. Projects remain responsible for recording
their own guidance choices until a separate approach is approved.

## 13. Open Questions and Deferred Work

The following remain outside this guide:

- Fixed design tokens, palettes, font families, or spacing systems.
- Production-ready templates or reusable software components.
- A separate pattern library.
- Separate medium-specific implementation guides.
- Framework-specific components or renderer requirements.
- Universal rendering checks or accessibility certification.
- A universal version-pinning mechanism.
- A universal status vocabulary or state machine.

Further guidance may be considered if project experience demonstrates a
reusable need and the work receives separate authorization.

## 14. References

- [COG Shared Information-Presentation Standard (COG-STD-005)](../standards/INFORMATION_PRESENTATION_STANDARD.md)
- [ADR-0003: Shared Information-Presentation Architecture](../governance/ADR-0003-shared-information-presentation-architecture.md)
- [ADR-0002: COG Information Lifecycle Architecture](../governance/ADR-0002-information-lifecycle-architecture.md)
- [ADR-0001: COG Operating Model](../governance/ADR-0001-cog-operating-model.md)
- [Shared vs Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
- [COG Documentation Standard](../standards/DOCUMENTATION_STANDARD.md)
- [COG Naming Standard](../standards/NAMING_STANDARD.md)
- [COG Repository Standard](../standards/REPOSITORY_STANDARD.md)
- [COG Decision Record Standard](../standards/DECISION_RECORD_STANDARD.md)
- [GitHub Development Workflow](../development/GITHUB_WORKFLOW.md)
