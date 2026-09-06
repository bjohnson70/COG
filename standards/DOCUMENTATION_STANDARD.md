# COG Documentation Standard

## 1. Purpose

This standard defines the minimum reusable documentation-governance rules for
projects that adopt the Common Operations Guide (COG).

Documentation should make a project easier to understand, operate, and
maintain. The requirements in this standard are intentionally repository-
agnostic and should remain proportional to the importance and expected
longevity of the document.

Documentation is part of the system. Changes to architecture, workflows,
standards, or repository organization may require corresponding documentation
changes.

## 2. Core Principles

- Define once. Reference everywhere.
- One governed concept MUST have one canonical authoritative source.
- Existing projects are evidence for COG standards, not authoritative
  templates.
- Required concepts and outcomes should be standardized before physical
  repository layouts are prescribed.
- Project-specific requirements remain within the project.
- Duplicate authoritative documents SHOULD be consolidated or deliberately
  retired.
- Documentation governance SHOULD avoid unnecessary bureaucracy and premature
  standardization.

## 3. Controlled Documents

A **controlled document** is a durable document that establishes or records
authoritative project information. Controlled documents generally include:

- Standards
- Governance documents
- Architecture decisions
- Policies
- Authoritative plans
- Authoritative catalogs or registers
- Durable operational procedures where formal control is appropriate

Not every Markdown file is a controlled document. README files,
temporary working notes, examples, lightweight instructions, generated output,
informal drafts, and template usage notes normally do not require controlled-
document metadata.

Projects MAY designate additional documents as controlled when their importance,
expected longevity, or operational context justifies it.

## 4. Canonical Sources

One governed concept MUST have one canonical authoritative source. Other
documents SHOULD reference that source rather than reproduce substantial
portions of its requirements.

A document MAY summarize another document for navigation or context, but the
summary MUST NOT create a competing authority. When duplicate authoritative
material is discovered, the project SHOULD identify the canonical source and
deliberately consolidate or retire the duplicate.

## 5. Document Identity and Metadata

Controlled documents MUST have a minimal identity and metadata model containing:

- Document ID
- Title
- Status
- Version
- Owner, identifying an accountable person, role, team, or project authority
- Last Updated

The following metadata MAY be used when useful, but is not universally
required:

- Canonical Path
- Dependencies
- Supersedes
- Superseded By
- Review Date
- Applies To

This standard does not require YAML front matter or any other serialization
format. A project MAY implement metadata using front matter, a document header,
a catalog, or another consistent mechanism.

Document identity SHOULD remain stable through reasonable file moves or
renames. The file path is not, by itself, the document's identity.

### 5.1 Document IDs

Document IDs MUST be unique within the adopting repository, stable throughout
the document lifecycle, and not silently reused after retirement. IDs SHOULD be
human-readable where practical. Projects MAY use project-specific ID schemes.

This standard does not establish a universal COG ID prefix taxonomy. ADR
numbering and decision-record practices are governed by the
[Decision Record Standard](DECISION_RECORD_STANDARD.md).

## 6. Document Lifecycle

The baseline lifecycle has exactly four states:

- **Draft**: The document is being developed or reviewed and is not yet the
  current authority.
- **Active**: The document is approved and is the current authority for its
  governed subject.
- **Superseded**: A replacement document is the current authority, while this
  document remains available for historical traceability where appropriate.
- **Retired**: The document is no longer current authority and is not expected
  to govern future work.

Projects MAY add lifecycle states when their needs justify them, but MUST
document the meaning and transition rules for any added states.

Deletion SHOULD NOT be the normal mechanism for replacing a historically
significant controlled document.

## 7. Document Catalogs

An adopting project with enough controlled documents that authoritative
inventory provides meaningful governance or navigation value SHOULD maintain
one authoritative catalog or equivalent inventory. The catalog SHOULD make
controlled documentation discoverable and help identify:

- Duplicates
- Missing documents
- Conflicting statuses
- Broken dependencies
- Superseded material
- Stale paths

This standard does not require a separate `INDEX.md`. A README MAY provide
human navigation while the catalog provides the authoritative inventory.
Projects MAY maintain the catalog manually or automatically; this standard does
not prescribe either method.

## 8. Navigation and Links

Documents SHOULD answer these questions where relevant:

1. What is this?
2. Why does it exist?
3. How does it work or apply?
4. Where is the authoritative additional information?

Repository-relative links SHOULD be used for internal repository documentation
where practical. References SHOULD point to canonical sources. When documents
are moved or renamed, affected references SHOULD be updated as part of the
same logical change where practical.

Documents SHOULD link to substantial authoritative material rather than copy
large sections of it merely to avoid a reference.

## 9. Dependencies and References

Controlled documents MAY identify documents they depend upon. Dependencies
SHOULD describe meaningful governance or operational relationships, not every
incidental hyperlink.

A material change to a foundational document SHOULD trigger review of
materially dependent documents. The affected documents SHOULD be updated,
annotated, or explicitly confirmed as still accurate.

## 10. Review and Maintenance

Controlled documents SHOULD be reviewed when:

- Governing assumptions materially change
- A dependency changes materially
- A conflicting document is discovered
- Implementation demonstrates that the document is inaccurate
- The document is being superseded or retired

This standard does not impose an arbitrary periodic review interval across all
projects. Projects MAY establish scheduled reviews when operational, legal, or
compliance needs justify them.

## 11. Supersession, Retirement, and Archival

When a controlled document is superseded, the project SHOULD:

1. Identify the replacement.
2. Update the document's lifecycle status.
3. Preserve historical traceability where useful.
4. Update the authoritative catalog.
5. Update material references.

Retired documents MUST NOT be treated as current authority. Projects MAY
archive retired documents according to project needs, provided their retired
status remains clear and they are not presented as current requirements.

## 12. Project Adoption and Exceptions

Adopting projects remain authoritative for their project-specific
documentation. A project MAY:

- Adopt a COG documentation requirement
- Declare a requirement not applicable
- Establish a documented exception
- Implement the requirement using a project-appropriate structure

Exceptions SHOULD identify the reason and, when appropriate, the project
authority approving or maintaining the exception.

COG does not require an existing repository to reorganize solely to match
COG's physical layout. Adoption is measured by the required concepts and
outcomes, not by identical directory structures.

## 13. Relationship to Other COG Documents

This standard governs documentation identity, authority, lifecycle, catalogs,
references, review, supersession, and retirement. The boundaries with related
COG standards are:

- [`REPOSITORY_STANDARD.md`](REPOSITORY_STANDARD.md) governs repository-level
  required concepts and organization outcomes.
- [`NAMING_STANDARD.md`](NAMING_STANDARD.md) governs naming conventions.
- [`DECISION_RECORD_STANDARD.md`](DECISION_RECORD_STANDARD.md) governs ADRs and
  decision-record practices.
- [`SHARED_VS_PROJECT_SPECIFIC.md`](../governance/SHARED_VS_PROJECT_SPECIFIC.md)
  governs whether a practice belongs in COG or within a project.

Those documents remain authoritative for their stated boundaries. This
standard SHOULD reference them rather than duplicate their detailed
requirements.