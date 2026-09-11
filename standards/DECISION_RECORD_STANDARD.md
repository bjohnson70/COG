---
document_id: COG-STD-003
title: COG Decision Record Standard
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-09-06
---

# COG Decision Record Standard

## 1. Purpose and Scope

This standard establishes the Common Operations Guide (COG) approach for
recording consequential architectural, engineering, governance, and
operational decisions.

An Architecture Decision Record (ADR) is COG's generic durable decision-record
mechanism. An ADR may record a consequential decision involving:

- Architecture
- Governance
- Operations
- Security
- Privacy
- Compliance
- Data
- Interoperability
- Other durable project concerns

ADR is the record mechanism even when a decision is governance or operational
rather than purely software architecture. COG does not create separate
record types merely because a decision belongs to a different domain.

The purpose of an ADR is to preserve:

- What was decided
- Why the decision was necessary
- What alternatives were considered
- What constraints influenced the decision
- What consequences resulted from the decision

A good ADR allows a future contributor to understand why the current system
exists without reconstructing the original conversation.

---

## 2. Core Principle

Consequential decisions and their rationale should not exist only in:

- Conversations or chat
- Meetings
- Issues or tasks
- Commit messages
- Personal memory

Those sources may provide useful evidence, but repository capture as an ADR is
expected only when the ADR threshold is met. The existence of a decision alone
does not require an ADR.

The repository should preserve meaningful decisions, not require future
maintainers to rediscover them.

COG standards define reusable concepts and outcomes. Existing projects provide
evidence for COG standards, but their conventions do not automatically become
COG requirements. Projects adopt applicable COG standards and may document
justified exceptions or non-applicability.

---

## 3. When an ADR Is Appropriate

An ADR SHOULD be created when a decision has durable or cross-cutting
consequences and one or more of the following apply:

- It has significant architectural impact.
- It is difficult, costly, or disruptive to reverse.
- It has material security, privacy, compliance, interoperability, data,
	operational, or governance consequences.
- It selects among meaningful alternatives.
- Future maintainers would reasonably be likely to revisit it without knowing
	the original rationale.
- It establishes a reusable project or cross-project precedent.

A decision does not need to satisfy every criterion. The deciding consideration
is whether preserving the decision and rationale will materially reduce future
uncertainty or inappropriate reconsideration.

Subject-area impact alone does not require an ADR. A decision in an important
area may remain ordinary project work when its consequences are minor,
reversible, or already determined by an accepted standard.

---

## 4. Decisions That Normally Do Not Require an ADR

The following normally SHOULD NOT require an ADR unless the decision
independently meets the consequentiality threshold:

- Routine implementation choices
- Ordinary maintenance
- Typographical or editorial corrections
- Straightforward conformance to an existing standard
- Routine dependency updates
- Ordinary file moves or renames
- Commits implementing an already-approved decision
- Temporary experiments or troubleshooting
- Low-consequence reversible choices
- Routine project-specific exceptions
- Issues or tasks that record work rather than establish a durable decision

A standards change or governance change is not automatically ADR-worthy. It
warrants an ADR when the change itself meets the threshold, especially when it
establishes durable policy, resolves meaningful alternatives, or creates a
precedent.

Avoid creating ADRs merely to document activity. Routine implementation and
maintenance should remain lightweight.

---

## 5. Decision Scope and Routing

An ADR is the durable record mechanism. A decision may be classified by:

**Scope**

- Project-specific
- Reusable or cross-project

**Domain**

- Architecture
- Governance
- Operational
- Security
- Data
- Interoperability
- Other appropriate domain

These classifications do not create separate ADR-like record types.

Routing guidance:

- Standards changes are ordinary changes unless consequential enough for an
	ADR.
- Governance changes use an ADR when they are durable or precedent-setting.
- Implementation decisions normally remain implementation work unless they
	meet the ADR threshold.
- Project-specific exceptions normally remain project governance unless they
	meet the ADR threshold.
- Temporary experiments normally remain notes, issues, tasks, or experimental
	artifacts until they result in a durable decision.

Reusable or cross-project decisions do not automatically become COG standards.
They should be evaluated through the applicable COG governance process. The
[Shared Versus Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
document may be referenced for boundary and navigation guidance, but it is
the authority for the boundary between reusable COG governance and
project-specific authority. It is not a substantive dependency of this Active
standard.

---

## 6. ADR Decision Status

ADR Decision Status describes the disposition of the decision, not the
controlled-document lifecycle of the ADR file.

The decision dispositions are:

- **Proposed**: Under review and not yet accepted.
- **Accepted**: Approved and currently authoritative as a decision.
- **Rejected**: Considered and explicitly not adopted.
- **Superseded**: Replaced by a later Accepted decision.

These dispositions are distinct from the controlled-document lifecycle. The
[COG Documentation Standard](DOCUMENTATION_STANDARD.md) governs controlled-
document status, metadata, lifecycle, supersession, and retirement. This
standard does not duplicate its Draft, Active, Superseded, or Retired rules.

An ADR SHOULD identify the related replacement when its decision status is
Superseded.

---

## 7. ADR Identity and Numbering

Adopting repositories SHOULD use sequential, repository-local ADR numbering in
the form:

```text
ADR-####
```

For example:

```text
ADR-0001
```

The numbering rules are:

- ADR numbering is repository-local.
- Numbers are assigned within the adopting repository or project.
- ADR numbers MUST NOT be reused.
- Gaps are acceptable.
- The ADR number remains stable throughout the decision's life.
- Moving or renaming the ADR file does not change the ADR's identity.
- References SHOULD be updated when paths change.

ADR numbering is distinct from COG controlled-standard IDs such as
`COG-STD-003`. ADR numbering does not establish a universal COG Document ID
taxonomy.

An ADR governed by this standard does not need a second general-purpose
controlled Document ID in addition to its ADR number. For that ADR, the
repository-local ADR number MAY serve as its stable document identifier for
the purposes of the Documentation Standard. This is a document-type-specific
identifier convention, not a universal Document ID taxonomy.

Filename syntax belongs to the [COG Naming Standard](NAMING_STANDARD.md). A
project MAY use a practical filename such as:

```text
ADR-0001-descriptive-title.md
```

This example does not impose a universal path, directory, or casing
requirement.

---

## 8. Minimum ADR Content

An ADR SHOULD contain the minimum durable information necessary to understand
the decision:

- Stable ADR number and title
- ADR Decision Status
- Decision date
- Context or problem
- Decision
- Rationale
- Consequences and meaningful tradeoffs
- Related documents or dependencies when material
- Supersedes or Superseded By references when applicable

Alternatives considered SHOULD be documented when meaningful alternatives
actually existed. Contributors SHOULD NOT fabricate alternatives for obvious or
routine decisions.

Implementation detail should remain proportional to what future maintainers
need to understand the decision. The [ADR Template](../templates/ADR_TEMPLATE.md)
provides the implementation form and will be refined separately; it is not the
governing authority for ADR requirements.

---

## 9. Location and Project Adoption

A project SHOULD maintain ADRs in a predictable and discoverable repository
location. A project MAY use an established existing ADR location when
authority and discoverability remain clear.

This standard does not require one universal ADR directory layout across all
adopting projects and does not require cosmetic repository migrations solely to
adopt the standard.

Repository organization outcomes belong to the [COG Repository Standard](REPOSITORY_STANDARD.md).
Naming syntax belongs to the [COG Naming Standard](NAMING_STANDARD.md).
Projects remain responsible for applying the standard, documenting justified
exceptions, and identifying ADRs in their own repository context.

---

## 10. Relationship to Other COG Documents

The boundaries with related COG documents are:

- [DOCUMENTATION_STANDARD.md](DOCUMENTATION_STANDARD.md) owns controlled-
	document identity principles, controlled-document metadata, controlled-
	document lifecycle, general Document ID governance, and general
	supersession and retirement governance.
- This standard owns the ADR threshold, ADR Decision Status, ADR numbering,
	stable ADR decision identity, and minimum durable ADR content.
- [NAMING_STANDARD.md](NAMING_STANDARD.md) owns filename and naming syntax.
- [REPOSITORY_STANDARD.md](REPOSITORY_STANDARD.md) owns repository
	organization outcomes and repository hygiene.
- [SHARED_VS_PROJECT_SPECIFIC.md](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
 provides authority for determining whether a practice belongs in COG or a
 project. It is referenced for boundary and navigation guidance only.
- [GITHUB_WORKFLOW.md](../development/GITHUB_WORKFLOW.md) owns detailed Git
 workflow execution for implementing accepted decisions. It is referenced for
 boundary and navigation guidance only.
- [ADR_TEMPLATE.md](../templates/ADR_TEMPLATE.md) provides the usable ADR
	form and is not the governing authority. It will be refined separately.

This standard does not govern general controlled-document lifecycle, physical
repository layout, filename syntax, detailed Git workflow execution, or
roadmap planning. It does not make Draft documents substantive dependencies.