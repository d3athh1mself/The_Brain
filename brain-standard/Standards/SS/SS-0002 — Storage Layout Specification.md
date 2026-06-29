# SS-0002 — Storage Layout Specification

Document ID: SS-0002
Title: Storage Layout Specification
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 2 — Storage Standard
Milestone: 2.2 — Storage Layout Specification
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and storage-layout rules are interpreted within SS-0002.

Where conflicts arise between storage layout, folder placement, filenames, vault structure, repository structure, source-material placement, Knowledge Record placement, governed-document placement, draft placement, archive placement, backup placement, import placement, export placement, migration placement, indexes, caches, implementation files, workflow files, agent files, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, or future specifications, the constitutional foundation and higher-authority standards SHALL guide interpretation and resolution.

SS-0002 is subordinate to TB-0000, TB-0001, TB-0002, TB-0003, the Phase 1 Knowledge Standards, and SS-0001.

SS-0002 extends SS-0001 by defining practical storage-layout expectations for compliant storage environments.

If SS-0002 appears to conflict with SS-0001, the conflict SHOULD be resolved by preserving the storage architecture defined in SS-0001 while applying SS-0002 only as the more specific layout document.

If SS-0002 appears to conflict with a constitutional document or Knowledge Standard, the higher-authority document takes precedence unless formally revised through governance.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Storage Standard refers to Layer 2 of The Brain Standard, responsible for defining how knowledge and source material may be stored, organized, referenced, moved, preserved, and retrieved without defining knowledge meaning.
- Storage Layout refers to the practical arrangement of storage areas, folder groups, repositories, vault sections, file locations, working areas, archive areas, implementation-support areas, import areas, export areas, migration areas, indexes, caches, and supporting assets.
- Storage Environment refers to any vault, repository, file system, database export, folder tree, archive, local directory, synchronized workspace, or implementation-specific storage location used to preserve or access governed entities.
- Root Storage Environment refers to the highest practical storage boundary for a compliant implementation, vault, repository, archive, or exported layout.
- Storage Area refers to a defined part of a Storage Layout used for a specific storage purpose.
- Placement Rule refers to a rule that defines where a governed entity, source artifact, working file, implementation file, archive, backup, export, import, migration artifact, index, cache, or supporting asset SHOULD or MUST be stored.
- Source Material Area refers to the storage area where Source Material is stored, staged, referenced, archived, or organized.
- Knowledge Record Area refers to the storage area where Knowledge Records are stored, reviewed, maintained, or made available for governed use.
- Governed Document Area refers to the storage area where standards, specifications, ADRs, RFCs, implementation documents, operational documents, and other governed documents are stored.
- Draft Area refers to a storage area for incomplete, proposed, temporary, or not-yet-approved work.
- Review Area refers to a storage area for material awaiting human, workflow, validation, governance, privacy, source-reference, provenance, or compatibility review.
- Archive Area refers to a storage area used to preserve historical, superseded, deprecated, rejected, inactive, migrated, or no-longer-current material.
- Backup Area refers to a storage area or backup target used for restoration, continuity, preservation, disaster recovery, or long-term retention.
- Import Area refers to a storage area used to hold material entering a compliant environment before classification, validation, review, or placement.
- Export Area refers to a storage area used to hold material produced from a compliant environment for transfer, publication, migration, sharing, review, or downstream use.
- Migration Area refers to a storage area used to support movement between storage systems, schemas, repositories, vaults, implementations, or standard versions.
- Implementation Support Area refers to a storage area used for implementation-specific files, configuration files, scripts, templates, plugins, generated artifacts, or tool-support files.
- Index or Cache Area refers to a storage area used for generated, temporary, derived, searchable, embedded, summarized, indexed, cached, or implementation-supporting data.
- Placement Signal refers to meaning implied or suggested by folder placement, filename, path, tag, index location, archive location, implementation location, or workflow location.
- Layout Conformance refers to whether a Storage Layout satisfies the requirements, boundaries, placement rules, and validation expectations defined by SS-0002 and higher-authority standards.

## 1. Purpose

The purpose of SS-0002 is to define the practical Storage Layout for The Brain Standard.

SS-0001 defines Storage Architecture at the conceptual standard level. SS-0002 extends that architecture by defining how a compliant storage environment SHOULD organize major storage areas so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup systems, synchronization systems, and implementations can locate, preserve, review, and maintain knowledge reliably.

SS-0002 exists to prevent layout confusion.

Layout confusion occurs when humans, agents, workflows, validators, storage systems, or implementations cannot reliably determine:

- where Source Material should be placed;
- where Knowledge Records should be placed;
- where governed documents should be placed;
- where drafts, review files, and working files should be placed;
- where archives, backups, exports, imports, and migration files should be placed;
- where implementation-support files should be placed;
- which storage areas are authoritative and which are supporting, temporary, generated, archival, or implementation-specific;
- whether a file location affects Object Identity, metadata, relationships, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, or governed meaning;
- whether a storage area is safe for agents, workflows, synchronization, indexing, publication, export, backup, or migration.

SS-0002 defines layout behavior for:

- root storage environments;
- top-level storage areas;
- Source Material placement;
- Knowledge Record placement;
- governed-document placement;
- draft and review placement;
- working-file placement;
- archive placement;
- backup placement;
- import placement;
- export placement;
- migration placement;
- implementation-support placement;
- agent-support placement;
- workflow-support placement;
- index and cache placement;
- generated-file placement;
- supporting-asset placement;
- layout validation;
- layout compatibility;
- conformance and success criteria.

SS-0002 does not define exact metadata fields, exact Markdown front matter syntax, exact Knowledge Record schemas, exact object-type schemas, exact validation rule syntax, exact Obsidian configuration, exact Codex setup, exact plugin behavior, exact scripts, exact database schemas, exact cloud-sync tools, exact backup schedules, exact user-interface behavior, or exact agent runtime behavior.

Those concerns belong to future specifications, implementation documents, workflow standards, agent standards, validation specifications, operational guides, reference implementations, and tool-specific profiles.

SS-0002 may define RECOMMENDED folder groups, storage areas, and placement rules.

Those storage areas support organization, retrieval, validation, routing, preservation, and implementation usability.

Those storage areas MUST NOT become the sole source of governed meaning.

A Knowledge Object MUST NOT receive its Object Identity from folder placement alone.

A Knowledge Record MUST NOT receive its Lifecycle State, Authority Level, Privacy Classification, Validation State, relationship meaning, Source Reference meaning, provenance meaning, or governed interpretation from folder placement alone.

SS-0002 is successful when a compliant storage environment is understandable, portable, inspectable, predictable, usable by humans, usable by agents, compatible with validation, compatible with migration, and capable of preserving knowledge without allowing storage layout to define knowledge meaning.

## 2. Relationship to SS-0001 and Prior Standards

SS-0002 is subordinate to and derived from the constitutional foundation, the Phase 1 Knowledge Standards, and SS-0001.

SS-0001 defines the Storage Architecture Standard.

SS-0002 does not replace SS-0001.

SS-0002 applies SS-0001 by defining the practical layout expectations that storage environments SHOULD follow.

In practical terms:

- SS-0001 answers: What is storage responsible for?
- SS-0001 answers: What must storage preserve?
- SS-0001 answers: What must storage not define?
- SS-0002 answers: Where should major categories of stored material be placed?
- SS-0002 answers: How should storage areas be separated?
- SS-0002 answers: What placement rules help humans, agents, workflows, validators, and implementations use storage reliably?
- SS-0002 answers: What layout constraints prevent folders, filenames, vault paths, repositories, archives, indexes, caches, or implementation files from becoming hidden sources of governed meaning?

SS-0002 depends on TB-0000 because The Brain is intended to remain implementation-independent, portable, durable, human-readable, AI-readable, and maintainable over time.

SS-0002 depends on TB-0001 because storage layout must preserve knowledge meaning, stable Object Identity, implementation independence, portability, explicit structure, governed evolution, and practical daily usability.

SS-0002 depends on TB-0002 because Storage is Layer 2 and must preserve Layer 1 meaning without allowing storage organization to define meaning.

SS-0002 depends on TB-0003 because layout rules, revisions, supersessions, compatibility concerns, and future changes must follow the governance model.

SS-0002 depends on KS-0001 because storage layout must preserve the distinction between Knowledge Objects, Knowledge Records, and Source Material.

SS-0002 depends on KS-0002 because folder placement, filenames, vault paths, repository paths, archive locations, import locations, export locations, migration locations, indexes, caches, and implementation-specific identifiers MUST NOT replace stable Object Identity.

SS-0002 depends on KS-0003 because metadata meaning must remain explicit, portable, inspectable, and governed rather than hidden inside storage layout.

SS-0002 depends on KS-0004 because relationships must remain explicit and portable rather than inferred only from folder proximity, filename similarity, path structure, backlinks, graph layout, or implementation-specific linking.

SS-0002 depends on KS-0005 because Source References and provenance must remain traceable even when Source Material, Knowledge Records, archives, backups, imports, exports, or migration artifacts are moved, renamed, reorganized, or stored externally.

SS-0002 depends on KS-0006 because Lifecycle State must remain explicit and distinguishable from storage area, folder placement, review folders, draft folders, archive folders, import folders, export folders, migration folders, or implementation-specific status locations.

SS-0002 depends on KS-0007 because Authority Level must remain explicit, scoped, and governed rather than inferred only from storage location, publication folder, archive folder, review folder, filename, or implementation visibility.

SS-0002 depends on KS-0008 because Privacy Classification must govern access, visibility, synchronization, indexing, export, backup, agent access, workflow access, implementation access, and downstream use regardless of where material is stored.

SS-0002 depends on KS-0009 because layout conformance, placement correctness, missing files, duplicate placement, broken references, unsafe exposure, invalid storage state, import readiness, export readiness, backup readiness, and migration readiness may require validation.

SS-0002 SHALL preserve the following storage boundary:

Storage layout may organize knowledge.

Storage layout may support navigation.

Storage layout may support retrieval.

Storage layout may support workflow routing.

Storage layout may support validation.

Storage layout may support agent operation.

Storage layout may support backup, synchronization, import, export, migration, and implementation behavior.

Storage layout MUST NOT define knowledge meaning by itself.

If a future implementation, workflow, agent, validator, plugin, script, database, vault system, or synchronization tool treats storage layout as the sole source of Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, or governed meaning, that behavior is non-conforming unless explicitly authorized by a higher-authority governed document.

## 3. Layout Scope and Constraints

SS-0002 applies to compliant storage environments used to store, organize, preserve, inspect, validate, synchronize, back up, import, export, migrate, or implement The Brain Standard.

A compliant storage environment MAY include:

- a local file-system vault;
- a repository;
- an Obsidian vault;
- a database export;
- a file tree generated from a database-backed implementation;
- a synchronized folder;
- a source archive;
- an implementation workspace;
- a backup target;
- an import staging area;
- an export package;
- a migration workspace;
- a future storage system that can preserve the requirements of The Brain Standard.

SS-0002 defines storage-layout expectations for major storage areas and placement behavior.

SS-0002 does not require every implementation to use the same exact folder names, visual ordering, operating system, cloud provider, synchronization tool, database structure, application interface, plugin system, or automation runtime.

A compliant implementation MAY adapt exact folder names, path separators, repository conventions, database export structures, or implementation-specific support files when required by its environment.

Such adaptation is compliant only if the implementation preserves the storage-layout meaning, separation rules, placement expectations, portability, validation expectations, privacy boundaries, and higher-authority standards defined by SS-0002.

A Storage Layout SHALL support clear separation between:

- Source Material;
- Knowledge Records;
- governed documents;
- drafts;
- review material;
- working files;
- implementation-support files;
- workflow-support files;
- agent-support files;
- supporting assets;
- archives;
- backups;
- imports;
- exports;
- migrations;
- indexes;
- caches;
- generated files.

A Storage Layout MUST preserve the distinction between current governed material and supporting, temporary, generated, archival, imported, exported, migrated, or implementation-specific material.

A Storage Layout MUST NOT require hidden application state for a human, agent, workflow, validator, storage system, migration process, import process, export process, backup process, synchronization process, or implementation to determine the basic purpose of a storage area.

A Storage Layout SHOULD be inspectable using ordinary file-system access where practical.

A Storage Layout SHOULD be understandable by a human without requiring a specific proprietary application.

A Storage Layout SHOULD be readable by agents and automation without relying on undocumented assumptions.

A Storage Layout SHOULD support local-first use where practical.

A Storage Layout MAY use cloud storage, synchronized storage, hosted databases, external archives, external repositories, or implementation-specific storage systems.

Those systems MUST NOT become required for the meaning of knowledge to remain understandable, portable, validatable, or recoverable.

Folder placement MAY support routing, review, convenience, discovery, filtering, synchronization, backup, import, export, migration, validation, or implementation behavior.

Folder placement MUST NOT be the only source of:

- Object Identity;
- Knowledge Object meaning;
- Knowledge Record interpretation;
- required metadata;
- relationship meaning;
- Source Reference meaning;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- import status;
- export status;
- migration status;
- backup status;
- publication permission;
- agent permission;
- workflow permission;
- downstream-use permission.

A filename MAY support human readability, sorting, recognition, display, retrieval, or implementation usability.

A filename MUST NOT be the only source of stable Object Identity, governed title, object type, Lifecycle State, Authority Level, Privacy Classification, Validation State, source support, relationship meaning, provenance, or governed interpretation.

A path MAY support navigation and placement validation.

A path MUST NOT replace explicit metadata, Source References, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation State, or governed meaning.

A Storage Layout MUST preserve privacy boundaries.

Restricted, sensitive, confidential, private, non-exportable, non-indexable, non-synchronizable, or agent-restricted material MUST NOT become exposed merely because it is easier to organize, search, summarize, back up, synchronize, index, export, migrate, or process.

A Storage Layout MUST preserve source traceability.

Source Material may be stored in the same root storage environment as Knowledge Records, in a separate source archive, in an external repository, or in another governed storage location.

Any compliant approach MUST preserve traceable Source References, provenance, source availability context, and source privacy expectations.

A Storage Layout SHOULD support validation.

A validator SHOULD be able to determine whether material is placed in an appropriate storage area, whether required separations are preserved, whether generated material is distinguishable from governed material, whether drafts are distinguishable from approved records, whether imports and exports are distinguishable from current records, whether archives remain historically interpretable, and whether privacy or source-reference risks exist.

A Storage Layout SHOULD support migration.

A compliant storage environment SHOULD allow material to be moved, renamed, exported, imported, backed up, restored, reorganized, or migrated without semantic loss.

Layout Scope and Constraints are successful when storage organization improves usability without weakening Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, implementation independence, portability, privacy, traceability, or governance.

## 4. Layout Principles

Storage Layout Principles define the rules that govern how storage areas, folder groups, file placement, working areas, generated files, archives, backups, imports, exports, migrations, implementation files, workflow files, and agent-support files should be organized within a compliant storage environment.

A Storage Layout SHALL preserve the architecture principle that knowledge meaning is defined by explicit governed structure, not by storage location alone.

A Storage Layout SHOULD make stored material easy to:

- locate;
- inspect;
- review;
- validate;
- preserve;
- back up;
- restore;
- migrate;
- export;
- import;
- synchronize;
- distinguish by storage purpose;
- process safely through agents and workflows.

A Storage Layout MUST preserve clear separation between storage areas that serve different purposes.

At minimum, a Storage Layout SHOULD distinguish between:

- current governed knowledge;
- Source Material;
- governed standards and specifications;
- drafts;
- review material;
- working material;
- implementation-support material;
- workflow-support material;
- agent-support material;
- generated material;
- indexes and caches;
- supporting assets;
- archives;
- backups;
- imports;
- exports;
- migrations.

Separation MAY be represented through folders, repositories, database partitions, storage buckets, labels, collections, or other implementation-specific storage structures.

The representation method may vary.

The separation meaning MUST remain explicit, inspectable, portable, and compatible with validation.

A Storage Layout SHOULD minimize hidden assumptions.

A future human, agent, workflow, validator, migration process, import process, export process, backup process, synchronization process, or implementation SHOULD be able to determine the intended purpose of a storage area without relying on undocumented user habits, application memory, agent memory, workflow memory, plugin behavior, or private implementation state.

A Storage Layout SHOULD favor durability over convenience where the two conflict.

Convenience structures MAY support navigation, filtering, search, sorting, synchronization, publication, workflow routing, or implementation behavior.

Convenience structures MUST NOT override Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, governance, or compatibility requirements.

A Storage Layout SHOULD avoid unnecessary complexity.

A storage area SHOULD exist only when it materially improves:

- clarity;
- durability;
- portability;
- source traceability;
- privacy handling;
- validation;
- reviewability;
- migration;
- backup and restoration;
- implementation independence;
- agent safety;
- workflow reliability;
- daily usability.

A Storage Layout SHOULD support progressive implementation.

A simple implementation MAY begin with fewer physical folders if it preserves the required distinctions.

A mature implementation MAY separate storage areas more granularly when scale, privacy, validation, workflow, agent, migration, synchronization, backup, publication, or implementation needs justify the added structure.

A Storage Layout MUST NOT collapse Source Material and Knowledge Records into the same governed meaning.

Source Material may be stored near Knowledge Records for usability, but it MUST remain distinguishable from structured Knowledge Records created from, about, or in response to that Source Material.

A Storage Layout MUST NOT collapse governed documents and implementation-support files into the same authority category.

Governed documents may define standards, specifications, decisions, implementation expectations, or operational guidance.

Implementation-support files may help realize the standard in a specific tool or environment.

Implementation-support files MUST NOT become higher-authority documents merely because they are stored near standards or used by automation.

A Storage Layout MUST distinguish current material from historical, deprecated, superseded, rejected, migrated, exported, imported, backed-up, or archived material where that distinction affects interpretation or use.

A Storage Layout MUST preserve privacy boundaries across all storage areas.

Private, confidential, sensitive, restricted, non-exportable, non-indexable, non-synchronizable, or agent-restricted material MUST NOT be exposed through layout convenience, search convenience, graph convenience, sync convenience, backup convenience, publication convenience, export convenience, or agent convenience.

A Storage Layout SHOULD support validation by making placement rules checkable.

A validator SHOULD be able to identify:

- missing required storage areas where required by a profile;
- files placed in the wrong storage area;
- drafts mixed with approved material;
- Source Material confused with Knowledge Records;
- generated files confused with governed files;
- implementation files confused with standards;
- archives confused with current material;
- imports or exports confused with governed records;
- privacy-sensitive material placed in unsafe areas;
- indexes or caches treated as authoritative records;
- broken or ambiguous layout boundaries.

A Storage Layout SHOULD support migration by making storage areas portable.

A compliant layout SHOULD be capable of being copied, exported, transformed, or mapped into another compliant storage environment without semantic loss.

Layout Principles are successful when storage organization improves clarity, usability, validation, preservation, and automation while preserving knowledge meaning, implementation independence, privacy, traceability, governance, and long-term portability.

## 5. Root Storage Environment

The Root Storage Environment is the highest practical storage boundary for a compliant vault, repository, archive, export package, implementation workspace, or storage system.

The Root Storage Environment exists so that humans, agents, workflows, validators, storage systems, backup systems, synchronization systems, import processes, export processes, migration processes, and implementations can determine where a compliant storage layout begins.

A Root Storage Environment MAY be:

- a local folder;
- an Obsidian vault;
- a Git repository;
- a synchronized directory;
- a database export directory;
- an archive package;
- a source-material repository;
- an implementation workspace;
- a migration workspace;
- a generated export package;
- a future storage container capable of preserving The Brain Standard.

A Root Storage Environment SHOULD be identifiable.

A compliant implementation SHOULD provide enough context for a future human, agent, workflow, validator, storage system, backup process, synchronization process, import process, export process, migration process, or implementation to determine:

- what the root represents;
- what standard or profile it follows;
- what storage areas it contains;
- whether it contains governed material;
- whether it contains implementation-support material;
- whether it contains Source Material;
- whether it contains generated material;
- whether it contains archives, backups, imports, exports, or migration material;
- whether privacy restrictions apply;
- whether validation is required before use.

A Root Storage Environment SHOULD include or support a root-level orientation document where practical.

A root-level orientation document MAY identify:

- the storage layout name;
- the applicable standard;
- the implementation profile where applicable;
- the purpose of the storage environment;
- the major storage areas;
- the expected handling rules;
- privacy warnings where applicable;
- validation expectations;
- backup or restoration notes;
- import, export, or migration notes;
- implementation-specific cautions.

A Root Storage Environment MUST NOT define Object Identity merely by root location.

Moving a compliant layout from one root folder, vault, repository, archive, storage device, synchronization target, export package, or implementation workspace to another MUST NOT change the Object Identity of contained Knowledge Objects.

A Root Storage Environment MUST NOT define authority merely by root location.

A file is not authoritative merely because it exists inside the Root Storage Environment.

Authority Level must remain explicit, scoped, governed, and compatible with the applicable standards.

A Root Storage Environment MUST NOT define lifecycle state merely by root location.

A file is not draft, review, approved, deprecated, superseded, rejected, archived, imported, exported, migrated, or backed up solely because it exists in a particular root unless a governed specification or workflow explicitly defines that behavior and preserves the required metadata and provenance.

A Root Storage Environment MUST NOT weaken Privacy Classification.

A root that contains restricted material MUST be handled according to the most restrictive applicable privacy expectations where exposure, indexing, synchronization, export, backup, publication, agent access, workflow access, or implementation access creates risk.

A Root Storage Environment SHOULD support portability.

A compliant Root Storage Environment SHOULD be movable, copyable, exportable, importable, restorable, and migratable without requiring a specific proprietary application to preserve meaning.

A Root Storage Environment SHOULD support ordinary inspection where practical.

A human SHOULD be able to inspect the major storage areas using ordinary file-system tools when the implementation uses a file-based layout.

A Root Storage Environment MAY contain implementation-specific files.

Implementation-specific files SHOULD be placed in an Implementation Support Area or another clearly identified support area unless the implementation requires root-level placement.

When implementation-specific files must exist at the root, they SHOULD remain clearly distinguishable from governed standards, Knowledge Records, Source Material, archives, backups, imports, exports, and migration material.

A Root Storage Environment MAY contain generated files, indexes, caches, or temporary files only when those files remain distinguishable from governed material.

Generated files, indexes, caches, and temporary files MUST NOT be treated as the sole authoritative source of Knowledge Object meaning, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, or governed interpretation.

A Root Storage Environment SHOULD support validation.

A validator SHOULD be able to determine whether the root contains the expected storage areas, whether required separations are preserved, whether privacy-sensitive material is protected, whether implementation files are distinguishable from governed files, and whether generated material is distinguishable from authoritative material.

The Root Storage Environment is successful when it provides a clear, portable, inspectable, and implementation-independent boundary for storage layout without becoming the source of governed knowledge meaning.

## 6. Top-Level Storage Areas

Top-Level Storage Areas are the primary storage divisions within a Root Storage Environment.

Top-Level Storage Areas exist to make stored material understandable, navigable, reviewable, validatable, portable, and maintainable.

A compliant Storage Layout SHOULD define Top-Level Storage Areas for the major classes of material used by The Brain Standard.

At minimum, a mature compliant layout SHOULD support storage areas for:

- governed documents;
- Knowledge Records;
- Source Material;
- drafts;
- review material;
- working material;
- implementation-support material;
- workflow-support material;
- agent-support material;
- supporting assets;
- archives;
- backups;
- imports;
- exports;
- migrations;
- indexes;
- caches;
- generated files.

A simple compliant layout MAY combine some physical storage areas if the combined area preserves the required distinctions through explicit structure, metadata, naming, documentation, validation rules, or implementation profile rules.

A combined storage area MUST NOT create ambiguity between governed material and supporting material.

A combined storage area MUST NOT create ambiguity between Source Material and Knowledge Records.

A combined storage area MUST NOT create ambiguity between current material and archived, imported, exported, migrated, generated, cached, or temporary material.

A combined storage area MUST NOT weaken privacy handling.

A Top-Level Storage Area SHOULD have a clear storage purpose.

A Top-Level Storage Area SHOULD NOT exist merely because a tool, plugin, agent, workflow, or user habit created it.

A Top-Level Storage Area becomes part of a compliant layout only when its purpose, placement expectations, and boundaries are documented or otherwise governed by an applicable standard, specification, implementation profile, workflow, or operational guide.

A Top-Level Storage Area MAY use human-readable folder names.

A Top-Level Storage Area MAY use implementation-specific names when required by a tool or environment.

Human-readable names are RECOMMENDED where practical because they improve inspection, review, maintenance, migration, and agent interpretation.

The following conceptual Top-Level Storage Areas are RECOMMENDED for a file-based reference layout:

- `00_System`
- `01_Governance`
- `02_Knowledge`
- `03_Sources`
- `04_Working`
- `05_Implementation`
- `06_Agents`
- `07_Workflows`
- `08_Assets`
- `09_Archives`
- `10_Exchange`
- `11_Generated`

These names are RECOMMENDED reference labels, not mandatory universal folder names.

A compliant implementation MAY rename, reorder, split, combine, or adapt these storage areas when required by scale, tool behavior, repository conventions, privacy needs, synchronization needs, migration needs, implementation profile, or user environment.

Any adaptation MUST preserve the layout purpose and higher-authority requirements.

`00_System` SHOULD contain root-level orientation, layout documentation, local readme files, storage manifests, validation notes, profile notes, and other system-level storage guidance.

`01_Governance` SHOULD contain governed documents such as constitutional documents, standards, specifications, ADRs, RFCs, implementation documents, operational documents, and governance-support records.

`02_Knowledge` SHOULD contain current Knowledge Records and governed knowledge representations.

`03_Sources` SHOULD contain or reference Source Material, source archives, source staging areas, source manifests, and source-support material.

`04_Working` SHOULD contain drafts, review material, temporary working files, proposed records, incomplete records, repair work, and material not yet ready for governed placement.

`05_Implementation` SHOULD contain implementation-support files, configuration files, templates, scripts, tool profiles, plugin-support files, setup files, and implementation-specific documentation.

`06_Agents` SHOULD contain agent-support files, agent instructions, agent role definitions, agent boundary documents, agent handoff templates, agent logs where governed, and agent-specific operational support material.

`07_Workflows` SHOULD contain workflow-support files, workflow definitions, routing instructions, review procedures, ingestion procedures, approval procedures, maintenance procedures, and workflow-specific operational support material.

`08_Assets` SHOULD contain supporting assets that are not themselves primary Knowledge Records or Source Material, such as diagrams, images, attachments, media, icons, exports used for display, and other support files.

`09_Archives` SHOULD contain historical, deprecated, superseded, rejected, inactive, migrated, preserved, or no-longer-current material that must remain available for traceability, restoration, compatibility, audit, governance, or historical review.

`10_Exchange` SHOULD contain import, export, migration, transfer, publication-preparation, and package-staging material.

`11_Generated` SHOULD contain generated files, indexes, caches, embeddings, summaries, reports, derived outputs, temporary machine outputs, validation outputs, and other non-authoritative generated material.

A Top-Level Storage Area MUST NOT be treated as authoritative merely because of its position, numeric prefix, name, sort order, visibility, sync status, index status, or implementation behavior.

Numeric prefixes MAY support predictable ordering.

Numeric prefixes MUST NOT define authority, lifecycle state, privacy classification, validation state, Object Identity, relationship meaning, source-reference meaning, provenance, publication permission, export permission, agent permission, workflow permission, or downstream-use permission.

Top-Level Storage Areas SHOULD be stable enough to support human memory, agent instructions, workflow routing, validation rules, backup rules, synchronization rules, import/export rules, and migration mappings.

Top-Level Storage Areas MAY evolve through governance when the layout requires improvement.

A layout change SHOULD preserve compatibility or provide migration guidance when existing material depends on the prior layout.

Top-Level Storage Areas are successful when they provide a practical, readable, portable, and validatable structure for storage without allowing the layout itself to become the source of knowledge meaning.

## 7. Source Material Area

The Source Material Area is the storage area used to store, stage, preserve, reference, or organize Source Material.

Source Material includes original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical-artifact records, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.

The Source Material Area exists so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup systems, synchronization systems, and implementations can distinguish original or externally derived material from structured Knowledge Records.

A compliant Storage Layout SHOULD provide a clearly identifiable Source Material Area.

In the RECOMMENDED file-based reference layout, the Source Material Area SHOULD be located under:

```text
03_Sources
```

This reference label is not mandatory.

A compliant implementation MAY use another name, structure, repository, archive, database partition, external storage system, or source-management system if the implementation preserves source traceability, provenance, privacy boundaries, validation expectations, and portability.

The Source Material Area MAY contain:

- original files;
- imported source files;
- scanned documents;
- PDFs;
- images;
- audio files;
- video files;
- transcripts;
- datasets;
- exports from external systems;
- web captures;
- email exports;
- message exports;
- notes used as Source Material;
- source manifests;
- source indexes;
- source availability records;
- source reliability notes;
- source authority notes;
- source privacy notes;
- extraction records;
- transformation records;
- source staging material;
- source archive material.

The Source Material Area SHOULD distinguish between current Source Material, staged Source Material, archived Source Material, restricted Source Material, externally referenced Source Material, and unavailable or missing Source Material where those distinctions affect review, validation, provenance, privacy, import, export, migration, or downstream use.

Source Material stored in the Source Material Area MUST remain distinguishable from Knowledge Records.

A Source Material file MUST NOT become a Knowledge Record merely because it is placed in a compliant storage environment.

A Knowledge Record created from, about, or in response to Source Material MUST remain distinguishable from the Source Material itself.

A Storage Layout MAY place source notes, extracted text, OCR outputs, summaries, or transformed source representations near the Source Material when useful.

Those derived or transformed materials SHOULD remain distinguishable from the original Source Material.

A derived source representation MUST NOT be treated as the original Source Material unless a governed specification or provenance record explicitly defines that role.

The Source Material Area MUST preserve Source References and provenance.

A Knowledge Record, relationship, decision, validation result, workflow output, agent output, import record, export record, migration record, or governed entity that depends on Source Material SHOULD be able to reference that Source Material through a traceable Source Reference, source identifier, external reference, archive reference, citation, manifest entry, or other governed reference mechanism.

A Source Material file MUST NOT rely only on filename or folder location for source identity where source identity affects meaning, provenance, validation, authority, privacy, import, export, migration, or downstream use.

The Source Material Area SHOULD support source availability tracking.

A source may be:

- available;
- unavailable;
- externally hosted;
- archived;
- moved;
- missing;
- restricted;
- partially available;
- corrupted;
- superseded;
- unverifiable;
- governed by another future source-availability condition.

This list is descriptive and does not define a complete controlled vocabulary.

A future specification MAY define exact source-availability values, source manifests, source-reference formats, source identifiers, archive references, citation formats, validation rules, and migration mappings.

The Source Material Area MUST preserve privacy boundaries.

Restricted, private, confidential, sensitive, non-exportable, non-indexable, non-synchronizable, or agent-restricted Source Material MUST NOT be exposed merely because it is stored in a source folder, indexed for search, used for extraction, included in a backup, synchronized across systems, exported for migration, summarized by an agent, or processed by a workflow.

A Storage Layout SHOULD support source-level privacy separation where practical.

A compliant implementation MAY separate Source Material by privacy classification, source type, project, origin, import batch, archive status, review status, or implementation profile.

Such separation MAY support handling and validation.

Such separation MUST NOT replace explicit Privacy Classification, Source References, provenance, Lifecycle State, Authority Level, Validation State, or governed metadata where those are required.

The Source Material Area SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source Material is distinguishable from Knowledge Records;
- source files are placed in an appropriate source area;
- source manifests exist where required by a profile;
- Source References can resolve or be reviewed where required;
- source privacy expectations are preserved;
- source availability issues are identifiable;
- derived source representations are distinguishable from originals;
- source archives are distinguishable from active source material;
- imported sources are distinguishable from reviewed sources;
- missing or moved sources are not silently treated as available.

The Source Material Area SHOULD support migration.

Source Material SHOULD be movable, exportable, importable, archived, restored, or migrated without breaking Source References, provenance, source availability context, source privacy expectations, or Knowledge Record interpretation.

The Source Material Area is successful when original and source-derived material remains traceable, reviewable, privacy-respecting, portable, validatable, and distinguishable from governed Knowledge Records.

## 8. Knowledge Record Area

The Knowledge Record Area is the storage area used to store current Knowledge Records and governed knowledge representations.

Knowledge Records are structured representations of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, workflow activity, import activity, migration activity, or governed review.

The Knowledge Record Area exists so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup systems, synchronization systems, and implementations can locate and preserve governed knowledge without confusing it with Source Material, drafts, implementation files, generated files, indexes, caches, archives, imports, exports, or migration artifacts.

A compliant Storage Layout SHOULD provide a clearly identifiable Knowledge Record Area.

In the RECOMMENDED file-based reference layout, the Knowledge Record Area SHOULD be located under:

```text
02_Knowledge
```

This reference label is not mandatory.

A compliant implementation MAY use another name, structure, repository, database partition, object store, graph store, or implementation-specific storage system if the implementation preserves Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, reviewability, and portability.

The Knowledge Record Area MAY contain:

- current Knowledge Records;
- approved Knowledge Records;
- reviewed Knowledge Records;
- active Knowledge Object representations;
- governed record files;
- object-type groupings;
- relationship-support records;
- metadata-support records;
- provenance-support records;
- validation-support records;
- knowledge indexes that are explicitly governed as records;
- human-authored knowledge;
- reviewed agent-generated knowledge;
- reviewed workflow-generated knowledge;
- imported knowledge after review;
- migrated knowledge after validation.

The Knowledge Record Area SHOULD NOT contain unreviewed drafts, temporary working notes, raw Source Material, generated caches, embeddings, tool indexes, implementation configuration files, backup copies, export packages, import staging files, or migration workspaces unless a governed implementation profile explicitly permits the placement and preserves the required distinctions.

A Knowledge Record stored in the Knowledge Record Area MUST preserve stable Object Identity.

A Knowledge Record MUST NOT receive its Object Identity merely from its folder, filename, sort order, path, backlink location, database row, graph position, search result, or implementation-specific identifier.

A Knowledge Record stored in the Knowledge Record Area MUST preserve explicit metadata where required by the applicable standard or specification.

Folder placement MAY support object grouping, retrieval, navigation, workflow routing, or validation.

Folder placement MUST NOT replace required metadata.

The Knowledge Record Area SHOULD preserve relationship meaning.

Relationships between Knowledge Records, Knowledge Objects, Source Material, governed documents, decisions, workflows, agents, implementations, and other governed entities MUST NOT rely only on folder proximity, filename similarity, tag coincidence, graph layout, search ranking, backlink behavior, or implementation-specific linking when relationship meaning affects interpretation, provenance, lifecycle state, authority, privacy, validation, migration, import, export, or downstream use.

The Knowledge Record Area SHOULD preserve Source References and provenance.

A Knowledge Record derived from or supported by Source Material SHOULD include or support traceable Source References and provenance sufficient for future review.

The Knowledge Record Area SHOULD preserve Lifecycle State.

A record being located in the Knowledge Record Area MAY indicate that it is part of the governed knowledge environment.

That placement MUST NOT by itself mean the record is approved, authoritative, valid, public, exportable, publishable, safe for agent access, or safe for downstream use.

Lifecycle State MUST remain explicit where lifecycle status affects interpretation or handling.

The Knowledge Record Area SHOULD preserve Authority Level.

A Knowledge Record MUST NOT be treated as authoritative merely because it is stored in the Knowledge Record Area.

Authority Level MUST remain explicit, scoped, reviewable, provenance-aware, and compatible with the applicable standards.

The Knowledge Record Area MUST preserve Privacy Classification.

A Knowledge Record stored in the Knowledge Record Area may still be private, confidential, sensitive, restricted, non-exportable, non-indexable, non-synchronizable, or agent-restricted.

Placement in the Knowledge Record Area MUST NOT weaken privacy handling.

The Knowledge Record Area SHOULD preserve Validation State.

A Knowledge Record stored in the Knowledge Record Area may still require validation, repair, review, privacy review, source-reference review, provenance review, relationship review, authority review, migration review, import review, export review, or compatibility review.

Placement in the Knowledge Record Area MUST NOT be treated as validation success unless a governed workflow or specification explicitly defines that behavior.

The Knowledge Record Area SHOULD support internal organization.

Knowledge Records MAY be organized by object type, domain, project, topic, relationship group, authority scope, privacy scope, lifecycle state, implementation profile, or another governed grouping method.

Any grouping method MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and portability.

A grouping method SHOULD NOT create excessive folder depth or hidden conventions that make knowledge harder to inspect, validate, migrate, or maintain.

The Knowledge Record Area SHOULD support validation.

A validator SHOULD be able to determine whether:

- Knowledge Records are distinguishable from Source Material;
- records preserve required identity and metadata;
- relationships remain explicit where required;
- Source References and provenance are preserved where required;
- lifecycle, authority, privacy, and validation expectations remain explicit;
- unreviewed drafts are not silently mixed with current governed records;
- generated files are not treated as governed records;
- archived, imported, exported, migrated, or backup copies are distinguishable from current records;
- privacy-sensitive records are not exposed through placement, indexing, synchronization, export, backup, or agent access.

The Knowledge Record Area SHOULD support migration.

Knowledge Records SHOULD be movable, exportable, importable, backed up, restored, reorganized, or migrated without losing Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, or governed meaning.

The Knowledge Record Area is successful when governed knowledge remains explicit, portable, traceable, reviewable, privacy-respecting, validatable, and distinguishable from Source Material and supporting storage artifacts.

## 9. Governed Document Area

The Governed Document Area is the storage area used to store documents that define, govern, explain, propose, record, implement, or operationalize The Brain Standard.

Governed documents may include constitutional documents, standards, specifications, ADRs, RFCs, implementation documents, operational documents, guides, procedures, checklists, decision records, compatibility notes, migration notes, validation profiles, and other documents governed by the applicable authority model.

The Governed Document Area exists so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup systems, synchronization systems, and implementations can locate the documents that define or support the standard.

A compliant Storage Layout SHOULD provide a clearly identifiable Governed Document Area.

In the RECOMMENDED file-based reference layout, the Governed Document Area SHOULD be located under:

```text
01_Governance
```

This reference label is not mandatory.

A compliant implementation MAY use another name, structure, repository, documentation site, database partition, version-controlled location, or implementation-specific storage system if the implementation preserves document identity, document authority, lifecycle state, provenance, reviewability, compatibility, and portability.

The Governed Document Area MAY contain:

- TB-series constitutional documents;
- KS-series Knowledge Standards;
- SS-series Storage Standards;
- AG-series Agent Standards;
- WF-series Workflow Standards;
- SC-series specifications;
- ADR-series Architecture Decision Records;
- RFC-series proposals;
- IM-series implementation documents;
- SOPs;
- operational guides;
- validation profiles;
- compatibility notes;
- migration notes;
- release notes;
- governance indexes;
- document manifests;
- standard-support documents.

The Governed Document Area SHOULD distinguish between document families where practical.

A compliant layout MAY organize governed documents by prefix, authority level, phase, milestone, lifecycle state, publication status, review status, implementation profile, or another governed grouping method.

Any grouping method MUST preserve the document authority hierarchy defined by governance.

A document MUST NOT become constitutional, standard-level, specification-level, approved, superseded, deprecated, rejected, authoritative, current, valid, public, exportable, publishable, or implementation-binding merely because of folder placement.

Document authority MUST remain explicit and governed.

Document lifecycle state MUST remain explicit where lifecycle status affects interpretation or use.

A governed document stored in the Governed Document Area MUST preserve its document identity.

Document identity MAY include a document ID, title, version, authority, phase, milestone, dependencies, supersession fields, related documents, or other governed metadata.

A governed document MUST NOT rely only on filename, folder path, storage location, sort order, index position, backlink behavior, publication location, or implementation visibility for document identity where document identity affects governance, compatibility, migration, review, validation, or downstream use.

The Governed Document Area SHOULD preserve dependency clarity.

A governed document SHOULD identify the higher-authority documents, standards, specifications, decisions, implementation profiles, workflows, or operational documents it depends on where those dependencies affect interpretation or use.

A Storage Layout MAY support dependency navigation through folders, indexes, manifests, relationship records, metadata, tables, graphs, or implementation-specific views.

Those navigation aids MUST NOT replace explicit dependency metadata where dependency meaning affects governance, validation, compatibility, or interpretation.

The Governed Document Area SHOULD preserve supersession and historical traceability.

Superseded, deprecated, rejected, archived, or historical governed documents MAY remain stored in or near the Governed Document Area when useful for governance review, compatibility review, migration, audit, restoration, or historical interpretation.

Historical governed documents SHOULD remain distinguishable from current approved documents.

A superseded document MUST NOT be treated as current merely because it remains visible, searchable, linked, indexed, synchronized, exported, backed up, or referenced.

The Governed Document Area MUST preserve privacy boundaries.

Some governed documents, drafts, RFCs, implementation notes, operational procedures, agent instructions, validation reports, or migration plans may contain private, restricted, sensitive, confidential, non-exportable, non-indexable, non-synchronizable, or agent-restricted information.

Placement in the Governed Document Area MUST NOT weaken Privacy Classification.

The Governed Document Area SHOULD distinguish governed documents from implementation-support files.

A script, template, plugin configuration, generated index, validator output, cache, automation file, or implementation setting MUST NOT become a governed document merely because it is stored near governed documents.

Implementation-support material SHOULD be placed in the Implementation Support Area unless it is intentionally governed as an implementation document, operational document, specification, or standard-support document.

The Governed Document Area SHOULD support validation.

A validator SHOULD be able to determine whether:

- governed documents have required document metadata;
- document IDs are present where required;
- authority levels are explicit;
- lifecycle states are explicit where required;
- dependencies are present where required;
- supersession fields are present where required;
- drafts are distinguishable from approved documents;
- superseded or deprecated documents are distinguishable from current documents;
- implementation-support files are not confused with governed documents;
- privacy-sensitive governed documents are not exposed through indexing, synchronization, export, publication, backup, or agent access.

The Governed Document Area SHOULD support migration.

Governed documents SHOULD be movable, exportable, importable, restorable, and migratable without losing document identity, authority, lifecycle state, dependencies, supersession history, provenance, privacy classification, validation state, or governance meaning.

The Governed Document Area is successful when the standard remains findable, reviewable, governable, portable, historically traceable, privacy-respecting, and distinguishable from implementation-support material.

## 10. Draft, Review, and Working Areas

Draft, Review, and Working Areas are storage areas used for incomplete, proposed, temporary, pending, repair, review, or in-progress material.

These areas exist so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup systems, synchronization systems, and implementations can distinguish material that is not yet ready for current governed placement.

A compliant Storage Layout SHOULD provide clearly identifiable areas for draft, review, and working material.

In the RECOMMENDED file-based reference layout, Draft, Review, and Working Areas SHOULD be located under:

```text
04_Working
```

This reference label is not mandatory.

A compliant implementation MAY use another name, structure, workspace, repository, queue, database partition, workflow system, or implementation-specific storage system if the implementation preserves lifecycle clarity, reviewability, provenance, privacy boundaries, validation expectations, and portability.

Draft, Review, and Working Areas MAY contain:

- draft Knowledge Records;
- proposed Knowledge Records;
- incomplete Knowledge Records;
- records awaiting review;
- records awaiting validation;
- records awaiting privacy review;
- records awaiting source-reference review;
- records awaiting provenance review;
- records awaiting relationship review;
- records awaiting authority review;
- records needing repair;
- temporary working notes;
- proposed governed documents;
- RFC drafts;
- draft implementation notes;
- draft workflow outputs;
- draft agent outputs;
- review packets;
- correction queues;
- staging material not yet ready for current placement.

Draft, Review, and Working Areas MUST remain distinguishable from current Knowledge Records, approved governed documents, Source Material, implementation-support files, generated files, archives, backups, imports, exports, and migration artifacts.

A file stored in a Draft, Review, or Working Area MUST NOT receive its Lifecycle State solely from placement.

Placement MAY indicate that the file is being worked on, reviewed, staged, repaired, or prepared.

Placement MUST NOT replace explicit Lifecycle State where lifecycle status affects interpretation, authority, privacy, validation, publication, export, migration, workflow behavior, agent behavior, or downstream use.

A file stored in a Draft, Review, or Working Area MUST NOT be treated as approved merely because it exists.

Draft material may be useful, but existence does not imply approval.

Review material may be ready for evaluation, but review placement does not imply approval.

Working material may support creation or maintenance, but working placement does not imply validity, authority, publication readiness, export readiness, or downstream-use permission.

Draft, Review, and Working Areas SHOULD preserve provenance.

Where draft, review, or working material is created by a human, agent, workflow, import process, migration process, validation process, or implementation, the relevant provenance SHOULD be preserved when it affects interpretation, review, authority, privacy, validation, source traceability, compatibility, publication, export, migration, or downstream use.

Draft, Review, and Working Areas SHOULD preserve source traceability.

Draft or review material derived from Source Material SHOULD preserve Source References or source context sufficient for later review.

A draft or review file MUST NOT silently detach source-derived knowledge from its Source Material where source support affects meaning, provenance, authority, privacy, validation, migration, import, export, or downstream use.

Draft, Review, and Working Areas MUST preserve privacy boundaries.

Drafts, review files, repair files, temporary notes, agent outputs, workflow outputs, validation reports, and working material may contain private, confidential, sensitive, restricted, non-exportable, non-indexable, non-synchronizable, or agent-restricted information.

Placement in a working area MUST NOT weaken Privacy Classification.

A Storage Layout SHOULD allow working material to be separated by review need where practical.

A compliant implementation MAY separate working material into subareas for:

- drafts;
- review;
- pending validation;
- pending privacy review;
- pending source review;
- pending relationship review;
- pending authority review;
- needs repair;
- temporary workspace;
- agent proposals;
- workflow outputs;
- rejected working material;
- future governed review categories.

These subareas MAY support routing, validation, review, and usability.

These subareas MUST NOT replace explicit lifecycle, authority, privacy, validation, provenance, relationship, or source-reference metadata where such metadata is required.

Draft, Review, and Working Areas SHOULD support promotion into current governed placement.

Promotion means moving, copying, transforming, approving, validating, or otherwise advancing material from a draft, review, or working area into an appropriate current storage area.

Promotion SHOULD preserve:

- Object Identity where applicable;
- required metadata;
- Source References;
- provenance;
- relationships;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- review history;
- compatibility context.

Promotion MUST NOT silently convert unreviewed material into approved material.

Promotion MUST NOT silently remove privacy restrictions.

Promotion MUST NOT silently discard source support, provenance, validation warnings, relationship concerns, authority limits, or compatibility concerns.

Draft, Review, and Working Areas SHOULD support rejection, repair, archival, or deletion handling.

Rejected or abandoned working material MAY be archived, deleted, quarantined, repaired, superseded, or preserved for historical review according to the applicable lifecycle, privacy, validation, governance, and operational requirements.

A rejected draft MUST NOT be confused with an approved record merely because it remains searchable, linked, backed up, indexed, synchronized, or visible.

Draft, Review, and Working Areas SHOULD support validation.

A validator SHOULD be able to determine whether:

- working material is distinguishable from current governed material;
- drafts are not silently treated as approved;
- review material has appropriate review context where required;
- validation-pending material remains distinguishable from validation-passed material;
- repair material remains distinguishable from valid current material;
- agent-generated proposals remain reviewable;
- workflow-generated outputs remain reviewable;
- source-derived drafts preserve Source References where required;
- privacy-sensitive working material is not exposed through indexing, synchronization, export, publication, backup, or agent access.

Draft, Review, and Working Areas SHOULD support migration.

Working material SHOULD be movable, exportable, importable, restorable, or migratable without losing review context, provenance, source traceability, privacy classification, validation state, lifecycle state, authority limits, or compatibility information.

Draft, Review, and Working Areas are successful when incomplete, proposed, temporary, review, repair, and working material remains clearly distinguishable from current governed material while remaining traceable, reviewable, privacy-respecting, validatable, and portable.

## 11. Implementation, Agent, and Workflow Support Areas

Implementation, Agent, and Workflow Support Areas are storage areas used to store files that support practical operation, automation, tool configuration, agent behavior, and workflow execution.

These areas exist so that implementation-support material, agent-support material, and workflow-support material remain distinguishable from Knowledge Records, Source Material, governed documents, drafts, archives, backups, imports, exports, migrations, indexes, caches, and generated files.

A compliant Storage Layout SHOULD provide clearly identifiable support areas for implementation, agent, and workflow material.

In the RECOMMENDED file-based reference layout, these support areas SHOULD be located under:

```text
05_Implementation
06_Agents
07_Workflows
```

These reference labels are not mandatory.

A compliant implementation MAY use another name, structure, repository, configuration directory, workflow system, agent directory, database partition, or implementation-specific storage system if the implementation preserves authority boundaries, reviewability, privacy boundaries, validation expectations, portability, and higher-authority standards.

The Implementation Support Area MAY contain:

- implementation profiles;
- setup notes;
- configuration files;
- templates;
- scripts;
- tool-support files;
- plugin-support files;
- schema-support files;
- validator-support files;
- local environment notes;
- reference implementation notes;
- implementation-specific documentation;
- implementation compatibility notes;
- implementation migration notes.

The Agent Support Area MAY contain:

- agent role definitions;
- agent boundary documents;
- agent instruction files;
- agent permission notes;
- agent handoff templates;
- agent review expectations;
- agent traceability notes;
- agent input/output expectations;
- agent logs where governed;
- agent-specific operational support material;
- future agent framework support files.

The Workflow Support Area MAY contain:

- workflow definitions;
- workflow procedures;
- routing instructions;
- ingestion procedures;
- review procedures;
- approval procedures;
- rejection procedures;
- maintenance procedures;
- publication procedures;
- import procedures;
- export procedures;
- migration procedures;
- validation procedures;
- workflow logs where governed;
- workflow-specific operational support material.

Implementation, Agent, and Workflow Support Areas MUST remain distinguishable from governed standards and specifications.

A support file MUST NOT become a standard, specification, ADR, RFC, implementation document, operational document, approved procedure, or governed decision merely because it is stored in a support area or used by an implementation, agent, workflow, script, plugin, or automation.

If a support file is intended to govern behavior, its document type, authority level, lifecycle state, review status, dependencies, and governance status SHOULD be explicit according to the applicable standards.

Implementation-support files MUST NOT redefine the standard.

An implementation may realize The Brain Standard in a specific tool, vault, database, repository, interface, or automation environment.

An implementation MUST NOT alter Object Identity, metadata meaning, relationship meaning, Source Reference behavior, provenance behavior, Lifecycle State, Authority Level, Privacy Classification, Validation, or governance meaning merely through implementation configuration.

Agent-support files MUST NOT make agents unreviewable authorities.

Agent instructions, prompts, logs, templates, routing files, or tool configurations MAY help agents read, classify, summarize, validate, propose, transform, or route material.

Agent-support files MUST NOT authorize agents to silently approve, publish, export, declassify, overwrite, delete, supersede, or reinterpret governed material where human review, governance, privacy, authority, validation, or compatibility review is required.

Workflow-support files MUST NOT replace governed lifecycle, authority, privacy, validation, source-reference, provenance, relationship, or identity rules.

A workflow may route, review, validate, approve, reject, repair, publish, import, export, migrate, or preserve material only within the boundaries defined by higher-authority standards and applicable workflow documents.

Workflow completion MUST NOT be treated as approval, authority, privacy permission, validation success, publication permission, export permission, or downstream-use permission unless a governed workflow specification explicitly defines that behavior.

Implementation, Agent, and Workflow Support Areas MUST preserve privacy boundaries.

Support files may contain private configuration, restricted instructions, sensitive operational details, agent boundaries, workflow permissions, validation reports, environment notes, source paths, credentials references, local paths, or other restricted information.

Placement in a support area MUST NOT weaken Privacy Classification.

Restricted support material SHOULD be protected from unsafe indexing, synchronization, export, publication, backup exposure, agent access, workflow access, or implementation visibility.

Implementation, Agent, and Workflow Support Areas SHOULD preserve provenance where support files affect governed behavior.

Where a support file materially affects validation, workflow routing, agent behavior, publication, export, migration, privacy handling, or implementation behavior, the relevant provenance, review status, version context, or compatibility context SHOULD be preserved.

Implementation, Agent, and Workflow Support Areas SHOULD support versioning and compatibility where practical.

A support file change MAY affect automation behavior, validator behavior, agent behavior, workflow behavior, migration behavior, import behavior, export behavior, publication behavior, or implementation compatibility.

A material support-file change SHOULD be reviewable when it affects governed meaning, privacy, validation, authority, workflow outcomes, agent permissions, migration, export, publication, or downstream use.

Implementation, Agent, and Workflow Support Areas SHOULD support validation.

A validator SHOULD be able to determine whether:

- implementation-support files are distinguishable from governed documents;
- agent-support files are distinguishable from agent outputs;
- workflow-support files are distinguishable from workflow outputs;
- support files do not silently redefine higher-authority standards;
- agent permissions remain reviewable;
- workflow procedures remain within governed boundaries;
- implementation configuration does not become the source of knowledge meaning;
- privacy-sensitive support files are not exposed through indexing, synchronization, export, publication, backup, or inappropriate agent access;
- generated support artifacts are distinguishable from authored support files.

Implementation, Agent, and Workflow Support Areas SHOULD support migration.

Support files SHOULD be movable, exportable, importable, restorable, or migratable without losing implementation context, agent context, workflow context, version context, privacy classification, validation state, review history, or compatibility information where those affect operation or governance.

Implementation, Agent, and Workflow Support Areas are successful when support material helps tools, agents, and workflows operate reliably without becoming hidden architecture, unreviewable authority, or the source of governed knowledge meaning.

## 12. Assets, Indexes, Caches, and Generated Files

Assets, Indexes, Caches, and Generated Files are storage-support materials that assist presentation, discovery, automation, validation, implementation behavior, reporting, or usability without automatically becoming governed Knowledge Records or governed documents.

These storage-support materials exist so that humans, agents, workflows, validators, storage systems, synchronization systems, backup systems, import processes, export processes, migration processes, and implementations can distinguish authored governed material from supporting, derived, generated, temporary, indexed, cached, or presentation-oriented material.

A compliant Storage Layout SHOULD provide clearly identifiable areas for supporting assets and generated material.

In the RECOMMENDED file-based reference layout, supporting assets SHOULD be located under:

```text
08_Assets
```

In the RECOMMENDED file-based reference layout, indexes, caches, and generated files SHOULD be located under:

```text
11_Generated
```

These reference labels are not mandatory.

A compliant implementation MAY use another name, structure, repository, cache directory, database partition, generated-output directory, media library, asset store, index store, embedding store, or implementation-specific storage system if the implementation preserves authority boundaries, privacy boundaries, validation expectations, portability, and higher-authority standards.

The Assets Area MAY contain:

- diagrams;
- images;
- media files;
- icons;
- attachments;
- display-support files;
- document-support images;
- visual aids;
- exported graphics used for presentation;
- non-source supporting media;
- supporting files referenced by governed documents;
- supporting files referenced by Knowledge Records;
- implementation-display assets;
- future support assets.

The Generated Area MAY contain:

- generated indexes;
- caches;
- embeddings;
- search indexes;
- vector indexes;
- summaries;
- reports;
- validation outputs;
- lint outputs;
- transformed outputs;
- derived files;
- temporary machine outputs;
- automation outputs;
- generated relationship maps;
- generated source maps;
- generated metadata reports;
- generated migration reports;
- generated export reports;
- generated import reports;
- future generated artifacts.

Assets MUST remain distinguishable from Source Material unless an asset is explicitly governed as Source Material.

An image, diagram, attachment, media file, or display-support file may be a supporting asset.

The same kind of file may also be Source Material in another context.

The role of the file MUST be explicit where that role affects Source References, provenance, authority, privacy, validation, citation, import, export, migration, or downstream use.

Assets MUST remain distinguishable from Knowledge Records unless an asset is explicitly governed as a Knowledge Record or representation of a Knowledge Object.

An asset may support a Knowledge Record.

An asset may be referenced by a Knowledge Record.

An asset may illustrate or display governed knowledge.

An asset MUST NOT become governed knowledge merely because it is linked, embedded, displayed, indexed, synchronized, backed up, exported, or used by an implementation.

Indexes and caches MUST remain distinguishable from governed records.

An index, cache, embedding store, search database, vector database, generated map, or generated report MAY support discovery, retrieval, validation, navigation, automation, or implementation behavior.

An index, cache, embedding, search result, generated report, or derived output MUST NOT be treated as the sole authoritative source of Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, or governed meaning.

Generated summaries MUST remain distinguishable from source content and governed knowledge.

A generated summary MAY support review, navigation, search, workflow routing, or agent operation.

A generated summary MUST NOT replace Source Material, Source References, provenance, or a reviewed Knowledge Record unless a governed workflow or specification explicitly defines the transformation, review, validation, provenance, authority, and lifecycle requirements.

Generated relationship maps MUST remain distinguishable from explicit governed relationships.

A generated map, graph, backlink list, recommendation, cluster, or similarity output MAY suggest potential relationships.

Such output MUST NOT become an approved relationship merely because a tool, agent, workflow, index, graph system, or model generated it.

Generated validation outputs MUST remain distinguishable from Validation State.

A validation report MAY support Validation State.

A validation output MUST NOT automatically become approval, rejection, authority, privacy permission, publication permission, export permission, or downstream-use permission unless a governed workflow or specification explicitly defines that behavior.

Assets, Indexes, Caches, and Generated Files MUST preserve privacy boundaries.

Generated files may expose restricted information through summaries, excerpts, embeddings, indexes, logs, reports, previews, thumbnails, relationship maps, source maps, validation results, or search metadata.

A generated file, index, cache, embedding, report, or asset MUST NOT expose private, confidential, sensitive, restricted, non-exportable, non-indexable, non-synchronizable, or agent-restricted material merely because generation, indexing, synchronization, backup, export, migration, search, or automation is convenient.

Indexes, caches, and generated files SHOULD be regenerable where practical.

A Storage Layout SHOULD distinguish between material that must be preserved as a governed record and material that may be safely regenerated from governed records, Source Material, metadata, relationships, validation rules, workflow outputs, or implementation processes.

A generated artifact that affects governance, validation, migration, audit, publication, export, import, compatibility, privacy, authority, or historical interpretation MAY require preservation, provenance, review, or archival handling.

Generated files SHOULD preserve generation context where needed.

Generation context MAY include:

- generation date;
- generating tool;
- agent or workflow involved;
- input files;
- source records;
- rule set;
- validation scope;
- implementation profile;
- migration context;
- export context;
- privacy constraints;
- limitations;
- review status.

This list is descriptive and does not define a complete required metadata set.

A future specification MAY define exact generated-file metadata, cache rules, index rules, embedding rules, report formats, validation-output formats, generation provenance, regeneration rules, retention rules, and deletion rules.

Assets, Indexes, Caches, and Generated Files SHOULD support validation.

A validator SHOULD be able to determine whether:

- assets are distinguishable from Source Material and Knowledge Records;
- generated files are distinguishable from authored governed files;
- indexes and caches are not treated as authoritative records;
- generated summaries are not treated as reviewed Knowledge Records;
- generated relationships are not treated as approved relationships;
- validation outputs are not treated as approval unless governed;
- privacy-sensitive data is not exposed through assets, indexes, caches, embeddings, summaries, reports, previews, thumbnails, or generated maps;
- generated files include generation context where required;
- stale or invalid generated files are distinguishable from current generated files;
- regenerable files are distinguishable from preserved governed outputs.

Assets, Indexes, Caches, and Generated Files SHOULD support migration.

Supporting assets SHOULD remain linked, referenced, portable, restorable, and migratable where they support governed records or governed documents.

Generated files, indexes, caches, embeddings, and reports MAY be excluded, regenerated, archived, or migrated according to the applicable privacy, validation, provenance, compatibility, import, export, backup, synchronization, and implementation requirements.

Assets, Indexes, Caches, and Generated Files are successful when supporting and generated material improves usability, presentation, discovery, automation, validation, and implementation behavior without becoming hidden authority, exposing restricted knowledge, or replacing governed knowledge meaning.

## 13. Archive and Backup Areas

Archive and Backup Areas are storage areas used to preserve historical, inactive, superseded, deprecated, rejected, migrated, no-longer-current, restorable, or continuity-supporting material.

These areas exist so that humans, agents, workflows, validators, storage systems, backup systems, synchronization systems, import processes, export processes, migration processes, and implementations can distinguish preserved historical material and restoration material from current governed material.

A compliant Storage Layout SHOULD provide clearly identifiable archive and backup handling.

In the RECOMMENDED file-based reference layout, archived material SHOULD be located under:

```text
09_Archives
```

This reference label is not mandatory.

A compliant implementation MAY use another name, structure, repository, archive package, backup target, external storage location, version-control mechanism, cold-storage system, database snapshot, or implementation-specific preservation system if the implementation preserves traceability, privacy boundaries, restoration context, validation expectations, compatibility, and portability.

The Archive Area MAY contain:

- superseded governed documents;
- deprecated governed documents;
- rejected governed documents preserved for history;
- archived Knowledge Records;
- historical Knowledge Records;
- archived Source Material;
- historical Source References;
- historical provenance records;
- historical validation results;
- migration records;
- import records;
- export records;
- retired implementation files;
- retired workflow files;
- retired agent files;
- preserved generated reports;
- audit-support material;
- compatibility-support material;
- restoration-support material.

The Backup Area MAY contain or reference:

- local backups;
- external backups;
- repository backups;
- vault snapshots;
- database snapshots;
- archive packages;
- restoration packages;
- disaster-recovery copies;
- encrypted backups;
- periodic exports used for recovery;
- version-control history;
- future backup mechanisms.

A Storage Layout MAY store backups inside the Root Storage Environment, outside the Root Storage Environment, in a separate repository, in offline storage, in encrypted storage, in cloud storage, in version control, or in another governed backup target.

The location of a backup MAY vary by implementation.

Backup handling MUST preserve privacy boundaries, restoration context, and compatibility expectations.

Archive placement MUST NOT define historical status by itself where historical status affects interpretation or use.

A file stored in an Archive Area MAY be historical, superseded, deprecated, rejected, inactive, migrated, or preserved for audit.

The applicable Lifecycle State, Authority Level, Validation State, supersession context, provenance, and compatibility context SHOULD remain explicit where those affect interpretation, restoration, migration, import, export, publication, agent behavior, workflow behavior, or downstream use.

Backup placement MUST NOT define current authority by itself.

A backup copy MUST NOT be treated as the current authoritative record merely because it is complete, recent, indexed, synchronized, restored, searchable, or easier to access.

A restored backup SHOULD be reviewed where restoration may affect Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, compatibility, import, export, migration, or downstream use.

Archive and Backup Areas MUST preserve Object Identity where applicable.

Archiving, backing up, restoring, copying, compressing, packaging, exporting, encrypting, syncing, or moving a Knowledge Object or Knowledge Record MUST NOT silently create a new Object Identity unless a governed identity decision defines that behavior.

Archive and Backup Areas SHOULD preserve provenance.

Archived or backed-up material SHOULD preserve enough provenance to determine:

- what was archived or backed up;
- when it was archived or backed up where applicable;
- why it was archived or backed up where applicable;
- what version or state was preserved;
- what source material or governed entity it relates to;
- what lifecycle state applied;
- what authority level applied;
- what privacy classification applied;
- what validation state applied;
- what restoration or compatibility context applies.

Archive and Backup Areas MUST preserve privacy boundaries.

Private, confidential, sensitive, restricted, non-exportable, non-indexable, non-synchronizable, or agent-restricted material MUST NOT become exposed merely because it was archived, backed up, restored, compressed, synchronized, copied, indexed, exported, migrated, or stored in a backup target.

Backups SHOULD be handled according to the most restrictive applicable privacy expectations where mixed-privacy material is included.

Archive and Backup Areas SHOULD preserve source traceability.

Archived or backed-up Source Material, Knowledge Records, governed documents, Source References, provenance records, validation results, import records, export records, or migration records SHOULD remain traceable enough for future review, restoration, compatibility analysis, or audit.

Archive and Backup Areas SHOULD support restoration.

Restoration means bringing archived or backed-up material back into a current, review, working, import, migration, or implementation environment.

Restoration SHOULD preserve or recover:

- Object Identity where applicable;
- document identity where applicable;
- required metadata;
- Source References;
- provenance;
- relationships;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- supersession history;
- compatibility context;
- restoration context.

Restoration MUST NOT silently promote archived, rejected, deprecated, superseded, or historical material into current approved use.

Restoration MUST NOT silently remove privacy restrictions.

Restoration MUST NOT silently discard validation warnings, source-reference concerns, provenance limitations, relationship concerns, authority limits, or compatibility concerns.

Archive and Backup Areas SHOULD support validation.

A validator SHOULD be able to determine whether:

- archived material is distinguishable from current governed material;
- backup copies are distinguishable from current governed material;
- superseded, deprecated, rejected, or historical material remains identifiable;
- restored material requires review where applicable;
- archived Source Material remains traceable where required;
- backup packages preserve privacy expectations;
- backup or archive contents do not expose restricted material through indexing, synchronization, export, publication, or agent access;
- restoration does not silently alter identity, lifecycle, authority, privacy, validation, provenance, or relationship meaning.

Archive and Backup Areas SHOULD support migration.

Archived and backed-up material SHOULD be portable, restorable, interpretable, and migratable where preservation, compatibility, audit, governance, or recovery requires it.

Archive and Backup Areas are successful when historical and restorable material remains preserved, traceable, privacy-respecting, validatable, portable, and distinguishable from current governed material.

## 14. Import, Export, and Migration Areas

Import, Export, and Migration Areas are storage areas used to stage, package, review, validate, transform, transfer, receive, produce, or move material into, out of, or between compliant storage environments.

These areas exist so that humans, agents, workflows, validators, storage systems, synchronization systems, backup systems, import processes, export processes, migration processes, and implementations can distinguish exchange and transition material from current governed material.

A compliant Storage Layout SHOULD provide clearly identifiable areas for import, export, and migration material.

In the RECOMMENDED file-based reference layout, import, export, and migration material SHOULD be located under:

```text
10_Exchange
```

This reference label is not mandatory.

A compliant implementation MAY use another name, structure, transfer directory, import queue, export package, migration workspace, repository branch, database partition, staging system, package system, or implementation-specific exchange system if the implementation preserves traceability, privacy boundaries, validation expectations, compatibility, and portability.

The Import Area MAY contain:

- incoming Source Material;
- incoming Knowledge Records;
- incoming governed documents;
- imported metadata;
- imported relationships;
- imported source references;
- imported provenance records;
- imported archives;
- imported exports from another system;
- import manifests;
- import logs where governed;
- import validation results;
- import review packets;
- import mapping files;
- material awaiting classification;
- material awaiting privacy review;
- material awaiting validation;
- material awaiting placement.

The Export Area MAY contain:

- export packages;
- publication packages;
- transfer packages;
- sharing packages;
- governed document exports;
- Knowledge Record exports;
- Source Material exports;
- metadata exports;
- relationship exports;
- source-reference exports;
- provenance exports;
- validation exports;
- export manifests;
- export logs where governed;
- export validation results;
- redacted exports;
- non-exportable exclusion reports;
- downstream-use packages.

The Migration Area MAY contain:

- migration workspaces;
- migration plans;
- migration mappings;
- migration manifests;
- migration validation results;
- migration logs where governed;
- transformed records;
- transformed Source Material;
- transformed metadata;
- transformed relationships;
- transformed Source References;
- transformed provenance;
- compatibility reports;
- rollback packages;
- pre-migration snapshots;
- post-migration review packets;
- migration repair material.

Import, Export, and Migration Areas MUST remain distinguishable from current governed material.

A file stored in an import, export, or migration area MUST NOT be treated as current, approved, authoritative, valid, public, publishable, exportable, migrated, or safe for downstream use merely because it exists in the exchange area.

Import placement MAY indicate that material is entering a compliant environment.

Import placement MUST NOT replace classification, validation, source-reference review, provenance review, privacy review, authority review, relationship review, lifecycle assignment, or governed placement.

Export placement MAY indicate that material is being prepared for transfer, sharing, publication, migration, or downstream use.

Export placement MUST NOT itself grant publication permission, export permission, declassification, authority, validation success, downstream-use permission, or privacy clearance.

Migration placement MAY indicate that material is being mapped, transformed, reviewed, validated, repaired, or moved between storage systems, repositories, vaults, schemas, formats, implementations, or standard versions.

Migration placement MUST NOT itself define migration success, compatibility, validation success, identity preservation, source-reference preservation, provenance preservation, or approval.

Import, Export, and Migration Areas MUST preserve Object Identity where applicable.

Importing, exporting, mapping, transforming, copying, packaging, converting, or migrating a Knowledge Object or Knowledge Record MUST NOT silently create, merge, split, replace, redirect, or reinterpret Object Identity unless a governed identity decision defines that behavior.

Import, Export, and Migration Areas SHOULD preserve metadata.

Required metadata SHOULD be preserved during import, export, and migration.

Where metadata cannot be preserved, mapped, validated, or safely transferred, the limitation SHOULD be recorded in import, export, migration, validation, compatibility, or provenance context.

Import, Export, and Migration Areas SHOULD preserve relationships.

Relationships SHOULD remain explicit, traceable, and portable during import, export, and migration where relationship meaning affects interpretation, provenance, lifecycle state, authority, privacy, validation, compatibility, or downstream use.

Where relationships cannot be preserved, resolved, mapped, validated, or safely transferred, the limitation SHOULD be recorded.

Import, Export, and Migration Areas SHOULD preserve Source References and provenance.

Source References and provenance SHOULD remain traceable during import, export, and migration where they affect meaning, reviewability, authority, privacy, validation, compatibility, restoration, or downstream use.

Where Source Material is unavailable, restricted, externally hosted, missing, moved, redacted, excluded, or only partially available, that source-availability context SHOULD be preserved.

Import, Export, and Migration Areas MUST preserve privacy boundaries.

Import material may contain unknown, sensitive, private, confidential, restricted, non-exportable, non-indexable, non-synchronizable, or agent-restricted content.

Export material may expose restricted knowledge outside its prior privacy boundary.

Migration material may temporarily combine, transform, duplicate, or expose restricted material.

Import, export, and migration handling MUST NOT expose restricted material merely because transfer, publication, sharing, transformation, validation, synchronization, indexing, backup, or automation is convenient.

Export packages SHOULD be reviewed for Privacy Classification, redaction requirements, exclusion requirements, source restrictions, downstream-use limits, and publication permissions before transfer outside the relevant privacy boundary.

Import, Export, and Migration Areas SHOULD preserve validation context.

Import, export, and migration material SHOULD identify or support identification of:

- validation scope;
- validation result;
- validation warnings;
- validation errors;
- validation date where applicable;
- validator where applicable;
- standard or specification version;
- implementation profile;
- mapping rules;
- unresolved issues;
- compatibility concerns;
- privacy concerns;
- source-reference concerns;
- provenance concerns;
- relationship concerns;
- authority concerns;
- lifecycle concerns.

This list is descriptive and does not define a complete required metadata set.

A future specification MAY define exact import, export, and migration metadata, manifests, package structures, mapping formats, validation formats, compatibility reports, redaction reports, exclusion reports, rollback formats, and transfer procedures.

Import, Export, and Migration Areas SHOULD support validation.

A validator SHOULD be able to determine whether:

- imported material is distinguishable from reviewed current material;
- exported material has appropriate privacy and validation review where required;
- migration material preserves identity, metadata, relationships, Source References, provenance, lifecycle, authority, privacy, validation, and compatibility expectations;
- imported material has not been silently promoted into approved use;
- export packages do not expose restricted or non-exportable material;
- migration transformations are traceable;
- unresolved import, export, or migration issues remain visible;
- exchange material remains distinguishable from archives, backups, current records, drafts, generated files, indexes, and caches.

Import, Export, and Migration Areas SHOULD support audit and rollback where practical.

A migration process SHOULD preserve enough context to determine what changed, what was mapped, what failed, what was excluded, what was transformed, what was validated, what requires repair, and how to recover or roll back where practical.

Import, Export, and Migration Areas are successful when exchange and transition material remains staged, traceable, privacy-respecting, validatable, portable, and distinguishable from current governed material.

## 15. Layout Validation and Compatibility

Layout Validation and Compatibility define how a Storage Layout is checked, reviewed, preserved, adapted, migrated, imported, exported, backed up, restored, synchronized, indexed, or implemented without losing governed meaning.

Layout Validation exists so that humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, backup systems, synchronization systems, and implementations can determine whether a storage environment satisfies SS-0002 and the higher-authority standards it depends on.

Layout Compatibility exists so that a storage environment can evolve, move, scale, synchronize, back up, restore, export, import, migrate, or be implemented in different tools without semantic loss.

A compliant Storage Layout SHOULD support validation.

A Storage Layout SHOULD be validatable for:

- root storage environment clarity;
- top-level storage area clarity;
- Source Material placement;
- Knowledge Record placement;
- governed document placement;
- draft, review, and working placement;
- implementation-support placement;
- agent-support placement;
- workflow-support placement;
- supporting asset placement;
- archive placement;
- backup placement;
- import placement;
- export placement;
- migration placement;
- generated-file placement;
- index and cache placement;
- privacy boundary preservation;
- current and historical material separation;
- generated and governed material separation;
- implementation-specific and governed material separation;
- source traceability;
- Object Identity preservation;
- metadata preservation;
- relationship preservation;
- Source Reference preservation;
- provenance preservation;
- Lifecycle State preservation;
- Authority Level preservation;
- Privacy Classification preservation;
- Validation State preservation;
- portability;
- migration readiness;
- import readiness;
- export readiness;
- restoration readiness.

A Layout Validation process MAY be performed by a human, agent, workflow, validator, script, implementation, migration process, import process, export process, backup process, synchronization process, or future governed mechanism.

A Layout Validation process MUST remain reviewable where validation affects governed meaning, privacy, authority, lifecycle state, publication, export, migration, restoration, or downstream use.

A Layout Validation process MUST NOT become approval by itself unless a governed workflow or specification explicitly defines that behavior.

A Layout Validation result MUST remain distinguishable from Lifecycle State, Authority Level, Privacy Classification, publication permission, export permission, agent permission, workflow permission, implementation visibility, backup success, synchronization success, index success, or downstream-use permission.

Layout Validation SHOULD identify errors and warnings.

A Layout Validation Error indicates that the Storage Layout does not satisfy a mandatory layout, separation, privacy, preservation, compatibility, or higher-authority requirement within the applicable validation scope.

A Layout Validation Warning indicates a potential issue, risk, ambiguity, incompleteness, inconsistency, or recommended improvement without necessarily making the Storage Layout invalid.

A future specification MAY define exact layout validation values, error codes, warning codes, conformance tests, validator outputs, machine-readable reports, and validation tooling.

A Storage Layout SHOULD preserve compatibility across layout changes.

A layout change SHOULD preserve the ability to locate, interpret, validate, migrate, import, export, back up, restore, synchronize, index, and process governed material.

A layout change SHOULD NOT silently break:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- source availability context;
- archive history;
- backup restoration;
- import mappings;
- export mappings;
- migration mappings;
- workflow routing;
- agent instructions;
- implementation profiles;
- privacy handling;
- downstream use.

A layout change that materially affects storage meaning, placement rules, validation expectations, privacy handling, import behavior, export behavior, migration behavior, backup behavior, synchronization behavior, implementation behavior, workflow routing, or agent behavior SHOULD be documented.

Documentation for a material layout change SHOULD identify:

- what changed;
- why it changed;
- what storage areas are affected;
- what governed entities are affected;
- whether migration is required;
- whether validation is required;
- whether privacy review is required;
- whether source references are affected;
- whether relationships are affected;
- whether workflows are affected;
- whether agents are affected;
- whether implementation files are affected;
- whether backups or archives are affected;
- whether compatibility risks exist.

A Storage Layout SHOULD support partial compliance review.

A simple implementation MAY conform to SS-0002 by preserving the required distinctions even if it does not physically implement every RECOMMENDED storage area.

A mature implementation SHOULD provide more explicit storage separation where scale, privacy, validation, agent use, workflow use, backup, synchronization, import, export, migration, or implementation complexity requires it.

Partial compliance MUST NOT be used to justify identity confusion, metadata loss, relationship loss, source-reference loss, provenance loss, privacy exposure, validation ambiguity, authority confusion, lifecycle ambiguity, archive confusion, import ambiguity, export ambiguity, migration ambiguity, backup ambiguity, or implementation lock-in.

A Storage Layout SHOULD support compatibility review during import, export, migration, backup, restoration, and synchronization.

Compatibility review SHOULD confirm that governed material remains:

- identifiable;
- distinguishable;
- traceable;
- reviewable;
- privacy-respecting;
- validatable;
- portable;
- restorable;
- migratable;
- implementation-independent;
- compatible with higher-authority standards.

A Storage Layout MUST preserve higher-authority meaning.

No layout validation result, compatibility result, folder placement, filename, path, index, cache, generated report, backup state, sync state, archive state, import state, export state, migration state, implementation state, workflow state, or agent state may override Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, governance, or knowledge meaning unless a higher-authority governed document explicitly defines that behavior.

Layout Validation and Compatibility are successful when storage layout can be checked, reviewed, repaired, moved, restored, synchronized, backed up, imported, exported, migrated, and implemented without semantic loss, privacy exposure, authority confusion, validation ambiguity, or governance drift.

## 16. Layout Governance and Evolution

Layout Governance and Evolution define how Storage Layouts may be changed, extended, deprecated, superseded, migrated, validated, or adapted over time.

Storage Layouts are expected to evolve as The Brain Standard grows, implementations mature, storage environments change, agents become more capable, workflows become more formal, and migration, backup, synchronization, import, export, validation, and privacy requirements become more precise.

Layout evolution is allowed.

Layout drift is not allowed.

Layout drift occurs when storage areas, folder names, placement rules, implementation defaults, plugin behavior, agent behavior, workflow convenience, synchronization behavior, backup behavior, import behavior, export behavior, migration behavior, index behavior, cache behavior, or user habit informally changes how the Storage Layout works without review, documentation, or governance where such change affects interpretation, privacy, validation, compatibility, or downstream use.

A Storage Layout MAY evolve through:

- adding a storage area;
- removing a storage area;
- renaming a storage area;
- splitting a storage area;
- combining storage areas;
- moving material between storage areas;
- changing placement rules;
- changing implementation-support placement;
- changing agent-support placement;
- changing workflow-support placement;
- changing archive or backup handling;
- changing import, export, or migration handling;
- changing generated-file or cache handling;
- changing validation expectations;
- changing privacy handling expectations;
- changing synchronization or indexing expectations;
- changing implementation profiles;
- changing reference-layout recommendations.

A layout change SHOULD be documented when it affects:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- governed document placement;
- Source Material placement;
- Knowledge Record placement;
- current and historical material separation;
- import behavior;
- export behavior;
- migration behavior;
- archive behavior;
- backup behavior;
- synchronization behavior;
- indexing behavior;
- generated-file behavior;
- agent behavior;
- workflow behavior;
- implementation behavior;
- downstream use.

Minor layout changes MAY be handled through ordinary maintenance when they do not affect governed meaning, privacy, validation, compatibility, source traceability, migration, import, export, backup, synchronization, agent behavior, workflow behavior, or implementation behavior.

A minor layout change MAY include:

- improving a folder label for clarity;
- correcting a spelling issue;
- adding a local readme;
- reorganizing temporary files;
- moving clearly non-governed support material;
- adding convenience notes;
- improving human readability;
- removing unused generated files where safe.

A material layout change SHOULD include review.

A material layout change SHOULD identify:

- what changed;
- why the change was made;
- what storage areas are affected;
- what governed entities are affected;
- whether migration is required;
- whether validation is required;
- whether privacy review is required;
- whether source traceability is affected;
- whether relationships are affected;
- whether provenance is affected;
- whether archives or backups are affected;
- whether import, export, or migration mappings are affected;
- whether agents or workflows are affected;
- whether implementation profiles are affected;
- whether compatibility risks exist.

A material layout change SHOULD preserve compatibility where practical.

Where compatibility cannot be fully preserved, the change SHOULD include migration guidance, validation guidance, deprecation notes, supersession notes, archive guidance, or implementation-profile guidance.

A layout change MUST NOT silently reinterpret existing material.

A layout change MUST NOT silently change Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, relationship meaning, Source Reference meaning, provenance meaning, publication permission, export permission, agent permission, workflow permission, or downstream-use permission.

A layout change MUST NOT silently expose restricted material.

A layout change MUST NOT silently move private, confidential, sensitive, restricted, non-exportable, non-indexable, non-synchronizable, or agent-restricted material into a less protected area.

A layout change SHOULD preserve historical traceability.

If a storage area is renamed, split, combined, deprecated, superseded, archived, replaced, or removed, the prior layout SHOULD remain understandable where historical review, restoration, audit, migration, validation, or compatibility requires it.

A Storage Layout MAY support layout manifests, layout maps, migration notes, compatibility notes, validation reports, or implementation profiles.

Those support materials MAY help humans, agents, workflows, validators, storage systems, and implementations understand layout changes.

Those support materials MUST NOT override higher-authority standards.

A Storage Layout SHOULD prevent informal implementation defaults from becoming architecture.

A tool, plugin, script, database, synchronization system, backup system, indexer, cache, agent, workflow, or user interface may create storage artifacts.

Such artifacts become part of the governed Storage Layout only when their role, handling expectations, validation expectations, privacy expectations, and compatibility expectations are documented or governed where needed.

Layout Governance and Evolution are successful when storage layouts can improve over time without governance drift, semantic loss, privacy exposure, validation ambiguity, compatibility failure, implementation lock-in, or hidden redefinition of knowledge meaning.

## 17. Implementation Boundaries

Implementation Boundaries define what a storage implementation may adapt, automate, generate, display, synchronize, index, cache, validate, import, export, migrate, or configure without redefining the Storage Layout or higher-authority knowledge meaning.

SS-0002 defines storage-layout expectations at the standard level.

SS-0002 does not require every implementation to use identical folder names, exact path structures, file-system ordering, database structures, plugin behavior, operating systems, synchronization tools, backup tools, validation tools, user interfaces, or automation runtimes.

A compliant implementation MAY adapt the physical layout to fit:

- local file systems;
- Obsidian vaults;
- Git repositories;
- database-backed systems;
- cloud-synchronized folders;
- encrypted storage systems;
- local-first applications;
- archive packages;
- export packages;
- migration workspaces;
- agent workspaces;
- workflow engines;
- future storage systems.

Implementation adaptation is allowed only when the implementation preserves the governed meaning, separation rules, privacy boundaries, validation expectations, portability, source traceability, and compatibility expectations defined by SS-0002 and higher-authority standards.

An implementation MUST NOT make implementation behavior the sole source of governed meaning.

Implementation behavior includes:

- plugin fields;
- database columns;
- hidden application state;
- user-interface state;
- graph layout;
- search ranking;
- tag behavior;
- backlink behavior;
- sync status;
- publication status;
- file visibility;
- generated indexes;
- generated caches;
- automation state;
- agent memory;
- workflow memory;
- local configuration;
- proprietary metadata;
- implementation-specific identifiers.

These mechanisms MAY support storage layout, usability, navigation, automation, indexing, validation, backup, synchronization, import, export, migration, or display.

They MUST NOT replace explicit Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, governance, or knowledge meaning where those are required.

An implementation MAY use recommended reference labels such as:

- `00_System`
- `01_Governance`
- `02_Knowledge`
- `03_Sources`
- `04_Working`
- `05_Implementation`
- `06_Agents`
- `07_Workflows`
- `08_Assets`
- `09_Archives`
- `10_Exchange`
- `11_Generated`

These labels are reference labels.

They are not mandatory universal folder names.

An implementation MAY rename, reorder, split, combine, translate, hide, or adapt these labels when required by the implementation environment.

Any adaptation MUST preserve the storage purpose and required distinctions.

An implementation MAY create implementation-specific files at the root level when required by a tool, repository, application, plugin, script, package manager, validator, automation system, or synchronization system.

Root-level implementation files SHOULD remain distinguishable from governed documents, Knowledge Records, Source Material, archives, backups, imports, exports, migrations, indexes, caches, and generated files.

An implementation MAY generate indexes, caches, embeddings, reports, manifests, maps, logs, or summaries.

Generated implementation artifacts MUST remain distinguishable from governed material unless a governed specification or workflow explicitly assigns them a governed role.

An implementation MAY automate placement, movement, validation, import, export, backup, synchronization, indexing, migration, or archive handling.

Automation MUST remain within governed boundaries.

Automation MUST NOT silently approve, reject, deprecate, supersede, archive, publish, export, declassify, delete, overwrite, migrate, or reinterpret governed material where human review, governance review, privacy review, validation review, source-reference review, provenance review, authority review, compatibility review, or workflow review is required.

An implementation MAY provide views, dashboards, search interfaces, graphs, reports, indexes, filters, tags, collections, saved queries, or navigation aids.

Implementation views MAY assist discovery, review, validation, workflow routing, and usability.

Implementation views MUST NOT replace governed storage placement, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, or governed meaning.

An implementation MAY store Source Material externally.

External Source Material storage is compliant only if Source References, source identifiers, source availability context, provenance, privacy expectations, validation expectations, import behavior, export behavior, migration behavior, and backup or preservation expectations remain traceable and reviewable.

An implementation MAY use external backup systems, cloud storage, synchronization tools, or version-control systems.

These systems MUST preserve privacy boundaries and MUST NOT become required for knowledge meaning to remain understandable, portable, validatable, or recoverable.

An implementation MAY use agents and workflows to assist storage-layout maintenance.

Agents and workflows MAY classify, suggest, validate, route, stage, summarize, index, map, import, export, migrate, or report on storage material.

Agents and workflows MUST NOT become unreviewable authorities for governed placement, approval, declassification, publication, export, deletion, supersession, migration, or reinterpretation where review is required.

Implementation Boundaries SHOULD support portability.

A compliant implementation SHOULD make it possible to export, inspect, migrate, or reconstruct the storage layout without relying exclusively on proprietary application state.

Implementation Boundaries SHOULD support validation.

A validator SHOULD be able to determine whether an implementation:

- preserves required storage distinctions;
- keeps implementation files distinguishable from governed files;
- keeps generated files distinguishable from authored files;
- keeps indexes and caches distinguishable from authoritative records;
- preserves Source Material and Knowledge Record boundaries;
- preserves Object Identity;
- preserves required metadata;
- preserves relationships;
- preserves Source References and provenance;
- preserves Lifecycle State;
- preserves Authority Level;
- preserves Privacy Classification;
- preserves Validation State;
- protects restricted material;
- supports import, export, migration, backup, restoration, and synchronization without semantic loss.

Implementation Boundaries are successful when implementations can adapt the Storage Layout to practical tools and environments without redefining the standard, weakening privacy, hiding meaning, breaking validation, or creating implementation lock-in.

## 18. Conformance and Success Criteria

Conformance and Success Criteria define when a Storage Layout satisfies SS-0002.

A Storage Layout conforms to SS-0002 when it preserves the required storage distinctions, placement expectations, privacy boundaries, validation expectations, source traceability, portability, and implementation-independence requirements defined by this document and higher-authority standards.

A conforming Storage Layout SHALL preserve the distinction between:

- Source Material;
- Knowledge Records;
- governed documents;
- drafts;
- review material;
- working material;
- implementation-support files;
- agent-support files;
- workflow-support files;
- supporting assets;
- archives;
- backups;
- imports;
- exports;
- migrations;
- generated files;
- indexes;
- caches;
- current governed material;
- historical material;
- temporary material;
- implementation-specific material.

A conforming Storage Layout MUST NOT use folder placement, filename, vault path, repository path, root location, archive location, backup location, import location, export location, migration location, generated-file location, index location, cache location, implementation visibility, sync state, graph position, search ranking, tag behavior, backlink behavior, agent memory, workflow memory, or hidden application state as the sole source of governed meaning.

A conforming Storage Layout SHALL preserve Object Identity.

A conforming Storage Layout SHALL preserve required metadata.

A conforming Storage Layout SHALL preserve relationship meaning.

A conforming Storage Layout SHALL preserve Source References and provenance.

A conforming Storage Layout SHALL preserve Lifecycle State where required.

A conforming Storage Layout SHALL preserve Authority Level where required.

A conforming Storage Layout SHALL preserve Privacy Classification.

A conforming Storage Layout SHALL preserve Validation State and validation expectations where required.

A conforming Storage Layout SHALL preserve source traceability.

A conforming Storage Layout SHALL preserve the distinction between current, draft, review, working, archived, backed-up, imported, exported, migrated, generated, cached, and implementation-specific material where those distinctions affect interpretation or use.

A conforming Storage Layout SHOULD be understandable to humans.

A human should be able to inspect the storage environment and understand the basic purpose of major storage areas without relying on hidden tool state.

A conforming Storage Layout SHOULD be usable by agents.

An agent should be able to identify storage areas, placement expectations, review boundaries, privacy risks, validation expectations, and non-authoritative generated material without relying on undocumented assumptions.

A conforming Storage Layout SHOULD be compatible with workflows.

A workflow should be able to route, review, validate, approve, reject, repair, archive, import, export, migrate, back up, restore, synchronize, or maintain material without silently redefining governed meaning.

A conforming Storage Layout SHOULD be compatible with validation.

A validator should be able to check placement, separation, privacy, source traceability, metadata preservation, identity preservation, relationship preservation, provenance preservation, lifecycle handling, authority handling, generated-file handling, import/export/migration handling, archive handling, backup handling, and implementation boundaries.

A conforming Storage Layout SHOULD be portable.

A compliant storage environment should be movable, copyable, exportable, importable, restorable, reorganizable, and migratable without semantic loss.

A conforming Storage Layout SHOULD be implementation-independent.

No specific application, plugin, database, model, agent runtime, workflow tool, cloud provider, synchronization system, backup tool, indexer, cache, graph system, or user interface may become required for the knowledge itself to remain understandable and usable.

A Storage Layout MAY be partially conforming.

Partial conformance may be acceptable for simple implementations, early reference implementations, prototypes, migrations, imports, exports, archives, or constrained environments when the required distinctions and higher-authority meaning are preserved.

Partial conformance MUST NOT justify:

- Object Identity confusion;
- metadata loss;
- relationship ambiguity;
- Source Reference loss;
- provenance loss;
- lifecycle ambiguity;
- authority ambiguity;
- privacy exposure;
- validation ambiguity;
- source traceability loss;
- archive confusion;
- backup confusion;
- import ambiguity;
- export ambiguity;
- migration ambiguity;
- generated-file authority confusion;
- implementation lock-in;
- governance drift.

A Storage Layout is non-conforming when it causes or permits:

- storage location to define knowledge meaning by itself;
- folder placement to define Object Identity by itself;
- filenames to define stable Object Identity by themselves;
- Source Material to be confused with Knowledge Records;
- drafts to be confused with approved current records;
- generated files to be confused with governed records;
- indexes or caches to be treated as authoritative records;
- implementation files to override standards;
- agent outputs to become unreviewable authority;
- workflow completion to become approval without governance;
- archived material to be treated as current without review;
- backup material to be treated as current authority without review;
- imported material to be silently promoted into governed use;
- exported material to bypass privacy or validation review;
- migration material to silently reinterpret identity, relationships, provenance, or meaning;
- restricted material to be exposed through layout, indexing, synchronization, export, backup, publication, or automation;
- layout changes to create governance drift.

SS-0002 is successful when storage layout provides a practical, readable, portable, validatable, privacy-respecting, agent-usable, workflow-compatible, and implementation-independent structure for The Brain Standard.

SS-0002 is successful when humans can understand where material belongs.

SS-0002 is successful when agents can operate without guessing hidden storage meaning.

SS-0002 is successful when workflows can route material without redefining governance.

SS-0002 is successful when validators can check placement and compatibility.

SS-0002 is successful when Source Material remains distinguishable from Knowledge Records.

SS-0002 is successful when governed documents remain distinguishable from implementation-support files.

SS-0002 is successful when drafts, reviews, archives, backups, imports, exports, migrations, indexes, caches, and generated files remain distinguishable from current governed material.

SS-0002 is successful when privacy boundaries are preserved across all storage areas.

SS-0002 is successful when storage organization supports knowledge without becoming the source of knowledge meaning.

SS-0002 is successful when future specifications, implementations, agents, workflows, validators, migration processes, backup systems, synchronization systems, import processes, export processes, and operational guides can rely on a clear practical layout without weakening the higher-authority standards.
