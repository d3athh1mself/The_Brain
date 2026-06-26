# TB-0002 — Layered Architecture

Document ID: TB-0002
Title: Layered Architecture
Version: 0.1.0
Status: Draft
Created: 2026-06-25
Last Updated: 2026-06-25
Authority: Constitutional
Phase: Phase 0 — Architecture
Milestone: 0.3 — Layered Architecture
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles
Supersedes: None
Superseded By: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and architectural rules are interpreted within TB-0002.

Where conflicts arise between layers, dependencies, implementations, workflows, or future specifications, the architectural principles defined in TB-0001 SHALL guide interpretation and resolution.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Constitutional Foundation refers to the highest-authority architectural documents that define the purpose, principles, and governing structure of The Brain Standard.
- Operational Architecture refers to the layered model through which The Brain Standard is organized into functional areas.
- Layer refers to a distinct architectural responsibility within The Brain Standard.
- Universal Knowledge Standard refers to the layer responsible for defining knowledge objects, metadata, relationships, semantics, lifecycle, and meaning.
- Storage Standard refers to the layer responsible for defining how knowledge and source material may be stored, organized, referenced, moved, and preserved without defining meaning.
- Agent Framework refers to the layer responsible for defining how agents may interact with knowledge while preserving reviewability, traceability, privacy, and governance.
- Workflow Engine refers to the layer responsible for defining repeatable processes that coordinate capture, transformation, validation, review, publication, maintenance, and automation.
- Implementation refers to any software, vault, database, file system, interface, agent system, or workflow environment that realizes The Brain Standard in practice.
- Dependency means a relationship in which one layer, document, specification, workflow, or implementation relies on another for authority, structure, or interpretation.
- Cross-Layer Rule refers to a rule that governs how two or more architectural layers interact.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to source material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, or other artifacts used as evidence, input, or reference material.
- Reference Implementation refers to an example implementation that demonstrates The Brain Standard without becoming the standard itself.

## 1. Purpose

The purpose of TB-0002 is to define the layered architecture of The Brain Standard.

TB-0000 establishes the vision and purpose of The Brain. TB-0001 establishes the architecture principles that govern future decisions. TB-0002 defines how the major architectural responsibilities of The Brain are organized into layers so that future standards, specifications, workflows, agents, and implementations can be designed without confusion about authority, dependency, or responsibility.

The layered architecture exists to ensure that The Brain remains:

- implementation-independent;
- modular;
- extensible;
- portable across storage systems and tools;
- understandable to humans and AI systems;
- governed by clear architectural boundaries;
- practical for daily use.

TB-0002 does not define detailed schemas, object fields, folder layouts, agent protocols, workflow procedures, or implementation-specific behavior. Those details belong to lower-level standards, specifications, implementation documents, and operational guides.

Instead, TB-0002 defines the architectural model that explains where those future documents belong and how they relate to each other.

The primary purpose of the layered architecture is to prevent architectural confusion. Each layer has a distinct responsibility. Lower layers define stable knowledge meaning and storage expectations. Higher layers define automation, workflows, and practical implementations that depend on the lower layers without redefining them.

## 2. Relationship to TB-0000 and TB-0001

TB-0002 is subordinate to and derived from TB-0000 and TB-0001.

TB-0000 defines The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time. TB-0001 defines the architecture principles that future documents, workflows, agents, and implementations must follow.

TB-0002 applies those principles by organizing The Brain Standard into a layered model.

In practical terms:

- TB-0000 answers: Why does The Brain exist?
- TB-0001 answers: What principles must The Brain follow?
- TB-0002 answers: How are the major architectural responsibilities organized?
- Later standards answer: What rules govern each layer?
- Specifications answer: What exact structures, schemas, and formats are required?
- Implementations answer: How can the standard be realized in software, files, databases, workflows, or interfaces?

TB-0002 must not contradict TB-0000 or TB-0001.

If a future layer-specific standard conflicts with TB-0002, it must be revised, formally justified through governance, or rejected. If TB-0002 appears to conflict with TB-0000 or TB-0001, the higher-authority document takes precedence.

TB-0002 does not replace the authority hierarchy defined in TB-0000. Instead, it provides an architectural organization model that helps determine where future standards and specifications belong.

## 3. Architectural Foundation

The Brain Standard is built on a constitutional foundation and an operational architecture.

The constitutional foundation consists of the highest-authority documents that define the purpose, principles, and governing structure of The Brain Standard. These documents include TB-0000, TB-0001, TB-0002, and other future TB-series constitutional documents.

The operational architecture consists of the functional layers that define how knowledge is represented, stored, acted on by agents, processed through workflows, and realized in implementations.

The constitutional foundation governs the operational architecture. It is not itself one of the five operational layers.

The five operational layers are:

1. Layer 1 — Universal Knowledge Standard
2. Layer 2 — Storage Standard
3. Layer 3 — Agent Framework
4. Layer 4 — Workflow Engine
5. Layer 5 — Implementations

Each operational layer has a distinct responsibility.

- Layer 1 defines the meaning of knowledge.
- Layer 2 defines how knowledge and source material may be stored without allowing storage to define meaning.
- Layer 3 defines how agents may interact with knowledge while preserving reviewability, traceability, privacy, and governance.
- Layer 4 defines repeatable workflows that coordinate knowledge capture, transformation, validation, review, maintenance, and publication.
- Layer 5 defines practical implementations that realize the standard through software, vaults, databases, interfaces, tools, automations, or operating environments.

The layered architecture SHALL preserve the distinction between constitutional authority and operational function.

Constitutional documents define what the system is and what it must preserve. Operational layers define how the system is organized and eventually implemented.

## 4. Layer Model Overview

The Brain Standard is organized into five operational layers.

These layers define the major architectural responsibilities required for a durable, portable, implementation-independent Knowledge Operating System.

The five operational layers are:

1. Layer 1 — Universal Knowledge Standard
2. Layer 2 — Storage Standard
3. Layer 3 — Agent Framework
4. Layer 4 — Workflow Engine
5. Layer 5 — Implementations

Each layer has a distinct responsibility, but no layer exists in isolation. The layers are designed to work together while preserving clear boundaries between meaning, storage, automation, workflow, and implementation.

- Layer 1 defines the meaning and structure of knowledge.
- Layer 2 defines how knowledge and source material may be stored, organized, referenced, and preserved.
- Layer 3 defines how agents may interact with knowledge, source material, metadata, storage structures, and workflow instructions while preserving architectural boundaries.
- Layer 4 defines repeatable workflows that coordinate activities across knowledge, storage, agents, review, maintenance, and publication.
- Layer 5 defines practical implementations that realize the standard through software, vaults, databases, file systems, interfaces, tools, automations, and operating environments.

The layers are ordered by architectural dependency.

Higher layers may depend on lower layers, but lower layers MUST NOT depend on higher layers.

For example:

- An implementation may depend on workflow rules, agent rules, storage rules, and knowledge rules.
- A workflow may depend on agent behavior, storage rules, and knowledge rules.
- An agent may depend on storage and knowledge standards.
- Storage may depend on knowledge identity and metadata requirements.
- Knowledge meaning must remain valid even if storage systems, agents, workflows, or implementations are replaced.

This dependency direction protects the long-term durability of knowledge.

The layered model SHALL NOT be interpreted as a required software stack. An implementation does not need to expose the layers as separate applications, services, folders, databases, or modules. The layers are architectural responsibilities, not mandatory physical components.

A simple implementation may realize several layers through one application or vault. A complex implementation may distribute the layers across multiple tools, databases, services, agents, and interfaces. Both approaches may be compliant if the architectural responsibilities and boundaries are preserved.

The purpose of the layer model is not to make The Brain more complex. Its purpose is to prevent architectural confusion by ensuring that each responsibility has a clear place within the standard.

## 5. Layer 1 — Universal Knowledge Standard

Layer 1 defines the universal structure and meaning of knowledge within The Brain Standard.

The Universal Knowledge Standard is the foundational operational layer. It defines how knowledge is represented independently of storage systems, applications, workflows, agents, user interfaces, databases, or file structures.

Layer 1 is responsible for defining the architecture of knowledge itself.

At minimum, Layer 1 SHALL define or govern:

- Knowledge Objects;
- Knowledge Records;
- object identity;
- object types;
- required metadata;
- recommended metadata;
- optional metadata;
- relationships between objects;
- source references;
- provenance;
- lifecycle states;
- authority levels;
- privacy classifications;
- version and revision behavior;
- semantic meaning;
- validation expectations.

Layer 1 exists to ensure that knowledge remains understandable, portable, traceable, and usable regardless of where it is stored or how it is presented.

A Knowledge Object SHALL retain its meaning and identity when moved between folders, vaults, databases, applications, interfaces, workflows, or implementations.

Storage systems may hold knowledge. Applications may display knowledge. Agents may process knowledge. Workflows may transform or review knowledge. Implementations may provide access to knowledge.

None of those layers define the core meaning of knowledge.

The meaning of a Knowledge Object SHALL be defined by the Universal Knowledge Standard through explicit identity, metadata, relationships, provenance, lifecycle state, authority, privacy classification, and governed structure.

- Layer 1 has the strongest operational authority among the five operational layers because all other operational layers depend on the stable meaning of knowledge.
- Layer 2 depends on Layer 1 because storage must preserve object identity and meaning.
- Layer 3 depends on Layer 1 because agents must understand what they are allowed to read, classify, modify, suggest, or validate.
- Layer 4 depends on Layer 1 because workflows must know what kind of knowledge they are capturing, transforming, reviewing, publishing, or maintaining.
- Layer 5 depends on Layer 1 because implementations must create, read, preserve, and present knowledge without redefining its meaning.

Layer 1 SHALL remain implementation-independent.

No specific application, storage system, database, file format, plugin, AI model, interface, or automation platform may become required for the meaning of knowledge to remain valid.

Layer 1 MAY be implemented or represented through Markdown-compatible files, databases, graph systems, object stores, APIs, or future formats, provided the representation preserves the meaning, identity, portability, reviewability, and governance expectations of the Universal Knowledge Standard.

Layer 1 SHALL distinguish between original source material and structured knowledge derived from, about, or in response to that source material.

A source file may provide evidence. A Knowledge Record may summarize, interpret, extract, classify, connect, or preserve knowledge from that source. The source and the Knowledge Record MUST remain distinguishable.

The success of Layer 1 is measured by whether knowledge can remain meaningful, portable, and trustworthy even if every storage system, workflow, agent, or implementation around it is replaced.

## 6. Layer 2 — Storage Standard

Layer 2 defines how knowledge and source material may be stored, organized, referenced, moved, preserved, and retrieved without allowing storage to define knowledge meaning.

The Storage Standard exists to support durable access to knowledge while preserving the implementation independence of Layer 1.

Layer 2 is responsible for storage architecture, not semantic authority.

At minimum, Layer 2 SHALL define or govern:

- storage organization;
- vault or repository structure;
- file and folder conventions;
- source material storage;
- Knowledge Record storage;
- links between Knowledge Records and source material;
- movement and renaming behavior;
- import and export expectations;
- backup and preservation expectations;
- local-first compatibility;
- storage portability;
- storage validation;
- handling of missing, moved, duplicated, or superseded files;
- boundaries between storage convenience and knowledge meaning.

Layer 2 depends on Layer 1.

Storage systems MUST preserve the identity, meaning, metadata, relationships, provenance, lifecycle state, authority level, and privacy classification defined by Layer 1.

Storage systems MAY assist with organization, navigation, retrieval, indexing, synchronization, backup, and presentation. However, storage structure MUST NOT become the only source of critical meaning.

Folders, filenames, vault locations, databases, URLs, tags, indexes, and application-specific views may support usability, but they SHALL NOT replace explicit Layer 1 identity, metadata, relationships, provenance, lifecycle state, authority, or privacy classification.

A Knowledge Object SHALL remain the same Knowledge Object when moved from one folder to another, renamed, copied into another compliant repository, migrated into a database, exported into another format, or accessed through a different implementation.

Layer 2 SHALL preserve the distinction between source material and Knowledge Records.

Source material may be stored inside the same repository as Knowledge Records, stored in a separate source archive, or referenced from an external location. Any of these approaches may be compliant if the relationship between the Knowledge Record and the source material remains traceable.

Layer 2 SHOULD support local-first storage where practical.

A compliant implementation SHOULD be capable of preserving and reading core knowledge without requiring cloud storage, proprietary synchronization, external accounts, or internet connectivity.

Cloud storage, hosted databases, synchronization services, and external file systems MAY be used as implementation choices, but they MUST NOT become required for the meaning of knowledge to remain understandable and portable.

Layer 2 SHALL support storage replacement.

The Brain Standard must allow knowledge to move from one storage mechanism to another without semantic loss. A file-based vault, database-backed system, graph store, object store, or future storage model may be compliant if it preserves the Layer 1 meaning and satisfies the storage expectations defined by the Storage Standard.

Layer 2 SHOULD make storage behavior predictable enough that humans and agents can locate, validate, reference, and maintain knowledge without relying on hidden application state.

Storage may improve access to knowledge, but it does not own knowledge.

The success of Layer 2 is measured by whether knowledge and source material remain findable, traceable, portable, and preserved even when folders, filenames, repositories, databases, synchronization systems, or storage providers change.

## 7. Layer 3 — Agent Framework

Layer 3 defines how agents may interact with knowledge, source material, metadata, storage structures, workflow instructions, and implementation environments while preserving the architecture of The Brain Standard.

The Agent Framework exists to make automation useful without allowing agents to become unreviewable authorities over knowledge.

Layer 3 is responsible for agent behavior, permissions, traceability, review expectations, and architectural boundaries.

At minimum, Layer 3 SHALL define or govern:

- agent roles;
- agent permissions;
- agent-access boundaries;
- review requirements;
- traceability requirements;
- source-use expectations;
- privacy-respecting behavior;
- allowed knowledge operations;
- prohibited knowledge operations;
- metadata extraction behavior;
- classification behavior;
- summarization behavior;
- linking behavior;
- validation behavior;
- drafting behavior;
- escalation to human review;
- agent-generated change records;
- interaction with workflows and implementations.

Layer 3 depends on Layer 1 and Layer 2.

Agents depend on Layer 1 because they must understand Knowledge Objects, Knowledge Records, identity, metadata, relationships, provenance, lifecycle states, authority levels, and privacy classifications.

Agents depend on Layer 2 because they may need to locate, read, reference, move, validate, or preserve knowledge and source material within a storage environment.

Agents MAY assist with capturing, classifying, summarizing, linking, validating, drafting, reviewing, organizing, and maintaining knowledge.

Agents MUST NOT silently redefine knowledge meaning, object identity, authority level, privacy classification, lifecycle state, provenance, or governed metadata.

Agent activity SHOULD be traceable to the responsible agent, workflow, instruction, source material, output, and review state.

Where an agent creates or modifies a Knowledge Record, the change SHOULD remain reviewable by a human unless a future governed workflow explicitly permits automatic approval for a limited and well-defined operation.

Layer 3 SHALL preserve human review capability.

Agents may recommend changes, prepare drafts, identify problems, extract metadata, propose relationships, detect duplicates, or execute approved workflows. However, agents MUST NOT become the final authority over constitutional meaning, governed standards, privacy boundaries, or critical knowledge revisions unless explicitly authorized by a higher-authority governance process.

Layer 3 SHALL preserve privacy boundaries.

An agent MUST NOT access, export, summarize, publish, synchronize, or expose restricted knowledge unless the relevant privacy classification, workflow, and permission model allow that action.

Agent access SHOULD be limited to the project, repository, vault, workflow, source material, or knowledge scope required for the task being performed.

Layer 3 SHALL remain implementation-independent.

No specific AI model, provider, prompt system, plugin, automation platform, or agent framework may become required for The Brain Standard to remain valid.

Different implementations may use different agent systems if they preserve the requirements of the Agent Framework.

The success of Layer 3 is measured by whether agents can reduce cognitive load, improve knowledge quality, and support automation without weakening knowledge meaning, privacy, provenance, reviewability, or governance.

## 8. Layer 4 — Workflow Engine

Layer 4 defines repeatable workflows that coordinate knowledge capture, transformation, validation, review, maintenance, publication, synchronization, and automation within The Brain Standard.

The Workflow Engine exists to make knowledge work consistent, traceable, reviewable, and practical without allowing workflows to redefine knowledge meaning, storage meaning, agent authority, or implementation requirements.

Layer 4 is responsible for workflow structure, workflow states, workflow inputs, workflow outputs, workflow responsibilities, review points, and execution expectations.

At minimum, Layer 4 SHALL define or govern:

- workflow types;
- workflow inputs;
- workflow outputs;
- workflow states;
- workflow triggers;
- workflow permissions;
- workflow review requirements;
- workflow approval requirements;
- workflow failure handling;
- workflow logging;
- workflow traceability;
- workflow interaction with Knowledge Objects;
- workflow interaction with source material;
- workflow interaction with storage structures;
- workflow interaction with agents;
- workflow interaction with implementations;
- lifecycle transitions caused by workflows;
- privacy checks required during workflows;
- escalation to human review;
- conditions for automation;
- conditions for rejection, rollback, or supersession.

Layer 4 depends on Layer 1, Layer 2, and Layer 3.

Workflows depend on Layer 1 because they must understand Knowledge Objects, Knowledge Records, metadata, relationships, provenance, lifecycle states, authority levels, privacy classifications, and validation expectations.

Workflows depend on Layer 2 because they may need to locate, create, move, reference, preserve, export, import, or validate knowledge and source material within a storage environment.

Workflows depend on Layer 3 when agents participate in workflow execution, drafting, classification, summarization, linking, validation, or review preparation.

Workflows MAY coordinate human actions, agent actions, storage actions, implementation actions, or combinations of these.

Workflows MUST NOT silently alter knowledge meaning, object identity, authority level, privacy classification, lifecycle state, provenance, or governed metadata.

A workflow that changes knowledge SHOULD make the change traceable to the workflow, triggering event, responsible actor, source material, agent activity if applicable, review state, and approval state.

Layer 4 SHALL preserve human review capability.

Some workflows may be fully manual. Some workflows may be assisted by agents. Some workflows may be partially automated. Some limited workflows may eventually be fully automated if future governance defines clear permissions, safeguards, and review expectations.

Automation within a workflow MUST remain bounded by the authority granted to that workflow.

A workflow MUST NOT use implementation convenience as justification for bypassing Layer 1 meaning, Layer 2 storage requirements, Layer 3 agent boundaries, privacy classifications, or governance rules.

Layer 4 SHALL preserve privacy boundaries.

A workflow MUST NOT export, publish, synchronize, summarize, index, expose, or route restricted knowledge unless the relevant privacy classification, permission model, and workflow rules allow that action.

Workflow design SHOULD reduce cognitive load.

A workflow should make routine knowledge work easier, not harder. Required workflow steps SHOULD be limited to those necessary for durability, portability, traceability, privacy, reviewability, governance, automation reliability, or long-term maintainability.

Layer 4 SHALL remain implementation-independent.

No specific task manager, automation platform, scripting language, application, plugin, AI model, database, or user interface may become required for The Brain Standard to remain valid.

Different implementations may execute workflows differently if they preserve the required workflow meaning, inputs, outputs, review states, traceability, privacy boundaries, and governance expectations.

The success of Layer 4 is measured by whether workflows make knowledge operations repeatable, traceable, reviewable, privacy-respecting, and practical without weakening knowledge meaning, storage portability, agent boundaries, or implementation independence.

## 9. Layer 5 — Implementations

Layer 5 defines how The Brain Standard may be realized in practical software, vaults, databases, file systems, interfaces, tools, automations, and operating environments.

The Implementations layer exists to allow The Brain Standard to be used in real systems without allowing any single implementation to become the standard itself.

Layer 5 is responsible for practical realization, not architectural authority.

At minimum, Layer 5 SHALL define or govern:

- reference implementations;
- implementation profiles;
- implementation-specific behavior;
- user interfaces;
- file-system realizations;
- database realizations;
- graph-system realizations;
- import and export tooling;
- validation tooling;
- synchronization behavior;
- backup behavior;
- agent runtime environments;
- workflow execution environments;
- interoperability behavior;
- migration behavior;
- implementation documentation;
- implementation compliance expectations.

Layer 5 depends on Layer 1, Layer 2, Layer 3, and Layer 4.

Implementations depend on Layer 1 because they must create, read, preserve, display, validate, and modify knowledge without redefining its meaning.

Implementations depend on Layer 2 because they must store, locate, retrieve, preserve, migrate, import, export, or reference knowledge and source material without allowing storage structure to define meaning.

Implementations depend on Layer 3 when they expose, host, coordinate, limit, or integrate agents.

Implementations depend on Layer 4 when they execute, support, enforce, automate, or display workflows.

An implementation MAY combine multiple operational layers inside one application, vault, database, plugin system, automation environment, or user interface.

An implementation MAY distribute operational layers across multiple tools, repositories, databases, services, scripts, agents, or interfaces.

Both simple and complex implementations may be compliant if they preserve the meaning, boundaries, dependencies, reviewability, privacy protections, and governance expectations defined by The Brain Standard.

Layer 5 SHALL remain replaceable.

No specific implementation, including a reference implementation, may become required for knowledge to remain understandable, portable, traceable, reviewable, and usable.

Reference implementations may demonstrate recommended patterns, default structures, workflows, tools, or validation behavior. However, a reference implementation MUST NOT redefine the standard, override constitutional documents, or impose implementation-specific requirements on other compliant implementations.

Layer 5 SHALL distinguish implementation behavior from standard behavior.

Implementation behavior may include user interface design, local folder choices, plugin settings, indexing strategies, display preferences, automation scripts, database optimizations, synchronization services, or application-specific features.

Standard behavior includes requirements necessary to preserve knowledge meaning, object identity, source distinction, privacy boundaries, provenance, lifecycle, portability, reviewability, interoperability, and governance.

Implementation-specific behavior MAY improve usability, performance, automation, search, visualization, or convenience, but it MUST NOT become necessary for the knowledge itself to remain valid.

Layer 5 SHOULD support practical daily use.

An implementation that technically preserves the standard but is too difficult to use consistently may fail the practical goals of The Brain. Implementations SHOULD reduce cognitive load, support predictable workflows, expose meaningful review points, and make compliant behavior easier than non-compliant behavior.

Layer 5 SHOULD support migration and replacement.

A compliant implementation SHOULD make it possible to export, migrate, validate, or inspect knowledge without losing Layer 1 meaning, Layer 2 storage relationships, Layer 3 agent traceability, or Layer 4 workflow history where applicable.

Layer 5 SHALL preserve privacy boundaries.

An implementation MUST NOT expose restricted knowledge through sync, publishing, search indexing, agent access, exports, backups, plugins, logs, or user interface behavior unless the relevant privacy classification and permission model allow that action.

Layer 5 SHALL remain open to multiple implementation forms.

A compliant implementation may be file-based, database-backed, graph-based, application-based, local-first, cloud-assisted, agent-integrated, workflow-oriented, or based on future technologies not yet defined.

The success of Layer 5 is measured by whether implementations make The Brain usable in practice while preserving implementation independence, knowledge meaning, portability, privacy, reviewability, and governance.

## 10. Constitutional Foundation and Operational Layers

The Brain Standard distinguishes between the constitutional foundation and the operational layers.

The constitutional foundation defines the purpose, authority, principles, and governing structure of The Brain Standard.

The operational layers define the functional architecture used to represent, store, automate, process, and implement knowledge.

The constitutional foundation governs the operational layers. It is not itself one of the operational layers.

The constitutional foundation includes TB-series documents that define the highest-level architecture of The Brain Standard. These documents establish the mission, vision, authority hierarchy, architecture principles, layered model, and other foundational rules that future standards must follow.

At minimum, the constitutional foundation includes:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- future approved TB-series constitutional documents.

The operational layers include:

1. Layer 1 — Universal Knowledge Standard
2. Layer 2 — Storage Standard
3. Layer 3 — Agent Framework
4. Layer 4 — Workflow Engine
5. Layer 5 — Implementations

The operational layers are governed by the constitutional foundation.

A lower-authority standard, specification, workflow, agent, implementation, guide, or operational document MUST NOT override the constitutional foundation.

A layer-specific standard MAY add detail to an operational layer, but it MUST NOT contradict the constitutional foundation.

For example:

- a Knowledge Standard may define object types, metadata fields, relationships, and lifecycle states;
- a Storage Standard may define vault structure, source storage, import and export expectations, and storage validation;
- an Agent Standard may define agent roles, permissions, review rules, and traceability expectations;
- a Workflow Standard may define workflow types, review states, automation boundaries, and lifecycle transitions;
- an Implementation document may define how a specific tool, vault, database, or interface realizes the standard.

These lower-level documents are valid only when they preserve the meaning, authority, boundaries, and principles established by the constitutional foundation.

The constitutional foundation SHOULD remain stable.

Changes to the constitutional foundation affect the entire architecture and SHOULD be made only through formal governance, documented rationale, compatibility review, and approval.

The operational layers MAY evolve more frequently than the constitutional foundation, provided that their changes remain compatible with higher-authority documents.

This distinction allows The Brain Standard to evolve without losing architectural coherence.

The constitutional foundation protects what The Brain is.

The operational layers define how The Brain works.

Implementations demonstrate how The Brain can be used in practice.

## 11. Cross-Layer Rules

Cross-layer rules define how the operational layers of The Brain Standard interact with each other.

These rules exist to preserve architectural boundaries, prevent responsibility confusion, and ensure that one layer does not silently redefine another layer.

The operational layers are designed to work together, but each layer has a distinct architectural responsibility.

- Layer 1 defines knowledge meaning.
- Layer 2 preserves knowledge and source material in storage.
- Layer 3 governs agent interaction with knowledge, storage, workflows, and implementation environments.
- Layer 4 governs repeatable workflows that coordinate knowledge operations.
- Layer 5 realizes the standard in practical implementations.

Cross-layer interaction is allowed and expected. Cross-layer authority confusion is not allowed.

### 11.1 Meaning Must Flow from Layer 1

Knowledge meaning SHALL originate in Layer 1.

Layer 2, Layer 3, Layer 4, and Layer 5 may store, process, route, validate, present, summarize, automate, or implement knowledge, but they MUST NOT redefine the core meaning of knowledge.

If storage structure, agent output, workflow behavior, or implementation behavior appears to conflict with Layer 1 meaning, Layer 1 meaning takes precedence unless a higher-authority governance process formally changes the standard.

### 11.2 Storage Must Preserve Meaning Without Owning Meaning

Layer 2 SHALL preserve the identity, structure, metadata, relationships, provenance, lifecycle state, authority, and privacy classification defined by Layer 1.

Storage MAY support organization, discovery, navigation, synchronization, backup, import, export, indexing, and preservation.

Storage MUST NOT become the sole source of critical meaning.

Folders, filenames, repository locations, database tables, indexes, URLs, tags, or application-specific storage structures may assist usability but MUST NOT replace explicit Layer 1 meaning.

### 11.3 Agents Must Operate Within Defined Boundaries

Layer 3 agents MAY interact with knowledge, source material, storage structures, workflow instructions, and implementation environments.

Agents MUST operate within the permissions, review expectations, privacy boundaries, and traceability rules defined by the Agent Framework.

Agents MUST NOT silently alter knowledge meaning, object identity, provenance, authority, privacy classification, lifecycle state, or governed metadata.

Where an agent participates in a workflow, the workflow MUST preserve the review, traceability, and privacy expectations of Layer 3.

### 11.4 Workflows Must Coordinate Without Redefining Lower Layers

Layer 4 workflows MAY coordinate actions across knowledge, storage, agents, implementations, and human review.

Workflows MUST NOT redefine Layer 1 knowledge meaning, Layer 2 storage requirements, or Layer 3 agent boundaries.

A workflow that changes knowledge SHOULD make the change traceable to the workflow, triggering event, responsible actor, source material, agent activity if applicable, review state, and approval state.

Workflow convenience MUST NOT justify bypassing privacy classifications, governance rules, review requirements, or source distinctions.

### 11.5 Implementations Must Realize, Not Redefine

Layer 5 implementations MAY combine, distribute, automate, display, optimize, or simplify operational layers.

An implementation MUST preserve the required meanings, boundaries, dependencies, and review expectations defined by Layers 1 through 4.

Implementation-specific behavior MUST NOT become required for knowledge to remain valid.

If an implementation introduces features that go beyond the standard, those features SHOULD be clearly distinguishable from standard behavior.

### 11.6 Privacy Must Be Preserved Across Layers

Privacy boundaries SHALL be preserved across every layer.

A privacy classification defined at the knowledge level MUST be respected by storage behavior, agent access, workflow routing, implementation features, exports, indexing, synchronization, publication, and backup behavior.

No layer may expose restricted knowledge merely because another layer can technically access it.

When privacy and operational convenience conflict, privacy SHALL take precedence.

### 11.7 Reviewability Must Be Preserved Across Layers

Human review capability SHALL remain available across cross-layer operations.

If knowledge is modified, transformed, summarized, classified, exported, published, or superseded through a cross-layer process, the process SHOULD preserve enough context for a human to understand what changed, why it changed, what source material was involved, and what actor or workflow caused the change.

Automation may reduce cognitive load, but it MUST NOT make critical changes unreviewable.

### 11.8 Cross-Layer Dependencies Must Be Explicit

When a standard, specification, workflow, agent, or implementation depends on another layer, that dependency SHOULD be explicit.

Hidden dependencies create architectural fragility.

Examples of hidden dependencies include:

- assuming a folder path defines object type;
- assuming a filename defines object identity;
- assuming an agent output is approved knowledge;
- assuming workflow completion means human approval;
- assuming implementation metadata is standard metadata;
- assuming a plugin feature is required by the standard.

Cross-layer dependencies SHOULD be documented when they affect meaning, portability, privacy, governance, validation, automation, or compliance.

### 11.9 Cross-Layer Conflicts Must Follow Authority

When layers appear to conflict, the following order SHALL guide resolution:

1. Constitutional foundation
2. Layer 1 — Universal Knowledge Standard
3. Layer 2 — Storage Standard
4. Layer 3 — Agent Framework
5. Layer 4 — Workflow Engine
6. Layer 5 — Implementations

This order does not mean higher-numbered layers are less important. It means that higher-numbered layers depend on lower-numbered layers for meaning, preservation, boundaries, and interpretation.

A lower-authority or higher-numbered layer MAY add detail, automation, usability, or implementation behavior, but it MUST NOT contradict the authority or meaning of the layers it depends on.

### 11.10 Cross-Layer Simplicity Should Be Preferred

Cross-layer designs SHOULD remain as simple as practical.

A cross-layer rule, workflow, agent behavior, storage convention, or implementation feature should be added only when it materially improves durability, portability, trustworthiness, privacy, reviewability, automation reliability, interoperability, or daily usability.

Complex cross-layer behavior SHOULD be justified by durable architectural value.

## 12. Dependency Rules

Dependency rules define how the constitutional foundation, operational layers, standards, specifications, workflows, agents, and implementations may rely on one another.

These rules exist to preserve architectural stability, prevent circular authority, and ensure that higher-level behavior does not silently redefine lower-level meaning.

A dependency exists when one document, layer, workflow, agent, implementation, schema, tool, or process relies on another for meaning, structure, authority, interpretation, validation, or execution.

Dependencies are allowed and expected.

Hidden, circular, or authority-reversing dependencies are not allowed.

### 12.1 Constitutional Documents Govern Lower-Authority Documents

TB-series constitutional documents have the highest architectural authority within The Brain Standard.

Lower-authority documents MUST NOT contradict constitutional documents.

Lower-authority documents MAY add detail, constraints, examples, schemas, workflows, implementation guidance, or operational procedures, but they MUST preserve the meaning, principles, and boundaries established by the constitutional foundation.

If a lower-authority document appears to conflict with a constitutional document, the constitutional document takes precedence unless formally superseded through governance.

### 12.2 Operational Layers Depend Downward

Operational layers are ordered by architectural dependency.

The dependency direction is:

- Layer 5 depends on Layers 4, 3, 2, and 1.
- Layer 4 depends on Layers 3, 2, and 1.
- Layer 3 depends on Layers 2 and 1.
- Layer 2 depends on Layer 1.
- Layer 1 depends on the constitutional foundation.

Higher-numbered operational layers MAY depend on lower-numbered operational layers.

Lower-numbered operational layers MUST NOT depend on higher-numbered operational layers for their meaning or authority.

For example:

- storage may depend on knowledge identity, but knowledge identity must not depend on folder location;
- agents may depend on storage access, but storage meaning must not depend on agent behavior;
- workflows may depend on agents, but agent boundaries must not depend on an individual workflow;
- implementations may execute workflows, but workflow meaning must not depend on one implementation.

### 12.3 Layer 1 Dependencies Must Be Minimal and Constitutional

Layer 1 SHOULD depend only on the constitutional foundation and formally approved knowledge standards or specifications.

Layer 1 MUST NOT depend on any specific storage system, agent system, workflow engine, implementation, application, database, file path, folder structure, plugin, AI model, or user interface.

This preserves the independence of knowledge meaning.

### 12.4 Layer 2 Dependencies Must Preserve Layer 1 Meaning

Layer 2 MAY depend on Layer 1 identity, metadata, relationships, provenance, lifecycle states, authority levels, privacy classifications, and validation expectations.

Layer 2 MUST NOT introduce storage rules that redefine Layer 1 meaning.

A storage dependency is compliant only if knowledge remains understandable and portable when storage mechanisms change.

### 12.5 Layer 3 Dependencies Must Respect Knowledge, Storage, and Privacy

Layer 3 MAY depend on Layer 1 knowledge meaning and Layer 2 storage access.

Layer 3 MUST preserve privacy classifications, source distinctions, provenance, lifecycle states, review requirements, and governed metadata.

Agent dependencies on prompts, models, APIs, tools, plugins, permissions, or implementation environments MUST NOT become requirements of The Brain Standard unless formally defined by a governed standard or specification.

### 12.6 Layer 4 Dependencies Must Be Traceable

Layer 4 MAY depend on Layer 1, Layer 2, and Layer 3.

Workflow dependencies SHOULD be explicit when they affect knowledge meaning, storage behavior, agent behavior, privacy, review states, lifecycle transitions, validation, publication, export, synchronization, or governance.

A workflow MUST NOT depend on hidden implementation state when that dependency affects critical meaning or compliance.

### 12.7 Layer 5 Dependencies Must Remain Replaceable

Layer 5 MAY depend on all lower operational layers.

An implementation MAY use specific software, databases, file systems, AI models, plugins, scripts, interfaces, cloud services, or operating environments.

However, those implementation dependencies MUST NOT become requirements for the standard itself.

A compliant implementation SHOULD allow knowledge to be exported, migrated, inspected, or validated without losing Layer 1 meaning, Layer 2 storage relationships, Layer 3 agent traceability, or Layer 4 workflow history where applicable.

### 12.8 Circular Dependencies Must Be Avoided

A circular dependency occurs when two or more layers, documents, workflows, agents, or implementations rely on each other in a way that makes authority, meaning, validation, or maintenance unclear.

Circular dependencies SHOULD be avoided.

Examples of circular dependency risks include:

- object identity depending on file path while file path depends on object identity;
- workflow approval depending on agent output while agent authority depends on workflow approval;
- implementation behavior defining a standard while the standard claims implementation independence;
- privacy classification depending only on storage location while storage routing depends on privacy classification.

Where a circular dependency cannot be avoided, it MUST be documented, justified, reviewed, and constrained.

### 12.9 External Dependencies Must Be Optional or Governed

External dependencies include proprietary software, cloud services, hosted databases, AI providers, synchronization systems, plugins, APIs, file formats, schemas, or third-party tools.

External dependencies MAY be used by implementations.

External dependencies MUST NOT be required for the knowledge itself to remain understandable, portable, reviewable, and usable unless formally approved by a higher-authority governance process.

Where external dependencies are used, implementations SHOULD document:

- what the dependency is;
- what function it provides;
- whether it is required or optional;
- what happens if it is removed;
- how knowledge can be exported, migrated, or preserved without it.

### 12.10 Dependency Changes Require Review

A dependency change SHOULD be reviewed when it affects:

- knowledge meaning;
- object identity;
- storage portability;
- agent permissions;
- workflow behavior;
- privacy boundaries;
- provenance;
- lifecycle states;
- governance;
- validation;
- implementation compliance;
- migration or export behavior.

Major dependency changes SHOULD be recorded through an ADR, RFC, standard, specification, or approved constitutional revision.

Undocumented dependencies MUST NOT become architecture by accident.

### 12.11 Dependency Simplicity Should Be Preferred

The Brain Standard SHOULD prefer simple, explicit, replaceable dependencies over complex, hidden, or fragile dependencies.

A dependency is justified when it materially improves durability, portability, trustworthiness, privacy, reviewability, automation reliability, interoperability, maintainability, or daily usability.

Dependency complexity SHOULD be minimized unless its long-term architectural value is clear.

## 13. Anti-Patterns

Anti-patterns are architectural choices that may appear useful in the short term but weaken the durability, portability, trustworthiness, reviewability, privacy, governance, or implementation independence of The Brain Standard.

The anti-patterns in this section apply specifically to the layered architecture.

A design, standard, specification, workflow, agent, or implementation SHOULD avoid these anti-patterns unless the deviation is explicitly documented, justified, and approved through governance.

### 13.1 Collapsing the Layers

Collapsing the layers occurs when two or more architectural layers are treated as the same responsibility.

Examples include:

- treating storage structure as knowledge meaning;
- treating agent output as approved knowledge;
- treating workflow completion as human review;
- treating implementation behavior as the standard;
- treating a reference implementation as the architecture itself.

This is an anti-pattern because The Brain depends on clear separation between meaning, storage, agents, workflows, and implementations.

### 13.2 Reversing Dependency Direction

Reversing dependency direction occurs when a lower-numbered layer depends on a higher-numbered layer for its meaning or authority.

Examples include:

- Knowledge Object identity depending on a folder path;
- metadata meaning depending on a plugin;
- source distinction depending on a user interface;
- privacy classification depending only on workflow routing;
- governance meaning depending on implementation behavior.

This is an anti-pattern because higher-numbered layers must remain replaceable.

### 13.3 Implementation-Defined Architecture

Implementation-defined architecture occurs when a specific application, vault, database, AI model, plugin, file system, interface, or automation platform becomes treated as the architecture.

This is an anti-pattern because implementations demonstrate the standard; they do not define it.

A reference implementation may show one compliant way to realize The Brain Standard, but it MUST NOT become the standard itself.

### 13.4 Storage-Defined Knowledge

Storage-defined knowledge occurs when folders, filenames, vault locations, database tables, URLs, tags, indexes, or application views become the only source of critical meaning.

This is an anti-pattern because storage may organize knowledge but must not define knowledge meaning.

Knowledge meaning must remain explicit enough to survive storage migration, renaming, reorganization, export, import, and implementation replacement.

### 13.5 Agent Authority Creep

Agent authority creep occurs when agents gradually gain the ability to create, modify, approve, publish, reclassify, delete, or supersede knowledge without clear permissions, traceability, review rules, or governance.

This is an anti-pattern because agents are participants in knowledge work, not constitutional authorities.

Automation should reduce cognitive load while preserving human review, privacy boundaries, provenance, and accountability.

### 13.6 Workflow Authority Creep

Workflow authority creep occurs when workflow completion becomes treated as proof that knowledge is correct, approved, governed, or safe to publish.

This is an anti-pattern because workflows coordinate actions; they do not automatically confer truth, authority, or approval unless the workflow explicitly includes governed review and approval requirements.

### 13.7 Hidden Cross-Layer Dependency

Hidden cross-layer dependency occurs when one layer quietly relies on another layer without documenting that dependency.

Examples include:

- a workflow depending on a plugin field that is not part of the standard;
- an agent assuming a filename represents object identity;
- an implementation treating a UI state as lifecycle state;
- a storage convention acting as privacy classification;
- a validation process relying on undocumented application behavior.

This is an anti-pattern because hidden dependencies make migration, validation, auditing, and replacement fragile.

### 13.8 Privacy Leakage Across Layers

Privacy leakage across layers occurs when restricted knowledge becomes exposed because one layer fails to respect privacy metadata or privacy boundaries from another layer.

Examples include:

- search indexing restricted content;
- agents reading content outside their permitted scope;
- workflows exporting restricted knowledge;
- implementations publishing private records;
- backups or logs exposing sensitive content.

This is an anti-pattern because privacy must be preserved across all layers, not only where the user happens to remember it.

### 13.9 Unreviewable Automation

Unreviewable automation occurs when agents, workflows, or implementations change knowledge without enough traceability for a human to understand what changed, why it changed, what source material was used, and what actor or process caused the change.

This is an anti-pattern because The Brain depends on trustworthy knowledge stewardship.

Automation may assist, accelerate, and simplify knowledge work, but it must not remove accountability for critical changes.

### 13.10 Over-Engineering the Layer Model

Over-engineering the layer model occurs when every minor feature, habit, folder, script, prompt, or preference is treated as a formal architectural layer or governed standard.

This is an anti-pattern because The Brain should remain practical for daily use.

The layered architecture exists to reduce confusion, not to create unnecessary bureaucracy.

### 13.11 Premature Implementation Optimization

Premature implementation optimization occurs when the architecture is shaped around performance, scale, automation, or tool-specific convenience before the knowledge model and architectural boundaries are stable.

This is an anti-pattern because implementation optimization should not weaken knowledge meaning, portability, reviewability, or governance.

Optimization may be valuable, but it belongs in implementations and specifications after the architectural foundation is clear.

### 13.12 Governance Bypass

Governance bypass occurs when major architectural decisions are made through habit, tool defaults, informal preference, agent behavior, or workflow convenience instead of documented review and approval.

This is an anti-pattern because The Brain Standard must evolve through governed decisions.

Undocumented practice MUST NOT become architecture by accident.

## 14. Review Checklist

The review checklist provides a practical method for evaluating whether a proposed standard, specification, workflow, agent, implementation, or architectural decision aligns with the layered architecture defined by TB-0002.

A proposal SHOULD be reviewed against this checklist before it is approved as part of The Brain Standard.

### 14.1 Constitutional Alignment

- Does the proposal align with TB-0000, TB-0001, and TB-0002?
- Does it preserve the distinction between the constitutional foundation and the operational layers?
- Does it avoid contradicting higher-authority documents?
- Does it require an ADR, RFC, specification, standard, or constitutional revision?

### 14.2 Layer Placement

- Is the proposal assigned to the correct architectural layer?
- Does it clearly identify whether it belongs to Layer 1, Layer 2, Layer 3, Layer 4, Layer 5, or the constitutional foundation?
- Does it avoid mixing responsibilities from multiple layers without documenting the interaction?
- Does it avoid creating a new layer when an existing layer is sufficient?

### 14.3 Layer 1 — Knowledge Meaning

- Does the proposal preserve Knowledge Object identity?
- Does it preserve knowledge meaning independently of storage, agents, workflows, and implementations?
- Does it make critical meaning explicit through metadata, relationships, provenance, lifecycle state, authority, privacy classification, or governed structure?
- Does it distinguish source material from Knowledge Records?

### 14.4 Layer 2 — Storage

- Does the proposal preserve Layer 1 meaning in storage?
- Does it avoid making folders, filenames, vault locations, database structures, URLs, tags, indexes, or application views the sole source of critical meaning?
- Does it support storage portability, migration, preservation, import, export, or validation where applicable?
- Does it preserve traceability between source material and Knowledge Records?

### 14.5 Layer 3 — Agents

- Does the proposal preserve agent boundaries?
- Does it define or respect agent permissions, traceability, review expectations, and privacy boundaries?
- Does it prevent agents from silently redefining knowledge meaning, identity, provenance, authority, privacy classification, lifecycle state, or governed metadata?
- Does it preserve human review for agent-created or agent-modified knowledge where required?

### 14.6 Layer 4 — Workflows

- Does the proposal define clear workflow inputs, outputs, states, triggers, responsibilities, and review points where applicable?
- Does it preserve traceability for workflow-driven changes?
- Does it avoid treating workflow completion as automatic proof of correctness, approval, or publication readiness?
- Does it preserve privacy, governance, and review requirements during workflow execution?

### 14.7 Layer 5 — Implementations

- Does the proposal distinguish implementation-specific behavior from standard behavior?
- Does it avoid making any specific implementation, application, plugin, AI model, database, file system, interface, or cloud service required for the standard?
- Does it support migration, export, validation, or inspection where applicable?
- Does it preserve implementation replaceability?

### 14.8 Cross-Layer Interaction

- Are cross-layer dependencies explicit?
- Does the proposal preserve the dependency direction defined by TB-0002?
- Does it avoid circular dependencies?
- Does it avoid hidden dependencies on tool behavior, file paths, UI state, plugin metadata, prompts, or application-specific conventions?
- If layers interact, are responsibility boundaries clear?

### 14.9 Privacy and Reviewability

- Are privacy classifications respected across storage, agents, workflows, implementations, exports, indexing, synchronization, backups, and publication?
- Does the proposal preserve human review capability where knowledge meaning, privacy, lifecycle, authority, or governance may be affected?
- Does automation remain traceable and bounded?
- Does the proposal avoid unreviewable critical changes?

### 14.10 Practical Usability

- Is the proposal practical for routine use?
- Does it reduce or increase cognitive load?
- Is the added structure justified by durability, portability, trustworthiness, privacy, reviewability, interoperability, automation reliability, or maintainability?
- Could the same goal be achieved with a simpler design?

### 14.11 Anti-Pattern Check

- Does the proposal avoid collapsing layers?
- Does it avoid reversing dependency direction?
- Does it avoid implementation-defined architecture?
- Does it avoid storage-defined knowledge?
- Does it avoid agent authority creep?
- Does it avoid workflow authority creep?
- Does it avoid hidden cross-layer dependencies?
- Does it avoid privacy leakage across layers?
- Does it avoid unreviewable automation?
- Does it avoid over-engineering the layer model?

### 14.12 Final Review Question

Before approval, every major proposal SHOULD answer the following question:

Does this proposal strengthen The Brain Standard’s layered architecture while preserving knowledge meaning, implementation independence, portability, privacy, reviewability, governance, and practical daily use?

## 15. Success Criteria

### 15.1 Architectural Success

TB-0002 is successful when it provides a clear, stable, and practical layered architecture for The Brain Standard.

The success of this document is measured by whether future standards, specifications, workflows, agents, and implementations can use the layered model to make consistent architectural decisions without confusing meaning, storage, automation, workflow, implementation, or constitutional authority.

TB-0002 is successful if it establishes that:

- the constitutional foundation governs the operational architecture;
- the operational architecture is organized into five clear layers;
- Layer 1 defines knowledge meaning;
- Layer 2 preserves knowledge and source material in storage;
- Layer 3 governs agent interaction with knowledge, storage, workflows, and implementation environments;
- Layer 4 governs repeatable workflows that coordinate knowledge operations;
- Layer 5 realizes the standard in practical implementations;
- higher-numbered layers may depend on lower-numbered layers;
- lower-numbered layers do not depend on higher-numbered layers for meaning or authority;
- implementations remain replaceable;
- storage does not define knowledge meaning;
- agents do not become unreviewable authorities;
- workflows do not bypass governance, privacy, or review;
- cross-layer dependencies remain explicit;
- circular dependencies are avoided or formally justified;
- privacy boundaries are preserved across all layers;
- human review remains available for critical knowledge changes;
- source material remains distinguishable from Knowledge Records;
- architectural anti-patterns are identifiable and avoidable;
- future proposals can be reviewed against a practical checklist.

### 15.2 Classification and Review Success

A future standard, specification, workflow, agent, or implementation SHOULD be easier to classify because of TB-0002.

A compliant design SHOULD be able to answer:

- which layer the design belongs to;
- which lower layers it depends on;
- what meaning it may define;
- what meaning it must preserve;
- what authority it has;
- what authority it does not have;
- what privacy boundaries it must respect;
- what review expectations apply;
- how it remains portable or replaceable;
- how it avoids implementation-defined architecture.

### 15.3 Drift Prevention

TB-0002 is also successful if it prevents architectural drift.

Architectural drift occurs when tool behavior, storage habits, workflow convenience, agent activity, or implementation defaults gradually become treated as architecture without review or approval.

This document should make such drift easier to detect, discuss, correct, and govern.

### 15.4 Human and AI Understandability

The layered architecture SHOULD remain understandable to both humans and AI systems.

A human reviewer should be able to read TB-0002 and understand where a proposed rule, schema, workflow, agent behavior, storage convention, or implementation belongs.

An AI system assisting with The Brain Standard should be able to use TB-0002 to classify responsibilities, identify boundary violations, detect anti-patterns, and recommend review paths without redefining the architecture.

### 15.5 Practical Use and Final Success Measure

TB-0002 is successful when the layer model reduces confusion rather than increasing bureaucracy.

The layered architecture should support practical daily use, not only theoretical completeness.

The final measure of success is whether The Brain can evolve across tools, storage systems, agents, workflows, interfaces, and implementations while preserving knowledge meaning, portability, privacy, reviewability, governance, and long-term trust.
