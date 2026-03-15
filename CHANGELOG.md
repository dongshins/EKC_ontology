# Changelog

All notable changes to this project will be documented in this file.

This project follows:
- Year label for scholarly communication (e.g., "EKC 2025")
- Semantic Versioning (SemVer) for releases (e.g., v2025.0.0)

## Evidence for ontology-header dates / 온톨로지 헤더 날짜의 공개 근거(검증 경로)

- (KR) 본 CHANGELOG의 각 릴리즈 제목 줄에 쓰인 “Primary 날짜(YYYY-MM-DD)”는, 해당 버전 TTL의 ontology header에 기록된 `dcterms:issued`/`dcterms:modified` 값(= export timestamp)을 기준으로 한다.
- (EN) The “Primary date” in each release header is derived from `dcterms:issued`/`dcterms:modified` in the TTL ontology header.

- (KR) 위 날짜의 **공개된 근거(원문 TTL/스냅샷)는** 아래 폴더에서 확인 가능:
  - `./version_history/`  (link: [./version_history/](./version_history/))
  - `./snapshots/`       (link: [./snapshots/](./snapshots/))
- (EN) Public evidence (raw TTL snapshots) is available under:
  - `./version_history/` (link: [./version_history/](./version_history/))
  - `./snapshots/`       (link: [./snapshots/](./snapshots/))

- (KR/EN) How to verify: open the relevant TTL snapshot and search for `dcterms:issued` and `dcterms:modified`.
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
<!--
### Deprecated
- (planned) Some legacy terms to be deprecated.
### Removed
- (planned) Terms to be removed after deprecation period.
### Fixed
- (planned) Validation fixes based on SHACL checks.
-->
---

## EKC 2025 [v2025.1.0] — 2026-03-13 (Patch: linking/mapping + metadata policy)

- Revised ontology documentation and release documentation for the EKC 2025 line.
- Updated repository metadata and release preparation materials for GitHub and Zenodo.
- Refined explanatory texts concerning ontology structure, documentation policy, and versioned release handling.

### Overview
EKC 2025 [v2025.1.0]은 EKC 2025 [v2025.0.0]의 핵심 스키마 구조를 유지하면서,
(1) ontology header 메타데이터를 정규화하고,
(2) 외부 링크/매핑(`owl:sameAs` vs `skos:*Match`)의 사용 규칙을 명문화하며,
(3) `dc:*`와 `dcterms:*` 메타데이터 프로퍼티의 운용 원칙을 보강한 패치 릴리즈이다. @ko

### Changed — Ontology header / publication metadata
- `owl:versionInfo` updated to `EKC 2025 [v2025.1.0]`.
- `dcterms:issued` normalized to the release date basis.
- `dcterms:modified` updated to reflect the v2025.1.0 patch date.
- `owl:priorVersion` IRI normalized for consistency.
- Added `dc:publisher` (EN/KO literals) and `dcat:contactPoint`.
- The ontology-header literal list formerly recorded in `dcterms:contributor` was removed. 

### Changed — Linking / mapping guidance
- Clarified the strict use of `owl:sameAs` for identity-level equivalence only.
- Added/curated `skos:mappingRelation`, `skos:exactMatch`, and `skos:closeMatch` for external vocabulary alignment.
- Clarified the policy that `dcterms:*` is used for **resource-valued** metadata, while `dc:*` is used for **annotation-style literal/IRI text**. 

### Versioning clarification

`v2025.1.0` is maintained as the current release of the `ekc-2025` ontology line. Accordingly, `ekc_2025_1_0.ttl` retains the existing metadata structure:

- `owl:versionIRI` → `http://dh.aks.ac.kr/ontologies/ekc-2025`
- `dcterms:replaces` → `http://dh.aks.ac.kr/ontologies/ekc-2022-alpha2507`
- `owl:priorVersion` → `http://dh.aks.ac.kr/ontologies/ekc-2022-alpha2507`

### Compatibility
- No changes to the core class set.
- No datatype-property changes.
- Existing data/queries should remain broadly compatible unless they depend on ontology-header literals or exact header IRI forms. 

### Migration Notes
- If any pipeline relied on ontology-header `dcterms:contributor` literal values, update it to refer to repository documentation (`README.md`, `CONTRIBUTORS.md`) instead. 
- If any rule depended on exact `http`/`https` distinction in version lineage IRIs, review that logic. 

### Documentation 
- **Detailed dossier:** [`docs/changes/v2025.1.0-ontology-revision.md`](https://github.com/dongshins/EKC_ontology/docs/changes/v2025.1.0-ontology-revision.md) <!--(**continuously updated with incremental additions**)--> 

### Links
- Release: [`v2025.1.0`](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.0) 
- Compare: [`v2025.0.0...v2025.1.0`](https://github.com/dongshins/EKC_ontology/compare/v2025.0.0...v2025.1.0)
<!-- - Release: TBD (Release 생성 후 링크로 교체); [EKC 2025 [v2025.1.0] – Minor Ontology Release](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.0) -->
<!-- - Release: TBD (To Be Determined; 추후 결정. Release 생성 후 링크로 교체) --> 
<!-- - Release: TBD (Release 생성 후 링크로 교체)--> 
<!-- - Release: https://github.com/dongshins/EKC_ontology/releases/tag/v2025.0.0-->
<!-- - Compare: TBD (예: `v2022-alpha2507...v2025.0.0`)-->
<!-- - Compare: https://github.com/dongshins/EKC_ontology/compare/v2022-alpha2507...v2025.0.0-->

---

## EKC 2025 [v2025.0.0] — 2026-02-18 (Major Release, Archived)

### Overview
EKC 2025는 EKC 온톨로지를 “버전 고정·인용 가능(citable)한 OWL/RDF 배포물”로 정식화하기 위해,
온톨로지 헤더(발행 메타데이터/버전 계통)를 강화한 릴리즈이다.
(스키마의 Class/ObjectProperty 구성은 EKC 2022.α2507과 호환 범위 내에서 유지됨.) @ko 
<!--EKC 2025 completes a versioned, citable release workflow for the EKC ontology.
It builds on the standards-based RDF/OWL distribution and LOV registration milestone established in EKC 2022.α2507,
and formalizes explicit ontology version metadata (e.g., `owl:versionIRI`) for reproducible reuse.
--> 
<!--
### Added
- SHACL shapes: `ekc-shapes.ttl` for core constraints.
- Wikidata alignment annotations (`schema:sameAs` / `wdt:*` mapping notes).
- Multilingual labels (ko/en) expanded for key classes and properties.
- New documentation: `docs/migration-2022a2507-to-2025.md`.
-->
### Changed — Ontology header / publication metadata (첨부 TTL 비교 근거)
- Explicit versioning added/curated:
  - `owl:versionIRI` (version IRI 고정)
  - `owl:priorVersion` (이전 버전 명시)
  - `owl:versionInfo` ("EKC 2025")
- Publication & provenance fields added/updated:
  - `dcterms:issued`, `dcterms:modified` (릴리즈 시각으로 정규화)
  - `dcterms:publisher`, `dcterms:license` (라이선스/발행 주체 명시)
  - `dcterms:replaces` (대상 교체 버전 명시)
- Credits & citation readiness:
  - `dcterms:contributor`에 기여자(21명) literal 목록을 반영
  - `dc:creator`에 기관 IRI + 다국어 literal 병기(출판 메타데이터 일관성)
  - `dc:title`(EN/KO) 정비(학술 인용용 타이틀)
- Documentation string improved:
  - `rdfs:comment`(EN) 확장(프로젝트 설명/범위 명시)
- Consistency:
  - 위 메타데이터 용어들을 `owl:AnnotationProperty`로 명시(헤더/주석 체계 정합성)
- **상세사항은 아래 Documentation 참조**.
<!--### Changed
- Publication metadata improved (e.g., `owl:versionIRI`, `owl:versionInfo`, issuance date).
- Packaging/documentation improved to support stable scholarly citation and reproducibility.
-->
<!--
- Reorganized class hierarchy for `ekc:Event` and `ekc:Agent`.
//- Normalized naming conventions (camelCase for properties; PascalCase for classes).
//- Improved ontology metadata: `owl:versionIRI`, `owl:versionInfo`, `dcterms:issued`.

//- Publication metadata updated (e.g., `owl:versionIRI`, `owl:versionInfo`, issuance date).
-->
<!--
### Deprecated
- `ekc:hasPeriod` (use `ekc:hasTimeSpan` instead).
- `ekc:Scholar` (use `ekc:Researcher` instead).
-->
<!--
### Removed
- (none)
-->
<!--
### Fixed
- Cardinality inconsistencies detected by SHACL validation.
- Typos in rdfs:label / skos:definition (ko/en).
-->
<!--
### Security
- (none)
-->
### Compatibility
- EKC 2022.α2507 대비 “스키마(클래스/오브젝트프로퍼티 집합) 변경”은 최소/없음.
- (주의) 메타데이터 필드 기반으로 파이프라인을 구성한 경우,
  versionIRI/issued/modified/license/publisher 반영에 맞춰 수집·인용 규칙만 업데이트 권장.

### Migration Notes
- SPARQL 패턴 자체는 대체로 영향이 없으나,
  (1) ontology header 메타데이터를 이용한 필터링/검증을 하는 경우,
  (2) 버전 IRI를 인용하기로 할 경우에는 본 릴리즈의 헤더를 기준으로 재정렬 필요.
<!-- - See this Changelog entry and related docs for notes on upgrading from EKC 2022.α2507.--> 
<!--
- See `docs/migration-2022a2507-to-2025.md`.
- Legacy terms remain resolvable for compatibility, but are not maintained.
-->
### Documentation 
- **Detailed dossier:** [`docs/changes/v2025.0.0-ontology-revision.md`](https://github.com/dongshins/EKC_ontology/docs/changes/v2025.0.0-ontology-revision.md) (**continuously updated with incremental additions**) 
<!-- - **Detailed dossier:** `docs/changes/v2025.0.0-ontology-revision.md` (continuously expanded via incremental addenda)--> 
<!-- - **Detailed dossier:** `docs/changes/v2025.0.0-ontology-revision.md`--> 
<!-- - **Detailed dossier:** `docs/changes/v2025.0.0-ontology-revision.md` (continuously updated with incremental additions) --> 
<!--//### References
//- **Details:** docs/changes/v2025.0.0-ontology-revision.md
-->
### Links
- Release: [EKC 2025 [v2025.0.0] – Major Ontology Release](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.0.0) 
- Compare: [`v2022-alpha2507...v2025.0.0`](https://github.com/dongshins/EKC_ontology/compare/v2022-alpha2507...v2025.0.0)
<!-- - Release: TBD (To Be Determined; 추후 결정. Release 생성 후 링크로 교체) --> 
<!-- - Release: TBD (Release 생성 후 링크로 교체)--> 
<!-- - Release: https://github.com/dongshins/EKC_ontology/releases/tag/v2025.0.0-->
<!-- - Compare: TBD (예: `v2022-alpha2507...v2025.0.0`)-->
<!-- - Compare: https://github.com/dongshins/EKC_ontology/compare/v2022-alpha2507...v2025.0.0-->

---

## EKC 2022.α2507 [v2022-alpha2507] — 2025-07-27 (Archived)

### Major Publication & Distribution Changes
- **Wiki → standards-based artifacts:** Consolidated the previously wiki-style EKC ontology documentation into machine-readable OWL/RDF deliverables (e.g., Turtle), authored and maintained in Protégé.
- **Korean Studies milestone (LOV):** Registered EKC in **Linked Open Vocabularies (LOV)** (added 2025-08-03), improving global discoverability and reuse in the Linked Data ecosystem.
- **Community note:** To the best of our knowledge, EKC is among the earliest Korean Studies–focused vocabularies registered in LOV.
<!-- - **Registry milestone (LOV):** Registered EKC in **Linked Open Vocabularies (LOV)** to improve global discoverability and reuse in the Linked Data ecosystem.--> 
<!-- - **Korean Studies milestone (LOV):** Registered EKC in **Linked Open Vocabularies (LOV)** (added 2025-08-03), improving global discoverability and reuse.--> 
<!-- - **Community note:** (To our knowledge) among the earliest LOV registrations of a Korean Studies–focused vocabulary.-->
### Changed — Ontology documentation re-encoded (Wiki → Turtle) with standards/consistency review
- Re-encoded wiki-style ontology documentation into RDF 1.1 Turtle and normalized serialization.
- Reviewed and revised ontology header/versioning (ontology IRI, versionIRI, imports, metadata).
- Harmonized IRIs, labels, and annotations; clarified definitions and provenance notes.
- Strengthened OWL modeling consistency (typing, domain/range, disjointness/equivalence, restrictions) and removed contradictions.
- Migration notes: 일부 용어 IRI/라벨 정비로 SPARQL 패턴 수정 필요.
- **상세사항은 아래 Documentation 참조**.
<!-- - Migration notes: 일부 용어 IRI/라벨 정비로 SPARQL 패턴 수정 필요. 상세는 아래 문서 참조.--> 
<!--
**Details:** docs/changes/v2022-alpha2507-ontology-revision.md  
**Diff:** https://github.com/dongshins/EKC_ontology/compare/v2022.%CE%B12507...v2022-alpha2507
[: compare 링크(태그A...태그B) ] 
--> 
### Documentation 
- **Detailed dossier:** `docs/releases/v2022-alpha2507.md` (**continuously expanded via incremental addenda**) 
<!-- - **Detailed dossier:** `docs/releases/v2022-alpha2507.md` (continuously expanded via incremental addenda) --> 

### References
- Wiki documentation (EKC 2022): https://dh.aks.ac.kr/~hanyang2/wiki/index.php/Ontology:EKC_2022
- LOV entry (ekc): https://lov.linkeddata.es/dataset/lov/vocabs/ekc

### Links
- Release: [EKC Ontology v2022.α2507 using Protégé](https://github.com/dongshins/EKC_ontology/releases/tag/v2022-alpha2507)

### Notes
- This version is archived and no longer maintained.
- The label "EKC 2022.α2507" denotes the 2022-series snapshot; the GitHub archiving/release record was created on 2025-07-27.
- Preserved for reproducibility, legacy dataset compatibility, and stable scholarly citation.
<!-- - Preserved for reproducibility and stable scholarly citation. --> 
