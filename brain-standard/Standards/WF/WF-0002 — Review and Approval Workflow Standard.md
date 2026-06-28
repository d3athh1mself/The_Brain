# WF-0002 — Review and Approval Workflow Standard

Document ID: WF-0002
Title: Review and Approval Workflow Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 4 — Workflow Engine
Milestone: 4.2 — Review and Approval Workflow Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; WF-0001 — Knowledge Ingestion Workflow Standard
Supersedes: None
Superseded By: None
Related: WF-0001 — Knowledge Ingestion Workflow Standard

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and review-and-approval workflow rules are interpreted within WF-0002.

Where conflicts arise between review behavior, approval behavior, rejection behavior, revision behavior, escalation behavior, lifecycle transitions, validation results, authority assignment, privacy review, Source References, provenance, relationships, workflow outputs, agent outputs, storage behavior, implementation behavior, publication readiness, export readiness, migration readiness, downstream-use readiness, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

WF-0002 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

WF-0002 depends on the Phase 1 Knowledge Standards because review and approval workflows must preserve knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation without redefining those concepts.

WF-0002 depends on the Phase 2 Storage Standards because review and approval workflows may route, stage, preserve, archive, or expose reviewed material without allowing storage placement to define meaning, lifecycle state, authority, privacy classification, validation state, approval, rejection, or downstream-use permission.

WF-0002 depends on AG-0001 because agents may assist review and approval workflows only within governed operating boundaries.

WF-0002 depends on WF-0001 because review and approval commonly follow ingestion and must preserve the distinction between Source Material, ingestion candidates, Draft Knowledge Records, workflow outputs, reviewed records, approved records, rejected records, repaired records, quarantined records, and archived records.

WF-0002 defines workflow behavior at the standard level.

WF-0002 does not define exact folder paths, exact filenames, exact metadata field names, exact Markdown front matter syntax, exact schemas, exact validation tooling, exact review forms, exact approval queues, exact agent prompts, exact model behavior, exact Obsidian behavior, exact Codex behavior, exact automation scripts, exact user-interface behavior, or exact implementation-specific routing.

Those concerns belong to later workflow specifications, storage specifications, agent specifications, implementation profiles, validation specifications, templates, operational guides, and reference implementations.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Workflow Engine refers to Layer 4 of The Brain Standard, responsible for defining repeatable workflows that coordinate knowledge capture, transformation, validation, review, maintenance, publication, synchronization, and automation.
- Workflow refers to a repeatable governed process that coordinates human actions, agent actions, storage actions, validation actions, review actions, approval actions, or implementation actions.
- Review refers to the governed evaluation of a Knowledge Object, Knowledge Record, Source Material, relationship, Source Reference, provenance record, metadata record, validation result, workflow output, agent output, import record, export record, migration record, governed document, decision, or other governed entity.
- Approval refers to formal acceptance of a governed entity for use within a defined scope.
- Rejection refers to a governed decision that a reviewed entity is not accepted for its intended use.
- Revision refers to a change made to a governed entity in response to review, validation, correction, clarification, source review, privacy review, authority review, relationship review, or workflow requirements.
- Repair refers to correction of structural, metadata, identity, relationship, provenance, source-reference, lifecycle, authority, privacy, validation, storage, agent, workflow, implementation, import, export, or migration issues identified during review.
- Escalation refers to routing a risk, conflict, ambiguity, privacy concern, authority concern, validation issue, source concern, relationship concern, destructive action, or unresolved review condition to a human, governance process, or higher-authority workflow.
- Human Review refers to review performed by a human to confirm, correct, reject, approve, limit, escalate, or route governed entities where human judgment is required.
- Agent Assistance refers to agent participation in review and approval through summarization, comparison, issue detection, validation support, metadata review, relationship review, source-reference review, provenance review, privacy-risk detection, authority-risk detection, draft revision, or review reporting within authorized boundaries.
- Review Candidate refers to any governed entity submitted, routed, staged, or identified for review.
- Approval Candidate refers to any reviewed entity being evaluated for approval within a defined scope.
- Review Output refers to any correction, comment, decision, validation result, issue report, approval decision, rejection decision, repair request, escalation, lifecycle transition, authority assignment, privacy determination, provenance entry, relationship decision, or workflow log entry created through review.
- Approval Scope refers to the defined context in which approval applies.
- Approval Decision refers to the recorded decision to approve, reject, defer, repair, quarantine, archive, escalate, supersede, deprecate, or otherwise route a reviewed entity.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Draft Knowledge Record refers to a Knowledge Record that has been created or proposed but has not yet completed required review, validation, approval, rejection, repair, or routing.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Validation refers to the process of checking whether a governed entity satisfies applicable standards, specifications, metadata expectations, provenance expectations, relationship expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Workflow State refers to the current processing position of a review candidate or approval candidate within the workflow.
- Workflow Log refers to a traceable record of material actions, decisions, outputs, actors, agents, validation results, review points, approvals, rejections, repairs, escalations, exceptions, or lifecycle transitions associated with a workflow.
- Downstream Use refers to later use of a governed entity for interpretation, automation, publication, export, migration, relationship creation, validation, decision support, agent reasoning, workflow execution, implementation behavior, or other dependent activity.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of WF-0002 is to define the standard-level workflow for reviewing, approving, rejecting, repairing, escalating, superseding, deprecating, archiving, and routing governed knowledge within The Brain Standard.

WF-0002 defines how Draft Knowledge Records, Knowledge Records, relationships, metadata, Source References, provenance records, validation results, workflow outputs, agent outputs, import outputs, migration outputs, and other governed entities move through review and approval without creating architectural drift.

Review and approval exist so that governed knowledge does not become accepted, authoritative, publishable, exportable, migratable, or ready for downstream use merely because it was created, ingested, validated, stored, indexed, summarized, processed by an agent, routed by a workflow, or made visible in an implementation.

WF-0002 exists to prevent review and approval confusion.

Review and approval confusion occurs when humans, agents, workflows, validators, storage systems, import processes, export processes, migration processes, publication processes, or implementations cannot reliably determine:

- whether a governed entity has been reviewed;
- whether a governed entity has been approved;
- what scope the approval applies to;
- whether review, approval, validation, authority, privacy clearance, publication readiness, export readiness, migration readiness, implementation visibility, workflow completion, and downstream-use readiness have been confused;
- whether a validation result supports approval or merely identifies conformance, warning, error, or repair need;
- whether agent confidence has been confused with human review, authority assignment, approval, or truth;
- whether a lifecycle transition was reviewed, approved, rejected, repaired, escalated, archived, superseded, deprecated, or quarantined;
- whether Source References, provenance, relationships, metadata, authority, privacy, and validation remain sufficient after review;
- whether approval was granted within a defined scope or incorrectly generalized beyond that scope.

WF-0002 defines review-and-approval workflow behavior for:

- review intake;
- review candidate classification;
- review scope definition;
- validation review;
- Source Reference review;
- provenance review;
- metadata review;
- relationship review;
- lifecycle review;
- authority review;
- privacy review;
- human review;
- agent-assisted review;
- approval decisions;
- rejection decisions;
- revision and repair;
- escalation;
- quarantine;
- archival;
- supersession;
- deprecation;
- workflow logging;
- auditability;
- conformance;
- success criteria.

WF-0002 does not define exact metadata fields, exact review forms, exact approval field values, exact lifecycle values, exact validation rule syntax, exact folder paths, exact Obsidian configuration, exact Codex setup, exact automation scripts, exact review queues, exact user-interface behavior, exact agent prompts, or exact implementation-specific procedures.

Those concerns belong to future workflow specifications, validation specifications, lifecycle specifications, authority specifications, privacy specifications, implementation documents, templates, operational guides, and reference implementations.

WF-0002 defines review and approval behavior at the standard level.

A future specification MAY define exact approval fields, review states, review queues, approval checklists, reviewer roles, escalation paths, repair states, rejection reasons, approval scopes, publication gates, export gates, migration gates, downstream-use gates, or serialization syntax.

Such specifications are valid only when they preserve the review-and-approval behavior defined by WF-0002.

The primary purpose of WF-0002 is to ensure that review and approval remain explicit, scoped, traceable, reviewable, privacy-respecting, validation-aware, authority-aware, lifecycle-aware, provenance-preserving, implementation-independent, and safe for downstream use.

WF-0002 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine:

- what entity was reviewed;
- what scope was reviewed;
- what decision was made;
- who or what participated in the review;
- what validation, Source References, provenance, relationships, metadata, lifecycle state, authority level, and privacy classification were considered;
- whether the entity was approved, rejected, deferred, repaired, escalated, quarantined, archived, superseded, or deprecated;
- whether approval applies only to a narrow scope or supports broader downstream use;
- whether privacy boundaries were preserved;
- whether validation results were used without being confused with approval;
- whether agent outputs were used without becoming unreviewable authority;
- whether the review decision remains meaningful across storage changes, workflow changes, agent changes, implementation changes, import, export, migration, backup, synchronization, indexing, or publication.

## 2. Relationship to Prior Standards

WF-0002 is subordinate to and derived from the constitutional foundation of The Brain Standard.

WF-0002 depends on:

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
- WF-0001 — Knowledge Ingestion Workflow Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

WF-0002 applies that purpose by defining review-and-approval workflow behavior that remains portable, traceable, reviewable, privacy-respecting, validation-aware, and independent of any single storage system, workflow engine, agent framework, software tool, user interface, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

WF-0002 applies those principles by requiring review and approval workflows to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- Source Material and Knowledge Record distinction;
- Source References;
- provenance;
- relationship meaning;
- lifecycle state;
- authority boundaries;
- privacy boundaries;
- validation boundaries;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability;
- governed evolution.

TB-0002 establishes the layered architecture of The Brain Standard.

WF-0002 belongs to Layer 4 — Workflow Engine.

Because WF-0002 is a workflow standard, it coordinates governed review, approval, rejection, repair, escalation, archival, supersession, deprecation, and routing. It does not define knowledge meaning, storage meaning, agent authority, implementation behavior, or exact technical schemas.

Layer 1 Knowledge Standards define what must be preserved during review and approval.

Layer 2 Storage Standards define how storage may support review and approval without allowing storage placement to define governed meaning.

Layer 3 Agent Standards define how agents may assist review and approval without becoming unreviewable authorities.

Layer 5 Implementation documents define how specific tools may realize review and approval without becoming the standard itself.

TB-0003 establishes the governance model for The Brain Standard.

WF-0002 follows the document authority hierarchy defined by TB-0003. As a standard-level document, WF-0002 has high authority within its scope but remains subordinate to constitutional documents.

WF-0002 does not replace TB-0003 document governance.

TB-0003 governs review and approval of standards, specifications, ADRs, RFCs, implementation documents, operational documents, and other governed documents.

WF-0002 defines review-and-approval workflow behavior for knowledge entities and related governed entities within The Brain Standard while remaining compatible with TB-0003.

KS-0001 defines the foundational Knowledge Object Model.

WF-0002 depends on KS-0001 because review and approval must preserve the distinction between Knowledge Objects, Knowledge Records, Source Material, metadata, relationships, provenance, lifecycle state, authority level, privacy classification, validation, and implementation behavior.

KS-0002 defines Object Identity.

WF-0002 depends on KS-0002 because review and approval decisions must not silently create, remove, merge, split, replace, redirect, or reinterpret Object Identity.

KS-0003 defines metadata behavior.

WF-0002 depends on KS-0003 because review and approval may inspect, correct, require, reject, or approve metadata while preserving metadata role boundaries.

KS-0004 defines relationship behavior.

WF-0002 depends on KS-0004 because review and approval may evaluate proposed, inferred, reviewed, approved, rejected, deprecated, superseded, archived, or repaired relationships.

KS-0005 defines Source Reference and provenance behavior.

WF-0002 depends on KS-0005 because review and approval must preserve source traceability, evidence context, attribution, extraction history, transformation history, review history, and workflow provenance.

KS-0006 defines Lifecycle State behavior.

WF-0002 depends on KS-0006 because review and approval often produce lifecycle transitions, but lifecycle transitions must remain explicit, traceable, and distinguishable from validation state, authority level, privacy classification, workflow state, agent state, and implementation state.

KS-0007 defines Authority Level behavior.

WF-0002 depends on KS-0007 because approval may affect authority handling, but approval does not automatically create broad authority unless the approval scope and authority assignment explicitly define that effect.

KS-0008 defines Privacy Classification behavior.

WF-0002 depends on KS-0008 because review and approval must preserve privacy boundaries and must not treat approval as publication permission, export permission, synchronization permission, indexing permission, agent-access permission, or downstream-use permission unless explicitly governed.

KS-0009 defines Validation behavior.

WF-0002 depends on KS-0009 because validation may support review and approval, but validation results must not be silently converted into approval, rejection, authority, privacy clearance, publication readiness, export readiness, migration readiness, or downstream-use permission.

SS-0001 defines storage architecture.

WF-0002 depends on SS-0001 because storage may support review staging, preservation, routing, archiving, and auditability without defining review status, approval status, authority, privacy, validation, or knowledge meaning.

SS-0002 defines practical storage layout.

WF-0002 depends on SS-0002 because review and approval workflows may use draft, review, archive, import, export, migration, implementation-support, workflow-support, agent-support, index, cache, and supporting-asset areas without allowing placement to replace explicit governed state.

AG-0001 defines agent operating boundaries.

WF-0002 depends on AG-0001 because agents may assist review and approval only when their outputs remain traceable, reviewable, scoped, and subordinate to governed human review or governed workflow authority.

WF-0001 defines Knowledge Ingestion behavior.

WF-0002 extends WF-0001 by defining the workflow behavior that follows or supports ingestion when Draft Knowledge Records, workflow outputs, Source References, provenance entries, metadata proposals, relationship proposals, validation results, repair requests, rejected candidates, quarantined items, or approved records require review and approval.

WF-0002 does not replace WF-0001.

WF-0001 answers: How does incoming material become an ingestion candidate, Draft Knowledge Record, workflow output, approved record, rejected item, repaired item, quarantined item, archived item, or routed item?

WF-0002 answers: How are governed entities reviewed, approved, rejected, revised, repaired, escalated, superseded, deprecated, archived, or cleared for downstream use?

WF-0002 is successful when it extends prior standards into a clear review-and-approval workflow without weakening Object Identity, metadata role boundaries, relationship behavior, source-reference behavior, provenance preservation, lifecycle handling, authority expectations, privacy boundaries, validation boundaries, storage boundaries, agent boundaries, implementation independence, or practical daily usability.

## 3. Workflow Scope and Boundaries

WF-0002 applies to review and approval workflows for governed entities within The Brain Standard.

A governed entity MAY require review and approval when its use affects knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage routing, agent behavior, workflow behavior, implementation behavior, publication, export, migration, synchronization, indexing, backup, archival, or downstream use.

Review and approval workflows MAY apply to:

- Knowledge Objects;
- Knowledge Records;
- Draft Knowledge Records;
- Source Material where review affects handling or downstream use;
- Source References;
- provenance records;
- metadata records;
- relationships;
- lifecycle states;
- authority assignments;
- privacy classifications;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- publication candidates;
- synchronization candidates;
- archived records;
- superseded records;
- deprecated records;
- rejected records;
- quarantined records;
- governed documents where applicable;
- decisions;
- other governed entities.

WF-0002 defines workflow behavior for reviewing and approving governed entities.

WF-0002 does not define the content meaning of the governed entities being reviewed.

Knowledge meaning remains governed by the Phase 1 Knowledge Standards.

Storage meaning remains governed by the Phase 2 Storage Standards.

Agent boundaries remain governed by the Phase 3 Agent Framework standards.

Implementation behavior remains governed by implementation documents and reference implementation profiles.

Review and approval workflows SHALL preserve the distinction between:

- review and approval;
- review and validation;
- review and authority;
- approval and authority;
- approval and privacy clearance;
- approval and publication readiness;
- approval and export readiness;
- approval and migration readiness;
- approval and downstream-use readiness;
- workflow completion and approval;
- agent confidence and approval;
- storage placement and approval;
- implementation visibility and approval;
- lifecycle state and validation state;
- lifecycle state and authority level;
- lifecycle state and privacy classification.

A reviewed entity is not automatically approved.

An approved entity is not automatically authoritative beyond its approval scope.

An approved entity is not automatically public, exportable, publishable, migratable, synchronized, indexed, or cleared for downstream use.

A validation-passing entity is not automatically approved.

A workflow-completed entity is not automatically approved.

An agent-recommended entity is not automatically approved.

A stored, indexed, visible, linked, or archived entity is not automatically approved.

Review and approval workflows MUST preserve approval scope.

Approval scope SHOULD identify what use, context, authority, audience, implementation, publication boundary, export boundary, migration boundary, workflow, agent use, or downstream use the approval applies to where that distinction affects interpretation or handling.

Approval outside the approved scope SHOULD require additional review unless a governed standard, specification, workflow, or decision explicitly permits broader use.

WF-0002 SHALL preserve human reviewability where review or approval affects governed meaning, Object Identity, lifecycle state, authority, privacy, publication, export, migration, deletion, supersession, deprecation, or downstream use.

Agents MAY assist review and approval workflows by identifying issues, summarizing records, checking consistency, comparing sources, proposing corrections, drafting review notes, proposing metadata, proposing relationships, supporting validation, detecting privacy risk, detecting authority risk, or preparing review reports.

Agent assistance MUST remain distinguishable from human review, approval, authority assignment, validation success, privacy clearance, publication permission, export permission, migration permission, deletion permission, and downstream-use permission.

Review and approval workflows MAY use storage routing, review folders, workflow queues, implementation displays, tags, statuses, database views, dashboards, or automation signals to support practical operation.

Those signals MUST NOT replace explicit review decisions, approval decisions, lifecycle state, authority level, privacy classification, validation state, provenance, or governed workflow logs where those affect meaning or use.

Review and approval workflows SHOULD minimize unnecessary burden.

A review process SHOULD be strict enough to preserve knowledge integrity, source traceability, privacy, authority, validation, compatibility, and governance, but not so burdensome that routine knowledge maintenance becomes impractical.

WF-0002 applies at the standard level.

A future workflow specification MAY define exact review stages, reviewer roles, approval gates, required checks, review forms, decision records, routing paths, escalation conditions, repair loops, rejection reasons, approval scopes, publication gates, export gates, migration gates, automation triggers, agent roles, or implementation-specific review procedures.

Such specifications are valid only when they preserve the workflow scope and boundaries defined by WF-0002.

## 4. Review Intake and Candidate Registration

Review Intake and Candidate Registration define how governed entities enter the review and approval workflow.

A review and approval workflow SHOULD begin when a governed entity is submitted, routed, staged, flagged, generated, imported, migrated, revised, validated, repaired, escalated, or otherwise identified as requiring review.

A Review Candidate MAY originate from:

- a Knowledge Ingestion workflow;
- a Draft Knowledge Record;
- a proposed Knowledge Record;
- a proposed relationship;
- proposed metadata;
- proposed Source References;
- proposed provenance;
- a validation result;
- an agent output;
- a workflow output;
- an import process;
- an export process;
- a migration process;
- a repair process;
- a privacy review;
- an authority review;
- a lifecycle transition;
- a supersession proposal;
- a deprecation proposal;
- a publication candidate;
- a synchronization candidate;
- another governed process.

Review intake exists so that review does not begin from hidden assumptions, informal routing, storage placement, implementation visibility, agent confidence, workflow completion, or undocumented practice.

A Review Candidate SHOULD be registered or otherwise made traceable where review affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, supersession, deprecation, or downstream use.

Review Candidate registration SHOULD identify or support identification of:

- what entity is being reviewed;
- why review is required;
- what workflow, agent, human, validator, implementation, import process, export process, migration process, or governance process submitted or routed the candidate;
- what prior workflow output, validation result, review note, repair request, escalation, or decision triggered review where applicable;
- what Source Material, Source References, provenance, metadata, relationships, lifecycle state, authority level, privacy classification, and validation state are relevant to the review;
- whether the candidate is new, revised, repaired, disputed, imported, migrated, superseding, deprecated, archived, rejected, quarantined, or otherwise governed;
- whether human review is required;
- whether agent assistance is permitted;
- whether privacy restrictions limit review access;
- whether approval, rejection, repair, escalation, quarantine, archival, supersession, deprecation, publication, export, migration, or downstream-use readiness is being considered.

Review Candidate registration MUST preserve Object Identity where Object Identity already exists.

A review workflow MUST NOT assign a new Object Identity merely because a governed entity entered review.

A review workflow MUST NOT silently merge, split, replace, redirect, supersede, or reinterpret Object Identity during intake.

Where identity is missing, ambiguous, duplicated, conflicting, temporary, imported, migrated, or otherwise unresolved, the Review Candidate SHOULD be flagged for identity review, repair, or escalation before approval.

Review Candidate registration SHOULD preserve Source Material and Knowledge Record distinction.

Source Material submitted for review MUST remain distinguishable from Knowledge Records, Draft Knowledge Records, extracted content, transformed content, workflow outputs, agent outputs, validation outputs, implementation artifacts, import artifacts, export artifacts, and migration artifacts where that distinction affects meaning or use.

Review Candidate registration SHOULD preserve provenance.

Where a Review Candidate is created, submitted, routed, generated, imported, migrated, validated, repaired, escalated, or transformed, the review workflow SHOULD preserve enough provenance to identify the origin and review context.

Review Candidate registration MUST preserve Privacy Classification.

Restricted, sensitive, private, confidential, non-exportable, non-publishable, or otherwise privacy-constrained material MUST NOT be exposed to reviewers, agents, validators, implementations, exports, publications, synchronization processes, indexing systems, or downstream users unless the applicable Privacy Classification and governed workflow permit that access.

Review Candidate registration MAY use storage routing, review folders, workflow queues, dashboards, tags, database views, or implementation signals to support practical operation.

Those signals MUST NOT replace explicit review intake, Review Candidate registration, workflow state, lifecycle state, privacy classification, validation state, provenance, or approval status where those affect governed meaning or use.

A Review Candidate SHOULD remain reviewable until it is approved, rejected, repaired, escalated, deferred, quarantined, archived, superseded, deprecated, withdrawn, or otherwise routed through a governed decision.

Review intake is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what entered review, why it entered review, what scope applies, what restrictions apply, what prior context exists, and what review decision remains pending.

## 5. Review Scope and Approval Scope

Review Scope and Approval Scope define the boundaries of what is being evaluated and what any approval decision permits.

Review Scope identifies what the review covers.

Approval Scope identifies what an approval decision authorizes.

Review Scope and Approval Scope MUST remain explicit where review or approval affects interpretation, authority, privacy, validation, publication, export, migration, automation, agent use, workflow use, implementation behavior, or downstream use.

A Review Scope MAY apply to:

- an entire Knowledge Object;
- a specific Knowledge Record;
- a Draft Knowledge Record;
- selected sections of a record;
- proposed metadata;
- proposed relationships;
- proposed Source References;
- proposed provenance;
- a lifecycle transition;
- an authority assignment;
- a privacy classification;
- a validation result;
- an agent output;
- a workflow output;
- an import record;
- an export record;
- a migration record;
- a publication candidate;
- a synchronization candidate;
- a supersession proposal;
- a deprecation proposal;
- another governed entity or governed change.

Review Scope SHOULD identify what is being reviewed and what is not being reviewed where that distinction affects meaning or use.

A review of metadata does not automatically review content meaning.

A review of structure does not automatically review source support.

A review of Source References does not automatically approve interpretation.

A review of validation results does not automatically approve the governed entity.

A review of privacy classification does not automatically grant publication, export, synchronization, indexing, agent access, implementation access, or downstream-use permission.

A review of authority does not automatically approve broader use beyond the authority scope.

Approval Scope SHOULD identify:

- what entity or change is approved;
- what use is approved;
- what audience, implementation, workflow, agent use, publication boundary, export boundary, migration boundary, or downstream-use context applies;
- whether approval is narrow or broad;
- whether approval is temporary, conditional, limited, historical, superseding, deprecated, archival, or current;
- whether approval depends on validation, privacy review, authority review, source review, relationship review, lifecycle review, repair, or future review;
- whether additional review is required before publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

Approval MUST NOT be generalized beyond its defined scope.

An entity approved for internal knowledge use is not automatically approved for publication.

An entity approved for publication is not automatically approved for unrestricted export.

An entity approved for export is not automatically approved for migration without compatibility review where migration affects governed meaning.

An entity approved for one implementation is not automatically approved as implementation-independent unless the approval scope explicitly supports that use.

An entity approved for one workflow is not automatically approved for all workflows.

An entity approved for agent-assisted use is not automatically approved for unrestricted agent access.

An approved entity may still require privacy restrictions.

An approved entity may still have limited authority.

An approved entity may still require validation for a narrower technical scope.

An approved entity may later become deprecated, superseded, archived, restricted, quarantined, or in need of repair.

Review Scope and Approval Scope MUST remain distinguishable from Lifecycle State.

A lifecycle state may indicate that an entity is Draft, Review, Approved, Rejected, Deprecated, Superseded, Archived, Restricted, Quarantined, Pending Review, Pending Validation, Needs Repair, or governed by another lifecycle state.

Review Scope and Approval Scope define what was reviewed and what approval permits.

Review Scope and Approval Scope MUST remain distinguishable from Authority Level.

Approval may support authority assignment, but approval does not automatically create broad authority unless the approval decision and authority assignment explicitly define that effect.

Review Scope and Approval Scope MUST remain distinguishable from Validation State.

Validation may support review, but validation does not define approval scope by itself.

Review Scope and Approval Scope MUST remain distinguishable from Privacy Classification.

Approval does not weaken privacy classification.

Privacy Classification SHALL take precedence where approval and privacy handling appear to conflict.

Review Scope and Approval Scope MUST remain distinguishable from workflow completion, agent confidence, implementation visibility, storage placement, indexing, publication status, export success, migration success, or downstream-use activity.

A review workflow SHOULD record or preserve enough information for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations to determine whether a later use falls inside or outside the approved scope.

Where scope is unclear, approval SHOULD be treated as limited until clarified by human review, governance review, or a future governed workflow.

Review Scope and Approval Scope are successful when approval remains explicit, bounded, traceable, privacy-respecting, validation-aware, authority-aware, lifecycle-aware, implementation-independent, and safe for downstream use.

## 6. Validation, Source Reference, and Provenance Review

Validation, Source Reference, and Provenance Review define how review and approval workflows evaluate conformance, source support, and origin history before a governed entity is approved, rejected, repaired, escalated, quarantined, archived, superseded, deprecated, or cleared for downstream use.

A review and approval workflow SHOULD consider Validation where validation affects interpretation, reviewability, lifecycle handling, authority handling, privacy handling, relationships, Source References, provenance, compatibility, workflow behavior, agent behavior, implementation behavior, publication, synchronization, indexing, backup, import, export, migration, or downstream use.

Validation Review MAY consider:

- whether validation was performed;
- what validation scope applies;
- what validation result applies;
- who or what performed validation;
- what standard, specification, workflow, implementation profile, object type, import process, export process, migration process, or downstream-use context was validated;
- whether validation is current, stale, partial, failed, passed, warning-only, disputed, superseded, or incomplete;
- whether validation produced errors;
- whether validation produced warnings;
- whether validation exceeded its scope;
- whether validation evidence is sufficient;
- whether validation findings require repair, escalation, quarantine, rejection, archival, deprecation, supersession, or additional review.

Validation may support approval.

Validation does not equal approval unless a future governed workflow or specification explicitly defines that behavior within a controlled scope.

Validation success MUST NOT silently create approval, Authority Level, Privacy Classification, publication readiness, export readiness, migration readiness, synchronization readiness, indexing readiness, implementation permission, agent permission, workflow permission, or downstream-use permission.

Validation failure SHOULD remain visible enough for review or repair within privacy boundaries.

A review and approval workflow SHOULD consider Source References where source support affects interpretation, authority, privacy, validation, relationships, lifecycle state, compatibility, publication, export, migration, or downstream use.

Source Reference Review MAY consider:

- whether required Source References exist;
- whether Source References point to the correct Source Material;
- whether Source Material remains distinguishable from Knowledge Records;
- whether source support is sufficient for the intended use;
- whether Source Material is available, unavailable, restricted, missing, superseded, disputed, stale, incomplete, or unreliable;
- whether Source References preserve privacy boundaries;
- whether source support contradicts, qualifies, limits, or weakens the proposed knowledge;
- whether source support requires authority limitation;
- whether source support requires additional review;
- whether source support requires repair, escalation, quarantine, rejection, archival, deprecation, or supersession.

A missing Source Reference does not automatically invalidate every governed entity.

A missing Source Reference SHOULD be evaluated according to the applicable standard, object type, claim type, review scope, authority scope, privacy classification, validation scope, and downstream-use context.

Where source support is required and missing, approval SHOULD be deferred, limited, repaired, escalated, rejected, or otherwise routed through a governed decision.

A review and approval workflow SHOULD consider Provenance where origin, authorship, extraction, transformation, agent activity, workflow activity, import, export, migration, validation, review, repair, or change history affects interpretation or use.

Provenance Review MAY consider:

- who or what created the governed entity;
- who or what modified it;
- what Source Material was used;
- what extraction occurred;
- what transformation occurred;
- what agent activity occurred;
- what workflow activity occurred;
- what validation activity occurred;
- what review activity occurred;
- what import, export, or migration activity occurred;
- what repair activity occurred;
- what prior decisions affect interpretation;
- whether provenance is sufficient for the intended approval scope;
- whether provenance creates privacy, authority, validation, compatibility, or downstream-use concerns.

Provenance does not replace validation.

Provenance does not create approval by itself.

Provenance does not create Authority Level by itself.

Provenance does not weaken Privacy Classification.

Provenance does not automatically permit publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

Where provenance is missing, incomplete, ambiguous, contradictory, privacy-sensitive, agent-generated, workflow-generated, imported, migrated, or otherwise uncertain, the review workflow SHOULD preserve the issue for human review, repair, escalation, limitation, quarantine, rejection, archival, deprecation, or supersession where required.

Validation, Source Reference, and Provenance Review SHOULD remain practical.

A review workflow SHOULD require the level of validation, source review, and provenance review appropriate to the risk, authority, privacy, lifecycle state, publication boundary, export boundary, migration boundary, implementation boundary, and downstream-use context of the Review Candidate.

A low-risk internal draft may require lighter review.

A high-authority, privacy-sensitive, publication-ready, export-ready, migration-ready, agent-used, or downstream-critical entity SHOULD require stronger review.

Validation, Source Reference, and Provenance Review are successful when review decisions are supported by explicit conformance evidence, source traceability, provenance context, privacy protection, authority awareness, lifecycle awareness, compatibility awareness, and governed scope without confusing validation, source support, or provenance with approval itself.

## 7. Metadata and Relationship Review

Metadata and Relationship Review define how review and approval workflows evaluate metadata and relationships before a governed entity is approved, rejected, repaired, escalated, quarantined, archived, superseded, deprecated, or cleared for downstream use.

A review and approval workflow SHOULD consider metadata where metadata affects Object Identity, interpretation, provenance, relationships, Source References, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, storage behavior, workflow behavior, agent behavior, implementation behavior, publication, export, migration, synchronization, indexing, backup, or downstream use.

Metadata Review MAY consider:

- whether required metadata is present;
- whether metadata is explicit enough for review and interpretation;
- whether metadata supports Object Identity without replacing Object Identity;
- whether metadata remains distinguishable from content;
- whether metadata remains distinguishable from implementation-specific behavior;
- whether metadata remains distinguishable from workflow state, agent output, storage placement, validation state, lifecycle state, authority level, and privacy classification;
- whether metadata is current, stale, incomplete, conflicting, duplicated, excessive, misleading, imported, migrated, agent-generated, workflow-generated, or implementation-specific;
- whether metadata preserves Source References and provenance where required;
- whether metadata preserves privacy boundaries;
- whether metadata supports validation and compatibility;
- whether metadata requires repair, escalation, rejection, quarantine, archival, deprecation, supersession, or additional review.

Metadata may support review.

Metadata does not create approval by itself.

Metadata does not create Authority Level by itself.

Metadata does not weaken Privacy Classification.

Metadata does not replace Source References, provenance, relationships, validation, lifecycle state, workflow logs, agent review, or human review.

A metadata field, tag, folder path, filename, database value, implementation property, workflow value, agent output, or interface signal MUST NOT be treated as approval unless a governed standard, specification, or workflow explicitly defines that behavior.

Where metadata is missing, unclear, inconsistent, excessive, misleading, implementation-specific, agent-generated, workflow-generated, imported, migrated, or otherwise uncertain, the review workflow SHOULD preserve the issue for repair, escalation, limitation, rejection, quarantine, archival, deprecation, supersession, or additional review where required.

A review and approval workflow SHOULD consider relationships where relationships affect meaning, context, provenance, dependency, hierarchy, sequence, evidence, supersession, derivation, governance, validation, authority, privacy, compatibility, publication, export, migration, or downstream use.

Relationship Review MAY consider:

- whether proposed relationships are explicit;
- whether relationship participants are identifiable;
- whether relationship participants resolve to stable Object Identity where required;
- whether Source Material and Knowledge Records remain distinguishable when either participates in a relationship;
- whether relationship type is clear;
- whether relationship direction is clear where direction affects meaning;
- whether relationship strength and relationship confidence remain distinguishable where used;
- whether relationship provenance is sufficient;
- whether relationship lifecycle state is clear;
- whether relationship authority is scoped and supported;
- whether relationship privacy is preserved;
- whether relationship validation has occurred where required;
- whether inferred relationships remain distinguishable from reviewed or approved relationships;
- whether agent-generated relationships remain distinguishable from human-approved relationships;
- whether workflow-generated relationships remain distinguishable from approved relationship meaning;
- whether implementation-specific links, backlinks, graph edges, search associations, vector similarities, tags, folder proximity, or interface signals have been confused with governed relationships.

A relationship may support interpretation.

A relationship does not create approval by itself.

A relationship does not create Authority Level by itself.

A relationship does not weaken Privacy Classification.

A relationship does not automatically permit publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

A proposed, inferred, agent-generated, workflow-generated, imported, migrated, or implementation-derived relationship SHOULD remain reviewable where relationship meaning affects interpretation, authority, privacy, validation, compatibility, publication, export, migration, or downstream use.

Where a relationship is missing, ambiguous, conflicting, circular, unsupported, privacy-sensitive, authority-sensitive, invalid, stale, inferred, agent-generated, workflow-generated, imported, migrated, or otherwise uncertain, the review workflow SHOULD preserve the issue for repair, escalation, limitation, rejection, quarantine, archival, deprecation, supersession, or additional review where required.

Metadata and Relationship Review SHOULD remain proportional to risk.

A low-risk internal draft may require lighter metadata and relationship review.

A high-authority, privacy-sensitive, publication-ready, export-ready, migration-ready, agent-used, relationship-dense, or downstream-critical entity SHOULD require stronger metadata and relationship review.

Metadata and Relationship Review are successful when metadata and relationships remain explicit, traceable, reviewable, privacy-respecting, validation-aware, authority-aware, lifecycle-aware, provenance-preserving, implementation-independent, and safe for downstream use without allowing metadata fields, links, graph signals, agent suggestions, workflow outputs, storage placement, or implementation behavior to become approval by accident.

## 8. Lifecycle, Authority, and Privacy Review

Lifecycle, Authority, and Privacy Review define how review and approval workflows evaluate governed state, interpretive weight, and access boundaries before a governed entity is approved, rejected, repaired, escalated, quarantined, archived, superseded, deprecated, published, exported, migrated, synchronized, indexed, or used downstream.

A review and approval workflow SHOULD consider Lifecycle State where lifecycle status affects interpretation, reviewability, approval, rejection, repair, escalation, quarantine, archival, deprecation, supersession, authority, privacy, validation, relationships, Source References, provenance, compatibility, workflow behavior, agent behavior, implementation behavior, publication, export, migration, or downstream use.

Lifecycle Review MAY consider:

- what lifecycle state applies;
- whether the lifecycle state is explicit;
- whether the lifecycle state is current or historical;
- whether a lifecycle transition is being proposed;
- whether the lifecycle transition has sufficient provenance;
- whether review, validation, approval, rejection, repair, escalation, quarantine, archival, deprecation, or supersession is required;
- whether lifecycle state has been confused with workflow state;
- whether lifecycle state has been confused with validation state;
- whether lifecycle state has been confused with authority level;
- whether lifecycle state has been confused with privacy classification;
- whether lifecycle state has been confused with agent state, implementation state, storage placement, or user-interface display.

A lifecycle transition MAY result from a review and approval workflow.

A lifecycle transition MUST be explicit where it affects governed meaning or use.

Workflow completion MUST NOT be treated as a lifecycle transition unless the transition is explicitly represented or governed.

Approval MAY support a lifecycle transition to Approved within a defined scope.

Approval does not automatically create broader authority, privacy clearance, publication permission, export permission, migration permission, synchronization permission, indexing permission, or downstream-use permission.

A review and approval workflow SHOULD consider Authority Level where authority affects interpretation, governance, review weight, trust boundary, publication, validation, automation, migration, export, relationship creation, agent reasoning, implementation behavior, or downstream use.

Authority Review MAY consider:

- what Authority Level applies;
- what authority scope applies;
- who or what assigned or proposed the Authority Level;
- whether authority is current, historical, limited, suspended, superseded, inherited, proposed, reviewed, approved, rejected, deprecated, archived, restricted, or otherwise governed;
- whether authority depends on approval, source support, provenance, validation, relationship context, privacy review, lifecycle state, compatibility, or governance decision;
- whether authority has been confused with approval;
- whether authority has been confused with lifecycle state;
- whether authority has been confused with validation state;
- whether authority has been confused with source existence, source reliability, relationship strength, relationship confidence, agent confidence, workflow completion, implementation visibility, storage placement, publication status, export success, or downstream use.

Approval may support authority assignment.

Approval does not automatically create broad authority unless the approval decision and authority assignment explicitly define that effect.

Authority Level MUST remain scoped where scope affects interpretation or use.

A low-authority approved entity MUST NOT be treated as high-authority merely because it was approved.

A high-authority entity MUST NOT be treated as current or usable merely because it is high-authority if it is superseded, deprecated, archived, restricted, quarantined, or otherwise limited.

A review and approval workflow MUST consider Privacy Classification where access, visibility, exposure, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream use affects privacy handling.

Privacy Review MAY consider:

- what Privacy Classification applies;
- what privacy scope applies;
- whether access is permitted;
- whether visibility is permitted;
- whether publication is permitted;
- whether synchronization is permitted;
- whether indexing is permitted;
- whether export is permitted;
- whether backup is permitted;
- whether agent access is permitted;
- whether workflow access is permitted;
- whether implementation access is permitted;
- whether downstream use is permitted;
- whether privacy handling is current, stale, incomplete, ambiguous, conflicting, inherited, escalated, reduced, restricted, or pending review;
- whether privacy has been confused with lifecycle state, authority level, validation state, source availability, storage placement, implementation visibility, workflow completion, or agent confidence.

Privacy Classification SHALL take precedence over convenience, automation, publication, export, migration, synchronization, indexing, backup, agent access, implementation access, and downstream use where privacy risk exists.

Approval does not weaken Privacy Classification.

Approval does not automatically permit publication.

Approval does not automatically permit export.

Approval does not automatically permit migration.

Approval does not automatically permit synchronization.

Approval does not automatically permit indexing.

Approval does not automatically permit agent access.

Approval does not automatically permit implementation exposure.

Approval does not automatically permit downstream use.

Where lifecycle, authority, or privacy information is missing, unclear, conflicting, unsupported, stale, imported, migrated, agent-generated, workflow-generated, implementation-specific, or otherwise uncertain, the review workflow SHOULD preserve the issue for human review, repair, escalation, limitation, rejection, quarantine, archival, deprecation, supersession, or additional review where required.

Lifecycle, Authority, and Privacy Review SHOULD remain proportional to risk.

A low-risk internal draft may require lighter lifecycle, authority, and privacy review.

A high-authority, privacy-sensitive, publication-ready, export-ready, migration-ready, agent-used, implementation-exposed, or downstream-critical entity SHOULD require stronger lifecycle, authority, and privacy review.

Lifecycle, Authority, and Privacy Review are successful when governed state, authority scope, and privacy boundaries remain explicit, traceable, reviewable, validation-aware, provenance-preserving, implementation-independent, and safe for downstream use without allowing lifecycle state, authority level, privacy classification, workflow completion, validation results, agent confidence, storage placement, or implementation visibility to be confused with one another.

## 9. Human Review and Agent-Assisted Review

Human Review and Agent-Assisted Review define how humans and agents participate in review and approval workflows while preserving reviewability, traceability, privacy, authority control, validation boundaries, and governance.

Human Review SHOULD be used where review or approval affects governed meaning, Object Identity, Source References, provenance, metadata, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, supersession, deprecation, or downstream use.

Human Review MAY include:

- confirming a Review Candidate;
- defining Review Scope;
- defining Approval Scope;
- evaluating validation results;
- evaluating Source References;
- evaluating provenance;
- evaluating metadata;
- evaluating relationships;
- evaluating lifecycle state;
- evaluating authority level;
- evaluating privacy classification;
- resolving ambiguity;
- correcting errors;
- requesting repair;
- approving a governed entity;
- rejecting a governed entity;
- deferring a decision;
- escalating a risk;
- quarantining unsafe material;
- archiving material;
- approving supersession;
- approving deprecation;
- limiting approval scope;
- limiting authority scope;
- limiting downstream use.

Human Review SHOULD preserve enough review context for future interpretation.

A human review decision SHOULD identify or support identification of:

- what entity was reviewed;
- what scope was reviewed;
- what decision was made;
- who performed or confirmed the review where applicable;
- when the review occurred where applicable;
- what validation, Source References, provenance, metadata, relationships, lifecycle state, authority level, and privacy classification were considered;
- what issues were found;
- what repairs were required;
- what limits apply;
- what approval scope applies;
- whether future review is required.

Human Review MUST remain distinguishable from workflow completion, validation success, agent confidence, storage placement, implementation visibility, publication status, export success, migration success, synchronization, indexing, backup, or downstream-use activity.

Agent-Assisted Review MAY support human review and governed workflow operation.

Agents MAY assist by:

- summarizing Review Candidates;
- comparing records;
- detecting inconsistencies;
- identifying missing metadata;
- identifying unclear relationships;
- identifying missing Source References;
- identifying provenance gaps;
- identifying lifecycle ambiguity;
- identifying authority ambiguity;
- identifying privacy risks;
- identifying validation errors;
- identifying validation warnings;
- suggesting repair actions;
- drafting review notes;
- drafting approval summaries;
- drafting rejection summaries;
- preparing issue reports;
- preparing escalation reports;
- preparing conformance reports;
- proposing limited approval scope;
- proposing downstream-use limits.

Agent assistance MUST remain traceable where agent output affects review, approval, rejection, repair, escalation, lifecycle handling, authority handling, privacy handling, validation, publication, export, migration, deletion, supersession, deprecation, or downstream use.

Agent assistance MUST remain distinguishable from Human Review.

Agent assistance MUST remain distinguishable from approval.

Agent assistance MUST remain distinguishable from Authority Level.

Agent assistance MUST remain distinguishable from Validation State.

Agent assistance MUST remain distinguishable from Privacy Classification.

Agent assistance MUST remain distinguishable from Lifecycle State.

Agent assistance MUST remain distinguishable from publication permission, export permission, migration permission, deletion permission, synchronization permission, indexing permission, implementation permission, and downstream-use permission.

An agent MAY recommend approval.

An agent MUST NOT silently approve a governed entity where human review or governed workflow approval is required.

An agent MAY recommend rejection.

An agent MUST NOT silently reject a governed entity where human review or governed workflow decision is required.

An agent MAY recommend repair.

An agent MUST NOT silently modify governed meaning, Object Identity, Source References, provenance, metadata, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation State, publication status, export permission, migration permission, or downstream-use permission unless explicitly authorized by a governed workflow within a defined scope.

An agent MAY identify privacy risk.

An agent MUST NOT declassify, expose, publish, export, synchronize, index, or route privacy-constrained material beyond its permitted boundary unless explicitly authorized by Privacy Classification and governed workflow.

An agent MAY support validation.

An agent MUST NOT treat its validation output as approval, authority, privacy clearance, publication readiness, export readiness, migration readiness, or downstream-use readiness unless a future governed workflow or specification explicitly defines that behavior within a controlled scope.

Human Review and Agent-Assisted Review SHOULD remain practical.

A review workflow SHOULD use human judgment where risk, ambiguity, authority, privacy, publication, export, migration, deletion, supersession, deprecation, or downstream use requires judgment.

A review workflow MAY use agent assistance to reduce cognitive load, improve consistency, identify issues, prepare review materials, and support maintenance.

Human Review and Agent-Assisted Review are successful when humans remain responsible for governed judgment where required, agents remain useful but bounded, outputs remain traceable, privacy boundaries remain protected, approval remains explicit, and review decisions remain meaningful across storage changes, workflow changes, agent changes, implementation changes, import, export, migration, backup, synchronization, indexing, publication, and downstream use.

## 10. Approval, Rejection, and Deferral Decisions

Approval, Rejection, and Deferral Decisions define how review and approval workflows record and apply governed decisions after review.

A review and approval workflow SHOULD produce an explicit decision where a Review Candidate has been evaluated and the result affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, synchronization, indexing, backup, agent use, implementation use, or downstream use.

A review decision MAY result in:

- approval;
- limited approval;
- conditional approval;
- rejection;
- deferral;
- revision request;
- repair request;
- escalation;
- quarantine;
- archival;
- supersession;
- deprecation;
- withdrawal;
- another governed routing outcome.

An Approval Decision SHOULD identify or support identification of:

- what entity was approved;
- what Approval Scope applies;
- who or what approved the entity where applicable;
- when approval occurred where applicable;
- what Review Scope was evaluated;
- what validation results were considered;
- what Source References were considered;
- what provenance was considered;
- what metadata was considered;
- what relationships were considered;
- what lifecycle state was considered;
- what Authority Level was considered;
- what Privacy Classification was considered;
- what limits, conditions, warnings, restrictions, or future review requirements apply;
- whether approval supports publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

Approval MUST remain explicit where approval affects governed meaning or use.

Approval MUST remain scoped where scope affects interpretation, authority, privacy, publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

Approval MUST NOT be inferred solely from:

- workflow completion;
- validation success;
- agent confidence;
- human visibility;
- implementation visibility;
- storage placement;
- folder location;
- filename;
- tag;
- backlink;
- graph position;
- search ranking;
- index presence;
- publication success;
- export success;
- migration success;
- synchronization success;
- backup success;
- downstream-use activity.

Approval MAY support a lifecycle transition.

Approval MAY support an authority assignment.

Approval MAY support publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use only where the Approval Scope and applicable standards permit that effect.

Approval does not weaken Privacy Classification.

Approval does not eliminate validation requirements outside the approved validation scope.

Approval does not remove Source Reference or provenance requirements where those remain required for interpretation or use.

Approval does not make an implementation-specific representation the standard.

Approval does not prevent future review, repair, deprecation, supersession, archival, quarantine, restriction, or rejection if later evidence, validation, privacy review, authority review, lifecycle review, compatibility review, governance review, import, export, migration, or implementation behavior reveals an issue.

A Rejection Decision SHOULD identify or support identification of:

- what entity was rejected;
- what Review Scope was evaluated;
- why rejection occurred;
- who or what rejected the entity where applicable;
- when rejection occurred where applicable;
- whether rejection applies to the whole entity or only a specific use, scope, claim, relationship, metadata element, Source Reference, provenance record, lifecycle transition, authority assignment, privacy classification, validation result, publication candidate, export candidate, migration candidate, or downstream-use context;
- whether rejected material should be repaired, archived, quarantined, superseded, deprecated, deleted, preserved historically, or routed elsewhere;
- whether privacy restrictions still apply;
- whether future review is permitted.

Rejection MUST NOT silently delete governed entities, Source Material, provenance, relationships, validation results, workflow logs, review history, or decision context where preservation is required for auditability, compatibility, migration, source traceability, privacy, governance, or historical interpretation.

Rejected material MAY remain historically preserved where preservation supports reviewability, auditability, provenance, compatibility, source traceability, governance, or future repair.

Rejected material MUST remain privacy-protected where privacy restrictions apply.

A Deferral Decision SHOULD identify or support identification of:

- what decision was deferred;
- why the decision was deferred;
- what issue prevents approval or rejection;
- what additional review, validation, Source Reference, provenance, metadata, relationship, lifecycle, authority, privacy, compatibility, human review, agent assistance, repair, escalation, or governance action is required;
- who or what deferred the decision where applicable;
- when deferral occurred where applicable;
- whether the Review Candidate may be used while deferred;
- what restrictions apply during deferral;
- when future review should occur where applicable.

Deferral MUST NOT be treated as approval.

Deferral MUST NOT be treated as rejection.

Deferral MUST NOT silently authorize publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

A deferred entity SHOULD remain in an explicit reviewable state until approved, rejected, repaired, escalated, quarantined, archived, superseded, deprecated, withdrawn, or otherwise routed through a governed decision.

Approval, Rejection, and Deferral Decisions SHOULD preserve workflow logs where logs are required for auditability, provenance, validation, review, authority, privacy, compatibility, governance, migration, import, export, publication, or downstream use.

Approval, Rejection, and Deferral Decisions are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what decision was made, what scope applies, what evidence was considered, what restrictions remain, what downstream use is permitted, and what future review or repair is required.

## 11. Revision, Repair, Escalation, and Quarantine

Revision, Repair, Escalation, and Quarantine define how review and approval workflows handle issues that prevent immediate approval, rejection, archival, supersession, deprecation, publication, export, migration, or downstream use.

A review and approval workflow SHOULD support Revision where a governed entity requires change before approval, continued use, publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

Revision MAY address:

- unclear content;
- incomplete content;
- inaccurate content;
- outdated content;
- missing metadata;
- incorrect metadata;
- missing Source References;
- weak source support;
- missing provenance;
- incomplete provenance;
- unclear relationships;
- incorrect relationships;
- lifecycle ambiguity;
- authority ambiguity;
- privacy ambiguity;
- validation errors;
- validation warnings;
- compatibility issues;
- implementation-specific assumptions;
- agent-generated uncertainty;
- workflow-generated uncertainty;
- import issues;
- export issues;
- migration issues;
- downstream-use concerns.

A Revision SHOULD preserve Object Identity unless the revision creates, separates, merges, splits, redirects, supersedes, or materially changes the Knowledge Object through a governed identity process.

A Revision SHOULD preserve provenance where the revision affects meaning, reviewability, authority, privacy, validation, relationships, Source References, compatibility, publication, export, migration, or downstream use.

A Revision SHOULD remain distinguishable from approval.

A revised entity SHOULD return to review where the revision affects governed meaning or use.

Repair is a corrective action used to resolve structural, metadata, identity, relationship, Source Reference, provenance, lifecycle, authority, privacy, validation, storage, agent, workflow, implementation, import, export, migration, compatibility, publication, or downstream-use issues.

Repair MAY be required when:

- required structure is missing;
- required metadata is missing or incorrect;
- Object Identity is missing, ambiguous, duplicated, conflicting, or unstable;
- relationships are missing, unsupported, invalid, misleading, or privacy-sensitive;
- Source References are missing, incorrect, unavailable, restricted, stale, disputed, or insufficient;
- provenance is missing, incomplete, ambiguous, contradictory, privacy-sensitive, or unsupported;
- lifecycle state is unclear, conflicting, or inappropriate;
- Authority Level is unclear, unsupported, overbroad, stale, or incorrectly assigned;
- Privacy Classification is unclear, insufficient, conflicting, stale, or unsafe;
- validation fails, becomes stale, exceeds scope, or produces unresolved warnings;
- storage placement creates confusion;
- agent output creates ambiguity;
- workflow output creates ambiguity;
- implementation behavior creates hidden assumptions;
- import, export, or migration creates compatibility risk.

A Repair Request SHOULD identify or support identification of:

- what issue requires repair;
- what entity is affected;
- what standard, specification, workflow, validation result, review decision, privacy requirement, authority requirement, lifecycle rule, relationship rule, Source Reference expectation, provenance expectation, storage rule, agent boundary, implementation boundary, import rule, export rule, migration rule, or governance requirement is involved;
- what repair action is requested;
- who or what requested repair where applicable;
- when repair was requested where applicable;
- whether the entity may be used before repair;
- whether additional review is required after repair;
- whether privacy restrictions apply during repair.

Repair MUST NOT silently create approval.

Repair MUST NOT silently create Authority Level.

Repair MUST NOT silently weaken Privacy Classification.

Repair MUST NOT silently authorize publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

Escalation is required where a review condition cannot be safely resolved within the current workflow scope.

A review and approval workflow SHOULD escalate when unresolved issues affect:

- Object Identity;
- governed meaning;
- Source Material distinction;
- Source References;
- provenance;
- metadata role boundaries;
- relationship meaning;
- lifecycle transitions;
- Authority Level;
- Privacy Classification;
- Validation;
- publication;
- export;
- migration;
- deletion;
- supersession;
- deprecation;
- compatibility;
- governance;
- human safety;
- legal sensitivity;
- security sensitivity;
- downstream-critical use.

Escalation MAY route an issue to:

- human review;
- governance review;
- privacy review;
- authority review;
- validation review;
- source review;
- relationship review;
- lifecycle review;
- compatibility review;
- implementation review;
- agent-boundary review;
- storage review;
- import review;
- export review;
- migration review;
- another governed workflow.

An Escalation SHOULD identify or support identification of:

- what issue was escalated;
- why escalation was required;
- what risk or ambiguity exists;
- what entity is affected;
- what scope applies;
- what decision is needed;
- who or what escalated the issue where applicable;
- when escalation occurred where applicable;
- what access restrictions apply;
- what temporary handling state applies;
- whether quarantine, deferral, repair, rejection, archival, supersession, or deprecation is required.

Quarantine is used to isolate or withhold a governed entity from normal use because of unresolved validity, safety, privacy, compatibility, source, provenance, integrity, authority, lifecycle, relationship, workflow, agent, implementation, import, export, migration, publication, or downstream-use concerns.

A review and approval workflow SHOULD quarantine material where continued normal use creates unacceptable risk before review, repair, escalation, rejection, archival, supersession, or deprecation can be completed.

Quarantine MAY apply when:

- Privacy Classification is missing, unclear, conflicting, or unsafe;
- Source Material is suspicious, restricted, corrupted, unavailable, or unverifiable;
- provenance is missing, contradictory, privacy-sensitive, or suspicious;
- Object Identity is conflicting or unstable;
- relationships expose restricted information;
- validation finds serious errors;
- authority is overstated or unsupported;
- lifecycle state is unsafe for use;
- agent output creates high-risk ambiguity;
- import, export, or migration creates compatibility risk;
- publication, synchronization, indexing, or downstream use would create exposure risk.

Quarantine MUST remain distinguishable from rejection.

Quarantine MUST remain distinguishable from archival.

Quarantine MUST remain distinguishable from deprecation.

Quarantine MUST remain distinguishable from supersession.

Quarantine MUST remain distinguishable from approval.

Quarantined material SHOULD remain traceable and reviewable within its permitted privacy boundary.

Quarantined material MUST NOT be exposed, published, exported, synchronized, indexed, used by agents, migrated, or used downstream unless the applicable Privacy Classification and governed workflow permit that handling.

Revision, Repair, Escalation, and Quarantine are successful when issues are corrected, contained, escalated, or withheld without silently changing governed meaning, weakening privacy, overstating authority, bypassing validation, erasing provenance, breaking relationships, losing source traceability, or creating downstream-use risk.

## 12. Supersession, Deprecation, Archival, and Historical Preservation

Supersession, Deprecation, Archival, and Historical Preservation define how review and approval workflows handle governed entities that are replaced, discouraged for future use, preserved for history, or retained for auditability and compatibility.

Supersession occurs when one governed entity, rule, record, relationship, Source Reference, provenance record, metadata element, lifecycle state, authority assignment, privacy classification, validation result, workflow output, decision, version, or representation is replaced by another while preserving historical traceability.

A review and approval workflow SHOULD support Supersession where a governed entity is replaced because of correction, revision, update, merge, split, migration, import, export, standard change, workflow change, implementation change, source change, validation change, authority change, privacy change, compatibility change, or governance decision.

A Supersession Decision SHOULD identify or support identification of:

- what entity is being superseded;
- what entity supersedes it;
- why supersession occurred;
- who or what approved supersession where applicable;
- when supersession occurred where applicable;
- what Review Scope was evaluated;
- what Approval Scope applies to the superseding entity;
- whether Object Identity is preserved, redirected, split, merged, replaced, or otherwise affected through a governed identity process;
- what Source References remain relevant;
- what provenance must be preserved;
- what relationships must be preserved, revised, deprecated, archived, repaired, redirected, or reviewed;
- what lifecycle transition applies;
- what authority changes apply;
- what privacy restrictions continue to apply;
- what validation or compatibility review is required;
- whether publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use is permitted.

Supersession MUST NOT silently erase the superseded entity where historical preservation is required for provenance, auditability, compatibility, legal sensitivity, privacy handling, migration, import, export, publication history, relationship interpretation, source traceability, governance, or downstream interpretation.

Supersession MUST preserve privacy boundaries.

Supersession MUST preserve enough provenance to determine why the prior entity was replaced.

Supersession SHOULD preserve or redirect relationships where relationship preservation affects meaning, compatibility, source traceability, authority, privacy, validation, migration, import, export, publication, or downstream use.

Deprecation occurs when a governed entity remains historically available but is no longer recommended for future use.

A review and approval workflow SHOULD support Deprecation where a governed entity is outdated, discouraged, replaced in practice, limited in authority, superseded for future use, incompatible with a newer standard, risky for downstream use, or otherwise no longer recommended.

A Deprecation Decision SHOULD identify or support identification of:

- what entity is deprecated;
- why deprecation occurred;
- who or what approved deprecation where applicable;
- when deprecation occurred where applicable;
- whether a replacement exists;
- whether the deprecated entity remains valid for historical interpretation;
- whether the deprecated entity remains authoritative for any limited scope;
- whether privacy restrictions continue to apply;
- whether relationships should remain active, limited, deprecated, archived, repaired, or superseded;
- whether Source References and provenance remain sufficient;
- whether validation or compatibility review is required;
- whether publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use is limited or prohibited.

Deprecation MUST remain distinguishable from rejection.

Deprecation MUST remain distinguishable from archival.

Deprecation MUST remain distinguishable from supersession.

Deprecation MUST remain distinguishable from invalidity.

A deprecated entity MAY remain valid for historical, evidentiary, audit, compatibility, migration, governance, or reference purposes.

A deprecated entity MUST NOT be treated as recommended for future use unless a later governed review revises its lifecycle state or approved use.

Archival occurs when a governed entity is preserved for historical, audit, compatibility, migration, governance, legal, privacy, source-traceability, provenance, or reference purposes but is not treated as active by default.

A review and approval workflow SHOULD support Archival where a governed entity no longer requires active review or use but must remain preserved.

An Archival Decision SHOULD identify or support identification of:

- what entity is archived;
- why archival occurred;
- who or what approved archival where applicable;
- when archival occurred where applicable;
- whether the archive is active, historical, restricted, superseded, deprecated, rejected, quarantined, or preserved for another reason;
- what privacy restrictions apply;
- what Source References and provenance must remain available;
- what relationships should remain visible, limited, deprecated, archived, repaired, or hidden;
- whether validation or compatibility review is required before future restoration or use;
- whether publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use is permitted.

Archival MUST NOT silently approve a governed entity.

Archival MUST NOT silently reject a governed entity.

Archival MUST NOT silently weaken Privacy Classification.

Archival MUST NOT silently erase provenance, Source References, relationships, validation results, workflow logs, review decisions, authority context, privacy context, or compatibility context where those remain required.

Historical Preservation exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can understand past decisions, prior states, replaced entities, deprecated entities, archived entities, rejected entities, quarantined entities, repairs, escalations, and review history.

Historical Preservation SHOULD retain enough context to determine:

- what changed;
- why it changed;
- who or what changed it where applicable;
- what review occurred;
- what approval, rejection, deferral, repair, escalation, quarantine, supersession, deprecation, or archival decision occurred;
- what Source References and provenance supported the decision;
- what relationships were affected;
- what lifecycle state changed;
- what authority changed;
- what privacy restrictions continued;
- what validation or compatibility findings existed;
- what downstream-use limits applied.

Historical Preservation MUST respect Privacy Classification.

Historical Preservation MUST NOT expose restricted information merely because historical access, auditability, search, validation, publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use would be convenient.

Supersession, Deprecation, Archival, and Historical Preservation are successful when prior knowledge remains interpretable, traceable, privacy-protected, validation-aware, authority-aware, relationship-aware, source-supported where required, compatible with migration, and usable for governance without allowing outdated, superseded, deprecated, archived, rejected, or quarantined material to be mistaken for current approved knowledge.

## 13. Publication, Export, Migration, and Downstream-Use Readiness

Publication, Export, Migration, and Downstream-Use Readiness define how review and approval workflows determine whether a governed entity may safely move beyond its current use boundary.

Readiness means that a governed entity has satisfied the applicable review, approval, validation, source-reference, provenance, metadata, relationship, lifecycle, authority, privacy, compatibility, storage, agent, workflow, implementation, publication, export, migration, or downstream-use expectations for a defined scope.

Readiness MUST remain scoped.

A governed entity may be ready for one use while not ready for another.

A governed entity approved for internal use is not automatically ready for publication.

A governed entity approved for publication is not automatically ready for unrestricted export.

A governed entity approved for export is not automatically ready for migration.

A governed entity approved for migration is not automatically ready for publication.

A governed entity approved for one downstream use is not automatically approved for all downstream use.

A review and approval workflow SHOULD evaluate Publication Readiness where a governed entity may be made visible, accessible, distributed, synchronized, indexed, displayed, cited, shared, or otherwise exposed beyond its prior boundary.

Publication Readiness MAY require review of:

- Approval Scope;
- Privacy Classification;
- Authority Level;
- Validation State;
- Source References;
- provenance;
- metadata;
- relationships;
- lifecycle state;
- publication audience;
- publication context;
- restricted content;
- redaction needs;
- source permissions;
- attribution needs;
- compatibility concerns;
- downstream-use limits;
- implementation behavior.

Publication Readiness MUST NOT be inferred solely from approval.

Publication Readiness MUST NOT be inferred solely from implementation visibility, storage placement, indexing, synchronization, agent confidence, validation success, export success, migration success, or workflow completion.

A review and approval workflow SHOULD evaluate Export Readiness where a governed entity may be produced, copied, packaged, shared, transferred, published, synchronized, migrated, or otherwise made available outside the current compliant environment.

Export Readiness MAY require review of:

- whether export is permitted by Privacy Classification;
- whether export is permitted by Approval Scope;
- whether export is permitted by Authority Level or use-authority limits;
- whether Source References and provenance are exportable;
- whether restricted Source Material is included, excluded, redacted, summarized, referenced, or withheld;
- whether relationships expose restricted or misleading context;
- whether metadata exposes restricted information;
- whether validation is current for the export scope;
- whether compatibility expectations are satisfied;
- whether export preserves Object Identity;
- whether export preserves lifecycle state;
- whether export preserves authority context;
- whether export preserves privacy context;
- whether export preserves review decisions and workflow logs where required.

Export Readiness MUST NOT be inferred solely from technical export success.

A file that can be exported is not automatically approved for export.

An export package that was generated successfully is not automatically valid, authoritative, public, privacy-cleared, migration-ready, or downstream-use ready.

A review and approval workflow SHOULD evaluate Migration Readiness where a governed entity may move between storage systems, implementations, schemas, vaults, repositories, databases, file formats, workflow environments, agent environments, or standard versions.

Migration Readiness MAY require review of:

- Object Identity preservation;
- metadata preservation;
- relationship preservation;
- Source Reference preservation;
- provenance preservation;
- lifecycle state preservation;
- authority preservation;
- privacy preservation;
- validation preservation;
- workflow log preservation;
- implementation-specific field handling;
- storage layout compatibility;
- archive handling;
- backup handling;
- import expectations;
- export expectations;
- migration provenance;
- compatibility risks;
- loss risks;
- review requirements after migration.

Migration Readiness MUST NOT be inferred solely from technical migration success.

A migrated entity is not automatically approved, authoritative, valid, publishable, exportable, privacy-cleared, or ready for downstream use.

A review and approval workflow SHOULD evaluate Downstream-Use Readiness where a governed entity may be used for later interpretation, automation, publication, export, migration, relationship creation, validation, decision support, agent reasoning, workflow execution, implementation behavior, or dependent activity.

Downstream-Use Readiness MAY require review of:

- intended use;
- approval scope;
- authority scope;
- privacy scope;
- validation scope;
- lifecycle state;
- source support;
- provenance context;
- relationship context;
- metadata completeness;
- compatibility expectations;
- risk level;
- agent-access permissions;
- implementation-access permissions;
- publication limits;
- export limits;
- migration limits;
- human review requirements.

Downstream-Use Readiness MUST NOT be inferred solely from approval unless the approval scope explicitly includes the downstream use.

Downstream-Use Readiness MUST NOT be inferred from agent confidence, workflow completion, validation success, implementation visibility, storage placement, publication, export, migration, synchronization, indexing, backup, citation, or repeated use.

Where Publication Readiness, Export Readiness, Migration Readiness, or Downstream-Use Readiness is unclear, the governed entity SHOULD be treated as not ready for that use until clarified through human review, validation review, privacy review, authority review, compatibility review, governance review, or a future governed workflow.

Readiness decisions SHOULD be traceable where readiness affects governed meaning, authority, privacy, publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use.

A readiness decision SHOULD identify or support identification of:

- what entity was evaluated;
- what readiness scope applies;
- what use is permitted;
- what use is not permitted;
- what approval decision supports readiness;
- what validation result supports readiness;
- what Source References and provenance support readiness;
- what lifecycle state applies;
- what Authority Level applies;
- what Privacy Classification applies;
- what relationships or metadata affect readiness;
- what restrictions, conditions, warnings, or future review requirements apply.

Publication, Export, Migration, and Downstream-Use Readiness are successful when governed entities move beyond their current boundary only through explicit, scoped, traceable, privacy-respecting, validation-aware, authority-aware, lifecycle-aware, provenance-preserving, and implementation-independent decisions.

## 14. Workflow Logging, Auditability, and Traceability

Workflow Logging, Auditability, and Traceability define how review and approval workflows preserve enough context for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations to understand what happened and why.

A review and approval workflow SHOULD preserve workflow logs where review activity affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, supersession, deprecation, archival, quarantine, or downstream use.

A Workflow Log MAY record or support identification of:

- what entity entered review;
- when the entity entered review where applicable;
- why review was required;
- who or what submitted the entity for review where applicable;
- what Review Scope applied;
- what Approval Scope applied;
- what validation results were considered;
- what Source References were considered;
- what provenance was considered;
- what metadata was considered;
- what relationships were considered;
- what lifecycle state was considered;
- what Authority Level was considered;
- what Privacy Classification was considered;
- what agent assistance occurred;
- what human review occurred;
- what issues were identified;
- what repair was requested;
- what escalation occurred;
- what quarantine decision occurred;
- what approval decision occurred;
- what rejection decision occurred;
- what deferral decision occurred;
- what supersession decision occurred;
- what deprecation decision occurred;
- what archival decision occurred;
- what readiness decision occurred;
- what publication, export, migration, synchronization, indexing, backup, agent-use, implementation-use, or downstream-use limits apply.

Workflow Logging MUST preserve privacy boundaries.

A workflow log MUST NOT expose restricted information merely because logging, auditability, validation, search, indexing, publication, export, migration, agent use, implementation use, or downstream use would be convenient.

Where a full log would expose restricted information, the workflow SHOULD preserve enough authorized traceability for future review without unnecessarily exposing restricted content.

Workflow Logging SHOULD preserve provenance.

Where review, approval, rejection, repair, escalation, quarantine, supersession, deprecation, archival, publication, export, migration, or downstream-use readiness affects interpretation or use, the workflow SHOULD preserve enough provenance to determine who or what participated and what context supported the decision.

Workflow Logging SHOULD preserve validation context.

Where validation affects review or approval, the workflow SHOULD preserve enough validation context to determine what was checked, what scope applied, what result occurred, what warnings or errors existed, and whether validation was used appropriately.

Workflow Logging SHOULD preserve agent context.

Where agent assistance affects review or approval, the workflow SHOULD preserve enough context to determine what the agent did, what output was produced, what confidence or uncertainty was expressed where applicable, what human review occurred, and whether the agent output remained subordinate to governed review.

Workflow Logging SHOULD preserve human-review context.

Where human review affects approval, rejection, repair, escalation, quarantine, supersession, deprecation, archival, readiness, or downstream use, the workflow SHOULD preserve enough context to determine what decision was made and what scope applied.

Auditability means that later review can determine whether the workflow followed the applicable standards, specifications, privacy expectations, validation expectations, authority expectations, lifecycle expectations, storage expectations, agent boundaries, implementation boundaries, and governance requirements.

Auditability SHOULD support:

- review reconstruction;
- decision review;
- provenance review;
- validation review;
- privacy review;
- authority review;
- lifecycle review;
- relationship review;
- Source Reference review;
- repair review;
- escalation review;
- quarantine review;
- supersession review;
- deprecation review;
- archival review;
- readiness review;
- import review;
- export review;
- migration review;
- compatibility review;
- governance review.

Traceability means that a workflow decision can be connected to the governed entity, review context, source support, provenance, metadata, relationships, lifecycle state, authority level, privacy classification, validation result, human review, agent assistance, storage action, implementation action, and downstream-use effect where those affect meaning or use.

Traceability MUST remain implementation-independent where traceability affects governed meaning, authority, privacy, validation, publication, export, migration, or downstream use.

A workflow log may be represented through Markdown records, metadata, review notes, workflow records, decision records, sidecar files, database records, issue records, audit trails, implementation logs, or future governed formats.

The representation method does not define workflow meaning.

A workflow log is compliant only if it preserves governed traceability across inspection, validation, migration, export, import, backup, restoration, synchronization, and implementation replacement where those concerns apply.

Workflow Logging, Auditability, and Traceability SHOULD remain proportional to risk.

A low-risk internal draft may require lighter logging.

A high-authority, privacy-sensitive, publication-ready, export-ready, migration-ready, agent-used, implementation-exposed, or downstream-critical entity SHOULD require stronger logging.

Workflow Logging, Auditability, and Traceability are successful when future review can determine what happened, why it happened, what evidence supported it, who or what participated, what scope applied, what restrictions remain, and whether the workflow preserved knowledge meaning, privacy boundaries, validation boundaries, authority boundaries, lifecycle handling, agent boundaries, storage boundaries, implementation independence, and governance.

## 15. Workflow Conformance Requirements

Workflow Conformance Requirements define the minimum behavior required for a review and approval workflow to conform to WF-0002.

A WF-0002-conformant workflow SHALL preserve the purpose, scope, boundaries, reviewability, traceability, privacy expectations, validation expectations, authority expectations, lifecycle expectations, storage expectations, agent boundaries, implementation independence, and downstream-use limits defined by this standard.

A conformance claim MUST identify or support identification of the workflow, workflow scope, governed entity types, review candidates, approval candidates, approval scopes, review outputs, decision outputs, storage areas, agent involvement, validation involvement, implementation involvement, and downstream-use contexts to which the claim applies where those affect interpretation or use.

A WF-0002-conformant workflow SHALL preserve Review Scope and Approval Scope.

Review and approval MUST remain explicit, scoped, traceable, and distinguishable from validation, authority, privacy clearance, publication readiness, export readiness, migration readiness, workflow completion, agent confidence, implementation visibility, storage placement, indexing, synchronization, backup, and downstream-use activity.

A WF-0002-conformant workflow SHALL preserve Object Identity boundaries.

Review, approval, rejection, deferral, repair, escalation, quarantine, archival, supersession, deprecation, publication, export, migration, synchronization, indexing, agent use, implementation use, or downstream use MUST NOT silently create, remove, merge, split, replace, redirect, or reinterpret Object Identity.

A WF-0002-conformant workflow SHALL preserve metadata boundaries.

Metadata may support review and approval.

Metadata MUST NOT become approval, authority, privacy clearance, validation success, lifecycle transition, publication permission, export permission, migration permission, or downstream-use permission unless a governed standard, specification, or workflow explicitly defines that behavior within a controlled scope.

A WF-0002-conformant workflow SHALL preserve relationship boundaries.

Proposed, inferred, agent-generated, workflow-generated, imported, migrated, implementation-derived, reviewed, approved, rejected, deprecated, superseded, archived, or repaired relationships SHOULD remain distinguishable where relationship status affects interpretation, authority, privacy, validation, compatibility, publication, export, migration, or downstream use.

A WF-0002-conformant workflow SHALL preserve Source Reference and provenance boundaries.

Source References and provenance may support review and approval.

Source References and provenance MUST NOT create approval, Authority Level, Privacy Classification, publication permission, export permission, migration permission, synchronization permission, indexing permission, agent permission, implementation permission, or downstream-use permission by themselves.

A WF-0002-conformant workflow SHALL preserve Lifecycle State boundaries.

Lifecycle State may be reviewed, repaired, approved, rejected, superseded, deprecated, archived, quarantined, or transitioned through a governed workflow.

Lifecycle State MUST remain distinguishable from workflow state, validation state, authority level, privacy classification, agent state, implementation state, storage placement, and user-interface display.

A WF-0002-conformant workflow SHALL preserve Authority Level boundaries.

Approval may support authority assignment.

Approval MUST NOT automatically create broad Authority Level unless the approval decision and authority assignment explicitly define that effect within a governed scope.

A WF-0002-conformant workflow SHALL preserve Privacy Classification boundaries.

Privacy Classification SHALL take precedence over convenience, automation, review speed, publication, export, migration, synchronization, indexing, backup, agent access, implementation access, and downstream use where privacy risk exists.

Approval MUST NOT weaken Privacy Classification.

A WF-0002-conformant workflow SHALL preserve Validation boundaries.

Validation may support review and approval.

Validation MUST NOT be treated as approval, rejection, authority, privacy clearance, publication readiness, export readiness, migration readiness, synchronization readiness, indexing readiness, implementation permission, agent permission, workflow permission, or downstream-use permission unless a future governed workflow or specification explicitly defines that behavior within a controlled scope.

A WF-0002-conformant workflow SHALL preserve Human Review boundaries.

Human Review MUST remain distinguishable from agent participation, workflow routing, validation output, implementation visibility, storage placement, publication status, export success, migration success, synchronization, indexing, backup, and workflow completion.

Where Human Review is required, an agent MUST NOT silently replace it.

A WF-0002-conformant workflow SHALL preserve agent boundaries.

Agents MAY assist review and approval only within authorized access, privacy, workflow, storage, source, validation, implementation, and task scope.

Agents MUST NOT silently approve, reject, declassify, publish, export, migrate, delete, overwrite, supersede, deprecate, archive, validate as authoritative, assign final authority, govern privacy, redefine Object Identity, or clear governed entities for downstream use without governed review where review is required.

A WF-0002-conformant workflow SHALL preserve storage boundaries.

Storage routing, folder placement, filenames, paths, vault areas, review queues, archive locations, backup locations, synchronization targets, index locations, cache locations, implementation locations, import locations, export locations, and migration locations MUST NOT become governed meaning, approval, rejection, lifecycle state, Authority Level, Privacy Classification, Validation State, publication readiness, export readiness, migration readiness, or downstream-use readiness by themselves.

A WF-0002-conformant workflow SHALL preserve implementation independence.

A workflow MUST NOT require Obsidian, Codex, a specific model, a specific agent runtime, a specific database, a specific file system, a specific plugin, a specific interface, a specific validation tool, a specific automation tool, or a specific implementation unless a future governed implementation profile explicitly defines that requirement within its proper scope.

A WF-0002-conformant workflow SHOULD support or preserve:

- review intake;
- Review Candidate registration;
- Review Scope definition;
- Approval Scope definition;
- validation review;
- Source Reference review;
- provenance review;
- metadata review;
- relationship review;
- lifecycle review;
- authority review;
- privacy review;
- Human Review;
- Agent-Assisted Review;
- approval decisions;
- rejection decisions;
- deferral decisions;
- revision;
- repair;
- escalation;
- quarantine;
- supersession;
- deprecation;
- archival;
- historical preservation;
- Publication Readiness review;
- Export Readiness review;
- Migration Readiness review;
- Downstream-Use Readiness review;
- workflow logging;
- auditability;
- traceability;
- privacy-respecting preservation;
- implementation-independent interpretation.

A workflow that cannot preserve these conformance requirements SHOULD NOT claim conformance to WF-0002 without an explicit exception, limitation, or future governed specification defining a narrower compliant scope.

Workflow Conformance Requirements are successful when review and approval workflows can be evaluated consistently without allowing informal practice, automation, storage layout, implementation behavior, validation tooling, agent output, or repeated convenience to redefine governed review and approval behavior.

## 16. Non-Conformance, Exceptions, and Recovery

Non-Conformance, Exceptions, and Recovery define how review and approval workflows handle failures, limitations, deviations, and recovery actions without allowing drift to become normal practice.

Non-conformance occurs when a review and approval workflow fails to preserve the requirements, boundaries, distinctions, traceability, privacy expectations, validation expectations, authority expectations, lifecycle expectations, storage expectations, agent boundaries, implementation independence, or downstream-use limits defined by WF-0002.

Non-conformance MAY occur when:

- review is confused with approval;
- validation is confused with approval;
- approval is generalized beyond its Approval Scope;
- authority is assigned without governed review where review is required;
- Privacy Classification is weakened for convenience;
- lifecycle state is changed without traceability where traceability is required;
- Source References are omitted where source support is required;
- provenance is lost where provenance is required;
- metadata is treated as approval without governed definition;
- relationships are treated as approved without governed relationship review;
- workflow completion is treated as approval without governed definition;
- agent confidence is treated as approval, authority, validation, privacy clearance, or truth;
- storage placement is treated as lifecycle state, approval, authority, privacy classification, validation, publication readiness, export readiness, migration readiness, or downstream-use readiness;
- implementation visibility is treated as governed approval;
- publication, export, migration, synchronization, indexing, backup, or downstream use occurs outside approved scope;
- restricted material is exposed outside permitted privacy boundaries;
- review logs are missing where auditability is required;
- historical context is erased where preservation is required;
- conformance is claimed for a workflow that does not preserve required WF-0002 behavior.

A non-conforming workflow MUST NOT claim full WF-0002 conformance unless the non-conformance is corrected, limited, documented as an exception, or resolved through a future governed specification.

A narrow, partial, experimental, implementation-specific, manual, automated, agent-assisted, import-specific, export-specific, migration-specific, publication-specific, or downstream-use-specific workflow MAY claim limited conformance only when the claim clearly identifies its scope and limitations.

A limited conformance claim MUST NOT be treated as full WF-0002 conformance.

An exception is a governed allowance for behavior that does not fully satisfy normal WF-0002 expectations but is permitted within a defined scope for a defined reason.

An exception SHOULD identify or support identification of:

- what requirement is being excepted;
- why the exception is needed;
- what entity, workflow, implementation, agent, storage area, publication process, export process, migration process, or downstream-use context is affected;
- what scope applies;
- what risk exists;
- what privacy restrictions apply;
- what authority restrictions apply;
- what validation restrictions apply;
- what lifecycle restrictions apply;
- what review restrictions apply;
- what compensating controls apply;
- who or what approved the exception where applicable;
- when the exception was approved where applicable;
- whether the exception is temporary, permanent, experimental, deprecated, historical, emergency-only, implementation-specific, or migration-specific;
- when the exception should be reviewed again where applicable.

Exceptions MUST remain explicit.

Exceptions MUST remain scoped.

Exceptions MUST remain traceable.

Exceptions MUST NOT silently weaken Privacy Classification.

Exceptions MUST NOT silently create broad Authority Level.

Exceptions MUST NOT silently create approval, publication permission, export permission, migration permission, synchronization permission, indexing permission, agent permission, implementation permission, or downstream-use permission.

Exceptions MUST NOT redefine WF-0002 unless a future governed standard or approved revision changes the standard itself.

A recovery action is a governed action used to restore compliance, traceability, reviewability, privacy protection, validation integrity, authority clarity, lifecycle clarity, source traceability, provenance preservation, relationship clarity, storage boundary integrity, agent boundary integrity, implementation independence, or downstream-use safety after non-conformance is found.

Recovery MAY include:

- clarifying Review Scope;
- clarifying Approval Scope;
- restoring missing provenance;
- restoring missing Source References;
- correcting metadata;
- repairing relationships;
- correcting lifecycle state;
- correcting Authority Level;
- correcting Privacy Classification;
- rerunning validation;
- limiting approval;
- withdrawing approval;
- rejecting a candidate;
- quarantining material;
- archiving material;
- superseding a record;
- deprecating a record;
- restoring historical context;
- restricting publication;
- restricting export;
- restricting migration;
- restricting synchronization;
- restricting indexing;
- restricting agent access;
- restricting implementation access;
- restricting downstream use;
- escalating to human review;
- escalating to governance review;
- documenting an exception;
- revising a workflow;
- revising an implementation profile;
- creating a future specification.

A Recovery Decision SHOULD identify or support identification of:

- what non-conformance occurred;
- what entity or workflow was affected;
- what risk was created;
- what corrective action was taken;
- who or what performed recovery where applicable;
- when recovery occurred where applicable;
- what evidence supports recovery;
- what review occurred;
- what validation occurred;
- what privacy review occurred;
- what authority review occurred;
- what lifecycle review occurred;
- what Source References or provenance were restored;
- what restrictions remain;
- whether future review is required.

Recovery MUST preserve privacy boundaries.

Recovery MUST preserve historical traceability where historical traceability is required.

Recovery MUST NOT erase evidence of non-conformance where preservation is required for auditability, governance, privacy, compatibility, migration, legal sensitivity, source traceability, or downstream interpretation.

Emergency handling MAY be permitted where immediate containment is required to protect privacy, prevent exposure, prevent destructive action, stop unsafe publication, stop unsafe export, stop unsafe migration, stop unsafe synchronization, stop unsafe indexing, stop unsafe agent use, stop unsafe implementation exposure, or prevent downstream harm.

Emergency handling SHOULD be followed by review, logging, repair, escalation, or governance review where required.

Non-Conformance, Exceptions, and Recovery are successful when deviations are contained, documented, corrected, limited, or escalated without allowing convenience, automation, implementation behavior, storage layout, validation tooling, agent output, or undocumented practice to become the standard.

## 17. Success Criteria

WF-0002 is successful when review and approval workflows preserve governed meaning, reviewability, traceability, privacy, validation boundaries, authority boundaries, lifecycle boundaries, storage boundaries, agent boundaries, implementation independence, and downstream-use safety.

A successful WF-0002 workflow allows future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, synchronization processes, indexing systems, backup processes, restoration processes, implementations, and governance processes to determine:

- what entity entered review;
- why review was required;
- what Review Scope applied;
- what Approval Scope applied;
- what Source References were considered;
- what provenance was considered;
- what metadata was considered;
- what relationships were considered;
- what lifecycle state was considered;
- what Authority Level was considered;
- what Privacy Classification was considered;
- what Validation State or validation result was considered;
- what human review occurred;
- what agent assistance occurred;
- what decision was made;
- what approval, rejection, deferral, repair, escalation, quarantine, archival, supersession, deprecation, publication, export, migration, or downstream-use decision occurred;
- what restrictions, limits, warnings, conditions, or future review requirements apply;
- whether the decision remains valid across storage changes, workflow changes, agent changes, implementation changes, import, export, migration, backup, restoration, synchronization, indexing, publication, and downstream use.

WF-0002 is successful when review and approval remain distinguishable from:

- validation;
- authority;
- privacy clearance;
- lifecycle state;
- workflow state;
- workflow completion;
- agent confidence;
- human visibility;
- implementation visibility;
- storage placement;
- metadata values;
- relationship suggestions;
- Source Reference existence;
- provenance existence;
- indexing;
- synchronization;
- backup;
- publication;
- export;
- migration;
- downstream-use activity.

WF-0002 is successful when Approval Scope remains explicit and approval is not silently generalized beyond its defined use.

WF-0002 is successful when Privacy Classification remains enforceable before, during, and after review.

WF-0002 is successful when Authority Level remains scoped and is not created by approval unless the approval decision and authority assignment explicitly define that effect.

WF-0002 is successful when Validation supports review without replacing review.

WF-0002 is successful when Source References and provenance remain available enough to support review, auditability, migration, compatibility, governance, and downstream interpretation where those concerns apply.

WF-0002 is successful when metadata and relationships remain explicit, traceable, reviewable, and distinguishable from implementation-specific signals.

WF-0002 is successful when lifecycle transitions remain explicit, traceable, reviewable, and distinguishable from workflow state, validation state, authority level, privacy classification, storage placement, agent state, implementation state, and user-interface display.

WF-0002 is successful when agents assist review without silently becoming reviewers, approvers, validators, authorities, privacy governors, publication governors, export governors, migration governors, or downstream-use governors.

WF-0002 is successful when storage supports review, routing, preservation, archival, quarantine, import, export, migration, backup, restoration, synchronization, indexing, and implementation access without defining governed meaning by itself.

WF-0002 is successful when implementations can realize review and approval workflows without becoming the standard itself.

WF-0002 is successful when non-conformance, exceptions, and recovery remain governed, scoped, traceable, privacy-respecting, validation-aware, authority-aware, lifecycle-aware, and implementation-independent.

WF-0002 is successful when routine daily review remains practical enough to use while preserving the integrity needed for long-term knowledge survival.

A WF-0002 workflow SHOULD be considered successful only when it reduces drift, preserves trust, protects restricted material, supports human reviewability, enables agent assistance safely, supports future automation, and keeps knowledge usable across time, tools, storage systems, workflows, agents, validators, implementations, import, export, migration, backup, restoration, synchronization, indexing, publication, and downstream use.

## 18. Closing Rule

Review and approval are governed acts.

A governed entity is not approved merely because it exists.

A governed entity is not approved merely because it was created.

A governed entity is not approved merely because it was captured.

A governed entity is not approved merely because it was ingested.

A governed entity is not approved merely because it was stored.

A governed entity is not approved merely because it was indexed.

A governed entity is not approved merely because it was synchronized.

A governed entity is not approved merely because it was backed up.

A governed entity is not approved merely because it was restored.

A governed entity is not approved merely because it was published.

A governed entity is not approved merely because it was exported.

A governed entity is not approved merely because it was migrated.

A governed entity is not approved merely because it was validated.

A governed entity is not approved merely because it was reviewed by an agent.

A governed entity is not approved merely because an agent recommended it.

A governed entity is not approved merely because a workflow completed.

A governed entity is not approved merely because a storage system routed it.

A governed entity is not approved merely because an implementation displayed it.

A governed entity is not approved merely because a human can see it.

A governed entity is not approved merely because it has metadata.

A governed entity is not approved merely because it has relationships.

A governed entity is not approved merely because it has Source References.

A governed entity is not approved merely because it has provenance.

A governed entity is not approved merely because it has a lifecycle state.

A governed entity is not approved merely because it has an Authority Level.

A governed entity is not approved merely because it has a Privacy Classification.

Approval must be explicit where approval affects governed meaning or use.

Approval must be scoped where scope affects interpretation, authority, privacy, validation, publication, export, migration, synchronization, indexing, backup, restoration, agent use, implementation use, or downstream use.

Review and approval workflows MUST preserve Object Identity, metadata role boundaries, relationship meaning, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage boundaries, agent boundaries, implementation independence, workflow traceability, auditability, and human reviewability.

Review and approval workflows MUST preserve privacy boundaries even when review, validation, automation, publication, export, migration, synchronization, indexing, backup, restoration, agent use, implementation use, or downstream use would be easier without them.

Review and approval workflows MUST preserve the distinction between governed decision and operational convenience.

If review and approval behavior becomes ambiguous, the ambiguity SHOULD be resolved in favor of explicit scope, preserved provenance, privacy protection, validation clarity, authority clarity, lifecycle clarity, source traceability, relationship clarity, human reviewability, implementation independence, and governed decision-making.

WF-0002 closes with this rule:

No governed entity becomes approved, authoritative, public, exportable, migratable, synchronized, indexed, agent-usable, implementation-usable, or ready for downstream use unless the applicable governed review and approval workflow explicitly permits that outcome within a defined scope.
