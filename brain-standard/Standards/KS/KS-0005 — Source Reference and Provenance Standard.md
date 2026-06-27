# KS-0005 — Source Reference and Provenance Standard

Document ID: KS-0005
Title: Source Reference and Provenance Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-26
Last Updated: 2026-06-26
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.5 — Source Reference and Provenance Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and source-reference and provenance rules are interpreted within KS-0005.

Where conflicts arise between Source Material, Source References, provenance, evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, source validation, source compatibility, Object Identity, metadata, relationships, lifecycle state, authority, privacy classification, storage behavior, agents, workflows, implementations, import behavior, export behavior, migration behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0005 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0005 extends KS-0001 by defining standard-level source-reference and provenance behavior for Knowledge Objects, Knowledge Records, Source Material, relationships, standards, decisions, workflows, agents, implementations, and other governed entities.

KS-0005 depends on KS-0002 because source references and provenance may rely on stable Object Identity, source identifiers, alternate identifiers, legacy identifiers, migration identifiers, import identifiers, export identifiers, and identity-change records.

KS-0005 depends on KS-0003 because source-reference and provenance meaning may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through metadata.

KS-0005 depends on KS-0004 because relationships may connect Knowledge Objects, Knowledge Records, Source Material, evidence, provenance records, validation records, workflows, agents, implementations, and other governed entities.

If KS-0005 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

If KS-0005 appears to conflict with KS-0001, the conflict SHOULD be resolved by preserving the Knowledge Object Model defined in KS-0001 while applying KS-0005 as the more specific standard for Source Reference and Provenance behavior.

If KS-0005 appears to conflict with KS-0002, the conflict SHOULD be resolved by preserving stable Object Identity while applying KS-0005 as the more specific standard for source-reference and provenance interpretation, review, validation, and compatibility.

If KS-0005 appears to conflict with KS-0003, the conflict SHOULD be resolved by preserving metadata role boundaries while applying KS-0005 as the more specific standard for source-reference and provenance behavior.

If KS-0005 appears to conflict with KS-0004, the conflict SHOULD be resolved by preserving relationship behavior while applying KS-0005 as the more specific standard for source support, evidence, attribution, provenance, and source-reference interpretation.

KS-0005 defines Source References and Provenance at the conceptual standard level.

KS-0005 does not define exact citation syntax, exact Markdown front matter syntax, exact metadata field names, exact source-reference schemas, exact database structures, exact API behavior, exact storage paths, exact source archive structure, exact validation tooling, exact citation style, exact bibliography format, exact import format, exact export format, exact migration format, or implementation-specific source-link behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation profiles, validation specifications, source-reference vocabularies, citation specifications, archival specifications, and operational documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, Object Identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Source Reference refers to a traceable reference from a Knowledge Object, Knowledge Record, relationship, decision, workflow, validation result, or other governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a Knowledge Object, Knowledge Record, Source Reference, relationship, decision, or other governed entity.
- Evidence refers to Source Material, extracted content, cited material, observation, validation result, relationship, reasoning record, or other support used to justify, explain, verify, challenge, or contextualize a Knowledge Object, Knowledge Record, claim, relationship, decision, classification, or interpretation.
- Attribution refers to information identifying the person, organization, system, source, author, creator, publisher, agent, workflow, or implementation associated with the creation, publication, modification, extraction, transformation, interpretation, or transmission of Source Material or governed knowledge.
- Source Identifier refers to an identifier associated with Source Material rather than with the Knowledge Object itself.
- Source Availability refers to whether Source Material is available, unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, or otherwise limited for review, validation, migration, import, export, preservation, or downstream use.
- Source Reliability refers to the assessed trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength of Source Material.
- Source Authority refers to the governance weight, interpretive relevance, official status, review status, or approved use assigned to Source Material within a particular context.
- Source Privacy refers to the privacy classification, visibility boundary, access expectation, redaction requirement, disclosure limitation, or handling rule associated with Source Material, Source References, evidence, attribution, provenance, or extracted content.
- Source Validation refers to the process of checking whether Source Material, Source References, evidence, attribution, provenance, extraction history, transformation history, availability status, reliability notes, privacy expectations, and compatibility expectations satisfy the applicable standards or specifications.
- Source Compatibility refers to whether Source Material, Source References, evidence, attribution, and provenance remain meaningful, portable, reviewable, privacy-respecting, and interpretable across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.
- Extraction refers to the process of selecting, copying, transcribing, parsing, summarizing, segmenting, or otherwise taking information from Source Material for use in a Knowledge Record, relationship, validation result, workflow output, agent output, or other governed entity.
- Transformation refers to the process of changing Source Material, extracted content, or prior knowledge into another representation, summary, translation, classification, interpretation, structured record, derived object, migrated form, or implementation-specific representation.
- Source-Derived Knowledge refers to Knowledge Objects, Knowledge Records, relationships, classifications, summaries, interpretations, or decisions created from, about, or in response to Source Material.
- Human-Created Provenance refers to provenance created, recorded, reviewed, corrected, approved, rejected, or maintained by a human.
- Agent-Generated Provenance refers to provenance created, proposed, modified, enriched, validated, extracted, classified, summarized, or inferred by an agent.
- Workflow-Generated Provenance refers to provenance created, proposed, modified, enriched, validated, extracted, classified, summarized, routed, approved, rejected, or preserved through a governed workflow.
- Import Provenance refers to provenance associated with bringing Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, or external content into a compliant environment.
- Export Provenance refers to provenance associated with producing Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, or external content from a compliant environment for use elsewhere.
- Migration Provenance refers to provenance associated with moving, converting, mapping, preserving, transforming, validating, or reviewing Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, or identifiers across systems, formats, repositories, vaults, implementations, standards versions, or storage environments.
- Citation refers to a human-readable, publication-oriented, academic, legal, technical, or external reference form that may identify Source Material. A citation may support a Source Reference, but citation syntax does not define Source Reference behavior by itself.
- External Reference refers to a reference to material, identifiers, systems, records, publications, URLs, datasets, databases, repositories, or artifacts outside the immediate compliant environment.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, source-reference, or operational context associated with a Knowledge Object, Knowledge Record, Source Material, relationship, or governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, or governed entity.
- Authority Level refers to the governance weight, review status, or interpretive authority assigned to a document, Knowledge Object, Knowledge Record, relationship, source, decision, or governed entity.
- Privacy Classification refers to explicit metadata describing permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.
- Validation refers to the process of checking whether a Knowledge Object, Knowledge Record, Source Material, Source Reference, provenance record, relationship, or governed entity satisfies the applicable standards, specifications, metadata expectations, provenance expectations, lifecycle expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0005 is to define how Source References and provenance work across The Brain Standard.

KS-0001 establishes that Knowledge Objects and Knowledge Records SHALL support Source References and provenance where Source Material, evidence, origin, reasoning, transformation, agent activity, workflow activity, import, export, migration, review, validation, or change history affects meaning, interpretation, authority, privacy, lifecycle state, relationships, compatibility, or downstream use.

KS-0005 defines the standard-level behavior required to create, interpret, preserve, validate, review, migrate, import, export, govern, and maintain Source References and provenance.

Source References exist so that knowledge can remain connected to the Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to it.

Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand where knowledge came from, how it was created or changed, what source material was used, what transformation occurred, who or what participated, and what review state applies.

KS-0005 exists to prevent source and provenance confusion.

Source and provenance confusion occurs when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, or implementations cannot reliably determine:

- what Source Material supports a Knowledge Object, Knowledge Record, relationship, decision, claim, standard, workflow, implementation, or governed entity;
- whether source support exists, is missing, is unavailable, is restricted, is uncertain, is superseded, or cannot be verified;
- whether a record contains original Source Material, extracted content, summarized content, interpreted content, transformed content, synthesized knowledge, human-authored knowledge, agent-generated knowledge, workflow-generated knowledge, imported knowledge, migrated knowledge, or reviewed knowledge;
- who or what created, modified, extracted, transformed, summarized, interpreted, validated, reviewed, approved, rejected, imported, exported, or migrated the knowledge;
- whether source support, attribution, or provenance affects meaning, authority, privacy, validation, lifecycle state, compatibility, migration, import, export, or governance;
- whether a Source Reference remains meaningful when files are renamed, moved, copied, archived, deleted, restricted, migrated, imported, exported, backed up, restored, synchronized, reindexed, transformed, validated, processed by an agent, processed by a workflow, or accessed through a different implementation.

KS-0005 defines source-reference and provenance behavior for:

- Source Material;
- Source References;
- provenance;
- evidence and support;
- attribution;
- Source Material and Knowledge Record boundaries;
- extraction provenance;
- transformation provenance;
- human-created provenance;
- agent-generated provenance;
- workflow-generated provenance;
- import, export, and migration provenance;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source validation;
- source compatibility;
- implementation boundaries;
- governance and evolution;
- conformance;
- success criteria.

KS-0005 does not define exact citation syntax, exact metadata field names, exact Markdown front matter syntax, exact database schemas, exact folder paths, exact source archive structure, exact API behavior, exact validation tooling, exact serialization formats, exact allowed values, exact external citation styles, or implementation-specific source-link behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, source-reference vocabularies, citation specifications, archival specifications, and operational guides.

KS-0005 defines Source References and provenance at the standard level.

A future specification MAY define exact source-reference formats, source identifiers, provenance fields, attribution fields, source availability values, source reliability values, citation syntax, archival structures, extraction records, transformation records, validation rules, import formats, export formats, or migration mappings.

Such specifications are valid only when they preserve the source-reference and provenance behavior defined by KS-0005.

The primary purpose of KS-0005 is to ensure that Source References and provenance remain explicit, interpretable, portable, traceable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent across time, tools, storage systems, workflows, agents, validators, and implementations.

KS-0005 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine:

- what Source Material supports a governed entity;
- what provenance applies to a governed entity;
- whether the source is available, unavailable, restricted, superseded, uncertain, or unverifiable;
- whether knowledge was human-created, agent-generated, workflow-generated, imported, exported, migrated, extracted, transformed, validated, reviewed, approved, rejected, or superseded;
- what evidence, attribution, extraction history, transformation history, review history, validation history, migration history, import history, or export history affects interpretation;
- whether Source Material and Knowledge Records remain distinguishable;
- whether Source References and provenance preserve privacy boundaries;
- whether Source References and provenance remain valid when storage systems, workflows, agents, validators, or implementations change;
- whether source-reference and provenance behavior can be preserved without relying on hidden application state, folder placement, filename convention, database internals, user memory, agent memory, workflow memory, citation style, or implementation-specific behavior.

## 2. Relationship to Prior Standards

KS-0005 is subordinate to and derived from the constitutional foundation of The Brain Standard.

KS-0005 depends on:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- KS-0001 — Knowledge Object Model;
- KS-0002 — Object Identity Standard;
- KS-0003 — Metadata Standard;
- KS-0004 — Relationship Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

KS-0005 applies that purpose by defining Source Reference and provenance behavior that remains portable, interpretable, reviewable, privacy-respecting, and independent of any single storage system, citation format, archive structure, database, workflow engine, agent framework, software tool, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

KS-0005 applies those principles by requiring Source References and provenance to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- distinction between Source Material and Knowledge Records;
- source traceability;
- evidence context;
- attribution;
- privacy boundaries;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability.

TB-0002 establishes the layered architecture of The Brain Standard.

KS-0005 belongs to Layer 1 — Universal Knowledge Standard.

Because Source References and provenance are part of knowledge meaning, KS-0005 defines source-reference and provenance behavior independently of storage systems, user interfaces, citation managers, folders, filenames, databases, backlink systems, graph tools, workflow engines, agent systems, validation tools, and implementations.

Layer 2 storage standards depend on KS-0005 because storage must preserve Source References, Source Material traceability, provenance, and source availability context without defining their meaning.

Layer 3 agent standards depend on KS-0005 because agents may read, extract, summarize, classify, validate, propose, transform, or enrich source-reference and provenance information without becoming unreviewable authorities.

Layer 4 workflow standards depend on KS-0005 because workflows may create, review, validate, approve, reject, import, export, migrate, supersede, or preserve Source References and provenance.

Layer 5 implementation documents depend on KS-0005 because implementations must create, read, preserve, display, migrate, export, import, validate, and synchronize Source References and provenance without redefining their standard-level meaning through implementation-specific behavior.

TB-0003 establishes the governance model for The Brain Standard.

KS-0005 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, KS-0005 has high authority within its scope but remains subordinate to constitutional documents.

KS-0001 defines the foundational Knowledge Object Model.

KS-0005 does not replace the Knowledge Object Model.

KS-0005 refines part of that model: Source References and provenance associated with Knowledge Objects, Knowledge Records, Source Material, relationships, decisions, workflows, agents, implementations, validation records, migration records, import records, export records, and other governed entities.

In practical terms:

- KS-0001 answers: What is a Knowledge Object?
- KS-0001 answers: What is a Knowledge Record?
- KS-0001 answers: Why must Source Material remain distinguishable from structured knowledge?
- KS-0001 answers: Why must Knowledge Objects and Knowledge Records support Source References and provenance?
- KS-0005 answers: How must Source References behave?
- KS-0005 answers: How must provenance behave?
- KS-0005 answers: How should evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, source validation, and source compatibility be handled?
- KS-0005 answers: How should human-created, agent-generated, workflow-generated, imported, exported, and migrated provenance be treated?

KS-0002 defines Object Identity.

KS-0005 depends on KS-0002 because Source References and provenance may need to identify, distinguish, preserve, compare, migrate, import, export, validate, or relate Knowledge Objects, Knowledge Records, Source Material, identifiers, and governed entities.

A Source Reference SHOULD reference or resolve to stable Object Identity where the referenced entity is a Knowledge Object.

A Source Reference SHOULD use an appropriate Source Identifier, external reference, citation, record identifier, document identifier, archive reference, or governed reference when the referenced entity is Source Material or another non-object entity.

A Source Reference MUST NOT confuse Source Identifiers with stable Object Identity unless a future governed specification explicitly defines a compliant identity relationship.

A Source Reference MUST NOT depend only on filename, folder path, storage location, display title, URL, backlink behavior, citation style, database row, search result, graph layout, user interface state, or implementation-specific identifier when that source reference affects meaning, provenance, lifecycle state, authority, privacy classification, validation, import, export, migration, or compatibility.

KS-0003 defines metadata behavior.

KS-0005 depends on KS-0003 because Source References and provenance may be expressed, described, classified, validated, reviewed, migrated, imported, exported, or governed through metadata.

Source-reference and provenance metadata MAY describe:

- source identity;
- source location;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source support;
- evidence context;
- attribution;
- extraction history;
- transformation history;
- creation context;
- revision context;
- agent involvement;
- workflow involvement;
- human review;
- validation state;
- import context;
- export context;
- migration context;
- compatibility expectations.

Source-reference and provenance metadata MUST remain distinguishable from Object Identity, relationship meaning, lifecycle state, authority level, privacy classification, validation status, storage behavior, workflow state, agent state, implementation metadata, and hidden application behavior.

KS-0004 defines relationship behavior.

KS-0005 depends on KS-0004 because Source References and provenance may be represented, supported, explained, or validated through relationships between governed entities.

A Source Reference MAY be associated with relationships that express source support, evidence, contradiction, attribution, derivation, citation, validation, import, export, migration, review, or governance relevance.

A relationship between Source Material and a Knowledge Record MUST preserve the distinction between original source material and structured knowledge.

A relationship involving Source Material SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, or another governed role.

KS-0005 preserves the following KS-0001 rules:

- Source Material and Knowledge Records SHALL remain distinguishable.
- Knowledge Records SHOULD preserve Source References when Source Material materially supports the content, interpretation, classification, relationship, decision, or validation of the record.
- Knowledge Records SHOULD preserve enough provenance to show what source material was used, what transformation occurred, who or what performed the transformation, whether human review occurred, and whether the source remains available where that context affects interpretation.
- Knowledge Objects and Knowledge Records MUST remain implementation-independent, portable, reviewable, and interpretable by humans and AI systems.

KS-0005 preserves the following KS-0002 rules:

- Object Identity remains independent of filenames, folder paths, storage locations, URLs, application-specific identifiers, and implementation-specific behavior.
- Source Identifiers are distinguishable from stable Object Identity unless governed otherwise.
- Identity decisions SHOULD preserve provenance when identity assignment, preservation, change, merge, split, redirect, import, export, migration, or supersession affects interpretation or compatibility.

KS-0005 preserves the following KS-0003 rules:

- Metadata may describe provenance, source references, source traceability, review state, validation state, compatibility, import, export, migration, workflow activity, and agent activity.
- Metadata MUST remain explicit, portable, inspectable, and distinguishable from hidden implementation state.
- Provenance metadata SHOULD be sufficient for future humans, agents, workflows, validators, storage systems, and implementations to understand where knowledge came from and how it has changed.
- Source-reference metadata SHOULD identify or describe source material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the knowledge.

KS-0005 preserves the following KS-0004 rules:

- Relationships SHOULD remain explicit when they affect interpretation, provenance, lifecycle state, authority, privacy, validation, compatibility, migration, import, export, workflow behavior, agent behavior, or governance.
- Relationships involving Source Material SHOULD preserve evidence, origin, attribution, support, contradiction, context, or reference meaning where applicable.
- Relationship provenance SHOULD remain reviewable where the origin, evidence, creator, agent, workflow, validation, import, migration, or reasoning behind the relationship affects interpretation.
- Relationships MUST preserve privacy boundaries.

KS-0005 is successful when it extends the prior standards into a clear source-reference and provenance model without weakening Object Identity, metadata role boundaries, relationship behavior, source distinction, lifecycle meaning, authority expectations, privacy boundaries, validation expectations, implementation independence, or practical daily usability.

## 3. Source Material Definition

Source Material is original or reference material used as evidence, input, origin, context, attribution, contradiction, or support for a Knowledge Object, Knowledge Record, relationship, decision, workflow, validation result, or other governed entity within The Brain Standard.

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
- physical artifacts;
- external references;
- database records;
- publications;
- research material;
- exported files;
- imported files;
- archived material;
- other original or reference artifacts.

Source Material provides evidence, input, context, origin, attribution, contradiction, or reference.

Source Material is not automatically a Knowledge Object.

Source Material is not automatically a Knowledge Record.

A Source Material artifact MAY become associated with a Knowledge Object or Knowledge Record when it is referenced, described, extracted from, transformed, summarized, interpreted, classified, validated, reviewed, related, imported, exported, migrated, archived, or governed.

A Source Material artifact MAY itself be represented by a Knowledge Record when the system creates structured knowledge about the source.

When a Knowledge Record is created about Source Material, the Knowledge Record MUST remain distinguishable from the Source Material itself.

A document, file, image, recording, dataset, message, transcript, web page, or other artifact stored inside a compliant repository is not automatically a Knowledge Record merely because it is stored near Knowledge Records.

A Knowledge Record stored outside a compliant repository is not automatically invalid merely because it is stored away from Source Material.

The distinction between Source Material and Knowledge Records depends on role, structure, metadata, provenance, source-reference behavior, lifecycle state, authority, privacy classification, validation expectations, and governed meaning.

Source Material MAY be:

- stored inside a compliant repository;
- stored in a separate source archive;
- stored externally;
- referenced through a durable identifier;
- referenced through a citation;
- referenced through an external reference;
- imported into a compliant environment;
- exported from a compliant environment;
- migrated between compliant environments;
- preserved as an archived artifact;
- unavailable but historically referenced;
- restricted by privacy, access, legal, ethical, contractual, or operational constraints.

Storage location does not define whether something is Source Material.

Filename does not define whether something is Source Material.

File format does not define whether something is Source Material.

Application type does not define whether something is Source Material.

Folder placement does not define whether something is Source Material.

A compliant implementation MAY store Source Material and Knowledge Records together.

A compliant implementation MAY store Source Material and Knowledge Records separately.

Both approaches may be compliant if Source Material remains distinguishable, traceable, reviewable, privacy-respecting, and portable.

Source Material SHOULD be referenced when it materially supports:

- content;
- interpretation;
- classification;
- extraction;
- transformation;
- summary;
- relationship creation;
- evidence claims;
- attribution;
- decisions;
- validation;
- authority;
- lifecycle state;
- privacy handling;
- import behavior;
- export behavior;
- migration behavior;
- compatibility;
- downstream use.

Source Material SHOULD NOT be copied unnecessarily when a durable Source Reference is sufficient.

Duplication MAY be acceptable for preservation, quotation, extraction, backup, review, accessibility, legal compliance, offline use, migration, export, import, or implementation convenience.

Duplication MUST NOT erase the distinction between original Source Material and structured knowledge derived from, about, or in response to that source.

Source Material MAY have identifiers.

A Source Identifier identifies or supports identification of Source Material.

A Source Identifier MUST remain distinguishable from stable Object Identity unless a future governed specification explicitly defines a compliant identity relationship.

Source Material MAY have metadata.

Source Material metadata MAY describe:

- source identity;
- source title or label;
- source type;
- source location;
- source creator;
- source publisher;
- source date;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source access conditions;
- source format;
- source preservation status;
- source extraction context;
- source transformation context;
- source validation state;
- source compatibility expectations;
- import context;
- export context;
- migration context.

Source Material metadata MUST NOT redefine Source Material as a Knowledge Record unless a governed process creates or identifies a Knowledge Record.

Source Material MAY participate in relationships.

A relationship involving Source Material SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, derivation, validation, or another governed role.

A relationship involving Source Material MUST preserve privacy boundaries.

A relationship involving Source Material MUST NOT cause Source Material and Knowledge Records to be treated as the same entity.

Source Material MAY be transformed.

Transformation MAY include:

- extraction;
- transcription;
- summarization;
- translation;
- classification;
- normalization;
- conversion;
- redaction;
- enrichment;
- segmentation;
- interpretation;
- synthesis;
- migration;
- import;
- export;
- archival processing;
- implementation-specific rendering.

When Source Material is transformed, the transformation SHOULD preserve enough provenance for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to understand what changed, who or what performed the transformation, what source was used, whether meaning changed, whether review occurred, and whether privacy boundaries were preserved.

Source Material MAY become unavailable, moved, restricted, deleted, corrupted, superseded, replaced, externally inaccessible, or unverifiable.

When Source Material availability changes, the associated Source References and provenance SHOULD preserve enough context for future review where the change affects meaning, validation, authority, privacy, lifecycle state, compatibility, migration, import, export, or downstream use.

Source Material MUST preserve privacy boundaries.

Source Material MUST NOT be exposed, copied, indexed, exported, published, synchronized, summarized, embedded, linked, or processed by an agent merely because doing so improves convenience, search, validation, automation, or implementation behavior.

Where Source Material is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted content.

Source Material SHOULD support validation.

A validator SHOULD be able to determine whether Source Material is distinguishable from Knowledge Records, whether a Source Reference identifies or describes it sufficiently, whether source availability affects interpretation, whether privacy boundaries are preserved, whether provenance is sufficient where required, and whether the source remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, and implementation replacement.

Source Material SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, or archive process MUST NOT silently discard, replace, collapse, expose, reinterpret, or detach Source Material in a way that causes loss of meaning, broken provenance, broken Source References, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, or implementation lock-in.

Source Material is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what material exists, what role it serves, what knowledge it supports, what provenance applies, whether it remains available, whether it is reliable enough for the intended use, whether it has authority in context, whether it is safe to expose, and whether it remains distinguishable from structured knowledge.

## 4. Source Reference Definition

A Source Reference is a traceable reference from a Knowledge Object, Knowledge Record, relationship, decision, workflow, validation result, migration record, import record, export record, or other governed entity to Source Material.

A Source Reference exists to preserve the connection between governed knowledge and the Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to that knowledge.

A Source Reference SHALL identify or describe Source Material clearly enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what source is being referenced where access is permitted.

A Source Reference MAY refer to Source Material that is:

- stored inside a compliant repository;
- stored in a separate source archive;
- stored externally;
- referenced through a durable identifier;
- referenced through a citation;
- referenced through an external reference;
- referenced through a source identifier;
- referenced through a document identifier;
- referenced through an archive reference;
- imported into a compliant environment;
- exported from a compliant environment;
- migrated between compliant environments;
- unavailable but historically referenced;
- restricted by privacy, access, legal, ethical, contractual, or operational constraints.

A Source Reference SHOULD be present when Source Material materially supports:

- content;
- interpretation;
- classification;
- extraction;
- transformation;
- summary;
- relationship creation;
- evidence claims;
- attribution;
- decisions;
- validation;
- authority;
- lifecycle state;
- privacy handling;
- import behavior;
- export behavior;
- migration behavior;
- compatibility;
- downstream use.

A Source Reference MUST preserve the distinction between Source Material and structured knowledge.

A Source Reference to Source Material does not make the Source Material a Knowledge Record.

A Source Reference from a Knowledge Record does not make the Knowledge Record identical to the Source Material.

A Source Reference MAY support a Knowledge Record, but it does not replace the Knowledge Record’s own identity, metadata, provenance, lifecycle state, authority, privacy classification, validation expectations, relationships, or governed meaning.

A Source Reference MAY identify Source Material directly.

A Source Reference MAY identify Source Material indirectly through a governed identifier, external reference, citation, archive reference, metadata record, relationship, source catalog, validation record, import record, export record, migration record, or future governed source-reference structure.

A Source Reference SHOULD be durable enough to remain meaningful when Source Material is renamed, moved, copied, archived, restricted, migrated, imported, exported, backed up, restored, synchronized, reindexed, transformed, validated, processed by an agent, processed by a workflow, or accessed through a different implementation.

A Source Reference MUST NOT depend only on:

- filename;
- folder path;
- storage location;
- display title;
- URL;
- citation style;
- database row;
- search result;
- graph layout;
- backlink behavior;
- user interface state;
- plugin behavior;
- hidden application state;
- agent memory;
- workflow memory;
- implementation-specific identifier.

These items MAY assist discovery, display, navigation, retrieval, storage, citation, validation, migration, import, export, or implementation behavior.

They MUST NOT define source-reference meaning by themselves when that meaning affects interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, workflow behavior, agent behavior, governance, or downstream use.

A Source Reference MAY include or support source-reference metadata.

Source-reference metadata MAY describe:

- referenced Source Material;
- source identifier;
- source title or label;
- source type;
- source location;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source access conditions;
- source support role;
- evidence context;
- attribution;
- extraction context;
- transformation context;
- citation context;
- archive context;
- validation state;
- review state;
- import context;
- export context;
- migration context;
- compatibility expectations.

KS-0005 does not define exact source-reference metadata fields.

A future specification MAY define exact source-reference fields, allowed values, citation structures, source identifiers, archive references, source catalogs, validation rules, import formats, export formats, migration mappings, or serialization syntax.

A Source Reference MAY be supported by a citation.

A citation may help humans recognize, locate, publish, or discuss Source Material.

A citation MUST NOT define the full Source Reference by itself unless a future governed specification explicitly defines how that citation syntax satisfies Source Reference requirements.

A Source Reference MAY be supported by a URL.

A URL may help retrieve Source Material.

A URL MUST NOT be treated as sufficient by itself when link rot, access restriction, moved content, changed content, privacy, provenance, validation, authority, migration, import, export, or compatibility affects interpretation.

A Source Reference MAY be supported by a Source Identifier.

A Source Identifier identifies or supports identification of Source Material.

A Source Identifier MUST remain distinguishable from stable Object Identity unless a future governed specification explicitly defines a compliant identity relationship.

A Source Reference MAY participate in relationships.

A relationship involving a Source Reference SHOULD make clear whether the source provides evidence, origin, attribution, context, support, contradiction, reference, derivation, validation, or another governed role.

A relationship involving a Source Reference MUST preserve the distinction between Source Material, Source References, Knowledge Records, and Knowledge Objects.

A Source Reference SHOULD preserve provenance.

Source-reference provenance MAY identify:

- who or what created the Source Reference;
- when the Source Reference was created where applicable;
- what Source Material was referenced;
- why the Source Reference was created;
- what content, claim, relationship, decision, validation result, or governed entity the source supports;
- whether the Source Reference was created by a human;
- whether the Source Reference was proposed or created by an agent;
- whether the Source Reference was created by a workflow;
- whether the Source Reference was imported;
- whether the Source Reference was exported;
- whether the Source Reference was migrated;
- whether the Source Reference was validated;
- whether the Source Reference was reviewed;
- whether the Source Reference was approved, rejected, deprecated, superseded, or archived.

A Source Reference SHOULD preserve source availability context where availability affects interpretation, validation, authority, privacy, lifecycle state, compatibility, migration, import, export, or downstream use.

If referenced Source Material becomes unavailable, moved, restricted, deleted, corrupted, superseded, replaced, externally inaccessible, or unverifiable, the Source Reference SHOULD preserve or support enough context for future review.

A Source Reference SHOULD preserve source reliability context where reliability affects interpretation, validation, authority, review, governance, or downstream use.

A Source Reference SHOULD preserve source authority context where authority affects reliance, interpretation, approval, governance, publication, validation, or downstream use.

A Source Reference MUST preserve privacy boundaries.

A Source Reference MUST NOT expose restricted Source Material merely to improve traceability, search, validation, linking, publication, migration, import, export, automation, or implementation convenience.

Where a Source Reference points to restricted Source Material, the Source Reference SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted content, restricted identifiers, restricted relationships, restricted attribution, restricted provenance, or restricted context.

A Source Reference SHOULD support validation.

A validator SHOULD be able to determine whether:

- a Source Reference is present where required;
- the referenced Source Material is identifiable where access is permitted;
- the Source Reference preserves the distinction between Source Material and Knowledge Records;
- the Source Reference relies on prohibited hidden implementation behavior;
- source availability affects interpretation;
- source reliability affects interpretation;
- source authority affects interpretation;
- source privacy boundaries are preserved;
- source-reference provenance is sufficient where required;
- the Source Reference remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

A Source Reference SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or citation tool MUST NOT silently discard, replace, collapse, expose, reinterpret, detach, or regenerate a Source Reference in a way that causes loss of meaning, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, or source confusion.

A Source Reference is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what Source Material is referenced, what governed entity the source supports, what role the source plays, whether the source remains available, whether the source is reliable enough for the intended use, whether the source has authority in context, whether the reference is safe to expose, whether provenance is sufficient, and whether the reference remains meaningful across time and implementation replacement.

## 5. Provenance Definition

Provenance is information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a Knowledge Object, Knowledge Record, Source Material, Source Reference, relationship, decision, validation result, migration record, import record, export record, or other governed entity.

Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand where knowledge came from, how it was created, how it changed, what source material was used, what transformations occurred, who or what participated, and what review or validation state applies.

Provenance SHALL be preserved where origin, source support, evidence, attribution, extraction, transformation, agent activity, workflow activity, import, export, migration, validation, review, approval, rejection, supersession, or change history affects meaning, interpretation, authority, privacy, lifecycle state, relationships, compatibility, governance, or downstream use.

Provenance MAY describe:

- original Source Material;
- source support;
- evidence context;
- attribution;
- creator;
- editor;
- reviewer;
- approver;
- rejecting actor;
- agent involvement;
- workflow involvement;
- extraction activity;
- transformation activity;
- summarization activity;
- classification activity;
- validation activity;
- import activity;
- export activity;
- migration activity;
- archival activity;
- revision activity;
- supersession activity;
- deprecation activity;
- privacy handling;
- source availability;
- source reliability;
- source authority;
- source compatibility;
- review state;
- validation state;
- lifecycle context;
- governance context.

Provenance MAY be associated with:

- Knowledge Objects;
- Knowledge Records;
- Source Material;
- Source References;
- relationships;
- metadata;
- validation records;
- decisions;
- standards;
- specifications;
- ADRs;
- RFCs;
- workflows;
- agents;
- implementations;
- imports;
- exports;
- migrations;
- archived artifacts;
- other governed entities.

Provenance is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

Provenance is the contextual information that explains where knowledge came from, what source was used, what action occurred, who or what performed the action, and how the action affects interpretation.

Provenance is not the same as a Source Reference.

A Source Reference points to or identifies Source Material.

Provenance explains the origin, use, handling, transformation, review, validation, movement, or change context associated with the Source Reference or the governed entity it supports.

A Source Reference MAY be part of provenance.

Provenance MAY include or refer to Source References.

Neither concept replaces the other.

Provenance is not the same as Object Identity.

Object Identity identifies the stable Knowledge Object.

Provenance explains how the object, record, source reference, relationship, decision, or governed entity was created, changed, reviewed, validated, imported, exported, migrated, or otherwise handled.

Provenance MUST NOT redefine stable Object Identity unless a governed identity-change process explicitly changes or records identity behavior under the applicable standard.

Provenance is not the same as metadata as a whole.

Provenance MAY be expressed through metadata.

Metadata may also describe identity, description, structure, relationships, lifecycle state, authority, privacy, validation, compatibility, workflow context, agent context, implementation context, or other information.

Provenance metadata is one metadata category, not a replacement for all metadata.

Provenance SHOULD be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine:

- what source material was used;
- what Source Reference applies;
- what evidence supports the governed entity;
- who or what created the governed entity;
- who or what modified the governed entity;
- who or what reviewed the governed entity;
- who or what validated the governed entity;
- whether an agent was involved;
- whether a workflow was involved;
- whether extraction occurred;
- whether transformation occurred;
- whether import occurred;
- whether export occurred;
- whether migration occurred;
- whether review occurred;
- whether approval, rejection, deprecation, supersession, or archival occurred;
- whether privacy boundaries affected what provenance may be exposed;
- whether source availability, reliability, authority, or compatibility affects interpretation.

Provenance SHOULD distinguish between human-created, agent-generated, workflow-generated, imported, exported, migrated, extracted, transformed, validated, reviewed, approved, rejected, superseded, deprecated, and archived knowledge where that distinction affects interpretation.

Provenance SHOULD distinguish evidence from interpretation where that distinction affects meaning, authority, validation, privacy, reviewability, governance, or downstream use.

Provenance SHOULD distinguish original source content from extracted content, summarized content, transformed content, interpreted content, synthesized content, and structured knowledge where that distinction affects interpretation.

Provenance SHOULD distinguish human-authored knowledge from agent-generated knowledge where that distinction affects reviewability, authority, privacy, validation, publication, export, or downstream use.

Provenance SHOULD distinguish agent-proposed output from human-reviewed or approved knowledge where review state affects authority, lifecycle state, validation, governance, or downstream use.

Provenance SHOULD distinguish workflow completion from approval unless a future governed workflow specification explicitly defines workflow completion as approval.

Provenance MAY be complete, partial, restricted, inferred, unavailable, uncertain, or historically preserved.

Where provenance is incomplete, uncertain, restricted, unavailable, or inferred, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, lifecycle state, compatibility, migration, import, export, governance, or downstream use.

Provenance MUST preserve privacy boundaries.

Provenance MUST NOT expose restricted Source Material, restricted attribution, restricted actors, restricted workflows, restricted relationships, restricted identifiers, restricted content, or restricted context merely to improve traceability, validation, linking, publication, migration, import, export, automation, or implementation convenience.

Where full provenance cannot be exposed because of privacy restrictions, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Provenance SHOULD support validation.

A validator SHOULD be able to determine whether provenance is present where required, whether provenance identifies source support where applicable, whether agent or workflow involvement is reviewable where required, whether extraction or transformation history is preserved where needed, whether privacy boundaries are preserved, and whether provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Provenance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or citation tool MUST NOT silently discard, replace, collapse, expose, reinterpret, detach, or regenerate provenance in a way that causes loss of meaning, broken Source References, broken relationships, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, or provenance confusion.

Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine where knowledge came from, what source material supports it, what transformation occurred, who or what participated, whether review or validation occurred, whether privacy boundaries apply, whether the provenance is complete enough for the intended use, and whether the provenance remains meaningful across time and implementation replacement.

## 6. Source Material and Knowledge Record Boundaries

Source Material and Knowledge Records SHALL remain distinguishable within The Brain Standard.

Source Material is evidence, input, origin, context, attribution, contradiction, or reference material.

A Knowledge Record is structured knowledge created from, about, or in response to Source Material, human reasoning, agent activity, workflow activity, import activity, export activity, migration activity, validation activity, or another governed process.

A Source Material artifact does not become a Knowledge Record merely because it is stored in a compliant repository.

A Knowledge Record does not become Source Material merely because it references, quotes, summarizes, extracts from, transforms, interprets, classifies, validates, or discusses Source Material.

A Knowledge Record MAY contain extracted, quoted, summarized, transformed, interpreted, classified, or synthesized content derived from Source Material.

When a Knowledge Record contains source-derived content, the record SHOULD preserve enough provenance for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to determine:

- what Source Material was used;
- what portion or aspect of the Source Material was used where applicable;
- whether the content was extracted, quoted, summarized, transformed, interpreted, classified, translated, normalized, redacted, synthesized, or otherwise changed;
- who or what performed the action;
- whether an agent was involved;
- whether a workflow was involved;
- whether human review occurred;
- whether validation occurred;
- whether the transformation changed meaning;
- whether privacy boundaries apply;
- whether the source remains available;
- whether source reliability, source authority, or source compatibility affects interpretation.

A Source Reference connects a Knowledge Record or other governed entity to Source Material.

A Source Reference MUST NOT erase the boundary between the source and the knowledge derived from the source.

A citation, URL, archive reference, source identifier, external reference, backlink, file path, database reference, graph edge, or implementation-specific link MAY help identify or retrieve Source Material.

Those mechanisms MUST NOT cause Source Material and Knowledge Records to be treated as the same entity unless a future governed specification explicitly defines a compliant representation that preserves the distinction.

A Source Material artifact MAY be described by a Knowledge Record.

A Knowledge Record about Source Material SHOULD make clear that it is describing, summarizing, interpreting, extracting from, transforming, classifying, validating, or otherwise creating structured knowledge about the source.

A Knowledge Record about Source Material MUST NOT falsely present itself as the original Source Material.

A Source Material artifact MAY be copied, quoted, extracted, summarized, transformed, converted, archived, imported, exported, migrated, backed up, restored, indexed, or rendered for practical use.

Such actions MUST preserve enough source-reference or provenance context to prevent confusion between:

- original Source Material;
- copied Source Material;
- archived Source Material;
- extracted content;
- quoted content;
- summarized content;
- transformed content;
- interpreted content;
- synthesized knowledge;
- Knowledge Records;
- implementation-specific representations;
- validation records;
- migration records;
- import records;
- export records.

Duplication MAY be acceptable for preservation, quotation, extraction, backup, review, accessibility, legal compliance, offline use, migration, export, import, or implementation convenience.

Duplication MUST NOT erase the distinction between original Source Material and structured knowledge derived from, about, or in response to that source.

A Knowledge Record SHOULD preserve Source References when Source Material materially supports content, interpretation, classification, relationship creation, evidence claims, attribution, decisions, validation, authority, lifecycle state, privacy handling, import behavior, export behavior, migration behavior, compatibility, or downstream use.

A Knowledge Record SHOULD preserve provenance when Source Material is used to create, modify, extract, transform, summarize, classify, validate, review, approve, reject, import, export, migrate, or supersede knowledge.

A Knowledge Record MUST NOT silently incorporate Source Material in a way that obscures the origin, evidence, attribution, extraction, transformation, review state, validation state, privacy boundary, or authority context when those factors affect interpretation.

A Knowledge Record MUST NOT falsely imply that Source Material remains available, verified, authoritative, unrestricted, current, complete, reliable, or unchanged when that condition is unknown, false, restricted, superseded, unverifiable, or materially uncertain.

Where Source Material is unavailable, moved, restricted, deleted, corrupted, superseded, replaced, externally inaccessible, or unverifiable, the Knowledge Record SHOULD preserve enough context for future review when that condition affects meaning, validation, authority, privacy, lifecycle state, compatibility, migration, import, export, governance, or downstream use.

A Knowledge Record MAY become Source Material for a later Knowledge Record.

When a Knowledge Record is used as Source Material for another Knowledge Record, the later record SHOULD preserve provenance that identifies the earlier Knowledge Record as the source used.

When a Knowledge Record is used as Source Material, it MUST remain clear whether the earlier record is being treated as:

- structured knowledge;
- evidence for later work;
- a prior interpretation;
- a reviewed record;
- an approved record;
- a superseded record;
- a deprecated record;
- an imported record;
- a migrated record;
- a validation record;
- a source-derived record;
- another governed role.

A Knowledge Record derived from Source Material MAY become a distinct Knowledge Object when it has its own governed meaning, identity, metadata, provenance, lifecycle state, authority, privacy classification, validation expectations, relationships, or compatibility expectations.

A Source Material artifact SHOULD NOT receive stable Object Identity merely because it is referenced, stored, cited, linked, archived, copied, imported, exported, migrated, indexed, or displayed.

A Source Material artifact MAY receive or be associated with stable Object Identity only when a governed standard, specification, or process defines it as a Knowledge Object or otherwise establishes a compliant identity relationship.

A Source Identifier MUST remain distinguishable from stable Object Identity unless a future governed specification explicitly defines a compliant identity relationship.

A Source Reference MUST remain distinguishable from both Source Material and the Knowledge Record that references the source.

A Source Reference is the traceable connection.

Source Material is the referenced material.

A Knowledge Record is the structured knowledge.

Provenance is the contextual history explaining origin, source use, transformation, review, validation, movement, or change.

These roles MAY interact, but they MUST remain distinguishable when the distinction affects meaning, interpretation, authority, privacy, lifecycle state, relationships, validation, compatibility, migration, import, export, governance, or downstream use.

A compliant implementation MAY store Source Material and Knowledge Records together.

A compliant implementation MAY store Source Material and Knowledge Records separately.

A compliant implementation MAY represent Source Material, Source References, Knowledge Records, and provenance through files, metadata, databases, graph structures, object records, sidecar files, APIs, indexes, archives, or future governed formats.

The representation method does not define the boundary.

The boundary is defined by role, governed meaning, metadata, Source References, provenance, lifecycle state, authority, privacy classification, validation expectations, and compatibility expectations.

Storage location MUST NOT be the only mechanism used to distinguish Source Material from Knowledge Records where the distinction affects meaning.

Filename MUST NOT be the only mechanism used to distinguish Source Material from Knowledge Records where the distinction affects meaning.

File format MUST NOT be the only mechanism used to distinguish Source Material from Knowledge Records where the distinction affects meaning.

Application type MUST NOT be the only mechanism used to distinguish Source Material from Knowledge Records where the distinction affects meaning.

Folder placement MUST NOT be the only mechanism used to distinguish Source Material from Knowledge Records where the distinction affects meaning.

Agent memory, workflow memory, user memory, hidden application state, plugin behavior, backlink behavior, graph layout, search ranking, vector similarity, or implementation-specific behavior MUST NOT be the only mechanism used to distinguish Source Material from Knowledge Records where the distinction affects meaning.

Source Material and Knowledge Record boundaries MUST preserve privacy.

A Knowledge Record MUST NOT expose restricted Source Material merely because the record is easier to search, summarize, index, validate, export, publish, migrate, process by an agent, or present through an implementation.

A Source Reference MUST NOT expose restricted Source Material merely because the referenced material supports a less restricted Knowledge Record.

Where Source Material and a Knowledge Record have different privacy expectations, the stricter applicable privacy expectation SHOULD govern handling unless a future governed privacy specification defines a different compliant rule.

Source Material and Knowledge Record boundaries SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Material is distinguishable from Knowledge Records;
- Source References are distinguishable from both sources and records;
- provenance is distinguishable from both sources and records;
- source-derived content is identified where required;
- extracted, quoted, summarized, transformed, interpreted, or synthesized content is distinguishable where needed;
- Source Identifiers are distinguishable from stable Object Identity;
- storage location, filename, file format, folder placement, URL, citation style, application state, agent memory, workflow memory, or implementation-specific behavior is not the only source of boundary meaning;
- privacy boundaries are preserved;
- source availability, reliability, authority, or compatibility affects interpretation;
- boundaries remain meaningful across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Source Material and Knowledge Record boundaries SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or citation tool MUST NOT silently collapse, discard, expose, reinterpret, detach, merge, duplicate, or replace Source Material, Knowledge Records, Source References, or provenance in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, or source confusion.

Source Material and Knowledge Record boundaries are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what remains original source material, what is structured knowledge, what reference connects them, what provenance explains their history, whether privacy boundaries apply, whether source support remains valid, and whether the distinction remains meaningful across time and implementation replacement.

## 7. Evidence and Support

Evidence is Source Material, extracted content, cited material, observation, validation result, relationship, reasoning record, or other support used to justify, explain, verify, challenge, or contextualize a Knowledge Object, Knowledge Record, claim, relationship, decision, classification, interpretation, validation result, workflow output, agent output, or other governed entity.

Support is the role evidence plays in relation to a governed entity.

Evidence and support SHALL remain distinguishable from Source Material, Source References, Provenance, Knowledge Records, relationships, authority, validation, approval, and truth claims.

Source Material may provide evidence.

A Source Reference may connect a governed entity to evidence.

Provenance may explain how evidence was used, extracted, transformed, interpreted, reviewed, validated, imported, exported, migrated, or changed.

A Knowledge Record may contain or describe evidence.

A relationship may express an evidence-supporting connection.

None of these roles replaces the others.

Evidence MAY support:

- content;
- claims;
- observations;
- interpretations;
- classifications;
- summaries;
- transformations;
- source-derived knowledge;
- relationships;
- decisions;
- validation results;
- authority assessments;
- lifecycle state changes;
- privacy handling;
- agent outputs;
- workflow outputs;
- import decisions;
- export decisions;
- migration decisions;
- governance decisions;
- downstream use.

Evidence MAY provide different support roles.

Support roles MAY include:

- direct support;
- indirect support;
- contextual support;
- background support;
- attribution support;
- origin support;
- contradiction;
- partial contradiction;
- uncertainty;
- limitation;
- example;
- comparison;
- validation support;
- review support;
- migration support;
- import support;
- export support;
- governance support.

KS-0005 does not define an exhaustive controlled vocabulary for evidence support roles.

A future specification MAY define exact evidence-support fields, support-role values, confidence values, citation formats, validation rules, evidence-ranking rules, source reliability values, authority values, contradiction handling, conflict handling, or review workflows.

Evidence SHOULD be connected to governed entities through Source References, relationships, provenance, metadata, validation records, review records, or another governed mechanism where evidence affects interpretation, authority, validation, lifecycle state, privacy, compatibility, governance, or downstream use.

Evidence MUST NOT be treated as authoritative merely because it exists.

Evidence MUST NOT be treated as validated merely because it is referenced.

Evidence MUST NOT be treated as approved merely because it is attached to a Knowledge Record.

Evidence MUST NOT be treated as true merely because it is structured, cited, indexed, summarized, embedded, linked, frequently used, generated by an agent, produced by a workflow, or stored in a compliant repository.

Evidence SHOULD remain reviewable where it materially affects meaning, authority, validation, lifecycle state, governance, publication, migration, import, export, or downstream use.

Evidence SHOULD preserve enough provenance to determine:

- what Source Material was used;
- what portion or aspect of the Source Material was used where applicable;
- whether the evidence was quoted, extracted, summarized, transformed, interpreted, classified, translated, normalized, redacted, synthesized, inferred, validated, reviewed, imported, exported, or migrated;
- who or what selected the evidence;
- who or what interpreted the evidence;
- whether an agent was involved;
- whether a workflow was involved;
- whether human review occurred;
- whether validation occurred;
- whether the evidence supports, contradicts, limits, contextualizes, or qualifies the governed entity;
- whether privacy boundaries apply;
- whether source availability, reliability, authority, or compatibility affects interpretation.

Evidence SHOULD distinguish between evidence and interpretation.

Evidence is what supports, challenges, explains, contextualizes, or qualifies a governed entity.

Interpretation is the meaning, conclusion, classification, summary, judgment, or structured knowledge derived from or associated with evidence.

A Knowledge Record MAY contain both evidence and interpretation.

Where evidence and interpretation are both present, the distinction SHOULD remain clear when it affects meaning, authority, privacy, validation, reviewability, governance, or downstream use.

Evidence SHOULD distinguish between original evidence and transformed evidence.

Original evidence is evidence that remains close to the original Source Material.

Transformed evidence is evidence that has been extracted, summarized, translated, normalized, redacted, classified, converted, synthesized, interpreted, or otherwise changed.

Where transformed evidence is used, provenance SHOULD preserve enough context to determine what transformation occurred and whether meaning, privacy, authority, validation, or compatibility was affected.

Evidence MAY be complete, partial, restricted, uncertain, contradictory, outdated, superseded, inferred, unavailable, unverifiable, or disputed.

Where evidence is incomplete, partial, restricted, uncertain, contradictory, outdated, superseded, inferred, unavailable, unverifiable, or disputed, that condition SHOULD be preserved or represented when it affects interpretation, validation, authority, lifecycle state, privacy, compatibility, migration, import, export, governance, or downstream use.

Evidence MAY conflict with other evidence.

Conflicting evidence MUST NOT be silently collapsed, ignored, overwritten, hidden, or treated as resolved merely because one source is newer, easier to access, more frequently referenced, agent-selected, workflow-selected, indexed, embedded, or implementation-preferred.

Where evidence conflicts, a compliant system SHOULD preserve enough context for future review, including source support, provenance, reliability, authority, availability, review state, validation state, and privacy boundaries where applicable.

Evidence MAY support uncertainty.

A Knowledge Record MAY explicitly preserve uncertainty when available evidence is incomplete, ambiguous, contradictory, low-confidence, restricted, unverifiable, or context-dependent.

Uncertainty MUST NOT be removed merely to improve readability, automation, graph clarity, search ranking, validation convenience, export formatting, workflow completion, or agent confidence.

Evidence MAY support contradiction.

Contradictory evidence SHOULD remain distinguishable from supporting evidence where contradiction affects interpretation, validation, authority, lifecycle state, governance, or downstream use.

A Source Reference or relationship MAY indicate that Source Material contradicts, limits, qualifies, challenges, or weakens a governed entity.

Evidence MAY support attribution.

Attribution evidence SHOULD identify or describe the person, organization, system, source, author, creator, publisher, agent, workflow, implementation, or other actor associated with the creation, publication, modification, extraction, transformation, interpretation, transmission, validation, or review of Source Material or governed knowledge where that context affects interpretation.

Evidence MAY support validation.

Validation evidence SHOULD preserve enough context to determine what was checked, what source was used, what rule or expectation applied, who or what performed validation, whether validation passed, failed, partially passed, was blocked, or was deferred, and whether validation affects meaning, authority, privacy, lifecycle state, compatibility, migration, import, export, or governance.

Evidence MAY support authority.

Evidence supporting authority SHOULD remain distinguishable from authority itself.

Authority is a governance, review, approval, or interpretive status.

Evidence may support an authority assessment, but evidence does not automatically create authority.

Evidence MAY support lifecycle state.

Evidence supporting lifecycle state SHOULD remain distinguishable from lifecycle state itself.

Evidence may support draft, review, approved, deprecated, superseded, rejected, archived, or other lifecycle decisions, but evidence does not automatically change lifecycle state unless a governed process or future specification defines that behavior.

Evidence MAY support privacy handling.

Evidence and support MUST preserve privacy boundaries.

Evidence MUST NOT expose restricted Source Material, restricted content, restricted attribution, restricted relationships, restricted identifiers, restricted provenance, restricted validation results, or restricted context merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, or implementation convenience.

Where evidence is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Evidence SHOULD support validation.

A validator SHOULD be able to determine whether:

- evidence is present where required;
- evidence is distinguishable from interpretation;
- evidence is distinguishable from approval;
- evidence is distinguishable from authority;
- evidence is distinguishable from validation status;
- evidence is connected to the governed entity it supports where applicable;
- evidence support role is clear where applicable;
- Source References identify or describe supporting Source Material where access is permitted;
- provenance is sufficient where evidence affects meaning;
- conflicting evidence is preserved where applicable;
- uncertainty is preserved where applicable;
- privacy boundaries are preserved;
- evidence remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Evidence SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, resolve, approve, reject, or regenerate evidence in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, evidence confusion, or source confusion.

Evidence and support are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what evidence exists, what governed entity it supports, what role the evidence plays, whether it supports or contradicts the governed entity, whether uncertainty remains, whether the evidence has been reviewed or validated, whether privacy boundaries apply, whether source support remains available, and whether evidence meaning remains intact across time and implementation replacement.

## 8. Attribution

Attribution is information identifying the person, organization, system, source, author, creator, publisher, agent, workflow, implementation, or other actor associated with the creation, publication, modification, extraction, transformation, interpretation, transmission, validation, review, approval, rejection, import, export, migration, or preservation of Source Material, Source References, provenance, evidence, Knowledge Objects, Knowledge Records, relationships, decisions, validation results, workflow outputs, agent outputs, or other governed entities.

Attribution exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand who or what is associated with source creation, knowledge creation, source handling, evidence selection, interpretation, transformation, review, validation, governance, or change.

Attribution SHALL be preserved where the responsible person, organization, system, source, agent, workflow, implementation, publisher, creator, reviewer, validator, importer, exporter, migrator, or other actor affects meaning, interpretation, authority, privacy, lifecycle state, validation, provenance, compatibility, governance, publication, or downstream use.

Attribution MAY identify:

- source author;
- source creator;
- source publisher;
- source owner;
- source provider;
- source repository;
- source system;
- source organization;
- human creator;
- human editor;
- human reviewer;
- human approver;
- human rejector;
- agent;
- model class;
- workflow;
- validator;
- implementation;
- import process;
- export process;
- migration process;
- archival process;
- transformation process;
- extraction process;
- summarization process;
- classification process;
- other responsible or associated actors.

Attribution is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, contradiction, or support.

Attribution identifies who or what created, published, modified, transmitted, selected, extracted, transformed, interpreted, reviewed, validated, approved, rejected, imported, exported, migrated, preserved, or otherwise handled that material or the knowledge derived from it.

Attribution is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

Attribution identifies the actor, source, organization, agent, workflow, system, implementation, or process associated with that source, reference, evidence, provenance, or governed entity.

Attribution is not the same as Provenance.

Provenance explains origin, source use, transformation, review, validation, movement, or change context.

Attribution identifies responsible or associated actors within that context.

Attribution MAY be part of provenance.

Provenance MAY include attribution.

Neither concept replaces the other.

Attribution is not the same as authority.

Attribution may identify an authoritative source, reviewer, approver, publisher, organization, standard, workflow, or implementation.

However, attribution alone does not make knowledge authoritative.

Authority requires governance, review status, approval status, interpretive weight, or another governed authority mechanism.

Attribution is not the same as truth.

Attribution identifies who or what is associated with information, evidence, source material, or knowledge.

Attribution does not prove that the associated content is accurate, current, complete, reliable, approved, validated, or authoritative.

Attribution is not the same as ownership.

Attribution may identify ownership where ownership affects source handling, privacy, licensing, authority, governance, publication, or downstream use.

However, attribution does not define a complete ownership, licensing, copyright, access-control, or legal-rights model.

A future specification MAY define exact ownership, licensing, rights, permissions, citation, or credit fields where required.

Attribution SHOULD distinguish between:

- creator;
- author;
- publisher;
- editor;
- source provider;
- reviewer;
- approver;
- validator;
- importer;
- exporter;
- migrator;
- agent;
- workflow;
- implementation;
- system;
- organization;
- other responsible or associated roles.

Attribution SHOULD preserve actor roles where role affects interpretation, authority, privacy, reviewability, validation, governance, publication, import, export, migration, or downstream use.

A person, organization, agent, workflow, system, implementation, or source MAY have more than one attribution role.

Multiple attribution roles are allowed.

Attribution role confusion is not allowed when the distinction affects meaning, authority, privacy, validation, governance, or downstream use.

For example:

- an author is not automatically a reviewer;
- a reviewer is not automatically an approver;
- an agent is not automatically a human reviewer;
- a workflow output is not automatically approved knowledge;
- a publisher is not automatically the creator;
- an implementation is not automatically the authority;
- a source provider is not automatically the owner;
- an importer is not automatically the creator;
- a validator is not automatically the final authority.

Attribution SHOULD identify agent involvement where an agent creates, modifies, extracts, summarizes, classifies, interprets, validates, links, proposes, enriches, imports, exports, migrates, or otherwise affects Source Material, Source References, provenance, evidence, Knowledge Objects, Knowledge Records, relationships, decisions, validation results, or workflow outputs.

Agent attribution SHOULD remain reviewable where agent activity affects meaning, authority, privacy, validation, publication, lifecycle state, governance, or downstream use.

Agent attribution MUST NOT make an agent an unreviewable authority.

Attribution SHOULD identify workflow involvement where a workflow creates, modifies, extracts, transforms, routes, validates, reviews, approves, rejects, imports, exports, migrates, archives, supersedes, or otherwise affects governed knowledge.

Workflow attribution SHOULD remain distinguishable from human approval unless a future governed workflow specification explicitly defines when workflow activity creates approval.

Attribution SHOULD identify human review where human review affects authority, lifecycle state, validation, privacy, publication, governance, or downstream use.

Where human review has not occurred, attribution MUST NOT falsely imply that a human reviewed, approved, validated, corrected, or accepted the knowledge.

Attribution SHOULD identify source authorship or source publication where that context affects interpretation, source reliability, source authority, evidence quality, citation, governance, legal handling, privacy, publication, or downstream use.

Where source authorship is unknown, uncertain, restricted, disputed, inferred, or unavailable, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, governance, publication, or downstream use.

Attribution MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, anonymous, pseudonymous, organizational, system-generated, agent-generated, workflow-generated, imported, exported, migrated, or historically preserved.

Where attribution is incomplete, uncertain, restricted, inferred, unavailable, disputed, anonymous, pseudonymous, organizational, system-generated, agent-generated, workflow-generated, imported, exported, or migrated, that condition SHOULD be preserved when it affects interpretation, authority, privacy, validation, lifecycle state, compatibility, governance, publication, or downstream use.

Attribution MAY be expressed through metadata.

Attribution metadata MAY describe:

- actor identity;
- actor role;
- actor type;
- source creator;
- source author;
- source publisher;
- source provider;
- source owner where applicable;
- editor;
- reviewer;
- approver;
- validator;
- agent;
- workflow;
- implementation;
- source system;
- import process;
- export process;
- migration process;
- transformation process;
- extraction process;
- review state;
- validation state;
- attribution certainty;
- attribution restriction;
- attribution privacy;
- attribution compatibility expectations.

KS-0005 does not define exact attribution metadata fields.

A future specification MAY define exact attribution fields, actor identifiers, role vocabularies, citation rules, ownership fields, source-author fields, agent-attribution fields, workflow-attribution fields, validation rules, import formats, export formats, migration mappings, or serialization syntax.

Attribution MAY be supported by Source References.

A Source Reference may identify Source Material that contains or supports attribution.

A Source Reference may also identify the source used to determine attribution.

Attribution supported by a Source Reference SHOULD preserve enough provenance to determine what source was used, whether attribution was extracted or inferred, whether review occurred, and whether privacy boundaries apply.

Attribution MAY be supported by evidence.

Evidence supporting attribution SHOULD remain distinguishable from attribution itself.

Evidence may support who created, published, modified, reviewed, validated, imported, exported, migrated, or transmitted source material or knowledge.

Evidence does not automatically make attribution certain, authoritative, complete, or approved.

Attribution MAY be supported by relationships.

A relationship may connect a governed entity to a person, organization, source, agent, workflow, system, implementation, validator, reviewer, approver, importer, exporter, migrator, or other actor.

A relationship involving attribution SHOULD make clear what attribution role is being expressed where the role affects meaning.

Attribution MUST preserve privacy boundaries.

Attribution MUST NOT expose restricted people, restricted organizations, restricted source systems, restricted agents, restricted workflows, restricted identifiers, restricted relationships, restricted Source Material, restricted content, restricted review history, or restricted context merely to improve traceability, citation, search, validation, publication, migration, import, export, automation, or implementation convenience.

Where attribution is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Attribution SHOULD support validation.

A validator SHOULD be able to determine whether:

- attribution is present where required;
- attribution role is clear where role affects interpretation;
- attribution is distinguishable from authority;
- attribution is distinguishable from truth;
- attribution is distinguishable from ownership unless ownership is explicitly represented;
- agent involvement is identified where required;
- workflow involvement is identified where required;
- human review is not falsely implied;
- attribution evidence is present where required;
- Source References support attribution where applicable;
- attribution uncertainty is preserved where applicable;
- attribution privacy boundaries are preserved;
- attribution remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Attribution SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, anonymize, deanonymize, or regenerate attribution in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, attribution confusion, or source confusion.

Attribution is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine who or what is associated with Source Material, Source References, evidence, provenance, Knowledge Objects, Knowledge Records, relationships, decisions, validation results, workflow outputs, agent outputs, or other governed entities; what attribution role applies; whether attribution is certain, partial, restricted, inferred, disputed, or unavailable; whether attribution affects authority, privacy, validation, governance, publication, or downstream use; and whether attribution remains meaningful across time and implementation replacement.

## 9. Extraction Provenance

Extraction Provenance is provenance associated with selecting, copying, quoting, transcribing, parsing, segmenting, summarizing, classifying, normalizing, redacting, or otherwise taking information from Source Material for use in a Knowledge Object, Knowledge Record, Source Reference, relationship, validation result, workflow output, agent output, or other governed entity.

Extraction Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what was taken from Source Material, how it was taken, who or what performed the extraction, whether the extraction changed meaning, whether review occurred, and whether privacy boundaries apply.

Extraction Provenance SHALL be preserved where extraction affects meaning, interpretation, evidence, attribution, authority, privacy, lifecycle state, validation, relationships, compatibility, governance, publication, migration, import, export, or downstream use.

Extraction MAY include:

- quotation;
- copying;
- transcription;
- parsing;
- segmentation;
- summarization;
- classification;
- normalization;
- redaction;
- translation;
- conversion;
- selection of excerpts;
- extraction of metadata;
- extraction of relationships;
- extraction of identifiers;
- extraction of evidence;
- extraction of claims;
- extraction of decisions;
- extraction of validation results;
- extraction performed by a human;
- extraction proposed or performed by an agent;
- extraction performed through a workflow;
- extraction performed during import;
- extraction performed during export;
- extraction performed during migration;
- extraction performed by an implementation.

Extraction Provenance SHOULD identify or describe:

- the Source Material used;
- the Source Reference used where applicable;
- the extracted content;
- the portion or aspect of the Source Material extracted where applicable;
- the extraction method;
- who or what performed the extraction;
- when extraction occurred where applicable;
- whether an agent was involved;
- whether a workflow was involved;
- whether the extraction was manual, automated, inferred, imported, exported, migrated, or implementation-generated;
- whether the extraction was reviewed;
- whether the extraction was validated;
- whether the extraction changed meaning;
- whether the extraction was complete, partial, restricted, uncertain, or lossy;
- whether privacy boundaries affected the extracted content;
- whether source availability, reliability, authority, or compatibility affects interpretation.

Extraction Provenance is not the same as Source Material.

Source Material is the original or reference material.

Extraction Provenance explains how information was taken from that material.

Extraction Provenance is not the same as extracted content.

Extracted content is the selected, copied, transcribed, parsed, summarized, classified, normalized, redacted, or transformed information.

Extraction Provenance explains where the extracted content came from, how it was produced, who or what produced it, and what context affects its interpretation.

Extraction Provenance is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

Extraction Provenance explains how information was extracted from that Source Material and how the extraction affects the governed entity.

Extraction Provenance is not the same as Transformation Provenance.

Extraction Provenance concerns taking information from Source Material.

Transformation Provenance concerns changing Source Material, extracted content, or prior knowledge into another representation, summary, translation, classification, interpretation, structured record, derived object, migrated form, or implementation-specific representation.

Extraction and transformation MAY occur together.

Where extraction and transformation occur together, the provenance SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to determine what was extracted, what was transformed, and whether meaning, authority, privacy, validation, compatibility, or governance was affected.

Extraction SHOULD preserve evidence boundaries.

Extracted content SHOULD remain distinguishable from:

- original Source Material;
- copied Source Material;
- quoted content;
- summarized content;
- transformed content;
- interpreted content;
- synthesized knowledge;
- Knowledge Records;
- Source References;
- provenance;
- validation results;
- agent outputs;
- workflow outputs;
- implementation-specific representations.

A Knowledge Record MAY contain extracted content.

When a Knowledge Record contains extracted content, the Knowledge Record SHOULD preserve enough Extraction Provenance to determine what Source Material was used, what extraction occurred, whether the extraction was reviewed, whether the extraction changed meaning, and whether privacy boundaries apply.

Extraction SHOULD preserve source context where context affects interpretation.

Source context MAY include:

- surrounding text;
- document section;
- page, paragraph, timestamp, line, field, frame, record, message, or segment location where applicable;
- source creator;
- source date;
- source version;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source format;
- source access conditions;
- source limitations;
- conflicting source context;
- superseded source context.

KS-0005 does not define exact locator syntax for extraction context.

A future specification MAY define exact page references, paragraph references, line references, timestamp references, fragment identifiers, quote selectors, extraction fields, source-location fields, redaction markers, validation rules, import formats, export formats, migration mappings, or serialization syntax.

Extraction MAY be complete or partial.

Partial extraction is allowed.

Partial extraction MUST NOT falsely imply that the extracted content represents the whole Source Material when omitted context affects interpretation, validation, authority, privacy, governance, publication, or downstream use.

Extraction MAY be lossy.

Lossy extraction occurs when content, formatting, structure, context, metadata, relationships, source quality, source order, source timing, or source meaning is changed, omitted, compressed, normalized, redacted, summarized, or otherwise reduced during extraction.

Where extraction is lossy, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, lifecycle state, compatibility, migration, import, export, governance, or downstream use.

Extraction MAY be uncertain.

Extraction uncertainty SHOULD be preserved when the extracted content, source location, source meaning, attribution, translation, transcription, parsing, segmentation, classification, or evidence role is unclear, disputed, incomplete, inferred, low-confidence, restricted, unavailable, or unverifiable.

Extraction MAY be performed by humans.

Human extraction SHOULD preserve attribution and review context where extraction affects meaning, authority, validation, privacy, publication, governance, or downstream use.

Extraction MAY be performed by agents.

Agent extraction SHOULD preserve agent attribution, instruction context, source context, extraction method, review state, validation state, and uncertainty where agent activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Agent-extracted content MUST NOT be treated as human-reviewed, validated, approved, authoritative, complete, accurate, or publication-ready merely because an agent produced it.

Extraction MAY be performed through workflows.

Workflow extraction SHOULD preserve workflow attribution, workflow state, source context, extraction method, review state, validation state, and approval state where workflow activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Workflow completion MUST NOT be treated as human approval unless a future governed workflow specification explicitly defines that behavior.

Extraction MAY occur during import, export, or migration.

Import Extraction Provenance SHOULD preserve what content was extracted from the import source, what source identifiers or legacy identifiers were used, what mapping occurred, whether meaning was changed, whether review occurred, and whether source context was preserved.

Export Extraction Provenance SHOULD preserve what content was extracted for export, what was omitted, whether privacy boundaries affected the export, whether meaning was changed, and whether export compatibility was preserved.

Migration Extraction Provenance SHOULD preserve what content was extracted during migration, what mapping occurred, whether source references remained valid, whether provenance remained intact, whether any loss occurred, and whether review or validation occurred.

Extraction MUST preserve privacy boundaries.

Extraction MUST NOT expose restricted Source Material, restricted content, restricted attribution, restricted relationships, restricted identifiers, restricted provenance, restricted validation results, restricted source context, or restricted metadata merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, or implementation convenience.

Where extracted content is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Where Source Material is restricted but extracted content is less restricted, the extraction SHOULD preserve enough context to prevent accidental exposure of restricted source details.

Where extracted content is more restricted than the Source Material because of interpretation, aggregation, synthesis, context, privacy risk, or downstream use, the stricter applicable privacy expectation SHOULD govern handling unless a future governed privacy specification defines a different compliant rule.

Extraction SHOULD support validation.

A validator SHOULD be able to determine whether:

- extracted content is distinguishable from Source Material;
- extracted content is distinguishable from interpretation;
- extracted content is distinguishable from transformed content;
- Extraction Provenance is present where required;
- the Source Material is identified or described where access is permitted;
- the extraction method is clear where method affects interpretation;
- the extraction actor is clear where attribution affects interpretation;
- agent or workflow involvement is identified where required;
- review state is clear where review affects authority or lifecycle state;
- validation state is clear where validation affects downstream use;
- lossy extraction is represented where applicable;
- partial extraction is represented where applicable;
- extraction uncertainty is preserved where applicable;
- privacy boundaries are preserved;
- Extraction Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Extraction SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, re-extract, or regenerate Extraction Provenance in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, extraction confusion, evidence confusion, or source confusion.

Extraction Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what was extracted, what source was used, what portion or aspect of the source was used where applicable, who or what performed the extraction, whether extraction changed meaning, whether extraction was reviewed or validated, whether privacy boundaries apply, whether extraction remains compatible across implementation replacement, and whether the extracted content remains distinguishable from original Source Material, transformed content, interpretation, and structured knowledge.

## 10. Transformation Provenance

Transformation Provenance is provenance associated with changing Source Material, extracted content, prior knowledge, metadata, relationships, evidence, Source References, validation results, workflow outputs, agent outputs, import records, export records, migration records, or other governed entities into another representation, summary, translation, classification, interpretation, structured record, derived object, migrated form, exported form, or implementation-specific representation.

Transformation Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what changed, why it changed, who or what performed the transformation, what source or prior state was used, whether meaning changed, whether review occurred, whether validation occurred, and whether privacy boundaries apply.

Transformation Provenance SHALL be preserved where transformation affects meaning, interpretation, evidence, attribution, authority, privacy, lifecycle state, validation, relationships, compatibility, governance, publication, migration, import, export, or downstream use.

Transformation MAY include:

- summarization;
- translation;
- normalization;
- classification;
- interpretation;
- synthesis;
- redaction;
- conversion;
- restructuring;
- segmentation;
- enrichment;
- annotation;
- deduplication;
- merging;
- splitting;
- mapping;
- migration;
- import transformation;
- export transformation;
- format conversion;
- schema conversion;
- metadata transformation;
- relationship transformation;
- source-reference transformation;
- validation-result transformation;
- implementation-specific rendering;
- agent-generated transformation;
- workflow-generated transformation;
- human-created transformation.

Transformation Provenance SHOULD identify or describe:

- the Source Material, extracted content, prior knowledge, metadata, relationship, validation result, or governed entity transformed;
- the Source Reference used where applicable;
- the prior state before transformation where applicable;
- the transformed output;
- the transformation method;
- the transformation purpose where applicable;
- who or what performed the transformation;
- when transformation occurred where applicable;
- whether an agent was involved;
- whether a workflow was involved;
- whether the transformation was manual, automated, inferred, imported, exported, migrated, or implementation-generated;
- whether the transformation was reviewed;
- whether the transformation was validated;
- whether the transformation changed meaning;
- whether the transformation was complete, partial, restricted, uncertain, lossy, reversible, or irreversible;
- whether privacy boundaries affected the transformation;
- whether source availability, source reliability, source authority, or source compatibility affects interpretation.

Transformation Provenance is not the same as Source Material.

Source Material is original or reference material.

Transformation Provenance explains how Source Material or source-derived material was changed.

Transformation Provenance is not the same as extracted content.

Extracted content is information taken from Source Material.

Transformation Provenance explains how that extracted content was changed, represented, summarized, classified, interpreted, normalized, translated, converted, migrated, imported, exported, or otherwise transformed.

Transformation Provenance is not the same as Extraction Provenance.

Extraction Provenance concerns taking information from Source Material.

Transformation Provenance concerns changing Source Material, extracted content, prior knowledge, metadata, relationships, evidence, Source References, validation results, workflow outputs, agent outputs, or other governed entities into a different form, meaning, structure, representation, or use.

Extraction and transformation MAY occur together.

Where extraction and transformation occur together, the provenance SHOULD preserve enough context to determine what was extracted, what was transformed, whether meaning changed, whether review occurred, whether validation occurred, and whether privacy boundaries apply.

Transformation Provenance is not the same as interpretation.

Interpretation is a meaning, conclusion, classification, summary, judgment, or structured knowledge derived from or associated with source material, evidence, or prior knowledge.

Transformation Provenance explains how that interpretation was produced, what source or prior state was used, who or what produced it, and whether review or validation occurred.

Transformation Provenance SHOULD preserve meaning boundaries.

A transformed output SHOULD remain distinguishable from:

- original Source Material;
- copied Source Material;
- extracted content;
- quoted content;
- summarized content;
- translated content;
- normalized content;
- redacted content;
- classified content;
- interpreted content;
- synthesized knowledge;
- Knowledge Records;
- Source References;
- provenance;
- validation results;
- agent outputs;
- workflow outputs;
- implementation-specific representations.

A Knowledge Record MAY contain transformed content.

When a Knowledge Record contains transformed content, the Knowledge Record SHOULD preserve enough Transformation Provenance to determine what was transformed, what source or prior state was used, whether the transformation changed meaning, whether the transformation was reviewed, whether the transformation was validated, and whether privacy boundaries apply.

Transformation MAY be lossless or lossy.

A lossless transformation preserves meaning, structure, source context, provenance, privacy expectations, relationships, validation expectations, and compatibility expectations sufficiently for the intended use.

A lossy transformation changes, omits, compresses, normalizes, redacts, summarizes, simplifies, restructures, or otherwise reduces meaning, structure, source context, provenance, privacy expectations, relationships, validation expectations, or compatibility expectations.

Where transformation is lossy, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, lifecycle state, compatibility, migration, import, export, governance, publication, or downstream use.

Transformation MAY be reversible or irreversible.

Where a transformation is irreversible, that condition SHOULD be represented or preserved when it affects meaning, validation, authority, privacy, compatibility, migration, import, export, governance, or downstream use.

Transformation MAY be complete or partial.

Partial transformation is allowed.

Partial transformation MUST NOT falsely imply that the transformed output represents the whole Source Material, extracted content, prior knowledge, metadata set, relationship set, validation result, workflow output, agent output, import, export, migration, or governed entity when omitted context affects interpretation.

Transformation MAY be uncertain.

Transformation uncertainty SHOULD be preserved when the source meaning, transformed meaning, classification, interpretation, translation, summarization, normalization, redaction, mapping, migration, import, export, or evidence role is unclear, disputed, incomplete, inferred, low-confidence, restricted, unavailable, or unverifiable.

Transformation MAY be performed by humans.

Human transformation SHOULD preserve attribution, source context, transformation method, review context, validation context, and uncertainty where transformation affects meaning, authority, validation, privacy, publication, governance, or downstream use.

Transformation MAY be performed by agents.

Agent transformation SHOULD preserve agent attribution, instruction context, source context, transformation method, review state, validation state, and uncertainty where agent activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Agent-transformed content MUST NOT be treated as human-reviewed, validated, approved, authoritative, complete, accurate, or publication-ready merely because an agent produced it.

Transformation MAY be performed through workflows.

Workflow transformation SHOULD preserve workflow attribution, workflow state, source context, transformation method, review state, validation state, and approval state where workflow activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Workflow completion MUST NOT be treated as human approval unless a future governed workflow specification explicitly defines that behavior.

Transformation MAY occur during import, export, or migration.

Import Transformation Provenance SHOULD preserve what source or prior representation was transformed during import, what mapping occurred, whether identifiers changed, whether metadata changed, whether relationships changed, whether Source References changed, whether meaning was changed, whether review occurred, and whether compatibility was preserved.

Export Transformation Provenance SHOULD preserve what was transformed for export, what was omitted, what format or representation was produced, whether privacy boundaries affected the export, whether meaning changed, and whether export compatibility was preserved.

Migration Transformation Provenance SHOULD preserve what was transformed during migration, what mapping occurred, whether Object Identity remained stable, whether Source References remained valid, whether provenance remained intact, whether relationships remained meaningful, whether any loss occurred, and whether review or validation occurred.

Transformation MAY affect Object Identity.

A transformation MUST NOT silently change stable Object Identity.

A transformed output SHOULD retain the same Object Identity only when it continues to represent the same Knowledge Object under the applicable identity rules.

A transformed output MAY require a new stable Object Identity when it becomes a meaningfully different Knowledge Object, derived object, split object, merged object, migrated object, superseding object, or separately governed record.

Where transformation affects Object Identity, the identity decision SHOULD preserve enough provenance for future review.

Transformation MAY affect relationships.

A transformation MUST NOT silently discard, reverse, collapse, reinterpret, duplicate, or replace relationships where those relationships affect meaning, provenance, lifecycle state, authority, privacy, validation, compatibility, migration, import, export, governance, or downstream use.

Where transformation changes relationships, the change SHOULD preserve enough provenance to determine what changed, why it changed, who or what changed it, whether review occurred, and whether validation occurred.

Transformation MAY affect metadata.

A transformation MUST NOT silently discard, overwrite, reinterpret, collapse, expose, or regenerate metadata where that metadata affects meaning, Object Identity, provenance, lifecycle state, authority, privacy classification, validation, relationships, compatibility, migration, import, export, governance, workflow behavior, agent behavior, or downstream use.

Where transformation changes metadata, the change SHOULD preserve enough provenance to determine what changed, why it changed, who or what changed it, whether review occurred, and whether validation occurred.

Transformation MUST preserve privacy boundaries.

Transformation MUST NOT expose restricted Source Material, restricted extracted content, restricted attribution, restricted relationships, restricted identifiers, restricted provenance, restricted validation results, restricted source context, restricted metadata, or restricted transformed output merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, or implementation convenience.

Where transformed content is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Where transformation changes privacy risk through aggregation, synthesis, interpretation, redaction, translation, classification, normalization, export, import, migration, or implementation rendering, the stricter applicable privacy expectation SHOULD govern handling unless a future governed privacy specification defines a different compliant rule.

Transformation SHOULD support validation.

A validator SHOULD be able to determine whether:

- transformed content is distinguishable from Source Material;
- transformed content is distinguishable from extracted content;
- transformed content is distinguishable from interpretation where that distinction affects meaning;
- Transformation Provenance is present where required;
- the source or prior state is identified or described where access is permitted;
- the transformation method is clear where method affects interpretation;
- the transformation actor is clear where attribution affects interpretation;
- agent or workflow involvement is identified where required;
- review state is clear where review affects authority or lifecycle state;
- validation state is clear where validation affects downstream use;
- lossy transformation is represented where applicable;
- partial transformation is represented where applicable;
- irreversible transformation is represented where applicable;
- transformation uncertainty is preserved where applicable;
- Object Identity changes are traceable where applicable;
- relationship changes are traceable where applicable;
- metadata changes are traceable where applicable;
- privacy boundaries are preserved;
- Transformation Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Transformation SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, re-transform, or regenerate Transformation Provenance in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, Object Identity confusion, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, transformation confusion, evidence confusion, or source confusion.

Transformation Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what was transformed, what source or prior state was used, what changed, who or what performed the transformation, whether meaning changed, whether transformation was reviewed or validated, whether privacy boundaries apply, whether Object Identity, metadata, relationships, Source References, provenance, validation, migration, import, export, or compatibility were affected, and whether the transformed content remains distinguishable from original Source Material, extracted content, interpretation, and structured knowledge.

## 11. Human-Created Provenance

Human-Created Provenance is provenance created, recorded, reviewed, corrected, approved, rejected, maintained, or otherwise supplied by a human.

Human-Created Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can distinguish human-originated, human-reviewed, human-corrected, human-approved, and human-rejected context from agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated provenance.

Human-Created Provenance SHALL be preserved where human creation, authorship, review, correction, approval, rejection, validation, interpretation, source selection, evidence selection, attribution, extraction, transformation, migration, import, export, or governance affects meaning, authority, privacy, lifecycle state, validation, compatibility, publication, or downstream use.

Human-Created Provenance MAY identify or describe:

- human author;
- human creator;
- human editor;
- human reviewer;
- human approver;
- human rejector;
- human validator;
- human source selector;
- human evidence selector;
- human interpreter;
- human decision-maker;
- human importer;
- human exporter;
- human migrator;
- human archivist;
- human correction activity;
- human review activity;
- human approval activity;
- human rejection activity;
- human validation activity;
- human governance activity;
- human notes where governed;
- other human involvement that affects interpretation.

Human-Created Provenance is not the same as provenance as a whole.

Provenance may be human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, implementation-generated, partial, restricted, uncertain, or historically preserved.

Human-Created Provenance is the subset of provenance associated with human action, judgment, review, authorship, correction, approval, rejection, or responsibility.

Human-Created Provenance is not the same as authorship.

Authorship may be one form of Human-Created Provenance.

A human may create, edit, review, approve, reject, validate, import, export, migrate, classify, interpret, or correct knowledge without being the original author.

Human-Created Provenance SHOULD preserve the human role where role affects meaning, authority, privacy, validation, lifecycle state, governance, publication, or downstream use.

Human-Created Provenance is not the same as approval.

A human may create, edit, comment on, extract, transform, or review knowledge without approving it.

Human approval requires an explicit governed approval action, lifecycle transition, authority assignment, or future governed approval mechanism.

Human-Created Provenance MUST NOT falsely imply approval merely because a human participated.

Human-Created Provenance is not the same as authority.

A human may contribute provenance without making the associated knowledge authoritative.

Authority requires governance weight, review status, approved use, interpretive authority, or another governed authority mechanism.

Human-Created Provenance may support authority, but it does not automatically create authority.

Human-Created Provenance is not the same as truth.

A human-created statement, correction, review, interpretation, extraction, transformation, approval, or rejection does not automatically make knowledge accurate, current, complete, reliable, validated, or authoritative.

Human-Created Provenance identifies human involvement.

Validation, evidence, authority, lifecycle state, and governance determine how the knowledge may be used.

Human-Created Provenance SHOULD distinguish between:

- human-created content;
- human-edited content;
- human-reviewed content;
- human-approved content;
- human-rejected content;
- human-validated content;
- human-corrected content;
- human-selected evidence;
- human-selected Source Material;
- human-created Source References;
- human-created relationships;
- human-created interpretations;
- human-created decisions;
- human-created migration notes;
- human-created import notes;
- human-created export notes;
- human-created governance records.

Human-Created Provenance SHOULD preserve human review context where review affects authority, lifecycle state, privacy, validation, publication, governance, or downstream use.

Human review context MAY include:

- what was reviewed;
- who reviewed it where appropriate and permitted;
- when review occurred where applicable;
- what source material was considered;
- what evidence was considered;
- what issue was reviewed;
- what correction was made;
- what decision was reached;
- whether approval occurred;
- whether rejection occurred;
- whether validation occurred;
- whether further review is required;
- whether privacy boundaries restrict review details.

Human-Created Provenance SHOULD preserve human correction context where correction affects meaning, provenance, evidence, attribution, authority, privacy, lifecycle state, validation, compatibility, governance, or downstream use.

Human correction context MAY include:

- what was corrected;
- what prior state existed;
- what new state replaced it;
- why the correction was made where applicable;
- what source or evidence supported the correction;
- who made the correction where appropriate and permitted;
- whether the correction was reviewed;
- whether the correction was validated;
- whether the correction affects Object Identity, metadata, relationships, Source References, provenance, lifecycle state, authority, privacy, or compatibility.

Human-Created Provenance SHOULD preserve human rejection context where rejection affects lifecycle state, authority, validation, governance, publication, workflow routing, agent output handling, or downstream use.

Human rejection context MAY include:

- what was rejected;
- why it was rejected where applicable;
- who rejected it where appropriate and permitted;
- whether the rejection applies to content, evidence, Source References, provenance, relationships, metadata, agent output, workflow output, import output, export output, migration output, or validation output;
- whether the rejected material must be archived, corrected, superseded, deleted, restricted, or preserved for audit;
- whether privacy boundaries restrict rejection details.

Human-Created Provenance SHOULD preserve distinction from agent-generated provenance.

A human may review, correct, approve, reject, or validate agent-generated provenance.

When this occurs, the provenance SHOULD distinguish the original agent-generated provenance from the later human-created review, correction, approval, rejection, or validation.

Agent-generated provenance MUST NOT be treated as human-created merely because a human later viewed it.

Human-reviewed agent output MUST remain distinguishable from human-authored knowledge where that distinction affects authority, validation, privacy, lifecycle state, governance, publication, or downstream use.

Human-Created Provenance SHOULD preserve distinction from workflow-generated provenance.

A human may participate in a workflow or approve a workflow output.

When this occurs, the provenance SHOULD distinguish human action from workflow activity.

Workflow completion MUST NOT be treated as human approval unless a future governed workflow specification explicitly defines that behavior.

Human-Created Provenance MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, anonymous, pseudonymous, organizational, historically preserved, imported, exported, or migrated.

Where Human-Created Provenance is incomplete, restricted, uncertain, inferred, unavailable, disputed, anonymous, pseudonymous, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, authority, privacy, validation, lifecycle state, compatibility, governance, publication, or downstream use.

Human-Created Provenance MAY be expressed through metadata.

Human-created provenance metadata MAY describe:

- human actor;
- human role;
- human action;
- creation context;
- editing context;
- review context;
- correction context;
- approval context;
- rejection context;
- validation context;
- source-selection context;
- evidence-selection context;
- interpretation context;
- decision context;
- import context;
- export context;
- migration context;
- privacy restriction;
- review state;
- validation state;
- compatibility expectations.

KS-0005 does not define exact Human-Created Provenance metadata fields.

A future specification MAY define exact human-provenance fields, actor identifiers, role vocabularies, review states, approval states, rejection states, validation states, correction records, audit records, import formats, export formats, migration mappings, or serialization syntax.

Human-Created Provenance MUST preserve privacy boundaries.

Human-Created Provenance MUST NOT expose restricted people, restricted attribution, restricted review history, restricted decisions, restricted Source Material, restricted evidence, restricted relationships, restricted identifiers, restricted metadata, restricted workflow context, restricted agent context, restricted validation results, or restricted governance context merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, or implementation convenience.

Where Human-Created Provenance is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Human-Created Provenance SHOULD support validation.

A validator SHOULD be able to determine whether:

- Human-Created Provenance is present where required;
- the human role is clear where role affects interpretation;
- human authorship is distinguishable from human review;
- human review is distinguishable from human approval;
- human approval is distinguishable from authority;
- human correction is distinguishable from original creation;
- human rejection is preserved where required;
- human action is distinguishable from agent-generated provenance;
- human action is distinguishable from workflow-generated provenance;
- human action is distinguishable from imported, exported, migrated, inferred, or implementation-generated provenance;
- privacy boundaries are preserved;
- Human-Created Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Human-Created Provenance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, anonymize, deanonymize, or regenerate Human-Created Provenance in a way that causes loss of meaning, false human attribution, false approval, false rejection, broken Source References, broken provenance, broken relationships, Object Identity confusion, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, human-review confusion, or source confusion.

Human-Created Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what human action occurred, what role the human action served, whether review, correction, approval, rejection, or validation occurred, whether privacy boundaries apply, whether the provenance remains distinguishable from agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated provenance, and whether human-created provenance remains meaningful across time and implementation replacement.

## 12. Agent-Generated Provenance

Agent-Generated Provenance is provenance created, proposed, modified, enriched, validated, extracted, classified, summarized, inferred, routed, transformed, or otherwise affected by an agent.

Agent-Generated Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can distinguish agent-originated, agent-proposed, agent-modified, agent-inferred, and agent-enriched provenance from human-created, human-reviewed, workflow-generated, imported, exported, migrated, inferred, or implementation-generated provenance.

Agent-Generated Provenance SHALL be preserved where agent activity affects meaning, evidence, attribution, authority, privacy, lifecycle state, validation, compatibility, publication, workflow behavior, governance, migration, import, export, or downstream use.

Agent-Generated Provenance MAY identify or describe:

- agent identity where governed and permitted;
- agent role;
- agent action;
- agent instruction context;
- agent input context;
- agent output context;
- agent confidence where applicable;
- agent uncertainty;
- agent source selection;
- agent evidence selection;
- agent extraction activity;
- agent transformation activity;
- agent summarization activity;
- agent classification activity;
- agent relationship proposal;
- agent Source Reference proposal;
- agent metadata proposal;
- agent validation activity;
- agent review recommendation;
- agent routing activity;
- agent import activity;
- agent export activity;
- agent migration activity;
- agent limitation;
- other agent involvement that affects interpretation.

Agent-Generated Provenance is not the same as provenance as a whole.

Provenance may be human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, implementation-generated, partial, restricted, uncertain, or historically preserved.

Agent-Generated Provenance is the subset of provenance associated with agent activity, agent output, agent inference, agent recommendation, agent transformation, agent validation, agent classification, agent enrichment, or agent-proposed action.

Agent-Generated Provenance is not the same as human-created provenance.

A human may review, correct, approve, reject, or validate agent-generated provenance.

When this occurs, the provenance SHOULD distinguish the original agent-generated provenance from the later human-created review, correction, approval, rejection, or validation.

Agent-Generated Provenance MUST NOT be treated as human-created merely because a human viewed it, accepted it into a workflow, or stored it in a compliant repository.

Agent-Generated Provenance is not the same as human review.

An agent may inspect, classify, summarize, validate, compare, enrich, or recommend knowledge without creating human review.

Human review requires explicit human action or a future governed review mechanism.

Agent-Generated Provenance MUST NOT falsely imply human review.

Agent-Generated Provenance is not the same as approval.

An agent may propose, classify, validate, enrich, or recommend knowledge without approving it.

Approval requires an explicit governed approval action, lifecycle transition, authority assignment, human approval, workflow approval rule, or future governed approval mechanism.

Agent-Generated Provenance MUST NOT falsely imply approval merely because an agent generated, validated, ranked, summarized, or recommended the content.

Agent-Generated Provenance is not the same as authority.

An agent may support authority assessment, but agent activity alone does not make knowledge authoritative.

Authority requires governance weight, review status, approved use, interpretive authority, or another governed authority mechanism.

Agent-Generated Provenance may support authority, but it does not automatically create authority.

Agent-Generated Provenance is not the same as truth.

Agent-generated content, classification, extraction, transformation, validation, recommendation, or provenance does not automatically make knowledge accurate, current, complete, reliable, reviewed, approved, validated, or authoritative.

Agent-Generated Provenance identifies agent involvement.

Validation, evidence, authority, lifecycle state, human review, workflow rules, and governance determine how the knowledge may be used.

Agent-Generated Provenance SHOULD distinguish between:

- agent-created content;
- agent-modified content;
- agent-proposed content;
- agent-extracted content;
- agent-transformed content;
- agent-summarized content;
- agent-classified content;
- agent-inferred provenance;
- agent-selected evidence;
- agent-selected Source Material;
- agent-created Source References;
- agent-proposed relationships;
- agent-created metadata;
- agent validation output;
- agent review recommendation;
- agent routing recommendation;
- agent migration output;
- agent import output;
- agent export output.

Agent-Generated Provenance SHOULD preserve agent instruction context where instruction context affects interpretation, authority, privacy, validation, reproducibility, governance, publication, or downstream use.

Agent instruction context MAY include:

- user instruction;
- system instruction where permitted;
- workflow instruction;
- validation instruction;
- extraction instruction;
- transformation instruction;
- classification instruction;
- privacy instruction;
- source-selection instruction;
- evidence-selection instruction;
- migration instruction;
- import instruction;
- export instruction;
- constraints applied to the agent;
- limitations known at the time of agent activity.

Agent-Generated Provenance SHOULD preserve agent input context where input context affects meaning, validation, privacy, authority, compatibility, governance, or downstream use.

Agent input context MAY include:

- Source Material used;
- Source References used;
- Knowledge Records used;
- metadata used;
- relationships used;
- validation results used;
- workflow state used;
- user-provided context;
- imported context;
- migrated context;
- restricted context where permitted;
- unavailable or partial context;
- omitted context where omission affects interpretation.

Agent-Generated Provenance SHOULD preserve agent output context where output context affects meaning, validation, privacy, authority, compatibility, governance, or downstream use.

Agent output context MAY include:

- generated text;
- proposed metadata;
- proposed Source References;
- proposed relationships;
- extracted content;
- transformed content;
- summaries;
- classifications;
- validations;
- confidence notes where applicable;
- uncertainty notes;
- limitations;
- rejected output where preservation is required;
- human review state;
- workflow state;
- approval state.

Agent-Generated Provenance SHOULD preserve uncertainty where agent uncertainty affects interpretation, validation, authority, privacy, lifecycle state, governance, publication, or downstream use.

Agent uncertainty MAY include:

- low confidence;
- incomplete source context;
- conflicting evidence;
- ambiguous extraction;
- uncertain attribution;
- uncertain classification;
- uncertain relationship;
- uncertain transformation;
- uncertain validation result;
- restricted source context;
- missing Source Material;
- unverifiable source support;
- implementation limitation.

Agent-Generated Provenance SHOULD preserve distinction from workflow-generated provenance.

An agent may operate inside a workflow.

When this occurs, provenance SHOULD distinguish agent action from workflow routing, workflow state, workflow completion, workflow approval, workflow rejection, workflow validation, or workflow governance behavior.

Workflow completion MUST NOT be treated as agent validation unless a future governed workflow specification explicitly defines that behavior.

Agent validation MUST NOT be treated as workflow approval unless a future governed workflow specification explicitly defines that behavior.

Agent-Generated Provenance MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, implementation-generated, historically preserved, imported, exported, or migrated.

Where Agent-Generated Provenance is incomplete, restricted, uncertain, inferred, unavailable, disputed, implementation-generated, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, authority, privacy, validation, lifecycle state, compatibility, governance, publication, or downstream use.

Agent-Generated Provenance MAY be expressed through metadata.

Agent-generated provenance metadata MAY describe:

- agent identifier where governed and permitted;
- agent role;
- agent action;
- agent input context;
- agent output context;
- instruction context;
- source-selection context;
- evidence-selection context;
- extraction context;
- transformation context;
- summarization context;
- classification context;
- validation context;
- relationship-proposal context;
- Source Reference proposal context;
- uncertainty;
- limitation;
- review state;
- validation state;
- approval state;
- workflow context;
- import context;
- export context;
- migration context;
- privacy restriction;
- compatibility expectations.

KS-0005 does not define exact Agent-Generated Provenance metadata fields.

A future specification MAY define exact agent-provenance fields, agent identifiers, model identifiers, role vocabularies, confidence values, uncertainty values, instruction records, input records, output records, review states, validation states, approval states, rejection states, audit records, import formats, export formats, migration mappings, or serialization syntax.

Agent-Generated Provenance MUST preserve privacy boundaries.

Agent-Generated Provenance MUST NOT expose restricted Source Material, restricted evidence, restricted attribution, restricted relationships, restricted identifiers, restricted metadata, restricted human review history, restricted workflow context, restricted validation results, restricted agent instructions, restricted source context, or restricted governance context merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, or implementation convenience.

Where Agent-Generated Provenance is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

An agent MUST NOT access, summarize, extract, transform, validate, classify, embed, index, route, export, publish, or otherwise process restricted Source Material or restricted provenance unless permitted by the applicable privacy classification, governance rule, workflow rule, or future governed specification.

Agent-Generated Provenance SHOULD support validation.

A validator SHOULD be able to determine whether:

- Agent-Generated Provenance is present where required;
- agent involvement is identified where required;
- the agent role is clear where role affects interpretation;
- agent-generated output is distinguishable from human-created output;
- agent-generated output is distinguishable from human-reviewed output;
- agent-generated output is distinguishable from workflow-generated output;
- agent validation is distinguishable from approval;
- agent recommendation is distinguishable from authority;
- agent uncertainty is preserved where applicable;
- agent instruction context is preserved where required;
- agent input context is preserved where required;
- agent output context is preserved where required;
- privacy boundaries are preserved;
- Agent-Generated Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Agent-Generated Provenance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, anonymize, deanonymize, or regenerate Agent-Generated Provenance in a way that causes loss of meaning, false human attribution, false human review, false approval, false authority, broken Source References, broken provenance, broken relationships, Object Identity confusion, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, agent-review confusion, or source confusion.

Agent-Generated Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what agent action occurred, what role the agent action served, what source or context was used, whether extraction, transformation, classification, validation, recommendation, or inference occurred, whether human review, approval, rejection, or correction occurred later, whether privacy boundaries apply, whether the provenance remains distinguishable from human-created, workflow-generated, imported, exported, migrated, inferred, or implementation-generated provenance, and whether agent-generated provenance remains meaningful across time and implementation replacement.

## 13. Workflow-Generated Provenance

Workflow-Generated Provenance is provenance created, proposed, modified, enriched, validated, extracted, classified, summarized, routed, approved, rejected, preserved, imported, exported, migrated, archived, superseded, or otherwise affected through a governed workflow.

Workflow-Generated Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can distinguish workflow-created, workflow-routed, workflow-validated, workflow-approved, workflow-rejected, workflow-preserved, and workflow-generated context from human-created, agent-generated, imported, exported, migrated, inferred, or implementation-generated provenance.

Workflow-Generated Provenance SHALL be preserved where workflow activity affects meaning, evidence, attribution, authority, privacy, lifecycle state, validation, compatibility, publication, governance, migration, import, export, or downstream use.

Workflow-Generated Provenance MAY identify or describe:

- workflow identity where governed and permitted;
- workflow role;
- workflow step;
- workflow state;
- workflow action;
- workflow instruction context;
- workflow input context;
- workflow output context;
- workflow routing activity;
- workflow review activity;
- workflow validation activity;
- workflow approval activity;
- workflow rejection activity;
- workflow correction activity;
- workflow preservation activity;
- workflow archival activity;
- workflow supersession activity;
- workflow import activity;
- workflow export activity;
- workflow migration activity;
- workflow limitation;
- human participation in the workflow where permitted;
- agent participation in the workflow where permitted;
- other workflow involvement that affects interpretation.

Workflow-Generated Provenance is not the same as provenance as a whole.

Provenance may be human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, implementation-generated, partial, restricted, uncertain, or historically preserved.

Workflow-Generated Provenance is the subset of provenance associated with workflow activity, workflow routing, workflow state, workflow decisions, workflow validation, workflow preservation, workflow approval, workflow rejection, workflow import, workflow export, workflow migration, or workflow-governed action.

Workflow-Generated Provenance is not the same as human-created provenance.

A human may participate in a workflow.

When this occurs, provenance SHOULD distinguish the human action from the workflow action.

Workflow-Generated Provenance MUST NOT be treated as human-created merely because a human participated in the workflow, viewed the workflow output, or allowed the workflow to continue.

Workflow-Generated Provenance is not the same as agent-generated provenance.

An agent may operate inside a workflow.

When this occurs, provenance SHOULD distinguish agent action from workflow routing, workflow state, workflow completion, workflow validation, workflow approval, workflow rejection, workflow import, workflow export, workflow migration, or workflow governance behavior.

Workflow-Generated Provenance MUST NOT be treated as agent-generated merely because an agent participated in one workflow step.

Agent-generated provenance MUST NOT be treated as workflow approval unless a future governed workflow specification explicitly defines that behavior.

Workflow-Generated Provenance is not the same as approval.

A workflow may route, classify, validate, reject, archive, import, export, migrate, or complete without approving knowledge.

Approval requires an explicit governed approval action, lifecycle transition, authority assignment, human approval, workflow approval rule, or future governed approval mechanism.

Workflow completion MUST NOT be treated as approval unless a future governed workflow specification explicitly defines that behavior.

Workflow-Generated Provenance MUST NOT falsely imply approval merely because a workflow completed, advanced, validated, routed, stored, exported, imported, or migrated the content.

Workflow-Generated Provenance is not the same as authority.

A workflow may support authority assessment, review, validation, publication, routing, or lifecycle state.

Workflow activity alone does not make knowledge authoritative unless a governed authority rule, approval rule, lifecycle rule, or future workflow specification explicitly defines that behavior.

Workflow-Generated Provenance may support authority, but it does not automatically create authority.

Workflow-Generated Provenance is not the same as truth.

Workflow-generated validation, routing, classification, approval, rejection, preservation, migration, import, export, or provenance does not automatically make knowledge accurate, current, complete, reliable, reviewed, approved, validated, authoritative, or publication-ready.

Workflow-Generated Provenance identifies workflow involvement.

Validation, evidence, authority, lifecycle state, human review, agent review, workflow rules, and governance determine how the knowledge may be used.

Workflow-Generated Provenance SHOULD distinguish between:

- workflow-created content;
- workflow-modified content;
- workflow-routed content;
- workflow-reviewed content;
- workflow-approved content;
- workflow-rejected content;
- workflow-validated content;
- workflow-corrected content;
- workflow-archived content;
- workflow-superseded content;
- workflow-selected Source Material;
- workflow-selected evidence;
- workflow-created Source References;
- workflow-created relationships;
- workflow-created metadata;
- workflow validation output;
- workflow routing output;
- workflow migration output;
- workflow import output;
- workflow export output.

Workflow-Generated Provenance SHOULD preserve workflow state where workflow state affects interpretation, authority, privacy, validation, lifecycle state, governance, publication, migration, import, export, or downstream use.

Workflow state MAY include:

- not started;
- pending;
- in progress;
- blocked;
- routed;
- waiting for review;
- waiting for validation;
- waiting for approval;
- approved;
- rejected;
- returned for correction;
- superseded;
- archived;
- imported;
- exported;
- migrated;
- completed;
- failed;
- deferred;
- cancelled;
- other governed workflow states.

KS-0005 does not define an exhaustive controlled vocabulary for workflow states.

A future workflow specification MAY define exact workflow states, state-transition rules, approval rules, rejection rules, routing rules, validation rules, lifecycle mappings, import rules, export rules, migration rules, audit records, or serialization syntax.

Workflow-Generated Provenance SHOULD preserve workflow instruction context where instruction context affects interpretation, authority, privacy, validation, reproducibility, governance, publication, or downstream use.

Workflow instruction context MAY include:

- workflow purpose;
- workflow rule;
- workflow trigger;
- workflow constraint;
- validation instruction;
- review instruction;
- approval instruction;
- rejection instruction;
- routing instruction;
- extraction instruction;
- transformation instruction;
- classification instruction;
- privacy instruction;
- migration instruction;
- import instruction;
- export instruction;
- constraints applied to the workflow;
- limitations known at the time of workflow activity.

Workflow-Generated Provenance SHOULD preserve workflow input context where input context affects meaning, validation, privacy, authority, compatibility, governance, migration, import, export, or downstream use.

Workflow input context MAY include:

- Source Material used;
- Source References used;
- Knowledge Records used;
- metadata used;
- relationships used;
- validation results used;
- human input used;
- agent input used;
- imported context;
- migrated context;
- restricted context where permitted;
- unavailable or partial context;
- omitted context where omission affects interpretation.

Workflow-Generated Provenance SHOULD preserve workflow output context where output context affects meaning, validation, privacy, authority, lifecycle state, compatibility, governance, migration, import, export, or downstream use.

Workflow output context MAY include:

- routed content;
- generated records;
- proposed metadata;
- proposed Source References;
- proposed relationships;
- extracted content;
- transformed content;
- validation results;
- review results;
- approval results;
- rejection results;
- lifecycle transitions;
- import outputs;
- export outputs;
- migration outputs;
- archive outputs;
- supersession outputs;
- error states;
- limitation notes;
- human review state;
- agent review state;
- approval state.

Workflow-Generated Provenance SHOULD preserve workflow routing context where routing affects reviewability, authority, privacy, validation, lifecycle state, governance, publication, or downstream use.

Workflow routing context MAY include:

- what was routed;
- where it was routed;
- why it was routed where applicable;
- who or what routed it;
- whether routing was human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated;
- whether routing exposed or restricted access;
- whether routing changed lifecycle state;
- whether routing requires review, validation, approval, rejection, correction, archival, or escalation.

Workflow-Generated Provenance SHOULD preserve workflow validation context where validation affects authority, privacy, lifecycle state, governance, publication, migration, import, export, compatibility, or downstream use.

Workflow validation context MAY include:

- what was checked;
- what rule or expectation applied;
- what source or evidence was used;
- who or what performed the validation;
- whether an agent participated;
- whether a human participated;
- whether validation passed;
- whether validation failed;
- whether validation partially passed;
- whether validation was blocked;
- whether validation was deferred;
- whether validation affected lifecycle state, authority, privacy, compatibility, migration, import, export, or governance.

Workflow-Generated Provenance MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, implementation-generated, historically preserved, imported, exported, or migrated.

Where Workflow-Generated Provenance is incomplete, restricted, uncertain, inferred, unavailable, disputed, implementation-generated, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, authority, privacy, validation, lifecycle state, compatibility, governance, publication, or downstream use.

Workflow-Generated Provenance MAY be expressed through metadata.

Workflow-generated provenance metadata MAY describe:

- workflow identifier where governed and permitted;
- workflow role;
- workflow action;
- workflow state;
- workflow step;
- workflow trigger;
- workflow input context;
- workflow output context;
- instruction context;
- routing context;
- review context;
- validation context;
- approval context;
- rejection context;
- correction context;
- archival context;
- supersession context;
- import context;
- export context;
- migration context;
- human participation;
- agent participation;
- uncertainty;
- limitation;
- privacy restriction;
- compatibility expectations.

KS-0005 does not define exact Workflow-Generated Provenance metadata fields.

A future specification MAY define exact workflow-provenance fields, workflow identifiers, workflow-state values, role vocabularies, approval values, rejection values, routing values, validation values, workflow audit records, import formats, export formats, migration mappings, or serialization syntax.

Workflow-Generated Provenance MUST preserve privacy boundaries.

Workflow-Generated Provenance MUST NOT expose restricted Source Material, restricted evidence, restricted attribution, restricted relationships, restricted identifiers, restricted metadata, restricted human review history, restricted agent context, restricted workflow context, restricted validation results, restricted source context, or restricted governance context merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, or implementation convenience.

Where Workflow-Generated Provenance is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A workflow MUST NOT access, summarize, extract, transform, validate, classify, embed, index, route, export, publish, synchronize, or otherwise process restricted Source Material or restricted provenance unless permitted by the applicable privacy classification, governance rule, workflow rule, or future governed specification.

Workflow-Generated Provenance SHOULD support validation.

A validator SHOULD be able to determine whether:

- Workflow-Generated Provenance is present where required;
- workflow involvement is identified where required;
- the workflow role is clear where role affects interpretation;
- workflow state is clear where state affects interpretation;
- workflow-generated output is distinguishable from human-created output;
- workflow-generated output is distinguishable from agent-generated output;
- workflow completion is distinguishable from approval;
- workflow validation is distinguishable from approval;
- workflow routing is distinguishable from authority;
- workflow rejection is preserved where required;
- workflow instruction context is preserved where required;
- workflow input context is preserved where required;
- workflow output context is preserved where required;
- privacy boundaries are preserved;
- Workflow-Generated Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Workflow-Generated Provenance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, anonymize, deanonymize, or regenerate Workflow-Generated Provenance in a way that causes loss of meaning, false human attribution, false human review, false agent attribution, false approval, false authority, broken Source References, broken provenance, broken relationships, Object Identity confusion, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, governance drift, implementation lock-in, workflow-review confusion, or source confusion.

Workflow-Generated Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what workflow action occurred, what workflow role applied, what workflow state existed, what source or context was used, whether routing, review, validation, approval, rejection, correction, preservation, import, export, or migration occurred, whether human or agent participation occurred, whether privacy boundaries apply, whether the provenance remains distinguishable from human-created, agent-generated, imported, exported, migrated, inferred, or implementation-generated provenance, and whether workflow-generated provenance remains meaningful across time and implementation replacement.


## 14. Import Provenance

Import Provenance is provenance associated with bringing Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, attribution, validation results, external references, identifiers, workflow outputs, agent outputs, or other governed entities into a compliant environment.

Import Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what was imported, where it came from, what source or prior system was used, what changed during import, what mapping occurred, whether meaning changed, whether review occurred, whether validation occurred, and whether privacy boundaries apply.

Import Provenance SHALL be preserved where import activity affects meaning, Object Identity, Source References, provenance, evidence, attribution, metadata, relationships, authority, privacy, lifecycle state, validation, compatibility, governance, publication, export, migration, or downstream use.

Import Provenance MAY identify or describe:

- import source;
- import actor;
- import process;
- import tool;
- import workflow;
- import agent;
- import date where applicable;
- imported Source Material;
- imported Knowledge Objects;
- imported Knowledge Records;
- imported Source References;
- imported metadata;
- imported relationships;
- imported identifiers;
- imported evidence;
- imported attribution;
- imported validation results;
- imported lifecycle state;
- imported authority context;
- imported privacy context;
- imported compatibility context;
- mapping activity;
- transformation activity;
- extraction activity;
- validation activity;
- review activity;
- omitted content;
- restricted content;
- failed import items;
- partial import items;
- uncertain import items;
- other import context that affects interpretation.

Import Provenance is not the same as provenance as a whole.

Provenance may describe creation, source use, extraction, transformation, review, validation, agent activity, workflow activity, import, export, migration, or other change history.

Import Provenance is the subset of provenance associated with bringing governed or source material into a compliant environment.

Import Provenance is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, contradiction, or support.

Import Provenance explains how Source Material or source-derived knowledge entered a compliant environment and what import context affects interpretation.

Import Provenance is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

Import Provenance explains whether the Source Reference was imported, created during import, mapped during import, validated during import, changed during import, or preserved from a prior environment.

Import Provenance is not the same as Transformation Provenance.

Import may include transformation.

When import includes transformation, Import Provenance SHOULD preserve enough context to determine what was imported, what was transformed, what mapping occurred, whether meaning changed, whether review occurred, and whether validation occurred.

Transformation Provenance SHOULD preserve the transformation-specific context.

Import Provenance is not the same as Migration Provenance.

Import Provenance concerns bringing material into a compliant environment.

Migration Provenance concerns moving, converting, mapping, preserving, transforming, validating, or reviewing governed entities across systems, formats, repositories, vaults, implementations, standards versions, or storage environments.

Import and migration MAY occur together.

Where import and migration occur together, provenance SHOULD preserve enough context to distinguish import behavior from migration behavior.

Import Provenance SHOULD preserve source context where source context affects interpretation, authority, privacy, validation, compatibility, governance, publication, export, migration, or downstream use.

Source context MAY include:

- source system;
- source repository;
- source archive;
- source file;
- source record;
- source format;
- source version;
- source date;
- source creator;
- source publisher;
- source owner where applicable;
- source identifier;
- legacy identifier;
- external identifier;
- citation;
- URL;
- archive reference;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source access conditions;
- source limitations;
- source licensing or rights context where applicable;
- source validation state;
- source compatibility expectations.

Import Provenance SHOULD preserve mapping context where mapping affects meaning, Object Identity, Source References, metadata, relationships, authority, privacy, validation, compatibility, migration, export, governance, or downstream use.

Mapping context MAY include:

- source identifier to stable Object Identity mapping;
- legacy identifier to stable Object Identity mapping;
- external identifier to Source Identifier mapping;
- source field to metadata field mapping;
- source relationship to governed relationship mapping;
- source reference to Source Reference mapping;
- source lifecycle state to governed lifecycle state mapping;
- source authority value to governed authority context mapping;
- source privacy value to governed privacy context mapping;
- source validation value to governed validation context mapping;
- source format to compliant representation mapping;
- unmapped source content;
- uncertain mapping;
- rejected mapping;
- deferred mapping;
- mapping requiring human review.

Import MUST preserve Object Identity boundaries.

An import process MUST NOT silently create, replace, merge, split, redirect, overwrite, or reinterpret stable Object Identity.

Where imported material corresponds to an existing Knowledge Object, the import process SHOULD preserve enough provenance to determine how the match was made and whether review or validation occurred.

Where imported material becomes a new Knowledge Object, the import process SHOULD preserve enough provenance to determine why a new Object Identity was created.

Where imported material cannot be safely matched to an existing Knowledge Object, the import process SHOULD preserve uncertainty rather than silently assigning identity.

Import MUST preserve Source Reference boundaries.

An imported citation, URL, file path, database reference, external reference, archive reference, source identifier, or implementation-specific link MUST NOT automatically become a complete Source Reference unless it satisfies Source Reference requirements or a future governed specification defines compliant conversion behavior.

Where Source References are imported, Import Provenance SHOULD preserve whether the reference was preserved as-is, mapped, normalized, transformed, validated, rejected, or marked uncertain.

Import MUST preserve metadata boundaries.

Imported metadata MUST NOT silently redefine Object Identity, relationship meaning, lifecycle state, authority level, privacy classification, validation status, Source References, provenance, workflow state, agent state, or implementation behavior.

Where metadata is imported, Import Provenance SHOULD preserve what metadata was imported, what mapping occurred, what was omitted, what was transformed, and whether review or validation occurred.

Import MUST preserve relationship boundaries.

Imported relationships MUST NOT silently redefine relationship type, direction, participants, strength, confidence, authority, privacy, validation, lifecycle state, or provenance.

Where relationships are imported, Import Provenance SHOULD preserve what relationship was imported, what participants were identified, what mapping occurred, whether Object Identity was used, whether the relationship was reviewed, and whether validation occurred.

Import MAY be complete or partial.

Partial import is allowed.

Partial import MUST NOT falsely imply that the imported material represents the whole source system, source file, source record, source archive, Source Material, Knowledge Object, Knowledge Record, metadata set, relationship set, evidence set, or governed entity when omitted context affects interpretation.

Import MAY be lossy.

Lossy import occurs when content, metadata, Source References, relationships, provenance, identifiers, formatting, structure, validation context, privacy context, authority context, lifecycle state, compatibility expectations, or source context is changed, omitted, compressed, normalized, redacted, summarized, mapped, or otherwise reduced during import.

Where import is lossy, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, lifecycle state, compatibility, migration, export, governance, publication, or downstream use.

Import MAY be uncertain.

Import uncertainty SHOULD be preserved when source meaning, source identity, object identity matching, metadata mapping, relationship mapping, Source Reference mapping, attribution, extraction, transformation, validation, privacy handling, authority handling, or compatibility is unclear, disputed, incomplete, inferred, low-confidence, restricted, unavailable, or unverifiable.

Import MAY be performed by humans.

Human import SHOULD preserve attribution, source context, mapping context, review context, validation context, and uncertainty where import affects meaning, authority, validation, privacy, publication, governance, or downstream use.

Import MAY be performed by agents.

Agent import SHOULD preserve agent attribution, instruction context, source context, mapping context, import method, review state, validation state, and uncertainty where agent activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Agent-imported content MUST NOT be treated as human-reviewed, validated, approved, authoritative, complete, accurate, or publication-ready merely because an agent imported it.

Import MAY be performed through workflows.

Workflow import SHOULD preserve workflow attribution, workflow state, source context, mapping context, import method, review state, validation state, and approval state where workflow activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Workflow completion MUST NOT be treated as human approval unless a future governed workflow specification explicitly defines that behavior.

Import MUST preserve privacy boundaries.

Import MUST NOT expose restricted Source Material, restricted evidence, restricted attribution, restricted relationships, restricted identifiers, restricted metadata, restricted provenance, restricted validation results, restricted source context, restricted workflow context, restricted agent context, or restricted imported output merely to improve traceability, review, validation, search, linking, indexing, publication, migration, export, automation, or implementation convenience.

Where imported content is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Where import changes privacy risk through aggregation, synthesis, interpretation, redaction, normalization, mapping, workflow routing, agent processing, storage, indexing, or implementation rendering, the stricter applicable privacy expectation SHOULD govern handling unless a future governed privacy specification defines a different compliant rule.

Import SHOULD support validation.

A validator SHOULD be able to determine whether:

- Import Provenance is present where required;
- imported material is distinguishable from existing governed material;
- imported Source Material is distinguishable from Knowledge Records;
- imported Source References are valid or marked uncertain where applicable;
- imported metadata remains within metadata role boundaries;
- imported relationships remain within relationship boundaries;
- imported identifiers do not silently redefine stable Object Identity;
- source context is preserved where required;
- mapping context is preserved where required;
- partial import is represented where applicable;
- lossy import is represented where applicable;
- import uncertainty is preserved where applicable;
- human, agent, and workflow involvement are distinguishable where applicable;
- privacy boundaries are preserved;
- Import Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Import SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, or normalize Import Provenance in a way that causes loss of meaning, broken Object Identity, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, migration loss, export ambiguity, governance drift, implementation lock-in, import confusion, or source confusion.

Import Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what was imported, where it came from, what mapping occurred, what changed, what was omitted, who or what performed the import, whether human, agent, or workflow involvement occurred, whether review or validation occurred, whether privacy boundaries apply, whether imported material remains distinguishable from existing governed material, and whether import provenance remains meaningful across time and implementation replacement.

## 15. Export Provenance

Export Provenance is provenance associated with producing, copying, packaging, converting, transmitting, publishing, synchronizing, archiving, rendering, or otherwise making Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, attribution, validation results, external references, identifiers, workflow outputs, agent outputs, or other governed entities from a compliant environment for use elsewhere.

Export Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what was exported, where it was exported from, where it was exported to where applicable, what changed during export, what was omitted, what mapping occurred, whether meaning changed, whether review occurred, whether validation occurred, and whether privacy boundaries apply.

Export Provenance SHALL be preserved where export activity affects meaning, Object Identity, Source References, provenance, evidence, attribution, metadata, relationships, authority, privacy, lifecycle state, validation, compatibility, governance, publication, import, migration, or downstream use.

Export Provenance MAY identify or describe:

- export source;
- export destination where applicable and permitted;
- export actor;
- export process;
- export tool;
- export workflow;
- export agent;
- export date where applicable;
- exported Source Material;
- exported Knowledge Objects;
- exported Knowledge Records;
- exported Source References;
- exported metadata;
- exported relationships;
- exported identifiers;
- exported evidence;
- exported attribution;
- exported validation results;
- exported lifecycle state;
- exported authority context;
- exported privacy context;
- exported compatibility context;
- mapping activity;
- transformation activity;
- extraction activity;
- validation activity;
- review activity;
- omitted content;
- restricted content;
- redacted content;
- failed export items;
- partial export items;
- uncertain export items;
- other export context that affects interpretation.

Export Provenance is not the same as provenance as a whole.

Provenance may describe creation, source use, extraction, transformation, review, validation, agent activity, workflow activity, import, export, migration, or other change history.

Export Provenance is the subset of provenance associated with producing governed or source material from a compliant environment for use elsewhere.

Export Provenance is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, contradiction, or support.

Export Provenance explains how Source Material or source-derived knowledge left, was copied from, was packaged from, was rendered from, or was otherwise produced from a compliant environment.

Export Provenance is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

Export Provenance explains whether the Source Reference was exported, omitted, redacted, mapped, normalized, transformed, validated, rejected, or marked uncertain during export.

Export Provenance is not the same as Transformation Provenance.

Export may include transformation.

When export includes transformation, Export Provenance SHOULD preserve enough context to determine what was exported, what was transformed, what mapping occurred, what was omitted, whether meaning changed, whether review occurred, and whether validation occurred.

Transformation Provenance SHOULD preserve the transformation-specific context.

Export Provenance is not the same as Migration Provenance.

Export Provenance concerns producing governed or source material from a compliant environment for use elsewhere.

Migration Provenance concerns moving, converting, mapping, preserving, transforming, validating, or reviewing governed entities across systems, formats, repositories, vaults, implementations, standards versions, or storage environments.

Export and migration MAY occur together.

Where export and migration occur together, provenance SHOULD preserve enough context to distinguish export behavior from migration behavior.

Export Provenance SHOULD preserve source context where source context affects interpretation, authority, privacy, validation, compatibility, governance, publication, import, migration, or downstream use.

Source context MAY include:

- source environment;
- source repository;
- source archive;
- source file;
- source record;
- source format;
- source version;
- source date;
- source creator;
- source publisher;
- source owner where applicable;
- source identifier;
- stable Object Identity where applicable;
- Source Identifier where applicable;
- legacy identifier;
- external identifier;
- citation;
- URL;
- archive reference;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source access conditions;
- source limitations;
- source licensing or rights context where applicable;
- source validation state;
- source compatibility expectations.

Export Provenance SHOULD preserve destination context where destination context affects interpretation, authority, privacy, validation, compatibility, governance, publication, re-import, migration, or downstream use.

Destination context MAY include:

- destination system;
- destination repository;
- destination archive;
- destination format;
- destination version;
- destination access expectation;
- destination privacy expectation;
- destination compatibility expectation;
- destination validation expectation;
- publication context;
- synchronization context;
- external-use context;
- re-import expectation;
- export limitation.

Export Provenance SHOULD preserve mapping context where mapping affects meaning, Object Identity, Source References, metadata, relationships, authority, privacy, validation, compatibility, import, migration, governance, or downstream use.

Mapping context MAY include:

- stable Object Identity to exported identifier mapping;
- Source Identifier to exported source identifier mapping;
- metadata field to exported field mapping;
- governed relationship to exported relationship mapping;
- Source Reference to exported reference mapping;
- lifecycle state to exported lifecycle representation mapping;
- authority context to exported authority representation mapping;
- privacy classification to exported privacy representation mapping;
- validation context to exported validation representation mapping;
- compliant representation to export format mapping;
- unmapped governed content;
- omitted governed content;
- redacted governed content;
- uncertain mapping;
- rejected mapping;
- deferred mapping;
- mapping requiring human review.

Export MUST preserve Object Identity boundaries.

An export process MUST NOT silently create, replace, merge, split, redirect, overwrite, or reinterpret stable Object Identity.

Where exported material corresponds to a Knowledge Object, the export process SHOULD preserve enough provenance to determine what Object Identity was exported, how it was represented, whether any exported identifier differs from stable Object Identity, and whether review or validation occurred.

Where export cannot safely preserve Object Identity, the export process SHOULD preserve that limitation rather than silently substituting filenames, titles, URLs, database rows, application identifiers, or implementation-specific identifiers as stable Object Identity.

Export MUST preserve Source Reference boundaries.

An exported citation, URL, file path, database reference, external reference, archive reference, source identifier, or implementation-specific link MUST NOT automatically replace a complete Source Reference unless it satisfies Source Reference requirements or a future governed specification defines compliant conversion behavior.

Where Source References are exported, Export Provenance SHOULD preserve whether the reference was preserved as-is, mapped, normalized, transformed, redacted, omitted, validated, rejected, or marked uncertain.

Export MUST preserve metadata boundaries.

Exported metadata MUST NOT silently redefine Object Identity, relationship meaning, lifecycle state, authority level, privacy classification, validation status, Source References, provenance, workflow state, agent state, or implementation behavior.

Where metadata is exported, Export Provenance SHOULD preserve what metadata was exported, what mapping occurred, what was omitted, what was transformed, what was redacted, and whether review or validation occurred.

Export MUST preserve relationship boundaries.

Exported relationships MUST NOT silently redefine relationship type, direction, participants, strength, confidence, authority, privacy, validation, lifecycle state, or provenance.

Where relationships are exported, Export Provenance SHOULD preserve what relationship was exported, what participants were identified, what mapping occurred, whether Object Identity was used, whether the relationship was reviewed, and whether validation occurred.

Export MAY be complete or partial.

Partial export is allowed.

Partial export MUST NOT falsely imply that the exported material represents the whole compliant environment, source repository, Source Material, Knowledge Object, Knowledge Record, metadata set, relationship set, evidence set, provenance set, validation set, workflow output, agent output, or governed entity when omitted context affects interpretation.

Export MAY be lossy.

Lossy export occurs when content, metadata, Source References, relationships, provenance, identifiers, formatting, structure, validation context, privacy context, authority context, lifecycle state, compatibility expectations, or source context is changed, omitted, compressed, normalized, redacted, summarized, mapped, rendered, packaged, or otherwise reduced during export.

Where export is lossy, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, lifecycle state, compatibility, import, migration, governance, publication, or downstream use.

Export MAY be uncertain.

Export uncertainty SHOULD be preserved when source meaning, object identity representation, metadata mapping, relationship mapping, Source Reference mapping, attribution, extraction, transformation, validation, privacy handling, authority handling, destination behavior, publication behavior, or compatibility is unclear, disputed, incomplete, inferred, low-confidence, restricted, unavailable, or unverifiable.

Export MAY be performed by humans.

Human export SHOULD preserve attribution, source context, destination context, mapping context, review context, validation context, and uncertainty where export affects meaning, authority, validation, privacy, publication, governance, or downstream use.

Export MAY be performed by agents.

Agent export SHOULD preserve agent attribution, instruction context, source context, destination context, mapping context, export method, review state, validation state, and uncertainty where agent activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Agent-exported content MUST NOT be treated as human-reviewed, validated, approved, authoritative, complete, accurate, or publication-ready merely because an agent exported it.

Export MAY be performed through workflows.

Workflow export SHOULD preserve workflow attribution, workflow state, source context, destination context, mapping context, export method, review state, validation state, and approval state where workflow activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Workflow completion MUST NOT be treated as human approval unless a future governed workflow specification explicitly defines that behavior.

Export MUST preserve privacy boundaries.

Export MUST NOT expose restricted Source Material, restricted evidence, restricted attribution, restricted relationships, restricted identifiers, restricted metadata, restricted provenance, restricted validation results, restricted source context, restricted workflow context, restricted agent context, restricted human review history, or restricted exported output merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, automation, or implementation convenience.

Where exported content is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Where export changes privacy risk through aggregation, synthesis, interpretation, redaction, normalization, mapping, publication, synchronization, workflow routing, agent processing, storage, indexing, or implementation rendering, the stricter applicable privacy expectation SHOULD govern handling unless a future governed privacy specification defines a different compliant rule.

Export SHOULD support validation.

A validator SHOULD be able to determine whether:

- Export Provenance is present where required;
- exported material is distinguishable from source governed material;
- exported Source Material is distinguishable from Knowledge Records;
- exported Source References are valid or marked uncertain where applicable;
- exported metadata remains within metadata role boundaries;
- exported relationships remain within relationship boundaries;
- exported identifiers do not silently redefine stable Object Identity;
- source context is preserved where required;
- destination context is preserved where required;
- mapping context is preserved where required;
- partial export is represented where applicable;
- lossy export is represented where applicable;
- export uncertainty is preserved where applicable;
- human, agent, and workflow involvement are distinguishable where applicable;
- privacy boundaries are preserved;
- Export Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.

Export SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, or package Export Provenance in a way that causes loss of meaning, broken Object Identity, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, migration loss, governance drift, implementation lock-in, export confusion, publication confusion, or source confusion.

Export Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what was exported, where it came from, where it went where applicable, what mapping occurred, what changed, what was omitted, what was redacted, who or what performed the export, whether human, agent, or workflow involvement occurred, whether review or validation occurred, whether privacy boundaries apply, whether exported material remains distinguishable from source governed material, and whether export provenance remains meaningful across time and implementation replacement.

## 16. Migration Provenance

Migration Provenance is provenance associated with moving, converting, mapping, preserving, transforming, validating, reviewing, importing, exporting, restoring, synchronizing, reindexing, restructuring, or otherwise carrying Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, attribution, validation results, identifiers, workflow outputs, agent outputs, or other governed entities across systems, formats, repositories, vaults, implementations, standards versions, storage environments, archives, backups, or compliant environments.

Migration Provenance exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what was migrated, where it came from, where it went, what changed, what was preserved, what was lost, what was mapped, whether meaning changed, whether review occurred, whether validation occurred, and whether privacy boundaries apply.

Migration Provenance SHALL be preserved where migration activity affects meaning, Object Identity, Source References, provenance, evidence, attribution, metadata, relationships, authority, privacy, lifecycle state, validation, compatibility, governance, publication, import, export, preservation, restoration, synchronization, or downstream use.

Migration Provenance MAY identify or describe:

- migration source;
- migration destination;
- migration actor;
- migration process;
- migration tool;
- migration workflow;
- migration agent;
- migration date where applicable;
- migrated Source Material;
- migrated Knowledge Objects;
- migrated Knowledge Records;
- migrated Source References;
- migrated metadata;
- migrated relationships;
- migrated identifiers;
- migrated evidence;
- migrated attribution;
- migrated validation results;
- migrated lifecycle state;
- migrated authority context;
- migrated privacy context;
- migrated compatibility context;
- mapping activity;
- transformation activity;
- extraction activity;
- import activity;
- export activity;
- validation activity;
- review activity;
- preservation activity;
- restoration activity;
- synchronization activity;
- reindexing activity;
- omitted content;
- restricted content;
- redacted content;
- failed migration items;
- partial migration items;
- uncertain migration items;
- compatibility limitations;
- other migration context that affects interpretation.

Migration Provenance is not the same as provenance as a whole.

Provenance may describe creation, source use, extraction, transformation, review, validation, agent activity, workflow activity, import, export, migration, or other change history.

Migration Provenance is the subset of provenance associated with carrying governed or source material across systems, formats, repositories, vaults, implementations, standards versions, storage environments, archives, backups, or compliant environments.

Migration Provenance is not the same as Import Provenance.

Import Provenance concerns bringing material into a compliant environment.

Migration Provenance concerns preserving, moving, converting, mapping, validating, reviewing, or transforming governed entities across environments or versions.

Import and migration MAY occur together.

Where import and migration occur together, provenance SHOULD preserve enough context to distinguish import behavior from migration behavior.

Migration Provenance is not the same as Export Provenance.

Export Provenance concerns producing governed or source material from a compliant environment for use elsewhere.

Migration Provenance concerns preserving, moving, converting, mapping, validating, reviewing, or transforming governed entities across environments or versions.

Export and migration MAY occur together.

Where export and migration occur together, provenance SHOULD preserve enough context to distinguish export behavior from migration behavior.

Migration Provenance is not the same as Transformation Provenance.

Migration may include transformation.

When migration includes transformation, Migration Provenance SHOULD preserve enough context to determine what was migrated, what was transformed, what mapping occurred, whether meaning changed, whether review occurred, and whether validation occurred.

Transformation Provenance SHOULD preserve the transformation-specific context.

Migration Provenance SHOULD preserve source environment context where source environment context affects interpretation, authority, privacy, validation, compatibility, governance, publication, import, export, restoration, synchronization, or downstream use.

Source environment context MAY include:

- source system;
- source repository;
- source vault;
- source archive;
- source database;
- source file system;
- source storage environment;
- source implementation;
- source standards version;
- source specification version;
- source format;
- source schema where applicable;
- source version;
- source date;
- source creator;
- source owner where applicable;
- source identifiers;
- legacy identifiers;
- implementation-specific identifiers;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source validation state;
- source compatibility expectations;
- source access conditions;
- source limitations.

Migration Provenance SHOULD preserve destination environment context where destination environment context affects interpretation, authority, privacy, validation, compatibility, governance, publication, import, export, restoration, synchronization, or downstream use.

Destination environment context MAY include:

- destination system;
- destination repository;
- destination vault;
- destination archive;
- destination database;
- destination file system;
- destination storage environment;
- destination implementation;
- destination standards version;
- destination specification version;
- destination format;
- destination schema where applicable;
- destination version;
- destination access expectation;
- destination privacy expectation;
- destination validation expectation;
- destination compatibility expectation;
- destination limitations.

Migration Provenance SHOULD preserve mapping context where mapping affects meaning, Object Identity, Source References, metadata, relationships, authority, privacy, validation, compatibility, import, export, governance, restoration, synchronization, or downstream use.

Mapping context MAY include:

- stable Object Identity mapping;
- legacy identifier to stable Object Identity mapping;
- implementation-specific identifier to stable Object Identity mapping;
- Source Identifier mapping;
- Source Reference mapping;
- metadata field mapping;
- relationship mapping;
- lifecycle state mapping;
- authority context mapping;
- privacy classification mapping;
- validation context mapping;
- provenance mapping;
- source archive mapping;
- file path mapping;
- storage location mapping;
- format mapping;
- schema mapping;
- unmapped governed content;
- omitted governed content;
- redacted governed content;
- uncertain mapping;
- rejected mapping;
- deferred mapping;
- mapping requiring human review.

Migration MUST preserve Object Identity boundaries.

A migration process MUST NOT silently create, replace, merge, split, redirect, overwrite, collapse, or reinterpret stable Object Identity.

Where migrated material corresponds to an existing Knowledge Object, the migration process SHOULD preserve enough provenance to determine how the match was made and whether review or validation occurred.

Where migrated material becomes a new Knowledge Object, the migration process SHOULD preserve enough provenance to determine why a new Object Identity was created.

Where migrated material cannot be safely matched to an existing Knowledge Object, the migration process SHOULD preserve uncertainty rather than silently assigning identity.

Where Object Identity changes during migration, the identity change SHOULD preserve enough provenance to determine what changed, why it changed, who or what changed it, whether review occurred, whether validation occurred, and whether prior references remain interpretable.

Migration MUST preserve Source Reference boundaries.

A migrated citation, URL, file path, database reference, external reference, archive reference, source identifier, or implementation-specific link MUST NOT automatically become, replace, or collapse a complete Source Reference unless it satisfies Source Reference requirements or a future governed specification defines compliant conversion behavior.

Where Source References are migrated, Migration Provenance SHOULD preserve whether each reference was preserved as-is, mapped, normalized, transformed, redacted, omitted, validated, rejected, or marked uncertain.

Migration MUST preserve provenance boundaries.

A migration process MUST NOT silently discard, collapse, overwrite, reinterpret, regenerate, anonymize, deanonymize, or replace provenance where provenance affects meaning, authority, privacy, validation, lifecycle state, relationships, Source References, compatibility, governance, or downstream use.

Where provenance is migrated, Migration Provenance SHOULD preserve what provenance was migrated, what mapping occurred, what was omitted, what was transformed, what was redacted, and whether review or validation occurred.

Migration MUST preserve metadata boundaries.

Migrated metadata MUST NOT silently redefine Object Identity, relationship meaning, lifecycle state, authority level, privacy classification, validation status, Source References, provenance, workflow state, agent state, or implementation behavior.

Where metadata is migrated, Migration Provenance SHOULD preserve what metadata was migrated, what mapping occurred, what was omitted, what was transformed, what was redacted, and whether review or validation occurred.

Migration MUST preserve relationship boundaries.

Migrated relationships MUST NOT silently redefine relationship type, direction, participants, strength, confidence, authority, privacy, validation, lifecycle state, or provenance.

Where relationships are migrated, Migration Provenance SHOULD preserve what relationship was migrated, what participants were identified, what mapping occurred, whether Object Identity was used, whether the relationship was reviewed, and whether validation occurred.

Migration MAY be complete or partial.

Partial migration is allowed.

Partial migration MUST NOT falsely imply that the migrated material represents the whole source environment, source repository, source archive, Source Material, Knowledge Object, Knowledge Record, metadata set, relationship set, evidence set, provenance set, validation set, workflow output, agent output, or governed entity when omitted context affects interpretation.

Migration MAY be lossless or lossy.

A lossless migration preserves meaning, Object Identity, Source References, provenance, metadata, relationships, lifecycle state, authority context, privacy expectations, validation expectations, compatibility expectations, and source context sufficiently for the intended use.

A lossy migration changes, omits, compresses, normalizes, redacts, summarizes, maps, renders, restructures, converts, or otherwise reduces meaning, Object Identity context, Source References, provenance, metadata, relationships, lifecycle state, authority context, privacy expectations, validation expectations, compatibility expectations, or source context.

Where migration is lossy, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, lifecycle state, compatibility, import, export, governance, publication, restoration, synchronization, or downstream use.

Migration MAY be uncertain.

Migration uncertainty SHOULD be preserved when source meaning, destination meaning, Object Identity matching, Source Reference mapping, metadata mapping, relationship mapping, attribution, extraction, transformation, validation, privacy handling, authority handling, compatibility, restoration behavior, synchronization behavior, or implementation behavior is unclear, disputed, incomplete, inferred, low-confidence, restricted, unavailable, or unverifiable.

Migration MAY be performed by humans.

Human migration SHOULD preserve attribution, source environment context, destination environment context, mapping context, review context, validation context, and uncertainty where migration affects meaning, authority, validation, privacy, publication, governance, or downstream use.

Migration MAY be performed by agents.

Agent migration SHOULD preserve agent attribution, instruction context, source environment context, destination environment context, mapping context, migration method, review state, validation state, and uncertainty where agent activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Agent-migrated content MUST NOT be treated as human-reviewed, validated, approved, authoritative, complete, accurate, or publication-ready merely because an agent migrated it.

Migration MAY be performed through workflows.

Workflow migration SHOULD preserve workflow attribution, workflow state, source environment context, destination environment context, mapping context, migration method, review state, validation state, and approval state where workflow activity affects meaning, authority, privacy, validation, publication, governance, or downstream use.

Workflow completion MUST NOT be treated as human approval unless a future governed workflow specification explicitly defines that behavior.

Migration MUST preserve privacy boundaries.

Migration MUST NOT expose restricted Source Material, restricted evidence, restricted attribution, restricted relationships, restricted identifiers, restricted metadata, restricted provenance, restricted validation results, restricted source context, restricted destination context, restricted workflow context, restricted agent context, restricted human review history, or restricted migrated output merely to improve traceability, review, validation, search, linking, indexing, publication, export, import, automation, synchronization, restoration, or implementation convenience.

Where migrated content is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Where migration changes privacy risk through aggregation, synthesis, interpretation, redaction, normalization, mapping, publication, synchronization, workflow routing, agent processing, storage, indexing, backup, restoration, or implementation rendering, the stricter applicable privacy expectation SHOULD govern handling unless a future governed privacy specification defines a different compliant rule.

Migration SHOULD support validation.

A validator SHOULD be able to determine whether:

- Migration Provenance is present where required;
- migrated material is distinguishable from source governed material;
- migrated Source Material is distinguishable from Knowledge Records;
- migrated Source References are valid or marked uncertain where applicable;
- migrated provenance remains present and interpretable where required;
- migrated metadata remains within metadata role boundaries;
- migrated relationships remain within relationship boundaries;
- migrated identifiers do not silently redefine stable Object Identity;
- source environment context is preserved where required;
- destination environment context is preserved where required;
- mapping context is preserved where required;
- partial migration is represented where applicable;
- lossy migration is represented where applicable;
- migration uncertainty is preserved where applicable;
- human, agent, and workflow involvement are distinguishable where applicable;
- privacy boundaries are preserved;
- Migration Provenance remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Migration SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, or migrate Migration Provenance in a way that causes loss of meaning, broken Object Identity, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, migration confusion, compatibility confusion, or source confusion.

Migration Provenance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what was migrated, where it came from, where it went, what mapping occurred, what changed, what was preserved, what was omitted, what was redacted, who or what performed the migration, whether human, agent, or workflow involvement occurred, whether review or validation occurred, whether privacy boundaries apply, whether migrated material remains distinguishable from source governed material, whether Object Identity, Source References, provenance, metadata, relationships, validation, privacy, authority, lifecycle state, and compatibility were preserved, and whether migration provenance remains meaningful across time and implementation replacement.

## 17. Source Availability

Source Availability is the condition describing whether Source Material, Source References, evidence, attribution, provenance, extracted content, transformed content, validation context, import context, export context, migration context, or other source-supporting material is available, unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, temporarily unavailable, unverifiable, or otherwise limited for review, validation, migration, import, export, preservation, publication, governance, or downstream use.

Source Availability exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether referenced Source Material or source-supporting context can still be accessed, reviewed, validated, preserved, migrated, imported, exported, or relied on for the intended use.

Source Availability SHALL be preserved where source availability affects meaning, interpretation, evidence, attribution, authority, privacy, lifecycle state, validation, relationships, compatibility, governance, publication, migration, import, export, preservation, restoration, synchronization, or downstream use.

Source Availability MAY identify or describe whether Source Material is:

- available;
- unavailable;
- partially available;
- temporarily unavailable;
- restricted;
- moved;
- missing;
- deleted;
- corrupted;
- archived;
- externally hosted;
- locally stored;
- duplicated;
- backed up;
- restored;
- superseded;
- deprecated;
- replaced;
- redacted;
- inaccessible;
- unverifiable;
- access-controlled;
- format-limited;
- permission-limited;
- privacy-limited;
- legally limited;
- contractually limited;
- technically limited;
- implementation-limited;
- migration-limited;
- import-limited;
- export-limited;
- preservation-limited;
- otherwise unavailable or constrained.

Source Availability is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

Source Availability describes whether that material can be accessed, reviewed, validated, preserved, migrated, imported, exported, or otherwise used.

Source Availability is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

Source Availability describes whether the referenced Source Material or source-supporting context remains accessible, reviewable, restricted, missing, moved, deleted, archived, superseded, or otherwise limited.

A Source Reference MAY remain valid even when Source Material is unavailable.

A Source Reference MAY become incomplete, uncertain, restricted, or review-limited when Source Material availability changes.

Source Availability is not the same as Source Reliability.

Source Availability describes access, presence, retrievability, preservation state, or reviewability.

Source Reliability describes trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength.

Available Source Material is not automatically reliable.

Unavailable Source Material is not automatically unreliable.

Partially available Source Material is not automatically invalid.

Source Availability is not the same as Source Authority.

Source Availability describes whether the source can be accessed or reviewed.

Source Authority describes governance weight, interpretive relevance, official status, review status, or approved use assigned to Source Material within a particular context.

Available Source Material is not automatically authoritative.

Unavailable Source Material may still have historical, evidentiary, audit, provenance, or governance relevance.

Source Availability is not the same as validation.

Validation may check Source Availability.

Source Availability may affect validation.

However, availability alone does not prove that Source Material is accurate, complete, reliable, approved, authoritative, current, compatible, or safe for downstream use.

Source Availability SHOULD be represented where unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, or unverifiable Source Material affects interpretation.

Source Availability SHOULD preserve enough context to determine:

- what Source Material availability condition applies;
- when the availability condition was observed where applicable;
- who or what observed the availability condition where applicable;
- whether the condition was human-recorded, agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated;
- whether the condition affects evidence;
- whether the condition affects attribution;
- whether the condition affects Source References;
- whether the condition affects provenance;
- whether the condition affects validation;
- whether the condition affects authority;
- whether the condition affects lifecycle state;
- whether the condition affects privacy handling;
- whether the condition affects migration, import, export, restoration, synchronization, preservation, publication, or downstream use.

Source Availability MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, historically preserved, imported, exported, or migrated.

Where Source Availability is incomplete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, authority, privacy, validation, lifecycle state, compatibility, governance, publication, preservation, migration, import, export, restoration, synchronization, or downstream use.

Source Availability MAY change over time.

Source Material may become available after being unavailable.

Source Material may become unavailable after being available.

Source Material may move, be deleted, become restricted, become corrupted, be archived, be restored, be superseded, be replaced, be redacted, or become externally inaccessible.

Availability changes SHOULD preserve provenance where the change affects meaning, authority, privacy, validation, lifecycle state, compatibility, governance, migration, import, export, preservation, restoration, synchronization, or downstream use.

A Source Reference SHOULD NOT be silently removed merely because Source Material becomes unavailable.

Unavailable Source Material SHOULD remain historically referenceable where it affects evidence, attribution, provenance, review history, validation history, lifecycle state, authority, governance, audit, migration, import, export, or downstream use.

Where Source Material becomes unavailable, the associated Source Reference SHOULD preserve or support enough context for future review.

Preserved context MAY include:

- source title or label;
- source type;
- source creator;
- source publisher;
- source date;
- source identifier;
- external reference;
- citation;
- archive reference;
- prior location;
- last known location;
- last known availability state;
- availability observation date where applicable;
- reason for unavailability where known;
- whether restricted access applies;
- whether a copy, archive, backup, export, or migrated representation exists;
- whether review or validation is blocked;
- whether downstream use is affected.

A Source Reference SHOULD NOT falsely imply that Source Material remains available when the source is unavailable, moved, missing, deleted, corrupted, restricted, archived, superseded, externally inaccessible, or unverifiable.

A Knowledge Record SHOULD NOT falsely imply that Source Material remains available, verified, unrestricted, current, complete, reliable, or unchanged when availability is unknown, restricted, false, superseded, unverifiable, or materially uncertain.

Source Availability MAY affect evidence.

Where Source Material is unavailable, partially available, restricted, corrupted, superseded, or unverifiable, evidence support MAY become limited, uncertain, review-limited, validation-limited, authority-limited, publication-limited, migration-limited, import-limited, export-limited, or governance-limited.

Such limitations SHOULD be preserved when they affect interpretation, validation, authority, lifecycle state, privacy, compatibility, governance, publication, or downstream use.

Source Availability MAY affect attribution.

Where Source Material availability affects authorship, publication context, source origin, actor identification, ownership context, review context, or provenance context, that availability condition SHOULD be preserved.

Source Availability MAY affect validation.

A validator SHOULD be able to determine whether Source Material is available enough to support required review, validation, migration, import, export, publication, preservation, or downstream use.

Where Source Material is unavailable, restricted, partially available, corrupted, missing, deleted, or unverifiable, validation SHOULD preserve whether validation passed, failed, partially passed, was blocked, was deferred, or requires human review.

Source Availability MAY affect authority.

A source availability condition MAY limit the authority, approved use, publication readiness, validation confidence, reviewability, or downstream use of source-derived knowledge.

Source Availability does not automatically remove authority.

Source Availability does not automatically create authority.

Authority impact SHOULD be governed through authority, validation, lifecycle, review, or future source-authority specifications.

Source Availability MAY affect lifecycle state.

A Knowledge Record, Source Reference, relationship, validation result, provenance record, or other governed entity MAY require review, correction, restriction, deprecation, supersession, archival, or other lifecycle handling when Source Material becomes unavailable, restricted, corrupted, deleted, superseded, or unverifiable.

Source Availability does not automatically change lifecycle state unless a governed process or future specification defines that behavior.

Source Availability MAY affect migration, import, and export.

Migration, import, and export processes SHOULD preserve availability context where availability affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, validation, authority, privacy, lifecycle state, compatibility, preservation, restoration, synchronization, or downstream use.

A migration, import, or export process MUST NOT silently convert unavailable, restricted, partial, corrupted, superseded, externally hosted, or unverifiable Source Material into an apparently available and complete source.

A migration, import, or export process SHOULD preserve whether Source Material was available, unavailable, restricted, partial, omitted, redacted, substituted, archived, copied, linked, referenced, validated, or marked uncertain.

Source Availability MAY be expressed through metadata.

Source Availability metadata MAY describe:

- availability state;
- availability date where applicable;
- availability observer where applicable and permitted;
- availability source;
- source location;
- source access condition;
- source restriction;
- source archive status;
- source backup status;
- source restoration status;
- source corruption status;
- source deletion status;
- source movement status;
- source supersession status;
- source replacement status;
- source external hosting status;
- source validation status;
- review limitation;
- validation limitation;
- migration limitation;
- import limitation;
- export limitation;
- preservation limitation;
- compatibility expectation.

KS-0005 does not define exact Source Availability metadata fields or exact availability-state values.

A future specification MAY define exact source-availability fields, allowed values, status vocabularies, validation rules, archival rules, backup rules, restoration rules, source-location fields, source-access fields, import formats, export formats, migration mappings, or serialization syntax.

Source Availability MUST preserve privacy boundaries.

Source Availability MUST NOT expose restricted Source Material, restricted source locations, restricted identifiers, restricted attribution, restricted relationships, restricted metadata, restricted provenance, restricted validation results, restricted archives, restricted backups, restricted access conditions, or restricted source context merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, restoration, synchronization, or implementation convenience.

Where Source Availability is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A system, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or implementation MUST NOT treat restricted Source Material as unavailable merely because the current actor lacks access.

Restricted is not the same as missing.

Missing is not the same as deleted.

Deleted is not the same as superseded.

Superseded is not the same as invalid.

Unavailable is not the same as unreliable.

Availability states SHOULD remain distinguishable where the distinction affects interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, or downstream use.

Source Availability SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Availability is present where required;
- Source Material is available, unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, temporarily unavailable, or unverifiable where applicable;
- availability state is distinguishable from reliability;
- availability state is distinguishable from authority;
- availability state is distinguishable from validation status;
- availability state is distinguishable from privacy classification;
- unavailable Source Material remains historically referenceable where required;
- restricted Source Material is not falsely treated as missing;
- missing Source Material is not falsely treated as deleted;
- superseded Source Material is not falsely treated as invalid;
- availability changes preserve provenance where required;
- Source References preserve enough context where source availability changed;
- migration, import, and export preserve availability context where required;
- privacy boundaries are preserved;
- Source Availability remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Source Availability SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, or migrate Source Availability in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, availability confusion, compatibility confusion, or source confusion.

Source Availability is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether Source Material or source-supporting context is available, unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, temporarily unavailable, or unverifiable; whether that availability state affects evidence, attribution, Source References, provenance, validation, authority, lifecycle state, privacy, compatibility, migration, import, export, restoration, synchronization, preservation, publication, or downstream use; and whether availability meaning remains intact across time and implementation replacement.

## 18. Source Reliability

Source Reliability is the assessed trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength of Source Material, Source References, evidence, attribution, provenance, extracted content, transformed content, validation context, import context, export context, migration context, or other source-supporting material.

Source Reliability exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand whether Source Material or source-supporting context is reliable enough for the intended use, what limitations affect interpretation, whether conflicting evidence exists, whether review occurred, and whether reliability concerns affect authority, validation, lifecycle state, privacy, compatibility, governance, publication, or downstream use.

Source Reliability SHALL be preserved where source reliability affects meaning, interpretation, evidence, attribution, authority, privacy, lifecycle state, validation, relationships, compatibility, governance, publication, migration, import, export, preservation, restoration, synchronization, or downstream use.

Source Reliability MAY identify or describe whether Source Material is:

- reliable;
- partially reliable;
- unreliable;
- uncertain;
- disputed;
- conflicting;
- incomplete;
- outdated;
- superseded;
- stale;
- fresh;
- current;
- reviewed;
- unreviewed;
- validated;
- unvalidated;
- low-confidence;
- high-confidence;
- biased or potentially biased;
- limited in scope;
- limited in evidence value;
- limited in context;
- limited by authorship;
- limited by publication context;
- limited by provenance;
- limited by availability;
- limited by translation;
- limited by extraction;
- limited by transformation;
- limited by import;
- limited by export;
- limited by migration;
- limited by implementation behavior;
- otherwise reliability-limited or reliability-relevant.

Source Reliability is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

Source Reliability describes whether that material is trustworthy, complete, current, uncertain, conflicted, limited, biased, reviewed, validated, or otherwise suitable for a particular governed use.

Source Reliability is not the same as Source Availability.

Source Availability describes whether Source Material can be accessed, reviewed, validated, preserved, migrated, imported, exported, or otherwise used.

Source Reliability describes the quality, trustworthiness, freshness, completeness, uncertainty, limitation, conflict, or evidentiary strength of the Source Material.

Available Source Material is not automatically reliable.

Unavailable Source Material is not automatically unreliable.

Partially available Source Material may still have reliability value where enough context remains for the intended use.

Source Reliability is not the same as Source Authority.

Source Authority describes governance weight, interpretive relevance, official status, review status, or approved use assigned to Source Material within a particular context.

Source Reliability describes source quality and evidentiary trustworthiness.

Reliable Source Material is not automatically authoritative.

Authoritative Source Material is not automatically complete, current, unbiased, or sufficient for every use.

Source Reliability is not the same as validation.

Validation may assess Source Reliability.

Source Reliability may affect validation.

However, reliability alone does not prove that Source Material is approved, authoritative, complete, current, privacy-cleared, compatible, or safe for downstream use.

Source Reliability is not the same as truth.

A source may be reliable for one purpose and still contain errors, omissions, outdated information, uncertain interpretation, conflicting evidence, limited scope, or privacy restrictions.

A source may be unreliable for one purpose and still preserve useful provenance, attribution, historical context, contradiction, or audit value.

Source Reliability SHOULD be represented where reliability affects interpretation, evidence, attribution, Source References, provenance, validation, authority, lifecycle state, privacy, migration, import, export, governance, publication, or downstream use.

Source Reliability SHOULD preserve enough context to determine:

- what reliability assessment applies;
- what Source Material or source-supporting context was assessed;
- who or what assessed reliability where applicable;
- when reliability was assessed where applicable;
- whether the assessment was human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated;
- what evidence supported the reliability assessment;
- whether review occurred;
- whether validation occurred;
- whether conflicting evidence exists;
- whether reliability is complete, partial, restricted, uncertain, inferred, disputed, stale, superseded, or historically preserved;
- whether reliability affects authority;
- whether reliability affects lifecycle state;
- whether reliability affects privacy handling;
- whether reliability affects migration, import, export, restoration, synchronization, preservation, publication, or downstream use.

Source Reliability MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, historically preserved, imported, exported, or migrated.

Where Source Reliability is incomplete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, authority, privacy, validation, lifecycle state, compatibility, governance, publication, preservation, migration, import, export, restoration, synchronization, or downstream use.

Source Reliability MAY change over time.

Source Material may become more reliable when additional evidence, review, validation, correction, official confirmation, provenance, context, or source availability becomes available.

Source Material may become less reliable when new conflicting evidence, supersession, correction, retraction, corruption, missing context, restricted access, outdated information, failed validation, or review concern appears.

Reliability changes SHOULD preserve provenance where the change affects meaning, authority, privacy, validation, lifecycle state, compatibility, governance, migration, import, export, preservation, restoration, synchronization, or downstream use.

A Source Reference SHOULD NOT be silently removed merely because Source Material is unreliable, disputed, incomplete, outdated, superseded, or low-confidence.

Unreliable, disputed, incomplete, outdated, superseded, or low-confidence Source Material MAY remain historically referenceable where it affects evidence, contradiction, attribution, provenance, review history, validation history, lifecycle state, authority, governance, audit, migration, import, export, or downstream use.

A Source Reference SHOULD NOT falsely imply that Source Material is reliable when reliability is unknown, disputed, incomplete, outdated, superseded, unvalidated, restricted, unavailable, or materially uncertain.

A Knowledge Record SHOULD NOT falsely imply that Source Material is reliable, verified, authoritative, current, complete, unbiased, reviewed, validated, or unchanged when reliability is unknown, restricted, false, superseded, unverifiable, disputed, or materially uncertain.

Source Reliability MAY affect evidence.

Where Source Material is unreliable, partially reliable, disputed, incomplete, outdated, superseded, biased, low-confidence, or unverifiable, evidence support MAY become limited, uncertain, review-limited, validation-limited, authority-limited, publication-limited, migration-limited, import-limited, export-limited, or governance-limited.

Such limitations SHOULD be preserved when they affect interpretation, validation, authority, lifecycle state, privacy, compatibility, governance, publication, or downstream use.

Source Reliability MAY affect attribution.

Where Source Reliability affects authorship, publication context, source origin, actor identification, ownership context, review context, evidence quality, or provenance context, that reliability condition SHOULD be preserved.

Source Reliability MAY affect validation.

A validator SHOULD be able to determine whether Source Material is reliable enough to support required review, validation, migration, import, export, publication, preservation, or downstream use.

Where Source Material is unreliable, partially reliable, disputed, incomplete, outdated, superseded, biased, low-confidence, restricted, unavailable, or unverifiable, validation SHOULD preserve whether validation passed, failed, partially passed, was blocked, was deferred, or requires human review.

Source Reliability MAY affect authority.

A source reliability condition MAY limit the authority, approved use, publication readiness, validation confidence, reviewability, or downstream use of source-derived knowledge.

Source Reliability does not automatically remove authority.

Source Reliability does not automatically create authority.

Authority impact SHOULD be governed through authority, validation, lifecycle, review, or future source-authority specifications.

Source Reliability MAY affect lifecycle state.

A Knowledge Record, Source Reference, relationship, validation result, provenance record, or other governed entity MAY require review, correction, restriction, deprecation, supersession, archival, rejection, or other lifecycle handling when Source Material becomes unreliable, disputed, incomplete, outdated, superseded, biased, low-confidence, or unverifiable.

Source Reliability does not automatically change lifecycle state unless a governed process or future specification defines that behavior.

Source Reliability MAY affect migration, import, and export.

Migration, import, and export processes SHOULD preserve reliability context where reliability affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, validation, authority, privacy, lifecycle state, compatibility, preservation, restoration, synchronization, or downstream use.

A migration, import, or export process MUST NOT silently convert unreliable, disputed, incomplete, outdated, superseded, biased, low-confidence, restricted, unavailable, or unverifiable Source Material into an apparently reliable and complete source.

A migration, import, or export process SHOULD preserve whether Source Material was reliable, partially reliable, unreliable, disputed, incomplete, outdated, superseded, low-confidence, reviewed, unreviewed, validated, unvalidated, omitted, redacted, substituted, copied, linked, referenced, or marked uncertain.

Source Reliability MAY be expressed through metadata.

Source Reliability metadata MAY describe:

- reliability state;
- reliability assessment date where applicable;
- reliability assessor where applicable and permitted;
- reliability source;
- reliability evidence;
- reliability limitation;
- reliability confidence;
- review state;
- validation state;
- conflict state;
- contradiction state;
- freshness state;
- completeness state;
- bias concern;
- scope limitation;
- source quality concern;
- source availability dependency;
- source authority dependency;
- source privacy dependency;
- source compatibility expectation;
- migration limitation;
- import limitation;
- export limitation;
- preservation limitation;
- downstream-use limitation.

KS-0005 does not define exact Source Reliability metadata fields or exact reliability-state values.

A future specification MAY define exact source-reliability fields, allowed values, confidence values, reliability vocabularies, evidence-ranking rules, validation rules, conflict-handling rules, review rules, source-quality fields, import formats, export formats, migration mappings, or serialization syntax.

Source Reliability MUST preserve privacy boundaries.

Source Reliability MUST NOT expose restricted Source Material, restricted source locations, restricted identifiers, restricted attribution, restricted relationships, restricted metadata, restricted provenance, restricted validation results, restricted reliability assessments, restricted review notes, restricted source context, restricted conflict context, or restricted evidence merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, restoration, synchronization, or implementation convenience.

Where Source Reliability is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A system, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or implementation MUST NOT treat restricted reliability context as absent merely because the current actor lacks access.

Reliable is not the same as authoritative.

Authoritative is not the same as reliable.

Available is not the same as reliable.

Unavailable is not the same as unreliable.

Reviewed is not the same as approved.

Validated is not the same as true.

Current is not the same as complete.

Outdated is not the same as invalid.

Superseded is not the same as useless.

Reliability states SHOULD remain distinguishable where the distinction affects interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, or downstream use.

Source Reliability SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Reliability is present where required;
- Source Material is reliable, partially reliable, unreliable, uncertain, disputed, incomplete, outdated, superseded, low-confidence, high-confidence, biased, reviewed, unreviewed, validated, or unvalidated where applicable;
- reliability state is distinguishable from availability;
- reliability state is distinguishable from authority;
- reliability state is distinguishable from validation status;
- reliability state is distinguishable from privacy classification;
- reliability state is distinguishable from truth;
- unreliable Source Material remains historically referenceable where required;
- restricted reliability context is not falsely treated as absent;
- disputed Source Material is not falsely treated as resolved;
- outdated Source Material is not falsely treated as invalid;
- superseded Source Material is not falsely treated as useless;
- reliability changes preserve provenance where required;
- Source References preserve enough context where source reliability changed;
- migration, import, and export preserve reliability context where required;
- privacy boundaries are preserved;
- Source Reliability remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Source Reliability SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, or migrate Source Reliability in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, reliability confusion, compatibility confusion, or source confusion.

Source Reliability is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether Source Material or source-supporting context is reliable, partially reliable, unreliable, uncertain, disputed, incomplete, outdated, superseded, low-confidence, high-confidence, biased, reviewed, unreviewed, validated, unvalidated, or otherwise reliability-limited; whether that reliability state affects evidence, attribution, Source References, provenance, validation, authority, lifecycle state, privacy, compatibility, migration, import, export, restoration, synchronization, preservation, publication, or downstream use; and whether reliability meaning remains intact across time and implementation replacement.

## 19. Source Authority

Source Authority is the governance weight, interpretive relevance, official status, review status, approved use, jurisdictional relevance, organizational relevance, contextual priority, or source-use permission assigned to Source Material, Source References, evidence, attribution, provenance, extracted content, transformed content, validation context, import context, export context, migration context, or other source-supporting material within a particular governed context.

Source Authority exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand whether Source Material or source-supporting context may be relied on for a particular purpose, what authority limits apply, whether authority depends on review or validation, and whether authority affects lifecycle state, privacy, compatibility, governance, publication, migration, import, export, or downstream use.

Source Authority SHALL be preserved where source authority affects meaning, interpretation, evidence, attribution, privacy, lifecycle state, validation, relationships, compatibility, governance, publication, migration, import, export, preservation, restoration, synchronization, or downstream use.

Source Authority MAY identify or describe whether Source Material is:

- authoritative;
- partially authoritative;
- non-authoritative;
- official;
- unofficial;
- primary;
- secondary;
- tertiary;
- advisory;
- contextual;
- historical;
- superseded;
- deprecated;
- draft;
- approved;
- rejected;
- reviewed;
- unreviewed;
- validated;
- unvalidated;
- internally authoritative;
- externally authoritative;
- jurisdiction-specific;
- organization-specific;
- domain-specific;
- project-specific;
- workflow-authorized;
- human-approved;
- agent-proposed;
- implementation-provided;
- publication-ready;
- not publication-ready;
- authority-limited;
- otherwise authority-relevant.

Source Authority is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

Source Authority describes the governed weight, role, official status, review status, approved use, or interpretive relevance assigned to that material in a particular context.

Source Authority is not the same as Source Availability.

Source Availability describes whether Source Material can be accessed, reviewed, validated, preserved, migrated, imported, exported, or otherwise used.

Source Authority describes whether Source Material carries governed weight or approved relevance for a particular use.

Available Source Material is not automatically authoritative.

Unavailable Source Material may still retain historical, evidentiary, audit, provenance, or governance authority where that authority remains meaningful.

Source Authority is not the same as Source Reliability.

Source Reliability describes source quality, trustworthiness, freshness, completeness, uncertainty, limitation, conflict, or evidentiary strength.

Source Authority describes governance weight, official status, review status, approved use, or interpretive relevance.

Reliable Source Material is not automatically authoritative.

Authoritative Source Material is not automatically reliable, complete, current, unbiased, available, or sufficient for every use.

Source Authority is not the same as validation.

Validation may check whether Source Authority is present, appropriate, current, or sufficient.

Source Authority may affect validation.

However, authority alone does not prove that Source Material is accurate, complete, reliable, current, privacy-cleared, compatible, or safe for downstream use.

Source Authority is not the same as truth.

An authoritative source may contain errors, omissions, outdated information, disputed interpretation, limited scope, restricted context, or superseded material.

A non-authoritative source may still preserve useful evidence, contradiction, attribution, provenance, historical context, review context, or audit value.

Source Authority SHOULD be represented where authority affects interpretation, evidence, attribution, Source References, provenance, validation, lifecycle state, privacy, migration, import, export, governance, publication, or downstream use.

Source Authority SHOULD preserve enough context to determine:

- what authority assessment applies;
- what Source Material or source-supporting context was assessed;
- who or what assigned authority where applicable;
- when authority was assigned where applicable;
- whether the authority was human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated;
- what evidence supported the authority assessment;
- whether review occurred;
- whether validation occurred;
- whether approval occurred;
- whether rejection occurred;
- whether authority is complete, partial, restricted, uncertain, inferred, disputed, stale, superseded, deprecated, or historically preserved;
- whether authority affects lifecycle state;
- whether authority affects privacy handling;
- whether authority affects migration, import, export, restoration, synchronization, preservation, publication, or downstream use.

Source Authority MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, historically preserved, imported, exported, or migrated.

Where Source Authority is incomplete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, privacy, validation, lifecycle state, compatibility, governance, publication, preservation, migration, import, export, restoration, synchronization, or downstream use.

Source Authority MAY change over time.

Source Material may gain authority when it is reviewed, validated, approved, officially adopted, superseding, governance-recognized, publication-approved, or assigned interpretive weight by a governed process.

Source Material may lose or reduce authority when it is superseded, deprecated, rejected, contradicted, corrected, retracted, invalidated, replaced, restricted, or found unsuitable for a particular use.

Authority changes SHOULD preserve provenance where the change affects meaning, privacy, validation, lifecycle state, compatibility, governance, migration, import, export, preservation, restoration, synchronization, or downstream use.

A Source Reference SHOULD NOT be silently removed merely because Source Material is non-authoritative, disputed, deprecated, rejected, superseded, or authority-limited.

Non-authoritative, disputed, deprecated, rejected, superseded, or authority-limited Source Material MAY remain historically referenceable where it affects evidence, contradiction, attribution, provenance, review history, validation history, lifecycle state, governance, audit, migration, import, export, or downstream use.

A Source Reference SHOULD NOT falsely imply that Source Material is authoritative when authority is unknown, disputed, deprecated, rejected, superseded, unreviewed, unvalidated, restricted, unavailable, or materially uncertain.

A Knowledge Record SHOULD NOT falsely imply that Source Material is authoritative, approved, official, reviewed, validated, current, complete, reliable, privacy-cleared, or publication-ready when authority is unknown, restricted, false, superseded, deprecated, rejected, unverifiable, disputed, or materially uncertain.

Source Authority MAY affect evidence.

Where Source Material is non-authoritative, partially authoritative, disputed, deprecated, rejected, superseded, unofficial, unreviewed, unvalidated, or authority-limited, evidence support MAY become limited, uncertain, review-limited, validation-limited, publication-limited, migration-limited, import-limited, export-limited, or governance-limited.

Such limitations SHOULD be preserved when they affect interpretation, validation, lifecycle state, privacy, compatibility, governance, publication, or downstream use.

Source Authority MAY affect attribution.

Where Source Authority affects authorship, publication context, source origin, official status, actor identification, ownership context, review context, evidence quality, or provenance context, that authority condition SHOULD be preserved.

Source Authority MAY affect validation.

A validator SHOULD be able to determine whether Source Material has enough authority to support required review, validation, migration, import, export, publication, preservation, or downstream use.

Where Source Material is non-authoritative, partially authoritative, disputed, deprecated, rejected, superseded, unofficial, unreviewed, unvalidated, authority-limited, restricted, unavailable, or unverifiable, validation SHOULD preserve whether validation passed, failed, partially passed, was blocked, was deferred, or requires human review.

Source Authority MAY affect lifecycle state.

A Knowledge Record, Source Reference, relationship, validation result, provenance record, or other governed entity MAY require review, correction, restriction, deprecation, supersession, approval, rejection, archival, or other lifecycle handling when Source Material becomes authoritative, non-authoritative, disputed, deprecated, rejected, superseded, unofficial, unreviewed, unvalidated, or authority-limited.

Source Authority does not automatically change lifecycle state unless a governed process or future specification defines that behavior.

Source Authority MAY affect migration, import, and export.

Migration, import, and export processes SHOULD preserve authority context where authority affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, validation, privacy, lifecycle state, compatibility, preservation, restoration, synchronization, publication, or downstream use.

A migration, import, or export process MUST NOT silently convert non-authoritative, disputed, deprecated, rejected, superseded, unofficial, unreviewed, unvalidated, authority-limited, restricted, unavailable, or unverifiable Source Material into an apparently authoritative and approved source.

A migration, import, or export process SHOULD preserve whether Source Material was authoritative, partially authoritative, non-authoritative, official, unofficial, reviewed, unreviewed, approved, rejected, validated, unvalidated, deprecated, superseded, omitted, redacted, substituted, copied, linked, referenced, or marked uncertain.

Source Authority MAY be expressed through metadata.

Source Authority metadata MAY describe:

- authority state;
- authority level;
- authority scope;
- authority assignment date where applicable;
- authority assessor where applicable and permitted;
- authority source;
- authority evidence;
- authority limitation;
- review state;
- approval state;
- rejection state;
- validation state;
- official status;
- supersession state;
- deprecation state;
- jurisdictional scope;
- organizational scope;
- domain scope;
- project scope;
- publication readiness;
- governance relevance;
- source availability dependency;
- source reliability dependency;
- source privacy dependency;
- source compatibility expectation;
- migration limitation;
- import limitation;
- export limitation;
- preservation limitation;
- downstream-use limitation.

KS-0005 does not define exact Source Authority metadata fields or exact authority-state values.

A future specification MAY define exact source-authority fields, allowed values, authority vocabularies, review rules, approval rules, rejection rules, validation rules, governance-weight values, official-status values, lifecycle mappings, publication rules, import formats, export formats, migration mappings, or serialization syntax.

Source Authority MUST preserve privacy boundaries.

Source Authority MUST NOT expose restricted Source Material, restricted source locations, restricted identifiers, restricted attribution, restricted relationships, restricted metadata, restricted provenance, restricted validation results, restricted authority assessments, restricted review notes, restricted governance context, restricted source context, restricted conflict context, or restricted evidence merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, restoration, synchronization, or implementation convenience.

Where Source Authority is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A system, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or implementation MUST NOT treat restricted authority context as absent merely because the current actor lacks access.

Authoritative is not the same as reliable.

Reliable is not the same as authoritative.

Available is not the same as authoritative.

Unavailable is not the same as non-authoritative.

Reviewed is not the same as approved.

Approved is not the same as true.

Official is not the same as complete.

Deprecated is not the same as useless.

Superseded is not the same as invalid.

Authority states SHOULD remain distinguishable where the distinction affects interpretation, validation, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, or downstream use.

Source Authority SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Authority is present where required;
- Source Material is authoritative, partially authoritative, non-authoritative, official, unofficial, reviewed, unreviewed, approved, rejected, validated, unvalidated, deprecated, superseded, disputed, or authority-limited where applicable;
- authority state is distinguishable from availability;
- authority state is distinguishable from reliability;
- authority state is distinguishable from validation status;
- authority state is distinguishable from privacy classification;
- authority state is distinguishable from truth;
- non-authoritative Source Material remains historically referenceable where required;
- restricted authority context is not falsely treated as absent;
- disputed authority is not falsely treated as resolved;
- deprecated Source Material is not falsely treated as useless;
- superseded Source Material is not falsely treated as invalid;
- authority changes preserve provenance where required;
- Source References preserve enough context where source authority changed;
- migration, import, and export preserve authority context where required;
- privacy boundaries are preserved;
- Source Authority remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Source Authority SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, or migrate Source Authority in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, authority confusion, compatibility confusion, or source confusion.

Source Authority is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether Source Material or source-supporting context is authoritative, partially authoritative, non-authoritative, official, unofficial, reviewed, unreviewed, approved, rejected, validated, unvalidated, deprecated, superseded, disputed, authority-limited, or otherwise authority-relevant; whether that authority state affects evidence, attribution, Source References, provenance, validation, lifecycle state, privacy, compatibility, migration, import, export, restoration, synchronization, preservation, publication, governance, or downstream use; and whether authority meaning remains intact across time and implementation replacement.

## 20. Source Privacy

Source Privacy is the privacy classification, visibility boundary, access expectation, redaction requirement, disclosure limitation, exposure risk, handling rule, routing constraint, publication constraint, indexing constraint, agent-access constraint, workflow-access constraint, synchronization constraint, backup constraint, import constraint, export constraint, migration constraint, or downstream-use restriction associated with Source Material, Source References, evidence, attribution, provenance, extracted content, transformed content, validation context, import context, export context, migration context, or other source-supporting material.

Source Privacy exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand whether Source Material or source-supporting context may be accessed, copied, summarized, extracted, transformed, indexed, embedded, linked, routed, published, exported, imported, migrated, synchronized, backed up, restored, or otherwise used.

Source Privacy SHALL be preserved where source privacy affects meaning, interpretation, evidence, attribution, authority, lifecycle state, validation, relationships, compatibility, governance, publication, migration, import, export, preservation, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Privacy MAY identify or describe whether Source Material or source-supporting context is:

- public;
- private;
- restricted;
- confidential;
- sensitive;
- internal;
- external;
- personal;
- identifying;
- anonymized;
- pseudonymized;
- redacted;
- partially redacted;
- access-controlled;
- permission-limited;
- publication-limited;
- export-limited;
- import-limited;
- migration-limited;
- synchronization-limited;
- backup-limited;
- restoration-limited;
- indexing-limited;
- embedding-limited;
- agent-limited;
- workflow-limited;
- implementation-limited;
- legally limited;
- ethically limited;
- contractually limited;
- operationally limited;
- source-location-limited;
- attribution-limited;
- evidence-limited;
- provenance-limited;
- otherwise privacy-restricted or privacy-relevant.

Source Privacy is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

Source Privacy describes how that material or its source-supporting context may be accessed, exposed, copied, summarized, transformed, published, exported, migrated, indexed, processed, or otherwise handled.

Source Privacy is not the same as Source Availability.

Source Availability describes whether Source Material can be accessed, reviewed, validated, preserved, migrated, imported, exported, or otherwise used.

Source Privacy describes whether access, review, validation, preservation, migration, import, export, publication, indexing, agent processing, workflow routing, or downstream use is permitted or restricted.

Restricted Source Material is not the same as unavailable Source Material.

Unavailable Source Material is not automatically private.

Available Source Material is not automatically public.

Source Privacy is not the same as Source Reliability.

Source Reliability describes source quality, trustworthiness, freshness, completeness, uncertainty, limitation, conflict, or evidentiary strength.

Source Privacy describes handling boundaries and exposure constraints.

Private Source Material may be reliable.

Public Source Material may be unreliable.

Reliable Source Material is not automatically safe to expose.

Source Privacy is not the same as Source Authority.

Source Authority describes governance weight, official status, review status, approved use, or interpretive relevance.

Source Privacy describes access, exposure, visibility, routing, publication, and handling boundaries.

Authoritative Source Material is not automatically public.

Private Source Material may be authoritative within a restricted context.

Source Privacy is not the same as validation.

Validation may check Source Privacy.

Source Privacy may limit validation.

However, privacy classification alone does not prove that Source Material is accurate, reliable, authoritative, current, complete, approved, compatible, or safe for downstream use.

Source Privacy is not the same as security.

Source Privacy defines source-level handling expectations within The Brain Standard.

Security mechanisms may enforce access, encryption, authentication, authorization, audit logging, retention, deletion, or transport protection.

KS-0005 does not define exact security mechanisms.

A future specification MAY define exact privacy classifications, access-control mappings, security expectations, encryption expectations, audit requirements, retention rules, redaction rules, publication rules, export rules, import rules, migration rules, or implementation-specific enforcement behavior.

Source Privacy SHOULD be represented where privacy affects interpretation, evidence, attribution, Source References, provenance, validation, authority, lifecycle state, relationships, migration, import, export, governance, publication, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Privacy SHOULD preserve enough context to determine:

- what privacy condition applies;
- what Source Material or source-supporting context is affected;
- who or what assigned the privacy condition where applicable;
- when the privacy condition was assigned where applicable;
- whether the privacy condition was human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated;
- whether access is permitted;
- whether exposure is permitted;
- whether copying is permitted;
- whether extraction is permitted;
- whether transformation is permitted;
- whether summarization is permitted;
- whether indexing is permitted;
- whether embedding is permitted;
- whether agent processing is permitted;
- whether workflow routing is permitted;
- whether publication is permitted;
- whether synchronization is permitted;
- whether backup or restoration is permitted;
- whether import, export, or migration is permitted;
- whether redaction is required;
- whether restricted context may be disclosed;
- whether privacy affects validation;
- whether privacy affects authority;
- whether privacy affects lifecycle state;
- whether privacy affects downstream use.

Source Privacy MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, historically preserved, imported, exported, or migrated.

Where Source Privacy is incomplete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, lifecycle state, compatibility, governance, publication, preservation, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Privacy MAY change over time.

Source Material may become more restricted when new privacy risk, aggregation risk, attribution risk, legal constraint, ethical constraint, contractual constraint, governance rule, review result, validation result, lifecycle change, or publication concern appears.

Source Material may become less restricted when review, redaction, de-identification, permission, expiration, governance approval, publication approval, or future governed handling rule permits broader use.

Privacy changes SHOULD preserve provenance where the change affects meaning, authority, validation, lifecycle state, compatibility, governance, migration, import, export, preservation, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

A Source Reference SHOULD NOT be silently removed merely because Source Material is private, restricted, redacted, access-controlled, or publication-limited.

Restricted Source Material MAY remain historically referenceable where it affects evidence, attribution, provenance, review history, validation history, lifecycle state, authority, governance, audit, migration, import, export, or downstream use.

A Source Reference SHOULD NOT falsely imply that Source Material is public, unrestricted, privacy-cleared, publication-ready, export-safe, agent-accessible, workflow-accessible, or indexable when privacy status is unknown, restricted, disputed, redacted, unavailable, or materially uncertain.

A Knowledge Record SHOULD NOT falsely imply that Source Material is public, unrestricted, privacy-cleared, publication-ready, export-safe, agent-accessible, workflow-accessible, indexable, reliable, authoritative, current, or complete when privacy status is unknown, restricted, false, superseded, unverifiable, disputed, or materially uncertain.

Source Privacy MAY affect evidence.

Where Source Material is private, restricted, redacted, access-controlled, attribution-limited, provenance-limited, publication-limited, export-limited, or agent-limited, evidence support MAY become review-limited, validation-limited, authority-limited, publication-limited, migration-limited, import-limited, export-limited, automation-limited, or governance-limited.

Such limitations SHOULD be preserved when they affect interpretation, validation, authority, lifecycle state, compatibility, governance, publication, or downstream use.

Source Privacy MAY affect attribution.

Where Source Privacy affects authorship, actor identification, source origin, publication context, ownership context, review context, evidence quality, provenance context, or attribution disclosure, that privacy condition SHOULD be preserved.

Attribution MUST NOT expose restricted people, organizations, systems, identifiers, source locations, review history, validation history, workflow history, agent context, or source context merely to improve traceability, citation, search, validation, publication, migration, import, export, automation, or implementation convenience.

Source Privacy MAY affect validation.

A validator SHOULD be able to determine whether Source Material is privacy-cleared enough to support required review, validation, migration, import, export, publication, preservation, synchronization, restoration, automation, agent processing, workflow routing, or downstream use.

Where Source Material is private, restricted, redacted, access-controlled, attribution-limited, provenance-limited, publication-limited, export-limited, agent-limited, workflow-limited, unavailable, or unverifiable, validation SHOULD preserve whether validation passed, failed, partially passed, was blocked, was deferred, or requires human review.

Validation MUST NOT expose restricted Source Material or restricted source-supporting context merely to prove that validation occurred.

Source Privacy MAY affect authority.

A source privacy condition MAY limit the authority, approved use, publication readiness, validation confidence, reviewability, or downstream use of source-derived knowledge.

Source Privacy does not automatically remove authority.

Source Privacy does not automatically create authority.

Authority impact SHOULD be governed through authority, validation, lifecycle, review, privacy, or future source-authority specifications.

Source Privacy MAY affect lifecycle state.

A Knowledge Record, Source Reference, relationship, validation result, provenance record, workflow output, agent output, import record, export record, migration record, or other governed entity MAY require review, correction, restriction, deprecation, supersession, archival, rejection, redaction, quarantine, or other lifecycle handling when Source Material becomes private, restricted, redacted, access-controlled, attribution-limited, provenance-limited, publication-limited, export-limited, agent-limited, workflow-limited, or otherwise privacy-sensitive.

Source Privacy does not automatically change lifecycle state unless a governed process or future specification defines that behavior.

Source Privacy MAY affect extraction and transformation.

Extraction and transformation processes SHOULD preserve privacy context where privacy affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, validation, authority, lifecycle state, compatibility, publication, preservation, restoration, synchronization, or downstream use.

Extraction or transformation MUST NOT silently convert restricted Source Material into apparently unrestricted extracted content, summarized content, transformed content, indexed content, embedded content, agent output, workflow output, or publication-ready content.

Where extraction or transformation changes privacy risk through aggregation, synthesis, interpretation, redaction, translation, classification, normalization, summarization, embedding, indexing, export, import, migration, workflow routing, agent processing, or implementation rendering, the stricter applicable privacy expectation SHOULD govern handling unless a future governed privacy specification defines a different compliant rule.

Source Privacy MAY affect migration, import, and export.

Migration, import, and export processes SHOULD preserve privacy context where privacy affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, validation, authority, lifecycle state, compatibility, preservation, restoration, synchronization, publication, automation, or downstream use.

A migration, import, or export process MUST NOT silently convert private, restricted, redacted, access-controlled, attribution-limited, provenance-limited, publication-limited, export-limited, agent-limited, workflow-limited, unavailable, or unverifiable Source Material into apparently public, unrestricted, privacy-cleared, publication-ready, export-safe, agent-accessible, workflow-accessible, or indexable material.

A migration, import, or export process SHOULD preserve whether Source Material was public, private, restricted, confidential, sensitive, redacted, partially redacted, access-controlled, permission-limited, publication-limited, export-limited, migration-limited, import-limited, agent-limited, workflow-limited, omitted, substituted, copied, linked, referenced, or marked uncertain.

Source Privacy MAY affect agents.

An agent MUST NOT access, summarize, extract, transform, validate, classify, embed, index, route, export, publish, synchronize, or otherwise process restricted Source Material, Source References, evidence, attribution, provenance, metadata, relationships, validation results, workflow context, import context, export context, migration context, or source-supporting context unless permitted by the applicable privacy classification, governance rule, workflow rule, user authorization, or future governed specification.

Agent convenience, search improvement, automation value, ranking improvement, summarization quality, validation value, relationship discovery, or implementation convenience MUST NOT override Source Privacy.

Agent-generated outputs SHOULD preserve privacy context where the output depends on restricted Source Material or restricted source-supporting context.

Agent output MUST NOT be treated as safe for broader use merely because the restricted source content is paraphrased, summarized, embedded, transformed, indexed, classified, or not directly quoted.

Source Privacy MAY affect workflows.

A workflow MUST NOT route, expose, summarize, extract, transform, validate, classify, index, export, publish, synchronize, or otherwise process restricted Source Material, Source References, evidence, attribution, provenance, metadata, relationships, validation results, agent context, import context, export context, migration context, or source-supporting context unless permitted by the applicable privacy classification, governance rule, workflow rule, user authorization, or future governed specification.

Workflow completion MUST NOT be treated as privacy clearance unless a future governed workflow specification explicitly defines that behavior.

Workflow routing MUST preserve privacy boundaries where routing affects access, visibility, exposure, review, validation, publication, export, migration, synchronization, restoration, or downstream use.

Source Privacy MAY be expressed through metadata.

Source Privacy metadata MAY describe:

- privacy state;
- privacy classification;
- visibility boundary;
- access expectation;
- permitted actors;
- restricted actors;
- permitted workflows;
- restricted workflows;
- permitted agents;
- restricted agents;
- redaction requirement;
- disclosure limitation;
- publication limitation;
- export limitation;
- import limitation;
- migration limitation;
- synchronization limitation;
- backup limitation;
- restoration limitation;
- indexing limitation;
- embedding limitation;
- extraction limitation;
- transformation limitation;
- summarization limitation;
- attribution limitation;
- provenance limitation;
- evidence limitation;
- source-location limitation;
- privacy assignment date where applicable;
- privacy assessor where applicable and permitted;
- privacy source;
- privacy review state;
- privacy validation state;
- privacy authority dependency;
- privacy reliability dependency;
- privacy availability dependency;
- privacy compatibility expectation;
- downstream-use limitation.

KS-0005 does not define exact Source Privacy metadata fields or exact privacy-state values.

A future specification MAY define exact source-privacy fields, allowed values, privacy classifications, access rules, exposure rules, redaction rules, agent-access rules, workflow-routing rules, indexing rules, embedding rules, publication rules, import formats, export formats, migration mappings, or serialization syntax.

Source Privacy MUST preserve privacy boundaries.

Source Privacy MUST NOT expose restricted Source Material, restricted source locations, restricted identifiers, restricted attribution, restricted relationships, restricted metadata, restricted provenance, restricted validation results, restricted privacy assessments, restricted review notes, restricted governance context, restricted source context, restricted conflict context, restricted evidence, restricted agent context, or restricted workflow context merely to improve traceability, review, validation, search, linking, indexing, publication, migration, import, export, automation, restoration, synchronization, or implementation convenience.

Where Source Privacy itself is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A system, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or implementation MUST NOT treat restricted privacy context as absent merely because the current actor lacks access.

Private is not the same as unavailable.

Restricted is not the same as missing.

Redacted is not the same as public.

Public is not the same as unrestricted for every use.

Available is not the same as privacy-cleared.

Reliable is not the same as safe to expose.

Authoritative is not the same as publication-ready.

Validated is not the same as privacy-approved.

Workflow completion is not the same as privacy clearance.

Agent access is not the same as downstream-use permission.

Privacy states SHOULD remain distinguishable where the distinction affects interpretation, validation, authority, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Privacy SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Privacy is present where required;
- Source Material is public, private, restricted, confidential, sensitive, redacted, partially redacted, access-controlled, publication-limited, export-limited, agent-limited, workflow-limited, or otherwise privacy-relevant where applicable;
- privacy state is distinguishable from availability;
- privacy state is distinguishable from reliability;
- privacy state is distinguishable from authority;
- privacy state is distinguishable from validation status;
- privacy state is distinguishable from truth;
- restricted Source Material is not falsely treated as missing;
- private Source Material is not falsely treated as unavailable;
- public Source Material is not falsely treated as unrestricted for every use;
- redacted Source Material is not falsely treated as fully public;
- privacy changes preserve provenance where required;
- Source References preserve enough context where source privacy changed;
- extraction and transformation preserve privacy context where required;
- migration, import, and export preserve privacy context where required;
- agent access remains within privacy boundaries;
- workflow routing remains within privacy boundaries;
- implementation behavior remains within privacy boundaries;
- Source Privacy remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Source Privacy SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, migrate, index, embed, summarize, or route Source Privacy in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, privacy confusion, compatibility confusion, or source confusion.

Source Privacy is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether Source Material or source-supporting context is public, private, restricted, confidential, sensitive, redacted, access-controlled, publication-limited, export-limited, import-limited, migration-limited, agent-limited, workflow-limited, implementation-limited, or otherwise privacy-relevant; whether that privacy state affects evidence, attribution, Source References, provenance, validation, authority, lifecycle state, reliability, availability, compatibility, migration, import, export, restoration, synchronization, preservation, publication, automation, agent behavior, workflow behavior, implementation behavior, or downstream use; and whether privacy meaning remains intact across time and implementation replacement.

## 21. Source Validation

Source Validation is the process of checking whether Source Material, Source References, evidence, attribution, provenance, extraction history, transformation history, source availability, source reliability, source authority, source privacy, import provenance, export provenance, migration provenance, compatibility expectations, and other source-supporting context satisfy applicable standards, specifications, governance rules, privacy expectations, validation expectations, or downstream-use requirements.

Source Validation exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether source-reference and provenance behavior is present, interpretable, reviewable, privacy-respecting, compatible, and sufficient for the intended use.

Source Validation SHALL be preserved where validation affects meaning, interpretation, evidence, attribution, authority, privacy, lifecycle state, relationships, compatibility, governance, publication, migration, import, export, preservation, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Validation MAY identify or describe whether:

- Source Material is distinguishable from Knowledge Records;
- Source References are present where required;
- Source References identify or describe Source Material where access is permitted;
- provenance is present where required;
- evidence is connected to the governed entity it supports where applicable;
- attribution is present where required;
- extraction provenance is present where required;
- transformation provenance is present where required;
- human-created provenance is distinguishable where required;
- agent-generated provenance is distinguishable where required;
- workflow-generated provenance is distinguishable where required;
- import provenance is present where required;
- export provenance is present where required;
- migration provenance is present where required;
- source availability is represented where required;
- source reliability is represented where required;
- source authority is represented where required;
- source privacy is represented where required;
- Source References remain compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement;
- privacy boundaries are preserved;
- validation passed;
- validation failed;
- validation partially passed;
- validation was blocked;
- validation was deferred;
- validation requires human review;
- validation requires agent review;
- validation requires workflow review;
- validation requires correction;
- validation requires restriction;
- validation requires migration repair;
- validation requires import repair;
- validation requires export repair;
- validation requires future specification handling;
- other validation context affects interpretation.

Source Validation is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

Source Validation checks whether Source Material and source-supporting context satisfy applicable expectations.

Source Validation is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

Source Validation checks whether the Source Reference is present, meaningful, durable, reviewable, privacy-respecting, compatible, and sufficient for the intended use.

Source Validation is not the same as provenance.

Provenance explains origin, source use, transformation, review, validation, movement, or change context.

Source Validation checks whether provenance is present, sufficient, distinguishable, interpretable, privacy-respecting, compatible, and reviewable where required.

Source Validation is not the same as Source Availability.

Source Availability describes whether Source Material or source-supporting context can be accessed, reviewed, validated, preserved, migrated, imported, exported, or otherwise used.

Source Validation may check Source Availability.

Availability alone does not determine whether validation passes.

Source Validation is not the same as Source Reliability.

Source Reliability describes trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength.

Source Validation may assess Source Reliability.

Reliability alone does not determine whether validation passes.

Source Validation is not the same as Source Authority.

Source Authority describes governance weight, official status, review status, approved use, or interpretive relevance.

Source Validation may check Source Authority.

Authority alone does not determine whether validation passes.

Source Validation is not the same as Source Privacy.

Source Privacy describes access, exposure, visibility, routing, publication, indexing, agent-processing, workflow-processing, import, export, migration, synchronization, backup, restoration, and downstream-use boundaries.

Source Validation may check Source Privacy.

Privacy classification alone does not determine whether validation passes.

Source Validation is not the same as truth.

A validation result may show that a Source Reference, provenance record, evidence record, attribution record, metadata record, relationship, or source-supporting context satisfies a standard or specification.

Validation does not automatically prove that Source Material is true, complete, current, unbiased, authoritative, privacy-cleared, publication-ready, or sufficient for every use.

Source Validation is not the same as approval.

A validation result may support approval.

Validation does not automatically approve knowledge unless a governed approval rule, lifecycle rule, workflow rule, authority rule, or future specification explicitly defines that behavior.

Source Validation is not the same as authority.

A validation result may support authority assessment.

Validation does not automatically create authority unless a governed authority rule, lifecycle rule, workflow rule, approval rule, or future specification explicitly defines that behavior.

Source Validation SHOULD preserve enough context to determine:

- what was validated;
- what validation scope applied;
- what standard or specification was checked;
- what validation rule or expectation applied;
- who or what performed validation where applicable;
- when validation occurred where applicable;
- whether validation was human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, or implementation-generated;
- what Source Material was checked;
- what Source References were checked;
- what provenance was checked;
- what evidence was checked;
- what attribution was checked;
- what availability context was checked;
- what reliability context was checked;
- what authority context was checked;
- what privacy context was checked;
- what compatibility context was checked;
- whether validation passed;
- whether validation failed;
- whether validation partially passed;
- whether validation was blocked;
- whether validation was deferred;
- whether validation requires correction;
- whether validation requires review;
- whether validation affects lifecycle state;
- whether validation affects authority;
- whether validation affects privacy handling;
- whether validation affects publication, migration, import, export, restoration, synchronization, preservation, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Validation MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, historically preserved, imported, exported, or migrated.

Where Source Validation is incomplete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, imported, exported, or migrated, that condition SHOULD be represented or preserved when it affects interpretation, authority, privacy, lifecycle state, compatibility, governance, publication, preservation, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Validation MAY change over time.

A prior validation result may become stale when Source Material changes, Source References break, provenance changes, metadata changes, relationships change, privacy expectations change, authority expectations change, standards change, specifications change, validation rules change, workflows change, agents change, implementations change, migration occurs, import occurs, export occurs, restoration occurs, synchronization occurs, or source availability changes.

Validation changes SHOULD preserve provenance where the change affects meaning, authority, privacy, lifecycle state, compatibility, governance, migration, import, export, preservation, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

A Source Reference SHOULD NOT be silently removed merely because Source Validation fails, is blocked, is deferred, is partial, is stale, is disputed, or requires review.

A failed, blocked, deferred, partial, stale, disputed, or review-required Source Validation result MAY remain historically referenceable where it affects evidence, attribution, provenance, review history, lifecycle state, authority, governance, audit, migration, import, export, or downstream use.

A Source Reference SHOULD NOT falsely imply that Source Validation passed when validation is unknown, failed, blocked, deferred, partial, stale, disputed, restricted, unavailable, or materially uncertain.

A Knowledge Record SHOULD NOT falsely imply that Source Material, Source References, evidence, attribution, provenance, availability, reliability, authority, privacy, or compatibility have been validated when validation is unknown, failed, blocked, deferred, partial, stale, disputed, restricted, unavailable, or materially uncertain.

Source Validation MAY affect evidence.

Where validation fails, partially passes, is blocked, is deferred, is stale, or requires review, evidence support MAY become limited, uncertain, review-limited, authority-limited, publication-limited, migration-limited, import-limited, export-limited, automation-limited, or governance-limited.

Such limitations SHOULD be preserved when they affect interpretation, authority, lifecycle state, privacy, compatibility, governance, publication, or downstream use.

Source Validation MAY affect attribution.

Where validation affects authorship, actor identification, source origin, publication context, ownership context, review context, evidence quality, provenance context, or attribution disclosure, that validation condition SHOULD be preserved.

Source Validation MAY affect authority.

A source validation condition MAY limit the authority, approved use, publication readiness, validation confidence, reviewability, or downstream use of source-derived knowledge.

Source Validation does not automatically remove authority.

Source Validation does not automatically create authority.

Authority impact SHOULD be governed through authority, validation, lifecycle, review, privacy, or future source-authority specifications.

Source Validation MAY affect lifecycle state.

A Knowledge Record, Source Reference, relationship, validation result, provenance record, workflow output, agent output, import record, export record, migration record, or other governed entity MAY require review, correction, restriction, deprecation, supersession, archival, rejection, redaction, quarantine, repair, or other lifecycle handling when Source Validation fails, partially passes, is blocked, is deferred, becomes stale, becomes disputed, or requires review.

Source Validation does not automatically change lifecycle state unless a governed process or future specification defines that behavior.

Source Validation MAY affect extraction and transformation.

Extraction and transformation processes SHOULD preserve validation context where validation affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, authority, privacy, lifecycle state, compatibility, publication, preservation, restoration, synchronization, or downstream use.

Extraction or transformation MUST NOT silently convert unvalidated, failed, partial, blocked, deferred, stale, disputed, or review-required source context into apparently validated extracted content, summarized content, transformed content, indexed content, embedded content, agent output, workflow output, or publication-ready content.

Source Validation MAY affect migration, import, and export.

Migration, import, and export processes SHOULD preserve validation context where validation affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, authority, privacy, lifecycle state, compatibility, preservation, restoration, synchronization, publication, automation, or downstream use.

A migration, import, or export process MUST NOT silently convert unvalidated, failed, partial, blocked, deferred, stale, disputed, restricted, unavailable, or review-required Source Material into apparently validated, complete, compatible, publication-ready, export-safe, agent-accessible, workflow-accessible, or indexable material.

A migration, import, or export process SHOULD preserve whether Source Material, Source References, evidence, attribution, provenance, metadata, relationships, availability, reliability, authority, privacy, or compatibility were validated, unvalidated, partially validated, failed, blocked, deferred, stale, disputed, omitted, redacted, substituted, copied, linked, referenced, or marked uncertain.

Source Validation MAY affect agents.

An agent MAY perform source validation where permitted by privacy classification, governance rule, workflow rule, user authorization, or future governed specification.

Agent validation MUST remain distinguishable from human validation, workflow approval, document authority, privacy clearance, publication readiness, truth, and final approval unless a future governed specification explicitly defines otherwise.

Agent validation SHOULD preserve agent attribution, instruction context, input context, validation method, validation scope, validation result, uncertainty, limitations, and review requirements where agent activity affects meaning, authority, privacy, lifecycle state, publication, governance, or downstream use.

Agent-generated validation output MUST NOT be treated as human-reviewed, approved, authoritative, complete, accurate, privacy-cleared, publication-ready, or final merely because an agent produced it.

Source Validation MAY affect workflows.

A workflow MAY perform, route, record, review, approve, reject, defer, block, repair, or preserve source validation where permitted by privacy classification, governance rule, workflow rule, user authorization, or future governed specification.

Workflow validation MUST remain distinguishable from human validation, human approval, source authority, privacy clearance, publication readiness, truth, and final approval unless a future governed workflow specification explicitly defines otherwise.

Workflow completion MUST NOT be treated as validation success unless a future governed workflow specification explicitly defines that behavior.

Source Validation MAY be expressed through metadata.

Source Validation metadata MAY describe:

- validation state;
- validation result;
- validation scope;
- validation target;
- validation standard;
- validation specification;
- validation rule;
- validation profile where applicable;
- validation actor;
- validation method;
- validation date where applicable;
- validation evidence;
- validation limitation;
- validation confidence where applicable;
- validation warning;
- validation error;
- validation blocker;
- validation deferral;
- validation review requirement;
- validation repair requirement;
- validation privacy condition;
- validation authority condition;
- validation lifecycle effect;
- validation compatibility expectation;
- source availability validation;
- source reliability validation;
- source authority validation;
- source privacy validation;
- Source Reference validation;
- provenance validation;
- evidence validation;
- attribution validation;
- extraction validation;
- transformation validation;
- import validation;
- export validation;
- migration validation;
- downstream-use limitation.

KS-0005 does not define exact Source Validation metadata fields or exact validation-state values.

A future specification MAY define exact source-validation fields, allowed values, validation profiles, validation rules, validation result vocabularies, validation error codes, validation warning codes, review rules, repair rules, lifecycle mappings, import formats, export formats, migration mappings, or serialization syntax.

Source Validation MUST preserve privacy boundaries.

Source Validation MUST NOT expose restricted Source Material, restricted source locations, restricted identifiers, restricted attribution, restricted relationships, restricted metadata, restricted provenance, restricted validation results, restricted privacy assessments, restricted review notes, restricted governance context, restricted source context, restricted conflict context, restricted evidence, restricted agent context, or restricted workflow context merely to prove validation, improve traceability, review, search, linking, indexing, publication, migration, import, export, automation, restoration, synchronization, or implementation convenience.

Where Source Validation itself is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A system, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or implementation MUST NOT treat restricted validation context as absent merely because the current actor lacks access.

Validated is not the same as true.

Validated is not the same as authoritative.

Validated is not the same as reliable.

Validated is not the same as privacy-cleared.

Validated is not the same as publication-ready.

Validated is not the same as approved.

Validation success is not the same as workflow completion.

Validation failure is not the same as source invalidity.

Partial validation is not the same as full validation.

Blocked validation is not the same as failed validation.

Deferred validation is not the same as approved use.

Agent validation is not the same as human validation.

Workflow validation is not the same as human approval.

Validation states SHOULD remain distinguishable where the distinction affects interpretation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Validation SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Validation is present where required;
- validation scope is clear where required;
- validation target is clear where required;
- validation result is clear where required;
- validation actor is clear where attribution affects interpretation;
- validation method is clear where method affects interpretation;
- validation state is distinguishable from truth;
- validation state is distinguishable from availability;
- validation state is distinguishable from reliability;
- validation state is distinguishable from authority;
- validation state is distinguishable from privacy classification;
- validation state is distinguishable from approval;
- validation state is distinguishable from publication readiness;
- validation failure is not falsely treated as source invalidity;
- partial validation is not falsely treated as full validation;
- blocked validation is not falsely treated as failed validation;
- deferred validation is not falsely treated as approved use;
- agent validation is not falsely treated as human validation;
- workflow validation is not falsely treated as human approval;
- validation changes preserve provenance where required;
- Source References preserve enough context where source validation changed;
- extraction and transformation preserve validation context where required;
- migration, import, and export preserve validation context where required;
- agent validation remains within privacy and authority boundaries;
- workflow validation remains within privacy and authority boundaries;
- implementation behavior remains within validation boundaries;
- Source Validation remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Source Validation SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, migrate, index, embed, summarize, route, approve, or reject Source Validation in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, validation confusion, compatibility confusion, or source confusion.

Source Validation is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether Source Material, Source References, evidence, attribution, provenance, extraction history, transformation history, source availability, source reliability, source authority, source privacy, import provenance, export provenance, migration provenance, compatibility expectations, and other source-supporting context were validated, unvalidated, partially validated, failed, blocked, deferred, stale, disputed, restricted, unavailable, or review-required; whether that validation state affects evidence, attribution, Source References, provenance, authority, lifecycle state, privacy, reliability, availability, compatibility, migration, import, export, restoration, synchronization, preservation, publication, automation, agent behavior, workflow behavior, implementation behavior, or downstream use; and whether validation meaning remains intact across time and implementation replacement.

## 22. Source Compatibility

Source Compatibility is the condition describing whether Source Material, Source References, evidence, attribution, provenance, extraction history, transformation history, source availability, source reliability, source authority, source privacy, source validation, import provenance, export provenance, migration provenance, and other source-supporting context remain meaningful, portable, reviewable, privacy-respecting, validatable, interpretable, and usable across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, backup, archive, publication, and implementation replacement.

Source Compatibility exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether source-reference and provenance behavior remains intact when tools, formats, storage systems, workflows, agents, validators, archives, repositories, or implementations change.

Source Compatibility SHALL be preserved where compatibility affects meaning, interpretation, evidence, attribution, authority, privacy, lifecycle state, validation, relationships, governance, publication, migration, import, export, preservation, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Compatibility MAY identify or describe whether Source Material or source-supporting context is:

- compatible;
- partially compatible;
- incompatible;
- compatibility-limited;
- migration-compatible;
- import-compatible;
- export-compatible;
- storage-compatible;
- archive-compatible;
- restoration-compatible;
- synchronization-compatible;
- validation-compatible;
- workflow-compatible;
- agent-compatible;
- implementation-compatible;
- human-readable;
- AI-readable;
- machine-readable;
- portable;
- partially portable;
- not portable;
- reviewable;
- partially reviewable;
- not reviewable;
- privacy-preserving;
- privacy-limited;
- source-reference-compatible;
- provenance-compatible;
- metadata-compatible;
- relationship-compatible;
- lifecycle-compatible;
- authority-compatible;
- otherwise compatibility-relevant.

Source Compatibility is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

Source Compatibility describes whether that material and its source-supporting context remain meaningful, portable, reviewable, privacy-respecting, validatable, and interpretable across changes in storage, tooling, workflows, agents, validators, migration, import, export, restoration, synchronization, or implementation.

Source Compatibility is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

Source Compatibility describes whether that connection remains meaningful when the referenced source is renamed, moved, copied, archived, restricted, migrated, imported, exported, backed up, restored, synchronized, reindexed, transformed, validated, processed by an agent, processed by a workflow, or accessed through a different implementation.

Source Compatibility is not the same as Source Availability.

Source Availability describes whether Source Material can be accessed, reviewed, validated, preserved, migrated, imported, exported, or otherwise used.

Source Compatibility describes whether source-reference and provenance meaning remains interpretable and portable across change.

Available Source Material is not automatically compatible.

Unavailable Source Material may still remain compatible where enough Source Reference, provenance, archival, validation, or migration context is preserved.

Source Compatibility is not the same as Source Reliability.

Source Reliability describes source quality, trustworthiness, freshness, completeness, uncertainty, limitation, conflict, or evidentiary strength.

Source Compatibility describes whether the source-supporting context can survive movement, transformation, implementation replacement, workflow activity, agent activity, validation, import, export, migration, restoration, synchronization, or storage replacement without losing governed meaning.

Reliable Source Material is not automatically compatible.

Compatible Source Material is not automatically reliable.

Source Compatibility is not the same as Source Authority.

Source Authority describes governance weight, official status, review status, approved use, or interpretive relevance.

Source Compatibility describes preservation of meaning across systems, formats, workflows, agents, validators, and implementations.

Authoritative Source Material is not automatically compatible.

Compatible Source Material is not automatically authoritative.

Source Compatibility is not the same as Source Privacy.

Source Privacy describes access, exposure, visibility, routing, publication, indexing, agent-processing, workflow-processing, import, export, migration, synchronization, backup, restoration, and downstream-use boundaries.

Source Compatibility describes whether those privacy boundaries remain preserved and interpretable across change.

A compatibility process MUST NOT treat privacy exposure as an acceptable compatibility strategy.

Source Compatibility is not the same as Source Validation.

Source Validation checks whether source-reference and provenance behavior satisfies applicable standards, specifications, governance rules, privacy expectations, validation expectations, or downstream-use requirements.

Source Compatibility may be checked by validation.

A validation result may describe compatibility.

However, validation does not automatically guarantee future compatibility unless the validated scope explicitly includes the relevant compatibility expectations.

Source Compatibility SHOULD be represented where compatibility affects interpretation, evidence, attribution, Source References, provenance, validation, authority, lifecycle state, privacy, migration, import, export, governance, publication, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Compatibility SHOULD preserve enough context to determine:

- what compatibility expectation applies;
- what Source Material or source-supporting context is affected;
- what system, format, repository, vault, archive, workflow, agent, validator, storage environment, implementation, import process, export process, or migration process is involved;
- whether compatibility was human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, validated, or implementation-generated;
- whether Source References remain meaningful;
- whether provenance remains meaningful;
- whether evidence remains connected to the governed entity it supports;
- whether attribution remains interpretable;
- whether extraction history remains interpretable;
- whether transformation history remains interpretable;
- whether source availability context remains interpretable;
- whether source reliability context remains interpretable;
- whether source authority context remains interpretable;
- whether source privacy context remains preserved;
- whether source validation context remains interpretable;
- whether metadata remains within metadata role boundaries;
- whether relationships remain within relationship boundaries;
- whether Object Identity boundaries remain preserved;
- whether compatibility is complete, partial, restricted, uncertain, inferred, disputed, stale, deprecated, superseded, lossy, or review-required;
- whether compatibility affects publication, migration, import, export, restoration, synchronization, preservation, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Compatibility MAY be complete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, historically preserved, imported, exported, migrated, validated, unvalidated, or review-required.

Where Source Compatibility is incomplete, partial, restricted, uncertain, inferred, unavailable, disputed, stale, superseded, deprecated, imported, exported, migrated, validated, unvalidated, or review-required, that condition SHOULD be represented or preserved when it affects interpretation, authority, privacy, lifecycle state, validation, governance, publication, preservation, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Compatibility MAY change over time.

Source Material, Source References, evidence, attribution, provenance, metadata, relationships, validation results, privacy expectations, authority expectations, storage formats, implementation behavior, workflow behavior, agent behavior, import behavior, export behavior, migration behavior, synchronization behavior, or restoration behavior may become more compatible or less compatible as standards, specifications, tools, repositories, workflows, agents, validators, and implementations evolve.

Compatibility changes SHOULD preserve provenance where the change affects meaning, authority, privacy, validation, lifecycle state, governance, migration, import, export, preservation, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

A Source Reference SHOULD NOT be silently removed merely because compatibility fails, is partial, is stale, is uncertain, is restricted, or requires review.

A failed, partial, stale, uncertain, restricted, or review-required compatibility condition MAY remain historically referenceable where it affects evidence, attribution, provenance, validation history, lifecycle state, authority, governance, audit, migration, import, export, or downstream use.

A Source Reference SHOULD NOT falsely imply that Source Compatibility is preserved when compatibility is unknown, failed, partial, stale, disputed, restricted, unavailable, or materially uncertain.

A Knowledge Record SHOULD NOT falsely imply that Source Material, Source References, evidence, attribution, provenance, availability, reliability, authority, privacy, validation, or compatibility remain fully portable, reviewable, preserved, or implementation-independent when compatibility is unknown, failed, partial, stale, disputed, restricted, unavailable, lossy, or materially uncertain.

Source Compatibility MAY affect evidence.

Where compatibility fails, partially passes, is blocked, is stale, is lossy, or requires review, evidence support MAY become limited, uncertain, review-limited, validation-limited, authority-limited, publication-limited, migration-limited, import-limited, export-limited, automation-limited, or governance-limited.

Such limitations SHOULD be preserved when they affect interpretation, authority, lifecycle state, privacy, validation, governance, publication, or downstream use.

Source Compatibility MAY affect attribution.

Where compatibility affects authorship, actor identification, source origin, publication context, ownership context, review context, evidence quality, provenance context, or attribution disclosure, that compatibility condition SHOULD be preserved.

Source Compatibility MAY affect validation.

A validator SHOULD be able to determine whether Source Material, Source References, evidence, attribution, provenance, extraction history, transformation history, availability context, reliability context, authority context, privacy context, and validation context remain compatible enough to support required review, migration, import, export, publication, preservation, restoration, synchronization, automation, agent processing, workflow routing, or downstream use.

Where Source Compatibility is failed, partial, blocked, stale, lossy, restricted, unavailable, disputed, or review-required, validation SHOULD preserve whether validation passed, failed, partially passed, was blocked, was deferred, or requires human review.

Source Compatibility MAY affect authority.

A source compatibility condition MAY limit the authority, approved use, publication readiness, validation confidence, reviewability, portability, or downstream use of source-derived knowledge.

Source Compatibility does not automatically remove authority.

Source Compatibility does not automatically create authority.

Authority impact SHOULD be governed through authority, validation, lifecycle, review, privacy, compatibility, or future source-authority specifications.

Source Compatibility MAY affect lifecycle state.

A Knowledge Record, Source Reference, relationship, validation result, provenance record, workflow output, agent output, import record, export record, migration record, or other governed entity MAY require review, correction, restriction, deprecation, supersession, archival, rejection, redaction, quarantine, repair, migration repair, import repair, export repair, compatibility repair, or other lifecycle handling when Source Compatibility fails, partially passes, is blocked, becomes stale, becomes disputed, becomes lossy, or requires review.

Source Compatibility does not automatically change lifecycle state unless a governed process or future specification defines that behavior.

Source Compatibility MAY affect extraction and transformation.

Extraction and transformation processes SHOULD preserve compatibility context where compatibility affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, validation, authority, privacy, lifecycle state, publication, preservation, restoration, synchronization, or downstream use.

Extraction or transformation MUST NOT silently convert incompatible, partially compatible, lossy, stale, disputed, restricted, unavailable, or review-required source context into apparently compatible extracted content, summarized content, transformed content, indexed content, embedded content, agent output, workflow output, or publication-ready content.

Source Compatibility MAY affect migration, import, and export.

Migration, import, and export processes SHOULD preserve compatibility context where compatibility affects meaning, Source References, provenance, metadata, relationships, evidence, attribution, validation, authority, privacy, lifecycle state, preservation, restoration, synchronization, publication, automation, or downstream use.

A migration, import, or export process MUST NOT silently convert incompatible, partially compatible, lossy, stale, disputed, restricted, unavailable, or review-required Source Material into apparently compatible, complete, portable, publication-ready, export-safe, agent-accessible, workflow-accessible, or implementation-independent material.

A migration, import, or export process SHOULD preserve whether Source Material, Source References, evidence, attribution, provenance, metadata, relationships, availability, reliability, authority, privacy, validation, or compatibility were compatible, partially compatible, incompatible, unvalidated, partially validated, failed, blocked, deferred, stale, disputed, omitted, redacted, substituted, copied, linked, referenced, mapped, transformed, repaired, or marked uncertain.

Source Compatibility MAY affect agents.

An agent MAY assess, preserve, repair, or propose compatibility context where permitted by privacy classification, governance rule, workflow rule, user authorization, or future governed specification.

Agent compatibility assessment MUST remain distinguishable from human validation, workflow approval, document authority, privacy clearance, publication readiness, truth, final approval, and guaranteed portability unless a future governed specification explicitly defines otherwise.

Agent-generated compatibility output MUST NOT be treated as human-reviewed, approved, authoritative, complete, accurate, privacy-cleared, publication-ready, portable, or final merely because an agent produced it.

Source Compatibility MAY affect workflows.

A workflow MAY assess, route, record, review, approve, reject, defer, block, repair, or preserve source compatibility where permitted by privacy classification, governance rule, workflow rule, user authorization, or future governed specification.

Workflow compatibility assessment MUST remain distinguishable from human validation, human approval, source authority, privacy clearance, publication readiness, truth, final approval, and guaranteed portability unless a future governed workflow specification explicitly defines otherwise.

Workflow completion MUST NOT be treated as compatibility success unless a future governed workflow specification explicitly defines that behavior.

Source Compatibility MAY be expressed through metadata.

Source Compatibility metadata MAY describe:

- compatibility state;
- compatibility result;
- compatibility scope;
- compatibility target;
- compatibility standard;
- compatibility specification;
- compatibility profile where applicable;
- compatibility actor;
- compatibility method;
- compatibility date where applicable;
- compatibility evidence;
- compatibility limitation;
- compatibility warning;
- compatibility error;
- compatibility blocker;
- compatibility deferral;
- compatibility review requirement;
- compatibility repair requirement;
- compatibility privacy condition;
- compatibility authority condition;
- compatibility lifecycle effect;
- source availability compatibility;
- source reliability compatibility;
- source authority compatibility;
- source privacy compatibility;
- source validation compatibility;
- Source Reference compatibility;
- provenance compatibility;
- evidence compatibility;
- attribution compatibility;
- extraction compatibility;
- transformation compatibility;
- import compatibility;
- export compatibility;
- migration compatibility;
- restoration compatibility;
- synchronization compatibility;
- implementation compatibility;
- downstream-use limitation.

KS-0005 does not define exact Source Compatibility metadata fields or exact compatibility-state values.

A future specification MAY define exact source-compatibility fields, allowed values, compatibility profiles, compatibility rules, compatibility result vocabularies, compatibility error codes, compatibility warning codes, review rules, repair rules, lifecycle mappings, import formats, export formats, migration mappings, restoration mappings, synchronization mappings, or serialization syntax.

Source Compatibility MUST preserve privacy boundaries.

Source Compatibility MUST NOT expose restricted Source Material, restricted source locations, restricted identifiers, restricted attribution, restricted relationships, restricted metadata, restricted provenance, restricted validation results, restricted privacy assessments, restricted review notes, restricted governance context, restricted source context, restricted conflict context, restricted evidence, restricted agent context, restricted workflow context, or restricted compatibility context merely to prove compatibility, improve traceability, review, search, linking, indexing, publication, migration, import, export, automation, restoration, synchronization, or implementation convenience.

Where Source Compatibility itself is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A system, workflow, agent, validator, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or implementation MUST NOT treat restricted compatibility context as absent merely because the current actor lacks access.

Compatible is not the same as true.

Compatible is not the same as authoritative.

Compatible is not the same as reliable.

Compatible is not the same as available.

Compatible is not the same as privacy-cleared.

Compatible is not the same as publication-ready.

Compatible is not the same as approved.

Compatible is not the same as lossless.

Portable is not the same as complete.

Human-readable is not the same as AI-readable.

AI-readable is not the same as validated.

Validation success is not the same as future compatibility.

Workflow completion is not the same as compatibility success.

Agent compatibility assessment is not the same as human validation.

Compatibility states SHOULD remain distinguishable where the distinction affects interpretation, authority, privacy, lifecycle state, validation, governance, publication, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Source Compatibility SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Compatibility is present where required;
- compatibility scope is clear where required;
- compatibility target is clear where required;
- compatibility result is clear where required;
- compatibility actor is clear where attribution affects interpretation;
- compatibility method is clear where method affects interpretation;
- compatibility state is distinguishable from truth;
- compatibility state is distinguishable from availability;
- compatibility state is distinguishable from reliability;
- compatibility state is distinguishable from authority;
- compatibility state is distinguishable from privacy classification;
- compatibility state is distinguishable from approval;
- compatibility state is distinguishable from publication readiness;
- compatibility state is distinguishable from losslessness;
- partial compatibility is not falsely treated as full compatibility;
- lossy compatibility is not falsely treated as lossless compatibility;
- blocked compatibility is not falsely treated as failed compatibility;
- deferred compatibility is not falsely treated as approved use;
- agent compatibility assessment is not falsely treated as human validation;
- workflow compatibility assessment is not falsely treated as human approval;
- compatibility changes preserve provenance where required;
- Source References preserve enough context where source compatibility changed;
- extraction and transformation preserve compatibility context where required;
- migration, import, and export preserve compatibility context where required;
- restoration and synchronization preserve compatibility context where required;
- agent compatibility behavior remains within privacy and authority boundaries;
- workflow compatibility behavior remains within privacy and authority boundaries;
- implementation behavior remains within compatibility boundaries;
- Source Compatibility remains meaningful across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Source Compatibility SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, migrate, index, embed, summarize, route, approve, reject, validate, or repair Source Compatibility in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, compatibility confusion, portability confusion, or source confusion.

Source Compatibility is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine whether Source Material, Source References, evidence, attribution, provenance, extraction history, transformation history, source availability, source reliability, source authority, source privacy, source validation, import provenance, export provenance, migration provenance, and other source-supporting context remain compatible, partially compatible, incompatible, compatibility-limited, portable, partially portable, reviewable, privacy-preserving, validatable, interpretable, lossy, lossless, stale, disputed, restricted, unavailable, or review-required; whether that compatibility state affects evidence, attribution, Source References, provenance, authority, lifecycle state, privacy, reliability, availability, validation, migration, import, export, restoration, synchronization, preservation, publication, automation, agent behavior, workflow behavior, implementation behavior, or downstream use; and whether compatibility meaning remains intact across time and implementation replacement.

## 23. Implementation Boundaries

Implementation Boundaries define the limits that software, vaults, databases, file systems, interfaces, agent systems, workflow environments, validation tools, citation tools, archive tools, synchronization tools, backup tools, restoration tools, import tools, export tools, migration tools, indexes, search systems, graph systems, embedding systems, and other implementations MUST respect when representing, storing, displaying, processing, validating, migrating, importing, exporting, synchronizing, restoring, or otherwise using Source Material, Source References, provenance, evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, source validation, source compatibility, or other source-supporting context.

Implementation Boundaries exist so that source-reference and provenance meaning remains governed by The Brain Standard rather than by application behavior, folder placement, filenames, database internals, plugin behavior, search ranking, backlink behavior, graph layout, embedding behavior, agent memory, workflow memory, user interface state, synchronization behavior, archive behavior, backup behavior, restoration behavior, import behavior, export behavior, migration behavior, or implementation-specific convenience.

Implementation Boundaries SHALL be preserved where implementation behavior affects meaning, interpretation, evidence, attribution, authority, privacy, lifecycle state, validation, relationships, compatibility, governance, publication, migration, import, export, preservation, restoration, synchronization, automation, agent behavior, workflow behavior, or downstream use.

An implementation MAY represent Source Material, Source References, provenance, evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, source validation, source compatibility, or other source-supporting context through:

- files;
- folders;
- Markdown;
- front matter;
- sidecar files;
- databases;
- records;
- indexes;
- search systems;
- graph structures;
- relationship stores;
- object stores;
- source archives;
- citation systems;
- validation systems;
- workflow systems;
- agent systems;
- synchronization systems;
- backup systems;
- restoration systems;
- import systems;
- export systems;
- migration systems;
- user interfaces;
- APIs;
- other implementation mechanisms.

These mechanisms MAY support storage, retrieval, display, editing, linking, validation, review, migration, import, export, synchronization, restoration, publication, automation, or daily use.

These mechanisms MUST NOT define standard-level source-reference or provenance meaning by themselves.

Implementation behavior is not the same as Source Material.

Source Material is the material used as evidence, input, origin, context, attribution, contradiction, or support.

An implementation may store, display, copy, archive, index, synchronize, migrate, import, export, restore, or process Source Material.

The implementation does not become the Source Material merely because it stores, displays, indexes, or processes it.

Implementation behavior is not the same as a Source Reference.

A Source Reference connects a governed entity to Source Material.

A link, backlink, file path, URL, citation string, database row, search result, graph edge, embedded vector, archive pointer, plugin link, user interface element, or implementation-specific identifier MAY support a Source Reference.

Those mechanisms MUST NOT replace the Source Reference unless they satisfy Source Reference requirements or a future governed specification defines compliant conversion behavior.

Implementation behavior is not the same as provenance.

Provenance explains origin, source use, transformation, review, validation, movement, or change context.

An implementation may record, display, infer, index, migrate, import, export, or validate provenance.

The implementation MUST NOT silently create, discard, collapse, reinterpret, overwrite, regenerate, detach, anonymize, deanonymize, expose, or hide provenance where provenance affects meaning, authority, privacy, validation, lifecycle state, relationships, Source References, compatibility, governance, or downstream use.

Implementation behavior is not the same as metadata.

Metadata is explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, source-reference, or operational context associated with a governed entity.

Implementation metadata MAY support standard metadata.

Implementation metadata MUST NOT silently redefine Object Identity, relationship meaning, lifecycle state, authority level, privacy classification, validation status, Source References, provenance, workflow state, agent state, source availability, source reliability, source authority, source privacy, source validation, or source compatibility.

Implementation behavior is not the same as validation.

An implementation may run checks, display warnings, enforce required fields, produce reports, block export, flag missing references, or support validators.

Implementation checks MUST NOT be treated as complete Source Validation unless the validation scope, rule, actor, method, result, and limitation are represented according to applicable standards or future governed validation specifications.

Implementation behavior is not the same as authority.

An implementation may rank, sort, recommend, highlight, prioritize, approve a workflow step, or mark content as complete.

Those behaviors MUST NOT create Source Authority, document authority, lifecycle approval, privacy clearance, publication readiness, or truth unless a governed authority rule, lifecycle rule, workflow rule, or future specification explicitly defines that behavior.

Implementation behavior is not the same as privacy clearance.

An implementation may display, hide, redact, filter, encrypt, restrict, synchronize, route, export, or process source-supporting context.

Those behaviors MUST NOT imply that Source Material, Source References, provenance, evidence, attribution, validation results, agent outputs, workflow outputs, imports, exports, migrations, backups, archives, or synchronized copies are public, unrestricted, privacy-cleared, publication-ready, export-safe, agent-accessible, workflow-accessible, indexable, or safe for downstream use.

Implementation behavior MUST preserve Source Material and Knowledge Record boundaries.

A compliant implementation MUST NOT treat Source Material and Knowledge Records as the same entity merely because they are stored in the same folder, displayed in the same interface, indexed together, linked together, synchronized together, exported together, imported together, migrated together, restored together, processed by the same agent, or routed through the same workflow.

A compliant implementation MUST NOT treat a Knowledge Record as original Source Material merely because it quotes, summarizes, extracts from, transforms, interprets, classifies, validates, or discusses Source Material.

A compliant implementation MUST NOT treat Source Material as a Knowledge Record merely because it is stored inside a compliant repository, given metadata, indexed, linked, cited, archived, migrated, imported, exported, or processed by an agent or workflow.

Implementation behavior MUST preserve Object Identity boundaries.

A compliant implementation MUST NOT use filenames, folder paths, URLs, database rows, application-specific identifiers, search results, graph positions, plugin identifiers, interface state, archive paths, synchronization identifiers, backup identifiers, import identifiers, export identifiers, migration identifiers, or embedding identifiers as stable Object Identity unless a future governed specification defines a compliant identity relationship.

Where an implementation uses implementation-specific identifiers, the implementation SHOULD preserve enough context to distinguish them from stable Object Identity, Source Identifiers, external identifiers, legacy identifiers, import identifiers, export identifiers, migration identifiers, archive identifiers, backup identifiers, and restoration identifiers.

Implementation behavior MUST preserve Source Reference boundaries.

A compliant implementation MUST NOT silently convert a citation, URL, file path, backlink, database reference, graph edge, search result, archive pointer, embedded vector, plugin link, or implementation-specific link into a complete Source Reference unless it satisfies Source Reference requirements or a future governed specification defines compliant conversion behavior.

Where implementation-specific links support Source References, the implementation SHOULD preserve enough context to determine what Source Material is referenced, what governed entity the source supports, what role the source plays, whether the source remains available, whether privacy boundaries apply, whether validation occurred, and whether the reference remains compatible across implementation replacement.

Implementation behavior MUST preserve provenance boundaries.

A compliant implementation MUST NOT silently discard, collapse, overwrite, reinterpret, regenerate, detach, anonymize, deanonymize, expose, hide, infer, or replace provenance where provenance affects meaning, authority, privacy, validation, lifecycle state, relationships, Source References, compatibility, governance, publication, migration, import, export, restoration, synchronization, or downstream use.

Where an implementation generates provenance, that provenance SHOULD remain distinguishable from human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, validated, reviewed, approved, rejected, archived, or implementation-generated provenance where the distinction affects interpretation.

Implementation behavior MUST preserve relationship boundaries.

A compliant implementation MUST NOT treat backlinks, graph edges, search similarity, embedding similarity, folder proximity, tag overlap, citation co-occurrence, workflow routing, agent recommendations, import mappings, export mappings, migration mappings, archive groupings, or user interface grouping as governed relationships unless relationship requirements are satisfied or a future governed specification defines compliant relationship behavior.

Where implementation mechanisms support relationships, the implementation SHOULD preserve enough context to determine relationship type, participants, direction, role, provenance, privacy, validation, compatibility, lifecycle state, and authority where applicable.

Implementation behavior MUST preserve metadata boundaries.

A compliant implementation MUST NOT silently redefine, infer, overwrite, hide, discard, collapse, normalize, regenerate, expose, or replace metadata where metadata affects Object Identity, Source References, provenance, evidence, attribution, relationships, lifecycle state, authority, privacy classification, validation, compatibility, migration, import, export, restoration, synchronization, workflow behavior, agent behavior, governance, or downstream use.

Implementation behavior MUST preserve source-state boundaries.

A compliant implementation MUST NOT collapse source availability, source reliability, source authority, source privacy, source validation, and source compatibility into a single status when those distinctions affect interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, or downstream use.

Available is not the same as reliable.

Reliable is not the same as authoritative.

Authoritative is not the same as privacy-cleared.

Privacy-cleared is not the same as validated.

Validated is not the same as compatible.

Compatible is not the same as approved.

Implementation behavior MUST preserve lifecycle boundaries.

A compliant implementation MUST NOT treat saved, synced, indexed, linked, imported, exported, migrated, restored, archived, validated, routed, completed, agent-processed, workflow-processed, or displayed content as approved unless a governed lifecycle rule, authority rule, workflow rule, or future specification explicitly defines that behavior.

Implementation behavior MUST preserve privacy boundaries.

A compliant implementation MUST NOT expose restricted Source Material, Source References, evidence, attribution, provenance, metadata, relationships, validation results, source availability context, source reliability context, source authority context, source privacy context, source validation context, source compatibility context, human review history, workflow context, agent context, import context, export context, migration context, archive context, backup context, restoration context, or implementation context merely to improve traceability, review, validation, search, indexing, linking, embedding, publication, migration, import, export, synchronization, restoration, automation, usability, or implementation convenience.

Where restricted context exists, a compliant implementation SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Implementation behavior MUST preserve agent boundaries.

A compliant implementation MUST NOT allow an agent to access, summarize, extract, transform, validate, classify, embed, index, route, export, publish, synchronize, restore, migrate, or otherwise process restricted Source Material, Source References, evidence, attribution, provenance, metadata, relationships, validation results, workflow context, import context, export context, migration context, archive context, backup context, restoration context, or source-supporting context unless permitted by applicable privacy classification, governance rule, workflow rule, user authorization, or future governed specification.

Agent convenience, search improvement, automation value, ranking improvement, summarization quality, validation value, relationship discovery, or implementation convenience MUST NOT override Source Privacy, provenance boundaries, Source Reference boundaries, Object Identity boundaries, relationship boundaries, metadata boundaries, validation boundaries, lifecycle boundaries, or governance boundaries.

Implementation behavior MUST preserve workflow boundaries.

A compliant implementation MUST NOT treat workflow routing, workflow completion, workflow validation, workflow export, workflow import, workflow migration, workflow synchronization, workflow archival, workflow restoration, or workflow state changes as human approval, source authority, privacy clearance, validation success, lifecycle approval, publication readiness, or final governance unless a governed workflow specification explicitly defines that behavior.

Implementation behavior MUST preserve import, export, and migration boundaries.

A compliant implementation MUST NOT silently convert imported, exported, or migrated Source Material, Source References, provenance, metadata, relationships, validation results, identifiers, agent outputs, workflow outputs, archive records, backup records, or restoration records into apparently complete, validated, authoritative, privacy-cleared, compatible, or implementation-independent material.

Import, export, and migration behavior SHOULD preserve source context, destination context, mapping context, transformation context, validation context, review context, privacy context, compatibility context, uncertainty, omissions, loss, redaction, and restrictions where those conditions affect interpretation or downstream use.

Implementation behavior MUST preserve archive, backup, restoration, and synchronization boundaries.

A compliant implementation MUST NOT treat archived, backed-up, restored, or synchronized material as unchanged, complete, validated, authoritative, privacy-cleared, compatible, or current merely because a technical operation completed.

Archive, backup, restoration, and synchronization behavior SHOULD preserve enough provenance to determine what was copied, restored, synchronized, omitted, corrupted, transformed, mapped, restricted, redacted, validated, reviewed, failed, or marked uncertain where that context affects interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, or downstream use.

Implementation behavior MAY improve usability.

A compliant implementation MAY provide search, indexing, linking, graph navigation, previews, citations, summaries, recommendations, dashboards, validation reports, workflow queues, agent assistance, import tools, export tools, migration tools, archive tools, backup tools, restoration tools, synchronization tools, or other practical features.

Such features are compliant only when they preserve the standard-level meaning, boundaries, privacy expectations, validation expectations, compatibility expectations, governance expectations, and reviewability defined by KS-0005 and related standards.

Implementation behavior MAY be lossy.

Lossy implementation behavior occurs when source context, Source References, provenance, metadata, relationships, evidence, attribution, validation results, privacy context, authority context, lifecycle state, compatibility expectations, formatting, structure, identifiers, archive context, backup context, restoration context, synchronization context, import context, export context, migration context, workflow context, or agent context is changed, omitted, compressed, normalized, redacted, summarized, mapped, rendered, indexed, embedded, or otherwise reduced by an implementation.

Where implementation behavior is lossy, that condition SHOULD be represented or preserved when it affects interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, or downstream use.

Implementation behavior MAY be partial.

Partial implementation support is allowed.

A partial implementation MUST NOT falsely claim or imply complete KS-0005 conformance where unsupported Source References, provenance, evidence, attribution, source availability, source reliability, source authority, source privacy, source validation, source compatibility, import, export, migration, restoration, synchronization, agent behavior, workflow behavior, or privacy behavior affects interpretation or downstream use.

Implementation behavior MAY be uncertain.

Implementation uncertainty SHOULD be preserved when Source References, provenance, evidence, attribution, metadata, relationships, source availability, source reliability, source authority, source privacy, source validation, source compatibility, import behavior, export behavior, migration behavior, restoration behavior, synchronization behavior, workflow behavior, agent behavior, or implementation behavior is unclear, disputed, incomplete, inferred, low-confidence, restricted, unavailable, unverifiable, or not fully supported.

Implementation behavior MAY be expressed through metadata.

Implementation-boundary metadata MAY describe:

- implementation name;
- implementation role;
- implementation version;
- implementation limitation;
- implementation behavior;
- implementation-generated context;
- implementation-specific identifier;
- implementation-specific link;
- implementation-specific mapping;
- implementation-specific validation;
- implementation-specific rendering;
- implementation-specific indexing;
- implementation-specific search behavior;
- implementation-specific graph behavior;
- implementation-specific embedding behavior;
- implementation-specific synchronization behavior;
- implementation-specific backup behavior;
- implementation-specific restoration behavior;
- implementation-specific import behavior;
- implementation-specific export behavior;
- implementation-specific migration behavior;
- implementation-specific archive behavior;
- implementation-specific workflow behavior;
- implementation-specific agent behavior;
- implementation compatibility expectation;
- implementation privacy expectation;
- implementation validation expectation;
- implementation limitation requiring review.

KS-0005 does not define exact implementation-boundary metadata fields or exact implementation-state values.

A future specification MAY define exact implementation-boundary fields, implementation profiles, conformance profiles, allowed values, validation rules, compatibility rules, privacy rules, import formats, export formats, migration mappings, synchronization mappings, restoration mappings, archive mappings, backup mappings, or serialization syntax.

Implementation Boundaries SHOULD support validation.

A validator SHOULD be able to determine whether:

- implementation behavior is distinguishable from standard-level meaning;
- implementation-specific identifiers are distinguishable from stable Object Identity;
- implementation-specific links are distinguishable from complete Source References unless compliant;
- implementation metadata remains within metadata role boundaries;
- implementation relationships remain within relationship boundaries;
- implementation validation is distinguishable from truth, approval, authority, privacy clearance, publication readiness, and final governance;
- implementation behavior preserves Source Material and Knowledge Record boundaries;
- implementation behavior preserves Source Reference boundaries;
- implementation behavior preserves provenance boundaries;
- implementation behavior preserves privacy boundaries;
- implementation behavior preserves source availability, reliability, authority, privacy, validation, and compatibility distinctions;
- implementation behavior preserves import, export, and migration context where required;
- implementation behavior preserves restoration, synchronization, backup, and archive context where required;
- implementation behavior preserves agent and workflow boundaries where required;
- partial implementation support is not falsely treated as complete conformance;
- lossy implementation behavior is represented where applicable;
- implementation uncertainty is preserved where applicable;
- Implementation Boundaries remain compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Implementation Boundaries SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, migrate, index, embed, summarize, route, approve, reject, validate, or repair implementation-boundary context in a way that causes loss of meaning, broken Object Identity, broken Source References, broken provenance, broken relationships, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, implementation confusion, compatibility confusion, or source confusion.

Implementation Boundaries are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what standard-level source-reference and provenance meaning exists, what implementation behavior exists, what implementation limitations apply, what implementation-specific identifiers or links were used, whether Source Material and Knowledge Records remain distinguishable, whether Source References remain meaningful, whether provenance remains interpretable, whether metadata and relationships remain within their boundaries, whether source availability, reliability, authority, privacy, validation, and compatibility remain distinguishable, whether import, export, migration, restoration, synchronization, backup, archive, workflow, and agent behavior preserved required context, whether privacy boundaries apply, and whether implementation-boundary meaning remains intact across time and implementation replacement.

## 24. Governance and Evolution

Governance and Evolution define how KS-0005 may be reviewed, revised, extended, deprecated, superseded, interpreted, validated, and maintained over time without weakening Source Reference behavior, provenance behavior, Source Material boundaries, Object Identity boundaries, metadata boundaries, relationship boundaries, privacy boundaries, validation expectations, compatibility expectations, implementation independence, or practical daily usability.

Governance and Evolution exist so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, and standards maintainers can evolve Source Reference and provenance behavior while preserving continuity, traceability, reviewability, compatibility, and architectural integrity.

KS-0005 SHALL evolve only through governed revision.

A change to KS-0005 SHALL preserve the constitutional foundation unless the constitutional foundation is formally revised through governance.

A change to KS-0005 SHALL preserve the Layer 1 role of KS-0005 unless a higher-authority governance process changes the architecture.

A change to KS-0005 MUST NOT silently redefine Source Material, Source References, provenance, evidence, attribution, Object Identity, metadata, relationships, lifecycle state, authority, privacy, validation, compatibility, agents, workflows, storage, or implementations.

KS-0005 MAY evolve through:

- clarification;
- correction;
- expansion;
- deprecation;
- supersession;
- replacement;
- profile creation;
- future specification;
- compatibility rule;
- validation rule;
- migration rule;
- import rule;
- export rule;
- privacy rule;
- source-reference vocabulary;
- provenance vocabulary;
- archival specification;
- citation specification;
- implementation profile;
- governance decision;
- other governed extension.

Governed evolution MUST preserve standard-level meaning.

A future specification MAY define exact source-reference fields, provenance fields, citation syntax, metadata fields, allowed values, validation rules, import formats, export formats, migration mappings, archive structures, storage behavior, agent behavior, workflow behavior, or implementation behavior.

A future specification MUST NOT weaken, collapse, replace, or bypass KS-0005 requirements unless KS-0005 is formally revised, deprecated, or superseded through governance.

A future specification MUST remain subordinate to KS-0005 within the scope of Source Reference and provenance behavior unless governance assigns a different authority relationship.

Governance and Evolution are not the same as implementation behavior.

An implementation may support revision tracking, validation reports, migration tools, import tools, export tools, dashboards, review workflows, agent review, compatibility repair, or publication workflows.

Those implementation features MUST NOT create standard-level governance authority by themselves.

Governance and Evolution are not the same as workflow completion.

A workflow may route, review, validate, approve, reject, publish, migrate, import, export, archive, or supersede governed material.

Workflow completion MUST NOT be treated as governance approval unless a governed workflow specification explicitly defines that behavior.

Governance and Evolution are not the same as agent recommendation.

An agent may propose corrections, identify conflicts, detect missing Source References, suggest provenance improvements, classify source reliability, flag privacy risk, recommend compatibility repairs, or draft future specifications.

Agent output MUST NOT be treated as governance approval, human review, validation success, authority, privacy clearance, publication readiness, or final standard text unless a governed process explicitly accepts it.

Governance and Evolution are not the same as validation.

Validation may determine whether KS-0005 requirements are satisfied within a defined scope.

Validation does not revise KS-0005.

Validation does not approve new standard meaning.

Validation does not automatically create authority unless a governed rule or future specification explicitly defines that behavior.

KS-0005 revisions SHOULD preserve provenance.

Revision provenance SHOULD identify or describe:

- what changed;
- why the change occurred where applicable;
- who or what proposed the change;
- who or what reviewed the change;
- who or what approved or rejected the change where applicable;
- when the change occurred where applicable;
- what prior text was affected;
- what new text replaced it;
- whether the change is corrective, clarifying, substantive, deprecating, superseding, compatibility-related, privacy-related, validation-related, or implementation-related;
- whether related standards are affected;
- whether future specifications are affected;
- whether migration, import, export, validation, privacy, compatibility, workflow, agent, or implementation behavior is affected.

KS-0005 revisions SHOULD preserve compatibility.

A revision SHOULD NOT break existing Source References, provenance records, evidence records, attribution records, source availability records, source reliability records, source authority records, source privacy records, source validation records, source compatibility records, implementation-boundary records, metadata records, relationships, import records, export records, migration records, workflow outputs, agent outputs, archives, backups, restorations, synchronized copies, or prior conformance results unless the break is explicitly governed, documented, and justified.

Where a revision creates incompatibility, the incompatibility SHOULD be represented or preserved when it affects interpretation, validation, privacy, authority, lifecycle state, migration, import, export, restoration, synchronization, publication, governance, or downstream use.

KS-0005 revisions SHOULD preserve migration paths.

Where a revision changes source-reference behavior, provenance behavior, terminology, validation expectations, compatibility expectations, privacy expectations, metadata expectations, relationship expectations, import behavior, export behavior, migration behavior, implementation-boundary behavior, or conformance expectations, a governed migration path SHOULD be provided or deferred to a future specification.

A migration path MAY include:

- mapping guidance;
- compatibility notes;
- validation expectations;
- deprecated behavior;
- replacement behavior;
- required review;
- required repair;
- source-reference conversion guidance;
- provenance conversion guidance;
- metadata conversion guidance;
- relationship conversion guidance;
- privacy handling guidance;
- import guidance;
- export guidance;
- implementation guidance;
- agent guidance;
- workflow guidance.

KS-0005 MAY be extended.

An extension MAY define additional source types, source-reference types, provenance categories, evidence roles, attribution roles, source availability states, source reliability states, source authority states, source privacy states, source validation states, source compatibility states, implementation-boundary profiles, citation structures, archive structures, or validation profiles.

An extension MUST remain compatible with KS-0005 unless the extension is explicitly marked experimental, provisional, incompatible, deprecated, superseding, or governed by a higher-authority revision.

An extension MUST NOT silently redefine Source Material, Source References, provenance, evidence, attribution, Object Identity, metadata, relationships, privacy, authority, validation, compatibility, workflows, agents, storage, or implementation behavior.

KS-0005 MAY be clarified.

A clarification explains existing meaning without changing standard-level requirements.

A clarification SHOULD NOT require migration unless prior ambiguity caused materially different interpretation.

Where clarification affects interpretation, validation, privacy, compatibility, migration, import, export, governance, or downstream use, the clarification SHOULD preserve revision provenance.

KS-0005 MAY be corrected.

A correction repairs spelling, grammar, formatting, duplicate text, broken references, inconsistent terminology, numbering errors, or obvious mistakes.

A correction SHOULD NOT change standard-level meaning unless it is explicitly governed as a substantive revision.

Where a correction changes meaning, that correction SHOULD be treated as a governed revision rather than a simple editorial correction.

KS-0005 MAY be deprecated.

Deprecation means a term, rule, behavior, section, field expectation, source-reference behavior, provenance behavior, validation expectation, compatibility expectation, implementation expectation, or other governed element should no longer be used for new work but remains historically interpretable.

Deprecated material MUST remain distinguishable from deleted material.

Deprecated material MAY remain historically referenceable where it affects evidence, attribution, provenance, validation history, lifecycle state, authority, privacy, compatibility, governance, migration, import, export, restoration, synchronization, publication, or downstream use.

A deprecated element SHOULD identify replacement behavior where replacement behavior exists.

KS-0005 MAY be superseded.

Supersession means a later governed standard, specification, revision, or section replaces part or all of KS-0005.

Superseded material MUST remain historically interpretable where it affects Source References, provenance, evidence, attribution, validation, authority, privacy, lifecycle state, compatibility, governance, migration, import, export, restoration, synchronization, publication, or downstream use.

A superseding document SHOULD identify what it supersedes, what remains valid, what changes, what migration path applies, and what compatibility expectations apply.

Supersession MUST NOT silently erase prior Source References, provenance, validation results, conformance claims, implementation behavior, import records, export records, migration records, or governed decisions.

KS-0005 MAY be replaced.

Replacement means a later governed standard takes over the full role of KS-0005.

Replacement MUST preserve enough governance provenance for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to determine why replacement occurred, what changed, what remained compatible, what became deprecated, what became superseded, and what migration or validation path applies.

Governance MUST preserve privacy boundaries.

Governance activity MUST NOT expose restricted Source Material, restricted Source References, restricted provenance, restricted attribution, restricted evidence, restricted metadata, restricted relationships, restricted validation results, restricted source availability context, restricted source reliability context, restricted source authority context, restricted source privacy context, restricted source validation context, restricted source compatibility context, restricted workflow context, restricted agent context, restricted implementation context, restricted import context, restricted export context, restricted migration context, restricted archive context, restricted backup context, or restricted restoration context merely to improve review, validation, traceability, publication, migration, import, export, automation, synchronization, restoration, or implementation convenience.

Where governance context is restricted, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

Governance SHOULD preserve authority boundaries.

A proposed change is not authoritative merely because it is written.

A reviewed change is not automatically approved.

An agent-proposed change is not automatically valid.

A workflow-routed change is not automatically accepted.

An implementation-supported change is not automatically standard-level meaning.

A published change is not automatically current unless it is governed as current.

Authority for KS-0005 changes comes from the applicable governance model, document authority hierarchy, lifecycle state, review process, approval process, and future governed specification where applicable.

Governance SHOULD preserve lifecycle boundaries.

A draft revision, review revision, approved revision, deprecated revision, superseded revision, rejected revision, archived revision, or experimental revision SHOULD remain distinguishable where lifecycle state affects interpretation, validation, authority, privacy, compatibility, migration, import, export, publication, implementation behavior, workflow behavior, agent behavior, or downstream use.

A lifecycle transition SHOULD preserve provenance where it affects governance, compatibility, validation, migration, import, export, publication, or downstream use.

Governance SHOULD preserve validation boundaries.

A validator SHOULD be able to determine whether a KS-0005 revision, extension, deprecation, supersession, replacement, profile, future specification, implementation profile, or conformance claim falls within the authority and scope it claims.

Validation SHOULD preserve whether governance validation passed, failed, partially passed, was blocked, was deferred, requires repair, requires review, or requires higher-authority decision.

Governance SHOULD preserve compatibility boundaries.

A compatibility claim MUST NOT imply broader compatibility than its scope supports.

Compatibility with one KS-0005 version does not automatically imply compatibility with all KS-0005 versions.

Compatibility with one implementation does not automatically imply compatibility with all implementations.

Compatibility with structure does not automatically imply compatibility with privacy, authority, validation, migration, import, export, restoration, synchronization, publication, automation, agent behavior, workflow behavior, or downstream use.

Governance MAY define conformance profiles.

A conformance profile MAY define a scoped set of KS-0005 requirements for a specific use case, implementation profile, storage profile, validation profile, source-reference profile, provenance profile, workflow profile, agent profile, migration profile, import profile, export profile, publication profile, archive profile, backup profile, restoration profile, or synchronization profile.

A conformance profile MUST NOT claim full KS-0005 conformance unless all required KS-0005 requirements within the claimed scope are satisfied.

A conformance profile SHOULD identify scope, exclusions, limitations, required review, required validation, compatibility expectations, privacy expectations, migration expectations, and downstream-use limitations.

Governance MAY define controlled vocabularies.

A future specification MAY define controlled vocabularies for source types, source-reference roles, provenance types, evidence roles, attribution roles, availability states, reliability states, authority states, privacy states, validation states, compatibility states, implementation states, lifecycle states, workflow states, agent roles, import states, export states, or migration states.

A controlled vocabulary MUST NOT collapse distinctions that KS-0005 requires to remain distinguishable.

A controlled vocabulary SHOULD remain extensible, reviewable, privacy-respecting, validatable, compatible, and implementation-independent.

Governance MAY define repair behavior.

Repair behavior MAY address missing Source References, incomplete provenance, broken references, unavailable sources, unreliable sources, authority conflicts, privacy violations, failed validation, compatibility failures, implementation-boundary violations, import ambiguity, export ambiguity, migration loss, archive loss, backup corruption, restoration conflict, synchronization conflict, workflow confusion, agent attribution failure, or other source-reference and provenance failures.

Repair behavior SHOULD preserve original failure context where the failure affects interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, or downstream use.

Repair MUST NOT silently erase evidence of the failure where future review requires that context.

Governance MAY define review behavior.

Review behavior MAY involve human review, agent-assisted review, workflow-routed review, validation review, privacy review, authority review, compatibility review, implementation review, migration review, import review, export review, publication review, archive review, backup review, restoration review, or synchronization review.

Human review SHOULD remain distinguishable from agent review, workflow review, implementation checks, validation reports, and automated recommendations.

Governance MAY define publication behavior.

Publication behavior MAY determine when Source References, provenance, evidence, attribution, validation results, source availability, source reliability, source authority, source privacy, source compatibility, implementation-boundary context, conformance claims, or governed records may be released outside a private or internal context.

Publication behavior MUST preserve privacy boundaries.

Publication behavior MUST NOT treat validation success, workflow completion, implementation support, or agent recommendation as publication readiness unless a governed publication rule explicitly defines that behavior.

Governance MAY define archival behavior.

Archival behavior MAY preserve older versions, superseded text, deprecated behavior, validation results, conformance claims, source-reference behavior, provenance behavior, migration history, import history, export history, implementation behavior, workflow behavior, agent behavior, and governance decisions.

Archived material SHOULD remain interpretable where it affects provenance, evidence, validation, authority, privacy, lifecycle state, compatibility, migration, import, export, publication, restoration, synchronization, governance, or downstream use.

Governance SHOULD support validation.

A validator SHOULD be able to determine whether:

- KS-0005 authority remains subordinate to constitutional documents;
- KS-0005 remains within Layer 1 scope;
- revisions preserve Source Material boundaries;
- revisions preserve Source Reference boundaries;
- revisions preserve provenance boundaries;
- revisions preserve Object Identity boundaries;
- revisions preserve metadata boundaries;
- revisions preserve relationship boundaries;
- revisions preserve privacy boundaries;
- revisions preserve validation boundaries;
- revisions preserve compatibility boundaries;
- revisions preserve implementation independence;
- future specifications remain subordinate where required;
- extensions do not silently redefine standard-level meaning;
- deprecations remain historically interpretable;
- supersessions preserve prior context where required;
- replacements preserve migration and compatibility context where required;
- agent-proposed changes remain distinguishable from human-approved changes;
- workflow completion is not falsely treated as governance approval;
- implementation support is not falsely treated as standard authority;
- governance provenance is preserved where required;
- privacy boundaries are preserved;
- governance meaning remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Governance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, migrate, index, embed, summarize, route, approve, reject, validate, or repair governance context in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, Object Identity confusion, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, evolution confusion, compatibility confusion, or source confusion.

Governance and Evolution are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, and standards maintainers can determine what version of KS-0005 applies, what changed, why it changed where applicable, who or what proposed, reviewed, approved, rejected, deprecated, superseded, or replaced the change, what authority applies, what lifecycle state applies, what compatibility expectations apply, what migration path applies, what privacy boundaries apply, what future specifications depend on the change, and whether Source Reference and provenance meaning remains intact across time and implementation replacement.

## 25. Conformance

Conformance defines how humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, specifications, profiles, and governed processes may determine whether Source Material, Source References, provenance, evidence, attribution, extraction history, transformation history, human-created provenance, agent-generated provenance, workflow-generated provenance, import provenance, export provenance, migration provenance, source availability, source reliability, source authority, source privacy, source validation, source compatibility, implementation boundaries, governance behavior, and future extensions satisfy KS-0005.

Conformance exists so that source-reference and provenance behavior can be evaluated consistently without relying on hidden application state, undocumented implementation behavior, agent memory, workflow memory, folder placement, filenames, database internals, plugin behavior, citation style, user memory, search ranking, graph layout, or implementation-specific assumptions.

A conformance claim SHALL identify the scope of the claim.

A conformance claim SHOULD identify what entity, system, workflow, agent, process, profile, specification, implementation, import, export, migration, archive, backup, restoration, synchronization, publication, validation result, or governed record is being evaluated.

A conformance claim MUST NOT imply broader conformance than its stated scope supports.

Conformance to KS-0005 MAY be claimed for:

- a Knowledge Object;
- a Knowledge Record;
- Source Material;
- a Source Reference;
- a provenance record;
- evidence;
- attribution;
- extraction provenance;
- transformation provenance;
- human-created provenance;
- agent-generated provenance;
- workflow-generated provenance;
- import provenance;
- export provenance;
- migration provenance;
- source availability context;
- source reliability context;
- source authority context;
- source privacy context;
- source validation context;
- source compatibility context;
- implementation-boundary context;
- a metadata structure;
- a relationship structure;
- a validation profile;
- a source-reference profile;
- a provenance profile;
- an import process;
- an export process;
- a migration process;
- a workflow;
- an agent;
- a storage system;
- an implementation;
- a specification;
- a governed extension;
- another governed entity or process.

Conformance is not the same as truth.

A conforming Source Reference, provenance record, evidence record, attribution record, validation result, metadata record, relationship, workflow output, agent output, import record, export record, migration record, or implementation behavior does not prove that Source Material is true, complete, current, unbiased, reliable, authoritative, privacy-cleared, publication-ready, approved, or sufficient for every use.

Conformance is not the same as approval.

A conforming entity may still require review, validation, approval, rejection, correction, restriction, deprecation, supersession, archival, publication review, privacy review, authority review, compatibility review, migration review, import review, export review, or governance action.

Conformance does not automatically change lifecycle state unless a governed lifecycle rule, workflow rule, authority rule, approval rule, or future specification defines that behavior.

Conformance is not the same as authority.

A conforming Source Reference or provenance record may support authority assessment.

Conformance does not automatically create Source Authority, document authority, review authority, publication authority, governance authority, or approval authority.

Conformance is not the same as validation.

Validation may evaluate conformance.

A validation result may support a conformance claim.

However, validation must identify scope, method, actor, rule, limitation, result, and review state where those conditions affect interpretation.

A validation result MUST NOT imply full KS-0005 conformance when only a limited subset of requirements was checked.

Conformance is not the same as implementation support.

An implementation may support files, folders, metadata, databases, indexes, graphs, backlinks, citations, archives, synchronization, backups, restorations, imports, exports, migrations, validators, workflows, agents, or user interfaces.

Implementation support does not automatically create KS-0005 conformance unless the implementation preserves the required standard-level source-reference and provenance meaning within the claimed scope.

A conforming entity SHOULD preserve Source Material boundaries.

A conforming entity MUST NOT treat Source Material and Knowledge Records as the same entity where their distinction affects meaning, evidence, attribution, provenance, validation, authority, privacy, lifecycle state, compatibility, governance, migration, import, export, publication, or downstream use.

A conforming entity SHOULD preserve Source Reference boundaries.

A conforming Source Reference SHOULD identify or describe Source Material clearly enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what source is being referenced where access is permitted.

A conforming Source Reference MUST NOT depend only on filename, folder path, storage location, display title, URL, citation style, database row, search result, graph layout, backlink behavior, user interface state, plugin behavior, hidden application state, agent memory, workflow memory, or implementation-specific identifier where that reference affects governed meaning.

A conforming entity SHOULD preserve provenance boundaries.

Conforming provenance SHOULD identify or describe origin, source use, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context where that context affects meaning, authority, privacy, lifecycle state, relationships, compatibility, governance, or downstream use.

A conforming entity MUST NOT silently discard, collapse, overwrite, reinterpret, detach, anonymize, deanonymize, expose, hide, infer, regenerate, or replace provenance where provenance affects governed meaning.

A conforming entity SHOULD preserve evidence and attribution boundaries.

Evidence SHOULD remain distinguishable from interpretation, authority, approval, validation status, and truth.

Attribution SHOULD remain distinguishable from authority, ownership, approval, validation, and truth.

A conforming entity MUST NOT falsely imply that evidence, attribution, citation, indexing, embedding, agent selection, workflow routing, or implementation display makes a source true, approved, authoritative, validated, complete, or privacy-cleared.

A conforming entity SHOULD preserve extraction and transformation provenance.

Extracted content SHOULD remain distinguishable from original Source Material, transformed content, interpreted content, synthesized knowledge, Knowledge Records, Source References, provenance, validation results, agent outputs, workflow outputs, and implementation-specific representations where the distinction affects interpretation.

Transformed content SHOULD preserve enough provenance to determine what changed, what source or prior state was used, who or what performed the transformation, whether meaning changed, whether review occurred, whether validation occurred, and whether privacy boundaries apply.

A conforming entity SHOULD preserve human, agent, and workflow provenance distinctions.

Human-created provenance MUST remain distinguishable from agent-generated provenance and workflow-generated provenance where the distinction affects meaning, authority, privacy, validation, lifecycle state, governance, publication, or downstream use.

Agent-generated provenance MUST NOT be treated as human-created, human-reviewed, approved, authoritative, complete, accurate, privacy-cleared, or publication-ready merely because an agent produced it.

Workflow-generated provenance MUST NOT be treated as human approval, agent validation, source authority, privacy clearance, validation success, lifecycle approval, publication readiness, or final governance unless a future governed workflow specification explicitly defines that behavior.

A conforming entity SHOULD preserve import, export, and migration provenance.

Import, export, and migration provenance SHOULD preserve source context, destination context where applicable, mapping context, transformation context, extraction context, validation context, review context, privacy context, compatibility context, omissions, redactions, restrictions, uncertainty, and loss where those conditions affect interpretation or downstream use.

A conforming import, export, or migration process MUST NOT silently convert incomplete, lossy, restricted, uncertain, unavailable, unvalidated, non-authoritative, privacy-limited, compatibility-limited, or implementation-specific material into apparently complete, lossless, public, validated, authoritative, privacy-cleared, compatible, or implementation-independent material.

A conforming entity SHOULD preserve source-state distinctions.

Source availability, source reliability, source authority, source privacy, source validation, and source compatibility MUST remain distinguishable where the distinction affects interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

Available is not the same as reliable.

Reliable is not the same as authoritative.

Authoritative is not the same as privacy-cleared.

Privacy-cleared is not the same as validated.

Validated is not the same as compatible.

Compatible is not the same as approved.

A conforming entity SHOULD preserve implementation boundaries.

Implementation behavior MUST remain distinguishable from standard-level meaning.

Implementation-specific identifiers MUST remain distinguishable from stable Object Identity.

Implementation-specific links MUST remain distinguishable from complete Source References unless they satisfy Source Reference requirements or a future governed specification defines compliant conversion behavior.

Implementation metadata, workflow state, agent state, search ranking, graph layout, embeddings, citation display, synchronization state, archive state, backup state, restoration state, import state, export state, and migration state MUST NOT silently redefine Source References, provenance, Object Identity, metadata, relationships, lifecycle state, authority, privacy, validation, compatibility, or governance meaning.

A conforming entity MUST preserve privacy boundaries.

Conformance MUST NOT require exposing restricted Source Material, restricted Source References, restricted provenance, restricted attribution, restricted evidence, restricted metadata, restricted relationships, restricted validation results, restricted source availability context, restricted source reliability context, restricted source authority context, restricted source privacy context, restricted source validation context, restricted source compatibility context, restricted workflow context, restricted agent context, restricted implementation context, restricted import context, restricted export context, restricted migration context, restricted archive context, restricted backup context, or restricted restoration context.

Where restricted context affects conformance, a compliant system SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted information.

A conformance evaluator MUST NOT treat restricted context as absent merely because the current actor lacks access.

Conformance MAY be complete, partial, scoped, provisional, experimental, restricted, uncertain, failed, blocked, deferred, stale, superseded, deprecated, imported, exported, migrated, or historically preserved.

Partial conformance is allowed.

Partial conformance MUST identify scope and limitation where unsupported KS-0005 behavior affects interpretation, validation, authority, privacy, lifecycle state, compatibility, governance, publication, migration, import, export, restoration, synchronization, automation, agent behavior, workflow behavior, implementation behavior, or downstream use.

A partial conformance claim MUST NOT falsely imply full KS-0005 conformance.

Conformance MAY be profile-based.

A conformance profile MAY define a scoped set of KS-0005 requirements for a specific source-reference profile, provenance profile, metadata profile, relationship profile, validation profile, implementation profile, storage profile, workflow profile, agent profile, import profile, export profile, migration profile, publication profile, archive profile, backup profile, restoration profile, or synchronization profile.

A conformance profile SHOULD identify:

- profile name;
- profile scope;
- required KS-0005 sections;
- excluded KS-0005 sections;
- required Source Reference behavior;
- required provenance behavior;
- required privacy behavior;
- required validation behavior;
- required compatibility behavior;
- required implementation-boundary behavior;
- allowed limitations;
- required review;
- required repair;
- downstream-use limitations;
- migration expectations;
- import expectations;
- export expectations.

A conformance profile MUST NOT weaken KS-0005 requirements outside its stated scope.

A conformance profile MUST NOT claim full KS-0005 conformance unless all required KS-0005 requirements are satisfied within the claimed scope.

Conformance MAY be evaluated by humans.

Human conformance review SHOULD preserve attribution, review scope, review method, review result, uncertainty, limitation, correction requirement, repair requirement, lifecycle effect, authority effect, privacy effect, validation effect, compatibility effect, and downstream-use limitation where those conditions affect interpretation.

Conformance MAY be evaluated by agents.

Agent conformance review MAY identify missing Source References, incomplete provenance, unclear attribution, broken evidence support, privacy risk, validation ambiguity, compatibility failure, implementation-boundary violation, import ambiguity, export ambiguity, migration loss, governance drift, or other conformance concerns.

Agent conformance review MUST remain distinguishable from human review, approval, authority, privacy clearance, publication readiness, truth, and final governance unless a future governed specification explicitly defines otherwise.

Conformance MAY be evaluated through workflows.

Workflow conformance review MAY route, validate, approve, reject, defer, block, repair, archive, publish, import, export, migrate, or preserve conformance context where permitted by governance and privacy rules.

Workflow completion MUST NOT be treated as conformance success unless a future governed workflow specification explicitly defines that behavior.

Conformance MAY be expressed through metadata.

Conformance metadata MAY describe:

- conformance claim;
- conformance scope;
- conformance profile;
- conformance target;
- conformance standard;
- conformance specification;
- conformance version;
- conformance actor;
- conformance method;
- conformance date where applicable;
- conformance result;
- conformance limitation;
- conformance exclusion;
- conformance failure;
- conformance blocker;
- conformance deferral;
- conformance review requirement;
- conformance repair requirement;
- conformance privacy condition;
- conformance authority condition;
- conformance lifecycle effect;
- conformance compatibility expectation;
- Source Reference conformance;
- provenance conformance;
- evidence conformance;
- attribution conformance;
- extraction conformance;
- transformation conformance;
- import conformance;
- export conformance;
- migration conformance;
- source availability conformance;
- source reliability conformance;
- source authority conformance;
- source privacy conformance;
- source validation conformance;
- source compatibility conformance;
- implementation-boundary conformance;
- governance conformance;
- downstream-use limitation.

KS-0005 does not define exact conformance metadata fields, exact conformance profiles, exact certification methods, exact test suites, exact scoring methods, exact validation tools, exact report formats, exact implementation checklists, exact operational procedures, or exact governance templates.

A future specification MAY define exact conformance fields, allowed values, conformance profiles, validation profiles, test rules, report formats, certification methods, error codes, warning codes, review rules, repair rules, lifecycle mappings, import formats, export formats, migration mappings, implementation mappings, or serialization syntax.

Conformance SHOULD preserve failure context.

A failed, partial, blocked, deferred, stale, superseded, deprecated, restricted, or uncertain conformance result SHOULD preserve enough context to determine:

- what was evaluated;
- what scope applied;
- what requirement failed;
- what requirement passed;
- what requirement was not evaluated;
- what evidence supported the result;
- who or what performed the evaluation;
- whether human review occurred;
- whether agent review occurred;
- whether workflow review occurred;
- whether correction is required;
- whether repair is required;
- whether privacy boundaries restricted the evaluation;
- whether authority is affected;
- whether lifecycle state is affected;
- whether compatibility is affected;
- whether migration, import, export, restoration, synchronization, publication, automation, agent behavior, workflow behavior, implementation behavior, or downstream use is affected.

Conformance SHOULD support validation.

A validator SHOULD be able to determine whether:

- conformance scope is explicit;
- conformance target is explicit;
- conformance profile is identified where applicable;
- conformance version is identified where applicable;
- Source Material remains distinguishable from Knowledge Records;
- Source References are present where required;
- Source References remain meaningful where required;
- provenance is present where required;
- evidence and interpretation remain distinguishable where required;
- attribution role is clear where required;
- extraction provenance is present where required;
- transformation provenance is present where required;
- human-created, agent-generated, and workflow-generated provenance remain distinguishable where required;
- import, export, and migration provenance are preserved where required;
- source availability, reliability, authority, privacy, validation, and compatibility remain distinguishable where required;
- implementation behavior remains subordinate to standard-level meaning;
- governance behavior remains within authority boundaries;
- privacy boundaries are preserved;
- partial conformance is not falsely treated as full conformance;
- implementation support is not falsely treated as standard conformance;
- workflow completion is not falsely treated as conformance success;
- agent review is not falsely treated as human review;
- failure context is preserved where required;
- conformance meaning remains compatible across migration, import, export, storage replacement, workflow activity, agent activity, validation, restoration, synchronization, and implementation replacement.

Conformance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, citation tool, publication tool, or review tool MUST NOT silently discard, collapse, expose, reinterpret, detach, overwrite, infer, replace, remap, regenerate, normalize, publish, package, synchronize, restore, migrate, index, embed, summarize, route, approve, reject, validate, repair, or claim conformance in a way that causes loss of meaning, broken Source References, broken provenance, broken relationships, Object Identity confusion, authority ambiguity, privacy exposure, validation failure, import ambiguity, export ambiguity, migration loss, restoration ambiguity, synchronization ambiguity, governance drift, implementation lock-in, conformance confusion, compatibility confusion, or source confusion.

Conformance is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, and standards maintainers can determine what KS-0005 requirements were evaluated, what scope applied, what profile applied where applicable, what passed, what failed, what was partial, what was blocked, what was deferred, what was restricted, what was not evaluated, what evidence supported the result, what review occurred, what repair remains required, what privacy boundaries apply, what authority or lifecycle effects apply, what compatibility expectations apply, what migration, import, export, restoration, synchronization, publication, automation, workflow, agent, or implementation limitations apply, and whether conformance meaning remains intact across time and implementation replacement.

## 26. Success Criteria

Success Criteria define how humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, standards maintainers, and governance processes determine whether KS-0005 fulfills its purpose within The Brain Standard.

KS-0005 succeeds when Source References and provenance remain explicit, interpretable, portable, traceable, reviewable, privacy-respecting, validatable, compatible, governed, maintainable, and implementation-independent across time, tools, workflows, agents, storage systems, migration processes, import processes, export processes, validation processes, restoration processes, synchronization processes, and implementation replacement.

KS-0005 succeeds when future humans can determine what Source Material supports a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, validation result, import record, export record, migration record, standard, specification, governance decision, or other governed entity.

KS-0005 succeeds when future humans can determine what provenance applies to a governed entity, including origin, source use, evidence, attribution, extraction, transformation, human involvement, agent involvement, workflow involvement, validation, review, import, export, migration, restoration, synchronization, governance, or change history where that context affects interpretation.

KS-0005 succeeds when future agents can read, propose, classify, summarize, validate, preserve, migrate, import, export, or enrich source-reference and provenance context only within applicable privacy boundaries, authority limits, validation expectations, workflow rules, governance rules, and review requirements.

KS-0005 succeeds when future workflows can create, route, review, validate, approve, reject, restrict, deprecate, supersede, archive, import, export, migrate, restore, synchronize, publish, or preserve Source References and provenance without treating workflow completion as human approval, source authority, privacy clearance, validation success, publication readiness, or final governance unless a future governed workflow specification explicitly defines that behavior.

KS-0005 succeeds when future validators can determine whether Source Material, Source References, provenance, evidence, attribution, extraction history, transformation history, human-created provenance, agent-generated provenance, workflow-generated provenance, import provenance, export provenance, migration provenance, source availability, source reliability, source authority, source privacy, source validation, source compatibility, implementation boundaries, governance behavior, and conformance claims satisfy applicable KS-0005 requirements within a defined scope.

KS-0005 succeeds when future implementations can store, display, search, index, link, cite, archive, validate, import, export, migrate, synchronize, back up, restore, process, route, summarize, embed, graph, or publish source-reference and provenance information without redefining standard-level source-reference or provenance meaning.

KS-0005 succeeds when Source Material remains distinguishable from Knowledge Records.

A file, document, image, recording, dataset, message, transcript, web page, external reference, archive record, imported artifact, exported artifact, migrated artifact, or other source artifact MUST NOT become a Knowledge Record merely because it is stored, indexed, linked, cited, processed, summarized, embedded, validated, imported, exported, migrated, restored, synchronized, or displayed by a compliant implementation.

A Knowledge Record MUST NOT become Source Material merely because it quotes, summarizes, extracts from, transforms, interprets, classifies, validates, discusses, cites, links to, imports, exports, migrates, or preserves Source Material.

KS-0005 succeeds when Source References remain meaningful.

A successful Source Reference identifies or describes Source Material clearly enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand what source is being referenced where access is permitted.

A successful Source Reference remains meaningful when Source Material is renamed, moved, copied, archived, restricted, migrated, imported, exported, backed up, restored, synchronized, reindexed, transformed, validated, processed by an agent, processed by a workflow, or accessed through a different implementation.

KS-0005 succeeds when Source References do not depend solely on filename, folder path, storage location, display title, URL, citation style, database row, search result, graph layout, backlink behavior, user interface state, plugin behavior, hidden application state, agent memory, workflow memory, user memory, or implementation-specific identifier where source-reference meaning affects interpretation.

KS-0005 succeeds when provenance remains interpretable.

Successful provenance preserves enough context to determine where knowledge came from, what source material was used, what evidence supported it, what action occurred, who or what participated, whether extraction occurred, whether transformation occurred, whether validation occurred, whether review occurred, whether import occurred, whether export occurred, whether migration occurred, whether privacy boundaries apply, and whether provenance remains compatible across implementation replacement.

KS-0005 succeeds when evidence remains distinguishable from interpretation, authority, approval, validation status, conformance, and truth.

Evidence may support, challenge, explain, contextualize, limit, or qualify a governed entity.

Evidence MUST NOT be treated as true, approved, authoritative, privacy-cleared, validated, or publication-ready merely because it is present, cited, indexed, embedded, linked, frequently used, agent-selected, workflow-routed, implementation-preferred, or stored in a compliant repository.

KS-0005 succeeds when attribution remains distinguishable from authority, ownership, approval, validation, and truth.

Attribution should make clear who or what is associated with Source Material, evidence, provenance, extraction, transformation, validation, import, export, migration, workflow activity, agent activity, implementation activity, review, approval, rejection, or governance where that role affects interpretation.

KS-0005 succeeds when extraction provenance remains sufficient.

Successful extraction provenance allows future review of what was taken from Source Material, what portion or aspect of the source was used where applicable, who or what performed the extraction, whether extraction was complete, partial, restricted, uncertain, lossy, reviewed, validated, imported, exported, migrated, agent-generated, workflow-generated, human-created, or implementation-generated, and whether privacy boundaries apply.

KS-0005 succeeds when transformation provenance remains sufficient.

Successful transformation provenance allows future review of what was changed, what source or prior state was used, what output was produced, who or what performed the transformation, whether meaning changed, whether transformation was complete, partial, restricted, uncertain, lossy, reversible, irreversible, reviewed, validated, imported, exported, migrated, agent-generated, workflow-generated, human-created, or implementation-generated, and whether privacy boundaries apply.

KS-0005 succeeds when human-created provenance remains distinguishable from agent-generated provenance, workflow-generated provenance, imported provenance, exported provenance, migrated provenance, inferred provenance, and implementation-generated provenance.

Human involvement SHOULD remain clear where authorship, review, correction, approval, rejection, validation, governance, source selection, evidence selection, extraction, transformation, import, export, migration, or interpretation affects meaning, authority, privacy, lifecycle state, validation, publication, governance, or downstream use.

KS-0005 succeeds when agent-generated provenance remains distinguishable from human-created provenance, human review, human approval, workflow approval, validation approval, source authority, privacy clearance, publication readiness, truth, and final governance.

Agent-generated output MUST NOT be treated as human-reviewed, approved, authoritative, complete, accurate, privacy-cleared, publication-ready, compatible, or final merely because an agent produced it.

KS-0005 succeeds when workflow-generated provenance remains distinguishable from human-created provenance, agent-generated provenance, human approval, source authority, privacy clearance, validation success, publication readiness, truth, and final governance.

Workflow completion MUST NOT be treated as approval, authority, validation success, privacy clearance, publication readiness, conformance success, or compatibility success unless a future governed workflow specification explicitly defines that behavior.

KS-0005 succeeds when import provenance remains sufficient.

Successful import provenance allows future review of what was imported, where it came from, what source system or prior environment was used, what mapping occurred, what changed, what was omitted, what was uncertain, what was restricted, what review occurred, what validation occurred, whether Object Identity boundaries were preserved, whether Source Reference boundaries were preserved, whether metadata and relationship boundaries were preserved, and whether privacy boundaries apply.

KS-0005 succeeds when export provenance remains sufficient.

Successful export provenance allows future review of what was exported, where it came from, where it went where applicable, what mapping occurred, what changed, what was omitted, what was redacted, what was restricted, what review occurred, what validation occurred, whether Object Identity boundaries were preserved, whether Source Reference boundaries were preserved, whether metadata and relationship boundaries were preserved, and whether privacy boundaries apply.

KS-0005 succeeds when migration provenance remains sufficient.

Successful migration provenance allows future review of what was migrated, where it came from, where it went, what mapping occurred, what changed, what was preserved, what was omitted, what was redacted, what was lost, what was uncertain, what review occurred, what validation occurred, whether Object Identity remained stable, whether Source References remained meaningful, whether provenance remained interpretable, whether metadata and relationships remained within their boundaries, and whether privacy boundaries apply.

KS-0005 succeeds when source availability remains distinguishable from source reliability, source authority, source privacy, source validation, source compatibility, lifecycle state, approval, and truth.

Available is not the same as reliable.

Unavailable is not the same as unreliable.

Restricted is not the same as missing.

Missing is not the same as deleted.

Superseded is not the same as invalid.

KS-0005 succeeds when source reliability remains distinguishable from source availability, source authority, source privacy, source validation, source compatibility, lifecycle state, approval, and truth.

Reliable is not the same as authoritative.

Authoritative is not the same as reliable.

Reviewed is not the same as approved.

Validated is not the same as true.

Current is not the same as complete.

KS-0005 succeeds when source authority remains distinguishable from source availability, source reliability, source privacy, source validation, source compatibility, lifecycle state, approval, publication readiness, and truth.

Authoritative is not the same as reliable.

Official is not the same as complete.

Approved is not the same as true.

Publication-ready is not the same as universally authoritative.

Superseded is not the same as useless.

KS-0005 succeeds when source privacy remains distinguishable from source availability, source reliability, source authority, source validation, source compatibility, lifecycle state, approval, security mechanisms, publication readiness, and truth.

Private is not the same as unavailable.

Available is not the same as privacy-cleared.

Reliable is not the same as safe to expose.

Authoritative is not the same as publication-ready.

Agent access is not the same as downstream-use permission.

KS-0005 succeeds when source validation remains distinguishable from truth, approval, authority, privacy clearance, publication readiness, compatibility, lifecycle state, workflow completion, agent validation, implementation checks, and conformance claims.

Validated is not the same as true.

Validated is not the same as approved.

Validated is not the same as authoritative.

Validated is not the same as privacy-cleared.

Validated is not the same as publication-ready.

KS-0005 succeeds when source compatibility remains distinguishable from availability, reliability, authority, privacy, validation, approval, publication readiness, losslessness, and truth.

Compatible is not the same as lossless.

Portable is not the same as complete.

Human-readable is not the same as AI-readable.

Validation success is not the same as future compatibility.

Implementation support is not the same as standard compatibility.

KS-0005 succeeds when implementation boundaries remain clear.

Implementation-specific identifiers, links, backlinks, citations, graph edges, database rows, file paths, folder paths, URLs, plugin state, search results, vector embeddings, indexes, aliases, tags, caches, APIs, synchronization records, backup records, restoration records, import records, export records, migration records, workflow state, agent state, and user interface elements MUST remain distinguishable from standard-level Source References, provenance, Object Identity, metadata, relationships, validation, authority, privacy, compatibility, lifecycle state, governance, and conformance meaning.

KS-0005 succeeds when privacy boundaries are preserved.

Restricted Source Material, Source References, provenance, attribution, evidence, metadata, relationships, validation results, source availability context, source reliability context, source authority context, source privacy context, source validation context, source compatibility context, workflow context, agent context, implementation context, import context, export context, migration context, archive context, backup context, restoration context, or governance context MUST NOT be exposed merely to improve traceability, search, review, validation, linking, indexing, embedding, publication, migration, import, export, synchronization, restoration, automation, usability, or implementation convenience.

KS-0005 succeeds when privacy-restricted context remains reviewable by authorized actors without being falsely treated as absent by unauthorized actors.

A compliant system MUST NOT treat restricted context as missing merely because the current actor lacks access.

KS-0005 succeeds when governance can evolve source-reference and provenance behavior without causing governance drift.

Future specifications, source-reference vocabularies, provenance vocabularies, citation specifications, archival specifications, validation specifications, conformance profiles, storage standards, agent standards, workflow standards, implementation profiles, import formats, export formats, migration mappings, restoration mappings, synchronization mappings, and operational guides may refine KS-0005 only when they preserve KS-0005 meaning or explicitly govern deprecation, supersession, replacement, incompatibility, migration, validation, and compatibility expectations.

KS-0005 succeeds when conformance can be reviewed.

A conformance claim SHOULD be able to demonstrate what scope was evaluated, what standard or specification applied, what profile applied where applicable, what passed, what failed, what was partial, what was blocked, what was deferred, what was restricted, what was not evaluated, what evidence supported the result, what review occurred, what repair remains required, what privacy boundaries apply, what authority or lifecycle effects apply, what compatibility expectations apply, and what downstream-use limitations remain.

KS-0005 succeeds when partial conformance is explicit.

A partial-conformance claim MUST NOT imply full KS-0005 conformance.

A scoped conformance claim MUST NOT imply broader conformance than the stated scope supports.

A conformance claim for one implementation MUST NOT imply conformance for all implementations.

A conformance claim for structure MUST NOT imply conformance for authority, privacy, validation, compatibility, publication, automation, migration, import, export, restoration, synchronization, workflow behavior, agent behavior, implementation behavior, or downstream use.

KS-0005 succeeds when failures remain repairable.

A source-reference or provenance failure SHOULD preserve enough context to determine what failed, what was missing, what was uncertain, what was restricted, what was incompatible, what was lost, what was omitted, what was redacted, what was transformed, what review is required, what repair is required, what privacy boundaries apply, and whether authority, lifecycle state, validation, compatibility, publication, migration, import, export, restoration, synchronization, workflow behavior, agent behavior, implementation behavior, governance, or downstream use is affected.

Repair MUST NOT silently erase evidence of the failure where future review requires that context.

KS-0005 succeeds when long-term maintainability is preserved.

Long-term maintainability requires enough source-reference and provenance structure to preserve meaning without creating unnecessary burden, excessive metadata, redundant rules, hidden implementation dependence, privacy risk, validation ambiguity, migration difficulty, or governance drift.

KS-0005 succeeds when daily use remains practical.

A compliant source-reference and provenance model SHOULD support real use by humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations without requiring unnecessary duplication, excessive fields, brittle citation syntax, tool-specific behavior, or manual reconstruction of context that should be preserved by the standard.

KS-0005 succeeds when future humans can trust the record enough to inspect it.

KS-0005 succeeds when future agents can assist without becoming unreviewable authorities.

KS-0005 succeeds when future workflows can coordinate work without hiding approval, review, validation, privacy, authority, or compatibility boundaries.

KS-0005 succeeds when future validators can detect missing Source References, incomplete provenance, unclear attribution, evidence confusion, privacy exposure, authority ambiguity, validation ambiguity, compatibility failure, implementation lock-in, import ambiguity, export ambiguity, migration loss, agent-boundary failure, workflow-boundary failure, conformance ambiguity, or governance drift.

KS-0005 succeeds when future implementations can be replaced without losing source-reference and provenance meaning.

KS-0005 succeeds when Source References and provenance remain useful even when files move, names change, tools are replaced, sources become restricted, sources become unavailable, sources are archived, records are imported, records are exported, records are migrated, records are restored, records are synchronized, agents change, workflows change, validators change, implementations change, and standards evolve.

KS-0005 fails when source-reference or provenance meaning depends on undocumented memory, hidden application state, folder placement, filename convention, citation style alone, database internals, plugin behavior, search ranking, graph layout, vector similarity, agent memory, workflow memory, user memory, or implementation-specific behavior that cannot be reviewed, preserved, validated, migrated, imported, exported, restored, synchronized, or replaced.

KS-0005 fails when Source Material and Knowledge Records become indistinguishable.

KS-0005 fails when Source References exist but cannot be interpreted.

KS-0005 fails when provenance exists but cannot explain origin, source use, transformation, review, validation, import, export, migration, agent activity, workflow activity, or governance context where that context affects meaning.

KS-0005 fails when privacy is exposed for convenience.

KS-0005 fails when agent output is treated as human approval.

KS-0005 fails when workflow completion is treated as governance approval.

KS-0005 fails when implementation support is treated as standard meaning.

KS-0005 fails when conformance claims exceed their scope.

KS-0005 fails when migration, import, export, restoration, synchronization, backup, archive, agent processing, workflow routing, indexing, embedding, summarization, citation display, graph display, or implementation replacement silently loses governed source-reference or provenance meaning.

KS-0005 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, and standards maintainers can determine what Source Material exists, what Source References exist, what provenance applies, what evidence supports the knowledge, what attribution applies, what extraction or transformation occurred, what human, agent, or workflow involvement occurred, what import, export, or migration context applies, what source availability, reliability, authority, privacy, validation, and compatibility states apply, what implementation boundaries apply, what governance and conformance context applies, what privacy boundaries restrict exposure, what repair remains required, what downstream-use limits remain, and whether source-reference and provenance meaning remains intact across time and implementation replacement.
