# TEMPLATE-0001 — Knowledge Record Template

Document ID: TEMPLATE-0001
Title: Knowledge Record Template
Version: 0.1.0
Status: Draft
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Operational Document
Phase: Operational Bootstrap
Milestone: 1.2 — Knowledge Record Template
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SC-0001 — Knowledge Record Metadata Field Specification
Supersedes: None
Superseded By: None
Related: TEMPLATE-0002 — Source Material Intake Template; TEMPLATE-0003 — Agent Activity Record Template; TEMPLATE-0004 — Review Record Template; VALID-0001 — Bare Usable Validation Checklist

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and template-use rules are interpreted within TEMPLATE-0001.

TEMPLATE-0001 is an operational template.

TEMPLATE-0001 does not define new standards, new metadata meanings, new authority levels, new lifecycle states, new validation states, new privacy classifications, new relationship rules, new provenance rules, or new agent permissions.

Where conflicts arise between this template and any higher-authority document, the higher-authority document SHALL take precedence.

Where conflicts arise between this template and SC-0001, SC-0001 SHALL control the metadata field names and minimum metadata expectations for Knowledge Records.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a Knowledge Object or Knowledge Record.
- Source Reference refers to a traceable reference from a Knowledge Record to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the record.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a Knowledge Record.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Validation State refers to the current validation status of a governed entity within a defined validation scope.
- Agent Assistance refers to agent participation in creating, classifying, summarizing, extracting, validating, drafting, or proposing changes to a Knowledge Record within authorized boundaries.
- Human Review refers to review performed by a human to confirm, correct, reject, approve, limit, escalate, or route governed entities where human judgment is required.
- Template refers to a reusable operational structure used to create a Knowledge Record without redefining the standards or specifications it depends on.

## 1. Purpose

The purpose of TEMPLATE-0001 is to provide a copy/paste-ready structure for creating bare usable Knowledge Records under The Brain Standard.

TEMPLATE-0001 turns the metadata field expectations defined by SC-0001 into a practical record form that humans, agents, workflows, validators, and implementations can use during knowledge creation.

TEMPLATE-0001 exists so that Knowledge Records can be created consistently without requiring each user, agent, workflow, or implementation to invent its own record structure.

A Knowledge Record created from this template SHOULD be:

- human-readable;
- AI-readable;
- Markdown-compatible;
- implementation-independent;
- traceable to source material where applicable;
- reviewable by a human;
- compatible with validation;
- compatible with future migration;
- compatible with agent-assisted workflows;
- clear enough to support daily use.

TEMPLATE-0001 is intended for Draft Knowledge Records during bare usable deployment.

A record created from this template is not automatically approved, authoritative, valid, published, export-ready, migration-ready, or safe for downstream use.

TEMPLATE-0001 provides structure.

It does not provide approval.

TEMPLATE-0001 supports agent assistance.

It does not grant agents authority over Object Identity, lifecycle transitions, authority assignment, privacy classification, validation approval, publication, export, migration, deletion, or downstream-use readiness.

The success of TEMPLATE-0001 is measured by whether a human or authorized agent can use it to create a Knowledge Record that preserves identity, metadata, provenance, source references, relationships, lifecycle state, authority level, privacy classification, validation state, review expectations, and agent traceability without depending on any single application, plugin, model, database, folder path, or user interface.

## 2. Relationship to SC-0001 and Prior Standards

TEMPLATE-0001 depends directly on SC-0001 — Knowledge Record Metadata Field Specification.

SC-0001 defines the exact metadata field names and minimum field expectations for bare usable Knowledge Records.

TEMPLATE-0001 consumes those field names.

TEMPLATE-0001 MUST NOT rename, replace, reinterpret, or redefine SC-0001 metadata fields.

TEMPLATE-0001 MAY explain how a field should be filled in during practical use, but that explanation MUST remain subordinate to SC-0001 and the higher-authority standards.

SC-0001 provides the field specification.

TEMPLATE-0001 provides the usable record form.

TEMPLATE-0001 depends on the constitutional foundation because Knowledge Records must preserve The Brain Standard’s implementation-independent, portable, governed, human-readable, and AI-readable architecture.

TEMPLATE-0001 depends on the Knowledge Standards because Knowledge Records must preserve:

- Knowledge Object meaning;
- Object Identity;
- metadata role boundaries;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State.

TEMPLATE-0001 depends on storage standards because a Knowledge Record may be stored, moved, copied, archived, imported, exported, backed up, indexed, or migrated without allowing storage location, filename, folder placement, application behavior, or repository structure to define its knowledge meaning.

TEMPLATE-0001 depends on agent standards because agents may assist with Knowledge Record creation only within governed operating boundaries.

TEMPLATE-0001 depends on workflow standards because Knowledge Records may be created through ingestion, review, approval, maintenance, publication, export, migration, or downstream-use workflows without allowing workflow state to replace lifecycle state, authority level, privacy classification, validation state, provenance, or human review.

TEMPLATE-0001 is lower authority than constitutional documents, standards, and specifications.

If this template appears to conflict with SC-0001, SC-0001 controls.

If this template appears to conflict with a Knowledge Standard, Storage Standard, Agent Standard, Workflow Standard, or constitutional document, the higher-authority document controls.

## 3. Template Scope and Use Rules

TEMPLATE-0001 applies to the creation of bare usable Knowledge Records.

A Knowledge Record created from this template MAY represent:

- knowledge extracted from Source Material;
- knowledge summarized from Source Material;
- knowledge interpreted from Source Material;
- knowledge created through human reasoning;
- knowledge drafted with agent assistance;
- knowledge produced through a governed workflow;
- knowledge imported from another system;
- knowledge prepared for later validation, review, approval, maintenance, or downstream use.

TEMPLATE-0001 does not apply to raw Source Material by itself.

Raw Source Material SHOULD use TEMPLATE-0002 when it is being registered, staged, classified, or prepared for ingestion.

TEMPLATE-0001 does not apply to agent activity logs by themselves.

Agent activity SHOULD use TEMPLATE-0003 when agent reads, classifications, summaries, extractions, validations, proposals, edits, movements, or other agent actions must be recorded.

TEMPLATE-0001 does not apply to review records by themselves.

Review decisions SHOULD use TEMPLATE-0004 when human review, approval, rejection, repair, escalation, validation review, privacy review, authority review, or downstream-use review must be recorded.

A Knowledge Record created from TEMPLATE-0001 MUST preserve the SC-0001 metadata field names.

A Knowledge Record created from TEMPLATE-0001 MUST distinguish the Knowledge Record from Source Material.

A Knowledge Record created from TEMPLATE-0001 MUST distinguish Object Identity from title, filename, folder path, alias, tag, application identifier, implementation identifier, workflow identifier, or agent identifier.

A Knowledge Record created from TEMPLATE-0001 MUST preserve Lifecycle State as distinct from Authority Level, Privacy Classification, Validation State, workflow state, agent state, storage state, and implementation state.

A Knowledge Record created from TEMPLATE-0001 MUST preserve Source References as distinct from provenance.

A Knowledge Record created from TEMPLATE-0001 MUST preserve relationships as explicit governed connections rather than treating backlinks, tags, search similarity, graph placement, or agent suggestions as approved relationships by default.

A Knowledge Record created from TEMPLATE-0001 MUST preserve human reviewability.

A Knowledge Record created from TEMPLATE-0001 MUST preserve agent traceability when agent assistance is used.

A Knowledge Record created from TEMPLATE-0001 MUST NOT be treated as approved merely because it is structurally complete.

A Knowledge Record created from TEMPLATE-0001 MUST NOT be treated as valid merely because it was created from the template.

A Knowledge Record created from TEMPLATE-0001 MUST NOT be treated as authoritative merely because it has a completed metadata block.

A Knowledge Record created from TEMPLATE-0001 MUST NOT be treated as publishable, export-ready, migration-ready, or downstream-use-ready unless the applicable workflow, validation, privacy, authority, and review requirements have been satisfied.

TEMPLATE-0001 MAY be used by humans, Codex, Obsidian, other LLM systems, local AI systems, validation tools, scripts, or future implementations.

No implementation becomes required merely because it can use this template.

The template remains valid only when it preserves the standards and specifications it depends on.

## 4. Knowledge Record Metadata Block

The following metadata block SHALL be used as the base metadata block for a bare usable Knowledge Record created from TEMPLATE-0001.

This block uses the SC-0001 field names exactly.

This block MUST NOT be treated as a new metadata specification.

This block MAY be copied into a Markdown Knowledge Record and completed during drafting, ingestion, review, validation, maintenance, or agent-assisted preparation.

```yaml
object_id: TBD
record_id: TBD
record_type: TBD
title: TBD
summary: TBD
lifecycle_state: draft
authority_level: unreviewed
privacy_classification: private
validation_state: not_validated
source_refs: []
provenance: TBD
relationships: []
created: TBD
updated: TBD
review_required: true
agent_assisted: false
human_reviewer: unassigned
```

The following supporting fields SHOULD be included when they materially improve discovery, reviewability, traceability, maintenance, validation, or agent-assisted workflow handling.

```yaml
aliases: []
keywords: []
review_refs: []
agent_activity_refs: []
```

The metadata block SHOULD appear near the beginning of the Knowledge Record so that humans, agents, validators, workflows, storage systems, and implementations can inspect the record without relying on hidden application state.

The metadata block MAY be represented as Markdown-compatible YAML front matter, a structured metadata section, a sidecar metadata file, a database field set, or another governed representation method.

The representation method does not define the metadata meaning.

The metadata meaning remains governed by SC-0001 and the higher-authority standards.

A compliant implementation MUST preserve the field names, field meanings, and field boundaries when importing, exporting, migrating, indexing, validating, or processing a Knowledge Record.

A Knowledge Record created from this template MUST NOT rely only on filename, folder path, tag, graph location, plugin field, database state, application display, agent memory, workflow memory, or user-interface state to preserve required metadata meaning.

## 5. Required Field Instructions

The required fields in the Knowledge Record metadata block MUST be completed or preserved according to SC-0001.

These instructions explain practical use only.

They do not redefine the fields.

### 5.1 object_id

`object_id` identifies the Knowledge Object represented by the Knowledge Record.

If stable Object Identity has not yet been assigned, the value MAY remain `TBD` during drafting.

An agent, workflow, implementation, folder path, filename, title, alias, tag, or database identifier MUST NOT replace governed Object Identity.

### 5.2 record_id

`record_id` identifies the specific Knowledge Record representation.

A Knowledge Object MAY have more than one Knowledge Record over time, across versions, drafts, migrations, imports, exports, or implementations.

The `record_id` MUST remain distinguishable from `object_id`.

### 5.3 record_type

`record_type` identifies the practical kind of Knowledge Record being created.

The value SHOULD be clear enough to support review, routing, validation, maintenance, and downstream use.

If the correct record type is uncertain, the value MAY remain `TBD` until review or validation.

### 5.4 title

`title` provides the human-readable name of the Knowledge Record.

The title SHOULD help humans recognize the record.

The title MUST NOT be treated as Object Identity.

The title MAY change without changing `object_id` unless a governed identity decision determines that the underlying Knowledge Object has changed.

### 5.5 summary

`summary` provides a concise explanation of what the Knowledge Record contains.

The summary SHOULD describe the record without replacing the body content, source references, provenance, relationships, validation, or review.

If the record is source-derived, the summary SHOULD avoid overstating unsupported claims.

### 5.6 lifecycle_state

`lifecycle_state` records the current governed lifecycle state of the Knowledge Record.

For new records created from this template, the default value SHALL be:

```yaml
lifecycle_state: draft
```

Lifecycle State MUST remain distinguishable from Authority Level, Privacy Classification, Validation State, workflow state, agent state, storage state, and implementation state.

### 5.7 authority_level

`authority_level` records the current authority level of the Knowledge Record.

For new records created from this template, the default value SHALL be:

```yaml
authority_level: unreviewed
```

Authority Level MUST NOT be treated as approval unless a governed review or approval workflow explicitly assigns that authority.

### 5.8 privacy_classification

`privacy_classification` records the privacy handling expectation for the Knowledge Record.

For new records created from this template, the default value SHALL be:

```yaml
privacy_classification: private
```

Privacy Classification MUST be reviewed before publication, export, synchronization, indexing, agent exposure, implementation exposure, or downstream use beyond the original privacy boundary.

### 5.9 validation_state

`validation_state` records the current validation status of the Knowledge Record.

For new records created from this template, the default value SHALL be:

```yaml
validation_state: not_validated
```

Validation State MUST NOT be treated as approval.

A record may be structurally complete and still remain unvalidated, unreviewed, unauthoritative, private, draft, or unsuitable for downstream use.

### 5.10 source_refs

`source_refs` records traceable references to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the Knowledge Record.

If no Source Material applies, the field SHOULD remain an empty list unless a governed rule or workflow requires an explanatory value.

Source References MUST remain distinguishable from provenance.

### 5.11 provenance

`provenance` records origin, source, reasoning, transformation, creator, editor, agent, workflow, validation, review, import, export, migration, or change context associated with the Knowledge Record.

If provenance has not yet been completed, the value MAY remain `TBD` during drafting.

Provenance MUST remain distinguishable from Source References.

### 5.12 relationships

`relationships` records explicit governed relationships between the Knowledge Record and other Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, or other governed entities.

For new records, the default value MAY be:

```yaml
relationships: []
```

Backlinks, tags, search similarity, graph placement, folder proximity, or agent suggestions MUST NOT be treated as approved relationships by default.

### 5.13 created

`created` records when the Knowledge Record was created.

The value SHOULD use a consistent date or timestamp format compatible with validation, migration, export, and long-term inspection.

If the creation date is not yet known, the value MAY remain `TBD` during drafting.

### 5.14 updated

`updated` records when the Knowledge Record was last materially updated.

The value SHOULD change when record content, required metadata, provenance, relationships, validation state, review state, lifecycle state, authority level, privacy classification, or other governed meaning changes.

If the record has not yet been updated after creation, `updated` MAY match `created`.

### 5.15 review_required

`review_required` records whether human or governed review is required.

For new records created from this template, the default value SHALL be:

```yaml
review_required: true
```

A record SHOULD remain review-required until the applicable workflow, review, validation, authority, privacy, and lifecycle expectations are satisfied.

### 5.16 agent_assisted

`agent_assisted` records whether an agent materially assisted with creating, classifying, summarizing, extracting, validating, drafting, editing, or proposing content for the Knowledge Record.

For human-only records, the value MAY remain:

```yaml
agent_assisted: false
```

If an agent materially assists the record, the value SHOULD be changed to:

```yaml
agent_assisted: true
```

Agent assistance MUST remain traceable where it affects metadata, content, source references, provenance, relationships, validation, review, lifecycle state, authority level, privacy classification, publication, export, migration, or downstream use.

### 5.17 human_reviewer

`human_reviewer` identifies the assigned human reviewer where review is required.

For new records created from this template, the default value SHALL be:

```yaml
human_reviewer: unassigned
```

If no reviewer has been assigned, the value SHOULD remain `unassigned`.

A named reviewer field does not mean review has been completed.

Review completion MUST be recorded through the applicable review process or review record.

## 6. Recommended Field Instructions

The recommended fields in this section SHOULD be included when they improve discovery, reviewability, maintenance, agent traceability, validation, or downstream usability.

These fields are recommended supporting fields.

They do not replace the required SC-0001 metadata field set.

### 6.1 aliases

`aliases` records alternate human-readable names, labels, spellings, abbreviations, former names, or recognition aids associated with the Knowledge Record or represented Knowledge Object.

Aliases SHOULD support discovery and human recognition.

Aliases MUST NOT replace Object Identity.

Aliases MUST NOT be treated as stable identifiers unless a governed standard or specification explicitly assigns that role.

Example:

```yaml
aliases:
  - Alternate Name
  - Prior Name
```

### 6.2 keywords

`keywords` records controlled or practical discovery terms that help humans, agents, workflows, validators, or implementations locate and classify the Knowledge Record.

Keywords SHOULD be useful without becoming a hidden taxonomy or replacement relationship system.

Keywords MUST NOT replace explicit relationships.

Keywords MUST NOT define lifecycle state, authority level, privacy classification, validation state, source support, or provenance.

Example:

```yaml
keywords:
  - knowledge-record
  - source-derived
  - draft
```

### 6.3 review_refs

`review_refs` records references to review records, review notes, review decisions, approval records, rejection records, repair requests, escalation records, or other governed review outputs.

Review references SHOULD be used when a Knowledge Record has entered review, completed review, been rejected, been repaired, been approved, been escalated, been reapproved, been deprecated, been superseded, or been routed for additional review.

Review references MUST NOT replace the review record itself.

Example:

```yaml
review_refs:
  - REVIEW-0000
```

### 6.4 agent_activity_refs

`agent_activity_refs` records references to agent activity records associated with the Knowledge Record.

This field SHOULD be used when an agent materially assisted with reading, classification, summarization, extraction, metadata suggestion, relationship suggestion, source-reference suggestion, provenance drafting, validation support, revision drafting, movement recommendation, or other governed activity.

Agent activity references SHOULD point to records created under TEMPLATE-0003 where applicable.

Agent activity references MUST NOT replace provenance, validation, human review, or approval.

Example:

```yaml
agent_activity_refs:
  - AG-ACT-0000
```

Recommended fields SHOULD remain minimal.

A Knowledge Record SHOULD NOT include supporting fields merely because an implementation, plugin, agent, workflow, or user interface can generate them.

Supporting fields are justified when they materially improve durability, portability, reviewability, traceability, validation, discovery, maintenance, or governed automation.

If a recommended field is not useful for a specific Knowledge Record, it MAY remain omitted unless a future specification, workflow, implementation profile, or validation rule requires it.

## 7. Knowledge Record Body Structure

The body of a Knowledge Record contains the usable knowledge content of the record.

The body MUST remain distinguishable from the metadata block.

The body MUST remain distinguishable from raw Source Material.

The body SHOULD be structured clearly enough that a human, agent, workflow, validator, or implementation can understand what the record says, what it is based on, what remains uncertain, and what review may be needed.

A Knowledge Record body SHOULD include the following practical sections where applicable:

```markdown
## Record Summary

TBD

## Knowledge Content

TBD

## Context and Scope

TBD

## Key Details

TBD

## Limits, Uncertainty, and Open Questions

TBD
```

The body structure MAY be expanded when the Knowledge Record requires additional explanation, examples, reasoning, comparison, extraction, interpretation, decision support, or maintenance notes.

The body structure SHOULD remain minimal when the Knowledge Record is simple.

A Knowledge Record body MUST NOT redefine metadata fields.

A Knowledge Record body MUST NOT replace Source References.

A Knowledge Record body MUST NOT replace provenance.

A Knowledge Record body MUST NOT replace relationships.

A Knowledge Record body MUST NOT replace validation.

A Knowledge Record body MUST NOT replace human review.

A Knowledge Record body MUST NOT imply approval, authority, publication readiness, export readiness, migration readiness, or downstream-use readiness unless the applicable governed metadata, validation, workflow, and review records support that interpretation.

### 7.1 Record Summary

The Record Summary section SHOULD provide a short human-readable explanation of the Knowledge Record.

The Record Summary SHOULD be consistent with the `summary` metadata field.

The Record Summary MAY provide more explanation than the metadata summary when useful.

The Record Summary MUST NOT introduce claims that are not supported by the Knowledge Content, Source References, provenance, review, or applicable context.

Example:

```markdown
## Record Summary

This Knowledge Record summarizes the main idea, source context, and current review status of the captured knowledge.
```

### 7.2 Knowledge Content

The Knowledge Content section SHOULD contain the main structured knowledge being preserved.

Knowledge Content MAY include:

- extracted facts;
- summarized ideas;
- interpreted meaning;
- reasoning notes;
- operational instructions;
- conceptual explanations;
- decision context;
- reference information;
- examples;
- definitions when they are record-specific;
- observations;
- open issues.

Knowledge Content MUST NOT redefine The Brain Standard, Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, specifications, templates, validation rules, or governance requirements unless the Knowledge Record itself is a governed standards document.

Example:

```markdown
## Knowledge Content

TBD
```

### 7.3 Context and Scope

The Context and Scope section SHOULD explain what the Knowledge Record applies to and what it does not apply to.

Context and Scope SHOULD be used when the record could otherwise be misunderstood, over-applied, or confused with a broader rule, standard, source, workflow, implementation, or decision.

Example:

```markdown
## Context and Scope

This record applies to TBD.

This record does not apply to TBD.
```

### 7.4 Key Details

The Key Details section SHOULD preserve important supporting points that make the Knowledge Record useful for recall, review, validation, maintenance, or downstream use.

Key Details MAY include extracted points, structured notes, examples, conditions, constraints, related considerations, or operational details.

Key Details SHOULD remain concise enough that the Knowledge Record remains usable.

Example:

```markdown
## Key Details

- TBD
- TBD
- TBD
```

### 7.5 Limits, Uncertainty, and Open Questions

The Limits, Uncertainty, and Open Questions section SHOULD be used when the Knowledge Record contains incomplete information, unresolved interpretation, weak evidence, unclear source support, disputed meaning, uncertain classification, pending review, or future maintenance needs.

This section SHOULD help prevent a draft or partially reviewed record from being treated as more complete, authoritative, or validated than it is.

Example:

```markdown
## Limits, Uncertainty, and Open Questions

- TBD
- TBD
- TBD
```

## 8. Source and Provenance Section

A Knowledge Record SHOULD include a Source and Provenance section when the record is derived from, supported by, transformed from, interpreted from, or connected to Source Material, human reasoning, agent activity, workflow activity, import activity, migration activity, or review activity.

The Source and Provenance section supports inspection.

It does not replace the `source_refs` metadata field.

It does not replace the `provenance` metadata field.

It does not replace governed Source Reference records, provenance records, review records, agent activity records, or workflow records where those are required.

A Source and Provenance section SHOULD use the following practical structure where applicable:

```markdown
## Source and Provenance

### Source Notes

TBD

### Provenance Notes

TBD

### Transformation Notes

TBD

### Evidence and Support Notes

TBD
```

### 8.1 Source Notes

Source Notes SHOULD explain what Source Material was used, referenced, summarized, interpreted, extracted, contradicted, compared, or transformed.

Source Notes SHOULD point back to the `source_refs` metadata field when source references are available.

Source Notes MUST NOT be treated as a substitute for governed source references when source references are required.

Example:

```markdown
### Source Notes

- Source reference: TBD
- Source role: TBD
- Source location or pointer: TBD
- Source relevance: TBD
```

### 8.2 Provenance Notes

Provenance Notes SHOULD explain how the Knowledge Record came into existence.

Provenance Notes MAY include origin context, human creator context, agent assistance context, workflow context, transformation context, import context, migration context, validation context, review context, or maintenance context.

Provenance Notes SHOULD remain consistent with the `provenance` metadata field.

Provenance Notes MUST NOT hide agent assistance, source transformation, unresolved uncertainty, or review requirements.

Example:

```markdown
### Provenance Notes

- Record origin: TBD
- Created by: TBD
- Created through: TBD
- Agent assistance used: TBD
- Human review status: TBD
```

### 8.3 Transformation Notes

Transformation Notes SHOULD be used when Source Material has been summarized, extracted, interpreted, converted, translated, migrated, reformatted, merged, split, or otherwise transformed into a Knowledge Record.

Transformation Notes SHOULD clarify whether the Knowledge Record is a direct extraction, summary, interpretation, derivative record, maintenance update, imported record, migrated record, or human-authored synthesis.

Example:

```markdown
### Transformation Notes

- Transformation type: TBD
- What changed from the source: TBD
- What was preserved from the source: TBD
- What may require review: TBD
```

### 8.4 Evidence and Support Notes

Evidence and Support Notes SHOULD explain how strongly the Source Material supports the Knowledge Record.

Evidence and Support Notes MAY identify supporting evidence, weak evidence, conflicting evidence, missing evidence, uncertain interpretation, or review needs.

Evidence and Support Notes MUST NOT convert unsupported claims into validated knowledge.

Example:

```markdown
### Evidence and Support Notes

- Supported by source: TBD
- Requires additional source support: TBD
- Conflicts or uncertainty: TBD
- Review needed: TBD
```

## 9. Relationships and Review Section

A Knowledge Record SHOULD include a Relationships and Review section when the record has known, proposed, uncertain, or review-relevant connections to other Knowledge Objects, Knowledge Records, Source Material, standards, workflows, reviews, agent activity, implementations, decisions, or downstream uses.

This section supports human and agent inspection.

It does not replace the `relationships` metadata field.

It does not replace governed relationship records.

It does not replace review records.

It does not replace validation records.

It does not approve relationships by itself.

A Relationships and Review section SHOULD use the following practical structure where applicable:

```markdown
## Relationships and Review

### Relationship Notes

TBD

### Review Notes

TBD

### Validation Notes

TBD

### Downstream Use Notes

TBD
```

### 9.1 Relationship Notes

Relationship Notes SHOULD identify known or proposed relationships involving the Knowledge Record.

Relationship Notes MAY include relationships to Source Material, related Knowledge Records, parent concepts, child concepts, supporting records, conflicting records, duplicate candidates, superseding records, deprecated records, workflows, standards, implementation notes, review records, or agent activity records.

Relationship Notes MUST distinguish confirmed governed relationships from proposed, suspected, inferred, or agent-suggested relationships.

Relationship Notes MUST NOT treat backlinks, tags, search similarity, graph placement, folder proximity, or agent suggestions as approved relationships by default.

Example:

```markdown
### Relationship Notes

- Related object or record: TBD
- Relationship reason: TBD
- Relationship status or handling: TBD
- Review needed: TBD
```

### 9.2 Review Notes

Review Notes SHOULD identify what human review is needed, who is assigned where known, and what review questions remain unresolved.

Review Notes SHOULD remain consistent with `review_required`, `human_reviewer`, and `review_refs`.

Review Notes MUST NOT replace a review record when a review record is required.

Review Notes MUST NOT imply that review has been completed merely because a reviewer is named.

Example:

```markdown
### Review Notes

- Review required: TBD
- Human reviewer: TBD
- Review question: TBD
- Review outcome reference: TBD
```

### 9.3 Validation Notes

Validation Notes SHOULD identify whether the record has been checked for structure, metadata completeness, source support, relationship handling, provenance completeness, privacy handling, authority handling, lifecycle handling, or downstream-use readiness.

Validation Notes SHOULD remain consistent with `validation_state`.

Validation Notes MUST NOT treat structural completeness as validation approval.

Validation Notes MUST NOT treat validation as publication approval, export approval, migration approval, or downstream-use approval.

Example:

```markdown
### Validation Notes

- Validation state: TBD
- Validation checks performed: TBD
- Validation gaps: TBD
- Repair needed: TBD
```

### 9.4 Downstream Use Notes

Downstream Use Notes SHOULD identify whether the Knowledge Record is intended for later publication, export, migration, automation, agent use, implementation use, reporting, research, decision support, or other downstream handling.

Downstream Use Notes SHOULD identify privacy, authority, validation, review, or source-support limits that may affect downstream use.

Downstream Use Notes MUST NOT declare the record downstream-use-ready unless the applicable governed workflow, validation, privacy, authority, lifecycle, and review requirements have been satisfied.

Example:

```markdown
### Downstream Use Notes

- Intended downstream use: TBD
- Restrictions or limits: TBD
- Required review before use: TBD
- Required validation before use: TBD
```

## 10. Agent-Assisted Record Instructions

A Knowledge Record MAY be created, drafted, reviewed, enriched, repaired, or maintained with agent assistance when the agent operates within authorized boundaries.

Agent assistance does not make a Knowledge Record approved, authoritative, validated, publication-ready, export-ready, migration-ready, or downstream-use-ready.

Agent assistance MUST remain visible when it materially affects the Knowledge Record.

If an agent materially assists with the Knowledge Record, the metadata field SHOULD be set to:

```yaml
agent_assisted: true
```

If an agent activity record exists, the metadata field SHOULD include a reference to that activity record:

```yaml
agent_activity_refs:
  - AG-ACT-0000
```

Agent activity references SHOULD point to records created under TEMPLATE-0003 where applicable.

TEMPLATE-0001 does not replace TEMPLATE-0003.

TEMPLATE-0001 MAY summarize agent assistance inside the Knowledge Record, but the agent activity record remains the proper place to preserve detailed agent actions, inputs, outputs, permissions, limitations, and traceability.

### 10.1 Permitted Agent Assistance

An authorized agent MAY assist with:

- reading Source Material;
- summarizing Source Material;
- extracting knowledge from Source Material;
- drafting Knowledge Content;
- suggesting metadata values;
- suggesting Source References;
- suggesting provenance notes;
- suggesting relationships;
- identifying duplicate candidates;
- identifying uncertainty;
- identifying missing source support;
- identifying privacy concerns;
- identifying validation gaps;
- preparing review notes;
- preparing repair suggestions;
- preparing downstream-use warnings.

Agent suggestions MUST remain reviewable.

Agent suggestions MUST NOT be treated as approved merely because they are included in the Knowledge Record.

### 10.2 Prohibited Agent Authority

An agent MUST NOT independently:

- assign final Object Identity;
- merge Knowledge Objects;
- split Knowledge Objects;
- approve lifecycle transitions;
- assign final Authority Level;
- reduce Privacy Classification;
- approve Validation State;
- complete human review;
- approve publication;
- approve export;
- approve migration;
- approve downstream use;
- delete governed material;
- suppress uncertainty;
- hide source limitations;
- hide agent involvement;
- treat inferred relationships as approved relationships;
- treat structural completeness as validation approval.

Agent activity MUST remain subordinate to the applicable standards, specifications, workflows, review requirements, and human authority.

### 10.3 Agent Assistance Notes

When agent assistance materially affects a Knowledge Record, the record SHOULD include an Agent Assistance Notes section.

The Agent Assistance Notes section supports inspection.

It does not replace the `agent_assisted` metadata field.

It does not replace `agent_activity_refs`.

It does not replace provenance.

It does not replace review.

It does not grant agent authority.

A practical Agent Assistance Notes section MAY use the following structure:

```markdown
## Agent Assistance Notes

- Agent role or function: TBD
- Agent actions performed: TBD
- Metadata fields suggested or modified: TBD
- Source references suggested or modified: TBD
- Provenance notes suggested or modified: TBD
- Relationships suggested or modified: TBD
- Validation gaps identified: TBD
- Privacy concerns identified: TBD
- Human review required: TBD
- Agent activity reference: TBD
```

### 10.4 Agent Uncertainty Handling

Agents MUST preserve uncertainty when uncertainty exists.

An agent SHOULD mark content, metadata, relationships, source references, provenance notes, validation notes, or review notes as uncertain when the agent cannot determine them reliably.

An agent MUST NOT fill uncertain fields with confident language merely to make the record appear complete.

When uncertainty exists, the Knowledge Record SHOULD preserve that uncertainty in one or more of the following locations:

- `summary`;
- `source_refs`;
- `provenance`;
- `relationships`;
- `review_required`;
- `human_reviewer`;
- `agent_activity_refs`;
- Limits, Uncertainty, and Open Questions;
- Source and Provenance;
- Relationships and Review;
- Agent Assistance Notes.

### 10.5 Agent Source Handling

An agent MUST NOT invent Source References.

An agent MUST distinguish between source-supported content, inferred content, summarized content, interpreted content, transformed content, and unsupported draft content.

If an agent uses Source Material, the Knowledge Record SHOULD preserve enough source context for a human reviewer to inspect the source relationship.

If an agent cannot verify a source, the agent SHOULD mark the source support as uncertain rather than treating the source as confirmed.

### 10.6 Agent Review Routing

When agent assistance creates or modifies a Knowledge Record, the record SHOULD remain review-required unless an applicable workflow and human review process determine otherwise.

Agent-created or agent-modified records SHOULD be routed for human review when they affect:

- Object Identity;
- metadata;
- Source References;
- provenance;
- relationships;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- publication readiness;
- export readiness;
- migration readiness;
- downstream-use readiness.

## 11. Validation and Completion Checklist

This checklist is an operational completion aid for TEMPLATE-0001.

It does not replace VALID-0001.

It does not define the full validation standard.

It does not approve the Knowledge Record.

It helps humans, agents, workflows, validators, and implementations determine whether a Knowledge Record is ready for review or further validation.

A Knowledge Record may pass this checklist and still remain draft, unreviewed, private, not validated, not authoritative, not approved, not publishable, not export-ready, not migration-ready, or not ready for downstream use.

### 11.1 Metadata Checklist

Before a Knowledge Record is treated as structurally complete, confirm that:

- [ ] `object_id` is present.
- [ ] `record_id` is present.
- [ ] `record_type` is present.
- [ ] `title` is present.
- [ ] `summary` is present.
- [ ] `lifecycle_state` is present.
- [ ] `authority_level` is present.
- [ ] `privacy_classification` is present.
- [ ] `validation_state` is present.
- [ ] `source_refs` is present.
- [ ] `provenance` is present.
- [ ] `relationships` is present.
- [ ] `created` is present.
- [ ] `updated` is present.
- [ ] `review_required` is present.
- [ ] `agent_assisted` is present.
- [ ] `human_reviewer` is present.

### 11.2 Field Boundary Checklist

Before a Knowledge Record is treated as ready for review, confirm that:

- [ ] Object Identity is not replaced by title, filename, folder path, alias, tag, application identifier, implementation identifier, workflow identifier, or agent identifier.
- [ ] Lifecycle State is not confused with Authority Level.
- [ ] Lifecycle State is not confused with Privacy Classification.
- [ ] Lifecycle State is not confused with Validation State.
- [ ] Authority Level is not treated as approval unless review supports it.
- [ ] Privacy Classification is not reduced without review.
- [ ] Validation State is not treated as approval.
- [ ] Source References remain distinct from provenance.
- [ ] Relationships remain distinct from backlinks, tags, search similarity, folder proximity, graph placement, and agent suggestions.

### 11.3 Body Checklist

Before a Knowledge Record is treated as usable, confirm that:

- [ ] The body is distinguishable from the metadata block.
- [ ] The body is distinguishable from raw Source Material.
- [ ] The Record Summary is consistent with the metadata summary.
- [ ] The Knowledge Content is clear enough for human review.
- [ ] Context and Scope are included where needed.
- [ ] Key Details are included where useful.
- [ ] Limits, Uncertainty, and Open Questions are included where uncertainty exists.
- [ ] The body does not redefine standards, specifications, metadata fields, relationships, validation, review, or authority.

### 11.4 Source and Provenance Checklist

Before a Knowledge Record is treated as source-aware, confirm that:

- [ ] Source Notes are included where Source Material applies.
- [ ] Source Notes align with `source_refs`.
- [ ] Provenance Notes are included where origin, creation, transformation, workflow, human, agent, import, migration, validation, review, or maintenance context matters.
- [ ] Provenance Notes align with `provenance`.
- [ ] Transformation Notes are included where material was summarized, extracted, interpreted, converted, translated, migrated, reformatted, merged, split, or otherwise transformed.
- [ ] Evidence and Support Notes are included where source support may be weak, conflicting, incomplete, or uncertain.
- [ ] Unsupported claims are not treated as validated knowledge.

### 11.5 Relationship and Review Checklist

Before a Knowledge Record is treated as review-ready, confirm that:

- [ ] Relationship Notes identify known or proposed relationships where applicable.
- [ ] Proposed relationships are clearly distinguished from confirmed governed relationships.
- [ ] Review Notes identify whether review is required.
- [ ] Review Notes align with `review_required`.
- [ ] Review Notes align with `human_reviewer`.
- [ ] Review Notes align with `review_refs` where review references exist.
- [ ] Validation Notes align with `validation_state`.
- [ ] Downstream Use Notes identify publication, export, migration, automation, agent-use, implementation-use, or other downstream limits where applicable.

### 11.6 Agent Traceability Checklist

Before an agent-assisted Knowledge Record is treated as review-ready, confirm that:

- [ ] `agent_assisted` is set correctly.
- [ ] `agent_activity_refs` is populated where an agent activity record exists.
- [ ] Agent Assistance Notes are included where agent assistance materially affected the record.
- [ ] Agent uncertainty is preserved.
- [ ] Agent source limitations are preserved.
- [ ] Agent-suggested metadata remains reviewable.
- [ ] Agent-suggested relationships remain reviewable.
- [ ] Agent-suggested validation findings remain reviewable.
- [ ] Agent assistance is not treated as approval.

### 11.7 Completion Statement

A Knowledge Record created from TEMPLATE-0001 SHOULD include a completion statement when it is ready for review.

The completion statement SHOULD identify whether the record is structurally complete, what remains unresolved, and what review or validation is still required.

Example:

```markdown
## Completion Statement

This Knowledge Record is structurally complete for draft review.

Remaining issues:

- TBD
- TBD
- TBD

Required next action:

- TBD
```

## 12. Template Success Criteria

TEMPLATE-0001 succeeds when it allows a human, agent, workflow, validator, or implementation to create a Knowledge Record that is usable without bypassing The Brain Standard.

A successful Knowledge Record created from TEMPLATE-0001 is:

- human-readable;
- AI-readable;
- Markdown-compatible;
- implementation-independent;
- structurally consistent;
- metadata-aware;
- identity-safe;
- source-aware where applicable;
- provenance-aware;
- relationship-aware;
- lifecycle-aware;
- authority-aware;
- privacy-aware;
- validation-aware;
- reviewable;
- agent-traceable where applicable;
- compatible with future maintenance;
- compatible with future migration;
- compatible with governed downstream use.

### 12.1 Success Conditions

A Knowledge Record created from TEMPLATE-0001 is successful when:

- the SC-0001 metadata field names are preserved;
- Object Identity remains distinct from title, filename, folder path, alias, tag, application identifier, implementation identifier, workflow identifier, and agent identifier;
- metadata remains distinct from body content;
- body content remains distinct from raw Source Material;
- Source References remain distinct from provenance;
- relationships remain explicit and governed;
- Lifecycle State remains distinct from Authority Level, Privacy Classification, Validation State, workflow state, agent state, storage state, and implementation state;
- review requirements remain visible;
- validation status remains visible;
- privacy handling remains visible;
- agent assistance remains visible where used;
- uncertainty remains visible where present;
- downstream-use limits remain visible where applicable.

### 12.2 Failure Conditions

A Knowledge Record created from TEMPLATE-0001 fails when:

- the template is used to redefine SC-0001 metadata fields;
- the template is used to bypass higher-authority standards;
- Object Identity is replaced by title, filename, folder path, alias, tag, application identifier, implementation identifier, workflow identifier, or agent identifier;
- Source References are replaced by informal notes when governed source references are required;
- provenance is omitted or hidden when provenance is required;
- backlinks, tags, search similarity, graph placement, folder proximity, or agent suggestions are treated as approved relationships by default;
- structural completeness is treated as validation approval;
- agent assistance is hidden;
- human review is bypassed;
- privacy classification is reduced without review;
- a draft record is treated as authoritative without approval;
- a private record is treated as publishable without privacy review;
- a record is treated as export-ready, migration-ready, or downstream-use-ready without the applicable workflow, validation, privacy, authority, lifecycle, and review requirements.

### 12.3 Final Use Rule

TEMPLATE-0001 provides a practical Knowledge Record structure.

It does not create authority.

It does not complete review.

It does not complete validation.

It does not approve publication.

It does not approve export.

It does not approve migration.

It does not approve downstream use.

A Knowledge Record created from TEMPLATE-0001 remains governed by the standards, specifications, workflows, validation rules, review requirements, privacy requirements, authority requirements, lifecycle requirements, and implementation constraints that apply to it.

### 12.4 Template Completion Criteria

TEMPLATE-0001 is complete when it provides:

- a clear purpose;
- a clear relationship to SC-0001 and prior standards;
- clear scope and use rules;
- a copy/paste-ready metadata block;
- required field instructions;
- recommended field instructions;
- a practical body structure;
- source and provenance handling;
- relationship and review handling;
- agent-assisted record instructions;
- a validation and completion checklist;
- success criteria.

When all twelve sections are present and structurally valid, TEMPLATE-0001 is ready for final review.