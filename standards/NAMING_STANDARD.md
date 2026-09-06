---
title: COG Naming Standard
document_id: COG-STD-002
version: 1.0
status: Active
owner: COG Project
last_updated: 2026-09-05
---

# COG Naming Standard

## 1. Purpose

This standard establishes reusable naming conventions for repositories,
directories, files, branches, and related development artifacts governed by
the Common Operations Guide (COG).

The objective is to create naming practices that improve:

- Predictability
- Discoverability
- Portability
- Maintainability

Projects adopting this standard SHOULD apply these conventions to new artifacts
unless a documented project-specific or ecosystem requirement justifies an
exception.

---

## 2. Core Principle

Naming conventions should reduce cognitive load.

A contributor should be able to reasonably predict:

- Where information belongs
- What a file contains
- Whether an artifact is project-specific or reusable
- How related artifacts will be named
- How to search for the artifact later

Consistency is more valuable than cleverness. Naming conventions SHOULD make
related artifacts easy to find and distinguish without creating unnecessary
project-wide rules.

---

## 3. Repository Names

Repository names SHOULD be:

- Concise
- Descriptive
- Stable
- URL-compatible
- Portable across common development environments

Repository names SHOULD NOT depend on local filesystem behavior for their
meaning. Names SHOULD use characters that behave predictably in URLs,
command-line tools, and common development environments.

Established acronyms MAY be used when they are meaningful to the intended
contributors.

Examples:

```text
COG
EIB
POG
VOG
```

Repository naming is intentionally independent from directory naming.

An established project may use an uppercase acronym as its repository name
while using lowercase functional directories within the repository.

---

## 4. Directory Names

Functional repository directories SHOULD use lowercase names.

These are naming defaults, not a universal physical repository layout. The
[COG Repository Standard](REPOSITORY_STANDARD.md) governs repository-
organization outcomes and does not require existing projects to rename
directories solely for cosmetic consistency.

Lowercase directory names:

- Align with common Git, GitHub, Linux, and open-source development practices
- Reduce case-sensitivity problems across operating systems
- Are easier to type in command-line environments
- Produce predictable paths and URLs
- Reduce ambiguity between repositories, directories, and document names

Examples:

```text
architecture/
config/
connectors/
data/
development/
docs/
governance/
implementation/
roadmap/
src/
standards/
templates/
tests/
```

New functional directories SHOULD use lowercase names unless a documented
technical, ecosystem, or project-specific requirement requires otherwise.

Directory names containing multiple words SHOULD use lowercase kebab-case
when practical.

Examples:

```text
data-sources/
security-controls/
test-data/
```

Avoid creating new functional directories that differ only by capitalization.

For example, do not create both:

```text
docs/
DOCS/
```

---

## 5. Conventional and Required Exceptions

Some repository artifacts have names established by GitHub, development
tooling, community convention, or external ecosystems.

These names SHOULD retain their conventional form. Externally defined or
technically required names take precedence over COG naming defaults when
necessary.

Examples include:

```text
.github/
README.md
LICENSE
CONTRIBUTING.md
CHANGELOG.md
CODE_OF_CONDUCT.md
SECURITY.md
```

Tool-generated or ecosystem-required directories MAY also retain the naming
required by the applicable technology.

Exceptions SHOULD be based on compatibility or recognized convention rather
than personal preference.

---

## 6. File Names

File naming SHOULD favor clarity, portability, predictable casing, and
predictable discovery.

Projects SHOULD use established ecosystem conventions when they exist.

Common repository-level documents SHOULD retain their conventional names,
including:

```text
README.md
LICENSE
CONTRIBUTING.md
CHANGELOG.md
SECURITY.md
```

Project-specific documentation SHOULD use a consistent naming convention
defined by the applicable COG documentation standard or documented
project-specific requirement.

File names SHOULD avoid:

- Unnecessary spaces
- Ambiguous abbreviations
- Unnecessary special characters
- Characters that create cross-platform compatibility problems
- Names that differ only by capitalization

Filenames SHOULD use an extension appropriate to the file format. Filenames
MUST NOT rely solely on case differences to distinguish separate artifacts.
Avoid spaces and unnecessary special characters in repository filenames unless
an external convention, tool, format, or project requirement justifies them.

COG does not require one universal filename casing rule where an established
ecosystem convention requires another form.

---

## 7. Identifiers and Filenames

Document IDs, other stable identifiers, filenames, paths, display titles, and
branch names are distinct concepts. A stable identifier MUST NOT be assumed to
be equivalent to a filename or path.

Controlled-document identity and Document ID governance belong to the
[COG Documentation Standard](DOCUMENTATION_STANDARD.md). This standard does
not create a Document ID taxonomy.

### 7.1 Markdown and Controlled-Document Filenames

A controlled document's filename SHOULD follow applicable naming conventions,
but its authoritative identity and lifecycle are governed by the COG
Documentation Standard. A controlled document's identity MUST NOT change
merely because its file is moved or renamed.

### 7.2 Date-Bearing Filenames

Dates SHOULD appear in filenames when the date is materially part of the
artifact's identity or meaning, such as:

- Snapshots
- Dated reports
- Chronological records
- Captured-state artifacts

When a calendar date is encoded in a filename, use the unambiguous ISO-style
format `YYYY-MM-DD` unless an external system or established project
requirement requires another format. Dates are not required in every filename.

### 7.3 Version Identifiers in Filenames

For ordinary controlled Markdown documents, versions SHOULD be represented in
controlled-document metadata rather than filenames. Avoid patterns such as
`document-v1.md`, `document-v2-final.md`, or `document-final-final.md` when
metadata and repository history provide authoritative versioning.

Version identifiers MAY remain in filenames when required by an external
system, artifact format, release packaging, compatibility requirement, or
another justified project-specific convention.

### 7.4 Abbreviations and Acronyms

Established abbreviations and acronyms MAY be used when they improve usability
and are meaningful to the intended contributors. Unfamiliar abbreviations
SHOULD be defined in authoritative project documentation.

Familiar repository identifiers such as COG, EIB, POG, and VOG do not need to
be expanded in every filename. Projects SHOULD NOT invent project-wide
acronyms merely to shorten filenames.

### 7.5 Development Artifacts

Scripts, configuration files, test fixtures, and generated artifacts intended
for repository storage SHOULD use the same clarity, portability, and
predictability principles as other filenames. This standard does not define
language-specific naming rules. Temporary and local-only artifacts are
governed by the [COG Repository Standard](REPOSITORY_STANDARD.md).

## 8. Branch Names

Branch names SHOULD be:

- Short
- Descriptive
- Lowercase
- Easy to type

Where multiple words are required, use lowercase kebab-case.

Examples:

```text
feature/rss-collector
fix/feed-parser
docs/repository-standard
refactor/config-loader
```

Projects MAY define additional branch prefixes when needed.

This section governs branch naming only. Operational branch creation, usage,
migration, commit sequencing, and verification belong to the
[GitHub Development Workflow](../development/GITHUB_WORKFLOW.md).

---

## 9. Legacy and Renamed Artifacts

Existing repositories are not required to perform disruptive, all-at-once
renaming solely to satisfy this standard. When an artifact is renamed, the new
canonical name SHOULD be clear and affected references SHOULD be updated as
part of the logical change where practical.

Temporary legacy names MAY coexist during migration when required, but the
canonical artifact MUST remain unambiguous. Detailed repository migration
belongs to the [COG Repository Standard](REPOSITORY_STANDARD.md) and the
[GitHub Development Workflow](../development/GITHUB_WORKFLOW.md). Detailed
controlled-document supersession and retirement belong to the
[COG Documentation Standard](DOCUMENTATION_STANDARD.md).

When an existing repository uses a different naming convention, contributors
SHOULD:

1. Avoid creating additional inconsistencies.
2. Apply this standard to new directories where doing so will not create
   unnecessary structural confusion.
3. Prefer small, reviewable naming changes over a single large restructuring.

Legacy structure is evidence of previous project decisions; it does not
automatically establish the standard for future projects.

---

## 10. Project-Specific Exceptions

A project MAY deviate from this standard when there is a legitimate reason,
such as:

- External systems
- Established ecosystem conventions
- Compatibility requirements
- Domain-specific needs
- Existing repository constraints

Exceptions SHOULD remain narrow and SHOULD be documented in the project's
authoritative architecture or governance documentation where appropriate.
Projects SHOULD consult [Shared Versus Project-Specific Governance](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
when deciding whether a convention belongs in COG or in the project. The
[Decision Record Standard](DECISION_RECORD_STANDARD.md) MAY be referenced for
consequential decisions, but this standard does not require an ADR merely
because a naming exception exists.

Exceptions SHOULD NOT redefine the COG standard for other projects.

---

## 11. Relationship to Other COG Documents

COG is the authoritative location for reusable naming conventions shared
across projects. Individual projects SHOULD reference this standard rather
than independently creating competing naming conventions.

The boundaries with related COG documents are:

- [DOCUMENTATION_STANDARD.md](DOCUMENTATION_STANDARD.md) governs controlled-
  document identity, metadata, lifecycle, catalogs, references, supersession,
  and retirement.
- [REPOSITORY_STANDARD.md](REPOSITORY_STANDARD.md) governs repository-level
  organization outcomes and repository hygiene.
- [DECISION_RECORD_STANDARD.md](DECISION_RECORD_STANDARD.md) governs ADRs and
  decision-record practices.
- [SHARED_VS_PROJECT_SPECIFIC.md](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
  governs whether a practice belongs in COG or within a project.
- [GITHUB_WORKFLOW.md](../development/GITHUB_WORKFLOW.md) governs detailed
  Git workflow execution, branch operations, migration sequencing, and
  verification.

This standard owns reusable naming syntax and naming conventions. It does not
own controlled-document lifecycle, Document ID taxonomy, physical repository
organization, ADR governance, Git workflow execution, security requirements,
AI-assisted development, device-specific workflow, or release management.

The governing naming principle is:

> Define the convention once in COG. Reference it everywhere else.

When accepted development practices materially change in a way that affects
this standard, update the COG standard first and then evaluate adopting
projects for appropriate migration. References to related COG documents establish boundaries and
navigation; they do not make this standard substantively dependent on their
unfinished requirements.