# KS-0007 — Authority Level Standard

Document ID: KS-0007
Title: Authority Level Standard
Version: 0.1.0
Status: Approved
Created: 2026-06-26
Last Updated: 2026-06-26
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.7 — Authority Level Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and authority-level rules are interpreted within KS-0007.

Where conflicts arise between Authority Level, authority metadata, authority scope, approval, lifecycle state, validation state, privacy classification, provenance, relationships, source references, source authority, agent confidence, workflow completion, implementation behavior, storage behavior, import behavior, export behavior, migration behavior, publication behavior, downstream use, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0007 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0007 extends KS-0001 by defining standard-level Authority Level behavior for Knowledge Objects, Knowledge Records, Source References, provenance records, relationships, validation results, workflow outputs, agent outputs, imports, exports, migrations, decisions, governed documents where applicable, and other governed entities.

KS-0007 depends on KS-0002 because Authority Level must preserve stable Object Identity across review, approval, validation, publication, import, export, migration, supersession, archival, and implementation replacement.

KS-0007 depends on KS-0003 because authority meaning may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through metadata.

KS-0007 depends on KS-0004 because relationships may carry authority-related meaning and because relationship authority must remain distinguishable from relationship existence, relationship strength, relationship confidence, graph position, backlink behavior, or implementation-specific linking.

KS-0007 depends on KS-0005 because Source References, provenance, evidence, attribution, source reliability, source authority, and source availability may support Authority Level without replacing it.

KS-0007 depends on KS-0006 because Lifecycle State may affect authority handling, but Lifecycle State does not replace Authority Level.

If KS-0007 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

If KS-0007 appears to conflict with KS-0001, the conflict SHOULD be resolved by preserving the Knowledge Object Model defined in KS-0001 while applying KS-0007 as the more specific standard for Authority Level behavior.

If KS-0007 appears to conflict with KS-0002, the conflict SHOULD be resolved by preserving stable Object Identity while applying KS-0007 as the more specific standard for authority interpretation, review, validation, and compatibility.

If KS-0007 appears to conflict with KS-0003, the conflict SHOULD be resolved by preserving metadata role boundaries while applying KS-0007 as the more specific standard for authority metadata and authority-level behavior.

If KS-0007 appears to conflict with KS-0004, the conflict SHOULD be resolved by preserving relationship behavior while applying KS-0007 as the more specific standard for relationship authority and authority interpretation.

If KS-0007 appears to conflict with KS-0005, the conflict SHOULD be resolved by preserving source-reference and provenance behavior while applying KS-0007 as the more specific standard for authority support, source authority, evidentiary authority, and provenance-supported authority.

If KS-0007 appears to conflict with KS-0006, the conflict SHOULD be resolved by preserving lifecycle-state behavior while applying KS-0007 as the more specific standard for Authority Level behavior.

KS-0007 defines Authority Level at the conceptual standard level.

KS-0007 does not define exact Markdown front matter syntax, exact metadata field names, exact authority values, exact authority scoring systems, exact trust scores, exact validation tooling, exact workflow approval procedures, exact agent confidence formats, exact publication rules, exact access-control systems, exact implementation-specific labels, exact storage paths, or exact user-interface behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation profiles, validation specifications, authority vocabularies, publication specifications, and operational documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, Object Identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a document, Knowledge Object, Knowledge Record, Source Reference, relationship, provenance record, validation result, workflow output, agent output, import record, export record, migration record, decision, or other governed entity within a defined scope.
- Authority Scope refers to the defined context in which an Authority Level applies.
- Authority Assignment refers to the act of assigning, proposing, confirming, revising, limiting, suspending, removing, or preserving Authority Level for a governed entity.
- Authority Review refers to the review process used to determine whether an Authority Level is appropriate, supported, scoped, traceable, current, compatible, and safe for downstream use.
- Authority Metadata refers to metadata that records, expresses, supports, validates, or preserves Authority Level, authority scope, authority assignment, authority review, or authority history.
- Governance Weight refers to the degree to which a governed entity may influence interpretation, standards, decisions, workflows, validation, publication, migration, implementation behavior, or downstream use within its defined scope.
- Interpretive Authority refers to the degree to which a governed entity may be relied on to guide meaning, interpretation, classification, explanation, relationship handling, source interpretation, or decision support within its defined scope.
- Use-Authority refers to whether and how a governed entity may be used for a particular purpose, workflow, publication context, export context, migration context, implementation context, agent context, or downstream-use context.
- Trust Boundary refers to the limit beyond which a governed entity MUST NOT be treated as authoritative without additional review, validation, approval, provenance, source support, privacy review, or governance action.
- Approval refers to formal acceptance of a governed entity for use within a defined scope.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Validation State refers to whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.
- Privacy Classification refers to explicit metadata describing permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Source Authority refers to the governance weight, official status, interpretive relevance, review status, or approved use assigned to Source Material within a defined context.
- Source Reliability refers to the assessed trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength of Source Material.
- Relationship Authority refers to the governance weight, review status, interpretive authority, or use-authority assigned to a relationship within a defined scope.
- Agent Confidence refers to an agent-generated indication of certainty, probability, model confidence, classification confidence, extraction confidence, relationship confidence, validation confidence, or recommendation confidence.
- Workflow Completion refers to the successful completion of a workflow step, workflow stage, workflow run, task sequence, automation, routing path, review queue, or operational procedure.
- Implementation Visibility refers to whether a governed entity is visible, surfaced, indexed, ranked, displayed, searched, cached, routed, filtered, published, synchronized, or exposed by a specific implementation.
- Downstream Use refers to later use of a governed entity for interpretation, automation, publication, export, migration, relationship creation, validation, decision support, agent reasoning, workflow execution, implementation behavior, or other dependent activity.
- Migration refers to movement from one storage system, implementation, representation, schema, vault, repository, database, file format, workflow environment, or tool environment to another.
- Import refers to the process of bringing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, Source References, provenance, or external content into a compliant environment.
- Export refers to the process of producing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, Source References, provenance, or external content from a compliant environment for use elsewhere.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.

## 1. Purpose

The purpose of KS-0007 is to define how Authority Level works across The Brain Standard.

KS-0001 establishes Authority Level as a required knowledge-level concept where authority affects interpretation, governance, review, trust, publication, validation, or downstream use.

KS-0007 defines the standard-level behavior required to create, assign, interpret, preserve, review, validate, limit, revise, migrate, import, export, govern, and maintain Authority Level.

Authority Level exists so that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine how much governance weight, interpretive authority, review weight, or use-authority a governed entity carries within a defined scope.

KS-0007 exists to prevent authority confusion.

Authority confusion occurs when humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, or implementations cannot reliably determine:

- whether a governed entity is authoritative;
- what scope the authority applies to;
- whether authority was assigned by a human, workflow, validator, agent, import process, export process, migration process, implementation, source, relationship, or governance decision;
- whether authority depends on approval, review, validation, provenance, source support, relationship context, privacy classification, lifecycle state, compatibility, or downstream-use limits;
- whether a governed entity may be relied on for interpretation, governance, publication, export, migration, automation, workflow routing, validation, relationship creation, agent reasoning, implementation behavior, or downstream use;
- whether Authority Level has been confused with Lifecycle State, approval, Validation State, Privacy Classification, Provenance, Source Reference existence, source reliability, source popularity, relationship strength, agent confidence, workflow completion, implementation visibility, storage location, search ranking, graph centrality, publication status, or downstream-use permission.

KS-0007 defines Authority Level behavior for:

- Knowledge Objects;
- Knowledge Records;
- Source References;
- Source Material where applicable;
- provenance records;
- relationships;
- metadata records;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- governed documents where applicable;
- decisions;
- other governed entities.

KS-0007 does not replace the document authority hierarchy defined by TB-0003.

TB-0003 defines document authority levels for governed documents.

KS-0007 defines standard-level Authority Level behavior for knowledge entities and related governed entities, while remaining compatible with TB-0003.

KS-0007 does not define exact metadata field names, exact Markdown front matter syntax, exact database schemas, exact API fields, exact authority values, exact scoring systems, exact trust metrics, exact validation tooling, exact workflow procedures, exact automation triggers, exact implementation-specific labels, exact storage paths, exact access-control rules, or exact user-interface behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation documents, validation specifications, authority vocabularies, authority transition specifications, publication specifications, privacy specifications, and operational guides.

KS-0007 defines Authority Level at the standard level.

A future specification MAY define exact authority fields, allowed authority values, authority scopes, assignment rules, review rules, validation rules, approval rules, limitation rules, inheritance rules, downgrade rules, escalation rules, publication rules, import mappings, export mappings, migration mappings, agent handling rules, workflow triggers, or serialization syntax.

Such specifications are valid only when they preserve the Authority Level behavior defined by KS-0007.

The primary purpose of KS-0007 is to ensure that Authority Level remains explicit, scoped, interpretable, portable, traceable, reviewable, privacy-respecting, provenance-preserving, validatable, compatible, and implementation-independent across time, tools, storage systems, workflows, agents, validators, and implementations.

KS-0007 is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine:

- what Authority Level applies to a governed entity;
- what the Authority Level means;
- what authority scope applies;
- who or what assigned the Authority Level where applicable;
- what review, validation, approval, provenance, source support, relationship context, lifecycle state, privacy classification, compatibility, or governance decision supports the Authority Level;
- whether the Authority Level is current, historical, limited, suspended, superseded, inherited, proposed, reviewed, approved, rejected, deprecated, archived, restricted, or otherwise governed;
- whether the Authority Level affects interpretation, governance, validation, relationships, Source References, provenance, privacy, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, publication, import, export, migration, or downstream use;
- whether Authority Level behavior can be preserved without relying on hidden application state, folder placement, filename convention, tag convention, user-interface state, workflow memory, agent memory, implementation-specific labels, search ranking, graph centrality, backlink behavior, popularity, or undocumented practice.

## 2. Relationship to Prior Standards

KS-0007 is subordinate to and derived from the constitutional foundation of The Brain Standard.

KS-0007 depends on:

- TB-0000 — Vision and Purpose;
- TB-0001 — Architecture Principles;
- TB-0002 — Layered Architecture;
- TB-0003 — Governance Model;
- KS-0001 — Knowledge Object Model;
- KS-0002 — Object Identity Standard;
- KS-0003 — Metadata Standard;
- KS-0004 — Relationship Standard;
- KS-0005 — Source Reference and Provenance Standard;
- KS-0006 — Lifecycle State Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

KS-0007 applies that purpose by defining Authority Level behavior that remains portable, interpretable, reviewable, privacy-respecting, provenance-preserving, and independent of any single storage system, workflow engine, agent framework, validation tool, software tool, user interface, graph engine, search system, publication system, or implementation.

TB-0001 establishes the architecture principles that govern The Brain Standard.

KS-0007 applies those principles by requiring Authority Level to preserve:

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

KS-0007 belongs to Layer 1 — Universal Knowledge Standard.

Because Authority Level affects knowledge meaning, interpretation, reviewability, governance, validation, privacy handling, provenance, publication, migration, import, export, automation, and downstream use, KS-0007 defines Authority Level behavior independently of storage systems, user interfaces, folders, filenames, tags, databases, graph tools, workflow engines, agent systems, validation tools, publication systems, and implementations.

Layer 2 storage standards depend on KS-0007 because storage must preserve Authority Level without defining authority meaning.

Layer 3 agent standards depend on KS-0007 because agents may read, propose, classify, validate, route, or recommend authority-related information without becoming unreviewable authorities.

Layer 4 workflow standards depend on KS-0007 because workflows may create, review, approve, reject, limit, revise, validate, publish, import, export, migrate, or preserve Authority Level.

Layer 5 implementation documents depend on KS-0007 because implementations must create, read, preserve, display, migrate, export, import, validate, publish, and synchronize Authority Level without redefining standard-level authority meaning through implementation-specific behavior.

TB-0003 establishes the governance model for The Brain Standard.

KS-0007 follows the document authority hierarchy defined by TB-0003.

As a standard-level document, KS-0007 has high authority within its scope but remains subordinate to constitutional documents.

TB-0003 defines document authority levels for governed documents.

KS-0007 does not replace those document authority rules.

KS-0007 extends authority-level behavior across Knowledge Objects, Knowledge Records, Source References, relationships, provenance records, validation results, workflow outputs, agent outputs, imports, exports, migrations, decisions, and other governed entities.

KS-0001 defines the foundational Knowledge Object Model.

KS-0007 does not replace the Knowledge Object Model.

KS-0007 refines one part of that model: Authority Level.

In practical terms:

- KS-0001 answers: What is a Knowledge Object?
- KS-0001 answers: What is a Knowledge Record?
- KS-0001 answers: Why must Authority Level exist where authority affects interpretation, governance, review, trust, publication, validation, or downstream use?
- KS-0007 answers: How must Authority Level behave?
- KS-0007 answers: What makes Authority Level explicit, scoped, interpretable, portable, reviewable, and validatable?
- KS-0007 answers: How should authority assignment, authority review, authority metadata, source authority, relationship authority, workflow-related authority, agent-related authority, implementation-facing authority, and downstream-use authority be treated?

KS-0002 defines Object Identity.

KS-0007 depends on KS-0002 because Authority Level must not change Object Identity by itself.

A Knowledge Object SHOULD retain its Object Identity when its Authority Level changes.

A Knowledge Object MUST NOT receive a new Object Identity merely because it becomes high-authority, low-authority, reviewed, unreviewed, authoritative, non-authoritative, source-supported, agent-generated, workflow-generated, approved for a narrow scope, deprecated, superseded, archived, restricted, or limited for downstream use.

An identity change MAY occur through a governed process where the Knowledge Object becomes a meaningfully different object, but the authority change alone does not define the identity change.

KS-0003 defines metadata behavior.

KS-0007 depends on KS-0003 because Authority Level may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through authority metadata.

Authority metadata MUST remain distinguishable from Object Identity, lifecycle metadata, privacy metadata, validation metadata, provenance metadata, relationship metadata, Source Reference metadata, workflow metadata, agent metadata, implementation metadata, storage metadata, and hidden application behavior.

KS-0004 defines relationship behavior.

KS-0007 depends on KS-0004 because relationships may have Authority Level and because authority may depend on explicit relationships, relationship provenance, relationship scope, relationship review, relationship validation, relationship lifecycle state, and relationship privacy.

A relationship MAY support authority.

A relationship MAY carry authority.

A relationship MAY limit authority.

A relationship MAY preserve historical authority.

A relationship MUST NOT become authoritative merely because it exists, is linked, is frequently traversed, appears central in a graph, has many backlinks, appears in search results, was inferred by an agent, or was created by an implementation.

KS-0005 defines Source Reference and Provenance behavior.

KS-0007 depends on KS-0005 because Source References, Source Material, evidence, attribution, source authority, source reliability, source availability, extraction history, transformation history, validation history, import provenance, export provenance, migration provenance, and review traceability may support Authority Level.

A Source Reference MAY support Authority Level.

Source authority MAY support Authority Level.

Source reliability MAY inform Authority Level.

Provenance MAY explain why Authority Level was assigned.

However, citation, evidence, attribution, provenance, source existence, source availability, source reliability, source popularity, or source authority MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

KS-0006 defines Lifecycle State behavior.

KS-0007 depends on KS-0006 because Lifecycle State may affect whether authority may be used, limited, suspended, reviewed, deprecated, superseded, archived, restricted, quarantined, repaired, published, exported, migrated, or applied downstream.

Lifecycle State MUST remain distinguishable from Authority Level.

Approval MAY affect authority, but approval does not automatically create unlimited authority.

Authority Level MUST remain scoped.

An entity may be:

- approved but low-authority;
- draft but based on a high-authority source;
- validated but not authoritative;
- private but high-authority;
- public but low-authority;
- superseded but historically authoritative;
- archived but authoritative for historical interpretation;
- agent-generated but not authoritative until reviewed;
- workflow-generated but not authoritative until governed;
- source-supported but not automatically authoritative.

KS-0007 preserves the following KS-0001 rules:

- Authority Level helps humans, agents, workflows, validators, and implementations understand the governance weight or interpretive authority of a Knowledge Object or Knowledge Record.
- Authority Level SHOULD be present or supported where authority affects interpretation, governance, review, trust, publication, validation, or downstream use.
- Authority Level MUST NOT be confused with factual truth, confidence score, popularity, or usefulness.
- Knowledge Objects and Knowledge Records MUST remain implementation-independent, portable, reviewable, and interpretable by humans and AI systems.

KS-0007 preserves the following KS-0002 rules:

- Object Identity remains independent of filenames, folder paths, storage locations, display titles, application-specific identifiers, and implementation-specific behavior.
- Authority changes MUST NOT silently create identity confusion.
- Identity changes SHOULD preserve provenance when assignment, preservation, change, merge, split, redirect, import, export, migration, or supersession affects interpretation or compatibility.

KS-0007 preserves the following KS-0003 rules:

- Authority metadata describes governance weight, review status, interpretive authority, or trust context.
- Authority metadata MUST NOT be confused with factual truth, confidence, popularity, usefulness, source reliability, or lifecycle state.
- Metadata MUST remain explicit, portable, inspectable, reviewable, privacy-respecting, validatable, compatible, governed, maintainable, and implementation-independent.
- Metadata MUST NOT allow workflows, agents, storage systems, or implementations to redefine Knowledge Object meaning by accident.

KS-0007 preserves the following KS-0004 rules:

- Relationships SHOULD remain explicit when they affect interpretation, provenance, lifecycle state, authority, privacy, validation, source traceability, or governance.
- Relationship Authority must remain distinguishable from relationship existence, relationship strength, relationship confidence, graph layout, backlink behavior, and implementation-specific relationship behavior.
- Agent-generated or workflow-generated relationships SHOULD remain reviewable when they affect interpretation, provenance, authority, privacy, lifecycle state, validation, publication, or downstream use.

KS-0007 preserves the following KS-0005 rules:

- Source References and provenance SHOULD preserve evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, validation history, import provenance, export provenance, migration provenance, and review traceability where those affect interpretation.
- Source Material and Knowledge Records SHALL remain distinguishable.
- Source References and provenance MAY support Authority Level, but source existence alone does not automatically create authority.
- Privacy boundaries MUST be preserved when source-reference or provenance information affects authority.

KS-0007 preserves the following KS-0006 rules:

- Lifecycle State MUST remain distinguishable from Authority Level.
- Approval MUST NOT imply unlimited authority.
- Authority MUST NOT imply approval where approval has not occurred.
- Validation success MUST NOT imply authority.
- Agent confidence MUST NOT imply authority.
- Workflow completion MUST NOT imply authority unless a governed workflow specification explicitly defines that result.
- Implementation visibility MUST NOT imply authority.
- Authority Level MUST remain scoped.
- Lifecycle changes MUST NOT silently remove, weaken, expand, transfer, inherit, override, downgrade, upgrade, or reinterpret Authority Level unless a governed process explicitly defines that behavior within a defined scope.

KS-0007 is successful when it extends the prior standards into a clear Authority Level model without weakening Object Identity, metadata role boundaries, relationship behavior, source-reference behavior, provenance preservation, lifecycle-state behavior, privacy boundaries, validation expectations, implementation independence, or practical daily usability.

## 3. Authority Level Definition

Authority Level is the governed interpretive weight, governance weight, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Authority Level exists to help humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations determine how strongly a governed entity may be relied on for interpretation, governance, review, validation, publication, automation, migration, export, import, relationship handling, agent reasoning, workflow behavior, implementation behavior, or downstream use.

A governed entity MAY include:

- a Knowledge Object;
- a Knowledge Record;
- a Source Reference;
- Source Material where applicable;
- a provenance record;
- a relationship;
- a metadata record;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Authority Level SHALL be explicit where authority affects:

- knowledge meaning;
- interpretation;
- governance;
- review;
- validation;
- publication;
- source reliance;
- relationship interpretation;
- workflow behavior;
- agent behavior;
- implementation behavior;
- import;
- export;
- migration;
- compatibility;
- privacy handling;
- downstream use.

Authority Level MUST be scoped.

An entity may be authoritative for one purpose, context, workflow, standard, specification, implementation profile, publication context, migration context, export context, validation context, relationship context, source-reference context, or downstream-use context without being authoritative for every other context.

Authority Level MUST NOT be treated as universal unless a governed authority process explicitly defines that authority as universal within the applicable standard scope.

Authority Level MUST remain distinguishable from Object Identity.

A Knowledge Object remains the same Knowledge Object when its Authority Level changes unless a separate governed identity decision determines that the object itself has become meaningfully different.

Authority Level MUST remain distinguishable from Lifecycle State.

Lifecycle State describes the current governed state of an entity.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to that entity within a defined scope.

An entity may be approved but low-authority.

An entity may be draft but based on a high-authority source.

An entity may be high-authority but superseded.

An entity may be archived but authoritative for historical interpretation.

An entity may be restricted but authoritative for authorized use.

Authority Level MUST remain distinguishable from approval.

Approval means an entity has been accepted for use within a defined scope.

Authority Level describes how much interpretive, governance, review, or use weight the entity carries within a defined scope.

Approval MAY support Authority Level.

Approval MUST NOT automatically create unlimited authority.

Authority Level MUST remain distinguishable from Validation State.

Validation State describes whether an entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

A valid entity may be low-authority.

An invalid entity may still preserve historically important authority context.

A validation-passing entity MUST NOT be treated as authoritative unless a governed authority process explicitly defines that result within a defined scope.

Authority Level MUST remain distinguishable from Privacy Classification.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.

Authority Level describes governance weight, interpretive authority, review weight, trust boundary, or use-authority.

A private entity may be high-authority.

A public entity may be low-authority.

A restricted entity may be authoritative only for authorized reviewers, workflows, agents, validators, implementations, or downstream uses.

Authority Level MUST NOT weaken privacy requirements.

Privacy Classification SHALL take precedence over operational convenience when authority handling creates privacy risk.

Authority Level MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context.

Provenance MAY support Authority Level.

Provenance MAY explain why Authority Level was assigned.

Provenance MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Authority Level MUST remain distinguishable from Source References.

A Source Reference may support, explain, contextualize, contradict, originate, or otherwise relate to a governed entity.

A Source Reference MAY support Authority Level.

A Source Reference MUST NOT automatically create Authority Level merely because a source exists, is cited, is available, is reliable, is official, is popular, is frequently referenced, or appears authoritative.

Authority Level MUST remain distinguishable from Source Reliability.

Source Reliability describes assessed trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength of Source Material.

A reliable source may support Authority Level.

A reliable source does not automatically make a Knowledge Record authoritative.

An unreliable source may still be relevant for historical, evidentiary, contradiction, attribution, or review purposes without becoming authoritative.

Authority Level MUST remain distinguishable from Relationship Authority.

A relationship may carry authority-related meaning.

A relationship may support, limit, transfer, preserve, or contextualize authority where a governed authority process defines that behavior.

A relationship MUST NOT automatically create Authority Level merely because it exists, is linked, is frequently traversed, appears central in a graph, has many backlinks, appears in search results, was inferred by an agent, or was created by an implementation.

Authority Level MUST remain distinguishable from Agent Confidence.

Agent Confidence describes an agent-generated indication of certainty, probability, model confidence, classification confidence, extraction confidence, relationship confidence, validation confidence, or recommendation confidence.

Agent Confidence MAY support review.

Agent Confidence MUST NOT create Authority Level by itself.

An agent-generated output is not authoritative unless reviewed, accepted, or governed through an authority process within a defined scope.

Authority Level MUST remain distinguishable from Workflow Completion.

Workflow Completion describes the successful completion of a workflow step, workflow stage, workflow run, task sequence, automation, routing path, review queue, or operational procedure.

Workflow Completion MAY support authority assignment where a governed workflow explicitly defines that result.

Workflow Completion MUST NOT create Authority Level by itself.

Authority Level MUST remain distinguishable from Implementation Visibility.

Implementation Visibility describes whether a governed entity is visible, surfaced, indexed, ranked, displayed, searched, cached, routed, filtered, published, synchronized, or exposed by a specific implementation.

Implementation Visibility MAY support discovery.

Implementation Visibility MUST NOT define Authority Level.

Search ranking, graph centrality, backlink count, usage frequency, folder placement, filename, tag, color, icon, user-interface state, plugin field, database row, cache state, workflow queue, agent task label, or implementation-specific status label MUST NOT define Authority Level by itself.

Authority Level SHOULD be portable.

Authority Level SHOULD remain meaningful when a governed entity is renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, reindexed, summarized, translated, validated, processed by an agent, processed by a workflow, archived, restricted, published, or accessed through a different implementation.

Authority Level SHOULD be reviewable.

A future human, agent, workflow, validator, storage system, migration process, import process, export process, publication process, or implementation SHOULD be able to determine what Authority Level applies, what scope applies, how the Authority Level was assigned where applicable, what provenance supports the assignment where applicable, and whether the Authority Level affects downstream use.

Authority Level SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, rename, reinterpret, expose, replace, promote, demote, inherit, transfer, or regenerate Authority Level in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority Level is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what authority applies to a governed entity, what scope the authority applies within, what supports the authority, what limits the authority, whether the authority is current or historical, whether review or validation is required, whether privacy or lifecycle handling affects authority, and whether the authority remains meaningful across time and implementation replacement.

## 4. Authority Level Requirements

Authority Level Requirements define the minimum behavior required for Authority Level to remain explicit, scoped, interpretable, reviewable, portable, privacy-respecting, provenance-preserving, validatable, compatible, and governable under KS-0007.

A governed entity SHALL include or support Authority Level where authority affects meaning, interpretation, governance, review, validation, publication, source reliance, relationship interpretation, workflow behavior, agent behavior, implementation behavior, import, export, migration, compatibility, privacy handling, or downstream use.

A governed entity MAY include:

- a Knowledge Object;
- a Knowledge Record;
- a Source Reference;
- Source Material where applicable;
- a provenance record;
- a relationship;
- a metadata record;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Authority Level SHALL be explicit enough that future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine how the governed entity may be interpreted, relied on, reviewed, validated, published, exported, migrated, automated, or used downstream.

Authority Level MUST be scoped.

An Authority Level without scope is incomplete where authority affects governed interpretation or use.

Authority scope SHOULD identify or support identification of:

- what entity the Authority Level applies to;
- what authority applies;
- what purpose the authority applies within;
- what context the authority applies within;
- who or what assigned the authority where applicable;
- when the authority was assigned where applicable;
- what review supports the authority where applicable;
- what validation supports the authority where applicable;
- what provenance supports the authority where applicable;
- what Source References support the authority where applicable;
- what relationships support or limit the authority where applicable;
- what lifecycle state affects the authority where applicable;
- what privacy classification affects the authority where applicable;
- what compatibility constraints affect the authority where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Authority Level MUST NOT depend only on hidden implementation behavior, storage location, folder placement, filename, tag, color, icon, user-interface state, workflow memory, agent memory, plugin behavior, database state, search ranking, graph position, backlink behavior, popularity, usage frequency, or undocumented convention.

Those signals MAY support discovery, routing, display, review, validation, implementation behavior, workflow convenience, or agent assistance.

They MUST NOT replace explicit Authority Level where authority affects governed meaning or use.

Authority Level MUST remain distinguishable from Object Identity.

An authority change MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when its Authority Level changes unless a separate governed identity decision determines that the object has become meaningfully different.

Authority Level MUST remain distinguishable from Lifecycle State.

A lifecycle state MAY affect how authority is assigned, reviewed, limited, suspended, deprecated, superseded, archived, restricted, published, exported, migrated, or used downstream.

Lifecycle State MUST NOT replace Authority Level.

Approval MAY support authority, but approval MUST NOT automatically create unlimited authority.

Rejection MAY limit authority, but rejection MUST NOT erase historical authority context where that context remains relevant for governance, provenance, source traceability, compatibility, migration, or review.

Deprecation MAY reduce future use-authority, but deprecation MUST NOT erase historical interpretive authority where the deprecated entity remains relevant for historical interpretation, compatibility, migration, governance, or audit.

Supersession MAY replace current authority, but supersession MUST NOT silently transfer all authority from the superseded entity to the superseding entity unless a governed process explicitly defines that transfer within a defined scope.

Archival MAY preserve authority for historical interpretation, but archival MUST NOT make an entity active, public, exportable, publishable, or broadly authoritative by itself.

Restriction MAY limit who or what may use authority, but restriction MUST NOT erase the authority record.

Quarantine MAY suspend authority use, but quarantine MUST NOT silently delete authority history.

Authority Level MUST remain distinguishable from Validation State.

Validation MAY support authority.

Validation MUST NOT equal authority unless a governed authority process, workflow, or specification explicitly defines that result within a defined scope.

A valid entity MAY be low-authority.

An invalid entity MAY preserve historical authority context.

A validation result MUST NOT silently promote, demote, approve, reject, suspend, inherit, transfer, or remove Authority Level unless a governed process explicitly permits that behavior within a defined scope.

Authority Level MUST remain distinguishable from Privacy Classification.

Authority Level MUST NOT weaken privacy requirements.

A high-authority entity MAY still be private, restricted, confidential, sensitive, non-exportable, agent-restricted, publication-restricted, or otherwise governed by privacy controls.

A low-authority entity MAY still require strong privacy protection.

Privacy Classification SHALL take precedence over operational convenience when authority handling creates privacy risk.

Authority Level MUST remain distinguishable from Provenance.

Provenance MAY support authority assignment, authority review, authority limitation, authority suspension, authority inheritance, authority transfer, authority downgrade, authority escalation, authority publication, authority migration, authority import, authority export, or authority preservation.

Provenance MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Authority Level SHOULD preserve provenance where authority affects interpretation, governance, review, validation, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, import, export, migration, or downstream use.

Authority Level MUST remain distinguishable from Source References.

A Source Reference MAY support authority.

A Source Reference MUST NOT automatically create authority.

Source existence, citation, availability, reliability, official status, popularity, frequency of citation, or source authority MUST NOT automatically make a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, or other governed entity authoritative unless a governed authority process explicitly defines that result within a defined scope.

Authority Level MUST remain distinguishable from Source Reliability.

Source Reliability MAY inform authority review.

Source Reliability MUST NOT replace Authority Level.

A reliable source may support a low-authority record if the record has not been reviewed, validated, scoped, or governed.

An unreliable source may still be preserved for contradiction, attribution, historical interpretation, evidence review, or source-quality analysis without becoming authoritative.

Authority Level MUST remain distinguishable from Relationship Authority.

A relationship MAY have its own Authority Level.

A relationship MAY support, limit, contextualize, preserve, inherit, transfer, downgrade, escalate, or contradict authority only where a governed authority process explicitly defines that behavior within a defined scope.

Relationship existence MUST NOT create authority by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, or implementation-specific links MUST NOT create Authority Level by themselves.

Authority Level MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support review, validation, routing, triage, prioritization, or human decision-making.

Agent Confidence MUST NOT create Authority Level by itself.

An agent MAY propose an Authority Level.

An agent MUST NOT become an unreviewable authority for assigning, escalating, downgrading, removing, transferring, publishing, exporting, migrating, or applying Authority Level where authority affects governed interpretation or use.

Agent-generated authority recommendations SHOULD remain reviewable where they affect meaning, governance, validation, privacy, publication, export, migration, relationships, Source References, provenance, lifecycle handling, compatibility, or downstream use.

Authority Level MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support Authority Level where a governed workflow explicitly defines that completion as part of an authority process.

Workflow Completion MUST NOT create Authority Level by itself.

A workflow MAY propose, route, review, validate, assign, limit, suspend, escalate, downgrade, transfer, preserve, or remove Authority Level only where the applicable workflow is governed to perform that role.

Workflow-generated authority changes SHOULD preserve enough provenance for future review where authority affects interpretation, governance, validation, privacy, publication, export, migration, relationships, Source References, lifecycle handling, compatibility, or downstream use.

Authority Level MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT define authority.

A governed entity MUST NOT become authoritative merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose Authority Level merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority Level SHOULD support review.

A reviewer SHOULD be able to determine:

- what Authority Level applies;
- whether the Authority Level is appropriate;
- what authority scope applies;
- whether the Authority Level was assigned through a governed process where required;
- whether the Authority Level is current or historical;
- whether the Authority Level is proposed, reviewed, approved, limited, suspended, inherited, transferred, downgraded, escalated, deprecated, superseded, archived, restricted, or otherwise governed;
- whether provenance supports the Authority Level;
- whether Source References support or limit the Authority Level;
- whether relationships support or limit the Authority Level;
- whether lifecycle state affects the Authority Level;
- whether privacy classification constrains authority handling;
- whether validation supports or challenges the Authority Level;
- whether compatibility, import, export, migration, publication, workflow behavior, agent behavior, implementation behavior, or downstream use is affected.

Authority Level SHOULD support validation.

A validator SHOULD be able to determine whether:

- Authority Level is present where required;
- Authority Level is scoped where required;
- Authority Level uses a governed value where a governed vocabulary exists;
- Authority Level is distinguishable from Object Identity, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Source Reliability, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- authority assignment preserves required provenance where applicable;
- authority review requirements are satisfied where applicable;
- authority changes preserve Object Identity;
- authority handling preserves privacy boundaries;
- authority handling preserves relationship meaning;
- authority handling preserves Source Reference and provenance context;
- authority handling remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority Level SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate Authority Level in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority Level SHOULD support historical preservation.

A governed entity MAY retain historical Authority Level even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical authority does not mean the entity remains current.

Historical authority does not mean the entity is approved for future use.

Historical authority does not mean the entity is public, exportable, publishable, valid, unrestricted, safe for agent use, or safe for downstream use.

Historical authority SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, and provenance review.

Authority Level Requirements are successful when Authority Level remains explicit, scoped, distinguishable, reviewable, portable, privacy-respecting, provenance-preserving, validatable, compatible, and governable across review, validation, approval, publication, import, export, migration, lifecycle handling, relationship handling, source-reference handling, workflow activity, agent activity, storage replacement, and implementation replacement.

## 5. Authority Level Categories

Authority Level Categories organize Authority Level by architectural purpose.

Authority Level Categories help humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations understand what kind of authority applies, what role the authority serves, what scope limits it, and how it should affect interpretation, governance, validation, publication, privacy handling, relationships, Source References, provenance, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, and downstream use.

KS-0007 defines Authority Level Categories at the conceptual standard level.

KS-0007 does not define an exhaustive controlled vocabulary of exact authority values.

A future authority specification MAY define exact authority values, allowed authority scopes, assignment rules, review rules, validation rules, publication rules, inheritance rules, limitation rules, suspension rules, transfer rules, downgrade rules, escalation rules, import mappings, export mappings, migration mappings, workflow effects, agent handling rules, implementation behavior, and serialization syntax.

At minimum, The Brain Standard recognizes the following Authority Level Categories:

- governance authority;
- interpretive authority;
- review authority;
- use-authority;
- source-supported authority;
- relationship authority;
- validation-supported authority;
- workflow-supported authority;
- agent-proposed authority;
- implementation-facing authority;
- publication authority;
- import, export, and migration authority;
- historical authority;
- restricted authority;
- provisional authority.

### 5.1 Governance Authority

Governance Authority describes the degree to which a governed entity may influence rules, standards, specifications, decisions, compatibility expectations, approval processes, workflows, implementations, or downstream governance.

Governance Authority MAY apply to:

- constitutional documents;
- standards;
- specifications;
- ADRs;
- accepted RFCs;
- governance decisions;
- approval records;
- compatibility records;
- migration decisions;
- implementation compliance decisions;
- other governed entities where governance weight affects interpretation or use.

Governance Authority MUST remain compatible with the document authority hierarchy defined by TB-0003.

KS-0007 does not replace TB-0003 document authority levels.

A governed document may have document authority under TB-0003 and Authority Level under KS-0007, but those concepts MUST remain distinguishable.

Governance Authority SHOULD identify or support identification of:

- what governed entity carries governance authority;
- what governance scope applies;
- what higher-authority documents govern the entity;
- what lower-authority documents, workflows, agents, implementations, or decisions may depend on the entity;
- what approval, review, provenance, lifecycle state, validation, privacy classification, compatibility context, or supersession context affects the authority.

Governance Authority MUST NOT arise merely from repeated practice, implementation behavior, agent output, workflow completion, folder placement, popularity, search ranking, graph centrality, or undocumented habit.

### 5.2 Interpretive Authority

Interpretive Authority describes the degree to which a governed entity may be relied on to guide meaning, interpretation, classification, explanation, relationship handling, source interpretation, validation interpretation, or decision support within a defined scope.

Interpretive Authority MAY apply to:

- Knowledge Objects;
- Knowledge Records;
- Source References;
- provenance records;
- relationships;
- standards;
- specifications;
- decisions;
- reviewed summaries;
- validated interpretations;
- other governed entities where interpretation affects use.

Interpretive Authority MUST be scoped.

A Knowledge Record may be authoritative for one interpretation while remaining non-authoritative for another interpretation.

A source-supported interpretation may be high-authority for historical explanation but low-authority for current operational use.

An interpretation that is useful, popular, clear, frequently cited, or frequently linked is not automatically authoritative.

Interpretive Authority SHOULD preserve provenance, Source References, relationship context, lifecycle state, validation state, review context, and privacy classification where those affect interpretation.

Interpretive Authority MUST NOT be confused with factual truth.

A high-authority interpretation may still be revised, superseded, limited, contradicted, deprecated, or rejected through governed review.

### 5.3 Review Authority

Review Authority describes the degree to which a governed entity has been reviewed, accepted, trusted, limited, challenged, or approved for review-dependent use within a defined scope.

Review Authority MAY apply to:

- human-reviewed Knowledge Records;
- reviewed relationships;
- reviewed Source References;
- reviewed provenance records;
- reviewed validation results;
- reviewed workflow outputs;
- reviewed agent outputs;
- reviewed import records;
- reviewed export records;
- reviewed migration records;
- governed documents;
- decisions;
- other reviewed entities.

Review Authority MUST identify or support identification of what review occurred where applicable.

Review MAY support Authority Level.

Review MUST NOT automatically create unlimited authority.

A reviewed entity may still be low-authority if the review was limited, incomplete, narrow, provisional, outdated, contradicted, privacy-constrained, validation-limited, or outside the relevant authority scope.

A non-reviewed entity may still preserve historical authority context, but it SHOULD NOT be treated as authoritative for review-dependent use unless a governed process explicitly permits that behavior.

Review Authority SHOULD remain traceable to the reviewer, workflow, validation process, governance process, approval record, or other review context where that context affects interpretation or downstream use.

### 5.4 Use-Authority

Use-Authority describes whether and how a governed entity may be used for a particular purpose within a defined scope.

Use-Authority MAY apply to:

- interpretation;
- governance;
- publication;
- export;
- migration;
- validation;
- relationship creation;
- source reliance;
- decision support;
- workflow execution;
- agent reasoning;
- implementation behavior;
- downstream use.

Use-Authority MUST be scoped to the intended purpose.

An entity may be authorized for internal review but not publication.

An entity may be authorized for historical interpretation but not current operational guidance.

An entity may be authorized for migration analysis but not export.

An entity may be authorized for agent reading but not agent modification.

An entity may be authorized for validation but not governance.

Use-Authority MUST preserve privacy boundaries.

Use-Authority MUST NOT override Privacy Classification, Lifecycle State, validation failure, restriction, quarantine, source limitations, relationship limitations, compatibility concerns, or governance constraints.

Use-Authority SHOULD identify or support identification of the permitted use, prohibited use, restricted use, conditional use, and downstream-use limits where applicable.

### 5.5 Source-Supported Authority

Source-Supported Authority describes Authority Level that is supported, limited, explained, challenged, or contextualized by Source Material, Source References, evidence, attribution, source reliability, source authority, source availability, extraction history, transformation history, or provenance.

Source-Supported Authority MAY apply when a governed entity depends on Source Material for interpretation, review, validation, publication, relationship creation, decision support, or downstream use.

Source-Supported Authority MUST preserve the distinction between Source Material and Knowledge Records.

A Source Reference MAY support authority.

A Source Reference MUST NOT automatically create authority.

Source reliability MAY inform authority review.

Source reliability MUST NOT replace Authority Level.

Source authority MAY support Authority Level within a defined scope.

Source authority MUST NOT automatically transfer to a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity unless a governed authority process explicitly defines that transfer.

Source-Supported Authority SHOULD identify or support identification of:

- what Source Material supports the authority;
- what Source References apply;
- whether the source is available, unavailable, restricted, superseded, contradicted, uncertain, or incomplete;
- what extraction or transformation occurred;
- what provenance supports the source use;
- what privacy classification applies;
- what review or validation supports the authority;
- what authority scope applies.

### 5.6 Relationship Authority

Relationship Authority describes Authority Level assigned to a relationship or authority meaning carried, supported, limited, preserved, inherited, transferred, downgraded, escalated, contradicted, or contextualized through a relationship within a defined scope.

Relationship Authority MAY apply to:

- explicit relationships;
- reviewed relationships;
- provenance-supported relationships;
- source-supported relationships;
- lifecycle-sensitive relationships;
- relationship records;
- relationship metadata;
- relationships between standards;
- relationships between Knowledge Objects;
- relationships between Knowledge Records;
- relationships between Source Material and Knowledge Records;
- relationships between decisions, workflows, agents, implementations, imports, exports, or migrations.

A relationship MAY have its own Authority Level.

A relationship MAY support Authority Level for another governed entity.

A relationship MAY limit Authority Level for another governed entity.

A relationship MAY preserve historical authority.

A relationship MAY support authority inheritance or authority transfer only where a governed authority process explicitly defines that behavior within a defined scope.

Relationship existence MUST NOT create authority by itself.

Relationship strength MUST NOT create authority by itself.

Relationship confidence MUST NOT create authority by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create Authority Level by themselves.

Relationship Authority SHOULD preserve relationship type, direction, participants, context, provenance, lifecycle state, validation state, privacy classification, compatibility, and authority scope where those affect interpretation or use.

### 5.7 Validation-Supported Authority

Validation-Supported Authority describes Authority Level that is supported, limited, challenged, suspended, or reviewed based on validation results within a defined scope.

Validation-Supported Authority MAY apply when validation affects:

- structural compliance;
- metadata completeness;
- Object Identity preservation;
- relationship validity;
- Source Reference validity;
- provenance sufficiency;
- lifecycle-state handling;
- authority scope;
- privacy handling;
- compatibility;
- publication;
- import;
- export;
- migration;
- workflow behavior;
- agent behavior;
- implementation behavior;
- downstream use.

Validation MAY support authority.

Validation MUST NOT equal authority unless a governed authority process, workflow, or specification explicitly defines that result within a defined scope.

A validation-passing entity may remain low-authority.

A validation-failing entity may retain historical authority context.

A validation result MAY trigger review, repair, limitation, suspension, downgrade, escalation, quarantine, or other governed authority handling only where a governed process defines that behavior.

Validation-Supported Authority SHOULD preserve the validation result, validation date, validator, validation scope, validation profile, validation errors, validation warnings, authority impact, review requirements, provenance, privacy impact, and compatibility impact where applicable.

### 5.8 Workflow-Supported Authority

Workflow-Supported Authority describes Authority Level that is proposed, routed, reviewed, validated, assigned, limited, suspended, escalated, downgraded, transferred, preserved, removed, or otherwise affected by a governed workflow.

Workflow-Supported Authority MAY apply to:

- workflow outputs;
- workflow decisions;
- review workflows;
- approval workflows;
- validation workflows;
- publication workflows;
- import workflows;
- export workflows;
- migration workflows;
- repair workflows;
- archival workflows;
- agent-assisted workflows;
- other governed workflows.

Workflow completion MAY support Authority Level where a governed workflow explicitly defines that completion as part of an authority process.

Workflow completion MUST NOT create Authority Level by itself.

A workflow MUST NOT become an unreviewable authority for assigning, escalating, downgrading, removing, transferring, publishing, exporting, migrating, or applying Authority Level where authority affects governed interpretation or use.

Workflow-Supported Authority SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, validation, privacy, publication, export, migration, relationships, Source References, lifecycle handling, compatibility, or downstream use.

### 5.9 Agent-Proposed Authority

Agent-Proposed Authority describes authority-related recommendations, classifications, flags, confidence signals, proposals, or suggested authority changes created by an agent.

Agent-Proposed Authority MAY include:

- proposed Authority Level;
- proposed authority scope;
- proposed source-supported authority;
- proposed relationship authority;
- proposed validation-supported authority;
- proposed workflow-supported authority;
- proposed downgrade;
- proposed escalation;
- proposed limitation;
- proposed suspension;
- proposed review requirement;
- proposed authority conflict.

Agent-Proposed Authority is not authoritative by itself.

Agent Confidence MUST NOT create Authority Level by itself.

An agent MAY propose Authority Level.

An agent MUST NOT become an unreviewable authority for assigning, escalating, downgrading, removing, transferring, publishing, exporting, migrating, or applying Authority Level where authority affects governed interpretation or use.

Agent-Proposed Authority SHOULD remain traceable to the agent, model class, instruction, workflow, source material, evidence, validation result, relationship context, confidence signal, review state, and human decision where applicable.

Agent-Proposed Authority SHOULD remain clearly distinguishable from human-approved authority, workflow-approved authority, validation-supported authority, source-supported authority, and governed Authority Level.

### 5.10 Implementation-Facing Authority

Implementation-Facing Authority describes how Authority Level may be displayed, routed, filtered, indexed, synchronized, published, exported, imported, migrated, cached, hidden, ranked, or otherwise handled by a specific implementation.

Implementation-Facing Authority MAY support:

- dashboards;
- review queues;
- publication queues;
- validation reports;
- authority badges;
- filters;
- search facets;
- graph views;
- source review views;
- relationship review views;
- migration reports;
- import reports;
- export reports;
- agent task lists;
- workflow routing.

Implementation-facing authority behavior MAY support usability.

Implementation-facing authority behavior MUST remain subordinate to standard-level Authority Level meaning.

An implementation MUST NOT define authority by itself.

A governed entity MUST NOT become authoritative merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, frequently used, or treated as important by a specific implementation.

A governed entity MUST NOT lose Authority Level merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Implementation-Facing Authority SHOULD preserve standard-level authority meaning across migration, export, import, backup, restoration, synchronization, publication, validation, workflow activity, agent activity, and implementation replacement.

### 5.11 Publication Authority

Publication Authority describes whether and how a governed entity may be used, exposed, cited, summarized, exported, synchronized, shared, or published within a defined publication context.

Publication Authority MAY apply to:

- public documents;
- internal documents;
- Knowledge Objects;
- Knowledge Records;
- source-derived summaries;
- Source References;
- provenance records;
- relationships;
- validation results;
- workflow outputs;
- agent outputs;
- exported records;
- implementation views;
- publication packages.

Publication Authority MUST be scoped.

An entity may be authoritative for internal use but not publication.

An entity may be approved for publication but not authoritative for broader governance.

An entity may be public but low-authority.

An entity may be private but high-authority.

Publication Authority MUST preserve Privacy Classification.

Publication Authority MUST preserve Source Reference and provenance constraints.

Publication Authority MUST preserve lifecycle limitations.

Publication Authority MUST preserve validation limitations.

Publication Authority MUST preserve relationship limitations.

Publication Authority MUST preserve compatibility limitations.

Publication Authority MUST NOT expose restricted, confidential, sensitive, private, non-exportable, unpublished, quarantined, or otherwise limited content merely because the content is authoritative within another scope.

### 5.12 Import, Export, and Migration Authority

Import, Export, and Migration Authority describes how Authority Level is preserved, limited, reviewed, mapped, suspended, downgraded, escalated, transferred, or re-established when governed entities move between systems, repositories, vaults, formats, implementations, standards versions, workflows, or storage environments.

Import Authority MAY describe whether imported authority may be trusted, limited, reviewed, mapped, suspended, or treated as provisional.

Export Authority MAY describe whether authority may be carried out of a compliant environment and under what conditions.

Migration Authority MAY describe whether authority remains meaningful after movement, conversion, mapping, transformation, validation, or implementation replacement.

Import, Export, and Migration Authority MUST preserve Object Identity where applicable.

Import, Export, and Migration Authority MUST preserve authority scope.

Import, Export, and Migration Authority MUST preserve provenance where authority interpretation depends on origin, source, review, validation, workflow, agent, import, export, or migration context.

Import, Export, and Migration Authority MUST preserve privacy boundaries.

Authority MUST NOT be silently upgraded, downgraded, inherited, transferred, removed, suspended, or regenerated during import, export, or migration unless a governed process explicitly defines that behavior within a defined scope.

A migrated entity MAY require review before its prior Authority Level is treated as current, active, publishable, exportable, agent-usable, or safe for downstream use.

### 5.13 Historical Authority

Historical Authority describes Authority Level preserved for historical interpretation, audit, governance review, compatibility review, source traceability, provenance review, migration analysis, restoration, supersession, deprecation, rejection, archival, or other historical purposes.

Historical Authority MAY apply to:

- deprecated entities;
- superseded entities;
- rejected entities;
- archived entities;
- restricted entities;
- quarantined entities;
- repaired entities;
- migrated entities;
- imported entities;
- exported entities;
- prior versions;
- prior decisions;
- prior relationships;
- prior Source References;
- prior validation results;
- prior workflow outputs;
- prior agent outputs.

Historical Authority does not mean the entity remains current.

Historical Authority does not mean the entity is approved for future use.

Historical Authority does not mean the entity is public, exportable, publishable, valid, unrestricted, safe for agent use, or safe for downstream use.

Historical Authority SHOULD preserve enough context for future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations to determine what authority existed, what scope applied, why it mattered, what replaced it where applicable, what limitations apply, and whether it remains relevant for interpretation.

### 5.14 Restricted Authority

Restricted Authority describes Authority Level that may exist but may only be used, viewed, processed, exported, published, synchronized, indexed, routed, or acted on under constrained conditions.

Restricted Authority MAY apply where authority intersects with:

- privacy classification;
- access limits;
- source restrictions;
- legal constraints;
- ethical constraints;
- contractual constraints;
- safety concerns;
- confidentiality requirements;
- non-exportable records;
- agent-restricted content;
- publication-restricted content;
- quarantined records;
- sensitive relationships;
- restricted provenance;
- restricted Source References.

Restricted Authority MUST preserve privacy boundaries.

Restriction does not erase Authority Level.

Restriction limits how authority may be used.

A restricted high-authority entity may be authoritative only for authorized users, workflows, agents, validators, implementations, exports, migrations, publications, or downstream uses.

A restricted entity MUST NOT become public, exportable, publishable, agent-readable, searchable, synchronized, or implementation-visible merely because it carries high Authority Level.

Restricted Authority SHOULD identify or support identification of the restriction, permitted use, prohibited use, authorized review context, authority scope, privacy classification, provenance constraints, source constraints, relationship constraints, publication limits, export limits, migration limits, agent limits, and downstream-use limits where applicable.

### 5.15 Provisional Authority

Provisional Authority describes Authority Level that is temporary, proposed, pending review, pending validation, pending approval, pending source verification, pending privacy review, pending migration review, or otherwise not yet fully accepted for governed use.

Provisional Authority MAY apply to:

- draft Knowledge Objects;
- draft Knowledge Records;
- proposed relationships;
- proposed Source References;
- proposed provenance records;
- agent-generated outputs;
- workflow-generated outputs;
- imported records awaiting review;
- migrated records awaiting validation;
- validation results awaiting human review;
- publication candidates;
- authority assignments awaiting approval;
- authority changes awaiting governance review.

Provisional Authority MUST be clearly distinguishable from reviewed, approved, current, final, publication-ready, export-ready, migration-ready, or downstream-use authority.

Provisional Authority MAY support limited temporary use where a governed process permits that use within a defined scope.

Provisional Authority MUST NOT be treated as final authority unless a governed review, validation, approval, or authority process explicitly changes its authority status.

Provisional Authority SHOULD preserve enough context for future review, including what authority was proposed, who or what proposed it, what scope applies, what evidence supports it, what validation exists, what review remains, what privacy limits apply, what lifecycle state applies, and what downstream-use limits exist.

### 5.16 Authority Level Category Success

Authority Level Categories are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what kind of authority applies, what scope applies, what supports the authority, what limits the authority, whether the authority is current or historical, whether the authority is provisional or approved, whether privacy or lifecycle handling constrains the authority, whether validation or source support affects the authority, whether relationships affect the authority, whether agent or workflow activity requires review, and whether the authority remains meaningful across implementation replacement.

## 6. Authority Scope

Authority Scope defines the context, boundary, purpose, use, condition, or domain within which an Authority Level applies.

Authority Scope exists because Authority Level is not automatically universal.

A governed entity may carry high Authority Level in one scope while carrying lower, limited, provisional, historical, restricted, or no Authority Level in another scope.

Authority Scope helps humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations determine where authority applies, where authority does not apply, and what conditions limit authority use.

Authority Scope SHALL be explicit where Authority Level affects:

- knowledge meaning;
- interpretation;
- governance;
- review;
- validation;
- publication;
- source reliance;
- relationship interpretation;
- workflow behavior;
- agent behavior;
- implementation behavior;
- import;
- export;
- migration;
- compatibility;
- privacy handling;
- downstream use.

Authority Scope MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a Source Reference;
- Source Material where applicable;
- a provenance record;
- a relationship;
- a metadata record;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Authority Scope SHOULD identify or support identification of:

- what entity the Authority Level applies to;
- what Authority Level applies;
- what purpose the authority applies within;
- what context the authority applies within;
- what standard, specification, workflow, implementation profile, publication context, import context, export context, migration context, validation context, relationship context, source-reference context, privacy context, or downstream-use context applies;
- who or what assigned the Authority Level where applicable;
- who or what reviewed the Authority Level where applicable;
- what provenance supports the Authority Level where applicable;
- what Source References support or limit the Authority Level where applicable;
- what relationships support or limit the Authority Level where applicable;
- what lifecycle state affects the Authority Level where applicable;
- what validation state affects the Authority Level where applicable;
- what privacy classification affects the Authority Level where applicable;
- what compatibility constraints affect the Authority Level where applicable;
- what permitted uses, restricted uses, prohibited uses, or conditional uses apply where applicable.

Authority Scope MUST remain distinguishable from Authority Level.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity.

Authority Scope describes where, when, why, how, or for what purpose that Authority Level applies.

An Authority Level without adequate scope is incomplete where authority affects governed interpretation or use.

Authority Scope MUST remain distinguishable from Object Identity.

Changing authority scope MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when its Authority Scope changes unless a separate governed identity decision determines that the object has become meaningfully different.

Authority Scope MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether authority is current, limited, suspended, deprecated, superseded, archived, restricted, quarantined, provisional, or historically preserved.

Lifecycle State does not define Authority Scope by itself.

An approved entity may be authoritative only within a narrow scope.

A draft entity may be based on a high-authority source but remain non-authoritative for publication.

A superseded entity may remain authoritative for historical interpretation but not current use.

An archived entity may remain authoritative for audit or compatibility review but not active workflow use.

Authority Scope MUST remain distinguishable from approval scope.

Approval scope describes the context in which an entity has been accepted for use.

Authority Scope describes the context in which an entity carries governance weight, interpretive authority, review weight, trust boundary, or use-authority.

Approval scope MAY support Authority Scope.

Approval scope MUST NOT automatically create broad Authority Scope.

Approval in one scope MUST NOT imply authority in every scope.

Authority Scope MUST remain distinguishable from Validation Scope.

Validation Scope describes the context in which validation was performed.

Authority Scope describes the context in which authority applies.

Validation within one scope MAY support authority within that same scope.

Validation within one scope MUST NOT automatically create authority in another scope.

A validation-passing entity may still be non-authoritative outside the validated scope.

A validation-failing entity may retain historical authority within a historical or audit scope.

Authority Scope MUST remain distinguishable from Privacy Scope.

Privacy Scope describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.

Authority Scope describes the context in which Authority Level applies.

Authority Scope MUST NOT weaken privacy boundaries.

A high-authority entity may remain private, restricted, confidential, sensitive, non-exportable, agent-restricted, publication-restricted, or otherwise constrained.

A public entity may remain low-authority or non-authoritative.

Where Authority Scope and Privacy Scope conflict, privacy SHALL take precedence over operational convenience.

Authority Scope MUST remain distinguishable from Source Scope.

Source Scope describes the context in which Source Material, Source References, source reliability, source authority, source availability, attribution, extraction history, transformation history, or provenance supports interpretation.

Authority Scope describes the context in which a governed entity may be treated as authoritative.

A high-authority source within one context does not automatically make every derived Knowledge Record authoritative.

A Source Reference may support Authority Scope only where the source, evidence, provenance, review, validation, and governed authority process support that scope.

A Source Reference MUST NOT automatically expand Authority Scope merely because the source exists, is cited, is available, is reliable, official, popular, frequently referenced, or appears authoritative.

Authority Scope MUST remain distinguishable from Relationship Scope.

Relationship Scope describes the context, direction, type, participants, meaning, lifecycle state, validation state, privacy classification, provenance, or compatibility constraints of a relationship.

Authority Scope describes the context in which authority applies.

A relationship may support, limit, transfer, preserve, inherit, downgrade, escalate, or contextualize Authority Scope only where a governed authority process explicitly defines that behavior.

Relationship existence MUST NOT create or expand Authority Scope by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create or expand Authority Scope by themselves.

Authority Scope MUST remain distinguishable from Agent Scope.

Agent Scope describes what an agent may read, propose, classify, validate, summarize, modify, route, export, migrate, publish, or otherwise process.

Authority Scope describes where Authority Level applies.

An agent MAY propose Authority Scope.

An agent MUST NOT become an unreviewable authority for assigning, expanding, narrowing, transferring, downgrading, escalating, suspending, removing, publishing, exporting, migrating, or applying Authority Scope where authority affects governed interpretation or use.

Agent access to a governed entity MUST NOT imply authority to use that entity in every scope.

Agent Confidence MUST NOT create Authority Scope by itself.

Authority Scope MUST remain distinguishable from Workflow Scope.

Workflow Scope describes the boundary within which a workflow operates.

Authority Scope describes the boundary within which Authority Level applies.

A workflow MAY propose, route, review, validate, assign, limit, suspend, escalate, downgrade, transfer, preserve, or remove Authority Scope only where the applicable workflow is governed to perform that role.

Workflow completion MUST NOT create or expand Authority Scope by itself.

A workflow completed successfully within one scope MUST NOT make the governed entity authoritative in another scope unless a governed workflow specification explicitly defines that result.

Authority Scope MUST remain distinguishable from Implementation Scope.

Implementation Scope describes the boundary of a specific software system, vault, database, file system, interface, plugin, workflow environment, agent system, publication system, or tool.

Authority Scope describes the boundary within which authority applies.

A governed entity MUST NOT become authoritative merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose Authority Scope merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority Scope SHOULD be portable.

Authority Scope SHOULD remain meaningful when a governed entity is renamed, moved, copied, migrated, imported, exported, backed up, restored, synchronized, reindexed, summarized, translated, validated, processed by an agent, processed by a workflow, archived, restricted, published, or accessed through a different implementation.

Authority Scope SHOULD support review.

A reviewer SHOULD be able to determine:

- what Authority Scope applies;
- whether the Authority Scope is appropriate;
- what Authority Level applies within the scope;
- whether the Authority Scope is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, or otherwise governed;
- whether the Authority Scope was assigned through a governed process where required;
- whether the Authority Scope was reviewed where required;
- whether the Authority Scope is supported by provenance;
- whether the Authority Scope is supported or limited by Source References;
- whether the Authority Scope is supported or limited by relationships;
- whether lifecycle state affects the Authority Scope;
- whether validation supports or challenges the Authority Scope;
- whether privacy classification constrains the Authority Scope;
- whether compatibility, import, export, migration, publication, workflow behavior, agent behavior, implementation behavior, or downstream use is affected.

Authority Scope SHOULD support validation.

A validator SHOULD be able to determine whether:

- Authority Scope is present where required;
- Authority Scope is explicit enough for the applicable use;
- Authority Scope uses a governed value where a governed vocabulary exists;
- Authority Scope remains distinguishable from Object Identity, Authority Level, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- Authority Scope is compatible with the assigned Authority Level;
- Authority Scope preserves required provenance where applicable;
- Authority Scope preserves privacy boundaries;
- Authority Scope preserves relationship meaning;
- Authority Scope preserves Source Reference and provenance context;
- Authority Scope remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority Scope SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate Authority Scope in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority Scope is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine where Authority Level applies, where it does not apply, what supports the scope, what limits the scope, whether the scope is current or historical, whether review or validation is required, whether privacy or lifecycle handling constrains the scope, and whether the scope remains meaningful across time and implementation replacement.

## 7. Authority Assignment

Authority Assignment is the governed act of assigning, proposing, confirming, revising, limiting, suspending, removing, preserving, transferring, downgrading, escalating, or otherwise changing Authority Level for a governed entity within a defined scope.

Authority Assignment exists so that Authority Level does not arise accidentally from storage behavior, implementation behavior, workflow completion, agent confidence, source existence, relationship existence, popularity, search ranking, graph centrality, folder placement, filename, tag, color, icon, user-interface state, plugin behavior, database state, or undocumented convention.

Authority Assignment MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a Source Reference;
- Source Material where applicable;
- a provenance record;
- a relationship;
- a metadata record;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Authority Assignment SHALL be governed where Authority Level affects:

- knowledge meaning;
- interpretation;
- governance;
- review;
- validation;
- publication;
- source reliance;
- relationship interpretation;
- workflow behavior;
- agent behavior;
- implementation behavior;
- import;
- export;
- migration;
- compatibility;
- privacy handling;
- downstream use.

Authority Assignment SHOULD identify or support identification of:

- what governed entity the assignment applies to;
- what Authority Level is assigned;
- what Authority Scope applies;
- who or what assigned the Authority Level where applicable;
- when the Authority Level was assigned where applicable;
- why the Authority Level was assigned where applicable;
- what review supports the assignment where applicable;
- what validation supports the assignment where applicable;
- what approval supports the assignment where applicable;
- what provenance supports the assignment where applicable;
- what Source References support or limit the assignment where applicable;
- what relationships support or limit the assignment where applicable;
- what lifecycle state affects the assignment where applicable;
- what privacy classification affects the assignment where applicable;
- what compatibility constraints affect the assignment where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Authority Assignment MUST be scoped.

An Authority Assignment without adequate scope is incomplete where authority affects governed interpretation or use.

Authority Assignment MUST NOT be treated as universal unless a governed authority process explicitly defines that assignment as universal within the applicable standard scope.

Authority Assignment MUST remain distinguishable from Object Identity.

Assigning, revising, limiting, suspending, removing, transferring, downgrading, or escalating Authority Level MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when its Authority Level is assigned or changed unless a separate governed identity decision determines that the object has become meaningfully different.

Authority Assignment MUST remain distinguishable from Lifecycle State.

A lifecycle state MAY affect whether Authority Level may be assigned, reviewed, limited, suspended, deprecated, superseded, archived, restricted, quarantined, repaired, published, exported, migrated, or used downstream.

Lifecycle State MUST NOT assign Authority Level by itself.

Approval MAY support Authority Assignment.

Approval MUST NOT automatically assign unlimited authority.

Rejection MAY limit or remove current use-authority.

Rejection MUST NOT erase historical authority context where that context remains relevant for governance, provenance, source traceability, compatibility, migration, audit, or review.

Deprecation MAY reduce future use-authority.

Deprecation MUST NOT erase historical interpretive authority where the deprecated entity remains relevant for historical interpretation, compatibility, migration, governance, or audit.

Supersession MAY replace current authority.

Supersession MUST NOT silently transfer all authority from the superseded entity to the superseding entity unless a governed process explicitly defines that transfer within a defined scope.

Archival MAY preserve authority for historical interpretation.

Archival MUST NOT assign active authority, public authority, export authority, publication authority, or broad downstream-use authority by itself.

Restriction MAY limit who or what may use authority.

Restriction MUST NOT erase the authority assignment record.

Quarantine MAY suspend authority use.

Quarantine MUST NOT silently delete authority history.

Authority Assignment MUST remain distinguishable from Validation State.

Validation MAY support Authority Assignment.

Validation MUST NOT assign Authority Level unless a governed authority process, workflow, or specification explicitly defines that result within a defined scope.

A validation result MAY trigger a proposed authority assignment, review requirement, limitation, suspension, downgrade, escalation, quarantine, repair, or rejection only where a governed process defines that behavior.

Authority Assignment MUST remain distinguishable from Privacy Classification.

Authority Assignment MUST NOT weaken privacy requirements.

A high-authority assignment MAY apply to a private, restricted, confidential, sensitive, non-exportable, agent-restricted, publication-restricted, or otherwise constrained entity.

Authority Assignment MUST NOT make restricted content public, exportable, publishable, searchable, synchronized, agent-readable, or implementation-visible unless privacy rules explicitly permit that behavior.

Where Authority Assignment creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority Assignment MUST remain distinguishable from Provenance.

Provenance MAY support Authority Assignment.

Provenance MAY explain why Authority Level was assigned.

Provenance SHOULD be preserved where Authority Assignment affects interpretation, governance, review, validation, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, import, export, migration, or downstream use.

Provenance MUST NOT assign Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Authority Assignment MUST remain distinguishable from Source References.

A Source Reference MAY support Authority Assignment.

A Source Reference MUST NOT assign Authority Level by itself.

Source existence, citation, availability, reliability, official status, popularity, frequency of citation, or source authority MUST NOT automatically assign Authority Level to a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity unless a governed authority process explicitly defines that result within a defined scope.

Authority Assignment MUST remain distinguishable from Relationship Authority.

A relationship MAY support Authority Assignment.

A relationship MAY limit Authority Assignment.

A relationship MAY preserve historical authority assignment.

A relationship MAY support authority inheritance, transfer, downgrade, or escalation only where a governed authority process explicitly defines that behavior within a defined scope.

Relationship existence MUST NOT assign Authority Level by itself.

Relationship strength MUST NOT assign Authority Level by itself.

Relationship confidence MUST NOT assign Authority Level by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT assign Authority Level by themselves.

Authority Assignment MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support review, validation, routing, triage, prioritization, or human decision-making.

Agent Confidence MUST NOT assign Authority Level by itself.

An agent MAY propose Authority Assignment.

An agent MUST NOT become an unreviewable authority for assigning, escalating, downgrading, removing, transferring, publishing, exporting, migrating, or applying Authority Level where authority affects governed interpretation or use.

Agent-proposed Authority Assignment SHOULD remain traceable to the agent, model class, instruction, workflow, source material, evidence, validation result, relationship context, confidence signal, review state, and human decision where applicable.

Agent-proposed Authority Assignment SHOULD remain clearly distinguishable from human-approved authority, workflow-approved authority, validation-supported authority, source-supported authority, and governed Authority Level.

Authority Assignment MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support Authority Assignment where a governed workflow explicitly defines that completion as part of an authority process.

Workflow Completion MUST NOT assign Authority Level by itself.

A workflow MAY propose, route, review, validate, assign, limit, suspend, escalate, downgrade, transfer, preserve, or remove Authority Level only where the applicable workflow is governed to perform that role.

Workflow-generated Authority Assignment SHOULD preserve enough provenance for future review where authority affects interpretation, governance, validation, privacy, publication, export, migration, relationships, Source References, lifecycle handling, compatibility, or downstream use.

Authority Assignment MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT assign Authority Level.

A governed entity MUST NOT become authoritative merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose Authority Level merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority Assignment SHOULD support review.

A reviewer SHOULD be able to determine:

- what Authority Level was assigned;
- what Authority Scope applies;
- whether the assignment is appropriate;
- whether the assignment was governed;
- whether the assignment is proposed, reviewed, approved, rejected, limited, suspended, inherited, transferred, downgraded, escalated, deprecated, superseded, archived, restricted, provisional, historical, or otherwise governed;
- who or what made the assignment where applicable;
- when the assignment occurred where applicable;
- why the assignment occurred where applicable;
- whether provenance supports the assignment;
- whether Source References support or limit the assignment;
- whether relationships support or limit the assignment;
- whether lifecycle state affects the assignment;
- whether validation supports or challenges the assignment;
- whether privacy classification constrains the assignment;
- whether compatibility, import, export, migration, publication, workflow behavior, agent behavior, implementation behavior, or downstream use is affected.

Authority Assignment SHOULD support validation.

A validator SHOULD be able to determine whether:

- Authority Assignment is present where required;
- Authority Assignment is scoped where required;
- Authority Assignment uses a governed value where a governed vocabulary exists;
- Authority Assignment remains distinguishable from Object Identity, Authority Level, Authority Scope, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- Authority Assignment preserves required provenance where applicable;
- Authority Assignment preserves privacy boundaries;
- Authority Assignment preserves relationship meaning;
- Authority Assignment preserves Source Reference and provenance context;
- Authority Assignment remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority Assignment SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate Authority Assignment in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority Assignment SHOULD support historical preservation.

A governed entity MAY retain historical Authority Assignment even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical Authority Assignment does not mean the entity remains current.

Historical Authority Assignment does not mean the entity is approved for future use.

Historical Authority Assignment does not mean the entity is public, exportable, publishable, valid, unrestricted, safe for agent use, or safe for downstream use.

Historical Authority Assignment SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, and provenance review.

Authority Assignment is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what Authority Level was assigned, what scope applies, who or what assigned it where applicable, what supports the assignment, what limits the assignment, whether the assignment is current or historical, whether review or validation is required, whether privacy or lifecycle handling constrains the assignment, and whether the assignment remains meaningful across time and implementation replacement.

## 8. Authority Review

Authority Review is the governed process used to determine whether an Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate, supported, scoped, traceable, current, compatible, privacy-respecting, and safe for downstream use.

Authority Review exists so that authority-related meaning remains reviewable by future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations.

Authority Review MAY apply to:

- a Knowledge Object;
- a Knowledge Record;
- a Source Reference;
- Source Material where applicable;
- a provenance record;
- a relationship;
- a metadata record;
- a validation result;
- a workflow output;
- an agent output;
- an import record;
- an export record;
- a migration record;
- a governed document;
- a decision;
- another governed entity.

Authority Review SHOULD occur where Authority Level affects:

- knowledge meaning;
- interpretation;
- governance;
- review;
- validation;
- publication;
- source reliance;
- relationship interpretation;
- workflow behavior;
- agent behavior;
- implementation behavior;
- import;
- export;
- migration;
- compatibility;
- privacy handling;
- downstream use.

Authority Review SHOULD determine or support determination of:

- what governed entity is being reviewed;
- what Authority Level applies;
- what Authority Scope applies;
- what Authority Assignment occurred where applicable;
- what authority category applies where applicable;
- whether the authority is proposed, reviewed, approved, rejected, limited, suspended, inherited, transferred, downgraded, escalated, deprecated, superseded, archived, restricted, provisional, historical, or otherwise governed;
- who or what assigned the Authority Level where applicable;
- who or what reviewed the Authority Level where applicable;
- when the review occurred where applicable;
- why the review occurred where applicable;
- what review decision was made where applicable;
- what provenance supports the review where applicable;
- what Source References support or limit the review where applicable;
- what relationships support or limit the review where applicable;
- what validation results support or challenge the review where applicable;
- what lifecycle state affects the review where applicable;
- what privacy classification affects the review where applicable;
- what compatibility constraints affect the review where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Authority Review MUST be scoped.

A review decision in one scope MUST NOT automatically create authority in another scope.

A review decision for one use MUST NOT automatically authorize all other uses.

A review decision for internal interpretation MUST NOT automatically authorize publication, export, migration, agent use, workflow use, implementation exposure, or downstream use.

A review decision for historical interpretation MUST NOT automatically authorize current operational use.

A review decision for source reliance MUST NOT automatically authorize relationship creation, publication, governance, validation, export, migration, or downstream automation.

Authority Review MUST remain distinguishable from Authority Level.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity.

Authority Review describes the process used to evaluate whether that Authority Level is appropriate within a defined scope.

Review may support Authority Level.

Review does not automatically create unlimited authority.

Authority Review MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

Authority Review evaluates whether Authority Assignment is appropriate, supported, scoped, traceable, current, compatible, privacy-respecting, and safe for downstream use.

A review MAY confirm an Authority Assignment.

A review MAY reject an Authority Assignment.

A review MAY limit an Authority Assignment.

A review MAY suspend an Authority Assignment.

A review MAY require further review, validation, source verification, privacy review, relationship review, provenance review, lifecycle review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Authority Review MUST remain distinguishable from Object Identity.

Reviewing, approving, rejecting, limiting, suspending, downgrading, escalating, transferring, or preserving Authority Level MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when its Authority Level is reviewed unless a separate governed identity decision determines that the object has become meaningfully different.

Authority Review MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether authority requires review, may be used, must be limited, must be suspended, may be deprecated, may be superseded, may be archived, must be restricted, must be quarantined, may be repaired, may be published, may be exported, may be migrated, or may be applied downstream.

Lifecycle State MUST NOT replace Authority Review.

Approval MAY result from review.

Approval MUST NOT imply unlimited authority.

Rejection MAY result from review.

Rejection MUST NOT erase historical authority context where that context remains relevant for governance, provenance, source traceability, compatibility, migration, audit, or review.

Deprecation MAY result from review.

Deprecation MUST NOT erase historical interpretive authority where the deprecated entity remains relevant for historical interpretation, compatibility, migration, governance, or audit.

Supersession MAY result from review.

Supersession MUST NOT silently transfer all authority from the superseded entity to the superseding entity unless a governed process explicitly defines that transfer within a defined scope.

Restriction MAY result from review.

Restriction MUST NOT erase the authority record.

Quarantine MAY result from review.

Quarantine MUST NOT silently delete authority history.

Authority Review MUST remain distinguishable from Validation State.

Validation MAY support Authority Review.

Validation MUST NOT replace Authority Review unless a governed authority process, workflow, or specification explicitly defines that result within a defined scope.

A validation-passing entity may still require Authority Review.

A validation-failing entity may still preserve historical authority context.

A validation result MAY trigger Authority Review where validation affects interpretation, governance, publication, privacy, relationships, Source References, provenance, lifecycle handling, compatibility, import, export, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

Authority Review MUST remain distinguishable from Privacy Classification.

Authority Review MUST preserve privacy boundaries.

Authority Review MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, or otherwise protected information merely to make review easier.

Authority Review SHOULD remain possible for authorized reviewers without causing restricted information to be treated as missing by unauthorized actors.

Where Authority Review creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority Review MUST remain distinguishable from Provenance.

Provenance MAY support Authority Review.

Provenance MAY explain why an Authority Level was assigned, reviewed, limited, suspended, downgraded, escalated, transferred, preserved, removed, approved, rejected, deprecated, superseded, archived, restricted, quarantined, or treated as historical.

Authority Review SHOULD preserve provenance where review affects interpretation, governance, validation, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, import, export, migration, or downstream use.

Provenance MUST NOT replace Authority Review unless a governed authority process explicitly defines that behavior within a defined scope.

Authority Review MUST remain distinguishable from Source References.

A Source Reference MAY support Authority Review.

A Source Reference MAY limit Authority Review.

A Source Reference MAY require Authority Review where source reliability, source authority, source availability, source privacy, extraction history, transformation history, contradiction, incompleteness, uncertainty, or provenance affects authority.

A Source Reference MUST NOT complete Authority Review by itself.

Source existence, citation, availability, reliability, official status, popularity, frequency of citation, or source authority MUST NOT automatically satisfy Authority Review unless a governed authority process explicitly defines that result within a defined scope.

Authority Review MUST remain distinguishable from Relationship Authority.

A relationship MAY support Authority Review.

A relationship MAY limit Authority Review.

A relationship MAY require Authority Review where relationship type, direction, participants, provenance, lifecycle state, validation state, privacy classification, compatibility, source traceability, or authority affects interpretation or use.

Relationship existence MUST NOT satisfy Authority Review by itself.

Relationship strength MUST NOT satisfy Authority Review by itself.

Relationship confidence MUST NOT satisfy Authority Review by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT satisfy Authority Review by themselves.

Authority Review MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support triage, routing, review prioritization, validation, source checking, relationship checking, conflict detection, or human decision-making.

Agent Confidence MUST NOT satisfy Authority Review by itself.

An agent MAY propose Authority Review outcomes.

An agent MAY flag an entity for Authority Review.

An agent MAY recommend downgrade, escalation, limitation, suspension, rejection, approval, source review, privacy review, validation review, relationship review, provenance review, lifecycle review, publication review, export review, migration review, or downstream-use review.

An agent MUST NOT become an unreviewable reviewer for Authority Review where authority affects governed interpretation or use.

Agent-supported Authority Review SHOULD remain traceable to the agent, model class, instruction, workflow, source material, evidence, validation result, relationship context, confidence signal, review state, and human decision where applicable.

Authority Review MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support Authority Review where a governed workflow explicitly defines completion as part of an authority review process.

Workflow Completion MUST NOT satisfy Authority Review by itself.

A workflow MAY route, perform, record, validate, approve, reject, limit, suspend, escalate, downgrade, transfer, preserve, or remove Authority Level only where the applicable workflow is governed to perform that role.

Workflow-supported Authority Review SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, validation, privacy, publication, export, migration, relationships, Source References, lifecycle handling, compatibility, or downstream use.

Authority Review MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT satisfy Authority Review.

A governed entity MUST NOT be treated as reviewed merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose review history merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority Review SHOULD support review history.

Authority Review history SHOULD identify or support identification of:

- prior Authority Level;
- new Authority Level where applicable;
- prior Authority Scope;
- new Authority Scope where applicable;
- review decision;
- reviewer where applicable;
- review date where applicable;
- review reason where applicable;
- reviewed evidence where applicable;
- reviewed Source References where applicable;
- reviewed provenance where applicable;
- reviewed relationships where applicable;
- reviewed validation results where applicable;
- reviewed lifecycle state where applicable;
- reviewed privacy classification where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Authority Review SHOULD support validation.

A validator SHOULD be able to determine whether:

- Authority Review is present where required;
- Authority Review is scoped where required;
- Authority Review uses a governed value where a governed vocabulary exists;
- Authority Review remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- Authority Review preserves required provenance where applicable;
- Authority Review preserves privacy boundaries;
- Authority Review preserves relationship meaning;
- Authority Review preserves Source Reference and provenance context;
- Authority Review remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority Review SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate Authority Review in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority Review SHOULD support historical preservation.

A governed entity MAY retain historical Authority Review even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical Authority Review does not mean the entity remains current.

Historical Authority Review does not mean the entity is approved for future use.

Historical Authority Review does not mean the entity is public, exportable, publishable, valid, unrestricted, safe for agent use, or safe for downstream use.

Historical Authority Review SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, and provenance review.

Authority Review is successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what authority was reviewed, what scope applied, who or what reviewed it where applicable, what evidence supported the review, what limits were applied, whether the review is current or historical, whether further review or validation is required, whether privacy or lifecycle handling constrains the review, and whether the review remains meaningful across time and implementation replacement.

## 9. Authority and Approval

Authority and Approval are related but distinct concepts.

Approval is the formal acceptance of a governed entity for use within a defined scope.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Approval MAY support Authority Level.

Approval MUST NOT automatically create unlimited authority.

Authority Level MUST NOT imply approval where approval has not occurred.

A governed entity may be:

- approved but low-authority;
- approved for one scope but non-authoritative in another scope;
- approved for internal use but not publication;
- approved for review use but not downstream automation;
- approved for historical interpretation but not current operational use;
- approved for migration analysis but not export;
- authoritative but not yet approved for a specific workflow;
- high-authority but private, restricted, confidential, sensitive, non-exportable, agent-restricted, or publication-restricted;
- source-supported but not approved;
- reviewed but not approved;
- validated but not approved;
- agent-generated but not approved;
- workflow-generated but not approved until governed.

Approval SHALL be scoped where approval affects Authority Level.

Approval scope SHOULD identify or support identification of:

- what governed entity was approved;
- what approval applies;
- what Authority Level is supported by the approval where applicable;
- what Authority Scope applies;
- who or what approved the entity where applicable;
- when approval occurred where applicable;
- why approval occurred where applicable;
- what review supports approval where applicable;
- what validation supports approval where applicable;
- what provenance supports approval where applicable;
- what Source References support or limit approval where applicable;
- what relationships support or limit approval where applicable;
- what lifecycle state affects approval where applicable;
- what privacy classification affects approval where applicable;
- what compatibility constraints affect approval where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Approval MUST remain distinguishable from Authority Level.

An approved entity is not automatically authoritative for every purpose.

An authoritative entity is not automatically approved for every use.

Approval in one context MUST NOT imply authority in every context.

Authority in one context MUST NOT imply approval in every context.

Approval MUST remain distinguishable from Authority Scope.

Approval scope describes where approval applies.

Authority Scope describes where Authority Level applies.

Approval scope MAY support Authority Scope.

Approval scope MUST NOT silently broaden Authority Scope.

Approval MUST remain distinguishable from Authority Assignment.

Approval MAY support an Authority Assignment.

Approval MAY confirm an Authority Assignment.

Approval MAY limit an Authority Assignment.

Approval MAY reject a proposed Authority Assignment.

Approval MUST NOT silently assign, transfer, inherit, downgrade, escalate, suspend, remove, or broaden Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Approval MUST remain distinguishable from Authority Review.

Authority Review may result in approval.

Authority Review may result in rejection, limitation, suspension, downgrade, escalation, further review, validation, source verification, privacy review, relationship review, provenance review, lifecycle review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

A reviewed entity is not automatically approved.

An approved entity may still require later Authority Review if new evidence, lifecycle changes, validation results, privacy constraints, source changes, relationship changes, migration changes, implementation changes, or governance changes affect authority.

Approval MUST remain distinguishable from Object Identity.

Approving, rejecting, limiting, suspending, downgrading, escalating, transferring, or preserving Authority Level MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when approval changes unless a separate governed identity decision determines that the object has become meaningfully different.

Approval MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether approval is current, proposed, limited, suspended, deprecated, superseded, archived, restricted, quarantined, repaired, published, exported, migrated, or applicable downstream.

Lifecycle State MUST NOT replace approval.

Approval MUST NOT replace Lifecycle State.

An approved entity may still be deprecated.

An approved entity may still be superseded.

An approved entity may still be archived.

An approved entity may still be restricted.

An approved entity may still require quarantine, repair, revalidation, or re-review.

Approval MUST remain distinguishable from Validation State.

Validation MAY support approval.

Validation MUST NOT equal approval unless a governed process, workflow, or specification explicitly defines that result within a defined scope.

A validation-passing entity may remain unapproved.

A validation-failing entity may preserve historical approval context.

A validation result MAY trigger approval review, rejection, limitation, suspension, downgrade, escalation, repair, quarantine, or further review only where a governed process defines that behavior.

Approval MUST remain distinguishable from Privacy Classification.

Approval MUST NOT weaken privacy requirements.

Approval MUST NOT make restricted content public, exportable, publishable, searchable, synchronized, agent-readable, or implementation-visible unless privacy rules explicitly permit that behavior.

A high-authority approved entity may remain private, restricted, confidential, sensitive, non-exportable, agent-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, or otherwise constrained.

Where approval creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Approval MUST remain distinguishable from Provenance.

Provenance MAY support approval.

Provenance MAY explain why approval occurred.

Provenance SHOULD be preserved where approval affects interpretation, governance, review, validation, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, import, export, migration, or downstream use.

Provenance MUST NOT create approval by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Approval MUST remain distinguishable from Source References.

A Source Reference MAY support approval.

A Source Reference MAY limit approval.

A Source Reference MAY require approval review where source reliability, source authority, source availability, source privacy, extraction history, transformation history, contradiction, incompleteness, uncertainty, or provenance affects authority.

A Source Reference MUST NOT create approval by itself.

Source existence, citation, availability, reliability, official status, popularity, frequency of citation, or source authority MUST NOT automatically approve a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity unless a governed approval process explicitly defines that result within a defined scope.

Approval MUST remain distinguishable from Relationship Authority.

A relationship MAY support approval.

A relationship MAY limit approval.

A relationship MAY require approval review.

A relationship MAY preserve historical approval context.

Relationship existence MUST NOT create approval by itself.

Relationship strength MUST NOT create approval by itself.

Relationship confidence MUST NOT create approval by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create approval by themselves.

Approval MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support triage, routing, review prioritization, validation, source checking, relationship checking, conflict detection, or human decision-making.

Agent Confidence MUST NOT create approval by itself.

An agent MAY propose approval.

An agent MAY recommend rejection, limitation, suspension, downgrade, escalation, source review, privacy review, validation review, relationship review, provenance review, lifecycle review, publication review, export review, migration review, or downstream-use review.

An agent MUST NOT become an unreviewable approver where approval affects governed interpretation or use.

Agent-supported approval recommendations SHOULD remain traceable to the agent, model class, instruction, workflow, source material, evidence, validation result, relationship context, confidence signal, review state, and human decision where applicable.

Approval MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support approval where a governed workflow explicitly defines completion as part of an approval process.

Workflow Completion MUST NOT create approval by itself.

A workflow MAY route, perform, record, validate, approve, reject, limit, suspend, escalate, downgrade, transfer, preserve, or remove approval only where the applicable workflow is governed to perform that role.

Workflow-supported approval SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, validation, privacy, publication, export, migration, relationships, Source References, lifecycle handling, compatibility, or downstream use.

Approval MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT create approval.

A governed entity MUST NOT be treated as approved merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose approval history merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Approval SHOULD support review history.

Approval history SHOULD identify or support identification of:

- prior approval state where applicable;
- new approval state where applicable;
- prior Authority Level where applicable;
- new Authority Level where applicable;
- prior Authority Scope where applicable;
- new Authority Scope where applicable;
- approval decision;
- approver where applicable;
- approval date where applicable;
- approval reason where applicable;
- reviewed evidence where applicable;
- reviewed Source References where applicable;
- reviewed provenance where applicable;
- reviewed relationships where applicable;
- reviewed validation results where applicable;
- reviewed lifecycle state where applicable;
- reviewed privacy classification where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Approval SHOULD support validation.

A validator SHOULD be able to determine whether:

- approval is present where required;
- approval is scoped where required;
- approval uses a governed value where a governed vocabulary exists;
- approval remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- approval preserves required provenance where applicable;
- approval preserves privacy boundaries;
- approval preserves relationship meaning;
- approval preserves Source Reference and provenance context;
- approval remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Approval SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate approval in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Approval SHOULD support historical preservation.

A governed entity MAY retain historical approval context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical approval does not mean the entity remains current.

Historical approval does not mean the entity is approved for future use.

Historical approval does not mean the entity is public, exportable, publishable, valid, unrestricted, safe for agent use, or safe for downstream use.

Historical approval SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, and provenance review.

Authority and Approval are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what approval occurred, what Authority Level it supports where applicable, what scope applies, who or what approved it where applicable, what evidence supported approval, what limits were applied, whether approval is current or historical, whether further review or validation is required, whether privacy or lifecycle handling constrains approval, and whether approval remains meaningful across time and implementation replacement.

## 10. Authority and Validation

Authority and Validation are related but distinct concepts.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Validation MAY support Authority Level.

Validation MUST NOT automatically create Authority Level.

Validation MUST NOT automatically create approval.

Validation success MUST NOT imply authority unless a governed authority process, workflow, or specification explicitly defines that result within a defined scope.

Authority Level MUST NOT imply validation success where validation has not occurred.

A governed entity may be:

- valid but low-authority;
- valid but unapproved;
- valid but provisional;
- valid but restricted;
- valid but non-authoritative outside its scope;
- invalid but historically authoritative;
- invalid but preserved for audit, review, contradiction, provenance, migration, or compatibility analysis;
- high-authority but requiring revalidation;
- source-supported but not validated;
- agent-generated and validation-passing but not authoritative until reviewed;
- workflow-generated and validation-passing but not authoritative until governed.

Validation SHALL be scoped where validation affects Authority Level.

Validation scope SHOULD identify or support identification of:

- what governed entity was validated;
- what validation profile, rule set, workflow, validator, or process applied where applicable;
- what Authority Level is supported, limited, challenged, or unaffected by validation where applicable;
- what Authority Scope applies;
- who or what performed validation where applicable;
- when validation occurred where applicable;
- why validation occurred where applicable;
- what validation result occurred where applicable;
- what review supports validation where applicable;
- what approval supports validation where applicable;
- what provenance supports validation where applicable;
- what Source References support or limit validation where applicable;
- what relationships support or limit validation where applicable;
- what lifecycle state affects validation where applicable;
- what privacy classification affects validation where applicable;
- what compatibility constraints affect validation where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Validation MUST remain distinguishable from Authority Level.

A validation-passing entity is not automatically authoritative.

An authoritative entity is not automatically validation-passing.

Validation in one context MUST NOT imply authority in every context.

Authority in one context MUST NOT imply validation in every context.

Validation MUST remain distinguishable from Authority Scope.

Validation Scope describes where validation applies.

Authority Scope describes where Authority Level applies.

Validation Scope MAY support Authority Scope.

Validation Scope MUST NOT silently broaden Authority Scope.

Validation MUST remain distinguishable from Authority Assignment.

Validation MAY support Authority Assignment.

Validation MAY challenge Authority Assignment.

Validation MAY trigger a proposed Authority Assignment.

Validation MAY trigger limitation, suspension, downgrade, escalation, quarantine, repair, review, approval review, source review, privacy review, relationship review, provenance review, lifecycle review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Validation MUST NOT silently assign, transfer, inherit, downgrade, escalate, suspend, remove, or broaden Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Validation MUST remain distinguishable from Authority Review.

Validation MAY support Authority Review.

Validation MAY trigger Authority Review.

Validation MAY provide evidence for Authority Review.

Validation MUST NOT replace Authority Review unless a governed authority process, workflow, or specification explicitly defines that result within a defined scope.

A validation-passing entity may still require Authority Review.

A validation-failing entity may still preserve historical authority context.

Validation MUST remain distinguishable from Approval.

Validation MAY support approval.

Validation MAY challenge approval.

Validation MAY trigger approval review.

Validation MUST NOT equal approval unless a governed process, workflow, or specification explicitly defines that result within a defined scope.

A validation-passing entity may remain unapproved.

A validation-failing entity may preserve historical approval context.

Validation MUST remain distinguishable from Object Identity.

Validating, failing validation, repairing validation, revalidating, approving validation, rejecting validation, limiting validation, suspending validation, downgrading validation, escalating validation, or preserving validation history MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when validation state changes unless a separate governed identity decision determines that the object has become meaningfully different.

Validation MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether validation is required, current, stale, failed, pending, limited, suspended, deprecated, superseded, archived, restricted, quarantined, repaired, published, exported, migrated, or applicable downstream.

Lifecycle State MUST NOT replace validation.

Validation MUST NOT replace Lifecycle State.

A draft entity may be validation-passing but not approved.

An approved entity may require revalidation.

A deprecated entity may retain historical validation context.

A superseded entity may retain validation history for audit or compatibility.

An archived entity may retain validation results for historical interpretation.

A quarantined entity may require validation repair before authority is restored.

Validation MUST remain distinguishable from Privacy Classification.

Validation MUST preserve privacy boundaries.

Validation MUST NOT make restricted content public, exportable, publishable, searchable, synchronized, agent-readable, or implementation-visible unless privacy rules explicitly permit that behavior.

A validation process MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, or otherwise protected information merely to complete validation.

Where validation creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Validation MUST remain distinguishable from Provenance.

Provenance MAY support validation.

Provenance MAY explain why validation occurred.

Provenance MAY explain why validation passed, failed, was skipped, was limited, was suspended, was repaired, was superseded, or requires review.

Provenance SHOULD be preserved where validation affects interpretation, governance, review, approval, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, import, export, migration, or downstream use.

Provenance MUST NOT create validation success by itself unless a governed validation process explicitly defines that behavior within a defined scope.

Validation MUST remain distinguishable from Source References.

A Source Reference MAY support validation.

A Source Reference MAY limit validation.

A Source Reference MAY require validation review where source reliability, source authority, source availability, source privacy, extraction history, transformation history, contradiction, incompleteness, uncertainty, or provenance affects authority.

A Source Reference MUST NOT create validation success by itself.

Source existence, citation, availability, reliability, official status, popularity, frequency of citation, or source authority MUST NOT automatically validate a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity unless a governed validation process explicitly defines that result within a defined scope.

Validation MUST remain distinguishable from Relationship Authority.

A relationship MAY support validation.

A relationship MAY limit validation.

A relationship MAY require validation review.

A relationship MAY preserve historical validation context.

Relationship existence MUST NOT create validation success by itself.

Relationship strength MUST NOT create validation success by itself.

Relationship confidence MUST NOT create validation success by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create validation success by themselves.

Validation MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support triage, routing, validation prioritization, source checking, relationship checking, conflict detection, repair recommendations, or human decision-making.

Agent Confidence MUST NOT create validation success by itself.

An agent MAY propose validation results.

An agent MAY recommend validation review, repair, downgrade, escalation, limitation, suspension, rejection, approval review, source review, privacy review, relationship review, provenance review, lifecycle review, publication review, export review, migration review, or downstream-use review.

An agent MUST NOT become an unreviewable validator where validation affects governed interpretation or use.

Agent-supported validation recommendations SHOULD remain traceable to the agent, model class, instruction, workflow, source material, evidence, validation result, relationship context, confidence signal, review state, and human decision where applicable.

Validation MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support validation where a governed workflow explicitly defines completion as part of a validation process.

Workflow Completion MUST NOT create validation success by itself.

A workflow MAY route, perform, record, validate, fail, repair, approve, reject, limit, suspend, escalate, downgrade, transfer, preserve, or remove validation only where the applicable workflow is governed to perform that role.

Workflow-supported validation SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, authority, privacy, publication, export, migration, relationships, Source References, lifecycle handling, compatibility, or downstream use.

Validation MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT create validation success.

A governed entity MUST NOT be treated as valid merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose validation history merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Validation SHOULD support validation history.

Validation history SHOULD identify or support identification of:

- prior validation state where applicable;
- new validation state where applicable;
- prior Authority Level where applicable;
- new Authority Level where applicable;
- prior Authority Scope where applicable;
- new Authority Scope where applicable;
- validation result;
- validator where applicable;
- validation date where applicable;
- validation reason where applicable;
- validation profile, rule set, workflow, or process where applicable;
- validation errors where applicable;
- validation warnings where applicable;
- reviewed evidence where applicable;
- reviewed Source References where applicable;
- reviewed provenance where applicable;
- reviewed relationships where applicable;
- reviewed lifecycle state where applicable;
- reviewed privacy classification where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Validation SHOULD support review.

A reviewer SHOULD be able to determine:

- what validation occurred;
- what validation scope applied;
- whether validation supports, limits, challenges, or does not affect Authority Level;
- whether validation supports, limits, challenges, or does not affect approval;
- whether validation is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, failed, or otherwise governed;
- whether validation requires further Authority Review;
- whether validation requires further approval review;
- whether validation requires source review, privacy review, relationship review, provenance review, lifecycle review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Validation SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate validation in a way that causes loss of meaning, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Validation SHOULD support historical preservation.

A governed entity MAY retain historical validation context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical validation does not mean the entity remains current.

Historical validation does not mean the entity is approved for future use.

Historical validation does not mean the entity is authoritative for future use.

Historical validation does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, or safe for downstream use.

Historical validation SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, and provenance review.

Authority and Validation are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what validation occurred, what Authority Level it supports or challenges where applicable, what scope applies, who or what validated it where applicable, what validation process applied, what evidence supported validation, what limits were applied, whether validation is current or historical, whether further review or approval is required, whether privacy or lifecycle handling constrains validation, and whether validation remains meaningful across time and implementation replacement.

## 11. Authority and Provenance

Authority and Provenance are related but distinct concepts.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Provenance MAY support Authority Level.

Provenance MAY explain why Authority Level was assigned, reviewed, approved, rejected, limited, suspended, downgraded, escalated, transferred, inherited, preserved, deprecated, superseded, archived, restricted, quarantined, or treated as historical.

Provenance MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

A governed entity may be:

- high-authority with strong provenance;
- high-authority with restricted provenance;
- low-authority with complete provenance;
- low-authority with incomplete provenance;
- provisional authority pending provenance review;
- historically authoritative because provenance preserves prior authority context;
- source-supported but not authoritative;
- reviewed but requiring additional provenance;
- approved but requiring provenance preservation;
- validated but not authoritative;
- agent-generated with provenance but not authoritative until reviewed;
- workflow-generated with provenance but not authoritative until governed.

Authority-related provenance SHOULD identify or support identification of:

- what governed entity the provenance applies to;
- what Authority Level applies where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment occurred where applicable;
- what Authority Review occurred where applicable;
- what approval occurred where applicable;
- what validation occurred where applicable;
- who or what created, assigned, reviewed, approved, validated, modified, migrated, imported, exported, or preserved the authority-related information where applicable;
- when authority-related activity occurred where applicable;
- why authority-related activity occurred where applicable;
- what Source References support or limit authority where applicable;
- what relationships support or limit authority where applicable;
- what lifecycle state affects authority where applicable;
- what privacy classification affects authority where applicable;
- what compatibility constraints affect authority where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Authority and Provenance MUST remain distinguishable.

Provenance may support authority.

Provenance may explain authority.

Provenance may limit authority.

Provenance may challenge authority.

Provenance may preserve authority history.

Provenance does not equal Authority Level.

Authority Level does not equal provenance.

A provenance-rich entity is not automatically authoritative.

An authoritative entity is not automatically provenance-complete.

Authority in one scope MUST NOT imply complete provenance in every scope.

Provenance in one scope MUST NOT imply authority in every scope.

Authority-related provenance MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Provenance describes the origin, evidence, reasoning, transformation, review, validation, workflow, agent, import, export, migration, or change context associated with the authority.

Provenance MAY support Authority Scope.

Provenance MAY limit Authority Scope.

Provenance MAY show that authority applies only within a narrow scope.

Provenance MUST NOT silently broaden Authority Scope.

Authority-related provenance MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

Provenance explains or preserves the context of that assignment.

Provenance MAY support Authority Assignment.

Provenance MAY challenge Authority Assignment.

Provenance MAY show that an Authority Assignment is incomplete, unsupported, outdated, contradicted, privacy-constrained, source-limited, relationship-limited, migration-limited, export-limited, publication-limited, or otherwise restricted.

Provenance MUST NOT assign Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related provenance MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

Provenance may provide evidence for Authority Review.

Provenance may explain Authority Review.

Provenance may show why Authority Review is required.

Provenance may show why Authority Review is incomplete.

Provenance MUST NOT replace Authority Review unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related provenance MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

Provenance may support approval.

Provenance may explain approval.

Provenance may preserve approval history.

Provenance may challenge approval where approval context is missing, incomplete, contradictory, outdated, restricted, or incompatible.

Provenance MUST NOT create approval by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Authority-related provenance MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

Provenance may support validation.

Provenance may explain validation.

Provenance may preserve validation history.

Provenance may show why validation is required.

Provenance MUST NOT create validation success by itself unless a governed validation process explicitly defines that behavior within a defined scope.

Authority-related provenance MUST remain distinguishable from Object Identity.

Creating, changing, reviewing, validating, approving, importing, exporting, migrating, repairing, preserving, or restricting provenance MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when authority-related provenance changes unless a separate governed identity decision determines that the object has become meaningfully different.

Authority-related provenance MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether provenance must be created, preserved, reviewed, limited, restricted, quarantined, archived, migrated, exported, or used downstream.

Lifecycle State MUST NOT replace provenance.

Provenance MUST NOT replace Lifecycle State.

A draft entity may have strong provenance.

An approved entity may have incomplete provenance.

A deprecated entity may require provenance preservation.

A superseded entity may retain provenance for historical authority interpretation.

An archived entity may retain provenance for audit, compatibility, or migration.

A quarantined entity may require provenance review before authority is restored.

Authority-related provenance MUST remain distinguishable from Privacy Classification.

Provenance MUST preserve privacy boundaries.

Provenance MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, publication-restricted, source-restricted, relationship-restricted, or otherwise protected information merely to support authority.

A high-authority entity may have restricted provenance.

A low-authority entity may have sensitive provenance.

A provenance record may be authoritative for audit while remaining restricted from publication, export, synchronization, indexing, agent use, or broad implementation visibility.

Where provenance handling creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority-related provenance MUST remain distinguishable from Source References.

A Source Reference may support provenance.

A Source Reference may be part of provenance.

A Source Reference may explain, contextualize, contradict, originate, or otherwise relate to authority.

A Source Reference MUST NOT replace provenance unless a governed process explicitly defines that behavior within a defined scope.

A Source Reference MUST NOT automatically create Authority Level merely because it exists, is cited, is available, is reliable, official, popular, frequently referenced, or appears authoritative.

Authority-related provenance SHOULD preserve the distinction between Source Material and Knowledge Records.

Source Material may provide evidence.

A Knowledge Record may interpret evidence.

Provenance should show what source material was used, what transformation occurred, who or what performed the transformation, whether review occurred, whether validation occurred, whether approval occurred, and whether authority was assigned within a defined scope where that context affects interpretation or use.

Authority-related provenance MUST remain distinguishable from Relationship Authority.

A relationship MAY support provenance.

A relationship MAY express provenance context.

A relationship MAY connect authority, source support, evidence, attribution, derivation, validation, review, approval, import, export, migration, or governance relevance.

A relationship MAY limit or challenge authority-related provenance.

Relationship existence MUST NOT create provenance completeness by itself.

Relationship strength MUST NOT create provenance completeness by itself.

Relationship confidence MUST NOT create provenance completeness by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create provenance completeness by themselves.

Authority-related provenance MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support provenance review, source checking, relationship checking, extraction review, transformation review, contradiction detection, authority review, validation review, or human decision-making.

Agent Confidence MUST NOT create provenance completeness by itself.

An agent MAY generate provenance.

An agent MAY propose provenance.

An agent MAY summarize provenance.

An agent MAY classify provenance.

An agent MAY flag missing, incomplete, contradictory, stale, restricted, or incompatible provenance.

An agent MUST NOT become an unreviewable authority for provenance where provenance affects governed interpretation or use.

Agent-generated provenance SHOULD remain traceable to the agent, model class, instruction, workflow, source material, evidence, extraction context, transformation context, confidence signal, review state, and human decision where applicable.

Authority-related provenance MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support provenance where a governed workflow explicitly defines completion as part of a provenance process.

Workflow Completion MUST NOT create provenance completeness by itself.

A workflow MAY create, route, review, validate, approve, reject, limit, restrict, repair, preserve, import, export, migrate, or archive provenance only where the applicable workflow is governed to perform that role.

Workflow-generated provenance SHOULD preserve enough context for future review where workflow activity affects interpretation, governance, authority, privacy, publication, export, migration, relationships, Source References, lifecycle handling, compatibility, or downstream use.

Authority-related provenance MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT create provenance completeness.

A governed entity MUST NOT be treated as provenance-complete merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose provenance merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority-related provenance SHOULD support provenance history.

Provenance history SHOULD identify or support identification of:

- prior Authority Level where applicable;
- new Authority Level where applicable;
- prior Authority Scope where applicable;
- new Authority Scope where applicable;
- authority assignment history where applicable;
- authority review history where applicable;
- approval history where applicable;
- validation history where applicable;
- source-reference history where applicable;
- relationship history where applicable;
- lifecycle history where applicable;
- privacy classification history where applicable;
- provenance creator where applicable;
- provenance editor where applicable;
- provenance date where applicable;
- provenance reason where applicable;
- reviewed evidence where applicable;
- reviewed Source References where applicable;
- reviewed relationships where applicable;
- reviewed lifecycle state where applicable;
- reviewed privacy classification where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Authority-related provenance SHOULD support review.

A reviewer SHOULD be able to determine:

- what provenance exists;
- what provenance is missing where applicable;
- what Authority Level the provenance supports, limits, challenges, or does not affect;
- what Authority Scope the provenance supports, limits, challenges, or does not affect;
- whether provenance supports, limits, challenges, or does not affect approval;
- whether provenance supports, limits, challenges, or does not affect validation;
- whether provenance is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, incomplete, contradicted, or otherwise governed;
- whether provenance requires further Authority Review;
- whether provenance requires source review, privacy review, relationship review, lifecycle review, validation review, approval review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Authority-related provenance SHOULD support validation.

A validator SHOULD be able to determine whether:

- provenance is present where required;
- provenance is scoped where required;
- provenance uses a governed value where a governed vocabulary exists;
- provenance remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Privacy Classification, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- provenance preserves privacy boundaries;
- provenance preserves relationship meaning;
- provenance preserves Source Reference context;
- provenance remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority-related provenance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate provenance in a way that causes loss of meaning, broken source traceability, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority-related provenance SHOULD support historical preservation.

A governed entity MAY retain historical provenance context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical provenance does not mean the entity remains current.

Historical provenance does not mean the entity is approved for future use.

Historical provenance does not mean the entity is authoritative for future use.

Historical provenance does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, or safe for downstream use.

Historical provenance SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, and evidence review.

Authority and Provenance are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what provenance exists, what Authority Level it supports or challenges where applicable, what scope applies, who or what created or modified the provenance where applicable, what source material or evidence supports the provenance, what transformations occurred, what review or validation occurred, what limits were applied, whether provenance is current or historical, whether further review or validation is required, whether privacy or lifecycle handling constrains provenance, and whether provenance remains meaningful across time and implementation replacement.

## 12. Authority and Source References

Authority and Source References are related but distinct concepts.

A Source Reference is a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

A Source Reference MAY support Authority Level.

A Source Reference MAY explain Authority Level.

A Source Reference MAY limit Authority Level.

A Source Reference MAY challenge Authority Level.

A Source Reference MAY preserve historical authority context.

A Source Reference MUST NOT automatically create Authority Level merely because a source exists, is cited, is available, is reliable, official, popular, frequently referenced, or appears authoritative.

A governed entity may be:

- source-referenced but low-authority;
- source-referenced but unreviewed;
- source-referenced but unapproved;
- source-referenced but unvalidated;
- source-referenced but provisional;
- source-referenced but restricted;
- source-referenced but contradicted;
- source-referenced but historically authoritative;
- source-referenced but non-authoritative outside its scope;
- source-supported and high-authority within a defined scope;
- based on a high-authority source but not itself authoritative;
- based on a restricted source and therefore authority-limited;
- based on a superseded source and therefore historically limited;
- agent-generated from Source Material but not authoritative until reviewed;
- workflow-generated from Source Material but not authoritative until governed.

Authority-related Source References SHOULD identify or support identification of:

- what governed entity the Source Reference applies to;
- what Source Material is referenced;
- what Authority Level the Source Reference supports, limits, challenges, or does not affect where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment occurred where applicable;
- what Authority Review occurred where applicable;
- what approval occurred where applicable;
- what validation occurred where applicable;
- what provenance supports the Source Reference where applicable;
- what relationship context affects the Source Reference where applicable;
- what lifecycle state affects the Source Reference where applicable;
- what privacy classification affects the Source Reference where applicable;
- what compatibility constraints affect the Source Reference where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Authority and Source References MUST remain distinguishable.

A Source Reference may support authority.

A Source Reference may explain authority.

A Source Reference may limit authority.

A Source Reference may challenge authority.

A Source Reference may preserve authority history.

A Source Reference does not equal Authority Level.

Authority Level does not equal a Source Reference.

A source-referenced entity is not automatically authoritative.

An authoritative entity is not automatically source-complete.

Authority in one scope MUST NOT imply adequate Source References in every scope.

A Source Reference in one scope MUST NOT imply authority in every scope.

Authority-related Source References MUST preserve the distinction between Source Material and Knowledge Records.

Source Material may provide evidence.

A Knowledge Record may interpret, summarize, extract, transform, classify, validate, or reason from Source Material.

A Source Reference should preserve traceability between the governed entity and the Source Material where that traceability affects interpretation, review, validation, approval, authority, privacy, lifecycle handling, compatibility, publication, import, export, migration, workflow behavior, agent behavior, implementation behavior, or downstream use.

A Knowledge Record MUST NOT inherit the authority of Source Material merely because it references that Source Material.

A Source Material item MUST NOT become authoritative for every derived Knowledge Record merely because it is official, reliable, available, cited, or frequently referenced.

Authority-related Source References MUST remain distinguishable from Source Authority.

Source Authority describes the governance weight, official status, interpretive relevance, review status, or approved use assigned to Source Material within a defined context.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Source Authority MAY support Authority Level.

Source Authority MUST NOT automatically transfer to a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity unless a governed authority process explicitly defines that transfer within a defined scope.

Authority-related Source References MUST remain distinguishable from Source Reliability.

Source Reliability describes assessed trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength of Source Material.

Source Reliability MAY inform Authority Review.

Source Reliability MAY support Authority Assignment.

Source Reliability MAY affect Authority Scope.

Source Reliability MAY trigger review, validation, approval review, provenance review, relationship review, privacy review, lifecycle review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Source Reliability MUST NOT replace Authority Level.

A reliable source may support a low-authority record.

An unreliable source may still be relevant for historical interpretation, contradiction, attribution, provenance, review, audit, or evidence comparison without becoming authoritative.

Authority-related Source References MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

A Source Reference may support Authority Scope.

A Source Reference may limit Authority Scope.

A Source Reference may show that authority applies only to a specific time, context, claim, interpretation, workflow, publication, export, migration, implementation, or downstream use.

A Source Reference MUST NOT silently broaden Authority Scope.

Authority-related Source References MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

A Source Reference may support Authority Assignment.

A Source Reference may challenge Authority Assignment.

A Source Reference may show that an Authority Assignment is incomplete, unsupported, contradicted, outdated, source-limited, provenance-limited, privacy-constrained, migration-limited, export-limited, publication-limited, or otherwise restricted.

A Source Reference MUST NOT assign Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related Source References MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

A Source Reference may provide evidence for Authority Review.

A Source Reference may explain why Authority Review is required.

A Source Reference may show why Authority Review is incomplete.

A Source Reference may show why Authority Level should be limited, suspended, downgraded, escalated, transferred, preserved, rejected, approved, deprecated, superseded, archived, restricted, quarantined, or treated as historical.

A Source Reference MUST NOT replace Authority Review unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related Source References MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

A Source Reference may support approval.

A Source Reference may limit approval.

A Source Reference may preserve approval context.

A Source Reference may challenge approval where source context is missing, incomplete, contradictory, outdated, restricted, superseded, unavailable, or incompatible.

A Source Reference MUST NOT create approval by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Authority-related Source References MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

A Source Reference may support validation.

A Source Reference may limit validation.

A Source Reference may show why validation is required.

A Source Reference may show why validation is incomplete.

A Source Reference MUST NOT create validation success by itself unless a governed validation process explicitly defines that behavior within a defined scope.

Authority-related Source References MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

A Source Reference may be part of provenance.

A Source Reference may support provenance.

A Source Reference may depend on provenance.

A Source Reference does not replace provenance unless a governed process explicitly defines that behavior within a defined scope.

Authority-related Source References SHOULD preserve enough provenance to determine what Source Material was used, what was extracted, what was transformed, who or what performed the work, whether review occurred, whether validation occurred, whether approval occurred, whether authority was assigned, and what scope applies where that context affects interpretation or use.

Authority-related Source References MUST remain distinguishable from Object Identity.

Creating, changing, reviewing, validating, approving, importing, exporting, migrating, repairing, preserving, restricting, or removing a Source Reference MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when authority-related Source References change unless a separate governed identity decision determines that the object has become meaningfully different.

Authority-related Source References MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether Source References must be created, preserved, reviewed, limited, restricted, quarantined, archived, migrated, exported, published, or used downstream.

Lifecycle State MUST NOT replace Source References.

Source References MUST NOT replace Lifecycle State.

A draft entity may have strong Source References.

An approved entity may have incomplete Source References.

A deprecated entity may require Source Reference preservation.

A superseded entity may retain Source References for historical authority interpretation.

An archived entity may retain Source References for audit, compatibility, or migration.

A quarantined entity may require Source Reference review before authority is restored.

Authority-related Source References MUST remain distinguishable from Privacy Classification.

Source References MUST preserve privacy boundaries.

A Source Reference MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, publication-restricted, provenance-restricted, relationship-restricted, or otherwise protected Source Material merely to support authority.

A high-authority entity may have restricted Source References.

A low-authority entity may have sensitive Source References.

A Source Reference may be authoritative for audit while remaining restricted from publication, export, synchronization, indexing, agent use, or broad implementation visibility.

Where Source Reference handling creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority-related Source References MUST remain distinguishable from Relationship Authority.

A relationship MAY connect a governed entity to Source Material.

A relationship MAY express source support, derivation, contradiction, attribution, evidence, interpretation, transformation, validation, review, approval, import, export, migration, or governance relevance.

A relationship MAY support, limit, or challenge authority-related Source References.

Relationship existence MUST NOT create Source Reference sufficiency by itself.

Relationship strength MUST NOT create Source Reference sufficiency by itself.

Relationship confidence MUST NOT create Source Reference sufficiency by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create Source Reference sufficiency by themselves.

Authority-related Source References MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support source review, source matching, extraction review, transformation review, contradiction detection, authority review, validation review, or human decision-making.

Agent Confidence MUST NOT create Source Reference sufficiency by itself.

An agent MAY propose Source References.

An agent MAY summarize Source Material.

An agent MAY classify Source References.

An agent MAY flag missing, incomplete, contradictory, stale, restricted, unavailable, superseded, or incompatible Source References.

An agent MUST NOT become an unreviewable authority for Source References where Source References affect governed interpretation or use.

Agent-generated Source References SHOULD remain traceable to the agent, model class, instruction, workflow, Source Material, evidence, extraction context, transformation context, confidence signal, review state, and human decision where applicable.

Authority-related Source References MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support Source References where a governed workflow explicitly defines completion as part of a source-reference process.

Workflow Completion MUST NOT create Source Reference sufficiency by itself.

A workflow MAY create, route, review, validate, approve, reject, limit, restrict, repair, preserve, import, export, migrate, or archive Source References only where the applicable workflow is governed to perform that role.

Workflow-generated Source References SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, authority, privacy, publication, export, migration, relationships, provenance, lifecycle handling, compatibility, or downstream use.

Authority-related Source References MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT create Source Reference sufficiency.

A governed entity MUST NOT be treated as source-supported merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT lose Source References merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority-related Source References SHOULD support source-reference history.

Source-reference history SHOULD identify or support identification of:

- prior Source References where applicable;
- new Source References where applicable;
- prior Authority Level where applicable;
- new Authority Level where applicable;
- prior Authority Scope where applicable;
- new Authority Scope where applicable;
- authority assignment history where applicable;
- authority review history where applicable;
- approval history where applicable;
- validation history where applicable;
- provenance history where applicable;
- relationship history where applicable;
- lifecycle history where applicable;
- privacy classification history where applicable;
- source-reference creator where applicable;
- source-reference editor where applicable;
- source-reference date where applicable;
- source-reference reason where applicable;
- reviewed Source Material where applicable;
- reviewed evidence where applicable;
- reviewed provenance where applicable;
- reviewed relationships where applicable;
- reviewed lifecycle state where applicable;
- reviewed privacy classification where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Authority-related Source References SHOULD support review.

A reviewer SHOULD be able to determine:

- what Source References exist;
- what Source References are missing where applicable;
- what Source Material is referenced;
- what Authority Level the Source References support, limit, challenge, or do not affect;
- what Authority Scope the Source References support, limit, challenge, or do not affect;
- whether Source References support, limit, challenge, or do not affect approval;
- whether Source References support, limit, challenge, or do not affect validation;
- whether Source References are current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, incomplete, contradicted, unavailable, or otherwise governed;
- whether Source References require further Authority Review;
- whether Source References require provenance review, privacy review, relationship review, lifecycle review, validation review, approval review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Authority-related Source References SHOULD support validation.

A validator SHOULD be able to determine whether:

- Source References are present where required;
- Source References are scoped where required;
- Source References use a governed value where a governed vocabulary exists;
- Source References remain distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Privacy Classification, Provenance, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- Source References preserve privacy boundaries;
- Source References preserve relationship meaning;
- Source References preserve provenance context;
- Source References remain compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority-related Source References SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, or regenerate Source References in a way that causes loss of meaning, broken source traceability, authority ambiguity, privacy exposure, validation failure, relationship failure, provenance failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority-related Source References SHOULD support historical preservation.

A governed entity MAY retain historical Source Reference context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical Source References do not mean the entity remains current.

Historical Source References do not mean the entity is approved for future use.

Historical Source References do not mean the entity is authoritative for future use.

Historical Source References do not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, or safe for downstream use.

Historical Source References SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, provenance review, and evidence review.

Authority and Source References are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what Source References exist, what Authority Level they support or challenge where applicable, what scope applies, what Source Material is referenced, what evidence supports authority, what provenance supports source use, what limits were applied, whether Source References are current or historical, whether further review or validation is required, whether privacy or lifecycle handling constrains Source References, and whether Source References remain meaningful across time and implementation replacement.

## 13. Authority and Relationships

Authority and Relationships are related but distinct concepts.

A relationship is a governed connection between entities where the connection affects meaning, interpretation, provenance, lifecycle state, authority, privacy classification, validation, compatibility, import, export, migration, governance, workflow behavior, agent behavior, implementation behavior, or downstream use.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

A relationship MAY support Authority Level.

A relationship MAY limit Authority Level.

A relationship MAY challenge Authority Level.

A relationship MAY preserve historical authority context.

A relationship MAY carry its own Authority Level where relationship meaning affects governed interpretation or use.

A relationship MUST NOT automatically create Authority Level merely because the relationship exists, is linked, is frequently traversed, appears central in a graph, has many backlinks, appears in search results, was inferred by an agent, was created by a workflow, was imported, was migrated, or was created by an implementation.

A governed entity may be:

- related but low-authority;
- related but unreviewed;
- related but unapproved;
- related but unvalidated;
- related but provisional;
- related but restricted;
- related but contradicted;
- related but historically authoritative;
- related but non-authoritative outside its scope;
- related to a high-authority entity without inheriting that authority;
- related to a restricted entity and therefore authority-limited;
- related to a superseded entity and therefore historically limited;
- connected by an agent-generated relationship but not authoritative until reviewed;
- connected by a workflow-generated relationship but not authoritative until governed.

Authority-related relationships SHOULD identify or support identification of:

- what governed entities participate in the relationship;
- what relationship type applies where applicable;
- what relationship direction applies where applicable;
- what Authority Level the relationship supports, limits, challenges, transfers, preserves, or does not affect where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment occurred where applicable;
- what Authority Review occurred where applicable;
- what approval occurred where applicable;
- what validation occurred where applicable;
- what Source References support or limit the relationship where applicable;
- what provenance supports the relationship where applicable;
- what lifecycle state affects the relationship where applicable;
- what privacy classification affects the relationship where applicable;
- what compatibility constraints affect the relationship where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Authority and Relationships MUST remain distinguishable.

A relationship may support authority.

A relationship may limit authority.

A relationship may challenge authority.

A relationship may preserve authority history.

A relationship may express authority context.

A relationship does not equal Authority Level.

Authority Level does not equal a relationship.

A related entity is not automatically authoritative.

An authoritative entity is not automatically relationship-complete.

Authority in one relationship context MUST NOT imply authority in every relationship context.

Relationship existence in one scope MUST NOT imply authority in every scope.

Authority-related relationships MUST remain distinguishable from Relationship Authority.

Relationship Authority describes the governance weight, review status, interpretive authority, or use-authority assigned to a relationship within a defined scope.

Authority Level may apply to a relationship.

Authority Level may apply to an entity participating in a relationship.

Authority Level may be supported, limited, challenged, transferred, preserved, inherited, downgraded, escalated, or contextualized through a relationship only where a governed authority process explicitly defines that behavior within a defined scope.

Relationship Authority MUST NOT be inferred merely from relationship existence, relationship count, graph centrality, backlink count, relationship strength, relationship confidence, visual graph position, search ranking, vector similarity, folder proximity, tag similarity, or implementation-specific linking.

Authority-related relationships MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Relationship context may support Authority Scope.

Relationship context may limit Authority Scope.

Relationship context may show that authority applies only between specific entities, within a specific direction, within a specific source context, within a specific workflow, within a specific publication context, within a specific migration context, or for a specific downstream use.

A relationship MUST NOT silently broaden Authority Scope.

A relationship MUST NOT silently make authority universal.

Authority-related relationships MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

A relationship may support Authority Assignment.

A relationship may challenge Authority Assignment.

A relationship may show that an Authority Assignment is incomplete, unsupported, contradicted, outdated, relationship-limited, source-limited, provenance-limited, privacy-constrained, migration-limited, export-limited, publication-limited, or otherwise restricted.

A relationship MUST NOT assign Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related relationships MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

A relationship may provide evidence for Authority Review.

A relationship may explain why Authority Review is required.

A relationship may show why Authority Review is incomplete.

A relationship may show why Authority Level should be limited, suspended, downgraded, escalated, transferred, preserved, rejected, approved, deprecated, superseded, archived, restricted, quarantined, or treated as historical.

A relationship MUST NOT replace Authority Review unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related relationships MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

A relationship may support approval.

A relationship may limit approval.

A relationship may preserve approval context.

A relationship may challenge approval where relationship context is missing, incomplete, contradictory, outdated, restricted, superseded, invalid, or incompatible.

A relationship MUST NOT create approval by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Authority-related relationships MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

A relationship may support validation.

A relationship may limit validation.

A relationship may show why validation is required.

A relationship may show why validation is incomplete.

A relationship MUST NOT create validation success by itself unless a governed validation process explicitly defines that behavior within a defined scope.

Authority-related relationships MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

A relationship may be supported by provenance.

A relationship may express provenance context.

A relationship may depend on provenance.

A relationship does not replace provenance unless a governed process explicitly defines that behavior within a defined scope.

Authority-related relationships SHOULD preserve enough provenance to determine why the relationship exists, who or what created it, what Source References support it, what review occurred, what validation occurred, whether approval occurred, whether authority was assigned, and what scope applies where that context affects interpretation or use.

Authority-related relationships MUST remain distinguishable from Source References.

A Source Reference is a traceable reference from a governed entity to Source Material.

A relationship may connect a governed entity to Source Material.

A relationship may connect Source Material to Knowledge Records, Knowledge Objects, provenance records, validation results, workflow outputs, agent outputs, import records, export records, migration records, decisions, or other governed entities.

A relationship MAY support Source Reference interpretation.

A relationship MAY limit Source Reference interpretation.

A relationship MUST NOT replace a Source Reference unless a governed process explicitly defines that behavior within a defined scope.

Relationship existence MUST NOT automatically make source support sufficient.

Authority-related relationships MUST remain distinguishable from Object Identity.

Creating, changing, reviewing, validating, approving, importing, exporting, migrating, repairing, preserving, restricting, or removing a relationship MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when authority-related relationships change unless a separate governed identity decision determines that the object has become meaningfully different.

Authority-related relationships MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether relationships must be created, preserved, reviewed, limited, restricted, quarantined, archived, migrated, exported, published, or used downstream.

Lifecycle State MUST NOT replace relationships.

Relationships MUST NOT replace Lifecycle State.

A draft entity may have authoritative relationships only within a limited scope.

An approved entity may have incomplete relationships.

A deprecated entity may require relationship preservation.

A superseded entity may retain relationships for historical authority interpretation.

An archived entity may retain relationships for audit, compatibility, or migration.

A quarantined entity may require relationship review before authority is restored.

Authority-related relationships MUST remain distinguishable from Privacy Classification.

Relationships MUST preserve privacy boundaries.

A relationship MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, publication-restricted, source-restricted, provenance-restricted, or otherwise protected information merely to support authority.

A high-authority entity may have restricted relationships.

A low-authority entity may have sensitive relationships.

A relationship may be authoritative for audit while remaining restricted from publication, export, synchronization, indexing, agent use, or broad implementation visibility.

Where relationship handling creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority-related relationships MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support relationship review, relationship matching, contradiction detection, authority review, validation review, source checking, provenance review, or human decision-making.

Agent Confidence MUST NOT create relationship authority by itself.

An agent MAY propose relationships.

An agent MAY classify relationships.

An agent MAY summarize relationships.

An agent MAY flag missing, incomplete, contradictory, stale, restricted, invalid, superseded, or incompatible relationships.

An agent MUST NOT become an unreviewable authority for relationships where relationships affect governed interpretation or use.

Agent-generated relationships SHOULD remain traceable to the agent, model class, instruction, workflow, Source Material, evidence, relationship context, confidence signal, review state, and human decision where applicable.

Authority-related relationships MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support relationships where a governed workflow explicitly defines completion as part of a relationship process.

Workflow Completion MUST NOT create relationship authority by itself.

A workflow MAY create, route, review, validate, approve, reject, limit, restrict, repair, preserve, import, export, migrate, or archive relationships only where the applicable workflow is governed to perform that role.

Workflow-generated relationships SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, authority, privacy, publication, export, migration, Source References, provenance, lifecycle handling, compatibility, or downstream use.

Authority-related relationships MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT create relationship authority.

A governed entity MUST NOT be treated as relationship-supported merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A relationship MUST NOT be treated as governed merely because an implementation displays a link, backlink, graph edge, database relation, search association, vector similarity, embedding relationship, folder association, tag association, or visual connection.

A governed entity MUST NOT lose relationships merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority-related relationships SHOULD support relationship history.

Relationship history SHOULD identify or support identification of:

- prior relationships where applicable;
- new relationships where applicable;
- prior Authority Level where applicable;
- new Authority Level where applicable;
- prior Authority Scope where applicable;
- new Authority Scope where applicable;
- authority assignment history where applicable;
- authority review history where applicable;
- approval history where applicable;
- validation history where applicable;
- Source Reference history where applicable;
- provenance history where applicable;
- lifecycle history where applicable;
- privacy classification history where applicable;
- relationship creator where applicable;
- relationship editor where applicable;
- relationship date where applicable;
- relationship reason where applicable;
- reviewed relationships where applicable;
- reviewed Source References where applicable;
- reviewed provenance where applicable;
- reviewed lifecycle state where applicable;
- reviewed privacy classification where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Authority-related relationships SHOULD support review.

A reviewer SHOULD be able to determine:

- what relationships exist;
- what relationships are missing where applicable;
- what entities participate in the relationships;
- what relationship type and direction apply where applicable;
- what Authority Level the relationships support, limit, challenge, transfer, preserve, or do not affect;
- what Authority Scope the relationships support, limit, challenge, or do not affect;
- whether relationships support, limit, challenge, or do not affect approval;
- whether relationships support, limit, challenge, or do not affect validation;
- whether relationships are current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, incomplete, contradicted, invalid, or otherwise governed;
- whether relationships require further Authority Review;
- whether relationships require Source Reference review, provenance review, privacy review, lifecycle review, validation review, approval review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Authority-related relationships SHOULD support validation.

A validator SHOULD be able to determine whether:

- relationships are present where required;
- relationships are scoped where required;
- relationships use a governed value where a governed vocabulary exists;
- relationships remain distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- relationships preserve privacy boundaries;
- relationships preserve relationship meaning;
- relationships preserve Source Reference context;
- relationships preserve provenance context;
- relationships remain compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority-related relationships SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, reverse, duplicate, or regenerate relationships in a way that causes loss of meaning, broken source traceability, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority-related relationships SHOULD support historical preservation.

A governed entity MAY retain historical relationship context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical relationships do not mean the entity remains current.

Historical relationships do not mean the entity is approved for future use.

Historical relationships do not mean the entity is authoritative for future use.

Historical relationships do not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, or safe for downstream use.

Historical relationships SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, provenance review, and evidence review.

Authority and Relationships are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what relationships exist, what Authority Level they support or challenge where applicable, what scope applies, what entities participate, what relationship type and direction apply, what Source References and provenance support relationship authority, what limits were applied, whether relationships are current or historical, whether further review or validation is required, whether privacy or lifecycle handling constrains relationships, and whether relationships remain meaningful across time and implementation replacement.

## 14. Authority and Lifecycle State

Authority and Lifecycle State are related but distinct concepts.

Lifecycle State describes the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, governed document, decision, or other governed entity.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Lifecycle State MAY affect Authority Level handling.

Lifecycle State MUST NOT replace Authority Level.

Authority Level MUST NOT replace Lifecycle State.

A lifecycle state MAY affect whether authority may be:

- assigned;
- proposed;
- reviewed;
- approved;
- rejected;
- limited;
- suspended;
- downgraded;
- escalated;
- transferred;
- inherited;
- preserved;
- deprecated;
- superseded;
- archived;
- restricted;
- quarantined;
- repaired;
- published;
- exported;
- migrated;
- synchronized;
- indexed;
- exposed to agents;
- exposed to workflows;
- exposed to implementations;
- applied downstream.

A lifecycle state MUST NOT automatically create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

A governed entity may be:

- approved but low-authority;
- draft but based on a high-authority source;
- high-authority but pending review;
- high-authority but pending validation;
- high-authority but deprecated;
- high-authority but superseded;
- high-authority but archived;
- high-authority but restricted;
- high-authority but quarantined;
- high-authority but requiring repair;
- validated but not authoritative;
- source-supported but not authoritative;
- relationship-supported but not authoritative;
- agent-generated but not authoritative until reviewed;
- workflow-generated but not authoritative until governed;
- authoritative for historical interpretation but not current use;
- authoritative for one scope but not another.

Authority-related lifecycle handling SHOULD identify or support identification of:

- what governed entity the lifecycle state applies to;
- what lifecycle state applies;
- what Authority Level applies where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment occurred where applicable;
- what Authority Review occurred where applicable;
- what approval occurred where applicable;
- what validation occurred where applicable;
- what Source References support or limit authority where applicable;
- what relationships support or limit authority where applicable;
- what provenance supports the lifecycle-authority relationship where applicable;
- what privacy classification affects authority where applicable;
- what compatibility constraints affect authority where applicable;
- what import, export, migration, publication, workflow, agent, implementation, or downstream-use limits apply where applicable.

Authority and Lifecycle State MUST remain distinguishable.

Lifecycle State may support authority handling.

Lifecycle State may limit authority handling.

Lifecycle State may suspend authority handling.

Lifecycle State may require authority review.

Lifecycle State may preserve authority history.

Lifecycle State does not equal Authority Level.

Authority Level does not equal Lifecycle State.

A lifecycle-approved entity is not automatically authoritative.

An authoritative entity is not automatically approved.

Authority in one lifecycle state MUST NOT imply authority in every lifecycle state.

Lifecycle State in one scope MUST NOT imply authority in every scope.

Authority-related lifecycle handling MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Lifecycle State describes the governed state of the entity.

A lifecycle state may affect Authority Scope.

A lifecycle state may limit Authority Scope.

A lifecycle state may show that authority applies only historically, internally, provisionally, restrictively, or conditionally.

A lifecycle state MUST NOT silently broaden Authority Scope.

A lifecycle state MUST NOT silently make authority universal.

Authority-related lifecycle handling MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

Lifecycle State may affect whether Authority Assignment is permitted, blocked, limited, suspended, preserved, reviewed, or required.

A lifecycle state may trigger proposed Authority Assignment only where a governed authority process explicitly defines that behavior within a defined scope.

A lifecycle state MUST NOT assign Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related lifecycle handling MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

Lifecycle State may require Authority Review.

Lifecycle State may limit Authority Review.

Lifecycle State may preserve Authority Review history.

Lifecycle State may show why Authority Review is incomplete.

Lifecycle State may show why Authority Level should be limited, suspended, downgraded, escalated, transferred, preserved, rejected, approved, deprecated, superseded, archived, restricted, quarantined, repaired, or treated as historical.

Lifecycle State MUST NOT replace Authority Review unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related lifecycle handling MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

Lifecycle State may record, reflect, or depend on approval.

Approval may affect Lifecycle State.

Approval may support Authority Level.

Approval MUST NOT automatically create unlimited authority.

An approved lifecycle state MUST NOT imply broad authority unless a governed authority process explicitly defines that result within a defined scope.

Authority-related lifecycle handling MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

Lifecycle State may require validation.

Validation may affect Lifecycle State.

Validation may support Authority Level.

Validation success MUST NOT imply authority unless a governed authority process explicitly defines that result within a defined scope.

A validation-passing lifecycle state may still require Authority Review.

A validation-failing lifecycle state may still preserve historical authority context.

Authority-related lifecycle handling MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

Lifecycle State may require provenance preservation.

Lifecycle State may depend on provenance.

Provenance may explain why lifecycle-related authority changed.

Provenance may show why authority was assigned, limited, suspended, downgraded, escalated, transferred, preserved, deprecated, superseded, archived, restricted, quarantined, repaired, or treated as historical.

Lifecycle State MUST NOT replace provenance.

Provenance MUST NOT replace Lifecycle State.

Authority-related lifecycle handling MUST remain distinguishable from Source References.

A Source Reference is a traceable reference from a governed entity to Source Material.

Lifecycle State may affect whether Source References must be reviewed, preserved, restricted, archived, exported, migrated, published, or used downstream.

A Source Reference may support lifecycle-related authority handling.

A Source Reference may limit lifecycle-related authority handling.

A Source Reference may challenge lifecycle-related authority handling.

Source existence, citation, availability, reliability, official status, popularity, frequency of citation, or source authority MUST NOT automatically override Lifecycle State or Authority Level unless a governed process explicitly defines that behavior within a defined scope.

Authority-related lifecycle handling MUST remain distinguishable from Relationship Authority.

A relationship may support lifecycle-related authority handling.

A relationship may limit lifecycle-related authority handling.

A relationship may preserve lifecycle-related authority history.

A relationship may show why authority is current, historical, deprecated, superseded, archived, restricted, quarantined, repaired, provisional, or otherwise governed.

Relationship existence MUST NOT create lifecycle authority by itself.

Relationship strength MUST NOT create lifecycle authority by itself.

Relationship confidence MUST NOT create lifecycle authority by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create lifecycle authority by themselves.

Authority-related lifecycle handling MUST remain distinguishable from Object Identity.

Changing Lifecycle State MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Changing Authority Level MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when lifecycle-related authority changes unless a separate governed identity decision determines that the object has become meaningfully different.

Authority-related lifecycle handling MUST remain distinguishable from Privacy Classification.

Lifecycle State and Authority Level MUST preserve privacy boundaries.

A high-authority entity may remain private, restricted, confidential, sensitive, non-exportable, agent-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, or otherwise protected.

A lifecycle-approved entity may still be private.

A lifecycle-archived entity may still be sensitive.

A lifecycle-deprecated entity may still require privacy protection.

A lifecycle-quarantined entity may require stronger privacy handling.

Lifecycle State MUST NOT make restricted content public, exportable, publishable, searchable, synchronized, agent-readable, or implementation-visible merely because the entity carries Authority Level.

Where lifecycle-authority handling creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority-related lifecycle handling MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support lifecycle review, authority review, validation review, source checking, relationship checking, contradiction detection, repair recommendations, or human decision-making.

Agent Confidence MUST NOT create Authority Level.

Agent Confidence MUST NOT create Lifecycle State.

An agent MAY propose lifecycle-related authority handling.

An agent MAY flag lifecycle-authority conflicts.

An agent MAY recommend review, validation, repair, limitation, suspension, downgrade, escalation, rejection, approval review, source review, privacy review, relationship review, provenance review, publication review, export review, migration review, or downstream-use review.

An agent MUST NOT become an unreviewable authority for lifecycle-related authority handling where authority affects governed interpretation or use.

Agent-supported lifecycle-authority recommendations SHOULD remain traceable to the agent, model class, instruction, workflow, Source Material, evidence, lifecycle context, authority context, confidence signal, review state, and human decision where applicable.

Authority-related lifecycle handling MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support lifecycle-related authority handling where a governed workflow explicitly defines completion as part of a lifecycle or authority process.

Workflow Completion MUST NOT create Authority Level by itself.

Workflow Completion MUST NOT create Lifecycle State by itself unless a governed workflow explicitly defines that lifecycle transition within a defined scope.

A workflow MAY create, route, review, validate, approve, reject, limit, suspend, downgrade, escalate, transfer, preserve, repair, import, export, migrate, publish, archive, restrict, or quarantine lifecycle-related authority only where the applicable workflow is governed to perform that role.

Workflow-supported lifecycle-authority handling SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, authority, privacy, publication, export, migration, Source References, relationships, provenance, lifecycle handling, compatibility, or downstream use.

Authority-related lifecycle handling MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT create Authority Level.

Implementation Visibility MUST NOT create Lifecycle State.

A governed entity MUST NOT be treated as authoritative merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, published, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT be treated as approved, deprecated, superseded, archived, restricted, quarantined, repaired, current, active, or final merely because of folder placement, filename convention, tag convention, user-interface state, plugin field, database row, search ranking, graph position, backlink behavior, workflow queue, agent task label, or implementation-specific status label.

A governed entity MUST NOT lose Lifecycle State or Authority Level merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

Authority-related lifecycle handling SHOULD support lifecycle-authority history.

Lifecycle-authority history SHOULD identify or support identification of:

- prior lifecycle state where applicable;
- new lifecycle state where applicable;
- prior Authority Level where applicable;
- new Authority Level where applicable;
- prior Authority Scope where applicable;
- new Authority Scope where applicable;
- authority assignment history where applicable;
- authority review history where applicable;
- approval history where applicable;
- validation history where applicable;
- Source Reference history where applicable;
- relationship history where applicable;
- provenance history where applicable;
- privacy classification history where applicable;
- lifecycle-authority creator where applicable;
- lifecycle-authority editor where applicable;
- lifecycle-authority date where applicable;
- lifecycle-authority reason where applicable;
- reviewed lifecycle state where applicable;
- reviewed Authority Level where applicable;
- reviewed Source References where applicable;
- reviewed relationships where applicable;
- reviewed provenance where applicable;
- reviewed privacy classification where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Authority-related lifecycle handling SHOULD support review.

A reviewer SHOULD be able to determine:

- what Lifecycle State applies;
- what Authority Level applies;
- what Authority Scope applies;
- whether Lifecycle State supports, limits, suspends, challenges, preserves, or does not affect Authority Level;
- whether Authority Level is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, quarantined, or otherwise governed;
- whether lifecycle-related authority requires further Authority Review;
- whether lifecycle-related authority requires Source Reference review, provenance review, relationship review, privacy review, validation review, approval review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Authority-related lifecycle handling SHOULD support validation.

A validator SHOULD be able to determine whether:

- Lifecycle State is present where required;
- Authority Level is present where required;
- Authority Scope is present where required;
- lifecycle-related authority is scoped where required;
- lifecycle-related authority uses a governed value where a governed vocabulary exists;
- lifecycle-related authority remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- lifecycle-related authority preserves privacy boundaries;
- lifecycle-related authority preserves Source Reference context;
- lifecycle-related authority preserves relationship meaning;
- lifecycle-related authority preserves provenance context;
- lifecycle-related authority remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority-related lifecycle handling SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, override, or regenerate Lifecycle State or Authority Level in a way that causes loss of meaning, broken source traceability, broken provenance, authority ambiguity, lifecycle ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority-related lifecycle handling SHOULD support historical preservation.

A governed entity MAY retain historical lifecycle-related authority context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical lifecycle-related authority does not mean the entity remains current.

Historical lifecycle-related authority does not mean the entity is approved for future use.

Historical lifecycle-related authority does not mean the entity is authoritative for future use.

Historical lifecycle-related authority does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, or safe for downstream use.

Historical lifecycle-related authority SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, provenance review, lifecycle review, and evidence review.

Authority and Lifecycle State are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what Lifecycle State applies, what Authority Level applies, what scope applies, whether lifecycle state supports or limits authority, what evidence and provenance support lifecycle-related authority handling, what limits were applied, whether the authority is current or historical, whether further review or validation is required, whether privacy handling constrains lifecycle-related authority, and whether lifecycle-related authority remains meaningful across time and implementation replacement.

## 15. Authority and Privacy Classification

Authority and Privacy Classification are related but distinct concepts.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation visibility, or handling expectations for a governed entity.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Privacy Classification MAY affect Authority Level handling.

Privacy Classification MUST NOT replace Authority Level.

Authority Level MUST NOT replace Privacy Classification.

Authority Level MUST NOT weaken privacy requirements.

A high-authority entity MAY remain:

- private;
- restricted;
- confidential;
- sensitive;
- non-exportable;
- agent-restricted;
- workflow-restricted;
- publication-restricted;
- source-restricted;
- provenance-restricted;
- relationship-restricted;
- implementation-restricted;
- migration-restricted;
- downstream-use restricted.

A low-authority entity MAY still require strong privacy protection.

A public entity MAY remain low-authority.

A private entity MAY be high-authority within an authorized scope.

A restricted entity MAY be authoritative only for authorized humans, agents, workflows, validators, storage systems, implementations, publications, exports, migrations, or downstream uses.

Privacy Classification SHALL take precedence over operational convenience where authority handling creates privacy risk.

Authority-related privacy handling SHOULD identify or support identification of:

- what governed entity the Privacy Classification applies to;
- what Privacy Classification applies;
- what Authority Level applies where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment occurred where applicable;
- what Authority Review occurred where applicable;
- what approval occurred where applicable;
- what validation occurred where applicable;
- what Lifecycle State applies where applicable;
- what Source References are privacy-relevant where applicable;
- what relationships are privacy-relevant where applicable;
- what provenance is privacy-relevant where applicable;
- what access, exposure, routing, publication, synchronization, indexing, backup, export, migration, agent, workflow, implementation, or downstream-use limits apply where applicable.

Authority and Privacy Classification MUST remain distinguishable.

Privacy Classification may limit authority use.

Privacy Classification may restrict authority exposure.

Privacy Classification may require authority review.

Privacy Classification may require privacy review before authority is used, published, exported, migrated, synchronized, indexed, routed, exposed to agents, exposed to workflows, or applied downstream.

Privacy Classification does not equal Authority Level.

Authority Level does not equal Privacy Classification.

A high-authority entity is not automatically public.

A public entity is not automatically authoritative.

A private entity is not automatically low-authority.

A restricted entity is not automatically unusable.

A restricted entity may be usable only within an authorized scope.

Authority in one privacy context MUST NOT imply authority in every privacy context.

Privacy Classification in one scope MUST NOT imply authority in every scope.

Authority-related privacy handling MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation visibility, or handling expectations.

Privacy Classification MAY limit Authority Scope.

Privacy Classification MAY show that authority applies only internally, privately, confidentially, restrictively, conditionally, or for authorized review.

Privacy Classification MUST NOT silently broaden Authority Scope.

Privacy Classification MUST NOT silently make authority public.

Privacy Classification MUST NOT silently make authority exportable, publishable, searchable, synchronized, agent-readable, workflow-readable, implementation-visible, or downstream-usable.

Authority-related privacy handling MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

Privacy Classification may affect whether Authority Assignment is permitted, blocked, limited, restricted, reviewed, or required.

Privacy Classification may require that Authority Assignment be visible only to authorized actors.

Privacy Classification may require that Authority Assignment preserve restricted provenance, restricted Source References, restricted relationships, restricted lifecycle history, restricted validation results, or restricted approval context.

Privacy Classification MUST NOT assign Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related privacy handling MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

Privacy Classification may require Authority Review.

Privacy Classification may limit Authority Review to authorized reviewers.

Privacy Classification may require privacy review before Authority Review can expose, cite, summarize, export, publish, synchronize, index, migrate, route, or share restricted information.

Privacy Classification may show why Authority Review is incomplete for unauthorized reviewers.

Privacy Classification MUST NOT replace Authority Review unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related privacy handling MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

Approval may be limited by Privacy Classification.

Privacy Classification may prevent approved content from being public, exportable, publishable, searchable, synchronized, indexed, agent-readable, workflow-readable, implementation-visible, or broadly downstream-usable.

An approved entity may still be private.

An approved entity may still be confidential.

An approved entity may still be non-exportable.

An approved entity may still be publication-restricted.

An approved entity may still be agent-restricted.

Approval MUST NOT override Privacy Classification unless a governed privacy process explicitly permits that behavior within a defined scope.

Authority-related privacy handling MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

Privacy Classification may affect validation requirements.

Validation may check whether privacy handling is present, scoped, preserved, compatible, and implementation-independent.

Validation success MUST NOT make restricted content public, exportable, publishable, searchable, synchronized, indexed, agent-readable, workflow-readable, implementation-visible, or downstream-usable unless privacy rules explicitly permit that behavior.

A validation-passing entity may remain private.

A validation-failing entity may require stronger privacy handling.

A validation result MUST NOT override Privacy Classification unless a governed privacy process explicitly defines that behavior within a defined scope.

Authority-related privacy handling MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect privacy handling.

Privacy Classification may affect lifecycle handling.

A draft entity may be private.

An approved entity may be private.

A deprecated entity may remain sensitive.

A superseded entity may remain confidential.

An archived entity may remain restricted.

A quarantined entity may require stronger privacy protection.

A repaired entity may require privacy review before authority is restored.

Lifecycle State MUST NOT override Privacy Classification unless a governed privacy process explicitly permits that behavior within a defined scope.

Privacy Classification MUST NOT replace Lifecycle State.

Authority-related privacy handling MUST remain distinguishable from Provenance.

Provenance may contain restricted information.

Provenance may explain why Privacy Classification was assigned, reviewed, limited, changed, preserved, migrated, exported, imported, archived, restricted, quarantined, or repaired.

Provenance may support privacy review.

Provenance may be required to interpret authority correctly.

Provenance MUST NOT be exposed merely because it supports Authority Level.

A provenance record may be authoritative for audit while remaining restricted from publication, export, synchronization, indexing, agent use, workflow use, or broad implementation visibility.

Where provenance and authority handling create privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority-related privacy handling MUST remain distinguishable from Source References.

Source References may contain or point to restricted Source Material.

Source References may require privacy review before use.

Source References may support Authority Level while remaining restricted.

Source References may be valid for authorized review while not being public, exportable, publishable, searchable, synchronized, indexed, agent-readable, workflow-readable, implementation-visible, or broadly downstream-usable.

A Source Reference MUST NOT expose restricted Source Material merely because the source supports Authority Level.

Source existence, citation, availability, reliability, official status, popularity, frequency of citation, or source authority MUST NOT override Privacy Classification unless a governed privacy process explicitly defines that behavior within a defined scope.

Authority-related privacy handling MUST remain distinguishable from Relationship Authority.

Relationships may contain privacy-sensitive meaning.

Relationships may reveal restricted connections, restricted sources, restricted provenance, restricted lifecycle history, restricted authority context, restricted validation results, or restricted downstream-use context.

A relationship may support Authority Level while remaining restricted.

A relationship may be authoritative for audit while not being public, exportable, publishable, searchable, synchronized, indexed, agent-readable, workflow-readable, implementation-visible, or broadly downstream-usable.

Relationship existence MUST NOT override Privacy Classification.

Relationship strength MUST NOT override Privacy Classification.

Relationship confidence MUST NOT override Privacy Classification.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT override Privacy Classification.

Authority-related privacy handling MUST remain distinguishable from Object Identity.

Changing Privacy Classification MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

Changing Authority Level MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when authority-related privacy handling changes unless a separate governed identity decision determines that the object has become meaningfully different.

Authority-related privacy handling MUST remain distinguishable from Agent Confidence.

Agent Confidence MAY support privacy review, authority review, routing, triage, validation, source checking, relationship checking, contradiction detection, or human decision-making.

Agent Confidence MUST NOT create Authority Level.

Agent Confidence MUST NOT create Privacy Classification.

Agent Confidence MUST NOT weaken Privacy Classification.

An agent MAY propose privacy-related authority handling.

An agent MAY flag privacy-authority conflicts.

An agent MAY recommend review, validation, repair, limitation, restriction, suspension, downgrade, escalation, rejection, approval review, source review, relationship review, provenance review, lifecycle review, publication review, export review, migration review, or downstream-use review.

An agent MUST NOT become an unreviewable authority for privacy-related authority handling where privacy affects governed interpretation or use.

Agent access to restricted information MUST NOT imply permission to expose, summarize, publish, export, synchronize, index, migrate, or use that information downstream.

Agent-supported privacy-authority recommendations SHOULD remain traceable to the agent, model class, instruction, workflow, Source Material, evidence, privacy context, authority context, confidence signal, review state, and human decision where applicable.

Authority-related privacy handling MUST remain distinguishable from Workflow Completion.

Workflow Completion MAY support privacy-related authority handling where a governed workflow explicitly defines completion as part of a privacy or authority process.

Workflow Completion MUST NOT create Authority Level by itself.

Workflow Completion MUST NOT create Privacy Classification by itself unless a governed workflow explicitly defines that privacy transition within a defined scope.

Workflow Completion MUST NOT weaken Privacy Classification by itself.

A workflow MAY create, route, review, validate, approve, reject, limit, suspend, downgrade, escalate, transfer, preserve, repair, import, export, migrate, publish, archive, restrict, quarantine, or expose privacy-related authority only where the applicable workflow is governed to perform that role.

Workflow-supported privacy-authority handling SHOULD preserve enough provenance for future review where workflow activity affects interpretation, governance, authority, privacy, publication, export, migration, Source References, relationships, provenance, lifecycle handling, compatibility, or downstream use.

Authority-related privacy handling MUST remain distinguishable from Implementation Visibility.

Implementation Visibility MUST NOT create Authority Level.

Implementation Visibility MUST NOT create Privacy Classification.

Implementation Visibility MUST NOT weaken Privacy Classification.

A governed entity MUST NOT be treated as public, unrestricted, exportable, publishable, searchable, synchronized, indexed, agent-readable, workflow-readable, implementation-visible, or downstream-usable merely because it is visible, searchable, indexed, ranked, displayed, linked, surfaced, synchronized, cached, placed in a folder, tagged, color-coded, starred, pinned, recommended, or frequently used by a specific implementation.

A governed entity MUST NOT be treated as private, restricted, confidential, non-exportable, unpublished, quarantined, or inaccessible merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, or displays it differently.

A governed entity MUST NOT lose Privacy Classification or Authority Level merely because an implementation hides, filters, archives, de-indexes, moves, renames, caches, exports, imports, migrates, synchronizes, publishes, or displays it differently.

Authority-related privacy handling SHOULD support privacy-authority history.

Privacy-authority history SHOULD identify or support identification of:

- prior Privacy Classification where applicable;
- new Privacy Classification where applicable;
- prior Authority Level where applicable;
- new Authority Level where applicable;
- prior Authority Scope where applicable;
- new Authority Scope where applicable;
- authority assignment history where applicable;
- authority review history where applicable;
- approval history where applicable;
- validation history where applicable;
- lifecycle history where applicable;
- Source Reference history where applicable;
- relationship history where applicable;
- provenance history where applicable;
- privacy-authority creator where applicable;
- privacy-authority editor where applicable;
- privacy-authority date where applicable;
- privacy-authority reason where applicable;
- reviewed privacy classification where applicable;
- reviewed Authority Level where applicable;
- reviewed Source References where applicable;
- reviewed relationships where applicable;
- reviewed provenance where applicable;
- reviewed lifecycle state where applicable;
- reviewed validation results where applicable;
- reviewed compatibility constraints where applicable;
- reviewed import, export, migration, publication, workflow, agent, implementation, or downstream-use limits where applicable.

Authority-related privacy handling SHOULD support review.

A reviewer SHOULD be able to determine:

- what Privacy Classification applies;
- what Authority Level applies;
- what Authority Scope applies;
- whether Privacy Classification limits, restricts, suspends, challenges, preserves, or does not affect Authority Level;
- whether Authority Level affects privacy handling;
- whether authority is permitted for internal review, publication, export, migration, synchronization, indexing, agent use, workflow use, implementation visibility, or downstream use;
- whether authority-related privacy handling is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, quarantined, or otherwise governed;
- whether privacy-related authority requires further Authority Review;
- whether privacy-related authority requires Source Reference review, provenance review, relationship review, lifecycle review, validation review, approval review, compatibility review, migration review, export review, publication review, workflow review, or agent-output review.

Authority-related privacy handling SHOULD support validation.

A validator SHOULD be able to determine whether:

- Privacy Classification is present where required;
- Authority Level is present where required;
- Authority Scope is present where required;
- privacy-related authority is scoped where required;
- privacy-related authority uses a governed value where a governed vocabulary exists;
- privacy-related authority remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Provenance, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- privacy-related authority preserves privacy boundaries;
- privacy-related authority preserves Source Reference context;
- privacy-related authority preserves relationship meaning;
- privacy-related authority preserves provenance context;
- privacy-related authority remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority-related privacy handling SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, override, or regenerate Privacy Classification or Authority Level in a way that causes loss of meaning, broken source traceability, broken provenance, authority ambiguity, privacy ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority-related privacy handling SHOULD support historical preservation.

A governed entity MAY retain historical privacy-related authority context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical privacy-related authority does not mean the entity remains current.

Historical privacy-related authority does not mean the entity is approved for future use.

Historical privacy-related authority does not mean the entity is authoritative for future use.

Historical privacy-related authority does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, safe for workflow use, or safe for downstream use.

Historical privacy-related authority SHOULD preserve enough context for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, privacy review, provenance review, lifecycle review, and evidence review.

Authority and Privacy Classification are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what Privacy Classification applies, what Authority Level applies, what scope applies, whether privacy classification permits or restricts authority use, what evidence and provenance support privacy-related authority handling, what limits were applied, whether the authority is current or historical, whether further review or validation is required, whether privacy handling constrains publication, export, migration, synchronization, indexing, agent use, workflow use, implementation visibility, or downstream use, and whether privacy-related authority remains meaningful across time and implementation replacement.

## 16. Authority and Agent Behavior

Authority and Agent Behavior are related but distinct concepts.

Agent Behavior describes how an agent may read, classify, summarize, extract, transform, propose, validate, route, review, flag, recommend, modify, publish, import, export, migrate, or otherwise process governed entities.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Agent Behavior MAY support Authority Level.

Agent Behavior MAY propose Authority Level.

Agent Behavior MAY recommend Authority Review.

Agent Behavior MAY recommend Authority Assignment.

Agent Behavior MAY recommend limitation, suspension, downgrade, escalation, transfer, preservation, rejection, approval review, validation review, source review, relationship review, provenance review, lifecycle review, privacy review, publication review, export review, migration review, workflow review, implementation review, or downstream-use review.

Agent Behavior MUST NOT create Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Agent Behavior MUST NOT create approval by itself.

Agent Behavior MUST NOT create validation success by itself.

Agent Behavior MUST NOT override Privacy Classification.

Agent Behavior MUST NOT override Lifecycle State.

Agent Behavior MUST NOT override Object Identity.

An agent MAY assist with authority-related work, but an agent MUST NOT become an unreviewable authority where authority affects governed interpretation or use.

Agent-related authority handling MAY apply to:

- Knowledge Objects;
- Knowledge Records;
- Source References;
- Source Material where applicable;
- provenance records;
- relationships;
- metadata records;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- governed documents;
- decisions;
- other governed entities.

Agent-related authority handling SHOULD identify or support identification of:

- what governed entity the agent processed;
- what agent performed the work where applicable;
- what model class, agent class, tool, workflow, prompt, instruction, or process was used where applicable;
- what Authority Level was read, proposed, supported, limited, challenged, or unaffected where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment was proposed or affected where applicable;
- what Authority Review is required where applicable;
- what approval is required where applicable;
- what validation occurred or is required where applicable;
- what Source References were used where applicable;
- what relationships were used or proposed where applicable;
- what provenance supports the agent activity where applicable;
- what Lifecycle State applies where applicable;
- what Privacy Classification applies where applicable;
- what compatibility constraints apply where applicable;
- what import, export, migration, publication, workflow, implementation, or downstream-use limits apply where applicable.

Authority and Agent Behavior MUST remain distinguishable.

Agent Behavior may support authority.

Agent Behavior may propose authority.

Agent Behavior may challenge authority.

Agent Behavior may route authority for review.

Agent Behavior may preserve authority history.

Agent Behavior does not equal Authority Level.

Authority Level does not equal Agent Behavior.

An agent-generated entity is not automatically authoritative.

An agent-reviewed entity is not automatically approved.

An agent-classified entity is not automatically valid.

An agent-summarized entity is not automatically source-complete.

An agent-routed entity is not automatically reviewed.

An agent-visible entity is not automatically permitted for agent use in every scope.

Authority in one agent context MUST NOT imply authority in every agent context.

Agent access in one scope MUST NOT imply authority in every scope.

Agent-related authority handling MUST remain distinguishable from Agent Confidence.

Agent Confidence describes an agent-generated indication of certainty, probability, model confidence, classification confidence, extraction confidence, relationship confidence, validation confidence, or recommendation confidence.

Agent Confidence MAY support triage, routing, prioritization, review, validation, source checking, relationship checking, contradiction detection, repair recommendations, or human decision-making.

Agent Confidence MUST NOT create Authority Level.

Agent Confidence MUST NOT create Authority Scope.

Agent Confidence MUST NOT create Approval.

Agent Confidence MUST NOT create Validation State.

Agent Confidence MUST NOT create Lifecycle State.

Agent Confidence MUST NOT create Privacy Classification.

Agent Confidence MUST NOT override Source References, provenance, relationships, lifecycle state, privacy classification, validation results, approval, review, workflow state, implementation behavior, or downstream-use limits.

A high-confidence agent output may still be low-authority.

A low-confidence agent output may still be useful for review, contradiction detection, triage, or source-checking.

A confidence score MUST NOT be treated as factual truth, approval, review completion, validation success, source authority, relationship authority, or governance authority by itself.

Agent-related authority handling MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Agent Scope describes what an agent may read, propose, classify, validate, summarize, modify, route, export, migrate, publish, or otherwise process.

Agent Scope may limit Authority Scope handling.

Authority Scope may limit Agent Behavior.

Agent access to a governed entity MUST NOT silently broaden Authority Scope.

Agent access to a governed entity MUST NOT silently make authority public, exportable, publishable, searchable, synchronized, indexable, workflow-readable, implementation-visible, or downstream-usable.

Agent-related authority handling MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

An agent MAY propose Authority Assignment.

An agent MAY recommend Authority Assignment.

An agent MAY flag missing, incomplete, contradictory, unsupported, stale, restricted, invalid, provisional, deprecated, superseded, archived, quarantined, or incompatible Authority Assignment.

An agent MUST NOT assign Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Agent-proposed Authority Assignment SHOULD remain clearly distinguishable from human-approved authority, workflow-approved authority, validation-supported authority, source-supported authority, and governed Authority Level.

Agent-related authority handling MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

An agent MAY support Authority Review.

An agent MAY prepare evidence for Authority Review.

An agent MAY recommend Authority Review.

An agent MAY flag authority conflicts for review.

An agent MAY summarize review context.

An agent MUST NOT satisfy Authority Review by itself unless a governed authority process explicitly defines that behavior within a defined scope.

An agent MUST NOT become an unreviewable reviewer where authority affects governed interpretation, governance, validation, publication, export, migration, workflow behavior, implementation behavior, or downstream use.

Agent-supported Authority Review SHOULD remain traceable to the agent, model class, instruction, workflow, Source Material, evidence, validation result, relationship context, confidence signal, review state, and human decision where applicable.

Agent-related authority handling MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

An agent MAY recommend approval.

An agent MAY recommend rejection.

An agent MAY recommend limitation, suspension, downgrade, escalation, repair, quarantine, privacy review, source review, relationship review, provenance review, lifecycle review, validation review, publication review, export review, migration review, or downstream-use review.

An agent MUST NOT approve a governed entity by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Agent-supported approval recommendations SHOULD remain clearly distinguishable from approval decisions.

Agent-related authority handling MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

An agent MAY perform validation where a governed validation process permits agent validation.

An agent MAY recommend validation.

An agent MAY flag validation failure.

An agent MAY flag validation uncertainty.

An agent MAY recommend repair.

An agent MUST NOT create validation success by itself unless a governed validation process explicitly defines that behavior within a defined scope.

Agent validation SHOULD remain traceable to the validator, model class, workflow, rule set, validation profile, validation result, validation date, evidence, Source References, provenance, review state, and human decision where applicable.

Agent-related authority handling MUST remain distinguishable from Lifecycle State.

Lifecycle State describes the current governed state of a governed entity.

An agent MAY propose lifecycle-related authority handling.

An agent MAY flag lifecycle-authority conflicts.

An agent MAY recommend lifecycle review, repair, quarantine, deprecation, supersession, archival, restriction, publication review, export review, migration review, or downstream-use review.

An agent MUST NOT create Lifecycle State by itself unless a governed lifecycle process explicitly defines that behavior within a defined scope.

Agent Behavior MUST NOT cause a draft, approved, rejected, deprecated, superseded, archived, restricted, quarantined, repaired, imported, exported, migrated, or published state to be treated as a different authority state unless a governed authority process explicitly defines that behavior within a defined scope.

Agent-related authority handling MUST remain distinguishable from Privacy Classification.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation visibility, or handling expectations.

Agent Behavior MUST preserve privacy boundaries.

Agent Behavior MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, workflow-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, implementation-restricted, migration-restricted, or downstream-use restricted information merely because the information is useful for authority handling.

Agent access to restricted information MUST NOT imply permission to summarize, expose, publish, export, synchronize, index, migrate, route, or use that information downstream.

An agent-readable entity is not automatically agent-modifiable.

An agent-readable entity is not automatically agent-publishable.

An agent-readable entity is not automatically exportable.

An agent-readable entity is not automatically safe for downstream use.

Where Agent Behavior creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Agent-related authority handling MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

Agent Behavior SHOULD preserve provenance where agent activity affects interpretation, governance, authority, validation, approval, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, implementation behavior, import, export, migration, or downstream use.

Agent-generated output SHOULD identify or support identification of the agent, model class, instruction, workflow, source material, evidence, extraction context, transformation context, confidence signal, review state, and human decision where applicable.

Agent Behavior MUST NOT erase human provenance.

Agent Behavior MUST NOT erase source provenance.

Agent Behavior MUST NOT erase workflow provenance.

Agent Behavior MUST NOT erase import, export, or migration provenance.

Agent Behavior MUST NOT replace provenance unless a governed process explicitly defines that behavior within a defined scope.

Agent-related authority handling MUST remain distinguishable from Source References.

A Source Reference is a traceable reference from a governed entity to Source Material.

An agent MAY propose Source References.

An agent MAY check Source References.

An agent MAY summarize Source Material.

An agent MAY classify Source References.

An agent MAY flag missing, incomplete, contradictory, stale, unavailable, restricted, superseded, or incompatible Source References.

An agent MUST NOT create source authority by itself.

An agent MUST NOT make a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity authoritative merely because the agent found, cited, summarized, ranked, or preferred a source.

Agent-generated Source References SHOULD remain traceable to Source Material, extraction context, transformation context, confidence signal, review state, and human decision where applicable.

Agent-related authority handling MUST remain distinguishable from Relationship Authority.

An agent MAY propose relationships.

An agent MAY classify relationships.

An agent MAY summarize relationships.

An agent MAY flag missing, incomplete, contradictory, stale, restricted, invalid, superseded, or incompatible relationships.

An agent MAY recommend relationship review.

An agent MAY recommend relationship repair.

An agent MUST NOT create relationship authority by itself.

Agent-generated relationships MUST NOT become authoritative merely because they were generated, ranked, repeated, inferred, embedded, clustered, recommended, or graph-connected by an agent.

Agent-generated relationships SHOULD remain traceable to Source Material, evidence, relationship context, confidence signal, review state, and human decision where applicable.

Agent-related authority handling MUST remain distinguishable from Workflow Completion.

Workflow Completion describes the successful completion of a workflow step, workflow stage, workflow run, task sequence, automation, routing path, review queue, or operational procedure.

An agent may operate inside a workflow.

A workflow may route agent output for review.

A workflow may require agent output before review.

A workflow may require human review after agent output.

Workflow Completion MUST NOT create Authority Level merely because an agent completed a task.

Agent task completion MUST NOT create Workflow Completion unless a governed workflow explicitly defines that result within a defined scope.

Agent-related authority handling MUST remain distinguishable from Implementation Visibility.

Implementation Visibility describes whether a governed entity is visible, surfaced, indexed, ranked, displayed, searched, cached, routed, filtered, published, synchronized, or exposed by a specific implementation.

Agent visibility MUST NOT create Authority Level.

Agent visibility MUST NOT create approval.

Agent visibility MUST NOT create validation success.

Agent visibility MUST NOT create Lifecycle State.

Agent visibility MUST NOT weaken Privacy Classification.

A governed entity MUST NOT be treated as authoritative merely because an agent can see it, retrieve it, summarize it, rank it, cite it, embed it, cluster it, link it, classify it, or recommend it.

A governed entity MUST NOT lose Authority Level, provenance, Source References, relationships, Lifecycle State, Privacy Classification, validation state, or approval history merely because an agent cannot access it.

Agent-related authority handling SHOULD support agent-activity history.

Agent-activity history SHOULD identify or support identification of:

- prior Authority Level where applicable;
- new or proposed Authority Level where applicable;
- prior Authority Scope where applicable;
- new or proposed Authority Scope where applicable;
- agent activity performed;
- agent or model class where applicable;
- instruction, prompt, workflow, tool, or process used where applicable;
- agent confidence where applicable;
- source material used where applicable;
- Source References used or proposed where applicable;
- relationships used or proposed where applicable;
- provenance created or modified where applicable;
- validation performed or proposed where applicable;
- approval recommended where applicable;
- lifecycle state affected or reviewed where applicable;
- privacy classification affected or reviewed where applicable;
- compatibility constraints reviewed where applicable;
- import, export, migration, publication, workflow, implementation, or downstream-use limits reviewed where applicable;
- human review state where applicable;
- human decision where applicable.

Agent-related authority handling SHOULD support review.

A reviewer SHOULD be able to determine:

- what agent activity occurred;
- what governed entity was affected;
- what Authority Level was read, proposed, supported, limited, challenged, or unaffected;
- what Authority Scope applies;
- what Source References, provenance, relationships, validation results, lifecycle state, privacy classification, approval context, workflow context, or implementation context were involved;
- whether the agent output is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, quarantined, unreviewed, reviewed, rejected, approved, or otherwise governed;
- whether the agent output requires further Authority Review;
- whether the agent output requires Source Reference review, provenance review, relationship review, lifecycle review, privacy review, validation review, approval review, compatibility review, migration review, export review, publication review, workflow review, or implementation review.

Agent-related authority handling SHOULD support validation.

A validator SHOULD be able to determine whether:

- agent-generated authority information is present where required;
- agent-generated authority information is scoped where required;
- agent-generated authority information remains distinguishable from human-approved authority, workflow-approved authority, validation-supported authority, source-supported authority, and governed Authority Level;
- agent-generated authority information remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior;
- agent-generated authority information preserves privacy boundaries;
- agent-generated authority information preserves Source Reference context;
- agent-generated authority information preserves relationship meaning;
- agent-generated authority information preserves provenance context;
- agent-generated authority information remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Agent-related authority handling SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, override, or regenerate agent-related authority information in a way that causes loss of meaning, broken source traceability, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Agent-related authority handling SHOULD support historical preservation.

A governed entity MAY retain historical agent-related authority context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical agent-related authority context does not mean the entity remains current.

Historical agent-related authority context does not mean the entity is approved for future use.

Historical agent-related authority context does not mean the entity is authoritative for future use.

Historical agent-related authority context does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, safe for workflow use, or safe for downstream use.

Historical agent-related authority context SHOULD preserve enough information for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, privacy review, provenance review, lifecycle review, validation review, and evidence review.

Authority and Agent Behavior are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what agent activity occurred, what Authority Level it supported or challenged where applicable, what scope applies, what Source References and provenance supported the agent activity, what confidence signals were present, what limits were applied, whether agent output is current or historical, whether human review or validation is required, whether privacy or lifecycle handling constrains agent use, and whether agent-related authority handling remains meaningful across time and implementation replacement.

## 17. Authority and Workflow Behavior

Authority and Workflow Behavior are related but distinct concepts.

Workflow Behavior describes how a governed workflow may route, create, review, validate, approve, reject, limit, suspend, downgrade, escalate, transfer, preserve, repair, import, export, migrate, publish, archive, restrict, quarantine, synchronize, index, expose, or otherwise process governed entities.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Workflow Behavior MAY support Authority Level.

Workflow Behavior MAY propose Authority Level.

Workflow Behavior MAY route Authority Level for review.

Workflow Behavior MAY support Authority Assignment.

Workflow Behavior MAY support Authority Review.

Workflow Behavior MAY support approval, validation, repair, publication, export, migration, archival, restriction, quarantine, or downstream-use decisions where a governed workflow explicitly defines that behavior within a defined scope.

Workflow Behavior MUST NOT create Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Workflow Completion MUST NOT create Authority Level by itself.

Workflow Completion MUST NOT create approval by itself.

Workflow Completion MUST NOT create validation success by itself.

Workflow Completion MUST NOT override Privacy Classification.

Workflow Completion MUST NOT override Lifecycle State.

Workflow Completion MUST NOT override Object Identity.

Workflow Completion MUST NOT override Source References, provenance, relationships, validation results, authority review requirements, approval requirements, agent review requirements, implementation constraints, publication limits, export limits, migration limits, or downstream-use limits.

A workflow MAY assist with authority-related work, but a workflow MUST NOT become an unreviewable authority where authority affects governed interpretation or use.

Workflow-related authority handling MAY apply to:

- Knowledge Objects;
- Knowledge Records;
- Source References;
- Source Material where applicable;
- provenance records;
- relationships;
- metadata records;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- governed documents;
- decisions;
- other governed entities.

Workflow-related authority handling SHOULD identify or support identification of:

- what governed entity the workflow processed;
- what workflow performed the work where applicable;
- what workflow step, workflow stage, workflow run, task sequence, automation, routing path, review queue, or operational procedure was used where applicable;
- what trigger initiated the workflow where applicable;
- what Authority Level was read, proposed, assigned, reviewed, supported, limited, challenged, preserved, or unaffected where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment occurred or was proposed where applicable;
- what Authority Review occurred or is required where applicable;
- what approval occurred or is required where applicable;
- what validation occurred or is required where applicable;
- what Source References were used where applicable;
- what relationships were used or proposed where applicable;
- what provenance supports the workflow activity where applicable;
- what Lifecycle State applies where applicable;
- what Privacy Classification applies where applicable;
- what Agent Behavior or Agent Confidence affected the workflow where applicable;
- what compatibility constraints apply where applicable;
- what import, export, migration, publication, implementation, or downstream-use limits apply where applicable.

Authority and Workflow Behavior MUST remain distinguishable.

Workflow Behavior may support authority.

Workflow Behavior may propose authority.

Workflow Behavior may challenge authority.

Workflow Behavior may route authority for review.

Workflow Behavior may preserve authority history.

Workflow Behavior does not equal Authority Level.

Authority Level does not equal Workflow Behavior.

A workflow-generated entity is not automatically authoritative.

A workflow-routed entity is not automatically reviewed.

A workflow-reviewed entity is not automatically approved.

A workflow-validated entity is not automatically authoritative.

A workflow-completed entity is not automatically valid.

A workflow-published entity is not automatically authoritative.

A workflow-exported entity is not automatically safe for downstream use.

A workflow-visible entity is not automatically permitted for every workflow use.

Authority in one workflow context MUST NOT imply authority in every workflow context.

Workflow access in one scope MUST NOT imply authority in every scope.

Workflow-related authority handling MUST remain distinguishable from Workflow Completion.

Workflow Completion describes the successful completion of a workflow step, workflow stage, workflow run, task sequence, automation, routing path, review queue, or operational procedure.

Workflow Completion MAY support Authority Level where a governed workflow explicitly defines completion as part of an authority process.

Workflow Completion MAY support Authority Assignment where a governed workflow explicitly defines completion as part of an assignment process.

Workflow Completion MAY support Authority Review where a governed workflow explicitly defines completion as part of a review process.

Workflow Completion MAY support approval where a governed workflow explicitly defines completion as part of an approval process.

Workflow Completion MAY support validation where a governed workflow explicitly defines completion as part of a validation process.

Workflow Completion MUST NOT create Authority Level, Authority Scope, Authority Assignment, Authority Review, approval, validation success, Lifecycle State, Privacy Classification, provenance completeness, Source Reference sufficiency, Relationship Authority, Agent Confidence, Implementation Visibility, publication permission, export permission, migration permission, or downstream-use permission by itself.

Workflow-related authority handling MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Workflow Scope describes the boundary within which a workflow operates.

Workflow Scope may limit Authority Scope handling.

Authority Scope may limit Workflow Behavior.

Workflow routing MUST NOT silently broaden Authority Scope.

Workflow completion MUST NOT silently make authority public, exportable, publishable, searchable, synchronized, indexable, agent-readable, implementation-visible, or downstream-usable.

Workflow execution in one scope MUST NOT make the governed entity authoritative in another scope unless a governed workflow specification explicitly defines that result within a defined scope.

Workflow-related authority handling MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

A workflow MAY propose Authority Assignment.

A workflow MAY route Authority Assignment for review.

A workflow MAY record Authority Assignment where the workflow is governed to perform that role.

A workflow MAY assign, limit, suspend, downgrade, escalate, transfer, preserve, or remove Authority Level only where a governed authority process explicitly defines that behavior within a defined scope.

A workflow MUST NOT assign Authority Level merely because a task, step, queue, automation, checklist, validation, agent action, import process, export process, migration process, publication process, or implementation action completed.

Workflow-supported Authority Assignment SHOULD remain clearly distinguishable from human-approved authority, validation-supported authority, source-supported authority, agent-proposed authority, and governed Authority Level.

Workflow-related authority handling MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

A workflow MAY support Authority Review.

A workflow MAY route a governed entity for Authority Review.

A workflow MAY collect evidence for Authority Review.

A workflow MAY record Authority Review where the workflow is governed to perform that role.

A workflow MAY require human review after workflow completion.

A workflow MAY require agent assistance before review.

A workflow MAY require validation before review.

A workflow MAY require privacy review before review output is exposed.

A workflow MUST NOT satisfy Authority Review by itself unless a governed authority process explicitly defines that behavior within a defined scope.

A workflow MUST NOT become an unreviewable reviewer where authority affects governed interpretation, governance, validation, publication, export, migration, agent behavior, implementation behavior, or downstream use.

Workflow-supported Authority Review SHOULD remain traceable to the workflow, workflow step, workflow stage, workflow run, trigger, task sequence, reviewer, validator, Source Material, evidence, validation result, relationship context, agent involvement, confidence signal where applicable, review state, and human decision where applicable.

Workflow-related authority handling MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

A workflow MAY route a governed entity for approval.

A workflow MAY recommend approval.

A workflow MAY recommend rejection.

A workflow MAY record approval where the workflow is governed to perform that role.

A workflow MAY require additional source review, relationship review, provenance review, lifecycle review, privacy review, validation review, publication review, export review, migration review, agent-output review, implementation review, or downstream-use review before approval.

A workflow MUST NOT approve a governed entity by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Workflow-supported approval recommendations SHOULD remain clearly distinguishable from approval decisions.

Workflow-related authority handling MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

A workflow MAY perform validation where a governed validation process permits workflow validation.

A workflow MAY route validation results for review.

A workflow MAY flag validation failure.

A workflow MAY flag validation uncertainty.

A workflow MAY recommend repair.

A workflow MAY require revalidation after repair, import, export, migration, publication, agent activity, relationship change, source-reference change, provenance change, lifecycle change, privacy change, authority change, or implementation change.

A workflow MUST NOT create validation success by itself unless a governed validation process explicitly defines that behavior within a defined scope.

Workflow validation SHOULD remain traceable to the workflow, validator, rule set, validation profile, validation result, validation date, evidence, Source References, provenance, review state, and human decision where applicable.

Workflow-related authority handling MUST remain distinguishable from Lifecycle State.

Lifecycle State describes the current governed state of a governed entity.

A workflow MAY propose lifecycle-related authority handling.

A workflow MAY route lifecycle-related authority handling.

A workflow MAY flag lifecycle-authority conflicts.

A workflow MAY recommend lifecycle review, repair, quarantine, deprecation, supersession, archival, restriction, publication review, export review, migration review, or downstream-use review.

A workflow MAY change Lifecycle State only where a governed lifecycle process explicitly defines that behavior within a defined scope.

Workflow Completion MUST NOT create Lifecycle State by itself unless a governed lifecycle process explicitly defines that transition within a defined scope.

Workflow Behavior MUST NOT cause a draft, approved, rejected, deprecated, superseded, archived, restricted, quarantined, repaired, imported, exported, migrated, or published state to be treated as a different authority state unless a governed authority process explicitly defines that behavior within a defined scope.

Workflow-related authority handling MUST remain distinguishable from Privacy Classification.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation visibility, or handling expectations.

Workflow Behavior MUST preserve privacy boundaries.

Workflow Behavior MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, workflow-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, implementation-restricted, migration-restricted, or downstream-use restricted information merely because the information is useful for authority handling.

Workflow access to restricted information MUST NOT imply permission to summarize, expose, publish, export, synchronize, index, migrate, route, or use that information downstream.

A workflow-readable entity is not automatically workflow-modifiable.

A workflow-readable entity is not automatically workflow-publishable.

A workflow-readable entity is not automatically exportable.

A workflow-readable entity is not automatically safe for agent use.

A workflow-readable entity is not automatically safe for downstream use.

Where Workflow Behavior creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Workflow-related authority handling MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

Workflow Behavior SHOULD preserve provenance where workflow activity affects interpretation, governance, authority, validation, approval, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, agent behavior, implementation behavior, import, export, migration, or downstream use.

Workflow-generated output SHOULD identify or support identification of the workflow, workflow step, workflow stage, workflow run, trigger, task sequence, source material, evidence, extraction context, transformation context, validation result, review state, approval state, agent involvement, and human decision where applicable.

Workflow Behavior MUST NOT erase human provenance.

Workflow Behavior MUST NOT erase source provenance.

Workflow Behavior MUST NOT erase agent provenance.

Workflow Behavior MUST NOT erase import, export, or migration provenance.

Workflow Behavior MUST NOT replace provenance unless a governed process explicitly defines that behavior within a defined scope.

Workflow-related authority handling MUST remain distinguishable from Source References.

A Source Reference is a traceable reference from a governed entity to Source Material.

A workflow MAY require Source References.

A workflow MAY create Source References where governed to do so.

A workflow MAY route Source References for review.

A workflow MAY check Source References.

A workflow MAY flag missing, incomplete, contradictory, stale, unavailable, restricted, superseded, or incompatible Source References.

A workflow MUST NOT create source authority by itself.

A workflow MUST NOT make a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity authoritative merely because the workflow found, cited, summarized, ranked, preferred, imported, exported, migrated, or routed a source.

Workflow-generated Source References SHOULD remain traceable to Source Material, extraction context, transformation context, validation context, review state, workflow state, and human decision where applicable.

Workflow-related authority handling MUST remain distinguishable from Relationship Authority.

A workflow MAY propose relationships.

A workflow MAY classify relationships.

A workflow MAY route relationships for review.

A workflow MAY validate relationships where a governed validation process permits that behavior.

A workflow MAY flag missing, incomplete, contradictory, stale, restricted, invalid, superseded, or incompatible relationships.

A workflow MAY recommend relationship review.

A workflow MAY recommend relationship repair.

A workflow MUST NOT create relationship authority by itself.

Workflow-generated relationships MUST NOT become authoritative merely because they were generated, routed, repeated, imported, exported, migrated, validated, published, synchronized, or graph-connected by a workflow.

Workflow-generated relationships SHOULD remain traceable to Source Material, evidence, relationship context, validation result, review state, workflow state, agent involvement where applicable, and human decision where applicable.

Workflow-related authority handling MUST remain distinguishable from Agent Behavior.

An agent may operate inside a workflow.

A workflow may route agent output for review.

A workflow may require agent output before review.

A workflow may require human review after agent output.

Agent task completion MUST NOT create Workflow Completion unless a governed workflow explicitly defines that behavior within a defined scope.

Agent output inside a workflow MUST NOT create Authority Level by itself.

Agent Confidence inside a workflow MUST NOT create Authority Level by itself.

Workflow completion that includes agent activity MUST NOT make agent output authoritative unless a governed authority process explicitly defines that behavior within a defined scope.

Workflow-related authority handling MUST remain distinguishable from Implementation Visibility.

Implementation Visibility describes whether a governed entity is visible, surfaced, indexed, ranked, displayed, searched, cached, routed, filtered, published, synchronized, or exposed by a specific implementation.

Workflow visibility MUST NOT create Authority Level.

Workflow visibility MUST NOT create approval.

Workflow visibility MUST NOT create validation success.

Workflow visibility MUST NOT create Lifecycle State.

Workflow visibility MUST NOT weaken Privacy Classification.

A governed entity MUST NOT be treated as authoritative merely because a workflow can see it, retrieve it, route it, validate it, summarize it, rank it, cite it, publish it, export it, migrate it, index it, synchronize it, classify it, or recommend it.

A governed entity MUST NOT lose Authority Level, provenance, Source References, relationships, Lifecycle State, Privacy Classification, validation state, review history, or approval history merely because a workflow cannot access it.

Workflow-related authority handling SHOULD support workflow-activity history.

Workflow-activity history SHOULD identify or support identification of:

- prior Authority Level where applicable;
- new or proposed Authority Level where applicable;
- prior Authority Scope where applicable;
- new or proposed Authority Scope where applicable;
- workflow activity performed;
- workflow name, workflow class, workflow step, workflow stage, workflow run, trigger, routing path, task sequence, or automation where applicable;
- workflow actor where applicable;
- reviewer where applicable;
- validator where applicable;
- approver where applicable;
- agent involvement where applicable;
- source material used where applicable;
- Source References used or proposed where applicable;
- relationships used or proposed where applicable;
- provenance created or modified where applicable;
- validation performed or proposed where applicable;
- approval recommended or recorded where applicable;
- lifecycle state affected or reviewed where applicable;
- privacy classification affected or reviewed where applicable;
- compatibility constraints reviewed where applicable;
- import, export, migration, publication, agent, implementation, or downstream-use limits reviewed where applicable;
- human review state where applicable;
- human decision where applicable.

Workflow-related authority handling SHOULD support review.

A reviewer SHOULD be able to determine:

- what workflow activity occurred;
- what governed entity was affected;
- what Authority Level was read, proposed, assigned, reviewed, supported, limited, challenged, or unaffected;
- what Authority Scope applies;
- what Source References, provenance, relationships, validation results, lifecycle state, privacy classification, approval context, agent context, implementation context, import context, export context, migration context, publication context, or downstream-use context were involved;
- whether the workflow output is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, quarantined, unreviewed, reviewed, rejected, approved, or otherwise governed;
- whether the workflow output requires further Authority Review;
- whether the workflow output requires Source Reference review, provenance review, relationship review, lifecycle review, privacy review, validation review, approval review, compatibility review, migration review, export review, publication review, agent-output review, or implementation review.

Workflow-related authority handling SHOULD support validation.

A validator SHOULD be able to determine whether:

- workflow-generated authority information is present where required;
- workflow-generated authority information is scoped where required;
- workflow-generated authority information remains distinguishable from human-approved authority, validation-supported authority, source-supported authority, agent-proposed authority, and governed Authority Level;
- workflow-generated authority information remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Agent Behavior, Implementation Visibility, storage behavior, and hidden application behavior;
- workflow-generated authority information preserves privacy boundaries;
- workflow-generated authority information preserves Source Reference context;
- workflow-generated authority information preserves relationship meaning;
- workflow-generated authority information preserves provenance context;
- workflow-generated authority information remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Workflow-related authority handling SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, override, or regenerate workflow-related authority information in a way that causes loss of meaning, broken source traceability, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, workflow-state ambiguity, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Workflow-related authority handling SHOULD support historical preservation.

A governed entity MAY retain historical workflow-related authority context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, or replaced.

Historical workflow-related authority context does not mean the entity remains current.

Historical workflow-related authority context does not mean the entity is approved for future use.

Historical workflow-related authority context does not mean the entity is authoritative for future use.

Historical workflow-related authority context does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, safe for workflow use, or safe for downstream use.

Historical workflow-related authority context SHOULD preserve enough information for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, privacy review, provenance review, lifecycle review, validation review, agent-output review, and evidence review.

Authority and Workflow Behavior are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what workflow activity occurred, what Authority Level it supported or challenged where applicable, what scope applies, what Source References and provenance supported the workflow activity, what workflow completion signals were present, what agent activity occurred inside the workflow where applicable, what limits were applied, whether workflow output is current or historical, whether human review or validation is required, whether privacy or lifecycle handling constrains workflow use, and whether workflow-related authority handling remains meaningful across time and implementation replacement.

## 18. Authority and Implementation Behavior

Authority and Implementation Behavior are related but distinct concepts.

Implementation Behavior describes how a software tool, vault, database, file system, interface, plugin, workflow environment, agent system, publication system, search system, graph system, synchronization system, storage system, or other implementation may display, store, index, rank, filter, cache, route, expose, hide, publish, export, import, migrate, synchronize, validate, transform, or otherwise handle governed entities.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Implementation Behavior MAY display Authority Level.

Implementation Behavior MAY route Authority Level for review.

Implementation Behavior MAY support discovery of Authority Level.

Implementation Behavior MAY preserve Authority Level.

Implementation Behavior MAY validate Authority Level where a governed validation process permits that behavior.

Implementation Behavior MAY support import, export, migration, publication, synchronization, indexing, backup, restoration, archival, review, workflow behavior, agent behavior, or downstream use where governed to do so.

Implementation Behavior MUST NOT create Authority Level by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Implementation Behavior MUST NOT define standard-level authority meaning.

Implementation Behavior MUST NOT replace Authority Level.

Authority Level MUST NOT depend on hidden implementation behavior.

A governed entity MUST NOT become authoritative merely because an implementation:

- displays it;
- indexes it;
- ranks it highly;
- surfaces it in search;
- places it in a graph;
- links to it;
- creates backlinks;
- places it in a folder;
- assigns a tag;
- assigns a color;
- assigns an icon;
- pins it;
- stars it;
- recommends it;
- caches it;
- synchronizes it;
- publishes it;
- exports it;
- imports it;
- migrates it;
- routes it through a queue;
- marks it with an implementation-specific label;
- stores it in a database row;
- exposes it through a plugin;
- makes it visible to an agent;
- makes it visible to a workflow;
- makes it frequently used.

A governed entity MUST NOT lose Authority Level merely because an implementation:

- hides it;
- filters it;
- archives it;
- de-indexes it;
- moves it;
- renames it;
- changes its display title;
- changes its folder path;
- changes its visual graph position;
- changes its search ranking;
- changes its tag display;
- changes its database representation;
- changes its plugin state;
- changes its cache state;
- changes its synchronization state;
- fails to display it;
- fails to expose it to an agent;
- fails to expose it to a workflow;
- migrates it into a different representation.

Implementation-related authority handling MAY apply to:

- Knowledge Objects;
- Knowledge Records;
- Source References;
- Source Material where applicable;
- provenance records;
- relationships;
- metadata records;
- validation results;
- workflow outputs;
- agent outputs;
- import records;
- export records;
- migration records;
- governed documents;
- decisions;
- other governed entities.

Implementation-related authority handling SHOULD identify or support identification of:

- what governed entity the implementation handled;
- what implementation handled the entity where applicable;
- what implementation profile, version, plugin, database, storage system, interface, search system, graph system, publication system, synchronization system, or tool behavior applied where applicable;
- what Authority Level was displayed, preserved, transformed, validated, imported, exported, migrated, synchronized, published, hidden, filtered, routed, or otherwise affected where applicable;
- what Authority Scope applies where applicable;
- what Authority Assignment applies where applicable;
- what Authority Review applies or remains required where applicable;
- what approval applies or remains required where applicable;
- what validation applies or remains required where applicable;
- what Source References were preserved, transformed, hidden, exposed, or affected where applicable;
- what relationships were preserved, transformed, hidden, exposed, or affected where applicable;
- what provenance was preserved, transformed, hidden, exposed, or affected where applicable;
- what Lifecycle State applies where applicable;
- what Privacy Classification applies where applicable;
- what Agent Behavior or Workflow Behavior affected implementation handling where applicable;
- what compatibility constraints apply where applicable;
- what import, export, migration, publication, synchronization, indexing, backup, restoration, archival, or downstream-use limits apply where applicable.

Authority and Implementation Behavior MUST remain distinguishable.

Implementation Behavior may support authority handling.

Implementation Behavior may display authority handling.

Implementation Behavior may route authority handling.

Implementation Behavior may preserve authority history.

Implementation Behavior may validate authority representation where governed.

Implementation Behavior does not equal Authority Level.

Authority Level does not equal Implementation Behavior.

An implementation-visible entity is not automatically authoritative.

An implementation-hidden entity is not automatically non-authoritative.

An implementation-indexed entity is not automatically approved.

An implementation-ranked entity is not automatically validated.

An implementation-published entity is not automatically authoritative.

An implementation-exported entity is not automatically safe for downstream use.

An implementation-migrated entity is not automatically authority-preserving unless authority meaning was preserved or the loss was explicitly disclosed.

Authority in one implementation context MUST NOT imply authority in every implementation context.

Implementation visibility in one scope MUST NOT imply authority in every scope.

Implementation-related authority handling MUST remain distinguishable from Implementation Visibility.

Implementation Visibility describes whether a governed entity is visible, surfaced, indexed, ranked, displayed, searched, cached, routed, filtered, published, synchronized, or exposed by a specific implementation.

Implementation Visibility MAY support discovery.

Implementation Visibility MAY support review.

Implementation Visibility MAY support routing.

Implementation Visibility MUST NOT create Authority Level.

Implementation Visibility MUST NOT create Authority Scope.

Implementation Visibility MUST NOT create Authority Assignment.

Implementation Visibility MUST NOT create Authority Review.

Implementation Visibility MUST NOT create approval.

Implementation Visibility MUST NOT create validation success.

Implementation Visibility MUST NOT create Lifecycle State.

Implementation Visibility MUST NOT create Privacy Classification.

Implementation Visibility MUST NOT create provenance completeness.

Implementation Visibility MUST NOT create Source Reference sufficiency.

Implementation Visibility MUST NOT create Relationship Authority.

Implementation Visibility MUST NOT create Agent Confidence.

Implementation Visibility MUST NOT create Workflow Completion.

Implementation-related authority handling MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Implementation Scope describes the boundary of a specific software system, vault, database, file system, interface, plugin, workflow environment, agent system, publication system, search system, graph system, synchronization system, or tool.

Implementation Scope may limit what an implementation can display or preserve.

Implementation Scope MUST NOT silently broaden Authority Scope.

Implementation Scope MUST NOT silently make authority public, exportable, publishable, searchable, synchronized, indexable, agent-readable, workflow-readable, or downstream-usable.

Implementation behavior in one scope MUST NOT make a governed entity authoritative in another scope unless a governed authority process explicitly defines that result within a defined scope.

Implementation-related authority handling MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

An implementation MAY record Authority Assignment where governed to do so.

An implementation MAY display Authority Assignment.

An implementation MAY route Authority Assignment for review.

An implementation MUST NOT assign Authority Level merely because a user interface state, folder path, filename, tag, graph edge, backlink, database row, search ranking, cache state, plugin field, workflow queue, agent task label, import state, export state, migration state, publication state, or synchronization state exists.

Implementation-supported Authority Assignment SHOULD remain clearly distinguishable from human-approved authority, workflow-approved authority, validation-supported authority, source-supported authority, agent-proposed authority, and governed Authority Level.

Implementation-related authority handling MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

An implementation MAY route a governed entity for Authority Review.

An implementation MAY display Authority Review state.

An implementation MAY preserve Authority Review history.

An implementation MAY support evidence collection for Authority Review where governed.

An implementation MUST NOT satisfy Authority Review by itself unless a governed authority process explicitly defines that behavior within a defined scope.

A search result, graph view, dashboard, queue, plugin field, database relation, validation report, publication interface, migration report, export report, or implementation badge MUST NOT be treated as Authority Review unless governed review occurred.

Implementation-related authority handling MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

An implementation MAY display approval.

An implementation MAY route a governed entity for approval.

An implementation MAY preserve approval history.

An implementation MAY restrict display, export, publication, synchronization, indexing, workflow access, agent access, or downstream use based on approval state where governed.

An implementation MUST NOT approve a governed entity by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Implementation-supported approval indicators SHOULD remain clearly distinguishable from approval decisions.

Implementation-related authority handling MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

An implementation MAY perform validation where a governed validation process permits implementation validation.

An implementation MAY display validation results.

An implementation MAY route validation failures for repair or review.

An implementation MAY prevent publication, export, migration, synchronization, indexing, workflow routing, agent access, or downstream use where validation failure requires restriction.

An implementation MUST NOT create validation success by itself unless a governed validation process explicitly defines that behavior within a defined scope.

Implementation validation SHOULD remain traceable to the implementation, version, rule set, validation profile, validation result, validation date, evidence, Source References, provenance, review state, and human decision where applicable.

Implementation-related authority handling MUST remain distinguishable from Lifecycle State.

Lifecycle State describes the current governed state of a governed entity.

An implementation MAY display Lifecycle State.

An implementation MAY route lifecycle-related authority handling.

An implementation MAY preserve lifecycle history.

An implementation MAY support lifecycle transitions where a governed lifecycle process permits implementation-supported transitions.

Implementation Behavior MUST NOT create Lifecycle State by itself unless a governed lifecycle process explicitly defines that transition within a defined scope.

Implementation folder placement, archive state, trash state, pinned state, hidden state, publication state, synchronization state, cache state, plugin state, database state, or graph position MUST NOT be treated as Lifecycle State unless governed lifecycle rules explicitly define that behavior.

Implementation-related authority handling MUST remain distinguishable from Privacy Classification.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation visibility, or handling expectations.

Implementation Behavior MUST preserve privacy boundaries.

Implementation Behavior MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, workflow-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, implementation-restricted, migration-restricted, or downstream-use restricted information merely because the implementation can display, index, search, rank, summarize, route, publish, export, synchronize, or migrate that information.

Implementation access to restricted information MUST NOT imply permission to summarize, expose, publish, export, synchronize, index, migrate, route, or use that information downstream.

An implementation-visible entity is not automatically public.

An implementation-readable entity is not automatically implementation-modifiable.

An implementation-readable entity is not automatically publishable.

An implementation-readable entity is not automatically exportable.

An implementation-readable entity is not automatically safe for agent use.

An implementation-readable entity is not automatically safe for downstream use.

Where Implementation Behavior creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Implementation-related authority handling MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

Implementation Behavior SHOULD preserve provenance where implementation activity affects interpretation, governance, authority, validation, approval, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, agent behavior, import, export, migration, synchronization, indexing, backup, restoration, archival, or downstream use.

Implementation-generated output SHOULD identify or support identification of the implementation, implementation version, implementation profile, plugin, database, storage system, interface, search system, graph system, publication system, synchronization system, transformation context, validation result, review state, approval state, workflow involvement, agent involvement, and human decision where applicable.

Implementation Behavior MUST NOT erase human provenance.

Implementation Behavior MUST NOT erase source provenance.

Implementation Behavior MUST NOT erase agent provenance.

Implementation Behavior MUST NOT erase workflow provenance.

Implementation Behavior MUST NOT erase import, export, or migration provenance.

Implementation Behavior MUST NOT replace provenance unless a governed process explicitly defines that behavior within a defined scope.

Implementation-related authority handling MUST remain distinguishable from Source References.

A Source Reference is a traceable reference from a governed entity to Source Material.

An implementation MAY display Source References.

An implementation MAY hide Source References from unauthorized actors.

An implementation MAY route Source References for review.

An implementation MAY validate Source References where governed.

An implementation MAY preserve Source References across import, export, migration, synchronization, backup, restoration, archival, and publication where permitted.

An implementation MUST NOT create source authority by itself.

An implementation MUST NOT make a Knowledge Object, Knowledge Record, relationship, decision, workflow output, agent output, import record, export record, migration record, or other governed entity authoritative merely because the implementation displays, ranks, cites, stores, imports, exports, migrates, synchronizes, or links a source.

Implementation-preserved Source References SHOULD remain traceable to Source Material, extraction context, transformation context, validation context, review state, implementation state, workflow state, agent involvement where applicable, and human decision where applicable.

Implementation-related authority handling MUST remain distinguishable from Relationship Authority.

An implementation MAY display relationships.

An implementation MAY create implementation-specific links for navigation.

An implementation MAY show backlinks, graph edges, database relations, search associations, folder associations, tag associations, vector similarities, embedding relationships, clusters, recommendations, or visual connections.

An implementation MAY preserve governed relationships.

An implementation MAY route governed relationships for review.

An implementation MAY validate governed relationships where a governed validation process permits that behavior.

Implementation-specific links MUST NOT become governed relationships merely because an implementation displays them.

Graph position MUST NOT create Relationship Authority.

Backlink count MUST NOT create Relationship Authority.

Search association MUST NOT create Relationship Authority.

Vector similarity MUST NOT create Relationship Authority.

Folder proximity MUST NOT create Relationship Authority.

Tag similarity MUST NOT create Relationship Authority.

Implementation-generated relationships MUST NOT become authoritative merely because they were generated, displayed, ranked, repeated, imported, exported, migrated, synchronized, cached, or graph-connected by an implementation.

Implementation-related authority handling MUST remain distinguishable from Agent Behavior.

An agent may operate inside an implementation.

An implementation may expose content to an agent.

An implementation may restrict content from an agent.

An implementation may route agent output for review.

Implementation access MUST NOT make agent output authoritative.

Agent visibility inside an implementation MUST NOT create Authority Level.

Agent Confidence displayed by an implementation MUST NOT create Authority Level.

Implementation-generated summaries of agent output MUST NOT create Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Implementation-related authority handling MUST remain distinguishable from Workflow Behavior.

A workflow may operate inside an implementation.

An implementation may route workflow output for review.

An implementation may display workflow state.

An implementation may preserve workflow history.

Workflow Completion displayed by an implementation MUST NOT create Authority Level by itself.

Implementation display of workflow completion MUST NOT create approval, validation success, privacy clearance, publication readiness, export permission, migration permission, or downstream-use permission unless a governed workflow explicitly defines that behavior within a defined scope.

Implementation-related authority handling SHOULD support implementation-activity history.

Implementation-activity history SHOULD identify or support identification of:

- prior Authority Level where applicable;
- new or proposed Authority Level where applicable;
- prior Authority Scope where applicable;
- new or proposed Authority Scope where applicable;
- implementation activity performed;
- implementation name, implementation class, implementation profile, version, plugin, database, storage system, interface, search system, graph system, publication system, synchronization system, or tool where applicable;
- implementation actor where applicable;
- workflow involvement where applicable;
- agent involvement where applicable;
- source material used where applicable;
- Source References used, displayed, transformed, hidden, or preserved where applicable;
- relationships used, displayed, transformed, hidden, or preserved where applicable;
- provenance created, modified, transformed, hidden, or preserved where applicable;
- validation performed or displayed where applicable;
- approval displayed or recorded where applicable;
- lifecycle state displayed or affected where applicable;
- privacy classification displayed or enforced where applicable;
- compatibility constraints reviewed where applicable;
- import, export, migration, publication, synchronization, indexing, backup, restoration, archival, agent, workflow, or downstream-use limits reviewed where applicable;
- human review state where applicable;
- human decision where applicable.

Implementation-related authority handling SHOULD support review.

A reviewer SHOULD be able to determine:

- what implementation activity occurred;
- what governed entity was affected;
- what Authority Level was displayed, preserved, transformed, hidden, routed, validated, imported, exported, migrated, synchronized, published, or otherwise affected;
- what Authority Scope applies;
- what Source References, provenance, relationships, validation results, lifecycle state, privacy classification, approval context, agent context, workflow context, import context, export context, migration context, publication context, synchronization context, or downstream-use context were involved;
- whether the implementation output is current, historical, provisional, restricted, limited, suspended, deprecated, superseded, archived, repaired, quarantined, unreviewed, reviewed, rejected, approved, or otherwise governed;
- whether the implementation output requires further Authority Review;
- whether the implementation output requires Source Reference review, provenance review, relationship review, lifecycle review, privacy review, validation review, approval review, compatibility review, migration review, export review, publication review, agent-output review, or workflow review.

Implementation-related authority handling SHOULD support validation.

A validator SHOULD be able to determine whether:

- implementation-related authority information is present where required;
- implementation-related authority information is scoped where required;
- implementation-related authority information remains distinguishable from human-approved authority, workflow-approved authority, validation-supported authority, source-supported authority, agent-proposed authority, implementation display, and governed Authority Level;
- implementation-related authority information remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Agent Behavior, Workflow Completion, Workflow Behavior, storage behavior, and hidden application behavior;
- implementation-related authority information preserves privacy boundaries;
- implementation-related authority information preserves Source Reference context;
- implementation-related authority information preserves relationship meaning;
- implementation-related authority information preserves provenance context;
- implementation-related authority information remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Implementation-related authority handling SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, override, or regenerate implementation-related authority information in a way that causes loss of meaning, broken source traceability, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, workflow-state ambiguity, agent-state ambiguity, implementation-state ambiguity, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Implementation-related authority handling SHOULD support historical preservation.

A governed entity MAY retain historical implementation-related authority context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, synchronized, published, restored, or replaced.

Historical implementation-related authority context does not mean the entity remains current.

Historical implementation-related authority context does not mean the entity is approved for future use.

Historical implementation-related authority context does not mean the entity is authoritative for future use.

Historical implementation-related authority context does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, safe for workflow use, or safe for downstream use.

Historical implementation-related authority context SHOULD preserve enough information for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, privacy review, provenance review, lifecycle review, validation review, workflow review, agent-output review, and evidence review.

Authority and Implementation Behavior are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what implementation activity occurred, what Authority Level it displayed, preserved, transformed, routed, or challenged where applicable, what scope applies, what Source References and provenance supported the implementation activity, what implementation visibility signals were present, what agent or workflow activity occurred inside the implementation where applicable, what limits were applied, whether implementation output is current or historical, whether human review or validation is required, whether privacy or lifecycle handling constrains implementation use, and whether implementation-related authority handling remains meaningful across time and implementation replacement.
## 19. Authority and Import, Export, and Migration

Authority and Import, Export, and Migration are related but distinct concepts.

Import describes the process of bringing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, Source References, provenance, validation results, lifecycle state, authority information, privacy information, workflow outputs, agent outputs, or external content into a compliant environment.

Export describes the process of producing Knowledge Objects, Knowledge Records, Source Material, metadata, identifiers, relationships, Source References, provenance, validation results, lifecycle state, authority information, privacy information, workflow outputs, agent outputs, or external content from a compliant environment for use elsewhere.

Migration describes movement from one storage system, implementation, representation, schema, vault, repository, database, file format, workflow environment, agent environment, validation environment, or tool environment to another.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

Import, Export, and Migration MAY preserve Authority Level.

Import, Export, and Migration MAY limit Authority Level.

Import, Export, and Migration MAY suspend Authority Level.

Import, Export, and Migration MAY require Authority Review.

Import, Export, and Migration MAY require validation.

Import, Export, and Migration MAY require privacy review.

Import, Export, and Migration MAY require provenance review.

Import, Export, and Migration MAY require Source Reference review.

Import, Export, and Migration MAY require relationship review.

Import, Export, and Migration MAY preserve historical authority context.

Import, Export, and Migration MUST NOT create Authority Level by themselves unless a governed authority process explicitly defines that behavior within a defined scope.

Import, Export, and Migration MUST NOT silently upgrade Authority Level.

Import, Export, and Migration MUST NOT silently downgrade Authority Level.

Import, Export, and Migration MUST NOT silently remove Authority Level.

Import, Export, and Migration MUST NOT silently broaden Authority Scope.

Import, Export, and Migration MUST NOT silently transfer Authority Level from one governed entity to another.

Import, Export, and Migration MUST NOT silently make restricted authority public, exportable, publishable, searchable, synchronized, agent-readable, workflow-readable, implementation-visible, or downstream-usable.

A governed entity may be:

- imported with preserved authority;
- imported with provisional authority;
- imported with suspended authority pending review;
- imported with authority limited to historical interpretation;
- imported with authority rejected for current use;
- exported with authority preserved;
- exported with authority redacted;
- exported with authority limited by Privacy Classification;
- exported with authority limited by Source Reference restrictions;
- exported with authority limited by provenance restrictions;
- migrated with authority preserved;
- migrated with authority mapped;
- migrated with authority requiring validation;
- migrated with authority requiring review;
- migrated with authority treated as historical until confirmed;
- migrated with authority loss explicitly disclosed.

Authority-related import, export, and migration handling SHOULD identify or support identification of:

- what governed entity was imported, exported, or migrated;
- what source environment was used where applicable;
- what destination environment was used where applicable;
- what representation, format, schema, storage system, vault, repository, database, workflow environment, agent environment, validation environment, publication environment, or implementation was involved where applicable;
- what Authority Level existed before import, export, or migration where applicable;
- what Authority Level exists after import, export, or migration where applicable;
- what Authority Scope existed before import, export, or migration where applicable;
- what Authority Scope exists after import, export, or migration where applicable;
- what Authority Assignment occurred where applicable;
- what Authority Review occurred or remains required where applicable;
- what approval occurred or remains required where applicable;
- what validation occurred or remains required where applicable;
- what Source References were preserved, transformed, redacted, restricted, lost, or require review where applicable;
- what relationships were preserved, transformed, redacted, restricted, lost, or require review where applicable;
- what provenance was preserved, transformed, redacted, restricted, lost, or requires review where applicable;
- what Lifecycle State applies where applicable;
- what Privacy Classification applies where applicable;
- what Agent Behavior, Workflow Behavior, or Implementation Behavior affected the import, export, or migration where applicable;
- what compatibility constraints apply where applicable;
- what publication, synchronization, indexing, backup, restoration, archival, or downstream-use limits apply where applicable.

Authority and Import, Export, and Migration MUST remain distinguishable.

Import does not equal Authority Level.

Export does not equal Authority Level.

Migration does not equal Authority Level.

Authority Level does not equal import status.

Authority Level does not equal export status.

Authority Level does not equal migration status.

An imported entity is not automatically authoritative.

An exported entity is not automatically safe for downstream use.

A migrated entity is not automatically authority-preserving.

A successfully migrated entity is not automatically approved.

A successfully exported entity is not automatically public.

A successfully imported entity is not automatically valid.

A compatible file format does not automatically preserve authority meaning.

A preserved field does not automatically preserve authority meaning.

A mapped field does not automatically preserve authority meaning.

Authority in one environment MUST NOT imply authority in every environment.

Authority in one representation MUST NOT imply authority in every representation.

Authority in one migration context MUST NOT imply authority in every migration context.

Authority-related import, export, and migration handling MUST remain distinguishable from Authority Scope.

Authority Scope describes where Authority Level applies.

Import Scope describes the boundary within which imported authority may be trusted, reviewed, limited, suspended, mapped, or treated as provisional.

Export Scope describes the boundary within which authority may be carried out of a compliant environment.

Migration Scope describes the boundary within which authority remains meaningful after movement, conversion, mapping, transformation, validation, or implementation replacement.

Import Scope, Export Scope, and Migration Scope MAY limit Authority Scope.

Import Scope, Export Scope, and Migration Scope MUST NOT silently broaden Authority Scope.

Import Scope, Export Scope, and Migration Scope MUST NOT silently make authority universal.

Authority-related import, export, and migration handling MUST remain distinguishable from Authority Assignment.

Authority Assignment changes or records Authority Level.

Import, Export, and Migration MAY preserve Authority Assignment.

Import, Export, and Migration MAY map Authority Assignment.

Import, Export, and Migration MAY flag Authority Assignment for review.

Import, Export, and Migration MAY require new Authority Assignment where prior authority cannot be trusted, preserved, validated, or interpreted.

Import, Export, and Migration MUST NOT assign Authority Level merely because data moved successfully.

Import, Export, and Migration MUST NOT assign Authority Level merely because a field, tag, folder path, database row, graph edge, backlink, plugin field, status label, export package, import package, migration report, or implementation-specific marker exists.

Authority-related import, export, and migration handling MUST remain distinguishable from Authority Review.

Authority Review evaluates whether Authority Level, Authority Scope, Authority Assignment, authority category, authority limitation, authority suspension, authority downgrade, authority escalation, authority transfer, authority preservation, or authority removal is appropriate.

Import, Export, and Migration MAY trigger Authority Review.

Import, Export, and Migration MAY require Authority Review before prior authority is treated as current, active, publishable, exportable, agent-usable, workflow-usable, implementation-visible, or safe for downstream use.

Import, Export, and Migration MUST NOT satisfy Authority Review by themselves unless a governed authority process explicitly defines that behavior within a defined scope.

A successful import report, export report, migration report, checksum, file conversion, database transfer, synchronization event, backup restoration, or implementation transfer MUST NOT be treated as Authority Review unless governed review occurred.

Authority-related import, export, and migration handling MUST remain distinguishable from Approval.

Approval is formal acceptance of a governed entity for use within a defined scope.

Import, Export, and Migration MAY preserve approval context.

Import, Export, and Migration MAY limit approval context.

Import, Export, and Migration MAY require approval review.

Import, Export, and Migration MUST NOT create approval merely because movement, conversion, mapping, packaging, synchronization, backup, restoration, or implementation replacement succeeded.

Approval in the source environment MUST NOT automatically become approval in the destination environment unless a governed approval process explicitly defines that behavior within a defined scope.

Authority-related import, export, and migration handling MUST remain distinguishable from Validation State.

Validation State describes whether a governed entity satisfies applicable structural, metadata, identity, provenance, relationship, lifecycle, authority, privacy, compatibility, source-reference, workflow, agent, implementation, import, export, or migration expectations.

Import, Export, and Migration SHOULD support validation.

Validation SHOULD determine whether Authority Level, Authority Scope, Authority Assignment, Authority Review, approval, Source References, relationships, provenance, Lifecycle State, Privacy Classification, compatibility context, workflow context, agent context, implementation context, and downstream-use limits were preserved, transformed, redacted, mapped, restricted, lost, or made ambiguous.

Validation success MUST NOT create Authority Level by itself.

Validation success MUST NOT create approval by itself.

Validation success MUST NOT make migrated authority current unless a governed authority process explicitly defines that behavior within a defined scope.

Authority-related import, export, and migration handling MUST remain distinguishable from Object Identity.

Import, Export, and Migration MUST preserve Object Identity where applicable.

Moving a governed entity between systems MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity during import, export, or migration unless a separate governed identity decision determines that the object has become meaningfully different.

If Object Identity cannot be preserved, the limitation MUST be explicit where identity affects authority, provenance, relationships, lifecycle state, Source References, validation, compatibility, publication, or downstream use.

Authority-related import, export, and migration handling MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether authority may be imported, exported, migrated, published, archived, restricted, quarantined, repaired, validated, reviewed, preserved, suspended, or used downstream.

Import, Export, and Migration MAY affect Lifecycle State where a governed lifecycle process explicitly defines that behavior.

Import, Export, and Migration MUST NOT create Lifecycle State by themselves unless a governed lifecycle process explicitly defines that transition within a defined scope.

A migrated entity may retain lifecycle history.

An exported entity may retain lifecycle limits.

An imported entity may require lifecycle review.

A restored entity may require lifecycle validation before authority is restored.

Authority-related import, export, and migration handling MUST remain distinguishable from Privacy Classification.

Privacy Classification describes permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation visibility, or handling expectations.

Import, Export, and Migration MUST preserve privacy boundaries.

Import, Export, and Migration MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, workflow-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, implementation-restricted, migration-restricted, or downstream-use restricted information merely because the information is useful for authority handling.

An exportable entity is not automatically public.

A migratable entity is not automatically publishable.

An importable entity is not automatically safe for agent use.

A backup-restored entity is not automatically safe for downstream use.

Where import, export, or migration creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority-related import, export, and migration handling MUST remain distinguishable from Provenance.

Provenance describes origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.

Import, Export, and Migration SHOULD preserve provenance where authority interpretation depends on origin, source, review, validation, workflow activity, agent activity, implementation behavior, import context, export context, migration context, transformation context, or compatibility context.

Import, Export, and Migration MUST NOT erase human provenance.

Import, Export, and Migration MUST NOT erase source provenance.

Import, Export, and Migration MUST NOT erase workflow provenance.

Import, Export, and Migration MUST NOT erase agent provenance.

Import, Export, and Migration MUST NOT erase prior import, export, or migration provenance where that provenance affects authority interpretation or compatibility.

Authority-related import, export, and migration handling MUST remain distinguishable from Source References.

A Source Reference is a traceable reference from a governed entity to Source Material.

Import, Export, and Migration SHOULD preserve Source References where Source References support, limit, explain, challenge, or preserve authority.

If Source References cannot be preserved, the limitation SHOULD be explicit where source traceability affects authority, validation, provenance, privacy, publication, export, migration, compatibility, or downstream use.

A source-referenced entity MUST NOT become authoritative merely because its Source References were imported, exported, migrated, converted, mapped, synchronized, restored, or displayed.

Authority-related import, export, and migration handling MUST remain distinguishable from Relationship Authority.

Import, Export, and Migration SHOULD preserve relationships where relationships support, limit, explain, challenge, transfer, preserve, or contextualize authority.

If relationships cannot be preserved, the limitation SHOULD be explicit where relationship meaning affects authority, validation, provenance, privacy, publication, export, migration, compatibility, or downstream use.

A relationship MUST NOT become authoritative merely because it was imported, exported, migrated, converted, mapped, synchronized, restored, displayed, or graph-connected.

Authority-related import, export, and migration handling MUST remain distinguishable from Agent Behavior.

An agent MAY assist with import, export, or migration.

An agent MAY map authority fields.

An agent MAY flag authority loss.

An agent MAY flag privacy risk.

An agent MAY flag source-reference loss.

An agent MAY flag provenance loss.

An agent MAY flag relationship loss.

An agent MAY recommend review, validation, repair, limitation, suspension, downgrade, escalation, rejection, approval review, source review, relationship review, provenance review, lifecycle review, privacy review, publication review, export review, migration review, workflow review, or implementation review.

Agent activity during import, export, or migration MUST NOT create Authority Level by itself.

Agent Confidence during import, export, or migration MUST NOT create Authority Level by itself.

Authority-related import, export, and migration handling MUST remain distinguishable from Workflow Behavior.

A workflow MAY assist with import, export, or migration.

A workflow MAY route imported, exported, or migrated entities for review.

A workflow MAY perform validation where governed to do so.

A workflow MAY preserve import, export, or migration provenance.

A workflow MAY restrict import, export, or migration where privacy, lifecycle, validation, authority, relationship, Source Reference, provenance, compatibility, publication, or downstream-use requirements are not satisfied.

Workflow Completion during import, export, or migration MUST NOT create Authority Level by itself.

Workflow Completion during import, export, or migration MUST NOT create approval, validation success, privacy clearance, publication permission, export permission, migration permission, or downstream-use permission unless a governed workflow explicitly defines that behavior within a defined scope.

Authority-related import, export, and migration handling MUST remain distinguishable from Implementation Behavior.

An implementation MAY perform import, export, or migration.

An implementation MAY preserve authority information.

An implementation MAY map authority information.

An implementation MAY display import, export, or migration status.

An implementation MAY generate import, export, or migration reports.

An implementation MUST NOT define Authority Level merely because it stores, displays, maps, converts, packages, exports, imports, migrates, synchronizes, restores, indexes, ranks, or routes a governed entity.

Implementation-specific labels, fields, statuses, folders, graph positions, search rankings, plugin states, database rows, export packages, import packages, migration reports, backup states, or synchronization states MUST NOT replace standard-level authority meaning.

Authority-related import, export, and migration handling SHOULD support import-export-migration history.

Import-export-migration history SHOULD identify or support identification of:

- prior Authority Level where applicable;
- new or mapped Authority Level where applicable;
- prior Authority Scope where applicable;
- new or mapped Authority Scope where applicable;
- import activity where applicable;
- export activity where applicable;
- migration activity where applicable;
- source environment where applicable;
- destination environment where applicable;
- representation, schema, format, tool, implementation, vault, repository, database, workflow environment, agent environment, validation environment, or storage system used where applicable;
- mapping rules used where applicable;
- transformation performed where applicable;
- authority loss where applicable;
- authority ambiguity where applicable;
- Source Reference preservation or loss where applicable;
- relationship preservation or loss where applicable;
- provenance preservation or loss where applicable;
- validation performed or required where applicable;
- approval preserved or required where applicable;
- lifecycle state preserved or affected where applicable;
- privacy classification preserved or enforced where applicable;
- compatibility constraints reviewed where applicable;
- publication, synchronization, indexing, backup, restoration, archival, agent, workflow, implementation, or downstream-use limits reviewed where applicable;
- human review state where applicable;
- human decision where applicable.

Authority-related import, export, and migration handling SHOULD support review.

A reviewer SHOULD be able to determine:

- what import, export, or migration activity occurred;
- what governed entity was affected;
- what Authority Level existed before the activity;
- what Authority Level exists after the activity;
- what Authority Scope applies;
- whether authority was preserved, mapped, limited, suspended, downgraded, escalated, transferred, rejected, redacted, lost, or made provisional;
- what Source References, provenance, relationships, validation results, Lifecycle State, Privacy Classification, approval context, agent context, workflow context, implementation context, publication context, synchronization context, or downstream-use context were involved;
- whether the imported, exported, or migrated entity requires further Authority Review;
- whether the imported, exported, or migrated entity requires Source Reference review, provenance review, relationship review, lifecycle review, privacy review, validation review, approval review, compatibility review, publication review, agent-output review, workflow review, or implementation review.

Authority-related import, export, and migration handling SHOULD support validation.

A validator SHOULD be able to determine whether:

- authority information is present where required;
- authority information is scoped where required;
- authority information was preserved, transformed, redacted, restricted, mapped, suspended, lost, or made ambiguous;
- authority information remains distinguishable from Object Identity, Authority Level, Authority Scope, Authority Assignment, Authority Review, Approval, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Agent Behavior, Workflow Completion, Workflow Behavior, Implementation Visibility, Implementation Behavior, storage behavior, and hidden application behavior;
- authority information preserves privacy boundaries;
- authority information preserves Source Reference context;
- authority information preserves relationship meaning;
- authority information preserves provenance context;
- authority information remains compatible across import, export, migration, backup, restoration, synchronization, publication, archival, and implementation replacement.

Authority-related import, export, and migration handling SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, override, or regenerate import-related, export-related, or migration-related authority information in a way that causes loss of meaning, broken source traceability, broken provenance, authority ambiguity, privacy exposure, validation failure, relationship failure, source-reference failure, workflow-state ambiguity, agent-state ambiguity, implementation-state ambiguity, compatibility loss, publication error, import ambiguity, export ambiguity, migration loss, governance drift, or implementation lock-in.

Authority-related import, export, and migration handling SHOULD support historical preservation.

A governed entity MAY retain historical import-related, export-related, or migration-related authority context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, synchronized, published, restored, or replaced.

Historical import-related, export-related, or migration-related authority context does not mean the entity remains current.

Historical import-related, export-related, or migration-related authority context does not mean the entity is approved for future use.

Historical import-related, export-related, or migration-related authority context does not mean the entity is authoritative for future use.

Historical import-related, export-related, or migration-related authority context does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, safe for workflow use, or safe for downstream use.

Historical import-related, export-related, or migration-related authority context SHOULD preserve enough information for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, privacy review, provenance review, lifecycle review, validation review, workflow review, agent-output review, implementation review, and evidence review.

Authority and Import, Export, and Migration are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine what import, export, or migration activity occurred, what Authority Level was preserved, transformed, mapped, limited, suspended, redacted, lost, or challenged where applicable, what scope applies, what Source References and provenance supported authority preservation, what relationships and lifecycle states affected authority, what privacy limits were applied, whether imported, exported, or migrated authority is current or historical, whether human review or validation is required, whether publication or downstream use is permitted, and whether import-related, export-related, and migration-related authority handling remains meaningful across time and implementation replacement.

## 20. Authority Level Conformance and Success Criteria

Authority Level Conformance defines whether a governed entity, workflow, agent, validator, storage system, import process, export process, migration process, publication process, implementation, specification, or operational practice satisfies the requirements of KS-0007 within a defined scope.

Authority Level Success Criteria define when Authority Level behavior has fulfilled its purpose within The Brain Standard.

KS-0007 is successful when Authority Level remains:

- explicit;
- scoped;
- interpretable;
- portable;
- traceable;
- reviewable;
- privacy-respecting;
- provenance-preserving;
- validatable;
- compatible;
- governable;
- implementation-independent.

Conformance to KS-0007 MUST be scoped.

A conformance claim for one entity MUST NOT imply conformance for every entity.

A conformance claim for one workflow MUST NOT imply conformance for every workflow.

A conformance claim for one agent MUST NOT imply conformance for every agent.

A conformance claim for one implementation MUST NOT imply conformance for every implementation.

A conformance claim for one import, export, migration, publication, synchronization, backup, restoration, archival, validation, or downstream-use context MUST NOT imply conformance for every context.

A partial-conformance claim MUST NOT imply full KS-0007 conformance.

A structural conformance claim MUST NOT imply authority conformance unless authority behavior was evaluated.

A metadata conformance claim MUST NOT imply authority conformance unless Authority Level, Authority Scope, Authority Assignment, Authority Review, authority history, authority preservation, authority privacy behavior, authority provenance behavior, and authority compatibility behavior were evaluated where applicable.

Authority Level Conformance SHOULD identify or support identification of:

- what entity, process, workflow, agent, validator, storage system, import process, export process, migration process, publication process, implementation, specification, or operational practice was evaluated;
- what KS-0007 scope was evaluated;
- what Authority Level requirements applied;
- what Authority Scope requirements applied;
- what Authority Assignment requirements applied;
- what Authority Review requirements applied;
- what approval requirements applied where applicable;
- what validation requirements applied where applicable;
- what provenance requirements applied where applicable;
- what Source Reference requirements applied where applicable;
- what relationship requirements applied where applicable;
- what Lifecycle State requirements applied where applicable;
- what Privacy Classification requirements applied where applicable;
- what Agent Behavior requirements applied where applicable;
- what Workflow Behavior requirements applied where applicable;
- what Implementation Behavior requirements applied where applicable;
- what import, export, migration, publication, synchronization, backup, restoration, archival, or downstream-use requirements applied where applicable;
- what passed;
- what failed;
- what was partial;
- what was blocked;
- what was deferred;
- what was restricted;
- what was not evaluated;
- what evidence supported the conformance result;
- what review occurred;
- what repair remains required;
- what downstream-use limits remain.

Authority Level Conformance MUST remain distinguishable from Authority Level.

Conformance describes whether KS-0007 requirements were satisfied.

Authority Level describes the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.

A conformant authority record is not automatically high-authority.

A nonconformant authority record may still preserve historical authority context.

A conformance-passing entity is not automatically approved for every use.

A conformance-passing entity is not automatically public.

A conformance-passing entity is not automatically exportable, migratable, publishable, agent-usable, workflow-usable, implementation-visible, or safe for downstream use.

Conformance MUST remain distinguishable from Authority Scope.

A conformance result applies only within the evaluated scope.

A conformance result in one scope MUST NOT silently broaden Authority Scope.

A conformance result in one scope MUST NOT silently create authority in another scope.

Authority Level Conformance MUST remain distinguishable from Authority Assignment.

A conformance result MAY support Authority Assignment where a governed authority process explicitly defines that behavior within a defined scope.

A conformance result MUST NOT assign Authority Level by itself.

A conformance result MUST NOT silently upgrade, downgrade, transfer, inherit, suspend, remove, or preserve Authority Level unless a governed authority process explicitly defines that behavior within a defined scope.

Authority Level Conformance MUST remain distinguishable from Authority Review.

A conformance result MAY support Authority Review.

A conformance result MAY trigger Authority Review.

A conformance result MAY show that Authority Review is incomplete.

A conformance result MUST NOT satisfy Authority Review by itself unless a governed authority process explicitly defines that behavior within a defined scope.

Authority Level Conformance MUST remain distinguishable from Approval.

A conformance result MAY support approval.

A conformance result MAY trigger approval review.

A conformance result MAY limit approval.

A conformance result MUST NOT create approval by itself unless a governed approval process explicitly defines that behavior within a defined scope.

Authority Level Conformance MUST remain distinguishable from Validation State.

Validation may determine whether KS-0007 conformance requirements are satisfied.

Validation success MAY support conformance.

Conformance success MAY support validation where a governed validation process explicitly defines that behavior within a defined scope.

Validation success MUST NOT create Authority Level by itself.

Conformance success MUST NOT create Authority Level by itself.

Authority Level Conformance MUST remain distinguishable from Object Identity.

A conformance result MUST NOT create, remove, merge, split, replace, redirect, or reinterpret Object Identity by itself.

A Knowledge Object SHOULD retain the same Object Identity when its authority conformance state changes unless a separate governed identity decision determines that the object has become meaningfully different.

Authority Level Conformance MUST remain distinguishable from Lifecycle State.

Lifecycle State may affect whether conformance is required, current, stale, failed, pending, limited, suspended, deprecated, superseded, archived, restricted, quarantined, repaired, published, exported, migrated, or applicable downstream.

A conformance-passing entity may still be draft.

A conformance-passing entity may still be deprecated.

A conformance-passing entity may still be superseded.

A conformance-passing entity may still be archived.

A conformance-passing entity may still be restricted.

A conformance-failing entity may still be preserved for historical interpretation, audit, compatibility review, migration analysis, or repair.

Authority Level Conformance MUST remain distinguishable from Privacy Classification.

Conformance evaluation MUST preserve privacy boundaries.

A conformance result MUST NOT expose restricted, confidential, sensitive, private, non-exportable, agent-restricted, workflow-restricted, publication-restricted, source-restricted, provenance-restricted, relationship-restricted, implementation-restricted, migration-restricted, or downstream-use restricted information merely to make conformance easier.

A conformance-passing entity may remain private.

A conformance-passing entity may remain restricted.

A conformance-passing entity may remain non-exportable.

A conformance-passing entity may remain publication-restricted.

Where conformance evaluation creates privacy risk, Privacy Classification SHALL take precedence over operational convenience.

Authority Level Conformance MUST remain distinguishable from Provenance.

Provenance MAY support conformance.

Provenance MAY explain why conformance passed, failed, was partial, was blocked, was deferred, was restricted, was not evaluated, or requires repair.

Conformance evaluation SHOULD preserve provenance where authority interpretation, governance, validation, approval, publication, source reliance, relationships, privacy handling, lifecycle handling, compatibility, workflow behavior, agent behavior, implementation behavior, import, export, migration, or downstream use is affected.

Authority Level Conformance MUST remain distinguishable from Source References.

Source References MAY support conformance.

Source References MAY be required for conformance where source traceability affects authority.

Source References MAY limit conformance where sources are missing, unavailable, restricted, superseded, contradicted, incomplete, uncertain, incompatible, or provenance-limited.

A conformance result MUST NOT treat Source References as sufficient merely because a source exists, is cited, is available, reliable, official, popular, frequently referenced, or appears authoritative.

Authority Level Conformance MUST remain distinguishable from Relationship Authority.

Relationships MAY support conformance.

Relationships MAY be required for conformance where relationship meaning affects authority.

Relationships MAY limit conformance where relationships are missing, incomplete, contradictory, stale, restricted, invalid, superseded, or incompatible.

Relationship existence MUST NOT create conformance by itself.

Relationship strength MUST NOT create conformance by itself.

Relationship confidence MUST NOT create conformance by itself.

Graph centrality, backlinks, relationship count, inferred relationships, agent-created relationships, workflow-created relationships, visual graph position, search ranking, or implementation-specific links MUST NOT create conformance by themselves.

Authority Level Conformance MUST remain distinguishable from Agent Behavior.

An agent MAY assist with conformance evaluation.

An agent MAY detect missing authority information.

An agent MAY flag authority ambiguity.

An agent MAY flag authority-scope problems.

An agent MAY flag Authority Assignment, Authority Review, approval, validation, Source Reference, relationship, provenance, lifecycle, privacy, compatibility, import, export, migration, publication, workflow, implementation, or downstream-use concerns.

An agent MAY recommend repair.

An agent MAY recommend review.

Agent output MUST NOT create conformance by itself unless a governed validation or conformance process explicitly defines that behavior within a defined scope.

Agent Confidence MUST NOT create conformance by itself.

Agent-supported conformance evaluation SHOULD remain traceable to the agent, model class, instruction, workflow, Source Material, evidence, validation result, relationship context, confidence signal, review state, and human decision where applicable.

Authority Level Conformance MUST remain distinguishable from Workflow Behavior.

A workflow MAY assist with conformance evaluation.

A workflow MAY route conformance failures for review.

A workflow MAY record conformance results where governed to do so.

A workflow MAY require repair, validation, approval review, privacy review, source review, relationship review, provenance review, lifecycle review, publication review, export review, migration review, agent-output review, implementation review, or downstream-use review before conformance is accepted.

Workflow Completion MUST NOT create conformance by itself unless a governed workflow explicitly defines that behavior within a defined scope.

Authority Level Conformance MUST remain distinguishable from Implementation Behavior.

An implementation MAY display conformance results.

An implementation MAY validate conformance where governed to do so.

An implementation MAY route conformance failures for review.

An implementation MAY prevent publication, export, migration, synchronization, indexing, workflow routing, agent access, implementation exposure, or downstream use where conformance failure requires restriction.

An implementation MUST NOT define KS-0007 conformance merely because a field, tag, folder path, database row, graph edge, backlink, plugin field, status label, export package, import package, migration report, validation badge, dashboard, or implementation-specific marker exists.

A compliant implementation MUST NOT silently discard, collapse, reinterpret, expose, replace, promote, demote, broaden, narrow, inherit, transfer, downgrade, escalate, suspend, remove, override, or regenerate Authority Level, Authority Scope, Authority Assignment, Authority Review, approval context, validation context, Source References, relationships, provenance, Lifecycle State, Privacy Classification, agent context, workflow context, implementation context, import context, export context, migration context, publication context, or downstream-use context in a way that breaks KS-0007 conformance.

Authority Level Conformance SHOULD support conformance history.

Conformance history SHOULD identify or support identification of:

- prior conformance state where applicable;
- new conformance state where applicable;
- evaluated entity;
- evaluated scope;
- evaluator where applicable;
- evaluation date where applicable;
- evaluation reason where applicable;
- standard or specification applied;
- conformance profile applied where applicable;
- validation profile applied where applicable;
- Authority Level evaluated;
- Authority Scope evaluated;
- Authority Assignment evaluated;
- Authority Review evaluated;
- approval context evaluated where applicable;
- validation context evaluated where applicable;
- Source References evaluated where applicable;
- relationships evaluated where applicable;
- provenance evaluated where applicable;
- Lifecycle State evaluated where applicable;
- Privacy Classification evaluated where applicable;
- Agent Behavior evaluated where applicable;
- Workflow Behavior evaluated where applicable;
- Implementation Behavior evaluated where applicable;
- import, export, migration, publication, synchronization, backup, restoration, archival, or downstream-use context evaluated where applicable;
- failures found where applicable;
- ambiguity found where applicable;
- restrictions found where applicable;
- repair required where applicable;
- review required where applicable;
- human decision where applicable.

Authority Level Conformance SHOULD support review.

A reviewer SHOULD be able to determine:

- what was evaluated;
- what scope was evaluated;
- what requirements applied;
- what passed;
- what failed;
- what was partial;
- what was blocked;
- what was deferred;
- what was restricted;
- what was not evaluated;
- what evidence supported the conformance result;
- what provenance supports the conformance result;
- whether the conformance result affects Authority Level, Authority Scope, Authority Assignment, Authority Review, approval, validation, Source References, relationships, Lifecycle State, Privacy Classification, Agent Behavior, Workflow Behavior, Implementation Behavior, import, export, migration, publication, synchronization, archival, or downstream use;
- whether further review, validation, repair, privacy review, source review, relationship review, provenance review, lifecycle review, approval review, export review, migration review, publication review, agent-output review, workflow review, or implementation review is required.

Authority Level Conformance SHOULD support validation.

A validator SHOULD be able to determine whether:

- Authority Level is present where required;
- Authority Scope is present where required;
- Authority Assignment is present where required;
- Authority Review is present where required;
- authority-related approval context is preserved where required;
- authority-related validation context is preserved where required;
- authority-related Source References are preserved where required;
- authority-related relationships are preserved where required;
- authority-related provenance is preserved where required;
- authority-related Lifecycle State is preserved where required;
- authority-related Privacy Classification is preserved where required;
- authority-related Agent Behavior is distinguishable where required;
- authority-related Workflow Behavior is distinguishable where required;
- authority-related Implementation Behavior is distinguishable where required;
- authority-related import, export, migration, publication, synchronization, backup, restoration, archival, or downstream-use context is preserved where required;
- authority information remains explicit, scoped, interpretable, portable, traceable, reviewable, privacy-respecting, provenance-preserving, validatable, compatible, governable, and implementation-independent;
- authority information remains distinguishable from Object Identity, Lifecycle State, Validation State, Privacy Classification, Provenance, Source References, Relationship Authority, Agent Confidence, Workflow Completion, Implementation Visibility, storage behavior, and hidden application behavior.

Authority Level Conformance SHOULD support compatibility.

A compliant implementation, workflow, agent, validator, storage system, import process, export process, migration process, backup process, restoration process, synchronization process, archive process, or publication process MUST NOT claim KS-0007 conformance where Authority Level meaning has been silently lost, collapsed, exposed, replaced, promoted, demoted, broadened, narrowed, inherited, transferred, downgraded, escalated, suspended, removed, overridden, regenerated, made ambiguous, made implementation-dependent, made privacy-unsafe, made source-untraceable, made provenance-incomplete, made relationship-ambiguous, made validation-ambiguous, made lifecycle-ambiguous, made import-ambiguous, made export-ambiguous, made migration-ambiguous, or made unsafe for downstream use.

Authority Level Conformance SHOULD support historical preservation.

A governed entity MAY retain historical authority conformance context even when it is deprecated, superseded, rejected, archived, restricted, quarantined, repaired, imported, exported, migrated, synchronized, published, restored, or replaced.

Historical authority conformance context does not mean the entity remains current.

Historical authority conformance context does not mean the entity is approved for future use.

Historical authority conformance context does not mean the entity is authoritative for future use.

Historical authority conformance context does not mean the entity is public, exportable, publishable, unrestricted, safe for agent use, safe for workflow use, or safe for downstream use.

Historical authority conformance context SHOULD preserve enough information for future interpretation, audit, migration, compatibility review, governance review, source traceability, authority review, privacy review, provenance review, lifecycle review, validation review, workflow review, agent-output review, implementation review, and evidence review.

KS-0007 is successful when future humans can inspect Authority Level and determine what authority applies, what scope applies, what supports the authority, what limits the authority, whether the authority is current or historical, whether review or validation is required, whether privacy or lifecycle handling constrains authority, and whether authority remains meaningful across time.

KS-0007 is successful when future agents can assist with authority interpretation, review, validation, source checking, relationship checking, provenance review, lifecycle review, privacy review, migration review, compatibility review, and maintenance without becoming unreviewable authorities.

KS-0007 is successful when future workflows can coordinate authority-related work without hiding approval, review, validation, privacy, provenance, Source Reference, relationship, lifecycle, compatibility, import, export, migration, publication, implementation, or downstream-use boundaries.

KS-0007 is successful when future validators can detect missing Authority Level, unclear Authority Scope, unsupported Authority Assignment, incomplete Authority Review, authority-approval confusion, authority-validation confusion, authority-provenance confusion, authority-source confusion, authority-relationship confusion, authority-lifecycle confusion, authority-privacy confusion, authority-agent confusion, authority-workflow confusion, authority-implementation confusion, authority-import ambiguity, authority-export ambiguity, authority-migration loss, authority-publication risk, compatibility failure, implementation lock-in, or governance drift.

KS-0007 is successful when future implementations can store, display, search, index, link, route, validate, import, export, migrate, synchronize, back up, restore, archive, process, publish, or preserve Authority Level without redefining standard-level authority meaning.

KS-0007 is successful when future import, export, and migration processes can preserve authority meaning or explicitly disclose authority loss, limitation, ambiguity, mapping, redaction, suspension, downgrade, escalation, transfer, review requirement, validation requirement, privacy constraint, provenance constraint, Source Reference constraint, relationship constraint, lifecycle constraint, compatibility constraint, publication constraint, or downstream-use limit.

KS-0007 is successful when future publication and downstream-use processes can determine whether authority may be exposed, cited, summarized, exported, synchronized, indexed, shared, published, used by agents, used by workflows, used by implementations, or applied downstream.

KS-0007 is successful when future governance can evolve Authority Level behavior without causing governance drift.

Future specifications, authority vocabularies, authority transition specifications, conformance profiles, validation specifications, storage standards, agent standards, workflow standards, implementation profiles, publication specifications, import formats, export formats, migration mappings, restoration mappings, synchronization mappings, and operational guides MAY refine KS-0007 only when they preserve KS-0007 meaning or explicitly govern deprecation, supersession, replacement, incompatibility, migration, validation, and compatibility expectations.

Authority Level Conformance and Success Criteria are successful when future humans, agents, workflows, validators, storage systems, migration processes, import processes, export processes, publication processes, and implementations can determine whether KS-0007 requirements were satisfied, what authority behavior was preserved, what authority behavior failed, what scope applies, what evidence supports the conformance result, what repair or review remains required, what privacy or lifecycle limits apply, what downstream-use limits remain, and whether Authority Level remains meaningful across time and implementation replacement.
