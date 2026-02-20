# Changelog

All notable changes to this project will be documented in this file.

This project follows:
- Year label for scholarly communication (e.g., "EKC 2025")
- Semantic Versioning (SemVer) for releases (e.g., v2025.0.0)
<!--  
## [Unreleased]
### Breaking Changes
- Renamed terms (IRIs changed):
  - `ekc:Scholar` → `ekc:Researcher`
  - `ekc:hasPeriod` → `ekc:hasTimeSpan`
- Restructured hierarchy:
  - `ekc:Event` subclasses reorganized (some moved under new intermediate classes).
- Domain/Range tightened for several properties (may break permissive legacy data).

### Migration Guide
If your dataset uses EKC 2022.α2507, apply the following mapping:

| EKC 2022.α2507 | EKC 2025 | Action |
|---|---|---|
| `ekc:Scholar` | `ekc:Researcher` | replace IRI |
| `ekc:hasPeriod` | `ekc:hasTimeSpan` | replace property |
| `ekc:hasAffiliation` (range: Literal) | `ekc:hasAffiliation` (range: Organization) | refactor values |

### Added
- (planned) Alignment to additional external vocabularies.
### Changed
- (planned) Improve documentation and examples.
### Deprecated
- (planned) Some legacy terms to be deprecated.
### Removed
- (planned) Terms to be removed after deprecation period.
### Fixed
- (planned) Validation fixes based on SHACL checks.

---
-->
## EKC 2025 [v2025.0.0] — 2026-02-18 (Major Release)

### Overview
EKC 2025 completes a versioned, citable release workflow for the EKC ontology.
It builds on the standards-based RDF/OWL distribution and LOV registration milestone established in EKC 2022.α2507,
and formalizes explicit ontology version metadata for reproducible reuse.
<!--
### Added
- SHACL shapes: `ekc-shapes.ttl` for core constraints.
- Wikidata alignment annotations (`schema:sameAs` / `wdt:*` mapping notes).
- Multilingual labels (ko/en) expanded for key classes and properties.
- New documentation: `docs/migration-2022a2507-to-2025.md`.
-->
### Changed
- Publication metadata improved (e.g., `owl:versionIRI`, `owl:versionInfo`, issuance date).
- Packaging/documentation improved to support stable scholarly citation and reproducibility.
<!--
- Reorganized class hierarchy for `ekc:Event` and `ekc:Agent`.
//- Normalized naming conventions (camelCase for properties; PascalCase for classes).
//- Improved ontology metadata: `owl:versionIRI`, `owl:versionInfo`, `dcterms:issued`.

//- Publication metadata updated (e.g., `owl:versionIRI`, `owl:versionInfo`, issuance date).
--><!--
### Deprecated
- `ekc:hasPeriod` (use `ekc:hasTimeSpan` instead).
- `ekc:Scholar` (use `ekc:Researcher` instead).
--><!--
### Removed
- (none)
--><!--
### Fixed
- Cardinality inconsistencies detected by SHACL validation.
- Typos in rdfs:label / skos:definition (ko/en).
--><!--
### Security
- (none)
--><!--
### Migration Notes
- See `docs/migration-2022a2507-to-2025.md`.
- Legacy terms remain resolvable for compatibility, but are not maintained.
-->
---

## EKC 2022.α2507 [v2022-alpha2507] - 2025-08-03 (Archived)
### Notes
- This version is archived and no longer maintained.
- Preserved for reproducibility and stable scholarly citation.
