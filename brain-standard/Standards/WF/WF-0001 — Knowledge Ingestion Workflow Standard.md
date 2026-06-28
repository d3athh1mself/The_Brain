# WF-0001 — Knowledge Ingestion Workflow Standard

Document ID: WF-0001
Title: Knowledge Ingestion Workflow Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 4 — Workflow Engine
Milestone: 4.1 — Knowledge Ingestion Workflow Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and workflow rules are interpreted within WF-0001.

Where conflicts arise between workflow behavior, workflow steps, workflow states, workflow outputs, Source Material, Knowledge Records, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, agent behavior, implementation behavior, import behavior, export behavior, migration behavior, publication behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

WF-0001 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

WF-0001 depends on the Phase 1 Knowledge Standards because ingestion workflows must preserve knowledge meaning without redefining it.

WF-0001 depends on the Phase 2 Storage Standards because ingestion workflows may locate, preserve, route, stage, reference, archive, or store Source Material, drafts, Knowledge Records, supporting assets, validation outputs, workflow logs, and approved records without allowing storage location to define meaning.

WF-0001 depends on AG-0001 because agents may assist ingestion workflows only within governed operating boundaries.

WF-0001 defines workflow behavior at the standard level.

WF-0001 does not define exact folder paths, exact filenames, exact metadata field names, exact Markdown front matter syntax, exact schemas, exact validation tooling, exact agent prompts, exact model behavior, exact Obsidian behavior, exact Codex behavior, exact automation scripts, exact user-interface behavior, or exact implementation-specific routing.

Those concerns belong to later workflow specifications, storage specifications, agent specifications, implementation profiles, validation specifications, templates, operational guides, and reference implementations.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Workflow Engine refers to Layer 4 of The Brain Standard, responsible for defining repeatable workflows that coordinate knowledge capture, transformation, validation, review, maintenance, publication, synchronization, and automation.
- Workflow refers to a repeatable governed process that coordinates human actions, agent actions, storage actions, validation actions, review actions, approval actions, or implementation actions.
- Knowledge Ingestion refers to the workflow process by which incoming Source Material, captured information, notes, documents, messages, records, files, datasets, media, observations, or other inputs are assessed, classified, transformed, reviewed, and routed toward governed knowledge use.
- Intake refers to the initial receipt, capture, registration, or staging of material before it becomes a Knowledge Record or is rejected, deferred, archived, quarantined, or routed elsewhere.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Draft Knowledge Record refers to a Knowledge Record that has been created or proposed through ingestion but has not yet completed required review, validation, approval, rejection, repair, or routing.
- Ingestion Candidate refers to Source Material, captured information, extracted content, proposed knowledge, draft record, or other input being evaluated through the ingestion workflow.
- Extraction refers to selecting, copying, transcribing, parsing, summarizing, segmenting, or otherwise taking information from Source Material for possible use in a Knowledge Record, relationship, Source Reference, provenance record, validation result, workflow output, or agent output.
- Transformation refers to changing Source Material, extracted content, or prior knowledge into another representation, summary, translation, classification, interpretation, structured record, derived object, migrated form, or implementation-specific representation.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Validation refers to the process of checking whether a governed entity satisfies applicable standards, specifications, metadata expectations, provenance expectations, relationship expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Human Review refers to review performed by a human to confirm, correct, reject, approve, limit, escalate, or route workflow outputs where governed review is required.
- Agent Assistance refers to agent participation in ingestion through reading, extraction, summarization, classification, metadata suggestion, relationship suggestion, validation support, draft preparation, issue detection, routing recommendation, or reporting within authorized boundaries.
- Workflow Output refers to any record, draft, classification, metadata proposal, Source Reference, provenance entry, relationship proposal, validation result, review note, routing decision, rejection record, repair request, log entry, or other artifact created by or through a workflow.
- Workflow State refers to the current processing position of an ingestion candidate within the workflow.
- Workflow Log refers to a traceable record of material actions, decisions, outputs, actors, agents, validation results, review points, approvals, rejections, repairs, escalations, or exceptions associated with a workflow.
- Approval refers to formal acceptance of a governed entity for use within a defined scope.
- Rejection refers to a governed decision that an ingestion candidate, draft, output, or proposed change is not accepted for the intended use.
- Repair refers to correction of structural, metadata, identity, relationship, provenance, source-reference, lifecycle, authority, privacy, validation, storage, agent, workflow, implementation, import, export, or migration issues identified during ingestion.
- Quarantine refers to isolation or withholding from normal use because of unresolved validity, safety, privacy, compatibility, source, provenance, or integrity concerns.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of WF-0001 is to define the standard-level workflow for ingesting Source Material and captured information into The Brain Standard.

WF-0001 defines how incoming material is received, staged, assessed, classified, extracted, transformed, referenced, validated, reviewed, repaired, approved, rejected, archived, quarantined, or routed toward Knowledge Records and downstream use.

Knowledge ingestion exists so that raw information does not become governed knowledge merely because it was captured, stored, summarized, indexed, processed by an agent, placed in a folder, imported into a vault, or referenced by an implementation.

WF-0001 exists to prevent ingestion confusion.

Ingestion confusion occurs when humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, or implementations cannot reliably determine:

- whether incoming material is Source Material, extracted content, a draft Knowledge Record, an approved Knowledge Record, a rejected candidate, a quarantined item, a workflow output, an implementation artifact, or another governed entity;
- whether Source Material has been preserved separately from Knowledge Records;
- whether a Knowledge Record has sufficient Object Identity, metadata, Source References, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, and compatibility context;
- whether agent-generated extraction, classification, summarization, metadata, relationships, validation results, or draft records have been reviewed where review is required;
- whether workflow completion has been confused with approval;
- whether validation has been confused with authority;
- whether storage placement has been confused with lifecycle state, privacy classification, or knowledge meaning;
- whether Source Material has been transformed without preserving provenance;
- whether restricted material has been exposed, indexed, summarized, exported, synchronized, published, or made available to agents without authorization;
- whether an ingestion candidate may be used downstream.

WF-0001 defines standard-level behavior for:

- intake;
- ingestion candidates;
- Source Material handling;
- source preservation;
- extraction;
- transformation;
- draft Knowledge Record creation;
- metadata suggestion and assignment;
- Source Reference creation;
- provenance creation;
- relationship suggestion;
- Lifecycle State handling;
- Authority Level handling;
- Privacy Classification handling;
- Validation handling;
- human review;
- agent assistance;
- approval;
- rejection;
- repair;
- quarantine;
- storage routing;
- workflow logging;
- workflow traceability;
- workflow outputs;
- workflow exceptions;
- downstream readiness.

WF-0001 does not define exact metadata fields, exact schemas, exact Markdown templates, exact folder paths, exact filenames, exact source archive layouts, exact agent prompts, exact validation scripts, exact review forms, exact implementation settings, exact user-interface behavior, exact automation triggers, or exact tool-specific ingestion behavior.

Those concerns belong to later workflow specifications, storage specifications, schema specifications, validation specifications, agent role specifications, implementation profiles, templates, and operational guides.

WF-0001 defines ingestion workflow behavior at the standard level.

A future specification MAY define exact ingestion states, required workflow fields, workflow log formats, intake forms, review checklists, metadata extraction rules, Source Reference formats, provenance fields, validation checks, agent task profiles, storage routing rules, import rules, export rules, migration rules, or automation behavior.

Such specifications are valid only when they preserve the ingestion behavior defined by WF-0001.

The primary purpose of WF-0001 is to ensure that incoming material becomes governed knowledge only through an explicit, traceable, reviewable, privacy-respecting, validation-aware, implementation-independent workflow.

WF-0001 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine:

- what material entered the ingestion workflow;
- where the material came from;
- what Source Material was preserved;
- what extraction or transformation occurred;
- what Knowledge Record, if any, was created;
- what Object Identity applies where applicable;
- what metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation apply;
- what agent assistance occurred where applicable;
- what human review occurred where required;
- what was approved, rejected, repaired, quarantined, archived, or routed;
- whether downstream use is permitted;
- whether ingestion behavior remains meaningful across storage replacement, workflow replacement, agent replacement, implementation replacement, import, export, migration, backup, restoration, synchronization, indexing, and publication.

## 2. Relationship to Prior Standards

WF-0001 is subordinate to and derived from the constitutional foundation of The Brain Standard.

WF-0001 depends on:

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
- KS-0009 — Validation Standard;
- SS-0001 — Storage Architecture Standard;
- SS-0002 — Storage Layout Specification;
- AG-0001 — Agent Operating Boundaries Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

WF-0001 applies that purpose by defining an ingestion workflow that transforms incoming information into governed knowledge without making knowledge dependent on any single tool, folder layout, agent system, workflow engine, model, database, interface, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

WF-0001 applies those principles by requiring ingestion workflows to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- Source Material distinction;
- metadata clarity;
- relationship clarity;
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

WF-0001 belongs to Layer 4 — Workflow Engine.

Layer 4 coordinates repeatable workflows across knowledge, storage, agents, review, validation, maintenance, publication, synchronization, and automation.

WF-0001 MUST preserve the Layer 4 boundary.

A workflow may coordinate governed action.

A workflow MUST NOT silently redefine knowledge meaning, Object Identity, metadata meaning, relationship meaning, Source Reference meaning, provenance meaning, Lifecycle State, Authority Level, Privacy Classification, Validation, storage meaning, agent authority, implementation behavior, or governance.

TB-0003 establishes the governance model for The Brain Standard.

WF-0001 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, WF-0001 has high authority within its workflow scope but remains subordinate to constitutional documents.

WF-0001 does not replace the governance lifecycle, authority hierarchy, approval expectations, review expectations, versioning expectations, supersession rules, ADR usage, RFC usage, compatibility review, or drift-prevention rules defined by TB-0003.

The Phase 1 Knowledge Standards define the meaning that ingestion workflows must preserve.

KS-0001 defines Knowledge Objects, Knowledge Records, Source Material distinction, and the minimum structural expectations needed for governed knowledge.

WF-0001 depends on KS-0001 because ingestion workflows create, propose, modify, validate, route, approve, reject, or preserve Knowledge Records.

KS-0002 defines Object Identity.

WF-0001 depends on KS-0002 because ingestion workflows may create new Knowledge Objects, detect duplicates, propose derivatives, route copies, preserve source identifiers, or flag identity conflicts.

An ingestion workflow MUST NOT assign, merge, split, replace, redirect, or reinterpret Object Identity silently.

KS-0003 defines metadata behavior.

WF-0001 depends on KS-0003 because ingestion workflows may extract, propose, assign, validate, repair, or preserve metadata.

Workflow-generated metadata MUST remain distinguishable from human-approved metadata, agent-generated metadata, implementation metadata, storage metadata, and hidden application behavior.

KS-0004 defines relationship behavior.

WF-0001 depends on KS-0004 because ingestion workflows may discover, propose, validate, reject, approve, repair, or preserve relationships.

An ingestion workflow MUST NOT treat inferred, agent-generated, implementation-generated, or storage-proximity-based links as approved relationships unless a governed review or specification permits that behavior.

KS-0005 defines Source Reference and Provenance behavior.

WF-0001 depends on KS-0005 because ingestion begins with Source Material and must preserve source distinction, Source References, evidence, attribution, extraction history, transformation history, agent activity, workflow activity, review history, import provenance, export provenance, migration provenance, and source availability context.

A Knowledge Record created through ingestion SHOULD preserve enough Source Reference and provenance context for future review.

KS-0006 defines Lifecycle State behavior.

WF-0001 depends on KS-0006 because ingestion candidates, Source References, draft Knowledge Records, relationships, workflow outputs, validation results, and approved records may require lifecycle states or lifecycle transitions.

Workflow State MUST remain distinguishable from Lifecycle State.

Workflow completion MUST NOT be treated as approval unless a future governed workflow specification explicitly defines that behavior.

KS-0007 defines Authority Level behavior.

WF-0001 depends on KS-0007 because ingestion workflows may assign, propose, limit, review, preserve, or escalate authority context.

Workflow completion, agent confidence, source existence, validation passing, storage routing, or implementation visibility MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior.

KS-0008 defines Privacy Classification behavior.

WF-0001 depends on KS-0008 because ingestion workflows may expose, route, summarize, index, synchronize, publish, export, or provide agent access to material only when privacy classification and access expectations permit that handling.

A workflow MUST NOT weaken Privacy Classification for convenience, automation, search, linking, validation, publication, export, synchronization, or implementation behavior.

KS-0009 defines Validation behavior.

WF-0001 depends on KS-0009 because ingestion workflows may validate structure, metadata, Object Identity, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, storage handling, agent activity, workflow outputs, import behavior, export behavior, and migration behavior.

Validation may support review and approval.

Validation MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that effect.

The Phase 2 Storage Standards define how storage supports ingestion without defining knowledge meaning.

WF-0001 depends on SS-0001 because ingestion workflows may stage, preserve, route, archive, back up, synchronize, index, import, export, or migrate Source Material, Knowledge Records, drafts, workflow logs, validation outputs, and supporting assets.

Storage location MUST NOT define Knowledge Object meaning, Lifecycle State, Authority Level, Privacy Classification, Validation State, or approval.

WF-0001 depends on SS-0002 because practical storage layout may support intake, staging, drafts, source preservation, review queues, approved records, rejected material, quarantine, archives, exports, and implementation-facing organization.

Storage layout may support workflow routing.

Storage layout MUST NOT replace explicit workflow state, lifecycle state, metadata, Source References, provenance, validation, review, or approval.

The Phase 3 Agent Framework defines how agents may participate in ingestion.

WF-0001 depends on AG-0001 because agents may assist ingestion only within governed boundaries.

Agents MAY assist with intake review, source classification, extraction, summarization, metadata suggestion, relationship suggestion, duplicate detection, validation support, draft preparation, issue detection, routing recommendations, repair recommendations, and workflow reporting.

Agents MUST NOT silently approve, reject, declassify, publish, export, migrate, delete, overwrite, supersede, validate as authoritative, assign final authority, govern privacy, redefine Object Identity, or transform Source Material into approved Knowledge Records without governed review where review is required.

WF-0001 is successful when it coordinates the prior standards into a repeatable ingestion process without weakening knowledge meaning, Object Identity, metadata boundaries, relationship behavior, Source Reference behavior, provenance preservation, Lifecycle State, Authority Level, Privacy Classification, Validation, storage boundaries, agent boundaries, implementation independence, governance, or practical daily usability.

## 3. Workflow Scope and Boundaries

WF-0001 applies to the ingestion of incoming material into The Brain Standard.

Incoming material MAY include:

- documents;
- notes;
- messages;
- emails;
- transcripts;
- bookmarks;
- web pages;
- PDFs;
- images;
- audio files;
- video files;
- datasets;
- code files;
- logs;
- forms;
- scans;
- research material;
- meeting notes;
- chat logs;
- observations;
- imported records;
- exported records from another system;
- migrated records;
- agent-generated drafts;
- workflow-generated drafts;
- implementation-generated artifacts;
- other material proposed for governed knowledge use.

WF-0001 governs the workflow behavior required to determine whether incoming material should become, support, modify, or be related to governed knowledge.

WF-0001 applies when a workflow performs or coordinates any of the following ingestion actions:

- receiving material;
- capturing material;
- registering material;
- staging material;
- classifying material;
- preserving Source Material;
- extracting information;
- transforming information;
- creating draft Knowledge Records;
- proposing Object Identity;
- detecting possible duplicates;
- proposing metadata;
- proposing relationships;
- creating Source References;
- creating provenance;
- assigning or proposing Lifecycle State;
- assigning or proposing Authority Level;
- assigning or proposing Privacy Classification;
- performing validation;
- routing for human review;
- routing for repair;
- routing for approval;
- routing for rejection;
- routing for quarantine;
- routing for archival;
- routing for storage;
- recording workflow logs;
- preparing material for downstream use.

WF-0001 applies to manual workflows, agent-assisted workflows, partially automated workflows, and future governed automated workflows.

A workflow MAY coordinate humans, agents, validators, storage systems, implementations, import processes, export processes, migration processes, backup processes, synchronization processes, indexing systems, publication processes, or other governed mechanisms.

A workflow MUST preserve the authority boundaries of the layers it coordinates.

A workflow MUST NOT silently redefine Layer 1 knowledge meaning.

A workflow MUST NOT silently redefine Object Identity, metadata meaning, relationship meaning, Source Reference meaning, provenance meaning, Lifecycle State, Authority Level, Privacy Classification, Validation, or compatibility expectations.

A workflow MUST NOT allow storage location, folder placement, filename, tag, index, search result, graph position, plugin field, workflow queue, workflow completion, agent output, implementation state, user-interface state, or hidden application state to become the sole source of governed meaning.

A workflow MUST NOT silently redefine Layer 2 storage meaning.

Storage may support intake, staging, routing, review, quarantine, archival, backup, export, migration, synchronization, indexing, implementation behavior, or practical use.

Storage MUST NOT become the source of knowledge meaning merely because an ingestion workflow places material in a folder, moves a file, creates a draft, archives a source, or routes a record.

A workflow MUST NOT silently redefine Layer 3 agent authority.

Agents may assist ingestion.

Agents MUST remain within authorized workflow scope, storage scope, privacy scope, source scope, review scope, validation scope, and permission scope.

Agent outputs MUST remain distinguishable from human decisions, workflow decisions, validation results, approved knowledge, authoritative records, and governed approvals.

A workflow MUST NOT silently redefine Layer 5 implementation behavior.

An implementation may execute, display, automate, index, route, validate, summarize, synchronize, publish, export, import, migrate, or log workflow activity.

Implementation behavior MUST NOT become a requirement of WF-0001 unless a future governed specification or implementation profile explicitly defines that behavior within its proper authority scope.

WF-0001 does not require every ingestion workflow to create a Knowledge Record.

An ingestion candidate MAY be:

- accepted for Knowledge Record drafting;
- preserved as Source Material only;
- linked to an existing Knowledge Record;
- used to update an existing Knowledge Record;
- routed for review;
- routed for repair;
- rejected;
- quarantined;
- archived;
- deferred;
- merged with another ingestion candidate;
- identified as a duplicate;
- treated as an implementation artifact;
- excluded from governed knowledge use.

WF-0001 does not require every ingestion workflow to use agents.

A compliant ingestion workflow MAY be fully manual.

A compliant ingestion workflow MAY be agent-assisted.

A compliant ingestion workflow MAY be partially automated.

A compliant ingestion workflow MAY become fully automated only where future governed standards, specifications, workflows, permissions, validation expectations, review expectations, privacy expectations, and exception-handling rules define that automation as safe and compliant for a limited scope.

WF-0001 does not define final publication rules.

Publication concerns belong to future workflow standards, publication specifications, privacy specifications, implementation profiles, and operational guides.

WF-0001 may identify when ingestion output appears ready for publication review, but ingestion readiness does not equal publication approval.

WF-0001 does not define final export or migration rules.

Export and migration concerns belong to future workflow standards, storage specifications, validation specifications, implementation profiles, and operational guides.

WF-0001 may identify when ingestion output appears export-ready or migration-ready, but ingestion completion does not equal export approval or migration approval.

WF-0001 does not define exact agent roles.

Agent roles, responsibility profiles, permission profiles, prompt profiles, tool-access profiles, and agent logging profiles belong to future agent specifications or implementation profiles.

WF-0001 may define what an ingestion workflow requires from agents, but it must not redefine agent authority.

WF-0001 does not define exact templates or schemas.

Templates, metadata field specifications, source-reference formats, provenance fields, relationship formats, lifecycle values, authority values, privacy values, validation rules, workflow-state vocabularies, and workflow-log schemas belong to future specifications.

WF-0001 may define the workflow behavior those future specifications must support.

WF-0001 is bounded by the following closing rule:

- Workflows coordinate governed action.
- Workflows do not silently create authority.
- Workflows do not silently approve knowledge.
- Workflows do not silently override privacy.
- Workflows do not silently replace validation.
- Workflows do not silently redefine storage meaning.
- Workflows do not silently expand agent authority.
- Workflows do not silently become implementation requirements.

## 4. Intake and Registration

Intake is the first governed stage of the Knowledge Ingestion workflow.

Intake exists to make incoming material visible, traceable, classifiable, and reviewable before it becomes a Knowledge Record, Source Reference, workflow output, archived item, rejected item, quarantined item, or downstream-use candidate.

An ingestion workflow SHALL provide or support an intake stage when incoming material is intended for possible governed knowledge use.

Intake MAY apply to:

- newly captured Source Material;
- imported material;
- migrated material;
- exported material from another system;
- human-created notes;
- agent-generated drafts;
- workflow-generated drafts;
- implementation-generated artifacts;
- extracted content;
- summarized content;
- transformed content;
- previously unclassified files;
- recovered files;
- inbox material;
- review material;
- other material proposed for knowledge use.

An intake stage SHOULD establish enough context for a future human, agent, workflow, validator, storage system, or implementation to determine:

- what material entered the workflow;
- when the material entered the workflow where applicable;
- who or what submitted, captured, imported, migrated, generated, or routed the material where applicable;
- whether the material is Source Material, extracted content, a draft Knowledge Record, a workflow output, an implementation artifact, or another candidate type;
- whether the material appears to contain restricted, sensitive, confidential, private, public, or unknown-privacy information;
- whether the material appears to require preservation as Source Material;
- whether the material appears to require Source References or provenance;
- whether the material appears to relate to existing Knowledge Objects or Knowledge Records;
- whether the material appears to be a duplicate, copy, derivative, update, correction, contradiction, replacement, or new knowledge candidate;
- whether the material requires review, repair, validation, quarantine, archival, rejection, or downstream routing.

Intake MUST preserve Source Material distinction.

Incoming material MUST NOT become a Knowledge Record merely because it has been captured, staged, uploaded, stored, indexed, summarized, parsed, imported, migrated, reviewed by an agent, or placed in an intake area.

Intake MUST preserve Object Identity boundaries.

An intake workflow MAY assign or use a temporary identifier, intake identifier, source identifier, file identifier, workflow identifier, or implementation identifier.

A temporary, intake, source, file, workflow, or implementation identifier MUST NOT be treated as stable Object Identity unless a governed identity process assigns or confirms that role.

Intake SHOULD preserve provenance.

Where intake context affects interpretation, review, privacy, validation, source traceability, authority, compatibility, import behavior, export behavior, migration behavior, or downstream use, the workflow SHOULD preserve enough provenance to identify how the material entered the workflow.

Intake SHOULD preserve privacy boundaries.

Incoming material with unknown privacy status SHOULD be handled conservatively until Privacy Classification is assigned, confirmed, or reviewed.

An ingestion workflow MUST NOT expose, publish, export, synchronize, index, summarize, route to agents, or make downstream use of intake material in a way that violates known or reasonably suspected privacy boundaries.

Intake MAY be manual, agent-assisted, partially automated, or implementation-supported.

Agent assistance during intake MAY include:

- identifying material type;
- identifying likely Source Material;
- identifying possible privacy concerns;
- identifying possible duplicates;
- identifying possible source context;
- identifying possible metadata;
- identifying possible relationships;
- identifying possible review needs;
- identifying possible validation needs;
- identifying possible routing options;
- generating an intake report.

Agent assistance during intake MUST remain reviewable where it affects Object Identity, metadata, Source References, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

An intake workflow MUST NOT silently approve material.

An intake workflow MUST NOT silently reject material unless a future governed workflow specification explicitly permits rejection for a narrow, low-risk, reviewable scope.

An intake workflow MUST NOT silently delete material.

An intake workflow MUST NOT silently overwrite existing Source Material, Knowledge Records, metadata, relationships, Source References, provenance, lifecycle states, authority assignments, privacy classifications, validation results, workflow logs, or governed records.

An intake workflow SHOULD create or support an intake record where the material requires traceability.

An intake record MAY include or support:

- intake identifier;
- intake date;
- submitting human, agent, workflow, implementation, import process, migration process, or other source where applicable;
- original filename, title, label, source identifier, external reference, or temporary identifier where applicable;
- material type;
- initial classification;
- suspected privacy classification;
- source availability context;
- source preservation requirement;
- proposed workflow route;
- review requirement;
- validation requirement;
- quarantine flag;
- repair flag;
- relationship candidates;
- duplicate candidates;
- provenance notes;
- agent involvement;
- workflow log reference;
- storage reference;
- other governed intake context.

Exact intake record fields, formats, values, schemas, storage paths, and validation rules are not defined by WF-0001.

Those concerns belong to future workflow specifications, metadata specifications, source-reference specifications, storage specifications, validation specifications, implementation profiles, templates, and operational guides.

Intake is successful when incoming material is registered or staged in a way that preserves traceability, privacy, source distinction, workflow visibility, reviewability, and downstream decision-making without silently converting raw material into governed knowledge.

## 5. Source Material Handling and Preservation

Source Material handling defines how incoming material is preserved, protected, referenced, routed, transformed, extracted from, or excluded during knowledge ingestion.

Source Material handling exists so that original evidence, context, attribution, and provenance remain available for future review where they affect meaning, authority, privacy, validation, relationships, lifecycle state, compatibility, or downstream use.

An ingestion workflow SHALL preserve Source Material where the material materially supports, explains, contextualizes, contradicts, originates, or otherwise affects a Knowledge Record, relationship, decision, validation result, workflow output, or other governed entity.

Source Material MAY be preserved as:

- an original file;
- an archived file;
- an imported artifact;
- a migrated artifact;
- a captured document;
- a transcript;
- a scan;
- an image;
- an audio file;
- a video file;
- a dataset;
- a message;
- an email;
- a web page capture;
- an external reference;
- a citation-supported source;
- a source record;
- another governed source representation.

An ingestion workflow MUST preserve the distinction between Source Material and Knowledge Records.

Source Material may support knowledge.

Source Material does not become a Knowledge Record merely because it is stored, cited, summarized, extracted, indexed, transformed, routed, processed by an agent, or used by a workflow.

A Knowledge Record may be created from, about, or in response to Source Material.

A Knowledge Record MUST remain distinguishable from the Source Material that supports it.

Source Material handling SHOULD preserve source availability context.

A workflow SHOULD identify or support identification of whether Source Material is:

- available;
- unavailable;
- externally hosted;
- locally preserved;
- partially available;
- restricted;
- redacted;
- archived;
- moved;
- missing;
- corrupted;
- superseded;
- unverifiable;
- deleted;
- duplicated;
- migrated;
- imported;
- exported;
- otherwise limited.

Source Material handling SHOULD preserve source privacy context.

A workflow MUST NOT expose restricted Source Material merely because source access improves extraction, summarization, metadata creation, relationship discovery, validation, indexing, publication, export, synchronization, backup, or implementation convenience.

Where Source Material is restricted, sensitive, confidential, private, or otherwise controlled, the workflow SHOULD preserve enough traceability for authorized review without exposing restricted content unnecessarily.

Source Material handling SHOULD preserve source provenance.

Where Source Material affects governed meaning or downstream use, a workflow SHOULD preserve enough provenance to identify:

- where the Source Material came from;
- who or what captured, submitted, imported, migrated, generated, or routed it where applicable;
- whether an agent processed the material;
- whether a workflow transformed the material;
- whether extraction occurred;
- whether summarization occurred;
- whether translation occurred;
- whether redaction occurred;
- whether migration occurred;
- whether import occurred;
- whether export occurred;
- whether validation occurred;
- whether human review occurred;
- whether the source was accepted, rejected, archived, quarantined, repaired, or deferred.

Source Material handling MAY include extraction.

Extraction MUST preserve enough context to avoid confusing extracted content with the full original source.

Extracted content SHOULD remain traceable to the Source Material from which it was extracted.

Extraction MAY be manual, agent-assisted, workflow-generated, implementation-supported, or performed by another governed mechanism.

Agent-generated extraction MUST remain reviewable where extraction affects meaning, source support, provenance, metadata, relationships, lifecycle state, authority, privacy, validation, publication, export, migration, or downstream use.

Source Material handling MAY include transformation.

Transformation MUST preserve provenance where transformation affects interpretation, meaning, evidence, authority, privacy, validation, compatibility, import behavior, export behavior, migration behavior, or downstream use.

A transformation MAY include:

- summarization;
- translation;
- transcription;
- redaction;
- conversion;
- normalization;
- classification;
- segmentation;
- structuring;
- reformatting;
- migration;
- extraction into a draft Knowledge Record;
- other governed transformation.

A transformed representation MUST NOT replace Source Material unless a governed preservation, migration, archival, or deletion rule explicitly permits that behavior.

A transformed representation SHOULD remain linked to or traceable from the original Source Material where source preservation is required.

Source Material handling SHOULD support storage routing.

Storage routing may place Source Material in an intake area, source area, review area, archive area, quarantine area, import area, migration area, export area, backup area, or another governed storage area.

Storage routing MUST NOT define knowledge meaning by itself.

Storage routing MUST NOT replace Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, review, approval, rejection, quarantine, or archival rules.

Source Material handling SHOULD support quarantine.

Source Material SHOULD be quarantined or withheld from normal ingestion use when it has unresolved issues involving:

- privacy risk;
- source authenticity;
- source corruption;
- malware or safety concern;
- legal or policy restriction;
- provenance uncertainty;
- identity conflict;
- source conflict;
- validation failure;
- compatibility risk;
- unauthorized access;
- unsafe publication risk;
- unsafe export risk;
- unsafe synchronization risk;
- unsafe agent access risk;
- other unresolved governed risk.

Quarantine MUST remain distinguishable from rejection, deletion, approval, archival, validation failure, privacy classification, and authority assignment.

Source Material handling MUST preserve auditability where source handling affects governed meaning, privacy, authority, validation, publication, export, migration, or downstream use.

A workflow SHOULD record material source-handling actions in a workflow log where those actions materially affect interpretation, review, validation, privacy, provenance, storage routing, publication, export, migration, or downstream use.

Source Material handling is successful when Source Material remains distinguishable, preserved where required, traceable, privacy-respecting, reviewable, compatible with validation, compatible with storage, compatible with workflow routing, and available for future review without allowing source files, storage placement, extraction, transformation, indexing, or agent output to silently become governed knowledge.

## 6. Ingestion Candidate Classification

Ingestion Candidate Classification defines how incoming material is initially classified for workflow handling.

Classification exists so that an ingestion workflow can determine how material should be reviewed, preserved, routed, validated, transformed, rejected, repaired, quarantined, archived, or used downstream.

An ingestion workflow SHOULD classify ingestion candidates before creating or modifying governed Knowledge Records where classification affects meaning, privacy, authority, validation, provenance, relationships, storage routing, review, or downstream use.

Classification MAY apply to:

- Source Material;
- extracted content;
- transformed content;
- draft Knowledge Records;
- imported records;
- migrated records;
- agent-generated drafts;
- workflow-generated outputs;
- implementation artifacts;
- duplicate candidates;
- derivative candidates;
- update candidates;
- correction candidates;
- contradiction candidates;
- rejected candidates;
- quarantined candidates;
- archived candidates;
- deferred candidates;
- other material under ingestion review.

Ingestion Candidate Classification MAY identify whether material is:

- Source Material only;
- candidate Knowledge Record material;
- supporting evidence;
- extracted content;
- transformed content;
- summary material;
- reference material;
- project material;
- decision material;
- procedure material;
- research material;
- operational material;
- implementation material;
- agent-support material;
- workflow-support material;
- governed-document material;
- duplicate material;
- derivative material;
- update material;
- correction material;
- contradiction material;
- supersession material;
- archive material;
- rejected material;
- quarantine material;
- unknown material;
- other governed candidate type.

Classification MUST remain distinguishable from Object Identity.

A candidate classification does not assign stable Object Identity by itself.

A candidate classification MAY support Object Identity review, duplicate detection, derivative detection, merge review, split review, or identity assignment.

Classification MUST remain distinguishable from Lifecycle State.

A candidate classification may indicate that material appears draft-like, review-ready, archival, rejected, or quarantine-relevant.

Such classification MUST NOT become Lifecycle State unless the lifecycle state is explicitly assigned or confirmed through a governed lifecycle process.

Classification MUST remain distinguishable from Authority Level.

A candidate classification may indicate that material appears official, high-value, unreliable, speculative, source-supported, source-poor, reviewed, or unreviewed.

Such classification MUST NOT create Authority Level unless authority is explicitly assigned or confirmed through a governed authority process.

Classification MUST remain distinguishable from Privacy Classification.

A candidate classification may identify suspected privacy risk, unknown privacy status, or possible sensitivity.

Such classification SHOULD trigger privacy review where needed.

A suspected privacy classification SHOULD be handled conservatively until confirmed or revised.

A classification workflow MUST NOT downgrade privacy handling merely because a candidate appears useful, low-risk, public, source-supported, highly connected, or important.

Classification MUST remain distinguishable from Validation.

A candidate classification may identify likely validity, incompleteness, missing metadata, source gaps, relationship uncertainty, or structural concerns.

Such classification does not equal Validation State unless validation is explicitly performed and recorded within a defined validation scope.

Classification MUST remain distinguishable from approval.

A candidate classification may recommend approval, rejection, repair, quarantine, archival, or downstream routing.

Such recommendation MUST NOT become approval, rejection, repair completion, quarantine, archival, publication permission, export permission, migration permission, or downstream-use permission unless a governed workflow or review process explicitly creates that effect.

Classification MAY be manual, agent-assisted, workflow-generated, implementation-supported, or partially automated.

Agent-assisted classification MAY include:

- material type identification;
- source type identification;
- topic identification;
- Knowledge Record candidate detection;
- Source Material preservation recommendation;
- duplicate detection;
- derivative detection;
- update detection;
- contradiction detection;
- metadata suggestion;
- relationship suggestion;
- privacy risk flagging;
- authority risk flagging;
- lifecycle recommendation;
- validation concern detection;
- routing recommendation.

Agent-assisted classification MUST remain reviewable where classification affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

Classification SHOULD preserve uncertainty.

Where the classification is uncertain, incomplete, inferred, agent-generated, source-poor, privacy-sensitive, or otherwise risky, the workflow SHOULD preserve that uncertainty through review notes, validation warnings, workflow logs, candidate status, or another governed mechanism.

Classification SHOULD support routing.

A classified ingestion candidate MAY be routed to:

- source preservation;
- Knowledge Record drafting;
- metadata review;
- relationship review;
- duplicate review;
- identity review;
- provenance review;
- privacy review;
- authority review;
- lifecycle review;
- validation review;
- human review;
- repair;
- quarantine;
- archival;
- rejection;
- import review;
- export review;
- migration review;
- implementation review;
- downstream-use review;
- another governed workflow route.

Classification routing MUST NOT silently override privacy, authority, lifecycle, validation, source-reference, provenance, relationship, storage, agent, or implementation boundaries.

Ingestion Candidate Classification is successful when incoming material is classified clearly enough to support review, preservation, validation, privacy handling, authority handling, routing, repair, quarantine, archival, rejection, Knowledge Record drafting, and downstream decision-making without silently converting classification into identity, lifecycle state, authority, privacy clearance, validation, approval, publication permission, export permission, migration permission, or governed knowledge.

## 7. Extraction and Transformation

Extraction and Transformation define how information may be selected, copied, transcribed, parsed, summarized, translated, normalized, structured, converted, or otherwise changed during the Knowledge Ingestion workflow.

Extraction exists to identify information from Source Material or ingestion candidates that may support a Knowledge Record, metadata, Source Reference, provenance record, relationship, validation result, workflow output, review note, or downstream decision.

Transformation exists to convert Source Material, extracted content, captured information, imported material, migrated material, or prior knowledge into a more usable representation without silently changing governed meaning.

An ingestion workflow MAY perform extraction or transformation when doing so supports review, preservation, classification, Knowledge Record drafting, metadata creation, Source Reference creation, provenance creation, relationship suggestion, validation, repair, quarantine, archival, import, export, migration, or downstream-use evaluation.

Extraction MAY include:

- copying selected text;
- transcribing audio or video;
- parsing structured data;
- identifying claims;
- identifying entities;
- identifying dates;
- identifying decisions;
- identifying tasks;
- identifying definitions;
- identifying procedures;
- identifying evidence;
- identifying contradictions;
- identifying relationships;
- identifying source details;
- identifying metadata candidates;
- identifying privacy concerns;
- identifying validation concerns;
- extracting sections from a document;
- extracting records from a dataset;
- extracting references from a source;
- other governed extraction activity.

Transformation MAY include:

- summarization;
- translation;
- transcription;
- normalization;
- reformatting;
- segmentation;
- classification;
- redaction;
- conversion;
- enrichment;
- structuring;
- deduplication support;
- migration support;
- draft Knowledge Record preparation;
- source-reference preparation;
- provenance preparation;
- relationship preparation;
- validation preparation;
- other governed transformation activity.

Extraction MUST preserve enough context to avoid confusing extracted content with the full Source Material.

Extracted content MUST NOT be treated as the complete source unless it is explicitly governed as a complete source representation.

Extracted content SHOULD remain traceable to the Source Material, ingestion candidate, workflow output, import record, migration record, or other governed origin from which it was extracted.

Transformation MUST preserve provenance where transformation affects meaning, interpretation, evidence, source support, authority, privacy, validation, compatibility, import behavior, export behavior, migration behavior, publication behavior, or downstream use.

A transformed representation MUST remain distinguishable from the original Source Material.

A transformed representation MUST NOT replace original Source Material unless a governed preservation, migration, archival, redaction, or deletion process explicitly permits that behavior.

Extraction and transformation MUST preserve Object Identity boundaries.

An extracted passage, generated summary, translated representation, normalized record, converted file, or structured draft MUST NOT become a new Knowledge Object merely because it was extracted or transformed.

A new Knowledge Object MAY be created from extracted or transformed material only when a governed identity process determines that the material represents a distinct unit of structured knowledge.

Extraction and transformation MUST preserve metadata boundaries.

Metadata may be extracted, proposed, enriched, normalized, or transformed.

Extracted or transformed metadata MUST NOT become approved standard metadata unless the applicable metadata process permits that result.

Agent-generated metadata MUST remain distinguishable from human-approved metadata where that distinction affects meaning, review, validation, privacy, authority, publication, export, migration, or downstream use.

Extraction and transformation MUST preserve relationship boundaries.

A workflow may identify possible relationships during extraction or transformation.

A possible relationship MUST remain distinguishable from an approved relationship unless a governed relationship process permits approval.

Relationship suggestions created through extraction or transformation SHOULD preserve enough context to explain why the relationship was proposed.

Extraction and transformation MUST preserve Source Reference and provenance boundaries.

A workflow may create or propose Source References and provenance during extraction or transformation.

A Source Reference or provenance record created through extraction or transformation SHOULD identify or support identification of:

- the Source Material or ingestion candidate used;
- the extracted or transformed content;
- the workflow action performed;
- whether a human, agent, implementation, validator, import process, export process, migration process, or other mechanism performed or supported the action;
- whether review is required;
- whether validation is required;
- whether privacy review is required;
- whether the output is complete, partial, inferred, summarized, translated, redacted, converted, or otherwise transformed.

Extraction and transformation MUST preserve Lifecycle State boundaries.

An extraction or transformation output may be draft, proposed, pending review, pending validation, needs repair, quarantined, archived, rejected, or governed by another lifecycle state where applicable.

Extraction or transformation by itself MUST NOT make an output approved.

Extraction and transformation MUST preserve Authority Level boundaries.

A summary, translation, transcription, normalized record, extracted claim, or structured draft MUST NOT inherit full authority merely because it was derived from authoritative Source Material.

Authority MAY be proposed, limited, reviewed, inherited, or assigned only through a governed authority process.

Extraction and transformation MUST preserve Privacy Classification boundaries.

A workflow MUST NOT weaken privacy handling because extraction or transformation makes material easier to search, summarize, classify, route, validate, publish, export, synchronize, index, or use downstream.

A transformed representation of restricted material may remain restricted even if it is shorter, summarized, redacted, translated, normalized, or partially extracted.

Privacy review SHOULD occur when extraction or transformation changes visibility, exposure, routing, indexing, publication risk, export risk, synchronization risk, agent access, implementation access, or downstream-use risk.

Extraction and transformation MUST preserve Validation boundaries.

A transformation may make validation easier.

A transformation may produce validation warnings or validation errors.

A validation-supporting transformation MUST NOT be treated as validation unless validation is explicitly performed and recorded within a defined validation scope.

Extraction and transformation MAY be manual, agent-assisted, workflow-generated, implementation-supported, validator-supported, import-supported, export-supported, migration-supported, or partially automated.

Agent-assisted extraction or transformation MAY include:

- extracting candidate facts;
- extracting candidate definitions;
- extracting candidate decisions;
- extracting candidate tasks;
- extracting candidate procedures;
- extracting source details;
- extracting metadata candidates;
- extracting relationship candidates;
- summarizing Source Material;
- translating Source Material;
- transcribing Source Material;
- redacting Source Material;
- normalizing Source Material;
- preparing draft Knowledge Records;
- identifying source-reference gaps;
- identifying provenance gaps;
- identifying validation concerns;
- identifying privacy concerns;
- identifying authority concerns;
- identifying repair needs.

Agent-assisted extraction or transformation MUST remain reviewable where it affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

Extraction and transformation SHOULD preserve uncertainty.

Where extracted or transformed content is partial, inferred, low-confidence, ambiguous, source-poor, agent-generated, translated, summarized, redacted, or otherwise uncertain, the workflow SHOULD preserve that uncertainty through review notes, validation warnings, provenance, workflow logs, candidate status, or another governed mechanism.

Extraction and transformation SHOULD support repair.

A workflow SHOULD route extraction or transformation outputs for repair when they contain:

- missing source context;
- unclear provenance;
- broken Source References;
- unclear Object Identity;
- missing metadata;
- unclear relationships;
- privacy uncertainty;
- authority uncertainty;
- validation errors;
- conflicting extracted claims;
- incomplete transformation;
- unsupported interpretation;
- source corruption;
- transformation loss;
- implementation-specific dependency;
- other governed defects.

Extraction and Transformation are successful when information can be extracted or transformed for useful ingestion work while preserving Source Material distinction, Object Identity, metadata boundaries, relationship boundaries, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, reviewability, auditability, compatibility, and implementation independence.

## 8. Draft Knowledge Record Creation

Draft Knowledge Record Creation defines how an ingestion workflow may create a proposed Knowledge Record from Source Material, extracted content, transformed content, human reasoning, agent output, workflow output, imported material, migrated material, or other ingestion candidates.

A Draft Knowledge Record exists to represent proposed structured knowledge before it has completed required review, validation, approval, rejection, repair, quarantine, archival, or downstream-use routing.

An ingestion workflow MAY create a Draft Knowledge Record when incoming material appears to contain knowledge that should be structured, preserved, reviewed, connected, validated, or used under The Brain Standard.

A Draft Knowledge Record MUST remain distinguishable from:

- Source Material;
- extracted content;
- transformed content;
- workflow notes;
- agent output;
- validation output;
- implementation artifacts;
- review comments;
- approved Knowledge Records;
- rejected candidates;
- quarantined material;
- archived material;
- export artifacts;
- migration artifacts.

Draft Knowledge Record creation MUST preserve Source Material distinction.

A draft may be created from Source Material.

A draft MUST NOT replace the Source Material that supports it unless a governed preservation, archival, migration, redaction, or deletion rule explicitly permits that behavior.

A draft SHOULD preserve or support Source References where Source Material materially supports, explains, contextualizes, contradicts, originates, or otherwise affects the draft.

Draft Knowledge Record creation MUST preserve Object Identity boundaries.

A Draft Knowledge Record MAY use a temporary identifier, draft identifier, workflow identifier, source identifier, import identifier, migration identifier, implementation identifier, or other non-stable identifier during drafting.

A temporary, draft, workflow, source, import, migration, or implementation identifier MUST NOT be treated as stable Object Identity unless a governed identity process assigns or confirms that role.

A Draft Knowledge Record MAY become associated with a new or existing Knowledge Object only through a governed identity determination.

A Draft Knowledge Record SHOULD be routed for identity review where the workflow detects:

- possible duplicate knowledge;
- possible derivative knowledge;
- possible update to an existing Knowledge Object;
- possible correction to an existing Knowledge Object;
- possible contradiction of an existing Knowledge Object;
- possible split candidate;
- possible merge candidate;
- possible supersession candidate;
- possible identity conflict;
- unclear source identity;
- unclear object boundary.

Draft Knowledge Record creation MUST preserve metadata boundaries.

A draft SHOULD include or support enough metadata for review, validation, routing, privacy handling, authority handling, relationship review, source-reference review, provenance review, compatibility review, and downstream decision-making.

Draft metadata MAY be incomplete where the draft is clearly identified as incomplete, pending review, pending validation, needs repair, or otherwise not ready for approval.

Draft metadata MUST NOT be treated as approved, complete, authoritative, privacy-cleared, validation-passing, publication-ready, export-ready, migration-ready, or downstream-ready unless the applicable governed process explicitly creates that effect.

Draft Knowledge Record creation MUST preserve relationship boundaries.

A draft MAY contain proposed relationships.

Proposed relationships MUST remain distinguishable from approved relationships unless a governed relationship process permits approval.

A draft SHOULD identify or support identification of relationship uncertainty where relationships are inferred, agent-generated, source-poor, unreviewed, conflicting, partial, or implementation-derived.

Draft Knowledge Record creation MUST preserve Source Reference and provenance boundaries.

A draft SHOULD include or support enough Source Reference and provenance context for future review where the draft depends on Source Material, extracted content, transformation, human reasoning, agent output, workflow output, import, export, migration, validation, or prior governed knowledge.

Draft provenance SHOULD identify or support identification of:

- the Source Material used;
- the extraction or transformation performed;
- the human, agent, workflow, implementation, validator, import process, migration process, or other mechanism involved where applicable;
- whether the draft was created manually;
- whether the draft was agent-assisted;
- whether the draft was workflow-generated;
- whether the draft was imported;
- whether the draft was migrated;
- whether validation has occurred;
- whether review is required;
- whether approval is required;
- whether repair is required;
- whether quarantine is required;
- whether privacy review is required.

Draft Knowledge Record creation MUST preserve Lifecycle State boundaries.

A Draft Knowledge Record is not approved by default.

A Draft Knowledge Record SHOULD carry or support a lifecycle state that makes its draft, pending-review, pending-validation, needs-repair, quarantined, rejected, archived, or other governed status clear where that status affects interpretation or use.

Draft creation by itself MUST NOT create approval.

Draft creation by itself MUST NOT create publication permission.

Draft creation by itself MUST NOT create export permission.

Draft creation by itself MUST NOT create migration permission.

Draft creation by itself MUST NOT create downstream-use permission.

Draft Knowledge Record creation MUST preserve Authority Level boundaries.

A Draft Knowledge Record MUST NOT become authoritative merely because it was created from authoritative Source Material, approved source material, high-quality evidence, agent confidence, validation output, storage placement, workflow completion, or implementation visibility.

A Draft Knowledge Record MAY carry proposed, limited, scoped, unknown, pending-review, or other governed authority context where applicable.

Authority assignment MUST follow the applicable authority process.

Draft Knowledge Record creation MUST preserve Privacy Classification boundaries.

A Draft Knowledge Record SHOULD inherit or conservatively preserve privacy restrictions from the Source Material, extracted content, transformed content, prior record, relationship, or provenance on which it depends until privacy review determines otherwise.

A draft MUST NOT weaken privacy handling merely because the draft is summarized, structured, redacted, partial, agent-generated, easier to search, easier to route, easier to validate, or intended for downstream use.

Draft Knowledge Record creation MUST preserve Validation boundaries.

A Draft Knowledge Record MAY be validated for structure, metadata, identity, relationships, Source References, provenance, lifecycle state, authority, privacy, compatibility, workflow handling, agent handling, storage handling, import behavior, export behavior, migration behavior, or downstream-use readiness.

Validation MAY support review.

Validation MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that effect.

Draft Knowledge Record creation MAY be manual, agent-assisted, workflow-generated, implementation-supported, import-supported, migration-supported, or partially automated.

Agent-assisted Draft Knowledge Record creation MAY include:

- drafting content;
- structuring extracted information;
- proposing a title;
- proposing metadata;
- proposing Source References;
- proposing provenance;
- proposing relationships;
- proposing lifecycle state;
- proposing authority context;
- proposing privacy classification;
- identifying validation concerns;
- identifying repair needs;
- identifying review needs;
- identifying duplicate candidates;
- identifying update candidates;
- identifying contradiction candidates;
- preparing a review summary.

Agent-created or agent-assisted drafts MUST remain reviewable where they affect meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

A Draft Knowledge Record SHOULD be routed to review, validation, repair, quarantine, archival, rejection, approval consideration, or another governed workflow route according to its content, risk, completeness, source support, privacy, authority, validation state, and compatibility.

Draft Knowledge Record Creation is successful when proposed knowledge can be represented in structured form without confusing drafts with approved records, Source Material, agent output, validation results, storage placement, lifecycle state, authority assignment, privacy clearance, publication permission, export permission, migration permission, or downstream-use permission.

## 9. Metadata, Source Reference, and Provenance Capture

Metadata, Source Reference, and Provenance Capture defines how an ingestion workflow records the context needed to interpret, review, validate, preserve, route, approve, reject, repair, quarantine, archive, export, migrate, or use ingestion outputs.

This section coordinates metadata, source-reference, and provenance capture during ingestion.

This section does not redefine metadata, Source Reference, or provenance standards.

An ingestion workflow SHOULD capture or support capture of metadata, Source References, and provenance where they affect meaning, Object Identity, source distinction, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, review, storage routing, import behavior, export behavior, migration behavior, publication behavior, compatibility, or downstream use.

Metadata capture MAY include:

- identity metadata;
- descriptive metadata;
- structural metadata;
- source-reference metadata;
- provenance metadata;
- relationship metadata;
- lifecycle metadata;
- authority metadata;
- privacy metadata;
- validation metadata;
- compatibility metadata;
- workflow metadata;
- agent metadata;
- import metadata;
- export metadata;
- migration metadata;
- implementation metadata where distinguishable from standard metadata;
- other governed metadata.

Source Reference capture MAY include:

- Source Material reference;
- source identifier;
- source title or label;
- source type;
- source location where permissible;
- source availability;
- source access limitation;
- source privacy context;
- source reliability note;
- source authority context;
- citation support where useful;
- external reference where applicable;
- archival reference where applicable;
- extracted passage reference where applicable;
- transformed representation reference where applicable;
- source relationship to a draft or Knowledge Record;
- other governed source-reference context.

Provenance capture MAY include:

- origin of material;
- creator where applicable;
- submitter where applicable;
- capturing human, agent, workflow, implementation, import process, migration process, or other mechanism where applicable;
- extraction history;
- transformation history;
- summarization history;
- transcription history;
- translation history;
- redaction history;
- classification history;
- metadata-generation history;
- relationship-suggestion history;
- validation history;
- review history;
- repair history;
- quarantine history;
- rejection history;
- approval history where applicable;
- archival history;
- import history;
- export history;
- migration history;
- agent involvement;
- workflow involvement;
- implementation involvement;
- other governed provenance context.

Metadata, Source Reference, and Provenance Capture MUST preserve Object Identity boundaries.

Captured metadata may include identifiers.

Only identifiers governed as stable Object Identity SHALL define Knowledge Object identity.

A source identifier, workflow identifier, draft identifier, intake identifier, import identifier, migration identifier, filename, folder path, title, tag, external reference, or implementation identifier MUST NOT be treated as stable Object Identity unless a governed identity process assigns or confirms that role.

Metadata, Source Reference, and Provenance Capture MUST preserve metadata boundaries.

Captured metadata MUST remain distinguishable from content, Source Material, Source References, provenance, relationships, lifecycle state, authority, privacy classification, validation results, workflow state, agent state, storage state, and implementation state where those distinctions affect meaning or use.

Workflow-generated metadata SHOULD remain distinguishable from agent-generated metadata, human-entered metadata, imported metadata, migrated metadata, implementation metadata, validation metadata, and approved standard metadata where that distinction affects review, authority, privacy, validation, publication, export, migration, or downstream use.

Metadata, Source Reference, and Provenance Capture MUST preserve Source Material distinction.

A Source Reference links or relates a governed entity to Source Material.

A Source Reference does not make the Source Material a Knowledge Record.

A Source Reference does not make the governed entity approved.

A Source Reference does not make the source authoritative by itself.

A Source Reference does not remove privacy obligations.

A Source Reference does not complete validation by itself.

Metadata, Source Reference, and Provenance Capture MUST preserve provenance boundaries.

Provenance explains origin, change history, transformation context, actor involvement, workflow activity, agent activity, validation activity, review activity, import activity, export activity, migration activity, or other history.

Provenance does not replace approval.

Provenance does not replace authority.

Provenance does not replace validation.

Provenance does not replace privacy classification.

Provenance does not replace lifecycle state.

Metadata, Source Reference, and Provenance Capture MUST preserve relationship boundaries.

A captured Source Reference, provenance entry, or metadata element MAY support a relationship suggestion.

A relationship suggestion MUST remain distinguishable from an approved relationship unless a governed relationship process permits approval.

Metadata, Source Reference, and Provenance Capture MUST preserve Lifecycle State boundaries.

Capturing metadata, Source References, or provenance does not make an entity approved.

Capturing metadata, Source References, or provenance does not make an entity ready for publication, export, migration, or downstream use by itself.

A workflow SHOULD identify whether captured metadata, Source References, or provenance are draft, proposed, pending review, pending validation, needs repair, approved within scope, rejected, archived, quarantined, imported, migrated, or otherwise governed where that status affects interpretation or use.

Metadata, Source Reference, and Provenance Capture MUST preserve Authority Level boundaries.

A well-sourced record may still require authority review.

A provenance-rich record may still be low-authority.

An agent-generated source summary may still be unreviewed.

An imported source reference may still be unvalidated.

A workflow MUST NOT assign Authority Level merely because metadata, Source References, or provenance are present.

Metadata, Source Reference, and Provenance Capture MUST preserve Privacy Classification boundaries.

Metadata, Source References, and provenance may expose restricted information even when the main content appears safe.

A workflow MUST handle metadata, Source References, and provenance according to applicable privacy boundaries.

A workflow MUST NOT expose restricted source details, provenance details, relationship details, identity details, review details, agent details, implementation details, import details, export details, migration details, or workflow details merely because they improve traceability, search, validation, publication, export, migration, automation, or downstream use.

Metadata, Source Reference, and Provenance Capture MUST preserve Validation boundaries.

Captured metadata, Source References, and provenance MAY support validation.

Captured metadata, Source References, and provenance MUST NOT be treated as validation results unless validation is explicitly performed and recorded within a defined validation scope.

Validation results concerning metadata, Source References, or provenance SHOULD remain traceable to the validation scope, validator, rule, finding, warning, error, review status, and remediation status where applicable.

Metadata, Source Reference, and Provenance Capture MAY be manual, agent-assisted, workflow-generated, implementation-supported, validator-supported, import-supported, export-supported, migration-supported, or partially automated.

Agent-assisted capture MAY include:

- proposing metadata;
- extracting source details;
- creating Source Reference candidates;
- identifying provenance gaps;
- reconstructing provenance from available evidence;
- identifying source availability;
- identifying source reliability concerns;
- identifying source privacy concerns;
- identifying source authority concerns;
- identifying missing attribution;
- identifying missing extraction history;
- identifying missing transformation history;
- identifying validation concerns;
- identifying repair needs;
- preparing a provenance report.

Agent-assisted metadata, Source Reference, and provenance capture MUST remain reviewable where it affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

A workflow SHOULD route captured metadata, Source References, or provenance for repair when they are missing, incomplete, inconsistent, conflicting, unclear, source-poor, privacy-risky, authority-risky, validation-failing, implementation-dependent, migration-risky, export-risky, or otherwise defective.

Metadata, Source Reference, and Provenance Capture is successful when ingestion outputs remain identifiable, traceable, reviewable, privacy-respecting, validatable, portable, compatible, and interpretable without relying on hidden application state, folder placement, filename convention, workflow memory, agent memory, implementation behavior, or undocumented practice.

## 10. Relationship Suggestion and Review

Relationship Suggestion and Review defines how an ingestion workflow may identify, propose, review, validate, approve, reject, repair, or preserve relationships during knowledge ingestion.

Relationship handling exists so that Knowledge Objects, Knowledge Records, Source Material, Source References, provenance records, decisions, standards, workflows, implementations, agents, validation results, import records, export records, migration records, and other governed entities can be connected without allowing inferred, temporary, implementation-specific, or agent-generated links to become approved relationships by accident.

An ingestion workflow MAY suggest relationships when incoming material, Source Material, extracted content, transformed content, Draft Knowledge Records, metadata, Source References, provenance, validation results, agent outputs, workflow outputs, import records, migration records, or existing governed knowledge indicate a possible connection.

Relationship suggestions MAY include:

- source-support relationships;
- evidence relationships;
- provenance relationships;
- duplicate-candidate relationships;
- derivative-candidate relationships;
- update-candidate relationships;
- correction-candidate relationships;
- contradiction relationships;
- supersession-candidate relationships;
- dependency relationships;
- containment relationships;
- sequence relationships;
- related-concept relationships;
- project relationships;
- decision relationships;
- procedure relationships;
- implementation relationships;
- workflow relationships;
- agent-support relationships;
- validation-support relationships;
- import relationships;
- export relationships;
- migration relationships;
- other governed relationship candidates.

A relationship suggestion MUST remain distinguishable from an approved relationship.

A relationship suggestion MUST NOT become approved merely because it was inferred by an agent, discovered by search, generated by a workflow, implied by folder placement, created by a backlink, detected by vector similarity, found through metadata similarity, created by an implementation, or repeated across multiple records.

Relationship suggestions SHOULD preserve enough context for future review.

A relationship suggestion SHOULD identify or support identification of:

- the proposed relationship participants;
- the proposed relationship type where known;
- whether direction affects meaning;
- the Source Material, metadata, provenance, workflow output, agent output, validation result, import record, migration record, or other evidence supporting the suggestion;
- whether the relationship was human-created, agent-generated, workflow-generated, implementation-generated, imported, migrated, inferred, validated, reviewed, or unreviewed;
- whether relationship confidence, uncertainty, source support, lifecycle state, authority, privacy, validation, compatibility, or downstream use is affected;
- whether human review is required;
- whether validation is required;
- whether repair is required;
- whether privacy review is required;
- whether authority review is required.

Relationship suggestions MUST preserve Object Identity boundaries.

A relationship suggestion SHOULD use stable Object Identity where stable Object Identity is known and applicable.

A relationship suggestion MUST NOT create, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Where relationship review reveals possible duplicate identity, derivative identity, update identity, split identity, merge identity, supersession identity, or identity conflict, the workflow SHOULD route the issue to identity review.

Relationship suggestions MUST preserve metadata boundaries.

A relationship suggestion MAY be supported by metadata.

Metadata similarity, shared tags, shared categories, shared titles, shared filenames, shared folders, shared source identifiers, shared implementation identifiers, shared workflow identifiers, or shared agent classifications MUST NOT become approved relationship meaning unless a governed relationship process permits that interpretation.

Relationship suggestions MUST preserve Source Reference and provenance boundaries.

A relationship suggestion SHOULD preserve Source References or provenance where the relationship affects meaning, authority, privacy, validation, lifecycle state, compatibility, import behavior, export behavior, migration behavior, publication behavior, or downstream use.

A relationship suggestion based on weak, missing, restricted, conflicting, inferred, agent-generated, imported, migrated, or implementation-specific source support SHOULD preserve that limitation.

Relationship suggestions MUST preserve Lifecycle State boundaries.

A proposed relationship is not an approved relationship by default.

A relationship MAY have its own lifecycle state or review state where that distinction affects interpretation, routing, validation, authority, privacy, compatibility, or downstream use.

The lifecycle state of a Knowledge Object, Knowledge Record, Source Material item, Source Reference, provenance record, validation result, workflow output, or agent output MUST NOT automatically determine the lifecycle state of a relationship unless a governed process explicitly defines that effect.

Relationship suggestions MUST preserve Authority Level boundaries.

A relationship suggestion MUST NOT become authoritative merely because it connects authoritative records, approved records, highly cited records, high-confidence agent output, validation-passing entities, frequently linked entities, or implementation-visible entities.

Relationship authority MAY be proposed, reviewed, limited, assigned, rejected, deprecated, superseded, archived, or repaired only through a governed authority or relationship process.

Relationship suggestions MUST preserve Privacy Classification boundaries.

Relationships can expose restricted knowledge even when the connected entities appear safe individually.

A workflow MUST treat relationship suggestions according to applicable privacy boundaries.

A workflow MUST NOT expose restricted relationships, restricted relationship participants, restricted source support, restricted provenance, restricted metadata, restricted review notes, or restricted relationship context merely because the relationship improves navigation, search, validation, automation, publication, export, migration, graph display, or downstream use.

Relationship suggestions MUST preserve Validation boundaries.

A relationship suggestion MAY be validated for participant identity, relationship type, direction, source support, provenance, lifecycle state, authority, privacy, compatibility, implementation independence, import behavior, export behavior, migration behavior, or downstream-use readiness.

Validation MAY support relationship review.

Validation MUST NOT be treated as relationship approval unless a governed workflow or specification explicitly defines that effect.

Relationship review MAY result in:

- approval within a defined scope;
- rejection;
- repair request;
- quarantine;
- archival;
- deferral;
- validation request;
- privacy review;
- authority review;
- identity review;
- source-reference review;
- provenance review;
- relationship-type review;
- relationship-direction review;
- relationship-confidence review;
- relationship-lifecycle review;
- import review;
- export review;
- migration review;
- downstream-use review;
- another governed outcome.

Relationship review SHOULD preserve review decisions and review rationale where the relationship affects meaning, authority, privacy, validation, source support, lifecycle state, compatibility, publication, export, migration, or downstream use.

Relationship review MAY be manual, agent-assisted, workflow-generated, validator-supported, implementation-supported, import-supported, export-supported, migration-supported, or partially automated.

Agent-assisted relationship work MAY include:

- identifying relationship candidates;
- identifying possible relationship participants;
- proposing relationship types;
- proposing relationship direction;
- identifying duplicate candidates;
- identifying derivative candidates;
- identifying update candidates;
- identifying contradiction candidates;
- identifying supersession candidates;
- identifying source support;
- identifying provenance gaps;
- identifying privacy risks;
- identifying authority concerns;
- identifying validation concerns;
- identifying relationship conflicts;
- preparing relationship review summaries.

Agent-assisted relationship work MUST remain reviewable where the relationship affects meaning, Object Identity, metadata, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

Relationship Suggestion and Review is successful when relationship candidates can be proposed, reviewed, validated, approved, rejected, repaired, quarantined, archived, or routed without confusing suggestions with approved relationships, inferred links with governed meaning, implementation links with standard relationships, storage proximity with relationship meaning, agent output with approval, validation with approval, or relationship usefulness with authority.

## 11. Lifecycle, Authority, Privacy, and Validation Handling

Lifecycle, Authority, Privacy, and Validation Handling defines how an ingestion workflow coordinates governed status, authority context, privacy boundaries, and validation expectations during ingestion.

This section coordinates Lifecycle State, Authority Level, Privacy Classification, and Validation during ingestion.

This section does not redefine Lifecycle State, Authority Level, Privacy Classification, or Validation standards.

An ingestion workflow SHOULD identify or support identification of Lifecycle State, Authority Level, Privacy Classification, and Validation needs where they affect meaning, review, routing, repair, quarantine, archival, rejection, approval consideration, publication readiness, export readiness, migration readiness, storage routing, agent access, implementation behavior, or downstream use.

Lifecycle handling MAY include:

- identifying draft status;
- identifying pending-review status;
- identifying pending-validation status;
- identifying needs-repair status;
- identifying quarantine needs;
- identifying rejection candidates;
- identifying archival candidates;
- identifying supersession candidates;
- identifying deprecation candidates;
- identifying approval candidates;
- identifying lifecycle transition needs;
- preserving lifecycle transition provenance;
- routing lifecycle issues for review;
- other governed lifecycle handling.

Authority handling MAY include:

- identifying proposed authority context;
- identifying authority scope;
- identifying source authority concerns;
- identifying relationship authority concerns;
- identifying agent-confidence limitations;
- identifying workflow-completion limitations;
- identifying validation limitations;
- identifying publication authority concerns;
- identifying export authority concerns;
- identifying migration authority concerns;
- routing authority issues for review;
- other governed authority handling.

Privacy handling MAY include:

- identifying suspected Privacy Classification;
- identifying unknown privacy status;
- identifying restricted material;
- identifying sensitive metadata;
- identifying restricted Source Material;
- identifying restricted relationships;
- identifying restricted provenance;
- identifying exposure risk;
- identifying indexing risk;
- identifying synchronization risk;
- identifying backup risk;
- identifying publication risk;
- identifying export risk;
- identifying migration risk;
- identifying agent-access risk;
- identifying implementation-access risk;
- routing privacy issues for review;
- other governed privacy handling.

Validation handling MAY include:

- identifying validation scope;
- identifying required validation;
- identifying structural validation needs;
- identifying identity validation needs;
- identifying metadata validation needs;
- identifying relationship validation needs;
- identifying Source Reference validation needs;
- identifying provenance validation needs;
- identifying lifecycle validation needs;
- identifying authority validation needs;
- identifying privacy validation needs;
- identifying compatibility validation needs;
- identifying workflow validation needs;
- identifying agent-output validation needs;
- identifying storage-routing validation needs;
- identifying import validation needs;
- identifying export validation needs;
- identifying migration validation needs;
- recording validation warnings;
- recording validation errors;
- routing validation issues for repair or review;
- other governed validation handling.

Lifecycle handling MUST preserve Workflow State boundaries.

Workflow State describes where an entity is inside the ingestion workflow.

Lifecycle State describes the governed status of the entity.

A workflow step, workflow queue, workflow route, workflow log, workflow completion, implementation status, storage location, or agent task state MUST NOT become Lifecycle State unless a governed lifecycle process explicitly creates that effect.

Lifecycle handling MUST NOT silently approve material.

A workflow MAY route material toward approval consideration.

A workflow MAY identify that material appears ready for review.

A workflow MAY record that review has occurred.

A workflow MUST NOT treat workflow completion, validation passing, agent confidence, storage placement, source existence, metadata completeness, relationship richness, or implementation visibility as approval unless a governed workflow or specification explicitly defines that effect.

Authority handling MUST preserve Lifecycle State boundaries.

Lifecycle State and Authority Level are distinct.

A draft may contain high-authority source material.

An approved record may still have limited authority.

A rejected item may remain historically useful.

A superseded item may remain authoritative for historical interpretation.

A workflow MUST NOT assign Authority Level merely because lifecycle status, workflow status, source existence, storage placement, validation result, agent confidence, or implementation visibility suggests usefulness.

Authority handling MUST preserve Validation boundaries.

A validation-passing entity is not automatically authoritative.

A validation-failing entity may still be useful for repair, review, historical preservation, conflict detection, or source analysis.

Validation MAY support authority review.

Validation MUST NOT create final authority unless a governed authority process explicitly defines that effect.

Privacy handling MUST take precedence over workflow convenience.

An ingestion workflow MUST NOT weaken Privacy Classification for convenience, automation, search, linking, summarization, validation, routing, publication, synchronization, backup, export, migration, agent use, implementation use, or downstream use.

Unknown or uncertain privacy status SHOULD be handled conservatively until reviewed.

A workflow SHOULD route privacy-sensitive or privacy-uncertain material for privacy review before exposure, indexing, summarization, publication, export, synchronization, migration, agent access, implementation access, or downstream use where those actions create privacy risk.

Privacy handling MUST preserve Authority Level boundaries.

Authority does not override privacy by itself.

A high-authority record may still be restricted.

An approved record may still be confidential.

A public source may still produce restricted notes, relationships, metadata, or provenance.

A workflow MUST NOT expose restricted material merely because the material is authoritative, useful, source-supported, validation-passing, or needed for automation.

Validation handling MUST preserve approval boundaries.

Validation checks conformance within a defined validation scope.

Validation may support review, repair, routing, approval consideration, rejection consideration, quarantine, archival, publication review, export review, migration review, or downstream-use review.

Validation MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that effect.

Validation handling MUST preserve Privacy Classification boundaries.

A validation process MUST NOT expose restricted content, restricted metadata, restricted Source References, restricted provenance, restricted relationships, restricted review notes, restricted workflow logs, restricted agent outputs, restricted implementation details, or restricted migration details merely because validation is easier with broad access.

Validation results involving restricted material SHOULD preserve enough detail for authorized review without unnecessarily exposing restricted information.

Validation handling MUST preserve Authority Level boundaries.

A validator may report that an entity satisfies a standard or specification.

A validator MUST NOT assign final authority unless authority assignment is explicitly within the validator’s governed scope.

A validation result SHOULD identify or support identification of validation scope, validation actor, validation method, validation result, validation evidence, validation warnings, validation errors, and remediation status where applicable.

Lifecycle, Authority, Privacy, and Validation handling MAY be manual, agent-assisted, workflow-generated, validator-supported, implementation-supported, import-supported, export-supported, migration-supported, or partially automated.

Agent assistance MAY include:

- proposing lifecycle status;
- identifying lifecycle transition needs;
- identifying authority concerns;
- proposing authority scope;
- identifying privacy risks;
- proposing privacy review routing;
- identifying validation scope;
- identifying validation warnings;
- identifying validation errors;
- identifying repair needs;
- preparing review summaries;
- preparing routing recommendations.

Agent assistance MUST remain reviewable where it affects Lifecycle State, Authority Level, Privacy Classification, Validation, Object Identity, metadata, relationships, Source References, provenance, publication, export, migration, deletion, or downstream use.

Lifecycle, Authority, Privacy, and Validation handling SHOULD support routing.

A workflow MAY route ingestion outputs to:

- lifecycle review;
- authority review;
- privacy review;
- validation review;
- repair;
- quarantine;
- archival;
- rejection;
- approval consideration;
- publication review;
- export review;
- migration review;
- downstream-use review;
- another governed workflow route.

Lifecycle, Authority, Privacy, and Validation Handling is successful when ingestion outputs carry enough governed status, authority context, privacy context, and validation context to support review, routing, repair, quarantine, rejection, approval consideration, archival, publication review, export review, migration review, and downstream decision-making without confusing workflow state with Lifecycle State, lifecycle status with authority, authority with privacy clearance, privacy with validation, validation with approval, or agent recommendation with human/governed decision.

## 12. Human Review and Agent Participation

Human Review and Agent Participation defines how humans and agents may participate in the Knowledge Ingestion workflow while preserving reviewability, traceability, privacy, authority boundaries, validation boundaries, and governance.

Human Review exists to ensure that ingestion outputs affecting governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, rejection, repair, quarantine, publication, export, migration, deletion, or downstream use can be inspected, corrected, limited, escalated, approved, rejected, or routed by an authorized human where review is required.

Agent Participation exists to support ingestion work without allowing agents to become silent authorities over knowledge, privacy, authority, validation, approval, deletion, publication, export, migration, governance, or implementation behavior.

An ingestion workflow SHOULD identify where Human Review is required.

Human Review SHOULD be required or strongly preferred where ingestion activity affects:

- creation of a new Knowledge Object;
- assignment or confirmation of stable Object Identity;
- merge decisions;
- split decisions;
- supersession decisions;
- duplicate resolution;
- approval of a Knowledge Record;
- rejection of a Knowledge Record;
- authority assignment;
- privacy classification reduction;
- publication readiness;
- export readiness;
- migration readiness;
- deletion;
- overwrite;
- relationship approval where meaning is affected;
- lifecycle transition where downstream use is affected;
- validation interpretation where approval or authority may be affected;
- source-reference or provenance repair where trust is affected;
- restricted material exposure;
- governance interpretation;
- other high-impact governed decisions.

Human Review MAY include:

- confirming extracted content;
- correcting transformed content;
- approving or rejecting Draft Knowledge Records;
- confirming Object Identity;
- resolving duplicates;
- resolving contradictions;
- reviewing metadata;
- reviewing relationships;
- reviewing Source References;
- reviewing provenance;
- reviewing lifecycle state;
- reviewing authority level;
- reviewing privacy classification;
- reviewing validation results;
- reviewing repair recommendations;
- reviewing quarantine recommendations;
- reviewing archival recommendations;
- reviewing publication readiness;
- reviewing export readiness;
- reviewing migration readiness;
- reviewing agent outputs;
- reviewing workflow logs;
- reviewing exceptions;
- reviewing downstream-use readiness.

Human Review SHOULD be traceable where the decision affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, rejection, repair, quarantine, archival, publication, export, migration, deletion, or downstream use.

A Human Review record MAY include or support:

- reviewer identity or role where applicable;
- review date where applicable;
- reviewed entity;
- reviewed workflow output;
- review scope;
- decision made;
- rationale where needed;
- source support reviewed;
- validation results reviewed;
- privacy considerations reviewed;
- authority considerations reviewed;
- repair actions requested;
- approval or rejection outcome where applicable;
- escalation outcome where applicable;
- downstream-use limitations where applicable;
- workflow log reference;
- other governed review context.

Exact Human Review record fields, formats, values, schemas, storage locations, and validation rules are not defined by WF-0001.

Those concerns belong to future workflow specifications, review specifications, metadata specifications, validation specifications, implementation profiles, templates, and operational guides.

Agent Participation MAY include:

- intake assistance;
- Source Material classification;
- extraction;
- transformation;
- summarization;
- transcription;
- translation;
- redaction support;
- metadata suggestion;
- Source Reference suggestion;
- provenance suggestion;
- relationship suggestion;
- duplicate detection;
- contradiction detection;
- identity-conflict detection;
- lifecycle recommendation;
- authority recommendation;
- privacy-risk flagging;
- validation support;
- repair recommendation;
- quarantine recommendation;
- archival recommendation;
- review-summary preparation;
- routing recommendation;
- workflow-log support;
- report generation;
- other governed assistance.

Agent Participation MUST remain within authorized scope.

An agent MUST NOT access, process, summarize, index, expose, export, publish, migrate, modify, delete, overwrite, or route material outside its authorized access, privacy, workflow, storage, source, validation, implementation, or task scope.

Agent Participation MUST remain distinguishable from Human Review.

An agent may recommend.

An agent may summarize.

An agent may classify.

An agent may extract.

An agent may validate within a governed validation scope where permitted.

An agent may prepare drafts.

An agent may identify risks.

An agent may route recommendations.

An agent MUST NOT silently replace Human Review where Human Review is required.

Agent Participation MUST preserve approval boundaries.

An agent MUST NOT silently approve, reject, declassify, publish, export, migrate, delete, overwrite, supersede, validate as authoritative, assign final authority, govern privacy, redefine Object Identity, or transform Source Material into approved Knowledge Records without governed review where review is required.

Agent Participation MUST preserve Object Identity boundaries.

An agent MAY identify identity candidates, duplicate candidates, derivative candidates, merge candidates, split candidates, supersession candidates, update candidates, or identity conflicts.

An agent MUST NOT silently assign, merge, split, replace, redirect, supersede, or reinterpret stable Object Identity unless a future governed specification explicitly permits that behavior for a limited, reviewable, low-risk scope.

Agent Participation MUST preserve metadata, relationship, Source Reference, and provenance boundaries.

Agent-generated metadata, relationships, Source References, and provenance MUST remain distinguishable from human-created, human-reviewed, approved, imported, migrated, validation-generated, workflow-generated, implementation-generated, and standard-governed material where those distinctions affect meaning, authority, privacy, validation, publication, export, migration, or downstream use.

Agent Participation MUST preserve Lifecycle State, Authority Level, Privacy Classification, and Validation boundaries.

An agent MAY propose lifecycle state, authority context, privacy risk, or validation findings.

An agent MUST NOT silently create final Lifecycle State, final Authority Level, final Privacy Classification, or final Validation State where human review, governance, privacy, authority, validation scope, publication, export, migration, or downstream use requires review.

Agent Participation MUST preserve privacy boundaries.

An agent MUST NOT process restricted material unless permitted by the applicable privacy classification, workflow authorization, implementation access rules, and governed task scope.

An agent-generated summary of restricted material may remain restricted.

An agent-generated metadata proposal, relationship proposal, Source Reference, provenance note, validation result, review summary, or workflow log may expose restricted information and SHOULD be handled according to applicable privacy boundaries.

Agent Participation MUST preserve auditability.

Where agent activity affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, rejection, repair, quarantine, archival, publication, export, migration, deletion, or downstream use, the workflow SHOULD preserve enough information to identify:

- what agent participated;
- what task was performed;
- what material was accessed;
- what output was created;
- what confidence, uncertainty, warning, or limitation was provided where applicable;
- whether human review occurred;
- whether validation occurred;
- whether repair was required;
- whether privacy review was required;
- whether the output was accepted, rejected, revised, quarantined, archived, or routed.

Agent Participation MAY be rejected, corrected, limited, escalated, or disabled where the agent output is inaccurate, incomplete, unsupported, privacy-risky, authority-risky, validation-failing, implementation-dependent, source-poor, ambiguous, unsafe, or outside scope.

Human Review and Agent Participation SHOULD support escalation.

Escalation SHOULD occur when an ingestion workflow detects:

- unresolved identity conflict;
- unresolved source conflict;
- unresolved privacy risk;
- unresolved authority concern;
- unresolved validation error;
- unresolved relationship conflict;
- missing provenance;
- missing Source References;
- unsafe agent access;
- unsafe publication risk;
- unsafe export risk;
- unsafe migration risk;
- deletion or overwrite risk;
- governance ambiguity;
- implementation dependency;
- other high-impact uncertainty.

Human Review and Agent Participation are successful when humans can review and govern high-impact ingestion decisions, agents can assist efficiently within defined boundaries, and ingestion outputs remain traceable, reviewable, privacy-respecting, validation-aware, authority-aware, implementation-independent, and protected from silent agent governance.

## 13. Approval, Rejection, Repair, and Quarantine

Approval, Rejection, Repair, and Quarantine define the major governed outcomes that may occur during or after knowledge ingestion.

These outcomes exist so that ingestion candidates, Source Material, Draft Knowledge Records, metadata, Source References, provenance records, relationship suggestions, validation results, workflow outputs, agent outputs, import records, migration records, and other governed entities can be accepted, rejected, corrected, isolated, archived, or routed without confusion.

An ingestion workflow MAY produce or route toward one or more of the following outcomes:

- approval;
- rejection;
- repair;
- quarantine;
- archival;
- deferral;
- escalation;
- continued review;
- validation review;
- privacy review;
- authority review;
- source-reference review;
- provenance review;
- relationship review;
- identity review;
- storage routing;
- publication review;
- export review;
- migration review;
- downstream-use review;
- another governed outcome.

Approval is the formal acceptance of a governed entity for use within a defined scope.

Approval MAY apply to:

- a Knowledge Record;
- a Source Reference;
- a provenance record;
- a relationship;
- metadata;
- a lifecycle transition;
- an authority assignment;
- a privacy classification;
- a validation interpretation;
- a repair result;
- a workflow output;
- an import result;
- a migration result;
- another governed entity or decision.

Approval MUST be scoped where scope affects interpretation or downstream use.

Approval of one entity, field, record, relationship, source reference, provenance entry, validation result, workflow output, or review decision MUST NOT imply approval of all related entities unless a governed process explicitly defines that effect.

Approval MUST preserve Object Identity boundaries.

Approval of a Draft Knowledge Record MUST NOT create, merge, split, replace, redirect, supersede, or reinterpret stable Object Identity unless a governed identity decision explicitly creates that effect.

Approval MUST preserve Lifecycle State boundaries.

Approval MAY support a Lifecycle State transition where a governed lifecycle process permits that transition.

Approval MUST NOT be inferred from workflow completion, validation passing, source existence, metadata completeness, relationship richness, storage placement, implementation visibility, or agent confidence unless a governed workflow or specification explicitly defines that effect.

Approval MUST preserve Authority Level boundaries.

Approval and Authority Level are related but distinct.

A governed entity may be approved for limited use without becoming broadly authoritative.

Authority assignment MUST follow the applicable authority process.

Approval MUST preserve Privacy Classification boundaries.

Approval MUST NOT weaken privacy obligations by itself.

An approved entity may still be private, confidential, restricted, non-exportable, non-publishable, non-indexable, non-synchronizable, or unavailable to agents where privacy classification requires that handling.

Approval MUST preserve Validation boundaries.

Approval MAY depend on validation.

Approval MAY occur after validation.

Approval MAY require validation.

Validation MUST NOT become approval unless a governed workflow or specification explicitly defines that effect.

Rejection is a governed decision that an ingestion candidate, draft, relationship suggestion, metadata proposal, Source Reference, provenance entry, validation interpretation, workflow output, agent output, import result, migration result, or proposed change is not accepted for the intended use.

Rejection MUST preserve traceability where the rejected material affects future review, auditability, provenance, source interpretation, duplicate detection, contradiction handling, privacy, authority, validation, compatibility, import, export, migration, or downstream use.

Rejection MUST NOT be treated as deletion by default.

A rejected entity MAY remain historically preserved, archived, restricted, quarantined, or available for future review according to applicable lifecycle, privacy, storage, governance, and retention expectations.

Rejection MUST preserve privacy boundaries.

Rejected material may still contain restricted information.

A workflow MUST NOT expose rejected material merely because it is not approved.

Repair is the correction of known or suspected issues identified during ingestion.

Repair MAY apply to:

- structure;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- lifecycle state;
- authority level;
- privacy classification;
- validation;
- source handling;
- extraction;
- transformation;
- draft content;
- agent output;
- workflow output;
- storage routing;
- import records;
- export records;
- migration records;
- implementation dependencies;
- other governed defects.

Repair SHOULD preserve the defect, repair action, repair actor, review state, validation state, and outcome where those details affect meaning, authority, privacy, validation, compatibility, auditability, or downstream use.

Repair MUST NOT silently overwrite governed material where the overwrite would remove traceability, provenance, review history, validation history, source context, relationship context, lifecycle history, authority context, privacy context, or compatibility context.

Repair MAY result in:

- corrected material;
- revised metadata;
- revised Source References;
- revised provenance;
- revised relationships;
- revised lifecycle state;
- revised authority context;
- revised privacy handling;
- revised validation result;
- revised storage routing;
- renewed review;
- renewed validation;
- quarantine;
- rejection;
- archival;
- approval consideration;
- another governed outcome.

Quarantine is the isolation or withholding of material from normal use because of unresolved validity, safety, privacy, compatibility, source, provenance, authority, validation, implementation, import, export, migration, or integrity concerns.

Quarantine MAY apply to:

- Source Material;
- ingestion candidates;
- Draft Knowledge Records;
- extracted content;
- transformed content;
- metadata;
- Source References;
- provenance records;
- relationship suggestions;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- implementation artifacts;
- other governed entities.

Quarantine SHOULD occur or be strongly considered where ingestion reveals:

- unresolved privacy risk;
- unsafe agent access;
- unsafe publication risk;
- unsafe export risk;
- unsafe migration risk;
- unsafe synchronization risk;
- source corruption;
- source authenticity concern;
- missing provenance;
- broken Source References;
- unresolved identity conflict;
- unresolved relationship conflict;
- validation failure;
- malware or safety concern;
- legal or policy restriction;
- implementation-specific dependency;
- unsupported transformation;
- unauthorized modification;
- deletion or overwrite risk;
- other high-impact uncertainty.

Quarantine MUST remain distinguishable from rejection.

Quarantine MUST remain distinguishable from approval.

Quarantine MUST remain distinguishable from deletion.

Quarantine MUST remain distinguishable from archival.

Quarantine MUST remain distinguishable from Privacy Classification, although privacy concerns may trigger quarantine.

Quarantine MUST remain distinguishable from Validation State, although validation concerns may trigger quarantine.

A quarantined entity SHOULD remain traceable where traceability can be preserved without violating privacy, safety, legal, security, or governance requirements.

Approval, Rejection, Repair, and Quarantine MAY be manual, agent-assisted, workflow-generated, validator-supported, implementation-supported, import-supported, export-supported, migration-supported, or partially automated.

Agent assistance MAY include:

- recommending approval consideration;
- recommending rejection;
- identifying repair needs;
- preparing repair suggestions;
- identifying quarantine risks;
- preparing quarantine summaries;
- identifying validation blockers;
- identifying privacy blockers;
- identifying authority blockers;
- identifying source-reference blockers;
- identifying provenance blockers;
- identifying relationship blockers;
- preparing review summaries;
- preparing routing recommendations.

Agent assistance MUST remain reviewable where approval, rejection, repair, quarantine, archival, publication, export, migration, deletion, overwrite, authority, privacy, validation, Object Identity, metadata, relationships, Source References, provenance, or downstream use is affected.

Approval, Rejection, Repair, and Quarantine are successful when ingestion outcomes are explicit, scoped, traceable, reviewable, privacy-respecting, validation-aware, authority-aware, source-aware, storage-compatible, agent-bounded, implementation-independent, and distinguishable from workflow completion, agent recommendation, storage placement, implementation visibility, validation passing, or informal practice.

## 14. Storage Routing and Preservation

Storage Routing and Preservation define how ingestion workflows may stage, route, preserve, archive, quarantine, review, export, migrate, or otherwise place material in storage without allowing storage placement to define governed meaning.

Storage routing exists to support practical organization, review, preservation, retrieval, validation, migration, backup, synchronization, indexing, and implementation use.

Storage routing does not define knowledge meaning.

Knowledge meaning remains defined by Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, governed structure, and applicable standards.

An ingestion workflow MAY route material to storage areas for:

- intake;
- staging;
- source preservation;
- draft creation;
- review;
- validation;
- repair;
- quarantine;
- rejection;
- archival;
- approved use;
- governed-document preservation;
- workflow support;
- agent support;
- implementation support;
- import;
- export;
- migration;
- backup;
- synchronization;
- indexing;
- downstream-use preparation;
- another governed storage purpose.

Storage routing MAY apply to:

- Source Material;
- Knowledge Records;
- Draft Knowledge Records;
- approved Knowledge Records;
- rejected candidates;
- quarantined material;
- archived material;
- metadata records;
- Source References;
- provenance records;
- relationship records;
- validation results;
- workflow logs;
- agent outputs;
- review records;
- repair records;
- import records;
- export records;
- migration records;
- supporting assets;
- implementation artifacts;
- other governed or supporting material.

Storage routing MUST preserve Source Material distinction.

Source Material SHOULD remain distinguishable from Knowledge Records where source distinction affects interpretation, review, validation, provenance, authority, privacy, compatibility, import, export, migration, publication, or downstream use.

Storage routing MUST preserve Draft Knowledge Record distinction.

A Draft Knowledge Record MUST NOT become approved merely because it is moved, copied, indexed, linked, backed up, synchronized, exported, migrated, or placed in a more permanent storage area.

Storage routing MUST preserve approved-record distinction.

A record placed in an approved area, approval queue, implementation view, index, or published-like location MUST NOT be treated as approved unless approval is explicitly represented through a governed process.

Storage routing MUST preserve Object Identity boundaries.

Folder placement, filename, vault path, repository path, archive location, import location, export location, migration location, backup location, synchronization location, index location, cache location, implementation path, or generated path MUST NOT create, replace, merge, split, redirect, supersede, or reinterpret stable Object Identity by itself.

Storage routing MUST preserve metadata boundaries.

Storage placement MAY support metadata.

Storage placement MUST NOT replace explicit metadata where metadata affects meaning, identity, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, import, export, migration, publication, or downstream use.

Storage routing MUST preserve relationship boundaries.

Folder proximity, path similarity, file naming similarity, shared archive location, shared import package, shared export package, shared migration package, shared implementation workspace, backlinks, indexes, caches, graph position, or storage grouping MUST NOT become approved relationship meaning unless a governed relationship process explicitly permits that interpretation.

Storage routing MUST preserve Source Reference and provenance boundaries.

A stored file may serve as Source Material.

A storage location may help locate Source Material.

A storage location does not replace Source References or provenance where source traceability affects governed meaning.

A workflow SHOULD preserve enough source and storage context to identify where Source Material, extracted content, transformed content, Draft Knowledge Records, approved records, workflow outputs, validation results, review records, and supporting artifacts were placed where that placement affects review, auditability, privacy, validation, import, export, migration, or downstream use.

Storage routing MUST preserve Lifecycle State boundaries.

Moving material into an intake area, draft area, review area, approved area, rejection area, repair area, quarantine area, archive area, import area, export area, migration area, backup area, or implementation area MUST NOT create Lifecycle State by itself unless a governed lifecycle process explicitly defines that effect.

Storage routing MUST preserve Authority Level boundaries.

Storage placement MUST NOT assign Authority Level by itself.

A record is not authoritative merely because it is easy to find, centrally stored, frequently linked, indexed, exposed in an implementation, stored with approved records, included in an export, or preserved in an archive.

Storage routing MUST preserve Privacy Classification boundaries.

Storage routing MUST NOT weaken privacy handling for convenience, search, indexing, synchronization, backup, publication, export, migration, agent access, implementation access, or downstream use.

A workflow SHOULD route privacy-sensitive material only to storage areas, systems, indexes, backups, synchronization targets, agents, implementations, and export or migration packages permitted by the applicable privacy classification and access expectations.

Unknown or uncertain privacy status SHOULD be handled conservatively until reviewed.

Storage routing MUST preserve Validation boundaries.

A file that is stored, moved, copied, archived, indexed, backed up, synchronized, imported, exported, migrated, or made visible to an implementation MUST NOT be treated as validation-passing unless validation is explicitly performed and recorded within a defined validation scope.

Storage routing MAY support validation by making material inspectable, locatable, stable, distinguishable, and reviewable.

Storage routing MUST preserve agent boundaries.

An ingestion workflow MUST NOT route material into an agent-accessible area merely because the material is useful for automation.

Agent access must remain governed by privacy classification, workflow authorization, implementation access rules, and task scope.

Storage routing MUST preserve implementation boundaries.

A storage layout MAY support Obsidian, Codex, local tools, databases, search systems, indexes, graph tools, validators, scripts, or future implementations.

Implementation-support storage MUST NOT become a requirement of WF-0001 unless a future governed implementation profile explicitly defines that requirement within its proper scope.

Storage routing SHOULD support preservation.

A workflow SHOULD preserve material where preservation is required for source traceability, review, validation, auditability, historical interpretation, authority review, privacy review, repair, import, export, migration, compatibility, backup, restoration, or downstream use.

Preservation MAY include:

- retaining Source Material;
- retaining extracted content;
- retaining transformed content;
- retaining Draft Knowledge Records;
- retaining approved records;
- retaining rejected records where historically useful;
- retaining quarantined material where safe and permitted;
- retaining archived material;
- retaining workflow logs;
- retaining validation results;
- retaining review records;
- retaining repair records;
- retaining import records;
- retaining export records;
- retaining migration records;
- retaining supporting assets;
- retaining compatibility context.

Storage routing SHOULD support repair and recovery.

Where storage routing creates confusion, breaks traceability, exposes restricted material, loses provenance, causes identity ambiguity, weakens validation, hides lifecycle state, weakens authority boundaries, breaks relationships, loses Source References, or creates implementation lock-in, the issue SHOULD be routed for repair or recovery.

Storage Routing and Preservation MAY be manual, agent-assisted, workflow-generated, validator-supported, implementation-supported, import-supported, export-supported, migration-supported, backup-supported, synchronization-supported, or partially automated.

Agent assistance MAY include:

- recommending storage routing;
- identifying misplaced material;
- identifying source-preservation needs;
- identifying draft/approved/rejected/quarantined/archive distinctions;
- identifying privacy routing concerns;
- identifying validation routing concerns;
- identifying missing storage references;
- identifying broken Source Material links;
- identifying import, export, or migration risks;
- preparing storage-routing reports;
- preparing repair recommendations.

Agent-assisted storage routing MUST remain reviewable where it affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, overwrite, or downstream use.

Storage Routing and Preservation are successful when ingestion material is placed, preserved, routed, archived, quarantined, backed up, synchronized, imported, exported, migrated, or made implementation-accessible in a way that supports practical use without allowing storage placement, filenames, folder paths, indexes, caches, exports, migrations, backups, synchronization targets, implementation files, or agent workspaces to define governed meaning.

## 15. Workflow Logging, Auditability, and Traceability

Workflow Logging, Auditability, and Traceability define how ingestion workflows preserve enough process history for future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, backup processes, synchronization processes, publication processes, and implementations to understand what happened during ingestion.

Workflow logging exists to make material workflow actions, decisions, outputs, reviews, validations, repairs, quarantines, approvals, rejections, storage routing, agent participation, and exceptions visible enough for review and maintenance.

Auditability exists so that governed ingestion activity can be inspected where it affects meaning, privacy, authority, validation, publication, export, migration, deletion, overwrite, governance, or downstream use.

Traceability exists so that ingestion outputs remain connected to their Source Material, intake context, extraction history, transformation history, metadata history, Source References, provenance, relationships, validation results, review decisions, agent outputs, storage routing, import history, export history, migration history, and downstream-use decisions where those connections affect interpretation or use.

An ingestion workflow SHOULD create or support workflow logging where ingestion activity affects:

- Source Material preservation;
- Object Identity;
- Knowledge Record creation;
- Draft Knowledge Record creation;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- Human Review;
- agent participation;
- approval;
- rejection;
- repair;
- quarantine;
- archival;
- storage routing;
- publication review;
- export review;
- migration review;
- deletion;
- overwrite;
- downstream use;
- governance interpretation;
- other high-impact governed activity.

A workflow log MAY include or support:

- workflow identifier;
- workflow name or type;
- workflow scope;
- ingestion candidate reference;
- Source Material reference;
- Knowledge Record reference;
- draft reference;
- actor or role where applicable;
- agent identifier where applicable;
- tool or implementation identifier where applicable;
- action performed;
- time or sequence where applicable;
- input material;
- output material;
- extraction activity;
- transformation activity;
- metadata activity;
- Source Reference activity;
- provenance activity;
- relationship activity;
- lifecycle activity;
- authority activity;
- privacy activity;
- validation activity;
- review activity;
- approval activity;
- rejection activity;
- repair activity;
- quarantine activity;
- archival activity;
- storage-routing activity;
- import activity;
- export activity;
- migration activity;
- warning;
- error;
- exception;
- escalation;
- outcome;
- downstream-use limitation;
- other governed workflow context.

Exact workflow log fields, formats, identifiers, schemas, storage paths, retention rules, validation rules, access-control rules, or implementation behavior are not defined by WF-0001.

Those concerns belong to future workflow specifications, logging specifications, metadata specifications, validation specifications, privacy specifications, storage specifications, implementation profiles, templates, and operational guides.

Workflow logging MUST preserve privacy boundaries.

A workflow log may expose restricted content, restricted metadata, restricted Source References, restricted provenance, restricted relationships, restricted review notes, restricted agent outputs, restricted validation results, restricted implementation details, restricted import details, restricted export details, restricted migration details, or restricted storage details.

A workflow MUST NOT expose restricted workflow logs merely because logs improve auditability, search, validation, automation, debugging, publication, export, migration, synchronization, indexing, backup, or downstream use.

Workflow logging SHOULD preserve enough detail for authorized review without unnecessarily exposing restricted information.

Workflow logging MUST preserve Object Identity boundaries.

A workflow log may reference Object Identity.

A workflow log MUST NOT create, replace, merge, split, redirect, supersede, or reinterpret stable Object Identity by itself.

Workflow logging MUST preserve metadata boundaries.

Workflow logs may contain metadata.

Workflow logs MUST NOT replace standard metadata where metadata affects meaning, identity, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, import, export, migration, publication, or downstream use.

Workflow logging MUST preserve Source Reference and provenance boundaries.

Workflow logs may support provenance.

Workflow logs may document Source Reference activity.

Workflow logs do not replace Source References or provenance where explicit Source References or provenance are required by the applicable standard, specification, workflow, review, validation, or downstream-use context.

Workflow logging MUST preserve relationship boundaries.

Workflow logs may record relationship suggestions, relationship review, relationship validation, relationship repair, relationship approval, or relationship rejection.

Workflow logs MUST NOT make a relationship approved unless a governed relationship process explicitly creates that effect.

Workflow logging MUST preserve Lifecycle State boundaries.

A workflow log may record lifecycle-related activity.

A workflow log entry MUST NOT become Lifecycle State unless a governed lifecycle process explicitly creates that effect.

Workflow logging MUST preserve Authority Level boundaries.

A workflow log may record authority-related activity.

A workflow log entry MUST NOT assign final Authority Level unless a governed authority process explicitly creates that effect.

Workflow logging MUST preserve Validation boundaries.

A workflow log may record validation activity.

A workflow log entry MUST NOT become a validation result unless validation is explicitly performed and recorded within a defined validation scope.

A validation log SHOULD identify or support identification of validation scope, validation actor, validation method, validation result, validation evidence, warnings, errors, remediation status, and review state where applicable.

Workflow logging MUST preserve Human Review boundaries.

A workflow log may document Human Review.

A workflow log MUST NOT imply Human Review occurred unless review actually occurred or the log clearly identifies the review status as proposed, pending, simulated, agent-generated, workflow-generated, incomplete, or unreviewed.

Workflow logging MUST preserve agent boundaries.

A workflow log may document agent activity.

A workflow log MUST NOT treat agent participation as Human Review, approval, authority assignment, privacy clearance, validation success, publication permission, export permission, migration permission, deletion permission, overwrite permission, or downstream-use permission by itself.

Workflow logging SHOULD preserve uncertainty.

Where workflow activity is incomplete, inferred, agent-generated, source-poor, privacy-sensitive, validation-failing, authority-risky, implementation-dependent, ambiguous, or disputed, the workflow SHOULD preserve that uncertainty through workflow logs, review notes, validation warnings, provenance, repair records, quarantine records, or another governed mechanism.

Workflow logging SHOULD support auditability.

A future authorized reviewer SHOULD be able to determine:

- what material entered ingestion;
- what source material was used;
- what extraction occurred;
- what transformation occurred;
- what draft was created;
- what metadata was proposed or changed;
- what Source References were created or changed;
- what provenance was created or changed;
- what relationships were proposed or changed;
- what lifecycle handling occurred;
- what authority handling occurred;
- what privacy handling occurred;
- what validation occurred;
- what Human Review occurred where applicable;
- what agent participation occurred where applicable;
- what was approved;
- what was rejected;
- what was repaired;
- what was quarantined;
- what was archived;
- what was routed;
- what storage routing occurred;
- what import, export, or migration activity occurred;
- what exceptions occurred;
- what downstream-use limits apply.

Workflow logging SHOULD support repair and recovery.

Where a workflow log reveals missing provenance, broken Source References, unclear identity, missing metadata, relationship ambiguity, lifecycle ambiguity, authority ambiguity, privacy risk, validation failure, storage confusion, agent overreach, implementation dependency, import ambiguity, export ambiguity, migration loss, publication risk, deletion risk, overwrite risk, or governance ambiguity, the issue SHOULD remain visible enough for appropriate repair, recovery, escalation, or review.

Workflow Logging, Auditability, and Traceability MAY be manual, agent-assisted, workflow-generated, validator-supported, implementation-supported, import-supported, export-supported, migration-supported, backup-supported, synchronization-supported, or partially automated.

Agent assistance MAY include:

- generating workflow summaries;
- identifying missing log context;
- identifying traceability gaps;
- identifying provenance gaps;
- identifying source-reference gaps;
- identifying review gaps;
- identifying validation gaps;
- identifying privacy risks in logs;
- identifying authority risks in logs;
- identifying agent-output risks;
- identifying storage-routing issues;
- identifying repair needs;
- preparing audit reports;
- preparing exception reports.

Agent-assisted workflow logging MUST remain reviewable where it affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, rejection, repair, quarantine, archival, publication, export, migration, deletion, overwrite, or downstream use.

Workflow Logging, Auditability, and Traceability are successful when ingestion activity remains visible, inspectable, privacy-respecting, validation-aware, authority-aware, repairable, recoverable, portable, compatible, implementation-independent, and traceable without allowing logs, audit records, agent summaries, implementation histories, storage locations, or workflow memory to become hidden sources of governed meaning.

## 16. Workflow Conformance Requirements

Workflow Conformance Requirements define the minimum behavior required for an ingestion workflow to conform to WF-0001.

A WF-0001-conformant workflow SHALL preserve the purpose, scope, boundaries, reviewability, traceability, privacy expectations, validation expectations, storage expectations, agent boundaries, and implementation independence defined by this standard.

A conformance claim MUST identify or support identification of the scope being claimed.

A conformance claim MAY apply to:

- a manual ingestion workflow;
- an agent-assisted ingestion workflow;
- a partially automated ingestion workflow;
- a workflow template;
- a workflow specification;
- a workflow implementation profile;
- an import workflow;
- a migration workflow;
- a storage-routing workflow;
- a validation-support workflow;
- a review-support workflow;
- another governed ingestion workflow scope.

A narrow conformance claim MUST NOT be treated as full WF-0001 conformance.

A workflow that supports only intake MUST NOT claim full WF-0001 conformance.

A workflow that supports only storage routing MUST NOT claim full WF-0001 conformance.

A workflow that supports only agent-assisted extraction MUST NOT claim full WF-0001 conformance.

A workflow that supports only validation routing MUST NOT claim full WF-0001 conformance.

A workflow that supports only implementation-specific automation MUST NOT claim full WF-0001 conformance.

A WF-0001-conformant workflow SHALL preserve Source Material distinction.

Source Material MUST remain distinguishable from Knowledge Records, Draft Knowledge Records, extracted content, transformed content, workflow outputs, agent outputs, validation outputs, review records, storage artifacts, import artifacts, export artifacts, migration artifacts, and implementation artifacts where that distinction affects meaning or use.

A WF-0001-conformant workflow SHALL preserve Object Identity boundaries.

A workflow MUST NOT silently create, replace, merge, split, redirect, supersede, or reinterpret stable Object Identity.

A WF-0001-conformant workflow SHALL preserve metadata boundaries.

Workflow-generated metadata, agent-generated metadata, imported metadata, migrated metadata, implementation metadata, validation metadata, and human-approved metadata SHOULD remain distinguishable where that distinction affects meaning, review, validation, authority, privacy, publication, export, migration, or downstream use.

A WF-0001-conformant workflow SHALL preserve relationship boundaries.

Relationship suggestions MUST remain distinguishable from approved relationships.

Implementation links, storage proximity, backlinks, graph position, vector similarity, search results, metadata similarity, workflow routing, or agent output MUST NOT become approved relationship meaning unless a governed relationship process explicitly defines that effect.

A WF-0001-conformant workflow SHALL preserve Source Reference and provenance boundaries.

A workflow SHOULD preserve enough Source Reference and provenance context for future review where ingestion activity affects meaning, authority, privacy, validation, lifecycle state, relationships, compatibility, publication, export, migration, or downstream use.

A WF-0001-conformant workflow SHALL preserve Lifecycle State boundaries.

Workflow State MUST remain distinguishable from Lifecycle State.

Workflow completion MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that effect.

A WF-0001-conformant workflow SHALL preserve Authority Level boundaries.

A workflow MUST NOT assign final Authority Level merely because material was captured, stored, sourced, validated, reviewed by an agent, routed, indexed, migrated, exported, imported, or made visible by an implementation.

A WF-0001-conformant workflow SHALL preserve Privacy Classification boundaries.

Privacy Classification SHALL take precedence over workflow convenience where privacy and convenience conflict.

A workflow MUST NOT weaken privacy handling for convenience, automation, search, summarization, validation, routing, publication, synchronization, indexing, backup, export, migration, agent use, implementation use, or downstream use.

A WF-0001-conformant workflow SHALL preserve Validation boundaries.

Validation MUST remain explicit, scoped, traceable, reviewable, privacy-respecting, and distinguishable from workflow completion, approval, authority, privacy clearance, publication readiness, export readiness, migration readiness, implementation permission, agent permission, or downstream-use permission.

A WF-0001-conformant workflow SHALL preserve Human Review boundaries.

Human Review MUST remain distinguishable from agent participation, workflow routing, validation output, implementation visibility, storage placement, and workflow completion.

Where Human Review is required, an agent MUST NOT silently replace it.

A WF-0001-conformant workflow SHALL preserve agent boundaries.

Agents MAY assist ingestion only within authorized access, privacy, workflow, storage, source, validation, implementation, and task scope.

Agents MUST NOT silently approve, reject, declassify, publish, export, migrate, delete, overwrite, supersede, validate as authoritative, assign final authority, govern privacy, redefine Object Identity, or transform Source Material into approved Knowledge Records without governed review where review is required.

A WF-0001-conformant workflow SHALL preserve storage boundaries.

Storage routing, folder placement, filenames, paths, vault areas, archive locations, backup locations, synchronization targets, index locations, cache locations, implementation locations, import locations, export locations, and migration locations MUST NOT become governed meaning by themselves.

A WF-0001-conformant workflow SHALL preserve implementation independence.

A workflow MUST NOT require Obsidian, Codex, a specific model, a specific agent runtime, a specific database, a specific file system, a specific plugin, a specific interface, a specific validation tool, a specific automation tool, or a specific implementation unless a future governed implementation profile explicitly defines that requirement within its proper scope.

A WF-0001-conformant workflow SHOULD support or preserve:

- intake;
- Source Material handling;
- ingestion candidate classification;
- extraction and transformation traceability where extraction or transformation occurs;
- Draft Knowledge Record distinction where drafts are created;
- metadata capture where metadata affects interpretation or use;
- Source Reference capture where source support affects interpretation or use;
- provenance capture where origin, change, review, agent activity, workflow activity, import, export, migration, or transformation affects interpretation or use;
- relationship suggestion and review where relationships affect interpretation or use;
- Lifecycle State handling where lifecycle affects interpretation or use;
- Authority Level handling where authority affects interpretation or use;
- Privacy Classification handling where privacy affects access, exposure, routing, publication, export, migration, agent use, implementation use, or downstream use;
- Validation handling where validation affects interpretation, review, repair, compatibility, publication, export, migration, or downstream use;
- Human Review where review is required;
- agent participation boundaries where agents assist;
- approval, rejection, repair, and quarantine outcomes where applicable;
- storage routing and preservation where material is stored or moved;
- workflow logging, auditability, and traceability where ingestion activity affects governed meaning or downstream use.

A WF-0001-conformant workflow SHOULD support repair and recovery.

Where a workflow detects missing provenance, broken Source References, unclear identity, missing metadata, relationship ambiguity, lifecycle ambiguity, authority ambiguity, privacy risk, validation failure, storage confusion, agent overreach, implementation dependency, import ambiguity, export ambiguity, migration loss, publication risk, deletion risk, overwrite risk, or governance ambiguity, the issue SHOULD remain visible enough for appropriate review, repair, recovery, escalation, quarantine, rejection, archival, or reprocessing.

A WF-0001-conformant workflow SHOULD support auditability.

A future authorized reviewer SHOULD be able to determine what material entered ingestion, what actions occurred, what outputs were created, what review occurred, what validation occurred, what agent participation occurred, what storage routing occurred, what decisions were made, what risks remain, and what downstream-use limits apply where those details affect interpretation or use.

Workflow Conformance Requirements are successful when a workflow can claim conformance only within a clear scope and only when it preserves source distinction, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, Human Review, agent boundaries, storage boundaries, implementation independence, auditability, repairability, recovery, and downstream-use limits.

## 17. Non-Conformance, Exceptions, and Recovery

Non-Conformance, Exceptions, and Recovery define how ingestion workflow failures, deviations, conflicts, risks, and temporary departures from WF-0001 are identified, handled, limited, repaired, or escalated.

Non-conformance occurs when an ingestion workflow fails to satisfy WF-0001 within its claimed scope.

Non-conformance MAY occur through:

- missing intake context;
- loss of Source Material distinction;
- Source Material being converted into a Knowledge Record without governed review where review is required;
- Draft Knowledge Records being treated as approved records;
- workflow completion being treated as approval without governed authorization;
- validation being treated as approval without governed authorization;
- validation being treated as authority without governed authorization;
- agent confidence being treated as validation, authority, approval, privacy clearance, publication readiness, export readiness, migration readiness, or downstream-use permission;
- storage placement being treated as Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, or governed meaning;
- implementation visibility being treated as approval, authority, validation, privacy clearance, publication readiness, export readiness, migration readiness, or downstream-use permission;
- missing metadata where metadata is required for interpretation or use;
- missing Source References where source support affects interpretation or use;
- missing provenance where origin, transformation, review, agent activity, workflow activity, import, export, migration, or change history affects interpretation or use;
- relationship suggestions being treated as approved relationships;
- restricted material being exposed through content, metadata, Source References, provenance, relationships, workflow logs, agent outputs, validation results, storage routing, indexing, synchronization, backup, publication, export, migration, or implementation behavior;
- agent activity exceeding authorized scope;
- Human Review being skipped where required;
- deletion or overwrite occurring without governed authorization;
- transformation replacing Source Material without governed authorization;
- workflow logs becoming hidden sources of governed meaning;
- import, export, migration, backup, synchronization, indexing, or publication success being treated as full conformance;
- another failure to preserve the boundaries defined by WF-0001.

A non-conformance finding SHOULD identify or support identification of:

- the affected workflow;
- the affected entity or material;
- the affected conformance scope;
- the requirement that was not satisfied;
- the actor, agent, workflow, implementation, validator, import process, export process, migration process, or storage process involved where applicable;
- the severity of the issue where applicable;
- whether privacy risk exists;
- whether authority risk exists;
- whether validation risk exists;
- whether source-reference or provenance risk exists;
- whether relationship risk exists;
- whether identity risk exists;
- whether publication, export, migration, deletion, overwrite, or downstream-use risk exists;
- what repair, recovery, quarantine, rejection, escalation, or review is required.

Non-conformance MUST remain visible enough for appropriate review, repair, recovery, escalation, quarantine, rejection, archival, validation, governance review, or downstream-use limitation.

A workflow MUST NOT hide, discard, overwrite, normalize away, or silently resolve non-conformance where doing so causes loss of meaning, broken provenance, privacy exposure, authority ambiguity, validation ambiguity, source-reference loss, relationship ambiguity, identity ambiguity, implementation lock-in, migration loss, export ambiguity, governance drift, or downstream-use risk.

An exception is a documented, scoped, reviewable deviation from WF-0001.

An exception MAY be permitted only where the deviation is necessary, justified, limited, traceable, privacy-respecting, reviewable, and compatible with higher-authority standards.

An exception SHOULD identify or support identification of:

- the exception scope;
- the requirement being excepted;
- the reason for the exception;
- the approving human, governance process, or authority where applicable;
- the affected material or workflow;
- the expected duration where applicable;
- the risk created;
- the privacy impact;
- the validation impact;
- the authority impact;
- the source-reference or provenance impact;
- the relationship impact;
- the storage impact;
- the agent impact;
- the implementation impact;
- the import, export, or migration impact where applicable;
- the recovery or closure condition;
- the review requirement.

An exception MUST NOT override the constitutional foundation.

An exception MUST NOT silently redefine knowledge meaning.

An exception MUST NOT silently weaken Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, Human Review, agent boundaries, storage boundaries, implementation independence, or governance.

An exception MUST NOT silently permit restricted material exposure, unauthorized agent access, unauthorized publication, unauthorized export, unauthorized migration, unauthorized deletion, unauthorized overwrite, or unauthorized downstream use.

An exception SHOULD be temporary where practical.

A long-term exception SHOULD be converted into a governed standard, specification, implementation profile, operational guide, ADR, RFC, or formal governance decision where it materially affects architecture, workflow behavior, conformance, privacy, authority, validation, storage, agents, implementations, publication, export, migration, or downstream use.

Recovery is the governed process of restoring, repairing, rerouting, revalidating, re-reviewing, quarantining, archiving, rejecting, or otherwise correcting ingestion workflow problems.

Recovery MAY include:

- restoring Source Material;
- restoring prior versions;
- restoring from backup;
- reconstructing provenance;
- repairing Source References;
- repairing metadata;
- repairing relationships;
- repairing Object Identity references;
- repairing lifecycle state;
- repairing authority context;
- repairing privacy handling;
- repairing validation results;
- repairing workflow logs;
- repairing storage routing;
- repairing agent outputs;
- repairing import records;
- repairing export records;
- repairing migration records;
- repairing implementation dependencies;
- rerouting to Human Review;
- rerouting to validation;
- rerouting to privacy review;
- rerouting to authority review;
- rerouting to source-reference review;
- rerouting to provenance review;
- rerouting to relationship review;
- quarantining affected material;
- rejecting affected material;
- archiving affected material;
- limiting downstream use;
- escalating to governance review.

Recovery SHOULD preserve enough traceability to determine what failed, what was repaired, what remains unresolved, and what downstream-use limits apply.

Recovery MUST preserve privacy boundaries.

Recovery MUST NOT expose restricted material merely because recovery, debugging, validation, repair, migration, export, synchronization, indexing, backup, implementation inspection, or agent assistance is easier with broad access.

Recovery MUST preserve agent boundaries.

Agents MAY assist recovery only within authorized scope.

Agent-assisted recovery MUST remain reviewable where recovery affects meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, rejection, repair, quarantine, archival, publication, export, migration, deletion, overwrite, or downstream use.

Recovery MUST preserve validation boundaries.

A repaired workflow output SHOULD be revalidated where the repair affects conformance, meaning, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, compatibility, publication, export, migration, or downstream use.

Recovery MUST preserve Human Review boundaries.

Recovered or repaired material SHOULD be routed for Human Review where the recovery affects high-impact governed decisions, approval, rejection, authority, privacy, Object Identity, publication, export, migration, deletion, overwrite, or downstream use.

Non-Conformance, Exceptions, and Recovery are successful when workflow failures and deviations remain explicit, scoped, traceable, reviewable, privacy-respecting, repairable, recoverable, governance-compatible, implementation-independent, and unable to silently redefine knowledge meaning, authority, privacy, validation, storage meaning, agent authority, or downstream-use permission.

## 18. Success Criteria and Closing Rule

WF-0001 is successful when The Brain Standard has a repeatable, implementation-independent workflow for turning incoming material into governed knowledge without allowing capture, storage, indexing, summarization, agent activity, workflow completion, validation, implementation visibility, import, export, migration, publication, or downstream use to silently redefine meaning.

A successful Knowledge Ingestion workflow enables future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, backup processes, synchronization processes, indexing systems, publication processes, and implementations to determine:

- what material entered ingestion;
- where the material came from;
- what Source Material was preserved;
- what classification occurred;
- what extraction occurred;
- what transformation occurred;
- what Draft Knowledge Record was created where applicable;
- what Knowledge Record was created or updated where applicable;
- what Object Identity applies where applicable;
- what metadata applies;
- what Source References apply;
- what provenance applies;
- what relationships were suggested, reviewed, approved, rejected, repaired, quarantined, archived, or deferred;
- what Lifecycle State applies;
- what Authority Level applies;
- what Privacy Classification applies;
- what Validation applies;
- what Human Review occurred where applicable;
- what agent participation occurred where applicable;
- what was approved;
- what was rejected;
- what was repaired;
- what was quarantined;
- what was archived;
- what was routed;
- what storage routing occurred;
- what workflow logs exist;
- what non-conformance exists where applicable;
- what exceptions exist where applicable;
- what recovery actions occurred where applicable;
- what downstream-use limits apply.

WF-0001 is successful when Source Material remains distinguishable from Knowledge Records.

WF-0001 is successful when Draft Knowledge Records remain distinguishable from approved Knowledge Records.

WF-0001 is successful when workflow outputs remain distinguishable from approved knowledge.

WF-0001 is successful when agent outputs remain distinguishable from Human Review and governed approval.

WF-0001 is successful when validation results remain distinguishable from approval, authority, privacy clearance, publication readiness, export readiness, migration readiness, and downstream-use permission.

WF-0001 is successful when storage routing remains distinguishable from Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, and governed meaning.

WF-0001 is successful when implementation behavior remains distinguishable from standard behavior.

WF-0001 is successful when workflows remain able to coordinate governed action without becoming hidden authorities over the meaning, status, privacy, validation, storage, agent behavior, implementation behavior, or downstream use of knowledge.

WF-0001 is successful when future specifications can safely define more exact ingestion states, required workflow fields, workflow log formats, intake forms, review checklists, metadata extraction rules, Source Reference formats, provenance fields, validation checks, agent task profiles, storage routing rules, import rules, export rules, migration rules, automation behavior, implementation mappings, and templates without weakening the standard-level behavior defined here.

WF-0001 is successful when future implementations can support ingestion in Obsidian, Codex, local tools, databases, file systems, repositories, interfaces, agents, validators, automations, or future platforms without making any single implementation the standard itself.

WF-0001 is successful when ingestion remains:

- explicit;
- traceable;
- reviewable;
- privacy-respecting;
- source-aware;
- provenance-preserving;
- validation-aware;
- authority-aware;
- lifecycle-aware;
- relationship-aware;
- storage-compatible;
- agent-bounded;
- implementation-independent;
- portable;
- repairable;
- recoverable;
- compatible with future specifications;
- usable by humans;
- usable by agents;
- durable across time.

The closing rule of WF-0001 is:

- Workflows coordinate governed ingestion.
- Workflows do not define knowledge meaning.
- Workflows do not create Object Identity silently.
- Workflows do not approve knowledge silently.
- Workflows do not assign authority silently.
- Workflows do not weaken privacy silently.
- Workflows do not convert validation into approval silently.
- Workflows do not convert storage placement into meaning silently.
- Workflows do not convert agent output into governance silently.
- Workflows do not convert implementation behavior into standard behavior silently.
- Workflows do not convert import, export, migration, backup, synchronization, indexing, publication, or downstream use into conformance silently.
- Workflows must preserve enough traceability for future review, repair, recovery, governance, and continued use.

WF-0001 is complete when it can guide a compliant ingestion workflow from intake through Source Material handling, classification, extraction, transformation, Draft Knowledge Record creation, metadata capture, Source Reference capture, provenance capture, relationship review, lifecycle handling, authority handling, privacy handling, validation handling, Human Review, agent participation, approval, rejection, repair, quarantine, storage routing, logging, conformance review, exception handling, recovery, and downstream-readiness assessment without creating architectural drift.
