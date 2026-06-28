# IMP-0001 — Obsidian and Codex Implementation Profile

Document ID: IMP-0001
Title: Obsidian and Codex Implementation Profile
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Implementation Profile
Phase: Phase 5 — Implementation Profiles
Milestone: 5.2 — Obsidian and Codex Implementation Profile
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; AG-0002 — Agent Role and Responsibility Standard; AG-0003 — Agent Permission and Traceability Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; WF-0003 — Knowledge Maintenance and Update Workflow Standard; WF-0004 — Publication, Export, and Downstream Use Workflow Standard; DEP-0001 — Bare Usable Deployment Readiness Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and implementation-profile rules are interpreted within IMP-0001.

Where conflicts arise between Obsidian behavior, Codex behavior, vault behavior, repository behavior, local machine setup, folder mapping, Markdown handling, metadata representation, Knowledge Record handling, Source Material handling, agent behavior, workflow execution, validation support, review support, backup behavior, sync behavior, export behavior, recovery behavior, implementation convenience, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, storage behavior, deployment readiness, or future specifications, the higher-authority standards SHALL guide interpretation and resolution.

IMP-0001 is subordinate to TB-0000, TB-0001, TB-0002, TB-0003, the Phase 1 Knowledge Standards, the Phase 2 Storage Standards, the Phase 3 Agent Standards, the Phase 4 Workflow Standards, and DEP-0001.

IMP-0001 is an implementation profile.

IMP-0001 does not define The Brain Standard itself.

IMP-0001 explains how Obsidian and Codex may realize The Brain Standard in practice while remaining subordinate to the governed standards.

If IMP-0001 appears to conflict with a constitutional document, Knowledge Standard, Storage Standard, Agent Standard, Workflow Standard, or DEP-0001, the higher-authority document takes precedence unless formally revised through governance.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Implementation Profile refers to a governed implementation document that explains how a specific tool, vault, repository, workflow environment, agent environment, or software stack realizes The Brain Standard in practice without becoming the standard itself.
- Obsidian refers to the Markdown-based local knowledge environment used by this implementation profile as a practical reference interface for reading, navigating, editing, linking, reviewing, and maintaining governed material.
- Codex refers to the agentic coding and file-operation environment used by this implementation profile to assist with repository work, file inspection, validation support, refactoring, template creation, scripted checks, and implementation-support tasks within governed boundaries.
- Vault refers to the practical local file environment used by Obsidian to access Markdown files, Source Material references, Knowledge Records, governed documents, implementation-support files, and related artifacts.
- Repository refers to the version-controlled storage environment used to preserve, review, compare, synchronize, and manage The Brain files.
- Local Machine refers to the computer or local workspace where the repository, vault, implementation-support files, scripts, templates, prompts, validators, backups, exports, and working files may exist.
- Implementation Environment refers to the combined practical environment made up of the local machine, repository, vault, Obsidian setup, Codex setup, supporting files, scripts, templates, validators, and operational instructions.
- Folder Mapping refers to the practical alignment between The Brain Standard storage areas and the folders used in the Obsidian vault or repository.
- Markdown Handling refers to the way Markdown files are created, displayed, edited, linked, validated, reviewed, preserved, and exported in the implementation environment.
- Metadata Representation refers to the implementation-specific way metadata is written, displayed, preserved, validated, or supported without redefining standard metadata meaning.
- Knowledge Record Handling refers to the practical process for creating, editing, reviewing, validating, storing, maintaining, and preserving Knowledge Records in Obsidian and Codex.
- Source Material Handling refers to the practical process for storing, staging, referencing, preserving, reviewing, importing, exporting, archiving, or restricting Source Material in the implementation environment.
- Agent Assistance refers to Codex or other agent-supported work performed within the boundaries defined by the Agent Standards.
- Workflow Execution refers to practical use of the governed Workflow Standards inside the implementation environment.
- Validation Support refers to implementation-level checks, scripts, prompts, reports, inspections, or review aids that help determine conformance without replacing governed validation.
- Review Support refers to implementation-level features, files, checklists, prompts, comments, diffs, or workflows that support human review without replacing approval authority.
- Implementation Limitation refers to any constraint, risk, missing capability, tool behavior, plugin behavior, sync behavior, automation behavior, or local setup issue that prevents the implementation from fully realizing the standard.
- Non-Conformance refers to a condition where the implementation does not satisfy the applicable standard, profile, workflow, storage, agent, validation, deployment-readiness, or governance expectation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Source Reference refers to a traceable reference from a governed entity to Source Material that supports, explains, contextualizes, contradicts, originates, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a governed entity.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, validation result, workflow output, agent output, import record, export record, migration record, or other governed entity.
- Authority Level refers to the governance weight, interpretive authority, review weight, trust boundary, or use-authority assigned to a governed entity within a defined scope.
- Privacy Classification refers to the explicit classification that defines permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, workflow access, implementation access, or downstream-use handling for a governed entity.
- Validation refers to the process of checking whether a governed entity satisfies applicable standards, specifications, metadata expectations, provenance expectations, relationship expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, workflow expectations, agent expectations, implementation expectations, import expectations, export expectations, migration expectations, publication expectations, synchronization expectations, indexing expectations, backup expectations, or downstream-use expectations.

## 1. Purpose

The purpose of IMP-0001 is to define how Obsidian and Codex may be used together as a practical implementation environment for The Brain Standard.

IMP-0001 explains how the governed standards are realized in a local Markdown-based vault, repository, and agent-assisted workflow without allowing Obsidian, Codex, plugins, prompts, scripts, templates, validators, sync tools, backup tools, generated files, graph views, search results, or automation to redefine the standard.

IMP-0001 exists to bridge the gap between standard-level architecture and practical daily use.

The Brain Standard defines the durable meaning of knowledge, storage, agents, workflows, validation, governance, deployment readiness, and implementation boundaries.

Obsidian and Codex provide practical tools for working with those governed files.

Obsidian may support:

- human-readable Markdown access;
- file navigation;
- linking and backlink visibility;
- graph views;
- note editing;
- vault-level organization;
- review support;
- search;
- local-first use;
- plugin-supported usability where allowed.

Codex may support:

- repository inspection;
- file comparison;
- syntax review;
- Markdown cleanup;
- structured drafting;
- batch editing;
- validator creation;
- script creation;
- template creation;
- implementation-support work;
- agent-assisted review within authorized boundaries.

IMP-0001 defines how these tools SHOULD be used together without creating architectural drift.

IMP-0001 is not a replacement for the Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, or DEP-0001.

IMP-0001 does not decide what a Knowledge Object is.

IMP-0001 does not decide what Object Identity means.

IMP-0001 does not decide what metadata means.

IMP-0001 does not decide what relationships mean.

IMP-0001 does not decide what Source References or provenance mean.

IMP-0001 does not decide what Lifecycle State, Authority Level, Privacy Classification, or Validation mean.

IMP-0001 does not decide what agents are allowed to do.

IMP-0001 does not decide what workflows approve, reject, publish, export, maintain, or archive.

Those meanings are defined by the governed standards.

IMP-0001 defines the practical implementation profile for applying those standards in an Obsidian and Codex environment.

The primary purpose of IMP-0001 is to make The Brain usable on a local machine and repository without sacrificing implementation independence, portability, human readability, AI readability, governance, reviewability, privacy protection, validation, or long-term maintainability.

IMP-0001 is successful when a future human, Codex agent, Obsidian user, repository maintainer, validator, workflow, or downstream implementer can determine:

- where The Brain files should live in the implementation environment;
- how Obsidian should interact with governed Markdown files;
- how Codex should assist without exceeding agent boundaries;
- how folders map to the Storage Standards;
- how metadata should be represented without redefining metadata meaning;
- how Knowledge Records should be created, edited, reviewed, and maintained;
- how Source Material should be staged, referenced, preserved, or restricted;
- how workflows should be executed or supported;
- how validation and review should be supported;
- how backup, sync, export, and recovery should be handled;
- what implementation limitations remain;
- what non-conformance must be routed for correction.

## 2. Relationship to Prior Standards

IMP-0001 is subordinate to and derived from the constitutional foundation, Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, and DEP-0001.

IMP-0001 depends on:

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
- DEP-0001 — Bare Usable Deployment Readiness Standard.

TB-0000 establishes The Brain as an implementation-independent knowledge architecture designed to preserve, organize, and evolve knowledge over time.

IMP-0001 applies that purpose by treating Obsidian and Codex as implementation tools rather than sources of standard authority.

TB-0001 establishes the architecture principles that govern The Brain Standard.

IMP-0001 applies those principles by requiring the Obsidian and Codex implementation to preserve:

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

IMP-0001 belongs to the implementation layer.

It depends on the lower layers but does not redefine them.

Layer 1 Knowledge Standards define knowledge meaning.

Layer 2 Storage Standards define storage organization.

Layer 3 Agent Standards define agent boundaries, roles, permissions, traceability, and review requirements.

Layer 4 Workflow Standards define governed workflow behavior.

Layer 5 Implementation Profiles explain how specific tools realize the standard in practice.

Because IMP-0001 is an implementation profile, it MAY define practical behavior for Obsidian, Codex, repository layout, local machine setup, implementation-support files, tool usage, scripts, validators, templates, prompts, and operational procedures.

However, IMP-0001 MUST NOT redefine:

- Knowledge Object meaning;
- Knowledge Record meaning;
- Object Identity;
- metadata meaning;
- relationship meaning;
- Source Reference meaning;
- provenance meaning;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage meaning;
- agent authority;
- workflow authority;
- approval;
- deployment readiness.

TB-0003 establishes the governance model for The Brain Standard.

IMP-0001 follows the document authority hierarchy defined by TB-0003.

As an implementation profile, IMP-0001 has lower authority than constitutional documents and standards.

If an Obsidian behavior, Codex behavior, plugin behavior, repository behavior, prompt pattern, script output, template, validator, automation, graph view, search result, index, cache, generated summary, or workflow convenience conflicts with a higher-authority standard, the higher-authority standard controls.

KS-0001 through KS-0009 define knowledge-level meaning.

IMP-0001 MUST preserve those meanings while explaining how they are represented, viewed, edited, validated, reviewed, and maintained in Obsidian and Codex.

SS-0001 and SS-0002 define storage architecture and layout expectations.

IMP-0001 MUST preserve storage boundaries while explaining how the repository, vault, local folders, implementation-support files, generated files, imports, exports, backups, archives, and working areas are used in practice.

AG-0001, AG-0002, and AG-0003 define agent operating boundaries, agent roles, responsibilities, permissions, traceability, review requirements, and escalation expectations.

IMP-0001 MUST preserve those boundaries while explaining how Codex or other agents may assist implementation work.

WF-0001 through WF-0004 define governed workflow behavior.

IMP-0001 MUST preserve workflow boundaries while explaining how Obsidian and Codex support ingestion, review and approval, maintenance and update, publication, export, and downstream-use workflows.

DEP-0001 defines bare usable deployment readiness.

IMP-0001 follows DEP-0001 by explaining the practical implementation profile that comes after deployment-readiness structure exists.

DEP-0001 completion does not mean IMP-0001 is complete.

IMP-0001 completion does not mean The Brain is publicly releasable, fully automated, unrestricted for export, unrestricted for synchronization, unrestricted for agent exposure, or unrestricted for downstream use.

IMP-0001 is successful when it makes Obsidian and Codex usable as an implementation environment while preserving the authority, boundaries, and meaning of all prior standards.

## 3. Implementation Scope and Boundaries

IMP-0001 applies to the Obsidian and Codex implementation environment for The Brain Standard.

The implementation environment includes:

- the local machine used to work with The Brain;
- the GitHub repository or local repository copy;
- the Obsidian vault or vault-like Markdown workspace;
- governed Markdown files;
- Source Material areas;
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
- agent-support files;
- workflow-support files;
- templates;
- prompts;
- validators;
- scripts;
- generated indexes;
- generated caches;
- operational notes;
- handoff summaries;
- setup instructions.

IMP-0001 defines how these implementation components SHOULD be organized, used, limited, validated, reviewed, backed up, synchronized, exported, recovered, and corrected.

IMP-0001 applies to Obsidian only as a reference implementation interface.

Obsidian MAY be used to:

- open and edit governed Markdown files;
- navigate standards and Knowledge Records;
- inspect links and backlinks;
- support human-readable review;
- display folder structure;
- assist daily use;
- support local-first knowledge work;
- improve discoverability;
- support non-authoritative graph or search exploration.

Obsidian MUST NOT be treated as the source of standard meaning.

Obsidian folder placement MUST NOT define Object Identity.

Obsidian backlinks MUST NOT define governed relationships by themselves.

Obsidian graph views MUST NOT define governed meaning.

Obsidian tags MUST NOT define governed metadata unless governed by a standard or specification.

Obsidian plugins MUST NOT redefine metadata, relationships, lifecycle state, authority level, privacy classification, validation, review status, approval, export permission, publication permission, or deployment readiness.

IMP-0001 applies to Codex only as an agentic implementation-support environment.

Codex MAY be used to:

- inspect files;
- compare files;
- identify syntax issues;
- identify structural inconsistencies;
- propose edits;
- draft implementation-support content;
- assist with validators;
- assist with scripts;
- assist with templates;
- assist with repository organization;
- assist with conformance checks;
- assist with handoff summaries;
- support workflow execution where authorized.

Codex MUST NOT be treated as an unreviewable authority.

Codex MUST NOT approve standards by itself.

Codex MUST NOT change lifecycle state, authority level, privacy classification, validation state, publication permission, export permission, migration permission, deployment readiness, or downstream-use readiness unless a governed workflow explicitly allows the change within a defined and reviewable scope.

Codex MUST NOT silently delete, overwrite, move, expose, publish, export, or restructure governed material where the action affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, reviewability, compatibility, storage meaning, workflow state, agent traceability, deployment readiness, or downstream use.

IMP-0001 is allowed to define practical implementation choices.

These may include:

- recommended local folder placement;
- repository-to-vault relationship;
- Obsidian vault opening behavior;
- Codex working boundaries;
- Markdown editing conventions;
- metadata representation conventions;
- file naming conventions where storage standards allow them;
- implementation-support folder use;
- validator support;
- template support;
- prompt support;
- backup support;
- sync support;
- export support;
- recovery support;
- non-conformance routing.

IMP-0001 is not allowed to redefine higher-authority meaning.

IMP-0001 MUST NOT redefine:

- the constitutional mission of The Brain;
- the layered architecture;
- governance authority;
- document lifecycle rules;
- Knowledge Object meaning;
- Knowledge Record meaning;
- Source Material meaning;
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
- storage layout meaning;
- agent roles;
- agent permissions;
- agent traceability;
- workflow authority;
- deployment readiness.

IMP-0001 SHOULD remain practical.

The implementation profile SHOULD be specific enough that a human or Codex-style agent can set up, inspect, maintain, validate, and operate the Obsidian and Codex environment without repeatedly inventing local rules.

IMP-0001 SHOULD remain portable.

The implementation profile SHOULD avoid tool-specific assumptions that would prevent future implementation profiles for other tools, such as Claude Code, ChatGPT, local AI systems, custom applications, databases, or future software.

IMP-0001 SHOULD remain local-first where practical.

The implementation profile SHOULD support a local copy of The Brain that remains usable without depending on a specific cloud service, plugin, proprietary database, hidden application state, or hosted AI memory.

IMP-0001 SHOULD remain reviewable.

A future human, agent, validator, workflow, or repository maintainer SHOULD be able to inspect the implementation environment and determine:

- what files are governed;
- what files are implementation-support files;
- what files are generated;
- what files are temporary;
- what files are source material;
- what files are Knowledge Records;
- what files require review;
- what files require validation;
- what files require privacy handling;
- what files require backup;
- what files may be exported;
- what files must not be exposed;
- what Codex may do;
- what Obsidian may display;
- what remains non-conformant.

The implementation scope of IMP-0001 is limited to Obsidian and Codex.

Future implementation profiles MAY define other environments.

Those future profiles MUST preserve the same higher-authority standards unless the standards are formally revised through governance.

## 4. Obsidian Role in the Implementation

Obsidian is the primary human-facing Markdown interface for this implementation profile.

Obsidian exists in IMP-0001 to make The Brain Standard practical to read, navigate, edit, review, and maintain in daily use.

Obsidian MAY be used as:

- a local Markdown vault;
- a human-readable document browser;
- a governed note-editing environment;
- a standards navigation interface;
- a Knowledge Record navigation interface;
- a review-support interface;
- a lightweight relationship-discovery aid;
- a search interface;
- a backlink visibility tool;
- a graph exploration tool;
- a practical local-first workspace.

Obsidian MUST remain subordinate to The Brain Standard.

Obsidian is not the standard.

Obsidian is not the source of Knowledge Object meaning.

Obsidian is not the source of Object Identity.

Obsidian is not the source of metadata meaning.

Obsidian is not the source of relationship meaning.

Obsidian is not the source of Source Reference or provenance meaning.

Obsidian is not the source of Lifecycle State, Authority Level, Privacy Classification, or Validation meaning.

Obsidian is not the source of approval.

Obsidian is not the source of deployment readiness.

Obsidian is not the source of publication, export, synchronization, indexing, backup, migration, or downstream-use permission.

Obsidian MAY display governed files.

Obsidian MUST NOT silently convert display behavior into governed meaning.

Obsidian MAY display folders.

Folder display MUST NOT define Object Identity, lifecycle state, authority, privacy classification, validation state, provenance, relationship meaning, source-reference meaning, or approval status by itself.

Obsidian MAY display links and backlinks.

Links and backlinks MAY help humans or agents discover possible relationships.

Links and backlinks MUST NOT be treated as governed relationships unless the relationship meaning is explicit, reviewable, and compliant with the applicable Relationship Standard.

Obsidian MAY display graph views.

Graph views MAY help exploration.

Graph views MUST NOT define governed meaning, relationship authority, relationship strength, validation state, approval state, or downstream-use readiness by themselves.

Obsidian MAY support tags.

Tags MAY support navigation, search, filtering, visual grouping, workflow convenience, or implementation usability.

Tags MUST NOT define standard metadata unless a governed standard, specification, or implementation profile explicitly defines the tag meaning and handling requirements.

Obsidian MAY support plugins.

Plugins MAY improve usability, navigation, search, review support, formatting, metadata display, templates, validation assistance, or export support.

Plugins MUST NOT redefine The Brain Standard.

Plugins MUST NOT become required for understanding governed meaning unless a future implementation profile explicitly defines the dependency, limitation, fallback behavior, and portability risk.

A compliant Obsidian setup SHOULD preserve human readability without requiring plugins.

A compliant Obsidian setup SHOULD preserve AI readability without requiring hidden plugin state.

A compliant Obsidian setup SHOULD allow governed files to remain understandable in a plain text editor.

A compliant Obsidian setup SHOULD allow The Brain repository to remain useful even if Obsidian is replaced.

Obsidian MAY assist with review.

Review support MAY include:

- opening files for inspection;
- comparing sections manually;
- checking visible metadata;
- following links;
- searching for duplicate terms;
- reviewing draft files;
- navigating to dependencies;
- inspecting local file organization;
- supporting checklist use.

Obsidian review support MUST NOT replace governed review or approval.

Obsidian MAY assist with workflow execution.

Workflow support MAY include:

- navigating ingestion candidates;
- opening draft Knowledge Records;
- reviewing source-linked records;
- moving through review folders;
- viewing maintenance candidates;
- preparing export candidates;
- inspecting archive areas;
- displaying operational checklists.

Obsidian workflow support MUST NOT redefine workflow authority.

Obsidian MAY assist with local-first use.

Local-first use SHOULD allow The Brain to remain usable when cloud sync, hosted AI, external services, or plugins are unavailable.

Obsidian MAY use synchronization tools.

Synchronization MUST preserve privacy classification, review boundaries, export limits, backup expectations, and downstream-use restrictions.

Synchronization MUST NOT be treated as publication approval.

Synchronization MUST NOT expose restricted material unless permitted by the applicable privacy classification and workflow review.

Obsidian MAY support search.

Search results MAY help discovery.

Search results MUST NOT define validation, approval, authority, relationship meaning, or knowledge truth by themselves.

Obsidian MAY support generated indexes, caches, or graph artifacts.

Generated indexes, caches, embeddings, graph files, plugin databases, or search artifacts MUST be treated as implementation-support material unless a governed specification defines otherwise.

Generated implementation-support material MUST NOT replace governed files.

Generated implementation-support material MUST NOT be treated as authoritative merely because it is useful, searchable, visible, or frequently used.

Obsidian is successful in this implementation when it helps humans work with The Brain Standard while preserving implementation independence, explicit meaning, portability, reviewability, privacy boundaries, validation expectations, and governance.

## 5. Codex Role in the Implementation

Codex is the primary agentic file-operation and repository-assistance environment for this implementation profile.

Codex exists in IMP-0001 to help inspect, draft, compare, validate, refactor, and maintain The Brain files within governed agent boundaries.

Codex MAY assist with:

- reading governed files;
- inspecting repository structure;
- comparing files;
- detecting syntax issues;
- detecting spelling and grammar issues;
- checking Markdown heading structure;
- checking metadata presence;
- checking section sequence;
- identifying duplicate rules or definitions;
- identifying possible standard-boundary conflicts;
- drafting new sections;
- drafting implementation-support files;
- drafting templates;
- drafting prompts;
- drafting validators;
- drafting scripts;
- preparing handoff summaries;
- preparing review reports;
- identifying non-conformance;
- recommending corrective routing.

Codex MUST remain subordinate to The Brain Standard.

Codex is not the standard.

Codex is not a governance authority.

Codex is not an approval authority.

Codex is not an unrestricted editor.

Codex is not an unrestricted migration actor.

Codex is not an unrestricted publication actor.

Codex is not an unrestricted export actor.

Codex is not an unrestricted deletion actor.

Codex MAY propose changes.

Codex MUST distinguish proposed changes from approved changes.

Codex MAY draft file content.

Codex MUST distinguish drafted content from approved content.

Codex MAY inspect compliance.

Codex MUST distinguish validation support from approval.

Codex MAY identify probable issues.

Codex MUST distinguish probable issues from final governance decisions.

Codex MAY recommend lifecycle, authority, privacy, validation, relationship, source-reference, provenance, storage, workflow, or implementation changes.

Codex MUST NOT apply those changes as governed truth unless the applicable workflow, permission, review, and approval requirements are satisfied.

Codex MAY assist with Knowledge Records.

Codex MAY extract, summarize, classify, structure, or propose Knowledge Records from Source Material where permitted by agent boundaries and workflow rules.

Codex MUST preserve the distinction between Source Material and Knowledge Records.

Codex MUST preserve source-reference and provenance expectations when working with source-derived knowledge.

Codex MUST NOT treat a generated summary as a Knowledge Record unless the applicable ingestion, metadata, source-reference, validation, and review requirements are satisfied.

Codex MAY assist with metadata.

Codex MAY propose metadata values.

Codex MUST NOT treat proposed metadata as approved metadata unless review and workflow requirements are satisfied.

Codex MUST NOT treat metadata as Object Identity unless the applicable standard or specification defines that identity role.

Codex MAY assist with relationships.

Codex MAY identify possible relationships.

Codex MAY propose relationship entries.

Codex MUST NOT treat inferred, suggested, linked, or search-derived relationships as governed relationships unless they are explicit, reviewable, and compliant with the Relationship Standard.

Codex MAY assist with validation.

Validation assistance MAY include:

- checking required metadata;
- checking section counts;
- checking heading order;
- checking dependency references;
- checking related-file references;
- checking lifecycle status;
- checking authority status;
- checking privacy-classification presence;
- checking source-reference presence;
- checking provenance expectations;
- checking storage placement;
- checking workflow routing;
- checking implementation-profile conformance.

Codex validation assistance MUST NOT be treated as approval by itself.

Codex MAY assist with repository work.

Repository work MAY include:

- locating files;
- comparing file versions;
- identifying missing files;
- identifying misplaced files;
- checking naming consistency;
- preparing pull requests;
- preparing commits where explicitly authorized;
- updating files where explicitly authorized;
- creating files where explicitly authorized;
- organizing implementation-support files where explicitly authorized.

Codex MUST NOT silently overwrite governed files.

Codex MUST NOT silently delete governed files.

Codex MUST NOT silently move governed files.

Codex MUST NOT silently expose restricted files.

Codex MUST NOT silently publish or export governed material.

Codex MUST NOT silently convert Draft material into Approved material.

Codex MUST NOT silently convert validation success into approval.

Codex MUST NOT silently convert agent confidence into Authority Level.

Codex MUST NOT silently convert workflow completion into downstream-use permission.

Codex activity SHOULD be traceable.

Traceability SHOULD identify:

- what Codex read;
- what Codex compared;
- what Codex proposed;
- what Codex changed where changes were authorized;
- what files were affected;
- what standards were used;
- what assumptions were made;
- what limitations remain;
- what review is still required;
- what human decision is needed.

Codex is successful in this implementation when it reduces manual burden while preserving human reviewability, governed meaning, privacy boundaries, source traceability, authority control, validation expectations, storage boundaries, workflow boundaries, deployment readiness, and implementation independence.

## 6. Repository and Local Machine Layout

The repository and local machine layout define how The Brain files are practically stored, opened, inspected, backed up, synchronized, and maintained in the Obsidian and Codex implementation environment.

The repository SHOULD remain the primary governed storage environment for The Brain Standard files.

The local machine SHOULD contain a working copy of the repository.

The Obsidian vault SHOULD open the appropriate local repository folder or a controlled vault folder mapped to the repository.

Codex SHOULD operate on the local repository copy or an explicitly authorized repository workspace.

The implementation SHOULD preserve a clear distinction between:

- governed standard files;
- governed specification files;
- implementation profile files;
- operational guide files;
- Knowledge Records;
- Source Material;
- drafts;
- review material;
- archives;
- imports;
- exports;
- backups;
- migration material;
- implementation-support files;
- agent-support files;
- workflow-support files;
- templates;
- prompts;
- validators;
- scripts;
- generated files;
- caches;
- indexes;
- temporary files.

The recommended repository path for IMP-0001 is:

`brain-standard/Standards/IMP/IMP-0001 — Obsidian and Codex Implementation Profile.md`

The repository SHOULD contain a dedicated `IMP` folder for implementation profiles.

The `IMP` folder SHOULD be located under:

`brain-standard/Standards/IMP/`

Implementation profiles SHOULD remain separate from constitutional documents, Knowledge Standards, Storage Standards, Agent Standards, Workflow Standards, and Deployment Readiness Standards.

The local machine SHOULD preserve the repository structure unless a governed implementation profile defines a controlled mapping.

A local Obsidian vault MAY open:

- the repository root;
- the `brain-standard` folder;
- a controlled vault folder that mirrors the repository structure;
- another explicitly documented folder mapping.

The chosen vault opening method SHOULD be documented.

The chosen vault opening method SHOULD preserve file paths enough for humans, agents, validators, and workflows to locate governed material reliably.

The chosen vault opening method SHOULD NOT hide governed files behind plugin-only views, database-only views, generated indexes, or application-specific state.

Codex SHOULD operate from the repository root or from an explicitly documented working directory.

Codex working context SHOULD be limited to the files required for the task.

Codex SHOULD NOT be given unrestricted practical scope over private, restricted, unrelated, generated, cached, backup, export, migration, or downstream-use material unless the applicable privacy, authority, workflow, and review boundaries permit it.

A compliant local machine layout SHOULD support:

- local editing;
- local review;
- local validation support;
- local backup;
- local recovery;
- controlled sync;
- controlled export;
- repository comparison;
- future migration;
- agent-assisted inspection;
- implementation replacement.

A compliant local machine layout SHOULD avoid placing governed meaning only in:

- Obsidian settings;
- plugin databases;
- hidden folders;
- generated caches;
- local-only indexes;
- Codex memory;
- agent memory;
- operating-system metadata;
- cloud-sync metadata;
- undocumented scripts;
- undocumented templates;
- undocumented prompts.

Implementation-support files MAY exist.

Implementation-support files SHOULD be stored in a clearly identified implementation-support area.

Implementation-support files MAY include:

- Obsidian setup notes;
- Codex usage notes;
- validator scripts;
- template files;
- prompt files;
- README files;
- setup checklists;
- export scripts;
- backup scripts;
- migration helpers;
- generated reports;
- conformance reports;
- operational examples.

Implementation-support files MUST NOT redefine higher-authority standards.

Generated files MAY exist.

Generated files SHOULD be clearly identified as generated, temporary, derived, cached, indexed, or implementation-supporting.

Generated files MUST NOT be treated as governed source-of-truth files unless a future governed specification explicitly defines that role.

Backup areas SHOULD be separated from active governed files.

Export areas SHOULD be separated from active governed files.

Import areas SHOULD be separated from active governed files.

Migration areas SHOULD be separated from active governed files.

Archive areas SHOULD be separated from active governed files while preserving historical traceability.

The local machine layout SHOULD allow a future human, Codex agent, Obsidian user, validator, or workflow to determine:

- what the active repository is;
- what the active vault is;
- what files are governed;
- what files are drafts;
- what files are implementation-support files;
- what files are generated;
- what files are source material;
- what files are Knowledge Records;
- what files are backups;
- what files are exports;
- what files are imports;
- what files are archived;
- what files are safe for Codex to inspect;
- what files require privacy review before inspection;
- what files may be synchronized;
- what files may be exported;
- what files require validation;
- what files require human review.

Repository and local machine layout is successful when The Brain can be opened in Obsidian, inspected by Codex, reviewed by a human, backed up, synchronized, exported, recovered, and migrated without allowing local setup convenience to redefine governed meaning.

## 7. Folder Mapping to The Brain Standard

Folder Mapping defines how the practical Obsidian and Codex implementation environment aligns with The Brain Standard storage areas.

Folder Mapping exists to help humans, agents, workflows, validators, and implementations locate material consistently without allowing folder placement to define governed meaning.

The implementation SHOULD map practical folders to the storage responsibilities defined by the Storage Standards.

A folder MAY help organize files.

A folder MUST NOT define Object Identity by itself.

A folder MUST NOT define Knowledge Object meaning by itself.

A folder MUST NOT define Knowledge Record meaning by itself.

A folder MUST NOT define Source Material meaning by itself.

A folder MUST NOT define metadata meaning by itself.

A folder MUST NOT define relationship meaning by itself.

A folder MUST NOT define Source Reference or provenance meaning by itself.

A folder MUST NOT define Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication permission, export permission, synchronization permission, backup permission, migration permission, or downstream-use readiness by itself.

Folder Mapping MAY include practical areas for:

- governed documents;
- standards;
- specifications;
- implementation profiles;
- operational guides;
- Knowledge Records;
- Source Material;
- drafts;
- review material;
- archives;
- imports;
- exports;
- backups;
- migration material;
- implementation-support files;
- agent-support files;
- workflow-support files;
- templates;
- prompts;
- validators;
- scripts;
- generated files;
- caches;
- indexes;
- temporary files.

The implementation SHOULD preserve the existing repository convention where governed standards are grouped under:

`brain-standard/Standards/`

Within that area, implementation profiles SHOULD use:

`brain-standard/Standards/IMP/`

The recommended file path for this implementation profile is:

`brain-standard/Standards/IMP/IMP-0001 — Obsidian and Codex Implementation Profile.md`

The implementation MAY use folders to support usability.

Usability folders MAY help with:

- browsing;
- review;
- workflow routing;
- import staging;
- export staging;
- backup separation;
- archive preservation;
- implementation setup;
- agent work;
- validation reports;
- operational support.

A folder used for usability MUST remain distinguishable from governed meaning.

A Draft folder MAY contain draft material.

However, placement in a Draft folder MUST NOT be the only expression of Lifecycle State when lifecycle state affects governed interpretation or use.

A Review folder MAY contain material awaiting review.

However, placement in a Review folder MUST NOT be treated as review completion, validation success, approval, authority assignment, publication permission, export permission, or downstream-use readiness.

An Archive folder MAY contain historical, superseded, deprecated, rejected, inactive, migrated, or no-longer-current material.

However, placement in an Archive folder MUST NOT erase provenance, relationships, source references, lifecycle history, authority context, privacy classification, validation history, or compatibility context.

An Import folder MAY contain incoming material.

However, placement in an Import folder MUST NOT make the material a Knowledge Record.

An Export folder MAY contain material prepared for transfer, publication, migration, sharing, review, or downstream use.

However, placement in an Export folder MUST NOT create export approval, publication approval, privacy clearance, migration readiness, or downstream-use readiness by itself.

A Backup folder MAY contain restoration or preservation copies.

However, placement in a Backup folder MUST NOT create recovery readiness unless backup integrity, scope, restoration path, privacy handling, and review expectations are satisfied.

A Generated folder MAY contain indexes, caches, embeddings, graph artifacts, validator outputs, reports, summaries, or implementation-support files.

However, generated material MUST remain distinguishable from governed source-of-truth material.

Generated material MUST NOT replace Knowledge Records, Source Material, metadata, relationships, Source References, provenance, lifecycle state, authority level, privacy classification, validation state, or governed approval.

The Obsidian vault MAY expose folder structure for navigation.

Obsidian folder views MUST NOT become the authority for interpreting governed files.

Codex MAY inspect folder structure for conformance support.

Codex folder inspection MUST NOT become the authority for interpreting governed files.

Folder Mapping SHOULD be documented clearly enough that a future human, Codex agent, Obsidian user, workflow, validator, repository maintainer, or downstream implementer can determine:

- where governed documents belong;
- where implementation profiles belong;
- where Knowledge Records belong;
- where Source Material belongs;
- where draft material belongs;
- where review material belongs;
- where archive material belongs;
- where import material belongs;
- where export material belongs;
- where backup material belongs;
- where migration material belongs;
- where generated material belongs;
- where implementation-support material belongs;
- what folder placement means;
- what folder placement does not mean;
- what material requires validation;
- what material requires review;
- what material requires privacy handling;
- what material is safe for Codex to inspect;
- what material must not be exposed by Obsidian, sync tools, exports, plugins, indexes, or agents.

Folder Mapping is successful when the implementation is easy to navigate without allowing folders, vault paths, repository paths, graph views, backlinks, tags, generated indexes, caches, or tool-specific organization to redefine The Brain Standard.

## 8. Metadata Representation

Metadata Representation defines how metadata may be written, displayed, preserved, inspected, validated, and supported in the Obsidian and Codex implementation environment.

Metadata Representation exists so that metadata remains usable in Markdown while preserving the meaning defined by the Knowledge Standards.

IMP-0001 MAY define practical metadata representation choices.

IMP-0001 MUST NOT redefine metadata meaning.

The meaning of metadata remains governed by the applicable Knowledge Standards, specifications, workflows, and higher-authority documents.

Metadata in this implementation SHOULD remain:

- explicit;
- human-readable;
- AI-readable;
- portable;
- inspectable;
- reviewable;
- compatible with validation;
- compatible with migration;
- compatible with plain-text use;
- compatible with Obsidian;
- compatible with Codex inspection;
- independent of hidden application state.

Metadata MAY be represented through:

- document header fields;
- Markdown-compatible fields;
- front matter where later specified;
- structured sections;
- tables;
- sidecar files where later specified;
- implementation-support files where appropriate;
- validation reports where appropriate;
- future governed metadata specifications.

The representation method MUST NOT define metadata meaning by itself.

A metadata field MUST NOT be treated as valid standard metadata merely because Obsidian displays it.

A metadata field MUST NOT be treated as valid standard metadata merely because Codex generated it.

A metadata field MUST NOT be treated as valid standard metadata merely because a plugin stores it.

A metadata field MUST NOT be treated as valid standard metadata merely because a script, validator, index, cache, graph view, database, or template uses it.

A compliant metadata representation MUST preserve the distinction between:

- standard metadata;
- implementation metadata;
- workflow metadata;
- agent-generated metadata;
- validation metadata;
- presentation metadata;
- storage metadata;
- generated metadata;
- temporary metadata;
- private operational notes.

Metadata SHOULD support Object Identity without becoming confused with Object Identity.

A title, filename, path, alias, tag, backlink, graph node, plugin identifier, database row, script output, Codex-generated label, Obsidian property, or implementation-specific value MUST NOT be treated as Stable Object Identity unless a governed standard or specification explicitly defines that role.

Metadata SHOULD support relationships without replacing relationship records.

A tag, backlink, graph edge, folder proximity, filename similarity, search result, plugin relation, generated index, or Codex suggestion MUST NOT be treated as a governed relationship unless the relationship is explicit, reviewable, and compliant with the applicable Relationship Standard.

Metadata SHOULD support Source References and provenance without replacing them.

A citation string, file path, URL, link, attachment, generated summary, extraction note, or Codex output MAY support source-reference and provenance handling.

However, it MUST NOT replace governed Source Reference or provenance expectations where those expectations affect meaning, authority, privacy, validation, lifecycle state, relationships, compatibility, import, export, migration, or downstream use.

Metadata SHOULD support Lifecycle State without confusing lifecycle state with folder placement, workflow state, implementation state, or user-interface state.

Metadata SHOULD support Authority Level without confusing authority with approval, search ranking, graph centrality, agent confidence, source popularity, workflow completion, or implementation visibility.

Metadata SHOULD support Privacy Classification without confusing privacy with folder placement, local-only storage, lack of sharing, hidden files, plugin visibility, sync exclusion, or agent access assumptions.

Metadata SHOULD support Validation without confusing validation support with approval.

A validator output, Codex review, script result, checklist result, Obsidian display, or workflow completion MUST NOT be treated as approval unless a governed workflow or standard explicitly defines that authority.

The Obsidian implementation MAY display metadata for usability.

Obsidian metadata display SHOULD help humans inspect governed files.

Obsidian metadata display MUST NOT hide metadata that affects identity, meaning, provenance, lifecycle state, authority, privacy, validation, compatibility, or downstream use.

Obsidian metadata display MUST NOT require hidden plugin state for understanding governed meaning.

Codex MAY inspect, propose, normalize, or report metadata issues.

Codex MAY assist with metadata consistency.

Codex MUST distinguish proposed metadata from approved metadata.

Codex MUST NOT silently overwrite metadata that affects identity, provenance, lifecycle state, authority, privacy, validation, relationships, source references, publication, export, migration, or downstream use.

Codex MUST NOT silently create metadata that changes governed meaning unless the applicable permission, workflow, validation, review, and approval requirements are satisfied.

Metadata templates MAY exist.

Metadata templates SHOULD reduce repetitive work.

Metadata templates MUST NOT create approval by being used.

Metadata templates MUST NOT create authority by being used.

Metadata templates MUST NOT create validation success by being used.

Metadata templates MUST NOT override higher-authority metadata standards.

Future metadata specifications MAY define exact fields, syntax, allowed values, front matter rules, validation rules, schemas, serialization formats, or object-type-specific metadata profiles.

Until such specifications exist, IMP-0001 SHOULD use simple, explicit, readable metadata conventions that preserve the meaning of the existing standards without pretending to be a complete schema.

Metadata Representation is successful when a future human, Obsidian user, Codex agent, validator, workflow, migration process, export process, or downstream implementation can determine:

- what metadata exists;
- what the metadata means;
- what standard governs the metadata;
- what metadata is required;
- what metadata is recommended;
- what metadata is optional;
- what metadata was proposed by an agent;
- what metadata was generated by a tool;
- what metadata requires review;
- what metadata affects privacy;
- what metadata affects authority;
- what metadata affects validation;
- what metadata affects lifecycle state;
- what metadata affects Source References or provenance;
- what metadata affects relationships;
- what metadata must survive migration;
- what metadata is implementation-specific and non-authoritative.

## 9. Knowledge Record and Source Material Handling

Knowledge Record and Source Material Handling defines how the Obsidian and Codex implementation environment should work with structured knowledge and original source artifacts.

This section exists to preserve the distinction between Source Material and Knowledge Records during practical use.

Source Material is not a Knowledge Record merely because it is stored in the repository, opened in Obsidian, processed by Codex, linked from a note, indexed, summarized, copied, backed up, synchronized, or placed in a folder.

A Knowledge Record is not Source Material merely because it references, quotes, summarizes, extracts from, interprets, transforms, or depends on Source Material.

The implementation MUST preserve the distinction between:

- original Source Material;
- extracted content;
- summarized content;
- interpreted content;
- transformed content;
- synthesized knowledge;
- Draft Knowledge Records;
- reviewed Knowledge Records;
- Approved Knowledge Records;
- rejected records;
- archived records;
- generated outputs;
- validation reports;
- workflow outputs;
- agent outputs;
- implementation-support files.

Obsidian MAY be used to view, edit, navigate, and review Knowledge Records.

Obsidian MAY be used to link Knowledge Records to relevant Source Material.

Obsidian MAY help humans inspect source context.

Obsidian MUST NOT convert Source Material into a Knowledge Record merely by linking, previewing, embedding, tagging, displaying, graphing, or indexing it.

Obsidian MUST NOT convert a Knowledge Record into approved knowledge merely by placing it in a folder, linking it, tagging it, displaying it, or including it in a graph view.

Codex MAY assist with Source Material handling where permitted.

Codex MAY inspect Source Material where privacy classification, agent permissions, and workflow rules allow access.

Codex MAY summarize Source Material.

Codex MAY extract candidate knowledge from Source Material.

Codex MAY propose Knowledge Records from Source Material.

Codex MAY propose metadata, Source References, provenance, relationships, lifecycle states, authority levels, privacy classifications, and validation findings.

Codex MUST distinguish Source Material from extracted content.

Codex MUST distinguish extracted content from interpreted content.

Codex MUST distinguish interpreted content from synthesized knowledge.

Codex MUST distinguish generated summaries from Knowledge Records.

Codex MUST distinguish Draft Knowledge Records from reviewed or Approved Knowledge Records.

Codex MUST preserve Source References and provenance when creating or proposing source-derived Knowledge Records.

Codex MUST NOT treat a generated summary, extraction, classification, transformation, or draft as approved knowledge unless the applicable ingestion, review, validation, authority, privacy, and workflow requirements are satisfied.

Knowledge Records SHOULD be stored in the appropriate Knowledge Record area defined by the storage layout.

Source Material SHOULD be stored, staged, archived, referenced, or restricted according to the applicable storage, privacy, workflow, source-reference, and provenance expectations.

Source Material SHOULD remain available for review where practical.

Where Source Material is unavailable, restricted, external, deleted, corrupted, superseded, incomplete, or uncertain, the Knowledge Record SHOULD preserve enough source-reference and provenance context for future review.

Knowledge Records SHOULD include or support metadata sufficient to preserve:

- Object Identity;
- title or label;
- record type where applicable;
- lifecycle state;
- authority level;
- privacy classification;
- validation state or validation expectations;
- Source References where applicable;
- provenance where applicable;
- relationships where applicable;
- review status where applicable;
- created or updated context where applicable;
- implementation limitations where applicable.

Source Material SHOULD include or support handling information sufficient to preserve:

- source identity or source identifier where applicable;
- source location;
- source availability;
- source privacy;
- source provenance;
- source reliability notes where applicable;
- source authority notes where applicable;
- import context where applicable;
- extraction context where applicable;
- transformation context where applicable;
- review context where applicable;
- restriction or quarantine context where applicable.

Knowledge Record creation SHOULD follow the Knowledge Ingestion Workflow where the record is created from incoming material, captured information, source files, notes, documents, messages, datasets, media, observations, or other inputs.

Knowledge Record review SHOULD follow the Review and Approval Workflow where the record affects governed meaning, authority, lifecycle state, privacy, validation, relationships, Source References, provenance, publication, export, migration, or downstream use.

Knowledge Record maintenance SHOULD follow the Knowledge Maintenance and Update Workflow where the record becomes stale, incorrect, incomplete, superseded, deprecated, invalid, privacy-sensitive, source-unsupported, or otherwise in need of correction.

Knowledge Record publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream use SHOULD follow the Publication, Export, and Downstream Use Workflow where applicable.

The implementation SHOULD avoid storing the only meaningful copy of Source Material inside a generated cache, plugin database, hidden folder, temporary download location, chat transcript, Codex memory, agent memory, or external system without a governed Source Reference or provenance record.

The implementation SHOULD avoid storing the only meaningful copy of a Knowledge Record inside Obsidian plugin state, Codex output, generated indexes, generated summaries, validator reports, graph artifacts, or undocumented implementation-support files.

A Knowledge Record SHOULD remain readable as Markdown where practical.

Source Material MAY exist in many formats.

Where Source Material cannot be represented directly in Markdown, the implementation SHOULD preserve a readable reference, provenance context, storage location, privacy classification, and review path.

Knowledge Records and Source Material MUST be handled according to privacy classification.

Restricted Source Material MUST NOT be exposed to Obsidian sync, Codex, plugins, exports, generated indexes, graph views, embeddings, summaries, public folders, or downstream users unless permitted by the applicable privacy classification and workflow review.

Knowledge Records derived from restricted Source Material SHOULD preserve privacy boundaries even when the record does not reproduce the full source.

Source-derived Knowledge Records SHOULD not weaken source privacy merely by summarizing, paraphrasing, extracting, transforming, or classifying restricted material.

Knowledge Record and Source Material Handling is successful when a future human, Obsidian user, Codex agent, validator, workflow, migration process, export process, or downstream implementation can determine:

- what material is Source Material;
- what material is a Knowledge Record;
- what material is a draft;
- what material is reviewed;
- what material is approved;
- what material is generated;
- what source supports a Knowledge Record;
- what provenance applies;
- what privacy boundary applies;
- what validation expectations apply;
- what review remains required;
- what agent actions were involved;
- what workflow produced or changed the record;
- what may be exported;
- what must remain restricted;
- what remains non-conformant.

## 10. Agent and Subagent Use in Obsidian and Codex

Agent and Subagent Use defines how Codex, supporting agents, scripts, validators, prompts, automations, and future agent-like tools may operate inside the Obsidian and Codex implementation environment.

Agent and subagent use exists to reduce manual burden while preserving governance, reviewability, privacy, traceability, authority boundaries, validation boundaries, and implementation independence.

The implementation MAY assign agent or subagent responsibilities based on the Agent Standards.

Agent and subagent responsibilities MAY include:

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
- validator support;
- script support;
- template support;
- repository inspection support;
- Obsidian setup support;
- Codex setup support.

Agent role assignment MUST NOT create permission by itself.

Agent role assignment MUST NOT create approval authority by itself.

Agent role assignment MUST NOT create publication authority by itself.

Agent role assignment MUST NOT create export authority by itself.

Agent role assignment MUST NOT create migration authority by itself.

Agent role assignment MUST NOT create deletion authority by itself.

Agent role assignment MUST NOT create privacy clearance by itself.

Agent role assignment MUST NOT create lifecycle-transition authority by itself.

Agent role assignment MUST NOT create validation acceptance by itself.

An agent role defines responsibility.

An agent permission defines allowed action.

An agent output defines a produced result.

An agent review defines inspection or evaluation.

An agent validation result defines a scoped validation finding.

None of these alone define approval, authority, lifecycle transition, privacy clearance, publication readiness, export readiness, migration permission, deletion permission, downstream-use permission, or governance acceptance unless a governed workflow or future specification explicitly defines that effect within a controlled scope.

Codex MAY act as an implementation-support agent.

Codex MAY perform multiple agent-support functions during a single work session where the scope is explicit and the action remains reviewable.

Codex SHOULD identify which role or support function it is performing when role distinction materially affects interpretation.

Codex SHOULD distinguish between:

- syntax inspection;
- standards validation support;
- metadata proposal;
- relationship proposal;
- Source Reference and provenance review;
- privacy review support;
- workflow routing support;
- duplicate and identity review;
- handoff preparation;
- implementation support;
- validation support;
- editing support;
- repository support.

Codex MUST NOT silently combine agent roles in a way that hides responsibility, bypasses review, weakens traceability, or creates hidden authority.

A Syntax Inspector MAY identify Markdown syntax issues, heading issues, malformed lists, broken code fences, formatting inconsistencies, spelling concerns, grammar concerns, duplicate headings, section-order issues, and visible structural defects.

A Syntax Inspector MUST NOT approve content meaning by itself.

A Standards Validator MAY compare material against applicable standards, identify possible conformance issues, identify missing dependencies, identify conflicting rules, identify redundant definitions, and recommend correction.

A Standards Validator MUST NOT approve a file by itself.

A Metadata Agent MAY inspect, propose, normalize, or flag metadata.

A Metadata Agent MUST NOT create approved metadata by itself.

A Relationship Agent MAY identify possible relationships, missing relationship context, duplicate relationship meaning, or relationship ambiguity.

A Relationship Agent MUST NOT create governed relationships by inference alone.

A Source and Provenance Agent MAY inspect Source References, provenance context, evidence support, attribution, transformation history, import context, export context, migration context, and source availability.

A Source and Provenance Agent MUST NOT treat citation syntax, links, attachments, file paths, summaries, or generated notes as sufficient provenance by themselves where governed provenance is required.

A Privacy Agent MAY inspect privacy classification, exposure risk, restricted material, synchronization risk, export risk, publication risk, indexing risk, plugin risk, agent-access risk, and downstream-use risk.

A Privacy Agent MUST NOT clear restricted material for exposure by itself unless a governed workflow or future specification explicitly grants that authority within a controlled scope.

A Workflow Agent MAY route work through ingestion, review and approval, maintenance and update, publication, export, downstream-use, implementation, or non-conformance workflows.

A Workflow Agent MUST NOT treat workflow routing as workflow completion.

A Duplicate and Identity Agent MAY inspect possible duplicates, identity conflicts, renamed files, copied files, split records, merged records, superseded records, deprecated records, redirects, aliases, and identity ambiguity.

A Duplicate and Identity Agent MUST NOT assign or change stable Object Identity without the applicable review and governance process.

A Handoff Agent MAY prepare handoff summaries, section counts, next steps, open issues, unresolved risks, and continuation instructions.

A Handoff Agent MUST NOT convert a handoff summary into approval, authority, validation acceptance, or lifecycle transition by itself.

An Implementation Agent MAY assist with Obsidian setup, Codex setup, local folder organization, repository layout, templates, scripts, validators, README files, operational guides, setup checklists, backup support, export support, and recovery support.

An Implementation Agent MUST NOT redefine The Brain Standard.

Agents and subagents MAY use Obsidian-visible files for navigation and context.

Agents and subagents MUST NOT treat Obsidian display state, graph state, backlinks, tags, plugin output, or folder placement as governed authority by itself.

Agents and subagents MAY use Codex-accessible repository files for inspection and implementation support.

Agents and subagents MUST NOT treat Codex access, tool capability, model confidence, prior success, generated summaries, local memory, hidden state, or convenience as permission.

Agent activity SHOULD be traceable.

Traceability SHOULD record or preserve:

- what agent role or support function was used;
- what files were inspected;
- what files were compared;
- what Source Material was accessed;
- what Knowledge Records were affected;
- what standards were used;
- what output was produced;
- what assumptions were made;
- what changes were proposed;
- what changes were applied where authorized;
- what permission scope applied;
- what review remains required;
- what risks or ambiguities remain;
- what escalation is required.

Agent and subagent outputs SHOULD be labeled or handled according to their status.

Possible output statuses MAY include:

- proposed;
- draft;
- generated;
- review-needed;
- validation-support;
- non-conformance finding;
- escalation-needed;
- applied-with-authorization;
- rejected;
- superseded;
- archived.

Agent and subagent use MUST preserve privacy classification.

Agents MUST NOT access, summarize, index, export, publish, synchronize, or expose restricted material unless the applicable privacy classification, permission scope, workflow, and review requirements permit it.

Agent and subagent use is successful when Codex, Obsidian-support tools, scripts, validators, prompts, automations, and future agents can assist The Brain without becoming hidden governance, hidden approval, hidden authority, hidden memory, hidden metadata, hidden relationships, hidden validation, hidden privacy clearance, or hidden implementation lock-in.

## 11. Workflow Execution in the Implementation

Workflow Execution defines how the Obsidian and Codex implementation environment supports governed workflows in practical use.

Workflow Execution exists so that ingestion, review, approval, maintenance, update, publication, export, downstream use, implementation work, and non-conformance routing can occur without allowing tools, folders, agents, generated outputs, or convenience behaviors to replace workflow authority.

The implementation MAY support the following governed workflows:

- Knowledge Ingestion Workflow;
- Review and Approval Workflow;
- Knowledge Maintenance and Update Workflow;
- Publication, Export, and Downstream Use Workflow;
- implementation-profile workflow support;
- non-conformance routing;
- repair routing;
- escalation routing;
- archival routing;
- recovery routing;
- future governed workflows.

Obsidian MAY support workflow execution by helping humans:

- open workflow candidates;
- inspect draft files;
- inspect Source Material;
- inspect Knowledge Records;
- inspect metadata;
- inspect Source References;
- inspect provenance;
- inspect relationships;
- inspect validation findings;
- inspect review notes;
- inspect lifecycle state;
- inspect authority level;
- inspect privacy classification;
- follow links;
- search for related material;
- navigate folders;
- use checklists;
- prepare review notes;
- prepare export candidates;
- prepare archival candidates.

Obsidian workflow support MUST NOT replace workflow authority.

Obsidian workflow support MUST NOT treat visibility, links, backlinks, tags, graph views, folder placement, plugin states, or local notes as review completion, approval, validation acceptance, publication readiness, export readiness, migration readiness, or downstream-use readiness by themselves.

Codex MAY support workflow execution by helping humans or authorized workflows:

- inspect files;
- compare files;
- identify missing metadata;
- identify missing Source References;
- identify missing provenance;
- identify relationship issues;
- identify lifecycle issues;
- identify authority issues;
- identify privacy issues;
- identify validation issues;
- identify duplicate or identity conflicts;
- identify repository placement issues;
- identify workflow routing issues;
- draft workflow reports;
- draft repair recommendations;
- draft handoff summaries;
- draft implementation-support files;
- draft validation-support reports.

Codex workflow support MUST NOT replace workflow authority.

Codex workflow support MUST NOT treat generation, summarization, classification, extraction, comparison, validation assistance, routing recommendation, or confidence as review completion, approval, validation acceptance, publication readiness, export readiness, migration readiness, or downstream-use readiness by itself.

The Knowledge Ingestion Workflow SHOULD be used when incoming material, Source Material, notes, documents, media, datasets, messages, transcripts, external references, scans, code files, logs, or other inputs may become Knowledge Records or support Knowledge Records.

Ingestion support MAY include:

- intake;
- staging;
- classification;
- source preservation;
- extraction;
- transformation;
- draft Knowledge Record creation;
- metadata proposal;
- Source Reference proposal;
- provenance proposal;
- relationship proposal;
- privacy classification proposal;
- validation support;
- review routing;
- repair routing;
- rejection routing;
- quarantine routing;
- archival routing.

Ingestion workflow support MUST preserve the distinction between incoming material, Source Material, extracted content, summarized content, interpreted content, transformed content, draft Knowledge Records, approved Knowledge Records, rejected candidates, quarantined material, workflow outputs, agent outputs, and implementation artifacts.

The Review and Approval Workflow SHOULD be used when governed material affects meaning, authority, lifecycle state, privacy, validation, relationships, Source References, provenance, publication, export, migration, or downstream use.

Review and approval support MAY include:

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
- approval decision support;
- rejection decision support;
- repair routing;
- escalation routing;
- quarantine routing;
- archival routing;
- supersession routing;
- deprecation routing;
- workflow logging.

Review support MUST remain distinguishable from approval.

Approval MUST remain scoped, reviewable, and governed.

The Knowledge Maintenance and Update Workflow SHOULD be used when governed material becomes stale, incorrect, incomplete, superseded, deprecated, invalid, privacy-sensitive, source-unsupported, duplicated, conflicting, non-conformant, or otherwise in need of correction.

Maintenance support MAY include:

- issue detection;
- update candidate identification;
- source re-checking;
- dependency review;
- relationship review;
- metadata review;
- lifecycle review;
- authority review;
- privacy review;
- validation re-checking;
- repair drafting;
- supersession support;
- deprecation support;
- archival support;
- compatibility review.

Maintenance workflow support MUST NOT silently rewrite history, erase provenance, weaken source traceability, remove review context, bypass privacy handling, or convert old material into corrected material without review where review is required.

The Publication, Export, and Downstream Use Workflow SHOULD be used when material may be published, exported, synchronized externally, migrated, shared, copied to another environment, indexed for external use, exposed to downstream systems, used by external agents, or packaged for another person or machine.

Publication, export, and downstream-use support MAY include:

- candidate identification;
- privacy review;
- authority review;
- lifecycle review;
- validation review;
- Source Reference review;
- provenance review;
- relationship review;
- compatibility review;
- export packaging;
- migration support;
- downstream-use limitation notes;
- publication limitation notes;
- restricted-material exclusion;
- export logs;
- handoff preparation.

Publication, export, synchronization, migration, and downstream-use support MUST NOT create permission by itself.

Workflow Execution SHOULD preserve workflow evidence.

Workflow evidence MAY include:

- source files inspected;
- records created;
- records changed;
- metadata proposed;
- metadata changed;
- relationships proposed;
- relationships changed;
- Source References proposed;
- provenance created;
- validation findings;
- review notes;
- approval scope;
- rejection rationale;
- repair actions;
- escalation rationale;
- agent outputs;
- human decisions;
- implementation limitations;
- unresolved risks.

The implementation MAY use folders, tags, checklists, reports, templates, scripts, validator outputs, Obsidian views, Codex summaries, or generated files to support workflow execution.

These support mechanisms MUST NOT become the workflow authority unless a governed workflow or future specification explicitly defines that effect within a controlled scope.

Workflow Execution is successful when a future human, Obsidian user, Codex agent, workflow, validator, repository maintainer, migration process, export process, or downstream implementation can determine:

- what workflow applies;
- what workflow step occurred;
- what material entered the workflow;
- what material left the workflow;
- what Source Material was used;
- what Knowledge Records were created or changed;
- what metadata was proposed or changed;
- what relationships were proposed or changed;
- what Source References and provenance apply;
- what validation was performed;
- what review occurred;
- what approval was granted, if any;
- what approval scope applies;
- what was rejected;
- what was repaired;
- what was escalated;
- what was archived;
- what remains unresolved;
- what may be used downstream;
- what must remain restricted;
- what remains non-conformant.

## 12. Validation and Review Support

Validation and Review Support defines how the Obsidian and Codex implementation environment may help determine whether governed material satisfies applicable standards, specifications, workflows, implementation profiles, deployment-readiness expectations, and review requirements.

Validation and Review Support exists to make conformance easier to inspect without confusing validation support with approval.

Validation support MAY be performed by:

- humans;
- Codex;
- scripts;
- validators;
- checklists;
- templates;
- Obsidian-assisted inspection;
- repository comparison;
- workflow outputs;
- agent outputs;
- implementation-support reports;
- future governed validation tools.

Validation support MAY inspect:

- Markdown syntax;
- heading structure;
- section sequence;
- metadata presence;
- metadata consistency;
- Object Identity support;
- relationship structure;
- Source Reference presence;
- provenance presence;
- lifecycle state;
- authority level;
- privacy classification;
- validation state;
- dependency references;
- related-document references;
- storage placement;
- folder mapping;
- agent permissions;
- agent traceability;
- workflow routing;
- review status;
- approval scope;
- publication readiness;
- export readiness;
- migration readiness;
- synchronization readiness;
- backup readiness;
- recovery readiness;
- implementation-profile conformance;
- deployment-readiness conformance.

Validation support MUST remain distinguishable from validation acceptance.

Validation support MUST remain distinguishable from approval.

Validation support MUST remain distinguishable from authority assignment.

Validation support MUST remain distinguishable from privacy clearance.

Validation support MUST remain distinguishable from lifecycle transition.

Validation support MUST remain distinguishable from publication permission.

Validation support MUST remain distinguishable from export permission.

Validation support MUST remain distinguishable from migration permission.

Validation support MUST remain distinguishable from downstream-use permission.

A passing syntax check does not approve content.

A passing spelling check does not approve content.

A passing grammar check does not approve content.

A passing heading-order check does not approve content.

A passing metadata-presence check does not approve metadata meaning.

A passing relationship-format check does not approve relationship meaning.

A passing Source Reference check does not approve source sufficiency by itself.

A passing provenance check does not approve the governed entity by itself.

A passing privacy check does not create publication permission by itself.

A passing export check does not create export approval by itself.

A passing implementation-profile check does not make the implementation complete by itself.

A passing deployment-readiness check does not make the deployment package mature, public, unrestricted, or downstream-ready by itself.

Obsidian MAY support validation and review by helping humans inspect files, links, backlinks, metadata displays, folder placement, visible structure, search results, graph views, review checklists, and local organization.

Obsidian validation support MUST NOT depend on hidden plugin state where governed meaning, reviewability, migration, compatibility, or long-term preservation is affected.

Obsidian review support MUST NOT convert visibility into approval.

Codex MAY support validation and review by comparing files, identifying inconsistencies, checking syntax, checking section counts, checking dependencies, checking metadata, identifying possible redundancy, identifying possible conflicts, proposing repairs, drafting review summaries, and preparing handoff summaries.

Codex validation support MUST NOT convert agent confidence into approval.

Codex validation support MUST NOT convert repeated successful behavior into permission.

Codex validation support MUST NOT convert generated reports into governance decisions.

Codex review support MUST NOT replace human review where human review is required.

Validators and scripts MAY exist.

Validators and scripts SHOULD be transparent enough that future humans, agents, repository maintainers, and implementers can determine:

- what rule was checked;
- what standard governed the rule;
- what files were checked;
- what result was produced;
- what evidence supports the result;
- what limitations apply;
- what false positives are possible;
- what false negatives are possible;
- what review remains required.

Validator outputs MAY include:

- pass results;
- fail results;
- warnings;
- informational findings;
- missing-field findings;
- structural findings;
- dependency findings;
- privacy findings;
- authority findings;
- lifecycle findings;
- relationship findings;
- Source Reference findings;
- provenance findings;
- implementation findings;
- workflow findings;
- export findings;
- migration findings;
- recovery findings.

Validator outputs MUST remain traceable to the rule, standard, file, scope, date or review context, and tool or agent that produced them where practical.

Validator outputs MUST NOT silently modify governed files unless the applicable permission, workflow, review, and approval requirements are satisfied.

Review support MAY include:

- review checklists;
- review notes;
- comparison reports;
- non-conformance reports;
- repair recommendations;
- escalation notes;
- approval-scope notes;
- rejection rationale;
- section counts;
- dependency checks;
- source-reference checks;
- privacy checks;
- authority checks;
- lifecycle checks;
- validation reports;
- handoff summaries.

Review support MUST distinguish between:

- not reviewed;
- review needed;
- under review;
- reviewed with warnings;
- reviewed with errors;
- repaired;
- approved;
- rejected;
- escalated;
- quarantined;
- superseded;
- deprecated;
- archived.

Review support MUST preserve approval scope where approval exists.

Approval MUST NOT be generalized beyond the reviewed scope.

Approval of syntax MUST NOT imply approval of meaning.

Approval of metadata format MUST NOT imply approval of metadata correctness.

Approval of a Knowledge Record MUST NOT imply approval of unrestricted export.

Approval of an implementation profile MUST NOT imply approval of all future implementations.

Approval of a workflow output MUST NOT imply approval of downstream use unless the applicable workflow explicitly grants that effect.

Validation and review records SHOULD remain inspectable.

Validation and review records SHOULD preserve:

- reviewer or reviewing agent where applicable;
- review date or review context where applicable;
- reviewed file or entity;
- review scope;
- applicable standards;
- applicable workflow;
- findings;
- warnings;
- errors;
- repair actions;
- unresolved risks;
- approval decision where applicable;
- approval scope where applicable;
- rejection decision where applicable;
- escalation route where applicable;
- remaining next steps.

Validation and Review Support is successful when a future human, Obsidian user, Codex agent, validator, workflow, repository maintainer, migration process, export process, or downstream implementation can determine:

- what was checked;
- why it was checked;
- what standard governed the check;
- what result was produced;
- what evidence supports the result;
- whether the result is current;
- whether the result is partial;
- whether the result requires review;
- whether approval exists;
- what approval scope applies;
- what errors remain;
- what warnings remain;
- what repairs are required;
- what escalation is required;
- what may proceed;
- what must not proceed;
- what remains non-conformant.

## 13. Backup, Synchronization, and Recovery

Backup, Synchronization, and Recovery defines how the Obsidian and Codex implementation environment preserves governed material, protects privacy, supports restoration, and avoids confusing operational copies with governed authority.

Backup exists to preserve recoverable copies of governed and implementation-support material.

Synchronization exists to keep authorized working copies aligned across approved devices, repositories, vaults, or environments.

Recovery exists to restore material after deletion, corruption, sync failure, migration failure, tool failure, agent error, user error, repository error, local machine failure, or other implementation disruption.

Backup, synchronization, and recovery MUST preserve The Brain Standard.

Backup MUST NOT redefine Object Identity.

Synchronization MUST NOT redefine Object Identity.

Recovery MUST NOT redefine Object Identity.

Backup MUST NOT redefine metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication permission, export permission, migration permission, synchronization permission, indexing permission, agent permission, implementation exposure, or downstream-use readiness.

Synchronization MUST NOT redefine metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication permission, export permission, migration permission, indexing permission, agent permission, implementation exposure, or downstream-use readiness.

Recovery MUST NOT redefine metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication permission, export permission, migration permission, synchronization permission, indexing permission, agent permission, implementation exposure, or downstream-use readiness.

The implementation SHOULD support backup of:

- governed standards;
- implementation profiles;
- operational guides;
- Knowledge Records;
- Source Material where permitted;
- metadata;
- relationships;
- Source References;
- provenance;
- lifecycle context;
- authority context;
- privacy context;
- validation records;
- workflow logs;
- agent traceability records;
- review records;
- approval-scope records;
- implementation-support files;
- templates;
- prompts;
- validators;
- scripts;
- setup instructions;
- handoff summaries;
- non-conformance records;
- recovery instructions.

Backup scope SHOULD be explicit.

Backup scope SHOULD identify:

- what is backed up;
- where it is backed up;
- when it is backed up;
- what tool or process created the backup;
- what privacy classification applies;
- what material must not be backed up to unrestricted locations;
- what material requires encryption, redaction, exclusion, or restricted handling;
- how restoration should occur;
- what validation is required after restoration;
- what review is required after restoration.

Backup MUST preserve privacy classification.

Restricted material MUST NOT be backed up to unauthorized locations.

Restricted material MUST NOT be copied into unrestricted cloud sync, public repositories, shared folders, plugin databases, generated indexes, external automation systems, agent memory, external model contexts, or downstream packages unless the applicable privacy classification and workflow clearance permit it.

Backup copies SHOULD remain distinguishable from active governed files.

Backup copies MUST NOT be treated as newer, more authoritative, approved, published, exported, migrated, synchronized, or downstream-ready merely because they exist.

A backup copy MAY support recovery.

A backup copy MUST NOT replace active governed material without a recovery action that preserves traceability.

Recovery actions SHOULD preserve:

- original file identity where applicable;
- restored file identity where applicable;
- restoration source;
- restoration date or context where applicable;
- reason for recovery;
- affected files;
- affected Source Material;
- affected Knowledge Records;
- affected metadata;
- affected relationships;
- affected Source References;
- affected provenance;
- affected lifecycle state;
- affected authority level;
- affected privacy classification;
- affected validation state;
- affected workflow logs;
- affected agent traceability records;
- review required after recovery;
- validation required after recovery;
- unresolved risks.

Synchronization MAY be used to support work across devices or environments.

Synchronization SHOULD remain controlled.

Synchronization SHOULD preserve:

- repository structure;
- vault structure where applicable;
- governed Markdown files;
- metadata visibility;
- Source References;
- provenance;
- relationship context;
- lifecycle context;
- authority context;
- privacy context;
- validation context;
- workflow logs;
- review context;
- agent traceability;
- implementation-support files where appropriate.

Synchronization MUST NOT expose restricted material without permission.

Synchronization MUST NOT be treated as publication.

Synchronization MUST NOT be treated as export approval.

Synchronization MUST NOT be treated as migration approval.

Synchronization MUST NOT be treated as downstream-use clearance.

Synchronization MUST NOT be treated as backup sufficiency by itself.

Synchronization conflicts SHOULD be handled as reviewable implementation events.

Sync conflicts MAY include:

- competing edits;
- deleted files;
- renamed files;
- duplicate files;
- stale local copies;
- corrupted files;
- partial uploads;
- partial downloads;
- hidden application-state conflicts;
- plugin database conflicts;
- generated cache conflicts;
- file-lock conflicts;
- branch conflicts;
- repository merge conflicts.

Sync conflicts affecting governed meaning MUST be routed for review or repair.

Sync conflicts affecting Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication, export, migration, agent access, implementation exposure, or downstream use MUST NOT be silently resolved by convenience.

Obsidian MAY participate in backup, synchronization, and recovery through local file access, vault configuration, plugins, file history, sync tools, or manual workflows.

Obsidian backup or sync behavior MUST NOT hide governed meaning inside plugin-only state.

Obsidian backup or sync behavior MUST NOT expose restricted material through graph files, cache files, plugin databases, sync logs, search indexes, or attachments unless permitted.

Codex MAY assist with backup, synchronization, and recovery by inspecting files, comparing versions, identifying missing files, identifying conflicts, drafting recovery notes, preparing repair recommendations, and validating restored structure.

Codex MUST NOT restore, delete, overwrite, synchronize, expose, or export governed material unless explicitly authorized within the applicable permission and workflow scope.

Codex MUST NOT treat repository access as recovery authority.

Codex MUST NOT treat file-system capability as backup permission.

Codex MUST NOT treat sync availability as privacy clearance.

Generated caches, indexes, graph artifacts, embeddings, summaries, validator outputs, and reports MAY be backed up where useful.

Generated material SHOULD remain distinguishable from governed source-of-truth material.

Generated material MAY be regenerated where appropriate.

Generated material MUST NOT become the only meaningful copy of governed knowledge, Source Material, metadata, Source References, provenance, relationships, review decisions, approval scope, or privacy classification.

Recovery SHOULD include validation support after restoration.

Post-recovery validation MAY inspect:

- file presence;
- file integrity;
- heading structure;
- metadata presence;
- dependency references;
- Source Reference availability;
- provenance preservation;
- relationship preservation;
- lifecycle state;
- authority level;
- privacy classification;
- validation state;
- workflow logs;
- agent traceability records;
- implementation-support files;
- backup completeness;
- unresolved sync conflicts.

Backup, Synchronization, and Recovery is successful when a future human, Obsidian user, Codex agent, validator, workflow, repository maintainer, migration process, export process, or downstream implementation can determine:

- what was backed up;
- what was synchronized;
- what was restored;
- what source was used for restoration;
- what material remains active;
- what material remains backup-only;
- what material is restricted;
- what privacy classification applies;
- what validation is required;
- what review is required;
- what conflicts remain;
- what files were changed;
- what agent actions occurred;
- what workflow applies;
- what may be used;
- what must not be exposed;
- what remains non-conformant.

## 14. Publication, Export, and Downstream Use in the Implementation

Publication, Export, and Downstream Use defines how the Obsidian and Codex implementation environment prepares material for use beyond its original working context.

Publication means making governed material available to an intended audience.

Export means producing governed material, Source Material, metadata, relationships, Source References, provenance, validation results, workflow outputs, implementation-support files, or packages for use outside the active implementation environment.

Downstream use means any use of governed material by another person, system, agent, vault, repository, implementation, workflow, publication process, migration process, training process, automation process, or external environment.

Publication, export, and downstream use MUST remain governed.

Publication MUST NOT occur merely because material is visible in Obsidian.

Export MUST NOT occur merely because material is copied to an export folder.

Downstream use MUST NOT occur merely because material is searchable, indexed, synchronized, backed up, linked, summarized, or accessible to Codex.

The implementation MUST distinguish between:

- active governed files;
- draft files;
- reviewed files;
- approved files;
- publication candidates;
- export candidates;
- migration candidates;
- synchronization candidates;
- indexing candidates;
- backup candidates;
- implementation-exposure candidates;
- agent-exposure candidates;
- downstream-use candidates;
- cleared packages;
- denied packages;
- restricted packages;
- redacted packages;
- repaired packages;
- quarantined packages;
- archived packages.

Publication candidates SHOULD be reviewed before publication.

Export candidates SHOULD be reviewed before export.

Downstream-use candidates SHOULD be reviewed before downstream use.

Migration candidates SHOULD be reviewed before migration.

Synchronization candidates SHOULD be reviewed before synchronization where privacy, authority, validation, source-reference, provenance, compatibility, implementation exposure, or downstream-use risk exists.

Indexing candidates SHOULD be reviewed before indexing where privacy, access, exposure, search visibility, embeddings, generated summaries, or agent access risk exists.

Backup candidates SHOULD be reviewed where backup location, retention, encryption, privacy, restoration, or exposure risk exists.

Implementation-exposure candidates SHOULD be reviewed before being exposed to tools, plugins, external systems, hosted services, cloud sync, external validators, or non-governed applications.

Agent-exposure candidates SHOULD be reviewed before being exposed to Codex, other agents, external AI tools, local AI systems, automation systems, or downstream agents where privacy or authority risk exists.

A material item SHOULD NOT be published, exported, migrated, synchronized, indexed, backed up, exposed to an implementation, exposed to an agent, or used downstream unless the applicable workflow, privacy classification, authority level, validation expectations, Source References, provenance, review state, approval scope, and compatibility expectations support the action.

Publication, export, and downstream-use decisions SHOULD preserve:

- Object Identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation State;
- review state;
- approval scope;
- clearance scope;
- workflow logs;
- agent traceability;
- implementation limitations;
- downstream-use limitations;
- compatibility context.

Publication, export, and downstream-use decisions MUST be scoped.

A clearance decision for one use MUST NOT automatically permit all future uses.

A clearance decision for one audience MUST NOT automatically permit all audiences.

A clearance decision for one export package MUST NOT automatically permit all export packages.

A clearance decision for one machine MUST NOT automatically permit all machines.

A clearance decision for one repository MUST NOT automatically permit all repositories.

A clearance decision for one vault MUST NOT automatically permit all vaults.

A clearance decision for one agent MUST NOT automatically permit all agents.

A clearance decision for one implementation MUST NOT automatically permit all implementations.

A clearance decision for one downstream user MUST NOT automatically permit all downstream users.

Approval of a governed file MUST NOT be treated as unrestricted publication permission.

Approval of a governed file MUST NOT be treated as unrestricted export permission.

Approval of a governed file MUST NOT be treated as unrestricted migration permission.

Approval of a governed file MUST NOT be treated as unrestricted synchronization permission.

Approval of a governed file MUST NOT be treated as unrestricted indexing permission.

Approval of a governed file MUST NOT be treated as unrestricted backup permission.

Approval of a governed file MUST NOT be treated as unrestricted implementation-exposure permission.

Approval of a governed file MUST NOT be treated as unrestricted agent-exposure permission.

Approval of a governed file MUST NOT be treated as unrestricted downstream-use permission.

Validation success MUST NOT be treated as clearance by itself.

Privacy classification MUST NOT be weakened for operational convenience.

Authority level MUST NOT be treated as permission for broader use without scope review.

Lifecycle state MUST NOT be treated as permission for broader use without review.

Storage placement MUST NOT be treated as permission for broader use.

Implementation visibility MUST NOT be treated as governed permission.

Agent access MUST NOT be treated as privacy clearance, approval, authority, publication permission, export permission, migration permission, synchronization permission, indexing permission, backup permission, implementation-exposure permission, or downstream-use permission.

Obsidian MAY support publication, export, and downstream-use preparation by helping humans inspect files, links, metadata, relationships, Source References, provenance, validation findings, privacy classification, authority level, lifecycle state, and review notes.

Obsidian MUST NOT publish or expose restricted material through plugins, sync services, graph exports, rendered previews, attachments, indexes, cache files, or shared vaults unless the applicable clearance exists.

Codex MAY support publication, export, and downstream-use preparation by identifying candidates, checking dependencies, checking privacy classifications, checking validation findings, preparing package lists, drafting handoff notes, identifying restricted material, identifying missing provenance, identifying unresolved review needs, and preparing export-support scripts where authorized.

Codex MUST NOT publish, export, migrate, synchronize, index, package, expose, or transmit governed material unless explicitly authorized within the applicable workflow and permission scope.

Codex MUST NOT redact material without review where redaction affects meaning, Source References, provenance, privacy, authority, validation, publication, export, migration, or downstream use.

Export packages SHOULD be reviewable.

An export package SHOULD identify:

- package purpose;
- package scope;
- included governed files;
- included Source Material where applicable and permitted;
- excluded restricted material;
- redacted material;
- metadata included;
- relationships included;
- Source References included;
- provenance included;
- validation results included;
- workflow logs included where appropriate;
- approval scope;
- clearance scope;
- privacy limitations;
- downstream-use limitations;
- known implementation limitations;
- known non-conformance;
- package date or context where applicable.

Publication outputs SHOULD preserve enough context for users to understand the authority, scope, limitations, and source support of the published material.

Downstream-use packages SHOULD preserve enough context for downstream users, machines, agents, workflows, validators, or implementations to avoid mistaking exported material for unrestricted, source-free, privacy-free, context-free, authority-free, or approval-free knowledge.

Publication, Export, and Downstream Use in the Implementation is successful when a future human, Obsidian user, Codex agent, validator, workflow, repository maintainer, migration process, export process, publication process, or downstream implementation can determine:

- what was published;
- what was exported;
- what was migrated;
- what was synchronized;
- what was indexed;
- what was backed up;
- what was exposed to an implementation;
- what was exposed to an agent;
- what was cleared for downstream use;
- what was denied;
- what was redacted;
- what was excluded;
- what approval scope applies;
- what clearance scope applies;
- what privacy classification applies;
- what Source References and provenance remain attached;
- what validation results apply;
- what limitations remain;
- what may be reused;
- what must not be reused;
- what remains non-conformant.

## 15. Implementation Limitations and Non-Conformance

Implementation Limitations and Non-Conformance defines how the Obsidian and Codex implementation environment identifies, records, routes, repairs, escalates, or accepts limitations and failures to satisfy The Brain Standard.

An Implementation Limitation is any practical constraint, tool behavior, missing capability, setup weakness, unsupported feature, plugin dependency, automation gap, sync risk, backup weakness, recovery weakness, export weakness, validation gap, privacy risk, agent limitation, repository limitation, Obsidian limitation, Codex limitation, local machine limitation, or workflow limitation that prevents the implementation from fully realizing the applicable standards.

Non-Conformance is any condition where the implementation does not satisfy a mandatory requirement, required boundary, governed workflow, storage expectation, agent permission, traceability expectation, privacy handling expectation, validation expectation, review expectation, backup expectation, synchronization expectation, export expectation, recovery expectation, deployment-readiness expectation, or implementation-profile requirement.

Implementation limitations MAY be acceptable temporarily.

Non-conformance MUST be visible, reviewable, and routed.

A limitation MUST NOT be hidden merely because the implementation remains usable.

A limitation MUST NOT be ignored merely because Obsidian displays files correctly.

A limitation MUST NOT be ignored merely because Codex can work around it.

A limitation MUST NOT be ignored merely because users understand the workaround.

A limitation MUST NOT be ignored merely because a plugin, script, prompt, template, validator, cache, index, graph view, sync tool, backup tool, or generated report makes the limitation less visible.

Non-conformance MAY include:

- missing required metadata;
- inconsistent metadata;
- missing Source References;
- weak provenance;
- unclear relationship meaning;
- duplicate records;
- Object Identity ambiguity;
- lifecycle-state confusion;
- authority-level confusion;
- privacy-classification gaps;
- validation-state gaps;
- approval-scope ambiguity;
- folder placement confusion;
- Source Material mixed with Knowledge Records;
- draft material treated as approved;
- generated material treated as governed source-of-truth;
- Obsidian plugin state treated as governed meaning;
- Codex output treated as approval;
- agent output lacking traceability;
- agent action lacking permission;
- workflow completion confused with approval;
- validation support confused with validation acceptance;
- approval confused with export clearance;
- privacy classification weakened for convenience;
- restricted material exposed to sync, indexing, export, agents, or downstream use;
- backup scope unclear;
- recovery path untested;
- export package incomplete;
- migration context missing;
- implementation-support files redefining standards;
- repository path inconsistency;
- file naming inconsistency;
- missing implementation documentation;
- stale handoff summaries;
- unresolved review notes;
- unresolved warnings;
- unresolved errors.

Implementation limitations SHOULD be recorded when they affect:

- meaning;
- identity;
- metadata;
- relationships;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage layout;
- agent behavior;
- workflow execution;
- reviewability;
- approval scope;
- publication;
- export;
- migration;
- synchronization;
- indexing;
- backup;
- recovery;
- downstream use;
- portability;
- implementation independence;
- long-term maintainability.

A limitation record SHOULD identify:

- limitation summary;
- affected file or area;
- affected standard;
- affected workflow;
- affected implementation component;
- affected privacy classification where applicable;
- affected authority level where applicable;
- affected validation scope where applicable;
- risk level where applicable;
- whether the issue is blocking;
- whether the issue is temporary;
- whether a workaround exists;
- whether review is required;
- whether escalation is required;
- recommended repair;
- responsible actor or role where applicable;
- date or context where applicable;
- remaining next step.

Non-conformance records SHOULD identify:

- non-conformance summary;
- violated requirement or boundary;
- affected governed entity;
- affected implementation component;
- severity where applicable;
- privacy impact where applicable;
- authority impact where applicable;
- validation impact where applicable;
- workflow impact where applicable;
- source-reference impact where applicable;
- provenance impact where applicable;
- downstream-use impact where applicable;
- recommended routing;
- required repair;
- required review;
- required escalation;
- whether work may continue;
- whether work must pause;
- whether material must be quarantined;
- whether material must be excluded from publication or export.

Obsidian MAY help identify implementation limitations through visible folder issues, broken links, missing files, unresolved backlinks, search results, graph anomalies, plugin warnings, sync issues, display problems, or review notes.

Obsidian MUST NOT hide non-conformance behind visual convenience.

Codex MAY help identify implementation limitations through file inspection, repository comparison, syntax checks, dependency checks, metadata checks, relationship checks, Source Reference checks, provenance checks, privacy checks, validation checks, workflow checks, and implementation-profile checks.

Codex MAY propose repair actions.

Codex MUST NOT silently repair non-conformance where the repair affects governed meaning, Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation State, approval, publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream use.

Codex MUST NOT hide non-conformance by rewriting, summarizing, deleting, moving, renaming, redacting, packaging, exporting, or regenerating material without proper permission and review.

Implementation limitations SHOULD be routed according to impact.

Minor implementation limitations MAY be routed to implementation-support repair.

Standards conflicts SHOULD be routed to standards review.

Metadata issues SHOULD be routed to metadata review.

Relationship issues SHOULD be routed to relationship review.

Source Reference or provenance issues SHOULD be routed to source and provenance review.

Privacy issues SHOULD be routed to privacy review or escalation.

Validation issues SHOULD be routed to validation review.

Agent permission or traceability issues SHOULD be routed to agent review.

Workflow issues SHOULD be routed to workflow review.

Storage layout issues SHOULD be routed to storage review.

Publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream-use issues SHOULD be routed to the Publication, Export, and Downstream Use Workflow.

A non-conformance MAY block continuation when it affects:

- Object Identity;
- Source Material preservation;
- source-reference sufficiency;
- provenance sufficiency;
- privacy classification;
- restricted material exposure;
- approval scope;
- export clearance;
- publication clearance;
- migration readiness;
- downstream-use readiness;
- destructive actions;
- data loss;
- unreviewable agent changes;
- hidden implementation state;
- inability to recover;
- inability to validate.

A non-conformance MAY allow continuation with warning when it is documented, scoped, non-destructive, reviewable, repairable, and does not expose restricted material, change governed meaning, weaken Object Identity, bypass approval, or create downstream-use risk.

Implementation limitations and non-conformance SHOULD be reviewed before final deployment, export, migration, publication, downstream use, or handoff to another person or machine.

Implementation Limitations and Non-Conformance is successful when a future human, Obsidian user, Codex agent, validator, workflow, repository maintainer, migration process, export process, or downstream implementation can determine:

- what limitation exists;
- what non-conformance exists;
- what standard is affected;
- what workflow is affected;
- what file or entity is affected;
- what risk exists;
- what repair is needed;
- what review is needed;
- what escalation is needed;
- what may continue;
- what must pause;
- what must be excluded;
- what must be quarantined;
- what must not be exported;
- what must not be published;
- what must not be synchronized;
- what must not be indexed;
- what must not be exposed to agents;
- what must not be used downstream.

## 16. Implementation Readiness Criteria

Implementation Readiness Criteria defines the minimum conditions that must be satisfied before the Obsidian and Codex implementation environment may be treated as ready for controlled use.

Implementation readiness means the environment is usable in a limited, governed, reviewable, and recoverable way.

Implementation readiness does not mean the implementation is mature.

Implementation readiness does not mean the implementation is public.

Implementation readiness does not mean the implementation is unrestricted.

Implementation readiness does not mean all future automation, validators, templates, prompts, plugins, scripts, exports, migrations, publication packages, or downstream-use packages are complete.

Implementation readiness means the Obsidian and Codex environment is structured enough that a future human, Codex agent, Obsidian user, validator, workflow, repository maintainer, or downstream implementer can use it without creating immediate architectural drift.

A minimally ready Obsidian and Codex implementation SHOULD satisfy the following criteria:

- the repository exists;
- the local machine has a working repository copy;
- the Obsidian vault or vault-like workspace can open the governed Markdown files;
- Codex can inspect the authorized repository or working directory;
- governed standards are locatable;
- implementation profile files are locatable;
- Knowledge Records can be separated from Source Material;
- Source Material can be staged, referenced, restricted, archived, or excluded as required;
- draft material can be distinguished from reviewed or approved material;
- implementation-support files can be distinguished from governed source-of-truth files;
- generated files can be distinguished from governed source-of-truth files;
- backup, synchronization, recovery, export, migration, and downstream-use boundaries are visible;
- privacy classification can be preserved;
- validation support can be performed;
- review requirements can be identified;
- non-conformance can be recorded and routed.

A minimally ready implementation SHOULD include or support:

- repository structure;
- vault opening guidance;
- folder mapping guidance;
- metadata representation guidance;
- Knowledge Record handling guidance;
- Source Material handling guidance;
- Codex operating boundaries;
- Obsidian operating boundaries;
- agent and subagent use boundaries;
- workflow execution support;
- validation and review support;
- backup expectations;
- synchronization expectations;
- recovery expectations;
- export expectations;
- downstream-use expectations;
- implementation limitation handling;
- non-conformance handling;
- next-step handoff context.

The implementation MUST preserve the distinction between controlled use and unrestricted use.

Controlled use MAY include:

- one person;
- one local machine;
- one repository;
- one vault;
- one implementation-development context;
- one governed review path;
- one limited Codex working scope;
- one limited Obsidian working scope.

Controlled use MUST remain bounded by privacy classification, authority level, validation state, lifecycle state, review state, workflow state, source-reference sufficiency, provenance sufficiency, storage boundaries, agent permissions, and downstream-use limits.

A controlled implementation MAY be used to continue building The Brain.

A controlled implementation MAY be used to ingest test material where privacy and workflow rules permit it.

A controlled implementation MAY be used to draft Knowledge Records where Source References, provenance, metadata, review state, and validation expectations remain visible.

A controlled implementation MAY be used to develop validators, scripts, templates, prompts, setup notes, operational guides, and repository-support files.

A controlled implementation MAY be used to prepare future deployment packages.

A controlled implementation MUST NOT be treated as unrestricted public release.

A controlled implementation MUST NOT be treated as unrestricted export clearance.

A controlled implementation MUST NOT be treated as unrestricted downstream-use clearance.

A controlled implementation MUST NOT be treated as unrestricted agent-access clearance.

A controlled implementation MUST NOT expose restricted Source Material, restricted Knowledge Records, restricted metadata, restricted relationships, restricted Source References, restricted provenance, restricted validation results, restricted workflow logs, restricted agent outputs, or restricted implementation-support files unless the applicable privacy classification and workflow clearance permit it.

A minimally ready Obsidian setup SHOULD allow:

- governed Markdown files to be opened;
- standards to be read;
- implementation profiles to be read;
- Knowledge Records to be navigated;
- Source Material references to be inspected where permitted;
- folder structure to be visible;
- links and backlinks to assist discovery without becoming authority;
- graph views to assist exploration without becoming authority;
- metadata to remain visible or inspectable;
- review notes to remain visible or inspectable;
- local-first work to continue where practical.

A minimally ready Obsidian setup MUST NOT require hidden plugin state for governed meaning.

A minimally ready Obsidian setup MUST NOT require graph views, backlinks, tags, properties, databases, sync state, or rendered previews to interpret governed meaning.

A minimally ready Codex setup SHOULD allow:

- repository inspection;
- file comparison;
- syntax checking;
- spelling and grammar support;
- section-count checking;
- dependency checking;
- metadata review support;
- relationship review support;
- Source Reference and provenance review support;
- privacy review support;
- validation support;
- workflow support;
- implementation-support drafting;
- handoff summary preparation;
- non-conformance identification.

A minimally ready Codex setup MUST NOT allow Codex access, model capability, tool capability, confidence, generated summaries, or repeated successful behavior to become permission, approval, authority, privacy clearance, validation acceptance, publication clearance, export clearance, migration clearance, synchronization clearance, backup clearance, implementation-exposure clearance, agent-exposure clearance, or downstream-use clearance.

Implementation readiness SHOULD include a known limitation list.

The limitation list SHOULD identify:

- missing files;
- missing folders;
- missing metadata specifications;
- missing validation specifications;
- missing templates;
- missing prompts;
- missing validators;
- missing backup tests;
- missing recovery tests;
- missing export tests;
- missing migration tests;
- missing Obsidian setup documentation;
- missing Codex setup documentation;
- unresolved repository inconsistencies;
- unresolved spelling or metadata issues;
- unresolved review warnings;
- unresolved non-conformance.

Implementation readiness SHOULD include a next-step statement.

The next-step statement SHOULD identify whether the implementation is ready for:

- continued drafting;
- final review;
- controlled repository creation;
- controlled local deployment;
- validator creation;
- template creation;
- prompt creation;
- operational guide creation;
- test ingestion;
- backup testing;
- recovery testing;
- export testing;
- handoff summary creation;
- another implementation profile.

Implementation Readiness Criteria is successful when a future human, Obsidian user, Codex agent, validator, workflow, repository maintainer, migration process, export process, or downstream implementation can determine whether the implementation may be used, what scope it may be used within, what remains incomplete, what must be repaired, what must not proceed, and what the next milestone should be.

## 17. Conformance Requirements

Conformance Requirements defines what must be true for the Obsidian and Codex implementation profile to conform to The Brain Standard.

IMP-0001 conforms when it realizes prior standards without redefining them.

IMP-0001 MUST remain subordinate to:

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
- DEP-0001 — Bare Usable Deployment Readiness Standard.

IMP-0001 MUST NOT redefine:

- The Brain mission;
- architecture principles;
- layered architecture;
- governance authority;
- Knowledge Object meaning;
- Knowledge Record meaning;
- Source Material meaning;
- Object Identity;
- metadata meaning;
- relationship meaning;
- Source Reference meaning;
- provenance meaning;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage architecture;
- storage layout meaning;
- agent roles;
- agent permissions;
- agent traceability;
- workflow authority;
- review authority;
- approval authority;
- publication clearance;
- export clearance;
- migration clearance;
- synchronization clearance;
- indexing clearance;
- backup clearance;
- implementation-exposure clearance;
- agent-exposure clearance;
- downstream-use clearance;
- deployment readiness.

IMP-0001 MUST preserve implementation independence.

Obsidian MUST remain an implementation interface.

Codex MUST remain an implementation-support agentic environment.

The repository MUST remain a storage and version-control environment.

The local machine MUST remain an operating environment.

Plugins, scripts, validators, templates, prompts, caches, indexes, graph artifacts, generated summaries, rendered previews, search results, sync tools, backup tools, and automation MUST remain subordinate support mechanisms unless a future governed standard or specification explicitly grants a defined role within a controlled scope.

A conforming implementation MUST preserve Object Identity across:

- file movement;
- file renaming;
- folder restructuring;
- vault opening changes;
- repository cloning;
- synchronization;
- backup;
- restoration;
- import;
- export;
- migration;
- indexing;
- cache generation;
- graph generation;
- agent inspection;
- workflow routing;
- implementation replacement.

A conforming implementation MUST preserve metadata as explicit, portable, inspectable, and governed.

A conforming implementation MUST preserve relationships as explicit, reviewable, and governed.

A conforming implementation MUST preserve Source References and provenance where source support, evidence, transformation, agent activity, workflow activity, import, export, migration, review, validation, or change history affects meaning, authority, privacy, lifecycle state, compatibility, or downstream use.

A conforming implementation MUST preserve Lifecycle State as explicit and governed.

A conforming implementation MUST preserve Authority Level as explicit, scoped, and governed.

A conforming implementation MUST preserve Privacy Classification as explicit, scoped, and governed.

A conforming implementation MUST preserve Validation State and validation results as scoped, reviewable, and distinguishable from approval.

A conforming implementation MUST preserve agent boundaries.

Agent roles MUST NOT create permission by themselves.

Agent outputs MUST NOT create approval by themselves.

Agent confidence MUST NOT create authority by itself.

Agent access MUST NOT create privacy clearance by itself.

Agent-generated summaries MUST NOT become Knowledge Records without the applicable ingestion, metadata, Source Reference, provenance, validation, and review requirements.

Agent activity MUST remain traceable where it affects governed material or governed handling.

A conforming implementation MUST preserve workflow boundaries.

Workflow support MUST NOT become workflow authority by itself.

Workflow routing MUST NOT become workflow completion by itself.

Workflow completion MUST NOT become approval unless the applicable governed workflow explicitly defines that effect within a controlled scope.

Review support MUST NOT become approval by itself.

Validation support MUST NOT become validation acceptance by itself.

Approval MUST remain scoped.

Publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, and downstream use MUST remain cleared only within their applicable scope.

A conforming implementation MUST preserve storage boundaries.

Folder placement MUST NOT define Object Identity by itself.

Folder placement MUST NOT define lifecycle state, authority level, privacy classification, validation state, relationship meaning, Source Reference meaning, provenance meaning, approval, publication permission, export permission, migration permission, synchronization permission, indexing permission, backup permission, implementation-exposure permission, agent-exposure permission, or downstream-use readiness by itself.

A conforming implementation MUST preserve Source Material and Knowledge Record separation.

Source Material MUST NOT become a Knowledge Record merely because it is stored, opened, linked, displayed, indexed, summarized, backed up, synchronized, or processed by Codex.

A Knowledge Record MUST NOT become Source Material merely because it quotes, summarizes, extracts from, interprets, transforms, or depends on Source Material.

A conforming implementation MUST preserve privacy boundaries.

Restricted material MUST NOT be exposed through Obsidian, Codex, plugins, sync tools, backups, exports, indexes, graph views, embeddings, generated summaries, public folders, shared vaults, external agents, external systems, or downstream packages unless the applicable privacy classification and workflow clearance permit it.

A conforming implementation MUST preserve backup, synchronization, and recovery boundaries.

Backup existence MUST NOT be confused with recovery readiness.

Synchronization MUST NOT be confused with publication, export, migration, backup sufficiency, or downstream-use clearance.

Recovery MUST preserve traceability where governed material is affected.

A conforming implementation MUST preserve non-conformance visibility.

Known non-conformance MUST be recorded, routed, repaired, escalated, quarantined, excluded, or accepted within a governed scope.

Known non-conformance MUST NOT be hidden by Obsidian convenience, Codex convenience, plugin behavior, generated reports, automation, local memory, folder placement, sync success, backup existence, export packaging, or workflow completion.

IMP-0001 conformance MAY be checked by:

- human review;
- Codex review support;
- Markdown syntax checks;
- section-count checks;
- metadata checks;
- dependency checks;
- standards-boundary checks;
- duplication checks;
- privacy checks;
- source-reference checks;
- provenance checks;
- relationship checks;
- validation checks;
- workflow checks;
- storage checks;
- implementation-readiness checks;
- final review.

IMP-0001 conformance MUST be evaluated within its authority level as an implementation profile.

Conformance to IMP-0001 does not approve all implementation behavior.

Conformance to IMP-0001 does not make every Obsidian setup compliant.

Conformance to IMP-0001 does not make every Codex action permitted.

Conformance to IMP-0001 does not make every export package cleared.

Conformance to IMP-0001 does not make every downstream use permitted.

Conformance to IMP-0001 does not make The Brain mature, public, automated, unrestricted, or complete.

Conformance Requirements are successful when a future human, Obsidian user, Codex agent, validator, workflow, repository maintainer, migration process, export process, or downstream implementation can determine whether the implementation profile satisfies its role without exceeding its authority.

## 18. Success Criteria and Next Milestone

Success Criteria and Next Milestone defines how IMP-0001 is judged complete and what should happen after it passes final review.

IMP-0001 is successful when it clearly explains how Obsidian and Codex may realize The Brain Standard in practice without redefining The Brain Standard.

IMP-0001 is successful when it preserves:

- implementation independence;
- human readability;
- AI readability;
- local-first usability;
- repository usability;
- vault usability;
- Codex-assisted inspection;
- Object Identity;
- metadata meaning;
- relationship meaning;
- Source References;
- provenance;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- storage boundaries;
- agent boundaries;
- workflow boundaries;
- review boundaries;
- approval boundaries;
- backup boundaries;
- synchronization boundaries;
- recovery boundaries;
- publication boundaries;
- export boundaries;
- downstream-use boundaries;
- non-conformance visibility.

IMP-0001 is successful when Obsidian is clearly defined as a human-facing Markdown implementation interface.

IMP-0001 is successful when Codex is clearly defined as an agentic implementation-support environment.

IMP-0001 is successful when the repository and local machine layout are described well enough for controlled use.

IMP-0001 is successful when Folder Mapping supports navigation without becoming governed meaning.

IMP-0001 is successful when Metadata Representation supports Markdown usability without redefining metadata.

IMP-0001 is successful when Knowledge Records and Source Material remain distinct.

IMP-0001 is successful when agent and subagent use remains bounded, permissioned, traceable, reviewable, and non-authoritative by default.

IMP-0001 is successful when workflow execution remains governed and does not become tool convenience.

IMP-0001 is successful when validation and review support remain distinguishable from approval.

IMP-0001 is successful when backup, synchronization, and recovery preserve privacy, traceability, and governed meaning.

IMP-0001 is successful when publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, and downstream use remain scoped and cleared.

IMP-0001 is successful when implementation limitations and non-conformance remain visible, reviewable, and routable.

IMP-0001 is successful when implementation readiness can be assessed without treating readiness as maturity, publication, export clearance, or downstream-use clearance.

IMP-0001 is successful when conformance can be inspected without making the implementation profile higher authority than the standards it depends on.

IMP-0001 SHOULD help a future human, Obsidian user, Codex agent, validator, workflow, repository maintainer, migration process, export process, or downstream implementation determine:

- what the implementation is;
- what the implementation is not;
- what Obsidian may do;
- what Obsidian must not do;
- what Codex may do;
- what Codex must not do;
- where implementation profiles belong;
- how folders map to the standard;
- how metadata should be represented;
- how Knowledge Records should be handled;
- how Source Material should be handled;
- how agents and subagents may assist;
- how workflows should be supported;
- how validation and review should be supported;
- how backup should be handled;
- how synchronization should be handled;
- how recovery should be handled;
- how publication and export should be handled;
- how downstream use should be handled;
- how limitations should be recorded;
- how non-conformance should be routed;
- what readiness means;
- what conformance requires;
- what remains to be built.

IMP-0001 SHOULD remain under 20 major numbered sections.

IMP-0001 contains 18 major numbered sections.

The 18 sections are:

1. Purpose
2. Relationship to Prior Standards
3. Implementation Scope and Boundaries
4. Obsidian Role in the Implementation
5. Codex Role in the Implementation
6. Repository and Local Machine Layout
7. Folder Mapping to The Brain Standard
8. Metadata Representation
9. Knowledge Record and Source Material Handling
10. Agent and Subagent Use in Obsidian and Codex
11. Workflow Execution in the Implementation
12. Validation and Review Support
13. Backup, Synchronization, and Recovery
14. Publication, Export, and Downstream Use in the Implementation
15. Implementation Limitations and Non-Conformance
16. Implementation Readiness Criteria
17. Conformance Requirements
18. Success Criteria and Next Milestone

After IMP-0001 is completed and passes final review, the next milestone SHOULD be an implementation-support file or operational guide that turns the profile into practical setup instructions.

The recommended next milestone is:

- IMP-0002 — Obsidian and Codex Setup Guide

IMP-0002 SHOULD define the practical setup procedure for:

- cloning or copying the repository;
- opening the correct folder in Obsidian;
- confirming the `brain-standard` structure;
- confirming the `Standards/IMP` location;
- configuring Obsidian for plain Markdown use;
- identifying optional plugins;
- documenting plugin limitations;
- configuring Codex working scope;
- defining safe Codex inspection boundaries;
- defining first-use validation checks;
- defining backup expectations;
- defining sync cautions;
- defining recovery expectations;
- identifying restricted-material cautions;
- identifying generated-file cautions;
- preparing the environment for controlled ingestion.

IMP-0002 SHOULD remain subordinate to IMP-0001.

IMP-0002 SHOULD provide operational setup steps without redefining the implementation profile.

IMP-0002 SHOULD NOT approve broad publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream use by itself.

A future milestone MAY define additional implementation-support files, including:

- Obsidian vault setup checklist;
- Codex operating prompt;
- agent role prompt pack;
- validation checklist;
- metadata template;
- Knowledge Record template;
- Source Material intake template;
- non-conformance log template;
- backup and recovery checklist;
- export package checklist;
- deployment package checklist.

Those future files SHOULD be created only after IMP-0001 passes final review or after a documented decision to create them earlier.

The next immediate step after adding sections 16 through 18 is final review of IMP-0001.

Final review SHOULD verify:

- syntax placement and correctness;
- spelling and grammar;
- section sequence;
- section count;
- metadata correctness;
- dependency correctness;
- file path correctness;
- redundancy against prior standards;
- standard-boundary preservation;
- implementation-profile scope;
- GitHub repository placement;
- known repo-side issues;
- unresolved non-conformance;
- readiness for handoff summary.

IMP-0001 succeeds when it can be used as the governed bridge between The Brain Standard and the practical Obsidian plus Codex environment without causing architecture drift, authority creep, privacy confusion, validation confusion, workflow confusion, storage confusion, export confusion, or downstream-use confusion.