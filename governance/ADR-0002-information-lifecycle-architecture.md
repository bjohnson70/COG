---
document_id: ADR-0002
title: "COG Information Lifecycle Architecture"
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-09-21
---

# ADR-0002: COG Information Lifecycle Architecture

## ADR Decision Status

Accepted

## Decision Date

2026-09-21

---

## Context

COG requires a reusable architecture for processing information from source
and evidence through interpretation, structured information, assessment, and
subsequent action. The architecture must support different project domains and
levels of automation without making one project's implementation, evidence, or
operational identities part of the COG standard.

The architecture must preserve the distinction between evidence processing and
decision processing. It must also support traceability, human authority,
quality measurement, and later re-evaluation without silently rewriting
historical processing.

## Decision

COG adopts a two-chain Information Lifecycle architecture consisting of an
Evidence Chain and a Decision Chain. The chains are connected by Effective
Information, which is the interface between them.

The architecture is reusable COG grammar and guidance. Implementing projects
remain authoritative for their operational facts, identities, evidence,
assessments, adjudications, decisions, dispositions, and implementation
choices.

### Accepted Design Direction

#### Two-Chain Model

The Evidence Chain is conceptually ordered as:

```text
Source / Evidence
    -> Machine Interpretation
    -> Structured Extraction
    -> Resolution
    -> Effective Information
```

The Evidence Chain determines what information downstream processes should
currently rely upon. It does not make the downstream decision on behalf of the
Decision Chain.

The Decision Chain begins with Effective Information. It evaluates that
information without rewriting the evidence or provenance that produced it.

Assessment is established as a Decision Chain concept. Assessment,
Recommendation, Decision, Disposition, and Presentation / Action are distinct
concepts and must not be assumed to be the same operation.

The architecture does not require every implementation to use every
conceptual stage or operation.

#### Effective Information

Effective Information is the interface between the Evidence Chain and the
Decision Chain. It represents the information that the Evidence Chain has
resolved as currently effective for downstream evaluation.

Effective Information does not erase or replace source evidence, machine
interpretation, structured extraction, resolution history, or provenance.

#### Human Review and Adjudication

Human Review / Adjudication is cross-cutting rather than a mandatory
sequential lifecycle stage. Human intervention should generally be
exception-oriented, while preserving cases where policy or authority requires
human participation.

Implementations should be able to represent three conceptual processing paths:

- Automation Path
- Exception / Human Adjudication Path
- Mandatory Human Authority Path

Human review is not required merely to establish traceability.

#### Traceability and Provenance

Traceability and provenance span both chains. The architecture must support
reconstruction, as applicable, of:

- Source evidence
- Machine interpretation
- Structured information
- Rules or guidelines used
- Assessment
- Recommendation, when applicable
- Decision
- Disposition
- Actor or decision authority
- Human adjudication, when applicable
- Effective result
- Subsequent re-evaluation or supersession

Prior evidence, machine processing, assessments, decisions, and adjudications
must not be silently rewritten. Historical processing must remain
reconstructable when later information, rules, or decisions change.

The architecture requires an append-only or tamper-evident decision history as
a direction for future implementation. This ADR does not select a technical
mechanism for achieving that property.

#### Decision Authority

Decision Authority is an architectural concept. An implementation may
authorize:

- Automated decision authority
- Mandatory human decision authority
- Project-defined or hybrid authority

The actor performing an assessment or recommendation does not necessarily
possess authority to make the resulting decision. Assessment, recommendation,
decision, disposition, and action must therefore remain distinguishable when
authority, accountability, or traceability requires that distinction.

#### Quality Assurance and Process Measurement

Quality Assurance / Process Measurement is a first-class cross-cutting
concern. COG defines reusable measurability and terminology; individual
projects establish acceptable thresholds based on risk, consequence, policy,
and decision authority.

The architecture should support measurement of at least:

- Automation Rate
- Human Review Rate
- Human Confirmation Rate
- Human Supersession Rate
- Human-Machine Agreement Rate
- Exception Rate
- Unresolved Rate
- Re-evaluation Rate
- Decision Reversal / Supersession Rate
- Trace Completeness
- Controlled QA Sampling
- Baseline / Drift Detection

A lower Human Review Rate is not inherently evidence of higher process
quality. Metrics must be interpreted in the context of risk, consequence,
policy, authority, and the quality of outcomes and traceability.

#### Public Standard and Local Context

COG defines reusable lifecycle concepts, states, roles, interfaces, and
conformance expectations. Implementing projects contain project-specific
operational facts, real identities, private evidence, inventories,
assessments, adjudication records, decisions, dispositions, and thresholds.

COG must not become a repository for those project-specific facts.

The following may be used as design cases for testing whether the architecture
remains reusable:

- HOG
- EIB
- Cyber Intelligence
- VOG
- TDL
- LIA
- VIM
- SAR
- BRM
- HPM
- CAE

These design cases are evidence used to derive and test reusable requirements.
They are not components of the COG architecture, and private operational
information from them must not be copied into COG.

### Candidate / Under Evaluation

The following relationships and structures are candidates for future
refinement, but are not finalized by this ADR:

- The exact sequence, boundaries, and requiredness of Decision Chain stages
  after Effective Information.
- Whether Recommendation is a canonical lifecycle stage, an optional output,
  or a project-defined operation.
- Whether Decision is always distinct from Recommendation or may be combined
  under defined authority conditions.
- The exact relationship and ordering of Assessment, Recommendation, Decision,
  Disposition, and Presentation / Action.
- The states, roles, interfaces, and conformance details needed for future
  implementation guidance.
- The technical mechanism used to provide append-only or tamper-evident
  decision history.
- Project-specific metric definitions, sampling designs, thresholds, and
  acceptance criteria.

### Open Questions

- What is the minimum canonical vocabulary required for interoperable use of
  the Decision Chain without prematurely fixing its stage model?
- Which transitions, if any, must be represented separately across all
  implementations?
- Under what conditions may an implementation combine assessment,
  recommendation, decision, disposition, or action while preserving authority
  and traceability?
- What information must be retained to reconstruct supersession and
  re-evaluation across changes in evidence, rules, authority, or outcomes?
- How should unresolved information and competing resolutions be represented
  without creating project-specific schemas in COG?
- What conformance expectations can COG define without prescribing a technical
  storage, audit, or workflow mechanism?
- Which cross-project metric definitions require tighter COG grammar, and which
  should remain project-defined?

## Rationale

The two-chain model separates determining effective information from evaluating
that information for a decision. This supports reuse across projects while
preserving project authority over domain-specific rules, facts, risk, and
operations.

Treating human review as cross-cutting supports automation where appropriate,
exception handling where needed, and mandatory human authority where required.
Separating decision authority from processing activity prevents an assessment
or recommendation from being mistaken for an authorized decision.

Cross-cutting provenance and measurement preserve the ability to evaluate both
outcomes and process behavior over time. Keeping unresolved relationships
explicit allows COG to capture the accepted architecture without prematurely
standardizing details that require further design evidence.

## Alternatives Considered

### Single Linear Lifecycle

A single mandatory sequence could make the architecture appear simpler, but
would conflate evidence processing, decision processing, and human authority.
It would also make optional, exception-oriented, and project-defined paths
harder to represent.

### Project-Specific Architectures Only

Leaving each project to define its own lifecycle would preserve local
flexibility, but would lose reusable grammar for effective information,
traceability, authority, and process measurement.

### Finalize All Decision Stages Immediately

Fixing the complete Decision Chain now would create premature standardization
while the relationship among assessment, recommendation, decision,
disposition, and action remains under evaluation.

## Consequences

### Benefits

- Establishes reusable COG architecture without selecting project
  implementations.
- Preserves evidence and decision traceability across the complete process.
- Supports automation, exception-oriented adjudication, and mandatory human
  authority.
- Makes decision authority and quality measurement explicit architectural
  concerns.
- Preserves open design questions for evidence-driven follow-up.

### Tradeoffs and Limitations

- Implementations must evaluate which concepts and paths apply to their risk,
  policy, authority, and operating context.
- The Decision Chain cannot yet be treated as a finalized canonical stage
  model.
- Projects remain responsible for metric thresholds, technical mechanisms,
  and domain-specific operational detail.
- Future COG guidance will need to refine terminology without creating a
  competing authority or silently changing historical meaning.

## Implementation Notes

This ADR establishes architectural direction only. It does not create schemas,
code, automation, templates, technical audit mechanisms, project-specific
logic, or additional standards.

Future design work should use project experience as evidence while preserving
the COG and project authority boundary. Any later normative lifecycle standard
should reference this ADR and explicitly resolve or retain the open questions
that remain material.

## Related Documents

- [COG Documentation Standard](../standards/DOCUMENTATION_STANDARD.md)
- [COG Decision Record Standard](../standards/DECISION_RECORD_STANDARD.md)
- [COG Shared vs Project-Specific Governance](SHARED_VS_PROJECT_SPECIFIC.md)
- [ADR-0001: COG Operating Model](ADR-0001-cog-operating-model.md)

## Supersedes

Not applicable.

## Superseded By

Not applicable.
