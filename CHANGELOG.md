# Changelog

## EKC 2025 (v2025.0.0) — 2026-02-18

All notable changes to this project will be documented in this file.

This project follows:
- Semantic Versioning (SemVer) for releases (e.g., v2025.0.0)
- Year label for scholarly communication (e.g., "EKC 2025")

## [Unreleased]
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

## [v2025.0.0] - 2025-09-18 — EKC 2025 (Major Release)
### Added
- SHACL shapes: `ekc-shapes.ttl` for core constraints.
- Wikidata alignment annotations (`schema:sameAs` / `wdt:*` mapping notes).
- Multilingual labels (ko/en) expanded for key classes and properties.
- New documentation: `docs/migration-2022a2507-to-2025.md`.

### Changed
- Reorganized class hierarchy for `ekc:Event` and `ekc:Agent`.
- Normalized naming conventions (camelCase for properties; PascalCase for classes).
- Improved ontology metadata: `owl:versionIRI`, `owl:versionInfo`, `dcterms:issued`.

### Deprecated
- `ekc:hasPeriod` (use `ekc:hasTimeSpan` instead).
- `ekc:Scholar` (use `ekc:Researcher` instead).

### Removed
- (none)

### Fixed
- Cardinality inconsistencies detected by SHACL validation.
- Typos in rdfs:label / skos:definition (ko/en).

### Security
- (none)

### Migration Notes
- See `docs/migration-2022a2507-to-2025.md`.
- Legacy terms remain resolvable for compatibility, but are not maintained.

---

## [v2022-alpha2507] - 2025-08-03 — EKC 2022.α2507 (Archived)
### Notes
- This version is archived and no longer maintained.
- Preserved for reproducibility and stable scholarly citation.
