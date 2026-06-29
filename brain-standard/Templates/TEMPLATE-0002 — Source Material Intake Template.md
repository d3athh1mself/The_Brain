# TEMPLATE-0002 — Source Material Intake Template

Document ID: TEMPLATE-0002
Title: Source Material Intake Template
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Operational Template
Phase: Bare Usable Deployment Support
Milestone: Template Set — Source Material Intake
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; SC-0001 — Knowledge Record Metadata Field Specification; TEMPLATE-0001 — Knowledge Record Template
Supersedes: None
Superseded By: None
Related: TEMPLATE-0003 — Agent Activity Record Template; TEMPLATE-0004 — Review Record Template; WF-SPEC-0001 — Controlled Ingestion Runbook

## 1. Purpose

The purpose of TEMPLATE-0002 is to provide a copy/paste-ready Source Material Intake structure for The Brain Standard.

This template is used to register, stage, describe, classify, and prepare Source Material before that material is transformed into one or more Knowledge Records.

TEMPLATE-0002 exists so that raw files, documents, notes, messages, images, recordings, datasets, scans, transcripts, web captures, or other source artifacts do not become governed knowledge merely because they were saved, summarized, indexed, processed by an agent, or placed in a folder.

This template supports the controlled intake process by helping humans, agents, workflows, validators, and implementations answer:

- what the Source Material is;
- where the Source Material came from;
- why the Source Material was captured;
- what type of material it appears to be;
- what privacy concerns may apply;
- what provenance is known;
- what extraction or transformation may be required;
- what Knowledge Records may be created from it;
- what agent assistance occurred;
- what review is required before ingestion, transformation, approval, export, publication, or downstream use.

TEMPLATE-0002 does not replace TEMPLATE-0001 — Knowledge Record Template.

TEMPLATE-0002 feeds TEMPLATE-0001.

A completed Source Material Intake Record may support creation of one Knowledge Record, many Knowledge Records, no Knowledge Records, a deferred intake decision, a rejection decision, a quarantine decision, an archive action, a review record, or a future controlled ingestion workflow output.

TEMPLATE-0002 is successful when Source Material can be understood, staged, traced, reviewed, classified, validated, and transformed without losing the distinction between raw Source Material and governed Knowledge Records.

## 2. Relationship to Prior Standards and Templates

TEMPLATE-0002 is an operational template.

It does not define new standards, new metadata fields, new privacy classes, new lifecycle states, new authority levels, new validation states, new relationship rules, new agent permissions, or new workflow authority.

Where this template appears to conflict with a higher-authority document, the higher-authority document governs.

TEMPLATE-0002 depends on the constitutional foundation of The Brain Standard because Source Material intake must remain implementation-independent, human-readable, AI-readable, portable, governed, and reviewable.

TEMPLATE-0002 depends on the Knowledge Standards because Source Material intake must preserve the distinction between:

- Source Material and Knowledge Records;
- source identifiers and Object Identity;
- source description and metadata;
- Source References and provenance;
- proposed relationships and approved relationships;
- lifecycle state and approval;
- authority level and source reliability;
- privacy classification and storage location;
- validation and review;
- agent assistance and agent authority.

TEMPLATE-0002 depends on the Storage Standards because intake material may be staged, moved, archived, quarantined, reviewed, exported, or migrated without allowing folder placement, filename, or storage location to define knowledge meaning.

TEMPLATE-0002 depends on AG-0001 because agents may assist intake only within governed operating boundaries.

Agents may inspect, summarize, classify, extract, validate, propose metadata, propose Source References, propose relationships, and draft outputs where authorized.

Agents must not independently approve Source Material, assign final authority, override privacy classification, delete material, publish material, export restricted material, or convert Source Material into approved Knowledge Records without the required review path.

TEMPLATE-0002 depends on WF-0001 because intake is the first controlled stage of knowledge ingestion.

TEMPLATE-0002 depends on WF-0002 because intake outputs may require human review, correction, approval, rejection, repair, escalation, quarantine, or archival routing.

TEMPLATE-0002 depends on SC-0001 only when intake outputs are used to create or support a Knowledge Record.

TEMPLATE-0002 does not rename, replace, reinterpret, or redefine the Knowledge Record metadata fields governed by SC-0001.

TEMPLATE-0002 relates to TEMPLATE-0001 as follows:

- TEMPLATE-0002 records and prepares Source Material.
- TEMPLATE-0001 records governed knowledge created from, about, or in response to Source Material.
- TEMPLATE-0002 may identify candidate Knowledge Records.
- TEMPLATE-0001 is used only when a Knowledge Record is actually drafted or created.

TEMPLATE-0002 relates to TEMPLATE-0003 as follows:

- TEMPLATE-0002 may summarize agent assistance during intake.
- TEMPLATE-0003 is used when detailed agent activity must be recorded.
- TEMPLATE-0002 must not replace a required Agent Activity Record.

TEMPLATE-0002 relates to TEMPLATE-0004 as follows:

- TEMPLATE-0002 may identify review needs.
- TEMPLATE-0004 is used when a formal review decision, approval, rejection, repair request, or escalation must be recorded.
- TEMPLATE-0002 must not replace a required Review Record.

## 3. Template Scope and Use Rules

TEMPLATE-0002 applies to Source Material before, during, or immediately after intake.

This template may be used for:

- a single file;
- a grouped source package;
- a copied excerpt;
- a transcript;
- a scanned document;
- a captured web page;
- a dataset;
- an image or media file;
- a message thread;
- a note dump;
- a research item;
- a project artifact;
- an imported external reference;
- another source artifact that may support future Knowledge Records.

When multiple files are handled together, the intake record should clearly state whether the record describes:

- one source artifact;
- a source bundle;
- a folder of related source artifacts;
- an import batch;
- a staged collection awaiting later separation.

TEMPLATE-0002 should be used when Source Material needs to be understood before transformation.

TEMPLATE-0002 should not be used as a substitute for a Knowledge Record.

TEMPLATE-0002 should not be used as a substitute for a Source Reference standard.

TEMPLATE-0002 should not be used as a substitute for a provenance standard.

TEMPLATE-0002 should not be used as a substitute for an Agent Activity Record.

TEMPLATE-0002 should not be used as a substitute for a Review Record.

TEMPLATE-0002 should not be used as an approval record.

TEMPLATE-0002 should not be used as a publication, export, migration, or downstream-use authorization record.

TEMPLATE-0002 may include proposed classifications, proposed extraction plans, proposed Knowledge Records, proposed relationships, proposed privacy concerns, and proposed review needs.

Proposed values remain proposed until reviewed or accepted through the applicable workflow.

A completed intake record does not mean the Source Material is approved.

A completed intake record does not mean extracted knowledge is approved.

A completed intake record does not mean privacy review is complete.

A completed intake record does not mean validation is complete.

A completed intake record does not mean publication, export, migration, indexing, synchronization, or downstream use is permitted.

Humans may complete this template manually.

Agents may assist with this template only within authorized boundaries.

When an agent assists with intake, the intake record should identify:

- what the agent inspected;
- what the agent proposed;
- what uncertainty remains;
- what review is required;
- whether a separate Agent Activity Record is needed.

Unknown values should be marked clearly rather than guessed.

Recommended placeholder values include:

- Unknown
- Not yet reviewed
- Not applicable
- Pending human review
- Pending validation
- Pending privacy review
- Pending source review
- Pending provenance review
- Pending relationship review

The intake record should preserve uncertainty rather than hide it.

The intake record should preserve privacy concerns rather than normalize them away.

The intake record should preserve source limitations rather than overstate reliability.

The intake record should preserve the boundary between source description, extracted knowledge, and governed Knowledge Records.

TEMPLATE-0002 is within scope when the goal is to prepare Source Material for controlled ingestion.

TEMPLATE-0002 is out of scope when the goal is to approve knowledge, publish knowledge, export knowledge, perform final review, record detailed agent behavior, or define new standards.
## 4. Source Material Intake Metadata Block

The following metadata block provides a practical intake structure for Source Material.

This block is for Source Material intake only.

It is not a Knowledge Record metadata block.

It does not replace SC-0001.

It does not define Object Identity for a Knowledge Object.

It does not approve Source Material for governed use.

It does not approve extracted knowledge.

It does not authorize publication, export, migration, synchronization, indexing, or downstream use.

Copy and complete the block below when registering Source Material for intake.

```yaml
intake_id: ""
intake_title: ""
intake_status: "Draft"
source_material_id: ""
source_title: ""
source_type: ""
source_format: ""
source_location: ""
source_origin: ""
source_creator: ""
source_capture_method: ""
captured_by: ""
captured: ""
intake_created: ""
intake_updated: ""
privacy_classification: "Pending privacy review"
source_availability: "Unknown"
source_reliability: "Not yet reviewed"
provenance_summary: ""
handling_restrictions: ""
extraction_required: "Unknown"
candidate_knowledge_records: []
related_existing_records: []
relationship_candidates: []
review_required: true
review_reason: ""
human_reviewer: ""
agent_assisted: false
agent_activity_refs: []
validation_state: "Pending validation"
intake_notes: ""
```

Field values may be completed by a human, proposed by an authorized agent, or produced through a governed workflow.

Agent-proposed values remain proposed until reviewed where review is required.

Unknown values should be marked clearly.

Do not guess source origin, privacy classification, provenance, reliability, or review status.

If a value is unavailable, use one of the following placeholder values where appropriate:

- Unknown
- Not applicable
- Not yet reviewed
- Pending human review
- Pending validation
- Pending privacy review
- Pending source review
- Pending provenance review
- Pending relationship review

If the intake record later supports creation of a Knowledge Record, the resulting Knowledge Record must use TEMPLATE-0001 and the applicable SC-0001 metadata fields.

## 5. Required Intake Field Instructions

Required intake fields must be completed or explicitly marked as unknown, pending, or not applicable.

A field is not complete if it is silently omitted when the value affects source handling, review, privacy, validation, provenance, extraction, transformation, or downstream use.

The following fields are required for a basic Source Material Intake Record.

**intake_id**

Records the identifier for this intake record.

The intake identifier identifies the intake record, not the Knowledge Object.

The intake identifier must not be treated as Object Identity for a Knowledge Record unless a governed specification explicitly creates that mapping.

**intake_title**

Provides a human-readable title for the intake record.

The intake title should help humans and agents recognize the intake item during review, routing, validation, and future lookup.

The intake title does not define source identity or Knowledge Object identity.

**intake_status**

Records the current intake handling state.

Use this field to show whether the material is draft, staged, pending review, quarantined, rejected, archived, or otherwise awaiting a governed workflow decision.

This field does not replace Lifecycle State for a Knowledge Record.

**source_material_id**

Records the identifier assigned to the Source Material when one exists.

This may be a local source identifier, temporary source identifier, import identifier, archive identifier, or other source-level identifier.

A source material identifier is not the same as Object Identity for a Knowledge Object.

**source_title**

Records the title, filename, label, subject, or best available human-readable name of the Source Material.

If the original source has no clear title, provide a descriptive title and preserve the uncertainty in the intake notes.

**source_type**

Records the general type of Source Material.

Examples may include document, image, transcript, dataset, note, message thread, scan, web capture, audio, video, code file, log, form, or imported reference.

This template does not define a final controlled vocabulary for source types.

**source_location**

Records where the Source Material is currently stored, staged, linked, archived, or referenced.

The source location may help humans, agents, workflows, and validators locate the material.

The source location must not define source meaning, Knowledge Object identity, approval, authority, privacy classification, or validation state.

**source_origin**

Records where the Source Material came from.

This may include a person, organization, system, website, repository, device, import batch, workflow, archive, capture process, or unknown origin.

If origin is uncertain, mark it as unknown or partially known rather than guessing.

**intake_created**

Records when the intake record was created.

Use a consistent date format within the implementation.

If the exact time is useful for review, import, audit, or provenance, include it.

**intake_updated**

Records when the intake record was last updated.

This field supports maintenance, review, validation, and traceability.

**privacy_classification**

Records the current privacy classification or proposed privacy classification for the Source Material.

If privacy is not yet reviewed, use Pending privacy review.

Agents must not reduce privacy classification without authorized review.

When privacy risk is uncertain, preserve the uncertainty and escalate for review.

**provenance_summary**

Summarizes what is known about source origin, capture, movement, transformation, import, extraction, agent involvement, workflow involvement, or human handling.

This field should be enough for a reviewer to understand where the Source Material came from and how it entered the system.

If provenance is missing or incomplete, state that clearly.

**extraction_required**

Records whether extraction, transcription, summarization, parsing, splitting, conversion, interpretation, or transformation is required before the material can support a Knowledge Record.

Use Unknown when extraction needs have not yet been reviewed.

**review_required**

Records whether human review, source review, privacy review, validation review, provenance review, relationship review, or workflow review is required.

This field should be true when uncertainty, privacy risk, source ambiguity, agent involvement, extraction, transformation, or downstream use affects handling.

**validation_state**

Records the current validation status of the intake record.

This field does not approve the Source Material.

Validation confirms whether the intake record satisfies applicable structure, metadata, provenance, privacy, relationship, storage, workflow, or agent expectations.

## 6. Recommended Intake Field Instructions

Recommended intake fields should be completed when practical.

These fields improve reviewability, traceability, automation reliability, privacy handling, source interpretation, extraction planning, relationship planning, validation, and future Knowledge Record creation.

The following fields are recommended for a stronger Source Material Intake Record.

**source_format**

Records the format or representation of the Source Material.

Examples may include Markdown, PDF, DOCX, TXT, CSV, JSON, PNG, JPG, MP3, MP4, HTML, email, database export, scan, or physical artifact reference.

**source_creator**

Records the known creator, author, sender, publisher, organization, system, agent, or workflow associated with the Source Material.

If authorship is uncertain, preserve the uncertainty.

**source_capture_method**

Records how the Source Material entered the system.

Examples may include manual upload, folder drop, scan, copy/paste, import, web capture, email export, repository pull, agent-assisted capture, workflow-generated capture, or migration.

**captured_by**

Records who or what captured the material.

This may be a human, agent, script, workflow, implementation, import process, migration process, or unknown actor.

**captured**

Records when the Source Material was captured, received, imported, exported, scanned, downloaded, copied, or staged.

This may differ from the date the source was originally created.

**source_availability**

Records whether the Source Material is available, unavailable, partially available, restricted, archived, missing, corrupted, externally hosted, superseded, or unknown.

This field supports future source review and validation.

**source_reliability**

Records a preliminary assessment of source reliability where useful.

This field may describe reliability concerns, bias concerns, freshness concerns, completeness concerns, uncertainty, conflict, or review needs.

This field must not be confused with Authority Level.

**handling_restrictions**

Records any known restrictions affecting access, privacy, publication, export, synchronization, indexing, backup, agent access, workflow access, or downstream use.

When restrictions are uncertain, escalate for review.

**candidate_knowledge_records**

Lists possible Knowledge Records that may be created from, about, or in response to the Source Material.

These are candidates only.

A candidate Knowledge Record is not approved or created until the applicable workflow produces it.

**related_existing_records**

Lists existing Knowledge Records, governed documents, Source Material records, review records, or workflow outputs that may relate to this intake item.

These relationships remain proposed until reviewed where review is required.

**relationship_candidates**

Lists possible relationships suggested by the intake process.

Relationship candidates may connect the Source Material to Knowledge Records, projects, people, topics, decisions, standards, workflows, or other governed entities.

Proposed relationships do not become approved relationships without applicable review.

**review_reason**

Explains why review is required.

Examples may include privacy uncertainty, unclear provenance, missing source origin, agent involvement, extraction complexity, conflicting sources, suspected duplicate, unclear relationship, validation issue, source reliability concern, or downstream-use risk.

**human_reviewer**

Records the person responsible for reviewing the intake record where a reviewer has been assigned.

If no reviewer has been assigned, use Pending human review.

**agent_activity_refs**

Lists references to Agent Activity Records when detailed agent activity must be preserved.

Use TEMPLATE-0003 when agent inspection, classification, extraction, validation, drafting, movement, modification, or recommendation requires a separate traceable record.

**intake_notes**

Records additional notes needed to understand, route, review, validate, repair, defer, quarantine, archive, transform, or reject the Source Material.

Intake notes should preserve uncertainty, source limitations, privacy concerns, provenance gaps, and review needs rather than hiding them.

## 7. Source Description and Context

This section records the plain-language description and context of the Source Material.

The purpose of this section is to help a future human, agent, workflow, validator, or implementation understand what the Source Material is before any extraction, transformation, Knowledge Record drafting, review, approval, publication, export, migration, or downstream use occurs.

This section should describe the Source Material without converting it into governed knowledge.

This section should not summarize the source so aggressively that source meaning, uncertainty, context, or provenance is lost.

Complete the following fields or subsections where applicable.

### 7.1 Source Description

Describe the Source Material in plain language.

Include what the material appears to be, what it contains, and why it may matter.

Recommended prompt:

What is this Source Material?

Example structure:

```text
This Source Material appears to be:
[brief description]

It contains:
[main visible contents, topics, or artifacts]

It may be relevant because:
[reason it may support future Knowledge Records, review, research, project work, reference, evidence, or archival use]
```

If the Source Material cannot be confidently described, state that clearly.

Do not invent context that is not visible, known, or supported.

### 7.2 Source Context

Record the context in which the Source Material was captured, received, created, imported, staged, or reviewed.

Recommended prompt:

Why is this Source Material being brought into The Brain?

Possible context may include:

- personal knowledge capture;
- research;
- project support;
- documentation;
- reference preservation;
- decision support;
- evidence preservation;
- workflow input;
- archive import;
- migration input;
- agent-assisted processing;
- future Knowledge Record creation.

If the context is unknown, use Unknown.

If the context is inferred, label it as inferred.

### 7.3 Source Boundaries

Describe what the Source Material does and does not include.

This helps prevent agents, workflows, or reviewers from overextending the source beyond its actual contents.

Recommended prompt:

What are the boundaries of this source?

Example structure:

```text
This source includes:
[known included material]

This source does not appear to include:
[known exclusions or missing context]

Unclear boundaries:
[uncertainties, missing pages, missing files, incomplete capture, partial transcript, unclear author, unclear date, broken links, missing attachments, or unknown scope]
```

Source boundaries should be preserved where missing context may affect interpretation, extraction, provenance, validation, authority, privacy, or downstream use.

### 7.4 Known Source Limitations

Record limitations that may affect source reliability, completeness, interpretation, extraction, validation, or downstream use.

Known limitations may include:

- missing pages;
- incomplete metadata;
- unclear origin;
- unknown author;
- unclear date;
- partial capture;
- poor scan quality;
- transcription uncertainty;
- image readability limits;
- audio quality issues;
- broken links;
- missing attachments;
- source bias;
- outdated information;
- conflicting information;
- unverifiable claims;
- privacy restrictions;
- access restrictions;
- uncertain provenance.

Limitations should be preserved rather than hidden.

A source with limitations may still be valuable, but those limitations must remain visible during review and transformation.

### 7.5 Initial Intake Notes

Record any intake notes that do not fit cleanly into the metadata block.

These notes may include:

- why the source was saved;
- what the user wants done with it;
- what the agent noticed;
- what should be reviewed later;
- what should not be extracted;
- what may require human judgment;
- what requires privacy caution;
- what appears duplicative;
- what appears related to existing records;
- what is unclear.

Initial intake notes are not final review notes.

Formal review decisions belong in TEMPLATE-0004 where required.

Detailed agent activity belongs in TEMPLATE-0003 where required.

## 8. Source Handling, Privacy, and Access Notes

This section records handling expectations for the Source Material.

Source handling must preserve privacy boundaries, access limits, review needs, validation needs, and downstream-use restrictions.

This section does not grant permission to publish, export, migrate, synchronize, index, back up, expose, or use the Source Material downstream.

Handling notes are used to route the Source Material safely through intake and review.

### 8.1 Privacy Review Notes

Record any known or suspected privacy concerns.

Privacy concerns may include:

- personal information;
- sensitive personal records;
- financial information;
- medical information;
- legal information;
- private communications;
- credentials or secrets;
- confidential project information;
- restricted source material;
- private identity details;
- location information;
- unpublished work;
- private organizational material;
- source material that should not be exposed to agents;
- source material that should not be exported or published.

If privacy classification is uncertain, use Pending privacy review.

Do not reduce privacy classification for convenience.

Do not treat storage location, filename, approval status, validation status, or agent usefulness as privacy clearance.

### 8.2 Access and Handling Restrictions

Record any known restrictions on who or what may access, process, move, copy, summarize, index, export, publish, or transform the Source Material.

Recommended prompt:

What restrictions apply to this source right now?

Example structure:

```text
Human access:
[allowed, restricted, pending review, unknown]

Agent access:
[allowed, restricted, prohibited, pending review, unknown]

Workflow access:
[allowed, restricted, pending review, unknown]

Implementation access:
[allowed, restricted, pending review, unknown]

Export or publication:
[not allowed, pending review, limited, unknown]
```

When access restrictions are unknown, preserve the uncertainty.

When source sensitivity is possible, use the more conservative handling path until reviewed.

### 8.3 Storage and Movement Notes

Record any storage, staging, archive, quarantine, import, export, migration, or movement concerns.

Storage and movement notes may include:

- current storage location;
- whether the source is staged for intake;
- whether the source should remain in place;
- whether the source should be quarantined;
- whether the source should be archived;
- whether the source may be copied;
- whether the source may be moved;
- whether the source is part of an import batch;
- whether the source is part of a migration package;
- whether the source has external dependencies;
- whether movement may break Source References or provenance.

Storage placement must not define source meaning, Object Identity, approval, authority, privacy classification, validation state, or downstream-use permission.

### 8.4 Agent Access Notes

Record whether agent assistance is allowed for this intake item.

Agent access notes should specify what kind of agent activity is permitted or prohibited.

Agent activity may include:

- reading;
- summarizing;
- classifying;
- extracting;
- proposing metadata;
- proposing Source References;
- proposing relationships;
- detecting privacy risks;
- detecting validation issues;
- drafting Knowledge Records;
- preparing review notes.

Agent access should be limited when the Source Material may contain restricted, sensitive, confidential, private, legally sensitive, identity-sensitive, or unknown-risk material.

Agents must not fabricate Source References, erase provenance uncertainty, reduce privacy classification, approve Source Material, or convert intake outputs into approved Knowledge Records without the required review path.

### 8.5 Quarantine or Escalation Conditions

Record conditions that require quarantine, escalation, repair, or human review before further processing.

Escalation may be required when the intake item has:

- unclear origin;
- unclear privacy classification;
- suspected sensitive information;
- missing provenance;
- source reliability concerns;
- conflicting source information;
- suspected duplicate identity;
- unclear relationship to existing records;
- validation failure;
- extraction uncertainty;
- corrupted or unreadable content;
- possible legal restriction;
- possible publication restriction;
- agent access risk;
- export or migration risk.

If quarantine is required, state the reason clearly.

If escalation is required, state who or what should review the issue where known.

## 9. Extraction and Transformation Planning

This section records how the Source Material may be extracted, transformed, summarized, split, interpreted, or converted for future use.

Extraction and transformation planning does not create approved knowledge.

Extraction and transformation planning does not approve a Knowledge Record.

Extraction and transformation planning does not replace Source References, provenance, validation, or review.

This section helps determine what work is needed before the Source Material can support Knowledge Records or other governed outputs.

### 9.1 Extraction Need

Record whether extraction is required.

Use one of the following values where practical:

- Required
- Not required
- Partially required
- Unknown
- Pending review

Extraction may be required when Source Material must be:

- transcribed;
- summarized;
- parsed;
- split;
- converted;
- translated;
- cleaned;
- structured;
- OCR-reviewed;
- manually inspected;
- source-referenced;
- privacy-reviewed;
- validated;
- transformed into one or more Knowledge Records.

If extraction need is uncertain, preserve that uncertainty.

### 9.2 Extraction Targets

Identify what information may need to be extracted.

Extraction targets may include:

- facts;
- definitions;
- claims;
- decisions;
- procedures;
- tasks;
- project information;
- people;
- organizations;
- dates;
- events;
- requirements;
- source references;
- provenance details;
- relationships;
- metadata candidates;
- privacy-sensitive details;
- validation concerns;
- open questions;
- contradictions;
- supporting evidence.

Extraction targets are candidates only.

Extracted material must remain traceable to the Source Material where source support affects meaning, authority, validation, provenance, or downstream use.

### 9.3 Transformation Plan

Describe any transformation that may be needed before the material can be used.

Transformation may include:

- converting file format;
- cleaning text;
- splitting one source into multiple intake records;
- combining related source fragments;
- creating one or more draft Knowledge Records;
- creating a source summary;
- creating a transcript;
- creating a structured table;
- creating metadata proposals;
- creating relationship proposals;
- creating review notes;
- creating validation findings;
- creating a redacted version;
- creating an archive copy;
- creating a migration-ready package.

Transformation must preserve Source Material boundaries.

Transformation must preserve provenance.

Transformation must preserve privacy restrictions.

Transformation must not silently convert Source Material into approved governed knowledge.

### 9.4 Candidate Knowledge Record Plan

List possible Knowledge Records that may be created from, about, or in response to the Source Material.

Recommended structure:

```text
Candidate Knowledge Records:
1. [Proposed title or topic]
   Purpose:
   Source support:
   Review needed:
   Notes:

2. [Proposed title or topic]
   Purpose:
   Source support:
   Review needed:
   Notes:
```

Candidate Knowledge Records remain proposed until created through the applicable workflow.

If no Knowledge Record should be created, state that clearly.

Reasons no Knowledge Record may be created include:

- source is only archival;
- source is duplicate;
- source is out of scope;
- source is unreliable;
- source is too sensitive;
- source requires later review;
- source should remain raw material only;
- source should be rejected or quarantined.

### 9.5 Extraction Risks and Open Questions

Record risks, uncertainties, and unresolved questions that may affect extraction or transformation.

Extraction risks may include:

- unclear source meaning;
- missing context;
- ambiguous author intent;
- privacy exposure;
- uncertain provenance;
- uncertain reliability;
- conflicting information;
- poor readability;
- incomplete capture;
- unsupported claims;
- unclear relationship to existing records;
- duplicate risk;
- validation risk;
- agent hallucination risk;
- transformation loss;
- source-reference loss;
- downstream-use risk.

Open questions should remain visible until resolved.

Do not hide unresolved questions by creating overly confident summaries or Knowledge Records.

## 10. Agent-Assisted Intake Instructions

This section defines how agents may assist with Source Material intake when agent assistance is allowed.

These instructions are operational template instructions.

They do not create new agent permissions.

They do not replace AG-0001.

They do not replace TEMPLATE-0003 — Agent Activity Record Template.

They do not allow agents to approve Source Material, approve Knowledge Records, override privacy classification, assign final authority, delete material, publish material, export restricted material, or make unreviewable governance decisions.

Agent assistance during intake must remain reviewable, traceable, bounded, and subordinate to human review and governed workflows.

### 10.1 Allowed Agent Assistance

Where authorized, agents may assist Source Material intake by:

- reading or inspecting Source Material;
- identifying visible source type;
- describing source contents;
- summarizing source context;
- identifying possible source origin;
- identifying provenance gaps;
- identifying privacy risks;
- identifying access or handling concerns;
- identifying extraction needs;
- proposing metadata values;
- proposing Source References;
- proposing relationship candidates;
- proposing candidate Knowledge Records;
- identifying duplicate or related material;
- identifying validation concerns;
- preparing intake notes;
- preparing review questions;
- drafting non-final intake outputs.

Agent assistance must preserve uncertainty.

Agent assistance must not silently convert uncertain information into confirmed information.

Agent assistance must not treat a model-generated summary as a substitute for Source Material.

### 10.2 Required Agent Boundaries

Agents must remain within the boundaries defined by the applicable agent standard, workflow standard, privacy rules, validation rules, and review requirements.

Agents must not:

- approve Source Material;
- approve extracted knowledge;
- approve Knowledge Records;
- assign final Authority Level;
- reduce Privacy Classification;
- erase provenance uncertainty;
- fabricate Source References;
- fabricate source origin;
- fabricate source reliability;
- fabricate relationships;
- delete Source Material;
- permanently move Source Material without authorization;
- publish Source Material;
- export restricted Source Material;
- convert Source Material into approved governed knowledge;
- treat workflow completion as approval;
- treat validation success as approval;
- treat confidence as authority.

When an agent identifies uncertainty, conflict, privacy risk, missing provenance, unclear source origin, suspected duplicate identity, extraction risk, validation issue, or downstream-use concern, the condition should be preserved in the intake record and escalated where required.

### 10.3 Agent Notes Required in Intake Record

When an agent assists with intake, the intake record should identify what the agent did.

At minimum, agent-assisted intake should record:

- whether agent assistance occurred;
- what Source Material the agent inspected;
- what metadata the agent proposed;
- what descriptions the agent generated;
- what extraction or transformation the agent recommended;
- what privacy concerns the agent identified;
- what provenance concerns the agent identified;
- what relationship candidates the agent proposed;
- what candidate Knowledge Records the agent proposed;
- what uncertainty remains;
- what human review is required.

If detailed traceability is required, create or reference an Agent Activity Record using TEMPLATE-0003.

### 10.4 When TEMPLATE-0003 Is Required

A separate Agent Activity Record should be created when agent activity materially affects review, validation, provenance, privacy, authority, relationships, extraction, transformation, movement, or downstream use.

TEMPLATE-0003 should be used when an agent:

- reads restricted or privacy-sensitive material;
- performs substantial extraction;
- performs substantial summarization;
- proposes Knowledge Records;
- proposes relationships;
- proposes Source References;
- proposes privacy classification;
- proposes authority-related handling;
- detects validation issues;
- detects duplicate or identity conflicts;
- recommends quarantine;
- recommends rejection;
- recommends archival;
- recommends movement;
- drafts a Knowledge Record;
- modifies intake content;
- produces outputs that require later audit.

If agent activity is minor, such as formatting assistance or simple spelling correction, a separate Agent Activity Record may not be required unless a workflow, reviewer, or higher-authority rule requires it.

### 10.5 Agent Output Review

Agent outputs must be reviewed according to the risk and scope of the intake item.

Agent-generated descriptions, summaries, classifications, relationships, extraction plans, and candidate Knowledge Records should be treated as proposals until reviewed.

Agent confidence must not be treated as validation, approval, authority, or privacy clearance.

Where agent output cannot be verified against the Source Material, the output should be marked as uncertain, rejected, deferred, or escalated for review.

## 11. Intake Validation and Completion Checklist

This checklist is used to determine whether a Source Material Intake Record is structurally complete enough for the next workflow step.

Checklist completion does not approve Source Material.

Checklist completion does not approve extracted knowledge.

Checklist completion does not approve a Knowledge Record.

Checklist completion does not authorize publication, export, migration, synchronization, indexing, or downstream use.

### 11.1 Structural Completeness

- [ ] The document has the correct title and document identifier.
- [ ] Sections 1 through 12 are present.
- [ ] Heading order is sequential.
- [ ] Code fences are balanced.
- [ ] The Source Material Intake Metadata Block is present.
- [ ] Required intake fields are completed or explicitly marked as unknown, pending, or not applicable.
- [ ] Placeholder values are used where information is not yet known.
- [ ] The intake record is readable by humans.
- [ ] The intake record is structured enough for agent and workflow use.

### 11.2 Source and Provenance Completeness

- [ ] Source Material is described clearly.
- [ ] Source type is identified or marked unknown.
- [ ] Source location is recorded or marked unknown.
- [ ] Source origin is recorded or marked unknown.
- [ ] Source creator is recorded where known.
- [ ] Capture method is recorded where known.
- [ ] Capture date is recorded where known.
- [ ] Provenance summary is present.
- [ ] Provenance gaps are preserved rather than hidden.
- [ ] Source availability is recorded or marked unknown.
- [ ] Source reliability is recorded or marked not yet reviewed.

### 11.3 Privacy and Handling Completeness

- [ ] Privacy classification is recorded or marked Pending privacy review.
- [ ] Handling restrictions are recorded where known.
- [ ] Access restrictions are recorded where known.
- [ ] Agent access limits are recorded where needed.
- [ ] Export or publication restrictions are recorded where known.
- [ ] Quarantine or escalation conditions are recorded where needed.
- [ ] Privacy uncertainty is preserved rather than normalized away.
- [ ] No privacy classification has been reduced by an agent without authorized review.

### 11.4 Extraction and Transformation Completeness

- [ ] Extraction need is recorded.
- [ ] Extraction targets are recorded where known.
- [ ] Transformation needs are recorded where known.
- [ ] Candidate Knowledge Records are listed where applicable.
- [ ] Related existing records are listed where known.
- [ ] Relationship candidates are listed where applicable.
- [ ] Extraction risks are recorded where present.
- [ ] Open questions are preserved.
- [ ] Source Material boundaries remain clear.
- [ ] Extracted or proposed knowledge is not treated as approved knowledge.

### 11.5 Agent and Review Completeness

- [ ] Agent assistance status is recorded.
- [ ] Agent activity references are listed where required.
- [ ] Agent-generated proposals are distinguishable from reviewed values.
- [ ] Human review requirement is recorded.
- [ ] Review reason is recorded where review is required.
- [ ] Human reviewer is assigned or marked Pending human review where applicable.
- [ ] Validation state is recorded.
- [ ] Issues requiring repair, escalation, quarantine, rejection, archival, or deferral are visible.
- [ ] The intake record is ready for the next governed workflow step.

## 12. Template Success Criteria

TEMPLATE-0002 is successful when it provides a practical, repeatable, copy/paste-ready structure for Source Material intake without redefining higher-authority standards.

A completed Source Material Intake Record should make the Source Material easier to understand, route, review, validate, preserve, extract, transform, archive, reject, quarantine, or convert into one or more draft Knowledge Records.

TEMPLATE-0002 succeeds when it preserves the distinction between:

- Source Material and Knowledge Records;
- intake records and approval records;
- source identifiers and Object Identity;
- source description and governed knowledge;
- proposed metadata and reviewed metadata;
- Source References and provenance;
- source reliability and Authority Level;
- privacy classification and storage location;
- validation and approval;
- agent assistance and agent authority;
- extraction planning and Knowledge Record creation;
- relationship candidates and approved relationships;
- review requirements and review decisions.

TEMPLATE-0002 succeeds when humans can use it manually without specialized tooling.

TEMPLATE-0002 succeeds when agents can use it without becoming unreviewable authorities.

TEMPLATE-0002 succeeds when workflows can use it to route Source Material into review, extraction, transformation, quarantine, archive, rejection, or Knowledge Record drafting.

TEMPLATE-0002 succeeds when validators can check whether intake records are structurally complete, source-aware, provenance-aware, privacy-aware, relationship-aware, review-aware, and agent-traceable.

TEMPLATE-0002 succeeds when implementations can store, display, migrate, export, import, search, or process intake records without making the template dependent on one application, plugin, LLM, database, folder layout, user interface, or automation tool.

TEMPLATE-0002 fails if it:

- becomes a Knowledge Record template;
- replaces TEMPLATE-0001;
- redefines SC-0001 metadata fields;
- redefines Source Material;
- redefines Source References;
- redefines provenance;
- redefines Object Identity;
- redefines privacy classifications;
- redefines lifecycle states;
- redefines validation states;
- redefines authority levels;
- acts as an approval record;
- acts as a formal review record;
- acts as a detailed agent activity record;
- allows agents to approve governed knowledge without review;
- allows storage placement to define meaning;
- allows validation to replace approval;
- allows source uncertainty to be hidden;
- allows privacy uncertainty to be ignored;
- allows Source Material to become governed knowledge merely because it was captured, summarized, indexed, or processed.

A Source Material Intake Record created from this template is ready for the next workflow step when:

- required intake fields are present or explicitly marked unknown, pending, or not applicable;
- source description and context are clear enough for review;
- provenance is recorded or gaps are visible;
- privacy classification is recorded or pending review;
- extraction and transformation needs are recorded;
- candidate Knowledge Records are proposed where applicable;
- agent assistance is recorded where applicable;
- review requirements are visible;
- validation state is recorded;
- unresolved risks and open questions remain visible.

When those criteria are met, the intake record may proceed to the applicable ingestion, review, validation, extraction, transformation, archival, quarantine, rejection, or Knowledge Record drafting workflow.