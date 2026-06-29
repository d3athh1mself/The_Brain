# IMP-0002 — Obsidian and Codex Setup Guide

Document ID: IMP-0002
Title: Obsidian and Codex Setup Guide
Version: 0.1.0
Status: Approved
Created: 2026-06-28
Last Updated: 2026-06-28
Authority: Implementation Guide
Phase: Phase 5 — Implementation Profiles
Milestone: 5.3 — Obsidian and Codex Setup Guide
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard; KS-0005 — Source Reference and Provenance Standard; KS-0006 — Lifecycle State Standard; KS-0007 — Authority Level Standard; KS-0008 — Privacy Classification Standard; KS-0009 — Validation Standard; SS-0001 — Storage Architecture Standard; SS-0002 — Storage Layout Specification; AG-0001 — Agent Operating Boundaries Standard; AG-0002 — Agent Role and Responsibility Standard; AG-0003 — Agent Permission and Traceability Standard; WF-0001 — Knowledge Ingestion Workflow Standard; WF-0002 — Review and Approval Workflow Standard; WF-0003 — Knowledge Maintenance and Update Workflow Standard; WF-0004 — Publication, Export, and Downstream Use Workflow Standard; DEP-0001 — Bare Usable Deployment Readiness Standard; IMP-0001 — Obsidian and Codex Implementation Profile
Supersedes: None
Superseded By: None
Related: IMP-0001 — Obsidian and Codex Implementation Profile

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and setup-guide instructions are interpreted within IMP-0002.

Where conflicts arise between setup behavior, local machine preparation, repository cloning, repository copying, Obsidian vault setup, Codex workspace setup, folder confirmation, Markdown handling, metadata representation, plugin use, agent access, validation checks, backup expectations, synchronization cautions, recovery expectations, import preparation, generated-file handling, restricted-material handling, or future implementation guidance, the higher-authority standards SHALL guide interpretation and resolution.

IMP-0002 is subordinate to TB-0000, TB-0001, TB-0002, TB-0003, the Phase 1 Knowledge Standards, the Phase 2 Storage Standards, the Phase 3 Agent Standards, the Phase 4 Workflow Standards, DEP-0001, and IMP-0001.

IMP-0002 is an implementation guide.

IMP-0002 does not define The Brain Standard itself.

IMP-0002 explains how to set up the Obsidian and Codex implementation environment described by IMP-0001.

If IMP-0002 appears to conflict with a constitutional document, Knowledge Standard, Storage Standard, Agent Standard, Workflow Standard, DEP-0001, or IMP-0001, the higher-authority document takes precedence unless formally revised through governance.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Implementation Guide refers to a practical setup or operating document that helps a human, agent, or implementation environment apply a governed implementation profile without redefining the standard.
- Obsidian refers to the Markdown-based local knowledge environment used as the human-facing interface for this setup guide.
- Codex refers to the agentic coding and file-operation environment used to inspect, compare, validate, draft, and support repository work within governed boundaries.
- Repository refers to the version-controlled storage environment used to preserve, review, compare, synchronize, and manage The Brain files.
- Local Repository Copy refers to a local clone or copy of the repository on a user’s machine.
- Vault refers to the practical local file environment opened by Obsidian to access Markdown files and related artifacts.
- Setup Environment refers to the combined local machine, repository copy, Obsidian vault, Codex workspace, implementation-support files, scripts, templates, validators, and operational instructions prepared for The Brain.
- Setup Step refers to an action taken to prepare, verify, configure, inspect, or correct the implementation environment.
- Setup Check refers to a review action used to confirm that the implementation environment satisfies the relevant setup expectation.
- Plugin refers to an optional Obsidian extension that may improve usability but must not redefine standard meaning.
- Generated File refers to a file produced by a tool, script, agent, validator, plugin, indexer, cache process, export process, or automation.
- Restricted Material refers to governed material whose Privacy Classification, Source Reference, provenance, authority, lifecycle state, validation state, or downstream-use boundary requires constrained handling.
- Controlled Ingestion refers to the prepared state in which the setup environment is ready to receive Source Material or captured information through governed ingestion workflows.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, or operational context associated with a governed entity.
- Validation refers to the process of checking whether a governed entity satisfies applicable standards, specifications, metadata expectations, provenance expectations, relationship expectations, lifecycle expectations, authority expectations, privacy expectations, compatibility expectations, workflow expectations, agent expectations, implementation expectations, import expectations, export expectations, migration expectations, publication expectations, synchronization expectations, indexing expectations, backup expectations, or downstream-use expectations.

## 1. Purpose

The purpose of IMP-0002 is to define the practical setup guide for preparing the Obsidian and Codex implementation environment for The Brain Standard.

IMP-0001 defines how Obsidian and Codex may be used together as a practical implementation environment.

IMP-0002 turns that implementation profile into setup instructions.

IMP-0002 exists so that a human user, repository maintainer, Codex agent, implementation-support agent, or future setup assistant can prepare a local working environment without inventing setup rules that conflict with The Brain Standard.

IMP-0002 defines how to:

- obtain or copy the repository;
- identify the correct repository root;
- confirm the `brain-standard` structure;
- confirm the `Standards/IMP` location;
- open the correct folder in Obsidian;
- configure Obsidian for plain Markdown use;
- identify optional Obsidian plugins;
- document plugin limitations;
- prepare Codex to work inside the correct repository scope;
- define safe Codex inspection boundaries;
- perform first-use setup checks;
- confirm backup expectations;
- identify synchronization cautions;
- identify recovery expectations;
- identify restricted-material cautions;
- identify generated-file cautions;
- prepare the environment for controlled ingestion.

IMP-0002 does not define what The Brain is.

IMP-0002 does not define Knowledge Object meaning.

IMP-0002 does not define Object Identity.

IMP-0002 does not define metadata meaning.

IMP-0002 does not define relationship meaning.

IMP-0002 does not define Source Reference or provenance meaning.

IMP-0002 does not define Lifecycle State, Authority Level, Privacy Classification, or Validation.

IMP-0002 does not define agent authority, workflow authority, publication clearance, export clearance, synchronization clearance, indexing clearance, backup clearance, implementation exposure, agent exposure, migration clearance, or downstream-use clearance.

Those meanings and permissions are defined by higher-authority standards and workflows.

IMP-0002 provides setup guidance only.

A completed setup under IMP-0002 means the local Obsidian and Codex environment is prepared for governed use.

A completed setup does not mean:

- the repository is fully validated;
- all files are approved;
- all Knowledge Records are ready for downstream use;
- all Source Material is safe for indexing;
- all material is safe for synchronization;
- all material is safe for agent exposure;
- all material is safe for publication;
- all material is safe for export;
- all material is safe for migration;
- backups have been tested;
- recovery has been proven;
- ingestion may proceed without review.

IMP-0002 is successful when a future human or Codex-style agent can set up The Brain in Obsidian and Codex, confirm the expected structure, identify setup risks, preserve governed boundaries, and prepare for controlled ingestion without creating architecture drift.

## 2. Relationship to IMP-0001 and Prior Standards

IMP-0002 is subordinate to IMP-0001 and all higher-authority standards that govern IMP-0001.

IMP-0001 defines the implementation profile.

IMP-0002 defines the setup guide for that implementation profile.

In practical terms:

- IMP-0001 answers: How may Obsidian and Codex realize The Brain Standard in practice?
- IMP-0002 answers: How should a user set up Obsidian and Codex for that implementation?
- DEP-0001 answers: What must exist before the system is ready for bare usable deployment?
- SS-0001 and SS-0002 answer: How must storage architecture and storage layout be preserved?
- AG-0001, AG-0002, and AG-0003 answer: What may agents do, what roles may they perform, and what traceability is required?
- WF-0001 through WF-0004 answer: How governed workflows handle ingestion, review, maintenance, publication, export, and downstream use.

IMP-0002 MUST preserve the boundaries established by IMP-0001.

IMP-0002 MAY define setup instructions for:

- local repository placement;
- repository cloning or copying;
- folder verification;
- Obsidian vault opening;
- Obsidian Markdown behavior;
- optional plugin review;
- Codex workspace selection;
- Codex inspection boundaries;
- setup validation checks;
- backup preparation;
- synchronization caution;
- recovery preparation;
- restricted-material caution;
- generated-file handling;
- controlled-ingestion preparation.

IMP-0002 MUST NOT redefine:

- The Brain mission;
- layered architecture;
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
- agent operating boundaries;
- agent roles;
- agent permissions;
- agent traceability;
- workflow authority;
- review authority;
- approval authority;
- publication readiness;
- export readiness;
- migration readiness;
- synchronization readiness;
- indexing readiness;
- backup readiness;
- implementation exposure;
- agent exposure;
- downstream-use readiness;
- deployment readiness.

IMP-0002 depends on the constitutional foundation because setup must preserve the original project vision that The Brain is implementation-independent, human-readable, AI-readable, portable, governed, and durable.

IMP-0002 depends on the Knowledge Standards because setup must preserve knowledge meaning, stable identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, and Validation.

IMP-0002 depends on the Storage Standards because setup must preserve storage areas, layout expectations, folder boundaries, import areas, export areas, backup areas, archive areas, implementation-support areas, and generated-file boundaries without allowing folder placement to define governed meaning.

IMP-0002 depends on the Agent Standards because Codex setup must keep agent activity bounded, role-aware, permission-aware, traceable, reviewable, and escalatable.

IMP-0002 depends on the Workflow Standards because setup must prepare the environment to support ingestion, review and approval, maintenance and update, publication, export, migration, synchronization, indexing, backup, recovery, implementation exposure, agent exposure, and downstream-use workflows without silently approving them.

IMP-0002 depends on DEP-0001 because setup should occur only after the bare usable deployment structure exists or is being actively verified.

IMP-0002 depends on IMP-0001 because IMP-0002 implements the setup path for the Obsidian and Codex implementation profile.

If a setup convenience conflicts with a higher-authority standard, the setup convenience MUST be rejected, revised, documented as non-conforming, or escalated for review.

## 3. Setup Scope and Boundaries

IMP-0002 applies to the initial setup of the Obsidian and Codex implementation environment for The Brain Standard.

The setup environment includes:

- the user’s local machine;
- the GitHub repository or local repository copy;
- the repository root;
- the `brain-standard` folder;
- the governed standards folders;
- the `Standards/IMP` folder;
- the Obsidian vault or vault-like Markdown workspace;
- Codex workspace access;
- implementation-support files;
- setup notes;
- optional plugins;
- scripts;
- templates;
- validators;
- generated indexes;
- generated caches;
- import areas;
- export areas;
- archive areas;
- backup areas;
- synchronization targets where used;
- recovery materials;
- controlled-ingestion preparation areas.

IMP-0002 applies before normal ingestion, maintenance, publication, export, migration, synchronization, indexing, backup automation, agent exposure, or downstream-use activity begins.

IMP-0002 does not approve those activities by itself.

The setup scope includes practical confirmation that the environment is ready to support governed work.

The setup scope does not include full validation of every governed file unless a later setup step explicitly invokes validation under the applicable standard or workflow.

IMP-0002 may guide a user to confirm that:

- the repository exists locally;
- the correct folder is opened in Obsidian;
- the expected standard folders are visible;
- implementation-profile files are stored under `Standards/IMP`;
- Obsidian is treating files as plain Markdown;
- optional plugins are disabled, absent, or documented before use;
- Codex is pointed at the correct repository scope;
- Codex is not operating outside the intended workspace;
- generated files are distinguishable from governed files;
- restricted material is not exposed unintentionally;
- backup expectations are understood before major work begins;
- synchronization risks are understood before sync is enabled;
- recovery expectations are documented before relying on the environment;
- controlled ingestion does not begin until setup checks pass.

IMP-0002 MUST NOT treat setup completion as approval.

IMP-0002 MUST NOT treat setup completion as validation success unless validation has been performed under the applicable validation scope.

IMP-0002 MUST NOT treat setup completion as publication readiness.

IMP-0002 MUST NOT treat setup completion as export readiness.

IMP-0002 MUST NOT treat setup completion as migration readiness.

IMP-0002 MUST NOT treat setup completion as synchronization readiness.

IMP-0002 MUST NOT treat setup completion as indexing readiness.

IMP-0002 MUST NOT treat setup completion as backup recovery proof.

IMP-0002 MUST NOT treat setup completion as unrestricted Codex access.

IMP-0002 MUST NOT treat setup completion as unrestricted agent exposure.

IMP-0002 MUST NOT treat setup completion as downstream-use readiness.

Obsidian setup is limited to human-facing Markdown access, navigation, editing, search, review support, and local usability.

Obsidian MUST NOT become the source of standard meaning.

Obsidian folder placement MUST NOT define Object Identity.

Obsidian backlinks MUST NOT define governed relationships by themselves.

Obsidian tags MUST NOT define governed metadata unless a governed standard or specification explicitly defines that use.

Obsidian plugins MUST NOT redefine metadata, relationships, lifecycle state, authority level, privacy classification, validation, review status, approval, export permission, publication permission, deployment readiness, or downstream-use readiness.

Codex setup is limited to authorized repository inspection, file comparison, syntax support, drafting support, validation support, setup checking, implementation-support work, and bounded agentic assistance.

Codex MUST NOT become an unreviewable authority.

Codex MUST NOT approve standards by itself.

Codex MUST NOT silently delete, overwrite, move, expose, publish, export, restructure, or migrate governed material where the action affects Object Identity, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, reviewability, compatibility, storage meaning, workflow state, agent traceability, deployment readiness, or downstream use.

Setup boundaries exist to prevent local convenience from becoming architecture.

IMP-0002 is successful when setup can be completed repeatably on a local machine while preserving implementation independence, governed storage boundaries, agent boundaries, workflow boundaries, privacy boundaries, validation expectations, and the practical usability required for controlled ingestion.

## 4. Repository Copy or Clone Setup

The repository copy or clone setup is the first practical setup step for IMP-0002.

A user SHOULD begin by obtaining a local copy of the GitHub repository that contains The Brain files.

The local copy MAY be created by:

- cloning the repository through Git;
- downloading a repository archive;
- copying a prepared deployment package;
- copying a verified local repository from another machine;
- restoring a repository copy from a trusted backup.

The RECOMMENDED repository source for the current implementation is:

```text
d3athh1mself/The_Brain
```

The local repository copy SHOULD preserve the repository structure exactly unless a governed migration, deployment, or storage-layout process explicitly allows a change.

A user SHOULD confirm that the local repository copy contains the expected root-level structure before opening the environment in Obsidian or Codex.

At minimum, the local repository copy SHOULD contain:

- the repository root;
- the `brain-standard` folder;
- the `brain-standard/Standards` folder;
- the existing governed standards folders;
- the `brain-standard/Standards/IMP` folder;
- IMP-0001;
- any approved prerequisite standards required by IMP-0002.

The setup process MUST NOT assume that a folder exists merely because it is expected.

The setup process SHOULD verify folder existence directly.

If the `IMP` folder does not exist, the folder SHOULD be created only by adding a governed implementation-profile or implementation-guide file at the appropriate path.

Git does not preserve empty folders by default.

Therefore, an empty `IMP` folder SHOULD NOT be treated as missing if the file that creates it has not yet been committed.

The expected path for this file is:

```text
brain-standard/Standards/IMP/IMP-0002 — Obsidian and Codex Setup Guide.md
```

The repository setup SHOULD preserve exact filenames where practical.

A filename change MUST NOT be treated as an Object Identity change by itself.

A repository path change MUST NOT be treated as an Object Identity change by itself.

A copied repository MUST NOT be treated as deployment-ready merely because the files are present.

Repository presence does not prove:

- metadata correctness;
- relationship correctness;
- Source Reference correctness;
- provenance completeness;
- Lifecycle State correctness;
- Authority Level correctness;
- Privacy Classification correctness;
- Validation success;
- backup readiness;
- synchronization readiness;
- export readiness;
- migration readiness;
- downstream-use readiness.

The local repository copy SHOULD be placed somewhere the user can inspect, back up, and recover without relying on hidden application state.

The repository SHOULD NOT be placed inside an application-controlled folder if doing so makes the files difficult to inspect, copy, validate, back up, or restore.

The repository SHOULD NOT be placed only inside a synchronization tool folder unless synchronization risk has been reviewed.

The repository SHOULD NOT be placed only inside an Obsidian-specific hidden configuration area.

The repository SHOULD remain accessible through normal file-system inspection.

A user SHOULD record or remember the local repository path before connecting Obsidian or Codex to it.

A Codex-style agent SHOULD be given the repository root or the specific governed working folder required for the task.

A Codex-style agent SHOULD NOT be given broader machine access than required.

A setup process SHOULD confirm the repository root before any agent is asked to inspect, edit, move, validate, or create files.

A repository root is the highest local folder that contains the working copy of the repository.

For this implementation, the repository root SHOULD contain the `brain-standard` folder.

The setup process SHOULD distinguish between:

- repository root;
- `brain-standard` root;
- Obsidian vault root;
- Standards folder;
- implementation-profile folder;
- generated-file area;
- backup area;
- export area;
- import area.

These locations MAY overlap in a simple deployment.

However, their meanings MUST remain distinguishable.

A simple setup MAY open the repository root or the `brain-standard` folder directly in Obsidian, depending on the chosen vault boundary.

The chosen vault boundary SHOULD be documented or consistently understood before normal use begins.

The repository copy or clone setup is complete when:

- the repository exists locally;
- the repository root is known;
- the `brain-standard` folder is present;
- the `Standards` folder is present;
- the `Standards/IMP` folder is present or ready to be created by adding IMP-0002;
- prerequisite standards are present;
- the user can inspect files outside Obsidian;
- Codex scope can be pointed at the correct folder;
- no setup step has treated folder placement as governed meaning;
- no setup step has approved ingestion, publication, export, migration, synchronization, indexing, backup automation, agent exposure, or downstream use by itself.

## 5. Obsidian Vault Setup

Obsidian vault setup prepares the human-facing Markdown environment for The Brain Standard.

Obsidian SHOULD be used as a practical interface for reading, navigating, editing, reviewing, and maintaining Markdown files.

Obsidian MUST NOT be treated as the source of standard meaning.

The user SHOULD open either:

- the repository root;
- the `brain-standard` folder;
- another governed vault boundary explicitly allowed by the implementation profile or future setup guidance.

For the simplest setup, opening the `brain-standard` folder as the Obsidian vault is RECOMMENDED.

Opening `brain-standard` keeps the visible vault focused on governed project content while avoiding unnecessary exposure of repository-level implementation files.

A user MAY open the full repository root if repository-level files, implementation-support files, scripts, templates, or GitHub-related files need to be visible in Obsidian.

If the full repository root is opened, the user SHOULD remain aware that not every visible file is a Knowledge Record, governed standard, Source Material item, or approved record.

Obsidian vault setup SHOULD confirm that the following areas are visible where present:

- `Standards`;
- `Standards/TB`;
- `Standards/KS`;
- `Standards/SS`;
- `Standards/AG`;
- `Standards/WF`;
- `Standards/DEP`;
- `Standards/IMP`.

The setup process SHOULD NOT require Obsidian-specific folders to define governed structure.

Obsidian may create implementation-specific files or folders, such as configuration files.

Those files MAY support user interface behavior.

Those files MUST NOT define Object Identity, metadata meaning, relationship meaning, Lifecycle State, Authority Level, Privacy Classification, Validation, approval, publication readiness, export readiness, or downstream-use readiness.

Obsidian vault setup SHOULD use plain Markdown as the primary working format.

Markdown files SHOULD remain readable outside Obsidian.

A user SHOULD be able to open governed Markdown files in a normal text editor and still understand their basic structure.

Obsidian links MAY support navigation.

Obsidian backlinks MAY support discovery.

Obsidian graph views MAY support exploration.

Obsidian search MAY support review and maintenance.

However:

- Obsidian links do not automatically create governed relationships;
- Obsidian backlinks do not automatically create governed relationships;
- Obsidian graph views do not define authority;
- Obsidian search ranking does not define importance;
- Obsidian tags do not define governed metadata unless governed elsewhere;
- Obsidian folders do not define Object Identity;
- Obsidian plugin output does not define Validation;
- Obsidian display state does not define Lifecycle State.

The Obsidian vault SHOULD be configured to avoid hiding file extensions, metadata, or Markdown structure in a way that makes review difficult.

Preview mode MAY be used for reading.

Source mode SHOULD remain available for inspection and editing.

A user SHOULD understand how to switch between reading view and source editing view before relying on Obsidian for governed work.

The setup process SHOULD avoid requiring proprietary or hidden Obsidian behavior.

Obsidian MAY improve usability, but the files MUST remain portable.

The vault SHOULD NOT depend on a plugin to make the basic document structure understandable.

The vault SHOULD NOT depend on a graph view to make governed relationships understandable.

The vault SHOULD NOT depend on a tag pane to make governed metadata understandable.

The vault SHOULD NOT depend on Obsidian cache state for validation, review, approval, publication, export, or downstream-use decisions.

Obsidian vault setup is complete when:

- the selected vault boundary is known;
- the vault opens successfully;
- the `Standards` folder is visible where expected;
- the `Standards/IMP` folder is visible where expected;
- IMP-0001 is visible where present;
- IMP-0002 can be added at the expected path;
- Markdown source remains inspectable;
- Obsidian-specific behavior has not been treated as standard meaning;
- plugins are absent, disabled, or documented for review before use;
- no setup step has approved ingestion, publication, export, migration, synchronization, indexing, backup automation, agent exposure, or downstream use by itself.

## 6. Plain Markdown Configuration

Plain Markdown configuration ensures that The Brain remains readable, portable, inspectable, and maintainable outside any single tool.

Obsidian SHOULD be configured so that governed documents remain normal Markdown files.

A governed Markdown file SHOULD remain usable when opened in:

- Obsidian;
- a plain text editor;
- a code editor;
- a GitHub file viewer;
- Codex;
- another Markdown-compatible implementation;
- a future compliant tool.

Plain Markdown configuration MUST preserve human readability.

Plain Markdown configuration MUST preserve AI readability.

Plain Markdown configuration MUST preserve repository portability.

Plain Markdown configuration MUST NOT require hidden application state to interpret governed meaning.

The following Markdown behavior is RECOMMENDED:

- headings use standard Markdown heading syntax;
- metadata remains visible as text unless a future governed specification defines another representation;
- lists use normal Markdown list syntax;
- code blocks use fenced Markdown syntax where needed;
- file paths are written as plain text or fenced code blocks where clarity requires it;
- setup instructions remain readable without plugin rendering;
- implementation warnings remain visible in source text;
- governed terms remain spelled consistently;
- section numbers remain explicit where used.

Plain Markdown configuration SHOULD avoid unnecessary formatting that reduces portability.

The following SHOULD be avoided in governed setup content unless a later specification allows them:

- plugin-only syntax required for interpretation;
- hidden fields required for meaning;
- embedded database views required for meaning;
- canvas-only structure required for meaning;
- graph-only relationship meaning;
- tag-only metadata meaning;
- callout-only warnings that disappear outside Obsidian;
- nonstandard markup required for approval, validation, privacy, authority, lifecycle, export, or publication decisions.

Obsidian callouts MAY be used for readability in operational notes or implementation-support material.

However, a callout MUST NOT be the only place where a governed requirement, warning, restriction, approval condition, privacy caution, validation condition, or export limitation is recorded.

Markdown front matter MAY be used if a future governed specification defines exact fields or if an implementation profile permits a temporary representation.

Until exact metadata fields are governed by a future specification, IMP-0002 SHOULD NOT invent required front matter fields.

A setup guide MAY include visible document metadata in the established header format used by the standards.

Plain Markdown configuration SHOULD preserve the existing document-header pattern.

For governed documents, the document header SHOULD remain visible near the top of the file.

The document header SHOULD include:

- Document ID;
- Title;
- Version;
- Status;
- Created;
- Last Updated;
- Authority;
- Phase;
- Milestone;
- Depends On;
- Supersedes;
- Superseded By;
- Related.

Plain Markdown configuration MUST NOT treat the displayed title as Object Identity by itself.

Plain Markdown configuration MUST NOT treat the filename as Object Identity by itself.

Plain Markdown configuration MUST NOT treat the folder path as Object Identity by itself.

Plain Markdown configuration MUST NOT treat a tag as governed metadata unless governed by a standard or specification.

Plain Markdown configuration MUST NOT treat visual formatting as approval, authority, privacy classification, validation, lifecycle state, publication readiness, export readiness, or downstream-use readiness.

A user SHOULD confirm that Markdown files can be opened and read outside Obsidian before relying on the setup.

A user SHOULD confirm that Codex or another file-inspection tool can read the Markdown text directly.

A user SHOULD confirm that GitHub can display the Markdown file without requiring Obsidian.

A user SHOULD avoid storing governed meaning only in Obsidian workspace state, plugin settings, graph layout, folded headings, pane arrangement, search state, or local cache files.

Plain Markdown configuration is complete when:

- governed files remain readable as plain Markdown;
- document headers remain visible;
- section headings remain visible;
- setup instructions remain visible;
- warnings and restrictions remain visible;
- file paths remain inspectable;
- plugin-only syntax is not required for meaning;
- Obsidian display behavior has not become standard meaning;
- Codex can inspect the file text directly;
- GitHub can display the file text directly;
- no setup step has converted formatting convenience into governed authority.

## 7. Optional Plugin Handling

Optional plugin handling defines how Obsidian plugins may be considered, limited, documented, reviewed, or rejected during setup.

Plugins MAY be used to improve usability.

Plugins MUST NOT be required for basic interpretation of governed files.

The setup environment SHOULD remain usable without any Obsidian plugin.

A plugin MAY support:

- navigation;
- search;
- editing convenience;
- table handling;
- backlink visibility;
- review support;
- task visibility;
- file organization;
- template assistance;
- export convenience;
- local usability.

A plugin MUST NOT define:

- Object Identity;
- Knowledge Object meaning;
- Knowledge Record meaning;
- Source Material meaning;
- metadata meaning;
- relationship meaning;
- Source Reference meaning;
- provenance meaning;
- Lifecycle State;
- Authority Level;
- Privacy Classification;
- Validation;
- approval;
- review authority;
- publication readiness;
- export readiness;
- migration readiness;
- synchronization readiness;
- indexing readiness;
- backup readiness;
- implementation exposure;
- agent exposure;
- downstream-use readiness.

A plugin SHOULD be treated as implementation support.

A plugin SHOULD NOT be treated as a governed standard, specification, workflow, validator, approval mechanism, or authority source unless a future governed document explicitly defines that role.

Plugin behavior SHOULD be reviewed before normal use.

Plugin behavior SHOULD be documented when it affects:

- file visibility;
- file editing;
- file movement;
- metadata display;
- link handling;
- backlink display;
- graph display;
- indexing;
- search;
- export;
- synchronization;
- publication;
- generated files;
- cache files;
- templates;
- validation support;
- agent-facing output;
- restricted material.

A plugin SHOULD NOT be enabled if its behavior is unclear, hidden, difficult to inspect, difficult to disable, or likely to create architecture drift.

A plugin SHOULD NOT be enabled if it stores governed meaning only in hidden application state.

A plugin SHOULD NOT be enabled if it modifies governed files without review.

A plugin SHOULD NOT be enabled if it silently rewrites Markdown, metadata, links, headings, paths, filenames, tags, or embedded content.

A plugin SHOULD NOT be enabled if it creates generated files that cannot be distinguished from governed files.

A plugin SHOULD NOT be enabled if it indexes restricted material without privacy review.

A plugin SHOULD NOT be enabled if it synchronizes, publishes, exports, uploads, embeds, summarizes, or transmits governed material without explicit review.

A plugin MAY be tested in a limited setup environment before being used on governed files.

Plugin testing SHOULD use non-sensitive test files where practical.

Plugin testing SHOULD confirm that the plugin does not silently alter:

- document headers;
- section headings;
- stable identifiers;
- metadata text;
- relationship references;
- Source References;
- provenance notes;
- lifecycle terms;
- authority terms;
- privacy terms;
- validation language;
- file paths;
- filenames.

If a plugin creates support files, generated files, caches, indexes, or configuration files, those files SHOULD remain distinguishable from governed documents.

Generated plugin files SHOULD NOT be treated as Knowledge Records unless a governed workflow creates or approves them as Knowledge Records.

Plugin configuration SHOULD be inspectable where practical.

Plugin configuration SHOULD NOT become the only place where setup meaning, workflow state, privacy restrictions, validation expectations, approval conditions, or export limits are recorded.

A plugin that supports templates MAY be used to reduce repetitive formatting.

However, a template plugin MUST NOT define required metadata, required schema, approval status, validation status, lifecycle status, authority status, privacy status, or relationship meaning unless a governed specification explicitly defines that behavior.

A plugin that supports links MAY be used to improve navigation.

However, plugin-created links MUST NOT be treated as governed relationships by themselves.

A plugin that supports graphs MAY be used to explore visible connections.

However, graph position, graph centrality, graph clustering, graph color, graph filtering, or graph visibility MUST NOT define authority, relationship meaning, knowledge importance, validation success, or downstream-use readiness.

A plugin that supports export MAY be used only within governed export boundaries.

Export convenience MUST NOT become export approval.

A plugin that supports synchronization MAY be used only after synchronization risk has been reviewed.

Synchronization convenience MUST NOT become synchronization readiness.

A plugin that supports AI features MUST be treated as agent or implementation exposure where it reads, summarizes, indexes, embeds, transmits, rewrites, classifies, or reasons over governed material.

AI plugin behavior MUST remain subordinate to the Agent Standards, Privacy Classification Standard, Validation Standard, Workflow Standards, IMP-0001, and this setup guide.

Optional plugin handling is complete when:

- the setup works without required plugins;
- any enabled plugin has a clear purpose;
- plugin behavior has been reviewed for setup risk;
- plugin-generated files are distinguishable from governed files;
- plugin behavior does not define governed meaning;
- plugin behavior does not silently approve, validate, publish, export, synchronize, index, migrate, expose, or route governed material;
- restricted material is not exposed through plugin behavior without review;
- plugin limitations are understood before normal use.

## 8. Codex Workspace Setup

Codex workspace setup prepares the agentic implementation-support environment for bounded repository work.

Codex MAY be used to assist with setup, inspection, comparison, drafting, validation support, template support, script support, and implementation-support work.

Codex MUST remain subordinate to The Brain Standard.

Codex MUST remain subordinate to IMP-0001 and this setup guide.

Codex MUST NOT be treated as an unreviewable authority.

Codex MUST NOT approve standards by itself.

Codex MUST NOT silently redefine governed meaning.

The Codex workspace SHOULD be pointed at the narrowest practical folder required for the current task.

For broad setup inspection, the Codex workspace MAY be pointed at the repository root.

For implementation-guide work, the Codex workspace SHOULD usually be pointed at the repository root or the `brain-standard` folder.

For standards-only inspection, the Codex workspace MAY be pointed at `brain-standard/Standards`.

For implementation-profile work, the Codex workspace MAY be pointed at `brain-standard/Standards/IMP`.

The selected Codex workspace SHOULD be known before Codex performs file inspection or drafting.

The selected Codex workspace SHOULD be documented in a task note, prompt, review note, or handoff summary when the scope matters.

Codex workspace setup SHOULD distinguish between:

- repository root;
- `brain-standard` root;
- Standards folder;
- implementation-profile folder;
- draft area;
- review area;
- archive area;
- import area;
- export area;
- backup area;
- migration area;
- implementation-support area;
- generated-file area;
- restricted-material area where applicable.

Codex SHOULD begin with read-only inspection where practical.

Codex SHOULD identify the relevant files before proposing changes.

Codex SHOULD compare new content against relevant higher-authority files before drafting or editing.

Codex SHOULD preserve existing naming conventions, heading conventions, metadata conventions, dependency wording, and section-flow conventions unless a correction is required.

Codex SHOULD be instructed to avoid broad changes when a task only requires a specific section, file, folder, or review scope.

Codex SHOULD NOT be given permission to inspect unrelated local files.

Codex SHOULD NOT be given permission to inspect private, restricted, sensitive, secret, or unrelated material unless the task explicitly requires it and the applicable privacy boundary allows it.

Codex SHOULD NOT be asked to operate from memory when the repository files are available for inspection.

Codex SHOULD NOT assume that a file exists merely because a handoff summary says it should exist.

Codex SHOULD verify file presence directly when repository access is available.

Codex SHOULD NOT assume that a repo-side issue remains open if the repository shows that it has already been corrected.

Codex SHOULD NOT assume that a missing folder is non-conforming without checking whether Git has omitted an empty folder.

Codex SHOULD NOT create, edit, move, delete, export, publish, migrate, synchronize, index, back up, or expose governed material without task-level authorization.

Codex workspace setup SHOULD define whether Codex may:

- read files;
- compare files;
- summarize files;
- identify issues;
- propose edits;
- draft new sections;
- draft new files;
- prepare copy/paste content;
- inspect repository paths;
- suggest folder placement;
- suggest validation checks;
- suggest scripts;
- suggest templates;
- report non-conformance.

Codex workspace setup SHOULD also define whether Codex must avoid:

- applying edits directly;
- moving files;
- deleting files;
- rewriting approved content;
- changing metadata status;
- changing authority levels;
- changing lifecycle states;
- changing privacy classifications;
- changing validation states;
- exporting files;
- publishing files;
- indexing files;
- synchronizing files;
- exposing restricted material;
- creating downstream-use packages.

A Codex workspace is not safe merely because it opens successfully.

A Codex workspace is safe for a task only when the task scope, file scope, permission scope, privacy boundary, and review expectation are clear enough for the work being performed.

Codex workspace setup is complete when:

- the workspace folder is known;
- the workspace folder is appropriate for the task;
- Codex can inspect the required files;
- Codex has not been given unnecessary machine-wide scope;
- Codex has not been given unnecessary restricted-material access;
- Codex permissions are bounded by task need;
- Codex output remains reviewable;
- Codex activity remains traceable where required;
- Codex has not been treated as approval authority;
- Codex has not been treated as validation authority unless a governed validation process explicitly defines that scope;
- Codex has not been treated as publication, export, migration, synchronization, indexing, backup, implementation-exposure, agent-exposure, or downstream-use authority.

## 9. Codex Inspection Boundaries

Codex inspection boundaries define what Codex may inspect during setup and how inspection must remain limited, reviewable, privacy-respecting, and subordinate to the governed standards.

Inspection means reading, opening, searching, comparing, summarizing, checking, or analyzing files without modifying them.

Inspection is usually lower risk than editing, moving, deleting, exporting, publishing, synchronizing, indexing, or migrating.

However, inspection may still create risk when material is private, restricted, sensitive, unpublished, unapproved, source-protected, confidential, or not intended for agent exposure.

Codex MAY inspect governed files when inspection is needed for an authorized setup, review, drafting, validation-support, comparison, or implementation-support task.

Codex SHOULD inspect the narrowest practical file set.

Codex SHOULD inspect higher-authority standards before proposing setup guidance that depends on them.

Codex SHOULD inspect IMP-0001 before proposing changes to IMP-0002.

Codex SHOULD inspect the relevant Storage Standards before proposing folder, layout, repository, backup, archive, import, export, or generated-file guidance.

Codex SHOULD inspect the relevant Agent Standards before proposing Codex access, Codex permission, Codex role, Codex traceability, or Codex output guidance.

Codex SHOULD inspect the relevant Workflow Standards before proposing ingestion, review, maintenance, publication, export, migration, synchronization, indexing, backup, or downstream-use setup guidance.

Codex SHOULD inspect DEP-0001 before making deployment-readiness claims.

Codex SHOULD NOT inspect files outside the authorized workspace unless the user explicitly provides them or the task scope requires them.

Codex SHOULD NOT inspect unrelated personal files.

Codex SHOULD NOT inspect secrets, credentials, private keys, tokens, passwords, unrelated personal records, or unrelated restricted material.

Codex SHOULD NOT inspect private or restricted Source Material unless the applicable task, privacy boundary, and workflow context permit that inspection.

Codex SHOULD NOT inspect material merely because it is visible in the file tree.

Visibility does not equal permission.

Repository access does not equal permission.

Folder access does not equal permission.

Search access does not equal permission.

Obsidian visibility does not equal permission.

Codex inspection SHOULD preserve the distinction between:

- governed documents;
- Knowledge Records;
- Source Material;
- drafts;
- review files;
- archived files;
- generated files;
- implementation-support files;
- plugin files;
- cache files;
- index files;
- export files;
- import files;
- backup files;
- migration files;
- operational notes;
- handoff summaries.

Codex SHOULD NOT treat generated files as governed files unless a governed workflow or specification says they are governed.

Codex SHOULD NOT treat handoff summaries as higher authority than the repository files.

Codex SHOULD NOT treat Obsidian configuration files as standard meaning.

Codex SHOULD NOT treat plugin files as standard meaning.

Codex SHOULD NOT treat cache files as standard meaning.

Codex SHOULD NOT treat search results as complete repository review.

Codex SHOULD NOT treat partial file snippets as full-file inspection when full-file inspection is required.

Codex SHOULD report uncertainty when it has inspected only part of a file.

Codex SHOULD report when a referenced file cannot be found.

Codex SHOULD report when a repository file differs from a handoff summary.

Codex SHOULD report when a requested file exists in the repository even if a handoff summary says it is missing.

Codex SHOULD report when a repo-side correction has already been made.

Codex SHOULD NOT silently resolve conflicts between uploaded files and repository files when the conflict affects governed meaning.

Where uploaded content and repository content differ, Codex SHOULD identify the difference and preserve the current task scope.

Codex MAY use uploaded files as the active working draft when the user provides them for review.

Codex MAY use repository files as comparison sources when the user requests repo comparison.

Codex SHOULD distinguish between:

- active uploaded draft;
- current repository version;
- prior handoff summary;
- proposed new content;
- approved standard;
- draft standard;
- implementation guide;
- operational note.

Codex inspection boundaries are complete when:

- the inspected file set is appropriate for the task;
- higher-authority comparison files have been checked where needed;
- restricted material has not been inspected without authorization;
- generated files have not been confused with governed files;
- Obsidian or plugin state has not been confused with governed meaning;
- repository state has been distinguished from handoff-state claims;
- Codex uncertainty has been reported where inspection is incomplete;
- Codex output remains reviewable;
- no inspection step has become approval, validation, publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream-use clearance.

## 10. First-Use Setup Checks

First-use setup checks confirm that the Obsidian and Codex setup environment is ready for controlled use.

First-use setup checks SHOULD occur before normal ingestion, maintenance, publication, export, migration, synchronization, indexing, backup automation, implementation exposure, agent exposure, or downstream use begins.

First-use setup checks are practical readiness checks.

First-use setup checks are not full validation unless a governed validation process is explicitly performed.

The setup environment SHOULD be checked in a predictable order.

The RECOMMENDED first-use setup check order is:

- repository presence;
- repository root confirmation;
- `brain-standard` folder confirmation;
- `Standards` folder confirmation;
- standards folder visibility;
- `Standards/IMP` folder confirmation;
- IMP-0001 presence;
- IMP-0002 placement;
- Markdown readability;
- Obsidian vault boundary confirmation;
- Codex workspace boundary confirmation;
- plugin status review;
- generated-file distinction;
- restricted-material caution;
- backup expectation review;
- synchronization caution review;
- recovery expectation review;
- controlled-ingestion readiness.

The setup process SHOULD confirm that the repository exists locally.

The setup process SHOULD confirm that the user knows where the repository is stored.

The setup process SHOULD confirm that the `brain-standard` folder is present.

The setup process SHOULD confirm that the `Standards` folder is present.

The setup process SHOULD confirm that expected standards folders are visible where present.

Expected standards folders include:

- `TB`;
- `KS`;
- `SS`;
- `AG`;
- `WF`;
- `DEP`;
- `IMP`.

The setup process SHOULD confirm that IMP-0001 is present before relying on IMP-0002.

The setup process SHOULD confirm that IMP-0002 is placed in the implementation-profile area.

The expected placement for IMP-0002 is:

    brain-standard/Standards/IMP/IMP-0002 — Obsidian and Codex Setup Guide.md

The setup process SHOULD confirm that Markdown files are readable outside Obsidian.

The setup process SHOULD confirm that the document headers remain visible.

The setup process SHOULD confirm that section headings remain visible.

The setup process SHOULD confirm that file paths, warnings, restrictions, and setup instructions remain visible in plain text.

The setup process SHOULD confirm that Obsidian opens the selected vault boundary successfully.

The setup process SHOULD confirm that the selected Obsidian vault boundary is known.

The setup process SHOULD confirm that the selected Codex workspace boundary is known.

The setup process SHOULD confirm that Codex has not been given unnecessary access outside the task scope.

The setup process SHOULD confirm that optional plugins are absent, disabled, or reviewed before use.

The setup process SHOULD confirm that plugin behavior does not define governed meaning.

The setup process SHOULD confirm that generated files, cache files, index files, plugin files, and implementation-support files can be distinguished from governed documents.

The setup process SHOULD confirm that restricted material is not exposed unintentionally.

The setup process SHOULD confirm that backup expectations are understood before major work begins.

The setup process SHOULD confirm that synchronization is disabled, limited, or reviewed before use.

The setup process SHOULD confirm that recovery expectations are understood before the environment is relied on.

The setup process SHOULD confirm that controlled ingestion does not begin until setup checks pass.

A setup check MAY be documented in a task note, setup note, review note, implementation-support file, handoff summary, or future checklist.

A setup check SHOULD identify:

- what was checked;
- what file or folder was inspected;
- what result was found;
- what issue remains, if any;
- whether the issue blocks setup;
- whether human review is required;
- whether escalation is required;
- whether the environment may proceed to the next setup step.

A setup check MUST NOT silently approve a governed file.

A setup check MUST NOT silently change Lifecycle State.

A setup check MUST NOT silently change Authority Level.

A setup check MUST NOT silently change Privacy Classification.

A setup check MUST NOT silently change Validation State.

A setup check MUST NOT silently approve publication.

A setup check MUST NOT silently approve export.

A setup check MUST NOT silently approve migration.

A setup check MUST NOT silently approve synchronization.

A setup check MUST NOT silently approve indexing.

A setup check MUST NOT silently approve backup automation.

A setup check MUST NOT silently approve implementation exposure.

A setup check MUST NOT silently approve agent exposure.

A setup check MUST NOT silently approve downstream use.

If a first-use setup check fails, the failure SHOULD be documented.

A failed setup check SHOULD be corrected before normal use continues if the failure affects usability, portability, reviewability, traceability, privacy, validation, storage boundaries, workflow boundaries, agent boundaries, backup expectations, synchronization risk, recovery expectations, or downstream-use safety.

A failed setup check MAY be deferred only when the deferral is documented and does not create uncontrolled drift.

First-use setup checks are complete when:

- the repository exists locally;
- the repository root is known;
- the `brain-standard` folder is present;
- the `Standards` folder is present;
- the implementation-profile area is present;
- IMP-0001 is present;
- IMP-0002 is placed correctly;
- Obsidian can open the selected vault boundary;
- Markdown files remain readable outside Obsidian;
- Codex workspace scope is known;
- plugin status is known;
- generated files are distinguishable from governed files;
- restricted material is not unintentionally exposed;
- backup expectations are understood;
- synchronization cautions are understood;
- recovery expectations are understood;
- controlled ingestion may proceed only under the applicable workflow.

## 11. Backup and Recovery Expectations

Backup and recovery expectations define what the setup environment should understand before The Brain is relied on for practical use.

Backup means preserving a copy of governed files, Source Material, implementation-support files, or supporting context for restoration, continuity, archival, audit, migration, disaster recovery, or long-term preservation.

Recovery means restoring files, folders, repository history, supporting context, or a usable setup environment after deletion, corruption, loss, device failure, synchronization failure, migration failure, tool failure, agent error, user error, or other disruption.

IMP-0002 does not define an exact backup tool.

IMP-0002 does not define an exact backup schedule.

IMP-0002 does not define an exact recovery tool.

IMP-0002 does not define an exact disaster-recovery plan.

Those concerns may belong to future operational guides, backup specifications, recovery specifications, implementation-support files, deployment packages, or reference implementations.

However, the setup process SHOULD confirm that backup and recovery expectations are understood before serious use begins.

A setup environment SHOULD be backed up in a way that preserves:

- governed standards;
- Knowledge Records;
- Source Material where allowed;
- Source References;
- provenance context;
- metadata context;
- relationship context;
- validation context;
- workflow context;
- agent traceability context;
- implementation-support files where needed;
- templates where needed;
- scripts where needed;
- prompts where needed;
- validators where needed;
- handoff summaries where needed;
- setup notes where needed.

A backup SHOULD preserve enough structure for a future human, agent, workflow, or implementation to understand what was restored.

A backup SHOULD preserve folder layout where practical.

A backup SHOULD preserve filenames where practical.

A backup SHOULD preserve Markdown readability.

A backup SHOULD preserve repository history where practical.

A backup SHOULD preserve reviewability.

A backup SHOULD preserve traceability.

A backup SHOULD preserve privacy boundaries.

A backup SHOULD preserve source-reference and provenance context.

A backup SHOULD preserve generated-file distinction.

A backup SHOULD preserve implementation-support distinction.

A backup MUST NOT redefine governed meaning.

A backup MUST NOT become the source of Object Identity by itself.

A backup MUST NOT become the source of metadata meaning by itself.

A backup MUST NOT become the source of relationship meaning by itself.

A backup MUST NOT become the source of Lifecycle State, Authority Level, Privacy Classification, Validation State, publication readiness, export readiness, migration readiness, synchronization readiness, indexing readiness, implementation exposure, agent exposure, or downstream-use readiness by itself.

A backup copy SHOULD be distinguishable from the active working copy.

A backup copy SHOULD NOT be edited as if it were the active governed repository unless a recovery or migration process explicitly makes it active.

A backup copy SHOULD NOT be exposed to agents, synchronization tools, indexing tools, publication tools, export tools, or downstream-use environments without review.

A backup copy SHOULD NOT include restricted material unless the applicable Privacy Classification and workflow context allow that backup.

A backup copy SHOULD NOT be stored in a location that violates privacy, access, synchronization, retention, export, publication, or downstream-use limits.

A recovery process SHOULD be tested before the setup is treated as dependable.

A recovery test MAY be limited during early setup.

A limited recovery test MAY confirm that:

- a backup copy exists;
- a file can be restored;
- a folder can be restored;
- Markdown remains readable after restore;
- repository structure remains understandable after restore;
- document headers remain intact after restore;
- setup notes remain understandable after restore;
- generated files remain distinguishable after restore;
- restricted material remains protected after restore.

Recovery SHOULD NOT silently overwrite active governed files without review.

Recovery SHOULD NOT silently replace newer governed files with older files without review.

Recovery SHOULD NOT silently change lifecycle state, authority level, privacy classification, validation state, approval status, publication readiness, export readiness, migration readiness, synchronization readiness, indexing readiness, implementation exposure, agent exposure, or downstream-use readiness.

Recovery SHOULD preserve evidence of what was restored where practical.

A recovery action SHOULD be documented when it affects governed files, Source Material, metadata, relationships, Source References, provenance, validation, workflow state, agent output, implementation-support files, or downstream-use context.

Backup and recovery expectations are complete when:

- the user understands where the active repository is located;
- the user understands what should be backed up;
- the user understands what should not be backed up without review;
- the user understands where backups may be stored;
- the user understands that backup is not approval;
- the user understands that backup is not validation;
- the user understands that backup is not synchronization readiness;
- the user understands that backup is not export readiness;
- the user understands that backup is not downstream-use readiness;
- the user understands that recovery should not silently overwrite governed material;
- at least one practical backup path or future backup task is identified before serious use.

## 12. Synchronization Cautions

Synchronization cautions define how the setup environment should treat copying, mirroring, syncing, replicating, caching, or transmitting governed files across devices, repositories, vaults, services, tools, implementations, or environments.

Synchronization MAY improve portability and continuity.

Synchronization MAY help keep multiple machines aligned.

Synchronization MAY support backup, migration, handoff, review, or collaboration.

However, synchronization can create risk.

Synchronization can expose restricted material.

Synchronization can copy draft material into unintended locations.

Synchronization can duplicate generated files.

Synchronization can create conflicting versions.

Synchronization can overwrite active work.

Synchronization can preserve deleted material.

Synchronization can transmit Source Material outside its allowed boundary.

Synchronization can expose governed files to indexing, search, embedding, summarization, AI features, cloud processing, third-party tooling, or agent access.

Synchronization MUST NOT be treated as automatically safe.

Synchronization MUST NOT be treated as approval.

Synchronization MUST NOT be treated as validation.

Synchronization MUST NOT be treated as backup proof.

Synchronization MUST NOT be treated as export readiness.

Synchronization MUST NOT be treated as publication readiness.

Synchronization MUST NOT be treated as migration readiness.

Synchronization MUST NOT be treated as implementation-exposure readiness.

Synchronization MUST NOT be treated as agent-exposure readiness.

Synchronization MUST NOT be treated as downstream-use readiness.

A synchronization tool SHOULD be reviewed before being used with governed material.

A synchronization tool SHOULD be reviewed for:

- what files it copies;
- where files are copied;
- whether files are encrypted;
- whether files are indexed;
- whether files are cached;
- whether files are transmitted to a third party;
- whether files are exposed to AI features;
- whether files are exposed to search systems;
- whether files are exposed to collaboration features;
- whether deleted files are retained;
- whether version history is retained;
- whether conflicts are created;
- whether hidden files are synchronized;
- whether generated files are synchronized;
- whether plugin files are synchronized;
- whether restricted material is included.

The setup environment SHOULD NOT enable synchronization until the user understands the synchronization boundary.

The synchronization boundary SHOULD identify:

- source folder;
- destination folder;
- service or tool;
- device scope;
- account scope;
- repository scope;
- vault scope;
- file-type scope;
- generated-file scope;
- restricted-material scope;
- conflict behavior;
- deletion behavior;
- recovery behavior;
- privacy behavior.

Synchronization SHOULD NOT include secrets, credentials, private keys, tokens, passwords, unrelated personal records, or unrelated restricted material.

Synchronization SHOULD NOT include restricted Source Material unless the applicable Privacy Classification and workflow context allow synchronization.

Synchronization SHOULD NOT include generated files unless those files are safe, useful, distinguishable, and intentionally included.

Synchronization SHOULD NOT include cache files unless those files are safe, useful, distinguishable, and intentionally included.

Synchronization SHOULD NOT include plugin files unless those files are safe, useful, distinguishable, and intentionally included.

Synchronization SHOULD NOT include export files unless export readiness has been determined for the relevant scope.

Synchronization SHOULD NOT include publication files unless publication readiness has been determined for the relevant scope.

Synchronization SHOULD NOT include migration files unless migration readiness has been determined for the relevant scope.

Synchronization SHOULD NOT include downstream-use packages unless downstream-use readiness has been determined for the relevant scope.

If synchronization is used, conflicts SHOULD be reviewed before either version is deleted or overwritten.

A synchronization conflict SHOULD NOT be resolved by automatic overwrite when governed meaning, metadata, relationships, Source References, provenance, Lifecycle State, Authority Level, Privacy Classification, Validation, reviewability, approval, publication readiness, export readiness, migration readiness, or downstream use may be affected.

If synchronization creates duplicate files, duplicate handling SHOULD preserve Object Identity rules.

Duplicate filenames MUST NOT be treated as duplicate Knowledge Objects by themselves.

Duplicate paths MUST NOT be treated as duplicate Knowledge Objects by themselves.

Duplicate content SHOULD be reviewed under the applicable Object Identity and validation expectations before merging, deleting, or replacing files.

Synchronization SHOULD be disabled, limited, or delayed when the setup environment contains unresolved restricted material, unresolved generated-file handling, unresolved backup expectations, unresolved recovery expectations, unresolved Codex scope, unresolved plugin behavior, unresolved privacy classification, or unresolved workflow routing.

Synchronization cautions are complete when:

- the user understands whether synchronization is enabled;
- the user understands what synchronization tool or service is involved;
- the user understands what folder or repository is synchronized;
- the user understands whether restricted material is included;
- the user understands whether generated files are included;
- the user understands whether plugin files are included;
- the user understands whether cache files are included;
- the user understands whether conflicts may occur;
- the user understands that synchronization is not approval;
- the user understands that synchronization is not validation;
- the user understands that synchronization is not backup proof;
- the user understands that synchronization is not export readiness;
- the user understands that synchronization is not downstream-use readiness;
- synchronization does not begin unless the applicable boundary is understood.

## 13. Restricted Material Handling

Restricted material handling defines how the setup environment should identify, limit, protect, review, and avoid unintended exposure of governed material whose access or use may be constrained.

Restricted Material may include material affected by Privacy Classification, Source Reference limits, provenance limits, authority limits, lifecycle limits, validation limits, review limits, publication limits, export limits, synchronization limits, indexing limits, backup limits, implementation-exposure limits, agent-exposure limits, or downstream-use limits.

IMP-0002 does not define exact privacy values.

IMP-0002 does not define exact access-control roles.

IMP-0002 does not define exact encryption methods.

IMP-0002 does not define exact redaction methods.

IMP-0002 does not define exact restricted-material folders.

Those concerns may belong to future privacy specifications, access-control specifications, storage specifications, workflow specifications, operational guides, implementation-support files, or reference implementations.

However, the setup process MUST treat restricted material cautiously.

A setup environment SHOULD assume that incoming Source Material, private notes, exported files, generated summaries, agent outputs, plugin caches, search indexes, backups, and synchronized copies may contain restricted material until reviewed.

Restricted material SHOULD NOT be exposed merely because it is visible in the repository, vault, folder tree, file search, plugin output, cache, index, backup, export package, or Codex workspace.

Visibility does not equal permission.

File access does not equal permission.

Vault access does not equal permission.

Repository access does not equal permission.

Plugin access does not equal permission.

Search access does not equal permission.

Backup access does not equal permission.

Synchronization access does not equal permission.

Codex access does not equal permission.

A setup environment SHOULD identify where restricted material may appear.

Restricted material may appear in:

- Source Material;
- imported files;
- draft Knowledge Records;
- review notes;
- workflow logs;
- agent outputs;
- provenance notes;
- Source References;
- metadata notes;
- relationship notes;
- validation notes;
- operational notes;
- handoff summaries;
- generated files;
- cache files;
- index files;
- plugin files;
- export packages;
- backup copies;
- synchronized folders;
- migration packages;
- implementation-support files.

Restricted material SHOULD NOT be placed in a location that implies publication, export, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream-use readiness unless the applicable workflow has determined that readiness.

Restricted material SHOULD NOT be copied into examples, templates, test files, screenshots, prompts, generated summaries, validator output, handoff summaries, implementation notes, or downstream-use packages unless the applicable privacy boundary permits it.

Restricted material SHOULD NOT be used for plugin testing unless the plugin has been reviewed and the material is allowed for that exposure.

Restricted material SHOULD NOT be used for AI plugin testing unless agent exposure and implementation exposure have been reviewed.

Restricted material SHOULD NOT be used for Codex testing unless the task scope, permission scope, and privacy boundary permit Codex inspection.

Restricted material SHOULD NOT be indexed unless indexing readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be synchronized unless synchronization readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be backed up unless backup readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be exported unless export readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be published unless publication readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be migrated unless migration readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be exposed to agents unless agent-exposure readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be exposed to implementations unless implementation-exposure readiness has been determined for the relevant scope.

Restricted material SHOULD NOT be used downstream unless downstream-use readiness has been determined for the relevant scope.

If restricted material is discovered during setup, the setup process SHOULD pause the affected exposure path until the risk is reviewed.

An exposure path may include:

- Obsidian visibility;
- plugin visibility;
- Codex visibility;
- file search visibility;
- backup visibility;
- synchronization visibility;
- export visibility;
- publication visibility;
- indexing visibility;
- migration visibility;
- downstream-use visibility.

If restricted material has already been exposed unintentionally, the issue SHOULD be documented and escalated for review.

The setup process SHOULD preserve enough context to determine:

- what material was exposed;
- where the material was exposed;
- what tool or process exposed it;
- whether a plugin was involved;
- whether Codex was involved;
- whether synchronization was involved;
- whether backup was involved;
- whether indexing was involved;
- whether export was involved;
- whether publication was involved;
- whether migration was involved;
- whether downstream use occurred;
- whether remediation is required;
- whether human review is required.

Restricted material handling MUST NOT redefine Privacy Classification.

Restricted material handling MUST NOT replace privacy review.

Restricted material handling MUST NOT replace source-reference review.

Restricted material handling MUST NOT replace provenance review.

Restricted material handling MUST NOT replace validation.

Restricted material handling MUST NOT replace workflow approval.

Restricted material handling MUST NOT create publication, export, migration, synchronization, indexing, backup, implementation-exposure, agent-exposure, or downstream-use clearance by itself.

Restricted material handling is complete when:

- the setup environment recognizes that restricted material may exist;
- likely restricted-material locations are understood;
- restricted material has not been intentionally exposed without review;
- plugin exposure risk has been considered;
- Codex exposure risk has been considered;
- synchronization exposure risk has been considered;
- backup exposure risk has been considered;
- indexing exposure risk has been considered;
- export exposure risk has been considered;
- publication exposure risk has been considered;
- migration exposure risk has been considered;
- downstream-use exposure risk has been considered;
- unresolved restricted-material concerns are documented or escalated.

## 14. Generated File Handling

Generated file handling defines how the setup environment should identify, separate, review, preserve, ignore, delete, regenerate, or restrict files produced by tools, plugins, agents, scripts, validators, indexers, caches, exporters, synchronizers, backup tools, migration tools, or automation.

Generated files MAY support usability.

Generated files MAY support search.

Generated files MAY support indexing.

Generated files MAY support validation support.

Generated files MAY support export packaging.

Generated files MAY support backup.

Generated files MAY support review.

Generated files MAY support implementation behavior.

However, generated files MUST NOT be confused with governed documents unless a governed workflow or specification explicitly makes them governed.

Generated files may include:

- Obsidian configuration files;
- Obsidian workspace files;
- plugin configuration files;
- plugin output files;
- cache files;
- index files;
- search artifacts;
- graph artifacts;
- generated tables;
- generated summaries;
- generated reports;
- validator outputs;
- script outputs;
- exported files;
- migration packages;
- backup manifests;
- synchronization metadata;
- agent outputs;
- temporary files;
- logs;
- build artifacts;
- transformed copies;
- derived Markdown files;
- derived metadata files.

A generated file SHOULD be distinguishable from a governed standard.

A generated file SHOULD be distinguishable from a Knowledge Record.

A generated file SHOULD be distinguishable from Source Material.

A generated file SHOULD be distinguishable from a reviewed workflow output.

A generated file SHOULD be distinguishable from an approved export package.

A generated file SHOULD be distinguishable from an approved publication package.

A generated file SHOULD be distinguishable from an approved migration package.

A generated file SHOULD be distinguishable from an approved downstream-use package.

Generated files SHOULD be stored, named, labeled, or documented in a way that makes their generated nature clear.

Generated files SHOULD NOT be placed where they appear to be approved governed standards unless they have completed the applicable governance process.

Generated files SHOULD NOT be placed where they appear to be approved Knowledge Records unless they have completed the applicable workflow.

Generated files SHOULD NOT be placed where they appear to be preserved Source Material unless they are the actual Source Material or an explicitly governed derivative.

Generated files SHOULD NOT silently overwrite governed files.

Generated files SHOULD NOT silently replace Source Material.

Generated files SHOULD NOT silently replace Knowledge Records.

Generated files SHOULD NOT silently replace reviewed workflow outputs.

Generated files SHOULD NOT silently alter metadata.

Generated files SHOULD NOT silently alter relationships.

Generated files SHOULD NOT silently alter Source References.

Generated files SHOULD NOT silently alter provenance.

Generated files SHOULD NOT silently alter Lifecycle State.

Generated files SHOULD NOT silently alter Authority Level.

Generated files SHOULD NOT silently alter Privacy Classification.

Generated files SHOULD NOT silently alter Validation State.

Generated files SHOULD NOT silently create approval, publication readiness, export readiness, migration readiness, synchronization readiness, indexing readiness, backup readiness, implementation-exposure readiness, agent-exposure readiness, or downstream-use readiness.

Generated files may be regenerated.

Therefore, the setup environment SHOULD identify whether a generated file is:

- disposable;
- reproducible;
- required for local usability;
- required for review support;
- required for validation support;
- required for export support;
- required for backup support;
- required for recovery support;
- required for traceability;
- unsafe to expose;
- unsafe to synchronize;
- unsafe to index;
- unsafe to delete;
- safe to ignore.

Generated files that support traceability SHOULD be preserved when they record material agent activity, workflow activity, validation activity, review activity, export activity, publication activity, backup activity, migration activity, synchronization activity, implementation exposure, agent exposure, or downstream-use decisions.

Generated files that merely support local display MAY be ignored, deleted, excluded, regenerated, or left unmanaged if doing so does not affect governed meaning, reviewability, traceability, privacy, validation, recovery, or downstream use.

Generated files that contain restricted material SHOULD be treated as restricted material.

Generated files that contain summaries of restricted material SHOULD be treated as restricted material.

Generated files that contain extracted content from Source Material SHOULD preserve source-reference and provenance expectations where applicable.

Generated files that contain agent output SHOULD remain reviewable and traceable where the output affects governed meaning or governed handling.

Generated files created by plugins SHOULD be reviewed before being committed, synchronized, indexed, backed up, exported, published, migrated, exposed to agents, or used downstream.

Generated files created by Codex SHOULD be reviewed before being accepted as governed content.

Generated files created by validators SHOULD be treated as validation support unless a governed validation process records them as validation results.

Generated files created by export tools SHOULD be treated as export candidates unless export readiness has been determined.

Generated files created by backup tools SHOULD be treated as backup artifacts unless backup readiness has been determined.

Generated files created by migration tools SHOULD be treated as migration candidates unless migration readiness has been determined.

Generated files created by synchronization tools SHOULD be treated as synchronization artifacts unless synchronization readiness has been determined.

Generated file handling MUST preserve the distinction between active governed files and derived support files.

Generated file handling MUST preserve the distinction between setup support and standard meaning.

Generated file handling MUST preserve the distinction between convenience output and approval.

Generated file handling MUST preserve the distinction between generated summaries and Source Material.

Generated file handling MUST preserve the distinction between validator output and governed validation state.

Generated file handling is complete when:

- generated files can be identified;
- generated files are distinguishable from governed documents;
- generated files are distinguishable from Knowledge Records;
- generated files are distinguishable from Source Material;
- generated files do not silently redefine governed meaning;
- generated files do not silently replace governed files;
- generated files do not silently alter metadata, relationships, Source References, provenance, lifecycle, authority, privacy, or validation;
- generated files containing restricted material are treated as restricted material;
- generated files requiring traceability are preserved or routed appropriately;
- disposable generated files may be ignored, excluded, deleted, or regenerated without losing governed meaning;
- generated files do not create approval, publication readiness, export readiness, migration readiness, synchronization readiness, indexing readiness, backup readiness, implementation-exposure readiness, agent-exposure readiness, or downstream-use readiness by themselves.

## 15. Controlled Ingestion Readiness

Controlled ingestion readiness defines when the setup environment is prepared to begin receiving Source Material, captured information, notes, files, messages, records, datasets, media, observations, or other inputs through the governed ingestion workflow.

Controlled ingestion readiness does not mean that ingestion has occurred.

Controlled ingestion readiness does not mean that incoming material is approved.

Controlled ingestion readiness does not mean that incoming material is validated.

Controlled ingestion readiness does not mean that incoming material is safe for publication, export, migration, synchronization, indexing, backup, implementation exposure, agent exposure, or downstream use.

Controlled ingestion readiness means the setup environment can begin ingestion without immediately creating uncontrolled drift.

The setup environment SHOULD be ready for controlled ingestion only after:

- the repository exists locally;
- the repository root is known;
- the `brain-standard` folder is present;
- the `Standards` folder is present;
- the implementation-profile area is present;
- IMP-0001 is present;
- IMP-0002 is present;
- Obsidian can open the selected vault boundary;
- Markdown files remain readable outside Obsidian;
- Codex workspace scope is known;
- optional plugin behavior has been reviewed or limited;
- first-use setup checks have been performed;
- backup expectations are understood;
- synchronization cautions are understood;
- recovery expectations are understood;
- restricted-material handling is understood;
- generated-file handling is understood.

Controlled ingestion SHOULD occur through the applicable ingestion workflow.

Controlled ingestion SHOULD preserve the distinction between:

- Source Material;
- extracted content;
- draft Knowledge Records;
- approved Knowledge Records;
- rejected candidates;
- quarantined material;
- workflow outputs;
- generated files;
- implementation-support files;
- operational notes;
- handoff summaries.

Incoming material SHOULD be staged before it is treated as governed knowledge.

Incoming material SHOULD be assessed before it is treated as a Knowledge Record.

Incoming material SHOULD preserve Source References where applicable.

Incoming material SHOULD preserve provenance where applicable.

Incoming material SHOULD preserve or receive metadata where applicable.

Incoming material SHOULD receive relationship review where applicable.

Incoming material SHOULD receive Lifecycle State review where applicable.

Incoming material SHOULD receive Authority Level review where applicable.

Incoming material SHOULD receive Privacy Classification review where applicable.

Incoming material SHOULD receive Validation review where applicable.

Incoming material SHOULD receive human review where required.

Incoming material SHOULD receive agent review only where the applicable permission boundary allows agent participation.

Controlled ingestion MUST NOT treat capture as approval.

Controlled ingestion MUST NOT treat storage as approval.

Controlled ingestion MUST NOT treat indexing as approval.

Controlled ingestion MUST NOT treat summarization as approval.

Controlled ingestion MUST NOT treat Codex output as approval.

Controlled ingestion MUST NOT treat Obsidian visibility as approval.

Controlled ingestion MUST NOT treat folder placement as Lifecycle State.

Controlled ingestion MUST NOT treat folder placement as Authority Level.

Controlled ingestion MUST NOT treat folder placement as Privacy Classification.

Controlled ingestion MUST NOT treat folder placement as Validation State.

Controlled ingestion MUST NOT treat a generated summary as Source Material.

Controlled ingestion MUST NOT treat an agent draft as an approved Knowledge Record.

Controlled ingestion MUST NOT treat a plugin-generated file as a governed Knowledge Record without workflow review.

Controlled ingestion MUST NOT treat a handoff summary as an approved standard unless it has been converted into a governed document through the appropriate process.

Controlled ingestion SHOULD begin with a small, reviewable intake batch where practical.

A small intake batch helps confirm that:

- source preservation works;
- draft creation is understandable;
- metadata expectations are clear enough for the stage;
- Source References can be captured;
- provenance can be preserved;
- privacy handling is understood;
- validation expectations are visible;
- review routing is possible;
- Codex assistance remains bounded;
- Obsidian navigation remains useful;
- generated files remain distinguishable;
- synchronization does not create uncontrolled exposure;
- backup expectations remain practical;
- downstream-use limits remain clear.

If controlled ingestion reveals a setup problem, ingestion SHOULD pause or narrow until the problem is repaired, documented, escalated, or accepted as a bounded non-conformance.

A setup problem may include:

- missing folders;
- unclear repository root;
- incorrect vault boundary;
- unclear Codex workspace scope;
- plugin behavior that changes files unexpectedly;
- generated files that appear governed;
- restricted material exposure;
- synchronization conflict;
- backup uncertainty;
- recovery uncertainty;
- unclear Source Material placement;
- unclear Knowledge Record placement;
- unclear workflow routing;
- unclear review responsibility;
- unclear validation expectation;
- unclear downstream-use boundary.

Controlled ingestion readiness is complete when:

- setup checks have passed or bounded exceptions are documented;
- Source Material can be staged without becoming approved knowledge automatically;
- draft Knowledge Records can be created without being mistaken for approved records;
- Codex assistance can occur within bounded permissions;
- Obsidian can support human review without becoming authority;
- plugin behavior does not define governed meaning;
- restricted material is not exposed without review;
- generated files remain distinguishable from governed files;
- backup expectations are understood;
- synchronization cautions are understood;
- recovery expectations are understood;
- ingestion can proceed through the applicable workflow;
- downstream-use readiness remains separate from ingestion readiness.

IMP-0002 is complete when Sections 1 through 15 provide a repeatable setup path for preparing the Obsidian and Codex implementation environment while preserving implementation independence, storage boundaries, agent boundaries, workflow boundaries, privacy boundaries, validation expectations, reviewability, portability, and controlled-ingestion readiness.