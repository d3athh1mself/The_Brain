# KS-0006 — Lifecycle State Standard

Document ID: KS-0006
Title: Lifecycle State Standard
Version: 0.1.0
Status: Draft
Created: 2026-06-26
Last Updated: 2026-06-26
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.6 — Lifecycle State Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and lifecycle-state rules are interpreted within KS-0006.

Where conflicts arise between lifecycle state, lifecycle metadata, lifecycle transitions, approval, rejection, deprecation, supersession, archival, restriction, quarantine, validation state, authority, privacy classification, provenance, relationships, source references, storage behavior, agent behavior, workflow behavior, implementation behavior, import behavior, export behavior, migration behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0006 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0006 extends KS-0001 by defining standard-level lifecycle-state behavior for Knowledge Objects, Knowledge Records, Source References, provenance records, relationships, validation results, workflow outputs, agent outputs, imports, exports, migrations, and other governed entities.

KS-0006 depends on KS-0002 because lifecycle state must preserve stable Object Identity across drafting, review, approval, rejection, deprecation, supersession, archival, import, export, migration, validation, and implementation replacement.

KS-0006 depends on KS-0003 because lifecycle meaning may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through metadata.

KS-0006 depends on KS-0004 because relationships may have lifecycle state and because lifecycle transitions may affect relationship interpretation, relationship validity, relationship authority, relationship privacy, relationship provenance, and relationship compatibility.

KS-0006 depends on KS-0005 because lifecycle transitions may require source-reference context, provenance preservation, evidence preservation, attribution preservation, validation history, import provenance, export provenance, migration provenance, and review traceability.

If KS-0006 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

If KS-0006 appears to conflict with KS-0001, the conflict SHOULD be resolved by preserving the Knowledge Object Model defined in KS-0001 while applying KS-0006 as the more specific standard for lifecycle-state behavior.

If KS-0006 appears to conflict with KS-0002, the conflict SHOULD be resolved by preserving stable Object Identity while applying KS-0006 as the more specific standard for lifecycle-state interpretation, transition, review, validation, and compatibility.

If KS-0006 appears to conflict with KS-0003, the conflict SHOULD be resolved by preserving metadata role boundaries while applying KS-0006 as the more specific standard for lifecycle metadata and lifecycle-state behavior.

If KS-0006 appears to conflict with KS-0004, the conflict SHOULD be resolved by preserving relationship behavior while applying KS-0006 as the more specific standard for lifecycle-state behavior.

If KS-0006 appears to conflict with KS-0005, the conflict SHOULD be resolved by preserving source-reference and provenance behavior while applying KS-0006 as the more specific standard for lifecycle-state behavior and lifecycle transitions.

KS-0006 defines lifecycle state at the conceptual standard level.

KS-0006 does not define exact Markdown front matter syntax, exact metadata field names, exact database structures, exact API behavior, exact workflow engine behavior, exact validation tooling, exact implementation-specific status labels, exact user-interface states, exact automation triggers, or exact storage paths.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation profiles, validation specifications, lifecycle vocabularies, transition specifications, and operational documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, Object Identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Lifecycle Transition refers to a governed change from one lifecycle state to another.
- Lifecycle Metadata refers to metadata that records, expresses, supports, validates, or preserves lifecycle state or lifecycle transition context.
- Document Lifecycle State refers to the governance status of a governed document, such as Draft, Review, Approved, Deprecated, Superseded, or Rejected.
- Knowledge Lifecycle State refers to the governed state of a Knowledge Object, Knowledge Record, or related governed entity within the knowledge system.
- Draft refers to a lifecycle state indicating that an entity is being created, revised, prepared, proposed, or otherwise not yet accepted for governed use.
- Review refers to a lifecycle state indicating that an entity is ready for evaluation but has not yet been approved.
- Approved refers to a lifecycle state indicating that an entity has been accepted for use within its stated scope.
- Rejected refers to a lifecycle state indicating that an entity has been reviewed and not accepted.
- Deprecated refers to a lifecycle state indicating that an entity remains historically available but is no longer recommended for future use.
- Superseded refers to a lifecycle state indicating that an entity has been replaced by another governed entity, rule, record, decision, version, or representation.
- Archived refers to a lifecycle state indicating that an entity is preserved for historical, audit, compatibility, migration, governance, or reference purposes but is not treated as active by default.
- Restricted refers to a lifecycle-related handling state indicating that an entity requires constrained access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or workflow handling.
- Quarantined refers to a lifecycle-related handling state indicating that an entity is isolated or withheld from normal use because of unresolved validity, safety, privacy, compatibility, source, provenance, or integrity concerns.
- Pending Review refers to a lifecycle state indicating that human, workflow, validator, or governed review is required before the entity may be treated as reviewed or approved.
- Pending Validation refers to a lifecycle state indicating that validation is required before the entity may be treated as valid for the applicable use.
- Needs Repair refers to a lifecycle state indicating that the entity has known structural, metadata, identity, relationship, provenance, privacy, validation, compatibility, source-reference, migration, import, export, workflow, agent, or implementation issues that require correction.
- Authority Level refers to the governance weight, review status, or interpretive authority assigned to a document, Knowledge Object, Knowledge Record, relationship, source, decision, or governed entity.
- Privacy Classification refers to explicit metadata describing permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.
- Validation refers to the process of checking whether a Knowledge Object, Knowledge Record, relationship, Source Reference, provenance record, metadata record, lifecycle state, transition, or governed entity satisfies the applicable standards, specifications, metadata expectations, provenance expectations, lifecycle expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0006 is to define how Lifecycle State works across The Brain Standard.

KS-0001 establishes Lifecycle State as a required knowledge-level concept where lifecycle status affects interpretation, review, authority, publication, supersession, deprecation, validation, workflow behavior, privacy handling, or downstream use.

KS-0006 defines the standard-level behavior required to create, interpret, preserve, validate, review, transition, migrate, import, export, govern, and maintain lifecycle states.

Lifecycle State exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine how a governed entity should be treated at a given point in time.

KS-0006 exists to prevent lifecycle confusion.

Lifecycle confusion occurs when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, or implementations cannot reliably determine:

- whether an entity is draft, pending review, reviewed, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending validation, needs repair, or governed by another lifecycle state;
- whether an entity may be used for interpretation, publication, export, automation, workflow routing, validation, migration, citation, source support, relationship creation, or downstream use;
- whether a lifecycle state was assigned by a human, workflow, validator, agent, import process, export process, migration process, implementation, or governance decision;
- whether a lifecycle transition has been reviewed, approved, validated, rejected, superseded, deprecated, archived, or restricted;
- whether lifecycle state has been confused with authority, privacy classification, validation state, provenance, workflow state, storage location, implementation status, or user-interface display state.

KS-0006 defines lifecycle-state behavior for:

- Knowledge Objects;
- Knowledge Records;
- Source References;
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
- other governed entities.

KS-0006 does not replace the document lifecycle expectations defined by TB-0003.

TB-0003 defines governance lifecycle states for documents.

KS-0006 defines standard-level lifecycle behavior for knowledge entities and related governed entities, while remaining compatible with TB-0003.

KS-0006 does not define exact metadata field names, exact Markdown front matter syntax, exact database schemas, exact API fields, exact validation tooling, exact workflow procedures, exact automation triggers, exact implementation-specific status values, exact storage paths, or exact user-interface labels.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, lifecycle vocabularies, transition specifications, and operational guides.

KS-0006 defines Lifecycle State at the standard level.

A future specification MAY define exact lifecycle fields, allowed values, transition rules, validation rules, approval rules, rejection rules, deprecation rules, supersession rules, archival rules, restriction rules, quarantine rules, repair rules, workflow triggers, agent handling rules, import mappings, export mappings, migration mappings, or serialization syntax.

Such specifications are valid only when they preserve the lifecycle-state behavior defined by KS-0006.

The primary purpose of KS-0006 is to ensure that lifecycle states remain explicit, interpretable, portable, traceable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent across time, tools, storage systems, workflows, agents, validators, and implementations.

KS-0006 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine:

- what lifecycle state applies to a governed entity;
- what the lifecycle state means;
- who or what assigned the lifecycle state where applicable;
- what lifecycle transition occurred where applicable;
- what provenance supports the lifecycle state or transition;
- whether review, validation, approval, rejection, deprecation, supersession, archival, restriction, quarantine, or repair is required;
- whether the lifecycle state affects authority, privacy, validation, relationships, source references, provenance, compatibility, workflow behavior, agent behavior, implementation behavior, publication, import, export, migration, or downstream use;
- whether lifecycle-state behavior can be preserved without relying on hidden application state, folder placement, filename convention, tag convention, user-interface state, workflow memory, agent memory, implementation-specific status labels, or undocumented practice.

## 2. Relationship to Prior Standards

KS-0006 is subordinate to and derived from the constitutional foundation of The Brain Standard.

KS-0006 depends on:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- KS-0001 — Knowledge Object Model;
- KS-0002 — Object Identity Standard;
- KS-0003 — Metadata Standard;
- KS-0004 — Relationship Standard;
- KS-0005 — Source Reference and Provenance Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

KS-0006 applies that purpose by defining lifecycle-state behavior that remains portable, interpretable, reviewable, privacy-respecting, and independent of any single storage system, workflow engine, agent framework, validation tool, software tool, user interface, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

KS-0006 applies those principles by requiring lifecycle states to preserve:

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

KS-0006 belongs to Layer 1 — Universal Knowledge Standard.

Because lifecycle state affects knowledge meaning, reviewability, authority, validation, privacy handling, provenance, publication, migration, import, export, and downstream use, KS-0006 defines lifecycle-state behavior independently of storage systems, user interfaces, folders, filenames, tags, databases, graph tools, workflow engines, agent systems, validation tools, and implementations.

Layer 2 storage standards depend on KS-0006 because storage must preserve lifecycle state without defining lifecycle meaning.

Layer 3 agent standards depend on KS-0006 because agents may read, propose, classify, validate, route, or update lifecycle-related information without becoming unreviewable authorities.

Layer 4 workflow standards depend on KS-0006 because workflows may create, review, approve, reject, deprecate, supersede, archive, restrict, quarantine, validate, repair, import, export, migrate, or preserve lifecycle states.

Layer 5 implementation documents depend on KS-0006 because implementations must create, read, preserve, display, migrate, export, import, validate, and synchronize lifecycle states without redefining standard-level lifecycle meaning through implementation-specific behavior.

TB-0003 establishes the governance model for The Brain Standard.

KS-0006 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, KS-0006 has high authority within its scope but remains subordinate to constitutional documents.

TB-0003 defines document lifecycle states for governed documents.

KS-0006 does not replace those document lifecycle rules.

KS-0006 extends lifecycle-state behavior across Knowledge Objects, Knowledge Records, Source References, relationships, provenance records, validation results, workflow outputs, agent outputs, imports, exports, migrations, and other governed entities.

KS-0001 defines the foundational Knowledge Object Model.

KS-0006 does not replace the Knowledge Object Model.

KS-0006 refines one part of that model: Lifecycle State.

In practical terms:

- KS-0001 answers: What is a Knowledge Object?
- KS-0001 answers: What is a Knowledge Record?
- KS-0001 answers: Why must Lifecycle State exist?
- KS-0006 answers: How must Lifecycle State behave?
- KS-0006 answers: What makes lifecycle state explicit, interpretable, portable, reviewable, and validatable?
- KS-0006 answers: How should lifecycle transitions be preserved?
- KS-0006 answers: How should draft, review, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending-review, pending-validation, and needs-repair states be treated?

KS-0002 defines Object Identity.

KS-0006 depends on KS-0002 because lifecycle state must not change Object Identity by itself.

A Knowledge Object SHOULD retain its Object Identity when its lifecycle state changes.

A Knowledge Object MUST NOT receive a new Object Identity merely because it becomes draft, pending review, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending validation, or needs repair.

An identity change MAY occur through a governed process where the Knowledge Object becomes a meaningfully different object, but the lifecycle transition alone does not define the identity change.

KS-0003 defines metadata behavior.

KS-0006 depends on KS-0003 because lifecycle state may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through lifecycle metadata.

Lifecycle metadata MUST remain distinguishable from Object Identity, authority metadata, privacy metadata, validation metadata, provenance metadata, relationship metadata, workflow metadata, agent metadata, implementation metadata, storage metadata, and hidden application behavior.

KS-0004 defines relationship behavior.

KS-0006 depends on KS-0004 because relationships may have lifecycle states and because lifecycle transitions may affect relationships.

A deprecated, superseded, rejected, archived, quarantined, or needs-repair entity SHOULD preserve relevant relationships where those relationships remain historically, evidentially, procedurally, or governably important.

A lifecycle transition MUST NOT silently break, reverse, discard, expose, reinterpret, or replace relationships where doing so causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, compatibility loss, import ambiguity, export ambiguity, migration loss, or governance drift.

KS-0005 defines Source Reference and Provenance behavior.

KS-0006 depends on KS-0005 because lifecycle states and lifecycle transitions may require provenance, evidence, attribution, source-reference context, validation history, import provenance, export provenance, migration provenance, and review traceability.

A lifecycle transition SHOULD preserve enough provenance for future review where the transition affects meaning, authority, privacy, validation, source references, relationships, compatibility, workflow behavior, agent behavior, implementation behavior, publication, import, export, migration, or downstream use.

KS-0006 preserves the following KS-0001 rules:

- Lifecycle State describes the current governed state of a Knowledge Object or Knowledge Record.
- Lifecycle State helps determine whether knowledge is proposed, active, under review, approved, deprecated, superseded, rejected, archived, or otherwise governed by future lifecycle rules.
- Lifecycle State SHOULD remain explicit where lifecycle status affects interpretation or use.
- Lifecycle State MUST NOT depend only on folder location, filename, tag, color, user-interface state, plugin field, search ranking, workflow memory, or hidden application state when lifecycle status affects meaning or use.
- Lifecycle State SHOULD remain distinguishable from Authority Level, Validation State, and Privacy Classification.
- Lifecycle transitions SHOULD be traceable when they affect meaning, authority, privacy, validation, relationships, source references, provenance, compatibility, workflow behavior, publication, or downstream use.

KS-0006 preserves the following KS-0002 rules:

- Object Identity remains independent of filenames, folder paths, storage locations, display titles, application-specific identifiers, and implementation-specific behavior.
- Identity changes SHOULD preserve provenance when assignment, preservation, change, merge, split, redirect, import, export, migration, or supersession affects interpretation or compatibility.
- Lifecycle changes MUST NOT silently create identity confusion.

KS-0006 preserves the following KS-0003 rules:

- Lifecycle metadata describes the current governed state of a Knowledge Object, Knowledge Record, relationship, source reference, metadata element, workflow output, agent output, validation result, import, export, migration, or other governed entity where state affects interpretation or handling.
- Lifecycle metadata MUST remain explicit and implementation-independent where lifecycle status affects meaning or use.
- Lifecycle metadata MUST remain distinguishable from authority metadata, privacy metadata, validation metadata, provenance metadata, workflow metadata, agent metadata, and implementation metadata.

KS-0006 preserves the following KS-0004 rules:

- Relationships may have lifecycle state.
- Proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, or needs-review relationships SHOULD remain distinguishable.
- Relationship lifecycle state SHOULD preserve relationship type, direction, provenance, authority, privacy, validation, compatibility, and import/export/migration behavior where those affect interpretation.
- Validation results MUST NOT be silently converted into approval.

KS-0006 preserves the following KS-0005 rules:

- Provenance SHOULD identify review, validation, approval, rejection, deprecation, supersession, migration, import, export, archival, and change context where it affects interpretation.
- Deprecated and superseded material SHOULD remain historically interpretable where it affects source references, provenance, evidence, attribution, validation, authority, privacy, lifecycle state, compatibility, governance, migration, import, export, restoration, synchronization, publication, or downstream use.
- A lifecycle transition SHOULD preserve provenance where it affects governance, compatibility, validation, migration, import, export, publication, or downstream use.
- Privacy boundaries MUST be preserved during lifecycle handling.

KS-0006 is successful when it extends the prior standards into a clear lifecycle-state model without weakening Object Identity, metadata role boundaries, relationship behavior, source-reference behavior, provenance preservation, authority expectations, privacy boundaries, validation expectations, implementation independence, or practical daily usability.

## 3. Lifecycle State Definition

Lifecycle State is the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, metadata record, validation result, workflow output, agent output, import record, export record, migration record, document, decision, or other governed entity within The Brain Standard.

Lifecycle State exists to describe how an entity should be interpreted, reviewed, used, preserved, routed, validated, published, restricted, repaired, superseded, deprecated, archived, imported, exported, migrated, or withheld at a given point in time.

Lifecycle State SHALL be explicit when lifecycle status affects:

- knowledge meaning;
- reviewability;
- approval;
- rejection;
- deprecation;
- supersession;
- archival;
- restriction;
- quarantine;
- repair;
- validation;
- authority;
- privacy handling;
- source references;
- provenance;
- relationships;
- compatibility;
- workflow behavior;
- agent behavior;
- implementation behavior;
- publication;
- import;
- export;
- migration;
- downstream use.

Lifecycle State MUST remain distinguishable from Object Identity.

A Knowledge Object remains the same Knowledge Object when its lifecycle state changes unless a governed identity decision determines that the object itself has become meaningfully different.

Lifecycle State MUST remain distinguishable from Authority Level.

Lifecycle State describes current governed state.

Authority Level describes governance weight, interpretive authority, or approved use.

An entity may be approved but low-authority.

An entity may be high-authority but superseded.

An entity may be restricted but approved.

An entity may be structurally valid but not authoritative.

Lifecycle State MUST remain distinguishable from Validation State.

Lifecycle State describes review, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, or other governed status.

Validation State describes whether an entity satisfies applicable structural, metadata, identity, provenance, relationship, privacy, authority, compatibility, lifecycle, source-reference, workflow, agent, implementation, import, export, or migration expectations.

An approved entity may later fail validation.

A validation-passing entity may still require review.

A validation result MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that behavior.

Lifecycle State MUST remain distinguishable from Privacy Classification.

Lifecycle State describes governed status.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.

An approved entity may be restricted.

A rejected entity may still contain restricted information.

An archived entity may still require privacy protection.

Lifecycle State MUST remain distinguishable from Provenance.

Lifecycle State describes current governed state.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context.

A lifecycle state SHOULD preserve provenance when that state or transition affects interpretation, authority, privacy, validation, relationships, source references, compatibility, publication, import, export, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Lifecycle State MUST remain distinguishable from Workflow State.

Workflow State describes where an entity is inside a workflow.

Lifecycle State describes the governed status of the entity.

A workflow may route an entity through a review step without making the entity approved.

A workflow may complete successfully without making an entity approved unless a governed workflow specification explicitly defines that behavior.

Lifecycle State MUST remain distinguishable from Agent State.

Agent State describes agent processing, agent output, agent confidence, agent task completion, agent review, or agent-generated classification.

Lifecycle State describes the governed status of the entity.

An agent may propose a lifecycle state.

An agent MUST NOT become an unreviewable authority for lifecycle transitions where human review, governance, privacy, authority, validation, publication, or downstream use is affected.

Lifecycle State MUST remain distinguishable from Implementation State.

Implementation State describes how a specific application, vault, database, interface, plugin, workflow system, file system, or tool represents, displays, indexes, hides, locks, routes, syncs, publishes, archives, or caches an entity.

Implementation State MAY support lifecycle handling.

Implementation State MUST NOT define lifecycle meaning by itself when lifecycle state affects governed interpretation or use.

Lifecycle State MUST NOT depend only on:

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
- workflow memory;
- agent memory;
- implementation-specific status label;
- undocumented convention.

These signals MAY support usability, discovery, routing, display, validation, search, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit governed lifecycle state where lifecycle status affects meaning, authority, privacy, validation, relationships, source references, provenance, compatibility, publication, import, export, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Lifecycle State SHOULD be portable.

A lifecycle state SHOULD remain meaningful when an entity is renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, reindexed, summarized, translated, validated, processed by an agent, processed by a workflow, archived, restricted, repaired, or accessed through a different implementation.

Lifecycle State SHOULD be reviewable.

A future human, agent, workflow, validator, storage system, migration process, import process, export process, or implementation SHOULD be able to determine what lifecycle state applies, what the state means, how it was assigned where applicable, whether transition provenance exists where needed, and whether the state affects downstream use.

Lifecycle State SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, or archive process MUST NOT silently discard, collapse, rename, reinterpret, expose, replace, promote, demote, or regenerate Lifecycle State in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, migration loss, import ambiguity, export ambiguity, publication error, workflow error, agent error, governance drift, or implementation lock-in.

Lifecycle State is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine what governed state applies to an entity, how that state should affect interpretation and handling, what provenance supports the state where needed, whether review or validation is required, whether authority or privacy is affected, and whether the state remains meaningful across time and implementation replacement.

## 4. Lifecycle State Requirements

Lifecycle State Requirements define the minimum behavior required for lifecycle state to be valid, interpretable, reviewable, portable, and governable under KS-0006.

A governed entity SHALL include or support Lifecycle State where lifecycle status affects meaning, review, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, validation, authority, privacy, provenance, relationships, source references, compatibility, workflow behavior, agent behavior, implementation behavior, publication, import, export, migration, or downstream use.

A governed entity MAY include:

- a Knowledge Object;
- a Knowledge Record;
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

Lifecycle State SHALL be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine how the entity should be interpreted and handled.

Lifecycle State MUST NOT depend only on hidden implementation behavior, storage location, folder placement, filename, tag, color, icon, user-interface state, workflow memory, agent memory, plugin behavior, database state, search ranking, graph position, backlink behavior, or undocumented convention.

Those signals MAY support discovery, navigation, routing, display, validation, automation, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit lifecycle state when lifecycle status affects governed meaning or use.

A lifecycle state SHOULD identify or support identification of:

- what entity the lifecycle state applies to;
- what lifecycle state applies;
- whether the state is current or historical;
- who or what assigned the state where applicable;
- when the state was assigned where applicable;
- what lifecycle transition occurred where applicable;
- what provenance supports the state or transition where applicable;
- whether review is required;
- whether validation is required;
- whether approval is required;
- whether restriction, quarantine, repair, archival, deprecation, rejection, or supersession applies;
- whether the state affects authority, privacy, relationships, source references, provenance, compatibility, publication, import, export, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Lifecycle State MUST remain distinguishable from Object Identity.

A lifecycle state change MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when it moves from Draft to Review, Review to Approved, Approved to Deprecated, Approved to Superseded, Review to Rejected, Approved to Archived, or any other governed lifecycle transition unless a separate governed identity decision determines that the object has become meaningfully different.

Lifecycle State MUST remain distinguishable from Authority Level.

Approval MAY affect authority, but lifecycle state and authority are not the same concept.

A governed entity MAY be:

- approved but low-authority;
- high-authority but superseded;
- approved for a narrow scope but not authoritative for broader use;
- rejected but historically preserved;
- archived but still authoritative for historical interpretation;
- deprecated but still relevant for migration or compatibility review.

Lifecycle State MUST remain distinguishable from Privacy Classification.

A lifecycle state MUST NOT weaken privacy requirements.

A governed entity MAY be draft and restricted, approved and restricted, rejected and sensitive, archived and confidential, superseded and private, or deprecated and non-exportable.

Privacy Classification SHALL take precedence over operational convenience when lifecycle handling creates privacy risk.

Lifecycle State MUST remain distinguishable from Validation State.

Validation MAY support lifecycle transitions, but validation does not equal approval unless a future governed workflow or specification explicitly defines that behavior.

A governed entity MAY be structurally valid but not approved.

A governed entity MAY be approved but later fail validation because of a changed standard, changed specification, broken relationship, missing source reference, privacy issue, migration issue, or implementation incompatibility.

A validation result MUST NOT silently promote, demote, approve, reject, deprecate, supersede, archive, restrict, quarantine, or repair a governed entity unless a future governed workflow or specification explicitly permits that behavior.

Lifecycle State MUST remain distinguishable from Provenance.

Lifecycle State describes the governed status of an entity.

Provenance explains origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context.

Lifecycle State SHOULD preserve provenance when lifecycle status or lifecycle transition affects meaning, authority, privacy, validation, relationships, source references, compatibility, workflow behavior, agent behavior, implementation behavior, publication, import, export, migration, or downstream use.

Lifecycle State MUST remain distinguishable from Relationship State.

A Knowledge Object, Knowledge Record, Source Reference, provenance record, or other governed entity may have one lifecycle state while its relationships have separate lifecycle states.

A relationship MAY be proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, quarantined, pending validation, or needs repair independently of the lifecycle state of the entities it connects.

A lifecycle transition affecting a governed entity SHOULD preserve, update, review, deprecate, supersede, archive, quarantine, or repair affected relationships where relationship meaning, provenance, authority, privacy, validation, compatibility, import, export, migration, or downstream use is affected.

Lifecycle State MUST remain distinguishable from Workflow State.

A workflow step MAY create, propose, review, validate, route, or request a lifecycle transition.

A workflow step MUST NOT be treated as a lifecycle transition unless the transition is explicitly represented or governed.

Workflow completion MUST NOT be treated as approval unless a future governed workflow specification explicitly defines that behavior.

Lifecycle State MUST remain distinguishable from Agent State.

An agent MAY propose, classify, validate, flag, route, or recommend a lifecycle state.

An agent-generated lifecycle recommendation MUST remain reviewable where lifecycle status affects meaning, authority, privacy, validation, publication, export, migration, governance, or downstream use.

An agent MUST NOT become an unreviewable authority for approval, rejection, deprecation, supersession, archival, restriction, quarantine, or repair.

Lifecycle State MUST remain distinguishable from Implementation State.

An implementation MAY display, sort, filter, lock, hide, route, index, synchronize, archive, or cache an entity according to lifecycle state.

Implementation behavior MUST NOT define lifecycle meaning by itself.

A compliant implementation MUST NOT silently convert implementation state into governed lifecycle state where that conversion affects meaning, authority, privacy, validation, relationships, source references, provenance, compatibility, publication, import, export, migration, workflow behavior, agent behavior, or downstream use.

Lifecycle State SHOULD support historical preservation.

A rejected, deprecated, superseded, archived, quarantined, or repaired entity MAY remain historically useful.

Historical preservation does not mean the entity remains current, approved, authoritative, valid, public, exportable, or safe for downstream use.

Lifecycle State SHOULD make current use and historical status distinguishable.

Lifecycle State SHOULD support review.

A reviewer SHOULD be able to determine:

- what lifecycle state applies;
- whether the state is appropriate;
- whether the state was assigned through a governed process where required;
- whether review, approval, validation, restriction, quarantine, repair, deprecation, supersession, or archival is required;
- whether affected relationships, source references, provenance, metadata, authority, privacy, compatibility, import, export, migration, workflow behavior, agent behavior, or implementation behavior require update.

Lifecycle State SHOULD support validation.

A validator SHOULD be able to determine whether:

- lifecycle state is present where required;
- lifecycle state uses a governed value where a governed vocabulary exists;
- lifecycle state is distinguishable from authority, privacy, validation, provenance, workflow state, agent state, implementation state, and storage state;
- lifecycle transitions preserve required provenance;
- lifecycle state is compatible with Object Identity;
- lifecycle state is compatible with relationships;
- lifecycle state preserves privacy boundaries;
- lifecycle state remains portable across import, export, migration, backup, restoration, synchronization, and implementation replacement.

Lifecycle State SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, or regenerate lifecycle state in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Lifecycle State Requirements are successful when lifecycle state remains explicit, distinguishable, reviewable, portable, privacy-respecting, validatable, and compatible across drafting, review, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, import, export, migration, workflow activity, agent activity, validation, storage replacement, and implementation replacement.

