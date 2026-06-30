# SC-0001 — Knowledge Record Metadata Field Specification

Document ID: SC-0001
Title: Knowledge Record Metadata Field Specification
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Specification
Phase: Bare Usable Operational Bootstrap Layer
Milestone: Operational Bootstrap 1.1 — Knowledge Record Metadata Field Specification
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard
Supersedes: None
Superseded By: None
Related: TEMPLATE-0001 — Knowledge Record Template; TEMPLATE-0002 — Source Material Intake Template; TEMPLATE-0003 — Agent Activity Record Template; TEMPLATE-0004 — Review Record Template; VALID-0001 — Bare Usable Validation Checklist; AG-SPEC-0001 — Agent Initialization Packet; AG-SPEC-0002 — Subagent Prompt and Role Profile Specification; WF-SPEC-0001 — Controlled Ingestion Runbook

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and metadata-field rules are interpreted within SC-0001.

Where conflicts arise between metadata field names, metadata field values, Knowledge Records, Object Identity, Source Material, Source References, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation State, agent activity, workflow outputs, storage behavior, implementation behavior, import behavior, export behavior, migration behavior, or future specifications, the constitutional foundation and higher-authority standards SHALL guide interpretation and resolution.

SC-0001 is subordinate to TB-0000, TB-0001, TB-0002, TB-0003, and all applicable approved standards.

SC-0001 defines exact metadata field names and field expectations for Knowledge Records at the specification level.

SC-0001 does not redefine knowledge meaning, Object Identity, metadata meaning, relationship behavior, source-reference behavior, provenance behavior, lifecycle-state behavior, authority behavior, privacy behavior, validation behavior, agent authority, workflow authority, storage meaning, or implementation compliance.

Those meanings remain governed by the applicable standards.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Specification refers to a governed lower-level document that defines exact structures, schemas, formats, fields, values, validation expectations, or technical requirements under higher-authority standards.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Metadata Field refers to a named metadata element used to express required, recommended, optional, operational, validation, source-reference, provenance, relationship, lifecycle, authority, privacy, compatibility, or agent-assistance information about a Knowledge Record.
- Field Name refers to the exact identifier used for a metadata field.
- Field Value refers to the content assigned to a metadata field.
- Required Field refers to a metadata field that MUST be present for a Knowledge Record to satisfy this specification.
- Recommended Field refers to a metadata field that SHOULD be present when practical because it improves interpretation, reviewability, validation, portability, source traceability, agent reliability, workflow routing, or long-term maintainability.
- Optional Field refers to a metadata field that MAY be used when relevant but is not required for basic Knowledge Record validity unless another governed specification, workflow, object type, implementation profile, or validation profile requires it.
- Conditional Field refers to a metadata field that becomes required only when a defined condition applies.
- Allowed Value refers to a value permitted by this specification or by a future governed vocabulary, profile, or specification.
- Placeholder Value refers to a temporary value used when information is unknown, pending, unavailable, not applicable, or awaiting review.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Source Reference refers to a traceable reference from a Knowledge Record or other governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Record or related governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a Knowledge Record within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a Knowledge Record.
- Validation State refers to the current validation status of a Knowledge Record within a defined validation scope.
- Agent-Assisted Record refers to a Knowledge Record whose creation, extraction, summarization, metadata proposal, relationship proposal, validation check, or review preparation involved an agent.
- Human Review refers to review performed by a human to confirm, correct, reject, approve, limit, escalate, or route governed entities where human judgment is required.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of SC-0001 is to define the exact metadata field names and minimum field expectations used by Knowledge Records within The Brain Standard.

SC-0001 translates the conceptual metadata requirements defined by the Knowledge Standards into a practical field specification that humans, agents, validators, templates, workflows, storage systems, and implementations can use consistently.

SC-0001 exists because the approved standards define metadata meaning at the conceptual standard level but do not define the exact field names, field order, field values, placeholder values, validation expectations, or template-ready metadata structure needed for bare usable deployment.

This specification provides that operational bridge.

SC-0001 defines the minimum metadata field set needed for a Knowledge Record to remain:

- identifiable;
- human-readable;
- AI-readable;
- source-aware;
- provenance-aware;
- relationship-aware;
- lifecycle-aware;
- authority-aware;
- privacy-aware;
- validation-aware;
- reviewable;
- portable;
- implementation-independent;
- compatible with controlled agent assistance.

SC-0001 is intended to support the first practical creation of Draft Knowledge Records through controlled ingestion, template use, validation checks, and human review.

SC-0001 is not intended to finalize every future metadata field that The Brain Standard may ever support.

Future specifications MAY define additional fields, object-type-specific fields, relationship-specific fields, source-reference fields, validation profiles, import fields, export fields, migration fields, implementation mappings, serialization profiles, or automation fields.

Such future specifications are valid only when they preserve the field meanings and governance boundaries established by SC-0001 and the higher-authority standards.

SC-0001 is successful when a future human, agent, workflow, validator, storage system, or implementation can open a Knowledge Record and determine:

- what Knowledge Object the record represents;
- what the record is called;
- what type of record it is;
- what lifecycle state applies;
- what authority level applies;
- what privacy classification applies;
- what validation state applies;
- what source material supports the record;
- what provenance applies;
- what relationships are proposed or established;
- whether agent assistance occurred;
- whether human review is required;
- whether the record may be used, routed, repaired, reviewed, approved, rejected, archived, exported, migrated, published, or withheld.

## 2. Relationship to Prior Standards

SC-0001 is subordinate to and derived from the constitutional foundation and the approved Knowledge, Storage, Agent, and Workflow Standards.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

SC-0001 supports that mission by defining Knowledge Record fields in a way that remains readable, portable, inspectable, and usable across tools without making any single tool, vault, database, model, or runtime the standard.

TB-0001 establishes the architecture principles that require knowledge integrity, implementation independence, portability, human and AI usability, explicit structure, governed evolution, and practical daily usability.

SC-0001 applies those principles by making meaning-critical Knowledge Record metadata explicit rather than hidden in folder placement, filenames, tags, application state, plugin behavior, agent memory, workflow memory, or undocumented convention.

TB-0002 establishes the layered architecture of The Brain Standard.

SC-0001 belongs to the specification layer that supports practical use of the Universal Knowledge Standard without redefining the standard itself.

SC-0001 depends on Layer 1 Knowledge Standards for field meaning.

SC-0001 depends on Layer 2 Storage Standards because metadata fields must remain meaningful when files are moved, renamed, copied, archived, imported, exported, migrated, backed up, synchronized, or represented through different storage systems.

SC-0001 depends on Layer 3 Agent Standards because agents may propose, populate, validate, or report on metadata fields only within governed boundaries.

SC-0001 depends on Layer 4 Workflow Standards because workflows may create, route, review, approve, reject, repair, quarantine, archive, maintain, export, or publish Knowledge Records based on field values without allowing workflow convenience to redefine field meaning.

TB-0003 establishes governance, authority hierarchy, review expectations, document lifecycle states, and drift-prevention rules.

SC-0001 follows that hierarchy as a Specification.

SC-0001 may define exact field names and field expectations, but it MUST NOT override the higher-authority standards that define the meaning of Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, agent boundaries, or workflow behavior.

KS-0001 defines the Knowledge Object Model and establishes that Knowledge Records require explicit structure sufficient to preserve identity, meaning, source distinction, provenance, relationships, lifecycle state, authority, privacy classification, validation expectations, portability, and reviewability.

SC-0001 makes those expectations usable by defining exact Knowledge Record metadata fields.

KS-0002 defines Object Identity.

SC-0001 preserves that standard by defining fields that reference or support Object Identity without allowing filenames, folder paths, titles, aliases, tags, implementation IDs, or temporary identifiers to replace Stable Object Identity.

KS-0003 defines metadata at the conceptual standard level.

SC-0001 extends KS-0003 by defining exact metadata field names, practical field expectations, and template-ready metadata structure for Knowledge Records.

KS-0004 defines relationship behavior.

SC-0001 supports KS-0004 by defining fields where relationships can be identified, proposed, reviewed, and preserved without confusing backlinks, inferred similarity, folder proximity, or agent suggestions with governed relationships.

KS-0005 defines Source Reference and provenance behavior.

SC-0001 supports KS-0005 by defining fields that preserve source references, source support, provenance, extraction context, transformation context, agent involvement, human review, and source distinction.

KS-0006 defines Lifecycle State behavior.

SC-0001 supports KS-0006 by defining the field used to express Knowledge Record lifecycle state while keeping lifecycle state distinct from authority, validation, privacy, workflow state, agent state, implementation state, and storage location.

KS-0007 defines Authority Level behavior.

SC-0001 supports KS-0007 by defining the field used to express authority level while keeping authority distinct from lifecycle state, validation state, agent confidence, source popularity, workflow completion, or implementation visibility.

KS-0008 defines Privacy Classification behavior.

SC-0001 supports KS-0008 by defining the field used to express privacy classification so that access, exposure, indexing, synchronization, export, publication, backup, agent access, workflow access, and downstream use remain governed.

KS-0009 defines Validation behavior.

SC-0001 supports KS-0009 by defining the field used to express validation state and related validation expectations while preserving the rule that validation does not automatically equal approval, authority, privacy permission, publication permission, export permission, or downstream-use permission.

AG-0001 defines agent operating boundaries.

SC-0001 supports AG-0001 by defining fields that allow agent-assisted work to remain traceable, reviewable, scoped, and distinguishable from approved human or governed decisions.

WF-0001 defines Knowledge Ingestion behavior.

SC-0001 supports WF-0001 by defining the fields needed when Source Material is transformed into a Draft Knowledge Record through controlled ingestion.

WF-0002 defines Review and Approval behavior.

SC-0001 supports WF-0002 by defining fields that make review requirement, review status, reviewer responsibility, and approval boundaries visible.

## 3. Specification Scope and Boundaries

SC-0001 defines exact metadata field names and field expectations for Knowledge Records.

SC-0001 applies to Knowledge Records created by:

- humans;
- agents;
- workflows;
- ingestion processes;
- maintenance processes;
- review processes;
- import processes;
- migration processes;
- implementation-supported drafting;
- future governed processes that create or revise Knowledge Records.

SC-0001 defines metadata fields for the default Knowledge Record form used during bare usable deployment.

SC-0001 governs metadata fields used by TEMPLATE-0001 — Knowledge Record Template.

SC-0001 also provides field expectations that may be referenced by validation checklists, controlled ingestion runbooks, agent initialization packets, subagent role profiles, review records, source intake records, implementation profiles, and future conformance tools.

SC-0001 defines:

- required Knowledge Record metadata fields;
- recommended Knowledge Record metadata fields;
- optional Knowledge Record metadata fields;
- conditional Knowledge Record metadata fields;
- field naming rules;
- field value expectations;
- placeholder value expectations;
- implementation-independent representation expectations;
- agent-handling expectations;
- review-handling expectations;
- validation expectations;
- compatibility expectations.

SC-0001 does not define the full content body of a Knowledge Record.

The Knowledge Record content body is defined by TEMPLATE-0001 and future object-type-specific templates or specifications.

SC-0001 does not define a complete object-type vocabulary.

A minimal record_type field is defined for bootstrap use, but future object-type specifications MAY define expanded values, type-specific metadata, or type-specific templates.

SC-0001 does not define a complete relationship vocabulary.

Relationship metadata fields are defined for bootstrap use, but future relationship specifications MAY define approved relationship types, directionality rules, cardinality rules, graph structures, relationship identifiers, relationship confidence rules, and relationship validation behavior.

SC-0001 does not define a complete source-reference or citation format.

Source-reference fields are defined for bootstrap use, but future source-reference specifications MAY define exact source identifiers, citation formats, archival formats, source availability values, source reliability values, attribution formats, and extraction records.

SC-0001 does not define a complete validation engine.

Validation fields are defined for bootstrap use, but future validation specifications MAY define validation profiles, rule syntax, error codes, warning formats, automated validators, conformance tests, or implementation mappings.

SC-0001 does not define exact storage placement.

Storage layout, source material placement, draft placement, archive placement, implementation-support placement, export placement, and migration placement remain governed by storage standards and later storage specifications.

SC-0001 does not define exact agent prompts.

Agents may use SC-0001 to populate, inspect, validate, or propose metadata fields, but prompts, role profiles, tool permissions, runtime behavior, and handoff procedures belong to agent specifications and operational guides.

SC-0001 does not define final approval authority.

A Knowledge Record that satisfies SC-0001 field requirements may still be Draft, Pending Review, Needs Repair, Quarantined, Rejected, Archived, or otherwise not approved.

Field completeness does not equal approval.

Validation success does not equal approval.

Agent confidence does not equal approval.

Workflow completion does not equal approval.

Storage placement does not equal approval.

Implementation visibility does not equal approval.

SC-0001 does not make any implementation mandatory.

A compliant implementation MAY represent SC-0001 metadata fields through Markdown front matter, document headers, structured fields, sidecar metadata, database fields, graph properties, API objects, or future governed representation formats.

For bare usable deployment, Markdown-compatible metadata is RECOMMENDED because it remains human-readable, AI-readable, portable, inspectable, and easy to validate.

Regardless of representation method, field meaning MUST remain explicit, portable, reviewable, and governed by this specification and higher-authority standards.

## 4. Metadata Representation Model

SC-0001 defines metadata fields as implementation-independent named fields.

A compliant Knowledge Record MAY represent SC-0001 metadata through different technical formats, provided that field meaning remains explicit, inspectable, portable, and governed.

For bare usable deployment, the RECOMMENDED representation is Markdown-compatible front matter because it is:

- human-readable;
- AI-readable;
- plain-text compatible;
- easy to inspect without specialized tooling;
- easy to copy, migrate, validate, and version;
- compatible with many note-taking, repository, documentation, and automation environments.

The recommended Markdown-compatible representation uses a field-name and field-value structure.

Example representation pattern:

```yaml
field_name: field_value
```

SC-0001 does not require YAML specifically.

A compliant implementation MAY represent the same fields through:

- Markdown front matter;
- Markdown tables;
- document headers;
- sidecar metadata files;
- structured JSON;
- database fields;
- graph properties;
- API objects;
- implementation-specific field mappings;
- future governed metadata formats.

The representation format does not define the meaning of the field.

Field meaning is defined by SC-0001 and the higher-authority standards.

A metadata representation is compliant only if a future human, agent, workflow, validator, storage system, import process, export process, migration process, or implementation can determine:

- the exact field name;
- the field value;
- whether the field is required, recommended, optional, or conditional;
- what governed meaning the field carries;
- whether the value is known, unknown, pending, unavailable, not applicable, or awaiting review;
- whether the value was assigned by a human, agent, workflow, import process, migration process, or implementation;
- whether the value affects identity, provenance, relationships, lifecycle state, authority, privacy, validation, workflow routing, agent handling, export, publication, migration, or downstream use.

Metadata fields MUST NOT depend only on:

- folder placement;
- filename;
- tags;
- visual formatting;
- user-interface state;
- plugin behavior;
- database internals;
- search ranking;
- graph position;
- backlink behavior;
- agent memory;
- workflow memory;
- undocumented implementation conventions.

Those signals MAY support usability, discovery, routing, or automation.

They MUST NOT replace explicit metadata fields where the field affects governed meaning, validation, review, authority, privacy, provenance, relationship handling, lifecycle handling, publication, export, migration, or downstream use.

A compliant implementation SHOULD preserve SC-0001 field names during export and migration when practical.

If an implementation must map SC-0001 fields to another representation, the mapping SHOULD be documented and reviewable.

A field mapping MUST NOT silently collapse, rename, reinterpret, discard, hide, or replace SC-0001 fields in a way that causes:

- identity confusion;
- source-reference loss;
- provenance loss;
- relationship ambiguity;
- lifecycle-state confusion;
- authority confusion;
- privacy exposure;
- validation failure;
- review failure;
- workflow routing error;
- agent permission confusion;
- export ambiguity;
- migration loss;
- governance drift.

## 5. Field Requirement Levels

SC-0001 uses four field requirement levels:

- Required;
- Recommended;
- Optional;
- Conditional.

A Required Field MUST be present in every Knowledge Record unless a future governed specification explicitly defines a narrower exception.

A Recommended Field SHOULD be present when practical because it improves interpretation, reviewability, portability, validation, workflow routing, agent reliability, maintenance, import, export, migration, or downstream use.

An Optional Field MAY be included when useful but is not required for basic Knowledge Record conformance unless another governed specification, object-type rule, implementation profile, workflow, validator, or template requires it.

A Conditional Field becomes required when a defined condition applies.

Examples of conditional field behavior include:

- if an agent assisted with the record, agent-related fields become required;
- if Source Material supports the record, source-reference fields become required;
- if the record was imported, import-provenance fields become required;
- if the record was migrated, migration-provenance fields become required;
- if the record is reviewed, review-related fields become required;
- if the record is approved, approval-scope fields become required;
- if privacy restrictions apply, privacy-scope or handling fields become required;
- if relationships are proposed or established, relationship fields become required;
- if validation has been performed, validation-result fields become required.

A field being required does not mean the final value is known.

When a required value is not yet known, the field MUST still be present with an approved placeholder value.

Placeholder values preserve structure and make missing information visible.

A missing required field creates a structural validation issue.

A present field with a placeholder value creates a review or completion issue unless the placeholder value is permitted for the record’s lifecycle state and validation scope.

Field requirement levels do not determine approval.

A Knowledge Record may contain all required fields and still remain Draft, Pending Review, Needs Repair, Quarantined, Rejected, Archived, Deprecated, Superseded, or otherwise not approved.

Field completeness does not equal approval.

Validation success does not equal approval.

Agent completion does not equal approval.

Workflow completion does not equal approval.

Storage placement does not equal approval.

Implementation visibility does not equal approval.

Field requirement levels are intended to make Knowledge Records easier to validate, review, route, repair, migrate, export, and maintain.

They are not intended to make metadata burdensome or excessive.

SC-0001 SHOULD require only fields that materially improve identity preservation, interpretation, source traceability, provenance, relationship clarity, lifecycle handling, authority handling, privacy protection, validation, reviewability, portability, agent reliability, workflow reliability, compatibility, or long-term maintainability.

## 6. Field Naming Rules

SC-0001 field names MUST be stable, explicit, readable, and implementation-independent.

Field names SHOULD use lowercase snake_case.

Example:

```yaml
object_id: TBD
record_type: concept
lifecycle_state: draft
```

Field names MUST be written consistently across templates, validation checklists, agent instructions, workflow runbooks, implementation profiles, import mappings, export mappings, migration mappings, and future specifications unless a governed revision changes the field name.

Field names SHOULD be concise but not cryptic.

A field name SHOULD clearly indicate the kind of information the field contains.

Preferred examples:

```yaml
object_id
record_type
lifecycle_state
authority_level
privacy_classification
validation_state
source_refs
created
updated
review_required
agent_assisted
```

Avoid unclear or overly broad names such as:

```yaml
id
type
state
status
refs
notes
flag
data
misc
```

Broad field names MAY appear in implementation-specific contexts, but they SHOULD NOT be used as governed SC-0001 field names where they could cause ambiguity.

A field name MUST NOT imply authority that the field does not have.

For example:

```yaml
approved: true
```

SHOULD NOT be used as the primary authority or lifecycle control field because it may confuse review state, approval scope, lifecycle state, validation state, and authority level.

Instead, SC-0001 SHOULD use explicit fields such as:

```yaml
lifecycle_state: approved
authority_level: governed
review_required: false
human_reviewer: reviewer_name_or_id
```

A field name MUST NOT make an implementation the standard.

Avoid implementation-specific field names such as:

```yaml
obsidian_status
notion_database_id
codex_state
plugin_tags
```

unless the field is clearly marked as implementation-specific metadata in a future implementation profile.

A field name MUST NOT make a workflow state, agent state, validation result, or storage location appear to be Object Identity.

For example:

```yaml
folder_id
draft_number
agent_record_id
validation_id
```

MUST NOT replace `object_id`.

A field name SHOULD remain useful across:

- file renaming;
- folder movement;
- storage reorganization;
- import;
- export;
- migration;
- backup;
- restoration;
- synchronization;
- indexing;
- agent processing;
- workflow processing;
- implementation replacement.

Field names defined by SC-0001 SHOULD NOT be changed casually.

A governed field-name change SHOULD include:

- rationale for the change;
- compatibility impact;
- migration impact;
- template impact;
- validator impact;
- workflow impact;
- agent impact;
- implementation impact;
- deprecated field handling where needed;
- review and approval under the applicable governance process.

A future specification MAY define aliases, legacy field mappings, deprecated field names, or implementation-specific mappings.

Such mappings MUST preserve the governed meaning of the SC-0001 field.

## 7. Placeholder Value Rules

Placeholder values exist so that required fields remain visible even when the final field value is not yet known, assigned, reviewed, approved, validated, or applicable.

A required metadata field MUST NOT be omitted merely because the correct value is unknown.

When a required value is not yet available, the field MUST remain present with an approved placeholder value.

Placeholder values make incomplete records easier to inspect, validate, route, repair, and review.

SC-0001 recognizes the following bootstrap placeholder values:

```yaml
TBD
unknown
not_applicable
pending_review
unassigned
none
[]
```

`TBD` means the value is required but has not yet been assigned.

`unknown` means the value may exist but cannot currently be determined from available information.

`not_applicable` means the field does not apply to the record in the current context.

`pending_review` means the value has been proposed, inferred, imported, generated, or assigned but has not yet completed required review.

`unassigned` means a human, agent, workflow, reviewer, validator, owner, or responsible actor has not yet been assigned.

`none` means the absence of a value has been intentionally recorded.

`[]` means the field is a list field and currently has no entries.

Placeholder values MUST be used consistently.

A placeholder value MUST NOT be used to hide uncertainty, avoid review, bypass validation, weaken privacy handling, avoid provenance, or imply approval.

A placeholder value MUST NOT be treated as equivalent to a confirmed value.

A Knowledge Record containing placeholder values MAY be valid as a Draft or Pending Review record.

A Knowledge Record containing placeholder values SHOULD NOT be treated as Approved unless the applicable workflow, validation profile, or approval scope explicitly permits those placeholders.

A placeholder value SHOULD trigger review when the field affects:

- Object Identity;
- record interpretation;
- source support;
- provenance;
- relationships;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- review routing;
- publication;
- export;
- migration;
- downstream use.

Placeholder values SHOULD remain machine-readable and human-readable.

Placeholder values SHOULD be written exactly as defined in this section unless a future governed specification revises them.

A future specification MAY define additional placeholder values, field-specific placeholder values, migration placeholder values, import placeholder values, validation placeholder values, relationship placeholder values, source-reference placeholder values, or implementation mappings.

Such future placeholder values MUST preserve the meaning, traceability, reviewability, and validation expectations defined by SC-0001.

## 8. Required Metadata Field Set

A bare usable Knowledge Record MUST include a minimum required metadata field set.

The required field set exists to ensure that every Knowledge Record remains identifiable, interpretable, source-aware, provenance-aware, lifecycle-aware, authority-aware, privacy-aware, validation-aware, reviewable, portable, and usable by humans, agents, workflows, validators, storage systems, and implementations.

The following metadata fields are REQUIRED for the default bare usable Knowledge Record:

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

The required field set is intentionally minimal for bare usable deployment.

It does not represent every field The Brain Standard may eventually support.

Future specifications MAY define additional fields for specialized object types, source-reference handling, relationship records, validation profiles, agent activity records, review records, import records, export records, migration records, publication records, implementation mappings, or downstream-use packages.

The required field set MUST remain present in TEMPLATE-0001 — Knowledge Record Template unless a future governed specification revises the template requirements.

A Knowledge Record missing one or more required fields has a structural validation issue.

A Knowledge Record with required fields present but populated with placeholder values may still require review, repair, validation, source inspection, privacy review, authority review, relationship review, or lifecycle review.

Required field presence does not equal approval.

Required field presence does not equal validation success.

Required field presence does not equal publication permission.

Required field presence does not equal export permission.

Required field presence does not equal migration readiness.

Required field presence does not equal downstream-use readiness.

The required field set is divided into the following metadata groups:

| Metadata Group                                         | Required Fields                                                                    | Purpose                                                                                                                                     |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Identity and descriptive metadata                      | `object_id`, `record_id`, `record_type`, `title`, `summary`                        | Identifies and describes the Knowledge Record and the Knowledge Object it represents.                                                       |
| Lifecycle, authority, privacy, and validation metadata | `lifecycle_state`, `authority_level`, `privacy_classification`, `validation_state` | Defines governed handling, trust boundary, access boundary, and validation status.                                                          |
| Source and provenance metadata                         | `source_refs`, `provenance`                                                        | Preserves source support, origin, transformation, authorship, agent involvement, workflow involvement, review context, or other provenance. |
| Relationship metadata                                  | `relationships`                                                                    | Preserves explicit proposed or established relationships to other governed entities.                                                        |
| Date and maintenance metadata                          | `created`, `updated`                                                               | Preserves basic creation and update context.                                                                                                |
| Review and agent metadata                              | `review_required`, `agent_assisted`, `human_reviewer`                              | Makes review need and agent involvement visible.                                                                                            |

The required field set SHOULD be represented near the top of the Knowledge Record where practical.

For Markdown-compatible records, the required field set SHOULD appear in front matter or another clearly marked metadata area.

Example:

```yaml
---
object_id: TBD
record_id: TBD
record_type: concept
title: Example Knowledge Record
summary: TBD
lifecycle_state: draft
authority_level: unreviewed
privacy_classification: private
validation_state: not_validated
source_refs: []
provenance: TBD
relationships: []
created: 2026-06-28
updated: 2026-06-28
review_required: true
agent_assisted: false
human_reviewer: unassigned
---
```

A compliant implementation MAY store the same fields outside Markdown front matter, but the required fields MUST remain explicit, inspectable, portable, and governed.

## 9. Identity and Descriptive Fields

Identity and descriptive fields identify the Knowledge Object, identify the Knowledge Record, classify the record at a basic level, and make the record understandable to humans and agents.

Identity and descriptive fields MUST preserve the distinction between:

- the Knowledge Object;
- the Knowledge Record;
- the title;
- the record type;
- aliases;
- summaries;
- keywords;
- filenames;
- folders;
- implementation identifiers;
- temporary identifiers.

Identity and descriptive metadata MUST NOT allow titles, filenames, folder paths, aliases, tags, search labels, graph labels, implementation IDs, or workflow IDs to replace stable Object Identity.

### 9.1 `object_id`

`object_id` is REQUIRED.

`object_id` identifies the Knowledge Object represented by the Knowledge Record.

The value of `object_id` MUST refer to stable Object Identity where stable Object Identity has already been assigned.

If stable Object Identity has not yet been assigned, `object_id` MUST be present with the placeholder value `TBD`.

Example:

```yaml
object_id: TBD
```

A Draft Knowledge Record MAY use `TBD` for `object_id`.

An Approved Knowledge Record SHOULD NOT use `TBD` for `object_id` unless a future governed specification explicitly allows that exception.

`object_id` MUST NOT be replaced by:

- filename;
- folder path;
- title;
- alias;
- tag;
- implementation ID;
- database row ID;
- plugin ID;
- workflow ID;
- agent ID;
- validation ID;
- import ID;
- export ID;
- migration ID.

Those identifiers MAY be recorded elsewhere when useful, but they do not replace `object_id`.

### 9.2 `record_id`

`record_id` is REQUIRED.

`record_id` identifies the specific Knowledge Record.

`record_id` is distinct from `object_id`.

A Knowledge Object may have one or more Knowledge Records over time, including draft records, reviewed records, archived records, migrated records, translated records, derivative records, source-derived records, or future representation-specific records.

Example:

```yaml
record_id: TBD
```

If a stable record identifier has not yet been assigned, `record_id` MUST be present with the placeholder value `TBD`.

`record_id` MUST NOT replace `object_id`.

`record_id` supports review, maintenance, migration, import, export, archival, and traceability for the record representation.

### 9.3 `record_type`

`record_type` is REQUIRED.

`record_type` identifies the bootstrap type of Knowledge Record.

`record_type` supports basic routing, review, validation, search, template selection, and agent handling.

SC-0001 defines the following bootstrap `record_type` values:

```yaml
concept
person
organization
project
source_summary
decision
procedure
reference
journal
task
event
claim
question
other
unknown
```

A Knowledge Record SHOULD use the most specific applicable bootstrap value.

`unknown` MAY be used when the record type cannot yet be determined.

`other` MAY be used when the record type is known but not represented by the bootstrap vocabulary.

Use of `unknown` or `other` SHOULD trigger review if record type affects routing, validation, authority, privacy, relationships, export, publication, migration, or downstream use.

The bootstrap `record_type` vocabulary is intentionally limited.

A future object-type specification MAY define expanded record types, object types, type-specific metadata, type-specific templates, allowed values, validation rules, migration mappings, or implementation mappings.

Such future values MUST preserve compatibility with SC-0001 or define a governed migration path.

### 9.4 `title`

`title` is REQUIRED.

`title` provides the primary human-readable name of the Knowledge Record.

Example:

```yaml
title: Knowledge Record Metadata Field Specification
```

A title SHOULD be clear, concise, and recognizable.

A title SHOULD help humans and agents identify the record during review, navigation, search, validation, routing, and maintenance.

A title MUST NOT replace `object_id`.

A title MUST NOT be treated as stable Object Identity.

A title MAY change when clarity, correction, review, deprecation, supersession, translation, migration, or implementation presentation requires it.

Changing a title SHOULD NOT change `object_id`.

Changing a title SHOULD NOT change `record_id` unless the record itself is being replaced, split, merged, superseded, or otherwise governed through a record-level change.

If a title has not yet been assigned, the field MUST remain present with the placeholder value `TBD`.

### 9.5 `summary`

`summary` is REQUIRED.

`summary` provides a short human-readable description of the Knowledge Record.

Example:

```yaml
summary: Defines the required metadata fields for bare usable Knowledge Records.
```

A summary SHOULD explain what the record is about without replacing the body of the Knowledge Record.

A summary SHOULD be short enough to support scanning, review, search, agent routing, validation reports, import review, export review, migration review, and downstream-use review.

A summary MUST NOT introduce claims that are not supported by the record body, Source References, provenance, or review context.

A summary MAY be drafted by an agent, but agent-drafted summaries SHOULD remain reviewable when the summary affects interpretation, routing, privacy, authority, validation, publication, export, migration, or downstream use.

If a summary has not yet been written, the field MUST remain present with the placeholder value `TBD`.

### 9.6 `aliases`

`aliases` is RECOMMENDED.

`aliases` records alternate names, prior names, abbreviations, search labels, common spellings, or recognition aids associated with the Knowledge Record or Knowledge Object.

Example:

```yaml
aliases:
  - KR metadata fields
  - Knowledge Record fields
```

Aliases improve search, recall, navigation, import matching, duplicate detection, and migration support.

Aliases MUST NOT replace `object_id`.

Aliases MUST NOT be treated as approved titles unless a governed review or specification explicitly assigns that role.

Aliases SHOULD remain reviewable when they affect duplicate detection, identity matching, relationship creation, authority, privacy, export, migration, or downstream use.

If no aliases are known or needed, the field MAY be omitted unless required by a future template, validator, implementation profile, or object-type specification.

### 9.7 `keywords`

`keywords` is RECOMMENDED.

`keywords` records implementation-independent descriptive terms that support discovery, search, recall, routing, review, validation, agent handling, and maintenance.

Example:

```yaml
keywords:
  - metadata
  - knowledge-record
  - specification
```

`keywords` SHOULD be descriptive rather than decorative.

`keywords` MUST NOT replace governed relationship metadata.

`keywords` MUST NOT replace `record_type`.

`keywords` MUST NOT replace Lifecycle State, Authority Level, Privacy Classification, or Validation State.

`keywords` SHOULD NOT depend on implementation-specific tag behavior.

A future implementation profile MAY map `keywords` to implementation-specific tags, labels, topics, properties, or database fields.

Such mappings MUST preserve the governed meaning of `keywords` and MUST NOT make implementation tags the standard.

## 10. Lifecycle, Authority, Privacy, and Validation Fields

Lifecycle, authority, privacy, and validation fields define how a Knowledge Record should be interpreted, handled, reviewed, routed, protected, validated, and used.

These fields MUST remain distinct from one another.

Lifecycle State describes the governed state of the Knowledge Record.

Authority Level describes the degree of interpretive, governance, review, trust, or use authority assigned to the Knowledge Record within a defined scope.

Privacy Classification describes permitted visibility, access, exposure, routing, synchronization, indexing, export, publication, backup, agent access, workflow access, implementation access, or downstream-use handling.

Validation State describes whether the Knowledge Record satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, workflow, agent, implementation, import, export, or migration expectations.

A Knowledge Record may be structurally valid but not approved.

A Knowledge Record may be approved but private.

A Knowledge Record may be authoritative but superseded.

A Knowledge Record may be public but low-authority.

A Knowledge Record may be draft but structurally valid.

A Knowledge Record may be agent-assisted but still require human review.

These fields MUST NOT be collapsed into a single `status` field.

A generic `status` field SHOULD NOT be used as the governed field for lifecycle, authority, privacy, or validation because it creates ambiguity.

### 10.1 `lifecycle_state`

`lifecycle_state` is REQUIRED.

`lifecycle_state` identifies the current governed lifecycle state of the Knowledge Record.

Default bootstrap value:

```yaml
lifecycle_state: draft
```

SC-0001 defines the following bootstrap `lifecycle_state` values:

```yaml
draft
pending_review
pending_validation
approved
rejected
needs_repair
quarantined
deprecated
superseded
archived
restricted
unknown
```

`draft` means the Knowledge Record is being created, revised, prepared, proposed, or otherwise not yet accepted for governed use.

`pending_review` means the Knowledge Record requires human, workflow, validator, governance, privacy, authority, source-reference, relationship, or compatibility review before it may be treated as reviewed or approved.

`pending_validation` means the Knowledge Record requires validation before it may be treated as valid within the applicable validation scope.

`approved` means the Knowledge Record has been accepted for use within its stated scope.

`rejected` means the Knowledge Record has been reviewed and not accepted for the intended use.

`needs_repair` means the Knowledge Record has known structural, metadata, identity, relationship, source-reference, provenance, privacy, authority, validation, compatibility, workflow, agent, storage, import, export, migration, or implementation issues that require correction.

`quarantined` means the Knowledge Record is isolated or withheld from normal use because of unresolved validity, safety, privacy, compatibility, source, provenance, authority, relationship, or integrity concerns.

`deprecated` means the Knowledge Record remains historically available but is no longer recommended for future use.

`superseded` means the Knowledge Record has been replaced by another governed record, object, decision, rule, version, or representation.

`archived` means the Knowledge Record is preserved for historical, audit, compatibility, migration, governance, or reference purposes but is not treated as active by default.

`restricted` means the Knowledge Record requires constrained handling because access, visibility, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream use is limited.

`unknown` means the lifecycle state cannot currently be determined.

Use of `unknown` SHOULD trigger review.

`lifecycle_state` MUST NOT replace `authority_level`.

`lifecycle_state` MUST NOT replace `privacy_classification`.

`lifecycle_state` MUST NOT replace `validation_state`.

`lifecycle_state` MUST NOT be inferred only from folder placement, filename, tag, user-interface state, workflow state, agent state, storage state, implementation state, or undocumented convention.

### 10.2 `authority_level`

`authority_level` is REQUIRED.

`authority_level` identifies the authority assigned to the Knowledge Record within a defined scope.

Default bootstrap value:

```yaml
authority_level: unreviewed
```

SC-0001 defines the following bootstrap `authority_level` values:

```yaml
unreviewed
working
source_only
reviewed
authoritative
governed
restricted_use
not_authoritative
disputed
unknown
```

`unreviewed` means no human or governed review has confirmed authority.

`working` means the Knowledge Record may support drafting, exploration, organization, or internal reasoning but should not be treated as authoritative.

`source_only` means the record primarily represents or summarizes Source Material and does not independently carry interpretive authority beyond the source context.

`reviewed` means the Knowledge Record has been reviewed but may still have limited authority, limited scope, unresolved issues, or downstream-use restrictions.

`authoritative` means the Knowledge Record may be relied on for interpretation or use within its stated scope.

`governed` means the Knowledge Record is part of a governed standard, specification, workflow, template, validation artifact, agent artifact, implementation artifact, decision record, or other formal governance structure.

`restricted_use` means the Knowledge Record may be used only within a limited authority scope.

`not_authoritative` means the Knowledge Record should not be relied on as an authority for interpretation, decision-making, workflow routing, publication, export, migration, or downstream use.

`disputed` means the Knowledge Record contains unresolved conflict, disagreement, contradiction, uncertainty, or contested authority.

`unknown` means the authority level cannot currently be determined.

Use of `unknown`, `unreviewed`, `working`, `restricted_use`, `not_authoritative`, or `disputed` SHOULD trigger review when the Knowledge Record affects interpretation, publication, export, migration, automation, relationship creation, workflow routing, validation, agent reasoning, or downstream use.

`authority_level` MUST NOT replace `lifecycle_state`.

`authority_level` MUST NOT replace `validation_state`.

`authority_level` MUST NOT replace `privacy_classification`.

`authority_level` MUST NOT be inferred only from approval appearance, folder placement, source popularity, source reliability, agent confidence, workflow completion, implementation visibility, search ranking, graph centrality, or undocumented convention.

### 10.3 `privacy_classification`

`privacy_classification` is REQUIRED.

`privacy_classification` identifies the privacy handling required for the Knowledge Record.

Default bootstrap value:

```yaml
privacy_classification: private
```

SC-0001 defines the following bootstrap `privacy_classification` values:

```yaml
public
internal
private
sensitive
restricted
unknown
```

`public` means the Knowledge Record may be visible or shared beyond the private working environment only when publication, export, synchronization, indexing, downstream-use, and authority requirements are also satisfied.

`internal` means the Knowledge Record is intended for controlled use within a defined trusted environment.

`private` means the Knowledge Record is intended for personal or limited-access use and should not be exposed publicly by default.

`sensitive` means the Knowledge Record contains information requiring heightened protection, review, limited access, or careful routing.

`restricted` means the Knowledge Record requires strict access, exposure, export, publication, synchronization, indexing, backup, agent-access, workflow-access, implementation-access, or downstream-use controls.

`unknown` means the privacy classification cannot currently be determined.

Use of `unknown` SHOULD trigger privacy review.

`private` is the default bootstrap value because bare usable deployment should avoid accidental exposure.

`public` MUST NOT be assigned merely because a record is approved, valid, stored in a public-facing folder, visible in an implementation, indexed by a tool, linked by another record, summarized by an agent, exported, migrated, or published.

`privacy_classification` MUST NOT replace `lifecycle_state`.

`privacy_classification` MUST NOT replace `authority_level`.

`privacy_classification` MUST NOT replace `validation_state`.

A Knowledge Record with `privacy_classification: sensitive`, `privacy_classification: restricted`, or `privacy_classification: unknown` SHOULD require human review before publication, export, synchronization, indexing, broad agent access, broad workflow access, or downstream use.

### 10.4 `validation_state`

`validation_state` is REQUIRED.

`validation_state` identifies the validation status of the Knowledge Record within the applicable validation scope.

Default bootstrap value:

```yaml
validation_state: not_validated
```

SC-0001 defines the following bootstrap `validation_state` values:

```yaml
not_validated
pending_validation
valid
valid_with_warnings
invalid
needs_repair
unknown
```

`not_validated` means validation has not yet been performed.

`pending_validation` means validation is required or underway but not complete.

`valid` means the Knowledge Record satisfies the applicable validation scope.

`valid_with_warnings` means the Knowledge Record satisfies mandatory validation requirements but has warnings, limitations, risks, incomplete recommended fields, review notes, or non-blocking issues.

`invalid` means the Knowledge Record fails one or more mandatory validation requirements within the applicable validation scope.

`needs_repair` means validation identified issues that require correction before the record can satisfy the applicable validation scope.

`unknown` means the validation state cannot currently be determined.

Use of `unknown`, `not_validated`, `pending_validation`, `valid_with_warnings`, `invalid`, or `needs_repair` SHOULD trigger review, repair, routing, or validation follow-up when the Knowledge Record affects authority, privacy, publication, export, migration, automation, relationship creation, workflow routing, agent reasoning, or downstream use.

`validation_state` MUST NOT replace `lifecycle_state`.

`validation_state` MUST NOT replace `authority_level`.

`validation_state` MUST NOT replace `privacy_classification`.

Validation success does not equal approval.

Validation success does not equal authority.

Validation success does not equal privacy clearance.

Validation success does not equal publication permission.

Validation success does not equal export permission.

Validation success does not equal migration readiness.

Validation success does not equal downstream-use readiness.

## 11. Source, Provenance, and Relationship Fields

Source, provenance, and relationship fields preserve traceability.

These fields help future humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations understand where a Knowledge Record came from, what supports it, how it was created or changed, and what other governed entities it connects to.

Source, provenance, and relationship fields MUST preserve the distinction between:

- Source Material;
- Source References;
- citations;
- evidence;
- attribution;
- provenance;
- extraction history;
- transformation history;
- relationships;
- inferred relationships;
- proposed relationships;
- approved relationships;
- implementation links;
- backlinks;
- tags;
- search associations;
- graph positions;
- agent suggestions;
- workflow outputs.

A Knowledge Record may have no Source References.

A Knowledge Record may have one Source Reference.

A Knowledge Record may have many Source References.

A Knowledge Record may be human-created, source-derived, agent-assisted, workflow-generated, imported, migrated, reviewed, validated, or a mixture of those origins.

A Knowledge Record may have no relationships.

A Knowledge Record may contain proposed relationships.

A Knowledge Record may contain approved relationships.

A Knowledge Record may contain relationships requiring review.

These distinctions MUST remain visible.

### 11.1 `source_refs`

`source_refs` is REQUIRED.

`source_refs` identifies Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the Knowledge Record.

Default bootstrap value:

```yaml
source_refs: []
```

`source_refs` MUST be represented as a list.

If no Source References are known or applicable, the field MUST remain present with an empty list.

Example:

```yaml
source_refs:
  - SRC-0001
  - SRC-0002
```

A source-derived Knowledge Record SHOULD NOT have an empty `source_refs` list unless the source is unknown, unavailable, restricted, missing, or pending review.

When a source is unknown but required, `source_refs` SHOULD include a placeholder entry or the Knowledge Record SHOULD be routed for source review.

Example:

```yaml
source_refs:
  - unknown
```

`source_refs` MUST NOT be replaced by citations alone.

A citation MAY support a Source Reference, but citation syntax does not define source-reference behavior by itself.

`source_refs` MUST NOT be replaced by:

- folder placement;
- filenames;
- backlinks;
- tags;
- copied excerpts;
- browser bookmarks;
- search results;
- implementation links;
- agent memory;
- workflow memory;
- undocumented source notes.

A future source-reference specification MAY define exact source-reference identifiers, source schemas, citation syntax, archival requirements, source availability values, source reliability values, source authority values, source privacy fields, extraction records, and validation rules.

### 11.2 `provenance`

`provenance` is REQUIRED.

`provenance` identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, import, export, migration, validation, review, evidence, or change context associated with the Knowledge Record.

Default bootstrap value:

```yaml
provenance: TBD
```

For bare usable deployment, `provenance` MAY be represented as a short text value, a structured object, or a reference to a provenance record.

A simple text representation is acceptable for early draft use:

```yaml
provenance: Created from user-provided notes during controlled ingestion.
```

A structured representation is RECOMMENDED when practical:

```yaml
provenance:
  created_by: human
  created_method: manual
  source_basis: human_created
  agent_activity_refs: []
  workflow_refs: []
  review_refs: []
```

SC-0001 defines the following bootstrap `created_method` values when structured provenance is used:

```yaml
manual
agent_assisted
workflow_generated
imported
migrated
extracted
transformed
mixed
unknown
```

SC-0001 defines the following bootstrap `source_basis` values when structured provenance is used:

```yaml
human_created
source_derived
source_summarized
source_extracted
agent_generated
workflow_generated
imported
migrated
mixed
unknown
none
```

`provenance` MUST remain distinguishable from `source_refs`.

`source_refs` identify source material.

`provenance` explains origin, creation, transformation, authorship, agent involvement, workflow involvement, review involvement, validation involvement, import context, export context, migration context, or change context.

A Knowledge Record with agent involvement SHOULD make that involvement visible through both `provenance` and the agent fields defined in this specification.

A Knowledge Record with workflow involvement SHOULD make that involvement visible through `provenance` or a related workflow record.

A Knowledge Record with import or migration history SHOULD preserve enough provenance for future validation, review, repair, export, migration, and compatibility checking.

`provenance` MUST NOT be hidden only in agent memory, workflow memory, implementation logs, application state, file history, sync history, or undocumented notes when provenance affects interpretation, source support, relationships, lifecycle state, authority, privacy, validation, publication, export, migration, or downstream use.

### 11.3 `relationships`

`relationships` is REQUIRED.

`relationships` records explicit proposed, reviewed, approved, rejected, deprecated, superseded, inferred, or otherwise governed relationships between the Knowledge Record and other governed entities.

Default bootstrap value:

```yaml
relationships: []
```

`relationships` MUST be represented as a list.

If no relationships are known or applicable, the field MUST remain present with an empty list.

A simple list representation MAY be used for early draft records:

```yaml
relationships:
  - OBJ-0001
  - OBJ-0002
```

A structured relationship representation is RECOMMENDED when relationship meaning, direction, provenance, confidence, review state, lifecycle state, authority, privacy, validation, migration, export, or downstream use matters.

Example:

```yaml
relationships:
  - target_id: OBJ-0001
    relationship_type: related_to
    relationship_state: proposed
    relationship_direction: outbound
    relationship_provenance: TBD
```

SC-0001 defines the following bootstrap `relationship_state` values when structured relationships are used:

```yaml
proposed
inferred
reviewed
approved
rejected
needs_review
deprecated
superseded
unknown
```

SC-0001 defines the following bootstrap `relationship_direction` values when structured relationships are used:

```yaml
outbound
inbound
bidirectional
non_directional
unknown
```

SC-0001 defines the following bootstrap `relationship_type` values for early use:

```yaml
related_to
supports
contradicts
depends_on
part_of
contains
derived_from
supersedes
superseded_by
references
duplicates
possible_duplicate
other
unknown
```

The bootstrap relationship vocabulary is intentionally limited.

A future relationship specification MAY define expanded relationship types, directionality rules, relationship identifiers, relationship confidence values, relationship lifecycle values, relationship authority values, relationship privacy handling, graph schemas, validation rules, migration mappings, and implementation mappings.

`relationships` MUST NOT be replaced by backlinks alone.

`relationships` MUST NOT be replaced by folder proximity, tags, search similarity, graph location, plugin behavior, agent suggestions, workflow suggestions, or implementation-generated links.

Backlinks, tags, search similarity, graph location, plugin behavior, agent suggestions, workflow suggestions, and implementation-generated links MAY help discover possible relationships.

They do not become governed relationships unless represented, reviewed, validated, or approved according to the applicable standards, specifications, or workflows.

## 12. Date, Review, and Agent Fields

Date, review, and agent fields preserve basic traceability for creation, update, review, and agent assistance.

These fields help humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, and implementations determine when a Knowledge Record was created or updated, whether review is required, whether an agent assisted, and who is responsible for human review.

Date, review, and agent fields MUST remain distinct from lifecycle, authority, privacy, validation, source-reference, provenance, relationship, workflow, storage, and implementation behavior.

A record being recently updated does not mean it is approved.

A record having a reviewer does not mean it has passed review.

A record being agent-assisted does not mean it is valid.

A record not being agent-assisted does not mean it is authoritative.

A record being reviewed does not mean it is public.

A record being old does not mean it is deprecated.

A record being new does not mean it is low-quality.

### 12.1 `created`

`created` is REQUIRED.

`created` records the date the Knowledge Record was created.

Default bootstrap value:

```yaml
created: TBD
```

The RECOMMENDED date format is ISO-style `YYYY-MM-DD`.

Example:

```yaml
created: 2026-06-28
```

A future specification MAY define exact datetime, timezone, timestamp, created-at, imported-at, migrated-at, or event-log requirements.

For bare usable deployment, `YYYY-MM-DD` is sufficient unless the workflow, implementation, import process, export process, migration process, review process, validation process, or agent activity requires more precise time tracking.

`created` SHOULD represent creation of the Knowledge Record, not necessarily creation of the Knowledge Object, Source Material, original idea, original event, original publication, original file, or original source.

Those other dates MAY be recorded in future fields or object-type-specific specifications.

`created` MUST NOT replace provenance.

### 12.2 `updated`

`updated` is REQUIRED.

`updated` records the date the Knowledge Record was last materially updated.

Default bootstrap value:

```yaml
updated: TBD
```

The RECOMMENDED date format is ISO-style `YYYY-MM-DD`.

Example:

```yaml
updated: 2026-06-28
```

`updated` SHOULD change when the Knowledge Record receives a material change to content, metadata, relationships, source references, provenance, lifecycle state, authority level, privacy classification, validation state, review status, agent activity references, workflow references, import context, export context, migration context, or downstream-use readiness.

`updated` MAY remain unchanged for minor formatting corrections, whitespace changes, spelling corrections, or non-material edits unless a future governance process, implementation profile, validator, workflow, or audit process requires stricter tracking.

`updated` MUST NOT replace review history.

`updated` MUST NOT replace provenance.

`updated` MUST NOT imply approval, validation success, authority, privacy clearance, publication permission, export permission, migration readiness, or downstream-use readiness.

### 12.3 `review_required`

`review_required` is REQUIRED.

`review_required` indicates whether human review or governed review is required before the Knowledge Record may be treated as reviewed, approved, authoritative, publishable, exportable, migratable, or ready for downstream use.

Default bootstrap value:

```yaml
review_required: true
```

SC-0001 defines the following bootstrap values:

```yaml
true
false
```

`review_required: true` means review is required.

`review_required: false` means review is not currently required within the applicable scope.

`review_required: false` MUST NOT be used to bypass required review.

`review_required: false` SHOULD only be used when review has been completed, determined not applicable, or waived under a governed workflow, specification, or approval scope.

A Knowledge Record SHOULD use `review_required: true` when:

- `object_id` is `TBD`;
- `record_id` is `TBD`;
- `record_type` is `unknown` or `other`;
- `title` is `TBD`;
- `summary` is `TBD`;
- `lifecycle_state` is `draft`, `pending_review`, `pending_validation`, `needs_repair`, `quarantined`, `restricted`, or `unknown`;
- `authority_level` is `unreviewed`, `working`, `restricted_use`, `not_authoritative`, `disputed`, or `unknown`;
- `privacy_classification` is `sensitive`, `restricted`, or `unknown`;
- `validation_state` is `not_validated`, `pending_validation`, `valid_with_warnings`, `invalid`, `needs_repair`, or `unknown`;
- source support is missing, unknown, restricted, or disputed;
- provenance is incomplete, unknown, agent-generated, imported, migrated, or pending review;
- relationships are proposed, inferred, disputed, unknown, or pending review;
- an agent assisted with creation, extraction, summarization, classification, relationship proposal, metadata proposal, validation, or review preparation;
- publication, export, migration, broad synchronization, broad indexing, or downstream use is being considered.

### 12.4 `agent_assisted`

`agent_assisted` is REQUIRED.

`agent_assisted` indicates whether an agent assisted with creation, extraction, summarization, classification, metadata proposal, relationship proposal, validation support, draft preparation, review preparation, import support, migration support, or other record activity.

Default bootstrap value:

```yaml
agent_assisted: false
```

SC-0001 defines the following bootstrap values:

```yaml
true
false
```

`agent_assisted: true` means agent assistance occurred.

`agent_assisted: false` means no known agent assistance occurred.

`agent_assisted: false` MUST NOT be used when an agent materially contributed to the record.

A Knowledge Record with `agent_assisted: true` SHOULD preserve agent involvement in provenance, agent activity records, workflow logs, review records, or implementation logs where applicable.

Agent assistance does not equal approval.

Agent assistance does not equal authority.

Agent assistance does not equal validation success.

Agent assistance does not equal privacy clearance.

Agent assistance does not equal publication permission.

Agent assistance does not equal export permission.

Agent assistance does not equal migration readiness.

Agent assistance does not equal downstream-use readiness.

### 12.5 `human_reviewer`

`human_reviewer` is REQUIRED.

`human_reviewer` identifies the human reviewer assigned to review the Knowledge Record where review is required or expected.

Default bootstrap value:

```yaml
human_reviewer: unassigned
```

If no human reviewer has been assigned, the value MUST remain `unassigned`.

If human review is not applicable under a governed workflow or specification, the value MAY be:

```yaml
human_reviewer: not_applicable
```

If a reviewer is assigned, the value SHOULD identify the reviewer in a stable, privacy-respecting, implementation-independent way.

Example:

```yaml
human_reviewer: Daniel Balcom
```

or:

```yaml
human_reviewer: reviewer-0001
```

`human_reviewer` MUST NOT imply approval by itself.

A named reviewer indicates assignment or participation, not necessarily completion, acceptance, approval, privacy clearance, authority assignment, validation success, publication readiness, export readiness, migration readiness, or downstream-use readiness.

Review decisions SHOULD be captured in a Review Record, workflow output, provenance entry, validation result, approval record, or future governed review field when needed.

### 12.6 `review_refs`

`review_refs` is RECOMMENDED.

`review_refs` identifies Review Records, review outputs, approval records, rejection records, repair records, escalation records, privacy reviews, authority reviews, validation reviews, source reviews, relationship reviews, or workflow logs associated with the Knowledge Record.

Default recommended value when used:

```yaml
review_refs: []
```

Example:

```yaml
review_refs:
  - REVIEW-0001
```

`review_refs` SHOULD be used when review decisions affect lifecycle state, authority level, privacy classification, validation state, publication, export, migration, or downstream use.

`review_refs` MUST NOT replace `human_reviewer`.

`review_refs` MUST NOT replace `review_required`.

`review_refs` MUST NOT imply approval unless the referenced review record explicitly records an approval decision within a governed approval scope.

### 12.7 `agent_activity_refs`

`agent_activity_refs` is RECOMMENDED.

`agent_activity_refs` identifies Agent Activity Records, agent outputs, agent validation reports, agent metadata proposals, agent relationship proposals, agent summaries, agent extraction reports, agent review reports, agent import reports, agent migration reports, or other agent-generated artifacts associated with the Knowledge Record.

Default recommended value when used:

```yaml
agent_activity_refs: []
```

Example:

```yaml
agent_activity_refs:
  - AG-ACT-0001
```

`agent_activity_refs` SHOULD be used when `agent_assisted` is `true`.

`agent_activity_refs` SHOULD be used when agent activity affects metadata, source references, provenance, relationships, lifecycle state, authority level, privacy classification, validation state, review routing, publication, export, migration, or downstream use.

`agent_activity_refs` MUST NOT replace provenance.

`agent_activity_refs` MUST NOT replace review.

`agent_activity_refs` MUST NOT imply approval, authority, validation success, privacy clearance, publication permission, export permission, migration readiness, or downstream-use readiness.

## 13. Field Value and Compatibility Rules

Field values define the content assigned to SC-0001 metadata fields.

Field values MUST remain explicit, readable, portable, reviewable, and implementation-independent.

A field value MUST preserve the governed meaning of the field.

A field value MUST NOT rely on hidden application state, folder placement, filename conventions, user-interface behavior, plugin behavior, database internals, agent memory, workflow memory, implementation defaults, or undocumented conventions where the value affects governed meaning.

SC-0001 recognizes the following bootstrap value forms:

- text values;
- controlled vocabulary values;
- boolean values;
- date values;
- list values;
- structured object values;
- placeholder values.

A text value is a human-readable string used for descriptive, explanatory, or reference information.

Example:

```yaml
title: Knowledge Record Metadata Field Specification
```

A controlled vocabulary value is a value selected from an allowed value set defined by SC-0001 or a future governed specification.

Example:

```yaml
lifecycle_state: draft
```

A boolean value is a true-or-false value.

Example:

```yaml
review_required: true
agent_assisted: false
```

A date value records a date or future governed datetime value.

Example:

```yaml
created: 2026-06-28
updated: 2026-06-28
```

A list value records zero, one, or many entries.

Example:

```yaml
source_refs:
  - SRC-0001
  - SRC-0002
```

An empty list is represented as:

```yaml
source_refs: []
```

A structured object value records nested information when simple text is not sufficient.

Example:

```yaml
provenance:
  created_by: human
  created_method: manual
  source_basis: human_created
  agent_activity_refs: []
  workflow_refs: []
  review_refs: []
```

A placeholder value records that information is unknown, pending, unavailable, unassigned, not applicable, intentionally absent, or awaiting review.

Example:

```yaml
object_id: TBD
human_reviewer: unassigned
source_refs: []
```

Field values SHOULD use lowercase snake_case when they are controlled vocabulary values.

Example:

```yaml
validation_state: valid_with_warnings
privacy_classification: private
authority_level: unreviewed
```

Field values SHOULD NOT use inconsistent capitalization, spacing, spelling, punctuation, or synonyms when a controlled vocabulary is defined.

Avoid inconsistent values such as:

```yaml
validation_state: Valid With Warnings
privacy_classification: Private Use
authority_level: not reviewed
```

unless a future governed specification explicitly defines mapping rules for those values.

A field value MUST NOT silently change meaning during import, export, migration, backup, restoration, synchronization, indexing, publication, agent processing, workflow processing, or implementation replacement.

A compliant implementation MAY map SC-0001 field values to implementation-specific values only when the mapping is documented, reviewable, and reversible where practical.

A field value mapping MUST NOT cause:

- Object Identity confusion;
- record identity confusion;
- title confusion;
- record-type confusion;
- source-reference loss;
- provenance loss;
- relationship ambiguity;
- lifecycle-state confusion;
- authority confusion;
- privacy exposure;
- validation error;
- review-routing error;
- agent-permission confusion;
- workflow-routing error;
- import ambiguity;
- export ambiguity;
- migration loss;
- publication error;
- downstream-use error;
- governance drift.

A future specification MAY define stricter field value rules, expanded allowed values, deprecated values, legacy mappings, implementation mappings, validator mappings, import mappings, export mappings, migration mappings, or serialization mappings.

Such future rules MUST preserve the governed meaning of SC-0001 fields or define a reviewed compatibility path.

## 14. Validation Expectations

SC-0001 defines metadata-field validation expectations for bare usable Knowledge Records.

SC-0001 does not define a complete validation engine.

SC-0001 does not define a complete conformance test suite.

SC-0001 does not define validator tooling, error-code syntax, warning-code syntax, automation scripts, implementation behavior, workflow behavior, or agent prompts.

Those concerns belong to future validation specifications, validator profiles, workflow specifications, agent specifications, implementation profiles, operational guides, and conformance tools.

A Knowledge Record satisfies SC-0001 metadata-field validation only when the applicable SC-0001 metadata expectations are met within the defined validation scope.

SC-0001 metadata-field validation SHOULD check at minimum whether:

- all required fields are present;
- required fields use valid field names;
- field names follow SC-0001 naming rules;
- controlled vocabulary fields use allowed bootstrap values or governed future values;
- placeholder values are used consistently;
- placeholder values do not hide required review;
- list fields are represented as lists;
- structured fields remain readable and inspectable;
- `object_id` remains distinct from `record_id`;
- `object_id` is not replaced by title, filename, folder path, alias, tag, implementation ID, workflow ID, agent ID, validation ID, import ID, export ID, or migration ID;
- `record_id` remains distinct from `object_id`;
- `record_type` uses a bootstrap value or governed future value;
- `title` is present;
- `summary` is present;
- `lifecycle_state` is present and distinct from authority, privacy, validation, workflow state, agent state, storage state, and implementation state;
- `authority_level` is present and distinct from lifecycle, privacy, validation, source reliability, agent confidence, workflow completion, and implementation visibility;
- `privacy_classification` is present and distinct from lifecycle, authority, validation, approval, publication status, export status, and implementation visibility;
- `validation_state` is present and distinct from lifecycle, authority, privacy, approval, publication permission, export permission, migration readiness, and downstream-use permission;
- `source_refs` is present and represented as a list;
- `provenance` is present;
- `relationships` is present and represented as a list;
- `created` is present;
- `updated` is present;
- `review_required` is present and boolean;
- `agent_assisted` is present and boolean;
- `human_reviewer` is present;
- agent assistance is traceable when `agent_assisted` is `true`;
- review need is visible when review-triggering conditions apply;
- field values remain implementation-independent;
- field values remain portable across import, export, migration, backup, restoration, synchronization, indexing, publication, workflow activity, agent activity, and implementation replacement.

A missing required field is a validation error within SC-0001 scope.

An invalid controlled vocabulary value is a validation error within SC-0001 scope unless a governed mapping or future specification explicitly permits it.

A required field populated with an inappropriate placeholder value SHOULD create a validation warning or validation error depending on the applicable validation scope.

An omitted recommended field SHOULD create a validation warning only when the field materially affects reviewability, portability, source traceability, provenance, relationship clarity, validation, maintenance, import, export, migration, agent reliability, workflow reliability, or downstream use.

An omitted optional field SHOULD NOT create a validation issue unless a future governed specification, object-type rule, workflow, implementation profile, or validation profile requires it.

A metadata-field validator MUST NOT overstate its scope.

A validator that checks only SC-0001 metadata fields MUST NOT claim full Knowledge Record validation.

A validator that checks only field presence MUST NOT claim full metadata validation.

A validator that checks only Markdown syntax MUST NOT claim SC-0001 conformance unless it also checks applicable SC-0001 field expectations.

A validator that checks SC-0001 conformance MUST NOT imply approval.

A validator that checks SC-0001 conformance MUST NOT imply authority.

A validator that checks SC-0001 conformance MUST NOT imply privacy clearance.

A validator that checks SC-0001 conformance MUST NOT imply publication permission.

A validator that checks SC-0001 conformance MUST NOT imply export permission.

A validator that checks SC-0001 conformance MUST NOT imply migration readiness.

A validator that checks SC-0001 conformance MUST NOT imply downstream-use readiness.

Agent-generated validation results MUST remain reviewable where validation affects meaning, authority, privacy, lifecycle handling, publication, export, migration, governance, or downstream use.

Workflow-generated validation results MUST remain traceable where validation affects review, approval, rejection, repair, routing, authority, privacy, publication, export, migration, or downstream use.

Validation results SHOULD identify the validation scope.

Example validation scope:

```yaml
validation_scope: SC-0001 metadata field validation
```

Validation results SHOULD identify whether validation was performed by a human, agent, workflow, tool, implementation, import process, export process, migration process, or other validator.

Example:

```yaml
validated_by: agent
validation_scope: SC-0001 metadata field validation
validation_result: valid_with_warnings
```

Detailed validation result storage belongs to VALID-0001, TEMPLATE-0004, future validation specifications, review records, workflow logs, or agent activity records.

SC-0001 only defines the metadata-field expectations those later artifacts should validate against.

## 15. Conformance and Success Criteria

SC-0001 conformance means that a Knowledge Record satisfies the metadata-field expectations defined by this specification within a stated scope.

SC-0001 conformance does not mean the Knowledge Record is fully approved, authoritative, public, exportable, publishable, migratable, complete, current, or ready for downstream use.

SC-0001 defines three bootstrap conformance levels:

- Non-Conformant;
- Bare Usable Conformant;
- Extended Conformant.

A Knowledge Record is Non-Conformant when it fails one or more mandatory SC-0001 requirements.

A Knowledge Record is Bare Usable Conformant when it includes all required SC-0001 fields, uses valid field names, uses valid bootstrap values or approved placeholder values, preserves required distinctions, and remains inspectable, portable, reviewable, and implementation-independent.

A Knowledge Record is Extended Conformant when it satisfies Bare Usable Conformance and also includes applicable recommended fields, structured provenance where practical, structured relationships where practical, review references where applicable, agent activity references where applicable, and any additional governed future specification requirements within the stated scope.

A Knowledge Record MUST NOT be marked Bare Usable Conformant if it omits any required SC-0001 field.

A Knowledge Record MUST NOT be marked Bare Usable Conformant if a required field is present but uses a value that violates SC-0001 field rules.

A Knowledge Record MUST NOT be marked Bare Usable Conformant if it collapses Object Identity, Record Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, Source References, Provenance, Relationships, review responsibility, or agent assistance into ambiguous or implementation-specific signals.

A Knowledge Record MUST NOT be marked Bare Usable Conformant if field meaning depends on hidden application state, folder placement, filename convention, plugin behavior, database internals, agent memory, workflow memory, or undocumented implementation behavior.

A Bare Usable Conformant Knowledge Record SHOULD allow a future human, agent, workflow, validator, storage system, import process, export process, migration process, or implementation to determine:

- what Knowledge Object the record represents;
- what specific Knowledge Record is being inspected;
- what type of record it is;
- what the record is called;
- what the record is about;
- what lifecycle state applies;
- what authority level applies;
- what privacy classification applies;
- what validation state applies;
- what Source References are known;
- what provenance is known;
- what relationships are known, proposed, or established;
- when the record was created;
- when the record was last materially updated;
- whether review is required;
- whether an agent assisted;
- who is assigned for human review;
- whether unresolved placeholders remain;
- whether the record requires repair, review, validation, privacy review, authority review, source review, relationship review, publication review, export review, migration review, or downstream-use review.

SC-0001 is successful when TEMPLATE-0001 can use its fields directly to create a usable Knowledge Record template.

SC-0001 is successful when TEMPLATE-0002 can reference its source, provenance, review, and relationship fields during Source Material intake.

SC-0001 is successful when TEMPLATE-0003 can reference its agent-related fields during Agent Activity Record creation.

SC-0001 is successful when TEMPLATE-0004 can reference its review-related fields during Review Record creation.

SC-0001 is successful when VALID-0001 can validate the presence, naming, value, placeholder, compatibility, and review expectations of bare usable Knowledge Records.

SC-0001 is successful when AG-SPEC-0001 can instruct agents to read, populate, inspect, and report on metadata fields without exceeding agent authority.

SC-0001 is successful when AG-SPEC-0002 can define subagent role profiles that propose metadata, relationships, source references, provenance, validation findings, and review routing without becoming unreviewable authorities.

SC-0001 is successful when WF-SPEC-0001 can use its fields during controlled ingestion without relying on hidden workflow state.

SC-0001 is successful when a Knowledge Record remains understandable after:

- file renaming;
- folder movement;
- storage reorganization;
- import;
- export;
- migration;
- backup;
- restoration;
- synchronization;
- indexing;
- publication review;
- agent processing;
- workflow processing;
- implementation replacement.

SC-0001 is successful when metadata remains useful without becoming excessive.

SC-0001 is successful when field structure supports daily use while preserving long-term identity, traceability, privacy, validation, reviewability, portability, compatibility, and governance.

SC-0001 is complete for bare usable deployment when:

- all 15 sections are present;
- required fields are defined;
- recommended fields are identified where needed;
- placeholder values are defined;
- field naming rules are defined;
- field value rules are defined;
- lifecycle, authority, privacy, and validation fields are distinct;
- source, provenance, and relationship fields are distinct;
- date, review, and agent fields are distinct;
- validation expectations are scoped;
- conformance criteria are defined;
- downstream templates and validation checklists can rely on the field set.

End of SC-0001.
