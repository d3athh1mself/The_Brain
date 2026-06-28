# SS-0001 — Storage Architecture Standard

Document ID: SS-0001
Title: Storage Architecture Standard
Version: 0.1.0
Status: Draft
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 2 — Storage Standard
Milestone: 2.1 — Storage Architecture Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and storage-architecture rules are interpreted within SS-0001.

Where conflicts arise between storage environments, vaults, repositories, folders, files, archives, source-material areas, Knowledge Records, drafts, approved records, implementation files, supporting assets, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, agents, workflows, implementations, import behavior, export behavior, migration behavior, backup behavior, synchronization behavior, indexing behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

SS-0001 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

SS-0001 depends on the Phase 1 Knowledge Standards because storage must preserve knowledge meaning without defining it.

SS-0001 defines storage architecture at the conceptual standard level.

SS-0001 does not define exact folder paths, exact filenames, exact file extensions, exact vault layouts, exact database schemas, exact sync tools, exact backup tools, exact operating-system behavior, exact Obsidian behavior, exact Codex behavior, exact repository structure, exact archive formats, exact implementation-specific storage rules, or exact automation scripts.

Those concerns belong to later storage specifications, implementation profiles, reference implementations, operational guides, templates, validators, migration specifications, backup specifications, synchronization specifications, and tool-specific setup documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Storage Standard refers to Layer 2 of The Brain Standard, responsible for defining how knowledge and source material may be stored, organized, referenced, moved, preserved, backed up, synchronized, indexed, imported, exported, and migrated without defining knowledge meaning.
- Storage Architecture refers to the standard-level organization of storage responsibilities, storage boundaries, storage environments, storage areas, storage representations, preservation expectations, and storage behavior within The Brain Standard.
- Storage Environment refers to any vault, repository, directory structure, database, file system, archive, export package, backup location, synchronization target, implementation workspace, or future storage medium used to store governed entities.
- Vault refers to a practical storage environment or repository used by an implementation to store Source Material, Knowledge Records, standards, specifications, decisions, workflows, agent files, implementation files, supporting assets, or related artifacts.
- Repository refers to a storage environment that may support versioning, review, synchronization, collaboration, backup, migration, implementation work, or governed preservation.
- Folder refers to a storage-level container used to organize files, records, source artifacts, assets, implementation files, or other stored representations.
- File refers to a storage-level representation of Source Material, a Knowledge Record, a governed document, a specification, a workflow, an agent file, an implementation document, an asset, an export, a backup, or another stored artifact.
- Storage Location refers to the place where a file, record, source artifact, representation, archive, backup, export, implementation object, or supporting asset is stored.
- Storage Representation refers to a particular stored form of a governed entity, such as a Markdown file, source file, sidecar metadata file, database record, archive copy, export copy, backup copy, implementation cache, or future representation.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Validation refers to the process of checking whether a governed entity satisfies the applicable standards, specifications, metadata expectations, provenance expectations, relationship expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Import refers to the process of bringing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, Source References, provenance, or external content into a compliant environment.
- Export refers to the process of producing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, Source References, provenance, or external content from a compliant environment for use elsewhere.
- Migration refers to movement from one storage system, implementation, representation, schema, vault, repository, database, file format, workflow environment, or tool environment to another.
- Backup refers to preserving a copy of a governed entity for restoration, continuity, archival, audit, migration, disaster recovery, or long-term preservation.
- Synchronization refers to copying, mirroring, syncing, replicating, caching, or transmitting a governed entity across devices, repositories, vaults, services, tools, implementations, or environments.
- Indexing refers to making a governed entity searchable, retrievable, ranked, embedded, summarized, vectorized, cached, tagged, categorized, or otherwise discoverable by a system, agent, workflow, validator, or implementation.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of SS-0001 is to define the standard-level storage architecture for The Brain Standard.

SS-0001 defines how storage environments, vaults, repositories, folders, files, archives, source-material areas, Knowledge Records, drafts, approved records, implementation files, supporting assets, exports, backups, synchronization targets, and migration packages should preserve governed knowledge without becoming the source of knowledge meaning.

Storage exists to preserve access, organization, durability, recovery, movement, inspection, and practical use.

Storage does not define knowledge meaning.

Knowledge meaning is defined by Layer 1 through Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility expectations, and governed structure.

SS-0001 exists to prevent storage confusion.

Storage confusion occurs when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, or implementations cannot reliably determine:

- whether a stored item is Source Material, a Knowledge Record, a governed standard, a specification, a decision, an implementation file, a workflow file, an agent file, a supporting asset, a backup, an export, a draft, or another storage representation;
- whether folder placement defines meaning or merely supports organization;
- whether filename changes affect Object Identity;
- whether moving a file changes the governed meaning of the entity;
- whether copied files represent the same Knowledge Object, a duplicate, a derivative object, a backup copy, an export copy, a migrated copy, or an implementation-specific copy;
- whether Source Material remains distinguishable from Knowledge Records;
- whether storage preserves metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and compatibility expectations;
- whether storage behavior has exposed restricted knowledge, broken provenance, weakened validation, hidden lifecycle state, weakened authority boundaries, or created implementation lock-in.

SS-0001 defines storage architecture for:

- storage environments;
- vaults;
- repositories;
- folders;
- files;
- source-material areas;
- Knowledge Record storage;
- governed document storage;
- draft storage;
- approved record storage;
- implementation file storage;
- supporting asset storage;
- archive storage;
- backup storage;
- synchronization storage;
- import storage;
- export storage;
- migration storage;
- indexing support;
- storage validation expectations;
- storage compatibility expectations.

SS-0001 does not define exact folder paths, exact filenames, exact file extensions, exact Markdown front matter syntax, exact schemas, exact database layouts, exact archive formats, exact backup tools, exact synchronization tools, exact indexing tools, exact Obsidian settings, exact Codex instructions, exact agent workspaces, exact scripts, exact operating-system conventions, or exact implementation-specific storage behavior.

Those concerns belong to later storage specifications, implementation profiles, reference implementations, validators, templates, operational guides, migration specifications, backup specifications, synchronization specifications, indexing specifications, and tool-specific setup documents.

SS-0001 defines storage behavior at the standard level.

A future storage specification MAY define exact folder structures, file naming rules, archive layouts, source-material storage rules, Knowledge Record placement rules, draft handling, approved record handling, export packaging, backup behavior, synchronization rules, indexing rules, migration staging rules, or validation checks.

Such specifications are valid only when they preserve the storage-architecture behavior defined by SS-0001.

The primary purpose of SS-0001 is to ensure that storage remains durable, inspectable, portable, reviewable, privacy-respecting, validation-compatible, migration-compatible, implementation-independent, and practical for daily use.

SS-0001 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, and implementations can determine:

- where governed entities may be stored;
- what kind of stored representation is being used;
- whether a stored item is Source Material, a Knowledge Record, a governed document, an implementation file, an agent file, a workflow file, a backup, an export, an archive, or another artifact;
- whether storage preserves Object Identity;
- whether storage preserves metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and compatibility expectations;
- whether Source Material and Knowledge Records remain distinguishable;
- whether storage supports import, export, migration, backup, synchronization, indexing, and restoration without redefining knowledge meaning;
- whether storage behavior can be preserved without relying on hidden application state, folder placement, filename convention, user memory, agent memory, workflow memory, plugin behavior, database internals, or undocumented implementation behavior.

## 2. Relationship to Prior Standards

SS-0001 is subordinate to and derived from the constitutional foundation of The Brain Standard.

SS-0001 depends on:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- KS-0001 — Knowledge Object Model;
- KS-0002 — Object Identity Standard;
- KS-0003 — Metadata Standard;
- KS-0004 — Relationship Standard;
- KS-0005 — Source Reference and Provenance Standard;
- KS-0006 — Lifecycle State Standard;
- KS-0007 — Authority Level Standard;
- KS-0008 — Privacy Classification Standard;
- KS-0009 — Validation Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

SS-0001 applies that purpose by defining storage behavior that preserves knowledge across files, folders, vaults, repositories, archives, exports, backups, synchronization targets, migration packages, databases, and future storage systems without allowing any one storage method to become the standard itself.

TB-0001 establishes the architecture principles that govern The Brain Standard.

SS-0001 applies those principles by requiring storage architecture to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- source distinction;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability;
- governed evolution.

TB-0002 establishes the layered architecture of The Brain Standard.

SS-0001 belongs to Layer 2 — Storage Standard.

Layer 2 defines how knowledge and source material may be stored, organized, referenced, moved, preserved, backed up, synchronized, indexed, imported, exported, and migrated without defining knowledge meaning.

Layer 2 depends on Layer 1.

Layer 2 MUST preserve the identity, structure, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and compatibility expectations defined by Layer 1.

Layer 2 MUST NOT redefine the core meaning of knowledge.

Layer 2 MUST NOT treat folder placement, filename, storage location, vault position, repository path, database table, archive location, sync location, backup location, index location, or implementation-specific storage behavior as the sole source of critical meaning.

TB-0003 establishes the governance model for The Brain Standard.

SS-0001 follows the document authority hierarchy defined by TB-0003. As a standard-level document, SS-0001 has high authority within its scope but remains subordinate to constitutional documents.

KS-0001 defines the foundational Knowledge Object Model.

SS-0001 does not replace the Knowledge Object Model.

SS-0001 preserves the rule that Knowledge Objects and Knowledge Records remain interpretable through explicit identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and governed structure rather than storage placement.

KS-0002 defines Object Identity.

SS-0001 depends on KS-0002 because storage must preserve Object Identity without defining it.

A Knowledge Object MUST NOT receive a new Object Identity merely because it is moved, renamed, copied, backed up, restored, synchronized, exported, imported, migrated, archived, indexed, cached, displayed, or stored in a different implementation.

KS-0003 defines metadata behavior.

SS-0001 depends on KS-0003 because storage may hold, organize, preserve, display, index, validate, migrate, import, export, back up, or synchronize metadata without redefining metadata meaning.

Storage metadata MAY exist.

Storage metadata MUST remain distinguishable from standard metadata unless a governed standard or specification defines its standard meaning.

KS-0004 defines relationship behavior.

SS-0001 depends on KS-0004 because storage may preserve, display, index, export, import, migrate, or synchronize relationships without redefining relationship meaning.

Folder proximity, file adjacency, backlink behavior, graph placement, search ranking, or implementation-specific links MUST NOT become the sole source of relationship meaning.

KS-0005 defines Source Reference and Provenance behavior.

SS-0001 depends on KS-0005 because storage must preserve Source Material, Source References, provenance, evidence context, attribution, extraction history, transformation history, import provenance, export provenance, migration provenance, and source availability context without confusing Source Material with Knowledge Records.

KS-0006 defines Lifecycle State behavior.

SS-0001 depends on KS-0006 because storage may support lifecycle handling, but storage location MUST NOT define Lifecycle State by itself when lifecycle state affects governed interpretation or handling.

KS-0007 defines Authority Level behavior.

SS-0001 depends on KS-0007 because storage may support authority handling, but storage location, folder placement, repository area, publication location, or implementation visibility MUST NOT define Authority Level by itself.

KS-0008 defines Privacy Classification behavior.

SS-0001 depends on KS-0008 because storage may expose, restrict, synchronize, index, export, back up, migrate, publish, or cache governed entities.

Storage architecture MUST preserve Privacy Classification and MUST NOT expose restricted knowledge merely because it is easier to organize, index, synchronize, back up, export, publish, or process.

KS-0009 defines Validation behavior.

SS-0001 depends on KS-0009 because storage architecture must support validation of storage representations, storage boundaries, source distinction, metadata preservation, relationship preservation, provenance preservation, lifecycle preservation, authority preservation, privacy preservation, compatibility, import, export, migration, backup, synchronization, indexing, and implementation independence.

Validation success MUST NOT be confused with storage success.

Storage success MUST NOT be confused with full conformance unless the applicable validation scope explicitly permits that interpretation.

SS-0001 is successful when it extends the prior standards into a clear storage architecture without weakening Object Identity, metadata role boundaries, relationship behavior, source-reference behavior, provenance preservation, Lifecycle State, Authority Level, Privacy Classification, Validation, implementation independence, or practical daily usability.

## 3. Storage Definition

Storage is the set of environments, structures, representations, locations, containers, files, archives, repositories, backups, synchronization targets, export packages, migration packages, indexes, and implementation-specific storage mechanisms used to preserve, organize, access, move, review, validate, restore, synchronize, import, export, migrate, or present governed entities within The Brain Standard.

Storage exists to preserve access to knowledge and source material.

Storage does not create knowledge meaning by itself.

A storage environment MAY contain:

- Source Material;
- Knowledge Objects;
- Knowledge Records;
- metadata records;
- relationship records;
- Source References;
- provenance records;
- validation results;
- lifecycle records;
- authority records;
- privacy records;
- standards;
- specifications;
- ADRs;
- RFCs;
- implementation documents;
- workflow documents;
- agent documents;
- operational guides;
- templates;
- source archives;
- drafts;
- approved records;
- deprecated records;
- superseded records;
- rejected records;
- backups;
- exports;
- imports;
- migration packages;
- indexes;
- caches;
- supporting assets;
- implementation-specific files.

A storage representation MAY be a file, folder, database row, archive entry, sidecar record, export item, backup copy, synchronized copy, migrated copy, index entry, cache entry, implementation object, or future representation.

A storage representation MUST remain distinguishable from the governed entity it represents where that distinction affects identity, meaning, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, import, export, migration, backup, synchronization, indexing, or implementation replacement.

A file may represent a Knowledge Record.

A folder may organize Knowledge Records.

A vault may store Knowledge Records.

A database may index Knowledge Records.

An archive may preserve Knowledge Records.

A backup may copy Knowledge Records.

An export may package Knowledge Records.

A migration may move Knowledge Records.

An implementation may display Knowledge Records.

None of these storage mechanisms define the Knowledge Object by themselves.

A storage location MAY support usability, navigation, review, routing, access control, synchronization, backup, indexing, implementation behavior, or workflow execution.

A storage location MUST NOT be the sole source of:

- Object Identity;
- Knowledge Object meaning;
- Knowledge Record interpretation;
- object type;
- relationship meaning;
- Source Reference meaning;
- provenance meaning;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- approval;
- publication permission;
- export permission;
- synchronization permission;
- indexing permission;
- backup permission;
- agent-use permission;
- workflow-use permission;
- implementation-use permission;
- downstream-use permission.

Storage SHOULD preserve enough explicit information for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, and implementations to determine what the stored entity is, what governed meaning applies, what source support exists, what provenance exists, what relationships exist, what lifecycle state applies, what authority applies, what privacy boundaries apply, what validation state applies, and what compatibility expectations apply.

Storage MAY support multiple representations of the same governed entity.

Multiple representations MUST NOT create identity confusion.

A copied, backed-up, synchronized, exported, imported, migrated, archived, cached, indexed, or implementation-specific representation SHOULD preserve the governed identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and compatibility context required by the applicable standards.

Storage SHOULD support human inspection where practical.

Storage SHOULD support AI interpretation where practical.

Storage SHOULD support validation where practical.

Storage SHOULD support migration where practical.

Storage SHOULD support restoration where practical.

Storage SHOULD support privacy-preserving organization, indexing, synchronization, backup, export, import, and migration.

Storage MUST remain implementation-independent at the standard level.

A compliant storage architecture MAY be realized through Markdown files, plain-text repositories, vaults, databases, file systems, archives, object stores, graph stores, cloud repositories, local repositories, hybrid systems, or future storage media.

The storage method may vary by implementation.

The governed meaning of knowledge MUST remain portable across storage methods.

Storage is successful when it preserves governed entities without becoming the authority that defines them.

## 4. Storage Requirements

Storage Requirements define the minimum behavior required for storage architecture to preserve governed entities under The Brain Standard.

A compliant storage architecture SHALL preserve the distinction between knowledge meaning and storage organization.

Storage MAY organize, locate, display, group, copy, synchronize, back up, index, archive, export, import, migrate, or restore governed entities.

Storage MUST NOT define the governed meaning of those entities by itself.

A storage environment SHALL preserve or support preservation of:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- compatibility expectations;
- import context;
- export context;
- migration context;
- backup context;
- synchronization context;
- indexing context where applicable;
- implementation-independence expectations.

Storage MUST NOT make critical meaning dependent only on:

- folder placement;
- filename;
- file extension;
- vault location;
- repository path;
- database table;
- archive location;
- backup location;
- synchronization target;
- index location;
- cache location;
- tag convention;
- application view;
- plugin behavior;
- user-interface state;
- hidden application state;
- agent memory;
- workflow memory;
- undocumented implementation behavior.

Those signals MAY support usability, navigation, search, routing, automation, review, validation, synchronization, backup, indexing, or implementation behavior.

They MUST NOT replace explicit governed meaning where meaning affects identity, interpretation, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, import, export, migration, backup, synchronization, indexing, agent use, workflow use, implementation use, or downstream use.

A compliant storage architecture SHALL preserve Source Material and Knowledge Records as distinguishable storage concerns.

Source Material MAY be stored near Knowledge Records, stored in a separate source-material area, stored in an archive, referenced externally, or represented through another governed storage method.

Any storage method MAY be compliant if Source References, provenance, source availability, source privacy, and source distinction remain preserved.

A compliant storage architecture SHALL support multiple storage representations where needed.

Multiple representations MAY include:

- working copies;
- draft copies;
- approved copies;
- archived copies;
- backup copies;
- synchronized copies;
- exported copies;
- imported copies;
- migrated copies;
- cached copies;
- indexed representations;
- implementation-specific representations.

Multiple representations MUST NOT create identity confusion.

Where multiple representations exist, storage SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, and implementations to determine:

- whether the representations refer to the same governed entity;
- whether one representation is a copy, backup, export, import, migration, derivative, duplicate, cache, index, archive, or implementation-specific representation;
- which representation is current where currentness matters;
- which representation is historical where historical preservation matters;
- which representation is authoritative within the applicable scope;
- which representation is restricted where privacy applies;
- which representation has passed validation within the applicable validation scope;
- what provenance supports the representation;
- what compatibility expectations apply.

Storage SHOULD remain human-inspectable where practical.

A future human SHOULD be able to inspect the storage environment and determine the purpose of stored areas, stored records, stored source material, stored governed documents, stored implementation files, stored assets, stored exports, stored backups, and stored migration packages without relying only on hidden tooling.

Storage SHOULD remain AI-readable where practical.

A future agent SHOULD be able to interpret storage purpose, storage boundaries, source distinction, record distinction, lifecycle handling, privacy handling, validation expectations, and migration context from explicit structure, metadata, documentation, or governed storage rules.

Storage SHOULD remain portable.

A compliant storage architecture SHOULD support movement between storage environments without semantic loss.

A compliant storage architecture MUST NOT require a specific application, vendor, plugin, database, cloud service, local operating system, synchronization tool, backup tool, indexer, or user interface for governed knowledge to remain understandable.

Storage SHOULD support local-first preservation where practical.

Cloud storage, hosted databases, synchronization services, remote archives, and external storage systems MAY be used as implementation choices.

They MUST NOT become required for the governed meaning of knowledge to remain understandable, inspectable, portable, or preservable.

Storage MUST preserve privacy boundaries.

A storage environment MUST NOT expose restricted knowledge merely because it is easier to organize, search, synchronize, back up, index, export, publish, migrate, cache, or process.

Storage SHOULD support validation.

A validator SHOULD be able to determine whether storage preserves the applicable identity, metadata, relationship, Source Reference, provenance, lifecycle, authority, privacy, compatibility, import, export, migration, backup, synchronization, indexing, and implementation-independence expectations.

Storage SHOULD support recovery.

A compliant storage architecture SHOULD allow governed entities to be restored after accidental deletion, corruption, synchronization failure, migration failure, implementation failure, or storage replacement where practical.

Storage SHOULD support governed evolution.

Storage conventions MAY change over time through approved standards, specifications, implementation profiles, migration rules, or operational guides.

A storage change MUST NOT silently break Object Identity, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, import behavior, export behavior, migration behavior, backup behavior, synchronization behavior, indexing behavior, or downstream use.

Storage Requirements are successful when storage remains durable, explicit, reviewable, privacy-respecting, portable, validation-compatible, migration-compatible, and implementation-independent without becoming the authority that defines knowledge meaning.

## 5. Storage Categories

Storage Categories organize storage responsibilities by architectural purpose.

Storage Categories help humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, and implementations understand what kind of stored material is being handled and what standard expectations apply.

SS-0001 defines Storage Categories at the conceptual standard level.

SS-0001 does not define exact folder names, exact file paths, exact filename formats, exact archive structures, exact database tables, exact repository layouts, exact sync targets, exact backup schedules, exact index formats, or exact implementation-specific locations.

A future storage specification MAY define those details.

At minimum, The Brain Standard recognizes the following Storage Categories:

- Source Material storage;
- Knowledge Record storage;
- governed document storage;
- draft and review storage;
- approved record storage;
- deprecated, superseded, rejected, and archived storage;
- implementation file storage;
- workflow and agent storage;
- supporting asset storage;
- metadata, relationship, and validation storage;
- import, export, and migration storage;
- backup, synchronization, and restoration storage;
- indexing and cache storage.

### 5.1 Source Material Storage

Source Material storage preserves original or referenced material used as evidence, input, origin, context, attribution, or reference material.

Source Material storage MAY contain original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical-artifact records, external references, or other source artifacts.

Source Material storage MUST preserve the distinction between Source Material and Knowledge Records.

Source Material storage SHOULD support Source References, provenance, source availability, source privacy, source validation, import context, export context, migration context, backup context, and preservation context where applicable.

### 5.2 Knowledge Record Storage

Knowledge Record storage preserves structured representations of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.

Knowledge Record storage MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and compatibility expectations where applicable.

Knowledge Record storage MUST NOT rely only on folder placement, filename, or implementation-specific organization to define Knowledge Object meaning.

### 5.3 Governed Document Storage

Governed document storage preserves constitutional documents, standards, specifications, ADRs, RFCs, implementation documents, operational documents, guides, procedures, and other governed documents.

Governed document storage SHOULD preserve document identity, document title, version, status, authority, phase, milestone, dependencies, supersession, related documents, lifecycle state, approval context, and compatibility context where applicable.

Governed document storage MUST preserve the authority hierarchy defined by the constitutional foundation.

### 5.4 Draft and Review Storage

Draft and review storage supports entities that are being created, revised, inspected, validated, corrected, routed, or prepared for approval.

Draft and review storage MAY contain incomplete records, proposed standards, proposed specifications, proposed relationships, proposed Source References, agent outputs, workflow outputs, validation findings, correction notes, or review packages.

Draft and review storage MUST NOT cause draft material to be treated as approved merely because it is visible, indexed, synchronized, backed up, exported, or stored in the same environment as approved material.

### 5.5 Approved Record Storage

Approved record storage supports governed entities accepted for use within their defined scope.

Approved record storage MAY contain approved Knowledge Records, approved standards, approved specifications, approved decisions, approved workflows, approved implementation documents, or other approved governed entities.

Approved record storage MUST preserve approval scope, authority context, lifecycle state, provenance, privacy classification, validation context, and compatibility expectations where applicable.

Storage in an approved area MUST NOT imply broader authority, broader publication permission, broader export permission, broader synchronization permission, broader indexing permission, or broader downstream-use permission than the governed metadata and applicable standards allow.

### 5.6 Deprecated, Superseded, Rejected, and Archived Storage

Deprecated, superseded, rejected, and archived storage preserves historical, compatibility, audit, migration, governance, source-reference, provenance, or recovery context.

This storage category MAY contain entities that are no longer current, no longer recommended, replaced, rejected, preserved for historical review, or held for compatibility purposes.

Storage in this category MUST preserve enough context to distinguish deprecated, superseded, rejected, archived, current, approved, restricted, quarantined, and needs-repair entities where those distinctions affect interpretation or handling.

Historical preservation MUST NOT imply current approval, current authority, current validation, publication permission, export permission, synchronization permission, indexing permission, or downstream-use permission.

### 5.7 Implementation File Storage

Implementation file storage preserves files used by a specific software tool, vault, database, plugin, interface, automation, script, agent system, workflow environment, or future implementation.

Implementation file storage MAY support practical operation.

Implementation file storage MUST NOT define The Brain Standard by itself.

Implementation-specific files MAY demonstrate or realize standard behavior, but they MUST remain subordinate to the governed standards and specifications.

### 5.8 Workflow and Agent Storage

Workflow and agent storage preserves workflow definitions, agent instructions, agent role descriptions, permission boundaries, activity records, handoff notes, validation outputs, routing records, review records, or automation-supporting files.

Workflow and agent storage MUST preserve reviewability, traceability, privacy boundaries, authority limits, validation context, and implementation independence where applicable.

Agent or workflow storage MUST NOT allow agents or workflows to become unreviewable authorities over Object Identity, metadata meaning, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, publication, export, synchronization, indexing, backup, or downstream use.

### 5.9 Supporting Asset Storage

Supporting asset storage preserves non-primary files that assist interpretation, presentation, review, implementation, validation, migration, or use.

Supporting assets MAY include images, diagrams, attachments, figures, exports, reports, generated artifacts, logs, helper files, templates, examples, or reference assets.

Supporting asset storage SHOULD make clear whether an asset is Source Material, evidence, illustration, implementation support, workflow support, validation output, generated material, or another governed storage representation.

### 5.10 Metadata, Relationship, and Validation Storage

Metadata, relationship, and validation storage preserves explicit context needed to interpret, connect, validate, migrate, import, export, review, or govern stored entities.

This storage category MAY include sidecar files, embedded metadata, relationship records, validation records, schema-supporting files, compatibility notes, migration mappings, or future governed representations.

Metadata, relationship, and validation storage MUST preserve the standard meaning of the governed information without making storage mechanism the source of that meaning.

### 5.11 Import, Export, and Migration Storage

Import, export, and migration storage supports controlled movement of governed entities into, out of, or between compliant environments.

This storage category MAY contain staging areas, import packages, export packages, migration packages, mapping files, transformation records, compatibility reports, validation results, or review records.

Import, export, and migration storage MUST preserve enough context to determine what changed, what moved, what was transformed, what identity was preserved, what provenance applies, what validation was performed, what privacy boundaries apply, and what compatibility expectations remain.

### 5.12 Backup, Synchronization, and Restoration Storage

Backup, synchronization, and restoration storage supports continuity, recovery, redundancy, device movement, repository mirroring, archival preservation, and disaster recovery.

This storage category MAY contain backup copies, synchronized copies, restore points, archive snapshots, replicated repositories, continuity packages, or recovery metadata.

Backup, synchronization, and restoration storage MUST preserve privacy boundaries and MUST NOT silently create unauthorized exposure, publication, export, indexing, agent access, workflow access, implementation access, or downstream use.

### 5.13 Indexing and Cache Storage

Indexing and cache storage supports search, retrieval, ranking, embedding, summarization, discovery, performance, or implementation convenience.

Indexing and cache storage MAY contain search indexes, vector indexes, summaries, previews, embeddings, derived metadata, temporary files, implementation caches, or retrieval-supporting structures.

Indexing and cache storage MUST NOT become the sole source of critical meaning.

Indexing and cache storage MUST respect Privacy Classification, provenance, validation scope, lifecycle state, authority limits, source-reference expectations, and downstream-use boundaries.

Storage Categories are successful when stored material remains understandable by category without allowing the category, folder, repository area, implementation view, or storage mechanism to define governed meaning by itself.

## 6. Storage Environment Boundaries

Storage Environment Boundaries define how storage environments separate, relate, expose, preserve, synchronize, index, back up, export, import, migrate, and protect governed entities.

A storage environment boundary is a conceptual boundary around a vault, repository, directory structure, database, archive, export package, backup location, synchronization target, implementation workspace, or future storage medium.

A storage environment boundary MAY be physical, logical, procedural, implementation-specific, or governed by specification.

A physical boundary MAY include a device, drive, folder tree, repository, database, archive, backup medium, or storage volume.

A logical boundary MAY include a vault, workspace, collection, access group, privacy scope, lifecycle scope, implementation profile, migration package, export package, or indexing scope.

A procedural boundary MAY include workflow routing, review handling, import staging, export staging, backup procedure, synchronization procedure, validation process, or migration process.

An implementation-specific boundary MAY include application settings, plugin behavior, database partitions, file-system conventions, cloud-service folders, index partitions, workspace views, or tool-specific storage areas.

Storage environment boundaries MAY support usability, access control, privacy protection, validation, review, synchronization, backup, import, export, migration, indexing, caching, and implementation behavior.

Storage environment boundaries MUST NOT define Object Identity, Knowledge Object meaning, relationship meaning, Source Reference meaning, provenance meaning, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication permission, export permission, synchronization permission, indexing permission, backup permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission by themselves.

A compliant storage environment SHOULD make its boundaries explicit where those boundaries affect:

- access;
- visibility;
- privacy;
- lifecycle handling;
- authority handling;
- validation;
- source distinction;
- provenance preservation;
- relationship preservation;
- import behavior;
- export behavior;
- migration behavior;
- backup behavior;
- synchronization behavior;
- indexing behavior;
- agent behavior;
- workflow behavior;
- implementation behavior;
- downstream use.

A storage environment MAY contain multiple areas with different purposes.

Different storage areas MAY support:

- source preservation;
- knowledge records;
- governed documents;
- draft work;
- review work;
- approved records;
- deprecated records;
- superseded records;
- rejected records;
- archived records;
- implementation files;
- workflow files;
- agent files;
- supporting assets;
- imports;
- exports;
- migrations;
- backups;
- synchronized copies;
- indexes;
- caches.

Storage areas SHOULD be distinguishable enough that humans, agents, workflows, validators, storage systems, and implementations can determine the intended purpose of the area.

Storage area purpose MUST NOT replace governed metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, or compatibility expectations.

A storage environment MAY contain restricted and less-restricted material.

When privacy boundaries differ within the same storage environment, the storage architecture MUST preserve those boundaries.

A restricted entity MUST NOT become less restricted merely because it is copied, moved, linked, indexed, synchronized, backed up, exported, imported, migrated, cached, previewed, summarized, or stored near less-restricted material.

A storage environment MAY contain current and historical material.

When current and historical material exist in the same storage environment, the storage architecture SHOULD preserve their lifecycle distinctions.

A deprecated, superseded, rejected, archived, quarantined, or needs-repair entity MUST NOT be treated as current or approved merely because it remains stored, visible, searchable, indexed, synchronized, backed up, exported, imported, migrated, or accessible.

A storage environment MAY contain standard-level files and implementation-level files.

When standards and implementation files exist in the same storage environment, the storage architecture MUST preserve their authority distinction.

An implementation file MUST NOT override a constitutional document, standard, or specification.

An implementation file MAY demonstrate, apply, configure, or operationalize a standard only within the limits allowed by the applicable governed documents.

A storage environment MAY contain source material and Knowledge Records.

When Source Material and Knowledge Records exist in the same storage environment, the storage architecture MUST preserve their distinction.

A Source Material file MUST NOT become a Knowledge Record merely because it is stored near, linked from, summarized by, indexed with, synchronized with, exported with, or displayed beside a Knowledge Record.

A Knowledge Record MUST NOT become original Source Material merely because it cites, embeds, extracts, summarizes, or transforms Source Material.

A storage environment MAY be replaced.

Storage replacement MUST preserve the governed meaning, identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility expectations, and privacy boundaries required by the applicable standards.

A storage environment boundary is successful when it supports organization, access, preservation, validation, privacy, backup, synchronization, indexing, import, export, migration, and implementation behavior without becoming the authority that defines governed meaning.

## 7. Storage Representation Rules

Storage Representation Rules define how stored forms of governed entities should behave across files, folders, repositories, vaults, databases, archives, exports, backups, synchronization targets, indexes, caches, implementation workspaces, and future storage systems.

A Storage Representation is not automatically the governed entity itself.

A Storage Representation is the stored form through which a governed entity is preserved, accessed, displayed, indexed, synchronized, backed up, exported, imported, migrated, restored, or processed.

A Storage Representation MAY include:

- a Markdown file;
- a plain-text file;
- a source file;
- a binary file;
- a sidecar metadata file;
- a database record;
- an archive entry;
- an export item;
- an import item;
- a migration item;
- a backup copy;
- a synchronized copy;
- an indexed representation;
- a cached representation;
- an implementation-specific object;
- a future storage form.

A Storage Representation MUST preserve the governed meaning of the entity it represents where that meaning affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, import, export, migration, backup, synchronization, indexing, restoration, implementation replacement, or downstream use.

A Storage Representation MUST NOT become the sole source of governed meaning merely because it is visible, editable, searchable, linked, indexed, synchronized, backed up, exported, imported, migrated, restored, or displayed by an implementation.

A file MAY represent a Knowledge Record.

A file MAY contain Source Material.

A file MAY contain a governed document.

A file MAY contain implementation support material.

A file MAY contain workflow or agent support material.

A file MAY contain supporting assets.

A file MAY contain metadata, relationship, provenance, validation, import, export, migration, backup, synchronization, or indexing context.

The file type does not define the governed role by itself.

A Markdown file does not automatically define a Knowledge Record.

A PDF does not automatically define Source Material.

A database row does not automatically define Object Identity.

A folder does not automatically define Lifecycle State.

An index entry does not automatically define authority.

A synchronized copy does not automatically define publication permission.

A backup copy does not automatically define approval.

A Storage Representation SHOULD make its governed role explicit where role affects interpretation or handling.

A Storage Representation SHOULD support identification of:

- what governed entity is represented;
- what storage role the representation serves;
- whether the representation is current or historical;
- whether the representation is a draft, review copy, approved copy, archive copy, backup copy, export copy, import copy, migration copy, cache, index, or implementation-specific representation;
- what Object Identity applies where applicable;
- what metadata applies where applicable;
- what Source References apply where applicable;
- what provenance applies where applicable;
- what relationships apply where applicable;
- what Lifecycle State applies where applicable;
- what Authority Level applies where applicable;
- what Privacy Classification applies where applicable;
- what Validation State or validation expectations apply where applicable;
- what compatibility expectations apply where applicable.

Multiple Storage Representations MAY exist for the same governed entity.

Multiple Storage Representations MUST NOT create identity confusion.

Where multiple Storage Representations exist, the storage architecture SHOULD preserve enough context to determine whether each representation is:

- the primary working representation;
- a secondary representation;
- a draft representation;
- a review representation;
- an approved representation;
- a deprecated representation;
- a superseded representation;
- a rejected representation;
- an archived representation;
- a backup representation;
- a synchronized representation;
- an exported representation;
- an imported representation;
- a migrated representation;
- a cached representation;
- an indexed representation;
- an implementation-specific representation;
- a derivative representation;
- a duplicate representation.

A Storage Representation MAY be transformed.

Transformation MAY include format conversion, extraction, summarization, translation, indexing, embedding, packaging, compression, encryption, redaction, normalization, migration, export, import, backup, restoration, or implementation-specific conversion.

A transformation MUST preserve or record enough provenance to determine what changed where the transformation affects identity, meaning, source distinction, metadata, relationships, Source References, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, publication, export, synchronization, indexing, backup, migration, or downstream use.

A Storage Representation MAY be copied.

A copy MUST NOT be treated as a new Knowledge Object merely because it exists in a different folder, repository, archive, backup, synchronization target, export package, migration package, implementation workspace, or storage medium.

A copy MAY become a derivative, duplicate, migrated representation, export copy, backup copy, archive copy, or implementation-specific representation when a governed process or standard-level interpretation defines that role.

A Storage Representation MAY be deleted, archived, restored, moved, renamed, indexed, synchronized, exported, imported, migrated, cached, or regenerated.

Those actions MUST NOT silently remove, replace, reinterpret, expose, or weaken governed meaning where the affected entity requires preservation of Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, or compatibility expectations.

A Storage Representation MAY contain implementation-specific information.

Implementation-specific information MUST remain distinguishable from governed standard meaning unless a governed standard or specification explicitly defines its standard role.

A compliant storage architecture SHOULD allow Storage Representations to be inspected without requiring hidden application state.

Storage Representation Rules are successful when stored forms remain useful, portable, reviewable, privacy-respecting, validation-compatible, and migration-compatible without becoming the authority that defines the governed entity by themselves.

## 8. Source Material Storage

Source Material Storage defines how original or referenced material should be preserved, organized, protected, reviewed, referenced, backed up, synchronized, indexed, imported, exported, migrated, or restored within The Brain Standard.

Source Material includes original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical-artifact records, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.

Source Material storage exists to preserve evidence, origin, context, attribution, and reviewability.

Source Material storage does not transform Source Material into a Knowledge Record by itself.

A Source Material file MUST remain distinguishable from a Knowledge Record.

A source file MAY be cited by a Knowledge Record.

A source file MAY be summarized by a Knowledge Record.

A source file MAY be extracted into a Knowledge Record.

A source file MAY be classified by an agent or workflow.

A source file MAY be indexed for retrieval.

A source file MAY be archived for preservation.

A source file MAY be migrated, exported, imported, synchronized, backed up, cached, or restored.

None of these actions automatically make the source file a Knowledge Record.

Source Material Storage SHOULD preserve enough context to determine:

- what the Source Material is;
- where the Source Material came from where known;
- whether the Source Material is original, copied, imported, exported, migrated, archived, externally referenced, unavailable, restricted, or partially available;
- what Source Identifier, external reference, archive reference, citation, or storage reference applies where applicable;
- what Knowledge Records reference the Source Material where applicable;
- what provenance applies to the Source Material;
- whether extraction, transformation, summarization, translation, redaction, or classification has occurred;
- whether the Source Material has privacy restrictions;
- whether the Source Material has authority or reliability context;
- whether the Source Material has validation concerns;
- whether the Source Material remains available for review;
- whether the Source Material may be exported, synchronized, indexed, backed up, migrated, published, or used downstream.

Source Material Storage MUST preserve Source References where Source Material materially supports a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, validation result, migration record, import record, export record, or other governed entity.

Source Material Storage MUST preserve provenance where provenance affects interpretation, authority, privacy, validation, lifecycle state, source availability, source reliability, migration, import, export, publication, or downstream use.

Source Material Storage MUST preserve privacy boundaries.

Restricted Source Material MUST NOT become less restricted merely because it is stored near less-restricted material, linked from a Knowledge Record, indexed, synchronized, backed up, exported, imported, migrated, cached, previewed, summarized, or processed by an agent or workflow.

Source Material Storage SHOULD support source availability tracking where availability affects interpretation or validation.

Source availability context MAY indicate that Source Material is available, unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, or otherwise limited.

Source Material Storage SHOULD support source integrity where practical.

Source integrity support MAY include preserving original files, recording transformations, preserving import context, preserving migration context, preserving checks or validation results, or documenting known limitations.

SS-0001 does not require a specific checksum method, archive method, file naming method, folder structure, citation style, database field, storage path, or preservation tool.

Those details belong to future specifications, implementation profiles, validation rules, archival specifications, or operational guides.

Source Material MAY be stored locally, externally, in an archive, in a repository, in a database, in an implementation workspace, in a backup, in an export package, in a migration package, or through a governed external reference.

External Source Material MAY be referenced without being fully copied into a compliant storage environment.

When Source Material is externally referenced, the storage architecture SHOULD preserve enough information to determine how the source may be found, whether it remains available, whether access is restricted, what provenance applies, and whether the external dependency affects validation, migration, export, backup, restoration, or downstream use.

Source Material Storage SHOULD support extraction and transformation traceability.

When Source Material is extracted, summarized, translated, redacted, classified, embedded, indexed, converted, or otherwise transformed, the transformation SHOULD preserve enough provenance to determine:

- what Source Material was used;
- what part of the Source Material was used where applicable;
- what transformation occurred;
- who or what performed the transformation where applicable;
- when the transformation occurred where applicable;
- whether human review occurred where applicable;
- whether agent or workflow activity was involved;
- whether privacy restrictions apply;
- whether validation is required;
- whether the output is a Knowledge Record, derivative, cache, index, summary, export, migration item, or another governed representation.

Source Material Storage SHOULD support long-term preservation where the source materially supports governed knowledge.

Source Material Storage MAY support deletion or removal where governed retention, privacy, legal, operational, or storage constraints require it.

Deletion or removal MUST NOT silently break Source References, provenance, validation, lifecycle state, authority context, privacy context, migration context, import context, export context, or downstream interpretability where those remain required.

Source Material Storage is successful when Source Material remains identifiable, reviewable, privacy-respecting, source-reference-compatible, provenance-preserving, validation-compatible, migration-compatible, and distinguishable from Knowledge Records.

## 9. Knowledge Record Storage

Knowledge Record Storage defines how structured representations of knowledge should be preserved, organized, protected, reviewed, validated, indexed, synchronized, backed up, imported, exported, migrated, restored, or presented within The Brain Standard.

A Knowledge Record is a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.

Knowledge Record Storage exists to preserve structured knowledge in a durable, inspectable, portable, reviewable, and AI-readable form.

Knowledge Record Storage does not define Knowledge Object meaning by storage placement alone.

A Knowledge Record MUST remain interpretable through explicit governed structure.

A Knowledge Record SHOULD preserve or support preservation of:

- Object Identity;
- human-readable title or label where applicable;
- metadata;
- relationships;
- Source References where applicable;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State or validation expectations where applicable;
- compatibility expectations;
- import context where applicable;
- export context where applicable;
- migration context where applicable;
- backup context where applicable;
- synchronization context where applicable;
- indexing context where applicable.

Knowledge Record Storage MUST NOT rely only on folder placement, filename, file extension, vault location, repository path, application view, database row, tag, backlink behavior, index entry, graph position, agent memory, workflow memory, plugin behavior, or hidden implementation state to define the meaning of a Knowledge Record.

A Knowledge Record MAY be represented as a Markdown file, structured text file, database record, graph object, sidecar-linked record, archive entry, export item, migration item, implementation object, or future governed representation.

The representation method may vary by implementation.

The governed meaning of the Knowledge Record MUST remain portable across representation methods.

A Knowledge Record MAY be stored near related Source Material.

A Knowledge Record MAY be stored separately from related Source Material.

A Knowledge Record MAY reference Source Material stored externally.

A Knowledge Record MAY reference multiple Source Material items.

A Knowledge Record MAY exist without Source Material where it is created through human reasoning, governed decision-making, operational knowledge, agent-assisted drafting, workflow output, or another governed process.

Regardless of storage arrangement, Knowledge Record Storage MUST preserve the distinction between the Knowledge Record and any Source Material it references, summarizes, extracts, transforms, cites, embeds, or interprets.

Knowledge Record Storage SHOULD support lifecycle handling.

Draft, review, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending-validation, and needs-repair records SHOULD remain distinguishable where lifecycle state affects interpretation, authority, privacy, validation, publication, export, synchronization, indexing, backup, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Knowledge Record Storage SHOULD support authority handling.

Storage in an approved area, published area, standards area, archive area, implementation area, agent area, workflow area, export package, backup location, or repository MUST NOT define Authority Level by itself.

Authority Level MUST remain explicit, scoped, and governed where authority affects interpretation, review, validation, publication, export, migration, automation, or downstream use.

Knowledge Record Storage MUST preserve privacy boundaries.

A restricted Knowledge Record MUST NOT become less restricted merely because it is copied, moved, renamed, linked, indexed, synchronized, backed up, exported, imported, migrated, cached, previewed, summarized, embedded, or displayed by an implementation.

Knowledge Record Storage SHOULD support validation.

A validator SHOULD be able to determine whether a Knowledge Record satisfies applicable identity, metadata, relationship, Source Reference, provenance, lifecycle, authority, privacy, compatibility, import, export, migration, backup, synchronization, indexing, and implementation-independence expectations.

Knowledge Record Storage SHOULD support relationship preservation.

Relationships SHOULD remain meaningful when Knowledge Records are renamed, moved, copied, exported, imported, migrated, backed up, restored, synchronized, indexed, cached, summarized, translated, or displayed in another implementation.

Relationship meaning MUST NOT depend only on file adjacency, folder proximity, backlink behavior, graph visualization, search ranking, tag coincidence, implementation-specific links, or agent inference.

Knowledge Record Storage SHOULD support provenance preservation.

Where a Knowledge Record is created, modified, extracted, transformed, summarized, translated, reviewed, validated, approved, rejected, deprecated, superseded, archived, imported, exported, migrated, backed up, restored, synchronized, indexed, or processed by an agent or workflow, provenance SHOULD be preserved where that context affects interpretation, authority, privacy, validation, compatibility, publication, export, migration, or downstream use.

Knowledge Record Storage MAY support multiple representations of the same Knowledge Record.

Multiple representations MUST NOT create identity confusion.

Where a Knowledge Record has multiple representations, storage SHOULD preserve enough context to determine whether a representation is a working copy, draft copy, approved copy, archived copy, backup copy, synchronized copy, exported copy, imported copy, migrated copy, cached copy, indexed representation, implementation-specific representation, duplicate, derivative, or superseded representation.

Knowledge Record Storage SHOULD support human readability where practical.

A future human SHOULD be able to inspect a Knowledge Record and understand its purpose, identity, status, source context, provenance, relationships, privacy expectations, validation expectations, and authority context without relying only on hidden tooling.

Knowledge Record Storage SHOULD support AI readability where practical.

A future agent SHOULD be able to interpret a Knowledge Record through explicit structure, metadata, relationships, Source References, provenance, lifecycle state, authority, privacy classification, validation expectations, and storage context without relying on hidden memory or implementation-specific behavior.

Knowledge Record Storage SHOULD support export and migration.

A Knowledge Record SHOULD remain understandable and portable when exported, imported, migrated, backed up, restored, synchronized, indexed, cached, or accessed through another compliant implementation.

Knowledge Record Storage is successful when Knowledge Records remain identifiable, structured, portable, reviewable, privacy-respecting, source-reference-compatible, provenance-preserving, validation-compatible, migration-compatible, relationship-compatible, and distinguishable from Source Material.

## 10. Governed Document Storage

Governed Document Storage defines how constitutional documents, standards, specifications, ADRs, RFCs, implementation documents, operational documents, guides, procedures, templates, and other governed documents should be preserved, organized, reviewed, validated, archived, exported, imported, migrated, synchronized, backed up, restored, or presented within The Brain Standard.

Governed Document Storage exists to preserve the documents that define, explain, govern, implement, or operationalize The Brain Standard.

A governed document MAY include:

- a constitutional document;
- a standard;
- a specification;
- an ADR;
- an RFC;
- an implementation document;
- a reference implementation document;
- an operational guide;
- a procedure;
- a checklist;
- a template;
- a validator description;
- a migration note;
- a compatibility note;
- another governed document type defined by a future standard or specification.

Governed Document Storage MUST preserve document identity where document identity affects authority, versioning, supersession, lifecycle state, dependencies, compatibility, governance review, import, export, migration, validation, or downstream use.

A governed document SHOULD preserve or support preservation of:

- Document ID;
- title;
- version;
- status;
- authority;
- phase;
- milestone;
- dependencies;
- supersession;
- related documents;
- lifecycle state;
- approval context where applicable;
- provenance where applicable;
- validation context where applicable;
- compatibility expectations where applicable;
- privacy classification where applicable.

Governed Document Storage MUST preserve the authority distinction between constitutional documents, standards, specifications, ADRs, RFCs, implementation documents, reference implementations, and operational documents.

A lower-authority document MUST NOT override a higher-authority document merely because it is stored in a more visible location, edited more recently, indexed more strongly, linked more often, synchronized more broadly, published more widely, or used more frequently by an implementation, workflow, or agent.

Storage location MUST NOT define document authority by itself.

A document stored in a standards area is not authoritative unless its governed metadata, lifecycle state, authority level, approval context, and applicable governance rules support that interpretation.

A document stored in an archive area is not automatically obsolete unless its lifecycle state, supersession context, deprecation context, or governance record supports that interpretation.

A document stored in an implementation area is not automatically part of the standard.

A document stored in an operational area is not automatically a governed requirement.

Governed Document Storage SHOULD support versioning and historical preservation.

Versioning MAY be supported through filenames, document metadata, repository history, changelogs, version-control systems, archival copies, supersession records, migration records, or future governed mechanisms.

The versioning method does not define document authority by itself.

Versioning support MUST preserve enough context to determine which document version is current, historical, deprecated, superseded, rejected, archived, draft, review, or approved where those distinctions affect interpretation or use.

Governed Document Storage SHOULD preserve supersession and deprecation context.

A superseded document SHOULD remain historically interpretable where it affects compatibility, migration, governance, provenance, validation, implementation behavior, workflow behavior, agent behavior, or downstream use.

A deprecated document MAY remain available for historical, compatibility, migration, audit, or reference purposes.

Historical availability MUST NOT imply current approval, current authority, current validation, publication permission, export permission, synchronization permission, indexing permission, or downstream-use permission.

Governed Document Storage SHOULD support review workflows.

Draft, review, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending-validation, and needs-repair documents SHOULD remain distinguishable where lifecycle state affects authority, governance, validation, privacy, compatibility, publication, export, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

A draft document MUST NOT be treated as approved merely because it is stored near approved documents, linked from approved documents, visible in a repository, indexed by a search system, synchronized across devices, backed up, exported, or referenced by an agent or workflow.

Governed Document Storage MUST preserve privacy boundaries.

A governed document containing restricted content, restricted source references, restricted provenance, restricted implementation details, restricted agent instructions, restricted workflow instructions, or restricted operational context MUST NOT become less restricted merely because it is stored in a standards area, implementation area, archive area, backup, export package, synchronized repository, index, cache, or migration package.

Governed Document Storage SHOULD support validation.

A validator SHOULD be able to determine whether a governed document satisfies applicable metadata, structure, authority, lifecycle, dependency, supersession, relationship, source-reference, provenance, privacy, compatibility, import, export, migration, backup, synchronization, indexing, and implementation-independence expectations.

Governed Document Storage SHOULD support portability.

A governed document SHOULD remain understandable when moved, renamed, copied, migrated, imported, exported, backed up, restored, synchronized, indexed, cached, archived, or accessed through a different compliant implementation.

Governed Document Storage is successful when governed documents remain identifiable, authoritative within scope, historically traceable, reviewable, privacy-respecting, validation-compatible, migration-compatible, and distinguishable from implementation files, operational notes, drafts, examples, and supporting assets.

## 11. Draft, Review, and Approval Storage

Draft, Review, and Approval Storage defines how unfinished, proposed, reviewed, approved, rejected, corrected, validated, or pending governed entities should be handled within storage architecture.

Draft, Review, and Approval Storage exists to prevent lifecycle confusion.

A storage environment MAY contain entities in different lifecycle states.

A storage environment MAY contain:

- draft Knowledge Records;
- draft governed documents;
- proposed Source References;
- proposed relationships;
- proposed metadata changes;
- agent-generated outputs;
- workflow-generated outputs;
- review packages;
- validation findings;
- correction notes;
- approval records;
- rejection records;
- deprecation records;
- supersession records;
- repair records;
- human review notes;
- migration review notes;
- import review notes;
- export review notes.

Storage location MAY support lifecycle handling.

Storage location MUST NOT define Lifecycle State by itself.

A file stored in a draft area is not necessarily Draft unless its governed lifecycle context supports that interpretation.

A file stored in a review area is not necessarily Review unless its governed lifecycle context supports that interpretation.

A file stored in an approved area is not necessarily Approved unless its governed lifecycle context supports that interpretation.

A file stored in an archive area is not necessarily Archived unless its governed lifecycle context supports that interpretation.

A lifecycle state MUST remain explicit where lifecycle status affects interpretation, authority, privacy, validation, publication, export, synchronization, indexing, backup, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Draft Storage supports entities that are being created, revised, extracted, transformed, summarized, generated, imported, migrated, or prepared.

A Draft entity MAY be incomplete.

A Draft entity MAY contain unresolved metadata, unresolved relationships, unresolved Source References, incomplete provenance, unconfirmed privacy classification, incomplete validation, provisional authority context, unresolved compatibility concerns, or pending review notes.

Draft Storage MUST NOT cause Draft entities to be treated as approved, authoritative, valid, publishable, exportable, synchronizable, indexable, safe for agent use, safe for workflow use, or safe for downstream use merely because they are stored, visible, linked, searchable, backed up, or accessible.

Review Storage supports entities that require evaluation.

A Review entity MAY require human review, governance review, source review, provenance review, relationship review, metadata review, lifecycle review, authority review, privacy review, validation review, compatibility review, import review, export review, migration review, workflow review, or agent-output review.

Review Storage SHOULD preserve enough context for a reviewer to determine:

- what entity requires review;
- what review scope applies;
- what source support exists where applicable;
- what provenance exists where applicable;
- what metadata requires review;
- what relationships require review;
- what lifecycle state applies;
- what authority context applies;
- what privacy boundaries apply;
- what validation findings exist;
- what compatibility concerns exist;
- what action remains required.

Approval Storage supports entities accepted for use within a defined scope.

Approval MUST remain distinguishable from storage location, validation success, workflow completion, agent confidence, implementation visibility, publication location, export packaging, synchronization status, backup status, indexing status, or downstream-use convenience.

An Approved entity MAY still be restricted.

An Approved entity MAY still be low-authority.

An Approved entity MAY later fail validation.

An Approved entity MAY be superseded, deprecated, archived, restricted, quarantined, or repaired through a governed lifecycle transition.

Approval Storage SHOULD preserve approval scope where scope affects interpretation, authority, publication, export, synchronization, indexing, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Rejection Storage supports entities that have been reviewed and not accepted.

A Rejected entity MAY remain historically useful.

A Rejected entity MUST NOT be treated as approved merely because it remains stored, linked, searchable, indexed, synchronized, backed up, exported, imported, migrated, cached, or accessible.

A Rejected entity SHOULD preserve enough context to determine why rejection occurred where that context affects governance, compatibility, source references, provenance, validation, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Draft, Review, and Approval Storage MUST preserve privacy boundaries.

A Draft, Review, Approved, Rejected, Deprecated, Superseded, Archived, Restricted, Quarantined, Pending-Validation, or Needs-Repair entity MUST NOT become less restricted merely because it moves between lifecycle-related storage areas.

Draft, Review, and Approval Storage SHOULD preserve provenance.

Where an entity moves between draft, review, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending-validation, or needs-repair states, storage SHOULD preserve enough provenance to determine what changed, who or what changed it where applicable, when it changed where applicable, what review occurred where applicable, what validation occurred where applicable, and what downstream limits remain.

Draft, Review, and Approval Storage SHOULD support repair.

Repair-related storage MAY contain correction notes, validation errors, validation warnings, missing metadata reports, broken relationship reports, broken Source Reference reports, privacy issues, authority issues, lifecycle issues, compatibility issues, migration issues, import issues, export issues, backup issues, synchronization issues, indexing issues, or implementation issues.

Repair Storage MUST NOT silently alter Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, compatibility, or historical traceability.

Draft, Review, and Approval Storage is successful when lifecycle-related storage supports creation, review, approval, rejection, repair, and historical preservation without allowing storage location to replace explicit governed lifecycle state, authority, privacy, validation, or provenance.

## 12. Archive, Backup, and Restoration Storage

Archive, Backup, and Restoration Storage defines how governed entities should be preserved for historical review, continuity, disaster recovery, audit, migration, compatibility, rollback, restoration, or long-term preservation.

Archive Storage preserves entities that are no longer active by default, preserved for history, retained for compatibility, kept for audit, held for migration, or maintained for reference.

Backup Storage preserves copies of governed entities for restoration, continuity, disaster recovery, redundancy, rollback, or long-term preservation.

Restoration Storage supports returning archived, backed-up, deleted, corrupted, moved, migrated, synchronized, exported, imported, or otherwise displaced entities to usable storage.

Archive, Backup, and Restoration Storage MUST preserve governed meaning where the stored entity requires preservation of:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- validation history;
- compatibility context;
- import context;
- export context;
- migration context;
- synchronization context;
- indexing context;
- restoration context;
- historical traceability.

Archive Storage MUST NOT cause archived entities to be treated as current, approved, authoritative, valid, public, exportable, synchronizable, indexable, safe for agent use, safe for workflow use, safe for implementation use, or safe for downstream use merely because they remain stored, visible, linked, searchable, backed up, exported, imported, migrated, cached, or accessible.

Backup Storage MUST NOT cause backed-up entities to be treated as new Knowledge Objects merely because they exist in a backup location, backup file, repository snapshot, archive package, synchronized copy, external drive, cloud repository, export package, migration package, or restoration area.

A backup copy SHOULD preserve enough context to determine:

- what entity was backed up;
- what Object Identity applies where applicable;
- what backup scope applies;
- when the backup was created where applicable;
- what storage environment was backed up where applicable;
- what privacy boundaries apply;
- what lifecycle state applied at backup time where applicable;
- what authority context applied at backup time where applicable;
- what validation state applied at backup time where applicable;
- whether restoration would require review, validation, migration, redaction, privacy review, or compatibility review.

Restoration MUST NOT silently overwrite, replace, merge, split, redirect, expose, promote, demote, approve, reject, deprecate, supersede, archive, validate, publish, export, synchronize, index, or authorize downstream use of a governed entity unless a governed process, workflow, specification, or human review permits that behavior.

Restoration SHOULD preserve enough context to determine:

- what was restored;
- what source backup, archive, export, import, migration package, synchronized copy, or storage source was used;
- what target environment received the restored entity;
- whether Object Identity was preserved;
- whether metadata was preserved;
- whether relationships were preserved;
- whether Source References were preserved;
- whether provenance was preserved;
- whether Lifecycle State was preserved;
- whether Authority Level was preserved;
- whether Privacy Classification was preserved;
- whether Validation State or validation history was preserved;
- whether compatibility was preserved;
- whether repair remains required;
- whether review remains required.

Archive, Backup, and Restoration Storage MUST preserve privacy boundaries.

Restricted entities MUST remain restricted in archives, backups, restore points, snapshots, synchronization histories, migration packages, export packages, cache-derived backups, index-derived backups, or restoration areas unless a governed privacy review permits a change.

Backup convenience MUST NOT override Privacy Classification.

Archive convenience MUST NOT override Privacy Classification.

Restoration convenience MUST NOT override Privacy Classification.

Archive, Backup, and Restoration Storage SHOULD preserve source distinction.

A restored Source Material file MUST remain distinguishable from a Knowledge Record.

A restored Knowledge Record MUST remain distinguishable from Source Material.

A restored archive, backup, or snapshot MUST NOT be treated as current merely because it has been restored into an active storage environment.

Archive, Backup, and Restoration Storage SHOULD support validation.

A validator SHOULD be able to determine whether an archive, backup, or restoration process preserved identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, compatibility, source distinction, and implementation independence.

Archive, Backup, and Restoration Storage MAY rely on implementation-specific tools.

Implementation-specific archive, backup, or restoration tools MUST NOT define standard meaning by themselves.

A backup tool, archive tool, synchronization tool, repository system, cloud provider, local file system, database export, or implementation-specific restore feature MAY support preservation.

The governed meaning of the restored or preserved entity MUST remain defined by the applicable standards rather than by the tool.

Archive, Backup, and Restoration Storage SHOULD support long-term durability.

Long-term durability MAY include redundant copies, offline copies, repository history, archive packages, migration packages, export packages, periodic validation, restoration tests, integrity checks, documentation, or future governed preservation methods.

SS-0001 does not require a specific backup tool, archive format, restoration tool, checksum method, repository system, storage medium, synchronization tool, encryption method, or schedule.

Those details belong to future backup specifications, archive specifications, restoration specifications, implementation profiles, security specifications, validation specifications, or operational guides.

Archive, Backup, and Restoration Storage is successful when governed entities can be preserved and restored without identity confusion, source confusion, lifecycle confusion, authority confusion, privacy exposure, validation overstatement, provenance loss, relationship loss, compatibility loss, implementation lock-in, or loss of historical traceability.
