# TB-0003 — Governance Model

Document ID: TB-0003
Title: Governance Model
Version: 0.1.0
Status: Draft
Created: 2026-06-25
Last Updated: 2026-06-25
Authority: Constitutional
Phase: Phase 0 — Architecture
Milestone: 0.4 — Governance Model
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture
Supersedes: None
Superseded By: None
Related: ADR-series; RFC-series

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and governance rules are interpreted within TB-0003.

Where conflicts arise between governance decisions, documents, standards, specifications, workflows, agents, implementations, or future revisions, the constitutional foundation SHALL guide interpretation and resolution.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Governance refers to the rules, processes, authority boundaries, review expectations, and decision records used to change, approve, supersede, or reject parts of The Brain Standard.
- Constitutional Document refers to a highest-authority TB-series document that defines foundational purpose, principles, architecture, governance, or other system-wide rules.
- Standard refers to a governed document that defines required or recommended behavior for a major architectural area of The Brain Standard.
- Specification refers to a lower-level document that defines exact structures, schemas, formats, fields, validation rules, or technical requirements.
- Implementation Document refers to a document describing how a specific tool, vault, database, workflow environment, file system, agent system, or interface realizes The Brain Standard.
- Operational Document refers to a guide, procedure, checklist, workflow instruction, or usage document that supports practical use without defining the standard itself.
- ADR or Architecture Decision Record refers to a document that records a significant architectural decision, its context, rationale, consequences, and status.
- RFC or Request for Comment refers to a proposed change, extension, or decision submitted for review before approval.
- Document Lifecycle State refers to the current governance status of a document, such as Draft, Review, Approved, Superseded, Deprecated, or Rejected.
- Supersession refers to the process by which one document, rule, decision, or version replaces another.
- Approval refers to the formal acceptance of a document, rule, revision, decision, or change into the governed standard.
- Compatibility refers to whether a change preserves the meaning, usability, portability, and interpretation of existing knowledge and documents.
- Governance Drift refers to the uncontrolled evolution of the standard through habit, tool behavior, undocumented decisions, implementation defaults, or informal practice.
- Revision refers to a change made to a document, rule, decision, specification, workflow, implementation expectation, or governance process.
- Deprecation refers to the process by which a document, rule, feature, workflow, implementation pattern, or decision remains historically available but is no longer recommended for future use.

## 1. Purpose

The purpose of TB-0003 is to define the governance model for The Brain Standard.

TB-0000 establishes the vision and purpose of The Brain. TB-0001 establishes the architecture principles that guide future decisions. TB-0002 establishes the layered architecture that organizes the major responsibilities of the standard. TB-0003 defines how the standard changes over time.

The governance model exists to ensure that The Brain Standard evolves deliberately, transparently, and consistently rather than through accidental drift.

TB-0003 defines how documents, decisions, revisions, proposals, approvals, supersessions, and compatibility concerns are managed across The Brain Standard.

The governance model is required because The Brain is intended to preserve knowledge across long periods of technological change. A standard designed for long-term use must be able to evolve without losing architectural coherence, breaking existing knowledge, or allowing tools, agents, workflows, or habits to redefine the standard informally.

TB-0003 is responsible for defining:

- document authority levels;
- document lifecycle states;
- approval expectations;
- review expectations;
- versioning expectations;
- supersession rules;
- ADR usage;
- RFC usage;
- compatibility review;
- governance boundaries;
- rules for changing constitutional documents;
- rules for changing standards, specifications, implementation documents, and operational documents;
- prevention of governance drift.

TB-0003 does not define the full content of every future document type. It defines how those documents are governed.

The primary purpose of the governance model is to preserve trust in The Brain Standard as it grows.

## 2. Relationship to TB-0000, TB-0001, and TB-0002

TB-0003 is subordinate to and derived from TB-0000, TB-0001, and TB-0002.

TB-0000 defines why The Brain exists. TB-0001 defines the architectural principles The Brain must follow. TB-0002 defines how the major architectural responsibilities of The Brain are organized. TB-0003 defines how those documents and all future governed documents may be changed, reviewed, approved, superseded, or rejected.

In practical terms:

- TB-0000 answers: Why does The Brain exist?
- TB-0001 answers: What principles must The Brain follow?
- TB-0002 answers: How are the major architectural responsibilities organized?
- TB-0003 answers: How does The Brain Standard change over time?
- Later standards answer: What rules govern each layer or domain?
- Specifications answer: What exact structures, schemas, and formats are required?
- Implementations answer: How can the standard be realized in software, files, databases, workflows, or interfaces?
- Operational documents answer: How should users or agents perform practical work within the standard?

TB-0003 must not contradict TB-0000, TB-0001, or TB-0002.

If a future governance process, document, implementation, workflow, agent, or operational practice conflicts with TB-0003, it must be revised, formally justified through a higher-authority process, or rejected.

If TB-0003 appears to conflict with TB-0000, TB-0001, or TB-0002, the higher-authority constitutional document takes precedence.

TB-0003 does not replace the authority hierarchy. It defines how that hierarchy is maintained, applied, and evolved.

## 3. Governance Principles

The governance model is guided by the following principles.

### 3.1 Governance Must Preserve the Standard

Governance exists to preserve The Brain Standard, not to create unnecessary bureaucracy.

A governance process is successful when it helps the standard remain durable, understandable, portable, reviewable, and trustworthy.

A governance process is unsuccessful when it makes routine improvement unnecessarily difficult, hides responsibility, or allows informal practice to become architecture without review.

### 3.2 Constitutional Stability Must Be Protected

Constitutional documents SHOULD remain stable.

Changes to constitutional documents affect the entire standard and SHOULD be made only when the change materially improves clarity, correctness, durability, portability, governance, or long-term architectural coherence.

A constitutional change SHOULD include documented rationale, compatibility review, impact review, and approval.

### 3.3 Lower-Authority Documents Must Not Override Higher-Authority Documents

Lower-authority documents MAY add detail, examples, schemas, workflows, procedures, implementation guidance, or operational instructions.

Lower-authority documents MUST NOT contradict or override higher-authority documents.

If a lower-authority document conflicts with a higher-authority document, the higher-authority document takes precedence unless the higher-authority document is formally revised or superseded.

### 3.4 Decisions Must Be Explicit

Significant architectural, governance, compatibility, or implementation decisions SHOULD be recorded.

Undocumented practice MUST NOT become part of The Brain Standard by accident.

A decision SHOULD be documented when it changes requirements, authority, compatibility, lifecycle behavior, privacy behavior, object meaning, storage expectations, agent boundaries, workflow behavior, implementation compliance, or governance process.

### 3.5 Change Must Be Reviewable

Changes to governed documents SHOULD be reviewable by a human.

A reviewable change should make clear:

- what changed;
- why it changed;
- what document or rule is affected;
- whether the change affects compatibility;
- whether the change affects authority;
- whether the change affects existing knowledge;
- whether the change requires an ADR, RFC, or version update.

### 3.6 Governance Must Support Practical Daily Use

The governance model MUST NOT make The Brain Standard too burdensome to use.

Not every typo, wording improvement, example, or clarification requires a full decision process.

Governance requirements SHOULD scale with the importance and risk of the change.

Minor editorial changes MAY follow a lighter process. Major architectural, compatibility, privacy, authority, lifecycle, or governance changes SHOULD require stronger review.

### 3.7 Governance Must Prevent Drift

Governance drift occurs when the standard changes informally through repeated habit, tool defaults, workflow convenience, agent behavior, or implementation-specific assumptions.

The governance model SHOULD make drift easier to detect and correct.

A practice is not part of The Brain Standard merely because it is repeated, automated, convenient, or implemented in a tool.

A practice becomes part of The Brain Standard only when it is documented, reviewed, and approved at the appropriate authority level.

## 4. Document Authority Levels

The Brain Standard uses document authority levels to determine how documents relate to one another and how conflicts are resolved.

Authority levels exist to prevent lower-authority documents, implementations, workflows, agents, examples, or habits from redefining the standard by accident.

A document authority level defines:

- what type of rule the document may establish;
- what lower-authority documents it may govern;
- what higher-authority documents it must obey;
- whether it may define requirements, recommendations, examples, proposals, or operational guidance;
- how conflicts involving that document should be resolved.

The authority hierarchy of The Brain Standard is:

| Level                     | Prefix         | Authority            |
| ------------------------- | -------------- | -------------------- |
| Constitutional            | TB             | Highest              |
| Standards                 | KS, SS, AG, WF | High                 |
| Specifications            | SC             | Medium               |
| ADRs                      | ADR            | Historical Decisions |
| RFCs                      | RFC            | Proposed Changes     |
| Reference Implementations | IM             | Examples             |
| Operational Documents     | SOP, Guide     | Lowest               |

Lower-authority documents MAY add detail, examples, procedures, schemas, workflows, implementation guidance, or operational instructions.

Lower-authority documents MUST NOT contradict higher-authority documents.

If a lower-authority document appears to conflict with a higher-authority document, the higher-authority document SHALL take precedence unless it is formally revised, superseded, or deprecated through governance.

### 4.1 Constitutional Documents

Constitutional documents are the highest-authority documents within The Brain Standard.

Constitutional documents use the `TB` prefix.

Constitutional documents define foundational purpose, principles, architecture, governance, authority, and other system-wide rules.

At minimum, constitutional documents include:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- future approved TB-series constitutional documents.

Constitutional documents govern all lower-authority documents.

A constitutional document MAY define:

- mission and vision;
- architectural principles;
- document authority hierarchy;
- layered architecture;
- governance rules;
- compatibility expectations;
- document lifecycle rules;
- standard-wide constraints;
- approval expectations;
- supersession rules;
- interpretation rules.

A constitutional document SHOULD remain stable.

A constitutional document SHOULD be changed only when the change materially improves clarity, correctness, governance, durability, portability, compatibility, or long-term architectural coherence.

A change to a constitutional document SHOULD include documented rationale, compatibility review, impact review, and approval.

### 4.2 Standards

Standards define required or recommended behavior for major architectural areas of The Brain Standard.

Standards have high authority but remain subordinate to constitutional documents.

Standards MAY define rules for operational layers, knowledge structure, storage behavior, agent behavior, workflow behavior, implementation compliance, privacy expectations, validation behavior, or interoperability.

The recommended standard prefixes are:

- `KS` for Knowledge Standards;
- `SS` for Storage Standards;
- `AG` for Agent Standards;
- `WF` for Workflow Standards.

A standard MAY define:

- mandatory requirements;
- recommended practices;
- allowed behaviors;
- prohibited behaviors;
- compliance expectations;
- validation expectations;
- lifecycle behavior;
- privacy behavior;
- interoperability requirements;
- compatibility expectations.

A standard MUST NOT contradict constitutional documents.

If a standard appears to conflict with a constitutional document, the constitutional document SHALL take precedence unless the constitutional document is formally revised.

### 4.3 Specifications

Specifications define exact structures, schemas, formats, fields, validation rules, or technical requirements.

Specifications use the `SC` prefix unless a future governed document defines more specific specification prefixes.

Specifications have medium authority.

A specification is valid only when it conforms to the constitutional documents and the relevant standards.

A specification MAY define:

- metadata fields;
- schema structures;
- file formats;
- naming formats;
- validation rules;
- object templates;
- relationship formats;
- lifecycle state values;
- privacy classification values;
- import and export formats;
- compatibility constraints.

Specifications SHOULD be precise enough that humans, agents, validators, and implementations can apply them consistently.

Specifications MUST NOT create new architectural principles, authority levels, operational layers, or governance rules unless those changes are approved at the appropriate higher authority level.

### 4.4 Architecture Decision Records

Architecture Decision Records record significant architectural decisions.

ADRs use the `ADR` prefix.

An ADR preserves the context, decision, rationale, consequences, and status of an architectural choice.

An ADR may explain why a decision was made, what alternatives were considered, what trade-offs were accepted, and what future documents may need to follow.

An ADR MAY record:

- a major design choice;
- a rejected alternative;
- an architectural trade-off;
- a compatibility decision;
- a governance decision;
- an implementation-independent rule that requires historical explanation;
- a decision that affects future standards, specifications, workflows, agents, or implementations.

An ADR records a decision; it does not automatically override constitutional documents or standards.

If an ADR conflicts with a higher-authority document, the higher-authority document SHALL take precedence unless the higher-authority document is formally revised.

An approved ADR may guide future work, but permanent requirements SHOULD be incorporated into the appropriate constitutional document, standard, or specification when necessary.

### 4.5 Requests for Comment

Requests for Comment are proposed changes or extensions submitted for review.

RFCs use the `RFC` prefix.

An RFC is not an approved change unless it is accepted through the appropriate governance process.

An RFC MAY propose:

- a new document;
- a revision to an existing document;
- a new standard;
- a new specification;
- a new workflow;
- a new object type;
- a new metadata field;
- a compatibility change;
- a deprecation;
- a supersession;
- an implementation profile;
- a governance change.

An RFC SHOULD include enough context, rationale, impact analysis, compatibility analysis, and proposed text for meaningful review.

An RFC may be accepted, revised, deferred, rejected, or superseded.

Accepted RFCs SHOULD result in updates to the appropriate governed documents.

Rejected RFCs MAY remain available as historical records.

### 4.6 Reference Implementations

Reference implementations demonstrate one way to realize The Brain Standard in practice.

Reference implementation documents use the `IM` prefix.

A reference implementation MAY define:

- example folder structures;
- example file layouts;
- example workflows;
- example validation tools;
- example agent configurations;
- example import and export processes;
- example user interfaces;
- example storage approaches;
- example implementation profiles.

Reference implementations are examples, not standards.

A reference implementation MUST NOT become required for The Brain Standard to remain valid.

A reference implementation MAY show a recommended pattern, but it MUST NOT override constitutional documents, standards, or specifications.

If a reference implementation reveals a gap in the standard, the gap SHOULD be addressed through an ADR, RFC, standard, specification, or constitutional revision rather than through implementation behavior alone.

### 4.7 Operational Documents

Operational documents support practical use of The Brain Standard.

Operational documents may include guides, checklists, procedures, standard operating procedures, onboarding notes, maintenance instructions, workflow instructions, and user-facing documentation.

Operational documents may use prefixes such as `SOP` or `Guide`.

Operational documents have the lowest authority.

An operational document MAY explain:

- how to perform a task;
- how to use a tool;
- how to follow a workflow;
- how to review a document;
- how to apply a checklist;
- how to maintain a vault;
- how to prepare a proposal;
- how to use a reference implementation.

Operational documents MUST NOT define architectural requirements unless those requirements already exist in a higher-authority document.

If an operational document conflicts with a higher-authority document, the higher-authority document SHALL take precedence.

Operational documents SHOULD be easy to revise because they support daily use and may need to change more often than constitutional documents, standards, or specifications.

### 4.8 Authority Conflict Resolution

When documents conflict, the following authority order SHALL guide resolution:

1. Constitutional documents
2. Standards
3. Specifications
4. ADRs
5. RFCs
6. Reference implementations
7. Operational documents

A lower-authority document MAY clarify or apply a higher-authority document, but it MUST NOT contradict it.

A conflict SHOULD be resolved through the following process:

1. identify the conflicting documents;
2. identify the authority level of each document;
3. determine whether the conflict is real or only interpretive;
4. apply the higher-authority document;
5. revise the lower-authority document if needed;
6. record the decision through an ADR, RFC, revision, or supersession when appropriate.

If the higher-authority document is unclear, incomplete, or outdated, the issue SHOULD be handled through governance rather than bypassed through implementation behavior, workflow convenience, agent output, or informal practice.

## 5. Document Lifecycle States

Document lifecycle states define the governance status of a document within The Brain Standard.

A lifecycle state helps humans, agents, workflows, and implementations understand whether a document is proposed, under review, approved, historically preserved, discouraged for future use, replaced, or rejected.

Every governed document SHOULD have a clear lifecycle state.

At minimum, The Brain Standard recognizes the following document lifecycle states:

- Draft;
- Review;
- Approved;
- Deprecated;
- Superseded;
- Rejected.

A document lifecycle state SHOULD be shown in the document metadata using the `Status` field.

Example:

```text
Status: Draft
```

A lifecycle state does not replace document authority.

For example, an approved operational guide remains lower authority than an approved constitutional document. A draft constitutional document may propose high-authority changes, but it does not become authoritative until approved.

Lifecycle state defines approval status.

Authority level defines governance weight.

Both are required to interpret a document correctly.

### 5.1 Draft

Draft means a document is being created, revised, or prepared.

A Draft document is not approved.

A Draft document MAY propose new rules, changes, examples, workflows, specifications, governance structures, implementation patterns, or operational guidance.

A Draft document MUST NOT be treated as authoritative unless an approved higher-authority document explicitly says otherwise.

Draft documents SHOULD be clearly marked with:

```text
Status: Draft
```

A Draft document MAY be incomplete.

A Draft document MAY contain unresolved questions, proposed language, alternatives, notes, or placeholders.

Draft documents SHOULD be reviewed before approval.

### 5.2 Review

Review means a document is ready for evaluation but has not yet been approved.

A Review document SHOULD be complete enough for meaningful assessment.

A Review document SHOULD be checked for:

- constitutional alignment;
- authority consistency;
- layer placement;
- compatibility impact;
- privacy impact;
- implementation impact;
- workflow impact;
- agent impact;
- clarity;
- completeness;
- syntax and formatting quality;
- contradiction with higher-authority documents.

A Review document MAY still change before approval.

A Review document MUST NOT be treated as approved unless formally accepted through governance.

Review documents SHOULD be clearly marked with:

```text
Status: Review
```

### 5.3 Approved

Approved means a document has been accepted into The Brain Standard at its stated authority level.

An Approved document is authoritative within the scope defined by its document type, authority level, and content.

Approved documents SHOULD be clearly marked with:

```text
Status: Approved
```

An Approved document SHOULD include a `Last Updated` date.

An Approved document SHOULD be stable enough for future documents, workflows, agents, and implementations to depend on.

Approval does not mean the document can never change.

An Approved document MAY be revised, deprecated, or superseded through governance.

Approved documents MUST NOT be silently modified in ways that change meaning, authority, compatibility, privacy behavior, lifecycle behavior, or governance expectations.

Material changes to Approved documents SHOULD follow the revision, review, and approval expectations defined by this governance model.

### 5.4 Deprecated

Deprecated means a document, rule, feature, workflow, implementation pattern, or decision remains historically available but is no longer recommended for future use.

A Deprecated document may still be valid for understanding historical decisions, existing implementations, or older knowledge structures.

Deprecation is appropriate when:

- a better replacement exists but migration may take time;
- the old document or rule remains historically important;
- existing implementations still depend on the older approach;
- immediate supersession would create unnecessary disruption;
- the old approach is discouraged but not invalid for all historical use.

Deprecated documents SHOULD be clearly marked with:

```text
Status: Deprecated
```

A Deprecated document SHOULD identify the reason for deprecation where practical.

A Deprecated document SHOULD identify a replacement, migration path, or future review path when one exists.

Deprecated documents SHOULD NOT be used as the basis for new standards, specifications, workflows, agents, or implementations unless explicitly justified.

### 5.5 Superseded

Superseded means a document, rule, decision, version, or requirement has been replaced by another governed document or decision.

A Superseded document remains historically available but is no longer the active authority for future work.

Superseded documents SHOULD be clearly marked with:

```text
Status: Superseded
```

A Superseded document SHOULD identify the document or version that supersedes it using the `Superseded By` metadata field.

Example:

```text
Superseded By: TB-0003 v0.2.0
```

A document that supersedes another document SHOULD identify what it supersedes using the `Supersedes` metadata field.

Example:

```text
Supersedes: TB-0003 v0.1.0
```

Supersession SHOULD preserve traceability.

A user, agent, workflow, or implementation should be able to determine:

- what document was replaced;
- what document replaced it;
- why it was replaced;
- whether compatibility is affected;
- whether migration is required;
- whether older knowledge remains valid.

Superseded documents MUST NOT be treated as the active authority when a current approved replacement exists.

### 5.6 Rejected

Rejected means a document, proposal, RFC, ADR candidate, specification, workflow, implementation pattern, or change request was reviewed and not accepted.

Rejected documents MAY remain available as historical records.

Rejected documents SHOULD be clearly marked with:

```text
Status: Rejected
```

A Rejected document SHOULD identify the reason for rejection where practical.

A Rejected document SHOULD NOT be treated as authoritative.

A Rejected document MAY be reconsidered later if new context, requirements, evidence, or architectural constraints justify review.

If a rejected proposal is reconsidered, the new proposal SHOULD reference the prior rejection and explain what has changed.

### 5.7 Lifecycle State Changes

A document lifecycle state MAY change through governance.

Common lifecycle transitions include:

- Draft to Review;
- Review to Approved;
- Review to Rejected;
- Approved to Deprecated;
- Approved to Superseded;
- Deprecated to Superseded;
- Rejected to Draft if reconsidered;
- Draft to Rejected if abandoned.

Lifecycle transitions SHOULD be traceable when the change affects authority, compatibility, implementation behavior, privacy, lifecycle behavior, or governance.

A lifecycle state change SHOULD update the document metadata.

At minimum, a lifecycle update SHOULD review:

- `Status`;
- `Last Updated`;
- `Supersedes`;
- `Superseded By`;
- related ADRs or RFCs;
- compatibility notes where applicable.

Lifecycle state changes MUST NOT be used to bypass authority rules.

A lower-authority document cannot become higher authority merely by being marked Approved.

A document becomes authoritative only within its correct document authority level.

## 6. Versioning Expectations

Versioning expectations define how governed documents indicate change over time.

Versioning exists to help humans, agents, workflows, validators, and implementations understand whether a document has changed, how significant the change is, and whether compatibility review may be required.

Every governed document SHOULD include a version in its metadata.

Example:

```text
Version: 0.1.0
```

The Brain Standard SHOULD use a simple three-part version format:

```text
Major.Minor.Patch
```

Example:

```text
Version: 1.2.3
```

The version number SHOULD communicate the significance of the change.

Versioning does not replace document status.

For example, a document may be:

```text
Version: 0.1.0
Status: Draft
```

or:

```text
Version: 1.0.0
Status: Approved
```

Version indicates revision history.

Status indicates lifecycle state.

Authority indicates governance weight.

All three should be interpreted together.

### 6.1 Draft Versioning

Draft documents SHOULD normally begin at version `0.1.0`.

Example:

```text
Version: 0.1.0
Status: Draft
```

Draft versions MAY change frequently while a document is being written, reviewed, or reorganized.

A Draft document MAY remain at the same version while text is being actively developed before approval.

Minor draft updates do not require a new version unless version tracking is useful for review.

A Draft document SHOULD receive clearer version tracking when it is circulated for review, used by workflows, referenced by other documents, or used as the basis for implementation work.

### 6.2 Approved Versioning

An Approved document SHOULD have a stable version number.

The first approved version of a constitutional document, standard, specification, implementation document, or operational document SHOULD normally be marked as:

```text
Version: 1.0.0
Status: Approved
```

However, early Phase 0 documents MAY remain at `0.x.x` while the architecture is still being established, provided the document status clearly indicates whether it is Draft, Review, or Approved.

An Approved document MUST NOT be materially changed without considering whether the version number should be updated.

Material changes include changes that affect:

- meaning;
- authority;
- compatibility;
- governance;
- lifecycle behavior;
- privacy behavior;
- object identity;
- storage expectations;
- agent boundaries;
- workflow behavior;
- implementation compliance;
- validation expectations.

### 6.3 Patch Versions

A patch version update changes the third number.

Example:

```text
Version: 1.0.1
```

Patch versions SHOULD be used for minor corrections that do not change the meaning of the document.

Patch-level changes MAY include:

- typo fixes;
- grammar fixes;
- formatting cleanup;
- broken link correction;
- wording clarification that does not change requirements;
- table formatting cleanup;
- metadata cleanup that does not affect authority or lifecycle state.

Patch changes SHOULD NOT alter architectural meaning, requirements, compatibility, privacy behavior, authority, or governance rules.

### 6.4 Minor Versions

A minor version update changes the second number.

Example:

```text
Version: 1.1.0
```

Minor versions SHOULD be used for meaningful additions or clarifications that remain backward-compatible.

Minor-level changes MAY include:

- adding a new subsection;
- clarifying an existing rule;
- adding examples;
- adding review criteria;
- adding recommended practices;
- adding lifecycle guidance;
- adding compatibility guidance;
- adding governance guidance that does not contradict prior approved rules.

Minor changes SHOULD preserve compatibility with existing approved documents and existing knowledge unless a higher-authority governance decision explicitly allows otherwise.

A minor version update SHOULD include review when it affects standards, specifications, workflows, agents, implementations, privacy behavior, or governance expectations.

### 6.5 Major Versions

A major version update changes the first number.

Example:

```text
Version: 2.0.0
```

Major versions SHOULD be used for changes that alter meaning, compatibility, authority, governance rules, lifecycle behavior, or required interpretation.

Major-level changes MAY include:

- changing a required rule;
- removing a required rule;
- changing document authority behavior;
- changing lifecycle state behavior;
- changing compatibility expectations;
- changing privacy requirements;
- changing object identity expectations;
- changing layer responsibilities;
- changing approval requirements;
- superseding a prior approved document;
- introducing breaking changes.

Major changes SHOULD include documented rationale, compatibility review, impact review, and approval.

Major changes MAY require an ADR, RFC, migration guidance, supersession notice, or constitutional review depending on the authority level of the affected document.

### 6.6 Version Reset Rules

When a higher version level changes, lower version numbers SHOULD reset to zero.

Examples:

```text
1.0.1 → 1.1.0
1.2.3 → 2.0.0
```

A minor version change SHOULD reset the patch number to zero.

A major version change SHOULD reset the minor and patch numbers to zero.

This keeps version numbers readable and predictable.

### 6.7 Versioning and Supersession

A new version may revise, deprecate, or supersede an earlier version.

When a document version supersedes an earlier version, the metadata SHOULD preserve traceability.

Example:

```text
Version: 2.0.0
Supersedes: TB-0003 v1.0.0
Superseded By: None
```

The older document version SHOULD identify the replacement where practical.

Example:

```text
Version: 1.0.0
Status: Superseded
Superseded By: TB-0003 v2.0.0
```

Supersession SHOULD make clear whether older knowledge, workflows, implementations, or references remain valid.

### 6.8 Versioning and Compatibility

Version changes SHOULD be reviewed for compatibility impact.

A compatibility review SHOULD consider whether the change affects:

- existing approved documents;
- existing Knowledge Objects;
- existing Knowledge Records;
- metadata interpretation;
- source references;
- storage organization;
- agent permissions;
- workflow behavior;
- validation behavior;
- privacy classifications;
- implementation compliance;
- migration expectations;
- human and AI readability.

Patch versions usually SHOULD NOT require compatibility review unless the patch affects meaning.

Minor versions SHOULD receive compatibility review when they add or clarify governed behavior.

Major versions SHOULD receive compatibility review before approval.

### 6.9 Versioning Discipline

Versioning SHOULD remain practical.

The Brain Standard should not require excessive version updates for every small editorial change during drafting.

However, once a document is Approved, versioning discipline becomes more important.

Approved documents SHOULD preserve a clear history of meaningful changes.

Version numbers SHOULD NOT be used to hide breaking changes.

Breaking changes SHOULD be documented, reviewed, and approved at the appropriate authority level.

A document’s version history should help future humans and AI systems understand how the standard evolved.

## 7. Approval and Review Expectations

Approval and review expectations define how documents, revisions, proposals, decisions, standards, specifications, workflows, agents, implementations, and operational guidance are evaluated before becoming part of The Brain Standard.

Review exists to preserve architectural integrity, compatibility, privacy, reviewability, implementation independence, and practical daily use.

Approval exists to formally accept a document, decision, revision, or change at the appropriate authority level.

A document or change SHOULD be reviewed before approval when it affects:

- constitutional meaning;
- architectural principles;
- document authority;
- operational layer responsibility;
- knowledge meaning;
- object identity;
- metadata requirements;
- source material handling;
- storage expectations;
- agent permissions;
- workflow behavior;
- privacy boundaries;
- lifecycle behavior;
- versioning behavior;
- compatibility;
- implementation compliance;
- governance process.

Not every change requires the same level of review.

Review depth SHOULD scale with the authority level, risk, scope, and long-term impact of the proposed change.

Minor editorial changes MAY receive lightweight review.

Major architectural, compatibility, privacy, authority, lifecycle, implementation, or governance changes SHOULD receive stronger review before approval.

### 7.1 Review Scope

A review SHOULD identify what the proposed document or change affects.

At minimum, a review SHOULD consider whether the change affects:

- constitutional documents;
- standards;
- specifications;
- ADRs;
- RFCs;
- reference implementations;
- operational documents;
- Knowledge Objects;
- Knowledge Records;
- source material;
- storage structures;
- agents;
- workflows;
- implementations;
- validation;
- privacy;
- compatibility;
- migration;
- governance.

A proposal with narrow scope MAY require limited review.

A proposal with broad or cross-layer scope SHOULD receive broader review.

### 7.2 Constitutional Review

A constitutional review applies to TB-series documents and changes that affect the foundation of The Brain Standard.

Constitutional review SHOULD be used when a proposal affects:

- mission;
- vision;
- scope;
- architectural principles;
- document authority hierarchy;
- layered architecture;
- governance rules;
- constitutional interpretation;
- compatibility expectations;
- approval rules;
- supersession rules;
- standard-wide constraints.

A constitutional change SHOULD include:

- documented rationale;
- compatibility review;
- impact review;
- authority review;
- privacy review where applicable;
- migration guidance where applicable;
- approval at the constitutional authority level.

Constitutional changes SHOULD be rare compared with changes to standards, specifications, implementation documents, or operational documents.

### 7.3 Standards Review

A standards review applies to documents that define required or recommended behavior for major architectural areas.

Standards review SHOULD be used when a proposal affects:

- Knowledge Standards;
- Storage Standards;
- Agent Standards;
- Workflow Standards;
- implementation compliance expectations;
- validation expectations;
- interoperability requirements;
- privacy expectations;
- lifecycle behavior;
- compatibility expectations.

A standard MUST conform to constitutional documents.

A standard SHOULD identify:

- the operational layer or architectural area it governs;
- the constitutional documents it depends on;
- the requirements it defines;
- the recommendations it defines;
- the behaviors it allows;
- the behaviors it prohibits;
- the compatibility expectations it creates;
- the documents or implementations likely to be affected.

A standard SHOULD be reviewed for clarity, necessity, compatibility, portability, implementation independence, privacy, reviewability, and practical usability.

### 7.4 Specification Review

A specification review applies to documents that define exact structures, schemas, formats, fields, validation rules, or technical requirements.

Specification review SHOULD be used when a proposal affects:

- metadata fields;
- object templates;
- schemas;
- file formats;
- naming formats;
- relationship structures;
- lifecycle values;
- privacy classification values;
- validation rules;
- import formats;
- export formats;
- compatibility constraints.

A specification MUST conform to constitutional documents and relevant standards.

A specification SHOULD be reviewed for:

- precision;
- consistency;
- validation feasibility;
- human readability;
- AI readability;
- compatibility;
- migration impact;
- implementation independence;
- risk of hidden dependencies;
- risk of over-specification.

Specifications SHOULD be exact enough to implement and validate, but not so rigid that they create unnecessary implementation lock-in.

### 7.5 ADR Review

An ADR review applies to Architecture Decision Records.

ADR review SHOULD be used when a decision affects architecture, compatibility, governance, implementation independence, privacy, lifecycle behavior, workflow behavior, agent behavior, or long-term maintainability.

An ADR SHOULD identify:

- the context of the decision;
- the decision made;
- alternatives considered;
- rationale;
- consequences;
- affected documents;
- affected layers;
- compatibility impact;
- whether future document updates are required.

An ADR may record a decision, but it MUST NOT override a higher-authority document.

If an ADR reveals that a constitutional document, standard, or specification must change, that change SHOULD be made in the appropriate governed document rather than only in the ADR.

### 7.6 RFC Review

An RFC review applies to proposed changes before they are accepted, rejected, deferred, revised, or superseded.

RFC review SHOULD be used when a proposed change is significant enough to require discussion before approval.

An RFC SHOULD identify:

- the problem or opportunity;
- the proposed change;
- the affected authority level;
- the affected documents;
- the affected layers;
- the expected benefits;
- the expected risks;
- compatibility impact;
- privacy impact where applicable;
- migration impact where applicable;
- alternatives considered;
- proposed approval path.

An RFC is not authoritative unless accepted through governance.

If accepted, an RFC SHOULD result in updates to the appropriate constitutional document, standard, specification, ADR, implementation document, or operational document.

### 7.7 Implementation Review

An implementation review applies to reference implementations, implementation profiles, tools, vault structures, databases, file systems, interfaces, validators, agents, scripts, or workflow environments that claim alignment with The Brain Standard.

An implementation review SHOULD determine whether the implementation preserves:

- knowledge meaning;
- object identity;
- source material distinction;
- metadata meaning;
- relationship meaning;
- privacy boundaries;
- reviewability;
- portability;
- implementation replaceability;
- validation expectations;
- governance boundaries.

An implementation MAY use specific tools, databases, AI models, scripts, folder structures, interfaces, or services.

However, implementation-specific behavior MUST NOT redefine the standard.

A reference implementation SHOULD clearly distinguish standard behavior from example behavior.

### 7.8 Operational Review

An operational review applies to guides, procedures, checklists, workflow instructions, onboarding documents, maintenance instructions, and other daily-use documents.

Operational review SHOULD determine whether the document:

- aligns with higher-authority documents;
- avoids defining new architectural requirements;
- accurately reflects approved standards and specifications;
- supports practical daily use;
- avoids unnecessary complexity;
- preserves privacy and reviewability;
- avoids encouraging governance bypass;
- remains easy to update when higher-authority documents change.

Operational documents MAY be reviewed more lightly than constitutional documents, standards, or specifications.

Operational documents SHOULD remain practical, clear, and easy to revise.

### 7.9 Approval Expectations

Approval means that a document, revision, decision, or change has been accepted at the appropriate authority level.

Approval SHOULD be explicit.

An approved document SHOULD include:

- `Status: Approved`;
- a version;
- a `Last Updated` date;
- dependencies where applicable;
- supersession metadata where applicable;
- related ADRs or RFCs where applicable.

Approval SHOULD confirm that the approved item:

- aligns with higher-authority documents;
- has the correct authority level;
- has the correct lifecycle state;
- uses appropriate normative language;
- avoids known anti-patterns;
- preserves compatibility or documents compatibility impact;
- preserves privacy and reviewability;
- remains practical for daily use.

Approval MUST NOT be implied merely because a document exists, is used, is copied, is implemented, or is referenced by an agent, workflow, or tool.

### 7.10 Review Checklist

Before approval, a governed document or material change SHOULD be reviewed against the following questions:

- Does it align with TB-0000, TB-0001, TB-0002, and TB-0003?
- Does it have the correct authority level?
- Does it have the correct lifecycle state?
- Does it preserve implementation independence?
- Does it preserve knowledge meaning?
- Does it preserve privacy boundaries?
- Does it preserve human reviewability?
- Does it preserve compatibility or document compatibility impact?
- Does it avoid hidden dependencies?
- Does it avoid allowing implementation behavior to define the standard?
- Does it avoid allowing agent or workflow behavior to become unreviewable authority?
- Does it require an ADR?
- Does it require an RFC?
- Does it require migration guidance?
- Does it update version metadata correctly?
- Does it update supersession metadata correctly where applicable?
- Is the change practical for daily use?

A proposal does not need to satisfy every question in the same way.

The purpose of the checklist is to identify risk, clarify review needs, and prevent accidental governance drift.

### 7.11 Approval Record

A significant approval SHOULD leave enough record for future humans and AI systems to understand what was approved and why.

An approval record MAY be captured through:

- document metadata;
- an ADR;
- an accepted RFC;
- a changelog;
- a review note;
- a supersession note;
- a version history entry;
- a governance log.

The approval record SHOULD be proportional to the importance of the decision.

Minor editorial approval may require only updated metadata.

Major constitutional, standards, specification, compatibility, privacy, lifecycle, or governance approvals SHOULD include stronger documentation.

An approval record SHOULD make clear:

- what was approved;
- when it was approved;
- what version was approved;
- what authority level applies;
- what documents were affected;
- what compatibility impact exists;
- whether future review is required.

## 8. ADR Usage

Architecture Decision Records preserve significant architectural decisions made during the evolution of The Brain Standard.

ADRs exist to make important decisions traceable, reviewable, and understandable over time.

An ADR records why a decision was made, what alternatives were considered, what trade-offs were accepted, and what consequences follow from the decision.

ADRs are historical decision records.

They do not replace constitutional documents, standards, or specifications.

An ADR MAY guide future work, but permanent requirements SHOULD be incorporated into the appropriate governed document when necessary.

### 8.1 Purpose of ADRs

The purpose of an ADR is to preserve decision context.

An ADR SHOULD explain:

- what decision was made;
- why the decision was needed;
- what problem or opportunity caused the decision;
- what alternatives were considered;
- why the chosen option was selected;
- what trade-offs were accepted;
- what consequences follow;
- what documents, layers, workflows, agents, implementations, or future work may be affected.

ADRs help prevent architectural knowledge from being lost.

Without ADRs, future users, agents, and maintainers may see the current rule but not understand the reasoning behind it.

### 8.2 When an ADR Should Be Created

An ADR SHOULD be created when a decision materially affects architecture, governance, compatibility, implementation independence, privacy, reviewability, workflow behavior, agent behavior, or long-term maintainability.

An ADR SHOULD be considered when a decision:

- introduces a significant architectural rule;
- rejects a plausible alternative;
- resolves an architectural trade-off;
- affects compatibility;
- affects document authority;
- affects governance behavior;
- affects layer boundaries;
- affects knowledge meaning;
- affects object identity;
- affects storage expectations;
- affects agent permissions or boundaries;
- affects workflow behavior;
- affects implementation compliance;
- affects privacy or reviewability;
- creates a precedent future documents may rely on.

An ADR is not required for every small edit, clarification, typo fix, or formatting cleanup.

ADR usage SHOULD remain practical.

### 8.3 ADR Authority

An ADR records a decision.

An ADR does not automatically override higher-authority documents.

If an ADR conflicts with a constitutional document, standard, or specification, the higher-authority document SHALL take precedence unless that higher-authority document is formally revised through governance.

An ADR MAY explain why a higher-authority document should be revised.

An ADR MAY recommend future changes to constitutional documents, standards, specifications, workflows, agents, implementations, or operational documents.

However, the recommended changes become authoritative only when incorporated into the appropriate governed document and approved at the correct authority level.

### 8.4 ADR Status

Each ADR SHOULD have a clear status.

Recommended ADR statuses include:

- Proposed;
- Accepted;
- Rejected;
- Deprecated;
- Superseded.

A Proposed ADR records a decision under consideration.

An Accepted ADR records a decision that has been approved.

A Rejected ADR records a decision that was considered but not accepted.

A Deprecated ADR records a decision that remains historically available but is no longer recommended for future use.

A Superseded ADR records a decision that has been replaced by a later ADR or governed document.

ADR status SHOULD be shown in ADR metadata.

Example:

```text
Status: Accepted
```

### 8.5 ADR Content Expectations

An ADR SHOULD include enough information for future humans and AI systems to understand the decision.

At minimum, an ADR SHOULD identify:

- title;
- status;
- date;
- context;
- decision;
- rationale;
- alternatives considered;
- consequences;
- affected documents;
- affected layers;
- compatibility impact;
- related ADRs or RFCs where applicable.

An ADR MAY also include:

- implementation notes;
- migration notes;
- open questions;
- review notes;
- supersession notes;
- links to affected standards or specifications.

ADR content SHOULD be concise but complete enough to preserve the reasoning behind the decision.

### 8.6 ADR Relationship to RFCs

An RFC proposes a change before approval.

An ADR records a decision after or during decision-making.

An RFC may lead to an ADR when the decision is significant enough to preserve historically.

An ADR may refer to an RFC when the RFC provided the proposal, discussion, or rationale for the decision.

Accepted RFCs SHOULD result in updates to the appropriate governed documents.

Accepted RFCs MAY also result in ADRs when the decision affects architecture, compatibility, governance, privacy, lifecycle behavior, implementation independence, or long-term maintainability.

Rejected RFCs MAY also result in ADRs if the rejection establishes an important architectural precedent.

### 8.7 ADR Relationship to Standards and Specifications

Standards and specifications define current governed requirements.

ADRs explain important decisions behind those requirements.

An ADR SHOULD NOT be the only place where an active requirement is defined if that requirement affects standard behavior.

If an ADR establishes a rule that should govern future documents, workflows, agents, implementations, or validation behavior, the rule SHOULD be incorporated into the appropriate constitutional document, standard, or specification.

An ADR MAY remain as the historical explanation for why the rule exists.

### 8.8 ADR Numbering and Naming

ADRs SHOULD use a predictable identifier.

Recommended ADR naming format:

```text
ADR-0001 — Short Decision Title
```

ADR numbers SHOULD be stable once assigned.

ADR titles SHOULD be short, descriptive, and human-readable.

An ADR filename SHOULD preserve the ADR identifier and title where practical.

Example:

```text
ADR-0001 — Use Markdown as Primary Human-Readable Format.md
```

ADR identifiers SHOULD NOT be reused for different decisions.

If an ADR is superseded or rejected, its identifier SHOULD remain historically reserved.

### 8.9 ADR Supersession

An ADR MAY be superseded by a later ADR or by a governed document.

A superseded ADR SHOULD identify what supersedes it.

Example:

```text
Superseded By: ADR-0007 — Revised Storage Portability Decision
```

A later ADR that supersedes an earlier ADR SHOULD identify what it supersedes.

Example:

```text
Supersedes: ADR-0002 — Original Storage Portability Decision
```

ADR supersession SHOULD preserve traceability.

A future reader should be able to determine:

- what decision was replaced;
- what decision replaced it;
- why the decision changed;
- whether compatibility is affected;
- whether a standard or specification was updated.

### 8.10 ADR Review Expectations

An ADR SHOULD be reviewed before being accepted.

ADR review SHOULD consider:

- whether the decision is clearly stated;
- whether the context is sufficient;
- whether alternatives were considered;
- whether the rationale is understandable;
- whether consequences are documented;
- whether affected documents are identified;
- whether compatibility impact is identified;
- whether the ADR conflicts with higher-authority documents;
- whether the decision should instead be handled through an RFC, standard, specification, or constitutional revision.

An ADR SHOULD NOT be accepted if it silently contradicts a higher-authority document.

### 8.11 ADR Practicality

ADR usage SHOULD remain practical.

The Brain Standard should avoid creating ADRs for every minor wording change, typo correction, formatting cleanup, or routine operational adjustment.

ADRs are most useful when they preserve meaningful architectural reasoning.

A useful ADR should reduce future confusion.

An ADR that adds process burden without preserving meaningful decision context should be avoided.

## 9. RFC Usage

Requests for Comment preserve proposed changes, extensions, revisions, and governance questions before they are accepted, rejected, deferred, revised, or superseded.

RFCs exist to make proposed changes reviewable before they become part of The Brain Standard.

An RFC is a proposal.

It is not authoritative unless accepted through the appropriate governance process.

An RFC MAY lead to changes in constitutional documents, standards, specifications, ADRs, implementation documents, reference implementations, operational documents, workflows, agents, validation rules, or governance processes.

### 9.1 Purpose of RFCs

The purpose of an RFC is to create a reviewable proposal before a significant change is approved.

An RFC SHOULD explain:

- what problem or opportunity exists;
- what change is proposed;
- why the change is needed;
- what documents or layers are affected;
- what benefits are expected;
- what risks may exist;
- what compatibility impact may occur;
- what privacy impact may occur;
- what migration impact may occur;
- what alternatives were considered;
- what approval path is recommended.

RFCs help prevent informal changes from becoming architecture without review.

RFCs also help future humans and AI systems understand why a proposed change was accepted, rejected, deferred, revised, or superseded.

### 9.2 When an RFC Should Be Created

An RFC SHOULD be created when a proposed change is significant enough to require review before approval.

An RFC SHOULD be considered when a proposal:

- creates a new constitutional document;
- revises a constitutional document;
- creates a new standard;
- revises an approved standard;
- creates a new specification;
- revises an approved specification;
- introduces a new Knowledge Object type;
- changes metadata expectations;
- changes lifecycle behavior;
- changes privacy behavior;
- changes storage expectations;
- changes agent permissions or boundaries;
- changes workflow behavior;
- changes implementation compliance expectations;
- changes validation behavior;
- changes governance behavior;
- creates compatibility or migration concerns;
- deprecates or supersedes an approved document, rule, workflow, or implementation pattern.

An RFC is not required for every minor typo fix, formatting cleanup, wording clarification, or small operational adjustment.

RFC usage SHOULD remain practical.

### 9.3 RFC Authority

An RFC has proposal authority, not approval authority.

An RFC may recommend a change, but it does not make that change authoritative by itself.

A proposed RFC change becomes authoritative only when accepted through governance and incorporated into the appropriate governed document.

If an RFC conflicts with an approved constitutional document, standard, or specification, the approved higher-authority document SHALL take precedence unless it is formally revised.

An RFC MAY propose revising a higher-authority document.

However, the revision is not active until approved at the correct authority level.

### 9.4 RFC Status

Each RFC SHOULD have a clear status.

Recommended RFC statuses include:

- Proposed;
- Under Review;
- Accepted;
- Rejected;
- Deferred;
- Revised;
- Superseded.

A Proposed RFC has been written but not yet reviewed.

An Under Review RFC is being evaluated.

An Accepted RFC has been approved through governance.

A Rejected RFC was reviewed and not accepted.

A Deferred RFC is not rejected but is postponed for later consideration.

A Revised RFC has been changed in response to review.

A Superseded RFC has been replaced by a later RFC or governed document.

RFC status SHOULD be shown in RFC metadata.

Example:

```text
Status: Proposed
```

### 9.5 RFC Content Expectations

An RFC SHOULD include enough information for meaningful review.

At minimum, an RFC SHOULD identify:

- title;
- status;
- date;
- author or proposer where applicable;
- problem statement;
- proposed change;
- rationale;
- affected documents;
- affected layers;
- compatibility impact;
- privacy impact where applicable;
- migration impact where applicable;
- alternatives considered;
- approval path;
- expected next steps.

An RFC MAY also include:

- implementation notes;
- examples;
- proposed document text;
- open questions;
- risks;
- review notes;
- related ADRs;
- related RFCs;
- supersession notes.

RFC content SHOULD be clear enough that reviewers can understand both the proposal and its consequences.

### 9.6 RFC Review Expectations

An RFC SHOULD be reviewed before acceptance.

RFC review SHOULD consider:

- whether the problem is clearly stated;
- whether the proposed change is clearly described;
- whether the affected authority level is identified;
- whether the affected documents are identified;
- whether the affected layers are identified;
- whether compatibility impact is identified;
- whether privacy impact is identified where applicable;
- whether migration impact is identified where applicable;
- whether alternatives were considered;
- whether the proposed approval path is appropriate;
- whether the proposal conflicts with higher-authority documents;
- whether the proposal should result in an ADR;
- whether the proposal should result in a standard, specification, implementation document, or operational document update.

An RFC SHOULD NOT be accepted if it silently contradicts a higher-authority document.

An RFC that requires a higher-authority change SHOULD identify that change explicitly.

### 9.7 RFC Outcomes

An RFC MAY result in one or more outcomes.

Possible RFC outcomes include:

- accepted without revision;
- accepted with revision;
- rejected;
- deferred;
- superseded by another RFC;
- converted into an ADR;
- incorporated into a constitutional document;
- incorporated into a standard;
- incorporated into a specification;
- incorporated into an implementation document;
- incorporated into an operational document;
- split into multiple RFCs;
- withdrawn.

An Accepted RFC SHOULD result in updates to the appropriate governed documents.

A Rejected RFC MAY remain available as a historical record.

A Deferred RFC SHOULD identify why the proposal was deferred where practical.

A Superseded RFC SHOULD identify what superseded it.

### 9.8 RFC Relationship to ADRs

RFCs and ADRs serve different but related purposes.

An RFC proposes a change.

An ADR records a decision.

An RFC MAY lead to an ADR when the accepted or rejected proposal establishes an important architectural decision.

An ADR MAY reference the RFC that produced the decision.

A significant RFC outcome SHOULD result in an ADR when future maintainers would benefit from understanding the decision context.

An RFC does not need to produce an ADR when the result is minor, self-explanatory, or fully captured by the updated governed document.

### 9.9 RFC Relationship to Governed Documents

An RFC SHOULD NOT be the only place where an accepted rule is defined.

If an RFC is accepted, the approved change SHOULD be incorporated into the appropriate governed document.

For example:

- a constitutional change SHOULD update the relevant TB-series document;
- a standard-level change SHOULD update the relevant standard;
- a schema or format change SHOULD update the relevant specification;
- an implementation example SHOULD update the relevant implementation document;
- an operational procedure SHOULD update the relevant guide or SOP.

The RFC may remain as the historical proposal record.

The governed document becomes the active authority after approval and update.

### 9.10 RFC Numbering and Naming

RFCs SHOULD use a predictable identifier.

Recommended RFC naming format:

```text
RFC-0001 — Short Proposal Title
```

RFC numbers SHOULD be stable once assigned.

RFC titles SHOULD be short, descriptive, and human-readable.

An RFC filename SHOULD preserve the RFC identifier and title where practical.

Example:

```text
RFC-0001 — Add Governance Lifecycle States.md
```

RFC identifiers SHOULD NOT be reused for different proposals.

If an RFC is rejected, deferred, withdrawn, or superseded, its identifier SHOULD remain historically reserved.

### 9.11 RFC Supersession

An RFC MAY be superseded by a later RFC or by a governed document.

A superseded RFC SHOULD identify what supersedes it.

Example:

```text
Superseded By: RFC-0007 — Revised Governance Lifecycle Proposal
```

A later RFC that supersedes an earlier RFC SHOULD identify what it supersedes.

Example:

```text
Supersedes: RFC-0002 — Original Governance Lifecycle Proposal
```

RFC supersession SHOULD preserve traceability.

A future reader should be able to determine:

- what proposal was replaced;
- what proposal replaced it;
- why the proposal changed;
- whether compatibility is affected;
- whether a governed document was updated.

### 9.12 RFC Practicality

RFC usage SHOULD remain practical.

The Brain Standard should avoid requiring RFCs for every minor wording change, typo correction, formatting cleanup, or routine operational update.

RFCs are most useful when they make significant proposals reviewable before approval.

An RFC should reduce risk and prevent governance drift.

An RFC that adds process burden without improving review quality should be avoided.

## 10. Supersession and Deprecation Rules

Supersession and deprecation rules define how documents, decisions, rules, workflows, implementation patterns, and versions are replaced, discouraged, or preserved historically.

These rules exist to preserve traceability while allowing The Brain Standard to evolve.

A governed item SHOULD NOT disappear silently when it is replaced, discouraged, or no longer recommended.

Future humans, agents, workflows, and implementations SHOULD be able to determine:

- what changed;
- what was replaced;
- what remains historically valid;
- what is no longer recommended;
- what document or decision is now authoritative;
- whether compatibility is affected;
- whether migration is required.

Supersession and deprecation preserve continuity.

They prevent older decisions from being lost while making clear which documents and rules govern future work.

### 10.1 Supersession

Supersession occurs when one governed document, rule, decision, version, workflow, implementation pattern, or requirement replaces another.

A superseded item remains historically available but is no longer the active authority when a current approved replacement exists.

Supersession SHOULD be used when:

- a new version replaces an older version;
- a new document replaces an older document;
- a new rule replaces an older rule;
- a new decision replaces an older decision;
- a new workflow replaces an older workflow;
- a new implementation pattern replaces an older implementation pattern;
- a previous approach is no longer the active authority.

Supersession SHOULD be explicit.

A superseded document SHOULD identify the document or version that supersedes it.

Example:

```text
Status: Superseded
Superseded By: TB-0003 v0.2.0
```

A superseding document SHOULD identify what it supersedes.

Example:

```text
Supersedes: TB-0003 v0.1.0
Superseded By: None
```

### 10.2 Deprecation

Deprecation occurs when a governed document, rule, decision, workflow, implementation pattern, feature, or practice remains historically available but is no longer recommended for future use.

Deprecation is different from supersession.

A deprecated item may not yet have a complete replacement.

A superseded item has been replaced by another governed item.

Deprecation SHOULD be used when:

- an item is discouraged but not yet replaced;
- a better approach exists but migration may take time;
- an older approach remains necessary for compatibility;
- immediate replacement would cause unnecessary disruption;
- an item should remain visible for historical or migration reasons;
- a practice should stop being used for future work but may still explain older work.

A deprecated item SHOULD identify the reason for deprecation where practical.

A deprecated item SHOULD identify a replacement, migration path, or review path when one exists.

Example:

```text
Status: Deprecated
Reason: Replaced by clearer lifecycle terminology.
Replacement: TB-0003 Section 5 — Document Lifecycle States
```

### 10.3 Supersession vs. Deprecation

Supersession and deprecation are related but not identical.

Supersession means replacement.

Deprecation means discouraged future use.

A document may be deprecated before it is superseded.

A document may be superseded without a long deprecation period when the replacement is clear and compatibility risk is low.

A document may remain deprecated for an extended period when migration is complex or existing implementations still depend on it.

Use supersession when the question is:

```text
What replaces this?
```

Use deprecation when the question is:

```text
Should this still be used for future work?
```

Both supersession and deprecation SHOULD preserve historical traceability.

### 10.4 Supersession Metadata

Supersession SHOULD be reflected in document metadata.

A document that replaces another document SHOULD use the `Supersedes` field.

Example:

```text
Supersedes: TB-0003 v0.1.0
```

A document that has been replaced SHOULD use the `Superseded By` field.

Example:

```text
Superseded By: TB-0003 v0.2.0
```

If a document does not supersede anything, it SHOULD use:

```text
Supersedes: None
```

If a document has not been superseded, it SHOULD use:

```text
Superseded By: None
```

Supersession metadata SHOULD be updated when a document is replaced.

Supersession metadata SHOULD NOT be left ambiguous when a replacement exists.

### 10.5 Deprecation Metadata

Deprecation SHOULD be visible in document metadata or document text.

A deprecated document SHOULD use:

```text
Status: Deprecated
```

A deprecated item SHOULD identify the reason for deprecation where practical.

A deprecated item SHOULD identify a replacement where one exists.

Deprecation details MAY appear in a metadata field, a deprecation notice, a changelog, an ADR, an RFC, or a supersession note.

Example:

```text
Status: Deprecated
Deprecation Reason: Replaced by governed workflow review rules.
Replacement: WF-0001 — Workflow Lifecycle Standard
```

If no replacement exists, the deprecation notice SHOULD say so.

Example:

```text
Status: Deprecated
Replacement: None
```

### 10.6 Historical Preservation

Superseded, deprecated, and rejected documents SHOULD remain historically available where practical.

Historical preservation allows future humans and AI systems to understand:

- why a rule changed;
- why a document was replaced;
- why a proposal was rejected;
- how compatibility evolved;
- what older implementations may depend on;
- what migration path may be needed.

Historical preservation does not mean the old item remains active authority.

A preserved document’s current lifecycle state SHOULD be clear.

A preserved document SHOULD NOT be silently edited in a way that hides its historical meaning.

If a historical document requires correction, the correction SHOULD preserve traceability.

### 10.7 Compatibility During Supersession

Supersession SHOULD consider compatibility impact.

Before superseding an approved document, rule, decision, workflow, or implementation pattern, review SHOULD consider whether the change affects:

- existing approved documents;
- existing Knowledge Objects;
- existing Knowledge Records;
- metadata interpretation;
- source references;
- storage organization;
- agent permissions;
- workflow behavior;
- validation behavior;
- privacy classifications;
- implementation compliance;
- migration expectations;
- human readability;
- AI readability.

A supersession that creates compatibility risk SHOULD include compatibility notes, migration guidance, an ADR, an RFC, or other appropriate governance record.

### 10.8 Migration Guidance

Migration guidance SHOULD be provided when supersession or deprecation affects existing documents, knowledge, workflows, agents, implementations, or validation behavior.

Migration guidance MAY explain:

- what changed;
- who or what is affected;
- what remains valid;
- what should be updated;
- what should not be used for new work;
- whether automated migration is allowed;
- whether human review is required;
- whether old references remain valid;
- whether compatibility is preserved.

Migration guidance SHOULD be proportional to the significance of the change.

Minor editorial supersession may require little or no migration guidance.

Major architectural, compatibility, privacy, workflow, agent, implementation, or governance supersession SHOULD include stronger migration guidance.

### 10.9 Supersession Through ADRs and RFCs

An ADR MAY supersede an earlier ADR.

An RFC MAY supersede an earlier RFC.

An accepted RFC MAY lead to a superseding document.

An ADR MAY explain why supersession occurred.

However, an ADR or RFC SHOULD NOT be the only place where an active replacement rule is defined if that rule affects standard behavior.

When supersession changes active requirements, the appropriate constitutional document, standard, or specification SHOULD be updated.

### 10.10 Supersession and Authority

Supersession MUST respect document authority levels.

A lower-authority document MUST NOT supersede a higher-authority document.

For example:

- an operational guide MUST NOT supersede a constitutional document;
- a reference implementation MUST NOT supersede a standard;
- an RFC MUST NOT supersede an approved standard unless the standard is formally revised through governance;
- an ADR MUST NOT supersede a constitutional rule unless the constitutional document is formally revised.

A lower-authority document MAY identify a problem with a higher-authority document.

A lower-authority document MAY propose that a higher-authority document be revised or superseded.

The higher-authority document changes only when approved through the correct governance process.

### 10.11 Deprecation and Authority

Deprecation MUST respect document authority levels.

A lower-authority document MUST NOT deprecate a higher-authority document.

A lower-authority document MAY recommend deprecation of a higher-authority document, rule, decision, workflow, or implementation pattern.

The deprecation becomes authoritative only when approved at the correct authority level.

Deprecation SHOULD NOT be used as a workaround for disagreement with an approved higher-authority document.

If a higher-authority document is unclear, outdated, or problematic, the issue SHOULD be handled through ADR, RFC, revision, or formal governance.

### 10.12 Supersession Practicality

Supersession and deprecation SHOULD remain practical.

The Brain Standard should not require heavy supersession or deprecation processes for every wording improvement, typo correction, formatting cleanup, or minor clarification.

The process SHOULD scale with the authority, risk, and compatibility impact of the change.

Supersession and deprecation are most important when older material may otherwise be mistaken for current authority.

A good supersession or deprecation record SHOULD reduce confusion, preserve history, and support safe evolution.

## 11. Governance Boundaries

Governance boundaries define what governance MAY control, what governance SHOULD guide, and what governance SHOULD avoid over-controlling.

Governance exists to preserve The Brain Standard without turning every routine choice, habit, example, tool setting, or implementation detail into architecture.

A governance boundary separates:

- standard behavior from implementation behavior;
- architectural rules from operational guidance;
- required structure from recommended practice;
- proposals from approved changes;
- examples from requirements;
- automation assistance from governance authority;
- personal workflow choices from standard rules.

Governance boundaries are necessary because The Brain Standard must remain durable and trustworthy while still being practical for daily use.

Over-governance can make the system too burdensome.

Under-governance can allow drift, hidden dependencies, implementation lock-in, privacy failure, or unreviewable automation.

The governance model SHOULD preserve the balance between architectural discipline and practical usability.

### 11.1 What Governance Controls

Governance controls changes to The Brain Standard.

At minimum, governance SHOULD control:

- constitutional documents;
- standards;
- specifications;
- document authority levels;
- document lifecycle states;
- approval expectations;
- review expectations;
- versioning expectations;
- supersession and deprecation rules;
- ADR usage;
- RFC usage;
- compatibility review;
- privacy-impact review;
- major implementation compliance expectations;
- major workflow requirements;
- major agent permission rules;
- changes that affect knowledge meaning, object identity, portability, reviewability, or governance.

Governance SHOULD apply when a decision affects the meaning, authority, compatibility, privacy, lifecycle, validation, or long-term maintainability of the standard.

### 11.2 What Governance Guides

Governance may guide behavior without controlling every detail.

Governance MAY guide:

- recommended workflows;
- reference implementation patterns;
- folder organization examples;
- naming examples;
- review checklists;
- migration practices;
- maintenance habits;
- agent-use practices;
- tool configuration examples;
- operational procedures;
- daily-use guidance.

Guidance helps users, agents, and implementations follow the standard consistently.

However, guidance MUST remain distinguishable from requirements.

A guide, checklist, reference implementation, example, or operational habit MUST NOT become a required part of The Brain Standard unless approved at the correct authority level.

### 11.3 What Governance Should Avoid Controlling

Governance SHOULD avoid controlling details that do not affect the standard.

Governance SHOULD NOT over-control:

- personal note-taking preferences;
- user interface preferences;
- editor choice;
- operating system choice;
- local folder convenience choices that do not define meaning;
- formatting preferences that do not affect interpretation;
- tool shortcuts;
- routine drafting habits;
- private working notes;
- temporary scratch files;
- implementation optimizations that do not affect standard behavior;
- operational details that do not affect compatibility, privacy, reviewability, or governance.

The Brain Standard should avoid turning every practical preference into a governed rule.

A detail should be governed only when governing it materially improves durability, portability, trustworthiness, privacy, reviewability, interoperability, automation reliability, or long-term maintainability.

### 11.4 Governance and Implementation Independence

Governance MUST preserve implementation independence.

No implementation, reference implementation, tool, plugin, database, file system, vault, AI model, workflow engine, or user interface MAY become the standard by default.

A reference implementation MAY demonstrate one compliant approach.

An implementation MAY include features that improve usability, performance, search, automation, validation, or review.

However, implementation behavior MUST NOT redefine standard behavior unless the standard is formally revised through governance.

If an implementation reveals a gap in the standard, the gap SHOULD be addressed through an ADR, RFC, standard, specification, or constitutional revision.

### 11.5 Governance and Operational Practice

Operational practice supports daily use of The Brain Standard.

Operational practice MAY include:

- how a user drafts notes;
- how a user reviews documents;
- how a user organizes temporary work;
- how a user uses an editor;
- how a user runs local checks;
- how a user interacts with agents;
- how a user prepares documents for approval;
- how a user maintains a vault.

Operational practice MUST NOT redefine the standard.

A repeated practice is not governance by itself.

A repeated practice becomes part of the governed standard only when it is documented, reviewed, and approved at the appropriate authority level.

Operational documents SHOULD make clear when they are describing recommended practice rather than required standard behavior.

### 11.6 Governance and Agents

Agents may assist governance, but agents are not governance authorities by default.

Agents MAY assist with:

- drafting documents;
- reviewing syntax;
- checking consistency;
- identifying conflicts;
- suggesting ADRs or RFCs;
- preparing review checklists;
- comparing documents;
- finding supersession issues;
- detecting governance drift;
- proposing revisions.

Agents MUST NOT silently approve, reject, supersede, deprecate, or materially revise governed documents unless a future approved governance process explicitly permits a defined and bounded automated action.

Agent output SHOULD remain reviewable by a human when it affects governance, authority, compatibility, privacy, lifecycle state, or standard meaning.

An agent recommendation does not become authoritative merely because it was generated.

### 11.7 Governance and Workflows

Workflows may coordinate governance activity, but workflows are not governance authorities by default.

Workflows MAY support:

- drafting;
- review routing;
- checklist execution;
- compatibility review;
- approval preparation;
- metadata updates;
- version checks;
- supersession checks;
- deprecation notices;
- ADR creation;
- RFC creation;
- archival preservation.

A workflow MUST NOT treat completion as approval unless the workflow explicitly includes an approved governance step that grants approval.

Workflow convenience MUST NOT bypass document authority, human review, privacy boundaries, compatibility review, or supersession rules.

Workflow outputs SHOULD remain traceable when they affect governed documents.

### 11.8 Governance and Privacy

Governance MUST preserve privacy boundaries.

A governance process MUST NOT expose restricted knowledge merely because it is relevant to a review, RFC, ADR, implementation, workflow, or agent task.

Governance reviews SHOULD consider whether a proposed change affects:

- privacy classification;
- agent access;
- workflow routing;
- storage exposure;
- search indexing;
- synchronization;
- backups;
- exports;
- publication;
- logs;
- implementation interfaces.

Privacy-sensitive governance records SHOULD reveal only the information necessary for review and traceability.

When privacy and governance transparency conflict, privacy SHALL take precedence unless a higher-authority process explicitly defines a safe disclosure rule.

### 11.9 Governance and Compatibility

Governance SHOULD preserve compatibility whenever reasonably possible.

A governance decision SHOULD consider whether existing documents, knowledge records, workflows, agents, implementations, or references may be affected.

Compatibility does not mean the standard can never change.

Compatibility means changes SHOULD be intentional, reviewed, documented, and supported by migration guidance where needed.

A governance decision that breaks compatibility SHOULD include documented rationale and impact review.

### 11.10 Governance and Experimentation

Experimentation MAY occur outside the approved standard.

Experimental documents, workflows, agents, implementation patterns, schemas, or tools MAY be created to test ideas.

Experimental work MUST be clearly distinguishable from approved standard behavior.

Experimental work MUST NOT redefine the standard unless later accepted through governance.

Experimental work SHOULD be marked clearly where practical.

Example:

```text
Status: Experimental
```

Experimental work SHOULD be reviewed before it influences approved constitutional documents, standards, specifications, workflows, agents, implementations, or operational guides.

### 11.11 Governance Boundary Review

When it is unclear whether something should be governed, the following questions SHOULD guide review:

- Does it affect knowledge meaning?
- Does it affect object identity?
- Does it affect document authority?
- Does it affect compatibility?
- Does it affect privacy?
- Does it affect lifecycle state?
- Does it affect versioning?
- Does it affect supersession or deprecation?
- Does it affect agent permissions?
- Does it affect workflow behavior?
- Does it affect implementation compliance?
- Does it create a hidden dependency?
- Does it create a precedent others may rely on?
- Would failure to govern it create drift or confusion?
- Would governing it create unnecessary burden?

If the answer indicates architectural risk, the item SHOULD be governed.

If the answer indicates only personal preference or low-risk operational convenience, the item SHOULD remain guidance, example, or implementation-specific behavior.

### 11.12 Governance Boundary Success

Governance boundaries are successful when they preserve the standard without making the standard difficult to use.

A successful governance boundary helps future humans, agents, workflows, and implementations understand:

- what is authoritative;
- what is proposed;
- what is historical;
- what is an example;
- what is implementation-specific;
- what is operational guidance;
- what requires review;
- what may remain flexible.

The goal is not to govern everything.

The goal is to govern the things that affect The Brain Standard’s durability, portability, trustworthiness, privacy, reviewability, compatibility, and long-term coherence.

## 12. Governance Drift Prevention

Governance drift occurs when The Brain Standard changes informally without review, approval, traceability, or proper authority.

Governance drift may happen through repeated habit, tool defaults, workflow convenience, agent behavior, implementation assumptions, undocumented decisions, copied examples, or informal operational practice.

Governance drift is dangerous because it can allow the standard to change without anyone explicitly deciding that it should change.

The Brain Standard MUST prevent governance drift where drift would affect meaning, authority, compatibility, privacy, reviewability, portability, implementation independence, or long-term maintainability.

Governance drift prevention exists to ensure that the standard evolves deliberately rather than accidentally.

### 12.1 Sources of Governance Drift

Governance drift MAY come from many sources.

Common sources include:

- repeated informal practice;
- undocumented decisions;
- tool defaults;
- implementation-specific behavior;
- workflow shortcuts;
- agent-generated changes;
- copied examples;
- unreviewed templates;
- outdated guides;
- abandoned drafts;
- unclear supersession;
- missing deprecation notices;
- ambiguous authority levels;
- unclear lifecycle states;
- implicit approval through repeated use;
- private working habits being treated as standard behavior.

A source of drift is not always harmful by itself.

A practice becomes a governance concern when it begins to affect how the standard is interpreted, applied, implemented, validated, or trusted.

### 12.2 Drift Through Repeated Practice

A repeated practice MUST NOT become part of The Brain Standard merely because it is repeated.

Repeated practice may reveal a useful pattern.

However, useful patterns SHOULD be reviewed before becoming standard behavior.

If a repeated practice appears valuable, it SHOULD be evaluated through the appropriate governance path.

Depending on the scope and risk, the practice MAY result in:

- an operational document;
- a reference implementation note;
- an ADR;
- an RFC;
- a standard update;
- a specification update;
- a constitutional revision.

Repeated use is evidence of usefulness, not evidence of authority.

### 12.3 Drift Through Tools and Implementations

Tools and implementations MUST NOT redefine The Brain Standard by default.

A tool may make certain behaviors easier, faster, or more visible.

An implementation may include defaults, constraints, automations, templates, or validation rules.

Those behaviors are implementation behavior unless approved as standard behavior.

If a tool or implementation introduces behavior that affects meaning, metadata, relationships, privacy, storage expectations, lifecycle state, validation, compatibility, or governance, the behavior SHOULD be reviewed.

A useful implementation behavior MAY become part of the standard only through the correct governance process.

### 12.4 Drift Through Agents

Agents MUST NOT become hidden governance authorities.

Agent output MAY support drafting, review, comparison, validation, consistency checks, and governance preparation.

Agent output MUST remain distinguishable from approved governance decisions.

An agent suggestion does not become authoritative merely because it is plausible, repeated, automated, or convenient.

Agent-generated changes SHOULD be reviewable when they affect:

- document authority;
- lifecycle state;
- versioning;
- supersession;
- deprecation;
- compatibility;
- privacy;
- metadata meaning;
- object identity;
- source handling;
- storage behavior;
- workflow behavior;
- implementation compliance;
- governance rules.

If an agent repeatedly recommends the same pattern, that pattern MAY be reviewed through ADR, RFC, standard, specification, implementation documentation, or operational guidance.

### 12.5 Drift Through Workflows

Workflows MUST NOT bypass governance.

A workflow may coordinate drafting, review, routing, validation, metadata updates, approval preparation, ADR creation, RFC creation, supersession checks, or publication.

However, workflow completion MUST NOT be treated as approval unless the workflow includes an approved governance step that grants approval.

Workflow convenience MUST NOT override document authority.

Workflow shortcuts SHOULD be reviewed if they affect compatibility, privacy, lifecycle state, versioning, supersession, deprecation, approval, or governed meaning.

A workflow may automate steps, but it MUST NOT hide decisions that require governance.

### 12.6 Drift Through Examples and Templates

Examples and templates are useful, but they are not automatically authoritative.

An example shows one possible way to follow the standard.

A template provides a reusable structure.

An example or template MUST NOT define a required rule unless the rule is approved in the appropriate governed document.

Examples and templates SHOULD clearly distinguish required fields from optional guidance where practical.

If an example or template becomes widely reused, it SHOULD be reviewed to ensure it does not accidentally introduce hidden requirements, implementation lock-in, privacy exposure, or compatibility assumptions.

### 12.7 Drift Through Documentation Gaps

Governance drift may occur when the standard is unclear, incomplete, or silent.

When users, agents, workflows, or implementations repeatedly fill the same gap informally, the gap SHOULD be reviewed.

A documentation gap MAY result in:

- clarification;
- new examples;
- an operational guide;
- a reference implementation note;
- a specification update;
- a standard update;
- an ADR;
- an RFC;
- a constitutional revision.

Unclear standard behavior SHOULD be resolved through governance rather than through uncontrolled habit.

### 12.8 Drift Through Outdated Documents

Outdated documents can create governance drift when users, agents, workflows, or implementations rely on old guidance as if it were current authority.

Approved, deprecated, superseded, rejected, and draft documents SHOULD be clearly distinguishable.

A document that has been replaced SHOULD identify its replacement where practical.

A document that is no longer recommended SHOULD identify its deprecated status where practical.

Operational documents SHOULD be reviewed or updated when higher-authority documents change.

Reference implementations SHOULD be reviewed when standards or specifications change.

### 12.9 Drift Detection

Governance drift SHOULD be actively detectable.

Drift detection MAY include:

- syntax review;
- metadata review;
- authority review;
- lifecycle-state review;
- version review;
- supersession review;
- deprecation review;
- compatibility review;
- privacy review;
- agent-output review;
- workflow-output review;
- implementation review;
- comparison against higher-authority documents.

A drift check SHOULD ask:

- Has a practice become common without approval?
- Has a tool default changed interpretation?
- Has an agent recommendation become treated as authority?
- Has an implementation behavior become required by habit?
- Has an operational guide contradicted a higher-authority document?
- Has a superseded document continued to be used as active authority?
- Has a deprecated practice continued to guide new work?
- Has a draft document been treated as approved?
- Has a template introduced hidden requirements?
- Has a workflow bypassed review?

Drift detection SHOULD focus on risks that affect meaning, authority, compatibility, privacy, reviewability, portability, or long-term maintainability.

### 12.10 Drift Correction

When governance drift is found, it SHOULD be corrected.

Drift correction MAY include:

- clarifying a document;
- updating metadata;
- correcting lifecycle state;
- adding a deprecation notice;
- adding a supersession notice;
- revising an operational guide;
- updating a reference implementation;
- creating an ADR;
- creating an RFC;
- revising a standard;
- revising a specification;
- revising a constitutional document;
- adding migration guidance;
- documenting a compatibility impact.

Correction SHOULD be proportional to the risk and authority level of the drift.

Minor drift may require only clarification.

Major drift affecting architecture, compatibility, privacy, authority, lifecycle behavior, implementation compliance, or governance SHOULD receive stronger review.

### 12.11 Drift and Compatibility

Governance drift may create compatibility risk.

If drift has affected existing documents, knowledge records, workflows, agents, implementations, or validation behavior, correction SHOULD consider compatibility impact.

A drift correction SHOULD avoid unnecessary breakage where possible.

When breakage is unavoidable, the correction SHOULD include documented rationale, impact review, compatibility notes, and migration guidance where needed.

The goal of drift correction is not only to restore formal correctness.

The goal is also to preserve trust in existing knowledge while preventing future confusion.

### 12.12 Drift Prevention Responsibilities

Governance drift prevention is a shared responsibility across humans, agents, workflows, and implementations.

Humans SHOULD review significant changes before approval.

Agents SHOULD surface likely conflicts, inconsistencies, missing metadata, and authority problems.

Workflows SHOULD preserve reviewability and traceability.

Implementations SHOULD distinguish standard behavior from implementation-specific behavior.

Operational documents SHOULD avoid turning convenience into authority.

Governed documents SHOULD clearly identify authority, lifecycle state, version, dependencies, supersession, and related decisions.

No single tool, agent, workflow, or implementation SHOULD be trusted to prevent all drift alone.

### 12.13 Drift Prevention Success

Governance drift prevention is successful when The Brain Standard changes deliberately, visibly, and traceably.

A successful drift-prevention model ensures that:

- approved rules remain distinguishable from proposals;
- examples remain distinguishable from requirements;
- implementation behavior remains distinguishable from standard behavior;
- agent suggestions remain distinguishable from governance decisions;
- workflows remain distinguishable from approval authority;
- deprecated material remains distinguishable from current guidance;
- superseded material remains distinguishable from active authority;
- historical records remain available without confusing current interpretation.

The purpose of drift prevention is not to stop evolution.

The purpose is to ensure that evolution remains governed, reviewable, compatible, and trustworthy.

## 13. Changing Constitutional Documents

Constitutional documents define the highest-authority foundation of The Brain Standard.

Changes to constitutional documents require special care because they may affect every standard, specification, ADR, RFC, workflow, agent, implementation, operational document, and future governance decision.

Constitutional documents SHOULD remain stable.

A constitutional document SHOULD be changed only when the change materially improves clarity, correctness, durability, portability, governance, compatibility, privacy, reviewability, implementation independence, or long-term architectural coherence.

A constitutional change MUST NOT be made casually.

A constitutional change SHOULD be deliberate, reviewable, traceable, and approved at the constitutional authority level.

### 13.1 Constitutional Change Scope

A constitutional change affects a TB-series document.

Constitutional changes MAY affect:

- mission;
- vision;
- scope;
- architectural principles;
- document authority hierarchy;
- layered architecture;
- governance model;
- compatibility expectations;
- privacy expectations;
- implementation independence;
- document lifecycle rules;
- versioning expectations;
- supersession and deprecation rules;
- approval and review expectations;
- ADR usage;
- RFC usage;
- governance boundaries;
- drift prevention rules;
- standard-wide interpretation.

A change SHOULD be treated as constitutional when it affects the foundation of The Brain Standard rather than only a lower-level detail.

### 13.2 When Constitutional Change Is Appropriate

A constitutional change SHOULD be considered when:

- an existing constitutional rule is unclear;
- an existing constitutional rule is incorrect;
- an existing constitutional rule creates unnecessary contradiction;
- an existing constitutional rule prevents necessary evolution;
- a foundational concept is missing;
- a higher-authority conflict cannot be resolved without constitutional revision;
- compatibility expectations need to be clarified;
- governance authority needs to be clarified;
- document authority hierarchy needs to be clarified;
- layer boundaries need to be clarified;
- long-term architectural coherence would be improved.

A constitutional change SHOULD NOT be used for ordinary operational convenience.

A constitutional change SHOULD NOT be used to bypass an approved standard, specification, ADR, RFC, implementation document, or operational document.

A lower-authority issue SHOULD be resolved at the lower authority level unless the issue reveals a true constitutional gap or conflict.

### 13.3 Constitutional Change Proposal

A constitutional change SHOULD begin as a reviewable proposal.

The proposal MAY take the form of:

- a draft revision;
- an RFC;
- an ADR;
- a review note;
- a constitutional amendment draft;
- a replacement constitutional document;
- a supersession proposal.

A constitutional change proposal SHOULD identify:

- the constitutional document affected;
- the section or rule affected;
- the proposed change;
- the reason for the change;
- the problem being solved;
- the authority impact;
- the compatibility impact;
- the privacy impact where applicable;
- the implementation impact where applicable;
- the workflow impact where applicable;
- the agent impact where applicable;
- alternatives considered;
- whether an ADR or RFC is required;
- whether migration guidance is required.

The proposal SHOULD be clear enough that future humans and AI systems can understand why the change was considered.

### 13.4 Constitutional Review Requirements

A constitutional change SHOULD receive stronger review than ordinary editorial or operational changes.

A constitutional review SHOULD consider:

- alignment with TB-0000;
- alignment with TB-0001;
- alignment with TB-0002;
- alignment with TB-0003;
- effect on document authority;
- effect on operational layers;
- effect on standards;
- effect on specifications;
- effect on ADRs and RFCs;
- effect on implementations;
- effect on workflows;
- effect on agents;
- effect on operational documents;
- compatibility impact;
- privacy impact;
- migration impact;
- risk of governance drift;
- risk of implementation lock-in;
- risk of ambiguity;
- risk of unnecessary burden.

A constitutional change SHOULD NOT be approved if its impact is unclear.

When the impact cannot be fully known, the uncertainty SHOULD be documented.

### 13.5 Constitutional Compatibility Review

A constitutional change SHOULD include compatibility review.

Compatibility review SHOULD consider whether the change affects:

- existing approved documents;
- future standards;
- future specifications;
- existing Knowledge Objects;
- existing Knowledge Records;
- source references;
- metadata interpretation;
- object identity;
- storage expectations;
- agent boundaries;
- workflow behavior;
- implementation compliance;
- validation behavior;
- privacy classifications;
- import or export expectations;
- migration expectations;
- human readability;
- AI readability.

A constitutional change that breaks compatibility SHOULD include documented rationale, impact review, and migration guidance where practical.

Compatibility breakage SHOULD be avoided unless the change materially improves the long-term correctness, durability, privacy, portability, or coherence of The Brain Standard.

### 13.6 Constitutional Privacy Review

A constitutional change SHOULD consider privacy impact where applicable.

Privacy review SHOULD consider whether the change affects:

- privacy boundaries;
- classification of knowledge;
- agent access;
- workflow routing;
- storage exposure;
- implementation access;
- validation logs;
- search indexing;
- synchronization;
- backups;
- exports;
- publication;
- human review boundaries.

A constitutional change MUST NOT weaken privacy boundaries accidentally.

If a constitutional change intentionally changes privacy expectations, the change SHOULD include documented rationale, impact review, and approval at the constitutional authority level.

When privacy and convenience conflict, privacy SHALL take precedence unless a higher-authority constitutional rule explicitly defines a safe exception.

### 13.7 Constitutional Approval

A constitutional change becomes authoritative only when approved at the constitutional authority level.

Approval SHOULD be explicit.

An approved constitutional change SHOULD update:

- `Status`;
- `Version`;
- `Last Updated`;
- `Supersedes`;
- `Superseded By`;
- related ADRs or RFCs where applicable;
- compatibility notes where applicable;
- migration notes where applicable.

Approval SHOULD make clear:

- what changed;
- why it changed;
- what authority level applies;
- what documents are affected;
- what compatibility impact exists;
- whether migration is required;
- whether future review is required.

A constitutional change MUST NOT become authoritative merely because it was drafted, copied, implemented, automated, repeated, or recommended by an agent.

### 13.8 Constitutional Versioning

Constitutional changes SHOULD follow the versioning expectations defined by this governance model.

Minor constitutional changes MAY use a minor version update when the change is backward-compatible and does not alter foundational meaning.

Patch constitutional changes MAY use a patch version update when the change corrects formatting, grammar, typos, metadata, or non-meaning-changing wording.

Major constitutional changes SHOULD use a major version update when the change affects foundational meaning, authority, compatibility, lifecycle behavior, privacy expectations, or governance interpretation.

A constitutional version update SHOULD preserve traceability.

### 13.9 Constitutional Supersession

A constitutional document MAY be superseded by another constitutional document.

A lower-authority document MUST NOT supersede a constitutional document.

A constitutional document that supersedes another constitutional document SHOULD identify what it supersedes.

Example:

```text
Supersedes: TB-0003 v0.1.0
```

A constitutional document that has been superseded SHOULD identify what superseded it.

Example:

```text
Status: Superseded
Superseded By: TB-0003 v0.2.0
```

Constitutional supersession SHOULD preserve historical access to the superseded document.

A superseded constitutional document remains historically important but is no longer the active constitutional authority when a current approved replacement exists.

### 13.10 Constitutional Deprecation

A constitutional rule or document MAY be deprecated when it remains historically available but is no longer recommended for future use.

Deprecation of constitutional material SHOULD be rare.

Constitutional deprecation SHOULD identify:

- what is deprecated;
- why it is deprecated;
- whether a replacement exists;
- what compatibility impact exists;
- whether migration is required;
- whether future review is required.

A lower-authority document MUST NOT deprecate a constitutional document or constitutional rule.

A lower-authority document MAY recommend constitutional deprecation through an RFC, ADR, or formal review process.

### 13.11 Constitutional Change Records

A significant constitutional change SHOULD leave a durable record.

A constitutional change record MAY be captured through:

- document metadata;
- an ADR;
- an accepted RFC;
- a changelog;
- a supersession note;
- a deprecation notice;
- a migration note;
- a governance log.

The record SHOULD explain:

- what changed;
- why it changed;
- what alternatives were considered;
- what trade-offs were accepted;
- what compatibility impact exists;
- what privacy impact exists where applicable;
- what documents or layers are affected;
- whether future work is required.

A constitutional change record SHOULD help future humans and AI systems understand why the foundation changed.

### 13.12 Constitutional Change Practicality

The constitutional change process SHOULD remain practical.

Not every typo, formatting cleanup, or wording clarification requires a full constitutional review.

However, any change that affects meaning, authority, compatibility, privacy, lifecycle state, governance, architecture, or implementation independence SHOULD receive appropriate constitutional review.

The process SHOULD scale with the risk and significance of the change.

Constitutional stability is important, but constitutional documents MUST remain correct, usable, and capable of deliberate evolution.

## 14. Changing Standards, Specifications, and Operational Documents

Standards, specifications, implementation documents, reference implementations, and operational documents MAY change more frequently than constitutional documents.

These documents support the practical evolution of The Brain Standard while remaining subordinate to the constitutional foundation.

Changes to lower-authority documents SHOULD preserve alignment with TB-0000, TB-0001, TB-0002, TB-0003, and any other applicable higher-authority documents.

A lower-authority document MUST NOT be changed in a way that contradicts a higher-authority document.

If a necessary change appears to conflict with a higher-authority document, the higher-authority issue SHOULD be resolved through the appropriate governance process before the lower-authority change is approved.

### 14.1 Scope of Lower-Authority Changes

Lower-authority changes MAY affect:

- standards;
- specifications;
- implementation documents;
- reference implementations;
- operational documents;
- guides;
- procedures;
- checklists;
- schemas;
- formats;
- metadata fields;
- validation rules;
- workflow guidance;
- agent guidance;
- implementation examples;
- migration guidance;
- compatibility notes.

A change SHOULD be handled at the lowest appropriate authority level that can resolve the issue without contradicting higher-authority documents.

A lower-authority change SHOULD NOT be escalated to constitutional review unless it reveals a constitutional gap, conflict, ambiguity, or foundational issue.

### 14.2 Changing Standards

Standards define required or recommended behavior for major architectural areas of The Brain Standard.

A standard change SHOULD be reviewed when it affects:

- Knowledge Standards;
- Storage Standards;
- Agent Standards;
- Workflow Standards;
- implementation compliance;
- interoperability;
- validation behavior;
- privacy expectations;
- compatibility expectations;
- lifecycle behavior;
- standard-wide recommended practice within a layer or domain.

A standard change MUST conform to constitutional documents.

A standard change SHOULD identify:

- the standard affected;
- the section or rule affected;
- the proposed change;
- the reason for the change;
- the affected operational layer or domain;
- compatibility impact;
- privacy impact where applicable;
- implementation impact where applicable;
- workflow impact where applicable;
- agent impact where applicable;
- whether an ADR or RFC is required;
- whether migration guidance is required.

A standard change SHOULD receive stronger review when it affects required behavior, compatibility, privacy, validation, implementation compliance, or cross-layer interpretation.

### 14.3 Changing Specifications

Specifications define exact structures, schemas, formats, fields, validation rules, and technical requirements.

A specification change SHOULD be reviewed when it affects:

- metadata fields;
- object templates;
- schemas;
- file formats;
- naming formats;
- relationship structures;
- lifecycle values;
- privacy classification values;
- validation rules;
- import formats;
- export formats;
- compatibility constraints.

A specification change MUST conform to constitutional documents and relevant standards.

A specification change SHOULD identify:

- the specification affected;
- the structure, schema, field, format, or rule affected;
- the proposed change;
- the reason for the change;
- validation impact;
- compatibility impact;
- privacy impact where applicable;
- migration impact where applicable;
- affected implementations;
- affected workflows;
- affected agents;
- affected Knowledge Objects or Knowledge Records;
- whether old data remains valid;
- whether automated migration is allowed;
- whether human review is required.

A specification change SHOULD be precise enough for humans, agents, validators, and implementations to apply consistently.

A specification change SHOULD avoid unnecessary implementation lock-in.

### 14.4 Changing Implementation Documents

Implementation documents describe how a specific tool, vault, database, workflow environment, file system, agent system, or interface realizes The Brain Standard.

An implementation document change MAY describe:

- tool configuration;
- folder layout;
- database structure;
- file organization;
- validation behavior;
- agent setup;
- workflow setup;
- import behavior;
- export behavior;
- synchronization behavior;
- backup behavior;
- user interface behavior;
- implementation profile behavior.

An implementation document MUST distinguish standard behavior from implementation-specific behavior.

An implementation document change MUST NOT redefine The Brain Standard.

If an implementation document reveals a gap in the standard, that gap SHOULD be addressed through an ADR, RFC, standard, specification, or constitutional revision.

An implementation document change SHOULD be reviewed when it affects compatibility, privacy, validation, portability, implementation compliance, workflow behavior, or agent behavior.

### 14.5 Changing Reference Implementations

Reference implementations demonstrate one compliant way to apply The Brain Standard.

A reference implementation MAY change when:

- a clearer example exists;
- a tool configuration improves;
- a validation method improves;
- a workflow example improves;
- a storage layout example improves;
- a standard or specification changes;
- an implementation pattern becomes outdated;
- an example creates confusion;
- an example no longer reflects approved documents.

Reference implementation changes SHOULD preserve the distinction between example behavior and required standard behavior.

A reference implementation MUST NOT become required merely because it is useful, popular, repeated, automated, or convenient.

If a reference implementation change introduces a pattern that should become required, the requirement SHOULD be proposed through the appropriate governed document rather than through the reference implementation alone.

### 14.6 Changing Operational Documents

Operational documents support practical use of The Brain Standard.

Operational documents MAY include:

- guides;
- checklists;
- procedures;
- standard operating procedures;
- onboarding notes;
- maintenance instructions;
- workflow instructions;
- review instructions;
- user-facing documentation.

Operational documents MAY change more frequently than constitutional documents, standards, or specifications.

Operational document changes SHOULD remain lightweight when they affect only clarity, usability, formatting, examples, or routine daily-use guidance.

Operational document changes SHOULD receive stronger review when they affect:

- interpretation of approved rules;
- privacy behavior;
- compatibility expectations;
- workflow behavior;
- agent behavior;
- validation behavior;
- migration behavior;
- approval behavior;
- supersession or deprecation guidance.

Operational documents MUST NOT define new architectural requirements unless those requirements already exist in a higher-authority document.

### 14.7 Editorial Changes

Editorial changes are changes that improve readability, formatting, grammar, spelling, organization, or clarity without changing meaning.

Editorial changes MAY follow a lighter review process.

Editorial changes MAY include:

- typo correction;
- grammar correction;
- formatting cleanup;
- heading cleanup;
- table formatting cleanup;
- link correction;
- wording clarification that does not change meaning;
- metadata cleanup that does not affect authority, lifecycle state, supersession, or compatibility.

An editorial change SHOULD NOT alter requirements, recommendations, permissions, authority, compatibility, privacy behavior, lifecycle behavior, or governance expectations.

If an apparent editorial change changes meaning, it SHOULD be treated as a substantive change.

### 14.8 Substantive Changes

Substantive changes affect meaning.

A substantive change MAY affect:

- requirements;
- recommendations;
- permissions;
- prohibited behavior;
- authority;
- lifecycle state;
- versioning;
- supersession;
- deprecation;
- compatibility;
- privacy;
- validation;
- implementation compliance;
- workflow behavior;
- agent behavior;
- migration expectations;
- interpretation of existing knowledge.

A substantive change SHOULD be reviewed before approval.

A substantive change SHOULD update version metadata according to the versioning expectations defined by this governance model.

A substantive change MAY require an ADR, RFC, compatibility review, privacy review, migration guidance, or supersession notice depending on authority level, scope, and risk.

### 14.9 Compatibility Review for Lower-Authority Changes

Lower-authority changes SHOULD consider compatibility impact when they affect existing documents, knowledge, workflows, agents, implementations, validation behavior, or operational practice.

Compatibility review SHOULD consider whether the change affects:

- existing approved documents;
- existing Knowledge Objects;
- existing Knowledge Records;
- metadata interpretation;
- source references;
- storage organization;
- agent permissions;
- workflow behavior;
- validation behavior;
- privacy classifications;
- implementation compliance;
- migration expectations;
- human readability;
- AI readability.

A lower-authority change that breaks compatibility SHOULD include documented rationale and migration guidance where practical.

Compatibility breakage SHOULD be avoided unless the change materially improves correctness, privacy, portability, durability, validation, or long-term maintainability.

### 14.10 Privacy Review for Lower-Authority Changes

Lower-authority changes SHOULD consider privacy impact when they affect access, storage, routing, visibility, logging, export, indexing, synchronization, backups, or agent behavior.

Privacy review SHOULD consider whether the change affects:

- privacy classification;
- source material exposure;
- agent access;
- workflow routing;
- storage exposure;
- search indexing;
- validation logs;
- synchronization;
- backups;
- exports;
- publication;
- implementation interfaces.

A lower-authority change MUST NOT weaken privacy boundaries accidentally.

If a lower-authority change intentionally changes privacy behavior, the change SHOULD include documented rationale, impact review, and approval at the appropriate authority level.

### 14.11 Versioning Lower-Authority Changes

Lower-authority documents SHOULD follow the versioning expectations defined by this governance model.

Patch version updates SHOULD be used for editorial changes that do not change meaning.

Minor version updates SHOULD be used for backward-compatible additions, clarifications, or extensions.

Major version updates SHOULD be used for changes that alter meaning, compatibility, privacy behavior, lifecycle behavior, validation behavior, implementation compliance, or required interpretation.

Version updates SHOULD preserve traceability.

Version numbers SHOULD NOT be used to hide breaking changes.

### 14.12 Superseding Lower-Authority Documents

A lower-authority document MAY be superseded by another document at the same or higher authority level.

A lower-authority document MUST NOT supersede a higher-authority document.

A superseding lower-authority document SHOULD identify what it supersedes.

Example:

```text
Supersedes: KS-0001 v1.0.0
```

A superseded lower-authority document SHOULD identify what superseded it.

Example:

```text
Status: Superseded
Superseded By: KS-0001 v1.1.0
```

Supersession SHOULD preserve historical access and traceability.

### 14.13 Deprecating Lower-Authority Documents

A lower-authority document, rule, workflow, implementation pattern, or operational practice MAY be deprecated when it remains historically available but is no longer recommended for future use.

Deprecation SHOULD identify:

- what is deprecated;
- why it is deprecated;
- whether a replacement exists;
- what compatibility impact exists;
- whether migration is required;
- whether future review is required.

A lower-authority document MUST NOT deprecate a higher-authority document.

A lower-authority document MAY recommend deprecation of a higher-authority document through ADR, RFC, or formal governance review.

### 14.14 Approval of Lower-Authority Changes

A lower-authority change becomes authoritative only when approved at the appropriate authority level.

Approval SHOULD be explicit.

Approval SHOULD confirm that the change:

- aligns with constitutional documents;
- aligns with relevant standards where applicable;
- has the correct authority level;
- has the correct lifecycle state;
- uses appropriate normative language;
- preserves compatibility or documents compatibility impact;
- preserves privacy or documents privacy impact;
- avoids hidden implementation dependencies;
- avoids governance drift;
- remains practical for daily use.

A lower-authority change MUST NOT become authoritative merely because it was drafted, copied, implemented, automated, repeated, or recommended by an agent.

### 14.15 Practicality of Lower-Authority Change Control

Lower-authority change control SHOULD remain practical.

Not every typo, formatting cleanup, wording clarification, example update, checklist improvement, or operational note requires heavy review.

The process SHOULD scale with the authority, scope, risk, compatibility impact, privacy impact, and long-term significance of the change.

Lower-authority documents SHOULD be easier to revise than constitutional documents.

However, lower-authority flexibility MUST NOT become a path for bypassing constitutional authority, standards authority, compatibility review, privacy boundaries, or governance discipline.

## 15. Compatibility Review

Compatibility review determines whether a proposed change preserves the meaning, usability, portability, interpretation, and trustworthiness of existing knowledge, documents, workflows, agents, implementations, and governance records.

Compatibility review exists because The Brain Standard is intended to preserve knowledge across long periods of technological and organizational change.

A change may be useful and still create compatibility risk.

Compatibility review helps ensure that change is deliberate, documented, and safe.

Compatibility review SHOULD be considered whenever a proposed change affects meaning, authority, metadata, object identity, storage expectations, workflow behavior, agent behavior, validation behavior, privacy behavior, implementation compliance, or governance interpretation.

### 15.1 Purpose of Compatibility Review

The purpose of compatibility review is to identify whether a change affects existing or future use of The Brain Standard.

Compatibility review SHOULD help determine:

- whether existing knowledge remains valid;
- whether existing documents remain interpretable;
- whether existing metadata retains its meaning;
- whether existing object identity remains stable;
- whether existing source references remain usable;
- whether existing workflows continue to behave correctly;
- whether existing agents can safely interpret the change;
- whether existing implementations remain compliant;
- whether existing validation rules remain accurate;
- whether migration guidance is required;
- whether supersession or deprecation is required.

Compatibility review does not exist to prevent all change.

Compatibility review exists to ensure that change is intentional, traceable, and understandable.

### 15.2 When Compatibility Review Is Required

Compatibility review SHOULD be performed when a proposed change affects:

- constitutional meaning;
- document authority;
- lifecycle state behavior;
- versioning behavior;
- supersession or deprecation behavior;
- Knowledge Object meaning;
- Knowledge Record meaning;
- metadata fields;
- object identity;
- relationship structures;
- source references;
- storage organization;
- privacy classification;
- agent permissions;
- workflow behavior;
- validation behavior;
- implementation compliance;
- import behavior;
- export behavior;
- migration expectations.

Compatibility review MAY be lightweight for minor editorial changes that do not change meaning.

Compatibility review SHOULD be stronger when the change affects approved documents, active workflows, existing implementations, privacy behavior, or long-term interpretation.

### 15.3 Compatibility With Constitutional Documents

All compatibility review SHOULD consider alignment with constitutional documents.

A proposed change SHOULD be checked against:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- future approved TB-series constitutional documents.

A change is not compatible if it contradicts the constitutional foundation.

If compatibility requires changing a constitutional document, the change SHOULD be handled through constitutional governance before lower-authority documents are treated as compatible.

A lower-authority change MUST NOT redefine constitutional meaning through implementation behavior, workflow convenience, agent output, operational guidance, or repeated use.

### 15.4 Compatibility With Existing Knowledge

Compatibility review SHOULD consider whether existing knowledge remains interpretable.

Review SHOULD consider whether the proposed change affects:

- Knowledge Objects;
- Knowledge Records;
- source material references;
- extracted knowledge;
- transformed knowledge;
- relationships between knowledge items;
- metadata values;
- classification values;
- object identity;
- provenance;
- auditability;
- human readability;
- AI readability.

A change SHOULD NOT cause existing knowledge to lose meaning without documented rationale and migration guidance.

If existing knowledge must be reinterpreted, converted, reclassified, migrated, deprecated, or superseded, the compatibility review SHOULD document that impact.

### 15.5 Compatibility With Metadata

Metadata compatibility is critical because metadata helps humans, agents, workflows, validators, and implementations interpret governed documents and knowledge records.

Compatibility review SHOULD consider whether a change affects:

- required metadata fields;
- optional metadata fields;
- metadata field names;
- metadata field values;
- metadata field meaning;
- lifecycle metadata;
- version metadata;
- supersession metadata;
- dependency metadata;
- privacy metadata;
- source metadata;
- relationship metadata;
- validation metadata.

A metadata change SHOULD preserve existing interpretation where practical.

If a metadata field is renamed, removed, split, merged, redefined, or replaced, the change SHOULD include migration guidance.

A metadata change that breaks existing interpretation SHOULD include documented rationale and compatibility notes.

### 15.6 Compatibility With Object Identity

Object identity compatibility determines whether existing objects remain identifiable across change.

Compatibility review SHOULD consider whether a change affects:

- object identifiers;
- object naming;
- object type definitions;
- object relationships;
- object versioning;
- object references;
- object lifecycle state;
- object provenance;
- import identity;
- export identity;
- duplicate detection;
- merge behavior.

A change SHOULD NOT break object identity without strong justification.

If object identity must change, the change SHOULD include migration guidance, traceability requirements, and review expectations.

Existing references SHOULD remain resolvable where practical.

### 15.7 Compatibility With Storage

Storage compatibility determines whether existing files, vaults, databases, folders, exports, backups, and synchronization structures remain usable.

Compatibility review SHOULD consider whether a change affects:

- file organization;
- folder organization;
- vault structure;
- database schema;
- file format;
- naming format;
- storage location;
- import behavior;
- export behavior;
- backup behavior;
- synchronization behavior;
- portability;
- recoverability;
- implementation independence.

Storage changes MUST NOT cause storage behavior to define knowledge meaning unless that meaning is approved in the appropriate governed document.

If a storage change affects portability, recoverability, import, export, or implementation independence, the change SHOULD receive stronger compatibility review.

### 15.8 Compatibility With Agents

Agent compatibility determines whether agents can safely interpret and operate within the changed standard.

Compatibility review SHOULD consider whether a change affects:

- agent permissions;
- agent boundaries;
- agent-readable metadata;
- agent-readable document structure;
- review requirements;
- approval behavior;
- privacy behavior;
- validation behavior;
- workflow participation;
- source material access;
- governed document editing;
- drift detection;
- human review requirements.

An agent compatibility issue SHOULD be reviewed carefully when the change affects authority, privacy, approval, lifecycle state, supersession, deprecation, or governed meaning.

Agents MUST NOT silently reinterpret a compatibility-breaking change as acceptable merely because it can be automated.

### 15.9 Compatibility With Workflows

Workflow compatibility determines whether existing workflows remain valid, safe, and reviewable after a change.

Compatibility review SHOULD consider whether a change affects:

- workflow steps;
- workflow routing;
- review checkpoints;
- approval checkpoints;
- metadata updates;
- validation steps;
- agent participation;
- human review;
- privacy handling;
- source handling;
- import steps;
- export steps;
- migration steps;
- operational maintenance.

A workflow change SHOULD preserve reviewability and traceability.

If a workflow must change because of a new standard, specification, lifecycle state, metadata field, privacy rule, or validation rule, the compatibility review SHOULD document the operational impact.

### 15.10 Compatibility With Implementations

Implementation compatibility determines whether existing implementations remain aligned with The Brain Standard.

Compatibility review SHOULD consider whether a change affects:

- reference implementations;
- implementation profiles;
- tool configurations;
- validators;
- importers;
- exporters;
- databases;
- vault structures;
- file systems;
- agent systems;
- workflow engines;
- user interfaces;
- automation scripts.

An implementation may need to change when the standard changes.

However, implementation convenience SHOULD NOT determine compatibility by itself.

A change SHOULD preserve implementation independence where practical.

If a change requires implementation updates, the compatibility review SHOULD identify affected implementations and whether migration guidance is needed.

### 15.11 Backward Compatibility

Backward compatibility means that existing approved documents, knowledge, workflows, agents, and implementations remain valid after a change.

Backward compatibility SHOULD be preserved where practical.

A backward-compatible change MAY include:

- adding optional metadata;
- clarifying wording without changing meaning;
- adding examples;
- adding guidance;
- adding a new lifecycle note without changing lifecycle behavior;
- adding a new validation recommendation that does not invalidate existing records;
- adding an implementation option without requiring it.

A change that claims backward compatibility SHOULD explain why existing material remains valid.

### 15.12 Breaking Changes

A breaking change is a change that alters existing meaning, invalidates existing structures, changes required interpretation, or requires migration.

Breaking changes SHOULD be avoided unless they materially improve correctness, privacy, durability, portability, governance, compatibility, validation, or long-term maintainability.

Breaking changes MAY affect:

- required metadata;
- object identity;
- relationship meaning;
- source reference meaning;
- lifecycle behavior;
- versioning behavior;
- validation rules;
- storage structure;
- agent behavior;
- workflow behavior;
- privacy behavior;
- implementation compliance;
- import or export behavior.

A breaking change SHOULD include:

- documented rationale;
- compatibility impact;
- migration guidance;
- affected documents;
- affected implementations where applicable;
- affected workflows where applicable;
- affected agents where applicable;
- versioning impact;
- supersession or deprecation notes where applicable.

Breaking changes MUST NOT be hidden as patch-level or editorial changes.

### 15.13 Migration Guidance

Migration guidance explains how affected documents, knowledge, workflows, agents, implementations, or operational practices should move from the old behavior to the new behavior.

Migration guidance SHOULD be provided when compatibility review identifies material impact.

Migration guidance MAY include:

- what changed;
- why it changed;
- what remains valid;
- what is deprecated;
- what is superseded;
- what should be updated;
- what should not be used for new work;
- whether automated migration is allowed;
- whether human review is required;
- whether old references remain valid;
- whether old records remain interpretable;
- what validation should be performed after migration.

Migration guidance SHOULD be proportional to the significance of the change.

A minor backward-compatible clarification may need little or no migration guidance.

A major breaking change SHOULD include clear migration guidance.

### 15.14 Compatibility Records

A compatibility review SHOULD leave a record when the change materially affects existing or future interpretation.

A compatibility record MAY be captured through:

- document metadata;
- an ADR;
- an RFC;
- a changelog;
- a review note;
- a migration guide;
- a supersession note;
- a deprecation notice;
- a governance log.

A compatibility record SHOULD identify:

- what changed;
- what compatibility risks were reviewed;
- what remains compatible;
- what is no longer compatible;
- what migration is required;
- what documents are affected;
- what workflows are affected;
- what agents are affected;
- what implementations are affected;
- whether privacy is affected;
- whether future review is required.

A compatibility record SHOULD be durable enough for future humans and AI systems to understand the impact of the change.

### 15.15 Compatibility Review Practicality

Compatibility review SHOULD remain practical.

Not every typo, formatting cleanup, wording improvement, example update, or operational note requires a heavy compatibility process.

The depth of compatibility review SHOULD scale with the authority level, risk, scope, privacy impact, implementation impact, workflow impact, agent impact, and long-term significance of the change.

A compatibility review is successful when it reduces avoidable breakage, preserves trust, and makes necessary change understandable.

Compatibility review SHOULD support evolution, not block it unnecessarily.

## 16. Approval Records and Change History

Approval records and change history preserve evidence of how The Brain Standard changes over time.

They exist to help future humans, agents, workflows, validators, and implementations understand what changed, why it changed, when it changed, who or what approved it where applicable, and what impact the change created.

A governed standard without approval records and change history can become difficult to trust.

The Brain Standard SHOULD preserve enough history to make meaningful changes traceable.

The amount of history required SHOULD scale with the authority level, risk, compatibility impact, privacy impact, and long-term significance of the change.

### 16.1 Purpose of Approval Records

The purpose of an approval record is to show that a governed document, revision, decision, proposal, or change was accepted at the appropriate authority level.

An approval record SHOULD make clear:

- what was approved;
- when it was approved;
- what document was affected;
- what version was approved;
- what authority level applies;
- what lifecycle state applies;
- what compatibility impact exists;
- what privacy impact exists where applicable;
- whether migration is required;
- whether supersession or deprecation occurred;
- whether related ADRs or RFCs exist;
- whether future review is required.

Approval records help prevent informal use, repeated practice, workflow completion, agent output, or implementation behavior from being mistaken for formal approval.

### 16.2 Purpose of Change History

The purpose of change history is to preserve the evolution of a governed document or decision over time.

A change history SHOULD help future humans and AI systems understand:

- what changed;
- why it changed;
- when it changed;
- whether the change was editorial or substantive;
- whether the change affected meaning;
- whether the change affected compatibility;
- whether the change affected privacy;
- whether the change affected governance;
- whether the change affected implementations, workflows, or agents;
- whether older versions remain valid;
- whether migration guidance exists.

Change history does not need to record every private drafting step.

Change history SHOULD record meaningful changes that affect interpretation, trust, compatibility, authority, lifecycle state, governance, or long-term maintainability.

### 16.3 Approval Record Locations

Approval records MAY be captured in one or more locations.

Possible approval record locations include:

- document metadata;
- a changelog section;
- an ADR;
- an accepted RFC;
- a governance log;
- a version history entry;
- a supersession note;
- a deprecation notice;
- a migration guide;
- a review note;
- an implementation compliance record.

The location SHOULD be appropriate to the authority level and importance of the change.

A minor editorial approval MAY be captured only through updated metadata.

A major constitutional, standards, specification, compatibility, privacy, lifecycle, or governance approval SHOULD leave a stronger record.

### 16.4 Minimum Metadata for Approval

An approved governed document SHOULD include enough metadata to identify its governance state.

At minimum, an approved governed document SHOULD include:

- `Document ID`;
- `Title`;
- `Version`;
- `Status`;
- `Created`;
- `Last Updated`;
- `Authority`;
- `Depends On` where applicable;
- `Supersedes`;
- `Superseded By`;
- related ADRs or RFCs where applicable.

Example:

```text
Document ID: TB-0003
Title: Governance Model
Version: 1.0.0
Status: Approved
Last Updated: 2026-06-25
Authority: Constitutional
Supersedes: None
Superseded By: None
Related: ADR-series; RFC-series
```

Metadata SHOULD remain consistent with the body of the document.

If metadata and document content conflict, the conflict SHOULD be corrected before approval where practical.

### 16.5 Change History Entries

A governed document MAY include a change history section when useful.

A change history entry SHOULD identify:

- version;
- date;
- lifecycle state;
- summary of change;
- type of change;
- authority level;
- compatibility impact;
- privacy impact where applicable;
- related ADR or RFC where applicable.

Example:

```markdown
| Version | Date       | Status   | Change Type | Summary                         |
| ------- | ---------- | -------- | ----------- | ------------------------------- |
| 0.1.0   | 2026-06-25 | Draft    | Initial     | Initial governance model draft. |
| 1.0.0   | 2026-06-25 | Approved | Approval    | First approved governance model. |
```

A change history table SHOULD remain concise.

Detailed rationale MAY be stored in an ADR, RFC, review note, or governance log when the explanation would make the document too heavy.

### 16.6 Change Types

Change history MAY classify changes by type.

Recommended change types include:

- Initial;
- Editorial;
- Clarification;
- Addition;
- Revision;
- Deprecation;
- Supersession;
- Compatibility;
- Privacy;
- Migration;
- Approval;
- Rejection;
- Governance.

A change type helps future readers understand the nature of a revision.

A change type does not replace lifecycle state, version number, authority level, or approval record.

### 16.7 Editorial Change Records

Editorial changes MAY receive lightweight change records.

Editorial changes include changes that improve readability, formatting, spelling, grammar, links, organization, examples, or Markdown quality without changing meaning.

An editorial change record MAY include only:

- updated `Last Updated` metadata;
- patch version update where appropriate;
- brief changelog note where useful.

Editorial change records SHOULD NOT imply that meaning, authority, compatibility, privacy behavior, lifecycle behavior, or governance expectations changed.

If an editorial change changes meaning, it SHOULD be treated as a substantive change.

### 16.8 Substantive Change Records

Substantive changes SHOULD leave stronger change records.

A substantive change affects meaning, authority, compatibility, privacy, lifecycle behavior, versioning, supersession, deprecation, validation, implementation compliance, workflow behavior, agent behavior, or governance interpretation.

A substantive change record SHOULD identify:

- what changed;
- why it changed;
- what authority level applies;
- what documents are affected;
- what compatibility impact exists;
- what privacy impact exists where applicable;
- whether migration is required;
- whether an ADR or RFC exists;
- whether the change supersedes or deprecates anything;
- whether future review is required.

A substantive change SHOULD NOT be hidden inside vague wording such as “cleanup,” “minor edits,” or “miscellaneous updates.”

### 16.9 Approval and Versioning

Approval records SHOULD align with versioning.

When a document is approved, the approved version SHOULD be clear.

When a new approved version replaces an older approved version, the supersession metadata SHOULD be updated.

A patch approval SHOULD indicate that the change does not materially change meaning.

A minor approval SHOULD indicate that the change is meaningful but compatible.

A major approval SHOULD indicate that the change materially affects meaning, compatibility, authority, privacy, lifecycle behavior, governance, or required interpretation.

Version numbers SHOULD NOT be used to obscure the significance of a change.

### 16.10 Approval and Supersession

When approval creates a replacement for an older governed document, rule, decision, version, workflow, implementation pattern, or operational practice, the approval record SHOULD preserve supersession traceability.

The superseding item SHOULD identify what it supersedes.

The superseded item SHOULD identify what superseded it where practical.

An approval record involving supersession SHOULD identify:

- what was replaced;
- what replaced it;
- why replacement occurred;
- whether older material remains valid;
- whether compatibility is affected;
- whether migration is required.

Supersession records SHOULD reduce confusion about which document or rule is current authority.

### 16.11 Approval and Deprecation

When approval deprecates a governed document, rule, decision, workflow, implementation pattern, or operational practice, the approval record SHOULD preserve deprecation traceability.

A deprecation approval record SHOULD identify:

- what was deprecated;
- why it was deprecated;
- whether a replacement exists;
- whether the deprecated item remains historically valid;
- whether new work should avoid it;
- whether migration is required;
- whether future review is required.

Deprecation records SHOULD help users, agents, workflows, and implementations distinguish historical material from recommended future behavior.

### 16.12 Approval and Compatibility

Approval records SHOULD identify compatibility impact when compatibility is material.

A compatibility-related approval record SHOULD identify whether the change is:

- backward-compatible;
- partially compatible;
- potentially incompatible;
- breaking;
- migration-required;
- historical-only.

A compatibility approval record SHOULD explain whether existing documents, knowledge, metadata, workflows, agents, implementations, validation behavior, imports, exports, or operational practices are affected.

When compatibility impact is unclear, the uncertainty SHOULD be documented.

### 16.13 Approval and Privacy

Approval records SHOULD identify privacy impact when privacy is material.

A privacy-related approval record SHOULD identify whether the change affects:

- privacy classification;
- source material exposure;
- agent access;
- workflow routing;
- storage exposure;
- search indexing;
- validation logs;
- synchronization;
- backups;
- exports;
- publication;
- implementation interfaces.

Privacy-sensitive approval records SHOULD reveal only the information necessary for review, traceability, and governance.

Approval history MUST NOT expose restricted knowledge unnecessarily.

### 16.14 Governance Logs

A governance log MAY be used to preserve approval records and change history across multiple documents.

A governance log MAY include:

- approved changes;
- rejected changes;
- deferred proposals;
- supersession events;
- deprecation events;
- compatibility decisions;
- privacy decisions;
- migration decisions;
- ADR references;
- RFC references;
- implementation-impact notes;
- workflow-impact notes;
- agent-impact notes.

A governance log SHOULD remain subordinate to governed documents.

A governance log MAY record what happened, but it MUST NOT override the authority of constitutional documents, standards, specifications, ADRs, RFCs, implementation documents, or operational documents.

### 16.15 Approval Record Practicality

Approval records and change history SHOULD remain practical.

Not every typo, formatting cleanup, wording clarification, checklist update, or operational note requires a heavy approval record.

The record depth SHOULD scale with the authority level, risk, compatibility impact, privacy impact, implementation impact, workflow impact, agent impact, and long-term significance of the change.

A good approval record SHOULD reduce future confusion.

A good change history SHOULD help future humans and AI systems understand the evolution of the standard without making the document unnecessarily difficult to maintain.

## 17. Governance Model Success Criteria

Governance model success criteria define how The Brain Standard can evaluate whether its governance approach is working.

The governance model is successful when it preserves the standard’s authority, clarity, compatibility, privacy, implementation independence, reviewability, and practical usability over time.

A governance model SHOULD NOT be judged only by whether it prevents mistakes.

It SHOULD also be judged by whether it allows useful, deliberate, traceable evolution.

The Brain Standard SHOULD remain stable enough to trust and flexible enough to improve.

### 17.1 Preservation of Constitutional Authority

The governance model is successful when constitutional authority remains clear.

Success means:

- constitutional documents remain the highest authority;
- lower-authority documents remain subordinate to constitutional documents;
- conflicts are resolved according to document authority;
- implementation behavior does not redefine constitutional meaning;
- workflow convenience does not bypass constitutional authority;
- agent output does not become governance authority by accident;
- constitutional changes are deliberate, reviewable, and traceable.

A governance model fails if constitutional documents can be silently overridden by tools, workflows, agents, implementation habits, or lower-authority documents.

### 17.2 Preservation of Architectural Coherence

The governance model is successful when The Brain Standard remains architecturally coherent as it grows.

Success means:

- new standards align with constitutional documents;
- new specifications align with relevant standards;
- new implementations remain replaceable;
- new workflows preserve reviewability;
- new agent behavior respects governance boundaries;
- document authority remains understandable;
- operational layers remain distinct;
- responsibilities do not collapse into one another.

Architectural coherence means that future growth strengthens the standard rather than fragmenting it.

### 17.3 Preservation of Compatibility

The governance model is successful when compatibility risks are visible, reviewed, and documented.

Success means:

- existing knowledge remains interpretable where practical;
- existing documents remain usable where practical;
- existing metadata remains meaningful where practical;
- existing object identity remains stable where practical;
- compatibility-breaking changes are not hidden;
- migration guidance exists when needed;
- supersession and deprecation are clear;
- old material is not mistaken for current authority.

Compatibility does not mean the standard never changes.

Compatibility means change is intentional, reviewed, traceable, and understandable.

### 17.4 Preservation of Privacy Boundaries

The governance model is successful when privacy boundaries remain protected during change.

Success means:

- governance review considers privacy impact where applicable;
- agents do not gain access merely because review is convenient;
- workflows do not expose restricted knowledge unnecessarily;
- approval records do not leak restricted information;
- compatibility records preserve privacy where needed;
- implementation behavior does not weaken privacy boundaries accidentally;
- privacy-sensitive material remains governed by appropriate access and review rules.

Privacy MUST remain stronger than convenience when the two conflict unless a higher-authority rule explicitly defines a safe exception.

### 17.5 Preservation of Implementation Independence

The governance model is successful when implementations remain replaceable.

Success means:

- no tool becomes the standard by default;
- no vault structure becomes mandatory unless approved as standard behavior;
- no database design defines meaning by accident;
- no AI model behavior becomes governance authority;
- reference implementations remain examples;
- implementation-specific behavior remains distinguishable from standard behavior;
- useful implementation discoveries are routed through ADRs, RFCs, standards, specifications, or constitutional revision when appropriate.

Implementation independence protects long-term portability.

### 17.6 Preservation of Human and AI Reviewability

The governance model is successful when changes remain reviewable by humans and interpretable by AI systems.

Success means:

- documents remain human-readable;
- documents remain AI-readable;
- metadata remains clear;
- lifecycle states remain visible;
- versioning remains understandable;
- review records remain traceable;
- approval records remain durable;
- compatibility impact remains discoverable;
- agent output remains distinguishable from approved governance decisions.

Reviewability supports trust.

A change that cannot be reviewed SHOULD NOT become authoritative without an approved governance process that explains why.

### 17.7 Prevention of Governance Drift

The governance model is successful when governance drift is detectable and correctable.

Success means:

- repeated practice does not become authority by accident;
- tool defaults do not redefine the standard;
- workflow shortcuts do not bypass review;
- agent suggestions do not become unreviewed decisions;
- templates do not introduce hidden requirements;
- outdated documents do not remain mistaken for active authority;
- deprecated and superseded material remains clearly marked;
- drift correction paths exist.

The purpose of drift prevention is not to block useful habits.

The purpose is to prevent useful habits from becoming architecture without review.

### 17.8 Practical Usability

The governance model is successful when it supports daily use.

Success means:

- minor editorial changes are not overburdened;
- operational documents remain easy to improve;
- lower-authority documents remain easier to revise than constitutional documents;
- review depth scales with risk;
- governance does not block ordinary drafting;
- users can understand what process applies;
- agents can assist without becoming hidden authorities;
- workflows can support governance without replacing approval.

A governance model that is too heavy will be ignored.

A governance model that is too weak will allow drift.

The successful model balances discipline with usability.

### 17.9 Traceability of Decisions

The governance model is successful when meaningful decisions remain traceable.

Success means:

- significant decisions are recorded;
- ADRs preserve architectural reasoning;
- RFCs preserve proposed changes;
- approval records preserve accepted changes;
- rejection records preserve rejected proposals where useful;
- supersession records identify replacements;
- deprecation records identify discouraged material;
- change history explains meaningful evolution.

Traceability helps future humans and AI systems understand not only what the standard says, but why it says it.

### 17.10 Safe Evolution

The governance model is successful when The Brain Standard can evolve safely.

Safe evolution means:

- changes are deliberate;
- changes are reviewable;
- changes are compatible where practical;
- breaking changes are documented;
- privacy impact is reviewed where applicable;
- migration guidance exists where needed;
- authority levels remain respected;
- approval is explicit;
- historical records remain available;
- future work can build on prior decisions confidently.

A standard that cannot evolve will become obsolete.

A standard that evolves without governance will become unreliable.

The Brain Standard requires both stability and evolution.

### 17.11 Success Review

The governance model SHOULD be reviewed periodically or when major governance problems appear.

A success review MAY consider:

- whether governance rules remain clear;
- whether authority levels remain useful;
- whether lifecycle states remain sufficient;
- whether ADR usage is practical;
- whether RFC usage is practical;
- whether compatibility review is effective;
- whether privacy review is sufficient;
- whether approval records are useful;
- whether change history is understandable;
- whether governance drift is being detected;
- whether the process is too heavy;
- whether the process is too weak.

A success review MAY result in clarification, an ADR, an RFC, a governance update, a standard update, an operational guide update, or a constitutional revision.

### 17.12 Failure Signals

The governance model may need revision if failure signals appear.

Failure signals include:

- repeated confusion about authority;
- frequent conflicts between documents;
- implementations redefining standard behavior;
- workflows bypassing approval;
- agents making unreviewed governance changes;
- outdated documents being used as current authority;
- compatibility impact being discovered too late;
- privacy impact being missed;
- approval records being unclear;
- change history being absent or misleading;
- users avoiding governance because it is too burdensome;
- routine changes requiring excessive process;
- major changes happening without enough review.

Failure signals SHOULD be treated as evidence for improvement, not as proof that governance should be abandoned.

### 17.13 Governance Model Success

The governance model succeeds when The Brain Standard remains trustworthy across time.

A successful governance model ensures that:

- authority remains clear;
- change remains deliberate;
- compatibility remains reviewable;
- privacy remains protected;
- implementation independence remains preserved;
- agent behavior remains bounded;
- workflow behavior remains reviewable;
- decisions remain traceable;
- documents remain understandable;
- daily use remains practical;
- future evolution remains possible.

The final measure of success is whether future humans and AI systems can understand, trust, maintain, and evolve The Brain Standard without losing its meaning.

## 18. Non-Goals

Non-goals define what the governance model intentionally does not attempt to control, define, or solve.

The purpose of this section is to prevent governance from expanding beyond its intended role.

Governance exists to preserve The Brain Standard, not to control every tool choice, personal habit, implementation detail, workflow preference, or operational convenience.

A non-goal does not mean the topic is unimportant.

A non-goal means the topic SHOULD NOT be treated as a responsibility of TB-0003 unless a future governed document explicitly changes that scope.

### 18.1 Not a Complete Legal Framework

TB-0003 does not define a complete legal framework.

This governance model does not define:

- legal ownership;
- licensing terms;
- liability rules;
- contract terms;
- regulatory compliance procedures;
- jurisdiction-specific legal obligations;
- intellectual property enforcement;
- external publication rights.

Legal, licensing, and regulatory matters MAY require separate governed documents.

Those documents SHOULD remain compatible with TB-0000, TB-0001, TB-0002, and TB-0003 where they affect The Brain Standard.

### 18.2 Not a Complete Security Standard

TB-0003 does not define a complete security standard.

This governance model defines privacy and governance boundaries, but it does not fully specify:

- authentication;
- authorization systems;
- encryption requirements;
- key management;
- network security;
- application security;
- threat modeling;
- incident response;
- secure coding practices;
- infrastructure hardening;
- vulnerability management.

Security requirements MAY be defined by future standards, specifications, implementation documents, or operational procedures.

Security-related documents MUST NOT contradict constitutional privacy, governance, or implementation-independence principles.

### 18.3 Not a Complete Privacy Classification System

TB-0003 does not define a complete privacy classification system.

This governance model requires privacy impact to be considered where applicable, but it does not fully define:

- privacy classification levels;
- access-control labels;
- redaction rules;
- disclosure rules;
- retention rules;
- private-source handling;
- publication boundaries;
- privacy-specific validation schemas.

A future privacy standard or specification MAY define these details.

Until then, privacy-sensitive governance decisions SHOULD remain conservative, reviewable, and traceable.

### 18.4 Not a Complete Document Template Standard

TB-0003 does not define every document template required by The Brain Standard.

This governance model identifies document types, authority levels, lifecycle states, approval expectations, ADR usage, RFC usage, supersession, deprecation, compatibility review, and change history expectations.

It does not fully define exact templates for:

- Knowledge Standards;
- Storage Standards;
- Agent Standards;
- Workflow Standards;
- Specifications;
- ADRs;
- RFCs;
- implementation documents;
- reference implementations;
- operational guides;
- SOPs;
- checklists.

Future standards or specifications MAY define stricter templates.

Those templates SHOULD conform to the governance expectations in TB-0003.

### 18.5 Not a Complete Workflow Engine Specification

TB-0003 does not define a complete workflow engine.

This governance model describes how workflows relate to governance, approval, review, drift prevention, compatibility, and authority.

It does not fully define:

- workflow execution formats;
- workflow runtime behavior;
- task scheduling;
- workflow state machines;
- automation APIs;
- orchestration systems;
- queue behavior;
- retry behavior;
- workflow-user interfaces;
- workflow storage formats.

A future Workflow Standard or Workflow Specification MAY define these details.

Workflow implementations MUST NOT treat execution mechanics as governance authority unless approved through the appropriate governance process.

### 18.6 Not a Complete Agent Standard

TB-0003 does not define a complete agent standard.

This governance model defines boundaries for agent participation in governance, but it does not fully define:

- agent roles;
- agent permissions;
- agent memory boundaries;
- agent tool access;
- agent validation procedures;
- agent review protocols;
- agent audit logs;
- agent task routing;
- agent implementation details;
- model-specific behavior.

A future Agent Standard or Agent Specification MAY define these details.

Agent behavior MUST remain subordinate to governed documents.

Agent output MUST NOT become authoritative merely because it was generated, repeated, automated, or accepted by a tool.

### 18.7 Not a Complete Storage Standard

TB-0003 does not define a complete storage standard.

This governance model discusses storage only where storage affects governance, compatibility, portability, object identity, metadata interpretation, implementation independence, or drift.

It does not fully define:

- folder structures;
- database schemas;
- file naming rules;
- storage backends;
- synchronization methods;
- backup requirements;
- export formats;
- import formats;
- archival formats;
- storage validation rules.

A future Storage Standard or Storage Specification MAY define those details.

Storage behavior MUST NOT define knowledge meaning unless that meaning is approved in the appropriate governed document.

### 18.8 Not a Complete Knowledge Model

TB-0003 does not define the complete knowledge model of The Brain Standard.

This governance model refers to Knowledge Objects, Knowledge Records, metadata, source material, object identity, compatibility, and interpretation only where they affect governance.

It does not fully define:

- Knowledge Object types;
- Knowledge Record structure;
- source extraction rules;
- relationship models;
- semantic fields;
- validation schemas;
- object lifecycle rules;
- knowledge transformation rules;
- knowledge review rules;
- knowledge import and export semantics.

A future Knowledge Standard or Knowledge Specification MAY define those details.

Knowledge-model changes SHOULD follow the governance, compatibility, approval, and review expectations defined in TB-0003.

### 18.9 Not a Complete Implementation Manual

TB-0003 does not define a complete implementation manual.

This governance model does not tell every implementation exactly how to build, store, display, synchronize, validate, or automate The Brain Standard.

Implementations MAY differ in:

- tools;
- databases;
- file systems;
- interfaces;
- programming languages;
- local folder layouts;
- search systems;
- validation systems;
- automation systems;
- user workflows.

Implementation differences are acceptable when they preserve standard meaning, compatibility, portability, privacy, reviewability, and governance boundaries.

Implementation-specific behavior MUST remain distinguishable from standard behavior.

### 18.10 Not a Personal Productivity System

TB-0003 does not define a personal productivity system.

This governance model does not control:

- personal note-taking style;
- daily planning habits;
- task management preferences;
- editor shortcuts;
- visual themes;
- personal folder convenience;
- private drafting habits;
- scratch-note organization;
- personal review rhythm.

Personal productivity practices MAY support The Brain Standard.

However, personal productivity practices MUST NOT become governed standard behavior unless documented, reviewed, and approved at the appropriate authority level.

### 18.11 Not a Tool-Specific Rulebook

TB-0003 does not define rules for one specific tool.

The Brain Standard is implementation-independent.

This governance model MUST NOT require a specific:

- editor;
- database;
- operating system;
- AI model;
- cloud service;
- file manager;
- vault application;
- plugin;
- automation tool;
- programming language.

Tool-specific guidance MAY appear in implementation documents, reference implementations, guides, or SOPs.

Tool-specific guidance MUST remain subordinate to the implementation-independent standard.

### 18.12 Not a Substitute for Judgment

TB-0003 does not eliminate the need for judgment.

Governance rules help guide review, approval, compatibility analysis, privacy analysis, supersession, deprecation, and drift prevention.

However, future humans, agents, workflows, and implementations may encounter cases that are unclear, novel, ambiguous, or not fully anticipated by this document.

When judgment is required, decisions SHOULD be guided by:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- applicable standards;
- applicable specifications;
- relevant ADRs;
- relevant RFCs;
- compatibility impact;
- privacy impact;
- practical usability;
- long-term maintainability.

Governance SHOULD support judgment, not replace it.

### 18.13 Non-Goal Discipline

Non-goals help preserve the boundaries of TB-0003.

A topic listed as a non-goal SHOULD NOT be forced into this document unless it directly affects governance, authority, compatibility, privacy, lifecycle state, approval, supersession, deprecation, or drift prevention.

If a non-goal becomes important enough to govern, it SHOULD be handled through the appropriate future document type.

Depending on scope, that may include:

- a constitutional document;
- a standard;
- a specification;
- an ADR;
- an RFC;
- an implementation document;
- a reference implementation;
- an operational document.

The governance model SHOULD remain focused on how The Brain Standard changes, not on defining every detail of the system.

## 19. Open Questions

Open questions identify unresolved governance topics that may require future clarification, ADRs, RFCs, standards, specifications, implementation documents, or operational documents.

Open questions are not approved rules.

They exist to preserve known uncertainty so that unresolved issues are not forgotten, hidden, or accidentally settled through informal practice.

An open question MAY later become:

- a clarification;
- an ADR;
- an RFC;
- a standard;
- a specification;
- an implementation document;
- a reference implementation;
- an operational document;
- a constitutional revision.

Open questions SHOULD remain visible until resolved, deferred, rejected, superseded, or incorporated into a governed document.

### 19.1 Open Question Status

Each open question SHOULD have a clear status when practical.

Recommended open question statuses include:

- Open;
- Under Review;
- Deferred;
- Resolved;
- Rejected;
- Superseded.

An Open question has not yet been answered.

An Under Review question is actively being evaluated.

A Deferred question is valid but postponed.

A Resolved question has been answered through governance or documented decision.

A Rejected question has been reviewed and determined not to require action.

A Superseded question has been replaced by a later question, ADR, RFC, or governed document.

### 19.2 Open Question Records

An open question SHOULD be recorded clearly enough for future review.

An open question record SHOULD identify:

- the question;
- why the question matters;
- what document or layer may be affected;
- what authority level may be involved;
- whether compatibility may be affected;
- whether privacy may be affected;
- whether implementation behavior may be affected;
- whether workflow behavior may be affected;
- whether agent behavior may be affected;
- what decision path may be appropriate.

Open question records SHOULD be concise.

A question that requires extensive discussion SHOULD usually become an RFC, ADR, review note, or separate governed document.

### 19.3 Governance Questions

Future governance questions MAY include:

- whether additional lifecycle states are needed;
- whether approval roles SHOULD be formally defined;
- whether formal reviewer roles should exist;
- whether approval records should follow a stricter template;
- whether governance logs should be required;
- whether change history should be mandatory for approved documents;
- whether constitutional documents should require a separate amendment process;
- whether different document authority levels need different review rules;
- whether future multi-user governance requires additional approval structure.

Governance questions SHOULD be resolved through the lowest appropriate authority level that preserves constitutional alignment.

### 19.4 Authority Questions

Future authority questions MAY include:

- whether additional authority levels are needed;
- whether more document prefixes should be defined;
- whether ADRs should have stronger or weaker authority;
- whether accepted RFCs should have a defined transition period;
- whether implementation profiles require their own authority category;
- whether privacy standards require special authority handling;
- whether validation specifications require stricter authority rules.

Authority questions SHOULD be reviewed carefully because they affect conflict resolution and document interpretation.

### 19.5 Compatibility Questions

Future compatibility questions MAY include:

- how long older versions should remain supported;
- when migration guidance becomes mandatory;
- how breaking changes should be classified;
- whether compatibility categories should be formally defined;
- whether backward compatibility should be measured by document validity, implementation compliance, or knowledge interpretability;
- how compatibility should be tested by agents, workflows, validators, or implementations;
- whether compatibility review should require a separate record for major changes.

Compatibility questions SHOULD be resolved before changes that may affect existing knowledge, documents, workflows, agents, or implementations.

### 19.6 Privacy Questions

Future privacy questions MAY include:

- whether privacy classification levels should be standardized;
- whether access-control metadata should be required;
- whether privacy-impact review should use a required checklist;
- whether redaction rules should be defined;
- whether agent access should be governed by privacy class;
- whether governance records may reference restricted source material;
- whether public and private versions of governance records should be supported.

Privacy questions SHOULD be handled conservatively.

When privacy impact is unclear, governance SHOULD avoid exposing restricted information until a safer rule is approved.

### 19.7 Agent Questions

Future agent questions MAY include:

- what roles agents may perform;
- what governance actions agents may recommend;
- what governance actions agents may execute;
- what human review is required for agent-generated changes;
- how agent permissions should be represented;
- how agent audit trails should be preserved;
- how agents should detect governance drift;
- how agents should distinguish drafts, proposals, approved rules, examples, and historical records.

Agent questions SHOULD preserve the principle that agents may assist governance but do not become governance authorities by default.

### 19.8 Workflow Questions

Future workflow questions MAY include:

- how governance workflows should be represented;
- whether workflow states should be standardized;
- whether approval workflows should require human confirmation;
- how workflow outputs should be recorded;
- how workflow failures should be handled;
- how workflow automation should interact with privacy rules;
- how workflow completion should be distinguished from governance approval;
- whether workflow templates should be governed as specifications, implementation documents, or operational documents.

Workflow questions SHOULD preserve reviewability, traceability, and authority boundaries.

### 19.9 Implementation Questions

Future implementation questions MAY include:

- whether implementation profiles should be standardized;
- whether reference implementations should use a common template;
- whether validators should be required for compliance claims;
- whether implementation conformance levels should exist;
- whether import and export behavior should be tested;
- whether tool-specific limitations should be documented in implementation records;
- whether implementation-specific metadata should be allowed;
- how implementation behavior should be separated from standard behavior.

Implementation questions SHOULD preserve implementation independence.

No implementation question SHOULD be resolved in a way that makes one tool, vault, database, workflow engine, AI model, or interface the standard by default.

### 19.10 Storage Questions

Future storage questions MAY include:

- whether a recommended vault structure should be defined;
- whether file naming should be standardized;
- whether folder naming should be standardized;
- whether database-backed implementations require specific portability rules;
- whether export formats should be mandatory;
- whether backup expectations should be governed;
- whether storage validation should be defined by specification;
- whether storage paths may carry meaning.

Storage questions SHOULD preserve the principle that storage must not define knowledge meaning unless that meaning is explicitly approved in the appropriate governed document.

### 19.11 Knowledge Model Questions

Future knowledge model questions MAY include:

- how Knowledge Objects should be defined;
- how Knowledge Records should be defined;
- how source material should be linked;
- how object identity should be assigned;
- how relationships should be represented;
- how metadata should be structured;
- how knowledge review should work;
- how knowledge transformation should be recorded;
- how human-readable and AI-readable structures should be balanced.

Knowledge model questions SHOULD be resolved through future knowledge standards and specifications rather than through governance text alone.

### 19.12 Resolving Open Questions

An open question SHOULD be resolved through the appropriate governance path.

Resolution MAY occur through:

- direct clarification in a governed document;
- an ADR;
- an RFC;
- a standard;
- a specification;
- an implementation document;
- a reference implementation;
- an operational document;
- a constitutional revision.

Resolution SHOULD identify:

- what question was resolved;
- what answer was accepted;
- what document was updated;
- what authority level applies;
- whether compatibility is affected;
- whether privacy is affected;
- whether migration is required;
- whether future review is needed.

A resolved open question SHOULD NOT remain ambiguous.

### 19.13 Open Question Practicality

Open questions SHOULD remain practical.

The Brain Standard SHOULD NOT accumulate unresolved questions that no longer matter.

Open questions SHOULD be reviewed, resolved, deferred, rejected, or superseded when they stop being useful.

An open question is useful when it preserves meaningful uncertainty for future governance.

An open question is not useful when it creates noise, duplicates an already resolved issue, or avoids making a decision that SHOULD be made.

The purpose of open questions is to preserve reviewable uncertainty, not to delay necessary governance decisions indefinitely.

## 20. Final Governance Statement

The governance model defined by TB-0003 exists to preserve The Brain Standard as it changes over time.

The Brain Standard is intended to remain durable, portable, reviewable, implementation-independent, human-readable, AI-readable, and trustworthy across long periods of technological change.

Governance is the mechanism that prevents that standard from drifting accidentally.

Governance does not exist to make change impossible.

Governance exists to make change deliberate.

A governed standard can evolve without losing its foundation.

A governed standard can improve without allowing tools, workflows, agents, implementations, habits, or convenience to redefine its meaning informally.

TB-0003 establishes that changes to The Brain Standard SHOULD be:

- explicit;
- reviewable;
- traceable;
- compatible where practical;
- privacy-preserving;
- authority-aware;
- implementation-independent;
- proportional to risk;
- practical for daily use.

The constitutional foundation SHALL guide governance interpretation.

Lower-authority documents MAY add detail, examples, workflows, specifications, implementation guidance, and operational procedures.

Lower-authority documents MUST NOT override higher-authority documents.

Drafts, RFCs, examples, reference implementations, operational habits, workflow outputs, and agent suggestions MUST NOT become authoritative merely because they exist, are repeated, are automated, or are useful.

Approved governed documents define current authority.

Historical records preserve why authority changed.

Supersession and deprecation preserve continuity.

Compatibility review protects existing knowledge.

Privacy review protects restricted knowledge.

Approval records and change history preserve trust.

Open questions preserve unresolved uncertainty without allowing uncertainty to become hidden architecture.

The success of this governance model depends on balance.

Too little governance allows drift.

Too much governance makes the standard difficult to use.

The correct governance model preserves architectural discipline while allowing practical improvement.

TB-0003 SHOULD be interpreted in service of the larger purpose defined by TB-0000, the principles defined by TB-0001, and the layered architecture defined by TB-0002.

The final governance rule is this:

The Brain Standard SHOULD change only when change improves the standard, and that change SHOULD remain understandable to future humans, agents, workflows, validators, and implementations.
