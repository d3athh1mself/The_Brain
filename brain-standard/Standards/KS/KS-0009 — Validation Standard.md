# KS-0009 — Validation Standard

Document ID: KS-0009
Title: Validation Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-27
Last Updated: 2026-06-27
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.9 — Validation Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and validation rules are interpreted within KS-0009.

Where conflicts arise between Validation, Validation State, validation results, validation scope, validation assignment, validation review, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, storage behavior, agent behavior, workflow behavior, implementation behavior, import behavior, export behavior, migration behavior, backup behavior, synchronization behavior, indexing behavior, publication behavior, downstream use, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0009 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0009 extends KS-0001 by defining standard-level Validation behavior for Knowledge Objects, Knowledge Records, Source References, provenance records, relationships, metadata records, lifecycle states, authority levels, privacy classifications, workflow outputs, agent outputs, imports, exports, migrations, governed documents where applicable, decisions, and other governed entities.

KS-0009 depends on KS-0002 because validation must preserve stable Object Identity across review, repair, import, export, migration, synchronization, backup, indexing, publication, and implementation replacement.

KS-0009 depends on KS-0003 because validation meaning may be expressed, described, reviewed, migrated, imported, exported, governed, or preserved through metadata.

KS-0009 depends on KS-0004 because relationships may require validation and because validation must preserve relationship meaning, direction, participants, provenance, authority, privacy, lifecycle state, compatibility, and implementation independence.

KS-0009 depends on KS-0005 because Source References, provenance, evidence, attribution, source availability, source reliability, source authority, source privacy, import provenance, export provenance, migration provenance, and review history may require validation or support validation.

KS-0009 depends on KS-0006 because Lifecycle State may require validation, but Lifecycle State does not replace Validation State.

KS-0009 depends on KS-0007 because Authority Level may require validation, but Authority Level does not replace Validation State.

KS-0009 depends on KS-0008 because Privacy Classification may require validation, but Privacy Classification does not replace Validation State.

If KS-0009 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

KS-0009 defines Validation at the conceptual standard level.

KS-0009 does not define exact Markdown front matter syntax, exact metadata field names, exact validation values, exact validation rule syntax, exact validation tooling, exact validator implementations, exact schemas, exact APIs, exact error codes, exact warning formats, exact test runners, exact automation triggers, exact workflow procedures, exact storage paths, exact user-interface behavior, or exact implementation-specific validation labels.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, validator profiles, schema specifications, conformance test suites, and operational guides.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, Object Identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Validation refers to the process of checking whether a governed entity satisfies applicable standards, specifications, metadata expectations, identity expectations, relationship expectations, source-reference expectations, provenance expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, workflow expectations, agent expectations, implementation expectations, import expectations, export expectations, or migration expectations.
- Validation State refers to the current validation status of a governed entity within a defined validation scope.
- Validation Result refers to the recorded outcome of a validation process.
- Validation Scope refers to the defined context, rule set, standard, specification, workflow, implementation profile, object type, migration process, import process, export process, or downstream-use context being validated.
- Validation Assignment refers to the act of assigning, proposing, confirming, revising, limiting, removing, or preserving Validation State for a governed entity.
- Validation Review refers to the review process used to determine whether a validation result is appropriate, complete, current, traceable, compatible, and safe for downstream use.
- Validator refers to a human, agent, workflow, tool, implementation, script, specification, process, or governed mechanism that performs or supports validation.
- Human Validation refers to validation performed, reviewed, corrected, approved, rejected, or confirmed by a human.
- Agent-Generated Validation refers to validation performed, proposed, enriched, classified, checked, or reported by an agent.
- Workflow-Generated Validation refers to validation performed, routed, recorded, reviewed, approved, rejected, or preserved through a governed workflow.
- Implementation Validation refers to validation performed or displayed by a software tool, vault, database, file system, interface, plugin, automation, or service.
- Structural Validation refers to validation of required structure, sections, object form, record form, field presence, document organization, or representation expectations.
- Identity Validation refers to validation of Object Identity, stable identifiers, alternate identifiers, legacy identifiers, temporary identifiers, source identifiers, duplicate handling, merge behavior, split behavior, supersession, redirects, or identity-change records.
- Metadata Validation refers to validation of required, recommended, optional, standard, implementation, workflow, agent, provenance, relationship, lifecycle, authority, privacy, validation, compatibility, import, export, or migration metadata.
- Relationship Validation refers to validation of relationship participants, relationship type, direction, context, strength, confidence, provenance, lifecycle state, authority, privacy, compatibility, and implementation independence.
- Source Reference Validation refers to validation of Source References, Source Material connections, evidence support, source availability, source reliability, source authority, source privacy, citation support, or source-reference compatibility.
- Provenance Validation refers to validation of origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, attribution, or change context.
- Lifecycle Validation refers to validation of Lifecycle State, lifecycle transitions, lifecycle metadata, review requirements, approval requirements, rejection handling, deprecation, supersession, archival, restriction, quarantine, repair, or historical preservation.
- Authority Validation refers to validation of Authority Level, authority scope, authority assignment, authority review, source authority, relationship authority, use-authority, trust boundaries, or downstream-use authority.
- Privacy Validation refers to validation of Privacy Classification, privacy scope, privacy assignment, privacy review, access expectations, visibility expectations, publication expectations, synchronization expectations, indexing expectations, export expectations, backup expectations, agent access, workflow access, implementation access, or downstream-use handling.
- Compatibility Validation refers to validation of whether a governed entity remains meaningful, portable, reviewable, privacy-respecting, provenance-preserving, importable, exportable, migratable, and implementation-independent across time and tool replacement.
- Import Validation refers to validation performed when governed entities are brought into a compliant environment.
- Export Validation refers to validation performed when governed entities are produced from a compliant environment for use elsewhere.
- Migration Validation refers to validation performed when governed entities move between storage systems, implementations, representations, schemas, vaults, repositories, file formats, workflow environments, or tool environments.
- Validation Error refers to a validation finding that indicates a governed entity does not satisfy a mandatory requirement within the applicable validation scope.
- Validation Warning refers to a validation finding that indicates a potential issue, risk, incompleteness, ambiguity, inconsistency, or recommended improvement without necessarily making the governed entity invalid.
- Validation Evidence refers to the source, rule, test, standard, specification, workflow output, agent output, human review, implementation check, or provenance that supports a validation result.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0009 is to define how Validation works across The Brain Standard.

KS-0001 establishes Validation as a required knowledge-level concept where structural correctness, metadata completeness, Object Identity, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, workflow behavior, agent behavior, implementation behavior, import behavior, export behavior, migration behavior, or downstream use affects whether a governed entity can be interpreted, reviewed, preserved, processed, published, synchronized, indexed, exported, backed up, migrated, or used safely.

KS-0009 defines the standard-level behavior required to create, interpret, preserve, review, assign, revise, migrate, import, export, govern, and maintain Validation State and validation results.

Validation exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine whether governed entities satisfy applicable standards, specifications, expectations, and compatibility requirements.

KS-0009 exists to prevent validation confusion.

Validation confusion occurs when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, or implementations cannot reliably determine:

- whether a governed entity satisfies the applicable standard or specification;
- what validation scope applies;
- what validation result applies;
- who or what performed validation where applicable;
- whether validation was performed by a human, agent, workflow, validator, implementation, import process, export process, migration process, or other governed mechanism;
- whether the validation result is current, historical, partial, complete, failed, passed, warning-only, superseded, stale, disputed, or requires review;
- whether validation depends on Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, workflow behavior, agent behavior, implementation behavior, import behavior, export behavior, migration behavior, or downstream-use context;
- whether validation has been confused with approval, authority, privacy permission, lifecycle state, workflow completion, agent confidence, implementation visibility, source reliability, publication status, export permission, synchronization permission, indexing permission, backup permission, or downstream-use permission.

KS-0009 defines Validation behavior for:

- Knowledge Objects;
- Knowledge Records;
- Source References;
- Source Material where applicable;
- provenance records;
- relationships;
- metadata records;
- lifecycle states;
- authority levels;
- privacy classifications;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- governed documents where applicable;
- decisions;
- other governed entities.

KS-0009 does not define exact metadata field names, exact Markdown front matter syntax, exact validation values, exact validation rule syntax, exact schemas, exact database structures, exact API fields, exact validator tooling, exact automation triggers, exact workflow procedures, exact agent validation formats, exact implementation-specific labels, exact storage paths, exact publication procedures, exact synchronization procedures, exact indexing procedures, exact backup procedures, or exact user-interface behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, schema specifications, validator profiles, conformance test suites, and operational guides.

KS-0009 defines Validation at the standard level.

A future specification MAY define exact validation fields, allowed validation states, validation scopes, validation rule sets, validation profiles, validation evidence formats, error formats, warning formats, validator responsibilities, conformance tests, import validation rules, export validation rules, migration validation rules, backup validation rules, synchronization validation rules, indexing validation rules, publication validation rules, agent handling rules, workflow triggers, implementation mappings, or serialization syntax.

Such specifications are valid only when they preserve the Validation behavior defined by KS-0009.

The primary purpose of KS-0009 is to ensure that Validation remains explicit, scoped, interpretable, portable, traceable, reviewable, privacy-respecting, provenance-aware, compatible, and implementation-independent across time, tools, storage systems, workflows, agents, validators, and implementations.

KS-0009 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine:

- what Validation State applies to a governed entity;
- what the Validation State means;
- what validation scope applies;
- what validation result applies;
- who or what performed validation where applicable;
- what rule, standard, specification, workflow, implementation profile, import process, export process, migration process, or compatibility expectation was used;
- what evidence supports the validation result;
- whether validation is current, stale, partial, failed, passed, warning-only, disputed, superseded, or requires review;
- whether validation affects interpretation, review, lifecycle handling, authority handling, privacy handling, relationships, Source References, provenance, compatibility, workflow behavior, agent behavior, implementation behavior, publication, synchronization, indexing, backup, import, export, migration, or downstream use;
- whether validation behavior can be preserved without relying on hidden application state, folder placement, filename convention, tag convention, user-interface state, workflow memory, agent memory, implementation-specific labels, search ranking, graph centrality, backlink behavior, publication status, or undocumented practice.

## 2. Relationship to Prior Standards

KS-0009 is subordinate to and derived from the constitutional foundation of The Brain Standard.

KS-0009 depends on:

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
- KS-0008 — Privacy Classification Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

KS-0009 applies that purpose by defining Validation behavior that remains portable, interpretable, reviewable, privacy-respecting, provenance-aware, compatible, and independent of any single storage system, workflow engine, agent framework, validation tool, schema language, software tool, user interface, indexing system, backup process, synchronization process, publication process, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

KS-0009 applies those principles by requiring Validation to preserve:

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

KS-0009 belongs to Layer 1 — Universal Knowledge Standard.

Because Validation affects whether governed entities satisfy knowledge-level expectations, KS-0009 defines Validation independently of storage systems, user interfaces, folders, filenames, tags, databases, graph tools, workflow engines, agent systems, validator tools, indexing tools, synchronization tools, backup tools, publication tools, and implementations.

Layer 2 storage standards depend on KS-0009 because storage must preserve validation-relevant information without defining validation meaning.

Layer 3 agent standards depend on KS-0009 because agents may read, propose, perform, report, classify, compare, or repair validation-related information without becoming unreviewable authorities over validation outcomes.

Layer 4 workflow standards depend on KS-0009 because workflows may create, route, review, approve, reject, escalate, repair, preserve, import, export, migrate, or act on validation results.

Layer 5 implementation documents depend on KS-0009 because implementations must create, read, preserve, display, validate, synchronize, index, back up, export, import, migrate, and report validation information without redefining standard-level validation meaning through implementation-specific behavior.

TB-0003 establishes the governance model for The Brain Standard.

KS-0009 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, KS-0009 has high authority within its scope but remains subordinate to constitutional documents.

KS-0001 defines the foundational Knowledge Object Model.

KS-0009 does not replace the Knowledge Object Model.

KS-0009 refines one part of that model: Validation.

In practical terms:

- KS-0001 answers: What is a Knowledge Object?
- KS-0001 answers: What is a Knowledge Record?
- KS-0001 answers: Why must Validation exist where structure, metadata, provenance, relationships, lifecycle, authority, privacy, compatibility, or downstream use affects interpretation?
- KS-0009 answers: How must Validation behave?
- KS-0009 answers: What makes Validation explicit, scoped, traceable, reviewable, portable, privacy-respecting, provenance-aware, compatible, and implementation-independent?
- KS-0009 answers: How should validation results, validation scope, validation assignment, validation review, validation errors, validation warnings, validator behavior, import validation, export validation, migration validation, and conformance be treated?

KS-0002 defines Object Identity.

KS-0009 depends on KS-0002 because Validation must not change Object Identity by itself.

A Knowledge Object SHOULD retain its Object Identity when its Validation State changes.

A Knowledge Object MUST NOT receive a new Object Identity merely because it passes validation, fails validation, receives warnings, requires repair, becomes partially valid, becomes stale, is revalidated, is validated by a different validator, is validated under a different scope, or is validated under a newer standard or specification.

An identity change MAY occur through a governed process where the Knowledge Object becomes a meaningfully different object, but the validation result alone does not define the identity change.

KS-0003 defines metadata behavior.

KS-0009 depends on KS-0003 because Validation may be expressed, described, reviewed, migrated, imported, exported, governed, or preserved through validation metadata.

Validation metadata MUST remain distinguishable from Object Identity, descriptive metadata, structural metadata, provenance metadata, relationship metadata, lifecycle metadata, authority metadata, privacy metadata, compatibility metadata, workflow metadata, agent metadata, implementation metadata, storage metadata, and hidden application behavior.

KS-0004 defines relationship behavior.

KS-0009 depends on KS-0004 because relationships may require Validation and because validation may depend on relationship participants, relationship type, direction, context, provenance, lifecycle state, authority, privacy, compatibility, and implementation independence.

A relationship MAY pass validation under one validation scope and fail validation under another.

A relationship MUST NOT be treated as valid merely because it exists, is linked, appears in backlinks, appears central in a graph, appears frequently in search results, was inferred by an agent, was created by a workflow, or is supported by an implementation-specific link.

KS-0005 defines Source Reference and Provenance behavior.

KS-0009 depends on KS-0005 because Source References, Source Material, evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, validation history, import provenance, export provenance, migration provenance, and review traceability may require Validation or support validation results.

A Source Reference MAY support validation.

Provenance MAY support validation.

Evidence MAY support validation.

However, Source Reference existence, provenance existence, source availability, source reliability, source authority, evidence availability, citation existence, or attribution MUST NOT automatically create validation success unless a governed validation scope explicitly defines that requirement.

KS-0006 defines Lifecycle State behavior.

KS-0009 depends on KS-0006 because Lifecycle State may affect validation requirements, validation timing, validation review, validation repair, lifecycle transition checks, import review, export review, migration review, publication readiness, archival handling, restriction handling, quarantine handling, and downstream use.

Lifecycle State MUST remain distinguishable from Validation State.

A lifecycle state may require validation, but it does not replace validation meaning.

An entity may be:

- draft and structurally valid;
- draft and invalid;
- approved and later invalid;
- rejected but still valid as a historical record;
- deprecated and valid for compatibility review;
- superseded and valid for historical interpretation;
- archived and valid for preservation;
- quarantined because validation failed;
- pending validation but otherwise reviewable;
- needs repair but still privacy-protected.

KS-0007 defines Authority Level behavior.

KS-0009 depends on KS-0007 because Authority Level may affect validation expectations, validation review, downstream use, publication readiness, import review, export review, migration review, and governance interpretation.

Authority Level MUST remain distinguishable from Validation State.

Validation success does not automatically create Authority Level.

A governed entity may be:

- valid but low-authority;
- valid but non-authoritative;
- invalid but based on a high-authority source;
- authoritative but stale under a newer validation scope;
- high-authority but privacy-restricted;
- validated for structure but not validated for authority;
- validated for metadata but not validated for downstream use.

KS-0008 defines Privacy Classification behavior.

KS-0009 depends on KS-0008 because Privacy Classification may require validation and because validation activity must preserve privacy boundaries.

Privacy Classification MUST remain distinguishable from Validation State.

Validation success does not automatically create access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission.

A governed entity may be:

- valid and confidential;
- valid and non-exportable;
- valid and agent-restricted;
- invalid and public;
- invalid and sensitive;
- structurally valid but privacy-invalid;
- privacy-valid but relationship-invalid;
- export-valid but not publication-valid.

KS-0009 preserves the following KS-0001 rules:

- Knowledge Objects and Knowledge Records must remain interpretable through explicit identity, metadata, relationships, provenance, lifecycle state, authority, privacy classification, validation expectations, and governed structure.
- Validation expectations SHOULD be present or supported where validation affects interpretation, use, compatibility, automation, import, export, migration, publication, or downstream use.
- Knowledge Objects and Knowledge Records MUST remain implementation-independent, portable, reviewable, and interpretable by humans and AI systems.

KS-0009 preserves the following KS-0002 rules:

- Object Identity remains independent of filenames, folder paths, storage locations, display titles, application-specific identifiers, and implementation-specific behavior.
- Validation changes MUST NOT silently create identity confusion.
- Identity decisions SHOULD preserve provenance when assignment, preservation, change, merge, split, redirect, import, export, migration, or supersession affects interpretation or compatibility.

KS-0009 preserves the following KS-0003 rules:

- Validation metadata describes whether a Knowledge Object, Knowledge Record, or governed entity satisfies applicable expectations.
- Metadata MUST remain explicit, portable, inspectable, reviewable, privacy-respecting, validatable, compatible, governed, maintainable, and implementation-independent.
- Metadata MUST NOT allow workflows, agents, storage systems, or implementations to redefine Knowledge Object meaning by accident.

KS-0009 preserves the following KS-0004 rules:

- Relationships may require validation.
- Relationship validation SHOULD preserve relationship type, direction, participants, provenance, authority, privacy, lifecycle state, compatibility, and implementation independence.
- Agent-generated or workflow-generated relationships SHOULD remain reviewable where they affect meaning, provenance, authority, privacy, lifecycle state, validation, publication, or downstream use.

KS-0009 preserves the following KS-0005 rules:

- Source References and provenance SHOULD preserve evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, validation history, import provenance, export provenance, migration provenance, and review traceability where those affect interpretation.
- Source Material and Knowledge Records SHALL remain distinguishable.
- Provenance MAY support validation but does not replace validation.
- Privacy boundaries MUST be preserved when source-reference or provenance information affects validation.

KS-0009 preserves the following KS-0006 rules:

- Lifecycle State MUST remain distinguishable from Validation State.
- Validation MAY support lifecycle transitions, but validation does not equal approval unless a future governed workflow or specification explicitly defines that behavior.
- A validation result MUST NOT silently promote, demote, approve, reject, deprecate, supersede, archive, restrict, quarantine, or repair a governed entity unless a future governed workflow or specification explicitly permits that behavior.

KS-0009 preserves the following KS-0007 rules:

- Authority Level MUST remain distinguishable from Validation State.
- Validation success MUST NOT imply authority.
- Agent confidence MUST NOT imply authority.
- Workflow completion MUST NOT imply authority unless a governed workflow specification explicitly defines that result.
- Implementation visibility MUST NOT imply authority.

KS-0009 preserves the following KS-0008 rules:

- Privacy Classification MUST remain distinguishable from Validation State.
- Validation does not create export permission by itself.
- Validation does not create publication permission by itself.
- Privacy Classification SHALL take precedence over operational convenience where privacy and convenience conflict.
- Privacy boundaries MUST be preserved during validation, repair, import, export, migration, indexing, synchronization, backup, publication, workflow activity, agent activity, and implementation behavior.

KS-0009 is successful when it extends the prior standards into a clear Validation model without weakening Object Identity, metadata role boundaries, relationship behavior, source-reference behavior, provenance preservation, lifecycle meaning, authority expectations, privacy boundaries, implementation independence, compatibility, or practical daily usability.

## 3. Validation Definition

Validation is the process of checking whether a governed entity satisfies applicable standards, specifications, metadata expectations, identity expectations, relationship expectations, source-reference expectations, provenance expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, workflow expectations, agent expectations, implementation expectations, import expectations, export expectations, migration expectations, or downstream-use expectations within a defined validation scope.

Validation exists to determine whether a governed entity conforms to the requirements that apply to it.

Validation does not define the entity by itself.

Validation does not create Object Identity.

Validation does not replace Metadata.

Validation does not create a relationship.

Validation does not create Source References.

Validation does not replace Provenance.

Validation does not define Lifecycle State.

Validation does not create Authority Level.

Validation does not create Privacy Classification.

Validation does not guarantee publication readiness.

Validation does not guarantee export permission.

Validation does not guarantee synchronization permission.

Validation does not guarantee indexing permission.

Validation does not guarantee backup permission.

Validation does not guarantee agent-use permission.

Validation does not guarantee workflow-use permission.

Validation does not guarantee implementation-use permission.

Validation does not guarantee downstream-use permission.

Validation SHALL be explicit when validation affects:

- interpretation;
- structure;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- compatibility;
- review;
- repair;
- import;
- export;
- migration;
- backup;
- restoration;
- synchronization;
- indexing;
- publication;
- agent behavior;
- workflow behavior;
- implementation behavior;
- downstream use;
- governance.

Validation MUST be scoped.

A Validation State or Validation Result is meaningful only within the validation scope that produced it.

Validation Scope MAY include:

- a standard;
- a specification;
- an object type;
- a record type;
- a metadata profile;
- a relationship profile;
- a source-reference profile;
- a provenance expectation;
- a lifecycle expectation;
- an authority expectation;
- a privacy expectation;
- a compatibility expectation;
- an import process;
- an export process;
- a migration process;
- a backup process;
- a restoration process;
- a synchronization process;
- an indexing process;
- a publication process;
- an agent profile;
- a workflow profile;
- an implementation profile;
- a downstream-use context;
- another governed validation context.

A governed entity MAY pass validation under one scope and fail validation under another.

A Knowledge Record may be structurally valid but fail privacy validation.

A relationship may be valid for internal use but invalid for export.

A Source Reference may be valid for traceability but invalid for publication.

A metadata record may pass field-presence validation but fail compatibility validation.

A migrated entity may pass import validation but fail full conformance validation.

An agent output may pass format validation but fail authority, provenance, or privacy validation.

A workflow output may pass workflow validation but still require human review.

Validation MUST remain distinguishable from approval.

Approval means a governed entity has been accepted for use within a defined scope.

Validation means a governed entity satisfies applicable checks within a defined validation scope.

A valid entity may still require review.

A valid entity may still lack authority.

A valid entity may still be private, confidential, sensitive, non-exportable, agent-restricted, workflow-restricted, implementation-restricted, or publication-restricted.

An invalid entity may still need preservation for provenance, audit, review, repair, compatibility, migration, or governance history.

Validation MUST remain distinguishable from Authority Level.

Authority Level describes governance weight, interpretive authority, review weight, trust boundary, or use-authority within a defined scope.

Validation describes whether applicable requirements have been satisfied within a defined validation scope.

A valid record is not automatically authoritative.

A high-authority record may fail validation under a newer standard, specification, implementation profile, import process, export process, migration process, or compatibility expectation.

Validation MUST remain distinguishable from Lifecycle State.

Lifecycle State describes the governed state of an entity.

Validation describes whether the entity satisfies applicable checks.

A draft entity may be valid.

An approved entity may become invalid.

A rejected entity may remain valid as a historical record.

A deprecated entity may remain valid for compatibility.

A superseded entity may remain valid for historical interpretation.

A quarantined entity may be quarantined because validation failed.

Validation MUST remain distinguishable from Privacy Classification.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling.

Validation describes whether privacy expectations, along with other applicable expectations, have been satisfied within a defined validation scope.

A privacy-valid entity may still be restricted.

A validation-passing entity may still be confidential.

A validation-passing entity may still be non-exportable.

A validation-passing entity may still be agent-restricted.

Validation MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context.

Validation may require provenance.

Validation may produce provenance.

Validation may depend on provenance.

However, provenance does not replace validation.

A governed entity with complete provenance may still fail validation.

A governed entity with incomplete provenance may pass a limited validation scope while still requiring provenance repair.

Validation MUST remain distinguishable from workflow completion.

A workflow may perform validation.

A workflow may route validation.

A workflow may record validation.

A workflow may require validation before transition, publication, export, migration, synchronization, indexing, backup, repair, or downstream use.

Workflow completion MUST NOT be treated as validation success unless a future governed workflow specification explicitly defines that behavior.

Validation MUST remain distinguishable from agent confidence.

An agent may propose a validation result.

An agent may perform validation checks.

An agent may identify validation errors or warnings.

An agent may recommend repair.

Agent confidence MUST NOT be treated as validation success unless a future governed agent standard, workflow standard, validation specification, or implementation profile explicitly defines that behavior within a controlled scope.

Validation MUST remain distinguishable from implementation behavior.

An implementation may display, cache, index, filter, sort, route, synchronize, export, import, migrate, back up, restore, publish, or report validation information.

Implementation behavior MUST NOT define validation meaning by itself.

A validator tool, plugin, script, database rule, graph engine, search index, interface state, file path, tag, color, dashboard, or hidden application state MUST NOT become the sole source of validation meaning where validation affects governed interpretation, authority, privacy, lifecycle handling, compatibility, publication, import, export, migration, or downstream use.

Validation SHOULD be traceable.

A validation result SHOULD identify or support identification of:

- what governed entity was validated;
- what validation scope applied;
- what standard, specification, rule set, profile, workflow, agent, implementation, import process, export process, migration process, or downstream-use context was used;
- what validator performed or supported validation where applicable;
- when validation occurred where applicable;
- what result was produced;
- what errors were found;
- what warnings were found;
- what evidence supports the result;
- what repair remains required;
- what review remains required;
- what compatibility limits remain;
- what privacy limits remain;
- what downstream-use limits remain.

Validation SHOULD be reviewable.

A future human, agent, workflow, validator, storage system, migration process, import process, export process, backup process, synchronization process, indexing system, publication process, or implementation SHOULD be able to determine what validation was performed, what scope applied, what result was produced, whether the result is current, whether the result is limited, whether the result is disputed, whether repair is required, and whether the result affects downstream use.

Validation SHOULD be portable.

Validation meaning SHOULD remain understandable when a governed entity is renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, reindexed, summarized, transformed, translated, validated by a different validator, processed by an agent, processed by a workflow, or accessed through a different implementation.

Validation SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, publication process, or downstream-use process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, or regenerate validation information in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, lifecycle confusion, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Validation is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what validation applies to a governed entity, what scope was used, what result was produced, what evidence supports the result, what repair or review remains, and whether the validation remains meaningful across time and implementation replacement.

## 4. Validation Requirements

Validation Requirements define the minimum behavior required for Validation to remain meaningful, scoped, traceable, reviewable, portable, privacy-respecting, provenance-aware, compatible, and implementation-independent under KS-0009.

A governed entity SHALL include or support Validation where validation affects meaning, interpretation, review, repair, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, import, export, migration, backup, restoration, synchronization, indexing, publication, workflow behavior, agent behavior, implementation behavior, or downstream use.

A governed entity MAY include:

- a Knowledge Object;
- a Knowledge Record;
- Source Material where applicable;
- a Source Reference;
- a provenance record;
- a relationship;
- a metadata record;
- a lifecycle state;
- an authority level;
- a privacy classification;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Validation SHALL be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine whether the governed entity satisfies the applicable expectations within the applicable validation scope.

Validation MUST NOT depend only on hidden implementation behavior, storage location, folder placement, filename, tag, color, icon, dashboard state, user-interface state, workflow memory, agent memory, plugin behavior, database state, search ranking, graph position, backlink behavior, validator cache, or undocumented convention.

Those signals MAY support discovery, navigation, routing, display, validation assistance, automation, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit validation where validation affects governed meaning or downstream use.

A Validation State SHOULD identify or support identification of:

- what governed entity the Validation State applies to;
- what validation scope applies;
- what validation result applies;
- whether validation passed, failed, partially passed, produced warnings, requires repair, requires review, is stale, is disputed, or is superseded;
- who or what performed validation where applicable;
- when validation was performed where applicable;
- what standard, specification, rule set, workflow, agent, implementation profile, import process, export process, migration process, or downstream-use context was used;
- what validation evidence supports the result;
- what validation errors exist;
- what validation warnings exist;
- what repair remains required;
- what review remains required;
- whether the result is current or historical;
- whether the result affects lifecycle handling, authority handling, privacy handling, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Validation MUST be scoped.

A Validation State without a known or inferable validation scope is incomplete where the result affects governed interpretation, review, repair, compatibility, publication, export, migration, automation, or downstream use.

A validation result MAY be valid for one scope and invalid for another.

A governed entity MUST NOT be treated as universally valid merely because it passed one validation scope.

Validation MUST remain distinguishable from Object Identity.

A validation change MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Validation MUST remain distinguishable from Metadata.

Validation metadata may record validation meaning.

Validation metadata does not replace the validation process, validation scope, validation result, validation evidence, or validation review where those are required.

Validation MUST remain distinguishable from Relationships.

A valid relationship does not make every connected entity valid.

A valid entity does not make all of its relationships valid.

Validation MUST remain distinguishable from Source References and Provenance.

A Source Reference, citation, evidence item, attribution note, or provenance record MAY support validation.

It MUST NOT be treated as validation success unless the applicable validation scope explicitly defines that requirement.

Validation MUST remain distinguishable from Lifecycle State.

A lifecycle state MAY require validation.

Validation does not equal approval, rejection, deprecation, supersession, archival, restriction, quarantine, or repair unless a future governed workflow or specification explicitly defines that behavior within a controlled scope.

Validation MUST remain distinguishable from Authority Level.

Validation success MUST NOT imply authority.

Authority Level MAY require validation support, but validation does not create governance weight, interpretive authority, review weight, trust boundary, or use-authority by itself.

Validation MUST remain distinguishable from Privacy Classification.

Validation success MUST NOT weaken privacy requirements.

A governed entity MAY pass validation and still remain private, confidential, sensitive, restricted, non-exportable, non-publishable, agent-restricted, workflow-restricted, implementation-restricted, or downstream-use restricted.

Privacy Classification SHALL take precedence over operational convenience when validation activity creates privacy risk.

Validation MUST remain distinguishable from Workflow State.

A workflow step MAY perform, request, route, or record validation.

Workflow completion MUST NOT be treated as validation success unless a future governed workflow specification explicitly defines that behavior.

Validation MUST remain distinguishable from Agent State.

An agent MAY propose, perform, classify, report, or recommend validation results.

An agent-generated validation result MUST remain reviewable where validation affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Validation MUST remain distinguishable from Implementation State.

An implementation MAY display, sort, filter, cache, index, synchronize, export, import, migrate, back up, restore, publish, or report validation information.

Implementation behavior MUST NOT define validation meaning by itself.

Validation SHOULD support repair.

A validation result SHOULD make clear whether repair is required, what issue requires repair where practical, what standard or expectation was not satisfied, and whether the repair requires human review, agent assistance, workflow routing, provenance preservation, privacy review, compatibility review, migration review, or governance action.

Validation SHOULD support review.

A reviewer SHOULD be able to determine whether:

- validation was performed under the correct scope;
- validation evidence is sufficient;
- validation errors are accurate;
- validation warnings are useful;
- validation results are current;
- validation repair is required;
- validation results were created by a human, agent, workflow, implementation, import process, export process, migration process, or other validator;
- privacy boundaries were preserved;
- lifecycle, authority, relationship, Source Reference, provenance, compatibility, and downstream-use effects were considered where applicable.

Validation SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, publication process, or downstream-use process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, or regenerate Validation State or validation results in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, lifecycle confusion, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Validation Requirements are successful when Validation remains explicit, scoped, distinguishable, traceable, reviewable, repair-supporting, portable, privacy-respecting, provenance-aware, compatible, and implementation-independent across validation activity, repair, review, import, export, migration, backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, storage replacement, and implementation replacement.

## 5. Validation Categories

Validation Categories organize validation by architectural purpose.

Validation Categories help humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations understand what kind of validation is being performed and what expectations are being checked.

KS-0009 defines Validation Categories at the conceptual standard level.

KS-0009 does not define an exhaustive controlled vocabulary of exact validation states, exact validation values, exact error codes, exact warning codes, exact rule syntax, exact schema syntax, exact validator tools, or exact conformance test suites.

A future validation specification MAY define exact validation states, allowed values, validation profiles, validation rule sets, validation evidence formats, error formats, warning formats, validator responsibilities, conformance checks, import validation rules, export validation rules, migration validation rules, publication validation rules, synchronization validation rules, indexing validation rules, backup validation rules, agent handling rules, workflow triggers, implementation mappings, and serialization syntax.

At minimum, The Brain Standard recognizes the following Validation Categories:

- structural validation;
- identity validation;
- metadata validation;
- relationship validation;
- source-reference validation;
- provenance validation;
- lifecycle validation;
- authority validation;
- privacy validation;
- compatibility validation;
- workflow validation;
- agent validation;
- implementation validation;
- import, export, and migration validation;
- conformance validation.

### 5.1 Structural Validation

Structural Validation checks whether a governed entity has the required form, organization, sections, records, fields, boundaries, or representation expected by the applicable standard, specification, workflow, implementation profile, or object type.

Structural Validation MAY check whether required headings exist, required sections are present, required records are complete, required fields are supported, required boundaries are clear, and required structural expectations are satisfied.

Structural Validation MUST NOT be treated as full conformance unless the validation scope explicitly includes all other required validation categories.

### 5.2 Identity Validation

Identity Validation checks whether Object Identity, stable identifiers, alternate identifiers, legacy identifiers, temporary identifiers, source identifiers, duplicate handling, merge behavior, split behavior, supersession, redirects, or identity-change records satisfy applicable identity expectations.

Identity Validation MUST preserve the Object Identity rules defined by KS-0002.

A governed entity MUST NOT be treated as identity-valid merely because its filename, folder path, title, tag, database row, interface label, link, search result, or implementation-specific identifier appears correct.

### 5.3 Metadata Validation

Metadata Validation checks whether metadata required or recommended by the applicable standard, specification, workflow, implementation profile, import process, export process, migration process, or downstream-use context is present, explicit, interpretable, portable, reviewable, privacy-respecting, compatible, and distinguishable from hidden implementation behavior.

Metadata Validation MAY check required metadata, recommended metadata, metadata categories, metadata role boundaries, metadata consistency, metadata completeness, metadata portability, metadata privacy, metadata provenance, metadata compatibility, and metadata preservation.

Metadata Validation MUST preserve the metadata role boundaries defined by KS-0003.

### 5.4 Relationship Validation

Relationship Validation checks whether relationships satisfy applicable expectations for participants, relationship type, direction, context, strength, confidence, provenance, lifecycle state, authority, privacy, compatibility, and implementation independence.

Relationship Validation MUST preserve the relationship behavior defined by KS-0004.

A relationship MUST NOT be treated as valid merely because an implementation displays a link, backlink, graph edge, database relation, search association, vector similarity, or plugin connection.

### 5.5 Source-Reference Validation

Source-Reference Validation checks whether Source References, Source Material connections, evidence support, source availability, source reliability, source authority, source privacy, citation support, source identifiers, and source-reference compatibility satisfy applicable expectations.

Source-Reference Validation MUST preserve the Source Reference behavior defined by KS-0005.

A citation MAY support a Source Reference, but citation syntax does not define Source Reference validity by itself unless a governed validation scope explicitly requires that citation format.

### 5.6 Provenance Validation

Provenance Validation checks whether origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, attribution, or change context is sufficiently preserved for the applicable scope.

Provenance Validation MUST preserve provenance meaning across review, repair, lifecycle transitions, authority review, privacy review, relationship handling, import, export, migration, publication, synchronization, indexing, backup, workflow activity, agent activity, and implementation replacement.

A governed entity with provenance may still fail validation if the provenance is incomplete, inconsistent, stale, unclear, privacy-exposing, incompatible, or insufficient for the validation scope.

### 5.7 Lifecycle Validation

Lifecycle Validation checks whether Lifecycle State, lifecycle transitions, lifecycle metadata, review requirements, approval requirements, rejection handling, deprecation, supersession, archival, restriction, quarantine, repair, historical preservation, and transition provenance satisfy applicable lifecycle expectations.

Lifecycle Validation MUST preserve the lifecycle-state behavior defined by KS-0006.

Lifecycle Validation does not approve a governed entity by itself unless a future governed workflow or specification explicitly defines that behavior.

### 5.8 Authority Validation

Authority Validation checks whether Authority Level, authority scope, authority assignment, authority review, source authority, relationship authority, use-authority, trust boundaries, and downstream-use authority satisfy applicable authority expectations.

Authority Validation MUST preserve the authority-level behavior defined by KS-0007.

Authority Validation does not create Authority Level by itself.

### 5.9 Privacy Validation

Privacy Validation checks whether Privacy Classification, privacy scope, privacy assignment, privacy review, access expectations, visibility expectations, publication expectations, synchronization expectations, indexing expectations, export expectations, backup expectations, agent access, workflow access, implementation access, and downstream-use handling satisfy applicable privacy expectations.

Privacy Validation MUST preserve the privacy-classification behavior defined by KS-0008.

Privacy Validation does not create access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission by itself.

### 5.10 Compatibility Validation

Compatibility Validation checks whether a governed entity remains meaningful, portable, reviewable, privacy-respecting, provenance-preserving, importable, exportable, migratable, restorable, synchronizable, indexable where permitted, publishable where permitted, and implementation-independent across time and tool replacement.

Compatibility Validation MAY check whether a governed entity can survive renaming, movement, copying, backup, restoration, synchronization, indexing, migration, import, export, implementation replacement, workflow activity, agent activity, validator changes, standard revisions, or specification revisions without losing governed meaning.

Compatibility Validation MUST NOT permit compatibility convenience to override privacy, provenance, authority, lifecycle, validation, relationship, source-reference, identity, or governance requirements.

### 5.11 Workflow Validation

Workflow Validation checks whether workflow outputs, workflow transitions, workflow routing, workflow-generated metadata, workflow-generated provenance, workflow-generated relationships, workflow review, workflow repair, workflow approval, workflow rejection, workflow import activity, workflow export activity, workflow migration activity, or workflow publication activity satisfy applicable workflow expectations.

Workflow Validation MUST NOT treat workflow completion as validation success unless the applicable workflow specification explicitly defines that behavior.

Workflow Validation MUST preserve reviewability, traceability, privacy, authority boundaries, lifecycle boundaries, and implementation independence.

### 5.12 Agent Validation

Agent Validation checks whether agent outputs, agent-generated metadata, agent-generated relationships, agent-generated provenance, agent-generated validation results, agent confidence, agent recommendations, agent repair proposals, agent access, agent restrictions, or agent task outcomes satisfy applicable agent expectations.

Agent Validation MUST NOT treat agent confidence as validation success unless a future governed agent standard, workflow standard, validation specification, or implementation profile explicitly defines that behavior within a controlled scope.

Agent Validation MUST preserve human reviewability where validation affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

### 5.13 Implementation Validation

Implementation Validation checks whether a software tool, vault, database, file system, interface, plugin, automation, service, or reference implementation preserves validation meaning without redefining it through implementation-specific behavior.

Implementation Validation MAY check whether implementation behavior preserves Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, compatibility, import behavior, export behavior, migration behavior, backup behavior, synchronization behavior, indexing behavior, publication behavior, workflow behavior, and agent behavior.

Implementation Validation MUST NOT allow user-interface display, plugin behavior, database state, folder placement, filename convention, graph layout, search index, cache, or hidden application state to become the sole source of validation meaning.

### 5.14 Import, Export, and Migration Validation

Import, Export, and Migration Validation checks whether governed entities remain meaningful, portable, traceable, reviewable, privacy-respecting, provenance-aware, compatible, and implementation-independent when brought into a compliant environment, produced from a compliant environment, or moved between systems.

This category MAY check import mapping, export mapping, migration mapping, identifier preservation, metadata preservation, relationship preservation, source-reference preservation, provenance preservation, lifecycle preservation, authority preservation, privacy preservation, validation-history preservation, compatibility preservation, and repair requirements.

Import success, export success, or migration success MUST NOT be treated as full validation success unless the applicable validation scope explicitly defines that behavior.

### 5.15 Conformance Validation

Conformance Validation checks whether a governed entity, document, standard, specification, workflow, agent, storage system, implementation, import process, export process, migration process, or downstream-use process satisfies the requirements required for conformance within a defined scope.

Conformance Validation MAY include multiple validation categories.

Conformance Validation MUST define what conformance scope applies.

A system, file, object, record, workflow, agent, or implementation MUST NOT claim full conformance merely because it passes a narrow validation check.

## 6. Validation Scope

Validation Scope defines the context in which Validation is performed and interpreted.

A Validation State or Validation Result is meaningful only within a Validation Scope.

Validation Scope identifies what expectations are being checked, which governed entity is being checked, what rule set applies, what level of completeness is expected, and what downstream use the validation result may support.

Validation Scope SHALL be explicit where validation affects meaning, review, repair, lifecycle handling, authority handling, privacy handling, relationships, Source References, provenance, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

A Validation Scope MAY be defined by:

- a constitutional document;
- a standard;
- a specification;
- an object type;
- a record type;
- a metadata profile;
- a relationship profile;
- a source-reference profile;
- a provenance expectation;
- a lifecycle expectation;
- an authority expectation;
- a privacy expectation;
- a compatibility expectation;
- a workflow standard;
- an agent standard;
- a storage standard;
- an implementation document;
- an import process;
- an export process;
- a migration process;
- a backup process;
- a restoration process;
- a synchronization process;
- an indexing process;
- a publication process;
- a downstream-use context;
- another governed validation context.

A governed entity MAY have multiple Validation Scopes.

A Knowledge Record may require one scope for structure, another scope for metadata, another scope for Source References, another scope for privacy, another scope for export, and another scope for publication.

A relationship may require one scope for internal use, another scope for source support, another scope for privacy, another scope for migration, and another scope for publication.

An implementation may require one scope for reference implementation conformance, another scope for storage compatibility, another scope for privacy preservation, another scope for synchronization, and another scope for export.

Validation Scope MUST be distinguishable from Validation State.

Validation Scope defines what is being checked.

Validation State describes the current validation status within that scope.

Validation Scope MUST be distinguishable from Validation Result.

Validation Scope defines the context of the check.

Validation Result records the outcome of the check.

Validation Scope MUST be distinguishable from Lifecycle State.

A lifecycle state may require a validation scope, but the lifecycle state does not define validation meaning by itself.

Validation Scope MUST be distinguishable from Authority Scope.

Authority Scope defines where Authority Level applies.

Validation Scope defines what expectations are being checked.

Validation may support authority review, but validation scope does not create authority scope by itself.

Validation Scope MUST be distinguishable from Privacy Scope.

Privacy Scope defines where Privacy Classification applies.

Validation Scope defines what privacy or non-privacy expectations are being checked.

A privacy validation scope may determine whether privacy expectations are satisfied, but it does not create privacy permission by itself.

Validation Scope SHOULD be narrow enough to be meaningful and broad enough to support the intended use.

A validation scope that is too broad may hide incomplete checks.

A validation scope that is too narrow may create false confidence.

A validation scope that is undefined may create validation confusion.

A validation result SHOULD NOT be reused outside its validation scope unless a governed standard, specification, workflow, implementation profile, or compatibility review explicitly permits that reuse.

Validation Scope SHOULD support traceability.

A reviewer SHOULD be able to determine what validation scope applied, why that scope was used, what rule set or expectation was checked, whether the scope was complete for the intended use, whether additional scopes are required, and whether the validation result may be reused.

Validation Scope SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, publication process, or downstream-use process MUST NOT silently change, collapse, generalize, expand, narrow, discard, or reinterpret validation scope in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, lifecycle confusion, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Validation Scope is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what was checked, why it was checked, what rule set applied, what result was produced, whether the result is reusable, and whether additional validation is required.

## 7. Validation Assignment

Validation Assignment is the act of assigning, proposing, confirming, revising, limiting, removing, preserving, or recording Validation State for a governed entity within a defined Validation Scope.

Validation Assignment exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what validation status applies, who or what assigned it where applicable, what scope it applies within, and whether it remains current, reviewable, portable, and safe for downstream use.

Validation Assignment MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- Source Material where applicable;
- a Source Reference;
- a provenance record;
- a relationship;
- a metadata record;
- a lifecycle state;
- an authority level;
- a privacy classification;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Validation Assignment SHALL be explicit where validation status affects meaning, review, repair, lifecycle handling, authority handling, privacy handling, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

A Validation Assignment SHOULD identify or support identification of:

- what governed entity the assignment applies to;
- what Validation State is assigned;
- what Validation Scope applies;
- what Validation Result supports the assignment where applicable;
- who or what assigned, proposed, confirmed, revised, limited, removed, or preserved the Validation State where applicable;
- when the assignment occurred where applicable;
- what standard, specification, rule set, workflow, agent, implementation profile, import process, export process, migration process, or downstream-use context was used;
- what validation evidence supports the assignment;
- whether the assignment is current or historical;
- whether the assignment is complete, partial, disputed, stale, superseded, warning-only, failed, passed, or requires review;
- whether repair remains required;
- whether review remains required;
- whether lifecycle, authority, privacy, relationship, Source Reference, provenance, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow, agent, implementation, or downstream-use effects exist.

Validation Assignment MUST be scoped.

A Validation Assignment without a known or inferable Validation Scope is incomplete where the assignment affects governed interpretation, repair, compatibility, publication, export, migration, automation, or downstream use.

Validation Assignment MUST remain distinguishable from Validation Scope.

Validation Scope defines what expectations are being checked.

Validation Assignment records, proposes, confirms, revises, limits, removes, or preserves the Validation State within that scope.

Validation Assignment MUST remain distinguishable from Validation Review.

Validation Assignment records or changes validation status.

Validation Review evaluates whether the assignment is appropriate, supported, current, traceable, compatible, and safe for use.

Validation Assignment MUST remain distinguishable from Object Identity.

A Validation Assignment MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when a Validation Assignment changes unless a separate governed identity decision determines that the object itself has become meaningfully different.

Validation Assignment MUST remain distinguishable from Metadata.

Validation metadata may record Validation Assignment.

Metadata storage does not make a Validation Assignment valid unless the assignment is explicit, scoped, interpretable, portable, reviewable, privacy-respecting, and governed by the applicable standard or specification.

Validation Assignment MUST remain distinguishable from Lifecycle State.

Assigning a Validation State MUST NOT automatically approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, or otherwise transition Lifecycle State unless a future governed workflow or specification explicitly defines that behavior within a controlled scope.

Validation Assignment MUST remain distinguishable from Authority Level.

Assigning a passing Validation State MUST NOT assign Authority Level by itself.

Assigning a failed Validation State MUST NOT remove historical authority by itself.

Authority changes require a governed authority process where authority is affected.

Validation Assignment MUST remain distinguishable from Privacy Classification.

Assigning a passing Validation State MUST NOT create access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission.

A Validation Assignment MUST preserve privacy boundaries where validation information, validation evidence, validation errors, validation warnings, or repair instructions expose restricted information.

Validation Assignment MAY be performed or proposed by:

- a human;
- an agent;
- a workflow;
- a validator;
- a storage system;
- an implementation;
- an import process;
- an export process;
- a migration process;
- a backup process;
- a restoration process;
- a synchronization process;
- an indexing process;
- a publication process;
- another governed mechanism.

Human Validation Assignment MAY assign, confirm, reject, revise, limit, or remove Validation State according to the applicable governance, workflow, review, or validation expectations.

Agent-generated Validation Assignment MAY propose, classify, check, enrich, or report Validation State.

Agent-generated Validation Assignment MUST remain reviewable where validation affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Workflow-generated Validation Assignment MAY route, record, preserve, approve for workflow purposes, reject for workflow purposes, or escalate Validation State according to the applicable workflow rules.

Workflow-generated Validation Assignment MUST NOT be treated as human approval unless a future governed workflow specification explicitly defines that behavior.

Implementation-generated Validation Assignment MAY support usability, automation, reporting, dashboards, filtering, indexing, synchronization, backup, import, export, migration, or publication workflows.

Implementation-generated Validation Assignment MUST NOT define validation meaning by itself.

A validator MAY assign Validation State within the scope it is authorized or configured to evaluate.

A validator MUST NOT imply broader validation success than the evaluated Validation Scope supports.

A validator MUST NOT claim full conformance when only structural, metadata, identity, relationship, privacy, import, export, migration, workflow, agent, implementation, or another narrow validation category was evaluated.

Validation Assignment SHOULD preserve provenance.

A Validation Assignment SHOULD preserve enough provenance for future review where the assignment affects meaning, authority, privacy, lifecycle handling, relationships, Source References, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation Assignment SHOULD support revision.

A Validation Assignment MAY be revised when:

- the governed entity changes;
- the applicable standard changes;
- the applicable specification changes;
- the validation scope changes;
- the validator changes;
- validation evidence changes;
- validation errors are repaired;
- validation warnings are resolved;
- provenance is corrected;
- privacy classification changes;
- lifecycle state changes;
- authority level changes;
- relationships change;
- Source References change;
- import context changes;
- export context changes;
- migration context changes;
- implementation behavior changes;
- compatibility expectations change;
- downstream-use expectations change.

A revised Validation Assignment SHOULD preserve prior validation history where prior results remain relevant for provenance, audit, compatibility, governance, migration, import, export, publication, repair, or downstream interpretation.

Validation Assignment SHOULD support removal or limitation.

A Validation Assignment MAY be removed, limited, suspended, superseded, or marked stale when it is no longer current, no longer supported, no longer scoped correctly, no longer compatible, no longer safe for downstream use, or no longer valid under the applicable standard or specification.

Removing or limiting a Validation Assignment MUST NOT silently delete historical validation information where that information remains relevant for provenance, audit, governance, compatibility, migration, import, export, repair, publication, or downstream interpretation.

Validation Assignment SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, publication process, or downstream-use process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, or regenerate Validation Assignment in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, lifecycle confusion, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Validation Assignment is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what Validation State was assigned, what scope it applies within, who or what assigned it where applicable, what evidence supports it, whether it remains current, whether review or repair remains required, and whether the assignment remains meaningful across time and implementation replacement.

## 8. Validation Review

Validation Review is the review process used to determine whether a Validation State, Validation Result, Validation Assignment, validation error, validation warning, validation evidence, validator output, repair recommendation, conformance claim, or validation-related decision is appropriate, complete, current, traceable, compatible, privacy-respecting, provenance-aware, and safe for downstream use.

Validation Review exists so that validation outcomes do not become unreviewable facts merely because a human, agent, workflow, tool, validator, implementation, import process, export process, migration process, or automation produced them.

Validation Review MAY apply to:

- a Validation State;
- a Validation Result;
- a Validation Assignment;
- a validation scope;
- a validation error;
- a validation warning;
- validation evidence;
- validation metadata;
- validator output;
- repair recommendations;
- conformance claims;
- import validation;
- export validation;
- migration validation;
- backup validation;
- restoration validation;
- synchronization validation;
- indexing validation;
- publication validation;
- workflow validation;
- agent validation;
- implementation validation;
- downstream-use validation.

Validation Review SHALL be available where validation affects meaning, authority, privacy, lifecycle handling, publication, synchronization, indexing, backup, export, migration, governance, or downstream use.

Validation Review SHOULD be performed or required when:

- validation scope is unclear;
- validation results conflict;
- validation evidence is incomplete;
- validation errors appear inaccurate;
- validation warnings appear misleading;
- validation results are stale;
- validation results are disputed;
- validation was generated by an agent;
- validation was generated by an implementation;
- validation was generated by a workflow without human review;
- validation affects privacy-sensitive information;
- validation affects authority;
- validation affects lifecycle transitions;
- validation affects publication;
- validation affects export;
- validation affects migration;
- validation affects downstream use;
- validation affects conformance claims;
- validation repair may alter governed meaning.

Validation Review SHOULD determine whether:

- the correct Validation Scope was used;
- the applicable standard or specification was used;
- the validator was appropriate for the scope;
- the validation result is complete;
- the validation result is current;
- the validation result is partial;
- the validation result is stale;
- the validation result is disputed;
- validation evidence is sufficient;
- validation errors are accurate;
- validation warnings are useful;
- repair recommendations are appropriate;
- privacy boundaries were preserved;
- provenance was preserved;
- relationships were preserved;
- Source References were preserved;
- Object Identity was preserved;
- Lifecycle State was not silently changed;
- Authority Level was not silently assigned;
- Privacy Classification was not weakened;
- workflow completion was not confused with validation success;
- agent confidence was not confused with validation success;
- implementation visibility was not confused with validation success;
- conformance was not overstated;
- downstream-use limits remain clear.

Validation Review MUST remain distinguishable from Validation Assignment.

Validation Assignment records, proposes, confirms, revises, limits, removes, or preserves Validation State.

Validation Review evaluates whether that assignment or result is appropriate and usable within its scope.

Validation Review MUST remain distinguishable from approval.

Validation Review MAY support approval where a governed workflow or specification defines that relationship.

Validation Review does not approve a governed entity by itself unless a future governed workflow or specification explicitly defines that behavior.

Validation Review MUST remain distinguishable from Authority Review.

Authority Review evaluates Authority Level, authority scope, use-authority, governance weight, interpretive authority, trust boundaries, and downstream-use authority.

Validation Review evaluates validation meaning, validation scope, validation evidence, validation errors, validation warnings, and validation results.

Validation Review MAY support Authority Review, but it does not create Authority Level by itself.

Validation Review MUST remain distinguishable from Privacy Review.

Privacy Review evaluates Privacy Classification, privacy scope, access expectations, visibility expectations, publication expectations, synchronization expectations, indexing expectations, export expectations, backup expectations, agent access, workflow access, implementation access, and downstream-use handling.

Validation Review may evaluate whether privacy requirements were checked correctly, but it does not create privacy permission by itself.

Validation Review MUST remain distinguishable from Lifecycle Review.

Lifecycle Review evaluates lifecycle state, lifecycle transitions, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, and historical preservation.

Validation Review may support lifecycle decisions, but it does not silently change Lifecycle State.

Validation Review MUST remain distinguishable from implementation behavior.

A dashboard, status icon, plugin check, database rule, search result, graph display, validator cache, report view, or implementation label MUST NOT replace Validation Review where validation affects governed meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Validation Review MAY be performed by:

- a human;
- a governed workflow;
- a validator;
- an agent operating within review boundaries;
- an implementation operating within a governed profile;
- an import process;
- an export process;
- a migration process;
- another governed review mechanism.

Human Validation Review SHOULD be required where validation affects approval, authority, privacy-sensitive exposure, publication, export, migration, governance, or high-impact downstream use.

Agent-assisted Validation Review MAY support review by identifying errors, warnings, missing evidence, stale results, inconsistent scopes, privacy risks, authority risks, lifecycle risks, relationship risks, source-reference risks, provenance gaps, compatibility issues, or repair options.

Agent-assisted Validation Review MUST remain reviewable where its output affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Workflow-supported Validation Review MAY route validation results, collect review decisions, preserve review history, request repair, escalate unresolved issues, or coordinate approval where a governed workflow defines that behavior.

Workflow-supported Validation Review MUST preserve reviewability, traceability, privacy boundaries, authority boundaries, lifecycle boundaries, and implementation independence.

Validation Review SHOULD preserve provenance.

A Validation Review SHOULD preserve enough provenance to determine:

- what was reviewed;
- who or what performed the review where applicable;
- when review occurred where applicable;
- what Validation Scope applied;
- what Validation Result was reviewed;
- what evidence supported the review;
- what errors or warnings were confirmed;
- what errors or warnings were rejected;
- what repair was required;
- what repair was completed where applicable;
- what review limitations remain;
- what downstream-use limits remain.

Validation Review SHOULD support repair.

A Validation Review MAY confirm that repair is required, reject a repair recommendation, request additional evidence, request human review, request privacy review, request authority review, request lifecycle review, request relationship review, request source-reference review, request provenance repair, request compatibility review, or request migration review.

Validation Review SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, publication process, or downstream-use process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, or regenerate Validation Review information in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, lifecycle confusion, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Validation Review is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what validation was reviewed, what scope applied, what evidence was considered, what result was accepted or disputed, what repair remains required, whether privacy and authority boundaries were preserved, and whether the reviewed validation remains meaningful across time and implementation replacement.

## 9. Validation and Object Identity

Validation and Object Identity are related but distinct concepts within The Brain Standard.

Object Identity defines which Knowledge Object is being referred to.

Validation determines whether a governed entity satisfies applicable expectations within a defined Validation Scope.

Validation MUST preserve Object Identity.

A Knowledge Object SHOULD retain its stable Object Identity when its Validation State changes.

A Knowledge Object MUST NOT receive a new stable Object Identity merely because:

- it passes validation;
- it fails validation;
- it receives validation warnings;
- it requires validation repair;
- it becomes partially valid;
- it becomes stale;
- it is revalidated;
- it is validated by a different validator;
- it is validated under a different Validation Scope;
- it is validated under a newer standard;
- it is validated under a newer specification;
- it is imported;
- it is exported;
- it is migrated;
- it is backed up;
- it is restored;
- it is synchronized;
- it is indexed;
- it is published;
- it is processed by an agent;
- it is processed by a workflow;
- it is displayed by a different implementation.

A validation result alone MUST NOT create an identity change.

An identity change MAY occur through a governed identity process when the Knowledge Object becomes a meaningfully different object.

Where validation discovers identity issues, validation MAY report, flag, recommend, or require identity review.

Validation MUST NOT silently repair, merge, split, redirect, replace, delete, or reinterpret Object Identity unless a future governed specification, workflow, or identity process explicitly permits that behavior within a controlled scope.

Validation MAY identify identity-related issues, including:

- missing stable Object Identity;
- duplicate stable identifiers;
- conflicting identifiers;
- invalid identifier format where a governed format exists;
- missing identity provenance;
- unclear identity assignment;
- conflicting legacy identifiers;
- unresolved temporary identifiers;
- broken redirects;
- ambiguous merge history;
- ambiguous split history;
- duplicate Knowledge Objects;
- confused Source Identifiers;
- implementation-specific identifiers treated as stable identity;
- filenames treated as identity;
- folder paths treated as identity;
- titles treated as identity;
- tags treated as identity;
- database rows treated as identity;
- user-interface labels treated as identity.

Identity Validation SHOULD determine whether the governed entity preserves the identity behavior required by KS-0002 and any applicable identity specification.

Identity Validation SHOULD check whether identity remains stable across:

- renaming;
- movement;
- copying;
- backup;
- restoration;
- synchronization;
- indexing;
- summarization;
- transformation;
- translation;
- validation;
- repair;
- review;
- lifecycle transition;
- authority assignment;
- privacy assignment;
- relationship changes;
- Source Reference changes;
- provenance changes;
- import;
- export;
- migration;
- implementation replacement.

Validation MUST remain distinguishable from identity assignment.

A validator MAY determine that identity is missing or invalid.

A validator MAY recommend identity assignment.

A validator MAY require identity repair before a governed entity can pass a particular validation scope.

A validator MUST NOT assign stable Object Identity unless a governed identity process, specification, workflow, or implementation profile explicitly permits that behavior.

Validation MUST remain distinguishable from duplicate resolution.

A validator MAY detect a possible duplicate.

A validator MAY report duplicate risk.

A validator MAY recommend review.

A validator MUST NOT merge or delete Knowledge Objects merely because duplicate risk was detected unless a future governed workflow or specification explicitly permits that behavior.

Validation MUST remain distinguishable from split and merge decisions.

A validator MAY detect that an object appears to contain multiple distinct meanings.

A validator MAY detect that multiple objects appear to describe the same meaning.

A validator MAY recommend split or merge review.

A validator MUST NOT perform a split or merge by itself unless a governed identity process explicitly permits that behavior.

Validation MUST remain distinguishable from supersession.

A validator MAY detect that a Knowledge Object appears stale, outdated, superseded, deprecated, or incompatible.

A validator MAY recommend supersession review.

A validator MUST NOT mark a Knowledge Object as superseded merely because validation failed unless a future governed workflow or specification explicitly defines that behavior.

Validation MUST preserve identity provenance.

Where validation affects Object Identity, identity review, duplicate handling, split handling, merge handling, redirect handling, supersession, import, export, migration, backup, restoration, synchronization, indexing, or implementation replacement, validation SHOULD preserve enough provenance for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to determine what was checked, what issue was found, what repair was proposed, what decision was made, and whether Object Identity remained stable.

Validation MUST preserve relationships that depend on Object Identity.

A validation process MUST NOT silently break, discard, reinterpret, replace, reverse, or expose relationships merely because identity validation failed.

Where identity validation affects relationships, validation SHOULD flag the affected relationships for review or repair.

Validation MUST preserve Source References and provenance that depend on Object Identity.

A validation process MUST NOT silently break, discard, reinterpret, replace, or expose Source References or provenance records merely because identity validation failed.

Where identity validation affects Source References or provenance, validation SHOULD flag the affected Source References or provenance records for review or repair.

Validation MUST preserve privacy boundaries during identity validation.

Identity-related validation results may expose sensitive information through titles, aliases, legacy identifiers, relationships, Source References, provenance, duplicate detection, split history, merge history, redirects, or implementation identifiers.

A validation process MUST NOT expose restricted identity information merely to improve search, repair, linking, migration, export, publication, synchronization, indexing, backup, agent reasoning, workflow convenience, or implementation behavior.

Validation SHOULD support identity repair without identity confusion.

Identity repair SHOULD preserve stable Object Identity where the entity remains the same Knowledge Object.

Identity repair SHOULD preserve identity history where identifiers are corrected, redirected, deprecated, merged, split, replaced, or superseded.

Identity repair SHOULD remain reviewable where it affects relationships, Source References, provenance, lifecycle state, authority, privacy, compatibility, import, export, migration, publication, or downstream use.

Validation and Object Identity are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine which Knowledge Object was validated, what identity expectations were checked, whether identity issues exist, what repair remains required, what provenance supports the validation, and whether Object Identity remained stable across time and implementation replacement.

## 10. Validation and Metadata

Validation and Metadata are related but distinct concepts within The Brain Standard.

Metadata describes, supports, records, contextualizes, or preserves information about a governed entity.

Validation checks whether a governed entity satisfies applicable expectations within a defined Validation Scope.

Validation MAY use metadata.

Validation MAY produce metadata.

Validation MAY be recorded through metadata.

Validation MUST NOT allow metadata to replace validation meaning where validation affects governed interpretation, authority, privacy, lifecycle handling, compatibility, publication, import, export, migration, governance, or downstream use.

Validation metadata MAY describe:

- Validation State;
- Validation Scope;
- Validation Result;
- validation evidence;
- validation errors;
- validation warnings;
- validator identity where applicable;
- validation date where applicable;
- validation rule set where applicable;
- validation profile where applicable;
- validation review state;
- validation repair state;
- validation history;
- validation provenance;
- import validation;
- export validation;
- migration validation;
- backup validation;
- restoration validation;
- synchronization validation;
- indexing validation;
- publication validation;
- workflow validation;
- agent validation;
- implementation validation;
- conformance validation.

Validation metadata SHALL be explicit where validation status affects meaning, review, repair, lifecycle handling, authority handling, privacy handling, relationships, Source References, provenance, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation metadata MUST remain distinguishable from Object Identity.

A metadata field, validation label, status tag, dashboard value, validator output, plugin field, database value, implementation flag, or workflow marker MUST NOT define stable Object Identity by itself.

Validation metadata MUST remain distinguishable from descriptive metadata.

A title, summary, description, keyword, topic, alias, label, tag, category, or display value MAY support validation.

It MUST NOT be treated as validation success merely because it is present, readable, well-formed, consistent, indexed, or displayed by an implementation.

Validation metadata MUST remain distinguishable from structural metadata.

Structural metadata MAY support validation by indicating object type, record type, required sections, representation role, schema expectations, or content organization.

Structural metadata does not prove full validation unless the applicable Validation Scope is limited to structural validation.

Validation metadata MUST remain distinguishable from relationship metadata.

Relationship metadata MAY support validation of relationship participants, type, direction, context, provenance, lifecycle state, authority, privacy, compatibility, or implementation independence.

Relationship metadata does not make the relationship valid unless the applicable relationship validation expectations are satisfied.

Validation metadata MUST remain distinguishable from Source Reference metadata.

Source Reference metadata MAY support validation by identifying source support, source availability, source reliability, source authority, source privacy, citation support, or source-reference compatibility.

Source Reference metadata does not make a Source Reference valid unless the applicable source-reference validation expectations are satisfied.

Validation metadata MUST remain distinguishable from provenance metadata.

Provenance metadata MAY support validation by identifying origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, attribution, or change context.

Provenance metadata does not replace validation.

Validation metadata MUST remain distinguishable from lifecycle metadata.

Lifecycle metadata MAY indicate that validation is required, pending, completed, stale, failed, disputed, or related to repair.

Lifecycle metadata does not define validation meaning by itself.

Validation metadata MUST remain distinguishable from authority metadata.

Authority metadata MAY require validation support.

Authority metadata does not create validation success.

Validation success does not create Authority Level by itself.

Validation metadata MUST remain distinguishable from privacy metadata.

Privacy metadata MAY require validation support.

Validation metadata MUST NOT weaken Privacy Classification.

A validation field, validator report, error message, warning message, repair note, or conformance result MUST NOT expose restricted metadata merely to improve validation convenience, search, review, indexing, publication, export, synchronization, backup, agent reasoning, workflow routing, or implementation display.

Validation metadata MUST remain distinguishable from workflow metadata.

A workflow may create, route, update, or preserve validation metadata.

Workflow metadata MUST NOT be treated as validation success unless a governed workflow specification explicitly defines that behavior within a controlled scope.

Validation metadata MUST remain distinguishable from agent metadata.

An agent may propose, generate, enrich, classify, check, or report validation metadata.

Agent-generated validation metadata MUST remain reviewable where validation affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Validation metadata MUST remain distinguishable from implementation metadata.

An implementation may store, display, index, cache, sort, filter, synchronize, export, import, migrate, back up, restore, publish, or report validation metadata.

Implementation metadata MUST NOT define validation meaning by itself.

Validation SHOULD check metadata completeness where required.

Metadata Validation MAY determine whether:

- required metadata is present;
- recommended metadata is present where applicable;
- metadata roles are distinguishable;
- metadata values are interpretable;
- metadata is portable;
- metadata preserves Object Identity boundaries;
- metadata preserves relationship meaning;
- metadata preserves Source References;
- metadata preserves provenance;
- metadata preserves Lifecycle State;
- metadata preserves Authority Level;
- metadata preserves Privacy Classification;
- metadata preserves Validation State;
- metadata supports compatibility;
- metadata supports import, export, and migration;
- metadata preserves privacy boundaries;
- metadata remains implementation-independent.

Validation SHOULD check metadata consistency where required.

Metadata inconsistency MAY include conflicting identifiers, conflicting titles, conflicting lifecycle states, conflicting authority scopes, conflicting privacy classifications, conflicting validation states, conflicting Source References, conflicting relationships, conflicting provenance, conflicting import records, conflicting export records, conflicting migration records, or conflicting implementation metadata.

Validation SHOULD check metadata portability where required.

Metadata portability means metadata remains meaningful when a governed entity is renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, indexed, summarized, transformed, translated, validated by a different validator, processed by an agent, processed by a workflow, or accessed through a different implementation.

Validation SHOULD check metadata privacy where required.

Metadata may reveal restricted information even when content is hidden.

A validator MUST NOT expose restricted metadata merely because metadata is useful for validation, discovery, linking, indexing, export, publication, synchronization, backup, workflow routing, agent reasoning, or implementation behavior.

Validation SHOULD support metadata repair.

Metadata repair MAY include adding missing metadata, correcting incorrect metadata, clarifying ambiguous metadata, preserving metadata provenance, resolving metadata conflicts, updating stale metadata, limiting exposed metadata, or marking metadata for review.

Metadata repair MUST NOT silently alter Object Identity, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, or governed meaning unless a future governed workflow or specification explicitly permits that behavior.

Validation and Metadata are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what metadata was validated, what metadata remains incomplete or invalid, what repair remains required, what privacy boundaries apply, and whether metadata meaning remains portable and implementation-independent.

## 11. Validation and Relationships

Validation and Relationships are related but distinct concepts within The Brain Standard.

A Relationship is an explicit connection between governed entities.

Validation checks whether a Relationship or relationship-related information satisfies applicable expectations within a defined Validation Scope.

Validation MAY check relationships.

Validation MAY use relationships as validation evidence.

Validation MAY produce validation results about relationships.

Validation MUST NOT create relationship meaning by itself.

A validation result MUST NOT create, remove, reverse, replace, merge, split, expose, or reinterpret a Relationship unless a future governed specification, workflow, or relationship process explicitly permits that behavior within a controlled scope.

Relationship Validation MAY apply to:

- relationship participants;
- relationship type;
- relationship direction;
- relationship context;
- relationship strength;
- relationship confidence;
- relationship provenance;
- relationship lifecycle state;
- relationship authority;
- relationship privacy;
- relationship validation state;
- relationship compatibility;
- relationship source support;
- relationship import behavior;
- relationship export behavior;
- relationship migration behavior;
- relationship backup behavior;
- relationship restoration behavior;
- relationship synchronization behavior;
- relationship indexing behavior;
- relationship publication behavior;
- relationship implementation behavior;
- inferred relationships;
- agent-generated relationships;
- workflow-generated relationships;
- implementation-specific links.

Relationship Validation SHALL be explicit where relationships affect meaning, provenance, lifecycle state, authority, privacy, validation, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve relationship participants.

A validator SHOULD be able to determine which governed entities participate in the Relationship.

A Relationship MUST NOT be treated as valid where its participants are missing, ambiguous, unstable, inaccessible where required, privacy-restricted beyond the validation scope, or identified only by hidden implementation behavior.

Validation MUST preserve relationship type.

A validator SHOULD be able to determine what kind of relationship is being expressed where relationship type affects meaning.

A Relationship MUST NOT be treated as valid merely because two entities are linked, near each other, similarly named, frequently co-mentioned, tagged alike, visually connected, graph-adjacent, or semantically similar.

Validation MUST preserve relationship direction.

Where direction affects meaning, a validator SHOULD be able to determine the origin participant and target participant.

A directional Relationship MUST NOT be treated as valid if direction is missing, reversed, ambiguous, inferred without review, or collapsed by an implementation in a way that changes meaning.

Validation MUST preserve relationship context.

Relationship context SHOULD explain why the Relationship exists, how it should be interpreted, when it applies, what evidence supports it, and whether it affects lifecycle, authority, privacy, compatibility, publication, export, migration, or downstream use.

A Relationship with missing context MAY fail validation where context is required for interpretation.

Validation MUST preserve relationship provenance.

A Relationship SHOULD preserve enough provenance to determine whether it was human-created, agent-generated, workflow-generated, imported, exported, migrated, inferred, validated, reviewed, approved, rejected, deprecated, superseded, or repaired where that context affects interpretation.

Validation MUST preserve relationship privacy.

A Relationship may expose sensitive information even when the connected entities are individually less sensitive.

Relationship Validation MUST NOT expose restricted relationship information merely to improve search, graph display, indexing, export, publication, synchronization, backup, agent reasoning, workflow routing, migration, or implementation convenience.

Validation MUST preserve relationship authority boundaries.

A Relationship MUST NOT become authoritative merely because it exists, is frequently traversed, appears central in a graph, has many backlinks, appears in search results, was inferred by an agent, was created by a workflow, or was displayed by an implementation.

Validation MAY support relationship authority review, but it does not create Relationship Authority by itself.

Validation MUST preserve relationship lifecycle boundaries.

A Relationship may be proposed, inferred, reviewed, approved, rejected, deprecated, superseded, archived, quarantined, pending validation, or needs repair independently of the lifecycle state of the entities it connects.

Relationship Validation MUST NOT silently change Relationship Lifecycle State unless a future governed workflow or specification explicitly permits that behavior.

Validation MUST preserve relationship compatibility.

Relationship meaning SHOULD remain understandable when governed entities are renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, indexed, summarized, transformed, translated, validated by a different validator, processed by an agent, processed by a workflow, or accessed through a different implementation.

Validation MAY identify relationship-related issues, including:

- missing relationship participants;
- ambiguous relationship participants;
- invalid relationship type where a governed type is required;
- missing relationship direction where direction is required;
- reversed relationship direction;
- missing relationship context;
- missing relationship provenance;
- missing source support where required;
- unsupported inferred relationship;
- unreviewed agent-generated relationship;
- conflicting relationships;
- duplicate relationships;
- stale relationships;
- deprecated relationships;
- superseded relationships;
- privacy-exposing relationships;
- authority-overstated relationships;
- lifecycle-confused relationships;
- implementation-specific links treated as governed relationships;
- backlinks treated as governed relationships;
- graph edges treated as governed relationships;
- search associations treated as governed relationships;
- vector similarity treated as governed relationship meaning.

Validation MUST remain distinguishable from relationship creation.

A validator MAY recommend creating a Relationship.

A validator MAY recommend removing or revising a Relationship.

A validator MAY flag a missing Relationship as a validation issue.

A validator MUST NOT create governed relationship meaning by itself unless a future governed relationship specification, workflow, or implementation profile explicitly permits that behavior within a controlled scope.

Validation MUST remain distinguishable from inferred relationship approval.

A validator MAY detect possible inferred relationships.

A validator MAY report inferred relationship candidates.

A validator MAY require review of inferred relationships.

A validator MUST NOT treat an inferred relationship as approved merely because it appears likely, useful, frequently detected, semantically similar, graph-adjacent, or agent-proposed.

Validation SHOULD support relationship repair.

Relationship repair MAY include correcting participants, clarifying type, correcting direction, adding context, adding provenance, adding source support, resolving duplicates, resolving conflicts, restricting exposure, updating lifecycle state through a governed process, requesting authority review, requesting privacy review, or marking the Relationship for human review.

Relationship repair MUST preserve Object Identity, Source References, provenance, lifecycle state, authority, privacy, compatibility, and historical traceability where those affect governed meaning.

Validation and Relationships are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what Relationship was validated, what relationship expectations were checked, whether relationship issues exist, what repair remains required, what privacy boundaries apply, and whether relationship meaning remains portable and implementation-independent.

## 12. Validation and Source References

Validation and Source References are related but distinct concepts within The Brain Standard.

A Source Reference is a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to that governed entity.

Validation checks whether Source References or source-reference-related information satisfy applicable expectations within a defined Validation Scope.

Validation MAY check Source References.

Validation MAY use Source References as validation evidence.

Validation MAY produce validation results about Source References.

Validation MUST NOT create Source Reference meaning by itself.

A validation result MUST NOT create, remove, replace, expose, reinterpret, or collapse a Source Reference unless a future governed specification, workflow, or source-reference process explicitly permits that behavior within a controlled scope.

Source Reference Validation MAY apply to:

- source-reference existence;
- source-reference target;
- Source Material identity;
- Source Material availability;
- Source Material accessibility within privacy boundaries;
- source identifiers;
- external references;
- citations;
- evidence support;
- source relevance;
- source contradiction;
- source context;
- source reliability;
- source authority;
- source privacy;
- source compatibility;
- source-reference provenance;
- extraction provenance;
- transformation provenance;
- import provenance;
- export provenance;
- migration provenance;
- backup preservation;
- restoration preservation;
- synchronization preservation;
- indexing permission;
- publication permission;
- downstream-use limits.

Source Reference Validation SHALL be explicit where Source References affect meaning, evidence support, provenance, lifecycle state, authority, privacy, validation, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve the distinction between Source Material and Knowledge Records.

Source Material may support, explain, contextualize, contradict, originate, or otherwise relate to a Knowledge Record.

Source Material is not automatically the same thing as the Knowledge Record created from, about, or in response to it.

A validator MUST NOT treat a Source Reference as valid if the validation process collapses Source Material and Knowledge Record meaning in a way that creates source confusion.

Validation MUST preserve source-reference target meaning.

A Source Reference SHOULD identify or support identification of what Source Material, source identifier, external reference, citation, archived source, extracted source, transformed source, or governed source record is being referenced.

A Source Reference MUST NOT be treated as valid merely because a filename, folder path, URL, backlink, citation string, database row, search result, user-interface label, plugin link, or implementation-specific identifier appears to point somewhere.

Validation MUST preserve source-reference provenance.

A Source Reference SHOULD preserve enough provenance to determine who or what created, extracted, transformed, imported, exported, migrated, validated, reviewed, repaired, or preserved the Source Reference where that context affects interpretation.

Validation MUST preserve source availability context.

A Source Reference MAY refer to Source Material that is available, unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, or otherwise limited.

A Source Reference MUST NOT be treated as invalid merely because Source Material is unavailable unless the applicable validation scope requires availability.

A Source Reference MUST NOT be treated as valid merely because Source Material is available unless the applicable validation scope also checks relevance, provenance, privacy, compatibility, and other required expectations.

Validation MUST preserve source privacy.

Source References may reveal restricted information through source titles, filenames, paths, URLs, citations, authors, organizations, dates, relationships, excerpts, provenance, source identifiers, or access patterns.

A validator MUST NOT expose restricted Source Reference information merely to improve evidence review, citation quality, search, indexing, export, publication, synchronization, backup, agent reasoning, workflow routing, migration, or implementation convenience.

Validation MUST preserve source authority boundaries.

Source authority, source reliability, source availability, citation existence, or evidence presence MAY support validation.

They MUST NOT automatically create validation success unless the applicable Validation Scope explicitly defines that requirement.

Validation MUST preserve source reliability boundaries.

A Source Reference MAY point to unreliable, uncertain, biased, incomplete, stale, conflicting, partial, or disputed Source Material.

A Source Reference may still be valid as a traceable reference even when the Source Material is low reliability, disputed, contradicted, or limited.

A validation scope SHOULD make clear whether it checks source-reference existence, source availability, source reliability, source authority, evidence strength, or publication readiness.

Validation MUST preserve citation boundaries.

A citation may support a Source Reference.

Citation syntax does not define Source Reference validity by itself unless a governed validation scope explicitly requires a citation format.

A well-formed citation may still point to the wrong source.

A poorly formatted citation may still preserve enough traceability for a limited validation scope.

Validation MUST preserve source-reference compatibility.

Source Reference meaning SHOULD remain understandable when Source Material or governed entities are renamed, moved, copied, archived, restricted, imported, exported, migrated, backed up, restored, synchronized, indexed where permitted, published where permitted, validated by a different validator, processed by an agent, processed by a workflow, or accessed through a different implementation.

Validation MAY identify source-reference-related issues, including:

- missing Source Reference where one is required;
- unclear source-reference target;
- broken source-reference target;
- unavailable Source Material;
- restricted Source Material;
- missing source identifier;
- confused source identifier;
- missing external reference;
- missing citation where citation is required;
- malformed citation where citation format is governed;
- citation pointing to the wrong source;
- missing evidence support;
- weak evidence support;
- contradictory source support;
- stale Source Material;
- disputed Source Material;
- missing source-reference provenance;
- missing extraction provenance;
- missing transformation provenance;
- missing import provenance;
- missing export provenance;
- missing migration provenance;
- privacy-exposing Source Reference;
- authority-overstated Source Reference;
- source reliability overstated;
- source availability overstated;
- Source Material confused with Knowledge Record;
- implementation-specific source link treated as governed Source Reference.

Validation MUST remain distinguishable from Source Reference creation.

A validator MAY recommend creating a Source Reference.

A validator MAY recommend revising a Source Reference.

A validator MAY flag a missing Source Reference as a validation issue.

A validator MUST NOT create governed Source Reference meaning by itself unless a future governed source-reference specification, workflow, or implementation profile explicitly permits that behavior within a controlled scope.

Validation SHOULD support Source Reference repair.

Source Reference repair MAY include clarifying the source target, correcting a source identifier, adding missing citation information, adding source-reference provenance, adding extraction provenance, adding transformation provenance, correcting source availability, correcting source privacy, limiting exposure, resolving broken links, replacing implementation-specific links with governed references, or marking the Source Reference for human review.

Source Reference repair MUST preserve Object Identity, metadata, relationships, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, and historical traceability where those affect governed meaning.

Validation and Source References are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what Source Reference was validated, what source-reference expectations were checked, whether source-reference issues exist, what repair remains required, what privacy boundaries apply, and whether source-reference meaning remains portable and implementation-independent.

## 13. Validation and Provenance

Validation and Provenance are related but distinct concepts within The Brain Standard.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, attribution, or change context associated with a governed entity.

Validation checks whether provenance or provenance-related information satisfies applicable expectations within a defined Validation Scope.

Validation MAY require provenance.

Validation MAY use provenance as validation evidence.

Validation MAY produce provenance.

Validation MAY validate provenance.

Validation MUST NOT replace provenance.

Provenance MUST NOT replace validation.

A governed entity with provenance may still fail validation.

A governed entity with incomplete provenance may pass a limited Validation Scope while still requiring provenance repair.

Provenance Validation MAY apply to:

- origin context;
- source context;
- reasoning context;
- transformation history;
- creator information;
- editor information;
- agent involvement;
- workflow involvement;
- import provenance;
- export provenance;
- migration provenance;
- backup provenance;
- restoration provenance;
- synchronization provenance;
- indexing provenance;
- publication provenance;
- validation history;
- review history;
- evidence context;
- attribution context;
- change history;
- repair history;
- provenance privacy;
- provenance compatibility.

Provenance Validation SHALL be explicit where provenance affects meaning, trust, review, repair, lifecycle handling, authority handling, privacy handling, relationships, Source References, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve provenance meaning.

A validator SHOULD be able to determine what provenance exists, what provenance is missing, what provenance is incomplete, what provenance is uncertain, what provenance is disputed, and what provenance is required for the applicable Validation Scope.

Validation MUST preserve provenance context.

Provenance context SHOULD make clear whether a governed entity was human-created, agent-generated, workflow-generated, imported, exported, migrated, extracted, transformed, summarized, translated, validated, reviewed, approved, rejected, repaired, deprecated, superseded, archived, restricted, quarantined, or otherwise governed where that context affects interpretation.

Validation MUST preserve validation provenance.

A validation result SHOULD preserve enough provenance to determine:

- what was validated;
- what Validation Scope applied;
- what validator performed or supported validation where applicable;
- when validation occurred where applicable;
- what rule set was used;
- what evidence supported the result;
- what errors were found;
- what warnings were found;
- what repair was recommended;
- what review occurred;
- what review remains required;
- what downstream-use limits remain.

Validation MUST preserve provenance privacy.

Provenance may reveal restricted information even when the main knowledge content appears safe to expose.

Provenance may reveal source names, personal names, organizations, file paths, URLs, timestamps, workflow routes, agent activity, review decisions, migration history, import history, export history, relationship context, authority context, privacy context, or sensitive decision history.

A validator MUST NOT expose restricted provenance merely to improve validation convenience, evidence review, search, indexing, export, publication, synchronization, backup, agent reasoning, workflow routing, migration, or implementation behavior.

Validation MUST preserve provenance authority boundaries.

Provenance MAY support authority review.

Provenance MAY explain why Authority Level was assigned.

Provenance MAY show what evidence, source, review, workflow, or decision supports a governed entity.

However, provenance existence, source existence, attribution, review history, validation history, or workflow history MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Validation MUST preserve provenance lifecycle boundaries.

Provenance MAY support lifecycle review.

Provenance MAY explain why a governed entity is draft, review, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending validation, or needs repair.

However, provenance existence or validation history MUST NOT silently change Lifecycle State unless a future governed workflow or specification explicitly defines that behavior.

Validation MUST preserve provenance compatibility.

Provenance SHOULD remain understandable when a governed entity is renamed, moved, copied, imported, exported, migrated, backed up, restored, synchronized, indexed where permitted, published where permitted, validated by a different validator, processed by an agent, processed by a workflow, or accessed through a different implementation.

Validation MAY identify provenance-related issues, including:

- missing provenance where provenance is required;
- incomplete provenance;
- unclear provenance;
- conflicting provenance;
- stale provenance;
- disputed provenance;
- missing source context;
- missing attribution;
- missing extraction history;
- missing transformation history;
- missing agent involvement;
- missing workflow involvement;
- missing import provenance;
- missing export provenance;
- missing migration provenance;
- missing validation history;
- missing review history;
- privacy-exposing provenance;
- authority-overstated provenance;
- lifecycle-confusing provenance;
- implementation-specific history treated as governed provenance;
- workflow memory treated as governed provenance;
- agent memory treated as governed provenance.

Validation MUST remain distinguishable from provenance creation.

A validator MAY recommend adding provenance.

A validator MAY recommend correcting provenance.

A validator MAY flag missing provenance as a validation issue.

A validator MUST NOT create governed provenance meaning by itself unless a future governed provenance specification, workflow, or implementation profile explicitly permits that behavior within a controlled scope.

Validation SHOULD support provenance repair.

Provenance repair MAY include adding missing provenance, correcting inaccurate provenance, clarifying ambiguous provenance, preserving validation history, preserving review history, correcting import provenance, correcting export provenance, correcting migration provenance, limiting exposed provenance, resolving conflicting provenance, or marking provenance for human review.

Provenance repair MUST preserve Object Identity, metadata, relationships, Source References, Lifecycle State, Authority Level, Privacy Classification, compatibility, and historical traceability where those affect governed meaning.

Validation and Provenance are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what provenance was validated, what provenance expectations were checked, whether provenance issues exist, what repair remains required, what privacy boundaries apply, and whether provenance meaning remains portable and implementation-independent.

## 14. Validation and Lifecycle State

Validation and Lifecycle State are related but distinct concepts within The Brain Standard.

Lifecycle State describes the current governed state of an entity.

Validation checks whether a governed entity satisfies applicable expectations within a defined Validation Scope.

Validation MAY support lifecycle decisions.

Lifecycle State MAY require validation.

Validation MUST NOT replace Lifecycle State.

Lifecycle State MUST NOT replace Validation State.

A validation result MUST NOT silently approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, promote, demote, or otherwise transition a governed entity unless a future governed workflow or specification explicitly permits that behavior within a controlled scope.

Lifecycle Validation MAY apply to:

- lifecycle state presence;
- lifecycle state meaning;
- lifecycle state scope where applicable;
- lifecycle transition history;
- lifecycle transition provenance;
- review requirements;
- approval requirements;
- rejection handling;
- deprecation handling;
- supersession handling;
- archival handling;
- restriction handling;
- quarantine handling;
- pending-review handling;
- pending-validation handling;
- needs-repair handling;
- lifecycle metadata;
- lifecycle compatibility;
- lifecycle privacy;
- lifecycle authority effects;
- lifecycle relationship effects;
- lifecycle source-reference effects;
- lifecycle import behavior;
- lifecycle export behavior;
- lifecycle migration behavior;
- lifecycle publication behavior;
- lifecycle downstream-use limits.

Lifecycle Validation SHALL be explicit where lifecycle status affects meaning, review, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, authority, privacy, relationships, Source References, provenance, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve Lifecycle State meaning.

A validator SHOULD be able to determine what Lifecycle State applies, what the state means, whether the state is current or historical, whether a transition occurred, and whether the lifecycle state requires validation, review, repair, restriction, quarantine, approval, rejection, deprecation, supersession, archival, or another governed action.

Validation MUST preserve lifecycle transition provenance.

Where a lifecycle transition affects meaning, authority, privacy, relationships, Source References, provenance, compatibility, publication, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use, validation SHOULD check whether enough provenance exists to determine what changed, who or what changed it where applicable, when it changed where applicable, and why the change occurred where practical.

Validation MUST preserve lifecycle privacy.

A lifecycle state or lifecycle transition may reveal sensitive information.

A rejected, quarantined, restricted, needs-repair, pending-validation, deprecated, or superseded state may expose review concerns, privacy concerns, source concerns, authority concerns, compatibility concerns, or governance concerns.

Validation MUST NOT expose restricted lifecycle information merely to improve review, routing, indexing, export, publication, synchronization, backup, migration, agent reasoning, workflow convenience, or implementation behavior.

Validation MUST preserve lifecycle authority boundaries.

A valid lifecycle state does not automatically create Authority Level.

An Approved lifecycle state may support authority review, but approval does not automatically create unlimited authority.

A Deprecated, Superseded, Archived, Rejected, Restricted, Quarantined, Pending Validation, or Needs Repair lifecycle state may limit authority or downstream use, but lifecycle state does not replace Authority Level.

Validation MUST preserve lifecycle validation boundaries.

An entity may be:

- draft and structurally valid;
- draft and invalid;
- review-ready but not approved;
- approved and valid;
- approved and later invalid;
- rejected but valid as a historical record;
- deprecated and valid for compatibility review;
- superseded and valid for historical interpretation;
- archived and valid for preservation;
- restricted and valid;
- quarantined because validation failed;
- pending validation but otherwise reviewable;
- needs repair but still privacy-protected.

Validation MUST preserve lifecycle compatibility.

Lifecycle State SHOULD remain understandable when a governed entity is renamed, moved, copied, imported, exported, migrated, backed up, restored, synchronized, indexed where permitted, published where permitted, validated by a different validator, processed by an agent, processed by a workflow, or accessed through a different implementation.

Validation MAY identify lifecycle-related issues, including:

- missing Lifecycle State where one is required;
- unclear Lifecycle State;
- conflicting Lifecycle State;
- stale Lifecycle State;
- invalid lifecycle value where a governed vocabulary exists;
- missing lifecycle transition provenance;
- unreviewed lifecycle transition;
- approval confused with validation success;
- validation success confused with approval;
- workflow completion confused with lifecycle transition;
- agent confidence confused with lifecycle transition;
- implementation status confused with governed Lifecycle State;
- folder placement treated as Lifecycle State;
- tag convention treated as Lifecycle State;
- user-interface state treated as Lifecycle State;
- lifecycle state weakening privacy requirements;
- lifecycle state overstating Authority Level;
- lifecycle state hiding validation failure;
- lifecycle state breaking relationships;
- lifecycle state breaking Source References;
- lifecycle state losing provenance.

Validation MUST remain distinguishable from lifecycle transition.

A validator MAY recommend a lifecycle transition.

A validator MAY require lifecycle review.

A validator MAY flag lifecycle inconsistency as a validation issue.

A validator MUST NOT transition Lifecycle State by itself unless a future governed workflow, lifecycle specification, validation specification, or implementation profile explicitly permits that behavior within a controlled scope.

Validation SHOULD support lifecycle repair.

Lifecycle repair MAY include clarifying lifecycle state, correcting lifecycle metadata, adding transition provenance, resolving lifecycle conflicts, marking lifecycle state as pending review, requesting lifecycle review, requesting validation review, requesting privacy review, requesting authority review, or marking the governed entity as needing repair.

Lifecycle repair MUST preserve Object Identity, metadata, relationships, Source References, provenance, Authority Level, Privacy Classification, compatibility, and historical traceability where those affect governed meaning.

Validation and Lifecycle State are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what Lifecycle State was validated, what lifecycle expectations were checked, whether lifecycle issues exist, what repair or review remains required, what privacy boundaries apply, and whether lifecycle meaning remains portable and implementation-independent.

## 15. Validation and Authority Level

Validation and Authority Level are related but distinct concepts within The Brain Standard.

Authority Level describes governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Validation checks whether a governed entity satisfies applicable expectations within a defined Validation Scope.

Validation MAY support authority review.

Authority Level MAY require validation support.

Validation MUST NOT replace Authority Level.

Authority Level MUST NOT replace Validation State.

Validation success MUST NOT create Authority Level by itself.

Validation failure MUST NOT remove historical Authority Level by itself.

Authority Validation MAY apply to:

- Authority Level presence;
- authority scope;
- authority assignment;
- authority review;
- authority provenance;
- authority evidence;
- source authority;
- relationship authority;
- use-authority;
- trust boundaries;
- authority limitations;
- authority suspension;
- authority supersession;
- authority inheritance where governed;
- authority downgrade;
- authority escalation;
- authority compatibility;
- authority privacy;
- authority publication effects;
- authority export effects;
- authority migration effects;
- authority downstream-use limits.

Authority Validation SHALL be explicit where Authority Level affects interpretation, governance, review, validation, publication, synchronization, indexing, backup, import, export, migration, relationship handling, Source Reference handling, provenance handling, privacy handling, workflow behavior, agent behavior, implementation behavior, or downstream use.

Validation MUST preserve Authority Level meaning.

A validator SHOULD be able to determine what Authority Level applies, what authority scope applies, what evidence supports the authority, what review supports the authority, whether authority is current or historical, whether authority is limited, and whether additional review is required.

Validation MUST preserve authority scope.

Authority Level is meaningful only within its Authority Scope.

A validation result MUST NOT expand Authority Scope.

A validation result MUST NOT collapse Authority Scope.

A validation result MUST NOT treat narrow authority as universal authority.

A validation result MUST NOT treat validation success as authority beyond the validated scope.

Validation MUST preserve authority provenance.

Where Authority Level affects interpretation, governance, publication, export, migration, automation, relationship handling, agent reasoning, workflow behavior, implementation behavior, or downstream use, validation SHOULD check whether enough provenance exists to determine who or what assigned authority where applicable, what evidence supported it, what review occurred, what source support exists, what limitations apply, and whether the authority remains current.

Validation MUST preserve authority privacy.

Authority information may reveal sensitive review decisions, source reliance, internal governance decisions, restricted relationships, restricted provenance, publication limits, export limits, or downstream-use limits.

Validation MUST NOT expose restricted authority information merely to improve review, trust scoring, search, indexing, export, publication, synchronization, backup, migration, agent reasoning, workflow convenience, or implementation display.

Validation MUST preserve authority and lifecycle boundaries.

Approval MAY support authority review, but approval does not automatically create unlimited authority.

A governed entity may be approved but low-authority.

A governed entity may be high-authority but superseded.

A governed entity may be archived but authoritative for historical interpretation.

A governed entity may be deprecated but still authoritative for compatibility review.

Validation MUST preserve authority and privacy boundaries.

A governed entity may be high-authority and private.

A governed entity may be high-authority and non-exportable.

A governed entity may be authoritative for internal use but not publishable.

A governed entity may be source-supported but still restricted.

Validation MUST NOT create access permission, publication permission, export permission, synchronization permission, indexing permission, backup permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission merely because Authority Level is high or validation succeeds.

Validation MUST preserve authority and source-reference boundaries.

Source References, Source Material, evidence, attribution, source reliability, source authority, and source availability MAY support Authority Level.

However, source existence, citation existence, provenance existence, source availability, source reliability, source popularity, or source authority MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Validation MUST preserve authority and relationship boundaries.

A Relationship MAY support authority.

A Relationship MAY carry authority.

A Relationship MAY limit authority.

A Relationship MUST NOT become authoritative merely because it exists, has many backlinks, appears central in a graph, appears frequently in search results, was inferred by an agent, was created by a workflow, or was displayed by an implementation.

Validation MAY identify authority-related issues, including:

- missing Authority Level where authority is required;
- unclear authority scope;
- conflicting authority assignments;
- unsupported Authority Level;
- stale Authority Level;
- authority overstated beyond its scope;
- authority assigned without sufficient provenance;
- authority assigned without required review;
- authority confused with approval;
- authority confused with validation success;
- authority confused with source reliability;
- authority confused with source popularity;
- authority confused with agent confidence;
- authority confused with workflow completion;
- authority confused with implementation visibility;
- authority weakening privacy requirements;
- authority overstating publication readiness;
- authority overstating export readiness;
- authority incompatible with lifecycle state;
- authority incompatible with downstream-use limits.

Validation MUST remain distinguishable from authority assignment.

A validator MAY recommend authority review.

A validator MAY flag missing or unsupported authority as a validation issue.

A validator MAY require authority repair before a governed entity passes a particular Validation Scope.

A validator MUST NOT assign, raise, lower, suspend, remove, inherit, or reinterpret Authority Level by itself unless a future governed authority specification, workflow, validation specification, or implementation profile explicitly permits that behavior within a controlled scope.

Validation SHOULD support authority repair.

Authority repair MAY include clarifying authority scope, adding authority provenance, correcting unsupported Authority Level, resolving conflicting authority, limiting overstated authority, requesting authority review, requesting source-reference review, requesting provenance repair, requesting privacy review, or marking authority for human review.

Authority repair MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Privacy Classification, compatibility, and historical traceability where those affect governed meaning.

Validation and Authority Level are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what Authority Level was validated, what authority expectations were checked, whether authority issues exist, what repair or review remains required, what privacy boundaries apply, and whether authority meaning remains scoped, portable, and implementation-independent.

## 16. Validation and Privacy Classification

Validation and Privacy Classification are related but distinct concepts within The Brain Standard.

Privacy Classification defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.

Validation checks whether a governed entity satisfies applicable expectations within a defined Validation Scope.

Validation MAY support privacy review.

Privacy Classification MAY require validation support.

Validation MUST NOT replace Privacy Classification.

Privacy Classification MUST NOT replace Validation State.

Validation success MUST NOT create privacy permission by itself.

Validation success MUST NOT weaken Privacy Classification.

Validation failure MUST NOT remove privacy obligations by itself.

Privacy Validation MAY apply to:

- Privacy Classification presence;
- privacy scope;
- privacy assignment;
- privacy review;
- access expectations;
- visibility expectations;
- exposure expectations;
- routing expectations;
- publication expectations;
- synchronization expectations;
- indexing expectations;
- export expectations;
- backup expectations;
- restoration expectations;
- agent access;
- workflow access;
- implementation access;
- downstream-use handling;
- privacy provenance;
- privacy metadata;
- privacy repair;
- privacy compatibility.

Privacy Validation SHALL be explicit where Privacy Classification affects interpretation, access, exposure, review, repair, authority, lifecycle handling, relationships, Source References, provenance, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve Privacy Classification meaning.

A validator SHOULD be able to determine what Privacy Classification applies, what privacy scope applies, what handling expectations apply, what review supports the classification where applicable, whether privacy status is current or historical, whether privacy handling is limited, and whether additional privacy review is required.

Validation MUST preserve privacy scope.

Privacy Classification is meaningful only within its Privacy Scope.

A validation result MUST NOT expand Privacy Scope.

A validation result MUST NOT collapse Privacy Scope.

A validation result MUST NOT treat narrow privacy permission as universal permission.

A validation result MUST NOT treat validation success as permission beyond the validated scope.

Validation MUST preserve privacy provenance.

Where Privacy Classification affects access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, restoration, agent access, workflow access, implementation access, or downstream use, validation SHOULD check whether enough provenance exists to determine who or what assigned the Privacy Classification where applicable, what review occurred, what limitations apply, and whether the classification remains current.

Validation MUST preserve privacy and authority boundaries.

A governed entity may be high-authority and private.

A governed entity may be high-authority and non-exportable.

A governed entity may be authoritative for internal use but not publishable.

A governed entity may be validated for authority but still restricted by Privacy Classification.

Validation MUST NOT create access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission merely because Authority Level is high or validation succeeds.

Validation MUST preserve privacy and lifecycle boundaries.

A governed entity may be draft and private.

A governed entity may be approved and private.

A governed entity may be rejected and still privacy-protected.

A governed entity may be deprecated and still restricted.

A governed entity may be superseded and still non-exportable.

A governed entity may be archived and still confidential.

A governed entity may be quarantined because validation exposed privacy risk.

Validation MUST NOT change Lifecycle State merely because privacy validation passed or failed unless a future governed workflow or specification explicitly permits that behavior within a controlled scope.

Validation MUST preserve privacy and source-reference boundaries.

Source References may reveal restricted information through source titles, source identifiers, authors, organizations, URLs, file paths, citations, excerpts, provenance, relationships, or access patterns.

A validator MUST NOT expose restricted Source Reference information merely to improve validation, citation quality, evidence review, search, indexing, export, publication, synchronization, backup, migration, agent reasoning, workflow routing, or implementation convenience.

Validation MUST preserve privacy and relationship boundaries.

Relationships may reveal restricted information even when individual connected entities appear safe.

A validator MUST NOT expose restricted relationship information merely to improve graph display, search, indexing, export, publication, synchronization, backup, migration, agent reasoning, workflow routing, or implementation convenience.

Validation MUST preserve privacy and metadata boundaries.

Metadata may reveal restricted information even when content is hidden.

A validator MUST NOT expose restricted metadata merely because metadata is useful for validation, discovery, linking, indexing, export, publication, synchronization, backup, workflow routing, agent reasoning, or implementation behavior.

Validation MUST preserve privacy and provenance boundaries.

Provenance may reveal restricted information about sources, people, organizations, decisions, workflows, agents, reviews, migrations, imports, exports, or access patterns.

A validator MUST NOT expose restricted provenance merely because provenance is useful for validation, evidence review, repair, indexing, publication, export, synchronization, backup, workflow routing, agent reasoning, or implementation behavior.

Validation MUST preserve privacy and agent boundaries.

An agent MAY validate privacy-related information only within its permitted access scope.

An agent MUST NOT access, expose, summarize, infer, copy, export, publish, index, synchronize, back up, or route restricted information beyond the permissions allowed by Privacy Classification and the applicable governance rules.

Agent-generated validation results involving privacy MUST remain reviewable where they affect access, exposure, publication, export, migration, governance, or downstream use.

Validation MUST preserve privacy and workflow boundaries.

A workflow MAY route, request, perform, or preserve privacy validation.

A workflow MUST NOT treat workflow completion as privacy clearance unless a future governed workflow specification explicitly defines that behavior within a controlled scope.

Workflow convenience MUST NOT override Privacy Classification.

Validation MUST preserve privacy and implementation boundaries.

An implementation MAY display, index, cache, filter, sort, route, synchronize, export, import, migrate, back up, restore, publish, or report privacy validation information only within permitted privacy boundaries.

Implementation visibility MUST NOT define Privacy Classification.

Implementation visibility MUST NOT create validation success.

Implementation visibility MUST NOT create publication, export, synchronization, indexing, backup, agent-use, workflow-use, implementation-use, or downstream-use permission.

Validation MAY identify privacy-related issues, including:

- missing Privacy Classification where one is required;
- unclear privacy scope;
- conflicting Privacy Classification;
- unsupported privacy assignment;
- stale Privacy Classification;
- privacy classification assigned without sufficient provenance;
- privacy classification assigned without required review;
- privacy confused with validation success;
- privacy confused with lifecycle state;
- privacy confused with authority level;
- privacy confused with source availability;
- privacy confused with folder location;
- privacy confused with filename convention;
- privacy confused with tag convention;
- privacy confused with implementation visibility;
- access permission overstated;
- publication permission overstated;
- export permission overstated;
- synchronization permission overstated;
- indexing permission overstated;
- backup permission overstated;
- agent access overstated;
- workflow access overstated;
- implementation access overstated;
- downstream-use permission overstated;
- metadata exposing restricted information;
- relationships exposing restricted information;
- Source References exposing restricted information;
- provenance exposing restricted information.

Validation MUST remain distinguishable from privacy assignment.

A validator MAY recommend privacy review.

A validator MAY flag missing or unsupported privacy classification as a validation issue.

A validator MAY require privacy repair before a governed entity passes a particular Validation Scope.

A validator MUST NOT assign, raise, lower, remove, inherit, weaken, expand, collapse, or reinterpret Privacy Classification by itself unless a future governed privacy specification, workflow, validation specification, or implementation profile explicitly permits that behavior within a controlled scope.

Validation SHOULD support privacy repair.

Privacy repair MAY include clarifying privacy scope, adding privacy provenance, correcting unsupported Privacy Classification, resolving conflicting privacy classifications, limiting overstated access, limiting overstated visibility, limiting exposed metadata, limiting exposed Source References, limiting exposed relationships, limiting exposed provenance, requesting privacy review, requesting authority review, requesting lifecycle review, or marking privacy for human review.

Privacy repair MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, validation history, compatibility, and historical traceability where those affect governed meaning.

Validation and Privacy Classification are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what Privacy Classification was validated, what privacy expectations were checked, whether privacy issues exist, what repair or review remains required, what exposure limits apply, and whether privacy meaning remains scoped, portable, and implementation-independent.

## 17. Validation and Agents

Validation and Agents are related but distinct concepts within The Brain Standard.

An agent is a governed actor or system that may read, interpret, classify, extract, transform, summarize, compare, validate, repair, route, recommend, or generate information within The Brain ecosystem according to its permissions, role, scope, and applicable governance rules.

Validation checks whether a governed entity, agent output, agent action, agent recommendation, agent-generated metadata, agent-generated relationship, agent-generated provenance, agent-generated validation result, or agent-access behavior satisfies applicable expectations within a defined Validation Scope.

Agents MAY support validation.

Agents MAY perform validation checks.

Agents MAY propose validation results.

Agents MAY identify validation errors.

Agents MAY identify validation warnings.

Agents MAY recommend repair.

Agents MAY support validation review.

Agents MUST NOT become unreviewable authorities over validation outcomes where validation affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Agent Validation MAY apply to:

- agent outputs;
- agent-generated metadata;
- agent-generated relationships;
- agent-generated Source References;
- agent-generated provenance;
- agent-generated validation results;
- agent confidence;
- agent recommendations;
- agent repair proposals;
- agent access;
- agent restrictions;
- agent task scope;
- agent workflow participation;
- agent import behavior;
- agent export behavior;
- agent migration behavior;
- agent publication behavior;
- agent indexing behavior;
- agent synchronization behavior;
- agent backup behavior;
- agent downstream-use behavior.

Agent Validation SHALL be explicit where agent behavior affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve agent role boundaries.

An agent may assist validation without owning final validation meaning.

An agent may propose a validation result without creating approval.

An agent may identify a validation issue without changing Lifecycle State.

An agent may recommend authority review without assigning Authority Level.

An agent may identify privacy risk without changing Privacy Classification.

An agent may suggest repair without performing governed repair.

Validation MUST preserve agent scope.

Agent validation is meaningful only within the agent’s permitted task scope, knowledge scope, access scope, validation scope, privacy scope, workflow scope, and implementation scope.

A validation result generated by an agent MUST NOT be treated as broader than the scope under which the agent operated.

Validation MUST preserve agent provenance.

Agent-generated validation SHOULD preserve enough provenance to determine:

- what agent performed or supported validation where applicable;
- what task the agent performed;
- what Validation Scope applied;
- what input was used where permitted;
- what output was produced;
- what rule set, standard, specification, workflow, implementation profile, import process, export process, migration process, or downstream-use context was used;
- what confidence or uncertainty was reported where applicable;
- what errors were identified;
- what warnings were identified;
- what repair was recommended;
- what human or workflow review remains required.

Validation MUST preserve agent privacy boundaries.

An agent MUST NOT access restricted information outside its permitted scope.

An agent MUST NOT expose restricted information through validation results, summaries, error messages, warnings, repair notes, recommendations, logs, embeddings, indexes, exports, publications, synchronization outputs, backup outputs, workflow messages, or implementation displays.

Agent convenience, reasoning quality, search quality, indexing quality, workflow convenience, repair quality, migration convenience, or implementation convenience MUST NOT override Privacy Classification.

Validation MUST preserve agent authority boundaries.

Agent confidence MUST NOT imply validation success.

Agent confidence MUST NOT imply Authority Level.

Agent confidence MUST NOT imply approval.

Agent confidence MUST NOT imply publication readiness.

Agent confidence MUST NOT imply export readiness.

Agent confidence MUST NOT imply privacy clearance.

An agent-generated validation result MAY support review, but it does not create final authority unless a future governed agent standard, workflow standard, validation specification, or implementation profile explicitly defines that behavior within a controlled scope.

Validation MUST preserve agent lifecycle boundaries.

An agent-generated validation result MUST NOT silently transition Lifecycle State.

An agent-generated recommendation MUST NOT silently approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, promote, or demote a governed entity unless a future governed workflow or specification explicitly permits that behavior within a controlled scope.

Validation MUST preserve agent relationship boundaries.

An agent MAY propose relationships.

An agent MAY identify relationship issues.

An agent MAY validate relationship structure or support.

An agent MUST NOT treat inferred relationships as governed relationships merely because they are probable, useful, semantically similar, graph-adjacent, frequently detected, or useful for reasoning unless a future governed relationship specification, workflow, or implementation profile explicitly permits that behavior.

Validation MUST preserve agent Source Reference boundaries.

An agent MAY propose Source References.

An agent MAY identify missing Source References.

An agent MAY check source-reference support within permitted access scope.

An agent MUST NOT create source-reference meaning by itself unless a future governed source-reference specification, workflow, or implementation profile explicitly permits that behavior.

Validation MUST preserve agent provenance boundaries.

An agent MAY produce provenance.

An agent MAY identify missing provenance.

An agent MAY recommend provenance repair.

An agent MUST NOT fabricate provenance.

An agent MUST NOT treat hidden agent memory as governed provenance.

An agent MUST NOT treat inferred reasoning as source evidence unless a future governed specification explicitly defines that behavior.

Validation MUST preserve agent compatibility.

Agent-generated validation meaning SHOULD remain understandable when a governed entity is renamed, moved, copied, imported, exported, migrated, backed up, restored, synchronized, indexed where permitted, published where permitted, validated by a different validator, processed by a different agent, processed by a workflow, or accessed through a different implementation.

Validation MAY identify agent-related issues, including:

- agent output missing validation scope;
- agent output missing provenance;
- agent output missing review status;
- agent confidence overstated;
- agent confidence confused with validation success;
- agent confidence confused with authority;
- agent confidence confused with approval;
- agent confidence confused with privacy clearance;
- agent recommendation treated as governed decision;
- agent-generated relationship treated as approved relationship;
- agent-generated Source Reference treated as verified source support;
- agent-generated metadata treated as reviewed metadata;
- agent-generated provenance treated as complete provenance;
- agent output exposing restricted information;
- agent output exceeding permitted scope;
- agent output relying on hidden memory;
- agent output relying on implementation-specific state;
- agent output lacking repair traceability;
- agent output losing compatibility during import, export, migration, backup, synchronization, indexing, or publication.

Validation MUST remain distinguishable from agent execution.

Successful agent execution does not automatically mean validation success.

Successful agent execution does not automatically mean workflow completion.

Successful agent execution does not automatically mean approval.

Successful agent execution does not automatically mean authority.

Successful agent execution does not automatically mean privacy clearance.

Successful agent execution does not automatically mean publication, export, synchronization, indexing, backup, or downstream-use permission.

Validation SHOULD support agent-output repair.

Agent-output repair MAY include adding validation scope, adding provenance, clarifying uncertainty, correcting overstated confidence, limiting exposed information, requesting human review, requesting workflow review, requesting privacy review, requesting authority review, requesting lifecycle review, requesting relationship review, requesting Source Reference review, requesting provenance repair, or marking the agent output as needing repair.

Agent-output repair MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, validation history, compatibility, and historical traceability where those affect governed meaning.

Validation and Agents are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what agent behavior was validated, what agent expectations were checked, whether agent-related issues exist, what review or repair remains required, what privacy boundaries apply, and whether agent-generated validation meaning remains scoped, reviewable, portable, and implementation-independent.

## 18. Validation and Workflows

Validation and Workflows are related but distinct concepts within The Brain Standard.

A workflow is a governed sequence, process, route, review path, approval path, repair path, automation, or operational procedure used to move governed entities through defined actions, checks, decisions, transitions, or outputs.

Validation checks whether a governed entity, workflow output, workflow transition, workflow-generated metadata, workflow-generated provenance, workflow-generated relationship, workflow-generated validation result, workflow route, workflow repair, workflow approval, workflow rejection, or workflow-related decision satisfies applicable expectations within a defined Validation Scope.

Workflows MAY support validation.

Workflows MAY perform validation checks.

Workflows MAY route validation results.

Workflows MAY require validation before specific transitions.

Workflows MAY preserve validation history.

Workflows MAY request review.

Workflows MAY request repair.

Workflows MUST NOT make validation meaning unreviewable where validation affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Workflow Validation MAY apply to:

- workflow outputs;
- workflow steps;
- workflow stages;
- workflow routing;
- workflow-generated metadata;
- workflow-generated relationships;
- workflow-generated Source References;
- workflow-generated provenance;
- workflow-generated validation results;
- workflow review;
- workflow repair;
- workflow approval;
- workflow rejection;
- workflow escalation;
- workflow lifecycle transitions;
- workflow authority handling;
- workflow privacy handling;
- workflow import activity;
- workflow export activity;
- workflow migration activity;
- workflow backup activity;
- workflow restoration activity;
- workflow synchronization activity;
- workflow indexing activity;
- workflow publication activity;
- workflow downstream-use activity.

Workflow Validation SHALL be explicit where workflow behavior affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, publication, synchronization, indexing, backup, import, export, migration, agent behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve workflow scope.

A workflow validation result is meaningful only within the workflow scope, validation scope, privacy scope, authority scope, lifecycle scope, implementation scope, and downstream-use scope under which the workflow operated.

A workflow result MUST NOT be treated as broader than the governed workflow specification, standard, validation scope, or review path allows.

Validation MUST preserve workflow provenance.

Workflow-generated validation SHOULD preserve enough provenance to determine:

- what workflow performed or supported validation where applicable;
- what workflow step or stage was involved;
- what governed entity was processed;
- what Validation Scope applied;
- what rule set, standard, specification, workflow profile, implementation profile, import process, export process, migration process, or downstream-use context was used;
- what output was produced;
- what errors were identified;
- what warnings were identified;
- what review occurred;
- what review remains required;
- what repair occurred;
- what repair remains required;
- what downstream-use limits remain.

Validation MUST preserve workflow privacy boundaries.

A workflow MUST NOT expose restricted information through routing, status messages, validation results, error messages, warnings, repair notes, review queues, summaries, notifications, logs, indexes, exports, publications, synchronization outputs, backup outputs, agent instructions, or implementation displays.

Workflow convenience, routing efficiency, review speed, automation convenience, migration convenience, indexing convenience, publication convenience, or implementation convenience MUST NOT override Privacy Classification.

Validation MUST preserve workflow authority boundaries.

Workflow completion MUST NOT imply validation success unless the applicable workflow specification explicitly defines that behavior within a controlled scope.

Workflow completion MUST NOT imply Authority Level.

Workflow completion MUST NOT imply approval outside the workflow scope.

Workflow completion MUST NOT imply publication readiness.

Workflow completion MUST NOT imply export readiness.

Workflow completion MUST NOT imply privacy clearance.

A workflow-generated validation result MAY support review, but it does not create final authority unless a future governed workflow standard, validation specification, or implementation profile explicitly defines that behavior within a controlled scope.

Validation MUST preserve workflow lifecycle boundaries.

A workflow MAY transition Lifecycle State only where a governed workflow specification explicitly permits that transition.

A workflow validation result MUST NOT silently approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, promote, or demote a governed entity unless that behavior is defined by a future governed workflow or lifecycle specification.

Validation MUST preserve workflow relationship boundaries.

A workflow MAY create, route, review, approve, reject, repair, or preserve relationships only where a governed workflow, relationship specification, or implementation profile permits that behavior.

Workflow-created relationships SHOULD preserve provenance, review status, authority boundaries, privacy boundaries, lifecycle state, validation status, and compatibility expectations where those affect governed meaning.

Validation MUST preserve workflow Source Reference boundaries.

A workflow MAY create, route, review, approve, reject, repair, or preserve Source References only where a governed workflow, source-reference specification, or implementation profile permits that behavior.

Workflow-created Source References SHOULD preserve source target meaning, source-reference provenance, source privacy, source authority boundaries, source reliability boundaries, validation status, and compatibility expectations where those affect governed meaning.

Validation MUST preserve workflow provenance boundaries.

A workflow MAY create provenance.

A workflow MAY update provenance.

A workflow MAY preserve provenance.

A workflow MUST NOT treat workflow memory as governed provenance unless the workflow output preserves provenance in a governed, portable, reviewable, privacy-respecting, and implementation-independent form.

Validation MUST preserve workflow compatibility.

Workflow-generated validation meaning SHOULD remain understandable when a governed entity is renamed, moved, copied, imported, exported, migrated, backed up, restored, synchronized, indexed where permitted, published where permitted, validated by a different validator, processed by an agent, processed by a different workflow, or accessed through a different implementation.

Validation MAY identify workflow-related issues, including:

- workflow output missing validation scope;
- workflow output missing provenance;
- workflow output missing review status;
- workflow output missing repair status;
- workflow completion confused with validation success;
- workflow completion confused with approval;
- workflow completion confused with authority;
- workflow completion confused with privacy clearance;
- workflow status confused with Lifecycle State;
- workflow route exposing restricted information;
- workflow output exceeding permitted scope;
- workflow-generated relationship lacking review;
- workflow-generated Source Reference lacking provenance;
- workflow-generated metadata lacking validation scope;
- workflow-generated provenance incomplete;
- workflow repair changing governed meaning without review;
- workflow transition missing transition provenance;
- workflow output relying on hidden implementation state;
- workflow output losing compatibility during import, export, migration, backup, synchronization, indexing, or publication.

Validation MUST remain distinguishable from workflow execution.

Successful workflow execution does not automatically mean validation success.

Successful workflow execution does not automatically mean approval outside the workflow scope.

Successful workflow execution does not automatically mean authority.

Successful workflow execution does not automatically mean privacy clearance.

Successful workflow execution does not automatically mean publication, export, synchronization, indexing, backup, or downstream-use permission.

Validation SHOULD support workflow-output repair.

Workflow-output repair MAY include adding validation scope, adding provenance, clarifying review status, correcting overstated completion, limiting exposed information, requesting human review, requesting agent support, requesting privacy review, requesting authority review, requesting lifecycle review, requesting relationship review, requesting Source Reference review, requesting provenance repair, or marking the workflow output as needing repair.

Workflow-output repair MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, validation history, compatibility, and historical traceability where those affect governed meaning.

Validation and Workflows are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what workflow behavior was validated, what workflow expectations were checked, whether workflow-related issues exist, what review or repair remains required, what privacy boundaries apply, and whether workflow-generated validation meaning remains scoped, reviewable, portable, and implementation-independent.

## 19. Validation and Implementations

Validation and Implementations are related but distinct concepts within The Brain Standard.

An Implementation is any software, vault, database, file system, interface, plugin, automation, service, agent system, workflow environment, validator, reference implementation, or tool that realizes The Brain Standard in practice.

Validation checks whether a governed entity, implementation behavior, implementation profile, implementation output, implementation-generated metadata, implementation-generated provenance, implementation-generated relationship, implementation-generated validation result, import behavior, export behavior, migration behavior, backup behavior, restoration behavior, synchronization behavior, indexing behavior, publication behavior, or downstream-use behavior satisfies applicable expectations within a defined Validation Scope.

Implementations MAY support validation.

Implementations MAY display validation information.

Implementations MAY store validation information.

Implementations MAY route validation information.

Implementations MAY perform validation checks.

Implementations MAY report validation results.

Implementations MAY preserve validation history.

Implementations MUST NOT define validation meaning by themselves.

Implementation Validation MAY apply to:

- software tools;
- vaults;
- databases;
- file systems;
- interfaces;
- plugins;
- automations;
- services;
- validator tools;
- reference implementations;
- agent systems;
- workflow environments;
- storage systems;
- indexing systems;
- synchronization systems;
- backup systems;
- restoration systems;
- publication systems;
- import processes;
- export processes;
- migration processes;
- downstream-use processes.

Implementation Validation SHALL be explicit where implementation behavior affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, governance, or downstream use.

Validation MUST preserve implementation independence.

A governed entity MUST remain interpretable without depending on a single implementation, plugin, database, user interface, cache, dashboard, graph view, search index, tag convention, folder convention, filename convention, hidden application state, workflow memory, agent memory, or undocumented implementation behavior.

Validation MUST preserve validation meaning across implementation replacement.

A governed entity SHOULD preserve validation meaning when moved from one compliant implementation to another.

A validation result SHOULD remain understandable when an implementation is replaced, upgraded, deprecated, unavailable, migrated away from, or no longer used.

Validation MUST preserve implementation role boundaries.

An implementation may support validation without owning final validation meaning.

An implementation may display validation information without creating validation success.

An implementation may cache validation information without becoming the authoritative record of validation.

An implementation may filter or sort validation information without changing validation status.

An implementation may report validation issues without approving repair.

An implementation may support repair without silently changing governed meaning.

Validation MUST preserve implementation provenance.

Implementation-supported validation SHOULD preserve enough provenance to determine:

- what implementation performed or supported validation where applicable;
- what version or profile was used where applicable;
- what governed entity was processed;
- what Validation Scope applied;
- what rule set, standard, specification, workflow profile, agent profile, implementation profile, import process, export process, migration process, or downstream-use context was used;
- what output was produced;
- what errors were identified;
- what warnings were identified;
- what repair was recommended;
- what review occurred;
- what review remains required;
- what downstream-use limits remain.

Validation MUST preserve implementation privacy boundaries.

An implementation MUST NOT expose restricted information through dashboards, search results, previews, graph views, links, backlinks, indexes, embeddings, caches, logs, exports, publications, synchronization outputs, backup outputs, workflow messages, agent instructions, validator reports, error messages, warning messages, repair notes, or user-interface labels.

Implementation convenience, search quality, graph usefulness, indexing quality, automation convenience, synchronization convenience, backup convenience, migration convenience, publication convenience, or user-interface convenience MUST NOT override Privacy Classification.

Validation MUST preserve implementation authority boundaries.

Implementation visibility MUST NOT imply validation success.

Implementation visibility MUST NOT imply Authority Level.

Implementation visibility MUST NOT imply approval.

Implementation visibility MUST NOT imply publication readiness.

Implementation visibility MUST NOT imply export readiness.

Implementation visibility MUST NOT imply privacy clearance.

Implementation visibility MUST NOT imply downstream-use permission.

Validation MUST preserve implementation lifecycle boundaries.

An implementation status, folder location, tag, dashboard value, database flag, plugin field, icon, color, view, or cache state MUST NOT silently become Lifecycle State.

An implementation-generated validation result MUST NOT silently approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, promote, or demote a governed entity unless a future governed workflow, lifecycle specification, validation specification, or implementation profile explicitly permits that behavior within a controlled scope.

Validation MUST preserve implementation relationship boundaries.

Implementation-specific links, backlinks, graph edges, database relations, search associations, vector similarities, plugin connections, or interface groupings MUST NOT become governed Relationships merely because an implementation displays or uses them.

A compliant implementation SHOULD preserve governed Relationships separately from implementation-specific linking behavior where relationship meaning affects interpretation, provenance, authority, privacy, lifecycle handling, validation, compatibility, publication, export, migration, or downstream use.

Validation MUST preserve implementation Source Reference boundaries.

Implementation-specific source links, file attachments, URLs, citations, previews, cached source records, search results, or plugin references MUST NOT become governed Source References merely because an implementation displays or stores them.

A compliant implementation SHOULD preserve governed Source References separately from implementation-specific source-handling behavior where source-reference meaning affects evidence, provenance, authority, privacy, validation, compatibility, publication, export, migration, or downstream use.

Validation MUST preserve implementation provenance boundaries.

Implementation history, interface history, database history, plugin logs, automation logs, cache records, or hidden application state MUST NOT replace governed Provenance.

A compliant implementation SHOULD preserve provenance in a portable, reviewable, privacy-respecting, and implementation-independent form where provenance affects interpretation, authority, privacy, lifecycle handling, validation, compatibility, import, export, migration, publication, or downstream use.

Validation MUST preserve implementation compatibility.

Implementation-generated validation meaning SHOULD remain understandable when a governed entity is renamed, moved, copied, imported, exported, migrated, backed up, restored, synchronized, indexed where permitted, published where permitted, validated by a different validator, processed by an agent, processed by a workflow, or accessed through a different implementation.

Validation MAY identify implementation-related issues, including:

- implementation output missing Validation Scope;
- implementation output missing provenance;
- implementation output missing review status;
- implementation output missing repair status;
- implementation visibility confused with validation success;
- implementation visibility confused with approval;
- implementation visibility confused with Authority Level;
- implementation visibility confused with Privacy Classification;
- implementation status confused with Lifecycle State;
- implementation-specific links treated as governed Relationships;
- implementation-specific source links treated as governed Source References;
- implementation logs treated as governed Provenance;
- implementation cache treated as governed validation history;
- implementation labels treated as governed metadata;
- implementation search ranking treated as validation evidence;
- implementation graph position treated as relationship meaning;
- implementation-generated output exposing restricted information;
- implementation output exceeding permitted scope;
- implementation output relying on hidden application state;
- implementation output losing compatibility during import, export, migration, backup, synchronization, indexing, publication, or restoration.

Validation MUST remain distinguishable from implementation execution.

Successful implementation execution does not automatically mean validation success.

Successful implementation execution does not automatically mean workflow completion.

Successful implementation execution does not automatically mean approval.

Successful implementation execution does not automatically mean authority.

Successful implementation execution does not automatically mean privacy clearance.

Successful implementation execution does not automatically mean publication, export, synchronization, indexing, backup, restoration, or downstream-use permission.

Validation SHOULD support implementation-output repair.

Implementation-output repair MAY include adding Validation Scope, adding provenance, clarifying review status, correcting overstated implementation status, limiting exposed information, separating implementation-specific links from governed Relationships, separating implementation-specific source links from governed Source References, preserving governed Provenance outside hidden logs, requesting human review, requesting workflow review, requesting agent support, requesting privacy review, requesting authority review, requesting lifecycle review, or marking the implementation output as needing repair.

Implementation-output repair MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, validation history, compatibility, and historical traceability where those affect governed meaning.

Validation and Implementations are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what implementation behavior was validated, what implementation expectations were checked, whether implementation-related issues exist, what review or repair remains required, what privacy boundaries apply, and whether implementation-supported validation meaning remains scoped, reviewable, portable, and implementation-independent.

## 20. Validation During Import, Export, and Migration

Validation During Import, Export, and Migration defines how Validation behaves when governed entities enter, leave, or move between compliant environments, storage systems, implementations, repositories, vaults, schemas, file formats, workflow environments, agent environments, validator environments, or downstream-use contexts.

Import is the process of bringing governed entities into a compliant environment.

Export is the process of producing governed entities from a compliant environment for use elsewhere.

Migration is the process of moving governed entities between storage systems, implementations, representations, schemas, vaults, repositories, file formats, workflow environments, agent environments, validator environments, or tool environments.

Validation during Import, Export, and Migration exists so that governed entities remain meaningful, portable, traceable, reviewable, privacy-respecting, provenance-aware, compatible, and implementation-independent when they move.

Import, Export, and Migration Validation MAY apply to:

- Knowledge Objects;
- Knowledge Records;
- Source Material where applicable;
- Source References;
- provenance records;
- relationships;
- metadata records;
- lifecycle states;
- authority levels;
- privacy classifications;
- validation states;
- validation results;
- validation assignments;
- validation reviews;
- validation evidence;
- validation errors;
- validation warnings;
- workflow outputs;
- agent outputs;
- implementation outputs;
- import records;
- export records;
- migration records;
- governed documents;
- decisions;
- other governed entities.

Import, Export, and Migration Validation SHALL be explicit where movement affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, compatibility, publication, synchronization, indexing, backup, restoration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

Validation MUST preserve Object Identity during Import, Export, and Migration.

A governed entity MUST NOT receive a new stable Object Identity merely because it was imported, exported, migrated, backed up, restored, synchronized, indexed, published, transformed, serialized, deserialized, converted, copied, moved, or processed by a different implementation.

Where identity mapping is required, validation SHOULD preserve enough information to determine the original identity, mapped identity, legacy identity, temporary identity, source identity, redirect, duplicate risk, merge history, split history, and identity repair requirements where applicable.

Validation MUST preserve metadata during Import, Export, and Migration.

Metadata SHOULD remain explicit, interpretable, portable, reviewable, privacy-respecting, compatible, and distinguishable from hidden implementation behavior after movement.

Metadata loss, metadata collapse, metadata reinterpretation, metadata exposure, metadata regeneration, or metadata mapping failure SHOULD be reported where metadata affects governed meaning or downstream use.

Validation MUST preserve Relationships during Import, Export, and Migration.

Relationships SHOULD preserve participants, type, direction, context, provenance, lifecycle state, authority, privacy, validation status, compatibility, and implementation independence after movement.

A migrated link, backlink, graph edge, database relation, or implementation-specific association MUST NOT be treated as a governed Relationship unless the applicable relationship expectations are preserved.

Validation MUST preserve Source References during Import, Export, and Migration.

Source References SHOULD preserve source target meaning, source identifiers, citation support where applicable, source availability context, source privacy, source authority boundaries, source reliability boundaries, source-reference provenance, and compatibility after movement.

A moved file path, URL, attachment, citation string, search result, plugin link, or implementation-specific source pointer MUST NOT be treated as a valid governed Source Reference unless the applicable source-reference expectations are preserved.

Validation MUST preserve Provenance during Import, Export, and Migration.

Provenance SHOULD preserve origin, source, reasoning, transformation, creator, editor, agent, workflow, validation, review, evidence, attribution, import history, export history, migration history, backup history, restoration history, synchronization history, indexing history, publication history, and change context where those affect governed meaning.

Movement history SHOULD be preserved where it affects traceability, compatibility, authority, privacy, lifecycle handling, validation, publication, export, migration, restoration, or downstream use.

Validation MUST preserve Lifecycle State during Import, Export, and Migration.

Lifecycle State SHOULD remain distinguishable from movement state.

Import success, export success, or migration success MUST NOT automatically approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, promote, or demote a governed entity unless a future governed workflow, lifecycle specification, validation specification, or implementation profile explicitly permits that behavior within a controlled scope.

Validation MUST preserve Authority Level during Import, Export, and Migration.

Authority Level SHOULD remain scoped, traceable, reviewable, and distinguishable from validation success, source availability, implementation visibility, import success, export success, migration success, publication status, and downstream-use permission.

A governed entity MUST NOT gain or lose Authority Level merely because movement succeeded or failed.

Validation MUST preserve Privacy Classification during Import, Export, and Migration.

Privacy Classification SHALL take precedence over movement convenience.

A governed entity MUST NOT become exportable, publishable, synchronizable, indexable, backup-permitted, agent-accessible, workflow-accessible, implementation-accessible, or downstream-use permitted merely because it passed a validation check or movement check.

Import, Export, and Migration Validation MUST NOT expose restricted information through mappings, logs, reports, error messages, warning messages, repair notes, manifests, indexes, caches, exported packages, migration summaries, agent outputs, workflow messages, or implementation displays.

Validation MUST preserve Validation State during Import, Export, and Migration.

Validation State, Validation Scope, Validation Result, Validation Assignment, Validation Review, validation evidence, validation errors, validation warnings, validation history, and validation repair status SHOULD remain understandable after movement where those affect governed meaning, compatibility, review, repair, publication, export, migration, or downstream use.

A validation result MUST NOT be treated as universally reusable after movement unless the applicable Validation Scope, standard, specification, workflow, implementation profile, import process, export process, migration process, or compatibility review explicitly permits that reuse.

Validation MUST distinguish movement validation from full conformance.

Import success does not automatically mean full conformance.

Export success does not automatically mean full conformance.

Migration success does not automatically mean full conformance.

Backup success does not automatically mean full conformance.

Restoration success does not automatically mean full conformance.

Synchronization success does not automatically mean full conformance.

Indexing success does not automatically mean full conformance.

Publication success does not automatically mean full conformance.

A movement process MAY pass a narrow movement validation scope while the governed entity still requires structural validation, identity validation, metadata validation, relationship validation, source-reference validation, provenance validation, lifecycle validation, authority validation, privacy validation, compatibility validation, workflow validation, agent validation, implementation validation, or conformance validation.

Validation SHOULD preserve movement provenance.

Import, Export, and Migration Validation SHOULD preserve enough provenance to determine:

- what governed entity moved;
- what movement process applied;
- what source environment was used where applicable;
- what target environment was used where applicable;
- what mapping was used where applicable;
- what Validation Scope applied;
- what rule set, standard, specification, workflow, agent, implementation profile, import process, export process, migration process, or downstream-use context was used;
- what was preserved;
- what was transformed;
- what was omitted;
- what was redacted;
- what was blocked;
- what was repaired;
- what errors were found;
- what warnings were found;
- what review remains required;
- what repair remains required;
- what downstream-use limits remain.

Validation MAY identify Import, Export, and Migration issues, including:

- Object Identity not preserved;
- identity mapping missing;
- metadata lost;
- metadata collapsed;
- metadata exposed;
- Relationship lost;
- Relationship direction lost;
- Relationship provenance lost;
- Source Reference broken;
- Source Reference target unclear;
- Source Material unavailable where required;
- provenance lost;
- provenance exposed;
- lifecycle state lost;
- lifecycle state confused with movement state;
- Authority Level lost;
- Authority Level expanded beyond scope;
- Privacy Classification lost;
- privacy boundary weakened;
- Validation State lost;
- Validation Scope lost;
- validation history lost;
- validation result overstated after movement;
- import success treated as full conformance;
- export success treated as publication permission;
- migration success treated as validation success;
- backup success treated as access permission;
- synchronization success treated as privacy clearance;
- indexing success treated as publication readiness;
- implementation-specific state treated as governed meaning;
- movement process exposing restricted information;
- movement process losing compatibility.

Validation SHOULD support movement repair.

Movement repair MAY include correcting identity mappings, restoring metadata, repairing relationships, repairing Source References, restoring provenance, clarifying lifecycle state, clarifying Authority Level, restoring Privacy Classification, restoring Validation State, adding movement provenance, limiting exposed information, redacting restricted material, blocking unsafe movement, requesting human review, requesting privacy review, requesting authority review, requesting lifecycle review, requesting relationship review, requesting Source Reference review, requesting provenance repair, requesting compatibility review, or marking the moved entity as needing repair.

Movement repair MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, validation history, compatibility, and historical traceability where those affect governed meaning.

Validation During Import, Export, and Migration is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations can determine what moved, what was checked, what was preserved, what changed, what was lost, what was redacted, what was blocked, what repair remains required, what privacy boundaries apply, and whether validation meaning remains scoped, reviewable, portable, and implementation-independent after movement.

## 21. Conformance and Success Criteria

Conformance and Success Criteria define how KS-0009 is satisfied at the standard level.

KS-0009 conformance means a governed entity, standard, specification, workflow, agent, storage system, implementation, validator, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, publication process, or downstream-use process preserves Validation behavior as defined by this document.

KS-0009 conformance is evaluated within a defined Conformance Scope.

A conformance claim MUST identify or support identification of what scope is being claimed.

A narrow conformance claim MUST NOT be treated as full conformance.

A structural validation pass MUST NOT be treated as full KS-0009 conformance unless all required validation categories, requirements, scopes, boundaries, and preservation expectations for the claimed scope are satisfied.

A system, file, object, record, workflow, agent, validator, implementation, import process, export process, migration process, backup process, restoration process, synchronization process, indexing process, publication process, or downstream-use process MUST NOT claim conformance merely because it can display, store, route, cache, index, export, import, migrate, or report validation information.

Conformance Validation MAY apply to:

- validation definition;
- validation requirements;
- validation categories;
- Validation Scope;
- Validation Assignment;
- Validation Review;
- validation and Object Identity;
- validation and metadata;
- validation and relationships;
- validation and Source References;
- validation and provenance;
- validation and Lifecycle State;
- validation and Authority Level;
- validation and Privacy Classification;
- validation and agents;
- validation and workflows;
- validation and implementations;
- validation during import, export, and migration;
- compatibility;
- privacy preservation;
- implementation independence;
- downstream-use limits.

A KS-0009-conformant governed entity SHOULD make Validation explicit where validation affects meaning, review, repair, lifecycle handling, authority handling, privacy handling, relationships, Source References, provenance, compatibility, publication, synchronization, indexing, backup, import, export, migration, workflow behavior, agent behavior, implementation behavior, governance, or downstream use.

A KS-0009-conformant validation result SHOULD identify or support identification of:

- what governed entity was validated;
- what Validation Scope applied;
- what Validation Result was produced;
- what Validation State applies;
- what standard, specification, rule set, workflow, agent, implementation profile, import process, export process, migration process, or downstream-use context was used;
- who or what performed validation where applicable;
- when validation occurred where applicable;
- what evidence supports the result;
- what errors were found;
- what warnings were found;
- what repair remains required;
- what review remains required;
- what privacy limits remain;
- what compatibility limits remain;
- what downstream-use limits remain.

A KS-0009-conformant validator MUST NOT overstate its scope.

A validator that checks only structure MUST NOT claim full validation.

A validator that checks only metadata MUST NOT claim full validation.

A validator that checks only privacy MUST NOT claim full validation.

A validator that checks only import, export, migration, backup, restoration, synchronization, indexing, publication, workflow behavior, agent behavior, or implementation behavior MUST NOT claim full validation unless the applicable Conformance Scope explicitly defines that as complete.

A KS-0009-conformant workflow MUST preserve validation boundaries.

Workflow completion MUST NOT imply validation success unless the applicable workflow specification explicitly defines that behavior within a controlled scope.

Workflow completion MUST NOT imply approval, Authority Level, Privacy Classification, publication readiness, export readiness, synchronization readiness, indexing readiness, backup readiness, restoration readiness, implementation permission, agent permission, workflow permission, or downstream-use permission unless a future governed specification explicitly defines that behavior within a controlled scope.

A KS-0009-conformant agent MUST preserve validation boundaries.

Agent confidence MUST NOT imply validation success.

Agent confidence MUST NOT imply Authority Level.

Agent confidence MUST NOT imply approval.

Agent confidence MUST NOT imply privacy clearance.

Agent confidence MUST NOT imply publication readiness, export readiness, synchronization readiness, indexing readiness, backup readiness, restoration readiness, implementation permission, workflow permission, or downstream-use permission unless a future governed specification explicitly defines that behavior within a controlled scope.

A KS-0009-conformant implementation MUST preserve validation boundaries.

Implementation visibility MUST NOT imply validation success.

Implementation visibility MUST NOT imply Authority Level.

Implementation visibility MUST NOT imply approval.

Implementation visibility MUST NOT imply Privacy Classification.

Implementation visibility MUST NOT imply publication readiness, export readiness, synchronization readiness, indexing readiness, backup readiness, restoration readiness, agent permission, workflow permission, implementation permission, or downstream-use permission unless a future governed specification explicitly defines that behavior within a controlled scope.

A KS-0009-conformant import, export, or migration process MUST preserve validation boundaries.

Import success MUST NOT imply full conformance.

Export success MUST NOT imply full conformance.

Migration success MUST NOT imply full conformance.

Backup success MUST NOT imply full conformance.

Restoration success MUST NOT imply full conformance.

Synchronization success MUST NOT imply full conformance.

Indexing success MUST NOT imply full conformance.

Publication success MUST NOT imply full conformance.

A KS-0009-conformant process MUST preserve Privacy Classification.

Validation success MUST NOT create access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, restoration permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission.

Privacy Classification SHALL take precedence over operational convenience where privacy and convenience conflict.

A KS-0009-conformant process MUST preserve Object Identity.

Validation MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Object Identity SHOULD remain stable across validation, repair, review, import, export, migration, backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, implementation behavior, and implementation replacement.

A KS-0009-conformant process MUST preserve Metadata, Relationships, Source References, Provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, compatibility, and historical traceability where those affect governed meaning.

A KS-0009-conformant process SHOULD support review and repair.

Where validation fails, produces warnings, becomes stale, becomes disputed, becomes incomplete, exceeds scope, exposes privacy risk, loses provenance, breaks relationships, breaks Source References, creates lifecycle ambiguity, creates authority ambiguity, creates privacy ambiguity, creates compatibility risk, or creates implementation lock-in, the issue SHOULD remain visible enough for appropriate review or repair within privacy boundaries.

KS-0009 does not define exact conformance test suites.

KS-0009 does not define exact validator tools.

KS-0009 does not define exact validation values.

KS-0009 does not define exact validation rule syntax.

KS-0009 does not define exact error codes.

KS-0009 does not define exact warning formats.

KS-0009 does not define exact schemas.

KS-0009 does not define exact metadata fields.

KS-0009 does not define exact APIs.

KS-0009 does not define exact user-interface behavior.

A future conformance specification MAY define exact conformance levels, conformance profiles, validation profiles, test suites, validator responsibilities, required evidence, required metadata, allowed values, rule syntax, error formats, warning formats, implementation mappings, import mappings, export mappings, migration mappings, backup mappings, restoration mappings, synchronization mappings, indexing mappings, publication mappings, agent handling rules, workflow triggers, and serialization syntax.

Such specifications are valid only when they preserve the Validation behavior defined by KS-0009.

KS-0009 is successful when Validation remains:

- explicit;
- scoped;
- interpretable;
- portable;
- traceable;
- reviewable;
- repair-supporting;
- privacy-respecting;
- provenance-aware;
- compatible;
- implementation-independent;
- distinguishable from Object Identity;
- distinguishable from Metadata;
- distinguishable from Relationships;
- distinguishable from Source References;
- distinguishable from Provenance;
- distinguishable from Lifecycle State;
- distinguishable from Authority Level;
- distinguishable from Privacy Classification;
- distinguishable from workflow completion;
- distinguishable from agent confidence;
- distinguishable from implementation visibility;
- distinguishable from import success;
- distinguishable from export success;
- distinguishable from migration success;
- distinguishable from publication status;
- distinguishable from downstream-use permission.

KS-0009 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, backup processes, restoration processes, synchronization processes, indexing systems, publication processes, implementations, and downstream users can determine what validation applies to a governed entity, what scope was used, what result was produced, what evidence supports the result, what repair or review remains, what privacy boundaries apply, whether conformance is being claimed accurately, and whether Validation remains meaningful across time, tools, storage systems, workflows, agents, validators, and implementation replacement.
