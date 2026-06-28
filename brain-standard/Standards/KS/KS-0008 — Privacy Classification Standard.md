# KS-0008 — Privacy Classification Standard

Document ID: KS-0008
Title: Privacy Classification Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-27
Last Updated: 2026-06-27
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.8 — Privacy Classification Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and privacy-classification rules are interpreted within KS-0008.

Where conflicts arise between Privacy Classification, privacy metadata, access, visibility, exposure, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation visibility, downstream use, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, validation state, storage behavior, import behavior, export behavior, migration behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0008 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0008 extends KS-0001 by defining standard-level Privacy Classification behavior for Knowledge Objects, Knowledge Records, Source References, provenance records, relationships, validation results, workflow outputs, agent outputs, imports, exports, migrations, governed documents where applicable, decisions, and other governed entities.

KS-0008 depends on KS-0002 because Privacy Classification must preserve stable Object Identity across access changes, visibility changes, restriction changes, publication, synchronization, indexing, export, backup, import, migration, archival, and implementation replacement.

KS-0008 depends on KS-0003 because privacy meaning may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through metadata.

KS-0008 depends on KS-0004 because relationships may expose, restrict, inherit, or imply privacy-sensitive information and because relationship privacy must remain distinguishable from relationship existence, relationship strength, relationship confidence, graph position, backlink behavior, or implementation-specific linking.

KS-0008 depends on KS-0005 because Source References, provenance, evidence, attribution, source privacy, source availability, and source handling may affect Privacy Classification without replacing it.

KS-0008 depends on KS-0006 because Lifecycle State may affect privacy handling, but Lifecycle State does not replace Privacy Classification.

KS-0008 depends on KS-0007 because Authority Level may affect review, publication, or downstream use, but Authority Level does not replace Privacy Classification.

If KS-0008 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

KS-0008 defines Privacy Classification at the conceptual standard level.

KS-0008 does not define exact Markdown front matter syntax, exact metadata field names, exact privacy values, exact access-control systems, exact encryption methods, exact user roles, exact permission schemas, exact publication rules, exact synchronization tooling, exact indexing mechanisms, exact backup procedures, exact agent permission formats, exact workflow routing rules, exact implementation-specific labels, exact storage paths, or exact user-interface behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, privacy vocabularies, access-control specifications, publication specifications, synchronization specifications, backup specifications, and operational guides.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, Object Identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Privacy Scope refers to the defined context in which a Privacy Classification applies.
- Privacy Assignment refers to the act of assigning, proposing, confirming, revising, limiting, escalating, reducing, removing, or preserving Privacy Classification for a governed entity.
- Privacy Review refers to the review process used to determine whether a Privacy Classification is appropriate, sufficient, current, traceable, compatible, and safe for access, exposure, publication, export, synchronization, indexing, backup, agent use, workflow use, implementation use, or downstream use.
- Privacy Metadata refers to metadata that records, expresses, supports, validates, or preserves Privacy Classification, privacy scope, privacy assignment, privacy review, or privacy history.
- Access refers to the ability of a human, agent, workflow, implementation, system, validator, storage process, export process, migration process, or downstream user to read, modify, route, index, expose, publish, copy, synchronize, export, back up, or otherwise interact with a governed entity.
- Visibility refers to whether a governed entity is discoverable, displayed, indexed, searched, listed, previewed, linked, surfaced, summarized, synchronized, published, or exposed by an implementation, workflow, agent, or storage system.
- Exposure refers to the disclosure, display, transmission, extraction, indexing, summarization, publication, export, synchronization, backup, migration, or downstream use of privacy-relevant knowledge.
- Publication refers to making a governed entity available beyond its prior privacy boundary.
- Synchronization refers to copying, mirroring, syncing, replicating, caching, or transmitting a governed entity across devices, repositories, vaults, services, tools, implementations, or environments.
- Indexing refers to making a governed entity searchable, retrievable, ranked, embedded, summarized, vectorized, cached, tagged, categorized, or otherwise discoverable by a system, agent, workflow, validator, or implementation.
- Export refers to the process of producing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, Source References, provenance, or external content from a compliant environment for use elsewhere.
- Backup refers to preserving a copy of a governed entity for restoration, continuity, archival, audit, migration, disaster recovery, or long-term preservation.
- Agent Access refers to the ability of an agent to read, classify, summarize, extract, transform, validate, route, link, modify, export, publish, or reason over a governed entity.
- Workflow Access refers to the ability of a workflow to route, review, validate, approve, reject, publish, restrict, quarantine, export, synchronize, back up, migrate, or otherwise process a governed entity.
- Implementation Access refers to the ability of a software tool, vault, database, file system, interface, plugin, automation, or service to expose, index, cache, sync, search, display, publish, export, back up, or process a governed entity.
- Downstream Use refers to later use of a governed entity for interpretation, automation, publication, export, migration, relationship creation, validation, decision support, agent reasoning, workflow execution, implementation behavior, or other dependent activity.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Validation refers to the process of checking whether a governed entity satisfies the applicable standards, specifications, metadata expectations, provenance expectations, relationship expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0008 is to define how Privacy Classification works across The Brain Standard.

KS-0001 establishes Privacy Classification as a required knowledge-level concept where permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream use affects knowledge handling.

KS-0008 defines the standard-level behavior required to create, assign, interpret, preserve, review, validate, limit, escalate, reduce, migrate, import, export, govern, and maintain Privacy Classification.

Privacy Classification exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine how a governed entity may be accessed, exposed, routed, processed, published, synchronized, indexed, exported, backed up, migrated, or used downstream.

KS-0008 exists to prevent privacy confusion.

Privacy confusion occurs when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, or implementations cannot reliably determine:

- what Privacy Classification applies to a governed entity;
- what scope the Privacy Classification applies to;
- whether access is permitted;
- whether visibility is permitted;
- whether publication is permitted;
- whether synchronization is permitted;
- whether indexing is permitted;
- whether export is permitted;
- whether backup is permitted;
- whether agent access is permitted;
- whether workflow access is permitted;
- whether implementation access is permitted;
- whether downstream use is permitted;
- whether privacy handling has been confused with Lifecycle State, Authority Level, Validation State, Provenance, Source Reference existence, relationship existence, storage location, folder placement, filename, tags, implementation visibility, workflow completion, agent confidence, or user-interface behavior.

KS-0008 defines Privacy Classification behavior for:

- Knowledge Objects;
- Knowledge Records;
- Source References;
- Source Material where applicable;
- provenance records;
- relationships;
- metadata records;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- governed documents where applicable;
- decisions;
- other governed entities.

KS-0008 does not define exact metadata field names, exact Markdown front matter syntax, exact privacy values, exact permission models, exact role-based access-control rules, exact encryption requirements, exact publication procedures, exact synchronization procedures, exact indexing procedures, exact backup procedures, exact agent permission formats, exact workflow routing rules, exact implementation-specific labels, exact storage paths, or exact user-interface behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, privacy vocabularies, access-control specifications, publication specifications, synchronization specifications, indexing specifications, backup specifications, and operational guides.

KS-0008 defines Privacy Classification at the standard level.

A future specification MAY define exact privacy fields, allowed privacy values, privacy scopes, assignment rules, review rules, validation rules, escalation rules, declassification rules, redaction rules, access-control mappings, publication rules, synchronization rules, indexing rules, backup rules, import mappings, export mappings, migration mappings, agent handling rules, workflow triggers, or serialization syntax.

Such specifications are valid only when they preserve the Privacy Classification behavior defined by KS-0008.

The primary purpose of KS-0008 is to ensure that Privacy Classification remains explicit, scoped, interpretable, portable, traceable, reviewable, privacy-preserving, provenance-aware, validatable, compatible, and implementation-independent across time, tools, storage systems, workflows, agents, validators, and implementations.

KS-0008 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine:

- what Privacy Classification applies to a governed entity;
- what the Privacy Classification means;
- what privacy scope applies;
- who or what assigned the Privacy Classification where applicable;
- what review, validation, provenance, source context, relationship context, lifecycle state, authority level, compatibility, or governance decision supports the Privacy Classification;
- whether the Privacy Classification is current, historical, limited, escalated, reduced, superseded, inherited, proposed, reviewed, approved, rejected, deprecated, archived, restricted, quarantined, or otherwise governed;
- whether the Privacy Classification affects access, visibility, routing, publication, synchronization, indexing, export, backup, migration, import, workflow behavior, agent behavior, implementation behavior, validation, relationships, Source References, provenance, authority, lifecycle handling, compatibility, or downstream use;
- whether Privacy Classification behavior can be preserved without relying on hidden application state, folder placement, filename convention, tag convention, user-interface state, workflow memory, agent memory, implementation-specific labels, search ranking, graph centrality, backlink behavior, publication status, or undocumented practice.

## 2. Relationship to Prior Standards

KS-0008 is subordinate to and derived from the constitutional foundation of The Brain Standard.

KS-0008 depends on:

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
- KS-0007 — Authority Level Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

KS-0008 applies that purpose by defining Privacy Classification behavior that remains portable, interpretable, reviewable, privacy-preserving, and independent of any single storage system, workflow engine, agent framework, validation tool, software tool, user interface, access-control system, synchronization service, indexing system, backup process, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

KS-0008 applies those principles by requiring Privacy Classification to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- source distinction;
- provenance;
- privacy boundaries;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability;
- governed evolution.

TB-0002 establishes the layered architecture of The Brain Standard.

KS-0008 belongs to Layer 1 — Universal Knowledge Standard.

Because Privacy Classification affects knowledge handling, access, exposure, visibility, routing, publication, synchronization, indexing, export, backup, migration, import, workflow behavior, agent behavior, implementation behavior, and downstream use, KS-0008 defines Privacy Classification independently of storage systems, user interfaces, folders, filenames, tags, databases, graph tools, workflow engines, agent systems, synchronization tools, indexing tools, backup tools, and implementations.

Layer 2 storage standards depend on KS-0008 because storage must preserve Privacy Classification without defining privacy meaning.

Layer 3 agent standards depend on KS-0008 because agents may read, propose, classify, validate, route, summarize, extract, transform, or restrict privacy-related information without becoming unreviewable authorities over privacy handling.

Layer 4 workflow standards depend on KS-0008 because workflows may create, review, approve, reject, escalate, reduce, validate, quarantine, redact, publish, synchronize, index, export, import, migrate, or preserve Privacy Classification.

Layer 5 implementation documents depend on KS-0008 because implementations must create, read, preserve, display, restrict, index, synchronize, export, import, back up, validate, and migrate Privacy Classification without redefining standard-level privacy meaning through implementation-specific behavior.

TB-0003 establishes the governance model for The Brain Standard.

KS-0008 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, KS-0008 has high authority within its scope but remains subordinate to constitutional documents.

KS-0001 defines the foundational Knowledge Object Model.

KS-0008 does not replace the Knowledge Object Model.

KS-0008 refines one part of that model: Privacy Classification.

In practical terms:

- KS-0001 answers: What is a Knowledge Object?
- KS-0001 answers: What is a Knowledge Record?
- KS-0001 answers: Why must Privacy Classification exist where privacy affects handling?
- KS-0008 answers: How must Privacy Classification behave?
- KS-0008 answers: What makes Privacy Classification explicit, scoped, portable, reviewable, and validatable?
- KS-0008 answers: How should access, visibility, exposure, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, and downstream use be treated?

KS-0002 defines Object Identity.

KS-0008 depends on KS-0002 because Privacy Classification must not change Object Identity by itself.

A Knowledge Object SHOULD retain its Object Identity when its Privacy Classification changes.

A Knowledge Object MUST NOT receive a new Object Identity merely because it becomes public, internal, private, restricted, confidential, sensitive, non-exportable, agent-restricted, workflow-restricted, implementation-restricted, publishable, non-publishable, indexed, non-indexed, synchronized, non-synchronized, backed up, not backed up, or governed by another privacy-related classification.

An identity change MAY occur through a governed process where the Knowledge Object becomes a meaningfully different object, but the privacy change alone does not define the identity change.

KS-0003 defines metadata behavior.

KS-0008 depends on KS-0003 because Privacy Classification may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through privacy metadata.

Privacy metadata MUST remain distinguishable from Object Identity, lifecycle metadata, authority metadata, validation metadata, provenance metadata, relationship metadata, Source Reference metadata, workflow metadata, agent metadata, implementation metadata, storage metadata, and hidden application behavior.

KS-0004 defines relationship behavior.

KS-0008 depends on KS-0004 because relationships may reveal, imply, inherit, restrict, preserve, or expose privacy-sensitive information.

A relationship MAY carry privacy handling requirements.

A relationship MAY reveal restricted context even when the related Knowledge Objects appear less restricted individually.

A relationship MAY require its own Privacy Classification where relationship existence, relationship type, direction, context, provenance, authority, lifecycle state, or validation state creates privacy risk.

A relationship MUST NOT become safe for exposure merely because the connected entities are visible, indexed, linked, frequently traversed, central in a graph, present in backlinks, returned in search results, inferred by an agent, or created by an implementation.

KS-0005 defines Source Reference and Provenance behavior.

KS-0008 depends on KS-0005 because Source References, Source Material, evidence, attribution, extraction history, transformation history, source privacy, source availability, import provenance, export provenance, migration provenance, and review traceability may affect Privacy Classification.

A Source Reference MAY require privacy handling.

Source Material MAY be more restricted than the Knowledge Record derived from it.

A Knowledge Record MAY be more restricted than its Source Material because of interpretation, aggregation, relationships, derived insight, personal context, workflow context, agent output, or downstream-use risk.

Provenance MAY contain privacy-sensitive information even when the main knowledge content appears safe to expose.

Source existence, citation existence, provenance existence, source availability, source reliability, source authority, or source popularity MUST NOT override Privacy Classification unless a governed privacy process explicitly defines that behavior within a defined scope.

KS-0006 defines Lifecycle State behavior.

KS-0008 depends on KS-0006 because Lifecycle State may affect whether a governed entity may be accessed, reviewed, restricted, quarantined, repaired, published, synchronized, indexed, exported, backed up, imported, migrated, archived, or used downstream.

Lifecycle State MUST remain distinguishable from Privacy Classification.

A lifecycle state may affect handling, but it does not replace privacy meaning.

An entity may be:

- draft and public;
- draft and restricted;
- approved and private;
- approved and confidential;
- rejected and sensitive;
- archived and restricted;
- superseded and confidential;
- deprecated and non-exportable;
- quarantined because of unresolved privacy risk.

KS-0007 defines Authority Level behavior.

KS-0008 depends on KS-0007 because Authority Level may affect review, governance, publication, validation, or downstream-use expectations, but Authority Level does not replace Privacy Classification.

Authority Level MUST remain distinguishable from Privacy Classification.

A governed entity may be:

- high-authority and private;
- high-authority and non-exportable;
- low-authority and public;
- approved and confidential;
- authoritative for internal use but not publishable;
- source-supported but still restricted;
- validated but not agent-readable;
- publishable but low-authority;
- archived but still privacy-protected.

Authority does not create access permission by itself.

Approval does not create publication permission by itself.

Validation does not create export permission by itself.

Publication does not remove privacy obligations by itself.

KS-0008 preserves the following KS-0001 rules:

- Privacy Classification describes permitted visibility, access, exposure, or handling expectations of a Knowledge Object or Knowledge Record.
- Privacy Classification SHOULD be present or supported where privacy affects interpretation, handling, access, publication, export, automation, or downstream use.
- Knowledge Objects and Knowledge Records MUST remain implementation-independent, portable, reviewable, and interpretable by humans and AI systems.
- Agents and workflows must not redefine knowledge meaning or governed handling through hidden behavior.

KS-0008 preserves the following KS-0002 rules:

- Object Identity remains independent of filenames, folder paths, storage locations, display titles, application-specific identifiers, and implementation-specific behavior.
- Privacy changes MUST NOT silently create identity confusion.
- Identity decisions SHOULD preserve provenance when assignment, preservation, change, merge, split, redirect, import, export, migration, or supersession affects interpretation or compatibility.

KS-0008 preserves the following KS-0003 rules:

- Privacy metadata describes permitted visibility, access, handling, routing, synchronization, indexing, export, backup, publication, agent access, or disclosure expectations.
- Privacy metadata MUST remain explicit where privacy affects handling.
- Privacy metadata SHALL take precedence over operational convenience when privacy and convenience conflict.
- Metadata MUST NOT expose restricted knowledge merely because it improves search, provenance, validation, linking, automation, review, export, publication, or implementation convenience.

KS-0008 preserves the following KS-0004 rules:

- Relationships may have privacy classification.
- Relationships MUST preserve privacy boundaries.
- Relationship existence, relationship type, relationship context, and relationship provenance may create privacy concerns even when the related entities appear safe in isolation.
- Implementation-specific links, backlinks, graph centrality, search ranking, or agent inference MUST NOT replace governed relationship privacy handling.

KS-0008 preserves the following KS-0005 rules:

- Source References and provenance may contain restricted information.
- Source Material and Knowledge Records SHALL remain distinguishable.
- Provenance SHOULD preserve privacy boundaries when provenance refers to restricted source material, restricted users, restricted workflows, restricted agents, or restricted content.
- Source-reference and provenance behavior MUST NOT rely on hidden application state, folder placement, filename convention, citation style, user memory, agent memory, workflow memory, or implementation-specific behavior when privacy affects handling.

KS-0008 preserves the following KS-0006 rules:

- Lifecycle State MUST remain distinguishable from Privacy Classification.
- A lifecycle state MUST NOT weaken privacy requirements.
- Draft, rejected, deprecated, superseded, archived, restricted, quarantined, pending-validation, or needs-repair entities may still contain private, confidential, sensitive, non-exportable, or agent-restricted information.
- Privacy boundaries MUST be preserved during lifecycle handling.

KS-0008 preserves the following KS-0007 rules:

- Authority Level MUST remain distinguishable from Privacy Classification.
- Authority does not automatically create access, publication, synchronization, indexing, export, backup, agent-use, workflow-use, implementation-use, or downstream-use permission.
- High-authority knowledge may still be private, confidential, sensitive, non-exportable, agent-restricted, workflow-restricted, or otherwise privacy-limited.
- Low-authority knowledge may still require privacy protection.

KS-0008 is successful when it extends the prior standards into a clear Privacy Classification model without weakening Object Identity, metadata role boundaries, relationship behavior, source-reference behavior, provenance preservation, lifecycle meaning, authority expectations, validation expectations, implementation independence, or practical daily usability.

## 3. Privacy Classification Definition

Privacy Classification is the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.

Privacy Classification exists to protect knowledge from accidental exposure, inappropriate access, unsafe routing, unauthorized publication, uncontrolled synchronization, excessive indexing, improper export, unsafe backup behavior, unauthorized agent processing, inappropriate workflow handling, implementation leakage, or downstream misuse.

Privacy Classification SHALL be explicit when privacy affects:

- access;
- visibility;
- exposure;
- routing;
- review;
- redaction;
- publication;
- synchronization;
- indexing;
- search;
- summarization;
- embedding;
- export;
- backup;
- restoration;
- import;
- migration;
- agent access;
- workflow access;
- implementation access;
- downstream use;
- source references;
- provenance;
- relationships;
- lifecycle handling;
- authority handling;
- validation;
- compatibility;
- governance.

Privacy Classification MUST remain distinguishable from Object Identity.

A Knowledge Object remains the same Knowledge Object when its Privacy Classification changes unless a separate governed identity decision determines that the object itself has become meaningfully different.

Privacy Classification MUST remain distinguishable from Metadata as a whole.

Privacy Classification may be expressed through metadata, but privacy is not merely a metadata convenience.

Privacy Classification defines governed handling expectations where privacy affects access, visibility, exposure, publication, synchronization, indexing, export, backup, agent behavior, workflow behavior, implementation behavior, or downstream use.

Privacy Classification MUST remain distinguishable from Lifecycle State.

Lifecycle State describes the governed state of an entity.

Privacy Classification describes permitted access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling.

An approved entity may be confidential.

A draft entity may be public.

A rejected entity may still be sensitive.

An archived entity may still be restricted.

A quarantined entity may require limited access because of unresolved privacy risk.

Privacy Classification MUST remain distinguishable from Authority Level.

Authority Level describes governance weight, interpretive authority, review weight, trust boundary, or use-authority within a defined scope.

Privacy Classification describes access and handling boundaries.

A high-authority entity may be private.

A low-authority entity may be public.

A validated entity may still be non-exportable.

An approved entity may still be agent-restricted.

A source-supported entity may still be confidential.

Privacy Classification MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

Privacy Classification describes what handling is permitted.

A privacy classification may pass validation but still require restricted handling.

A record may fail validation because privacy classification is missing, unclear, contradictory, unsupported, overexposed, or incompatible with downstream use.

A validation result MUST NOT publish, expose, synchronize, index, export, back up, declassify, or grant access to a governed entity unless a governed workflow or specification explicitly defines that behavior.

Privacy Classification MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context.

Privacy Classification describes permitted handling.

Provenance may contain restricted information.

Privacy Classification SHOULD protect provenance where provenance reveals restricted source material, personal information, sensitive context, restricted workflows, agent activity, confidential reasoning, migration history, import context, export context, or review history.

Privacy Classification MUST remain distinguishable from Source Reference existence.

A Source Reference does not make a governed entity public.

A publicly available source does not automatically make derived knowledge public.

A private source does not automatically prevent all derived knowledge from being used, but the privacy implications MUST be reviewed where source privacy affects interpretation, exposure, publication, export, indexing, agent access, or downstream use.

Privacy Classification MUST remain distinguishable from relationship existence.

A relationship does not make a governed entity visible, publishable, exportable, indexable, agent-readable, workflow-readable, or implementation-readable by itself.

Relationship context may create additional privacy risk.

A relationship may reveal sensitive associations, dependencies, identities, evidence, decisions, source use, workflow behavior, agent involvement, or downstream implications.

Privacy Classification MUST remain distinguishable from access-control implementation.

Access-control systems may enforce privacy rules.

Privacy Classification defines the standard-level privacy meaning.

An implementation may use file permissions, database permissions, encryption, access roles, vault separation, folder visibility, search filters, sync controls, publication settings, backup policies, or agent permission settings to support Privacy Classification.

Those enforcement mechanisms do not define Privacy Classification by themselves.

Privacy Classification MUST NOT depend only on:

- folder location;
- filename;
- file extension;
- tag;
- color;
- icon;
- sort order;
- search result;
- graph position;
- backlink behavior;
- user-interface state;
- plugin field;
- database row;
- hidden application state;
- access-control configuration;
- synchronization setting;
- publication setting;
- backup setting;
- workflow memory;
- agent memory;
- implementation-specific status label;
- undocumented convention.

These signals MAY support usability, discovery, routing, display, restriction, validation, search, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit governed Privacy Classification where privacy affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Privacy Classification SHOULD be scoped.

A privacy classification SHOULD identify the context in which it applies.

A governed entity may be internal for one use, private for another use, non-exportable for migration, agent-restricted for automation, publishable after redaction, indexable for local search only, or backup-restricted for a particular environment.

Privacy Classification SHOULD be reviewable.

A future human, agent, workflow, validator, storage system, migration process, import process, export process, backup process, publication process, synchronization process, indexing system, or implementation SHOULD be able to determine what Privacy Classification applies, what the classification means, how it was assigned where applicable, whether review is required, whether redaction is required, whether access is permitted, whether publication is permitted, whether export is permitted, whether agent access is permitted, and whether downstream use is limited.

Privacy Classification SHOULD be portable.

A privacy classification SHOULD remain meaningful when an entity is renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, reindexed, summarized, translated, validated, processed by an agent, processed by a workflow, archived, restricted, repaired, or accessed through a different implementation.

Privacy Classification SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, indexing process, or publication process MUST NOT silently discard, collapse, rename, reinterpret, expose, replace, promote, demote, declassify, over-classify, or regenerate Privacy Classification in a way that causes privacy exposure, loss of meaning, broken provenance, authority ambiguity, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, synchronization error, backup exposure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Privacy Classification is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine what privacy handling applies to a governed entity, how that handling affects access and use, what provenance supports the classification where needed, whether review or redaction is required, whether authority or lifecycle handling is affected, and whether privacy meaning remains preserved across time and implementation replacement.

## 4. Privacy Classification Requirements

Privacy Classification Requirements define the minimum behavior required for Privacy Classification to be valid, interpretable, reviewable, portable, privacy-preserving, and governable under KS-0008.

A governed entity SHALL include or support Privacy Classification where privacy affects access, visibility, exposure, routing, review, redaction, publication, synchronization, indexing, search, summarization, embedding, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

A governed entity MAY include:

- a Knowledge Object;
- a Knowledge Record;
- Source Material;
- a Source Reference;
- a provenance record;
- a relationship;
- a metadata record;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Privacy Classification SHALL be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine how the entity may be accessed, exposed, routed, processed, published, synchronized, indexed, exported, backed up, restored, migrated, imported, or used downstream.

Privacy Classification MUST NOT depend only on hidden implementation behavior, storage location, folder placement, filename, tag, color, icon, user-interface state, workflow memory, agent memory, plugin behavior, database state, search ranking, graph position, backlink behavior, access-control settings, synchronization settings, publication settings, backup settings, or undocumented convention.

Those signals MAY support discovery, navigation, routing, display, validation, restriction, automation, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification when privacy affects governed handling or use.

A Privacy Classification SHOULD identify or support identification of:

- what entity the Privacy Classification applies to;
- what Privacy Classification applies;
- whether the classification is current or historical;
- what privacy scope applies;
- who or what assigned the classification where applicable;
- when the classification was assigned where applicable;
- what privacy review occurred where applicable;
- what provenance supports the classification where applicable;
- whether review is required;
- whether redaction is required;
- whether access is permitted;
- whether visibility is permitted;
- whether publication is permitted;
- whether synchronization is permitted;
- whether indexing is permitted;
- whether export is permitted;
- whether backup is permitted;
- whether restoration is permitted;
- whether import is permitted;
- whether migration is permitted;
- whether agent access is permitted;
- whether workflow access is permitted;
- whether implementation access is permitted;
- whether downstream use is limited;
- whether the classification affects relationships, Source References, provenance, lifecycle state, authority level, validation, compatibility, publication, export, migration, workflow behavior, agent behavior, implementation behavior, or governance.

Privacy Classification MUST remain distinguishable from Object Identity.

A Privacy Classification change MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when it moves from public to private, private to restricted, restricted to confidential, confidential to sensitive, exportable to non-exportable, agent-readable to agent-restricted, publishable to non-publishable, indexable to non-indexable, synchronized to non-synchronized, or any other governed privacy transition unless a separate governed identity decision determines that the object has become meaningfully different.

Privacy Classification MUST remain distinguishable from Lifecycle State.

A lifecycle transition MUST NOT weaken privacy requirements.

A governed entity MAY be approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending validation, or needs repair while still requiring private, confidential, sensitive, non-exportable, agent-restricted, workflow-restricted, implementation-restricted, or otherwise constrained privacy handling.

Privacy Classification MUST remain distinguishable from Authority Level.

Authority does not grant access by itself.

Approval does not grant publication by itself.

Validation does not grant export by itself.

Source authority does not grant agent access by itself.

A high-authority entity MAY remain private, confidential, sensitive, non-exportable, non-publishable, non-indexable, or agent-restricted.

A low-authority entity MAY still require strong privacy protection.

Privacy Classification MUST remain distinguishable from Validation State.

Validation MAY check Privacy Classification.

Validation MAY identify missing, unclear, conflicting, unsafe, overexposed, underprotected, or incompatible Privacy Classification.

Validation MUST NOT expose, publish, synchronize, index, export, back up, declassify, grant access to, or route a governed entity beyond its privacy boundary unless a governed workflow or specification explicitly permits that behavior.

Privacy Classification MUST remain distinguishable from Provenance.

A Privacy Classification SHOULD preserve provenance when privacy assignment, privacy review, privacy escalation, privacy reduction, redaction, publication, synchronization, indexing, export, backup, import, migration, agent access, workflow access, implementation access, or downstream use affects interpretation, governance, compatibility, validation, authority, lifecycle state, relationships, Source References, or future review.

Privacy Classification MUST preserve privacy boundaries for provenance itself.

Provenance SHOULD NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless access is permitted by the applicable privacy classification.

Privacy Classification MUST preserve relationship privacy.

A relationship MAY require equal or stronger privacy handling than the entities it connects.

A relationship SHOULD be reviewed for privacy risk when the relationship reveals sensitive association, identity, source use, dependency, decision logic, workflow activity, agent activity, provenance, authority, lifecycle state, validation state, or downstream-use context.

A relationship MUST NOT be exposed, published, indexed, synchronized, exported, backed up, or made agent-readable merely because the related entities are individually accessible.

Privacy Classification MUST preserve Source Reference and Source Material privacy.

Source Material MAY require a different Privacy Classification than the Knowledge Record derived from it.

A Knowledge Record MAY require a different Privacy Classification than its Source Material.

A Source Reference MAY expose restricted source context even when the referenced source is public.

A derived record MAY become more sensitive than the original source because of aggregation, interpretation, connection, summarization, extraction, transformation, classification, decision support, personal context, or downstream-use risk.

Privacy Classification SHALL take precedence over operational convenience when privacy and convenience conflict.

Search convenience MUST NOT override privacy.

Graph visibility MUST NOT override privacy.

Agent usefulness MUST NOT override privacy.

Workflow speed MUST NOT override privacy.

Publication convenience MUST NOT override privacy.

Export convenience MUST NOT override privacy.

Synchronization convenience MUST NOT override privacy.

Backup convenience MUST NOT override privacy.

Implementation convenience MUST NOT override privacy.

Privacy Classification SHOULD avoid unnecessary over-classification.

Over-classification occurs when a governed entity is assigned a more restrictive Privacy Classification than needed for its actual risk, source context, legal context, ethical context, governance context, workflow context, agent context, implementation context, or downstream-use context.

Over-classification may reduce usability, searchability, automation reliability, review efficiency, migration quality, publication readiness, or long-term maintainability.

Privacy Classification SHOULD avoid under-classification.

Under-classification occurs when a governed entity is assigned a less restrictive Privacy Classification than needed for its actual risk, source context, legal context, ethical context, governance context, workflow context, agent context, implementation context, or downstream-use context.

Under-classification may cause accidental exposure, unauthorized access, unsafe publication, uncontrolled synchronization, excessive indexing, improper export, unsafe backup behavior, inappropriate agent processing, implementation leakage, or downstream misuse.

Privacy Classification SHOULD support review.

A reviewer SHOULD be able to determine:

- what Privacy Classification applies;
- whether the classification is appropriate;
- whether privacy scope is clear;
- whether access is permitted;
- whether visibility is permitted;
- whether publication is permitted;
- whether synchronization is permitted;
- whether indexing is permitted;
- whether export is permitted;
- whether backup is permitted;
- whether agent access is permitted;
- whether workflow access is permitted;
- whether implementation access is permitted;
- whether redaction is required;
- whether provenance supports the classification where needed;
- whether relationships, Source References, lifecycle state, Authority Level, validation state, compatibility, import, export, migration, workflow behavior, agent behavior, implementation behavior, publication, synchronization, indexing, backup, or downstream use require additional review.

Privacy Classification SHOULD support validation.

A validator SHOULD be able to determine whether:

- Privacy Classification is present where required;
- Privacy Classification uses a governed value where a governed vocabulary exists;
- privacy scope is explicit where needed;
- Privacy Classification is distinguishable from Object Identity, Lifecycle State, Authority Level, Validation State, Provenance, Source References, relationships, workflow state, agent state, implementation state, access-control state, and storage state;
- Privacy Classification preserves relationship privacy;
- Privacy Classification preserves Source Reference and Source Material privacy;
- Privacy Classification preserves provenance privacy;
- Privacy Classification remains compatible with access, visibility, publication, synchronization, indexing, export, backup, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, and downstream use.

Privacy Classification SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, indexing process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, declassify, over-classify, under-classify, or regenerate Privacy Classification in a way that causes privacy exposure, loss of meaning, broken provenance, authority ambiguity, lifecycle ambiguity, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, synchronization error, backup exposure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Privacy Classification Requirements are successful when Privacy Classification remains explicit, scoped, distinguishable, reviewable, portable, privacy-preserving, validatable, and compatible across access, visibility, exposure, routing, review, redaction, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow activity, agent activity, validation, storage replacement, and implementation replacement.

## 5. Privacy Classification Categories

Privacy Classification Categories organize privacy-related handling by architectural purpose.

Privacy Classification Categories help humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations understand what kind of privacy handling applies, what role it serves, and how it should affect access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, and downstream use.

KS-0008 defines Privacy Classification Categories at the conceptual standard level.

KS-0008 does not define an exhaustive controlled vocabulary of exact privacy values.

A future privacy specification MAY define exact privacy values, allowed transitions, privacy inheritance rules, privacy conflict-resolution rules, access-control mappings, redaction rules, publication rules, synchronization rules, indexing rules, backup rules, export rules, agent-access rules, workflow-access rules, implementation-access rules, validation rules, import mappings, export mappings, migration mappings, and implementation profiles.

At minimum, The Brain Standard recognizes the following Privacy Classification Categories:

- public visibility categories;
- internal-use categories;
- private-access categories;
- restricted-access categories;
- confidential-handling categories;
- sensitive-information categories;
- personal-information categories;
- publication-restricted categories;
- export-restricted categories;
- synchronization and indexing restricted categories;
- backup and restoration restricted categories;
- agent-access categories;
- workflow-access categories;
- implementation and downstream-use categories;
- privacy category success criteria.

### 5.1 Public Visibility Categories

Public Visibility Categories describe governed entities that may be visible, exposed, published, indexed, exported, synchronized, backed up, or used downstream within a defined public or broadly accessible scope.

A Public Visibility Category MUST remain scoped.

Public visibility does not automatically mean:

- approved;
- high-authority;
- validated for every use;
- unrestricted for export;
- unrestricted for indexing;
- unrestricted for synchronization;
- unrestricted for backup;
- unrestricted for agent access;
- unrestricted for workflow access;
- unrestricted for implementation access;
- unrestricted for downstream use.

A public governed entity MAY still have restricted Source References, restricted provenance, restricted relationships, restricted validation results, restricted lifecycle history, restricted authority context, or restricted implementation context.

Where public knowledge depends on restricted supporting context, the public representation SHOULD preserve enough traceability for authorized review without exposing restricted information.

A Public Visibility Category MUST NOT override Lifecycle State, Authority Level, Validation State, Source Reference restrictions, provenance restrictions, relationship restrictions, compatibility limits, or governance requirements.

### 5.2 Internal-Use Categories

Internal-Use Categories describe governed entities intended for use within a defined internal scope but not necessarily for public release.

Internal use may apply to:

- personal internal use;
- project internal use;
- vault internal use;
- workflow internal use;
- implementation internal use;
- organization internal use where future multi-user support exists;
- another governed internal scope.

An Internal-Use Category SHOULD identify or support identification of the internal scope where scope affects access, visibility, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream use.

Internal knowledge MUST NOT be treated as public merely because it appears in:

- search results;
- graph views;
- dashboards;
- summaries;
- exports;
- backups;
- indexes;
- embeddings;
- synchronized copies;
- workflow queues;
- agent-readable contexts;
- implementation views.

Internal use describes handling scope.

Internal use does not define Authority Level, Lifecycle State, Validation State, Object Identity, source reliability, relationship meaning, or publication readiness.

### 5.3 Private-Access Categories

Private-Access Categories describe governed entities intended for limited access by a specific person, owner, role, workflow, agent, governed access group, implementation context, or authorized review process.

Private access SHOULD identify permitted access scope where scope affects handling.

Private knowledge MUST NOT be exposed through publication, broad export, unrestricted synchronization, shared indexes, unrestricted backups, search summaries, graph views, embeddings, workflow logs, agent output, implementation caches, or derived metadata unless a governed process explicitly permits that exposure within a defined scope.

A private governed entity MAY or MAY NOT contain personal information.

Private access describes handling expectations.

Personal information describes content or context involving a person.

A personal note may be private.

A private record may not be personal.

A private record may still be high-authority within an authorized scope.

A private record may still be valid while remaining non-public, non-exportable, non-indexable, or agent-restricted.

Private-access handling SHOULD be preserved during import, export, migration, backup, synchronization, indexing, validation, workflow activity, agent activity, and implementation replacement where privacy affects downstream handling.

### 5.4 Restricted-Access Categories

Restricted-Access Categories describe governed entities that require constrained access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream use because exposure may create material risk, ambiguity, governance concern, privacy concern, compatibility concern, source concern, or review concern.

Restricted access MAY apply when:

- privacy classification is unclear;
- source privacy is unresolved;
- provenance contains restricted information;
- relationships reveal restricted associations;
- validation has identified privacy risk;
- lifecycle state indicates quarantine, restriction, pending review, or needs repair;
- authority handling is limited to an authorized scope;
- export, publication, synchronization, indexing, backup, agent access, workflow access, implementation access, or downstream use requires review.

Restricted access SHOULD be conservative where classification details are incomplete.

A restricted governed entity MUST NOT be treated as public, exportable, publishable, searchable, synchronized, agent-readable, workflow-readable, implementation-visible, or broadly downstream-usable merely because it exists in a compliant environment.

Restriction MUST remain distinguishable from Lifecycle State.

A restricted lifecycle state may support restricted handling, but Restricted as a privacy category describes access and handling boundaries.

### 5.5 Confidential-Handling Categories

Confidential-Handling Categories describe governed entities whose exposure could create governance, personal, operational, security, legal, contractual, ethical, reputational, strategic, or other material risk.

Confidential handling SHOULD require explicit review before:

- publication;
- export;
- broad indexing;
- external synchronization;
- unrestricted backup;
- agent access;
- workflow routing;
- implementation exposure;
- relationship exposure;
- provenance exposure;
- source-reference exposure;
- validation output exposure;
- migration output exposure;
- downstream use.

Confidential knowledge MUST NOT be exposed merely to improve search, navigation, summarization, validation, linking, provenance traceability, authority assessment, publication, export, backup, indexing, synchronization, migration, automation, implementation convenience, or agent usefulness.

A Confidential-Handling Category SHOULD preserve enough traceability for authorized review without unnecessarily exposing confidential information.

Confidential handling does not make a governed entity invalid, low-authority, unapproved, unusable, or unreviewable.

Confidential handling means use is limited to the authorized scope.

### 5.6 Sensitive-Information Categories

Sensitive-Information Categories describe governed entities containing or revealing information that requires careful handling because exposure may create personal, operational, ethical, security, legal, reputational, financial, identity-related, relationship-related, decision-related, or downstream-use risk.

Sensitive information MAY include information about:

- identity;
- preferences;
- behavior;
- relationships;
- locations;
- communications;
- decisions;
- health;
- finances;
- credentials;
- security posture;
- personal context;
- confidential reasoning;
- restricted source material;
- restricted workflow activity;
- restricted agent activity;
- restricted implementation behavior;
- another sensitive context.

This list is descriptive and does not define a complete sensitive-information taxonomy.

Sensitive information SHOULD be handled conservatively where exposure risk is unclear.

Sensitive information MUST NOT be exposed merely because it improves personalization, search, summarization, relationship discovery, provenance review, validation, automation, publication, export, indexing, synchronization, backup, migration, implementation convenience, or agent usefulness.

Sensitive-Information Categories SHOULD support redaction, minimization, review, restricted access, restricted indexing, restricted synchronization, restricted backup, restricted agent access, restricted workflow handling, and downstream-use limits where applicable.

### 5.7 Personal-Information Categories

Personal-Information Categories describe governed entities that contain, identify, describe, infer, connect, summarize, classify, or reveal information about a person.

Personal information MAY be explicit or inferred.

Personal information MAY appear in:

- Knowledge Objects;
- Knowledge Records;
- Source Material;
- Source References;
- provenance;
- relationships;
- metadata;
- summaries;
- extracts;
- transformations;
- validation results;
- workflow outputs;
- agent outputs;
- indexes;
- embeddings;
- caches;
- backups;
- exports;
- migrations;
- implementation records.

A Personal-Information Category SHOULD preserve privacy boundaries where information identifies or could reasonably reveal a person, personal context, preference, behavior, relationship, communication, decision, location, credential, financial context, health context, or other personal context.

Personal information MUST NOT be made public, exported, synchronized, indexed, backed up outside the permitted scope, exposed to agents, exposed to workflows, exposed to implementations, or used downstream merely because it appears in a valid Knowledge Record.

Where personal information is used to improve agent behavior, workflow behavior, search, indexing, summarization, relationship discovery, or implementation behavior, the applicable Privacy Classification SHOULD remain explicit and reviewable.

### 5.8 Publication-Restricted Categories

Publication-Restricted Categories describe governed entities that may not be published, externally shared, broadly displayed, or exposed beyond their permitted privacy boundary without review or a governed publication process.

Publication restriction MAY apply even when a governed entity is:

- approved;
- high-authority;
- structurally valid;
- source-supported;
- internally visible;
- exportable for a limited scope;
- useful for agents;
- useful for workflows;
- useful for downstream decision support.

Publication permission MUST NOT be inferred from approval, Authority Level, Validation State, source reliability, relationship existence, workflow completion, agent confidence, implementation visibility, or storage location.

A publication-restricted entity SHOULD identify or support identification of:

- what publication restriction applies;
- what publication scope is blocked or limited;
- whether redaction is required;
- whether privacy review is required;
- whether Source References are publication-restricted;
- whether provenance is publication-restricted;
- whether relationships are publication-restricted;
- whether summaries, extracts, transformations, validation outputs, or agent outputs require separate review.

Publication-restricted handling MUST remain portable across implementation replacement.

### 5.9 Export-Restricted Categories

Export-Restricted Categories describe governed entities that may not be exported, copied out, transferred, shared, serialized, migrated outward, or included in external packages without review or a governed export process.

Export restriction MAY apply to:

- a full Knowledge Object;
- a Knowledge Record;
- Source Material;
- Source References;
- provenance;
- relationships;
- metadata;
- validation results;
- workflow outputs;
- agent outputs;
- indexes;
- embeddings;
- backups;
- exports;
- migrations;
- derived records.

Export permission MUST NOT be inferred from access permission, publication permission, approval, Authority Level, Validation State, source availability, workflow completion, agent confidence, implementation visibility, or file availability.

An export-restricted entity SHOULD identify or support identification of whether export is:

- prohibited;
- permitted only after review;
- permitted only after redaction;
- permitted only within an authorized scope;
- permitted only for backup;
- permitted only for migration;
- permitted only for validation;
- permitted only for a specific implementation profile;
- permitted only under a future governed specification.

Export-restricted handling SHOULD preserve enough context for authorized review without exposing restricted content in export logs, manifests, summaries, indexes, filenames, or metadata.

### 5.10 Synchronization and Indexing Restricted Categories

Synchronization and Indexing Restricted Categories describe governed entities that require limits on copying, mirroring, syncing, replication, caching, searchability, retrieval, ranking, embedding, summarization, vectorization, tagging, categorization, graph display, or other discoverability behavior.

Synchronization restriction MAY apply when a governed entity should remain local, vault-bound, device-bound, environment-bound, implementation-bound, or limited to an authorized repository.

Indexing restriction MAY apply when search, graph display, embeddings, summaries, previews, snippets, tags, cached content, relationship maps, or derived metadata could expose restricted knowledge.

A governed entity MUST NOT become synchronized or indexed merely because synchronization or indexing is technically available.

Synchronization and indexing permission MUST NOT be inferred from storage location, filename, folder placement, tag, implementation visibility, search ranking, graph position, backlink behavior, workflow completion, agent confidence, or validation success.

Where synchronization or indexing is restricted, derived artifacts SHOULD inherit applicable privacy limits where exposure could reveal protected information.

Derived artifacts MAY include:

- search indexes;
- embeddings;
- graph indexes;
- summaries;
- previews;
- snippets;
- tags;
- relationship maps;
- caches;
- logs;
- validation outputs;
- workflow outputs;
- agent outputs.

### 5.11 Backup and Restoration Restricted Categories

Backup and Restoration Restricted Categories describe governed entities that require constrained backup, restoration, archival, replication, disaster recovery, or continuity handling.

Backup restriction MAY apply when a governed entity should not be copied into unrestricted backup systems, shared backup repositories, external cloud storage, broad archives, unencrypted archives, public snapshots, unrestricted migration packages, or implementation caches.

Restoration restriction MAY apply when restoring a governed entity could expose, publish, synchronize, index, export, or route privacy-sensitive information beyond its permitted scope.

Backup permission MUST NOT be inferred from approval, Authority Level, Validation State, file existence, storage location, workflow completion, implementation defaults, or operational convenience.

A backup-restricted entity SHOULD identify or support identification of:

- whether backup is permitted;
- what backup scope is permitted;
- whether backup requires encryption or another future governed safeguard;
- whether backup metadata must be restricted;
- whether restoration requires review;
- whether backup logs may expose restricted information;
- whether Source References, provenance, relationships, indexes, embeddings, summaries, validation results, workflow outputs, or agent outputs require separate backup handling.

Backup and restoration behavior MUST preserve Privacy Classification where privacy affects future access, review, migration, compatibility, publication, synchronization, indexing, export, or downstream use.

### 5.12 Agent-Access Categories

Agent-Access Categories describe whether and how agents may read, classify, summarize, extract, transform, validate, route, link, modify, export, publish, migrate, synchronize, index, back up, or reason over a governed entity.

Agent access MUST remain scoped.

Agent-readable does not automatically mean:

- publishable;
- exportable;
- indexable;
- synchronizable;
- unrestricted for every agent;
- usable for model training;
- usable for downstream output;
- safe to summarize;
- safe to transform;
- safe to expose in logs;
- safe to include in prompts;
- safe to include in embeddings.

Agent-restricted entities MUST NOT be exposed to agents merely because agent processing would improve search, summarization, validation, linking, classification, workflow routing, automation, implementation convenience, or downstream usefulness.

An agent MAY propose Privacy Classification, identify privacy conflicts, recommend review, recommend redaction, or flag exposure risk.

An agent MUST NOT become an unreviewable authority for privacy assignment, privacy reduction, declassification, publication permission, export permission, synchronization permission, indexing permission, backup permission, workflow permission, implementation permission, or downstream-use permission where privacy affects governed handling.

Agent outputs derived from privacy-sensitive entities SHOULD inherit applicable privacy limits where output exposure may reveal restricted content, source context, relationships, provenance, lifecycle state, authority context, validation context, or downstream-use limits.

### 5.13 Workflow-Access Categories

Workflow-Access Categories describe whether and how workflows may route, review, validate, approve, reject, restrict, quarantine, redact, publish, synchronize, index, export, import, migrate, back up, restore, archive, repair, or otherwise process a governed entity.

Workflow access MUST remain scoped.

Workflow-readable does not automatically mean:

- approved;
- publishable;
- exportable;
- agent-readable;
- implementation-visible;
- unrestricted for every workflow;
- safe for logs;
- safe for derived outputs;
- safe for downstream use.

Workflow completion MUST NOT create, remove, weaken, expand, reinterpret, transfer, inherit, override, downgrade, upgrade, collapse, or resolve Privacy Classification unless a governed workflow specification explicitly defines that transition within a defined scope.

A workflow MAY support privacy review, privacy assignment, privacy escalation, privacy reduction, redaction, quarantine, validation, publication review, export review, synchronization review, indexing review, backup review, migration review, or downstream-use review.

Workflow outputs derived from privacy-sensitive entities SHOULD inherit applicable Privacy Classification, restriction, review requirements, redaction requirements, Source Reference limits, relationship limits, provenance limits, authority limits, validation limits, and downstream-use limits where output exposure may reveal protected information.

### 5.14 Implementation and Downstream-Use Categories

Implementation and Downstream-Use Categories describe whether and how a governed entity may be exposed, displayed, indexed, cached, synchronized, published, exported, backed up, routed, transformed, summarized, embedded, searched, linked, visualized, logged, or used by a specific implementation or later dependent process.

Implementation access MUST remain distinguishable from Privacy Classification.

An implementation may enforce privacy, but implementation visibility does not define privacy by itself.

A governed entity MUST NOT become public, exportable, publishable, searchable, synchronized, indexed, backed up, agent-readable, workflow-readable, or downstream-usable merely because an implementation can display, cache, search, export, sync, publish, back up, or process it.

Downstream use MUST remain scoped.

A governed entity may be usable for one downstream purpose but prohibited for another.

A governed entity may be:

- visible but not exportable;
- searchable but not publishable;
- readable by a workflow but not by an agent;
- approved but not public;
- high-authority but restricted;
- valid but non-exportable;
- backed up but not synchronized;
- indexed locally but not externally searchable;
- publishable only after redaction;
- migratable only with explicit privacy mapping.

Implementation and downstream-use handling SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations to determine what use is permitted and what review is required.

### 5.15 Privacy Classification Category Success

Privacy Classification Categories are successful when they help future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations determine what kind of privacy handling applies and how that handling affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, and downstream use.

Privacy Classification Categories are also successful when they remain:

- explicit;
- scoped;
- reviewable;
- portable;
- privacy-preserving;
- provenance-aware;
- compatible with Object Identity;
- compatible with metadata role boundaries;
- compatible with relationships;
- compatible with Source References;
- compatible with Lifecycle State;
- compatible with Authority Level;
- compatible with validation;
- compatible with import, export, and migration;
- implementation-independent.

Privacy Classification Categories MUST NOT become a hidden access-control system, exact permission model, exact field vocabulary, exact encryption requirement, exact folder layout, exact role model, exact user-interface convention, or implementation-specific behavior.

Those concerns belong to future specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, privacy vocabularies, access-control specifications, and operational guides.

## 6. Privacy Scope

Privacy Scope is the defined context in which a Privacy Classification applies.

Privacy Scope exists so that a governed entity is not treated as public, private, restricted, confidential, sensitive, exportable, publishable, agent-readable, workflow-readable, implementation-visible, synchronizable, indexable, backed up, migratable, or downstream-usable outside the context for which that classification was assigned, reviewed, or approved.

Privacy Scope SHALL be explicit where privacy handling differs by context.

Privacy Scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- Source Material;
- a Source Reference;
- a provenance record;
- a relationship;
- a metadata element;
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
- an implementation representation;
- another governed entity.

A Privacy Classification without clear scope may create privacy confusion.

Privacy confusion may occur when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, or implementations cannot determine:

- who may access the entity;
- what may be exposed;
- where the entity may be used;
- whether publication is permitted;
- whether export is permitted;
- whether synchronization is permitted;
- whether indexing is permitted;
- whether backup is permitted;
- whether restoration is permitted;
- whether agent access is permitted;
- whether workflow access is permitted;
- whether implementation access is permitted;
- whether downstream use is permitted;
- whether redaction is required;
- whether review is required;
- whether the scope is current or historical;
- whether scope changed during import, export, migration, synchronization, indexing, backup, restoration, publication, workflow activity, agent activity, or implementation replacement.

Privacy Scope SHOULD identify or support identification of:

- the governed entity the scope applies to;
- the Privacy Classification that applies;
- the permitted audience where applicable;
- the permitted environment where applicable;
- the permitted implementation where applicable;
- the permitted workflow where applicable;
- the permitted agent class or agent role where applicable;
- the permitted publication context where applicable;
- the permitted export context where applicable;
- the permitted synchronization context where applicable;
- the permitted indexing context where applicable;
- the permitted backup context where applicable;
- the permitted migration context where applicable;
- the permitted downstream-use context where applicable;
- the restricted contexts where applicable;
- the review process required where applicable;
- the redaction requirement where applicable;
- the provenance supporting the scope where applicable.

Privacy Scope MUST remain distinguishable from Object Identity.

Changing privacy scope MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when its permitted audience, access scope, publication scope, export scope, synchronization scope, indexing scope, backup scope, workflow scope, agent scope, implementation scope, or downstream-use scope changes unless a separate governed identity decision determines that the object has become meaningfully different.

Privacy Scope MUST remain distinguishable from Lifecycle State.

A lifecycle transition may affect whether privacy scope must be reviewed, preserved, restricted, quarantined, repaired, redacted, inherited, migrated, exported, published, synchronized, indexed, backed up, or applied downstream.

Lifecycle State does not define Privacy Scope by itself.

Privacy Scope MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Privacy Scope describes where Privacy Classification applies.

Authority Scope MAY be limited by Privacy Scope.

Privacy Scope MUST NOT silently broaden Authority Scope.

Authority Scope MUST NOT silently broaden Privacy Scope.

A governed entity may be authoritative in one privacy scope and non-usable in another.

A governed entity may be public in one representation and restricted in another.

A governed entity may be exportable in one migration scope and non-exportable in another.

A governed entity may be agent-readable in one workflow scope and agent-restricted in another.

Privacy Scope MUST remain distinguishable from implementation access-control configuration.

Access-control systems MAY enforce Privacy Scope.

Implementation settings MAY support Privacy Scope.

Storage layout MAY assist Privacy Scope.

Workflow routing MAY apply Privacy Scope.

Agent permissions MAY respect Privacy Scope.

None of those mechanisms define Privacy Scope by themselves unless their meaning is governed by an approved standard or specification.

Privacy Scope MUST NOT depend only on:

- folder location;
- filename;
- file extension;
- tag;
- color;
- icon;
- user-interface state;
- plugin field;
- database row;
- access-control setting;
- synchronization setting;
- publication setting;
- backup setting;
- workflow memory;
- agent memory;
- implementation-specific status label;
- undocumented convention.

These signals MAY support usability, enforcement, routing, discovery, restriction, validation, or implementation behavior.

They MUST NOT replace explicit governed Privacy Scope where scope affects access, visibility, exposure, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Privacy Scope SHOULD be conservative where scope is missing, ambiguous, unsupported, conflicting, inherited from uncertain context, or changed by import, export, migration, synchronization, indexing, backup, restoration, publication, workflow activity, agent activity, or implementation replacement.

Where Privacy Scope is unclear, privacy-sensitive knowledge SHOULD be treated as restricted until reviewed or corrected.

Privacy Scope SHOULD support inheritance only where a future governed privacy specification, workflow specification, implementation profile, or validation specification defines inheritance behavior.

Privacy Scope MUST NOT be silently inherited from folders, filenames, tags, relationships, Source References, provenance, lifecycle state, Authority Level, validation state, workflow state, agent state, implementation visibility, or access-control settings unless a governed process explicitly permits that behavior.

Privacy Scope SHOULD support review.

A reviewer SHOULD be able to determine:

- what scope applies;
- whether the scope is appropriate;
- whether the scope is current;
- whether the scope is historical;
- whether the scope was assigned manually, by workflow, by agent proposal, by import, by export, by migration, by validation, or by implementation behavior;
- whether scope expansion requires review;
- whether scope reduction requires review;
- whether redaction is required;
- whether Source References, provenance, relationships, lifecycle state, Authority Level, validation state, compatibility, workflow behavior, agent behavior, implementation behavior, publication, export, synchronization, indexing, backup, migration, or downstream use require additional review.

Privacy Scope SHOULD support validation.

A validator SHOULD be able to determine whether:

- scope is present where required;
- scope is compatible with the assigned Privacy Classification;
- scope is compatible with Source References;
- scope is compatible with provenance;
- scope is compatible with relationships;
- scope is compatible with Lifecycle State;
- scope is compatible with Authority Level;
- scope is compatible with validation expectations;
- scope is compatible with import, export, migration, publication, synchronization, indexing, backup, workflow behavior, agent behavior, implementation behavior, and downstream use.

Privacy Scope is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine where a Privacy Classification applies, where it does not apply, what review is required, what redaction is required, whether scope changed, and whether privacy meaning remains preserved across time and implementation replacement.

## 7. Privacy Assignment

Privacy Assignment is the act of assigning, proposing, confirming, revising, limiting, escalating, reducing, removing, or preserving Privacy Classification for a governed entity.

Privacy Assignment exists so that Privacy Classification does not emerge accidentally from storage location, folder placement, filename, tag, user-interface behavior, workflow memory, agent memory, implementation visibility, access-control settings, publication settings, synchronization settings, indexing settings, backup settings, or undocumented convention.

Privacy Assignment SHALL be explicit where Privacy Classification affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Privacy Assignment MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- Source Material;
- a Source Reference;
- a provenance record;
- a relationship;
- a metadata element;
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
- an implementation representation;
- another governed entity.

Privacy Assignment MAY be performed, proposed, supported, or preserved by:

- a human;
- a governed workflow;
- a validator;
- an import process;
- an export process;
- a migration process;
- a backup process;
- a restoration process;
- a synchronization process;
- an indexing process;
- an implementation;
- an agent where permitted;
- another governed process.

A human MAY assign, confirm, revise, escalate, reduce, remove, or preserve Privacy Classification where permitted by governance, workflow expectations, validation expectations, privacy expectations, implementation expectations, and future specifications.

A workflow MAY assign, propose, confirm, revise, escalate, reduce, remove, or preserve Privacy Classification only where a governed workflow process explicitly permits that behavior within a defined scope.

A validator MAY check, flag, reject, warn about, or recommend Privacy Classification handling, but validation MUST NOT assign, reduce, remove, declassify, publish, export, synchronize, index, back up, or expose a governed entity unless a governed workflow or specification explicitly permits that behavior within a defined scope.

An agent MAY propose Privacy Classification, flag privacy conflicts, identify exposure risk, recommend review, recommend escalation, recommend reduction, recommend redaction, or support validation.

An agent MUST NOT become an unreviewable authority for Privacy Assignment where privacy affects access, visibility, exposure, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Import, export, and migration processes MAY preserve or map Privacy Classification where permitted by governed process.

Import, export, and migration processes MUST NOT silently discard, weaken, broaden, collapse, reinterpret, declassify, over-classify, under-classify, or regenerate Privacy Classification in a way that causes privacy exposure, loss of meaning, broken provenance, authority ambiguity, lifecycle ambiguity, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, synchronization error, backup exposure, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Privacy Assignment SHOULD identify or support identification of:

- what entity the assignment applies to;
- what Privacy Classification was assigned;
- what Privacy Scope applies;
- who or what assigned the classification where applicable;
- when the classification was assigned where applicable;
- whether the assignment was manual, workflow-generated, agent-proposed, validator-supported, imported, exported, migrated, synchronized, indexed, backed up, restored, or implementation-supported;
- what provenance supports the assignment where applicable;
- what Source References support or constrain the assignment where applicable;
- what relationships affect the assignment where applicable;
- what Lifecycle State affects the assignment where applicable;
- what Authority Level affects the assignment where applicable;
- what Validation State affects the assignment where applicable;
- whether review is required;
- whether redaction is required;
- whether access is permitted;
- whether visibility is permitted;
- whether publication is permitted;
- whether synchronization is permitted;
- whether indexing is permitted;
- whether export is permitted;
- whether backup is permitted;
- whether restoration is permitted;
- whether import is permitted;
- whether migration is permitted;
- whether agent access is permitted;
- whether workflow access is permitted;
- whether implementation access is permitted;
- whether downstream use is limited.

Privacy Assignment MUST preserve Object Identity.

A Privacy Assignment MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Changing Privacy Classification is not an identity change unless a separate governed identity decision determines that the Knowledge Object has become meaningfully different.

Privacy Assignment MUST preserve metadata role boundaries.

Privacy Assignment may be expressed through metadata, but Privacy Assignment is not the same as all metadata.

Privacy Assignment MUST remain distinguishable from descriptive metadata, lifecycle metadata, authority metadata, validation metadata, provenance metadata, relationship metadata, source-reference metadata, workflow metadata, agent metadata, implementation metadata, storage metadata, and hidden application behavior.

Privacy Assignment MUST preserve relationship privacy.

Where a relationship creates privacy risk, Privacy Assignment SHOULD consider whether the relationship requires equal or stronger privacy handling than the related entities.

A Privacy Assignment for one entity MUST NOT automatically expose its relationships unless relationship privacy permits that exposure.

Privacy Assignment MUST preserve Source Reference and provenance privacy.

A Privacy Assignment SHOULD consider whether Source Material, Source References, extraction history, transformation history, attribution, review history, import provenance, export provenance, migration provenance, validation history, agent involvement, workflow involvement, or implementation context contain restricted information.

A Privacy Assignment for a Knowledge Record MUST NOT automatically expose its Source Material, Source References, provenance, relationships, or supporting context unless the applicable privacy scope permits that exposure.

Privacy Assignment MUST preserve Lifecycle State boundaries.

Approval does not automatically assign public privacy.

Rejection does not automatically remove privacy requirements.

Archival does not automatically make a governed entity safe for broad access.

Quarantine may indicate privacy risk, but quarantine does not replace Privacy Classification.

Needs Repair may indicate privacy metadata failure, but repair state does not define the corrected Privacy Classification.

Privacy Assignment MUST preserve Authority Level boundaries.

Authority does not assign Privacy Classification by itself.

A high-authority entity may remain private, confidential, sensitive, non-exportable, non-publishable, non-indexable, or agent-restricted.

A low-authority entity may still require strong privacy protection.

Authority review may inform Privacy Assignment, but it does not replace privacy review unless a governed privacy process explicitly defines that behavior within a defined scope.

Privacy Assignment SHOULD avoid unnecessary over-classification.

Privacy Assignment SHOULD avoid unsafe under-classification.

Where classification is unknown, ambiguous, unsupported, conflicting, inherited from uncertain context, or affected by unresolved source, relationship, provenance, lifecycle, authority, validation, compatibility, workflow, agent, implementation, import, export, migration, synchronization, indexing, backup, restoration, publication, or downstream-use concerns, privacy-sensitive knowledge SHOULD be handled conservatively until reviewed or corrected.

Privacy Assignment SHOULD be traceable when assignment affects access, visibility, exposure, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Privacy Assignment SHOULD support review.

A reviewer SHOULD be able to determine:

- what was assigned;
- why it was assigned where practical;
- who or what assigned it where applicable;
- when it was assigned where applicable;
- whether assignment was proposed or confirmed;
- whether assignment was human-created, workflow-generated, agent-proposed, validator-supported, imported, exported, migrated, synchronized, indexed, backed up, restored, or implementation-supported;
- whether the assignment is scoped;
- whether redaction is required;
- whether review is required;
- whether the assignment affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Validation State, compatibility, publication, synchronization, indexing, export, backup, import, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Privacy Assignment SHOULD support validation.

A validator SHOULD be able to determine whether:

- Privacy Classification is assigned where required;
- assignment scope is explicit where needed;
- assignment provenance exists where needed;
- assignment is compatible with Source References;
- assignment is compatible with provenance;
- assignment is compatible with relationships;
- assignment is compatible with Lifecycle State;
- assignment is compatible with Authority Level;
- assignment is compatible with validation expectations;
- assignment is compatible with import, export, migration, publication, synchronization, indexing, backup, workflow behavior, agent behavior, implementation behavior, and downstream use.

Privacy Assignment is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine what Privacy Classification was assigned, what scope applies, what provenance supports the assignment where needed, whether review or redaction is required, whether assignment changed, and whether privacy meaning remains preserved across time and implementation replacement.

## 8. Privacy Review

Privacy Review is the review process used to determine whether a Privacy Classification is appropriate, sufficient, current, traceable, compatible, and safe for access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, governance, and downstream use.

Privacy Review exists so that Privacy Classification does not become stale, ambiguous, unsafe, over-classified, under-classified, unsupported, or dependent on hidden implementation behavior.

Privacy Review SHALL be available where Privacy Classification affects governed handling or downstream use.

Privacy Review MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- Source Material;
- a Source Reference;
- a provenance record;
- a relationship;
- a metadata element;
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
- an implementation representation;
- another governed entity.

Privacy Review MAY be performed or supported by:

- a human reviewer;
- a governed workflow;
- a validator;
- an import process;
- an export process;
- a migration process;
- a backup process;
- a restoration process;
- a synchronization process;
- an indexing process;
- an implementation;
- an agent where permitted;
- another governed process.

A human reviewer MAY confirm, revise, escalate, reduce, reject, defer, preserve, or request repair of Privacy Classification where permitted by governance, workflow expectations, validation expectations, privacy expectations, implementation expectations, and future specifications.

A workflow MAY route, request, record, support, or execute Privacy Review only where a governed workflow process explicitly permits that behavior within a defined scope.

A validator MAY check whether Privacy Classification is present, scoped, supported, compatible, and distinguishable from other governed concepts.

A validator MUST NOT grant access, publish, export, synchronize, index, back up, declassify, reduce, remove, or weaken Privacy Classification unless a governed workflow or specification explicitly permits that behavior within a defined scope.

An agent MAY assist Privacy Review by identifying privacy-sensitive content, flagging conflicts, detecting missing classification, recommending redaction, identifying exposure risk, comparing privacy scope, or proposing review questions.

An agent MUST NOT become an unreviewable authority for Privacy Review where privacy affects access, visibility, exposure, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Privacy Review SHOULD determine whether:

- Privacy Classification is present where required;
- Privacy Classification is appropriate for the governed entity;
- Privacy Scope is clear;
- access is permitted;
- visibility is permitted;
- exposure is permitted;
- routing is permitted;
- publication is permitted;
- synchronization is permitted;
- indexing is permitted;
- export is permitted;
- backup is permitted;
- restoration is permitted;
- import is permitted;
- migration is permitted;
- agent access is permitted;
- workflow access is permitted;
- implementation access is permitted;
- downstream use is permitted;
- redaction is required;
- provenance supports the classification where needed;
- Source References affect privacy handling;
- relationships affect privacy handling;
- Lifecycle State affects privacy handling;
- Authority Level affects privacy handling;
- Validation State affects privacy handling;
- compatibility concerns affect privacy handling.

Privacy Review SHOULD determine whether classification is current.

A Privacy Classification MAY become outdated when:

- knowledge content changes;
- Source Material changes;
- Source References change;
- provenance changes;
- relationships change;
- Lifecycle State changes;
- Authority Level changes;
- validation results change;
- publication context changes;
- export context changes;
- synchronization context changes;
- indexing context changes;
- backup context changes;
- workflow context changes;
- agent context changes;
- implementation context changes;
- migration context changes;
- downstream-use context changes;
- governance changes;
- a future privacy specification changes.

Privacy Review SHOULD determine whether classification is over-classified.

A governed entity SHOULD NOT remain more restricted than necessary when lower restriction would preserve privacy boundaries, governance expectations, source constraints, relationship constraints, provenance constraints, lifecycle constraints, authority constraints, validation constraints, compatibility constraints, and downstream-use limits.

Privacy Review SHOULD determine whether classification is under-classified.

A governed entity MUST NOT remain less restricted than necessary where lower restriction would create privacy exposure, unauthorized access, unsafe publication, uncontrolled synchronization, excessive indexing, improper export, unsafe backup behavior, inappropriate agent processing, implementation leakage, or downstream misuse.

Privacy Review SHOULD determine whether redaction is required.

Redaction MAY be required when a governed entity may be used, published, exported, synchronized, indexed, backed up, migrated, exposed to agents, exposed to workflows, exposed to implementations, or used downstream only if restricted information is removed, masked, summarized, separated, transformed, or otherwise limited through a governed process.

Redaction MUST NOT silently change knowledge meaning, Object Identity, provenance, Source References, relationship meaning, Lifecycle State, Authority Level, Validation State, compatibility, or governance context.

Where redaction changes meaning, the change SHOULD be explicit, reviewable, provenance-preserving, and compatible with future repair or audit.

Privacy Review MUST preserve Object Identity.

A Privacy Review decision MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Privacy Review MUST preserve metadata role boundaries.

Privacy Review may evaluate privacy metadata, but Privacy Review is not the same as metadata validation, lifecycle review, authority review, relationship review, source-reference review, provenance review, implementation review, workflow review, or agent review.

Privacy Review MUST preserve relationship privacy.

A Privacy Review SHOULD consider whether relationships create exposure risk even when related entities appear safe individually.

A Privacy Review SHOULD consider whether relationship existence, relationship type, direction, context, provenance, lifecycle state, authority, validation state, source context, or downstream-use context requires additional privacy handling.

Privacy Review MUST preserve Source Reference and provenance privacy.

A Privacy Review SHOULD consider whether Source Material, Source References, extraction history, transformation history, attribution, creator identity, editor identity, review history, validation history, import provenance, export provenance, migration provenance, agent involvement, workflow involvement, or implementation context contains restricted information.

Privacy Review MUST preserve Lifecycle State boundaries.

A Privacy Review does not approve, reject, deprecate, supersede, archive, quarantine, repair, or restore a governed entity unless a governed lifecycle process explicitly defines that result within a defined scope.

Privacy Review MUST preserve Authority Level boundaries.

A Privacy Review does not make a governed entity authoritative, non-authoritative, high-authority, low-authority, approved, source-supported, publishable, exportable, or valid unless a governed authority, lifecycle, validation, publication, or workflow process explicitly defines that result within a defined scope.

Privacy Review SHOULD be traceable where privacy handling affects access, visibility, exposure, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Privacy Review SHOULD identify or support identification of:

- what entity was reviewed;
- what Privacy Classification was reviewed;
- what Privacy Scope was reviewed;
- who or what performed the review where applicable;
- when review occurred where applicable;
- what issue triggered review where applicable;
- what review result occurred;
- whether classification was confirmed;
- whether classification was escalated;
- whether classification was reduced;
- whether classification was rejected;
- whether classification requires repair;
- whether redaction is required;
- whether further review is required;
- what provenance supports the review where applicable;
- what Source References, relationships, lifecycle state, Authority Level, Validation State, compatibility, workflow behavior, agent behavior, implementation behavior, publication, synchronization, indexing, export, backup, import, migration, or downstream-use limits were considered.

Privacy Review SHOULD support validation.

A validator SHOULD be able to determine whether Privacy Review occurred where required, whether review scope is clear, whether review provenance exists where needed, whether review results are compatible with Privacy Classification, and whether review results preserve privacy boundaries.

Privacy Review is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine what privacy review occurred, what decision was made, what scope applies, what provenance supports the review where needed, whether redaction or repair is required, and whether privacy meaning remains preserved across time and implementation replacement.

## 9. Privacy and Access

Privacy and Access defines how Privacy Classification affects the ability to read, modify, route, expose, publish, copy, synchronize, index, export, back up, restore, migrate, process, or otherwise interact with a governed entity.

Access exists so that humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can interact with knowledge only within permitted privacy boundaries.

Access SHALL be governed where privacy affects handling or downstream use.

Access MAY apply to:

- human reading;
- human editing;
- human review;
- agent reading;
- agent summarization;
- agent extraction;
- agent classification;
- agent validation;
- agent transformation;
- workflow routing;
- workflow review;
- workflow approval;
- workflow rejection;
- workflow publication;
- workflow export;
- workflow synchronization;
- workflow indexing;
- workflow backup;
- implementation display;
- implementation search;
- implementation indexing;
- implementation caching;
- implementation synchronization;
- implementation publication;
- implementation export;
- implementation backup;
- migration;
- restoration;
- downstream use.

Access MUST be scoped.

A governed entity may be accessible for one purpose but not another.

A governed entity may be:

- readable but not editable;
- editable but not publishable;
- reviewable but not exportable;
- visible but not fully readable;
- searchable but not previewable;
- indexable locally but not externally indexable;
- synchronizable locally but not externally synchronizable;
- backed up in one environment but not another;
- readable by a workflow but not by an agent;
- readable by one agent role but not another;
- usable for validation but not publication;
- usable for migration but not downstream publication.

Access permission MUST NOT be inferred from:

- file existence;
- storage location;
- folder placement;
- filename;
- file extension;
- tag;
- icon;
- color;
- search result;
- graph position;
- backlink behavior;
- user-interface visibility;
- implementation visibility;
- database presence;
- access-control setting alone;
- synchronization setting alone;
- publication setting alone;
- backup setting alone;
- workflow completion;
- agent confidence;
- validation success;
- Authority Level;
- Lifecycle State;
- source availability;
- relationship existence;
- undocumented convention.

These signals MAY support access enforcement, routing, display, validation, discovery, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where access affects governed handling or downstream use.

Privacy Classification SHOULD determine whether access is permitted, restricted, conditional, review-required, redaction-required, prohibited, scoped, temporary, historical, or governed by another future access condition.

Access MUST remain distinguishable from Visibility.

Visibility describes whether an entity is discoverable, displayed, indexed, searched, listed, previewed, linked, surfaced, summarized, synchronized, published, or exposed.

Access describes whether interaction with the entity is permitted.

A governed entity may be visible but not accessible.

A governed entity may be accessible to an authorized process but not broadly visible.

A governed entity may be visible as a redacted reference while restricted content remains inaccessible.

A governed entity may be indexed for authorized retrieval but not visible in unrestricted search.

Access MUST remain distinguishable from Authority Level.

Authority does not grant access by itself.

A high-authority entity may be inaccessible outside its privacy scope.

A low-authority entity may be accessible within an authorized scope.

An approved entity may still be access-restricted.

A source-supported entity may still be inaccessible to agents.

Access MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect access handling, but lifecycle status does not define access permission by itself.

A draft entity may be accessible to an author but not to an agent.

An approved entity may be private.

An archived entity may require restricted access.

A rejected entity may still require privacy protection.

A quarantined entity may require highly limited access until review or repair occurs.

Access MUST remain distinguishable from Validation State.

Validation may check whether access rules are represented or enforced.

Validation does not grant access by itself.

A valid entity may still be inaccessible.

An invalid entity may still require restricted access.

A validation result MUST NOT expose, publish, export, synchronize, index, back up, or grant access to a governed entity unless a governed workflow or specification explicitly permits that behavior within a defined scope.

Access MUST preserve Source Reference and provenance privacy.

Access to a Knowledge Record does not automatically grant access to its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence.

Access to Source Material does not automatically grant access to every derived Knowledge Record.

Access to provenance does not automatically grant access to restricted source content, restricted user context, restricted workflow context, restricted agent context, or restricted implementation context.

Access MUST preserve relationship privacy.

Access to one governed entity does not automatically grant access to its relationships.

Access to a relationship does not automatically grant access to all connected entities.

Access to connected entities does not automatically grant access to the relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A relationship MAY reveal restricted context even when each related entity appears safe in isolation.

Access SHOULD support least exposure.

Least exposure means that a compliant process SHOULD expose only the minimum knowledge, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, implementation context, or downstream-use context required for the permitted purpose.

Least exposure SHOULD NOT break reviewability, provenance preservation, validation, compatibility, governance, or future repair where those are required.

Access SHOULD support redaction where appropriate.

A governed entity MAY be partially accessible where a redacted, summarized, transformed, or limited representation can satisfy the permitted purpose without exposing restricted information.

A redacted representation MUST remain distinguishable from the unredacted governed entity.

A redacted representation SHOULD preserve enough context for authorized review without exposing restricted information.

Access SHOULD support review.

A reviewer SHOULD be able to determine:

- who or what may access the governed entity where applicable;
- what kind of access is permitted;
- what access scope applies;
- whether access is current or historical;
- whether access is temporary or persistent;
- whether access requires review;
- whether access requires redaction;
- whether access is limited by Source References;
- whether access is limited by provenance;
- whether access is limited by relationships;
- whether access is limited by Lifecycle State;
- whether access is limited by Authority Level;
- whether access is limited by Validation State;
- whether access is limited by compatibility;
- whether access is limited by publication, synchronization, indexing, export, backup, import, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Access SHOULD support validation.

A validator SHOULD be able to determine whether access rules are explicit where required, whether access scope is compatible with Privacy Classification, whether access handling preserves Source References and provenance, whether access handling preserves relationship privacy, and whether access handling remains compatible across import, export, migration, backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, and implementation replacement.

Access is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether access is permitted, what scope applies, what limits exist, whether redaction is required, whether access changed, and whether privacy meaning remains preserved across time and implementation replacement.

## 10. Privacy and Visibility

Privacy and Visibility defines how Privacy Classification affects discovery, display, search, listing, preview, linking, surfacing, summarization, indexing, graph display, synchronization, publication, caching, and implementation presentation of a governed entity.

Visibility exists so that a governed entity is not exposed merely because a system, interface, search index, graph view, agent, workflow, validator, storage system, synchronization process, backup process, publication process, or implementation can surface it.

Visibility SHALL be governed where visibility affects privacy handling or downstream use.

Visibility MAY include:

- file listing;
- title display;
- metadata display;
- preview display;
- snippet display;
- search result display;
- graph display;
- backlink display;
- dashboard display;
- relationship map display;
- index inclusion;
- embedding inclusion;
- summary inclusion;
- tag display;
- category display;
- source-reference display;
- provenance display;
- validation-result display;
- lifecycle-state display;
- authority-level display;
- workflow-queue display;
- agent-context display;
- implementation-cache display;
- synchronized-copy display;
- publication display;
- export-manifest display;
- backup-manifest display;
- migration-report display.

Visibility MUST be scoped.

A governed entity may be visible in one context but hidden, redacted, summarized, minimized, masked, or unavailable in another.

A governed entity may be:

- visible to an owner but hidden from agents;
- visible to a workflow but hidden from publication;
- visible in local search but hidden from external search;
- visible as a title but not as content;
- visible as a redacted summary but not as full text;
- visible as a reference but not as Source Material;
- visible in an audit log but not in a graph view;
- visible in a migration report but not in an export package;
- visible in a backup manifest but not restorable without review;
- visible in an implementation but not publishable.

Visibility MUST NOT be inferred from:

- file existence;
- storage location;
- folder placement;
- filename;
- file extension;
- tag;
- icon;
- color;
- search result;
- graph position;
- backlink behavior;
- user-interface display;
- implementation visibility;
- database presence;
- access-control setting alone;
- synchronization setting alone;
- publication setting alone;
- backup setting alone;
- workflow completion;
- agent confidence;
- validation success;
- Authority Level;
- Lifecycle State;
- source availability;
- relationship existence;
- undocumented convention.

These signals MAY support display, discovery, routing, validation, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where visibility affects governed handling or downstream use.

Visibility MUST remain distinguishable from Access.

Visibility describes whether a governed entity or part of its context is discoverable, displayed, indexed, listed, previewed, surfaced, summarized, synchronized, published, cached, or exposed.

Access describes whether interaction with the governed entity is permitted.

A governed entity may be visible but not accessible.

A governed entity may be accessible to an authorized reviewer but not broadly visible.

A governed entity may be visible only as a redacted title, restricted reference, placeholder, access-denied notice, audit entry, or review-needed signal.

Visibility MUST remain distinguishable from Publication.

Publication exposes a governed entity beyond its prior privacy boundary.

Visibility may occur inside an authorized local, internal, workflow, agent, implementation, validation, audit, or migration context without creating publication.

A visible entity is not automatically publishable.

A published entity may still carry privacy limits, provenance limits, relationship limits, source-reference limits, export limits, indexing limits, synchronization limits, backup limits, agent-use limits, workflow-use limits, implementation-use limits, or downstream-use limits.

Visibility MUST remain distinguishable from Indexing.

Indexing may create visibility, but indexing and visibility are not the same concept.

A governed entity may be indexed for authorized retrieval without being broadly visible.

A governed entity may be visible in a restricted interface without being indexed.

An index may expose restricted information through titles, snippets, embeddings, tags, relationship maps, cached content, ranking signals, or summaries.

Visibility review SHOULD consider indexing artifacts where indexing could reveal restricted information.

Visibility MUST remain distinguishable from Authority Level.

Authority does not create visibility permission by itself.

A high-authority entity may be hidden outside its privacy scope.

A low-authority entity may be visible within an authorized scope.

An approved entity may still be hidden, redacted, restricted, or non-public.

Visibility MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether visibility should be limited, reviewed, restricted, quarantined, repaired, archived, restored, or published.

Lifecycle State does not define visibility permission by itself.

A draft entity may be visible to an author.

An approved entity may be hidden from publication.

A rejected entity may remain visible only for historical review.

An archived entity may be visible only in an authorized archive context.

A quarantined entity may be hidden from normal discovery.

Visibility MUST preserve Source Reference and provenance privacy.

Displaying a Knowledge Record MUST NOT automatically display its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence.

Displaying provenance MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless the applicable Privacy Classification permits that exposure.

Visibility MUST preserve relationship privacy.

Displaying a governed entity MUST NOT automatically display its relationships.

Displaying a relationship MUST NOT automatically display all connected entities.

Displaying connected entities MUST NOT automatically display relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A relationship may reveal restricted association, dependency, identity, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Visibility SHOULD support minimization.

Visibility minimization means that a compliant process SHOULD display only the minimum title, label, placeholder, summary, metadata, Source Reference, provenance, relationship, validation result, lifecycle state, authority context, workflow context, agent context, implementation context, or downstream-use context required for the permitted purpose.

Visibility minimization SHOULD NOT break reviewability, provenance preservation, validation, compatibility, governance, or future repair where those are required.

Visibility SHOULD support redaction.

A governed entity MAY be visible through a redacted, summarized, masked, placeholder, or limited representation where full visibility would expose restricted information.

A redacted visible representation MUST remain distinguishable from the full governed entity.

A redacted visible representation SHOULD preserve enough context for authorized review without exposing restricted information.

Visibility SHOULD support review.

A reviewer SHOULD be able to determine:

- whether the governed entity may be visible;
- what visibility scope applies;
- what visible representation is permitted;
- whether full visibility is permitted;
- whether partial visibility is permitted;
- whether redaction is required;
- whether visibility is current or historical;
- whether visibility is temporary or persistent;
- whether visibility requires review;
- whether visibility is limited by Source References;
- whether visibility is limited by provenance;
- whether visibility is limited by relationships;
- whether visibility is limited by Lifecycle State;
- whether visibility is limited by Authority Level;
- whether visibility is limited by Validation State;
- whether visibility is limited by compatibility;
- whether visibility is limited by publication, synchronization, indexing, export, backup, import, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Visibility SHOULD support validation.

A validator SHOULD be able to determine whether visibility rules are explicit where required, whether visibility scope is compatible with Privacy Classification, whether visibility handling preserves Source References and provenance, whether visibility handling preserves relationship privacy, and whether visibility handling remains compatible across import, export, migration, backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, and implementation replacement.

Visibility is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether visibility is permitted, what visible representation is permitted, what scope applies, what limits exist, whether redaction is required, whether visibility changed, and whether privacy meaning remains preserved across time and implementation replacement.

## 11. Privacy and Publication

Privacy and Publication defines how Privacy Classification affects making a governed entity available beyond its prior privacy boundary.

Publication exists so that a governed entity is not exposed to a broader audience, environment, implementation, workflow, agent system, export package, synchronization target, index, archive, public interface, or downstream-use context merely because it is approved, visible, accessible, validated, source-supported, high-authority, indexed, synchronized, backed up, or technically publishable.

Publication SHALL be governed where privacy affects exposure, access, visibility, export, synchronization, indexing, backup, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Publication MAY include:

- public release;
- external sharing;
- broad internal sharing;
- web publishing;
- report publishing;
- documentation publishing;
- dashboard publishing;
- reference implementation display;
- export package release;
- shared repository release;
- synchronization to a broader environment;
- indexing into a broader search system;
- inclusion in a public or shared archive;
- inclusion in a model-readable context;
- inclusion in agent-readable context;
- inclusion in workflow-readable context;
- inclusion in downstream decision-support material;
- another governed publication context.

Publication MUST be scoped.

A governed entity may be publishable in one context but not another.

A governed entity may be:

- publishable internally but not externally;
- publishable after redaction but not in full;
- publishable as a summary but not as Source Material;
- publishable as a citation but not as provenance;
- publishable as a public Knowledge Record but not as supporting evidence;
- publishable in a governed report but not in an unrestricted export;
- publishable to humans but not to agents;
- publishable to a workflow but not to a public implementation;
- publishable only after privacy review;
- publishable only under a future governed specification.

Publication permission MUST NOT be inferred from:

- approval;
- Authority Level;
- Validation State;
- Lifecycle State;
- source reliability;
- source authority;
- source availability;
- relationship existence;
- provenance existence;
- access permission;
- visibility permission;
- search visibility;
- graph visibility;
- implementation visibility;
- file existence;
- storage location;
- folder placement;
- filename;
- tag;
- workflow completion;
- agent confidence;
- export success;
- synchronization success;
- indexing success;
- backup success;
- undocumented convention.

These signals MAY support publication review, routing, validation, display, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where publication affects governed handling or downstream use.

Publication MUST remain distinguishable from Access.

Access may permit a governed entity to be read, modified, reviewed, processed, or routed within a defined scope.

Publication makes the governed entity available beyond its prior privacy boundary.

A governed entity may be accessible to an authorized reviewer but not publishable.

A governed entity may be accessible to a workflow but not publishable outside that workflow.

A governed entity may be accessible to an agent but not publishable in agent output.

Publication MUST remain distinguishable from Visibility.

Visibility may expose a governed entity within a permitted interface, search result, graph, index, workflow queue, audit log, migration report, or implementation view.

Publication expands availability beyond the prior privacy boundary.

A visible entity is not automatically publishable.

A redacted visible representation is not automatically publishable in full.

Publication MUST remain distinguishable from Export.

Export produces a governed entity or representation for use elsewhere.

Publication makes a governed entity available to a broader audience, environment, interface, or downstream-use context.

A governed entity may be exportable for backup but not publishable.

A governed entity may be publishable as a redacted report but not exportable as source material.

A governed entity may be exportable to a governed archive but not publishable to users.

Publication MUST remain distinguishable from Synchronization.

Synchronization copies, mirrors, replicates, caches, or transmits a governed entity across environments.

Publication exposes a governed entity beyond its prior privacy boundary.

Synchronization may create publication risk if a synchronized target has broader access, visibility, indexing, backup, implementation exposure, workflow exposure, agent exposure, or downstream-use scope.

Publication review SHOULD consider synchronization behavior where synchronization could broaden exposure.

Publication MUST remain distinguishable from Indexing.

Indexing may make a governed entity searchable, retrievable, embedded, cached, summarized, ranked, categorized, or discoverable.

Publication may use indexes, but indexing alone does not define publication permission.

An index may expose restricted titles, snippets, embeddings, summaries, tags, cached content, relationship maps, source references, provenance, validation results, lifecycle context, authority context, or implementation context.

Publication review SHOULD consider indexing artifacts where indexed material may become visible outside the permitted privacy scope.

Publication MUST preserve Source Reference and provenance privacy.

Publishing a Knowledge Record MUST NOT automatically publish its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence.

Publishing a citation MUST NOT expose restricted source context unless the applicable Privacy Classification permits that exposure.

Publishing provenance MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless the applicable Privacy Classification permits that exposure.

Publication MUST preserve relationship privacy.

Publishing a governed entity MUST NOT automatically publish its relationships.

Publishing a relationship MUST NOT automatically publish all connected entities.

Publishing connected entities MUST NOT automatically publish relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A relationship may reveal restricted association, dependency, identity, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Publication MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity publishable.

A draft entity may be publishable only as a draft if the applicable privacy and lifecycle scope permits it.

A rejected entity may require restricted historical access and may not be publishable.

A superseded entity may be publishable for historical context only where governed.

An archived entity may remain non-public.

A quarantined entity MUST NOT be published unless a governed process explicitly permits publication within a defined scope.

Publication MUST preserve Authority Level boundaries.

Authority does not grant publication permission by itself.

A high-authority entity may be confidential, private, sensitive, non-exportable, non-indexable, non-synchronizable, or non-publishable.

A low-authority entity may be public.

Publication of high-authority content SHOULD preserve authority context where omission would create misleading interpretation.

Publication of low-authority content SHOULD preserve authority limits where omission would create misleading reliance.

Publication SHOULD support redaction.

A governed entity MAY be published through a redacted, summarized, masked, transformed, or limited representation where full publication would expose restricted information.

A redacted published representation MUST remain distinguishable from the unredacted governed entity.

A redacted published representation SHOULD preserve enough context for authorized review without exposing restricted information.

Publication SHOULD support minimization.

Publication minimization means that a compliant process SHOULD publish only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, implementation context, or downstream-use context required for the permitted publication purpose.

Publication minimization SHOULD NOT break reviewability, provenance preservation, validation, compatibility, governance, or future repair where those are required.

Publication SHOULD support review.

A reviewer SHOULD be able to determine:

- whether publication is permitted;
- what publication scope applies;
- what publication audience applies;
- what representation may be published;
- whether full publication is permitted;
- whether partial publication is permitted;
- whether redaction is required;
- whether publication is current or historical;
- whether publication is temporary or persistent;
- whether publication requires review;
- whether publication is limited by Source References;
- whether publication is limited by provenance;
- whether publication is limited by relationships;
- whether publication is limited by Lifecycle State;
- whether publication is limited by Authority Level;
- whether publication is limited by Validation State;
- whether publication is limited by compatibility;
- whether publication is limited by synchronization, indexing, export, backup, import, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Publication SHOULD support validation.

A validator SHOULD be able to determine whether publication rules are explicit where required, whether publication scope is compatible with Privacy Classification, whether publication handling preserves Source References and provenance, whether publication handling preserves relationship privacy, and whether publication handling remains compatible across import, export, migration, backup, restoration, synchronization, indexing, workflow activity, agent activity, implementation replacement, and downstream use.

Publication is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether publication is permitted, what published representation is permitted, what scope applies, what limits exist, whether redaction is required, whether publication changed, and whether privacy meaning remains preserved across time and implementation replacement.

## 12. Privacy and Synchronization

Privacy and Synchronization defines how Privacy Classification affects copying, mirroring, syncing, replicating, caching, transmitting, or otherwise reproducing a governed entity across devices, repositories, vaults, services, tools, implementations, environments, workflows, agents, indexes, backups, or downstream-use contexts.

Synchronization exists so that a governed entity is not copied into a broader, less protected, less governed, incompatible, unreviewed, external, public, agent-readable, workflow-readable, implementation-visible, indexable, exportable, or downstream-usable environment merely because synchronization is technically available or operationally convenient.

Synchronization SHALL be governed where privacy affects access, visibility, exposure, publication, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Synchronization MAY include:

- local device synchronization;
- vault synchronization;
- repository synchronization;
- cloud synchronization;
- external service synchronization;
- implementation synchronization;
- workflow synchronization;
- agent-context synchronization;
- index synchronization;
- cache synchronization;
- backup synchronization;
- archive synchronization;
- migration synchronization;
- publication synchronization;
- export synchronization;
- cross-environment replication;
- downstream-use replication;
- another governed synchronization context.

Synchronization MUST be scoped.

A governed entity may be synchronizable in one context but not another.

A governed entity may be:

- synchronizable locally but not externally;
- synchronizable to a private device but not to a shared service;
- synchronizable to a governed vault but not to an unrestricted repository;
- synchronizable after redaction but not in full;
- synchronizable as metadata but not as content;
- synchronizable as a Knowledge Record but not as Source Material;
- synchronizable for backup but not for publication;
- synchronizable for migration but not for indexing;
- synchronizable for a workflow but not for agents;
- synchronizable only under a future governed specification.

Synchronization permission MUST NOT be inferred from:

- file existence;
- storage location;
- folder placement;
- filename;
- file extension;
- tag;
- icon;
- color;
- user-interface visibility;
- implementation visibility;
- access-control setting alone;
- publication setting alone;
- backup setting alone;
- index inclusion;
- workflow completion;
- agent confidence;
- validation success;
- approval;
- Authority Level;
- Lifecycle State;
- source availability;
- relationship existence;
- undocumented convention.

These signals MAY support synchronization enforcement, routing, display, validation, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where synchronization affects governed handling or downstream use.

Synchronization MUST remain distinguishable from Access.

Access permits interaction with a governed entity within a defined scope.

Synchronization creates or updates copies, replicas, caches, mirrors, or transmitted representations.

A governed entity may be accessible locally but not synchronizable externally.

A governed entity may be accessible to a workflow but not synchronizable into workflow logs.

A governed entity may be accessible to an agent but not synchronizable into agent memory, prompts, embeddings, caches, or outputs.

Synchronization MUST remain distinguishable from Visibility.

Visibility describes discovery, display, search, listing, preview, linking, surfacing, summarization, indexing, graph display, caching, or implementation presentation.

Synchronization may create visibility if the synchronized environment exposes, indexes, displays, caches, publishes, exports, backs up, or routes the synchronized entity.

A synchronized entity is not automatically safe to display, index, publish, export, back up, or use downstream.

Synchronization MUST remain distinguishable from Publication.

Synchronization copies or transmits a governed entity across environments.

Publication exposes a governed entity beyond its prior privacy boundary.

Synchronization may become publication when the target environment broadens access, visibility, indexing, workflow access, agent access, implementation access, export, backup, or downstream use.

Synchronization review SHOULD determine whether synchronization creates publication risk.

Synchronization MUST remain distinguishable from Backup.

Backup preserves a copy for restoration, continuity, audit, migration, disaster recovery, or long-term preservation.

Synchronization keeps environments aligned, replicated, mirrored, cached, or transmitted.

A synchronized copy is not automatically a governed backup.

A backup copy is not automatically synchronizable.

Synchronization MUST preserve Source Reference and provenance privacy.

Synchronizing a Knowledge Record MUST NOT automatically synchronize its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that behavior.

Synchronizing provenance MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Synchronization MUST preserve relationship privacy.

Synchronizing a governed entity MUST NOT automatically synchronize its relationships.

Synchronizing a relationship MUST NOT automatically synchronize all connected entities.

Synchronizing connected entities MUST NOT automatically synchronize relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A synchronized relationship may reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Synchronization MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity synchronizable.

A draft entity may be synchronizable only within an authorized drafting scope.

A rejected entity may remain restricted from synchronization.

An archived entity may be synchronizable only within authorized archival or restoration scope.

A quarantined entity MUST NOT be synchronized into normal-use environments unless a governed process explicitly permits that behavior within a defined scope.

Synchronization MUST preserve Authority Level boundaries.

Authority does not grant synchronization permission by itself.

A high-authority entity may be non-synchronizable outside its privacy scope.

A low-authority entity may be synchronizable within an authorized scope.

Synchronizing authority context SHOULD preserve authority limits where omission would create misleading interpretation or downstream misuse.

Synchronization SHOULD support redaction and minimization.

A governed entity MAY be synchronized through a redacted, summarized, masked, transformed, metadata-only, placeholder, or limited representation where full synchronization would expose restricted information.

A redacted synchronized representation MUST remain distinguishable from the full governed entity.

Synchronization minimization means that a compliant process SHOULD synchronize only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, implementation context, or downstream-use context required for the permitted synchronization purpose.

Synchronization SHOULD support inheritance only where a future governed privacy specification, synchronization specification, workflow specification, implementation profile, or validation specification defines inheritance behavior.

Synchronization MUST NOT silently inherit privacy permission from folder placement, filename, tag, relationship, Source Reference, provenance, lifecycle state, Authority Level, validation state, workflow state, agent state, implementation visibility, access-control settings, or prior synchronization success unless a governed process explicitly permits that behavior.

Synchronization SHOULD support review.

A reviewer SHOULD be able to determine:

- whether synchronization is permitted;
- what synchronization scope applies;
- what source environment applies;
- what target environment applies;
- what synchronized representation is permitted;
- whether full synchronization is permitted;
- whether partial synchronization is permitted;
- whether redaction is required;
- whether synchronization is current or historical;
- whether synchronization is temporary or persistent;
- whether synchronization requires review;
- whether synchronization is limited by Source References;
- whether synchronization is limited by provenance;
- whether synchronization is limited by relationships;
- whether synchronization is limited by Lifecycle State;
- whether synchronization is limited by Authority Level;
- whether synchronization is limited by Validation State;
- whether synchronization is limited by compatibility;
- whether synchronization is limited by access, visibility, publication, indexing, export, backup, import, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Synchronization SHOULD support validation.

A validator SHOULD be able to determine whether synchronization rules are explicit where required, whether synchronization scope is compatible with Privacy Classification, whether synchronization handling preserves Source References and provenance, whether synchronization handling preserves relationship privacy, and whether synchronization handling remains compatible across import, export, migration, backup, restoration, indexing, publication, workflow activity, agent activity, implementation replacement, and downstream use.

Synchronization is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether synchronization is permitted, what synchronized representation is permitted, what source and target scopes apply, what limits exist, whether redaction is required, whether synchronization changed, and whether privacy meaning remains preserved across time and implementation replacement.

## 13. Privacy and Indexing

Privacy and Indexing defines how Privacy Classification affects making a governed entity searchable, retrievable, ranked, embedded, summarized, vectorized, cached, tagged, categorized, graph-visible, relationship-discoverable, or otherwise discoverable through an index, search system, graph system, embedding system, retrieval system, agent context, workflow context, implementation cache, or downstream-use process.

Indexing exists so that a governed entity is not made discoverable, searchable, inferable, retrievable, summarized, embedded, cached, ranked, or exposed merely because indexing improves usability, search, automation, validation, relationship discovery, publication, synchronization, export, backup, migration, implementation behavior, workflow behavior, agent behavior, or downstream usefulness.

Indexing SHALL be governed where privacy affects access, visibility, exposure, publication, synchronization, export, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Indexing MAY include:

- filename indexing;
- title indexing;
- metadata indexing;
- full-text indexing;
- source-reference indexing;
- provenance indexing;
- relationship indexing;
- lifecycle-state indexing;
- authority-level indexing;
- validation-result indexing;
- tag indexing;
- category indexing;
- graph indexing;
- backlink indexing;
- search-result indexing;
- preview indexing;
- snippet indexing;
- summary indexing;
- embedding indexing;
- vector indexing;
- cache indexing;
- workflow indexing;
- agent-context indexing;
- implementation indexing;
- publication indexing;
- export-manifest indexing;
- backup-manifest indexing;
- migration-report indexing;
- another governed indexing context.

Indexing MUST be scoped.

A governed entity may be indexable in one context but not another.

A governed entity may be:

- indexable locally but not externally;
- indexable by title but not full text;
- indexable as metadata but not as content;
- indexable as a redacted summary but not as Source Material;
- indexable for authorized review but not general search;
- indexable for validation but not for publication;
- indexable for migration but not for downstream retrieval;
- indexable by a workflow but not by an agent;
- indexable by one implementation but not another;
- indexable only under a future governed specification.

Indexing permission MUST NOT be inferred from:

- file existence;
- storage location;
- folder placement;
- filename;
- file extension;
- tag;
- icon;
- color;
- user-interface visibility;
- implementation visibility;
- access-control setting alone;
- synchronization setting alone;
- publication setting alone;
- backup setting alone;
- workflow completion;
- agent confidence;
- validation success;
- approval;
- Authority Level;
- Lifecycle State;
- source availability;
- relationship existence;
- search usefulness;
- graph usefulness;
- automation usefulness;
- undocumented convention.

These signals MAY support indexing enforcement, routing, display, validation, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where indexing affects governed handling or downstream use.

Indexing MUST remain distinguishable from Access.

Access permits interaction with a governed entity within a defined scope.

Indexing makes information searchable, retrievable, ranked, embedded, cached, summarized, categorized, or discoverable.

A governed entity may be accessible to an authorized reviewer but not broadly indexable.

A governed entity may be indexed for authorized retrieval while content remains inaccessible without permission.

A governed entity may be accessible to a workflow but not indexable in workflow logs, search, summaries, embeddings, or caches.

Indexing MUST remain distinguishable from Visibility.

Indexing may create visibility, but indexing and visibility are not the same concept.

An indexed entity may be hidden from general display.

A visible entity may not be indexed.

An index may reveal restricted information even when the original governed entity is not displayed.

Indexing MUST remain distinguishable from Publication.

Indexing may support publication, but indexing alone does not create publication permission.

A governed entity may be indexed for internal search but not publishable.

A governed entity may be publishable as a redacted record but not indexable in full.

A published entity may still require restricted indexing for Source References, provenance, relationships, metadata, validation results, lifecycle context, authority context, workflow context, agent context, or implementation context.

Indexing MUST remain distinguishable from Synchronization.

Synchronization copies or transmits governed entities or representations across environments.

Indexing creates or updates discovery structures, retrieval structures, embeddings, summaries, caches, graph structures, relationship maps, or search artifacts.

Synchronization may copy indexes.

Indexing may require synchronization.

Neither behavior grants permission for the other by itself.

Indexing MUST preserve Source Reference and provenance privacy.

Indexing a Knowledge Record MUST NOT automatically index its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that behavior.

Indexing provenance MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Indexing MUST preserve relationship privacy.

Indexing a governed entity MUST NOT automatically index its relationships.

Indexing a relationship MUST NOT automatically index all connected entities.

Indexing connected entities MUST NOT automatically index relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A relationship index may reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Indexing MUST preserve derived artifact privacy.

Derived indexing artifacts MAY include:

- search indexes;
- embeddings;
- vector stores;
- graph indexes;
- relationship maps;
- summaries;
- previews;
- snippets;
- tags;
- categories;
- rankings;
- caches;
- logs;
- validation outputs;
- workflow outputs;
- agent outputs;
- implementation records.

Derived indexing artifacts SHOULD inherit applicable Privacy Classification, privacy scope, relationship limits, Source Reference limits, provenance limits, lifecycle limits, authority limits, validation limits, compatibility limits, publication limits, export limits, synchronization limits, backup limits, workflow limits, agent limits, implementation limits, and downstream-use limits where exposure may reveal protected information.

Indexing MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity indexable.

A draft entity may be indexable only within an authorized drafting or review scope.

A rejected entity may remain indexable only for authorized historical review where permitted.

An archived entity may be indexable only in an authorized archive context.

A quarantined entity MUST NOT be indexed into normal-use search, graph, retrieval, embedding, workflow, agent, publication, or downstream-use contexts unless a governed process explicitly permits that behavior within a defined scope.

Indexing MUST preserve Authority Level boundaries.

Authority does not grant indexing permission by itself.

A high-authority entity may be non-indexable outside its privacy scope.

A low-authority entity may be indexable within an authorized scope.

Indexing authority context SHOULD preserve authority limits where omission would create misleading interpretation or downstream misuse.

Indexing SHOULD support redaction and minimization.

A governed entity MAY be indexed through a redacted, summarized, masked, metadata-only, title-only, placeholder, vector-limited, cache-limited, or otherwise constrained representation where full indexing would expose restricted information.

A redacted indexed representation MUST remain distinguishable from the full governed entity.

Indexing minimization means that a compliant process SHOULD index only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, implementation context, or downstream-use context required for the permitted indexing purpose.

Indexing SHOULD support review.

A reviewer SHOULD be able to determine:

- whether indexing is permitted;
- what indexing scope applies;
- what index type applies;
- what indexed representation is permitted;
- whether full indexing is permitted;
- whether partial indexing is permitted;
- whether redaction is required;
- whether indexing is current or historical;
- whether indexing is temporary or persistent;
- whether indexing requires review;
- whether indexing is limited by Source References;
- whether indexing is limited by provenance;
- whether indexing is limited by relationships;
- whether indexing is limited by Lifecycle State;
- whether indexing is limited by Authority Level;
- whether indexing is limited by Validation State;
- whether indexing is limited by compatibility;
- whether indexing is limited by access, visibility, publication, synchronization, export, backup, import, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Indexing SHOULD support validation.

A validator SHOULD be able to determine whether indexing rules are explicit where required, whether indexing scope is compatible with Privacy Classification, whether indexing handling preserves Source References and provenance, whether indexing handling preserves relationship privacy, whether derived indexing artifacts preserve applicable privacy limits, and whether indexing handling remains compatible across import, export, migration, backup, restoration, synchronization, publication, workflow activity, agent activity, implementation replacement, and downstream use.

Indexing is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether indexing is permitted, what indexed representation is permitted, what scope applies, what limits exist, whether redaction is required, whether indexing changed, and whether privacy meaning remains preserved across time and implementation replacement.

## 14. Privacy and Export

Privacy and Export defines how Privacy Classification affects producing, copying, packaging, transferring, serializing, sharing, or moving a governed entity or representation from a compliant environment for use elsewhere.

Export exists so that a governed entity is not copied out, transferred, shared, serialized, packaged, migrated outward, published indirectly, exposed to agents, exposed to workflows, exposed to implementations, synchronized externally, backed up externally, indexed externally, or used downstream merely because export is technically possible or operationally convenient.

Export SHALL be governed where privacy affects access, visibility, exposure, publication, synchronization, indexing, backup, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Export MAY include:

- Markdown export;
- metadata export;
- Source Material export;
- Source Reference export;
- provenance export;
- relationship export;
- validation-result export;
- lifecycle-state export;
- authority-level export;
- privacy-metadata export;
- workflow-output export;
- agent-output export;
- index export;
- embedding export;
- cache export;
- backup package export;
- migration package export;
- publication package export;
- implementation-specific export;
- archive export;
- report export;
- another governed export context.

Export MUST be scoped.

A governed entity may be exportable in one context but not another.

A governed entity may be:

- exportable for backup but not publication;
- exportable for migration but not public release;
- exportable as metadata but not as content;
- exportable as a redacted summary but not as Source Material;
- exportable as a Knowledge Record but not as provenance;
- exportable as a citation but not as source context;
- exportable to a governed implementation but not to an unrestricted tool;
- exportable for validation but not for downstream use;
- exportable for human review but not for agent processing;
- exportable only under a future governed specification.

Export permission MUST NOT be inferred from:

- access permission;
- visibility permission;
- publication permission;
- synchronization permission;
- indexing permission;
- backup permission;
- approval;
- Authority Level;
- Validation State;
- Lifecycle State;
- source reliability;
- source authority;
- source availability;
- relationship existence;
- provenance existence;
- workflow completion;
- agent confidence;
- implementation visibility;
- file existence;
- storage location;
- folder placement;
- filename;
- tag;
- export tool availability;
- successful prior export;
- undocumented convention.

These signals MAY support export review, export routing, validation, display, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where export affects governed handling or downstream use.

Export MUST remain distinguishable from Publication.

Publication makes a governed entity available beyond its prior privacy boundary.

Export produces a governed entity or representation for use elsewhere.

An export may create publication risk if the exported package, receiving environment, downstream user, implementation, workflow, agent, index, backup, archive, or repository broadens exposure.

Export review SHOULD determine whether export creates publication risk.

Export MUST remain distinguishable from Synchronization.

Synchronization keeps environments aligned, replicated, mirrored, cached, or transmitted.

Export produces a package, copy, representation, serialization, record, archive, or transfer object for use elsewhere.

A governed entity may be synchronizable within a controlled scope but not exportable.

A governed entity may be exportable for migration but not synchronizable into a broader environment.

Export MUST remain distinguishable from Backup.

Backup preserves a copy for restoration, continuity, audit, migration, disaster recovery, or long-term preservation.

Export produces an external representation for use elsewhere.

A backup may use export-like packaging, but backup permission does not automatically create export permission.

Export permission does not automatically create unrestricted backup permission.

Export MUST remain distinguishable from Access.

Access permits interaction with a governed entity within a defined scope.

Export creates a representation that may leave the current environment or context.

A governed entity may be accessible locally but not exportable.

A governed entity may be accessible to a workflow but not exportable by that workflow.

A governed entity may be accessible to an agent but not exportable in prompts, files, logs, caches, embeddings, or outputs.

Export MUST preserve Object Identity.

Exporting a governed entity MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Export SHOULD preserve stable Object Identity where doing so is necessary for interpretation, relationship preservation, provenance preservation, lifecycle handling, authority handling, privacy handling, validation, import, migration, compatibility, or future review.

Export MUST preserve Source Reference and provenance privacy.

Exporting a Knowledge Record MUST NOT automatically export its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that behavior.

Exporting provenance MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Export MUST preserve relationship privacy.

Exporting a governed entity MUST NOT automatically export its relationships.

Exporting a relationship MUST NOT automatically export all connected entities.

Exporting connected entities MUST NOT automatically export relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A relationship included in an export may reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Export MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity exportable.

A draft entity may be exportable only within an authorized drafting, review, backup, or migration scope.

A rejected entity may remain non-exportable.

An archived entity may be exportable only within authorized archival, audit, restoration, or migration scope.

A quarantined entity MUST NOT be exported into normal-use, external, public, agent-readable, workflow-readable, or downstream-use environments unless a governed process explicitly permits that behavior within a defined scope.

Export MUST preserve Authority Level boundaries.

Authority does not grant export permission by itself.

A high-authority entity may be non-exportable outside its privacy scope.

A low-authority entity may be exportable within an authorized scope.

Exporting authority context SHOULD preserve authority limits where omission would create misleading interpretation or downstream misuse.

Export SHOULD support redaction and minimization.

A governed entity MAY be exported through a redacted, summarized, masked, transformed, metadata-only, source-reference-only, relationship-limited, provenance-limited, placeholder, or otherwise constrained representation where full export would expose restricted information.

A redacted exported representation MUST remain distinguishable from the full governed entity.

Export minimization means that a compliant process SHOULD export only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, implementation context, indexing context, backup context, or downstream-use context required for the permitted export purpose.

Export SHOULD preserve enough context for authorized review without exposing restricted information.

Export SHOULD support compatibility.

A compliant export process SHOULD preserve Privacy Classification, privacy scope, privacy assignment, privacy review context, Source Reference limits, provenance limits, relationship limits, lifecycle limits, authority limits, validation limits, synchronization limits, indexing limits, backup limits, workflow limits, agent limits, implementation limits, and downstream-use limits where those limits affect future interpretation or use.

An export process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, declassify, over-classify, under-classify, or regenerate Privacy Classification in a way that causes privacy exposure, loss of meaning, broken provenance, authority ambiguity, lifecycle ambiguity, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, synchronization error, backup exposure, import ambiguity, migration loss, governance drift, or implementation lock-in.

Export SHOULD support review.

A reviewer SHOULD be able to determine:

- whether export is permitted;
- what export scope applies;
- what export purpose applies;
- what receiving environment applies;
- what exported representation is permitted;
- whether full export is permitted;
- whether partial export is permitted;
- whether redaction is required;
- whether export is current or historical;
- whether export is temporary or persistent;
- whether export requires review;
- whether export is limited by Source References;
- whether export is limited by provenance;
- whether export is limited by relationships;
- whether export is limited by Lifecycle State;
- whether export is limited by Authority Level;
- whether export is limited by Validation State;
- whether export is limited by compatibility;
- whether export is limited by access, visibility, publication, synchronization, indexing, backup, import, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Export SHOULD support validation.

A validator SHOULD be able to determine whether export rules are explicit where required, whether export scope is compatible with Privacy Classification, whether export handling preserves Source References and provenance, whether export handling preserves relationship privacy, whether exported artifacts preserve applicable privacy limits, and whether export handling remains compatible across import, migration, backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, implementation replacement, and downstream use.

Export is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether export is permitted, what exported representation is permitted, what source and receiving scopes apply, what limits exist, whether redaction is required, whether export changed privacy meaning, and whether privacy meaning remains preserved across time and implementation replacement.

## 15. Privacy and Backup

Privacy and Backup defines how Privacy Classification affects preserving copies of governed entities for restoration, continuity, archival, audit, migration, disaster recovery, rollback, verification, or long-term preservation.

Backup exists so that a governed entity is not copied into an unrestricted, insecure, external, public, broadly synchronized, broadly indexed, agent-readable, workflow-readable, implementation-visible, exportable, publishable, or downstream-usable preservation environment merely because backup is technically available or operationally convenient.

Backup SHALL be governed where privacy affects access, visibility, exposure, publication, synchronization, indexing, export, restoration, import, migration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Backup MAY include:

- local backup;
- external backup;
- cloud backup;
- repository backup;
- vault backup;
- archive backup;
- database backup;
- file-system backup;
- implementation backup;
- workflow backup;
- agent-output backup;
- index backup;
- embedding backup;
- cache backup;
- Source Material backup;
- Source Reference backup;
- provenance backup;
- relationship backup;
- metadata backup;
- validation-result backup;
- export-package backup;
- migration-package backup;
- another governed backup context.

Backup MUST be scoped.

A governed entity may be backed up in one context but not another.

A governed entity may be:

- backed up locally but not externally;
- backed up in encrypted form under a future governed safeguard;
- backed up as metadata but not as content;
- backed up as a redacted representation but not in full;
- backed up for restoration but not export;
- backed up for archival but not publication;
- backed up for migration but not indexing;
- backed up as a Knowledge Record but not as Source Material;
- backed up without agent-readable outputs;
- backed up only under a future governed specification.

Backup permission MUST NOT be inferred from:

- access permission;
- visibility permission;
- publication permission;
- synchronization permission;
- indexing permission;
- export permission;
- approval;
- Authority Level;
- Validation State;
- Lifecycle State;
- source reliability;
- source authority;
- source availability;
- relationship existence;
- provenance existence;
- workflow completion;
- agent confidence;
- implementation visibility;
- file existence;
- storage location;
- folder placement;
- filename;
- tag;
- backup tool availability;
- successful prior backup;
- undocumented convention.

These signals MAY support backup review, backup routing, validation, display, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where backup affects governed handling or downstream use.

Backup MUST remain distinguishable from Export.

Export produces a representation for use elsewhere.

Backup preserves a copy for restoration, continuity, archival, audit, migration, disaster recovery, rollback, verification, or long-term preservation.

A backup may later become an export source if restored or transferred.

Export review SHOULD occur when a backup is used for a purpose beyond backup, restoration, audit, continuity, migration, or preservation.

Backup MUST remain distinguishable from Synchronization.

Synchronization keeps environments aligned, replicated, mirrored, cached, or transmitted.

Backup preserves a copy for recovery or preservation.

A synchronized copy is not automatically a governed backup.

A backup copy is not automatically synchronizable.

Backup MUST remain distinguishable from Publication.

Backup does not make a governed entity public by itself.

A backup may create publication risk if backup storage, backup metadata, backup manifests, backup logs, restoration tools, synchronized backups, indexed backups, agent-readable backups, workflow-readable backups, or implementation-visible backups expose restricted information beyond the permitted privacy scope.

Backup review SHOULD determine whether backup creates publication, synchronization, indexing, export, or downstream-use risk.

Backup MUST remain distinguishable from Access.

Access permits interaction with a governed entity within a defined scope.

Backup preserves a copy that may be restored, inspected, audited, migrated, or reused later.

A governed entity may be accessible but not backed up externally.

A governed entity may be backed up but not accessible without authorized restoration review.

Backup MUST preserve Object Identity.

Backing up a governed entity MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Backup SHOULD preserve stable Object Identity where doing so is necessary for restoration, relationship preservation, provenance preservation, lifecycle handling, authority handling, privacy handling, validation, migration, compatibility, or future review.

Backup MUST preserve Source Reference and provenance privacy.

Backing up a Knowledge Record MUST NOT automatically back up its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that behavior.

Backing up provenance MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Backup MUST preserve relationship privacy.

Backing up a governed entity MUST NOT automatically back up its relationships.

Backing up a relationship MUST NOT automatically back up all connected entities.

Backing up connected entities MUST NOT automatically back up relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A relationship included in a backup may reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Backup MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity backup-permitted in every environment.

A draft entity may be backed up only within an authorized drafting, review, continuity, or restoration scope.

A rejected entity may remain backup-restricted where historical preservation would create privacy risk.

An archived entity may be backup-permitted only within authorized archival or preservation scope.

A quarantined entity MUST NOT be backed up into normal-use, external, public, agent-readable, workflow-readable, or downstream-use environments unless a governed process explicitly permits that behavior within a defined scope.

Backup MUST preserve Authority Level boundaries.

Authority does not grant backup permission by itself.

A high-authority entity may be backup-restricted outside its privacy scope.

A low-authority entity may be backup-permitted within an authorized scope.

Backing up authority context SHOULD preserve authority limits where omission would create misleading interpretation, restoration error, or downstream misuse.

Backup SHOULD support restoration review.

Restoration review SHOULD determine whether restoring a backed-up entity would expose, publish, synchronize, index, export, route, migrate, agent-process, workflow-process, implementation-display, or downstream-use restricted information beyond the permitted privacy scope.

A backup that was permitted at the time of creation may require review before restoration if Privacy Classification, Privacy Scope, Source References, provenance, relationships, Lifecycle State, Authority Level, Validation State, compatibility, implementation context, or governance expectations changed.

Backup SHOULD support redaction and minimization.

A governed entity MAY be backed up through a redacted, summarized, masked, transformed, metadata-only, source-reference-only, relationship-limited, provenance-limited, placeholder, or otherwise constrained representation where full backup would expose restricted information.

A redacted backup representation MUST remain distinguishable from the full governed entity.

Backup minimization means that a compliant process SHOULD back up only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, implementation context, indexing context, export context, or downstream-use context required for the permitted backup purpose.

Backup SHOULD preserve enough context for authorized restoration, audit, migration, validation, compatibility review, and governance without exposing restricted information beyond the permitted scope.

Backup SHOULD support compatibility.

A compliant backup process SHOULD preserve Privacy Classification, privacy scope, privacy assignment, privacy review context, Source Reference limits, provenance limits, relationship limits, lifecycle limits, authority limits, validation limits, synchronization limits, indexing limits, export limits, workflow limits, agent limits, implementation limits, and downstream-use limits where those limits affect future interpretation, restoration, migration, audit, or use.

A backup process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, declassify, over-classify, under-classify, or regenerate Privacy Classification in a way that causes privacy exposure, loss of meaning, broken provenance, authority ambiguity, lifecycle ambiguity, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, synchronization error, export exposure, restoration ambiguity, migration loss, governance drift, or implementation lock-in.

Backup SHOULD support review.

A reviewer SHOULD be able to determine:

- whether backup is permitted;
- what backup scope applies;
- what backup purpose applies;
- what backup environment applies;
- what backed-up representation is permitted;
- whether full backup is permitted;
- whether partial backup is permitted;
- whether redaction is required;
- whether backup is current or historical;
- whether backup is temporary or persistent;
- whether backup requires review;
- whether restoration requires review;
- whether backup is limited by Source References;
- whether backup is limited by provenance;
- whether backup is limited by relationships;
- whether backup is limited by Lifecycle State;
- whether backup is limited by Authority Level;
- whether backup is limited by Validation State;
- whether backup is limited by compatibility;
- whether backup is limited by access, visibility, publication, synchronization, indexing, export, import, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Backup SHOULD support validation.

A validator SHOULD be able to determine whether backup rules are explicit where required, whether backup scope is compatible with Privacy Classification, whether backup handling preserves Source References and provenance, whether backup handling preserves relationship privacy, whether backed-up artifacts preserve applicable privacy limits, whether restoration review is required, and whether backup handling remains compatible across import, export, migration, restoration, synchronization, indexing, publication, workflow activity, agent activity, implementation replacement, and downstream use.

Backup is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether backup is permitted, what backed-up representation is permitted, what backup and restoration scopes apply, what limits exist, whether redaction is required, whether restoration review is required, whether backup changed privacy meaning, and whether privacy meaning remains preserved across time and implementation replacement.

## 16. Privacy and Agent Behavior

Privacy and Agent Behavior defines how Privacy Classification affects agent reading, classification, extraction, summarization, transformation, validation, routing, linking, modification, publication support, synchronization support, indexing support, export support, backup support, migration support, reasoning, recommendation, and output generation.

Privacy and Agent Behavior exists so that agents may assist knowledge work without becoming unreviewable authorities over privacy assignment, privacy reduction, privacy escalation, declassification, access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, workflow permission, implementation permission, or downstream-use permission.

Agent behavior SHALL be governed where privacy affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Agent behavior MAY include:

- reading governed entities;
- proposing Privacy Classification;
- identifying privacy-sensitive content;
- detecting missing Privacy Classification;
- detecting conflicting Privacy Classification;
- identifying exposure risk;
- recommending privacy review;
- recommending redaction;
- summarizing governed entities;
- extracting information;
- transforming information;
- generating metadata;
- proposing relationships;
- validating privacy expectations;
- routing entities for workflow review;
- preparing publication candidates;
- preparing synchronization candidates;
- preparing indexing candidates;
- preparing export candidates;
- preparing backup candidates;
- preparing migration candidates;
- producing agent outputs;
- producing logs;
- producing embeddings;
- producing caches;
- producing prompts;
- producing derived records;
- another governed agent activity.

Agent access MUST be scoped.

A governed entity may be agent-readable in one context but agent-restricted in another.

A governed entity may be:

- readable by one agent role but not another;
- readable for validation but not summarization;
- readable for privacy review but not publication;
- readable for extraction but not downstream output;
- readable for local processing but not external processing;
- readable as metadata but not content;
- readable as a redacted representation but not full text;
- readable by a workflow-supervised agent but not by an autonomous agent;
- readable for migration support but not model training;
- readable only under a future governed specification.

Agent permission MUST NOT be inferred from:

- access permission alone;
- visibility permission alone;
- publication permission alone;
- synchronization permission alone;
- indexing permission alone;
- export permission alone;
- backup permission alone;
- approval;
- Authority Level;
- Validation State;
- Lifecycle State;
- source reliability;
- source authority;
- source availability;
- relationship existence;
- provenance existence;
- workflow completion;
- agent confidence;
- implementation visibility;
- file existence;
- storage location;
- folder placement;
- filename;
- tag;
- successful prior agent processing;
- undocumented convention.

These signals MAY support agent routing, validation, display, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where agent behavior affects governed handling or downstream use.

Agent behavior MUST remain distinguishable from human review.

An agent MAY propose, classify, summarize, extract, transform, validate, route, recommend, flag, or support privacy handling.

A human or governed workflow MAY confirm, revise, reject, limit, escalate, reduce, or approve privacy-related actions where required.

An agent MUST NOT be treated as the final authority for privacy decisions where governance, publication, export, synchronization, indexing, backup, agent output, workflow routing, implementation exposure, or downstream use affects privacy boundaries unless a future governed specification explicitly permits that behavior within a defined scope.

Agent behavior MUST remain distinguishable from workflow behavior.

A workflow may permit, constrain, route, review, approve, reject, or record agent activity.

Agent task completion does not automatically mean Privacy Classification was assigned, reviewed, approved, reduced, escalated, declassified, published, synchronized, indexed, exported, backed up, migrated, or made safe for downstream use.

Workflow completion MUST NOT be treated as privacy approval unless a governed workflow specification explicitly defines that result within a defined scope.

Agent behavior MUST remain distinguishable from validation.

An agent may support validation.

An agent may run or assist a validator.

An agent may identify missing, unclear, conflicting, unsafe, overexposed, underprotected, or incompatible Privacy Classification.

An agent-generated validation result MUST NOT expose, publish, synchronize, index, export, back up, declassify, grant access to, or route a governed entity beyond its privacy boundary unless a governed workflow or specification explicitly permits that behavior within a defined scope.

Agent behavior MUST preserve Object Identity.

Agent processing MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

An agent-generated summary, transformation, extraction, classification, embedding, cache, prompt, output, relationship, metadata record, or derived record MUST remain distinguishable from the original governed entity where confusion would affect identity, provenance, privacy, authority, lifecycle state, validation, compatibility, import, export, migration, or downstream use.

Agent behavior MUST preserve Source Reference and provenance privacy.

Agent access to a Knowledge Record MUST NOT automatically grant access to its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that access.

Agent outputs MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Agent behavior MUST preserve relationship privacy.

Agent access to a governed entity MUST NOT automatically grant access to its relationships.

Agent access to a relationship MUST NOT automatically grant access to all connected entities.

Agent access to connected entities MUST NOT automatically grant access to relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

An agent-generated relationship MAY reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Agent-generated relationships SHOULD remain proposed, reviewable, provenance-aware, and privacy-preserving unless a governed process explicitly approves them.

Agent behavior MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity agent-readable.

A draft entity may be agent-readable only within an authorized drafting, review, validation, or workflow scope.

A rejected entity may remain agent-restricted.

An archived entity may be agent-readable only within authorized archival, audit, validation, restoration, or migration scope.

A quarantined entity MUST NOT be exposed to normal-use agents unless a governed process explicitly permits that behavior within a defined scope.

Agent behavior MUST preserve Authority Level boundaries.

Authority does not grant agent access by itself.

A high-authority entity may be agent-restricted outside its privacy scope.

A low-authority entity may be agent-readable within an authorized scope.

Agent outputs SHOULD preserve authority limits where omission would create misleading interpretation, automation error, validation error, publication error, export error, or downstream misuse.

Agent behavior SHOULD preserve privacy in derived artifacts.

Derived agent artifacts MAY include:

- prompts;
- completions;
- summaries;
- extracts;
- transformations;
- classifications;
- metadata;
- relationships;
- validation outputs;
- routing recommendations;
- publication candidates;
- synchronization candidates;
- indexing candidates;
- export candidates;
- backup candidates;
- migration candidates;
- embeddings;
- vector records;
- caches;
- logs;
- temporary files;
- implementation records.

Derived agent artifacts SHOULD inherit applicable Privacy Classification, privacy scope, relationship limits, Source Reference limits, provenance limits, lifecycle limits, authority limits, validation limits, compatibility limits, access limits, visibility limits, publication limits, synchronization limits, indexing limits, export limits, backup limits, workflow limits, implementation limits, and downstream-use limits where exposure may reveal protected information.

Agent behavior SHOULD support minimization.

Agent minimization means that a compliant agent process SHOULD access, include, transform, summarize, cache, log, embed, export, synchronize, index, or output only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, implementation context, or downstream-use context required for the permitted agent purpose.

Agent minimization SHOULD NOT break reviewability, provenance preservation, validation, compatibility, governance, or future repair where those are required.

Agent behavior SHOULD support review.

A reviewer SHOULD be able to determine:

- whether agent access is permitted;
- what agent scope applies;
- what agent role or agent class applies where applicable;
- what agent action was performed or proposed;
- what source material was accessed where applicable;
- what governed entity was accessed where applicable;
- what output was produced where applicable;
- whether redaction was required;
- whether agent behavior was current or historical;
- whether agent behavior was temporary or persistent;
- whether agent behavior required review;
- whether agent behavior is limited by Source References;
- whether agent behavior is limited by provenance;
- whether agent behavior is limited by relationships;
- whether agent behavior is limited by Lifecycle State;
- whether agent behavior is limited by Authority Level;
- whether agent behavior is limited by Validation State;
- whether agent behavior is limited by compatibility;
- whether agent behavior is limited by access, visibility, publication, synchronization, indexing, export, backup, import, migration, workflow behavior, implementation behavior, or downstream use.

Agent behavior SHOULD support validation.

A validator SHOULD be able to determine whether agent rules are explicit where required, whether agent scope is compatible with Privacy Classification, whether agent handling preserves Source References and provenance, whether agent handling preserves relationship privacy, whether derived agent artifacts preserve applicable privacy limits, and whether agent handling remains compatible across import, export, migration, backup, restoration, synchronization, indexing, publication, workflow activity, implementation replacement, and downstream use.

Privacy and Agent Behavior is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether agent behavior is permitted, what agent action is permitted, what input and output scope applies, what limits exist, whether redaction is required, whether review is required, whether agent-derived artifacts preserve privacy, and whether privacy meaning remains preserved across time and implementation replacement.

## 17. Privacy and Workflow Behavior

Privacy and Workflow Behavior defines how Privacy Classification affects workflow routing, review, validation, approval support, rejection support, restriction, quarantine, redaction, publication support, synchronization support, indexing support, export support, backup support, restoration support, import support, migration support, repair, archival, logging, task assignment, and downstream workflow output.

Privacy and Workflow Behavior exists so that workflows may coordinate privacy-sensitive knowledge operations without silently weakening, broadening, replacing, bypassing, or redefining Privacy Classification.

Workflow behavior SHALL be governed where privacy affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Workflow behavior MAY include:

- routing a governed entity for review;
- routing a governed entity for validation;
- routing a governed entity for privacy review;
- routing a governed entity for redaction;
- routing a governed entity for publication review;
- routing a governed entity for export review;
- routing a governed entity for synchronization review;
- routing a governed entity for indexing review;
- routing a governed entity for backup review;
- routing a governed entity for restoration review;
- routing a governed entity for import review;
- routing a governed entity for migration review;
- routing a governed entity for agent processing;
- routing a governed entity for implementation processing;
- assigning work to a human;
- assigning work to an agent where permitted;
- generating workflow logs;
- generating workflow outputs;
- generating workflow metadata;
- generating workflow summaries;
- generating workflow validation results;
- generating workflow review records;
- generating workflow repair records;
- generating workflow publication candidates;
- generating workflow export candidates;
- generating workflow synchronization candidates;
- generating workflow backup candidates;
- generating workflow migration candidates;
- another governed workflow activity.

Workflow access MUST be scoped.

A governed entity may be workflow-readable in one workflow context but restricted in another.

A governed entity may be:

- readable by a privacy-review workflow but not by a publication workflow;
- readable by a validation workflow but not by an export workflow;
- readable by a redaction workflow but not by an indexing workflow;
- routable to a human reviewer but not to an agent;
- routable to an agent under supervision but not to an autonomous workflow;
- available as metadata but not full content;
- available as a redacted representation but not unredacted content;
- available for migration review but not downstream publication;
- available for backup review but not external synchronization;
- available only under a future governed workflow specification.

Workflow permission MUST NOT be inferred from:

- access permission alone;
- visibility permission alone;
- publication permission alone;
- synchronization permission alone;
- indexing permission alone;
- export permission alone;
- backup permission alone;
- agent permission alone;
- implementation visibility alone;
- approval;
- Authority Level;
- Validation State;
- Lifecycle State;
- source reliability;
- source authority;
- source availability;
- relationship existence;
- provenance existence;
- workflow completion;
- agent confidence;
- file existence;
- storage location;
- folder placement;
- filename;
- tag;
- successful prior workflow execution;
- undocumented convention.

These signals MAY support workflow routing, review, validation, restriction, implementation behavior, agent assistance, or operational convenience.

They MUST NOT replace explicit Privacy Classification where workflow behavior affects governed handling or downstream use.

Workflow behavior MUST remain distinguishable from Privacy Assignment.

A workflow MAY propose, route, record, support, or execute Privacy Assignment only where a governed workflow process explicitly permits that behavior within a defined scope.

Workflow completion MUST NOT assign, reduce, remove, declassify, escalate, weaken, broaden, collapse, reinterpret, or replace Privacy Classification unless a governed workflow specification explicitly defines that result within a defined scope.

Workflow behavior MUST remain distinguishable from Privacy Review.

A workflow may route an entity through a privacy review step.

A workflow may record that review occurred.

A workflow may preserve the review result.

However, workflow routing or completion does not mean Privacy Review occurred unless the workflow explicitly includes and records a governed Privacy Review process.

Workflow behavior MUST remain distinguishable from Validation.

A workflow may run validation.

A workflow may route validation results.

A workflow may block or warn based on validation results.

Validation success does not grant workflow permission, publication permission, export permission, synchronization permission, indexing permission, backup permission, agent permission, implementation permission, or downstream-use permission by itself.

Workflow behavior MUST preserve Object Identity.

Workflow processing MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A workflow-generated summary, extract, transformation, classification, relationship, metadata record, validation result, review result, publication candidate, export candidate, backup candidate, migration candidate, or derived record MUST remain distinguishable from the original governed entity where confusion would affect identity, provenance, privacy, authority, lifecycle state, validation, compatibility, import, export, migration, or downstream use.

Workflow behavior MUST preserve Source Reference and provenance privacy.

Workflow access to a Knowledge Record MUST NOT automatically grant access to its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that access.

Workflow outputs MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Workflow behavior MUST preserve relationship privacy.

Workflow access to a governed entity MUST NOT automatically grant access to its relationships.

Workflow access to a relationship MUST NOT automatically grant access to all connected entities.

Workflow access to connected entities MUST NOT automatically grant access to relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A workflow-generated relationship MAY reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Workflow-generated relationships SHOULD remain proposed, reviewable, provenance-aware, and privacy-preserving unless a governed process explicitly approves them.

Workflow behavior MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity workflow-readable for every workflow.

A draft entity may be workflow-readable only within an authorized drafting, review, validation, repair, or workflow scope.

A rejected entity may remain workflow-restricted.

An archived entity may be workflow-readable only within authorized archival, audit, validation, restoration, or migration scope.

A quarantined entity MUST NOT be routed into normal-use workflows unless a governed process explicitly permits that behavior within a defined scope.

Workflow behavior MUST preserve Authority Level boundaries.

Authority does not grant workflow access by itself.

A high-authority entity may be workflow-restricted outside its privacy scope.

A low-authority entity may be workflow-readable within an authorized scope.

Workflow outputs SHOULD preserve authority limits where omission would create misleading interpretation, automation error, validation error, publication error, export error, migration error, or downstream misuse.

Workflow behavior SHOULD preserve privacy in derived artifacts.

Derived workflow artifacts MAY include:

- workflow logs;
- task records;
- review records;
- validation outputs;
- privacy review outputs;
- redaction outputs;
- routing decisions;
- summaries;
- extracts;
- transformations;
- classifications;
- metadata;
- relationships;
- publication candidates;
- synchronization candidates;
- indexing candidates;
- export candidates;
- backup candidates;
- restoration candidates;
- import candidates;
- migration candidates;
- repair records;
- audit records;
- implementation records.

Derived workflow artifacts SHOULD inherit applicable Privacy Classification, privacy scope, relationship limits, Source Reference limits, provenance limits, lifecycle limits, authority limits, validation limits, compatibility limits, access limits, visibility limits, publication limits, synchronization limits, indexing limits, export limits, backup limits, agent limits, implementation limits, and downstream-use limits where exposure may reveal protected information.

Workflow behavior SHOULD support minimization.

Workflow minimization means that a compliant workflow process SHOULD route, expose, transform, summarize, log, export, synchronize, index, back up, migrate, or output only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, agent context, implementation context, or downstream-use context required for the permitted workflow purpose.

Workflow minimization SHOULD NOT break reviewability, provenance preservation, validation, compatibility, governance, or future repair where those are required.

Workflow behavior SHOULD support review.

A reviewer SHOULD be able to determine:

- whether workflow access is permitted;
- what workflow scope applies;
- what workflow stage or workflow type applies where applicable;
- what workflow action was performed or proposed;
- what governed entity was accessed where applicable;
- what source material was accessed where applicable;
- what output was produced where applicable;
- whether redaction was required;
- whether workflow behavior was current or historical;
- whether workflow behavior was temporary or persistent;
- whether workflow behavior required review;
- whether workflow behavior is limited by Source References;
- whether workflow behavior is limited by provenance;
- whether workflow behavior is limited by relationships;
- whether workflow behavior is limited by Lifecycle State;
- whether workflow behavior is limited by Authority Level;
- whether workflow behavior is limited by Validation State;
- whether workflow behavior is limited by compatibility;
- whether workflow behavior is limited by access, visibility, publication, synchronization, indexing, export, backup, import, migration, agent behavior, implementation behavior, or downstream use.

Workflow behavior SHOULD support validation.

A validator SHOULD be able to determine whether workflow rules are explicit where required, whether workflow scope is compatible with Privacy Classification, whether workflow handling preserves Source References and provenance, whether workflow handling preserves relationship privacy, whether derived workflow artifacts preserve applicable privacy limits, and whether workflow handling remains compatible across import, export, migration, backup, restoration, synchronization, indexing, publication, agent activity, implementation replacement, and downstream use.

Privacy and Workflow Behavior is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether workflow behavior is permitted, what workflow action is permitted, what input and output scope applies, what limits exist, whether redaction is required, whether review is required, whether workflow-derived artifacts preserve privacy, and whether privacy meaning remains preserved across time and implementation replacement.

## 18. Privacy and Implementation Behavior

Privacy and Implementation Behavior defines how Privacy Classification affects software tools, vaults, databases, file systems, interfaces, plugins, automations, services, search systems, graph systems, synchronization systems, backup systems, publication systems, agent systems, workflow systems, and other implementations that create, read, display, index, cache, synchronize, publish, export, back up, restore, import, migrate, validate, or process governed entities.

Privacy and Implementation Behavior exists so that implementations may enforce, display, preserve, validate, and operationalize privacy rules without becoming the source of privacy meaning.

Implementation behavior SHALL be governed where privacy affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow behavior, agent behavior, validation, compatibility, governance, or downstream use.

Implementation behavior MAY include:

- displaying governed entities;
- hiding governed entities;
- filtering governed entities;
- searching governed entities;
- indexing governed entities;
- caching governed entities;
- synchronizing governed entities;
- exporting governed entities;
- backing up governed entities;
- restoring governed entities;
- importing governed entities;
- migrating governed entities;
- publishing governed entities;
- routing governed entities;
- validating governed entities;
- rendering metadata;
- rendering Source References;
- rendering provenance;
- rendering relationships;
- rendering lifecycle state;
- rendering Authority Level;
- rendering Privacy Classification;
- rendering validation results;
- creating implementation logs;
- creating implementation caches;
- creating implementation indexes;
- creating implementation previews;
- creating implementation summaries;
- creating implementation manifests;
- creating implementation records;
- another governed implementation activity.

Implementation access MUST be scoped.

A governed entity may be implementation-visible in one implementation context but restricted in another.

A governed entity may be:

- visible in a local vault but hidden in a shared interface;
- searchable in one implementation but not another;
- indexable locally but not externally;
- cacheable temporarily but not persistently;
- exportable through one governed profile but not another;
- publishable through a redacted interface but not in full;
- restorable in an authorized archive view but not normal navigation;
- available to a validator but not a public dashboard;
- available to a workflow system but not an agent system;
- available only under a future governed implementation profile.

Implementation permission MUST NOT be inferred from:

- file existence;
- storage location;
- folder placement;
- filename;
- file extension;
- tag;
- icon;
- color;
- user-interface visibility;
- implementation visibility;
- database presence;
- access-control setting alone;
- synchronization setting alone;
- publication setting alone;
- backup setting alone;
- indexing behavior alone;
- cache behavior alone;
- workflow completion;
- agent confidence;
- validation success;
- approval;
- Authority Level;
- Lifecycle State;
- source availability;
- relationship existence;
- successful prior implementation processing;
- undocumented convention.

These signals MAY support implementation enforcement, display, routing, validation, restriction, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where implementation behavior affects governed handling or downstream use.

Implementation behavior MUST remain distinguishable from Privacy Classification.

Privacy Classification defines standard-level privacy meaning.

Implementation behavior may enforce, display, route, restrict, validate, or preserve that meaning.

An implementation MUST NOT define Privacy Classification by itself unless a governed standard or specification explicitly defines that implementation behavior as a compliant representation within a defined scope.

Implementation behavior MUST remain distinguishable from access-control enforcement.

Access-control systems may enforce Privacy Classification.

File permissions, database permissions, encryption, vault separation, role-based access controls, application permissions, workflow permissions, agent permissions, synchronization controls, indexing controls, publication settings, backup policies, and implementation-specific restrictions may support privacy enforcement.

Those enforcement mechanisms do not define Privacy Classification by themselves.

Where implementation enforcement and Privacy Classification conflict, the conflict SHOULD be treated as a reviewable privacy issue.

A permissive implementation setting MUST NOT override a restrictive Privacy Classification.

A restrictive implementation setting MAY protect knowledge more strongly than the current Privacy Classification, but the reason for that restriction SHOULD remain reviewable where it affects governance, compatibility, migration, import, export, restoration, publication, synchronization, indexing, workflow behavior, agent behavior, or downstream use.

Implementation behavior MUST remain distinguishable from Visibility.

An implementation may display, hide, list, preview, summarize, index, cache, or search a governed entity.

Implementation visibility does not make the governed entity public, publishable, exportable, synchronizable, indexable in every context, backup-permitted, agent-readable, workflow-readable, or downstream-usable.

Implementation behavior MUST remain distinguishable from Publication.

An implementation may publish, render, or expose a governed entity.

Publication permission must still be governed by Privacy Classification and scope.

A public-facing implementation MUST NOT expose restricted content merely because the implementation can read, render, cache, search, index, route, export, back up, or synchronize it.

Implementation behavior MUST preserve Object Identity.

Implementation processing MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Implementation-specific identifiers, database rows, file paths, URLs, cache keys, search IDs, graph IDs, plugin IDs, synchronization IDs, backup IDs, and export IDs MUST NOT replace stable Object Identity unless a governed specification explicitly defines a compliant mapping.

Implementation behavior MUST preserve Source Reference and provenance privacy.

Displaying, indexing, caching, exporting, backing up, synchronizing, restoring, importing, migrating, publishing, or processing a Knowledge Record MUST NOT automatically expose its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that exposure.

Implementation logs, caches, previews, indexes, manifests, dashboards, summaries, and audit views MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Implementation behavior MUST preserve relationship privacy.

Displaying, indexing, caching, exporting, backing up, synchronizing, restoring, importing, migrating, publishing, or processing a governed entity MUST NOT automatically expose its relationships.

Displaying, indexing, caching, exporting, backing up, synchronizing, restoring, importing, migrating, publishing, or processing a relationship MUST NOT automatically expose all connected entities.

A relationship exposed through implementation behavior may reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Implementation behavior MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity visible, searchable, indexable, cacheable, exportable, synchronizable, backup-permitted, publishable, agent-readable, workflow-readable, or downstream-usable in every implementation.

A draft entity may be implementation-visible only within an authorized drafting, review, validation, repair, or workflow scope.

A rejected entity may remain implementation-restricted.

An archived entity may be implementation-visible only within authorized archival, audit, validation, restoration, or migration scope.

A quarantined entity MUST NOT be exposed through normal-use implementation behavior unless a governed process explicitly permits that behavior within a defined scope.

Implementation behavior MUST preserve Authority Level boundaries.

Authority does not grant implementation access by itself.

A high-authority entity may be implementation-restricted outside its privacy scope.

A low-authority entity may be implementation-visible within an authorized scope.

Implementation displays SHOULD preserve authority limits where omission would create misleading interpretation, automation error, validation error, publication error, export error, migration error, or downstream misuse.

Implementation behavior SHOULD preserve privacy in derived artifacts.

Derived implementation artifacts MAY include:

- indexes;
- search results;
- graph records;
- previews;
- snippets;
- summaries;
- caches;
- thumbnails;
- metadata views;
- relationship maps;
- dashboards;
- logs;
- manifests;
- exports;
- backups;
- restoration records;
- synchronization records;
- import records;
- migration records;
- validation outputs;
- workflow records;
- agent records;
- audit records;
- temporary files.

Derived implementation artifacts SHOULD inherit applicable Privacy Classification, privacy scope, relationship limits, Source Reference limits, provenance limits, lifecycle limits, authority limits, validation limits, compatibility limits, access limits, visibility limits, publication limits, synchronization limits, indexing limits, export limits, backup limits, workflow limits, agent limits, and downstream-use limits where exposure may reveal protected information.

Implementation behavior SHOULD support minimization.

Implementation minimization means that a compliant implementation SHOULD display, index, cache, synchronize, publish, export, back up, restore, import, migrate, log, or expose only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, or downstream-use context required for the permitted implementation purpose.

Implementation minimization SHOULD NOT break reviewability, provenance preservation, validation, compatibility, governance, or future repair where those are required.

Implementation behavior SHOULD support review.

A reviewer SHOULD be able to determine:

- whether implementation access is permitted;
- what implementation scope applies;
- what implementation profile or context applies where applicable;
- what implementation action was performed or proposed;
- what governed entity was accessed where applicable;
- what source material was accessed where applicable;
- what output or artifact was produced where applicable;
- whether redaction was required;
- whether implementation behavior was current or historical;
- whether implementation behavior was temporary or persistent;
- whether implementation behavior required review;
- whether implementation behavior is limited by Source References;
- whether implementation behavior is limited by provenance;
- whether implementation behavior is limited by relationships;
- whether implementation behavior is limited by Lifecycle State;
- whether implementation behavior is limited by Authority Level;
- whether implementation behavior is limited by Validation State;
- whether implementation behavior is limited by compatibility;
- whether implementation behavior is limited by access, visibility, publication, synchronization, indexing, export, backup, import, migration, workflow behavior, agent behavior, or downstream use.

Implementation behavior SHOULD support validation.

A validator SHOULD be able to determine whether implementation rules are explicit where required, whether implementation scope is compatible with Privacy Classification, whether implementation handling preserves Source References and provenance, whether implementation handling preserves relationship privacy, whether derived implementation artifacts preserve applicable privacy limits, and whether implementation handling remains compatible across import, export, migration, backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, implementation replacement, and downstream use.

Privacy and Implementation Behavior is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether implementation behavior is permitted, what implementation action is permitted, what input and output scope applies, what limits exist, whether redaction is required, whether review is required, whether implementation-derived artifacts preserve privacy, and whether privacy meaning remains preserved across time and implementation replacement.

## 19. Privacy and Import, Export, and Migration

Privacy and Import, Export, and Migration defines how Privacy Classification is preserved, mapped, reviewed, limited, repaired, or blocked when governed entities move into, out of, or between compliant environments, storage systems, implementations, representations, schemas, vaults, repositories, archives, databases, workflow environments, agent environments, publication environments, backup environments, or tool environments.

This section does not replace the specific export behavior defined in Section 14.

Section 14 defines privacy expectations for export as a distinct operation.

Section 19 defines privacy expectations for movement, mapping, preservation, compatibility, and transition across import, export, and migration together.

Privacy and Import, Export, and Migration exists so that Privacy Classification is not silently discarded, weakened, broadened, collapsed, reinterpreted, declassified, over-classified, under-classified, regenerated, or exposed during movement across systems or contexts.

Import, export, and migration SHALL be governed where privacy affects access, visibility, exposure, publication, synchronization, indexing, backup, restoration, workflow behavior, agent behavior, implementation behavior, validation, compatibility, governance, or downstream use.

Import, export, and migration MAY include:

- importing Knowledge Objects;
- importing Knowledge Records;
- importing Source Material;
- importing Source References;
- importing provenance;
- importing relationships;
- importing metadata;
- importing validation results;
- importing lifecycle state;
- importing Authority Level;
- importing Privacy Classification;
- importing workflow outputs;
- importing agent outputs;
- importing implementation records;
- exporting governed entities;
- exporting governed representations;
- exporting metadata;
- exporting indexes;
- exporting embeddings;
- exporting backups;
- exporting archives;
- migrating between storage systems;
- migrating between implementations;
- migrating between schemas;
- migrating between serialization formats;
- migrating between vaults;
- migrating between repositories;
- migrating between workflow environments;
- migrating between agent environments;
- migrating between indexing systems;
- migrating between backup systems;
- another governed import, export, or migration context.

Import, export, and migration MUST be scoped.

A governed entity may be importable, exportable, or migratable in one context but not another.

A governed entity may be:

- importable for review but not direct use;
- importable as quarantined until privacy is reviewed;
- exportable for migration but not publication;
- exportable as metadata but not full content;
- exportable after redaction but not in full;
- migratable within a private vault but not to a shared environment;
- migratable between governed implementations but not unrestricted tools;
- migratable as a Knowledge Record but not Source Material;
- migratable without agent outputs;
- migratable only with explicit privacy mapping;
- migratable only under a future governed specification.

Import, export, and migration permission MUST NOT be inferred from:

- access permission;
- visibility permission;
- publication permission;
- synchronization permission;
- indexing permission;
- backup permission;
- approval;
- Authority Level;
- Validation State;
- Lifecycle State;
- source reliability;
- source authority;
- source availability;
- relationship existence;
- provenance existence;
- workflow completion;
- agent confidence;
- implementation visibility;
- file existence;
- storage location;
- folder placement;
- filename;
- tag;
- successful prior import;
- successful prior export;
- successful prior migration;
- undocumented convention.

These signals MAY support import, export, or migration review, routing, validation, display, restriction, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Privacy Classification where import, export, or migration affects governed handling or downstream use.

Import MUST preserve Privacy Classification.

An import process MUST NOT silently assign public, internal, private, restricted, confidential, sensitive, exportable, non-exportable, agent-readable, workflow-readable, implementation-visible, publishable, synchronizable, indexable, backup-permitted, or downstream-usable status merely because the imported entity lacks privacy metadata, uses an unfamiliar privacy value, comes from a trusted source, comes from a public source, comes from a private source, appears in a file, appears in a folder, or is technically readable.

Where imported privacy classification is missing, ambiguous, conflicting, unsupported, incompatible, or unknown, the imported entity SHOULD be treated conservatively until reviewed or corrected.

An import process SHOULD preserve the original privacy representation where useful for review, even when the current environment cannot directly map the original value.

Export MUST preserve Privacy Classification.

An export process MUST preserve Privacy Classification, privacy scope, privacy assignment, privacy review context, redaction status, Source Reference limits, provenance limits, relationship limits, lifecycle limits, authority limits, validation limits, synchronization limits, indexing limits, backup limits, workflow limits, agent limits, implementation limits, and downstream-use limits where those limits affect future interpretation or use.

An export process MUST NOT produce an exported artifact that appears less restricted than the source entity unless a governed privacy process explicitly permits that result within a defined scope.

Migration MUST preserve Privacy Classification.

A migration process MUST preserve privacy meaning even when exact field names, metadata formats, schemas, folder structures, application labels, database fields, access-control rules, workflow states, agent states, implementation states, indexing structures, or backup structures differ between environments.

A migration process MAY map privacy values, scopes, fields, structures, or representations only where the mapping preserves privacy meaning or records the limitation for review.

A migration process MUST NOT silently collapse distinct privacy classifications into a single weaker classification where doing so would cause privacy exposure, loss of meaning, broken provenance, relationship failure, source-reference failure, authority ambiguity, lifecycle ambiguity, validation failure, compatibility loss, publication error, synchronization error, indexing exposure, backup exposure, import ambiguity, export ambiguity, governance drift, or implementation lock-in.

Import, export, and migration MUST preserve Object Identity.

Moving a governed entity across systems, formats, environments, or implementations MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Import, export, and migration SHOULD preserve stable Object Identity where doing so is necessary for interpretation, relationship preservation, provenance preservation, lifecycle handling, authority handling, privacy handling, validation, compatibility, or future review.

Where identity mapping is required, privacy handling SHOULD remain conservative until the mapping is validated or reviewed.

Import, export, and migration MUST preserve Source Reference and provenance privacy.

Moving a Knowledge Record MUST NOT automatically move, expose, export, import, migrate, synchronize, index, back up, publish, or agent-process its Source Material, Source References, provenance, extraction history, transformation history, attribution, review history, validation history, import provenance, export provenance, migration provenance, or supporting evidence unless the applicable Privacy Classification permits that behavior.

Import, export, and migration provenance MUST NOT expose restricted source material, restricted users, restricted workflows, restricted agents, restricted implementation details, confidential reasoning, personal information, or sensitive review history unless permitted by the applicable privacy scope.

Import, export, and migration MUST preserve relationship privacy.

Moving a governed entity MUST NOT automatically move, expose, export, import, migrate, synchronize, index, back up, publish, or agent-process its relationships.

Moving a relationship MUST NOT automatically move all connected entities.

Moving connected entities MUST NOT automatically move relationship context, relationship provenance, relationship lifecycle state, relationship authority, relationship validation state, or relationship privacy classification.

A relationship included in an import, export, or migration package may reveal restricted associations, dependencies, identities, source use, decision logic, workflow activity, agent activity, or downstream-use context.

Import, export, and migration MUST preserve Lifecycle State boundaries.

Approval does not automatically make a governed entity importable, exportable, or migratable in every environment.

A draft entity may be importable, exportable, or migratable only within an authorized drafting, review, backup, restoration, or migration scope.

A rejected entity may remain non-exportable or migration-restricted.

An archived entity may be importable, exportable, or migratable only within authorized archival, audit, restoration, or migration scope.

A quarantined entity MUST NOT be imported, exported, or migrated into normal-use, external, public, agent-readable, workflow-readable, implementation-visible, or downstream-use environments unless a governed process explicitly permits that behavior within a defined scope.

Import, export, and migration MUST preserve Authority Level boundaries.

Authority does not grant import, export, or migration permission by itself.

A high-authority entity may be non-exportable or migration-restricted outside its privacy scope.

A low-authority entity may be importable, exportable, or migratable within an authorized scope.

Authority context SHOULD be preserved during import, export, and migration where omission would create misleading interpretation, automation error, validation error, publication error, export error, migration error, or downstream misuse.

Import, export, and migration SHOULD support redaction and minimization.

A governed entity MAY be imported, exported, or migrated through a redacted, summarized, masked, transformed, metadata-only, source-reference-only, relationship-limited, provenance-limited, placeholder, or otherwise constrained representation where full movement would expose restricted information.

A redacted import, export, or migration representation MUST remain distinguishable from the full governed entity.

Import, export, and migration minimization means that a compliant process SHOULD move only the minimum content, metadata, Source References, provenance, relationships, validation results, lifecycle context, authority context, workflow context, agent context, implementation context, indexing context, backup context, or downstream-use context required for the permitted movement purpose.

Import, export, and migration SHOULD support compatibility.

A compliant import, export, or migration process SHOULD identify or support identification of:

- what entity was moved;
- what source environment applied;
- what receiving environment applied;
- what Privacy Classification applied before movement;
- what Privacy Classification applies after movement;
- what privacy scope applied before movement;
- what privacy scope applies after movement;
- what mapping occurred where applicable;
- what was preserved;
- what was transformed;
- what was redacted;
- what was omitted;
- what was restricted;
- what was blocked;
- what requires review;
- what requires repair;
- what provenance supports the movement;
- what Source References, relationships, lifecycle state, Authority Level, Validation State, compatibility limits, workflow behavior, agent behavior, implementation behavior, indexing behavior, backup behavior, synchronization behavior, publication behavior, or downstream-use limits were affected.

Import, export, and migration SHOULD support review.

A reviewer SHOULD be able to determine:

- whether import, export, or migration is permitted;
- what movement scope applies;
- what movement purpose applies;
- what source environment applies;
- what receiving environment applies;
- what representation is permitted;
- whether full movement is permitted;
- whether partial movement is permitted;
- whether redaction is required;
- whether movement is current or historical;
- whether movement is temporary or persistent;
- whether movement requires review;
- whether movement is limited by Source References;
- whether movement is limited by provenance;
- whether movement is limited by relationships;
- whether movement is limited by Lifecycle State;
- whether movement is limited by Authority Level;
- whether movement is limited by Validation State;
- whether movement is limited by compatibility;
- whether movement is limited by access, visibility, publication, synchronization, indexing, backup, restoration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Import, export, and migration SHOULD support validation.

A validator SHOULD be able to determine whether import, export, and migration rules are explicit where required, whether movement scope is compatible with Privacy Classification, whether movement handling preserves Source References and provenance, whether movement handling preserves relationship privacy, whether moved artifacts preserve applicable privacy limits, whether mapping is valid, whether review is required, whether repair is required, and whether movement handling remains compatible across backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, implementation replacement, and downstream use.

Privacy and Import, Export, and Migration is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine whether import, export, or migration is permitted, what representation is permitted, what source and receiving scopes apply, what limits exist, whether redaction is required, whether review is required, whether mapping preserved privacy meaning, whether repair is required, and whether privacy meaning remains preserved across time and implementation replacement.

## 20. Privacy Classification Conformance and Success Criteria

Privacy Classification Conformance and Success Criteria define the minimum expectations a governed entity, process, workflow, agent, validator, storage system, import process, export process, migration process, backup process, synchronization process, indexing system, publication process, implementation, or future specification must satisfy to conform to KS-0008.

Conformance exists so that Privacy Classification remains explicit, scoped, interpretable, portable, reviewable, privacy-preserving, provenance-aware, validatable, compatible, and implementation-independent across time, tools, storage systems, workflows, agents, validators, and implementations.

A governed entity conforms to KS-0008 when it includes or supports Privacy Classification where privacy affects:

- access;
- visibility;
- exposure;
- routing;
- review;
- redaction;
- publication;
- synchronization;
- indexing;
- search;
- summarization;
- embedding;
- export;
- backup;
- restoration;
- import;
- migration;
- agent access;
- workflow access;
- implementation access;
- downstream use;
- Source References;
- provenance;
- relationships;
- lifecycle handling;
- authority handling;
- validation;
- compatibility;
- governance.

Privacy Classification SHALL be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine what privacy handling applies to the governed entity.

A conforming governed entity SHOULD identify or support identification of:

- what Privacy Classification applies;
- what Privacy Scope applies;
- what entity the classification applies to;
- whether the classification is current or historical;
- who or what assigned the classification where applicable;
- when the classification was assigned where applicable;
- what review occurred where applicable;
- what redaction is required where applicable;
- what provenance supports the classification where applicable;
- what Source References affect the classification where applicable;
- what relationships affect the classification where applicable;
- what Lifecycle State affects the classification where applicable;
- what Authority Level affects the classification where applicable;
- what Validation State affects the classification where applicable;
- what access, visibility, publication, synchronization, indexing, export, backup, import, migration, workflow, agent, implementation, or downstream-use limits apply.

A conforming process MUST preserve Privacy Classification when it creates, reads, reviews, validates, routes, modifies, redacts, publishes, synchronizes, indexes, exports, backs up, restores, imports, migrates, archives, repairs, exposes, summarizes, transforms, or otherwise processes a governed entity.

A conforming process MUST NOT silently discard, weaken, broaden, collapse, reinterpret, declassify, over-classify, under-classify, regenerate, hide, bypass, or replace Privacy Classification in a way that causes privacy exposure, loss of meaning, broken provenance, authority ambiguity, lifecycle ambiguity, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, synchronization error, indexing exposure, export exposure, backup exposure, import ambiguity, migration loss, governance drift, or implementation lock-in.

Privacy Classification MUST remain distinguishable from:

- Object Identity;
- Metadata as a whole;
- Privacy Metadata;
- Lifecycle State;
- Authority Level;
- Validation State;
- Provenance;
- Source Reference existence;
- Source Material availability;
- relationship existence;
- relationship privacy;
- access-control settings;
- implementation visibility;
- storage location;
- folder placement;
- filename;
- tags;
- workflow state;
- workflow completion;
- agent state;
- agent confidence;
- publication status;
- synchronization status;
- indexing status;
- export status;
- backup status;
- undocumented convention.

A conforming process MAY use metadata, access-control systems, workflow routing, agent permissions, implementation settings, storage layout, encryption controls, synchronization controls, indexing controls, backup controls, publication settings, validation rules, or user-interface behavior to support Privacy Classification.

Those support mechanisms MUST NOT define or replace Privacy Classification by themselves unless a future governed standard or specification explicitly defines that behavior within a compliant scope.

A conforming process MUST preserve Object Identity.

A Privacy Classification change, privacy review, access change, visibility change, publication change, synchronization change, indexing change, export change, backup change, workflow action, agent action, implementation action, import action, or migration action MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A conforming process MUST preserve Source Reference and provenance privacy.

A Knowledge Record, Source Material item, Source Reference, provenance record, extraction history, transformation history, attribution record, review history, validation history, import provenance, export provenance, migration provenance, workflow history, agent history, or supporting evidence MUST NOT be exposed merely because the related governed entity is accessible, visible, indexed, synchronized, published, exported, backed up, migrated, reviewed, validated, or implementation-readable.

A conforming process MUST preserve relationship privacy.

A governed entity MUST NOT expose, publish, synchronize, index, export, back up, migrate, agent-process, workflow-process, implementation-display, or downstream-use its relationships merely because the entity itself is permitted for one of those actions.

A relationship MUST NOT expose all connected entities merely because the relationship is visible, accessible, synchronized, indexed, exported, backed up, migrated, reviewed, validated, or implementation-readable.

A conforming process MUST preserve Lifecycle State boundaries.

Lifecycle State may affect privacy handling, but Lifecycle State MUST NOT replace Privacy Classification.

Approval does not create public status by itself.

Review does not create publication permission by itself.

Archival does not remove privacy obligations by itself.

Quarantine does not replace Privacy Classification by itself.

A conforming process MUST preserve Authority Level boundaries.

Authority Level may affect review, governance, publication, validation, or downstream use, but Authority Level MUST NOT replace Privacy Classification.

High authority does not create access permission by itself.

High authority does not create publication permission by itself.

High authority does not create export permission by itself.

Low authority does not remove privacy obligations by itself.

A conforming process MUST preserve Validation State boundaries.

Validation may check whether Privacy Classification is present, scoped, compatible, and correctly represented.

Validation MUST NOT publish, expose, synchronize, index, export, back up, declassify, grant access to, or route a governed entity beyond its privacy boundary unless a governed workflow or specification explicitly permits that behavior within a defined scope.

A conforming agent MUST preserve Privacy Classification.

An agent MAY propose Privacy Classification, identify privacy-sensitive content, flag missing classification, recommend review, recommend redaction, detect exposure risk, support validation, or assist privacy-preserving transformation.

An agent MUST NOT become an unreviewable authority for privacy assignment, privacy reduction, privacy escalation, declassification, access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, workflow permission, implementation permission, migration permission, or downstream-use permission where privacy affects governed handling.

A conforming workflow MUST preserve Privacy Classification.

A workflow MAY route, review, validate, approve, reject, restrict, quarantine, redact, publish, synchronize, index, export, import, migrate, back up, restore, archive, repair, or otherwise process a governed entity only within the applicable privacy scope.

Workflow completion MUST NOT create, remove, weaken, expand, reinterpret, transfer, inherit, override, downgrade, upgrade, collapse, or resolve Privacy Classification unless a governed workflow specification explicitly defines that transition within a defined scope.

A conforming implementation MUST preserve Privacy Classification.

An implementation MAY enforce, display, restrict, validate, route, index, synchronize, publish, export, back up, restore, import, migrate, or process Privacy Classification.

An implementation MUST NOT become the source of privacy meaning merely because it can display, hide, cache, index, sync, publish, export, back up, restore, migrate, route, or process a governed entity.

A conforming import, export, or migration process MUST preserve Privacy Classification.

Import, export, and migration processes MUST preserve or explicitly map Privacy Classification, Privacy Scope, Privacy Assignment, Privacy Review context, redaction status, Source Reference limits, provenance limits, relationship limits, lifecycle limits, authority limits, validation limits, workflow limits, agent limits, implementation limits, and downstream-use limits where those limits affect future interpretation or use.

Where privacy classification is missing, ambiguous, conflicting, unsupported, incompatible, or unknown during import, export, or migration, the governed entity SHOULD be treated conservatively until reviewed or corrected.

A conforming backup, restoration, synchronization, indexing, or publication process MUST preserve Privacy Classification.

Backup MUST NOT make a governed entity broadly accessible by itself.

Restoration MUST NOT bypass privacy review where restored exposure would exceed permitted scope.

Synchronization MUST NOT copy a governed entity into a broader environment unless permitted.

Indexing MUST NOT expose restricted information through titles, snippets, summaries, embeddings, caches, search results, graph views, relationship maps, logs, or derived artifacts unless permitted.

Publication MUST NOT expose a governed entity beyond its prior privacy boundary unless publication is permitted within the applicable privacy scope.

A conforming future specification MAY define exact privacy fields, allowed privacy values, privacy scopes, assignment rules, review rules, validation rules, escalation rules, declassification rules, redaction rules, access-control mappings, publication rules, synchronization rules, indexing rules, backup rules, import mappings, export mappings, migration mappings, agent handling rules, workflow triggers, implementation profiles, or serialization syntax.

A future specification is conforming only when it preserves the Privacy Classification behavior defined by KS-0008.

A future specification MUST NOT weaken KS-0008 by making privacy meaning dependent on hidden application state, storage location, folder placement, filename, tag, interface state, workflow memory, agent memory, implementation-specific labels, access-control settings, search ranking, graph position, synchronization state, backup state, publication state, or undocumented convention.

KS-0008 conformance SHOULD support validation.

A validator SHOULD be able to determine whether:

- Privacy Classification is present where required;
- Privacy Scope is clear where needed;
- Privacy Assignment is traceable where needed;
- Privacy Review occurred where required;
- privacy handling is compatible with Object Identity;
- privacy handling is compatible with metadata role boundaries;
- privacy handling is compatible with Source References;
- privacy handling is compatible with provenance;
- privacy handling is compatible with relationships;
- privacy handling is compatible with Lifecycle State;
- privacy handling is compatible with Authority Level;
- privacy handling is compatible with Validation State;
- privacy handling is compatible with access;
- privacy handling is compatible with visibility;
- privacy handling is compatible with publication;
- privacy handling is compatible with synchronization;
- privacy handling is compatible with indexing;
- privacy handling is compatible with export;
- privacy handling is compatible with backup;
- privacy handling is compatible with restoration;
- privacy handling is compatible with import;
- privacy handling is compatible with migration;
- privacy handling is compatible with workflow behavior;
- privacy handling is compatible with agent behavior;
- privacy handling is compatible with implementation behavior;
- privacy handling is compatible with downstream use.

KS-0008 conformance SHOULD support review.

A reviewer SHOULD be able to determine:

- whether Privacy Classification is appropriate;
- whether Privacy Classification is current;
- whether Privacy Scope is sufficient;
- whether classification is over-classified;
- whether classification is under-classified;
- whether redaction is required;
- whether review is required;
- whether repair is required;
- whether privacy meaning changed;
- whether privacy handling was preserved across movement, transformation, validation, workflow activity, agent activity, implementation behavior, publication, synchronization, indexing, export, backup, restoration, import, or migration.

KS-0008 is successful when Privacy Classification remains explicit, scoped, interpretable, portable, traceable, reviewable, privacy-preserving, provenance-aware, validatable, compatible, and implementation-independent across access, visibility, exposure, routing, review, redaction, publication, synchronization, indexing, export, backup, restoration, import, migration, workflow activity, agent activity, validation, storage replacement, and implementation replacement.

KS-0008 is also successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, publication processes, synchronization processes, indexing systems, and implementations can determine:

- what Privacy Classification applies;
- what the Privacy Classification means;
- what Privacy Scope applies;
- who or what assigned the classification where applicable;
- what review occurred where applicable;
- what redaction is required where applicable;
- what limits exist;
- what actions are permitted;
- what actions are prohibited;
- what actions require review;
- what provenance supports privacy handling where needed;
- whether Source References are protected;
- whether provenance is protected;
- whether relationships are protected;
- whether lifecycle boundaries are preserved;
- whether authority boundaries are preserved;
- whether validation boundaries are preserved;
- whether agent boundaries are preserved;
- whether workflow boundaries are preserved;
- whether implementation boundaries are preserved;
- whether movement across systems preserved privacy meaning;
- whether future specifications can add detail without changing the standard-level privacy meaning.

KS-0008 is complete when it provides a stable privacy-classification foundation that later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, privacy vocabularies, access-control specifications, publication specifications, synchronization specifications, indexing specifications, backup specifications, and operational guides can depend on without redefining privacy meaning.
