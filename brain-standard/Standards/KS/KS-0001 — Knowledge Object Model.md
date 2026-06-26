# KS-0001 — Knowledge Object Model

Document ID: KS-0001
Title: Knowledge Object Model
Version: 0.1.0
Status: Approved
Created: 2026-06-25
Last Updated: 2026-06-26
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.1 — Knowledge Object Model
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and knowledge-model rules are interpreted within KS-0001.

Where conflicts arise between knowledge objects, knowledge records, metadata, relationships, provenance, lifecycle states, source references, storage behavior, workflows, agents, implementations, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0001 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

If KS-0001 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, object identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to source material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, or other artifacts used as evidence, input, or reference material.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, or relationship information associated with a Knowledge Object or Knowledge Record.
- Required Metadata refers to metadata that MUST be present for a Knowledge Object or Knowledge Record to be valid under this standard.
- Optional Metadata refers to metadata that MAY be included when useful but is not required for basic validity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, agent, workflow, or evidence associated with a Knowledge Object or Knowledge Record.
- Source Reference refers to a traceable reference from a Knowledge Record to source material that supports, explains, or contextualizes the record.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, source material, standards, decisions, workflows, implementations, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Object or Knowledge Record. KS-0001 uses lifecycle state as a knowledge-level concept while remaining compatible with the document lifecycle expectations defined by TB-0003.
- Privacy Classification refers to explicit metadata describing the permitted visibility, access, exposure, or handling expectations of a Knowledge Object or Knowledge Record.
- Authority Level refers to the governance weight, review status, or interpretive authority assigned to a document, Knowledge Object, Knowledge Record, source, or decision.
- Validation refers to the process of checking whether a Knowledge Object or Knowledge Record satisfies the structural, metadata, provenance, relationship, lifecycle, privacy, and compatibility expectations defined by the relevant standards or specifications.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0001 is to define the foundational unit of knowledge within The Brain Standard.

KS-0001 establishes what a Knowledge Object is, how a Knowledge Object is represented through Knowledge Records, how Knowledge Objects differ from source material, how object identity is preserved, what metadata is required, how relationships are represented, how provenance is maintained, and how humans, agents, workflows, and implementations should interpret structured knowledge.

The Knowledge Object Model exists to ensure that knowledge remains:

- implementation-independent;
- portable across storage systems and tools;
- understandable to humans;
- interpretable by AI systems;
- traceable to source material where applicable;
- reviewable over time;
- protected by explicit privacy boundaries;
- governed through clear lifecycle and authority expectations;
- extensible without losing meaning.

KS-0001 defines the meaning and minimum structural expectations of Knowledge Objects and Knowledge Records.

KS-0001 does not define folder layouts, database schemas, application behavior, workflow execution steps, agent permissions, interface behavior, or daily operating procedures. Those concerns belong to later storage standards, agent standards, workflow standards, implementation documents, specifications, and operational guides.

The primary purpose of KS-0001 is to prevent knowledge meaning from becoming dependent on storage location, filenames, tools, agents, workflows, or implementation-specific behavior.

A Knowledge Object SHALL retain its identity and meaning even when it is moved, renamed, copied, migrated, exported, imported, indexed, summarized, displayed differently, or processed by an agent or workflow.

A compliant system may store or display Knowledge Objects in many ways, but the meaning of the Knowledge Object MUST remain defined by explicit identity, metadata, relationships, provenance, lifecycle state, authority, privacy classification, and governed structure.

KS-0001 is the first standard within Phase 1 — Universal Knowledge Standard.

Its success is measured by whether future knowledge standards, storage standards, agent standards, workflow standards, specifications, and implementations can rely on a stable, explicit, portable, and reviewable model of knowledge.

## 2. Relationship to Constitutional Documents

KS-0001 is subordinate to and derived from the constitutional foundation of The Brain Standard.

The constitutional foundation establishes the mission, principles, layered architecture, and governance model that KS-0001 must follow.

KS-0001 depends on:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

KS-0001 applies that purpose by defining the foundational model for structured knowledge.

TB-0001 establishes the architecture principles that govern The Brain Standard.

KS-0001 applies those principles by requiring Knowledge Objects and Knowledge Records to preserve:

- stable identity;
- explicit meaning;
- source distinction;
- metadata clarity;
- provenance;
- privacy boundaries;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability.

TB-0002 establishes the layered architecture of The Brain Standard.

KS-0001 belongs to Layer 1 — Universal Knowledge Standard.

Layer 1 defines the meaning and structure of knowledge independently of storage systems, agents, workflows, user interfaces, databases, or implementations.

Because KS-0001 is a Layer 1 standard, it defines knowledge meaning but does not define storage behavior, agent behavior, workflow execution, implementation setup, or operational procedure.

TB-0003 establishes the governance model for The Brain Standard.

KS-0001 follows the document authority hierarchy defined by TB-0003. As a standard-level document, KS-0001 has high authority within its scope but remains subordinate to constitutional documents.

KS-0001 MAY define required and recommended behavior for Knowledge Objects, Knowledge Records, metadata, relationships, provenance, lifecycle state, privacy classification, and validation expectations.

KS-0001 MUST NOT contradict the constitutional foundation.

If KS-0001 conflicts with TB-0000, TB-0001, TB-0002, or TB-0003, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

If a later specification, workflow, agent standard, storage standard, implementation document, operational guide, or reference implementation conflicts with KS-0001, the conflict SHOULD be resolved according to the authority hierarchy defined by TB-0003.

KS-0001 provides the foundation for future knowledge specifications.

Future specifications MAY define exact schemas, templates, fields, relationship formats, validation rules, object types, lifecycle values, privacy classifications, or import and export formats.

Those future specifications are valid only when they preserve the knowledge meaning, identity, source distinction, provenance, privacy expectations, and implementation independence defined by KS-0001.

KS-0001 also provides the foundation for future storage, agent, workflow, and implementation documents.

Storage standards depend on KS-0001 because storage must preserve Knowledge Object identity and meaning.

Agent standards depend on KS-0001 because agents must understand what they are allowed to read, classify, summarize, validate, modify, or propose.

Workflow standards depend on KS-0001 because workflows must understand what kind of knowledge they are capturing, transforming, reviewing, approving, superseding, or maintaining.

Implementation documents depend on KS-0001 because implementations must create, read, preserve, validate, and present knowledge without redefining its meaning.

The relationship between KS-0001 and the constitutional foundation can be summarized as follows:

- TB-0000 defines why The Brain exists.
- TB-0001 defines the principles The Brain must follow.
- TB-0002 defines where the knowledge model belongs in the layered architecture.
- TB-0003 defines how KS-0001 is governed.
- KS-0001 defines the foundational model for structured knowledge.

KS-0001 is successful when it extends the constitutional foundation into a practical, stable, portable, and reviewable model of knowledge without weakening implementation independence, privacy, provenance, governance, or daily usability.

## 3. Knowledge Object Definition

A Knowledge Object is a discrete unit of structured knowledge managed under The Brain Standard.

A Knowledge Object represents knowledge that has been identified, structured, contextualized, and made interpretable through governed metadata, relationships, provenance, lifecycle state, privacy classification, and authority expectations.

A Knowledge Object is not merely a file, note, folder, database row, application record, tag, search result, or source artifact.

Those things may store, display, reference, index, or support a Knowledge Object, but they do not define the Knowledge Object by themselves.

A Knowledge Object SHALL have a stable identity that remains independent of:

- filename;
- folder path;
- vault location;
- database identifier;
- application-specific identifier;
- display title;
- user interface;
- storage backend;
- workflow state;
- agent output;
- implementation-specific behavior.

A Knowledge Object SHALL preserve its meaning when moved, renamed, copied, migrated, exported, imported, displayed differently, indexed, summarized, validated, or processed by an agent or workflow.

A Knowledge Object MUST be interpretable through explicit structure rather than hidden convention.

At minimum, a Knowledge Object SHALL be capable of expressing:

- object identity;
- object type where applicable;
- human-readable title or label;
- required metadata;
- relationships to other Knowledge Objects where applicable;
- source references where applicable;
- provenance;
- lifecycle state;
- authority level where applicable;
- privacy classification;
- validation state or validation expectations where applicable.

A Knowledge Object MAY be represented by one or more Knowledge Records.

A Knowledge Object MAY be derived from source material, created through human reasoning, generated through an approved workflow, proposed by an agent, or created through a combination of these sources.

Regardless of how it is created, a Knowledge Object MUST remain distinguishable from the source material, tool, agent, workflow, or implementation that produced or stores it.

A Knowledge Object exists to preserve meaning.

Storage exists to preserve access.

Agents exist to assist interpretation and maintenance.

Workflows exist to coordinate knowledge operations.

Implementations exist to realize the standard in practical systems.

None of those lower or higher operational concerns may redefine the core identity or meaning of a Knowledge Object.

A compliant Knowledge Object SHOULD be understandable to a human reading it directly and interpretable by an AI system or validator operating under The Brain Standard.

A Knowledge Object is successful when its identity, meaning, context, provenance, relationships, privacy expectations, and review state remain understandable even if the surrounding storage system, workflow, agent system, or implementation is replaced.

## 4. Knowledge Record Definition

A Knowledge Record is a structured representation of knowledge created from, about, or in response to source material, human reasoning, agent activity, or governed workflows.

A Knowledge Record is the inspectable representation through which a Knowledge Object is described, preserved, reviewed, validated, related, and used.

A Knowledge Object represents the stable unit of knowledge.

A Knowledge Record represents that knowledge in a form that humans, agents, workflows, validators, storage systems, and implementations can inspect and process.

A Knowledge Record MAY be stored as a Markdown-compatible file, database entry, graph node, object record, API object, or future representation.

The storage format does not define the meaning of the Knowledge Record.

The meaning of the Knowledge Record is defined by its object identity, metadata, content, relationships, provenance, lifecycle state, authority expectations, privacy classification, and governed structure.

A Knowledge Record SHALL remain distinguishable from source material.

Source material may provide evidence, input, context, or reference material.

A Knowledge Record may summarize, extract, classify, interpret, transform, connect, or preserve knowledge from source material, but it is not automatically the same thing as the source material.

A Knowledge Record SHOULD preserve source references when the record depends on source material for evidence, context, accuracy, interpretation, or review.

A Knowledge Record SHALL include enough explicit structure for its associated Knowledge Object to remain understandable outside any single implementation.

At minimum, a Knowledge Record SHALL be capable of expressing:

- the identity of the Knowledge Object it represents;
- the title or human-readable label of the Knowledge Object;
- required metadata;
- content or structured knowledge body;
- source references where applicable;
- provenance;
- relationships where applicable;
- lifecycle state;
- privacy classification;
- authority level where applicable;
- validation expectations where applicable.

A Knowledge Object SHOULD have at least one primary Knowledge Record.

The primary Knowledge Record is the main representation used to inspect, review, preserve, and maintain the Knowledge Object.

A Knowledge Object MAY have additional records, views, exports, summaries, translations, indexes, embeddings, cached representations, or implementation-specific representations.

Additional representations MUST NOT replace the primary Knowledge Record unless a governed process explicitly changes which record is primary.

If multiple Knowledge Records represent the same Knowledge Object, the relationship between those records SHOULD be explicit enough to avoid identity confusion, duplication, or conflicting authority.

A Knowledge Record MAY be created by:

- a human;
- an agent;
- a workflow;
- an import process;
- an extraction process;
- a transformation process;
- a migration process;
- a governed implementation process.

Regardless of how a Knowledge Record is created, it SHOULD remain reviewable.

Where a Knowledge Record is created or modified by an agent or workflow, the record SHOULD preserve enough provenance for a human to understand:

- what created or modified the record;
- what source material was used;
- what transformation occurred;
- what assumptions or classifications were applied;
- whether human review has occurred;
- what lifecycle state applies.

A Knowledge Record MUST NOT silently alter the meaning, identity, provenance, authority, privacy classification, or lifecycle state of a Knowledge Object.

A Knowledge Record MAY evolve over time through revision, review, correction, enrichment, supersession, migration, or reclassification.

When a Knowledge Record changes in a way that affects meaning, provenance, privacy, authority, lifecycle state, validation, or compatibility, the change SHOULD be traceable.

A compliant Knowledge Record SHOULD remain understandable when read directly by a human and structured enough for reliable interpretation by agents, workflows, validators, and implementations.

A Knowledge Record is successful when it preserves the meaning of a Knowledge Object in a durable, explicit, portable, reviewable, privacy-respecting, and implementation-independent form.

## 5. Source Material vs. Knowledge Records

Source Material and Knowledge Records serve different roles within The Brain Standard.

Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, or other artifacts used as evidence, input, or reference material.

A Knowledge Record refers to a structured representation of knowledge created from, about, or in response to source material, human reasoning, agent activity, or governed workflows.

Source Material is evidence, input, context, or reference.

A Knowledge Record is structured knowledge.

The Brain Standard SHALL preserve the distinction between Source Material and Knowledge Records.

A source artifact MAY support a Knowledge Record, but the source artifact is not automatically the same thing as the Knowledge Record.

A Knowledge Record MAY summarize, extract, classify, interpret, transform, connect, or preserve knowledge from Source Material.

A Knowledge Record MUST NOT obscure the fact that it is derived from, related to, or supported by Source Material when that source is materially relevant to the record.

Source Material MAY include:

- documents;
- notes;
- emails;
- messages;
- images;
- audio recordings;
- video recordings;
- datasets;
- PDFs;
- spreadsheets;
- web pages;
- transcripts;
- code files;
- logs;
- forms;
- scans;
- external references;
- other original artifacts.

A Knowledge Record MAY include:

- a summary of source material;
- an extraction from source material;
- a classification of source material;
- an interpretation of source material;
- a structured note about source material;
- a decision derived from source material;
- a relationship created between source material and other knowledge;
- a review record;
- a transformed representation;
- a synthesized knowledge statement;
- a governed object record.

A source artifact MAY be stored inside a compliant repository, linked from a compliant repository, archived externally, or referenced through a durable source reference.

Storage location does not determine whether something is Source Material or a Knowledge Record.

A file stored in a vault is not automatically a Knowledge Record.

A Knowledge Record stored outside a vault is not automatically invalid.

The distinction depends on role, structure, metadata, provenance, and governed meaning.

A Knowledge Record SHOULD preserve source references when source material materially supports the content, interpretation, classification, relationship, decision, or validation of the record.

A source reference SHOULD be sufficient for a future human, agent, workflow, validator, or implementation to understand what source material supports the record.

A Knowledge Record SHOULD NOT copy source material unnecessarily when a durable reference is sufficient.

Duplication MAY be acceptable for preservation, quotation, extraction, backup, review, accessibility, or implementation convenience, but duplication MUST NOT erase the distinction between original source material and structured knowledge.

When a Knowledge Record contains extracted or transformed content from source material, the record SHOULD preserve enough provenance to show:

- what source material was used;
- what portion or aspect of the source was used where applicable;
- who or what performed the extraction or transformation;
- when the extraction or transformation occurred where applicable;
- whether human review occurred;
- whether the transformation changed meaning;
- whether the source remains available.

If Source Material is unavailable, moved, deleted, restricted, corrupted, superseded, or replaced, the Knowledge Record SHOULD remain interpretable where practical.

However, the Knowledge Record SHOULD NOT falsely imply that source support remains available when the source can no longer be verified.

Source availability, source reliability, and source authority MAY be represented by future metadata, provenance, validation, or source-reference specifications.

A compliant implementation MAY store Source Material and Knowledge Records together or separately.

Both approaches may be compliant if the distinction remains clear, traceable, and reviewable.

An implementation MUST NOT rely only on folder location, filename, file extension, application type, or user memory to distinguish Source Material from Knowledge Records when that distinction affects meaning, provenance, validation, privacy, or authority.

The distinction between Source Material and Knowledge Records is successful when future humans, agents, workflows, validators, and implementations can determine:

- what original material exists;
- what structured knowledge was created from or about it;
- what source supports a record;
- what transformation occurred;
- what remains evidence;
- what remains interpretation;
- what remains governed knowledge.

## 6. Object Identity

Object Identity is the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.

Object Identity exists so that a Knowledge Object can remain the same object even when its representation, storage location, display title, filename, format, workflow state, or implementation changes.

A Knowledge Object SHALL have stable identity.

A Knowledge Object MUST NOT depend on a filename, folder path, vault location, database row number, application-specific identifier, tag, search result, URL, user interface state, or agent-generated label as its only identity.

Those identifiers may support discovery, storage, display, indexing, or implementation behavior, but they MUST NOT be the sole source of Knowledge Object identity.

Object Identity SHALL be explicit enough that humans, agents, workflows, validators, storage systems, and implementations can determine whether two representations refer to the same Knowledge Object.

A compliant Knowledge Object SHOULD preserve identity across:

- renaming;
- moving;
- copying;
- migration;
- import;
- export;
- indexing;
- summarization;
- transformation;
- translation;
- backup;
- restoration;
- synchronization;
- implementation replacement.

A Knowledge Object MAY have multiple identifiers used for different purposes.

For example, a Knowledge Object may have:

- a stable object identifier;
- a human-readable title;
- an implementation-specific identifier;
- a storage path;
- a source reference;
- an external reference;
- a legacy identifier;
- a temporary workflow identifier.

Only identifiers governed as Object Identity may define the stable identity of the Knowledge Object.

A human-readable title SHOULD support recognition and usability, but it SHOULD NOT be treated as stable identity.

A storage path SHOULD support retrieval, but it SHOULD NOT be treated as stable identity.

An implementation-specific identifier MAY support application behavior, but it SHOULD NOT be treated as stable identity unless a future governed specification defines how that identifier remains portable and durable.

Object Identity SHOULD be durable enough to support:

- relationships between Knowledge Objects;
- source references;
- provenance;
- citations;
- lifecycle history;
- review history;
- validation;
- migration;
- duplicate detection;
- supersession;
- deprecation;
- import and export;
- long-term maintenance.

A Knowledge Object SHOULD NOT receive a new stable identity merely because it has been renamed, moved, reformatted, reindexed, backed up, restored, summarized, translated, or displayed differently.

A Knowledge Object MAY receive a new stable identity when it becomes a meaningfully different object.

A new stable identity SHOULD be considered when:

- the knowledge meaning materially changes;
- the object is split into multiple independent objects;
- multiple objects are merged into a new object;
- a derivative object is created for a distinct purpose;
- a source artifact is transformed into a governed Knowledge Record;
- a draft object becomes a separately governed object;
- a superseding object replaces an older object while preserving the older object historically.

Changes to Object Identity SHOULD be traceable when they affect relationships, provenance, lifecycle state, authority, privacy classification, validation, import, export, migration, or compatibility.

An implementation MAY generate object identifiers automatically.

An implementation MAY allow humans to assign object identifiers manually.

An implementation MAY use a combination of automatic and human-assigned identifiers.

Regardless of how an identifier is created, the identifier SHOULD remain stable, unique within its intended scope, inspectable, portable, and independent of implementation-specific hidden state.

A future specification MAY define exact identifier formats, uniqueness scopes, collision rules, alias behavior, redirect behavior, merge behavior, split behavior, and migration behavior.

Until such a specification exists, KS-0001 defines the requirement for stable Object Identity but does not mandate a specific identifier format.

Object Identity is successful when a Knowledge Object can be reliably recognized as the same object across storage changes, implementation changes, workflow operations, agent activity, migration, export, import, and long-term maintenance.

## 7. Required Metadata

Required Metadata is the metadata that MUST be present for a Knowledge Object or Knowledge Record to be valid under KS-0001.

Required Metadata exists to make knowledge identifiable, interpretable, traceable, reviewable, privacy-respecting, and portable across implementations.

KS-0001 defines required metadata at the conceptual level.

KS-0001 does not define exact field names, serialization formats, schema syntax, validation syntax, or storage placement for required metadata.

A future specification MAY define exact metadata fields, formats, allowed values, schema requirements, and validation rules.

Until such a specification exists, compliant Knowledge Objects and Knowledge Records MUST preserve the meaning of the required metadata categories defined in this section.

At minimum, a Knowledge Object or Knowledge Record SHALL be capable of expressing:

- object identity;
- title or human-readable label;
- object type where applicable;
- lifecycle state;
- privacy classification;
- provenance;
- source references where applicable;
- relationships where applicable;
- authority level where applicable;
- creation date or creation context where applicable;
- last updated date or revision context where applicable;
- validation state or validation expectations where applicable.

Required Metadata MUST be explicit enough that a future human, agent, workflow, validator, storage system, or implementation can understand the basic identity, status, context, and handling expectations of the knowledge.

Required Metadata MUST NOT exist only in hidden application state when that metadata affects meaning, identity, provenance, lifecycle state, privacy, authority, validation, or compatibility.

Required Metadata MAY be represented in front matter, document headers, structured fields, database columns, graph properties, API fields, sidecar metadata, or future representation formats.

The representation method may vary by implementation.

The meaning of required metadata MUST remain portable and inspectable.

### 7.1 Object Identity

A Knowledge Object or Knowledge Record SHALL include or reference stable Object Identity.

Object Identity identifies what knowledge object the record represents.

Object Identity MUST remain independent of filename, folder path, storage location, display title, application-specific identifier, workflow state, or user interface.

A future specification MAY define the exact identifier format.

### 7.2 Title or Human-Readable Label

A Knowledge Object or Knowledge Record SHALL include a title or human-readable label.

The title or label exists to support human recognition, review, navigation, and communication.

A title or label SHOULD be concise, descriptive, and understandable without requiring hidden implementation context.

A title or label SHOULD NOT be treated as stable Object Identity unless a future specification explicitly defines that behavior.

### 7.3 Object Type

A Knowledge Object or Knowledge Record SHOULD identify its object type where applicable.

Object type helps humans, agents, workflows, validators, and implementations understand what kind of knowledge is being represented.

Examples of future object types MAY include concept, person, organization, source, project, decision, procedure, reference, event, claim, task, note, or other governed types.

KS-0001 does not approve or require a complete object-type list.

A future knowledge specification MAY define allowed object types, type hierarchy, type metadata, and validation rules.

Until then, object type SHOULD be used carefully and MUST NOT become an implementation-specific hidden assumption.

### 7.4 Lifecycle State

A Knowledge Object or Knowledge Record SHALL include or support a lifecycle state where lifecycle status affects interpretation, review, authority, publication, supersession, deprecation, validation, or workflow behavior.

Lifecycle state helps determine whether knowledge is draft, under review, approved, superseded, deprecated, rejected, or otherwise governed by future knowledge lifecycle rules.

KS-0001 does not define the complete lifecycle state system for all Knowledge Objects.

A future specification MAY define exact knowledge lifecycle states and allowed transitions.

Until then, lifecycle state SHOULD remain compatible with the governance expectations defined by TB-0003.

### 7.5 Privacy Classification

A Knowledge Object or Knowledge Record SHALL include or support privacy classification.

Privacy classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, and agent access expectations.

Privacy classification MUST be explicit enough that humans, agents, workflows, storage systems, validators, and implementations can avoid exposing restricted knowledge by accident.

A future privacy specification MAY define exact privacy classes, access rules, inheritance behavior, redaction behavior, and validation rules.

Until then, privacy-sensitive knowledge SHOULD be handled conservatively.

### 7.6 Provenance

A Knowledge Object or Knowledge Record SHALL include or support provenance.

Provenance identifies the origin, source, reasoning, creator, agent, workflow, transformation, or evidence associated with the knowledge.

Provenance SHOULD be sufficient for a future human, agent, workflow, validator, or implementation to understand where the knowledge came from and how it was created or changed.

Where knowledge is created or modified by an agent, workflow, import, extraction, transformation, or migration process, provenance SHOULD identify that process where practical.

### 7.7 Source References

A Knowledge Object or Knowledge Record SHALL include source references where source material materially supports the content, interpretation, classification, relationship, decision, or validation of the record.

A source reference SHOULD identify the relevant source material clearly enough for future review.

Source references MAY point to source material stored inside a repository, stored externally, archived separately, or referenced through another durable mechanism.

A future specification MAY define source-reference formats, source identifiers, citation behavior, link durability requirements, and source availability metadata.

### 7.8 Relationships

A Knowledge Object or Knowledge Record SHALL support relationships where relationships are needed to preserve meaning, context, provenance, dependency, hierarchy, sequence, evidence, supersession, derivation, or governance.

Relationships SHOULD be explicit when they affect interpretation or future use.

A relationship MUST NOT depend only on folder proximity, filename similarity, tag coincidence, search ranking, or hidden application behavior when that relationship affects meaning.

A future relationship specification MAY define relationship types, directionality, cardinality, validation rules, and serialization formats.

### 7.9 Authority Level

A Knowledge Object or Knowledge Record SHALL include or support authority level where authority affects interpretation, governance, review, trust, publication, validation, or downstream use.

Authority level helps humans, agents, workflows, validators, and implementations understand the governance weight or interpretive authority of the object or record.

Authority level MUST NOT be confused with factual truth, confidence score, popularity, or usefulness.

A future specification MAY define authority levels for Knowledge Objects and Knowledge Records.

### 7.10 Creation and Revision Context

A Knowledge Object or Knowledge Record SHALL include or support creation and revision context where that context affects provenance, reviewability, lifecycle state, authority, validation, or compatibility.

Creation context MAY include creation date, creator, originating workflow, source import, agent action, or initial source material.

Revision context MAY include last updated date, editor, agent, workflow, reason for change, validation result, or review state.

KS-0001 does not require a complete change-history model for every Knowledge Record.

However, changes that affect meaning, identity, provenance, privacy, authority, lifecycle state, validation, or compatibility SHOULD remain traceable.

### 7.11 Validation State or Validation Expectations

A Knowledge Object or Knowledge Record SHALL include or support validation state or validation expectations where validation affects compliance, review, workflow behavior, import, export, migration, publication, or implementation interoperability.

Validation state MAY indicate whether a record is unchecked, valid, invalid, partially valid, needs review, or governed by future validation states.

KS-0001 does not define exact validation states.

A future validation specification MAY define required validation fields, states, rules, validators, error behavior, and compatibility expectations.

### 7.12 Required Metadata Success

Required Metadata is successful when a Knowledge Object or Knowledge Record remains identifiable, interpretable, traceable, reviewable, privacy-respecting, portable, and validatable without depending on hidden application state, folder placement, filenames, workflow memory, or implementation-specific assumptions.

## 8. Optional Metadata

Optional Metadata is metadata that MAY be included when useful but is not required for basic validity under KS-0001.

Optional Metadata exists to improve interpretation, navigation, discovery, validation, automation, review, interoperability, usability, or long-term maintenance without making routine knowledge capture unnecessarily burdensome.

Optional Metadata SHOULD remain clearly distinguishable from Required Metadata.

A Knowledge Object or Knowledge Record MUST NOT be treated as invalid merely because Optional Metadata is absent, unless a future governed specification, workflow, implementation profile, or object-type rule explicitly requires that metadata for a narrower scope.

KS-0001 defines Optional Metadata at the conceptual level.

KS-0001 does not define exact optional field names, serialization formats, allowed values, schema syntax, validation syntax, or storage placement.

A future specification MAY define optional metadata fields, recommended metadata profiles, object-type-specific metadata, implementation profiles, or validation rules.

Optional Metadata MAY include:

- aliases;
- alternate titles;
- descriptions;
- summaries;
- keywords;
- tags;
- topics;
- categories;
- object status notes;
- review notes;
- quality notes;
- confidence notes;
- source reliability notes;
- source availability notes;
- extraction notes;
- transformation notes;
- version notes;
- revision notes;
- related workflows;
- related agents;
- related implementations;
- related standards;
- related decisions;
- external references;
- citations;
- backlinks;
- forward links;
- semantic relationships;
- embedding references;
- index references;
- access notes;
- publication notes;
- archival notes;
- migration notes;
- interoperability notes.

Optional Metadata MAY support human use, agent use, workflow execution, validation, search, filtering, sorting, visualization, summarization, reporting, migration, publication, or implementation-specific optimization.

Optional Metadata SHOULD be explicit when it affects interpretation.

Optional Metadata SHOULD NOT create hidden meaning that only one tool, plugin, workflow, agent, database, or implementation can understand.

Optional Metadata MAY be generated manually, automatically, or through a combination of human, agent, workflow, import, extraction, transformation, validation, or implementation processes.

Agent-generated Optional Metadata SHOULD be reviewable when it affects interpretation, classification, relationship creation, privacy, authority, source handling, validation, or downstream workflow behavior.

Optional Metadata SHOULD NOT silently override Required Metadata.

If Optional Metadata appears to conflict with Required Metadata, Required Metadata SHALL take precedence unless a governed process revises the required metadata.

Optional Metadata MAY become Required Metadata in a future standard or specification if governance determines that the metadata is necessary for identity, interpretation, provenance, privacy, validation, compatibility, interoperability, or long-term maintainability.

When Optional Metadata becomes required, the change SHOULD include compatibility review and migration guidance where applicable.

Optional Metadata SHOULD remain practical.

The Brain Standard SHOULD avoid encouraging excessive optional metadata that increases cognitive load without durable value.

Optional Metadata is justified when it materially improves:

- human understanding;
- AI interpretation;
- search and discovery;
- relationship mapping;
- provenance clarity;
- reviewability;
- privacy handling;
- validation quality;
- workflow reliability;
- migration;
- interoperability;
- publication;
- maintenance;
- long-term durability.

### 8.1 Aliases and Alternate Titles

A Knowledge Object or Knowledge Record MAY include aliases or alternate titles.

Aliases and alternate titles support search, recognition, migration, import, export, duplicate detection, and human usability.

Aliases and alternate titles SHOULD NOT replace the primary title or stable Object Identity.

If an alias becomes the preferred title, the change SHOULD be traceable where it affects recognition, relationships, citations, source references, or compatibility.

### 8.2 Descriptions and Summaries

A Knowledge Object or Knowledge Record MAY include descriptions or summaries.

Descriptions and summaries help humans, agents, workflows, validators, and implementations understand the purpose, scope, or contents of the object or record.

A summary SHOULD preserve the meaning of the underlying record.

A summary MUST NOT be treated as a replacement for the full Knowledge Record unless a governed process explicitly defines that behavior.

Agent-generated summaries SHOULD be reviewable when they affect interpretation, publication, privacy, authority, or downstream use.

### 8.3 Keywords, Tags, Topics, and Categories

A Knowledge Object or Knowledge Record MAY include keywords, tags, topics, or categories.

These metadata elements support navigation, search, grouping, filtering, discovery, visualization, and automation.

Keywords, tags, topics, and categories SHOULD NOT be the only source of critical meaning.

If a tag or category affects object type, lifecycle state, privacy classification, authority, validation, or workflow behavior, that meaning SHOULD be represented through governed metadata rather than hidden convention.

A future specification MAY define controlled vocabularies, tag behavior, topic structures, category rules, or classification metadata.

### 8.4 Notes and Review Comments

A Knowledge Object or Knowledge Record MAY include notes, review comments, quality notes, confidence notes, or editorial comments.

These notes may help preserve context, uncertainty, review status, assumptions, limitations, or future maintenance needs.

Review comments SHOULD remain distinguishable from approved knowledge content.

A note or comment MUST NOT become authoritative merely because it appears near governed content.

Where review comments affect lifecycle state, approval, authority, privacy, or validation, the relevant governed metadata SHOULD be updated rather than relying only on informal notes.

### 8.5 Source Reliability and Availability Notes

A Knowledge Object or Knowledge Record MAY include source reliability notes or source availability notes.

Source reliability notes may describe uncertainty, limitations, quality concerns, bias concerns, freshness concerns, or review concerns related to source material.

Source availability notes may describe whether source material is available, missing, restricted, moved, archived, superseded, corrupted, or externally hosted.

These notes MAY support review, validation, maintenance, migration, and future source-reference specifications.

Source reliability notes SHOULD NOT be confused with authority level unless a future governed specification defines that relationship.

### 8.6 Workflow, Agent, and Implementation References

A Knowledge Object or Knowledge Record MAY reference related workflows, agents, or implementations.

These references may help explain how the object or record was created, transformed, validated, reviewed, migrated, published, or maintained.

Workflow, agent, and implementation references SHOULD remain subordinate to the Knowledge Object’s identity, metadata, provenance, lifecycle state, authority, and privacy classification.

A workflow, agent, or implementation reference MUST NOT redefine the meaning of a Knowledge Object or Knowledge Record.

### 8.7 External References and Citations

A Knowledge Object or Knowledge Record MAY include external references or citations.

External references and citations may support evidence, attribution, source traceability, research, publication, review, or interoperability.

External references SHOULD be durable where practical.

External references SHOULD NOT be the only source of critical meaning unless a future governed specification defines how that dependency is preserved, validated, and migrated.

Where an external reference materially supports a Knowledge Record, it SHOULD be treated as a source reference rather than only optional convenience metadata.

### 8.8 Indexing, Embedding, and Search Metadata

A Knowledge Object or Knowledge Record MAY include indexing, embedding, search, retrieval, or discovery metadata.

This metadata may support search engines, vector indexes, graph systems, recommendation systems, validation tools, or AI-assisted navigation.

Indexing and embedding metadata MUST NOT become the only source of knowledge meaning.

A generated embedding, index entry, search score, ranking, cache, or retrieval hint MUST NOT override explicit metadata, provenance, relationships, lifecycle state, authority, privacy classification, or source references.

Indexing and embedding metadata SHOULD be regenerable or replaceable where practical.

### 8.9 Publication, Archival, and Migration Notes

A Knowledge Object or Knowledge Record MAY include publication notes, archival notes, or migration notes.

Publication notes may describe whether knowledge has been prepared for sharing, export, public release, internal distribution, or downstream use.

Archival notes may describe preservation status, historical value, restricted use, or long-term storage expectations.

Migration notes may describe prior identifiers, prior locations, prior formats, conversion steps, compatibility concerns, or migration validation results.

These notes SHOULD support traceability without redefining Object Identity or Required Metadata.

### 8.10 Optional Metadata Success

Optional Metadata is successful when it improves interpretation, navigation, discovery, automation, validation, review, interoperability, migration, or maintenance without creating hidden requirements, unnecessary cognitive burden, implementation lock-in, or confusion with Required Metadata.

## 9. Relationships Between Knowledge Objects

Relationships are explicit connections between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, or other governed entities.

Relationships exist to preserve context, meaning, provenance, dependency, hierarchy, sequence, evidence, derivation, supersession, reviewability, and navigation.

A Knowledge Object MAY relate to one or more other Knowledge Objects.

A Knowledge Record MAY express relationships on behalf of the Knowledge Object it represents.

Relationships SHOULD be explicit when they affect interpretation, validation, provenance, lifecycle state, authority, privacy, workflow behavior, source traceability, or long-term maintenance.

A relationship MUST NOT depend only on folder proximity, filename similarity, tag coincidence, search ranking, visual placement, application state, or agent inference when that relationship affects meaning.

Those signals may assist discovery, recommendation, indexing, or navigation, but they do not replace explicit governed relationships.

Relationships SHOULD be durable enough that they remain understandable when knowledge is moved, renamed, migrated, exported, imported, indexed, displayed differently, or processed by agents and workflows.

KS-0001 defines relationships at the conceptual level.

KS-0001 does not define exact relationship field names, syntax, serialization formats, relationship-type vocabularies, graph schemas, directionality rules, cardinality rules, or validation rules.

A future relationship specification MAY define those details.

Until such a specification exists, compliant Knowledge Objects and Knowledge Records SHOULD preserve the meaning of relationships clearly enough for humans, agents, workflows, validators, and implementations to interpret them.

Relationships MAY express:

- association;
- dependency;
- hierarchy;
- containment;
- sequence;
- derivation;
- citation;
- source support;
- evidence;
- contradiction;
- refinement;
- duplication;
- similarity;
- supersession;
- deprecation;
- replacement;
- ownership;
- responsibility;
- workflow participation;
- implementation support;
- governance relevance;
- review relevance.

A relationship SHOULD identify the related object, record, source, decision, workflow, implementation, or entity clearly enough to support future review.

A relationship SHOULD preserve direction where direction affects meaning.

For example, “depends on” and “is depended on by” are related but not identical.

A relationship SHOULD preserve type where type affects meaning.

For example, “cites,” “supersedes,” “duplicates,” “derives from,” and “contradicts” express different kinds of relationship and should not be collapsed into a generic link when the distinction matters.

A relationship SHOULD preserve context where context affects interpretation.

Relationship context MAY include:

- why the relationship exists;
- who or what created the relationship;
- when the relationship was created where applicable;
- what source material supports the relationship;
- whether the relationship has been reviewed;
- whether the relationship is inferred, proposed, validated, or approved;
- whether the relationship affects lifecycle state, authority, privacy, or validation.

Relationships MAY be created by humans, agents, workflows, imports, transformations, migrations, validators, or implementations.

Agent-created or workflow-created relationships SHOULD remain reviewable when they affect interpretation, provenance, authority, privacy, lifecycle state, validation, publication, or downstream use.

A relationship MUST NOT silently alter the identity or meaning of a Knowledge Object.

A relationship MAY change how a Knowledge Object is interpreted, navigated, reviewed, validated, or used, but the relationship itself SHOULD remain explicit and traceable when it materially affects meaning.

Relationships SHOULD preserve source distinction.

A relationship between a Knowledge Record and Source Material SHOULD make clear whether the source provides evidence, context, origin, attribution, support, contradiction, or reference.

A relationship between two Knowledge Objects SHOULD make clear whether the relationship is conceptual, evidential, procedural, hierarchical, historical, derivative, governance-related, or implementation-related where that distinction matters.

Relationships SHOULD preserve privacy boundaries.

A relationship MUST NOT expose restricted knowledge merely because another object is public, less restricted, or more broadly accessible.

Where a relationship crosses privacy boundaries, the relationship SHOULD be handled conservatively and according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationships SHOULD support portability.

A relationship SHOULD remain understandable outside a single application, database, plugin, graph view, search index, or user interface.

Implementation-specific links MAY support convenience, but they SHOULD NOT be the only representation of a relationship when the relationship affects meaning.

A future specification MAY define relationship identifiers, relationship records, graph structures, backlinks, forward links, relationship validation, inferred relationships, relationship confidence, relationship provenance, and relationship lifecycle behavior.

Until then, KS-0001 requires that meaningful relationships remain explicit, inspectable, portable, and reviewable.

Relationships are successful when future humans, agents, workflows, validators, and implementations can determine:

- what entities are connected;
- what kind of connection exists;
- why the connection matters;
- whether the connection is source-supported;
- whether the connection is inferred or reviewed;
- whether the connection affects meaning, authority, privacy, lifecycle state, validation, or governance;
- whether the connection remains valid across migration, export, import, and implementation replacement.

## 10. Provenance and Source References

Provenance and Source References preserve the origin, evidence, context, transformation history, and reviewability of Knowledge Objects and Knowledge Records.

Provenance refers to information that identifies where knowledge came from, how it was created, who or what created it, what Source Material supports it, what transformations occurred, and what review state applies.

A Source Reference is a traceable reference from a Knowledge Record to Source Material that supports, explains, or contextualizes the record.

Provenance and Source References are related but not identical.

Provenance explains origin, creation, transformation, and responsibility.

Source References identify supporting, originating, contextual, or evidentiary material.

A Knowledge Object or Knowledge Record SHALL include or support provenance.

A Knowledge Record SHALL include Source References when Source Material materially supports the content, interpretation, classification, relationship, decision, validation, or authority of the record.

A Knowledge Record SHOULD NOT imply source support when no source is available, no source was used, or the source cannot be verified.

Provenance SHOULD be explicit enough for a future human, agent, workflow, validator, or implementation to understand:

- where the knowledge came from;
- what Source Material supports it where applicable;
- who or what created it;
- who or what modified it where applicable;
- what workflow, agent, import, extraction, transformation, migration, or review process was involved where applicable;
- whether the knowledge was copied, summarized, extracted, interpreted, transformed, synthesized, or generated;
- whether human review occurred;
- whether the source remains available where applicable.

Source References SHOULD be explicit enough for a future human, agent, workflow, validator, or implementation to locate, identify, or understand the relevant source material.

A Source Reference MAY refer to:

- a file stored in a repository;
- a file stored outside a repository;
- a document;
- an email;
- a message;
- an image;
- an audio recording;
- a video recording;
- a dataset;
- a web page;
- a database record;
- a code file;
- a transcript;
- a scan;
- a physical artifact;
- an external citation;
- another Knowledge Object or Knowledge Record;
- another governed document.

Source References MAY use filenames, paths, object identifiers, source identifiers, URLs, citations, archive references, external identifiers, repository references, or future governed formats.

However, a Source Reference SHOULD NOT depend only on a fragile location when a more durable identifier or contextual reference is practical.

A future source-reference specification MAY define exact source-reference formats, source identifiers, citation rules, archive rules, source availability metadata, link durability requirements, validation rules, and migration behavior.

Until such a specification exists, KS-0001 requires Source References to remain traceable, inspectable, and understandable.

Provenance SHOULD distinguish between:

- original source material;
- extracted content;
- summarized content;
- interpreted content;
- transformed content;
- synthesized knowledge;
- agent-generated content;
- workflow-generated content;
- human-authored content;
- reviewed content;
- approved content;
- migrated content.

A Knowledge Record SHOULD preserve enough provenance to avoid confusing evidence with interpretation.

A quotation, extraction, summary, classification, inference, and decision are not the same kind of knowledge activity.

Where the distinction affects meaning, authority, validation, review, privacy, or downstream use, the distinction SHOULD be explicit.

Agent-created or agent-modified Knowledge Records SHOULD preserve provenance identifying the agent, workflow, instruction, source material, transformation, and review state where practical.

Workflow-created or workflow-modified Knowledge Records SHOULD preserve provenance identifying the workflow, trigger, actor, source material, transformation, output, and review state where practical.

Human-created or human-modified Knowledge Records SHOULD preserve provenance identifying the creator, editor, review state, or reason for change where that information affects meaning, authority, validation, privacy, or compatibility.

Provenance SHOULD preserve privacy boundaries.

A provenance record or Source Reference MUST NOT expose restricted knowledge merely to improve traceability.

Where provenance or source references involve restricted material, the record SHOULD preserve enough traceability for authorized review without unnecessarily exposing the restricted content.

If Source Material is unavailable, moved, deleted, restricted, corrupted, superseded, or replaced, the Knowledge Record SHOULD remain interpretable where practical.

The Knowledge Record SHOULD indicate that the source is unavailable, restricted, uncertain, superseded, or otherwise changed when that condition affects interpretation, validation, authority, or review.

A Knowledge Record MAY rely on human reasoning, memory, observation, or analysis without external Source Material.

When no external Source Material exists, provenance SHOULD still identify the origin or basis of the knowledge where practical.

Source References SHOULD support portability.

A Source Reference SHOULD remain understandable across migration, export, import, backup, restoration, storage replacement, and implementation replacement.

Implementation-specific links MAY support convenience, but they SHOULD NOT be the only representation of a Source Reference when the reference affects meaning, provenance, validation, authority, or review.

Provenance and Source References are successful when future humans, agents, workflows, validators, and implementations can determine:

- where knowledge came from;
- what evidence supports it where applicable;
- what transformation occurred;
- who or what created or modified it where applicable;
- whether the source remains available;
- whether the record contains evidence, interpretation, extraction, summary, synthesis, or decision;
- whether the knowledge has been reviewed;
- whether privacy boundaries are preserved;
- whether the record remains traceable across migration and implementation replacement.

## 11. Lifecycle State

Lifecycle State describes the current governed state of a Knowledge Object or Knowledge Record.

Lifecycle State helps humans, agents, workflows, validators, storage systems, and implementations understand whether knowledge is proposed, active, under review, approved, deprecated, superseded, rejected, archived, or otherwise governed by future lifecycle rules.

KS-0001 defines Lifecycle State at the conceptual level.

KS-0001 does not define the complete lifecycle state system for all Knowledge Objects and Knowledge Records.

A future lifecycle specification MAY define exact lifecycle states, allowed transitions, transition rules, validation behavior, workflow effects, approval requirements, archival behavior, and migration expectations.

Until such a specification exists, Lifecycle State SHOULD remain compatible with the governance expectations defined by TB-0003.

A Knowledge Object or Knowledge Record SHALL include or support Lifecycle State when lifecycle status affects interpretation, review, authority, publication, supersession, deprecation, validation, workflow behavior, privacy handling, or downstream use.

Lifecycle State SHOULD be explicit enough that a future human, agent, workflow, validator, storage system, or implementation can understand how the Knowledge Object or Knowledge Record should be treated.

Lifecycle State MUST NOT depend only on folder location, filename, tag, color, user interface state, plugin field, search ranking, workflow memory, or hidden application state when lifecycle status affects meaning or use.

Those signals may support usability, but they MUST NOT replace explicit governed lifecycle metadata when lifecycle status matters.

Lifecycle State MAY indicate whether a Knowledge Object or Knowledge Record is:

- draft;
- under review;
- approved;
- rejected;
- deprecated;
- superseded;
- archived;
- experimental;
- proposed;
- imported;
- needs review;
- needs validation;
- restricted;
- governed by a future lifecycle state.

This list is descriptive, not a complete approved lifecycle vocabulary.

KS-0001 does not approve every listed value as a required lifecycle state.

A future specification SHOULD define which lifecycle values are valid for Knowledge Objects and Knowledge Records.

Lifecycle State SHOULD remain distinguishable from Authority Level.

Lifecycle State describes the current governance or review status of the object or record.

Authority Level describes the interpretive or governance weight assigned to the object, record, source, document, or decision.

For example, a Knowledge Record may be high authority but superseded, or low authority but approved for a narrow purpose.

Lifecycle State SHOULD remain distinguishable from Validation State.

Lifecycle State describes review, approval, supersession, deprecation, rejection, or other governed status.

Validation State describes whether the record satisfies structural, metadata, provenance, relationship, privacy, compatibility, or implementation expectations.

For example, a Knowledge Record may be approved but later fail validation after a schema changes.

Lifecycle State SHOULD remain distinguishable from Privacy Classification.

Lifecycle State describes governed status.

Privacy Classification describes permitted visibility, access, exposure, routing, export, indexing, synchronization, publication, backup, and agent access expectations.

For example, a Knowledge Record may be approved but restricted.

Lifecycle transitions SHOULD be traceable when they affect meaning, authority, privacy, validation, relationships, source references, provenance, compatibility, workflow behavior, publication, or downstream use.

A lifecycle transition MAY occur because of:

- human review;
- approval;
- rejection;
- supersession;
- deprecation;
- archival;
- correction;
- reclassification;
- validation failure;
- validation success;
- import;
- migration;
- workflow execution;
- agent-assisted review;
- governance decision;
- implementation maintenance.

Agent-assisted lifecycle changes SHOULD remain reviewable when they affect meaning, authority, privacy, validation, publication, supersession, deprecation, rejection, or governance.

Workflow-driven lifecycle changes SHOULD preserve enough traceability to show:

- what lifecycle state changed;
- what object or record changed;
- what triggered the change;
- who or what performed the change;
- what source material or evidence was involved where applicable;
- whether human review occurred;
- whether authority, privacy, validation, provenance, or compatibility was affected.

A Knowledge Object or Knowledge Record MUST NOT be treated as approved merely because it exists, is stored, is indexed, is linked, is referenced, is used by a workflow, appears in an implementation, or was generated by an agent.

Approval SHOULD be explicit when approval affects authority, publication, downstream use, or governance.

A Knowledge Object or Knowledge Record MUST NOT be treated as superseded, deprecated, rejected, archived, or invalid merely because it was moved, renamed, hidden from a view, excluded from search, or omitted from a workflow.

Those actions may reflect lifecycle status only when the lifecycle state is explicitly represented or traceably governed.

Lifecycle State SHOULD support historical preservation.

A superseded, deprecated, rejected, or archived Knowledge Object or Knowledge Record MAY remain historically useful.

Historical availability does not mean the object or record remains current authority.

Lifecycle State SHOULD make current use and historical status distinguishable.

Lifecycle State SHOULD preserve relationships and provenance.

When a Knowledge Object or Knowledge Record is superseded, deprecated, rejected, archived, or replaced, relationships to prior versions, replacement objects, supporting sources, decisions, workflows, or review records SHOULD remain traceable where practical.

Lifecycle State SHOULD preserve privacy boundaries.

A lifecycle transition MUST NOT expose restricted knowledge merely because the object or record becomes approved, published, superseded, deprecated, archived, or reviewed.

If lifecycle status affects visibility, access, export, publication, indexing, synchronization, backup, or agent access, privacy classification SHOULD be checked before the lifecycle transition is applied.

Lifecycle State SHOULD support portability.

Lifecycle status SHOULD remain understandable across migration, export, import, backup, restoration, implementation replacement, and workflow replacement.

Implementation-specific lifecycle fields MAY support convenience, but they SHOULD NOT be the only representation of lifecycle state when lifecycle status affects meaning, authority, validation, privacy, or use.

Lifecycle State is successful when future humans, agents, workflows, validators, and implementations can determine:

- what state a Knowledge Object or Knowledge Record is in;
- whether the object or record is proposed, reviewable, approved, superseded, deprecated, rejected, archived, or governed by another lifecycle state;
- whether the lifecycle state affects authority, privacy, validation, publication, relationships, provenance, or downstream use;
- what caused a lifecycle transition where applicable;
- whether human review occurred where applicable;
- whether the object or record remains current, historical, restricted, or superseded;
- whether lifecycle meaning survives migration and implementation replacement.

## 12. Human and AI Readability

Human and AI readability means that Knowledge Objects and Knowledge Records SHOULD be understandable to humans and interpretable by AI systems operating under The Brain Standard.

Human readability exists so that knowledge remains inspectable, reviewable, maintainable, and trustworthy without requiring a specific application, database, plugin, agent, workflow, or implementation.

AI readability exists so that agents, workflows, validators, search systems, and future implementations can assist with classification, summarization, relationship discovery, validation, migration, maintenance, and review without redefining knowledge meaning.

A Knowledge Object or Knowledge Record SHOULD be readable enough for a human to understand its purpose, meaning, context, source support, provenance, lifecycle state, privacy classification, authority expectations, and relationships where applicable.

A Knowledge Object or Knowledge Record SHOULD be structured enough for AI systems and validators to identify its basic knowledge model elements.

At minimum, a readable Knowledge Object or Knowledge Record SHOULD make the following understandable where applicable:

- object identity;
- title or human-readable label;
- object type;
- required metadata;
- optional metadata;
- knowledge content;
- source references;
- provenance;
- relationships;
- lifecycle state;
- authority level;
- privacy classification;
- validation expectations;
- review status;
- implementation-independent meaning.

Human readability MUST NOT depend only on hidden application state, proprietary interface behavior, visual layout, plugin behavior, undocumented database fields, agent memory, or workflow memory.

AI readability MUST NOT require hidden prompts, undocumented assumptions, non-portable embeddings, proprietary indexes, or implementation-specific behavior as the only way to interpret the Knowledge Object or Knowledge Record.

A compliant implementation MAY improve readability through user interfaces, graph views, search indexes, summaries, previews, rendered views, structured editors, forms, templates, or AI-assisted explanations.

However, those conveniences MUST NOT become the only place where critical meaning exists.

Critical meaning SHOULD be preserved in explicit structure, metadata, relationships, provenance, and governed content.

A Knowledge Record SHOULD remain understandable when read directly in its durable representation where practical.

For Markdown-compatible representations, this means that the record SHOULD remain useful as plain text even if rendered views, plugins, databases, or applications are unavailable.

For database, graph, API, or other structured representations, this means that the record SHOULD be exportable or inspectable in a way that preserves its meaning outside the original implementation.

Human-readable language SHOULD be clear, direct, and sufficient for review.

A Knowledge Record SHOULD avoid unnecessary ambiguity when ambiguity affects meaning, authority, validation, privacy, source interpretation, or downstream use.

AI-readable structure SHOULD be explicit, consistent, and inspectable.

AI systems SHOULD be able to distinguish:

- governed content from informal notes;
- original evidence from interpretation;
- source material from Knowledge Records;
- required metadata from optional metadata;
- current knowledge from superseded or deprecated knowledge;
- approved knowledge from draft or proposed knowledge;
- public knowledge from restricted knowledge;
- human-authored content from agent-generated or workflow-generated content where applicable.

A Knowledge Record SHOULD NOT rely on stylistic convention alone to communicate governed meaning.

For example, capitalization, color, indentation, folder placement, emoji, visual grouping, tag coincidence, or display order SHOULD NOT be the only representation of lifecycle state, privacy classification, authority, validation, provenance, or relationship meaning.

Templates MAY support readability.

Forms MAY support readability.

Schemas MAY support readability.

Rendered interfaces MAY support readability.

AI summaries MAY support readability.

None of these replace the requirement that critical meaning remain explicit and reviewable.

Agent-generated interpretations, classifications, summaries, or relationships SHOULD remain reviewable when they affect meaning, authority, privacy, lifecycle state, validation, publication, or downstream use.

AI systems SHOULD assist interpretation without becoming the sole authority for meaning.

Where an AI system proposes a change that affects identity, meaning, provenance, source references, relationships, lifecycle state, authority, privacy classification, or validation, the change SHOULD be traceable and reviewable.

Human and AI readability SHOULD support accessibility.

Knowledge Records SHOULD avoid unnecessary formatting complexity when simpler structure preserves meaning adequately.

A future specification MAY define readability profiles, templates, schema patterns, plain-text requirements, accessibility expectations, AI-parsing requirements, or validation rules.

Until such a specification exists, KS-0001 requires that Knowledge Objects and Knowledge Records preserve meaning in a form that is practical for humans to review and structured enough for AI systems to interpret.

Human and AI readability is successful when future humans, agents, workflows, validators, and implementations can determine:

- what the Knowledge Object or Knowledge Record means;
- what metadata applies;
- what Source Material supports it where applicable;
- what provenance applies;
- what relationships exist;
- what lifecycle state applies;
- what authority expectations apply;
- what privacy classification applies;
- whether the record is draft, reviewed, approved, superseded, deprecated, restricted, or otherwise governed;
- whether critical meaning survives migration, export, import, and implementation replacement.

## 13. Compatibility Requirements

Compatibility Requirements define what Knowledge Objects, Knowledge Records, standards, specifications, storage systems, agents, workflows, validators, and implementations must preserve in order to remain compatible with KS-0001.

Compatibility exists so that knowledge can survive tool changes, storage changes, workflow changes, agent changes, schema evolution, migration, export, import, and long-term maintenance.

A compatible system MUST preserve the meaning, identity, provenance, source distinction, relationships, lifecycle state, authority expectations, privacy classification, validation expectations, and human-reviewability of Knowledge Objects and Knowledge Records.

Compatibility with KS-0001 does not require every implementation to use the same storage format, database schema, file layout, user interface, workflow engine, agent framework, plugin system, or application design.

Compatibility requires preserving the knowledge model defined by this standard.

An implementation MAY store Knowledge Records as Markdown-compatible files, database rows, graph nodes, API objects, structured documents, or future formats.

A storage format is compatible only when it preserves enough explicit structure for Knowledge Objects and Knowledge Records to remain identifiable, interpretable, portable, reviewable, traceable, and privacy-respecting.

A compatible implementation MUST NOT redefine Knowledge Object meaning through storage location, filename, database identifier, application behavior, user interface state, workflow memory, agent memory, hidden prompt context, plugin behavior, or undocumented convention.

Those mechanisms may support convenience, performance, navigation, automation, or implementation behavior, but they MUST NOT be the sole source of critical knowledge meaning.

A compatible implementation SHOULD preserve:

- Object Identity;
- Knowledge Record structure;
- Required Metadata;
- meaningful Optional Metadata where applicable;
- Source Material distinction;
- Source References;
- provenance;
- relationships;
- Lifecycle State;
- Authority Level where applicable;
- Privacy Classification;
- validation state or validation expectations where applicable;
- human and AI readability;
- migration and export interpretability.

A compatible implementation SHOULD support export or inspection in a durable form where practical.

Exported knowledge SHOULD remain understandable without requiring the original application, database, plugin, workflow engine, agent environment, or user interface.

A compatible implementation SHOULD support migration without silently changing object identity, meaning, provenance, relationships, lifecycle state, authority, privacy classification, or validation expectations.

If migration changes meaning, structure, identity, provenance, relationships, lifecycle state, authority, privacy classification, or validation expectations, the change SHOULD be traceable.

A compatible specification MUST remain subordinate to KS-0001 within the Layer 1 knowledge-model scope.

A future specification MAY define exact schemas, templates, fields, identifier formats, relationship formats, lifecycle states, privacy classifications, validation rules, source-reference formats, or object types.

Such specifications are compatible only if they preserve the core requirements of KS-0001.

A future storage standard is compatible with KS-0001 only if storage preserves knowledge meaning without owning or redefining it.

A future agent standard is compatible with KS-0001 only if agents can read, classify, propose, summarize, validate, or transform knowledge without silently redefining identity, meaning, provenance, authority, privacy, lifecycle state, relationships, or validation.

A future workflow standard is compatible with KS-0001 only if workflows coordinate knowledge operations without redefining the knowledge model.

A future implementation document is compatible with KS-0001 only if it realizes the standard in practice without replacing the standard with implementation-specific assumptions.

Compatibility SHOULD be evaluated when:

- a Knowledge Object is created;
- a Knowledge Record is created;
- required metadata changes;
- object identity changes;
- source references change;
- provenance changes;
- relationships change;
- lifecycle state changes;
- authority level changes;
- privacy classification changes;
- validation expectations change;
- a record is imported;
- a record is exported;
- a record is migrated;
- an agent modifies or proposes changes;
- a workflow transforms knowledge;
- a storage system changes;
- an implementation changes;
- a specification is introduced or revised.

Compatibility does not require perfect preservation of every optional convenience feature.

Compatibility does require preservation of meaning-critical structure, metadata, provenance, relationships, lifecycle state, privacy expectations, authority expectations, validation expectations, and reviewability.

If a system cannot preserve a knowledge element during import, export, migration, transformation, or implementation replacement, the limitation SHOULD be explicit.

Lossy conversion MAY be acceptable for limited purposes, but lossy conversion MUST NOT be presented as full compatibility when meaning, provenance, identity, privacy, authority, lifecycle state, validation, or relationships are lost.

A compatibility failure SHOULD be treated as a reviewable issue.

A compatibility failure MAY require correction, migration guidance, validation warnings, governance review, implementation changes, or future specification work.

Compatibility Requirements are successful when Knowledge Objects and Knowledge Records can move across tools, storage systems, workflows, agents, validators, specifications, and implementations without losing identity, meaning, provenance, source distinction, relationships, lifecycle state, authority expectations, privacy classification, validation expectations, or human reviewability.

## 14. Privacy Requirements

Privacy Requirements define how Knowledge Objects and Knowledge Records preserve visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, and agent access expectations.

Privacy exists to prevent knowledge from being exposed, processed, copied, summarized, indexed, exported, synchronized, published, or acted on in ways that violate the intended handling boundaries of the object or record.

A Knowledge Object or Knowledge Record SHALL include or support Privacy Classification when privacy affects access, visibility, exposure, routing, synchronization, indexing, export, backup, publication, agent access, workflow behavior, validation, or downstream use.

Privacy Classification SHOULD be explicit enough that humans, agents, workflows, validators, storage systems, and implementations can determine how the knowledge should be handled.

Privacy Classification MUST NOT depend only on folder location, filename, tag, color, user interface state, plugin field, search ranking, workflow memory, agent memory, or hidden application state when privacy affects handling.

Those signals may support usability or implementation behavior, but they MUST NOT replace explicit privacy metadata when privacy matters.

KS-0001 defines privacy at the conceptual level.

KS-0001 does not define the complete privacy classification system for all Knowledge Objects and Knowledge Records.

A future privacy specification MAY define exact privacy classes, access rules, inheritance behavior, redaction rules, export rules, synchronization rules, indexing rules, agent access rules, validation rules, and migration behavior.

Until such a specification exists, privacy-sensitive knowledge SHOULD be handled conservatively.

Privacy Classification MAY describe whether knowledge is:

- public;
- internal;
- private;
- restricted;
- confidential;
- sensitive;
- personal;
- externally shareable;
- not externally shareable;
- agent-readable;
- agent-restricted;
- exportable;
- non-exportable;
- governed by a future privacy classification.

This list is descriptive, not a complete approved privacy vocabulary.

KS-0001 does not approve every listed value as a required privacy classification.

A future specification SHOULD define which privacy values are valid for Knowledge Objects and Knowledge Records.

Privacy Classification SHOULD remain distinguishable from Lifecycle State.

Lifecycle State describes governed status, such as draft, approved, deprecated, superseded, rejected, or archived.

Privacy Classification describes permitted handling, visibility, access, exposure, routing, synchronization, indexing, export, backup, publication, and agent access expectations.

For example, a Knowledge Record may be approved but restricted.

Privacy Classification SHOULD remain distinguishable from Authority Level.

Authority Level describes governance weight or interpretive authority.

Privacy Classification describes handling boundaries.

For example, a high-authority record may still be private, and a low-authority record may still be public.

Privacy Classification SHOULD remain distinguishable from Validation State.

Validation State describes whether a record satisfies structural, metadata, provenance, relationship, privacy, compatibility, or implementation expectations.

Privacy Classification describes how the record may be handled.

For example, a record may be structurally valid but not approved for export.

Privacy Requirements SHOULD apply to:

- Knowledge Objects;
- Knowledge Records;
- Source Material;
- Source References;
- metadata;
- relationships;
- provenance;
- lifecycle state;
- authority metadata;
- validation metadata;
- summaries;
- extracts;
- transformations;
- indexes;
- embeddings;
- caches;
- exports;
- backups;
- migrations;
- agent-generated outputs;
- workflow-generated outputs.

A Knowledge Record MUST NOT expose restricted Source Material merely because the record itself is easier to access, summarize, index, export, or publish.

A Source Reference MUST NOT expose restricted Source Material merely to improve traceability.

A relationship MUST NOT expose restricted knowledge merely because it connects to a public or less restricted object.

A summary, extraction, transformation, or agent-generated output MUST preserve applicable privacy boundaries from the source knowledge where practical.

If privacy classification is unknown, ambiguous, missing, or conflicting, a compliant system SHOULD treat the knowledge conservatively until reviewed or corrected.

Agents and workflows SHOULD NOT assume that missing privacy metadata means public access is permitted.

A future privacy specification MAY define default privacy behavior, inheritance rules, conflict-resolution rules, and review requirements.

Privacy Classification SHOULD be checked when:

- a Knowledge Object is created;
- a Knowledge Record is created;
- Source Material is linked;
- Source References are added;
- provenance is recorded;
- relationships are created;
- lifecycle state changes;
- authority level changes;
- validation state changes;
- an agent reads or modifies knowledge;
- a workflow routes or transforms knowledge;
- a record is summarized;
- a record is indexed;
- a record is embedded;
- a record is exported;
- a record is imported;
- a record is migrated;
- a record is published;
- a record is synchronized;
- a record is backed up;
- an implementation changes access behavior.

Privacy-sensitive changes SHOULD be traceable when they affect access, visibility, exposure, export, publication, synchronization, indexing, backup, agent access, workflow behavior, validation, or downstream use.

Agent-created or agent-modified privacy classifications SHOULD remain reviewable when they affect handling, access, publication, export, synchronization, indexing, or downstream use.

Workflow-driven privacy changes SHOULD preserve enough traceability to show:

- what privacy classification changed;
- what object, record, source, relationship, or output changed;
- what triggered the change;
- who or what performed the change;
- whether human review occurred;
- whether lifecycle state, authority, provenance, validation, or compatibility was affected.

Privacy Requirements SHOULD support portability.

Privacy meaning SHOULD remain understandable across migration, export, import, backup, restoration, synchronization, implementation replacement, workflow replacement, and agent replacement.

Implementation-specific access controls MAY support enforcement, but they SHOULD NOT be the only representation of privacy meaning when privacy affects knowledge handling.

A compatible implementation SHOULD preserve privacy metadata during migration, export, import, backup, restoration, and synchronization.

If privacy metadata cannot be preserved, the limitation SHOULD be explicit and treated as a reviewable compatibility issue.

Privacy Requirements are successful when future humans, agents, workflows, validators, storage systems, and implementations can determine:

- what privacy classification applies;
- what visibility or access expectations apply;
- whether the object, record, source, relationship, metadata, summary, extract, index, embedding, export, or backup is restricted;
- whether privacy affects agent access, workflow behavior, publication, export, synchronization, indexing, or downstream use;
- whether privacy classification has been reviewed where applicable;
- whether privacy boundaries survive migration and implementation replacement.

## 15. Validation Expectations

Validation Expectations define how Knowledge Objects and Knowledge Records should be checked for conformance with KS-0001 and related governed standards or specifications.

Validation exists to help humans, agents, workflows, validators, storage systems, and implementations detect missing structure, missing metadata, unclear provenance, broken relationships, privacy risks, lifecycle ambiguity, compatibility issues, and loss of meaning.

KS-0001 defines validation at the conceptual level.

KS-0001 does not define exact validation tools, schema syntax, field names, test suites, error codes, severity levels, validator behavior, or implementation-specific enforcement mechanisms.

A future validation specification MAY define exact validation rules, validation states, validator requirements, error behavior, warning behavior, reporting formats, compatibility tests, migration tests, and certification expectations.

Until such a specification exists, validation under KS-0001 SHOULD focus on whether Knowledge Objects and Knowledge Records preserve the meaning and minimum expectations defined by this standard.

A Knowledge Object or Knowledge Record SHOULD be validatable for:

- Object Identity;
- Knowledge Record structure;
- Required Metadata;
- Source Material distinction;
- Source References where applicable;
- provenance;
- relationships where applicable;
- Lifecycle State;
- Authority Level where applicable;
- Privacy Classification;
- validation state or validation expectations where applicable;
- human and AI readability;
- compatibility with KS-0001;
- portability across implementations.

Validation SHOULD determine whether required knowledge-model elements are present, explicit, interpretable, traceable, and portable.

Validation SHOULD NOT depend only on hidden application state, folder location, filename, visual layout, plugin behavior, workflow memory, agent memory, proprietary indexes, or undocumented conventions.

Those mechanisms may support validation, but they MUST NOT be the only evidence that a Knowledge Object or Knowledge Record satisfies KS-0001 when meaning, identity, provenance, privacy, authority, lifecycle state, relationships, or compatibility are affected.

Validation MAY be performed by:

- humans;
- agents;
- workflows;
- validators;
- storage systems;
- implementations;
- import processes;
- export processes;
- migration processes;
- review processes;
- governance processes.

Human validation MAY be sufficient for early drafts, small systems, or manual review.

Automated validation MAY assist with scale, consistency, migration, import, export, compatibility checking, and agent-assisted maintenance.

Agent-assisted validation SHOULD remain reviewable when validation affects meaning, authority, privacy, lifecycle state, publication, export, migration, or downstream use.

Validation SHOULD distinguish between:

- structural validity;
- metadata validity;
- provenance validity;
- relationship validity;
- source-reference validity;
- privacy validity;
- lifecycle validity;
- authority validity;
- compatibility validity;
- readability validity;
- implementation-specific validity.

A Knowledge Record may be valid in one sense and invalid in another.

For example, a Knowledge Record may have valid structure but missing Source References.

A Knowledge Record may have complete metadata but an unresolved privacy classification.

A Knowledge Record may be approved but fail compatibility validation during migration.

Validation results SHOULD be explicit where validation affects interpretation, review, workflow behavior, publication, export, migration, compatibility, privacy, authority, or downstream use.

Validation State MAY indicate whether a Knowledge Object or Knowledge Record is:

- unchecked;
- valid;
- invalid;
- partially valid;
- needs review;
- needs source review;
- needs privacy review;
- needs relationship review;
- needs provenance review;
- needs migration review;
- governed by a future validation state.

This list is descriptive, not a complete approved validation vocabulary.

KS-0001 does not approve every listed value as a required validation state.

A future validation specification SHOULD define which validation values are valid for Knowledge Objects and Knowledge Records.

Validation State SHOULD remain distinguishable from Lifecycle State.

Lifecycle State describes governed status, such as draft, approved, deprecated, superseded, rejected, or archived.

Validation State describes whether the object or record satisfies structural, metadata, provenance, relationship, privacy, compatibility, or implementation expectations.

Validation State SHOULD remain distinguishable from Authority Level.

Authority Level describes governance weight or interpretive authority.

Validation State describes conformance with expected structure, metadata, provenance, privacy, relationships, compatibility, or implementation requirements.

Validation State SHOULD remain distinguishable from Privacy Classification.

Privacy Classification describes handling boundaries.

Validation State may indicate whether those handling boundaries are present, clear, conflicting, missing, or enforceable.

Validation SHOULD check that a Knowledge Object or Knowledge Record does not silently depend on implementation-specific assumptions for critical meaning.

Validation SHOULD check that Source Material remains distinguishable from Knowledge Records.

Validation SHOULD check that Source References are present when source support is materially relevant.

Validation SHOULD check that provenance is sufficient for review where provenance affects meaning, authority, privacy, lifecycle state, validation, or downstream use.

Validation SHOULD check that relationships are explicit when relationships affect meaning, context, provenance, hierarchy, dependency, lifecycle state, authority, privacy, or validation.

Validation SHOULD check that Privacy Classification is present or supported when privacy affects handling.

Validation SHOULD check that Lifecycle State is present or supported when lifecycle status affects interpretation, authority, review, publication, supersession, deprecation, validation, or workflow behavior.

Validation SHOULD check that compatibility requirements are preserved during import, export, migration, transformation, storage replacement, workflow replacement, agent replacement, or implementation replacement.

Validation failures SHOULD be traceable when they affect meaning, identity, provenance, relationships, lifecycle state, authority, privacy, compatibility, migration, publication, export, or downstream use.

A validation failure MAY require:

- human review;
- correction;
- metadata completion;
- source-reference repair;
- provenance repair;
- relationship repair;
- privacy review;
- lifecycle review;
- compatibility review;
- migration guidance;
- governance review;
- future specification work.

A validation failure MUST NOT automatically destroy, delete, hide, supersede, deprecate, reject, or invalidate the historical value of a Knowledge Object or Knowledge Record.

Validation failure indicates that review, correction, qualification, or governance action may be needed.

A Knowledge Object or Knowledge Record MAY remain historically useful even if it fails current validation expectations.

Validation Expectations SHOULD support portability.

Validation meaning SHOULD remain understandable across migration, export, import, backup, restoration, implementation replacement, workflow replacement, and agent replacement.

Implementation-specific validation tools MAY support enforcement, but they SHOULD NOT be the only representation of validation meaning when validation affects knowledge interpretation or use.

Validation Expectations are successful when future humans, agents, workflows, validators, storage systems, and implementations can determine:

- whether a Knowledge Object or Knowledge Record satisfies KS-0001;
- what validation state applies;
- what validation issues exist where applicable;
- whether required metadata is present;
- whether provenance and Source References are sufficient where applicable;
- whether relationships are explicit where needed;
- whether privacy, lifecycle, authority, and compatibility expectations are preserved;
- whether validation results remain reviewable;
- whether validation meaning survives migration and implementation replacement.

## 16. Anti-Patterns

Anti-patterns are practices that appear convenient but weaken the knowledge model defined by KS-0001.

Anti-patterns SHOULD be avoided because they make Knowledge Objects and Knowledge Records harder to preserve, review, validate, migrate, govern, or interpret across tools, agents, workflows, and implementations.

A system, workflow, agent, specification, or implementation MAY still be recoverable if an anti-pattern exists, but the anti-pattern SHOULD be treated as a reviewable design or maintenance issue.

### 16.1 Treating Files as Knowledge Objects by Default

A file MUST NOT be treated as a Knowledge Object merely because it exists in a vault, folder, repository, database, or application.

Files may store, display, support, or represent Knowledge Objects.

However, a Knowledge Object requires governed identity, metadata, meaning, provenance, relationships, lifecycle state, privacy classification, and reviewability where applicable.

A file without governed knowledge structure is not automatically a valid Knowledge Object.

### 16.2 Treating Source Material as a Knowledge Record

Source Material MUST NOT be treated as a Knowledge Record merely because it is imported, linked, stored, indexed, summarized, or placed near other records.

Source Material may support a Knowledge Record.

A Knowledge Record may be created from, about, or in response to Source Material.

The distinction between evidence, input, context, interpretation, and governed knowledge SHOULD remain explicit.

### 16.3 Using Folder Location as Meaning

Folder location MUST NOT be the only source of critical meaning.

Folder location may support navigation, organization, access control, storage behavior, or implementation convenience.

However, folder location SHOULD NOT be the only representation of object identity, lifecycle state, privacy classification, authority level, validation state, relationship meaning, provenance, or source distinction.

### 16.4 Using Filenames as Stable Identity

A filename MUST NOT be the only stable identity of a Knowledge Object.

Filenames may support human recognition, sorting, search, display, migration, or storage.

However, renaming a file SHOULD NOT silently change the identity or meaning of a Knowledge Object.

Stable Object Identity SHOULD remain explicit and portable.

### 16.5 Hiding Meaning in Application State

Critical meaning MUST NOT exist only in hidden application state.

Examples of hidden application state may include:

- database-only fields without export;
- plugin-specific fields without durable representation;
- user interface status indicators;
- color coding;
- collapsed views;
- search ranking;
- workflow memory;
- agent memory;
- hidden prompts;
- proprietary indexes;
- undocumented implementation behavior.

These mechanisms may support usability or automation, but they SHOULD NOT be the only place where governed meaning exists.

### 16.6 Relying on Tags as Governance

Tags SHOULD NOT be the only representation of governed meaning.

Tags may support discovery, filtering, grouping, or automation.

However, tags SHOULD NOT be the only representation of object type, lifecycle state, privacy classification, authority level, validation state, source distinction, relationship type, or provenance when those meanings affect interpretation or downstream use.

### 16.7 Collapsing Provenance into Content

Provenance SHOULD NOT be hidden inside ordinary content when provenance affects meaning, authority, privacy, lifecycle state, validation, or review.

A Knowledge Record SHOULD distinguish between:

- what the record says;
- where the knowledge came from;
- what Source Material supports it;
- who or what created it;
- what transformation occurred;
- whether review occurred.

Content and provenance may appear near each other, but they SHOULD remain distinguishable.

### 16.8 Treating Agent Output as Approved Knowledge

Agent output MUST NOT be treated as approved knowledge merely because an agent generated it.

Agent-created summaries, classifications, relationships, metadata, transformations, or recommendations SHOULD remain reviewable when they affect meaning, authority, privacy, lifecycle state, validation, publication, export, or downstream use.

Agent assistance may improve knowledge operations, but it MUST NOT silently replace governance.

### 16.9 Treating Workflow Completion as Approval

A workflow finishing successfully MUST NOT automatically mean that the resulting Knowledge Object or Knowledge Record is approved.

Workflow completion may indicate that a process ran.

Approval indicates governed review status.

Where approval affects authority, publication, downstream use, or governance, approval SHOULD remain explicit and traceable.

### 16.10 Mixing Privacy with Visibility Alone

Privacy MUST NOT be reduced to whether something is currently visible in a user interface.

A hidden record is not automatically private.

A visible record is not automatically public.

Privacy Classification SHOULD describe permitted handling, access, exposure, routing, export, publication, synchronization, indexing, backup, and agent access expectations.

### 16.11 Losing Source Distinction During Summarization

A summary MUST NOT erase the distinction between Source Material, extraction, interpretation, synthesis, and governed knowledge.

Summaries SHOULD preserve enough provenance and source reference information for future review where the source materially supports the record.

A summary SHOULD NOT imply source support that does not exist or can no longer be verified.

### 16.12 Treating Links as Relationships Without Meaning

A link SHOULD NOT be treated as a complete governed relationship unless the relationship meaning is clear enough for interpretation and review.

Links may support navigation.

Governed relationships SHOULD preserve what is connected, why it is connected, what type of relationship exists, whether direction matters, and whether the relationship affects meaning, authority, privacy, lifecycle state, validation, or governance.

### 16.13 Ignoring Supersession and Deprecation

A Knowledge Object or Knowledge Record SHOULD NOT be deleted, hidden, overwritten, or replaced without preserving supersession, deprecation, or historical context where that context affects meaning, authority, provenance, relationships, validation, or review.

Older knowledge may remain historically useful even when it is no longer current authority.

Supersession and deprecation SHOULD be traceable where practical.

### 16.14 Treating Compatibility as File Conversion Only

Compatibility MUST NOT be reduced to whether a file can be opened or converted.

A converted record is compatible only when identity, meaning, metadata, provenance, source distinction, relationships, lifecycle state, authority expectations, privacy classification, validation expectations, and reviewability are preserved where applicable.

Lossy conversion SHOULD be explicit.

### 16.15 Overloading Optional Metadata

Optional Metadata SHOULD NOT become excessive, inconsistent, or required by hidden convention.

Optional Metadata is useful when it improves interpretation, navigation, discovery, automation, validation, review, interoperability, migration, or maintenance.

Optional Metadata becomes harmful when it creates unnecessary cognitive burden, implementation lock-in, hidden requirements, or confusion with Required Metadata.

### 16.16 Anti-Patterns Success

Anti-pattern identification is successful when future humans, agents, workflows, validators, storage systems, and implementations can detect practices that weaken identity, meaning, provenance, source distinction, relationships, lifecycle state, authority, privacy, validation, compatibility, readability, or governance before those practices become embedded in the system.

## 17. Review Checklist

The Review Checklist provides a practical way to evaluate whether a Knowledge Object, Knowledge Record, specification, workflow, agent behavior, storage behavior, validator, or implementation remains aligned with KS-0001.

The checklist is not a complete validation specification.

The checklist exists to support human review, agent-assisted review, workflow review, governance review, migration review, and implementation review until future validation specifications define exact rules.

A reviewer SHOULD use this checklist when:

- creating a Knowledge Object;
- creating a Knowledge Record;
- reviewing a Knowledge Record;
- importing knowledge;
- exporting knowledge;
- migrating knowledge;
- summarizing Source Material;
- creating relationships;
- changing lifecycle state;
- changing privacy classification;
- changing authority level;
- validating records;
- designing storage behavior;
- designing agent behavior;
- designing workflow behavior;
- designing implementation behavior;
- drafting future specifications.

### 17.1 Knowledge Object Review

A Knowledge Object SHOULD satisfy the following review questions:

- Does the object represent a discrete unit of structured knowledge?
- Is the object distinguishable from files, folders, tags, database rows, source artifacts, workflows, agents, and implementations?
- Does the object have or support stable Object Identity?
- Does the object preserve meaning independent of filename, folder path, storage location, application state, workflow state, or agent output?
- Is the object interpretable through explicit metadata, relationships, provenance, lifecycle state, authority expectations, privacy classification, and governed structure?
- Can a future human, agent, workflow, validator, storage system, or implementation understand what the object means?
- Can the object remain recognizable across migration, export, import, backup, restoration, and implementation replacement?

### 17.2 Knowledge Record Review

A Knowledge Record SHOULD satisfy the following review questions:

- Does the record represent a Knowledge Object in an inspectable form?
- Is the record distinguishable from Source Material?
- Does the record include or reference the identity of the Knowledge Object it represents?
- Does the record include enough structure to remain understandable outside one implementation?
- Does the record include Required Metadata?
- Does the record include content or a structured knowledge body where applicable?
- Does the record preserve Source References where Source Material materially supports the record?
- Does the record preserve provenance where provenance affects meaning, authority, privacy, lifecycle state, validation, or review?
- Does the record preserve relationships where relationships affect meaning, context, provenance, hierarchy, dependency, lifecycle state, authority, privacy, or validation?
- Does the record remain reviewable when created or modified by an agent or workflow?
- Does the record avoid silently changing the meaning, identity, provenance, authority, privacy classification, or lifecycle state of the Knowledge Object?

### 17.3 Metadata Review

Required Metadata SHOULD satisfy the following review questions:

- Is Object Identity present or supported?
- Is a title or human-readable label present?
- Is object type present where applicable?
- Is Lifecycle State present or supported where lifecycle status affects interpretation or use?
- Is Privacy Classification present or supported where privacy affects handling?
- Is provenance present or supported?
- Are Source References present where Source Material materially supports the record?
- Are relationships present where relationships affect meaning or future use?
- Is Authority Level present or supported where authority affects interpretation, governance, review, trust, publication, validation, or downstream use?
- Is creation or revision context present where it affects provenance, reviewability, lifecycle state, authority, validation, or compatibility?
- Is validation state or validation expectation present where validation affects compliance, review, workflow behavior, import, export, migration, publication, or interoperability?
- Is Required Metadata explicit enough to avoid relying on hidden application state, user memory, workflow memory, or agent memory?

### 17.4 Source Material and Source Reference Review

Source Material and Source References SHOULD satisfy the following review questions:

- Is Source Material distinguishable from Knowledge Records?
- Is the role of Source Material clear?
- Does the Knowledge Record avoid treating Source Material as governed knowledge by default?
- Are Source References present where source support is materially relevant?
- Are Source References traceable enough for future review?
- Does provenance explain whether content was copied, summarized, extracted, interpreted, transformed, synthesized, or generated?
- Does the record avoid implying source support when no source is available or verifiable?
- Does the record preserve privacy boundaries around Source Material and Source References?
- Can Source References survive migration, export, import, backup, restoration, and implementation replacement where practical?

### 17.5 Relationship Review

Relationships SHOULD satisfy the following review questions:

- Are meaningful relationships explicit?
- Is it clear what entities are connected?
- Is the relationship type clear where type affects meaning?
- Is relationship direction clear where direction affects meaning?
- Is relationship context clear where context affects interpretation?
- Is it clear whether the relationship is inferred, proposed, reviewed, validated, or approved where applicable?
- Does the relationship avoid relying only on folder proximity, filename similarity, tag coincidence, search ranking, visual placement, application state, or agent inference?
- Does the relationship preserve privacy boundaries?
- Does the relationship remain portable across migration, export, import, backup, restoration, and implementation replacement?

### 17.6 Provenance Review

Provenance SHOULD satisfy the following review questions:

- Is the origin of the knowledge clear?
- Is it clear who or what created the record where applicable?
- Is it clear who or what modified the record where applicable?
- Is it clear what Source Material supports the record where applicable?
- Is it clear what transformation occurred?
- Is it clear whether human review occurred?
- Is it clear whether the record contains evidence, extraction, summary, interpretation, synthesis, decision, or agent-generated content?
- Is provenance sufficient for review without unnecessarily exposing restricted knowledge?
- Does provenance remain portable across migration and implementation replacement?

### 17.7 Lifecycle Review

Lifecycle State SHOULD satisfy the following review questions:

- Is the lifecycle state explicit where lifecycle status affects interpretation or use?
- Is the object or record draft, under review, approved, rejected, deprecated, superseded, archived, or governed by another lifecycle state?
- Is Lifecycle State distinguishable from Authority Level, Validation State, and Privacy Classification?
- Are lifecycle transitions traceable where they affect meaning, authority, privacy, validation, relationships, provenance, compatibility, workflow behavior, publication, or downstream use?
- Is approval explicit where approval affects authority, publication, downstream use, or governance?
- Does the record preserve historical context where supersession, deprecation, rejection, archival, or replacement affects future interpretation?
- Does lifecycle meaning survive migration and implementation replacement?

### 17.8 Privacy Review

Privacy Classification SHOULD satisfy the following review questions:

- Is Privacy Classification explicit where privacy affects handling?
- Is privacy distinguishable from Lifecycle State, Authority Level, and Validation State?
- Does the record avoid assuming missing privacy metadata means public access is permitted?
- Does the record preserve privacy boundaries across Source Material, Source References, metadata, relationships, provenance, summaries, extracts, transformations, indexes, embeddings, exports, backups, migrations, agent outputs, and workflow outputs?
- Are privacy-sensitive changes traceable where they affect access, visibility, exposure, export, publication, synchronization, indexing, backup, agent access, workflow behavior, validation, or downstream use?
- Does privacy meaning survive migration, export, import, backup, restoration, synchronization, and implementation replacement?

### 17.9 Compatibility Review

Compatibility SHOULD satisfy the following review questions:

- Does the object or record preserve identity across tools, storage systems, workflows, agents, validators, specifications, and implementations?
- Does the object or record preserve meaning across migration, export, import, backup, restoration, and implementation replacement?
- Does the object or record preserve Required Metadata?
- Does the object or record preserve Source Material distinction?
- Does the object or record preserve Source References where applicable?
- Does the object or record preserve provenance?
- Does the object or record preserve meaningful relationships?
- Does the object or record preserve Lifecycle State?
- Does the object or record preserve Authority Level where applicable?
- Does the object or record preserve Privacy Classification?
- Does the object or record preserve validation state or validation expectations where applicable?
- Does the object or record preserve human and AI readability?
- Are lossy conversions explicitly identified?
- Are compatibility failures treated as reviewable issues?

### 17.10 Validation Review

Validation SHOULD satisfy the following review questions:

- Can the Knowledge Object or Knowledge Record be checked against KS-0001?
- Are required knowledge-model elements present?
- Are required knowledge-model elements explicit?
- Are required knowledge-model elements interpretable?
- Are required knowledge-model elements traceable?
- Are required knowledge-model elements portable?
- Is validation state explicit where validation affects interpretation, review, workflow behavior, publication, export, migration, compatibility, privacy, authority, or downstream use?
- Are validation failures traceable?
- Are validation failures treated as reviewable issues rather than automatic destruction, deletion, hiding, supersession, deprecation, rejection, or historical invalidation?
- Does validation meaning survive migration and implementation replacement?

### 17.11 Anti-Pattern Review

A reviewer SHOULD check whether the object, record, system, workflow, agent, specification, validator, or implementation relies on any of the following anti-patterns:

- treating files as Knowledge Objects by default;
- treating Source Material as Knowledge Records by default;
- using folder location as meaning;
- using filenames as stable identity;
- hiding meaning in application state;
- relying on tags as governance;
- collapsing provenance into content;
- treating agent output as approved knowledge;
- treating workflow completion as approval;
- mixing privacy with visibility alone;
- losing source distinction during summarization;
- treating links as relationships without meaning;
- ignoring supersession and deprecation;
- treating compatibility as file conversion only;
- overloading Optional Metadata.

### 17.12 Review Checklist Success

The Review Checklist is successful when it helps future humans, agents, workflows, validators, storage systems, and implementations identify whether a Knowledge Object, Knowledge Record, specification, workflow, agent behavior, storage behavior, validator, or implementation preserves identity, meaning, provenance, source distinction, relationships, lifecycle state, authority, privacy, validation, compatibility, readability, and governance under KS-0001.

## 18. Success Criteria

Success Criteria define the conditions under which KS-0001 can be considered successful as the foundational Knowledge Object Model for The Brain Standard.

KS-0001 is successful when it provides a stable, implementation-independent model for Knowledge Objects and Knowledge Records that future standards, specifications, workflows, agents, validators, storage systems, and implementations can rely on.

KS-0001 succeeds when Knowledge Objects remain understandable as discrete units of structured knowledge rather than being confused with files, folders, tags, database rows, source artifacts, workflows, agents, or implementations.

KS-0001 succeeds when Knowledge Records remain inspectable representations of Knowledge Objects and preserve identity, meaning, metadata, provenance, relationships, lifecycle state, authority expectations, privacy classification, validation expectations, and reviewability.

KS-0001 succeeds when Source Material remains distinguishable from Knowledge Records.

A compliant system SHOULD allow future humans, agents, workflows, validators, storage systems, and implementations to determine:

- what original material exists;
- what structured knowledge was created from or about it;
- what Source Material supports a record where applicable;
- what transformation occurred;
- what remains evidence;
- what remains interpretation;
- what remains governed knowledge.

KS-0001 succeeds when Object Identity remains stable across:

- renaming;
- moving;
- copying;
- migration;
- import;
- export;
- indexing;
- summarization;
- transformation;
- translation;
- backup;
- restoration;
- synchronization;
- implementation replacement.

KS-0001 succeeds when Required Metadata is explicit enough to make Knowledge Objects and Knowledge Records identifiable, interpretable, traceable, reviewable, privacy-respecting, portable, and validatable.

KS-0001 succeeds when Optional Metadata improves interpretation, navigation, discovery, automation, validation, review, interoperability, migration, or maintenance without creating hidden requirements, implementation lock-in, unnecessary cognitive burden, or confusion with Required Metadata.

KS-0001 succeeds when meaningful relationships remain explicit, inspectable, portable, and reviewable.

A compliant system SHOULD allow future humans, agents, workflows, validators, storage systems, and implementations to determine:

- what entities are connected;
- what kind of connection exists;
- why the connection matters;
- whether the connection is source-supported;
- whether the connection is inferred or reviewed;
- whether the connection affects meaning, authority, privacy, lifecycle state, validation, or governance;
- whether the connection remains valid across migration, export, import, and implementation replacement.

KS-0001 succeeds when provenance and Source References allow future review of where knowledge came from, what evidence supports it where applicable, what transformation occurred, who or what created or modified it where applicable, whether review occurred, and whether privacy boundaries were preserved.

KS-0001 succeeds when Lifecycle State makes current use, review status, approval status, historical status, supersession, deprecation, rejection, archival, and downstream use distinguishable where applicable.

KS-0001 succeeds when human and AI readability allow Knowledge Objects and Knowledge Records to remain useful to humans and interpretable by AI systems without depending on hidden application state, hidden prompts, proprietary indexes, workflow memory, agent memory, or undocumented implementation behavior.

KS-0001 succeeds when compatibility requirements allow Knowledge Objects and Knowledge Records to move across tools, storage systems, workflows, agents, validators, specifications, and implementations without losing identity, meaning, provenance, source distinction, relationships, lifecycle state, authority expectations, privacy classification, validation expectations, or human reviewability.

KS-0001 succeeds when Privacy Classification preserves handling boundaries across Source Material, Source References, metadata, relationships, provenance, summaries, extracts, transformations, indexes, embeddings, exports, backups, migrations, agent outputs, workflow outputs, and implementation behavior.

KS-0001 succeeds when validation expectations allow humans, agents, workflows, validators, storage systems, and implementations to identify missing structure, missing metadata, unclear provenance, broken relationships, privacy risks, lifecycle ambiguity, compatibility issues, and loss of meaning.

KS-0001 succeeds when anti-patterns can be detected before they become embedded in systems, workflows, agents, specifications, validators, or implementations.

KS-0001 succeeds when future Layer 1 specifications can define exact schemas, templates, metadata fields, identifier formats, relationship formats, lifecycle states, privacy classifications, validation rules, source-reference formats, object types, and import/export formats without contradicting the core Knowledge Object Model.

KS-0001 succeeds when future Layer 2 storage standards can preserve Knowledge Object identity and meaning without allowing storage layout, filenames, file paths, database rows, or application-specific identifiers to define knowledge meaning.

KS-0001 succeeds when future Layer 3 agent standards can define agent behavior without allowing agents to silently redefine identity, meaning, provenance, authority, privacy, lifecycle state, relationships, validation, or approval.

KS-0001 succeeds when future Layer 4 workflow standards can coordinate knowledge operations without allowing workflow completion, routing, automation state, or workflow memory to replace governed knowledge meaning.

KS-0001 succeeds when future Layer 5 implementation documents can realize the standard in practical tools without replacing the standard with implementation-specific assumptions.

KS-0001 succeeds when The Brain Standard remains practical for daily use.

The Knowledge Object Model SHOULD support durable structure without requiring unnecessary metadata burden, excessive manual work, or tool-specific complexity.

KS-0001 is successful when future humans, agents, workflows, validators, storage systems, and implementations can preserve, review, validate, migrate, relate, protect, and interpret knowledge over time without losing the meaning, identity, provenance, source distinction, privacy boundaries, governance expectations, or implementation independence required by The Brain Standard.

## 19. Non-Goals

Non-Goals define what KS-0001 intentionally does not attempt to define.

Non-Goals exist to preserve architectural boundaries, prevent scope creep, and ensure that the Knowledge Object Model remains focused on knowledge meaning rather than storage, tooling, workflow execution, agent behavior, or implementation detail.

KS-0001 is a Layer 1 Universal Knowledge Standard document.

KS-0001 defines the foundational model for Knowledge Objects and Knowledge Records.

KS-0001 does not define every system, process, file layout, schema, workflow, agent behavior, implementation behavior, or operational practice required to build The Brain.

The following concerns are intentionally outside the scope of KS-0001.

### 19.1 Storage Layouts

KS-0001 does not define folder structures, vault layouts, repository layouts, database schemas, table designs, graph database structures, file naming systems, storage paths, backup layouts, synchronization layouts, or archive layouts.

Storage standards and implementation documents MAY define those concerns later.

Any future storage design MUST preserve the Knowledge Object identity, meaning, metadata, provenance, relationships, lifecycle state, privacy classification, validation expectations, and reviewability defined by KS-0001.

### 19.2 Exact Metadata Fields

KS-0001 does not define exact metadata field names, front matter syntax, schema syntax, allowed values, serialization formats, or storage placement.

KS-0001 defines required and optional metadata at the conceptual level.

A future metadata specification MAY define exact fields, field names, field formats, allowed values, templates, schemas, validation rules, and migration behavior.

### 19.3 Identifier Formats

KS-0001 does not define exact Object Identity formats.

KS-0001 requires stable Object Identity but does not mandate UUIDs, slugs, file-based identifiers, numeric identifiers, graph identifiers, database identifiers, URI formats, or any other specific identifier system.

A future identity specification MAY define identifier formats, uniqueness scopes, collision rules, alias behavior, redirect behavior, merge behavior, split behavior, and migration behavior.

### 19.4 Object Type Vocabulary

KS-0001 does not define a complete vocabulary of Knowledge Object types.

Examples such as concept, person, organization, source, project, decision, procedure, reference, event, claim, task, or note are illustrative unless approved by a future governed specification.

A future object-type specification MAY define approved object types, type hierarchy, type metadata, type-specific validation rules, and migration expectations.

### 19.5 Relationship Vocabulary

KS-0001 does not define a complete governed relationship vocabulary.

KS-0001 requires meaningful relationships to be explicit, inspectable, portable, and reviewable.

A future relationship specification MAY define relationship types, directionality, cardinality, allowed targets, graph structures, relationship records, validation rules, inferred relationship behavior, relationship confidence, and lifecycle behavior.

### 19.6 Source Reference Formats

KS-0001 does not define exact citation formats, source-reference syntax, archive rules, source identifiers, source availability states, link durability requirements, or evidence rules.

KS-0001 requires Source References to remain traceable, inspectable, and understandable where Source Material materially supports a Knowledge Record.

A future source-reference specification MAY define exact source-reference formats, citation behavior, archival behavior, source availability metadata, evidence expectations, validation rules, and migration behavior.

### 19.7 Lifecycle State System

KS-0001 does not define the complete lifecycle state system for all Knowledge Objects and Knowledge Records.

Lifecycle examples such as draft, under review, approved, rejected, deprecated, superseded, archived, experimental, proposed, imported, needs review, or needs validation are descriptive unless approved by a future governed specification.

A future lifecycle specification MAY define exact lifecycle states, allowed transitions, transition rules, approval requirements, archival behavior, validation behavior, workflow effects, and migration expectations.

### 19.8 Privacy Classification System

KS-0001 does not define the complete privacy classification system for all Knowledge Objects and Knowledge Records.

Privacy examples such as public, internal, private, restricted, confidential, sensitive, personal, externally shareable, not externally shareable, agent-readable, agent-restricted, exportable, or non-exportable are descriptive unless approved by a future governed specification.

A future privacy specification MAY define exact privacy classes, access rules, inheritance behavior, redaction behavior, export rules, synchronization rules, indexing rules, agent access rules, validation rules, and migration behavior.

### 19.9 Authority Model Details

KS-0001 does not define a complete authority model for all Knowledge Objects, Knowledge Records, Source Material, decisions, standards, specifications, workflows, agents, or implementations.

KS-0001 requires Authority Level to be supported where authority affects interpretation, governance, review, trust, publication, validation, or downstream use.

A future authority specification MAY define authority levels, authority inheritance, review status, approval behavior, conflict handling, source authority, knowledge authority, and validation expectations.

### 19.10 Validation Tooling

KS-0001 does not define exact validation tools, schema languages, validator implementations, error codes, warning levels, certification tests, compliance suites, or enforcement mechanisms.

KS-0001 defines validation expectations conceptually.

A future validation specification MAY define exact validation rules, validation states, validators, reporting formats, severity levels, compatibility tests, migration tests, certification behavior, and enforcement expectations.

### 19.11 Agent Permissions and Behavior

KS-0001 does not define agent permissions, agent roles, agent memory behavior, tool access rules, execution limits, prompt formats, model choices, review gates, or automation boundaries.

Agent standards and implementation documents MAY define those concerns later.

Any future agent behavior MUST preserve Knowledge Object identity, meaning, provenance, relationships, lifecycle state, authority expectations, privacy classification, validation expectations, and reviewability.

### 19.12 Workflow Execution

KS-0001 does not define workflow engines, workflow triggers, routing rules, automation steps, approval queues, execution states, task systems, scheduling behavior, or operational procedures.

Workflow standards and implementation documents MAY define those concerns later.

Any future workflow behavior MUST coordinate knowledge operations without redefining the Knowledge Object Model.

### 19.13 User Interface Behavior

KS-0001 does not define user interfaces, graph views, dashboards, editor layouts, forms, colors, icons, panes, search interfaces, templates, navigation systems, or display behavior.

Implementations MAY provide user interfaces that improve usability.

However, user interface behavior MUST NOT become the only source of critical knowledge meaning.

### 19.14 Daily Operating Procedures

KS-0001 does not define daily routines, capture habits, review schedules, maintenance procedures, inbox processing, note-taking methods, or personal operating practices.

Operational guides and SOP documents MAY define those practices later.

Daily use SHOULD remain compatible with KS-0001, but KS-0001 itself is not a daily operating manual.

### 19.15 Implementation Lock-In

KS-0001 does not endorse or require a specific application, vendor, platform, database, file system, plugin, workflow engine, AI model, agent framework, or storage backend.

Implementations may vary.

Compliance depends on preserving the Knowledge Object Model, not on using a particular tool.

### 19.16 Non-Goals Success

Non-Goals are successful when KS-0001 remains focused on defining knowledge meaning, identity, metadata, provenance, relationships, lifecycle state, privacy, authority, validation expectations, readability, compatibility, and reviewability without absorbing the responsibilities of storage standards, agent standards, workflow standards, implementation documents, specifications, operational guides, or user-interface designs.

## 20. Open Questions

Open Questions identify unresolved issues, future decisions, and areas that may require later standards, specifications, ADRs, RFCs, implementation documents, or operational guides.

Open Questions are not approved requirements.

Open Questions exist to preserve uncertainty explicitly without forcing premature design decisions into KS-0001.

An Open Question SHOULD remain visible until it is resolved, rejected, deferred, superseded, or converted into a governed document.

A future governance process MAY resolve Open Questions through:

- a later standard;
- a specification;
- an ADR;
- an RFC;
- an implementation document;
- a workflow document;
- an agent document;
- a validation document;
- an operational guide.

Resolved Open Questions SHOULD be traceable where the resolution affects identity, metadata, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, implementation behavior, or governance.

### 20.1 Object Identity Format

KS-0001 requires stable Object Identity but does not define the exact identifier format.

Future work SHOULD determine whether The Brain Standard should define:

- UUID-based identifiers;
- human-readable slugs;
- document-style identifiers;
- hierarchical identifiers;
- graph identifiers;
- URI-based identifiers;
- hybrid identifiers;
- implementation-specific identifiers mapped to stable governed identifiers.

This question SHOULD be resolved in a future identity specification.

### 20.2 Metadata Field Names and Schema

KS-0001 defines Required Metadata and Optional Metadata conceptually but does not define exact field names, schema syntax, serialization format, or storage placement.

Future work SHOULD determine:

- which metadata fields are required in practice;
- which metadata fields are optional but recommended;
- how fields should be named;
- whether front matter should be used;
- whether sidecar metadata should be allowed;
- whether database or graph representations require equivalent fields;
- how metadata should be validated;
- how metadata should migrate across implementations.

This question SHOULD be resolved in a future metadata or schema specification.

### 20.3 Object Type Vocabulary

KS-0001 does not approve a complete object-type vocabulary.

Future work SHOULD determine which Knowledge Object types are needed first.

Possible candidates MAY include:

- concept;
- source;
- person;
- organization;
- project;
- decision;
- procedure;
- reference;
- claim;
- event;
- task;
- note;
- standard;
- specification;
- workflow;
- agent;
- implementation.

This question SHOULD be resolved in a future object-type specification.

### 20.4 Relationship Vocabulary

KS-0001 requires meaningful relationships to be explicit but does not define a complete relationship vocabulary.

Future work SHOULD determine:

- approved relationship types;
- directionality rules;
- cardinality rules;
- relationship metadata;
- relationship provenance;
- relationship validation;
- inferred relationship behavior;
- relationship confidence;
- relationship lifecycle behavior;
- relationship privacy behavior.

This question SHOULD be resolved in a future relationship specification.

### 20.5 Source Reference Format

KS-0001 requires Source References where Source Material materially supports a Knowledge Record but does not define exact source-reference formats.

Future work SHOULD determine:

- source identifier formats;
- citation formats;
- source path behavior;
- archive behavior;
- source availability states;
- link durability expectations;
- page, timestamp, range, excerpt, or section-reference behavior;
- source validation rules;
- source migration behavior.

This question SHOULD be resolved in a future source-reference specification.

### 20.6 Provenance Model

KS-0001 requires provenance but does not define a complete provenance model.

Future work SHOULD determine:

- provenance fields;
- provenance event types;
- creator and modifier representation;
- agent provenance;
- workflow provenance;
- transformation provenance;
- migration provenance;
- review provenance;
- approval provenance;
- provenance privacy behavior;
- provenance validation rules.

This question SHOULD be resolved in a future provenance specification.

### 20.7 Lifecycle State System

KS-0001 defines Lifecycle State conceptually but does not define the complete lifecycle state system for Knowledge Objects and Knowledge Records.

Future work SHOULD determine:

- approved lifecycle states;
- allowed transitions;
- transition rules;
- review requirements;
- approval requirements;
- rejection behavior;
- deprecation behavior;
- supersession behavior;
- archival behavior;
- workflow effects;
- validation effects;
- migration effects.

This question SHOULD be resolved in a future lifecycle specification.

### 20.8 Privacy Classification System

KS-0001 requires Privacy Classification where privacy affects handling but does not define the complete privacy classification system.

Future work SHOULD determine:

- approved privacy classes;
- default privacy behavior;
- inheritance rules;
- source privacy behavior;
- relationship privacy behavior;
- summary and extraction privacy behavior;
- index and embedding privacy behavior;
- export rules;
- synchronization rules;
- backup rules;
- agent access rules;
- redaction behavior;
- privacy validation rules.

This question SHOULD be resolved in a future privacy specification.

### 20.9 Authority Model

KS-0001 requires Authority Level where authority affects interpretation, governance, review, trust, publication, validation, or downstream use.

Future work SHOULD determine:

- authority levels for Knowledge Objects;
- authority levels for Knowledge Records;
- authority levels for Source Material;
- authority levels for standards and specifications;
- authority inheritance behavior;
- source authority behavior;
- review and approval relationships;
- conflict-resolution behavior;
- authority validation rules.

This question SHOULD be resolved in a future authority specification.

### 20.10 Validation Rules

KS-0001 defines validation expectations conceptually but does not define exact validation rules or tooling.

Future work SHOULD determine:

- required validation rules;
- recommended validation rules;
- validation states;
- error levels;
- warning levels;
- validation reporting formats;
- validator behavior;
- human review behavior;
- agent-assisted validation behavior;
- migration validation behavior;
- compatibility validation behavior;
- certification expectations.

This question SHOULD be resolved in a future validation specification.

### 20.11 Markdown Representation

KS-0001 allows Markdown-compatible representations but does not define an exact Markdown template.

Future work SHOULD determine:

- whether Knowledge Records should use Markdown front matter;
- what heading structure should be required;
- how content sections should be named;
- how Source References should appear;
- how relationships should appear;
- how provenance should appear;
- how lifecycle, authority, privacy, and validation fields should appear;
- how Markdown records should remain compatible with non-Markdown implementations.

This question SHOULD be resolved in a future Markdown representation specification or implementation profile.

### 20.12 Storage Separation

KS-0001 distinguishes Source Material from Knowledge Records but does not define whether they must be stored together or separately.

Future work SHOULD determine:

- whether Source Material and Knowledge Records should live in separate repositories;
- whether Source Material and Knowledge Records should live in separate folders;
- whether source files should be copied, linked, archived, or referenced;
- how storage systems should preserve source distinction;
- how storage systems should preserve privacy boundaries;
- how storage systems should support migration and backup.

This question SHOULD be resolved in a future storage standard.

### 20.13 Agent Review Boundaries

KS-0001 requires agent-created or agent-modified knowledge to remain reviewable where meaning, authority, privacy, lifecycle state, validation, publication, or downstream use are affected.

Future work SHOULD determine:

- which agent actions require human review;
- which agent actions may be automated;
- which agent actions are prohibited;
- how agents should propose changes;
- how agents should record provenance;
- how agents should handle privacy;
- how agents should handle conflicting knowledge;
- how agents should interact with validation.

This question SHOULD be resolved in a future agent standard.

### 20.14 Workflow Approval Boundaries

KS-0001 states that workflow completion is not the same as approval.

Future work SHOULD determine:

- which workflows may create draft records;
- which workflows may modify approved records;
- which workflows require human approval;
- which workflows may change lifecycle state;
- which workflows may change privacy classification;
- which workflows may publish, export, or synchronize records;
- how workflows should record provenance;
- how workflow failures should be handled.

This question SHOULD be resolved in a future workflow standard.

### 20.15 Implementation Profiles

KS-0001 is implementation-independent and does not define exact implementation profiles.

Future work SHOULD determine whether The Brain Standard should define profiles such as:

- Markdown file profile;
- Obsidian vault profile;
- database profile;
- graph database profile;
- local-first profile;
- multi-user profile;
- agent-assisted profile;
- archival profile;
- public publishing profile.

Implementation profiles SHOULD remain subordinate to KS-0001.

### 20.16 Open Questions Success

Open Questions are successful when unresolved issues remain explicit, traceable, and available for future governance without weakening the approved requirements, boundaries, compatibility expectations, or implementation independence of KS-0001.
