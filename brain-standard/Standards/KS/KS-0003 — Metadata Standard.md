# KS-0003 — Metadata Standard

Document ID: KS-0003
Title: Metadata Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-26
Last Updated: 2026-06-26
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.3 — Metadata Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and metadata rules are interpreted within KS-0003.

Where conflicts arise between metadata, object identity, Knowledge Objects, Knowledge Records, relationships, provenance, lifecycle states, authority, privacy classification, validation, storage behavior, agents, workflows, implementations, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0003 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0003 depends on KS-0001 for the foundational Knowledge Object Model and KS-0002 for Object Identity rules.

If KS-0003 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

If KS-0003 appears to conflict with KS-0001 or KS-0002, the conflict SHOULD be resolved according to document authority, scope, and governance review.

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
- Stable Object Identifier refers to an identifier governed as part of Object Identity and intended to remain stable across movement, renaming, copying, migration, import, export, and implementation replacement.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a Knowledge Object or Knowledge Record.
- Required Metadata refers to metadata that MUST be present or supported for a Knowledge Object or Knowledge Record to satisfy the applicable standard.
- Recommended Metadata refers to metadata that SHOULD be included when practical because it improves interpretation, reviewability, portability, automation reliability, validation, or long-term maintenance.
- Optional Metadata refers to metadata that MAY be included when useful but is not required for basic validity unless a future governed specification, workflow, implementation profile, or object-type rule requires it for a narrower scope.
- Metadata Category refers to a conceptual grouping of metadata by purpose, such as identity metadata, descriptive metadata, provenance metadata, lifecycle metadata, privacy metadata, relationship metadata, authority metadata, or validation metadata.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, agent, workflow, or evidence associated with a Knowledge Object or Knowledge Record.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, source material, standards, decisions, workflows, implementations, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Object or Knowledge Record.
- Authority Level refers to the governance weight, review status, or interpretive authority assigned to a document, Knowledge Object, Knowledge Record, source, or decision.
- Privacy Classification refers to explicit metadata describing the permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, or agent access expectations of a Knowledge Object or Knowledge Record.
- Validation refers to the process of checking whether a Knowledge Object or Knowledge Record satisfies the structural, metadata, provenance, relationship, lifecycle, privacy, compatibility, and implementation expectations defined by the relevant standards or specifications.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0003 is to define the standard-level metadata model for Knowledge Objects and Knowledge Records within The Brain Standard.

Metadata exists to make knowledge identifiable, interpretable, traceable, reviewable, portable, privacy-respecting, governable, validatable, and usable by both humans and AI systems.

KS-0003 establishes what metadata is, why metadata matters, what categories of metadata are required or recommended, how metadata supports Object Identity, and how metadata interacts with relationships, provenance, lifecycle state, authority, privacy classification, validation, import, export, migration, compatibility, workflows, agents, and implementations.

KS-0003 defines metadata at the conceptual standard level.

KS-0003 does not define exact Markdown front matter syntax, exact field names, exact schemas, exact database columns, exact storage layouts, exact validation tooling, exact serialization formats, exact allowed values, exact API fields, or implementation-specific metadata behavior.

Those details belong to future specifications, storage standards, serialization profiles, validation specifications, implementation profiles, and operational documents.

Metadata under The Brain Standard SHALL remain implementation-independent.

A compliant implementation MAY represent metadata through Markdown-compatible headers, front matter, structured fields, database columns, graph properties, API objects, sidecar files, embedded structures, or future formats.

The representation method may vary by implementation.

The meaning of metadata MUST remain explicit, portable, inspectable, and governed by the applicable standard.

Metadata MUST NOT become dependent on hidden application state, folder placement, filename conventions, user interface state, plugin behavior, database internals, agent memory, workflow memory, or undocumented implementation assumptions when that metadata affects meaning, identity, provenance, lifecycle, authority, privacy, validation, compatibility, or governance.

KS-0003 exists to prevent metadata from becoming inconsistent, hidden, implementation-specific, excessive, or confused with Object Identity.

Metadata supports knowledge meaning.

Metadata does not replace knowledge content.

Metadata supports Object Identity.

Metadata does not define Object Identity unless the metadata element is governed as part of Object Identity.

Metadata supports storage, workflows, agents, validation, and implementations.

Metadata does not allow those layers to redefine Knowledge Object meaning.

A compliant metadata model SHOULD reduce cognitive load by requiring only metadata that materially improves durability, portability, trustworthiness, reviewability, automation reliability, privacy protection, compatibility, or long-term maintainability.

KS-0003 is successful when future humans, agents, workflows, validators, storage systems, and implementations can interpret and preserve Knowledge Object metadata without relying on hidden assumptions, implementation lock-in, or unstable conventions.

## 2. Relationship to KS-0001 and KS-0002

KS-0003 builds directly on KS-0001 and KS-0002.

KS-0001 defines the foundational model for Knowledge Objects and Knowledge Records.

KS-0002 defines Object Identity and the rules that preserve stable identity across movement, renaming, copying, duplication, derivation, split, merge, supersession, deprecation, redirect, import, export, migration, validation, and compatibility.

KS-0003 defines the metadata model that supports those standards.

KS-0003 does not replace KS-0001 or KS-0002.

KS-0003 clarifies how metadata should be understood, categorized, required, recommended, preserved, validated, and used without weakening the Knowledge Object Model or Object Identity rules.

Under KS-0001, Knowledge Objects and Knowledge Records require explicit structure sufficient to preserve identity, meaning, source distinction, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, portability, and reviewability.

KS-0003 expands those expectations into a standard-level metadata model.

Under KS-0002, Object Identity must remain stable and independent of filenames, folder paths, display titles, storage locations, application-specific identifiers, and implementation-specific behavior.

KS-0003 preserves that boundary by requiring metadata to support Object Identity without becoming confused with Object Identity.

Metadata MAY include identifiers.

Only identifiers governed as Object Identity SHALL define stable Knowledge Object identity.

A metadata field, title, tag, path, alias, category, database identifier, application identifier, workflow identifier, or implementation-specific identifier MUST NOT be treated as Stable Object Identity unless a governed standard or specification explicitly defines that role.

KS-0003 depends on KS-0001 for the following concepts:

- Knowledge Object;
- Knowledge Record;
- Source Material;
- Required Metadata;
- Optional Metadata;
- relationships;
- provenance;
- lifecycle state;
- authority level;
- privacy classification;
- validation expectations;
- human and AI readability;
- compatibility expectations.

KS-0003 depends on KS-0002 for the following concepts:

- Object Identity;
- Stable Object Identifiers;
- identifier roles;
- identity persistence;
- identity changes;
- copy behavior;
- duplicate behavior;
- derivative behavior;
- split behavior;
- merge behavior;
- supersession;
- deprecation;
- redirects;
- identity rules during import, export, and migration.

KS-0003 SHALL preserve the distinction between metadata and Object Identity.

Object Identity answers:

- Which Knowledge Object is this?

Metadata answers:

- What is known about this Knowledge Object or Knowledge Record?
- How should it be interpreted?
- Where did it come from?
- What state is it in?
- What relationships does it have?
- What authority applies?
- What privacy boundaries apply?
- What validation expectations apply?
- What compatibility considerations apply?

Metadata may describe identity, but metadata as a whole is broader than identity.

A compliant metadata model MUST preserve the stable identity requirements of KS-0002 while also supporting the broader knowledge interpretation requirements of KS-0001.

Future specifications MAY define exact metadata fields, allowed values, schemas, serialization formats, metadata profiles, object-type-specific requirements, and validation rules.

Those specifications are valid only when they preserve the meaning, boundaries, and requirements of KS-0001, KS-0002, and KS-0003.

## 3. Metadata Definition

Metadata is explicit information associated with a Knowledge Object or Knowledge Record that supports identity, interpretation, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, discovery, automation, review, migration, or implementation behavior.

Metadata describes knowledge context.

Metadata does not replace the knowledge content itself.

Metadata SHALL be explicit when it affects meaning, identity, provenance, lifecycle state, authority, privacy classification, validation, compatibility, governance, or downstream use.

Metadata MAY be simple or complex depending on the purpose of the Knowledge Object, the maturity of the standard, the applicable specification, and the needs of a compliant implementation.

Metadata may describe:

- what the Knowledge Object is;
- what Knowledge Record represents it;
- what stable identity applies;
- what human-readable title or label applies;
- what type or category applies where governed;
- where the knowledge came from;
- what source material supports it;
- who or what created it;
- who or what modified it;
- what workflow or agent was involved;
- what relationships connect it to other entities;
- what lifecycle state applies;
- what authority level applies;
- what privacy classification applies;
- what validation state or validation expectation applies;
- what compatibility expectations apply;
- what import, export, or migration context applies;
- what implementation-specific information exists without defining standard meaning.

Metadata under The Brain Standard SHOULD be:

- explicit;
- inspectable;
- portable;
- human-readable where practical;
- AI-readable where practical;
- compatible with validation;
- compatible with migration;
- distinguishable from implementation-specific behavior;
- distinguishable from Object Identity unless governed as identity metadata;
- limited to what provides durable value.

Metadata MUST NOT depend solely on hidden application state when the metadata affects standard meaning.

Metadata MUST NOT be treated as valid standard metadata merely because an application, plugin, database, agent, workflow, or interface stores it.

Implementation metadata MAY exist.

Implementation metadata becomes standard metadata only when its meaning is defined by a governed standard or specification.

A title may be metadata.

A tag may be metadata.

A path may be metadata.

A folder may imply organizational context.

A database field may store metadata.

A user interface may display metadata.

An agent may generate metadata.

A workflow may update metadata.

However, none of these mechanisms define standard metadata unless the meaning is explicit, portable, and governed by the applicable standard or specification.

Metadata SHALL preserve the distinction between:

- standard metadata;
- implementation metadata;
- derived metadata;
- temporary metadata;
- workflow metadata;
- agent-generated metadata;
- validation metadata;
- presentation metadata;
- storage metadata;
- private operational notes.

This distinction prevents hidden behavior from becoming architecture by accident.

Metadata is successful when a future human, agent, workflow, validator, storage system, or implementation can understand what the metadata means, why it exists, how it should be handled, whether it affects governed meaning, and whether it remains valid across migration or implementation replacement.

## 4. Metadata Requirements

Metadata requirements define what metadata must preserve in order for Knowledge Objects and Knowledge Records to remain identifiable, interpretable, traceable, portable, reviewable, privacy-respecting, governable, and validatable.

A Knowledge Object or Knowledge Record SHALL include or support the metadata required by the applicable standard or specification.

At the KS-0003 standard level, compliant metadata SHALL preserve the meaning of required metadata categories even when exact field names, schemas, formats, or storage mechanisms vary.

Metadata MUST be explicit enough to support the applicable interpretation, review, validation, migration, and compatibility expectations.

Metadata MUST NOT exist only in hidden application state when that metadata affects:

- Object Identity;
- Knowledge Object meaning;
- Knowledge Record interpretation;
- source distinction;
- source references;
- provenance;
- relationships;
- lifecycle state;
- authority level;
- privacy classification;
- validation state;
- validation expectations;
- compatibility;
- import behavior;
- export behavior;
- migration behavior;
- governance;
- workflow behavior;
- agent permissions;
- downstream use.

Metadata SHOULD be represented in a form that remains inspectable by humans and interpretable by AI systems where practical.

Metadata MAY be stored or represented in different ways by different implementations.

Acceptable representation methods MAY include:

- Markdown-compatible metadata;
- document headers;
- front matter;
- structured fields;
- tables;
- database columns;
- graph properties;
- API fields;
- sidecar files;
- embedded metadata structures;
- metadata records;
- future governed representation formats.

The representation method does not define metadata meaning.

A metadata representation is compliant only if it preserves governed metadata meaning across inspection, validation, migration, export, import, and implementation replacement.

Metadata SHOULD be minimal where possible.

The Brain Standard SHOULD require only metadata that materially improves:

- stable identity;
- interpretation;
- provenance;
- source traceability;
- relationship clarity;
- lifecycle handling;
- authority handling;
- privacy protection;
- validation;
- compatibility;
- migration;
- human readability;
- AI readability;
- long-term maintainability.

Metadata requirements MUST NOT create unnecessary cognitive burden.

A metadata requirement is justified only when the value of preserving the metadata outweighs the burden of capturing, maintaining, validating, and migrating it.

Required metadata SHOULD be stable, durable, and broadly useful.

Recommended metadata SHOULD improve reviewability, automation reliability, discovery, interoperability, or maintenance.

Optional metadata SHOULD remain useful without becoming a hidden requirement.

Metadata MAY be created manually, automatically, or through a combination of human, agent, workflow, import, extraction, transformation, validation, migration, or implementation processes.

Agent-generated metadata SHOULD remain reviewable when it affects meaning, identity, provenance, relationships, lifecycle state, authority, privacy, validation, publication, export, or downstream use.

Workflow-generated metadata SHOULD preserve traceability when it changes interpretation, lifecycle state, validation state, authority, privacy, provenance, relationships, or compatibility.

Metadata changes SHOULD be traceable when they affect governed meaning, Object Identity, lifecycle state, authority, privacy classification, validation, provenance, relationships, source references, import, export, migration, or compatibility.

Metadata MUST preserve privacy boundaries.

Metadata MUST NOT expose restricted knowledge merely because it improves search, provenance, validation, linking, automation, review, export, publication, or implementation convenience.

Where metadata refers to restricted source material, restricted relationships, restricted provenance, or restricted content, the metadata SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Metadata MUST remain subordinate to higher-authority documents.

A metadata convention, field, tool default, workflow output, agent suggestion, implementation behavior, or common habit MUST NOT become a required part of The Brain Standard unless approved through the appropriate governance process.

## 5. Metadata Categories

Metadata categories organize metadata by architectural purpose.

Metadata categories help humans, agents, workflows, validators, storage systems, and implementations understand what kind of metadata is being used and what standard role it serves.

KS-0003 defines metadata categories at the conceptual level.

KS-0003 does not define exact field names, exact schemas, exact serialization formats, exact allowed values, exact validation rules, or exact storage layouts.

A future metadata specification MAY define those details.

At minimum, The Brain Standard recognizes the following metadata categories:

- identity metadata;
- descriptive metadata;
- structural metadata;
- provenance metadata;
- relationship metadata;
- lifecycle metadata;
- authority metadata;
- privacy metadata;
- validation metadata;
- compatibility metadata;
- import, export, and migration metadata;
- workflow metadata;
- agent metadata;
- implementation metadata.

### 5.1 Identity Metadata

Identity metadata supports recognition of the Knowledge Object or Knowledge Record.

Identity metadata MAY include stable object identifiers, record identifiers, aliases, legacy identifiers, external identifiers, redirect identifiers, or other identity-related information.

Identity metadata MUST preserve the Object Identity boundaries defined by KS-0002.

Only identifiers governed as Object Identity SHALL define stable Knowledge Object identity.

A title, alias, filename, path, tag, database identifier, workflow identifier, or application identifier MUST NOT become the sole source of stable Object Identity unless a future governed specification explicitly defines that behavior.

### 5.2 Descriptive Metadata

Descriptive metadata supports human recognition, interpretation, discovery, navigation, and communication.

Descriptive metadata MAY include title, human-readable label, description, summary, keywords, topics, categories, aliases, or other descriptive information.

Descriptive metadata SHOULD improve usability without replacing Object Identity, lifecycle state, authority, privacy classification, provenance, validation, or relationships.

Descriptive metadata MUST NOT be the only source of critical meaning when critical meaning affects standard interpretation.

### 5.3 Structural Metadata

Structural metadata describes how a Knowledge Object or Knowledge Record is organized or classified within the knowledge model.

Structural metadata MAY include object type, record type, content structure, section role, representation role, parent-child structure, containment context, or schema-related expectations.

Structural metadata SHOULD remain implementation-independent.

Structural metadata MUST NOT depend only on folder placement, filename convention, document layout, visual grouping, plugin behavior, database table, or hidden implementation state when it affects meaning.

### 5.4 Provenance Metadata

Provenance metadata describes origin, source, creation, transformation, responsibility, evidence, review, and change context.

Provenance metadata MAY identify source material, creator, editor, agent, workflow, import process, extraction process, transformation process, migration process, review state, or supporting evidence.

Provenance metadata SHOULD be sufficient for a future human, agent, workflow, validator, or implementation to understand where the knowledge came from and how it has been changed.

Provenance metadata MUST preserve privacy boundaries when provenance refers to restricted source material, restricted users, restricted workflows, or restricted content.

### 5.5 Relationship Metadata

Relationship metadata describes explicit connections between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, or other governed entities.

Relationship metadata MAY include relationship type, direction, target object, source object, context, evidence, review state, provenance, or validation state.

Relationship metadata SHOULD be explicit when relationships affect meaning, provenance, lifecycle state, authority, privacy, validation, source traceability, or governance.

Relationship metadata MUST NOT rely only on folder proximity, filename similarity, tag coincidence, backlink behavior, search ranking, graph visualization, or agent inference when the relationship affects meaning.

### 5.6 Lifecycle Metadata

Lifecycle metadata describes the current governed state of a Knowledge Object or Knowledge Record.

Lifecycle metadata MAY indicate draft, review, approved, rejected, deprecated, superseded, archived, experimental, imported, needs review, needs validation, or future governed lifecycle states.

This list is descriptive and does not define a complete approved lifecycle vocabulary.

Lifecycle metadata SHOULD remain compatible with the governance expectations defined by TB-0003 and the knowledge lifecycle expectations defined by KS-0001.

Lifecycle metadata MUST remain distinguishable from authority metadata, privacy metadata, and validation metadata.

### 5.7 Authority Metadata

Authority metadata describes governance weight, review status, interpretive authority, or trust context assigned to a Knowledge Object, Knowledge Record, source, document, or decision.

Authority metadata MAY indicate whether knowledge is constitutional, standard-level, specification-level, operational, source-derived, reviewed, approved for a narrow purpose, or otherwise governed by future authority rules.

Authority metadata MUST NOT be confused with factual truth, confidence, popularity, usefulness, source reliability, or lifecycle state.

Authority metadata SHOULD help humans, agents, workflows, validators, and implementations understand how strongly a record may be relied on for interpretation, governance, publication, or downstream use.

### 5.8 Privacy Metadata

Privacy metadata describes permitted visibility, access, handling, routing, synchronization, indexing, export, backup, publication, agent access, or disclosure expectations.

Privacy metadata MAY indicate whether knowledge is public, internal, private, restricted, confidential, sensitive, personal, exportable, non-exportable, agent-readable, agent-restricted, or governed by a future privacy classification.

This list is descriptive and does not define a complete approved privacy vocabulary.

Privacy metadata MUST be explicit enough to prevent accidental exposure where privacy affects handling.

Privacy metadata SHALL take precedence over operational convenience when privacy and convenience conflict.

### 5.9 Validation Metadata

Validation metadata describes whether a Knowledge Object or Knowledge Record satisfies applicable structure, metadata, provenance, relationship, lifecycle, privacy, authority, compatibility, or implementation expectations.

Validation metadata MAY indicate validation state, validation date, validator, validation profile, validation rule set, validation errors, validation warnings, or review expectations.

KS-0003 does not define exact validation states or validation tooling.

A future validation specification MAY define those details.

Validation metadata SHOULD support review and correction without becoming the sole authority for knowledge meaning.

### 5.10 Compatibility Metadata

Compatibility metadata describes how a Knowledge Object, Knowledge Record, metadata element, representation, import, export, migration, or implementation relates to compatibility expectations.

Compatibility metadata MAY identify standard version, specification version, metadata profile, serialization profile, migration status, compatibility notes, deprecated fields, legacy identifiers, or known limitations.

Compatibility metadata SHOULD help preserve interpretation across standard evolution, implementation replacement, and migration.

Compatibility metadata MUST NOT hide loss of meaning, provenance, privacy, relationships, lifecycle state, authority, validation, or Object Identity.

### 5.11 Import, Export, and Migration Metadata

Import, export, and migration metadata describes context created when knowledge moves between systems, formats, repositories, vaults, implementations, or standards versions.

This metadata MAY include source system, target system, import date, export date, migration date, migration process, conversion notes, legacy identifiers, mapping notes, loss warnings, validation results, or review state.

Import, export, and migration metadata SHOULD preserve traceability when movement affects identity, meaning, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, or source references.

### 5.12 Workflow Metadata

Workflow metadata describes the workflow context associated with a Knowledge Object or Knowledge Record.

Workflow metadata MAY identify workflow name, workflow state, workflow trigger, workflow actor, workflow output, review state, approval state, or workflow history.

Workflow metadata MUST NOT redefine Knowledge Object meaning, Object Identity, authority, privacy classification, lifecycle state, provenance, or validation unless a governed workflow explicitly permits that change.

Workflow metadata SHOULD remain traceable where workflow activity affects governed metadata or knowledge meaning.

### 5.13 Agent Metadata

Agent metadata describes agent involvement in creating, modifying, classifying, summarizing, linking, validating, reviewing, importing, exporting, or migrating knowledge.

Agent metadata MAY identify the agent, instruction, model class, tool, workflow, source material, output, review status, or transformation performed.

Agent metadata SHOULD remain reviewable when agent activity affects interpretation, relationships, lifecycle state, authority, privacy, validation, publication, export, or downstream use.

Agent metadata MUST NOT make an agent an unreviewable authority over knowledge.

### 5.14 Implementation Metadata

Implementation metadata supports a specific software system, database, interface, plugin, vault, workflow environment, or tool.

Implementation metadata MAY support display, indexing, caching, synchronization, database operation, application state, search, graph views, user interface behavior, or performance optimization.

Implementation metadata is allowed.

Implementation metadata MUST remain distinguishable from standard metadata when it affects portability, validation, migration, or interpretation.

Implementation metadata MUST NOT become required for Knowledge Object meaning unless a governed standard or specification explicitly adopts that metadata meaning.

### 5.15 Metadata Category Success

Metadata categories are successful when future humans, agents, workflows, validators, storage systems, and implementations can determine what kind of metadata exists, what role it serves, whether it affects governed meaning, whether it is required, recommended, optional, derived, temporary, or implementation-specific, and how it should be preserved across migration and implementation replacement.

## 6. Required Metadata

Required Metadata is metadata that MUST be present or supported for a Knowledge Object or Knowledge Record to satisfy the applicable standard.

Required Metadata exists to preserve the minimum context needed for knowledge to remain identifiable, interpretable, traceable, reviewable, privacy-respecting, portable, governable, and validatable across implementations.

KS-0003 defines Required Metadata at the conceptual standard level.

KS-0003 does not define exact field names, exact Markdown front matter syntax, exact schema syntax, exact database columns, exact storage layouts, exact allowed values, exact serialization formats, or exact validation tooling.

A future metadata specification MAY define those details.

Until such a specification exists, compliant Knowledge Objects and Knowledge Records MUST preserve the meaning of Required Metadata categories even when their representation differs across implementations.

A Knowledge Object or Knowledge Record SHALL include or support Required Metadata sufficient to express:

- stable Object Identity or a reference to stable Object Identity;
- a title or human-readable label;
- object type or record type where applicable;
- provenance;
- lifecycle state;
- privacy classification;
- authority level where applicable;
- source-reference metadata where source material materially supports the record;
- relationship metadata where relationships affect meaning, provenance, dependency, governance, lifecycle, validation, or interpretation;
- validation metadata or validation expectations where validation affects compliance, workflow behavior, import, export, migration, publication, or interoperability;
- creation context where creation context affects provenance, authority, reviewability, or compatibility;
- revision context where revision context affects meaning, lifecycle state, authority, privacy, validation, provenance, or compatibility;
- compatibility metadata where compatibility affects interpretation, migration, import, export, validation, or implementation replacement.

Required Metadata MUST be explicit enough that future humans, agents, workflows, validators, storage systems, and implementations can understand how the Knowledge Object or Knowledge Record should be interpreted and handled.

Required Metadata MUST NOT exist only in hidden application state when the metadata affects meaning, Object Identity, provenance, lifecycle state, authority, privacy classification, validation, compatibility, governance, workflow behavior, agent behavior, import, export, migration, or downstream use.

Required Metadata MAY be represented through different implementation mechanisms.

Permitted representation mechanisms MAY include:

- Markdown-compatible metadata;
- document headers;
- front matter;
- structured fields;
- database fields;
- graph properties;
- API fields;
- sidecar metadata;
- embedded metadata structures;
- metadata records;
- future governed representation formats.

The representation mechanism does not define the metadata meaning.

A representation is compliant only when it preserves Required Metadata meaning in a portable, inspectable, and validatable form.

### 6.1 Identity Metadata

A Knowledge Object or Knowledge Record SHALL include or reference identity metadata sufficient to determine what Knowledge Object is being represented.

Identity metadata MUST preserve the Object Identity boundaries defined by KS-0002.

Only identifiers governed as Object Identity SHALL define stable Knowledge Object identity.

Identity metadata MUST distinguish stable Object Identity from:

- title;
- alias;
- alternate identifier;
- legacy identifier;
- source identifier;
- temporary identifier;
- implementation-specific identifier;
- storage path;
- filename;
- tag;
- category;
- workflow identifier;
- agent-generated label.

Identity metadata MUST NOT depend only on filename, folder path, storage location, display title, tag, database identifier, application identifier, workflow identifier, agent label, or hidden implementation state.

Identity metadata SHOULD allow humans, agents, workflows, validators, import processes, export processes, migration processes, and implementations to determine whether two representations refer to the same Knowledge Object.

Where identity metadata changes, the change SHOULD remain traceable when it affects relationships, provenance, lifecycle state, authority, privacy classification, validation, import, export, migration, supersession, deprecation, duplicate detection, or compatibility.

### 6.2 Title or Human-Readable Label

A Knowledge Object or Knowledge Record SHALL include a title or human-readable label.

A title or human-readable label exists to support recognition, review, navigation, communication, display, search, and human usability.

A title or human-readable label SHOULD be concise, descriptive, and understandable without requiring hidden implementation context.

A title or human-readable label SHOULD remain distinguishable from stable Object Identity.

A title or human-readable label MUST NOT be treated as stable Object Identity unless a future governed specification explicitly defines that behavior.

A title or human-readable label MAY change without creating a new Object Identity when the underlying knowledge meaning remains the same.

Where a title change affects recognition, relationships, citations, source references, imports, exports, migrations, validation, or compatibility, the change SHOULD remain traceable.

### 6.3 Object Type or Record Type Metadata

A Knowledge Object or Knowledge Record SHOULD include or support object type or record type metadata where type affects interpretation, validation, workflow behavior, authority, privacy, relationships, or downstream use.

Object type metadata helps humans, agents, workflows, validators, storage systems, and implementations understand what kind of knowledge is being represented.

Record type metadata helps distinguish different representations, views, extracts, summaries, translations, exports, or implementation-specific records associated with the same Knowledge Object.

KS-0003 does not define a complete approved type vocabulary.

A future object-type specification MAY define exact allowed object types, record types, type hierarchies, type-specific metadata, validation rules, and compatibility expectations.

Until such a specification exists, type metadata SHOULD be used carefully and MUST NOT become an implementation-specific hidden assumption.

Object type or record type metadata MUST NOT depend only on folder placement, filename conventions, tags, visual layout, database table names, plugin behavior, interface state, or undocumented workflow assumptions when type affects meaning.

### 6.4 Provenance Metadata

A Knowledge Object or Knowledge Record SHALL include or support provenance metadata.

Provenance metadata identifies the origin, source, creator, editor, agent, workflow, import process, extraction process, transformation process, migration process, evidence, reasoning, review state, or change context associated with the knowledge.

Provenance metadata SHOULD be sufficient for a future human, agent, workflow, validator, storage system, or implementation to understand where the knowledge came from and how it was created or changed.

Provenance metadata SHOULD identify source material where source material materially supports the record.

Provenance metadata SHOULD identify agent or workflow involvement where an agent or workflow creates, modifies, classifies, summarizes, links, validates, imports, exports, migrates, or transforms knowledge.

Provenance metadata MUST distinguish evidence from interpretation where that distinction affects meaning, authority, validation, privacy, reviewability, or downstream use.

Provenance metadata MUST preserve privacy boundaries.

Provenance metadata MUST NOT expose restricted source material, restricted relationships, restricted actors, restricted workflows, or restricted content merely to improve traceability.

Where full provenance cannot be exposed due to privacy restrictions, the metadata SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

### 6.5 Lifecycle Metadata

A Knowledge Object or Knowledge Record SHALL include or support lifecycle metadata where lifecycle state affects interpretation, review, approval, authority, publication, supersession, deprecation, rejection, archival, validation, workflow behavior, privacy handling, or downstream use.

Lifecycle metadata describes the current governed state of the Knowledge Object or Knowledge Record.

Lifecycle metadata MAY describe whether knowledge is draft, under review, approved, rejected, superseded, deprecated, archived, experimental, imported, needs review, needs validation, or governed by a future lifecycle state.

This list is descriptive and does not define a complete approved lifecycle vocabulary.

A future lifecycle specification MAY define exact lifecycle states, allowed transitions, transition rules, approval requirements, review requirements, validation behavior, workflow effects, archival behavior, and migration expectations.

Lifecycle metadata MUST remain distinguishable from:

- authority metadata;
- privacy metadata;
- validation metadata;
- provenance metadata;
- implementation state;
- workflow state.

A Knowledge Object or Knowledge Record MUST NOT be treated as approved merely because it exists, is stored, is indexed, is linked, is referenced, appears in an implementation, or was generated by an agent.

Lifecycle metadata SHOULD remain traceable when lifecycle transitions affect meaning, authority, privacy, validation, provenance, relationships, publication, export, migration, or downstream use.

### 6.6 Privacy Metadata

A Knowledge Object or Knowledge Record SHALL include or support privacy metadata where privacy affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow behavior, validation, or downstream use.

Privacy metadata describes how knowledge may be accessed, handled, exposed, routed, shared, indexed, exported, synchronized, backed up, published, or processed by agents and workflows.

Privacy metadata MUST be explicit enough that humans, agents, workflows, validators, storage systems, and implementations can avoid exposing restricted knowledge by accident.

Privacy metadata MUST NOT depend only on folder placement, filename, tag, color, user interface state, plugin field, search ranking, workflow memory, agent memory, or hidden implementation state when privacy affects handling.

Privacy metadata SHALL take precedence over operational convenience when privacy and convenience conflict.

A Knowledge Record MUST NOT expose restricted source material merely because the record itself is easier to search, summarize, index, export, publish, or process.

A relationship, source reference, summary, extraction, transformation, index, embedding, export, backup, migration record, agent output, or workflow output MUST preserve applicable privacy boundaries.

A future privacy specification MAY define exact privacy classes, access rules, inheritance behavior, redaction rules, export rules, synchronization rules, indexing rules, backup rules, agent access rules, validation rules, and migration behavior.

Until such a specification exists, privacy-sensitive knowledge SHOULD be handled conservatively.

### 6.7 Authority Metadata

A Knowledge Object or Knowledge Record SHALL include or support authority metadata where authority affects interpretation, governance, review, trust, publication, validation, workflow behavior, or downstream use.

Authority metadata describes the governance weight, review status, interpretive authority, or approved use of a Knowledge Object, Knowledge Record, source, document, or decision.

Authority metadata MUST remain distinguishable from:

- factual truth;
- confidence;
- popularity;
- usefulness;
- source reliability;
- lifecycle state;
- privacy classification;
- validation state.

A record may have high authority but be superseded.

A record may be approved for a narrow purpose but not authoritative for broader interpretation.

A record may be private even when it has high authority.

A record may be valid structurally without having high authority.

Authority metadata SHOULD help humans, agents, workflows, validators, and implementations determine how strongly the record may be relied on for interpretation, governance, publication, automation, or downstream use.

A future authority specification MAY define exact authority levels, authority inheritance behavior, authority review rules, authority validation rules, and authority migration behavior.

### 6.8 Relationship Metadata

A Knowledge Object or Knowledge Record SHALL include or support relationship metadata where relationships affect meaning, provenance, dependency, hierarchy, sequence, evidence, source traceability, lifecycle state, authority, privacy, validation, governance, workflow behavior, or downstream use.

Relationship metadata describes explicit connections between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, agents, implementations, or other governed entities.

Relationship metadata SHOULD identify what is connected, what kind of connection exists, and why the relationship matters where that context affects interpretation.

Relationship metadata SHOULD preserve direction where direction affects meaning.

Relationship metadata SHOULD preserve type where type affects meaning.

Relationship metadata SHOULD preserve provenance where the origin or review state of the relationship affects interpretation, authority, privacy, validation, or downstream use.

Relationship metadata MUST NOT depend only on folder proximity, filename similarity, tag coincidence, backlink behavior, graph visualization, search ranking, application state, or agent inference when the relationship affects meaning.

Agent-generated or workflow-generated relationship metadata SHOULD remain reviewable when it affects interpretation, authority, privacy, lifecycle state, validation, publication, export, or downstream use.

A future relationship specification MAY define exact relationship types, directionality rules, cardinality rules, relationship metadata fields, validation rules, relationship provenance, inferred relationship behavior, and relationship lifecycle behavior.

### 6.9 Source-Reference Metadata

A Knowledge Object or Knowledge Record SHALL include source-reference metadata where Source Material materially supports the content, interpretation, classification, relationship, decision, validation, authority, or provenance of the record.

Source-reference metadata identifies or describes the source material that supports, explains, contextualizes, contradicts, or originated the knowledge.

Source-reference metadata SHOULD be sufficient for a future human, agent, workflow, validator, storage system, or implementation to locate, identify, or understand the relevant source material where access is permitted.

Source-reference metadata MAY refer to source material stored inside a compliant repository, stored externally, archived separately, referenced through a durable identifier, or represented through a future governed source-reference format.

Source-reference metadata MUST preserve the distinction between Source Material and Knowledge Records.

A source artifact is evidence, input, context, or reference.

A Knowledge Record is structured knowledge.

A source identifier MUST remain distinguishable from Object Identity unless a future governed specification defines a compliant identity relationship.

Source-reference metadata MUST preserve privacy boundaries.

A source reference MUST NOT expose restricted source material merely to improve traceability.

Where source material is unavailable, moved, deleted, restricted, corrupted, superseded, or replaced, source-reference metadata SHOULD indicate that condition when it affects interpretation, validation, authority, provenance, or review.

A future source-reference specification MAY define exact source-reference formats, source identifiers, citation behavior, archive behavior, source availability metadata, source reliability metadata, link durability expectations, and migration behavior.

### 6.10 Validation Metadata or Validation Expectations

A Knowledge Object or Knowledge Record SHALL include or support validation metadata or validation expectations where validation affects compliance, review, workflow behavior, import, export, migration, publication, interoperability, or implementation replacement.

Validation metadata describes whether a Knowledge Object or Knowledge Record satisfies applicable structure, metadata, provenance, relationship, lifecycle, privacy, authority, compatibility, and implementation expectations.

Validation metadata MAY indicate validation state, validation result, validation date, validator, validation profile, validation rule set, validation errors, validation warnings, or required review.

KS-0003 does not define exact validation states or validation tooling.

A future validation specification MAY define exact validation fields, validation states, validation rules, validator behavior, error behavior, warning behavior, validation profiles, and compatibility expectations.

Validation metadata MUST NOT replace human review where human review is required by governance, lifecycle, authority, privacy, or workflow rules.

Validation metadata MUST NOT silently override explicit metadata, Object Identity, provenance, lifecycle state, authority, privacy classification, relationships, or source references.

Validation metadata SHOULD make missing metadata, invalid metadata, unclear provenance, broken relationships, privacy risks, lifecycle ambiguity, compatibility issues, and meaning loss detectable.

### 6.11 Creation and Revision Context

A Knowledge Object or Knowledge Record SHALL include or support creation context where creation context affects provenance, identity, reviewability, lifecycle state, authority, validation, privacy, source traceability, or compatibility.

Creation context MAY identify when the object or record was created, who or what created it, what workflow or agent was involved, what source material supported it, what import process created it, or what initial review state applied.

A Knowledge Object or Knowledge Record SHALL include or support revision context where revision context affects meaning, provenance, privacy, authority, lifecycle state, validation, relationships, source references, compatibility, or downstream use.

Revision context MAY identify when the object or record was modified, who or what modified it, what workflow or agent was involved, what changed, why the change occurred, whether review occurred, whether validation changed, or whether compatibility was affected.

KS-0003 does not require a complete change-history model for every Knowledge Object or Knowledge Record.

However, changes that affect meaning, Object Identity, provenance, privacy, authority, lifecycle state, validation, relationships, source references, import, export, migration, or compatibility SHOULD remain traceable.

A future revision specification MAY define exact revision metadata, version metadata, change records, approval records, review records, and migration behavior.

### 6.12 Compatibility Metadata

A Knowledge Object or Knowledge Record SHALL include or support compatibility metadata where compatibility affects interpretation, validation, migration, import, export, implementation replacement, standard evolution, or downstream use.

Compatibility metadata helps preserve meaning across changes to standards, specifications, schemas, metadata profiles, storage systems, workflows, agents, validators, and implementations.

Compatibility metadata MAY identify standard version, specification version, metadata profile, serialization profile, migration status, deprecated metadata, superseded metadata, legacy identifiers, compatibility notes, known limitations, or migration mappings.

Compatibility metadata SHOULD make it clear when a representation is fully compatible, partially compatible, migrated, lossy, deprecated, superseded, or requiring review.

Compatibility metadata MUST NOT hide loss of meaning, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, or source references.

A conversion, migration, import, or export that loses meaning-critical metadata MUST NOT be presented as full compatibility.

A future compatibility specification MAY define exact compatibility states, metadata profile identifiers, migration metadata, deprecated metadata behavior, compatibility warnings, and validation requirements.

### 6.13 Required Metadata Role Boundaries

Required Metadata MUST remain distinguishable from Recommended Metadata, Optional Metadata, derived metadata, temporary metadata, implementation metadata, workflow metadata, and agent metadata.

Required Metadata defines the minimum metadata meaning needed for standard-level interpretation and use.

Recommended Metadata improves quality, reliability, automation, reviewability, discovery, or maintenance but may not be mandatory in every context.

Optional Metadata may improve usability or context but is not required for basic validity unless a future governed specification, workflow, implementation profile, or object-type rule requires it for a narrower scope.

Derived metadata may be generated from existing content, relationships, indexes, workflows, agents, validators, or implementations.

Temporary metadata may support drafting, ingestion, import, migration, validation, or workflow execution.

Implementation metadata may support application behavior, display, indexing, caching, synchronization, database operation, or performance optimization.

Workflow metadata may support workflow execution, routing, review, approval, or traceability.

Agent metadata may support review of agent involvement, generated output, classification, summarization, linking, validation, or transformation.

These metadata roles MAY overlap in practice.

Overlap is allowed.

Confusion is not allowed.

When a metadata element serves multiple roles, those roles SHOULD be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine which role controls governed interpretation.

A metadata element MUST NOT become Required Metadata merely because a tool, plugin, workflow, agent, implementation, template, or habit commonly uses it.

A metadata element becomes required only when required by an approved standard, specification, governed workflow, implementation profile, or other appropriate authority.

### 6.14 Required Metadata Success

Required Metadata is successful when a Knowledge Object or Knowledge Record remains:

- identifiable;
- interpretable;
- traceable;
- reviewable;
- privacy-respecting;
- portable;
- governable;
- validatable;
- compatible with migration;
- understandable to humans;
- interpretable by AI systems;
- independent of hidden implementation state.

Required Metadata is successful when future humans, agents, workflows, validators, storage systems, and implementations can determine:

- which Knowledge Object is represented;
- what title or label supports recognition;
- what type applies where applicable;
- where the knowledge came from;
- what source material supports it where applicable;
- what relationships affect interpretation;
- what lifecycle state applies;
- what authority applies where applicable;
- what privacy classification applies;
- what validation expectations apply;
- what creation or revision context matters;
- what compatibility concerns exist;
- whether the metadata remains valid across migration, import, export, and implementation replacement.

Required Metadata is successful when it preserves critical meaning without creating unnecessary cognitive burden, implementation lock-in, hidden requirements, privacy exposure, validation ambiguity, or confusion with Object Identity.

## 7. Recommended Metadata

Recommended Metadata is metadata that SHOULD be included when practical because it improves interpretation, reviewability, portability, automation reliability, validation, discovery, interoperability, migration, or long-term maintenance.

Recommended Metadata is not required for basic validity unless a future governed specification, workflow, implementation profile, object-type rule, or validation profile requires it for a narrower scope.

Recommended Metadata exists to improve the usefulness and durability of Knowledge Objects and Knowledge Records without creating unnecessary cognitive burden.

KS-0003 defines Recommended Metadata at the conceptual standard level.

KS-0003 does not define exact field names, exact schemas, exact Markdown front matter syntax, exact database columns, exact allowed values, exact serialization formats, or exact validation tooling for Recommended Metadata.

A future metadata specification MAY define those details.

Recommended Metadata SHOULD be included when it materially improves:

- human understanding;
- AI interpretation;
- reviewability;
- source traceability;
- relationship clarity;
- provenance clarity;
- lifecycle handling;
- authority handling;
- privacy handling;
- validation quality;
- discovery;
- navigation;
- automation reliability;
- import behavior;
- export behavior;
- migration behavior;
- compatibility;
- long-term maintainability.

Recommended Metadata SHOULD remain distinguishable from Required Metadata.

A Knowledge Object or Knowledge Record MUST NOT be treated as invalid merely because Recommended Metadata is absent unless a future governed specification, workflow, implementation profile, object-type rule, or validation profile explicitly makes that metadata required for a defined context.

Recommended Metadata SHOULD remain practical.

A recommended metadata element is justified only when its long-term value outweighs the burden of capturing, maintaining, validating, and migrating it.

Recommended Metadata MUST NOT create hidden requirements.

Recommended Metadata MUST NOT become required merely because a tool, plugin, template, workflow, agent, validator, implementation, or common habit expects it.

Recommended Metadata MAY become Required Metadata in a future governed standard or specification if governance determines that the metadata is necessary for identity, interpretation, provenance, privacy, validation, compatibility, interoperability, or long-term maintainability.

Where Recommended Metadata becomes required, the change SHOULD include compatibility review and migration guidance where applicable.

### 7.1 Descriptive Enrichment Metadata

A Knowledge Object or Knowledge Record SHOULD include descriptive enrichment metadata when additional description improves recognition, interpretation, discovery, navigation, review, or communication.

Descriptive enrichment metadata MAY include summaries, descriptions, alternate labels, explanatory notes, topic descriptions, scope notes, or other human-readable context.

Descriptive enrichment metadata SHOULD clarify what the Knowledge Object or Knowledge Record is about without replacing the primary content, stable Object Identity, Required Metadata, provenance, lifecycle state, authority, privacy classification, validation expectations, or relationships.

Descriptive enrichment metadata MUST NOT become the only source of critical meaning when that meaning affects standard interpretation.

Where descriptive enrichment metadata is generated by an agent, the metadata SHOULD remain reviewable when it affects interpretation, publication, privacy, authority, validation, relationship creation, or downstream use.

### 7.2 Alias and Alternate Recognition Metadata

A Knowledge Object or Knowledge Record SHOULD include alias or alternate recognition metadata when alternate names improve search, import, export, migration, duplicate detection, human recognition, or interoperability.

Alias and alternate recognition metadata MAY include alternate titles, former titles, abbreviations, spelling variants, legacy names, imported labels, external names, or human-recognition aids.

Alias and alternate recognition metadata SHOULD remain distinguishable from stable Object Identity.

An alias, alternate title, former title, abbreviation, spelling variant, legacy name, imported label, or external name MUST NOT define stable Object Identity unless a future governed specification explicitly defines that behavior.

Where an alias becomes the preferred title or primary label, the change SHOULD remain traceable when it affects recognition, relationships, citations, source references, import, export, migration, validation, or compatibility.

### 7.3 Discovery and Navigation Metadata

A Knowledge Object or Knowledge Record SHOULD include discovery and navigation metadata when it improves retrieval, browsing, grouping, filtering, sorting, search, review, or user orientation.

Discovery and navigation metadata MAY include keywords, topics, categories, tags, navigation hints, index terms, collection references, map references, or other discovery aids.

Discovery and navigation metadata SHOULD improve usability without becoming the only source of critical meaning.

A keyword, topic, category, tag, navigation hint, index term, or collection reference MUST NOT replace governed metadata for Object Identity, object type, lifecycle state, authority, privacy classification, provenance, validation, source references, or relationships.

Where discovery and navigation metadata affects workflow routing, privacy handling, authority handling, validation, import, export, migration, publication, or downstream use, the meaning SHOULD be represented through governed metadata rather than hidden convention.

### 7.4 Source Reliability and Source Availability Metadata

A Knowledge Object or Knowledge Record SHOULD include source reliability or source availability metadata when source condition affects interpretation, authority, validation, review, maintenance, migration, or downstream use.

Source reliability metadata MAY describe uncertainty, limitations, quality concerns, bias concerns, freshness concerns, conflict with other sources, or review concerns related to source material.

Source availability metadata MAY describe whether source material is available, missing, restricted, moved, archived, superseded, corrupted, externally hosted, partially available, or unavailable for review.

Source reliability metadata SHOULD remain distinguishable from authority metadata unless a future governed specification defines a relationship between those concepts.

Source availability metadata SHOULD remain distinguishable from source-reference metadata.

A source reference identifies or describes the source.

Source availability metadata describes whether and how that source can be accessed, verified, reviewed, or preserved.

Where source material becomes unavailable, restricted, corrupted, moved, superseded, or replaced, Recommended Metadata SHOULD preserve enough context for future humans, agents, workflows, validators, and implementations to understand the effect on interpretation, validation, authority, provenance, or review.

### 7.5 Review and Quality Metadata

A Knowledge Object or Knowledge Record SHOULD include review or quality metadata when review state, quality assessment, uncertainty, limitations, or maintenance concerns affect interpretation or downstream use.

Review and quality metadata MAY include review notes, editorial notes, quality notes, confidence notes, limitation notes, unresolved-question notes, maintenance notes, or future-review notes.

Review and quality metadata SHOULD remain distinguishable from lifecycle metadata, authority metadata, validation metadata, and approved knowledge content.

A review note, quality note, confidence note, limitation note, or editorial comment MUST NOT become authoritative merely because it appears near governed content.

Where review or quality metadata affects lifecycle state, approval, authority, privacy, validation, publication, export, workflow behavior, or downstream use, the relevant governed metadata SHOULD be updated rather than relying only on informal notes.

Agent-generated review or quality metadata SHOULD remain reviewable when it affects interpretation, classification, source handling, relationships, authority, privacy, validation, publication, or downstream use.

### 7.6 Relationship Context Metadata

A Knowledge Object or Knowledge Record SHOULD include relationship context metadata when relationships need explanation, evidence, review status, direction, type, scope, or provenance to remain interpretable.

Relationship context metadata MAY explain why a relationship exists, who or what created it, when it was created where applicable, what source material supports it, whether it was inferred, whether it was reviewed, whether it was approved, and whether it affects lifecycle state, authority, privacy, validation, or governance.

Relationship context metadata SHOULD be included when a relationship would otherwise be ambiguous.

Relationship context metadata SHOULD preserve direction where direction affects meaning.

Relationship context metadata SHOULD preserve relationship type where type affects meaning.

Relationship context metadata SHOULD preserve review state where review state affects trust, authority, workflow behavior, validation, or downstream use.

Relationship context metadata MUST NOT allow inferred, suggested, visual, search-based, or agent-generated relationships to become authoritative without review where review is required.

### 7.7 Workflow Reference Metadata

A Knowledge Object or Knowledge Record SHOULD include workflow reference metadata when workflow activity affects creation, transformation, review, approval, validation, import, export, migration, publication, maintenance, or downstream use.

Workflow reference metadata MAY identify the workflow involved, workflow state, workflow trigger, workflow actor, workflow output, review point, approval point, failure condition, rollback condition, or workflow history.

Workflow reference metadata SHOULD preserve traceability when workflow activity changes metadata, relationships, provenance, lifecycle state, authority, privacy classification, validation state, compatibility, or knowledge meaning.

Workflow reference metadata MUST NOT redefine Knowledge Object meaning, Object Identity, authority, privacy classification, lifecycle state, provenance, or validation unless a governed workflow explicitly permits that change.

Workflow completion MUST NOT be treated as approval unless a future governed workflow specification explicitly defines that behavior.

### 7.8 Agent Reference Metadata

A Knowledge Object or Knowledge Record SHOULD include agent reference metadata when agent activity affects creation, classification, summarization, extraction, transformation, linking, validation, review preparation, import, export, migration, publication, or downstream use.

Agent reference metadata MAY identify the agent, instruction, model class, tool, workflow, source material, generated output, transformation performed, review state, or approval state.

Agent reference metadata SHOULD make agent involvement reviewable where agent activity affects interpretation, relationships, lifecycle state, authority, privacy, validation, publication, export, or downstream use.

Agent reference metadata MUST NOT make an agent an unreviewable authority over knowledge.

Agent-generated metadata SHOULD remain distinguishable from human-authored metadata and approved governed metadata when that distinction affects reviewability, authority, privacy, validation, or downstream use.

Where agent output is accepted, rejected, revised, superseded, or used as the basis for governed knowledge, the relevant metadata SHOULD preserve enough context for future review.

### 7.9 Compatibility and Migration Notes

A Knowledge Object or Knowledge Record SHOULD include compatibility or migration notes when compatibility status, conversion history, prior structure, legacy metadata, deprecated metadata, migration mapping, or known limitation affects interpretation, validation, import, export, migration, or implementation replacement.

Compatibility and migration notes MAY describe prior systems, prior formats, prior identifiers, prior metadata profiles, conversion steps, migration decisions, deprecated structures, lossy transformations, validation results, compatibility warnings, or required review.

Compatibility and migration notes SHOULD preserve traceability without replacing Required Metadata.

A migration note MUST NOT hide loss of meaning-critical metadata.

A conversion, import, export, or migration that loses Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or other meaning-critical metadata MUST NOT be represented as fully compatible.

Compatibility and migration notes SHOULD help future humans, agents, workflows, validators, storage systems, and implementations determine whether additional review, mapping, repair, or migration guidance is needed.

### 7.10 External Reference and Citation Metadata

A Knowledge Object or Knowledge Record SHOULD include external reference or citation metadata when external sources, external systems, publications, identifiers, standards, datasets, repositories, or documents materially support interpretation, evidence, attribution, interoperability, publication, or review.

External reference and citation metadata MAY include citations, external identifiers, external URLs, archive references, repository references, publication references, dataset references, standard references, or other durable external references.

External reference and citation metadata SHOULD be durable where practical.

External reference and citation metadata SHOULD remain distinguishable from source-reference metadata unless the external reference materially supports the Knowledge Record.

Where an external reference materially supports the content, interpretation, classification, relationship, decision, validation, authority, or provenance of a Knowledge Record, it SHOULD be treated as source-reference metadata rather than only Recommended Metadata.

External references MUST NOT expose restricted information merely to improve attribution, discovery, publication, validation, interoperability, import, export, or migration.

### 7.11 Publication and Archival Metadata

A Knowledge Object or Knowledge Record SHOULD include publication or archival metadata when publication, sharing, export, preservation, retention, historical status, or archival handling affects interpretation, privacy, authority, validation, compatibility, or downstream use.

Publication metadata MAY describe whether knowledge is prepared for public release, internal distribution, restricted sharing, export, publication review, or downstream use.

Archival metadata MAY describe preservation status, retention expectations, historical value, restricted use, deprecation context, supersession context, or long-term storage expectations.

Publication metadata MUST preserve privacy classification.

Publication readiness MUST NOT override privacy boundaries, authority limits, lifecycle state, validation expectations, source restrictions, or governance rules.

Archival metadata SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, and implementations to understand whether the object or record remains active, historical, deprecated, superseded, restricted, preserved for evidence, or retained for compatibility.

### 7.12 Recommended Metadata Success

Recommended Metadata is successful when it improves the usefulness, trustworthiness, portability, reviewability, automation reliability, discovery, validation, interoperability, migration, and maintenance of Knowledge Objects and Knowledge Records without creating hidden requirements or unnecessary cognitive burden.

Recommended Metadata is successful when future humans, agents, workflows, validators, storage systems, and implementations can determine:

- what additional context improves interpretation;
- what aliases or alternate labels support recognition;
- what discovery metadata supports navigation;
- what source reliability or availability concerns exist;
- what review or quality notes affect interpretation;
- what relationship context matters;
- what workflow involvement matters;
- what agent involvement matters;
- what compatibility or migration notes matter;
- what external references or citations matter;
- what publication or archival handling applies;
- whether the metadata is recommended rather than required;
- whether the metadata remains valid across migration, import, export, and implementation replacement.

Recommended Metadata is successful when it adds durable value without weakening Required Metadata, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, compatibility, governance, or implementation independence.

## 8. Optional Metadata

Optional Metadata is metadata that MAY be included when useful but is not required for basic validity under KS-0003.

Optional Metadata exists to support additional context, usability, discovery, review, automation, implementation behavior, experimentation, reporting, presentation, or operational convenience without creating unnecessary burden or hidden requirements.

Optional Metadata SHOULD remain clearly distinguishable from Required Metadata and Recommended Metadata.

A Knowledge Object or Knowledge Record MUST NOT be treated as invalid merely because Optional Metadata is absent unless a future governed specification, workflow, implementation profile, object-type rule, or validation profile explicitly requires that metadata for a narrower scope.

KS-0003 defines Optional Metadata at the conceptual standard level.

KS-0003 does not define exact optional field names, exact schemas, exact Markdown front matter syntax, exact database columns, exact allowed values, exact serialization formats, or exact validation tooling.

A future metadata specification MAY define those details.

Optional Metadata MAY support:

- human usability;
- agent assistance;
- workflow convenience;
- search;
- filtering;
- sorting;
- visualization;
- display;
- reporting;
- indexing;
- summarization;
- experimentation;
- implementation optimization;
- local organization;
- temporary processing;
- operational notes;
- archival context;
- publication preparation;
- personal interpretation;
- future review.

Optional Metadata SHOULD remain useful without becoming required by accident.

Optional Metadata MUST NOT create hidden meaning that only one tool, plugin, workflow, agent, database, interface, or implementation can understand when that meaning affects standard interpretation.

Optional Metadata MAY be created manually, automatically, or through a combination of human, agent, workflow, import, extraction, transformation, validation, indexing, migration, or implementation processes.

Agent-generated Optional Metadata SHOULD remain reviewable when it affects interpretation, classification, relationship creation, privacy, authority, validation, publication, export, or downstream workflow behavior.

Optional Metadata SHOULD NOT silently override Required Metadata or Recommended Metadata.

If Optional Metadata conflicts with Required Metadata, Required Metadata SHALL take precedence unless a governed process revises the required metadata.

If Optional Metadata conflicts with Recommended Metadata, the conflict SHOULD be reviewed when it affects interpretation, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, or downstream use.

Optional Metadata MAY become Recommended Metadata or Required Metadata in a future governed standard or specification if governance determines that the metadata has durable value for interpretation, portability, validation, privacy, automation reliability, compatibility, or long-term maintenance.

When Optional Metadata is promoted to Recommended Metadata or Required Metadata, the change SHOULD include compatibility review and migration guidance where applicable.

### 8.1 Contextual Optional Metadata

A Knowledge Object or Knowledge Record MAY include contextual Optional Metadata when additional context improves understanding but is not necessary for basic validity.

Contextual Optional Metadata MAY include background notes, usage notes, interpretation notes, personal notes, local context, examples, reminders, assumptions, informal explanations, or future-review prompts.

Contextual Optional Metadata SHOULD remain distinguishable from approved knowledge content.

A contextual note MUST NOT become authoritative merely because it appears near governed content.

Where contextual Optional Metadata affects lifecycle state, authority, privacy, validation, publication, export, migration, or downstream use, the relevant governed metadata SHOULD be updated rather than relying only on informal context.

### 8.2 Presentation Metadata

A Knowledge Object or Knowledge Record MAY include presentation metadata when display behavior, formatting, layout, ordering, visualization, or interface support improves usability.

Presentation metadata MAY include display order, view preference, icon reference, color reference, layout hint, collapsed or expanded state, dashboard grouping, visual grouping, or rendering preference.

Presentation metadata MUST remain distinguishable from standard metadata that affects meaning.

Presentation metadata MUST NOT define Object Identity, object type, lifecycle state, authority, privacy classification, validation state, provenance, relationships, source references, or compatibility by itself.

Presentation metadata MAY improve usability inside a specific implementation.

Presentation metadata MUST NOT become required for the Knowledge Object or Knowledge Record to remain understandable outside that implementation.

### 8.3 Local Organization Metadata

A Knowledge Object or Knowledge Record MAY include local organization metadata when local grouping, personal workflow, repository organization, or implementation convenience improves daily use.

Local organization metadata MAY include local collection names, workspace references, vault-specific groupings, personal categories, project areas, local sorting keys, local review queues, or local navigation aids.

Local organization metadata SHOULD remain distinguishable from governed object type, governed relationships, lifecycle state, authority, privacy classification, and validation expectations.

Local organization metadata MUST NOT become the only source of critical meaning.

A local category, workspace, folder grouping, personal queue, or local navigation aid MUST NOT define standard meaning unless a future governed specification explicitly adopts that meaning.

### 8.4 Operational Notes

A Knowledge Object or Knowledge Record MAY include operational notes when practical use, maintenance, review, repair, cleanup, or future work would benefit from informal guidance.

Operational notes MAY include maintenance reminders, cleanup notes, review reminders, migration reminders, repair notes, follow-up notes, editorial notes, or implementation notes.

Operational notes SHOULD remain distinguishable from Required Metadata, Recommended Metadata, approved content, lifecycle state, authority metadata, validation metadata, and workflow metadata.

An operational note MUST NOT bypass governance, validation, privacy, lifecycle, authority, or review requirements.

Where an operational note identifies a required action that affects governed meaning, the relevant workflow, lifecycle, validation, or governance metadata SHOULD be updated where applicable.

### 8.5 Experimental Metadata

A Knowledge Object or Knowledge Record MAY include experimental metadata when testing new metadata concepts, workflows, validation approaches, agent behavior, indexing methods, relationship structures, or implementation patterns.

Experimental metadata MUST be clearly distinguishable from approved standard metadata when confusion could affect interpretation, validation, compatibility, privacy, authority, lifecycle state, relationships, or downstream use.

Experimental metadata MUST NOT redefine Knowledge Object meaning, Object Identity, Required Metadata, Recommended Metadata, lifecycle state, authority, privacy classification, provenance, relationships, validation, or compatibility.

Experimental metadata SHOULD remain isolated enough that it can be revised, removed, deprecated, promoted, or superseded without breaking standard meaning.

If experimental metadata proves durable and broadly useful, it MAY be proposed for promotion through the appropriate governance process.

### 8.6 Derived Metadata

A Knowledge Object or Knowledge Record MAY include derived metadata when metadata is generated from content, source material, relationships, indexes, embeddings, workflows, agents, validators, imports, exports, migrations, or implementations.

Derived metadata MAY include extracted keywords, generated summaries, inferred topics, calculated statistics, detected entities, link suggestions, duplicate-detection signals, indexing hints, embedding references, or validation-derived notes.

Derived metadata SHOULD identify or preserve enough context to determine how it was generated when the generation method affects interpretation, validation, authority, privacy, compatibility, or downstream use.

Derived metadata MUST NOT override explicit Required Metadata, Recommended Metadata, Object Identity, provenance, lifecycle state, authority, privacy classification, relationships, source references, or validation expectations.

Derived metadata SHOULD be regenerable or replaceable where practical.

If derived metadata cannot be regenerated and affects interpretation, validation, migration, or compatibility, its provenance SHOULD be preserved.

### 8.7 Temporary Metadata

A Knowledge Object or Knowledge Record MAY include temporary metadata during drafting, ingestion, import, export, migration, validation, workflow execution, agent processing, review, or repair.

Temporary metadata MAY include temporary identifiers, staging notes, import flags, migration flags, review queues, processing status, workflow scratch data, validation scratch data, or agent-processing notes.

Temporary metadata SHOULD be clearly distinguishable from stable metadata.

Temporary metadata MUST NOT be treated as stable Object Identity, stable provenance, lifecycle state, authority, privacy classification, validation state, relationship authority, source-reference authority, or compatibility state unless a governed process explicitly promotes or maps it into stable metadata.

Temporary metadata SHOULD be resolved, removed, archived, mapped, or reviewed before the Knowledge Object or Knowledge Record is treated as complete where temporary metadata affects interpretation, validation, import, export, migration, compatibility, privacy, or downstream use.

### 8.8 Implementation Optimization Metadata

A Knowledge Object or Knowledge Record MAY include implementation optimization metadata when an implementation needs additional metadata for performance, indexing, caching, synchronization, user interface behavior, database operation, search optimization, graph display, or local automation.

Implementation optimization metadata MAY include cache keys, search indexes, embedding identifiers, sync identifiers, display settings, plugin settings, database indexes, graph-layout data, application state, or implementation-specific processing markers.

Implementation optimization metadata MUST remain distinguishable from standard metadata.

Implementation optimization metadata MUST NOT define Knowledge Object meaning, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or compatibility by itself.

A compliant implementation SHOULD be able to remove, regenerate, replace, or migrate implementation optimization metadata without losing standard meaning.

Where implementation optimization metadata affects privacy, export, synchronization, indexing, backup, publication, or agent access, privacy classification and governance expectations MUST be preserved.

### 8.9 Personalization Metadata

A Knowledge Object or Knowledge Record MAY include personalization metadata when personal preferences, local use patterns, reading status, learning status, review habits, or user-specific organization improves usability.

Personalization metadata MAY include favorites, personal ratings, reading status, personal priority, personal reminders, local importance markers, user-specific notes, or preferred views.

Personalization metadata SHOULD remain distinguishable from authority metadata, lifecycle metadata, validation metadata, privacy metadata, and approved knowledge content.

A personal rating, priority marker, favorite marker, or reading status MUST NOT be treated as authority, validation, truth, approval, or lifecycle state unless a future governed specification explicitly defines that behavior.

Personalization metadata SHOULD remain portable where practical but MAY be implementation-specific when it does not affect standard meaning.

### 8.10 Optional Metadata Boundaries

Optional Metadata MUST remain subordinate to Required Metadata, Recommended Metadata, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, compatibility expectations, and governance.

Optional Metadata MUST NOT silently change:

- Knowledge Object meaning;
- Object Identity;
- source distinction;
- source references;
- provenance;
- relationships;
- lifecycle state;
- authority level;
- privacy classification;
- validation state;
- validation expectations;
- import behavior;
- export behavior;
- migration behavior;
- compatibility behavior;
- governance interpretation.

Optional Metadata MAY assist humans, agents, workflows, validators, storage systems, and implementations.

Optional Metadata MUST NOT become an unreviewed substitute for governed metadata.

Optional Metadata MAY be ignored by an implementation unless a future governed specification, workflow, implementation profile, object-type rule, or validation profile requires support for that metadata in a defined context.

An implementation that does not preserve Optional Metadata SHOULD avoid claiming full fidelity when the omitted metadata affects interpretation, reviewability, migration, usability, publication, archival handling, or downstream use.

### 8.11 Optional Metadata Success

Optional Metadata is successful when it improves usability, context, discovery, review, automation, implementation behavior, experimentation, presentation, or maintenance without creating hidden requirements, implementation lock-in, privacy exposure, validation ambiguity, authority confusion, or cognitive burden.

Optional Metadata is successful when future humans, agents, workflows, validators, storage systems, and implementations can determine:

- what optional context exists;
- whether the metadata affects interpretation;
- whether the metadata is personal, temporary, derived, experimental, presentation-related, operational, or implementation-specific;
- whether the metadata may be ignored safely;
- whether the metadata should be preserved during migration;
- whether the metadata affects privacy handling;
- whether the metadata requires review before publication, export, migration, or downstream use;
- whether the metadata should be promoted, revised, deprecated, superseded, archived, or removed.

Optional Metadata is successful when it provides practical value while preserving the authority, clarity, portability, privacy, validation, and implementation independence of The Brain Standard.

## 9. Metadata Role Boundaries

Metadata Role Boundaries define how different kinds of metadata are distinguished so that metadata does not become confused with Object Identity, knowledge content, storage structure, implementation behavior, workflow state, agent output, or presentation behavior.

Metadata Role Boundaries exist to prevent hidden assumptions from becoming architecture by accident.

A compliant metadata model SHALL preserve the distinction between:

- Object Identity;
- Knowledge Object meaning;
- Knowledge Record content;
- Required Metadata;
- Recommended Metadata;
- Optional Metadata;
- standard metadata;
- implementation metadata;
- derived metadata;
- temporary metadata;
- workflow metadata;
- agent metadata;
- validation metadata;
- presentation metadata;
- storage metadata;
- privacy metadata;
- authority metadata;
- lifecycle metadata;
- relationship metadata;
- provenance metadata.

These roles MAY overlap in practice.

Overlap is allowed.

Confusion is not allowed.

When a metadata element serves more than one role, the roles SHOULD be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine which role controls governed interpretation.

A metadata element MUST NOT become standard metadata merely because it exists in a tool, plugin, database, template, file header, user interface, agent output, workflow log, index, cache, graph view, or implementation-specific field.

A metadata element becomes standard metadata only when its meaning is defined by an approved standard, specification, governed workflow, implementation profile, or other appropriate authority.

### 9.1 Metadata and Object Identity

Metadata MUST remain distinguishable from Object Identity.

Object Identity identifies which Knowledge Object is being represented.

Metadata describes what is known about the Knowledge Object or Knowledge Record.

Metadata MAY include identity-related information.

Only identifiers governed as Object Identity SHALL define stable Knowledge Object identity.

A title, alias, tag, category, filename, folder path, storage location, database identifier, application identifier, workflow identifier, agent-generated label, source identifier, or temporary identifier MUST NOT define stable Object Identity by itself unless a future governed specification explicitly defines that behavior.

Metadata may support identity.

Metadata does not replace identity.

When metadata affects identity interpretation, the metadata SHOULD preserve enough context for humans, agents, workflows, validators, import processes, export processes, migration processes, and implementations to distinguish stable Object Identity from supporting identifiers.

### 9.2 Metadata and Knowledge Content

Metadata MUST remain distinguishable from Knowledge Object content and Knowledge Record content.

Knowledge content expresses the substance of the knowledge.

Metadata provides context about the knowledge.

A metadata element MUST NOT replace the knowledge content itself unless a future governed specification explicitly defines a metadata-only representation for a narrow purpose.

A summary, description, extracted keyword, classification, tag, title, or generated note MUST NOT be treated as the complete Knowledge Record unless a governed process defines that representation as complete for a specific object type or record type.

Metadata MAY improve interpretation of content.

Metadata MUST NOT silently change content meaning.

Where metadata changes interpretation, authority, privacy, validation, lifecycle state, relationships, provenance, or downstream use, the change SHOULD be explicit and reviewable.

### 9.3 Metadata and Filenames

Metadata MUST remain distinguishable from filenames.

A filename may support storage, recognition, sorting, retrieval, export, import, backup, or human usability.

A filename MUST NOT be the only source of Object Identity, lifecycle state, authority, privacy classification, validation state, provenance, relationship meaning, source-reference meaning, or compatibility status.

A compliant implementation MAY use filenames as a convenience mechanism.

A compliant implementation MUST NOT require filename interpretation as the only way to preserve critical metadata meaning.

Where a filename reflects metadata, the underlying metadata meaning SHOULD remain explicit or recoverable through governed metadata rather than depending only on the filename.

### 9.4 Metadata and Folder Paths

Metadata MUST remain distinguishable from folder paths and storage locations.

A folder path may support organization, retrieval, navigation, backup, synchronization, export, import, or implementation convenience.

A folder path MUST NOT be the only source of Object Identity, object type, lifecycle state, authority, privacy classification, validation state, provenance, source distinction, relationship meaning, or compatibility status.

Moving a Knowledge Object or Knowledge Record to another folder MUST NOT silently change its standard meaning.

Moving a Knowledge Object or Knowledge Record to another folder MUST NOT silently change its Object Identity.

Moving a Knowledge Object or Knowledge Record to another folder MUST NOT silently weaken privacy classification, authority, lifecycle state, validation expectations, provenance, relationships, or compatibility.

Where folder placement implies organization, the implication SHOULD remain distinguishable from governed metadata.

### 9.5 Metadata and Tags

Metadata MUST remain distinguishable from tags.

Tags may support discovery, filtering, navigation, grouping, search, visualization, workflow convenience, or implementation behavior.

A tag MUST NOT be the only source of critical meaning when that meaning affects Object Identity, object type, lifecycle state, authority, privacy classification, validation state, provenance, relationships, source references, import, export, migration, or compatibility.

A tag MAY reflect governed metadata.

A tag MUST NOT replace governed metadata unless a future governed specification explicitly defines tag behavior for a narrow scope.

Where a tag affects workflow routing, privacy handling, authority handling, validation, import, export, migration, publication, or downstream use, the meaning SHOULD be represented through governed metadata rather than hidden tag convention.

### 9.6 Metadata and User Interface State

Metadata MUST remain distinguishable from user interface state.

User interface state may include visible panels, collapsed sections, view modes, colors, icons, filters, dashboards, graph layouts, sorting preferences, display preferences, selected items, or local presentation settings.

User interface state MAY improve usability.

User interface state MUST NOT define Knowledge Object meaning, Object Identity, lifecycle state, authority, privacy classification, validation state, provenance, relationships, source references, or compatibility by itself.

A Knowledge Object or Knowledge Record SHOULD remain understandable when viewed outside the user interface that created or displayed it.

A compliant implementation MUST NOT require hidden user interface state for critical metadata interpretation.

### 9.7 Metadata and Database Fields

Metadata MUST remain distinguishable from database fields.

A database field may store metadata.

A database field does not define standard metadata merely because it exists.

A database field becomes standard metadata only when its meaning is governed by an approved standard, specification, implementation profile, or other appropriate authority.

A database identifier, row number, table name, index key, cache key, internal ID, or query result MUST NOT define Object Identity, lifecycle state, authority, privacy classification, validation state, provenance, relationships, source references, or compatibility by itself.

A compliant database-backed implementation MUST preserve governed metadata meaning across export, import, migration, backup, restoration, synchronization, validation, and implementation replacement.

### 9.8 Metadata and Application or Plugin Behavior

Metadata MUST remain distinguishable from application behavior and plugin behavior.

Applications and plugins MAY create, display, transform, validate, index, infer, cache, synchronize, or organize metadata.

Application or plugin behavior MUST NOT redefine standard metadata meaning unless the behavior is governed by an approved standard, specification, implementation profile, or other appropriate authority.

A plugin field, tool default, automatic classification, graph relationship, inferred backlink, generated tag, validation result, display state, or application-specific property MUST NOT become required standard metadata by accident.

Where an application or plugin creates metadata that affects meaning, identity, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, import, export, migration, or downstream use, the metadata SHOULD remain explicit, reviewable, and portable.

### 9.9 Metadata and Workflow State

Metadata MUST remain distinguishable from workflow state.

Workflow state describes the status or context of a process.

Metadata describes context associated with a Knowledge Object or Knowledge Record.

Workflow state MAY create or update metadata when permitted by a governed workflow.

Workflow completion MUST NOT be treated as approval unless a future governed workflow specification explicitly defines that behavior.

Workflow state MUST NOT silently redefine Object Identity, Knowledge Object meaning, lifecycle state, authority, privacy classification, provenance, validation, relationships, source references, or compatibility.

Where workflow state affects governed metadata, the change SHOULD be traceable to the workflow, triggering event, responsible actor, agent involvement where applicable, source material where applicable, review state, and approval state.

### 9.10 Metadata and Agent Output

Metadata MUST remain distinguishable from agent output.

Agent output may include generated summaries, classifications, proposed relationships, extracted entities, validation suggestions, metadata suggestions, import mappings, migration notes, or review recommendations.

Agent output MUST NOT become authoritative metadata merely because an agent produced it.

Agent-generated metadata SHOULD remain reviewable when it affects interpretation, relationships, lifecycle state, authority, privacy, validation, publication, export, import, migration, compatibility, or downstream use.

An agent MUST NOT silently redefine Knowledge Object meaning, Object Identity, authority, privacy classification, lifecycle state, provenance, relationships, validation, or governed metadata.

Where agent output is accepted into governed metadata, the accepted metadata SHOULD preserve enough provenance for future review where the provenance affects interpretation, authority, privacy, validation, compatibility, or downstream use.

### 9.11 Metadata and Validation State

Metadata MUST remain distinguishable from validation state.

Validation state describes whether a Knowledge Object, Knowledge Record, metadata element, relationship, source reference, lifecycle state, privacy classification, authority assignment, import, export, migration, or representation satisfies applicable expectations.

Validation state MAY be represented as metadata.

Validation state MUST NOT replace the underlying metadata being validated.

A valid validation state MUST NOT imply factual truth, authority, approval, privacy clearance, publication readiness, or lifecycle approval unless a future governed specification explicitly defines that relationship.

A validation result SHOULD identify what was checked where practical.

A validation result SHOULD distinguish errors, warnings, missing metadata, incomplete metadata, ambiguous metadata, unsupported metadata, compatibility issues, privacy risks, and review requirements where practical.

### 9.12 Metadata and Privacy Handling

Metadata MUST remain distinguishable from privacy handling, but metadata MUST support privacy handling where privacy affects access, exposure, routing, indexing, synchronization, export, backup, publication, or agent access.

Privacy metadata describes handling expectations.

Privacy handling applies those expectations through workflows, agents, storage systems, implementations, validators, exports, imports, backups, indexes, publications, or access controls.

A privacy label alone is not sufficient if the implementation, workflow, export, index, backup, or agent system ignores it.

A compliant metadata model SHOULD make privacy expectations explicit enough to support enforcement, review, validation, and migration.

Metadata MUST NOT expose restricted content merely by describing, summarizing, indexing, linking, or referencing restricted knowledge.

Where privacy handling and metadata usefulness conflict, privacy SHALL take precedence.

### 9.13 Metadata and Authority

Metadata MUST remain distinguishable from authority.

Authority metadata may describe governance weight, review status, interpretive authority, or approved use.

Authority itself is governed by document status, authority level, review process, lifecycle state, approval process, and applicable standards or specifications.

Authority metadata MUST NOT be confused with popularity, confidence, validation success, usefulness, recency, source availability, source reliability, search ranking, or agent certainty.

A Knowledge Object or Knowledge Record MAY be valid but low authority.

A Knowledge Object or Knowledge Record MAY be high authority but superseded.

A Knowledge Object or Knowledge Record MAY be private regardless of authority.

A Knowledge Object or Knowledge Record MAY be useful without being authoritative.

Authority metadata SHOULD help interpretation.

Authority metadata MUST NOT bypass governance.

### 9.14 Metadata and Implementation Profiles

Metadata MUST remain distinguishable from implementation profiles.

An implementation profile may define how a specific implementation represents, stores, validates, displays, imports, exports, migrates, or synchronizes metadata.

An implementation profile MAY require additional metadata for that implementation’s scope.

An implementation profile MUST NOT override KS-0003, KS-0002, KS-0001, or any higher-authority document.

An implementation profile MUST distinguish implementation-specific metadata from standard metadata when the distinction affects portability, validation, migration, compatibility, privacy, or interpretation.

A Knowledge Object or Knowledge Record SHOULD remain interpretable outside a specific implementation profile where practical.

Where implementation-profile metadata is lost during migration or export, the migration or export process SHOULD identify whether the loss affects standard meaning, usability, validation, compatibility, or downstream use.

### 9.15 Metadata Role Boundary Success

Metadata Role Boundaries are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine:

- what metadata exists;
- what role the metadata serves;
- whether the metadata is required, recommended, optional, derived, temporary, workflow-related, agent-generated, presentation-related, storage-related, or implementation-specific;
- whether the metadata affects Object Identity;
- whether the metadata affects Knowledge Object meaning;
- whether the metadata affects provenance;
- whether the metadata affects relationships;
- whether the metadata affects lifecycle state;
- whether the metadata affects authority;
- whether the metadata affects privacy classification;
- whether the metadata affects validation;
- whether the metadata affects compatibility;
- whether the metadata can be ignored safely;
- whether the metadata must be preserved during migration;
- whether the metadata requires review before publication, export, import, migration, automation, or downstream use.

Metadata Role Boundaries are successful when metadata supports knowledge without becoming confused with identity, content, filenames, folders, tags, user interface state, database internals, plugin behavior, workflow state, agent output, validation results, privacy enforcement, authority, or implementation-specific behavior.

## 10. Metadata and Object Identity

Metadata and Object Identity are closely related but not interchangeable.

Object Identity defines which Knowledge Object is being represented.

Metadata describes context associated with a Knowledge Object or Knowledge Record.

A compliant metadata model SHALL support Object Identity without weakening, replacing, duplicating, or confusing the Object Identity rules defined by KS-0002.

Metadata MAY describe identity.

Metadata MAY reference identity.

Metadata MAY preserve identity-related context.

Metadata MUST NOT redefine stable Object Identity unless a future governed specification explicitly assigns that role to a metadata element.

Only identifiers governed as Object Identity SHALL define stable Knowledge Object identity.

A Knowledge Object or Knowledge Record MUST preserve enough identity metadata for future humans, agents, workflows, validators, import processes, export processes, migration processes, and implementations to determine which Knowledge Object is being represented.

Identity-related metadata SHOULD remain explicit, portable, inspectable, and validatable.

Identity-related metadata MUST NOT depend only on hidden application state, filename, folder path, storage location, display title, tag, category, database identifier, application identifier, workflow identifier, agent-generated label, index key, cache key, or user interface state.

### 10.1 Identity Metadata Purpose

Identity metadata exists to support recognition, continuity, traceability, duplicate detection, relationship integrity, import, export, migration, validation, supersession, deprecation, redirect behavior, and implementation replacement.

Identity metadata SHOULD help determine:

- which Knowledge Object is represented;
- whether two records represent the same Knowledge Object;
- whether an identifier is stable or temporary;
- whether an identifier is governed or implementation-specific;
- whether an identifier is current, legacy, redirected, deprecated, superseded, or external;
- whether identity-related metadata affects relationships;
- whether identity-related metadata affects provenance;
- whether identity-related metadata affects migration;
- whether identity-related metadata affects validation;
- whether identity-related metadata affects compatibility.

Identity metadata MUST support Object Identity.

Identity metadata MUST NOT become a substitute for governed Object Identity rules.

### 10.2 Stable Object Identifier Metadata

A Knowledge Object or Knowledge Record SHALL include or reference metadata sufficient to identify the Stable Object Identifier where a Stable Object Identifier is required by the applicable standard or specification.

Stable Object Identifier metadata MUST remain distinguishable from:

- title;
- alias;
- alternate label;
- display name;
- filename;
- folder path;
- storage location;
- tag;
- category;
- external identifier;
- source identifier;
- temporary identifier;
- workflow identifier;
- agent-generated identifier;
- application identifier;
- database identifier;
- index identifier;
- cache identifier.

Stable Object Identifier metadata MUST preserve identity continuity across movement, renaming, copying, import, export, migration, implementation replacement, and storage reorganization.

A Stable Object Identifier MUST NOT change merely because a file is renamed, moved, copied, reformatted, indexed, exported, imported, migrated, synchronized, backed up, restored, or displayed differently.

Where Stable Object Identifier metadata is missing, ambiguous, duplicated, corrupted, conflicting, or incompatible, the condition SHOULD be detectable during validation or review.

### 10.3 Supporting Identifier Metadata

A Knowledge Object or Knowledge Record MAY include supporting identifier metadata.

Supporting identifier metadata MAY include aliases, alternate identifiers, external identifiers, legacy identifiers, source identifiers, import identifiers, migration identifiers, redirect identifiers, deprecated identifiers, or implementation-specific identifiers.

Supporting identifier metadata SHOULD clarify its role where confusion with Stable Object Identity is possible.

Supporting identifier metadata MUST NOT define stable Object Identity unless a future governed specification explicitly assigns that role.

Supporting identifier metadata SHOULD remain traceable when it affects duplicate detection, relationship resolution, source references, import, export, migration, validation, compatibility, supersession, deprecation, or redirects.

Supporting identifier metadata MAY help humans, agents, workflows, validators, storage systems, and implementations map old representations to current Knowledge Objects.

### 10.4 Title and Identity Boundary

A title or human-readable label MAY support recognition of a Knowledge Object or Knowledge Record.

A title or human-readable label MUST remain distinguishable from stable Object Identity.

A title MUST NOT be the only source of stable Object Identity unless a future governed specification explicitly defines that behavior.

A Knowledge Object or Knowledge Record MAY change title without changing Object Identity when the underlying knowledge identity remains the same.

A title change SHOULD remain traceable when the change affects recognition, relationships, source references, citations, import, export, migration, validation, compatibility, publication, or downstream use.

Where a title is used for display, sorting, navigation, search, or publication, the implementation SHOULD preserve the distinction between display recognition and stable identity.

### 10.5 Filename and Identity Boundary

A filename MAY support recognition, storage, sorting, retrieval, import, export, backup, or human usability.

A filename MUST remain distinguishable from stable Object Identity.

A filename MUST NOT be the only source of stable Object Identity unless a future governed specification explicitly defines that behavior.

A Knowledge Object or Knowledge Record MAY be renamed without changing Object Identity when the underlying knowledge identity remains the same.

A filename change SHOULD NOT require relationship repair, source-reference repair, authority repair, privacy repair, lifecycle repair, validation repair, or compatibility repair when stable identity metadata is preserved.

Where filenames reflect identifiers, the governed identity metadata SHOULD remain explicit or recoverable without depending only on filename parsing.

### 10.6 Folder Path and Identity Boundary

A folder path or storage location MAY support organization, retrieval, navigation, synchronization, backup, import, export, migration, or implementation convenience.

A folder path or storage location MUST remain distinguishable from stable Object Identity.

A folder path or storage location MUST NOT be the only source of stable Object Identity unless a future governed specification explicitly defines that behavior.

A Knowledge Object or Knowledge Record MAY move between folders, repositories, vaults, storage systems, databases, or implementations without changing Object Identity when the underlying knowledge identity remains the same.

Moving a Knowledge Object or Knowledge Record MUST NOT silently create a new Object Identity.

Moving a Knowledge Object or Knowledge Record MUST NOT silently erase identity continuity.

Where storage movement affects identity resolution, migration, import, export, validation, compatibility, or relationship integrity, the movement SHOULD remain traceable.

### 10.7 Tags, Categories, and Identity Boundary

Tags, categories, topics, labels, groups, or collections MAY support discovery, navigation, filtering, classification, workflow routing, or implementation behavior.

Tags, categories, topics, labels, groups, or collections MUST remain distinguishable from stable Object Identity.

A tag, category, topic, label, group, or collection MUST NOT define stable Object Identity unless a future governed specification explicitly defines that behavior.

A Knowledge Object or Knowledge Record MAY change tags, categories, topics, labels, groups, or collections without changing Object Identity when the underlying knowledge identity remains the same.

Where tags, categories, topics, labels, groups, or collections affect relationship creation, privacy handling, lifecycle state, authority, validation, import, export, migration, publication, or downstream use, the relevant governed metadata SHOULD remain explicit and reviewable.

### 10.8 External Identifier Boundary

A Knowledge Object or Knowledge Record MAY include external identifiers.

External identifiers MAY include identifiers from source systems, external repositories, public standards, datasets, publications, archival systems, imported systems, vendor systems, or third-party services.

External identifiers SHOULD remain distinguishable from Stable Object Identifiers.

An external identifier MUST NOT define internal stable Object Identity unless a future governed specification explicitly defines that relationship.

An external identifier MAY support source traceability, citation, import mapping, export mapping, migration mapping, duplicate detection, relationship resolution, or interoperability.

Where external identifiers are used for interoperability, the metadata SHOULD preserve enough context to determine the identifier source, scope, stability, authority, and relationship to the Knowledge Object.

External identifiers MUST preserve privacy boundaries.

An external identifier MUST NOT expose restricted information merely to improve discovery, citation, import, export, migration, validation, or interoperability.

### 10.9 Temporary Identifier Boundary

A Knowledge Object or Knowledge Record MAY include temporary identifiers during drafting, ingestion, import, export, migration, validation, workflow execution, agent processing, review, or repair.

Temporary identifiers MUST remain distinguishable from Stable Object Identifiers.

A temporary identifier MUST NOT define stable Object Identity unless a governed process explicitly promotes or maps it into stable identity metadata.

Temporary identifiers SHOULD be resolved, removed, archived, mapped, or reviewed before the Knowledge Object or Knowledge Record is treated as complete where the temporary identifier affects identity, relationships, source references, provenance, validation, import, export, migration, compatibility, or downstream use.

Where temporary identifiers are mapped to Stable Object Identifiers, the mapping SHOULD remain traceable when it affects duplicate detection, relationship repair, source-reference repair, import, export, migration, validation, compatibility, or auditability.

### 10.10 Duplicate Detection Metadata

A Knowledge Object or Knowledge Record SHOULD support duplicate detection where duplicate detection affects Object Identity, relationships, provenance, source references, validation, compatibility, import, export, migration, or downstream use.

Duplicate detection metadata MAY include supporting identifiers, source references, content fingerprints, import identifiers, migration identifiers, similarity signals, external identifiers, prior titles, aliases, or review notes.

Duplicate detection metadata MUST NOT create or merge Object Identity automatically unless a governed process explicitly permits that behavior.

A possible duplicate is not the same as an identity match.

A confirmed duplicate SHOULD preserve enough metadata to explain the decision where the decision affects relationships, provenance, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, or downstream use.

### 10.11 Identity Metadata During Import, Export, and Migration

Identity metadata MUST be preserved during import, export, and migration when identity affects interpretation, relationships, provenance, lifecycle state, authority, privacy classification, validation, compatibility, or downstream use.

Import, export, or migration processes MUST NOT replace stable Object Identity with filenames, folder paths, storage locations, application identifiers, database identifiers, workflow identifiers, agent labels, tags, titles, or temporary identifiers unless a governed migration process explicitly maps identity in a valid way.

Where identity metadata is transformed, mapped, deprecated, redirected, repaired, split, merged, or superseded during migration, the process SHOULD preserve enough context for future review.

A migration that loses stable Object Identity MUST NOT be represented as full compatibility.

An export that omits stable Object Identity SHOULD disclose the omission when identity affects reuse, validation, import, interoperability, or downstream interpretation.

### 10.12 Identity Metadata and Relationships

Relationship metadata SHOULD rely on stable Object Identity where relationships affect meaning, provenance, dependency, hierarchy, sequence, evidence, source traceability, lifecycle state, authority, privacy, validation, governance, or downstream use.

A relationship SHOULD NOT rely only on title, filename, folder path, tag, backlink, visual graph state, search result, application state, or agent inference when the relationship affects governed interpretation.

Where supporting identifiers are used to resolve relationships, the metadata SHOULD preserve enough context to determine whether the relationship target is stable, temporary, external, deprecated, redirected, superseded, or ambiguous.

Identity ambiguity in relationships SHOULD be detectable during validation or review.

### 10.13 Identity Metadata and Validation

Validation SHOULD be able to detect identity metadata issues where identity affects interpretation, relationships, provenance, lifecycle state, authority, privacy classification, import, export, migration, compatibility, or downstream use.

Identity metadata issues MAY include:

- missing Stable Object Identifier;
- malformed Stable Object Identifier;
- duplicate Stable Object Identifier;
- conflicting identifiers;
- ambiguous supporting identifiers;
- unresolved temporary identifiers;
- broken redirect identifiers;
- deprecated identifiers without mapping;
- external identifiers without context;
- identity metadata dependent on hidden implementation state;
- relationships that depend on unstable identifiers;
- migration records that lose identity continuity.

KS-0003 does not define exact identity validation tooling.

A future validation specification MAY define exact identity validation fields, states, rules, errors, warnings, repair guidance, and compatibility behavior.

### 10.14 Identity Metadata Success

Identity metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations can determine:

- which Knowledge Object is represented;
- which identifier is stable;
- which identifiers are supporting identifiers;
- which identifiers are temporary;
- which identifiers are external;
- which identifiers are deprecated, redirected, superseded, or legacy;
- whether two records refer to the same Knowledge Object;
- whether a title change affects identity;
- whether a filename change affects identity;
- whether a folder movement affects identity;
- whether a migration preserved identity;
- whether relationships resolve to stable identities;
- whether identity-related metadata requires review;
- whether identity metadata remains valid across implementation replacement.

Identity metadata is successful when it preserves Object Identity without confusing identity with titles, filenames, folder paths, tags, categories, source identifiers, temporary identifiers, external identifiers, database identifiers, application identifiers, workflow identifiers, agent labels, or hidden implementation state.

## 11. Metadata and Relationships

Metadata and relationships are closely connected because relationships require context to remain interpretable, traceable, reviewable, portable, validatable, and useful across implementations.

Relationship metadata describes explicit connections between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, agents, implementations, or other governed entities.

A compliant metadata model SHALL support relationship interpretation without relying only on hidden application state, folder proximity, filename similarity, tag coincidence, backlink behavior, graph visualization, search ranking, user interface state, workflow memory, agent memory, or undocumented implementation assumptions.

Relationship metadata SHOULD make clear:

- what entities are connected;
- what kind of relationship exists;
- what direction applies where direction affects meaning;
- what source or evidence supports the relationship where applicable;
- what provenance applies to the relationship;
- what lifecycle state applies to the relationship where applicable;
- what authority applies to the relationship where applicable;
- what privacy boundaries apply to the relationship;
- what validation expectations apply to the relationship;
- whether the relationship is explicit, inferred, proposed, reviewed, approved, deprecated, superseded, or rejected where applicable.

KS-0003 defines relationship metadata at the conceptual standard level.

KS-0003 does not define exact relationship field names, exact relationship types, exact schemas, exact allowed values, exact serialization formats, exact database columns, exact graph structures, or exact validation tooling.

A future relationship specification MAY define those details.

### 11.1 Relationship Metadata Purpose

Relationship metadata exists to preserve the meaning and context of relationships between governed entities.

Relationship metadata SHOULD support:

- interpretation;
- navigation;
- source traceability;
- provenance;
- dependency tracking;
- hierarchy;
- sequence;
- evidence tracking;
- duplicate detection;
- validation;
- lifecycle handling;
- authority handling;
- privacy handling;
- import behavior;
- export behavior;
- migration behavior;
- compatibility;
- agent review;
- workflow execution;
- downstream use.

A relationship is successful only when future humans, agents, workflows, validators, storage systems, and implementations can determine why the relationship exists and how it should be interpreted.

A relationship MUST NOT be treated as governed merely because two items are near each other, share a tag, share a folder, appear near each other in a graph, appear in the same search result, or were linked by an agent.

### 11.2 Relationship Participants

Relationship metadata SHOULD identify the participants in a relationship.

Relationship participants MAY include:

- Knowledge Objects;
- Knowledge Records;
- Source Material;
- standards;
- specifications;
- decisions;
- workflows;
- agents;
- implementations;
- external references;
- imported records;
- exported records;
- migration records;
- validation records;
- future governed entities.

Relationship participant metadata SHOULD rely on stable Object Identity where relationships affect meaning, provenance, dependency, hierarchy, sequence, evidence, source traceability, lifecycle state, authority, privacy, validation, governance, import, export, migration, compatibility, or downstream use.

Where a relationship participant is identified only by title, filename, folder path, tag, backlink, search result, application state, temporary identifier, or agent inference, the relationship SHOULD be treated as lower-confidence or requiring review when the relationship affects governed interpretation.

### 11.3 Relationship Type Metadata

Relationship metadata SHOULD identify relationship type where type affects meaning.

Relationship type metadata describes the nature of the connection between entities.

Relationship type metadata MAY indicate that one entity:

- references another entity;
- supports another entity;
- contradicts another entity;
- depends on another entity;
- supersedes another entity;
- deprecates another entity;
- replaces another entity;
- derives from another entity;
- summarizes another entity;
- extracts from another entity;
- validates another entity;
- implements another entity;
- governs another entity;
- belongs to another entity;
- contains another entity;
- is part of another entity;
- is related to another entity in a future governed way.

This list is descriptive and does not define a complete approved relationship vocabulary.

A future relationship specification MAY define exact relationship types, relationship classes, allowed values, type constraints, validation rules, and migration behavior.

Relationship type metadata MUST NOT be inferred solely from visual layout, folder placement, tag similarity, backlink existence, graph proximity, or agent suggestion when type affects governed meaning.

### 11.4 Relationship Direction Metadata

Relationship metadata SHOULD preserve direction where direction affects meaning.

Direction metadata identifies whether a relationship is one-way, reciprocal, hierarchical, dependent, sequential, evidentiary, derivative, superseding, deprecating, validating, implementing, or otherwise directional.

A relationship from one entity to another may not mean the same thing when reversed.

For example, a source may support a Knowledge Record, but the Knowledge Record does not support the source in the same way.

A standard may govern an implementation, but the implementation does not govern the standard.

A newer record may supersede an older record, but the older record does not supersede the newer record.

Relationship direction MUST NOT depend only on backlink behavior, graph layout, folder hierarchy, visual position, user interface state, or undocumented implementation behavior when direction affects meaning.

Where direction is ambiguous, the relationship SHOULD require review before it is used for authority, validation, lifecycle, privacy, migration, publication, or downstream automation.

### 11.5 Relationship Strength and Confidence Metadata

Relationship metadata MAY include strength or confidence metadata where confidence affects interpretation, review, validation, automation, authority, publication, migration, or downstream use.

Relationship strength or confidence metadata MAY indicate whether a relationship is confirmed, proposed, inferred, weak, strong, reviewed, unreviewed, disputed, experimental, machine-suggested, human-approved, or requiring review.

This list is descriptive and does not define a complete approved confidence vocabulary.

Relationship confidence MUST remain distinguishable from authority metadata.

A high-confidence relationship is not automatically authoritative.

An authoritative relationship is not automatically private, public, valid, current, or approved for all downstream uses.

Agent-inferred or workflow-inferred relationship metadata SHOULD remain reviewable when it affects interpretation, authority, privacy, lifecycle state, validation, publication, export, migration, or downstream use.

### 11.6 Relationship Provenance Metadata

Relationship metadata SHOULD include provenance where the origin, creator, source, evidence, workflow, agent, import process, migration process, or review state of the relationship affects interpretation, authority, privacy, validation, compatibility, or downstream use.

Relationship provenance metadata MAY identify:

- who created the relationship;
- what agent created or suggested the relationship;
- what workflow created or updated the relationship;
- what source material supports the relationship;
- what import process created the relationship;
- what migration process transformed the relationship;
- what validation process checked the relationship;
- what review process approved or rejected the relationship;
- when the relationship was created or changed where applicable;
- why the relationship exists where applicable.

Relationship provenance MUST preserve privacy boundaries.

Relationship provenance MUST NOT expose restricted source material, restricted actors, restricted relationships, restricted workflows, or restricted content merely to improve traceability.

Where relationship provenance cannot be fully exposed due to privacy restrictions, the metadata SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

### 11.7 Relationship Lifecycle Metadata

Relationship metadata MAY include lifecycle metadata where relationship state affects interpretation, authority, privacy, validation, migration, publication, workflow behavior, or downstream use.

Relationship lifecycle metadata MAY indicate whether a relationship is draft, proposed, reviewed, approved, rejected, deprecated, superseded, archived, experimental, imported, migrated, needs review, needs validation, or governed by a future lifecycle state.

This list is descriptive and does not define a complete approved relationship lifecycle vocabulary.

A relationship MUST NOT be treated as approved merely because it exists, is visible, is linked, appears in a graph, appears in a backlink list, appears in search, was imported, or was generated by an agent.

Relationship lifecycle metadata SHOULD remain distinguishable from Knowledge Object lifecycle metadata.

A Knowledge Object may be approved while one of its relationships remains proposed, disputed, deprecated, or requiring review.

### 11.8 Relationship Authority Metadata

Relationship metadata MAY include authority metadata where relationship authority affects interpretation, governance, publication, validation, automation, or downstream use.

Relationship authority metadata describes how strongly a relationship may be relied on for interpretation, reasoning, workflow execution, validation, publication, or governance.

Relationship authority metadata MUST remain distinguishable from:

- relationship existence;
- relationship confidence;
- relationship popularity;
- relationship visibility;
- relationship validation state;
- relationship lifecycle state;
- relationship source availability;
- relationship usefulness;
- relationship recency.

A relationship may be valid structurally without being authoritative.

A relationship may be high authority but superseded.

A relationship may be useful for discovery without being authoritative for governance.

Relationship authority MUST NOT be assigned automatically by backlink count, graph centrality, search rank, tag frequency, agent certainty, or implementation convenience unless a future governed specification explicitly defines that behavior.

### 11.9 Relationship Privacy Metadata

Relationship metadata MUST preserve privacy boundaries.

A relationship may reveal sensitive knowledge even when the connected objects appear harmless separately.

Relationship privacy metadata SHOULD describe permitted visibility, handling, routing, indexing, synchronization, export, backup, publication, and agent access where the relationship affects privacy.

A relationship MUST NOT expose restricted source material, restricted identity, restricted provenance, restricted authority, restricted lifecycle state, restricted classification, or restricted content merely to improve navigation, discovery, validation, automation, publication, export, or migration.

A relationship involving restricted knowledge SHOULD be handled conservatively when privacy expectations are unclear.

Where a relationship crosses privacy boundaries, the relationship SHOULD require review before publication, export, indexing, synchronization, backup, agent access, or downstream use.

### 11.10 Relationship Validation Metadata

Relationship metadata SHOULD support validation where relationships affect interpretation, provenance, dependency, hierarchy, sequence, evidence, source traceability, lifecycle state, authority, privacy, governance, import, export, migration, compatibility, or downstream use.

Relationship validation MAY detect:

- missing relationship target;
- ambiguous relationship target;
- unstable relationship target;
- invalid relationship type;
- missing relationship direction;
- invalid relationship direction;
- missing relationship provenance;
- relationship privacy risk;
- relationship authority ambiguity;
- relationship lifecycle ambiguity;
- relationship dependent on hidden implementation state;
- relationship dependent on filename, folder path, tag, backlink, graph layout, or search result;
- broken relationship after import, export, or migration;
- relationship incompatible with applicable standards or specifications.

KS-0003 does not define exact relationship validation tooling.

A future relationship validation specification MAY define exact relationship validation fields, states, rules, errors, warnings, repair guidance, compatibility behavior, and migration behavior.

### 11.11 Relationship Metadata During Import, Export, and Migration

Relationship metadata SHOULD be preserved during import, export, and migration where relationships affect meaning, provenance, dependency, hierarchy, sequence, evidence, source traceability, lifecycle state, authority, privacy, validation, governance, compatibility, or downstream use.

Import, export, or migration processes MUST NOT replace governed relationship metadata with folder placement, filename similarity, tag coincidence, backlink existence, graph proximity, application state, or agent inference unless a governed migration process explicitly maps the relationship in a valid way.

Where relationship metadata is transformed, mapped, deprecated, redirected, repaired, split, merged, superseded, or omitted during migration, the process SHOULD preserve enough context for future review.

A migration that loses meaning-critical relationship metadata MUST NOT be represented as full compatibility.

An export that omits meaning-critical relationship metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, or downstream interpretation.

### 11.12 Inferred and Agent-Generated Relationships

Inferred and agent-generated relationships MAY support discovery, review, organization, automation, and knowledge development.

Inferred and agent-generated relationships MUST remain distinguishable from reviewed or approved governed relationships when the distinction affects interpretation, authority, privacy, validation, publication, export, migration, or downstream use.

An inferred relationship is not automatically valid.

An agent-generated relationship is not automatically authoritative.

A workflow-generated relationship is not automatically approved.

A relationship suggested by search, similarity, embeddings, graph analysis, source proximity, title similarity, or tag similarity MUST NOT become governed relationship metadata without appropriate review where review is required.

Where inferred or agent-generated relationships are accepted into governed metadata, the accepted relationship SHOULD preserve enough provenance for future review.

### 11.13 Relationship Metadata Success

Relationship metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations can determine:

- what entities are connected;
- what type of relationship exists;
- what direction applies where applicable;
- what source or evidence supports the relationship where applicable;
- what provenance applies to the relationship;
- what lifecycle state applies to the relationship where applicable;
- what authority applies to the relationship where applicable;
- what privacy boundaries apply to the relationship;
- what validation expectations apply to the relationship;
- whether the relationship is explicit, inferred, proposed, reviewed, approved, deprecated, superseded, rejected, imported, migrated, or experimental where applicable;
- whether the relationship can be used for interpretation, navigation, validation, automation, publication, export, migration, or downstream use;
- whether the relationship remains valid across implementation replacement.

Relationship metadata is successful when relationships remain meaningful, portable, reviewable, privacy-respecting, validatable, and implementation-independent.

## 12. Metadata and Provenance

Metadata and provenance are closely connected because provenance preserves the origin, source, creation context, transformation context, review context, and change history needed for knowledge to remain trustworthy, traceable, reviewable, validatable, and portable across implementations.

Provenance metadata describes where knowledge came from, how it was created, what source material supports it, who or what contributed to it, what workflows or agents affected it, and what transformations, imports, exports, migrations, validations, reviews, or revisions occurred.

A compliant metadata model SHALL support provenance without relying only on hidden application state, folder placement, filename convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, or undocumented implementation assumptions.

Provenance metadata SHOULD help future humans, agents, workflows, validators, storage systems, and implementations determine:

- where the knowledge came from;
- what source material supports the knowledge where applicable;
- who or what created the knowledge;
- who or what modified the knowledge;
- what workflow was involved where applicable;
- what agent was involved where applicable;
- what import process was involved where applicable;
- what export process was involved where applicable;
- what migration process was involved where applicable;
- what transformation occurred where applicable;
- what review occurred where applicable;
- what validation occurred where applicable;
- what evidence supports the record where applicable;
- what interpretation was added where applicable;
- what privacy boundaries apply to provenance;
- whether provenance remains valid across implementation replacement.

KS-0003 defines provenance metadata at the conceptual standard level.

KS-0003 does not define exact provenance field names, exact schemas, exact allowed values, exact serialization formats, exact database columns, exact audit-log structures, exact citation formats, or exact validation tooling.

A future provenance specification MAY define those details.

### 12.1 Provenance Metadata Purpose

Provenance metadata exists to preserve traceability, accountability, reviewability, source distinction, evidence context, workflow context, agent context, transformation context, validation context, migration context, and long-term trust.

Provenance metadata SHOULD support:

- source traceability;
- evidence review;
- authorship context;
- agent involvement review;
- workflow involvement review;
- import traceability;
- export traceability;
- migration traceability;
- transformation traceability;
- revision review;
- validation review;
- authority assessment;
- privacy handling;
- compatibility assessment;
- downstream interpretation.

Provenance metadata MUST distinguish source material from Knowledge Records.

Provenance metadata MUST distinguish evidence from interpretation where that distinction affects meaning, authority, privacy, validation, reviewability, publication, export, migration, or downstream use.

Provenance metadata MUST preserve privacy boundaries.

### 12.2 Source Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include source provenance metadata where source material materially supports the content, interpretation, classification, relationship, decision, validation, authority, or provenance of the record.

Source provenance metadata MAY identify:

- source material;
- source type;
- source origin;
- source creator where applicable;
- source location where permitted;
- source date where applicable;
- source availability;
- source restrictions;
- source reliability concerns;
- source transformation history;
- source extraction context;
- source relationship to the Knowledge Record.

Source provenance metadata SHOULD be sufficient for authorized humans, agents, workflows, validators, storage systems, and implementations to understand how source material supports the record.

Source provenance metadata MUST NOT expose restricted source material merely to improve traceability, validation, discovery, automation, publication, export, or migration.

Where source material is unavailable, moved, deleted, restricted, corrupted, superseded, or replaced, source provenance metadata SHOULD indicate that condition when it affects interpretation, validation, authority, provenance, review, or downstream use.

### 12.3 Creation Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include creation provenance metadata where creation context affects interpretation, reviewability, authority, lifecycle state, privacy, validation, source traceability, compatibility, or downstream use.

Creation provenance metadata MAY identify:

- when the object or record was created;
- who created it where applicable;
- what agent created it where applicable;
- what workflow created it where applicable;
- what source material supported creation where applicable;
- what import process created it where applicable;
- what extraction process created it where applicable;
- what transformation process created it where applicable;
- what initial lifecycle state applied;
- what initial authority context applied;
- what initial privacy classification applied;
- what initial validation expectations applied.

Creation provenance metadata SHOULD remain distinguishable from Object Identity.

The creator of a record does not define the stable identity of the Knowledge Object unless a future governed specification explicitly defines that relationship.

Creation provenance metadata SHOULD remain traceable when creation context affects meaning, authority, privacy, validation, compatibility, or migration.

### 12.4 Revision Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include revision provenance metadata where revision context affects meaning, provenance, privacy, authority, lifecycle state, validation, relationships, source references, compatibility, publication, export, migration, or downstream use.

Revision provenance metadata MAY identify:

- when the object or record was modified;
- who modified it where applicable;
- what agent modified it where applicable;
- what workflow modified it where applicable;
- what changed where applicable;
- why the change occurred where applicable;
- what source material supported the change where applicable;
- whether review occurred;
- whether validation changed;
- whether authority changed;
- whether privacy classification changed;
- whether lifecycle state changed;
- whether relationships changed;
- whether compatibility changed.

KS-0003 does not require a complete change-history model for every Knowledge Object or Knowledge Record.

However, revisions that affect governed meaning SHOULD remain traceable.

A future revision specification MAY define exact revision metadata, version metadata, change records, approval records, review records, and migration behavior.

### 12.5 Agent Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include agent provenance metadata where agent activity affects creation, classification, summarization, extraction, transformation, linking, validation, review preparation, import, export, migration, publication, or downstream use.

Agent provenance metadata MAY identify:

- the agent involved;
- the instruction or task context where appropriate;
- the model class where appropriate;
- the tool used where appropriate;
- the workflow involved where applicable;
- the source material used where applicable;
- the output generated;
- the transformation performed;
- the review state;
- the approval state where applicable;
- limitations or uncertainty where applicable.

Agent provenance metadata SHOULD make agent involvement reviewable where agent activity affects interpretation, relationships, lifecycle state, authority, privacy, validation, publication, export, migration, compatibility, or downstream use.

Agent provenance metadata MUST NOT make an agent an unreviewable authority over knowledge.

Agent-generated content, classifications, relationships, summaries, validations, or transformations SHOULD remain distinguishable from human-authored and approved governed metadata when that distinction affects reviewability, authority, privacy, validation, or downstream use.

### 12.6 Workflow Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include workflow provenance metadata where workflow activity affects creation, transformation, review, approval, validation, import, export, migration, publication, maintenance, or downstream use.

Workflow provenance metadata MAY identify:

- the workflow involved;
- workflow trigger;
- workflow actor;
- workflow state;
- workflow output;
- workflow decision;
- review point;
- approval point;
- failure condition;
- rollback condition;
- source material used;
- agent involvement;
- validation result;
- migration result;
- publication result.

Workflow provenance metadata SHOULD preserve traceability when workflow activity changes metadata, relationships, provenance, lifecycle state, authority, privacy classification, validation state, compatibility, or knowledge meaning.

Workflow completion MUST NOT be treated as approval unless a future governed workflow specification explicitly defines that behavior.

Workflow provenance metadata MUST NOT bypass governance, privacy, lifecycle, authority, validation, review, or compatibility requirements.

### 12.7 Transformation Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include transformation provenance metadata where extraction, summarization, translation, normalization, classification, conversion, mapping, enrichment, compression, redaction, or restructuring affects meaning, provenance, authority, privacy, validation, compatibility, or downstream use.

Transformation provenance metadata MAY identify:

- what transformation occurred;
- what source material or record was transformed;
- who or what performed the transformation;
- what workflow or agent was involved;
- what information was added;
- what information was removed;
- what information was normalized;
- what information was redacted;
- what meaning may have changed;
- what validation occurred after transformation;
- what review is required;
- what compatibility limits exist.

Transformation provenance metadata SHOULD distinguish direct source extraction from interpretation.

A summary is not the same as the source.

A translation is not the same as the source.

A classification is not the same as the source.

A normalized record is not the same as the source unless a future governed specification explicitly defines that equivalence.

Where transformation loses meaning-critical metadata, the loss SHOULD be explicit and reviewable.

### 12.8 Import, Export, and Migration Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include import, export, and migration provenance metadata where movement between systems, formats, repositories, vaults, implementations, or standards versions affects identity, meaning, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, source references, or downstream use.

Import, export, and migration provenance metadata MAY identify:

- source system;
- target system;
- source format;
- target format;
- import date where applicable;
- export date where applicable;
- migration date where applicable;
- migration process;
- conversion process;
- mapping decisions;
- legacy identifiers;
- compatibility notes;
- loss warnings;
- validation results;
- review requirements.

Import, export, and migration provenance metadata SHOULD preserve traceability when movement affects governed meaning.

A migration that loses meaning-critical provenance metadata MUST NOT be represented as full compatibility.

An export that omits meaning-critical provenance metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, review, or downstream interpretation.

### 12.9 Validation Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include validation provenance metadata where validation affects compliance, review, workflow behavior, import, export, migration, publication, interoperability, or implementation replacement.

Validation provenance metadata MAY identify:

- what was validated;
- when validation occurred where applicable;
- what validator was used where applicable;
- what validation profile applied where applicable;
- what rule set applied where applicable;
- what errors were found;
- what warnings were found;
- what metadata was missing;
- what relationships were broken;
- what privacy risks were detected;
- what compatibility issues were detected;
- what review remains required.

Validation provenance metadata SHOULD remain distinguishable from the validated metadata itself.

A validation result MUST NOT silently override explicit metadata, Object Identity, provenance, lifecycle state, authority, privacy classification, relationships, or source references.

A valid structure does not guarantee factual truth, authority, approval, publication readiness, privacy clearance, or lifecycle approval unless a future governed specification explicitly defines that relationship.

### 12.10 Review and Approval Provenance Metadata

A Knowledge Object or Knowledge Record SHOULD include review and approval provenance metadata where review or approval affects lifecycle state, authority, privacy classification, publication, validation, governance, compatibility, or downstream use.

Review and approval provenance metadata MAY identify:

- whether review occurred;
- who reviewed where applicable;
- what agent prepared review where applicable;
- what workflow supported review where applicable;
- what was reviewed;
- what decision was made;
- what approval scope applies;
- what approval limits apply;
- what unresolved issues remain;
- what follow-up review is required;
- what lifecycle state changed;
- what authority changed;
- what privacy classification changed;
- what validation changed.

Review metadata MUST remain distinguishable from approval metadata.

A record may be reviewed without being approved.

A record may be approved for a narrow scope without being authoritative for broader interpretation.

A record may be valid without being approved.

A record may be approved but later superseded, deprecated, restricted, or archived.

### 12.11 Provenance Privacy Metadata

Provenance metadata MUST preserve privacy boundaries.

Provenance may reveal sensitive information even when the knowledge content appears harmless.

Provenance privacy metadata SHOULD describe permitted visibility, handling, routing, indexing, synchronization, export, backup, publication, and agent access where provenance affects privacy.

Provenance metadata MUST NOT expose restricted source material, restricted actors, restricted workflows, restricted relationships, restricted identities, restricted decisions, restricted locations, restricted timestamps, or restricted content merely to improve traceability, discovery, validation, automation, publication, export, or migration.

Where full provenance cannot be exposed due to privacy restrictions, the metadata SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Where provenance usefulness and privacy conflict, privacy SHALL take precedence.

### 12.12 Provenance and Authority

Provenance metadata SHOULD support authority assessment.

Provenance metadata MAY help determine whether a Knowledge Object, Knowledge Record, relationship, source reference, classification, validation result, workflow output, or agent output may be relied on for interpretation, governance, publication, automation, or downstream use.

Provenance metadata MUST remain distinguishable from authority metadata.

A known provenance does not automatically make knowledge authoritative.

An unknown provenance does not automatically make knowledge false.

A source-derived record is not automatically authoritative.

An agent-generated record is not automatically low quality.

A human-authored record is not automatically authoritative.

Authority depends on governance, review, lifecycle state, source context, approval scope, applicable standards, and future authority specifications.

### 12.13 Provenance and Compatibility

Provenance metadata SHOULD support compatibility across standards, specifications, schemas, metadata profiles, storage systems, workflows, agents, validators, and implementations.

Compatibility metadata SHOULD identify when provenance has been preserved, transformed, partially preserved, redacted, omitted, deprecated, superseded, or lost during import, export, migration, or implementation replacement.

A representation that loses meaning-critical provenance metadata MUST NOT be treated as fully compatible.

Where provenance metadata is transformed or mapped, the mapping SHOULD remain reviewable when it affects interpretation, authority, privacy, validation, relationships, lifecycle state, source references, migration, export, import, or downstream use.

A future compatibility specification MAY define exact provenance compatibility states, warnings, migration requirements, validation rules, and repair guidance.

### 12.14 Provenance Metadata Success

Provenance metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations can determine:

- where the knowledge came from;
- what source material supports it where applicable;
- who or what created it;
- who or what modified it;
- what workflow affected it where applicable;
- what agent affected it where applicable;
- what transformation occurred where applicable;
- what import, export, or migration process affected it where applicable;
- what validation occurred where applicable;
- what review or approval occurred where applicable;
- what evidence supports the record where applicable;
- what interpretation was added where applicable;
- what privacy boundaries apply to provenance;
- what authority implications exist;
- what compatibility concerns exist;
- whether provenance remains valid across implementation replacement.

Provenance metadata is successful when knowledge remains traceable, reviewable, privacy-respecting, validatable, portable, compatible, and implementation-independent without exposing restricted information or creating unnecessary metadata burden.

## 13. Metadata and Lifecycle State

Metadata and lifecycle state are closely connected because lifecycle metadata describes the current governed state of a Knowledge Object, Knowledge Record, relationship, source reference, metadata element, workflow output, agent output, validation result, import, export, migration, or other governed entity where state affects interpretation or handling.

Lifecycle metadata helps humans, agents, workflows, validators, storage systems, and implementations determine whether knowledge is draft, under review, approved, rejected, deprecated, superseded, archived, experimental, imported, migrated, needs review, needs validation, or governed by a future lifecycle state.

This list is descriptive and does not define a complete approved lifecycle vocabulary.

A compliant metadata model SHALL support lifecycle interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, graph display, search ranking, or undocumented implementation assumptions.

Lifecycle metadata SHOULD help determine:

- what state applies;
- what the state means;
- what entity the state applies to;
- who or what assigned the state where applicable;
- when the state changed where applicable;
- what review occurred where applicable;
- what approval occurred where applicable;
- what validation occurred where applicable;
- what privacy boundaries apply;
- what authority implications exist;
- what compatibility concerns exist;
- whether the lifecycle state affects publication, export, import, migration, automation, or downstream use.

KS-0003 defines lifecycle metadata at the conceptual standard level.

KS-0003 does not define exact lifecycle field names, exact lifecycle states, exact transition rules, exact schemas, exact allowed values, exact serialization formats, exact database columns, exact workflow states, or exact validation tooling.

A future lifecycle specification MAY define those details.

### 13.1 Lifecycle Metadata Purpose

Lifecycle metadata exists to preserve state clarity, reviewability, governance, validation, privacy handling, authority handling, publication readiness, archival handling, deprecation handling, supersession handling, migration behavior, and downstream use.

Lifecycle metadata SHOULD support:

- drafting;
- review;
- approval;
- rejection;
- supersession;
- deprecation;
- archival;
- publication control;
- validation control;
- privacy handling;
- authority handling;
- workflow routing;
- agent handling;
- import handling;
- export handling;
- migration handling;
- compatibility review;
- downstream interpretation.

Lifecycle metadata MUST remain distinguishable from authority metadata, privacy metadata, validation metadata, provenance metadata, workflow state, implementation state, and user interface state.

A lifecycle state may affect authority, privacy, validation, workflow behavior, publication, export, migration, or downstream use.

A lifecycle state does not automatically define those meanings unless a future governed specification explicitly defines the relationship.

### 13.2 Lifecycle State Scope

Lifecycle metadata SHOULD make clear what entity the lifecycle state applies to.

Lifecycle state MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- a future governed entity.

A Knowledge Object and one of its Knowledge Records MAY have different lifecycle states.

A Knowledge Object may be approved while a specific relationship remains proposed.

A Knowledge Record may be archived while the Knowledge Object remains active.

A source reference may require review while the Knowledge Record remains usable.

An agent output may be unreviewed while the human-approved record is approved.

Lifecycle scope MUST be explicit enough to prevent state confusion where state affects interpretation, authority, privacy, validation, publication, export, migration, or downstream use.

### 13.3 Draft Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have draft lifecycle metadata when it is incomplete, developing, unreviewed, or not yet approved for governed use.

Draft lifecycle metadata SHOULD indicate that the object or record should not be treated as approved merely because it exists, is stored, is indexed, is linked, appears in search, appears in a graph, was imported, or was generated by an agent.

Draft lifecycle metadata MAY support review routing, validation expectations, workflow handling, agent restrictions, publication limits, export limits, and downstream-use limits.

A draft state MUST NOT be treated as approval.

A draft state MUST NOT be treated as high authority unless a future governed specification explicitly defines a narrow exception.

Where draft knowledge is exported, published, indexed, synchronized, migrated, or used by agents, the draft state SHOULD be preserved when it affects interpretation or downstream use.

### 13.4 Review Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have review lifecycle metadata when it is being evaluated for correctness, completeness, privacy, provenance, relationships, authority, validation, compatibility, publication, export, migration, or governance.

Review lifecycle metadata MAY indicate that review is pending, active, blocked, completed, failed, or governed by a future review state.

This list is descriptive and does not define a complete approved review vocabulary.

Review lifecycle metadata SHOULD remain distinguishable from approval metadata.

A record may be under review without being approved.

A record may complete review without being approved if the review identifies unresolved issues.

A review state SHOULD preserve enough provenance to determine what was reviewed, who or what reviewed it where applicable, what workflow or agent supported review where applicable, what decision was made, and what follow-up remains required where applicable.

### 13.5 Approval Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have approval lifecycle metadata when it has been accepted for a defined governed purpose.

Approval lifecycle metadata SHOULD identify approval scope where scope affects interpretation, authority, publication, validation, export, migration, automation, or downstream use.

Approval may be broad or narrow.

A Knowledge Object or Knowledge Record may be approved for internal use but not publication.

A Knowledge Object or Knowledge Record may be approved for a specific workflow but not as a general authority.

A Knowledge Object or Knowledge Record may be approved structurally but still require privacy review before export.

Approval lifecycle metadata MUST remain distinguishable from authority metadata.

Approval does not automatically mean constitutional authority, standard authority, factual truth, public release, privacy clearance, full compatibility, or unrestricted downstream use unless a future governed specification explicitly defines that relationship.

### 13.6 Rejection Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have rejection lifecycle metadata when it is rejected for a defined purpose.

Rejection lifecycle metadata SHOULD indicate the reason for rejection where that reason affects future review, validation, authority, privacy, publication, export, migration, compatibility, or downstream use.

A rejected Knowledge Object or Knowledge Record MAY be retained for evidence, audit, history, duplicate detection, source traceability, compatibility, or governance.

A rejected state MUST NOT silently delete provenance, source references, relationships, review history, validation results, or compatibility context where those remain necessary for future interpretation.

A rejected state SHOULD prevent accidental treatment as approved where approval affects interpretation, publication, export, migration, automation, or downstream use.

### 13.7 Supersession Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have supersession lifecycle metadata when it has been replaced, overridden, or made secondary by a newer or higher-authority object, record, standard, specification, decision, source, or governed entity.

Supersession lifecycle metadata SHOULD identify what supersedes the object or record where identification is permitted and materially affects interpretation.

Supersession metadata SHOULD preserve direction.

An older record may be superseded by a newer record.

The newer record does not become superseded by the older record merely because the relationship exists.

Supersession lifecycle metadata SHOULD remain traceable where supersession affects relationships, authority, validation, privacy, publication, export, migration, compatibility, or downstream use.

A superseded object or record MAY remain accessible for history, evidence, audit, compatibility, or migration.

A superseded object or record MUST NOT be treated as current merely because it remains stored, linked, indexed, visible, or referenced.

### 13.8 Deprecation Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have deprecation lifecycle metadata when it remains available but is discouraged, outdated, replaced, unsafe for new use, or maintained only for compatibility, history, audit, or migration.

Deprecation lifecycle metadata SHOULD indicate why the object or record is deprecated where that reason affects interpretation, validation, authority, privacy, publication, export, migration, or downstream use.

Deprecation metadata SHOULD identify replacement or superseding entities where applicable and permitted.

A deprecated object or record MAY remain valid for historical interpretation while being invalid for new use.

A deprecated object or record MUST NOT be treated as current merely because it remains visible, indexed, linked, imported, exported, or referenced.

Deprecation lifecycle metadata SHOULD be preserved during import, export, and migration where deprecation affects interpretation or compatibility.

### 13.9 Archival Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have archival lifecycle metadata when it is retained for history, evidence, audit, compatibility, migration, preservation, legal, governance, or long-term reference purposes.

Archival lifecycle metadata SHOULD describe whether the object or record remains active, inactive, historical, retained for evidence, retained for compatibility, restricted, preserved, or governed by a future archival state.

This list is descriptive and does not define a complete approved archival vocabulary.

Archival lifecycle metadata SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, and implementations to understand whether the object or record may be used, cited, exported, migrated, published, revised, or only retained.

An archived state MUST NOT erase privacy, authority, provenance, validation, relationship, source-reference, or compatibility requirements.

An archived object or record MAY require restricted handling even when it is no longer active.

### 13.10 Experimental Lifecycle Metadata

A Knowledge Object or Knowledge Record MAY have experimental lifecycle metadata when it is used for testing, prototyping, evaluation, agent behavior exploration, workflow development, metadata experimentation, relationship experimentation, validation experimentation, or implementation experimentation.

Experimental lifecycle metadata MUST remain distinguishable from approved lifecycle states.

Experimental knowledge MUST NOT be treated as approved, authoritative, stable, publication-ready, export-ready, migration-ready, or fully compatible merely because it exists in a compliant repository.

Experimental lifecycle metadata SHOULD make clear when review, validation, privacy review, authority review, compatibility review, or governance approval is required before downstream use.

If experimental knowledge becomes durable and broadly useful, it MAY be promoted through the appropriate governance process.

### 13.11 Lifecycle Metadata and Workflows

Lifecycle metadata MAY be created or updated by governed workflows.

A workflow MAY route objects or records through drafting, review, approval, rejection, deprecation, supersession, archival, validation, publication, export, migration, or future lifecycle states.

Workflow state MUST remain distinguishable from lifecycle metadata.

Workflow completion MUST NOT be treated as lifecycle approval unless a future governed workflow specification explicitly defines that behavior.

Where a workflow changes lifecycle metadata, the change SHOULD remain traceable to the workflow, triggering event, responsible actor, agent involvement where applicable, source material where applicable, validation result where applicable, review state, and approval state.

Workflow-generated lifecycle metadata SHOULD remain reviewable where it affects interpretation, authority, privacy, validation, publication, export, migration, compatibility, or downstream use.

### 13.12 Lifecycle Metadata and Agents

Agent activity MAY propose, prepare, classify, or update lifecycle metadata where permitted by a governed workflow or specification.

Agent-generated lifecycle metadata MUST remain distinguishable from human-approved or governance-approved lifecycle metadata when that distinction affects interpretation, authority, privacy, validation, publication, export, migration, compatibility, or downstream use.

An agent MUST NOT silently approve, reject, supersede, deprecate, archive, publish, export, migrate, or validate a Knowledge Object or Knowledge Record unless a governed workflow explicitly permits that behavior.

Agent-generated lifecycle suggestions SHOULD preserve enough provenance for future review.

Where agent lifecycle metadata is accepted into governed metadata, the accepted metadata SHOULD preserve enough context to determine what was proposed, what was accepted, what was rejected, what was revised, and what review or approval occurred.

### 13.13 Lifecycle Metadata and Privacy

Lifecycle metadata MUST preserve privacy boundaries.

Lifecycle state may reveal sensitive information even when the knowledge content appears harmless.

Lifecycle metadata SHOULD describe permitted visibility, handling, routing, indexing, synchronization, export, backup, publication, and agent access where lifecycle state affects privacy.

A lifecycle state MUST NOT expose restricted source material, restricted actors, restricted workflows, restricted relationships, restricted decisions, restricted identities, restricted timestamps, or restricted content merely to improve review, validation, discovery, automation, publication, export, or migration.

Where lifecycle usefulness and privacy conflict, privacy SHALL take precedence.

### 13.14 Lifecycle Metadata and Validation

Lifecycle metadata SHOULD support validation where lifecycle state affects compliance, review, workflow behavior, import, export, migration, publication, interoperability, or implementation replacement.

Lifecycle validation MAY detect:

- missing lifecycle state where required;
- ambiguous lifecycle state;
- invalid lifecycle state;
- unsupported lifecycle state;
- lifecycle state dependent on hidden implementation state;
- lifecycle state conflicting with authority metadata;
- lifecycle state conflicting with privacy metadata;
- lifecycle state conflicting with validation metadata;
- lifecycle state conflicting with provenance metadata;
- lifecycle state conflicting with publication metadata;
- lifecycle state lost during import, export, or migration;
- deprecated or superseded records presented as current;
- draft or unreviewed records presented as approved.

KS-0003 does not define exact lifecycle validation tooling.

A future lifecycle validation specification MAY define exact lifecycle validation fields, states, rules, errors, warnings, repair guidance, compatibility behavior, and migration behavior.

### 13.15 Lifecycle Metadata During Import, Export, and Migration

Lifecycle metadata SHOULD be preserved during import, export, and migration where lifecycle state affects interpretation, provenance, relationships, authority, privacy, validation, governance, compatibility, publication, archival handling, or downstream use.

Import, export, or migration processes MUST NOT replace governed lifecycle metadata with folder placement, filename convention, tag convention, application state, workflow state, user interface state, or agent inference unless a governed migration process explicitly maps lifecycle state in a valid way.

Where lifecycle metadata is transformed, mapped, deprecated, redirected, repaired, superseded, archived, or omitted during migration, the process SHOULD preserve enough context for future review.

A migration that loses meaning-critical lifecycle metadata MUST NOT be represented as full compatibility.

An export that omits meaning-critical lifecycle metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, publication, archival handling, or downstream interpretation.

### 13.16 Lifecycle Metadata Success

Lifecycle metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations can determine:

- what lifecycle state applies;
- what entity the lifecycle state applies to;
- what the lifecycle state means;
- whether the object or record is draft, under review, approved, rejected, superseded, deprecated, archived, experimental, imported, migrated, needs review, needs validation, or governed by a future lifecycle state;
- whether the lifecycle state affects authority;
- whether the lifecycle state affects privacy;
- whether the lifecycle state affects validation;
- whether the lifecycle state affects provenance;
- whether the lifecycle state affects relationships;
- whether the lifecycle state affects publication;
- whether the lifecycle state affects import, export, or migration;
- whether the lifecycle state affects downstream use;
- whether the lifecycle state remains valid across implementation replacement.

Lifecycle metadata is successful when governed state remains explicit, portable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent without being confused with authority, privacy, validation, workflow state, implementation state, or user interface state.

## 14. Metadata and Authority

Metadata and authority are closely connected because authority metadata helps humans, agents, workflows, validators, storage systems, and implementations determine how strongly a Knowledge Object, Knowledge Record, relationship, source reference, standard, specification, decision, workflow output, agent output, validation result, import, export, migration, or other governed entity may be relied on for interpretation, governance, publication, automation, or downstream use.

Authority metadata describes governance weight, review status, approval scope, interpretive authority, reliance level, or trust context assigned to a governed entity.

Authority metadata MUST remain distinguishable from factual truth, popularity, usefulness, confidence, validation state, lifecycle state, privacy classification, source reliability, search ranking, graph centrality, recency, agent certainty, implementation convenience, or frequency of use.

A compliant metadata model SHALL support authority interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, graph display, search ranking, backlink count, or undocumented implementation assumptions.

Authority metadata SHOULD help determine:

- what authority applies;
- what entity the authority applies to;
- what authority scope applies;
- what governance source assigned the authority where applicable;
- what review or approval supports the authority where applicable;
- what lifecycle state affects the authority;
- what privacy boundaries affect authority visibility or use;
- what validation expectations affect reliance;
- what provenance supports authority assessment;
- whether the authority is current, superseded, deprecated, restricted, provisional, experimental, or requiring review;
- whether the authority affects publication, export, import, migration, automation, or downstream use.

KS-0003 defines authority metadata at the conceptual standard level.

KS-0003 does not define exact authority field names, exact authority levels, exact authority vocabularies, exact schemas, exact allowed values, exact inheritance rules, exact serialization formats, exact database columns, exact workflow states, or exact validation tooling.

A future authority specification MAY define those details.

### 14.1 Authority Metadata Purpose

Authority metadata exists to preserve governance clarity, interpretive reliability, reviewability, approval scope, reliance boundaries, publication control, automation safety, validation support, compatibility, and long-term maintainability.

Authority metadata SHOULD support:

- governance interpretation;
- standard interpretation;
- specification interpretation;
- review decisions;
- approval decisions;
- publication decisions;
- automation decisions;
- agent handling;
- workflow routing;
- validation expectations;
- privacy handling;
- import handling;
- export handling;
- migration handling;
- compatibility review;
- downstream reliance.

Authority metadata MUST help prevent low-authority, draft, experimental, deprecated, superseded, private, unreviewed, or agent-generated knowledge from being mistaken for approved governing knowledge.

Authority metadata MUST remain distinguishable from lifecycle metadata, privacy metadata, validation metadata, provenance metadata, source reliability metadata, workflow state, implementation state, and user interface state.

### 14.2 Authority Scope

Authority metadata SHOULD make clear what scope the authority applies to.

Authority scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a standard;
- a specification;
- a decision;
- a workflow output;
- an agent output;
- a validation result;
- an import record;
- an export record;
- a migration record;
- a publication record;
- a future governed entity.

Authority may be broad or narrow.

A Knowledge Record may be authoritative for one purpose but not another.

A source-derived record may be useful as evidence without being authoritative as interpretation.

A workflow output may be authoritative for routing without being authoritative for knowledge meaning.

An agent output may be useful for review preparation without being authoritative.

Authority scope MUST be explicit enough to prevent authority confusion where authority affects interpretation, governance, privacy, validation, publication, export, migration, automation, or downstream use.

### 14.3 Constitutional Authority Metadata

Constitutional authority metadata MAY identify documents, decisions, or governed entities that have constitutional authority within The Brain Standard.

Constitutional authority applies to foundational meaning, architectural principles, governance constraints, and interpretation rules established by constitutional documents.

Constitutional authority metadata MUST remain distinguishable from standard authority, specification authority, operational authority, workflow authority, implementation authority, source authority, and agent output.

A document, record, source, workflow, implementation, or agent output MUST NOT be treated as constitutional merely because it is important, frequently referenced, highly connected, approved, or useful.

Only governed documents or decisions assigned constitutional authority through the appropriate governance process SHALL carry constitutional authority.

Where lower-authority metadata conflicts with constitutional authority, constitutional authority SHALL take precedence unless the constitutional document is formally revised through governance.

### 14.4 Standard Authority Metadata

Standard authority metadata MAY identify documents, Knowledge Objects, Knowledge Records, specifications, decisions, or governed entities that have standard-level authority within The Brain Standard.

Standard authority supports stable interpretation of approved standard-level rules.

Standard authority metadata MUST remain distinguishable from constitutional authority and implementation-specific behavior.

A standard-level document MUST NOT override constitutional documents.

A standard-level document MAY govern future specifications, implementation profiles, workflows, validation profiles, and operational procedures within its scope.

A Knowledge Object, Knowledge Record, relationship, metadata element, workflow, or implementation MUST NOT be treated as standard authority merely because it follows a common pattern, appears in a template, was generated by an agent, or is used frequently.

Standard authority MUST be assigned through governance.

### 14.5 Specification Authority Metadata

Specification authority metadata MAY identify future specifications that define exact fields, schemas, allowed values, validation rules, lifecycle states, authority levels, privacy classes, relationship types, provenance fields, compatibility states, serialization formats, implementation profiles, or operational rules.

Specification authority MUST remain subordinate to constitutional documents and applicable standards.

A specification MAY define narrower rules within its governed scope.

A specification MUST NOT override KS-0003 unless KS-0003 is formally revised through governance or the specification is explicitly authorized to define narrower implementation details consistent with KS-0003.

Specification authority metadata SHOULD preserve enough context to determine:

- what specification applies;
- what version applies;
- what scope applies;
- what entities are governed;
- what validation expectations apply;
- what compatibility expectations apply;
- whether the specification has been superseded, deprecated, or replaced.

### 14.6 Operational Authority Metadata

Operational authority metadata MAY identify operational documents, workflows, procedures, templates, profiles, or implementation instructions that govern day-to-day handling within a defined scope.

Operational authority MAY support routing, maintenance, review, publication, import, export, migration, validation, backup, synchronization, indexing, or implementation behavior.

Operational authority MUST remain subordinate to constitutional documents, standards, and applicable specifications.

Operational authority MUST NOT redefine Knowledge Object meaning, Object Identity, required metadata, privacy classification, lifecycle state, relationship meaning, provenance requirements, validation expectations, or compatibility expectations unless a higher-authority document explicitly permits that behavior.

Operational authority metadata SHOULD make scope explicit so that operational convenience does not become architecture by accident.

### 14.7 Source Authority Metadata

Source authority metadata MAY describe how strongly source material may be relied on as evidence, context, origin, or support for a Knowledge Record.

Source authority metadata MUST remain distinguishable from source reliability metadata, source availability metadata, provenance metadata, lifecycle metadata, validation metadata, and Knowledge Record authority.

A source may be reliable but not authoritative for a specific interpretation.

A source may be authoritative for one domain but not another.

A source may be unavailable but still historically important.

A source may be restricted even when highly authoritative.

A source-derived record MUST NOT become authoritative merely because it references a source.

Where source authority affects interpretation, publication, validation, governance, export, migration, or downstream use, the authority scope SHOULD be explicit and reviewable.

### 14.8 Human Review Authority Metadata

Human review authority metadata MAY identify human review, editorial review, governance review, privacy review, technical review, validation review, or approval review that affects authority.

Human review authority metadata SHOULD identify review scope where scope affects interpretation, publication, export, migration, validation, governance, automation, or downstream use.

A human-reviewed record is not automatically approved.

A human-approved record is not automatically constitutional.

A human-authored record is not automatically authoritative.

A human decision may be authoritative only within the scope granted by governance.

Human review authority metadata SHOULD preserve enough provenance to determine what was reviewed, who reviewed where applicable, what decision was made, what scope applies, what limitations remain, and what follow-up review is required where applicable.

### 14.9 Agent Authority Boundary

Agent output MUST NOT be treated as authoritative merely because an agent generated it.

Agent authority metadata MAY describe whether an agent output is proposed, reviewed, accepted, rejected, revised, approved for a narrow purpose, or incorporated into governed metadata.

Agent-generated summaries, classifications, relationships, validations, transformations, imports, exports, migrations, or recommendations MUST remain distinguishable from human-approved or governance-approved authority when that distinction affects interpretation, privacy, validation, publication, export, migration, automation, or downstream use.

An agent MAY assist authority assessment.

An agent MUST NOT silently assign constitutional authority, standard authority, specification authority, approval authority, privacy clearance, publication readiness, or unrestricted downstream authority unless a governed workflow explicitly permits that behavior.

Where agent-generated metadata is accepted into governed authority metadata, the accepted metadata SHOULD preserve enough provenance for future review.

### 14.10 Authority and Lifecycle State

Authority metadata MUST remain distinguishable from lifecycle metadata.

Lifecycle state describes governed status.

Authority metadata describes reliance weight, governance weight, approval scope, or interpretive authority.

A Knowledge Object or Knowledge Record may be approved but low authority.

A Knowledge Object or Knowledge Record may be high authority but superseded.

A Knowledge Object or Knowledge Record may be archived but still authoritative for historical interpretation.

A Knowledge Object or Knowledge Record may be draft and therefore not authoritative for governed use.

A lifecycle transition MAY affect authority.

A lifecycle transition MUST NOT silently redefine authority unless a future governed lifecycle or authority specification explicitly defines that relationship.

Where lifecycle state affects authority, the relationship SHOULD be explicit and reviewable.

### 14.11 Authority and Validation

Authority metadata MUST remain distinguishable from validation metadata.

Validation describes whether applicable structure, metadata, provenance, relationships, lifecycle state, privacy classification, compatibility, or implementation expectations have been satisfied.

Authority describes how strongly the entity may be relied on for interpretation, governance, publication, automation, or downstream use.

A valid record is not automatically authoritative.

An authoritative record may still require validation.

A validation result MUST NOT silently assign authority unless a future governed validation or authority specification explicitly defines that behavior.

Where validation affects authority, the relationship SHOULD be explicit and reviewable.

Validation metadata SHOULD help detect authority issues where authority affects interpretation, governance, publication, export, migration, automation, or downstream use.

### 14.12 Authority and Privacy

Authority metadata MUST preserve privacy boundaries.

Authority state may reveal sensitive information even when the knowledge content appears harmless.

Authority metadata SHOULD describe permitted visibility, handling, routing, indexing, synchronization, export, backup, publication, and agent access where authority affects privacy.

Authority metadata MUST NOT expose restricted source material, restricted actors, restricted workflows, restricted relationships, restricted decisions, restricted identities, restricted timestamps, or restricted content merely to improve governance, discovery, validation, automation, publication, export, or migration.

High authority does not override privacy.

Public usefulness does not override privacy.

Publication readiness does not override privacy.

Where authority usefulness and privacy conflict, privacy SHALL take precedence.

### 14.13 Authority and Compatibility

Authority metadata SHOULD support compatibility across standards, specifications, schemas, metadata profiles, storage systems, workflows, agents, validators, and implementations.

Compatibility metadata SHOULD identify when authority metadata has been preserved, transformed, partially preserved, redacted, omitted, deprecated, superseded, or lost during import, export, migration, or implementation replacement.

A representation that loses meaning-critical authority metadata MUST NOT be treated as fully compatible.

Where authority metadata is transformed or mapped, the mapping SHOULD remain reviewable when it affects interpretation, governance, privacy, validation, relationships, lifecycle state, provenance, source references, publication, export, import, migration, automation, or downstream use.

A future compatibility specification MAY define exact authority compatibility states, warnings, migration requirements, validation rules, and repair guidance.

### 14.14 Authority Metadata During Import, Export, and Migration

Authority metadata SHOULD be preserved during import, export, and migration where authority affects interpretation, provenance, relationships, lifecycle state, privacy, validation, governance, compatibility, publication, archival handling, automation, or downstream use.

Import, export, or migration processes MUST NOT replace governed authority metadata with folder placement, filename convention, tag convention, application state, workflow state, user interface state, backlink count, graph centrality, search ranking, or agent inference unless a governed migration process explicitly maps authority in a valid way.

Where authority metadata is transformed, mapped, deprecated, redirected, repaired, superseded, archived, redacted, or omitted during migration, the process SHOULD preserve enough context for future review.

A migration that loses meaning-critical authority metadata MUST NOT be represented as full compatibility.

An export that omits meaning-critical authority metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, publication, governance, automation, or downstream interpretation.

### 14.15 Authority Validation Metadata

Authority metadata SHOULD support validation where authority affects compliance, review, workflow behavior, governance, publication, import, export, migration, interoperability, automation, or implementation replacement.

Authority validation MAY detect:

- missing authority metadata where required;
- ambiguous authority scope;
- invalid authority level;
- unsupported authority value;
- authority dependent on hidden implementation state;
- authority conflicting with lifecycle metadata;
- authority conflicting with privacy metadata;
- authority conflicting with validation metadata;
- authority conflicting with provenance metadata;
- deprecated or superseded records presented as current authority;
- draft or unreviewed records presented as authoritative;
- agent-generated output presented as authoritative without review;
- lower-authority metadata conflicting with higher-authority standards;
- authority metadata lost during import, export, or migration.

KS-0003 does not define exact authority validation tooling.

A future authority validation specification MAY define exact authority validation fields, states, rules, errors, warnings, repair guidance, compatibility behavior, and migration behavior.

### 14.16 Authority Metadata Success

Authority metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations can determine:

- what authority applies;
- what entity the authority applies to;
- what authority scope applies;
- what governance source assigned the authority where applicable;
- whether the authority is constitutional, standard-level, specification-level, operational, source-derived, reviewed, approved, provisional, deprecated, superseded, restricted, experimental, or governed by a future authority state;
- whether the authority affects interpretation;
- whether the authority affects governance;
- whether the authority affects privacy;
- whether the authority affects validation;
- whether the authority affects provenance;
- whether the authority affects relationships;
- whether the authority affects lifecycle state;
- whether the authority affects publication;
- whether the authority affects import, export, or migration;
- whether the authority affects automation or downstream use;
- whether the authority remains valid across implementation replacement.

Authority metadata is successful when governance weight, reliance scope, review status, and interpretive authority remain explicit, portable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent without being confused with truth, popularity, usefulness, confidence, lifecycle state, validation state, privacy classification, source reliability, agent certainty, workflow state, implementation state, or user interface state.

## 15. Metadata and Privacy Classification

Metadata and privacy classification are closely connected because privacy metadata describes how Knowledge Objects, Knowledge Records, relationships, source references, provenance, lifecycle states, authority metadata, validation results, workflow outputs, agent outputs, imports, exports, migrations, publications, indexes, backups, and other governed entities may be accessed, handled, exposed, routed, synchronized, published, exported, backed up, indexed, or processed.

Privacy classification protects knowledge from accidental exposure, inappropriate access, unsafe automation, improper publication, unauthorized export, uncontrolled indexing, unsafe synchronization, or unrestricted agent use.

A compliant metadata model SHALL support privacy interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, access-control assumptions, graph display, search ranking, or undocumented implementation behavior.

Privacy metadata SHOULD help determine:

- what privacy classification applies;
- what entity the privacy classification applies to;
- what access is permitted;
- what visibility is permitted;
- what handling restrictions apply;
- what publication restrictions apply;
- what export restrictions apply;
- what indexing restrictions apply;
- what synchronization restrictions apply;
- what backup restrictions apply;
- what agent access restrictions apply;
- what workflow restrictions apply;
- what downstream-use restrictions apply;
- whether the privacy classification affects relationships, provenance, lifecycle state, authority, validation, compatibility, import, export, migration, or publication.

Privacy classification SHALL take precedence over operational convenience when privacy and convenience conflict.

KS-0003 defines privacy metadata at the conceptual standard level.

KS-0003 does not define exact privacy field names, exact privacy classes, exact access-control rules, exact redaction rules, exact inheritance rules, exact schemas, exact allowed values, exact serialization formats, exact database columns, exact workflow states, or exact validation tooling.

A future privacy specification MAY define those details.

### 15.1 Privacy Metadata Purpose

Privacy metadata exists to preserve confidentiality, access clarity, handling control, disclosure prevention, publication safety, export safety, indexing safety, synchronization safety, backup safety, agent safety, workflow safety, and downstream-use control.

Privacy metadata SHOULD support:

- access control;
- visibility control;
- publication review;
- export review;
- import review;
- migration review;
- synchronization control;
- indexing control;
- backup control;
- agent access control;
- workflow routing;
- validation expectations;
- authority handling;
- provenance handling;
- relationship handling;
- compatibility review;
- downstream-use restrictions.

Privacy metadata MUST prevent restricted knowledge from being treated as unrestricted merely because it is stored, indexed, linked, summarized, exported, backed up, synchronized, migrated, displayed, or processed by an agent.

Privacy metadata MUST remain distinguishable from authority metadata, lifecycle metadata, validation metadata, provenance metadata, workflow state, implementation state, and user interface state.

### 15.2 Privacy Classification Scope

Privacy metadata SHOULD make clear what entity the privacy classification applies to.

Privacy classification MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- an index;
- an embedding;
- a backup;
- a synchronized copy;
- a future governed entity.

A Knowledge Object and one of its Knowledge Records MAY have different privacy classifications.

A relationship may require stronger privacy handling than either connected object appears to require separately.

A provenance element may require restricted handling even when the main knowledge content is less restricted.

A source reference may reveal restricted information even when the Knowledge Record is safe to view.

Privacy scope MUST be explicit enough to prevent privacy confusion where privacy affects access, routing, indexing, synchronization, backup, publication, export, migration, automation, agent access, or downstream use.

### 15.3 Privacy Classification Levels

Privacy metadata MAY indicate that knowledge is public, internal, private, restricted, confidential, sensitive, personal, exportable, non-exportable, agent-readable, agent-restricted, or governed by a future privacy classification.

This list is descriptive and does not define a complete approved privacy vocabulary.

A future privacy specification MAY define exact privacy classes, access rules, handling expectations, inheritance behavior, redaction rules, export rules, publication rules, synchronization rules, indexing rules, backup rules, agent access rules, validation rules, and migration behavior.

Privacy classification SHOULD be explicit where privacy affects handling.

Privacy classification MUST NOT depend only on folder placement, filename, tag, color, user interface state, plugin field, search ranking, workflow memory, agent memory, or hidden implementation state.

Where privacy classification is missing, ambiguous, unsupported, conflicting, or inherited from uncertain context, privacy-sensitive knowledge SHOULD be handled conservatively until review resolves the classification.

### 15.4 Public Privacy Metadata

A Knowledge Object or Knowledge Record MAY have public privacy metadata when it is approved or permitted for unrestricted or broadly visible use within the defined publication or access scope.

Public privacy metadata SHOULD remain distinguishable from publication readiness.

Public visibility does not automatically mean approved content.

Public visibility does not automatically mean high authority.

Public visibility does not automatically mean full compatibility.

Public visibility does not automatically mean unrestricted export, indexing, synchronization, backup, transformation, or agent use unless a future governed privacy specification explicitly defines that relationship.

A public privacy classification MUST NOT override lifecycle state, authority limits, source restrictions, validation expectations, provenance restrictions, relationship restrictions, or governance requirements.

Where public knowledge depends on restricted source material, restricted provenance, restricted relationships, or restricted review context, privacy metadata SHOULD preserve boundaries between public content and restricted supporting context.

### 15.5 Internal Privacy Metadata

A Knowledge Object or Knowledge Record MAY have internal privacy metadata when it is intended for use within a defined internal scope but not necessarily for public release.

Internal privacy metadata SHOULD indicate the relevant internal scope where scope affects access, publication, export, synchronization, indexing, backup, agent access, or downstream use.

Internal knowledge MUST NOT be treated as public merely because it appears in search results, graph views, dashboards, summaries, exports, backups, indexes, or agent-readable contexts.

Internal privacy metadata SHOULD remain distinguishable from authority metadata.

Internal knowledge may be high authority, low authority, draft, approved, deprecated, or experimental.

Internal status describes visibility and handling, not authority by itself.

### 15.6 Private Privacy Metadata

A Knowledge Object or Knowledge Record MAY have private privacy metadata when it is intended for limited access by a specific person, owner, role, workflow, or governed access group.

Private privacy metadata SHOULD indicate permitted access scope where scope affects handling.

Private knowledge MUST NOT be exposed through publication, broad export, unrestricted synchronization, shared indexes, unrestricted backups, search summaries, graph views, embeddings, agent output, workflow logs, or derived metadata unless a governed process explicitly permits that exposure.

Private privacy metadata MUST remain distinguishable from personal preference metadata.

A personal note may be private.

A private record may or may not be personal.

A private classification describes access and handling expectations.

Private privacy metadata SHOULD be preserved during import, export, migration, backup, synchronization, indexing, and implementation replacement where privacy affects downstream handling.

### 15.7 Restricted and Confidential Privacy Metadata

A Knowledge Object or Knowledge Record MAY have restricted or confidential privacy metadata when exposure would create governance, personal, operational, security, legal, contractual, ethical, reputational, or other material risk.

Restricted or confidential privacy metadata SHOULD require conservative handling where classification details are incomplete.

Restricted or confidential knowledge MUST NOT be exposed merely to improve search, navigation, summarization, validation, linking, provenance traceability, authority assessment, publication, export, backup, indexing, synchronization, migration, automation, or implementation convenience.

Restricted or confidential privacy metadata SHOULD control or restrict:

- publication;
- export;
- indexing;
- synchronization;
- backup;
- agent access;
- workflow routing;
- derived metadata creation;
- relationship exposure;
- provenance exposure;
- source-reference exposure;
- validation output exposure;
- migration output exposure;
- downstream use.

Restricted or confidential privacy metadata SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

### 15.8 Sensitive and Personal Privacy Metadata

A Knowledge Object or Knowledge Record MAY have sensitive or personal privacy metadata when the knowledge contains or reveals information about a person, identity, preference, behavior, relationship, location, communication, decision, health, finances, credentials, security posture, or other personal context requiring careful handling.

This list is descriptive and does not define a complete privacy taxonomy.

Sensitive or personal privacy metadata SHOULD be handled conservatively where exposure risk is unclear.

Sensitive or personal knowledge MUST NOT be exposed merely because it improves personalization, search, summarization, relationship discovery, provenance review, validation, automation, publication, export, indexing, synchronization, backup, migration, or agent usefulness.

Sensitive or personal privacy metadata SHOULD support redaction, minimization, review, restricted access, and downstream-use limits where applicable.

Where personal knowledge is used to improve agent behavior or workflow behavior, the applicable privacy metadata SHOULD remain explicit and reviewable.

### 15.9 Privacy Metadata and Relationships

Relationship metadata MUST preserve privacy boundaries.

A relationship may reveal restricted knowledge even when the connected entities appear less restricted separately.

A relationship involving restricted, confidential, sensitive, or personal knowledge SHOULD be handled according to the most restrictive applicable privacy classification unless a future governed privacy specification defines a different rule.

A relationship MUST NOT expose restricted source material, restricted identity, restricted provenance, restricted authority, restricted lifecycle state, restricted classification, restricted content, or restricted association merely to improve navigation, discovery, validation, automation, publication, export, migration, or downstream use.

Where relationship privacy is ambiguous, the relationship SHOULD require review before publication, export, indexing, synchronization, backup, agent access, migration, or downstream use.

### 15.10 Privacy Metadata and Provenance

Provenance metadata MUST preserve privacy boundaries.

Provenance may reveal restricted actors, restricted sources, restricted workflows, restricted decisions, restricted timestamps, restricted locations, restricted relationships, restricted identities, or restricted context even when the main knowledge content appears less restricted.

Provenance involving restricted, confidential, sensitive, or personal knowledge SHOULD be handled according to the most restrictive applicable privacy classification unless a future governed privacy specification defines a different rule.

Provenance metadata MUST NOT expose restricted information merely to improve traceability, discovery, validation, authority assessment, automation, publication, export, migration, or downstream use.

Where full provenance cannot be exposed due to privacy restrictions, metadata SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

### 15.11 Privacy Metadata and Authority

Authority metadata MUST preserve privacy boundaries.

High authority does not override privacy.

Public usefulness does not override privacy.

Publication readiness does not override privacy.

A highly authoritative Knowledge Object or Knowledge Record may remain restricted, confidential, sensitive, or personal.

Authority metadata involving restricted information SHOULD be handled according to applicable privacy classification.

Authority metadata MUST NOT expose restricted decisions, reviewers, sources, workflows, identities, timestamps, classifications, or governance context merely to improve interpretive reliability, governance clarity, validation, publication, export, migration, automation, or downstream use.

Where authority usefulness and privacy conflict, privacy SHALL take precedence.

### 15.12 Privacy Metadata and Lifecycle State

Lifecycle metadata MUST preserve privacy boundaries.

Lifecycle state may reveal restricted information about review, rejection, approval, deprecation, supersession, archival, publication, export, migration, or governance decisions.

Lifecycle metadata involving restricted, confidential, sensitive, or personal knowledge SHOULD be handled according to applicable privacy classification.

A lifecycle state MUST NOT expose restricted source material, restricted actors, restricted workflows, restricted relationships, restricted decisions, restricted identities, restricted timestamps, or restricted content merely to improve review, validation, discovery, automation, publication, export, migration, or downstream use.

Where lifecycle usefulness and privacy conflict, privacy SHALL take precedence.

### 15.13 Privacy Metadata and Validation

Privacy metadata SHOULD support validation where privacy affects access, routing, indexing, synchronization, backup, publication, export, migration, automation, agent access, or downstream use.

Privacy validation MAY detect:

- missing privacy classification where required;
- ambiguous privacy classification;
- unsupported privacy classification;
- conflicting privacy classifications;
- privacy metadata dependent on hidden implementation state;
- restricted knowledge in public metadata;
- restricted source references exposed improperly;
- restricted provenance exposed improperly;
- restricted relationships exposed improperly;
- restricted authority metadata exposed improperly;
- restricted lifecycle metadata exposed improperly;
- restricted validation output exposed improperly;
- agent-readable metadata that should be agent-restricted;
- exportable metadata that should be non-exportable;
- indexable metadata that should be non-indexable;
- privacy metadata lost during import, export, migration, backup, synchronization, or implementation replacement.

KS-0003 does not define exact privacy validation tooling.

A future privacy validation specification MAY define exact privacy validation fields, states, rules, errors, warnings, repair guidance, compatibility behavior, and migration behavior.

### 15.14 Privacy Metadata During Import, Export, and Migration

Privacy metadata MUST be preserved during import, export, and migration where privacy affects interpretation, handling, access, indexing, synchronization, backup, publication, archival handling, validation, governance, compatibility, automation, agent access, or downstream use.

Import, export, or migration processes MUST NOT replace governed privacy metadata with folder placement, filename convention, tag convention, color convention, application state, workflow state, user interface state, access-control assumption, or agent inference unless a governed migration process explicitly maps privacy in a valid way.

Where privacy metadata is transformed, mapped, redacted, omitted, deprecated, restricted, repaired, inherited, or partially preserved during migration, the process SHOULD preserve enough context for authorized future review.

A migration that loses meaning-critical privacy metadata MUST NOT be represented as full compatibility.

An export that omits meaning-critical privacy metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, publication, governance, automation, agent access, or downstream interpretation.

### 15.15 Privacy Metadata and Agents

Agent access MUST respect privacy metadata.

Agent-readable status MUST remain distinguishable from general accessibility.

A Knowledge Object or Knowledge Record may be visible to a human but restricted from agent processing.

A Knowledge Object or Knowledge Record may be available to a workflow but not available to all agents.

An agent MUST NOT access, summarize, classify, embed, export, publish, migrate, infer relationships from, or generate derived metadata from restricted knowledge unless permitted by applicable privacy metadata and governed workflow rules.

Agent-generated metadata MUST preserve privacy boundaries.

An agent output MUST NOT expose restricted source material, restricted provenance, restricted relationships, restricted authority, restricted lifecycle state, restricted validation details, restricted identity, or restricted content merely because the agent had access during processing.

Where agent processing affects privacy handling, agent provenance SHOULD remain reviewable by authorized reviewers.

### 15.16 Privacy Metadata and Derived Metadata

Derived metadata MUST preserve privacy boundaries.

Derived metadata may reveal restricted knowledge even when the original restricted content is not directly reproduced.

Derived metadata MAY include summaries, keywords, classifications, embeddings, indexes, entity detections, relationship suggestions, validation notes, migration notes, or workflow outputs.

Derived metadata created from restricted, confidential, sensitive, or personal knowledge SHOULD inherit appropriate privacy restrictions unless a future governed privacy specification defines a different rule.

Derived metadata MUST NOT expose restricted information merely because it is shorter, transformed, summarized, indexed, embedded, anonymized, or easier to search.

Where derived metadata cannot safely preserve privacy boundaries, it SHOULD require review, redaction, restriction, deletion, or exclusion from publication, export, indexing, synchronization, backup, agent use, or downstream use.

### 15.17 Privacy Metadata Success

Privacy metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations can determine:

- what privacy classification applies;
- what entity the privacy classification applies to;
- what access is permitted;
- what visibility is permitted;
- what handling restrictions apply;
- what publication restrictions apply;
- what export restrictions apply;
- what indexing restrictions apply;
- what synchronization restrictions apply;
- what backup restrictions apply;
- what agent access restrictions apply;
- what workflow restrictions apply;
- what downstream-use restrictions apply;
- whether privacy affects relationships;
- whether privacy affects provenance;
- whether privacy affects lifecycle state;
- whether privacy affects authority;
- whether privacy affects validation;
- whether privacy affects compatibility;
- whether privacy affects import, export, or migration;
- whether privacy remains valid across implementation replacement.

Privacy metadata is successful when access, visibility, handling, publication, export, indexing, synchronization, backup, agent access, workflow handling, and downstream-use expectations remain explicit, portable, reviewable, validatable, compatible, and implementation-independent without exposing restricted information or being confused with authority, lifecycle state, validation state, workflow state, implementation state, user interface state, folder placement, filename convention, tag convention, or operational convenience.

## 16. Metadata and Validation

Metadata and validation are closely connected because validation determines whether Knowledge Objects, Knowledge Records, metadata elements, relationships, source references, provenance, lifecycle states, authority assignments, privacy classifications, compatibility metadata, workflow outputs, agent outputs, imports, exports, migrations, publications, indexes, backups, and other governed entities satisfy applicable standards, specifications, profiles, workflows, and implementation expectations.

Validation metadata describes whether applicable requirements have been checked, what was checked, what result occurred, what issues were detected, what warnings remain, what repair is required, and whether the validated entity can be used for a defined purpose.

A compliant metadata model SHALL support validation interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, access-control assumptions, graph display, search ranking, or undocumented implementation behavior.

Validation metadata SHOULD help determine:

- what entity was validated;
- what validation scope applied;
- what standard or specification was used;
- what validation profile was used where applicable;
- what validator was used where applicable;
- what result occurred;
- what errors were found;
- what warnings were found;
- what metadata was missing;
- what metadata was malformed;
- what metadata was ambiguous;
- what relationships were broken;
- what provenance issues were detected;
- what lifecycle issues were detected;
- what authority issues were detected;
- what privacy issues were detected;
- what compatibility issues were detected;
- what import, export, or migration issues were detected;
- what review remains required.

Validation metadata MUST remain distinguishable from factual truth, authority, approval, lifecycle state, privacy clearance, publication readiness, source reliability, agent certainty, workflow completion, implementation success, and user interface status.

KS-0003 defines validation metadata at the conceptual standard level.

KS-0003 does not define exact validation field names, exact validation states, exact validator behavior, exact validation profiles, exact schemas, exact allowed values, exact serialization formats, exact database columns, exact workflow states, or exact validation tooling.

A future validation specification MAY define those details.

### 16.1 Validation Metadata Purpose

Validation metadata exists to preserve compliance clarity, reviewability, repairability, workflow safety, automation safety, publication safety, export safety, migration safety, compatibility assessment, and long-term maintainability.

Validation metadata SHOULD support:

- standards compliance;
- specification compliance;
- metadata completeness checks;
- metadata correctness checks;
- relationship checks;
- provenance checks;
- lifecycle checks;
- authority checks;
- privacy checks;
- compatibility checks;
- import checks;
- export checks;
- migration checks;
- publication checks;
- workflow routing;
- agent handling;
- repair guidance;
- downstream-use decisions.

Validation metadata MUST help prevent invalid, incomplete, ambiguous, incompatible, private, unreviewed, agent-generated, migrated, or lossy knowledge from being mistaken for complete governed knowledge.

Validation metadata MUST remain distinguishable from the metadata being validated.

Validation metadata MUST NOT silently override explicit metadata, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, compatibility metadata, or source references.

### 16.2 Validation Scope

Validation metadata SHOULD make clear what entity and what scope were validated.

Validation scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a privacy classification;
- a compatibility statement;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- an index;
- an embedding;
- a backup;
- a synchronized copy;
- a future governed entity.

Validation scope MUST be explicit enough to prevent validation confusion where validation affects interpretation, authority, privacy, lifecycle state, publication, export, migration, automation, agent access, or downstream use.

A Knowledge Object may pass one validation scope while failing another.

A record may be structurally valid but not publication-ready.

A metadata element may be syntactically valid but semantically ambiguous.

A migration may be technically complete but compatibility-limited.

An agent output may be useful for review while remaining unvalidated for governed use.

### 16.3 Validation State Metadata

Validation metadata MAY indicate validation state.

Validation state MAY include valid, invalid, partially valid, unvalidated, needs review, needs repair, warning, blocked, deprecated, superseded, incompatible, migrated with loss, or governed by a future validation state.

This list is descriptive and does not define a complete approved validation vocabulary.

A future validation specification MAY define exact validation states, validation result codes, severity levels, validation profiles, validation rules, repair guidance, compatibility behavior, and migration behavior.

Validation state MUST remain distinguishable from lifecycle state.

A valid record is not automatically approved.

An invalid record is not automatically rejected.

A warning is not automatically a failure unless a governed validation profile defines that behavior.

A record that passes validation is not automatically authoritative, public, publication-ready, privacy-cleared, or suitable for unrestricted downstream use.

### 16.4 Structural Validation Metadata

Structural validation metadata describes whether a Knowledge Object, Knowledge Record, metadata element, relationship, source reference, or representation satisfies applicable structural expectations.

Structural validation MAY check:

- required heading presence;
- heading order;
- section numbering;
- list marker consistency;
- metadata presence;
- metadata placement;
- metadata format;
- field completeness where applicable;
- relationship structure;
- source-reference structure;
- import structure;
- export structure;
- migration structure;
- serialization structure;
- implementation-profile structure.

Structural validation MUST NOT be confused with semantic correctness.

A structurally valid record may still contain incorrect, outdated, private, low-authority, incomplete, or unreviewed knowledge.

A structurally invalid record may still contain useful knowledge that requires repair.

Structural validation SHOULD support repair without destroying meaning-critical metadata.

### 16.5 Semantic Validation Metadata

Semantic validation metadata describes whether metadata meaning is clear, consistent, compatible, and interpretable under applicable standards or specifications.

Semantic validation MAY check:

- whether metadata meaning is explicit;
- whether metadata conflicts with Object Identity;
- whether metadata conflicts with provenance;
- whether metadata conflicts with relationships;
- whether metadata conflicts with lifecycle state;
- whether metadata conflicts with authority;
- whether metadata conflicts with privacy classification;
- whether metadata conflicts with compatibility expectations;
- whether metadata depends on hidden implementation state;
- whether required distinctions remain clear;
- whether source material and Knowledge Records remain distinct;
- whether evidence and interpretation remain distinct.

Semantic validation SHOULD identify ambiguity where ambiguity affects interpretation, governance, privacy, validation, publication, export, migration, automation, or downstream use.

Semantic validation MUST NOT silently rewrite governed meaning unless a governed repair workflow explicitly permits that behavior.

### 16.6 Identity Validation Metadata

Validation metadata SHOULD support Object Identity checks where identity affects interpretation, relationships, provenance, lifecycle state, authority, privacy, import, export, migration, compatibility, or downstream use.

Identity validation MAY detect:

- missing Stable Object Identifier;
- malformed Stable Object Identifier;
- duplicate Stable Object Identifier;
- conflicting identifiers;
- ambiguous supporting identifiers;
- unresolved temporary identifiers;
- broken redirects;
- deprecated identifiers without mapping;
- external identifiers without context;
- identity metadata dependent on hidden implementation state;
- relationships that depend on unstable identifiers;
- migration records that lose identity continuity.

Identity validation MUST preserve the Object Identity boundaries defined by KS-0002.

A validation result MUST NOT create, merge, split, redirect, supersede, or deprecate Object Identity unless a governed identity or migration process explicitly permits that behavior.

### 16.7 Relationship Validation Metadata

Validation metadata SHOULD support relationship checks where relationships affect meaning, provenance, dependency, hierarchy, sequence, evidence, source traceability, lifecycle state, authority, privacy, governance, import, export, migration, compatibility, or downstream use.

Relationship validation MAY detect:

- missing relationship target;
- ambiguous relationship target;
- unstable relationship target;
- invalid relationship type;
- unsupported relationship type;
- missing relationship direction;
- invalid relationship direction;
- missing relationship provenance;
- relationship privacy risk;
- relationship authority ambiguity;
- relationship lifecycle ambiguity;
- relationship dependent on hidden implementation state;
- relationship dependent on filename, folder path, tag, backlink, graph layout, or search result;
- broken relationship after import, export, or migration.

Relationship validation MUST NOT convert inferred, suggested, visual, search-based, or agent-generated relationships into governed relationships without appropriate review where review is required.

### 16.8 Provenance Validation Metadata

Validation metadata SHOULD support provenance checks where provenance affects interpretation, authority, privacy, validation, reviewability, source traceability, publication, export, migration, compatibility, or downstream use.

Provenance validation MAY detect:

- missing provenance where required;
- ambiguous provenance;
- inaccessible source material;
- unavailable source material;
- restricted source material exposed improperly;
- unclear evidence source;
- unclear interpretation source;
- missing creation context;
- missing revision context;
- missing agent provenance;
- missing workflow provenance;
- missing transformation provenance;
- provenance dependent on hidden implementation state;
- provenance lost during import, export, or migration.

Provenance validation MUST preserve privacy boundaries.

A provenance validation result MUST NOT expose restricted source material, restricted actors, restricted workflows, restricted relationships, restricted decisions, restricted identities, restricted timestamps, or restricted content merely to improve validation clarity.

### 16.9 Lifecycle Validation Metadata

Validation metadata SHOULD support lifecycle checks where lifecycle state affects interpretation, authority, privacy, validation, publication, export, migration, automation, workflow behavior, or downstream use.

Lifecycle validation MAY detect:

- missing lifecycle state where required;
- ambiguous lifecycle state;
- invalid lifecycle state;
- unsupported lifecycle state;
- lifecycle state dependent on hidden implementation state;
- lifecycle state conflicting with authority metadata;
- lifecycle state conflicting with privacy metadata;
- lifecycle state conflicting with validation metadata;
- lifecycle state conflicting with provenance metadata;
- lifecycle state conflicting with publication metadata;
- lifecycle state lost during import, export, or migration;
- deprecated or superseded records presented as current;
- draft or unreviewed records presented as approved.

Lifecycle validation MUST remain distinguishable from lifecycle transition.

A validation result may identify a lifecycle issue.

A validation result MUST NOT silently change lifecycle state unless a governed workflow explicitly permits that behavior.

### 16.10 Authority Validation Metadata

Validation metadata SHOULD support authority checks where authority affects interpretation, governance, publication, export, migration, automation, validation, or downstream use.

Authority validation MAY detect:

- missing authority metadata where required;
- ambiguous authority scope;
- invalid authority level;
- unsupported authority value;
- authority dependent on hidden implementation state;
- authority conflicting with lifecycle metadata;
- authority conflicting with privacy metadata;
- authority conflicting with validation metadata;
- authority conflicting with provenance metadata;
- deprecated or superseded records presented as current authority;
- draft or unreviewed records presented as authoritative;
- agent-generated output presented as authoritative without review;
- lower-authority metadata conflicting with higher-authority standards;
- authority metadata lost during import, export, or migration.

Authority validation MUST preserve governance hierarchy.

A validation result MUST NOT assign constitutional, standard, specification, operational, approval, or publication authority unless a governed authority workflow explicitly permits that behavior.

### 16.11 Privacy Validation Metadata

Validation metadata SHOULD support privacy checks where privacy affects access, routing, indexing, synchronization, backup, publication, export, migration, automation, agent access, or downstream use.

Privacy validation MAY detect:

- missing privacy classification where required;
- ambiguous privacy classification;
- unsupported privacy classification;
- conflicting privacy classifications;
- privacy metadata dependent on hidden implementation state;
- restricted knowledge in public metadata;
- restricted source references exposed improperly;
- restricted provenance exposed improperly;
- restricted relationships exposed improperly;
- restricted authority metadata exposed improperly;
- restricted lifecycle metadata exposed improperly;
- restricted validation output exposed improperly;
- agent-readable metadata that should be agent-restricted;
- exportable metadata that should be non-exportable;
- indexable metadata that should be non-indexable;
- privacy metadata lost during import, export, migration, backup, synchronization, or implementation replacement.

Privacy validation MUST preserve privacy boundaries.

A validation report MUST NOT expose restricted knowledge merely to explain a privacy issue.

Where validation usefulness and privacy conflict, privacy SHALL take precedence.

### 16.12 Compatibility Validation Metadata

Validation metadata SHOULD support compatibility checks where compatibility affects interpretation, import, export, migration, standards evolution, implementation replacement, validation, publication, or downstream use.

Compatibility validation MAY detect:

- missing compatibility metadata where required;
- ambiguous compatibility state;
- unsupported metadata profile;
- unsupported standard version;
- unsupported specification version;
- deprecated metadata;
- superseded metadata;
- lossy migration;
- unmapped legacy metadata;
- omitted meaning-critical metadata;
- incompatible serialization;
- implementation-specific metadata presented as standard metadata;
- compatibility claims unsupported by validation evidence.

Compatibility validation SHOULD identify whether a representation is fully compatible, partially compatible, migrated, lossy, deprecated, superseded, incompatible, or requiring review where applicable.

A compatibility validation result MUST NOT hide loss of Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or other meaning-critical metadata.

### 16.13 Validation Metadata During Import, Export, and Migration

Validation metadata SHOULD be preserved during import, export, and migration where validation affects interpretation, compliance, governance, publication, archival handling, compatibility, automation, agent access, or downstream use.

Import, export, or migration processes SHOULD preserve enough validation context to determine:

- what was validated before movement;
- what was validated after movement;
- what validation profile applied;
- what validation results changed;
- what metadata was lost;
- what metadata was transformed;
- what repair remains required;
- what review remains required;
- what compatibility limits apply.

Import, export, or migration processes MUST NOT represent validation as successful when meaning-critical metadata has been lost, corrupted, hidden, redacted without disclosure, mapped ambiguously, or made dependent on hidden implementation state.

A migration that loses meaning-critical validation metadata SHOULD disclose the loss when the loss affects reuse, review, compliance, import, interoperability, publication, governance, automation, agent access, or downstream interpretation.

### 16.14 Validation Metadata and Agents

Agent activity MAY assist validation by detecting missing metadata, malformed metadata, ambiguity, broken relationships, provenance issues, lifecycle issues, authority issues, privacy risks, compatibility problems, import issues, export issues, or migration issues.

Agent-generated validation metadata MUST remain distinguishable from governed validation results when that distinction affects interpretation, authority, privacy, publication, export, migration, automation, or downstream use.

An agent validation suggestion is not automatically a governed validation result.

An agent-generated warning is not automatically a failure.

An agent-generated pass is not automatically compliance.

An agent MUST NOT silently validate, approve, publish, export, migrate, classify, repair, redact, or expose Knowledge Objects or Knowledge Records unless a governed workflow explicitly permits that behavior.

Where agent validation output is accepted into governed validation metadata, the accepted metadata SHOULD preserve enough provenance for future review.

### 16.15 Validation Metadata and Workflows

Workflow activity MAY create or update validation metadata where permitted by a governed workflow or specification.

A workflow MAY route objects or records through validation, review, repair, approval, rejection, publication, export, migration, archival handling, or future validation states.

Workflow state MUST remain distinguishable from validation metadata.

Workflow completion MUST NOT be treated as validation success unless a future governed workflow or validation specification explicitly defines that behavior.

Where a workflow changes validation metadata, the change SHOULD remain traceable to the workflow, triggering event, responsible actor, agent involvement where applicable, source material where applicable, validation profile, validation result, review state, repair state, and approval state.

Workflow-generated validation metadata SHOULD remain reviewable where it affects interpretation, authority, privacy, publication, export, migration, compatibility, automation, or downstream use.

### 16.16 Validation Metadata Success

Validation metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations can determine:

- what entity was validated;
- what validation scope applied;
- what standard or specification applied;
- what validation profile applied where applicable;
- what validator was used where applicable;
- what result occurred;
- what errors were found;
- what warnings were found;
- what metadata was missing;
- what metadata was malformed;
- what metadata was ambiguous;
- what relationships were broken;
- what provenance issues were detected;
- what lifecycle issues were detected;
- what authority issues were detected;
- what privacy issues were detected;
- what compatibility issues were detected;
- what import, export, or migration issues were detected;
- what repair remains required;
- what review remains required;
- whether validation remains valid across implementation replacement.

Validation metadata is successful when compliance state, issue detection, repair needs, review needs, compatibility limits, and downstream-use expectations remain explicit, portable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent without being confused with truth, authority, approval, lifecycle state, privacy clearance, publication readiness, workflow completion, agent certainty, implementation state, or user interface state.

## 17. Metadata and Compatibility

Metadata and compatibility are closely connected because compatibility metadata describes whether Knowledge Objects, Knowledge Records, metadata elements, relationships, source references, provenance, lifecycle states, authority assignments, privacy classifications, validation results, workflow outputs, agent outputs, imports, exports, migrations, publications, indexes, backups, synchronized copies, and other governed entities remain interpretable, portable, validatable, and usable across standards, specifications, schemas, storage systems, workflows, agents, validators, and implementations.

Compatibility metadata helps preserve meaning across standard evolution, specification changes, implementation replacement, import, export, migration, serialization, synchronization, backup, restoration, publication, archival handling, and downstream use.

A compliant metadata model SHALL support compatibility interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, graph display, search ranking, access-control assumptions, or undocumented implementation behavior.

Compatibility metadata SHOULD help determine:

- what standard version applies;
- what specification version applies where applicable;
- what metadata profile applies where applicable;
- what serialization profile applies where applicable;
- what implementation profile applies where applicable;
- whether the representation is fully compatible;
- whether the representation is partially compatible;
- whether the representation has been migrated;
- whether the representation is lossy;
- whether meaning-critical metadata has been preserved;
- whether meaning-critical metadata has been transformed;
- whether meaning-critical metadata has been omitted;
- whether meaning-critical metadata has been redacted;
- whether legacy metadata remains;
- whether deprecated metadata remains;
- whether superseded metadata remains;
- what mapping decisions occurred;
- what review remains required;
- what validation remains required;
- whether compatibility remains valid across implementation replacement.

Compatibility metadata MUST NOT hide loss of Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or other meaning-critical metadata.

KS-0003 defines compatibility metadata at the conceptual standard level.

KS-0003 does not define exact compatibility field names, exact compatibility states, exact compatibility profiles, exact migration rules, exact serialization rules, exact schemas, exact allowed values, exact database columns, exact validation tooling, or exact implementation behavior.

A future compatibility specification MAY define those details.

### 17.1 Compatibility Metadata Purpose

Compatibility metadata exists to preserve interpretation, portability, migration safety, implementation replacement, standard evolution, specification evolution, validation reliability, archival usability, publication safety, import reliability, export reliability, and downstream-use clarity.

Compatibility metadata SHOULD support:

- standard-version tracking;
- specification-version tracking;
- metadata-profile tracking;
- serialization-profile tracking;
- implementation-profile tracking;
- migration tracking;
- import review;
- export review;
- validation review;
- provenance preservation;
- relationship preservation;
- lifecycle preservation;
- authority preservation;
- privacy preservation;
- source-reference preservation;
- lossy-conversion detection;
- deprecated-metadata detection;
- superseded-metadata detection;
- repair guidance;
- downstream-use decisions.

Compatibility metadata MUST help prevent partially compatible, lossy, deprecated, superseded, redacted, migrated, or implementation-specific representations from being mistaken for fully compatible governed knowledge.

Compatibility metadata MUST remain distinguishable from validation metadata.

Validation may check compatibility.

Compatibility describes whether meaning and required context remain usable across changes.

### 17.2 Compatibility Scope

Compatibility metadata SHOULD make clear what entity and what scope the compatibility statement applies to.

Compatibility scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a privacy classification;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- a serialization;
- an index;
- an embedding;
- a backup;
- a synchronized copy;
- a future governed entity.

Compatibility scope MUST be explicit enough to prevent compatibility confusion where compatibility affects interpretation, validation, publication, import, export, migration, archival handling, automation, agent access, or downstream use.

A Knowledge Object may be compatible at the identity level while one of its records is incompatible at the metadata-profile level.

A record may be structurally compatible while losing provenance context.

A migration may preserve content while losing relationship metadata.

An export may preserve public content while omitting restricted metadata for privacy reasons.

A representation may be compatible for reading but not for re-import, validation, publication, or automation.

### 17.3 Standard Version Compatibility Metadata

Compatibility metadata SHOULD identify applicable standard versions where standard version affects interpretation, validation, migration, import, export, publication, archival handling, automation, or downstream use.

Standard version compatibility metadata MAY identify:

- the standard used to create the record;
- the standard used to validate the record;
- the standard used during migration;
- the standard expected by an implementation;
- the standard expected by an export;
- the standard expected by an import;
- the standard expected by a future governed process.

Standard version metadata MUST NOT be treated as proof of compliance by itself.

A record may declare a standard version but still fail validation.

A record may comply with a prior standard version while requiring migration for a newer version.

A record may be partially compatible with a future standard version.

Where standard versions differ, compatibility metadata SHOULD preserve enough context to determine whether migration, validation, repair, review, or restriction is required.

### 17.4 Specification Compatibility Metadata

Compatibility metadata SHOULD identify applicable specifications where specification version affects fields, allowed values, relationships, lifecycle states, authority levels, privacy classifications, validation profiles, serialization formats, import behavior, export behavior, migration behavior, or implementation behavior.

Specification compatibility metadata MAY identify:

- what specification applies;
- what specification version applies;
- what specification scope applies;
- what metadata fields are governed;
- what allowed values are governed;
- what validation rules are governed;
- what migration rules are governed;
- whether the specification has been superseded;
- whether the specification has been deprecated;
- whether review is required.

A specification MUST remain subordinate to applicable higher-authority standards and constitutional documents.

Compatibility metadata MUST NOT allow a lower-authority specification to override higher-authority meaning.

Where a specification changes, compatibility metadata SHOULD help determine whether the affected metadata remains valid, needs migration, needs validation, needs review, or must be deprecated.

### 17.5 Metadata Profile Compatibility

Compatibility metadata MAY identify metadata profiles where profiles define narrower requirements for object types, record types, workflows, agents, implementations, validation contexts, publication contexts, import contexts, export contexts, migration contexts, or archival contexts.

Metadata profile compatibility SHOULD identify:

- what profile applies;
- what profile version applies;
- what entity the profile applies to;
- what required metadata differs from the base standard;
- what recommended metadata differs from the base standard;
- what optional metadata is supported;
- what validation profile applies;
- what migration behavior applies;
- what compatibility limits exist.

A metadata profile MUST NOT redefine standard meaning unless the profile is governed and authorized by an applicable higher-authority standard or specification.

Where profile-specific metadata is lost during export, import, migration, synchronization, backup, or implementation replacement, the loss SHOULD be disclosed when it affects interpretation, validation, usability, publication, automation, or downstream use.

### 17.6 Serialization Compatibility Metadata

Compatibility metadata MAY identify serialization compatibility where metadata is represented through Markdown, front matter, structured fields, database columns, graph properties, API objects, sidecar files, embedded structures, export packages, backup formats, or future governed formats.

Serialization compatibility metadata SHOULD identify:

- source serialization format;
- target serialization format;
- serialization profile where applicable;
- unsupported fields;
- transformed fields;
- omitted fields;
- redacted fields;
- lossy transformations;
- preserved metadata;
- validation results;
- review requirements.

Serialization compatibility MUST preserve governed metadata meaning.

A serialization that preserves visible text but loses Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or compatibility context MUST NOT be represented as fully compatible.

A format conversion is not automatically a compatible migration.

### 17.7 Implementation Compatibility Metadata

Compatibility metadata MAY identify whether a Knowledge Object, Knowledge Record, metadata element, relationship, source reference, or representation remains usable across implementations.

Implementation compatibility metadata MAY describe:

- implementation profile;
- supported standard version;
- supported specification version;
- supported metadata profile;
- unsupported metadata;
- implementation-specific metadata;
- local-only behavior;
- plugin-dependent behavior;
- database-dependent behavior;
- user-interface-dependent behavior;
- agent-dependent behavior;
- workflow-dependent behavior;
- export limitations;
- import limitations;
- migration limitations.

Implementation compatibility metadata MUST distinguish standard metadata from implementation-specific metadata.

A compliant implementation MUST NOT require hidden implementation state for governed metadata meaning.

Where implementation-specific metadata is lost, ignored, regenerated, or transformed during migration or export, compatibility metadata SHOULD identify whether the loss affects standard meaning, usability, validation, privacy, publication, automation, or downstream use.

### 17.8 Import Compatibility Metadata

Compatibility metadata SHOULD describe import compatibility where knowledge enters a repository, vault, implementation, workflow, standard version, specification version, metadata profile, or serialization format.

Import compatibility metadata MAY identify:

- source system;
- source format;
- source standard version where applicable;
- source specification version where applicable;
- source metadata profile where applicable;
- imported identifiers;
- imported relationships;
- imported provenance;
- imported lifecycle states;
- imported authority metadata;
- imported privacy metadata;
- imported validation metadata;
- imported compatibility metadata;
- mapped metadata;
- omitted metadata;
- transformed metadata;
- required repair;
- required review.

Import compatibility metadata SHOULD make clear whether imported knowledge is fully compatible, partially compatible, staged, quarantined, needs review, needs repair, lossy, deprecated, superseded, or governed by a future import state.

This list is descriptive and does not define a complete approved import compatibility vocabulary.

### 17.9 Export Compatibility Metadata

Compatibility metadata SHOULD describe export compatibility where knowledge leaves a repository, vault, implementation, workflow, standard version, specification version, metadata profile, or serialization format.

Export compatibility metadata MAY identify:

- target system;
- target format;
- target standard version where applicable;
- target specification version where applicable;
- target metadata profile where applicable;
- exported identifiers;
- exported relationships;
- exported provenance;
- exported lifecycle states;
- exported authority metadata;
- exported privacy metadata;
- exported validation metadata;
- exported compatibility metadata;
- omitted metadata;
- redacted metadata;
- transformed metadata;
- export limitations;
- re-import limitations;
- downstream-use limitations.

Export compatibility metadata MUST preserve privacy boundaries.

An export MUST NOT expose restricted metadata merely to improve compatibility.

Where export omits or redacts meaning-critical metadata, the omission or redaction SHOULD be disclosed when disclosure is permitted and affects reuse, validation, re-import, interoperability, publication, governance, automation, or downstream interpretation.

### 17.10 Migration Compatibility Metadata

Compatibility metadata SHOULD describe migration compatibility where knowledge moves between standards, specifications, schemas, profiles, formats, repositories, vaults, storage systems, databases, workflows, agents, or implementations.

Migration compatibility metadata MAY identify:

- source standard version;
- target standard version;
- source specification version;
- target specification version;
- source metadata profile;
- target metadata profile;
- source format;
- target format;
- migration process;
- mapping decisions;
- transformed metadata;
- repaired metadata;
- deprecated metadata;
- superseded metadata;
- omitted metadata;
- redacted metadata;
- lossy transformations;
- validation before migration;
- validation after migration;
- review requirements.

Migration compatibility metadata SHOULD make clear whether migration preserved meaning-critical metadata.

A migration that loses meaning-critical metadata MUST NOT be represented as full compatibility.

A migration that preserves content but loses identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or compatibility context is not fully compatible.

### 17.11 Lossy Compatibility Metadata

Compatibility metadata MUST identify lossy conditions where meaning-critical metadata is lost, omitted, transformed, redacted, corrupted, hidden, unsupported, unmapped, or made dependent on implementation-specific behavior.

Lossy compatibility metadata MAY identify loss affecting:

- Object Identity;
- title or label;
- object type;
- record type;
- source references;
- provenance;
- relationships;
- lifecycle state;
- authority;
- privacy classification;
- validation metadata;
- compatibility metadata;
- import metadata;
- export metadata;
- migration metadata;
- workflow metadata;
- agent metadata;
- implementation metadata where relevant to usability.

A lossy representation MAY still be useful.

A lossy representation MUST NOT be described as fully compatible.

Where metadata loss is intentional for privacy, publication, archival, or export reasons, compatibility metadata SHOULD disclose the loss when disclosure is permitted and necessary for correct downstream interpretation.

### 17.12 Deprecated and Superseded Metadata Compatibility

Compatibility metadata SHOULD identify deprecated or superseded metadata where prior metadata remains present, referenced, imported, exported, migrated, validated, indexed, archived, or used for compatibility.

Deprecated metadata MAY remain useful for history, migration, duplicate detection, source traceability, relationship repair, audit, archival handling, or backward compatibility.

Superseded metadata MAY remain useful for redirect behavior, prior interpretation, compatibility repair, validation, or historical review.

Deprecated or superseded metadata MUST NOT be treated as current merely because it remains stored, indexed, visible, linked, exported, imported, or referenced.

Where deprecated or superseded metadata is retained, compatibility metadata SHOULD identify replacement metadata where applicable and permitted.

Where deprecated or superseded metadata is removed, compatibility metadata SHOULD preserve enough context to support migration review where removal affects interpretation, validation, relationships, authority, privacy, provenance, publication, export, or downstream use.

### 17.13 Compatibility Metadata and Privacy

Compatibility metadata MUST preserve privacy boundaries.

Compatibility context may reveal restricted source material, restricted relationships, restricted provenance, restricted authority, restricted lifecycle state, restricted validation results, restricted migration behavior, restricted implementation behavior, restricted identities, restricted timestamps, or restricted decisions.

Compatibility metadata MUST NOT expose restricted information merely to improve migration, validation, discovery, automation, publication, export, import, interoperability, or downstream interpretation.

Where compatibility usefulness and privacy conflict, privacy SHALL take precedence.

Where compatibility metadata is redacted or omitted for privacy reasons, the representation SHOULD preserve enough permitted context for authorized review without exposing restricted information.

### 17.14 Compatibility Metadata and Validation

Compatibility metadata SHOULD support validation where compatibility affects interpretation, import, export, migration, standards evolution, implementation replacement, publication, archival handling, automation, or downstream use.

Compatibility validation MAY detect:

- missing compatibility metadata where required;
- ambiguous compatibility state;
- unsupported metadata profile;
- unsupported standard version;
- unsupported specification version;
- deprecated metadata;
- superseded metadata;
- lossy migration;
- unmapped legacy metadata;
- omitted meaning-critical metadata;
- incompatible serialization;
- implementation-specific metadata presented as standard metadata;
- compatibility claims unsupported by validation evidence.

A compatibility validation result MUST NOT hide loss of Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or other meaning-critical metadata.

A future compatibility validation specification MAY define exact compatibility validation fields, states, rules, errors, warnings, repair guidance, migration behavior, and profile behavior.

### 17.15 Compatibility Metadata and Agents

Agent activity MAY assist compatibility review by detecting unsupported metadata, deprecated metadata, superseded metadata, lossy conversion, identity loss, broken relationships, missing provenance, privacy risks, validation issues, profile mismatches, serialization issues, import issues, export issues, or migration issues.

Agent-generated compatibility metadata MUST remain distinguishable from governed compatibility metadata when that distinction affects interpretation, validation, authority, privacy, publication, export, migration, automation, or downstream use.

An agent compatibility suggestion is not automatically a governed compatibility result.

An agent-generated migration mapping is not automatically approved.

An agent-generated compatibility pass is not automatically compliance.

An agent MUST NOT silently convert, migrate, map, omit, redact, publish, export, import, repair, validate, or declare compatibility unless a governed workflow explicitly permits that behavior.

Where agent compatibility output is accepted into governed compatibility metadata, the accepted metadata SHOULD preserve enough provenance for future review.

### 17.16 Compatibility Metadata Success

Compatibility metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, and implementations can determine:

- what standard version applies;
- what specification version applies where applicable;
- what metadata profile applies where applicable;
- what serialization profile applies where applicable;
- what implementation profile applies where applicable;
- whether the representation is fully compatible;
- whether the representation is partially compatible;
- whether the representation has been imported;
- whether the representation has been exported;
- whether the representation has been migrated;
- whether the representation is lossy;
- whether meaning-critical metadata has been preserved;
- whether meaning-critical metadata has been transformed;
- whether meaning-critical metadata has been omitted;
- whether meaning-critical metadata has been redacted;
- whether legacy metadata remains;
- whether deprecated metadata remains;
- whether superseded metadata remains;
- what mapping decisions occurred;
- what repair remains required;
- what review remains required;
- what validation remains required;
- whether compatibility remains valid across implementation replacement.

Compatibility metadata is successful when meaning, identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, import context, export context, migration context, and downstream-use expectations remain explicit, portable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent without hiding loss, redaction, deprecation, supersession, profile mismatch, serialization limits, or implementation-specific dependency.

## 18. Metadata During Import, Export, and Migration

Metadata during import, export, and migration is required to preserve Knowledge Object meaning, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, compatibility context, source references, workflow context, agent context, publication context, archival context, and downstream-use expectations when knowledge moves between systems, formats, repositories, vaults, storage layers, workflows, agents, validators, standards, specifications, or implementations.

Import, export, and migration metadata describes the movement context of knowledge.

Movement context includes where knowledge came from, where it is going, what changed, what was preserved, what was omitted, what was redacted, what was transformed, what was mapped, what was repaired, what was deprecated, what was superseded, what was validated, what failed validation, what requires review, and what compatibility limits remain.

A compliant metadata model SHALL support import, export, and migration interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, graph display, search ranking, access-control assumptions, or undocumented implementation behavior.

Import, export, and migration metadata SHOULD help determine:

- what movement occurred;
- what entity was moved;
- what source system or representation was involved;
- what target system or representation was involved;
- what source standard version applied where applicable;
- what target standard version applied where applicable;
- what source specification version applied where applicable;
- what target specification version applied where applicable;
- what source metadata profile applied where applicable;
- what target metadata profile applied where applicable;
- what source serialization format applied where applicable;
- what target serialization format applied where applicable;
- what metadata was preserved;
- what metadata was transformed;
- what metadata was mapped;
- what metadata was omitted;
- what metadata was redacted;
- what metadata was repaired;
- what metadata was deprecated;
- what metadata was superseded;
- what validation occurred;
- what review remains required;
- what compatibility limits remain.

Import, export, and migration metadata MUST NOT hide loss of Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, compatibility metadata, or other meaning-critical metadata.

KS-0003 defines import, export, and migration metadata at the conceptual standard level.

KS-0003 does not define exact import fields, exact export fields, exact migration fields, exact package formats, exact mapping rules, exact schemas, exact allowed values, exact serialization formats, exact database columns, exact validation tooling, or exact implementation behavior.

A future import, export, and migration specification MAY define those details.

### 18.1 Import, Export, and Migration Metadata Purpose

Import, export, and migration metadata exists to preserve meaning, identity continuity, traceability, compatibility, validation reliability, privacy safety, authority clarity, lifecycle continuity, relationship integrity, source-reference continuity, implementation replacement, archival usability, publication safety, and downstream-use clarity during movement.

Import, export, and migration metadata SHOULD support:

- import review;
- export review;
- migration review;
- identity preservation;
- source-reference preservation;
- provenance preservation;
- relationship preservation;
- lifecycle preservation;
- authority preservation;
- privacy preservation;
- validation preservation;
- compatibility preservation;
- mapping review;
- loss detection;
- redaction disclosure where permitted;
- repair guidance;
- workflow traceability;
- agent traceability;
- archival handling;
- publication handling;
- downstream-use decisions.

Import, export, and migration metadata MUST help prevent moved knowledge from being mistaken for fully compatible governed knowledge when meaning-critical metadata has been lost, hidden, corrupted, transformed ambiguously, redacted without permitted disclosure, or made dependent on implementation-specific behavior.

### 18.2 Movement Scope

Import, export, and migration metadata SHOULD make clear what entity and what scope the movement applies to.

Movement scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a privacy classification;
- a validation result;
- a compatibility statement;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- a serialization;
- an index;
- an embedding;
- a backup;
- a synchronized copy;
- a future governed entity.

Movement scope MUST be explicit enough to prevent ambiguity where movement affects interpretation, Object Identity, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, publication, archival handling, automation, agent access, or downstream use.

A Knowledge Object may be migrated while one of its records is excluded.

A record may be exported while restricted provenance is omitted.

A relationship may be imported while its target requires identity repair.

A source reference may be preserved while source material remains unavailable.

A representation may be export-compatible but not re-import-compatible.

### 18.3 Import Metadata

Import metadata describes context created when knowledge enters a repository, vault, implementation, workflow, standard version, specification version, metadata profile, serialization format, or governed environment.

Import metadata MAY identify:

- source system;
- source repository;
- source vault;
- source format;
- source standard version where applicable;
- source specification version where applicable;
- source metadata profile where applicable;
- source serialization profile where applicable;
- import date where applicable;
- import process;
- imported identifiers;
- imported source references;
- imported provenance;
- imported relationships;
- imported lifecycle states;
- imported authority metadata;
- imported privacy metadata;
- imported validation metadata;
- imported compatibility metadata;
- imported workflow metadata;
- imported agent metadata;
- omitted metadata;
- transformed metadata;
- required repair;
- required review.

Import metadata SHOULD make clear whether imported knowledge is fully compatible, partially compatible, staged, quarantined, needs review, needs repair, lossy, deprecated, superseded, restricted, or governed by a future import state.

This list is descriptive and does not define a complete approved import vocabulary.

Imported knowledge MUST NOT be treated as approved, authoritative, valid, public, privacy-cleared, publication-ready, or fully compatible merely because import succeeded.

### 18.4 Export Metadata

Export metadata describes context created when knowledge leaves a repository, vault, implementation, workflow, standard version, specification version, metadata profile, serialization format, or governed environment.

Export metadata MAY identify:

- target system;
- target repository;
- target vault;
- target format;
- target standard version where applicable;
- target specification version where applicable;
- target metadata profile where applicable;
- target serialization profile where applicable;
- export date where applicable;
- export process;
- exported identifiers;
- exported source references;
- exported provenance;
- exported relationships;
- exported lifecycle states;
- exported authority metadata;
- exported privacy metadata;
- exported validation metadata;
- exported compatibility metadata;
- exported workflow metadata;
- exported agent metadata;
- omitted metadata;
- redacted metadata;
- transformed metadata;
- export limitations;
- re-import limitations;
- downstream-use limitations.

Export metadata MUST preserve privacy boundaries.

An export MUST NOT expose restricted metadata merely to improve portability, traceability, compatibility, validation, publication, automation, agent usefulness, or downstream use.

Where export omits or redacts meaning-critical metadata, the omission or redaction SHOULD be disclosed when disclosure is permitted and affects reuse, validation, re-import, interoperability, governance, automation, publication, archival handling, or downstream interpretation.

### 18.5 Migration Metadata

Migration metadata describes context created when knowledge moves between standards, specifications, schemas, profiles, formats, repositories, vaults, storage systems, databases, workflows, agents, validators, or implementations.

Migration metadata MAY identify:

- source standard version;
- target standard version;
- source specification version;
- target specification version;
- source metadata profile;
- target metadata profile;
- source serialization format;
- target serialization format;
- source implementation profile;
- target implementation profile;
- migration date where applicable;
- migration process;
- migration actor where applicable;
- migration workflow where applicable;
- migration agent where applicable;
- mapping decisions;
- transformed metadata;
- repaired metadata;
- deprecated metadata;
- superseded metadata;
- omitted metadata;
- redacted metadata;
- lossy transformations;
- validation before migration;
- validation after migration;
- review requirements.

Migration metadata SHOULD make clear whether migration preserved meaning-critical metadata.

A migration that loses meaning-critical metadata MUST NOT be represented as full compatibility.

A migration that preserves content but loses identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, or compatibility context is not fully compatible.

### 18.6 Identity Preservation During Movement

Import, export, and migration processes MUST preserve Object Identity where identity affects interpretation, relationships, provenance, lifecycle state, authority, privacy classification, validation, compatibility, publication, archival handling, automation, or downstream use.

Movement processes MUST NOT replace Stable Object Identity with filenames, folder paths, storage locations, display titles, tags, categories, database identifiers, application identifiers, workflow identifiers, agent labels, temporary identifiers, or source identifiers unless a governed mapping process explicitly defines a valid identity relationship.

Identity movement metadata SHOULD identify:

- stable identifiers preserved;
- supporting identifiers preserved;
- temporary identifiers resolved;
- legacy identifiers mapped;
- external identifiers preserved;
- identifiers deprecated;
- identifiers redirected;
- identifiers superseded;
- identifiers repaired;
- identifiers omitted;
- identity conflicts detected;
- identity review required.

A movement process that loses stable Object Identity MUST NOT be represented as full compatibility.

Where identity mapping occurs, the mapping SHOULD remain traceable when it affects duplicate detection, relationship repair, source-reference repair, provenance, validation, import, export, migration, compatibility, or auditability.

### 18.7 Provenance Preservation During Movement

Import, export, and migration processes SHOULD preserve provenance metadata where provenance affects interpretation, authority, privacy, validation, reviewability, source traceability, compatibility, publication, archival handling, automation, or downstream use.

Movement provenance metadata SHOULD identify:

- provenance preserved;
- provenance transformed;
- provenance mapped;
- provenance redacted;
- provenance omitted;
- provenance lost;
- source material availability;
- source-reference continuity;
- creator context preservation;
- revision context preservation;
- workflow context preservation;
- agent context preservation;
- transformation context preservation;
- validation context preservation;
- review context preservation.

A movement process that loses meaning-critical provenance metadata MUST NOT be represented as full compatibility.

Where full provenance cannot be preserved or exposed due to privacy restrictions, movement metadata SHOULD preserve enough permitted context for authorized review without unnecessarily exposing restricted information.

### 18.8 Relationship Preservation During Movement

Import, export, and migration processes SHOULD preserve relationship metadata where relationships affect meaning, provenance, dependency, hierarchy, sequence, evidence, source traceability, lifecycle state, authority, privacy, validation, governance, compatibility, publication, archival handling, automation, or downstream use.

Movement relationship metadata SHOULD identify:

- relationships preserved;
- relationships transformed;
- relationships mapped;
- relationships omitted;
- relationships redacted;
- relationships broken;
- relationship targets unresolved;
- relationship directions preserved;
- relationship types preserved;
- relationship provenance preserved;
- relationship lifecycle preserved;
- relationship authority preserved;
- relationship privacy preserved;
- relationship validation required.

A movement process MUST NOT replace governed relationship metadata with folder placement, filename similarity, tag coincidence, backlink existence, graph proximity, application state, search result, or agent inference unless a governed migration process explicitly maps the relationship in a valid way.

A movement process that loses meaning-critical relationship metadata MUST NOT be represented as full compatibility.

### 18.9 Lifecycle Preservation During Movement

Import, export, and migration processes SHOULD preserve lifecycle metadata where lifecycle state affects interpretation, authority, privacy, validation, publication, archival handling, governance, compatibility, automation, or downstream use.

Movement lifecycle metadata SHOULD identify:

- lifecycle states preserved;
- lifecycle states transformed;
- lifecycle states mapped;
- lifecycle states omitted;
- lifecycle states redacted;
- lifecycle states deprecated;
- lifecycle states superseded;
- lifecycle states requiring review;
- lifecycle states requiring validation;
- lifecycle conflicts detected;
- lifecycle state assumptions made.

Movement processes MUST NOT treat imported, exported, or migrated knowledge as approved merely because movement succeeded.

Movement processes MUST NOT silently convert draft, review, deprecated, superseded, archived, experimental, restricted, or unvalidated knowledge into approved current knowledge.

A movement process that loses meaning-critical lifecycle metadata MUST NOT be represented as full compatibility.

### 18.10 Authority Preservation During Movement

Import, export, and migration processes SHOULD preserve authority metadata where authority affects interpretation, governance, publication, validation, compatibility, automation, or downstream use.

Movement authority metadata SHOULD identify:

- authority preserved;
- authority transformed;
- authority mapped;
- authority omitted;
- authority redacted;
- authority deprecated;
- authority superseded;
- authority conflicts detected;
- authority scope preserved;
- authority scope changed;
- authority review required.

Movement processes MUST NOT replace governed authority metadata with folder placement, filename convention, tag convention, application state, workflow state, user interface state, backlink count, graph centrality, search ranking, or agent inference unless a governed migration process explicitly maps authority in a valid way.

Movement processes MUST NOT silently elevate authority.

A movement process that loses meaning-critical authority metadata MUST NOT be represented as full compatibility.

### 18.11 Privacy Preservation During Movement

Import, export, and migration processes MUST preserve privacy metadata where privacy affects interpretation, handling, access, indexing, synchronization, backup, publication, archival handling, validation, governance, compatibility, automation, agent access, or downstream use.

Movement privacy metadata SHOULD identify:

- privacy classifications preserved;
- privacy classifications transformed;
- privacy classifications mapped;
- privacy classifications omitted;
- privacy classifications redacted;
- privacy classifications inherited;
- privacy conflicts detected;
- restricted metadata excluded;
- restricted metadata exposed;
- privacy review required;
- agent access restrictions preserved;
- export restrictions preserved;
- indexing restrictions preserved;
- synchronization restrictions preserved;
- backup restrictions preserved.

Movement processes MUST NOT replace governed privacy metadata with folder placement, filename convention, tag convention, color convention, application state, workflow state, user interface state, access-control assumption, or agent inference unless a governed migration process explicitly maps privacy in a valid way.

Movement processes MUST NOT expose restricted metadata merely to improve compatibility, validation, search, automation, publication, export, import, migration, or downstream use.

Where movement usefulness and privacy conflict, privacy SHALL take precedence.

### 18.12 Validation During Movement

Import, export, and migration processes SHOULD create or preserve validation metadata where validation affects interpretation, compliance, governance, publication, archival handling, compatibility, automation, agent access, or downstream use.

Movement validation metadata SHOULD identify:

- validation before movement;
- validation during movement where applicable;
- validation after movement;
- validation profile used;
- validation result;
- validation errors;
- validation warnings;
- missing metadata;
- malformed metadata;
- ambiguous metadata;
- broken relationships;
- identity issues;
- provenance issues;
- lifecycle issues;
- authority issues;
- privacy issues;
- compatibility issues;
- repair required;
- review required.

Movement processes MUST NOT represent validation as successful when meaning-critical metadata has been lost, corrupted, hidden, redacted without permitted disclosure, mapped ambiguously, or made dependent on hidden implementation state.

A movement validation result MUST remain distinguishable from approval, authority, lifecycle state, privacy clearance, publication readiness, and factual truth.

### 18.13 Mapping Metadata

Mapping metadata describes how metadata from one system, standard, specification, schema, profile, serialization, workflow, agent, validator, or implementation corresponds to metadata in another.

Mapping metadata MAY identify:

- source field or concept;
- target field or concept;
- mapping rule;
- mapping confidence;
- mapping actor where applicable;
- mapping workflow where applicable;
- mapping agent where applicable;
- mapping date where applicable;
- mapping loss;
- mapping ambiguity;
- mapping assumptions;
- mapping validation;
- mapping review requirements.

Mapping metadata SHOULD be preserved where mapping affects Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, source references, publication, archival handling, automation, or downstream use.

A mapping decision MUST NOT silently redefine governed meaning.

A mapping decision that changes, narrows, broadens, omits, redacts, or transforms meaning-critical metadata SHOULD remain reviewable.

### 18.14 Redaction and Omission During Movement

Import, export, and migration processes MAY redact or omit metadata where required by privacy, governance, publication, archival handling, legal, contractual, ethical, operational, implementation, or compatibility constraints.

Redaction and omission metadata SHOULD identify:

- what was redacted where permitted;
- what was omitted where permitted;
- why redaction occurred where permitted;
- why omission occurred where permitted;
- whether redaction affects interpretation;
- whether omission affects interpretation;
- whether redaction affects validation;
- whether omission affects validation;
- whether redaction affects compatibility;
- whether omission affects compatibility;
- whether authorized review is required.

Redaction and omission MUST preserve privacy boundaries.

A redacted or omitted representation MAY still be useful.

A redacted or omitted representation MUST NOT be represented as fully compatible where redaction or omission removes meaning-critical metadata.

Where disclosing the redaction itself would expose restricted information, metadata SHOULD preserve enough permitted context for authorized review without exposing restricted information.

### 18.15 Agent and Workflow Movement Metadata

Agents and workflows MAY assist import, export, and migration by identifying metadata, mapping fields, preserving identifiers, detecting loss, repairing structure, validating output, redacting restricted metadata, generating compatibility notes, or preparing review.

Agent-generated or workflow-generated movement metadata MUST remain distinguishable from governed movement metadata where that distinction affects interpretation, authority, privacy, validation, compatibility, publication, automation, or downstream use.

An agent-generated import mapping is not automatically approved.

An agent-generated export package is not automatically privacy-cleared.

An agent-generated migration result is not automatically compatible.

A workflow-completed migration is not automatically valid unless a governed workflow or validation specification explicitly defines that behavior.

Where agent or workflow movement output is accepted into governed metadata, the accepted metadata SHOULD preserve enough provenance for future review.

### 18.16 Import, Export, and Migration Metadata Success

Import, export, and migration metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, and implementations can determine:

- what movement occurred;
- what entity was moved;
- what source system or representation was involved;
- what target system or representation was involved;
- what standard version applied;
- what specification version applied where applicable;
- what metadata profile applied where applicable;
- what serialization profile applied where applicable;
- what Object Identity was preserved;
- what provenance was preserved;
- what relationships were preserved;
- what lifecycle state was preserved;
- what authority was preserved;
- what privacy classification was preserved;
- what validation metadata was preserved;
- what compatibility metadata was preserved;
- what source references were preserved;
- what metadata was transformed;
- what metadata was mapped;
- what metadata was omitted;
- what metadata was redacted;
- what metadata was repaired;
- what metadata was deprecated;
- what metadata was superseded;
- what validation occurred;
- what review remains required;
- what compatibility limits remain;
- whether moved knowledge remains valid across implementation replacement.

Import, export, and migration metadata is successful when moved knowledge remains identifiable, interpretable, traceable, reviewable, privacy-respecting, validatable, compatible, portable, and implementation-independent without hiding loss, redaction, mapping ambiguity, deprecated metadata, superseded metadata, broken relationships, identity discontinuity, authority confusion, privacy exposure, validation ambiguity, or implementation-specific dependency.

## 19. Metadata and Workflows

Metadata and workflows are closely connected because workflows may create, update, validate, route, review, approve, reject, publish, export, import, migrate, archive, repair, classify, redact, synchronize, back up, or otherwise process Knowledge Objects, Knowledge Records, metadata elements, relationships, source references, provenance, lifecycle states, authority assignments, privacy classifications, validation results, compatibility metadata, agent outputs, and other governed entities.

Workflow metadata describes the process context associated with governed knowledge.

Workflow context includes what workflow acted, what triggered the workflow, what entity was processed, what state changed, what metadata changed, what validation occurred, what review occurred, what approval occurred, what agent activity occurred, what error occurred, what repair occurred, what output was produced, what remains pending, and what downstream use is permitted.

A compliant metadata model SHALL support workflow interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, graph display, search ranking, access-control assumptions, or undocumented implementation behavior.

Workflow metadata SHOULD help determine:

- what workflow acted;
- what entity the workflow acted on;
- what triggered the workflow;
- what workflow state applied;
- what workflow step occurred;
- what actor or agent participated where applicable;
- what metadata was created;
- what metadata was changed;
- what metadata was validated;
- what review occurred;
- what approval occurred;
- what rejection occurred;
- what repair occurred;
- what publication, import, export, or migration action occurred;
- what error, warning, or exception occurred;
- what privacy boundaries applied;
- what authority limits applied;
- what downstream-use limits remain.

Workflow metadata MUST remain distinguishable from Object Identity, Knowledge Object meaning, lifecycle state, authority, privacy classification, validation state, provenance, compatibility metadata, implementation state, user interface state, and agent output.

KS-0003 defines workflow metadata at the conceptual standard level.

KS-0003 does not define exact workflow field names, exact workflow states, exact workflow engines, exact workflow schemas, exact allowed values, exact automation rules, exact database columns, exact validation tooling, or exact implementation behavior.

A future workflow specification MAY define those details.

### 19.1 Workflow Metadata Purpose

Workflow metadata exists to preserve process traceability, reviewability, automation safety, validation reliability, privacy safety, authority clarity, lifecycle continuity, repairability, publication safety, import safety, export safety, migration safety, and downstream-use clarity.

Workflow metadata SHOULD support:

- workflow routing;
- workflow review;
- approval review;
- rejection review;
- validation review;
- privacy review;
- authority review;
- lifecycle transition review;
- provenance preservation;
- relationship preservation;
- repair tracking;
- error tracking;
- exception handling;
- agent traceability;
- import handling;
- export handling;
- migration handling;
- publication handling;
- archival handling;
- downstream-use decisions.

Workflow metadata MUST help prevent workflow activity from silently redefining governed metadata, Object Identity, knowledge meaning, authority, privacy classification, lifecycle state, validation status, provenance, relationships, compatibility, or source-reference meaning.

### 19.2 Workflow Scope

Workflow metadata SHOULD make clear what entity and what scope the workflow applies to.

Workflow scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a privacy classification;
- a validation result;
- a compatibility statement;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- an archival record;
- a repair record;
- a synchronized copy;
- a backup;
- a future governed entity.

Workflow scope MUST be explicit enough to prevent process ambiguity where workflow activity affects interpretation, Object Identity, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, publication, archival handling, automation, agent access, or downstream use.

A workflow may act on a Knowledge Record without acting on the entire Knowledge Object.

A workflow may review one relationship without reviewing all relationships.

A workflow may validate structure without approving content.

A workflow may prepare export without authorizing export.

A workflow may archive a record without deprecating the Knowledge Object.

### 19.3 Workflow State Metadata

Workflow metadata MAY indicate workflow state.

Workflow state MAY include pending, active, blocked, completed, failed, canceled, paused, routed, reviewed, approved, rejected, repaired, published, exported, imported, migrated, archived, needs review, needs validation, or governed by a future workflow state.

This list is descriptive and does not define a complete approved workflow vocabulary.

A future workflow specification MAY define exact workflow states, allowed transitions, transition rules, routing rules, validation rules, escalation behavior, rollback behavior, approval behavior, agent behavior, and migration behavior.

Workflow state MUST remain distinguishable from lifecycle state.

A completed workflow is not automatically approval.

A completed workflow is not automatically validation success.

A completed workflow is not automatically privacy clearance.

A completed workflow is not automatically authority assignment.

A failed workflow is not automatically rejection unless a governed workflow specification explicitly defines that relationship.

### 19.4 Workflow Triggers

Workflow metadata MAY identify workflow triggers where trigger context affects interpretation, reviewability, validation, lifecycle state, authority, privacy, publication, import, export, migration, compatibility, automation, or downstream use.

Workflow triggers MAY include:

- human request;
- scheduled process;
- validation result;
- metadata change;
- source update;
- relationship change;
- lifecycle transition;
- authority review;
- privacy review;
- import event;
- export event;
- migration event;
- publication event;
- archival event;
- agent suggestion;
- implementation event;
- future governed trigger.

Workflow trigger metadata SHOULD remain traceable where the trigger affects governed meaning or downstream handling.

A trigger MUST NOT silently authorize a workflow action unless a governed workflow specification explicitly defines that behavior.

A trigger from an agent MUST remain distinguishable from a trigger from a human reviewer, governance decision, validator, implementation, or scheduled process where that distinction affects authority, privacy, validation, publication, export, migration, or downstream use.

### 19.5 Workflow Actors and Responsibility

Workflow metadata SHOULD identify workflow actors where actor context affects provenance, reviewability, authority, privacy, validation, publication, import, export, migration, compatibility, automation, or downstream use.

Workflow actors MAY include:

- human users;
- reviewers;
- approvers;
- maintainers;
- agents;
- validators;
- import processes;
- export processes;
- migration processes;
- publication processes;
- archival processes;
- implementations;
- future governed actors.

Workflow actor metadata MUST preserve privacy boundaries.

Workflow actor metadata MUST NOT expose restricted identities, roles, decisions, timestamps, workflows, source material, or content merely to improve traceability, automation, validation, publication, export, migration, or downstream use.

Where workflow responsibility affects authority, approval, rejection, validation, privacy clearance, publication readiness, or migration compatibility, the applicable responsibility metadata SHOULD be explicit and reviewable.

### 19.6 Workflow Actions

Workflow metadata SHOULD identify workflow actions where action context affects interpretation, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, publication, import, export, migration, automation, or downstream use.

Workflow actions MAY include:

- create;
- update;
- classify;
- summarize;
- link;
- unlink;
- validate;
- review;
- approve;
- reject;
- repair;
- redact;
- publish;
- unpublish;
- import;
- export;
- migrate;
- archive;
- restore;
- synchronize;
- back up;
- route;
- escalate;
- cancel;
- rollback;
- future governed actions.

Workflow actions MUST NOT silently redefine governed metadata.

Where a workflow action changes meaning-critical metadata, the change SHOULD preserve enough provenance for future review.

Where a workflow action fails, partially succeeds, or produces warnings, workflow metadata SHOULD preserve the result where the result affects interpretation, validation, privacy, authority, publication, import, export, migration, compatibility, or downstream use.

### 19.7 Workflow-Generated Metadata

Workflow-generated metadata MAY support routing, review, approval, validation, repair, privacy handling, publication, import, export, migration, archival handling, synchronization, backup, automation, or downstream use.

Workflow-generated metadata MUST remain distinguishable from human-authored metadata, agent-generated metadata, implementation metadata, lifecycle metadata, authority metadata, privacy metadata, validation metadata, provenance metadata, relationship metadata, and compatibility metadata when the distinction affects governed interpretation.

Workflow-generated metadata MUST NOT become authoritative merely because a workflow produced it.

Workflow-generated metadata MUST NOT become required standard metadata merely because an implementation depends on it.

Where workflow-generated metadata is accepted into governed metadata, the accepted metadata SHOULD preserve enough provenance to determine what workflow created it, what trigger caused it, what actor or agent participated, what validation occurred, what review occurred, what approval occurred, and what limitations remain.

### 19.8 Workflow Metadata and Lifecycle State

Workflow metadata MAY support lifecycle transitions where permitted by a governed workflow or specification.

A workflow MAY route objects or records through drafting, review, approval, rejection, deprecation, supersession, archival, validation, publication, import, export, migration, or future lifecycle states.

Workflow state MUST remain distinguishable from lifecycle state.

Workflow completion MUST NOT be treated as lifecycle approval unless a governed workflow specification explicitly defines that behavior.

Where a workflow changes lifecycle metadata, the change SHOULD remain traceable to the workflow, triggering event, responsible actor, agent involvement where applicable, source material where applicable, validation result where applicable, review state, and approval state.

A workflow MUST NOT silently convert draft, review, deprecated, superseded, archived, experimental, restricted, or unvalidated knowledge into approved current knowledge unless a governed workflow explicitly permits that transition.

### 19.9 Workflow Metadata and Authority

Workflow metadata MAY support authority assignment or authority review where permitted by governance.

Workflow activity MUST remain distinguishable from authority.

A workflow may prepare authority review without assigning authority.

A workflow may route an object to an approver without approval occurring.

A workflow may record approval without creating constitutional authority.

A workflow may assign operational authority only where a governed workflow or authority specification permits that behavior.

Workflow metadata MUST NOT silently assign constitutional authority, standard authority, specification authority, approval authority, publication authority, privacy clearance, or unrestricted downstream authority unless a governed workflow explicitly permits that behavior.

Where workflow activity affects authority, the authority scope, actor, review basis, approval basis, lifecycle state, privacy boundaries, validation results, and limitations SHOULD remain explicit and reviewable.

### 19.10 Workflow Metadata and Privacy

Workflow metadata MUST preserve privacy boundaries.

Workflow context may reveal restricted source material, restricted relationships, restricted provenance, restricted authority, restricted lifecycle state, restricted validation results, restricted migration behavior, restricted identities, restricted timestamps, restricted decisions, restricted workflows, or restricted content.

Workflow metadata MUST NOT expose restricted information merely to improve process traceability, validation, discovery, automation, publication, export, import, migration, compatibility, or downstream interpretation.

Workflow metadata SHOULD support privacy handling where workflows affect access, routing, indexing, synchronization, backup, publication, export, migration, agent access, automation, or downstream use.

Where workflow usefulness and privacy conflict, privacy SHALL take precedence.

Where workflow metadata is redacted or omitted for privacy reasons, the representation SHOULD preserve enough permitted context for authorized review without exposing restricted information.

### 19.11 Workflow Metadata and Validation

Workflow metadata SHOULD support validation where workflow activity affects compliance, interpretation, governance, privacy, lifecycle state, authority, publication, import, export, migration, archival handling, automation, agent access, or downstream use.

Workflow validation MAY detect:

- missing workflow metadata where required;
- ambiguous workflow state;
- unsupported workflow state;
- workflow state dependent on hidden implementation state;
- workflow completion presented as approval without governance;
- workflow completion presented as validation success without validation;
- workflow output presented as authority without review;
- workflow output exposing restricted metadata;
- workflow activity conflicting with lifecycle metadata;
- workflow activity conflicting with authority metadata;
- workflow activity conflicting with privacy metadata;
- workflow activity conflicting with validation metadata;
- workflow metadata lost during import, export, or migration.

A workflow validation result MUST remain distinguishable from workflow state.

A validation result may identify a workflow issue.

A validation result MUST NOT silently change workflow state unless a governed workflow explicitly permits that behavior.

### 19.12 Workflow Metadata During Import, Export, and Migration

Workflow metadata SHOULD be preserved during import, export, and migration where workflow context affects interpretation, provenance, lifecycle state, authority, privacy, validation, compatibility, publication, archival handling, automation, agent access, or downstream use.

Import, export, or migration processes MUST NOT replace governed workflow metadata with folder placement, filename convention, tag convention, color convention, application state, user interface state, workflow memory, or agent inference unless a governed migration process explicitly maps workflow metadata in a valid way.

Where workflow metadata is transformed, mapped, omitted, redacted, deprecated, superseded, repaired, or partially preserved during migration, the process SHOULD preserve enough context for authorized future review.

A migration that loses meaning-critical workflow metadata MUST NOT be represented as full compatibility.

An export that omits meaning-critical workflow metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, publication, governance, automation, agent access, or downstream interpretation.

### 19.13 Workflow Metadata and Agents

Agents MAY participate in workflows where permitted by governance, privacy classification, authority rules, validation expectations, and applicable workflow specifications.

Agent participation in a workflow MUST remain distinguishable from human review, human approval, governance approval, validation success, privacy clearance, publication readiness, and authority assignment.

Agent workflow metadata MAY identify:

- agent involved;
- agent task;
- instruction context where appropriate;
- source material used where permitted;
- output generated;
- metadata changed;
- validation performed;
- review prepared;
- review required;
- approval status;
- limitations or uncertainty where applicable.

An agent MUST NOT silently approve, reject, validate, publish, export, migrate, classify, redact, repair, archive, supersede, deprecate, or assign authority unless a governed workflow explicitly permits that behavior.

Where agent workflow output is accepted into governed metadata, the accepted metadata SHOULD preserve enough provenance for future review.

### 19.14 Workflow Errors, Exceptions, and Repair Metadata

Workflow metadata SHOULD identify errors, exceptions, partial failures, repair actions, rollback actions, unresolved issues, and required follow-up where those conditions affect interpretation, validation, privacy, authority, lifecycle state, publication, import, export, migration, compatibility, automation, or downstream use.

Workflow error metadata MAY identify:

- failed step;
- error type;
- warning type;
- affected entity;
- affected metadata;
- failed validation;
- broken relationship;
- missing source reference;
- privacy risk;
- authority conflict;
- lifecycle conflict;
- compatibility issue;
- repair action;
- rollback action;
- review required.

Workflow error metadata MUST preserve privacy boundaries.

A workflow failure MUST NOT silently erase provenance, validation results, source references, relationships, privacy classification, authority metadata, lifecycle state, compatibility metadata, or movement context where those remain necessary for future review.

Repair metadata SHOULD remain traceable where repair affects governed meaning.

### 19.15 Workflow Metadata and Implementation Independence

Workflow metadata MUST remain implementation-independent where workflow context affects governed meaning, validation, privacy, authority, lifecycle state, publication, import, export, migration, compatibility, automation, or downstream use.

A workflow may be executed by a specific implementation.

A workflow may be displayed through a specific user interface.

A workflow may be stored in a specific database.

A workflow may be automated by a specific tool.

A workflow may involve a specific agent system.

None of those implementation mechanisms define standard workflow meaning unless a governed standard or specification explicitly defines that behavior.

A compliant implementation SHOULD preserve governed workflow metadata across export, import, migration, backup, restoration, synchronization, validation, and implementation replacement.

A workflow that cannot be interpreted outside one implementation SHOULD NOT be used as the only source of meaning-critical metadata.

### 19.16 Workflow Metadata Success

Workflow metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, and implementations can determine:

- what workflow acted;
- what entity the workflow acted on;
- what workflow scope applied;
- what triggered the workflow;
- what workflow state applied;
- what workflow step occurred;
- what actor or agent participated where applicable;
- what metadata was created;
- what metadata was changed;
- what metadata was validated;
- what review occurred;
- what approval occurred;
- what rejection occurred;
- what repair occurred;
- what publication, import, export, or migration action occurred;
- what error, warning, or exception occurred;
- what privacy boundaries applied;
- what authority limits applied;
- what validation expectations applied;
- what compatibility limits remained;
- what downstream-use limits remained;
- whether workflow metadata remains valid across implementation replacement.

Workflow metadata is successful when process context remains explicit, portable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent without being confused with Object Identity, knowledge meaning, lifecycle state, authority, privacy classification, validation state, provenance, compatibility metadata, implementation state, user interface state, or agent output.

## 20. Metadata and Agents

Metadata and agents are closely connected because agents may create, modify, classify, summarize, extract, transform, link, validate, review, route, redact, import, export, migrate, publish, index, embed, synchronize, repair, or otherwise process Knowledge Objects, Knowledge Records, metadata elements, relationships, source references, provenance, lifecycle states, authority assignments, privacy classifications, validation results, compatibility metadata, workflow outputs, and other governed entities.

Agent metadata describes the agent context associated with governed knowledge.

Agent context includes what agent acted, what task was performed, what instruction or workflow guided the action, what source material was used, what metadata was created, what metadata was changed, what relationship was proposed, what validation occurred, what output was generated, what uncertainty remains, what review is required, what approval occurred, what privacy boundaries applied, what authority limits applied, and what downstream use is permitted.

A compliant metadata model SHALL support agent interpretation without relying only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, agent memory, workflow memory, graph display, search ranking, access-control assumptions, or undocumented implementation behavior.

Agent metadata SHOULD help determine:

- what agent acted;
- what entity the agent acted on;
- what task the agent performed;
- what workflow governed the agent activity where applicable;
- what instruction context applied where appropriate;
- what source material was used where permitted;
- what metadata was created;
- what metadata was changed;
- what relationship was suggested or created;
- what validation was suggested or performed;
- what output was generated;
- what uncertainty or limitation remains;
- what review remains required;
- what approval occurred where applicable;
- what privacy boundaries applied;
- what authority limits applied;
- what downstream-use limits remain.

Agent metadata MUST remain distinguishable from Object Identity, Knowledge Object meaning, lifecycle state, authority, privacy classification, validation state, provenance, compatibility metadata, workflow state, implementation state, user interface state, and agent output.

KS-0003 defines agent metadata at the conceptual standard level.

KS-0003 does not define exact agent field names, exact agent classes, exact model identifiers, exact tool identifiers, exact prompt formats, exact instruction records, exact schemas, exact allowed values, exact database columns, exact validation tooling, or exact implementation behavior.

A future agent metadata specification MAY define those details.

### 20.1 Agent Metadata Purpose

Agent metadata exists to preserve agent traceability, reviewability, automation safety, validation reliability, privacy safety, authority clarity, provenance clarity, workflow continuity, repairability, publication safety, import safety, export safety, migration safety, and downstream-use clarity.

Agent metadata SHOULD support:

- agent involvement review;
- agent-output review;
- source-use review;
- instruction-context review;
- workflow review;
- validation review;
- privacy review;
- authority review;
- lifecycle review;
- relationship review;
- provenance preservation;
- repair tracking;
- uncertainty tracking;
- limitation tracking;
- import handling;
- export handling;
- migration handling;
- publication handling;
- downstream-use decisions.

Agent metadata MUST help prevent agent activity from silently redefining governed metadata, Object Identity, knowledge meaning, authority, privacy classification, lifecycle state, validation status, provenance, relationships, compatibility, or source-reference meaning.

Agent metadata MUST make agent involvement reviewable where agent activity affects governed meaning.

### 20.2 Agent Scope

Agent metadata SHOULD make clear what entity and what scope the agent activity applies to.

Agent scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a privacy classification;
- a validation result;
- a compatibility statement;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- an index;
- an embedding;
- a backup;
- a synchronized copy;
- a future governed entity.

Agent scope MUST be explicit enough to prevent ambiguity where agent activity affects interpretation, Object Identity, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, publication, archival handling, automation, workflow behavior, agent access, or downstream use.

An agent may act on one Knowledge Record without acting on the entire Knowledge Object.

An agent may suggest one relationship without validating all relationships.

An agent may summarize source material without approving the summary.

An agent may prepare review without completing review.

An agent may assist migration without declaring compatibility.

### 20.3 Agent Identity Metadata

Agent metadata SHOULD identify the agent where agent identity affects provenance, reviewability, authority, privacy, validation, publication, import, export, migration, compatibility, automation, or downstream use.

Agent identity metadata MAY identify:

- agent name;
- agent role;
- agent class;
- model class where appropriate;
- tool context where appropriate;
- workflow context where applicable;
- implementation context where applicable;
- responsible human or process where applicable;
- future governed agent identifier.

Agent identity metadata MUST remain distinguishable from Object Identity.

An agent identifier identifies the agent or process involved.

An agent identifier does not identify the Knowledge Object.

Agent identity metadata SHOULD preserve privacy boundaries.

Agent identity metadata MUST NOT expose restricted identities, workflows, source material, instructions, decisions, timestamps, or content merely to improve traceability, validation, publication, export, migration, or downstream use.

### 20.4 Agent Task Metadata

Agent metadata SHOULD identify the task performed where task context affects interpretation, provenance, lifecycle state, authority, privacy, validation, compatibility, publication, import, export, migration, workflow behavior, automation, or downstream use.

Agent tasks MAY include:

- drafting;
- summarization;
- extraction;
- classification;
- normalization;
- transformation;
- translation;
- relationship suggestion;
- relationship creation;
- metadata suggestion;
- metadata update;
- validation suggestion;
- validation execution;
- review preparation;
- privacy review preparation;
- authority review preparation;
- import mapping;
- export preparation;
- migration mapping;
- compatibility review;
- redaction assistance;
- indexing;
- embedding;
- repair suggestion;
- future governed agent task.

Agent task metadata MUST remain distinguishable from agent output.

A task description explains what the agent attempted or performed.

A task description does not make the resulting output correct, valid, approved, authoritative, public, privacy-cleared, or compatible.

Where an agent task affects meaning-critical metadata, the task SHOULD remain traceable for future review.

### 20.5 Agent Instruction Metadata

Agent metadata MAY identify instruction context where instructions affect interpretation, provenance, validation, privacy, authority, publication, import, export, migration, compatibility, workflow behavior, or downstream use.

Instruction metadata MAY describe:

- task instruction;
- workflow instruction;
- validation instruction;
- privacy instruction;
- authority instruction;
- source-use instruction;
- transformation instruction;
- migration instruction;
- review instruction;
- limitation instruction;
- future governed instruction context.

Instruction metadata SHOULD remain explicit enough to support review where instruction context affects governed meaning.

Instruction metadata MUST preserve privacy boundaries.

An instruction record MUST NOT expose restricted source material, restricted prompts, restricted workflows, restricted identities, restricted decisions, restricted credentials, restricted security context, or restricted content merely to improve traceability or reproducibility.

Where full instruction context cannot be exposed due to privacy or security restrictions, metadata SHOULD preserve enough permitted context for authorized review without exposing restricted information.

### 20.6 Agent Source-Use Metadata

Agent metadata SHOULD identify source material used by an agent where source use affects interpretation, provenance, validation, privacy, authority, publication, import, export, migration, compatibility, or downstream use.

Agent source-use metadata MAY identify:

- source material used;
- source reference used;
- source scope used;
- source excerpt used where permitted;
- source availability;
- source restriction;
- source transformation;
- source omission;
- source uncertainty;
- source conflict;
- source review requirement.

Agent source-use metadata MUST preserve the distinction between source material and agent output.

An agent output is not the source.

An agent summary is not the source.

An agent extraction is not automatically complete source representation.

An agent classification is not automatically source truth.

Agent source-use metadata MUST preserve privacy boundaries.

Restricted source material MUST NOT be exposed merely to explain agent activity.

### 20.7 Agent-Generated Metadata

Agent-generated metadata MAY support drafting, classification, summarization, extraction, transformation, linking, validation, review preparation, import, export, migration, publication, indexing, embedding, repair, or downstream use.

Agent-generated metadata MUST remain distinguishable from human-authored metadata, workflow-generated metadata, implementation metadata, lifecycle metadata, authority metadata, privacy metadata, validation metadata, provenance metadata, relationship metadata, and compatibility metadata when the distinction affects governed interpretation.

Agent-generated metadata MUST NOT become authoritative merely because an agent produced it.

Agent-generated metadata MUST NOT become required standard metadata merely because an implementation depends on it.

Where agent-generated metadata is accepted into governed metadata, the accepted metadata SHOULD preserve enough provenance to determine what agent created it, what task caused it, what workflow governed it, what source material supported it where permitted, what validation occurred, what review occurred, what approval occurred, and what limitations remain.

### 20.8 Agent Output Metadata

Agent output metadata describes the output produced by an agent.

Agent output MAY include:

- summary;
- extraction;
- classification;
- relationship suggestion;
- metadata suggestion;
- validation suggestion;
- migration mapping;
- compatibility note;
- review note;
- repair note;
- redaction suggestion;
- publication note;
- transformed record;
- generated draft;
- future governed output.

Agent output metadata MUST remain distinguishable from approved Knowledge Records and governed metadata.

An agent output is not automatically valid.

An agent output is not automatically approved.

An agent output is not automatically authoritative.

An agent output is not automatically privacy-cleared.

An agent output is not automatically publication-ready.

An agent output is not automatically compatible.

Agent output SHOULD require review where it affects Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, publication, import, export, migration, automation, or downstream use.

### 20.9 Agent Metadata and Provenance

Agent metadata SHOULD support provenance where agent activity affects creation, modification, classification, summarization, extraction, transformation, linking, validation, review preparation, import, export, migration, publication, indexing, embedding, repair, or downstream use.

Agent provenance metadata SHOULD identify:

- agent involved;
- task performed;
- workflow involved where applicable;
- instruction context where appropriate;
- source material used where permitted;
- output generated;
- metadata changed;
- relationship changed;
- validation changed;
- privacy handling applied;
- review required;
- approval status where applicable.

Agent provenance metadata MUST preserve privacy boundaries.

Agent provenance MUST NOT expose restricted source material, restricted instructions, restricted actors, restricted workflows, restricted decisions, restricted identities, restricted timestamps, restricted credentials, or restricted content merely to improve traceability, validation, publication, export, migration, or downstream use.

### 20.10 Agent Metadata and Relationships

Agent activity MAY suggest, create, update, review, validate, migrate, or remove relationship metadata where permitted by governance, privacy classification, authority rules, validation expectations, and applicable workflow specifications.

Agent-suggested relationships MUST remain distinguishable from reviewed or approved governed relationships where that distinction affects interpretation, authority, privacy, validation, publication, export, migration, automation, or downstream use.

An agent-suggested relationship is not automatically valid.

An agent-created relationship is not automatically authoritative.

An agent-detected relationship is not automatically approved.

A relationship suggested by embeddings, similarity, search, graph analysis, source proximity, title similarity, tag similarity, or classification MUST NOT become governed relationship metadata without appropriate review where review is required.

Where an agent-generated relationship is accepted into governed metadata, the accepted relationship SHOULD preserve enough provenance for future review.

### 20.11 Agent Metadata and Lifecycle State

Agent metadata MAY support lifecycle classification or lifecycle transition preparation where permitted by a governed workflow or specification.

Agent-generated lifecycle metadata MUST remain distinguishable from human-approved or governance-approved lifecycle metadata when that distinction affects interpretation, authority, privacy, validation, publication, export, migration, compatibility, automation, or downstream use.

An agent MUST NOT silently approve, reject, supersede, deprecate, archive, publish, export, migrate, validate, or complete a lifecycle transition unless a governed workflow explicitly permits that behavior.

Agent lifecycle suggestions SHOULD preserve enough provenance for future review.

Where agent lifecycle metadata is accepted into governed metadata, the accepted metadata SHOULD preserve enough context to determine what was proposed, what was accepted, what was rejected, what was revised, and what review or approval occurred.

### 20.12 Agent Metadata and Authority

Agent metadata MUST remain distinguishable from authority metadata.

Agent output MUST NOT be treated as authoritative merely because an agent generated it.

Agent certainty is not authority.

Agent confidence is not authority.

Agent fluency is not authority.

Agent frequency of use is not authority.

Agent output may support authority review.

Agent output may not assign constitutional authority, standard authority, specification authority, operational authority, approval authority, privacy clearance, publication readiness, or unrestricted downstream authority unless a governed workflow explicitly permits that behavior.

Where agent activity affects authority, the authority scope, review basis, approval basis, lifecycle state, privacy boundaries, validation results, and limitations SHOULD remain explicit and reviewable.

### 20.13 Agent Metadata and Privacy

Agent metadata MUST preserve privacy boundaries.

Agent context may reveal restricted source material, restricted relationships, restricted provenance, restricted authority, restricted lifecycle state, restricted validation results, restricted migration behavior, restricted identities, restricted timestamps, restricted decisions, restricted workflows, restricted instructions, or restricted content.

Agent metadata MUST NOT expose restricted information merely to improve process traceability, validation, discovery, automation, publication, export, import, migration, compatibility, or downstream interpretation.

Agent access MUST respect privacy metadata.

An agent MUST NOT access, summarize, classify, embed, export, publish, migrate, infer relationships from, or generate derived metadata from restricted knowledge unless permitted by applicable privacy metadata and governed workflow rules.

Where agent usefulness and privacy conflict, privacy SHALL take precedence.

### 20.14 Agent Metadata and Validation

Agent metadata SHOULD support validation where agent activity affects compliance, interpretation, governance, privacy, lifecycle state, authority, publication, import, export, migration, archival handling, automation, agent access, or downstream use.

Agent validation MAY detect:

- missing agent metadata where required;
- ambiguous agent involvement;
- unsupported agent metadata;
- agent output presented as approved content;
- agent output presented as authoritative without review;
- agent output presented as validation success without validation;
- agent output exposing restricted metadata;
- agent access conflicting with privacy metadata;
- agent activity conflicting with lifecycle metadata;
- agent activity conflicting with authority metadata;
- agent activity conflicting with validation metadata;
- agent metadata dependent on hidden implementation state;
- agent metadata lost during import, export, or migration.

An agent validation result MUST remain distinguishable from agent output.

A validation result may identify an agent metadata issue.

A validation result MUST NOT silently approve agent output unless a governed workflow explicitly permits that behavior.

### 20.15 Agent Metadata During Import, Export, and Migration

Agent metadata SHOULD be preserved during import, export, and migration where agent context affects interpretation, provenance, lifecycle state, authority, privacy, validation, compatibility, publication, archival handling, automation, agent access, or downstream use.

Import, export, or migration processes MUST NOT replace governed agent metadata with folder placement, filename convention, tag convention, color convention, application state, user interface state, workflow memory, agent memory, or implementation inference unless a governed migration process explicitly maps agent metadata in a valid way.

Where agent metadata is transformed, mapped, omitted, redacted, deprecated, superseded, repaired, or partially preserved during migration, the process SHOULD preserve enough context for authorized future review.

A migration that loses meaning-critical agent metadata MUST NOT be represented as full compatibility.

An export that omits meaning-critical agent metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, publication, governance, automation, agent access, or downstream interpretation.

### 20.16 Agent Metadata and Implementation Independence

Agent metadata MUST remain implementation-independent where agent context affects governed meaning, validation, privacy, authority, lifecycle state, publication, import, export, migration, compatibility, automation, or downstream use.

An agent may operate inside a specific implementation.

An agent may use a specific tool.

An agent may depend on a specific workflow environment.

An agent may produce output through a specific user interface.

An agent may store intermediate state in a specific database.

None of those implementation mechanisms define standard agent metadata meaning unless a governed standard or specification explicitly defines that behavior.

A compliant implementation SHOULD preserve governed agent metadata across export, import, migration, backup, restoration, synchronization, validation, and implementation replacement.

Agent metadata that cannot be interpreted outside one implementation SHOULD NOT be used as the only source of meaning-critical context.

### 20.17 Agent Metadata Success

Agent metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, and implementations can determine:

- what agent acted;
- what entity the agent acted on;
- what agent scope applied;
- what task the agent performed;
- what workflow governed the agent activity where applicable;
- what instruction context applied where appropriate;
- what source material was used where permitted;
- what metadata was created;
- what metadata was changed;
- what relationship was suggested or created;
- what validation was suggested or performed;
- what output was generated;
- what uncertainty or limitation remains;
- what review remains required;
- what approval occurred where applicable;
- what privacy boundaries applied;
- what authority limits applied;
- what validation expectations applied;
- what compatibility limits remained;
- what downstream-use limits remained;
- whether agent metadata remains valid across implementation replacement.

Agent metadata is successful when agent context remains explicit, portable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent without being confused with Object Identity, knowledge meaning, lifecycle state, authority, privacy classification, validation state, provenance, compatibility metadata, workflow state, implementation state, user interface state, or agent output.

## 21. Metadata and Implementations

Metadata and implementations are closely connected because implementations represent, store, display, validate, index, synchronize, import, export, migrate, back up, restore, publish, route, automate, or otherwise process Knowledge Objects, Knowledge Records, metadata elements, relationships, source references, provenance, lifecycle states, authority assignments, privacy classifications, validation results, compatibility metadata, workflow outputs, agent outputs, and other governed entities.

Implementation metadata describes implementation-specific context without allowing an implementation to redefine standard meaning.

Implementation context includes what software, vault, database, file system, interface, plugin, workflow environment, agent system, storage layer, index, cache, synchronization process, backup process, API, or tool represented or processed governed metadata.

A compliant metadata model SHALL support implementation use without relying only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, graph display, search ranking, access-control assumptions, or undocumented implementation behavior.

Implementation metadata SHOULD help determine:

- what implementation represented the metadata;
- what implementation-specific metadata exists;
- what standard metadata exists;
- what implementation profile applies where applicable;
- what storage mechanism applies where applicable;
- what serialization mechanism applies where applicable;
- what index or cache exists where applicable;
- what synchronization behavior applies where applicable;
- what backup or restoration behavior applies where applicable;
- what plugin, tool, workflow, or agent dependency exists where applicable;
- what metadata is portable;
- what metadata is local-only;
- what metadata can be regenerated;
- what metadata must be preserved;
- what metadata may be ignored safely;
- what implementation-specific limitations exist;
- what migration or export risks exist.

Implementation metadata MUST remain distinguishable from Object Identity, Knowledge Object meaning, lifecycle state, authority, privacy classification, validation state, provenance, relationship metadata, compatibility metadata, workflow state, agent metadata, and user interface state.

KS-0003 defines implementation metadata at the conceptual standard level.

KS-0003 does not define exact implementation field names, exact implementation profiles, exact database schemas, exact file layouts, exact plugin behavior, exact API fields, exact cache structures, exact indexing structures, exact synchronization rules, exact backup formats, exact validation tooling, or exact implementation behavior.

A future implementation metadata specification MAY define those details.

### 21.1 Implementation Metadata Purpose

Implementation metadata exists to preserve portability, implementation independence, migration safety, validation reliability, compatibility review, operational clarity, synchronization safety, backup safety, restoration safety, indexing clarity, automation safety, agent safety, workflow safety, and downstream-use clarity.

Implementation metadata SHOULD support:

- implementation review;
- implementation-profile review;
- storage review;
- serialization review;
- indexing review;
- cache review;
- synchronization review;
- backup review;
- restoration review;
- import handling;
- export handling;
- migration handling;
- validation review;
- privacy review;
- compatibility review;
- agent handling;
- workflow handling;
- downstream-use decisions.

Implementation metadata MUST help prevent implementation-specific behavior from silently becoming standard meaning.

Implementation metadata MUST help prevent tool defaults, plugin fields, database identifiers, folder paths, filenames, graph views, user interface states, search indexes, embeddings, caches, workflow states, or agent states from being mistaken for governed metadata unless a governed standard or specification explicitly defines that meaning.

### 21.2 Implementation Scope

Implementation metadata SHOULD make clear what entity and what scope the implementation context applies to.

Implementation scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a privacy classification;
- a validation result;
- a compatibility statement;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a publication record;
- a serialization;
- an index;
- an embedding;
- a cache;
- a backup;
- a synchronized copy;
- a future governed entity.

Implementation scope MUST be explicit enough to prevent ambiguity where implementation behavior affects interpretation, Object Identity, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, publication, archival handling, automation, agent access, workflow behavior, import, export, migration, or downstream use.

An implementation may support one metadata category while not supporting another.

An implementation may preserve visible content while losing hidden metadata.

An implementation may support reading a record while not supporting full validation.

An implementation may support export while not supporting full re-import.

An implementation may preserve standard metadata while dropping local-only metadata.

### 21.3 Standard Metadata and Implementation Metadata Boundary

Standard metadata MUST remain distinguishable from implementation metadata.

Standard metadata is governed by The Brain Standard, applicable standards, specifications, profiles, workflows, or other approved authority.

Implementation metadata supports a specific software system, database, file system, vault, plugin, interface, workflow environment, agent system, index, cache, synchronization process, or tool.

Implementation metadata MAY be useful.

Implementation metadata MAY be necessary for a specific implementation.

Implementation metadata MUST NOT become required standard metadata merely because an implementation depends on it.

A database field, plugin property, application setting, file path, view state, graph location, cache key, embedding identifier, sync identifier, or internal identifier does not define standard metadata merely because it exists.

Implementation metadata becomes standard metadata only when its meaning is explicitly defined by a governed standard, specification, implementation profile, or other appropriate authority.

### 21.4 Implementation Profiles

An implementation profile MAY define how a specific implementation represents, stores, validates, displays, imports, exports, migrates, synchronizes, backs up, restores, or processes metadata.

Implementation profile metadata MAY identify:

- implementation name;
- implementation version where applicable;
- supported standard version;
- supported specification version;
- supported metadata profile;
- supported serialization profile;
- supported validation profile;
- supported import behavior;
- supported export behavior;
- supported migration behavior;
- unsupported metadata;
- local-only metadata;
- implementation-specific metadata;
- compatibility limitations;
- review requirements.

An implementation profile MUST remain subordinate to constitutional documents, standards, and applicable specifications.

An implementation profile MUST NOT override Object Identity, Knowledge Object meaning, required metadata, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, compatibility expectations, or governance.

Where implementation-profile behavior affects metadata interpretation, the behavior SHOULD be explicit, reviewable, and compatible with migration.

### 21.5 Storage Implementation Metadata

Storage implementation metadata MAY describe how metadata is stored in files, folders, repositories, vaults, databases, object stores, graph stores, indexes, sidecar files, embedded structures, APIs, backup packages, synchronized copies, or future storage mechanisms.

Storage implementation metadata SHOULD distinguish storage mechanism from standard meaning.

A storage location is not Object Identity.

A folder path is not lifecycle state.

A database table is not authority.

A graph edge is not automatically a governed relationship.

A file header is not automatically standard metadata unless its meaning is governed.

Storage implementation metadata MUST NOT become the only source of meaning-critical metadata unless a governed standard or specification explicitly defines that storage representation as authoritative for a defined scope.

Where storage changes affect metadata preservation, the change SHOULD remain traceable when it affects interpretation, validation, privacy, authority, compatibility, import, export, migration, or downstream use.

### 21.6 Serialization Implementation Metadata

Serialization implementation metadata MAY describe how metadata is represented in Markdown, front matter, structured fields, database rows, graph properties, API objects, sidecar files, embedded metadata structures, export packages, backup formats, or future serialization formats.

Serialization metadata SHOULD identify:

- source serialization format;
- target serialization format;
- serialization profile where applicable;
- supported metadata;
- unsupported metadata;
- transformed metadata;
- omitted metadata;
- redacted metadata;
- lossy transformations;
- validation results;
- review requirements.

Serialization MUST preserve governed metadata meaning.

A serialization that preserves visible text but loses Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, compatibility metadata, workflow metadata, or agent metadata MUST NOT be represented as fully compatible.

Serialization metadata MUST remain distinguishable from the metadata being serialized.

### 21.7 Database and Internal Identifier Metadata

A database-backed implementation MAY use internal identifiers, row identifiers, table identifiers, index keys, cache keys, query identifiers, object identifiers, transaction identifiers, or other implementation-specific identifiers.

Database and internal identifier metadata MUST remain distinguishable from Stable Object Identity.

A database identifier MUST NOT define Object Identity unless a governed identity specification explicitly defines that behavior.

An internal identifier MUST NOT define lifecycle state, authority, privacy classification, validation state, provenance, relationship meaning, source-reference meaning, workflow state, agent identity, or compatibility status by itself.

Where internal identifiers are used to support import, export, migration, synchronization, backup, restoration, validation, duplicate detection, or relationship repair, their implementation-specific role SHOULD be explicit.

Internal identifiers SHOULD be removable, replaceable, or mappable without losing standard meaning.

### 21.8 Indexing, Search, and Embedding Metadata

Implementations MAY create indexing, search, or embedding metadata to support retrieval, discovery, navigation, similarity detection, summarization, automation, agent use, or performance optimization.

Indexing, search, and embedding metadata MAY include:

- search indexes;
- keyword indexes;
- graph indexes;
- vector indexes;
- embedding identifiers;
- similarity signals;
- ranking signals;
- cache records;
- retrieval logs;
- generated snippets;
- future retrieval-support metadata.

Indexing, search, and embedding metadata MUST remain distinguishable from governed metadata.

A search result is not a relationship.

A ranking signal is not authority.

An embedding is not approval.

A similarity score is not Object Identity.

A generated snippet is not a complete Knowledge Record.

Indexing, search, and embedding metadata MUST preserve privacy boundaries.

Restricted knowledge MUST NOT be exposed merely because it improves search, retrieval, embeddings, summarization, graph navigation, automation, publication, export, migration, or agent usefulness.

### 21.9 User Interface Implementation Metadata

Implementations MAY create user interface metadata to support display, layout, navigation, filtering, sorting, dashboards, panels, colors, icons, view states, graph layouts, collapsed sections, selected items, or local presentation preferences.

User interface metadata MUST remain distinguishable from standard metadata.

User interface state MUST NOT define Knowledge Object meaning, Object Identity, lifecycle state, authority, privacy classification, validation state, provenance, relationships, source references, compatibility, workflow state, or agent output by itself.

A Knowledge Object or Knowledge Record SHOULD remain understandable when viewed outside the user interface that created or displayed it.

Where user interface metadata affects workflow routing, publication, export, privacy handling, validation, migration, or downstream use, the relevant governed metadata SHOULD remain explicit rather than depending only on interface state.

### 21.10 Plugin and Tool Metadata

Implementations MAY use plugins, tools, extensions, scripts, validators, importers, exporters, migration utilities, indexing tools, synchronization tools, backup tools, agent tools, or workflow tools.

Plugin and tool metadata MAY describe:

- tool used;
- plugin used;
- tool version where applicable;
- plugin version where applicable;
- configuration where permitted;
- supported metadata;
- unsupported metadata;
- generated metadata;
- transformed metadata;
- validation performed;
- warnings produced;
- limitations;
- review requirements.

Plugin and tool metadata MUST remain distinguishable from standard metadata.

A plugin field, tool default, generated label, automatic tag, validation message, graph edge, file movement, or transformation result MUST NOT become governed metadata unless accepted through a governed process where acceptance is required.

Where plugin or tool behavior changes meaning-critical metadata, the change SHOULD remain traceable and reviewable.

### 21.11 Synchronization, Backup, and Restoration Metadata

Implementations MAY create synchronization, backup, and restoration metadata to preserve, replicate, recover, or reconcile Knowledge Objects, Knowledge Records, metadata, source references, indexes, caches, workflows, agent outputs, and other governed entities.

Synchronization, backup, and restoration metadata SHOULD identify:

- what was synchronized;
- what was backed up;
- what was restored;
- what metadata was preserved;
- what metadata was omitted;
- what metadata was redacted;
- what metadata was transformed;
- what conflict occurred;
- what version or copy was selected;
- what validation occurred;
- what review remains required.

Synchronization, backup, and restoration metadata MUST preserve Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, compatibility metadata, workflow metadata, agent metadata, and source references where those affect governed meaning.

A restored copy MUST NOT silently replace current governed metadata unless a governed restoration workflow explicitly permits that behavior.

A synchronized copy MUST NOT weaken privacy classification, authority, lifecycle state, validation expectations, provenance, relationships, or compatibility.

### 21.12 Implementation Metadata and Privacy

Implementation metadata MUST preserve privacy boundaries.

Implementation context may reveal restricted source material, restricted relationships, restricted provenance, restricted authority, restricted lifecycle state, restricted validation results, restricted workflows, restricted agents, restricted indexes, restricted embeddings, restricted identities, restricted timestamps, restricted decisions, restricted storage locations, or restricted implementation behavior.

Implementation metadata MUST NOT expose restricted information merely to improve traceability, indexing, synchronization, backup, validation, automation, publication, export, import, migration, compatibility, or downstream interpretation.

Where implementation usefulness and privacy conflict, privacy SHALL take precedence.

Where implementation metadata is redacted or omitted for privacy reasons, the representation SHOULD preserve enough permitted context for authorized review without exposing restricted information.

### 21.13 Implementation Metadata and Validation

Implementation metadata SHOULD support validation where implementation behavior affects compliance, interpretation, governance, privacy, lifecycle state, authority, publication, import, export, migration, archival handling, automation, agent access, or downstream use.

Implementation validation MAY detect:

- missing implementation metadata where required by a profile;
- ambiguous implementation-specific metadata;
- unsupported implementation metadata;
- hidden implementation dependency;
- standard metadata stored only in hidden implementation state;
- implementation metadata presented as standard metadata;
- internal identifier presented as Object Identity;
- user interface state presented as governed metadata;
- plugin output presented as approved metadata;
- search ranking presented as authority;
- graph proximity presented as relationship meaning;
- embedding metadata exposed improperly;
- implementation metadata conflicting with privacy metadata;
- implementation metadata lost during import, export, or migration.

An implementation validation result MUST remain distinguishable from implementation state.

A validation result may identify an implementation metadata issue.

A validation result MUST NOT silently convert implementation metadata into standard metadata unless a governed process explicitly permits that behavior.

### 21.14 Implementation Metadata During Import, Export, and Migration

Implementation metadata SHOULD be preserved during import, export, and migration where implementation context affects interpretation, usability, validation, privacy, authority, publication, archival handling, automation, agent access, compatibility, or downstream use.

Import, export, or migration processes MUST NOT replace governed standard metadata with implementation metadata unless a governed migration process explicitly maps the metadata in a valid way.

Where implementation metadata is transformed, mapped, omitted, redacted, deprecated, superseded, repaired, regenerated, or partially preserved during migration, the process SHOULD preserve enough context for authorized future review.

A migration that loses meaning-critical implementation context MUST NOT be represented as full compatibility when that implementation context affects standard meaning, validation, privacy, authority, publication, automation, or downstream use.

An export that omits meaning-critical implementation metadata SHOULD disclose the omission when the omission affects reuse, validation, import, interoperability, publication, governance, automation, agent access, or downstream interpretation.

### 21.15 Implementation Metadata and Agents

Agents MAY interact with implementation metadata when permitted by governance, privacy classification, authority rules, validation expectations, workflow rules, and applicable implementation profiles.

Agent use of implementation metadata MUST remain distinguishable from governed knowledge interpretation.

An agent MUST NOT treat implementation state, user interface state, search ranking, graph layout, plugin output, cache state, index state, database internals, synchronization state, backup state, or tool output as governed metadata unless a governed standard, specification, workflow, or implementation profile explicitly defines that behavior.

Agent-generated interpretation of implementation metadata SHOULD remain reviewable where it affects Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, publication, import, export, migration, automation, or downstream use.

Agent access to implementation metadata MUST preserve privacy boundaries.

### 21.16 Implementation Metadata Success

Implementation metadata is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, and implementations can determine:

- what implementation represented the metadata;
- what implementation-specific metadata exists;
- what standard metadata exists;
- what implementation profile applies where applicable;
- what storage mechanism applies where applicable;
- what serialization mechanism applies where applicable;
- what index or cache exists where applicable;
- what synchronization behavior applies where applicable;
- what backup or restoration behavior applies where applicable;
- what plugin, tool, workflow, or agent dependency exists where applicable;
- what metadata is portable;
- what metadata is local-only;
- what metadata can be regenerated;
- what metadata must be preserved;
- what metadata may be ignored safely;
- what implementation-specific limitations exist;
- what migration or export risks exist;
- whether implementation metadata remains valid across implementation replacement.

Implementation metadata is successful when implementation context remains explicit, portable where required, reviewable, privacy-respecting, validatable, compatible, and subordinate to standard meaning without being confused with Object Identity, knowledge meaning, lifecycle state, authority, privacy classification, validation state, provenance, relationship metadata, compatibility metadata, workflow state, agent metadata, user interface state, storage behavior, plugin behavior, database internals, search ranking, graph display, index state, cache state, or hidden implementation behavior.

## 22. Metadata Governance and Evolution

Metadata governance and evolution are required because metadata definitions, categories, requirements, profiles, validation expectations, compatibility expectations, implementation profiles, workflows, agents, privacy rules, authority rules, import behavior, export behavior, migration behavior, and future specifications may change over time.

Metadata governance defines how metadata meaning is introduced, revised, deprecated, superseded, validated, migrated, extended, or retired without weakening Object Identity, Knowledge Object meaning, provenance, relationships, lifecycle state, authority, privacy classification, compatibility, implementation independence, or long-term maintainability.

Metadata evolution MUST be governed because metadata affects how humans, agents, workflows, validators, storage systems, and implementations interpret and process knowledge.

A compliant metadata model SHALL support metadata evolution without relying only on hidden application state, tool defaults, plugin behavior, folder placement, filename convention, tag convention, user interface state, database internals, workflow memory, agent memory, implementation convenience, or undocumented operational habits.

Metadata governance SHOULD help determine:

- what metadata rule changed;
- why the metadata rule changed;
- what authority approved the change;
- what scope the change applies to;
- what metadata category is affected;
- what Knowledge Objects or Knowledge Records are affected;
- what validation expectations are affected;
- what privacy expectations are affected;
- what authority expectations are affected;
- what compatibility expectations are affected;
- what import, export, or migration behavior is affected;
- what implementation profiles are affected;
- what workflows are affected;
- what agents are affected;
- what transition guidance is required;
- what migration guidance is required;
- what review remains required.

Metadata governance MUST preserve the authority hierarchy defined by the constitutional and standard documents.

Metadata evolution MUST NOT allow local convenience, implementation behavior, agent output, workflow habit, plugin defaults, database fields, or user interface state to redefine governed metadata meaning without appropriate governance.

KS-0003 defines metadata governance and evolution at the conceptual standard level.

KS-0003 does not define exact governance workflow fields, exact change-request formats, exact voting rules, exact review templates, exact registry schemas, exact deprecation schedules, exact migration procedures, exact validation tooling, or exact implementation behavior.

A future metadata governance specification MAY define those details.

### 22.1 Metadata Governance Purpose

Metadata governance exists to preserve stable meaning, controlled evolution, compatibility, validation reliability, privacy safety, authority clarity, implementation independence, migration safety, profile consistency, workflow safety, agent safety, and long-term maintainability.

Metadata governance SHOULD support:

- metadata change review;
- metadata rule approval;
- metadata rule rejection;
- metadata rule deprecation;
- metadata rule supersession;
- metadata category review;
- metadata profile review;
- validation-rule review;
- privacy-rule review;
- authority-rule review;
- compatibility review;
- implementation-profile review;
- import review;
- export review;
- migration review;
- workflow review;
- agent review;
- downstream-use decisions.

Metadata governance MUST prevent uncontrolled metadata growth from creating unnecessary cognitive burden, hidden requirements, implementation lock-in, validation ambiguity, privacy exposure, authority confusion, migration failure, or inconsistent interpretation.

Metadata governance MUST also prevent useful metadata from being discarded without review where that metadata affects governed meaning, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, workflows, agents, implementations, publication, archival handling, or downstream use.

### 22.2 Metadata Governance Scope

Metadata governance MAY apply to:

- metadata categories;
- required metadata;
- recommended metadata;
- optional metadata;
- metadata role boundaries;
- metadata definitions;
- metadata profiles;
- metadata field names where governed by future specifications;
- metadata allowed values where governed by future specifications;
- validation expectations;
- compatibility expectations;
- privacy classifications;
- authority levels;
- lifecycle states;
- relationship metadata;
- provenance metadata;
- import metadata;
- export metadata;
- migration metadata;
- workflow metadata;
- agent metadata;
- implementation metadata;
- serialization profiles;
- implementation profiles;
- future governed metadata entities.

Governance scope MUST be explicit enough to prevent confusion over whether a metadata change applies broadly across The Brain Standard or only within a narrower specification, implementation profile, workflow, agent, object type, record type, repository, vault, or operational context.

A metadata convention may be local.

A metadata convention may be experimental.

A metadata convention may be implementation-specific.

A metadata convention may be recommended.

A metadata convention may be required.

Those states MUST remain distinguishable.

A local or experimental convention MUST NOT be treated as standard metadata merely because it is useful, common, automated, indexed, displayed, imported, exported, or generated by an agent.

### 22.3 Metadata Change Control

Metadata changes SHOULD be controlled when they affect governed meaning, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, workflows, agents, implementations, publication, archival handling, or downstream use.

Metadata change control MAY apply to:

- adding metadata;
- removing metadata;
- renaming metadata;
- redefining metadata;
- narrowing metadata scope;
- broadening metadata scope;
- changing required metadata;
- changing recommended metadata;
- changing optional metadata;
- changing validation expectations;
- changing compatibility expectations;
- changing privacy handling;
- changing authority interpretation;
- changing lifecycle interpretation;
- changing migration behavior;
- changing implementation-profile behavior.

A metadata change SHOULD preserve enough context to determine:

- what changed;
- why it changed;
- who or what proposed the change where applicable;
- what authority approved the change where applicable;
- what standard or specification was affected;
- what compatibility impact exists;
- what migration impact exists;
- what validation impact exists;
- what privacy impact exists;
- what downstream review remains required.

Metadata changes MUST NOT silently redefine existing Knowledge Objects or Knowledge Records unless a governed migration, revision, or compatibility process explicitly permits that behavior.

### 22.4 Required Metadata Governance

Changes to Required Metadata require careful governance because Required Metadata defines the minimum metadata meaning needed for standard-level interpretation and use.

Required Metadata SHOULD change only when the change materially improves:

- Object Identity preservation;
- interpretation;
- provenance;
- relationship clarity;
- lifecycle handling;
- authority handling;
- privacy protection;
- validation reliability;
- compatibility;
- import safety;
- export safety;
- migration safety;
- workflow safety;
- agent safety;
- implementation independence;
- long-term maintainability.

Adding Required Metadata increases burden.

Removing Required Metadata may weaken interpretation.

Renaming Required Metadata may create migration complexity.

Redefining Required Metadata may create compatibility risk.

A change to Required Metadata SHOULD include compatibility review and migration guidance where applicable.

A future metadata specification MAY define exact required fields and exact migration procedures, but those details MUST remain consistent with the conceptual requirements of KS-0003.

### 22.5 Recommended and Optional Metadata Governance

Recommended Metadata and Optional Metadata MAY evolve more flexibly than Required Metadata, but their evolution still requires review where changes affect governed interpretation, validation, privacy, compatibility, publication, import, export, migration, workflows, agents, implementations, or downstream use.

Recommended Metadata MAY be promoted to Required Metadata when governance determines that it is necessary for standard-level validity.

Optional Metadata MAY be promoted to Recommended Metadata when governance determines that it provides durable value across multiple contexts.

Optional Metadata MAY be promoted directly to Required Metadata only where governance determines that the metadata is necessary for identity, interpretation, provenance, privacy, validation, compatibility, migration, or long-term maintainability.

Recommended Metadata MAY be demoted to Optional Metadata when it no longer provides enough value to justify its maintenance burden.

Optional Metadata MAY be deprecated, superseded, archived, removed, or left implementation-specific when it does not affect governed meaning.

Promotion, demotion, deprecation, or supersession SHOULD preserve compatibility guidance where existing records depend on the affected metadata.

### 22.6 Metadata Extension Governance

Metadata extensions MAY be introduced by future standards, specifications, implementation profiles, workflows, agents, object-type profiles, record-type profiles, validation profiles, import profiles, export profiles, migration profiles, or operational documents.

Metadata extensions MUST preserve the boundaries established by KS-0003.

A metadata extension MUST NOT silently redefine:

- Object Identity;
- Knowledge Object meaning;
- source distinction;
- provenance;
- relationships;
- lifecycle state;
- authority;
- privacy classification;
- validation expectations;
- compatibility expectations;
- import behavior;
- export behavior;
- migration behavior;
- governance interpretation.

A metadata extension SHOULD identify:

- extension purpose;
- extension scope;
- governing authority;
- affected metadata category;
- required metadata where applicable;
- recommended metadata where applicable;
- optional metadata where applicable;
- validation expectations;
- privacy expectations;
- compatibility expectations;
- migration expectations;
- implementation expectations;
- review requirements.

Metadata extensions MAY be useful without becoming standard metadata.

A metadata extension becomes standard metadata only when its meaning is approved through the appropriate governance process.

### 22.7 Metadata Profile Governance

Metadata profiles MAY define narrower metadata requirements for specific object types, record types, workflows, agents, implementations, validation contexts, publication contexts, import contexts, export contexts, migration contexts, archival contexts, or operational contexts.

Metadata profiles MUST remain subordinate to constitutional documents, KS-0001, KS-0002, KS-0003, and any applicable higher-authority standards.

A metadata profile MAY add requirements within its governed scope.

A metadata profile MAY refine interpretation within its governed scope.

A metadata profile MAY define exact fields, allowed values, serialization behavior, validation behavior, or migration behavior where authorized by a future specification.

A metadata profile MUST NOT weaken Required Metadata unless a higher-authority governed specification explicitly permits a narrower exception.

A metadata profile SHOULD make clear:

- what profile applies;
- what profile version applies;
- what scope applies;
- what metadata is required;
- what metadata is recommended;
- what metadata is optional;
- what validation profile applies;
- what privacy rules apply;
- what compatibility rules apply;
- what migration guidance applies.

Metadata profile changes SHOULD include compatibility and migration review where existing objects or records depend on the profile.

### 22.8 Deprecation and Supersession Governance

Metadata may become deprecated or superseded when it is replaced, discouraged, unsafe for new use, incompatible with later standards, redundant, ambiguous, implementation-specific, privacy-risky, or no longer useful.

Deprecation governance SHOULD identify:

- what metadata is deprecated;
- why it is deprecated;
- what replacement exists where applicable;
- what scope deprecation applies to;
- whether existing records may retain the metadata;
- whether new records may use the metadata;
- what validation warning applies where applicable;
- what migration guidance applies where applicable;
- what compatibility limits remain.

Supersession governance SHOULD identify:

- what metadata is superseded;
- what metadata supersedes it;
- what direction the supersession relationship has;
- what authority approved the supersession;
- what migration guidance applies;
- what compatibility guidance applies;
- what historical context should be preserved.

Deprecated or superseded metadata MUST NOT be treated as current merely because it remains stored, indexed, visible, linked, exported, imported, migrated, displayed, or generated by an agent.

Deprecation and supersession metadata SHOULD remain traceable where it affects interpretation, validation, relationships, authority, privacy, provenance, publication, import, export, migration, automation, or downstream use.

### 22.9 Metadata Conflict Governance

Metadata conflicts SHOULD be reviewed when two or more metadata elements, standards, specifications, profiles, workflows, agents, implementations, imports, exports, migrations, validations, or operational conventions provide inconsistent meaning.

Metadata conflicts MAY involve:

- Object Identity conflicts;
- provenance conflicts;
- relationship conflicts;
- lifecycle conflicts;
- authority conflicts;
- privacy conflicts;
- validation conflicts;
- compatibility conflicts;
- import conflicts;
- export conflicts;
- migration conflicts;
- workflow conflicts;
- agent conflicts;
- implementation-profile conflicts;
- serialization conflicts.

Conflict governance SHOULD preserve the authority hierarchy.

Where metadata conflicts with a constitutional document, the constitutional document SHALL take precedence unless formally revised through governance.

Where metadata conflicts with KS-0001, KS-0002, or KS-0003, the conflict SHOULD be resolved according to document authority, scope, and governance review.

Where privacy and operational convenience conflict, privacy SHALL take precedence.

Where implementation convenience and standard meaning conflict, standard meaning SHALL take precedence.

Where agent output and governed metadata conflict, governed metadata SHALL take precedence unless a governed review process accepts the agent output.

### 22.10 Metadata Review and Approval Governance

Metadata review and approval SHOULD be required where metadata changes affect governed interpretation, Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, publication, workflows, agents, implementations, or downstream use.

Metadata review MAY include:

- human review;
- governance review;
- privacy review;
- authority review;
- validation review;
- compatibility review;
- migration review;
- implementation review;
- workflow review;
- agent-output review;
- source-review where applicable;
- future governed review types.

Metadata approval SHOULD identify approval scope.

Approval may apply broadly or narrowly.

Approval for one implementation does not automatically approve standard-level metadata.

Approval for internal use does not automatically approve publication.

Approval for structure does not automatically approve authority.

Approval for migration does not automatically approve compatibility.

Approval for agent use does not automatically approve public release.

Review and approval metadata SHOULD preserve enough provenance to support future review where approval affects interpretation, validation, authority, privacy, compatibility, publication, import, export, migration, automation, or downstream use.

### 22.11 Metadata Registry Governance

A future metadata registry MAY define governed metadata names, categories, roles, descriptions, requirements, allowed values, profiles, validation rules, compatibility notes, deprecation state, supersession state, migration mappings, and implementation guidance.

If a metadata registry exists, it SHOULD remain subordinate to applicable constitutional documents, standards, and specifications.

A metadata registry MAY support:

- metadata discovery;
- metadata consistency;
- metadata validation;
- profile management;
- compatibility review;
- migration planning;
- deprecation tracking;
- supersession tracking;
- implementation guidance;
- workflow guidance;
- agent guidance.

A metadata registry MUST NOT redefine standard meaning unless it is itself governed by an appropriate standard or specification.

A registry entry MUST distinguish required metadata, recommended metadata, optional metadata, derived metadata, temporary metadata, workflow metadata, agent metadata, implementation metadata, and deprecated metadata where that distinction affects interpretation or validation.

Where a registry entry changes, the change SHOULD preserve compatibility guidance and migration guidance where applicable.

### 22.12 Metadata Governance and Privacy

Metadata governance MUST preserve privacy boundaries.

Governance processes may reveal restricted source material, restricted relationships, restricted provenance, restricted authority, restricted lifecycle state, restricted validation results, restricted workflows, restricted agents, restricted implementation behavior, restricted identities, restricted timestamps, restricted decisions, or restricted content.

Metadata governance MUST NOT expose restricted information merely to improve review, validation, migration, compatibility, automation, publication, export, implementation guidance, agent usefulness, or downstream interpretation.

Where governance usefulness and privacy conflict, privacy SHALL take precedence.

Governance records SHOULD preserve enough permitted context for authorized review without exposing restricted information.

A privacy-sensitive metadata change SHOULD receive privacy review where the change affects access, visibility, handling, publication, export, indexing, synchronization, backup, agent access, workflow routing, migration, or downstream use.

### 22.13 Metadata Governance and Validation

Metadata governance SHOULD support validation by defining which metadata rules, profiles, expectations, and compatibility requirements apply.

Validation governance MAY define:

- what metadata is required;
- what metadata is recommended;
- what metadata is optional;
- what validation profile applies;
- what validation result states exist;
- what warnings exist;
- what errors exist;
- what repair guidance applies;
- what review is required;
- what migration validation applies;
- what compatibility validation applies.

Validation rules MUST remain subordinate to governed metadata meaning.

A validator MUST NOT redefine metadata merely because it can check a pattern.

A validation profile MUST NOT turn Optional Metadata into Required Metadata outside its governed scope.

A validation result MUST NOT silently approve, reject, publish, export, migrate, classify, deprecate, supersede, or assign authority unless a governed workflow explicitly permits that behavior.

Where metadata governance changes validation expectations, compatibility and migration impacts SHOULD be reviewed.

### 22.14 Metadata Governance During Import, Export, and Migration

Metadata governance SHOULD define how metadata changes are handled during import, export, and migration.

Import, export, and migration governance SHOULD identify:

- what metadata must be preserved;
- what metadata may be transformed;
- what metadata may be omitted;
- what metadata may be redacted;
- what metadata must be mapped;
- what metadata is deprecated;
- what metadata is superseded;
- what validation is required;
- what compatibility limits apply;
- what review remains required.

Migration governance MUST NOT hide loss of meaning-critical metadata.

A migration process MUST NOT represent moved knowledge as fully compatible when Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, compatibility metadata, workflow metadata, agent metadata, or other meaning-critical metadata has been lost, corrupted, hidden, redacted without permitted disclosure, or mapped ambiguously.

Import, export, and migration governance SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, and implementations to determine whether moved knowledge remains usable.

### 22.15 Metadata Governance and Agents

Agents MAY assist metadata governance by detecting inconsistencies, drafting change proposals, identifying deprecated metadata, suggesting migration mappings, preparing validation reports, finding privacy risks, identifying compatibility risks, or preparing review summaries.

Agent participation in metadata governance MUST remain distinguishable from human review, governance approval, validation success, privacy clearance, authority assignment, publication readiness, and compatibility approval.

An agent-generated metadata governance recommendation is not automatically approved.

An agent-generated migration mapping is not automatically valid.

An agent-generated validation report is not automatically compliance.

An agent-generated deprecation recommendation is not automatically deprecation.

An agent MUST NOT silently approve, reject, revise, deprecate, supersede, migrate, validate, publish, export, or assign authority to metadata rules unless a governed workflow explicitly permits that behavior.

Where agent governance output is accepted into governed metadata decisions, the accepted decision SHOULD preserve enough provenance for future review.

### 22.16 Metadata Governance Success

Metadata governance and evolution are successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, and implementations can determine:

- what metadata rule exists;
- what authority governs the metadata rule;
- what scope the metadata rule applies to;
- whether the metadata is required, recommended, optional, derived, temporary, workflow-related, agent-related, implementation-specific, deprecated, or superseded;
- what metadata changes occurred;
- why metadata changes occurred;
- what review occurred;
- what approval occurred;
- what privacy boundaries apply;
- what validation expectations apply;
- what compatibility expectations apply;
- what migration guidance applies;
- what implementation-profile guidance applies;
- what workflow guidance applies;
- what agent guidance applies;
- what downstream-use limits remain;
- whether metadata governance remains valid across implementation replacement.

Metadata governance and evolution are successful when metadata can change over time without losing meaning, weakening Object Identity, hiding provenance, breaking relationships, confusing lifecycle state, misassigning authority, exposing restricted information, invalidating compatibility, creating migration ambiguity, creating hidden implementation dependency, or allowing workflows, agents, tools, plugins, databases, user interfaces, or operational habits to redefine The Brain Standard by accident.

## 23. Metadata Conformance

Metadata conformance defines what it means for Knowledge Objects, Knowledge Records, metadata elements, relationships, source references, provenance records, lifecycle states, authority assignments, privacy classifications, validation results, compatibility statements, workflow outputs, agent outputs, implementation profiles, imports, exports, migrations, publications, indexes, backups, synchronized copies, and other governed entities to satisfy KS-0003.

Conformance exists to make metadata reviewable, portable, validatable, privacy-respecting, compatible, implementation-independent, and usable by future humans, agents, workflows, validators, storage systems, and implementations.

A compliant metadata model SHALL preserve governed metadata meaning even when exact field names, schemas, serializations, storage systems, user interfaces, plugins, databases, workflows, agents, validators, and implementations differ.

Metadata conformance MUST be evaluated according to meaning, role, scope, authority, privacy, validation expectations, compatibility expectations, and governance context.

Metadata conformance MUST NOT depend only on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, search ranking, graph display, access-control assumptions, or undocumented implementation behavior.

Metadata conformance SHOULD help determine:

- whether Required Metadata is present or supported;
- whether Recommended Metadata is handled appropriately;
- whether Optional Metadata remains subordinate to governed metadata;
- whether metadata roles are distinguishable;
- whether Object Identity boundaries are preserved;
- whether provenance is sufficient;
- whether relationships are explicit and reviewable;
- whether lifecycle state is clear;
- whether authority scope is clear;
- whether privacy classification is preserved;
- whether validation expectations are supported;
- whether compatibility expectations are supported;
- whether import, export, and migration metadata is preserved;
- whether workflow metadata remains distinguishable from governed state;
- whether agent metadata remains reviewable;
- whether implementation metadata remains subordinate to standard meaning;
- whether metadata governance is respected;
- whether implementation replacement remains possible.

KS-0003 defines metadata conformance at the conceptual standard level.

KS-0003 does not define exact conformance test suites, exact machine-readable schemas, exact validator behavior, exact certification processes, exact report formats, exact database rules, exact serialization profiles, exact implementation profiles, or exact operational procedures.

A future conformance specification MAY define those details.

### 23.1 Metadata Conformance Purpose

Metadata conformance exists to preserve trust, portability, reviewability, implementation independence, validation reliability, compatibility, governance, privacy safety, authority clarity, workflow safety, agent safety, migration safety, publication safety, archival usability, and downstream-use clarity.

Metadata conformance SHOULD support:

- human review;
- agent review;
- workflow review;
- validator review;
- implementation review;
- privacy review;
- authority review;
- compatibility review;
- import review;
- export review;
- migration review;
- publication review;
- archival review;
- profile review;
- governance review;
- downstream-use decisions.

Metadata conformance MUST help prevent incomplete, ambiguous, private, unreviewed, lossy, implementation-specific, agent-generated, workflow-generated, migrated, deprecated, superseded, or invalid metadata from being mistaken for complete governed metadata.

Metadata conformance MUST preserve meaning before convenience.

### 23.2 Conformance Scope

Metadata conformance MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a metadata element;
- a metadata category;
- a relationship;
- a source reference;
- a provenance element;
- a lifecycle state;
- an authority assignment;
- a privacy classification;
- a validation result;
- a compatibility statement;
- a workflow output;
- an agent output;
- an implementation profile;
- an import record;
- an export record;
- a migration record;
- a publication record;
- an index;
- an embedding;
- a cache;
- a backup;
- a synchronized copy;
- a future governed entity.

Conformance scope MUST be explicit enough to prevent confusion about what has passed, what has failed, what remains unreviewed, what requires repair, and what is outside the checked scope.

A Knowledge Object may conform at the identity level while a specific Knowledge Record fails provenance conformance.

A record may conform structurally while failing privacy conformance.

A relationship may conform syntactically while remaining unapproved.

An export may conform to a public-release profile while being incompatible with full re-import.

An implementation may support standard metadata while failing to preserve implementation-specific optional metadata.

### 23.3 Required Metadata Conformance

A Knowledge Object or Knowledge Record SHALL conform to Required Metadata expectations when the applicable standard or specification requires that metadata for validity.

Required Metadata conformance SHOULD verify that required metadata meaning is present, explicit, portable, inspectable, validatable, privacy-respecting, and not dependent only on hidden implementation state.

Required Metadata conformance SHOULD check whether the object or record includes or supports:

- stable Object Identity or reference to stable Object Identity;
- title or human-readable label;
- object type or record type where applicable;
- provenance;
- lifecycle state;
- privacy classification;
- authority level where applicable;
- source-reference metadata where applicable;
- relationship metadata where applicable;
- validation metadata or validation expectations where applicable;
- creation context where applicable;
- revision context where applicable;
- compatibility metadata where applicable.

A record MUST NOT be treated as conformant merely because a template contains fields.

The metadata must preserve governed meaning.

A record MUST NOT be treated as nonconformant merely because its field names differ from a future implementation unless the applicable specification requires exact field names for that scope.

### 23.4 Recommended Metadata Conformance

Recommended Metadata conformance SHOULD determine whether recommended metadata is included where practical and whether its absence materially reduces interpretation, reviewability, portability, automation reliability, validation, discovery, interoperability, migration, or long-term maintenance.

Recommended Metadata absence SHOULD NOT make a Knowledge Object or Knowledge Record invalid unless a future governed specification, workflow, implementation profile, object-type rule, or validation profile requires that metadata for a defined scope.

Recommended Metadata conformance SHOULD evaluate whether recommended metadata:

- improves interpretation;
- improves reviewability;
- improves source traceability;
- improves relationship clarity;
- improves provenance clarity;
- improves lifecycle handling;
- improves authority handling;
- improves privacy handling;
- improves validation quality;
- improves discovery;
- improves migration behavior;
- improves compatibility;
- improves long-term maintainability.

Recommended Metadata MUST NOT create hidden requirements.

Where Recommended Metadata is omitted, the omission SHOULD be noted only when the omission affects interpretation, validation, privacy, compatibility, publication, import, export, migration, automation, or downstream use.

### 23.5 Optional Metadata Conformance

Optional Metadata conformance SHOULD determine whether optional metadata remains useful, subordinate, distinguishable, and safe.

Optional Metadata MAY be present without being required.

Optional Metadata MAY be absent without causing nonconformance unless a future governed specification, workflow, implementation profile, object-type rule, or validation profile requires it for a defined scope.

Optional Metadata conformance SHOULD verify that optional metadata does not silently change:

- Object Identity;
- Knowledge Object meaning;
- source distinction;
- provenance;
- relationships;
- lifecycle state;
- authority;
- privacy classification;
- validation expectations;
- compatibility expectations;
- import behavior;
- export behavior;
- migration behavior;
- governance interpretation.

Optional Metadata SHOULD remain removable, ignorable, replaceable, or migratable without losing standard meaning unless a governed process promotes that metadata into a higher role.

Optional Metadata that affects privacy, publication, export, indexing, synchronization, backup, agent access, automation, or downstream use SHOULD require review before unrestricted use.

### 23.6 Role Boundary Conformance

Metadata conformance MUST preserve role boundaries.

Role boundary conformance SHOULD verify that metadata remains distinguishable from:

- Object Identity;
- Knowledge Object content;
- Knowledge Record content;
- filenames;
- folder paths;
- tags;
- user interface state;
- database fields;
- application behavior;
- plugin behavior;
- workflow state;
- agent output;
- validation state;
- privacy handling;
- authority;
- implementation profiles;
- storage behavior;
- presentation behavior;
- temporary processing state.

A metadata element MAY serve multiple roles.

Where metadata serves multiple roles, the controlling role SHOULD be explicit enough to support governed interpretation, validation, privacy handling, import, export, migration, compatibility, publication, automation, and downstream use.

Role boundary confusion SHOULD be treated as a conformance issue where confusion affects governed meaning.

### 23.7 Identity Conformance

Metadata conformance MUST preserve the Object Identity boundaries defined by KS-0002.

Identity conformance SHOULD verify that Stable Object Identity remains distinguishable from:

- title;
- alias;
- filename;
- folder path;
- tag;
- category;
- source identifier;
- external identifier;
- temporary identifier;
- database identifier;
- application identifier;
- workflow identifier;
- agent-generated label;
- implementation-specific identifier;
- index identifier;
- cache identifier.

A record MUST NOT be considered identity-conformant if stable identity depends only on filename, folder path, storage location, display title, tag, database identifier, application identifier, workflow identifier, agent label, or hidden implementation state.

Where identity is missing, ambiguous, duplicated, corrupted, conflicting, deprecated, redirected, superseded, or dependent on unstable identifiers, the condition SHOULD be detectable during validation or review.

A migration, export, import, backup, restoration, synchronization, or implementation replacement that loses stable Object Identity MUST NOT be represented as fully conformant.

### 23.8 Provenance and Relationship Conformance

Metadata conformance SHOULD verify that provenance and relationship metadata remain sufficient for interpretation, reviewability, validation, privacy handling, authority assessment, compatibility, import, export, migration, publication, automation, and downstream use.

Provenance conformance SHOULD determine whether future authorized humans, agents, workflows, validators, storage systems, and implementations can determine:

- where knowledge came from;
- what source material supports it where applicable;
- who or what created it where applicable;
- who or what modified it where applicable;
- what workflow affected it where applicable;
- what agent affected it where applicable;
- what transformation occurred where applicable;
- what import, export, or migration process affected it where applicable;
- what validation occurred where applicable;
- what review or approval occurred where applicable.

Relationship conformance SHOULD determine whether future authorized humans, agents, workflows, validators, storage systems, and implementations can determine:

- what entities are connected;
- what relationship type applies where applicable;
- what direction applies where applicable;
- what source or evidence supports the relationship where applicable;
- what provenance applies to the relationship where applicable;
- what lifecycle state applies to the relationship where applicable;
- what authority applies to the relationship where applicable;
- what privacy boundaries apply to the relationship;
- what validation expectations apply to the relationship.

A record that preserves visible content but loses meaning-critical provenance or relationship metadata SHOULD NOT be treated as fully conformant.

### 23.9 Lifecycle and Authority Conformance

Metadata conformance SHOULD verify that lifecycle state and authority metadata remain explicit, distinguishable, reviewable, validatable, compatible, and privacy-respecting.

Lifecycle conformance SHOULD determine whether the applicable lifecycle state is clear and whether it applies to the correct entity.

Lifecycle state MUST remain distinguishable from authority, validation, privacy, workflow state, implementation state, and user interface state.

A record MUST NOT be treated as approved merely because it exists, is stored, is indexed, is linked, appears in an implementation, appears in a graph, appears in search, was imported, was migrated, or was generated by an agent.

Authority conformance SHOULD determine whether authority scope, governance source, review basis, approval basis, lifecycle effects, privacy boundaries, validation expectations, and reliance limits are explicit where authority affects interpretation, governance, publication, automation, export, migration, or downstream use.

Authority metadata MUST remain distinguishable from truth, confidence, popularity, usefulness, validation success, lifecycle state, privacy classification, source reliability, workflow completion, implementation state, user interface state, search ranking, graph centrality, and agent certainty.

### 23.10 Privacy Conformance

Metadata conformance MUST preserve privacy boundaries.

Privacy conformance SHOULD determine whether privacy classification is explicit enough to support access, visibility, handling, routing, indexing, synchronization, backup, publication, export, migration, workflow behavior, agent access, automation, and downstream-use decisions.

Privacy conformance SHOULD detect:

- missing privacy classification where required;
- ambiguous privacy classification;
- unsupported privacy classification;
- conflicting privacy classifications;
- restricted knowledge exposed in public metadata;
- restricted source references exposed improperly;
- restricted provenance exposed improperly;
- restricted relationships exposed improperly;
- restricted authority metadata exposed improperly;
- restricted lifecycle metadata exposed improperly;
- restricted validation output exposed improperly;
- restricted agent output exposed improperly;
- privacy metadata lost during import, export, migration, backup, synchronization, or implementation replacement.

A metadata representation MUST NOT be considered privacy-conformant if it exposes restricted information merely to improve traceability, validation, automation, search, publication, export, migration, compatibility, implementation convenience, agent usefulness, or downstream interpretation.

Where privacy usefulness and metadata usefulness conflict, privacy SHALL take precedence.

### 23.11 Validation and Compatibility Conformance

Metadata conformance SHOULD support validation and compatibility checks without confusing validation results with factual truth, authority, approval, privacy clearance, lifecycle state, publication readiness, workflow completion, implementation success, or agent certainty.

Validation conformance SHOULD determine whether validation metadata identifies:

- what was validated;
- what validation scope applied;
- what standard or specification applied;
- what validation profile applied where applicable;
- what result occurred;
- what errors were found;
- what warnings were found;
- what repair remains required;
- what review remains required.

Compatibility conformance SHOULD determine whether compatibility metadata identifies:

- what standard version applies;
- what specification version applies where applicable;
- what metadata profile applies where applicable;
- what serialization profile applies where applicable;
- what implementation profile applies where applicable;
- whether the representation is fully compatible;
- whether the representation is partially compatible;
- whether the representation is lossy;
- whether meaning-critical metadata has been preserved, transformed, omitted, or redacted;
- whether deprecated or superseded metadata remains;
- what review, repair, validation, or migration remains required.

A record MUST NOT be treated as fully conformant where compatibility metadata hides loss of Object Identity, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, source references, workflow context, agent context, implementation context, or other meaning-critical metadata.

### 23.12 Import, Export, and Migration Conformance

Import, export, and migration conformance SHOULD determine whether movement preserved governed metadata meaning.

Movement conformance SHOULD verify whether future authorized humans, agents, workflows, validators, storage systems, and implementations can determine:

- what movement occurred;
- what entity was moved;
- what source system or representation was involved;
- what target system or representation was involved;
- what metadata was preserved;
- what metadata was transformed;
- what metadata was mapped;
- what metadata was omitted;
- what metadata was redacted;
- what metadata was repaired;
- what metadata was deprecated;
- what metadata was superseded;
- what validation occurred;
- what review remains required;
- what compatibility limits remain.

A movement process MUST NOT be treated as conformant where it silently loses, corrupts, hides, redacts without permitted disclosure, ambiguously maps, or makes implementation-dependent any meaning-critical metadata.

A moved representation MAY be useful while still being partially conformant, lossy, restricted, staged, quarantined, needs review, needs repair, or limited to a defined use.

### 23.13 Workflow, Agent, and Implementation Conformance

Workflow conformance SHOULD determine whether workflow metadata remains explicit, traceable, distinguishable from lifecycle state, and subordinate to governed meaning.

Workflow completion MUST NOT be treated as approval, validation success, privacy clearance, authority assignment, publication readiness, or compatibility unless a governed workflow or specification explicitly defines that behavior.

Agent conformance SHOULD determine whether agent involvement remains explicit, reviewable, privacy-respecting, distinguishable from human review, and subordinate to governed authority.

Agent output MUST NOT be treated as approved, authoritative, valid, privacy-cleared, publication-ready, or compatible merely because an agent generated it.

Implementation conformance SHOULD determine whether implementation metadata remains distinguishable from standard metadata and whether governed metadata remains portable across implementation replacement.

Implementation behavior MUST NOT redefine metadata meaning unless a governed standard, specification, workflow, or implementation profile explicitly defines that behavior.

A tool, plugin, database, file system, user interface, workflow engine, agent system, search index, graph view, cache, or embedding system MUST NOT become the hidden source of standard meaning.

### 23.14 Conformance Failure and Repair

A conformance failure occurs when metadata does not satisfy applicable requirements, role boundaries, validation expectations, privacy expectations, compatibility expectations, governance expectations, or implementation-independence expectations.

Conformance failures MAY include:

- missing Required Metadata;
- ambiguous metadata;
- malformed metadata;
- unsupported metadata;
- conflicting metadata;
- hidden implementation dependency;
- Object Identity confusion;
- provenance loss;
- relationship loss;
- lifecycle ambiguity;
- authority ambiguity;
- privacy exposure;
- validation ambiguity;
- compatibility loss;
- import loss;
- export loss;
- migration loss;
- workflow confusion;
- agent-output confusion;
- implementation-specific meaning;
- deprecated metadata treated as current;
- superseded metadata treated as current.

Conformance failure SHOULD result in review, repair, restriction, quarantine, warning, migration guidance, deprecation, supersession, rejection, or another governed response appropriate to the failure scope.

A conformance failure MUST NOT be silently ignored where it affects Object Identity, knowledge meaning, provenance, relationships, lifecycle state, authority, privacy classification, validation, compatibility, publication, import, export, migration, automation, or downstream use.

Repair actions SHOULD preserve provenance and reviewability where repair affects governed meaning.

### 23.15 Conformance and Governance

Metadata conformance MUST remain subordinate to governance.

A conformance rule MUST NOT override constitutional documents, KS-0001, KS-0002, KS-0003, or higher-authority standards.

A conformance rule MAY be narrowed by a future governed specification, metadata profile, validation profile, implementation profile, workflow, or operational document only within its authorized scope.

A conformance claim SHOULD identify the standard, specification, profile, validation scope, implementation scope, and review context that support the claim where those details affect interpretation.

A conformance claim MUST NOT imply broader validity than its scope supports.

Conformance for one implementation does not automatically mean conformance for all implementations.

Conformance for reading does not automatically mean conformance for export.

Conformance for export does not automatically mean conformance for re-import.

Conformance for structure does not automatically mean conformance for authority, privacy, publication, compatibility, automation, or downstream use.

### 23.16 Metadata Conformance Success

Metadata conformance is successful when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, and implementations can determine:

- what conformance scope was evaluated;
- what standard or specification applied;
- what profile applied where applicable;
- what Required Metadata was present or supported;
- what Recommended Metadata was included or omitted;
- what Optional Metadata exists;
- what metadata roles were distinguishable;
- whether Object Identity was preserved;
- whether provenance was sufficient;
- whether relationships were explicit and reviewable;
- whether lifecycle state was clear;
- whether authority scope was clear;
- whether privacy classification was preserved;
- whether validation expectations were supported;
- whether compatibility expectations were supported;
- whether import, export, and migration metadata was preserved;
- whether workflow metadata remained distinguishable from governed state;
- whether agent metadata remained reviewable;
- whether implementation metadata remained subordinate to standard meaning;
- whether metadata governance was respected;
- what failures occurred;
- what repair remains required;
- what review remains required;
- what downstream-use limits remain;
- whether conformance remains valid across implementation replacement.

Metadata conformance is successful when metadata remains explicit, portable, reviewable, privacy-respecting, validatable, compatible, governed, and implementation-independent without hiding loss, ambiguity, role confusion, privacy exposure, authority confusion, validation ambiguity, compatibility ambiguity, workflow confusion, agent-output confusion, or implementation-specific dependency.

## 24. Metadata Standard Success Criteria

Metadata Standard Success Criteria define when KS-0003 has fulfilled its purpose within The Brain Standard.

KS-0003 is successful when metadata remains explicit, portable, reviewable, privacy-respecting, validatable, compatible, governed, and implementation-independent across time, tools, workflows, agents, storage systems, and implementations.

KS-0003 is successful when Knowledge Objects and Knowledge Records can be interpreted without relying on hidden application state, folder placement, filename convention, tag convention, color convention, user interface state, plugin behavior, database internals, workflow memory, agent memory, search ranking, graph display, access-control assumptions, or undocumented implementation behavior.

KS-0003 is successful when metadata supports knowledge meaning without replacing knowledge content.

KS-0003 is successful when metadata supports Object Identity without becoming confused with Object Identity.

KS-0003 is successful when metadata supports relationships, provenance, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, workflows, agents, implementations, governance, and conformance without allowing any of those concerns to redefine standard meaning by accident.

Metadata Standard Success Criteria SHOULD help determine whether:

- metadata meaning is explicit;
- metadata roles are distinguishable;
- Required Metadata is preserved;
- Recommended Metadata adds durable value;
- Optional Metadata remains subordinate;
- Object Identity boundaries are protected;
- provenance remains traceable;
- relationships remain meaningful;
- lifecycle state remains clear;
- authority scope remains explicit;
- privacy classification is preserved;
- validation expectations are supported;
- compatibility expectations are supported;
- import, export, and migration preserve meaning;
- workflow metadata remains reviewable;
- agent metadata remains reviewable;
- implementation metadata remains subordinate to standard meaning;
- governance controls metadata evolution;
- conformance can be evaluated;
- implementation replacement remains possible.

KS-0003 defines success criteria at the conceptual standard level.

KS-0003 does not define exact certification methods, exact test suites, exact scoring methods, exact validation tools, exact report formats, exact implementation checklists, exact operational procedures, or exact governance templates.

A future conformance, validation, or implementation specification MAY define those details.

### 24.1 Human Interpretability Success

KS-0003 is successful when future humans can understand what metadata exists, what it means, what role it serves, what entity it applies to, and how it should be handled.

Human interpretability success SHOULD include the ability to determine:

- which Knowledge Object or Knowledge Record is being described;
- what Required Metadata is present;
- what Recommended Metadata is present;
- what Optional Metadata is present;
- what metadata affects meaning;
- what metadata affects privacy;
- what metadata affects authority;
- what metadata affects validation;
- what metadata affects compatibility;
- what metadata affects import, export, or migration;
- what metadata is implementation-specific;
- what metadata requires review.

Metadata fails human interpretability when a future human cannot determine whether metadata is standard, optional, temporary, derived, workflow-related, agent-generated, implementation-specific, deprecated, superseded, private, authoritative, valid, compatible, or safe for downstream use.

### 24.2 AI Interpretability Success

KS-0003 is successful when future agents can interpret metadata reliably without becoming unreviewable authorities over the knowledge.

AI interpretability success SHOULD include the ability for agents to determine:

- what metadata is governed;
- what metadata is required;
- what metadata is recommended;
- what metadata is optional;
- what metadata is private or restricted;
- what metadata may be used for reasoning;
- what metadata requires human review;
- what metadata is agent-generated;
- what metadata is workflow-generated;
- what metadata is implementation-specific;
- what metadata is deprecated or superseded;
- what metadata cannot be trusted without review.

An agent MUST NOT treat metadata as authoritative, public, valid, approved, compatible, or unrestricted merely because it is present, indexed, embedded, frequently used, highly connected, or easy to parse.

KS-0003 succeeds when agents can assist review, validation, migration, discovery, and maintenance while remaining subordinate to governance, privacy, authority, validation, and human review requirements.

### 24.3 Portability Success

KS-0003 is successful when metadata can move across files, repositories, vaults, databases, applications, workflows, agents, validators, storage systems, and implementations without losing governed meaning.

Portability success SHOULD include preservation of:

- Object Identity;
- title or human-readable label;
- provenance;
- relationships;
- lifecycle state;
- authority;
- privacy classification;
- validation expectations;
- compatibility context;
- source references;
- import context;
- export context;
- migration context;
- workflow context where applicable;
- agent context where applicable;
- implementation context where applicable.

Metadata portability does not require every implementation to preserve every local-only or optional metadata element.

Metadata portability does require that loss, omission, redaction, transformation, mapping, deprecation, supersession, or implementation dependency be detectable where it affects governed meaning, privacy, validation, compatibility, or downstream use.

### 24.4 Validation Success

KS-0003 is successful when metadata can be validated for structure, meaning, role boundaries, privacy, authority, provenance, relationships, lifecycle state, compatibility, import behavior, export behavior, migration behavior, workflow behavior, agent behavior, implementation behavior, governance, and conformance.

Validation success SHOULD include the ability to detect:

- missing Required Metadata;
- malformed metadata;
- ambiguous metadata;
- conflicting metadata;
- unsupported metadata;
- hidden implementation dependency;
- Object Identity confusion;
- provenance loss;
- relationship loss;
- lifecycle ambiguity;
- authority ambiguity;
- privacy exposure;
- compatibility loss;
- workflow confusion;
- agent-output confusion;
- implementation-specific meaning;
- deprecated metadata treated as current;
- superseded metadata treated as current.

Validation success does not mean factual truth.

Validation success does not mean authority.

Validation success does not mean approval.

Validation success does not mean publication readiness.

Validation success does not mean privacy clearance.

Validation success means the applicable metadata expectations were checked within a defined scope.

### 24.5 Privacy Success

KS-0003 is successful when metadata preserves privacy boundaries across access, visibility, handling, routing, indexing, synchronization, backup, publication, import, export, migration, workflow activity, agent activity, validation, implementation behavior, and downstream use.

Privacy success SHOULD include the ability to determine:

- what privacy classification applies;
- what entity the classification applies to;
- what access is permitted;
- what publication is permitted;
- what export is permitted;
- what indexing is permitted;
- what synchronization is permitted;
- what backup is permitted;
- what agent access is permitted;
- what derived metadata must inherit restrictions;
- what relationships or provenance require restricted handling;
- what review remains required.

KS-0003 fails privacy success if metadata exposes restricted knowledge merely to improve traceability, validation, discovery, automation, search, publication, export, migration, compatibility, implementation convenience, or agent usefulness.

Where metadata usefulness and privacy conflict, privacy SHALL take precedence.

### 24.6 Governance Success

KS-0003 is successful when metadata can evolve without losing meaning, weakening Object Identity, hiding provenance, breaking relationships, confusing lifecycle state, misassigning authority, exposing restricted information, invalidating compatibility, creating migration ambiguity, or creating hidden implementation dependency.

Governance success SHOULD include the ability to determine:

- what metadata rule exists;
- what authority governs the rule;
- what scope the rule applies to;
- whether metadata is required, recommended, optional, deprecated, or superseded;
- what changes occurred;
- why changes occurred;
- what review occurred;
- what approval occurred;
- what compatibility impact exists;
- what migration guidance applies;
- what validation expectations apply;
- what downstream-use limits remain.

Metadata governance succeeds when metadata can change through controlled review rather than through accidental tool behavior, plugin defaults, workflow habits, agent output, database structure, file naming, folder placement, user interface state, or operational convenience.

### 24.7 Implementation Independence Success

KS-0003 is successful when governed metadata meaning survives implementation replacement.

Implementation independence success SHOULD include the ability to interpret metadata outside the original:

- software application;
- vault;
- database;
- file system;
- user interface;
- plugin;
- workflow engine;
- agent system;
- search index;
- graph view;
- cache;
- synchronization process;
- backup process;
- API;
- tool.

An implementation may store, display, index, cache, synchronize, validate, import, export, or migrate metadata.

An implementation MUST NOT become the hidden source of standard metadata meaning unless a governed standard, specification, workflow, or implementation profile explicitly defines that behavior.

KS-0003 succeeds when implementation-specific metadata remains useful without becoming accidental architecture.

### 24.8 Import, Export, and Migration Success

KS-0003 is successful when import, export, and migration processes preserve governed metadata meaning or clearly disclose permitted loss, transformation, omission, redaction, mapping, repair, deprecation, supersession, or compatibility limitation.

Import, export, and migration success SHOULD include the ability to determine:

- what moved;
- where it came from;
- where it went;
- what standard version applied;
- what specification version applied where applicable;
- what metadata profile applied where applicable;
- what serialization profile applied where applicable;
- what metadata was preserved;
- what metadata was transformed;
- what metadata was omitted;
- what metadata was redacted;
- what metadata was mapped;
- what metadata was repaired;
- what validation occurred;
- what review remains required;
- what compatibility limits remain.

A movement process fails KS-0003 success when it silently loses meaning-critical metadata or represents a lossy movement as fully compatible.

A moved representation may remain useful while still requiring review, repair, restriction, or compatibility limitation.

### 24.9 Workflow and Agent Success

KS-0003 is successful when workflows and agents can use metadata safely without becoming hidden authorities over knowledge.

Workflow success SHOULD include the ability to determine:

- what workflow acted;
- what triggered the workflow;
- what entity was affected;
- what metadata changed;
- what review occurred;
- what approval occurred;
- what validation occurred;
- what repair occurred;
- what remains pending;
- what downstream-use limits remain.

Agent success SHOULD include the ability to determine:

- what agent acted;
- what task was performed;
- what source material was used where permitted;
- what output was generated;
- what metadata was suggested or changed;
- what uncertainty remains;
- what review is required;
- what approval occurred where applicable;
- what privacy boundaries applied;
- what authority limits applied.

Workflow completion MUST NOT be confused with approval, validation success, privacy clearance, publication readiness, compatibility, or authority unless a governed workflow explicitly defines that behavior.

Agent output MUST NOT be confused with approved, authoritative, valid, public, privacy-cleared, publication-ready, or compatible metadata merely because an agent generated it.

### 24.10 Conformance Success

KS-0003 is successful when metadata conformance can be evaluated within a clear scope.

Conformance success SHOULD include the ability to determine:

- what standard or specification was applied;
- what profile was applied where applicable;
- what entity was evaluated;
- what metadata was present;
- what metadata was missing;
- what metadata was valid;
- what metadata was ambiguous;
- what metadata was incompatible;
- what metadata failed privacy expectations;
- what metadata failed authority expectations;
- what metadata failed compatibility expectations;
- what repair remains required;
- what review remains required;
- what downstream-use limits remain.

A conformance claim MUST NOT imply broader validity than its scope supports.

Conformance for one implementation does not automatically mean conformance for all implementations.

Conformance for structure does not automatically mean conformance for authority, privacy, publication, compatibility, automation, or downstream use.

### 24.11 Long-Term Maintainability Success

KS-0003 is successful when metadata remains maintainable across years of revision, expansion, import, export, migration, implementation replacement, workflow changes, agent changes, validation changes, and governance changes.

Long-term maintainability success SHOULD include:

- minimal unnecessary metadata burden;
- clear Required Metadata;
- useful Recommended Metadata;
- safe Optional Metadata;
- explicit role boundaries;
- stable identity support;
- traceable provenance;
- reviewable relationships;
- clear lifecycle state;
- explicit authority;
- preserved privacy;
- validatable structure;
- compatible evolution;
- governed extensions;
- repairable failures;
- portable representation;
- implementation independence.

KS-0003 fails long-term maintainability when metadata becomes excessive, unclear, hidden, redundant, implementation-specific, privacy-risky, difficult to validate, difficult to migrate, or dependent on undocumented operational habits.

Metadata should make knowledge easier to preserve, not harder to maintain.

### 24.12 Metadata Standard Success

KS-0003 succeeds when future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, archival processes, governance processes, and implementations can determine:

- what metadata exists;
- what the metadata means;
- what role the metadata serves;
- what entity the metadata applies to;
- whether the metadata is required, recommended, optional, derived, temporary, workflow-related, agent-related, implementation-specific, deprecated, or superseded;
- whether the metadata affects Object Identity;
- whether the metadata affects Knowledge Object meaning;
- whether the metadata affects provenance;
- whether the metadata affects relationships;
- whether the metadata affects lifecycle state;
- whether the metadata affects authority;
- whether the metadata affects privacy classification;
- whether the metadata affects validation;
- whether the metadata affects compatibility;
- whether the metadata affects import, export, or migration;
- whether the metadata affects workflow behavior;
- whether the metadata affects agent behavior;
- whether the metadata affects implementation behavior;
- whether the metadata affects governance;
- whether the metadata affects conformance;
- whether the metadata can be ignored safely;
- whether the metadata must be preserved;
- whether the metadata requires review;
- whether the metadata requires repair;
- whether the metadata remains valid across implementation replacement.

KS-0003 succeeds when metadata remains explicit, portable, inspectable, reviewable, privacy-respecting, validatable, compatible, governed, maintainable, and implementation-independent.

KS-0003 succeeds when metadata supports The Brain Standard without becoming a hidden source of architecture by accident.
