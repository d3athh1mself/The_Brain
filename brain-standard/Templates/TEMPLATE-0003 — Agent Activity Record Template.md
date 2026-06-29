# TEMPLATE-0003 — Agent Activity Record Template

Document ID: TEMPLATE-0003
Title: Agent Activity Record Template
Version: 0.1.0
Status: Draft
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Template
Phase: Phase 3 — Agent Framework
Milestone: Template Set — Bare Usable Deployment
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; TEMPLATE-0001 — Knowledge Record Template; TEMPLATE-0002 — Source Material Intake Template
Supersedes: None
Superseded By: None
Related: TEMPLATE-0004 — Review Record Template; VALID-0001 — Bare Usable Validation Checklist

## 1. Purpose

The purpose of TEMPLATE-0003 is to provide a copy/paste-ready Agent Activity Record structure for documenting agent or subagent work within The Brain Standard.

An Agent Activity Record records what an agent did, what material the agent interacted with, what outputs the agent produced, what proposals or concerns were raised, what boundaries applied, and what human review or validation remains required.

TEMPLATE-0003 exists so agent assistance remains traceable, reviewable, and governed.

This template is used when an agent or subagent reads, inspects, searches, classifies, summarizes, extracts, proposes, drafts, validates, compares, modifies, moves, routes, flags, or otherwise assists with governed work.

An Agent Activity Record should answer:

- which agent or subagent acted;
- what role the agent was operating under;
- what task, workflow, file, source, Knowledge Record, template, standard, or governed entity the agent interacted with;
- what action the agent performed;
- what output the agent produced;
- what proposals the agent made;
- what changes, if any, the agent applied;
- what uncertainty, limitation, or ambiguity remained;
- what privacy, authority, validation, source, provenance, relationship, lifecycle, or storage concerns appeared;
- what review, approval, validation, repair, escalation, or follow-up is required;
- what a human should verify before accepting, relying on, publishing, exporting, moving, deleting, or approving any resulting output.

An Agent Activity Record is not proof that an agent output is correct.

An Agent Activity Record is not approval.

An Agent Activity Record is not validation by itself.

An Agent Activity Record is not a Knowledge Record.

An Agent Activity Record is not a Review Record.

An Agent Activity Record is not a replacement for AG-0001, AG-0002, AG-0003, WF-0001, WF-0002, WF-0003, WF-0004, KS-0009, VALID-0001, or any future agent, workflow, validation, or review specification.

The primary purpose of TEMPLATE-0003 is to preserve traceability between agent activity and governed knowledge work without allowing agent activity to become unreviewable authority.

## 2. Relationship to Prior Standards and Templates

TEMPLATE-0003 is subordinate to the constitutional foundation of The Brain Standard.

TEMPLATE-0003 depends on:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model.

The constitutional foundation establishes that The Brain must remain implementation-independent, portable, human-readable, AI-readable, reviewable, and governed. TEMPLATE-0003 supports that foundation by ensuring agent participation is documented without allowing any agent, model, implementation, workflow, tool, plugin, or automation system to redefine the standard by habit or convenience.

TEMPLATE-0003 depends on the Phase 1 Knowledge Standards because agent activity may interact with Knowledge Objects, Knowledge Records, metadata, relationships, Source References, provenance, lifecycle state, Authority Level, Privacy Classification, and validation state.

TEMPLATE-0003 must preserve the distinctions defined by the Knowledge Standards, including:

- Source Material is not the same as a Knowledge Record.
- Agent output is not the same as reviewed knowledge.
- Agent confidence is not the same as Authority Level.
- Agent validation support is not the same as approval.
- Agent-suggested metadata is not automatically accepted metadata.
- Agent-suggested relationships are not automatically approved relationships.
- Agent-detected privacy concerns are not completed privacy review.
- Agent-detected validation concerns are not completed validation.
- Agent-created drafts do not become approved Knowledge Records merely because they were generated.

TEMPLATE-0003 depends on KS-0005 because agent activity may involve extraction, transformation, source interpretation, provenance notes, source-reference proposals, or evidence handling. Agent Activity Records should preserve enough source and provenance context for later review.

TEMPLATE-0003 depends on KS-0008 because agents may encounter, infer, expose, summarize, classify, or route privacy-sensitive material. Agent Activity Records must record privacy concerns without treating an agent’s privacy note as a final privacy determination.

TEMPLATE-0003 depends on KS-0009 because agents may perform or support validation checks. Agent Activity Records must distinguish validation findings, validation warnings, validation errors, validation scope, and unresolved validation concerns from approval or final acceptance.

TEMPLATE-0003 depends on SS-0001 and SS-0002 because agent activity may involve files, folders, source areas, draft areas, review areas, Knowledge Record areas, archive areas, implementation-support areas, or workflow-support areas. Storage location may be recorded for traceability, but storage location must not define Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, or governed meaning by itself.

TEMPLATE-0003 depends on AG-0001 because AG-0001 defines agent operating boundaries. TEMPLATE-0003 does not grant permissions. It records activity performed under permissions, boundaries, prohibitions, limits, or review requirements defined elsewhere.

TEMPLATE-0003 depends on WF-0001 because agent activity may occur during knowledge ingestion, source intake, extraction, classification, draft Knowledge Record creation, metadata suggestion, relationship suggestion, validation support, routing, or reporting.

TEMPLATE-0003 depends on WF-0002 because agent outputs may require review, approval, rejection, repair, revision, escalation, privacy review, authority review, source review, relationship review, validation review, or lifecycle handling.

TEMPLATE-0003 relates to TEMPLATE-0001 because an agent may draft, inspect, validate, or propose changes to a Knowledge Record. The Agent Activity Record documents the agent’s work; it does not replace the Knowledge Record.

TEMPLATE-0003 relates to TEMPLATE-0002 because an agent may assist with Source Material intake. The Agent Activity Record documents the agent’s work; it does not replace the Source Material Intake Record.

TEMPLATE-0003 relates to TEMPLATE-0004 because agent activity may later require human review. The Agent Activity Record records what the agent did; the Review Record records review decisions, corrections, approvals, rejections, repairs, escalations, and reviewer conclusions.

## 3. Template Scope and Use Rules

TEMPLATE-0003 applies to records created to document agent or subagent activity.

This template should be used when agent activity affects or may affect:

- Source Material;
- Source Material intake;
- Knowledge Objects;
- Knowledge Records;
- metadata;
- relationships;
- Source References;
- provenance;
- lifecycle state;
- Authority Level;
- Privacy Classification;
- validation state;
- storage placement;
- draft creation;
- review routing;
- workflow outputs;
- implementation-support files;
- import, export, migration, publication, synchronization, indexing, or downstream-use readiness;
- governed documents;
- templates;
- standards;
- specifications;
- runbooks;
- validation checklists;
- hand-off summaries.

An Agent Activity Record should be created when an agent performs material work that a future human, validator, workflow, implementation, or agent may need to inspect, reproduce, verify, accept, reject, correct, repair, or escalate.

This template may be used for:

- read-only inspection;
- source review support;
- summarization;
- extraction;
- classification;
- metadata proposal;
- relationship proposal;
- Source Reference proposal;
- provenance note proposal;
- privacy concern detection;
- authority concern detection;
- validation support;
- duplicate or identity concern detection;
- draft Knowledge Record creation;
- draft governed document creation;
- template completion;
- syntax review;
- spelling and grammar review;
- standards consistency review;
- workflow support;
- storage placement recommendation;
- file movement recommendation;
- implementation-support review;
- hand-off preparation.

This template must not be used as:

- an agent permission standard;
- an agent role specification;
- an approval record;
- a Review Record;
- a Knowledge Record;
- a Source Material Intake Record;
- a validation checklist;
- a workflow runbook;
- a storage layout rule;
- a privacy classification decision;
- an authority assignment decision;
- a publication approval;
- an export approval;
- a migration approval;
- a deletion approval;
- an implementation-specific log that cannot be interpreted outside one tool.

An Agent Activity Record may document that an agent proposed, drafted, modified, or recommended something.

An Agent Activity Record must not treat the agent’s proposal, draft, modification, recommendation, confidence, validation result, classification, summary, or warning as approved unless a separate governed review or workflow record establishes that approval.

Agent Activity Records should remain software-neutral and AI-neutral.

This template must not require Obsidian, Codex, ChatGPT, Claude, local AI, a specific model provider, a specific repository host, a specific plugin, a specific user interface, a specific automation framework, or a specific runtime.

Implementation-specific details may be recorded when useful for traceability, but they must remain clearly distinguishable from standard-level meaning.

An Agent Activity Record should capture enough information to support later review while avoiding unnecessary duplication of full source material, full Knowledge Record content, full review decisions, full validation reports, or full workflow logs when those belong in separate governed records.

An Agent Activity Record is complete only when it clearly identifies:

- the agent activity being recorded;
- the actor or agent role involved;
- the governed entity or material touched;
- the action performed;
- the output produced;
- the boundaries or permissions relevant to the activity;
- the proposals, changes, or recommendations made;
- the uncertainty, limitation, or unresolved issue remaining;
- the privacy, authority, validation, source, provenance, lifecycle, relationship, storage, or workflow concerns raised;
- the human review, validation, repair, escalation, or follow-up required.

TEMPLATE-0003 succeeds when future humans, agents, workflows, validators, storage systems, and implementations can determine what an agent did without confusing agent activity with authority, review, validation, approval, governed knowledge, or implementation-specific behavior.

## 4. Agent Activity Metadata Block

Use the following metadata block at the beginning of each Agent Activity Record.

The metadata block exists to identify the activity, the agent or subagent involved, the governed material touched, the operation performed, the output produced, and the review or validation requirements that remain.

```text
Agent Activity Record ID:
Record Title:
Record Type: Agent Activity Record
Template Used: TEMPLATE-0003 — Agent Activity Record Template
Created:
Last Updated:
Activity Date:
Activity Status:

Agent Name or Identifier:
Agent Role:
Agent Type:
Permission / Boundary Reference:
Human Request or Trigger:
Workflow Context:

Activity Type:
Operation Mode:
Target Entity Type:
Target Entity Identifier:
Target Entity Title or Label:
Target Entity Location or Reference:
Related Source Material:
Related Knowledge Record:
Related Intake Record:
Related Review Record:
Related Validation Record:

Output Type:
Output Location or Reference:
Change Applied:
Change Summary:
Proposal Summary:
Uncertainty or Limitation:
Privacy Concern:
Authority Concern:
Validation Concern:
Source / Provenance Concern:
Relationship Concern:
Lifecycle Concern:
Storage or Placement Concern:
Escalation Required:
Human Review Required:
Validation Required:
Follow-Up Required:

Reviewed By:
Review Date:
Review Outcome:
Notes:
```

The metadata block may be represented in Markdown, front matter, a table, a form, a database row, a sidecar file, or another implementation-specific structure when needed.

The representation method does not define the meaning of the fields.

The meaning of the fields must remain governed by The Brain Standard and this template.

An implementation may hide, display, sort, search, or transform these fields for usability, but it must not change their governed meaning by interface behavior alone.

Field values may be left blank when unknown, unavailable, not applicable, or pending review.

Blank fields should not be treated as approval, rejection, validation, privacy clearance, authority assignment, or workflow completion.

Where a field is unknown but important to later review, the field should be marked as one of the following:

```text
Unknown
Not Applicable
Pending Review
Pending Validation
Pending Human Decision
Restricted
Not Recorded
```

These placeholder values are operational aids.

They do not replace governed lifecycle state, authority level, Privacy Classification, validation state, review decision, approval decision, or workflow state.

An Agent Activity Record may include additional implementation-specific fields when needed.

Implementation-specific fields must remain clearly distinguishable from standard-level fields.

Implementation-specific fields must not become required standard fields unless a future governed standard, specification, implementation profile, or template formally defines them.

## 5. Required Agent Activity Field Instructions

The following fields should be treated as required for a basic Agent Activity Record unless a future governed specification defines a narrower record profile.

**Agent Activity Record ID** identifies the specific Agent Activity Record.

This identifier belongs to the activity record.

It does not define the Object Identity of any Knowledge Object, Knowledge Record, Source Material, Review Record, or Validation Record referenced by the activity.

**Record Title** provides a human-readable title for the activity record.

The title should briefly describe the activity without replacing the record identifier.

A title may change for clarity.

The Agent Activity Record ID should remain stable once assigned.

**Record Type** identifies the record as an Agent Activity Record.

The value should remain:

```text
Agent Activity Record
```

**Template Used** identifies the template used to create the record.

The value should identify TEMPLATE-0003 and should preserve the template version where practical.

**Created** records when the Agent Activity Record was created.

**Last Updated** records when the Agent Activity Record was last materially revised.

Minor formatting changes may update this field if the implementation or workflow requires it.

**Activity Date** records when the agent activity occurred.

If the activity occurred across multiple sessions, the field may contain a date range or refer to a more detailed activity log.

**Activity Status** records the status of this Agent Activity Record.

Activity Status does not define the Lifecycle State of the governed entity touched by the agent.

Recommended activity status values include:

```text
Draft
Complete
Pending Human Review
Pending Validation
Needs Repair
Escalated
Archived
```

**Agent Name or Identifier** records the agent, subagent, automation, script, model-assisted actor, or assistant that performed or assisted the activity.

When the exact agent is unknown, the field should state:

```text
Unknown
```

**Agent Role** records the role the agent was operating under.

Examples may include:

```text
Syntax Inspector
Standards Validator
Metadata Agent
Relationship Agent
Source / Provenance Agent
Privacy Agent
Workflow Agent
Duplicate / Identity Agent
Handoff Agent
Implementation Agent
General Assistant
```

Agent Role records the operating role.

It does not grant permission by itself.

**Agent Type** records the general kind of actor involved.

Examples may include:

```text
Human-directed AI assistant
Subagent
Automation script
Validation tool
Workflow assistant
Implementation assistant
Manual human-assisted record
```

**Permission / Boundary Reference** identifies the rule, instruction, workflow, standard, permission profile, or operating boundary that authorized or limited the agent activity.

This field should reference AG-0001, a future agent specification, a workflow standard, a runbook, or a specific human instruction where applicable.

This field records boundaries.

It does not create new permissions.

**Human Request or Trigger** records why the agent activity occurred.

Examples include:

```text
User request
Workflow step
Validation finding
Review request
Maintenance trigger
Import review
Source intake
Template creation
Handoff preparation
```

**Workflow Context** records the workflow, milestone, phase, or process in which the activity occurred.

Examples include:

```text
Knowledge ingestion
Review and approval
Maintenance and update
Publication / export review
Bare usable validation
Template creation
Agent setup
Controlled ingestion run
```

**Activity Type** records the type of work performed.

Examples include:

```text
Read
Inspect
Summarize
Extract
Classify
Draft
Validate
Compare
Propose Metadata
Propose Relationship
Propose Source Reference
Detect Issue
Recommend Move
Apply Edit
Prepare Handoff
```

**Operation Mode** records whether the activity was read-only, proposed, applied, destructive, export-related, publication-related, migration-related, or otherwise sensitive.

Recommended operation mode values include:

```text
Read-Only
Proposal Only
Draft Created
Applied Change
Movement Recommended
Movement Applied
Deletion Requested
Deletion Applied
Export Requested
Export Prepared
Publication Requested
Publication Prepared
Migration Requested
Migration Prepared
```

An Operation Mode value does not prove that the action was authorized.

Authorization must come from the applicable standard, workflow, permission profile, or human review.

**Target Entity Type** records what kind of material the agent interacted with.

Examples include:

```text
Source Material
Source Material Intake Record
Knowledge Record
Draft Knowledge Record
Agent Activity Record
Review Record
Validation Record
Standard
Specification
Template
Workflow
Runbook
Implementation Document
Repository File
Folder / Storage Area
```

**Target Entity Identifier** records the identifier of the entity touched by the agent where one exists.

This may be a Document ID, Object ID, record ID, source identifier, file identifier, path reference, issue identifier, pull request identifier, or other traceable reference.

**Target Entity Title or Label** records the human-readable title or label of the material touched by the agent.

This field supports recognition.

It does not replace stable identity.

**Target Entity Location or Reference** records the storage path, repository path, URL, vault reference, folder reference, source reference, or implementation reference needed to locate the material.

Storage location supports traceability.

Storage location must not be treated as Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval status, or governed meaning.

**Output Type** records the type of output produced by the agent.

Examples include:

```text
Summary
Draft text
Metadata proposal
Relationship proposal
Source Reference proposal
Validation finding
Issue report
Privacy warning
Authority warning
Repair recommendation
File movement recommendation
Handoff summary
Implementation recommendation
No output produced
```

**Output Location or Reference** records where the output can be found.

If the output is contained directly in the Agent Activity Record, the field may state:

```text
Contained in this record
```

**Change Applied** records whether the agent applied a change.

Recommended values include:

```text
No
Yes
Proposal Only
Pending Human Review
Unknown
```

A value of `Yes` should be accompanied by a Change Summary.

**Human Review Required** records whether a human must review the activity, output, proposal, or applied change before it may affect governed meaning, approval, authority, privacy, publication, export, migration, deletion, or downstream use.

Recommended values include:

```text
Yes
No
Conditional
Pending Determination
```

When uncertain, this field should default to:

```text
Yes
```

## 6. Recommended Agent Activity Field Instructions

The following fields are recommended because they improve traceability, reviewability, validation, privacy handling, authority handling, provenance, workflow continuity, and later maintenance.

They may be omitted when the activity is low-risk, read-only, fully documented elsewhere, or not applicable.

**Related Source Material** identifies Source Material connected to the agent activity.

This field should be used when the agent read, summarized, extracted from, transformed, cited, classified, routed, or proposed knowledge from Source Material.

This field should not duplicate full Source Material.

It should provide enough reference information for later review.

**Related Knowledge Record** identifies a Knowledge Record or Draft Knowledge Record connected to the activity.

This field should be used when the agent drafted, inspected, validated, revised, summarized, compared, or proposed changes to a Knowledge Record.

**Related Intake Record** identifies a Source Material Intake Record connected to the activity.

This field should be used when the agent assisted with intake, staging, source handling, extraction planning, candidate record identification, or intake validation.

**Related Review Record** identifies a Review Record connected to the activity.

This field should be used when the agent supported human review, prepared review notes, detected review issues, summarized review candidates, or responded to review feedback.

**Related Validation Record** identifies a Validation Record, checklist, validation result, or validation report connected to the activity.

This field should be used when the agent performed or supported validation.

Agent-generated validation must remain distinguishable from human validation, workflow validation, implementation validation, and approval.

**Change Summary** summarizes any edit, movement, creation, deletion, export preparation, publication preparation, migration preparation, or other applied change.

If no change was applied, the field should state:

```text
No change applied.
```

**Proposal Summary** summarizes recommendations made by the agent.

Examples include proposed metadata, proposed relationships, proposed Source References, proposed privacy flags, proposed authority limits, proposed lifecycle handling, proposed validation repairs, proposed storage moves, or proposed review actions.

A proposal is not approval.

A proposal is not validation.

A proposal is not a workflow decision.

**Uncertainty or Limitation** records uncertainty, ambiguity, incomplete access, missing evidence, model limitation, source limitation, conflict, assumption, or unresolved issue affecting the activity.

This field should be used whenever a future reviewer should not treat the agent output as complete or final.

**Privacy Concern** records privacy-sensitive material, possible exposure, access limitation, restricted content, publication risk, export risk, synchronization risk, indexing risk, agent-access concern, or downstream-use concern detected during the activity.

This field records a concern.

It does not complete privacy review.

**Authority Concern** records concerns about whether the activity or output may be relied on for interpretation, governance, decision support, publication, export, migration, automation, or downstream use.

This field records a concern.

It does not assign Authority Level.

**Validation Concern** records structural, metadata, identity, relationship, source-reference, provenance, lifecycle, authority, privacy, storage, workflow, agent, implementation, import, export, migration, compatibility, or downstream-use issues detected during activity.

This field records a concern.

It does not replace a Validation Record or validation checklist.

**Source / Provenance Concern** records missing, incomplete, ambiguous, restricted, unavailable, unreliable, superseded, conflicting, transformed, agent-generated, workflow-generated, imported, migrated, or otherwise uncertain source or provenance context.

This field should be used when the activity depends on source support or transformation history.

**Relationship Concern** records concerns about proposed, inferred, missing, duplicated, conflicting, reversed, unsupported, unreviewed, deprecated, superseded, or implementation-specific relationships.

This field should be used when relationship meaning may affect interpretation, navigation, validation, authority, source support, privacy, or downstream use.

**Lifecycle Concern** records concerns about draft status, pending review, pending validation, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, or other lifecycle-related handling.

This field records a concern.

It does not change Lifecycle State.

**Storage or Placement Concern** records concerns about where material is stored, staged, routed, archived, moved, exported, imported, migrated, indexed, cached, backed up, or exposed.

This field records a concern.

It does not authorize movement.

**Escalation Required** records whether the activity should be escalated to a human, reviewer, workflow, governance process, privacy review, authority review, validation review, source review, relationship review, identity review, or implementation review.

Recommended values include:

```text
Yes
No
Conditional
Pending Determination
```

When the activity involves deletion, publication, export, migration, privacy-sensitive material, identity change, authority change, approval, supersession, deprecation, or unresolved validation error, escalation should normally be marked:

```text
Yes
```

**Validation Required** records whether additional validation is needed before the output may be relied on.

Recommended values include:

```text
Yes
No
Conditional
Pending Determination
```

**Follow-Up Required** records the next action needed after the agent activity.

Examples include:

```text
Human review
Validation check
Privacy review
Authority review
Source verification
Relationship review
Identity review
Repair required
Workflow routing
No follow-up required
```

**Reviewed By** records the human or governed review process that reviewed the Agent Activity Record.

This field may remain blank until review occurs.

**Review Date** records when the Agent Activity Record was reviewed.

**Review Outcome** records the result of review.

Recommended values include:

```text
Accepted
Accepted with Corrections
Rejected
Needs Repair
Escalated
Deferred
Not Reviewed
```

Review Outcome belongs to the Agent Activity Record.

It does not automatically approve the target entity, Knowledge Record, Source Material, metadata, relationship, Source Reference, provenance, lifecycle transition, authority assignment, privacy classification, validation result, publication, export, migration, deletion, or downstream use.

**Notes** records additional context that does not fit cleanly into the other fields.

Notes should be concise.

Notes should not contain full source material, full review decisions, full validation reports, or full workflow logs when those belong in separate governed records.

## 7. Activity Description and Source Interaction

Use this section to describe what the agent did and what material the agent interacted with.

The activity description should be specific enough that a future human, reviewer, validator, workflow, implementation, or agent can understand the activity without relying on hidden memory, chat context, tool state, or implementation-specific assumptions.

The activity description should identify:

- what the agent was asked to do;
- what material the agent inspected;
- what operation the agent performed;
- what source, record, file, workflow, standard, template, specification, or governed entity was involved;
- whether the activity was read-only, proposal-only, draft-producing, edit-producing, movement-related, validation-related, review-supporting, or escalation-related;
- what output or recommendation resulted;
- what uncertainty or limitation remained.

Use the following structure:

```text
### Activity Description

Agent Request or Task:

Activity Summary:

Material Inspected:

Material Not Inspected:

Operation Performed:

Reason for Activity:

Workflow or Milestone Context:

Relevant Human Instruction:

Relevant Agent Boundary:

Activity Limitations:

Unresolved Questions:
```

**Agent Request or Task** records the instruction, trigger, workflow step, or review need that caused the agent activity.

This field should preserve the user request or workflow instruction closely enough that the activity can be interpreted later.

The field should not include unrelated conversation history unless that history materially affects the activity.

**Activity Summary** describes what the agent actually did.

The summary should be concise but complete.

The summary should distinguish between:

- inspection;
- extraction;
- classification;
- validation support;
- drafting;
- editing;
- movement;
- recommendation;
- escalation;
- hand-off preparation.

**Material Inspected** identifies the files, Source Material, Knowledge Records, templates, standards, specifications, workflow records, validation records, review records, repository paths, folders, or other governed entities the agent reviewed.

This field should include identifiers, titles, filenames, paths, or references where available.

Material Inspected should not imply that the agent inspected every related file unless the agent actually did so.

**Material Not Inspected** identifies relevant material that was unavailable, inaccessible, intentionally skipped, outside scope, not provided, not searched, not opened, or not reviewed.

This field helps prevent false completeness.

If no known material was excluded, this field may state:

```text
No known relevant material was excluded.
```

If the agent could not verify repository contents, external files, source material, or implementation state, this field should state that limitation clearly.

**Operation Performed** describes the actual operation carried out by the agent.

Examples include:

```text
Read-only inspection
Syntax review
Spelling and grammar review
Standards consistency review
Metadata proposal
Relationship proposal
Source/provenance review
Privacy-risk review
Validation support
Draft section creation
Template continuation
Workflow support
Handoff preparation
```

**Reason for Activity** records why the activity mattered.

Examples include:

```text
Continue template creation
Reduce governance drift
Prepare reviewable agent output
Support source intake
Support Knowledge Record drafting
Support validation readiness
Support bare usable deployment
Support agent traceability
```

**Workflow or Milestone Context** records where the activity fits in the larger project flow.

Examples include:

```text
Template Set — Bare Usable Deployment
Knowledge ingestion preparation
Review and approval preparation
Agent framework preparation
Controlled ingestion setup
Validation checklist preparation
Repository implementation preparation
```

**Relevant Human Instruction** records the human instruction that limited or directed the activity.

This field may include a short paraphrase or direct reference to the instruction.

If the activity occurred under a standing instruction, the field should identify that instruction.

**Relevant Agent Boundary** records the agent boundary that applied to the work.

Examples include:

```text
Read-only inspection only
Proposal only
Draft text permitted
No approval authority
No deletion permitted
No publication permitted
No export permitted
Human review required
Escalation required for destructive action
```

This field records the boundary.

It does not create the boundary.

**Activity Limitations** records limits affecting the reliability, completeness, or reviewability of the activity.

Examples include:

```text
GitHub code search returned no file-level matches.
Only uploaded file text was fully inspected.
Only provided standards were available for comparison.
External implementation state was not inspected.
Repository path could not be verified.
Source Material was not provided.
No human review has occurred yet.
```

**Unresolved Questions** records questions that remain after the activity.

Unresolved questions should be stated plainly.

If there are no unresolved questions, this field may state:

```text
No unresolved questions identified.
```

### Source Interaction Notes

Use this subsection when the agent activity involved Source Material, Source References, extraction, transformation, provenance, or source-dependent interpretation.

```text
Source Material Used:

Source Reference Used:

Source Excerpt or Segment Reviewed:

Extraction Performed:

Transformation Performed:

Source Availability Concern:

Source Reliability Concern:

Source Privacy Concern:

Source / Provenance Notes:
```

**Source Material Used** identifies any Source Material the agent interacted with.

This field should distinguish original Source Material from intake records, Knowledge Records, summaries, drafts, and agent outputs.

**Source Reference Used** identifies any Source Reference used during the activity.

A Source Reference used by the agent does not prove the source supports the final output unless source support is later reviewed or validated where required.

**Source Excerpt or Segment Reviewed** identifies the part of the source the agent reviewed.

This field should be used when the agent inspected only part of a longer source.

If the full source was reviewed, this field may state:

```text
Full source reviewed.
```

If the full source was not reviewed, the field should not imply full-source coverage.

**Extraction Performed** records whether the agent selected, copied, summarized, transcribed, parsed, segmented, or otherwise extracted information from Source Material.

Recommended values include:

```text
No extraction performed.
Summary extraction performed.
Metadata extraction performed.
Relationship extraction performed.
Source-reference extraction performed.
Partial extraction performed.
Full extraction performed.
Pending review.
```

**Transformation Performed** records whether the agent changed source content into another form.

Examples include summarization, classification, translation, restructuring, template conversion, Knowledge Record drafting, metadata proposal, relationship proposal, or validation report creation.

A transformation must not be confused with original Source Material.

**Source Availability Concern** records whether the source was missing, inaccessible, restricted, partial, external, moved, corrupted, unavailable, not provided, or otherwise difficult to verify.

**Source Reliability Concern** records concerns about uncertainty, source quality, conflict, incompleteness, age, bias, authority, unsupported claims, unclear authorship, or lack of review.

**Source Privacy Concern** records privacy-sensitive material, restricted source handling, possible exposure, agent-access concern, indexing concern, publication risk, export risk, or downstream-use concern.

**Source / Provenance Notes** records source and provenance context that future reviewers may need.

This field should not replace a Source Material Intake Record, Source Reference record, provenance record, or Review Record when those are required elsewhere.

## 8. Agent Output and Proposal Tracking

Use this section to record what the agent produced, proposed, changed, or recommended.

Agent outputs must remain distinguishable from approved knowledge, reviewed decisions, final validation, privacy determinations, authority assignments, lifecycle transitions, workflow decisions, and implementation requirements.

Use the following structure:

```text
### Agent Output Summary

Output Produced:

Output Format:

Output Location:

Output Status:

Direct Changes Applied:

Drafts Created:

Metadata Proposed:

Relationships Proposed:

Source References Proposed:

Provenance Notes Proposed:

Validation Findings:

Privacy Findings:

Authority Findings:

Lifecycle Findings:

Storage / Placement Findings:

Recommended Follow-Up:
```

**Output Produced** describes the result of the activity.

Examples include:

```text
No output produced
Summary
Draft section
Draft Knowledge Record
Metadata proposal
Relationship proposal
Source Reference proposal
Validation finding
Issue report
Review support notes
Repair recommendation
Movement recommendation
Handoff summary
```

**Output Format** records the form of the output.

Examples include:

```text
Markdown text
Metadata block
Checklist
Table
Narrative report
Inline comments
Patch proposal
Repository file
Chat response
Workflow note
Validation note
```

**Output Location** records where the output exists.

Examples include:

```text
Contained in this Agent Activity Record
Contained in draft file
Contained in Knowledge Record
Contained in Review Record
Contained in validation report
Contained in repository path
Contained in chat response
External reference
Not saved
```

If the output is not saved in a governed location, this should be stated clearly.

**Output Status** records whether the output is draft, proposed, applied, pending review, rejected, accepted, needs repair, escalated, or archived.

Recommended values include:

```text
Draft
Proposal
Applied
Pending Human Review
Pending Validation
Needs Repair
Rejected
Accepted for Review
Escalated
Archived
```

Output Status applies to the agent output.

It does not automatically define the Lifecycle State, Authority Level, Privacy Classification, Validation State, approval status, or downstream-use permission of the target entity.

**Direct Changes Applied** records whether the agent changed any file, record, metadata, relationship, source reference, storage location, implementation file, workflow output, validation record, or governed document.

Recommended values include:

```text
No direct changes applied.
Direct changes applied.
Proposal only.
Draft created only.
Unable to determine.
```

If direct changes were applied, the record should identify what changed, where it changed, and whether human review is required.

**Drafts Created** records any draft Knowledge Record, draft governed document, draft template section, draft review note, draft validation note, draft metadata block, draft relationship proposal, or draft workflow output created by the agent.

Drafts are not approved merely because they were created.

**Metadata Proposed** records metadata values proposed by the agent.

Metadata proposals should identify the field, proposed value, rationale, source support where applicable, and review status.

Use this structure when needed:

```text
Proposed Metadata Field:
Proposed Value:
Reason:
Source or Evidence:
Confidence or Limitation:
Review Required:
```

Agent-proposed metadata must not be treated as accepted metadata until reviewed or approved under the applicable workflow or standard.

**Relationships Proposed** records relationships proposed by the agent.

Relationship proposals should identify the origin participant, target participant, relationship type, direction where applicable, source support, confidence or limitation, and review requirement.

Use this structure when needed:

```text
Origin Participant:
Target Participant:
Proposed Relationship Type:
Direction:
Reason:
Source or Evidence:
Confidence or Limitation:
Review Required:
```

Agent-proposed relationships must not be treated as approved relationships until reviewed or approved under the applicable workflow or standard.

**Source References Proposed** records Source References proposed by the agent.

Source Reference proposals should identify the source, target governed entity, reason for the reference, evidence or excerpt where applicable, source availability, source privacy, and review requirement.

Use this structure when needed:

```text
Target Governed Entity:
Proposed Source Material:
Proposed Source Reference:
Reason:
Evidence or Segment:
Source Availability:
Source Privacy Concern:
Review Required:
```

Agent-proposed Source References must not be treated as final source support until reviewed or validated where required.

**Provenance Notes Proposed** records provenance information proposed by the agent.

Provenance notes may include creation context, transformation context, extraction context, agent involvement, workflow involvement, import context, migration context, review context, or validation context.

Agent-proposed provenance must remain distinguishable from human-confirmed provenance.

**Validation Findings** records validation errors, warnings, missing fields, structural concerns, identity concerns, metadata concerns, relationship concerns, source-reference concerns, provenance concerns, lifecycle concerns, authority concerns, privacy concerns, storage concerns, workflow concerns, implementation concerns, compatibility concerns, or downstream-use concerns detected by the agent.

Validation Findings are not approval.

Validation Findings are not final validation unless a governed workflow, validator, or specification grants that role.

**Privacy Findings** records privacy risks or handling concerns detected by the agent.

Privacy Findings are not final privacy classification or clearance.

**Authority Findings** records concerns about whether the material may be relied on for interpretation, governance, decision support, publication, export, migration, automation, or downstream use.

Authority Findings are not Authority Level assignments.

**Lifecycle Findings** records lifecycle-related issues, such as draft status, pending review, pending validation, approval ambiguity, rejection, repair need, deprecation, supersession, archival, restriction, quarantine, or lifecycle transition concerns.

Lifecycle Findings are not lifecycle transitions by themselves.

**Storage / Placement Findings** records storage-location concerns, movement recommendations, draft placement concerns, review-area concerns, archive concerns, import/export area concerns, implementation-support area concerns, generated-file concerns, or cache/index concerns.

Storage / Placement Findings do not authorize movement by themselves.

**Recommended Follow-Up** records what should happen next.

Examples include:

```text
Human review required.
Validation required.
Privacy review required.
Authority review required.
Source verification required.
Relationship review required.
Identity review required.
Repair required.
Escalation required.
No follow-up required.
```

When the agent is uncertain, when the activity affects governed meaning, or when the output could affect publication, export, migration, deletion, identity, privacy, authority, lifecycle, validation, or downstream use, the recommended follow-up should default to human review.

### Proposal Tracking Table

Use this table when the activity produced multiple proposals.

| Proposal ID | Proposal Type | Target Entity | Summary | Source / Evidence | Risk or Concern | Review Required | Status |
|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |

Proposal Type may include:

```text
Metadata
Relationship
Source Reference
Provenance
Privacy Flag
Authority Limit
Lifecycle Handling
Validation Repair
Storage Move
Draft Creation
Review Action
Workflow Routing
```

Proposal Status may include:

```text
Proposed
Pending Review
Accepted
Accepted with Changes
Rejected
Needs Repair
Escalated
Deferred
```

Accepted proposal status in this table records the status of the proposal inside the Agent Activity Record.

It does not automatically approve the target governed entity unless a separate governed Review Record, workflow output, approval decision, or validation record establishes that result.

## 9. Permission, Privacy, and Boundary Notes

Use this section to record the boundaries that applied to the agent activity and any privacy, authority, validation, escalation, destructive-action, publication, export, migration, or downstream-use concerns.

This section does not grant permission.

This section records permission context, limits, concerns, and escalation needs.

Use the following structure:

```text
### Permission and Boundary Review

Permission Source:

Allowed Actions:

Disallowed Actions:

Boundary Applied:

Boundary Concern:

Human Review Requirement:

Escalation Requirement:

Destructive Action Involved:

Publication / Export / Migration Involved:

Downstream Use Concern:

Boundary Notes:
```

**Permission Source** identifies the standard, specification, workflow, runbook, permission profile, human instruction, or implementation rule that authorized or limited the activity.

Examples include:

```text
AG-0001 — Agent Operating Boundaries Standard
WF-0001 — Knowledge Ingestion Workflow Standard
WF-0002 — Review and Approval Workflow Standard
Human instruction
Future agent permission profile
Future controlled ingestion runbook
```

Permission Source records the source of permission or limitation.

It does not create permission by itself.

**Allowed Actions** records what the agent was allowed to do during the activity.

Examples include:

```text
Read files
Inspect text
Summarize
Extract
Classify
Draft
Suggest metadata
Suggest relationships
Suggest Source References
Suggest validation issues
Recommend follow-up
Prepare handoff
```

**Disallowed Actions** records what the agent was not allowed to do.

Examples include:

```text
Approve governed knowledge
Assign final Authority Level
Complete privacy review
Publish material
Export material
Delete material
Move files without authorization
Override Object Identity
Apply lifecycle transition without review
Treat validation as approval
Treat proposal as decision
```

**Boundary Applied** records the practical limit that governed the activity.

Examples include:

```text
Read-only
Proposal only
Draft creation allowed
No direct file changes
Human review required
Validation required
Escalation required
Restricted source handling
No publication
No export
No deletion
No migration
```

**Boundary Concern** records any possible boundary violation, unclear permission, missing instruction, conflicting standard, workflow ambiguity, privacy risk, authority risk, validation risk, source risk, relationship risk, identity risk, lifecycle risk, storage risk, publication risk, export risk, migration risk, or downstream-use risk.

If no boundary concern was identified, this field may state:

```text
No boundary concern identified.
```

**Human Review Requirement** records whether human review is required before relying on the output.

Recommended values include:

```text
Required
Not Required
Conditional
Pending Determination
```

When the output affects governed meaning, metadata, relationships, Source References, provenance, lifecycle state, Authority Level, Privacy Classification, Validation State, publication, export, migration, deletion, or downstream use, the value should normally be:

```text
Required
```

**Escalation Requirement** records whether the activity requires escalation.

Recommended values include:

```text
Required
Not Required
Conditional
Pending Determination
```

Escalation should normally be required when the activity involves:

- destructive action;
- identity change;
- privacy-sensitive material;
- publication;
- export;
- migration;
- deletion;
- authority assignment;
- approval;
- lifecycle transition;
- unresolved validation error;
- source conflict;
- relationship conflict;
- repository-wide change;
- implementation-wide change;
- unclear permission.

**Destructive Action Involved** records whether the agent deleted, overwrote, replaced, moved, archived, renamed, discarded, removed, or otherwise made material less available.

Recommended values include:

```text
No
Yes
Requested Only
Recommended Only
Unable to Determine
```

If `Yes`, `Requested Only`, or `Recommended Only` is used, the activity should normally require human review and escalation.

**Publication / Export / Migration Involved** records whether the activity involved making material available beyond its prior boundary, preparing material for use elsewhere, or moving material between storage systems, implementations, schemas, vaults, repositories, file formats, or workflow environments.

Recommended values include:

```text
No
Publication Requested
Publication Prepared
Export Requested
Export Prepared
Migration Requested
Migration Prepared
Unable to Determine
```

Publication, export, and migration concerns should not be treated as approved without a governed workflow or review decision.

**Downstream Use Concern** records concerns about whether the output could later be used for interpretation, automation, publication, export, migration, relationship creation, validation, decision support, agent reasoning, workflow execution, implementation behavior, or other dependent activity.

If the output should not be used downstream without review, this field should state:

```text
Do not use downstream without human review.
```

### Privacy Notes

Use this subsection when the agent encountered or may have encountered privacy-sensitive material.

```text
Privacy Classification Observed:

Privacy Classification Proposed:

Privacy Risk:

Access Concern:

Exposure Concern:

Indexing Concern:

Synchronization Concern:

Publication Concern:

Export Concern:

Agent Access Concern:

Privacy Review Required:
```

**Privacy Classification Observed** records any existing Privacy Classification visible to the agent.

**Privacy Classification Proposed** records any Privacy Classification suggested by the agent.

An agent-proposed Privacy Classification is not final unless reviewed or approved under the applicable standard or workflow.

**Privacy Risk** records the privacy-sensitive issue detected.

**Access Concern** records whether the agent, workflow, implementation, reviewer, or downstream user may lack permission to access the material.

**Exposure Concern** records whether the activity may expose restricted, confidential, sensitive, personal, private, or otherwise controlled material.

**Indexing Concern** records whether search, embeddings, vectorization, summarization, caching, previews, graph views, backlinks, generated indexes, or implementation features may expose privacy-sensitive material.

**Synchronization Concern** records whether syncing, mirroring, copying, backup, cloud storage, repository hosting, or multi-device use may expose privacy-sensitive material.

**Publication Concern** records whether the material may be published beyond its permitted boundary.

**Export Concern** records whether the material may be exported beyond its permitted boundary.

**Agent Access Concern** records whether the agent should have been allowed to read, summarize, transform, extract from, route, or reason over the material.

**Privacy Review Required** records whether a human or governed privacy workflow must review the material before further use.

Recommended values include:

```text
Yes
No
Conditional
Pending Determination
```

When uncertain, the value should default to:

```text
Yes
```

### Boundary Success Criteria

This section is successful when a future reviewer can determine:

- what permission source governed the activity;
- what the agent was allowed to do;
- what the agent was not allowed to do;
- whether the agent stayed within boundary;
- whether the output requires human review;
- whether escalation is required;
- whether destructive action, publication, export, migration, privacy exposure, authority risk, validation risk, or downstream-use risk exists;
- whether any agent proposal, draft, finding, warning, or recommendation remains unapproved.

## 10. Review, Validation, and Escalation Notes

Use this section to record review needs, validation needs, escalation conditions, unresolved issues, and follow-up actions created or identified during agent activity.

This section does not approve agent output.

This section does not complete validation.

This section does not replace a Review Record.

This section does not replace a Validation Record.

This section does not replace a workflow decision.

This section records what must be reviewed, validated, repaired, escalated, or followed up before the agent activity or output can be relied on for governed use.

Use the following structure:

```text
### Review Notes

Human Review Required:

Review Reason:

Suggested Reviewer or Review Role:

Review Scope:

Review Priority:

Review Deadline or Timing:

Review Notes:
```

**Human Review Required** records whether a human must review the agent activity, output, proposal, applied change, warning, or recommendation.

Recommended values include:

```text
Yes
No
Conditional
Pending Determination
```

When the activity affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, publication, export, migration, deletion, or downstream use, the value should normally be:

```text
Yes
```

**Review Reason** records why review is required.

Examples include:

```text
Agent output affects governed meaning.
Agent proposed metadata.
Agent proposed relationships.
Agent proposed Source References.
Agent detected a privacy concern.
Agent detected a validation concern.
Agent detected an authority concern.
Agent created draft governed text.
Agent recommended file movement.
Agent identified source or provenance uncertainty.
Agent could not inspect all relevant material.
Human decision required.
```

**Suggested Reviewer or Review Role** identifies who or what role should review the activity.

Examples include:

```text
Human owner
Reviewer
Privacy reviewer
Authority reviewer
Validation reviewer
Source / Provenance reviewer
Relationship reviewer
Workflow reviewer
Implementation reviewer
Governance reviewer
```

**Review Scope** records what the reviewer should inspect.

Examples include:

```text
Agent output only
Target entity only
Source support
Metadata proposal
Relationship proposal
Privacy concern
Authority concern
Validation finding
Storage placement
Applied change
Full activity record
```

**Review Priority** records how urgent the review is.

Recommended values include:

```text
Low
Normal
High
Critical
Pending Determination
```

High or Critical priority should be used when unresolved issues may affect privacy, authority, validation, deletion, publication, export, migration, Object Identity, or downstream use.

**Review Deadline or Timing** records when review should occur if timing matters.

This field may be blank when no timing requirement exists.

**Review Notes** records review context that does not fit into the other fields.

Review Notes should not duplicate the full Review Record when a separate Review Record is required.

### Validation Notes

Use this subsection to record validation needs or validation findings connected to the agent activity.

```text
Validation Required:

Validation Scope:

Validation Findings Summary:

Validation Errors:

Validation Warnings:

Validation Evidence:

Validation Limitations:

Validation Follow-Up:
```

**Validation Required** records whether validation is needed before the output, proposal, change, or target entity may be relied on.

Recommended values include:

```text
Yes
No
Conditional
Pending Determination
```

When uncertain, this field should normally default to:

```text
Yes
```

**Validation Scope** records what should be validated.

Examples include:

```text
Structure
Metadata
Object Identity
Relationships
Source References
Provenance
Lifecycle State
Authority Level
Privacy Classification
Storage placement
Workflow conformance
Agent boundary conformance
Template conformance
Implementation compatibility
Publication readiness
Export readiness
Migration readiness
Downstream-use readiness
```

**Validation Findings Summary** summarizes validation issues detected during the agent activity.

This summary should distinguish between findings produced by an agent and findings confirmed by a human, workflow, validator, or implementation.

**Validation Errors** records issues that appear to violate mandatory requirements.

Validation Errors should identify the affected entity, rule, field, section, or output where practical.

**Validation Warnings** records issues that may require review but do not necessarily make the output invalid.

Validation Warnings may include missing optional context, uncertainty, incomplete source access, possible duplication, unclear relationship direction, unresolved privacy concern, or implementation-specific ambiguity.

**Validation Evidence** records the standard, specification, template, source, workflow, review note, or observed file condition that supports the validation finding.

**Validation Limitations** records why validation may be incomplete.

Examples include:

```text
Source material not provided.
Repository search returned no file-level matches.
Only uploaded file was inspected.
Validation tool was not run.
Human review has not occurred.
Related files were not accessible.
External implementation state was not inspected.
```

**Validation Follow-Up** records the next validation action needed.

Examples include:

```text
Run checklist.
Inspect related source material.
Verify metadata fields.
Verify relationship proposals.
Verify Source References.
Verify privacy classification.
Verify authority scope.
Verify lifecycle state.
Verify storage placement.
Escalate to human review.
No additional validation required.
```

### Escalation Notes

Use this subsection when the activity identifies a condition that should be routed to a human, reviewer, workflow, governance process, privacy review, authority review, validation review, source review, relationship review, identity review, or implementation review.

```text
Escalation Required:

Escalation Reason:

Escalation Target:

Escalation Priority:

Escalation Status:

Escalation Notes:
```

**Escalation Required** records whether escalation is needed.

Recommended values include:

```text
Yes
No
Conditional
Pending Determination
```

Escalation should normally be required when the activity involves or identifies:

- destructive action;
- deletion;
- publication;
- export;
- migration;
- Object Identity change;
- merge or split concern;
- duplicate identity concern;
- privacy-sensitive material;
- unresolved privacy concern;
- authority assignment concern;
- lifecycle transition concern;
- unresolved validation error;
- source conflict;
- missing provenance;
- relationship conflict;
- implementation-wide change;
- repository-wide change;
- unclear permission;
- possible agent boundary violation.

**Escalation Reason** records why escalation is required.

**Escalation Target** records who or what process should receive the escalation.

Examples include:

```text
Human owner
Privacy review
Authority review
Validation review
Source / Provenance review
Relationship review
Identity review
Workflow review
Governance review
Implementation review
```

**Escalation Priority** records urgency.

Recommended values include:

```text
Low
Normal
High
Critical
Pending Determination
```

**Escalation Status** records whether escalation has occurred.

Recommended values include:

```text
Not Escalated
Escalated
Pending Escalation
Resolved
Deferred
Rejected
```

**Escalation Notes** records additional context needed by the escalation target.

Escalation Notes should be clear enough that a reviewer can understand what happened, why it matters, what material is affected, and what decision is needed.

### Follow-Up Action Table

Use this table when more than one follow-up action is required.

| Follow-Up ID | Action Needed | Reason | Target Entity | Assigned To | Priority | Status |
|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

Follow-Up Status may include:

```text
Not Started
Pending
In Progress
Complete
Blocked
Deferred
Escalated
Not Required
```

Follow-up completion does not automatically approve the agent output, target entity, Knowledge Record, Source Reference, relationship, metadata, privacy classification, authority level, validation result, publication, export, migration, deletion, or downstream use unless a governed workflow or Review Record establishes that outcome.

## 11. Agent Activity Completion Checklist

Use this checklist before treating an Agent Activity Record as complete.

The checklist confirms that the record is structurally usable, traceable, reviewable, and clear enough for future humans, agents, workflows, validators, storage systems, and implementations.

This checklist does not approve the agent output.

This checklist does not validate the target entity.

This checklist does not replace a Review Record, Validation Record, workflow log, privacy review, authority review, source review, or governance decision.

```text
### Completion Checklist

[ ] Agent Activity Record ID is present.
[ ] Record Title is present.
[ ] Record Type is identified as Agent Activity Record.
[ ] Template Used identifies TEMPLATE-0003.
[ ] Created date is recorded.
[ ] Activity Date is recorded or marked unknown.
[ ] Activity Status is recorded.
[ ] Agent Name or Identifier is recorded or marked unknown.
[ ] Agent Role is recorded.
[ ] Agent Type is recorded where applicable.
[ ] Permission / Boundary Reference is recorded or marked pending.
[ ] Human Request or Trigger is recorded.
[ ] Workflow Context is recorded where applicable.
[ ] Activity Type is recorded.
[ ] Operation Mode is recorded.
[ ] Target Entity Type is recorded.
[ ] Target Entity Identifier is recorded where available.
[ ] Target Entity Title or Label is recorded where available.
[ ] Target Entity Location or Reference is recorded where available.
[ ] Output Type is recorded.
[ ] Output Location or Reference is recorded.
[ ] Change Applied is recorded.
[ ] Change Summary is recorded if a change was applied.
[ ] Proposal Summary is recorded if proposals were made.
[ ] Uncertainty or Limitation is recorded where applicable.
[ ] Privacy Concern is recorded or marked not identified.
[ ] Authority Concern is recorded or marked not identified.
[ ] Validation Concern is recorded or marked not identified.
[ ] Source / Provenance Concern is recorded or marked not identified.
[ ] Relationship Concern is recorded or marked not identified.
[ ] Lifecycle Concern is recorded or marked not identified.
[ ] Storage or Placement Concern is recorded or marked not identified.
[ ] Escalation Required is recorded.
[ ] Human Review Required is recorded.
[ ] Validation Required is recorded.
[ ] Follow-Up Required is recorded.
[ ] Material Inspected is identified.
[ ] Material Not Inspected is identified where relevant.
[ ] Agent output is distinguished from approved knowledge.
[ ] Agent proposals are distinguished from approved changes.
[ ] Agent validation findings are distinguished from final validation.
[ ] Agent privacy findings are distinguished from privacy review.
[ ] Agent authority findings are distinguished from Authority Level assignment.
[ ] Agent lifecycle findings are distinguished from lifecycle transitions.
[ ] Agent storage findings are distinguished from movement authorization.
[ ] Destructive actions are identified.
[ ] Publication, export, or migration concerns are identified.
[ ] Downstream-use concerns are identified.
[ ] Review needs are recorded.
[ ] Validation needs are recorded.
[ ] Escalation needs are recorded.
[ ] Follow-up actions are recorded.
[ ] Notes are concise and do not duplicate full source material, full review records, full validation reports, or full workflow logs.
```

A checklist item may be left incomplete when it is not applicable, unknown, unavailable, restricted, or pending review.

Incomplete checklist items should not be hidden.

If a required item is incomplete, the Agent Activity Record should identify whether the issue requires repair, review, validation, escalation, or no action.

Recommended completion states include:

```text
Complete
Complete with Limitations
Pending Human Review
Pending Validation
Needs Repair
Escalated
Deferred
Archived
```

**Complete** means the Agent Activity Record contains enough information to understand and review the agent activity.

**Complete with Limitations** means the record is usable but has clearly stated limits, missing context, unavailable material, or unresolved questions.

**Pending Human Review** means a human must review the activity or output before it may be relied on.

**Pending Validation** means validation must occur before the output, proposal, change, or target entity may be relied on.

**Needs Repair** means the Agent Activity Record is incomplete, unclear, structurally deficient, missing required context, or inconsistent with the applicable standard, template, workflow, or instruction.

**Escalated** means the activity has been routed to a human, workflow, governance process, privacy review, authority review, validation review, source review, relationship review, identity review, or implementation review.

**Deferred** means the activity record is preserved but not currently being advanced.

**Archived** means the activity record is preserved for traceability, audit, history, or reference but is not active by default.

An Agent Activity Record should not be marked Complete if:

- the agent identity is unknown and material to review;
- the target entity is unclear;
- the operation performed is unclear;
- applied changes are not described;
- proposals are not distinguishable from approved changes;
- source interaction is unclear where source support matters;
- privacy concerns are unresolved;
- authority concerns are unresolved;
- validation concerns are unresolved;
- destructive action is unclear;
- publication, export, or migration involvement is unclear;
- downstream-use risk is unclear;
- human review is required but not recorded;
- escalation is required but not recorded.

Completion of this checklist means the Agent Activity Record is structurally ready for use.

It does not mean the agent output is correct, approved, validated, privacy-cleared, authoritative, publishable, exportable, migratable, or safe for downstream use.

## 12. Template Success Criteria

TEMPLATE-0003 is successful when it provides a reusable, implementation-independent structure for recording agent and subagent activity without allowing agent activity to become unreviewable authority.

A completed Agent Activity Record should allow a future human, agent, workflow, validator, storage system, implementation, or governance process to determine:

- which agent or subagent acted;
- what role the agent operated under;
- what instruction, workflow step, or trigger caused the activity;
- what material the agent inspected;
- what material the agent did not inspect;
- what operation the agent performed;
- what output the agent produced;
- whether the agent applied a change;
- what proposals the agent made;
- what uncertainty or limitation remained;
- what source or provenance context mattered;
- what privacy concerns appeared;
- what authority concerns appeared;
- what validation concerns appeared;
- what relationship concerns appeared;
- what lifecycle concerns appeared;
- what storage or placement concerns appeared;
- what permission or boundary applied;
- whether the agent stayed within boundary;
- whether human review is required;
- whether validation is required;
- whether escalation is required;
- what follow-up action is needed.

The template succeeds when it preserves the following separations:

- agent activity is not agent authority;
- agent role is not permission by itself;
- agent output is not approved knowledge;
- agent proposal is not an approved change;
- agent confidence is not Authority Level;
- agent validation finding is not approval;
- agent privacy finding is not privacy clearance;
- agent source use is not final source support;
- agent provenance note is not confirmed provenance;
- agent relationship proposal is not an approved relationship;
- agent lifecycle finding is not a lifecycle transition;
- agent storage recommendation is not movement authorization;
- agent draft is not a reviewed Knowledge Record;
- agent completion is not workflow completion;
- agent activity record completion is not target-entity approval.

TEMPLATE-0003 should reduce drift by making agent work visible, bounded, reviewable, and traceable.

TEMPLATE-0003 should support the bare usable deployment goal by enabling agents and subagents to assist with:

- intake support;
- source inspection;
- extraction;
- summarization;
- classification;
- metadata proposal;
- relationship proposal;
- Source Reference proposal;
- provenance notes;
- privacy concern detection;
- authority concern detection;
- validation support;
- draft Knowledge Record creation;
- draft governed document creation;
- workflow support;
- review support;
- maintenance support;
- hand-off preparation.

TEMPLATE-0003 must remain software-neutral and AI-neutral.

The template must be usable in Markdown, plain files, repositories, vaults, databases, forms, future agent systems, and future implementations without requiring one specific tool.

The template may be adapted by future implementation profiles, but those adaptations must not redefine the meaning of Agent Activity Records unless a governed standard, specification, or approved implementation profile explicitly does so.

A compliant use of TEMPLATE-0003 should avoid:

- hiding agent activity in chat history only;
- relying on agent memory as provenance;
- treating repeated automation as governance;
- treating tool output as approval;
- treating folder placement as meaning;
- treating validation as review;
- treating review as publication approval unless the workflow says so;
- treating agent confidence as authority;
- treating source summaries as source truth;
- treating implementation logs as standard records unless mapped to this template or a future governed equivalent.

TEMPLATE-0003 is complete when:

- it can document read-only agent work;
- it can document proposal-only agent work;
- it can document draft-producing agent work;
- it can document applied agent changes;
- it can document agent validation support;
- it can document agent privacy concerns;
- it can document agent authority concerns;
- it can document agent source and provenance concerns;
- it can document relationship and lifecycle concerns;
- it can document storage and movement concerns;
- it can document review, validation, escalation, and follow-up needs;
- it keeps Agent Activity Records separate from Knowledge Records, Source Material Intake Records, Review Records, Validation Records, workflow runbooks, permission standards, and implementation-specific logs.

A TEMPLATE-0003 record is successful when a reviewer can answer:

```text
What did the agent do?

Why did the agent do it?

What did the agent inspect?

What did the agent not inspect?

What did the agent produce?

What did the agent propose?

What changed, if anything?

What remains uncertain?

What must be reviewed?

What must be validated?

What must be escalated?

What should not be trusted yet?
```

If those questions cannot be answered from the Agent Activity Record or linked governed records, the record should be treated as incomplete, pending review, pending validation, needing repair, or escalated.

TEMPLATE-0003 reaches its intended bare usable form when it can support supervised agent activity across The Brain without making any agent, model, workflow tool, repository, vault, plugin, implementation, or automation system the authority over knowledge meaning.