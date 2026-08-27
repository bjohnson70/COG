# COG Naming Standard

## 1. Purpose

This document establishes reusable naming conventions for repositories,
directories, files, branches, and related development artifacts governed by
the Common Operation Guide (COG).

The objective is to create naming practices that are:

- Predictable
- Human-readable
- Searchable
- Portable across operating systems
- Compatible with Git and GitHub
- Easy to use from desktop and mobile devices
- Sustainable across multiple projects

COG naming standards apply to new projects unless a documented
project-specific requirement justifies an exception.

---

## 2. Core Principle

Naming conventions should reduce cognitive load.

A contributor should be able to reasonably predict:

- Where information belongs
- What a file contains
- Whether an artifact is project-specific or reusable
- How related artifacts will be named
- How to search for the artifact later

Consistency is more valuable than cleverness.

---

## 3. Repository Names

Repository names should be:

- Short
- Descriptive
- Stable
- Easy to type
- Appropriate for use in URLs and command-line tools

Project acronyms may be used when the acronym represents an established
project or framework.

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

These names SHOULD retain their conventional form.

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

File naming SHOULD favor clarity, portability, and predictable discovery.

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
- Characters that create cross-platform compatibility problems
- Names that differ only by capitalization

---

## 7. Branch Names

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

---

## 8. Legacy Repository Migration

Existing repositories are not required to perform disruptive, all-at-once
renaming solely to satisfy this standard.

When an existing repository uses a different naming convention:

1. Do not create additional inconsistencies.
2. Apply this standard to new directories where doing so will not create
   unnecessary structural confusion.
3. Document planned structural changes before renaming established paths.
4. Update links, scripts, configuration, documentation, workflows, and other
   references when a directory is renamed.
5. Prefer small, reviewable migration changes over a single large
   restructuring commit.
6. Verify repository functionality after each migration step.

Legacy structure is evidence of previous project decisions; it does not
automatically establish the standard for future projects.

---

## 9. Project-Specific Exceptions

A project MAY deviate from this standard when there is a legitimate reason,
such as:

- Framework or tooling requirements
- Compatibility with an external system
- Established ecosystem conventions
- Migration risk
- A documented architectural requirement

Project-specific exceptions SHOULD be documented in the project's architecture
or decision records.

Exceptions SHOULD remain narrow and should not redefine the COG standard for
other projects.

---

## 10. Governance

COG is the authoritative location for reusable naming standards shared across
projects.

Individual projects SHOULD reference this standard rather than independently
creating competing naming conventions.

The governing principle is:

> Define the convention once in COG. Reference it everywhere else.

When accepted development practices materially change, update the COG
standard first and then evaluate downstream projects for appropriate
migration.