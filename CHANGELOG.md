# Changelog

All notable changes to this project will be documented in this file.

This project follows:
- Year label for scholarly communication (e.g., "EKC 2025")
- Semantic Versioning (SemVer) for releases (e.g., v2025.0.0)

## Evidence for ontology-header dates / 온톨로지 헤더 날짜의 공개 근거(검증 경로)

- (KR) 본 CHANGELOG의 각 릴리즈 제목 줄에 쓰인 “Primary 날짜(YYYY-MM-DD)”는, 해당 버전 TTL의 ontology header에 기록된 `dcterms:issued` / `dcterms:modified` 값(= export timestamp)을 기준으로 한다.
- (EN) The “Primary date” in each release header is derived from `dcterms:issued` / `dcterms:modified` in the TTL ontology header.
- (KR) 위 날짜의 **공개된 근거(원문 TTL/스냅샷)** 는 아래 폴더에서 확인 가능:
  - `./version_history/` (link: [./version_history/](./version_history/))
  - `./snapshots/` (link: [./snapshots/](./snapshots/))
- (EN) Public evidence (raw TTL snapshots) is available under:
  - `./version_history/` (link: [./version_history/](./version_history/))
  - `./snapshots/` (link: [./snapshots/](./snapshots/))
- (KR/EN) How to verify: open the relevant TTL snapshot and search for `dcterms:issued` and `dcterms:modified`.

---

## EKC 2025 [v2025.1.17] — 2026-04-15 (Patch: core-line cleanup + derivative-scope separation)

- Revised ontology documentation and release documentation for the EKC 2025 line.
- Updated ontology-header date serialization and selected annotation-property declarations.
- Simplified EKC-local overlays for identity/mapping predicates in order to keep the core EKC TTL leaner.
- Clarified the practical separation between the **core EKC ontology line** and derivative/project-local extension handling.

### Overview

EKC 2025 [v2025.1.17]은 EKC 2025 [v2025.1.0]의 핵심 스키마 구조를 유지하면서, (1) ontology header 날짜 literal의 표현을 `xsd:date` 중심으로 정리하고, (2) `dcterms:issued` 및 `dcterms:modified`의 annotation-property range를 `rdfs:Literal`로 조정하며, (3) `owl:sameAs` 및 `skos:*Match` 계열에 대한 EKC 내부의 로컬 설명 블록을 축약·정리한 패치 릴리즈이다. 이 변화는 의미론적 엄밀성을 포기한 것이 아니라, **EKC 본체(core)** 와 **파생·로컬 확장 계열** 의 역할을 더 분명하게 나누기 위한 정리로 이해해야 한다. @ko

### Changed — Ontology header / publication metadata

- `owl:versionInfo` updated to `EKC 2025 [v2025.1.17]`.
- `dcterms:issued` literal changed from `xsd:dateTime` to `xsd:date` while preserving the same calendar-date basis.
- `dcterms:modified` updated to the v2025.1.17 patch date and changed from `xsd:dateTime` to `xsd:date`.
- `dcterms:issued` and `dcterms:modified` annotation-property ranges were relaxed from `xsd:dateTime` to `rdfs:Literal`.
- Added `rdfs:label "See also"@en` to `rdfs:seeAlso`.
- Added `rdfs:label "contact point"@en` to `dcat:contactPoint`.
- Added explicit datatype declaration: `xsd:date rdf:type rdfs:Datatype`.

### Changed — Identity / mapping presentation in the EKC core line

- `owl:sameAs` remains available in EKC, but its local descriptive block was simplified.
- The local `owl:TransitiveProperty` typing on `owl:sameAs` was removed.
- Local redeclaration/documentation blocks for `skos:mappingRelation`, `skos:exactMatch`, and `skos:closeMatch` were removed from the published EKC TTL.

### Interpretation note — EKC core vs derivative extension line

- `v2025.1.17` should be read as a cleanup of what is embedded directly in the **EKC core TTL**.
- More project-local or derivative-level extension logic—especially stronger local usage guidance for mapping predicates or other extension-oriented semantic policy—may be maintained in a separate derivative ontology line rather than in EKC itself.
- In that sense, this release clarifies **where** certain guidance belongs, rather than weakening the project’s semantic discipline.

### Serialization / editorial cleanup

- EKC term declarations are now serialized with explicit `ekc:` prefix notation instead of relying mainly on the local default `:` form.
- This is a notation/serialization cleanup only; EKC IRIs themselves are unchanged.

### Compatibility

- No changes to the core class set.
- No EKC namespace IRI change.
- No newly introduced EKC classes.
- No newly introduced EKC object properties.
- Existing data/queries should remain broadly compatible unless they depend on:
  - ontology-header date typing as `xsd:dateTime` only,
  - local EKC-side documentation blocks for `skos:mappingRelation`, `skos:exactMatch`, `skos:closeMatch`,
  - the earlier stricter local wording and transitive typing attached to `owl:sameAs`.

### Migration Notes

- If a pipeline validates ontology-header dates strictly as `xsd:dateTime`, update it to accept `xsd:date` or literal-based handling at the annotation layer.
- If a workflow relied on EKC-local explanatory overlays for mapping predicates, review whether that policy should instead be maintained in derivative documentation or in a derivative ontology line.
- If documentation or training material quoted the earlier stricter EKC-local explanation of `owl:sameAs`, update that explanation accordingly.

### Documentation

- **Detailed dossier:** [`docs/changes/v2025.1.17-ontology-revision.md`](https://github.com/dongshins/EKC_ontology/blob/main/docs/changes/v2025.1.17-ontology-revision.md)

### Links

- Release: [`v2025.1.17`](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.17)
- Compare: [`v2025.1.0...v2025.1.17`](https://github.com/dongshins/EKC_ontology/compare/v2025.1.0...v2025.1.17)

---

## EKC 2025 [v2025.1.0] — 2026-03-13 (Patch: linking/mapping + metadata policy)

- Revised ontology documentation and release documentation for the EKC 2025 line.
- Updated repository metadata and release preparation materials for GitHub and Zenodo.
- Refined explanatory texts concerning ontology structure, documentation policy, and versioned release handling.

### Overview

EKC 2025 [v2025.1.0]은 EKC 2025 [v2025.0.0]의 핵심 스키마 구조를 유지하면서, (1) ontology header 메타데이터를 정규화하고, (2) 외부 링크/매핑(`owl:sameAs` vs `skos:*Match`)의 사용 규칙을 명문화하며, (3) `dc:*`와 `dcterms:*` 메타데이터 프로퍼티의 운용 원칙을 보강한 패치 릴리즈이다. @ko

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

`v2025.1.0` is maintained as the current release of the `ekc-2025` ontology line.

Accordingly, `ekc_2025_1_0.ttl` retains the existing metadata structure:
- `owl:versionIRI` → `http://dh.aks.ac.kr/ontologies/ekc-2025`
- `dcterms:replaces` → `http://dh.aks.ac.kr/ontologies/ekc-2022-alpha2507`
- `owl:priorVersion` → `http://dh.aks.ac.kr/ontologies/ekc-2022-alpha2507`

### Compatibility

- No changes to the core class set.
- No datatype-property changes.
- Existing data/queries should remain broadly compatible unless they depend on ontology-header literals or exact header IRI forms.

### Migration Notes

- If any pipeline relied on ontology-header `dcterms:contributor` literal values, update it to refer to repository documentation (`README.md`, `CONTRIBUTORS.md`) instead.
- If any rule depended on exact `http` / `https` distinction in version lineage IRIs, review that logic.

### Documentation

- **Detailed dossier:** [`docs/changes/v2025.1.0-ontology-revision.md`](https://github.com/dongshins/EKC_ontology/blob/main/docs/changes/v2025.1.0-ontology-revision.md)

### Links

- Release: [`v2025.1.0`](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.1.0)
- Compare: [`v2025.0.0...v2025.1.0`](https://github.com/dongshins/EKC_ontology/compare/v2025.0.0...v2025.1.0)

---

## EKC 2025 [v2025.0.0] — 2026-02-18 (Major Release, Archived)

### Overview

EKC 2025는 EKC 온톨로지를 “버전 고정·인용 가능(citable)한 OWL/RDF 배포물”로 정식화하기 위해, 온톨로지 헤더(발행 메타데이터/버전 계통)를 강화한 릴리즈이다. (스키마의 Class/ObjectProperty 구성은 EKC 2022.α2507과 호환 범위 내에서 유지됨.) @ko

### Changed — Ontology header / publication metadata

- Explicit versioning added/curated:
  - `owl:versionIRI` (version IRI 고정)
  - `owl:priorVersion` (이전 버전 명시)
  - `owl:versionInfo` (`"EKC 2025"`)
- Publication & provenance fields added/updated:
  - `dcterms:issued`, `dcterms:modified` (릴리즈 시각으로 정규화)
  - `dcterms:publisher`, `dcterms:license` (라이선스/발행 주체 명시)
  - `dcterms:replaces` (대상 교체 버전 명시)
- Credits & citation readiness:
  - `dcterms:contributor`에 기여자(21명) literal 목록 반영
  - `dc:creator`에 기관 IRI + 다국어 literal 병기
  - `dc:title`(EN/KO) 정비
- Documentation string improved:
  - `rdfs:comment`(EN) 확장
- Consistency:
  - 위 메타데이터 용어들을 `owl:AnnotationProperty`로 명시

### Links

- Release: [`v2025.0.0`](https://github.com/dongshins/EKC_ontology/releases/tag/v2025.0.0)
