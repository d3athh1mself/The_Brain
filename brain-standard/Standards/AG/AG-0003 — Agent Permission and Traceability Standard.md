# AG-0003 — Agent Permission and Traceability Standard

Document ID: AG-0003
Title: Agent Permission and Traceability Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Standard
Phase: Phase 3 — Agent Framework
Milestone: 3.3 — Agent Permission and Traceability Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; AG-0002 — Agent Role and Responsibility Standard
Supersedes: None
Superseded By: None
Related: AG-0001 — Agent Operating Boundaries Standard; AG-0002 — Agent Role and Responsibility Standard

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, traceability expectations, review requirements, escalation requirements, and agent-permission rules are interpreted within AG-0003.

Where conflicts arise between agent permission, agent access, agent role responsibility, agent authority, activity records, output traceability, review records, approval records, escalation records, permission profiles, workflow behavior, storage behavior, implementation behavior, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, downstream use, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

AG-0003 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

AG-0003 depends on the Phase 1 Knowledge Standards because agent permissions and traceability records must preserve knowledge meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation.

AG-0003 depends on the Phase 2 Storage Standards because agent permissions may apply to stored material, storage movement, storage inspection, storage staging, imports, exports, archives, backups, migration packages, implementation-support files, and generated records without allowing storage placement to define knowledge meaning or permission.

AG-0003 depends on AG-0001 because permission and traceability requirements must operate inside the agent operating boundaries already defined by the Agent Framework.

AG-0003 depends on AG-0002 because agent roles and subagent responsibilities require explicit permission scope, traceability, reviewability, and escalation handling before role outputs can safely affect governed material.

AG-0003 defines agent permission and traceability behavior at the conceptual standard level.

AG-0003 does not define exact prompts, exact model behavior, exact tool APIs, exact runtime permissions files, exact access-control syntax, exact log schemas, exact database structures, exact folder paths, exact automation scripts, exact user-interface behavior, exact implementation-specific permission systems, or exact agent-framework configuration files.

Those concerns belong to later agent specifications, permission profiles, traceability specifications, workflow standards, implementation profiles, operational guides, validation specifications, templates, and reference implementations.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Agent Framework refers to Layer 3 of The Brain Standard, responsible for defining how agents may interact with knowledge, source material, storage structures, workflow instructions, and implementation environments while preserving reviewability, traceability, privacy, and governance.
- Agent refers to a human-directed or system-directed AI, automation, script, model-driven process, tool-using assistant, workflow participant, or future automated actor that reads, classifies, summarizes, extracts, proposes, validates, drafts, moves, edits, creates, deletes, exports, publishes, migrates, or otherwise acts on governed material.
- Agent Role refers to a standard-level responsibility profile that describes the kind of work an agent may perform or support within a governed scope.
- Subagent refers to a narrower agent instance, tool, process, script, workflow participant, or assistant that performs part of an Agent Role.
- Agent Permission refers to an allowed agent capability within a defined scope.
- Permission Scope refers to the defined boundary within which an Agent Permission applies, including applicable role, action, target material, workflow context, privacy boundary, authority boundary, lifecycle boundary, validation boundary, implementation context, or time limit.
- Permission Profile refers to a defined grouping of allowed, restricted, conditional, or prohibited agent actions within a governed scope.
- Permission Grant refers to an explicit assignment of a permission or permission profile to an agent, role, subagent, workflow, implementation, or operation within a defined scope.
- Permission Constraint refers to a condition, limitation, review requirement, privacy requirement, workflow requirement, escalation requirement, or traceability requirement that limits how a permission may be used.
- Permission Denial refers to a rule, decision, absence of permission, revoked permission, expired permission, or scope limit that prevents an agent from performing an action.
- Permission Review refers to the governed evaluation of whether a permission, permission profile, permission grant, permission constraint, or permission use remains appropriate, safe, current, traceable, and compliant.
- Permission Revocation refers to the removal, suspension, reduction, or withdrawal of an Agent Permission or Permission Profile.
- Permission Expiration refers to the end of a permission’s validity due to time limit, workflow completion, scope completion, review failure, lifecycle change, privacy change, authority change, validation issue, or other governed condition.
- Agent Access refers to an agent’s ability to read, inspect, search, summarize, extract, index, classify, modify, move, copy, export, publish, delete, migrate, or otherwise interact with a governed entity.
- Agent Authority refers to governed decision-making power explicitly granted by a standard, specification, workflow, governance process, or permission profile.
- Agent Activity refers to any action, recommendation, classification, extraction, validation, summary, draft, change, movement, deletion, export, publication, migration, or decision-support output produced or assisted by an agent.
- Agent Activity Record refers to a traceable record of material agent activity, including what action occurred, what scope applied, what material was affected or inspected, what output was produced, what review is required, and what escalation or privacy boundary applies where applicable.
- Agent Output refers to a result produced by an agent, including a summary, classification, proposed metadata, proposed relationship, validation result, draft record, proposed edit, file movement recommendation, warning, report, transformation, or generated content.
- Output Traceability refers to the ability to determine what agent, role, permission scope, source material, inspected material, assumptions, evidence, review requirement, privacy boundary, workflow context, or implementation context produced or affected an Agent Output.
- Traceability Record refers to a record that preserves enough context to review, validate, explain, reproduce, reject, approve, repair, escalate, or audit an agent activity or agent output where governed meaning or governed handling may be affected.
- Review Record refers to a traceable record of review activity, including what was reviewed, by whom or by what process, what decision or finding resulted, what scope applied, and what unresolved issues remain.
- Approval Traceability refers to traceability that connects an approval decision to its scope, reviewer, reviewed material, review basis, applicable permissions, applicable workflow, and downstream-use limits.
- Escalation Record refers to a traceable record of a routed risk, ambiguity, conflict, privacy concern, authority concern, validation issue, destructive action, unresolved decision, or critical knowledge change requiring human review or governed workflow handling.
- High-Risk Operation refers to an agent operation that may affect Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, downstream use, governance, or implementation behavior.
- Restricted Operation refers to an agent operation that requires explicit permission, heightened traceability, review, escalation, privacy handling, or workflow control before it may be performed.
- Critical Knowledge Change refers to a change that affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, governed meaning, publication, export, migration, deletion, supersession, deprecation, or downstream use.
- Governed Entity refers to a Knowledge Object, Knowledge Record, Source Material, Source Reference, provenance record, relationship, metadata record, validation result, lifecycle state, authority assignment, privacy classification, governed document, workflow output, agent output, import record, export record, migration record, decision, or other entity governed by The Brain Standard.
- Human Review refers to review, correction, acceptance, rejection, approval, or escalation performed by an authorized human.
- Escalation refers to routing a condition, ambiguity, risk, conflict, privacy concern, authority concern, validation issue, destructive action, or critical knowledge change to human review or a governed workflow.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of AG-0003 is to define permission and traceability requirements for agents operating within The Brain Standard.

AG-0001 defines agent operating boundaries.

AG-0002 defines agent roles and responsibilities.

AG-0003 defines how agent actions become permissioned, inspectable, traceable, reviewable, and accountable.

The Agent Permission and Traceability Standard exists so future humans, agents, workflows, validators, storage systems, implementations, and governance processes can determine:

- what an agent is allowed to do;
- what an agent is not allowed to do;
- what permission scope applies to an agent action;
- what constraints apply to an agent action;
- what must be recorded when an agent acts;
- what traceability must exist for agent outputs;
- what review is required before agent output may affect governed material;
- what escalation is required when an agent encounters ambiguity, risk, conflict, or restricted material;
- what permission review, revocation, or expiration is required;
- how agent work remains useful without becoming hidden governance.

AG-0003 exists to prevent permission confusion and traceability failure.

Permission confusion occurs when agent access, tool capability, role responsibility, workflow routing, implementation visibility, storage location, agent confidence, prior successful behavior, or user-interface convenience is mistaken for permission, authority, approval, validation acceptance, privacy clearance, lifecycle transition, publication permission, export permission, migration permission, deletion permission, downstream-use permission, or governance acceptance.

Traceability failure occurs when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, or governance processes cannot determine what agent acted, what material was inspected, what material was changed or proposed for change, what permission applied, what evidence supported the output, what assumptions were made, what review occurred, what review remains required, what escalation occurred, or what risk remains unresolved.

AG-0003 defines standard-level behavior for:

- agent permission profiles;
- read permissions;
- proposal permissions;
- write and edit permissions;
- move and storage permissions;
- validation permissions;
- creation permissions;
- high-risk and restricted permissions;
- agent activity records;
- output traceability;
- review and approval traceability;
- escalation records;
- permission review;
- permission revocation;
- permission expiration;
- conformance;
- non-conformance;
- exceptions;
- success criteria.

AG-0003 does not make agents authorities by default.

AG-0003 does not make agent roles self-permissioning.

AG-0003 does not make activity logs approval records by default.

AG-0003 does not make traceability a substitute for review.

AG-0003 does not make review preparation the same as review completion.

AG-0003 does not make validation support the same as validation acceptance.

AG-0003 does not make workflow completion the same as approval unless a governed workflow or future specification explicitly defines that effect within a controlled scope.

AG-0003 does not allow hidden memory, hidden application state, plugin behavior, database internals, storage location, folder placement, workflow memory, implementation defaults, model confidence, or repeated agent behavior to become the only source of permission or traceability where governed meaning or governed handling is affected.

The primary purpose of AG-0003 is to ensure that agent activity remains bounded, permissioned, traceable, privacy-respecting, reviewable, and implementation-independent.

AG-0003 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, and governance processes can determine:

- what permission applied to an agent action;
- what permission did not apply;
- what agent output was produced;
- what governed entity was affected or inspected;
- what review is required;
- what approval state exists or does not exist;
- what escalation is required;
- what privacy boundary applies;
- what traceability record supports accountability;
- whether the action preserved The Brain Standard without silently creating authority, approval, validation acceptance, privacy clearance, lifecycle transition, publication permission, export permission, migration permission, deletion permission, downstream-use permission, or governance acceptance.

## 2. Relationship to Prior Standards

AG-0003 is subordinate to and derived from the constitutional foundation of The Brain Standard.

AG-0003 depends on:

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
- AG-0002 — Agent Role and Responsibility Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

AG-0003 applies that purpose by requiring agent permissions and traceability to remain portable, explicit, inspectable, reviewable, privacy-respecting, and independent of any single model, tool, vault, plugin, runtime, database, folder layout, user interface, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

AG-0003 applies those principles by requiring agent permission and traceability behavior to preserve:

- knowledge integrity;
- implementation independence;
- portability;
- explicit structure;
- source distinction;
- provenance;
- privacy boundaries;
- human reviewability;
- governed evolution;
- practical daily usability.

TB-0002 establishes the layered architecture of The Brain Standard.

AG-0003 belongs to Layer 3 — Agent Framework.

Because agent permissions and traceability affect how agents interact with knowledge, storage, workflows, and implementations, AG-0003 must preserve the lower-layer meanings defined by the Universal Knowledge Standard and Storage Standard while supporting higher-layer workflows and future implementations.

AG-0003 MUST NOT allow Layer 3 agent behavior to redefine Layer 1 knowledge meaning.

AG-0003 MUST NOT allow Layer 3 agent behavior to redefine Layer 2 storage meaning.

AG-0003 MUST NOT allow Layer 3 agent behavior to silently override Layer 4 workflow review, approval, escalation, or routing rules.

AG-0003 MUST NOT allow Layer 5 implementation behavior to become the source of agent permission, authority, or traceability unless a governed specification explicitly defines that behavior within a controlled scope.

TB-0003 establishes the governance model for The Brain Standard.

AG-0003 follows the document authority hierarchy defined by TB-0003. As a standard-level document, AG-0003 has high authority within its scope but remains subordinate to constitutional documents.

AG-0003 supports governance by requiring agent activity that affects governed meaning, privacy, authority, validation, lifecycle state, publication, export, migration, deletion, or downstream use to remain traceable and reviewable.

KS-0001 defines the Knowledge Object Model.

AG-0003 depends on KS-0001 because agent permissions and traceability must preserve the distinction between Knowledge Objects, Knowledge Records, Source Material, metadata, relationships, provenance, lifecycle state, authority, privacy classification, validation, workflows, agents, and implementations.

An agent MAY assist with Knowledge Objects and Knowledge Records only within its permission scope.

An agent MUST NOT cause knowledge meaning to depend on hidden agent state, hidden workflow state, hidden implementation behavior, or unrecorded output where governed meaning is affected.

KS-0002 defines Object Identity.

AG-0003 depends on KS-0002 because agent activity may read, propose, validate, move, create, merge, split, redirect, supersede, deprecate, or otherwise affect identity-related material.

An agent role or permission MUST NOT silently create, merge, split, redirect, supersede, delete, or reassign Object Identity unless a governed permission, workflow, review requirement, and traceability requirement explicitly allow the action within scope.

KS-0003 defines Metadata behavior.

AG-0003 depends on KS-0003 because agents may inspect, extract, propose, validate, edit, or create metadata.

Agent-generated metadata MUST remain distinguishable from human-reviewed, workflow-approved, validated, or authoritative metadata unless a governed workflow or future specification explicitly changes that status.

KS-0004 defines Relationship behavior.

AG-0003 depends on KS-0004 because agents may inspect, infer, propose, validate, edit, or create relationships.

Agent-generated relationships MUST remain distinguishable from reviewed, approved, deprecated, superseded, rejected, or authoritative relationships unless a governed workflow or future specification explicitly changes that status.

KS-0005 defines Source Reference and Provenance behavior.

AG-0003 depends on KS-0005 because agent activity may inspect Source Material, extract evidence, summarize sources, propose Source References, create provenance records, or transform source-derived material.

Agent-generated Source References and provenance records MUST preserve source boundaries, attribution expectations, privacy boundaries, extraction context, transformation context, and review needs.

KS-0006 defines Lifecycle State behavior.

AG-0003 depends on KS-0006 because agents may inspect, propose, validate, route, or support lifecycle-state handling.

An agent may propose lifecycle state or identify lifecycle risk.

An agent MUST NOT silently perform a lifecycle transition where review, approval, authority, privacy, validation, publication, export, migration, deletion, or downstream use may be affected unless a governed workflow or future specification explicitly grants that permission within scope.

KS-0007 defines Authority Level behavior.

AG-0003 depends on KS-0007 because agents may inspect, propose, validate, or report authority-related information.

Agent confidence is not Authority Level.

Agent permission is not Authority Level.

Agent output is not Authority Level.

Agent review support is not Authority Review completion.

An agent MUST NOT assign, raise, lower, remove, or rely on Authority Level beyond its governed permission scope.

KS-0008 defines Privacy Classification behavior.

AG-0003 depends on KS-0008 because agent permissions and traceability records must preserve privacy boundaries.

Agent access is not privacy clearance.

Agent visibility is not privacy permission.

Traceability records, activity records, review records, and escalation records MUST NOT expose restricted material beyond the permitted scope.

Where restricted material is involved, records SHOULD preserve enough information for review without unnecessarily exposing restricted content.

KS-0009 defines Validation behavior.

AG-0003 depends on KS-0009 because agents may perform validation support, produce validation findings, identify validation risk, or propose validation status.

Agent-generated validation is not approval.

Validation support is not validation acceptance.

Validation passing is not permission to publish, export, migrate, delete, approve, or use downstream unless a governed workflow or future specification explicitly defines that effect within scope.

SS-0001 defines Storage Architecture.

AG-0003 depends on SS-0001 because agents may inspect, route, preserve, recommend, move, copy, export, import, archive, or organize stored material only without allowing storage behavior to define knowledge meaning.

SS-0002 defines Storage Layout.

AG-0003 depends on SS-0002 because agents may interact with practical storage areas, draft areas, review areas, archives, import areas, export areas, migration areas, implementation-support areas, indexes, caches, and generated files.

Storage location may support permission handling.

Storage location MUST NOT be treated as permission by itself.

AG-0001 defines Agent Operating Boundaries.

AG-0003 does not replace AG-0001.

AG-0003 extends AG-0001 by defining how agent actions are permissioned, recorded, traced, reviewed, escalated, constrained, revoked, or expired.

AG-0001 answers:

- What are agents allowed or prohibited from doing at the boundary level?

AG-0003 answers:

- What permissions, records, traceability, review requirements, and escalation evidence must exist when agents act?

AG-0002 defines Agent Roles and Responsibilities.

AG-0003 does not replace AG-0002.

AG-0003 extends AG-0002 by requiring roles to operate through explicit permissions and traceability.

AG-0002 answers:

- What roles exist?
- What is each role responsible for?

AG-0003 answers:

- What actions may each role perform only when permissioned?
- What must be recorded when the role acts?
- What output traceability is required?
- What review, approval traceability, escalation, revocation, or expiration applies?

AG-0003 SHALL preserve the distinction between role, permission, authority, review, approval, validation, privacy classification, lifecycle state, storage behavior, workflow behavior, and implementation behavior.

AG-0003 is successful when it extends prior standards into a clear permission and traceability model without weakening agent boundaries, role separation, Object Identity, metadata role boundaries, relationship behavior, source-reference behavior, provenance preservation, lifecycle handling, authority expectations, privacy protection, validation expectations, storage independence, workflow review, implementation independence, or practical daily usability.

## 3. Agent Permission Model

The Agent Permission Model defines how agent actions become allowed, limited, denied, recorded, reviewed, escalated, revoked, or expired within The Brain Standard.

Agent permission is an explicit allowance for an agent, role, subagent, workflow participant, tool-using process, automation, script, or implementation-support process to perform a defined action within a defined scope.

Agent permission is not the same as agent access.

Agent access describes what an agent can technically reach, open, search, inspect, modify, move, export, publish, delete, or otherwise interact with.

Agent permission describes what an agent is allowed to do under The Brain Standard.

An agent may have access without permission.

An agent may have tool capability without permission.

An agent may have visibility without permission.

An agent may have searchability without permission.

An agent may have role responsibility without permission.

An agent may produce output without approval.

An agent may support validation without validation acceptance.

An agent may support review without review completion.

An agent may participate in a workflow without receiving authority.

A compliant Agent Permission Model SHALL preserve the following distinctions:

- access is not authority;
- access is not permission by itself;
- visibility is not permission;
- searchability is not permission;
- tool capability is not permission;
- agent confidence is not authority;
- role responsibility is not permission;
- permission is not approval;
- permission is not Authority Level;
- permission is not Privacy Classification;
- permission is not Lifecycle State transition;
- permission is not Validation State;
- validation support is not approval;
- review preparation is not review completion;
- workflow completion is not approval unless explicitly governed;
- implementation behavior is not standard meaning;
- logs are not governed meaning by themselves;
- traceability does not replace approval.

Agent permissions SHALL be scoped.

A permission scope SHOULD define, where applicable:

- the agent, role, subagent, workflow, implementation, or process receiving permission;
- the permitted action or action category;
- the governed entity or storage area affected;
- the allowed input material;
- the allowed output type;
- the privacy boundary;
- the authority boundary;
- the lifecycle boundary;
- the validation boundary;
- the workflow context;
- the implementation context;
- the time limit or expiration condition;
- the review requirement;
- the escalation requirement;
- the traceability requirement;
- the downstream-use limit.

An agent permission MAY allow an action only under conditions.

Conditional permission MAY depend on:

- human direction;
- workflow stage;
- lifecycle state;
- privacy classification;
- authority level;
- validation state;
- source availability;
- provenance sufficiency;
- relationship status;
- review state;
- approval scope;
- storage area;
- implementation context;
- risk level;
- prior escalation outcome;
- time limit;
- permission profile;
- future governed specification.

A permission grant MUST NOT be broader than necessary for the intended action.

A permission profile SHOULD use the least permission needed for the agent’s role, task, workflow stage, implementation context, and risk level.

A permission grant SHOULD be narrower when an action may affect:

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
- implementation behavior.

A role does not automatically grant permission.

A Syntax Inspector role does not automatically have write permission.

A Standards Validator role does not automatically have approval authority.

A Metadata Agent role does not automatically have permission to change metadata.

A Relationship Agent role does not automatically have permission to approve relationships.

A Source and Provenance Agent role does not automatically have permission to expose restricted sources.

A Privacy Agent role does not automatically have permission to downgrade Privacy Classification.

A Workflow Agent role does not automatically have permission to transition Lifecycle State.

A Duplicate and Identity Agent role does not automatically have permission to merge, split, redirect, supersede, or delete Object Identity.

A Handoff Agent role does not automatically have permission to expose restricted context.

An Implementation Agent role does not automatically have permission to redefine standards through implementation behavior.

Agent permissions SHALL remain distinguishable from agent outputs.

An agent may produce:

- findings;
- warnings;
- recommendations;
- proposed metadata;
- proposed relationships;
- proposed Source References;
- proposed provenance records;
- proposed lifecycle states;
- proposed authority levels;
- proposed privacy classifications;
- validation findings;
- draft Knowledge Records;
- draft governed documents;
- movement recommendations;
- implementation-support outputs;
- handoff notes;
- escalation notes.

Such outputs remain agent outputs unless reviewed, accepted, approved, validated, routed, or otherwise handled through a governed workflow or future specification.

Agent permissions SHALL remain distinguishable from approval.

Permission allows an action within scope.

Approval accepts a governed entity, change, output, decision, or use within an approval scope.

An agent may be permitted to propose a change without being permitted to approve the change.

An agent may be permitted to draft a record without being permitted to publish the record.

An agent may be permitted to validate structure without being permitted to accept the validation result as final.

An agent may be permitted to move a file within a staging area without being permitted to change Object Identity, Lifecycle State, Privacy Classification, Authority Level, or publication status.

Agent permissions SHALL remain distinguishable from traceability.

Traceability records what happened or preserves accountability context.

Traceability does not make an action permitted if permission was absent.

Traceability does not approve an action.

Traceability does not validate an action by itself.

Traceability does not authorize downstream use by itself.

An unpermitted action remains non-conforming even if it was logged.

A logged output remains an agent output unless a governed review, approval, validation, workflow, or future specification gives it another status within a defined scope.

The Agent Permission Model SHALL support proportional traceability.

Low-risk read operations MAY require lighter records where they do not expose restricted material, affect governed meaning, produce governed output, change storage placement, modify metadata, alter relationships, create Source References, affect provenance, change Lifecycle State, affect Authority Level, affect Privacy Classification, affect Validation, trigger publication, trigger export, support migration, delete material, or affect downstream use.

High-risk operations SHALL require stronger traceability, review, and escalation handling.

Restricted operations SHALL require explicit permission before execution unless a governed emergency, repair, quarantine, or exception process explicitly defines otherwise.

The Agent Permission Model SHALL preserve privacy.

Permission records, activity records, traceability records, review records, approval records, escalation records, logs, reports, and handoff outputs MUST NOT expose restricted material beyond the permitted scope.

Where restricted material is involved, a record SHOULD identify that restricted material exists, what privacy boundary applies, what review is required, and what escalation is needed without unnecessarily revealing restricted content.

The Agent Permission Model SHALL preserve implementation independence.

A compliant implementation MAY use filesystem permissions, repository permissions, application roles, database privileges, workflow queues, prompt constraints, configuration files, access-control systems, scripts, validators, or tool settings to support agent permissions.

Those implementation mechanisms do not define standard permission by themselves.

Permission meaning MUST remain explicit, portable, inspectable, reviewable, and governed by The Brain Standard, applicable standards, applicable workflows, applicable specifications, or future implementation profiles.

The Agent Permission Model is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, and governance processes can determine:

- whether an agent action was permitted;
- what permission scope applied;
- what constraints applied;
- what material was affected;
- what output was produced;
- what traceability exists;
- what review was required;
- what approval was or was not granted;
- what escalation occurred or remains required;
- what privacy boundary applied;
- whether the action preserved governed meaning;
- whether the action remained within AG-0001 boundaries and AG-0002 role responsibilities.

## 4. Permission Profiles

Permission Profiles define reusable permission patterns that may be assigned to agents, roles, subagents, workflows, implementation processes, tools, scripts, or future automated actors within a governed scope.

A Permission Profile exists so agent permissions can be applied consistently without allowing broad access, tool capability, implementation visibility, or role responsibility to become unrestricted permission.

A Permission Profile SHALL define a bounded set of allowed, conditional, restricted, or prohibited actions.

A Permission Profile MUST remain subordinate to:

- AG-0001 — Agent Operating Boundaries Standard;
- AG-0002 — Agent Role and Responsibility Standard;
- the applicable Knowledge Standards;
- the applicable Storage Standards;
- the applicable Workflow Standards;
- applicable Privacy Classification;
- applicable Authority Level;
- applicable Lifecycle State;
- applicable Validation State;
- applicable governance requirements.

A Permission Profile MUST NOT grant authority merely because it grants action permission.

A Permission Profile MUST NOT grant approval merely because it grants proposal, drafting, validation-support, write, movement, or implementation-support permission.

A Permission Profile MUST NOT override Privacy Classification.

A Permission Profile MUST NOT override Authority Level.

A Permission Profile MUST NOT transition Lifecycle State by itself.

A Permission Profile MUST NOT create Validation State by itself.

A Permission Profile MUST NOT make an agent output approved, authoritative, published, exportable, migratable, deletable, or safe for downstream use by itself.

A Permission Profile SHOULD identify:

- the profile name;
- the profile purpose;
- the agent, role, subagent, workflow, implementation, tool, script, or process that may use the profile;
- the allowed action categories;
- the prohibited action categories;
- the conditional action categories;
- the governed entities or storage areas within scope;
- the privacy boundaries that apply;
- the authority boundaries that apply;
- the lifecycle boundaries that apply;
- the validation boundaries that apply;
- the workflow context that applies;
- the implementation context that applies;
- the traceability requirements that apply;
- the review requirements that apply;
- the escalation requirements that apply;
- the expiration or revocation conditions that apply.

A Permission Profile MAY be broad enough to support repeated work, but it MUST remain narrow enough to prevent uncontrolled action.

A Permission Profile MAY support one agent role.

A Permission Profile MAY support multiple agent roles.

A Permission Profile MAY support a workflow stage.

A Permission Profile MAY support an implementation-support process.

A Permission Profile MAY support a future agent specification.

A Permission Profile MUST NOT silently inherit across unrelated scopes.

Permission granted for one Knowledge Object does not grant permission for every Knowledge Object.

Permission granted for one Source Material set does not grant permission for every Source Material set.

Permission granted for one storage area does not grant permission for every storage area.

Permission granted for one workflow stage does not grant permission for every workflow stage.

Permission granted for draft material does not grant permission for approved material.

Permission granted for proposal does not grant permission for write.

Permission granted for write does not grant permission for approval.

Permission granted for validation support does not grant permission for validation acceptance.

Permission granted for export preparation does not grant permission for export release.

Permission granted for migration preparation does not grant permission for migration completion.

Permission granted for deletion recommendation does not grant permission for deletion.

At minimum, The Brain Standard recognizes the following conceptual Permission Profile types:

- no-access profile;
- read-only profile;
- read-and-summarize profile;
- extraction-support profile;
- proposal-only profile;
- validation-support profile;
- drafting-support profile;
- bounded-write profile;
- bounded-move profile;
- implementation-support profile;
- workflow-support profile;
- escalation-only profile;
- high-risk restricted profile;
- future governed permission profiles.

A no-access profile denies agent interaction with a governed scope.

A read-only profile permits inspection without modification.

A read-and-summarize profile permits bounded summaries where privacy allows.

An extraction-support profile permits bounded extraction where source distinction and provenance are preserved.

A proposal-only profile permits recommendations without applying changes.

A validation-support profile permits validation findings without final validation acceptance.

A drafting-support profile permits draft creation without approval.

A bounded-write profile permits limited changes within an explicit scope.

A bounded-move profile permits limited storage movement within an explicit scope.

An implementation-support profile permits practical setup, scripting, templating, configuration, or validator support without redefining the standard.

A workflow-support profile permits routing, reporting, preparation, and escalation within workflow boundaries.

An escalation-only profile permits issue identification and routing without broader action permission.

A high-risk restricted profile may permit sensitive actions only with explicit scope, traceability, review, and escalation controls.

A future governed Permission Profile MAY define more exact permission behavior.

Such profiles are valid only when they preserve the distinction between permission, access, role responsibility, authority, approval, privacy clearance, lifecycle transition, validation acceptance, publication permission, export permission, migration permission, deletion permission, downstream-use permission, and governance acceptance.

A Permission Profile SHOULD require stronger traceability where the profile allows activity that may affect:

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
- implementation behavior.

Permission Profiles SHOULD remain reviewable.

A reviewer SHOULD be able to determine:

- what profile applied;
- what scope applied;
- what actions were allowed;
- what actions were prohibited;
- what conditions applied;
- what agent activity occurred;
- what output was produced;
- what traceability exists;
- what review is required;
- what escalation is required;
- whether the profile remained valid.

A Permission Profile MAY be revoked, suspended, narrowed, superseded, deprecated, expired, or replaced through a governed process.

An agent MUST NOT continue operating under a revoked, expired, superseded, rejected, or invalid Permission Profile.

Permission Profiles are successful when humans, agents, workflows, validators, storage systems, implementations, and governance processes can determine what an agent was allowed to do, what it was not allowed to do, what scope applied, what traceability is required, and whether the profile preserved The Brain Standard.

## 5. Read Permission Requirements

Read Permission Requirements define when and how an agent may inspect, open, search, parse, view, summarize, extract from, classify, index for permitted review, or otherwise consume governed material without directly modifying the governed entity.

Read permission exists because even non-writing agent activity can affect privacy, provenance, traceability, review, validation, source interpretation, downstream use, and implementation behavior.

Read permission is not harmless by default.

A read operation may expose restricted material.

A read operation may create summaries.

A read operation may create logs.

A read operation may create extracted content.

A read operation may influence metadata proposals, relationship proposals, Source Reference proposals, provenance proposals, validation findings, workflow routing, implementation behavior, publication preparation, export preparation, migration preparation, or downstream use.

An agent MAY read governed material only when the read operation is allowed by the applicable permission scope.

A Read Permission SHOULD identify:

- what agent, role, subagent, workflow, implementation, tool, script, or process may read;
- what governed entity, Source Material set, Knowledge Record, storage area, workflow context, or implementation context may be read;
- what purpose the read operation supports;
- what privacy boundary applies;
- what authority boundary applies where applicable;
- what lifecycle boundary applies where applicable;
- what validation boundary applies where applicable;
- whether summarization is allowed;
- whether extraction is allowed;
- whether indexing, caching, embedding, or generated-file creation is allowed;
- whether read activity must be recorded;
- whether output traceability is required;
- whether human review is required;
- whether escalation is required.

A Read Permission MUST respect Privacy Classification.

An agent MUST NOT read restricted material unless the applicable privacy boundary permits agent access within the defined scope.

An agent MUST NOT expose restricted material through summaries, extracted content, metadata proposals, relationship proposals, Source References, provenance records, validation findings, logs, prompts, indexes, embeddings, caches, generated files, exports, publication drafts, migration packages, implementation displays, or downstream outputs unless the applicable privacy boundary permits that exposure.

Read permission is not permission to summarize unless summarization is included or implied within the governed scope.

Read permission is not permission to extract unless extraction is included or implied within the governed scope.

Read permission is not permission to index, cache, embed, vectorize, or generate derived files unless that behavior is included or implied within the governed scope.

Read permission is not permission to publish.

Read permission is not permission to export.

Read permission is not permission to migrate.

Read permission is not permission to write.

Read permission is not permission to approve.

Read permission is not permission to change metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, Object Identity, storage location, or downstream-use status.

Read operations SHOULD preserve source distinction.

An agent MUST NOT treat Source Material as a Knowledge Record merely because it can read both.

An agent MUST NOT treat an agent summary as Source Material.

An agent MUST NOT treat extracted content as a complete or final representation of Source Material unless a governed specification or review process explicitly supports that interpretation.

Read operations SHOULD preserve Object Identity where the read output refers to existing Knowledge Objects or Knowledge Records.

An agent SHOULD identify the stable Object Identity where available rather than relying only on filename, title, folder path, storage location, tag, search result, backlink, graph position, implementation-specific identifier, or model memory.

Read operations SHOULD preserve provenance where the read output affects:

- interpretation;
- metadata;
- relationships;
- Source References;
- provenance records;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- review;
- publication;
- export;
- migration;
- deletion;
- downstream use;
- governance.

A Read Activity Record MAY be lightweight when the read operation is low-risk, does not expose restricted material, does not produce governed output, does not affect review, does not affect validation, does not affect workflow routing, and does not affect downstream use.

A Read Activity Record SHOULD be stronger when the read operation affects governed meaning, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, or downstream use.

A Read Activity Record SHOULD identify or support identification of:

- what agent read the material;
- what permission scope applied;
- what material was read;
- what material was not read where that limitation affects the output;
- why the material was read;
- what output was produced;
- what source support was used;
- what assumptions were made;
- what uncertainty remains;
- what privacy boundary applies;
- what review is required;
- what escalation is required.

Read operations SHOULD be escalated when:

- Privacy Classification is missing, conflicting, or unclear;
- read access is uncertain;
- restricted material may be exposed;
- the agent cannot determine whether summarization or extraction is permitted;
- the agent detects source uncertainty;
- the agent detects Object Identity ambiguity;
- the agent detects relationship ambiguity;
- the agent detects provenance gaps;
- the agent detects authority conflict;
- the agent detects validation risk;
- the agent detects lifecycle ambiguity;
- the read operation may affect publication, export, migration, deletion, or downstream use.

A read operation MUST remain distinguishable from review completion.

An agent may inspect material.

Inspection is not approval.

An agent may summarize material.

Summary is not approval.

An agent may extract material.

Extraction is not approval.

An agent may classify material.

Classification is not approval.

An agent may identify risks.

Risk identification is not final governance action.

Read Permission Requirements are successful when agents can inspect and understand governed material without expanding access, exposing restricted content, weakening source distinction, creating hidden authority, bypassing review, or turning technical visibility into governed permission.

## 6. Proposal Permission Requirements

Proposal Permission Requirements define when and how an agent may recommend, suggest, draft, classify, flag, prepare, or otherwise propose a governed action without making that action final.

Proposal permission exists because agents are often most useful when they identify possible improvements, corrections, classifications, relationships, Source References, provenance, lifecycle states, authority handling, privacy handling, validation findings, workflow routing, storage movement, publication preparation, export preparation, migration preparation, or implementation-support actions.

A proposal is not an applied change.

A proposal is not approval.

A proposal is not authority.

A proposal is not validation acceptance.

A proposal is not privacy clearance.

A proposal is not lifecycle transition.

A proposal is not publication permission.

A proposal is not export permission.

A proposal is not migration permission.

A proposal is not deletion permission.

A proposal is not downstream-use permission.

A proposal is not governance acceptance.

An agent MAY propose a governed action only when proposal activity is allowed by the applicable permission scope.

A Proposal Permission SHOULD identify:

- what agent, role, subagent, workflow, implementation, tool, script, or process may propose;
- what proposal type is allowed;
- what governed entity or storage area may be affected;
- what source material or evidence may be used;
- what output form is expected;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies;
- what validation boundary applies;
- what review is required;
- what escalation is required;
- what traceability is required;
- whether the proposal may be stored;
- whether the proposal may be routed to another agent, workflow, reviewer, implementation, or downstream process.

An agent MAY propose:

- metadata;
- relationships;
- Source References;
- provenance records;
- lifecycle states;
- authority-related handling;
- privacy classifications;
- validation findings;
- repair actions;
- Knowledge Record drafts;
- governed document drafts;
- storage movement;
- import mappings;
- export packages;
- migration mappings;
- publication drafts;
- deletion recommendations;
- archive recommendations;
- quarantine recommendations;
- workflow routing;
- implementation-support actions;
- escalation actions;
- future governed actions.

A proposal MUST remain distinguishable from an approved governed change.

A metadata proposal is not approved metadata.

A relationship proposal is not an approved relationship.

A Source Reference proposal is not an approved Source Reference.

A provenance proposal is not sufficient provenance by itself.

A lifecycle proposal is not a Lifecycle State transition.

An authority proposal is not Authority Level assignment.

A privacy proposal is not Privacy Classification assignment.

A validation finding is not validation acceptance.

A repair proposal is not an applied repair.

A storage movement proposal is not movement authorization.

An export proposal is not export approval.

A publication proposal is not publication approval.

A migration proposal is not migration approval.

A deletion proposal is not deletion authorization.

A workflow proposal is not workflow completion.

An implementation proposal is not standard-level meaning.

A Proposal Permission MUST preserve reviewability.

A proposal SHOULD identify:

- what is being proposed;
- why it is being proposed;
- what evidence, source, standard, workflow, validation result, reasoning, or prior decision supports it where applicable;
- what uncertainty exists;
- what assumptions were made;
- what was inspected;
- what was not inspected where that limitation matters;
- what privacy boundary applies;
- what role or workflow should review it;
- whether the proposal affects governed meaning;
- whether the proposal affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, downstream use, governance, or implementation behavior.

A Proposal Permission MUST preserve privacy.

An agent MUST NOT expose restricted material in a proposal unless the recipient, storage location, workflow, implementation, reviewer, export, publication context, migration context, or downstream-use context is authorized to receive it.

Where restricted material supports a proposal, the proposal SHOULD preserve enough safe context for authorized review without unnecessarily exposing restricted content.

A Proposal Permission MUST preserve source and provenance boundaries.

An agent MUST NOT fabricate source support.

An agent MUST NOT fabricate provenance.

An agent MUST NOT treat a citation-like reference as sufficient Source Reference behavior unless the reference remains traceable, reviewable, and compatible with the applicable Source Reference and Provenance Standard.

A Proposal Permission MUST preserve Object Identity.

An agent MAY propose that Object Identity requires review.

An agent MAY identify duplicate risk, merge candidates, split candidates, redirect candidates, supersession candidates, or identity conflicts.

An agent MUST NOT silently create, merge, split, redirect, supersede, delete, or reassign Object Identity through a proposal.

A Proposal Permission SHOULD preserve proportional traceability.

Low-risk proposals MAY require lighter traceability where they do not affect governed meaning, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, or downstream use.

High-risk proposals SHALL require stronger traceability.

High-risk proposals include proposals that may affect:

- Object Identity;
- metadata required for validity;
- relationships required for interpretation;
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
- implementation behavior.

A Proposal Activity Record SHOULD identify or support identification of:

- what agent produced the proposal;
- what permission scope applied;
- what governed entity was affected;
- what proposal type was produced;
- what source material, evidence, standard, workflow, or reasoning supported the proposal where applicable;
- what assumptions were made;
- what uncertainty remains;
- what privacy boundary applies;
- what review is required;
- what escalation is required;
- whether the proposal was accepted, rejected, revised, deferred, escalated, superseded, archived, or left pending.

An agent SHOULD escalate proposal activity when:

- the proposal affects Object Identity;
- the proposal affects Privacy Classification;
- the proposal affects Authority Level;
- the proposal affects Lifecycle State;
- the proposal affects Validation State;
- the proposal affects publication, export, migration, deletion, or downstream use;
- the proposal depends on uncertain source support;
- the proposal depends on missing or weak provenance;
- the proposal would expose restricted material;
- the proposal conflicts with a higher-authority standard;
- the proposal requires human judgment;
- the proposal exceeds the agent’s role, permission, workflow, privacy, validation, authority, or implementation scope.

Proposal Permission Requirements are successful when agents can provide useful recommendations without silently applying changes, creating approval, weakening privacy, fabricating support, collapsing review boundaries, or converting agent output into governed meaning by accident.

## 7. Write and Edit Permission Requirements

Write and Edit Permission Requirements define when and how an agent may modify, revise, annotate, enrich, correct, restructure, replace, or otherwise alter governed material within a defined permission scope.

Write and edit permission exists because agent-generated changes may affect governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, downstream use, governance, and implementation behavior.

Write permission is higher-risk than read permission.

Edit permission is higher-risk than proposal permission.

A proposal identifies a possible change.

A write or edit operation applies a change.

An agent MAY write to or edit governed material only when the action is allowed by the applicable permission scope.

A Write or Edit Permission SHOULD identify:

- what agent, role, subagent, workflow, implementation, tool, script, or process may write or edit;
- what governed entity, file, record, storage area, workflow output, implementation artifact, or generated material may be changed;
- what type of change is allowed;
- what type of change is prohibited;
- whether the change is reversible;
- whether the change affects governed meaning;
- whether the change affects Object Identity;
- whether the change affects metadata;
- whether the change affects relationships;
- whether the change affects Source References;
- whether the change affects provenance;
- whether the change affects Lifecycle State;
- whether the change affects Authority Level;
- whether the change affects Privacy Classification;
- whether the change affects Validation State;
- whether the change affects publication, export, migration, deletion, or downstream use;
- what review is required before or after the change;
- what traceability is required;
- what escalation is required.

A Write or Edit Permission MUST preserve Object Identity.

An agent MUST NOT silently create, remove, merge, split, redirect, supersede, delete, reassign, or reinterpret Object Identity through a write or edit operation unless a governed workflow or future specification explicitly permits that action within scope.

A Write or Edit Permission MUST preserve source and provenance boundaries.

An agent MUST NOT fabricate Source References.

An agent MUST NOT fabricate provenance.

An agent MUST NOT remove Source References or provenance merely to simplify a record.

An agent MUST NOT weaken source traceability where source traceability affects meaning, authority, privacy, validation, publication, export, migration, governance, or downstream use.

A Write or Edit Permission MUST preserve Privacy Classification.

An agent MUST NOT write restricted material into an unrestricted location, unrestricted output, unrestricted log, unrestricted cache, unrestricted index, unrestricted export, unrestricted publication draft, unrestricted migration package, or unrestricted implementation display.

An agent MUST NOT lower, remove, bypass, or reinterpret Privacy Classification through a write or edit operation unless a governed privacy process explicitly permits that change within scope.

A Write or Edit Permission MUST preserve review boundaries.

An agent MAY be permitted to edit draft material without being permitted to edit approved material.

An agent MAY be permitted to correct syntax without being permitted to change governed meaning.

An agent MAY be permitted to update implementation-support material without being permitted to update the governing standard.

An agent MAY be permitted to apply a reversible repair without being permitted to apply an irreversible repair.

An agent MAY be permitted to make a bounded edit without being permitted to approve the edited material.

A write or edit operation MUST NOT be treated as approval by itself.

A write or edit operation MUST NOT be treated as validation acceptance by itself.

A write or edit operation MUST NOT be treated as Authority Level assignment by itself.

A write or edit operation MUST NOT be treated as Privacy Classification approval by itself.

A write or edit operation MUST NOT be treated as Lifecycle State transition by itself.

A write or edit operation MUST NOT be treated as publication permission by itself.

A write or edit operation MUST NOT be treated as export permission by itself.

A write or edit operation MUST NOT be treated as migration permission by itself.

A write or edit operation MUST NOT be treated as downstream-use permission by itself.

Write and edit operations SHOULD be reversible where practical.

Where reversibility is not practical, stronger permission, traceability, review, and escalation requirements SHOULD apply.

A Write or Edit Activity Record SHOULD identify or support identification of:

- what agent performed or proposed the write or edit operation;
- what permission scope applied;
- what governed entity was changed;
- what content, metadata, relationship, Source Reference, provenance, workflow output, implementation artifact, or storage representation was changed;
- what prior state existed where practical;
- what new state exists;
- what source, evidence, rule, workflow, validation result, or human instruction supported the change;
- what assumptions were made;
- what uncertainty remains;
- whether the change was proposed, applied, rejected, reverted, superseded, approved, archived, or escalated;
- what privacy boundary applies;
- what review is required;
- what escalation is required.

An agent SHOULD escalate write or edit activity when:

- the permission scope is unclear;
- the target material is approved, authoritative, restricted, archived, superseded, deprecated, validation-sensitive, publication-sensitive, export-sensitive, migration-sensitive, or downstream-use-sensitive;
- the edit may affect Object Identity;
- the edit may affect Privacy Classification;
- the edit may affect Authority Level;
- the edit may affect Lifecycle State;
- the edit may affect Validation State;
- the edit may affect Source References or provenance;
- the edit may affect relationships;
- the edit may affect publication, export, migration, deletion, or downstream use;
- the edit may expose restricted material;
- the edit conflicts with a higher-authority standard;
- the edit requires human judgment.

Write and Edit Permission Requirements are successful when agents can apply bounded changes without silently rewriting governed meaning, weakening provenance, exposing restricted content, bypassing review, expanding authority, or converting applied changes into approval by accident.

## 8. Move and Storage Permission Requirements

Move and Storage Permission Requirements define when and how an agent may recommend, prepare, or perform changes to the storage location, storage grouping, storage representation, staging area, archive area, backup area, import area, export area, migration area, implementation-support area, workflow-support area, index area, cache area, or generated-file area of governed material.

Move and storage permission exists because storage actions can affect discoverability, source traceability, provenance, relationship integrity, validation, privacy, workflow routing, archive behavior, backup behavior, import behavior, export behavior, migration behavior, implementation behavior, and downstream use.

Storage movement is not knowledge meaning.

Storage placement is not Object Identity.

Storage placement is not Lifecycle State.

Storage placement is not Authority Level.

Storage placement is not Privacy Classification.

Storage placement is not Validation State.

Storage placement is not approval.

Storage placement is not publication permission.

Storage placement is not export permission.

Storage placement is not migration permission.

Storage placement is not deletion permission.

An agent MAY move, stage, organize, copy, route, archive, prepare, or otherwise change storage handling only when the action is allowed by the applicable permission scope.

A Move or Storage Permission SHOULD identify:

- what agent, role, subagent, workflow, implementation, tool, script, or process may perform or recommend the storage action;
- what governed entity or stored representation may be moved or organized;
- what source location is involved;
- what destination location is involved;
- whether the movement is temporary, draft, review-related, approved, archival, backup-related, import-related, export-related, migration-related, implementation-supporting, workflow-supporting, generated, cached, indexed, or permanent;
- whether copying is allowed;
- whether deletion of the prior representation is allowed;
- whether references must be updated;
- whether validation must occur before or after movement;
- whether privacy review is required;
- whether human review is required;
- what traceability is required;
- what escalation is required.

A Move or Storage Permission MUST preserve the distinction between:

- Source Material;
- Knowledge Records;
- governed documents;
- drafts;
- review material;
- approved material;
- working material;
- implementation-support material;
- workflow-support material;
- agent-support material;
- assets;
- indexes;
- caches;
- generated files;
- archives;
- backups;
- imports;
- exports;
- migrations;
- future governed storage categories.

An agent MUST NOT treat movement from one storage area to another as a change in governed meaning unless a governed standard, workflow, or future specification explicitly defines that effect within scope.

An agent MUST NOT use folder placement, filename, vault path, repository path, database location, archive location, backup location, import location, export location, migration location, index location, cache location, generated-file location, implementation workspace, tag, sort order, graph position, or search result as the sole source of governed meaning.

A Move or Storage Permission MUST preserve Object Identity.

An agent MUST NOT create identity confusion through movement, copying, renaming, staging, archiving, backup, import, export, migration, indexing, caching, or generated-file handling.

Where storage movement changes paths, filenames, references, links, indexes, caches, exports, imports, migration maps, or implementation behavior, the movement SHOULD preserve or update references needed for review, validation, recovery, provenance, source traceability, and downstream interpretation.

A Move or Storage Permission MUST preserve Privacy Classification.

An agent MUST NOT move restricted material into an unrestricted area.

An agent MUST NOT copy restricted material into an unrestricted cache, index, generated-file area, export package, publication draft, migration package, backup, implementation display, or downstream system unless the applicable privacy boundary permits that action.

A Move or Storage Permission MUST preserve validation expectations.

An agent MUST NOT treat successful movement as validation success.

An agent MUST NOT treat storage placement in a valid-looking area as proof that the material is valid.

An agent MUST NOT treat storage placement in an approved-looking area as proof that the material is approved.

An agent MUST NOT treat storage placement in an archive area as proof that the material is deprecated, superseded, deleted, or no longer governed unless a governed lifecycle rule defines that effect.

Move and storage operations SHOULD be reversible where practical.

Where reversibility is not practical, stronger permission, traceability, review, and escalation requirements SHOULD apply.

A Move or Storage Activity Record SHOULD identify or support identification of:

- what agent performed or recommended the movement;
- what permission scope applied;
- what governed entity or stored representation was moved;
- what source location was involved;
- what destination location was involved;
- whether copying, renaming, indexing, caching, archiving, backup, import preparation, export preparation, or migration preparation occurred;
- what references were preserved or updated;
- what validation occurred;
- what privacy boundary applied;
- what review occurred or remains required;
- what escalation occurred or remains required;
- what unresolved risk remains.

An agent SHOULD escalate move or storage activity when:

- the source or destination scope is unclear;
- movement may affect Object Identity;
- movement may affect Source References or provenance;
- movement may affect relationships;
- movement may affect Lifecycle State interpretation;
- movement may affect Authority Level interpretation;
- movement may affect Privacy Classification;
- movement may affect Validation State;
- movement may affect publication, export, migration, deletion, or downstream use;
- movement may expose restricted material;
- movement may break links, references, indexes, caches, archives, backups, imports, exports, migrations, or implementation behavior;
- movement conflicts with the Storage Architecture Standard or Storage Layout Specification;
- movement requires human judgment.

Move and Storage Permission Requirements are successful when agents can organize stored material without allowing storage behavior to redefine knowledge meaning, weaken privacy, break traceability, create identity confusion, bypass validation, or silently complete workflow or lifecycle actions.

## 9. Validation Permission Requirements

Validation Permission Requirements define when and how an agent may inspect, test, compare, report, classify, or otherwise support validation of governed material, agent activity, agent output, permission use, storage handling, workflow handling, implementation behavior, import preparation, export preparation, migration preparation, publication preparation, or downstream-use preparation.

Validation permission exists because agents may help determine whether material appears to satisfy a defined validation scope without becoming the final authority for approval, truth, lifecycle transition, privacy clearance, publication readiness, export readiness, migration readiness, deletion permission, downstream-use permission, or governance acceptance.

Validation support is not approval.

Validation support is not Authority Level.

Validation support is not Privacy Classification.

Validation support is not Lifecycle State transition.

Validation support is not publication permission.

Validation support is not export permission.

Validation support is not migration permission.

Validation support is not deletion permission.

Validation support is not downstream-use permission.

Validation support is not governance acceptance.

An agent MAY perform validation support only when validation activity is allowed by the applicable permission scope.

A Validation Permission SHOULD identify:

- what agent, role, subagent, workflow, implementation, tool, script, validator, or process may validate;
- what governed entity, output, record, storage area, workflow result, implementation artifact, import package, export package, migration package, publication candidate, or downstream-use candidate may be inspected;
- what validation scope applies;
- what standards, specifications, workflows, schemas, rules, templates, or criteria may be applied;
- what standards, specifications, workflows, schemas, rules, templates, or criteria are outside scope;
- what validation output may be produced;
- whether validation findings may be stored;
- whether validation findings may be routed;
- whether validation findings may block further action;
- whether validation findings may trigger escalation;
- whether human review is required;
- what traceability is required;
- what privacy boundary applies.

A Validation Permission MUST preserve validation scope.

A validation result that checks one concern MUST NOT imply that every concern has been checked.

A syntax validation result does not imply standards conformance.

A standards validation result does not imply approval.

A metadata validation result does not imply relationship validation.

A relationship validation result does not imply source-reference validation.

A source-reference validation result does not imply provenance sufficiency.

A privacy validation result does not imply publication approval.

An authority validation result does not imply Authority Level assignment.

A lifecycle validation result does not imply lifecycle transition.

A storage validation result does not imply knowledge validity.

An implementation validation result does not imply standard-level approval.

An export validation result does not imply export release.

A migration validation result does not imply migration completion.

A publication validation result does not imply publication approval.

A downstream-use validation result does not imply unrestricted downstream use.

A Validation Permission MUST preserve privacy.

An agent MUST NOT expose restricted material in validation findings unless the reviewer, workflow, implementation, export context, migration context, publication context, or downstream-use context is authorized to receive that information.

Where validation requires restricted evidence, the validation output SHOULD preserve enough safe context for authorized review without unnecessarily exposing restricted material.

A Validation Permission MUST preserve source and provenance expectations.

An agent MUST NOT treat unsupported claims as validated merely because the structure is valid.

An agent MUST NOT treat a present citation as sufficient Source Reference behavior unless the applicable source-reference requirements are satisfied.

An agent MUST NOT treat a present provenance note as sufficient provenance unless the applicable provenance requirements are satisfied.

A Validation Permission MUST preserve role and permission boundaries.

A Standards Validator role does not automatically have permission to validate every file, record, workflow output, implementation artifact, import package, export package, migration package, publication candidate, or downstream-use candidate.

A validation-support permission does not grant write permission.

A validation-support permission does not grant move permission.

A validation-support permission does not grant approval permission.

A validation-support permission does not grant publication, export, migration, deletion, or downstream-use permission.

A validation finding MAY recommend repair.

A validation finding MAY recommend escalation.

A validation finding MAY recommend review.

A validation finding MAY block further action only where the applicable workflow, permission profile, specification, or governance process permits blocking behavior within scope.

A Validation Activity Record SHOULD identify or support identification of:

- what agent performed the validation;
- what permission scope applied;
- what validation scope applied;
- what governed entity or output was inspected;
- what standards, specifications, workflows, rules, templates, or criteria were applied;
- what was not validated where that limitation affects interpretation;
- what evidence was used;
- what validation findings were produced;
- whether findings are errors, warnings, recommendations, informational notes, blocked actions, or escalations;
- what uncertainty remains;
- what privacy boundary applies;
- what review is required;
- what escalation is required;
- what downstream use is permitted or prohibited.

An agent SHOULD escalate validation activity when:

- validation scope is unclear;
- required evidence is missing;
- validation findings conflict;
- validation depends on restricted material;
- validation may affect Object Identity;
- validation may affect metadata;
- validation may affect relationships;
- validation may affect Source References;
- validation may affect provenance;
- validation may affect Lifecycle State;
- validation may affect Authority Level;
- validation may affect Privacy Classification;
- validation may affect publication, export, migration, deletion, or downstream use;
- validation failure would require repair;
- validation success may be misread as approval;
- the agent lacks permission to complete the needed validation;
- human judgment is required.

Validation Permission Requirements are successful when agents can support conformance checking and risk detection without converting scoped validation findings into approval, authority, privacy clearance, lifecycle transition, publication approval, export approval, migration approval, deletion authorization, downstream-use permission, or governance acceptance.

## 10. Creation Permission Requirements

Creation Permission Requirements define when and how an agent may create new governed material, draft material, proposed Knowledge Records, governed documents, workflow outputs, implementation-support material, validation-support material, traceability records, reports, templates, generated files, or other new artifacts within The Brain Standard.

Creation permission exists because creating new material can affect governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, downstream use, governance, and implementation behavior.

Creation is not approval.

Creation is not authority.

Creation is not validation acceptance.

Creation is not Lifecycle State transition.

Creation is not Privacy Classification approval.

Creation is not publication permission.

Creation is not export permission.

Creation is not migration permission.

Creation is not downstream-use permission.

An agent MAY create governed material only when creation activity is allowed by the applicable permission scope.

A Creation Permission SHOULD identify:

- what agent, role, subagent, workflow, implementation, tool, script, or process may create material;
- what type of material may be created;
- what governed entity or storage area may receive the created material;
- what source material may be used;
- what metadata is required;
- what Source References are required where applicable;
- what provenance is required;
- what relationship handling is required;
- what Privacy Classification applies;
- what Authority Level may or may not apply;
- what Lifecycle State applies;
- what Validation State applies;
- whether the created material is draft, proposed, generated, reviewed, approved, implementation-supporting, workflow-supporting, temporary, or final within a defined scope;
- what review is required;
- what traceability is required;
- what escalation is required.

An agent-created item MUST remain distinguishable from approved governed material unless a governed workflow or future specification explicitly defines a controlled approval path.

An agent-created Knowledge Record draft is not an approved Knowledge Record.

An agent-created governed document draft is not an approved standard.

An agent-created metadata record is not approved metadata by itself.

An agent-created relationship is not an approved relationship by itself.

An agent-created Source Reference is not an approved Source Reference by itself.

An agent-created provenance note is not sufficient provenance by itself unless it satisfies the applicable provenance requirements and review expectations.

An agent-created validation finding is not validation acceptance by itself.

An agent-created implementation-support file is not standard-level meaning by itself.

An agent-created workflow output is not workflow approval by itself.

A Creation Permission MUST preserve Object Identity.

An agent MAY create a draft candidate for a new Knowledge Object where permitted.

An agent MAY propose that a new Object Identity is needed where permitted.

An agent MUST NOT silently assign final Object Identity where Object Identity affects relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, or downstream use.

An agent MUST NOT create duplicate Knowledge Objects merely because material is renamed, moved, summarized, reformatted, copied, imported, restored, indexed, cached, generated, or displayed differently.

A Creation Permission MUST preserve source and provenance boundaries.

An agent MUST NOT fabricate Source References.

An agent MUST NOT fabricate provenance.

An agent MUST NOT create source-supported material without preserving enough source context for review.

An agent MUST NOT treat generated material as Source Material merely because it was derived from Source Material.

An agent MUST NOT treat generated material as authoritative merely because it is complete, plausible, useful, repeated, model-confident, validated by a tool, or stored in a governed location.

A Creation Permission MUST preserve Privacy Classification.

An agent MUST NOT create unrestricted material from restricted material unless the applicable privacy boundary permits that transformation and exposure.

An agent MUST NOT create summaries, indexes, caches, embeddings, generated files, reports, handoff notes, export packages, publication drafts, migration packages, or implementation displays that expose restricted material beyond the permitted scope.

Where created material depends on restricted material, the created material SHOULD preserve the applicable privacy boundary or identify that restricted support exists without unnecessarily exposing restricted content.

A Creation Permission SHOULD preserve minimum required metadata.

Created material SHOULD identify or support identification of:

- what created material exists;
- what agent created it;
- what permission scope applied;
- what source material or governed entity was used where applicable;
- what purpose the material serves;
- whether the material is draft, proposed, generated, reviewed, approved, rejected, superseded, archived, temporary, or pending review;
- what privacy boundary applies;
- what review is required;
- what escalation is required;
- what downstream use is permitted or prohibited.

Agent-created material SHOULD be stored only where the applicable storage standard, storage layout, workflow, implementation profile, permission scope, and privacy boundary allow.

Storage location MUST NOT cause agent-created material to become approved, authoritative, validated, published, exportable, migratable, deletable, or safe for downstream use by itself.

An agent SHOULD escalate creation activity when:

- the creation permission scope is unclear;
- the created material may become confused with approved governed material;
- the created material may affect Object Identity;
- the created material may affect metadata, relationships, Source References, or provenance;
- the created material may affect Lifecycle State, Authority Level, Privacy Classification, or Validation State;
- the created material may affect publication, export, migration, deletion, or downstream use;
- the created material depends on restricted material;
- the created material lacks source support where source support is required;
- the created material may duplicate an existing Knowledge Object;
- the created material requires human judgment.

Creation Permission Requirements are successful when agents can create useful drafts, records, reports, templates, generated files, and implementation-support outputs without silently creating approved knowledge, authority, validation acceptance, privacy clearance, lifecycle transition, publication permission, export permission, migration permission, deletion authorization, downstream-use permission, or governance acceptance.

## 11. High-Risk and Restricted Permission Requirements

High-Risk and Restricted Permission Requirements define how agent permissions must be limited, reviewed, traced, escalated, or denied when an agent action may affect sensitive governed material, critical knowledge handling, privacy boundaries, authority boundaries, validation boundaries, lifecycle handling, destructive activity, publication, export, migration, deletion, downstream use, governance, or implementation behavior.

High-risk permissions exist because some agent actions can cause significant damage even when the agent output appears useful, plausible, technically correct, reversible, or convenient.

Restricted permissions exist because some actions require explicit scope, heightened traceability, human review, governed workflow authorization, privacy handling, escalation, or future specification before execution.

A high-risk operation is not prohibited solely because it is high-risk.

A restricted operation is not permitted solely because an agent has access, tool capability, role responsibility, implementation visibility, or workflow proximity.

High-risk and restricted operations require stronger control.

At minimum, high-risk and restricted operations include agent activity that may affect:

- Object Identity;
- required metadata;
- governed relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- review outcomes;
- approval outcomes;
- publication;
- export;
- migration;
- deletion;
- archival;
- backup;
- synchronization;
- indexing;
- caching;
- embedding;
- generated files;
- implementation exposure;
- downstream use;
- governance behavior;
- standard-level meaning;
- future governed high-risk categories.

A High-Risk or Restricted Permission SHOULD identify:

- what operation is high-risk or restricted;
- what agent, role, subagent, workflow, implementation, tool, script, or process may perform or support the operation;
- what governed entity or storage area is affected;
- what action is allowed;
- what action is prohibited;
- what conditions must be satisfied before action;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies;
- what validation boundary applies;
- what review is required before action;
- what review is required after action;
- what traceability is required;
- what escalation is required;
- whether the action is reversible;
- what recovery or rollback expectation applies where practical;
- what downstream-use limits apply.

High-risk and restricted permissions MUST be explicit where silent action could affect governed meaning, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, downstream use, governance, or implementation behavior.

An agent MUST NOT infer high-risk or restricted permission from:

- file access;
- folder access;
- vault access;
- repository access;
- database access;
- tool capability;
- plugin capability;
- model capability;
- prompt instruction;
- implementation visibility;
- workflow routing;
- storage placement;
- search result presence;
- prior successful behavior;
- repeated automation;
- user-interface convenience;
- agent confidence.

High-risk and restricted permissions SHOULD use the least permission necessary.

A permission to inspect high-risk material does not imply permission to summarize it.

A permission to summarize high-risk material does not imply permission to expose it.

A permission to propose a high-risk change does not imply permission to apply it.

A permission to apply a bounded high-risk change does not imply permission to approve it.

A permission to prepare export does not imply permission to release export.

A permission to prepare migration does not imply permission to complete migration.

A permission to recommend deletion does not imply permission to delete.

A permission to quarantine does not imply permission to delete.

A permission to archive does not imply permission to deprecate, supersede, or discard.

A permission to validate does not imply permission to approve.

High-risk and restricted permissions MUST preserve Privacy Classification.

An agent MUST NOT expose restricted material through activity records, traceability records, validation findings, review notes, escalation records, logs, reports, summaries, indexes, caches, embeddings, exports, publication drafts, migration packages, generated files, implementation displays, or downstream outputs unless permitted.

Where a high-risk or restricted operation involves restricted material, records SHOULD identify enough safe context for authorized review without unnecessarily exposing restricted content.

High-risk and restricted permissions MUST preserve review and escalation boundaries.

An agent SHOULD escalate high-risk or restricted activity when:

- permission scope is unclear;
- privacy handling is unclear;
- authority handling is unclear;
- lifecycle handling is unclear;
- validation handling is unclear;
- source support is missing or weak;
- provenance is missing or weak;
- Object Identity may be affected;
- publication may be affected;
- export may be affected;
- migration may be affected;
- deletion may be affected;
- downstream use may be affected;
- a destructive action is possible;
- an action may be irreversible;
- a record may expose restricted material;
- implementation behavior may redefine standard meaning;
- human judgment is required.

A High-Risk or Restricted Activity Record SHOULD identify or support identification of:

- what high-risk or restricted operation occurred or was proposed;
- what agent performed or proposed the operation;
- what permission scope applied;
- what governed entity or storage area was affected;
- what condition made the operation high-risk or restricted;
- what review occurred before action where applicable;
- what review remains required;
- what escalation occurred;
- what privacy boundary applied;
- what authority boundary applied;
- what validation boundary applied;
- what lifecycle boundary applied;
- what evidence or source support was used where applicable;
- what action was taken or blocked;
- whether the action was reversible;
- what recovery, rollback, quarantine, repair, or follow-up is required;
- what downstream use is permitted or prohibited.

A future governed workflow MAY allow limited automatic execution of a high-risk operation only when the operation is explicitly scoped, reversible where practical, validated, privacy-respecting, traceable, reviewable, compatible with higher-authority standards, and permitted by the applicable workflow or specification.

High-Risk and Restricted Permission Requirements are successful when sensitive and critical agent actions remain explicitly scoped, traceable, reviewable, privacy-preserving, escalation-ready, and subordinate to governance without making useful automation impossible.

## 12. Agent Activity Records

Agent Activity Records define what must be captured when an agent reads, searches, summarizes, extracts, proposes, validates, creates, edits, moves, deletes, exports, publishes, migrates, routes, escalates, reports, hands off, or otherwise acts on governed material.

Agent Activity Records exist because agent activity must remain inspectable where it affects governed meaning, privacy, authority, validation, lifecycle handling, publication, export, migration, deletion, downstream use, governance, or implementation behavior.

An Agent Activity Record is not approval.

An Agent Activity Record is not authority.

An Agent Activity Record is not validation acceptance.

An Agent Activity Record is not Privacy Classification.

An Agent Activity Record is not Lifecycle State transition.

An Agent Activity Record is not permission by itself.

An Agent Activity Record is not governed meaning by itself.

An Agent Activity Record records or supports review of what happened.

The presence of an Agent Activity Record does not make an unpermitted action conforming.

The absence of an Agent Activity Record does not automatically invalidate all governed material unless the applicable standard, workflow, validation rule, permission profile, specification, or governance process requires the record.

Agent Activity Records SHOULD be proportional to risk.

Low-risk activity MAY require lightweight records when the activity does not affect governed meaning, does not expose restricted material, does not produce governed output, does not change storage placement, does not alter metadata, does not alter relationships, does not create Source References, does not affect provenance, does not change Lifecycle State, does not affect Authority Level, does not affect Privacy Classification, does not affect Validation, does not trigger publication, does not trigger export, does not support migration, does not delete material, and does not affect downstream use.

Higher-risk activity SHALL require stronger records.

At minimum, an Agent Activity Record SHOULD identify or support identification of:

- what agent, role, subagent, workflow, implementation, tool, script, or process acted;
- what task or instruction applied;
- what permission scope applied;
- what operation type occurred;
- what governed entity, storage area, workflow context, implementation context, or output was affected;
- what material was inspected where applicable;
- what material was not inspected where that limitation affects interpretation;
- what source material or evidence was used where applicable;
- what output was produced;
- whether the activity was read-only, proposed, applied, blocked, rejected, reverted, approved, escalated, archived, superseded, or left pending;
- what assumptions were made;
- what uncertainty remains;
- what privacy boundary applies;
- what authority boundary applies where applicable;
- what lifecycle boundary applies where applicable;
- what validation boundary applies where applicable;
- what review is required;
- what escalation is required;
- what downstream use is permitted or prohibited where applicable.

Agent Activity Records MAY apply to:

- read activity;
- search activity;
- summarization activity;
- extraction activity;
- classification activity;
- metadata proposal activity;
- relationship proposal activity;
- Source Reference proposal activity;
- provenance proposal activity;
- privacy proposal activity;
- authority proposal activity;
- lifecycle proposal activity;
- validation activity;
- creation activity;
- write activity;
- edit activity;
- move activity;
- storage organization activity;
- import preparation activity;
- export preparation activity;
- migration preparation activity;
- publication preparation activity;
- deletion recommendation activity;
- archive recommendation activity;
- quarantine recommendation activity;
- workflow routing activity;
- escalation activity;
- handoff activity;
- implementation-support activity;
- generated-file activity;
- future governed agent activity.

Agent Activity Records MUST preserve Privacy Classification.

An activity record MUST NOT expose restricted material beyond the permitted scope.

Where restricted material is involved, an activity record SHOULD record that restricted material was involved, what privacy boundary applies, and what review or escalation is required without unnecessarily exposing the restricted content.

Agent Activity Records SHOULD preserve source and provenance context where agent activity affects interpretation, review, validation, authority, privacy, publication, export, migration, deletion, or downstream use.

An Agent Activity Record MUST NOT replace a Source Reference where a Source Reference is required.

An Agent Activity Record MUST NOT replace a provenance record where a provenance record is required.

An Agent Activity Record MUST NOT replace a review record where review is required.

An Agent Activity Record MUST NOT replace an approval record where approval is required.

An Agent Activity Record MUST NOT replace an escalation record where escalation is required.

Agent Activity Records SHOULD remain portable and implementation-independent.

A compliant implementation MAY use logs, sidecar files, metadata fields, workflow records, repository commits, database records, reports, generated files, audit trails, or future traceability mechanisms to support activity records.

Those mechanisms do not define activity-record meaning by themselves.

Activity-record meaning MUST remain explicit, inspectable, portable, privacy-respecting, and governed.

Agent Activity Records SHOULD be retained where retention is required for review, provenance, validation, auditability, security, recovery, governance, or downstream use.

Agent Activity Records SHOULD NOT be retained indefinitely where retention creates privacy, security, storage, governance, or operational risk without a governed reason.

An agent SHOULD escalate activity-record issues when:

- required activity records are missing;
- activity scope is unclear;
- permission scope is unclear;
- the affected material is unclear;
- the output is unclear;
- review status is unclear;
- approval status is unclear;
- privacy boundary is unclear;
- source support is unclear;
- provenance is unclear;
- validation scope is unclear;
- restricted material may be exposed;
- high-risk or restricted activity occurred without sufficient record;
- downstream use depends on unrecorded agent activity;
- implementation logs are being treated as governed meaning by themselves;
- human judgment is required.

Agent Activity Records are successful when agent work can be inspected, reviewed, validated, escalated, repaired, rejected, approved within scope, or audited without creating hidden authority, exposing restricted material, replacing required provenance, or making implementation logs the standard.

## 13. Output Traceability Requirements

Output Traceability Requirements define what must be preserved when an agent produces an output that may affect governed meaning, review, validation, privacy, authority, lifecycle handling, publication, export, migration, deletion, downstream use, governance, or implementation behavior.

Output traceability exists because agent output may be useful, plausible, complete, well-formatted, tool-generated, workflow-routed, validated within a limited scope, or implementation-visible without being approved, authoritative, final, publishable, exportable, migratable, deletable, or safe for downstream use.

Output traceability is not approval.

Output traceability is not authority.

Output traceability is not validation acceptance.

Output traceability is not Privacy Classification.

Output traceability is not Lifecycle State transition.

Output traceability is not publication permission.

Output traceability is not export permission.

Output traceability is not migration permission.

Output traceability is not deletion authorization.

Output traceability is not downstream-use permission.

Output traceability preserves enough context to inspect, review, validate, accept, reject, repair, escalate, audit, migrate, export, or use an agent output within a governed scope.

An Agent Output SHOULD have traceability where the output affects:

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
- implementation behavior.

At minimum, Output Traceability SHOULD identify or support identification of:

- what agent, role, subagent, workflow, implementation, tool, script, or process produced the output;
- what permission scope applied;
- what task, instruction, workflow step, or operation produced the output;
- what governed entity or storage area was affected;
- what source material was used where applicable;
- what material was inspected;
- what material was not inspected where that limitation affects interpretation;
- what output was produced;
- what output type applies;
- whether the output is informational, analytical, extracted, summarized, proposed, generated, applied, validated, reviewed, rejected, accepted, escalated, superseded, archived, or pending review;
- what assumptions were made;
- what evidence, source support, standard, workflow, validation result, or prior decision supports the output where applicable;
- what uncertainty remains;
- what confidence, limitation, or risk applies where applicable;
- what privacy boundary applies;
- what review is required;
- what escalation is required;
- what downstream use is permitted or prohibited.

Agent Output MUST remain distinguishable from Source Material.

An agent summary is not Source Material.

An agent extraction is not complete Source Material by default.

An agent interpretation is not source authority.

An agent-generated draft is not approved governed material by default.

An agent report is not approval by default.

An agent validation finding is not validation acceptance by default.

Agent Output MUST remain distinguishable from human-reviewed material unless a governed review process explicitly changes that status within a defined scope.

Agent Output MUST remain distinguishable from approved material unless a governed approval process explicitly changes that status within a defined scope.

Agent Output MUST remain distinguishable from authoritative material unless the applicable authority rule explicitly gives the output authority within a defined scope.

Agent Output MUST remain distinguishable from implementation-generated material where that distinction affects interpretation, validation, privacy, review, publication, export, migration, or downstream use.

Output Traceability MUST preserve permission context.

An agent output produced without permission remains non-conforming even if the output is useful.

An agent output produced outside permission scope remains non-conforming even if the output is accurate.

An agent output produced under one permission scope MUST NOT be treated as valid under every permission scope.

An output produced for review MUST NOT be treated as approved.

An output produced for export preparation MUST NOT be treated as export release.

An output produced for migration preparation MUST NOT be treated as migration completion.

An output produced for publication preparation MUST NOT be treated as publication approval.

Output Traceability MUST preserve source and provenance context.

An agent MUST NOT fabricate source support for an output.

An agent MUST NOT fabricate provenance for an output.

An agent MUST NOT remove source or provenance context merely to simplify output handling.

Where an output relies on Source Material, the output SHOULD preserve enough source context for review without treating the output as the source.

Where an output transforms Source Material, the output SHOULD preserve transformation context.

Where an output aggregates multiple sources, the output SHOULD preserve source distinction.

Where an output is unsupported, uncertain, partial, inferred, or speculative, that condition SHOULD remain visible.

Output Traceability MUST preserve Privacy Classification.

An output traceability record MUST NOT expose restricted material beyond the permitted scope.

Where restricted material supports an output, traceability SHOULD identify that restricted support exists and what privacy boundary applies without unnecessarily exposing restricted content.

An agent MUST NOT expose restricted assumptions, restricted sources, restricted identities, restricted relationships, restricted provenance, restricted validation findings, restricted workflow context, restricted implementation context, or restricted downstream-use context through output traceability unless permitted.

Output Traceability SHOULD remain portable and implementation-independent.

A compliant implementation MAY use metadata fields, sidecar records, logs, workflow records, repository commits, database records, generated reports, audit trails, templates, or future traceability mechanisms to support Output Traceability.

Those mechanisms do not define Output Traceability meaning by themselves.

Output Traceability meaning MUST remain explicit, inspectable, privacy-respecting, portable, and governed by The Brain Standard.

Output Traceability SHOULD be escalated when:

- output origin is unclear;
- permission scope is unclear;
- source support is missing, weak, or uncertain;
- provenance is missing, weak, or uncertain;
- inspected material is unclear;
- output status is unclear;
- review status is unclear;
- approval status is unclear;
- privacy boundary is unclear;
- output may affect Object Identity;
- output may affect metadata, relationships, Source References, or provenance;
- output may affect Lifecycle State, Authority Level, Privacy Classification, or Validation;
- output may affect publication, export, migration, deletion, or downstream use;
- output may expose restricted material;
- output may be confused with approved governed material;
- output depends on hidden memory, hidden tool state, hidden application state, hidden workflow state, hidden implementation behavior, or undocumented practice;
- human judgment is required.

Output Traceability Requirements are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, implementations, and governance processes can determine what produced an agent output, what supported it, what scope applied, what review is required, what privacy boundary applies, and whether the output may safely affect governed material.

## 14. Review and Approval Traceability

Review and Approval Traceability defines what must be preserved when agent activity, agent output, agent-generated changes, proposals, validation findings, workflow outputs, storage actions, publication candidates, export candidates, migration candidates, deletion candidates, or downstream-use candidates are reviewed, accepted, rejected, approved, deferred, escalated, revised, reverted, superseded, archived, or otherwise handled through a governed review process.

Review traceability exists because review must remain inspectable, scoped, privacy-respecting, and distinguishable from approval.

Approval traceability exists because approval must remain accountable, scoped, reviewable, and distinguishable from permission, validation, authority, lifecycle state, privacy classification, workflow completion, implementation visibility, and agent confidence.

Review is not approval by itself.

Review preparation is not review completion.

Review routing is not review completion.

Validation support is not review completion.

Workflow completion is not approval unless a governed workflow explicitly defines that effect within a controlled scope.

Implementation visibility is not approval.

Permission is not approval.

Traceability is not approval.

A Review Record SHOULD identify or support identification of:

- what was reviewed;
- what agent, role, workflow, implementation, tool, script, or process prepared the reviewed material where applicable;
- what reviewer, workflow, role, or governed process performed the review where applicable;
- what review scope applied;
- what material was inspected;
- what material was not inspected where that limitation affects interpretation;
- what source material, evidence, standard, workflow, validation result, prior decision, or assumption was considered where applicable;
- what issue, output, proposal, change, action, or candidate was reviewed;
- what finding or outcome resulted;
- what uncertainty remains;
- what privacy boundary applies;
- what escalation is required;
- what downstream use is permitted or prohibited.

A Review Record MAY support the following outcomes:

- accepted;
- accepted with changes;
- approved for limited scope;
- approved for full stated scope;
- rejected;
- returned for revision;
- deferred;
- escalated;
- quarantined;
- marked needs repair;
- reverted;
- superseded;
- archived;
- left pending;
- governed by a future review outcome.

Review outcomes MUST preserve scope.

A review outcome for one output MUST NOT be treated as a review outcome for every output.

A review outcome for one Knowledge Record MUST NOT be treated as a review outcome for every Knowledge Record.

A review outcome for one Source Reference MUST NOT be treated as a review outcome for every Source Reference.

A review outcome for metadata MUST NOT be treated as relationship approval.

A review outcome for a relationship MUST NOT be treated as publication approval.

A review outcome for validation findings MUST NOT be treated as validation acceptance beyond the reviewed scope.

A review outcome for export preparation MUST NOT be treated as export release.

A review outcome for migration preparation MUST NOT be treated as migration completion.

A review outcome for publication preparation MUST NOT be treated as publication approval unless explicitly approved within scope.

An Approval Record SHOULD identify or support identification of:

- what was approved;
- who, what role, what workflow, or what governed process approved it where applicable;
- what approval scope applies;
- what reviewed material supported approval;
- what source material, evidence, standard, validation result, workflow result, or prior decision supported approval where applicable;
- what conditions apply;
- what limitations apply;
- what downstream use is permitted;
- what downstream use is prohibited;
- what privacy boundary applies;
- what authority boundary applies where applicable;
- what lifecycle boundary applies where applicable;
- what validation boundary applies where applicable;
- what publication, export, migration, deletion, or downstream-use limits apply;
- what unresolved issue remains where applicable.

Approval MUST preserve scope.

Approval for draft use is not approval for publication.

Approval for internal use is not approval for export.

Approval for export is not approval for public release unless the approval scope says so.

Approval for migration preparation is not approval for migration completion.

Approval for one implementation is not approval for every implementation.

Approval for one downstream use is not approval for every downstream use.

Approval of structure is not approval of content.

Approval of content is not approval of source sufficiency unless source sufficiency was in scope.

Approval of source sufficiency is not approval of Privacy Classification unless privacy was in scope.

Approval of Privacy Classification is not approval of Authority Level unless authority was in scope.

Review and Approval Traceability MUST preserve Privacy Classification.

Review records and approval records MUST NOT expose restricted material beyond the permitted scope.

Where restricted material supports review or approval, the record SHOULD preserve enough safe context for authorized review without unnecessarily exposing restricted content.

Review and Approval Traceability MUST preserve source and provenance expectations.

A review record MUST NOT fabricate review history.

An approval record MUST NOT fabricate approval history.

A review record MUST NOT imply that source support was checked if source support was outside review scope.

An approval record MUST NOT imply that validation was accepted if validation acceptance was outside approval scope.

A review or approval record MUST NOT erase agent involvement where agent involvement affects interpretation, provenance, validation, privacy, authority, publication, export, migration, deletion, or downstream use.

Review and Approval Traceability SHOULD remain portable and implementation-independent.

A compliant implementation MAY use workflow records, review notes, approval records, metadata fields, repository commits, logs, database records, sidecar files, generated reports, audit trails, or future traceability mechanisms to support review and approval traceability.

Those mechanisms do not define review or approval meaning by themselves.

Review and approval meaning MUST remain explicit, inspectable, privacy-respecting, portable, and governed.

Review and approval issues SHOULD be escalated when:

- review scope is unclear;
- approval scope is unclear;
- reviewer identity or review process is unclear where required;
- reviewed material is unclear;
- approval basis is unclear;
- source support is unclear;
- provenance is unclear;
- validation scope is unclear;
- privacy boundary is unclear;
- authority boundary is unclear;
- lifecycle effect is unclear;
- publication, export, migration, deletion, or downstream-use effect is unclear;
- review or approval depends on hidden memory, hidden workflow state, hidden implementation state, undocumented practice, or unreviewable agent output;
- an agent output may be confused with approval;
- restricted material may be exposed;
- human judgment is required.

Review and Approval Traceability Requirements are successful when review and approval decisions remain explicit, scoped, accountable, privacy-respecting, portable, inspectable, and distinguishable from agent output, validation support, workflow routing, implementation visibility, permission, authority, lifecycle state, and governance assumptions.

## 15. Escalation Records

Escalation Records define what must be captured when an agent, role, workflow, validator, implementation, tool, script, or governed process identifies ambiguity, conflict, risk, missing evidence, privacy concern, authority concern, validation issue, lifecycle concern, destructive-action risk, publication risk, export risk, migration risk, deletion risk, downstream-use risk, governance concern, implementation concern, or unresolved decision requiring human review or governed workflow handling.

Escalation Records exist because unresolved risk must remain visible, reviewable, privacy-respecting, traceable, and actionable.

Escalation is not approval.

Escalation is not rejection.

Escalation is not repair.

Escalation is not deletion.

Escalation is not publication.

Escalation is not export.

Escalation is not migration.

Escalation is not privacy clearance.

Escalation is not authority assignment.

Escalation is not lifecycle transition.

Escalation is not validation acceptance.

Escalation routes an issue for review or governed handling.

An Escalation Record SHOULD be created or supported when an agent identifies or suspects risk affecting:

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
- implementation behavior;
- future governed escalation categories.

An Escalation Record SHOULD identify or support identification of:

- what issue was escalated;
- what agent, role, subagent, workflow, implementation, tool, script, validator, or process identified the issue;
- what permission scope applied where applicable;
- what governed entity, storage area, workflow context, implementation context, or output is affected;
- what condition triggered escalation;
- what risk exists;
- what standard, specification, workflow, validation scope, privacy boundary, authority boundary, lifecycle boundary, permission profile, or implementation behavior may be affected;
- what material was inspected;
- what material was not inspected where that limitation affects interpretation;
- what source material or evidence was used where applicable;
- what assumptions were made;
- what uncertainty remains;
- whether restricted material is involved;
- what context may be safely shown to the reviewer;
- what action is recommended;
- what action is prohibited until review;
- whether the escalation blocks further activity;
- what review is required;
- what follow-up is required;
- what downstream use is permitted or prohibited until resolution.

An Escalation Record MAY categorize the escalation as:

- identity escalation;
- metadata escalation;
- relationship escalation;
- Source Reference escalation;
- provenance escalation;
- lifecycle escalation;
- authority escalation;
- privacy escalation;
- validation escalation;
- review escalation;
- approval escalation;
- workflow escalation;
- storage escalation;
- implementation escalation;
- publication escalation;
- export escalation;
- migration escalation;
- deletion escalation;
- downstream-use escalation;
- governance escalation;
- security escalation;
- future governed escalation type.

Escalation Records MUST preserve Privacy Classification.

An Escalation Record MUST NOT expose restricted material beyond the permitted scope.

Where restricted material is involved, the Escalation Record SHOULD identify that restricted material is involved and what privacy boundary applies without unnecessarily exposing restricted content.

An Escalation Record SHOULD allow an authorized reviewer to locate or request the restricted context through governed means where direct exposure is not permitted.

Escalation Records MUST preserve source and provenance boundaries.

An Escalation Record MUST NOT fabricate evidence.

An Escalation Record MUST NOT fabricate provenance.

An Escalation Record MUST NOT claim source support that was not inspected.

An Escalation Record MUST NOT claim review, approval, validation, privacy clearance, authority assignment, lifecycle transition, publication approval, export approval, migration approval, deletion authorization, or downstream-use permission merely because escalation occurred.

Escalation Records SHOULD preserve blocking status where applicable.

An escalation MAY block further agent activity.

An escalation MAY block publication.

An escalation MAY block export.

An escalation MAY block migration.

An escalation MAY block deletion.

An escalation MAY block downstream use.

An escalation MAY block approval.

Blocking behavior is valid only where the applicable standard, workflow, permission profile, validation rule, privacy rule, authority rule, implementation profile, or governance process permits blocking within scope.

Escalation Records SHOULD preserve resolution status.

An Escalation Record MAY be:

- open;
- under review;
- resolved;
- resolved with changes;
- rejected;
- deferred;
- superseded;
- archived;
- transferred;
- blocked;
- unblocked;
- quarantined;
- needs repair;
- governed by a future escalation status.

Escalation resolution MUST preserve scope.

Resolving one escalation does not resolve every related escalation.

Resolving a metadata escalation does not resolve a privacy escalation unless privacy was in scope.

Resolving a validation escalation does not approve publication unless publication approval was in scope.

Resolving an export escalation does not approve migration unless migration approval was in scope.

Resolving an identity escalation does not approve relationship changes unless relationship approval was in scope.

An Escalation Record SHOULD identify or support identification of resolution context where applicable:

- what decision was made;
- who, what role, what workflow, or what governed process resolved the escalation where applicable;
- what evidence was reviewed;
- what change was required;
- what change was prohibited;
- what risk remains;
- what privacy boundary remains;
- what review remains required;
- what downstream use is permitted or prohibited;
- whether the escalation should inform future standards, workflows, permission profiles, validation rules, implementation profiles, or operational guidance.

Escalation Records SHOULD remain portable and implementation-independent.

A compliant implementation MAY use workflow queues, issue records, review notes, metadata fields, sidecar files, logs, repository issues, database records, generated reports, audit trails, or future traceability mechanisms to support Escalation Records.

Those mechanisms do not define escalation meaning by themselves.

Escalation meaning MUST remain explicit, inspectable, privacy-respecting, portable, and governed.

Escalation Records are successful when risks, ambiguities, conflicts, privacy concerns, authority concerns, validation issues, destructive-action concerns, publication concerns, export concerns, migration concerns, deletion concerns, downstream-use concerns, governance concerns, and implementation concerns remain visible, reviewable, actionable, privacy-preserving, and traceable until resolved within a governed scope.

## 16. Permission Review, Revocation, and Expiration

Permission Review, Revocation, and Expiration define how agent permissions, permission profiles, permission grants, permission constraints, permission denials, and permission uses are evaluated, narrowed, suspended, revoked, expired, replaced, or escalated within The Brain Standard.

Permission review exists because an agent permission that was appropriate in one scope, workflow stage, privacy boundary, authority boundary, lifecycle state, validation state, implementation context, or time period may become inappropriate later.

Permission revocation exists because permissions must be removable when they become unsafe, outdated, excessive, non-conforming, privacy-sensitive, authority-sensitive, validation-sensitive, lifecycle-sensitive, implementation-sensitive, or no longer needed.

Permission expiration exists because permissions should not remain active indefinitely merely because they were once useful.

Permission Review is not approval.

Permission Review is not Authority Level assignment.

Permission Review is not Privacy Classification assignment.

Permission Review is not Lifecycle State transition.

Permission Review is not validation acceptance.

Permission Review is not publication permission.

Permission Review is not export permission.

Permission Review is not migration permission.

Permission Review is not deletion authorization.

Permission Review evaluates whether permission remains appropriate within scope.

A Permission Review SHOULD determine:

- what permission, permission profile, permission grant, permission constraint, or permission use is being reviewed;
- what agent, role, subagent, workflow, implementation, tool, script, or process used or may use the permission;
- what scope applies;
- what governed entity, storage area, workflow context, implementation context, or output may be affected;
- what actions are allowed;
- what actions are prohibited;
- what conditions apply;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies;
- what validation boundary applies;
- what traceability exists;
- what review has occurred;
- what escalation has occurred;
- whether the permission remains necessary;
- whether the permission remains safe;
- whether the permission should continue, narrow, suspend, expire, revoke, supersede, or be replaced.

Permission Review MAY be:

- scheduled;
- workflow-triggered;
- lifecycle-triggered;
- privacy-triggered;
- authority-triggered;
- validation-triggered;
- escalation-triggered;
- implementation-triggered;
- incident-triggered;
- migration-triggered;
- export-triggered;
- publication-triggered;
- deletion-triggered;
- downstream-use-triggered;
- human-requested;
- future governed review type.

A Permission Review SHOULD occur when:

- permission scope is unclear;
- permission use exceeds scope;
- an agent role changes;
- a workflow changes;
- a governed entity changes Lifecycle State;
- Authority Level changes;
- Privacy Classification changes;
- Validation State changes;
- storage placement changes in a way that affects handling;
- implementation behavior changes;
- source or provenance support changes;
- publication, export, migration, deletion, or downstream use becomes possible;
- an escalation identifies permission risk;
- a high-risk or restricted operation is requested;
- permission has not been reviewed within the expected review interval;
- human judgment is required.

A permission MAY be continued only when it remains appropriate within the reviewed scope.

A permission MAY be narrowed when the prior permission is broader than needed.

A permission MAY be suspended when temporary uncertainty, risk, conflict, validation failure, privacy concern, implementation concern, or escalation requires further review.

A permission MAY be revoked when the permission is unsafe, invalid, expired, excessive, non-conforming, superseded, unsupported, unauthorized, or no longer needed.

A permission MAY expire automatically when:

- a time limit ends;
- a workflow stage ends;
- a task completes;
- a review fails;
- a permission condition is no longer satisfied;
- a Lifecycle State changes;
- an Authority Level changes;
- a Privacy Classification changes;
- a Validation State changes;
- an implementation context changes;
- an export, publication, migration, deletion, or downstream-use boundary is reached;
- a governed specification defines expiration;
- another governed expiration condition occurs.

An agent MUST NOT continue operating under a revoked permission.

An agent MUST NOT continue operating under an expired permission.

An agent MUST NOT continue operating under a suspended permission unless the suspension explicitly allows limited activity within scope.

An agent MUST NOT treat an old permission as still active merely because the agent previously used it successfully.

An agent MUST NOT treat access, storage visibility, tool capability, workflow routing, implementation access, model memory, prompt context, or user-interface convenience as evidence that a revoked, expired, or suspended permission remains valid.

Permission revocation, suspension, narrowing, expiration, or replacement SHOULD preserve traceability.

A Permission Review Record SHOULD identify or support identification of:

- what permission was reviewed;
- what permission profile or grant applied;
- what agent, role, subagent, workflow, implementation, tool, script, or process was affected;
- what review scope applied;
- what evidence was considered;
- what activity records were considered;
- what output traceability was considered;
- what review records were considered;
- what escalation records were considered;
- what decision was made;
- whether permission continued, narrowed, suspended, revoked, expired, superseded, replaced, or remained pending;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies;
- what validation boundary applies;
- what downstream use remains permitted or prohibited;
- what follow-up review is required.

Permission Review Records MUST preserve Privacy Classification.

A Permission Review Record MUST NOT expose restricted material beyond the permitted scope.

Where restricted material supports permission review, the record SHOULD preserve enough safe context for authorized review without unnecessarily exposing restricted content.

Permission review, revocation, and expiration are successful when agent permissions remain current, scoped, necessary, traceable, reviewable, privacy-respecting, and revocable without relying on hidden implementation behavior, stale assumptions, or unreviewable agent memory.

## 17. Conformance, Non-Conformance, and Exceptions

Conformance, Non-Conformance, and Exceptions define how agent permission and traceability behavior is evaluated against AG-0003.

AG-0003 conformance means that agent permissions, permission profiles, permission grants, permission constraints, permission denials, activity records, output traceability, review records, approval records, escalation records, permission reviews, revocations, expirations, and exception handling preserve The Brain Standard within the defined scope.

A conforming agent, workflow, implementation, permission profile, or traceability mechanism does not need to use a specific prompt, model, tool, runtime, folder path, database, schema, plugin, interface, or automation system.

Conformance is based on preserved meaning and governed behavior.

Implementation success is not conformance by itself.

Tool success is not conformance by itself.

Model confidence is not conformance by itself.

Workflow completion is not conformance by itself.

Storage placement is not conformance by itself.

A compliant implementation MAY satisfy AG-0003 through different technical mechanisms if the required permission and traceability meanings remain explicit, inspectable, privacy-respecting, portable, reviewable, and governed.

AG-0003 conforms when:

- agent permissions are scoped;
- agent access is not confused with permission;
- role responsibility is not confused with permission;
- permission is not confused with approval;
- permission is not confused with Authority Level;
- permission is not confused with Privacy Classification;
- permission is not confused with Lifecycle State transition;
- permission is not confused with Validation State;
- agent output remains distinguishable from approved governed material;
- activity records exist where required;
- output traceability exists where required;
- review and approval traceability preserve scope;
- escalation records preserve unresolved risk;
- high-risk and restricted operations receive stronger control;
- permission review, revocation, and expiration remain possible;
- privacy boundaries are preserved;
- source and provenance boundaries are preserved;
- storage behavior does not define knowledge meaning;
- implementation behavior does not become the standard itself;
- human review remains available where required.

Non-Conformance occurs when an agent, workflow, implementation, permission profile, traceability mechanism, or governed process violates AG-0003 requirements.

Non-conformance MAY include:

- unscoped permission;
- excessive permission;
- missing permission;
- expired permission use;
- revoked permission use;
- silent permission inheritance;
- access treated as permission;
- role responsibility treated as permission;
- tool capability treated as permission;
- implementation visibility treated as permission;
- permission treated as approval;
- validation support treated as validation acceptance;
- workflow completion treated as approval without governed basis;
- activity records missing where required;
- output traceability missing where required;
- review scope unclear;
- approval scope unclear;
- escalation records missing where required;
- restricted material exposed through records or outputs;
- Source References fabricated;
- provenance fabricated;
- Object Identity silently changed;
- Privacy Classification silently lowered;
- Authority Level silently assigned;
- Lifecycle State silently transitioned;
- publication, export, migration, deletion, or downstream-use permission silently created;
- implementation logs treated as governed meaning by themselves;
- hidden memory, hidden application state, hidden workflow state, or undocumented practice treated as the source of permission or traceability.

Non-conformance does not automatically mean all related governed material is invalid.

Non-conformance means the affected scope requires review, correction, quarantine, rollback, escalation, documentation, revalidation, permission repair, traceability repair, or other governed handling as appropriate.

A Non-Conformance Record SHOULD identify or support identification of:

- what requirement was violated;
- what agent, role, subagent, workflow, implementation, tool, script, or process was involved;
- what permission scope applied or should have applied;
- what governed entity, output, storage area, workflow context, or implementation context was affected;
- what activity occurred;
- what traceability exists;
- what traceability is missing;
- what privacy boundary applies;
- what source or provenance issue exists where applicable;
- what review is required;
- what escalation is required;
- what repair, rollback, quarantine, revocation, expiration, or follow-up action is required;
- what downstream use is permitted or prohibited until resolution.

Exceptions are limited allowances to deviate from AG-0003 within a governed scope.

An exception MUST NOT be treated as a permanent rule unless formally adopted through governance.

An exception MUST NOT silently override higher-authority standards.

An exception MUST NOT silently override Privacy Classification.

An exception MUST NOT silently create approval, authority, validation acceptance, lifecycle transition, publication permission, export permission, migration permission, deletion authorization, downstream-use permission, or governance acceptance.

An Exception Record SHOULD identify or support identification of:

- what exception is being granted or requested;
- why the exception is needed;
- what requirement is affected;
- what agent, role, workflow, implementation, tool, script, or process is affected;
- what scope applies;
- what risk exists;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies;
- what validation boundary applies;
- what review approved or denied the exception where applicable;
- what expiration condition applies;
- what traceability is required;
- what escalation is required;
- what downstream use is permitted or prohibited.

Exceptions SHOULD be narrow, time-bounded where practical, reviewable, traceable, privacy-respecting, and reversible where practical.

An exception SHOULD be escalated when it affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, publication, export, migration, deletion, downstream use, governance, or implementation behavior.

Conformance, Non-Conformance, and Exceptions are successful when AG-0003 can be applied consistently without making the standard brittle, while still preventing unscoped permission, hidden authority, missing traceability, privacy exposure, and implementation-defined governance.

## 18. Success Criteria and Closing Rule

AG-0003 is successful when agent permission and traceability behavior remains explicit, scoped, inspectable, privacy-respecting, reviewable, portable, implementation-independent, and subordinate to The Brain Standard.

A successful AG-0003 implementation allows future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, downstream systems, and governance processes to determine:

- what agent acted;
- what role or subagent was involved;
- what permission scope applied;
- what permission did not apply;
- what material was read;
- what material was created;
- what material was proposed for change;
- what material was changed;
- what material was moved;
- what material was validated;
- what material was reviewed;
- what material was escalated;
- what output was produced;
- what evidence supported the output;
- what source material was used;
- what provenance applies;
- what assumptions were made;
- what uncertainty remains;
- what privacy boundary applies;
- what authority boundary applies;
- what lifecycle boundary applies;
- what validation boundary applies;
- what review is required;
- what approval exists or does not exist;
- what escalation exists or remains unresolved;
- what permission review, revocation, or expiration applies;
- what downstream use is permitted or prohibited.

AG-0003 is successful when agent work can reduce cognitive load, improve consistency, support review, support validation, support maintenance, support implementation, and support future automation without allowing agents to become hidden authorities over knowledge.

AG-0003 is successful when permission remains distinguishable from:

- access;
- visibility;
- searchability;
- tool capability;
- role responsibility;
- agent confidence;
- agent output;
- traceability;
- review preparation;
- review routing;
- workflow completion;
- validation support;
- storage placement;
- implementation behavior;
- approval;
- Authority Level;
- Privacy Classification;
- Lifecycle State;
- Validation State;
- publication permission;
- export permission;
- migration permission;
- deletion authorization;
- downstream-use permission;
- governance acceptance.

AG-0003 is successful when traceability remains distinguishable from:

- permission;
- approval;
- authority;
- validation acceptance;
- Privacy Classification;
- Lifecycle State transition;
- publication permission;
- export permission;
- migration permission;
- deletion authorization;
- downstream-use permission;
- governed truth.

AG-0003 is successful when activity records, output traceability records, review records, approval records, escalation records, permission review records, non-conformance records, and exception records preserve enough context to support review, validation, repair, auditability, migration, export, publication, downstream use, and governance without exposing restricted material beyond the permitted scope.

AG-0003 is successful when high-risk and restricted operations are explicit, limited, traceable, reviewable, privacy-preserving, escalation-ready, and revocable.

AG-0003 is successful when low-risk agent assistance remains practical and does not become overburdened by unnecessary process, while high-risk agent activity receives stronger control.

AG-0003 is successful when future implementations can represent permissions and traceability through different technical mechanisms without changing the meaning of the standard.

AG-0003 is successful when The Brain remains usable with ChatGPT, Codex, local AI models, scripts, validators, Obsidian tools, repositories, databases, workflow systems, or future implementations without allowing any one implementation to become the standard itself.

AG-0003 is successful when AG-0001, AG-0002, and AG-0003 together provide a complete minimum Agent Framework foundation:

- AG-0001 defines agent operating boundaries;
- AG-0002 defines agent roles and responsibilities;
- AG-0003 defines agent permissions and traceability.

The closing rule of AG-0003 is:

Agents may assist, inspect, summarize, extract, propose, validate, draft, create, edit, move, route, report, escalate, and support implementation only within explicit permission scope and traceability expectations.

Agents must not silently govern.

Agent access is not permission.

Agent role is not permission.

Agent permission is not approval.

Agent output is not authority.

Agent confidence is not Authority Level.

Agent traceability is not review completion.

Agent validation support is not validation acceptance.

Agent workflow participation is not lifecycle transition.

Agent storage behavior is not knowledge meaning.

Agent implementation behavior is not the standard.

Where permission, traceability, review, privacy, authority, lifecycle, validation, publication, export, migration, deletion, downstream use, or governance is unclear, the agent SHOULD preserve the current governed state, avoid expanding authority, avoid exposing restricted material, record uncertainty where appropriate, and escalate for human review or governed workflow handling.

AG-0003 is complete when future humans, agents, workflows, validators, storage systems, implementations, and governance processes can use it to keep agent activity bounded, permissioned, traceable, reviewable, privacy-respecting, implementation-independent, and subordinate to The Brain Standard.
