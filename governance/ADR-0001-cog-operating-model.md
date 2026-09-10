---
document_id: ADR-0001
title: "COG Operating Model: Reusable Cross-Project Governance with Project-Specific Authority"
status: Active
version: 1.0
owner: COG Project
last_updated: 2026-09-09
---

# ADR-0001: COG Operating Model - Reusable Cross-Project Governance with Project-Specific Authority

## ADR Decision Status

Accepted

## Decision Date

2026-09-09

---

## Context

COG was established because reusable engineering and governance practices were
emerging across projects. Maintaining equivalent reusable rules independently
in each project would create duplicated maintenance, documentation drift, and
inconsistent interpretation.

At the opposite extreme, moving project-specific requirements, architecture,
implementation, operations, and local governance into one central repository
would over-centralize authority and couple projects to structures that may not
fit their domains.

A durable authority boundary was therefore needed between reusable
cross-project governance and project-specific authority and implementation.

## Decision

COG is authoritative for reusable cross-project governance when centralization
is justified. Individual projects remain authoritative for their
project-specific requirements, architecture, implementation, operations, and
local governance.

Projects evaluate whether COG guidance applies before adopting it. COG does
not require identical physical repository layouts. Existing projects are
evidence for reusable practices, not automatic templates for COG or future
projects. Projects should reference authoritative COG sources rather than
wholesale-copying reusable governance when practical.

Detailed placement criteria, promotion flow, exception handling, and adoption
rules remain authoritative in [SHARED_VS_PROJECT_SPECIFIC.md](SHARED_VS_PROJECT_SPECIFIC.md).

## Rationale

The hybrid model was selected because it reduces duplicated governance and
documentation drift while improving consistency for genuinely reusable
practices. It preserves project autonomy and accommodates domain-specific
requirements and operating contexts.

It also allows future projects to adopt COG selectively, avoids cosmetic
repository migrations, and keeps COG reusable rather than tied to current
projects. The model establishes a durable basis for evaluating future
project-derived practices without making project history an automatic source
of COG authority.

## Alternatives Considered

### Fully Project-Local Governance

Each project independently defines and maintains its own governance and
engineering conventions.

This provides maximum local autonomy, but creates duplicated maintenance,
divergence, and inconsistent interpretation. It also makes reusable governance
harder to maintain coherently.

### Fully Centralized or Uniform Governance

COG centrally defines reusable governance and mandates common physical
repository structures or implementation models.

This could provide greater uniformity, but would create inappropriate coupling,
encourage cosmetic migrations, reduce project autonomy, and risk forcing
domain-specific needs into generic structures.

## Consequences

### Benefits

- Centralized reusable governance
- Reduced duplication and interpretive drift
- Clearer authority boundaries
- Easier adoption by future projects
- Preserved rationale for the COG operating model

### Tradeoffs

- Projects must evaluate applicability.
- Intentional differences between projects will remain.
- COG and project documentation must maintain clear references.
- Promotion into COG requires judgment.
- Project teams remain responsible for applying COG appropriately.

### Risks and Limitations

- COG may become over-centralized if project-specific material is promoted too
  aggressively.
- Projects may diverge unnecessarily if applicable reusable guidance is
  ignored.
- Authority may become ambiguous when standards are copied instead of
  referenced.
- The model requires continuing judgment about canonical ownership.

## Implementation Notes

The operating governance for this decision is implemented through the Active
COG standards and [SHARED_VS_PROJECT_SPECIFIC.md](SHARED_VS_PROJECT_SPECIFIC.md).
Projects may adopt applicable COG governance without cosmetic restructuring.

## Related Documents

The following are authoritative operating sources for their respective
subjects:

- [SHARED_VS_PROJECT_SPECIFIC.md](SHARED_VS_PROJECT_SPECIFIC.md)
- [DOCUMENTATION_STANDARD.md](../standards/DOCUMENTATION_STANDARD.md)
- [REPOSITORY_STANDARD.md](../standards/REPOSITORY_STANDARD.md)
- [NAMING_STANDARD.md](../standards/NAMING_STANDARD.md)
- [DECISION_RECORD_STANDARD.md](../standards/DECISION_RECORD_STANDARD.md)

## Supersedes

Not applicable. This is the first COG ADR.

## Superseded By

Not applicable.
