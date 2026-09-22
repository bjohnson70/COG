COG Practitioner Discovery Standard

Status: Draft
Project: COG — Common Operations Guide
Standard: Practitioner Discovery
Purpose: Capture and preserve practitioner knowledge describing how work is currently performed before attempting to improve, automate, or redesign it.

---

1. Purpose

Practitioner Discovery is the COG method for understanding work from the people who actually perform it.

Repositories, policies, procedures, management documentation, and system documentation may describe how work is intended to occur. They may not completely describe how work is actually performed.

Practitioners frequently possess operational knowledge gained through performing the work, including:

- actual workflow steps;
- decisions and judgment;
- dependencies;
- handoffs;
- exceptions;
- system limitations;
- manual activities;
- undocumented procedures;
- workarounds;
- recurring problems;
- historical context; and
- opportunities for improvement.

COG therefore treats practitioners as important sources of operational evidence.

Practitioner Discovery is intended to capture that evidence without assuming that any individual practitioner's description represents the complete or authoritative organizational process.

---

2. Core Principle

«You cannot improve nothing. You can improve a poorly executed something.»

Before COG attempts to optimize, automate, redesign, or otherwise improve work, the existing work must first be understood sufficiently to establish an AS-IS representation.

Practitioner Discovery therefore separates:

1. Discovery — understand what currently occurs.
2. Analysis — examine the discovered process.
3. Improvement — identify potential changes.
4. Decision — determine what changes should be adopted.
5. Implementation — establish the resulting TO-BE process.

Discovery must not be prematurely replaced by optimization.

---

3. The Practitioner Is Not the Process

Practitioner Discovery evaluates the work, not the person performing the work.

The objective is to understand:

- what work occurs;
- why it occurs;
- how it occurs;
- what information is required;
- what systems and tools are used;
- where decisions occur;
- where handoffs occur;
- what constraints exist;
- what exceptions occur; and
- where friction exists.

The discovery process must not characterize workflow problems as practitioner deficiencies without supporting evidence.

A practitioner may be correctly executing an inefficient process.

A practitioner may also have developed an effective workaround for an inefficient or incomplete process.

Both are valuable discoveries.

---

4. Practitioner Knowledge

COG uses practitioner knowledge to describe knowledge acquired or maintained by individuals through performing work.

Practitioner knowledge may overlap with:

- operational knowledge;
- institutional knowledge;
- experiential knowledge; and
- undocumented operational knowledge.

These terms are related but are not interchangeable.

Practitioner knowledge should be captured because repository owners, managers, architects, process owners, and other stakeholders cannot be expected to possess all knowledge held by the individuals performing the work.

---

5. Sources of Understanding

Practitioner Discovery may combine multiple sources of information.

5.1 Practitioner Statements

Information provided through conversation with the practitioner.

Examples:

- "I receive this spreadsheet every Monday."
- "I check these three fields before approving it."
- "When this condition occurs, I contact the program area."

Practitioner statements are evidence of how the practitioner understands or performs the work.

They are not automatically organizational requirements.

5.2 Governing Documentation

Documentation defining how work is expected or required to occur.

Examples include:

- laws;
- regulations;
- policies;
- standards;
- procedures;
- contracts;
- operating instructions;
- security requirements;
- privacy requirements; and
- approved process documentation.

5.3 Operational Artifacts

Artifacts generated or consumed while performing the work.

Examples include:

- forms;
- spreadsheets;
- reports;
- checklists;
- tickets;
- templates;
- emails;
- screenshots;
- system output; and
- completed examples.

5.4 Observed Examples

Examples showing how the process has actually been performed.

Examples can expose differences between:

documented process and actual process.

---

6. Evidence Solicitation

The AI conducting Practitioner Discovery should request supporting evidence when that evidence would materially improve understanding.

For example, when a practitioner says:

«"I review the request against our requirements."»

the AI should determine whether supporting material exists.

A useful follow-up may be:

«"Is there a policy, procedure, checklist, form, example, or other documentation that defines those requirements? If it is appropriate to provide within this approved environment, please provide it."»

The AI should not continuously request documents without purpose.

Evidence should be requested when it can:

- clarify the workflow;
- validate a requirement;
- explain a decision;
- identify an input or output;
- resolve uncertainty;
- document an exception;
- demonstrate an example; or
- distinguish documented procedure from actual practice.

---

7. Information Handling

Practitioner Discovery must respect organizational information-handling requirements.

The public COG repository contains the methodology.

Project repositories may contain generalized, non-sensitive implementation guidance.

Practitioner interviews may involve:

- internal processes;
- employee information;
- internal system information;
- security information;
- privacy information;
- protected information;
- proprietary information; or
- other non-public organizational information.

Such information must remain within environments authorized to process it.

COG does not require practitioner evidence to be stored in a public repository.

The preferred separation is:

PUBLIC
COG methodology
        ↓
Project implementation
        ↓
Practitioner Discovery instructions

PRIVATE / AUTHORIZED ENVIRONMENT
Practitioner conversation
        ↓
Supporting evidence
        ↓
Practitioner Knowledge Record

---

8. Project-Specific Discovery

COG defines the Practitioner Discovery methodology.

Individual projects define the context in which Practitioner Discovery occurs.

Examples may include:

- SAR;
- BSB;
- EIB;
- HOG; and
- future COG-compatible projects.

A project implementing this standard SHOULD provide a project-level file named:

"PRACTITIONER-DISCOVERY.md"

The project file should contain sufficient context for an AI system to understand:

- the project;
- its purpose;
- relevant terminology;
- known roles;
- known workflow;
- applicable public documentation;
- known constraints; and
- the objectives of Practitioner Discovery within that project.

The practitioner should not be required to understand COG before participating.

---

9. Practitioner Discovery Entry Point

A practitioner may begin discovery using either:

URL Mode

The practitioner provides the approved AI system with the public URL to the project's:

"PRACTITIONER-DISCOVERY.md"

The AI retrieves and reads the file before beginning discovery.

File / Content Mode

If the AI environment cannot retrieve external URLs, the practitioner may:

- upload the Markdown file;
- paste the Markdown into the conversation; or
- otherwise provide its contents.

Both methods should initialize substantially the same discovery process.

COG must not depend upon a particular AI vendor or product.

---

10. Discovery Dimensions

Practitioner Discovery should progressively establish the following.

Role

What responsibility does the practitioner have within the process?

Scope

What portion of the overall process does the practitioner perform?

Trigger

What causes the work to begin?

Inputs

What information, documents, requests, approvals, or system events are required?

Activities

What does the practitioner actually do?

Sequence

In what order does the work normally occur?

Tools

What systems, applications, spreadsheets, forms, communications, or other tools are used?

Decisions

Where must the practitioner make a decision or exercise judgment?

Handoffs

Who provides work or information to the practitioner?

Who receives work or information from the practitioner?

Outputs

What is produced?

What constitutes completion?

Exceptions

What happens when the normal process cannot be followed?

Constraints

What requirements limit how the work can be performed?

Examples include:

- policy;
- law;
- security;
- privacy;
- technology;
- staffing;
- contractual requirements;
- separation of duties; and
- organizational authority.

Friction

What portions of the process are:

- repetitive;
- manual;
- slow;
- confusing;
- duplicative;
- error-prone; or
- unnecessarily difficult?

Practitioner Ideas

What would the practitioner change if an appropriate improvement were possible?

Practitioner ideas should be preserved as evidence and potential improvement opportunities.

They are not automatically adopted as decisions.

---

11. Conversational Discovery

Practitioner Discovery should normally be conducted conversationally.

The AI should avoid presenting the practitioner with an unnecessarily large questionnaire.

Questions should build upon previous answers.

The AI should:

1. establish the practitioner's role;
2. establish the portion of the process performed;
3. follow the workflow from beginning to completion;
4. clarify decisions and exceptions;
5. request relevant supporting evidence;
6. identify unresolved questions;
7. summarize understanding periodically; and
8. allow the practitioner to correct misunderstandings.

The AI should favor questions such as:

«"What happens next?"»

«"What information do you need before you can do that?"»

«"How do you decide between those two outcomes?"»

«"What happens when that information is missing?"»

«"Is that requirement documented somewhere?"»

«"Who receives the work after you finish?"»

These questions encourage discovery without prematurely prescribing a solution.

---

12. Multiple Practitioners

A process may involve multiple practitioners.

They may:

- perform the same work;
- perform different portions of the work;
- perform the work differently;
- understand requirements differently; or
- encounter different exceptions.

COG must not prematurely combine these perspectives into a single representation.

Each practitioner's knowledge should initially remain distinguishable.

Example:

Practitioner A
        ↓
AS-IS-A

Practitioner B
        ↓
AS-IS-B

Practitioner C
        ↓
AS-IS-C

Subsequent analysis may identify:

- common steps;
- variations;
- role-specific activities;
- conflicting interpretations;
- undocumented requirements;
- unnecessary duplication;
- effective practices;
- exceptions; and
- opportunities for standardization.

Differences between practitioners are evidence.

They should not automatically be treated as errors.

---

13. Conversation Is Not the System of Record

AI conversations may be temporary.

Conversation history may be affected by:

- organizational retention policies;
- account changes;
- platform changes;
- model changes;
- access limitations; or
- the creation of a new conversation.

Therefore:

«Conversation is transient. Artifacts are durable.»

Important Practitioner Discovery information should be preserved outside the conversation whenever possible.

Markdown is the preferred COG format for portable Practitioner Discovery records.

---

14. Practitioner Knowledge Record

Practitioner Discovery SHOULD maintain a durable Markdown artifact representing the current state of discovery.

Recommended filename:

"PRACTITIONER-RECORD.md"

Projects may establish more specific naming conventions.

The record should contain, where applicable:

# Practitioner Knowledge Record

## Metadata

## Practitioner Role

## Process / Function

## Discovery Scope

## Current Understanding

## AS-IS Workflow

### Trigger
### Inputs
### Activities
### Decisions
### Handoffs
### Outputs
### Exceptions

## Systems and Tools

## Governing Documentation

## Supporting Evidence

## Practitioner Knowledge

## Known Variations

## Constraints

## Friction / Pain Points

## Practitioner Ideas

## Questions Remaining

## Evidence Requested

## Evidence Not Yet Available

## Improvement Observations

## Decisions

## Session History

## Continuation Instructions

The Practitioner Knowledge Record should distinguish:

- practitioner statements;
- documentary evidence;
- observed examples;
- assumptions;
- unresolved questions;
- proposed improvements; and
- approved decisions.

---

15. Checkpointing

Practitioner Discovery must not assume that the current AI conversation will remain available.

The practitioner should be able to request:

«Update my Practitioner Record.»

The AI should then generate the complete current Markdown record, not merely a list of changes.

A checkpoint should also be encouraged:

- after substantial discovery;
- after important evidence is reviewed;
- when the AS-IS understanding materially changes;
- before ending a working session; and
- whenever loss of conversation state would cause significant rework.

Full-file output is preferred over patches or diffs because it improves portability between AI systems and reduces manual reconstruction.

---

16. Continuing in a New AI Conversation

A Practitioner Knowledge Record should contain sufficient context to continue discovery in another approved AI conversation.

When provided with an existing record, the AI should:

1. read the entire record;
2. identify the project and practitioner role;
3. understand the existing AS-IS representation;
4. identify unresolved questions;
5. identify evidence previously requested;
6. determine whether material circumstances have changed;
7. continue discovery rather than restarting it; and
8. produce an updated complete record when appropriate.

The Markdown artifact therefore functions as portable operational memory.

---

17. AS-IS Before TO-BE

Practitioner Discovery primarily concerns the AS-IS state.

During discovery, potential improvements may become obvious.

These observations should be captured without allowing them to replace discovery.

Example:

DISCOVERY

"We manually copy these fields into another system."

        ↓

CAPTURE

Potential improvement opportunity:
Evaluate whether duplicate entry can be reduced.

        ↓

CONTINUE DISCOVERY

How often does this occur?
Why is the second system required?
What validation occurs?
What happens when values differ?

Optimization occurs after sufficient understanding exists.

---

18. Relationship to Evidence and Decisions

Practitioner Discovery contributes to the COG Evidence Chain.

Conceptually:

Practitioner Statement
        +
Supporting Documentation
        +
Operational Artifact
        +
Observed Example
        ↓
Evidence
        ↓
Analysis
        ↓
Validated AS-IS Understanding

Potential changes subsequently enter the appropriate Decision Chain.

Validated AS-IS
        ↓
Improvement Opportunity
        ↓
Analysis
        ↓
Proposed TO-BE
        ↓
Decision
        ↓
Approved Change

Practitioner knowledge should not silently become organizational policy.

Likewise, organizational documentation should not automatically override evidence showing that actual operations differ from documented expectations.

The difference itself may require analysis.

---

19. Human Role

AI assists Practitioner Discovery.

AI does not replace practitioner expertise.

The practitioner provides operational experience and context.

Other stakeholders may provide:

- organizational requirements;
- governance;
- technical expertise;
- policy interpretation;
- security expertise;
- privacy expertise;
- management decisions; and
- process ownership.

COG combines these sources to improve understanding.

The objective is collaborative discovery:

«Understand the work with the people who perform the work.»

---

20. Expected Outcome

Successful Practitioner Discovery should produce enough evidence to answer:

- Who performs the work?
- What role does each practitioner perform?
- What starts the work?
- What information is required?
- What actually happens?
- What systems and tools are involved?
- Where are decisions made?
- Where are handoffs?
- What outputs are produced?
- What exceptions occur?
- What requirements constrain the work?
- Where does friction exist?
- What documentation supports the process?
- Where does documented procedure differ from actual practice?
- What remains unknown?
- What opportunities warrant further analysis?

Only after these questions are sufficiently understood should the process move deliberately toward optimization or redesign.

---

21. COG Design Principle

Practitioners are not merely consumers of operational repositories.

They are participants in the knowledge lifecycle.

COG-compatible systems should therefore support:

Organization
     +
Leadership
     +
Practitioners
     +
Evidence
     ↓
Shared Understanding
     ↓
Analysis
     ↓
Decisions
     ↓
Improved Operations
     ↓
New Practitioner Experience
     ↓
New Evidence

The repository should not merely document work.

The repository should be capable of learning from the work.

---

22. Implementation Pattern

A COG-compatible project implementing Practitioner Discovery should generally follow:

PUBLIC / PORTABLE
────────────────────────────────

COG
Practitioner Discovery Standard
        ↓
Project Repository
PRACTITIONER-DISCOVERY.md
        ↓
URL / File / Copy-Paste

APPROVED AI ENVIRONMENT
────────────────────────────────

Project Context
        +
Practitioner Conversation
        +
Approved Supporting Evidence
        ↓

PRIVATE / AUTHORIZED STORAGE
────────────────────────────────

PRACTITIONER-RECORD.md
        ↓
AS-IS Representation
        ↓
Cross-Practitioner Analysis
        ↓
Improvement Opportunities
        ↓
Proposed TO-BE
        ↓
Decision Chain

---

23. Next Implementation

The initial implementation and validation of this standard should occur through a project-specific Practitioner Discovery implementation.

SAR — Software Assessment and Review — may be used as an initial test implementation.

Project-specific experience should be treated as evidence for improving this COG standard.

Project-specific behavior should not automatically become a generalized COG requirement without review.

---

End of Standard