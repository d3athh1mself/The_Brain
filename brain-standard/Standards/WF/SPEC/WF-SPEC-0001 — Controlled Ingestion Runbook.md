# WF-SPEC-0001 — Controlled Ingestion Runbook

Document ID: WF-SPEC-0001
Title: Controlled Ingestion Runbook
Version: 0.1.0
Status: Approved
Created: 2026-06-29
Last Updated: 2026-06-29
Authority: Specification
Phase: Phase 4 — Workflow Engine
Milestone: 4.S1 — Controlled Ingestion Runbook
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; AG-SPEC-0001 — Agent Initialization Packet; AG-SPEC-0002 — Subagent Prompt and Role Profile Specification; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; WF-0003 — Knowledge Maintenance and Update Workflow Standard; WF-0004 — Publication, Export, and Downstream Use Workflow Standard
Supersedes: None
Superseded By: None
Related: TEMPLATE-0001 — Knowledge Record Template; TEMPLATE-0002 — Source Material Intake Template; TEMPLATE-0003 — Agent Activity Record Template; TEMPLATE-0004 — Review Record Template; VALID-0001 — Bare Usable Validation Checklist

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and controlled-ingestion runbook rules are interpreted within WF-SPEC-0001.

Where conflicts arise between controlled ingestion activity, Source Material, Source References, provenance, extraction, transformation, Draft Knowledge Records, metadata proposals, relationship proposals, validation results, review preparation, routing, escalation, storage behavior, agent behavior, subagent behavior, workflow behavior, implementation behavior, import behavior, export behavior, publication behavior, privacy handling, authority handling, or future specifications, the constitutional foundation and higher-authority standards SHALL guide interpretation and resolution.

WF-SPEC-0001 is subordinate to TB-0000, TB-0001, TB-0002, TB-0003, the Phase 1 Knowledge Standards, the Phase 2 Storage Standards, the Agent Standards, AG-SPEC-0001, AG-SPEC-0002, and the Phase 4 Workflow Standards.

WF-SPEC-0001 extends WF-0001 by defining a practical controlled-ingestion runbook for moving raw material from intake into reviewable workflow outputs.

WF-SPEC-0001 does not replace WF-0001.

WF-SPEC-0001 does not define the full review-and-approval process. That responsibility belongs to WF-0002.

WF-SPEC-0001 does not define maintenance behavior. That responsibility belongs to WF-0003.

WF-SPEC-0001 does not define publication, export, migration, synchronization, indexing, backup, or downstream-use approval. Those responsibilities belong to WF-0004 and later specifications.

WF-SPEC-0001 does not define exact folder paths, exact filenames, exact Markdown front matter syntax, exact metadata field names, exact schemas, exact validation tooling, exact agent prompts, exact subagent prompts, exact model behavior, exact application behavior, exact automation scripts, exact user-interface behavior, or exact implementation-specific routing.

Those concerns belong to templates, validation specifications, implementation profiles, operational guides, reference implementations, and tool-specific setup documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Controlled Ingestion refers to the governed process of receiving, inspecting, classifying, extracting, transforming, drafting, validating, and routing incoming material without allowing intake or automation to become approval.
- Controlled Ingestion Runbook refers to the repeatable operational procedure defined by WF-SPEC-0001.
- Intake refers to the receipt, capture, registration, or staging of incoming material before it becomes a Knowledge Record or is routed elsewhere.
- Intake Area refers to the storage area or implementation-equivalent location where incoming material is staged for controlled ingestion.
- Ingestion Candidate refers to Source Material, captured information, extracted content, proposed knowledge, draft record, or other input being evaluated through the controlled ingestion runbook.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Draft Knowledge Record refers to a proposed Knowledge Record created during ingestion that has not yet completed required validation, review, approval, rejection, repair, quarantine, archival, or routing.
- Extraction refers to selecting, copying, transcribing, parsing, summarizing, segmenting, or otherwise taking information from Source Material for possible governed use.
- Transformation refers to changing Source Material, extracted content, or prior knowledge into another representation, summary, translation, classification, interpretation, structured record, derived object, migrated form, or implementation-specific representation.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context.
- Metadata Proposal refers to metadata suggested during ingestion but not yet approved as final governed metadata unless a higher-authority workflow or specification permits that action.
- Relationship Proposal refers to a proposed connection between governed entities that requires validation and review before it may be treated as approved.
- Validation Result refers to the recorded outcome of checking whether an entity satisfies applicable standards, specifications, templates, workflow expectations, privacy expectations, authority expectations, or implementation boundaries.
- Review Preparation refers to the creation of reviewable outputs that allow a human, governed workflow, or authorized reviewer to inspect ingestion results.
- Routing refers to sending an ingestion candidate or workflow output to the next appropriate state, area, queue, review path, repair path, quarantine path, archive path, rejection path, or escalation path.
- Stop Condition refers to a condition that prevents normal ingestion from continuing until review, repair, privacy handling, authority review, source review, validation, or escalation occurs.
- Agent refers to a human-directed or system-directed AI, automation, script, model-driven process, tool-using assistant, workflow participant, or future automated actor operating under The Brain Standard.
- Subagent refers to a specialized agent role operating under AG-SPEC-0002.
- Human Review refers to review performed by a human to confirm, correct, reject, approve, limit, escalate, or route workflow outputs where governed judgment is required.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of WF-SPEC-0001 is to define a controlled ingestion runbook for moving incoming material from raw intake into reviewable knowledge workflow outputs.

WF-SPEC-0001 exists so that The Brain can support practical file-drop, intake, sorting, extraction, drafting, validation, and routing activity without allowing storage placement, automation, agent output, indexing, summarization, or workflow convenience to become hidden authority.

Controlled ingestion is the bridge between raw information and governed knowledge work.

Raw information MAY enter The Brain through many sources, including files, notes, messages, images, documents, transcripts, datasets, scans, forms, logs, exports, imports, research material, personal captures, or other Source Material.

Raw information does not become governed knowledge merely because it is received, stored, indexed, summarized, classified, extracted, placed in an intake area, processed by an agent, processed by a subagent, or converted into a Draft Knowledge Record.

WF-SPEC-0001 defines the runbook behavior required to:

- receive Source Material;
- preserve Source Material as Source Material;
- inspect incoming material;
- classify material for controlled handling;
- identify privacy and authority risks;
- preserve source context;
- capture provenance;
- extract useful content;
- create Draft Knowledge Records where appropriate;
- propose metadata;
- propose relationships;
- propose Source References;
- perform validation checks;
- prepare review outputs;
- route material to the correct next state;
- escalate ambiguity, conflict, risk, or stop conditions.

WF-SPEC-0001 is intended for supervised bare-usable deployment.

It supports agent and subagent assistance, but it does not permit agents or subagents to become unreviewable authorities over Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, publication, export, migration, deletion, supersession, deprecation, or downstream use.

WF-SPEC-0001 is implementation-independent.

A compliant implementation MAY realize this runbook through folders, forms, scripts, manual steps, local files, repositories, databases, workflow tools, AI agents, subagents, command-line tools, note-taking software, document systems, or future platforms.

The implementation method does not define the standard.

The controlled ingestion behavior defined by WF-SPEC-0001 remains the governing requirement.

WF-SPEC-0001 is successful when future humans, agents, subagents, workflows, validators, storage systems, and implementations can determine:

- what material entered ingestion;
- where it came from;
- what Source Material was preserved;
- what was extracted;
- what was transformed;
- what Draft Knowledge Records were created;
- what metadata was proposed;
- what relationships were proposed;
- what Source References were proposed;
- what validation findings were produced;
- what privacy or authority risks were detected;
- what review output was prepared;
- what routing decision was made;
- what still requires human or governed review.

## 2. Relationship to Prior Standards

WF-SPEC-0001 is subordinate to and derived from the constitutional foundation of The Brain Standard.

WF-SPEC-0001 depends on:

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
- AG-0001 — Agent Operating Boundaries Standard;
- AG-SPEC-0001 — Agent Initialization Packet;
- AG-SPEC-0002 — Subagent Prompt and Role Profile Specification;
- WF-0001 — Knowledge Ingestion Workflow Standard;
- WF-0002 — Review and Approval Workflow Standard;
- WF-0003 — Knowledge Maintenance and Update Workflow Standard;
- WF-0004 — Publication, Export, and Downstream Use Workflow Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

WF-SPEC-0001 applies that purpose by defining a practical ingestion runbook that preserves knowledge durability, traceability, reviewability, portability, and implementation independence during intake activity.

TB-0001 establishes architecture principles.

WF-SPEC-0001 applies those principles by preserving:

- knowledge integrity;
- implementation independence;
- source distinction;
- explicit structure;
- provenance;
- privacy boundaries;
- authority boundaries;
- validation expectations;
- human reviewability;
- AI readability;
- practical daily usability;
- governed evolution.

TB-0002 establishes the layered architecture.

WF-SPEC-0001 belongs to Layer 4 — Workflow Engine.

Because WF-SPEC-0001 is a workflow specification, it MAY define repeatable operational procedure.

It MUST NOT redefine knowledge meaning, storage meaning, agent authority, implementation requirements, document governance, or standard-level definitions established by higher-authority documents.

The Phase 1 Knowledge Standards define the meaning and governance behavior of Knowledge Objects, Knowledge Records, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation.

WF-SPEC-0001 uses those concepts during ingestion.

WF-SPEC-0001 does not redefine those concepts.

The Phase 2 Storage Standards define how storage may support knowledge and Source Material without defining meaning.

WF-SPEC-0001 may use intake areas, draft areas, review areas, quarantine areas, archive areas, source-material areas, knowledge-record areas, workflow-output areas, or implementation-support areas.

Those storage areas support routing and usability.

They do not define Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, rejection, publication readiness, export readiness, or downstream-use permission by themselves.

AG-0001 defines agent operating boundaries.

WF-SPEC-0001 allows agents to assist controlled ingestion only within those boundaries.

Agents MAY inspect, classify, summarize, extract, draft, propose metadata, propose relationships, propose Source References, detect risks, validate, prepare review outputs, and recommend routing where authorized.

Agents MUST NOT silently approve governed entities, assign final Object Identity, assign final Authority Level, assign final Privacy Classification, finalize relationships, finalize Source References, perform final lifecycle transitions, publish, export, migrate, delete, merge, split, supersede, deprecate, or override governance.

AG-SPEC-0001 defines the initialization expectations for agents before work begins.

WF-SPEC-0001 assumes that any agent assisting controlled ingestion has received sufficient initialization context, including applicable standards, permission scope, privacy expectations, authority limits, validation expectations, workflow expectations, and escalation rules.

AG-SPEC-0002 defines reusable subagent prompt and role profiles.

WF-SPEC-0001 may use those subagent roles during ingestion, including intake, classification, extraction, metadata proposal, relationship proposal, validation, privacy-risk detection, review preparation, maintenance support, export-preparation support, and implementation support.

Subagent role specialization does not create additional authority.

A subagent operating inside controlled ingestion remains subordinate to the runbook, the workflow standards, agent standards, knowledge standards, storage standards, and constitutional foundation.

WF-0001 defines the standard-level Knowledge Ingestion Workflow.

WF-SPEC-0001 operationalizes WF-0001 by defining the controlled runbook sequence for intake and review preparation.

WF-0002 defines review and approval behavior.

WF-SPEC-0001 may prepare material for review, but it does not complete approval unless a higher-authority workflow or specification explicitly defines a limited approval behavior.

WF-0003 defines maintenance and update behavior.

WF-SPEC-0001 may route material to maintenance if ingestion reveals that existing governed knowledge needs correction, update, validation refresh, source-reference repair, relationship repair, privacy review, authority review, or lifecycle reassessment.

WF-0004 defines publication, export, and downstream-use behavior.

WF-SPEC-0001 may identify publication, export, migration, synchronization, indexing, backup, or downstream-use concerns, but it does not grant permission for those actions.

WF-SPEC-0001 is successful when it applies prior standards without duplicating, weakening, overriding, or redefining them.

## 3. Controlled Ingestion Scope and Use Rules

WF-SPEC-0001 applies to controlled ingestion activity within The Brain Standard.

Controlled ingestion activity includes any governed process where incoming material is received, staged, inspected, classified, extracted, summarized, transformed, drafted, validated, reviewed, routed, repaired, quarantined, rejected, archived, or prepared for later approval.

Controlled ingestion MAY apply to:

- documents;
- notes;
- messages;
- images;
- recordings;
- transcripts;
- datasets;
- web pages;
- scans;
- forms;
- logs;
- exports;
- imports;
- research material;
- reference material;
- personal captures;
- project files;
- operational records;
- implementation artifacts;
- other Source Material.

Controlled ingestion MAY be performed manually, agent-assisted, subagent-assisted, workflow-assisted, implementation-assisted, or automation-assisted.

The method of execution does not change the governed meaning of the process.

### 3.1 In-Scope Activities

The following activities are in scope for WF-SPEC-0001:

- receiving incoming material;
- registering or noting intake context;
- preserving Source Material;
- identifying material type;
- identifying likely knowledge value;
- identifying privacy risks;
- identifying authority risks;
- identifying source context;
- capturing provenance;
- extracting relevant content;
- summarizing where appropriate;
- creating Draft Knowledge Records where appropriate;
- proposing metadata;
- proposing relationships;
- proposing Source References;
- identifying duplicate, derivative, merge, split, supersession, or maintenance concerns;
- performing validation checks;
- preparing review notes;
- recommending routing;
- routing to review, repair, quarantine, archive, rejection, maintenance, or escalation.

### 3.2 Out-of-Scope Activities

The following activities are out of scope for WF-SPEC-0001 unless a higher-authority workflow, specification, or governance decision explicitly authorizes them:

- final approval of Knowledge Records;
- final assignment of stable Object Identity;
- final approval of metadata;
- final approval of relationships;
- final approval of Source References;
- final approval of provenance records;
- final assignment of Authority Level;
- final assignment of Privacy Classification;
- final lifecycle transitions into approved, deprecated, superseded, archived, published, exported, migrated, or downstream-use-ready states;
- publication;
- export;
- migration;
- synchronization approval;
- indexing approval where privacy or authority risk exists;
- backup approval where privacy or handling risk exists;
- deletion;
- destructive overwrite;
- merge;
- split;
- supersession;
- deprecation;
- governance override;
- privacy override;
- authority override;
- treating validation success as approval.

### 3.3 Controlled Ingestion Use Rules

Controlled ingestion SHALL begin with Source Material or captured information.

Controlled ingestion SHALL preserve the distinction between Source Material and Knowledge Records.

A Source Material item MUST NOT become a Knowledge Record merely because it is stored, moved, renamed, indexed, summarized, classified, extracted, transformed, processed by an agent, or placed in a workflow.

A Draft Knowledge Record created during controlled ingestion MUST remain distinguishable from an approved Knowledge Record.

A Draft Knowledge Record MUST NOT be treated as approved merely because it is structurally complete, validation-passing, agent-generated, human-readable, useful, linked, indexed, or stored in a convenient location.

Controlled ingestion SHOULD preserve enough provenance to determine:

- what material was received;
- where it came from;
- when it entered ingestion where available;
- who or what processed it where applicable;
- what extraction or transformation occurred;
- what agent or subagent participated where applicable;
- what validation results were produced;
- what review preparation output was created;
- what routing decision or recommendation was made.

Controlled ingestion MUST include privacy-risk awareness before material is broadly exposed, summarized, indexed, synchronized, exported, published, or made available to agents beyond the authorized scope.

Controlled ingestion MUST include authority-risk awareness before material is treated as reliable, official, approved, governing, publication-ready, export-ready, migration-ready, or suitable for downstream use.

Controlled ingestion SHOULD create reviewable outputs rather than hidden state.

A future human, agent, workflow, validator, or implementation SHOULD be able to inspect the ingestion result and determine what happened.

### 3.4 Agent and Subagent Use Rules

Agents and subagents MAY assist controlled ingestion only within authorized boundaries.

An agent or subagent MAY:

- inspect Source Material;
- summarize Source Material;
- classify material type;
- identify likely knowledge value;
- extract relevant content;
- identify possible Source References;
- propose provenance entries;
- propose metadata;
- propose relationships;
- draft Knowledge Records;
- identify validation issues;
- detect privacy risks;
- detect authority risks;
- prepare review notes;
- recommend routing.

An agent or subagent MUST NOT:

- silently approve Knowledge Records;
- silently convert Source Material into approved knowledge;
- silently assign final Object Identity;
- silently approve metadata;
- silently approve relationships;
- silently approve Source References;
- silently assign Authority Level;
- silently assign Privacy Classification;
- silently perform final Lifecycle State transitions;
- silently publish;
- silently export;
- silently migrate;
- silently delete;
- silently merge;
- silently split;
- silently supersede;
- silently deprecate;
- silently override human review;
- silently override governance.

Agent or subagent confidence MUST NOT be treated as approval.

Agent or subagent completion MUST NOT be treated as approval.

Agent or subagent output MUST remain traceable where it affects meaning, metadata, relationships, Source References, provenance, lifecycle handling, authority, privacy, validation, routing, review, publication, export, migration, deletion, or downstream use.

### 3.5 Storage and Implementation Use Rules

Controlled ingestion MAY use implementation-specific storage areas, queues, labels, tags, forms, dashboards, scripts, commands, prompts, or workflow tools.

Those mechanisms support execution.

They do not define governed meaning by themselves.

Storage placement MUST NOT be the sole source of:

- Object Identity;
- Source Reference validity;
- provenance validity;
- metadata validity;
- relationship validity;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- approval;
- rejection;
- publication readiness;
- export readiness;
- migration readiness;
- downstream-use readiness.

Implementation behavior MUST NOT redefine controlled ingestion.

A tool may make ingestion easier.

A tool does not become the standard.

A compliant implementation MUST preserve the runbook’s governed meaning even if its interface, folder structure, database structure, automation, plugin behavior, script behavior, model provider, or workflow engine changes.

### 3.6 Stop Conditions

Controlled ingestion MUST stop normal processing and route to review, repair, quarantine, archive, rejection, or escalation when a stop condition is detected.

Stop conditions include:

- unknown or unclear source origin;
- missing or insufficient provenance where provenance is required;
- privacy-sensitive material without clear handling permission;
- restricted material exposed to an unauthorized agent, workflow, implementation, index, sync target, export, publication path, or downstream-use path;
- unclear authority level where downstream use may depend on trust;
- conflicting source material;
- suspected duplicate requiring identity review;
- possible merge, split, supersession, or deprecation concern;
- validation failure affecting required structure, identity, metadata, relationships, Source References, provenance, lifecycle, authority, privacy, compatibility, or workflow handling;
- corrupted, unreadable, incomplete, or unsupported material;
- destructive action request;
- publication, export, migration, synchronization, indexing, backup, or downstream-use risk;
- agent or subagent uncertainty that affects governed meaning or handling;
- any ambiguity that cannot be safely resolved within the authorized scope of ingestion.

A stop condition MUST NOT be ignored merely because ingestion automation can continue.

A stop condition SHOULD produce a reviewable note explaining the issue, affected material, applicable risk, and recommended routing.

## 4. Intake Folder and Source Material Handling

The purpose of this section is to define how incoming material is handled at the beginning of controlled ingestion.

Incoming material SHALL be treated as Source Material or captured information until a governed workflow determines otherwise.

Placement in an intake folder, intake area, upload queue, import area, repository path, note-taking inbox, database table, automation queue, or implementation-specific capture location MUST NOT convert incoming material into a Knowledge Record by itself.

The intake process exists to preserve Source Material, prevent premature interpretation, establish initial handling context, identify risks, and prepare material for inspection.

### 4.1 Intake Area Purpose

An Intake Area is a practical staging location for material entering controlled ingestion.

An Intake Area MAY be implemented as:

- a folder;
- a repository path;
- a database queue;
- an upload location;
- a note-taking inbox;
- a form submission area;
- an import staging area;
- a manual review pile;
- an agent-readable workspace;
- an implementation-specific equivalent.

The Intake Area supports workflow execution.

The Intake Area does not define knowledge meaning.

A file, note, record, source artifact, image, transcript, dataset, message, scan, or other item placed in an Intake Area remains an intake item until the controlled ingestion process inspects, classifies, extracts, validates, routes, archives, rejects, quarantines, or drafts from it.

Storage placement MAY help humans, agents, subagents, workflows, or implementations locate incoming material.

Storage placement MUST NOT be the sole basis for Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication readiness, export readiness, migration readiness, or downstream-use permission.

### 4.2 Source Material Preservation

Controlled ingestion SHALL preserve Source Material in a form sufficient for future review where preservation is practical, lawful, safe, and within the applicable privacy boundary.

Preservation SHOULD maintain enough context to determine:

- what the Source Material is;
- where it came from;
- when it entered intake where available;
- who or what provided it where available;
- whether it was imported, exported, copied, captured, scanned, downloaded, transcribed, generated, or manually created;
- whether it is complete, partial, corrupted, redacted, restricted, unavailable, or uncertain;
- whether any transformation occurred before ingestion;
- whether the material contains privacy-sensitive or restricted information;
- whether the material requires quarantine or special handling.

Source Material SHOULD remain distinguishable from:

- extracted content;
- summaries;
- transformations;
- Draft Knowledge Records;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- validation results;
- review notes;
- workflow logs;
- agent outputs;
- implementation-generated artifacts.

A Source Material item MUST NOT be overwritten by an extracted, summarized, cleaned, converted, or transformed version unless the original has been preserved or the loss is explicitly reviewed and accepted under a governed process.

Where exact preservation is not possible, the ingestion output SHOULD record the limitation.

Examples of preservation limitations MAY include:

- source unavailable;
- original deleted before intake;
- partial capture only;
- unreadable file;
- corrupted file;
- redacted source;
- restricted source;
- external reference only;
- source too large for current implementation;
- unsupported format;
- unclear origin.

### 4.3 Intake Registration

Controlled ingestion SHOULD create or support an intake registration record where the incoming material has ongoing knowledge, privacy, authority, source, review, validation, or workflow value.

An intake registration record SHOULD identify or support identification of:

- intake item title or temporary label;
- intake date where available;
- intake source where available;
- material type where known;
- file format or representation where relevant;
- source origin where known;
- source owner, creator, sender, publisher, or provider where known;
- initial privacy concern where known;
- initial authority concern where known;
- initial handling restriction where known;
- assigned agent, subagent, human, workflow, or implementation where applicable;
- initial routing state;
- temporary identifier where needed;
- location of preserved Source Material where applicable.

An intake registration record MAY be lightweight.

The intake registration process SHOULD NOT create excessive burden for low-risk, low-value, or temporary material.

However, intake registration MUST be sufficient where missing context would create source confusion, provenance loss, privacy exposure, validation failure, authority confusion, duplicate confusion, or review ambiguity.

Temporary identifiers MAY be used during intake.

A temporary identifier MUST remain distinguishable from stable Object Identity.

A temporary identifier MUST NOT be treated as final Object Identity unless a governed identity process later confirms or assigns that identity.

### 4.4 Intake Safety Handling

Controlled ingestion MUST check whether incoming material requires restricted handling before broad processing occurs.

Restricted handling MAY be required when material contains or appears to contain:

- personal information;
- credentials;
- private communications;
- sensitive financial information;
- sensitive health information;
- confidential project information;
- legal material;
- security-sensitive information;
- restricted source material;
- proprietary information;
- private images, recordings, or transcripts;
- information subject to publication, export, synchronization, indexing, or sharing limits.

Where restricted handling is suspected, controlled ingestion SHOULD limit exposure until review determines the appropriate Privacy Classification and handling path.

Agents and subagents MUST NOT be granted broader access than necessary merely because material was placed in the Intake Area.

An intake item SHOULD be routed to quarantine, privacy review, or escalation when its privacy handling is unclear and normal processing could expose restricted information.

A privacy warning does not reject the material by itself.

A privacy warning controls handling until the material is reviewed, restricted, repaired, redacted, quarantined, archived, or routed under an approved process.

### 4.5 Intake Outputs

The intake stage SHOULD produce enough output to support the next stage of controlled ingestion.

Intake outputs MAY include:

- preserved Source Material;
- intake registration record;
- temporary label or temporary identifier;
- initial material-type note;
- initial privacy-risk note;
- initial authority-risk note;
- initial provenance note;
- initial handling restriction;
- initial routing recommendation;
- quarantine note where needed;
- escalation note where needed.

The intake stage SHOULD NOT produce final Knowledge Records, final metadata, final relationships, final Source References, final Authority Level, final Privacy Classification, final Lifecycle State, publication approval, export approval, migration approval, or downstream-use approval.

The intake stage prepares material for inspection.

It does not complete ingestion.

## 5. Initial Inspection and Classification Steps

The purpose of initial inspection and classification is to determine what the incoming material appears to be, how it should be handled, whether it has knowledge value, and what risks or workflow paths apply.

Initial inspection and classification SHALL remain provisional unless a higher-authority workflow, specification, or review process explicitly defines final classification behavior.

Classification supports routing.

Classification does not create approval.

### 5.1 Inspection Preconditions

Before inspection begins, the ingestion actor SHOULD confirm that the material is safe and authorized to inspect within the current workflow scope.

The ingestion actor MAY be a human, agent, subagent, workflow, implementation, script, validator, or other authorized participant.

Inspection SHOULD confirm or note:

- whether the item is accessible;
- whether the item is readable;
- whether the file or record appears complete;
- whether the format is supported;
- whether the item appears duplicated;
- whether source origin is known;
- whether privacy risk is visible;
- whether authority risk is visible;
- whether the material appears to be Source Material, extracted content, generated content, transformed content, or an existing Knowledge Record;
- whether the item should continue through normal ingestion.

If the material cannot be safely inspected, the ingestion actor SHOULD route it to review, repair, quarantine, archive, rejection, or escalation.

Inspection MUST NOT bypass stop conditions.

### 5.2 Material Type Classification

Controlled ingestion SHOULD classify incoming material by apparent material type.

Material type classification MAY include:

- document;
- note;
- message;
- image;
- recording;
- transcript;
- dataset;
- web page;
- scan;
- form;
- log;
- code file;
- export;
- import package;
- reference material;
- personal capture;
- project material;
- operational record;
- implementation artifact;
- unknown or mixed material.

Material type classification SHOULD support later extraction, provenance capture, metadata proposal, validation, review preparation, and routing.

Material type classification MUST remain distinguishable from Knowledge Object type unless a governed specification explicitly maps the material into a Knowledge Object type.

A document about a concept is not automatically a Concept Knowledge Object.

A message about a project is not automatically a Project Knowledge Object.

A file stored in a project folder is not automatically project knowledge.

A material type classification describes the incoming material.

It does not finalize the meaning of the knowledge that may later be created from that material.

### 5.3 Knowledge Value Assessment

Controlled ingestion SHOULD assess whether incoming material has potential knowledge value.

Knowledge value assessment MAY consider whether the material:

- contains reusable information;
- supports an existing Knowledge Record;
- may justify a new Draft Knowledge Record;
- provides evidence for a claim, decision, procedure, project, person, concept, source, event, or reference;
- updates or corrects existing knowledge;
- creates a possible relationship;
- affects authority, privacy, lifecycle, validation, publication, export, migration, or downstream use;
- should be archived as Source Material only;
- should be rejected as irrelevant, duplicate, unsafe, corrupted, or out of scope.

Knowledge value assessment is provisional.

A high-value assessment does not approve the material.

A low-value assessment does not delete the material by itself.

A no-value assessment SHOULD route material to rejection, archive, or review according to the applicable workflow and privacy requirements.

### 5.4 Risk Classification

Controlled ingestion MUST identify visible risks that affect handling.

Risk classification SHOULD include:

- privacy risk;
- authority risk;
- source-origin risk;
- provenance risk;
- validation risk;
- duplicate risk;
- relationship risk;
- lifecycle risk;
- storage risk;
- compatibility risk;
- publication risk;
- export risk;
- migration risk;
- downstream-use risk;
- agent-access risk;
- implementation-exposure risk.

Risk classification does not resolve the risk by itself.

A detected risk SHOULD produce a routing recommendation, review note, quarantine note, repair note, or escalation note.

A high-risk item SHOULD NOT continue through normal ingestion unless the risk is handled within the authorized workflow scope.

### 5.5 Classification Outputs

The inspection and classification stage SHOULD produce reviewable classification output.

Classification output MAY include:

- material type;
- apparent source type;
- apparent content type;
- apparent knowledge value;
- apparent privacy risk;
- apparent authority risk;
- apparent provenance status;
- apparent duplicate status;
- apparent extraction suitability;
- apparent Draft Knowledge Record suitability;
- recommended subagent role where applicable;
- recommended validation checks;
- recommended routing path;
- stop condition note where applicable.

Classification output SHOULD remain explicitly provisional until reviewed or confirmed under a governed process.

An agent-generated classification MUST be marked or traceable as agent-generated where the classification affects routing, privacy handling, authority handling, validation, review, extraction, drafting, publication, export, migration, or downstream use.

Classification output MUST NOT silently become final metadata, final lifecycle state, final privacy classification, final authority level, final relationship, final Source Reference, approval, rejection, publication readiness, export readiness, migration readiness, or downstream-use readiness.

## 6. Source Extraction and Provenance Capture

The purpose of source extraction and provenance capture is to select useful information from Source Material while preserving enough context to determine where the information came from, how it was handled, and what limitations apply.

Extraction SHALL remain distinguishable from approval.

Extracted content does not become governed knowledge merely because it was copied, summarized, transcribed, parsed, transformed, or drafted into a structured format.

Provenance capture exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can understand the origin and handling history of extracted content.

### 6.1 Extraction Preconditions

Before extraction begins, the ingestion actor SHOULD confirm that extraction is permitted within the applicable privacy, authority, source, workflow, and agent-access boundaries.

Extraction SHOULD NOT proceed normally when:

- Source Material is unavailable;
- source origin is unknown and required;
- material is unreadable or corrupted;
- privacy handling is unclear;
- authority handling is unclear;
- extraction would expose restricted content;
- extraction would violate source restrictions;
- extraction would exceed authorized agent or subagent scope;
- the material requires quarantine;
- the material requires human review before processing;
- another stop condition applies.

Where extraction cannot proceed, the ingestion actor SHOULD record the reason and route the item to review, repair, quarantine, archive, rejection, or escalation.

### 6.2 Extraction Methods

Controlled ingestion MAY use different extraction methods depending on material type, implementation capability, privacy boundary, and workflow need.

Extraction methods MAY include:

- manual reading;
- copying selected text;
- transcription;
- summarization;
- parsing;
- segmentation;
- image description;
- table extraction;
- metadata extraction;
- entity extraction;
- keyword extraction;
- claim extraction;
- decision extraction;
- procedure extraction;
- relationship cue extraction;
- source-reference cue extraction;
- conversion into a reviewable intermediate format.

Extraction methods SHOULD be selected to preserve meaning, context, source traceability, privacy handling, and reviewability.

An extraction method MUST NOT silently discard context where context is required for interpretation, authority, privacy, validation, relationship handling, Source Reference handling, provenance, review, publication, export, migration, or downstream use.

Automated extraction MAY be used where authorized.

Automated extraction MUST remain reviewable where the extracted content affects governed meaning.

### 6.3 Extraction Boundaries

Extraction SHOULD distinguish between:

- direct copied content;
- paraphrased content;
- summarized content;
- transcribed content;
- interpreted content;
- translated content;
- transformed content;
- inferred content;
- agent-generated content;
- human-authored content;
- workflow-generated content.

The extraction output SHOULD indicate when material has been summarized, interpreted, transformed, translated, or inferred rather than directly copied.

Extraction MUST NOT present interpretation as direct source content.

Extraction MUST NOT present agent-generated wording as source wording.

Extraction MUST NOT present uncertain source support as confirmed source support.

Extraction SHOULD preserve uncertainty where uncertainty affects meaning, authority, validation, review, or downstream use.

Extracted content MAY support a Draft Knowledge Record.

Extracted content does not approve the Draft Knowledge Record.

Extracted content MAY support a Source Reference proposal.

Extracted content does not approve the Source Reference.

Extracted content MAY support a relationship proposal.

Extracted content does not approve the relationship.

### 6.4 Provenance Capture Requirements

Controlled ingestion SHOULD capture provenance for extraction activity where provenance affects interpretation, authority, privacy, validation, review, compatibility, publication, export, migration, or downstream use.

Provenance capture SHOULD identify or support identification of:

- Source Material used;
- source origin where known;
- source location or reference where available;
- source availability status where relevant;
- source reliability concern where known;
- source authority concern where known;
- source privacy concern where known;
- extraction actor where relevant;
- agent or subagent involved where applicable;
- extraction method where relevant;
- extraction date where available;
- transformation or summarization performed;
- limitations or uncertainty;
- review requirement;
- validation requirement;
- routing recommendation.

Provenance capture MAY be lightweight where the material is low-risk, low-authority, temporary, or not intended for downstream use.

Provenance capture MUST be stronger where the material affects governed meaning, review, authority, privacy, validation, relationships, Source References, publication, export, migration, or downstream use.

Where provenance is missing, incomplete, uncertain, or restricted, the extraction output SHOULD clearly state that limitation.

Missing provenance MUST NOT be hidden by confident language, agent confidence, workflow completion, formatting quality, or storage placement.

### 6.5 Extraction Outputs

The extraction and provenance stage SHOULD produce reviewable outputs.

Extraction outputs MAY include:

- extracted content;
- source excerpts where permitted;
- source summaries;
- transcription notes;
- transformation notes;
- interpretation notes;
- uncertainty notes;
- provenance notes;
- source availability notes;
- source reliability notes;
- source authority notes;
- source privacy notes;
- extraction method notes;
- agent or subagent participation notes;
- Draft Knowledge Record readiness notes;
- Source Reference proposal readiness notes;
- relationship proposal readiness notes;
- validation recommendations;
- review recommendations;
- routing recommendations.

Extraction outputs SHOULD be organized so that later stages can determine whether the material should become:

- a Draft Knowledge Record;
- a metadata proposal;
- a relationship proposal;
- a Source Reference proposal;
- a validation finding;
- a review note;
- a maintenance trigger;
- an archive item;
- a rejected item;
- a quarantined item;
- an escalated item.

Extraction output MUST NOT be treated as final approval.

Extraction output MUST remain traceable to the Source Material or to the reason why the Source Material is unavailable, restricted, incomplete, uncertain, or unverifiable.

## 7. Draft Knowledge Record Creation

The purpose of this section is to define how controlled ingestion may create Draft Knowledge Records from Source Material, extracted content, human reasoning, agent activity, subagent activity, or workflow outputs.

A Draft Knowledge Record is a proposed Knowledge Record.

A Draft Knowledge Record is not an approved Knowledge Record merely because it is structured, useful, readable, linked, indexed, validated, agent-generated, human-reviewed in part, or placed in a knowledge-record area.

Draft Knowledge Record creation exists to make possible knowledge reviewable.

It does not complete approval.

### 7.1 Draft Creation Preconditions

Controlled ingestion SHOULD create a Draft Knowledge Record only when the intake, inspection, classification, extraction, and provenance stages indicate that the material has potential governed knowledge value.

A Draft Knowledge Record MAY be appropriate when incoming material:

- contains reusable knowledge;
- supports a new Knowledge Object;
- supports an existing Knowledge Object;
- updates or corrects existing knowledge;
- provides evidence for a claim, decision, procedure, project, person, concept, event, source, or reference;
- contains structured information worth preserving;
- creates a useful relationship proposal;
- requires review before being approved, rejected, archived, repaired, quarantined, or escalated.

A Draft Knowledge Record SHOULD NOT be created merely because material exists.

A Draft Knowledge Record SHOULD NOT be created merely because an agent or subagent can summarize the material.

A Draft Knowledge Record SHOULD NOT be created when the material should remain Source Material only, be archived without transformation, be rejected as out of scope, be quarantined, or be escalated before drafting.

Where draft suitability is uncertain, the ingestion actor SHOULD create a review note rather than forcing a Draft Knowledge Record.

### 7.2 Draft Knowledge Record Boundaries

A Draft Knowledge Record MUST remain distinguishable from:

- Source Material;
- extracted content;
- summaries;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- provenance notes;
- validation results;
- review notes;
- workflow logs;
- agent outputs;
- subagent outputs;
- implementation-generated artifacts;
- approved Knowledge Records.

A Draft Knowledge Record MAY contain extracted, summarized, interpreted, transformed, or synthesized content.

When it does, the draft SHOULD preserve enough context to determine whether the content is:

- directly copied;
- paraphrased;
- summarized;
- transcribed;
- interpreted;
- translated;
- transformed;
- inferred;
- human-authored;
- agent-generated;
- subagent-generated;
- workflow-generated.

A Draft Knowledge Record MUST NOT present Source Material, extracted content, or agent-generated content as approved knowledge unless review and approval have occurred under the applicable workflow.

A Draft Knowledge Record MUST NOT hide uncertainty, missing source context, missing provenance, privacy concerns, authority concerns, validation issues, duplicate concerns, or relationship concerns.

### 7.3 Draft Identity Handling

Draft Knowledge Records MAY use temporary identifiers during controlled ingestion.

A temporary identifier supports drafting, review, routing, validation, and traceability.

A temporary identifier MUST remain distinguishable from stable Object Identity.

A temporary identifier MUST NOT be treated as final Object Identity unless a governed identity process later assigns or confirms stable Object Identity.

A Draft Knowledge Record SHOULD include or support enough identity context to determine whether it may represent:

- a new Knowledge Object;
- an existing Knowledge Object;
- a duplicate of an existing Knowledge Object;
- a derivative object;
- a possible split;
- a possible merge;
- a possible supersession;
- a possible update to an existing record;
- a temporary workflow output that should not become a Knowledge Object.

Where identity is uncertain, the draft SHOULD mark identity as unresolved and route to identity review, repair, or escalation.

An agent or subagent MAY propose identity handling.

An agent or subagent MUST NOT assign final stable Object Identity unless a future governed specification explicitly grants that limited authority under reviewable conditions.

### 7.4 Draft Content Requirements

A Draft Knowledge Record SHOULD contain enough structure to support validation and review.

A Draft Knowledge Record SHOULD identify or support identification of:

- proposed title or label;
- temporary identifier where used;
- source material used;
- extraction or transformation context;
- proposed knowledge content;
- source support or source limitation;
- provenance notes;
- proposed metadata;
- proposed relationships;
- proposed Source References;
- privacy concerns;
- authority concerns;
- validation concerns;
- duplicate or identity concerns;
- review questions;
- routing recommendation.

A Draft Knowledge Record SHOULD be written in a form that is understandable to humans and interpretable by AI systems.

A Draft Knowledge Record SHOULD avoid excessive structure where the material is simple.

A Draft Knowledge Record SHOULD include stronger structure where the material affects authority, privacy, validation, relationships, Source References, publication, export, migration, or downstream use.

Draft content MUST NOT rely only on hidden application state, agent memory, workflow memory, folder placement, tags, interface state, plugin behavior, or implementation-specific metadata where that information affects governed meaning.

### 7.5 Draft Knowledge Record Outputs

The Draft Knowledge Record creation stage SHOULD produce reviewable outputs.

Draft outputs MAY include:

- Draft Knowledge Record;
- temporary identifier;
- proposed title;
- proposed object-type note where applicable;
- source support note;
- provenance note;
- extraction summary;
- transformation note;
- metadata proposal note;
- relationship proposal note;
- Source Reference proposal note;
- validation issue note;
- privacy issue note;
- authority issue note;
- identity issue note;
- duplicate concern note;
- review question;
- routing recommendation.

Draft outputs MUST remain subject to validation and review.

A Draft Knowledge Record MAY proceed to metadata proposal, relationship proposal, Source Reference proposal, validation, review preparation, repair, quarantine, archive, rejection, maintenance routing, or escalation.

A Draft Knowledge Record MUST NOT proceed to final approval, publication, export, migration, deletion, supersession, deprecation, or downstream-use readiness through controlled ingestion alone.

## 8. Metadata, Relationship, and Source Reference Proposal Steps

The purpose of this section is to define how controlled ingestion may propose metadata, relationships, and Source References for Draft Knowledge Records or other ingestion outputs.

Metadata, relationship, and Source Reference proposals support later review.

They do not create final governed approval by themselves.

A proposal remains a proposal until reviewed, accepted, corrected, rejected, repaired, superseded, archived, or otherwise routed under the applicable standard, workflow, or specification.

### 8.1 Metadata Proposal Steps

Controlled ingestion MAY propose metadata for Source Material, Draft Knowledge Records, extraction outputs, validation outputs, workflow outputs, agent outputs, subagent outputs, and review outputs.

Metadata proposals SHOULD support:

- identification;
- interpretation;
- source traceability;
- provenance;
- lifecycle handling;
- authority handling;
- privacy handling;
- validation;
- review;
- routing;
- compatibility;
- future maintenance.

Metadata proposals MAY include or support:

- proposed title or label;
- proposed type or category where applicable;
- temporary identifier;
- source context;
- provenance context;
- lifecycle recommendation;
- authority concern;
- privacy concern;
- validation state or validation finding;
- review status;
- routing state;
- duplicate concern;
- relationship cue;
- Source Reference cue;
- maintenance concern.

Metadata proposals MUST remain distinguishable from approved metadata.

An agent-generated metadata proposal MUST be traceable as agent-generated where the proposal affects meaning, routing, privacy, authority, validation, review, publication, export, migration, or downstream use.

Metadata proposals MUST NOT override Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, Source References, provenance, relationships, approval, publication readiness, export readiness, migration readiness, or downstream-use readiness by themselves.

### 8.2 Relationship Proposal Steps

Controlled ingestion MAY propose relationships when Source Material, extracted content, Draft Knowledge Records, metadata, provenance, or review context suggests a meaningful connection.

Relationship proposals MAY connect:

- Draft Knowledge Records;
- existing Knowledge Records;
- Knowledge Objects;
- Source Material;
- Source References;
- provenance records;
- standards;
- specifications;
- workflows;
- agents;
- decisions;
- implementation artifacts;
- validation results;
- maintenance concerns;
- other governed entities.

A relationship proposal SHOULD identify or support identification of:

- origin participant;
- target participant;
- proposed relationship type where known;
- direction where direction affects meaning;
- relationship context;
- source support;
- provenance support;
- confidence or uncertainty where relevant;
- privacy concern where relevant;
- authority concern where relevant;
- validation concern where relevant;
- review requirement.

A relationship proposal MUST remain distinguishable from an approved relationship.

A proposed relationship MUST NOT be treated as approved merely because it appears in a graph, backlink list, folder structure, tag list, search result, embedding result, agent output, subagent output, workflow output, or implementation interface.

An agent or subagent MAY propose relationships.

An agent or subagent MUST NOT silently approve relationships where relationship meaning affects governed interpretation, provenance, authority, privacy, validation, publication, export, migration, or downstream use.

### 8.3 Source Reference Proposal Steps

Controlled ingestion SHOULD propose Source References when Source Material supports, explains, contextualizes, contradicts, originates, or otherwise relates to a Draft Knowledge Record, relationship proposal, metadata proposal, validation result, review note, or workflow output.

A Source Reference proposal SHOULD identify or support identification of:

- referenced Source Material;
- source location or reference where available;
- source origin where known;
- source availability status where relevant;
- source reliability concern where known;
- source authority concern where known;
- source privacy concern where known;
- supported draft content or claim where applicable;
- extraction or transformation context;
- provenance context;
- uncertainty or limitation;
- review requirement.

A Source Reference proposal MUST remain distinguishable from an approved Source Reference.

A citation, link, file path, bookmark, attachment, note title, folder location, search result, or implementation-specific pointer MAY support a Source Reference proposal.

It does not define Source Reference validity by itself.

A Source Reference proposal SHOULD preserve enough information for future review even if the Source Material is moved, renamed, restricted, archived, exported, imported, migrated, unavailable, or represented differently by an implementation.

Where Source Material is unavailable, restricted, incomplete, or uncertain, the Source Reference proposal SHOULD state that limitation.

A missing or uncertain Source Reference MUST NOT be hidden by confident draft language.

### 8.4 Proposal Review Boundaries

Metadata, relationship, and Source Reference proposals MUST remain reviewable.

A future human, agent, workflow, validator, storage system, migration process, import process, export process, or implementation SHOULD be able to determine:

- what was proposed;
- who or what proposed it where applicable;
- what Source Material supports it;
- what provenance supports it;
- what uncertainty applies;
- what validation issue applies;
- what privacy issue applies;
- what authority issue applies;
- whether it requires review, repair, rejection, quarantine, archive, maintenance, or escalation.

A proposal MUST NOT become final merely because:

- it passes formatting checks;
- it passes partial validation;
- it is generated by an agent;
- it is generated by a subagent;
- it appears useful;
- it is linked;
- it is indexed;
- it is stored in the expected location;
- it appears in a template;
- it appears in an implementation interface;
- it is repeated by a workflow.

Where a proposal affects governed meaning, review is required before final acceptance unless a future governed specification explicitly defines limited automatic acceptance.

### 8.5 Proposal Outputs

The proposal stage SHOULD produce reviewable outputs.

Proposal outputs MAY include:

- metadata proposal;
- relationship proposal;
- Source Reference proposal;
- provenance support note;
- source support note;
- source limitation note;
- uncertainty note;
- duplicate or identity concern;
- privacy concern;
- authority concern;
- validation concern;
- review question;
- repair recommendation;
- routing recommendation;
- escalation recommendation.

Proposal outputs SHOULD be structured enough to support validation and review.

Proposal outputs SHOULD avoid unnecessary complexity where the material is simple, low-risk, low-authority, and not intended for downstream use.

Proposal outputs MUST preserve the distinction between proposed, reviewed, approved, rejected, repaired, quarantined, archived, superseded, deprecated, and escalated states where those distinctions affect interpretation or handling.

## 9. Validation and Review Preparation

The purpose of this section is to define how controlled ingestion validates ingestion outputs and prepares them for review.

Validation checks whether ingestion outputs satisfy applicable requirements.

Review preparation makes ingestion outputs understandable, inspectable, correctable, and routable.

Validation does not equal approval.

Review preparation does not equal approval.

A validation-passing Draft Knowledge Record, metadata proposal, relationship proposal, Source Reference proposal, extraction output, or review packet MUST NOT be treated as approved merely because it passed validation.

### 9.1 Validation Scope

Controlled ingestion SHOULD define or identify the validation scope before validation begins.

Validation scope MAY include:

- structural validation;
- identity validation;
- metadata validation;
- relationship validation;
- Source Reference validation;
- provenance validation;
- lifecycle validation;
- authority validation;
- privacy validation;
- compatibility validation;
- workflow validation;
- agent-output validation;
- subagent-output validation;
- storage-layout validation;
- implementation-boundary validation;
- review-readiness validation.

Validation scope SHOULD be appropriate to the material.

Low-risk, low-authority, temporary, or archival material MAY require lighter validation.

Material affecting governed meaning, authority, privacy, publication, export, migration, or downstream use SHOULD require stronger validation.

Validation MUST NOT silently ignore required checks where missing validation could cause identity confusion, source confusion, provenance loss, relationship confusion, authority confusion, privacy exposure, compatibility loss, workflow error, or governance drift.

### 9.2 Validation Checks

Controlled ingestion SHOULD validate whether ingestion outputs are complete enough for the next workflow stage.

Validation checks MAY ask whether:

- Source Material is preserved or limitation is recorded;
- intake context is recorded where required;
- material type is identified or marked unknown;
- privacy risk is identified;
- authority risk is identified;
- provenance is captured or limitation is recorded;
- extraction method is clear where relevant;
- extracted content remains distinguishable from interpretation;
- Draft Knowledge Record is marked as draft;
- temporary identifiers remain distinguishable from stable Object Identity;
- metadata proposals are marked as proposals;
- relationship proposals are marked as proposals;
- Source Reference proposals are marked as proposals;
- validation findings are recorded;
- stop conditions are identified;
- routing recommendation is present;
- review questions are clear.

Validation SHOULD distinguish between errors and warnings.

A validation error indicates that a mandatory requirement is not satisfied within the applicable scope.

A validation warning indicates a risk, incompleteness, ambiguity, or recommended improvement that may not invalidate the output by itself.

Validation results SHOULD be recorded in a reviewable form.

### 9.3 Review Preparation Requirements

Controlled ingestion SHOULD prepare review outputs so that a reviewer can quickly determine what happened and what decision is needed.

Review preparation SHOULD include or support:

- intake summary;
- Source Material reference;
- material type classification;
- knowledge value assessment;
- privacy-risk note;
- authority-risk note;
- provenance summary;
- extraction summary;
- Draft Knowledge Record where created;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- validation results;
- stop condition notes;
- unresolved questions;
- recommended routing;
- required reviewer action.

Review preparation SHOULD make unresolved issues explicit.

Review preparation MUST NOT hide missing source support, missing provenance, identity uncertainty, privacy risk, authority risk, validation failure, duplicate concern, relationship uncertainty, Source Reference uncertainty, or stop conditions.

Review preparation SHOULD avoid forcing the reviewer to infer workflow state from folder placement, filenames, tags, graph position, search results, hidden application state, agent memory, workflow memory, or implementation-specific interface behavior.

### 9.4 Review Packet

Controlled ingestion MAY produce a Review Packet when ingestion output requires human review, governed review, approval, repair, rejection, quarantine, archive, maintenance routing, or escalation.

A Review Packet MAY include:

- intake record;
- preserved Source Material reference;
- inspection and classification output;
- extraction output;
- provenance output;
- Draft Knowledge Record;
- metadata proposal;
- relationship proposal;
- Source Reference proposal;
- validation result;
- risk notes;
- stop condition notes;
- reviewer questions;
- recommended decision;
- routing recommendation.

A Review Packet SHOULD be concise enough to support practical review.

A Review Packet SHOULD be complete enough to prevent hidden assumptions.

A Review Packet MUST remain distinguishable from approval.

A Review Packet organizes review.

It does not make the reviewed material approved.

### 9.5 Validation and Review Preparation Outputs

The validation and review preparation stage SHOULD produce outputs that support the next workflow decision.

Outputs MAY include:

- validation result;
- validation error list;
- validation warning list;
- review packet;
- review note;
- repair request;
- quarantine recommendation;
- archive recommendation;
- rejection recommendation;
- maintenance recommendation;
- escalation recommendation;
- approval-readiness recommendation;
- downstream workflow recommendation.

An approval-readiness recommendation is not approval.

A routing recommendation is not approval.

A validation result is not approval.

A reviewer note is not approval unless the applicable review-and-approval workflow records approval within its defined scope.

Validation and review preparation outputs SHOULD route to the next appropriate stage under Section 10.

## 10. Routing, Escalation, and Stop Conditions

The purpose of this section is to define how controlled ingestion routes ingestion candidates, Draft Knowledge Records, workflow outputs, validation findings, review packets, and stop conditions after validation and review preparation.

Routing determines the next appropriate workflow path.

Routing does not create approval by itself.

A routing decision or routing recommendation MUST remain distinguishable from approval, rejection, publication readiness, export readiness, migration readiness, downstream-use readiness, deletion, supersession, deprecation, or final lifecycle transition unless a higher-authority workflow or specification explicitly defines that behavior.

### 10.1 Routing Principles

Controlled ingestion SHOULD route each ingestion candidate or workflow output to the safest and most useful next state.

Routing SHOULD preserve:

- Source Material distinction;
- Draft Knowledge Record distinction;
- Object Identity boundaries;
- metadata proposal boundaries;
- relationship proposal boundaries;
- Source Reference proposal boundaries;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- reviewability;
- implementation independence;
- traceability.

Routing MUST NOT depend only on folder placement, filename, tag, color, graph location, search result, hidden application state, workflow memory, agent memory, plugin behavior, implementation label, or automation status where the routing decision affects governed meaning or handling.

A routing decision SHOULD be reviewable where it affects approval, rejection, repair, quarantine, archive, maintenance, escalation, publication, export, migration, deletion, supersession, deprecation, or downstream use.

### 10.2 Standard Routing Outcomes

Controlled ingestion MAY route ingestion candidates or workflow outputs to one or more of the following outcomes:

- continue ingestion;
- create or revise Draft Knowledge Record;
- propose metadata;
- propose relationships;
- propose Source References;
- run validation;
- prepare review;
- route to human review;
- route to governed review;
- route to repair;
- route to privacy review;
- route to authority review;
- route to source review;
- route to identity review;
- route to relationship review;
- route to maintenance workflow;
- route to quarantine;
- route to archive;
- route to rejection;
- route to escalation;
- defer until required information is available.

A routing outcome MAY be provisional.

A provisional routing outcome SHOULD indicate what condition must be resolved before further processing.

Examples of conditions MAY include:

- missing provenance;
- missing Source Material;
- unclear source origin;
- unresolved privacy risk;
- unresolved authority risk;
- duplicate concern;
- identity ambiguity;
- validation failure;
- relationship uncertainty;
- unsupported format;
- corrupted material;
- unclear review scope;
- insufficient human context.

### 10.3 Review Routing

Controlled ingestion SHOULD route material to review when human judgment, governed workflow judgment, privacy review, authority review, source review, validation review, relationship review, identity review, publication review, export review, migration review, or downstream-use review is required.

Review routing SHOULD occur when:

- a Draft Knowledge Record is ready for review;
- metadata proposals require acceptance or correction;
- relationship proposals require acceptance or correction;
- Source Reference proposals require acceptance or correction;
- validation findings require interpretation;
- privacy handling is uncertain;
- authority handling is uncertain;
- source support is unclear;
- provenance is incomplete;
- Object Identity is unresolved;
- duplicate, merge, split, derivative, supersession, or deprecation concerns exist;
- a stop condition blocks normal ingestion.

Review routing MUST identify or support identification of the review need.

Review routing SHOULD include enough context for the reviewer to determine what action is required.

Review routing MUST NOT imply approval merely because material was routed to a review area, review queue, review folder, review label, review dashboard, or review packet.

### 10.4 Repair Routing

Controlled ingestion SHOULD route material to repair when issues can likely be corrected without rejecting or quarantining the material.

Repair routing MAY apply when:

- required metadata is missing;
- source context is incomplete;
- provenance is incomplete;
- extracted content is unclear;
- Draft Knowledge Record structure is incomplete;
- relationship proposal is malformed;
- Source Reference proposal is incomplete;
- validation warning requires correction;
- validation error is correctable;
- formatting prevents review;
- temporary identifier handling is unclear;
- routing state is ambiguous;
- review packet is incomplete.

Repair routing SHOULD identify:

- what issue requires repair;
- what standard, specification, template, or workflow expectation is affected where known;
- what material is affected;
- what correction is recommended;
- whether human review is required after repair.

Repair routing MUST NOT silently modify governed meaning where the repair affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, supersession, deprecation, or downstream use.

### 10.5 Quarantine Routing

Controlled ingestion MUST route material to quarantine when normal processing could create unresolved privacy, safety, validity, source, provenance, compatibility, authority, implementation, agent-access, publication, export, migration, or downstream-use risk.

Quarantine routing MAY apply when:

- privacy-sensitive material lacks clear handling permission;
- restricted material may be exposed improperly;
- source origin is unknown and required;
- provenance is missing where required;
- material appears corrupted, unsafe, or unreliable;
- material appears malicious or dangerous to process;
- material contains credentials or secrets;
- material contains legal, financial, health, or confidential information requiring special handling;
- authority risk is unresolved;
- validation failure blocks safe use;
- implementation exposure risk is unresolved;
- publication, export, synchronization, indexing, backup, migration, or downstream-use risk is unresolved.

Quarantine does not reject the material by itself.

Quarantine isolates or restricts material until review, repair, redaction, restriction, archive, rejection, escalation, or governed routing occurs.

A quarantined item SHOULD preserve enough information for future review without unnecessarily exposing restricted content.

Agents and subagents SHOULD NOT process quarantined material unless explicitly authorized within the applicable privacy, authority, workflow, and implementation scope.

### 10.6 Archive and Rejection Routing

Controlled ingestion MAY route material to archive when it should be preserved but not actively converted into governed knowledge at the current time.

Archive routing MAY apply when material:

- has historical value;
- has evidentiary value;
- supports future review;
- supports provenance;
- is low-priority but potentially useful;
- is outside current ingestion scope but worth preserving;
- is superseded or duplicated but still useful for traceability;
- cannot currently be processed but should not be discarded.

Controlled ingestion MAY route material to rejection when it should not proceed through the intended ingestion path.

Rejection routing MAY apply when material is:

- irrelevant;
- out of scope;
- unusable;
- unsupported;
- unsafe;
- duplicate without preservation need;
- not permitted for use;
- lacking necessary source permission;
- not worth preserving under the current workflow;
- unsuitable for Draft Knowledge Record creation.

Rejection does not necessarily mean deletion.

Deletion is a separate governed action and MUST NOT occur merely because material was rejected during ingestion.

Rejected material MAY still require preservation, privacy protection, provenance notes, review notes, or archive routing.

### 10.7 Maintenance Routing

Controlled ingestion SHOULD route material to maintenance when incoming material appears to affect existing governed knowledge.

Maintenance routing MAY apply when incoming material:

- updates an existing Knowledge Record;
- corrects an existing Knowledge Record;
- contradicts existing knowledge;
- identifies stale knowledge;
- identifies broken Source References;
- identifies missing provenance;
- identifies relationship changes;
- identifies privacy reclassification needs;
- identifies authority reassessment needs;
- identifies validation failure in existing records;
- identifies supersession, deprecation, archival, or reapproval needs.

Maintenance routing MUST preserve the distinction between new ingestion and maintenance of existing governed entities.

An ingestion workflow MAY identify a maintenance need.

It does not complete maintenance unless the applicable maintenance workflow authorizes that action.

### 10.8 Escalation Requirements

Controlled ingestion MUST escalate issues that cannot be safely resolved within the current authorized scope.

Escalation SHOULD occur when:

- privacy risk cannot be resolved;
- authority risk cannot be resolved;
- source origin is required but unknown;
- provenance is required but missing;
- Object Identity cannot be safely determined;
- duplicate, merge, split, derivative, supersession, or deprecation concerns require governed judgment;
- validation failure blocks review or safe routing;
- material may require deletion or destructive overwrite;
- material may require publication, export, migration, synchronization, indexing, backup, or downstream-use review;
- agent or subagent output conflicts with a higher-authority standard;
- workflow output conflicts with a higher-authority standard;
- implementation behavior conflicts with governed meaning;
- the ingestion actor lacks permission to continue.

Escalation SHOULD identify:

- the affected material;
- the unresolved issue;
- the risk category;
- the applicable standard, specification, workflow, or boundary where known;
- the recommended reviewer or workflow;
- whether normal processing is stopped;
- whether quarantine is required;
- whether repair is possible;
- whether rejection or archive is recommended.

Escalation MUST NOT be bypassed merely because automation can continue.

### 10.9 Routing Outputs

The routing stage SHOULD produce reviewable outputs.

Routing outputs MAY include:

- routing decision;
- routing recommendation;
- stop condition note;
- review request;
- repair request;
- quarantine note;
- archive recommendation;
- rejection recommendation;
- maintenance routing note;
- escalation note;
- approval-readiness recommendation;
- unresolved issue list;
- required next action.

Routing outputs SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations to determine why the route was selected.

Routing outputs MUST remain distinguishable from approval.

WF-SPEC-0001 is successful only when routing keeps controlled ingestion safe, reviewable, traceable, and subordinate to governed review.

## 11. Controlled Ingestion Runbook Template

The purpose of this section is to provide a reusable controlled-ingestion runbook template that can be copied, filled out, adapted, or implemented without changing the standard-level meaning of WF-SPEC-0001.

The template is an operational aid.

The template does not replace the requirements of WF-SPEC-0001 or higher-authority standards.

A compliant implementation MAY use this template directly, adapt it into another Markdown format, convert it into a form, implement it as a database record, implement it as a workflow checklist, implement it as an agent instruction packet, or represent it through a future implementation.

The representation may change.

The governed meaning MUST remain consistent with WF-SPEC-0001.

### 11.1 Template Use Rules

The controlled-ingestion runbook template SHOULD be used when intake material requires reviewable handling.

The template MAY be shortened for low-risk, low-authority, temporary, or simple material.

The template SHOULD be completed more fully when material affects:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- publication;
- export;
- migration;
- deletion;
- supersession;
- deprecation;
- downstream use.

Template fields MAY be marked unknown, not applicable, pending, restricted, unavailable, or requires review where appropriate.

Unknown fields SHOULD NOT be silently filled by assumption.

Agent-generated, subagent-generated, workflow-generated, implementation-generated, and human-created entries SHOULD remain distinguishable where the distinction affects meaning, review, privacy, authority, validation, or downstream use.

### 11.2 Template

```markdown
# Controlled Ingestion Runbook Entry

Runbook Entry ID:
Related Intake Item:
Related Source Material:
Temporary Identifier:
Date Created:
Created By:
Agent or Subagent Involved:
Workflow Scope:
Current Routing State:

## 1. Intake Summary

Intake Title or Label:
Material Received:
Material Type:
File Format or Representation:
Source Origin:
Source Provider, Creator, Sender, or Publisher:
Intake Location:
Preserved Source Material Location:
Initial Handling Restriction:
Initial Notes:

## 2. Source Material Handling

Source Material Preserved:
Preservation Method:
Source Availability:
Source Completeness:
Known Source Limitation:
Restricted Source Concern:
Original Material Modified:
If Modified, Explain:
Source Material Distinguishable from Draft Output:

## 3. Initial Inspection

Readable:
Complete:
Supported Format:
Duplicate Concern:
Existing Knowledge Record Concern:
Existing Knowledge Object Concern:
Material Appears To Be:
Inspection Notes:

## 4. Classification

Proposed Material Type:
Proposed Content Type:
Potential Knowledge Value:
Draft Knowledge Record Suitable:
Source-Only Archive Suitable:
Rejection Candidate:
Quarantine Candidate:
Maintenance Candidate:
Classification Confidence or Uncertainty:

## 5. Privacy and Authority Risk

Privacy Risk Detected:
Privacy Risk Description:
Recommended Privacy Handling:
Authority Risk Detected:
Authority Risk Description:
Recommended Authority Handling:
Agent Access Concern:
Implementation Exposure Concern:

## 6. Extraction and Provenance

Extraction Performed:
Extraction Method:
Extracted Content Location:
Extraction Actor:
Agent or Subagent Participation:
Direct Source Content Used:
Summary or Interpretation Used:
Transformation Performed:
Provenance Captured:
Provenance Limitation:
Source Reliability Concern:
Source Authority Concern:
Source Privacy Concern:

## 7. Draft Knowledge Record

Draft Created:
Draft Location:
Draft Title:
Temporary Identifier:
Proposed Knowledge Object Status:
Existing Knowledge Object Candidate:
Duplicate, Merge, Split, Derivative, or Supersession Concern:
Draft Content Notes:
Draft Limitations:

## 8. Metadata Proposal

Metadata Proposed:
Proposed Title or Label:
Proposed Type or Category:
Proposed Lifecycle Handling:
Proposed Authority Handling:
Proposed Privacy Handling:
Validation Metadata:
Routing Metadata:
Metadata Uncertainty:

## 9. Relationship Proposal

Relationship Proposed:
Origin Participant:
Target Participant:
Proposed Relationship Type:
Direction Required:
Relationship Context:
Source Support:
Relationship Uncertainty:
Relationship Review Required:

## 10. Source Reference Proposal

Source Reference Proposed:
Referenced Source Material:
Supported Draft Content or Claim:
Source Location or Reference:
Source Availability:
Source Limitation:
Source Reference Review Required:

## 11. Validation

Validation Scope:
Validation Performed:
Validation Errors:
Validation Warnings:
Review-Readiness:
Required Repair:
Required Revalidation:

## 12. Review Preparation

Review Packet Created:
Reviewer Needed:
Review Questions:
Required Reviewer Action:
Approval-Readiness Recommendation:
Unresolved Issues:

## 13. Routing

Recommended Route:
Routing Reason:
Stop Condition Present:
Repair Required:
Quarantine Required:
Archive Recommended:
Rejection Recommended:
Maintenance Routing Recommended:
Escalation Required:
Next Required Action:

## 14. Final Ingestion Notes

What Was Completed:
What Was Not Completed:
What Requires Review:
What Requires Repair:
What Requires Escalation:
Do Not Treat As Approved Until:
Additional Notes:
```

### 11.3 Template Output Expectations

A completed controlled-ingestion runbook entry SHOULD make the ingestion state reviewable.

A completed entry SHOULD allow a future human, agent, subagent, workflow, validator, storage system, migration process, import process, export process, or implementation to determine:

- what material entered ingestion;
- how Source Material was handled;
- what inspection found;
- what classification was proposed;
- what privacy or authority risks exist;
- what extraction occurred;
- what provenance was captured;
- what Draft Knowledge Record was created where applicable;
- what metadata was proposed;
- what relationships were proposed;
- what Source References were proposed;
- what validation found;
- what review preparation occurred;
- what routing was recommended;
- what remains unresolved.

A completed template MUST NOT be treated as approval by itself.

A completed template supports review.

It does not replace review.

### 11.4 Template Adaptation Rules

Implementations MAY adapt the template for practical use.

Adaptations MAY include:

- shorter checklists;
- forms;
- tables;
- front matter;
- database fields;
- issue templates;
- pull request templates;
- workflow cards;
- agent task packets;
- subagent task packets;
- validation reports;
- review packets;
- implementation-specific dashboards.

Adaptations MUST preserve the meaning of required controlled-ingestion concepts.

Adaptations MUST NOT remove reviewability where reviewability affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, supersession, deprecation, or downstream use.

Adaptations MUST NOT make implementation-specific fields, folders, labels, tags, dashboards, scripts, forms, prompts, or tools the standard.

## 12. Controlled Ingestion Success Criteria

The purpose of this section is to define the success criteria for WF-SPEC-0001.

WF-SPEC-0001 is successful when controlled ingestion reliably moves incoming material from raw intake into reviewable workflow outputs without allowing raw information, storage placement, automation, agent output, validation output, or workflow completion to become hidden authority.

Success criteria apply to the runbook itself and to implementations that use the runbook.

### 12.1 File-Level Success Criteria

WF-SPEC-0001 satisfies its file-level purpose when it:

- defines controlled ingestion as a practical runbook;
- remains subordinate to higher-authority standards;
- extends WF-0001 without replacing it;
- preserves implementation independence;
- preserves Source Material distinction;
- preserves Draft Knowledge Record distinction;
- preserves Object Identity boundaries;
- preserves metadata proposal boundaries;
- preserves relationship proposal boundaries;
- preserves Source Reference proposal boundaries;
- preserves provenance expectations;
- preserves Lifecycle State boundaries;
- preserves Authority Level boundaries;
- preserves Privacy Classification boundaries;
- preserves Validation boundaries;
- preserves agent and subagent operating boundaries;
- defines intake handling;
- defines inspection and classification;
- defines extraction and provenance capture;
- defines Draft Knowledge Record creation;
- defines proposal steps;
- defines validation and review preparation;
- defines routing and escalation;
- provides a reusable runbook template;
- defines success criteria.

### 12.2 Controlled Ingestion Outcome Criteria

A controlled ingestion run is successful when it produces a reviewable outcome appropriate to the material.

A successful controlled ingestion run SHOULD determine or record:

- what material was received;
- whether Source Material was preserved;
- what source context is known;
- what provenance was captured;
- what privacy risk exists;
- what authority risk exists;
- what classification was proposed;
- what extraction occurred;
- whether a Draft Knowledge Record was created;
- what metadata was proposed;
- what relationships were proposed;
- what Source References were proposed;
- what validation found;
- what review output was prepared;
- what route was recommended;
- what unresolved issues remain.

A successful controlled ingestion run does not require every material item to become a Draft Knowledge Record.

A successful controlled ingestion run MAY result in review, repair, quarantine, archive, rejection, maintenance routing, escalation, or deferred action.

A successful controlled ingestion run MUST preserve the ability to understand why that outcome occurred.

### 12.3 Governance Success Criteria

Controlled ingestion satisfies governance expectations when it prevents workflow convenience from becoming authority.

Governance success requires that:

- Source Material does not become governed knowledge merely because it was ingested;
- Draft Knowledge Records do not become approved Knowledge Records merely because they were created;
- metadata proposals do not become approved metadata merely because they were proposed;
- relationship proposals do not become approved relationships merely because they were proposed;
- Source Reference proposals do not become approved Source References merely because they were proposed;
- validation results do not become approval merely because they passed;
- review packets do not become approval merely because they are complete;
- routing recommendations do not become approval merely because they are useful;
- agent output does not become authority merely because it is confident;
- subagent output does not become authority merely because it is specialized;
- implementation behavior does not become the standard merely because it is convenient;
- storage placement does not define meaning merely because it is organized.

Controlled ingestion MUST preserve human or governed review wherever review is required by the applicable standards, workflows, specifications, privacy expectations, authority expectations, validation expectations, or downstream-use conditions.

### 12.4 Agent and Subagent Success Criteria

Agent-assisted or subagent-assisted controlled ingestion is successful when agents reduce workload without expanding their authority beyond the authorized scope.

Agent and subagent success requires that:

- agent actions remain within AG-0001 boundaries;
- subagent actions remain within AG-SPEC-0002 role boundaries;
- agent and subagent outputs remain traceable where needed;
- agent and subagent uncertainty is preserved where relevant;
- agent and subagent recommendations remain distinguishable from approval;
- agents and subagents do not silently assign final Object Identity;
- agents and subagents do not silently assign final Authority Level;
- agents and subagents do not silently assign final Privacy Classification;
- agents and subagents do not silently approve metadata, relationships, Source References, or provenance;
- agents and subagents do not silently publish, export, migrate, delete, merge, split, supersede, deprecate, or override governance.

Agent and subagent assistance is successful when it improves intake, classification, extraction, drafting, proposal creation, validation, review preparation, and routing while preserving reviewability.

### 12.5 Implementation Success Criteria

An implementation of WF-SPEC-0001 is successful when it realizes the runbook without redefining the standard.

Implementation success requires that:

- the runbook can be performed through the chosen tool or environment;
- Source Material remains distinguishable from Knowledge Records;
- Draft Knowledge Records remain distinguishable from approved Knowledge Records;
- proposals remain distinguishable from approved governed entities;
- validation remains distinguishable from approval;
- routing remains distinguishable from approval;
- privacy risks can be identified and routed;
- authority risks can be identified and routed;
- stop conditions can halt normal processing;
- review outputs can be inspected;
- provenance can be preserved;
- storage placement supports workflow without defining meaning;
- implementation-specific behavior remains subordinate to the standard.

A compliant implementation MAY use folders, files, repositories, databases, note-taking tools, forms, scripts, agents, subagents, validators, workflow systems, dashboards, or future software.

The implementation method does not define WF-SPEC-0001.

### 12.6 Completion Criteria

WF-SPEC-0001 is complete when it can guide a controlled ingestion run from raw material intake through review preparation and routing.

WF-SPEC-0001 does not complete the full review-and-approval workflow.

WF-SPEC-0001 does not complete maintenance.

WF-SPEC-0001 does not complete publication, export, migration, synchronization, indexing, backup, or downstream-use approval.

Those actions belong to their respective standards, workflows, specifications, implementation documents, and governed review processes.

WF-SPEC-0001 is complete when future humans, agents, subagents, workflows, validators, storage systems, and implementations can use it to determine:

- how to receive material;
- how to preserve Source Material;
- how to inspect and classify incoming material;
- how to extract content;
- how to capture provenance;
- how to create Draft Knowledge Records;
- how to propose metadata;
- how to propose relationships;
- how to propose Source References;
- how to validate ingestion outputs;
- how to prepare review;
- how to route outcomes;
- when to stop;
- when to repair;
- when to quarantine;
- when to archive;
- when to reject;
- when to maintain;
- when to escalate.
