# AG-0002 — Agent Role and Responsibility Standard

Document ID: AG-0002
Title: Agent Role and Responsibility Standard
Version: 0.1.0
Status: Draft
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 3 — Agent Framework
Milestone: 3.2 — Agent Role and Responsibility Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard
Supersedes: None
Superseded By: None
Related: AG-0001 — Agent Operating Boundaries Standard; AG-0003 — Agent Permission and Traceability Standard

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

