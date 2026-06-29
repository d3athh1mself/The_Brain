# SC-0001 — Knowledge Record Metadata Field Specification

Document ID: SC-0001
Title: Knowledge Record Metadata Field Specification
Version: 0.1.0
Status: Draft
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
