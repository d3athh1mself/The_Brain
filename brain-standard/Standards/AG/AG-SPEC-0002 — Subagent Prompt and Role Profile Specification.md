# AG-SPEC-0002 — Subagent Prompt and Role Profile Specification

Document ID: AG-SPEC-0002
Title: Subagent Prompt and Role Profile Specification
Version: 0.1.0
Status: Draft
Created: 2026-06-29
Last Updated: 2026-06-29
Authority: Specification
Phase: Phase 3 — Agent Framework
Milestone: 3.5 — Subagent Prompt and Role Profile Specification
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; AG-0002 — Agent Role and Responsibility Standard; AG-0003 — Agent Permission and Traceability Standard; AG-SPEC-0001 — Agent Initialization Packet
Supersedes: None
Superseded By: None
Related: WF-SPEC-0001 — Controlled Ingestion Runbook

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, prompt rules, and role-profile rules are interpreted within AG-SPEC-0002.

Where conflicts arise between subagent prompts, subagent role profiles, agent initialization packets, agent roles, agent responsibilities, agent permissions, agent traceability, workflow instructions, tool access, platform behavior, model behavior, implementation behavior, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, publication behavior, export behavior, migration behavior, deletion behavior, or future specifications, the constitutional foundation and higher-authority standards SHALL guide interpretation and resolution.

AG-SPEC-0002 is subordinate to TB-0000, TB-0001, TB-0002, TB-0003, the Phase 1 Knowledge Standards, the Phase 2 Storage Standards, AG-0001, AG-0002, AG-0003, and AG-SPEC-0001.

AG-SPEC-0002 extends AG-SPEC-0001 by defining reusable subagent prompts and role profiles that may be included in, referenced by, or derived from an Agent Initialization Packet.

AG-SPEC-0002 defines subagent prompt and role-profile requirements at the specification level.

AG-SPEC-0002 does not define the full controlled file-drop ingestion process, exact workflow run steps, exact folder routing sequence, exact source-material processing sequence, exact review checklist, exact validation checklist, exact tool configuration, exact model provider, exact agent runtime, exact Obsidian behavior, exact Codex behavior, exact GitHub behavior, exact automation script, exact implementation setup, or exact user-interface behavior.

Those concerns belong to workflow specifications, implementation profiles, operational guides, setup guides, templates, validators, and tool-specific reference implementations.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Agent Framework refers to Layer 3 of The Brain Standard, responsible for defining how agents and subagents may interact with knowledge, source material, storage structures, workflow instructions, and implementation environments while preserving reviewability, traceability, privacy, and governance.
- Agent refers to a human-directed or system-directed AI, automation, script, model-driven process, tool-using assistant, workflow participant, or future automated actor that reads, classifies, summarizes, extracts, proposes, validates, drafts, moves, edits, creates, deletes, exports, publishes, migrates, or otherwise acts on governed material.
- Subagent refers to a bounded agent role, assistant process, prompt-defined worker, delegated agent, specialized model interaction, automation participant, script-assisted worker, or future agentic component that performs a narrower task under a parent agent, workflow, initialization packet, or governed operating scope.
- Parent Agent refers to the agent, process, workflow, human operator, or implementation context that invokes, coordinates, supervises, or receives output from one or more subagents.
- Subagent Profile refers to a reusable governed description of a subagent’s identity, purpose, scope, allowed inputs, allowed outputs, permissions, prohibitions, escalation rules, activity-recording expectations, handoff behavior, and success criteria.
- Role Profile refers to the part of a subagent profile that defines the subagent’s functional responsibility, such as intake support, classification support, source extraction support, metadata proposal, relationship proposal, validation support, privacy-risk detection, review preparation, maintenance support, export-preparation support, or implementation support.
- Subagent Prompt refers to a reusable instruction structure used to initialize or direct a subagent within a bounded scope.
- Prompt Structure refers to the required organization of a subagent prompt, including identity, task scope, inputs, outputs, constraints, permissions, prohibitions, source handling, privacy handling, validation expectations, traceability requirements, escalation rules, and handoff requirements.
- Agent Initialization Packet refers to the bounded startup packet defined by AG-SPEC-0001 that establishes what an agent or subagent must know before governed work begins.
- Agent Permission refers to an allowed agent or subagent capability within a defined scope.
- Agent Boundary refers to a rule, permission, prohibition, scope limit, review requirement, privacy constraint, authority limit, validation requirement, workflow dependency, or governance expectation that controls agent or subagent behavior.
- Agent Output refers to a result produced by an agent or subagent, including a summary, classification, proposed metadata, proposed relationship, validation result, draft record, proposed edit, file movement recommendation, warning, report, transformation, or generated content.
- Handoff refers to the structured transfer of subagent output, findings, warnings, unresolved issues, assumptions, source references, validation notes, or recommended next actions to a parent agent, workflow, reviewer, or governed record.
- Escalation refers to routing a condition, ambiguity, risk, conflict, privacy concern, authority concern, validation issue, destructive action, or critical knowledge change to human review, a parent agent, or a governed workflow.
- Governed Entity refers to a Knowledge Object, Knowledge Record, Source Material, Source Reference, provenance record, relationship, metadata record, validation result, lifecycle state, authority assignment, privacy classification, governed document, workflow output, agent output, import record, export record, migration record, decision, or other entity governed by The Brain Standard.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of AG-SPEC-0002 is to define how reusable subagent prompts and role profiles SHALL be structured within The Brain Standard.

AG-SPEC-0001 defines the Agent Initialization Packet required before agents or subagents begin governed work. AG-SPEC-0002 extends that packet by defining reusable prompt and role-profile structures for specialized subagents.

Subagent prompts and role profiles exist so that agent work can be divided into smaller, repeatable, reviewable, traceable, privacy-aware, validation-aware, source-aware, authority-aware, and implementation-independent tasks.

AG-SPEC-0002 exists to prevent subagent drift.

Subagent drift occurs when a specialized prompt, role, automation, tool configuration, implementation feature, model habit, platform default, or repeated agent behavior begins to redefine knowledge meaning, storage meaning, workflow authority, approval behavior, privacy handling, validation status, lifecycle transitions, publication readiness, export readiness, migration readiness, deletion authority, or governance without explicit authorization.

AG-SPEC-0002 defines requirements for:

- reusable subagent profiles;
- reusable subagent prompts;
- subagent identity fields;
- subagent role fields;
- subagent task scope;
- subagent input boundaries;
- subagent output boundaries;
- subagent permissions;
- subagent prohibitions;
- subagent source-awareness requirements;
- subagent privacy-awareness requirements;
- subagent validation-awareness requirements;
- subagent authority-awareness requirements;
- subagent relationship-awareness requirements;
- subagent activity recording;
- subagent handoff behavior;
- subagent escalation and stop conditions;
- standard subagent role profiles;
- subagent profile success criteria.

AG-SPEC-0002 does not make any specific model, platform, prompt syntax, agent runtime, plugin, API, repository, vault, note-taking tool, code assistant, file watcher, script, automation framework, or implementation required.

A compliant implementation MAY use AG-SPEC-0002 with ChatGPT, Codex, Claude, local models, scripted agents, Obsidian workflows, GitHub workflows, custom software, or future agent systems.

The implementation may vary.

The governed meaning of the subagent profile MUST remain explicit, portable, reviewable, and subordinate to The Brain Standard.

AG-SPEC-0002 does not define the full controlled ingestion workflow.

The full file-drop, source-material handling, extraction, draft-record creation, review routing, validation routing, repair routing, quarantine routing, approval routing, rejection routing, archive routing, and workflow-log procedure belongs to WF-SPEC-0001 — Controlled Ingestion Runbook.

AG-SPEC-0002 defines the reusable subagent roles that WF-SPEC-0001 MAY invoke.

AG-SPEC-0002 is successful when future humans, agents, workflows, validators, storage systems, implementations, and future platforms can determine:

- what a subagent is for;
- what role the subagent performs;
- what inputs the subagent may inspect;
- what outputs the subagent may produce;
- what permissions the subagent has;
- what actions the subagent is prohibited from performing;
- what standards the subagent must preserve;
- what source, privacy, validation, authority, lifecycle, metadata, relationship, and provenance boundaries apply;
- what must be recorded;
- what must be handed off;
- what must be escalated;
- when the subagent must stop;
- whether the subagent profile remains valid across implementation replacement.

## 2. Relationship to Prior Standards

AG-SPEC-0002 is subordinate to and derived from the constitutional foundation of The Brain Standard.

AG-SPEC-0002 depends on:

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
- AG-SPEC-0001 — Agent Initialization Packet.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

AG-SPEC-0002 applies that purpose by ensuring that subagent prompts and role profiles remain part of the standard-controlled Agent Framework rather than becoming hidden, tool-specific, model-specific, platform-specific, or implementation-specific behavior.

TB-0001 establishes the architecture principles that govern The Brain Standard.

AG-SPEC-0002 applies those principles by requiring subagent profiles to preserve:

- knowledge meaning;
- stable Object Identity;
- explicit structure;
- Source Material distinction;
- metadata clarity;
- relationship clarity;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- human reviewability;
- implementation independence;
- portability;
- practical daily usability;
- governed evolution.

TB-0002 establishes the layered architecture of The Brain Standard.

AG-SPEC-0002 belongs to Layer 3 — Agent Framework.

Layer 3 depends on Layer 1 and Layer 2.

Subagents may support Layer 4 workflows, but subagent prompts and role profiles MUST NOT redefine workflow authority.

Subagents may operate inside Layer 5 implementations, but subagent prompts and role profiles MUST NOT make any implementation the standard.

AG-SPEC-0002 MUST NOT create a circular dependency where:

- knowledge meaning depends on subagent output;
- storage meaning depends on subagent behavior;
- workflow approval depends on subagent confidence;
- validation state depends on subagent assertion alone;
- authority level depends on subagent confidence alone;
- privacy permission depends on subagent convenience;
- implementation compliance depends on a specific prompt format, model, tool, or runtime.

TB-0003 establishes the governance model for The Brain Standard.

AG-SPEC-0002 follows the document authority hierarchy defined by TB-0003.

As a specification-level document, AG-SPEC-0002 may define exact prompt structures, role-profile fields, output expectations, handoff requirements, and success criteria within its scope.

AG-SPEC-0002 MUST NOT contradict constitutional documents, Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, or AG-SPEC-0001.

KS-0001 defines the Knowledge Object Model.

AG-SPEC-0002 depends on KS-0001 because subagents may assist with Knowledge Objects, Knowledge Records, Source Material, Draft Knowledge Records, and governed knowledge outputs.

A subagent MAY propose, summarize, classify, extract, validate, draft, or route knowledge-related outputs.

A subagent MUST NOT cause Source Material, extracted content, a note, a folder, an implementation record, an agent output, or a draft to become approved governed knowledge merely because the subagent processed it.

KS-0002 defines Object Identity.

AG-SPEC-0002 depends on KS-0002 because subagents may encounter duplicate candidates, copied files, renamed files, moved records, source identifiers, temporary identifiers, implementation identifiers, or identity conflicts.

A subagent MAY flag identity concerns.

A subagent MAY propose possible duplicate, split, merge, derivative, or supersession concerns.

A subagent MUST NOT create, remove, merge, split, replace, redirect, or reinterpret stable Object Identity as a final governed action unless a future governed workflow or specification explicitly permits that operation within a defined scope.

KS-0003 defines metadata behavior.

AG-SPEC-0002 depends on KS-0003 because subagents may extract, propose, classify, enrich, or validate metadata.

Subagent-generated metadata MUST remain distinguishable from reviewed or approved metadata where metadata affects Object Identity, meaning, provenance, relationships, Lifecycle State, Authority Level, Privacy Classification, Validation, compatibility, publication, export, migration, or downstream use.

KS-0004 defines relationship behavior.

AG-SPEC-0002 depends on KS-0004 because subagents may propose, infer, validate, repair, enrich, or flag relationships.

A subagent-generated relationship MUST remain distinguishable from a human-reviewed or approved relationship unless a governed workflow or future specification explicitly defines automatic approval for a limited relationship type.

KS-0005 defines Source Reference and Provenance behavior.

AG-SPEC-0002 depends on KS-0005 because subagents may inspect Source Material, summarize source content, extract information, propose Source References, or create provenance notes.

Subagent activity SHOULD preserve enough provenance for a future reviewer to determine the responsible subagent role, task instruction, source material, extraction method, transformation, output, confidence where used, and review state where those affect interpretation, authority, privacy, validation, publication, export, migration, or downstream use.

KS-0006 defines Lifecycle State behavior.

AG-SPEC-0002 depends on KS-0006 because subagents may propose lifecycle states, route items for review, flag items as pending validation, or identify items needing repair.

A subagent MUST NOT approve, reject, deprecate, supersede, archive, restrict, quarantine, repair, or transition Lifecycle State as a final governed action unless a future governed workflow or specification explicitly permits that behavior within a defined scope.

KS-0007 defines Authority Level behavior.

AG-SPEC-0002 depends on KS-0007 because subagents may propose or flag authority-related information.

Subagent confidence MUST NOT be treated as Authority Level.

A subagent MAY identify possible authority concerns.

A subagent MUST NOT assign final Authority Level unless a future governed workflow or specification explicitly permits that behavior within a defined scope.

KS-0008 defines Privacy Classification behavior.

AG-SPEC-0002 depends on KS-0008 because subagents may encounter restricted, sensitive, private, export-limited, publication-limited, indexing-limited, backup-limited, or agent-limited material.

A subagent MAY detect privacy risk.

A subagent MAY propose privacy classification.

A subagent MUST NOT reduce, override, remove, bypass, or ignore Privacy Classification as a final governed action.

KS-0009 defines Validation behavior.

AG-SPEC-0002 depends on KS-0009 because subagents may perform validation checks or produce validation findings.

A subagent-generated validation result MUST NOT be treated as approval.

A validation-passing output may still require review, authority assignment, privacy review, source review, relationship review, lifecycle review, or workflow completion.

SS-0001 and SS-0002 define storage architecture and storage layout expectations.

AG-SPEC-0002 depends on the storage standards because subagents may inspect, route, recommend placement, or produce storage-related outputs without allowing folder placement, filename, path, vault behavior, repository behavior, index visibility, cache behavior, or implementation location to define knowledge meaning.

AG-0001 defines agent operating boundaries.

AG-SPEC-0002 depends on AG-0001 because every subagent profile MUST preserve agent boundaries, permissions, prohibitions, reviewability, escalation, and traceability.

AG-0002 defines agent role and responsibility expectations.

AG-SPEC-0002 depends on AG-0002 because every subagent profile MUST define a clear role, responsibility scope, input boundary, output boundary, and coordination expectation.

AG-0003 defines agent permission and traceability expectations.

AG-SPEC-0002 depends on AG-0003 because every subagent profile MUST define what actions are permitted, what actions are prohibited, what activity must be recorded, and what output must be traceable.

AG-SPEC-0001 defines the Agent Initialization Packet.

AG-SPEC-0002 depends on AG-SPEC-0001 because a subagent profile does not independently authorize work.

A subagent profile MAY be referenced by an Agent Initialization Packet.

A subagent profile MAY provide reusable role instructions for initialization.

A subagent profile MUST NOT replace the initialization packet.

A subagent may begin governed work only when its role profile is used within a bounded initialization context, workflow context, parent-agent instruction, or human-approved operating scope.

WF-SPEC-0001 — Controlled Ingestion Runbook is related but separate.

AG-SPEC-0002 defines reusable subagent roles.

WF-SPEC-0001 defines the controlled workflow that may invoke those roles.

AG-SPEC-0002 MUST NOT define the full controlled ingestion process.

WF-SPEC-0001 MUST NOT rely on undefined or unbounded subagent behavior when invoking subagents.

## 3. Subagent Profile Scope and Use Rules

A Subagent Profile is a reusable governed structure that defines how a specialized subagent may be initialized, instructed, limited, reviewed, traced, and handed off within The Brain Standard.

A Subagent Profile SHALL define a narrow role.

A Subagent Profile SHALL define a bounded task scope.

A Subagent Profile SHALL define allowed inputs.

A Subagent Profile SHALL define allowed outputs.

A Subagent Profile SHALL define permissions.

A Subagent Profile SHALL define prohibitions.

A Subagent Profile SHALL define escalation and stop conditions.

A Subagent Profile SHALL define handoff expectations.

A Subagent Profile SHALL preserve implementation independence.

A Subagent Profile MAY be used by:

- a human operator;
- a parent agent;
- a workflow;
- an implementation profile;
- an operational guide;
- a setup guide;
- a validator;
- a script;
- a future compliant agent framework.

A Subagent Profile MAY support repeated work such as:

- intake support;
- classification support;
- source extraction support;
- metadata proposal;
- relationship proposal;
- validation support;
- privacy-risk detection;
- review preparation;
- maintenance support;
- export-preparation support;
- implementation support.

A Subagent Profile MUST NOT be treated as final authority merely because it is reusable, convenient, automated, effective, platform-supported, model-supported, or repeatedly used.

A subagent profile is not a governance decision.

A subagent prompt is not approval.

A subagent output is not final authority.

A subagent confidence statement is not Authority Level.

A subagent validation finding is not approval.

A subagent classification is not final metadata assignment.

A subagent privacy-risk finding is not final Privacy Classification.

A subagent relationship proposal is not an approved relationship.

A subagent source-reference proposal is not an approved Source Reference.

A subagent lifecycle recommendation is not a final Lifecycle State transition.

A Subagent Profile MUST preserve the distinction between:

- Source Material;
- extracted content;
- summarized content;
- transformed content;
- Draft Knowledge Records;
- Knowledge Records;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- provenance notes;
- validation findings;
- privacy-risk findings;
- authority-risk findings;
- review outputs;
- workflow outputs;
- approved governed material.

A Subagent Profile MUST NOT allow a subagent to silently:

- approve Knowledge Records;
- assign final Object Identity;
- merge Knowledge Objects;
- split Knowledge Objects;
- delete governed entities;
- publish governed material;
- export governed material;
- migrate governed material;
- assign final Authority Level;
- assign final Privacy Classification;
- approve relationships;
- approve Source References;
- approve provenance records;
- perform final lifecycle transitions;
- override validation findings;
- bypass human review;
- bypass workflow requirements;
- bypass privacy boundaries;
- bypass authority boundaries;
- bypass governance.

A Subagent Profile MAY allow a subagent to perform read-only inspection where permitted.

A Subagent Profile MAY allow a subagent to summarize material where permitted.

A Subagent Profile MAY allow a subagent to extract information where permitted.

A Subagent Profile MAY allow a subagent to classify material as a proposal.

A Subagent Profile MAY allow a subagent to draft Knowledge Records as proposed outputs.

A Subagent Profile MAY allow a subagent to propose metadata.

A Subagent Profile MAY allow a subagent to propose relationships.

A Subagent Profile MAY allow a subagent to propose Source References.

A Subagent Profile MAY allow a subagent to propose provenance notes.

A Subagent Profile MAY allow a subagent to perform validation checks.

A Subagent Profile MAY allow a subagent to detect privacy risk.

A Subagent Profile MAY allow a subagent to detect authority risk.

A Subagent Profile MAY allow a subagent to prepare review outputs.

A Subagent Profile MAY allow a subagent to recommend routing, repair, quarantine, rejection, escalation, archival, or further review.

A Subagent Profile MUST define whether the subagent may write outputs directly, only return proposed outputs, or only report findings.

A Subagent Profile MUST define whether the subagent may modify files, create files, move files, rename files, or only recommend those actions.

A Subagent Profile MUST define whether the subagent may access Source Material, Draft Knowledge Records, approved Knowledge Records, governed documents, implementation-support files, workflow logs, validation outputs, archive areas, import areas, export areas, or migration areas.

A Subagent Profile MUST define what the subagent must do when material is ambiguous, missing context, privacy-sensitive, source-uncertain, authority-sensitive, validation-failing, identity-conflicting, relationship-conflicting, lifecycle-conflicting, storage-conflicting, publication-sensitive, export-sensitive, migration-sensitive, or outside scope.

A Subagent Profile MUST require escalation when a subagent encounters:

- unresolved identity conflict;
- possible duplicate, merge, split, or supersession condition;
- missing or unreliable source support;
- uncertain provenance;
- privacy risk;
- authority risk;
- validation failure affecting governed use;
- conflict with higher-authority standards;
- destructive action request;
- publication request;
- export request;
- migration request;
- deletion request;
- unsupported tool behavior;
- implementation-specific assumption that may affect standard meaning;
- task request outside the subagent profile.

A Subagent Profile MUST remain portable across implementations.

A compliant profile SHOULD be understandable without requiring a specific model, prompt engine, plugin, API, tool interface, file watcher, repository structure, vault interface, database, or automation framework.

A Subagent Profile MAY include implementation-specific notes only when those notes are clearly marked as implementation guidance and do not redefine standard-level subagent behavior.

A Subagent Profile is successful when a future human, parent agent, workflow, validator, implementation, or future model can use the profile to run a specialized subagent without losing role clarity, permission boundaries, traceability, privacy handling, source handling, validation awareness, authority control, workflow compatibility, governance alignment, or implementation independence.

## 4. Required Subagent Identity and Role Fields

A Subagent Profile SHALL include enough identity and role information for a future human, parent agent, workflow, validator, implementation, or future agent system to determine what the subagent is, what it is allowed to do, what it is not allowed to do, what output it may produce, and how its activity should be reviewed.

Subagent identity fields exist to identify the subagent profile.

Subagent identity fields do not create Knowledge Object Identity unless a future governed specification explicitly assigns that role.

A Subagent Profile MUST NOT confuse:

- subagent profile identity;
- agent identity;
- parent agent identity;
- workflow identity;
- Knowledge Object identity;
- Source Material identity;
- implementation-specific identity;
- tool-specific identity;
- temporary task identity.

A Subagent Profile SHALL include or support the following required identity fields:

- Subagent Profile ID;
- Subagent Profile Title;
- Subagent Role Name;
- Subagent Role Type;
- Version;
- Status;
- Authority;
- Created Date;
- Last Updated Date;
- Depends On;
- Related Workflows;
- Related Templates where applicable;
- Related Validation Checklists where applicable;
- Parent Agent or Invoking Context;
- Profile Owner or Responsible Reviewer where applicable.

A Subagent Profile ID SHALL identify the profile as a reusable governed profile.

A Subagent Profile ID MUST remain distinguishable from Object Identity, file identity, task identity, workflow identity, implementation identity, and model identity.

A Subagent Profile Title SHOULD be human-readable.

A Subagent Role Name SHALL identify the functional role the subagent performs.

A Subagent Role Type SHALL identify the broader category of subagent work.

Recommended Subagent Role Types MAY include:

- Intake Support;
- Classification Support;
- Source Extraction Support;
- Metadata Proposal;
- Relationship Proposal;
- Validation Support;
- Privacy-Risk Detection;
- Review Preparation;
- Maintenance Support;
- Export-Preparation Support;
- Implementation Support.

A Subagent Profile SHALL include a Purpose field.

The Purpose field SHALL explain why the subagent exists and what governed work it supports.

A Subagent Profile SHALL include a Scope field.

The Scope field SHALL define what the subagent may inspect, process, produce, or recommend.

A Subagent Profile SHALL include an Out-of-Scope field.

The Out-of-Scope field SHALL define what the subagent must not inspect, process, produce, decide, approve, modify, expose, publish, export, migrate, delete, or route.

A Subagent Profile SHALL include an Allowed Inputs field.

Allowed Inputs SHALL identify the kinds of material the subagent may receive or inspect.

Allowed Inputs MAY include:

- Source Material;
- extracted content;
- Draft Knowledge Records;
- proposed metadata;
- proposed relationships;
- proposed Source References;
- provenance notes;
- validation findings;
- privacy-risk findings;
- review notes;
- workflow outputs;
- implementation-support files;
- maintenance candidates;
- export-preparation candidates.

A Subagent Profile SHALL include a Restricted Inputs field when the subagent may encounter material that requires privacy, authority, lifecycle, validation, source, storage, implementation, publication, export, migration, or deletion limits.

A Subagent Profile SHALL include an Allowed Outputs field.

Allowed Outputs SHALL identify what the subagent may produce.

Allowed Outputs MAY include:

- summaries;
- classifications;
- extraction notes;
- proposed metadata;
- proposed relationships;
- proposed Source References;
- proposed provenance notes;
- validation findings;
- privacy-risk findings;
- authority-risk findings;
- draft Knowledge Record content;
- review-preparation notes;
- routing recommendations;
- repair recommendations;
- escalation notes;
- handoff summaries.

A Subagent Profile SHALL include a Prohibited Outputs field.

Prohibited Outputs SHALL identify outputs the subagent must not produce or must not represent as final.

A Subagent Profile SHALL include a Permission Scope field.

Permission Scope SHALL define what operations the subagent may perform within the profile.

A Subagent Profile SHALL include a Prohibited Actions field.

Prohibited Actions SHALL identify actions that are not allowed even if the subagent has tool access, storage visibility, model capability, or implementation support.

A Subagent Profile SHALL include a Source Handling field.

Source Handling SHALL define how the subagent must treat Source Material, extracted content, Source References, evidence, attribution, and provenance.

A Subagent Profile SHALL include a Privacy Handling field.

Privacy Handling SHALL define what the subagent must do when material has a Privacy Classification, suspected privacy risk, unclear privacy status, export limitation, publication limitation, indexing limitation, synchronization limitation, backup limitation, or agent-access limitation.

A Subagent Profile SHALL include an Authority Handling field.

Authority Handling SHALL define how the subagent must treat Authority Level, authority uncertainty, authority risk, source authority, relationship authority, and subagent confidence.

A Subagent Profile SHALL include a Validation Handling field.

Validation Handling SHALL define what validation checks the subagent may perform, what validation findings it may report, and what validation findings require escalation.

A Subagent Profile SHALL include a Lifecycle Handling field.

Lifecycle Handling SHALL define how the subagent must treat Draft, Review, Approved, Rejected, Deprecated, Superseded, Archived, Restricted, Quarantined, Pending Review, Pending Validation, Needs Repair, or future governed lifecycle states.

A Subagent Profile SHALL include a Relationship Handling field when the subagent may propose, inspect, validate, flag, or summarize relationships.

A Subagent Profile SHALL include an Activity Recording field.

Activity Recording SHALL define what the subagent must record or report so that its activity remains reviewable and traceable.

A Subagent Profile SHALL include a Handoff Requirement field.

Handoff Requirement SHALL define what the subagent must return to the parent agent, workflow, reviewer, or governed record after completing work.

A Subagent Profile SHALL include an Escalation and Stop Conditions field.

Escalation and Stop Conditions SHALL define when the subagent must stop work, refuse to proceed, return a warning, request human review, or route the issue to a governed workflow.

A Subagent Profile SHALL include a Success Criteria field.

Success Criteria SHALL define how a reviewer, parent agent, workflow, or validator can determine whether the subagent completed its bounded role successfully.

A Subagent Profile MAY include implementation notes.

Implementation notes MUST be clearly marked as implementation guidance.

Implementation notes MUST NOT redefine standard-level subagent identity, role, permissions, prohibitions, authority, privacy handling, validation handling, workflow behavior, or governance.

A Subagent Profile is valid only when its identity and role fields make the subagent’s purpose, scope, permissions, outputs, boundaries, review expectations, traceability requirements, and escalation conditions explicit.

## 5. Required Prompt Structure

A Subagent Prompt SHALL provide a clear, bounded, reviewable instruction structure for directing a subagent within a governed scope.

A Subagent Prompt MAY be written in Markdown, plain text, structured fields, YAML-compatible blocks, JSON-compatible structures, prompt templates, implementation-specific prompt formats, or future governed prompt formats.

The prompt format may vary by implementation.

The governed meaning of the prompt MUST remain explicit, portable, reviewable, and subordinate to The Brain Standard.

A Subagent Prompt MUST NOT rely on hidden model memory, hidden tool state, undocumented platform behavior, chat history, implementation defaults, repository visibility, folder placement, or prior agent behavior when those affect governed meaning, permissions, privacy, authority, validation, lifecycle state, source handling, relationship handling, publication, export, migration, deletion, or downstream use.

A Subagent Prompt SHALL include the following required structure:

1. Subagent Identity
2. Role Purpose
3. Operating Context
4. Task Scope
5. Allowed Inputs
6. Required Outputs
7. Permission Boundaries
8. Prohibited Actions
9. Source and Provenance Requirements
10. Privacy Requirements
11. Authority Requirements
12. Validation Requirements
13. Relationship Requirements where applicable
14. Lifecycle Requirements where applicable
15. Activity Recording Requirements
16. Handoff Requirements
17. Escalation and Stop Conditions
18. Success Criteria

The Subagent Identity section SHALL identify the subagent role being invoked.

The Subagent Identity section SHOULD include:

- Subagent Profile ID;
- Role Name;
- Role Type;
- Version;
- Parent Agent or Invoking Context;
- Related workflow where applicable.

The Role Purpose section SHALL state what the subagent is responsible for.

The Role Purpose section MUST state the role as bounded assistance, not final authority.

The Operating Context section SHALL define the standards, workflow, storage context, source context, implementation context, or human instruction that governs the subagent’s work.

The Operating Context section MUST identify AG-SPEC-0001 or an equivalent initialization context when the subagent is being used for governed work.

The Task Scope section SHALL define what the subagent must do.

The Task Scope section MUST be narrow enough that the subagent can complete the task without redefining its role, inventing new authority, or crossing into unrelated workflow behavior.

The Allowed Inputs section SHALL identify the material the subagent may inspect or process.

The Allowed Inputs section MUST identify privacy, authority, source, validation, lifecycle, storage, implementation, publication, export, migration, or deletion limits where they are known.

The Required Outputs section SHALL define the expected output format.

Required Outputs SHOULD be structured enough for review, validation, handoff, and later reuse.

Required Outputs MAY include:

- findings;
- proposals;
- warnings;
- extracted content;
- classification notes;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- provenance notes;
- validation findings;
- privacy-risk findings;
- authority-risk findings;
- routing recommendations;
- unresolved questions;
- escalation notes.

The Permission Boundaries section SHALL state what the subagent may do.

The Prohibited Actions section SHALL state what the subagent must not do.

A Subagent Prompt MUST NOT omit prohibited actions when the task involves governed material, Source Material, privacy-sensitive content, authority-sensitive content, validation-sensitive content, storage changes, workflow routing, publication, export, migration, deletion, or downstream use.

The Source and Provenance Requirements section SHALL define how the subagent must preserve source context, extraction context, transformation context, evidence notes, attribution notes, or uncertainty notes.

The Privacy Requirements section SHALL define how the subagent must handle known or suspected privacy boundaries.

The Authority Requirements section SHALL define how the subagent must handle authority boundaries and confidence statements.

The Validation Requirements section SHALL define what validation checks, warnings, limitations, or review requirements apply.

The Relationship Requirements section SHALL be included when the subagent may identify, propose, inspect, validate, or flag relationships.

The Lifecycle Requirements section SHALL be included when the subagent may inspect, propose, route, or flag lifecycle-related status.

The Activity Recording Requirements section SHALL define what the subagent must report about its work.

Activity recording SHOULD include:

- role invoked;
- task performed;
- inputs inspected;
- outputs produced;
- assumptions made;
- uncertainty identified;
- source issues found;
- privacy issues found;
- authority issues found;
- validation issues found;
- relationship issues found where applicable;
- lifecycle issues found where applicable;
- escalation conditions triggered;
- recommended next action.

The Handoff Requirements section SHALL define what the subagent must return to the parent agent, workflow, reviewer, or governed record.

A handoff SHOULD be structured enough that another human, agent, workflow, or validator can continue without relying on hidden context.

The Escalation and Stop Conditions section SHALL define when the subagent must stop or escalate instead of continuing.

A Subagent Prompt MUST require the subagent to stop or escalate when:

- the task exceeds the subagent role;
- required input is missing;
- source support is missing or unreliable;
- provenance is uncertain;
- privacy risk is present or unclear;
- authority risk is present or unclear;
- validation fails in a way that affects governed use;
- Object Identity conflict is detected;
- relationship conflict is detected;
- lifecycle conflict is detected;
- the prompt conflicts with a higher-authority standard;
- the prompt requests a prohibited action;
- the prompt requires publication, export, migration, deletion, final approval, final Authority Level, final Privacy Classification, final lifecycle transition, approved relationship, or approved Source Reference without governed authorization.

The Success Criteria section SHALL define how completion is evaluated.

A Subagent Prompt is successful when the subagent can perform its bounded task, produce reviewable output, preserve source and provenance context, respect privacy and authority boundaries, report validation concerns, escalate unresolved issues, and hand off results without redefining the standard, workflow, implementation, or governance.

## 6. Required Permission and Authority Boundaries

A Subagent Profile SHALL define permission and authority boundaries before the subagent performs governed work.

Permission defines what the subagent may do.

Authority defines what the subagent’s output may mean.

Permission does not create authority.

Tool access does not create permission.

Permission does not create approval.

Approval does not exist merely because a subagent completed a task.

A Subagent Profile MUST preserve the distinction between:

- allowed access;
- allowed operation;
- allowed output;
- recommended action;
- proposed change;
- validation finding;
- confidence statement;
- review output;
- workflow output;
- approved governed action.

A Subagent Profile SHALL identify whether the subagent may perform:

- read operations;
- search operations;
- inspection operations;
- summarization operations;
- extraction operations;
- classification operations;
- metadata proposal operations;
- relationship proposal operations;
- Source Reference proposal operations;
- provenance proposal operations;
- validation-support operations;
- privacy-risk detection operations;
- authority-risk detection operations;
- draft-preparation operations;
- review-preparation operations;
- routing-recommendation operations;
- write operations;
- move operations;
- rename operations;
- archive-recommendation operations;
- quarantine-recommendation operations;
- export-preparation operations;
- implementation-support operations.

A Subagent Profile SHALL identify whether each permitted operation is:

- read-only;
- proposal-only;
- draft-producing;
- report-producing;
- write-capable;
- movement-capable;
- implementation-supporting;
- workflow-supporting;
- human-review-required;
- prohibited.

A Subagent Profile MUST define permission scope by at least:

- governed entity type;
- storage area or input source where applicable;
- workflow stage where applicable;
- allowed operation;
- allowed output;
- required review;
- privacy limit;
- authority limit;
- validation expectation;
- escalation condition.

A Subagent Profile MUST NOT treat broad tool access as broad permission.

A subagent that can technically read files MAY only read files permitted by its profile, initialization packet, workflow context, privacy boundary, and governed instruction.

A subagent that can technically write files MAY only write files when the profile, initialization packet, workflow context, storage rules, privacy boundaries, and human or governed authorization allow writing.

A subagent that can technically move, rename, archive, export, publish, migrate, or delete files MUST NOT perform those actions unless a governed workflow or explicit authorization permits the action within a defined scope.

A Subagent Profile SHALL define authority limits.

Authority limits SHALL state what the subagent output can and cannot mean.

Subagent output MAY mean:

- proposed classification;
- proposed metadata;
- proposed relationship;
- proposed Source Reference;
- proposed provenance note;
- proposed lifecycle recommendation;
- proposed authority concern;
- proposed privacy concern;
- validation finding;
- review preparation;
- routing recommendation;
- escalation recommendation;
- draft content;
- implementation-support note.

Subagent output MUST NOT mean final approval unless a future governed workflow or specification explicitly grants limited approval authority within a defined scope.

Subagent output MUST NOT silently create:

- approved Knowledge Records;
- approved Source References;
- approved relationships;
- final Authority Levels;
- final Privacy Classifications;
- final Lifecycle State transitions;
- final Validation State where review is required;
- publication permission;
- export permission;
- migration permission;
- deletion permission;
- downstream-use permission.

A Subagent Profile MUST state that subagent confidence does not equal Authority Level.

A high-confidence subagent output may still be wrong, incomplete, unsupported, privacy-risky, authority-limited, validation-failing, lifecycle-inappropriate, source-uncertain, relationship-conflicting, or outside scope.

A Subagent Profile MUST state that validation findings do not equal approval.

A validation-passing output may still require source review, privacy review, authority review, relationship review, lifecycle review, workflow review, implementation review, or human approval.

A Subagent Profile MUST state that workflow completion does not equal approval unless the applicable workflow explicitly defines that approval transition.

A Subagent Profile MUST require human or governed review before final decisions that affect:

- Object Identity;
- Knowledge Object meaning;
- Knowledge Record approval;
- Source Reference approval;
- provenance approval;
- relationship approval;
- Lifecycle State transition;
- Authority Level assignment;
- Privacy Classification assignment;
- Validation State acceptance where review is required;
- publication;
- export;
- migration;
- deletion;
- merge;
- split;
- supersession;
- deprecation;
- downstream use;
- governance.

A Subagent Profile MAY define limited automatic behavior only when a higher-authority standard, governed workflow, or future specification explicitly permits that behavior.

Limited automatic behavior MUST be:

- scoped;
- reviewable;
- traceable;
- reversible where practical;
- privacy-respecting;
- validation-aware;
- authority-aware;
- source-aware;
- implementation-independent where governed meaning is affected;
- compatible with the applicable workflow.

A Subagent Profile MUST require escalation when permission or authority is unclear.

A subagent MUST stop rather than continue when continuing would require inventing permission, assuming approval, bypassing privacy, overriding authority, ignoring validation, or treating implementation capability as governance.

A Subagent Profile is successful when a future human, parent agent, workflow, validator, implementation, or future agent system can determine exactly what the subagent may do, what the subagent may produce, what the output means, what the output does not mean, what requires review, what requires escalation, and what actions are prohibited.

