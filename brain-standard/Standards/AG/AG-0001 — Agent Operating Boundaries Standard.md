# AG-0001 — Agent Operating Boundaries Standard

Document ID: AG-0001
Title: Agent Operating Boundaries Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 3 — Agent Framework
Milestone: 3.1 — Agent Operating Boundaries Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and agent-operating-boundary rules are interpreted within AG-0001.

Where conflicts arise between agent behavior, agent permissions, agent access, agent outputs, agent-generated changes, agent confidence, agent memory, agent tools, workflow execution, storage behavior, implementation behavior, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, import behavior, export behavior, migration behavior, publication behavior, deletion behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

AG-0001 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

AG-0001 depends on the Phase 1 Knowledge Standards because agents must preserve knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation.

AG-0001 depends on the Phase 2 Storage Standards because agents may need to locate, read, classify, propose, move, preserve, validate, import, export, archive, or organize stored material without allowing storage placement to define knowledge meaning.

AG-0001 defines agent operating boundaries at the conceptual standard level.

AG-0001 does not define exact prompts, exact model behavior, exact agent frameworks, exact tool APIs, exact runtime environments, exact permissions files, exact automation scripts, exact implementation-specific agent roles, exact workflow procedures, exact validation tooling, exact storage paths, or exact user-interface behavior.

Those concerns belong to later agent specifications, workflow standards, implementation profiles, operational guides, tool-specific setup documents, permission profiles, validation specifications, and reference implementations.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Agent Framework refers to Layer 3 of The Brain Standard, responsible for defining how agents may interact with knowledge, source material, storage structures, workflow instructions, and implementation environments while preserving reviewability, traceability, privacy, and governance.
- Agent refers to a human-directed or system-directed AI, automation, script, model-driven process, tool-using assistant, workflow participant, or future automated actor that reads, classifies, summarizes, extracts, proposes, validates, drafts, moves, edits, creates, deletes, exports, publishes, migrates, or otherwise acts on governed material.
- Agent Activity refers to any action, recommendation, classification, extraction, validation, summary, draft, change, movement, deletion, export, publication, migration, or decision-support output produced or assisted by an agent.
- Agent Operation refers to a specific action performed by an agent within a governed scope.
- Agent Boundary refers to a rule, permission, prohibition, scope limit, review requirement, privacy constraint, authority limit, validation requirement, workflow dependency, or governance expectation that controls agent behavior.
- Agent Permission refers to an allowed agent capability within a defined scope.
- Agent Access refers to an agent’s ability to read, inspect, search, summarize, extract, index, classify, modify, move, copy, export, publish, delete, migrate, or otherwise interact with a governed entity.
- Agent Output refers to a result produced by an agent, including a summary, classification, proposed metadata, proposed relationship, validation result, draft record, proposed edit, file movement recommendation, warning, report, transformation, or generated content.
- Agent-Generated Change refers to any proposed or applied change created, recommended, assisted, or executed by an agent.
- Agent Confidence refers to an agent-generated indication of certainty, probability, classification confidence, extraction confidence, validation confidence, relationship confidence, recommendation confidence, or model confidence.
- Human Review refers to review, correction, acceptance, rejection, approval, or escalation performed by an authorized human.
- Escalation refers to routing a condition, ambiguity, risk, conflict, privacy concern, authority concern, validation issue, destructive action, or critical knowledge change to human review or a governed workflow.
- Critical Knowledge Change refers to a change that affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, governed meaning, publication, export, migration, deletion, supersession, deprecation, or downstream use.
- Governed Entity refers to a Knowledge Object, Knowledge Record, Source Material, Source Reference, provenance record, relationship, metadata record, validation result, lifecycle state, authority assignment, privacy classification, governed document, workflow output, agent output, import record, export record, migration record, decision, or other entity governed by The Brain Standard.
- Read Operation refers to an agent activity that inspects, searches, opens, parses, indexes, summarizes, extracts from, or otherwise consumes governed material without modifying the governed entity.
- Write Operation refers to an agent activity that creates, edits, rewrites, annotates, modifies, enriches, replaces, restructures, or records governed material.
- Move Operation refers to an agent activity that changes the storage location of a file, record, source artifact, draft, archive item, implementation file, export, import, migration package, or other stored representation.
- Delete Operation refers to an agent activity that removes, trashes, discards, erases, overwrites, purges, or otherwise makes a governed entity or storage representation unavailable.
- Export Operation refers to an agent activity that produces governed material, source material, metadata, relationships, Source References, provenance, validation results, or implementation artifacts for use outside the current compliant environment.
- Publication Operation refers to an agent activity that makes governed material available beyond its prior privacy, authority, review, or implementation boundary.
- Migration Operation refers to an agent activity that moves, converts, maps, transforms, packages, validates, or preserves governed material across storage systems, implementations, representations, schemas, vaults, repositories, or file formats.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of AG-0001 is to define the standard-level operating boundaries for agents within The Brain Standard.

AG-0001 establishes what agents may do, what agents must not do, what agent activity must preserve, when agent activity must remain reviewable, and when agent activity must be escalated to a human or governed workflow.

The Agent Framework exists to make automation useful without allowing agents to become unreviewable authorities over knowledge.

Agents may assist with knowledge work.

Agents do not own knowledge meaning.

Agents may support storage organization.

Agents do not define storage meaning.

Agents may participate in workflows.

Agents do not replace governance unless a future governed workflow explicitly grants a limited and reviewable authority.

Agents may operate within implementations.

Agents do not make any implementation, model, prompt system, plugin, runtime, or tool the standard itself.

AG-0001 exists to prevent agent authority creep.

Agent authority creep occurs when agent behavior, agent confidence, agent memory, agent output, workflow convenience, implementation defaults, or repeated automation begins to redefine knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage meaning, publication status, export permission, migration behavior, or governance without explicit review and approval.

AG-0001 defines agent operating boundaries for:

- reading governed material;
- searching governed material;
- classifying governed material;
- summarizing governed material;
- extracting metadata;
- proposing metadata;
- proposing relationships;
- proposing Source References;
- proposing provenance records;
- proposing lifecycle states;
- proposing authority levels;
- proposing privacy classifications;
- performing validation checks;
- drafting Knowledge Records;
- drafting governed documents;
- moving stored material;
- editing governed material;
- creating governed material;
- deleting stored material;
- exporting governed material;
- publishing governed material;
- migrating governed material;
- escalating ambiguity, risk, conflict, or destructive action;
- preserving traceability;
- preserving human reviewability;
- preserving implementation independence.

AG-0001 does not define exact prompts, exact agent names, exact agent personas, exact model providers, exact tools, exact runtime permissions, exact file paths, exact automation scripts, exact workflow steps, exact validation rules, exact metadata fields, exact storage layouts, exact user-interface behavior, or exact implementation-specific setup.

Those concerns belong to later agent specifications, workflow standards, implementation documents, operational guides, permission profiles, validation specifications, templates, and reference implementations.

The primary purpose of AG-0001 is to ensure that agents can reduce cognitive load, improve knowledge quality, support automation, and assist with maintenance without weakening knowledge meaning, source traceability, privacy boundaries, authority control, lifecycle handling, validation expectations, storage boundaries, human reviewability, governance, or implementation independence.

AG-0001 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine:

- what an agent is allowed to do;
- what an agent is prohibited from doing;
- what scope an agent may operate within;
- what source material, Knowledge Records, metadata, relationships, provenance, lifecycle states, authority levels, privacy classifications, validation results, storage areas, workflow instructions, and implementation files an agent may access;
- whether an agent action is read-only, proposed, applied, destructive, privacy-sensitive, authority-sensitive, publication-sensitive, export-sensitive, or migration-sensitive;
- whether human review is required before an agent output may affect governed meaning;
- whether a workflow explicitly authorizes an agent action;
- whether agent activity has sufficient traceability;
- whether agent output has been confused with approval, authority, truth, validation, lifecycle transition, privacy permission, publication permission, export permission, or governance;
- whether agent behavior remains valid when implementations, storage systems, model providers, tools, prompts, plugins, or automation frameworks change.

## 2. Relationship to Prior Standards

AG-0001 is subordinate to and derived from the constitutional foundation of The Brain Standard.

AG-0001 depends on:

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
- SS-0002 — Storage Layout Specification.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

AG-0001 applies that purpose by allowing agents to assist with knowledge work while preserving The Brain as a standard rather than a tool-specific, model-specific, or automation-specific system.

TB-0001 establishes the architecture principles that govern The Brain Standard.

AG-0001 applies those principles by requiring agent activity to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- source distinction;
- provenance;
- privacy boundaries;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability;
- governed evolution.

TB-0002 establishes the layered architecture of The Brain Standard.

AG-0001 belongs to Layer 3 — Agent Framework.

Layer 3 depends on Layer 1 and Layer 2.

AG-0001 depends on Layer 1 because agents must understand Knowledge Objects, Knowledge Records, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, and governed meaning.

AG-0001 depends on Layer 2 because agents may need to locate, read, reference, classify, move, preserve, validate, import, export, archive, or organize governed material within a storage environment.

AG-0001 MUST NOT allow Layer 3 agent behavior to redefine Layer 1 knowledge meaning or Layer 2 storage meaning.

AG-0001 MUST NOT create a circular dependency where knowledge meaning depends on agent output, storage meaning depends on agent behavior, workflow authority depends on agent confidence, or implementation compliance depends on a specific agent system.

TB-0003 establishes the governance model for The Brain Standard.

AG-0001 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, AG-0001 has high authority within its scope but remains subordinate to constitutional documents.

AG-0001 may define required and recommended behavior for agent boundaries, permissions, access, traceability, escalation, reviewability, and prohibited operations.

AG-0001 MUST NOT contradict constitutional documents.

KS-0001 defines the foundational Knowledge Object Model.

AG-0001 depends on KS-0001 because agents may interact with Knowledge Objects and Knowledge Records but must not confuse source material, files, notes, folders, storage paths, application records, drafts, or agent outputs with governed knowledge meaning.

An agent MAY create or propose a Knowledge Record.

An agent MUST NOT cause a Knowledge Record to become approved, authoritative, published, exportable, or valid merely because the agent created it.

KS-0002 defines Object Identity.

AG-0001 depends on KS-0002 because agent activity must preserve stable Object Identity across reading, editing, moving, copying, deduplication, import, export, migration, validation, and implementation replacement.

An agent MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity unless a governed workflow or future specification explicitly permits that operation within a defined scope.

KS-0003 defines metadata behavior.

AG-0001 depends on KS-0003 because agents may extract, propose, classify, enrich, validate, or update metadata.

Agent-generated metadata SHOULD remain reviewable where metadata affects meaning, Object Identity, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, publication, export, migration, or downstream use.

KS-0004 defines relationship behavior.

AG-0001 depends on KS-0004 because agents may propose, infer, validate, repair, enrich, or flag relationships.

An agent-generated relationship MUST remain distinguishable from a human-reviewed or approved relationship unless a governed workflow or future specification explicitly defines automatic approval for a limited relationship type.

KS-0005 defines Source Reference and Provenance behavior.

AG-0001 depends on KS-0005 because agents may extract from Source Material, summarize source content, propose Source References, create provenance notes, or transform source-derived knowledge.

Agent activity SHOULD preserve provenance sufficient to identify the responsible agent, instruction, source material, transformation, output, and review state where those affect interpretation, authority, privacy, validation, publication, export, migration, or downstream use.

KS-0006 defines Lifecycle State behavior.

AG-0001 depends on KS-0006 because agents may propose lifecycle states, route items for review, flag items as needing repair, or identify deprecated, superseded, archived, restricted, quarantined, pending-review, or pending-validation material.

An agent MUST NOT approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, or transition lifecycle state as a final governed action unless a future governed workflow or specification explicitly permits that behavior within a defined scope.

KS-0007 defines Authority Level behavior.

AG-0001 depends on KS-0007 because agents may propose, classify, validate, or recommend authority-related information.

Agent confidence MUST NOT be treated as Authority Level.

Agent output MUST NOT become authoritative merely because it is plausible, repeated, validated by a tool, generated by a preferred model, produced by a workflow, or surfaced by an implementation.

KS-0008 defines Privacy Classification behavior.

AG-0001 depends on KS-0008 because agents may access, summarize, classify, index, route, export, publish, or expose privacy-sensitive material.

An agent MUST NOT access, summarize, expose, synchronize, publish, export, or migrate restricted material unless the relevant Privacy Classification, permission boundary, and governed workflow allow that operation.

KS-0009 defines Validation behavior.

AG-0001 depends on KS-0009 because agents may perform or support validation.

Agent-generated validation MUST remain distinguishable from approval, authority, truth, privacy permission, lifecycle transition, publication permission, export permission, migration permission, or governance acceptance unless a future governed workflow or specification explicitly defines that result.

SS-0001 defines storage architecture.

AG-0001 depends on SS-0001 because agents may interact with storage environments, vaults, repositories, folders, files, archives, backups, imports, exports, migrations, indexes, caches, and generated files without allowing storage placement or agent movement to redefine knowledge meaning.

SS-0002 defines the practical Storage Layout.

AG-0001 depends on SS-0002 because agents may need to operate across Source Material, Knowledge Records, governed documents, drafts, reviews, working areas, implementation support areas, workflow support areas, assets, indexes, caches, generated files, archives, backups, imports, exports, and migration areas while preserving the boundaries assigned to each area.

AG-0001 is successful when it extends the prior standards into a clear agent-boundary model without weakening Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage architecture, storage layout, governance, implementation independence, or practical daily usability.

## 3. Agent Scope and Boundaries

Agent scope defines the governed range within which an agent may operate.

Agent boundaries define the rules that limit what an agent may access, change, infer, propose, validate, move, delete, export, publish, migrate, or escalate.

An agent’s scope SHOULD be explicit before the agent acts where the action may affect governed material.

An agent scope MAY include:

- a specific task;
- a specific Knowledge Object;
- a specific Knowledge Record;
- a specific Source Material set;
- a specific storage area;
- a specific workflow stage;
- a specific validation scope;
- a specific import package;
- a specific export package;
- a specific migration package;
- a specific implementation environment;
- a specific privacy boundary;
- a specific authority boundary;
- a specific review boundary;
- another governed scope.

An agent MUST operate only within the scope authorized by the user, workflow, implementation profile, permission model, or governed standard.

An agent MUST NOT treat access to a file, folder, repository, vault, database, chat context, tool, plugin, model memory, index, cache, search result, or implementation environment as permission to perform all possible actions on that material.

Access is not authority.

Visibility is not permission.

Searchability is not permission.

Agent confidence is not authority.

Tool capability is not governance.

Workflow completion is not approval unless a governed workflow explicitly defines that result.

### 3.1 Read Boundaries

An agent MAY read, inspect, search, parse, summarize, extract from, or classify governed material when the task scope, privacy classification, workflow, and permission model allow read access.

A read operation SHOULD preserve source distinction.

An agent MUST NOT confuse Source Material with a Knowledge Record merely because the agent can read both.

An agent MUST NOT expose restricted knowledge through summaries, extracted metadata, search results, embeddings, logs, prompts, caches, generated files, exports, or implementation outputs unless the relevant Privacy Classification permits that exposure.

A read operation SHOULD remain traceable where the result affects metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, or downstream use.

### 3.2 Proposal Boundaries

An agent MAY propose classifications, summaries, metadata, relationships, Source References, provenance notes, lifecycle states, authority notes, privacy classifications, validation findings, file movements, repairs, drafts, or workflow actions.

Agent proposals SHOULD remain distinguishable from approved governed changes.

An agent proposal MUST NOT become a governed fact, approved Knowledge Record, approved relationship, approved lifecycle transition, assigned Authority Level, assigned Privacy Classification, validation approval, publication approval, export approval, migration approval, or deletion approval unless a human or governed workflow accepts it according to the applicable standard.

An agent MAY identify ambiguity, inconsistency, missing metadata, broken relationships, privacy risk, validation failure, duplicate risk, source-reference issue, provenance gap, lifecycle issue, authority conflict, storage-placement issue, or implementation incompatibility.

An agent SHOULD escalate issues that affect governed meaning, privacy, authority, validation, lifecycle state, publication, export, migration, deletion, or downstream use.

### 3.3 Write Boundaries

An agent MAY create, edit, annotate, enrich, restructure, or draft governed material only when the action is within an authorized scope.

Agent-generated writing SHOULD remain distinguishable from human-authored, human-reviewed, approved, or authoritative material where that distinction affects meaning, provenance, lifecycle state, authority, privacy, validation, publication, export, migration, or downstream use.

An agent MUST preserve Object Identity when editing or moving a Knowledge Record unless a governed identity-change process explicitly permits a change.

An agent MUST NOT silently overwrite, replace, delete, supersede, deprecate, publish, export, migrate, declassify, approve, reject, or reinterpret governed material when the action affects meaning, identity, provenance, lifecycle state, authority, privacy, validation, source traceability, relationships, compatibility, or governance.

Agent-generated changes SHOULD preserve sufficient provenance to identify:

- what changed;
- what agent performed or proposed the change;
- what instruction, task, workflow, or tool was involved;
- what source material or governed entity was used;
- what review state applies;
- whether the change was proposed, applied, rejected, reverted, superseded, or approved.

### 3.4 Move and Organization Boundaries

An agent MAY recommend or perform storage movement only when the movement is allowed by the applicable storage standard, layout specification, workflow, permission model, and privacy boundary.

An agent MUST NOT treat folder movement as a change in Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, or governed meaning.

An agent MUST NOT use folder placement, filename, tag, index location, cache location, generated-file location, archive location, backup location, import location, export location, migration location, or implementation workspace as the sole source of governed meaning.

An agent SHOULD preserve Source References, provenance, relationships, metadata, lifecycle state, authority level, privacy classification, validation expectations, and compatibility context when moving, copying, archiving, importing, exporting, or migrating stored material.

### 3.5 Destructive Action Boundaries

Delete operations are high-risk agent operations.

An agent MUST NOT permanently delete, purge, overwrite, discard, or make unavailable governed material unless a future governed workflow or specification explicitly permits that operation within a defined scope.

An agent MAY recommend deletion, quarantine, archival, repair, deprecation, supersession, or cleanup where appropriate.

An agent SHOULD escalate destructive actions to human review unless the operation is explicitly defined as safe, reversible, limited, and governed.

An agent MUST NOT delete Source Material, Knowledge Records, governed documents, provenance records, relationship records, validation records, imports, exports, migrations, archives, or backups where deletion would break source traceability, provenance, compatibility, auditability, privacy protection, recovery, or governance.

### 3.6 Export, Publication, and Migration Boundaries

Export, publication, and migration operations are high-risk agent operations.

An agent MUST NOT export, publish, synchronize, transmit, expose, migrate, or package governed material beyond its current environment unless the relevant Privacy Classification, Authority Level, Lifecycle State, Validation State, workflow, permission model, and governance expectations allow that action.

An agent MAY prepare export packages, publication drafts, migration mappings, compatibility reports, or validation reports.

Prepared outputs SHOULD remain pending review unless a future governed workflow explicitly permits automatic completion for a limited and well-defined operation.

An agent MUST preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage context, and compatibility expectations during export, publication, or migration where those affect interpretation or downstream use.

### 3.7 Authority and Review Boundaries

An agent MAY support review.

An agent MAY recommend approval, rejection, repair, deprecation, supersession, quarantine, restriction, publication, export, migration, or escalation.

An agent MUST NOT become the final authority for constitutional meaning, governed standards, critical knowledge revisions, privacy boundaries, authority assignment, lifecycle transitions, validation acceptance, publication approval, export approval, migration approval, or destructive actions unless explicitly authorized by a higher-authority governance process or future governed workflow within a defined scope.

Human review SHALL remain available for critical knowledge changes.

Agent activity SHOULD remain traceable, inspectable, reversible where practical, and bounded by the applicable standard, specification, workflow, permission model, privacy classification, and governance process.

AG-0001 preserves the following operating rule:

Agents may assist, propose, draft, validate, organize, and execute bounded workflow steps.

Agents must not silently govern.

## 4. Agent Permission Model

The Agent Permission Model defines how agent capabilities are granted, limited, interpreted, reviewed, and revoked within The Brain Standard.

Agent permissions exist so that agents can perform useful work without gaining uncontrolled access, hidden authority, or implementation-defined power over governed material.

An Agent Permission SHALL be explicit where agent activity affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, workflow behavior, publication, export, migration, deletion, or downstream use.

An Agent Permission MAY allow an agent to:

- read governed material;
- search governed material;
- summarize governed material;
- extract information from governed material;
- classify governed material;
- propose metadata;
- propose relationships;
- propose Source References;
- propose provenance records;
- propose lifecycle states;
- propose authority-related handling;
- propose privacy classifications;
- perform validation checks;
- draft records or documents;
- recommend storage movement;
- perform bounded storage movement;
- prepare import, export, or migration material;
- prepare review reports;
- escalate issues;
- perform other governed operations defined by a future specification or workflow.

An Agent Permission MUST NOT be interpreted as broader than its defined scope.

Agent permissions are successful when future humans, agents, workflows, validators, storage systems, and implementations can determine what an agent was allowed to do, what the agent actually did, what scope applied, what review was required, and whether the permission remained valid.

### 4.1 Permission Scope

Permission Scope defines the range within which an Agent Permission applies.

Permission Scope MAY be limited by:

- task;
- governed entity;
- Knowledge Object;
- Knowledge Record;
- Source Material set;
- storage area;
- workflow stage;
- implementation environment;
- privacy classification;
- authority scope;
- lifecycle state;
- validation scope;
- import package;
- export package;
- migration package;
- time period;
- responsible human;
- future governed permission boundary.

An agent MUST NOT treat permission in one scope as permission in every scope.

Permission to read one Knowledge Record does not imply permission to read all Knowledge Records.

Permission to summarize Source Material does not imply permission to approve a Knowledge Record.

Permission to propose metadata does not imply permission to modify governed metadata.

Permission to validate structure does not imply permission to approve content.

Permission to prepare an export does not imply permission to release the export.

Permission to move a draft does not imply permission to move approved governed material.

Permission Scope SHOULD be recorded or inferable where the agent activity affects interpretation, privacy, authority, lifecycle handling, validation, publication, export, migration, deletion, or downstream use.

### 4.2 Permission Categories

Agent permissions SHOULD be categorized by operational risk.

At minimum, The Brain Standard recognizes the following Agent Permission Categories:

- read permissions;
- search permissions;
- extraction permissions;
- summarization permissions;
- classification permissions;
- proposal permissions;
- validation-support permissions;
- drafting permissions;
- write permissions;
- move permissions;
- import-preparation permissions;
- export-preparation permissions;
- migration-preparation permissions;
- publication-preparation permissions;
- destructive-action permissions;
- escalation permissions.

Read, search, extraction, summarization, classification, proposal, validation-support, drafting, and escalation permissions MAY be lower-risk when they remain bounded, privacy-respecting, and reviewable.

Write, move, import, export, migration, publication, and destructive-action permissions SHOULD be treated as higher-risk where they affect governed meaning, privacy, authority, lifecycle state, validation, source traceability, compatibility, or downstream use.

A future agent specification MAY define exact permission categories, permission levels, permission fields, permission inheritance rules, permission logging requirements, or permission validation rules.

Such specifications are valid only when they preserve the boundaries defined by AG-0001.

### 4.3 Permission Sources

An Agent Permission MAY originate from:

- a human instruction;
- a governed workflow;
- a governed implementation profile;
- a future agent specification;
- a permission profile;
- a validation process;
- a migration process;
- an import process;
- an export process;
- a publication process;
- another governed mechanism.

A tool capability is not a Permission Source by itself.

A model capability is not a Permission Source by itself.

A plugin capability is not a Permission Source by itself.

A file-system permission is not a governed Agent Permission by itself.

A search result is not a governed Agent Permission by itself.

An implementation default is not a governed Agent Permission by itself.

A repeated agent behavior is not a governed Agent Permission by itself.

Where a human instruction conflicts with a higher-authority standard, privacy boundary, lifecycle state, validation expectation, authority rule, workflow rule, or implementation boundary, the higher-authority governed rule SHALL guide interpretation unless formally revised through governance.

### 4.4 Permission Non-Inheritance

Agent permissions SHOULD NOT silently inherit across scopes.

Permission to access one storage area MUST NOT imply permission to access all storage areas.

Permission to work on Source Material MUST NOT imply permission to modify Knowledge Records.

Permission to work on drafts MUST NOT imply permission to modify approved material.

Permission to inspect restricted material MUST NOT imply permission to summarize, expose, export, publish, index, embed, cache, migrate, or use that restricted material downstream.

Permission to prepare a change MUST NOT imply permission to apply the change.

Permission to apply a reversible change MUST NOT imply permission to perform an irreversible change.

Permission to propose approval MUST NOT imply permission to approve.

Permission to propose deletion MUST NOT imply permission to delete.

Permission inheritance MAY be defined by a future governed workflow, permission profile, implementation profile, or agent specification.

Any such inheritance MUST remain explicit, reviewable, privacy-respecting, and subordinate to higher-authority standards.

### 4.5 Read Permissions

Read Permissions allow an agent to inspect, search, parse, summarize, extract from, classify, or otherwise consume governed material without directly modifying it.

Read Permissions SHALL respect Privacy Classification.

An agent MUST NOT read restricted material unless the applicable privacy boundary permits agent access within the defined scope.

An agent MUST NOT expose restricted content through summaries, extraction results, logs, prompts, embeddings, caches, indexes, reports, exports, generated files, implementation displays, or downstream outputs unless permitted.

Read Permissions SHOULD preserve source distinction.

Read Permissions SHOULD preserve enough provenance to determine what material was read where the resulting output affects interpretation, metadata, relationships, Source References, lifecycle state, authority, privacy, validation, publication, export, migration, or downstream use.

### 4.6 Proposal Permissions

Proposal Permissions allow an agent to recommend, suggest, draft, classify, identify, flag, or prepare a possible governed action without making that action final.

An agent MAY propose:

- metadata;
- relationships;
- Source References;
- provenance records;
- lifecycle states;
- authority-related handling;
- privacy classifications;
- validation findings;
- repairs;
- drafts;
- storage movement;
- import mappings;
- export packages;
- migration mappings;
- publication drafts;
- escalation actions;
- future governed actions.

A proposal MUST remain distinguishable from an approved governed change.

An agent proposal MUST NOT silently become a final decision, approval, lifecycle transition, Authority Level assignment, Privacy Classification assignment, validation acceptance, publication approval, export approval, migration approval, deletion approval, or governance action.

Proposal Permissions SHOULD support human review.

### 4.7 Write Permissions

Write Permissions allow an agent to create, edit, annotate, enrich, rewrite, restructure, or record governed material within an authorized scope.

Write Permissions are higher-risk than Read Permissions or Proposal Permissions.

An agent MUST NOT write to governed material unless the action is authorized by the applicable user instruction, workflow, permission model, implementation profile, or future governed specification.

An agent-generated write operation SHOULD preserve provenance where the change affects meaning, Object Identity, metadata, relationships, Source References, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, or downstream use.

An agent MUST NOT silently overwrite human-reviewed, approved, authoritative, restricted, archived, superseded, deprecated, or validation-sensitive material.

Where a write operation affects governed meaning, the change SHOULD remain reviewable and reversible where practical.

### 4.8 Move Permissions

Move Permissions allow an agent to change the storage location of a stored representation within a defined scope.

Move Permissions MUST preserve Object Identity.

Move Permissions MUST preserve the distinction between Source Material, Knowledge Records, governed documents, drafts, reviews, working material, implementation-support material, workflow-support material, assets, indexes, caches, generated files, archives, backups, imports, exports, and migrations.

An agent MUST NOT treat movement as a change in knowledge meaning.

An agent MUST NOT treat movement as approval, rejection, deprecation, supersession, archival, restriction, validation success, Authority Level assignment, Privacy Classification assignment, publication, export, migration, or deletion.

Move Permissions SHOULD preserve or update references where movement affects discoverability, Source References, provenance, validation, compatibility, backups, archives, imports, exports, migrations, or implementation behavior.

### 4.9 High-Risk Permissions

High-risk permissions include agent permissions that may affect:

- Object Identity;
- governed metadata;
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
- archival;
- backup;
- synchronization;
- indexing;
- implementation exposure;
- downstream use.

High-risk permissions SHOULD require explicit scope.

High-risk permissions SHOULD require human review, governed workflow authorization, or both.

A future governed workflow MAY allow limited automatic execution of high-risk operations only when the operation is reversible, bounded, validated, privacy-respecting, traceable, and compatible with higher-authority standards.

### 4.10 Permission Review and Revocation

Agent permissions SHOULD be reviewable.

A reviewer SHOULD be able to determine:

- what permission was granted;
- who or what granted the permission where applicable;
- what scope applied;
- what governed entities were affected;
- what agent activity occurred;
- whether the activity stayed within scope;
- what privacy boundary applied;
- what authority boundary applied;
- what lifecycle state applied;
- what validation scope applied;
- what output was produced;
- whether the output was proposed, applied, rejected, reverted, escalated, or approved.

Agent permissions MAY be revoked, narrowed, suspended, superseded, deprecated, or replaced by a governed process.

An agent MUST NOT continue operating under a revoked, expired, superseded, rejected, or invalid permission.

Permission review is successful when humans, agents, workflows, validators, and implementations can determine whether an agent acted within authorized boundaries and whether corrective action is required.

## 5. Allowed Agent Operations

Allowed Agent Operations define what agents may do when authorized by the applicable scope, permission model, privacy boundary, workflow, implementation profile, validation expectation, and governance process.

An operation is allowed only within its defined scope.

An allowed operation MUST remain subordinate to Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage architecture, storage layout, workflow boundaries, governance, and implementation independence.

An allowed operation MUST NOT become unrestricted merely because it is useful, convenient, automated, technically possible, repeated, model-generated, workflow-supported, or implementation-supported.

Allowed Agent Operations are successful when agents can reduce workload, improve consistency, support review, and assist with automation without silently governing.

### 5.1 Reading and Searching

An agent MAY read and search governed material where read access is permitted.

Reading and searching MAY support:

- discovery;
- review preparation;
- source inspection;
- metadata inspection;
- relationship inspection;
- validation support;
- duplicate detection;
- source-reference checking;
- provenance checking;
- lifecycle review;
- authority review;
- privacy review;
- storage review;
- workflow routing;
- implementation support.

An agent MUST preserve privacy boundaries during reading and searching.

Searchability MUST NOT be treated as permission to expose, summarize, export, publish, index, embed, migrate, or use material downstream.

### 5.2 Summarization and Extraction

An agent MAY summarize or extract from governed material where permitted.

Summarization and extraction MAY support:

- source review;
- Knowledge Record drafting;
- metadata proposal;
- relationship proposal;
- provenance preparation;
- validation support;
- workflow routing;
- migration preparation;
- import review;
- export review;
- publication preparation.

An agent summary is not the source.

An agent extraction is not automatically complete.

An agent extraction is not automatically correct.

An agent summary MUST NOT replace Source Material, Source References, provenance, human review, validation, authority assignment, or privacy review where those are required.

Summaries and extractions SHOULD preserve enough source context for future review where they affect governed interpretation.

### 5.3 Classification and Metadata Proposal

An agent MAY classify governed material or propose metadata where permitted.

Classification and metadata proposal MAY include:

- object type suggestions;
- descriptive metadata suggestions;
- structural metadata suggestions;
- provenance metadata suggestions;
- relationship metadata suggestions;
- lifecycle metadata suggestions;
- authority metadata suggestions;
- privacy metadata suggestions;
- validation metadata suggestions;
- compatibility metadata suggestions;
- workflow metadata suggestions;
- implementation metadata suggestions.

Agent-generated metadata MUST remain distinguishable from approved governed metadata where that distinction affects interpretation, authority, privacy, lifecycle state, validation, publication, export, migration, or downstream use.

An agent MUST NOT make metadata authoritative merely by generating, repeating, ranking, validating, or displaying it.

### 5.4 Relationship Suggestion

An agent MAY suggest relationships where permitted.

Relationship suggestion MAY support:

- identifying related Knowledge Objects;
- identifying related Knowledge Records;
- identifying Source Material support;
- identifying possible duplicates;
- identifying dependency relationships;
- identifying supersession relationships;
- identifying contradiction or conflict;
- identifying missing links;
- identifying broken links;
- identifying relationship repair needs.

Agent-suggested relationships SHOULD remain proposed, inferred, uncertain, or pending review unless accepted through a governed process.

An agent MUST NOT silently create authoritative relationship meaning.

An agent MUST NOT rely only on filename similarity, folder proximity, tag similarity, backlink behavior, graph layout, search ranking, vector similarity, prompt context, model memory, or hidden implementation behavior where relationship meaning affects governed interpretation.

### 5.5 Source Reference and Provenance Assistance

An agent MAY assist with Source References and provenance where permitted.

Source Reference and provenance assistance MAY include:

- identifying possible Source Material;
- checking whether a Knowledge Record has source support;
- proposing Source References;
- identifying missing provenance;
- recording agent involvement;
- preparing extraction history;
- preparing transformation history;
- identifying source availability issues;
- identifying source reliability concerns;
- identifying source privacy concerns;
- identifying attribution gaps;
- identifying import, export, or migration provenance gaps.

An agent MUST NOT fabricate Source References.

An agent MUST NOT treat an unsupported claim as source-supported.

An agent MUST NOT erase or weaken provenance merely to simplify a record.

An agent SHOULD escalate source or provenance uncertainty where it affects meaning, authority, privacy, validation, publication, export, migration, or downstream use.

### 5.6 Validation Support

An agent MAY support validation where permitted.

Validation support MAY include:

- checking required structure;
- checking required metadata presence;
- checking Object Identity consistency;
- checking relationship structure;
- checking Source Reference presence;
- checking provenance presence;
- checking Lifecycle State presence;
- checking Authority Level presence;
- checking Privacy Classification presence;
- checking compatibility expectations;
- identifying validation errors;
- identifying validation warnings;
- recommending repair.

Agent validation support MUST remain distinguishable from final validation acceptance unless a future governed workflow or specification explicitly defines that behavior within a limited scope.

An agent-generated validation result MUST NOT silently create approval, authority, lifecycle transition, privacy clearance, publication permission, export permission, migration permission, or governance acceptance.

### 5.7 Drafting and Review Preparation

An agent MAY draft Knowledge Records, governed documents, review notes, repair notes, migration notes, export notes, publication drafts, or other governed material where permitted.

Agent-drafted material SHOULD remain clearly distinguishable from reviewed, approved, authoritative, published, exportable, or final governed material until accepted through the applicable process.

Drafting MAY support human review.

Drafting MUST NOT replace human review where human review is required.

An agent MAY prepare review summaries, issue lists, comparison notes, or conformance reports.

Review preparation MUST NOT be treated as review completion unless a governed workflow explicitly defines that behavior.

### 5.8 Organization and Storage Assistance

An agent MAY assist with storage organization where permitted.

Storage assistance MAY include:

- identifying misplaced material;
- recommending movement;
- identifying draft material;
- identifying review material;
- identifying Source Material;
- identifying Knowledge Records;
- identifying governed documents;
- identifying implementation-support material;
- identifying workflow-support material;
- identifying assets;
- identifying indexes, caches, and generated files;
- identifying archive candidates;
- identifying backup candidates;
- identifying import, export, or migration packages.

An agent MUST NOT allow storage placement to define knowledge meaning.

An agent MUST NOT treat folder movement as Object Identity change, lifecycle transition, authority assignment, privacy assignment, validation success, publication, export, migration, or deletion.

### 5.9 Import, Export, and Migration Preparation

An agent MAY prepare import, export, or migration work where permitted.

Preparation MAY include:

- mapping fields;
- comparing formats;
- identifying missing metadata;
- identifying relationship risks;
- identifying Source Reference risks;
- identifying provenance risks;
- identifying lifecycle risks;
- identifying authority risks;
- identifying privacy risks;
- identifying validation risks;
- identifying compatibility risks;
- preparing migration reports;
- preparing export packages for review;
- preparing import review notes.

Preparation is not completion.

An agent-prepared import, export, or migration package SHOULD remain pending review unless a future governed workflow explicitly permits automatic completion for a limited and controlled case.

### 5.10 Escalation and Risk Reporting

An agent MAY escalate issues where permitted or required.

Escalation MAY be required when an agent detects:

- identity conflict;
- duplicate risk;
- source uncertainty;
- provenance gap;
- relationship conflict;
- lifecycle ambiguity;
- authority conflict;
- privacy risk;
- validation failure;
- storage-placement issue;
- import risk;
- export risk;
- migration risk;
- publication risk;
- deletion risk;
- implementation incompatibility;
- governance conflict.

Escalation SHOULD preserve enough context for a human or governed workflow to review the issue without exposing restricted information beyond the permitted scope.

### 5.11 Implementation Support

An agent MAY support implementation work where permitted.

Implementation support MAY include:

- preparing templates;
- preparing validator logic;
- preparing folder setup instructions;
- preparing Obsidian-facing guidance;
- preparing Codex-facing guidance;
- preparing scripts;
- preparing configuration notes;
- preparing implementation documentation;
- checking implementation conformance;
- identifying implementation drift.

Implementation support MUST remain subordinate to The Brain Standard.

An agent MUST NOT make a specific tool, model, vault, plugin, repository, database, script, prompt, runtime, or interface the standard itself.

### 5.12 Reporting and Traceability

An agent MAY generate reports where permitted.

Reports MAY include:

- inspection reports;
- validation reports;
- relationship reports;
- source-reference reports;
- provenance reports;
- privacy reports;
- authority reports;
- lifecycle reports;
- storage reports;
- import reports;
- export reports;
- migration reports;
- implementation reports;
- conformance reports.

Agent reports SHOULD distinguish findings, assumptions, evidence, confidence, uncertainty, recommendations, and required review.

An agent report MUST NOT create approval, authority, validation acceptance, privacy clearance, publication permission, export permission, migration permission, deletion permission, or governance acceptance by itself.

## 6. Prohibited Agent Operations

Prohibited Agent Operations define what agents must not do within The Brain Standard unless a future higher-authority governance process, standard, specification, or governed workflow explicitly permits a limited exception within a defined scope.

A prohibited operation remains prohibited even when the agent has technical capability to perform it.

A prohibited operation remains prohibited even when the operation is convenient.

A prohibited operation remains prohibited even when the agent output appears correct.

A prohibited operation remains prohibited even when the operation is repeated, automated, validated by a tool, surfaced by an implementation, or requested by an implementation default.

Prohibited Agent Operations exist to prevent agents from silently governing The Brain.

### 6.1 Unbounded Access

An agent MUST NOT access governed material outside its authorized scope.

An agent MUST NOT treat vault access, repository access, file-system access, database access, tool access, plugin access, chat context, model context, search index access, cache access, or implementation visibility as unrestricted permission.

An agent MUST NOT search, read, summarize, extract, index, embed, cache, classify, export, publish, migrate, or use restricted material downstream unless permitted by Privacy Classification and the applicable governed scope.

### 6.2 Silent Object Identity Changes

An agent MUST NOT silently create, remove, replace, merge, split, redirect, reassign, reinterpret, or collapse Object Identity.

An agent MUST NOT treat filename, title, folder path, storage location, search result, graph position, backlink behavior, tag, prompt context, model memory, source similarity, or implementation identifier as stable Object Identity unless a governed identity rule defines that behavior.

An agent MAY identify possible identity conflicts or duplicates.

An agent MUST escalate identity changes where Object Identity affects relationships, Source References, provenance, lifecycle state, authority, privacy, validation, compatibility, import, export, migration, or downstream use.

### 6.3 Silent Lifecycle Transitions

An agent MUST NOT silently approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, publish, export, migrate, or otherwise transition Lifecycle State as a final governed action.

An agent MAY propose lifecycle transitions.

An agent MAY recommend review.

An agent MAY identify lifecycle inconsistencies.

An agent-generated lifecycle recommendation MUST remain distinguishable from an approved lifecycle transition unless a future governed workflow explicitly permits automatic transition within a limited scope.

### 6.4 Authority Overreach

An agent MUST NOT create Authority Level by itself.

An agent MUST NOT treat agent confidence, fluency, frequency, model preference, tool output, validation result, workflow completion, implementation visibility, source popularity, relationship strength, graph centrality, search ranking, or user convenience as Authority Level.

An agent MUST NOT become an unreviewable authority where authority affects governed interpretation, publication, export, migration, validation, privacy handling, workflow behavior, implementation behavior, or downstream use.

An agent MAY recommend authority review.

An agent MAY identify authority conflicts.

An agent MAY propose authority-related handling.

Such proposals MUST remain reviewable.

### 6.5 Privacy Violations

An agent MUST NOT override Privacy Classification.

An agent MUST NOT expose restricted content merely because it improves traceability, search quality, summary quality, relationship quality, validation quality, migration quality, publication convenience, export convenience, implementation convenience, or downstream usefulness.

An agent MUST NOT reveal restricted Source Material, restricted relationships, restricted provenance, restricted lifecycle state, restricted authority context, restricted validation results, restricted workflows, restricted identities, restricted instructions, restricted prompts, restricted credentials, restricted security context, or restricted content to an unauthorized user, agent, workflow, index, cache, export, publication, implementation, or downstream system.

Where agent usefulness and privacy conflict, privacy SHALL take precedence.

### 6.6 Source Reference and Provenance Violations

An agent MUST NOT fabricate Source References, provenance, evidence, attribution, review history, validation history, approval history, migration history, import history, export history, or source support.

An agent MUST NOT remove Source References or provenance merely to simplify a record.

An agent MUST NOT treat an agent summary as the original source.

An agent MUST NOT treat extracted content as complete source representation unless a governed review or specification supports that interpretation.

An agent MUST NOT weaken source traceability where traceability affects meaning, authority, privacy, validation, compatibility, publication, export, migration, governance, or downstream use.

### 6.7 Relationship Overreach

An agent MUST NOT silently create approved relationship meaning.

An agent MUST NOT treat inferred, suggested, generated, indexed, embedded, searched, linked, ranked, or visually displayed relationships as approved relationships by themselves.

An agent MUST NOT connect a relationship to the wrong Knowledge Object, Knowledge Record, Source Material, governed document, workflow, implementation, decision, identifier, or other governed entity.

An agent MUST NOT expose restricted relationship meaning through summaries, graph views, search results, indexes, logs, exports, publications, dashboards, APIs, plugins, caches, prompts, or generated files.

### 6.8 Validation Overreach

An agent MUST NOT treat validation support as final approval unless a future governed workflow or specification explicitly defines that result within a controlled scope.

An agent MUST NOT treat validation success as Authority Level, Lifecycle State approval, Privacy Classification approval, publication readiness, export readiness, migration readiness, deletion permission, or governance acceptance.

An agent MUST NOT silently repair validation failures where repair affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, publication, export, migration, or downstream use.

An agent MAY recommend repair.

Repair recommendations SHOULD remain reviewable.

### 6.9 Storage-Defined Meaning

An agent MUST NOT allow storage placement to define knowledge meaning.

An agent MUST NOT treat a folder, filename, vault path, repository path, archive location, backup location, import location, export location, migration location, index location, cache location, generated-file location, implementation workspace, tag, sort order, graph location, or search result as the sole source of governed meaning.

An agent MUST NOT move material in a way that breaks Object Identity, Source References, provenance, relationships, lifecycle state, authority, privacy, validation, compatibility, recovery, or governance.

### 6.10 Destructive Actions

An agent MUST NOT permanently delete, purge, overwrite, discard, erase, corrupt, or make unavailable governed material unless a future governed workflow or specification explicitly permits that operation within a defined scope.

An agent MUST NOT delete Source Material, Knowledge Records, governed documents, metadata records, relationship records, Source References, provenance records, validation records, lifecycle records, authority records, privacy records, archives, backups, import records, export records, or migration records where deletion would break traceability, auditability, compatibility, privacy protection, restoration, governance, or downstream interpretation.

An agent MAY recommend deletion, archival, quarantine, supersession, deprecation, or cleanup.

Destructive recommendations SHOULD be escalated for human review.

### 6.11 Unauthorized Export, Publication, or Migration

An agent MUST NOT export, publish, synchronize, transmit, expose, migrate, package, or release governed material beyond its current authorized boundary unless permitted by Privacy Classification, Authority Level, Lifecycle State, Validation State, workflow rules, permission scope, and governance expectations.

An agent MUST NOT treat export preparation as export approval.

An agent MUST NOT treat publication drafting as publication approval.

An agent MUST NOT treat migration mapping as migration approval.

An agent MUST NOT expose restricted material through exports, publication drafts, migration packages, logs, generated files, validation reports, summaries, indexes, caches, embeddings, or implementation outputs.

### 6.12 Implementation or Model Lock-In

An agent MUST NOT make any implementation, model, prompt, plugin, database, vault, repository, file system, interface, runtime, API, automation system, index, cache, script, or tool the standard itself.

An agent MUST NOT redefine standard behavior through implementation-specific assumptions.

An agent MUST NOT treat model memory, prompt context, hidden tool state, application state, database internals, plugin metadata, UI state, or workflow memory as governed truth unless the relevant meaning is explicit, portable, inspectable, and governed.

An agent may use implementation-specific signals to assist analysis.

Those signals MUST remain subordinate to The Brain Standard.

### 6.13 Hidden Governance

An agent MUST NOT silently govern.

An agent MUST NOT allow repeated automation, successful outputs, implementation convenience, workflow convenience, user habit, model confidence, tool availability, validation success, indexing behavior, or storage placement to become a standard-level rule without documented governance.

An agent MUST NOT make undocumented practice part of The Brain Standard.

An agent MUST NOT bypass human review where human review is required for critical knowledge changes.

Prohibited Agent Operations are successful when future humans, agents, workflows, validators, storage systems, and implementations can distinguish agent assistance from agent governance.

## 7. Agent Output and Provenance

Agent Output and Provenance define how agent-produced material must be identified, interpreted, reviewed, preserved, validated, and governed within The Brain Standard.

Agent Output exists because agents may create useful summaries, classifications, metadata proposals, relationship proposals, Source Reference proposals, validation findings, drafts, reports, transformations, recommendations, and implementation-support material.

Agent Provenance exists because future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations must be able to determine what an agent produced, why it was produced, what source material or governed entities were used, what scope applied, what confidence or uncertainty was expressed, and what review state applies.

Agent Output MUST remain distinguishable from:

- human-authored material;
- human-reviewed material;
- approved governed material;
- authoritative material;
- Source Material;
- Knowledge Records;
- validated material;
- published material;
- export-approved material;
- migration-approved material;
- implementation-specific generated files;
- workflow-approved outputs;
- future governed output categories.

Agent Output MUST NOT become approved, authoritative, valid, source-supported, published, exportable, migratable, or final merely because an agent produced it.

Agent Output and Provenance are successful when future humans, agents, workflows, validators, storage systems, and implementations can determine what was generated, what was proposed, what was changed, what was reviewed, what was accepted, what was rejected, and what remains unresolved.

### 7.1 Agent Output Definition

Agent Output is any result created, proposed, assisted, transformed, classified, summarized, validated, routed, reported, generated, or modified by an agent.

Agent Output MAY include:

- summaries;
- classifications;
- extracted content;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- provenance notes;
- lifecycle recommendations;
- authority recommendations;
- privacy classification recommendations;
- validation findings;
- repair recommendations;
- Knowledge Record drafts;
- governed document drafts;
- review reports;
- storage movement recommendations;
- import mappings;
- export packages;
- migration mappings;
- publication drafts;
- implementation-support files;
- workflow-support notes;
- generated files;
- other agent-created material.

Agent Output SHOULD identify or support identification of its agent origin where that origin affects meaning, review, authority, privacy, lifecycle handling, validation, publication, export, migration, or downstream use.

Agent Output MUST remain distinguishable from Source Material.

An agent summary of Source Material is not the Source Material.

An agent extraction from Source Material is not automatically complete.

An agent interpretation of Source Material is not automatically correct.

An agent draft of a Knowledge Record is not automatically an approved Knowledge Record.

### 7.2 Agent Output Categories

Agent Output SHOULD be categorized where category affects interpretation, handling, review, storage, validation, privacy, authority, lifecycle state, export, migration, publication, or downstream use.

At minimum, The Brain Standard recognizes the following Agent Output Categories:

- informational outputs;
- analytical outputs;
- extracted outputs;
- summarized outputs;
- classification outputs;
- metadata proposal outputs;
- relationship proposal outputs;
- Source Reference proposal outputs;
- provenance outputs;
- validation-support outputs;
- draft outputs;
- review-support outputs;
- implementation-support outputs;
- workflow-support outputs;
- generated files;
- applied-change records;
- escalation outputs.

A future agent specification MAY define exact output categories, output fields, output metadata, output lifecycle states, output validation rules, output storage rules, or output serialization syntax.

Such specifications are valid only when they preserve the boundaries defined by AG-0001.

### 7.3 Agent Provenance Requirements

Agent Provenance SHOULD identify or support identification of:

- what agent produced or assisted the output;
- what model, tool, script, workflow, implementation, or process was involved where applicable;
- what instruction, task, prompt, workflow step, or permission scope applied where applicable;
- what Source Material was used where applicable;
- what Knowledge Objects, Knowledge Records, relationships, metadata, Source References, provenance records, lifecycle states, authority levels, privacy classifications, validation results, or storage areas were used where applicable;
- what output was produced;
- when the output was produced where applicable;
- whether the output was proposed, applied, rejected, reverted, superseded, approved, archived, or pending review;
- what human review occurred where applicable;
- what validation occurred where applicable;
- what uncertainty, limitation, or unresolved issue applies where applicable.

Agent Provenance SHALL be explicit where agent activity affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

Agent Provenance MUST NOT expose restricted information beyond the applicable Privacy Classification.

Where provenance refers to restricted material, the provenance SHOULD preserve enough traceability for authorized review without unnecessarily exposing restricted content.

### 7.4 Agent Output Review State

Agent Output SHOULD have or support a review state where review affects interpretation, authority, privacy, validation, lifecycle handling, publication, export, migration, or downstream use.

Agent Output MAY be:

- generated;
- proposed;
- pending review;
- under review;
- accepted;
- rejected;
- revised;
- applied;
- reverted;
- superseded;
- archived;
- quarantined;
- needs repair;
- governed by a future output review state.

Agent Output review state MUST remain distinguishable from Lifecycle State unless a future governed specification explicitly defines how they relate.

Agent Output review state MUST remain distinguishable from Authority Level.

Agent Output review state MUST remain distinguishable from Validation State.

Agent Output review state MUST remain distinguishable from Privacy Classification.

Agent Output that is accepted for one scope MUST NOT be treated as accepted for every scope.

### 7.5 Agent Output and Object Identity

Agent Output MUST preserve Object Identity.

Agent Output MUST NOT create, remove, merge, split, replace, redirect, reassign, reinterpret, or collapse Object Identity unless a governed workflow or future specification explicitly permits that operation within a defined scope.

An agent-generated draft MAY propose a new Knowledge Object.

An agent-generated draft MAY identify possible duplicate objects.

An agent-generated draft MAY recommend identity review.

An agent-generated draft MUST NOT silently assign final Object Identity where identity affects relationships, Source References, provenance, lifecycle state, authority, privacy, validation, import, export, migration, compatibility, or downstream use.

Where Agent Output references an existing Knowledge Object, it SHOULD preserve the stable Object Identity rather than relying on filename, folder path, title, tag, search result, graph position, or implementation-specific identifier.

### 7.6 Agent Output and Metadata

Agent Output MAY propose, enrich, classify, validate, or repair metadata where permitted.

Agent-generated metadata MUST remain distinguishable from approved governed metadata where that distinction affects meaning, Object Identity, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, or downstream use.

An agent MUST NOT treat generated metadata as authoritative merely because it appears complete, consistent, useful, plausible, repeated, model-confident, validated by a tool, or surfaced by an implementation.

Agent Output SHOULD preserve metadata provenance where metadata changes affect governed interpretation.

### 7.7 Agent Output and Relationships

Agent Output MAY propose, infer, classify, validate, or repair relationships where permitted.

Agent-generated relationships MUST remain distinguishable from human-reviewed or approved relationships unless a governed workflow or future specification explicitly defines automatic approval for a limited relationship type.

Agent Output MUST NOT silently create approved relationship meaning.

Agent Output SHOULD identify relationship provenance where the relationship affects meaning, authority, privacy, lifecycle state, validation, source traceability, compatibility, publication, export, migration, governance, or downstream use.

Agent Output SHOULD preserve relationship uncertainty where a relationship is inferred, weakly supported, disputed, incomplete, or pending review.

### 7.8 Agent Output and Source References

Agent Output MAY propose Source References where permitted.

Agent Output MUST NOT fabricate Source References.

Agent Output MUST NOT treat unsupported content as source-supported.

Agent Output MUST NOT treat a source mention, filename, folder location, search result, citation style, link preview, memory reference, or model statement as a valid Source Reference unless the reference remains traceable, reviewable, and compatible with the applicable Source Reference and Provenance Standard.

Agent Output SHOULD preserve source context where summaries, extractions, classifications, relationships, validations, or drafts rely on Source Material.

Agent Output SHOULD identify missing, uncertain, restricted, unavailable, superseded, or unverifiable sources where that affects meaning, authority, privacy, validation, publication, export, migration, or downstream use.

### 7.9 Agent Output and Privacy

Agent Output MUST preserve Privacy Classification.

Agent Output MUST NOT expose restricted material through summaries, metadata, relationships, Source References, provenance, validation results, reports, logs, indexes, caches, embeddings, generated files, exports, publication drafts, migration packages, implementation displays, or downstream outputs unless permitted.

An agent MUST NOT lower, remove, bypass, or reinterpret Privacy Classification merely to improve usefulness, traceability, validation, search, migration, export, publication, implementation convenience, or downstream use.

Where Agent Output contains restricted material, the output SHOULD inherit or preserve the applicable privacy boundary unless a governed privacy process explicitly permits a different classification.

Privacy SHALL take precedence over agent usefulness where they conflict.

### 7.10 Agent Output and Validation

Agent Output MAY support validation.

Agent Output MUST NOT be treated as validation acceptance unless a future governed workflow or specification explicitly defines that result within a limited scope.

Agent Output MUST NOT treat validation findings as approval, authority, privacy permission, lifecycle transition, publication readiness, export readiness, migration readiness, deletion permission, or governance acceptance.

Agent-generated validation findings SHOULD identify scope.

A validation finding that checks only one concern MUST NOT imply full validation.

Agent Output SHOULD preserve validation evidence where validation affects meaning, privacy, authority, lifecycle state, publication, export, migration, compatibility, or downstream use.

### 7.11 Agent Output Storage

Agent Output MAY be stored where permitted by the applicable storage standard, storage layout, workflow, implementation profile, privacy classification, and permission model.

Agent Output storage MUST NOT define Agent Output meaning by itself.

Storage location MUST NOT cause Agent Output to become approved, authoritative, valid, published, exportable, migratable, private, public, archived, superseded, deprecated, or deleted.

Agent Output stored in drafts, review areas, working areas, generated-file areas, caches, indexes, implementation-support areas, workflow-support areas, import areas, export areas, migration areas, archives, or backups MUST preserve its review state, provenance, privacy boundary, validation context, and compatibility expectations where those affect downstream use.

### 7.12 Agent Output Success Criteria

Agent Output handling conforms to AG-0001 when:

- agent origin remains identifiable where required;
- output type remains distinguishable;
- Source Material remains distinguishable from agent summaries and extractions;
- proposals remain distinguishable from approvals;
- validation support remains distinguishable from validation acceptance;
- agent confidence remains distinguishable from Authority Level;
- storage location does not define output meaning;
- privacy boundaries are preserved;
- provenance is preserved where needed;
- human review remains available where required;
- implementation-specific generated material does not become the standard itself.

Agent Output and Provenance are successful when agent assistance remains useful, traceable, reviewable, privacy-respecting, validation-compatible, and subordinate to governance.

## 8. Agent Review, Escalation, and Human Approval

Agent Review, Escalation, and Human Approval define how agent activity is inspected, routed, accepted, rejected, corrected, limited, or approved within The Brain Standard.

Agent review exists because agents may assist with important knowledge work but must not become unreviewable authorities over governed material.

Escalation exists because agents will encounter ambiguity, conflict, missing context, privacy risk, authority risk, validation failure, source uncertainty, lifecycle uncertainty, destructive-action risk, export risk, publication risk, migration risk, or governance risk.

Human Approval exists because some actions require accountable review before they may affect governed meaning, authority, privacy, validation, publication, export, migration, deletion, or downstream use.

Agent Review, Escalation, and Human Approval are successful when humans, agents, workflows, validators, storage systems, and implementations can determine what needs review, what was escalated, who or what reviewed it, what decision was made, what remains unresolved, and what downstream action is allowed.

### 8.1 Review Requirement

Agent activity SHOULD be reviewable where it affects:

- governed meaning;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage movement;
- publication;
- export;
- migration;
- deletion;
- archival;
- synchronization;
- indexing;
- implementation exposure;
- downstream use.

Human review SHALL remain available for critical knowledge changes.

A future governed workflow MAY define limited automatic approval only when the action is bounded, reversible where practical, validated, privacy-respecting, traceable, compatible, and explicitly permitted.

### 8.2 Review Scope

Review Scope defines what part of agent activity is being reviewed.

Review Scope MAY include:

- a single Agent Output;
- a proposed metadata change;
- a proposed relationship;
- a proposed Source Reference;
- a proposed provenance record;
- a proposed lifecycle transition;
- an authority recommendation;
- a privacy classification recommendation;
- a validation finding;
- a storage movement;
- an import mapping;
- an export package;
- a migration mapping;
- a publication draft;
- a deletion recommendation;
- a workflow recommendation;
- an implementation-support output;
- another governed review scope.

A review result MUST NOT imply broader approval than the reviewed scope supports.

Approval of a summary does not imply approval of all metadata.

Approval of metadata does not imply approval of relationships.

Approval of a relationship does not imply approval of publication.

Approval of export preparation does not imply approval to release the export.

Approval of migration mapping does not imply approval to complete migration.

### 8.3 Human Approval

Human Approval is the review-based acceptance of an Agent Output, agent-generated change, recommendation, draft, validation finding, storage action, workflow action, publication action, export action, migration action, or other governed action by an authorized human.

Human Approval SHOULD be explicit where approval affects:

- governed meaning;
- Object Identity;
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
- archival;
- downstream use.

Human Approval MUST preserve scope.

Human Approval in one context MUST NOT be treated as approval in every context.

Human Approval SHOULD preserve enough provenance to determine what was approved, who approved it where applicable, when approval occurred where applicable, what evidence was reviewed where applicable, what conditions apply, and what downstream use is permitted.

### 8.4 Escalation Triggers

An agent SHOULD escalate when it detects or suspects:

- Object Identity conflict;
- duplicate risk;
- merge risk;
- split risk;
- source uncertainty;
- missing Source References;
- provenance gap;
- relationship conflict;
- lifecycle ambiguity;
- authority conflict;
- privacy risk;
- validation failure;
- validation scope uncertainty;
- storage-placement conflict;
- destructive-action risk;
- export risk;
- publication risk;
- migration risk;
- restricted-content exposure risk;
- implementation incompatibility;
- governance conflict;
- instruction conflict;
- standard conflict;
- unresolved ambiguity.

An agent MUST escalate rather than silently resolve an issue where silent resolution would affect governed meaning, authority, privacy, validation, lifecycle state, source traceability, publication, export, migration, deletion, or governance.

Escalation SHOULD preserve enough context for review without exposing restricted information beyond the authorized scope.

### 8.5 Escalation Output

Escalation Output SHOULD identify or support identification of:

- what issue was detected;
- what governed entity is affected;
- what agent detected the issue where applicable;
- what source material or evidence was involved where applicable;
- what standard, workflow, permission, privacy boundary, validation scope, or authority scope may be affected;
- what risk exists;
- what action is recommended;
- whether immediate action is required;
- whether human review is required;
- whether the issue blocks further agent action;
- whether restricted information is involved;
- what context may be safely shown to the reviewer.

Escalation Output MUST NOT expose restricted material beyond the permitted scope.

Escalation Output MUST NOT become approval, rejection, repair, deletion, publication, export, migration, privacy clearance, authority assignment, or lifecycle transition by itself.

### 8.6 Review Outcomes

A review outcome MAY be:

- accepted;
- accepted with changes;
- rejected;
- returned for revision;
- escalated further;
- approved for limited scope;
- approved for full stated scope;
- deferred;
- quarantined;
- marked needs repair;
- superseded;
- archived;
- reverted;
- governed by a future review outcome.

Review outcomes SHOULD preserve scope.

A rejected Agent Output MAY remain historically useful for audit, comparison, error analysis, governance review, or future repair.

A rejected Agent Output MUST NOT be treated as approved, authoritative, valid, publishable, exportable, migratable, or safe for downstream use.

A deferred review MUST NOT be treated as approval.

A partial approval MUST remain distinguishable from full approval.

### 8.7 Review Provenance

Review Provenance SHOULD identify or support identification of:

- what was reviewed;
- who or what reviewed it where applicable;
- what review scope applied;
- what source material, evidence, validation result, relationship, metadata, or prior decision was considered where applicable;
- what outcome was assigned;
- what changes were required;
- what restrictions remain;
- what follow-up action is required;
- what downstream use is permitted or prohibited.

Review Provenance SHALL be preserved where the review affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

Review Provenance MUST preserve Privacy Classification.

### 8.8 Review and Workflow Boundaries

A workflow may route Agent Output for review.

Workflow routing is not review completion.

Workflow completion is not approval unless a governed workflow explicitly defines that result within a limited scope.

An agent may prepare review material.

Preparation is not review completion.

A validator may support review.

Validation support is not approval unless a governed workflow explicitly defines that result within a limited scope.

An implementation may display review status.

Implementation visibility is not approval.

### 8.9 Review and Authority Boundaries

Review may support Authority Level.

Review does not automatically create Authority Level unless the applicable authority rule, workflow, or specification defines that effect.

Approval MAY affect authority within a defined scope.

Approval does not automatically create unlimited authority.

Authority MUST remain scoped, explicit, and reviewable where authority affects interpretation, governance, publication, export, migration, validation, privacy handling, workflow behavior, implementation behavior, or downstream use.

Agent review support MUST NOT be confused with authority assignment.

### 8.10 Review Success Criteria

Agent review, escalation, and human approval conform to AG-0001 when:

- review scope is clear where needed;
- agent proposals remain distinguishable from approvals;
- escalation occurs when ambiguity or risk affects governed handling;
- human review remains available for critical knowledge changes;
- review outcomes preserve provenance where needed;
- review outcomes preserve Privacy Classification;
- approval remains scoped;
- workflow completion does not silently become approval;
- validation support does not silently become approval;
- implementation visibility does not silently become approval;
- rejected or deferred outputs do not become authoritative by accident.

Agent Review, Escalation, and Human Approval are successful when review protects knowledge meaning, privacy, authority, validation, source traceability, lifecycle handling, governance, and downstream use without preventing agents from providing useful assistance.

## 9. Agent Validation and Compatibility

Agent Validation and Compatibility define how agent behavior, Agent Output, agent permissions, agent-generated changes, and agent-supported workflows are checked for conformance with The Brain Standard.

Agent Validation exists so that agent activity can be evaluated without confusing agent usefulness, confidence, fluency, tool success, workflow completion, or implementation visibility with governed correctness.

Agent Compatibility exists so that agent behavior remains portable, reviewable, privacy-respecting, traceable, and implementation-independent across different models, tools, workflows, storage environments, and implementations.

Agent Validation and Compatibility are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine whether agent activity stayed within scope, preserved governed meaning, respected privacy, preserved provenance, avoided authority creep, and remained compatible with higher-authority standards.

### 9.1 Agent Validation Scope

Agent Validation Scope defines what aspect of agent activity is being validated.

Agent Validation Scope MAY include:

- agent access;
- agent permissions;
- Agent Output;
- agent-generated metadata;
- agent-generated relationships;
- agent-generated Source References;
- agent-generated provenance;
- agent-generated lifecycle recommendations;
- agent-generated authority recommendations;
- agent-generated privacy recommendations;
- agent-generated validation findings;
- agent-generated drafts;
- agent-supported storage movement;
- agent-supported import preparation;
- agent-supported export preparation;
- agent-supported migration preparation;
- agent-supported publication preparation;
- agent-supported deletion recommendations;
- agent escalation behavior;
- agent review behavior;
- implementation-specific agent behavior;
- workflow-specific agent behavior;
- another governed validation scope.

A validation result MUST NOT imply broader validation than its scope supports.

### 9.2 Agent Validation Requirements

Agent activity SHOULD be validated where it affects:

- governed meaning;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage behavior;
- workflow behavior;
- publication;
- export;
- migration;
- deletion;
- synchronization;
- indexing;
- implementation exposure;
- downstream use.

Agent validation SHOULD check whether the agent acted within authorized scope.

Agent validation SHOULD check whether privacy boundaries were preserved.

Agent validation SHOULD check whether agent outputs remained distinguishable from approved governed material.

Agent validation SHOULD check whether required provenance was preserved.

Agent validation SHOULD check whether agent confidence was kept separate from authority, validation acceptance, approval, privacy clearance, lifecycle transition, publication readiness, export readiness, migration readiness, and governance acceptance.

### 9.3 Validation of Agent Permissions

Validation of Agent Permissions SHOULD determine whether:

- the agent had permission to act;
- the permission scope was explicit where required;
- the agent stayed within scope;
- the permission matched the operation type;
- the permission respected Privacy Classification;
- high-risk permissions had appropriate review or workflow authorization;
- permissions were not silently inherited beyond scope;
- revoked, expired, superseded, rejected, or invalid permissions were not used;
- tool capability was not confused with governed permission.

A permission validation result MUST NOT become permission by itself.

A failed permission validation SHOULD block or escalate further agent action where continued action creates privacy, authority, validation, lifecycle, publication, export, migration, deletion, or governance risk.

### 9.4 Validation of Agent Output

Validation of Agent Output SHOULD determine whether:

- the output is identifiable as Agent Output;
- the output category is clear where needed;
- the output scope is clear where needed;
- source material remains distinguishable from summaries and extractions;
- proposals remain distinguishable from approvals;
- validation support remains distinguishable from validation acceptance;
- agent confidence remains distinguishable from Authority Level;
- privacy boundaries are preserved;
- provenance is preserved where needed;
- review state is clear where needed;
- storage location does not define output meaning;
- implementation-specific output does not become standard-level meaning.

Agent Output validation MUST NOT make the output approved, authoritative, publishable, exportable, migratable, or safe for downstream use unless a future governed workflow or specification explicitly defines that result.

### 9.5 Validation of Agent-Generated Changes

Validation of Agent-Generated Changes SHOULD determine whether the change:

- stayed within authorized scope;
- preserved Object Identity;
- preserved metadata meaning;
- preserved relationships;
- preserved Source References;
- preserved provenance;
- preserved Lifecycle State;
- preserved Authority Level;
- preserved Privacy Classification;
- preserved Validation State;
- preserved compatibility expectations;
- preserved storage boundaries;
- preserved human reviewability;
- avoided hidden governance;
- avoided implementation lock-in.

An agent-generated change that fails validation SHOULD be escalated, reverted, repaired, quarantined, or returned for review according to the applicable workflow, permission model, privacy classification, and governance expectation.

A validation failure MUST NOT be silently hidden merely because the agent output is useful.

### 9.6 Agent Compatibility Requirements

Agent behavior SHOULD remain compatible across:

- different AI models;
- different model providers;
- different prompt systems;
- different agent frameworks;
- different workflow engines;
- different storage environments;
- different vaults;
- different repositories;
- different databases;
- different file systems;
- different operating systems;
- different interfaces;
- different implementation profiles;
- future implementations.

Agent compatibility means the governed meaning of knowledge does not depend on a specific model, prompt, runtime, tool, plugin, index, cache, API, interface, or hidden implementation state.

A compliant agent design MUST NOT require a specific AI model, provider, prompt system, plugin, tool, workflow engine, or implementation for The Brain Standard to remain valid.

### 9.7 Compatibility With Prior Standards

Agent behavior MUST remain compatible with the constitutional foundation and the Phase 1 and Phase 2 standards.

Agent behavior MUST preserve:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage architecture;
- storage layout;
- source distinction;
- Knowledge Record distinction;
- governed document boundaries;
- draft, review, and approval boundaries;
- archive, backup, import, export, and migration boundaries;
- implementation independence;
- human reviewability;
- AI readability;
- practical daily usability;
- governed evolution.

Agent behavior MUST NOT weaken a higher-authority standard for implementation convenience, model convenience, workflow convenience, speed, automation, summarization quality, search quality, storage convenience, or user-interface convenience.

### 9.8 Compatibility During Import, Export, and Migration

Agent-supported import, export, and migration work SHOULD preserve agent-related context where that context affects interpretation, review, validation, privacy, authority, source traceability, compatibility, or downstream use.

Agent-supported import, export, and migration SHOULD preserve:

- agent-generated output status;
- agent provenance;
- review state;
- validation scope;
- permission scope where applicable;
- privacy boundaries;
- authority boundaries;
- lifecycle context;
- Source Reference context;
- relationship context;
- storage context;
- compatibility notes.

An agent MUST NOT collapse proposed, reviewed, approved, rejected, superseded, archived, generated, cached, indexed, or implementation-specific material into a single indistinguishable state during import, export, or migration.

An agent MUST NOT expose restricted Agent Output during import, export, or migration unless permitted.

### 9.9 Agent Validation Findings

Agent Validation Findings SHOULD be categorized as errors, warnings, recommendations, informational notes, blocked actions, escalations, or future governed finding types.

A validation error SHOULD indicate that an agent activity failed a mandatory requirement within the defined validation scope.

A validation warning SHOULD indicate potential risk, ambiguity, incompleteness, inconsistency, or recommended improvement without necessarily making the agent activity invalid.

A recommendation SHOULD remain distinguishable from a required correction.

An informational note SHOULD remain distinguishable from a validation error.

Agent Validation Findings SHOULD preserve enough context for review without exposing restricted information beyond the permitted scope.

### 9.10 Agent Validation Success Criteria

Agent validation conforms to AG-0001 when:

- validation scope is clear;
- agent permissions are checked where needed;
- Agent Output remains distinguishable from approved governed material;
- agent confidence remains distinguishable from authority and validation acceptance;
- privacy boundaries are preserved;
- required provenance is preserved;
- human review remains available where required;
- storage location does not define agent output meaning;
- implementation-specific behavior does not become standard-level behavior;
- import, export, and migration preserve agent-related context where needed;
- validation findings remain reviewable;
- validation does not silently create approval, authority, lifecycle transition, privacy permission, publication readiness, export readiness, migration readiness, deletion permission, or governance acceptance.

Agent Validation and Compatibility are successful when agent activity can be trusted as bounded assistance without allowing agents to redefine knowledge meaning, privacy, authority, validation, lifecycle state, storage meaning, workflow meaning, implementation compliance, or governance.

## 10. Agent Privacy, Security, and Access Handling

Agent Privacy, Security, and Access Handling defines how agents must preserve privacy boundaries, access limits, exposure controls, and security-sensitive handling within The Brain Standard.

This section exists because agents may read, summarize, extract, classify, index, route, validate, export, publish, migrate, or otherwise process governed material that may be private, restricted, sensitive, confidential, or otherwise limited by Privacy Classification.

Agent usefulness MUST NOT override Privacy Classification.

Agent access MUST remain bounded by the applicable task, workflow, permission model, privacy boundary, authority boundary, implementation environment, and governed standard.

Agent Privacy, Security, and Access Handling is successful when agents can assist with knowledge work without exposing restricted material, weakening access boundaries, leaking sensitive context, bypassing review, or making hidden implementation behavior the basis for privacy decisions.

### 10.1 Privacy Preservation

An agent MUST preserve Privacy Classification.

An agent MUST NOT lower, remove, bypass, reinterpret, or ignore Privacy Classification unless a governed privacy process explicitly permits that change within a defined scope.

An agent MUST NOT treat visibility, searchability, tool access, model context, file-system access, implementation access, vault access, repository access, database access, index access, or cache access as permission to expose restricted material.

Privacy Classification SHALL take precedence over agent usefulness, automation convenience, search quality, summarization quality, validation quality, migration convenience, publication convenience, export convenience, or implementation convenience.

### 10.2 Agent Access Limits

Agent access SHOULD be limited to the minimum scope required for the task.

Agent access MAY be limited by:

- Knowledge Object;
- Knowledge Record;
- Source Material;
- storage area;
- workflow stage;
- permission scope;
- privacy classification;
- authority scope;
- lifecycle state;
- validation scope;
- import package;
- export package;
- migration package;
- implementation environment;
- responsible human;
- future governed access boundary.

An agent MUST NOT access governed material outside its authorized scope.

An agent MUST NOT infer that access in one scope grants access in another scope.

An agent MUST NOT use restricted material downstream unless that downstream use is permitted.

### 10.3 Exposure Controls

Exposure occurs when governed material is revealed, transmitted, displayed, summarized, extracted, indexed, embedded, cached, exported, published, migrated, logged, or otherwise made available beyond its prior boundary.

An agent MUST NOT expose restricted material unless the relevant Privacy Classification, permission scope, workflow, and governance expectations allow that exposure.

Restricted material MUST NOT be exposed through:

- summaries;
- metadata;
- relationships;
- Source References;
- provenance;
- validation findings;
- review reports;
- logs;
- prompts;
- indexes;
- embeddings;
- caches;
- generated files;
- exports;
- publication drafts;
- migration packages;
- implementation displays;
- downstream outputs.

Where limited exposure is permitted, the agent SHOULD expose only the minimum necessary information required for the authorized task.

### 10.4 Security-Sensitive Material

Security-sensitive material includes information that may create privacy, access, operational, governance, or system-integrity risk if exposed, copied, summarized, indexed, exported, published, migrated, or used downstream.

Security-sensitive material MAY include:

- credentials;
- secrets;
- access tokens;
- private keys;
- restricted prompts;
- internal instructions;
- private workflow rules;
- restricted source material;
- private identifiers;
- security context;
- unpublished governance decisions;
- restricted relationship information;
- restricted provenance;
- restricted validation results;
- restricted implementation details;
- future governed sensitive categories.

An agent MUST NOT expose security-sensitive material unless explicitly permitted within a governed scope.

An agent SHOULD escalate when security-sensitive material is discovered in an unexpected location, output, cache, index, export, migration package, publication draft, or implementation area.

### 10.5 Privacy-Aware Summarization

An agent MAY summarize governed material only where summarization is permitted.

An agent summary MUST preserve Privacy Classification.

An agent MUST NOT summarize restricted material for an unauthorized user, workflow, agent, implementation, index, export, publication, migration package, or downstream system.

An agent MUST NOT create a summary that reveals restricted facts, restricted identities, restricted relationships, restricted source context, restricted provenance, restricted validation findings, restricted authority context, restricted lifecycle context, or restricted implementation details beyond the permitted scope.

Where a safe summary is needed, the agent SHOULD produce a privacy-preserving summary that avoids exposing restricted details while preserving enough context for authorized review.

### 10.6 Privacy-Aware Indexing, Caching, and Embedding

Indexing, caching, and embedding can expose governed material by making it searchable, retrievable, ranked, clustered, summarized, or available to future systems.

An agent MUST NOT index, cache, embed, vectorize, cluster, summarize, or otherwise make restricted material discoverable unless permitted by Privacy Classification and the applicable workflow or implementation profile.

An agent MUST NOT assume that an index, cache, embedding store, generated file, search database, model context, or implementation memory has the same privacy protections as the original governed environment.

Agent-supported indexing, caching, and embedding SHOULD preserve:

- Privacy Classification;
- source distinction;
- Object Identity where applicable;
- provenance;
- review state;
- validation context;
- export restrictions;
- migration restrictions;
- deletion or retention expectations where applicable.

### 10.7 Privacy During Validation

Agent validation MUST preserve Privacy Classification.

An agent MUST NOT expose restricted material in validation findings unless the reviewer, workflow, implementation, or downstream system is authorized to receive that information.

Validation reports SHOULD distinguish between:

- public findings;
- internal findings;
- restricted findings;
- redacted findings;
- findings requiring authorized review;
- findings requiring escalation.

An agent MAY report that a privacy-restricted issue exists without exposing restricted details where exposure would violate the applicable privacy boundary.

### 10.8 Privacy During Export, Publication, and Migration

Export, publication, and migration are high-risk privacy contexts.

An agent MUST NOT export, publish, synchronize, transmit, package, migrate, or release governed material unless the relevant Privacy Classification, Authority Level, Lifecycle State, Validation State, workflow, permission model, and governance expectations allow that action.

An agent MUST NOT include restricted material in export packages, publication drafts, migration packages, generated files, logs, validation reports, indexes, caches, embeddings, summaries, or implementation outputs unless permitted.

An agent SHOULD escalate when export, publication, or migration could expose restricted material.

Agent-supported export, publication, and migration SHOULD preserve privacy metadata and privacy handling context where required for downstream interpretation.

### 10.9 Privacy Review and Escalation

An agent SHOULD escalate privacy issues where it detects or suspects:

- missing Privacy Classification;
- conflicting Privacy Classification;
- restricted material in an unexpected location;
- restricted material in an unrestricted output;
- restricted material in an index, cache, embedding, log, export, publication draft, or migration package;
- unauthorized access;
- unauthorized summarization;
- unauthorized exposure;
- privacy downgrade without governed review;
- privacy ambiguity;
- privacy and authority conflict;
- privacy and validation conflict;
- privacy and workflow conflict;
- privacy and implementation conflict;
- another privacy risk.

An agent MUST escalate rather than silently resolve privacy issues where silent resolution would affect access, exposure, publication, export, migration, validation, governance, or downstream use.

### 10.10 Privacy and Security Success Criteria

Agent Privacy, Security, and Access Handling conforms to AG-0001 when:

- Privacy Classification is preserved;
- access remains scoped;
- restricted material is not exposed beyond permitted boundaries;
- summaries preserve privacy;
- validation findings preserve privacy;
- indexes, caches, embeddings, and generated files preserve privacy;
- export, publication, and migration preserve privacy;
- security-sensitive material is escalated where needed;
- privacy risks remain reviewable;
- agent usefulness does not override privacy.

Agent privacy handling is successful when agents can assist without creating unauthorized exposure, hidden access expansion, downstream leakage, or privacy drift.

## 11. Agent Interaction With Storage and Workflows

Agent Interaction With Storage and Workflows defines how agents may operate across storage environments and workflow processes without redefining knowledge meaning, storage meaning, lifecycle behavior, approval, authority, validation, privacy, or governance.

Agents may need to locate, inspect, classify, summarize, move, draft, validate, route, import, export, migrate, archive, or organize stored material.

Agents may also need to participate in workflows that coordinate capture, transformation, validation, review, approval, rejection, publication, maintenance, import, export, migration, archival, or repair.

Agent interaction with storage and workflows MUST remain subordinate to the Knowledge Standards, Storage Standards, Workflow Standards, and governance model.

### 11.1 Storage Interaction Principles

An agent MAY interact with storage environments where permitted.

Agent storage interaction MAY include:

- locating files;
- inspecting files;
- reading Source Material;
- reading Knowledge Records;
- identifying governed documents;
- identifying drafts;
- identifying review material;
- identifying working material;
- identifying implementation-support material;
- identifying workflow-support material;
- identifying assets;
- identifying indexes;
- identifying caches;
- identifying generated files;
- identifying archives;
- identifying backups;
- identifying imports;
- identifying exports;
- identifying migration packages;
- recommending movement;
- performing bounded movement;
- preparing storage reports.

An agent MUST NOT allow storage placement to define governed meaning.

An agent MUST NOT treat folder location, filename, vault path, repository path, database location, archive location, backup location, import location, export location, migration location, index location, cache location, generated-file location, or implementation workspace as the sole source of Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, publication permission, export permission, migration permission, or downstream-use permission.

### 11.2 Source Material and Knowledge Record Boundaries

An agent MUST preserve the distinction between Source Material and Knowledge Records.

An agent MAY extract from Source Material.

An agent MAY summarize Source Material.

An agent MAY propose a Knowledge Record based on Source Material.

An agent MUST NOT treat Source Material as a Knowledge Record merely because it has been stored, indexed, summarized, cited, classified, or processed.

An agent MUST NOT treat an agent-generated summary or extraction as the original Source Material.

An agent SHOULD preserve Source References and provenance when Source Material is used to create, enrich, validate, repair, or review Knowledge Records.

### 11.3 Draft, Review, and Approved Material

An agent MUST preserve the distinction between draft, review, and approved material.

An agent MAY work on draft material where permitted.

An agent MAY prepare review material where permitted.

An agent MAY inspect approved material where permitted.

An agent MUST NOT treat draft material as approved merely because it is complete, well-written, validated, stored near approved material, indexed, visible, or generated by a preferred model.

An agent MUST NOT treat review material as approved merely because it has been routed, summarized, validated, or prepared for human inspection.

An agent MUST NOT modify approved material unless the action is permitted by scope, workflow, authority, privacy, validation, and governance expectations.

### 11.4 Storage Movement

An agent MAY recommend storage movement where permitted.

An agent MAY perform bounded storage movement where explicitly authorized.

Storage movement MUST preserve:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- compatibility expectations;
- source distinction;
- record distinction;
- archive context;
- backup context;
- import context;
- export context;
- migration context;
- implementation-independence expectations.

An agent MUST NOT move material in a way that creates identity confusion, broken Source References, broken provenance, privacy exposure, validation failure, authority ambiguity, lifecycle ambiguity, import ambiguity, export ambiguity, migration loss, archive loss, backup loss, or governance drift.

### 11.5 Workflow Participation

An agent MAY participate in workflows where permitted.

Agent workflow participation MAY include:

- capturing input;
- extracting metadata;
- proposing relationships;
- proposing Source References;
- checking provenance;
- checking privacy classification;
- checking lifecycle state;
- checking authority level;
- performing validation support;
- preparing drafts;
- preparing review packages;
- routing issues;
- escalating risks;
- preparing import mappings;
- preparing export packages;
- preparing migration mappings;
- generating reports;
- performing bounded approved actions.

An agent MUST NOT treat workflow participation as workflow authority.

An agent MUST NOT treat workflow completion as approval unless a governed workflow explicitly defines that result within a limited scope.

### 11.6 Workflow State and Lifecycle State

Workflow State and Lifecycle State MUST remain distinguishable.

Workflow State describes where an entity is within a workflow.

Lifecycle State describes the governed status of an entity.

An agent MAY route material through workflow stages.

An agent MAY recommend Lifecycle State changes.

An agent MUST NOT silently convert workflow progress into Lifecycle State approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, publication, export, or migration.

A workflow MAY define lifecycle effects only through a governed workflow standard or specification.

### 11.7 Workflow Review and Approval

An agent MAY prepare material for workflow review.

Preparation is not review completion.

An agent MAY identify whether required workflow steps appear complete.

Workflow step completion is not approval unless explicitly governed.

An agent MAY recommend approval, rejection, repair, quarantine, deprecation, supersession, archival, publication, export, or migration.

A recommendation is not final approval.

Human review SHALL remain available for critical knowledge changes.

A governed workflow MAY define limited automatic approval only where the action is bounded, reversible where practical, validated, privacy-respecting, traceable, compatible, and explicitly permitted.

### 11.8 Workflow Logging and Traceability

Agent workflow activity SHOULD preserve traceability where it affects governed handling.

Workflow traceability SHOULD identify or support identification of:

- what agent acted;
- what workflow was involved;
- what workflow stage applied;
- what governed entity was affected;
- what permission scope applied;
- what Source Material was used;
- what output was produced;
- what validation occurred;
- what review occurred;
- what escalation occurred;
- what decision was made;
- what downstream action was permitted;
- what unresolved issue remains.

Workflow traceability MUST preserve Privacy Classification.

### 11.9 Agent Interaction With Archives, Backups, Imports, Exports, and Migrations

An agent MAY assist with archives, backups, imports, exports, and migrations where permitted.

An agent MUST preserve archive, backup, import, export, and migration context where that context affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, recovery, governance, or downstream use.

An agent MUST NOT treat archived material as deleted.

An agent MUST NOT treat backup material as current merely because it is available.

An agent MUST NOT treat import material as approved merely because it entered the system.

An agent MUST NOT treat export material as released merely because it was packaged.

An agent MUST NOT treat migration material as successfully migrated merely because it was mapped or copied.

### 11.10 Storage and Workflow Success Criteria

Agent interaction with storage and workflows conforms to AG-0001 when:

- storage placement does not define meaning;
- Source Material and Knowledge Records remain distinguishable;
- draft, review, and approved states remain distinguishable;
- workflow state does not silently become Lifecycle State;
- workflow completion does not silently become approval;
- agent movement preserves governed context;
- workflow participation remains traceable;
- privacy boundaries are preserved;
- archive, backup, import, export, and migration contexts remain distinguishable;
- agents assist workflows without silently governing them.

Agent storage and workflow interaction is successful when agents improve organization, routing, review, validation, and maintenance without weakening the standards that govern knowledge meaning.

## 12. Agent Interaction With Implementations, Tools, and Models

Agent Interaction With Implementations, Tools, and Models defines how agents may use specific software, tools, models, prompts, APIs, plugins, scripts, interfaces, databases, indexes, caches, repositories, or runtime environments without making any of them the standard itself.

The Brain Standard is implementation-independent.

Agents may operate through implementations.

Agents may use tools.

Agents may depend on models for execution.

Agents may use prompts or instructions.

However, no implementation, tool, model, prompt, plugin, script, interface, runtime, API, database, index, cache, or hidden application state may become the authority that defines The Brain Standard.

### 12.1 Implementation Independence

Agent behavior MUST remain implementation-independent at the standard level.

A compliant agent design MUST NOT require a specific:

- AI model;
- model provider;
- prompt system;
- plugin;
- tool;
- runtime;
- API;
- script;
- database;
- vault;
- repository;
- file system;
- operating system;
- interface;
- workflow engine;
- automation platform;
- indexing system;
- cache system;
- embedding system;
- application;
- future implementation.

Different implementations MAY use different agent systems if they preserve the requirements of AG-0001 and higher-authority standards.

### 12.2 Tool Capability and Governed Permission

Tool capability is not governed permission.

An agent MUST NOT treat the ability to use a tool as permission to perform every action the tool supports.

A tool may allow reading.

Reading capability is not permission to expose.

A tool may allow editing.

Editing capability is not permission to modify governed material.

A tool may allow deletion.

Deletion capability is not permission to delete.

A tool may allow export.

Export capability is not permission to export.

A tool may allow publication.

Publication capability is not permission to publish.

Tool use MUST remain bounded by scope, Privacy Classification, Authority Level, Lifecycle State, Validation State, workflow rules, permission model, and governance expectations.

### 12.3 Model Output and Governed Meaning

Model output MUST NOT define governed meaning by itself.

An agent MUST NOT treat model fluency, confidence, ranking, repetition, plausibility, source-like wording, or preferred-model status as authority, truth, approval, validation, privacy clearance, lifecycle transition, publication readiness, export readiness, migration readiness, or governance acceptance.

Model output MAY support:

- drafting;
- summarization;
- extraction;
- classification;
- relationship suggestion;
- source-reference proposal;
- validation support;
- repair recommendation;
- review preparation;
- implementation support;
- workflow support.

Model output MUST remain reviewable where it affects governed meaning, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, or downstream use.

### 12.4 Prompt and Instruction Boundaries

Prompts and instructions may guide agent behavior.

Prompts and instructions do not override The Brain Standard.

An agent MUST NOT follow a prompt or instruction that conflicts with higher-authority standards, Privacy Classification, authority boundaries, lifecycle requirements, validation expectations, workflow requirements, or governance expectations.

Prompt content SHOULD remain distinguishable from governed knowledge unless a future standard or specification explicitly defines how prompt material becomes governed material.

An agent MUST NOT treat hidden prompt context, system instructions, tool instructions, model memory, chat history, implementation state, or undocumented operating assumptions as governed truth unless the relevant meaning is explicit, portable, inspectable, and governed.

### 12.5 Implementation State

Implementation State describes how a specific software environment displays, indexes, caches, routes, stores, hides, locks, synchronizes, publishes, exports, imports, migrates, or otherwise manages governed material.

Implementation State MAY support agent work.

Implementation State MUST NOT define governed meaning by itself.

An agent MUST NOT treat implementation display state, plugin metadata, database row state, UI status, file color, icon, tag, sort order, graph position, search ranking, cache state, index state, model memory, workflow queue, or tool status as Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication permission, export permission, migration permission, deletion permission, or governance acceptance.

### 12.6 Tool-Generated and Implementation-Generated Files

Tools and implementations MAY generate files, indexes, caches, logs, reports, previews, sidecar records, embeddings, summaries, exports, migration files, or other artifacts.

Generated files MUST remain distinguishable from governed source material, Knowledge Records, governed documents, approved outputs, validation records, archives, backups, imports, exports, and migrations where that distinction affects interpretation or downstream use.

An agent MUST NOT treat a generated file as authoritative merely because it was created by an implementation, tool, model, script, plugin, workflow, validator, or automation.

Generated files SHOULD preserve provenance, privacy boundaries, validation context, source context, and review state where those affect governed handling.

### 12.7 Tool Logs, Agent Logs, and Hidden State

Logs and hidden state MAY support troubleshooting, audit, validation, implementation behavior, or workflow operation.

Logs and hidden state MUST NOT become governed meaning by themselves.

An agent MUST NOT rely on hidden logs, hidden tool state, hidden application state, hidden model memory, hidden prompt context, hidden workflow memory, hidden database internals, or hidden plugin behavior as the sole source of governed meaning.

Where logs affect provenance, validation, review, auditability, security, privacy, export, migration, or governance, their relevant meaning SHOULD be made explicit, inspectable, and governed.

Logs MUST preserve Privacy Classification where they include or reveal restricted material.

### 12.8 Model Replacement and Agent Portability

The Brain Standard MUST remain valid when a model, provider, prompt system, tool, plugin, script, runtime, implementation, workflow engine, interface, index, cache, or database is replaced.

An agent design SHOULD support replacement without loss of:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage context;
- workflow context;
- review context;
- compatibility expectations.

Agent portability is successful when agent responsibilities, permissions, outputs, validation expectations, privacy requirements, and review requirements can be preserved across implementations.

### 12.9 Implementation-Specific Agent Profiles

A future implementation profile MAY define how a specific implementation realizes AG-0001.

An implementation-specific agent profile MAY define:

- tool configuration;
- model choices;
- prompt templates;
- file paths;
- repository behavior;
- validation scripts;
- logging behavior;
- permission files;
- runtime behavior;
- user-interface behavior;
- operational procedures;
- integration methods;
- implementation-specific constraints.

An implementation-specific agent profile MUST remain subordinate to AG-0001 and higher-authority standards.

An implementation profile MUST NOT redefine agent permissions, privacy boundaries, authority behavior, lifecycle behavior, validation meaning, storage meaning, workflow meaning, or governance unless a governed standard or specification explicitly permits that behavior.

### 12.10 Implementation, Tool, and Model Success Criteria

Agent interaction with implementations, tools, and models conforms to AG-0001 when:

- no specific implementation becomes required by the standard;
- tool capability does not become governed permission;
- model output does not become governed meaning by itself;
- prompts do not override higher-authority standards;
- implementation state does not define Object Identity, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, publication, export, migration, deletion, or governance;
- generated files remain distinguishable from governed material;
- logs and hidden state do not become hidden architecture;
- privacy boundaries are preserved;
- agent behavior remains portable across models, tools, workflows, storage systems, and implementations.

Agent implementation interaction is successful when agents can use practical tools without creating model lock-in, tool lock-in, implementation lock-in, hidden governance, or standard drift.

## 13. Agent Logging, Auditability, and Traceability

Agent Logging, Auditability, and Traceability define how agent activity may be recorded, inspected, reviewed, validated, corrected, preserved, limited, or excluded within The Brain Standard.

Logging exists because agent activity may affect governed material, review decisions, validation findings, storage movement, workflow routing, import preparation, export preparation, migration preparation, publication preparation, deletion recommendations, privacy exposure, implementation behavior, or downstream use.

Auditability exists because future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations must be able to determine whether agent activity stayed within scope and preserved the applicable standards.

Traceability exists because agent activity should not become hidden governance.

Agent Logging, Auditability, and Traceability are successful when agent activity can be inspected without exposing restricted information, creating hidden authority, weakening privacy, or making implementation-specific logs the source of governed meaning.

### 13.1 Logging Purpose

Agent logs MAY support:

- review;
- validation;
- provenance;
- troubleshooting;
- workflow coordination;
- storage movement review;
- permission review;
- privacy review;
- security review;
- import review;
- export review;
- migration review;
- publication review;
- deletion review;
- conformance review;
- governance review;
- recovery.

Agent logs SHOULD exist where agent activity affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, workflow behavior, publication, export, migration, deletion, or downstream use.

Agent logs MUST NOT become governed meaning by themselves.

A missing log does not automatically invalidate a governed entity unless the applicable standard, specification, workflow, validation rule, or governance process requires that log.

A present log does not automatically prove correctness, approval, authority, validation success, privacy clearance, publication readiness, export readiness, migration readiness, deletion permission, or governance acceptance.

### 13.2 Log Scope

Log Scope defines what agent activity is being recorded or made auditable.

Log Scope MAY include:

- agent identity or role;
- agent task;
- permission scope;
- access scope;
- workflow stage;
- Source Material used;
- Knowledge Records used;
- governed documents used;
- metadata inspected or changed;
- relationships inspected or changed;
- Source References inspected or changed;
- provenance inspected or changed;
- Lifecycle State inspected or proposed;
- Authority Level inspected or proposed;
- Privacy Classification inspected or proposed;
- Validation checked or proposed;
- storage movement;
- import preparation;
- export preparation;
- migration preparation;
- publication preparation;
- deletion recommendation;
- escalation;
- review result;
- implementation interaction;
- future governed log scope.

Log Scope SHOULD be explicit where the log affects interpretation, review, validation, privacy, authority, lifecycle handling, publication, export, migration, deletion, governance, or downstream use.

A log entry MUST NOT imply broader scope than it actually records.

### 13.3 Minimum Traceability Expectations

Where traceability is required, an agent activity record SHOULD identify or support identification of:

- what agent acted;
- what task or instruction applied;
- what permission scope applied;
- what governed entity was involved;
- what source material was used where applicable;
- what action was proposed or performed;
- what output was produced;
- whether the action was read-only, proposed, applied, escalated, rejected, reverted, approved, archived, or superseded;
- what validation occurred where applicable;
- what review occurred where applicable;
- what uncertainty or limitation remains where applicable;
- what downstream use is permitted or prohibited where applicable.

Traceability SHALL be preserved where agent activity affects critical knowledge changes.

Traceability MUST preserve Privacy Classification.

### 13.4 Agent Activity Records

An Agent Activity Record is a record of agent activity that supports review, provenance, validation, auditability, workflow coordination, or governance.

An Agent Activity Record MAY include:

- agent name, role, or identifier;
- instruction or task summary;
- permission scope;
- operation type;
- affected governed entity;
- source context;
- output reference;
- validation result;
- review state;
- escalation state;
- privacy boundary;
- authority boundary;
- lifecycle context;
- storage context;
- implementation context;
- timestamp where applicable;
- future governed activity-record fields.

Agent Activity Records SHOULD be structured enough for humans and agents to interpret.

Agent Activity Records MUST NOT expose restricted material beyond the permitted scope.

Agent Activity Records MUST NOT replace Source References, provenance records, validation records, review records, lifecycle records, authority records, privacy records, workflow records, or governance records where those are required separately.

### 13.5 Auditability Requirements

Agent activity SHOULD be auditable where it affects:

- governed meaning;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- approval;
- rejection;
- publication;
- export;
- migration;
- deletion;
- archival;
- backup;
- restoration;
- synchronization;
- indexing;
- implementation exposure;
- downstream use.

Auditability means that a reviewer can determine what happened, what scope applied, what evidence was used, what output was produced, what review occurred, and whether the activity conformed to the applicable standards.

Auditability MUST NOT require reliance on hidden model memory, hidden prompt context, hidden tool state, hidden application state, hidden workflow memory, hidden database internals, or undocumented implementation behavior.

Where hidden state is relevant, its governed meaning SHOULD be made explicit, portable, inspectable, and reviewable.

### 13.6 Privacy-Preserving Logs

Logs may expose restricted material.

Agent logs MUST preserve Privacy Classification.

An agent MUST NOT log restricted content into an unrestricted log, unrestricted cache, unrestricted index, unrestricted generated file, unrestricted export, unrestricted publication draft, unrestricted migration package, or unrestricted implementation display.

Where full logging would expose restricted material, the agent SHOULD use privacy-preserving logging.

Privacy-preserving logging MAY include:

- redaction;
- restricted references;
- scoped identifiers;
- safe summaries;
- access-controlled log areas;
- separation between public findings and restricted details;
- escalation without exposing restricted content;
- future governed privacy-preserving log methods.

A privacy-preserving log SHOULD preserve enough context for authorized review without exposing restricted details to unauthorized users, agents, workflows, implementations, or downstream systems.

### 13.7 Logs and Provenance

Agent logs MAY support provenance.

Agent logs are not automatically provenance records.

A provenance record SHOULD remain explicit where provenance affects interpretation, authority, privacy, validation, publication, export, migration, governance, or downstream use.

Agent logs MUST NOT fabricate provenance.

Agent logs MUST NOT replace Source References.

Agent logs MUST NOT weaken source traceability.

Where logs are used to support provenance, the relevant provenance meaning SHOULD be explicit, reviewable, and compatible with the Source Reference and Provenance Standard.

### 13.8 Logs and Validation

Agent logs MAY support validation.

Agent logs are not validation acceptance by themselves.

A validation process MAY inspect agent logs to determine whether agent activity stayed within scope, preserved privacy, preserved provenance, avoided hidden governance, and respected the applicable standards.

A log entry MUST NOT make an activity valid merely because the activity was recorded.

A missing log SHOULD be escalated where required traceability is absent and the absence affects meaning, authority, privacy, validation, publication, export, migration, deletion, governance, or downstream use.

### 13.9 Logs and Retention

Agent logs SHOULD be retained where retention is required for review, provenance, validation, auditability, security, recovery, governance, or downstream use.

Agent logs SHOULD NOT be retained indefinitely where retention creates privacy, security, storage, legal, governance, or operational risk without a governed reason.

A future specification MAY define log retention rules, deletion rules, redaction rules, archive rules, backup rules, export rules, migration rules, and validation rules.

Such rules MUST preserve Privacy Classification, provenance expectations, reviewability, auditability, and implementation independence.

### 13.10 Logging and Auditability Success Criteria

Agent logging, auditability, and traceability conform to AG-0001 when:

- agent activity remains inspectable where required;
- logs preserve scope;
- logs preserve Privacy Classification;
- logs do not become governed meaning by themselves;
- logs do not replace Source References or provenance records where those are required;
- hidden state does not become hidden governance;
- auditability does not require a specific implementation;
- traceability supports review, validation, recovery, and governance;
- restricted information is not exposed through logs;
- missing required traceability is escalated where needed.

Agent logging is successful when it makes agent assistance accountable without creating privacy leakage, implementation lock-in, hidden authority, or audit noise.

## 14. Agent Governance and Evolution

Agent Governance and Evolution define how agent-related rules, permissions, behavior, specifications, implementation profiles, workflow integrations, validation expectations, and operating boundaries may change over time within The Brain Standard.

Agent behavior will evolve as models, tools, workflows, storage systems, implementations, and user needs evolve.

Governance exists to ensure that agent evolution does not create silent authority creep, privacy drift, validation drift, workflow drift, implementation lock-in, or standard drift.

Agent Governance and Evolution are successful when agent behavior can improve over time while remaining subordinate to the constitutional foundation, Knowledge Standards, Storage Standards, future Workflow Standards, implementation profiles, and governed review processes.

### 14.1 Governance Scope

Agent Governance Scope MAY include:

- agent boundaries;
- agent permissions;
- agent access rules;
- agent operation categories;
- allowed operations;
- prohibited operations;
- Agent Output handling;
- Agent Provenance;
- review requirements;
- escalation requirements;
- validation expectations;
- privacy handling;
- security handling;
- storage interaction;
- workflow interaction;
- implementation interaction;
- tool interaction;
- model interaction;
- logging expectations;
- auditability expectations;
- failure handling;
- recovery behavior;
- implementation-specific agent profiles;
- future governed agent concerns.

Agent Governance Scope SHOULD be explicit where a governance decision affects interpretation, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, workflow behavior, implementation behavior, or downstream use.

### 14.2 Authority of Agent Standards

AG-0001 is a standard-level document within Phase 3 — Agent Framework.

AG-0001 may define agent operating boundaries, permission expectations, output handling, provenance requirements, review requirements, validation expectations, privacy handling, storage interaction rules, workflow interaction rules, implementation interaction rules, logging expectations, auditability expectations, and prohibited operations.

AG-0001 MUST remain subordinate to constitutional documents.

AG-0001 MUST remain compatible with the Phase 1 Knowledge Standards and Phase 2 Storage Standards.

Future agent specifications, templates, implementation profiles, operational guides, prompts, tools, scripts, validators, or workflows MUST NOT contradict AG-0001 unless AG-0001 is formally revised or a higher-authority governance process explicitly permits a limited exception.

### 14.3 Agent Specification Evolution

Future agent specifications MAY define more exact requirements for:

- agent roles;
- permission profiles;
- access profiles;
- prompt templates;
- output schemas;
- provenance fields;
- review states;
- escalation formats;
- validation rules;
- logging rules;
- tool-use rules;
- implementation profiles;
- workflow integrations;
- import handling;
- export handling;
- migration handling;
- publication handling;
- destructive-action handling;
- recovery behavior.

Agent specifications MUST remain subordinate to AG-0001 and higher-authority standards.

Agent specifications MUST NOT make implementation-specific behavior the standard itself.

Agent specifications SHOULD identify their dependencies, scope, authority level, supersession behavior, and validation expectations.

### 14.4 Implementation Profile Evolution

Implementation profiles MAY define how a specific implementation realizes agent behavior.

An implementation profile MAY define:

- supported tools;
- supported models;
- supported prompts;
- supported file paths;
- supported permission files;
- supported workflow integrations;
- supported validation scripts;
- supported log locations;
- supported storage areas;
- supported review interfaces;
- supported import methods;
- supported export methods;
- supported migration methods;
- supported publication methods;
- operational procedures;
- implementation constraints.

Implementation profiles MUST remain subordinate to AG-0001 and higher-authority standards.

An implementation profile MUST NOT silently redefine agent authority, privacy boundaries, validation meaning, lifecycle behavior, storage meaning, workflow meaning, Object Identity, Source References, provenance, publication permission, export permission, migration permission, deletion permission, or governance.

### 14.5 Agent Behavior Changes

Agent behavior MAY change when models, tools, prompts, workflows, storage systems, implementations, or standards evolve.

Agent behavior changes SHOULD be reviewed where they affect:

- governed meaning;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- review behavior;
- escalation behavior;
- publication;
- export;
- migration;
- deletion;
- storage movement;
- workflow behavior;
- implementation behavior;
- downstream use.

An agent behavior change MUST NOT silently expand permissions.

An agent behavior change MUST NOT silently weaken privacy.

An agent behavior change MUST NOT silently convert proposals into approvals.

An agent behavior change MUST NOT silently convert validation support into validation acceptance.

An agent behavior change MUST NOT silently make a model, tool, workflow, or implementation authoritative.

### 14.6 Drift Detection

Agent drift occurs when agent behavior begins to diverge from the applicable standards, specifications, workflows, permissions, privacy boundaries, validation expectations, or governance rules.

Agent drift MAY include:

- authority creep;
- privacy drift;
- validation drift;
- lifecycle drift;
- relationship drift;
- provenance drift;
- storage drift;
- workflow drift;
- implementation drift;
- prompt drift;
- model drift;
- tool drift;
- logging drift;
- review drift;
- escalation drift.

Agents, workflows, validators, implementations, and humans SHOULD support detection of agent drift where drift affects governed meaning, privacy, authority, validation, lifecycle state, publication, export, migration, deletion, governance, or downstream use.

Detected drift SHOULD be escalated, reviewed, corrected, documented, or governed.

### 14.7 Governance Records

Governance decisions affecting agent behavior SHOULD be recorded where the decision affects interpretation, permissions, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, workflow behavior, implementation behavior, or downstream use.

Governance records SHOULD identify or support identification of:

- what decision was made;
- what scope applied;
- what standard, specification, workflow, or implementation profile was affected;
- what agent behavior was affected;
- what reason supported the decision;
- what review occurred where applicable;
- what validation occurred where applicable;
- what privacy boundary applies;
- what authority boundary applies;
- what implementation impact exists;
- what downstream use is permitted or prohibited;
- what supersession or revision effect applies.

Governance records MUST preserve Privacy Classification.

Governance records MUST NOT rely solely on hidden implementation state, model memory, workflow memory, user habit, or undocumented practice.

### 14.8 Deprecation and Supersession of Agent Rules

Agent rules, permission profiles, implementation profiles, prompts, workflows, validators, scripts, tools, or operational procedures MAY be deprecated, superseded, replaced, or archived through a governed process.

Deprecation MUST NOT erase provenance.

Supersession MUST NOT create identity confusion.

Replacement MUST NOT weaken privacy.

Archival MUST NOT imply deletion.

A deprecated or superseded agent rule MUST NOT continue to govern current behavior unless the applicable governance process explicitly permits limited continued use.

Deprecated or superseded behavior SHOULD remain traceable where it affects historical interpretation, validation, auditability, migration, export, publication, or downstream use.

### 14.9 Governance and Human Review

Human review SHALL remain available for critical changes to agent governance.

Critical agent-governance changes MAY include changes that affect:

- agent authority;
- privacy handling;
- validation acceptance;
- lifecycle transitions;
- Object Identity handling;
- Source Reference handling;
- provenance handling;
- publication behavior;
- export behavior;
- migration behavior;
- deletion behavior;
- automatic approval;
- implementation compliance;
- workflow authority;
- downstream use.

A future governed workflow MAY define limited automatic governance actions only where the action is bounded, reversible where practical, validated, privacy-respecting, traceable, compatible, and explicitly permitted.

### 14.10 Governance and Evolution Success Criteria

Agent Governance and Evolution conform to AG-0001 when:

- agent rules remain subordinate to higher-authority standards;
- future specifications do not silently contradict AG-0001;
- implementation profiles do not redefine the standard;
- behavior changes remain reviewable where needed;
- permissions do not silently expand;
- privacy does not silently weaken;
- validation support does not silently become approval;
- proposals do not silently become final governed decisions;
- drift can be detected and escalated;
- governance records preserve scope, provenance, and Privacy Classification;
- deprecated and superseded agent behavior remains traceable where needed.

Agent governance is successful when agents can evolve without causing authority creep, privacy drift, validation drift, implementation lock-in, workflow confusion, or standard drift.

## 15. Agent Failure Modes and Recovery

Agent Failure Modes and Recovery define how The Brain Standard recognizes, contains, reviews, corrects, reverts, repairs, escalates, or learns from agent failures.

Agents may fail because of incomplete context, incorrect inference, source ambiguity, privacy confusion, authority confusion, validation gaps, storage ambiguity, workflow ambiguity, implementation behavior, model limitations, prompt ambiguity, tool errors, permission mismatch, or governance drift.

Failure handling exists so that agent errors do not silently become governed meaning.

Recovery exists so that agent-assisted systems can restore trust, preserve provenance, protect privacy, repair damage, and prevent recurrence.

Agent Failure Modes and Recovery are successful when failures remain visible, bounded, reviewable, correctable, privacy-respecting, and subordinate to governance.

### 15.1 Agent Failure Definition

An Agent Failure occurs when agent activity does not conform to the applicable standard, specification, workflow, permission scope, privacy boundary, authority boundary, validation expectation, storage rule, implementation profile, or governed instruction.

An Agent Failure MAY include:

- unauthorized access;
- unauthorized exposure;
- incorrect summary;
- incorrect extraction;
- fabricated Source Reference;
- missing provenance;
- broken provenance;
- incorrect metadata;
- incorrect relationship;
- Object Identity confusion;
- lifecycle-state confusion;
- authority overreach;
- privacy violation;
- validation overreach;
- storage movement error;
- workflow-routing error;
- export error;
- publication error;
- migration error;
- destructive-action error;
- implementation-lock-in;
- hidden governance;
- failure to escalate;
- another governed failure mode.

An Agent Failure MUST NOT be ignored merely because the output appears useful.

### 15.2 Failure Severity

Agent failures SHOULD be categorized by severity where severity affects review, escalation, correction, quarantine, rollback, privacy handling, validation, governance, or downstream use.

Failure severity MAY include:

- informational issue;
- minor issue;
- warning;
- validation issue;
- review-blocking issue;
- privacy issue;
- authority issue;
- lifecycle issue;
- source-reference issue;
- provenance issue;
- identity issue;
- destructive-action issue;
- export issue;
- publication issue;
- migration issue;
- governance issue;
- critical issue;
- future governed severity type.

A future specification MAY define exact severity levels.

Severity levels MUST remain subordinate to Privacy Classification, Authority Level, Lifecycle State, Validation, governance, and human review requirements.

### 15.3 Containment

Containment limits the effect of an Agent Failure.

Containment MAY include:

- stopping further agent action;
- limiting access;
- removing output from downstream use;
- marking output as disputed;
- marking output as needs repair;
- quarantine;
- reverting a change;
- pausing a workflow;
- blocking export;
- blocking publication;
- blocking migration;
- blocking deletion;
- restricting indexes or caches;
- escalating to human review;
- preserving evidence for audit;
- creating a recovery record.

An agent SHOULD contain failures where continued action may affect governed meaning, privacy, authority, validation, lifecycle state, publication, export, migration, deletion, governance, or downstream use.

An agent MUST NOT silently continue after detecting a critical failure unless a governed workflow explicitly permits continued limited action.

### 15.4 Escalation of Failures

An agent SHOULD escalate failures where the failure affects or may affect:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- review state;
- publication;
- export;
- migration;
- deletion;
- storage integrity;
- workflow integrity;
- implementation integrity;
- governance;
- downstream use.

An agent MUST escalate privacy violations, authority overreach, fabricated Source References, destructive-action errors, unauthorized publication, unauthorized export, unauthorized migration, and hidden governance risks.

Escalation SHOULD preserve enough context for authorized review without exposing restricted information beyond the applicable privacy boundary.

### 15.5 Reversion and Repair

Reversion returns a governed entity, storage representation, workflow state, validation state, implementation state, or Agent Output to a prior acceptable state where practical.

Repair corrects a failure while preserving governed meaning, provenance, privacy, validation, auditability, and compatibility.

An agent MAY recommend reversion or repair.

An agent MAY perform bounded reversion or repair only when explicitly authorized by scope, workflow, permission model, privacy classification, validation expectation, and governance process.

Reversion and repair MUST preserve Object Identity unless an explicit governed identity-change process permits otherwise.

Reversion and repair SHOULD preserve evidence of the failure where needed for auditability, validation, governance, recovery, or future prevention.

### 15.6 Quarantine and Restricted Handling

Quarantine separates material that may be unsafe, invalid, privacy-risky, authority-risky, source-uncertain, corrupted, misleading, or otherwise unsuitable for normal downstream use.

An agent MAY recommend quarantine.

An agent MAY place material into quarantine only where explicitly authorized.

Quarantine MUST NOT be treated as deletion.

Quarantine MUST NOT automatically resolve the underlying issue.

Quarantine MUST preserve Privacy Classification.

Quarantine SHOULD preserve enough provenance and context for authorized review.

Material in quarantine MUST NOT be exported, published, migrated, indexed for unrestricted use, used as authority, treated as validated, or used downstream unless a governed review or workflow permits that action.

### 15.7 Recovery Records

A Recovery Record documents a failure, containment action, repair action, reversion action, escalation, review outcome, or governance decision related to agent failure.

A Recovery Record SHOULD identify or support identification of:

- what failed;
- what agent activity was involved;
- what governed entity was affected;
- what scope applied;
- what privacy boundary applied;
- what authority boundary applied;
- what validation scope applied;
- what workflow was involved;
- what implementation was involved where applicable;
- what containment occurred;
- what repair or reversion occurred;
- what review occurred;
- what unresolved issue remains;
- what downstream use is permitted or prohibited.

Recovery Records MUST preserve Privacy Classification.

Recovery Records MUST NOT fabricate provenance, hide errors, or erase auditability.

### 15.8 Learning From Failure

Agent failures MAY inform future improvements to standards, specifications, workflows, validators, permission profiles, implementation profiles, prompts, tools, scripts, storage layouts, training examples, review procedures, or operational guidance.

Learning from failure MUST NOT convert a one-time workaround into a governed rule without governance.

Learning from failure MUST NOT weaken privacy, authority, validation, lifecycle handling, provenance, Source References, storage meaning, workflow meaning, implementation independence, or human reviewability.

Repeated failures SHOULD be reviewed for drift, unclear standards, insufficient permissions, inadequate validation, poor workflow design, unsafe tool use, implementation mismatch, or governance gaps.

### 15.9 Recovery and Downstream Use

Agent failures may affect downstream use.

Where downstream use may be affected, recovery SHOULD identify:

- what downstream outputs relied on the failed agent activity;
- what Knowledge Records may be affected;
- what metadata may be affected;
- what relationships may be affected;
- what Source References may be affected;
- what provenance may be affected;
- what validation results may be affected;
- what privacy exposure may have occurred;
- what publication, export, or migration packages may be affected;
- what implementation outputs may be affected;
- what corrective action is required.

An agent MUST NOT allow known failed output to remain in downstream use without review where the failure affects governed meaning, privacy, authority, validation, publication, export, migration, deletion, or governance.

### 15.10 Failure and Recovery Success Criteria

Agent failure handling conforms to AG-0001 when:

- failures remain visible where needed;
- failures are contained where risk requires containment;
- failures are escalated where required;
- privacy is preserved during failure handling;
- Source References and provenance are not fabricated or erased;
- Object Identity is preserved during recovery;
- reversion and repair remain reviewable where needed;
- quarantine does not become deletion;
- logs and recovery records support auditability;
- downstream effects are considered;
- repeated failures inform governed improvement rather than undocumented workaround behavior.

Agent recovery is successful when agent errors can be corrected without weakening knowledge meaning, source traceability, privacy, authority, validation, lifecycle handling, storage meaning, workflow meaning, implementation independence, or governance.

## 16. Agent Conformance Requirements

Agent Conformance Requirements define how agent behavior, Agent Output, agent permissions, agent operations, agent-supported workflows, implementation-specific agent profiles, and future agent specifications are evaluated against AG-0001.

Conformance exists so that humans, agents, workflows, validators, storage systems, implementations, import processes, export processes, migration processes, publication processes, and governance processes can determine whether an agent is operating within The Brain Standard.

Agent conformance MUST be evaluated within a defined scope.

A conformance claim MUST NOT imply broader conformance than the evaluated scope supports.

An agent, workflow, implementation, tool, model, prompt, script, validator, or implementation profile conforms to AG-0001 only when it preserves the operating boundaries defined by this document and the higher-authority standards.

Agent Conformance Requirements are successful when conformance can be tested, reviewed, explained, preserved, and migrated without depending on hidden model behavior, hidden implementation state, undocumented practice, or unreviewable agent authority.

### 16.1 Conformance Scope

Conformance Scope defines what is being evaluated for AG-0001 conformance.

Conformance Scope MAY include:

- an agent role;
- an agent task;
- an agent workflow;
- an agent permission profile;
- an agent access profile;
- an Agent Output type;
- an Agent Activity Record;
- an implementation-specific agent profile;
- a tool integration;
- a model integration;
- a prompt template;
- a validation rule;
- a storage interaction;
- a workflow interaction;
- an import process;
- an export process;
- a migration process;
- a publication process;
- a deletion or cleanup process;
- a logging process;
- a recovery process;
- a full implementation environment;
- a future governed conformance scope.

A conformance claim SHALL identify scope where scope affects interpretation, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, governance, or downstream use.

Partial conformance MUST remain distinguishable from full conformance.

Tool-specific conformance MUST remain distinguishable from standard-level conformance.

Implementation-specific conformance MUST remain distinguishable from The Brain Standard itself.

### 16.2 Required Preservation

An agent conforms to AG-0001 only when agent activity preserves or supports preservation of:

- governed meaning;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- source distinction;
- Knowledge Record distinction;
- governed document distinction;
- draft, review, and approval boundaries;
- storage boundaries;
- workflow boundaries;
- implementation independence;
- human reviewability;
- traceability;
- portability;
- governed evolution.

An agent MUST NOT weaken a required preservation concern for convenience, speed, automation quality, search quality, summarization quality, implementation convenience, model preference, tool capability, workflow convenience, or user-interface convenience.

### 16.3 Permission Conformance

An agent conforms to AG-0001 only when permissions remain scoped, explicit where required, reviewable, and subordinate to higher-authority standards.

Permission conformance requires that:

- access is not treated as authority;
- visibility is not treated as permission;
- searchability is not treated as permission;
- tool capability is not treated as governed permission;
- model capability is not treated as governed permission;
- implementation access is not treated as unrestricted permission;
- permissions do not silently inherit across scopes;
- revoked, expired, superseded, rejected, or invalid permissions are not used;
- high-risk permissions are reviewed or governed where required.

A permission model MUST NOT allow agents to silently approve, reject, declassify, publish, export, migrate, delete, overwrite, supersede, or reinterpret governed material outside an authorized scope.

### 16.4 Operation Conformance

Agent operations conform to AG-0001 only when they remain within authorized scope and preserve the applicable boundaries.

Allowed operations MUST remain bounded.

Prohibited operations MUST remain prohibited unless a future higher-authority governance process, standard, specification, or governed workflow explicitly permits a limited exception within a defined scope.

High-risk operations SHOULD require explicit authorization, traceability, validation, privacy review, governed workflow review, human review, or a combination of these controls.

High-risk operations include:

- Object Identity changes;
- lifecycle transitions;
- authority assignments;
- privacy classification changes;
- validation acceptance;
- publication;
- export;
- migration;
- deletion;
- destructive cleanup;
- automatic approval;
- implementation compliance claims;
- governance changes.

An agent operation MUST NOT silently convert technical capability into governed authority.

### 16.5 Agent Output Conformance

Agent Output conforms to AG-0001 only when output remains distinguishable from source material, human-authored material, reviewed material, approved material, authoritative material, validation acceptance, publication approval, export approval, migration approval, and final governed decisions.

Agent Output conformance requires that:

- agent origin remains identifiable where needed;
- output category is clear where needed;
- output scope is clear where needed;
- proposals remain distinguishable from approvals;
- summaries remain distinguishable from Source Material;
- extractions remain distinguishable from complete source representation;
- validation support remains distinguishable from validation acceptance;
- confidence remains distinguishable from Authority Level;
- review state remains distinguishable from Lifecycle State;
- storage location does not define output meaning;
- privacy boundaries are preserved;
- provenance is preserved where required.

Agent Output MUST NOT become authoritative merely because it is plausible, useful, repeated, fluent, validated by a tool, surfaced by an implementation, or produced by a preferred model.

### 16.6 Privacy and Security Conformance

Agent privacy and security handling conforms to AG-0001 only when Privacy Classification and security-sensitive handling are preserved.

Privacy and security conformance requires that:

- restricted material is not accessed outside authorized scope;
- restricted material is not exposed beyond permitted boundaries;
- summaries preserve privacy;
- metadata preserves privacy;
- relationships preserve privacy;
- Source References and provenance preserve privacy;
- validation findings preserve privacy;
- logs preserve privacy;
- indexes, caches, embeddings, and generated files preserve privacy;
- exports, publications, and migrations preserve privacy;
- security-sensitive material is not exposed without governed permission;
- privacy risks are escalated where required.

Agent usefulness MUST NOT override Privacy Classification.

Where privacy and agent usefulness conflict, privacy SHALL take precedence.

### 16.7 Validation and Review Conformance

Agent validation and review conform to AG-0001 only when validation support, review preparation, workflow routing, and implementation visibility remain distinguishable from approval.

Validation and review conformance requires that:

- validation scope is clear;
- validation findings remain reviewable;
- validation support does not silently become validation acceptance;
- review preparation does not silently become review completion;
- workflow completion does not silently become approval;
- implementation visibility does not silently become approval;
- human review remains available for critical knowledge changes;
- review outcomes preserve scope;
- review provenance is preserved where required;
- rejected, deferred, quarantined, or needs-repair outputs are not treated as approved.

Validation success MUST NOT become Authority Level, Lifecycle State approval, Privacy Classification approval, publication readiness, export readiness, migration readiness, deletion permission, or governance acceptance unless a future governed workflow explicitly defines that result within a limited scope.

### 16.8 Implementation Independence Conformance

Agent implementation behavior conforms to AG-0001 only when the standard remains independent of any specific model, provider, prompt system, tool, plugin, runtime, API, script, vault, repository, database, file system, workflow engine, index, cache, interface, or application.

Implementation independence conformance requires that:

- no specific model becomes required by the standard;
- no specific tool becomes required by the standard;
- no specific prompt becomes required by the standard;
- no specific implementation becomes required by the standard;
- implementation state does not define governed meaning;
- hidden state does not define governed meaning;
- logs and generated files do not become hidden architecture;
- agent behavior remains portable across implementations;
- replacement of a model, tool, prompt, workflow engine, or implementation does not invalidate governed meaning.

A specific implementation MAY realize AG-0001 through an implementation profile.

That profile MUST remain subordinate to AG-0001 and higher-authority standards.

### 16.9 Conformance Evidence

Conformance evidence MAY include:

- reviewed agent behavior;
- permission records;
- access records;
- Agent Activity Records;
- Agent Output records;
- validation reports;
- review records;
- escalation records;
- workflow records;
- privacy review records;
- audit logs;
- recovery records;
- implementation profiles;
- tool configuration records;
- migration reports;
- export reports;
- publication review records;
- governance records.

Conformance evidence SHOULD preserve enough context to support review without exposing restricted material beyond the permitted scope.

Conformance evidence MUST NOT fabricate approval, authority, validation, privacy clearance, lifecycle transition, publication permission, export permission, migration permission, deletion permission, or governance acceptance.

### 16.10 Agent Conformance Success Criteria

Agent conformance satisfies AG-0001 when:

- conformance scope is clear;
- agent activity remains within authorized boundaries;
- Object Identity is preserved;
- metadata, relationships, Source References, and provenance are preserved;
- Lifecycle State, Authority Level, Privacy Classification, and Validation remain distinct;
- Agent Output remains distinguishable from approved governed material;
- privacy and security boundaries are preserved;
- validation support does not become approval;
- tool capability does not become permission;
- implementation behavior does not become the standard;
- logs and traceability support review without creating hidden authority;
- failures are visible, containable, and recoverable;
- governance remains explicit.

Agent conformance is successful when agent assistance remains useful, bounded, reviewable, traceable, privacy-respecting, validation-compatible, portable, and subordinate to The Brain Standard.

## 17. Agent Non-Conformance and Exceptions

Agent Non-Conformance and Exceptions define how failures to conform to AG-0001 are identified, classified, contained, reviewed, corrected, documented, and governed.

Non-conformance exists because agents, tools, models, prompts, workflows, implementations, validators, storage systems, and users may fail to preserve the required boundaries of The Brain Standard.

Exceptions exist because future standards, specifications, workflows, or implementation profiles may permit limited deviations or controlled special handling.

A non-conformance MUST NOT be ignored merely because the agent output appears useful.

An exception MUST NOT become a general rule unless adopted through governance.

Agent Non-Conformance and Exceptions are successful when deviations remain visible, bounded, reviewable, privacy-respecting, traceable, and correctable.

### 17.1 Non-Conformance Definition

Agent Non-Conformance occurs when agent activity, Agent Output, agent permissions, agent operations, agent-supported workflows, implementation-specific behavior, or future agent specifications fail to satisfy AG-0001 within the applicable scope.

Agent Non-Conformance MAY include:

- unauthorized access;
- unauthorized exposure;
- unbounded permission use;
- silent permission inheritance;
- hidden governance;
- authority overreach;
- validation overreach;
- privacy violation;
- source-reference fabrication;
- provenance loss;
- Object Identity confusion;
- relationship confusion;
- metadata corruption;
- lifecycle confusion;
- storage-defined meaning;
- workflow-defined approval;
- implementation-defined meaning;
- model-defined meaning;
- tool-defined permission;
- unreviewed high-risk action;
- missing required traceability;
- failed escalation;
- unrecoverable destructive action;
- unsupported conformance claim;
- another governed non-conformance type.

Non-conformance SHOULD be classified by scope, severity, affected governed entities, affected standards, privacy impact, authority impact, validation impact, lifecycle impact, storage impact, workflow impact, implementation impact, and downstream impact where applicable.

### 17.2 Non-Conformance Severity

Non-conformance severity SHOULD be assigned where severity affects containment, review, validation, privacy handling, recovery, publication, export, migration, deletion, governance, or downstream use.

Severity MAY include:

- informational non-conformance;
- minor non-conformance;
- warning-level non-conformance;
- validation-blocking non-conformance;
- review-blocking non-conformance;
- privacy non-conformance;
- authority non-conformance;
- lifecycle non-conformance;
- source-reference non-conformance;
- provenance non-conformance;
- identity non-conformance;
- destructive-action non-conformance;
- export non-conformance;
- publication non-conformance;
- migration non-conformance;
- governance non-conformance;
- critical non-conformance;
- future governed severity type.

Severity classification MUST NOT reduce Privacy Classification, weaken Authority Level requirements, bypass validation, override human review, or excuse governance requirements.

### 17.3 Non-Conformance Containment

Non-conformance SHOULD be contained where continued use may affect governed meaning, privacy, authority, validation, lifecycle state, publication, export, migration, deletion, governance, or downstream use.

Containment MAY include:

- stopping further agent action;
- limiting agent access;
- marking output as disputed;
- marking output as needs repair;
- quarantining affected material;
- blocking publication;
- blocking export;
- blocking migration;
- blocking deletion;
- restricting indexes or caches;
- reverting a change;
- repairing a change;
- escalating to human review;
- recording the non-conformance;
- opening governance review;
- notifying an authorized reviewer.

Containment MUST preserve Privacy Classification.

Containment MUST NOT erase evidence required for auditability, validation, recovery, or governance.

### 17.4 Non-Conformance Review

Non-conformance SHOULD be reviewed where it affects:

- governed meaning;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage behavior;
- workflow behavior;
- implementation behavior;
- publication;
- export;
- migration;
- deletion;
- downstream use.

Non-conformance review SHOULD determine:

- what failed;
- what scope applied;
- what governed entities were affected;
- what standards were affected;
- what privacy risk exists;
- what authority risk exists;
- what validation risk exists;
- what lifecycle risk exists;
- what downstream use may be affected;
- whether containment is required;
- whether repair or reversion is required;
- whether governance action is required.

Non-conformance review MUST preserve Privacy Classification.

### 17.5 Corrective Action

Corrective action addresses Agent Non-Conformance.

Corrective action MAY include:

- revising Agent Output;
- rejecting Agent Output;
- reverting an agent-generated change;
- repairing metadata;
- repairing relationships;
- repairing Source References;
- repairing provenance;
- correcting Lifecycle State;
- correcting Authority Level handling;
- correcting Privacy Classification handling;
- correcting validation findings;
- correcting storage movement;
- correcting workflow routing;
- correcting implementation behavior;
- updating permission profiles;
- updating prompts;
- updating tools;
- updating validators;
- updating implementation profiles;
- opening governance review.

Corrective action MUST NOT create additional non-conformance.

Corrective action SHOULD preserve evidence of the original non-conformance where needed for auditability, recovery, validation, governance, or future prevention.

### 17.6 Exceptions

An exception is a governed, documented, limited permission to deviate from an AG-0001 requirement within a defined scope.

An exception MAY be allowed only when a higher-authority governance process, future standard, future specification, or governed workflow explicitly permits the exception.

An exception MUST define:

- what requirement is affected;
- what scope applies;
- why the exception exists;
- what risk is accepted;
- what controls apply;
- what review is required;
- what validation is required;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies where applicable;
- what expiration, review, or supersession behavior applies where applicable.

An exception MUST NOT silently become a general rule.

An exception MUST NOT override constitutional documents unless a higher-authority governance process formally permits that change.

### 17.7 Temporary Deviations

A temporary deviation is a short-term exception used to preserve continuity, recover from failure, migrate material, test a controlled implementation, or resolve an operational issue.

A temporary deviation SHOULD be time-bounded, scope-bounded, reviewable, traceable, and reversible where practical.

A temporary deviation MUST preserve Privacy Classification.

A temporary deviation MUST NOT permanently redefine agent authority, validation meaning, lifecycle behavior, storage meaning, workflow meaning, implementation behavior, Object Identity, Source References, provenance, publication permission, export permission, migration permission, deletion permission, or governance.

A temporary deviation SHOULD be resolved by correction, formal exception, governed revision, or rejection.

### 17.8 Exception Records

An Exception Record documents a governed exception or temporary deviation.

An Exception Record SHOULD identify or support identification of:

- what requirement is affected;
- what scope applies;
- what agent, workflow, implementation, tool, model, prompt, or process is affected;
- what governed entities may be affected;
- what risk is accepted;
- what controls apply;
- what review occurred;
- what validation occurred;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies where applicable;
- what expiration or review date applies where applicable;
- what downstream use is permitted or prohibited.

Exception Records MUST preserve Privacy Classification.

Exception Records MUST NOT rely solely on hidden implementation state, model memory, workflow memory, user habit, or undocumented practice.

### 17.9 Non-Conformance and Exception Success Criteria

Agent non-conformance and exceptions conform to AG-0001 when:

- non-conformance is visible where needed;
- non-conformance is classified by scope and severity where needed;
- non-conformance is contained where risk requires containment;
- privacy is preserved during review and correction;
- corrective action does not create additional non-conformance;
- exceptions are explicit, scoped, documented, and governed;
- temporary deviations remain temporary;
- exception records preserve scope, controls, privacy, and review expectations;
- undocumented practice does not become a rule;
- governance remains available for unresolved conflicts.

Non-conformance and exception handling is successful when AG-0001 can tolerate controlled operational reality without permitting silent drift, authority creep, privacy erosion, validation confusion, implementation lock-in, or hidden governance.

## 18. Success Criteria and Closing Rule

Success Criteria and Closing Rule define the final evaluation criteria for AG-0001 and the enduring operating rule that governs agents within The Brain Standard.

AG-0001 succeeds when agents can assist with knowledge work while remaining bounded, reviewable, traceable, privacy-respecting, validation-compatible, implementation-independent, and subordinate to governance.

AG-0001 fails if agents become unreviewable authorities over knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage meaning, workflow meaning, implementation behavior, publication, export, migration, deletion, or governance.

The closing rule exists to preserve the core boundary of the Agent Framework:

Agents may assist.

Agents must not silently govern.

### 18.1 Document-Level Success Criteria

AG-0001 is successful when future humans, agents, workflows, validators, storage systems, implementations, import processes, export processes, migration processes, publication processes, and governance processes can determine:

- what agents may do;
- what agents must not do;
- what permissions agents require;
- what scope limits agent behavior;
- what operations are allowed;
- what operations are prohibited;
- what outputs agents may produce;
- how Agent Output remains distinguishable;
- how Agent Provenance is preserved;
- when review is required;
- when escalation is required;
- when human approval is required;
- how validation applies to agent activity;
- how privacy and security are preserved;
- how storage and workflow interaction remain bounded;
- how tools, models, prompts, and implementations remain subordinate to the standard;
- how logging, auditability, and traceability are handled;
- how governance and evolution are controlled;
- how failures are contained and recovered;
- how conformance, non-conformance, and exceptions are evaluated.

### 18.2 Agent-Level Success Criteria

An agent operating under The Brain Standard is successful when it can:

- reduce cognitive load;
- improve consistency;
- support source review;
- support metadata work;
- support relationship work;
- support Source References and provenance;
- support validation;
- support drafting;
- support review;
- support storage organization;
- support workflow routing;
- support import preparation;
- support export preparation;
- support migration preparation;
- support publication preparation;
- support implementation work;
- support governance review;
- identify risk;
- escalate ambiguity;
- preserve privacy;
- remain bounded by scope;
- remain traceable;
- remain reviewable.

An agent is not successful if usefulness is achieved by weakening standards, bypassing privacy, inventing authority, hiding provenance, replacing review, or creating implementation lock-in.

### 18.3 Knowledge Preservation Success Criteria

AG-0001 succeeds when agent behavior preserves:

- Knowledge Objects;
- Knowledge Records;
- Source Material distinction;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- governed document boundaries;
- draft, review, and approval boundaries;
- storage boundaries;
- workflow boundaries;
- implementation boundaries;
- import context;
- export context;
- migration context;
- publication context;
- archival context;
- backup context;
- downstream-use context.

Agent activity MUST NOT degrade knowledge preservation for automation convenience.

### 18.4 Governance Success Criteria

AG-0001 succeeds when agent behavior remains governed.

Governance success requires that:

- constitutional documents remain higher authority;
- Knowledge Standards remain protected;
- Storage Standards remain protected;
- future Workflow Standards remain protected;
- implementation profiles remain subordinate;
- agent specifications remain subordinate;
- prompts remain subordinate;
- tools remain subordinate;
- models remain subordinate;
- workflows remain subordinate;
- validation support remains distinguishable from approval;
- human review remains available for critical knowledge changes;
- exceptions remain explicit and governed;
- drift can be detected, reviewed, and corrected.

Governance success is lost when agent behavior, implementation behavior, tool capability, model output, workflow convenience, repeated automation, or undocumented practice becomes a hidden rule.

### 18.5 Portability and Implementation Independence Success Criteria

AG-0001 succeeds when agent behavior remains portable across models, tools, workflows, storage systems, and implementations.

Portability and implementation independence require that:

- no specific model is required;
- no specific provider is required;
- no specific prompt system is required;
- no specific tool is required;
- no specific plugin is required;
- no specific workflow engine is required;
- no specific vault is required;
- no specific repository is required;
- no specific database is required;
- no specific file system is required;
- no specific user interface is required;
- no hidden implementation state is required to preserve governed meaning.

Implementation-specific support is allowed.

Implementation-specific authority creep is not allowed.

### 18.6 Human and Agent Collaboration Success Criteria

AG-0001 succeeds when humans and agents can collaborate without confusing assistance with authority.

Human and agent collaboration is successful when:

- humans can inspect agent activity;
- agents can explain or support explanation of their outputs where needed;
- agent proposals remain reviewable;
- human decisions remain distinguishable from agent recommendations;
- agent validation remains distinguishable from validation acceptance;
- agent confidence remains distinguishable from Authority Level;
- agent output remains distinguishable from approved governed material;
- humans can correct agent errors;
- agents can escalate uncertainty;
- critical knowledge changes remain reviewable;
- governance remains accountable.

Agents SHOULD increase capacity without reducing accountability.

### 18.7 Final Closing Rule

AG-0001 establishes the following closing rule:

Agents may read, search, summarize, extract, classify, propose, validate, draft, organize, report, route, and execute bounded workflow steps when authorized.

Agents may assist with storage, workflows, implementations, imports, exports, migrations, publications, reviews, validation, governance, and recovery when authorized.

Agents must preserve Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage boundaries, workflow boundaries, implementation independence, traceability, reviewability, and governance.

Agents must not silently approve, reject, declassify, publish, export, migrate, delete, overwrite, supersede, reinterpret, validate, authorize, govern, or redefine governed material.

Agents may assist.

Agents must not silently govern.
