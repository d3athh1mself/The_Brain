# AG-SPEC-0001 — Agent Initialization Packet

Document ID: AG-SPEC-0001
Title: Agent Initialization Packet
Version: 0.1.0
Status: Approved
Created: 2026-06-29
Last Updated: 2026-06-29
Authority: Specification
Phase: Phase 3 — Agent Framework
Milestone: 3.4 — Agent Initialization Packet
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; AG-0002 — Agent Role and Responsibility Standard; AG-0003 — Agent Permission and Traceability Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; WF-0003 — Knowledge Maintenance and Update Workflow Standard; WF-0004 — Publication, Export, and Downstream Use Workflow Standard; VALID-0001 — Bare Usable Validation Checklist
Supersedes: None
Superseded By: None
Related: AG-SPEC-0002 — Subagent Prompt and Role Profile Specification; WF-SPEC-0001 — Controlled Ingestion Runbook; TEMPLATE-0003 — Agent Activity Record Template; TEMPLATE-0004 — Review Record Template

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, initialization rules, agent boundaries, role assignments, operating context, traceability expectations, and escalation requirements are interpreted within AG-SPEC-0001.

Where conflicts arise between agent initialization, agent identity, agent roles, agent permissions, operating context, tool access, model access, workflow participation, storage access, Source Material handling, Knowledge Records, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, review requirements, activity recording, escalation, stop conditions, implementation behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

AG-SPEC-0001 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

AG-SPEC-0001 is subordinate to AG-0001, AG-0002, and AG-0003.

AG-SPEC-0001 operationalizes prior agent standards by defining the practical packet used to initialize an agent before governed work begins.

AG-SPEC-0001 does not replace AG-0001, AG-0002, or AG-0003.

AG-SPEC-0001 does not define full subagent prompt profiles.

Detailed subagent prompt profiles belong to AG-SPEC-0002 — Subagent Prompt and Role Profile Specification.

AG-SPEC-0001 does not define the full controlled file-drop ingestion process.

The controlled ingestion process belongs to WF-SPEC-0001 — Controlled Ingestion Runbook.

If AG-SPEC-0001 appears to conflict with a higher-authority document, the higher-authority document takes precedence unless formally revised through governance.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Agent Framework refers to Layer 3 of The Brain Standard, responsible for defining how agents may interact with knowledge, source material, storage structures, workflow instructions, and implementation environments while preserving reviewability, traceability, privacy, and governance.
- Agent refers to a human-directed or system-directed AI, automation, script, model-driven process, tool-using assistant, workflow participant, or future automated actor that performs governed work within The Brain Standard.
- Subagent refers to an agent assigned to a narrower role, task, workflow stage, review function, validation function, or operating scope within the Agent Framework.
- Agent Initialization refers to the process of preparing an agent before governed work begins by giving it the identity, role, operating context, permission boundaries, source awareness, privacy awareness, validation expectations, traceability requirements, escalation rules, and stop conditions required for safe operation.
- Agent Initialization Packet or Initialization Packet refers to the structured startup packet that defines what an agent is, what it is assigned to do, what standards govern it, what it may access, what it may produce, what it must record, and what it must escalate.
- Agent Identity refers to the explicit identification of an agent, subagent, automation, tool-using process, model-assisted process, script, or implementation-specific agent profile operating within The Brain Standard.
- Operating Context refers to the governed project, file set, storage area, workflow stage, task, implementation environment, source set, review state, or other bounded context in which an agent is operating.
- Role Assignment refers to the governed assignment of an agent to a defined role, responsibility, task category, workflow function, or subagent profile.
- Permission Boundary refers to the explicit limit on what an agent may read, search, summarize, extract, classify, propose, validate, draft, write, move, export, publish, migrate, delete, or otherwise affect.
- Authority Boundary refers to the limit preventing an agent from becoming the final authority for governed meaning, approval, lifecycle transition, Authority Level assignment, Privacy Classification assignment, validation acceptance, publication, export, migration, deletion, or governance unless explicitly permitted by a higher-authority governed process.
- Privacy Boundary refers to the Privacy Classification, access rule, exposure limit, routing limit, publication limit, export limit, synchronization limit, indexing limit, agent-access limit, or downstream-use limit that governs how material may be handled.
- Source Awareness refers to the agent’s required understanding of Source Material, Source References, provenance, extraction history, transformation history, and source-derived knowledge boundaries.
- Validation Awareness refers to the agent’s required understanding that validation may support review but does not become approval, authority, privacy clearance, publication permission, export permission, migration permission, or downstream-use permission by itself.
- Agent Activity Record refers to a traceable record of agent identity, task, operating context, permissions, inputs, outputs, actions, recommendations, validation findings, review state, escalation, and other required activity details.
- Traceability refers to the ability to determine what an agent did, what material it used, what output it produced, what permission scope applied, what review state applies, and whether escalation or correction is required.
- Escalation refers to routing ambiguity, risk, conflict, privacy concern, authority concern, validation issue, destructive action, or critical knowledge change to human review or a governed workflow.
- Stop Condition refers to a condition that requires an agent to pause, refuse, escalate, or avoid continuing because proceeding may violate a standard, permission boundary, privacy boundary, workflow rule, validation expectation, authority limit, or governance requirement.
- Human Review refers to review, correction, acceptance, rejection, approval, or escalation performed by an authorized human.
- Governed Entity refers to a Knowledge Object, Knowledge Record, Source Material, Source Reference, provenance record, relationship, metadata record, validation result, lifecycle state, authority assignment, privacy classification, governed document, workflow output, agent output, import record, export record, migration record, decision, or other entity governed by The Brain Standard.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of AG-SPEC-0001 is to define the Agent Initialization Packet used to prepare an agent before it performs governed work inside The Brain Standard.

AG-SPEC-0001 turns the existing agent standards into a practical startup structure.

The Agent Initialization Packet exists so that an agent does not begin work from hidden assumptions, incomplete context, tool defaults, model defaults, workflow convenience, implementation behavior, memory, chat history, folder access, or search visibility.

An agent initialized under AG-SPEC-0001 should know:

- what project it is operating inside;
- what standard governs its work;
- what role it has been assigned;
- what task it is performing;
- what material it may access;
- what material it must not access;
- what actions it may perform;
- what actions it must not perform;
- what output it may produce;
- what output requires human review;
- what source, privacy, validation, authority, lifecycle, and relationship boundaries apply;
- what activity must be recorded;
- what ambiguity, risk, conflict, or prohibited condition must be escalated;
- what conditions require the agent to stop.

AG-SPEC-0001 exists to prevent initialization drift.

Initialization drift occurs when agents begin governed work with unclear identity, unclear role, unclear scope, unclear permission boundaries, unclear privacy limits, unclear source requirements, unclear validation expectations, unclear review requirements, unclear activity-recording expectations, or unclear escalation rules.

Initialization drift can cause agent authority creep, privacy exposure, validation confusion, relationship confusion, source-reference gaps, provenance loss, lifecycle-state confusion, authority confusion, workflow drift, storage drift, implementation lock-in, or governance drift.

AG-SPEC-0001 defines initialization behavior for:

- agent identity;
- assigned role;
- operating context;
- task scope;
- permission boundaries;
- authority boundaries;
- privacy boundaries;
- source-awareness requirements;
- validation-awareness requirements;
- relationship-awareness requirements;
- lifecycle-awareness requirements;
- activity-recording requirements;
- traceability expectations;
- escalation requirements;
- stop conditions;
- initialization success criteria.

AG-SPEC-0001 does not grant agents new authority.

AG-SPEC-0001 does not approve autonomous operation.

AG-SPEC-0001 does not allow an agent to approve Knowledge Records, assign final Authority Level, assign final Privacy Classification, perform final lifecycle transitions, publish, export, migrate, delete, supersede, deprecate, or govern knowledge unless a higher-authority governed workflow or specification explicitly permits that action within a defined scope.

AG-SPEC-0001 does not replace AG-0001.

AG-0001 defines standard-level agent operating boundaries.

AG-SPEC-0001 defines how those boundaries are delivered to an agent before operation.

AG-SPEC-0001 does not replace AG-0002.

AG-0002 defines agent roles and responsibilities.

AG-SPEC-0001 requires the initialization packet to identify the assigned role.

AG-SPEC-0001 does not replace AG-0003.

AG-0003 defines agent permission, traceability, and review expectations.

AG-SPEC-0001 requires the initialization packet to identify the permission and traceability boundaries that apply before work begins.

The primary purpose of AG-SPEC-0001 is to make agent startup repeatable, bounded, inspectable, reviewable, privacy-respecting, validation-aware, source-aware, authority-aware, workflow-compatible, and implementation-independent.

AG-SPEC-0001 is successful when future humans, agents, workflows, validators, storage systems, implementations, import processes, export processes, migration processes, publication processes, and governance processes can determine:

- what agent was initialized;
- what role the agent was assigned;
- what task the agent was given;
- what operating context applied;
- what permission scope applied;
- what privacy boundary applied;
- what authority boundary applied;
- what source and provenance expectations applied;
- what validation expectations applied;
- what activity-recording requirement applied;
- what escalation and stop conditions applied;
- whether the agent was initialized sufficiently before operating;
- whether the agent remained within its initialized scope.

## 2. Relationship to Prior Standards

AG-SPEC-0001 is subordinate to and derived from the constitutional foundation of The Brain Standard.

AG-SPEC-0001 depends on:

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
- WF-0004 — Publication, Export, and Downstream Use Workflow Standard;
- VALID-0001 — Bare Usable Validation Checklist.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

AG-SPEC-0001 applies that purpose by ensuring that agents can assist knowledge work without making agent memory, model behavior, prompts, tools, folder access, implementation defaults, or workflow convenience the source of governed meaning.

TB-0001 establishes the architecture principles that govern The Brain Standard.

AG-SPEC-0001 applies those principles by requiring agent initialization to preserve:

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

AG-SPEC-0001 belongs to Layer 3 — Agent Framework.

Layer 3 may define how agents interact with knowledge, storage, workflows, validation, and implementations.

Layer 3 MUST NOT redefine Layer 1 knowledge meaning.

Layer 3 MUST NOT redefine Layer 2 storage meaning.

Layer 3 MUST NOT make Layer 4 workflow authority depend on agent confidence.

Layer 3 MUST NOT make Layer 5 implementation behavior the standard.

AG-SPEC-0001 preserves these layer boundaries by requiring every initialized agent to receive explicit operating context, role assignment, permission boundaries, and escalation requirements before acting.

TB-0003 establishes the governance model for The Brain Standard.

AG-SPEC-0001 follows the document authority hierarchy defined by TB-0003.

As a specification-level document, AG-SPEC-0001 may define exact initialization structure, fields, required packet elements, and startup behavior for agents.

AG-SPEC-0001 MUST NOT contradict constitutional documents or higher-authority standards.

The Phase 1 Knowledge Standards define the meaning that agents must preserve.

AG-SPEC-0001 depends on KS-0001 through KS-0009 because an initialized agent may interact with Knowledge Objects, Knowledge Records, Source Material, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation.

An Initialization Packet MUST make the agent aware that it may assist with these concepts but MUST NOT redefine them.

The Phase 2 Storage Standards define how storage supports knowledge without defining knowledge meaning.

AG-SPEC-0001 depends on SS-0001 and SS-0002 because initialized agents may read, classify, draft, route, recommend movement, or operate within storage environments.

An Initialization Packet MUST make clear that storage access is not unrestricted permission and that folder placement, filenames, paths, tags, index location, cache location, or implementation workspace do not define governed meaning by themselves.

AG-0001 defines agent operating boundaries.

AG-SPEC-0001 operationalizes AG-0001 by requiring those boundaries to be present before agent work begins.

An Initialization Packet MUST preserve the AG-0001 rule that agents may assist, propose, draft, validate, organize, and execute bounded workflow steps, but must not silently govern.

AG-0002 defines agent roles and responsibilities.

AG-SPEC-0001 depends on AG-0002 because initialization requires role assignment.

An Initialization Packet MUST identify the role the agent is performing or state that the role is unresolved and requires review before governed work proceeds.

AG-0003 defines agent permission, traceability, and review expectations.

AG-SPEC-0001 depends on AG-0003 because initialization requires permission boundaries, activity recording, review requirements, output traceability, and escalation handling.

An Initialization Packet MUST identify what the agent may do, what it must not do, what it must record, what requires review, and what requires escalation.

The Phase 4 Workflow Standards define how agents participate in governed workflows.

AG-SPEC-0001 depends on WF-0001 through WF-0004 because initialized agents may assist ingestion, review, maintenance, publication preparation, export preparation, migration preparation, or downstream-use evaluation only within governed workflow boundaries.

An Initialization Packet MUST NOT convert workflow participation into approval, authority, privacy clearance, validation acceptance, publication permission, export permission, migration permission, deletion permission, or downstream-use clearance.

VALID-0001 defines bare usable validation expectations.

AG-SPEC-0001 supports VALID-0001 by making supervised agent setup more repeatable, inspectable, reviewable, and testable during bare usable deployment.

AG-SPEC-0001 is successful when it extends the prior standards into a practical initialization packet without weakening Object Identity, metadata boundaries, relationship behavior, Source Reference behavior, provenance preservation, Lifecycle State, Authority Level, Privacy Classification, Validation, storage boundaries, agent boundaries, workflow boundaries, implementation independence, governance, or practical daily usability.

## 3. Initialization Packet Scope and Use Rules

Initialization Packet Scope and Use Rules define when an Agent Initialization Packet is required, what the packet governs, what it does not govern, and how the packet should be used before agent activity begins.

An Agent Initialization Packet applies to any agent, subagent, automation, model-assisted process, tool-using assistant, workflow participant, script, implementation-specific agent profile, or future automated actor that performs governed work inside The Brain Standard.

An Initialization Packet SHOULD be used before an agent performs work that may affect:

- Knowledge Objects;
- Knowledge Records;
- Source Material;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- governed documents;
- storage routing;
- workflow outputs;
- agent outputs;
- import preparation;
- export preparation;
- migration preparation;
- publication preparation;
- deletion recommendations;
- downstream use;
- governance.

An Initialization Packet MAY be used for low-risk read-only work when doing so improves consistency, traceability, reviewability, privacy protection, validation support, or implementation independence.

An Initialization Packet MUST be used where agent activity affects governed meaning, privacy boundaries, authority boundaries, validation state, lifecycle transitions, Source References, provenance, relationship proposals, publication readiness, export readiness, migration readiness, destructive action, or downstream-use permission.

### 3.1 Packet Scope

An Initialization Packet SHALL define or support identification of the scope in which the agent is operating.

Packet scope MAY include:

- a specific agent identity;
- a specific role;
- a specific task;
- a specific user instruction;
- a specific workflow stage;
- a specific Knowledge Object;
- a specific Knowledge Record;
- a specific Source Material set;
- a specific storage area;
- a specific governed document;
- a specific validation scope;
- a specific privacy boundary;
- a specific authority boundary;
- a specific import package;
- a specific export package;
- a specific migration package;
- a specific implementation environment;
- a specific review package;
- another governed scope.

A packet scope MUST NOT imply broader permission than it explicitly grants.

Permission to inspect one file does not imply permission to inspect all files.

Permission to summarize Source Material does not imply permission to create an approved Knowledge Record.

Permission to propose metadata does not imply permission to assign final metadata.

Permission to propose relationships does not imply permission to create approved relationships.

Permission to validate does not imply permission to approve.

Permission to prepare an export does not imply permission to release the export.

Permission to recommend deletion does not imply permission to delete.

### 3.2 Required Use Before Governed Work

An agent SHOULD NOT begin governed work until it has received enough initialization context to determine:

- what it is;
- what role it is performing;
- what task it has been assigned;
- what standards govern the task;
- what material it may access;
- what material is out of scope;
- what operations it may perform;
- what operations are prohibited;
- what output it may create;
- what output must remain proposed;
- what output requires review;
- what must be recorded;
- what must be escalated;
- what requires the agent to stop.

Where initialization context is incomplete, ambiguous, contradictory, privacy-sensitive, authority-sensitive, validation-sensitive, or high-risk, the agent SHOULD escalate before proceeding.

Where proceeding would violate a higher-authority standard, privacy boundary, permission boundary, workflow rule, validation expectation, governance requirement, or explicit stop condition, the agent MUST stop or refuse the affected action.

### 3.3 Packet Authority

An Initialization Packet is an operating instruction.

An Initialization Packet is not a constitutional document, standard, approval record, authority assignment, privacy clearance, validation result, publication approval, export approval, migration approval, deletion approval, or downstream-use clearance by itself.

An Initialization Packet MAY grant bounded task permission where the permission is consistent with higher-authority standards, workflows, privacy classifications, authority levels, validation expectations, and governance rules.

An Initialization Packet MUST NOT grant permission that contradicts higher-authority documents.

An Initialization Packet MUST NOT override AG-0001, AG-0002, AG-0003, or any applicable Knowledge Standard, Storage Standard, Workflow Standard, validation requirement, privacy boundary, authority boundary, or governance requirement.

If a packet instruction conflicts with a higher-authority document, the higher-authority document controls unless formally revised through governance.

### 3.4 Packet Completeness

An Initialization Packet SHOULD be complete enough for the assigned agent task.

A complete packet SHOULD identify:

- agent identity;
- role assignment;
- assigned task;
- operating context;
- governing standards;
- allowed operations;
- prohibited operations;
- permission scope;
- privacy boundary;
- authority boundary;
- validation expectations;
- Source Material and provenance expectations;
- required output format;
- required activity recording;
- required review points;
- escalation conditions;
- stop conditions.

A partial packet MAY be used only for low-risk work where missing context does not affect governed meaning, privacy, authority, validation, lifecycle state, source traceability, relationships, publication, export, migration, deletion, or downstream use.

A packet with missing required context MUST be treated as incomplete.

An incomplete packet SHOULD trigger clarification, limitation of scope, or escalation.

### 3.5 Packet Reuse

An Initialization Packet MAY be reused for repeated tasks only when the task, role, scope, permissions, privacy boundary, authority boundary, validation expectations, and workflow context remain materially the same.

A reused packet MUST NOT silently expand to new tasks, new storage areas, new privacy classes, new authority contexts, new workflow stages, new implementations, new exports, new migrations, new publication contexts, or new destructive actions.

Where task scope changes, the packet SHOULD be reviewed and updated.

Where privacy, authority, validation, workflow, source, provenance, lifecycle, relationship, or storage conditions change, the packet SHOULD be reviewed before reuse.

### 3.6 Implementation Independence

An Initialization Packet MUST remain implementation-independent.

An Initialization Packet MAY be represented in Markdown, plain text, YAML, JSON, a prompt template, a task card, a workflow form, an implementation profile, a script configuration, or another practical format.

The representation does not define the standard.

A specific model, prompt system, tool, plugin, vault, repository, script, user interface, agent runtime, automation framework, operating system, or software implementation MUST NOT become required by AG-SPEC-0001.

A compliant implementation MAY adapt the packet format to its environment only if the adapted format preserves the meaning, boundaries, reviewability, traceability, privacy expectations, validation expectations, authority limits, and escalation rules defined by AG-SPEC-0001.

### 3.7 Packet Output Handling

An initialized agent MAY produce outputs allowed by its packet, role, scope, permission boundary, and governing workflow.

Agent output MAY include:

- summaries;
- classifications;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- provenance notes;
- lifecycle-state proposals;
- authority notes;
- privacy-classification proposals;
- validation findings;
- draft Knowledge Records;
- draft governed documents;
- review reports;
- repair recommendations;
- routing recommendations;
- escalation notes;
- implementation-support notes;
- future governed output types.

Agent output MUST remain distinguishable from approved governed material unless accepted through a governed review or workflow process.

Agent output MUST NOT become approval, authority, privacy clearance, validation acceptance, publication permission, export permission, migration permission, deletion permission, or downstream-use clearance merely because the agent was initialized.

### 3.8 Packet Review and Update

An Initialization Packet SHOULD be reviewable.

A reviewer SHOULD be able to determine:

- what packet initialized the agent;
- what version of the packet was used;
- what agent received the packet;
- what role was assigned;
- what task was assigned;
- what scope applied;
- what permissions applied;
- what privacy boundary applied;
- what authority boundary applied;
- what validation expectations applied;
- what output was allowed;
- what review was required;
- what escalation and stop conditions applied.

An Initialization Packet MAY be revised, replaced, superseded, deprecated, archived, or rejected through a governed process.

A revised packet SHOULD preserve enough traceability to determine what changed and whether prior agent activity remains valid, limited, rejected, repairable, or subject to review.

An agent MUST NOT continue operating under a packet that is revoked, rejected, superseded, expired, invalid, or outside the current task scope.

### 3.9 Scope and Use Success Criteria

Initialization Packet Scope and Use Rules conform to AG-SPEC-0001 when:

- agents receive explicit startup context before governed work;
- agent identity is known or traceable;
- role assignment is explicit;
- task scope is bounded;
- permission boundaries are explicit;
- privacy boundaries are preserved;
- authority boundaries are preserved;
- validation expectations are known;
- Source Material and provenance expectations are known;
- output handling is defined;
- review requirements are defined;
- escalation conditions are defined;
- stop conditions are defined;
- packet reuse does not silently expand scope;
- packet format remains implementation-independent;
- packet instructions do not override higher-authority standards;
- agent output remains distinguishable from governed approval, authority, privacy clearance, validation acceptance, publication permission, export permission, migration permission, deletion permission, or downstream-use clearance.

Initialization Packet Scope and Use Rules are successful when agents can begin useful work without creating hidden authority, hidden permission, hidden privacy exposure, hidden validation approval, hidden workflow approval, hidden storage meaning, hidden implementation dependence, or hidden governance.

## 4. Required Agent Identity Fields

Required Agent Identity Fields define the minimum identity information that an Agent Initialization Packet MUST include or support before an agent performs governed work inside The Brain Standard.

Agent identity exists so that future humans, agents, workflows, validators, storage systems, implementations, import processes, export processes, migration processes, publication processes, and governance processes can determine who or what performed agent activity, what role was assigned, what task was performed, what scope applied, what permissions applied, what output was produced, and what review state applies.

An Agent Initialization Packet MUST identify the agent clearly enough to distinguish the agent from:

- a human reviewer;
- another agent;
- a subagent;
- a workflow;
- a validator;
- an implementation;
- a script;
- a tool;
- a model provider;
- a storage system;
- a prior agent run;
- a future agent run;
- an uninitialized automation.

Agent Identity MUST remain distinguishable from Object Identity.

Agent Identity identifies the actor or automated participant.

Object Identity identifies the Knowledge Object.

An agent MUST NOT create, replace, merge, split, redirect, supersede, or reinterpret Object Identity merely because the agent has been assigned an identity.

Agent Identity MUST remain distinguishable from Role Assignment.

Agent Identity identifies who or what is operating.

Role Assignment identifies what function the agent is performing.

A single agent MAY perform different roles at different times only when each role assignment is explicit, scoped, and traceable.

A single role MAY be performed by different agents only when each agent identity remains explicit and traceable.

Agent Identity MUST remain distinguishable from Permission Boundary.

Agent Identity identifies the agent.

Permission Boundary defines what the agent may do.

Identifying an agent does not grant permission by itself.

### 4.1 Required Identity Field Categories

An Agent Initialization Packet SHALL include or support the following identity field categories where applicable:

- Agent Name or Identifier;
- Agent Type;
- Agent Role Reference;
- Agent Instance or Run Identifier;
- Agent Operator or Requesting Human where applicable;
- Agent Runtime or Implementation Context where applicable;
- Model, Tool, Script, or Automation Reference where applicable;
- Initialization Date or Time where applicable;
- Packet Version or Packet Reference;
- Assigned Task Reference;
- Activity Record Reference where applicable;
- Review Contact or Escalation Contact where applicable.

These categories define the minimum identity context required for traceable operation.

A future specification MAY define exact field names, exact syntax, exact allowed values, exact identifier formats, exact packet serialization, exact logging format, or exact implementation-specific mappings.

Such specifications are valid only when they preserve the identity behavior defined by AG-SPEC-0001 and higher-authority standards.

### 4.2 Agent Name or Identifier

An Agent Initialization Packet MUST include or support an Agent Name or Identifier.

The Agent Name or Identifier SHOULD allow a reviewer to determine which agent, subagent, automation, script, model-assisted process, or implementation-specific agent profile was initialized.

The Agent Name or Identifier MAY be human-readable.

The Agent Name or Identifier MAY include an implementation-specific identifier where useful.

An implementation-specific identifier MUST NOT become the standard identity of the agent unless a governed specification explicitly defines that role.

Where an agent is temporary, experimental, manually invoked, or one-time-use, the packet SHOULD still identify the agent clearly enough for review, traceability, and escalation.

### 4.3 Agent Type

An Agent Initialization Packet SHOULD identify the Agent Type.

Agent Type MAY describe whether the agent is:

- a general assistant;
- a subagent;
- a validator;
- a workflow participant;
- a script;
- a tool-using assistant;
- a model-assisted process;
- an implementation-specific agent profile;
- a future governed agent type.

Agent Type helps reviewers understand the broad operating category of the agent.

Agent Type does not define permission by itself.

A validator-type agent does not automatically receive authority to approve validation results.

A workflow-participant agent does not automatically receive authority to approve workflow outputs.

A tool-using assistant does not automatically receive permission to use every available tool.

A script does not automatically receive permission to modify, move, export, publish, migrate, or delete governed material.

### 4.4 Agent Role Reference

An Agent Initialization Packet MUST identify the assigned role or state that role assignment is unresolved.

The Agent Role Reference SHOULD connect the initialized agent to a governed role, responsibility, workflow function, task category, or subagent profile.

Where the role is unresolved, ambiguous, conflicting, or not yet governed, the agent SHOULD limit activity to low-risk inspection, clarification, or escalation.

The Agent Role Reference MUST NOT silently create a new role with new authority.

New recurring roles SHOULD be defined or reviewed through AG-SPEC-0002 or another governed agent specification.

### 4.5 Agent Instance or Run Identifier

An Agent Initialization Packet SHOULD include or support an Agent Instance or Run Identifier where traceability requires distinguishing one execution, task session, workflow participation, validation pass, ingestion pass, review pass, maintenance pass, export-preparation pass, migration-preparation pass, or publication-preparation pass from another.

The Agent Instance or Run Identifier SHOULD help determine:

- when the agent was initialized;
- what task the agent performed;
- what packet version applied;
- what inputs were used;
- what outputs were produced;
- what review state applies;
- whether the run was completed, paused, stopped, escalated, rejected, repaired, superseded, or archived.

Where implementation systems automatically generate run identifiers, those identifiers MAY be recorded.

Automatically generated identifiers MUST remain distinguishable from governed Object Identity, Source Identifiers, Knowledge Record identifiers, workflow identifiers, and validation identifiers unless a governed specification defines the mapping.

### 4.6 Operator or Requesting Human

An Agent Initialization Packet SHOULD identify the operator, requesting human, reviewer, owner, or responsible party where that information affects reviewability, accountability, escalation, privacy handling, authority handling, validation, publication, export, migration, deletion, or downstream use.

The operator or requesting human MAY be omitted where the agent activity is low-risk, routine, non-sensitive, or governed by another traceable workflow record.

Where a human request gives the agent task direction, the packet SHOULD preserve enough context to determine the instruction that initiated the work.

The operator or requesting human does not become the approving authority merely because they requested agent activity unless a governed workflow or authority rule grants that approval role.

### 4.7 Runtime, Tool, Model, or Implementation Reference

An Agent Initialization Packet MAY identify the runtime, tool, model, script, automation framework, plugin, interface, repository, vault, or implementation environment used by the agent.

This information SHOULD be included where it affects:

- permission boundaries;
- tool capabilities;
- privacy exposure;
- source access;
- storage access;
- validation behavior;
- output format;
- reproducibility;
- auditability;
- error review;
- compatibility;
- migration;
- import;
- export;
- publication;
- downstream use.

Runtime, tool, model, or implementation references are operational context.

They do not define the standard.

A specific model, prompt, tool, plugin, vault, repository, script, interface, or automation framework MUST NOT become required by AG-SPEC-0001.

### 4.8 Packet Version or Packet Reference

An Agent Initialization Packet SHOULD identify the packet version, packet date, packet reference, or packet source used to initialize the agent.

Packet versioning helps reviewers determine which rules, fields, permissions, escalation requirements, and stop conditions applied when the agent acted.

Where packet content changes materially, prior agent activity SHOULD remain traceable to the packet version used at the time of operation.

A revised packet MUST NOT retroactively authorize prior agent activity unless a governed review determines that the prior activity remains valid within the revised scope.

### 4.9 Agent Identity Success Criteria

Agent Identity Fields conform to AG-SPEC-0001 when:

- the initialized agent is identifiable;
- the agent role is identified or marked unresolved;
- the agent instance or run is traceable where needed;
- the operator or requesting human is identified where needed;
- the runtime, tool, model, or implementation context is identified where it affects reviewability or risk;
- the packet version or packet reference is identifiable;
- agent identity remains distinguishable from Object Identity;
- agent identity remains distinguishable from role assignment;
- agent identity remains distinguishable from permission;
- agent identity remains distinguishable from approval;
- agent identity remains distinguishable from authority;
- agent identity remains distinguishable from privacy clearance;
- agent identity remains distinguishable from validation acceptance.

Agent Identity Fields are successful when future review can determine who or what acted without allowing agent identity, implementation identity, tool identity, model identity, script identity, or runtime identity to become governed meaning, approval, authority, privacy clearance, validation acceptance, publication permission, export permission, migration permission, deletion permission, or downstream-use clearance.

## 5. Required Operating Context

Required Operating Context defines the minimum contextual information an Agent Initialization Packet MUST include or support so that an agent can operate within the correct project, task, workflow, storage area, source set, review state, implementation environment, and governed boundary.

Operating Context exists so that an agent does not treat general access, search results, memory, tool capability, folder visibility, repository visibility, chat context, workflow convenience, implementation defaults, or prior activity as permission to operate broadly.

An Agent Initialization Packet MUST define or support enough Operating Context for the agent to determine:

- what project it is operating inside;
- what task it has been assigned;
- what workflow stage applies where applicable;
- what material is in scope;
- what material is out of scope;
- what storage area applies where applicable;
- what source set applies where applicable;
- what review state applies where applicable;
- what implementation environment applies where applicable;
- what output destination applies where applicable;
- what governing standards apply;
- what uncertainty requires escalation.

Operating Context MUST remain distinguishable from Permission Boundary.

Operating Context describes where and why the agent is operating.

Permission Boundary describes what the agent may do.

Operating inside a context does not automatically authorize every possible operation inside that context.

Operating Context MUST remain distinguishable from Storage Location.

A storage location may help define practical scope.

A storage location does not define governed meaning by itself.

Operating Context MUST remain distinguishable from Workflow State.

Workflow State describes where material is in a workflow.

Operating Context describes the agent’s bounded work environment.

An agent may operate in a workflow context without receiving authority to approve workflow outputs.

### 5.1 Project Context

An Agent Initialization Packet MUST identify that the agent is operating inside The Brain or a compliant environment governed by The Brain Standard.

The packet SHOULD identify the relevant project, vault, repository, storage environment, workspace, implementation profile, or deployment context where practical.

Project Context helps prevent an agent from applying unrelated rules, external assumptions, implementation defaults, or generic knowledge-management behavior where The Brain Standard controls.

A packet MUST NOT allow the project context to be replaced by a tool context.

Operating in Obsidian, Codex, GitHub, a local file system, a chat interface, a script, a database, or a future implementation does not make that implementation the standard.

### 5.2 Task Context

An Agent Initialization Packet MUST identify the assigned task or task category.

Task Context SHOULD state what the agent is being asked to do.

Task Context MAY include:

- inspect;
- summarize;
- classify;
- extract;
- propose metadata;
- propose relationships;
- propose Source References;
- propose provenance notes;
- validate;
- draft;
- review support;
- repair recommendation;
- route recommendation;
- maintenance support;
- ingestion support;
- export-preparation support;
- migration-preparation support;
- publication-preparation support;
- implementation-support work;
- another governed task category.

Task Context MUST be narrow enough to prevent unintended expansion.

A task to inspect a file does not authorize rewriting it.

A task to draft a Knowledge Record does not authorize approval.

A task to validate a record does not authorize lifecycle transition.

A task to prepare an export does not authorize release.

A task to identify duplicates does not authorize merge.

A task to recommend deletion does not authorize deletion.

### 5.3 Material Scope

An Agent Initialization Packet MUST identify or support identification of the material in scope.

Material Scope MAY include:

- specific Source Material;
- specific Knowledge Records;
- specific governed documents;
- specific folders or storage areas;
- specific review packages;
- specific ingestion candidates;
- specific validation candidates;
- specific workflow outputs;
- specific agent outputs;
- specific import packages;
- specific export packages;
- specific migration packages;
- specific implementation-support files;
- another bounded material set.

Material Scope SHOULD also identify material that is out of scope where ambiguity is likely.

An agent MUST NOT treat search access, repository access, vault access, folder access, chat history, prompt context, model memory, generated cache, index result, or implementation visibility as unlimited material scope.

### 5.4 Workflow Context

An Agent Initialization Packet SHOULD identify the workflow context where the agent is operating within a governed workflow.

Workflow Context MAY include:

- ingestion;
- review and approval;
- maintenance and update;
- publication preparation;
- export preparation;
- migration preparation;
- downstream-use evaluation;
- validation support;
- implementation setup;
- another governed workflow context.

Workflow Context SHOULD identify the current workflow stage where the stage affects permissions, output handling, review requirements, escalation, lifecycle state, authority handling, privacy handling, validation, publication, export, migration, deletion, or downstream use.

Workflow Context MUST NOT become approval by itself.

Workflow completion MUST NOT become approval unless a governed workflow explicitly defines that result within a limited scope.

### 5.5 Storage Context

An Agent Initialization Packet SHOULD identify the relevant storage context where storage access, storage routing, file placement, archival, import, export, migration, review, drafts, implementation support, indexes, caches, or generated files affect the task.

Storage Context MAY identify:

- source-material area;
- Knowledge Record area;
- governed-document area;
- draft area;
- review area;
- archive area;
- import area;
- export area;
- migration area;
- implementation-support area;
- agent-support area;
- workflow-support area;
- index or cache area;
- generated-file area;
- another governed storage area.

Storage Context MUST NOT define knowledge meaning by itself.

Storage Context MUST NOT silently change Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, publication permission, export permission, migration permission, deletion permission, or downstream-use permission.

### 5.6 Source Context

An Agent Initialization Packet SHOULD identify Source Context where the agent is reading, summarizing, extracting, transforming, citing, proposing Source References, creating provenance notes, drafting Knowledge Records, validating source support, or reviewing source-derived knowledge.

Source Context MAY include:

- source file;
- source set;
- source identifier;
- source location;
- source availability;
- source privacy classification;
- source reliability notes;
- source authority notes;
- extraction scope;
- transformation scope;
- provenance expectation;
- citation or reference expectation;
- known source limitations.

Source Context MUST preserve the distinction between Source Material and Knowledge Records.

An agent MUST NOT treat Source Material as an approved Knowledge Record merely because it has been read, summarized, extracted, indexed, copied, staged, or placed in a workflow.

### 5.7 Review Context

An Agent Initialization Packet SHOULD identify Review Context where agent output may require human review, validation review, privacy review, authority review, source review, relationship review, lifecycle review, workflow review, publication review, export review, migration review, deletion review, or downstream-use review.

Review Context SHOULD identify:

- whether the output is draft, proposed, validated, flagged, escalated, or ready for review;
- who or what should review the output where applicable;
- what review standard or workflow applies;
- what output must not be treated as final;
- what conditions prevent approval;
- what escalation path applies.

Review Context MUST NOT be confused with approval.

A review-ready output is not approved merely because it is ready for review.

### 5.8 Implementation Context

An Agent Initialization Packet MAY identify Implementation Context where the agent operates through a specific software tool, model provider, vault, repository, file system, interface, plugin, script, runtime, workflow environment, or automation framework.

Implementation Context SHOULD be included where implementation behavior affects:

- file access;
- tool access;
- privacy exposure;
- indexing;
- caching;
- generated outputs;
- logging;
- synchronization;
- export;
- migration;
- publication;
- validation;
- display;
- review routing;
- error handling;
- reproducibility.

Implementation Context MUST remain subordinate to The Brain Standard.

An implementation may realize the standard.

An implementation does not define the standard.

### 5.9 Operating Context Success Criteria

Operating Context conforms to AG-SPEC-0001 when:

- project context is identified;
- task context is identified;
- material scope is bounded;
- workflow context is identified where applicable;
- storage context is identified where applicable;
- source context is identified where applicable;
- review context is identified where applicable;
- implementation context is identified where applicable;
- in-scope and out-of-scope material are distinguishable where needed;
- operating context does not silently expand permission;
- operating context does not replace governed meaning;
- operating context remains implementation-independent.

Operating Context is successful when an agent can determine where it is operating, what it is working on, why it is working, what standards apply, what material is in scope, what material is out of scope, and when uncertainty requires escalation, without allowing context, visibility, storage location, workflow state, tool capability, implementation behavior, or prior memory to become permission, authority, approval, privacy clearance, validation acceptance, publication permission, export permission, migration permission, deletion permission, or downstream-use clearance.

## 6. Required Authority and Permission Boundaries

Required Authority and Permission Boundaries define the limits that an Agent Initialization Packet MUST place on agent action before governed work begins.

Authority and Permission Boundaries exist so that agents can assist with knowledge work without becoming unreviewable authorities over knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, workflow behavior, publication, export, migration, deletion, downstream use, or governance.

An Agent Initialization Packet MUST identify or support identification of:

- allowed operations;
- prohibited operations;
- conditional operations;
- required review points;
- required escalation points;
- authority limits;
- privacy limits;
- validation limits;
- workflow limits;
- storage limits;
- implementation limits;
- destructive-action limits;
- downstream-use limits.

Permission Boundary and Authority Boundary MUST remain distinguishable.

Permission Boundary defines what an agent may do.

Authority Boundary defines what an agent may decide or finalize.

An agent may have permission to draft without authority to approve.

An agent may have permission to validate without authority to accept validation as final approval.

An agent may have permission to classify without authority to assign final Authority Level or final Privacy Classification.

An agent may have permission to prepare an export without authority to release it.

### 6.1 Allowed Operations

An Agent Initialization Packet SHALL identify the operations the agent is allowed to perform within the assigned scope.

Allowed operations MAY include:

- read;
- inspect;
- search;
- summarize;
- extract;
- classify;
- propose metadata;
- propose relationships;
- propose Source References;
- propose provenance notes;
- propose lifecycle states;
- propose authority notes;
- propose privacy classifications;
- perform validation checks;
- draft Knowledge Records;
- draft governed documents;
- prepare review reports;
- recommend repairs;
- recommend routing;
- recommend file movement;
- prepare implementation-support outputs;
- perform another explicitly authorized operation.

Allowed operations MUST be interpreted within the assigned task, material scope, workflow context, storage context, privacy boundary, authority boundary, validation expectation, and review requirement.

An allowed operation does not authorize broader operations by implication.

### 6.2 Prohibited Operations

An Agent Initialization Packet SHALL identify or preserve prohibited operations.

Unless explicitly permitted by a higher-authority governed workflow or specification within a defined scope, an agent MUST NOT:

- approve Knowledge Records;
- assign final Authority Level;
- assign final Privacy Classification;
- perform final lifecycle transitions;
- create final approved relationships;
- create final approved Source References;
- accept validation as final approval;
- publish governed material;
- export governed material;
- migrate governed material;
- delete governed material;
- permanently remove Source Material;
- merge Knowledge Objects;
- split Knowledge Objects;
- replace Object Identity;
- supersede governed entities;
- deprecate governed entities;
- clear governed entities for downstream use;
- override privacy boundaries;
- override authority boundaries;
- override review requirements;
- override validation requirements;
- override governance requirements.

A packet MAY include stricter prohibited operations for a specific agent, task, role, workflow, privacy class, authority class, implementation context, or deployment context.

### 6.3 Conditional Operations

An Agent Initialization Packet MAY define conditional operations.

Conditional operations are actions an agent MAY perform only when required conditions are satisfied.

Conditional operations MAY include:

- write operations requiring review;
- file movement requiring storage approval;
- export preparation requiring privacy review;
- migration preparation requiring compatibility review;
- publication preparation requiring authority and privacy review;
- validation output requiring human review;
- metadata update requiring provenance;
- relationship proposal requiring source support;
- Source Reference proposal requiring source availability;
- lifecycle proposal requiring workflow review;
- deletion recommendation requiring human approval;
- quarantine recommendation requiring escalation.

Conditional operations MUST identify the condition that must be satisfied before the operation proceeds.

Where the condition is not satisfied, the agent MUST stop, limit activity, or escalate.

### 6.4 Read Permission Boundary

An Agent Initialization Packet SHOULD define the read permission boundary where the agent may inspect, search, parse, summarize, extract from, classify, index, or otherwise consume governed material.

Read permission MUST respect Privacy Classification.

Read permission MUST respect material scope.

Read permission MUST respect workflow context.

Read permission MUST respect implementation exposure limits.

Read permission MUST NOT be inferred from visibility alone.

An agent MUST NOT expose restricted material through summaries, prompts, logs, embeddings, indexes, caches, generated files, exported files, review reports, or downstream outputs unless the relevant Privacy Classification, permission boundary, and governed workflow allow that exposure.

### 6.5 Write Permission Boundary

An Agent Initialization Packet SHOULD define the write permission boundary where the agent may create, edit, annotate, restructure, enrich, draft, or record governed material.

Write permission MUST identify whether the agent may:

- create drafts;
- edit drafts;
- propose edits to approved material;
- create validation reports;
- create review reports;
- create activity records;
- create metadata proposals;
- create relationship proposals;
- create Source Reference proposals;
- create provenance notes;
- create implementation-support files;
- perform another authorized write action.

Write permission MUST NOT be treated as approval permission.

Agent-written material SHOULD remain distinguishable from reviewed, approved, authoritative, published, exportable, migrated, or downstream-cleared material unless accepted through a governed process.

### 6.6 Move Permission Boundary

An Agent Initialization Packet SHOULD define whether the agent may recommend or perform movement of stored material.

Move permission MAY apply to:

- drafts;
- review files;
- Source Material;
- Knowledge Records;
- governed documents;
- workflow outputs;
- agent outputs;
- import files;
- export files;
- migration files;
- archive files;
- implementation-support files;
- generated files;
- another stored representation.

Move permission MUST preserve Object Identity, Source References, provenance, lifecycle state, Authority Level, Privacy Classification, Validation, workflow state, review state, and storage-layout meaning.

An agent MUST NOT treat movement as approval, rejection, archival, publication, export, migration, deletion, or downstream-use clearance unless a governed workflow explicitly defines that result.

### 6.7 Destructive-Action Boundary

An Agent Initialization Packet MUST define destructive-action limits where the task involves deletion, overwriting, replacement, purging, permanent removal, irreversible movement, identity change, merge, split, supersession, deprecation, publication, export, migration, or privacy exposure.

Destructive actions SHOULD require human review unless a future governed workflow or specification explicitly permits a narrow automated action with traceability, reviewability, recovery support, and privacy protection.

An agent MUST NOT perform destructive action merely because it has tool capability.

Tool capability is not governance.

Write access is not deletion permission.

Repository access is not migration permission.

Storage access is not publication permission.

Visibility is not export permission.

### 6.8 Authority Boundary

An Agent Initialization Packet MUST define the agent’s Authority Boundary where the task affects interpretation, approval, lifecycle state, Authority Level, Privacy Classification, Validation, Source References, provenance, relationships, publication, export, migration, deletion, downstream use, or governance.

The default Authority Boundary is proposal-only unless a higher-authority governed workflow or specification explicitly grants limited authority.

An agent MAY recommend.

An agent MAY classify.

An agent MAY validate.

An agent MAY draft.

An agent MAY identify risk.

An agent MAY escalate.

An agent MUST NOT become the final authority unless explicitly permitted by a governed workflow or specification within a defined scope.

Agent confidence MUST NOT be treated as Authority Level.

Agent output MUST NOT become authoritative merely because it is plausible, repeated, generated by a preferred model, produced by a workflow, validated by a tool, surfaced by an implementation, or accepted by habit.

### 6.9 Permission and Authority Success Criteria

Authority and Permission Boundaries conform to AG-SPEC-0001 when:

- allowed operations are explicit;
- prohibited operations are preserved;
- conditional operations identify required conditions;
- read boundaries are defined where needed;
- write boundaries are defined where needed;
- move boundaries are defined where needed;
- destructive-action boundaries are defined where needed;
- authority boundaries are explicit;
- permission is not confused with authority;
- access is not confused with permission;
- visibility is not confused with permission;
- tool capability is not confused with governance;
- workflow participation is not confused with approval;
- validation is not confused with approval;
- agent confidence is not confused with Authority Level;
- agent output is not confused with approved governed material.

Authority and Permission Boundaries are successful when an agent can perform useful work within a defined scope while preserving human reviewability, traceability, privacy protection, validation boundaries, authority boundaries, workflow boundaries, storage boundaries, implementation independence, and governance.

## 7. Required Role Assignment

Required Role Assignment defines how an Agent Initialization Packet MUST identify the role an agent is performing before governed work begins.

Role Assignment exists so that an agent does not operate as a general-purpose authority, undefined assistant, unrestricted automation, hidden reviewer, unbounded validator, or implementation-controlled actor.

An Agent Initialization Packet MUST assign the agent to a role, responsibility, workflow function, task category, or governed subagent profile before the agent performs governed work.

Where the role is not yet known, not yet governed, ambiguous, conflicting, or outside the agent’s current permission scope, the Initialization Packet MUST mark the role as unresolved and limit the agent to clarification, low-risk inspection, or escalation.

Role Assignment MUST remain distinguishable from Agent Identity.

Agent Identity identifies who or what is operating.

Role Assignment identifies what function the agent is performing.

Role Assignment MUST remain distinguishable from Permission Boundary.

Role Assignment identifies the agent’s function.

Permission Boundary identifies what the agent may do within that function.

A role does not grant unrestricted permission by itself.

Role Assignment MUST remain distinguishable from Authority Level.

Role Assignment defines task responsibility.

Authority Level defines governance weight, interpretive authority, review weight, trust boundary, or use-authority.

An agent assigned to a review-support role does not automatically become an approving authority.

An agent assigned to a validation role does not automatically become the authority that accepts validation as final approval.

An agent assigned to a privacy-support role does not automatically assign final Privacy Classification.

An agent assigned to a metadata role does not automatically approve metadata.

An agent assigned to a relationship role does not automatically approve relationships.

### 7.1 Required Role Identification

An Agent Initialization Packet SHALL identify the assigned role clearly enough for future review.

Role identification SHOULD include or support:

- role name;
- role purpose;
- role scope;
- role source or governing document where applicable;
- assigned task category;
- allowed outputs;
- prohibited outputs;
- review requirements;
- escalation requirements;
- stop conditions;
- relationship to other agents or subagents where applicable.

A role MAY be general or specialized.

A general role MAY support broad inspection, summarization, drafting, or review support when the permission boundary remains narrow and explicit.

A specialized role MAY support a specific function such as syntax inspection, standards validation, metadata proposal, relationship proposal, source-reference review, privacy-risk detection, duplicate detection, workflow routing, implementation support, or handoff preparation.

### 7.2 Role Source

An Agent Initialization Packet SHOULD identify the source of the assigned role where practical.

The role source MAY be:

- AG-0002 — Agent Role and Responsibility Standard;
- AG-SPEC-0002 — Subagent Prompt and Role Profile Specification;
- a workflow standard;
- a workflow specification;
- an implementation profile;
- an operational guide;
- a human assignment;
- a task-specific packet;
- another governed role source.

A role assigned by a human MAY be valid for a single task when it remains consistent with higher-authority standards and the packet defines permission boundaries, review requirements, escalation requirements, and stop conditions.

A recurring role SHOULD be defined in AG-SPEC-0002 or another governed agent specification.

An informal role name MUST NOT silently become a governed role by repetition, convenience, prompt reuse, implementation defaults, workflow defaults, or agent memory.

### 7.3 Role Scope

An Agent Initialization Packet MUST define or support the Role Scope.

Role Scope describes where the assigned role applies.

Role Scope MAY include:

- one file;
- one Source Material item;
- one Knowledge Record;
- one governed document;
- one folder or storage area;
- one workflow stage;
- one validation pass;
- one review package;
- one import package;
- one export package;
- one migration package;
- one implementation-support task;
- one recurring task type;
- another bounded scope.

Role Scope MUST NOT silently expand beyond the assigned task.

A Metadata Agent assigned to one Knowledge Record does not become a Metadata Agent for the whole repository.

A Privacy Agent assigned to detect risk does not become the final privacy authority.

A Workflow Agent assigned to route a draft does not become an approval authority.

A Relationship Agent assigned to propose relationships does not become authorized to approve relationships.

### 7.4 Role Responsibility

An Agent Initialization Packet SHOULD identify the responsibility of the assigned role.

Role Responsibility describes what the agent is expected to produce or support.

Role Responsibility MAY include:

- inspecting text;
- checking syntax;
- identifying missing metadata;
- proposing metadata;
- proposing relationships;
- checking Source References;
- preserving provenance;
- detecting privacy risk;
- detecting authority risk;
- checking validation issues;
- drafting Knowledge Records;
- preparing review notes;
- routing workflow outputs;
- recommending repair;
- preparing handoff summaries;
- supporting implementation setup;
- another governed responsibility.

Role Responsibility MUST remain bounded by the packet’s permission and authority limits.

Responsibility to detect an issue does not authorize correction unless write permission is granted.

Responsibility to recommend repair does not authorize applying the repair unless write permission is granted.

Responsibility to prepare review notes does not authorize approval.

Responsibility to support implementation setup does not authorize changing the standard.

### 7.5 Role Output

An Agent Initialization Packet MUST identify or support identification of the expected Role Output.

Role Output MAY include:

- summary;
- classification;
- extraction;
- metadata proposal;
- relationship proposal;
- Source Reference proposal;
- provenance note;
- lifecycle-state proposal;
- authority note;
- privacy-classification proposal;
- validation report;
- draft Knowledge Record;
- draft governed document;
- review note;
- repair recommendation;
- routing recommendation;
- escalation note;
- handoff summary;
- implementation-support note;
- another governed output.

Role Output MUST remain distinguishable from approved governed material unless accepted through a governed review or workflow process.

Role Output MUST identify whether it is draft, proposed, reviewed, escalated, rejected, repaired, approved, or governed by another applicable lifecycle or review state.

### 7.6 Role Conflict

An Agent Initialization Packet MUST require escalation where the assigned role conflicts with:

- higher-authority standards;
- permission boundaries;
- authority boundaries;
- privacy boundaries;
- validation expectations;
- workflow requirements;
- Source Reference requirements;
- provenance requirements;
- storage boundaries;
- implementation boundaries;
- user instructions;
- another agent role;
- another active workflow;
- governance requirements.

Where role conflict exists, the agent SHOULD stop or limit activity to safe clarification and escalation.

An agent MUST NOT resolve role conflict by choosing the most convenient instruction, broadest permission, preferred implementation behavior, model confidence, tool capability, or prior memory.

### 7.7 Multi-Role Assignment

An Agent Initialization Packet MAY assign more than one role to an agent only when each role is explicit, scoped, and compatible.

Where an agent receives multiple roles, the packet SHOULD identify:

- each role;
- each role scope;
- each role output;
- each permission boundary;
- each authority boundary;
- each review requirement;
- each escalation condition;
- any role priority or sequencing rule.

Multi-role assignment MUST NOT create hidden permission expansion.

An agent assigned to inspect syntax and propose metadata does not automatically receive permission to approve the file.

An agent assigned to validate and route does not automatically receive permission to approve, export, publish, migrate, or delete.

If role responsibilities conflict, the stricter boundary SHOULD apply unless a higher-authority governed process resolves the conflict.

### 7.8 Role Assignment Success Criteria

Role Assignment conforms to AG-SPEC-0001 when:

- the agent role is explicit or marked unresolved;
- the role source is identified where practical;
- the role scope is bounded;
- the role responsibility is stated;
- the expected output is identified;
- role output remains distinguishable from approval;
- role assignment does not grant unrestricted permission;
- role assignment does not create final authority;
- role conflict triggers escalation;
- multi-role assignment remains explicit and bounded;
- recurring roles are routed toward governed specification where needed.

Role Assignment is successful when future review can determine what function the agent was performing, what output it was expected to produce, what limits applied, and whether the agent remained inside its assigned role.

## 8. Required Source, Privacy, and Validation Awareness

Required Source, Privacy, and Validation Awareness defines what an Agent Initialization Packet MUST make clear before an agent handles Source Material, source-derived knowledge, privacy-relevant material, validation-sensitive material, or output that may affect review, authority, publication, export, migration, deletion, or downstream use.

Source, Privacy, and Validation Awareness exists so that agents do not confuse source access with source authority, privacy visibility with privacy clearance, validation findings with approval, or agent confidence with governed truth.

An Agent Initialization Packet MUST require the agent to preserve the distinction between:

- Source Material and Knowledge Records;
- extracted content and governed knowledge;
- source support and approval;
- provenance and authority;
- privacy visibility and privacy permission;
- validation result and approval;
- agent confidence and Authority Level;
- workflow completion and downstream-use clearance.

Source Awareness, Privacy Awareness, and Validation Awareness MAY be handled as separate packet fields or as a combined awareness block.

The packet format may vary by implementation.

The meaning of these awareness requirements MUST remain governed, explicit, reviewable, traceable, and implementation-independent.

### 8.1 Source Awareness

An Agent Initialization Packet MUST require Source Awareness where the agent reads, summarizes, extracts, transforms, cites, references, classifies, drafts from, validates against, or creates output from Source Material.

Source Awareness SHOULD identify or support identification of:

- Source Material in scope;
- Source Material out of scope where needed;
- source location or reference where applicable;
- source availability where applicable;
- source privacy classification where applicable;
- source reliability notes where applicable;
- source authority notes where applicable;
- extraction scope where applicable;
- transformation scope where applicable;
- provenance expectation;
- Source Reference expectation;
- known source limitations;
- review requirement for source-derived output.

The agent MUST preserve the distinction between Source Material and Knowledge Records.

Source Material does not become governed knowledge merely because it is stored, staged, summarized, extracted, indexed, classified, copied, transformed, embedded, routed, or processed by an agent.

Source-derived output SHOULD remain proposed until reviewed through the applicable workflow.

### 8.2 Provenance Awareness

An Agent Initialization Packet MUST require Provenance Awareness where the agent creates, modifies, summarizes, extracts, transforms, validates, routes, or proposes governed output.

Provenance Awareness SHOULD identify what provenance must be preserved for:

- source use;
- extraction;
- transformation;
- agent participation;
- workflow participation;
- validation findings;
- review outputs;
- metadata proposals;
- relationship proposals;
- Source Reference proposals;
- lifecycle-state proposals;
- authority notes;
- privacy-classification proposals;
- repair recommendations;
- routing recommendations;
- publication-preparation outputs;
- export-preparation outputs;
- migration-preparation outputs.

An agent MUST NOT remove, hide, collapse, overwrite, or obscure provenance where provenance affects meaning, reviewability, authority, privacy, validation, Source References, relationships, lifecycle state, workflow behavior, publication, export, migration, deletion, downstream use, or governance.

Where provenance is missing, incomplete, unclear, contradictory, or unreliable, the agent SHOULD flag the issue and escalate where needed.

### 8.3 Privacy Awareness

An Agent Initialization Packet MUST require Privacy Awareness where the agent may access, summarize, extract, transform, classify, index, route, expose, export, publish, migrate, cache, embed, log, or otherwise process privacy-relevant material.

Privacy Awareness SHOULD identify or support identification of:

- applicable Privacy Classification;
- privacy scope;
- access limits;
- visibility limits;
- exposure limits;
- routing limits;
- indexing limits;
- synchronization limits;
- backup limits;
- export limits;
- publication limits;
- agent-access limits;
- workflow-access limits;
- implementation-access limits;
- downstream-use limits;
- escalation conditions.

Privacy Awareness MUST apply even when the material is technically visible to the agent.

Visibility is not permission.

Search access is not privacy clearance.

Repository access is not export permission.

Tool access is not publication permission.

Model context is not downstream-use clearance.

An agent MUST NOT expose privacy-relevant material beyond the initialized scope unless permitted by the applicable Privacy Classification, workflow, permission boundary, and review process.

### 8.4 Validation Awareness

An Agent Initialization Packet MUST require Validation Awareness where the agent performs validation checks, reads validation results, proposes validation findings, creates validation reports, routes validation issues, or relies on validation state.

Validation Awareness SHOULD identify or support identification of:

- validation scope;
- applicable standard or specification;
- validation target;
- validation method where applicable;
- validation output format where applicable;
- validation evidence where applicable;
- validation warnings;
- validation errors;
- unresolved validation issues;
- review requirement;
- escalation condition;
- limits on validation authority.

Validation Awareness MUST preserve the distinction between validation and approval.

A validation-passing output is not automatically approved.

A validation report is not automatically an approval record.

A validation agent is not automatically an approving authority.

A validation tool is not governance.

A validation result MUST NOT be treated as Authority Level, Privacy Classification, Lifecycle State approval, publication permission, export permission, migration permission, deletion permission, or downstream-use clearance unless a governed workflow or specification explicitly defines that behavior within a limited scope.

### 8.5 Authority Awareness

An Agent Initialization Packet SHOULD require Authority Awareness where the agent handles material that affects interpretation, trust, review weight, use-authority, governance weight, publication, export, migration, deletion, or downstream use.

Authority Awareness SHOULD identify or support identification of:

- applicable Authority Level;
- authority scope;
- authority limits;
- authority source where applicable;
- authority review requirement;
- authority-related risks;
- downstream-use limits;
- conditions that require escalation.

Authority Awareness MUST preserve the distinction between agent confidence and Authority Level.

Agent confidence may help review.

Agent confidence does not define authority.

A plausible agent output, repeated agent output, preferred-model output, tool-validated output, workflow-generated output, or implementation-surfaced output MUST NOT become authoritative unless accepted through a governed process.

### 8.6 Lifecycle Awareness

An Agent Initialization Packet SHOULD require Lifecycle Awareness where the agent handles material whose lifecycle state affects review, approval, rejection, deprecation, supersession, archival, restriction, quarantine, repair, validation, authority, privacy, publication, export, migration, deletion, or downstream use.

Lifecycle Awareness SHOULD identify or support identification of:

- current lifecycle state where applicable;
- proposed lifecycle state where applicable;
- lifecycle transition limits;
- lifecycle review requirement;
- lifecycle-related risks;
- repair or quarantine conditions;
- escalation conditions.

Lifecycle Awareness MUST preserve the distinction between lifecycle state and workflow state.

A workflow step does not automatically change lifecycle state.

A lifecycle-state proposal does not become a final lifecycle transition unless accepted through a governed workflow.

An agent MUST NOT approve, reject, deprecate, supersede, archive, quarantine, or clear material for downstream use unless a higher-authority governed workflow or specification explicitly permits that action within a defined scope.

### 8.7 Relationship Awareness

An Agent Initialization Packet SHOULD require Relationship Awareness where the agent proposes, reviews, validates, routes, repairs, or relies on relationships.

Relationship Awareness SHOULD identify or support identification of:

- relationship participants;
- proposed relationship type;
- relationship direction where applicable;
- relationship context;
- relationship source support;
- relationship provenance;
- relationship confidence where applicable;
- relationship lifecycle state where applicable;
- relationship authority where applicable;
- relationship privacy where applicable;
- review requirement;
- escalation condition.

Relationship Awareness MUST preserve the distinction between relationship proposal and approved relationship.

An inferred relationship is not automatically approved.

A repeated relationship suggestion is not automatically authoritative.

A graph link, backlink, tag, folder placement, search result, or implementation-specific connection does not define a governed relationship by itself.

### 8.8 Awareness Conflict and Escalation

An Agent Initialization Packet MUST require escalation where Source Awareness, Privacy Awareness, Validation Awareness, Authority Awareness, Lifecycle Awareness, or Relationship Awareness reveals ambiguity, conflict, missing context, privacy risk, authority risk, validation failure, source-reference gap, provenance gap, relationship confusion, lifecycle confusion, implementation conflict, or downstream-use risk.

The agent SHOULD stop or limit activity where continuing could:

- expose restricted material;
- create unsupported source-derived knowledge;
- hide missing provenance;
- treat validation as approval;
- treat confidence as authority;
- treat visibility as permission;
- treat workflow completion as approval;
- treat storage placement as meaning;
- treat implementation behavior as the standard;
- publish without approval;
- export without approval;
- migrate without review;
- delete without approval;
- clear downstream use without governance.

Where awareness requirements conflict, the stricter boundary SHOULD apply until a human review or governed workflow resolves the conflict.

### 8.9 Source, Privacy, and Validation Awareness Success Criteria

Source, Privacy, and Validation Awareness conforms to AG-SPEC-0001 when:

- Source Material remains distinguishable from Knowledge Records;
- source-derived output remains traceable;
- provenance expectations are known;
- privacy boundaries are explicit where needed;
- visibility is not treated as permission;
- validation is not treated as approval;
- agent confidence is not treated as Authority Level;
- lifecycle state is not confused with workflow state;
- relationship proposals are not treated as approved relationships;
- missing source support is flagged;
- missing provenance is flagged;
- privacy risk triggers escalation;
- validation failure triggers escalation;
- authority risk triggers escalation;
- downstream-use risk triggers escalation.

Source, Privacy, and Validation Awareness is successful when an initialized agent can work with Source Material, privacy-relevant material, validation-sensitive material, and source-derived knowledge without creating source confusion, provenance loss, privacy exposure, validation confusion, authority confusion, lifecycle confusion, relationship confusion, publication risk, export risk, migration risk, deletion risk, downstream-use risk, implementation dependence, or governance drift.

## 9. Required Activity Recording and Traceability

Required Activity Recording and Traceability defines what an Agent Initialization Packet MUST require an agent to record or support so that agent activity remains inspectable, reviewable, correctable, auditable, and governable.

Activity Recording and Traceability exist so that future humans, agents, workflows, validators, storage systems, implementations, import processes, export processes, migration processes, publication processes, and governance processes can determine what an agent did, why it acted, what it used, what it produced, what boundaries applied, what review is needed, and whether repair or escalation is required.

An Agent Initialization Packet MUST require activity recording where agent activity affects:

- Knowledge Objects;
- Knowledge Records;
- Source Material;
- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage routing;
- workflow outputs;
- review outputs;
- publication preparation;
- export preparation;
- migration preparation;
- deletion recommendation;
- downstream use;
- governance.

Activity Recording MAY be minimal for low-risk read-only work.

Activity Recording MUST be stronger where agent activity affects governed meaning, privacy, authority, validation, lifecycle state, Source References, provenance, relationships, publication, export, migration, deletion, downstream use, or governance.

### 9.1 Activity Record Requirement

An Agent Initialization Packet MUST identify whether an Agent Activity Record is required.

Where required, the Activity Record SHOULD identify or support identification of:

- agent identity;
- agent role;
- packet reference;
- packet version where applicable;
- task;
- operating context;
- material scope;
- workflow context where applicable;
- storage context where applicable;
- source context where applicable;
- permission boundary;
- authority boundary;
- privacy boundary;
- validation scope;
- inputs used;
- outputs produced;
- actions performed;
- recommendations made;
- files or records affected;
- review requirement;
- escalation made;
- stop condition triggered;
- unresolved issues;
- timestamp or run reference where applicable.

The Activity Record MAY be created through TEMPLATE-0003 — Agent Activity Record Template, a workflow log, an implementation log, a task record, a review record, or another governed activity-recording method.

The recording method may vary by implementation.

The traceability meaning MUST remain explicit, portable, reviewable, and governed.

### 9.2 Input Traceability

An Agent Initialization Packet SHOULD require Input Traceability where the agent reads, summarizes, extracts, transforms, validates, classifies, drafts from, or proposes changes based on Source Material, Knowledge Records, governed documents, workflow outputs, agent outputs, implementation files, indexes, caches, imports, exports, migration packages, or other governed material.

Input Traceability SHOULD identify:

- what input was used;
- where the input came from;
- what source or record identifier applies where available;
- what version or state applied where available;
- what privacy boundary applied;
- what authority context applied;
- what validation context applied;
- what source limitations were known;
- what material was excluded where exclusion matters.

An agent MUST NOT obscure input sources where source support, provenance, privacy, authority, validation, relationships, lifecycle state, publication, export, migration, deletion, downstream use, or governance depends on knowing the input.

### 9.3 Output Traceability

An Agent Initialization Packet MUST require Output Traceability where the agent produces summaries, classifications, metadata proposals, relationship proposals, Source Reference proposals, provenance notes, validation findings, draft Knowledge Records, draft governed documents, review reports, routing recommendations, repair recommendations, export-preparation outputs, migration-preparation outputs, publication-preparation outputs, deletion recommendations, downstream-use notes, or other governed outputs.

Output Traceability SHOULD identify:

- what output was produced;
- what role produced it;
- what task produced it;
- what input supported it;
- what permission boundary applied;
- what authority boundary applied;
- what privacy boundary applied;
- what validation scope applied;
- whether the output is draft, proposed, reviewed, escalated, rejected, repaired, approved, archived, or governed by another lifecycle or review state;
- what review is required;
- what unresolved risks remain.

Agent output MUST remain distinguishable from approved governed material unless accepted through a governed review or workflow process.

### 9.4 Action Traceability

An Agent Initialization Packet SHOULD require Action Traceability where the agent performs actions that affect records, files, storage placement, metadata, relationships, Source References, provenance, lifecycle state, Authority Level, Privacy Classification, Validation, review routing, workflow routing, export preparation, migration preparation, publication preparation, deletion recommendation, or downstream-use evaluation.

Action Traceability SHOULD identify:

- what action was performed;
- when the action was performed where applicable;
- what material was affected;
- what permission allowed the action;
- what condition applied where applicable;
- what result occurred;
- whether the action was successful, partial, failed, stopped, escalated, or reversed;
- what review or repair is required.

An agent MUST NOT perform or obscure material actions in a way that prevents later review, correction, validation, rollback, repair, escalation, or governance review.

### 9.5 Decision and Recommendation Traceability

An Agent Initialization Packet SHOULD require traceability for agent decisions, recommendations, classifications, warnings, and proposed actions.

Decision and Recommendation Traceability SHOULD identify:

- what recommendation was made;
- what reasoning or source support was used where practical;
- what confidence or uncertainty applies where useful;
- what standard, workflow, or packet rule applies where known;
- whether the recommendation is proposed or final;
- what human review is required;
- what risk or ambiguity remains.

Agent recommendations MUST NOT be treated as final decisions unless a governed workflow or specification explicitly permits that result within a defined scope.

Agent confidence MUST NOT be treated as Authority Level.

A recommendation repeated by multiple agents MUST NOT become approval by repetition alone.

### 9.6 Escalation Traceability

An Agent Initialization Packet MUST require Escalation Traceability where the agent detects ambiguity, conflict, privacy risk, authority risk, validation failure, missing source support, missing provenance, relationship confusion, lifecycle confusion, destructive action, publication risk, export risk, migration risk, deletion risk, downstream-use risk, implementation conflict, or governance conflict.

Escalation Traceability SHOULD identify:

- what triggered escalation;
- what material was affected;
- what standard, workflow, or packet rule was involved where known;
- what risk was identified;
- what action was stopped or limited;
- what output was produced before escalation;
- what review is required;
- what decision is needed;
- whether quarantine, repair, rejection, archival, or other routing is recommended.

Escalation records SHOULD be clear enough for a human reviewer or governed workflow to continue without guessing what happened.

### 9.7 Stop-Condition Traceability

An Agent Initialization Packet MUST require Stop-Condition Traceability where a stop condition is triggered.

Stop-Condition Traceability SHOULD identify:

- what stop condition was triggered;
- why the agent stopped;
- what material was involved;
- what action was prevented;
- what risk or conflict applied;
- what standard, workflow, packet rule, privacy boundary, authority boundary, validation expectation, or governance requirement applied where known;
- what review or escalation is required.

An agent MUST NOT silently continue after a stop condition merely because the task is convenient, the tool allows it, the model is confident, the implementation exposes the material, or a prior similar action was completed.

### 9.8 Record Location and Preservation

An Agent Initialization Packet SHOULD identify where activity records, logs, review notes, validation outputs, escalation notes, or other traceability outputs should be stored or routed where practical.

Record location MAY be defined by:

- TEMPLATE-0003 — Agent Activity Record Template;
- TEMPLATE-0004 — Review Record Template;
- a workflow standard;
- a workflow specification;
- a storage layout;
- an implementation profile;
- a task packet;
- another governed method.

Record location MUST NOT define record meaning by itself.

A log entry, file location, folder placement, tag, implementation event, workflow state, or generated artifact does not become an approved activity record unless it preserves the required traceability meaning.

Traceability records SHOULD be preserved where needed for review, validation, repair, governance, privacy audit, authority review, publication review, export review, migration review, deletion review, downstream-use review, or future maintenance.

### 9.9 Activity Recording and Traceability Success Criteria

Activity Recording and Traceability conforms to AG-SPEC-0001 when:

- activity recording requirements are explicit;
- agent identity is traceable;
- role assignment is traceable;
- packet reference is traceable where needed;
- task context is traceable;
- input use is traceable where needed;
- output production is traceable;
- material actions are traceable;
- recommendations are traceable;
- escalation is traceable;
- stop conditions are traceable;
- review requirements are traceable;
- privacy-relevant activity is traceable;
- validation-relevant activity is traceable;
- authority-relevant activity is traceable;
- publication, export, migration, deletion, and downstream-use preparation are traceable where applicable;
- traceability does not depend only on hidden application state;
- traceability remains implementation-independent.

Activity Recording and Traceability is successful when future review can determine what an agent did, what it used, what it produced, what boundaries applied, what risks were found, what review is required, and whether the agent activity remains valid, limited, rejected, repairable, escalated, superseded, archived, or subject to governance.

## 10. Required Escalation and Stop Conditions

Required Escalation and Stop Conditions define when an Agent Initialization Packet MUST require an agent to pause, limit activity, refuse an action, route an issue to review, or stop work entirely.

Escalation and Stop Conditions exist so that agents do not continue operating when ambiguity, conflict, privacy risk, authority risk, validation failure, source uncertainty, provenance loss, destructive action, implementation behavior, workflow confusion, or governance conflict could damage The Brain Standard.

An Agent Initialization Packet MUST identify or preserve escalation and stop conditions before governed work begins.

Escalation means the agent routes the issue, risk, ambiguity, conflict, or prohibited condition to a human reviewer or governed workflow.

A stop condition means the agent must pause, refuse, avoid continuing, or limit work because proceeding may violate a standard, permission boundary, privacy boundary, authority boundary, validation expectation, workflow rule, source requirement, provenance requirement, storage boundary, implementation boundary, or governance requirement.

Escalation and Stop Conditions MUST remain distinguishable.

Escalation routes an issue for review.

A stop condition prevents the agent from continuing the affected action.

Some conditions may require both escalation and stopping.

### 10.1 Escalation Requirement

An Agent Initialization Packet SHALL identify when escalation is required.

Escalation SHOULD be required where the agent detects:

- unclear task scope;
- unclear agent role;
- unclear permission boundary;
- unclear authority boundary;
- unclear privacy boundary;
- unclear validation scope;
- unclear workflow state;
- unclear lifecycle state;
- unclear Source Material status;
- missing Source References;
- missing provenance;
- conflicting metadata;
- conflicting relationships;
- conflicting instructions;
- possible duplicate Knowledge Objects;
- destructive-action risk;
- publication risk;
- export risk;
- migration risk;
- deletion risk;
- downstream-use risk;
- implementation conflict;
- governance conflict.

An agent SHOULD escalate before taking action where the outcome may affect governed meaning, privacy, authority, validation, lifecycle state, Source References, provenance, relationships, publication, export, migration, deletion, downstream use, or governance.

### 10.2 Stop Condition Requirement

An Agent Initialization Packet SHALL identify when the agent must stop or refuse the affected action.

A stop condition MUST apply where proceeding would:

- violate a higher-authority standard;
- exceed the initialized scope;
- exceed the assigned role;
- exceed the permission boundary;
- exceed the authority boundary;
- violate a privacy boundary;
- treat validation as approval;
- treat agent confidence as Authority Level;
- treat Source Material as an approved Knowledge Record;
- treat storage location as governed meaning;
- treat workflow completion as approval;
- publish without approval;
- export without approval;
- migrate without review;
- delete without approval;
- remove or obscure provenance;
- overwrite governed material without permission;
- change Object Identity without governed authority;
- merge Knowledge Objects without governed authority;
- split Knowledge Objects without governed authority;
- supersede governed entities without governed authority;
- deprecate governed entities without governed authority;
- clear material for downstream use without governance;
- continue under a revoked, rejected, superseded, expired, invalid, or out-of-scope packet.

Where a stop condition applies, the agent MUST stop the affected action even if the tool allows the action, the model is confident, the instruction appears convenient, the implementation exposes the material, or a prior similar action was completed.

### 10.3 Privacy Escalation and Stop Conditions

An Agent Initialization Packet MUST require escalation where privacy classification, privacy scope, exposure limits, routing limits, indexing limits, synchronization limits, export limits, publication limits, agent-access limits, implementation-access limits, or downstream-use limits are unclear.

An agent MUST stop where continuing would expose privacy-relevant material beyond the initialized scope.

An agent MUST stop where restricted material may be disclosed through:

- summaries;
- prompts;
- logs;
- generated files;
- review reports;
- indexes;
- caches;
- embeddings;
- exports;
- publications;
- migrations;
- synchronization;
- downstream outputs;
- implementation-specific exposure.

Visibility is not permission.

Access is not privacy clearance.

Tool capability is not exposure permission.

### 10.4 Authority Escalation and Stop Conditions

An Agent Initialization Packet MUST require escalation where Authority Level, authority source, review weight, use-authority, approval status, publication readiness, export readiness, migration readiness, deletion authority, or downstream-use authority is unclear.

An agent MUST stop where continuing would create or imply final authority without a governed basis.

An agent MUST NOT treat the following as final authority:

- agent confidence;
- repeated agent output;
- model preference;
- tool validation;
- workflow convenience;
- implementation display;
- search ranking;
- folder placement;
- backlinks;
- tags;
- generated summaries;
- accepted suggestions;
- prior agent behavior.

Authority must remain governed, traceable, reviewable, and subordinate to the applicable standards and workflows.

### 10.5 Validation Escalation and Stop Conditions

An Agent Initialization Packet MUST require escalation where validation scope, validation result, validation method, validation evidence, unresolved validation issue, validation failure, or validation authority is unclear.

An agent MUST stop where continuing would treat validation as approval.

An agent MUST NOT treat a validation result as:

- final approval;
- final Authority Level;
- final Privacy Classification;
- final Lifecycle State;
- publication permission;
- export permission;
- migration permission;
- deletion permission;
- downstream-use clearance;
- governance acceptance.

Validation may support review.

Validation does not replace review unless a higher-authority governed workflow or specification explicitly defines that behavior within a limited scope.

### 10.6 Source and Provenance Escalation and Stop Conditions

An Agent Initialization Packet MUST require escalation where source support, Source References, provenance, extraction history, transformation history, source reliability, source authority, or source availability is missing, unclear, contradictory, or insufficient for the assigned task.

An agent MUST stop where continuing would create unsupported source-derived knowledge, obscure source limitations, remove provenance, collapse provenance, or present source-derived output as approved governed knowledge without review.

An agent MUST preserve the distinction between:

- Source Material and Knowledge Records;
- extracted information and governed knowledge;
- source support and approval;
- provenance and authority;
- summary and validated record;
- draft and approved record.

Where source support is insufficient, the agent SHOULD flag the issue, limit the output, and escalate where needed.

### 10.7 Workflow and Implementation Escalation and Stop Conditions

An Agent Initialization Packet MUST require escalation where workflow state, review state, lifecycle state, publication state, export state, migration state, deletion state, downstream-use state, implementation behavior, storage behavior, or tool behavior is unclear or conflicting.

An agent MUST stop where continuing would allow an implementation to override The Brain Standard.

An agent MUST NOT treat the following as governed approval or governed meaning by itself:

- file location;
- folder placement;
- tag assignment;
- backlink creation;
- graph connection;
- index inclusion;
- cache generation;
- workflow status label;
- software state;
- tool output;
- model output;
- script completion;
- automation success;
- repository visibility;
- vault visibility;
- user-interface display.

Implementation behavior may support the standard.

Implementation behavior does not define the standard.

### 10.8 Destructive-Action Escalation and Stop Conditions

An Agent Initialization Packet MUST require escalation before destructive action unless a higher-authority governed workflow or specification explicitly permits a narrow automated action within a defined scope.

Destructive action includes:

- deletion;
- permanent removal;
- overwrite;
- replacement;
- irreversible movement;
- merge;
- split;
- Object Identity change;
- supersession;
- deprecation;
- archival where archival changes governed use;
- quarantine where quarantine changes governed use;
- publication;
- export;
- migration;
- privacy exposure;
- downstream-use clearance.

An agent MUST stop where destructive action is requested but not explicitly permitted.

An agent MAY recommend destructive action where the role and permission boundary allow recommendation.

A recommendation to delete, merge, split, supersede, deprecate, publish, export, migrate, or clear downstream use MUST remain proposed until accepted through a governed process.

### 10.9 Escalation and Stop Conditions Success Criteria

Escalation and Stop Conditions conform to AG-SPEC-0001 when:

- escalation triggers are explicit;
- stop conditions are explicit;
- privacy risk triggers escalation or stop;
- authority risk triggers escalation or stop;
- validation confusion triggers escalation or stop;
- missing source support triggers escalation or limitation;
- missing provenance triggers escalation or limitation;
- relationship conflict triggers escalation;
- lifecycle conflict triggers escalation;
- workflow conflict triggers escalation;
- implementation conflict triggers escalation;
- destructive action requires explicit governed permission;
- agents stop when continuing would violate higher-authority standards;
- agents do not continue merely because a tool, model, implementation, workflow, or user instruction makes continuation possible.

Escalation and Stop Conditions are successful when an agent can identify risk, pause unsafe action, preserve governed meaning, preserve privacy, preserve authority boundaries, preserve validation boundaries, preserve source and provenance requirements, preserve workflow boundaries, preserve implementation independence, and route unresolved issues to human review or a governed workflow.

## 11. Agent Initialization Packet Template

The Agent Initialization Packet Template defines a practical structure that MAY be used to initialize agents under AG-SPEC-0001.

The template exists so that humans, agents, subagents, workflows, validators, storage systems, implementations, and future automation can initialize agents consistently without redefining agent authority, role behavior, permission boundaries, source requirements, privacy requirements, validation requirements, traceability requirements, escalation requirements, or stop conditions.

The template is a usable packet structure.

The template is not the only permitted representation.

A compliant implementation MAY adapt the template into Markdown, plain text, YAML, JSON, a prompt template, a workflow form, a task card, an implementation profile, a script configuration, an agent runtime configuration, or another practical format.

Adapted formats MUST preserve the meaning, boundaries, reviewability, traceability, privacy expectations, validation expectations, authority limits, escalation rules, stop conditions, and implementation independence defined by AG-SPEC-0001.

### 11.1 Template Use Rules

The Agent Initialization Packet Template SHOULD be used before governed agent work begins.

The template MAY be shortened for low-risk read-only work where missing fields do not affect governed meaning, privacy, authority, validation, lifecycle state, Source References, provenance, relationships, publication, export, migration, deletion, downstream use, or governance.

The template SHOULD NOT be shortened where agent activity affects governed meaning, privacy boundaries, authority boundaries, validation state, lifecycle transitions, Source References, provenance, relationship proposals, publication readiness, export readiness, migration readiness, destructive action, or downstream-use permission.

Where required information is unknown, the packet SHOULD mark the field as:

- Unresolved;
- Not Applicable;
- Pending Review;
- Not Authorized;
- Escalation Required;
- another clear governed status.

Blank fields SHOULD NOT be treated as permission.

Missing context SHOULD NOT be treated as approval.

### 11.2 Minimum Initialization Packet Template

The following template MAY be used as the minimum practical Agent Initialization Packet:

 **Agent Initialization Packet**

Document Reference:

- Packet ID:
- Packet Version:
- Packet Date:
- Initialized By:
- Review Contact:
- Related Activity Record:

Agent Identity:

- Agent Name or Identifier:
- Agent Type:
- Agent Instance or Run Identifier:
- Runtime, Tool, Model, Script, or Implementation Reference:
- Operator or Requesting Human:

Role Assignment:

- Assigned Role:
- Role Source:
- Role Scope:
- Role Responsibility:
- Expected Role Output:
- Multi-Role Assignment:
- Role Conflict Status:

Operating Context:

- Project Context:
- Task Context:
- Material Scope:
- Material Out of Scope:
- Workflow Context:
- Storage Context:
- Source Context:
- Review Context:
- Implementation Context:

Governing References:

- Constitutional Documents:
- Knowledge Standards:
- Storage Standards:
- Agent Standards:
- Workflow Standards:
- Templates:
- Validation References:
- Implementation Profiles:

Permission Boundary:

- Allowed Operations:
- Prohibited Operations:
- Conditional Operations:
- Read Permission:
- Write Permission:
- Move Permission:
- Destructive-Action Permission:
- Downstream-Use Permission:

Authority Boundary:

- Default Authority:
- Final Approval Permission:
- Authority-Level Permission:
- Privacy-Classification Permission:
- Lifecycle-State Permission:
- Validation-Acceptance Permission:
- Publication Permission:
- Export Permission:
- Migration Permission:
- Deletion Permission:

Source, Privacy, and Validation Awareness:

- Source Material in Scope:
- Source Material out of Scope:
- Source Reference Expectations:
- Provenance Expectations:
- Privacy Classification:
- Privacy Limits:
- Validation Scope:
- Validation Limits:
- Authority Awareness:
- Lifecycle Awareness:
- Relationship Awareness:

Required Outputs:

- Output Type:
- Output Format:
- Output Destination:
- Draft or Proposed Status:
- Required Review:
- Required Citations or Source References:
- Required Provenance Notes:
- Required Validation Notes:
- Required Escalation Notes:

Activity Recording and Traceability:

- Activity Record Required:
- Activity Record Location:
- Input Traceability Required:
- Output Traceability Required:
- Action Traceability Required:
- Decision or Recommendation Traceability Required:
- Escalation Traceability Required:
- Stop-Condition Traceability Required:
- Preservation Requirement:

Escalation Conditions:

- Scope Ambiguity:
- Role Ambiguity:
- Permission Ambiguity:
- Authority Risk:
- Privacy Risk:
- Validation Risk:
- Source Risk:
- Provenance Risk:
- Relationship Risk:
- Lifecycle Risk:
- Workflow Risk:
- Implementation Risk:
- Destructive-Action Risk:
- Downstream-Use Risk:
- Governance Conflict:

Stop Conditions:

- Higher-Authority Conflict:
- Out-of-Scope Action:
- Unpermitted Read:
- Unpermitted Write:
- Unpermitted Move:
- Unpermitted Destructive Action:
- Unpermitted Publication:
- Unpermitted Export:
- Unpermitted Migration:
- Unpermitted Deletion:
- Unpermitted Downstream Use:
- Privacy Boundary Violation:
- Authority Boundary Violation:
- Validation-as-Approval Risk:
- Source or Provenance Failure:
- Revoked, Rejected, Superseded, Expired, Invalid, or Out-of-Scope Packet:

Initialization Decision:

- Initialization Status:
- Authorized Scope:
- Restricted Scope:
- Unresolved Issues:
- Required Human Review:
- Agent May Proceed:
- Agent Must Escalate:
- Agent Must Stop:

### 11.3 Field Completion Rules

Template fields SHOULD be completed clearly enough for the assigned task.

A field MAY be marked Not Applicable only where the field does not affect the task, permission boundary, authority boundary, privacy boundary, validation expectation, source requirement, provenance requirement, relationship behavior, lifecycle state, workflow state, publication, export, migration, deletion, downstream use, or governance.

A field SHOULD be marked Unresolved where the agent cannot determine the required information.

A field SHOULD be marked Not Authorized where the action is outside the permission boundary.

A field SHOULD be marked Pending Review where the agent may propose but not finalize.

A field SHOULD be marked Escalation Required where the agent cannot safely proceed without review.

Template completion MUST NOT convert unresolved fields into permission.

Template completion MUST NOT convert proposed fields into approved fields.

Template completion MUST NOT convert validation fields into approval fields.

Template completion MUST NOT convert implementation fields into standards.

### 11.4 Template Adaptation Rules

A compliant implementation MAY adapt the template structure if the adapted packet preserves required meaning.

Adaptation MAY include:

- changing field names;
- changing field order;
- using frontmatter;
- using tables;
- using JSON;
- using YAML;
- using forms;
- using task cards;
- using prompts;
- using workflow records;
- using implementation configuration;
- using script-readable configuration;
- using another practical representation.

Adaptation MUST preserve:

- agent identity;
- role assignment;
- operating context;
- permission boundary;
- authority boundary;
- privacy boundary;
- source awareness;
- provenance awareness;
- validation awareness;
- activity recording;
- traceability;
- escalation;
- stop conditions;
- reviewability;
- implementation independence.

An adapted packet MUST NOT remove required meaning merely because an implementation has a different interface or file format.

### 11.5 Template Output Handling

A completed Agent Initialization Packet SHOULD be stored, linked, referenced, embedded, logged, or otherwise preserved where needed for review, validation, maintenance, governance, privacy audit, authority review, publication review, export review, migration review, deletion review, downstream-use review, or future troubleshooting.

The packet MAY be referenced by an Agent Activity Record.

The packet MAY be referenced by a Review Record.

The packet MAY be referenced by a workflow output.

The packet MAY be referenced by an implementation-support file.

The packet MAY be referenced by a future agent configuration.

Packet storage location does not define packet authority by itself.

A packet is authoritative only within the boundaries defined by AG-SPEC-0001 and higher-authority standards.

### 11.6 Template Success Criteria

The Agent Initialization Packet Template conforms to AG-SPEC-0001 when:

- it can identify the agent;
- it can assign the role;
- it can define the operating context;
- it can identify governing references;
- it can define permission boundaries;
- it can define authority boundaries;
- it can preserve source awareness;
- it can preserve privacy awareness;
- it can preserve validation awareness;
- it can require activity recording;
- it can support traceability;
- it can identify escalation conditions;
- it can identify stop conditions;
- it can state whether the agent may proceed;
- it can remain implementation-independent;
- it can be reviewed by a human or governed workflow.

The template is successful when it can initialize an agent clearly enough for useful work while preventing hidden scope expansion, hidden permission, hidden authority, hidden privacy exposure, hidden validation approval, hidden workflow approval, hidden storage meaning, hidden implementation dependence, and hidden governance.

## 12. Initialization Success Criteria

Initialization Success Criteria define when an Agent Initialization Packet is sufficient for governed agent work under AG-SPEC-0001.

An agent is sufficiently initialized only when it has enough identity, role, operating context, permission boundary, authority boundary, source awareness, privacy awareness, validation awareness, traceability requirement, escalation condition, and stop condition to perform the assigned task without creating hidden authority, hidden permission, hidden privacy exposure, hidden validation approval, hidden workflow approval, hidden storage meaning, hidden implementation dependence, or governance drift.

Initialization success does not mean the agent output is approved.

Initialization success does not mean the agent may operate autonomously without review.

Initialization success does not mean the agent has authority to publish, export, migrate, delete, approve, assign final Authority Level, assign final Privacy Classification, perform final lifecycle transitions, approve relationships, approve Source References, clear downstream use, or override governance.

Initialization success means the agent may proceed only within the initialized role, task, scope, permissions, boundaries, review requirements, escalation requirements, and stop conditions.

### 12.1 Minimum Success Criteria

An Agent Initialization Packet conforms to AG-SPEC-0001 when:

- agent identity is explicit or traceable;
- role assignment is explicit or marked unresolved;
- task context is defined;
- operating context is defined;
- material scope is bounded;
- governing standards are identified or inferable from the packet;
- allowed operations are identified;
- prohibited operations are preserved;
- permission boundaries are explicit;
- authority boundaries are explicit;
- privacy boundaries are identified where needed;
- source-awareness requirements are identified where needed;
- provenance requirements are identified where needed;
- validation expectations are identified where needed;
- activity recording requirements are identified where needed;
- traceability requirements are identified where needed;
- escalation conditions are identified;
- stop conditions are identified;
- output handling is defined;
- review requirements are defined;
- implementation behavior remains subordinate to the standard.

Where these criteria are not met, the packet SHOULD be treated as incomplete, limited, or escalation-required.

### 12.2 Safe Proceed Criteria

An agent may proceed with governed work only when:

- the assigned task is known;
- the assigned role is known;
- the material scope is known;
- the permission boundary is known;
- the authority boundary is known;
- the privacy boundary is known where applicable;
- the validation scope is known where applicable;
- the source and provenance expectations are known where applicable;
- the required output is known;
- the required review state is known;
- escalation conditions are known;
- stop conditions are known;
- no higher-authority conflict is known;
- no unresolved risk prevents safe operation.

If these criteria are not satisfied, the agent SHOULD limit activity to clarification, low-risk inspection, or escalation.

An agent MUST stop where proceeding would violate a higher-authority standard, privacy boundary, authority boundary, permission boundary, validation expectation, workflow rule, source requirement, provenance requirement, storage boundary, implementation boundary, or governance requirement.

### 12.3 Output Success Criteria

Agent output created after initialization conforms to AG-SPEC-0001 when:

- the output is within the initialized task;
- the output is within the assigned role;
- the output is within material scope;
- the output is within permission boundaries;
- the output preserves authority boundaries;
- the output preserves privacy boundaries;
- the output preserves source distinctions;
- the output preserves provenance where required;
- the output preserves validation limits;
- the output preserves lifecycle limits;
- the output preserves relationship limits;
- the output is distinguishable from approved governed material;
- the output identifies required review where needed;
- the output identifies escalation where needed;
- the output does not imply approval, authority, privacy clearance, validation acceptance, publication permission, export permission, migration permission, deletion permission, or downstream-use clearance unless explicitly permitted by a governed process.

Agent output is successful when future review can determine what the agent produced, why it produced it, what boundaries applied, what review is required, what risks remain, and whether the output may be accepted, rejected, repaired, escalated, superseded, archived, or used in a later governed workflow.

### 12.4 Traceability Success Criteria

Agent initialization is traceable when future review can determine:

- what packet initialized the agent;
- what packet version applied;
- what agent was initialized;
- what role was assigned;
- what task was assigned;
- what material was in scope;
- what material was out of scope where needed;
- what permissions applied;
- what authority limits applied;
- what privacy limits applied;
- what validation expectations applied;
- what Source Material expectations applied;
- what provenance expectations applied;
- what activity recording was required;
- what output was produced;
- what action was performed;
- what recommendation was made;
- what escalation occurred;
- what stop condition occurred;
- what review remains required.

Traceability is successful when agent activity can be reviewed, corrected, limited, rejected, repaired, escalated, superseded, archived, or governed without relying only on hidden application state, model memory, chat history, tool logs, implementation defaults, or human memory.

### 12.5 Failure Criteria

An Agent Initialization Packet fails AG-SPEC-0001 when:

- agent identity is missing where required;
- role assignment is missing or misleading;
- task scope is unclear;
- material scope is unclear;
- permission boundaries are missing;
- authority boundaries are missing;
- privacy boundaries are missing where needed;
- validation expectations are missing where needed;
- source-awareness requirements are missing where needed;
- provenance expectations are missing where needed;
- activity recording is missing where required;
- escalation conditions are missing;
- stop conditions are missing;
- implementation behavior overrides the standard;
- output handling is unclear;
- review requirements are unclear;
- unresolved ambiguity is treated as permission;
- validation is treated as approval;
- visibility is treated as permission;
- tool capability is treated as governance;
- agent confidence is treated as Authority Level;
- workflow completion is treated as approval;
- storage location is treated as meaning;
- agent output is treated as approved governed material without review.

A failed packet SHOULD be repaired, replaced, rejected, superseded, or escalated through a governed process.

An agent initialized under a failed packet SHOULD NOT continue governed work until the failure is resolved or the task is limited to safe clarification, low-risk inspection, or escalation.

### 12.6 Relationship to Future Specifications

Future agent specifications, subagent profiles, workflow runbooks, implementation profiles, templates, scripts, prompts, tools, agent runtimes, automation frameworks, or storage systems MAY extend AG-SPEC-0001.

Future extensions MUST NOT weaken:

- agent identity requirements;
- role assignment requirements;
- operating context requirements;
- permission boundaries;
- authority boundaries;
- privacy boundaries;
- source awareness;
- provenance awareness;
- validation awareness;
- activity recording;
- traceability;
- escalation;
- stop conditions;
- reviewability;
- implementation independence;
- governance.

AG-SPEC-0002 MAY define reusable subagent prompts, role profiles, and role-specific initialization details.

WF-SPEC-0001 MAY define the controlled ingestion runbook that uses Agent Initialization Packets during file-drop ingestion.

Implementation profiles MAY define platform-specific ways to represent or execute initialization packets.

No future implementation profile, prompt, model, tool, script, plugin, vault, repository, folder, interface, or automation framework may override AG-SPEC-0001 unless the standard is formally revised through governance.

### 12.7 Final Success Statement

AG-SPEC-0001 is successful when agents can be initialized in a repeatable, bounded, inspectable, reviewable, privacy-respecting, validation-aware, source-aware, authority-aware, workflow-compatible, traceable, portable, and implementation-independent way.

AG-SPEC-0001 is successful when an initialized agent can help The Brain perform useful work without becoming the hidden source of governed meaning, hidden authority, hidden approval, hidden privacy clearance, hidden validation acceptance, hidden publication permission, hidden export permission, hidden migration permission, hidden deletion permission, hidden downstream-use clearance, or hidden governance.

AG-SPEC-0001 is successful when future humans, agents, workflows, validators, storage systems, implementations, import processes, export processes, migration processes, publication processes, and governance processes can determine:

- what agent was initialized;
- what role was assigned;
- what task was assigned;
- what context applied;
- what permission scope applied;
- what authority boundary applied;
- what privacy boundary applied;
- what source and provenance expectations applied;
- what validation expectations applied;
- what activity recording was required;
- what escalation and stop conditions applied;
- what output was produced;
- what review remains required;
- whether the agent stayed within its initialized scope.

AG-SPEC-0001 closes with the following rule:

Agents may begin governed work only when initialized within a bounded, reviewable, traceable, privacy-respecting, validation-aware, source-aware, authority-aware, and implementation-independent packet.

Agent initialization permits bounded assistance.

Agent initialization does not create final authority.
