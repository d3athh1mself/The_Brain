# KS-0004 — Relationship Standard

Document ID: KS-0004
Title: Relationship Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-26
Last Updated: 2026-06-26
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.4 — Relationship Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and relationship rules are interpreted within KS-0004.

Where conflicts arise between relationships, relationship participants, relationship types, relationship direction, relationship strength or confidence, relationship provenance, relationship lifecycle state, relationship authority, relationship privacy, relationship validation, relationship compatibility, inferred relationships, agent-generated relationships, workflow-generated relationships, implementation behavior, storage behavior, migration behavior, import behavior, export behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0004 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0004 extends KS-0001 by defining standard-level relationship behavior for Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, and other governed entities.

KS-0004 depends on KS-0002 because relationships rely on stable Object Identity when they connect, reference, compare, validate, migrate, import, export, or preserve Knowledge Objects.

KS-0004 depends on KS-0003 because relationship meaning may be expressed, described, validated, reviewed, migrated, imported, exported, or governed through metadata.

If KS-0004 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

If KS-0004 appears to conflict with KS-0001, the conflict SHOULD be resolved by preserving the Knowledge Object Model defined in KS-0001 while applying KS-0004 as the more specific standard for relationship behavior.

If KS-0004 appears to conflict with KS-0002, the conflict SHOULD be resolved by preserving stable Object Identity while applying KS-0004 as the more specific standard for relationship meaning, interpretation, review, validation, and compatibility.

If KS-0004 appears to conflict with KS-0003, the conflict SHOULD be resolved by preserving metadata role boundaries while applying KS-0004 as the more specific standard for relationship behavior.

KS-0004 defines relationships at the conceptual standard level.

KS-0004 does not define exact graph schemas, database structures, metadata field names, API behavior, backlink behavior, Obsidian-specific behavior, vector-search behavior, visualization behavior, implementation-specific relationship storage, or implementation-specific relationship traversal.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation profiles, validation specifications, relationship vocabularies, graph specifications, and operational documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, Object Identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to source material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, or other artifacts used as evidence, input, or reference material.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, or relationship information associated with a Knowledge Object, Knowledge Record, relationship, or governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Relationship Participant refers to any governed entity that takes part in a relationship.
- Origin Participant refers to the participant from which a directional relationship is expressed.
- Target Participant refers to the participant to which a directional relationship is expressed.
- Non-Directional Relationship refers to a relationship where direction does not materially affect meaning.
- Directional Relationship refers to a relationship where direction materially affects meaning.
- Relationship Type refers to the conceptual kind of connection expressed by a relationship.
- Relationship Context refers to information that explains why a relationship exists, how it should be interpreted, or when it matters.
- Relationship Strength refers to the relative importance, closeness, dependency, or significance of a relationship where that distinction affects interpretation.
- Relationship Confidence refers to the degree of certainty, review status, evidence support, or reliability associated with a relationship where that distinction affects interpretation.
- Relationship Provenance refers to information identifying the origin, source, reasoning, creator, agent, workflow, import, migration, validation, or evidence associated with a relationship.
- Relationship Lifecycle State refers to the current governed state of a relationship, such as proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or a future governed lifecycle state.
- Relationship Authority refers to the governance weight, review status, or interpretive authority assigned to a relationship.
- Relationship Privacy refers to the privacy classification, visibility boundary, access expectation, or handling rule associated with a relationship.
- Relationship Validation refers to the process of checking whether a relationship satisfies the identity, participant, type, direction, provenance, lifecycle, privacy, authority, compatibility, and implementation-independence expectations defined by the relevant standards or specifications.
- Relationship Compatibility refers to whether a relationship remains meaningful, portable, reviewable, privacy-respecting, and interpretable across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.
- Explicit Relationship refers to a relationship that is directly represented, declared, or recorded in a reviewable form.
- Inferred Relationship refers to a relationship proposed or derived from evidence, metadata, content similarity, source material, agent analysis, workflow activity, validation output, or implementation signals but not yet necessarily approved.
- Agent-Generated Relationship refers to a relationship created, proposed, modified, classified, validated, or enriched by an agent.
- Workflow-Generated Relationship refers to a relationship created, proposed, modified, classified, validated, or enriched through a governed workflow.
- Human-Reviewed Relationship refers to a relationship that has been inspected, confirmed, corrected, rejected, or approved by a human according to the applicable governance or workflow expectations.
- Implementation-Specific Link refers to a link, edge, backlink, pointer, database relation, graph connection, plugin relationship, search association, interface connection, or application-specific reference created or used by a particular implementation.
- Migration refers to movement from one storage system, implementation, representation, schema, vault, repository, database, file format, workflow environment, or tool environment to another.
- Import refers to the process of bringing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, or external content into a compliant environment.
- Export refers to the process of producing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, or external content from a compliant environment for use elsewhere.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, agent, workflow, migration, import, export, or evidence associated with a Knowledge Object, Knowledge Record, relationship, or governed entity.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, relationship, or governed entity.
- Privacy Classification refers to explicit metadata describing permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.
- Authority Level refers to the governance weight, review status, or interpretive authority assigned to a document, Knowledge Object, Knowledge Record, relationship, source, or decision.
- Validation refers to the process of checking whether a Knowledge Object, Knowledge Record, relationship, or governed entity satisfies the applicable standards, specifications, metadata expectations, provenance expectations, lifecycle expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0004 is to define how relationships work across The Brain Standard.

KS-0001 establishes that Knowledge Objects and Knowledge Records SHALL support relationships where relationships are needed to preserve meaning, context, provenance, dependency, hierarchy, sequence, evidence, supersession, derivation, governance, or validation.

KS-0004 defines the standard-level behavior required to create, interpret, preserve, validate, review, migrate, import, export, govern, and maintain those relationships.

Relationships exist so that knowledge does not remain isolated.

A Knowledge Object gains meaning from its identity, metadata, content, provenance, lifecycle state, authority, privacy classification, validation expectations, and relationships to other governed entities.

KS-0004 exists to prevent relationship confusion.

Relationship confusion occurs when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, or implementations cannot reliably determine:

- what entities are connected;
- what kind of connection exists;
- whether the relationship has direction;
- why the relationship exists;
- what source, evidence, reasoning, workflow, agent, or human review supports the relationship;
- whether the relationship is explicit, inferred, proposed, reviewed, approved, deprecated, superseded, rejected, or invalid;
- whether the relationship affects meaning, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, or implementation behavior.

KS-0004 defines relationship behavior for:

- relationship purpose;
- relationship definition;
- relationship participants;
- relationship types;
- relationship direction;
- relationship strength or confidence;
- relationship provenance;
- relationship lifecycle state;
- relationship authority;
- relationship privacy;
- relationship validation;
- relationship compatibility;
- relationship behavior during import, export, and migration;
- inferred relationships;
- agent-generated relationships;
- workflow-generated relationships;
- implementation boundaries;
- relationship governance;
- relationship conformance;
- relationship success criteria.

KS-0004 does not define exact relationship field names, exact Markdown front matter syntax, exact graph schemas, exact database tables, exact API structures, exact backlink behavior, exact query behavior, exact visualization behavior, exact vector-search behavior, exact implementation-specific link storage, exact relationship-type vocabularies, exact relationship identifiers, exact cardinality rules, or exact validation syntax.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, relationship vocabularies, graph specifications, and operational guides.

KS-0004 defines relationships at the standard level.

A future specification MAY define exact relationship vocabularies, relationship identifiers, relationship records, relationship metadata fields, relationship serialization formats, relationship validation rules, directionality rules, cardinality rules, confidence values, lifecycle values, privacy handling rules, inferred relationship rules, graph structures, import formats, export formats, or migration mappings.

Such specifications are valid only when they preserve the relationship behavior defined by KS-0004.

The primary purpose of KS-0004 is to ensure that relationships remain explicit, interpretable, portable, traceable, reviewable, privacy-respecting, validatable, and implementation-independent across time, tools, storage systems, workflows, agents, validators, and implementations.

KS-0004 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine:

- what relationship exists;
- which entities participate in the relationship;
- whether each participant is a Knowledge Object, Knowledge Record, Source Material, standard, decision, workflow, implementation, identifier, or other governed entity;
- what kind of relationship is being expressed;
- whether direction affects the meaning of the relationship;
- whether relationship strength or confidence affects interpretation;
- what provenance supports the relationship;
- whether the relationship is human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, validated, reviewed, or approved;
- whether the relationship affects Object Identity, metadata, provenance, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, or governance;
- whether the relationship remains valid when objects are renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, reindexed, summarized, translated, validated, processed by an agent, processed by a workflow, or accessed through a different implementation;
- whether the relationship can be preserved without relying on hidden application state, folder proximity, filename similarity, tag coincidence, search ranking, graph layout, backlink behavior, vector similarity, or implementation-specific behavior.

## 2. Relationship to Prior Standards

KS-0004 is subordinate to and derived from the constitutional foundation of The Brain Standard.

KS-0004 depends on:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- KS-0001 — Knowledge Object Model;
- KS-0002 — Object Identity Standard;
- KS-0003 — Metadata Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

KS-0004 applies that purpose by defining relationship behavior that remains portable, interpretable, reviewable, and independent of any single storage system, application, graph engine, backlink system, database, workflow engine, agent framework, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

KS-0004 applies those principles by requiring relationships to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- source distinction;
- provenance;
- privacy boundaries;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability.

TB-0002 establishes the layered architecture of The Brain Standard.

KS-0004 belongs to Layer 1 — Universal Knowledge Standard.

Because relationships are part of knowledge meaning, KS-0004 defines relationship behavior independently of storage systems, user interfaces, graph databases, backlinks, tags, folders, search indexes, visualization tools, vector indexes, workflow engines, agent systems, and implementations.

Layer 2 storage standards depend on KS-0004 because storage must preserve relationships without defining their meaning.

Layer 3 agent standards depend on KS-0004 because agents must understand when they are reading, proposing, modifying, validating, rejecting, or preserving relationships.

Layer 4 workflow standards depend on KS-0004 because workflows may create, review, validate, approve, reject, migrate, import, export, or supersede relationships.

Layer 5 implementation documents depend on KS-0004 because implementations must create, read, preserve, display, migrate, export, import, validate, and synchronize relationships without redefining relationship meaning through implementation-specific behavior.

TB-0003 establishes the governance model for The Brain Standard.

KS-0004 follows the document authority hierarchy defined by TB-0003. As a standard-level document, KS-0004 has high authority within its scope but remains subordinate to constitutional documents.

KS-0001 defines the foundational Knowledge Object Model.

KS-0004 does not replace the Knowledge Object Model.

KS-0004 refines one part of that model: relationships between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, and other governed entities.

In practical terms:

- KS-0001 answers: What is a Knowledge Object?
- KS-0001 answers: What is a Knowledge Record?
- KS-0001 answers: Why must Knowledge Objects support relationships?
- KS-0004 answers: How must relationships behave?
- KS-0004 answers: What makes a relationship explicit, interpretable, portable, and reviewable?
- KS-0004 answers: How should relationship participants, types, direction, confidence, provenance, lifecycle state, authority, privacy, validation, and compatibility be handled?
- KS-0004 answers: How should inferred, agent-generated, workflow-generated, imported, exported, and migrated relationships be treated?

KS-0002 defines Object Identity.

KS-0004 depends on KS-0002 because relationships require stable identity when they connect Knowledge Objects or Knowledge Records.

A relationship SHOULD reference or resolve to stable Object Identity where Object Identity is applicable.

A relationship MUST NOT depend only on filename, folder path, storage location, display title, backlink behavior, graph layout, search result, tag coincidence, vector similarity, or implementation-specific identifier when that relationship affects meaning, provenance, lifecycle state, authority, privacy classification, validation, import, export, migration, or compatibility.

A Knowledge Object SHOULD remain connected to its valid relationships when it is renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, reindexed, summarized, translated, validated, processed by an agent, processed by a workflow, or accessed through a different implementation.

KS-0003 defines metadata behavior.

KS-0004 depends on KS-0003 because relationships may be expressed, described, classified, validated, reviewed, migrated, imported, exported, or governed through metadata.

Relationship metadata MAY describe:

- relationship type;
- relationship participants;
- relationship direction;
- relationship context;
- relationship strength;
- relationship confidence;
- relationship provenance;
- relationship lifecycle state;
- relationship authority;
- relationship privacy;
- relationship validation state;
- relationship compatibility expectations.

Relationship metadata MUST remain distinguishable from Object Identity, source identity, implementation-specific identifiers, storage paths, tags, search indexes, graph layout, interface state, or hidden application behavior.

KS-0004 preserves the following KS-0001 rules:

- Relationships SHOULD be explicit when they affect interpretation, validation, provenance, lifecycle state, authority, privacy, workflow behavior, source traceability, or long-term maintenance.
- A relationship MUST NOT depend only on folder proximity, filename similarity, tag coincidence, search ranking, visual placement, application state, or agent inference when that relationship affects meaning.
- Relationships SHOULD preserve direction where direction affects meaning.
- Relationships SHOULD preserve type where type affects meaning.
- Relationships SHOULD preserve context where context affects interpretation.
- Agent-created or workflow-created relationships SHOULD remain reviewable when they affect interpretation, provenance, authority, privacy, lifecycle state, validation, publication, or downstream use.
- Relationships SHOULD preserve privacy boundaries.
- Relationships SHOULD support portability.

KS-0004 preserves the following KS-0002 rules:

- Relationships between Knowledge Objects depend on stable Object Identity.
- Relationships SHOULD refer to stable Object Identity rather than relying only on title, filename, folder path, storage location, URL, application-specific identifier, search result, index entry, or display state.
- Identity changes SHOULD preserve, review, update, redirect, or historically retain affected relationships.
- A relationship MUST NOT silently point to the wrong Knowledge Object because of an identity change.

KS-0004 preserves the following KS-0003 rules:

- Metadata may describe relationship meaning and context.
- Relationship-related metadata SHOULD remain explicit when it affects interpretation.
- Metadata MUST NOT create hidden implementation assumptions.
- Metadata SHOULD support validation, migration, import, export, privacy, authority, lifecycle state, provenance, compatibility, agents, workflows, and implementations.

KS-0004 is successful when it extends the prior standards into a clear relationship model without weakening Object Identity, metadata role boundaries, provenance, lifecycle meaning, authority expectations, privacy boundaries, validation expectations, implementation independence, or practical daily usability.

## 3. Relationship Definition

A Relationship is an explicit connection between two or more governed entities within The Brain Standard.

A Relationship exists to preserve meaning, context, dependency, provenance, hierarchy, sequence, evidence, derivation, supersession, reviewability, validation, navigation, governance, or compatibility.

A Relationship MAY connect:

- Knowledge Objects;
- Knowledge Records;
- Source Material;
- standards;
- specifications;
- decisions;
- ADRs;
- RFCs;
- workflows;
- agents;
- implementations;
- identifiers;
- metadata records;
- validation records;
- migration records;
- import records;
- export records;
- other governed entities.

A Relationship SHALL be explicit when it affects knowledge meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

A Relationship MUST NOT depend only on hidden application state, folder proximity, filename similarity, tag coincidence, search ranking, graph layout, backlink behavior, vector similarity, cached index behavior, user interface placement, or implementation-specific behavior when the relationship affects meaning.

Those signals MAY assist discovery, recommendation, navigation, search, visualization, indexing, duplicate detection, or implementation convenience.

They MUST NOT replace explicit relationship meaning.

A Relationship SHOULD identify or resolve to its participants clearly enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what entities are connected.

A Relationship SHOULD preserve its type where type affects meaning.

A Relationship SHOULD preserve its direction where direction affects meaning.

A Relationship SHOULD preserve its context where context affects interpretation.

A Relationship SHOULD preserve provenance where the origin, evidence, creator, agent, workflow, import process, migration process, validation process, or reasoning behind the relationship affects interpretation.

A Relationship SHOULD preserve lifecycle state where review, approval, rejection, deprecation, supersession, archival, or validation affects how the relationship should be used.

A Relationship SHOULD preserve authority where governance weight, review status, or interpretive authority affects downstream use.

A Relationship MUST preserve privacy boundaries.

A Relationship MUST NOT expose restricted knowledge merely because it connects to a less restricted object, source, workflow, implementation, or record.

Where a Relationship crosses privacy boundaries, the Relationship SHOULD be handled conservatively and according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

A Relationship SHOULD support validation.

A validator SHOULD be able to determine whether the Relationship is explicit, whether its participants are identifiable, whether its type and direction are clear where required, whether provenance is sufficient where needed, whether privacy boundaries are preserved, and whether the Relationship remains compatible across migration, import, export, and implementation replacement.

A Relationship SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, or storage system MUST NOT silently discard, collapse, reinterpret, reverse, duplicate, expose, or replace a Relationship in a way that causes loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

A Relationship is not the same as a storage link.

A storage link MAY help retrieve or navigate a related entity.

A storage link MUST NOT define the relationship by itself when the relationship affects meaning.

A Relationship is not the same as a backlink.

A backlink MAY show that one representation references another.

A backlink MUST NOT define relationship type, direction, authority, provenance, lifecycle state, privacy classification, validation status, or compatibility by itself unless a future governed specification explicitly defines that behavior.

A Relationship is not the same as a graph edge.

A graph edge MAY represent or visualize a relationship.

A graph edge MUST NOT redefine the standard-level meaning of a Relationship through implementation-specific graph behavior.

A Relationship is not the same as vector similarity.

Vector similarity MAY suggest possible relatedness.

Vector similarity MUST NOT create an approved Relationship by itself when the relationship affects meaning, authority, privacy, provenance, lifecycle state, validation, or downstream use.

A Relationship is not the same as human memory or informal convention.

A relationship that matters to interpretation SHOULD be represented explicitly enough that it remains understandable outside the memory of a particular user, agent, workflow, application, vault, graph view, search index, or implementation.

A Relationship is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what is connected, why it is connected, how the connection should be interpreted, whether it is valid, whether it is reviewed, whether it is safe to expose, and whether it remains meaningful across time and implementation replacement.

## 4. Relationship Participants

Relationship Participants are the governed entities that take part in a Relationship.

A Relationship SHALL have identifiable participants.

A Relationship MUST identify or resolve to its participants clearly enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what entities are connected.

A Relationship MAY include two participants.

A Relationship MAY include more than two participants when the relationship meaning cannot be accurately represented as a simple pair.

A Relationship Participant MAY be:

- a Knowledge Object;
- a Knowledge Record;
- Source Material;
- a standard;
- a specification;
- an ADR;
- an RFC;
- a decision;
- a workflow;
- an agent;
- an implementation;
- an identifier;
- a metadata record;
- a validation record;
- a migration record;
- an import record;
- an export record;
- another governed entity.

A Relationship Participant SHOULD be referenced through stable Object Identity when the participant is a Knowledge Object.

A Relationship Participant SHOULD be referenced through an appropriate stable identifier, source reference, document identifier, record identifier, or governed reference when the participant is not a Knowledge Object.

A Relationship MUST NOT rely only on a filename, folder path, storage location, title, display label, backlink, graph position, search result, tag, vector similarity, user interface state, or implementation-specific identifier to identify a participant when the relationship affects meaning.

Those signals MAY support discovery, navigation, display, indexing, search, visualization, validation, migration, import, export, or implementation convenience.

They MUST NOT replace participant identity where participant identity affects meaning, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

A Relationship SHOULD distinguish between participant identity and participant role.

Participant identity identifies what entity is connected.

Participant role identifies how the entity participates in the relationship.

Participant roles MAY include:

- origin participant;
- target participant;
- source participant;
- evidence participant;
- derived-from participant;
- derived-to participant;
- parent participant;
- child participant;
- prior participant;
- successor participant;
- dependency participant;
- dependent participant;
- supporting participant;
- contradicting participant;
- referenced participant;
- referencing participant;
- responsible participant;
- affected participant;
- other governed participant roles.

Participant roles SHOULD be explicit where role affects interpretation.

A directional Relationship SHOULD identify which participant is the origin and which participant is the target when direction affects meaning.

A non-directional Relationship SHOULD still identify its participants clearly even when origin and target roles are not meaningful.

A Relationship MAY involve Source Material.

When Source Material participates in a Relationship, the relationship SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role.

A Relationship between a Knowledge Record and Source Material MUST preserve the distinction between structured knowledge and original source material.

A Relationship MAY involve a Knowledge Record.

When a Knowledge Record participates in a Relationship, the relationship SHOULD make clear whether the record represents a Knowledge Object, provides a representation of knowledge, preserves evidence, records review, captures validation, or serves another governed role.

A Relationship MAY involve a standard, specification, ADR, RFC, decision, workflow, agent, implementation, or validation record.

When these entities participate in a Relationship, the relationship SHOULD make clear whether the connection expresses dependency, governance relevance, authority, implementation support, workflow participation, validation result, supersession, deprecation, derivation, compatibility, or another governed relationship type.

A Relationship MAY connect entities across different authority levels.

A Relationship between entities of different authority levels MUST NOT allow a lower-authority entity to override a higher-authority entity.

For example, an implementation may relate to a standard, but the implementation MUST NOT redefine the standard through that relationship.

A Relationship MAY connect entities across different lifecycle states.

A Relationship between entities with different lifecycle states SHOULD preserve enough context for future humans, agents, workflows, validators, and implementations to determine whether the relationship is active, historical, proposed, deprecated, superseded, rejected, archived, or requires review.

A Relationship MAY connect entities across different privacy classifications.

A Relationship that crosses privacy boundaries MUST preserve the stricter applicable privacy expectation unless a future governed privacy specification defines different behavior.

A Relationship MUST NOT expose restricted participant information merely because another participant is less restricted or publicly visible.

A Relationship SHOULD preserve participant provenance where participant selection affects interpretation.

Participant provenance MAY identify:

- who or what selected the participant;
- why the participant was selected;
- what source material supports the participant selection;
- whether the participant was identified by a human;
- whether the participant was identified by an agent;
- whether the participant was identified by a workflow;
- whether the participant was imported;
- whether the participant was migrated;
- whether the participant was validated;
- whether the participant requires review.

A Relationship SHOULD support participant validation.

A validator SHOULD be able to determine whether:

- required participants are present;
- participants are identifiable;
- participants are distinguishable from titles, filenames, folder paths, tags, backlinks, graph positions, search results, vector similarities, and implementation-specific identifiers;
- participant roles are clear where required;
- participant identity is stable enough for the relationship purpose;
- participant privacy boundaries are preserved;
- participant lifecycle states do not create ambiguity;
- participant authority levels are not confused;
- participant references remain compatible across migration, import, export, and implementation replacement.

Relationship Participants are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what entities participate in a Relationship, how they participate, whether their identities are stable enough, whether their roles are clear, whether privacy boundaries are preserved, and whether the relationship remains meaningful across time and implementation replacement.

## 5. Relationship Types

Relationship Types describe the conceptual kind of connection expressed by a Relationship.

A Relationship Type exists so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what kind of connection exists between Relationship Participants.

A Relationship SHOULD preserve its type where type affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

A Relationship MUST NOT collapse materially different relationship meanings into a generic connection when the distinction affects interpretation.

For example, the following relationship meanings are not equivalent:

- cites;
- supports;
- contradicts;
- depends on;
- supersedes;
- derives from;
- duplicates;
- refines;
- replaces;
- contains;
- is part of;
- follows;
- precedes;
- implements;
- validates;
- governs;
- references.

A generic relationship MAY be used when the exact type is unknown, unnecessary, or not yet governed.

A generic relationship SHOULD NOT be used when a more specific type is required to preserve meaning, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

KS-0004 does not define a complete controlled vocabulary of relationship types.

A future specification MAY define exact relationship-type vocabularies, allowed values, type hierarchies, inverse types, compatibility rules, validation rules, relationship-type metadata, or migration mappings.

Until such a specification exists, Relationship Types SHOULD remain human-readable, interpretable by agents, and explicit enough to preserve meaning.

A Relationship Type MAY express:

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
- validation relevance;
- authority relevance;
- privacy relevance;
- migration relevance;
- import relevance;
- export relevance;
- review relevance.

A Relationship Type SHOULD be compatible with the Relationship Participants.

For example:

- a Knowledge Object may depend on another Knowledge Object;
- a Knowledge Record may cite Source Material;
- a standard may govern a specification;
- an implementation may implement a standard;
- a workflow may produce a Knowledge Record;
- an agent may propose a Relationship;
- a validation record may validate a Knowledge Object;
- a newer document may supersede an older document.

A Relationship Type SHOULD NOT imply authority that the Relationship Participants do not have.

A lower-authority participant MUST NOT override a higher-authority participant merely because a Relationship Type suggests dependency, implementation, support, reference, or association.

A Relationship Type SHOULD preserve direction where direction affects meaning.

For example:

- `depends on` is not the same as `is depended on by`;
- `supersedes` is not the same as `is superseded by`;
- `derives from` is not the same as `has derivative`;
- `cites` is not the same as `is cited by`;
- `implements` is not the same as `is implemented by`;
- `validates` is not the same as `is validated by`.

A Relationship Type SHOULD preserve source distinction.

A relationship between a Knowledge Record and Source Material SHOULD make clear whether the source provides evidence, origin, attribution, support, contradiction, context, or reference.

A Relationship Type MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

A Relationship Type SHOULD preserve Object Identity.

A relationship between Knowledge Objects SHOULD refer to or resolve to stable Object Identity where practical.

A Relationship Type MUST NOT depend only on filename, folder path, title, backlink behavior, graph layout, tag coincidence, search result, vector similarity, or implementation-specific identifier when the relationship affects meaning.

A Relationship Type SHOULD preserve provenance.

Where a Relationship Type is assigned, changed, inferred, imported, migrated, validated, rejected, approved, deprecated, or superseded, the action SHOULD preserve enough provenance for future review when the type affects interpretation.

A Relationship Type SHOULD preserve lifecycle state.

A Relationship Type may be proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or governed by a future relationship lifecycle state.

A Relationship Type MUST NOT be treated as approved merely because it was created by an implementation, backlink system, graph view, search index, vector index, workflow, or agent.

A Relationship Type SHOULD preserve authority.

Some relationship types may affect governance or interpretation more strongly than others.

For example, `governs`, `supersedes`, `validates`, `rejects`, and `approves` may carry stronger authority implications than `is related to`.

Where authority is affected, the Relationship Type SHOULD be explicit and reviewable.

A Relationship Type MUST preserve privacy boundaries.

A Relationship Type MUST NOT reveal restricted knowledge merely by naming or exposing the nature of a relationship.

Where a Relationship Type would expose sensitive meaning, the relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

A Relationship Type SHOULD support validation.

A validator SHOULD be able to determine whether:

- a required relationship type is present;
- the relationship type is understandable;
- the relationship type is compatible with the participants;
- the relationship type preserves direction where direction matters;
- the relationship type does not create authority confusion;
- the relationship type does not violate privacy boundaries;
- the relationship type remains compatible across migration, import, export, and implementation replacement.

A Relationship Type SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, reverse, duplicate, expose, or replace a Relationship Type in a way that causes loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Types are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what kind of connection exists, whether that connection affects meaning, whether direction matters, whether authority or privacy is affected, and whether the relationship remains interpretable across time and implementation replacement.

## 6. Relationship Direction

Relationship Direction describes whether the meaning of a Relationship depends on the order, orientation, or role of its participants.

A Relationship MAY be directional.

A Relationship MAY be non-directional.

A directional Relationship is a Relationship where direction materially affects meaning.

A non-directional Relationship is a Relationship where direction does not materially affect meaning.

Relationship Direction exists so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether participant order affects interpretation.

A Relationship SHOULD preserve direction where direction affects meaning, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

A Relationship MUST NOT silently lose, reverse, collapse, infer, or reinterpret direction when direction affects meaning.

Examples of directional relationship meanings include:

- depends on;
- supersedes;
- derives from;
- cites;
- implements;
- validates;
- governs;
- replaces;
- follows;
- precedes;
- contains;
- is part of;
- produces;
- reviews;
- approves;
- rejects.

Examples of non-directional or potentially non-directional relationship meanings MAY include:

- is related to;
- is similar to;
- overlaps with;
- is associated with;
- is equivalent to;
- is a duplicate of;
- conflicts with;
- co-occurs with.

A Relationship Type SHOULD indicate whether direction matters when direction affects interpretation.

A directional Relationship SHOULD identify participant roles clearly enough to determine the origin participant and target participant.

The origin participant is the participant from which the directional relationship is expressed.

The target participant is the participant to which the directional relationship is expressed.

For example:

- Document A `depends on` Document B means Document A requires Document B.
- Document A `supersedes` Document B means Document A replaces Document B.
- Document A `derives from` Source B means Document A was created from Source B.
- Implementation A `implements` Standard B means Implementation A realizes Standard B.
- Validator A `validates` Record B means Validator A checks Record B.

These meanings MUST NOT be treated as equivalent to their reverse relationships unless a future governed specification explicitly defines inverse behavior.

A directional Relationship MAY have an inverse relationship.

An inverse relationship expresses the same relationship from the opposite participant perspective.

For example:

- `depends on` may have the inverse `is depended on by`;
- `supersedes` may have the inverse `is superseded by`;
- `derives from` may have the inverse `has derivative`;
- `cites` may have the inverse `is cited by`;
- `implements` may have the inverse `is implemented by`;
- `validates` may have the inverse `is validated by`.

KS-0004 does not define a complete inverse-relationship vocabulary.

A future specification MAY define exact inverse relationship types, direction values, participant-role rules, cardinality rules, traversal rules, validation rules, or relationship serialization formats.

Until such a specification exists, inverse relationships SHOULD remain explicit enough that humans, agents, workflows, validators, and implementations can avoid direction confusion.

A Relationship MUST NOT be considered non-directional merely because an implementation displays it without direction.

A graph view, backlink panel, search result, tag list, folder structure, index entry, vector similarity result, or user interface display MAY show related entities without showing direction.

That display behavior MUST NOT remove direction from the governed Relationship when direction affects meaning.

A Relationship Direction SHOULD preserve Object Identity.

When a directional Relationship connects Knowledge Objects, the origin and target SHOULD refer to or resolve to stable Object Identity where practical.

A Relationship Direction MUST NOT depend only on filename order, folder order, visual layout, graph position, backlink order, search result order, index order, tag order, or implementation-specific display order when direction affects meaning.

A Relationship Direction SHOULD preserve source distinction.

When a directional Relationship connects a Knowledge Record and Source Material, direction SHOULD make clear whether the Knowledge Record cites, derives from, summarizes, interprets, transforms, supports, contradicts, or references the Source Material.

A directional Relationship MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

A Relationship Direction SHOULD preserve provenance.

Where Relationship Direction is assigned, changed, inferred, imported, migrated, validated, rejected, approved, deprecated, or superseded, the action SHOULD preserve enough provenance for future review when direction affects interpretation.

A Relationship Direction SHOULD preserve lifecycle state.

A proposed, inferred, reviewed, approved, deprecated, superseded, rejected, or archived Relationship SHOULD preserve direction where direction affects how the relationship should be used.

A Relationship Direction SHOULD preserve authority.

Direction may affect authority.

For example:

- a standard may govern an implementation;
- an implementation does not govern the standard;
- a newer document may supersede an older document;
- the older document does not supersede the newer document;
- a validator may validate a record;
- the record does not validate the validator.

A lower-authority participant MUST NOT override a higher-authority participant because a directional relationship is reversed, misread, or collapsed.

A Relationship Direction MUST preserve privacy boundaries.

A directional Relationship MUST NOT expose restricted knowledge merely by revealing which participant points to another participant.

Where direction would expose sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

A Relationship Direction SHOULD support validation.

A validator SHOULD be able to determine whether:

- the Relationship is directional or non-directional;
- the origin participant is clear where required;
- the target participant is clear where required;
- participant roles are compatible with the Relationship Type;
- direction is not silently reversed;
- direction is not silently removed;
- direction is not inferred as approved without review where review is required;
- direction does not create authority confusion;
- direction does not violate privacy boundaries;
- direction remains compatible across migration, import, export, and implementation replacement.

A Relationship Direction SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, or storage system MUST NOT silently discard, reverse, collapse, infer, duplicate, expose, or replace Relationship Direction in a way that causes loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Direction is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether direction matters, which participant is the origin, which participant is the target, whether an inverse relationship exists, whether authority or privacy is affected, and whether the relationship remains meaningful across time and implementation replacement.

## 7. Relationship Strength and Confidence

Relationship Strength and Relationship Confidence describe different interpretive qualities of a Relationship.

Relationship Strength describes the relative importance, closeness, dependency, significance, or practical weight of a Relationship where that distinction affects interpretation.

Relationship Confidence describes the degree of certainty, evidence support, review status, reliability, or trust associated with a Relationship where that distinction affects interpretation.

Relationship Strength and Relationship Confidence are not the same thing.

A strong Relationship may have low confidence.

A weak Relationship may have high confidence.

For example:

- a proposed dependency may be important but not yet verified;
- a minor citation may be fully verified but not central to the Knowledge Object;
- a similarity relationship may be obvious but not important;
- a governance relationship may be important and require high confidence before use.

A Relationship MAY include Relationship Strength.

A Relationship MAY include Relationship Confidence.

A Relationship SHOULD include Relationship Strength where the relative importance, dependency, closeness, or significance of the relationship affects interpretation, workflow behavior, validation, governance, review, migration, import, export, or downstream use.

A Relationship SHOULD include Relationship Confidence where certainty, source support, evidence quality, review status, inference quality, agent output, workflow output, validation result, or human approval affects interpretation, workflow behavior, validation, governance, review, migration, import, export, or downstream use.

Relationship Strength MUST NOT be treated as Relationship Confidence.

Relationship Confidence MUST NOT be treated as Relationship Strength.

A Relationship MUST NOT be treated as approved, authoritative, validated, or safe for downstream use merely because it has high strength.

A Relationship MUST NOT be treated as important merely because it has high confidence.

Relationship Strength MAY describe whether a Relationship is:

- central;
- strong;
- moderate;
- weak;
- peripheral;
- incidental;
- context-dependent;
- unknown;
- governed by a future strength value.

Relationship Confidence MAY describe whether a Relationship is:

- confirmed;
- reviewed;
- validated;
- supported;
- inferred;
- proposed;
- uncertain;
- disputed;
- rejected;
- unknown;
- governed by a future confidence value.

KS-0004 does not define a complete controlled vocabulary for Relationship Strength or Relationship Confidence.

A future specification MAY define exact strength values, confidence values, confidence scoring rules, evidence requirements, review rules, validation rules, lifecycle mappings, metadata fields, or serialization formats.

Until such a specification exists, Relationship Strength and Relationship Confidence SHOULD remain human-readable, interpretable by agents, and explicit enough to preserve meaning.

Relationship Strength SHOULD be used carefully.

A Relationship SHOULD NOT receive a strength value unless that value improves interpretation, prioritization, validation, workflow behavior, governance, migration, import, export, review, or downstream use.

Relationship Confidence SHOULD be used carefully.

A Relationship SHOULD NOT receive a confidence value unless that value improves interpretation, reviewability, validation, evidence handling, workflow behavior, governance, migration, import, export, or downstream use.

Relationship Strength MAY be based on:

- semantic importance;
- dependency importance;
- governance importance;
- workflow importance;
- frequency of use;
- relationship centrality;
- review priority;
- maintenance priority;
- migration priority;
- implementation relevance;
- other governed criteria.

Relationship Confidence MAY be based on:

- human review;
- source evidence;
- provenance quality;
- validation result;
- workflow result;
- agent analysis;
- import confidence;
- migration confidence;
- duplicate-detection confidence;
- inference quality;
- source reliability;
- review history;
- other governed criteria.

Relationship Strength SHOULD preserve context.

A strong Relationship in one context may be weak in another context.

For example, a relationship may be strong for migration but weak for conceptual interpretation.

Where context affects strength, the context SHOULD be explicit enough that humans, agents, workflows, validators, and implementations can determine how the strength value should be interpreted.

Relationship Confidence SHOULD preserve context.

A Relationship may have high confidence for source attribution but low confidence for interpretation.

For example, it may be certain that Source A was cited by Record B, but uncertain whether Source A fully supports the interpretation in Record B.

Where context affects confidence, the context SHOULD be explicit enough that humans, agents, workflows, validators, and implementations can determine how the confidence value should be interpreted.

Relationship Strength SHOULD preserve provenance where strength affects interpretation.

Where Relationship Strength is assigned, changed, inferred, imported, migrated, validated, rejected, approved, deprecated, or superseded, the action SHOULD preserve enough provenance for future review when strength affects interpretation.

Relationship Confidence SHOULD preserve provenance where confidence affects interpretation.

Where Relationship Confidence is assigned, changed, inferred, imported, migrated, validated, rejected, approved, deprecated, or superseded, the action SHOULD preserve enough provenance for future review when confidence affects interpretation.

Agent-generated Relationship Strength SHOULD remain reviewable when it affects meaning, workflow behavior, authority, privacy, validation, migration, import, export, governance, publication, or downstream use.

Agent-generated Relationship Confidence SHOULD remain reviewable when it affects meaning, workflow behavior, authority, privacy, validation, migration, import, export, governance, publication, or downstream use.

Workflow-generated Relationship Strength SHOULD remain traceable to the workflow that produced or modified it.

Workflow-generated Relationship Confidence SHOULD remain traceable to the workflow that produced or modified it.

Inferred Relationship Strength MUST NOT be treated as human-approved unless a governed review process confirms it.

Inferred Relationship Confidence MUST NOT be treated as human-approved unless a governed review process confirms it.

Relationship Strength SHOULD preserve lifecycle state.

A proposed, inferred, reviewed, approved, deprecated, superseded, rejected, or archived Relationship MAY have different strength expectations depending on its lifecycle state.

A rejected Relationship MUST NOT remain active merely because it once had high strength.

A deprecated or superseded Relationship SHOULD preserve historical strength information where that information is useful for review, migration, compatibility, or governance.

Relationship Confidence SHOULD preserve lifecycle state.

A proposed, inferred, reviewed, approved, deprecated, superseded, rejected, or archived Relationship MAY have different confidence expectations depending on its lifecycle state.

A rejected Relationship MUST NOT remain active merely because it once had high confidence.

A deprecated or superseded Relationship SHOULD preserve historical confidence information where that information is useful for review, migration, compatibility, or governance.

Relationship Strength SHOULD preserve authority boundaries.

A high-strength Relationship MUST NOT allow a lower-authority participant to override a higher-authority participant.

Relationship Confidence SHOULD preserve authority boundaries.

A high-confidence Relationship MUST NOT allow a lower-authority participant to override a higher-authority participant.

Relationship Strength MUST preserve privacy boundaries.

A Relationship Strength value MUST NOT expose restricted knowledge merely by revealing that a relationship is central, strong, weak, important, dependency-related, governance-related, or sensitive.

Relationship Confidence MUST preserve privacy boundaries.

A Relationship Confidence value MUST NOT expose restricted knowledge merely by revealing certainty, uncertainty, evidence support, review status, validation status, dispute status, or rejection status.

Where Relationship Strength or Relationship Confidence would expose sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Strength SHOULD support validation.

A validator SHOULD be able to determine whether:

- Relationship Strength is present where required;
- Relationship Strength is understandable;
- Relationship Strength is distinguishable from Relationship Confidence;
- Relationship Strength has sufficient context where context affects interpretation;
- Relationship Strength does not create authority confusion;
- Relationship Strength does not violate privacy boundaries;
- Relationship Strength remains compatible across migration, import, export, and implementation replacement.

Relationship Confidence SHOULD support validation.

A validator SHOULD be able to determine whether:

- Relationship Confidence is present where required;
- Relationship Confidence is understandable;
- Relationship Confidence is distinguishable from Relationship Strength;
- Relationship Confidence has sufficient context where context affects interpretation;
- Relationship Confidence has sufficient provenance where provenance affects interpretation;
- Relationship Confidence does not create authority confusion;
- Relationship Confidence does not violate privacy boundaries;
- Relationship Confidence remains compatible across migration, import, export, and implementation replacement.

Relationship Strength and Relationship Confidence SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, reverse, duplicate, expose, or replace Relationship Strength or Relationship Confidence in a way that causes loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Strength and Relationship Confidence are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine how important a relationship is, how certain or supported it is, what context applies, what provenance supports the value, whether review is required, whether authority or privacy is affected, and whether the relationship remains interpretable across time and implementation replacement.

## 8. Relationship Provenance

Relationship Provenance describes the origin, source, reasoning, creator, agent, workflow, import process, migration process, validation process, or evidence associated with a Relationship.

Relationship Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine where a Relationship came from, why it exists, how it was created, and whether it should be trusted, reviewed, preserved, revised, rejected, deprecated, superseded, or approved.

A Relationship SHOULD preserve provenance where provenance affects meaning, interpretation, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

A Relationship MUST preserve provenance where the absence of provenance would create ambiguity about whether the relationship is valid, reviewed, approved, inferred, imported, migrated, agent-generated, workflow-generated, human-created, or source-supported.

Relationship Provenance MAY identify:

- who created the Relationship;
- what created the Relationship;
- when the Relationship was created;
- why the Relationship was created;
- what source material supports the Relationship;
- what Knowledge Object or Knowledge Record supports the Relationship;
- what evidence supports the Relationship;
- what reasoning supports the Relationship;
- what workflow produced or modified the Relationship;
- what agent produced or modified the Relationship;
- what import process produced or modified the Relationship;
- what migration process produced or modified the Relationship;
- what validation process checked the Relationship;
- whether the Relationship was inferred;
- whether the Relationship was proposed;
- whether the Relationship was reviewed;
- whether the Relationship was approved;
- whether the Relationship was rejected;
- whether the Relationship was deprecated;
- whether the Relationship was superseded;
- whether the Relationship requires further review.

Relationship Provenance SHOULD distinguish between human-created, agent-generated, workflow-generated, imported, migrated, inferred, validated, and implementation-generated Relationships where that distinction affects interpretation.

A human-created Relationship MAY have provenance identifying the responsible human, review context, source material, reasoning, or approval state where practical.

An agent-generated Relationship SHOULD preserve enough provenance to identify the responsible agent, instruction, workflow context, source material, reasoning basis, confidence basis, review state, and whether human review has occurred.

A workflow-generated Relationship SHOULD preserve enough provenance to identify the responsible workflow, trigger, input, output, actor, source material, agent activity where applicable, review state, and approval state.

An imported Relationship SHOULD preserve enough provenance to identify the import source, prior identifier where applicable, original relationship meaning where available, import process, transformation behavior, and review state.

A migrated Relationship SHOULD preserve enough provenance to identify the prior storage system, representation, schema, identifier, relationship structure, migration process, migration mapping, transformation behavior, validation result, and review state.

An inferred Relationship SHOULD preserve enough provenance to identify the basis of inference.

The basis of inference MAY include:

- source material;
- metadata;
- content similarity;
- explicit textual reference;
- citation;
- duplicate-detection signal;
- validation result;
- agent analysis;
- workflow output;
- import mapping;
- migration mapping;
- graph analysis;
- search result;
- vector similarity;
- implementation signal;
- other governed inference basis.

An inferred Relationship MUST NOT be treated as approved merely because it has provenance.

Provenance explains where the Relationship came from.

Provenance does not by itself approve the Relationship.

A Relationship generated from an implementation-specific link, backlink, graph edge, search index, tag, folder structure, vector similarity, or user interface signal SHOULD preserve that origin when the signal is used to propose, infer, display, validate, migrate, import, export, or review a Relationship.

An implementation-specific signal MUST NOT become governed Relationship Provenance in a way that hides its implementation-specific origin.

Relationship Provenance SHOULD preserve source distinction.

When Source Material supports a Relationship, the provenance SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role.

A Relationship between a Knowledge Record and Source Material MUST NOT imply that the Knowledge Record and Source Material are the same entity.

Relationship Provenance SHOULD preserve Object Identity.

When a Relationship connects Knowledge Objects, provenance SHOULD refer to or resolve to stable Object Identity where practical.

Relationship Provenance MUST NOT depend only on filenames, folder paths, display titles, tags, backlink behavior, graph layout, search results, vector similarity, implementation-specific identifiers, or hidden application state when provenance affects meaning.

Relationship Provenance SHOULD preserve Relationship Type, Relationship Direction, Relationship Strength, and Relationship Confidence where provenance explains how those qualities were assigned, changed, inferred, imported, migrated, validated, rejected, approved, deprecated, or superseded.

Relationship Provenance SHOULD preserve lifecycle state.

A proposed, inferred, reviewed, approved, deprecated, superseded, rejected, or archived Relationship SHOULD preserve enough provenance to explain the lifecycle state where that state affects interpretation.

A rejected Relationship SHOULD preserve provenance explaining why it was rejected where practical.

A deprecated or superseded Relationship SHOULD preserve provenance explaining why it was deprecated or superseded where practical.

Relationship Provenance SHOULD preserve authority boundaries.

Provenance MUST NOT allow a lower-authority participant, workflow, agent, implementation, source, or process to override a higher-authority participant, standard, decision, or approved governance rule.

A Relationship supported by weak or unclear provenance SHOULD NOT be treated as authoritative merely because it exists.

A Relationship supported by strong provenance SHOULD still respect document authority, lifecycle state, privacy classification, validation expectations, and governance rules.

Relationship Provenance MUST preserve privacy boundaries.

Relationship Provenance MUST NOT expose restricted knowledge merely by identifying a source, creator, agent, workflow, evidence base, reasoning path, import source, migration source, validation result, or relationship origin.

Where provenance would expose sensitive meaning, restricted source material, protected identity, confidential reasoning, private workflow activity, or restricted agent activity, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Provenance SHOULD support validation.

A validator SHOULD be able to determine whether:

- required provenance is present;
- provenance is understandable;
- provenance identifies the origin of the Relationship where required;
- provenance distinguishes human-created, agent-generated, workflow-generated, imported, migrated, inferred, validated, and implementation-generated Relationships where required;
- provenance supports Relationship Type where required;
- provenance supports Relationship Direction where required;
- provenance supports Relationship Strength or Relationship Confidence where required;
- provenance supports lifecycle state where required;
- provenance does not create authority confusion;
- provenance does not violate privacy boundaries;
- provenance remains compatible across migration, import, export, and implementation replacement.

Relationship Provenance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, reverse, duplicate, expose, or replace Relationship Provenance in a way that causes loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine where a Relationship came from, what supports it, who or what created or changed it, whether it was inferred or reviewed, whether authority or privacy is affected, and whether the relationship remains interpretable across time and implementation replacement.

## 9. Relationship Lifecycle State

Relationship Lifecycle State describes the current governed state of a Relationship.

Relationship Lifecycle State exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether a Relationship is proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or governed by a future lifecycle state.

A Relationship MAY have a lifecycle state.

A Relationship SHOULD have a lifecycle state where lifecycle status affects meaning, interpretation, provenance, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

A Relationship MUST have enough lifecycle information to prevent confusion when the Relationship is not approved, is no longer active, has been superseded, has been rejected, was inferred, was imported, was migrated, was generated by an agent, or requires review.

Relationship Lifecycle State MAY include:

- proposed;
- inferred;
- reviewed;
- approved;
- deprecated;
- superseded;
- rejected;
- archived;
- needs review;
- governed by a future lifecycle state.

KS-0004 does not define a complete controlled vocabulary for Relationship Lifecycle State.

A future specification MAY define exact relationship lifecycle states, lifecycle transitions, lifecycle metadata fields, validation rules, approval rules, rejection rules, supersession rules, archival rules, or serialization formats.

Until such a specification exists, Relationship Lifecycle State SHOULD remain human-readable, interpretable by agents, and explicit enough to preserve meaning.

A proposed Relationship is a Relationship that has been suggested but has not yet been reviewed or approved.

A proposed Relationship MUST NOT be treated as approved merely because it exists.

An inferred Relationship is a Relationship derived from evidence, metadata, content similarity, source material, agent analysis, workflow activity, validation output, import behavior, migration behavior, or implementation signals.

An inferred Relationship MUST NOT be treated as approved unless a governed review or approval process confirms it.

A reviewed Relationship is a Relationship that has been inspected by a human, workflow, validator, or governed review process.

A reviewed Relationship MUST NOT be treated as approved unless the review process explicitly approves it.

An approved Relationship is a Relationship accepted for use under the applicable governance, validation, or workflow expectations.

An approved Relationship SHOULD preserve enough provenance to determine who or what approved it, what review occurred, what evidence supports it, and what lifecycle state applies.

A deprecated Relationship is a Relationship that remains historically available but is no longer recommended for future use.

A deprecated Relationship SHOULD preserve enough context for future humans, agents, workflows, validators, and implementations to determine why it was deprecated and what should be used instead where applicable.

A superseded Relationship is a Relationship replaced by another Relationship, Knowledge Object, Knowledge Record, standard, decision, workflow, implementation, identifier, or governed entity.

A superseded Relationship SHOULD identify or reference the superseding Relationship or governed entity where practical.

A rejected Relationship is a Relationship that has been reviewed and not accepted.

A rejected Relationship MUST NOT be treated as active, approved, authoritative, or safe for downstream use unless a future governed process revises its state.

A rejected Relationship SHOULD preserve enough provenance to explain why it was rejected where practical.

An archived Relationship is a Relationship preserved for historical, audit, migration, compatibility, or governance reasons.

An archived Relationship SHOULD remain distinguishable from active Relationships.

A Relationship that needs review is a Relationship whose meaning, type, direction, provenance, strength, confidence, authority, privacy classification, validation state, compatibility, import behavior, migration behavior, or downstream use requires further review.

A Relationship Lifecycle State SHOULD preserve Relationship Type.

A Relationship Type MAY remain historically visible when the Relationship is deprecated, superseded, rejected, or archived, but the lifecycle state SHOULD make clear how the type should be interpreted.

A Relationship Lifecycle State SHOULD preserve Relationship Direction.

A Relationship Direction MAY remain historically visible when the Relationship is deprecated, superseded, rejected, or archived, but the lifecycle state SHOULD make clear how the direction should be interpreted.

A Relationship Lifecycle State SHOULD preserve Relationship Strength and Relationship Confidence.

A rejected, deprecated, superseded, or archived Relationship MUST NOT remain active merely because it has high strength or high confidence.

A Relationship Lifecycle State SHOULD preserve Relationship Provenance.

Where a Relationship changes lifecycle state, the lifecycle transition SHOULD preserve enough provenance for future review when the transition affects meaning, interpretation, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

Lifecycle transition provenance MAY identify:

- the prior lifecycle state;
- the new lifecycle state;
- who or what changed the lifecycle state;
- why the lifecycle state changed;
- when the lifecycle state changed where practical;
- what evidence supported the lifecycle change;
- what review occurred;
- what validation occurred;
- what workflow caused the lifecycle change;
- what agent participated in the lifecycle change;
- what import or migration process caused the lifecycle change;
- whether downstream relationships or records were affected.

A Relationship Lifecycle State SHOULD preserve Object Identity.

A lifecycle state change MUST NOT cause a Relationship to point to the wrong Knowledge Object, Knowledge Record, Source Material, standard, decision, workflow, implementation, identifier, or governed entity.

A Relationship Lifecycle State MUST NOT depend only on filename, folder path, title, tag, backlink behavior, graph layout, search result, vector similarity, implementation-specific identifier, or hidden application state when lifecycle state affects meaning.

A Relationship Lifecycle State SHOULD preserve source distinction.

A lifecycle state applied to a Relationship between a Knowledge Record and Source Material MUST NOT cause the Knowledge Record and Source Material to be treated as the same entity.

A Relationship Lifecycle State SHOULD preserve authority boundaries.

A lifecycle state MUST NOT allow a lower-authority participant, workflow, agent, implementation, source, or process to override a higher-authority participant, standard, decision, or approved governance rule.

A Relationship marked approved by a lower-authority process MUST NOT override a higher-authority document or governed decision.

A Relationship Lifecycle State MUST preserve privacy boundaries.

A lifecycle state MUST NOT expose restricted knowledge merely by revealing that a Relationship is proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or needs review.

Where lifecycle state would expose sensitive meaning, restricted source material, protected identity, confidential reasoning, private workflow activity, or restricted agent activity, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Lifecycle State SHOULD support validation.

A validator SHOULD be able to determine whether:

- lifecycle state is present where required;
- lifecycle state is understandable;
- lifecycle state is compatible with the Relationship Type;
- lifecycle state is compatible with Relationship Direction;
- lifecycle state is supported by provenance where required;
- lifecycle state does not create authority confusion;
- lifecycle state does not violate privacy boundaries;
- lifecycle state distinguishes active, historical, proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, and needs-review Relationships where required;
- lifecycle state remains compatible across migration, import, export, and implementation replacement.

Relationship Lifecycle State SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, reverse, duplicate, expose, or replace Relationship Lifecycle State in a way that causes loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Lifecycle State is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether a Relationship is active, proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or requires review; what provenance supports that state; whether authority or privacy is affected; and whether the relationship remains interpretable across time and implementation replacement.

## 10. Relationship Authority

Relationship Authority describes the governance weight, review status, approval status, interpretive authority, or downstream reliability assigned to a Relationship.

Relationship Authority exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether a Relationship may influence interpretation, validation, workflow behavior, governance, publication, migration, import, export, or downstream use.

A Relationship MAY have authority.

A Relationship SHOULD have authority information where the Relationship affects meaning, interpretation, provenance, lifecycle state, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

Relationship Authority MUST remain distinguishable from document authority.

Document authority describes the governance weight of a document.

Relationship Authority describes the governance weight or interpretive reliability of a Relationship.

A Relationship connected to a high-authority document does not automatically become high-authority.

A Relationship created by a high-authority document, standard, workflow, validator, agent, implementation, or source SHOULD preserve enough provenance and lifecycle context for future review.

Relationship Authority MUST remain distinguishable from Relationship Lifecycle State.

Lifecycle state describes whether a Relationship is proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or requires review.

Authority describes how much governance weight or interpretive reliability the Relationship carries.

A Relationship may be approved but low-authority for some uses.

A Relationship may be high-impact but still require review before it becomes authoritative.

Relationship Authority MUST remain distinguishable from Relationship Confidence.

Confidence describes certainty, evidence support, review quality, or reliability.

Authority describes governance weight or permission to influence interpretation or action.

A high-confidence Relationship MUST NOT override governance authority.

A low-confidence Relationship MUST NOT be treated as authoritative merely because it is useful, repeated, indexed, displayed, inferred, or frequently referenced.

Relationship Authority MAY describe whether a Relationship is:

- authoritative;
- approved;
- reviewed;
- advisory;
- provisional;
- inferred;
- proposed;
- disputed;
- deprecated;
- superseded;
- rejected;
- informational;
- implementation-specific;
- governed by a future authority value.

KS-0004 does not define a complete controlled vocabulary for Relationship Authority.

A future specification MAY define exact relationship authority values, authority levels, approval rules, review rules, validation rules, metadata fields, authority inheritance rules, conflict-resolution rules, or serialization formats.

Until such a specification exists, Relationship Authority SHOULD remain human-readable, interpretable by agents, and explicit enough to preserve meaning.

A Relationship SHOULD be treated as authoritative only when the applicable governance, review, validation, workflow, or approval expectations support that authority.

A Relationship MUST NOT become authoritative merely because:

- it appears in a file;
- it appears in metadata;
- it appears in a backlink;
- it appears in a graph view;
- it appears in a search result;
- it appears in a vector index;
- it appears in an implementation;
- it was created by an agent;
- it was created by a workflow;
- it was imported;
- it was migrated;
- it is frequently used;
- it has high strength;
- it has high confidence;
- it connects to a high-authority participant.

A Relationship MAY support authority interpretation.

For example:

- a standard may govern a specification;
- a specification may constrain an implementation;
- an ADR may explain a decision;
- an RFC may propose a change;
- a workflow may require review before approval;
- a validator may support a validation result;
- a source may support a Knowledge Record.

A Relationship that expresses governance authority SHOULD be explicit, reviewable, traceable, and compatible with the authority hierarchy defined by the constitutional foundation.

A lower-authority Relationship MUST NOT override a higher-authority document, standard, decision, specification, workflow rule, validation rule, privacy rule, or governance rule.

A Relationship between entities of different authority levels SHOULD preserve enough context to determine which entity has authority and what the Relationship means.

For example:

- an implementation may implement a standard, but the implementation does not govern the standard;
- an RFC may propose a change to a standard, but the RFC does not approve the change;
- an ADR may explain a decision, but it does not override a constitutional document;
- a validator may report a result, but the result does not automatically supersede the governed standard being checked;
- an agent may propose a Relationship, but the proposal does not become authoritative without governed review where review is required.

Relationship Authority SHOULD preserve Relationship Type.

Some Relationship Types may carry stronger authority implications than others.

For example, `governs`, `approves`, `rejects`, `validates`, `supersedes`, and `requires` may carry stronger authority implications than `references`, `is related to`, `is similar to`, or `mentions`.

Where Relationship Type affects authority, the Relationship Type and Relationship Authority SHOULD remain distinguishable and reviewable.

Relationship Authority SHOULD preserve Relationship Direction.

Direction may determine which participant has authority over another participant.

For example:

- a standard may govern an implementation;
- an implementation does not govern the standard;
- a newer approved standard may supersede an older standard;
- the older standard does not supersede the newer approved standard;
- a validation rule may constrain a record;
- the record does not constrain the validation rule.

A Relationship MUST NOT gain, lose, reverse, or confuse authority because direction is silently lost, reversed, collapsed, inferred, duplicated, or reinterpreted.

Relationship Authority SHOULD preserve Relationship Strength and Relationship Confidence.

Relationship Strength and Relationship Confidence may inform authority review, but they MUST NOT replace authority.

A strong Relationship is not automatically authoritative.

A high-confidence Relationship is not automatically authoritative.

Relationship Authority SHOULD preserve Relationship Provenance.

Where Relationship Authority is assigned, changed, inferred, imported, migrated, validated, rejected, approved, deprecated, or superseded, the action SHOULD preserve enough provenance for future review when authority affects interpretation.

Relationship Authority SHOULD preserve Relationship Lifecycle State.

A proposed, inferred, deprecated, superseded, rejected, or archived Relationship MUST NOT be treated as active authority unless a future governed process explicitly defines that behavior.

An approved Relationship SHOULD preserve enough lifecycle and provenance information to support its authority.

Relationship Authority SHOULD preserve Object Identity.

When a Relationship connects Knowledge Objects, authority interpretation SHOULD refer to or resolve to stable Object Identity where practical.

Relationship Authority MUST NOT depend only on filename, folder path, title, tag, backlink behavior, graph layout, search result, vector similarity, implementation-specific identifier, or hidden application state when authority affects meaning.

Relationship Authority SHOULD preserve source distinction.

A Relationship between a Knowledge Record and Source Material MUST NOT cause the Source Material and Knowledge Record to be treated as the same entity.

Source support MAY influence confidence or review, but Source Material does not automatically govern the Knowledge Record unless a future governed specification defines that behavior.

Relationship Authority MUST preserve privacy boundaries.

Relationship Authority MUST NOT expose restricted knowledge merely by revealing that a Relationship is authoritative, advisory, disputed, rejected, provisional, implementation-specific, governance-related, validation-related, or approval-related.

Where authority would expose sensitive meaning, restricted source material, protected identity, confidential reasoning, private workflow activity, or restricted agent activity, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Authority SHOULD support validation.

A validator SHOULD be able to determine whether:

- authority information is present where required;
- authority information is understandable;
- authority is distinguishable from lifecycle state;
- authority is distinguishable from confidence;
- authority is distinguishable from document authority;
- authority is compatible with Relationship Type;
- authority is compatible with Relationship Direction;
- authority is supported by provenance where required;
- authority does not allow a lower-authority entity to override a higher-authority entity;
- authority does not violate privacy boundaries;
- authority remains compatible across migration, import, export, and implementation replacement.

Relationship Authority SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, reverse, duplicate, expose, or replace Relationship Authority in a way that causes loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Authority is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what governance weight or interpretive authority a Relationship carries, whether that authority is supported by provenance and lifecycle state, whether authority is compatible with participant authority levels, whether privacy is affected, and whether the relationship remains interpretable across time and implementation replacement.

## 11. Relationship Privacy

Relationship Privacy describes the privacy classification, visibility boundary, access expectation, exposure risk, or handling rule associated with a Relationship.

Relationship Privacy exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether a Relationship may be viewed, indexed, searched, displayed, exported, imported, migrated, synchronized, published, summarized, processed by an agent, or used in downstream workflows.

A Relationship MAY have privacy information.

A Relationship SHOULD have privacy information where the Relationship affects meaning, interpretation, provenance, lifecycle state, authority, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, exposure risk, or downstream use.

A Relationship MUST preserve privacy boundaries.

A Relationship MUST NOT expose restricted knowledge merely because one or more Relationship Participants are less restricted, public, searchable, indexed, exported, displayed, or visible in an implementation.

Relationship Privacy MAY describe whether a Relationship is:

- public;
- internal;
- private;
- confidential;
- sensitive;
- restricted;
- redacted;
- hidden;
- visible only by permission;
- governed by a future privacy value.

KS-0004 does not define a complete controlled vocabulary for Relationship Privacy.

A future privacy standard or specification MAY define exact privacy classifications, access-control rules, redaction behavior, inheritance behavior, visibility rules, indexing rules, agent-access rules, export rules, synchronization rules, publication rules, validation rules, metadata fields, or serialization formats.

Until such a specification exists, Relationship Privacy SHOULD remain human-readable, interpretable by agents, and explicit enough to prevent accidental exposure.

A Relationship MAY have a privacy classification that differs from one or more of its participants.

A Relationship SHOULD be handled according to the stricter applicable privacy classification when privacy classifications differ unless a future governed privacy specification defines different behavior.

For example:

- a public Knowledge Object may have a restricted relationship to private Source Material;
- an internal Knowledge Record may have a confidential relationship to a sensitive decision;
- a public standard may have a restricted relationship to a private implementation note;
- an agent may propose a relationship that should not be exposed until reviewed.

A Relationship MUST NOT reveal restricted participant information merely by existing.

A Relationship MUST NOT reveal restricted meaning merely through its type, direction, strength, confidence, provenance, lifecycle state, authority, validation state, metadata, display behavior, search behavior, graph behavior, backlink behavior, export behavior, or implementation behavior.

Relationship Privacy SHOULD preserve participant privacy.

When Relationship Participants have different privacy classifications, the Relationship SHOULD preserve enough information for humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to determine which privacy boundary applies.

A Relationship between a less restricted participant and a more restricted participant SHOULD NOT expose the more restricted participant to users, agents, workflows, exports, indexes, search results, graph views, summaries, or implementations that are not permitted to access it.

Relationship Privacy SHOULD preserve Relationship Type.

A Relationship Type may reveal sensitive meaning.

For example, `contradicts`, `rejects`, `depends on`, `supersedes`, `approves`, `governs`, `validates`, `is derived from`, or `is supported by` may expose meaning even when participant names are hidden.

Where Relationship Type exposes sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Privacy SHOULD preserve Relationship Direction.

Relationship Direction may reveal sensitive meaning.

For example, knowing that a restricted source supports a public record, that a confidential decision governs an implementation, or that one object depends on another may expose knowledge even if the full content is not visible.

Where Relationship Direction exposes sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Privacy SHOULD preserve Relationship Strength and Relationship Confidence.

Relationship Strength or Relationship Confidence may reveal sensitive meaning by showing that a relationship is central, weak, uncertain, disputed, validated, rejected, or strongly supported.

Where Relationship Strength or Relationship Confidence exposes sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Privacy SHOULD preserve Relationship Provenance.

Relationship Provenance may reveal sensitive sources, creators, agents, workflows, reasoning paths, evidence, import sources, migration sources, validation results, or review history.

Where Relationship Provenance exposes sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Privacy SHOULD preserve Relationship Lifecycle State.

Lifecycle state may reveal sensitive review, approval, rejection, deprecation, supersession, archival, or needs-review information.

Where Relationship Lifecycle State exposes sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Privacy SHOULD preserve Relationship Authority.

Authority may reveal sensitive governance, validation, approval, dispute, rejection, or implementation-specific meaning.

Where Relationship Authority exposes sensitive meaning, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Relationship Privacy SHOULD preserve Object Identity.

When a Relationship connects Knowledge Objects, privacy behavior SHOULD refer to or resolve to stable Object Identity where practical.

Relationship Privacy MUST NOT depend only on filename, folder path, title, tag, backlink behavior, graph layout, search result, vector similarity, implementation-specific identifier, or hidden application state when privacy affects meaning or exposure.

Relationship Privacy SHOULD preserve source distinction.

A Relationship between a Knowledge Record and Source Material MUST NOT cause Source Material to be exposed merely because the Knowledge Record is visible.

A Relationship between Source Material and a Knowledge Record SHOULD preserve whether the source is available, restricted, redacted, hidden, external, sensitive, or governed by another privacy expectation where that distinction affects exposure.

Relationship Privacy SHOULD preserve agent boundaries.

An agent MUST NOT access, infer, summarize, export, index, transform, publish, or expose a Relationship unless the relevant privacy classification, workflow, permission model, and governance rules allow that action.

An agent-generated Relationship SHOULD preserve enough privacy context for future review when the relationship affects restricted knowledge, private source material, sensitive reasoning, or downstream exposure.

Relationship Privacy SHOULD preserve workflow boundaries.

A workflow MUST NOT route, export, publish, synchronize, index, summarize, or expose a Relationship unless the relevant privacy classification, permission model, and workflow rules allow that action.

A workflow-generated Relationship SHOULD preserve enough privacy context for future review when the relationship affects restricted knowledge, private source material, sensitive reasoning, or downstream exposure.

Relationship Privacy SHOULD preserve implementation boundaries.

An implementation MUST NOT expose a restricted Relationship through backlink panels, graph views, search results, indexes, summaries, previews, exports, sync systems, caches, logs, metadata displays, vector stores, recommendation systems, dashboards, APIs, plugins, or user interfaces unless the relevant privacy classification and permission model allow that exposure.

Relationship Privacy SHOULD support redaction where practical.

A redacted Relationship MAY preserve enough information to show that a relationship exists without exposing restricted participants, type, direction, strength, confidence, provenance, lifecycle state, authority, validation state, or sensitive context.

Redaction MUST NOT create false meaning.

A redacted Relationship SHOULD make clear that information has been withheld where that fact is safe to reveal.

Relationship Privacy SHOULD support validation.

A validator SHOULD be able to determine whether:

- privacy information is present where required;
- privacy information is understandable;
- privacy classification is compatible with participant privacy;
- privacy classification is compatible with Relationship Type;
- privacy classification is compatible with Relationship Direction;
- privacy classification is compatible with Relationship Provenance;
- privacy classification is compatible with Relationship Lifecycle State;
- privacy classification is compatible with Relationship Authority;
- privacy boundaries are not weakened by implementation behavior;
- privacy boundaries are not weakened by agent behavior;
- privacy boundaries are not weakened by workflow behavior;
- privacy boundaries remain compatible across migration, import, export, synchronization, backup, restoration, indexing, and implementation replacement.

Relationship Privacy SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, search process, graph process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, weaken, expose, duplicate, or replace Relationship Privacy in a way that causes privacy exposure, loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Privacy is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine who or what may access a Relationship, whether the Relationship exposes restricted knowledge, whether stricter participant privacy applies, whether redaction is required, whether agent or workflow access is allowed, and whether the relationship remains privacy-respecting across time and implementation replacement.

## 12. Relationship Validation

Relationship Validation describes the process of checking whether a Relationship satisfies the identity, participant, type, direction, strength, confidence, provenance, lifecycle, authority, privacy, compatibility, and implementation-independence expectations defined by The Brain Standard.

Relationship Validation exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether a Relationship is valid, incomplete, ambiguous, unsafe, conflicting, deprecated, superseded, rejected, or requires review.

A Relationship MAY be validated.

A Relationship SHOULD be validated where the Relationship affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

Relationship Validation MUST NOT redefine relationship meaning.

Validation checks whether a Relationship satisfies applicable standards, specifications, workflow rules, governance expectations, privacy expectations, and compatibility expectations.

Validation does not create new relationship meaning unless a future governed specification explicitly defines that behavior.

Relationship Validation MAY determine whether:

- required Relationship Participants are present;
- Relationship Participants are identifiable;
- Relationship Participants are stable enough for the relationship purpose;
- Relationship Participant roles are clear where required;
- Relationship Type is present where required;
- Relationship Type is understandable;
- Relationship Type is compatible with the participants;
- Relationship Direction is clear where required;
- Relationship Strength is present where required;
- Relationship Confidence is present where required;
- Relationship Strength and Relationship Confidence remain distinguishable;
- Relationship Provenance is sufficient where required;
- Relationship Lifecycle State is present where required;
- Relationship Authority is clear where required;
- Relationship Privacy is preserved;
- Relationship Compatibility is preserved;
- the Relationship remains implementation-independent;
- the Relationship requires human review;
- the Relationship should be accepted, revised, rejected, deprecated, superseded, archived, or escalated.

Relationship Validation SHOULD distinguish between structural validity, interpretive validity, governance validity, privacy validity, compatibility validity, and implementation validity where those distinctions affect interpretation.

Structural validity checks whether the Relationship has the required form, participants, references, metadata, and required fields under applicable standards or specifications.

Interpretive validity checks whether the Relationship can be understood without ambiguity.

Governance validity checks whether the Relationship respects authority, lifecycle state, approval expectations, review expectations, and governance boundaries.

Privacy validity checks whether the Relationship preserves privacy classifications, visibility boundaries, access expectations, redaction expectations, and exposure controls.

Compatibility validity checks whether the Relationship can survive migration, import, export, backup, restoration, synchronization, indexing, validation, and implementation replacement without losing meaning.

Implementation validity checks whether a specific implementation preserves the Relationship without redefining it through implementation-specific behavior.

A Relationship may pass one validation type and fail another.

For example:

- a Relationship may be structurally valid but lack sufficient provenance;
- a Relationship may have clear participants but unclear direction;
- a Relationship may be valid for private use but unsafe for export;
- a Relationship may be compatible with one implementation but not portable enough for the standard;
- a Relationship may be high confidence but still fail authority validation;
- a Relationship may be approved but still require privacy review before publication.

A validation result MUST NOT be treated as approval unless the applicable governance, workflow, or specification explicitly defines that validation result as approval.

Validation may support approval.

Validation does not automatically replace approval.

A validator MAY be human, agentic, workflow-based, software-based, implementation-specific, specification-based, or governed by a future validation specification.

A validator SHOULD identify what standard, specification, rule, workflow, or expectation was used during validation where that information affects interpretation.

Relationship Validation SHOULD preserve Relationship Participants.

A validator SHOULD be able to determine whether participants are present, identifiable, distinguishable, stable enough, compatible with the Relationship Type, and safe to expose under applicable privacy expectations.

Relationship Validation SHOULD preserve Relationship Type.

A validator SHOULD be able to determine whether the Relationship Type is present where required, understandable, compatible with the participants, compatible with authority expectations, compatible with privacy expectations, and preserved across migration, import, export, and implementation replacement.

Relationship Validation SHOULD preserve Relationship Direction.

A validator SHOULD be able to determine whether direction is required, whether origin and target participants are clear where required, whether inverse relationships are represented safely where applicable, and whether direction has been silently lost, reversed, collapsed, inferred, duplicated, or reinterpreted.

Relationship Validation SHOULD preserve Relationship Strength and Relationship Confidence.

A validator SHOULD be able to determine whether strength and confidence are present where required, distinguishable from each other, supported by context where needed, supported by provenance where needed, and not incorrectly treated as authority or approval.

Relationship Validation SHOULD preserve Relationship Provenance.

A validator SHOULD be able to determine whether provenance identifies the origin, source, reasoning, creator, agent, workflow, import process, migration process, validation process, or evidence associated with the Relationship where required.

A validation result SHOULD preserve enough provenance to explain the validation action where the result affects interpretation, lifecycle state, authority, privacy classification, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

Validation provenance MAY identify:

- what validator performed the validation;
- what rule or standard was checked;
- what specification was used;
- what workflow triggered the validation;
- what input was validated;
- what result was produced;
- what issue was found;
- what correction was recommended;
- whether human review is required;
- whether downstream use is allowed;
- whether export, publication, migration, or synchronization is safe.

Relationship Validation SHOULD preserve Relationship Lifecycle State.

A validator SHOULD be able to determine whether the Relationship is proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, needs review, or governed by a future lifecycle state.

A validation result MAY recommend a lifecycle state change.

A validation result MUST NOT silently change Relationship Lifecycle State unless a governed workflow or future specification explicitly allows that behavior.

Relationship Validation SHOULD preserve Relationship Authority.

A validator SHOULD be able to determine whether the Relationship carries authority, whether that authority is supported by governance, review, provenance, lifecycle state, and participant authority levels, and whether the Relationship improperly allows lower-authority entities to override higher-authority entities.

A validation result MUST NOT elevate Relationship Authority unless a governed workflow or future specification explicitly allows that behavior.

Relationship Validation MUST preserve Relationship Privacy.

A validator MUST NOT expose restricted Relationship Participants, Relationship Type, Relationship Direction, Relationship Strength, Relationship Confidence, Relationship Provenance, Relationship Lifecycle State, Relationship Authority, validation results, or sensitive context to users, agents, workflows, exports, indexes, graph views, summaries, logs, caches, dashboards, APIs, plugins, or implementations that are not permitted to access them.

A privacy validation failure SHOULD prevent publication, export, synchronization, indexing, summarization, or agent processing where those actions would expose restricted knowledge.

Relationship Validation SHOULD preserve Object Identity.

When a Relationship connects Knowledge Objects, validation SHOULD refer to or resolve to stable Object Identity where practical.

Relationship Validation MUST NOT depend only on filename, folder path, title, tag, backlink behavior, graph layout, search result, vector similarity, implementation-specific identifier, or hidden application state when validation affects meaning.

Relationship Validation SHOULD preserve source distinction.

A validator MUST NOT treat Source Material and Knowledge Records as the same entity.

A validator SHOULD be able to determine whether Source Material provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role where that distinction affects interpretation.

Relationship Validation SHOULD preserve agent boundaries.

An agent MAY validate, propose validation results, identify validation issues, suggest corrections, or escalate Relationships for human review.

An agent MUST NOT silently approve, reject, expose, publish, export, migrate, or modify a Relationship unless the relevant agent standard, workflow rule, privacy rule, and governance rule allow that behavior.

Relationship Validation SHOULD preserve workflow boundaries.

A workflow MAY validate, route, escalate, approve, reject, deprecate, supersede, archive, export, import, migrate, or publish a Relationship only when the applicable workflow standard, privacy rule, validation rule, and governance rule allow that behavior.

Relationship Validation SHOULD preserve implementation boundaries.

An implementation MAY provide validation tools, validation views, validation reports, validation warnings, validation indexes, or validation automation.

An implementation MUST NOT redefine Relationship Validation through implementation-specific behavior unless that behavior is clearly marked as implementation-specific and remains subordinate to The Brain Standard.

Relationship Validation SHOULD support corrective action.

A validation result MAY recommend:

- adding missing participants;
- clarifying participant roles;
- correcting Relationship Type;
- clarifying Relationship Direction;
- adding context;
- adding provenance;
- changing lifecycle state;
- reviewing authority;
- strengthening privacy handling;
- redacting restricted relationship information;
- rejecting an invalid Relationship;
- deprecating a Relationship;
- superseding a Relationship;
- escalating for human review;
- preserving a compatibility warning;
- updating import, export, or migration handling.

Corrective action MUST preserve provenance where the correction affects meaning, lifecycle state, authority, privacy classification, compatibility, governance, publication, or downstream use.

Relationship Validation SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, search process, graph process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, weaken, expose, duplicate, approve, reject, or replace Relationship Validation in a way that causes privacy exposure, loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Relationship Validation is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether a Relationship satisfies the applicable standards, what validation was performed, what result was produced, what evidence or rule supports the result, whether review is required, whether privacy or authority is affected, and whether the relationship remains valid across time and implementation replacement.

## 13. Relationship Compatibility

Relationship Compatibility describes whether a Relationship remains meaningful, portable, reviewable, privacy-respecting, validatable, and interpretable across storage systems, workflows, agents, validators, import processes, export processes, migration processes, backups, restorations, synchronizations, indexes, and implementation replacement.

Relationship Compatibility exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can preserve Relationships without losing meaning, identity, participant clarity, type, direction, strength, confidence, provenance, lifecycle state, authority, privacy, validation state, or governance context.

A Relationship SHOULD preserve compatibility where the Relationship affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

Relationship Compatibility MUST NOT be treated as simple file conversion.

A file may be converted while Relationship meaning is lost.

A storage system may preserve a visible link while losing Relationship Type, Relationship Direction, Relationship Provenance, Relationship Lifecycle State, Relationship Authority, Relationship Privacy, or Relationship Validation.

A graph may preserve an edge while losing governed relationship meaning.

A search index may preserve discoverability while losing relationship context.

A vector index may preserve similarity while losing explicit relationship interpretation.

Compatibility requires preserving governed relationship meaning, not merely preserving a technical pointer, link, edge, tag, filename, folder path, search result, or implementation-specific reference.

Relationship Compatibility SHOULD preserve Relationship Participants.

A compatible Relationship SHOULD allow future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to determine what entities participate in the Relationship.

Relationship Participants SHOULD remain identifiable across:

- renaming;
- moving;
- copying;
- backup;
- restoration;
- synchronization;
- indexing;
- import;
- export;
- migration;
- validation;
- workflow activity;
- agent activity;
- implementation replacement.

Relationship Compatibility SHOULD preserve Object Identity.

When a Relationship connects Knowledge Objects, the Relationship SHOULD refer to or resolve to stable Object Identity where practical.

A compatible Relationship MUST NOT point to the wrong Knowledge Object because of filename changes, folder changes, title changes, storage changes, backlink changes, graph changes, search index changes, vector index changes, implementation-specific identifier changes, or hidden application state.

Relationship Compatibility SHOULD preserve Relationship Type.

A compatible Relationship SHOULD preserve the conceptual kind of connection expressed by the Relationship where type affects meaning.

A Relationship Type MUST NOT be silently collapsed into a generic relationship when the distinction affects interpretation, provenance, lifecycle state, authority, privacy classification, validation, import, export, migration, workflow behavior, agent behavior, governance, publication, or downstream use.

Relationship Compatibility SHOULD preserve Relationship Direction.

A compatible Relationship SHOULD preserve direction where direction affects meaning.

A Relationship Direction MUST NOT be silently lost, reversed, collapsed, inferred, duplicated, or reinterpreted during storage, indexing, backup, restoration, synchronization, validation, import, export, migration, workflow activity, agent activity, or implementation replacement.

Relationship Compatibility SHOULD preserve Relationship Strength and Relationship Confidence.

A compatible Relationship SHOULD preserve strength and confidence where those values affect interpretation, review, validation, governance, privacy, migration, import, export, workflow behavior, agent behavior, publication, or downstream use.

Relationship Strength and Relationship Confidence MUST remain distinguishable across compatible representations.

Relationship Compatibility SHOULD preserve Relationship Provenance.

A compatible Relationship SHOULD preserve enough provenance to determine where the Relationship came from, what supports it, who or what created or changed it, whether it was inferred, reviewed, imported, migrated, validated, approved, rejected, deprecated, superseded, or generated by an agent or workflow.

Relationship Provenance MUST NOT be silently discarded when provenance affects meaning, authority, privacy, validation, migration, import, export, governance, publication, or downstream use.

Relationship Compatibility SHOULD preserve Relationship Lifecycle State.

A compatible Relationship SHOULD preserve whether the Relationship is proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, needs review, or governed by a future lifecycle state.

A rejected, deprecated, superseded, archived, or needs-review Relationship MUST NOT become active merely because it was imported, exported, migrated, restored, synchronized, indexed, displayed, or represented in a different implementation.

Relationship Compatibility SHOULD preserve Relationship Authority.

A compatible Relationship SHOULD preserve authority information where authority affects interpretation, governance, validation, workflow behavior, publication, migration, import, export, or downstream use.

A compatible process MUST NOT allow lower-authority Relationships, agents, workflows, implementations, sources, imports, exports, migrations, or validation results to override higher-authority documents, standards, decisions, specifications, privacy rules, validation rules, workflow rules, or governance rules.

Relationship Compatibility MUST preserve Relationship Privacy.

A compatible process MUST NOT expose restricted Relationships, restricted Relationship Participants, restricted Relationship Types, restricted Relationship Direction, restricted Relationship Strength, restricted Relationship Confidence, restricted Relationship Provenance, restricted Relationship Lifecycle State, restricted Relationship Authority, restricted validation results, or restricted relationship context.

A compatible process MUST NOT weaken privacy classification during storage, indexing, backup, restoration, synchronization, validation, import, export, migration, workflow activity, agent activity, publication, or implementation replacement.

Where Relationship Privacy cannot be preserved safely, the Relationship SHOULD be marked for review, restricted, redacted, withheld, or excluded according to the stricter applicable privacy expectation unless a future governed privacy specification defines different behavior.

Relationship Compatibility SHOULD preserve Relationship Validation.

A compatible Relationship SHOULD preserve validation state where validation affects interpretation, governance, privacy, migration, import, export, publication, workflow behavior, agent behavior, or downstream use.

A validation result MUST NOT be silently converted into approval.

A validation warning MUST NOT be silently removed when the warning affects meaning, authority, privacy, lifecycle state, compatibility, migration, import, export, publication, or downstream use.

Relationship Compatibility SHOULD preserve source distinction.

A compatible process MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

A Relationship between a Knowledge Record and Source Material SHOULD preserve whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role where that distinction affects interpretation.

Relationship Compatibility SHOULD preserve implementation independence.

A Relationship MUST NOT depend only on implementation-specific links, backlinks, graph edges, database relations, plugin behavior, application state, user interface position, cached indexes, vector indexes, search indexes, folder paths, filenames, tags, aliases, or storage-specific identifiers when the Relationship affects meaning.

Implementation-specific representations MAY assist storage, display, search, indexing, visualization, validation, import, export, migration, or navigation.

Implementation-specific representations MUST NOT replace governed relationship meaning.

Relationship Compatibility SHOULD support graceful degradation.

When full Relationship information cannot be preserved, a compliant process SHOULD preserve the strongest available traceable information and mark the Relationship for review.

Graceful degradation MAY include preserving:

- unresolved Relationship Participants;
- prior participant identifiers;
- legacy identifiers;
- prior Relationship Type;
- uncertain Relationship Direction;
- prior strength values;
- prior confidence values;
- provenance notes;
- lifecycle notes;
- authority notes;
- privacy notes;
- validation notes;
- compatibility notes;
- import mappings;
- export mappings;
- migration mappings;
- review-required status.

Graceful degradation MUST NOT silently pretend that a Relationship is fully valid, approved, authoritative, private, portable, or compatible when required relationship information is missing, conflicting, ambiguous, unsafe, or unresolved.

Relationship Compatibility SHOULD support conflict detection.

A compatibility process SHOULD identify Relationship conflicts where practical.

Relationship conflicts MAY include:

- conflicting participants;
- conflicting Relationship Types;
- conflicting Relationship Direction;
- conflicting Relationship Strength;
- conflicting Relationship Confidence;
- conflicting provenance;
- conflicting lifecycle states;
- conflicting authority expectations;
- conflicting privacy classifications;
- conflicting validation results;
- conflicting import mappings;
- conflicting export mappings;
- conflicting migration mappings;
- conflicting implementation representations.

A compatibility conflict SHOULD be marked for review when it affects meaning, authority, privacy, validation, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

Relationship Compatibility SHOULD support agent boundaries.

An agent MUST NOT treat a Relationship as compatible merely because the agent can read, infer, summarize, index, classify, or generate it.

An agent SHOULD preserve enough compatibility context for future review when the Relationship affects meaning, provenance, lifecycle state, authority, privacy, validation, migration, import, export, publication, or downstream use.

Relationship Compatibility SHOULD support workflow boundaries.

A workflow MUST NOT treat a Relationship as compatible merely because a workflow step completed successfully.

A workflow SHOULD preserve enough compatibility context for future review when the Relationship affects meaning, provenance, lifecycle state, authority, privacy, validation, migration, import, export, publication, or downstream use.

Relationship Compatibility SHOULD support implementation boundaries.

An implementation MUST NOT claim Relationship Compatibility merely because it can display, store, index, link, search, visualize, export, import, or migrate a Relationship.

An implementation SHOULD preserve governed relationship meaning across its internal storage, interface, index, cache, graph, plugin, API, export, import, migration, backup, restoration, and synchronization behavior.

Relationship Compatibility SHOULD support validation.

A validator SHOULD be able to determine whether:

- Relationship Participants remain identifiable;
- Object Identity is preserved where applicable;
- Relationship Type is preserved where required;
- Relationship Direction is preserved where required;
- Relationship Strength and Relationship Confidence remain distinguishable;
- Relationship Provenance remains sufficient;
- Relationship Lifecycle State remains clear;
- Relationship Authority remains clear;
- Relationship Privacy is preserved;
- Relationship Validation state remains clear;
- source distinction is preserved;
- implementation-specific behavior has not redefined relationship meaning;
- import, export, migration, backup, restoration, synchronization, indexing, and implementation replacement preserve governed relationship behavior.

Relationship Compatibility is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can move, preserve, validate, review, display, index, synchronize, back up, restore, import, export, and migrate Relationships without losing meaning, breaking identity, weakening privacy, confusing authority, erasing provenance, collapsing lifecycle state, invalidating validation results, or creating implementation lock-in.

## 14. Import, Export, and Migration Behavior

Import, Export, and Migration Behavior describes how Relationships are brought into, produced from, moved between, transformed across, or preserved within compliant environments.

Import, Export, and Migration Behavior exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can move Relationships without losing meaning, identity, participant clarity, type, direction, strength, confidence, provenance, lifecycle state, authority, privacy, validation state, compatibility, or governance context.

Import is the process of bringing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, Relationships, or external content into a compliant environment.

Export is the process of producing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, Relationships, or external content from a compliant environment for use elsewhere.

Migration is the process of moving from one storage system, implementation, representation, schema, vault, repository, database, file format, workflow environment, or tool environment to another.

A Relationship SHOULD preserve governed meaning during import, export, and migration where the Relationship affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, workflow behavior, agent behavior, governance, publication, or downstream use.

Import, export, and migration MUST NOT be treated as successful merely because files, links, identifiers, graph edges, tags, folders, backlinks, indexes, search results, vector records, database records, or implementation-specific references were moved.

An import process MUST preserve Relationship meaning where that meaning affects interpretation.

An export process MUST preserve Relationship meaning where that meaning affects downstream use.

A migration process MUST preserve Relationship meaning where that meaning affects continued use, governance, validation, privacy, compatibility, or review.

Import, export, and migration processes SHOULD preserve Relationship Participants.

Relationship Participants SHOULD remain identifiable before, during, and after import, export, or migration.

Where participants cannot be resolved, the process SHOULD preserve the strongest available traceable participant information and mark the Relationship for review.

Participant preservation MAY include:

- stable Object Identity;
- prior Object Identity;
- source identifiers;
- record identifiers;
- document identifiers;
- implementation identifiers;
- legacy identifiers;
- unresolved participant references;
- participant role information;
- participant provenance;
- participant privacy context;
- review-required status.

Import, export, and migration processes SHOULD preserve Object Identity.

When a Relationship connects Knowledge Objects, the process SHOULD refer to or resolve to stable Object Identity where practical.

An import, export, or migration process MUST NOT cause a Relationship to point to the wrong Knowledge Object because of filename changes, folder changes, title changes, storage changes, backlink changes, graph changes, search index changes, vector index changes, implementation-specific identifier changes, or hidden application state.

Import, export, and migration processes SHOULD preserve Relationship Type.

A process MUST NOT silently collapse Relationship Type into a generic relationship when type affects interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, workflow behavior, agent behavior, governance, publication, or downstream use.

Where exact Relationship Type cannot be mapped, the process SHOULD preserve the original type where practical, record the mapping uncertainty, and mark the Relationship for review.

Import, export, and migration processes SHOULD preserve Relationship Direction.

A process MUST NOT silently lose, reverse, collapse, infer, duplicate, or reinterpret Relationship Direction when direction affects meaning.

Where exact Relationship Direction cannot be mapped, the process SHOULD preserve the original direction where practical, record the mapping uncertainty, and mark the Relationship for review.

Import, export, and migration processes SHOULD preserve Relationship Strength and Relationship Confidence.

Relationship Strength and Relationship Confidence MUST remain distinguishable during import, export, and migration.

A process MUST NOT convert strength into confidence, confidence into strength, either value into authority, or either value into approval unless a future governed specification explicitly defines that behavior.

Import, export, and migration processes SHOULD preserve Relationship Provenance.

A process SHOULD preserve enough provenance to determine where the Relationship came from, what supports it, who or what created or changed it, whether it was inferred, reviewed, imported, migrated, validated, approved, rejected, deprecated, superseded, or generated by an agent or workflow.

Import provenance MAY identify:

- the import source;
- the import process;
- the prior representation;
- the prior identifier;
- the mapping rule used;
- the transformation applied;
- unresolved information;
- validation results;
- review-required status.

Export provenance MAY identify:

- the export process;
- the export target;
- the representation produced;
- the fields included;
- the fields withheld;
- the privacy rules applied;
- the validation results;
- the compatibility warnings.

Migration provenance MAY identify:

- the prior storage system;
- the new storage system;
- the prior representation;
- the new representation;
- the prior identifier;
- the new identifier;
- the migration mapping;
- the transformation applied;
- the validation result;
- the unresolved information;
- the review-required status.

Import, export, and migration processes SHOULD preserve Relationship Lifecycle State.

A proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or needs-review Relationship SHOULD remain distinguishable after import, export, or migration.

A rejected, deprecated, superseded, archived, or needs-review Relationship MUST NOT become active merely because it was imported, exported, migrated, restored, synchronized, indexed, displayed, or represented in another implementation.

Import, export, and migration processes SHOULD preserve Relationship Authority.

A process MUST NOT allow lower-authority Relationships, agents, workflows, implementations, sources, imports, exports, migrations, or validation results to override higher-authority documents, standards, decisions, specifications, privacy rules, validation rules, workflow rules, or governance rules.

Import, export, and migration processes MUST preserve Relationship Privacy.

A process MUST NOT expose restricted Relationships, restricted Relationship Participants, restricted Relationship Types, restricted Relationship Direction, restricted Relationship Strength, restricted Relationship Confidence, restricted Relationship Provenance, restricted Relationship Lifecycle State, restricted Relationship Authority, restricted validation results, or restricted relationship context.

Where Relationship Privacy cannot be preserved safely, the Relationship SHOULD be restricted, redacted, withheld, excluded, or marked for review according to the stricter applicable privacy expectation unless a future governed privacy specification defines different behavior.

Import, export, and migration processes SHOULD preserve Relationship Validation.

A process SHOULD preserve validation state where validation affects interpretation, governance, privacy, migration, import, export, publication, workflow behavior, agent behavior, or downstream use.

A validation result MUST NOT be silently converted into approval.

A validation warning MUST NOT be silently removed when the warning affects meaning, authority, privacy, lifecycle state, compatibility, migration, import, export, publication, or downstream use.

Import, export, and migration processes SHOULD preserve Relationship Compatibility.

A process SHOULD preserve enough compatibility information to determine whether the Relationship remains meaningful, portable, reviewable, privacy-respecting, validatable, and interpretable after movement or transformation.

Where compatibility cannot be confirmed, the process SHOULD mark the Relationship for review.

Import, export, and migration processes SHOULD preserve source distinction.

A process MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

A Relationship between a Knowledge Record and Source Material SHOULD preserve whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role where that distinction affects interpretation.

Import, export, and migration processes SHOULD preserve implementation independence.

A Relationship MUST NOT become dependent on implementation-specific links, backlinks, graph edges, database relations, plugin behavior, application state, user interface position, cached indexes, vector indexes, search indexes, folder paths, filenames, tags, aliases, or storage-specific identifiers when the Relationship affects meaning.

Implementation-specific representations MAY be imported, exported, or migrated as supporting information.

Implementation-specific representations MUST NOT replace governed Relationship meaning.

Import, export, and migration processes SHOULD support mapping.

A mapping MAY describe how a Relationship, participant, type, direction, strength, confidence, provenance, lifecycle state, authority, privacy classification, validation state, compatibility note, identifier, or implementation-specific reference is transformed between representations.

A mapping SHOULD be explicit where transformation affects meaning, authority, privacy, validation, compatibility, governance, publication, or downstream use.

A mapping MUST NOT silently change governed relationship meaning.

Import, export, and migration processes SHOULD support conflict detection.

Conflicts MAY include:

- unresolved participants;
- duplicate Relationships;
- conflicting Relationship Types;
- conflicting Relationship Direction;
- conflicting Relationship Strength;
- conflicting Relationship Confidence;
- conflicting provenance;
- conflicting lifecycle states;
- conflicting authority expectations;
- conflicting privacy classifications;
- conflicting validation results;
- conflicting compatibility results;
- conflicting import mappings;
- conflicting export mappings;
- conflicting migration mappings;
- conflicting implementation representations.

A conflict SHOULD be marked for review when it affects meaning, authority, privacy, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

Import, export, and migration processes SHOULD support graceful degradation.

When full Relationship information cannot be preserved, the process SHOULD preserve the strongest available traceable information and mark the Relationship for review.

Graceful degradation MUST NOT silently pretend that a Relationship is fully valid, approved, authoritative, private, portable, or compatible when required relationship information is missing, conflicting, ambiguous, unsafe, or unresolved.

Import, export, and migration processes SHOULD support validation.

A validator SHOULD be able to determine whether:

- Relationship Participants were preserved;
- Object Identity was preserved where applicable;
- Relationship Type was preserved where required;
- Relationship Direction was preserved where required;
- Relationship Strength and Relationship Confidence remain distinguishable;
- Relationship Provenance remains sufficient;
- Relationship Lifecycle State remains clear;
- Relationship Authority remains clear;
- Relationship Privacy was preserved;
- Relationship Validation state remains clear;
- Relationship Compatibility remains clear;
- source distinction was preserved;
- implementation-specific behavior did not redefine relationship meaning;
- unresolved information was marked for review;
- conflicts were identified where practical;
- mappings were preserved where required.

Import, export, and migration behavior is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can move Relationships into, out of, and across compliant environments without losing meaning, breaking identity, weakening privacy, confusing authority, erasing provenance, collapsing lifecycle state, invalidating validation results, or creating implementation lock-in.

## 15. Inferred Relationships

Inferred Relationships are Relationships proposed or derived from evidence, metadata, content similarity, source material, agent analysis, workflow activity, validation output, import behavior, migration behavior, implementation signals, or other governed inference bases.

Inferred Relationships exist so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can distinguish between Relationships that are explicitly approved and Relationships that have been suggested, detected, estimated, or derived.

An Inferred Relationship MAY be useful.

An Inferred Relationship MUST NOT be treated as approved merely because it exists.

An Inferred Relationship MUST NOT be treated as authoritative merely because it was detected by an agent, workflow, implementation, search system, graph system, backlink system, vector system, validation process, import process, export process, or migration process.

An Inferred Relationship SHOULD remain reviewable where it affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, workflow behavior, agent behavior, governance, publication, migration, import, export, or downstream use.

Inference MAY be based on:

- source material;
- metadata;
- explicit textual references;
- citations;
- shared identifiers;
- content similarity;
- semantic similarity;
- duplicate-detection signals;
- graph analysis;
- backlink analysis;
- search results;
- vector similarity;
- workflow output;
- agent analysis;
- validation output;
- import mappings;
- export mappings;
- migration mappings;
- implementation-specific signals;
- human notes;
- other governed inference bases.

Inference basis SHOULD be preserved where it affects interpretation.

An Inferred Relationship SHOULD preserve enough provenance to identify why the Relationship was inferred.

Inference provenance MAY identify:

- what inference basis was used;
- what source material was considered;
- what metadata was considered;
- what agent produced the inference;
- what workflow produced the inference;
- what validation process produced the inference;
- what import process produced the inference;
- what migration process produced the inference;
- what implementation signal produced the inference;
- what confidence value was assigned;
- what strength value was assigned;
- whether human review occurred;
- whether review is required.

An Inferred Relationship SHOULD preserve Relationship Participants.

The participants of an Inferred Relationship SHOULD be identifiable enough for future review.

An Inferred Relationship MUST NOT point to a Knowledge Object, Knowledge Record, Source Material, standard, decision, workflow, implementation, identifier, or governed entity merely because of filename similarity, folder proximity, title similarity, backlink behavior, graph layout, search ranking, tag coincidence, vector similarity, or implementation-specific behavior when that inference affects meaning.

Those signals MAY support inference.

They MUST NOT replace participant identity where participant identity affects meaning, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

An Inferred Relationship SHOULD preserve Object Identity.

When an Inferred Relationship connects Knowledge Objects, the Relationship SHOULD refer to or resolve to stable Object Identity where practical.

An inferred participant match MUST NOT become a stable identity claim unless a governed review or validation process confirms it where confirmation is required.

An Inferred Relationship SHOULD preserve Relationship Type.

Where Relationship Type is inferred, the inferred type SHOULD remain distinguishable from a reviewed or approved type.

An inferred Relationship Type MUST NOT be treated as approved merely because the inference appears plausible, repeated, indexed, displayed, or frequently used.

Where exact Relationship Type cannot be inferred safely, the Relationship SHOULD be marked as generic, uncertain, proposed, or needing review rather than silently assigned a specific type.

An Inferred Relationship SHOULD preserve Relationship Direction.

Where Relationship Direction is inferred, the inferred direction SHOULD remain distinguishable from reviewed or approved direction.

An inferred direction MUST NOT be treated as approved merely because it appears in a backlink, graph view, search result, vector result, folder order, filename order, citation order, index order, or implementation display.

Where direction cannot be inferred safely, the Relationship SHOULD be marked as direction-uncertain or needing review rather than silently assigned a direction.

An Inferred Relationship MAY include Relationship Strength.

An Inferred Relationship MAY include Relationship Confidence.

Inferred Relationship Strength and Inferred Relationship Confidence MUST remain distinguishable.

A strong inferred Relationship may still have low confidence.

A high-confidence inferred Relationship may still require review before use.

Inferred Relationship Strength MUST NOT be treated as approval.

Inferred Relationship Confidence MUST NOT be treated as approval.

An Inferred Relationship SHOULD preserve lifecycle state.

An Inferred Relationship SHOULD be marked as inferred, proposed, needs review, or governed by a future lifecycle state unless a governed review or approval process changes that state.

An Inferred Relationship MUST NOT silently become approved during import, export, migration, validation, indexing, synchronization, backup, restoration, workflow activity, agent activity, or implementation replacement.

A rejected inferred Relationship MUST NOT remain active merely because the original inference signal remains present.

A deprecated or superseded inferred Relationship SHOULD preserve enough historical context to explain why the inferred Relationship is no longer recommended or has been replaced.

An Inferred Relationship SHOULD preserve authority boundaries.

An Inferred Relationship MUST NOT allow a lower-authority participant, agent, workflow, implementation, source, import process, migration process, validation result, or inference signal to override a higher-authority document, standard, decision, specification, privacy rule, validation rule, workflow rule, or governance rule.

An Inferred Relationship SHOULD NOT be treated as authoritative unless the applicable governance, validation, workflow, or approval expectations support that authority.

An Inferred Relationship MUST preserve privacy boundaries.

Inference MUST NOT expose restricted knowledge merely by revealing that a Relationship may exist.

Inference MUST NOT expose restricted participants, restricted Relationship Type, restricted Relationship Direction, restricted strength, restricted confidence, restricted provenance, restricted lifecycle state, restricted authority, restricted validation results, or sensitive relationship context to users, agents, workflows, indexes, graph views, summaries, exports, logs, caches, dashboards, APIs, plugins, or implementations that are not permitted to access them.

Where an inferred Relationship would expose sensitive meaning, restricted source material, protected identity, confidential reasoning, private workflow activity, restricted agent activity, or restricted implementation behavior, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

An Inferred Relationship SHOULD preserve source distinction.

An inference involving Source Material MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

Where Source Material supports an inferred Relationship, the inference SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role.

An Inferred Relationship SHOULD support validation.

A validator SHOULD be able to determine whether:

- the Relationship is inferred;
- the inference basis is present where required;
- the inference basis is understandable;
- Relationship Participants are identifiable;
- Object Identity is preserved where applicable;
- Relationship Type is inferred, reviewed, approved, uncertain, or missing;
- Relationship Direction is inferred, reviewed, approved, uncertain, or missing;
- Relationship Strength and Relationship Confidence remain distinguishable;
- Relationship Provenance remains sufficient;
- Relationship Lifecycle State remains clear;
- Relationship Authority is not overstated;
- Relationship Privacy is preserved;
- Relationship Compatibility is preserved;
- human review is required;
- the inferred Relationship should be accepted, revised, rejected, deprecated, superseded, archived, or escalated.

An Inferred Relationship SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, search process, graph process, vector process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, weaken, expose, duplicate, approve, reject, or replace an Inferred Relationship in a way that causes privacy exposure, loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Inferred Relationships are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine that a Relationship was inferred, what evidence or signal supported the inference, whether the Relationship requires review, whether privacy or authority is affected, whether the Relationship should be accepted or rejected, and whether the relationship remains interpretable across time and implementation replacement.

## 16. Agent-Generated Relationships

Agent-Generated Relationships are Relationships created, proposed, modified, classified, validated, enriched, reviewed, rejected, deprecated, superseded, or archived by an agent.

Agent-Generated Relationships exist so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can distinguish between Relationships created or changed by agents and Relationships created, reviewed, or approved through other governed processes.

An Agent-Generated Relationship MAY be useful.

An Agent-Generated Relationship MUST NOT be treated as approved merely because an agent generated it.

An Agent-Generated Relationship MUST NOT be treated as authoritative merely because an agent generated it, repeated it, displayed it, validated it, ranked it, recommended it, or used it in downstream output.

An Agent-Generated Relationship SHOULD remain reviewable where it affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, workflow behavior, governance, publication, migration, import, export, or downstream use.

An agent MAY generate a Relationship by:

- proposing a new Relationship;
- identifying possible Relationship Participants;
- assigning a Relationship Type;
- assigning Relationship Direction;
- assigning Relationship Strength;
- assigning Relationship Confidence;
- adding Relationship Context;
- adding Relationship Provenance;
- recommending a Relationship Lifecycle State;
- recommending Relationship Authority;
- applying Relationship Privacy handling;
- validating a Relationship;
- recommending correction;
- recommending rejection;
- recommending deprecation;
- recommending supersession;
- recommending archival;
- enriching an existing Relationship;
- identifying a duplicate Relationship;
- identifying a conflicting Relationship;
- identifying a missing Relationship;
- identifying a broken Relationship.

Agent generation MUST remain distinguishable from human approval.

Agent generation MUST remain distinguishable from workflow approval.

Agent generation MUST remain distinguishable from validation approval.

Agent generation MUST remain distinguishable from document authority.

An Agent-Generated Relationship SHOULD preserve enough provenance to identify the agent activity that produced or modified the Relationship.

Agent provenance MAY identify:

- the agent that generated or modified the Relationship;
- the agent role;
- the instruction or task that produced the Relationship;
- the workflow context where applicable;
- the source material considered;
- the Knowledge Objects or Knowledge Records considered;
- the metadata considered;
- the inference basis used;
- the validation basis used;
- the confidence basis used;
- the strength basis used;
- the date or event of generation where practical;
- whether human review occurred;
- whether review is required;
- whether the agent output was accepted, revised, rejected, deprecated, superseded, or archived.

An Agent-Generated Relationship SHOULD preserve Relationship Participants.

The participants of an Agent-Generated Relationship SHOULD be identifiable enough for future review.

An agent MUST NOT create or modify a Relationship Participant in a way that causes the Relationship to point to the wrong Knowledge Object, Knowledge Record, Source Material, standard, decision, workflow, implementation, identifier, or governed entity.

An agent MUST NOT rely only on filename similarity, folder proximity, title similarity, backlink behavior, graph layout, search ranking, tag coincidence, vector similarity, implementation-specific behavior, conversation memory, prompt context, or hidden tool state when participant identity affects meaning.

Those signals MAY support agent analysis.

They MUST NOT replace participant identity where participant identity affects meaning, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

An Agent-Generated Relationship SHOULD preserve Object Identity.

When an Agent-Generated Relationship connects Knowledge Objects, the Relationship SHOULD refer to or resolve to stable Object Identity where practical.

An agent-generated participant match MUST NOT become a stable identity claim unless a governed review or validation process confirms it where confirmation is required.

An Agent-Generated Relationship SHOULD preserve Relationship Type.

Where an agent assigns or modifies Relationship Type, the type SHOULD remain distinguishable as agent-generated unless it is later confirmed by a governed review or approval process.

An agent-assigned Relationship Type MUST NOT be treated as approved merely because the type appears plausible, repeated, indexed, displayed, validated, or frequently used.

Where exact Relationship Type cannot be assigned safely, the agent SHOULD mark the Relationship as generic, uncertain, proposed, inferred, or needing review rather than silently assigning a specific type.

An Agent-Generated Relationship SHOULD preserve Relationship Direction.

Where an agent assigns or modifies Relationship Direction, the direction SHOULD remain distinguishable as agent-generated unless it is later confirmed by a governed review or approval process.

An agent-assigned direction MUST NOT be treated as approved merely because it appears in source order, backlink order, graph view, search result, vector result, citation order, index order, implementation display, or generated text.

Where direction cannot be assigned safely, the agent SHOULD mark the Relationship as direction-uncertain or needing review rather than silently assigning direction.

An Agent-Generated Relationship MAY include Relationship Strength.

An Agent-Generated Relationship MAY include Relationship Confidence.

Agent-generated Relationship Strength and Agent-generated Relationship Confidence MUST remain distinguishable.

An agent-assigned strength value MUST NOT be treated as approval.

An agent-assigned confidence value MUST NOT be treated as approval.

An agent SHOULD preserve enough context to explain why strength or confidence was assigned where those values affect interpretation, validation, authority, privacy, compatibility, governance, publication, migration, import, export, workflow behavior, or downstream use.

An Agent-Generated Relationship SHOULD preserve lifecycle state.

An Agent-Generated Relationship SHOULD be marked as agent-generated, proposed, inferred, needs review, or governed by a future lifecycle state unless a governed review or approval process changes that state.

An Agent-Generated Relationship MUST NOT silently become approved during validation, indexing, synchronization, backup, restoration, import, export, migration, workflow activity, agent activity, or implementation replacement.

A rejected Agent-Generated Relationship MUST NOT remain active merely because the agent can regenerate it or because the original signal remains present.

A deprecated or superseded Agent-Generated Relationship SHOULD preserve enough historical context to explain why it is no longer recommended or has been replaced.

An Agent-Generated Relationship SHOULD preserve authority boundaries.

An Agent-Generated Relationship MUST NOT allow an agent, model output, prompt instruction, tool output, implementation, source, import process, migration process, validation result, inference signal, or lower-authority participant to override a higher-authority document, standard, decision, specification, privacy rule, validation rule, workflow rule, or governance rule.

An Agent-Generated Relationship SHOULD NOT be treated as authoritative unless the applicable governance, validation, workflow, or approval expectations support that authority.

Agent output MUST remain subordinate to governed documents.

An Agent-Generated Relationship MUST preserve privacy boundaries.

An agent MUST NOT expose restricted knowledge merely by generating, proposing, summarizing, indexing, classifying, validating, or displaying a Relationship.

An agent MUST NOT expose restricted participants, restricted Relationship Type, restricted Relationship Direction, restricted strength, restricted confidence, restricted provenance, restricted lifecycle state, restricted authority, restricted validation results, restricted source material, private reasoning, private workflow activity, or sensitive relationship context to users, agents, workflows, indexes, graph views, summaries, exports, logs, caches, dashboards, APIs, plugins, or implementations that are not permitted to access them.

Where an Agent-Generated Relationship would expose sensitive meaning, restricted source material, protected identity, confidential reasoning, private workflow activity, restricted agent activity, or restricted implementation behavior, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

An Agent-Generated Relationship SHOULD preserve source distinction.

An agent MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

Where Source Material supports an Agent-Generated Relationship, the Relationship SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role.

An Agent-Generated Relationship SHOULD preserve agent boundaries.

An agent MAY propose, classify, enrich, validate, or recommend Relationships only within the permissions, privacy boundaries, workflow expectations, and governance rules applicable to that agent.

An agent MUST NOT silently approve, reject, expose, publish, export, migrate, delete, or modify a Relationship unless the relevant agent standard, workflow rule, privacy rule, validation rule, and governance rule allow that behavior.

An agent SHOULD escalate Relationships for human review where the Relationship affects authority, privacy, publication, governance, high-impact interpretation, migration, import, export, or downstream use.

An Agent-Generated Relationship SHOULD preserve workflow boundaries.

When an agent acts within a workflow, the Relationship SHOULD preserve enough context to determine the workflow, task, trigger, input, output, review state, and approval state where those details affect interpretation.

A workflow using an agent MUST NOT treat agent completion as approval unless the applicable workflow rule or future governed specification explicitly defines that behavior.

An Agent-Generated Relationship SHOULD preserve implementation boundaries.

An implementation MAY assist an agent by providing search results, graph results, vector results, metadata, links, backlinks, indexes, summaries, validation results, or source material.

Implementation-provided signals MUST NOT become governed Relationship meaning merely because an agent used them.

An agent MUST NOT redefine relationship behavior through implementation-specific assumptions unless those assumptions are clearly marked as implementation-specific and remain subordinate to The Brain Standard.

An Agent-Generated Relationship SHOULD support validation.

A validator SHOULD be able to determine whether:

- the Relationship is agent-generated;
- the responsible agent is identifiable where required;
- the agent role or task is understandable where required;
- the generation basis is present where required;
- Relationship Participants are identifiable;
- Object Identity is preserved where applicable;
- Relationship Type is agent-generated, reviewed, approved, uncertain, or missing;
- Relationship Direction is agent-generated, reviewed, approved, uncertain, or missing;
- Relationship Strength and Relationship Confidence remain distinguishable;
- Relationship Provenance remains sufficient;
- Relationship Lifecycle State remains clear;
- Relationship Authority is not overstated;
- Relationship Privacy is preserved;
- Relationship Compatibility is preserved;
- human review is required;
- the Agent-Generated Relationship should be accepted, revised, rejected, deprecated, superseded, archived, or escalated.

An Agent-Generated Relationship SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, search process, graph process, vector process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, weaken, expose, duplicate, approve, reject, or replace an Agent-Generated Relationship in a way that causes privacy exposure, loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Agent-Generated Relationships are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine that a Relationship was generated or modified by an agent, what agent activity produced it, what evidence or signal supported it, whether review is required, whether privacy or authority is affected, whether the Relationship should be accepted or rejected, and whether the relationship remains interpretable across time and implementation replacement.

## 17. Workflow-Generated Relationships

Workflow-Generated Relationships are Relationships created, proposed, modified, classified, validated, enriched, reviewed, approved, rejected, deprecated, superseded, archived, routed, or maintained through a governed workflow.

Workflow-Generated Relationships exist so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can distinguish between Relationships created or changed through workflow execution and Relationships created, reviewed, approved, or modified through other governed processes.

A Workflow-Generated Relationship MAY be useful.

A Workflow-Generated Relationship MUST NOT be treated as approved merely because a workflow generated it.

A Workflow-Generated Relationship MUST NOT be treated as authoritative merely because a workflow generated it, routed it, displayed it, validated it, repeated it, accepted it, exported it, migrated it, synchronized it, or used it in downstream output.

A Workflow-Generated Relationship SHOULD remain reviewable where it affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, agent behavior, governance, publication, migration, import, export, or downstream use.

A workflow MAY generate or modify a Relationship by:

- proposing a new Relationship;
- identifying Relationship Participants;
- assigning a Relationship Type;
- assigning Relationship Direction;
- assigning Relationship Strength;
- assigning Relationship Confidence;
- adding Relationship Context;
- adding Relationship Provenance;
- assigning or recommending a Relationship Lifecycle State;
- assigning or recommending Relationship Authority;
- applying Relationship Privacy handling;
- validating a Relationship;
- routing a Relationship for review;
- routing a Relationship for approval;
- recommending correction;
- recommending rejection;
- recommending deprecation;
- recommending supersession;
- recommending archival;
- enriching an existing Relationship;
- identifying a duplicate Relationship;
- identifying a conflicting Relationship;
- identifying a missing Relationship;
- identifying a broken Relationship;
- producing an import, export, or migration result.

Workflow generation MUST remain distinguishable from human approval.

Workflow generation MUST remain distinguishable from agent generation.

Workflow generation MUST remain distinguishable from validation approval.

Workflow generation MUST remain distinguishable from document authority.

A workflow MAY include human steps, agent steps, validation steps, implementation steps, import steps, export steps, migration steps, review steps, approval steps, or publication steps.

A Relationship produced by a workflow SHOULD preserve enough context to determine which steps affected the Relationship where those steps affect interpretation.

A Workflow-Generated Relationship SHOULD preserve enough provenance to identify the workflow activity that produced or modified the Relationship.

Workflow provenance MAY identify:

- the workflow that generated or modified the Relationship;
- the workflow version where practical;
- the workflow trigger;
- the workflow step that produced the Relationship;
- the actor responsible for the step where applicable;
- the agent involved where applicable;
- the validator involved where applicable;
- the source material considered;
- the Knowledge Objects or Knowledge Records considered;
- the metadata considered;
- the inference basis used;
- the validation basis used;
- the confidence basis used;
- the strength basis used;
- the import, export, or migration process involved;
- whether human review occurred;
- whether approval occurred;
- whether review is required;
- whether the workflow output was accepted, revised, rejected, deprecated, superseded, or archived.

A Workflow-Generated Relationship SHOULD preserve Relationship Participants.

The participants of a Workflow-Generated Relationship SHOULD be identifiable enough for future review.

A workflow MUST NOT create or modify a Relationship Participant in a way that causes the Relationship to point to the wrong Knowledge Object, Knowledge Record, Source Material, standard, decision, workflow, implementation, identifier, or governed entity.

A workflow MUST NOT rely only on filename similarity, folder proximity, title similarity, backlink behavior, graph layout, search ranking, tag coincidence, vector similarity, implementation-specific behavior, workflow state, temporary routing state, queue state, automation state, or hidden tool state when participant identity affects meaning.

Those signals MAY support workflow activity.

They MUST NOT replace participant identity where participant identity affects meaning, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.

A Workflow-Generated Relationship SHOULD preserve Object Identity.

When a Workflow-Generated Relationship connects Knowledge Objects, the Relationship SHOULD refer to or resolve to stable Object Identity where practical.

A workflow-generated participant match MUST NOT become a stable identity claim unless a governed review or validation process confirms it where confirmation is required.

A Workflow-Generated Relationship SHOULD preserve Relationship Type.

Where a workflow assigns or modifies Relationship Type, the type SHOULD remain distinguishable as workflow-generated unless it is later confirmed by a governed review or approval process.

A workflow-assigned Relationship Type MUST NOT be treated as approved merely because the workflow completed, repeated, displayed, validated, exported, migrated, or synchronized it.

Where exact Relationship Type cannot be assigned safely, the workflow SHOULD mark the Relationship as generic, uncertain, proposed, inferred, or needing review rather than silently assigning a specific type.

A Workflow-Generated Relationship SHOULD preserve Relationship Direction.

Where a workflow assigns or modifies Relationship Direction, the direction SHOULD remain distinguishable as workflow-generated unless it is later confirmed by a governed review or approval process.

A workflow-assigned direction MUST NOT be treated as approved merely because it appears in source order, routing order, task order, backlink order, graph view, search result, vector result, citation order, index order, implementation display, or generated output.

Where direction cannot be assigned safely, the workflow SHOULD mark the Relationship as direction-uncertain or needing review rather than silently assigning direction.

A Workflow-Generated Relationship MAY include Relationship Strength.

A Workflow-Generated Relationship MAY include Relationship Confidence.

Workflow-generated Relationship Strength and Workflow-generated Relationship Confidence MUST remain distinguishable.

A workflow-assigned strength value MUST NOT be treated as approval.

A workflow-assigned confidence value MUST NOT be treated as approval.

A workflow SHOULD preserve enough context to explain why strength or confidence was assigned where those values affect interpretation, validation, authority, privacy, compatibility, governance, publication, migration, import, export, agent behavior, or downstream use.

A Workflow-Generated Relationship SHOULD preserve lifecycle state.

A Workflow-Generated Relationship SHOULD be marked as workflow-generated, proposed, inferred, reviewed, approved, rejected, deprecated, superseded, archived, needs review, or governed by a future lifecycle state as applicable.

A Workflow-Generated Relationship MUST NOT silently become approved merely because the workflow completed unless the applicable workflow rule or future governed specification explicitly defines that completion as approval.

A rejected Workflow-Generated Relationship MUST NOT remain active merely because the workflow can regenerate it or because the original workflow signal remains present.

A deprecated or superseded Workflow-Generated Relationship SHOULD preserve enough historical context to explain why it is no longer recommended or has been replaced.

A Workflow-Generated Relationship SHOULD preserve authority boundaries.

A Workflow-Generated Relationship MUST NOT allow a workflow, automation step, agent, validator, implementation, source, import process, migration process, validation result, inference signal, or lower-authority participant to override a higher-authority document, standard, decision, specification, privacy rule, validation rule, workflow rule, or governance rule.

A Workflow-Generated Relationship SHOULD NOT be treated as authoritative unless the applicable governance, validation, workflow, review, or approval expectations support that authority.

Workflow output MUST remain subordinate to governed documents.

A Workflow-Generated Relationship MUST preserve privacy boundaries.

A workflow MUST NOT expose restricted knowledge merely by generating, routing, summarizing, indexing, classifying, validating, exporting, migrating, synchronizing, publishing, or displaying a Relationship.

A workflow MUST NOT expose restricted participants, restricted Relationship Type, restricted Relationship Direction, restricted strength, restricted confidence, restricted provenance, restricted lifecycle state, restricted authority, restricted validation results, restricted source material, private reasoning, private agent activity, private workflow activity, or sensitive relationship context to users, agents, workflows, indexes, graph views, summaries, exports, logs, caches, dashboards, APIs, plugins, or implementations that are not permitted to access them.

Where a Workflow-Generated Relationship would expose sensitive meaning, restricted source material, protected identity, confidential reasoning, private workflow activity, restricted agent activity, or restricted implementation behavior, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

A Workflow-Generated Relationship SHOULD preserve source distinction.

A workflow MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

Where Source Material supports a Workflow-Generated Relationship, the Relationship SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role.

A Workflow-Generated Relationship SHOULD preserve agent boundaries.

When an agent participates in a workflow, the Relationship SHOULD preserve enough context to determine what was generated by the agent and what was generated, routed, approved, rejected, or modified by the workflow.

A workflow MUST NOT treat agent completion as approval unless the applicable workflow rule or future governed specification explicitly defines that behavior.

A Workflow-Generated Relationship SHOULD preserve workflow boundaries.

A workflow MAY propose, classify, enrich, validate, route, approve, reject, deprecate, supersede, archive, import, export, migrate, publish, or synchronize Relationships only within the permissions, privacy boundaries, validation expectations, and governance rules applicable to that workflow.

A workflow MUST NOT silently approve, reject, expose, publish, export, migrate, delete, or modify a Relationship unless the relevant workflow rule, privacy rule, validation rule, and governance rule allow that behavior.

A workflow SHOULD escalate Relationships for human review where the Relationship affects authority, privacy, publication, governance, high-impact interpretation, migration, import, export, or downstream use.

A Workflow-Generated Relationship SHOULD preserve implementation boundaries.

An implementation MAY assist a workflow by providing routing, queues, forms, search results, graph results, vector results, metadata, links, backlinks, indexes, summaries, validation results, permissions, or source material.

Implementation-provided signals MUST NOT become governed Relationship meaning merely because a workflow used them.

A workflow MUST NOT redefine relationship behavior through implementation-specific assumptions unless those assumptions are clearly marked as implementation-specific and remain subordinate to The Brain Standard.

A Workflow-Generated Relationship SHOULD support validation.

A validator SHOULD be able to determine whether:

- the Relationship is workflow-generated;
- the responsible workflow is identifiable where required;
- the workflow role or task is understandable where required;
- the generation basis is present where required;
- Relationship Participants are identifiable;
- Object Identity is preserved where applicable;
- Relationship Type is workflow-generated, reviewed, approved, uncertain, or missing;
- Relationship Direction is workflow-generated, reviewed, approved, uncertain, or missing;
- Relationship Strength and Relationship Confidence remain distinguishable;
- Relationship Provenance remains sufficient;
- Relationship Lifecycle State remains clear;
- Relationship Authority is not overstated;
- Relationship Privacy is preserved;
- Relationship Compatibility is preserved;
- human review is required;
- the Workflow-Generated Relationship should be accepted, revised, rejected, deprecated, superseded, archived, or escalated.

A Workflow-Generated Relationship SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, search process, graph process, vector process, routing process, queue process, or storage system MUST NOT silently discard, collapse, rename, reinterpret, weaken, expose, duplicate, approve, reject, or replace a Workflow-Generated Relationship in a way that causes privacy exposure, loss of meaning, broken provenance, lifecycle ambiguity, authority ambiguity, validation failure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Workflow-Generated Relationships are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine that a Relationship was generated or modified by a workflow, what workflow activity produced it, what evidence or signal supported it, whether review is required, whether privacy or authority is affected, whether the Relationship should be accepted or rejected, and whether the relationship remains interpretable across time and implementation replacement.

## 18. Implementation Boundaries

Implementation Boundaries define how implementations may store, display, index, search, link, visualize, validate, import, export, migrate, synchronize, back up, restore, or process Relationships without redefining relationship meaning.

Implementation Boundaries exist so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can distinguish governed Relationships from implementation-specific behavior.

An implementation MAY represent a Relationship through implementation-specific structures.

Implementation-specific structures MAY include:

- links;
- backlinks;
- graph edges;
- database relations;
- file references;
- metadata fields;
- indexes;
- search associations;
- vector records;
- embeddings;
- tags;
- aliases;
- folders;
- dashboards;
- user interface elements;
- plugin state;
- caches;
- APIs;
- synchronization records;
- import records;
- export records;
- migration records;
- other implementation-specific representations.

Implementation-specific structures MAY support Relationship storage, display, search, indexing, visualization, validation, import, export, migration, synchronization, backup, restoration, navigation, or workflow behavior.

Implementation-specific structures MUST NOT replace governed Relationship meaning where the Relationship affects interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

A Relationship MUST remain interpretable outside any single implementation where the Relationship affects meaning.

An implementation MUST NOT define Relationship meaning solely through:

- folder location;
- filename;
- title;
- tag;
- alias;
- backlink behavior;
- graph layout;
- database row;
- storage path;
- search ranking;
- vector similarity;
- cached index;
- plugin behavior;
- user interface position;
- hidden application state;
- implementation-specific identifier;
- undocumented implementation convention.

Those signals MAY assist implementation behavior.

They MUST NOT become governed Relationship meaning unless a future governed specification explicitly defines how they are interpreted.

Implementation behavior MUST remain subordinate to The Brain Standard.

An implementation MUST NOT override the meaning of Relationship Participants, Relationship Type, Relationship Direction, Relationship Strength, Relationship Confidence, Relationship Provenance, Relationship Lifecycle State, Relationship Authority, Relationship Privacy, Relationship Validation, Relationship Compatibility, or import, export, and migration behavior.

An implementation MAY add implementation-specific convenience features.

Convenience features MAY include:

- relationship previews;
- backlink panels;
- graph views;
- search views;
- relationship filters;
- relationship dashboards;
- relationship recommendations;
- relationship warnings;
- relationship validation reports;
- relationship import tools;
- relationship export tools;
- relationship migration tools;
- relationship synchronization tools;
- relationship navigation tools.

Convenience features MUST NOT create, approve, reject, deprecate, supersede, expose, hide, collapse, reverse, duplicate, or reinterpret governed Relationships unless the relevant standard, specification, workflow rule, privacy rule, validation rule, or governance rule allows that behavior.

An implementation SHOULD make implementation-specific behavior distinguishable from governed Relationship behavior where the distinction affects interpretation.

For example:

- a backlink may suggest a possible Relationship, but it does not define Relationship Type by itself;
- a graph edge may visualize a Relationship, but it does not define Relationship Direction by itself;
- a vector result may suggest similarity, but it does not approve an Inferred Relationship by itself;
- a tag may assist discovery, but it does not define authority by itself;
- a folder may support organization, but it does not define participant identity by itself;
- a database relation may store a Relationship, but it does not redefine governed Relationship meaning by itself.

Implementation Boundaries SHOULD preserve Relationship Participants.

An implementation MUST NOT cause a Relationship to point to the wrong Knowledge Object, Knowledge Record, Source Material, standard, decision, workflow, implementation, identifier, or governed entity because of renaming, moving, copying, indexing, caching, synchronization, backup, restoration, import, export, migration, plugin behavior, database behavior, or user interface behavior.

Implementation Boundaries SHOULD preserve Object Identity.

When a Relationship connects Knowledge Objects, an implementation SHOULD refer to or resolve to stable Object Identity where practical.

An implementation MUST NOT substitute filenames, folder paths, titles, aliases, database row identifiers, temporary identifiers, interface identifiers, cache identifiers, plugin identifiers, or hidden application identifiers for stable Object Identity where Object Identity affects Relationship meaning.

Implementation Boundaries SHOULD preserve Relationship Type.

An implementation MUST NOT silently collapse materially different Relationship Types into a generic connection when type affects interpretation.

An implementation MAY store or display Relationship Types using implementation-specific labels, fields, icons, colors, menus, graph styles, or database values.

Such representations MUST remain mappable to governed Relationship meaning where type affects interpretation.

Implementation Boundaries SHOULD preserve Relationship Direction.

An implementation MUST NOT silently lose, reverse, collapse, infer, duplicate, or reinterpret Relationship Direction when direction affects meaning.

An implementation MAY display Relationships in simplified, non-directional, visual, or bidirectional forms for usability.

Such display behavior MUST NOT remove governed direction where direction affects interpretation.

Implementation Boundaries SHOULD preserve Relationship Strength and Relationship Confidence.

An implementation MUST NOT convert strength into confidence, confidence into strength, either value into authority, or either value into approval unless a future governed specification explicitly defines that behavior.

An implementation MAY display strength or confidence through labels, scores, icons, colors, filters, dashboards, or ranking behavior.

Such display behavior MUST NOT hide uncertainty, review requirements, lifecycle state, authority limits, or privacy boundaries.

Implementation Boundaries SHOULD preserve Relationship Provenance.

An implementation MUST NOT silently discard, hide, collapse, overwrite, or reinterpret provenance where provenance affects interpretation, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, governance, publication, or downstream use.

Implementation-generated provenance SHOULD remain distinguishable from human-created, agent-generated, workflow-generated, imported, migrated, inferred, reviewed, approved, rejected, deprecated, superseded, or archived provenance.

Implementation Boundaries SHOULD preserve Relationship Lifecycle State.

An implementation MUST NOT silently convert proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or needs-review Relationships into another lifecycle state.

A Relationship MUST NOT become active, approved, authoritative, or safe for downstream use merely because an implementation displays, indexes, exports, imports, migrates, synchronizes, restores, or validates it.

Implementation Boundaries SHOULD preserve Relationship Authority.

An implementation MUST NOT treat storage behavior, display behavior, graph behavior, search behavior, backlink behavior, vector behavior, plugin behavior, database behavior, workflow completion, agent output, or user interface state as governance authority unless a governed standard, specification, workflow rule, or decision explicitly defines that behavior.

Implementation output MUST remain subordinate to governed documents.

Implementation Boundaries MUST preserve Relationship Privacy.

An implementation MUST NOT expose restricted Relationships, restricted Relationship Participants, restricted Relationship Types, restricted Relationship Direction, restricted strength, restricted confidence, restricted provenance, restricted lifecycle state, restricted authority, restricted validation results, restricted source material, private reasoning, private agent activity, private workflow activity, or sensitive relationship context through user interface behavior, search behavior, graph behavior, indexing behavior, caching behavior, logging behavior, synchronization behavior, backup behavior, export behavior, import behavior, migration behavior, plugin behavior, API behavior, dashboard behavior, or recommendation behavior.

Where implementation behavior could expose sensitive meaning, restricted source material, protected identity, confidential reasoning, private workflow activity, restricted agent activity, or restricted implementation behavior, the Relationship SHOULD be handled according to the stricter applicable privacy classification unless a future governed privacy specification defines different behavior.

Implementation Boundaries SHOULD preserve Relationship Validation.

An implementation MAY provide validation tools, validation warnings, validation reports, validation dashboards, validation indexes, or validation automation.

Implementation validation MUST remain distinguishable from governed approval unless a future governed specification explicitly defines that validation as approval.

An implementation MUST NOT hide validation failures, privacy failures, authority conflicts, lifecycle ambiguity, unresolved participants, broken relationships, compatibility warnings, import warnings, export warnings, or migration warnings where those issues affect interpretation or downstream use.

Implementation Boundaries SHOULD preserve Relationship Compatibility.

A compliant implementation SHOULD preserve governed Relationship meaning across storage, display, indexing, search, graph views, backlinks, vector indexes, metadata, APIs, plugins, caches, logs, backups, restorations, synchronizations, imports, exports, migrations, workflows, agents, validators, and implementation replacement.

An implementation MUST NOT create implementation lock-in by making governed Relationship meaning dependent on private state, proprietary indexes, undocumented behavior, hidden identifiers, plugin-only structures, non-exportable fields, or inaccessible application data.

Implementation Boundaries SHOULD preserve source distinction.

An implementation MUST NOT cause Source Material and Knowledge Records to be treated as the same entity through storage behavior, display behavior, graph behavior, backlink behavior, search behavior, indexing behavior, vector behavior, import behavior, export behavior, migration behavior, or user interface behavior.

An implementation MAY display Source Material and Knowledge Records together for usability.

Such display behavior MUST preserve the distinction between original source material and structured knowledge where that distinction affects interpretation.

Implementation Boundaries SHOULD preserve agent boundaries.

An implementation MAY provide tools, source material, metadata, search results, graph results, vector results, validation results, summaries, indexes, dashboards, or APIs to agents.

Implementation-provided signals MUST NOT become governed Relationship meaning merely because an agent used them.

An implementation MUST NOT allow an agent to access, infer, summarize, export, index, transform, publish, or expose Relationships beyond the relevant privacy classification, permission model, workflow expectation, and governance rule.

Implementation Boundaries SHOULD preserve workflow boundaries.

An implementation MAY support workflow routing, queues, forms, tasks, review states, approval states, validation steps, import steps, export steps, migration steps, synchronization steps, or publication steps.

Implementation workflow mechanics MUST NOT become governance authority merely because the implementation completed, displayed, stored, routed, synchronized, exported, imported, or migrated a workflow step.

Implementation Boundaries SHOULD support validation.

A validator SHOULD be able to determine whether:

- implementation-specific behavior is distinguishable from governed Relationship behavior;
- Relationship Participants remain identifiable;
- Object Identity is preserved where applicable;
- Relationship Type is preserved where required;
- Relationship Direction is preserved where required;
- Relationship Strength and Relationship Confidence remain distinguishable;
- Relationship Provenance remains sufficient;
- Relationship Lifecycle State remains clear;
- Relationship Authority is not overstated;
- Relationship Privacy is preserved;
- Relationship Validation state remains clear;
- Relationship Compatibility is preserved;
- source distinction is preserved;
- agent boundaries are preserved;
- workflow boundaries are preserved;
- implementation-specific structures do not redefine relationship meaning;
- implementation-specific behavior does not create lock-in.

Implementation Boundaries are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can use specific tools, vaults, databases, file systems, interfaces, plugins, APIs, indexes, graphs, search systems, vector systems, agents, and workflow environments without allowing implementation behavior to redefine Relationship meaning, weaken privacy, confuse authority, erase provenance, collapse lifecycle state, invalidate validation, break compatibility, or create implementation lock-in.

## 19. Governance and Evolution

Governance and Evolution define how Relationship rules, Relationship interpretations, Relationship specifications, Relationship vocabularies, Relationship validation behavior, and Relationship-compatible implementations may change over time without weakening the meaning of The Brain Standard.

Governance and Evolution exist so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can revise, extend, deprecate, supersede, or refine relationship behavior while preserving identity, meaning, provenance, lifecycle state, authority, privacy, validation, compatibility, and implementation independence.

KS-0004 is governed by the constitutional foundation of The Brain Standard.

KS-0004 MUST remain subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

A future relationship specification, storage standard, agent standard, workflow standard, implementation document, validation specification, graph specification, relationship vocabulary, import format, export format, migration mapping, or operational guide MUST NOT contradict KS-0004 unless KS-0004 is formally revised, superseded, or deprecated through governance.

Relationship governance SHOULD preserve the purpose of KS-0004.

Relationship governance SHOULD ensure that Relationships remain:

- explicit;
- interpretable;
- portable;
- traceable;
- reviewable;
- privacy-respecting;
- validatable;
- compatible;
- implementation-independent;
- governed across time.

A future specification MAY refine Relationship behavior.

A future specification MAY define:

- exact Relationship identifiers;
- exact Relationship records;
- exact Relationship metadata fields;
- exact Relationship Type vocabularies;
- exact inverse Relationship rules;
- exact participant-role rules;
- exact direction rules;
- exact cardinality rules;
- exact strength values;
- exact confidence values;
- exact provenance fields;
- exact lifecycle values;
- exact authority values;
- exact privacy values;
- exact validation rules;
- exact compatibility rules;
- exact import formats;
- exact export formats;
- exact migration mappings;
- exact graph representations;
- exact serialization formats;
- exact implementation profiles.

A future specification is valid only when it preserves the standard-level behavior defined by KS-0004.

A future specification MUST NOT make relationship meaning dependent only on filenames, folder paths, tags, backlinks, graph layouts, search results, vector similarity, database rows, implementation-specific identifiers, plugin behavior, user interface state, hidden application state, workflow memory, agent memory, or undocumented implementation behavior.

Relationship vocabularies MAY evolve.

A relationship vocabulary MAY add, revise, deprecate, supersede, merge, split, clarify, or remove Relationship Types, inverse terms, participant roles, direction values, strength values, confidence values, lifecycle values, authority values, privacy values, validation values, or compatibility values.

Relationship vocabulary changes SHOULD preserve traceability.

A vocabulary change SHOULD identify:

- what value changed;
- why the value changed;
- what prior value existed;
- what new value replaces it where applicable;
- whether the change is compatible;
- whether migration is required;
- whether existing Relationships are affected;
- whether validation rules are affected;
- whether privacy boundaries are affected;
- whether authority interpretation is affected;
- whether implementation behavior is affected.

A vocabulary change MUST NOT silently reinterpret existing Relationships in a way that changes meaning, authority, privacy, validation, lifecycle state, provenance, compatibility, migration behavior, import behavior, export behavior, workflow behavior, agent behavior, publication behavior, or downstream use.

Relationship rules MAY evolve.

A Relationship rule MAY be clarified, refined, deprecated, superseded, extended, or replaced through governance.

A Relationship rule change SHOULD preserve compatibility where practical.

A Relationship rule change MUST preserve historical interpretability.

A Relationship created under an older rule SHOULD remain understandable after the rule changes.

A deprecated Relationship rule SHOULD remain historically available where it is needed to understand older Relationships, older implementations, older migrations, older imports, older exports, older validation results, older workflows, older agent output, or older governance decisions.

A superseded Relationship rule SHOULD identify the replacement rule where practical.

A rejected Relationship rule SHOULD NOT be treated as authoritative unless a future governed process reopens and revises it.

Relationship governance SHOULD preserve Relationship Participants.

A governance change MUST NOT cause Relationships to point to the wrong Knowledge Object, Knowledge Record, Source Material, standard, decision, workflow, implementation, identifier, or governed entity.

Relationship governance SHOULD preserve Object Identity.

A governance change MUST NOT replace stable Object Identity with filenames, folder paths, titles, tags, backlinks, graph positions, search results, vector results, implementation-specific identifiers, or hidden application state where Object Identity affects Relationship meaning.

Relationship governance SHOULD preserve Relationship Type.

A governance change MUST NOT silently collapse materially different Relationship Types into a generic relationship when type affects meaning.

A deprecated or superseded Relationship Type SHOULD remain historically interpretable where existing Relationships depend on it.

A new Relationship Type SHOULD define enough meaning to avoid confusion with existing Relationship Types where practical.

Relationship governance SHOULD preserve Relationship Direction.

A governance change MUST NOT silently reverse, remove, collapse, duplicate, infer, or reinterpret Relationship Direction when direction affects meaning.

A change to direction rules SHOULD identify whether inverse Relationships, participant roles, validation rules, import mappings, export mappings, migration mappings, workflow behavior, agent behavior, or implementation behavior are affected.

Relationship governance SHOULD preserve Relationship Strength and Relationship Confidence.

A governance change MUST NOT convert strength into confidence, confidence into strength, either value into authority, or either value into approval unless a future governed specification explicitly defines that behavior and preserves traceability.

A change to strength or confidence values SHOULD identify whether existing Relationships require review, migration, validation, or compatibility notes.

Relationship governance SHOULD preserve Relationship Provenance.

A governance change affecting Relationships SHOULD preserve enough provenance for future review.

Governance provenance MAY identify:

- who proposed the change;
- what document, specification, decision, ADR, RFC, workflow, agent, implementation, validator, or source supported the change;
- why the change was made;
- what review occurred;
- what approval occurred;
- what compatibility impact was considered;
- what privacy impact was considered;
- what migration guidance exists;
- what Relationships are affected;
- what implementation behavior is affected.

Relationship governance SHOULD preserve Relationship Lifecycle State.

A governance change SHOULD preserve whether affected Relationships are proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, needs review, or governed by a future lifecycle state.

A governance change MUST NOT silently convert proposed, inferred, deprecated, superseded, rejected, archived, or needs-review Relationships into approved or active Relationships.

Relationship governance SHOULD preserve Relationship Authority.

A governance change MUST NOT allow a lower-authority document, specification, workflow, agent, implementation, validation result, import process, export process, migration process, or Relationship to override a higher-authority document, standard, decision, privacy rule, validation rule, workflow rule, or governance rule.

Where authority changes, the change SHOULD preserve enough context for future humans, agents, workflows, validators, and implementations to determine the prior authority, new authority, reason for change, scope of change, and affected Relationships.

Relationship governance MUST preserve Relationship Privacy.

A governance change MUST NOT expose restricted Relationships, restricted Relationship Participants, restricted Relationship Types, restricted Relationship Direction, restricted strength, restricted confidence, restricted provenance, restricted lifecycle state, restricted authority, restricted validation results, restricted source material, private reasoning, private agent activity, private workflow activity, or sensitive relationship context.

Where a governance change affects privacy-sensitive relationship behavior, the stricter applicable privacy classification SHOULD apply unless a future governed privacy specification defines different behavior.

Relationship governance SHOULD preserve Relationship Validation.

A governance change MAY update validation rules, validation expectations, validation warnings, validation results, validator behavior, or validation specifications.

A validation rule change MUST NOT silently treat prior validation results as approval.

A validation rule change SHOULD identify whether existing Relationships need revalidation, migration, review, deprecation, supersession, archival, or compatibility warnings.

Relationship governance SHOULD preserve Relationship Compatibility.

A governance change SHOULD identify compatibility impact where the change affects existing Relationships, existing implementations, import behavior, export behavior, migration behavior, validation behavior, workflow behavior, agent behavior, publication behavior, or downstream use.

A compatibility-impacting change SHOULD identify:

- affected Relationship Types;
- affected participants;
- affected direction rules;
- affected strength or confidence values;
- affected provenance expectations;
- affected lifecycle states;
- affected authority rules;
- affected privacy rules;
- affected validation rules;
- affected import mappings;
- affected export mappings;
- affected migration mappings;
- affected implementation behavior;
- affected agent behavior;
- affected workflow behavior;
- recommended review or migration action.

Relationship governance SHOULD preserve source distinction.

A governance change MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

A governance change involving Source Material SHOULD preserve whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role where that distinction affects interpretation.

Relationship governance SHOULD preserve agent boundaries.

An agent MAY propose relationship-governance changes only within the permissions, privacy boundaries, workflow expectations, and governance rules applicable to that agent.

An agent-generated governance recommendation MUST NOT become authoritative merely because an agent produced it, repeated it, validated it, ranked it, displayed it, or used it in downstream output.

Relationship governance SHOULD preserve workflow boundaries.

A workflow MAY route, review, validate, approve, reject, deprecate, supersede, archive, import, export, migrate, or publish relationship-governance changes only within the permissions, privacy boundaries, validation expectations, and governance rules applicable to that workflow.

Workflow completion MUST NOT become governance approval unless the applicable workflow rule or future governed specification explicitly defines that completion as approval.

Relationship governance SHOULD preserve implementation boundaries.

An implementation MAY support relationship governance through tools, dashboards, forms, validation reports, graph views, search views, workflow tools, agent tools, import tools, export tools, migration tools, review tools, or approval tools.

Implementation behavior MUST NOT become governance authority merely because the implementation stores, displays, routes, validates, exports, imports, migrates, synchronizes, indexes, summarizes, or publishes a relationship-governance change.

Relationship governance SHOULD support review.

A reviewer SHOULD be able to determine whether a Relationship change:

- preserves Relationship Participants;
- preserves Object Identity where applicable;
- preserves Relationship Type;
- preserves Relationship Direction;
- preserves Relationship Strength and Relationship Confidence distinctions;
- preserves Relationship Provenance;
- preserves Relationship Lifecycle State;
- preserves Relationship Authority;
- preserves Relationship Privacy;
- preserves Relationship Validation;
- preserves Relationship Compatibility;
- preserves source distinction;
- preserves agent boundaries;
- preserves workflow boundaries;
- preserves implementation boundaries;
- requires migration guidance;
- requires import or export guidance;
- requires compatibility warnings;
- requires privacy review;
- requires authority review;
- requires human approval;
- affects future specifications or implementations.

Relationship governance SHOULD support safe evolution.

Safe evolution means Relationship behavior can improve without losing prior meaning.

Safe evolution SHOULD ensure that:

- changes are deliberate;
- changes are reviewable;
- changes are compatible where practical;
- breaking changes are documented;
- privacy impact is reviewed where applicable;
- authority impact is reviewed where applicable;
- validation impact is reviewed where applicable;
- migration guidance exists where needed;
- historical Relationships remain understandable;
- future specifications can build on prior decisions.

Governance and Evolution are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can revise, extend, deprecate, supersede, validate, migrate, and implement relationship behavior without losing meaning, breaking identity, weakening privacy, confusing authority, erasing provenance, collapsing lifecycle state, invalidating validation, breaking compatibility, or creating implementation lock-in.

## 20. Conformance

Conformance defines what it means for a Relationship, specification, validator, workflow, agent, storage system, import process, export process, migration process, or implementation to satisfy KS-0004.

Conformance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether relationship behavior preserves the requirements of The Brain Standard.

A conforming Relationship SHOULD preserve the standard-level meaning required by KS-0004.

A conforming Relationship SHOULD be explicit where the Relationship affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, workflow behavior, agent behavior, governance, publication, migration, import, export, or downstream use.

A conforming Relationship SHOULD identify or resolve to its Relationship Participants clearly enough for future review.

A conforming Relationship SHOULD preserve stable Object Identity where the Relationship connects Knowledge Objects.

A conforming Relationship MUST NOT rely only on filename, folder path, storage location, title, tag, backlink behavior, graph layout, search result, vector similarity, implementation-specific identifier, plugin behavior, user interface state, hidden application state, workflow memory, agent memory, or undocumented implementation behavior when the Relationship affects meaning.

A conforming Relationship SHOULD preserve Relationship Type where type affects meaning.

A conforming Relationship SHOULD preserve Relationship Direction where direction affects meaning.

A conforming Relationship SHOULD preserve Relationship Strength where strength affects interpretation.

A conforming Relationship SHOULD preserve Relationship Confidence where confidence affects interpretation.

Relationship Strength and Relationship Confidence MUST remain distinguishable.

A conforming Relationship SHOULD preserve Relationship Provenance where provenance affects interpretation.

A conforming Relationship SHOULD preserve Relationship Lifecycle State where lifecycle state affects interpretation or downstream use.

A conforming Relationship SHOULD preserve Relationship Authority where authority affects interpretation, governance, validation, workflow behavior, publication, migration, import, export, or downstream use.

A conforming Relationship MUST preserve Relationship Privacy.

A conforming Relationship SHOULD support Relationship Validation.

A conforming Relationship SHOULD support Relationship Compatibility.

A conforming Relationship SHOULD preserve source distinction.

A Relationship between a Knowledge Record and Source Material MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

A conforming Relationship SHOULD remain reviewable where it is inferred, agent-generated, workflow-generated, imported, exported, migrated, implementation-generated, deprecated, superseded, rejected, archived, uncertain, or needs review.

A conforming relationship specification MAY define exact relationship structures, schemas, formats, fields, values, validation rules, vocabularies, mappings, or serialization behavior.

A conforming relationship specification MUST preserve the standard-level behavior defined by KS-0004.

A conforming relationship specification MUST NOT make relationship meaning dependent only on implementation-specific behavior unless a higher-authority governed specification explicitly defines that behavior and preserves compatibility, provenance, validation, authority, privacy, and reviewability.

A conforming relationship vocabulary MAY define approved Relationship Types, inverse terms, participant roles, direction values, strength values, confidence values, lifecycle values, authority values, privacy values, validation values, or compatibility values.

A conforming relationship vocabulary MUST preserve traceability when values are added, revised, deprecated, superseded, merged, split, removed, or replaced.

A conforming relationship vocabulary MUST NOT silently reinterpret existing Relationships in a way that changes meaning, authority, privacy, validation, lifecycle state, provenance, compatibility, migration behavior, import behavior, export behavior, workflow behavior, agent behavior, publication behavior, or downstream use.

A conforming validator MAY check Relationship structure, participants, type, direction, strength, confidence, provenance, lifecycle state, authority, privacy, compatibility, implementation boundaries, import behavior, export behavior, migration behavior, agent behavior, workflow behavior, or governance behavior.

A conforming validator MUST NOT treat validation as approval unless a governed workflow or future specification explicitly defines that validation result as approval.

A conforming validator MUST preserve privacy boundaries.

A conforming validator MUST NOT expose restricted Relationships, restricted Relationship Participants, restricted Relationship Types, restricted Relationship Direction, restricted strength, restricted confidence, restricted provenance, restricted lifecycle state, restricted authority, restricted validation results, restricted source material, private reasoning, private agent activity, private workflow activity, or sensitive relationship context.

A conforming validator SHOULD preserve enough provenance to explain validation results where those results affect interpretation, lifecycle state, authority, privacy, compatibility, governance, publication, migration, import, export, workflow behavior, agent behavior, or downstream use.

A conforming agent MAY propose, infer, classify, enrich, validate, summarize, review, or recommend Relationships only within the permissions, privacy boundaries, workflow expectations, and governance rules applicable to that agent.

A conforming agent MUST NOT silently approve, reject, expose, publish, export, migrate, delete, or modify a Relationship unless the relevant agent standard, workflow rule, privacy rule, validation rule, and governance rule allow that behavior.

A conforming agent MUST preserve agent-generated provenance where agent activity affects interpretation, lifecycle state, authority, privacy, validation, compatibility, governance, publication, migration, import, export, workflow behavior, or downstream use.

A conforming workflow MAY propose, classify, enrich, validate, route, review, approve, reject, deprecate, supersede, archive, import, export, migrate, publish, or synchronize Relationships only within the permissions, privacy boundaries, validation expectations, and governance rules applicable to that workflow.

A conforming workflow MUST NOT treat workflow completion as approval unless the applicable workflow rule or future governed specification explicitly defines that completion as approval.

A conforming workflow MUST preserve workflow-generated provenance where workflow activity affects interpretation, lifecycle state, authority, privacy, validation, compatibility, governance, publication, migration, import, export, agent behavior, or downstream use.

A conforming implementation MAY store, display, index, search, link, visualize, validate, import, export, migrate, synchronize, back up, restore, or process Relationships.

A conforming implementation MUST NOT redefine governed Relationship meaning through storage behavior, display behavior, graph behavior, backlink behavior, search behavior, vector behavior, plugin behavior, database behavior, cache behavior, API behavior, user interface behavior, or hidden application state.

A conforming implementation MUST preserve implementation-specific behavior as distinguishable from governed Relationship behavior where that distinction affects interpretation.

A conforming implementation MUST NOT create implementation lock-in by making governed Relationship meaning dependent on private state, proprietary indexes, undocumented behavior, hidden identifiers, plugin-only structures, non-exportable fields, or inaccessible application data.

A conforming storage system MAY preserve Relationships through files, metadata, records, indexes, databases, graphs, links, sidecars, manifests, or other storage representations.

A conforming storage system MUST preserve governed Relationship meaning where the Relationship affects interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, workflow behavior, agent behavior, governance, publication, migration, import, export, or downstream use.

A conforming storage system MUST NOT allow storage layout, filenames, file paths, database rows, graph edges, tags, backlinks, search indexes, vector indexes, or implementation-specific references to define Relationship meaning by themselves where meaning is governed by KS-0004.

A conforming import process SHOULD preserve Relationship Participants, Object Identity, Relationship Type, Relationship Direction, Relationship Strength, Relationship Confidence, Relationship Provenance, Relationship Lifecycle State, Relationship Authority, Relationship Privacy, Relationship Validation, Relationship Compatibility, source distinction, and implementation boundaries.

A conforming export process SHOULD preserve Relationship Participants, Object Identity, Relationship Type, Relationship Direction, Relationship Strength, Relationship Confidence, Relationship Provenance, Relationship Lifecycle State, Relationship Authority, Relationship Privacy, Relationship Validation, Relationship Compatibility, source distinction, and implementation boundaries.

A conforming migration process SHOULD preserve Relationship Participants, Object Identity, Relationship Type, Relationship Direction, Relationship Strength, Relationship Confidence, Relationship Provenance, Relationship Lifecycle State, Relationship Authority, Relationship Privacy, Relationship Validation, Relationship Compatibility, source distinction, and implementation boundaries.

A conforming import, export, or migration process MUST NOT silently change governed Relationship meaning.

Where full preservation is not possible, a conforming import, export, or migration process SHOULD preserve the strongest available traceable information, record unresolved information, preserve relevant mappings, and mark affected Relationships for review.

A conforming process MUST NOT silently pretend that a Relationship is fully valid, approved, authoritative, private, portable, or compatible when required relationship information is missing, conflicting, ambiguous, unsafe, or unresolved.

A conforming governance change MUST preserve the constitutional foundation and authority hierarchy of The Brain Standard.

A conforming governance change SHOULD preserve historical interpretability, compatibility where practical, privacy boundaries, authority boundaries, validation traceability, migration guidance, and affected relationship context.

A conforming governance change MUST NOT allow lower-authority documents, specifications, workflows, agents, implementations, validation results, import processes, export processes, migration processes, or Relationships to override higher-authority documents, standards, decisions, privacy rules, validation rules, workflow rules, or governance rules.

A conforming Relationship or process SHOULD be able to demonstrate conformance through reviewable evidence.

Conformance evidence MAY include:

- explicit Relationship Participants;
- stable Object Identity references where applicable;
- Relationship Type;
- Relationship Direction;
- Relationship Strength;
- Relationship Confidence;
- Relationship Provenance;
- Relationship Lifecycle State;
- Relationship Authority;
- Relationship Privacy;
- Relationship Validation results;
- Relationship Compatibility notes;
- source distinction;
- import mappings;
- export mappings;
- migration mappings;
- implementation-boundary notes;
- agent provenance;
- workflow provenance;
- governance provenance;
- review history;
- approval history where applicable;
- rejection history where applicable;
- deprecation history where applicable;
- supersession history where applicable.

Conformance MAY be partial.

A Relationship, specification, validator, workflow, agent, storage system, import process, export process, migration process, or implementation MAY conform to some KS-0004 expectations while failing others.

Partial conformance SHOULD be explicit where the missing or failed expectation affects meaning, authority, privacy, validation, compatibility, governance, publication, migration, import, export, workflow behavior, agent behavior, or downstream use.

A partial-conformance claim MUST NOT imply full conformance.

A nonconforming Relationship or process SHOULD be marked for review where nonconformance affects interpretation, lifecycle state, authority, privacy, validation, compatibility, governance, publication, migration, import, export, workflow behavior, agent behavior, or downstream use.

Conformance to KS-0004 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether a Relationship or relationship-handling process preserves governed relationship meaning, respects authority and privacy boundaries, remains validatable and compatible, avoids implementation lock-in, and remains interpretable across time and implementation replacement.

## 21. Success Criteria

Success Criteria define how humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations determine whether KS-0004 fulfills its purpose.

KS-0004 succeeds when Relationships remain explicit, interpretable, portable, traceable, reviewable, privacy-respecting, validatable, compatible, implementation-independent, and governed across time.

KS-0004 succeeds when a future human can understand a Relationship without relying on hidden application state, undocumented implementation behavior, private memory, folder proximity, filename similarity, backlink behavior, graph layout, tag coincidence, search ranking, vector similarity, workflow memory, agent memory, or informal convention.

KS-0004 succeeds when a future agent can read, propose, classify, validate, summarize, review, or preserve Relationships only within applicable privacy boundaries, workflow expectations, governance rules, validation expectations, and authority limits.

KS-0004 succeeds when a future workflow can create, route, review, approve, reject, deprecate, supersede, archive, import, export, migrate, publish, or synchronize Relationships without treating workflow completion as approval unless a governed workflow rule explicitly defines that behavior.

KS-0004 succeeds when a future validator can determine whether a Relationship satisfies applicable requirements for participants, Object Identity, type, direction, strength, confidence, provenance, lifecycle state, authority, privacy, validation, compatibility, import, export, migration, implementation boundaries, agent behavior, workflow behavior, and governance.

KS-0004 succeeds when a future implementation can store, display, index, search, link, visualize, validate, import, export, migrate, synchronize, back up, restore, or process Relationships without redefining governed Relationship meaning.

KS-0004 succeeds when a Relationship identifies or resolves to its Relationship Participants clearly enough for future review.

KS-0004 succeeds when Relationships that connect Knowledge Objects refer to or resolve to stable Object Identity where practical.

KS-0004 succeeds when Relationship Participants remain distinguishable from filenames, folder paths, titles, aliases, tags, backlinks, graph positions, search results, vector similarities, implementation-specific identifiers, user interface state, plugin state, workflow state, agent memory, or hidden application state.

KS-0004 succeeds when Relationship Participant roles are clear where role affects interpretation.

KS-0004 succeeds when Source Material and Knowledge Records remain distinguishable where either participates in a Relationship.

KS-0004 succeeds when Relationship Type remains explicit where type affects meaning, interpretation, provenance, lifecycle state, authority, privacy, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, publication, or downstream use.

KS-0004 succeeds when materially different Relationship Types are not silently collapsed into generic connections.

KS-0004 succeeds when Relationship Direction remains explicit where direction affects meaning.

KS-0004 succeeds when direction is not silently lost, reversed, collapsed, inferred, duplicated, or reinterpreted during storage, display, indexing, validation, backup, restoration, synchronization, import, export, migration, workflow activity, agent activity, or implementation replacement.

KS-0004 succeeds when Relationship Strength and Relationship Confidence remain distinguishable.

KS-0004 succeeds when strength is not treated as confidence.

KS-0004 succeeds when confidence is not treated as strength.

KS-0004 succeeds when strength or confidence is not treated as approval, authority, validation, publication permission, privacy permission, or downstream-use permission unless a future governed specification explicitly defines that behavior.

KS-0004 succeeds when Relationship Provenance is preserved where provenance affects interpretation.

KS-0004 succeeds when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine where a Relationship came from, what evidence or reasoning supports it, who or what created or modified it, whether it was inferred, whether it was reviewed, whether it was approved, whether it was imported or migrated, and whether privacy or authority is affected.

KS-0004 succeeds when Relationship Lifecycle State remains clear where lifecycle state affects interpretation or downstream use.

KS-0004 succeeds when proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, and needs-review Relationships remain distinguishable where those distinctions affect meaning.

KS-0004 succeeds when rejected, deprecated, superseded, archived, or needs-review Relationships do not silently become active, approved, authoritative, or safe for downstream use because of import, export, migration, synchronization, restoration, indexing, validation, workflow activity, agent activity, or implementation behavior.

KS-0004 succeeds when Relationship Authority remains distinguishable from document authority, lifecycle state, confidence, validation, implementation behavior, agent output, workflow output, and storage behavior.

KS-0004 succeeds when lower-authority Relationships, agents, workflows, implementations, validation results, imports, exports, migrations, sources, or participants do not override higher-authority documents, standards, decisions, specifications, privacy rules, validation rules, workflow rules, or governance rules.

KS-0004 succeeds when Relationship Privacy is preserved.

KS-0004 succeeds when restricted Relationships, restricted Relationship Participants, restricted Relationship Types, restricted Relationship Direction, restricted strength, restricted confidence, restricted provenance, restricted lifecycle state, restricted authority, restricted validation results, restricted source material, private reasoning, private agent activity, private workflow activity, or sensitive relationship context are not exposed to users, agents, workflows, exports, indexes, graph views, summaries, logs, caches, dashboards, APIs, plugins, implementations, or publications that are not permitted to access them.

KS-0004 succeeds when Relationships crossing privacy boundaries are handled according to the stricter applicable privacy expectation unless a future governed privacy specification defines different behavior.

KS-0004 succeeds when Relationship Validation supports review without redefining relationship meaning.

KS-0004 succeeds when validation results are not treated as approval unless a governed workflow or future specification explicitly defines that validation result as approval.

KS-0004 succeeds when validation can detect missing participants, unclear participant roles, unclear type, unclear direction, insufficient provenance, lifecycle ambiguity, authority confusion, privacy exposure, compatibility failure, implementation lock-in, import ambiguity, export ambiguity, migration loss, agent-boundary failure, workflow-boundary failure, or governance drift.

KS-0004 succeeds when Relationship Compatibility preserves governed relationship meaning across storage systems, workflows, agents, validators, import processes, export processes, migration processes, backups, restorations, synchronizations, indexes, and implementation replacement.

KS-0004 succeeds when compatibility is not treated as simple file conversion.

KS-0004 succeeds when import, export, and migration processes preserve Relationship Participants, Object Identity, Relationship Type, Relationship Direction, Relationship Strength, Relationship Confidence, Relationship Provenance, Relationship Lifecycle State, Relationship Authority, Relationship Privacy, Relationship Validation, Relationship Compatibility, source distinction, mappings, unresolved information, review requirements, and implementation boundaries where those elements affect meaning.

KS-0004 succeeds when import, export, and migration processes do not silently pretend that a Relationship is fully valid, approved, authoritative, private, portable, or compatible when required relationship information is missing, conflicting, ambiguous, unsafe, or unresolved.

KS-0004 succeeds when Inferred Relationships remain distinguishable from approved Relationships.

KS-0004 succeeds when inference basis, inference provenance, inferred type, inferred direction, inferred strength, inferred confidence, lifecycle state, authority limits, privacy boundaries, validation expectations, and review requirements remain clear where they affect interpretation.

KS-0004 succeeds when Agent-Generated Relationships remain distinguishable from human approval, workflow approval, validation approval, document authority, and governed relationship meaning.

KS-0004 succeeds when agent-generated provenance remains sufficient to determine what agent activity produced or modified the Relationship, what evidence or signal supported it, whether review is required, and whether privacy or authority is affected.

KS-0004 succeeds when Workflow-Generated Relationships remain distinguishable from human approval, agent generation, validation approval, document authority, and governed relationship meaning.

KS-0004 succeeds when workflow-generated provenance remains sufficient to determine what workflow activity produced or modified the Relationship, what steps affected it, whether review occurred, whether approval occurred, and whether privacy or authority is affected.

KS-0004 succeeds when implementation-specific links, backlinks, graph edges, database relations, file references, metadata fields, indexes, search associations, vector records, embeddings, tags, aliases, folders, dashboards, user interface elements, plugin state, caches, APIs, synchronization records, import records, export records, and migration records remain distinguishable from governed Relationship meaning.

KS-0004 succeeds when implementation convenience features support relationship use without silently creating, approving, rejecting, deprecating, superseding, exposing, hiding, collapsing, reversing, duplicating, or reinterpreting governed Relationships.

KS-0004 succeeds when future relationship specifications, relationship vocabularies, validation specifications, storage standards, agent standards, workflow standards, implementation documents, graph specifications, import formats, export formats, migration mappings, and operational guides can refine relationship behavior without contradicting KS-0004.

KS-0004 succeeds when relationship governance preserves historical interpretability, compatibility where practical, privacy boundaries, authority boundaries, validation traceability, migration guidance, source distinction, agent boundaries, workflow boundaries, implementation boundaries, and affected relationship context.

KS-0004 succeeds when conformance can be reviewed.

A conforming Relationship or relationship-handling process SHOULD be able to demonstrate conformance through reviewable evidence where conformance affects meaning, authority, privacy, validation, compatibility, governance, publication, migration, import, export, workflow behavior, agent behavior, or downstream use.

KS-0004 succeeds when partial conformance is explicit.

A partial-conformance claim MUST NOT imply full conformance.

KS-0004 succeeds when nonconforming Relationships or relationship-handling processes are marked for review where nonconformance affects interpretation, lifecycle state, authority, privacy, validation, compatibility, governance, publication, migration, import, export, workflow behavior, agent behavior, or downstream use.

KS-0004 succeeds when relationship anti-patterns can be detected before they become embedded in systems, workflows, agents, specifications, validators, storage systems, import processes, export processes, migration processes, or implementations.

Relationship anti-patterns MAY include:

- treating backlinks as governed Relationships without explicit meaning;
- treating graph edges as governed Relationships without explicit meaning;
- treating vector similarity as approval;
- treating workflow completion as approval;
- treating agent output as authority;
- treating validation as approval without a governed rule;
- treating storage links as relationship meaning;
- treating filenames or folder paths as participant identity;
- treating tags as governance;
- treating confidence as authority;
- treating strength as approval;
- treating migration success as compatibility success without relationship review;
- treating export success as privacy safety;
- treating implementation display as relationship truth;
- treating hidden application state as governed meaning;
- treating partial conformance as full conformance.

KS-0004 succeeds when future humans and AI systems can understand, trust, maintain, validate, migrate, implement, and evolve Relationships without losing meaning, breaking identity, weakening privacy, confusing authority, erasing provenance, collapsing lifecycle state, invalidating validation, breaking compatibility, or creating implementation lock-in.

KS-0004 succeeds when it provides a stable relationship foundation that future Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, specifications, validators, implementation documents, operational guides, and tools can depend on without replacing or weakening The Brain Standard.
