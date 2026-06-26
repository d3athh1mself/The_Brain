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

A constitutional change SHOULD include documented rationale, compatibility review, impact review, and approval.

Changes to constitutional documents affect the entire standard and SHOULD be made only when the change materially improves clarity, correctness, durability, portability, governance, or long-term architectural coherence.

A constitutional change SHOULD include documented rationale, compatibility review, and approval.

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

An RFC is not an approved standard unless it is accepted through the appropriate governance process.

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

A conflict SHOULD be resolved by:

1. identifying the conflicting documents;
2. identifying the authority level of each document;
3. determining whether the conflict is real or only interpretive;
4. applying the higher-authority document;
5. revising the lower-authority document if needed;
6. recording the decision through an ADR, RFC, revision, or supersession when appropriate.

If the higher-authority document is unclear, incomplete, or outdated, the issue SHOULD be handled through governance rather than bypassed through implementation behavior, workflow convenience, agent output, or informal practice.
