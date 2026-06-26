# TB-0001 — Architecture Principles

Document ID: TB-0001
Title: Architecture Principles
Version: 0.1.0
Status: Approved
Created: 2026-06-25
Last Updated: 2026-06-25
Authority: Constitutional
Phase: Phase 0 — Architecture
Milestone: 0.2 — Architecture Principles
Depends On: TB-0000 — Vision and Purpose
Supersedes: None
Superseded By: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and architectural rules are interpreted within TB-0001.

Where conflicts arise between architectural principles, dependencies, implementations, workflows, or future specifications, the architectural principles defined in TB-0001 SHALL guide interpretation and resolution.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Implementation refers to any software, workflow, vault, database, application, agent system, or interface that creates, reads, validates, modifies, or presents knowledge according to The Brain Standard.
- Reference Implementation refers to an example implementation that demonstrates the standard without becoming the standard itself.
- Architecture Principle refers to a rule or guiding constraint used to evaluate, design, extend, or reject standards, implementations, workflows, and tools.
- Architectural Trade-Off refers to a decision where two or more desirable goals conflict and priority must be assigned.

## 1. Purpose

The purpose of TB-0001 is to define the foundational architecture principles of The Brain Standard.

TB-0000 establishes the mission, vision, scope, philosophy, objectives, non-goals, and authority hierarchy of The Brain. TB-0001 translates that constitutional foundation into enforceable architectural principles that guide all future standards, specifications, implementations, workflows, agent behavior, and governance decisions.

These principles exist to ensure that The Brain remains:

- implementation-independent;
- durable across technological change;
- readable by both humans and AI systems;
- portable across tools and storage systems;
- extensible without architectural fragmentation;
- trustworthy through provenance, lifecycle, and governance;
- practical for daily use.

TB-0001 does not define detailed schemas, file layouts, object models, agent protocols, workflow engines, or implementation requirements. Those concerns belong to lower-level standards and specifications.

Instead, TB-0001 defines the rules by which those future documents shall be evaluated.
A lower-authority document is compliant only if it preserves the architectural intent expressed in TB-0000 and the principles defined in TB-0001.

## 2. Relationship to TB-0000

TB-0001 is subordinate to and derived from TB-0000.
TB-0000 defines The Brain as an implementation-independent knowledge architecture whose primary purpose is to preserve, organize, and evolve knowledge over time. TB-0001 extends that foundation by defining the principles that future standards and implementations must follow.

TB-0001 must not contradict TB-0000.

Where TB-0000 defines the constitutional vision of The Brain, TB-0001 defines the architectural discipline required to preserve that vision during design, implementation, extension, and governance.

In practical terms:

- TB-0000 answers: Why does The Brain exist?
- TB-0001 answers: What principles must The Brain follow?
- Later standards answer: How must specific parts of The Brain work?
- Specifications answer: What exact structures, schemas, and formats are required?
- Implementations answer: How can the standard be realized in software or workflows?

If a future standard, specification, implementation, workflow, or automation conflicts with TB-0001, it must either be revised, formally justified through governance, or rejected.
If TB-0001 appears to conflict with TB-0000, TB-0000 takes precedence.

## 3. Principle Categories

TB-0001 organizes architecture principles into categories used to evaluate future standards, specifications, implementations, workflows, and agents.
These categories are derived from TB-0000 but do not restate its full philosophy.
The principle categories are:

### 3.1 Knowledge Integrity

Ensures knowledge retains its meaning, identity, context, and trustworthiness over time.
    
### 3.2 Implementation Independence

Ensures The Brain Standard remains separate from any specific application, vendor, interface, database, AI model, or storage provider.
    
### 3.3 Portability and Durability

Ensures knowledge can survive migration, reorganization, technological change, and replacement of tools.

### 3.4 Human and AI Usability

Ensures knowledge remains understandable to humans while also being structured enough for reliable AI interpretation and automation.

### 3.5 Explicit Structure

Ensures important meaning is represented through clear metadata, relationships, lifecycle states, provenance, and governed standards rather than hidden assumptions.

### 3.6 Governed Evolution

Ensures the standard changes through documented decisions, versioning, compatibility rules, ADRs, RFCs, and approval processes.

### 3.7 Practical Usability

Ensures the architecture remains usable in daily life and does not become too complex, burdensome, or theoretical.

## 4. Required Architecture Principles

Required architecture principles are mandatory rules that all lower-authority standards, specifications, workflows, agents, and implementations must follow unless formally superseded by a higher-authority document.

A design, implementation, workflow, or automation that violates a required architecture principle is non-compliant unless the violation is explicitly approved through governance.

### 4.1 Knowledge Meaning Must Be Preserved

The meaning of a Knowledge Object SHALL be preserved across storage systems, implementations, workflows, migrations, exports, imports, and automation processes.
No implementation, agent, workflow, or storage mechanism may alter the meaning of knowledge without making that change explicit, reviewable, and traceable.
Knowledge may be reformatted, indexed, summarized, linked, or transformed only if its original meaning remains recoverable or the change is recorded as a deliberate revision.

### 4.2 Object Identity Must Be Stable

Each Knowledge Object SHALL have a stable identity that is independent of its filename, folder path, display title, storage location, database identifier, or application-specific reference.
A Knowledge Object may be renamed, moved, reorganized, copied, migrated, or presented differently without losing its identity.
Stable identity is required so that relationships, citations, provenance, workflows, and automation do not break when storage or presentation changes.

### 4.3 Storage Must Not Define Meaning

Storage structure SHALL NOT be the primary source of meaning for Knowledge Objects.
Folders, filenames, vault locations, databases, URLs, tags, indexes, and application views may assist organization, discovery, or presentation, but they MUST NOT be the only place where critical meaning is defined.
Critical meaning SHOULD be represented through explicit metadata, object identity, relationships, provenance, lifecycle state, and governed standards.

### 4.4 Implementations Must Be Replaceable

The Brain Standard SHALL remain independent of any specific implementation.
No application, vault system, database, AI model, plugin, operating system, cloud service, local tool, or interface may become required for the knowledge itself to remain understandable and usable.
Reference implementations may demonstrate the standard, but they MUST NOT define or limit the standard.

### 4.5 Source Material Must Remain Distinguishable from Knowledge Records

Original source material SHALL remain distinguishable from Knowledge Records created from, about, or in response to that source material.
A source file, document, image, recording, web page, message, dataset, or other artifact may serve as evidence, input, or reference material, but it is not automatically the same thing as a Knowledge Object.
Knowledge Records SHOULD preserve references to relevant source material when that source materially supports the record.

### 4.6 Critical Meaning Must Be Explicit

Critical meaning SHALL be represented explicitly.

This includes, where applicable:

- object identity;
- object type;
- title or human-readable label;
- relationships;
- source references;
- provenance;
- lifecycle state;
- authority level;
- privacy classification;
- version or revision state.

Implicit conventions may be used for convenience, but they MUST NOT be the only source of meaning for critical architecture behavior.

### 4.7 Human Review Must Remain Available

The Brain Standard SHALL preserve the ability for humans to review, understand, correct, approve, reject, or supersede knowledge.
Agents and automation may assist with capture, transformation, classification, linking, summarization, validation, and workflow execution, but they MUST NOT become unreviewable authorities.
Where automation changes knowledge, the change SHOULD be traceable to the responsible workflow, agent, rule, or human approval.

### 4.8 Privacy Boundaries Must Be Preserved

Knowledge architecture SHALL preserve privacy boundaries.
Private, internal, confidential, sensitive, or restricted knowledge MUST NOT be exposed, exported, published, synchronized, or shared merely because it exists within the same implementation, vault, repository, database, or workflow system as less restricted knowledge.
Privacy classification SHOULD be explicit enough that future workflows, agents, repositories, and implementations can respect it.

### 4.9 Governance Decisions Must Be Recorded

Major architectural decisions SHALL be recorded through governed documents such as standards, specifications, ADRs, RFCs, or approved constitutional documents.

A decision SHOULD be recorded when it:

- changes the meaning of the standard;
- introduces or removes a required rule;
- affects compatibility;
- changes object identity, storage, metadata, lifecycle, privacy, or governance behavior;
- creates a new authority level;
- supersedes a previous decision;
- creates a new implementation expectation.

Undocumented practice MUST NOT become architecture by accident.

### 4.10 Daily Use Must Remain Practical

The Brain Standard SHALL remain practical for routine use.
Required structure, metadata, governance, workflows, and validation rules MUST NOT create unnecessary cognitive burden.
A requirement is justified only if it materially improves durability, portability, interoperability, trustworthiness, automation reliability, or long-term maintainability.
Architecture that is technically correct but too burdensome to use consistently is not acceptable.

## 5. Recommended Architecture Principles

Recommended architecture principles are strong design preferences. They should be followed unless there is a clear reason not to.
A lower-authority document may deviate from a recommended principle, but the reason for deviation SHOULD be documented when the decision affects long-term architecture, compatibility, governance, or implementation behavior.

### 5.1 Prefer Open and Durable Formats

Knowledge SHOULD be representable using open, documented, durable, and human-inspectable formats.
Plain text and Markdown-compatible formats are preferred where practical because they support long-term readability, portability, version control, and AI interpretation.
Proprietary formats MAY be used for source material or implementation-specific functionality, but they SHOULD NOT be the only representation of core knowledge.

### 5.2 Prefer Minimal Required Metadata

The Brain Standard SHOULD require only the metadata necessary for identity, interpretation, governance, portability, and trustworthy use.
Additional metadata may be recommended, optional, derived, or automation-generated.
The standard SHOULD avoid making daily capture difficult by requiring excessive manual metadata entry.

### 5.3 Prefer Separation of Concerns

The architecture SHOULD separate distinct responsibilities instead of combining them into fragile structures.

At minimum, the following concerns SHOULD remain separable:

- identity;
- storage;
- presentation;
- source material;
- knowledge records;
- metadata;
- relationships;
- lifecycle;
- privacy;
- implementation behavior;
- governance.

This separation allows the system to evolve without forcing unrelated parts of the architecture to change together.

### 5.4 Prefer Explicit Relationships Over Duplication

Knowledge SHOULD be connected through stable references and explicit relationships rather than copied repeatedly across the system.
Duplication may be acceptable for readability, summaries, exports, backups, or implementation convenience, but authoritative meaning SHOULD remain traceable to the appropriate Knowledge Object or source.

### 5.5 Prefer Local-First Compatibility

A compliant implementation SHOULD be capable of functioning locally without requiring internet connectivity, cloud services, proprietary accounts, or external AI providers.
Cloud services, synchronization systems, hosted databases, and online AI systems may extend functionality, but they SHOULD NOT be required for basic access, interpretation, or preservation of knowledge.

### 5.6 Prefer Backward Compatibility

The Brain Standard SHOULD evolve in a way that preserves backward compatibility whenever reasonably possible.
When breaking changes are necessary, they SHOULD be documented, versioned, justified, and accompanied by migration guidance.

### 5.7 Prefer Automation That Reduces Cognitive Load

Automation SHOULD reduce the burden of capturing, organizing, validating, and maintaining knowledge.
Automation SHOULD NOT increase confusion, hide important decisions, create unreviewable changes, or require users to understand unnecessary implementation details.
The purpose of automation is to support human stewardship, not replace it.

## 6. Trade-Off Resolution Rules

Trade-off resolution rules define how decisions should be made when two or more architecture goals conflict.
These rules apply to standards, specifications, implementations, workflows, agents, governance decisions, and future revisions of The Brain Standard.

### 6.1 Knowledge Integrity Over Implementation Convenience

When knowledge integrity conflicts with implementation convenience, knowledge integrity SHALL take precedence.
An implementation may be made easier to build, operate, or automate only if doing so does not weaken the meaning, identity, provenance, portability, or trustworthiness of knowledge.

### 6.2 Portability Over Vendor Optimization

When portability conflicts with vendor-specific features, portability SHALL take precedence.
Vendor-specific capabilities may be supported as extensions, but they MUST NOT become required for preserving, interpreting, or migrating knowledge.

### 6.3 Explicit Meaning Over Hidden Convention

When explicit meaning conflicts with hidden convention, explicit meaning SHALL take precedence.
Folders, filenames, visual layouts, application states, plugin behavior, and undocumented habits may support usability, but they MUST NOT replace explicit architecture where critical meaning is required.

### 6.4 Human Understandability Over Automation Efficiency

When automation efficiency conflicts with human understandability, human understandability SHALL take precedence.
Automation may optimize workflows, classification, linking, and validation, but it MUST NOT make the knowledge system opaque to human review.

### 6.5 Simplicity Over Premature Completeness

When simplicity conflicts with premature completeness, simplicity SHOULD take precedence.
The Brain Standard should not attempt to solve every future use case before the architecture has proven useful in daily operation.
Extensions should be added when justified by durable architectural value, not theoretical possibility alone.

### 6.6 Governance Over Informal Drift

When informal practice conflicts with documented governance, documented governance SHALL take precedence.
Repeated behavior, tool defaults, personal habits, or implementation shortcuts do not become part of The Brain Standard unless formally documented and approved through the appropriate authority level.

### 6.7 Privacy Over Operational Convenience

When privacy boundaries conflict with operational convenience, privacy SHALL take precedence.
It is better for a workflow, repository, export, sync process, or automation to require additional review than to risk exposing restricted knowledge.

### 6.8 Daily Usability Over Theoretical Purity

When theoretical architectural purity conflicts with daily usability, daily usability SHOULD be strongly considered.
A standard that users cannot realistically follow will fail even if it is conceptually elegant.
However, usability improvements MUST NOT violate required principles unless formally approved through governance.

## 7. Compliance Expectations

Compliance expectations define how future documents, implementations, workflows, agents, and tools are evaluated against TB-0001.
Compliance with TB-0001 does not require that every implementation look the same, use the same software, store data in the same way, or expose the same interface. Compliance requires that the architectural meaning, constraints, and principles of The Brain Standard are preserved.

### 7.1 Compliant Documents

A document is compliant with TB-0001 when it:

- does not contradict TB-0000 or TB-0001;
- uses normative language consistently;
- preserves implementation independence;
- respects the document authority hierarchy;
- defines its scope clearly;
- avoids creating hidden architectural requirements;
- records major architectural decisions through the appropriate governance mechanism;
- does not redefine terms, principles, or authority levels without formal approval.

A lower-authority document MAY add detail, constraints, examples, schemas, templates, or implementation guidance, but it MUST NOT override a higher-authority document.

### 7.2 Compliant Implementations

An implementation is compliant with TB-0001 when it can create, read, preserve, and manage knowledge without violating the required architecture principles.

A compliant implementation MUST preserve:

- stable object identity;
- knowledge meaning;
- explicit critical metadata;
- source distinction;
- privacy boundaries;
- human review capability;
- portability of knowledge;
- separation between the standard and implementation-specific behavior.

An implementation MAY add features, interfaces, automations, plugins, databases, indexes, or visualizations, provided those additions do not become required for the knowledge itself to remain understandable and usable.

### 7.3 Compliant Workflows

A workflow is compliant with TB-0001 when it supports the capture, transformation, review, movement, publication, synchronization, or maintenance of knowledge without weakening the principles of the standard.

A compliant workflow SHOULD make clear:

- what input it uses;
- what output it creates;
- whether it changes existing knowledge;
- whether human review is required;
- what source material supports the result;
- what privacy boundaries apply;
- what lifecycle state applies after the workflow completes.

Workflows that alter knowledge SHOULD make the change traceable.

### 7.4 Compliant Agents

An agent is compliant with TB-0001 when it operates within defined architectural boundaries and does not become an unreviewable authority over knowledge.
A compliant agent MUST NOT silently alter the meaning, identity, provenance, privacy classification, lifecycle state, or authority level of a Knowledge Object.

An agent MAY assist with:

- ingestion;
- classification;
- summarization;
- metadata extraction;
- linking;
- validation;
- duplicate detection;
- workflow execution;
- drafting;
- review preparation.

Agent-created or agent-modified knowledge SHOULD remain traceable to the agent, workflow, instruction, source material, and review state involved.

### 7.5 Compliance Levels

The Brain Standard recognizes three general compliance levels for future evaluation.

#### 7.5.1 Compliant

A document, implementation, workflow, or agent is compliant when it satisfies all applicable required principles and does not contradict TB-0000 or TB-0001.

#### 7.5.2 Partially Compliant

A document, implementation, workflow, or agent is partially compliant when it follows the intent of TB-0001 but lacks one or more required capabilities, safeguards, or documentation elements.
Partial compliance SHOULD identify the missing or incomplete areas.

#### 7.5.3 Non-Compliant

A document, implementation, workflow, or agent is non-compliant when it violates one or more required architecture principles without formal approval.
A non-compliant design SHOULD be revised, rejected, isolated as experimental, or documented as intentionally outside The Brain Standard.

### 7.6 Experimental Exceptions

Experimental work MAY temporarily deviate from TB-0001 if it is clearly marked as experimental and does not redefine the standard.
Experimental exceptions MUST NOT be treated as approved architecture unless later accepted through governance.

## 8. Architectural Anti-Patterns

Architectural anti-patterns are design choices that appear useful in the short term but weaken the long-term integrity, portability, maintainability, or trustworthiness of The Brain Standard.
Anti-patterns SHOULD be avoided in standards, specifications, implementations, workflows, agents, and operational practices.

### 8.1 Application-Centric Architecture

Application-centric architecture occurs when the behavior, structure, or limitations of a specific tool become treated as the architecture itself.
Examples include designing the standard around a specific note-taking app, database, plugin system, AI provider, sync service, or user interface.
This is an anti-pattern because implementations are replaceable. The standard must outlive them.

### 8.2 Folder-Defined Meaning

Folder-defined meaning occurs when critical knowledge meaning exists only in the folder path, vault location, or file placement of an object.
Folders may support organization, but they MUST NOT be the sole source of object type, authority, lifecycle state, privacy class, or relationship meaning.

### 8.3 Filename-Dependent Identity

Filename-dependent identity occurs when a Knowledge Object is identified only by its filename or display title.
This is an anti-pattern because filenames and titles are presentation concerns. They may change over time.
Stable identity must survive renaming, moving, migration, and reorganization.

### 8.4 Hidden Metadata

Hidden metadata occurs when important meaning is stored only in application state, plugin data, database internals, caches, indexes, or undocumented conventions.
This is an anti-pattern because hidden meaning is difficult to inspect, migrate, validate, preserve, or interpret outside the original implementation.

### 8.5 Automation Without Review

Automation without review occurs when agents or workflows change knowledge in ways that cannot be inspected, reversed, approved, rejected, or traced.
This is an anti-pattern because The Brain depends on trustworthy human stewardship.
Automation may assist knowledge work, but it must not remove accountability.

### 8.6 Source Confusion

Source confusion occurs when original source material and Knowledge Records are treated as the same thing.
This is an anti-pattern because sources serve as evidence, while Knowledge Records represent structured interpretation, summary, extraction, analysis, or organization.
The system must preserve the distinction between source artifacts and knowledge derived from them.

### 8.7 Privacy Leakage by Architecture

Privacy leakage by architecture occurs when restricted knowledge can be exposed because privacy boundaries depend only on user memory, folder placement, repository habits, or manual caution.
This is an anti-pattern because privacy protection should be represented explicitly enough that workflows, agents, and implementations can respect it.

### 8.8 Governance by Habit

Governance by habit occurs when repeated behavior becomes treated as an official standard without being documented, reviewed, or approved.
This is an anti-pattern because undocumented decisions are difficult to challenge, revise, supersede, or explain later.

### 8.9 Excessive Required Structure

Excessive required structure occurs when the standard demands more metadata, classification, workflow steps, or governance than users can realistically maintain.
This is an anti-pattern because a system that is too burdensome will become inconsistent or abandoned.

### 8.10 Premature Optimization for Scale

Premature optimization for scale occurs when the architecture becomes unnecessarily complex in order to solve future large-scale problems before basic use has been proven.
The Brain should remain compatible with future scale, but early standards should not sacrifice daily usability for theoretical completeness.

## 9. Review Checklist

The review checklist provides a practical test for evaluating future standards, specifications, workflows, agents, and implementations against TB-0001.
A proposal SHOULD be reviewed against this checklist before it is approved as part of The Brain Standard.

### 9.1 Constitutional Alignment

- Does the proposal align with TB-0000?
- Does it preserve the purpose of The Brain as an implementation-independent Knowledge Operating System?
- Does it avoid contradicting higher-authority documents?
- Does it respect the document authority hierarchy?

### 9.2 Knowledge Integrity

- Does the proposal preserve knowledge meaning?
- Does it preserve stable object identity?
- Does it distinguish source material from Knowledge Records?
- Does it preserve provenance, context, lifecycle, and authority where applicable?

### 9.3 Implementation Independence

- Does the proposal avoid depending on a specific application, vendor, AI model, database, cloud service, or interface?
- If implementation-specific behavior is included, is it clearly marked as implementation-specific?
- Could another implementation satisfy the same standard differently?

### 9.4 Portability and Durability

- Can the knowledge survive migration to another tool or storage system?
- Are critical meanings represented outside hidden application state?
- Are open, documented, durable, or inspectable formats preferred where practical?

### 9.5 Human and AI Usability

- Can a human inspect and understand the knowledge without specialized software?
- Is the structure clear enough for AI systems to interpret reliably?
- Does automation preserve human review and correction?

### 9.6 Explicit Structure

- Are critical meanings explicit?
- Are relationships, metadata, lifecycle states, privacy classifications, and source references defined where needed?
- Does the proposal avoid relying only on folders, filenames, tags, or unstated conventions?

### 9.7 Privacy and Security

- Are privacy boundaries preserved?
- Could restricted knowledge be accidentally exported, published, synced, indexed, or exposed?
- Are privacy classifications explicit enough for future workflows and agents to respect?

### 9.8 Governance

- Does the proposal require an ADR, RFC, standard, specification, or other governed document?
- Does it introduce a new rule, object type, metadata requirement, workflow expectation, or compatibility concern?
- Does it supersede or modify an earlier decision?

### 9.9 Practical Usability

- Is the proposal practical for routine use?
- Does it reduce or increase cognitive load?
- Is the required structure justified by long-term value?
- Could the same goal be achieved with a simpler design?

### 9.10 Final Review Question

Before approval, every major proposal SHOULD answer the following question:
Does this strengthen the long-term durability, portability, trustworthiness, and usability of knowledge without creating unnecessary dependency, complexity, or risk?

## 10. Success Criteria

TB-0001 shall be considered successful when it provides a clear and usable decision framework for The Brain Standard.
The success of TB-0001 is not measured by theoretical completeness. It is measured by whether future documents, implementations, workflows, agents, and governance decisions can use it to make consistent architectural decisions.

### 10.1 Clear Decision Guidance

TB-0001 succeeds when future contributors can use it to determine whether a proposed design aligns with The Brain Standard.
A successful principle should help approve, revise, defer, or reject a proposal.

### 10.2 Reduced Architectural Drift

TB-0001 succeeds when it prevents implementations, workflows, tools, or habits from redefining the standard accidentally.
The standard should evolve through documented decisions rather than informal drift.

### 10.3 Preserved Implementation Independence

TB-0001 succeeds when The Brain can support multiple implementations without making any one implementation canonical.
Tools may differ, but the knowledge must remain portable and interpretable.

### 10.4 Stronger Knowledge Integrity

TB-0001 succeeds when knowledge meaning, identity, context, source references, lifecycle state, and privacy boundaries remain stable across workflows and implementations.

### 10.5 Practical Daily Use

TB-0001 succeeds when its principles improve architecture without making the system too burdensome to use.
A principle that cannot be followed consistently in real use should be revised, clarified, or moved to a lower-authority document.

### 10.6 Useful Review Standard

TB-0001 succeeds when it can be used as a checklist for reviewing future standards, specifications, implementations, workflows, and agents.
The document should make architectural review more consistent and less subjective.

### 10.7 Compatibility with Future Growth

TB-0001 succeeds when it supports the early single-user system while leaving room for future multi-user, organizational, agent-driven, and large-scale implementations.
The principles should guide growth without forcing premature complexity.
