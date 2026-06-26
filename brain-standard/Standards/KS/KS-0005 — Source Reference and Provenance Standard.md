# KS-0005 — Source Reference and Provenance Standard

Document ID: KS-0005
Title: Source Reference and Provenance Standard
Version: 0.1.0
Status: Draft
Created: 2026-06-26
Last Updated: 2026-06-26
Authority: Standard
Phase: Phase 1 — Universal Knowledge Standard
Milestone: 1.5 — Source Reference and Provenance Standard
Depends On: TB-0000 — Vision and Purpose; TB-0001 — Architecture Principles; TB-0002 — Layered Architecture; TB-0003 — Governance Model; KS-0001 — Knowledge Object Model; KS-0002 — Object Identity Standard; KS-0003 — Metadata Standard; KS-0004 — Relationship Standard
Supersedes: None
Superseded By: None
Related: None

## Normative Language

The words SHALL, MUST, SHOULD, MAY, and RECOMMENDED are interpreted consistently throughout The Brain Standard.

- SHALL / MUST means a mandatory requirement.
- SHOULD means a strong recommendation.
- MAY means an optional implementation choice.

These terms define how requirements, recommendations, permissions, constraints, and source-reference and provenance rules are interpreted within KS-0005.

Where conflicts arise between Source Material, Source References, provenance, evidence, attribution, extraction history, transformation history, source availability, source reliability, source authority, source privacy, source validation, source compatibility, Object Identity, metadata, relationships, lifecycle state, authority, privacy classification, storage behavior, agents, workflows, implementations, import behavior, export behavior, migration behavior, or future specifications, the constitutional foundation SHALL guide interpretation and resolution.

KS-0005 is subordinate to TB-0000, TB-0001, TB-0002, and TB-0003.

KS-0005 extends KS-0001 by defining standard-level source-reference and provenance behavior for Knowledge Objects, Knowledge Records, Source Material, relationships, standards, decisions, workflows, agents, implementations, and other governed entities.

KS-0005 depends on KS-0002 because source references and provenance may rely on stable Object Identity, source identifiers, alternate identifiers, legacy identifiers, migration identifiers, import identifiers, export identifiers, and identity-change records.

KS-0005 depends on KS-0003 because source-reference and provenance meaning may be expressed, described, validated, reviewed, migrated, imported, exported, governed, or preserved through metadata.

KS-0005 depends on KS-0004 because relationships may connect Knowledge Objects, Knowledge Records, Source Material, evidence, provenance records, validation records, workflows, agents, implementations, and other governed entities.

If KS-0005 appears to conflict with a constitutional document, the constitutional document takes precedence unless the constitutional document is formally revised through governance.

If KS-0005 appears to conflict with KS-0001, the conflict SHOULD be resolved by preserving the Knowledge Object Model defined in KS-0001 while applying KS-0005 as the more specific standard for Source Reference and Provenance behavior.

If KS-0005 appears to conflict with KS-0002, the conflict SHOULD be resolved by preserving stable Object Identity while applying KS-0005 as the more specific standard for source-reference and provenance interpretation, review, validation, and compatibility.

If KS-0005 appears to conflict with KS-0003, the conflict SHOULD be resolved by preserving metadata role boundaries while applying KS-0005 as the more specific standard for source-reference and provenance behavior.

If KS-0005 appears to conflict with KS-0004, the conflict SHOULD be resolved by preserving relationship behavior while applying KS-0005 as the more specific standard for source support, evidence, attribution, provenance, and source-reference interpretation.

KS-0005 defines Source References and Provenance at the conceptual standard level.

KS-0005 does not define exact citation syntax, exact Markdown front matter syntax, exact metadata field names, exact source-reference schemas, exact database structures, exact API behavior, exact storage paths, exact source archive structure, exact validation tooling, exact citation style, exact bibliography format, exact import format, exact export format, exact migration format, or implementation-specific source-link behavior.

Those concerns belong to later specifications, storage standards, agent standards, workflow standards, implementation profiles, validation specifications, source-reference vocabularies, citation specifications, archival specifications, and operational documents.

## Terminology

Throughout this document:

- The Brain refers to the overall project and ecosystem.
- The Brain Standard refers to the implementation-independent architectural standard defined by the project.
- Knowledge Operating System or KOS refers to the role fulfilled by The Brain Standard as a durable foundation for organizing, preserving, navigating, and automating knowledge.
- Universal Knowledge Standard refers to Layer 1 of The Brain Standard, responsible for defining knowledge meaning, Object Identity, metadata, relationships, provenance, lifecycle, authority, privacy, validation, and interpretation.
- Knowledge Object refers to a discrete unit of structured knowledge managed under The Brain Standard.
- Knowledge Record refers to a structured representation of knowledge created from, about, or in response to Source Material, human reasoning, agent activity, or governed workflows.
- Source Material refers to original files, documents, messages, images, recordings, datasets, web pages, transcripts, scans, code files, logs, forms, physical artifacts, external references, or other artifacts used as evidence, input, origin, context, attribution, or reference material.
- Source Reference refers to a traceable reference from a Knowledge Object, Knowledge Record, relationship, decision, workflow, validation result, or other governed entity to Source Material that supports, explains, contextualizes, contradicts, originated, or otherwise relates to the governed entity.
- Provenance refers to information that identifies the origin, source, reasoning, transformation, creator, editor, agent, workflow, migration, import, export, validation, review, evidence, or change context associated with a Knowledge Object, Knowledge Record, Source Reference, relationship, decision, or other governed entity.
- Evidence refers to Source Material, extracted content, cited material, observation, validation result, relationship, reasoning record, or other support used to justify, explain, verify, challenge, or contextualize a Knowledge Object, Knowledge Record, claim, relationship, decision, classification, or interpretation.
- Attribution refers to information identifying the person, organization, system, source, author, creator, publisher, agent, workflow, or implementation associated with the creation, publication, modification, extraction, transformation, interpretation, or transmission of Source Material or governed knowledge.
- Source Identifier refers to an identifier associated with Source Material rather than with the Knowledge Object itself.
- Source Availability refers to whether Source Material is available, unavailable, restricted, moved, missing, deleted, corrupted, archived, superseded, externally hosted, partially available, or otherwise limited for review, validation, migration, import, export, preservation, or downstream use.
- Source Reliability refers to the assessed trustworthiness, quality, uncertainty, freshness, completeness, bias concern, limitation, conflict, review concern, or evidentiary strength of Source Material.
- Source Authority refers to the governance weight, interpretive relevance, official status, review status, or approved use assigned to Source Material within a particular context.
- Source Privacy refers to the privacy classification, visibility boundary, access expectation, redaction requirement, disclosure limitation, or handling rule associated with Source Material, Source References, evidence, attribution, provenance, or extracted content.
- Source Validation refers to the process of checking whether Source Material, Source References, evidence, attribution, provenance, extraction history, transformation history, availability status, reliability notes, privacy expectations, and compatibility expectations satisfy the applicable standards or specifications.
- Source Compatibility refers to whether Source Material, Source References, evidence, attribution, and provenance remain meaningful, portable, reviewable, privacy-respecting, and interpretable across migration, import, export, storage replacement, workflow activity, agent activity, validation, and implementation replacement.
- Extraction refers to the process of selecting, copying, transcribing, parsing, summarizing, segmenting, or otherwise taking information from Source Material for use in a Knowledge Record, relationship, validation result, workflow output, agent output, or other governed entity.
- Transformation refers to the process of changing Source Material, extracted content, or prior knowledge into another representation, summary, translation, classification, interpretation, structured record, derived object, migrated form, or implementation-specific representation.
- Source-Derived Knowledge refers to Knowledge Objects, Knowledge Records, relationships, classifications, summaries, interpretations, or decisions created from, about, or in response to Source Material.
- Human-Created Provenance refers to provenance created, recorded, reviewed, corrected, approved, rejected, or maintained by a human.
- Agent-Generated Provenance refers to provenance created, proposed, modified, enriched, validated, extracted, classified, summarized, or inferred by an agent.
- Workflow-Generated Provenance refers to provenance created, proposed, modified, enriched, validated, extracted, classified, summarized, routed, approved, rejected, or preserved through a governed workflow.
- Import Provenance refers to provenance associated with bringing Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, or external content into a compliant environment.
- Export Provenance refers to provenance associated with producing Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, or external content from a compliant environment for use elsewhere.
- Migration Provenance refers to provenance associated with moving, converting, mapping, preserving, transforming, validating, or reviewing Knowledge Objects, Knowledge Records, Source Material, Source References, metadata, relationships, evidence, or identifiers across systems, formats, repositories, vaults, implementations, standards versions, or storage environments.
- Citation refers to a human-readable, publication-oriented, academic, legal, technical, or external reference form that may identify Source Material. A citation may support a Source Reference, but citation syntax does not define Source Reference behavior by itself.
- External Reference refers to a reference to material, identifiers, systems, records, publications, URLs, datasets, databases, repositories, or artifacts outside the immediate compliant environment.
- Object Identity refers to the stable identity of a Knowledge Object independent of filename, folder path, storage location, application-specific identifier, user interface, or implementation.
- Metadata refers to explicit descriptive, structural, governance, lifecycle, privacy, provenance, relationship, validation, compatibility, source-reference, or operational context associated with a Knowledge Object, Knowledge Record, Source Material, relationship, or governed entity.
- Relationship refers to an explicit connection between Knowledge Objects, Knowledge Records, Source Material, standards, decisions, workflows, implementations, identifiers, or other governed entities.
- Lifecycle State refers to the current governed state of a Knowledge Object, Knowledge Record, Source Reference, provenance record, relationship, or governed entity.
- Authority Level refers to the governance weight, review status, or interpretive authority assigned to a document, Knowledge Object, Knowledge Record, relationship, source, decision, or governed entity.
- Privacy Classification refers to explicit metadata describing permitted visibility, access, exposure, routing, publication, synchronization, indexing, export, backup, agent access, or handling expectations.
- Validation refers to the process of checking whether a Knowledge Object, Knowledge Record, Source Material, Source Reference, provenance record, relationship, or governed entity satisfies the applicable standards, specifications, metadata expectations, provenance expectations, lifecycle expectations, privacy expectations, compatibility expectations, or implementation boundaries.
- Implementation refers to any software, vault, database, file system, interface, agent system, workflow environment, or tool that realizes The Brain Standard in practice.
