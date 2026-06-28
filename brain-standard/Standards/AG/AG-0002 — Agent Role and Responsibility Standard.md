# AG-0002 — Agent Role and Responsibility Standard

Document ID: AG-0002
Title: Agent Role and Responsibility Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 3 — Agent Framework
Milestone: 3.2 — Agent Role and Responsibility Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard
Supersedes: None
Superseded By: None
Related: AG-0001 — Agent Operating Boundaries Standard; AG-0003 — Agent Permission and Traceability Standard

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and agent-role responsibility rules are interpreted within AG-0002.

Where conflicts arise between agent roles, agent responsibilities, role outputs, role boundaries, role handoffs, role coordination, role escalation, agent permissions, agent authority, agent confidence, agent-generated output, workflow behavior, storage behavior, implementation behavior, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, import behavior, export behavior, migration behavior, publication behavior, deletion behavior, downstream use, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

AG-0002 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

AG-0002 depends on the Phase 1 Knowledge Standards because agent roles must preserve knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation.

AG-0002 depends on the Phase 2 Storage Standards because agent roles may inspect, classify, recommend, route, or support storage behavior without allowing storage placement to define knowledge meaning.

AG-0002 depends on AG-0001 because agent roles may operate only within governed agent operating boundaries.

AG-0002 defines agent roles and responsibilities at the conceptual standard level.

AG-0002 does not define exact prompts, exact model behavior, exact agent frameworks, exact tool APIs, exact runtime environments, exact permission files, exact activity-log schemas, exact implementation-specific agent configurations, exact workflow automation, exact validation rule syntax, exact storage paths, or exact user-interface behavior.

Those concerns belong to AG-0003, future agent specifications, workflow standards, implementation profiles, operational guides, permission profiles, traceability specifications, validation specifications, templates, and reference implementations.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Agent Framework refers to Layer 3 of The Brain Standard, responsible for defining how agents may interact with knowledge, source material, storage structures, workflow instructions, and implementation environments while preserving reviewability, traceability, privacy, and governance.
- Agent refers to a human-directed or system-directed AI, automation, script, model-driven process, tool-using assistant, workflow participant, or future automated actor that reads, classifies, summarizes, extracts, proposes, validates, drafts, moves, edits, creates, deletes, exports, publishes, migrates, or otherwise acts on governed material.
- Agent Role refers to a standard-level responsibility profile that describes the kind of work an agent may perform or support within a governed scope.
- Subagent refers to a narrower agent instance, tool, process, script, workflow participant, or assistant that performs part of an Agent Role.
- Role Scope refers to the defined responsibility area, inspection target, output type, boundary, workflow context, or governed activity assigned to an Agent Role.
- Role Output refers to a result produced by an Agent Role, including findings, proposals, classifications, reports, recommendations, warnings, summaries, drafts, validation notes, handoff notes, or implementation-support outputs.
- Role Boundary refers to a limit that prevents one Agent Role from silently assuming another role’s responsibility, permission, authority, approval power, validation scope, privacy clearance, or governance effect.
- Role Handoff refers to a traceable transfer of findings, context, assumptions, unresolved issues, review needs, escalation needs, or next-step recommendations from one role, workflow step, or implementation process to another.
- Agent Permission refers to an allowed agent capability within a defined scope.
- Agent Authority refers to governed decision-making power explicitly granted by a standard, specification, workflow, governance process, or permission profile.
- Agent Confidence refers to an agent-generated indication of certainty, probability, classification confidence, extraction confidence, validation confidence, relationship confidence, recommendation confidence, or model confidence.
- Human Review refers to review, correction, acceptance, rejection, approval, or escalation performed by an authorized human.
- Escalation refers to routing a condition, ambiguity, risk, conflict, privacy concern, authority concern, validation issue, destructive action, or critical knowledge change to human review or a governed workflow.
- Governed Entity refers to a Knowledge Object, Knowledge Record, Source Material, Source Reference, provenance record, relationship, metadata record, validation result, lifecycle state, authority assignment, privacy classification, governed document, workflow output, agent output, import record, export record, migration record, decision, or other entity governed by The Brain Standard.
- Critical Knowledge Change refers to a change that affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, governed meaning, publication, export, migration, deletion, supersession, deprecation, or downstream use.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of AG-0002 is to define the core agent and subagent roles used within The Brain Standard.

AG-0001 defines the operating boundaries for agents.

AG-0002 defines the standard-level roles that may operate inside those boundaries.

The Agent Role and Responsibility Standard exists so future humans, agents, workflows, validators, storage systems, implementations, and governance processes can determine:

- what agent roles exist;
- what each role is responsible for;
- what each role may inspect;
- what each role may produce;
- what each role must preserve;
- what each role must escalate;
- what each role must not decide by itself;
- how role separation prevents authority creep;
- how agent work remains reviewable, traceable, privacy-respecting, and implementation-independent.

AG-0002 does not grant permission merely by naming a role.

An agent role defines responsibility.

An agent permission defines allowed action.

An agent output defines a produced result.

An agent review defines inspection or evaluation.

An agent validation result defines a scoped validation finding.

None of these alone define approval, authority, lifecycle transition, privacy clearance, publication readiness, export readiness, migration permission, deletion permission, or governance acceptance unless a governed workflow or future specification explicitly defines that effect within a controlled scope.

AG-0002 exists to prevent role confusion.

Role confusion occurs when a human, agent, workflow, validator, implementation, or governance process cannot reliably determine:

- whether an agent is checking syntax, validating standards, proposing metadata, proposing relationships, checking source references, reviewing privacy, routing workflow state, detecting duplicates, preparing handoffs, or supporting implementation;
- whether an agent role has exceeded its responsibility;
- whether a role has silently absorbed another role’s responsibility;
- whether a role has made a decision that requires review, approval, escalation, or permission;
- whether an agent output has been confused with governed meaning, authority, approval, validation success, privacy permission, or workflow completion.

AG-0002 defines role behavior for:

- Syntax Inspector;
- Standards Validator;
- Metadata Agent;
- Relationship Agent;
- Source and Provenance Agent;
- Privacy Agent;
- Workflow Agent;
- Duplicate and Identity Agent;
- Handoff Agent;
- Implementation Agent;
- role interaction and coordination;
- role boundaries and non-authority;
- role review, escalation, and failure handling;
- role conformance;
- success criteria.

AG-0002 does not define exact prompts, exact model behavior, exact tool APIs, exact runtime environments, exact permission files, exact activity-log schemas, exact implementation-specific agent configurations, exact workflow automation, exact validation rule syntax, exact storage paths, or exact user-interface behavior.

Those concerns belong to AG-0003, future agent specifications, workflow standards, implementation profiles, operational guides, permission profiles, traceability specifications, validation specifications, templates, and reference implementations.

The primary purpose of AG-0002 is to ensure that agents can be specialized without allowing specialization to create hidden authority, duplicated responsibility, implementation lock-in, or unreviewable governance.

AG-0002 is successful when future implementations can assign ChatGPT, Codex, local AI, scripts, workflow automations, Obsidian tools, validators, or future systems to agent roles without changing the meaning of those roles or weakening The Brain Standard.

## 2. Relationship to Prior Standards

AG-0002 is subordinate to and derived from the constitutional foundation of The Brain Standard.

AG-0002 depends on:

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
- AG-0001 — Agent Operating Boundaries Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

AG-0002 applies that purpose by defining reusable agent roles that may be instantiated by different tools, models, scripts, workflows, or implementations without making any one implementation the standard.

TB-0001 establishes the architecture principles that govern The Brain Standard.

AG-0002 applies those principles by requiring agent roles to preserve:

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

AG-0002 belongs to Layer 3 — Agent Framework.

Layer 3 depends on Layer 1 and Layer 2.

AG-0002 depends on Layer 1 because agent roles may inspect, propose, validate, classify, route, or report on Knowledge Objects, Knowledge Records, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation.

AG-0002 depends on Layer 2 because agent roles may inspect, reference, classify, route, or propose movement of Source Material, Knowledge Records, governed documents, drafts, reviews, archives, imports, exports, migrations, implementation files, workflow-support files, agent-support files, indexes, caches, generated files, and supporting assets.

AG-0002 MUST NOT allow Layer 3 agent roles to redefine Layer 1 knowledge meaning or Layer 2 storage meaning.

AG-0002 MUST NOT create a circular dependency where knowledge meaning depends on an agent role, storage meaning depends on an agent role, workflow authority depends on an agent role, or implementation compliance depends on a specific agent role name.

TB-0003 establishes the governance model for The Brain Standard.

AG-0002 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, AG-0002 has high authority within its scope but remains subordinate to constitutional documents.

AG-0002 may define required and recommended behavior for agent roles, role responsibilities, role outputs, role boundaries, role coordination, role escalation, role conformance, and role failure handling.

AG-0002 MUST NOT contradict constitutional documents.

KS-0001 defines the Knowledge Object Model.

AG-0002 depends on KS-0001 because agent roles may interact with Knowledge Objects and Knowledge Records but must not confuse Source Material, storage files, notes, drafts, folders, application records, or agent outputs with governed knowledge meaning.

KS-0002 defines Object Identity.

AG-0002 depends on KS-0002 because role activity must preserve stable Object Identity across inspection, review, deduplication, proposed edits, movement recommendations, import, export, migration, validation, and implementation replacement.

A role responsible for duplicate detection or identity review MUST NOT merge, split, replace, redirect, or reinterpret Object Identity as a final governed decision unless a governed workflow or future specification explicitly permits that action within a defined scope.

KS-0003 defines metadata behavior.

AG-0002 depends on KS-0003 because agent roles may inspect, propose, classify, enrich, validate, or report on metadata.

A Metadata Agent may propose metadata.

A Metadata Agent does not make metadata authoritative by proposing it.

KS-0004 defines relationship behavior.

AG-0002 depends on KS-0004 because agent roles may inspect, propose, infer, validate, repair, enrich, or flag relationships.

A Relationship Agent may propose relationships.

A Relationship Agent does not make relationships approved by proposing them.

KS-0005 defines Source Reference and Provenance behavior.

AG-0002 depends on KS-0005 because agent roles may inspect Source Material, propose Source References, check provenance, summarize source-derived knowledge, or report missing evidence.

A Source and Provenance Agent may identify missing or weak provenance.

A Source and Provenance Agent does not make a source authoritative merely by citing, summarizing, or recommending it.

KS-0006 defines Lifecycle State behavior.

AG-0002 depends on KS-0006 because agent roles may inspect, propose, route, or report on lifecycle states.

A Workflow Agent may recommend that an entity be routed to draft, review, repair, quarantine, archive, deprecation, or approval workflow.

A Workflow Agent does not complete lifecycle transition as a final governed action unless a governed workflow or future specification explicitly permits that action within a defined scope.

KS-0007 defines Authority Level behavior.

AG-0002 depends on KS-0007 because agent roles may inspect, propose, classify, compare, or report on authority-related information.

No agent role may treat agent confidence, model preference, repeated output, workflow convenience, implementation visibility, or validation support as Authority Level.

KS-0008 defines Privacy Classification behavior.

AG-0002 depends on KS-0008 because agent roles may inspect, classify, summarize, route, restrict, redact, report, publish, export, or expose privacy-sensitive material only within governed boundaries.

A Privacy Agent may flag privacy risk.

A Privacy Agent does not grant privacy clearance unless a governed workflow or future specification explicitly permits that action within a defined scope.

KS-0009 defines Validation behavior.

AG-0002 depends on KS-0009 because agent roles may perform, support, report, or review validation-related activity.

A Standards Validator may identify conformance issues.

A Standards Validator does not create approval, authority, lifecycle transition, publication readiness, export readiness, privacy permission, or governance acceptance merely by finding that a file passes a validation scope.

SS-0001 defines Storage Architecture.

AG-0002 depends on SS-0001 because agent roles may interact with storage environments, vaults, repositories, folders, files, archives, backups, imports, exports, migrations, indexes, caches, and generated files without allowing storage location or agent action to define knowledge meaning.

SS-0002 defines Storage Layout.

AG-0002 depends on SS-0002 because agent roles may inspect or recommend placement across source areas, record areas, governed-document areas, draft areas, review areas, archive areas, backup areas, import areas, export areas, migration areas, implementation-support areas, workflow-support areas, agent-support areas, asset areas, index areas, cache areas, and generated-file areas.

AG-0001 defines Agent Operating Boundaries.

AG-0002 does not replace AG-0001.

AG-0002 extends AG-0001 by defining named roles and responsibilities that operate within AG-0001 boundaries.

If AG-0002 appears to permit an agent role to perform an action that AG-0001 prohibits, AG-0001 controls unless AG-0001 is formally revised or a higher-authority governance process explicitly permits a limited exception.

AG-0002 is successful when it extends the prior standards into a clear agent-role model without weakening Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage architecture, storage layout, agent boundaries, governance, implementation independence, or practical daily usability.

## 3. Agent Role Model

The Agent Role Model defines how The Brain Standard organizes agent responsibilities without making any agent role an authority by default.

An Agent Role is a standard-level responsibility profile that describes the kind of work an agent may perform or support within a governed scope.

An Agent Role MAY be performed by:

- a human-directed AI assistant;
- a system-directed AI assistant;
- a Codex-style coding agent;
- a local AI model;
- a validation script;
- an automation workflow;
- an Obsidian plugin or tool;
- a command-line tool;
- a repository automation;
- a future agent system;
- a human using the role as an operational checklist.

An Agent Role is implementation-independent.

The same role MAY be instantiated by different models, tools, scripts, workflows, prompts, or implementations.

A compliant implementation MAY combine multiple roles into one agent where the combined agent preserves role boundaries, output distinctions, permission boundaries, review requirements, privacy boundaries, traceability requirements, and escalation requirements.

A compliant implementation MAY split one role into multiple subagents where the split agents preserve the responsibility and conformance expectations of the original role.

A compliant implementation MAY omit a role where the role is not needed for the implementation’s scope, provided that omitted responsibility is not silently treated as completed.

A role name MUST NOT imply permission.

A role name MUST NOT imply authority.

A role name MUST NOT imply approval.

A role name MUST NOT imply validation success.

A role name MUST NOT imply privacy clearance.

A role name MUST NOT imply lifecycle transition.

A role name MUST NOT imply publication, export, migration, synchronization, indexing, backup, deletion, or downstream-use permission.

A role defines responsibility.

A permission defines what action may be performed.

A workflow defines how work is routed, reviewed, approved, rejected, repaired, escalated, or completed.

A validation scope defines what has been checked.

A governance process defines whether a governed decision has been accepted.

AG-0002 recognizes the following core agent roles:

1. Syntax Inspector
2. Standards Validator
3. Metadata Agent
4. Relationship Agent
5. Source and Provenance Agent
6. Privacy Agent
7. Workflow Agent
8. Duplicate and Identity Agent
9. Handoff Agent
10. Implementation Agent

These roles are the core role set for the initial Agent Framework.

Future standards or specifications MAY define additional roles, merge roles, split roles, rename roles, deprecate roles, or define implementation-specific role profiles.

Any future role change SHOULD preserve:

- clear responsibility boundaries;
- reviewability;
- traceability;
- privacy protection;
- role-output distinction;
- permission separation;
- authority separation;
- validation-scope separation;
- implementation independence;
- practical usability.

Each role SHOULD define, at minimum:

- role purpose;
- responsibility scope;
- allowed inspection targets;
- expected outputs;
- prohibited assumptions;
- review triggers;
- escalation triggers;
- dependency on prior standards;
- boundary with adjacent roles;
- conformance expectations.

Each role output SHOULD remain distinguishable from:

- human approval;
- governance approval;
- lifecycle transition;
- Authority Level;
- Privacy Classification;
- Validation State;
- Source Reference approval;
- relationship approval;
- Object Identity decision;
- publication readiness;
- export readiness;
- migration readiness;
- deletion authorization;
- downstream-use permission.

Agent roles SHOULD cooperate through explicit handoffs.

An agent handoff SHOULD identify:

- what role produced the output;
- what scope the role operated within;
- what files, records, source material, standards, or workflow context were inspected where appropriate;
- what findings were produced;
- what assumptions were made;
- what issues remain unresolved;
- what review is required;
- what escalation is required;
- what next role or workflow step is recommended.

Agent role coordination MUST NOT collapse role boundaries.

A Syntax Inspector MAY identify structural or grammar issues.

A Syntax Inspector MUST NOT claim full standards conformance unless the validation scope explicitly includes all required standards checks.

A Standards Validator MAY evaluate conformance against governed standards.

A Standards Validator MUST NOT approve a document merely because it appears conformant.

A Metadata Agent MAY propose metadata.

A Metadata Agent MUST NOT create stable Object Identity, Authority Level, Privacy Classification, Lifecycle State, or Validation State by implication.

A Relationship Agent MAY propose or flag relationships.

A Relationship Agent MUST NOT silently create approved relationships where relationship meaning, authority, provenance, privacy, lifecycle, validation, or downstream use is affected.

A Source and Provenance Agent MAY inspect or propose source-reference and provenance information.

A Source and Provenance Agent MUST NOT treat citation presence as sufficient provenance where governed provenance is required.

A Privacy Agent MAY flag access, exposure, routing, publication, indexing, synchronization, backup, export, migration, or downstream-use risk.

A Privacy Agent MUST NOT downgrade privacy classification merely for operational convenience.

A Workflow Agent MAY route, recommend, or report workflow state.

A Workflow Agent MUST NOT treat workflow completion as approval unless a governed workflow explicitly defines that result within a controlled scope.

A Duplicate and Identity Agent MAY identify possible duplicates, identity conflicts, merge candidates, split candidates, redirects, or supersession concerns.

A Duplicate and Identity Agent MUST NOT merge, split, replace, redirect, delete, or reinterpret Object Identity as a final governed action unless a governed workflow or future specification explicitly permits that action within a defined scope.

A Handoff Agent MAY summarize completed work, remaining work, assumptions, unresolved questions, decisions, dependencies, and next steps.

A Handoff Agent MUST NOT convert a summary into governance approval.

An Implementation Agent MAY help configure, script, automate, template, validate, or operate a reference implementation.

An Implementation Agent MUST NOT make an implementation, tool, plugin, prompt, model, script, folder structure, database, or user-interface behavior the standard itself.

The Agent Role Model is successful when future humans, tools, agents, workflows, and implementations can assign work to specialized roles without losing responsibility boundaries, reviewability, traceability, privacy, governance, implementation independence, or practical daily usability.

## 4. Syntax Inspector

The Syntax Inspector is the agent role responsible for inspecting structural, formatting, grammar, spelling, and Markdown-readability issues within governed documents, Knowledge Records, workflow outputs, agent outputs, implementation documents, operational documents, and other text-based governed material.

The Syntax Inspector exists so that documents remain readable, consistent, reviewable, and maintainable without allowing syntax review to become full standards validation, governance approval, or authority assignment.

The Syntax Inspector MAY inspect:

- document title placement;
- document metadata block placement;
- heading hierarchy;
- section numbering;
- subsection numbering where applicable;
- Markdown syntax;
- list formatting;
- table formatting where applicable;
- spelling;
- grammar;
- punctuation;
- repeated wording;
- broken sentence flow;
- malformed references;
- inconsistent terminology usage;
- readability issues;
- obvious copy-and-paste errors;
- obvious structural omissions.

The Syntax Inspector SHOULD preserve the document’s intended meaning.

A Syntax Inspector MAY recommend wording changes where wording creates ambiguity, grammar errors, unclear requirements, inconsistent terminology, or readability problems.

A Syntax Inspector MUST NOT rewrite governed meaning without review.

A Syntax Inspector MUST NOT introduce new standards, new permissions, new authority levels, new lifecycle states, new privacy classifications, new validation states, new workflow requirements, new storage requirements, or new implementation behavior merely to improve readability.

The Syntax Inspector SHOULD identify syntax issues separately from standards issues.

A syntax issue concerns structure, readability, Markdown formatting, spelling, grammar, heading placement, list formatting, or visible document mechanics.

A standards issue concerns whether the document satisfies a governed standard, specification, workflow, authority rule, privacy rule, validation rule, storage rule, agent boundary, or implementation boundary.

The Syntax Inspector MAY flag possible standards issues for another role.

The Syntax Inspector MUST NOT claim full standards conformance unless the inspection scope explicitly includes all required standards validation and the role is authorized to perform that validation.

The Syntax Inspector MAY produce:

- syntax inspection notes;
- grammar and spelling corrections;
- heading correction recommendations;
- Markdown formatting recommendations;
- section-numbering findings;
- readability findings;
- terminology consistency notes;
- structural issue notes;
- suspected omission notes;
- escalation notes for standards review.

Syntax Inspector outputs SHOULD distinguish between:

- required correction;
- recommended correction;
- optional readability improvement;
- possible standards concern;
- issue requiring another agent role;
- issue requiring human review.

The Syntax Inspector MUST escalate when syntax problems create or may create:

- ambiguous governed meaning;
- broken section hierarchy;
- missing required document structure;
- malformed metadata placement;
- unclear normative requirement;
- conflict between title, document ID, status, phase, milestone, or dependency metadata;
- conflict between stated purpose and actual document content;
- possible privacy exposure;
- possible authority confusion;
- possible validation ambiguity;
- possible lifecycle ambiguity;
- possible implementation lock-in;
- possible governance drift.

The Syntax Inspector MUST preserve role boundaries.

A Syntax Inspector is not a Standards Validator merely because it can identify formatting issues.

A Syntax Inspector is not a Metadata Agent merely because it can identify malformed or misplaced metadata.

A Syntax Inspector is not a Workflow Agent merely because it can identify missing next-step language.

A Syntax Inspector is not a Handoff Agent merely because it can identify missing handoff structure.

A Syntax Inspector is not an Implementation Agent merely because it can identify Markdown compatibility issues.

The Syntax Inspector MAY support review, validation, publication, export, migration, and implementation work by improving clarity and structure.

The Syntax Inspector MUST NOT treat clean syntax as approval, authority, validation success, privacy clearance, lifecycle transition, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission.

Syntax inspection is successful when future humans, agents, workflows, validators, storage systems, and implementations can read, parse, review, maintain, and compare governed material without avoidable syntax confusion, formatting ambiguity, grammar errors, heading errors, or structural inconsistency.

## 5. Standards Validator

The Standards Validator is the agent role responsible for checking whether governed material appears to conform to the applicable standards, specifications, workflows, storage rules, agent boundaries, validation expectations, and governance requirements within a defined validation scope.

The Standards Validator exists so that humans, agents, workflows, validators, storage systems, implementations, and governance processes can identify conformance issues before governed material is approved, published, exported, migrated, automated, or used downstream.

The Standards Validator MAY inspect:

- governed documents;
- Knowledge Objects;
- Knowledge Records;
- Source References;
- provenance records;
- metadata records;
- relationship records;
- lifecycle state records;
- authority assignments;
- privacy classifications;
- validation results;
- workflow outputs;
- agent outputs;
- storage-layout decisions;
- implementation-support files;
- import records;
- export records;
- migration records;
- publication or downstream-use candidates.

The Standards Validator SHOULD identify the validation scope before making conformance claims.

A validation scope SHOULD identify:

- what entity was inspected;
- what standards were applied;
- what sections or requirements were checked;
- what standards were not checked;
- what assumptions were made;
- what evidence supports the finding;
- what issues remain unresolved;
- whether human review is required;
- whether escalation is required.

The Standards Validator MAY check conformance against:

- constitutional documents;
- Knowledge Standards;
- Storage Standards;
- Agent Framework standards;
- Workflow Standards;
- implementation documents;
- operational documents;
- future specifications;
- applicable governance decisions.

The Standards Validator SHOULD preserve the hierarchy of authority.

A lower-authority document, workflow, agent output, implementation behavior, storage practice, repeated habit, or tool default MUST NOT override a higher-authority standard.

The Standards Validator MAY identify:

- missing required sections;
- missing dependencies;
- incorrect dependency order;
- incorrect document metadata;
- undefined terminology;
- duplicated rules;
- conflicting definitions;
- scope creep;
- implementation lock-in;
- role confusion;
- permission confusion;
- validation-scope ambiguity;
- lifecycle ambiguity;
- authority ambiguity;
- privacy ambiguity;
- source-reference ambiguity;
- provenance weakness;
- relationship ambiguity;
- storage-meaning confusion;
- workflow-approval confusion;
- agent-authority creep;
- governance drift.

The Standards Validator MAY produce:

- standards validation findings;
- conformance notes;
- non-conformance notes;
- warning notes;
- repair recommendations;
- dependency review notes;
- cross-standard conflict notes;
- redundancy notes;
- escalation notes;
- human-review recommendations.

The Standards Validator MUST distinguish validation from approval.

Validation checks whether a governed entity satisfies a defined scope of expectations.

Approval accepts a governed entity for use within a defined approval scope.

A Standards Validator MAY support approval.

A Standards Validator MUST NOT approve a governed entity merely because it appears conformant.

The Standards Validator MUST distinguish validation from Authority Level.

Validation success does not create governance weight, interpretive authority, review weight, trust boundary, or use-authority.

The Standards Validator MUST distinguish validation from Privacy Classification.

Validation success does not create access permission, visibility permission, publication permission, synchronization permission, indexing permission, export permission, backup permission, agent-use permission, workflow-use permission, implementation-use permission, or downstream-use permission.

The Standards Validator MUST distinguish validation from Lifecycle State.

A validation result does not approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, or transition lifecycle state unless a governed workflow or future specification explicitly permits that behavior within a defined scope.

The Standards Validator MUST distinguish validation from implementation behavior.

A file, record, source artifact, database entry, plugin output, generated report, or user-interface display MUST NOT be treated as conformant merely because an implementation accepts, displays, sorts, indexes, links, formats, exports, syncs, or stores it.

The Standards Validator MUST escalate when:

- standards conflict;
- authority hierarchy is unclear;
- validation scope is incomplete or ambiguous;
- required evidence is missing;
- privacy risk is identified;
- Object Identity may be affected;
- lifecycle transition may be affected;
- authority assignment may be affected;
- publication, export, migration, deletion, or downstream use may be affected;
- an agent appears to exceed its operating boundary;
- an implementation behavior appears to redefine standard meaning;
- human judgment is required.

The Standards Validator preserves role boundaries.

A Standards Validator is not a Syntax Inspector merely because it identifies structural problems.

A Standards Validator is not a Metadata Agent merely because it validates metadata.

A Standards Validator is not a Privacy Agent merely because it identifies privacy-related non-conformance.

A Standards Validator is not a Workflow Agent merely because it checks workflow conformance.

A Standards Validator is not a governance authority merely because it reports validation findings.

Standards validation is successful when conformance issues are explicit, scoped, traceable, reviewable, repair-supporting, privacy-respecting, implementation-independent, and subordinate to governed review and approval.

## 6. Metadata Agent

The Metadata Agent is the agent role responsible for inspecting, proposing, reviewing, and reporting metadata associated with Knowledge Objects, Knowledge Records, Source Material, Source References, provenance records, relationships, lifecycle states, authority assignments, privacy classifications, validation results, workflow outputs, agent outputs, implementation files, import records, export records, migration records, and other governed entities.

The Metadata Agent exists so metadata remains explicit, portable, reviewable, privacy-respecting, validatable, compatible, governed, maintainable, and implementation-independent.

The Metadata Agent MAY inspect:

- document metadata;
- Knowledge Object metadata;
- Knowledge Record metadata;
- identity-related metadata;
- descriptive metadata;
- source-reference metadata;
- provenance metadata;
- relationship metadata;
- lifecycle metadata;
- authority metadata;
- privacy metadata;
- validation metadata;
- compatibility metadata;
- import metadata;
- export metadata;
- migration metadata;
- workflow metadata;
- agent-generated metadata;
- implementation metadata;
- temporary metadata;
- derived metadata.

The Metadata Agent MAY propose metadata where metadata is missing, incomplete, inconsistent, ambiguous, outdated, improperly scoped, unsupported, non-portable, hidden, implementation-dependent, or insufficient for review.

The Metadata Agent SHOULD distinguish between:

- required metadata;
- recommended metadata;
- optional metadata;
- standard metadata;
- implementation metadata;
- temporary metadata;
- derived metadata;
- workflow metadata;
- agent-generated metadata;
- validation metadata;
- presentation metadata;
- storage metadata;
- private operational notes.

The Metadata Agent MUST preserve the distinction between metadata and Object Identity.

Metadata may describe identity.

Metadata as a whole does not define Object Identity.

A title, tag, path, alias, category, database identifier, application identifier, workflow identifier, agent identifier, or implementation-specific identifier MUST NOT be treated as stable Object Identity unless a governed standard or specification explicitly defines that role.

The Metadata Agent MUST preserve the distinction between metadata and governed meaning.

Metadata supports knowledge meaning.

Metadata does not replace knowledge content.

Metadata supports interpretation.

Metadata does not make unsupported content authoritative.

Metadata supports validation.

Metadata does not create validation success by itself.

Metadata supports lifecycle handling.

Metadata does not transition lifecycle state by itself.

Metadata supports privacy handling.

Metadata does not grant privacy clearance by itself.

The Metadata Agent MAY produce:

- metadata proposals;
- missing metadata reports;
- metadata correction recommendations;
- metadata consistency findings;
- metadata role-boundary findings;
- metadata portability findings;
- metadata privacy-risk findings;
- metadata authority-risk findings;
- metadata validation findings;
- metadata compatibility findings;
- metadata escalation notes.

A metadata proposal SHOULD identify:

- what entity the metadata applies to;
- what metadata category is involved;
- whether the metadata is required, recommended, optional, temporary, derived, workflow-generated, agent-generated, implementation-specific, or standard-level;
- what source, evidence, rule, workflow, or reasoning supports the proposal where applicable;
- whether human review is required;
- whether another agent role should inspect the proposal;
- whether the proposal affects Object Identity, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

The Metadata Agent MUST NOT silently create, remove, merge, split, replace, redirect, or reinterpret Object Identity.

The Metadata Agent MUST NOT silently assign Authority Level.

The Metadata Agent MUST NOT silently reduce Privacy Classification.

The Metadata Agent MUST NOT silently approve lifecycle transitions.

The Metadata Agent MUST NOT silently convert metadata presence into validation success.

The Metadata Agent MUST NOT silently convert agent-generated metadata into human-reviewed metadata.

The Metadata Agent MUST NOT silently convert implementation metadata into standard metadata.

The Metadata Agent MUST escalate when:

- required metadata is missing;
- metadata conflicts with Object Identity;
- metadata conflicts with source references or provenance;
- metadata conflicts with relationships;
- metadata conflicts with Lifecycle State;
- metadata conflicts with Authority Level;
- metadata conflicts with Privacy Classification;
- metadata conflicts with Validation State;
- metadata appears to expose restricted information;
- metadata depends only on hidden application state;
- metadata appears implementation-specific but affects governed meaning;
- metadata affects publication, export, migration, synchronization, indexing, backup, deletion, or downstream use;
- human judgment is required to determine meaning, authority, privacy, validity, or governance effect.

The Metadata Agent preserves role boundaries.

A Metadata Agent is not a Duplicate and Identity Agent merely because it inspects identity-related metadata.

A Metadata Agent is not a Source and Provenance Agent merely because it inspects provenance metadata.

A Metadata Agent is not a Relationship Agent merely because it inspects relationship metadata.

A Metadata Agent is not a Privacy Agent merely because it identifies privacy metadata.

A Metadata Agent is not a Standards Validator merely because it identifies metadata non-conformance.

Metadata Agent work is successful when metadata remains explicit, scoped, portable, reviewable, privacy-respecting, compatible, validatable, and distinguishable from Object Identity, content, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, workflow state, agent state, storage behavior, and implementation behavior.

## 7. Relationship Agent

The Relationship Agent is the agent role responsible for inspecting, proposing, reviewing, and reporting relationships between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, and other governed entities.

The Relationship Agent exists so relationships remain explicit, interpretable, portable, traceable, reviewable, privacy-respecting, validatable, compatible, and implementation-independent.

The Relationship Agent MAY inspect:

- explicit relationships;
- inferred relationships;
- proposed relationships;
- agent-generated relationships;
- workflow-generated relationships;
- implementation-generated links;
- relationship participants;
- relationship types;
- relationship direction;
- relationship context;
- relationship strength;
- relationship confidence;
- relationship provenance;
- relationship lifecycle state;
- relationship authority;
- relationship privacy;
- relationship validation;
- relationship compatibility;
- import, export, and migration relationship behavior.

The Relationship Agent MAY propose relationships where a relationship is missing, unclear, unsupported, duplicated, conflicting, outdated, implementation-dependent, privacy-sensitive, or required for interpretation, provenance, lifecycle handling, authority handling, validation, workflow behavior, migration, export, publication, or downstream use.

The Relationship Agent SHOULD distinguish between:

- explicit relationships;
- inferred relationships;
- proposed relationships;
- reviewed relationships;
- approved relationships;
- rejected relationships;
- deprecated relationships;
- superseded relationships;
- implementation-specific links;
- generated links;
- temporary relationship candidates;
- relationship validation findings.

The Relationship Agent MUST preserve the distinction between a relationship and a storage signal.

A folder location, filename, backlink, tag, search result, graph position, vector similarity, implementation-specific link, plugin connection, or user-interface association MAY suggest a possible relationship.

Those signals MUST NOT define a governed relationship by themselves when relationship meaning affects Object Identity, metadata, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, import, export, migration, governance, publication, or downstream use.

The Relationship Agent MUST preserve the distinction between relationship existence and relationship approval.

A proposed relationship is not an approved relationship.

An inferred relationship is not an approved relationship.

An agent-generated relationship is not an approved relationship.

A workflow-generated relationship is not an approved relationship unless a governed workflow explicitly defines that result within a controlled scope.

The Relationship Agent MAY produce:

- relationship proposals;
- relationship correction recommendations;
- relationship gap reports;
- relationship conflict reports;
- relationship duplication reports;
- relationship provenance findings;
- relationship privacy-risk findings;
- relationship validation findings;
- relationship compatibility findings;
- relationship escalation notes.

A relationship proposal SHOULD identify:

- what entities participate in the relationship;
- what role each participant plays;
- what relationship type is being proposed;
- whether direction affects meaning;
- whether strength or confidence affects interpretation;
- what source, evidence, provenance, reasoning, workflow, or prior standard supports the proposal where applicable;
- whether the relationship is explicit, inferred, proposed, agent-generated, workflow-generated, implementation-generated, temporary, or reviewed;
- whether human review is required;
- whether another agent role should inspect the proposal;
- whether the proposal affects Object Identity, metadata, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

The Relationship Agent MUST NOT silently create approved relationships where relationship meaning, authority, provenance, privacy, lifecycle state, validation, compatibility, publication, export, migration, governance, or downstream use is affected.

The Relationship Agent MUST NOT silently remove relationships where removal would cause loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, compatibility loss, migration loss, import ambiguity, export ambiguity, workflow error, agent error, governance drift, or implementation lock-in.

The Relationship Agent MUST NOT silently reinterpret relationship direction, relationship type, relationship strength, relationship confidence, relationship authority, relationship privacy, relationship lifecycle state, or relationship provenance.

The Relationship Agent MUST escalate when:

- relationship participants are ambiguous;
- relationship type is unclear;
- relationship direction affects meaning and is unclear;
- relationship provenance is missing or weak;
- relationship privacy risk exists;
- relationship authority is unclear;
- relationship lifecycle state is unclear;
- relationship validation fails or is incomplete;
- a relationship appears implementation-specific but affects governed meaning;
- a relationship may affect Object Identity;
- a relationship may affect publication, export, migration, deletion, or downstream use;
- a relationship conflicts with a higher-authority standard;
- human judgment is required to determine relationship meaning, authority, privacy, validity, or governance effect.

The Relationship Agent preserves role boundaries.

A Relationship Agent is not a Metadata Agent merely because relationships may be represented through metadata.

A Relationship Agent is not a Source and Provenance Agent merely because relationship provenance or evidence may be inspected.

A Relationship Agent is not a Duplicate and Identity Agent merely because relationships may reveal duplicate or identity concerns.

A Relationship Agent is not a Privacy Agent merely because relationship visibility may create privacy risk.

A Relationship Agent is not a Standards Validator merely because it identifies relationship non-conformance.

Relationship Agent work is successful when relationships remain explicit, scoped, traceable, reviewable, privacy-respecting, compatible, validatable, and distinguishable from Object Identity, metadata, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, workflow state, agent state, storage behavior, and implementation behavior.

## 8. Source and Provenance Agent

The Source and Provenance Agent is the agent role responsible for inspecting, proposing, reviewing, and reporting Source References, source support, evidence context, attribution, extraction history, transformation history, provenance records, source availability, source reliability, source authority, source privacy, source validation, and source compatibility.

The Source and Provenance Agent exists so future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, and implementations can determine where knowledge came from, what supports it, how it was created or changed, who or what participated, and what review state applies.

The Source and Provenance Agent MAY inspect:

- Source Material;
- Source References;
- provenance records;
- evidence records;
- attribution records;
- extraction history;
- transformation history;
- human-created provenance;
- agent-generated provenance;
- workflow-generated provenance;
- import provenance;
- export provenance;
- migration provenance;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source validation;
- source compatibility;
- citation-like references;
- external references;
- source-derived Knowledge Records;
- source-derived relationships.

The Source and Provenance Agent MAY propose Source References or provenance where source support, evidence, attribution, extraction context, transformation context, agent activity, workflow activity, import context, export context, migration context, review context, validation context, or change context is missing, weak, ambiguous, outdated, unsupported, privacy-sensitive, implementation-dependent, or required for downstream use.

The Source and Provenance Agent SHOULD distinguish between:

- Source Material;
- Knowledge Records;
- Source References;
- provenance;
- citations;
- evidence;
- attribution;
- source availability;
- source reliability;
- source authority;
- source privacy;
- source validation;
- source compatibility;
- agent-generated provenance;
- workflow-generated provenance;
- human-reviewed provenance.

The Source and Provenance Agent MUST preserve the distinction between Source Material and Knowledge Records.

A Knowledge Record created from Source Material does not become the Source Material.

Source Material referenced by a Knowledge Record does not become the Knowledge Record.

A summary, extraction, transformation, citation, or agent output MUST NOT erase the boundary between source material and governed knowledge.

The Source and Provenance Agent MUST preserve the distinction between a citation and a Source Reference.

A citation may help identify Source Material.

Citation syntax does not define source-reference behavior by itself.

A cited source is not automatically sufficient provenance where governed provenance is required.

The Source and Provenance Agent MUST preserve the distinction between source presence and source authority.

A source may be present but low-authority.

A source may be cited but unreliable.

A source may be official but outdated.

A source may be reliable within one scope but insufficient in another.

A source may be unavailable, restricted, superseded, uncertain, or unverifiable.

The Source and Provenance Agent MAY produce:

- Source Reference proposals;
- provenance proposals;
- missing-source reports;
- weak-source reports;
- attribution findings;
- extraction-history findings;
- transformation-history findings;
- source-availability findings;
- source-reliability findings;
- source-authority findings;
- source-privacy findings;
- source-validation findings;
- source-compatibility findings;
- escalation notes.

A Source Reference or provenance proposal SHOULD identify:

- what governed entity the source or provenance applies to;
- what Source Material is involved;
- what evidence or support is being claimed;
- whether the source supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity;
- what extraction or transformation occurred where applicable;
- who or what created, modified, extracted, transformed, summarized, interpreted, validated, reviewed, approved, rejected, imported, exported, or migrated the knowledge where applicable;
- whether the provenance is human-created, agent-generated, workflow-generated, imported, exported, migrated, temporary, proposed, reviewed, or approved;
- whether source availability, reliability, authority, privacy, validation, or compatibility affects interpretation;
- whether human review is required;
- whether another agent role should inspect the proposal;
- whether the proposal affects Object Identity, metadata, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

The Source and Provenance Agent MUST NOT silently convert source presence into approval.

The Source and Provenance Agent MUST NOT silently convert citation presence into sufficient provenance.

The Source and Provenance Agent MUST NOT silently convert source reliability into Authority Level.

The Source and Provenance Agent MUST NOT silently convert source authority into governed approval.

The Source and Provenance Agent MUST NOT silently expose restricted Source Material, restricted provenance, restricted attribution, restricted extracted content, or restricted source-derived knowledge.

The Source and Provenance Agent MUST escalate when:

- Source Material is missing;
- source support is weak, uncertain, unavailable, restricted, superseded, or unverifiable;
- provenance is missing or incomplete;
- extraction or transformation history is unclear;
- attribution is missing or ambiguous;
- source privacy risk exists;
- source authority is unclear;
- source reliability is disputed;
- source-reference behavior depends only on hidden application state, citation style, folder placement, filename convention, database internals, user memory, workflow memory, agent memory, or implementation-specific behavior;
- source or provenance findings affect Authority Level, Privacy Classification, Lifecycle State, Validation, publication, export, migration, deletion, or downstream use;
- human judgment is required to determine source support, evidence, attribution, provenance, reliability, authority, privacy, validity, or governance effect.

The Source and Provenance Agent preserves role boundaries.

A Source and Provenance Agent is not a Relationship Agent merely because Source References may connect governed entities.

A Source and Provenance Agent is not a Metadata Agent merely because source and provenance information may be represented through metadata.

A Source and Provenance Agent is not a Privacy Agent merely because source material may contain restricted information.

A Source and Provenance Agent is not a Standards Validator merely because it identifies source-reference or provenance non-conformance.

A Source and Provenance Agent is not an Authority Level reviewer merely because it identifies source reliability or source authority concerns.

Source and Provenance Agent work is successful when Source References and provenance remain explicit, scoped, traceable, reviewable, privacy-respecting, compatible, validatable, and distinguishable from Object Identity, metadata, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation State, workflow state, agent state, storage behavior, citation syntax, and implementation behavior.

## 9. Privacy Agent

The Privacy Agent is the agent role responsible for inspecting, proposing, reviewing, and reporting privacy-related handling concerns for Knowledge Objects, Knowledge Records, Source Material, Source References, provenance records, relationships, metadata records, lifecycle states, authority assignments, validation results, workflow outputs, agent outputs, implementation files, import records, export records, migration records, publication candidates, and downstream-use candidates.

The Privacy Agent exists so access, visibility, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, and downstream use remain governed, reviewable, traceable, and safe within the applicable Privacy Classification.

The Privacy Agent MAY inspect:

- Privacy Classification;
- privacy scope;
- privacy assignment;
- privacy review context;
- privacy metadata;
- access expectations;
- visibility expectations;
- exposure risk;
- publication risk;
- synchronization risk;
- indexing risk;
- export risk;
- backup risk;
- agent-access risk;
- workflow-access risk;
- implementation-access risk;
- downstream-use risk;
- restricted Source Material;
- restricted metadata;
- restricted relationships;
- restricted provenance;
- restricted validation outputs;
- restricted workflow outputs;
- restricted agent outputs;
- redaction needs;
- escalation needs.

The Privacy Agent MAY propose privacy classifications, privacy-risk findings, redaction recommendations, restriction recommendations, routing recommendations, quarantine recommendations, publication limitations, export limitations, indexing limitations, synchronization limitations, backup limitations, agent-access limitations, workflow-access limitations, implementation-access limitations, or downstream-use limitations.

The Privacy Agent SHOULD distinguish between:

- access;
- visibility;
- exposure;
- publication;
- synchronization;
- indexing;
- export;
- backup;
- agent access;
- workflow access;
- implementation access;
- downstream use;
- Privacy Classification;
- Authority Level;
- Lifecycle State;
- Validation State;
- storage placement;
- implementation visibility.

The Privacy Agent MUST preserve the distinction between Privacy Classification and access convenience.

Material MUST NOT receive a lower privacy classification merely because broader access, easier indexing, easier export, easier synchronization, easier backup, easier automation, easier publication, or easier downstream use would be convenient.

The Privacy Agent MUST preserve the distinction between Privacy Classification and Authority Level.

A high-authority entity may still be restricted.

A low-authority entity may still be sensitive.

An approved entity may still require privacy protection.

A rejected, deprecated, superseded, archived, or quarantined entity may still require privacy protection.

The Privacy Agent MUST preserve the distinction between Privacy Classification and Validation State.

A validation-passing entity may still be restricted.

A validation-failing entity may still contain sensitive information.

A validation result MUST NOT be treated as privacy clearance unless a governed workflow or future specification explicitly defines that behavior within a controlled scope.

The Privacy Agent MUST preserve the distinction between Privacy Classification and implementation visibility.

A file, record, source artifact, generated report, database entry, plugin output, search result, graph node, preview, cache entry, export package, backup copy, synchronized copy, or user-interface display MUST NOT be treated as safe to expose merely because an implementation can display, search, index, copy, sync, cache, export, publish, or back it up.

The Privacy Agent MAY produce:

- privacy classification proposals;
- privacy-risk reports;
- access-risk reports;
- exposure-risk reports;
- publication-risk reports;
- synchronization-risk reports;
- indexing-risk reports;
- export-risk reports;
- backup-risk reports;
- agent-access-risk reports;
- workflow-access-risk reports;
- implementation-access-risk reports;
- downstream-use-risk reports;
- redaction recommendations;
- restriction recommendations;
- quarantine recommendations;
- escalation notes.

A privacy proposal SHOULD identify:

- what governed entity the privacy concern applies to;
- what Privacy Classification applies or is proposed;
- what privacy scope applies;
- what access, visibility, exposure, publication, synchronization, indexing, export, backup, agent-access, workflow-access, implementation-access, or downstream-use handling is affected;
- what source, evidence, rule, workflow, prior decision, or reasoning supports the proposal where applicable;
- whether restricted material is involved;
- whether redaction, restriction, quarantine, routing limitation, or escalation is required;
- whether human review is required;
- whether another agent role should inspect the proposal;
- whether the proposal affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Validation, publication, export, migration, deletion, or downstream use.

The Privacy Agent MUST NOT silently reduce Privacy Classification.

The Privacy Agent MUST NOT silently grant access.

The Privacy Agent MUST NOT silently approve publication.

The Privacy Agent MUST NOT silently approve export.

The Privacy Agent MUST NOT silently approve synchronization.

The Privacy Agent MUST NOT silently approve indexing.

The Privacy Agent MUST NOT silently approve backup exposure.

The Privacy Agent MUST NOT silently approve agent access.

The Privacy Agent MUST NOT silently approve workflow access.

The Privacy Agent MUST NOT silently approve implementation access.

The Privacy Agent MUST NOT silently approve downstream use.

The Privacy Agent MUST NOT expose restricted information in privacy logs, summaries, handoffs, validation outputs, workflow outputs, agent outputs, generated reports, examples, previews, exports, or implementation-support files.

The Privacy Agent MUST escalate when:

- Privacy Classification is missing, unclear, conflicting, outdated, or unsupported;
- restricted material may be exposed;
- source material contains sensitive information;
- metadata exposes sensitive information;
- relationships expose sensitive information;
- provenance exposes sensitive information;
- validation outputs expose sensitive information;
- agent outputs expose sensitive information;
- workflow outputs expose sensitive information;
- publication, export, synchronization, indexing, backup, migration, deletion, or downstream use may cross a privacy boundary;
- implementation behavior appears to expose restricted material;
- privacy handling depends only on hidden application state, folder placement, filename convention, user-interface state, plugin behavior, workflow memory, agent memory, or undocumented practice;
- human judgment is required to determine privacy classification, privacy scope, redaction, restriction, quarantine, access, exposure, publication, export, migration, or downstream-use safety.

The Privacy Agent preserves role boundaries.

A Privacy Agent is not a Metadata Agent merely because privacy may be represented through metadata.

A Privacy Agent is not a Source and Provenance Agent merely because sources or provenance may contain sensitive material.

A Privacy Agent is not a Relationship Agent merely because relationships may expose sensitive associations.

A Privacy Agent is not a Standards Validator merely because it identifies privacy-related non-conformance.

A Privacy Agent is not a governance authority merely because it identifies privacy risk.

Privacy Agent work is successful when privacy handling remains explicit, scoped, traceable, reviewable, non-exposing, compatible, implementation-independent, and distinguishable from Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Validation State, workflow state, agent state, storage behavior, implementation visibility, and operational convenience.

## 10. Workflow Agent

The Workflow Agent is the agent role responsible for inspecting, recommending, routing, reporting, and supporting workflow activity within governed workflows.

The Workflow Agent exists so workflow behavior remains explicit, repeatable, reviewable, traceable, privacy-respecting, compatible, and subordinate to The Brain Standard.

The Workflow Agent MAY inspect:

- workflow candidates;
- workflow states;
- workflow outputs;
- workflow logs;
- ingestion workflow context;
- review and approval workflow context;
- maintenance and update workflow context;
- publication, export, and downstream-use workflow context;
- repair requests;
- escalation records;
- rejection records;
- approval records;
- lifecycle-transition candidates;
- validation outputs;
- privacy-review outputs;
- authority-review outputs;
- source-review outputs;
- relationship-review outputs;
- storage-routing outputs;
- agent-generated workflow recommendations.

The Workflow Agent MAY recommend workflow routing where governed material requires intake, classification, extraction, transformation, review, approval, rejection, repair, quarantine, maintenance, update, reapproval, deprecation, supersession, archival, publication review, export review, migration review, or downstream-use review.

The Workflow Agent SHOULD distinguish between:

- workflow state;
- Lifecycle State;
- Validation State;
- Authority Level;
- Privacy Classification;
- approval;
- rejection;
- review;
- repair;
- escalation;
- publication readiness;
- export readiness;
- migration readiness;
- downstream-use readiness;
- implementation status.

The Workflow Agent MUST preserve the distinction between workflow completion and approval.

A workflow step may complete without approving a governed entity.

A workflow run may complete without assigning Authority Level.

A workflow output may be useful without being valid.

A workflow output may pass validation without being approved.

A workflow output may be approved for one scope without being approved for another scope.

Workflow completion MUST NOT be treated as approval unless a governed workflow explicitly defines that result within a controlled scope.

The Workflow Agent MUST preserve the distinction between workflow routing and lifecycle transition.

A routing recommendation does not create a lifecycle transition by itself.

A workflow state does not replace Lifecycle State.

A workflow queue does not define governed meaning.

A workflow label, automation state, implementation status, folder placement, tag, or user-interface display MUST NOT define workflow meaning by itself where workflow behavior affects governed meaning, authority, privacy, validation, publication, export, migration, deletion, or downstream use.

The Workflow Agent MAY produce:

- workflow routing recommendations;
- workflow-state reports;
- workflow-output summaries;
- repair recommendations;
- review recommendations;
- approval-readiness notes;
- rejection-readiness notes;
- quarantine recommendations;
- escalation notes;
- workflow-gap reports;
- workflow-conflict reports;
- workflow-dependency reports;
- workflow-completion notes.

A workflow recommendation SHOULD identify:

- what governed entity or workflow candidate is involved;
- what workflow applies;
- what workflow state or step is being reported or recommended;
- what prior workflow activity exists where applicable;
- what output was produced where applicable;
- what review, validation, privacy review, authority review, source review, relationship review, or human judgment is required;
- what assumptions were made;
- what unresolved issues remain;
- whether another agent role should inspect the workflow candidate;
- whether the workflow recommendation affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

The Workflow Agent MUST NOT silently approve workflow outputs.

The Workflow Agent MUST NOT silently reject workflow outputs.

The Workflow Agent MUST NOT silently complete lifecycle transitions.

The Workflow Agent MUST NOT silently assign Authority Level.

The Workflow Agent MUST NOT silently grant privacy clearance.

The Workflow Agent MUST NOT silently convert validation success into approval.

The Workflow Agent MUST NOT silently publish, export, migrate, delete, synchronize, index, back up, or authorize downstream use.

The Workflow Agent MUST escalate when:

- workflow state is unclear;
- workflow output is incomplete;
- workflow routing conflicts with a higher-authority standard;
- human review is required;
- approval, rejection, repair, quarantine, deprecation, supersession, archival, publication, export, migration, deletion, or downstream use is affected;
- privacy risk exists;
- authority assignment is unclear;
- lifecycle transition is required or disputed;
- validation results are missing, conflicting, or incomplete;
- Source References or provenance are missing where required;
- an agent appears to exceed its operating boundary;
- implementation behavior appears to redefine workflow meaning;
- workflow behavior depends only on hidden application state, folder placement, filename convention, tag convention, user-interface state, plugin behavior, workflow memory, agent memory, or undocumented practice.

The Workflow Agent preserves role boundaries.

A Workflow Agent is not a Standards Validator merely because workflows may require validation.

A Workflow Agent is not a Privacy Agent merely because workflow routing may involve privacy risk.

A Workflow Agent is not a Metadata Agent merely because workflow state may be represented through metadata.

A Workflow Agent is not a Handoff Agent merely because workflows may require handoff notes.

A Workflow Agent is not a governance authority merely because it recommends routing.

Workflow Agent work is successful when workflow behavior remains explicit, scoped, traceable, reviewable, privacy-respecting, compatible, implementation-independent, and distinguishable from Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, role output, storage behavior, and implementation behavior.

## 11. Duplicate and Identity Agent

The Duplicate and Identity Agent is the agent role responsible for inspecting, comparing, proposing, reviewing, and reporting possible duplicates, identity conflicts, copy concerns, derivative-object concerns, merge candidates, split candidates, redirect candidates, supersession concerns, and Object Identity risks.

The Duplicate and Identity Agent exists so stable Object Identity remains preserved, traceable, reviewable, compatible, and independent of filenames, folder paths, storage locations, titles, aliases, implementation identifiers, application records, user-interface state, or agent-generated labels.

The Duplicate and Identity Agent MAY inspect:

- Knowledge Objects;
- Knowledge Records;
- stable Object Identifiers;
- temporary identifiers;
- alternate identifiers;
- legacy identifiers;
- implementation-specific identifiers;
- source identifiers;
- titles;
- aliases;
- filenames;
- folder paths;
- storage locations;
- copies;
- duplicates;
- derivative objects;
- merge candidates;
- split candidates;
- supersession candidates;
- redirect candidates;
- identity-change records;
- import records;
- export records;
- migration records;
- relationship evidence;
- provenance evidence;
- source-reference evidence;
- validation evidence.

The Duplicate and Identity Agent MAY propose duplicate findings, identity-conflict findings, copy classifications, derivative-object classifications, merge recommendations, split recommendations, redirect recommendations, supersession recommendations, identity-preservation warnings, or identity-review escalation.

The Duplicate and Identity Agent SHOULD distinguish between:

- same Object Identity;
- possible duplicate;
- confirmed duplicate;
- copy;
- derivative object;
- related object;
- alias;
- alternate identifier;
- legacy identifier;
- implementation-specific identifier;
- source identifier;
- temporary identifier;
- merge candidate;
- split candidate;
- redirect candidate;
- supersession candidate;
- identity-change candidate.

The Duplicate and Identity Agent MUST preserve the distinction between similarity and identity.

Similar titles do not prove shared Object Identity.

Similar filenames do not prove shared Object Identity.

Similar folder placement does not prove shared Object Identity.

Similar content does not always prove shared Object Identity.

Similar metadata does not always prove shared Object Identity.

Similar relationships do not always prove shared Object Identity.

Vector similarity, search similarity, backlink similarity, tag similarity, graph proximity, agent confidence, or implementation grouping MUST NOT define Object Identity by itself.

The Duplicate and Identity Agent MUST preserve the distinction between duplicate detection and merge approval.

A possible duplicate is not a confirmed duplicate.

A duplicate finding is not a merge decision.

A merge recommendation is not a merge approval.

A split recommendation is not a split approval.

A redirect recommendation is not a redirect approval.

A supersession recommendation is not a supersession approval.

The Duplicate and Identity Agent MAY produce:

- possible-duplicate reports;
- identity-conflict reports;
- identity-preservation reports;
- copy findings;
- derivative-object findings;
- merge-candidate reports;
- split-candidate reports;
- redirect-candidate reports;
- supersession-candidate reports;
- identity-risk warnings;
- identity-validation findings;
- escalation notes.

An identity or duplicate proposal SHOULD identify:

- what governed entities are involved;
- what identifiers are involved;
- what evidence suggests sameness, duplication, copying, derivation, split, merge, redirect, or supersession;
- what evidence suggests difference;
- what source, provenance, relationship, metadata, lifecycle, authority, privacy, validation, import, export, or migration context is relevant;
- what confidence or uncertainty applies;
- whether human review is required;
- whether another agent role should inspect the proposal;
- whether the proposal affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

The Duplicate and Identity Agent MUST NOT silently create, remove, merge, split, replace, redirect, delete, or reinterpret Object Identity.

The Duplicate and Identity Agent MUST NOT silently collapse two Knowledge Objects into one.

The Duplicate and Identity Agent MUST NOT silently create a new Knowledge Object because an existing object appears outdated, incomplete, duplicated, renamed, moved, copied, reformatted, reindexed, summarized, translated, backed up, restored, or displayed differently.

The Duplicate and Identity Agent MUST NOT silently discard identity history.

The Duplicate and Identity Agent MUST NOT silently erase aliases, alternate identifiers, legacy identifiers, source identifiers, import identifiers, export identifiers, migration identifiers, redirects, supersession history, or identity-change provenance where those remain relevant.

The Duplicate and Identity Agent MUST escalate when:

- Object Identity is missing, ambiguous, conflicting, duplicated, unstable, or implementation-dependent;
- two or more governed entities appear to describe the same knowledge;
- one governed entity appears to contain multiple distinct knowledge objects;
- merge, split, redirect, supersession, deprecation, archival, deletion, import, export, migration, or downstream use may be affected;
- identity evidence conflicts with metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, or Validation;
- duplicate detection would expose restricted material;
- identity resolution requires human judgment;
- identity behavior depends only on filename, folder path, storage location, tag, database row, search result, graph position, user-interface state, plugin behavior, workflow memory, agent memory, or undocumented practice.

The Duplicate and Identity Agent preserves role boundaries.

A Duplicate and Identity Agent is not a Metadata Agent merely because identity information may be represented through metadata.

A Duplicate and Identity Agent is not a Relationship Agent merely because relationships may reveal identity concerns.

A Duplicate and Identity Agent is not a Source and Provenance Agent merely because provenance may support identity analysis.

A Duplicate and Identity Agent is not a Standards Validator merely because it identifies identity non-conformance.

A Duplicate and Identity Agent is not a governance authority merely because it recommends merge, split, redirect, supersession, or identity review.

Duplicate and Identity Agent work is successful when Object Identity remains stable, explicit, traceable, reviewable, portable, privacy-respecting, compatible, implementation-independent, and distinguishable from filenames, folder paths, titles, aliases, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, workflow state, agent state, storage behavior, and implementation behavior.

## 12. Handoff Agent

The Handoff Agent is the agent role responsible for preparing, preserving, summarizing, and transferring work context between humans, agents, workflows, implementation steps, review stages, maintenance stages, publication stages, migration stages, or future project sessions.

The Handoff Agent exists so work can continue without loss of context, hidden assumptions, undocumented decisions, unresolved issues, role confusion, privacy leakage, authority confusion, validation confusion, or governance drift.

The Handoff Agent MAY inspect:

- current work context;
- governed documents;
- draft sections;
- completed sections;
- remaining sections;
- review notes;
- validation notes;
- correction notes;
- unresolved questions;
- assumptions;
- decisions made;
- dependencies;
- blockers;
- workflow state;
- agent outputs;
- escalation notes;
- implementation notes;
- next-step recommendations;
- section counts;
- milestone counts;
- file-status notes.

The Handoff Agent MAY produce:

- handoff summaries;
- continuation notes;
- next-step summaries;
- completed-work summaries;
- remaining-work summaries;
- assumption lists;
- unresolved-question lists;
- decision summaries;
- dependency summaries;
- blocker summaries;
- review-state summaries;
- validation-state summaries;
- section-count summaries;
- milestone summaries;
- escalation notes.

A handoff output SHOULD identify:

- what file, standard, workflow, implementation, or milestone the handoff concerns;
- what work has been completed;
- what work remains;
- what section count or milestone count applies where relevant;
- what assumptions were made;
- what decisions were made;
- what unresolved questions remain;
- what dependencies apply;
- what blockers or risks exist;
- what corrections are required before continuing;
- what role or workflow should act next;
- what should not be changed;
- what privacy boundaries apply;
- whether human review is required;
- whether escalation is required.

The Handoff Agent MUST preserve the distinction between handoff and approval.

A handoff summary is not approval.

A handoff summary is not validation success.

A handoff summary is not Authority Level.

A handoff summary is not Privacy Classification.

A handoff summary is not a lifecycle transition.

A handoff summary is not publication readiness.

A handoff summary is not export readiness.

A handoff summary is not migration readiness.

A handoff summary is not deletion authorization.

A handoff summary is not downstream-use permission.

The Handoff Agent MUST preserve the distinction between summary and source material.

A handoff may summarize a source, document, workflow, review, validation result, or decision.

A handoff summary does not replace the governed record, Source Reference, provenance record, validation record, approval record, decision record, or workflow log where those are required.

The Handoff Agent MUST preserve privacy boundaries.

A Handoff Agent MUST NOT expose restricted information in a handoff where the recipient, workflow, storage location, export context, publication context, implementation context, agent context, or downstream-use context is not permitted to receive it.

A Handoff Agent SHOULD summarize restricted context safely where possible without disclosing restricted content.

The Handoff Agent MUST preserve traceability.

A handoff SHOULD make clear what was inspected, what was not inspected, what was produced, what remains uncertain, what requires review, and what requires escalation.

The Handoff Agent MUST NOT silently invent completed work.

The Handoff Agent MUST NOT silently omit unresolved blockers.

The Handoff Agent MUST NOT silently convert assumptions into decisions.

The Handoff Agent MUST NOT silently convert recommendations into approvals.

The Handoff Agent MUST NOT silently convert draft material into approved material.

The Handoff Agent MUST NOT silently hide failures, corrections, review needs, validation gaps, privacy risks, authority risks, identity risks, relationship risks, source-reference risks, provenance gaps, workflow risks, implementation risks, or governance risks.

The Handoff Agent MUST escalate when:

- the next step depends on unresolved human judgment;
- a handoff would expose restricted information;
- completed work cannot be verified;
- section counts, file status, dependencies, or milestone status are unclear;
- validation status is unclear;
- approval status is unclear;
- authority status is unclear;
- privacy status is unclear;
- lifecycle status is unclear;
- workflow status is unclear;
- source or provenance support is missing where required;
- Object Identity may be affected;
- publication, export, migration, deletion, or downstream use may be affected;
- a prior agent appears to have exceeded its operating boundary;
- work context depends only on hidden memory, hidden application state, undocumented practice, or unreviewable agent output.

The Handoff Agent preserves role boundaries.

A Handoff Agent is not a Standards Validator merely because it summarizes validation state.

A Handoff Agent is not a Workflow Agent merely because it recommends next workflow steps.

A Handoff Agent is not a Metadata Agent merely because it summarizes document metadata.

A Handoff Agent is not a Privacy Agent merely because it must preserve privacy boundaries.

A Handoff Agent is not a governance authority merely because it summarizes completed work and next steps.

Handoff Agent work is successful when future humans, agents, workflows, validators, storage systems, implementation processes, and project sessions can continue work with clear context, explicit section counts, visible assumptions, preserved decisions, unresolved issues, privacy protection, traceability, implementation independence, and no silent conversion of summaries into approval, authority, validation, lifecycle transition, or governance.

## 13. Implementation Agent

The Implementation Agent is the agent role responsible for supporting implementation-specific setup, configuration, scripting, templating, automation, validation support, migration support, export support, integration support, and operational tooling while preserving The Brain Standard.

The Implementation Agent exists so reference implementations, tool-specific environments, scripts, templates, validators, repositories, vaults, plugins, integrations, and automation workflows can be built without allowing implementation behavior to redefine standard meaning.

The Implementation Agent MAY inspect:

- implementation documents;
- reference implementation files;
- operational guides;
- configuration files;
- scripts;
- templates;
- validators;
- schema-like support files;
- repository structure;
- vault structure;
- implementation-support areas;
- workflow-support areas;
- agent-support areas;
- storage-layout files;
- import-support files;
- export-support files;
- migration-support files;
- generated files;
- index files;
- cache files;
- tool-specific settings;
- implementation-specific errors;
- implementation-specific logs.

The Implementation Agent MAY propose implementation-support outputs where practical setup, automation, validation, migration, export, import, synchronization, indexing, backup, scripting, templating, or tool integration is needed.

The Implementation Agent SHOULD distinguish between:

- The Brain Standard;
- reference implementation;
- implementation document;
- operational guide;
- tool-specific configuration;
- script;
- template;
- validation tool;
- generated file;
- index;
- cache;
- implementation convenience;
- standard requirement;
- implementation-specific limitation.

The Implementation Agent MUST preserve implementation independence.

A tool may implement the standard.

A tool does not become the standard.

A vault may demonstrate the standard.

A vault does not become the standard.

A script may support the standard.

A script does not become the standard.

A template may represent standard expectations.

A template does not define standard meaning unless a governed standard or specification explicitly defines that role.

A plugin, database, file system, automation platform, model, prompt, repository, user interface, or implementation behavior MUST NOT become required for The Brain Standard to remain valid unless a higher-authority governed document explicitly defines that requirement.

The Implementation Agent MUST preserve the distinction between implementation conformance and standard conformance.

An implementation may conform within a defined scope.

A tool-specific success does not prove full standard conformance.

A script passing does not prove governance approval.

A template rendering correctly does not prove knowledge validity.

A validator running successfully does not prove approval, Authority Level, Privacy Classification, lifecycle transition, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission.

The Implementation Agent MAY produce:

- implementation setup recommendations;
- configuration recommendations;
- script recommendations;
- template recommendations;
- validator recommendations;
- migration-support recommendations;
- export-support recommendations;
- import-support recommendations;
- automation recommendations;
- repository-support recommendations;
- vault-support recommendations;
- implementation-risk reports;
- implementation-conformance notes;
- implementation-dependency notes;
- implementation-escalation notes.

An implementation proposal SHOULD identify:

- what implementation, tool, repository, vault, script, template, validator, integration, or operational environment is involved;
- what standard, specification, workflow, storage expectation, or agent boundary the implementation is intended to support;
- what implementation-specific behavior is being proposed;
- what assumptions were made;
- what dependencies apply;
- what standard-level meaning must be preserved;
- what is implementation-specific and not part of the standard;
- whether human review is required;
- whether another agent role should inspect the proposal;
- whether the proposal affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

The Implementation Agent MUST NOT silently redefine knowledge meaning.

The Implementation Agent MUST NOT silently redefine storage meaning.

The Implementation Agent MUST NOT silently redefine workflow meaning.

The Implementation Agent MUST NOT silently redefine agent permission or authority.

The Implementation Agent MUST NOT silently convert implementation behavior into standard behavior.

The Implementation Agent MUST NOT silently convert implementation success into validation success.

The Implementation Agent MUST NOT silently convert implementation convenience into governance approval.

The Implementation Agent MUST NOT silently weaken privacy boundaries, traceability, reviewability, portability, source distinction, Object Identity, metadata expectations, relationship expectations, provenance expectations, lifecycle expectations, authority expectations, or validation expectations for implementation convenience.

The Implementation Agent MUST escalate when:

- an implementation appears to redefine standard meaning;
- an implementation requires behavior not defined by the applicable standard or specification;
- tool limitations create risk to Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, workflow behavior, publication, export, migration, deletion, or downstream use;
- implementation behavior depends only on hidden application state;
- generated files, indexes, caches, scripts, plugins, or templates could be confused with governed records;
- implementation-specific identifiers could be confused with stable Object Identity;
- implementation visibility could expose restricted material;
- implementation automation could make unreviewed changes;
- implementation outputs could be mistaken for approval, authority, validation success, lifecycle transition, privacy clearance, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission;
- human judgment is required to determine implementation safety, compatibility, privacy, authority, validity, or governance effect.

The Implementation Agent preserves role boundaries.

An Implementation Agent is not a Standards Validator merely because it checks implementation conformance.

An Implementation Agent is not a Metadata Agent merely because it creates or edits templates containing metadata.

An Implementation Agent is not a Workflow Agent merely because it creates workflow-support automation.

An Implementation Agent is not a Privacy Agent merely because implementation behavior may expose restricted material.

An Implementation Agent is not a governance authority merely because it builds or configures a working system.

Implementation Agent work is successful when implementations can realize The Brain Standard in practical tools, repositories, vaults, scripts, templates, validators, workflows, and automations without weakening standard meaning, governance, reviewability, privacy, traceability, portability, compatibility, or implementation independence.

## 14. Role Interaction and Coordination

Role Interaction and Coordination defines how Agent Roles cooperate without collapsing responsibility boundaries, permission boundaries, authority boundaries, validation scopes, privacy boundaries, or review requirements.

Role interaction exists because many governed tasks require more than one role.

A Knowledge Record may require syntax inspection, standards validation, metadata review, relationship review, source-reference review, privacy review, workflow routing, duplicate detection, handoff preparation, and implementation support.

No single role SHOULD silently absorb all responsibilities merely because it can technically inspect, summarize, generate, validate, edit, route, or automate the work.

Agent Roles MAY coordinate through:

- explicit handoffs;
- workflow logs;
- validation findings;
- review notes;
- correction notes;
- escalation notes;
- role-output summaries;
- dependency notes;
- implementation-support records;
- human review records;
- governed workflow outputs.

Role coordination SHOULD identify:

- what role acted;
- what scope the role acted within;
- what material was inspected;
- what output was produced;
- what was not inspected;
- what assumptions were made;
- what unresolved issues remain;
- what role should act next;
- what workflow step should act next;
- what human review is required;
- what escalation is required;
- what privacy boundaries apply;
- what standard or specification applies where relevant.

Role interaction MUST preserve role-output distinction.

A Syntax Inspector output is not a Standards Validator output unless the role and validation scope explicitly include standards validation.

A Standards Validator output is not approval.

A Metadata Agent output is not Object Identity assignment, Authority Level assignment, Privacy Classification approval, Lifecycle State transition, or Validation State acceptance by itself.

A Relationship Agent output is not relationship approval by itself.

A Source and Provenance Agent output is not source authority, sufficient provenance, or approval by itself.

A Privacy Agent output is not privacy clearance by itself.

A Workflow Agent output is not workflow approval or lifecycle transition by itself.

A Duplicate and Identity Agent output is not merge, split, redirect, deletion, or supersession approval by itself.

A Handoff Agent output is not governance approval by itself.

An Implementation Agent output is not standard-level meaning by itself.

Role coordination MUST preserve permission boundaries.

A role may identify a needed action without having permission to perform that action.

A role may recommend an edit without having write permission.

A role may recommend movement without having move permission.

A role may recommend publication without having publication permission.

A role may recommend export without having export permission.

A role may recommend deletion without having deletion permission.

A role may recommend lifecycle transition without having lifecycle-transition permission.

A role may recommend privacy restriction without having privacy-classification authority.

Role coordination MUST preserve human review where required.

A coordinated agent chain MUST NOT convert repeated agent agreement into human review.

A coordinated agent chain MUST NOT convert multiple agent outputs into approval unless a governed workflow explicitly defines that result within a controlled scope.

A coordinated agent chain MUST NOT bypass review because all participating agents produced consistent recommendations.

Role coordination MUST preserve privacy boundaries.

A role handoff MUST NOT expose restricted content to a role, workflow, implementation, log, export, publication context, migration package, generated file, cache, index, or downstream-use context that is not permitted to receive it.

A role handoff SHOULD preserve enough context for review without unnecessarily exposing restricted material.

Role coordination MUST preserve traceability.

Where multiple roles contribute to a task, their outputs SHOULD remain traceable by role, scope, finding, assumption, unresolved issue, escalation, and review state.

A later role SHOULD NOT erase prior role outputs where those outputs remain relevant to review, validation, privacy, authority, lifecycle handling, provenance, compatibility, governance, or downstream use.

Role coordination MAY be sequential, parallel, iterative, or workflow-driven.

Sequential coordination occurs when one role acts after another.

Parallel coordination occurs when multiple roles inspect the same material for different concerns.

Iterative coordination occurs when one role’s finding causes another role to inspect, repair, validate, or escalate.

Workflow-driven coordination occurs when a governed workflow determines role order, review points, routing, approval, rejection, repair, escalation, or completion.

Role coordination SHOULD remain practical.

The Brain Standard SHOULD NOT require every role to inspect every file, record, workflow output, implementation artifact, or source item.

Role use SHOULD be proportional to risk, scope, maturity, privacy, authority, lifecycle state, validation need, publication risk, export risk, migration risk, and downstream-use impact.

Role coordination MUST escalate when:

- two roles produce conflicting findings;
- role responsibility is unclear;
- role output is being treated as approval;
- role output is being treated as Authority Level;
- role output is being treated as Privacy Classification clearance;
- role output is being treated as lifecycle transition;
- role output is being treated as validation success outside its scope;
- role output is being treated as publication, export, migration, deletion, or downstream-use permission;
- a role requires permission it does not have;
- privacy boundaries would be crossed by coordination;
- human review is required;
- implementation behavior obscures what role acted or what output was produced.

Role interaction and coordination are successful when multiple Agent Roles can cooperate efficiently while preserving responsibility boundaries, permission boundaries, authority boundaries, validation scopes, privacy boundaries, traceability, reviewability, implementation independence, and practical daily usability.

## 15. Role Boundaries and Non-Authority

Role Boundaries and Non-Authority define the limits that prevent Agent Roles from becoming hidden governance authorities.

An Agent Role defines responsibility.

An Agent Role does not define permission by itself.

An Agent Role does not define authority by itself.

An Agent Role does not define approval by itself.

An Agent Role does not define validation success by itself.

An Agent Role does not define Privacy Classification clearance by itself.

An Agent Role does not define Lifecycle State transition by itself.

An Agent Role does not define publication readiness by itself.

An Agent Role does not define export readiness by itself.

An Agent Role does not define migration readiness by itself.

An Agent Role does not define deletion authorization by itself.

An Agent Role does not define downstream-use permission by itself.

Role boundaries exist to prevent role names, tool capabilities, model confidence, workflow convenience, implementation defaults, repeated automation, or human habit from redefining The Brain Standard.

A role MAY inspect.

Inspection is not approval.

A role MAY propose.

Proposal is not approval.

A role MAY recommend.

Recommendation is not approval.

A role MAY validate within a scope.

Validation is not approval unless a governed workflow or future specification explicitly defines that effect within a controlled scope.

A role MAY route.

Routing is not lifecycle transition unless a governed workflow explicitly defines that effect within a controlled scope.

A role MAY summarize.

Summary is not source material, provenance, approval, or governed record replacement.

A role MAY generate.

Generation is not review, approval, authority, validity, privacy clearance, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission.

A role MAY automate.

Automation is not governance.

Role authority MUST be explicit where it exists.

A role has governed authority only when a standard, specification, workflow, governance process, or permission profile explicitly grants that authority within a defined scope.

Role authority SHOULD identify:

- what role is granted authority;
- what action is authorized;
- what scope applies;
- what conditions apply;
- what review is required;
- what traceability is required;
- what privacy boundaries apply;
- what escalation rules apply;
- what expiration, revocation, or limitation applies where relevant.

Agent confidence MUST NOT be treated as role authority.

Tool capability MUST NOT be treated as role authority.

Access MUST NOT be treated as role authority.

Visibility MUST NOT be treated as role authority.

Searchability MUST NOT be treated as role authority.

Implementation success MUST NOT be treated as role authority.

Workflow completion MUST NOT be treated as role authority unless explicitly governed.

Repeated correct behavior MUST NOT be treated as role authority.

Human habit MUST NOT be treated as role authority.

Role boundaries MUST protect the following governed concerns:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- review;
- approval;
- publication;
- export;
- migration;
- deletion;
- downstream use;
- governance;
- implementation independence.

A role MUST escalate when its output may affect a governed concern beyond its responsibility, permission, authority, validation scope, privacy scope, workflow scope, implementation scope, or review scope.

A role MUST escalate when a human, agent, workflow, validator, storage system, implementation, or downstream user treats the role output as more authoritative than its scope supports.

Role boundaries MUST remain visible in implementation.

A compliant implementation SHOULD make clear which role produced an output, what the role scope was, what permission applied, what review is required, what validation scope applies, and what authority does or does not exist.

A compliant implementation MUST NOT hide role boundaries in prompts, scripts, tools, logs, workflow memory, agent memory, generated files, user-interface state, database internals, or undocumented conventions where hidden boundaries would affect governed meaning, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, or downstream use.

Role Boundaries and Non-Authority are successful when Agent Roles can perform useful specialized work without silently becoming permission models, approval mechanisms, validation authorities, privacy clearance mechanisms, lifecycle-transition authorities, publication authorities, export authorities, migration authorities, deletion authorities, downstream-use authorities, implementation requirements, or governance authorities.

## 16. Role Review, Escalation, and Failure Handling

Role Review, Escalation, and Failure Handling define how Agent Roles handle uncertainty, conflict, incomplete work, boundary risk, privacy risk, authority risk, validation risk, workflow risk, implementation risk, and other conditions that require review or escalation.

Role review exists because agent outputs may be useful without being final.

An Agent Role MAY inspect, propose, recommend, summarize, validate within a scope, route, generate, or automate support work.

Those outputs may support governed activity.

Those outputs do not become governed approval, final authority, privacy clearance, lifecycle transition, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission merely because the role produced them.

Role review SHOULD occur when an agent output affects or may affect:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- workflow state;
- approval state;
- publication;
- export;
- migration;
- synchronization;
- indexing;
- backup;
- restoration;
- deletion;
- downstream use;
- implementation behavior;
- governance interpretation.

Role review MAY be performed by:

- an authorized human;
- a governed workflow;
- a Standards Validator;
- another Agent Role operating within scope;
- a future validation process;
- a future governance process;
- a future implementation-specific review mechanism.

Role review MUST remain distinguishable from role output.

A role output may require review.

A role output may support review.

A role output may be attached to review.

A role output may be considered during review.

A role output MUST NOT silently replace review where review is required.

Escalation is required when an Agent Role encounters a condition outside its responsibility, permission, authority, validation scope, privacy scope, workflow scope, implementation scope, or review scope.

Escalation MAY route an issue to:

- human review;
- governance review;
- standards validation;
- privacy review;
- authority review;
- lifecycle review;
- source-reference review;
- provenance review;
- relationship review;
- identity review;
- metadata review;
- workflow review;
- implementation review;
- repair workflow;
- quarantine workflow;
- rejection workflow;
- approval workflow;
- future specification review.

An Agent Role MUST escalate when:

- governed meaning is ambiguous;
- Object Identity may be changed, merged, split, redirected, replaced, deleted, or reinterpreted;
- metadata affects governed meaning and is missing, conflicting, unsupported, or implementation-dependent;
- a relationship affects governed meaning and is missing, conflicting, unsupported, privacy-sensitive, or implementation-dependent;
- Source References or provenance are missing where required;
- source support is weak, uncertain, restricted, unavailable, superseded, or unverifiable;
- Privacy Classification is missing, unclear, conflicting, outdated, unsupported, or at risk of being weakened;
- restricted material may be exposed;
- Authority Level is unclear, disputed, unsupported, or being inferred from agent confidence, implementation visibility, validation support, workflow convenience, or source presence;
- Lifecycle State is unclear, disputed, unsupported, or being changed without governed review;
- validation scope is unclear, incomplete, stale, disputed, or being overstated;
- workflow completion is being treated as approval without a governed rule;
- implementation behavior appears to redefine standard meaning;
- publication, export, migration, synchronization, indexing, backup, restoration, deletion, or downstream use may cross a governed boundary;
- an agent appears to exceed its operating boundary;
- a role output is being treated as more authoritative than its scope supports;
- human judgment is required.

Failure handling applies when an Agent Role cannot complete its assigned responsibility safely, correctly, traceably, or within scope.

Agent-role failure MAY include:

- incomplete inspection;
- unsupported proposal;
- ambiguous output;
- conflicting findings;
- missing evidence;
- missing source support;
- missing provenance;
- privacy risk;
- authority risk;
- validation risk;
- lifecycle risk;
- relationship ambiguity;
- metadata ambiguity;
- Object Identity ambiguity;
- workflow ambiguity;
- implementation ambiguity;
- tool failure;
- model limitation;
- missing access;
- insufficient permission;
- unreviewable output;
- hallucinated or invented information;
- hidden dependency;
- unsupported assumption;
- loss of traceability.

An Agent Role MUST NOT hide failure.

An Agent Role MUST NOT treat failure as success.

An Agent Role MUST NOT proceed as though review occurred when review did not occur.

An Agent Role MUST NOT proceed as though validation passed when validation was incomplete, failed, stale, disputed, or outside scope.

An Agent Role MUST NOT proceed as though privacy clearance exists when privacy review did not occur or remains unresolved.

An Agent Role MUST NOT proceed as though authority exists when authority was not explicitly granted.

An Agent Role MUST NOT proceed as though implementation behavior is standard behavior.

Where failure occurs, the Agent Role SHOULD produce a failure note or escalation note that identifies:

- what role was operating;
- what scope applied;
- what material was inspected;
- what material was not inspected;
- what failure occurred;
- what assumption failed or remains uncertain;
- what risk exists;
- what review is required;
- what escalation is required;
- what repair is recommended;
- what should not proceed until resolved.

When failure involves privacy risk, the failure output MUST NOT expose restricted material beyond the permitted scope.

When failure involves source or provenance weakness, the failure output SHOULD identify the weakness without inventing unsupported source support.

When failure involves Object Identity ambiguity, the failure output MUST preserve all relevant identity candidates, identifiers, aliases, source references, provenance, and uncertainty until governed review resolves the issue.

When failure involves validation ambiguity, the failure output MUST preserve the validation scope, validation limits, and unresolved findings.

When failure involves implementation ambiguity, the failure output MUST identify what behavior is implementation-specific and what standard-level meaning must be preserved.

Role conflict occurs when two or more Agent Roles produce findings that cannot all be true, complete, compatible, or safe within the same governed scope.

Role conflict MUST be escalated when it affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, downstream use, or governance interpretation.

A later Agent Role MUST NOT silently overwrite a prior role’s unresolved finding where the prior finding remains relevant.

A later Agent Role MAY revise, correct, supersede, or reject a prior role output only through a traceable review, validation, workflow, or governance process appropriate to the scope.

Where an Agent Role is omitted, unavailable, unsupported, or intentionally not used, the omitted responsibility MUST NOT be silently treated as completed.

A workflow or implementation MAY proceed without a role only where the role is not required for the scope or where the missing role responsibility is explicitly marked as not performed, deferred, out of scope, or requiring later review.

Role Review, Escalation, and Failure Handling are successful when agent-role problems remain visible, traceable, reviewable, privacy-respecting, repairable, and unable to silently become governed meaning, approval, authority, privacy clearance, validation success, lifecycle transition, publication readiness, export readiness, migration readiness, deletion authorization, downstream-use permission, implementation requirement, or governance acceptance.

## 17. Role Conformance Requirements

Role Conformance Requirements define the minimum behavior required for an Agent Role, subagent, workflow-supported role, script-supported role, implementation-supported role, or human checklist using AG-0002 to conform to this standard.

An AG-0002-conformant role SHALL preserve the purpose, scope, boundaries, reviewability, traceability, privacy expectations, validation expectations, authority expectations, lifecycle expectations, storage expectations, workflow expectations, implementation independence, and governance limits defined by this standard.

A conformance claim SHOULD identify:

- what Agent Role or roles are being claimed as conformant;
- what implementation, workflow, human process, script, model, tool, or checklist performs the role;
- what role scope applies;
- what material the role may inspect;
- what outputs the role may produce;
- what outputs the role may not produce;
- what permissions are required;
- what authority does or does not exist;
- what review is required;
- what escalation is required;
- what traceability is preserved;
- what privacy boundaries apply;
- what standards or specifications apply;
- what limitations, exceptions, or unsupported areas exist.

A conformant role MUST preserve responsibility boundaries.

A role MUST NOT silently absorb another role’s responsibility where doing so affects governed meaning, reviewability, traceability, privacy, validation, authority, lifecycle handling, publication, export, migration, deletion, downstream use, or governance interpretation.

A conformant role MUST preserve permission boundaries.

A role name MUST NOT grant permission.

A role output MUST NOT grant permission.

A tool capability MUST NOT grant permission.

Implementation visibility MUST NOT grant permission.

Agent confidence MUST NOT grant permission.

Workflow convenience MUST NOT grant permission.

A conformant role MUST preserve authority boundaries.

A role MUST NOT become a governance authority unless a governed standard, specification, workflow, governance process, or permission profile explicitly grants that authority within a defined scope.

A conformant role MUST preserve review boundaries.

Agent participation MUST NOT replace human review where human review is required.

Multiple agent outputs MUST NOT replace review unless a governed workflow explicitly defines that effect within a controlled scope.

A conformant role MUST preserve validation boundaries.

Validation MUST remain scoped.

A role that checks only syntax MUST NOT claim full validation.

A role that checks only metadata MUST NOT claim full validation.

A role that checks only relationships MUST NOT claim full validation.

A role that checks only source references or provenance MUST NOT claim full validation.

A role that checks only privacy MUST NOT claim full validation.

A role that checks only workflow behavior MUST NOT claim full validation.

A role that checks only implementation behavior MUST NOT claim full validation.

A conformant role MUST preserve privacy boundaries.

A role MUST NOT expose restricted information outside the permitted scope.

A role MUST NOT downgrade Privacy Classification for convenience.

A role MUST NOT place restricted information into summaries, logs, examples, validation outputs, workflow outputs, generated files, implementation-support files, caches, indexes, exports, migrations, publications, or downstream-use contexts where that exposure is not permitted.

A conformant role MUST preserve traceability.

Where a role output affects governed meaning, review, validation, privacy, authority, lifecycle state, publication, export, migration, deletion, or downstream use, the output SHOULD remain traceable to:

- role name;
- role scope;
- inspected material;
- produced output;
- assumptions;
- evidence or source support where applicable;
- unresolved issues;
- review needs;
- escalation needs;
- date or workflow context where applicable;
- implementation context where applicable.

A conformant role MUST preserve implementation independence.

A role MAY be implemented through a model, prompt, script, plugin, database, file system, interface, automation, validator, repository, vault, or future tool.

The implementation MUST NOT redefine the role’s standard-level meaning.

The implementation MUST NOT make itself required for AG-0002 unless a future governed implementation profile explicitly defines that requirement within its proper scope.

A conformant implementation MAY combine roles.

Combined roles are conformant only when the implementation preserves role boundaries, output distinctions, permission boundaries, review requirements, privacy boundaries, traceability requirements, escalation requirements, and non-authority rules.

A conformant implementation MAY split roles.

Split roles are conformant only when the implementation preserves the responsibility, reviewability, traceability, privacy expectations, escalation requirements, and non-authority rules of the original role.

A conformant implementation MAY omit roles where they are not required for the implementation scope.

Omitted roles are conformant only when omitted responsibilities are not silently treated as completed.

A conformant Syntax Inspector SHALL preserve the distinction between syntax inspection and standards validation.

A conformant Standards Validator SHALL preserve the distinction between validation, approval, authority, privacy clearance, lifecycle transition, publication readiness, export readiness, migration readiness, deletion authorization, and downstream-use permission.

A conformant Metadata Agent SHALL preserve the distinction between metadata, Object Identity, governed meaning, authority, privacy, lifecycle state, validation state, workflow state, agent state, storage behavior, and implementation behavior.

A conformant Relationship Agent SHALL preserve the distinction between relationships, storage signals, implementation-specific links, inferred associations, proposed relationships, and approved relationships.

A conformant Source and Provenance Agent SHALL preserve the distinction between Source Material, Knowledge Records, citations, Source References, provenance, source presence, source reliability, source authority, and approval.

A conformant Privacy Agent SHALL preserve the distinction between Privacy Classification, access, visibility, exposure, authority, validation, lifecycle state, implementation visibility, publication, export, synchronization, indexing, backup, migration, deletion, and downstream use.

A conformant Workflow Agent SHALL preserve the distinction between workflow state, workflow routing, workflow completion, review, approval, Lifecycle State, Validation State, Authority Level, Privacy Classification, publication readiness, export readiness, migration readiness, deletion authorization, and downstream-use permission.

A conformant Duplicate and Identity Agent SHALL preserve the distinction between similarity, duplication, copying, derivation, aliasing, alternate identifiers, legacy identifiers, implementation identifiers, Object Identity, merge approval, split approval, redirect approval, supersession approval, and deletion approval.

A conformant Handoff Agent SHALL preserve the distinction between summary, source material, governed record, validation result, approval record, decision record, workflow log, authority, privacy clearance, lifecycle transition, publication readiness, export readiness, migration readiness, deletion authorization, and downstream-use permission.

A conformant Implementation Agent SHALL preserve the distinction between standard meaning, reference implementation, implementation behavior, tool configuration, scripts, templates, validators, generated files, indexes, caches, automation, user-interface behavior, implementation success, and standard conformance.

A role or implementation is non-conformant when it:

- treats a role name as permission;
- treats a role output as approval;
- treats agent confidence as authority;
- treats validation as approval outside a governed scope;
- treats workflow completion as approval outside a governed scope;
- treats implementation visibility as permission;
- treats storage placement as governed meaning;
- hides role boundaries;
- hides review requirements;
- hides escalation requirements;
- exposes restricted material;
- weakens Privacy Classification for convenience;
- changes Object Identity without governed review;
- creates untraceable governed changes;
- makes implementation behavior the standard;
- omits a required role responsibility while treating it as completed.

Role Conformance Requirements are successful when Agent Roles can be evaluated consistently across humans, AI assistants, scripts, workflows, validators, repositories, vaults, implementations, and future systems without allowing role names, tool capabilities, implementation behavior, automation, confidence, convenience, or repeated practice to redefine The Brain Standard.

## 18. Success Criteria and Closing Rule

AG-0002 is successful when The Brain Standard has a clear, reusable, implementation-independent role model for agent and subagent responsibility.

AG-0002 is successful when future humans, agents, workflows, validators, storage systems, repositories, vaults, implementations, and governance processes can determine:

- what Agent Roles exist;
- what each role is responsible for;
- what each role may inspect;
- what each role may produce;
- what each role must preserve;
- what each role must escalate;
- what each role must not decide by itself;
- how roles cooperate;
- how roles remain separate;
- how role outputs remain reviewable;
- how role outputs remain traceable;
- how privacy boundaries are preserved;
- how validation boundaries are preserved;
- how authority boundaries are preserved;
- how workflow boundaries are preserved;
- how implementation independence is preserved.

AG-0002 is successful when the following core Agent Roles can be used without redefining their standard-level meaning:

1. Syntax Inspector
2. Standards Validator
3. Metadata Agent
4. Relationship Agent
5. Source and Provenance Agent
6. Privacy Agent
7. Workflow Agent
8. Duplicate and Identity Agent
9. Handoff Agent
10. Implementation Agent

AG-0002 is successful when the Syntax Inspector can improve readability, structure, Markdown correctness, grammar, spelling, heading consistency, and document mechanics without becoming a full standards validator, reviewer, approver, privacy governor, lifecycle authority, or governance authority.

AG-0002 is successful when the Standards Validator can evaluate conformance within a defined validation scope without becoming an approver, authority, privacy clearance mechanism, lifecycle-transition mechanism, publication authority, export authority, migration authority, deletion authority, or downstream-use authority.

AG-0002 is successful when the Metadata Agent can inspect and propose metadata without silently creating Object Identity, Authority Level, Privacy Classification, Lifecycle State, Validation State, approval, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission.

AG-0002 is successful when the Relationship Agent can inspect and propose relationships without silently approving relationships, redefining relationship meaning, exposing private associations, or converting storage signals into governed relationships.

AG-0002 is successful when the Source and Provenance Agent can inspect and propose Source References and provenance without converting citation presence, source presence, source reliability, or source authority into approval, Authority Level, validation success, privacy clearance, or governed acceptance.

AG-0002 is successful when the Privacy Agent can identify and escalate privacy risk without weakening Privacy Classification, exposing restricted material, or converting operational convenience into access permission, publication permission, export permission, synchronization permission, indexing permission, backup permission, agent permission, workflow permission, implementation permission, or downstream-use permission.

AG-0002 is successful when the Workflow Agent can route, recommend, and report workflow state without converting workflow completion into approval, Lifecycle State transition, validation success, Authority Level, Privacy Classification clearance, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission.

AG-0002 is successful when the Duplicate and Identity Agent can identify possible duplicates, copies, derivative objects, merge candidates, split candidates, redirect candidates, supersession candidates, and Object Identity risks without silently merging, splitting, replacing, redirecting, deleting, or reinterpreting Object Identity.

AG-0002 is successful when the Handoff Agent can preserve and transfer context without converting summaries into approval, authority, validation success, privacy clearance, lifecycle transition, publication readiness, export readiness, migration readiness, deletion authorization, or downstream-use permission.

AG-0002 is successful when the Implementation Agent can support practical tools, repositories, vaults, scripts, templates, validators, workflows, integrations, and automations without making any implementation, tool, plugin, prompt, model, script, folder structure, database, or user-interface behavior the standard itself.

AG-0002 is successful when role interaction remains efficient without collapsing role boundaries.

AG-0002 is successful when role conformance can be evaluated without requiring a specific model, runtime, software platform, database, file system, plugin, prompt, workflow tool, validation tool, repository structure, vault structure, or user interface.

AG-0002 is successful when role failure remains visible, traceable, reviewable, repairable, privacy-respecting, and escalated where required.

AG-0002 is successful when omitted roles are not silently treated as completed work.

AG-0002 is successful when combined roles remain distinguishable by responsibility, output, permission, authority, review requirement, privacy boundary, validation scope, escalation requirement, and traceability.

AG-0002 is successful when split roles preserve the responsibility and boundary expectations of the role they support.

AG-0002 is successful when agents can help The Brain operate more consistently without becoming hidden governors of The Brain.

The closing rule of AG-0002 is:

Agents may assist.

Agents may inspect.

Agents may propose.

Agents may summarize.

Agents may validate within scope.

Agents may route within workflow boundaries.

Agents may support implementation.

Agents may prepare handoffs.

Agents may identify risk.

Agents may escalate.

Agents must not silently govern.

An Agent Role is a responsibility profile, not a permission grant.

An Agent Role is a support structure, not an approval mechanism.

An Agent Role is an operational aid, not a governance substitute.

AG-0002 closes when Agent Roles are explicit enough to support practical agent work and constrained enough to preserve human reviewability, traceability, privacy, validation boundaries, authority boundaries, lifecycle boundaries, storage boundaries, workflow boundaries, implementation independence, and governed evolution.
