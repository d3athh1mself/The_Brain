# DEP-0001 — Bare Usable Deployment Readiness Standard

Document ID: DEP-0001
Title: Bare Usable Deployment Readiness Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 5 — Deployment Readiness
Milestone: 5.1 — Bare Usable Deployment Readiness Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; AG-0002 — Agent Role and Responsibility Standard; AG-0003 — Agent Permission and Traceability Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; WF-0003 — Knowledge Maintenance and Update Workflow Standard; WF-0004 — Publication, Export, and Downstream Use Workflow Standard
Supersedes: None
Superseded By: None
Related: IMP-0001 — Obsidian and Codex Implementation Profile

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and deployment-readiness rules are interpreted within DEP-0001.

Where conflicts arise between deployment readiness, file completeness, folder readiness, metadata readiness, workflow readiness, agent readiness, validation readiness, review readiness, export readiness, backup readiness, implementation readiness, copying behavior, installation behavior, reusable package behavior, handoff behavior, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, agent behavior, workflow behavior, implementation behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

DEP-0001 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

DEP-0001 depends on the Phase 1 Knowledge Standards because deployment readiness must preserve knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation without redefining those concepts.

DEP-0001 depends on the Phase 2 Storage Standards because deployment readiness requires a storage environment, folder layout, governed document placement, source material handling, archive handling, import handling, export handling, backup handling, and implementation-support placement that preserve storage meaning without defining knowledge meaning.

DEP-0001 depends on the Phase 3 Agent Standards because a deployable Brain package must define the agent roles, boundaries, permissions, traceability expectations, review requirements, and escalation behavior required before agents or subagents may safely operate on governed material.

DEP-0001 depends on the Phase 4 Workflow Standards because a deployable Brain package must support ingestion, review and approval, maintenance and update, publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, and downstream-use behavior without creating architectural drift.

DEP-0001 defines deployment-readiness behavior at the standard level.

DEP-0001 does not define exact Obsidian settings, exact Codex prompts, exact model behavior, exact plugin behavior, exact scripts, exact validator code, exact folder paths beyond readiness expectations, exact automation setup, exact synchronization tooling, exact backup tooling, exact export formats, or exact tool-specific implementation behavior.

Those concerns belong to implementation profiles, deployment guides, operational checklists, templates, validators, scripts, reference implementations, tool-specific setup files, and future implementation documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Deployment Readiness refers to the governed determination that a Brain package contains the minimum required standards, storage structure, metadata expectations, workflow boundaries, agent boundaries, validation expectations, review expectations, and handoff context needed for safe practical use.
- Bare Usable Deployment refers to the minimum usable version of The Brain that can be copied, installed, reused, or handed to another machine or person without requiring the entire mature standard to be complete.
- Deployment Package refers to the set of files, folders, standards, specifications, implementation-support files, templates, prompts, validators, documentation, source areas, archive areas, and operational instructions prepared for use in another environment.
- Minimum File Set refers to the required files that MUST exist before a deployment package may be treated as bare usable.
- Required File refers to a file that MUST exist for the deployment package to satisfy DEP-0001.
- Recommended File refers to a file that SHOULD exist because it improves safety, usability, automation reliability, reviewability, or long-term maintainability.
- Optional File refers to a file that MAY exist but is not required for bare usable deployment unless a future standard, specification, implementation profile, or operational guide makes it required within a narrower scope.
- Folder Readiness refers to whether the storage layout contains the minimum required areas for governed documents, Knowledge Records, Source Material, drafts, review files, archives, imports, exports, backups, implementation support, agent support, workflow support, and generated files.
- Metadata Readiness refers to whether governed files contain or support enough metadata to preserve identity, title, status, authority, dependencies, related documents, lifecycle state, privacy classification, validation state, provenance, and reviewability where required.
- Workflow Readiness refers to whether the deployment package contains enough workflow standards and instructions for ingestion, review, maintenance, publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, and downstream use to occur safely.
- Agent Readiness refers to whether the deployment package contains enough agent standards, role definitions, permission boundaries, traceability requirements, and escalation rules for agents or subagents to assist without becoming unreviewable authorities.
- Validation Readiness refers to whether the deployment package contains enough standards, expectations, and review paths to determine whether files, metadata, relationships, workflows, agents, storage layout, and deployment actions conform to the standard.
- Review Readiness refers to whether a human or governed workflow can inspect, approve, reject, repair, defer, or escalate deployment materials before they are used.
- Handoff Readiness refers to whether a future human, agent, Codex-style workflow, Obsidian-style vault, repository, or local machine can continue using the package without losing context, misreading authority, or creating drift.
- Implementation Profile refers to a document that explains how a specific tool, vault, workflow environment, agent system, or software stack realizes The Brain Standard without becoming the standard itself.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Validation refers to the process of checking whether a governed entity satisfies applicable standards, specifications, metadata expectations, provenance expectations, relationship expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, workflow expectations, agent expectations, implementation expectations, import expectations, export expectations, migration expectations, publication expectations, synchronization expectations, indexing expectations, backup expectations, or downstream-use expectations.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of DEP-0001 is to define the minimum deployment-readiness requirements for a bare usable Brain package.

DEP-0001 exists to answer when The Brain can be safely copied, installed, reused, handed to another machine, handed to another person, connected to an implementation, or used by agents without requiring the entire mature standard to be complete.

The Brain is intended to remain implementation-independent, portable, human-readable, AI-readable, governed, and usable across tools.

Deployment readiness exists so that practical use can begin without allowing convenience, incomplete setup, missing folders, missing standards, missing metadata, missing workflows, missing agent boundaries, missing validation expectations, or tool-specific assumptions to redefine the architecture.

DEP-0001 defines what MUST be present before The Brain may be treated as bare usable.

Bare usable does not mean complete.

Bare usable means the deployment package contains enough governed structure to support safe initial use, controlled expansion, human review, agent assistance, source preservation, Knowledge Record creation, storage organization, workflow routing, validation, backup, export, and future implementation work without creating uncontrolled drift.

DEP-0001 is responsible for defining deployment-readiness behavior for:

- minimum required standards;
- required folder readiness;
- governed document readiness;
- Knowledge Record readiness;
- Source Material readiness;
- metadata readiness;
- relationship readiness;
- source-reference and provenance readiness;
- lifecycle readiness;
- authority readiness;
- privacy readiness;
- validation readiness;
- storage readiness;
- agent readiness;
- workflow readiness;
- review readiness;
- export readiness;
- backup readiness;
- implementation-profile readiness;
- handoff readiness;
- copy and reuse readiness;
- deployment non-conformance;
- deployment success criteria.

DEP-0001 does not replace the Knowledge Standards, Storage Standards, Agent Standards, or Workflow Standards.

DEP-0001 does not define the final mature implementation of The Brain.

DEP-0001 does not define a complete Obsidian setup.

DEP-0001 does not define a complete Codex setup.

DEP-0001 does not define exact templates, prompts, scripts, validators, plugins, automation, dashboards, graph views, sync tools, backup tools, or export formats.

Those concerns belong to future implementation profiles, operational guides, templates, validators, deployment packages, and reference implementations.

DEP-0001 defines the readiness boundary before those implementation-specific documents may safely depend on the current standard set.

The primary purpose of DEP-0001 is to prevent premature deployment.

Premature deployment occurs when The Brain is copied, installed, reused, automated, exposed to agents, used inside an implementation, or handed to another environment before the minimum required standards, folder areas, metadata expectations, workflow boundaries, agent boundaries, validation expectations, review expectations, and handoff context are present.

DEP-0001 is successful when a future human, agent, Codex-style workflow, Obsidian-style vault, local machine, repository, or implementation profile can determine:

- whether the package is ready for bare usable deployment;
- what files must exist;
- what files may remain draft;
- what files must be approved;
- what folders must exist;
- what metadata expectations must be present;
- what workflows are usable;
- what agents may safely do;
- what validation expectations apply;
- what review is still required;
- what export, backup, copy, or handoff limits remain;
- what future implementation profile should follow.

## 2. Relationship to Prior Standards

DEP-0001 is subordinate to and derived from the constitutional foundation of The Brain Standard.

DEP-0001 depends on:

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
- AG-0002 — Agent Role and Responsibility Standard;
- AG-0003 — Agent Permission and Traceability Standard;
- WF-0001 — Knowledge Ingestion Workflow Standard;
- WF-0002 — Review and Approval Workflow Standard;
- WF-0003 — Knowledge Maintenance and Update Workflow Standard;
- WF-0004 — Publication, Export, and Downstream Use Workflow Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

DEP-0001 applies that purpose by defining the minimum package needed for practical use without making any specific implementation, tool, vault, repository, prompt, script, plugin, or agent runtime the source of truth.

TB-0001 establishes the architecture principles that govern The Brain Standard.

DEP-0001 applies those principles by requiring deployment readiness to preserve:

- knowledge integrity;
- implementation independence;
- portability;
- durability;
- human usability;
- AI usability;
- explicit structure;
- governed evolution;
- practical daily usability.

TB-0002 establishes the layered architecture of The Brain Standard.

DEP-0001 is a cross-layer deployment-readiness standard.

DEP-0001 does not create a new knowledge layer.

DEP-0001 does not redefine Layer 1, Layer 2, Layer 3, Layer 4, or Layer 5.

DEP-0001 checks whether enough of those layers are present and usable for bare deployment.

Layer 1 Knowledge Standards define meaning.

Layer 2 Storage Standards define storage organization.

Layer 3 Agent Standards define agent boundaries, roles, permissions, and traceability.

Layer 4 Workflow Standards define governed processes.

Layer 5 Implementation Profiles define how specific tools realize the standard.

DEP-0001 sits between workflow completion and implementation profiling.

DEP-0001 answers whether the current standard package is ready to be copied, installed, reused, handed off, or implemented.

TB-0003 establishes the governance model for The Brain Standard.

DEP-0001 follows the document authority hierarchy defined by TB-0003.

DEP-0001 MUST NOT approve, supersede, deprecate, reject, or revise prior standards by implication.

DEP-0001 MAY identify whether prior standards are required for deployment readiness.

DEP-0001 MAY identify whether a prior standard must be Approved, Draft, Review, or otherwise governed before deployment.

DEP-0001 MAY define deployment-readiness checks that depend on prior standards.

DEP-0001 MUST NOT redefine the content or authority of those prior standards.

The Phase 1 Knowledge Standards define the meaning of knowledge.

DEP-0001 depends on those standards because a deployment package is not usable unless knowledge objects, identity, metadata, relationships, Source References, provenance, lifecycle state, authority level, privacy classification, and validation expectations are present or supported.

The Phase 2 Storage Standards define how governed material may be stored without allowing storage placement to define meaning.

DEP-0001 depends on those standards because a deployment package is not usable unless source areas, record areas, governed document areas, draft areas, review areas, archive areas, import areas, export areas, backup areas, implementation-support areas, agent-support areas, workflow-support areas, and generated-file areas are understandable and safe.

The Phase 3 Agent Standards define how agents may operate.

DEP-0001 depends on those standards because a deployment package is not safe for AI-assisted use unless agent roles, agent permissions, agent traceability, escalation behavior, review requirements, and prohibited actions are explicit.

The Phase 4 Workflow Standards define repeatable governed processes.

DEP-0001 depends on those standards because a deployment package is not usable unless it can ingest, review, approve, maintain, update, publish, export, migrate, synchronize, index, back up, recover, expose, and route knowledge through governed workflows.

DEP-0001 prepares for implementation profiles.

An implementation profile MAY define exact Obsidian behavior, Codex behavior, local folder behavior, prompts, scripts, templates, validators, dashboards, indexes, or tool-specific operations only after DEP-0001 establishes that the deployment package is ready enough to support practical implementation without architectural drift.

DEP-0001 is successful when it connects the completed standards foundation to practical deployment without redefining knowledge meaning, storage meaning, agent authority, workflow authority, validation meaning, privacy classification, authority level, lifecycle state, Source References, provenance, relationships, or implementation independence.

## 3. Deployment Scope and Boundaries

DEP-0001 applies to the readiness of a bare usable Brain deployment package.

A deployment package MAY include:

- governed standards;
- specifications;
- implementation profiles;
- operational guides;
- templates;
- prompts;
- validation files;
- scripts;
- folder structures;
- source-material areas;
- Knowledge Record areas;
- governed document areas;
- draft areas;
- review areas;
- archive areas;
- import areas;
- export areas;
- backup areas;
- migration areas;
- implementation-support areas;
- agent-support areas;
- workflow-support areas;
- generated-file areas;
- handoff summaries;
- logs;
- manifests;
- readme files;
- future supporting assets.

DEP-0001 defines whether the package is ready enough to be used.

DEP-0001 does not require the package to be mature, complete, fully automated, fully validated by scripts, fully implemented in Obsidian, fully integrated with Codex, or ready for public release.

Bare usable deployment is the minimum safe deployment state.

A bare usable deployment package SHALL contain enough standards, folder structure, metadata expectations, workflow instructions, agent boundaries, validation expectations, and handoff context for controlled use.

A bare usable deployment package SHOULD allow a user to:

- place new Source Material into the correct intake or source area;
- create or stage a Draft Knowledge Record;
- preserve Object Identity expectations;
- apply minimum metadata expectations;
- distinguish Source Material from Knowledge Records;
- preserve Source References and provenance where required;
- classify lifecycle state, authority level, privacy classification, and validation state where required;
- route material through ingestion;
- route material through review and approval;
- maintain and update governed knowledge;
- determine whether publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, or downstream use is allowed;
- identify what agents may assist with;
- identify what agents must not do;
- identify when human review is required;
- identify when validation, repair, quarantine, escalation, archive, export, or backup is required.

DEP-0001 SHALL preserve the distinction between deployment readiness and implementation readiness.

Deployment readiness answers whether the package has enough governed structure to be safely copied, installed, reused, or handed off.

Implementation readiness answers whether a specific tool, vault, runtime, agent system, plugin stack, script set, or interface is configured to realize the standard in practice.

A deployment package MAY be deployment-ready before any specific implementation profile is complete.

A deployment package MUST NOT be treated as fully implementation-ready merely because it is deployment-ready.

DEP-0001 SHALL preserve the distinction between deployment readiness and public release readiness.

Bare usable deployment MAY be appropriate for personal use, controlled local use, test use, internal handoff, or implementation-profile development.

Bare usable deployment does not automatically authorize public distribution, organization-wide rollout, unrestricted sharing, publication, export, migration, synchronization, indexing, agent exposure, or downstream use.

Those actions remain governed by the applicable standards and workflows.

DEP-0001 SHALL preserve the distinction between file existence and file readiness.

A file is not deployment-ready merely because it exists.

A file SHOULD be inspected for:

- correct document ID;
- correct title;
- correct status;
- correct authority;
- correct phase;
- correct milestone;
- correct dependencies;
- correct related files;
- correct heading structure;
- correct section sequence;
- syntax correctness;
- grammar and spelling;
- redundancy risk;
- conflict with higher-authority standards;
- implementation-specific leakage;
- missing handoff context where required.

DEP-0001 SHALL preserve the distinction between folder existence and folder readiness.

A folder is not deployment-ready merely because it exists.

A folder SHOULD have a clear purpose, appropriate placement, safe use boundary, and compatibility with SS-0001 and SS-0002.

DEP-0001 SHALL preserve the distinction between agent availability and agent readiness.

An agent is not deployment-ready merely because a prompt, role name, tool, model, or automation exists.

Agent readiness requires explicit role, permission, traceability, escalation, review, and boundary expectations.

DEP-0001 SHALL preserve the distinction between workflow existence and workflow readiness.

A workflow is not deployment-ready merely because a workflow standard exists.

Workflow readiness requires that the workflow can be followed, reviewed, validated, logged where required, and connected to the relevant standards without redefining their meaning.

DEP-0001 SHALL preserve the distinction between validation possibility and validation readiness.

A deployment package is not validation-ready merely because a human or agent can inspect it.

Validation readiness requires enough rules, expectations, metadata, structure, and review pathways to determine whether the package satisfies the applicable standards.

DEP-0001 SHALL preserve the distinction between backup existence and recovery readiness.

A backup is not recovery-ready merely because a copy exists.

Recovery readiness requires enough context to restore, inspect, validate, repair, quarantine, or escalate recovered material without losing governed meaning, privacy, authority, lifecycle state, validation state, provenance, relationships, source traceability, or compatibility.

DEP-0001 is successful when the deployment boundary is clear enough that future humans, agents, validators, implementations, repositories, vaults, and downstream users can determine what is ready, what is incomplete, what remains draft-only, what requires approval, what may be copied, what may be used, what must be reviewed, and what must not be treated as implementation authority.

## 4. Minimum Deployment File Set

The Minimum Deployment File Set defines which governed files MUST exist before a Brain package may be treated as bare usable.

A bare usable deployment package SHALL include enough governed files to preserve the constitutional foundation, Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, deployment-readiness expectations, and handoff context needed for controlled use.

A file MUST NOT be treated as deployment-ready merely because it exists.

A required file SHOULD be inspected for:

- correct document ID;
- correct title;
- correct version;
- correct status;
- correct creation date;
- correct last-updated date;
- correct authority level;
- correct phase;
- correct milestone;
- correct dependency list;
- correct related-file references where applicable;
- correct Markdown heading structure;
- correct section sequence;
- absence of blocking syntax issues;
- absence of unresolved drift against higher-authority standards;
- compatibility with the deployment package scope.

A bare usable deployment package SHALL include the constitutional foundation:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model.

The constitutional foundation SHOULD be Approved before deployment beyond controlled personal or local use.

A bare usable deployment package SHALL include the Knowledge Standards required to preserve knowledge meaning:

- KS-0001 — Knowledge Object Model;
- KS-0002 — Object Identity Standard;
- KS-0003 — Metadata Standard;
- KS-0004 — Relationship Standard;
- KS-0005 — Source Reference and Provenance Standard;
- KS-0006 — Lifecycle State Standard;
- KS-0007 — Authority Level Standard;
- KS-0008 — Privacy Classification Standard;
- KS-0009 — Validation Standard.

The Knowledge Standards SHOULD be Approved before a deployment package is handed to another person, machine, repository, or implementation for regular use.

A bare usable deployment package SHALL include the Storage Standards required to preserve storage organization without allowing storage placement to define knowledge meaning:

- SS-0001 — Storage Architecture Standard;
- SS-0002 — Storage Layout Specification.

The Storage Standards SHOULD be sufficiently complete to identify the minimum required storage areas, draft areas, review areas, source areas, archive areas, import areas, export areas, backup areas, implementation-support areas, agent-support areas, workflow-support areas, and generated-file areas.

A bare usable deployment package SHALL include the Agent Standards required to prevent agent authority creep:

- AG-0001 — Agent Operating Boundaries Standard;
- AG-0002 — Agent Role and Responsibility Standard;
- AG-0003 — Agent Permission and Traceability Standard.

The Agent Standards SHOULD be Approved before agents or subagents are allowed to modify, move, create, delete, publish, export, migrate, synchronize, index, back up, or expose governed material.

A bare usable deployment package SHALL include the Workflow Standards required to support governed use:

- WF-0001 — Knowledge Ingestion Workflow Standard;
- WF-0002 — Review and Approval Workflow Standard;
- WF-0003 — Knowledge Maintenance and Update Workflow Standard;
- WF-0004 — Publication, Export, and Downstream Use Workflow Standard.

The Workflow Standards SHOULD be sufficiently complete to allow a future human, agent, validator, implementation, or repository process to determine how material enters, moves through, changes within, exits, or is exposed from the system.

A bare usable deployment package SHALL include DEP-0001.

DEP-0001 defines whether the package itself is ready for bare usable deployment.

A bare usable deployment package SHOULD include a deployment manifest.

A deployment manifest SHOULD identify:

- what files are included;
- what files are required;
- what files are recommended;
- what files are optional;
- what files are missing;
- what files remain Draft;
- what files are Approved;
- what folders are present;
- what folders are missing;
- what implementation profiles are included;
- what implementation profiles are not yet created;
- what agent files are included;
- what workflow files are included;
- what validation files are included;
- what handoff summaries are included;
- what known limitations remain.

A bare usable deployment package SHOULD include a current handoff summary.

A handoff summary SHOULD identify:

- what has been completed;
- what remains incomplete;
- what standards are approved;
- what standards remain draft;
- what deployment risks remain;
- what implementation work should happen next;
- what assumptions were made;
- what unresolved questions remain;
- what files should be created next;
- what files should not be redefined.

A bare usable deployment package MAY include implementation profiles.

Implementation profiles are not required for standard-level deployment readiness unless the deployment package is being handed off for immediate use in a specific tool, vault, agent runtime, repository workflow, or software environment.

A bare usable deployment package SHOULD NOT require IMP-0001 before DEP-0001 is complete.

IMP-0001 SHOULD follow DEP-0001.

DEP-0001 defines whether the package is ready for implementation profiling.

IMP-0001 defines how a specific Obsidian and Codex implementation realizes the standard.

A deployment package MAY include Draft files.

Draft files MUST remain clearly marked as Draft.

Draft files MUST NOT be treated as Approved merely because they are included in a deployment package.

A deployment package MAY include planned files, placeholders, or roadmap entries.

Planned files, placeholders, and roadmap entries MUST NOT be treated as existing governed standards.

A missing required file SHALL block bare usable deployment unless the deployment scope is explicitly limited, logged, and reviewed.

A missing recommended file SHOULD be recorded as a deployment limitation.

A missing optional file MAY be recorded where it affects implementation planning, future automation, or handoff clarity.

The Minimum Deployment File Set is successful when future humans, agents, validators, repositories, implementation profiles, and downstream users can determine what files must exist, what files do exist, what files are missing, what files remain draft, what files are approved, and whether the package is ready for controlled bare usable deployment.

## 5. Required Folder and Layout Readiness

Required Folder and Layout Readiness define the minimum storage-layout expectations that MUST be satisfied before a Brain package may be treated as bare usable.

DEP-0001 does not define exact folder paths.

DEP-0001 does not define exact folder names where those names are implementation-specific.

DEP-0001 defines whether the storage layout contains enough understandable storage areas to support controlled deployment.

A bare usable deployment package SHALL include or support a root storage environment.

The root storage environment SHOULD make clear where the deployment package begins and what material belongs inside the governed package.

A bare usable deployment package SHALL include or support a governed document area.

The governed document area SHOULD contain standards, specifications, implementation profiles, operational documents, ADRs, RFCs, deployment documents, handoff summaries, manifests, and other governed project files.

A bare usable deployment package SHALL include or support a Source Material area.

The Source Material area SHOULD allow original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other source artifacts to be stored, staged, referenced, or archived without being confused with Knowledge Records.

A bare usable deployment package SHALL include or support a Knowledge Record area.

The Knowledge Record area SHOULD allow structured Knowledge Records to be stored, reviewed, maintained, validated, related, and used without being confused with Source Material.

A bare usable deployment package SHALL include or support a draft area.

The draft area SHOULD allow incomplete, proposed, temporary, generated, or not-yet-approved material to remain separate from approved governed material.

A bare usable deployment package SHALL include or support a review area.

The review area SHOULD allow material awaiting human review, validation review, privacy review, source-reference review, provenance review, relationship review, authority review, lifecycle review, compatibility review, workflow review, or deployment review to be identified and handled.

A bare usable deployment package SHALL include or support an archive area.

The archive area SHOULD preserve historical, superseded, deprecated, rejected, inactive, migrated, or no-longer-current material without allowing archived material to be confused with active approved material.

A bare usable deployment package SHALL include or support an import area.

The import area SHOULD hold material entering the compliant environment before classification, validation, review, quarantine, rejection, archival, or placement.

A bare usable deployment package SHALL include or support an export area.

The export area SHOULD hold material prepared for transfer, publication, migration, sharing, review, backup, or downstream use only where export handling remains governed by the applicable standards and workflows.

A bare usable deployment package SHALL include or support a backup area or backup target.

The backup area or backup target SHOULD preserve material for restoration, continuity, archival, audit, migration, disaster recovery, or long-term retention.

A bare usable deployment package SHALL include or support a migration area where migration is expected.

The migration area SHOULD support movement between storage systems, schemas, repositories, vaults, implementations, file formats, standard versions, or future environments.

A bare usable deployment package SHOULD include or support an implementation-support area.

The implementation-support area MAY contain configuration files, scripts, templates, prompts, plugin notes, generated artifacts, local setup notes, or tool-support files.

Implementation-support files MUST NOT redefine the standard.

A bare usable deployment package SHOULD include or support an agent-support area.

The agent-support area MAY contain agent profiles, prompt drafts, permission profiles, role mappings, traceability notes, review outputs, validation outputs, or task-support material.

Agent-support files MUST remain subordinate to AG-0001, AG-0002, and AG-0003.

A bare usable deployment package SHOULD include or support a workflow-support area.

The workflow-support area MAY contain workflow checklists, routing notes, review logs, approval logs, maintenance logs, publication logs, export logs, migration logs, backup logs, recovery logs, or operational workflow aids.

Workflow-support files MUST remain subordinate to WF-0001, WF-0002, WF-0003, and WF-0004.

A bare usable deployment package MAY include or support an index or cache area.

Index or cache material MUST be treated as generated, derived, temporary, implementation-supporting, or validation-supporting unless a governed standard or specification explicitly defines otherwise.

An index, cache, embedding, search result, graph view, backlink, generated summary, or implementation artifact MUST NOT define Object Identity, metadata meaning, relationship meaning, lifecycle state, authority level, privacy classification, validation state, approval, publication clearance, export permission, migration permission, agent permission, or downstream-use permission by itself.

A folder is deployment-ready only when its purpose is clear enough for future humans, agents, validators, workflows, implementations, repositories, and downstream users to determine how it should be used.

Folder existence alone does not establish readiness.

Folder placement alone does not establish governed meaning.

Folder names alone do not establish authority, lifecycle state, privacy classification, validation state, source status, publication permission, export permission, migration permission, agent permission, or downstream-use permission.

A deployment package SHOULD include enough layout documentation, manifest information, README material, or handoff context for a future user to determine:

- where governed documents belong;
- where Source Material belongs;
- where Knowledge Records belong;
- where drafts belong;
- where review material belongs;
- where archives belong;
- where imports belong;
- where exports belong;
- where backups belong;
- where migration material belongs;
- where implementation-support files belong;
- where agent-support files belong;
- where workflow-support files belong;
- where generated files belong;
- which areas are authoritative;
- which areas are supporting;
- which areas are temporary;
- which areas are restricted;
- which areas require review before use.

Required Folder and Layout Readiness are successful when a Brain package can be copied, installed, reused, handed off, inspected, validated, backed up, restored, migrated, or implemented without allowing folder placement, file location, tool behavior, generated indexes, caches, or operational convenience to redefine governed meaning.

## 6. Metadata and Governed Document Readiness

Metadata and Governed Document Readiness define the minimum document and metadata expectations that MUST be satisfied before a Brain package may be treated as bare usable.

DEP-0001 does not define a complete metadata schema.

DEP-0001 does not define exact Markdown front matter syntax.

DEP-0001 does not define exact database columns, API fields, validator rules, schema files, or implementation-specific metadata formats.

DEP-0001 defines whether governed documents and deployment materials contain enough explicit metadata and document structure to support safe deployment.

A governed document included in a bare usable deployment package SHALL contain or support enough metadata to identify:

- what the document is;
- what document ID applies;
- what title applies;
- what version applies;
- what status applies;
- when the document was created;
- when the document was last updated;
- what authority level applies;
- what phase applies;
- what milestone applies;
- what dependencies apply;
- what the document supersedes where applicable;
- what supersedes the document where applicable;
- what related files exist where applicable.

A governed document SHOULD use the standard document metadata pattern already established across The Brain Standard unless a future governed specification defines a different representation.

A governed document MUST NOT rely only on filename, folder placement, UI display, repository location, plugin metadata, database state, hidden application state, agent memory, workflow memory, or undocumented convention for metadata that affects governed meaning.

A deployment package SHALL preserve document status.

A Draft document MUST remain identifiable as Draft.

A Review document MUST remain identifiable as Review where that status is used.

An Approved document MUST remain identifiable as Approved.

A Deprecated, Superseded, Rejected, Archived, Restricted, Quarantined, Pending Review, Pending Validation, or Needs Repair document MUST remain identifiable where that state affects interpretation, use, publication, export, migration, implementation exposure, agent exposure, or downstream use.

A deployment package SHALL preserve document authority.

A constitutional document MUST remain distinguishable from a standard.

A standard MUST remain distinguishable from a specification.

A specification MUST remain distinguishable from an implementation profile.

An implementation profile MUST remain distinguishable from an operational guide, template, script, prompt, validator, checklist, manifest, or generated artifact.

A deployment package SHALL preserve dependency information.

A governed document SHOULD identify the higher-authority documents, prior standards, supporting standards, workflows, agent standards, storage standards, implementation profiles, specifications, or operational documents it depends on.

A deployment package SHOULD preserve related-file information where related files affect interpretation, implementation planning, handoff, validation, maintenance, or downstream use.

A deployment package SHALL preserve Object Identity expectations.

Knowledge Objects and Knowledge Records MUST NOT receive identity from filename, folder placement, repository path, implementation identifier, plugin field, graph position, backlink behavior, search ranking, cache entry, or agent-generated label alone.

A deployment package SHALL preserve Source Material and Knowledge Record distinction.

Source Material MUST NOT become a Knowledge Record merely because it is stored, copied, indexed, summarized, embedded, linked, reviewed, exported, backed up, or processed by an agent.

A Knowledge Record MUST NOT lose its governed meaning merely because it is copied, exported, migrated, synchronized, backed up, restored, indexed, summarized, displayed differently, or processed by an implementation.

A deployment package SHOULD preserve relationship readiness.

Relationship metadata, relationship records, relationship references, backlinks, graph edges, cross-references, or related-file lists SHOULD remain explicit enough that future humans, agents, validators, workflows, implementations, and repositories can determine whether a relationship is governed, proposed, inferred, reviewed, approved, deprecated, superseded, rejected, archived, implementation-specific, or merely navigational.

A deployment package SHOULD preserve source-reference and provenance readiness.

Source References and provenance SHOULD remain explicit where source support, evidence, attribution, extraction history, transformation history, review history, validation history, import history, export history, migration history, or agent activity affects interpretation, authority, privacy, validation, lifecycle state, compatibility, or downstream use.

A deployment package SHOULD preserve lifecycle readiness.

Lifecycle State SHOULD remain explicit where lifecycle status affects review, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, validation, authority, privacy handling, source references, relationships, provenance, compatibility, workflow behavior, agent behavior, implementation behavior, publication, import, export, migration, or downstream use.

A deployment package SHOULD preserve authority readiness.

Authority Level SHOULD remain explicit where governance weight, interpretive authority, review weight, trust boundary, or use-authority affects interpretation, validation, publication, export, migration, agent reasoning, workflow routing, implementation behavior, or downstream use.

A deployment package SHOULD preserve privacy readiness.

Privacy Classification SHOULD remain explicit where permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling affects governed material.

A deployment package SHOULD preserve validation readiness.

Validation State, validation results, validation warnings, validation errors, validation scope, or validation review context SHOULD remain explicit where validation affects deployment readiness, review readiness, publication readiness, export readiness, migration readiness, implementation readiness, agent readiness, or downstream use.

A deployment package SHOULD preserve review readiness.

Review notes, approval notes, rejection notes, repair notes, escalation notes, unresolved issues, known limitations, handoff summaries, and audit-relevant records SHOULD remain available where they affect deployment decisions or future use.

A governed document is metadata-ready when a future human, agent, validator, workflow, implementation, repository, or downstream user can determine what the document is, what state it is in, what authority it has, what it depends on, how it should be interpreted, whether it may be used, and what review or validation remains required.

Metadata and Governed Document Readiness are successful when deployment materials remain identifiable, traceable, reviewable, portable, privacy-respecting, authority-aware, lifecycle-aware, validation-aware, implementation-independent, and usable without relying on hidden tool state or undocumented assumptions.

## 7. Knowledge Record and Source Material Readiness

Knowledge Record and Source Material Readiness define the minimum expectations required before a deployment package may safely accept, preserve, stage, review, transform, or use Source Material and Knowledge Records.

A bare usable deployment package SHALL preserve the distinction between Source Material and Knowledge Records.

Source Material is original input, evidence, reference, artifact, capture, or context.

A Knowledge Record is governed structured knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.

Source Material MUST NOT become a Knowledge Record merely because it is stored, copied, indexed, summarized, linked, embedded, processed by an agent, included in a repository, added to a vault, or placed in a deployment package.

A Knowledge Record MUST NOT be treated as Source Material merely because it cites, summarizes, extracts from, links to, or preserves evidence from Source Material.

A bare usable deployment package SHALL include or support a place for Source Material to be received, staged, preserved, reviewed, archived, quarantined, rejected, or routed.

A Source Material area or equivalent storage support SHOULD allow future humans, agents, workflows, validators, and implementations to determine:

- what Source Material was received;
- where it came from where known;
- whether it has been reviewed;
- whether it has been classified;
- whether it is restricted;
- whether it has been used to create a Knowledge Record;
- whether it has source-reference or provenance requirements;
- whether it should be archived, quarantined, rejected, imported, exported, backed up, or migrated;
- whether agent access is permitted;
- whether downstream use is permitted.

A bare usable deployment package SHALL include or support a place for Knowledge Records to be created, staged, reviewed, approved, maintained, archived, exported, migrated, or otherwise governed.

A Knowledge Record area or equivalent storage support SHOULD allow future humans, agents, workflows, validators, and implementations to determine:

- what Knowledge Object or governed entity the record represents;
- what Object Identity applies where required;
- what metadata applies;
- what relationships apply where required;
- what Source References apply where required;
- what provenance applies where required;
- what Lifecycle State applies;
- what Authority Level applies;
- what Privacy Classification applies;
- what Validation State applies;
- what review remains required;
- what downstream-use limits remain.

A bare usable deployment package SHOULD support Draft Knowledge Records.

A Draft Knowledge Record MUST remain distinguishable from an Approved Knowledge Record.

A Draft Knowledge Record MUST NOT be treated as approved, authoritative, validated, publishable, exportable, migratable, indexable, agent-readable, or downstream-usable merely because it exists in the deployment package.

A bare usable deployment package SHOULD support reviewed and approved Knowledge Records where practical.

An Approved Knowledge Record SHOULD preserve approval scope, review context, authority context, validation context, privacy context, source-reference context, provenance context, and downstream-use limits where those affect use.

A bare usable deployment package SHALL preserve Object Identity expectations for Knowledge Records.

A Knowledge Record MUST NOT receive its governed identity from filename, folder placement, repository path, application identifier, graph position, search result, tag, plugin field, cache entry, agent-generated label, or implementation-specific identifier alone.

A bare usable deployment package SHOULD preserve enough metadata for Knowledge Records to remain interpretable across copying, installation, backup, recovery, migration, synchronization, export, indexing, agent processing, and implementation replacement.

A bare usable deployment package SHALL preserve Source Reference and provenance expectations where Source Material materially supports a Knowledge Record, relationship, decision, classification, validation result, workflow output, or downstream-use decision.

A Knowledge Record created from Source Material SHOULD identify or support identification of:

- what Source Material was used;
- what extraction occurred;
- what transformation occurred;
- what interpretation occurred;
- what agent activity occurred where applicable;
- what workflow activity occurred where applicable;
- what human review occurred where applicable;
- what validation occurred where applicable;
- what limitations, uncertainty, restriction, or unresolved issue remains.

A bare usable deployment package SHOULD preserve relationship readiness for Knowledge Records.

A Knowledge Record SHOULD be capable of expressing, preserving, or referencing relationships where relationships affect meaning, provenance, dependency, hierarchy, sequence, evidence, supersession, derivation, validation, authority, privacy, workflow routing, or downstream use.

A bare usable deployment package SHOULD preserve privacy readiness for Source Material and Knowledge Records.

Restricted Source Material MUST NOT be exposed to Knowledge Records, agents, workflows, implementations, exports, indexes, backups, migrations, or downstream users without preserving applicable privacy boundaries.

Restricted Knowledge Records MUST NOT be exposed, published, exported, migrated, synchronized, indexed, backed up, summarized, or handed off without applicable privacy review and governed permission.

A bare usable deployment package SHOULD preserve validation readiness for Source Material and Knowledge Records.

Source Material and Knowledge Records SHOULD be capable of review, validation, repair, quarantine, rejection, archival, export limitation, migration limitation, backup limitation, or downstream-use limitation where required.

Knowledge Record and Source Material Readiness are successful when a future human, agent, workflow, validator, implementation, repository, vault, or downstream user can determine what material is source input, what material is governed knowledge, what source support exists, what provenance exists, what review remains required, what privacy limits apply, what validation state applies, and what may safely be used.

## 8. Agent and Workflow Readiness

Agent and Workflow Readiness define the minimum expectations required before agents, subagents, workflows, or automation may safely operate inside a bare usable deployment package.

A bare usable deployment package SHALL include or reference the Agent Standards required for safe agent participation.

At minimum, Agent Readiness requires:

- AG-0001 — Agent Operating Boundaries Standard;
- AG-0002 — Agent Role and Responsibility Standard;
- AG-0003 — Agent Permission and Traceability Standard.

A deployment package MUST NOT be treated as agent-ready merely because an agent, model, prompt, script, tool, plugin, automation, or runtime is available.

Agent availability is not Agent Readiness.

Agent capability is not Agent Permission.

Agent confidence is not Authority Level.

Agent output is not approval.

Agent completion is not workflow completion unless a governed workflow explicitly defines that effect within a controlled scope.

A bare usable deployment package SHALL make clear what agents may do, what agents must not do, what agents may only propose, and what actions require human review or governed workflow approval.

Agent Readiness SHOULD support:

- read boundaries;
- proposal boundaries;
- write boundaries;
- move boundaries;
- creation boundaries;
- deletion boundaries;
- publication boundaries;
- export boundaries;
- migration boundaries;
- synchronization boundaries;
- indexing boundaries;
- backup boundaries;
- implementation-exposure boundaries;
- agent-exposure boundaries;
- downstream-use boundaries;
- escalation boundaries;
- traceability requirements.

A bare usable deployment package SHOULD include or support agent role mapping.

Agent role mapping SHOULD identify which agent or subagent responsibilities are available for deployment use, including where applicable:

- Syntax Inspector;
- Standards Validator;
- Metadata Agent;
- Relationship Agent;
- Source and Provenance Agent;
- Privacy Agent;
- Workflow Agent;
- Duplicate and Identity Agent;
- Handoff Agent;
- Implementation Agent.

Agent role mapping MUST NOT grant permission by itself.

Agent permission remains governed by AG-0001, AG-0003, applicable workflow standards, applicable privacy limits, and any future permission profile or implementation profile.

A bare usable deployment package SHOULD support agent traceability.

Agent traceability SHOULD allow future review of:

- what agent acted;
- what role the agent performed;
- what permission scope applied;
- what material was inspected;
- what material was created, edited, moved, proposed, summarized, validated, exported, published, migrated, indexed, backed up, or exposed;
- what output was produced;
- what source material or evidence was used;
- what assumptions were made;
- what confidence or uncertainty was reported where applicable;
- what human review is required;
- what escalation occurred;
- what unresolved issue remains.

A bare usable deployment package SHALL include or reference the Workflow Standards required for safe governed use.

At minimum, Workflow Readiness requires:

- WF-0001 — Knowledge Ingestion Workflow Standard;
- WF-0002 — Review and Approval Workflow Standard;
- WF-0003 — Knowledge Maintenance and Update Workflow Standard;
- WF-0004 — Publication, Export, and Downstream Use Workflow Standard.

A deployment package MUST NOT be treated as workflow-ready merely because files, folders, agents, scripts, or implementation tools exist.

Workflow Readiness requires enough standard-level process clarity for future humans, agents, validators, implementations, and repositories to determine how governed material should be received, reviewed, approved, maintained, updated, exported, published, migrated, synchronized, indexed, backed up, recovered, exposed, or used downstream.

A bare usable deployment package SHOULD support ingestion workflow readiness.

Ingestion readiness SHOULD allow incoming Source Material, captured information, draft records, extracted content, or proposed knowledge to be received, staged, classified, sourced, transformed, validated, reviewed, rejected, repaired, quarantined, archived, or routed.

A bare usable deployment package SHOULD support review and approval workflow readiness.

Review readiness SHOULD allow governed entities to be inspected, corrected, approved, rejected, deferred, repaired, escalated, quarantined, archived, superseded, deprecated, or routed.

Approval readiness SHOULD preserve approval scope.

Approval readiness MUST NOT convert validation success, agent confidence, workflow completion, storage placement, implementation visibility, or user convenience into approval by implication.

A bare usable deployment package SHOULD support maintenance and update workflow readiness.

Maintenance readiness SHOULD allow governed entities to be checked for currency, correctness, source support, relationship validity, metadata completeness, lifecycle state, authority, privacy, validation, compatibility, repair needs, supersession, deprecation, archival, or reapproval needs.

A bare usable deployment package SHOULD support publication, export, and downstream-use workflow readiness.

Downstream-use readiness SHOULD allow governed entities to be evaluated for publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, and downstream use within explicit scope and permission boundaries.

Agent and Workflow Readiness are successful when agents and workflows can assist deployment use without becoming hidden authorities, bypassing review, weakening privacy, redefining validation, changing Object Identity, replacing provenance, overwriting relationships, expanding authority, bypassing lifecycle state, or turning implementation behavior into standard meaning.

## 9. Validation, Review, and Approval Readiness

Validation, Review, and Approval Readiness define the minimum expectations required before a deployment package may be treated as inspectable, governable, and safe for controlled use.

A bare usable deployment package SHALL support validation readiness.

Validation readiness means the package contains enough standards, structure, metadata, folder expectations, workflow expectations, agent expectations, and handoff context to determine whether the deployment package satisfies its applicable requirements.

Validation readiness does not require full automated validation.

Validation readiness does not require final mature tooling.

Validation readiness does require that future humans, agents, validators, workflows, repositories, or implementations can identify what should be checked and what result should block, warn, limit, repair, quarantine, escalate, or approve deployment use.

A deployment package SHOULD support validation checks for:

- required file presence;
- required metadata presence;
- required document status visibility;
- required authority visibility;
- required dependency visibility;
- required folder or storage-area support;
- Source Material and Knowledge Record distinction;
- Object Identity preservation;
- relationship readiness;
- Source Reference readiness;
- provenance readiness;
- lifecycle readiness;
- authority readiness;
- privacy readiness;
- validation state readiness;
- agent readiness;
- workflow readiness;
- review readiness;
- backup readiness;
- export readiness;
- handoff readiness;
- implementation-profile readiness.

A validation result MUST NOT be treated as approval unless a governed workflow or future specification explicitly defines that effect within a controlled scope.

A passing validation result means only that the validated material satisfied the applicable validation scope at the time of validation.

A failed validation result SHOULD block, limit, repair, quarantine, defer, or escalate deployment use where the failure affects governed meaning, identity, metadata, relationships, Source References, provenance, lifecycle state, authority, privacy, workflow behavior, agent behavior, implementation behavior, backup, export, migration, publication, or downstream use.

A validation warning SHOULD be reviewed where it indicates a risk, incompleteness, ambiguity, compatibility concern, missing context, unresolved issue, or deployment limitation.

A bare usable deployment package SHALL support review readiness.

Review readiness means the package can be inspected by a human or governed workflow before deployment decisions, approval decisions, publication decisions, export decisions, migration decisions, implementation decisions, agent-exposure decisions, or downstream-use decisions are made.

A deployment package SHOULD support review of:

- file completeness;
- document metadata;
- section structure;
- syntax correctness;
- grammar and spelling;
- dependency correctness;
- related-file correctness;
- standard boundary preservation;
- redundancy risk;
- implementation-specific leakage;
- folder readiness;
- Source Material readiness;
- Knowledge Record readiness;
- metadata readiness;
- privacy readiness;
- authority readiness;
- lifecycle readiness;
- validation readiness;
- agent readiness;
- workflow readiness;
- handoff readiness.

A review finding SHOULD identify:

- what was reviewed;
- what issue was found;
- what standard or expectation applies;
- whether the issue is blocking;
- whether correction is required;
- whether escalation is required;
- whether deployment may continue with limitation;
- whether the issue should be recorded in a handoff summary or deployment manifest.

A bare usable deployment package SHALL support approval readiness.

Approval readiness means the package can be evaluated for a scoped deployment decision.

Approval readiness does not mean the package is automatically approved.

Approval readiness does not mean the package is publicly releasable.

Approval readiness does not mean the package is implementation-complete.

Approval readiness does not mean agents may operate without permission.

Approval readiness does not mean publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, or downstream use is automatically permitted.

A deployment approval decision SHOULD identify:

- what package or scope is approved;
- what files are included;
- what files remain Draft;
- what files remain incomplete;
- what folders are included;
- what standards are approved;
- what standards still require approval;
- what implementation profiles are missing;
- what agent limits remain;
- what workflow limits remain;
- what validation limits remain;
- what privacy limits remain;
- what export or backup limits remain;
- what future work is required.

A bare usable deployment package MAY be approved for limited use.

Limited-use approval SHOULD define:

- the permitted use;
- the deployment scope;
- the allowed user or environment;
- the excluded uses;
- the known limitations;
- the review requirements;
- the validation requirements;
- the agent restrictions;
- the publication restrictions;
- the export restrictions;
- the migration restrictions;
- the downstream-use restrictions.

A deployment package SHOULD preserve review and approval traceability.

Review and approval traceability SHOULD allow future humans, agents, validators, workflows, repositories, implementations, and downstream users to determine what was approved, why it was approved, who or what reviewed it, what limitations remained, and what future work was expected.

Validation, Review, and Approval Readiness are successful when deployment decisions remain explicit, scoped, traceable, reviewable, privacy-respecting, authority-aware, lifecycle-aware, validation-aware, implementation-independent, and compatible with future correction, handoff, maintenance, export, migration, and implementation work.

## 10. Backup, Recovery, Export, and Copy Readiness

Backup, Recovery, Export, and Copy Readiness define the minimum expectations required before a deployment package may be copied, backed up, restored, exported, migrated, transferred, shared, or reused without losing governed meaning.

DEP-0001 does not define exact backup tools.

DEP-0001 does not define exact recovery tools.

DEP-0001 does not define exact export formats.

DEP-0001 does not define exact migration formats.

DEP-0001 does not define exact synchronization tools.

DEP-0001 does not define exact repository workflows.

DEP-0001 defines whether the deployment package contains enough structure, context, metadata, standards, workflow boundaries, and handoff information for backup, recovery, export, copy, transfer, and reuse to occur safely.

A bare usable deployment package SHALL support copy readiness.

Copy readiness means the package can be copied to another location, machine, repository, storage environment, vault, archive, backup target, or implementation-support area without losing the ability to interpret the package.

A copied package SHOULD preserve:

- governed files;
- required standards;
- required specifications where applicable;
- folder structure or layout context;
- Source Material areas where included;
- Knowledge Record areas where included;
- draft areas where included;
- review areas where included;
- archive areas where included;
- import areas where included;
- export areas where included;
- backup areas where included;
- implementation-support areas where included;
- agent-support areas where included;
- workflow-support areas where included;
- metadata;
- Object Identity expectations;
- relationships;
- Source References;
- provenance;
- lifecycle state;
- authority level;
- privacy classification;
- validation state;
- handoff summaries;
- manifests;
- known limitations.

A copied package MUST NOT treat the copy event itself as approval, publication permission, export clearance, migration clearance, synchronization permission, indexing permission, backup permission, recovery success, implementation approval, agent permission, or downstream-use permission.

A bare usable deployment package SHALL support backup readiness.

Backup readiness means the package can be preserved for restoration, continuity, disaster recovery, rollback, audit, archival, or migration support without losing governed context.

A backup SHOULD preserve enough information to determine:

- what was backed up;
- when the backup was created where known;
- what scope the backup covers;
- what files were included;
- what folders were included;
- what material was excluded;
- what privacy restrictions apply;
- what validation status applied at the time of backup;
- what known limitations existed;
- whether the backup is complete, partial, restricted, test-only, archival, or recovery-ready.

A backup MUST NOT be treated as recovery-ready merely because a copy exists.

Recovery readiness requires enough context to restore, inspect, validate, repair, quarantine, escalate, or reject restored material.

A bare usable deployment package SHALL support recovery readiness.

Recovery readiness means recovered material can be checked before being treated as active governed material.

A recovery process SHOULD allow future humans, agents, validators, workflows, implementations, or repositories to determine:

- what material was restored;
- what backup or source was used;
- whether metadata remained intact;
- whether Object Identity expectations remained intact;
- whether relationships remained intact;
- whether Source References remained intact;
- whether provenance remained intact;
- whether lifecycle state remained intact;
- whether authority level remained intact;
- whether privacy classification remained intact;
- whether validation state remained intact;
- whether restored files conflict with newer files;
- whether restored files supersede or are superseded by current files;
- whether restored material requires review;
- whether restored material requires quarantine;
- whether restored material may be used.

A recovered file MUST NOT be treated as current, approved, authoritative, validated, publishable, exportable, migratable, implementation-ready, agent-readable, or downstream-usable merely because it was restored.

A bare usable deployment package SHALL support export readiness.

Export readiness means the package can identify whether material may be prepared for transfer, publication, migration, sharing, review, backup, or downstream use within governed limits.

Export readiness does not grant export permission by itself.

Export permission remains governed by applicable privacy, authority, lifecycle, validation, source-reference, provenance, relationship, workflow, and downstream-use requirements.

An export-ready package SHOULD allow future humans, agents, validators, workflows, implementations, repositories, or downstream users to determine:

- what material is being exported;
- why the export is occurring;
- what scope applies;
- what format or representation is used where known;
- what metadata is included;
- what metadata is excluded;
- what Source References are included;
- what provenance is included;
- what relationships are included;
- what privacy restrictions apply;
- what authority limits apply;
- what lifecycle limits apply;
- what validation limits apply;
- what downstream-use limits apply;
- what review remains required.

A bare usable deployment package SHOULD support migration readiness.

Migration readiness means the package can be moved between storage environments, repositories, vaults, implementations, formats, machines, or future standard versions without losing governed meaning.

Migration readiness SHOULD preserve or support preservation of:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- lifecycle state;
- authority level;
- privacy classification;
- validation state;
- file status;
- dependency context;
- review context;
- handoff context;
- known limitations.

A migration-ready package MUST NOT treat migration success as validation success, approval, publication clearance, export permission, privacy clearance, agent permission, implementation approval, or downstream-use permission.

A bare usable deployment package SHOULD support synchronization readiness where synchronization is expected.

Synchronization readiness means the package can identify what material may be synchronized, what material must not be synchronized, what material requires privacy review, and what conflicts require review before use.

Synchronization MUST NOT weaken privacy classification, authority level, lifecycle state, validation state, Source References, provenance, Object Identity, relationships, approval scope, or downstream-use limits.

A bare usable deployment package SHOULD support indexing readiness where indexing is expected.

Indexing readiness means the package can identify what material may be indexed, what material must not be indexed, what material may be indexed only in restricted form, and what generated index material must remain subordinate to governed source files.

An index, embedding, cache, graph, search database, generated summary, or derived representation MUST NOT replace the governed entity it represents.

Backup, Recovery, Export, and Copy Readiness are successful when deployment material can be preserved, restored, copied, exported, migrated, synchronized, indexed, transferred, or reused without confusing preservation with approval, export with clearance, recovery with currency, copy with authority, migration with validation, or implementation convenience with governed meaning.

## 11. Implementation Profile Readiness

Implementation Profile Readiness defines the minimum expectations required before a deployment package may safely support tool-specific implementation work.

DEP-0001 does not define the implementation profile itself.

DEP-0001 does not define exact Obsidian behavior.

DEP-0001 does not define exact Codex behavior.

DEP-0001 does not define exact local AI behavior.

DEP-0001 does not define exact repository automation.

DEP-0001 does not define exact scripts, plugins, dashboards, templates, prompts, validators, folder names, hotkeys, views, sync behavior, backup tools, or runtime configuration.

DEP-0001 defines when the standard package is ready enough for an implementation profile to depend on it.

An implementation profile SHOULD NOT be created as the source of truth for knowledge meaning.

An implementation profile SHOULD explain how a specific tool, vault, repository, AI system, local machine, workflow environment, or software stack realizes The Brain Standard in practice.

An implementation profile MUST remain subordinate to the constitutional foundation, Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, and deployment-readiness requirements.

A bare usable deployment package is implementation-profile ready when it contains enough governed context for a future implementation profile to determine:

- what standards must be followed;
- what files are required;
- what files are draft;
- what files are approved;
- what folders or storage areas are expected;
- what metadata expectations apply;
- what Object Identity expectations apply;
- what relationship expectations apply;
- what Source Reference expectations apply;
- what provenance expectations apply;
- what lifecycle expectations apply;
- what authority expectations apply;
- what privacy expectations apply;
- what validation expectations apply;
- what agent boundaries apply;
- what workflow boundaries apply;
- what backup, export, migration, synchronization, indexing, and downstream-use limits apply;
- what handoff context exists;
- what limitations remain.

A bare usable deployment package SHOULD identify which implementation profile is expected next.

Where Obsidian and Codex are the next target implementation, the expected next implementation profile SHOULD be:

- IMP-0001 — Obsidian and Codex Implementation Profile.

IMP-0001 SHOULD define how Obsidian and Codex realize the standard in practice.

IMP-0001 SHOULD NOT redefine the standard.

IMP-0001 SHOULD explain tool-specific handling for:

- vault or repository placement;
- folder layout realization;
- Markdown file handling;
- metadata representation;
- Knowledge Record handling;
- Source Material handling;
- templates;
- prompts;
- agent usage;
- workflow execution;
- validation support;
- review support;
- search and navigation;
- graph or backlink behavior;
- indexing behavior;
- backup behavior;
- export behavior;
- sync behavior where applicable;
- local machine setup;
- limitations and risks.

An implementation profile MUST NOT treat tool capability as standard authority.

An implementation profile MUST NOT treat plugin behavior as governed meaning.

An implementation profile MUST NOT treat UI visibility as privacy clearance.

An implementation profile MUST NOT treat search results as validation.

An implementation profile MUST NOT treat backlinks as governed relationships unless the applicable relationship standard or specification supports that use.

An implementation profile MUST NOT treat file location as Object Identity.

An implementation profile MUST NOT treat agent access as permission.

An implementation profile MUST NOT treat automation success as review approval.

An implementation profile MUST NOT treat repository presence as deployment approval.

An implementation profile MUST NOT treat synchronization as publication permission.

An implementation profile MUST NOT treat backup as downstream-use permission.

An implementation profile MAY define implementation-specific constraints.

Implementation-specific constraints SHOULD be recorded as implementation behavior, not standard behavior.

Implementation-specific constraints MAY include:

- tool limitations;
- plugin limitations;
- local file-system limitations;
- repository limitations;
- operating-system limitations;
- model limitations;
- automation limitations;
- synchronization limitations;
- backup limitations;
- export limitations;
- indexing limitations;
- validation limitations;
- privacy limitations;
- human workflow limitations.

A deployment package MAY be bare usable before an implementation profile is complete.

A deployment package MUST NOT be treated as implementation-complete merely because DEP-0001 is complete.

DEP-0001 approves readiness to proceed toward implementation profiling, not completion of the implementation.

Implementation Profile Readiness is successful when a future implementation profile can realize The Brain Standard in a specific tool environment without becoming the standard, weakening governance, hiding assumptions, bypassing review, or redefining knowledge meaning through software behavior.

## 12. Deployment Package Manifest and Handoff Readiness

Deployment Package Manifest and Handoff Readiness define the minimum expectations required for a deployment package to be understandable, inspectable, transferable, and usable by a future human, agent, repository, vault, implementation, or machine.

A bare usable deployment package SHOULD include a deployment manifest.

The deployment manifest SHOULD identify the contents, status, scope, limitations, and readiness state of the package.

A deployment manifest SHOULD include:

- package name;
- package version where applicable;
- package date where applicable;
- deployment scope;
- intended use;
- excluded use;
- included standards;
- missing standards;
- approved files;
- draft files;
- review files;
- deprecated files;
- superseded files;
- required files;
- recommended files;
- optional files;
- included folders or storage areas;
- missing folders or storage areas;
- included implementation profiles;
- missing implementation profiles;
- included agent-support files;
- included workflow-support files;
- included validation-support files;
- included templates;
- included scripts;
- included prompts;
- included Source Material areas;
- included Knowledge Record areas;
- included archive areas;
- included import areas;
- included export areas;
- included backup areas;
- known risks;
- known limitations;
- unresolved questions;
- next required step.

A deployment manifest SHOULD NOT become the source of truth for governed meaning.

A deployment manifest summarizes package state.

A deployment manifest does not approve files by itself.

A deployment manifest does not validate files by itself.

A deployment manifest does not grant publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, or downstream-use permission by itself.

A deployment manifest MUST remain subordinate to the applicable standards, specifications, workflows, agent permissions, privacy classifications, validation results, approval decisions, and handoff records.

A bare usable deployment package SHOULD include a current handoff summary.

The handoff summary SHOULD preserve enough context for another person, agent, workflow, implementation, repository, vault, or future session to continue without losing the project’s scope, architecture, standards boundaries, current status, remaining work, or known risks.

A handoff summary SHOULD identify:

- what has been completed;
- what file or milestone the handoff is for;
- what sections were created;
- how many sections the file contains;
- what sections remain;
- what standards were reviewed;
- what files were compared;
- what known drift risks were checked;
- what corrections were made;
- what corrections remain;
- what files should be created next;
- what files should not be redefined;
- what decisions were made;
- what assumptions were made;
- what dependencies matter;
- what implementation work should follow;
- what user instructions should continue to apply.

A handoff summary SHOULD preserve the three-section batching context where applicable.

A handoff summary SHOULD identify the current running count of completed sections.

A handoff summary SHOULD identify whether the next response should continue drafting, review the full file, finalize metadata, request approval, create a repository file, create an implementation profile, create a deployment manifest, or stop for user confirmation.

A handoff summary MUST NOT replace the standard.

A handoff summary MUST NOT approve the file unless approval is explicitly granted through the appropriate governance process.

A handoff summary MUST NOT create new standards by implication.

A handoff summary MUST NOT redefine prior standards.

A handoff summary MUST NOT silently change scope, authority, lifecycle state, privacy classification, validation state, implementation readiness, deployment readiness, or downstream-use permission.

A deployment package SHOULD include enough README or orientation material for basic use.

Orientation material SHOULD explain:

- what The Brain package is;
- what it is not;
- where standards are stored;
- where Source Material belongs;
- where Knowledge Records belong;
- where drafts belong;
- where review material belongs;
- where archives belong;
- where exports belong;
- where backups belong;
- what agents may do;
- what agents must not do;
- what workflows exist;
- what validation means;
- what approval means;
- what implementation profile should be used next;
- what limitations remain.

A deployment package SHOULD include known limitation records where limitations affect deployment use.

Known limitation records SHOULD identify:

- missing files;
- incomplete files;
- draft files;
- unapproved files;
- missing folders;
- missing templates;
- missing validators;
- missing scripts;
- missing implementation profiles;
- missing agent prompts;
- missing workflow aids;
- unresolved metadata questions;
- unresolved privacy issues;
- unresolved validation issues;
- unresolved source-reference issues;
- unresolved provenance issues;
- unresolved relationship issues;
- unresolved backup issues;
- unresolved export issues;
- unresolved migration issues;
- unresolved implementation issues.

A deployment package SHOULD support continuation by a future human or agent.

Continuation readiness means the next actor can determine what has already been done, what remains to do, what must be reviewed, what must not be changed, what must not be redefined, and what next milestone should occur.

Deployment Package Manifest and Handoff Readiness are successful when a deployment package can be handed to another human, agent, implementation, repository, vault, local machine, or future session without losing context, weakening governance, confusing draft status with approval, confusing deployment readiness with implementation completion, or causing architectural drift.

## 13. Non-Conformance, Gaps, and Corrective Routing

Non-Conformance, Gaps, and Corrective Routing define how deployment-readiness failures, missing materials, incomplete files, unresolved risks, structural conflicts, and deployment limitations are identified and routed.

A deployment package is non-conforming when it fails to satisfy a mandatory deployment-readiness requirement defined by DEP-0001 or by a higher-authority standard that DEP-0001 depends on.

A deployment package has a gap when a required, recommended, expected, or planned file, folder, metadata element, workflow support, agent support, validation support, review support, manifest item, handoff item, backup support, export support, implementation-support item, or deployment context item is missing, incomplete, ambiguous, outdated, unreviewed, or not yet approved.

A gap is not always blocking.

A non-conformance may be blocking.

The deployment package SHOULD distinguish between:

- blocking non-conformance;
- limited-use non-conformance;
- correctable gap;
- deferred gap;
- known limitation;
- implementation-specific limitation;
- unresolved governance issue;
- unresolved privacy issue;
- unresolved validation issue;
- unresolved source-reference issue;
- unresolved provenance issue;
- unresolved relationship issue;
- unresolved agent issue;
- unresolved workflow issue;
- unresolved storage-layout issue;
- unresolved handoff issue.

A blocking non-conformance SHALL prevent bare usable deployment until the issue is corrected, explicitly scoped out, or escalated through a governed review process.

Blocking non-conformance includes any condition that prevents future humans, agents, workflows, validators, repositories, vaults, implementations, or downstream users from determining:

- what the package is;
- what files are required;
- what files are missing;
- what files are Draft;
- what files are Approved;
- what authority applies;
- what dependencies apply;
- what storage areas are expected;
- what Source Material is present;
- what Knowledge Records are present;
- what metadata expectations apply;
- what Object Identity expectations apply;
- what privacy limits apply;
- what validation state applies;
- what agent permissions apply;
- what workflow routing applies;
- what backup, export, migration, synchronization, indexing, or downstream-use limits apply;
- what handoff context applies.

A deployment package SHALL be treated as non-conforming if it is missing the constitutional foundation required for interpretation.

A deployment package SHALL be treated as non-conforming if it lacks enough Knowledge Standards to preserve knowledge meaning.

A deployment package SHALL be treated as non-conforming if it lacks enough Storage Standards to distinguish storage support from governed meaning.

A deployment package SHALL be treated as non-conforming if it lacks enough Agent Standards to prevent agent authority creep.

A deployment package SHALL be treated as non-conforming if it lacks enough Workflow Standards to support governed ingestion, review, maintenance, publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, or downstream use.

A deployment package SHALL be treated as non-conforming if DEP-0001 itself is missing, incomplete, corrupted, misidentified, or materially inconsistent with the standards it depends on.

A deployment package SHOULD be treated as non-conforming if required metadata is missing from governed documents.

A deployment package SHOULD be treated as non-conforming if document status cannot be determined.

A deployment package SHOULD be treated as non-conforming if Draft material can be confused with Approved material.

A deployment package SHOULD be treated as non-conforming if Source Material can be confused with Knowledge Records.

A deployment package SHOULD be treated as non-conforming if folder placement, filename, repository path, implementation identifier, plugin behavior, graph position, cache entry, search result, backlink, or agent-generated label is being treated as Object Identity by itself.

A deployment package SHOULD be treated as non-conforming if privacy classification cannot be determined for restricted or potentially restricted material.

A deployment package SHOULD be treated as non-conforming if agent access is treated as permission.

A deployment package SHOULD be treated as non-conforming if validation success is treated as approval.

A deployment package SHOULD be treated as non-conforming if workflow completion is treated as publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, or downstream-use permission without governed clearance.

A deployment package SHOULD be treated as non-conforming if implementation behavior redefines standard meaning.

A deployment package SHOULD be treated as non-conforming if a copy, backup, export, migration, synchronization, index, generated summary, cache, embedding, graph, or repository state is treated as the governed source of truth without review.

Corrective routing SHOULD identify the appropriate path for each issue.

A deployment-readiness issue MAY be routed to:

- correction;
- metadata repair;
- syntax repair;
- grammar repair;
- standards review;
- redundancy review;
- dependency review;
- folder-layout review;
- privacy review;
- source-reference review;
- provenance review;
- relationship review;
- validation review;
- agent-boundary review;
- workflow review;
- implementation-boundary review;
- backup review;
- export review;
- migration review;
- quarantine;
- limited-use approval;
- deferred work;
- handoff documentation;
- governance escalation.

A corrective routing record SHOULD identify:

- what issue was found;
- where the issue appears;
- what standard or expectation applies;
- whether the issue is blocking;
- whether limited use is allowed;
- what correction is required;
- who or what should review the correction;
- what evidence or source material applies;
- what risk remains;
- whether the issue must be added to the deployment manifest;
- whether the issue must be added to the handoff summary;
- whether deployment may continue.

A missing required file SHALL be routed to correction or explicit limited-scope review.

A missing recommended file SHOULD be routed to known limitation tracking.

A missing optional file MAY be routed to future work tracking where it affects implementation planning or handoff clarity.

A missing folder or storage area SHALL be routed to layout correction where the missing area prevents safe use.

A missing metadata expectation SHALL be routed to metadata repair where the missing metadata affects identity, authority, lifecycle state, privacy, validation, provenance, relationship context, dependency context, or deployment interpretation.

A privacy issue SHALL be routed to privacy review before exposure, publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream use.

An agent-permission issue SHALL be routed to agent-boundary review or permission review before the agent may act.

A workflow ambiguity SHALL be routed to workflow review before the affected process is treated as deployable.

An implementation-specific conflict SHALL be routed to implementation-profile work unless the conflict reveals a standard-level issue.

A standard-level conflict SHALL be routed to governance review.

A non-conforming deployment package MAY be used only under explicitly limited conditions where the limitation is recorded, reviewed, and understood.

Limited use MUST NOT conceal non-conformance.

Limited use MUST NOT convert Draft material into Approved material.

Limited use MUST NOT grant agent permission, publication permission, export permission, migration permission, synchronization permission, indexing permission, backup permission, recovery permission, implementation approval, or downstream-use permission by implication.

Non-Conformance, Gaps, and Corrective Routing are successful when every deployment-readiness failure, limitation, missing item, unresolved issue, or drift risk can be identified, classified, routed, corrected, deferred, escalated, or recorded without weakening governance or hiding risk.

## 14. Deployment Conformance Requirements

Deployment Conformance Requirements define the conditions that MUST be satisfied before a Brain package may be classified as conforming to DEP-0001.

A DEP-0001-conforming deployment package SHALL preserve the constitutional foundation of The Brain Standard.

A DEP-0001-conforming deployment package SHALL preserve the distinction between:

- knowledge meaning and storage placement;
- deployment readiness and implementation readiness;
- implementation profile and standard;
- Source Material and Knowledge Record;
- Draft status and Approved status;
- validation result and approval decision;
- agent role and agent permission;
- agent output and governed meaning;
- workflow completion and downstream-use clearance;
- backup existence and recovery readiness;
- export preparation and export permission;
- migration success and validation success;
- synchronization and publication permission;
- indexing and governed source of truth;
- handoff summary and standard authority.

A DEP-0001-conforming deployment package SHALL include or support the required constitutional files.

A DEP-0001-conforming deployment package SHALL include or support the required Knowledge Standards.

A DEP-0001-conforming deployment package SHALL include or support the required Storage Standards.

A DEP-0001-conforming deployment package SHALL include or support the required Agent Standards.

A DEP-0001-conforming deployment package SHALL include or support the required Workflow Standards.

A DEP-0001-conforming deployment package SHALL include DEP-0001.

A DEP-0001-conforming deployment package SHOULD include or support a deployment manifest.

A DEP-0001-conforming deployment package SHOULD include or support a current handoff summary.

A DEP-0001-conforming deployment package SHALL preserve document identity, title, version, status, authority, phase, milestone, dependencies, supersession information, and related-file information where those apply.

A DEP-0001-conforming deployment package SHALL preserve enough folder-layout context to determine where governed documents, Source Material, Knowledge Records, drafts, review material, archives, imports, exports, backups, migration material, implementation-support files, agent-support files, workflow-support files, generated files, and supporting assets belong.

A DEP-0001-conforming deployment package SHALL preserve enough metadata context to support Object Identity, document interpretation, governance review, dependency review, lifecycle review, authority review, privacy review, validation review, provenance review, relationship review, workflow review, agent review, implementation review, export review, backup review, and handoff review.

A DEP-0001-conforming deployment package SHALL preserve enough Source Material context to determine what source artifacts exist, where they belong, what review applies, what privacy limits apply, what provenance applies, what Source References apply, and whether the material has been used to create governed knowledge.

A DEP-0001-conforming deployment package SHALL preserve enough Knowledge Record context to determine what governed knowledge exists, what Object Identity applies, what metadata applies, what Source References apply, what provenance applies, what relationships apply, what lifecycle state applies, what authority level applies, what privacy classification applies, what validation state applies, and what review remains required.

A DEP-0001-conforming deployment package SHALL preserve enough agent context to determine what agents may inspect, propose, create, edit, move, validate, summarize, route, export, publish, migrate, synchronize, index, back up, expose, or escalate.

A DEP-0001-conforming deployment package SHALL preserve enough workflow context to determine how governed material is ingested, reviewed, approved, rejected, repaired, maintained, updated, deprecated, superseded, archived, published, exported, migrated, synchronized, indexed, backed up, recovered, exposed, or used downstream.

A DEP-0001-conforming deployment package SHALL preserve enough validation context to determine what checks apply, what results mean, what blocks deployment, what limits deployment, what requires repair, what requires quarantine, and what requires escalation.

A DEP-0001-conforming deployment package SHALL preserve enough review and approval context to determine what has been reviewed, what remains unreviewed, what has been approved, what remains Draft, what remains incomplete, what remains limited-use only, and what requires future governance action.

A DEP-0001-conforming deployment package SHALL preserve enough backup, recovery, export, copy, migration, synchronization, and indexing context to prevent operational actions from being confused with governed approval or clearance.

A DEP-0001-conforming deployment package SHOULD preserve enough implementation-profile context to determine what implementation profile should follow and what implementation-specific work is not yet complete.

A DEP-0001-conforming deployment package SHALL identify known limitations that affect deployment use.

A DEP-0001-conforming deployment package SHALL identify blocking non-conformance where known.

A DEP-0001-conforming deployment package SHOULD identify non-blocking gaps where known.

A DEP-0001-conforming deployment package SHOULD identify deferred work where known.

A DEP-0001-conforming deployment package MUST NOT hide Draft status, missing files, missing folders, missing metadata, unresolved privacy issues, unresolved validation issues, unresolved source-reference issues, unresolved provenance issues, unresolved relationship issues, unresolved agent issues, unresolved workflow issues, unresolved implementation issues, or unresolved handoff issues.

A DEP-0001-conforming deployment package MUST NOT require a specific tool to interpret standard-level meaning.

A DEP-0001-conforming deployment package MUST NOT require Obsidian, Codex, a plugin, a script, a database, a graph view, an index, a cache, an embedding store, a repository interface, or an agent runtime to determine the basic deployment-readiness state of the package.

A DEP-0001-conforming deployment package MAY be designed to work well with specific tools.

Tool support MUST remain subordinate to the standard.

A deployment package MAY be classified as:

- Not Ready;
- Draft Deployment Package;
- Limited-Use Deployment Package;
- Bare Usable Deployment Package;
- Implementation-Ready Candidate;
- Implementation-Ready Package;
- Public-Release Candidate;
- Public-Release Package.

Not Ready means blocking non-conformance prevents deployment use.

Draft Deployment Package means the package is being assembled but has not yet satisfied bare usable deployment requirements.

Limited-Use Deployment Package means the package may be used only within an explicitly limited scope.

Bare Usable Deployment Package means the package satisfies DEP-0001 enough for controlled practical use.

Implementation-Ready Candidate means the package appears ready to support a specific implementation profile but still requires implementation-profile review.

Implementation-Ready Package means the package and implementation profile have been reviewed for a specific tool environment.

Public-Release Candidate means the package is being reviewed for broader distribution beyond controlled use.

Public-Release Package means the package has passed the additional review, privacy, licensing, export, documentation, implementation, and governance requirements needed for broader distribution.

DEP-0001 primarily governs the transition from Draft Deployment Package or Limited-Use Deployment Package to Bare Usable Deployment Package.

Implementation-ready and public-release classifications require additional implementation, privacy, review, publication, export, documentation, and governance controls beyond DEP-0001.

Deployment Conformance Requirements are successful when a future human, agent, validator, repository, vault, implementation profile, or downstream user can determine whether a deployment package conforms to DEP-0001, what classification applies, what limitations remain, and what additional work is required before broader implementation or release.

## 15. Bare Usable Deployment Checklist

The Bare Usable Deployment Checklist defines the minimum review sequence that SHOULD be completed before a Brain package is treated as a Bare Usable Deployment Package.

The checklist is a readiness aid.

The checklist does not replace DEP-0001.

The checklist does not replace validation.

The checklist does not replace review.

The checklist does not approve the deployment package by itself.

A checklist item marked complete means only that the item was checked within the stated scope.

A bare usable deployment review SHOULD verify constitutional readiness.

Constitutional readiness SHOULD confirm that:

- TB-0000 exists;
- TB-0001 exists;
- TB-0002 exists;
- TB-0003 exists;
- the constitutional files are identifiable;
- the constitutional files have visible status;
- the constitutional files preserve implementation independence;
- the constitutional files do not conflict with DEP-0001.

A bare usable deployment review SHOULD verify Knowledge Standard readiness.

Knowledge Standard readiness SHOULD confirm that:

- KS-0001 exists;
- KS-0002 exists;
- KS-0003 exists;
- KS-0004 exists;
- KS-0005 exists;
- KS-0006 exists;
- KS-0007 exists;
- KS-0008 exists;
- KS-0009 exists;
- knowledge meaning remains distinct from storage placement;
- Object Identity is preserved as implementation-independent;
- metadata expectations are explicit;
- relationship expectations are explicit;
- Source Reference and provenance expectations are explicit;
- Lifecycle State expectations are explicit;
- Authority Level expectations are explicit;
- Privacy Classification expectations are explicit;
- Validation expectations are explicit.

A bare usable deployment review SHOULD verify Storage Standard readiness.

Storage Standard readiness SHOULD confirm that:

- SS-0001 exists;
- SS-0002 exists;
- storage architecture is distinguishable from storage layout;
- governed document placement is supported;
- Source Material placement is supported;
- Knowledge Record placement is supported;
- draft placement is supported;
- review placement is supported;
- archive placement is supported;
- import placement is supported;
- export placement is supported;
- backup placement or backup targeting is supported;
- migration placement is supported where needed;
- implementation-support placement is supported where needed;
- agent-support placement is supported where needed;
- workflow-support placement is supported where needed;
- generated-file or index/cache placement is understood where needed;
- folder placement does not define governed meaning by itself.

A bare usable deployment review SHOULD verify Agent Standard readiness.

Agent Standard readiness SHOULD confirm that:

- AG-0001 exists;
- AG-0002 exists;
- AG-0003 exists;
- agent operating boundaries are explicit;
- agent roles are explicit;
- agent permissions are explicit or supportable;
- agent traceability expectations are explicit;
- agent outputs do not equal approval by themselves;
- agent access does not equal permission by itself;
- agent confidence does not equal authority by itself;
- high-risk agent operations require review, permission, or escalation;
- agent use remains subordinate to standards and workflows.

A bare usable deployment review SHOULD verify Workflow Standard readiness.

Workflow Standard readiness SHOULD confirm that:

- WF-0001 exists;
- WF-0002 exists;
- WF-0003 exists;
- WF-0004 exists;
- ingestion workflow behavior is defined;
- review and approval workflow behavior is defined;
- maintenance and update workflow behavior is defined;
- publication, export, and downstream-use workflow behavior is defined;
- workflow completion does not equal approval unless explicitly defined;
- approval does not equal publication or export clearance unless explicitly cleared;
- workflow routing can handle repair, rejection, quarantine, escalation, archive, export, migration, backup, and downstream-use decisions.

A bare usable deployment review SHOULD verify DEP-0001 readiness.

DEP-0001 readiness SHOULD confirm that:

- DEP-0001 exists;
- DEP-0001 has correct document metadata;
- DEP-0001 has correct dependency references;
- DEP-0001 has correct section sequence;
- DEP-0001 does not redefine prior standards;
- DEP-0001 defines deployment readiness rather than implementation behavior;
- DEP-0001 identifies minimum file readiness;
- DEP-0001 identifies folder readiness;
- DEP-0001 identifies metadata readiness;
- DEP-0001 identifies Source Material and Knowledge Record readiness;
- DEP-0001 identifies agent and workflow readiness;
- DEP-0001 identifies validation, review, and approval readiness;
- DEP-0001 identifies backup, recovery, export, and copy readiness;
- DEP-0001 identifies implementation-profile readiness;
- DEP-0001 identifies manifest and handoff readiness;
- DEP-0001 identifies non-conformance routing;
- DEP-0001 identifies conformance requirements.

A bare usable deployment review SHOULD verify document hygiene.

Document hygiene SHOULD confirm that:

- all required files have readable titles;
- all required files have readable document IDs;
- all required files have visible status;
- all required files have visible authority;
- all required files have visible dependency information;
- headings are correctly formed;
- section numbering is correct where used;
- duplicate headings are not present unless intentionally allowed;
- Markdown syntax is usable;
- spelling and grammar have been reviewed;
- no blocking syntax errors remain;
- no unresolved standard-boundary conflicts remain.

A bare usable deployment review SHOULD verify package usability.

Package usability SHOULD confirm that a future user can determine:

- where to place new Source Material;
- where to create or stage Draft Knowledge Records;
- where governed documents belong;
- where drafts belong;
- where review material belongs;
- where archives belong;
- where exports belong;
- where backups belong;
- what files are required;
- what files remain Draft;
- what files are Approved;
- what agents may do;
- what agents must not do;
- what workflows apply;
- what review is required;
- what validation means;
- what approval means;
- what implementation profile should follow.

A bare usable deployment review SHOULD verify copy and handoff readiness.

Copy and handoff readiness SHOULD confirm that:

- the package can be copied without losing context;
- the package can be handed off without losing current status;
- the package can be restored or reviewed after backup;
- the package can identify known limitations;
- the package can identify missing files;
- the package can identify draft files;
- the package can identify next steps;
- the package can identify what should not be redefined;
- the package can identify whether implementation profiling may begin.

A bare usable deployment review SHOULD verify limitation tracking.

Limitation tracking SHOULD confirm that:

- missing required files are recorded;
- missing recommended files are recorded where relevant;
- missing folders are recorded where relevant;
- Draft files are recorded;
- unapproved files are recorded;
- missing templates are recorded where relevant;
- missing validators are recorded where relevant;
- missing prompts are recorded where relevant;
- missing implementation profiles are recorded where relevant;
- unresolved privacy issues are recorded;
- unresolved validation issues are recorded;
- unresolved source-reference issues are recorded;
- unresolved provenance issues are recorded;
- unresolved relationship issues are recorded;
- unresolved backup issues are recorded;
- unresolved export issues are recorded;
- unresolved migration issues are recorded;
- unresolved implementation issues are recorded.

A bare usable deployment review SHOULD end with a scoped readiness finding.

The readiness finding SHOULD classify the package as:

- Not Ready;
- Draft Deployment Package;
- Limited-Use Deployment Package;
- Bare Usable Deployment Package;
- Implementation-Ready Candidate.

A readiness finding SHOULD identify:

- whether deployment may proceed;
- whether use must be limited;
- what corrections are required;
- what risks remain;
- what files should be created next;
- whether a handoff summary is required;
- whether implementation profiling may begin.

The Bare Usable Deployment Checklist is successful when a future human, agent, validator, repository, vault, implementation profile, or downstream user can inspect the package consistently and determine whether The Brain is ready for controlled bare usable deployment.

## 16. Success Criteria

DEP-0001 is successful when it defines a clear, reviewable, implementation-independent readiness boundary for a bare usable Brain deployment package.

A deployment package satisfies the success criteria for DEP-0001 when future humans, agents, validators, workflows, repositories, vaults, implementations, and downstream users can determine whether the package is ready for controlled practical use.

DEP-0001 success requires that deployment readiness can be evaluated without relying on hidden tool state, undocumented assumptions, agent memory, plugin behavior, user-interface display, generated indexes, caches, embeddings, graph views, search results, repository convenience, or implementation-specific behavior.

A successful bare usable deployment package SHALL preserve the constitutional foundation of The Brain Standard.

A successful bare usable deployment package SHALL preserve implementation independence.

A successful bare usable deployment package SHALL preserve the distinction between the standard and any specific tool, vault, repository, software environment, agent runtime, automation system, plugin stack, local machine, or future implementation.

A successful bare usable deployment package SHALL include or support the minimum required standards needed for controlled use.

At minimum, success requires the package to include or support:

- constitutional foundation files;
- Knowledge Standards;
- Storage Standards;
- Agent Standards;
- Workflow Standards;
- DEP-0001;
- enough folder-layout context for use;
- enough metadata context for interpretation;
- enough Source Material context for preservation;
- enough Knowledge Record context for governed knowledge use;
- enough agent context for safe assistance;
- enough workflow context for governed process use;
- enough validation context for inspection;
- enough review context for approval decisions;
- enough backup, recovery, export, copy, migration, synchronization, and indexing context to prevent operational confusion;
- enough implementation-profile context to identify the next implementation step;
- enough manifest or handoff context to preserve continuity.

A successful bare usable deployment package SHALL make file readiness distinguishable from file existence.

A successful bare usable deployment package SHALL make folder readiness distinguishable from folder existence.

A successful bare usable deployment package SHALL make deployment readiness distinguishable from implementation readiness.

A successful bare usable deployment package SHALL make implementation readiness distinguishable from public-release readiness.

A successful bare usable deployment package SHALL make Source Material distinguishable from Knowledge Records.

A successful bare usable deployment package SHALL make Draft material distinguishable from Approved material.

A successful bare usable deployment package SHALL make validation distinguishable from approval.

A successful bare usable deployment package SHALL make review distinguishable from approval.

A successful bare usable deployment package SHALL make approval distinguishable from publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, and downstream-use permission.

A successful bare usable deployment package SHALL make agent role distinguishable from agent permission.

A successful bare usable deployment package SHALL make agent output distinguishable from governed meaning.

A successful bare usable deployment package SHALL make workflow completion distinguishable from downstream-use clearance.

A successful bare usable deployment package SHALL make backup existence distinguishable from recovery readiness.

A successful bare usable deployment package SHALL make copy, export, migration, synchronization, indexing, cache generation, embedding generation, search generation, graph generation, summary generation, or repository presence distinguishable from governed authority.

A successful bare usable deployment package SHOULD allow a future user to determine:

- what files exist;
- what files are required;
- what files are missing;
- what files are Draft;
- what files are Approved;
- what files are recommended;
- what files are optional;
- what folders or storage areas exist;
- what folders or storage areas are missing;
- what metadata expectations apply;
- what Object Identity expectations apply;
- what relationships apply;
- what Source References apply;
- what provenance applies;
- what Lifecycle State applies;
- what Authority Level applies;
- what Privacy Classification applies;
- what Validation State applies;
- what agents may do;
- what agents must not do;
- what workflows apply;
- what review remains required;
- what approval scope exists;
- what backup limits apply;
- what export limits apply;
- what migration limits apply;
- what synchronization limits apply;
- what indexing limits apply;
- what implementation limits apply;
- what downstream-use limits apply;
- what handoff context applies;
- what next step should occur.

A successful bare usable deployment package SHOULD support controlled use by one person, one machine, one repository, one vault, or one implementation-development context without requiring the entire mature system to be complete.

A successful bare usable deployment package MAY support broader use only where additional review, privacy review, licensing review, implementation review, publication review, export review, documentation review, and governance review have occurred.

A successful DEP-0001 file SHALL help prevent deployment drift.

Deployment drift occurs when incomplete setup, missing standards, missing folders, missing metadata, missing review, missing validation, missing handoff context, agent convenience, workflow convenience, implementation convenience, storage convenience, or user-interface convenience silently changes the meaning or use of The Brain Standard.

DEP-0001 succeeds when deployment drift can be identified, corrected, limited, escalated, or recorded before the package is copied, installed, reused, handed off, implemented, automated, exposed to agents, published, exported, migrated, synchronized, indexed, backed up, recovered, or used downstream.

A successful DEP-0001 file SHALL help prepare the next implementation step.

The next implementation step SHOULD be an implementation profile or deployment-support document that explains how a specific tool environment realizes the standard in practice.

Where Obsidian and Codex are the next target environment, the next implementation step SHOULD be:

- IMP-0001 — Obsidian and Codex Implementation Profile.

DEP-0001 success does not mean IMP-0001 is complete.

DEP-0001 success means the standard package is ready enough for IMP-0001 to be created without forcing Obsidian, Codex, local AI, repository behavior, scripts, plugins, templates, prompts, validators, or automation to become the source of standard meaning.

DEP-0001 success does not mean the deployment package is mature.

DEP-0001 success does not mean the deployment package is publicly releasable.

DEP-0001 success does not mean all templates, prompts, validators, scripts, manifests, README files, indexes, or implementation-support files are complete.

DEP-0001 success means the package has crossed the minimum governed threshold for controlled bare usable deployment.

DEP-0001 is successful when a future human, agent, workflow, validator, repository, vault, implementation profile, or downstream user can inspect the deployment package and determine whether it is Not Ready, Draft, Limited-Use, Bare Usable, or ready to proceed toward implementation profiling.

## 17. Closing Rule

A Brain deployment package MUST NOT be treated as bare usable unless it satisfies DEP-0001 within a defined scope.

Deployment readiness MUST remain explicit.

Deployment readiness MUST remain reviewable.

Deployment readiness MUST remain limited to the scope actually reviewed.

A file, folder, vault, repository, archive, backup, export, migration package, synchronized copy, implementation profile, agent output, generated index, generated cache, generated embedding, graph view, search result, generated summary, checklist, handoff summary, manifest, README, script, prompt, plugin, model output, or automation result MUST NOT be treated as deployment approval by itself.

Bare usable deployment approval requires a scoped readiness finding.

A scoped readiness finding SHOULD identify:

- what package was reviewed;
- what files were included;
- what folders were included;
- what standards were included;
- what files remain Draft;
- what files remain incomplete;
- what required files are missing;
- what recommended files are missing;
- what limitations apply;
- what non-conformance remains;
- what corrective routing applies;
- what use is permitted;
- what use is excluded;
- what review remains required;
- what validation remains required;
- what agent limits apply;
- what workflow limits apply;
- what implementation limits apply;
- what publication limits apply;
- what export limits apply;
- what migration limits apply;
- what downstream-use limits apply;
- what next milestone should occur.

A deployment package MAY be approved for limited use before full implementation readiness.

Limited use MUST be explicit.

Limited use MUST be traceable.

Limited use MUST identify the allowed scope.

Limited use MUST identify excluded use.

Limited use MUST NOT conceal missing files, Draft files, missing folders, missing metadata, unresolved privacy issues, unresolved validation issues, unresolved source-reference issues, unresolved provenance issues, unresolved relationship issues, unresolved agent issues, unresolved workflow issues, unresolved implementation issues, unresolved backup issues, unresolved export issues, unresolved migration issues, unresolved downstream-use issues, or unresolved governance issues.

A deployment package MUST NOT be expanded from limited use to broader use without review.

A deployment package MUST NOT be treated as public-release ready merely because it is bare usable.

A deployment package MUST NOT be treated as implementation-ready merely because it is bare usable.

A deployment package MUST NOT be treated as agent-ready unless agent readiness has been reviewed within the relevant scope.

A deployment package MUST NOT be treated as workflow-ready unless workflow readiness has been reviewed within the relevant scope.

A deployment package MUST NOT be treated as validation-ready unless validation readiness has been reviewed within the relevant scope.

A deployment package MUST NOT be treated as export-ready unless export readiness has been reviewed within the relevant scope.

A deployment package MUST NOT be treated as migration-ready unless migration readiness has been reviewed within the relevant scope.

A deployment package MUST NOT be treated as backup-ready unless backup readiness has been reviewed within the relevant scope.

A deployment package MUST NOT be treated as downstream-use ready unless downstream-use readiness has been reviewed within the relevant scope.

The closing rule of DEP-0001 is:

The Brain may proceed to bare usable deployment only when the minimum required standards, folder readiness, metadata readiness, Source Material readiness, Knowledge Record readiness, agent readiness, workflow readiness, validation readiness, review readiness, backup readiness, export readiness, implementation-profile readiness, manifest readiness, handoff readiness, and non-conformance routing are explicit enough for controlled use without architectural drift.

If this condition is not satisfied, the package SHALL remain Not Ready, Draft, Limited-Use, or otherwise restricted until corrected or explicitly approved within a limited scope.

## 18. Milestone Completion and Handoff Boundary

DEP-0001 completes Milestone 5.1 when all required sections are drafted, reviewed, structurally valid, and aligned with the standards DEP-0001 depends on.

Milestone completion for DEP-0001 does not equal final approval by itself.

Milestone completion means the DEP-0001 draft has reached a complete section structure and is ready for full final review.

DEP-0001 contains 18 numbered sections:

1. Purpose
2. Relationship to Prior Standards
3. Deployment Scope and Boundaries
4. Minimum Deployment File Set
5. Required Folder and Layout Readiness
6. Metadata and Governed Document Readiness
7. Knowledge Record and Source Material Readiness
8. Agent and Workflow Readiness
9. Validation, Review, and Approval Readiness
10. Backup, Recovery, Export, and Copy Readiness
11. Implementation Profile Readiness
12. Deployment Package Manifest and Handoff Readiness
13. Non-Conformance, Gaps, and Corrective Routing
14. Deployment Conformance Requirements
15. Bare Usable Deployment Checklist
16. Success Criteria
17. Closing Rule
18. Milestone Completion and Handoff Boundary

Before DEP-0001 may be treated as complete, the full file SHOULD receive a final review for:

- document metadata correctness;
- dependency correctness;
- related-file correctness;
- Markdown syntax correctness;
- heading structure correctness;
- section sequence correctness;
- spelling and grammar;
- standard-boundary preservation;
- redundancy risk;
- conflict with higher-authority standards;
- conflict with Knowledge Standards;
- conflict with Storage Standards;
- conflict with Agent Standards;
- conflict with Workflow Standards;
- implementation-specific leakage;
- deployment-readiness clarity;
- checklist usability;
- handoff readiness.

If the final review passes, DEP-0001 MAY be marked ready for approval review.

If the approval review passes, DEP-0001 MAY be updated from Draft to Approved through the applicable governance process.

DEP-0001 approval SHOULD indicate that The Brain Standard has enough deployment-readiness structure to proceed toward controlled bare usable deployment.

DEP-0001 approval SHOULD NOT be interpreted as approval of public release.

DEP-0001 approval SHOULD NOT be interpreted as approval of a specific implementation.

DEP-0001 approval SHOULD NOT be interpreted as completion of IMP-0001.

DEP-0001 approval SHOULD NOT be interpreted as completion of templates, prompts, validators, scripts, manifests, README files, operational guides, local setup files, repository automation, vault configuration, or tool-specific deployment instructions.

After DEP-0001 is complete, the next recommended milestone SHOULD be creation of the first implementation profile or deployment-support package.

Where the next implementation target is Obsidian and Codex, the next recommended file SHOULD be:

- IMP-0001 — Obsidian and Codex Implementation Profile.

IMP-0001 SHOULD define how Obsidian and Codex realize The Brain Standard in practice without redefining the standard.

A handoff summary SHOULD be created after final review passes and before moving into IMP-0001 or implementation-package creation.

The handoff summary SHOULD identify:

- what DEP-0001 completed;
- what standards DEP-0001 depends on;
- how DEP-0001 prevents deployment drift;
- what sections DEP-0001 contains;
- what files were reviewed;
- what GitHub comparison found;
- what corrections were made;
- what risks remain;
- what approval step remains;
- what repository step remains;
- what folder step remains;
- what implementation step comes next.

The handoff boundary for DEP-0001 is the transition from standard-level deployment readiness to implementation-profile creation.

The handoff boundary MUST NOT be used to skip final review.

The handoff boundary MUST NOT be used to skip approval review.

The handoff boundary MUST NOT be used to convert Draft status into Approved status.

The handoff boundary MUST NOT be used to treat DEP-0001 as an implementation profile.

The handoff boundary MUST NOT be used to treat IMP-0001 as already complete.

The handoff boundary MUST NOT authorize public release, unrestricted export, unrestricted publication, unrestricted synchronization, unrestricted indexing, unrestricted agent exposure, unrestricted downstream use, or unrestricted implementation deployment.

Milestone 5.1 is ready to close when DEP-0001 passes final review, receives the appropriate approval decision, and has a handoff summary prepared for the next implementation-profile milestone.