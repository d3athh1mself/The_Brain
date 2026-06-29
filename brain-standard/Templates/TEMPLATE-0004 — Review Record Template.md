# TEMPLATE-0004 — Review Record Template

Document ID: TEMPLATE-0004
Title: Review Record Template
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Template
Phase: Phase 6 — Templates and Validation Support
Milestone: 6.4 — Review Record Template
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; WF-0003 — Knowledge Maintenance and Update Workflow Standard; WF-0004 — Publication, Export, and Downstream Use Workflow Standard; TEMPLATE-0001 — Knowledge Record Template; TEMPLATE-0002 — Source Material Intake Template; TEMPLATE-0003 — Agent Activity Record Template
Supersedes: None
Superseded By: None
Related: VALID-0001 — Bare Usable Validation Checklist; AG-SPEC-0001 — Agent Initialization Packet; WF-SPEC-0001 — Controlled Ingestion Runbook

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and review-record template rules are interpreted within TEMPLATE-0004.

Where conflicts arise between review records, review decisions, approval scope, rejection scope, correction requests, validation findings, privacy findings, authority findings, agent outputs, workflow outputs, downstream-use permissions, publication readiness, export readiness, migration readiness, or future specifications, the constitutional foundation and higher-authority standards SHALL guide interpretation and resolution.

TEMPLATE-0004 is subordinate to TB-0000, TB-0001, TB-0002, TB-0003, the Phase 1 Knowledge Standards, the Phase 2 Storage Standards, Agent Framework standards, Workflow Engine standards, and applicable governed specifications.

TEMPLATE-0004 defines a reusable review-record structure.

TEMPLATE-0004 does not define review authority by itself.

TEMPLATE-0004 does not replace WF-0002.

TEMPLATE-0004 does not replace validation standards, privacy standards, authority standards, lifecycle standards, agent standards, workflow standards, or governed approval processes.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Review Record refers to a structured record documenting what was reviewed, what evidence was considered, what decision was made, what corrections were required, what was accepted, what was rejected, what was escalated, and what downstream use is permitted or blocked.
- Review Subject refers to the governed entity, Source Material, record, template, workflow output, agent output, validation result, or proposed change being reviewed.
- Reviewer refers to the human, governed role, workflow participant, or authorized review process responsible for evaluating the Review Subject.
- Review Decision refers to the recorded outcome of review, including approval, rejection, repair required, escalation required, deferral, quarantine, archival, supersession, deprecation, or limited acceptance.
- Approval Scope refers to the defined context in which a review approval applies.
- Correction Request refers to a documented request to repair, revise, clarify, restructure, validate, source, reclassify, or otherwise correct a reviewed entity.
- Escalation refers to routing an unresolved issue, risk, conflict, ambiguity, privacy concern, authority concern, validation concern, source concern, destructive action, or downstream-use concern to a higher-authority review process.
- Downstream Use refers to later use of reviewed material for interpretation, automation, publication, export, migration, relationship creation, validation, decision support, agent reasoning, workflow execution, implementation behavior, or other dependent activity.
- Agent Output refers to a result produced by an agent, including a summary, classification, proposed metadata, proposed relationship, validation result, draft record, proposed edit, recommendation, warning, report, or generated content.
- Workflow Output refers to a record, decision, routing action, validation result, review note, approval decision, rejection decision, repair request, escalation, lifecycle transition, or other artifact created through a governed workflow.
- Validation Finding refers to a validation result, warning, error, issue, gap, inconsistency, or conformance concern identified during review or validation.
- Privacy Finding refers to a privacy-related concern, classification issue, access concern, exposure risk, publication risk, export risk, indexing risk, synchronization risk, backup concern, or downstream-use limitation.
- Authority Finding refers to a concern or determination related to Authority Level, authority scope, trust boundary, approval weight, review status, or use-authority.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of TEMPLATE-0004 is to provide a standard, copy/paste-ready structure for recording governed review activity within The Brain Standard.

A Review Record documents what was reviewed, who or what performed the review, what evidence was considered, what decision was made, what corrections were required, what was accepted, what was rejected, what was escalated, and what downstream use is permitted or blocked.

TEMPLATE-0004 exists so review decisions remain explicit, traceable, portable, human-readable, AI-readable, and implementation-independent.

## 2. Relationship to Prior Standards and Templates

TEMPLATE-0004 is subordinate to the constitutional foundation of The Brain Standard.

TEMPLATE-0004 depends on prior knowledge, storage, agent, workflow, and template documents because review records must preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage boundaries, agent boundaries, and workflow review requirements.

TEMPLATE-0004 supports the Review and Approval Workflow Standard by providing a repeatable structure for recording review outcomes without replacing the workflow itself.

TEMPLATE-0003 records what an agent did.

TEMPLATE-0004 records what a reviewer decided.

A Review Record may reference an Agent Activity Record, but it does not become an Agent Activity Record.

A Review Record may review a Knowledge Record, but it does not become the Knowledge Record itself.

A Review Record may record validation findings, but it does not become a validation checklist.

## 3. Template Scope and Use Rules

TEMPLATE-0004 applies when a review decision must be recorded in a governed, traceable, and reusable form.

A Review Record SHOULD be created when review affects approval, rejection, repair, escalation, lifecycle state, Authority Level, Privacy Classification, validation state, source-reference adequacy, provenance adequacy, relationship approval, metadata acceptance, downstream-use permission, publication readiness, export readiness, migration readiness, archival routing, quarantine routing, agent-output acceptance, or workflow-output acceptance.

A Review Record MUST identify the reviewed subject clearly enough that a future human, agent, workflow, validator, storage system, or implementation can determine what was reviewed.

A Review Record MUST distinguish:

- the reviewed subject from the review decision;
- reviewer notes from approved Knowledge Record content;
- correction requests from completed corrections;
- escalation notes from completed escalation;
- validation findings from approval;
- privacy concerns from privacy clearance;
- authority concerns from Authority Level assignment;
- agent recommendations from reviewer decisions;
- workflow routing from lifecycle approval.

A Review Record MUST NOT silently approve, reject, publish, export, migrate, delete, archive, supersede, deprecate, or change Object Identity.

A Review Record MUST record the scope of any approval, rejection, limitation, permission, or downstream-use decision.

Approval for one scope MUST NOT be treated as approval for every scope.

TEMPLATE-0004 is software-neutral and AI-neutral.

TEMPLATE-0004 MUST NOT depend on Obsidian, Codex, ChatGPT, Claude, GitHub, a specific file system, a specific model, a specific plugin, a specific repository layout, or a specific implementation.

## 4. Review Record Metadata Block

Each Review Record SHOULD include a metadata block that identifies the review record, the reviewed subject, the reviewer, the review date, the review decision, the approval scope where applicable, and the downstream-use result.

The metadata block exists to make the Review Record traceable, reviewable, searchable, portable, and interpretable by humans, agents, workflows, validators, storage systems, and implementations.

A Review Record metadata block SHOULD use the following structure unless a future governed specification defines a more exact schema:

```yaml
review_record_id:
review_record_title:
review_record_type: Review Record
review_status:
created:
last_updated:
review_date:
reviewer:
reviewer_role:
review_subject_id:
review_subject_title:
review_subject_type:
review_subject_location:
review_subject_lifecycle_state:
review_subject_authority_level:
review_subject_privacy_classification:
review_scope:
review_decision:
approval_scope:
correction_required:
escalation_required:
validation_result:
privacy_result:
authority_result:
source_reference_result:
provenance_result:
relationship_result:
downstream_use_result:
publication_result:
export_result:
migration_result:
related_agent_activity_record:
related_workflow_record:
related_validation_record:
related_source_material:
related_knowledge_record:
notes:
```

The metadata block MAY be represented in Markdown front matter, a table, a form, a database record, a sidecar file, or another governed representation.

The representation method does not define the meaning of the Review Record.

The meaning of the Review Record is defined by the explicit fields, the review decision, the approval scope, the reviewed subject, the evidence considered, and the applicable standards or workflows.

A Review Record metadata block SHOULD remain minimal enough for practical use while still preserving the information required for traceability, reviewability, validation, maintenance, and downstream-use control.

A Review Record metadata block MUST NOT rely only on hidden application state, folder location, filename, tag, user-interface state, workflow memory, agent memory, plugin behavior, database behavior, or implementation-specific status labels when review decisions affect governed meaning, approval, privacy, authority, validation, publication, export, migration, or downstream use.

The metadata block SHOULD be completed as accurately as practical during review.

Unknown, unavailable, deferred, not applicable, or unresolved values SHOULD be recorded explicitly rather than silently omitted when the missing value affects interpretation, review, approval, validation, privacy, authority, publication, export, migration, or downstream use.

## 5. Required Review Field Instructions

Required Review Record fields are fields that SHOULD be present whenever a Review Record is created for governed review.

A future specification MAY make some fields mandatory for a narrower review scope.

At the template level, the following fields SHOULD be treated as required for a usable Review Record.

### 5.1 review_record_id

The `review_record_id` field identifies the Review Record itself.

The `review_record_id` SHOULD be unique within the compliant storage environment.

The `review_record_id` MUST NOT be confused with the Object Identity of the reviewed subject.

A Review Record has its own record identity.

The reviewed subject has its own identity.

### 5.2 review_record_title

The `review_record_title` field provides a human-readable title for the Review Record.

The title SHOULD clearly indicate what was reviewed.

The title MAY include the reviewed subject title, review type, review date, or review decision.

The title MUST NOT be treated as stable Object Identity.

### 5.3 review_record_type

The `review_record_type` field identifies the record as a Review Record.

The value SHOULD be:

```yaml
review_record_type: Review Record
```

This field helps humans, agents, workflows, validators, and implementations distinguish Review Records from Knowledge Records, Source Material Intake Records, Agent Activity Records, validation checklists, workflow logs, and governed standards.

### 5.4 review_status

The `review_status` field records the current status of the Review Record.

Recommended values MAY include:

- Draft;
- Pending Review;
- Complete;
- Needs Repair;
- Escalated;
- Superseded;
- Archived.

The review status describes the Review Record.

The review status does not automatically describe the reviewed subject unless the review decision explicitly records that outcome within a defined scope.

### 5.5 created

The `created` field records when the Review Record was created.

The value SHOULD use a consistent date format.

A future specification MAY define the exact date format.

### 5.6 last_updated

The `last_updated` field records when the Review Record was last revised.

The field SHOULD be updated when the Review Record changes in a way that affects review interpretation, decision scope, corrections, escalation, validation, privacy, authority, downstream use, publication, export, or migration.

### 5.7 review_date

The `review_date` field records when the review occurred.

If review occurs across multiple dates, the Review Record SHOULD identify either the final review date or the relevant review date range.

### 5.8 reviewer

The `reviewer` field identifies the human, governed role, workflow participant, or authorized review process responsible for the review decision.

If an agent assisted the review, the agent SHOULD be referenced separately through `related_agent_activity_record` or an equivalent field.

An agent assistant MUST NOT be treated as the reviewer unless a future governed workflow explicitly grants that role.

### 5.9 reviewer_role

The `reviewer_role` field records the reviewer’s role for the review.

Examples MAY include:

- Owner;
- Human Reviewer;
- Standards Reviewer;
- Privacy Reviewer;
- Authority Reviewer;
- Validation Reviewer;
- Workflow Reviewer;
- Implementation Reviewer.

The reviewer role SHOULD clarify the scope of review authority.

The reviewer role MUST NOT imply unlimited approval authority.

### 5.10 review_subject_id

The `review_subject_id` field identifies the governed entity being reviewed.

This field SHOULD reference the stable identifier of the reviewed subject when one exists.

If the reviewed subject does not yet have a stable identifier, the Review Record SHOULD record the best available temporary identifier, source identifier, filename, path, or workflow reference.

Temporary identifiers MUST NOT be treated as stable Object Identity unless a governed process assigns or confirms stable identity.

### 5.11 review_subject_title

The `review_subject_title` field records the human-readable title or label of the reviewed subject.

This field helps humans identify what was reviewed.

The title MUST NOT replace the reviewed subject’s stable identifier where stable identity exists.

### 5.12 review_subject_type

The `review_subject_type` field records what kind of entity was reviewed.

Examples MAY include:

- Knowledge Object;
- Knowledge Record;
- Source Material;
- Source Reference;
- Provenance Record;
- Relationship;
- Metadata Proposal;
- Validation Result;
- Agent Output;
- Workflow Output;
- Draft Record;
- Governed Document;
- Implementation Support File;
- Import Output;
- Export Output;
- Migration Output.

The type SHOULD help determine what standards, workflows, templates, or validation expectations apply.

### 5.13 review_scope

The `review_scope` field records what the review covered.

Examples MAY include:

- structural review;
- metadata review;
- source-reference review;
- provenance review;
- relationship review;
- lifecycle review;
- authority review;
- privacy review;
- validation review;
- workflow review;
- agent-output review;
- publication-readiness review;
- export-readiness review;
- migration-readiness review;
- downstream-use review.

The review scope MUST be clear enough to prevent overextending the review decision beyond what was actually reviewed.

### 5.14 review_decision

The `review_decision` field records the outcome of the review.

Recommended values MAY include:

- Approved;
- Approved with Limits;
- Rejected;
- Deferred;
- Needs Repair;
- Escalated;
- Quarantined;
- Archived;
- Superseded;
- Deprecated;
- No Decision.

The review decision MUST be interpreted only within its stated review scope and approval scope.

A review decision MUST NOT silently authorize publication, export, migration, deletion, identity change, authority change, privacy clearance, or downstream use unless those permissions are explicitly recorded.

### 5.15 approval_scope

The `approval_scope` field records the scope within which approval applies.

If the review decision is not an approval, the field SHOULD record `Not Applicable`, `None`, or an equivalent explicit value.

Approval scope SHOULD identify what use is allowed.

Examples MAY include:

- internal use only;
- draft continuation;
- metadata update only;
- relationship update only;
- source-reference update only;
- workflow progression;
- validation repair completed;
- approved Knowledge Record use;
- publication readiness;
- export readiness;
- migration readiness;
- downstream use within defined limits.

Approval scope MUST NOT be assumed.

Approval for one scope MUST NOT be treated as approval for all scopes.

## 6. Recommended Review Field Instructions

Recommended Review Record fields are fields that SHOULD be included when they improve traceability, reviewability, validation, maintenance, privacy handling, authority handling, downstream-use control, publication review, export review, or migration review.

These fields MAY be omitted when they are not applicable, unavailable, or unnecessary for a low-risk review.

Omitted recommended fields SHOULD NOT create ambiguity where the missing information affects review interpretation or downstream use.

### 6.1 review_subject_location

The `review_subject_location` field records the storage location, path, link, repository reference, archive reference, workflow reference, or implementation reference where the reviewed subject was located at the time of review.

This field supports traceability.

This field MUST NOT define Object Identity.

A reviewed subject may move after review without becoming a different entity.

### 6.2 review_subject_lifecycle_state

The `review_subject_lifecycle_state` field records the lifecycle state of the reviewed subject at the time of review.

This field helps clarify whether the subject was draft, pending review, approved, rejected, deprecated, superseded, archived, restricted, quarantined, pending validation, or needs repair.

The lifecycle state recorded in the Review Record SHOULD NOT be treated as a lifecycle transition unless the review decision explicitly records that transition within a governed scope.

### 6.3 review_subject_authority_level

The `review_subject_authority_level` field records the Authority Level of the reviewed subject at the time of review where known.

This field helps identify whether the reviewed subject had authority implications.

The field MUST NOT assign Authority Level by itself.

Authority assignment requires a governed review decision or applicable authority process.

### 6.4 review_subject_privacy_classification

The `review_subject_privacy_classification` field records the Privacy Classification of the reviewed subject at the time of review where known.

This field helps identify privacy boundaries and handling requirements.

The field MUST NOT clear privacy concerns by itself.

Privacy clearance requires an explicit review decision within a defined privacy scope.

### 6.5 correction_required

The `correction_required` field records whether correction, repair, revision, restructuring, sourcing, reclassification, validation, or other remediation is required.

Recommended values MAY include:

- Yes;
- No;
- Partial;
- Unknown;
- Deferred;
- Not Applicable.

If correction is required, the Review Record SHOULD describe the correction in the correction, repair, and escalation sections of the record.

A correction request is not a completed correction.

### 6.6 escalation_required

The `escalation_required` field records whether unresolved issues must be routed to a higher-authority review process, human reviewer, governance process, privacy review, authority review, validation review, source review, workflow review, or implementation review.

Recommended values MAY include:

- Yes;
- No;
- Conditional;
- Unknown;
- Deferred;
- Not Applicable.

An escalation note is not a completed escalation.

Completion of escalation SHOULD be recorded separately.

### 6.7 validation_result

The `validation_result` field records the validation outcome or validation status considered during review.

Recommended values MAY include:

- Passed;
- Passed with Warnings;
- Failed;
- Not Checked;
- Not Applicable;
- Pending Validation;
- Needs Repair;
- Escalated.

A validation result MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that behavior.

### 6.8 privacy_result

The `privacy_result` field records the privacy outcome or privacy concern identified during review.

Recommended values MAY include:

- Cleared;
- Cleared with Limits;
- Restricted;
- Needs Privacy Review;
- Privacy Risk Identified;
- Not Checked;
- Not Applicable;
- Escalated.

Privacy clearance MUST apply only within the recorded privacy and approval scope.

### 6.9 authority_result

The `authority_result` field records the authority outcome or authority concern identified during review.

Recommended values MAY include:

- Authority Confirmed;
- Authority Limited;
- Authority Rejected;
- Needs Authority Review;
- Authority Risk Identified;
- Not Checked;
- Not Applicable;
- Escalated.

An authority result MUST NOT be treated as unlimited authority assignment.

Authority decisions MUST remain scoped.

### 6.10 source_reference_result

The `source_reference_result` field records whether source references were reviewed and whether they were adequate for the review scope.

Recommended values MAY include:

- Adequate;
- Adequate with Limits;
- Missing;
- Incomplete;
- Conflicting;
- Unverified;
- Not Checked;
- Not Applicable;
- Needs Repair;
- Escalated.

Source-reference adequacy SHOULD be evaluated only within the stated review scope.

### 6.11 provenance_result

The `provenance_result` field records whether provenance was reviewed and whether it was adequate for the review scope.

Recommended values MAY include:

- Adequate;
- Adequate with Limits;
- Missing;
- Incomplete;
- Unverified;
- Not Checked;
- Not Applicable;
- Needs Repair;
- Escalated.

Provenance adequacy SHOULD be sufficient to explain origin, transformation, review, agent involvement, workflow involvement, import context, export context, migration context, or decision context where those affect interpretation.

### 6.12 relationship_result

The `relationship_result` field records whether relationships were reviewed and whether they were accepted, rejected, repaired, deferred, or escalated.

Recommended values MAY include:

- Accepted;
- Accepted with Limits;
- Rejected;
- Needs Repair;
- Proposed Only;
- Not Checked;
- Not Applicable;
- Escalated.

A relationship result MUST NOT silently convert proposed relationships into approved relationships unless the review decision explicitly approves them within scope.

### 6.13 downstream_use_result

The `downstream_use_result` field records whether the reviewed subject may be used downstream.

Recommended values MAY include:

- Permitted;
- Permitted with Limits;
- Blocked;
- Pending Repair;
- Pending Review;
- Pending Validation;
- Restricted;
- Not Applicable;
- Escalated.

Downstream use MUST remain scoped.

Downstream-use permission MUST NOT imply publication, export, migration, indexing, synchronization, or agent access unless explicitly recorded.

### 6.14 publication_result

The `publication_result` field records whether the reviewed subject is ready for publication within a defined publication scope.

Recommended values MAY include:

- Ready;
- Ready with Limits;
- Not Ready;
- Blocked;
- Pending Privacy Review;
- Pending Authority Review;
- Pending Validation;
- Not Applicable;
- Escalated.

Publication readiness MUST NOT be assumed from general approval.

### 6.15 export_result

The `export_result` field records whether the reviewed subject is ready for export within a defined export scope.

Recommended values MAY include:

- Ready;
- Ready with Limits;
- Not Ready;
- Blocked;
- Pending Privacy Review;
- Pending Authority Review;
- Pending Validation;
- Not Applicable;
- Escalated.

Export readiness MUST NOT be assumed from general approval.

### 6.16 migration_result

The `migration_result` field records whether the reviewed subject is ready for migration within a defined migration scope.

Recommended values MAY include:

- Ready;
- Ready with Limits;
- Not Ready;
- Blocked;
- Pending Repair;
- Pending Validation;
- Not Applicable;
- Escalated.

Migration readiness MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and review traceability.

### 6.17 related records

The following fields SHOULD reference related records where applicable:

```yaml
related_agent_activity_record:
related_workflow_record:
related_validation_record:
related_source_material:
related_knowledge_record:
```

These fields help preserve traceability across agent activity, workflow activity, validation activity, source material, and Knowledge Records.

Related record fields MUST NOT merge the meaning of separate records.

A Review Record may reference another record without becoming that record.

### 6.18 notes

The `notes` field MAY record additional review context.

Notes SHOULD be concise, relevant, and scoped to the review.

Notes MUST NOT be treated as approved Knowledge Record content unless a governed review decision explicitly approves their incorporation into a Knowledge Record.

## 7. Review Subject and Evidence

The Review Subject and Evidence section records what was reviewed and what information, sources, records, outputs, findings, or context supported the review.

This section exists so a future human, agent, workflow, validator, storage system, or implementation can determine why the review decision was made and what evidence the reviewer considered.

A Review Record SHOULD identify the Review Subject with enough detail to distinguish it from related records, drafts, files, source artifacts, workflow outputs, agent outputs, validation records, or implementation-specific representations.

The Review Subject SHOULD be identified by stable identifier where available.

If a stable identifier is not available, the Review Record SHOULD identify the Review Subject using the best available temporary identifier, filename, title, path, source identifier, workflow reference, import reference, export reference, migration reference, or other traceable locator.

A temporary identifier, filename, title, path, or implementation-specific reference MUST NOT be treated as stable Object Identity unless a governed process assigns or confirms that identity.

A Review Record SHOULD describe the Review Subject in plain language.

The description SHOULD make clear:

- what entity was reviewed;
- why the entity required review;
- what review scope applied;
- what state the entity was in at the time of review;
- what evidence was considered;
- what evidence was missing, incomplete, conflicting, restricted, or unresolved;
- whether agent output, workflow output, validation output, or source material influenced the review.

Evidence MAY include:

- Source Material;
- Source References;
- provenance records;
- metadata;
- relationships;
- validation results;
- agent activity records;
- workflow records;
- prior review records;
- Knowledge Records;
- draft records;
- import records;
- export records;
- migration records;
- maintenance records;
- governed standards;
- governed specifications;
- reviewer observations.

Evidence listed in a Review Record SHOULD remain distinguishable from the review decision.

Evidence supports review.

Evidence does not become approval by itself.

Evidence does not become Knowledge Record content by itself.

Evidence does not become validation by itself.

Evidence does not become source truth by itself.

If evidence is missing, incomplete, unavailable, restricted, unverifiable, conflicting, outdated, or uncertain, the Review Record SHOULD record that limitation.

A Review Record SHOULD identify whether the evidence was sufficient for the review scope.

A Review Record MUST NOT imply that evidence was reviewed when it was not reviewed.

A Review Record MUST NOT imply that source support exists when source support is missing, unavailable, or unverified.

A Review Record MUST NOT treat agent-generated summaries, classifications, metadata proposals, relationship proposals, validation findings, or recommendations as reviewed evidence unless they were actually considered during review.

Agent output MAY support review.

Agent output does not replace reviewer judgment.

Workflow output MAY support review.

Workflow output does not replace reviewer judgment unless a governed workflow explicitly defines that authority.

Validation output MAY support review.

Validation output does not replace approval unless a governed workflow or specification explicitly defines that behavior.

The Review Subject and Evidence section SHOULD preserve enough context to support future maintenance, reapproval, supersession, deprecation, archival, repair, escalation, publication review, export review, migration review, or downstream-use review.

## 8. Review Decision Tracking

The Review Decision Tracking section records the outcome of the review and the scope in which that outcome applies.

This section exists to prevent review decisions from becoming ambiguous, overextended, undocumented, or confused with validation, authority, privacy, workflow routing, agent confidence, implementation status, or downstream-use permission.

A Review Record SHOULD state the review decision clearly.

Recommended review decision values MAY include:

- Approved;
- Approved with Limits;
- Rejected;
- Deferred;
- Needs Repair;
- Escalated;
- Quarantined;
- Archived;
- Superseded;
- Deprecated;
- No Decision.

A review decision MUST be interpreted only within the recorded review scope and approval scope.

A review decision MUST NOT be treated as approval for unrelated scopes.

Approval for one scope MUST NOT be treated as approval for all scopes.

Approval for internal use MUST NOT be treated as approval for publication.

Approval for review completion MUST NOT be treated as approval for export.

Approval for export MUST NOT be treated as approval for publication.

Approval for publication MUST NOT be treated as approval for migration.

Approval for metadata correction MUST NOT be treated as approval for relationship changes.

Approval for relationship changes MUST NOT be treated as approval for source-reference adequacy.

Approval for source-reference adequacy MUST NOT be treated as Authority Level assignment.

Approval for validation repair MUST NOT be treated as full knowledge approval unless explicitly recorded.

A Review Record SHOULD identify whether the decision affects:

- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- Source References;
- provenance;
- relationships;
- metadata;
- storage routing;
- workflow progression;
- agent-output acceptance;
- publication readiness;
- export readiness;
- migration readiness;
- downstream-use readiness.

If the review decision changes Lifecycle State, the Review Record SHOULD identify the prior state, the new state, the reason for the transition, and the scope of the transition.

If the review decision affects Authority Level, the Review Record SHOULD identify the authority assignment, limitation, rejection, deferral, or escalation.

Authority decisions MUST remain scoped.

If the review decision affects Privacy Classification, the Review Record SHOULD identify the privacy classification, privacy scope, access limits, exposure limits, publication limits, export limits, indexing limits, synchronization limits, backup limits, agent-access limits, workflow-access limits, or downstream-use limits.

Privacy clearance MUST remain scoped.

If the review decision affects validation, the Review Record SHOULD identify whether validation passed, passed with warnings, failed, was not checked, remains pending, requires repair, or requires escalation.

Validation findings MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that behavior.

If the review decision affects relationships, the Review Record SHOULD identify whether relationship proposals were accepted, accepted with limits, rejected, deferred, repaired, or escalated.

Proposed relationships MUST NOT become approved relationships unless explicitly approved within scope.

If the review decision affects Source References or provenance, the Review Record SHOULD identify whether source support and provenance were adequate, limited, missing, incomplete, conflicting, unverified, repaired, or escalated.

If the review decision affects downstream use, the Review Record SHOULD identify the permitted or blocked downstream-use scope.

Downstream-use permission MUST NOT imply publication, export, migration, indexing, synchronization, backup, agent access, or implementation exposure unless explicitly recorded.

If no decision was made, the Review Record SHOULD state why no decision was made and what must happen next.

A Review Record SHOULD preserve the reviewer’s reasoning at a level sufficient for future review without becoming excessive, speculative, or duplicative.

The reviewer’s reasoning SHOULD explain the decision.

The reviewer’s reasoning MUST NOT introduce unreviewed Knowledge Record content unless a governed update process incorporates and approves that content.

## 9. Corrections, Repairs, and Escalations

The Corrections, Repairs, and Escalations section records what must be fixed, routed, restricted, clarified, re-reviewed, validated, or escalated before the reviewed subject may proceed.

This section exists to ensure review findings result in traceable follow-up rather than informal, forgotten, or ambiguous action.

A Review Record SHOULD identify correction or repair requirements when the reviewed subject contains structural, metadata, identity, relationship, source-reference, provenance, lifecycle, authority, privacy, validation, storage, workflow, agent, implementation, import, export, migration, publication, or downstream-use issues.

A correction request SHOULD identify:

- what issue was found;
- where the issue appears;
- why the issue matters;
- what correction is required;
- who or what should perform the correction where known;
- what review is required after correction;
- whether validation is required after correction;
- whether privacy review is required after correction;
- whether authority review is required after correction;
- whether downstream use remains blocked until correction is complete.

A correction request is not a completed correction.

A repair note is not a completed repair.

An escalation note is not a completed escalation.

A Review Record SHOULD distinguish between:

- correction requested;
- correction completed;
- repair requested;
- repair completed;
- escalation required;
- escalation completed;
- validation required;
- validation completed;
- privacy review required;
- privacy review completed;
- authority review required;
- authority review completed;
- downstream use blocked;
- downstream use cleared.

Corrections MAY include:

- fixing Markdown structure;
- correcting metadata;
- clarifying title or description;
- repairing Source References;
- adding missing provenance;
- revising relationship proposals;
- correcting lifecycle state;
- correcting Authority Level;
- correcting Privacy Classification;
- resolving validation warnings;
- resolving validation errors;
- improving review notes;
- correcting agent-output interpretation;
- correcting workflow routing;
- repairing import context;
- repairing export context;
- repairing migration context.

Repairs SHOULD preserve Object Identity unless a governed identity-change process determines that identity must change.

Repairs MUST NOT silently merge, split, delete, supersede, deprecate, publish, export, migrate, or reclassify a reviewed subject without an explicit governed decision.

Escalation SHOULD occur when review identifies:

- unresolved ambiguity;
- source conflict;
- missing evidence;
- provenance weakness;
- privacy risk;
- authority risk;
- validation failure;
- identity conflict;
- duplicate conflict;
- relationship conflict;
- lifecycle conflict;
- publication risk;
- export risk;
- migration risk;
- destructive action;
- implementation dependency;
- governance conflict;
- human judgment requirement.

Escalation SHOULD identify the escalation target where known.

Escalation targets MAY include:

- human reviewer;
- standards reviewer;
- privacy reviewer;
- authority reviewer;
- validation reviewer;
- workflow reviewer;
- implementation reviewer;
- governance process;
- future specification;
- future runbook;
- future hand-off summary.

If escalation is required, the Review Record SHOULD state what action is blocked until escalation is resolved.

Blocked actions MAY include:

- approval;
- lifecycle transition;
- Authority Level assignment;
- privacy clearance;
- validation acceptance;
- relationship approval;
- metadata update;
- Knowledge Record approval;
- workflow progression;
- publication;
- export;
- migration;
- deletion;
- downstream use;
- agent execution.

A Review Record SHOULD record whether corrected or repaired material requires re-review.

If re-review is required, the Review Record SHOULD identify the re-review scope.

Re-review scope SHOULD be limited to the affected issue unless the correction materially changes the reviewed subject, source support, provenance, privacy handling, authority handling, validation state, relationship meaning, lifecycle state, publication readiness, export readiness, migration readiness, or downstream-use readiness.

Corrections, repairs, and escalations SHOULD remain traceable across future maintenance, validation, review, approval, rejection, supersession, deprecation, archival, publication review, export review, migration review, or downstream-use review.

## 10. Validation, Privacy, Authority, and Downstream-Use Notes

The Validation, Privacy, Authority, and Downstream-Use Notes section records review findings that affect whether the reviewed subject may be trusted, exposed, used, routed, published, exported, migrated, indexed, synchronized, backed up, processed by agents, or used downstream.

This section exists to keep high-risk review concerns explicit and scoped.

A Review Record SHOULD include validation notes when the review identifies structural, metadata, identity, relationship, Source Reference, provenance, lifecycle, authority, privacy, compatibility, workflow, agent, implementation, import, export, migration, publication, or downstream-use issues.

Validation notes SHOULD identify:

- what validation was performed;
- what validation scope applied;
- what validation findings were found;
- whether findings were errors, warnings, limitations, or unresolved concerns;
- whether repair is required;
- whether revalidation is required;
- whether validation affects approval, publication, export, migration, or downstream use.

A validation finding MUST NOT be treated as approval unless a governed workflow or specification explicitly defines that behavior.

A validation pass MUST NOT override unresolved privacy, authority, source-reference, provenance, relationship, lifecycle, or downstream-use concerns.

A Review Record SHOULD include privacy notes when the reviewed subject affects access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream use.

Privacy notes SHOULD identify:

- what Privacy Classification applies;
- what privacy scope applies;
- whether privacy review was completed;
- whether privacy concerns remain unresolved;
- whether access is limited;
- whether publication is blocked or limited;
- whether export is blocked or limited;
- whether indexing is blocked or limited;
- whether synchronization is blocked or limited;
- whether backup handling is limited;
- whether agent access is blocked or limited;
- whether downstream use is blocked or limited.

Privacy clearance MUST remain scoped.

Privacy clearance for one use MUST NOT be treated as privacy clearance for every use.

A Review Record SHOULD include authority notes when the reviewed subject affects interpretation, governance weight, review weight, trust boundary, approval scope, publication readiness, export readiness, migration readiness, or downstream-use authority.

Authority notes SHOULD identify:

- what Authority Level applies;
- what authority scope applies;
- whether authority was confirmed, limited, rejected, deferred, or escalated;
- whether authority depends on source support;
- whether authority depends on provenance;
- whether authority depends on validation;
- whether authority depends on privacy review;
- whether authority affects downstream use.

Authority Level MUST remain distinguishable from Lifecycle State, Validation State, Privacy Classification, source reliability, agent confidence, workflow completion, implementation visibility, publication status, or storage location.

An authority note MUST NOT assign unlimited authority unless the review decision explicitly grants authority within a defined scope.

A Review Record SHOULD include downstream-use notes when the reviewed subject may be used by later humans, agents, workflows, validators, implementations, publication processes, export processes, migration processes, indexing processes, synchronization processes, backup processes, or decision-support processes.

Downstream-use notes SHOULD identify:

- what downstream use is permitted;
- what downstream use is blocked;
- what downstream use is limited;
- what review must occur before downstream use;
- what validation must occur before downstream use;
- what privacy clearance must occur before downstream use;
- what authority review must occur before downstream use;
- what repair must occur before downstream use;
- what escalation must be resolved before downstream use.

Downstream-use permission MUST remain scoped.

Downstream-use permission MUST NOT imply publication, export, migration, indexing, synchronization, backup, agent access, implementation exposure, or external sharing unless explicitly recorded.

A Review Record SHOULD explicitly state when downstream use is blocked.

Blocked downstream use SHOULD identify the reason for the block and the condition required to remove the block.

A Review Record SHOULD preserve these notes in a way that supports future maintenance, validation, review, reapproval, supersession, deprecation, archival, publication review, export review, migration review, or downstream-use review.

## 11. Review Completion Checklist

The Review Completion Checklist provides a practical final check before a Review Record is treated as complete.

The checklist exists to ensure that review decisions are traceable, scoped, and usable without requiring the Review Record to become a separate workflow standard, validation checklist, Knowledge Record, Agent Activity Record, or source record.

A Review Record SHOULD be considered complete only when the reviewer can answer the applicable checklist items.

### 11.1 Identity and Subject Checklist

- The Review Record identifies itself.
- The Review Subject is clearly identified.
- Stable identifiers are used where available.
- Temporary identifiers are clearly treated as temporary where applicable.
- The Review Subject is not confused with the Review Record.
- The Review Subject is not confused with Source Material, agent output, workflow output, validation output, or implementation-specific representation.

### 11.2 Review Scope Checklist

- The review scope is recorded.
- The approval scope is recorded where applicable.
- The review decision is limited to the stated scope.
- Approval for one scope is not treated as approval for all scopes.
- No unstated publication, export, migration, deletion, identity change, authority change, privacy clearance, or downstream-use permission is implied.

### 11.3 Evidence Checklist

- Evidence considered during review is identified.
- Missing evidence is recorded where relevant.
- Incomplete evidence is recorded where relevant.
- Conflicting evidence is recorded where relevant.
- Restricted evidence is recorded where relevant.
- Agent output is not treated as reviewed evidence unless it was actually reviewed.
- Workflow output is not treated as reviewed evidence unless it was actually reviewed.
- Validation output is not treated as approval unless a governed workflow or specification explicitly allows it.

### 11.4 Decision Checklist

- The review decision is recorded.
- The reviewer or review role is recorded.
- The review date is recorded.
- Any limits on the decision are recorded.
- Any unresolved issues are recorded.
- Any required corrections are recorded.
- Any required repairs are recorded.
- Any required escalations are recorded.
- Any blocked actions are recorded.

### 11.5 Validation Checklist

- Validation findings are recorded where applicable.
- Validation scope is clear where applicable.
- Validation warnings are not treated as approval.
- Validation errors are not ignored.
- Required revalidation is recorded where applicable.
- Validation state remains distinguishable from Lifecycle State, Authority Level, Privacy Classification, and review approval.

### 11.6 Privacy Checklist

- Privacy Classification is recorded where applicable.
- Privacy scope is recorded where applicable.
- Privacy concerns are recorded where applicable.
- Privacy clearance is scoped where granted.
- Publication, export, indexing, synchronization, backup, agent access, implementation access, and downstream-use limits are recorded where applicable.
- Privacy concerns are not cleared by implication.

### 11.7 Authority Checklist

- Authority Level is recorded where applicable.
- Authority scope is recorded where applicable.
- Authority limits are recorded where applicable.
- Authority concerns are recorded where applicable.
- Authority assignment is not implied from validation, lifecycle state, privacy classification, agent confidence, workflow completion, publication status, or implementation visibility.

### 11.8 Relationship and Source Checklist

- Relationship findings are recorded where applicable.
- Proposed relationships are not treated as approved unless explicitly approved.
- Source Reference findings are recorded where applicable.
- Provenance findings are recorded where applicable.
- Missing, incomplete, conflicting, or unverified Source References are recorded where applicable.
- Missing, incomplete, conflicting, or unverified provenance is recorded where applicable.

### 11.9 Downstream-Use Checklist

- Downstream-use permission is recorded where applicable.
- Downstream-use limits are recorded where applicable.
- Publication readiness is recorded where applicable.
- Export readiness is recorded where applicable.
- Migration readiness is recorded where applicable.
- Blocked downstream use is recorded where applicable.
- Conditions for clearing blocked downstream use are recorded where applicable.

### 11.10 Completion Checklist

- The Review Record is complete enough for future review.
- The Review Record is not duplicating the reviewed entity unnecessarily.
- The Review Record is not replacing the reviewed entity.
- The Review Record is not replacing Source Material.
- The Review Record is not replacing validation.
- The Review Record is not replacing workflow approval requirements.
- The Review Record is not replacing agent activity records.
- The Review Record is not creating hidden implementation dependency.
- The Review Record remains human-readable.
- The Review Record remains AI-readable.
- The Review Record remains software-neutral and AI-neutral.

If checklist items cannot be completed, the Review Record SHOULD identify what remains unresolved and whether repair, escalation, validation, privacy review, authority review, source review, workflow review, or governance review is required.

## 12. Template Success Criteria

TEMPLATE-0004 is successful when it provides a practical, repeatable, and implementation-independent structure for recording review decisions without allowing review records to replace the standards, workflows, validations, records, sources, or governed entities they reference.

A completed Review Record SHOULD make clear:

- what was reviewed;
- who or what reviewed it;
- when the review occurred;
- what review scope applied;
- what evidence was considered;
- what evidence was missing or limited;
- what decision was made;
- what approval scope applies;
- what was accepted;
- what was rejected;
- what requires correction;
- what requires repair;
- what requires escalation;
- what remains unresolved;
- what downstream use is permitted;
- what downstream use is blocked;
- what publication, export, or migration limits apply.

TEMPLATE-0004 succeeds when it preserves the distinction between review activity and review authority.

TEMPLATE-0004 succeeds when it preserves the distinction between reviewer notes and approved Knowledge Record content.

TEMPLATE-0004 succeeds when it preserves the distinction between correction requests and completed corrections.

TEMPLATE-0004 succeeds when it preserves the distinction between escalation notes and completed escalation.

TEMPLATE-0004 succeeds when it preserves the distinction between validation findings and approval.

TEMPLATE-0004 succeeds when it preserves the distinction between privacy concerns and privacy clearance.

TEMPLATE-0004 succeeds when it preserves the distinction between authority concerns and Authority Level assignment.

TEMPLATE-0004 succeeds when it preserves the distinction between agent recommendations and reviewer decisions.

TEMPLATE-0004 succeeds when it preserves the distinction between workflow routing and lifecycle approval.

TEMPLATE-0004 succeeds when it preserves the distinction between downstream-use permission and publication, export, migration, indexing, synchronization, backup, agent access, or implementation exposure.

TEMPLATE-0004 succeeds when humans can use it without unnecessary complexity.

TEMPLATE-0004 succeeds when agents can read it without becoming authorities.

TEMPLATE-0004 succeeds when workflows can reference it without redefining review meaning.

TEMPLATE-0004 succeeds when validators can inspect it without converting validation into approval.

TEMPLATE-0004 succeeds when implementations can store, display, search, export, migrate, or archive it without making implementation behavior the source of review meaning.

TEMPLATE-0004 succeeds when future maintenance can determine what review occurred, what decision was made, what scope applied, what remains unresolved, and what must happen next.

TEMPLATE-0004 MUST remain software-neutral and AI-neutral.

TEMPLATE-0004 MUST NOT depend on Obsidian, Codex, ChatGPT, Claude, GitHub, a specific file system, a specific model, a specific plugin, a specific repository layout, or a specific implementation.

TEMPLATE-0004 is complete when it can be used to create Review Records that are explicit, scoped, traceable, reviewable, source-aware, privacy-aware, authority-aware, validation-aware, downstream-use-aware, portable, human-readable, AI-readable, and governed by The Brain Standard.
